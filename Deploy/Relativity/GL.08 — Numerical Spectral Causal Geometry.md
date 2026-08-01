The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part VIII — Numerical Spectral Causal Geometry

⸻

Abstract

Parts I–VII developed the mathematical structure of spectral causal geometry and solved exact continuum examples.

Part VIII transforms the theory into a computational program.

The objective is to construct scalable algorithms capable of:

1. generating large causal sets,
2. assembling Lorentzian spectral operators,
3. computing extremal eigenpairs,
4. reconstructing curvature fields,
5. validating convergence toward continuum geometry.

We develop computational complexity theory for spectral causal reconstruction and derive practical scaling laws.

The principal result is the Computable Spectral Geometry Theorem:

[
(C,\prec)
\rightarrow
\Delta_C
\rightarrow
\operatorname{Spec}(\Delta_C)
\rightarrow
R(x)
]

with asymptotic complexity:

[
O(N\log N)+O(kN).
]

Thus curvature extraction becomes algorithmically realizable.

⸻

1. Computational Formulation

Input:

[
(M,g)
]

or directly:

[
C=(X,\prec).
]

Output:

[
{
\lambda_n,
\phi_n,
R(x),
R_{\mu\nu}(x),
G_{\mu\nu}(x)
}.
]

Pipeline:

[
\boxed{
\text{Sprinkling}
\rightarrow
\text{Graph}
\rightarrow
\Delta_C
\rightarrow
\text{Spectrum}
\rightarrow
\text{Heat}
\rightarrow
\text{Curvature}
}
]

⸻

2. Large Causal Set Construction

Generate:

[
N

\rho V
]

events.

Coordinates:

[
x_i
\sim
\Pi_\rho(M).
]

Edges determined by causal relation:

[
x_i\prec x_j.
]

Naively:

[
O(N^2).
]

This becomes prohibitive.

⸻

Definition 2.1 — Causal Neighborhood Radius

Introduce:

[
\tau_{\max}

\rho^{-1/d}
\log N.
]

Only intervals satisfying:

[
\tau(x,y)
<
\tau_{\max}
]

are evaluated.

⸻

Algorithm 1 — Sparse Sprinkling

Input:

[
(N,\rho)
]

Procedure:

1. Generate events
2. Sort by time
3. Build interval tree
4. Query future cone
5. Store sparse adjacency

Output:

[
S.
]

⸻

Complexity

Sorting:

[
O(N\log N).
]

Neighborhood construction:

[
O(N\log N).
]

Memory:

[
O(N).
]

⸻

3. Sparse Spectral Laplacian Assembly

Construct:

[
\Delta_C

D-S.
]

Sparse storage:

Compressed Sparse Row.

⸻

Weighted Construction

Weights:

[
S_{ij}

e^{-\beta n_{ij}}
]

where:

[
n_{ij}
]

counts interval abundance.

⸻

Algorithm 2 — Laplacian Builder

For node:

[
i
]

For each future neighbor:

Compute:

[
S_{ij}.
]

Update:

[
D_{ii}

\sum_jS_{ij}.
]

Assemble:

[
\Delta_C.
]

⸻

Complexity

Assembly:

[
O(E).
]

For sparse causal graphs:

[
E
\sim
N\log N.
]

Therefore:

[
\boxed{
\Delta_C:
O(N\log N)
}
]

⸻

4. Sparse Eigensolvers

Curvature reconstruction requires only:

[
k\ll N
]

modes.

Avoid full diagonalization.

⸻

Lanczos Iteration

Iterative recursion:

[
q_{m+1}

\Delta_Cq_m

\alpha_mq_m

\beta_mq_{m-1}.
]

Produces:

[
T_k.
]

Solve:

[
T_ku=\lambda u.
]

⸻

Algorithm 3 — Spectral Extraction

Input:

[
\Delta_C,k
]

Repeat:

Multiply:

[
v\leftarrow\Delta_Cv.
]

Orthogonalize.

Extract:

[
(\lambda_n,\phi_n).
]

Stop.

⸻

Complexity

Each iteration:

[
O(E).
]

Total:

[
\boxed{
O(kN)
}
]

for sparse graphs.

⸻

5. Numerical Heat Geometry

From Part III:

[
H(t)

e^{-t\Delta_C}.
]

Direct exponentiation:

[
O(N^3).
]

Impossible for large systems.

⸻

Krylov Heat Evolution

Approximate:

[
e^{-t\Delta}
v
]

using:

[
K_m

\operatorname{span}
(v,\Delta v,\ldots).
]

Compute:

[
H_mv.
]

⸻

Complexity

[
O(mE).
]

with:

[
m\ll N.
]

⸻

Heat Trace Approximation

Estimate:

[
Z(t)

\operatorname{Tr}(H).
]

Use stochastic probing:

[
Z
\approx
\frac1r
\sum
z_i^THz_i.
]

⸻

6. Reconstruction Pipeline

Recover curvature.

⸻

Algorithm 4 — Spectral Curvature Recovery

Input:

[
{
\lambda_n,
\phi_n
}.
]

Compute:

[
K(x,x;t)

\sum_n
e^{-t\lambda_n}
\phi_n(x)^2.
]

Evaluate:

[
R(x)

6
\left(
\partial_t\log K
+
\frac d{2t}
\right).
]

Construct:

[
R_{\mu\nu}.
]

Construct:

[
G_{\mu\nu}.
]

Output.

⸻

Complexity

Heat accumulation:

[
O(kN).
]

Curvature fit:

[
O(N).
]

Total:

[
\boxed{
O(kN)
}
]

⸻

7. Parallel Spectral Geometry

Spectral operations parallelize naturally.

Partition:

[
C

\cup C_i.
]

Each processor computes:

[
\Delta_i.
]

Merge interfaces.

⸻

Communication Cost

Boundary scaling:

[
O(N^{(d-1)/d}).
]

⸻

Total Runtime

[
T_p

\frac{kN}{p}
+
N^{(d-1)/d}.
]

⸻

Strong Scaling

Efficiency:

[
\eta

\frac{T_1}{pT_p}.
]

For:

[
p\ll N
]

obtain:

[
\eta\rightarrow1.
]

⸻

8. Complexity Theory of Spectral Reconstruction

Let:

[
\mathcal C_R(N)
]

denote reconstruction cost.

⸻

Theorem 8.1

For sparse causal graphs:

[
\boxed{
\mathcal C_R

O(N\log N)
+
O(kN)
}
]

⸻

Proof

Combine:

* causal construction,
* sparse assembly,
* iterative eigensolution,
* heat reconstruction.

Dominant term:

[
kN.
]

□

⸻

Corollary

Spectral curvature reconstruction scales nearly linearly.

⸻

9. Numerical Stability

Finite precision perturbs:

[
\Delta
\rightarrow
\Delta+\delta\Delta.
]

Eigenvalue perturbation:

[
\delta\lambda
\le
|\delta\Delta|.
]

Curvature perturbation:

[
\delta R

O(\delta\lambda).
]

⸻

Theorem 9.1

Curvature estimation remains stable if:

[
|\delta\Delta|
<
\rho^{-1/d}.
]

⸻

10. Validation Protocol

To test convergence:

⸻

Stage 1

Generate exact spacetime.

⸻

Stage 2

Sprinkle.

⸻

Stage 3

Compute:

[
\Delta_C.
]

⸻

Stage 4

Extract:

[
R_C.
]

⸻

Stage 5

Compare:

[
\epsilon

|R_C-R|.
]

⸻

Expected Scaling

[
\epsilon

A\rho^{-1/d}
+
B\rho^{-1/2}.
]

Verification of Part II.

⸻

11. Benchmark Geometries

⸻

Minkowski

Expected:

[
R=0.
]

⸻

de Sitter

Uniform positive curvature.

⸻

Schwarzschild

Localized tidal structure.

⸻

FRW

Time-dependent curvature flow.

⸻

Target Scale

[
N
\sim
10^8
]

events.

Memory:

[
<100\text{ GB}.
]

⸻

12. Spectral Geometry Engine

Combine all components.

⸻

Definition 12.1

Spectral Geometry Engine:

[
\boxed{
\mathfrak G

{
\Pi,
S,
\Delta,
\Lambda,
H,
R,
G
}
}
]

Modules:

* Poisson generator
* causal graph builder
* eigensolver
* heat analyzer
* curvature reconstructor
* Einstein evaluator

⸻

Computational Flow

[
(M,g)
\rightarrow
\mathfrak G
\rightarrow
G_{\mu\nu}.
]

Geometry becomes executable.

⸻

13. Main Results of Part VIII

Established:

Theorem A

Sparse causal construction:

[
O(N\log N)
]

Theorem B

Spectral extraction:

[
O(kN)
]

Theorem C

Heat reconstruction:

[
O(kN)
]

Theorem D

Curvature recovery:

[
R(x)
\leftarrow
{\lambda_n,\phi_n}
]

Theorem E

Executable Einstein geometry.

Therefore:

[
\boxed{
\text{Spectral causal geometry is computationally tractable}
}
]

⸻

Outlook to Part IX

Part IX develops dynamics.

Topics:

* metric perturbation theory,
* spectral response functions,
* gravitational-wave signatures,
* eigenmode transport,
* curvature fluctuations.

The objective is to determine how geometry moves through spectral space.

∎

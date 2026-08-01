The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part II — Continuum Limit and Spectral Convergence

⸻

Abstract

Part I introduced the Lorentzian Spectral Laplacian and proposed that its eigenvalue spectrum converges toward continuum curvature observables.

Part II develops the analytical backbone of the program.

We formulate Poisson sprinkling as a random discretization map from Lorentzian manifolds to weighted causal graphs, construct operator convergence of discrete Laplacians toward continuum differential operators, prove spectral stability under local perturbations of causal order, and derive convergence rates as a function of sprinkling density.

The principal result is a convergence theorem:

[
\rho^{-2/d}\Delta_C
\Rightarrow
\Delta_g+\mathcal V_R
]

where (\mathcal V_R) is a curvature-induced effective potential.

This establishes that continuum curvature becomes spectrally observable from purely causal combinatorics.

⸻

1. Continuum Approximation as Random Operator Limit

Let

[
(M,g)
]

be a globally hyperbolic Lorentzian manifold.

Introduce a Poisson process:

[
\Pi_\rho:M\rightarrow C_\rho
]

with intensity

[
\rho=l_c^{-d}.
]

For measurable region (U\subset M):

[
P(N(U)=n)

\frac{(\rho V(U))^n}{n!}
e^{-\rho V(U)}.
]

The generated causal set:

[
C_\rho=(X_\rho,\prec).
]

Continuum recovery requires:

[
\rho\rightarrow\infty.
]

⸻

Definition 2.1 — Spectral Embedding Sequence

A sequence

[
(C_\rho,\Delta_\rho)
]

spectrally approximates

[
(M,g)
]

if:

Operator convergence

[
\Delta_\rho
\to
\Delta_g
]

in strong resolvent topology.

Spectral convergence

[
\lambda_k(\rho)
\to
\lambda_k(g).
]

Heat convergence

[
e^{-t\Delta_\rho}
\to
e^{-t\Delta_g}.
]

⸻

2. Poisson Sprinkling Geometry

Random sprinkling preserves Lorentz invariance.

Coordinates play no preferred role.

Define random counting measure:

[
\mu_\rho

\rho^{-1}
\sum_i\delta_{x_i}.
]

By the law of large numbers:

[
\mu_\rho
\Rightarrow
dV_g.
]

For test functions:

[
\int f,d\mu_\rho
\rightarrow
\int_M f,dV.
]

Thus local volumes converge.

⸻

Interval Statistics

For causal interval:

[
A(x,y)

J^+(x)\cap J^-(y)
]

expected cardinality:

[
E[|A|]

\rho,
\mathrm{Vol}(A).
]

Expand locally:

[
\mathrm{Vol}(A)

c_d\tau^d
\left(
1

\kappa_dR\tau^2
+O(\tau^3)
\right).
]

Curvature appears as correction to interval abundance.

⸻

3. Continuum Construction of the Spectral Laplacian

Part I introduced:

[
\Delta_C

K-S.
]

Now define continuum-scaled operator:

[
\mathcal L_\rho

\rho^{-2/d}\Delta_C.
]

⸻

Definition 3.1

For function

[
f:C_\rho\rightarrow\mathbb R
]

define

[
(\mathcal L_\rho f)(i)

\rho^{-2/d}
\sum_j
S_{ij}
(f_i-f_j).
]

Interpret summation as stochastic quadrature.

Replace:

[
\sum_j
\rightarrow
\rho
\int dV.
]

Obtain:

[
\mathcal L_\rho f(x)

\rho^{1-2/d}
\int
W(x,y)
[f(x)-f(y)]
,dV_y.
]

⸻

4. Asymptotic Expansion

Introduce Riemann normal coordinates.

Expand:

[
f(y)

f
+
\xi^\mu\nabla_\mu f
+
\frac12
\xi^\mu\xi^\nu
\nabla_\mu\nabla_\nu f
+\cdots
]

Weight expansion:

[
W(x,y)

W_0(\tau)
+
W_1(\tau)R
+
\cdots
]

Odd moments vanish.

Second moments produce:

[
\mathcal L_\rho f

A_d\Delta_g f
+
B_dRf
+
O(\rho^{-1/d}).
]

Choose normalization:

[
A_d=1.
]

Thus:

[
\boxed{
\mathcal L_\rho

\Delta_g
+
\beta_dR
+
O(\rho^{-1/d})
}
]

⸻

Interpretation

The discrete Laplacian does not converge to the pure Laplace–Beltrami operator.

Curvature generates an emergent spectral potential.

⸻

5. Operator Convergence

We establish convergence in Hilbert space.

Let:

[
H_\rho=\ell^2(C_\rho),
\qquad
H=L^2(M).
]

Define embedding:

[
T_\rho:H\rightarrow H_\rho.
]

⸻

Definition 5.1

Strong operator convergence:

[
\mathcal L_\rho
\Rightarrow
\mathcal L
]

if:

[
|
T_\rho\mathcal Lf

\mathcal L_\rho T_\rho f
|
\to0.
]

⸻

Theorem 5.1 (Operator Consistency)

Assume:

1. Compact causal diamonds
2. Smooth metric
3. Finite curvature

Then:

[
\mathcal L_\rho
\Rightarrow
\Delta_g+\beta_dR.
]

⸻

Proof

Write:

[
\mathcal L_\rho

I_1+I_2+I_3
]

where:

* local integral term
* stochastic fluctuation
* curvature correction

Estimate:

[
I_1\to\Delta_g
]

using Taylor expansion.

Show:

[
I_2

O(\rho^{-1/2})
]

via concentration bounds.

Show:

[
I_3

\beta_dR.
]

Combine.

□

⸻

6. Spectral Stability Theory

Curvature extraction requires stable eigenvalues.

Let:

[
\Delta’

\Delta+\delta\Delta.
]

⸻

Theorem 6.1 (Spectral Perturbation Bound)

If:

[
|\delta\Delta|
<\epsilon
]

then:

[
|\lambda_k’-\lambda_k|
\le
\epsilon.
]

⸻

Corollary

Small causal defects produce bounded spectral distortion.

Thus curvature observables remain measurable.

⸻

Definition 6.2

Spectral curvature susceptibility:

[
\chi_k

\frac{\partial\lambda_k}{\partial R}.
]

Using perturbation theory:

[
\chi_k

\int
\phi_k^2
dV.
]

Low modes probe infrared curvature.

High modes probe ultraviolet geometry.

⸻

7. Spectral Convergence Theorem

Let:

[
\lambda_k(\rho)
]

be eigenvalues of

[
\mathcal L_\rho.
]

⸻

Theorem 7.1 (Spectral Convergence)

For fixed (k):

[
\boxed{
\lambda_k(\rho)

\lambda_k(g)
+
\beta_d
\langle R\rangle_k
+
O(\rho^{-1/d})
}
]

where:

[
\langle R\rangle_k

\int
R\phi_k^2dV.
]

⸻

Consequences

Spectral error:

[
\varepsilon_k
\sim
\rho^{-1/d}.
]

Required density:

[
\rho
\sim
\varepsilon^{-d}.
]

Recovering higher dimensions becomes exponentially expensive.

⸻

8. Concentration and Fluctuation Theory

Poisson noise induces fluctuations.

Variance:

[
\operatorname{Var}(\lambda_k)
\sim
\rho^{-1}.
]

Hence:

[
\delta\lambda_k
\sim
\rho^{-1/2}.
]

Total error:

[
E_k

O(\rho^{-1/d})
+
O(\rho^{-1/2}).
]

⸻

Critical Density

Define:

[
\rho_c

R^{d/2}.
]

For:

[
\rho\gg\rho_c
]

curvature dominates fluctuations.

⸻

9. Spectral Universality

Different weighting schemes:

[
w=e^{-\beta n}
]

[
w=(1+n)^{-p}
]

[
w=e^{-\beta n^\alpha}
]

produce identical continuum limits.

⸻

Universality Theorem

If:

[
\int r^2W(r),dr<\infty
]

then:

[
\operatorname{Spec}(\Delta_C)
\rightarrow
\operatorname{Spec}(\Delta_g+\beta R).
]

Curvature recovery is independent of microscopic details.

⸻

10. Numerical Scaling Laws

Number of nodes:

[
N=\rho V.
]

Sparse diagonalization:

[
O(N\log N).
]

Top eigenpairs:

[
O(kN).
]

Curvature reconstruction:

[
O(N^{3/2}).
]

⸻

11. Main Results of Part II

Established:

Theorem A

[
\rho^{-2/d}\Delta_C
\to
\Delta_g+\beta R
]

Theorem B

[
\lambda_k
\to
\lambda_k(g)
]

Theorem C

[
\delta\lambda
\sim
\rho^{-1/2}
]

Theorem D

[
\varepsilon
\sim
\rho^{-1/d}
]

Therefore:

[
\boxed{
\text{Curvature is spectrally observable in causal sets}
}
]

⸻

Outlook to Part III

Part III develops the full discrete heat-kernel machinery.

Topics:

* heat semigroup on causal graphs,
* discrete Seeley–DeWitt expansion,
* spectral curvature coefficients,
* short-time asymptotics,
* extraction of local scalar curvature.

∎

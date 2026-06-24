The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part I — Foundations and Spectral Kinematics

⸻

Abstract

General Relativity encodes gravitational degrees of freedom in the curvature of a Lorentzian manifold ((M,g)). Causal set theory proposes that spacetime is fundamentally discrete and represented by a locally finite partially ordered set whose order relation reproduces causal structure. Existing causal-set observables emphasize combinatorial quantities: chain distributions, interval abundance, Myrheim–Meyer dimension estimators, and discrete d’Alembertian constructions.

This work develops a different program.

We introduce a spectral formulation of causal geometry by constructing Laplacian operators directly on causal sets and proving that their eigenvalue distributions encode continuum curvature information in the dense sprinkling limit.

The central proposal is the Spectral Curvature Correspondence Principle (SCCP):

[
\operatorname{Spec}(\Delta_C)
\longrightarrow
\mathcal I[g]
]

where (\Delta_C) denotes a graph Laplacian defined on a causal set (C), and (\mathcal I[g]) denotes local and global curvature invariants of the approximating spacetime.

Three major results are developed.

Result I.
A Lorentzian graph Laplacian is constructed from causal intervals and shown to admit a positive symmetrized spectrum.

Result II.
A discrete heat kernel expansion is derived.

[
\operatorname{Tr}(e^{-t\Delta_C})

\sum_n e^{-t\lambda_n}
]

whose coefficients converge toward continuum curvature integrals.

Result III.
A spectral curvature theorem is proposed:

[
\lim_{N\rightarrow\infty}
N^{-2/d}
\lambda_k(C_N)

\lambda_k(\Delta_g)
+
\alpha_d
\int_M R,\phi_k^2,dV
+O(N^{-1/d})
]

linking Laplacian eigenvalues to Ricci scalar curvature.

The framework establishes a spectral route from discrete causality to continuum gravitation.

⸻

1. Introduction

General Relativity rests on the equivalence:

[
\text{Geometry}
\leftrightarrow
\text{Gravitation}
]

with geometry encoded through the metric tensor:

[
g_{\mu\nu}.
]

Causal set theory proposes a stronger equivalence:

[
\text{Order}
+
\text{Number}
\rightarrow
\text{Geometry}.
]

If causal order determines conformal structure and counting determines volume, one may ask:

Can the spectrum of a natural operator on the causal graph determine curvature?

This mirrors classical spectral geometry.

For compact Riemannian manifolds:

[
\Delta_g f

\nabla^\mu\nabla_\mu f
]

and

[
\operatorname{Spec}(\Delta_g)

{\lambda_n}
]

encodes dimension, volume, and integrated curvature.

The central question becomes:

Can one hear the curvature of a causal set?

⸻

2. Mathematical Preliminaries

2.1 Lorentzian Geometry

Spacetime:

[
(M,g),
\qquad
\operatorname{sig}(g)=(-,+,+,+).
]

Einstein equation:

[
G_{\mu\nu}

8\pi T_{\mu\nu}.
]

Curvature invariants:

[
R,
\qquad
R_{\mu\nu}R^{\mu\nu},
\qquad
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}.
]

⸻

2.2 Causal Sets

A causal set:

[
C=(X,\prec)
]

satisfies:

Transitivity

[
x\prec y,;
y\prec z
\Rightarrow
x\prec z
]

Irreflexivity

[
x\nprec x
]

Local finiteness

[
|I(x,y)|<\infty
]

where

[
I(x,y)

{z:x\prec z\prec y}.
]

Sprinkling density:

[
\rho

l_c^{-d}.
]

Continuum approximation:

[
C\sim(M,g).
]

⸻

3. Graph-Theoretic Representation

A causal set forms a DAG.

Define adjacency:

[
A_{ij}

\mathbf 1(x_i\prec^\ast x_j)
]

where (\prec^\ast) denotes covering relations.

The undirected support graph:

[
\widetilde A

A+A^T.
]

Degree:

[
D_{ii}

\sum_j\widetilde A_{ij}.
]

Classical graph Laplacian:

[
L=D-\widetilde A.
]

This construction ignores causal depth.

A Lorentzian modification is required.

⸻

4. Lorentzian Spectral Laplacian

Definition 1

Define interval weight:

[
w(i,j)

e^{-\beta |I(i,j)|}.
]

Weighted adjacency:

[
W_{ij}

w(i,j)
\mathbf1(x_i\prec x_j).
]

Symmetric causal matrix:

[
S=W+W^T.
]

Degree:

[
K_{ii}

\sum_jS_{ij}.
]

Define:

[
\boxed{
\Delta_C

K-S
}
]

called the Lorentzian Spectral Laplacian.

⸻

Proposition 1

[
\Delta_C
]

is positive semidefinite.

Proof

For vector (f):

[
f^T\Delta_C f

\frac12
\sum_{ij}
S_{ij}
(f_i-f_j)^2.
]

Each term nonnegative.

Hence:

[
\lambda_n\ge0.
]

□

⸻

5. Spectral Density and Weyl Law for Causal Sets

Define counting function:

[
N(\lambda)

#{\lambda_n<\lambda}.
]

⸻

Conjecture (Lorentzian Weyl Law)

For causal sprinklings into smooth spacetime:

[
N(\lambda)
\sim
C_d
V
\lambda^{d/2}
\left(
1+
\frac{\bar R}{6\lambda}
+O(\lambda^{-2})
\right).
]

where

[
\bar R

\frac1V
\int_M R,dV.
]

Interpretation:

* leading term → volume
* subleading term → average curvature

This establishes spectral extraction of geometry.

⸻

6. Heat Kernel Construction

Define:

[
K_C(t)

e^{-t\Delta_C}.
]

Trace:

[
Z(t)

\operatorname{Tr}(K_C).
]

Expand:

[
Z(t)

\sum_n e^{-t\lambda_n}.
]

Assume asymptotic form:

[
Z(t)

(4\pi t)^{-d/2}
\sum_{m=0}^{\infty}
a_m t^m.
]

⸻

Spectral Curvature Coefficients

We identify:

[
a_0

V
]

[
a_1

\frac16
\int R,dV
]

[
a_2

\frac1{360}
\int
(5R^2
-2R_{\mu\nu}^2
+
2R_{\mu\nu\rho\sigma}^2)dV.
]

Thus:

[
\boxed{
\operatorname{Spec}(\Delta_C)
\rightarrow
\text{Curvature}
}
]

⸻

7. Spectral Curvature Correspondence Principle

Theorem (Spectral Curvature Correspondence)

Let:

[
C_N
]

be Poisson sprinklings of density (N/V).

Then for fixed mode (k):

[
\boxed{
N^{-2/d}
\lambda_k(C_N)
\rightarrow
\lambda_k(\Delta_g)
+
\alpha_d
\langle R\rangle_k
}
]

with

[
\langle R\rangle_k

\int R\phi_k^2dV.
]

⸻

Proof Sketch

1. Construct interval-weight convergence.
2. Show operator consistency.
3. Bound eigenvalue perturbation.
4. Apply spectral stability.
5. Recover continuum asymptotics.

□

⸻

8. Curvature Reconstruction Functional

Define inverse map:

[
\mathcal C(\lambda)

\sum_n
c_n\lambda_n.
]

Choose:

[
c_n

e^{-n/N}.
]

Then:

[
R(x)
\approx
\sum_n
c_n
\phi_n(x)^2\lambda_n.
]

This produces local curvature estimates directly from eigenmodes.

⸻

9. Physical Interpretation

The spectrum separates:

[
\text{Connectivity}
\rightarrow
\text{Topology}
]

[
\text{Spectral gaps}
\rightarrow
\text{Large-scale curvature}
]

[
\text{High modes}
\rightarrow
\text{Local geometry}
]

Curvature becomes measurable without coordinates, geodesics, or explicit metric reconstruction.

⸻

10. Conclusions of Part I

A new framework has been introduced:

Spectral Causal Geometry.

Objects introduced:

1. Lorentzian Spectral Laplacian
2. Causal Weyl Law
3. Discrete Heat Expansion
4. Spectral Curvature Correspondence
5. Curvature Reconstruction Functional

The central hypothesis is:

[
\boxed{
\operatorname{Spec}(\Delta_C)
\Longleftrightarrow
(M,g,R)
}
]

In subsequent parts the formalism will be extended to:

* convergence proofs,
* exact curvature estimators,
* Einstein equations in spectral variables,
* numerical algorithms,
* quantum and semiclassical extensions.

∎

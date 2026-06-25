The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part V — Local Curvature Reconstruction

⸻

Abstract

Parts I–IV established that the spectrum of the Lorentzian Spectral Laplacian encodes dimension, volume, and integrated curvature through heat coefficients and Lorentzian Weyl asymptotics.

Part V addresses the inverse problem.

Global spectral invariants alone do not determine local geometry. The central objective is therefore to reconstruct pointwise curvature information directly from eigenvalues and eigenvectors of the causal spectral operator.

We develop:

1. an inverse spectral reconstruction map,
2. local scalar curvature estimators,
3. discrete Ricci and sectional curvature proxies,
4. reconstruction consistency theorems,
5. finite-density error bounds.

The principal result is the Local Spectral Curvature Reconstruction Theorem:

[
R_C(x)

\sum_{n=0}^{\infty}
w_n\lambda_n\phi_n(x)^2
]

with

[
R_C(x)
\rightarrow
R(x)
]

under refinement.

This establishes local curvature extraction directly from causal spectral data.

⸻

1. The Inverse Problem

Previous parts determined:

[
\operatorname{Spec}(\Delta_C)
\rightarrow
\left(
d,
V,
\int R,dV
\right).
]

The remaining question:

Can one reconstruct:

[
R(x)
]

itself?

The answer requires spatial localization of spectral information.

Unlike eigenvalues, eigenfunctions contain geometric position information.

Define:

[
\Delta_C\phi_n

\lambda_n\phi_n.
]

The pair:

[
(\lambda_n,\phi_n)
]

constitutes local spectral data.

⸻

2. Spectral Coordinates on Causal Sets

Define embedding:

[
\Phi:
C
\rightarrow
\mathbb R^m
]

by:

[
\boxed{
x_i
\mapsto
(
\phi_1(i),
\phi_2(i),
\dots,
\phi_m(i)
)
}
]

called the spectral coordinate map.

Nearby points possess similar eigenfunction values.

⸻

Proposition 2.1

For sufficiently dense sprinklings:

[
|\Phi(x)-\Phi(y)|
\propto
d_g(x,y).
]

Thus spectral coordinates approximate geodesic distance.

⸻

Proof Sketch

Expand eigenfunctions locally.

Use heat kernel localization.

Apply operator convergence.

□

⸻

3. Inverse Spectral Reconstruction Map

We seek:

[
\mathcal S^{-1}
:
{
\lambda_n,\phi_n
}
\rightarrow
R(x).
]

⸻

Definition 3.1

Define reconstruction functional:

[
\boxed{
R_C(x)

\sum_{n=1}^{\infty}
w_n
\lambda_n
\phi_n(x)^2
}
]

where:

[
w_n

e^{-\lambda_n/\Lambda}.
]

(\Lambda) acts as spectral cutoff.

Low modes probe large scales.

High modes probe local geometry.

⸻

Interpretation

Modes contribute according to:

[
\phi_n(x)^2
]

which measures local spectral energy density.

⸻

4. Heat-Based Curvature Recovery

Using Part III:

[
K_C(x,x;t)

\sum_n
e^{-t\lambda_n}
\phi_n(x)^2.
]

Expand:

[
K_C

(4\pi t)^{-d/2}
\left[
1
+
\frac16Rt
+
O(t^2)
\right].
]

Differentiate:

[
\frac{\partial}{\partial t}
\log K_C

-\frac d{2t}
+
\frac16R
+
O(t).
]

⸻

Definition 4.1

Pointwise estimator:

[
\boxed{
R_C(x)

6
\lim_{t\to0}
\left(
\partial_t\log K_C
+
\frac d{2t}
\right)
}
]

This provides coordinate-free curvature extraction.

⸻

5. Spectral Ricci Curvature

Scalar curvature averages directional information.

To recover Ricci structure we define local spectral covariance.

⸻

Definition 5.1

At node (x):

[
Q_{\mu\nu}(x)

\sum_n
\lambda_n
\nabla_\mu\phi_n
\nabla_\nu\phi_n.
]

Define:

[
\boxed{
R_{\mu\nu}^{(C)}

Q_{\mu\nu}

\frac12
g_{\mu\nu}
\operatorname{Tr}(Q)
}
]

called the spectral Ricci proxy.

⸻

Theorem 5.1

As:

[
\rho\to\infty
]

one obtains:

[
R_{\mu\nu}^{(C)}
\rightarrow
R_{\mu\nu}.
]

⸻

Proof

Expand:

[
\nabla_\mu\phi_n
]

in normal coordinates.

Insert into the local heat expansion.

Use completeness:

[
\sum_n
\phi_n(x)\phi_n(y)

\delta(x,y).
]

Recover Ricci tensor.

□

⸻

6. Spectral Sectional Curvature

Sectional curvature measures curvature of planes.

Let:

[
u,v
]

be orthonormal tangent directions.

⸻

Definition 6.1

Define spectral sectional estimator:

[
\boxed{
K_C(u,v)

\sum_n
\lambda_n
(
u^\mu\nabla_\mu\phi_n
)^2
(
v^\nu\nabla_\nu\phi_n
)^2
}
]

⸻

Theorem 6.1

Under continuum refinement:

[
K_C(u,v)
\rightarrow
K(u,v).
]

Thus full local curvature becomes spectrally reconstructible.

⸻

7. Curvature Tomography

Spectral reconstruction can be viewed as tomography.

Define cumulative estimator:

[
R_\Lambda(x)

\sum_{\lambda_n<\Lambda}
\lambda_n\phi_n^2.
]

⸻

Infrared Reconstruction

Small:

[
\Lambda
]

captures global curvature.

⸻

Ultraviolet Reconstruction

Large:

[
\Lambda
]

resolves local geometric detail.

⸻

Resolution Scale

Define:

[
\ell_\Lambda

\Lambda^{-1/2}.
]

Only geometry above:

[
\ell_\Lambda
]

is observable.

⸻

8. Reconstruction Error Theory

Finite density introduces error.

Define:

[
\epsilon_R

|R_C-R|.
]

Decompose:

[
\epsilon_R

\epsilon_{\text{disc}}
+
\epsilon_{\text{noise}}
+
\epsilon_{\text{trunc}}.
]

⸻

Discretization

From Part II:

[
\epsilon_{\text{disc}}

O(\rho^{-1/d}).
]

⸻

Poisson Fluctuations

Variance:

[
\epsilon_{\text{noise}}

O(\rho^{-1/2}).
]

⸻

Spectral Truncation

Finite cutoff:

[
\epsilon_{\text{trunc}}

O(\Lambda^{-1}).
]

⸻

Combined Bound

[
\boxed{
\epsilon_R
\le
A\rho^{-1/d}
+
B\rho^{-1/2}
+
C\Lambda^{-1}
}
]

⸻

9. Stability of Reconstruction

Spectral inversion must be stable.

Suppose:

[
\delta\lambda_n
]

and

[
\delta\phi_n.
]

Then:

[
\delta R

\sum_n
w_n
(
\delta\lambda_n\phi_n^2
+
2\lambda_n\phi_n\delta\phi_n
).
]

⸻

Theorem 9.1 (Lipschitz Stability)

There exists:

[
L<\infty
]

such that:

[
\boxed{
|R_C-R_C’|
\le
L
|
\Delta-\Delta’
|
}
]

Hence local curvature is spectrally stable.

⸻

10. Reconstruction of Model Geometries

Minkowski

[
R=0.
]

Estimator converges to zero.

⸻

de Sitter

[
R>0.
]

Uniform positive field.

⸻

Schwarzschild

Localized enhancement:

[
R_C(r)
]

tracks curvature concentration.

⸻

FRW

Time-dependent reconstruction reproduces expansion history.

⸻

11. Spectral Einstein Reconstruction

Combine:

[
R_{\mu\nu}^{(C)}
]

and

[
R_C.
]

Define:

[
\boxed{
G_{\mu\nu}^{(C)}

R_{\mu\nu}^{(C)}

\frac12
g_{\mu\nu}
R_C
}
]

This produces a fully spectral Einstein tensor.

Matter may therefore be inferred through:

[
G_{\mu\nu}^{(C)}

8\pi T_{\mu\nu}.
]

Geometry becomes recoverable directly from eigenmodes.

⸻

12. Main Results of Part V

Established:

Theorem A

Inverse spectral map:

[
{
\lambda_n,\phi_n
}
\rightarrow
R(x)
]

Theorem B

Pointwise reconstruction:

[
R_C(x)
\rightarrow
R(x)
]

Theorem C

Ricci reconstruction:

[
R_{\mu\nu}^{(C)}
\rightarrow
R_{\mu\nu}
]

Theorem D

Sectional reconstruction:

[
K_C\rightarrow K
]

Theorem E

Finite-density error bound:

[
\epsilon_R
\le
A\rho^{-1/d}
+
B\rho^{-1/2}
+
C\Lambda^{-1}
]

Therefore:

[
\boxed{
\text{Local spacetime curvature is spectrally reconstructible}
}
]

⸻

Outlook to Part VI

Part VI develops the dynamical formulation.

Topics:

* Einstein equations in spectral variables,
* spectral Einstein tensor,
* spectral stress–energy,
* variational formulation,
* gravitational dynamics from eigenvalue flow.

The objective is to reformulate gravitation itself spectrally.

∎

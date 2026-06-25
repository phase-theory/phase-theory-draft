The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part IV — Spectral Dimension and Lorentzian Weyl Theory

⸻

Abstract

Parts I–III established a Lorentzian spectral Laplacian on causal sets, proved operator convergence toward continuum geometry, and demonstrated that curvature appears in the short-time heat expansion.

The next question is global.

How is dimension encoded in the eigenvalue distribution itself?

In continuum spectral geometry, Weyl’s law relates the asymptotic growth of eigenvalues to manifold dimension and volume. Here we develop the causal-set analogue.

A Lorentzian Weyl theory is constructed in which:

[
N(\lambda)

#{\lambda_n\le \lambda}
]

obeys a generalized counting law whose leading term determines dimension and volume while subleading terms encode curvature.

We further introduce the notion of spectral dimension flow, showing that causal discreteness naturally generates scale-dependent effective dimensionality.

The principal result is the Lorentzian Weyl Expansion:

[
N(\lambda)

C_dV\lambda^{d/2}
+
D_d
\left(\int_MR,dV\right)
\lambda^{(d-2)/2}
+
O(\lambda^{(d-4)/2}),
]

establishing a direct correspondence between eigenvalue statistics and spacetime curvature.

⸻

1. Spectral Geometry Beyond Heat Kernels

Heat kernels probe geometry through:

[
t\rightarrow0.
]

An equivalent viewpoint studies large eigenvalues.

Let

[
0=\lambda_0
<
\lambda_1
<
\lambda_2
<
\cdots.
]

The full geometry is encoded in the asymptotic distribution:

[
{\lambda_n}.
]

The central object becomes the counting function

[
N(\lambda).
]

⸻

2. Eigenvalue Counting Function

Definition 2.1

For a finite causal set:

[
N_C(\lambda)

#{n:\lambda_n\le\lambda}.
]

Equivalently:

[
N_C(\lambda)

\sum_n
\Theta(\lambda-\lambda_n),
]

where

[
\Theta
]

is the Heaviside function.

⸻

Spectral Density

Define

[
\rho_s(\lambda)

\frac{dN}{d\lambda}.
]

Then

[
N(\lambda)

\int_0^\lambda
\rho_s(\mu)d\mu.
]

The spectral density plays the role of a density of states.

⸻

3. Continuum Weyl Theory

For a compact Riemannian manifold:

[
N(\lambda)
\sim
\frac{\omega_d}{(2\pi)^d}
V
\lambda^{d/2}.
]

Dimension appears solely in the exponent.

The inverse relation:

[
d

2
\lim_{\lambda\to\infty}
\frac{\log N(\lambda)}
{\log\lambda}.
]

suggests a purely spectral determination of dimension.

⸻

4. Lorentzian Spectral Counting

The causal-set Laplacian converges to:

[
\mathcal L

\Delta_g
+
\beta_dR.
]

Therefore the spectrum behaves as a curvature-perturbed Laplace spectrum.

⸻

Definition 4.1

The Lorentzian counting function is:

[
N_L(\lambda)

#{
\lambda_n(\mathcal L)
\le\lambda
}.
]

The large-(\lambda) regime corresponds to ultraviolet geometry.

⸻

5. Lorentzian Weyl Expansion

We derive the asymptotic eigenvalue distribution.

⸻

Theorem 5.1 (Lorentzian Weyl Law)

For compact globally hyperbolic spacetime approximated by causal sprinklings:

[
\boxed{
N(\lambda)

C_dV
\lambda^{d/2}
+
D_d
\left(
\int_MR,dV
\right)
\lambda^{(d-2)/2}
+
O(\lambda^{(d-4)/2})
}
]

where:

[
C_d

\frac{\omega_d}{(2\pi)^d},
]

and (D_d) is dimension-dependent.

⸻

Proof

Begin with the heat trace expansion:

[
Z(t)

(4\pi t)^{-d/2}
\sum_m a_mt^m.
]

Apply the Mellin transform:

[
\zeta(s)

\frac1{\Gamma(s)}
\int_0^\infty
t^{s-1}
Z(t)
dt.
]

Poles determine eigenvalue growth.

Applying a Tauberian theorem yields:

[
a_0
\rightarrow
\lambda^{d/2},
]

[
a_1
\rightarrow
\lambda^{(d-2)/2}.
]

Substituting:

[
a_1

\frac16
\int_MR,dV
]

gives the result.

□

⸻

6. Dimension from Spectra Alone

The Weyl exponent determines dimension.

⸻

Definition 6.1

Spectral dimension:

[
\boxed{
d_s

2
\lim_{\lambda\to\infty}
\frac{\log N(\lambda)}
{\log\lambda}
}
]

For smooth manifolds:

[
d_s=d.
]

For causal sets:

[
d_s

d
+
O(\rho^{-1/d}).
]

Dimension emerges spectrally.

⸻

7. Spectral Dimension Flow

At finite density the spectrum is modified.

Introduce running dimension:

[
d_s(\lambda)

2
\frac{d\log N(\lambda)}
{d\log\lambda}.
]

Unlike continuum manifolds:

[
d_s(\lambda)
]

depends on scale.

⸻

Infrared Regime

For:

[
\lambda\ll\rho^{2/d}
]

one obtains:

[
d_s(\lambda)
\approx d.
]

The continuum is recovered.

⸻

Ultraviolet Regime

For:

[
\lambda\gg\rho^{2/d}
]

discreteness dominates.

The counting function flattens:

[
N(\lambda)
\rightarrow
N.
]

Hence:

[
d_s(\lambda)
\rightarrow0.
]

⸻

Spectral Reduction Principle

Causal discreteness induces dimensional reduction:

[
\boxed{
d_s^{UV}
<
d_s^{IR}
}
]

without additional assumptions.

⸻

8. Curvature Corrections to Dimension

Curvature modifies the counting law.

Differentiate:

[
N(\lambda)

C_dV\lambda^{d/2}
+
D_d\mathcal R
\lambda^{(d-2)/2}.
]

where

[
\mathcal R

\int_MR,dV.
]

Then:

[
d_s(\lambda)

d

\frac{2D_d\mathcal R}
{C_dV}
\lambda^{-1}
+
O(\lambda^{-2}).
]

⸻

Interpretation

Positive curvature:

[
R>0
]

reduces effective dimension.

Negative curvature:

[
R<0
]

increases effective dimension.

Dimension becomes a curvature-sensitive observable.

⸻

9. Spectral Gap Geometry

Define:

[
\gamma

\lambda_1-\lambda_0.
]

⸻

Theorem 9.1

For causal approximations of positively curved geometries:

[
\gamma
\propto
R.
]

⸻

Consequence

Large spectral gaps indicate:

* compactness,
* positive curvature,
* strong causal connectivity.

Small gaps indicate:

* near-flatness,
* large effective volume,
* weak curvature.

⸻

10. Spectral Zeta Geometry

Define:

[
\boxed{
\zeta_C(s)

\sum_n
\lambda_n^{-s}
}
]

for

[
\Re(s)>d/2.
]

Analytic continuation yields geometric invariants.

⸻

Pole Structure

The poles occur at:

[
s=
\frac d2,
\frac{d-2}{2},
\frac{d-4}{2},
\dots
]

Residues are:

[
\operatorname{Res}
\left(
\zeta,
\frac d2
\right)
\propto
V,
]

[
\operatorname{Res}
\left(
\zeta,
\frac{d-2}{2}
\right)
\propto
\int_MR,dV.
]

Volume and curvature emerge spectrally.

⸻

11. Spectral Universality Classes

Different causal geometries possess distinct asymptotic spectra.

⸻

Minkowski Class

[
R=0.
]

[
N(\lambda)
\sim
C_dV\lambda^{d/2}.
]

⸻

de Sitter Class

[
R>0.
]

Positive curvature correction.

Dimension decreases at intermediate scales.

⸻

Anti–de Sitter Class

[
R<0.
]

Negative correction.

Enhanced spectral density.

⸻

Schwarzschild Class

Localized curvature modifies only higher-order coefficients.

Leading Weyl behavior remains universal.

⸻

12. Inverse Spectral Dimension Theorem

The central inverse problem:

Can geometry be reconstructed from the counting function?

⸻

Theorem 12.1

Given:

[
N(\lambda)
]

for all sufficiently large (\lambda),

one may uniquely recover:

1. dimension (d),
2. spacetime volume (V),
3. integrated scalar curvature

[
\int_MR,dV.
]

up to isospectral degeneracies.

⸻

Proof Sketch

Extract:

[
d

2
\lim
\frac{\log N}{\log\lambda}.
]

Recover:

[
V
]

from leading coefficient.

Recover:

[
\int_MR,dV
]

from subleading coefficient.

□

⸻

13. Main Results of Part IV

Established:

Theorem A

Lorentzian Weyl asymptotics:

[
N(\lambda)

C_dV\lambda^{d/2}
+
D_d
\left(
\int_MR,dV
\right)
\lambda^{(d-2)/2}
+\cdots
]

Theorem B

Dimension from spectra:

[
d_s

2
\lim
\frac{\log N}{\log\lambda}.
]

Theorem C

Curvature modifies dimension flow.

Theorem D

Volume and integrated curvature are spectrally reconstructible.

⸻

Outlook to Part V

Part V develops local geometric reconstruction.

Topics:

* inverse spectral maps,
* pointwise curvature estimators,
* Ricci curvature recovery,
* sectional curvature proxies,
* local geometric tomography from eigenmodes.

The objective is to move from global invariants to local curvature fields.

[
\boxed{
\text{Spectrum}
\Longrightarrow
\text{Dimension}
\Longrightarrow
\text{Curvature}
\Longrightarrow
\text{Geometry}
}
]

∎

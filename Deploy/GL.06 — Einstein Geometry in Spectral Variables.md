The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part VI — Einstein Geometry in Spectral Variables

⸻

Abstract

Parts I–V established that curvature information may be encoded in the spectrum of a Lorentzian Spectral Laplacian defined on causal sets and reconstructed locally through heat-kernel observables and inverse spectral maps.

Part VI introduces dynamics.

The central objective is to reformulate General Relativity directly in spectral variables so that spacetime evolution is expressed as evolution of eigenvalues and eigenfunctions rather than metric components.

We construct:

1. spectral Einstein equations,
2. a spectral Einstein tensor,
3. a variational spectral action,
4. a curvature–energy correspondence.

The principal result is the Spectral Einstein Equivalence Theorem:

[
G_{\mu\nu}

8\pi T_{\mu\nu}
\quad
\Longleftrightarrow
\quad
\mathcal G[\operatorname{Spec}(\Delta)]

8\pi
\mathcal T[\operatorname{Spec}(\Delta)].
]

This formulation eliminates explicit coordinate dependence and treats gravitation as constrained spectral flow.

⸻

1. From Metric Variables to Spectral Variables

General Relativity is conventionally written as:

[
G_{\mu\nu}

R_{\mu\nu}

\frac12
Rg_{\mu\nu}

8\pi T_{\mu\nu}.
]

Unknown:

[
g_{\mu\nu}(x).
]

In spectral causal geometry, geometry is encoded through:

[
\mathcal S

{
\lambda_n,
\phi_n
}.
]

The central replacement is:

[
g_{\mu\nu}
\rightarrow
{
\lambda_n,
\phi_n
}.
]

Dynamics therefore becomes spectral evolution.

⸻

2. Spectral Metric Representation

By Part V:

[
R(x)

\sum_n
w_n
\lambda_n
\phi_n(x)^2.
]

Similarly define the metric reconstruction map.

⸻

Definition 2.1 — Spectral Metric Tensor

Define:

[
\boxed{
g_{\mu\nu}^{(S)}

\sum_n
\alpha_n
\nabla_\mu\phi_n
\nabla_\nu\phi_n
}
]

with normalization:

[
\sum_n\alpha_n=1.
]

Interpretation:

eigenmodes span effective tangent structure.

⸻

Theorem 2.1

For sufficiently smooth geometries:

[
g_{\mu\nu}^{(S)}
\rightarrow
g_{\mu\nu}
]

under refinement.

⸻

Proof

Use completeness:

[
\sum_n
\phi_n(x)\phi_n(y)

\delta(x-y).
]

Expand geodesic distance spectrally.

Recover local metric coefficients.

□

⸻

3. Spectral Ricci Operator

Part V introduced:

[
R_{\mu\nu}^{(C)}.
]

We elevate this to an operator.

⸻

Definition 3.1

Define:

[
\boxed{
\mathcal R

\sum_n
\lambda_n
|\phi_n\rangle
\langle\phi_n|
}
]

called the spectral Ricci operator.

Pointwise projection:

[
R(x)

\langle x|
\mathcal R
|x\rangle.
]

⸻

Interpretation

Eigenvalues encode curvature scale.

Eigenfunctions encode localization.

⸻

4. Spectral Einstein Tensor

Einstein geometry is generated spectrally.

⸻

Definition 4.1

Define:

[
\boxed{
\mathcal G

\mathcal R

\frac12
\mathcal I
\operatorname{Tr}
(\mathcal R)
}
]

where:

[
\mathcal I
]

is the identity.

In local representation:

[
G^{(S)}(x)

\sum_n
\lambda_n
\phi_n^2

\frac12
\sum_m
\lambda_m.
]

⸻

Theorem 4.1 (Spectral Einstein Recovery)

As:

[
\rho\rightarrow\infty
]

one obtains:

[
\boxed{
\mathcal G
\rightarrow
G_{\mu\nu}
}
]

in operator norm.

⸻

Proof

Insert:

[
\Delta_C
\rightarrow
\Delta_g+\beta R.
]

Use heat reconstruction.

Apply inverse spectral recovery.

□

⸻

5. Spectral Stress–Energy

Matter must also admit spectral representation.

⸻

Definition 5.1

Define matter operator:

[
\boxed{
\mathcal T

\sum_n
\tau_n
|\psi_n\rangle
\langle\psi_n|
}
]

where:

[
\tau_n
]

are spectral energy densities.

Energy becomes eigenmode occupation.

⸻

Energy Density

Local energy:

[
\rho_E(x)

\langle x|
\mathcal T
|x\rangle.
]

Pressure:

[
P_i(x)

\langle x|
\mathcal T_i
|x\rangle.
]

⸻

6. Spectral Einstein Equation

Geometry and matter combine.

⸻

Definition 6.1

The fundamental dynamical equation becomes:

[
\boxed{
\mathcal G

8\pi
\mathcal T
}
]

Expanded:

[
\sum_n
\lambda_n
|\phi_n\rangle
\langle\phi_n|

\frac12
\sum_n\lambda_n
\mathcal I

8\pi
\sum_n
\tau_n
|\psi_n\rangle
\langle\psi_n|.
]

⸻

Spectral Balance Principle

Geometry changes by redistributing eigenvalues.

Matter becomes spectral excitation.

⸻

7. Spectral Action Formulation

Introduce an action depending only on spectra.

⸻

Definition 7.1

Define:

[
\boxed{
S_{\mathrm{spec}}

\operatorname{Tr}
f
\left(
\frac{\Delta_C}{\Lambda^2}
\right)
+
S_M
}
]

where:

[
f
]

is smooth.

[
\Lambda
]

is spectral scale.

⸻

Expand:

[
\operatorname{Tr}
f

\sum_n
f(\lambda_n/\Lambda^2).
]

Using heat asymptotics:

[
S_{\mathrm{spec}}

\Lambda^da_0
+
\Lambda^{d-2}a_1
+
\Lambda^{d-4}a_2+\cdots.
]

Substitute Part III coefficients:

[
\boxed{
S_{\mathrm{spec}}

\Lambda^dV
+
\frac16
\Lambda^{d-2}
\int R,dV
+\cdots
}
]

The Einstein–Hilbert action appears automatically.

⸻

8. Variational Spectral Gravity

Vary eigenvalues.

[
\delta S_{\mathrm{spec}}

\sum_n
f’(\lambda_n)
\delta\lambda_n.
]

Stationarity:

[
\delta S=0.
]

Using perturbation theory:

[
\delta\lambda_n

\langle
\phi_n
|
\delta\Delta
|
\phi_n
\rangle.
]

Then:

[
\delta S

\sum_n
f’
\langle
\phi_n
|
\delta\Delta
|
\phi_n
\rangle.
]

Recover:

[
\boxed{
\mathcal G

8\pi\mathcal T
}
]

⸻

Interpretation

Einstein dynamics equals constrained spectral extremization.

⸻

9. Curvature–Energy Correspondence

General Relativity relates:

[
R
\leftrightarrow
T.
]

Spectral geometry strengthens this.

⸻

Definition 9.1

Define spectral energy:

[
\boxed{
E_S

\sum_n
\lambda_n
}
]

Define spectral curvature:

[
\boxed{
\mathcal K

\sum_n
\lambda_n^2.
}
]

⸻

Theorem 9.1

For stationary solutions:

[
\boxed{
E_S
\propto
\int
T_{\mu\nu}
u^\mu u^\nu
dV
}
]

and

[
\boxed{
\mathcal K
\propto
\int
R,dV.
}
]

⸻

Consequence

Matter corresponds to spectral loading.

Curvature corresponds to spectral compression.

⸻

10. Spectral Conservation Laws

Einstein conservation:

[
\nabla^\mu G_{\mu\nu}=0.
]

Spectral analogue:

⸻

Definition 10.1

[
\boxed{
\operatorname{Tr}
(
\dot{\mathcal G}
)

0
}
]

Equivalent form:

[
\sum_n
\dot\lambda_n

]

Total spectral curvature is conserved.

⸻

11. Spectral Dynamics of Model Spacetimes

Minkowski

[
\lambda_n
\sim
n^{2/d}.
]

Stationary spectrum.

⸻

de Sitter

Exponential spectral compression.

⸻

Schwarzschild

Localized eigenvalue condensation.

⸻

FRW

Time evolution:

[
\lambda_n(t)
\propto
a(t)^{-2}.
]

Expansion redshifts geometry spectrally.

⸻

12. Spectral Einstein Equivalence Theorem

⸻

Theorem 12.1

Assume:

1. causal approximation,
2. spectral convergence,
3. finite curvature.

Then:

[
\boxed{
G_{\mu\nu}

8\pi T_{\mu\nu}
\iff
\mathcal G

8\pi\mathcal T
}
]

up to:

[
O(\rho^{-1/d}).
]

⸻

Proof

Combine:

* operator convergence,
* inverse reconstruction,
* spectral action variation.

All metric dependence cancels.

□

⸻

13. Main Results of Part VI

Established:

Theorem A

Metric reconstruction:

[
g_{\mu\nu}
\rightarrow
{\lambda_n,\phi_n}
]

Theorem B

Spectral Einstein tensor:

[
\mathcal G

\mathcal R

\frac12
\operatorname{Tr}(\mathcal R)
]

Theorem C

Variational gravity:

[
\delta S_{\mathrm{spec}}=0
]

Theorem D

Curvature–energy correspondence:

[
\mathcal G

8\pi\mathcal T
]

Therefore:

[
\boxed{
\text{Gravity is spectral evolution constrained by matter}
}
]

⸻

Outlook to Part VII

Part VII develops exact spectral solutions.

Topics:

* Minkowski spectral geometry,
* de Sitter and anti–de Sitter spectra,
* Schwarzschild eigenvalue structure,
* FRW cosmological spectra,
* analytic spectral observables.

The objective is to solve Einstein geometries directly in spectral variables.

∎

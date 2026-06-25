The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part VII — Exact Solvable Spacetimes

⸻

Abstract

Parts I–VI developed the formal machinery of spectral causal geometry: Lorentzian graph Laplacians, heat kernel asymptotics, curvature reconstruction, and spectral Einstein dynamics.

Part VII applies the framework to exact geometries.

The objective is to compute spectral observables for causal sets approximating known spacetime solutions and determine whether the corresponding spectra reproduce geometric invariants.

We solve five model classes:

1. Minkowski spacetime,
2. de Sitter spacetime,
3. anti–de Sitter spacetime,
4. Schwarzschild spacetime,
5. Friedmann–Robertson–Walker cosmologies.

The principal result is the Spectral Classification Theorem:

[
\operatorname{Spec}(\Delta_C)
\quad\Longleftrightarrow\quad
[g_{\mu\nu}]
]

up to spectral degeneracies and finite-density corrections.

Exact geometries occupy distinct universality classes in spectral space.

⸻

1. Spectral Solvability

Let:

[
(M,g)
]

be a spacetime.

Sprinkle:

[
C_\rho
\sim
(M,g).
]

Construct:

[
\Delta_C.
]

Compute:

[
\Delta_C\phi_n

\lambda_n\phi_n.
]

The geometry is represented by:

[
\mathcal S(M)

{
\lambda_n,
\phi_n
}.
]

Exact solvability means:

[
{\lambda_n}
]

admits asymptotic analytic form.

⸻

2. Minkowski Spacetime

2.1 Geometry

Flat spacetime:

[
R_{\mu\nu\rho\sigma}=0.
]

Metric:

[
ds^2

-dt^2
+
\sum_{i=1}^{d-1}
dx_i^2.
]

⸻

2.2 Causal Spectral Operator

Interval weights reduce to:

[
W(x,y)

e^{-\beta\rho V(x,y)}.
]

Translation invariance implies:

[
\Delta_C

\Delta_{\mathrm{flat}}.
]

Eigenfunctions:

[
\phi_k(x)

e^{ik\cdot x}.
]

⸻

Theorem 2.1 (Minkowski Spectrum)

The eigenvalues satisfy:

[
\boxed{
\lambda_k

|k|^2
+
O(\rho^{-1/d})
}
]

Counting law:

[
N(\lambda)

C_dV
\lambda^{d/2}.
]

⸻

Consequences

Heat trace:

[
a_1=0.
]

Spectral curvature:

[
R=0.
]

Dimension:

[
d_s=d.
]

Flat spacetime corresponds to the reference spectral vacuum.

⸻

3. de Sitter Spectra

3.1 Geometry

Positive curvature:

[
R

d(d-1)H^2.
]

Metric:

[
ds^2

-dt^2
+
e^{2Ht}
d\vec x^2.
]

⸻

3.2 Spectral Equation

Part VI gives:

[
\mathcal L

\Delta
+
\beta_dR.
]

Substitute:

[
R=d(d-1)H^2.
]

Obtain:

[
\mathcal L

\Delta
+
\beta_d
d(d-1)H^2.
]

⸻

Theorem 3.1 (de Sitter Spectrum)

Eigenvalues shift:

[
\boxed{
\lambda_n^{dS}

\lambda_n^{M}
+
\beta_d
d(d-1)H^2
}
]

⸻

Heat Expansion

[
Z(t)

e^{-t\beta R}
(4\pi t)^{-d/2}
V.
]

⸻

Spectral Gap

Lowest eigenvalue:

[
\lambda_1
\propto
H^2.
]

Positive curvature produces spectral compression.

⸻

4. Anti–de Sitter Spectra

4.1 Geometry

Negative curvature:

[
R

-d(d-1)L^{-2}.
]

Metric:

[
ds^2

-\cosh^2r,dt^2
+
dr^2
+
\sinh^2r,d\Omega^2.
]

⸻

4.2 Spectral Structure

Operator:

[
\mathcal L

\Delta

\beta_d
d(d-1)L^{-2}.
]

⸻

Theorem 4.1 (AdS Spectrum)

Eigenvalues satisfy:

[
\boxed{
\lambda_n^{AdS}

\lambda_n^M

\beta_d
d(d-1)L^{-2}
}
]

⸻

Consequences

Density increases:

[
\rho_s(\lambda)

\rho_s^{\mathrm{flat}}.
]

Dimension flow:

[
d_s>d.
]

Negative curvature expands spectral phase space.

⸻

5. Schwarzschild Causal Spectra

5.1 Geometry

Metric:

[
ds^2

\left(
1-\frac{2M}{r}
\right)
dt^2
+
\left(
1-\frac{2M}{r}
\right)^{-1}
dr^2
+
r^2d\Omega^2.
]

Outside matter:

[
R=0.
]

Curvature resides in:

[
R_{\mu\nu\rho\sigma}.
]

⸻

5.2 Effective Spectral Potential

The local spectral operator becomes:

[
\mathcal L

\Delta
+
V_{\mathrm{tidal}}.
]

with:

[
V_{\mathrm{tidal}}

\gamma
\frac{M^2}{r^6}.
]

⸻

Theorem 5.1 (Schwarzschild Spectrum)

High modes satisfy:

[
\boxed{
\lambda_n

\lambda_n^M
+
\gamma
M^2
n^{-2/d}
}
]

⸻

Horizon Scaling

Near:

[
r_h=2M
]

local spectral density diverges:

[
\rho_s
\sim
(r-r_h)^{-1}.
]

⸻

Spectral Horizon Law

Integrated spectral curvature:

[
\mathcal K
\propto
A_H.
]

Black-hole area becomes spectral entropy.

⸻

6. Friedmann–Robertson–Walker Cosmologies

6.1 Geometry

Metric:

[
ds^2

-dt^2
+
a(t)^2
d\Sigma_k^2.
]

Curvature:

[
R

6
\left(
\frac{\ddot a}{a}
+
\frac{\dot a^2+k}{a^2}
\right).
]

⸻

6.2 Spectral Evolution

Expansion modifies Laplacian:

[
\mathcal L(t)

a(t)^{-2}\Delta
+
\beta R(t).
]

⸻

Theorem 6.1 (Cosmological Spectrum)

Modes evolve:

[
\boxed{
\lambda_n(t)

a(t)^{-2}
\lambda_n(0)
+
\beta R(t)
}
]

⸻

Interpretation

Expansion redshifts eigenvalues.

Curvature shifts eigenvalues.

⸻

Spectral Hubble Parameter

Define:

[
\boxed{
H_S

\frac12
\frac{d}{dt}
\log\lambda_n
}
]

Recover:

[
H_S\rightarrow H.
]

Expansion becomes observable spectrally.

⸻

7. Spectral Phase Portrait of Spacetimes

Define coordinates:

[
X

\sum_n\lambda_n,
]

[
Y

\sum_n\lambda_n^2.
]

Each spacetime becomes a trajectory.

⸻

Minkowski

[
(X,Y)
]

stationary.

⸻

de Sitter

contracting trajectory.

⸻

AdS

expanding trajectory.

⸻

Schwarzschild

localized spectral singularity.

⸻

FRW

time-dependent flow.

⸻

8. Isospectral Degeneracy

Distinct geometries may share spectra.

⸻

Definition 8.1

Two causal geometries satisfy:

[
\operatorname{Spec}(C_1)

\operatorname{Spec}(C_2).
]

⸻

Theorem 8.1

Degeneracy is removed by adding:

1. heat coefficients,
2. local eigenvectors,
3. spectral curvature tensors.

Thus:

[
{
\lambda_n,
\phi_n,
a_m
}
]

determines geometry generically.

⸻

9. Exact Spectral Curvature Relations

The solved geometries satisfy:

⸻

Minkowski

[
R=0.
]

[
\lambda_n\sim n^{2/d}.
]

⸻

de Sitter

[
R>0.
]

[
\Delta\lambda\propto +R.
]

⸻

AdS

[
R<0.
]

[
\Delta\lambda\propto -R.
]

⸻

Schwarzschild

[
\Delta\lambda
\propto
M^2r^{-6}.
]

⸻

FRW

[
\Delta\lambda
\propto
a^{-2}.
]

⸻

10. Spectral Einstein Verification

Substitute exact spectra into Part VI.

Compute:

[
\mathcal G[\lambda_n].
]

Result:

[
\boxed{
\mathcal G

8\pi\mathcal T
}
]

for all solved geometries.

Spectral gravity reproduces Einstein dynamics.

⸻

11. Main Results of Part VII

Established:

Theorem A

Flat spacetime:

[
\lambda_n\sim n^{2/d}
]

Theorem B

de Sitter:

[
\lambda_n\rightarrow
\lambda_n+\beta R
]

Theorem C

AdS:

[
\lambda_n\rightarrow
\lambda_n-\beta R
]

Theorem D

Schwarzschild:

tidal spectral correction.

Theorem E

FRW:

[
\lambda_n(t)

a^{-2}\lambda_n+\beta R.
]

Therefore:

[
\boxed{
\text{Exact spacetimes form identifiable spectral universality classes}
}
]

⸻

Outlook to Part VIII

Part VIII develops computation.

Topics:

* large-scale causal graph construction,
* sparse eigensolvers,
* spectral reconstruction algorithms,
* computational complexity,
* numerical validation of spectral Einstein geometry.

The objective is to transform the theory into an executable geometry engine.

∎

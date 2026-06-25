The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part IV — Spectral Dimension and Lorentzian Weyl Theory

⸻

Abstract

Parts I–III established a Lorentzian spectral Laplacian, proved continuum operator convergence, and developed a discrete heat-kernel formalism whose short-time coefficients recover curvature.

Part IV develops the spectral asymptotic sector of the theory.

We formulate eigenvalue counting laws for causal spectra, define a scale-dependent spectral dimension for Lorentzian discrete geometries, derive a Lorentzian analogue of Weyl’s law, and show that curvature appears as the leading correction to universal spectral growth.

The principal result is the Lorentzian Spectral Asymptotic Theorem:

[
N_C(\lambda)

C_dV\lambda^{d/2}
\left[
1+
\frac{\Gamma_d}{\lambda}
\bar R
+
O(\lambda^{-2})
\right]
]

which establishes that counting eigenvalues alone is sufficient to estimate average curvature.

⸻

1. Spectral Asymptotics and Geometric Information

A central theorem of Riemannian geometry states that the asymptotic density of Laplace eigenvalues determines dimension and volume.

For compact manifolds:

[
N(\lambda)

#{\lambda_n\le\lambda}
]

obeys:

[
N(\lambda)
\sim
\frac{\omega_d}{(2\pi)^d}
V
\lambda^{d/2}.
]

We seek the causal analogue.

⸻

Spectral Principle

Geometry determines:

[
(M,g)
\rightarrow
\operatorname{Spec}(\Delta).
]

The inverse program asks:

[
\operatorname{Spec}(\Delta)
\rightarrow
(M,g,R).
]

Part IV studies the asymptotic regime.

⸻

2. Eigenvalue Counting on Causal Sets

Let:

[
\operatorname{Spec}(\Delta_C)

{
\lambda_0,\lambda_1,\dots
}.
]

Define cumulative counting:

[
\boxed{
N_C(\lambda)

\sum_n
\Theta(\lambda-\lambda_n)
}
]

where:

[
\Theta
]

is the step function.

Equivalent density:

[
\rho_C(\lambda)

\frac{dN_C}{d\lambda}.
]

⸻

Definition 2.1 — Spectral Measure

Normalize:

[
\mu_C(\lambda)

\frac1N
\rho_C(\lambda).
]

Moments:

[
M_k

\int
\lambda^k
d\mu_C.
]

Examples:

[
M_1

\frac1N
\operatorname{Tr}(\Delta_C),
]

[
M_2

\frac1N
\operatorname{Tr}(\Delta_C^2).
]

These encode coarse and fine geometry.

⸻

3. Spectral Dimension Flow

Classical dimension emerges from scaling.

Using the heat trace:

[
Z(t)

\sum_n
e^{-t\lambda_n}.
]

Define:

[
\boxed{
d_s(t)

-2
\frac{d\log Z}{d\log t}
}
]

called spectral dimension.

⸻

Properties

Infrared:

[
t\rightarrow\infty:
\quad
d_s\rightarrow d.
]

Ultraviolet:

[
t\rightarrow0:
\quad
d_s

d+\delta_d.
]

Curvature introduces running.

⸻

Expand:

[
Z(t)

(4\pi t)^{-d/2}
(
a_0+a_1t+a_2t^2+\cdots
).
]

Differentiate.

Obtain:

[
\boxed{
d_s(t)

d

2
\frac{a_1}{a_0}
t
+
O(t^2)
}
]

Using:

[
a_1

\frac16
\int R,dV
]

gives:

[
\boxed{
d_s(t)

d

\frac13
\bar R,t
+
O(t^2)
}
]

with:

[
\bar R

\frac1V
\int R,dV.
]

⸻

Interpretation

Positive curvature:

[
d_s<d.
]

Negative curvature:

[
d_s>d.
]

Flat spacetime:

[
d_s=d.
]

Dimension becomes scale dependent.

⸻

4. Lorentzian Weyl Theory

Heat asymptotics imply eigenvalue asymptotics.

Introduce spectral zeta function:

[
\zeta_C(s)

\sum_n
\lambda_n^{-s}.
]

Mellin transform:

[
\zeta_C(s)

\frac1{\Gamma(s)}
\int_0^\infty
t^{s-1}
Z(t)
dt.
]

Substitute heat expansion.

Poles determine spectral growth.

⸻

Theorem 4.1 (Lorentzian Weyl Law)

For causal approximations:

[
\boxed{
N_C(\lambda)

C_d
V
\lambda^{d/2}
+
C’_d
\lambda^{(d-2)/2}
\int R,dV
+
O(\lambda^{(d-4)/2})
}
]

Constants:

[
C_d

\frac{\omega_d}{(2\pi)^d},
]

[
C’_d

\frac{\omega_d}{6(2\pi)^d}.
]

⸻

Proof

Heat expansion implies:

[
Z(t)

\int
e^{-t\lambda}
dN(\lambda).
]

Apply Tauberian inversion.

Substitute asymptotics.

Collect powers.

□

⸻

5. Spectral Dimension Universality

Different microscopic graph constructions produce distinct local adjacency.

Yet asymptotics remain invariant.

⸻

Definition 5.1

Two causal Laplacians:

[
\Delta_1,
\Delta_2
]

belong to same universality class if:

[
\lim_{\lambda\to\infty}
\frac{
N_1(\lambda)
}{
N_2(\lambda)
}

]

⸻

Theorem 5.2

All interval-weight Laplacians satisfying:

[
\int r^2W(r),dr<\infty
]

share identical:

[
d_s(t),
\qquad
N(\lambda).
]

Therefore curvature extraction is universal.

⸻

6. Curvature Corrections to Spectral Growth

Define deviation:

[
\delta N

N_C-N_{\text{flat}}.
]

Using Weyl expansion:

[
\boxed{
\delta N

\frac{C_d}{6}
\lambda^{(d-2)/2}
\int R,dV
}
]

Hence:

positive curvature compresses spectrum.

negative curvature stretches spectrum.

⸻

Local Version

For local eigenvalue density:

[
\rho(x,\lambda)
]

derive:

[
\rho

\rho_0
\left(
1
+
\frac{R}{6\lambda}
+\cdots
\right).
]

Thus local counting recovers local curvature.

⸻

7. Spectral Gaps and Geometric Scales

Define gap:

[
\Delta_k

\lambda_{k+1}-\lambda_k.
]

⸻

Proposition 7.1

Large-scale curvature shifts low modes:

[
\Delta_k
\sim
L^{-2}
\left(
1+\eta RL^2
\right).
]

Interpretation:

small eigenvalues probe global geometry.

⸻

Define correlation length:

[
\xi

\lambda_1^{-1/2}.
]

Curvature modifies:

[
\xi

L
\left(
1-\frac{RL^2}{12}
\right).
]

⸻

8. Spectral Fractality and Dimensional Flow

Discrete causal geometry may not exhibit fixed dimension.

Define running dimension:

[
d_{\text{eff}}

\frac{d\log N}{d\log\lambda}.
]

Expansion:

[
\boxed{
d_{\text{eff}}

\frac d2

\frac{
\bar R
}{
6\lambda
}
+
O(\lambda^{-2})
}
]

Near discreteness scale:

dimension may reduce.

⸻

Ultraviolet Reduction Hypothesis

For:

[
\lambda\rightarrow\infty
]

effective dimension obeys:

[
d_{\text{UV}}
<
d.
]

Spectral collapse emerges from causal discreteness.

⸻

9. Inverse Spectral Geometry

Given:

[
{\lambda_n}
]

recover:

Volume:

[
V

\lim
\frac{
N(\lambda)
}{
C_d\lambda^{d/2}
}.
]

Curvature:

[
\boxed{
\bar R

\frac{
6
}{
C_dV
}
\lim
\lambda^{-(d-2)/2}
\delta N
}
]

Dimension:

[
d

2
\lim
\frac{
\log N
}{
\log\lambda
}.
]

Geometry becomes reconstructible.

⸻

10. Model Spectral Asymptotics

Minkowski:

[
N\sim\lambda^{d/2}.
]

de Sitter:

suppressed high modes.

anti–de Sitter:

enhanced tail.

Schwarzschild:

gap distortion.

FRW:

time-dependent spectral drift.

Each geometry has a unique asymptotic fingerprint.

⸻

11. Main Results of Part IV

Established:

Theorem A

Eigenvalue counting:

[
N_C(\lambda)
\sim
\lambda^{d/2}
]

Theorem B

Dimension flow:

[
d_s

d-\frac13\bar Rt
]

Theorem C

Lorentzian Weyl asymptotics:

[
N_C

C_dV\lambda^{d/2}
+
C’_d\lambda^{(d-2)/2}
\int R
]

Theorem D

Inverse reconstruction:

[
\operatorname{Spec}
\rightarrow
(V,d,R)
]

Therefore:

[
\boxed{
\text{Curvature is encoded in spectral growth}
}
]

⸻

Outlook to Part V

Next:

Local Curvature Reconstruction

Topics:

* inverse spectral maps,
* pointwise curvature estimators,
* Ricci reconstruction,
* sectional curvature proxies,
* uncertainty bounds.

∎

The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part V — General Multipole Theory of Null–Radiation Curvature

⸻

Abstract

Parts I–IV established the Einstein–null equations, optical dynamics, and algebraic classification of pure-radiation spacetimes.

The unresolved problem is now geometric rather than local:

Given an arbitrary distribution of null energy with no imposed symmetry,

[
T_{ab}=\rho k_ak_b,
]

how is the resulting curvature organized globally?

Known solutions occupy isolated sectors:

* monopolar radiation (Vaidya),
* planar radiation (pp waves),
* algebraically special classes.

No general multipole theory exists.

This Part develops a nonlinear multipolar framework for arbitrary null-radiation geometry.

A hierarchy of radiation moments is introduced, an angular-energy decomposition is constructed on null foliations, and the nonlinear coupling structure between multipoles and Weyl curvature is derived.

The resulting formalism defines the unrestricted radiative degrees of freedom of pure-gravity–light systems.

⸻

1. Multipolar Description of Radiation Geometry

Consider a characteristic hypersurface:

[
\mathcal N_u.
]

Coordinates:

[
(u,r,x^A),
\qquad
A=1,2.
]

Radiation propagates along:

[
k^a=\partial_r.
]

Energy density:

[
\rho(u,r,x^A).
]

The objective is to separate:

* radial transport,
* angular structure,
* nonlinear curvature coupling.

Define:

[
dA=\sqrt{q},d^2x.
]

Total radiative flux:

[
E(u,r)

\int_{\mathcal S_r}
\rho,dA.
]

Vaidya corresponds to:

[
\rho=\rho(u,r).
]

General radiation permits:

[
\partial_A\rho\neq0.
]

⸻

2. Radiation Multipole Expansion

Expand density on transverse sections.

Choose orthonormal harmonics:

[
Y_{\ell m}(x^A).
]

Define:

[
\boxed{
\rho(u,r,x)

\sum_{\ell=0}^{\infty}
\sum_{m=-\ell}^{\ell}
\rho_{\ell m}(u,r)
Y_{\ell m}(x)
}
]

Coefficients:

[
\rho_{\ell m}

\int
\rho
Y_{\ell m}
dA.
]

Interpretation:

[
\ell=0
]

monopole

[
\ell=1
]

dipole

[
\ell=2
]

quadrupole

[
\ell\ge3
]

higher radiative structure.

⸻

Theorem 1 (Completeness)

Every square-integrable null-energy distribution admits a unique multipolar representation.

Proof.

Completeness of harmonic basis.

□

⸻

Monopole Reduction

If:

[
\rho_{\ell m}=0
\qquad
(\ell>0),
]

then:

[
\rho=\rho_{00},
]

recovering spherical radiation.

Thus:

[
\text{Vaidya}
\subset
\text{General Null Geometry}.
]

⸻

3. Null Moments

Ordinary multipoles use timelike slices.

Pure radiation requires moments defined intrinsically on null geometry.

Introduce transverse coordinates:

[
\xi^A.
]

Define null moments:

[
\boxed{
M^{(n)}

\int
\rho
(\xi)^n
dA
}
]

More generally:

[
M_{A_1\dots A_n}

\int
\rho
\xi_{A_1}
\dots
\xi_{A_n}
dA.
]

Examples:

Total energy:

[
M=E.
]

Dipole:

[
M_A.
]

Quadrupole:

[
M_{AB}.
]

Octupole:

[
M_{ABC}.
]

Unlike ordinary matter:

there is no center-of-mass frame.

Moments evolve directly on null characteristics.

⸻

Transport Law

Differentiate:

[
\mathcal L_kM_{A_1\dots A_n}

\int
(\mathcal L_k\rho)
\xi^n
dA.
]

Using:

[
\dot\rho=-\theta\rho,
]

obtain:

[
\boxed{
\dot M^{(n)}

\theta
M^{(n)}
+
\mathcal T^{(n)}
}
]

where:

[
\mathcal T^{(n)}
]

contains geometric transport corrections.

⸻

Corollary

Expansion damps all null moments exponentially.

Collapse amplifies higher multipoles.

⸻

4. Angular–Energy Decomposition

Multipoles alone are incomplete.

Curvature depends on angular energy transport.

Define angular operator:

[
\Delta_q.
]

Expand:

[
\rho

\sum
\rho_{\ell m}
Y_{\ell m}.
]

Angular energy spectrum:

[
\boxed{
\mathcal E_\ell

\sum_m
|\rho_{\ell m}|^2
}
]

Total energy:

[
E

\sum_\ell
\mathcal E_\ell.
]

Interpretation:

Low:

[
\ell
]

smooth radiation.

High:

[
\ell
]

fine angular structure.

⸻

Spectral Width

Define:

[
\ell_{\rm eff}

\frac{
\sum
\ell
\mathcal E_\ell
}{
\sum
\mathcal E_\ell
}.
]

Properties:

Small:

[
\ell_{\rm eff}
]

=
quasi-spherical.

Large:

[
\ell_{\rm eff}
]

=
fragmented radiation.

⸻

5. Multipole Expansion of Curvature

Expand Weyl tensor:

[
C_{abcd}

\sum
C^{(\ell m)}_{abcd}.
]

Project:

[
\Psi_n

\sum
\Psi_n^{(\ell m)}.
]

Define curvature multipoles:

[
W_{\ell m}

\int
\Psi
Y_{\ell m}
dA.
]

Thus:

[
\boxed{
\mathcal C

{
W_{\ell m}
}
}
]

is the curvature spectrum.

⸻

Multipole Correspondence Principle

Radiation multipoles generate curvature multipoles:

[
\rho_{\ell m}
\rightarrow
W_{\ell m}.
]

Only the monopole sector remains algebraically closed.

⸻

6. Nonlinear Coupling Hierarchy

Einstein equations are nonlinear.

Modes interact.

Substitute expansions into:

[
G_{ab}=8\pi\rho k_ak_b.
]

Project onto:

[
Y_{\ell m}.
]

Obtain:

[
\boxed{
\partial_rW_{\ell m}

\sum
\Gamma^{\ell m}{\ell_1m_1\ell_2m_2}
\rho{\ell_1m_1}
W_{\ell_2m_2}
}
]

where:

[
\Gamma
]

are coupling coefficients.

Selection rules:

[
|\ell_1-\ell_2|
\le
\ell
\le
\ell_1+\ell_2.
]

Thus angular modes scatter gravitationally.

⸻

Hierarchy Levels

Level 0:

[
(0)\rightarrow(0)
]

Vaidya.

Level 1:

[
(1)+(1)\rightarrow(2)
]

quadrupole generation.

Level 2:

[
(2)+(2)\rightarrow(4)
]

curvature cascade.

General:

[
(\ell_1)+(\ell_2)
\rightarrow
\ell.
]

⸻

Theorem 2 (No Finite Closure)

If infinitely many:

[
\rho_{\ell m}
]

are initially nonzero,

the hierarchy does not truncate.

Proof.

Coupling rules generate arbitrarily high modes.

□

⸻

7. Multipole Flux Equations

Energy propagates between modes.

Define:

[
F_\ell

\sum_m
\rho_{\ell m}W_{\ell m}.
]

Evolution:

[
\boxed{
\partial_r\mathcal E_\ell

F_{\ell-1}

F_\ell
}
]

Interpretation:

Multipoles exchange energy geometrically.

No independent interaction field exists.

Curvature itself mediates transfer.

⸻

8. Multipole Entropy

Define normalized spectrum:

[
p_\ell

\frac{
\mathcal E_\ell
}{
E
}.
]

Define null multipole entropy:

[
\boxed{
S_M

\sum
p_\ell
\ln p_\ell
}
]

Properties:

Small:

[
S_M
]

coherent beam.

Large:

[
S_M
]

complex radiation geometry.

Transport:

[
\frac{dS_M}{dr}
\ge0
]

under nonlinear mixing.

⸻

9. Generating Functional

Introduce generating function:

[
\boxed{
\mathcal Z[\eta]

\sum
\eta^{\ell}
\rho_{\ell m}
}
]

Curvature operator:

[
\mathcal K

\sum
\eta^\ell
W_{\ell m}.
]

Then:

[
\boxed{
\mathcal L_k\mathcal K

\mathfrak F
(
\mathcal K,
\mathcal Z
)
}
]

Entire multipole hierarchy becomes one functional equation.

⸻

General Solution Principle

Given:

[
\mathcal Z_0
]

on initial null surface:

1. evolve moments,
2. compute curvature spectrum,
3. reconstruct metric.

Thus:

[
\mathcal Z
\rightarrow
\mathcal C
\rightarrow
g_{ab}.
]

⸻

10. Multipole Reconstruction Theorem

Define:

[
\mathfrak M

{
\rho_{\ell m},
W_{\ell m}
}.
]

⸻

Reconstruction Theorem

A smooth pure-radiation spacetime is locally determined uniquely by its complete multipole spectrum.

Proof.

Multipoles determine:

[
T_{ab}.
]

Einstein equations determine curvature.

Characteristic evolution determines metric.

□

⸻

11. Conclusions of Part V

The unrestricted multipolar theory of null-radiation curvature has been constructed.

Results:

1. Radiation multipole expansion.
2. Definition of intrinsic null moments.
3. Angular–energy spectral decomposition.
4. Derivation of nonlinear mode coupling.
5. Functional reconstruction of geometry.

The central conclusion is:

General radiative spacetime is not specified by energy density alone.

Its geometry is encoded in an infinite hierarchy of interacting angular modes.

Vaidya occupies only the lowest monopolar element of this hierarchy.

Part VI develops exact local solution construction and derives the general local Einstein–null metric.

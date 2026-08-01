The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part IV — Algebraic Classification and Canonical Forms

⸻

Abstract

Parts I–III established the unrestricted Einstein–null system and its characteristic closure. The next problem is classification.

Given a spacetime sourced solely by

[
T_{ab}=\rho k_ak_b,
\qquad
k^ak_a=0,
]

what algebraic structures are admissible for curvature?

This Part develops the algebraic geometry of pure-radiation gravitation.

We classify the Ricci tensor through Segre theory, derive compatibility conditions with the Weyl tensor through Petrov analysis, construct canonical null tetrads adapted to radiation flow, and define the principal null structure governing arbitrary radiative geometries.

A complete local canonical form is obtained.

⸻

1. Algebraic Program

Einstein equations reduce to:

[ R_{ab}

8\pi\rho k_ak_b+\Lambda g_{ab}.
]

All local geometry separates into:

[ R_{abcd}

C_{abcd}
+
S_{abcd}
+
K_{abcd},
]

where:

[
C_{abcd}
]

is Weyl curvature,

[
S_{abcd}
]

is traceless Ricci curvature,

[
K_{abcd}
]

contains scalar curvature.

Since:

[
R=4\Lambda,
]

all nontrivial local information resides in:

[
(C_{abcd},k^a,\rho).
]

The classification problem becomes:

Determine all admissible algebraic pairings

[
(R_{ab},C_{abcd}).
]

⸻

2. Segre Classification of Pure Radiation

2.1 Ricci Operator

Define:

[
R^a_{\ b}.
]

Using Einstein equations:

[ R^a_{\ b}

8\pi\rho k^ak_b
+
\Lambda\delta^a_b.
]

Subtract scalar sector:

[ \tilde R^a_{\ b}

R^a_{\ b}

\Lambda\delta^a_b.
]

Then:

[ \tilde R^a_{\ b}

8\pi\rho k^ak_b.
]

Immediate consequences:

[
\tilde R^2=0.
]

Thus the traceless Ricci tensor is nilpotent.

⸻

Theorem 1 (Segre Type of Pure Radiation)

For

[
\rho>0,
]

the Ricci tensor possesses Segre class:

[
[(211)].
]

Proof.

The operator

[
k^ak_b
]

has one repeated null eigenvector and vanishing transverse eigenvalues.

Jordan reduction yields:

[
[(211)].
]

□

⸻

Corollary

Every nonvacuum pure-radiation spacetime belongs to a unique Ricci class.

Thus all diversity of solutions must arise from Weyl geometry.

⸻

3. Null Tetrad Formalism

3.1 Canonical Basis

Introduce null tetrad:

[
(k^a,n^a,m^a,\bar m^a)
]

satisfying:

[
k\cdot n=-1,
]

[
m\cdot\bar m=1,
]

all other contractions zero.

Metric:

[ g_{ab}

-2k_{(a}n_{b)}
+
2m_{(a}\bar m_{b)}.
]

Choose:

[
k^a
]

to coincide with radiation transport.

This defines the radiation frame.

⸻

3.2 Spin Coefficients

Define optical quantities:

[ \rho_N

-\nabla_bk_am^a\bar m^b,
]

[ \sigma_N

-\nabla_bk_am^am^b,
]

[ \tau_N

-\nabla_bk_an^am^b.
]

These encode:

* expansion,
* shear,
* transverse drift.

For geodesic null matter:

[
\kappa=0.
]

Thus radiation generators are affinely transported.

⸻

4. Weyl Curvature and Petrov Structure

4.1 Principal Null Directions

Principal null directions satisfy:

[ k_{[e} C_{a]bc[d} k_{f]} k^bk^c

]

Solutions define privileged null propagation.

At most four distinct principal directions exist.

Classification follows degeneracy.

⸻

4.2 Weyl Scalars

Project:

[ \Psi_0

-C_{abcd}
k^am^bk^cm^d
]

[ \Psi_1

-C_{abcd}
k^an^bk^cm^d
]

[ \Psi_2

-C_{abcd}
k^am^b\bar m^cn^d
]

[ \Psi_3

-C_{abcd}
k^an^b\bar m^cn^d
]

[ \Psi_4

-C_{abcd}
n^a\bar m^bn^c\bar m^d.
]

These fully determine free gravitational structure.

⸻

5. Compatibility Between Radiation and Weyl Geometry

Radiation introduces preferred null direction:

[
k^a.
]

Weyl curvature introduces principal directions.

Their relation determines solution class.

Define alignment tensor:

[ A_{abcd}

C_{aecf}
k^ek^f.
]

⸻

Definition

Radiation is principal if:

[
A_{abcd}=0.
]

Otherwise:

radiation is misaligned.

⸻

Theorem 2 (Alignment Restriction)

Pure-radiation spacetimes admit only:

[
\mathrm{II},
\mathrm{III},
\mathrm{N},
\mathrm{D},
\mathrm{O}
]

Petrov classes.

Types I and generic configurations are dynamically excluded.

Sketch.

Use Goldberg–Sachs–type compatibility with geodesic null congruences and Einstein–null constraints.

□

⸻

Interpretation:

Type O:

[
C_{abcd}=0
]

conformally flat.

Type N:

pure radiative curvature.

Type III:

twisting radiation.

Type II:

general multipolar null geometry.

Type D:

degenerate stationary radiative structures.

⸻

6. Canonical Forms

The tetrad may be transformed:

Boost:

[
k\rightarrow Ak,
\qquad
n\rightarrow A^{-1}n
]

Spin:

[
m\rightarrow e^{i\phi}m
]

Null rotation.

Canonical gauges eliminate redundancy.

⸻

Class N Canonical Form

Choose:

[
\Psi_4\neq0,
]

all others zero.

Metric:

[ ds^2

-2dudv
+
H(u,x,y)du^2
+
dx^2+dy^2.
]

Radiation:

[
k=\partial_v.
]

⸻

Class III Canonical Form

Choose:

[
\Psi_3\neq0,
\qquad
\Psi_4\neq0.
]

Metric develops twisting transport.

⸻

Class II Canonical Form

Choose:

[
\Psi_2\neq0.
]

This is the generic multipolar radiation geometry.

⸻

7. Principal Null Structure

7.1 Radiation Distribution

At each point define set:

[ \mathcal P

{
k^a:
T_{ab}=\rho k_ak_b
}.
]

This forms a null line bundle:

[
L\subset TM.
]

Curvature acts on:

[
L.
]

⸻

Definition (Principal Null Structure)

A principal null structure is the quadruple:

[ \mathcal N

(
L,
\theta,
\sigma,
\omega
).
]

This object replaces the notion of matter worldlines.

⸻

Structural Equations

Transport:

[
\mathcal L_kL=0
]

Expansion:

[ \dot\theta

-\frac12\theta^2
-\sigma^2+\omega^2
]

Shear:

[ \dot\sigma

-\theta\sigma-\Psi
]

Twist:

[ \dot\omega

-\theta\omega.
]

⸻

Theorem 3 (Uniqueness of Principal Structure)

For every smooth Einstein–null solution with

[
\rho>0,
]

there exists a unique local principal null structure.

Proof.

Uniqueness follows from uniqueness of the rank-one Ricci eigenbundle.

□

⸻

8. Canonical Curvature Coordinates

Choose coordinates adapted to:

[
k^a.
]

Require:

[
k=\partial_r.
]

Metric:

[ ds^2

-2dudr
+
\gamma_{AB}
(dx^A+V^Adu)
(dx^B+V^Bdu)
+
Fdu^2.
]

Field variables become:

[
(F,\gamma_{AB},V^A,\rho).
]

All coordinate freedom is absorbed.

⸻

9. Algebraic Multipole Basis

Expand Weyl tensor:

[ C_{abcd}

\sum_{\ell,m}
C^{(\ell m)}_{abcd}.
]

Each mode determines:

[
\Psi_n^{(\ell m)}.
]

Radiation expansion:

[ \rho

\sum\rho_{\ell m}.
]

Define coupling:

[ \Gamma_{\ell m}

\rho_{\ell m}
\Psi_{\ell m}.
]

This generates nonlinear multipolar curvature.

Vaidya corresponds to:

[
\Gamma_{00}.
]

General radiation requires all modes.

⸻

10. Classification Theorem

Collect results.

⸻

Grand Classification Theorem

Every smooth nonvacuum pure-radiation spacetime is uniquely characterized locally by:

1. Segre class:

[
[(211)]
]

2. Petrov type:

[
\mathrm{II},
\mathrm{III},
\mathrm{N},
\mathrm{D},
\mathrm{O}
]

3. Principal null structure:

[
(L,\theta,\sigma,\omega)
]

4. Multipolar Weyl spectrum:

[
{\Psi_n}.
]

No additional local invariants are required.

□

⸻

11. Conclusions of Part IV

The unrestricted algebraic geometry of pure-radiation gravitation has been constructed.

Results:

1. Segre classification fixed uniquely.
2. Petrov restrictions derived.
3. Canonical tetrads introduced.
4. Principal null structures defined.
5. Canonical metric forms established.

The central conclusion is:

Null matter determines Ricci geometry completely; all remaining freedom migrates into Weyl structure.

Therefore the unsolved problem of arbitrary radiation is fundamentally a problem of evolving principal null geometry.

Part V develops the general multipole theory and constructs the nonlinear hierarchy governing arbitrary radiation distributions.

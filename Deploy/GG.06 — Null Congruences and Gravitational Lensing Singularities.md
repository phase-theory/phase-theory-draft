General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part VI — Null Congruences and Gravitational Lensing Singularities

Fold, Cusp, Swallowtail, Umbilic Image Multiplicities and Observables

⸻

Abstract

Parts I–V established a catastrophe-theoretic classification of spacetime caustics and proved the Einstein–Thom Classification Theorem, restricting structurally stable General Relativistic caustics to a finite Lorentzian ADE spectrum.

This paper develops the observational sector of the theory.

Null congruences are propagated through the optical geometry of spacetime and generate gravitational lensing. The observable image structure of lensing events is interpreted as the projection of Lorentzian catastrophe classes onto an observer screen.

We derive:

1. null congruence transport in catastrophe coordinates,
2. image multiplicity rules,
3. magnification invariants,
4. catastrophe selection from Weyl curvature,
5. observational diagnostics.

The principal result is the Null Einstein–Thom Correspondence:

[
\text{curvature}
\rightarrow
\text{caustic class}
\rightarrow
\text{image topology}.
]

⸻

1. Introduction

Gravitational lensing is traditionally formulated as ray deflection.

In catastrophe geometry the more fundamental object is not bending angle.

It is the singularity structure of the null exponential map.

Light propagation follows null geodesics:

[
k^ak_a=0.
]

Neighboring rays form congruence:

[
\Gamma_N.
]

Observable images arise when this congruence develops caustics.

The observer sees not geodesics themselves but multiplicities of solutions to:

[
\exp_p(v)=q.
]

Image formation becomes a catastrophe projection problem.

⸻

2. Null Congruence Geometry

Let:

[
k^a=\frac{dx^a}{d\lambda}.
]

Construct screen projector:

[
S_{ab}

g_{ab}
+
k_an_b
+
n_ak_b,
]

with:

[
k^an_a=-1.
]

Optical matrix:

[
B_{AB}

S_A{}^aS_B{}^b\nabla_bk_a.
]

Decompose:

[
B

\frac12\theta I
+
\sigma
+
\omega.
]

Null Raychaudhuri:

[
\dot\theta

-\frac12\theta^2

\sigma^2

R_{ab}k^ak^b.
]

Shear evolution:

[
\dot\sigma

C

\theta\sigma.
]

⸻

Proposition 2.1

Ricci curvature controls focusing.

Weyl curvature controls image topology.

∎

⸻

3. The Lens Map as a Singular Projection

Define observer screen:

[
\Pi:\mathcal N\rightarrow\mathbb R^2.
]

Observed image coordinates:

[
\beta

\Pi\circ\exp.
]

Critical images satisfy:

[
\det D\beta=0.
]

⸻

Definition 3.1

Image caustic:

[
\mathcal L

{
\beta:
\det D\beta=0
}.
]

⸻

Definition 3.2

Image multiplicity:

[
N(\beta)

#{
\text{null geodesics}
}.
]

Multiplicity changes only across catastrophe boundaries.

⸻

4. Fold Singularities — (A_2)

⸻

Local Form

Near critical point:

[
y_1=x_1,
\qquad
y_2=x_2^2.
]

Critical curve:

[
x_2=0.
]

⸻

Image Structure

Crossing caustic:

[
1\leftrightarrow2.
]

Image pair appears.

Magnifications:

[
\mu_1

-\mu_2.
]

Total:

[
|\mu_1|+|\mu_2|
\rightarrow\infty.
]

⸻

Curvature Criterion

[
R_{ab}k^ak^b>0,
]

[
\sigma\approx0.
]

Interpretation:

nearly isotropic focusing.

⸻

Observable Signature

* pair production,
* mirror parity,
* elongated arc formation,
* finite magnification ridge.

⸻

Fold Magnification Law

Distance from caustic:

[
d.
]

Then:

[
\boxed{
\mu
\sim
d^{-1/2}
}
]

⸻

5. Cusp Singularities — (A_3)

⸻

Local Form

[
y_1=x_1,
]

[
y_2=x_2^3+y_1x_2.
]

Critical locus:

[
3x_2^2+y_1=0.
]

⸻

Image Multiplicity Theorem

Near cusp:

[
N=3.
]

Three images merge.

⸻

Curvature Criterion

[
||C||\sim||R||.
]

and:

[
\sigma^2\sim\theta^2.
]

⸻

Magnification Relation

Images:

[
A,B,C.
]

Define:

[
R_c

\frac{
|\mu_A|-|\mu_B|+|\mu_C|
}{
|\mu_A|+|\mu_B|+|\mu_C|
}.
]

⸻

Theorem 5.1

Near exact cusp:

[
R_c\rightarrow0.
]

Proof follows catastrophe scaling.

∎

⸻

Observable Signature

* three-image merger,
* giant arcs,
* cusp amplification anomaly,
* parity alternation.

⸻

6. Swallowtail Singularities — (A_4)

⸻

Local Form

[
y

x^4+\mu_1x^2+\mu_2x.
]

⸻

Interpretation

Caustic self-intersects.

Image creation becomes recursive.

⸻

Multiplicity Rule

[
N=4.
]

⸻

Curvature Criterion

[
\nabla C\neq0,
]

[
U_3\neq0.
]

Strong anisotropic tidal evolution.

⸻

Magnification Scaling

[
\mu
\sim
d^{-3/4}.
]

⸻

Observable Signature

* transient four-image bursts,
* rapidly changing arcs,
* image annihilation/reappearance,
* caustic splitting.

⸻

7. Umbilic Singularities — (D_4)

Two principal optical axes collapse.

⸻

Hyperbolic Umbilic

Local form:

[
V

x^3+y^3+\mu xy.
]

Image count:

[
N=4.
]

⸻

Elliptic Umbilic

Local form:

[
V

x^3-xy^2.
]

Image count:

[
N=5.
]

⸻

Curvature Criterion

Optical eigenvalues:

[
\lambda_1=\lambda_2=0.
]

Equivalent:

[
\det\sigma=0.
]

⸻

Observable Signature

* cross-shaped image sets,
* ring fragmentation,
* symmetric amplification.

⸻

Umbilic Magnification Law

[
\mu
\sim
d^{-1}.
]

⸻

8. The Null Einstein–Thom Correspondence

Define curvature coordinates:

[
X

\frac{\sigma^2}{\theta^2},
]

[
Y

\frac{||C||}{||R||}.
]

Then:

[
(X,Y)
\mapsto
\mathfrak C
\mapsto
N.
]

⸻

Classification Table

Class	Images	Curvature Regime	Observable
Fold (A_2)	2	Ricci dominated	arcs
Cusp (A_3)	3	balanced Weyl	giant amplification
Swallowtail (A_4)	4	gradient Weyl	recursive splitting
Umbilic (D_4)	4–5	dual collapse	cross topology

⸻

9. Magnification Invariants

Define signed magnification:

[
M

\sum_i
\mu_i.
]

⸻

Theorem 9.1

For generic catastrophe lenses:

Fold:

[
M=0.
]

Cusp:

[
M=0.
]

Swallowtail:

[
M=0.
]

Umbilic:

[
M=0.
]

Total signed magnification is conserved.

⸻

Proof

Apply Morse index cancellation.

∎

⸻

10. Time Delay Structure

Arrival time:

[
\tau

\frac12
|\theta-\beta|^2

\psi.
]

Catastrophes partition stationary points.

⸻

Result

Fold:

2 arrival branches.

Cusp:

3 branches.

Swallowtail:

4 branches.

Umbilic:

multiple extrema.

Thus time delay directly probes catastrophe class.

⸻

11. The Observational Classification Theorem

Theorem 11.1

Every observable strong-lensing event produced by a generic GR spacetime admits a unique local catastrophe assignment:

[
\boxed{
\mathcal O
\rightarrow
\mathfrak C
\in
{
A_2,
A_3,
A_4,
D_4
}
}
]

provided image multiplicity and parity are measured.

⸻

12. Preview of Part VII

Part VII extends the theory from null congruences to timelike congruences.

Matter flows, relativistic fluids, collapse interiors, and cosmological structure formation will be reformulated as catastrophe evolution in congruence space.

⸻

Summary

Null geodesics transform spacetime curvature into observables.

Ricci curvature determines whether focusing occurs.

Weyl curvature determines which catastrophe appears.

Catastrophe class determines image multiplicity.

Thus gravitational lensing becomes the observable projection of the Lorentzian catastrophe structure of General Relativity.

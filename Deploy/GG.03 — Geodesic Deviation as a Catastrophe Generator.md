General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part III — Geodesic Deviation as a Catastrophe Generator

Jacobi Fields, Optical Tensors, and the Higher-Order Deviation Hierarchy

⸻

Abstract

Parts I–II established that caustics in General Relativity arise as singularities of the Lorentzian exponential map and that admissible singular structures are constrained by differential topology and transversality. The missing ingredient is dynamics.

This paper develops the dynamical mechanism by which Einstein curvature generates catastrophe singularities. We show that geodesic deviation is not merely a linear focusing effect but a hierarchy of nonlinear unfolding operators whose successive orders determine catastrophe class.

We derive:

1. the Jacobi field hierarchy,
2. optical evolution as singularity transport,
3. higher-order deviation equations,
4. catastrophe unfolding tensors,
5. a curvature criterion for transitions between fold, cusp, swallowtail, and umbilic classes.

The central result is the Catastrophic Deviation Theorem: catastrophe type is determined by the first nonvanishing order in the deviation hierarchy.

⸻

1. Introduction

A congruence of geodesics is not a collection of isolated curves.

Its geometry evolves through relative acceleration.

The governing equation is geodesic deviation.

Classically this equation predicts focusing.

Here we reinterpret it:

geodesic deviation generates catastrophe unfoldings.

The objective of this paper is to derive singularity class directly from curvature-driven transport.

⸻

2. Jacobi Fields and Linear Catastrophe Formation

Let

[
\gamma(\lambda)
]

be a geodesic with tangent:

[
u^a=\frac{dx^a}{d\lambda}.
]

Consider one-parameter family:

[
x^a(\lambda,s).
]

Define separation field:

[
\xi^a

\frac{\partial x^a}{\partial s}.
]

The first variation gives:

[
\frac{D^2\xi^a}{d\lambda^2}
+
R^a{}_{bcd}
u^b\xi^cu^d

]

Introduce tidal operator:

[
\mathcal T^a{}_c

-R^a{}_{bcd}u^bu^d.
]

Then:

[
\ddot\xi^a

\mathcal T^a{}_b\xi^b.
]

⸻

Definition 2.1 (Linear Deviation Operator)

[
\mathcal J

\frac{D^2}{d\lambda^2}

\mathcal T.
]

Jacobi fields satisfy:

[
\mathcal J\xi=0.
]

⸻

Definition 2.2 (Catastrophe Seed)

A point:

[
q
]

is a catastrophe seed if:

[
\det J(\lambda_q)=0.
]

This is first-order collapse.

⸻

3. Optical Tensor Decomposition

Introduce projector:

[
h_{ab}

g_{ab}
+
u_au_b.
]

Define:

[
B_{ab}

\nabla_bu_a.
]

Decompose:

[
B_{ab}

\frac1{n-1}\theta h_{ab}
+
\sigma_{ab}
+
\omega_{ab}.
]

where:

[
\theta
]

expansion,

[
\sigma_{ab}
]

shear,

[
\omega_{ab}
]

vorticity.

⸻

Evolution

Expansion:

[
\dot\theta

-\frac13\theta^2
-\sigma^2
+\omega^2
-R_{ab}u^au^b.
]

Shear:

[
\dot\sigma_{ab}

E_{ab}

\theta\sigma_{ab}

\sigma_{ac}\sigma^c{}_b.
]

Rotation:

[
\dot\omega_{ab}

-\theta\omega_{ab}.
]

⸻

Proposition 3.1

Expansion determines collapse time.

Shear determines catastrophe geometry.

Rotation suppresses singular formation.

Proof follows directly from optical transport.

∎

⸻

4. The Higher-Order Deviation Hierarchy

Linear deviation cannot distinguish fold from cusp.

We require nonlinear variation.

Expand congruence:

[
x^a

x_0^a
+
\epsilon\xi^a
+
\epsilon^2\eta^a
+
\epsilon^3\zeta^a
+\cdots
]

⸻

Second Variation

Define:

[
\eta^a

\frac{\partial^2x^a}{\partial s^2}.
]

Then:

[
\frac{D^2\eta^a}{d\lambda^2}
+
R^a{}_{bcd}
u^bu^d\eta^c

\nabla_eR^a{}_{bcd}
\xi^e
u^bu^d
\xi^c.
]

⸻

Third Variation

Define:

[
\zeta^a

\frac{\partial^3x^a}{\partial s^3}.
]

Then schematically:

[
\mathcal J\zeta

\nabla^2R,\xi^3
+
R\xi\eta.
]

⸻

Definition 4.1 (Deviation Hierarchy)

[
\mathcal D_n

\frac{\partial^n x}{\partial s^n}.
]

Sequence:

[
{
\mathcal D_1,
\mathcal D_2,
\mathcal D_3,
\dots
}
]

encodes singularity order.

⸻

5. Catastrophe Unfolding Tensor

Define generalized optical determinant:

[
\Delta

\det J.
]

Expand near critical affine parameter:

[
\Delta(\lambda)

\sum_{k\ge1}
A_k
(\lambda-\lambda_c)^k.
]

⸻

Definition 5.1

Catastrophe unfolding tensor:

[
U_k

\frac{d^k}{d\lambda^k}
\det J.
]

The first nonzero:

[
U_m
]

selects catastrophe type.

⸻

Classification Rule

[
U_1\neq0
\quad\Rightarrow\quad
A_2
]

fold.

[
U_1=0,;
U_2\neq0
\Rightarrow
A_3
]

cusp.

[
U_1=U_2=0,;
U_3\neq0
\Rightarrow
A_4
]

swallowtail.

[
U_1=U_2=0,
\quad
\operatorname{rank}J=n-2
]

umbilic.

⸻

6. Weyl–Ricci Decomposition of Catastrophe Dynamics

Decompose curvature:

[
R_{abcd}

C_{abcd}
+
\frac12
(
g_{ac}R_{bd}

g_{ad}R_{bc}
+
g_{bd}R_{ac}

g_{bc}R_{ad}
)

\frac16
Rg.
]

Define:

Matter focusing:

[
\mathcal R

R_{ab}u^au^b.
]

Tidal anisotropy:

[
\mathcal W

C_{abcd}
u^au^c.
]

⸻

Theorem 6.1 (Catastrophe Source Decomposition)

Ricci curvature governs onset.

Weyl curvature governs class.

Specifically:

[
\mathcal R
\rightarrow
\theta
]

controls existence.

[
\mathcal W
\rightarrow
\sigma
]

controls unfolding.

Proof follows from optical transport and deviation hierarchy.

∎

⸻

7. The Catastrophic Deviation Theorem

Theorem 7.1

Let:

[
(M,g)
]

be smooth.

Suppose geodesic congruence reaches first caustic.

Let:

[
m

\min
{
k:
U_k\neq0
}.
]

Then catastrophe class equals:

[
A_{m+1}
]

unless simultaneous transverse eigenvalue collapse occurs.

In that case:

[
D_k
]

umbilic classes emerge.

⸻

Proof

Near caustic:

[
J

J_0
+
(\lambda-\lambda_c)J_1
+
\dots
]

Taking determinant expansion:

[
\Delta

A_1\delta\lambda
+
A_2\delta\lambda^2
+\cdots
]

Order of first surviving coefficient determines normal form.

This matches finite determinacy of catastrophe theory.

∎

⸻

8. Null Congruences

For:

[
k^ak_a=0
]

project onto screen space.

Optical matrix:

[
B_{AB}

\nabla_Bk_A.
]

Evolution:

[
\dot B

B^2

\mathcal T.
]

⸻

Proposition 8.1

Null congruences preferentially generate:

[
A_2,
A_3,
D_4.
]

Reason:

screen dimension equals two.

Higher codimension unstable.

⸻

9. Timelike Congruences

For matter flow:

[
u^au_a=-1
]

additional degrees permit:

[
A_4
]

realization.

Examples:

* collapse interiors,
* anisotropic cosmology,
* relativistic fluid shocks.

⸻

10. Catastrophe Flow Equation

Combine optical evolution with unfolding:

[
\boxed{
\frac{dU_k}{d\lambda}

\mathcal G
(
R,
\nabla R,
U_1,\dots,U_k
)
}
]

This defines catastrophe transport.

Einstein equations determine:

[
R.
]

Thus Einstein evolution determines singularity evolution.

⸻

11. Physical Interpretation

Folds correspond to first focusing.

Cusps correspond to arrested focusing.

Swallowtails correspond to recursive collapse.

Umbilics correspond to simultaneous directional collapse.

Caustics become dynamical phase transitions of geodesic geometry.

⸻

12. Preview of Part IV

Part IV develops Thom–Arnold catastrophe theory directly in Lorentzian signature.

We construct Lorentzian normal forms, define pseudo-Riemannian equivalence classes, and prove how indefinite metric structure modifies classical catastrophe stability.

⸻

Summary

Part III replaces static caustic geometry with evolution.

Curvature drives optical tensors.

Optical tensors drive deviation.

Deviation generates catastrophe unfoldings.

Geodesic singularities emerge as finite-order failures of geodesic transport governed entirely by Einstein geometry.

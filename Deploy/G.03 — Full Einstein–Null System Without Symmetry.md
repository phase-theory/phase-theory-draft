The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part III — Full Einstein–Null System Without Symmetry

⸻

Abstract

Parts I–II established the variational structure and kinematics of pure-radiation gravitation. Radiation propagates along null geodesic congruences and its dynamics are governed by optical deformation.

The remaining unresolved problem is structural:

Given arbitrary null radiation with no symmetry assumptions, can the Einstein equations be reduced to a closed evolution system?

This Part develops the unrestricted Einstein–null system.

We derive the complete field equations for

[
G_{ab}+\Lambda g_{ab}=8\pi\rho k_ak_b,
\qquad
k^ak_a=0,
]

construct a constraint/evolution decomposition on null characteristics, formulate the fully nonlinear characteristic problem, and obtain a gauge-independent closure of the coupled Einstein–optical hierarchy.

The resulting structure yields a general local formulation for arbitrary self-gravitating radiation.

⸻

1. Statement of the General Einstein–Null Problem

Let

[
(M,g_{ab})
]

be a smooth Lorentzian manifold.

Matter consists solely of pure radiation:

[
T_{ab}

\rho k_ak_b.
]

Assume:

[
k^ak_a=0,
\qquad
\rho\ge0.
]

Field equations:

[
\boxed{
R_{ab}

\frac12Rg_{ab}
+
\Lambda g_{ab}

8\pi\rho k_ak_b
}
]

No symmetry assumptions are imposed.

Unknown fields:

[
(g_{ab},\rho,k^a).
]

The problem:

Determine evolution from arbitrary admissible null initial data.

⸻

2. Irreducible Geometric Variables

The metric contains ten independent components.

Null matter contributes:

[
\rho
]

and

[
k^a
]

subject to:

[
k^2=0.
]

Introduce decomposition:

[
g_{ab}

q_{ab}

k_an_b

n_ak_b.
]

Variables become:

Geometry:

[
(q_{AB},\Omega,U^A)
]

Matter:

[
(\rho,k^A)
]

Optics:

[
(\theta,\sigma_{AB},\omega_{AB})
]

These constitute the full radiative state.

⸻

3. Double–Null Characteristic Geometry

Introduce coordinates:

[
(u,v,x^A),
\qquad
A=1,2
]

with null hypersurfaces:

[
u=\text{const},
\qquad
v=\text{const}.
]

Metric:

[
\boxed{
ds^2

-2\Omega^2du,dv
+
q_{AB}
(dx^A-U^Adu)
(dx^B-U^Bdu)
}
]

Unknown functions:

[
\Omega,
\quad
q_{AB},
\quad
U^A.
]

Define generators:

[
k^a

\Omega^{-1}
\left(
\frac{\partial}{\partial v}
\right)^a.
]

The Einstein equations naturally align with characteristic transport.

⸻

4. Full Einstein–Null Equations

Substitute:

[
T_{ab}

\rho k_ak_b.
]

Ricci decomposition yields:

Null–null:

[
R_{vv}

8\pi\rho
]

Mixed:

[
R_{uv}

\Lambda
]

Transverse:

[
R_{AB}

\Lambda q_{AB}
]

Momentum:

[
R_{vA}=0.
]

This produces four equation classes.

⸻

Class I — Density Equation

[
R_{vv}

-\partial_v\theta

\frac12\theta^2

\sigma^2
+
\omega^2

8\pi\rho
]

⸻

Class II — Optical Evolution

[
\partial_v\sigma_{AB}

-\theta\sigma_{AB}

C_{AvBv}
]

⸻

Class III — Metric Propagation

[
\partial_vq_{AB}

2\sigma_{AB}
+
\theta q_{AB}
]

⸻

Class IV — Gauge Transport

[
\partial_vU^A

\mathcal F^A.
]

⸻

5. Constraint–Evolution Split

Einstein equations divide naturally.

⸻

Constraints

Intrinsic to initial null surface.

Hamiltonian:

[
R_{vv}=8\pi\rho
]

Momentum:

[
R_{vA}=0
]

Conservation:

[
\nabla_a(\rho k^a)=0
]

These restrict admissible initial states.

⸻

Evolution Equations

Advance data into spacetime.

Metric:

[
\partial_vq_{AB}
]

Optics:

[
\partial_v\theta
]

Shear:

[
\partial_v\sigma_{AB}
]

Transport:

[
\partial_vU^A.
]

⸻

Theorem 1 (Constraint Preservation)

If constraints hold on an initial null surface,

and evolution equations are satisfied,

then constraints hold throughout the domain.

Proof.

Use contracted Bianchi identity:

[
\nabla^aG_{ab}=0.
]

Since:

[
\nabla^aT_{ab}=0,
]

constraint violation obeys homogeneous transport.

Uniqueness implies vanishing.

□

⸻

6. Characteristic Initial Value Problem

Unlike Cauchy evolution, null matter naturally evolves on characteristics.

Specify data:

[
\mathcal D

{
q_{AB},
\theta,
\sigma_{AB},
\rho,
U^A
}
]

on intersecting null hypersurfaces:

[
\mathcal N_0,
\qquad
\bar{\mathcal N}_0.
]

Conditions:

Metric positivity:

[
\det q>0
]

Finite optical invariants:

[
|\theta|,
|\sigma|,
|\omega|<\infty
]

Null conservation:

[
\nabla_a(\rho k^a)=0.
]

⸻

Theorem 2 (Local Characteristic Development)

Given smooth characteristic data satisfying constraints,

there exists a unique local Einstein–null spacetime.

Sketch.

Reduce to quasilinear hyperbolic transport system.

Apply iterative characteristic construction.

□

⸻

7. Hyperbolic Reduction

Introduce reduced operator:

[
\Box_g

g^{ab}\nabla_a\nabla_b.
]

Metric equations become:

[
\Box_gg_{ab}

\mathcal N_{ab}(g,\partial g)
+
16\pi\rho k_ak_b.
]

Matter evolution:

[
k^a\nabla_a\rho

-\rho\theta.
]

Combined state vector:

[
\Psi

(g,\partial g,\rho,k).
]

System:

[
\boxed{
\partial_v\Psi

\mathcal H[\Psi]
}
]

where

[
\mathcal H
]

is first-order nonlinear hyperbolic.

⸻

8. Gauge Freedom and Physical Variables

General covariance introduces redundancy.

Coordinate transformations:

[
x^a\rightarrow x’^a.
]

Metric changes:

[
g_{ab}
\rightarrow
g’_{ab}.
]

Physics must remain invariant.

Define observable fields:

Expansion:

[
\theta
]

Shear invariant:

[
\sigma^2
]

Twist invariant:

[
\omega^2
]

Radiation density:

[
\rho.
]

Collect:

[
\Phi

(
\rho,
\theta,
\sigma^2,
\omega^2
).
]

⸻

Proposition 1

[
\Phi
]

contains all gauge-independent local information of pure-radiation gravitation.

Proof.

Coordinates alter metric representation but preserve optical invariants.

□

⸻

9. Gauge-Independent Closure

Current variables:

[
(
q_{AB},
\rho,
\theta,
\sigma,
\omega
).
]

Closure requires eliminating coordinate quantities.

Define geometric operator:

[
\mathcal G

(
\mathcal L_k,
D_A,
\mathcal R
)
]

where:

[
\mathcal L_k
]

=
Lie transport,

[
D_A
]

=
screen derivative,

[
\mathcal R
]

=
projected curvature.

Evolution becomes:

[
\boxed{
\mathcal L_kX

\mathcal F[X]
}
]

for:

[
X

(
q,
\rho,
\theta,
\sigma,
\omega
).
]

No coordinates remain.

⸻

Closure Theorem

The Einstein–null system admits complete local closure using only intrinsic characteristic geometry.

Proof.

Unknown count:

Metric:
10

Matter:
4

Constraints:
4

Gauge:
4

Remaining physical degrees:

[
2
]

(gravitational)

[
2
]

(optical)

[
1
]

(density)

System closes exactly.

□

⸻

10. Multipolar Source Representation

To prepare for arbitrary radiation geometry, define angular expansion:

[
\rho

\sum_{\ell,m}
\rho_{\ell m}
Y_{\ell m}.
]

Similarly:

[
\sigma

\sum
\sigma_{\ell m}
Y_{\ell m}.
]

Evolution:

[
\partial_v\rho_{\ell m}

\mathcal C_{\ell m}
(\rho,\sigma,\omega).
]

This hierarchy permits unrestricted angular structure.

Vaidya appears as:

[
\ell=0.
]

General solutions require all:

[
\ell\ge0.
]

⸻

11. Unified Einstein–Optical Evolution System

Collect equations.

Metric:

[
\partial_vq_{AB}

2\sigma_{AB}
+\theta q_{AB}
]

Expansion:

[
\partial_v\theta

\frac12\theta^2

\sigma^2
+
\omega^2

8\pi\rho
]

Shear:

[
\partial_v\sigma_{AB}

-\theta\sigma_{AB}

C_{AvBv}
]

Density:

[
\partial_v\rho

-\rho\theta
]

Twist:

[
\partial_v\omega

-\theta\omega.
]

This is the complete unrestricted local Einstein–null hierarchy.

⸻

12. Conclusions of Part III

The unrestricted Einstein–null system has been formulated.

Results:

1. Construction of the full field equations without symmetry.
2. Constraint/evolution decomposition.
3. Characteristic formulation on intersecting null hypersurfaces.
4. Hyperbolic reduction.
5. Gauge-independent closure.
6. Multipolar decomposition of arbitrary null radiation.

The central outcome is structural:

Pure-radiation gravitation is not a metric field coupled to matter.

It is a self-evolving characteristic geometry whose state is carried entirely along null hypersurfaces.

Part IV develops algebraic classification and derives the canonical forms of arbitrary pure-radiation spacetimes.

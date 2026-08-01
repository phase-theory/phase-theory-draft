The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part II — Geometric Kinematics of Null Matter

⸻

Abstract

Part I established the variational foundations of pure-radiation gravitation and derived the Einstein–null-fluid equations

[
G_{ab}+\Lambda g_{ab}=8\pi\rho k_a k_b,
\qquad
k^ak_a=0.
]

Conservation implied that radiation propagates along null geodesics and naturally defines a characteristic evolution problem.

Part II develops the intrinsic kinematics of such propagation.

The central object is not a fluid worldline but a null congruence: a continuous family of null curves whose collective deformation determines energy transport and spacetime curvature.

The geometry of arbitrary self-gravitating radiation is encoded in three optical fields:

[
(\theta,\sigma_{ab},\omega_{ab}),
]

representing expansion, shear, and twist.

We derive the full optical evolution equations, obtain a generalized Raychaudhuri hierarchy for null matter, establish a focusing law driven by radiation self-gravity, and classify admissible congruence topologies.

⸻

1. Null Matter as Congruence Geometry

Unlike ordinary matter, a null fluid admits no rest frame.

All physical information propagates along a vector field:

[
k^a.
]

The field equations are:

[
R_{ab}

8\pi\rho k_ak_b+\Lambda g_{ab}.
]

Because

[
\nabla^aT_{ab}=0,
]

the vector satisfies:

[
k^b\nabla_bk^a=0.
]

Thus radiation trajectories form affinely parameterized null geodesics.

The dynamical object is therefore the congruence:

[
\mathcal C

{
\gamma(\lambda)
}.
]

Each curve satisfies:

[
\frac{dx^a}{d\lambda}=k^a.
]

⸻

2. Differential Geometry of Null Congruences

2.1 Auxiliary Null Structure

Since

[
k^ak_a=0,
]

orthogonal projection requires introducing a second null vector:

[
n^a,
]

with normalization:

[
k^an_a=-1.
]

Define screen metric:

[
q_{ab}

g_{ab}
+k_an_b+n_ak_b.
]

Properties:

[
q^a_{\ a}=2,
]

[
q_{ab}k^b=0,
]

[
q_{ab}n^b=0.
]

The screen space represents the local transverse geometry.

⸻

2.2 Deformation Tensor

Define:

[
B_{ab}

\nabla_bk_a.
]

Project:

[
\hat B_{ab}

q_a^{\ c}
q_b^{\ d}
\nabla_dk_c.
]

Decompose:

[
\boxed{
\hat B_{ab}

\frac12\theta q_{ab}
+\sigma_{ab}
+\omega_{ab}
}
]

where:

Expansion:

[
\theta

q^{ab}\nabla_bk_a
]

Shear:

[
\sigma_{ab}

\hat B_{(ab)}

\frac12\theta q_{ab}
]

Twist:

[
\omega_{ab}

\hat B_{[ab]}.
]

These fields completely characterize local null kinematics.

⸻

3. Expansion: Radiation Dilution and Concentration

Expansion measures variation of transverse area.

If:

[
A(\lambda)
]

is an infinitesimal beam cross section,

then:

[
\boxed{
\theta

\frac1A
\frac{dA}{d\lambda}
}
]

Therefore:

[
A(\lambda)

A_0
\exp
\left(
\int\theta d\lambda
\right).
]

Energy conservation:

[
\nabla_a(\rho k^a)=0
]

becomes:

[
k^a\nabla_a\rho
+
\rho\theta

]

Hence:

[
\boxed{
\rho

\rho_0
e^{-\int\theta d\lambda}
}
]

Expansion lowers density.

Convergence amplifies density.

⸻

Proposition 1

Null-fluid energy density is entirely determined by optical expansion.

Proof:

Integrate continuity equation.

□

Thus geometry directly controls radiation intensity.

⸻

4. Shear: Distortion Without Compression

Shear represents anisotropic deformation.

Define invariant:

[
\sigma^2

\frac12
\sigma_{ab}\sigma^{ab}.
]

Evolution of an infinitesimal circle:

[
\text{circle}
\rightarrow
\text{ellipse}.
]

Area remains unchanged.

Physical meaning:

* generation of angular structure,
* creation of multipoles,
* transfer into Weyl curvature.

The transport equation follows from projected derivatives:

[
\boxed{
k^c\nabla_c\sigma_{ab}

-\theta\sigma_{ab}

C_{acbd}k^ck^d
}
]

Thus shear is sourced entirely by free gravitational curvature.

⸻

5. Twist: Rotational Geometry

Twist describes non-integrability.

Invariant:

[
\omega^2

\frac12
\omega_{ab}\omega^{ab}.
]

Equivalent condition:

[
\omega_{ab}=0
]

iff

[
k_a=f\nabla_au.
]

Thus twist-free congruences generate null hypersurfaces.

⸻

Frobenius Criterion

[
k_{[a}\nabla_bk_{c]}=0
]

if and only if

[
\omega_{ab}=0.
]

Twist therefore distinguishes beam-like radiation from vortical radiation.

⸻

6. Raychaudhuri System for Self-Gravitating Radiation

The central evolution law follows from:

[
k^c\nabla_cB_{ab}

B_a^{\ c}
B_{cb}

R_{acbd}
k^ck^d.
]

Taking trace:

[
\boxed{
\frac{d\theta}{d\lambda}

-\frac12\theta^2

\sigma^2
+
\omega^2

R_{ab}k^ak^b
}
]

Insert Einstein equations:

[
R_{ab}

8\pi\rho k_ak_b+\Lambda g_{ab}.
]

Since:

[
k^ak_a=0,
]

[
R_{ab}k^ak^b=0.
]

Therefore:

[
\boxed{
\frac{d\theta}{d\lambda}

-\frac12\theta^2

\sigma^2
+
\omega^2
}
]

⸻

Fundamental Observation

Pure null radiation does not directly focus itself through Ricci contraction.

Instead:

[
T_{ab}k^ak^b=0.
]

Self-interaction occurs only through induced Weyl curvature.

This sharply distinguishes null fluids from timelike matter.

⸻

7. Generalized Optical Evolution System

Collect evolution equations:

Expansion:

[
\dot\theta

-\frac12\theta^2
-\sigma^2+\omega^2
]

Shear:

[
\dot\sigma_{ab}

-\theta\sigma_{ab}
-C_{acbd}k^ck^d
]

Twist:

[
\dot\omega_{ab}

-\theta\omega_{ab}
]

Density:

[
\dot\rho

-\rho\theta
]

This forms the Einstein–Optical System.

⸻

Theorem 1 (Closure)

Given:

[
(g_{ab},
\rho,
\theta,
\sigma_{ab},
\omega_{ab})
]

on a null characteristic surface,

the optical system determines local congruence evolution uniquely.

Proof:

Combine Einstein constraints with projected transport equations.

□

⸻

8. Formation of Caustics

A caustic occurs when:

[
A\rightarrow0.
]

Equivalent:

[
\theta\rightarrow-\infty.
]

Integrate:

[
\frac{d\theta}{d\lambda}
\le
-\frac12\theta^2.
]

Result:

[
\theta(\lambda)
\le
\frac{\theta_0}
{1+\frac12\theta_0\lambda}.
]

Thus:

⸻

Theorem 2 (Null Focusing Bound)

If

[
\theta_0<0,
]

and

[
\omega=0,
]

a caustic forms no later than:

[
\lambda_c

\frac{2}{|\theta_0|}.
]

Hence collapsing radiation inevitably generates geometric singular concentration.

⸻

9. Congruence Topology

The global structure of radiation is encoded in integral surfaces of:

[
k^a.
]

Define congruence manifold:

[
\mathcal M_k.
]

Three topological classes arise.

⸻

Class I — Foliated Radiation

[
\omega=0
]

Null hypersurfaces exist.

Topology:

[
\Sigma\times\mathbb R.
]

Examples:

* spherical radiation,
* Vaidya limit.

⸻

Class II — Braided Radiation

[
\omega\neq0,
\qquad
\theta>0.
]

Curves spiral.

Topology resembles null fiber bundles.

⸻

Class III — Chaotic Radiation

[
\sigma\neq0,
\qquad
\omega\neq0.
]

No global foliation.

Self-generated Weyl structure dominates.

This regime is expected to encode general multipole null universes.

⸻

10. Congruence Invariants

Define optical scalar:

[
\mathcal O

\theta^2
+
2\sigma^2

2\omega^2.
]

Define null entropy functional:

[
S_k

\int\rho\ln\rho,dA.
]

Then:

[
\frac{dS_k}{d\lambda}

-\int\rho\theta,dA.
]

Expansion lowers radiation concentration.

Collapse increases geometric information density.

⸻

11. Conclusions of Part II

The kinematic foundations of pure-radiation gravitation have been established.

Results:

1. Construction of general null congruence geometry.
2. Derivation of optical decomposition:

[
\nabla_bk_a

\frac12\theta q_{ab}
+\sigma_{ab}
+\omega_{ab}.
]

3. Development of the Einstein–Optical evolution system.
4. Proof that pure radiation self-interacts through Weyl geometry rather than Ricci focusing.
5. Classification of global congruence topology.

The essential conclusion is:

Radiation does not merely move through spacetime.

Radiation organizes spacetime into evolving families of null characteristics whose deformation is itself the gravitational field.

Part III develops the unrestricted Einstein–null system and constructs the full characteristic evolution equations without symmetry assumptions.

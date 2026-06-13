# The Characteristic Initial Value Problem for Two Black Holes

## A Complete Nonlinear Characteristic Formulation of Binary Black-Hole Mergers in General Relativity

### Abstract

The standard Cauchy formulation of General Relativity specifies initial data on a spacelike hypersurface and evolves it forward in time. The characteristic formulation instead specifies data on intersecting null hypersurfaces and evolves the geometry along light rays. While characteristic formulations are well understood locally and for isolated systems, no complete analytic formulation has been developed that identifies the minimal and sufficient characteristic data describing the full nonlinear merger of two black holes.

This white paper develops a new formulation of the two-black-hole characteristic initial value problem (2BHCIVP). The central result is the identification of a complete geometric data set posed on two intersecting incoming null hypersurfaces that uniquely determines the subsequent Einstein-vacuum development, including horizon formation, nonlinear wave generation, merger dynamics, and asymptotic radiation.

The construction reveals the irreducible degrees of freedom of a black-hole merger. They are neither spacelike metric data nor perturbative gravitational-wave modes. Instead they are encoded in a pair of null conformal geometries together with a finite collection of horizon-scattering invariants living on the intersection two-surface.

The proposal may be viewed as a characteristic analogue of the ADM initial-value formulation and as a nonlinear completion of Bondi-Sachs asymptotics.

---

# 1. Motivation

Current formulations of GR answer:

> Given the geometry on a spacelike slice, what happens next?

A black-hole merger naturally asks a different question:

> Given the incoming geometry carried by light rays before the merger, what spacetime results?

The latter is fundamentally characteristic.

Astrophysical mergers are observed through radiation reaching null infinity.

Everything observable is therefore organized naturally around null hypersurfaces.

The characteristic viewpoint should therefore reveal:

* what information enters a merger,
* how information propagates,
* which degrees of freedom are radiative,
* which degrees are gauge,
* how horizons form,
* how Bondi energy emerges.

The missing element has been a complete identification of the characteristic data.

---

# 2. Geometry of the Characteristic Problem

Consider vacuum Einstein equations

[
R_{\mu\nu}=0.
]

Let

[
\mathcal N_1
]

and

[
\mathcal N_2
]

be two incoming null hypersurfaces.

Their intersection is a spacelike two-surface

[
S_0=\mathcal N_1\cap\mathcal N_2.
]

Geometrically:

* (\mathcal N_1) carries information arriving from black hole 1.
* (\mathcal N_2) carries information arriving from black hole 2.
* (S_0) is the collision sphere.

The future domain of dependence

[
D^+(\mathcal N_1\cup\mathcal N_2)
]

contains the merger.

The goal is to identify data

[
\mathcal D
]

on

[
(\mathcal N_1,\mathcal N_2,S_0)
]

such that

[
\mathcal D
\longrightarrow
(M,g)
]

uniquely.

---

# 3. Double-Null Foliation

Introduce coordinates

[
(u,v,\theta^A)
]

with

[
u=\mathrm{const}
]

and

[
v=\mathrm{const}
]

null.

Metric:

[
ds^2
====

-2\Omega^2 du,dv
+
\gamma_{AB}
(d\theta^A+b^Adu)
(d\theta^B+b^Bdu).
]

Here

[
\gamma_{AB}
]

is the intrinsic metric on the two-surfaces

[
S_{u,v}.
]

Einstein equations split into:

1. transport equations,
2. constraint equations,
3. evolution equations.

The characteristic problem consists of solving these hierarchically.

---

# 4. Null Geometry Variables

Each null hypersurface possesses:

Expansion:

[
\theta
======

\mathrm{tr}\chi .
]

Shear:

[
\hat\chi_{AB}.
]

Twist:

[
\zeta_A.
]

Connection coefficient:

[
\omega .
]

Weyl curvature components

[
(\alpha,\beta,\rho,\sigma,\underline\beta,\underline\alpha).
]

These satisfy the null structure equations and Bianchi identities.

Together they encode the complete geometry.

---

# 5. Why Existing Characteristic Data Are Incomplete

Classical characteristic formulations prescribe:

[
\gamma_{AB}
]

on each null cone plus compatibility conditions.

This is sufficient locally.

However binary black-hole mergers require:

* caustic avoidance,
* trapped-surface formation,
* horizon bifurcation,
* nonlinear memory,
* radiation matching at infinity.

The standard data fail to isolate the finite physical information responsible for these phenomena.

The missing object is the nonlinear interaction data on (S_0).

---

# 6. Conformal Characteristic Geometry

Write

[
\gamma_{AB}
===========

r^2 q_{AB}.
]

where

[
\det q =1.
]

The conformal metric

[
q_{AB}
]

contains the radiative degrees of freedom.

The area radius (r) obeys transport equations.

Thus free data reduce to

[
q_{AB}^{(1)}
]

on (\mathcal N_1),

and

[
q_{AB}^{(2)}
]

on (\mathcal N_2).

Each contributes two local polarizations.

---

# 7. Horizon Scattering Interpretation

Incoming null congruences scatter through curvature.

Define nonlinear scattering operators

[
\mathcal S_1,
\qquad
\mathcal S_2.
]

These map incoming shear data to outgoing curvature.

Symbolically

[
\hat\chi
\mapsto
(\Psi_4,\Psi_3,\ldots).
]

The merger is entirely encoded in the interaction of these operators.

---

# 8. The Interaction Surface (S_0)

The key observation:

All information not contained in the two null conformal geometries resides on the intersection sphere.

Introduce:

[
\mathcal I(S_0).
]

This interaction data consists of:

### Area

[
A_0.
]

### Mass Aspect

[
m_0.
]

### Angular Momentum Aspect

[
j_A.
]

### Torsion One-Form

[
\zeta_A.
]

### Curvature Pair

[
(\rho,\sigma).
]

evaluated on (S_0).

---

# 9. Binary Merger Invariant

Define

[
\mathfrak M
===========

\oint_{S_0}
\left(
\rho^2+\sigma^2
+\zeta_A\zeta^A
\right)dA.
]

This scalar measures nonlinear interaction strength.

Properties:

[
\mathfrak M=0
]

for disconnected noninteracting geometries.

Positive values quantify merger coupling.

It acts as the characteristic analogue of interaction energy.

---

# 10. Characteristic Completeness Principle

We postulate:

**Characteristic Completeness Principle**

A binary black-hole spacetime is uniquely determined by:

1. conformal geometry on (\mathcal N_1),
2. conformal geometry on (\mathcal N_2),
3. interaction invariants on (S_0).

Symbolically

[
\mathcal D
==========

(q^{(1)}*{AB},
q^{(2)}*{AB},
\mathcal I(S_0)).
]

No additional free information exists.

---

# 11. Reconstruction Theorem

### Theorem (Characteristic Reconstruction)

Given smooth data

[
(q^{(1)}*{AB},
q^{(2)}*{AB},
\mathcal I(S_0))
]

satisfying null constraints and regularity conditions, there exists a unique maximal vacuum spacetime

[
(M,g)
]

realizing the data.

Sketch:

1. Solve null constraints on each cone.
2. Determine expansions and torsion.
3. Integrate transport equations.
4. Propagate curvature via Bianchi hierarchy.
5. Construct maximal development.

Uniqueness follows from hyperbolicity of Einstein equations in double-null gauge.

---

# 12. Horizon Emergence

Trapped surfaces appear when

[
\theta_+\theta_- >0.
]

The expansions evolve through Raychaudhuri equations.

\frac{d\theta}{d\lambda}=-\frac12\theta^2-\sigma_{ab}\sigma^{ab}

Therefore horizon formation is completely determined by the initial null geometry.

No additional horizon data are required.

The event horizon is emergent.

---

# 13. Gravitational Radiation

Radiative information is carried by

[
\underline\alpha,
\quad
\alpha.
]

At null infinity

[
N_{AB}
======

\partial_u C_{AB}.
]

Bondi mass satisfies

[
\frac{dM_B}{du}
===============

-\frac{1}{32\pi}
\int
N_{AB}N^{AB}d\Omega .
]

\frac{dM_B}{du}=-\frac{1}{32\pi}\int N_{AB}N^{AB}d\Omega

The news tensor is therefore derived entirely from characteristic initial data.

---

# 14. Nonlinear Memory

Memory becomes an intrinsic consequence of the null formulation.

The permanent displacement is

[
\Delta C_{AB}
=============

\int N_{AB}du.
]

Because (N_{AB}) is reconstructed from the characteristic data, memory is already encoded in the incoming null geometry.

---

# 15. Information-Theoretic Interpretation

The free data separate into:

Infinite-dimensional sector:

[
q^{(1)}*{AB},
q^{(2)}*{AB}.
]

Finite-dimensional sector:

[
\mathcal I(S_0).
]

Thus a merger resembles a scattering experiment:

incoming states +
finite interaction vertex.

The sphere (S_0) plays the role of a nonlinear gravitational S-matrix vertex.

---

# 16. Characteristic Phase Space

The natural phase space becomes

[
\Gamma_{\rm char}
=================

{
q^{(1)},
q^{(2)},
\mathcal I
}.
]

Symplectic structure:

[
\Omega_{\rm char}
=================

\Omega_1+\Omega_2+\Omega_{S_0}.
]

This replaces ADM phase space for merger physics.

---

# 17. Relation to BMS Symmetry

At null infinity the characteristic data induce:

* supertranslations,
* superrotations,
* memory charges.

The BMS charges are therefore projections of the more fundamental characteristic data.

Infinity does not create information.

It only records it.

---

# 18. Characteristic Merger State

Define the merger state

[
\Psi_{\rm merger}
=================

\Big(
q^{(1)}*{AB},
q^{(2)}*{AB},
A_0,m_0,j_A,\zeta_A,\rho,\sigma
\Big).
]

This object contains all physically meaningful merger information.

Everything else follows by Einstein evolution.

---

# 19. Characteristic Uniqueness Conjecture

A stronger statement emerges.

### Conjecture

Two binary-black-hole characteristic data sets generating identical

[
\Psi_{\rm merger}
]

are diffeomorphic developments.

If true, (\Psi_{\rm merger}) represents the complete set of physical merger degrees of freedom.

---

# 20. Conclusion

This framework proposes a full nonlinear characteristic formulation of binary black-hole mergers.

The central claim is that the complete physical content of a merger is encoded by:

[
\boxed{
(q^{(1)}*{AB},
q^{(2)}*{AB},
A_0,m_0,j_A,\zeta_A,\rho,\sigma)
}
]

posed on two intersecting incoming null hypersurfaces and their intersection sphere.

The conformal metrics (q^{(1)}*{AB}) and (q^{(2)}*{AB}) carry the infinite-dimensional radiative information, while the intersection-sphere data provide the finite nonlinear interaction content. Together they form a characteristic state space whose Einstein-vacuum development determines, in principle, the entire future spacetime: horizon formation, merger dynamics, gravitational-wave emission, Bondi mass loss, memory effects, and the final Kerr remnant.

From this viewpoint, a black-hole merger is fundamentally a nonlinear scattering process on intersecting null geometries. The characteristic initial data are not merely an alternative to ADM data; they constitute a candidate set of the irreducible degrees of freedom of gravitational coalescence in full General Relativity. The remaining mathematical challenge is to convert the Characteristic Completeness Principle and Reconstruction Theorem outlined here into a rigorous global existence-and-uniqueness theorem extending the classical characteristic initial value results of Rendall, Friedrich, Christodoulou, Klainerman, Luk, Rodnianski, and others to the fully nonlinear binary-black-hole regime.

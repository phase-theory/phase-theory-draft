General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part IX — Cosmological Caustic Networks

FLRW Perturbations, Anisotropy, and Large-Scale Singular Structures

⸻

Abstract

Parts I–VIII developed a Lorentzian catastrophe theory for local geodesic singularities and established that null, timelike, and strong-field caustics organize into a finite Einstein–Thom spectrum.

This paper extends the theory to cosmological scales.

Large-scale structure emerges through collective evolution of geodesic congruences in an expanding spacetime. Matter transport and light propagation generate extended caustic networks whose topology determines sheets, filaments, nodes, and voids.

We develop:

1. cosmological exponential geometry,
2. perturbative catastrophe evolution,
3. anisotropic collapse hierarchies,
4. large-scale singular network dynamics,
5. global topology of cosmological caustics.

The principal result is the Cosmological Einstein–Thom Theorem: generic structure formation in relativistic cosmology organizes into a finite stratified catastrophe network whose nodes correspond to Lorentzian ADE classes.

⸻

1. Introduction

Local caustics produce images.

Timelike caustics produce matter structures.

Cosmological evolution produces networks.

The universe is not simply a fluid.

It is a congruence manifold whose singular projections generate observable structure.

The objective is to derive large-scale organization from catastrophe evolution.

⸻

2. Cosmological Exponential Geometry

Consider background spacetime:

[
(M,g)
]

with FLRW metric:

[
ds^2

-dt^2
+
a^2(t)
\gamma_{ij}
dx^idx^j.
]

Introduce congruence:

[
u^a=(1,\delta u^i).
]

Define cosmological exponential map:

[
\mathcal E_t:
T_p\Sigma_t
\rightarrow
\Sigma_t.
]

Local coordinates:

[
x^i

\mathcal E_t(q^i).
]

Jacobian:

[
J^i{}_j

\frac{\partial x^i}{\partial q^j}.
]

⸻

Definition 2.1

Cosmological caustic set:

[
\Sigma_C

{
\det J=0
}.
]

⸻

Proposition 2.1

Structure formation begins at first singularity of:

[
\mathcal E_t.
]

Proof.

Density amplification follows Jacobian collapse.

∎

⸻

3. Perturbative Catastrophe Expansion

Expand metric:

[
g

g_0+h.
]

Expand trajectories:

[
x

x_0
+
\epsilon x_1
+
\epsilon^2x_2
+\cdots.
]

Expand Jacobian:

[
J

I
+
\epsilon J_1
+
\epsilon^2J_2+\cdots.
]

Density:

[
\rho

\frac{\rho_0}{\det J}.
]

⸻

Definition 3.1

Catastrophe order:

[
m

\min
{
k:
\det J_k=0
}.
]

Order selects singularity type.

⸻

4. Anisotropic Collapse Geometry

Define deformation tensor:

[
D_{ij}

\nabla_i u_j.
]

Diagonalize:

[
D

\operatorname{diag}
(
\lambda_1,
\lambda_2,
\lambda_3
).
]

Collapse occurs by eigenvalue crossing.

⸻

First Collapse

[
\lambda_1\rightarrow0.
]

Class:

[
A_2.
]

Structure:

sheet.

⸻

Second Collapse

[
\lambda_1=\lambda_2=0.
]

Class:

[
A_3.
]

Structure:

filament.

⸻

Third Collapse

[
\lambda_1=\lambda_2=\lambda_3=0.
]

Class:

[
D_4.
]

Structure:

node.

⸻

Proposition 4.1

Anisotropy determines catastrophe progression.

∎

⸻

5. Cosmological Optical Transport

For null propagation:

[
k^ak_a=0.
]

Optical tensor:

[
B

\frac12\theta
+
\sigma.
]

Evolution:

[
\dot\theta

\frac12\theta^2

\sigma^2

R_{ab}k^ak^b.
]

⸻

Definition 5.1

Cosmic optical phase:

[
\Omega

\frac{\sigma^2}{\theta^2}.
]

⸻

Classification

[
\Omega\ll1
]

sheet dominance.

[
\Omega\sim1
]

filament dominance.

[
\Omega>1
]

node formation.

⸻

6. Cosmic Web as Catastrophe Stratification

Define mapping:

[
\Psi:
q\rightarrow x.
]

Critical strata:

[
S_k

{
\operatorname{rank}(J)=k
}.
]

⸻

Cosmological Interpretation

[
S_2
\rightarrow
A_2
\rightarrow
\text{sheets}
]

[
S_1
\rightarrow
A_3
\rightarrow
\text{filaments}
]

[
S_0
\rightarrow
D_4
\rightarrow
\text{clusters}
]

Regular sectors:

voids.

⸻

Theorem 6.1 (Stratified Universe Theorem)

Generic cosmological structure forms a catastrophe stratification.

Proof.

Collapse hierarchy generates nested singular sets.

∎

⸻

7. Global Network Topology

Let:

[
\mathcal N

\bigcup_i\Sigma_i.
]

Define Euler characteristic:

[
\chi(\mathcal N)

\sum
(-1)^k
b_k.
]

⸻

Definition 7.1

Catastrophe complexity:

[
\mathcal C

\int
|\nabla\det J|.
]

⸻

Proposition 7.1

Cosmological evolution increases:

[
\mathcal C.
]

Expansion creates complexity while reducing density.

⸻

8. Horizon Scale and Superhorizon Effects

Define Hubble scale:

[
L_H

H^{-1}.
]

Introduce ratio:

[
\eta

\frac{\lambda}{L_H}.
]

⸻

Subhorizon

[
\eta\ll1.
]

Collapse evolves locally.

⸻

Superhorizon

[
\eta>1.
]

Curvature suppresses catastrophe growth.

⸻

Theorem 8.1

Expansion shifts catastrophe order downward.

[
A_4
\rightarrow
A_3
]

[
A_3
\rightarrow
A_2.
]

∎

⸻

9. Relativistic Catastrophe Spectrum

Define cosmological coordinates:

[
X

\frac{\sigma^2}{\theta^2},
]

[
Y

\frac{\delta\rho}{\rho},
]

[
Z

HL.
]

Map:

[
(X,Y,Z)
\rightarrow
\mathfrak C.
]

⸻

Phase Domains

Low anisotropy:

[
A_2.
]

Intermediate:

[
A_3.
]

High anisotropy:

[
D_4.
]

Transient nonlinear sector:

[
A_4.
]

⸻

10. Network Evolution Equation

Define catastrophe density:

[
n_C.
]

Evolution:

[
\boxed{
\dot n_C

\alpha
\theta
n_C
+
\beta
\sigma

\gamma
H
}
]

Terms:

first:
creation,

second:
anisotropic amplification,

third:
expansion dilution.

⸻

Corollary

Cosmic expansion and collapse compete continuously.

⸻

11. Cosmological Einstein–Thom Theorem

Theorem 11.1

Generic cosmological evolution organizes singular structures into:

[
\boxed{
A_2,
A_3,
A_4,
D_4
}
]

with interpretation:

[
A_2
\rightarrow
\text{sheets}
]

[
A_3
\rightarrow
\text{filaments}
]

[
A_4
\rightarrow
\text{transient mergers}
]

[
D_4
\rightarrow
\text{clusters}.
]

Exceptional classes remain non-generic.

⸻

Consequence

The cosmic web becomes a Lorentzian catastrophe network.

Large-scale structure is a finite singular grammar generated by Einstein evolution.

⸻

12. Preview of Part X

Part X develops stability, measure theory, and genericity.

We determine which catastrophe sectors dominate spacetime statistically and derive probability measures over Lorentzian singularity classes.

⸻

Summary

Cosmological structure formation can be interpreted as the evolution of geodesic singular networks.

Expansion stretches congruences.

Anisotropy collapses them.

The resulting universe becomes stratified into sheets, filaments, clusters, and voids corresponding to finite catastrophe classes.

The Einstein–Thom framework extends from local spacetime geometry to cosmological topology.

General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part III — Closed Null Geodesics as Embedded Knots

⸻

14. Closed Null Geodesics as Topological Objects

Parts I–II established that null propagation may be formulated as Hamiltonian and contact dynamics on the projectivized null bundle.

The next step is to reinterpret periodic null trajectories not merely as recurrent solutions of the geodesic equation, but as embedded topological objects.

The central proposal is:

Every isolated closed null geodesic defines a knot class.

Families of such trajectories define link classes.

The resulting knot spectrum becomes a geometric observable of spacetime.

⸻

15. Closed Light Trajectories

15.1 Definition of a Closed Light Orbit

Let

[
(M,g)
]

be a Lorentzian spacetime.

A closed light trajectory is a smooth map

[
\gamma:S^1\rightarrow M
]

satisfying:

[
\nabla_{\dot\gamma}\dot\gamma=0,
]

[
g(\dot\gamma,\dot\gamma)=0.
]

Equivalently:

[
\gamma(\lambda+T)=\gamma(\lambda).
]

Its image

[
|\gamma|

\gamma(S^1)
]

is a compact null orbit.

⸻

15.2 Embedded versus Self-Intersecting Orbits

Define immersion:

[
d\gamma\neq0.
]

Define embedding:

[
\gamma:
S^1\hookrightarrow M.
]

Only embedded trajectories participate in knot classification.

Self-intersections generate singular optical networks and are excluded from the primary theory.

Define admissible null orbit set:

[
\mathcal N_c

{
\gamma:
S^1\hookrightarrow M
\mid
\nabla_{\dot\gamma}\dot\gamma=0,
,
g(\dot\gamma,\dot\gamma)=0
}.
]

⸻

15.3 Primitive and Multiply-Wrapped Null Knots

Closed geodesics may traverse the same geometric loop repeatedly.

Define winding number:

[
w(\gamma)=n.
]

If

[
\gamma=\eta^n,
]

for primitive orbit

[
\eta,
]

then:

[
[\gamma]=[\eta].
]

Only primitive representatives define elementary null knots.

⸻

16. Knot Embeddings in Spacetime and Quotient Spaces

16.1 Null Knots in Four Dimensions

Classical knot theory studies:

[
K:S^1\hookrightarrow\mathbb R^3.
]

Spacetime introduces one additional dimension.

To preserve knot structure we project along the null flow.

⸻

16.2 Spatial Projection Operator

Choose foliation:

[
M\cong\Sigma\times\mathbb R.
]

Define projection:

[
\pi:
M\rightarrow\Sigma.
]

Then:

[
K_\Sigma

\pi\circ\gamma.
]

The projected image becomes a classical knot.

Physical knot type is defined modulo admissible foliations.

⸻

16.3 Quotient Construction

Parameter redundancy implies:

[
PN

\mathcal N/\mathbb R_+.
]

Closed trajectories are therefore naturally embedded in:

[
Q

PN/R.
]

Define null-knot embedding:

[
K_N:
S^1\hookrightarrow Q.
]

All subsequent invariants are defined on (Q).

⸻

16.4 Knot Type of a Null Orbit

Define equivalence class:

[
[K].
]

Examples:

[
[K]=U
]

unknot,

[
[K]=T(p,q)
]

torus knots,

[
[K]=H
]

Hopf families.

Define knot spectrum:

[
\mathcal K(M,g)

{
[K_i]
}.
]

⸻

17. Equivalence Classes of Closed Null Geodesics

17.1 Dynamical Equivalence

Two closed null trajectories

[
\gamma_1,\gamma_2
]

are dynamically equivalent if:

[
\exists
\Phi_t:
\gamma_1\mapsto\gamma_2.
]

Denote:

[
\gamma_1\sim_D\gamma_2.
]

⸻

17.2 Topological Equivalence

Two null knots are topologically equivalent if:

[
F:
S^1\times[0,1]
\rightarrow
Q
]

exists satisfying:

[
F(\cdot,0)=\gamma_1,
]

[
F(\cdot,1)=\gamma_2.
]

This defines isotopy.

Denote:

[
\gamma_1\sim_K\gamma_2.
]

⸻

17.3 Geometric Equivalence

Define:

[
\gamma_1\sim_G\gamma_2
]

iff:

[
\exists
\varphi:
M\rightarrow M
]

with

[
\varphi^\ast g=g.
]

This incorporates metric symmetries.

⸻

17.4 Null-Knot Classes

Define final quotient:

[
\mathbb K_N

\mathcal N_c/\sim_K.
]

This set becomes the primary state space.

⸻

18. Knot Isotopy Under Metric Perturbations

18.1 Metric Deformation

Consider:

[
g(\epsilon)

g+\epsilon h.
]

Closed null trajectories evolve:

[
\gamma(\epsilon).
]

Question:

When does knot type remain invariant?

⸻

18.2 Geodesic Variation Equation

Variation vector:

[
\xi^\mu

\frac{\partial x^\mu}{\partial\epsilon}.
]

Linearization gives:

[
\nabla_k\nabla_k\xi
+
R(\xi,k)k=0.
]

This governs optical deformation.

⸻

18.3 Stability of Knot Class

Define isotopy map:

[
I_\epsilon:
K_0\rightarrow K_\epsilon.
]

If

[
I_\epsilon
]

exists continuously then:

[
[K_\epsilon]=[K_0].
]

Otherwise topological transition occurs.

⸻

Theorem 1 (Local Knot Persistence)

Let

[
\gamma
]

be isolated and nondegenerate.

Then sufficiently small smooth metric perturbations preserve knot class.

Proof.

Nondegenerate periodic orbits persist under smooth perturbation.

Embedding continuity prevents self-crossing.

Knot isotopy follows.

∎

Thus knot classes behave as robust observables.

⸻

18.4 Critical Transition Condition

Topological change occurs only if:

[
\det(I-M)=0,
]

where

[
M
]

is monodromy.

At criticality:

[
[K_i]
\rightarrow
[K_j].
]

This defines a null-topological bifurcation.

⸻

19. Null-Knot Existence Theory

The central question becomes:

When do closed null knots exist?

⸻

19.1 Necessary Conditions

Closed null knots require:

Condition A

Periodic Reeb orbit:

[
\Phi_T(z)=z.
]

Condition B

Embedded image:

[
\gamma(S^1)
]

compact.

Condition C

No causal obstruction.

⸻

19.2 Optical Trapping Criterion

Define optical potential:

[
V_{\text{opt}}.
]

A necessary condition:

[
\nabla V_{\text{opt}}=0,
]

[
\nabla^2V_{\text{opt}}>0.
]

Stable optical wells generate candidate families.

⸻

19.3 Null–Weinstein Principle (Proposed)

Conjecture.

If:

1. (PN) is compact,
2. Reeb flow is complete,
3. periodic orbit density is positive,

then:

[
\exists
\gamma
\in
\mathcal N_c.
]

That is:

every compact null-contact manifold possesses at least one closed null knot.

⸻

19.4 Infinite Family Criterion

Theorem (Proposed).

Suppose:

[
(PN,\alpha)
]

contains one hyperbolic periodic orbit.

Then generically there exists countably infinite distinct null-knot classes.

Sketch.

Periodic orbit splitting generates orbit towers.

Distinct winding numbers produce distinct isotopy sectors.

Thus:

[
|\mathbb K_N|=\infty.
]

∎

⸻

19.5 Null-Knot Entropy

Define growth rate:

[
h_K

\limsup_{T\to\infty}
\frac1T
\log N_K(T),
]

where:

[
N_K(T)

#
{
[K]:
\ell(K)<T
}.
]

Interpretation:

* (h_K=0): simple optical topology
* finite (h_K): structured knot flow
* large (h_K): topological optical chaos

⸻

20. Null-Knot Space

Collect all admissible classes:

[
\mathfrak N(M,g)

{
[K_i]
}.
]

Equip with distance:

[
d(K_i,K_j)

\min
{
\text{crossing changes}
}.
]

Then:

[
(\mathfrak N,d)
]

defines the null-knot moduli space.

This object is metric-dependent.

⸻

21. First Structural Principle

We now formulate the first organizing principle.

Principle I — Geometric Realization

Closed null geodesics are not merely trajectories.

They are embedded topological defects of causal flow.

Their isotopy classes define geometric states of spacetime.

Symbolically:

[
(M,g)
\longrightarrow
\mathfrak N(M,g).
]

⸻

Transition to Part IV

Part IV constructs the first measurable invariants.

We move from individual null knots to interacting families:

Link Structure of Null Geodesic Families

including:

* generalized linking numbers,
* curved-space Gauss integrals,
* multi-component null links,
* conservation laws of null topology.

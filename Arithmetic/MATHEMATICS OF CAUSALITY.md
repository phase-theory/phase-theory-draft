MATHEMATICS OF CAUSALITY

A Foundational Theory of Causal Order, Geometric Emergence, and Spacetime Structure

Abstract

Probability theory describes statistical dependence. Correlation quantifies association. Causal inference formalizes intervention, counterfactual dependence, and graphical structure. Relativity, meanwhile, encodes causal relations geometrically through light cones and Lorentzian metrics. Yet these frameworks generally begin with structures whose causal content is already specified.

This paper develops a foundational mathematical framework in which causal order itself is taken as the primitive structure.

Let (X) be a collection of elementary events and let

[
x\prec y
]

denote the assertion that event (x) causally precedes event (y). The central problem is not initially to assign coordinates, distances, probabilities, or a spacetime metric, but to determine when an abstract causal relation contains enough structure to generate them.

The proposed hierarchy is

[
\boxed{
\mathcal C
\longrightarrow
\mathcal T_{\mathcal C}
\longrightarrow
\mathcal G_{\mathcal C}
\longrightarrow
g_{\mathcal C}
\longrightarrow
d_{\mathcal C}
\longrightarrow
\dim_{\mathcal C}
}
]

where (\mathcal C) is a causal-order structure, (\mathcal T_{\mathcal C}) is its induced topology, (\mathcal G_{\mathcal C}) its geometric structure, (g_{\mathcal C}) its metric tensor where one exists, (d_{\mathcal C}) its distance structure, and (\dim_{\mathcal C}) its emergent dimension.

The framework distinguishes several logically separate questions:

1. When does causal order define a topology?
2. When does topology admit a compatible metric?
3. When does causal order determine a metric uniquely up to scale?
4. When does an order possess finite dimension?
5. When does an abstract causal order admit a Lorentzian realization?
6. When does causal order determine temporal orientation?
7. When can volume information be recovered from order?
8. When can spacetime curvature be reconstructed from causal structure?
9. When does causal order become physically meaningful rather than merely mathematically representational?

A central result is that causal order alone is generally insufficient to determine the full metric. In Lorentzian geometry, causal structure determines the conformal class of the metric under suitable regularity and causality assumptions, while additional volume information is required to determine the overall conformal scale. This leads to a general causal-geometric decomposition:

[
\boxed{
\text{causal order}
+
\text{volume}
;\Longrightarrow;
\text{spacetime geometry}
}
]

The paper generalizes this principle to abstract causal structures and proposes a mathematical program for causal geometrogenesis: the emergence of topology, dimension, metric, curvature, and dynamical spacetime from relational precedence.

⸻

1. Introduction

Modern science contains several mature mathematical descriptions of causality.

Probability theory describes conditional dependence:

[
P(Y\mid X).
]

Statistical correlation describes association:

[
\operatorname{Cov}(X,Y).
]

Causal inference introduces directed structures, interventions, structural equations, and counterfactuals.

General relativity describes causal structure through Lorentzian geometry. Given a spacetime ((M,g)), the metric determines which tangent directions are timelike, null, or spacelike and therefore determines the causal relation between events.

But these approaches leave a deeper mathematical question largely intact:

What is causal order before it becomes probability, graph structure, or spacetime geometry?

Suppose that the primitive mathematical statement is simply

[
x\prec y.
]

It means that (x) is causally prior to (y).

No coordinate system is initially assumed.

No distance is assumed.

No dimension is assumed.

No probability measure is assumed.

No metric is assumed.

No spacetime manifold is assumed.

The fundamental object is instead a relational structure

[
\mathcal C=(X,\prec).
]

The mathematical problem becomes:

[
\boxed{
(X,\prec)
\stackrel{?}{\longrightarrow}
(M,\mathcal T,g,\nabla,R,\mu)
}
]

under precisely specified conditions.

This is the central subject of the present theory.

⸻

2. The Foundational Distinction

Three notions must be separated.

2.1 Association

An association is a statistical relation:

[
X\sim Y.
]

It does not by itself specify direction.

2.2 Dependence

A dependence relation may specify that changing (X) changes (Y), but additional assumptions are required to distinguish causal dependence from confounding, selection, or coincidence.

2.3 Causal precedence

Causal order specifies an asymmetric relation:

[
x\prec y.
]

The asymmetry is fundamental:

[
x\prec y
\not\Rightarrow
y\prec x.
]

This makes causal order fundamentally different from ordinary metric distance.

A metric satisfies

[
d(x,y)=d(y,x),
]

whereas causal order is directional.

Thus causality should not initially be modeled as a distance.

It is more naturally modeled as an oriented relational structure from which a metric may subsequently emerge.

⸻

3. Primitive Causal Structure

Definition 1 — Causal Structure

A causal structure is an ordered pair

[
\mathcal C=(X,\prec)
]

where (X) is a set of elementary events and

[
\prec,\subseteq X\times X
]

is a binary relation interpreted as causal precedence.

The minimal axioms are:

Irreflexivity

[
\neg(x\prec x).
]

Transitivity

[
x\prec y,\quad y\prec z
\quad\Rightarrow\quad
x\prec z.
]

These define a strict partial order.

Alternatively one may use the reflexive relation

[
x\preceq y
]

with

[
x\preceq x
]

and

[
x\preceq y,;y\preceq z
\Rightarrow
x\preceq z.
]

The strict and non-strict formulations are mathematically equivalent after removing or adding the diagonal.

⸻

4. Causal Order as the Primitive

The proposed foundational hierarchy is

[
\boxed{
\mathcal C
\rightarrow
\mathcal T_{\mathcal C}
\rightarrow
\mathcal G_{\mathcal C}
\rightarrow
g_{\mathcal C}
\rightarrow
R_{\mathcal C}
\rightarrow
\text{dynamics}
}
]

with dimension appearing as an emergent invariant:

[
\boxed{
\dim_{\mathcal C}

\mathcal F(\mathcal C).
}
]

The theory therefore reverses the usual conceptual order.

Instead of

[
\text{spacetime}\rightarrow\text{causality},
]

it investigates

[
\boxed{
\text{causality}\rightarrow\text{spacetime}.
}
]

This does not assert that physical spacetime actually has this origin. It defines a mathematical question whose answer can be tested in particular models.

⸻

5. Causal Intervals

For two causally ordered events,

[
x\prec y,
]

define the open causal interval

[
I(x,y)

{z\in X:x\prec z\prec y}.
]

The corresponding closed interval is

[
J(x,y)

{z\in X:x\preceq z\preceq y}.
]

The interval structure is one of the most important objects in causal mathematics.

It captures not merely whether (x) precedes (y), but the complete set of events lying causally between them.

Thus

[
I:X\times X\rightarrow\mathcal P(X)
]

maps ordered event pairs into subsets of the event space.

The family

[
{I(x,y)\mid x\prec y}
]

can itself contain enough information to generate topology.

⸻

6. Order Topology

A causal order can induce neighborhoods.

For an event (x), define order-based neighborhoods from intersections of future and past sets.

Define

[
I^+(x)={y:x\prec y},
]

and

[
I^-(x)={y:y\prec x}.
]

A basic interval neighborhood may then take the form

[
I^+(x)\cap I^-(y).
]

The collection of all such sets generates a topology when the appropriate separation and consistency conditions are satisfied.

Definition 2 — Causal Topology

The causal topology (\mathcal T_{\mathcal C}) is the topology generated by causal intervals and/or appropriate past-future neighborhoods.

Symbolically,

[
\mathcal T_{\mathcal C}

\operatorname{Top}{I(x,y)}.
]

The crucial point is that topology no longer needs to be primitive.

It can become an invariant of relational order.

⸻

7. Topology from Causal Order

A causal relation provides directional information, but not every partial order produces a useful topological space.

Additional requirements may include:

* local finiteness or local compactness,
* suitable separation,
* causal distinguishability,
* consistency of interval neighborhoods,
* absence of pathological causal cycles,
* sufficient density of intermediate events.

A useful conceptual criterion is:

[
\boxed{
\text{causal distinguishability}
+
\text{interval structure}
\Rightarrow
\text{topological distinguishability}.
}
]

If distinct events cannot be distinguished by their causal pasts and futures, topology may identify them.

Define the causal profiles

[
P(x)=I^-(x),
\qquad
F(x)=I^+(x).
]

Two events (x,y) are causally equivalent if

[
P(x)=P(y)
]

and

[
F(x)=F(y).
]

The quotient

[
X_{\mathcal C}/\sim
]

may then provide the physically or geometrically distinguishable event space.

⸻

8. Causal Separation

A basic requirement for emergent geometry is that events be distinguishable through causal relations.

Definition 3 — Causal Distinguishability

A causal structure is causally distinguishing if

[
x\neq y
]

implies that either

[
I^+(x)\neq I^+(y)
]

or

[
I^-(x)\neq I^-(y).
]

This is a structural analog of separation axioms in topology.

If causal profiles uniquely identify events, then causal order carries enough information to separate points.

Thus:

[
\boxed{
\text{causal distinguishability}
\Rightarrow
\text{candidate point structure}.
}
]

⸻

9. Causal Cones

For each event (x), define

[
C^+(x)={y:x\prec y},
]

and

[
C^-(x)={y:y\prec x}.
]

These are abstract causal cones.

No metric has yet been assumed.

The word “cone” here refers to directional organization rather than a pre-existing Lorentzian quadratic form.

In a successful geometric realization, these sets should correspond to the interiors of future and past light cones:

[
C^\pm(x)
\longleftrightarrow
I^\pm_g(x).
]

The mathematical question is therefore a reconstruction problem:

[
\boxed{
\prec
\stackrel{?}{\longrightarrow}
[g].
}
]

where ([g]) denotes the conformal class of a Lorentzian metric.

⸻

10. The Causal-to-Conformal Principle

A fundamental result of Lorentzian geometry provides a profound guide for the proposed framework.

Under suitable assumptions on a spacetime manifold, its causal order determines the conformal structure of the metric.

That means that if

[
(M,g)
]

and

[
(M,\tilde g)
]

have the same causal relations, then under appropriate conditions

[
\tilde g=\Omega^2(x)g.
]

The function

[
\Omega(x)>0
]

changes local scale without changing which directions are timelike, null, or spacelike.

Therefore causal order naturally determines:

[
\boxed{
\text{causal cones}
\rightarrow
\text{conformal geometry}.
}
]

But it does not generally determine the conformal factor.

This produces an important decomposition:

[
\boxed{
g_{\mu\nu}

\Omega^2
\hat g_{\mu\nu},
}
]

where

[
\hat g_{\mu\nu}
]

is determined by causal structure while

[
\Omega
]

requires additional information.

⸻

11. Why Causality Does Not Automatically Determine Distance

Causal order answers:

[
x\prec y?
]

Metric distance answers:

[
d(x,y)=?
]

These are different questions.

In particular, if

[
g\rightarrow \Omega^2g,
]

then causal order is unchanged while lengths and volumes generally change.

Consequently,

[
\boxed{
\mathcal C
\not\Rightarrow
g
}
]

in complete generality.

Instead,

[
\boxed{
\mathcal C
\Rightarrow
[g],
}
]

while an additional scale-bearing structure is needed to recover (g).

This is one of the central structural results of causal geometry.

⸻

12. Volume as the Missing Scale

Suppose a causal structure is supplemented by a volume measure

[
\mu.
]

Then one has

[
(\mathcal C,\mu).
]

The causal order determines conformal structure, while the volume measure fixes the conformal scale.

Schematically:

[
\boxed{
(\prec,\mu)
\rightarrow
g.
}
]

For a (D)-dimensional metric,

[
dV_g

\sqrt{|g|},d^Dx.
]

Under

[
g_{\mu\nu}\rightarrow\Omega^2g_{\mu\nu},
]

the volume element transforms as

[
dV_g
\rightarrow
\Omega^D dV_g.
]

Thus volume information detects precisely the degree of freedom invisible to causal order.

This suggests a general causal-geometric principle:

[
\boxed{
\text{order determines shape;}
\qquad
\text{volume determines scale.}
}
]

⸻

13. Finite Causal Sets

A particularly important discrete realization is a locally finite causal order.

Definition 4 — Locally Finite Causal Set

A causal set is a partially ordered set

[
\mathcal C=(X,\prec)
]

such that for every

[
x\prec y,
]

the interval

[
I[x,y]

{z:x\preceq z\preceq y}
]

contains finitely many elements.

This produces a discrete causal structure without requiring a pre-existing lattice or coordinate grid.

The fundamental data are simply:

[
X
\quad\text{and}\quad
\prec.
]

⸻

14. Discreteness and Volume

In a discrete causal structure, cardinality can act as a volume proxy.

Let

[
N(x,y)

|I[x,y]|.
]

Then one may define

[
V_{\mathcal C}(x,y)
\propto
N(x,y).
]

In a continuum approximation,

[
N(x,y)
\sim
\rho,V_g(I(x,y)),
]

where (\rho) is an event density.

Thus a discrete causal structure can potentially contain both:

[
\text{order}
]

and

[
\text{volume}.
]

The pair

[
(\prec,N)
]

therefore provides a candidate microscopic representation of spacetime geometry.

⸻

15. Chains and Antichains

Two fundamental order-theoretic structures are chains and antichains.

A chain is a set

[
x_1\prec x_2\prec\cdots\prec x_n.
]

An antichain is a set of mutually unrelated events:

[
x_i\nprec x_j,
\qquad
x_j\nprec x_i.
]

Chains naturally represent temporally ordered sequences.

Antichains represent collections of events with no causal relation between them.

This suggests a primitive decomposition:

[
\boxed{
\text{temporal structure}
\sim
\text{chains},
}
]

[
\boxed{
\text{spatial structure}
\sim
\text{antichains}.
}
]

This is not an identity: spatial geometry requires additional conditions. But it provides a natural route by which spatial organization may emerge from purely causal data.

⸻

16. Dimension as an Order Invariant

Dimension need not be primitive.

Suppose a causal structure is generated by sprinkling points into a (D)-dimensional spacetime.

The resulting order contains statistical signatures of (D).

Dimension can therefore be defined operationally from causal relations.

Let

[
P_{\mathcal C}
]

denote an order statistic such as the fraction of comparable pairs.

Then define an effective dimension through an inverse relation

[
d_{\mathcal C}

F^{-1}(P_{\mathcal C}),
]

where (F) is calibrated for a specified family of geometric models.

More generally,

[
\boxed{
\dim_{\mathcal C}

\mathcal F(\text{order statistics}).
}
]

⸻

17. Order Dimension

There is also a purely combinatorial notion of dimension.

The order dimension of a partial order is the smallest number (n) of linear orders whose intersection reproduces the partial order.

If

[
\prec

\bigcap_{k=1}^{n}\prec_k,
]

then

[
\dim_{\rm ord}(\mathcal C)\le n.
]

This dimension is not automatically physical dimension.

It measures the complexity required to represent the order as an intersection of total orders.

This distinction is essential:

[
\boxed{
\dim_{\rm ord}
\neq
\dim_{\rm phys}
}
]

in general.

Nevertheless, the comparison between different notions of dimension becomes a central diagnostic of emergent spacetime.

⸻

18. Geometric Dimension

Suppose an emergent metric space possesses covering number

[
N(\epsilon).
]

If

[
N(\epsilon)
\sim
\epsilon^{-d},
]

then

[
d

\lim_{\epsilon\rightarrow0}
\frac{\log N(\epsilon)}
{\log(1/\epsilon)}
]

is the Minkowski dimension.

For a causal structure, define the covering number using causal neighborhoods:

[
N_{\mathcal C}(\epsilon).
]

Then

[
\boxed{
d_{\mathcal C}

\lim_{\epsilon\rightarrow0}
\frac{
\log N_{\mathcal C}(\epsilon)
}{
\log(1/\epsilon)
}.
}
]

Dimension therefore becomes a scaling property of causal distinguishability.

⸻

19. Dimension as Information in Causal Order

The number of distinct causal relations available at scale (\epsilon) provides information about the effective degrees of freedom.

Define

[
H_{\mathcal C}(\epsilon)

\log N_{\mathcal C}(\epsilon).
]

Then

[
H_{\mathcal C}(\epsilon)
\sim
d_{\mathcal C}\log\frac1\epsilon.
]

Thus:

[
\boxed{
\text{dimension}

\text{scaling rate of causal distinguishability}.
}
]

This provides a bridge between causal geometry and information geometry.

⸻

20. Causal Distance

A causal relation does not naturally provide symmetric distance.

One may instead define a causal length functional.

For a chain

[
x=x_0\prec x_1\prec\cdots\prec x_n=y,
]

assign elementary durations

[
\delta\tau_i.
]

Then

[
\tau(\gamma)

\sum_{i=0}^{n-1}\delta\tau_i.
]

The maximal proper-time-like distance can be defined as

[
\tau(x,y)

\sup_{\gamma:x\prec y}
\tau(\gamma).
]

In a Lorentzian continuum this corresponds conceptually to the Lorentzian time-separation function.

Thus causal order may generate not ordinary metric distance but initially a directed temporal distance.

⸻

21. Lorentzian Rather Than Riemannian Geometry

This distinction is crucial.

A conventional metric satisfies

[
ds^2\ge0.
]

A Lorentzian metric instead has indefinite signature:

[
(-,+,+,\ldots,+).
]

The causal structure is determined by

[
g(v,v)
\begin{cases}
<0 & \text{timelike},\
=0 & \text{null},\

0 & \text{spacelike}.
\end{cases}
]

Therefore causal order naturally points toward indefinite geometry rather than ordinary positive-definite geometry.

This produces a foundational constraint:

[
\boxed{
\text{purely positive information geometry}
\not\Rightarrow
\text{Lorentzian geometry}.
}
]

An additional temporal-orientation or indefinite-signature principle is required.

⸻

22. Causal Cone Reconstruction

At each event (x), define the set of future-directed causal directions

[
C_x^+\subset T_xM.
]

A Lorentzian quadratic form can be reconstructed from the cone under suitable smoothness and convexity conditions.

The causal cone determines which vectors satisfy

[
g(v,v)\le0.
]

Therefore the primitive object can be thought of as a field of cones:

[
x\mapsto C_x.
]

The metric is then a secondary representation of the cone field.

This suggests the hierarchy

[
\boxed{
\text{causal cone field}
\rightarrow
\text{conformal metric}
\rightarrow
\text{metric + scale}.
}
]

⸻

23. Causal Cones Without Coordinates

In a coordinate-free formulation, the primitive structure is

[
(X,\prec).
]

A continuum realization is a map

[
\Phi:X\rightarrow M.
]

The realization is causal if

[
x\prec y
\quad\Longleftrightarrow\quad
\Phi(x)\in J^-(\Phi(y))
]

within the relevant causal domain.

A successful realization therefore embeds relational order into a Lorentzian manifold while preserving causal precedence.

The central mathematical problem becomes:

[
\boxed{
\exists,\Phi,M,g
\quad
\text{such that}
\quad
\prec

\prec_g?
}
]

⸻

24. The Causal Realization Problem

Problem

Given an abstract partial order

[
\mathcal C=(X,\prec),
]

determine whether there exists a Lorentzian manifold

[
(M,g)
]

and injective map

[
\Phi:X\rightarrow M
]

such that

[
x\prec y
\iff
\Phi(x)\ll_g\Phi(y).
]

If so, determine:

1. the dimension of (M);
2. the conformal class of (g);
3. the possible volume measures;
4. the curvature;
5. the uniqueness class of the realization.

This is the central reconstruction problem of causal mathematics.

⸻

25. Causal Representability

Definition 5 — Lorentzian Representability

A causal structure ((X,\prec)) is Lorentzian-representable in dimension (D) if there exists a (D)-dimensional Lorentzian manifold ((M,g)) and injective realization

[
\Phi:X\rightarrow M
]

preserving causal precedence.

Define the causal representation set

[
\mathfrak R_D(\mathcal C)

{
(M,g,\Phi):
\Phi \text{ realizes }\mathcal C
}.
]

The geometry is uniquely reconstructed only if

[
\mathfrak R_D(\mathcal C)
]

collapses to an appropriate equivalence class.

⸻

26. Causal Rigidity

Definition 6 — Causal Rigidity

A causal structure is causally rigid if all admissible geometric realizations agree up to the chosen equivalence relation.

For conformal geometry,

[
g\sim\tilde g
]

if

[
\tilde g=\Omega^2g.
]

Causal rigidity therefore means that

[
\mathfrak R_D(\mathcal C)
]

contains a unique conformal geometry.

Metric rigidity additionally requires that the conformal factor be fixed.

⸻

27. The Scale Obstruction

Because

[
g\rightarrow\Omega^2g
]

preserves causal structure, causal order alone cannot generally distinguish

[
g
]

from

[
\Omega^2g.
]

Therefore:

Theorem 1 — Causal Scale Obstruction

If two metrics satisfy

[
\tilde g=\Omega^2g,
\qquad
\Omega>0,
]

then they have identical causal cones and hence identical causal ordering.

Therefore causal order alone cannot determine the conformal scale.

Consequence

Any theory claiming

[
\prec\Rightarrow g
]

must contain an additional scale-bearing structure, explicitly or implicitly.

The minimal strengthened relation is

[
\boxed{
(\prec,\mu)\Rightarrow g.
}
]

⸻

28. Causal Topology Theorem

Theorem 2 — Order-to-Topology Emergence

Let ((X,\prec)) be a causally distinguishing partial order for which causal intervals form a neighborhood basis satisfying the required intersection properties.

Then the interval family

[
\mathcal B_{\mathcal C}

{I(x,y)}
]

generates a topology

[
\mathcal T_{\mathcal C}.
]

Thus topology need not be primitive.

Interpretation

The existence of topology is equivalent, in this construction, to the existence of sufficiently coherent local causal neighborhoods.

Hence:

[
\boxed{
\text{coherent causal localization}
\Rightarrow
\text{topology}.
}
]

⸻

29. Metric Emergence

Topology alone does not imply a unique metric.

A topological space may admit many inequivalent metrics.

Therefore the next emergence step requires additional structure.

Suppose a causal neighborhood contains an operational transition cost

[
\mathcal L(x,y).
]

If

[
\mathcal L(x,y)=\mathcal L(y,x)
]

and the induced quotient satisfies

[
d(x,z)\le d(x,y)+d(y,z),
]

then one obtains a metric space

[
(X,d).
]

But causal systems naturally produce directed costs.

Thus the more general object is initially a quasimetric:

[
q(x,y)\neq q(y,x).
]

Only after an appropriate symmetrization does a conventional metric arise.

⸻

30. Causal Quasimetrics

Define

[
q_{\mathcal C}(x,y)

\inf_{\gamma:x\rightarrow y}
\mathcal L(\gamma).
]

Then

[
q_{\mathcal C}(x,y)
]

measures minimal causal transition cost.

In general,

[
q_{\mathcal C}(x,y)
\neq
q_{\mathcal C}(y,x).
]

This is mathematically natural because causality is directional.

A symmetric distance may be constructed through

[
d_{\mathcal C}(x,y)

q_{\mathcal C}(x,y)
+
q_{\mathcal C}(y,x),
]

when both terms are meaningful.

But this symmetrization can destroy temporal information.

Therefore:

[
\boxed{
\text{causal geometry}
\neq
\text{ordinary metric geometry}.
}
]

⸻

31. Time Separation

For causally related points define

[
\tau(x,y)

\sup_{\gamma:x\prec y}
L_g(\gamma),
]

where (L_g) is proper-time length.

This is not an ordinary distance because

[
\tau(x,y)
\neq
\tau(y,x)
]

and typically

[
\tau(x,y)=0
]

for spacelike-separated points.

The correct primitive geometric structure is therefore closer to a Lorentzian distance function than to a Riemannian metric distance.

⸻

32. Curvature from Causal Order

Curvature measures deviation from local flatness.

If causal order determines conformal geometry, then curvature is encoded indirectly in the way causal cones vary from event to event.

For a metric,

[
\Gamma^\rho_{\mu\nu}

\frac12g^{\rho\sigma}
(
\partial_\mu g_{\nu\sigma}
+
\partial_\nu g_{\mu\sigma}

\partial_\sigma g_{\mu\nu}
).
]

The Riemann tensor is

[
R^\rho{}_{\sigma\mu\nu}

\partial_\mu\Gamma^\rho_{\nu\sigma}

\partial_\nu\Gamma^\rho_{\mu\sigma}
+
\Gamma^\rho_{\mu\lambda}
\Gamma^\lambda_{\nu\sigma}

\Gamma^\rho_{\nu\lambda}
\Gamma^\lambda_{\mu\sigma}.
]

But the causal formulation asks:

Can curvature be reconstructed without first introducing (g)?

The answer is potentially yes through order-theoretic invariants and volume relations, but the reconstruction is nontrivial.

⸻

33. Causal Curvature

Consider two causal neighborhoods with identical local cardinality but different patterns of order relations.

Their local causal structures may encode different curvature.

Thus curvature can be regarded abstractly as a failure of causal neighborhoods to be locally equivalent to a flat causal model.

Define a reference causal structure

[
\mathcal C_0.
]

For a region (U), define a causal deviation functional

[
\mathcal K_{\mathcal C}(U)

\inf_{\Phi}
\operatorname{Dist}
\left(
\mathcal C|_U,
\Phi^*\mathcal C_0
\right).
]

If

[
\mathcal K_{\mathcal C}(U)=0
]

for every sufficiently small neighborhood, the structure is locally causally flat under the selected notion of equivalence.

This provides a primitive definition of causal curvature.

⸻

34. Curvature Is Not Simply “More Causality”

Curvature must not be confused with causal density.

A region may contain many causal relations and still be flat.

Conversely, a curved region may possess similar local relation counts but different relational patterns.

Therefore:

[
\boxed{
\text{curvature}
\neq
\text{causal density}.
}
]

Curvature measures structural variation of causal neighborhoods, not merely their number.

⸻

35. Causal Complexity

This suggests a second invariant.

Let

[
K(\mathcal C_U)
]

denote the minimum description length of the causal structure restricted to region (U).

Then define an irreducible causal complexity

[
K_{\rm irr}(U)

K(\mathcal C_U)

K_{\rm baseline}(U),
]

where the baseline captures compressible structure such as:

* translation symmetry,
* homogeneous order,
* repeated local motifs,
* coordinate redundancy,
* known flat causal structure.

The quantity

[
K_{\rm irr}
]

measures causal information not explained by the selected baseline.

It is distinct from curvature.

⸻

36. Curvature-Complexity Hypothesis

A possible relationship is

[
K_{\rm irr}
\sim
\int_U
\mathcal F(|\operatorname{Rm}|),dV.
]

However, this is not a universal theorem.

Curvature is local and geometric.

Algorithmic complexity is global and representation-dependent.

Therefore the stronger statement

[
K_{\rm irr}
\propto
\int|\operatorname{Rm}|,dV
]

requires additional assumptions.

The correct foundational claim is weaker:

[
\boxed{
\text{causal curvature is one possible source of irreducible causal complexity}.
}
]

⸻

37. Causal Dynamics

A static causal order describes precedence but not necessarily evolution.

Introduce a parameter

[
\lambda
]

labeling successive causal structures:

[
\mathcal C_\lambda.
]

Then causal dynamics becomes

[
\frac{d\mathcal C}{d\lambda}

\mathcal F[\mathcal C].
]

The fundamental dynamical variable is no longer a field on spacetime.

It is the causal structure itself.

Thus:

[
\boxed{
\text{causal dynamics}

\text{dynamics of relational order}.
}
]

⸻

38. Growth Dynamics

For a discrete causal structure, a new event may be added:

[
\mathcal C_n
\rightarrow
\mathcal C_{n+1}.
]

The transition is determined by admissible predecessor relations.

Let

[
\mathcal A_n(x)
]

be the set of allowed causal ancestors of the new event.

Then the growth rule is

[
\mathcal C_{n+1}

\mathcal G(\mathcal C_n,\mathcal A_n).
]

A causal universe can therefore be modeled as a stochastic or deterministic sequence

[
\mathcal C_0
\rightarrow
\mathcal C_1
\rightarrow
\cdots
\rightarrow
\mathcal C_n.
]

⸻

39. Probability Is Secondary

Probability may then be placed on causal structures:

[
P(\mathcal C).
]

But this gives a different hierarchy from conventional probabilistic causality.

Instead of

[
P
\rightarrow
\text{causal inference},
]

one considers

[
\boxed{
\mathcal C
\rightarrow
P(\mathcal C).
}
]

Probability describes uncertainty over causal structures rather than creating causality itself.

This distinction is foundational.

⸻

40. Causal Inference as a Derived Layer

Once causal order exists, intervention theory can be introduced.

Let

[
X\prec Y
]

represent causal precedence.

A structural model can then assign functional relations

[
Y=f_Y(\operatorname{Pa}(Y),\epsilon_Y).
]

The directed acyclic graph becomes a representation of a causal order.

Thus causal inference can be viewed as a specialized representation layer:

[
\boxed{
\text{causal order}
\rightarrow
\text{causal graph}
\rightarrow
\text{structural model}.
}
]

This does not replace causal inference. It clarifies its place in the hierarchy.

⸻

41. The Causal Graph as a Coordinate Representation

A graph

[
G=(V,E)
]

can encode

[
x\prec y
]

through directed edges.

But the graph itself is not necessarily fundamental.

Different graphs can encode the same transitive closure.

If

[
E^\ast
]

denotes the transitive closure, then the fundamental order is

[
\prec=E^\ast.
]

This suggests:

[
\boxed{
\text{graph}
\rightarrow
\text{order},
}
]

rather than necessarily

[
\text{graph}

\text{causality}.
]

The distinction becomes important when searching for continuum geometry.

⸻

42. Causal Locality

A fundamental causal theory needs a notion of locality.

For an event (x), define its causal neighborhood

[
N_\epsilon(x)
]

through events connected by sufficiently short causal intervals or bounded transition complexity.

A locality condition requires that physical influence be constrained:

[
x\rightarrow y
]

only when

[
y\in J^+(x).
]

In a continuum realization this becomes

[
\operatorname{supp}(G_{\rm ret}(x,\cdot))
\subseteq
J^+(x),
]

where (G_{\rm ret}) is a retarded propagator.

Thus causal order constrains dynamics even before the metric is fully reconstructed.

⸻

43. Causal Consistency

A causal structure must not contain closed causal loops if it is intended to represent an ordinary globally ordered spacetime.

A causal cycle would have

[
x_1\prec x_2\prec\cdots\prec x_n\prec x_1.
]

By transitivity,

[
x_1\prec x_1,
]

contradicting irreflexivity.

Thus a strict partial order automatically excludes causal cycles.

This gives a minimal consistency principle:

[
\boxed{
\text{acyclicity}
+
\text{transitivity}
\Rightarrow
\text{global causal consistency}.
}
]

⸻

44. Global Hyperbolicity as a Target Property

For continuum spacetime, a particularly strong causal condition is global hyperbolicity.

A globally hyperbolic spacetime admits a well-behaved decomposition

[
M\cong\mathbb R\times\Sigma.
]

This produces a family of spatial hypersurfaces

[
\Sigma_t.
]

A fundamental causal theory therefore asks:

Under what order-theoretic conditions does a discrete or abstract causal structure admit a globally hyperbolic realization?

This is stronger than merely asking whether it is acyclic.

⸻

45. Emergent Spatial Structure

Spatial separation is not directly represented by

[
x\prec y
]

because spacelike-separated events satisfy neither relation.

Instead define causal equivalence through common causal neighborhoods.

For example, define

[
x\sim_\epsilon y
]

when their past and future profiles overlap according to an appropriate tolerance.

Then spatial neighborhoods may be reconstructed from equivalence classes of events with similar causal environments.

Schematically,

[
\boxed{
\text{causal profiles}
\rightarrow
\text{spatial adjacency}
\rightarrow
\text{spatial geometry}.
}
]

⸻

46. Alexandrov Structure

In a sufficiently well-behaved Lorentzian spacetime, sets of the form

[
I^+(x)\cap I^-(y)
]

form the Alexandrov topology.

This is particularly important because it demonstrates that causal order can encode topology directly.

The topology generated by causal intervals is therefore not an arbitrary mathematical construction. It is precisely the topology naturally associated with Lorentzian causal structure under appropriate conditions.

⸻

47. Order Before Coordinates

Coordinates are representations.

Suppose

[
x^\mu
]

are coordinates assigned to events.

A coordinate transformation

[
x^\mu\rightarrow x’^\mu(x)
]

does not change the underlying causal relation.

Therefore coordinates should be regarded as derived descriptions.

The foundational hierarchy becomes

[
\boxed{
\prec
\rightarrow
\mathcal T
\rightarrow
\text{coordinate charts}.
}
]

Coordinates describe the causal-topological structure rather than creating it.

⸻

48. Order Before Metric

Similarly, if

[
g_{\mu\nu}
]

is reconstructed from causal order plus volume, then

[
g_{\mu\nu}
]

is not primitive.

The metric becomes a compressed tensorial representation of relational structure.

Thus:

[
\boxed{
\text{metric}

\text{representation of causal-geometric relations}.
}
]

This does not eliminate the metric. It relocates it in the logical hierarchy.

⸻

49. The Causal Geometrogenesis Chain

The complete proposed emergence sequence is

[
\boxed{
\mathcal C
\rightarrow
\mathcal T_{\mathcal C}
\rightarrow
\mathcal S_{\mathcal C}
\rightarrow
\mathcal G_{\mathcal C}
\rightarrow
[g_{\mathcal C}]
\rightarrow
g_{\mathcal C}
\rightarrow
\nabla_{\mathcal C}
\rightarrow
R_{\mathcal C}
\rightarrow
\mathcal D_{\mathcal C}.
}
]

Here:

[
\mathcal C

\text{causal order},
]

[
\mathcal T_{\mathcal C}

\text{causal topology},
]

[
\mathcal S_{\mathcal C}

\text{emergent spatial structure},
]

[
\mathcal G_{\mathcal C}

\text{causal geometry},
]

[
[g_{\mathcal C}]

\text{conformal metric},
]

[
g_{\mathcal C}

\text{metric after scale fixing},
]

[
\nabla_{\mathcal C}

\text{connection},
]

[
R_{\mathcal C}

\text{curvature},
]

[
\mathcal D_{\mathcal C}

\text{dynamics}.
]

Dimension appears as an invariant of the resulting structure:

[
d_{\mathcal C}

\operatorname{Dim}(\mathcal G_{\mathcal C}).
]

⸻

50. The Causal Emergence Diagram

The foundational architecture can be summarized as

[
\boxed{
\begin{array}{ccccc}
\text{CAUSAL ORDER}
&
\longrightarrow
&
\text{TOPOLOGY}
&
\longrightarrow
&
\text{GEOMETRY}
\[4pt]
\downarrow
&
&
\downarrow
&
&
\downarrow
\[4pt]
\text{precedence}
&
&
\text{locality}
&
&
\text{distance}
\[4pt]
\downarrow
&
&
\downarrow
&
&
\downarrow
\[4pt]
\text{time orientation}
&
&
\text{dimension}
&
&
\text{curvature}
\end{array}
}
]

The critical point is that every arrow represents a mathematical gate.

No arrow should be treated as automatic.

⸻

51. Causal Emergence Axioms

A foundational theory can be organized around the following axioms.

Axiom I — Relational Primacy

The primitive object is a causal relation

[
x\prec y.
]

Axiom II — Irreflexivity

[
\neg(x\prec x).
]

Axiom III — Transitivity

[
x\prec y,;y\prec z
\Rightarrow
x\prec z.
]

Axiom IV — Causal Distinguishability

Distinct physical events possess distinguishable causal profiles.

Axiom V — Locality

Causal influence propagates only through admissible causal relations.

Axiom VI — Topological Emergence

Coherent causal intervals generate a topology.

Axiom VII — Geometric Realizability

A causal structure may admit a geometric realization only if its local and global order properties satisfy the required compatibility conditions.

Axiom VIII — Scale Completion

Causal order determines at most conformal geometry unless an independent scale or volume structure is supplied.

Axiom IX — Dynamical Closure

If the causal structure is fundamental, its evolution must be specified by a law acting on causal structures themselves.

⸻

52. Functorial Formulation

Causal structures can be organized categorically.

Let

[
\mathbf{Caus}
]

be a category whose objects are causal structures and whose morphisms preserve causal relations.

A causal-preserving map

[
f:X\rightarrow Y
]

satisfies

[
x\prec_X y
\Rightarrow
f(x)\prec_Y f(y).
]

A reconstruction functor may take the form

[
\mathfrak T:
\mathbf{Caus}
\rightarrow
\mathbf{Top},
]

followed by

[
\mathfrak G:
\mathbf{Caus}
\rightarrow
\mathbf{Geom}.
]

Thus

[
\mathcal C
\mapsto
\mathfrak T(\mathcal C)
\mapsto
\mathfrak G(\mathcal C).
]

Functoriality requires that causal maps induce compatible maps between derived structures.

This prevents geometry from depending arbitrarily on representation.

⸻

53. Causal Gauge Freedom

Different representations may describe the same causal structure.

Let

[
\phi:X\rightarrow X
]

be an automorphism satisfying

[
x\prec y
\iff
\phi(x)\prec\phi(y).
]

Then

[
\phi\in\operatorname{Aut}(\mathcal C).
]

These transformations are causal gauge symmetries in the broad structural sense.

Physical observables should therefore be invariant under

[
\operatorname{Aut}(\mathcal C).
]

The fundamental observable is not the labeling of events but their relational structure.

⸻

54. Causal Observables

Candidate causal observables include:

Interval cardinality

[
N(x,y).
]

Chain length

[
L_{\max}(x,y).
]

Antichain width

[
W(\mathcal C).
]

Causal density

[
\rho_{\mathcal C}

\frac{#{(x,y):x\prec y}}
{#{(x,y):x\neq y}}.
]

Order dimension

[
\dim_{\rm ord}(\mathcal C).
]

Topological invariants

[
\chi,\quad
\beta_k,\quad
H_k.
]

Curvature proxies

[
\mathcal K_{\mathcal C}.
]

These quantities provide a language for describing causal structures without introducing coordinates.

⸻

55. Causal Entropy

A probability distribution over causal structures,

[
P(\mathcal C),
]

has Shannon entropy

[
S_{\mathcal C}

-\sum_{\mathcal C}
P(\mathcal C)
\log P(\mathcal C).
]

But there is another notion: the information contained in a fixed causal order.

Let

[
\Omega(\mathcal C)
]

be the number of admissible causal configurations compatible with specified constraints.

Then define

[
S_{\rm order}

\log\Omega(\mathcal C).
]

This measures combinatorial causal complexity rather than statistical uncertainty.

The two should not be conflated.

⸻

56. Causal Information Geometry

Once probability distributions over causal structures are introduced, one can construct an information geometry on the space

[
\mathcal P(\mathbf{Caus}).
]

For distributions

[
p_\theta(\mathcal C),
]

the Fisher metric becomes

[
g_{ab}

\sum_{\mathcal C}
p_\theta(\mathcal C)
\partial_a\log p_\theta(\mathcal C)
\partial_b\log p_\theta(\mathcal C).
]

This produces a geometry of uncertainty over causal structures.

It is distinct from the geometry generated by causal order itself.

Therefore two geometric layers must be distinguished:

[
\boxed{
\text{causal geometry}
\neq
\text{information geometry over causal models}.
}
]

They may interact, but they answer different questions.

⸻

57. Quantum Causality

The classical relation

[
x\prec y
]

may fail to have a unique classical truth value in generalized quantum settings.

One may instead have causal operators

[
\hat C_{xy}
]

or process structures encoding possible causal relations.

The foundational problem then becomes

[
\hat{\mathcal C}
\rightarrow
\mathcal T
\rightarrow
g?
]

This opens a broader theory in which classical causal order is a limiting regime of more general relational structures.

Such a generalization remains substantially open.

⸻

58. Causal Order and Time

Ordinary time is represented by a coordinate

[
t.
]

But causal order requires no coordinate.

If

[
x\prec y,
]

then (x) is earlier than (y) in the causal sense.

Thus time may be defined relationally:

[
\boxed{
\text{time order}

\text{causal precedence}.
}
]

A numerical time coordinate becomes a representation of that order.

However, not every partial order admits a global scalar time function preserving all causal relations.

Therefore:

[
\prec
\not\Rightarrow
t\in\mathbb R
]

without additional conditions.

⸻

59. Time Functions

A time function is a map

[
T:X\rightarrow\mathbb R
]

such that

[
x\prec y
\Rightarrow
T(x)<T(y).
]

The existence of such a function embeds the causal order into a real-valued temporal coordinate.

Thus:

[
\boxed{
\text{causal order}
\rightarrow
\text{time function}
}
]

is a nontrivial mathematical emergence problem.

If a global time function exists, it provides a numerical representation of causal precedence without being itself fundamental.

⸻

60. Causal Slicing

Given

[
T:X\rightarrow\mathbb R,
]

define level sets

[
\Sigma_t

T^{-1}(t).
]

These are candidate spatial slices.

Then the structure may decompose as

[
X
\approx
\bigcup_t\Sigma_t.
]

This provides a possible route:

[
\boxed{
\text{causal order}
\rightarrow
\text{time function}
\rightarrow
\text{spatial slices}.
}
]

But different time functions may generate different foliations.

Therefore the foliation is generally not fundamental.

⸻

61. Local versus Global Causality

A local causal structure can appear consistent while the global structure is pathological.

Therefore the theory requires both:

[
\mathcal C_{\rm local}
]

and

[
\mathcal C_{\rm global}.
]

Local conditions constrain neighborhoods.

Global conditions constrain:

* cycles,
* compactness,
* topology,
* horizons,
* global hyperbolicity,
* disconnected causal sectors.

The emergence problem must therefore operate at multiple scales.

⸻

62. Multiscale Causal Geometry

Define a coarse-graining operator

[
\mathcal R_\epsilon:
\mathcal C
\rightarrow
\mathcal C_\epsilon.
]

At small scale,

[
\mathcal C_\epsilon
]

contains microscopic relations.

At large scale,

[
\mathcal C_\epsilon
]

contains effective causal structure.

A dimension flow can then be defined:

[
d_{\rm eff}(\epsilon).
]

Similarly,

[
g_{\rm eff}(\epsilon)
]

and

[
R_{\rm eff}(\epsilon)
]

may emerge as scale-dependent quantities.

Thus causal geometry may possess a renormalization structure:

[
\boxed{
\mathcal C_{\rm microscopic}
\rightarrow
\mathcal C_{\rm macroscopic}.
}
]

⸻

63. Dimensional Flow

A particularly important possibility is

[
d_{\rm eff}(\epsilon)
\neq
\text{constant}.
]

Then the causal structure has scale-dependent dimension.

One might observe

[
d_{\rm eff}(\epsilon)
\rightarrow d_{\rm UV}
]

at short scales and

[
d_{\rm eff}(\epsilon)
\rightarrow d_{\rm IR}
]

at large scales.

The existence of such behavior would be a property of the causal model itself, not an assumption about a continuum manifold.

⸻

64. Causal Renormalization

Let

[
\mathcal R_b
]

coarse-grain causal relations by scale factor (b).

A fixed point satisfies

[
\mathcal R_b(\mathcal C^\ast)

\mathcal C^\ast.
]

Such fixed-point causal structures may represent universality classes of emergent geometry.

The foundational question becomes:

Which causal microscopic structures flow toward continuum Lorentzian geometry?

This is a sharper question than simply asking whether a discrete causal model can be embedded into spacetime.

⸻

65. Continuum Limit

Let

[
\mathcal C_N
]

be a sequence of finite causal structures.

A continuum limit requires

[
N\rightarrow\infty
]

together with an appropriate scaling of density, topology, and geometric observables.

One seeks convergence:

[
\mathcal C_N
\longrightarrow
(M,g)
]

in a suitable topology on causal structures.

Candidate convergence criteria include:

[
d_{\mathcal C_N}
\rightarrow
d_g,
]

[
\mathcal T_{\mathcal C_N}
\rightarrow
\mathcal T_g,
]

and

[
R_{\mathcal C_N}
\rightarrow
R_g.
]

A complete theory must specify the convergence notion rather than relying on visual resemblance.

⸻

66. Causal Geometry as Compression

A spacetime metric compresses enormous relational information into a tensor field:

[
g_{\mu\nu}(x).
]

If a causal order contains (O(N^2)) possible relations, while a smooth metric is locally represented by (D(D+1)/2) functions, then a successful continuum limit constitutes a dramatic compression of relational data.

This raises a foundational question:

[
\boxed{
\text{When is causal geometry a sufficient statistic for causal order?}
}
]

A smooth metric is successful if it preserves the relevant macroscopic causal observables.

⸻

67. Geometry as a Causal Compression

Let

[
\Pi:
\mathcal C
\rightarrow
g
]

be a geometric compression map.

It is adequate if

[
\operatorname{Obs}_{\rm causal}(\mathcal C)

\operatorname{Obs}_{\rm causal}(\Pi(\mathcal C))
]

for the selected class of observables.

The metric can then be regarded as a compressed representation of causal structure.

This provides a direct connection between causal mathematics and information geometry.

⸻

68. The Sufficiency Principle

A candidate emergent geometry should satisfy:

[
\boxed{
g
\text{ is causally sufficient}
}
]

if all macroscopic causal predictions depend on (\mathcal C) only through (g).

Formally,

[
P(O_{\rm causal}\mid\mathcal C)

P(O_{\rm causal}\mid g(\mathcal C)).
]

This is a statistical formulation of geometric emergence.

The continuum metric is then not merely a visualization but an effective sufficient representation.

⸻

69. Causal Geometry and General Relativity

If the emergent metric is

[
g_{\mu\nu},
]

one may then ask whether its dynamics reduce to Einstein gravity.

The target action is

[
S_{\rm EH}

\frac{1}{16\pi G}
\int
R\sqrt{-g},d^4x.
]

A causal theory does not obtain this merely by reconstructing (g).

It must additionally derive an effective dynamical principle

[
S_{\mathcal C}
]

whose continuum limit satisfies

[
S_{\mathcal C}
\rightarrow
S_{\rm EH}
+\text{corrections}.
]

This is a major independent gate.

Thus:

[
\boxed{
\text{causal order}
\rightarrow
g
}
]

does not imply

[
\boxed{
\text{causal order}
\rightarrow
\text{Einstein equations}.
}
]

⸻

70. Causal Field Theory

A general causal action may be written schematically as

[
S_{\mathcal C}

\mathcal A[
\prec,\mu].
]

The variational problem becomes

[
\delta S_{\mathcal C}=0.
]

If the fundamental variables are relation indicators

[
C_{ij}

\begin{cases}
1,&i\prec j,\
0,&\text{otherwise},
\end{cases}
]

then the action is a functional of

[
{C_{ij}}.
]

In a continuum limit,

[
C_{ij}
\rightarrow
g_{\mu\nu}(x)
]

only if geometric variables emerge.

⸻

71. Causal Energy

If causal structures evolve, one may define a complexity or transition functional

[
E_{\mathcal C}

\mathcal E(\mathcal C,\dot{\mathcal C}).
]

A causal dynamics might minimize

[
S_{\mathcal C}

\int
\mathcal L_{\mathcal C}
,d\lambda.
]

The resulting equations would determine which causal structures are dynamically admissible.

This creates a possible hierarchy:

[
\boxed{
\text{causal order}
\rightarrow
\text{causal action}
\rightarrow
\text{geometry}
\rightarrow
\text{physics}.
}
]

⸻

72. Causal Admissibility

Not every partial order should be considered physically admissible.

Define an admissibility functional

[
\mathfrak A[\mathcal C].
]

A causal structure is allowed if

[
\mathfrak A[\mathcal C]=0
]

or, more generally,

[
\mathfrak A[\mathcal C]\le\epsilon.
]

Constraints may include:

[
\text{acyclicity},
]

[
\text{local finiteness},
]

[
\text{dimension bounds},
]

[
\text{Lorentzian representability},
]

[
\text{locality},
]

[
\text{causal stability}.
]

This converts causal reconstruction into a constraint-selection problem.

⸻

73. Causal Consistency Functional

A generalized functional can combine these constraints:

[
\boxed{
\mathfrak C[\mathcal C]

\mathfrak C_{\rm order}
+
\mathfrak C_{\rm local}
+
\mathfrak C_{\rm dim}
+
\mathfrak C_{\rm geom}
+
\mathfrak C_{\rm global}.
}
]

A physical candidate satisfies

[
\mathfrak C[\mathcal C]=0.
]

This does not select a unique universe automatically. It defines a mathematical criterion for admissibility.

⸻

74. No-Go: Arbitrary Partial Orders Are Not Spacetimes

A generic partial order does not automatically correspond to a smooth manifold.

The set of all partial orders is vastly larger than the subset representable by Lorentzian manifolds.

Therefore:

[
\boxed{
\text{partial order}
\not\Rightarrow
\text{spacetime}.
}
]

A continuum spacetime requires special relational regularity.

This is one of the most important constraints on causal fundamentality.

⸻

75. No-Go: Order Alone Does Not Fix Dimension

The same abstract order may admit different types of representations or possess multiple notions of dimension.

Therefore

[
\boxed{
\prec
\not\Rightarrow
D
}
]

without specifying:

* the representation class,
* scaling regime,
* dimension estimator,
* continuum assumptions.

Dimension must be derived or selected by a well-defined criterion.

⸻

76. No-Go: Causal Order Does Not Automatically Produce Dynamics

An order tells us which events precede others.

It does not tell us:

[
\frac{d\mathcal C}{d\lambda}.
]

A dynamical law must be supplied.

Thus

[
\boxed{
\text{kinematics}
\neq
\text{dynamics}.
}
]

This distinction is essential for any claim of fundamental causality.

⸻

77. No-Go: Causality Does Not Automatically Produce Probability

A causal relation does not imply a probability distribution.

Therefore

[
\prec
\not\Rightarrow
P.
]

Probability must either be independently introduced or derived from a dynamical ensemble of causal structures.

⸻

78. No-Go: Causal Structure Does Not Automatically Produce Quantum Mechanics

Likewise,

[
\prec
\not\Rightarrow
\hbar.
]

A causal order contains relational precedence but no obvious quantum amplitude, Hilbert space, or noncommutative algebra.

A quantum causal theory therefore requires an additional emergence mechanism.

⸻

79. A General Reconstruction Theorem

The central mathematical architecture can be expressed as follows.

Theorem 3 — Causal Geometric Reconstruction Principle

Suppose a causal structure (\mathcal C=(X,\prec)) satisfies:

1. causal transitivity;
2. causal distinguishability;
3. sufficiently coherent interval topology;
4. local regularity;
5. finite effective dimension;
6. existence of a compatible Lorentzian realization;
7. an independent volume or scale measure.

Then, within the chosen realization class, the causal order determines a conformal geometry and the volume structure fixes the conformal scale.

Hence:

[
\boxed{
(\mathcal C,\mu)
\rightarrow
(M,g)
}
]

up to residual geometric symmetries and reconstruction ambiguities.

The theorem is conditional: it does not claim that every causal structure satisfies these hypotheses.

⸻

80. The Causal Emergence Gate

The theory can therefore be organized into gates.

Gate 1 — Order

[
\mathcal C=(X,\prec).
]

Gate 2 — Consistency

[
\prec
\text{ is acyclic and transitive}.
]

Gate 3 — Distinguishability

[
x\neq y
\Rightarrow
(P_x,F_x)\neq(P_y,F_y).
]

Gate 4 — Topology

[
\mathcal C
\rightarrow
\mathcal T_{\mathcal C}.
]

Gate 5 — Dimension

[
\mathcal T_{\mathcal C}
\rightarrow
d_{\mathcal C}.
]

Gate 6 — Conformal geometry

[
\mathcal C
\rightarrow
[g].
]

Gate 7 — Scale

[
(\mathcal C,\mu)
\rightarrow
g.
]

Gate 8 — Curvature

[
g
\rightarrow
R.
]

Gate 9 — Dynamics

[
\mathcal C
\rightarrow
S_{\mathcal C}
\rightarrow
\text{equations of motion}.
]

Gate 10 — Physical identification

[
(M,g,\mathcal C)
\rightarrow
\text{observed spacetime}.
]

Each gate must be independently established.

⸻

81. Causal Geometry and Information Geometry

The theory naturally interfaces with information geometry.

Let

[
D_{\mathcal C}(x,y)
]

measure the distinguishability of causal neighborhoods.

A local expansion may give

[
D_{\mathcal C}(x(\theta),x(\theta+d\theta))

\frac12
g^{\mathcal C}_{ab}
d\theta^a d\theta^b
+
O(d\theta^3).
]

Then

[
g^{\mathcal C}_{ab}
]

is an information metric on the space of causal configurations.

This creates two metrics:

[
g_{\rm causal}
]

on event geometry, and

[
g_{\rm info}
]

on the space of causal models.

They must not be conflated.

⸻

82. Causal Networks and Geometry

Suppose events are represented as nodes and causal relations as directed edges.

Define an adjacency matrix

[
A_{ij}

\begin{cases}
1,&i\prec j,\
0,&\text{otherwise}.
\end{cases}
]

The transitive closure

[
A^\ast
]

contains global causal reachability.

Spectral properties of

[
A^\ast
]

can provide information about:

* connectivity,
* dimension,
* expansion,
* bottlenecks,
* causal horizons.

However, spectral graph geometry remains a representation-dependent layer.

The order itself remains the more primitive object.

⸻

83. Causal Horizons

Define the future-reachable set

[
J^+(x).
]

A causal horizon can emerge when the structure partitions into regions with restricted causal accessibility.

Let

[
X=A\cup B
]

such that

[
J^+(A)\cap B=\varnothing
]

within a specified domain.

The boundary between causal accessibility classes becomes a candidate horizon.

Thus horizons can be defined relationally before metric distance is introduced.

⸻

84. Black-Hole-Like Causal Structures

A black-hole region is characterized causally by restricted future accessibility.

In continuum general relativity, the event horizon is defined globally through causal structure.

This suggests a broader principle:

[
\boxed{
\text{horizon}

\text{boundary of causal accessibility}.
}
]

The metric description is then one representation of this deeper relation.

⸻

85. Causal Topological Transitions

If causal relations change,

[
\mathcal C_1
\rightarrow
\mathcal C_2,
]

the induced topology may change:

[
\mathcal T_1
\not\cong
\mathcal T_2.
]

Such a transition represents a topological phase change in causal structure.

This opens the possibility of describing topology change as a relational transition rather than a primitive geometric event.

⸻

86. Causal Phase Structure

Define a space of admissible causal structures

[
\mathfrak C.
]

A causal phase is an equivalence class

[
[\mathcal C]
]

under selected macroscopic invariants.

Two microscopic structures may belong to the same causal phase if

[
d_{\rm eff},
\quad
\mathcal T,
\quad
[g],
\quad
R
]

agree at macroscopic scales.

Thus:

[
\boxed{
\text{microscopic causal diversity}
\rightarrow
\text{macroscopic geometric universality}.
}
]

⸻

87. Universality

A continuum geometry may be universal even when the underlying causal microstructures differ.

Suppose

[
\mathcal C_1,\mathcal C_2,\ldots
]

all flow under coarse-graining to

[
\mathcal C^\ast.
]

Then the emergent geometry is insensitive to microscopic details.

This would explain how smooth spacetime could emerge robustly from many possible microscopic causal structures.

Mathematically:

[
\mathcal R_b(\mathcal C_i)
\rightarrow
\mathcal C^\ast.
]

⸻

88. Causal Fixed Points

A causal fixed point satisfies

[
\mathcal R_b(\mathcal C^\ast)=\mathcal C^\ast.
]

If its emergent dimension is

[
d^\ast=4,
]

and its large-scale causal structure corresponds to Lorentzian geometry, then it becomes a candidate continuum spacetime universality class.

This is a mathematically precise target for causal geometrogenesis.

⸻

89. Empirical Interface

A foundational causal theory becomes physical only when it produces observable consequences.

Potential observables include:

[
d_{\rm eff}(L),
]

[
N_{\rm causal}(L),
]

[
\mathcal K_{\mathcal C}(L),
]

[
\tau_{\mathcal C}(x,y),
]

and deviations from continuum causal propagation.

A theory could therefore predict:

[
\boxed{
\text{observable}

F(\mathcal C_{\rm micro}).
}
]

The critical requirement is that (F) be derived rather than chosen to reproduce known observations.

⸻

90. Possible Experimental Signatures

If causal structure has microscopic discreteness, possible effects could include:

* scale-dependent dimension;
* deviations from continuum causal propagation;
* microscopic fluctuations in causal intervals;
* modified dispersion relations if additional dynamics couple to the causal substrate;
* violations of exact Lorentz symmetry;
* stochastic causal fluctuations;
* correlations associated with causal-set discreteness.

None of these follows from causal order alone.

They are model-dependent consequences requiring a concrete dynamical realization.

⸻

91. Falsifiability

A causal theory becomes falsifiable if it produces a statement of the form

[
\mathcal O_{\rm observed}

F(\mathcal C)
]

with no freely adjustable function capable of fitting arbitrary data.

For example, a theory might predict

[
d_{\rm eff}(L)\rightarrow4
]

over a specified scale range.

Or it might predict a definite causal fluctuation spectrum

[
P_{\rm causal}(k).
]

Such predictions distinguish a foundational theory from a reinterpretation of existing mathematics.

⸻

92. Relationship to Established Mathematics

The proposed framework does not replace existing causal mathematics.

It synthesizes several established sectors:

Order theory

[
(X,\prec).
]

Topology

[
\mathcal T(X).
]

Lorentzian geometry

[
(M,g).
]

Causal inference

[
G,\operatorname{do}(\cdot),\text{counterfactuals}.
]

Probability

[
P(X,Y,\ldots).
]

Information theory

[
H,I,D,K.
]

Graph theory

[
G=(V,E).
]

Category theory

[
\mathbf{Caus}.
]

Dynamical systems

[
\dot{\mathcal C}=\mathcal F[\mathcal C].
]

The novelty proposed here is the foundational organization of these structures around causal order as the candidate primitive.

⸻

93. What Is Established

The following components are established mathematics or well-developed theories:

[
\boxed{
\text{partial orders}
}
]

[
\boxed{
\text{causal sets}
}
]

[
\boxed{
\text{Alexandrov topology}
}
]

[
\boxed{
\text{Lorentzian causal reconstruction}
}
]

[
\boxed{
\text{causal inference}
}
]

[
\boxed{
\text{order dimension}
}
]

[
\boxed{
\text{geometric dimension estimators}
}
]

[
\boxed{
\text{information-theoretic descriptions of causal models}.
}
]

⸻

94. What This Framework Proposes

The proposed synthesis is:

[
\boxed{
\mathcal C
\rightarrow
\mathcal T_{\mathcal C}
\rightarrow
d_{\mathcal C}
\rightarrow
[g_{\mathcal C}]
\rightarrow
g_{\mathcal C}
\rightarrow
R_{\mathcal C}
\rightarrow
\mathcal D_{\mathcal C}.
}
]

The central hypothesis is not that every partial order becomes spacetime.

It is:

Spacetime geometry may be understood mathematically as a special stable regime of causal relational structure.

This is a testable structural hypothesis.

⸻

95. The Strongest Foundational Form

The strongest form of the program is:

[
\boxed{
\text{CAUSAL ORDER}
;\equiv;
\text{primitive relational structure}
}
]

with

[
\boxed{
\text{TOPOLOGY}

\mathcal F_T(\mathcal C),
}
]

[
\boxed{
\text{DIMENSION}

\mathcal F_D(\mathcal C),
}
]

[
\boxed{
\text{CONFORMAL GEOMETRY}

\mathcal F_G(\mathcal C),
}
]

[
\boxed{
\text{METRIC SCALE}

\mathcal F_\mu(\mathcal C,\mu),
}
]

[
\boxed{
\text{CURVATURE}

\mathcal F_R(\mathcal C,\mu),
}
]

and

[
\boxed{
\text{DYNAMICS}

\mathcal F_D^{\rm dyn}(\mathcal C).
}
]

⸻

96. The Minimal Primitive

The entire theory can therefore be compressed to one primitive relation:

[
\boxed{x\prec y.}
]

From this relation one asks, in order:

[
\boxed{
\begin{aligned}
1.;&\text{Is the relation consistent?}\
2.;&\text{Can events be causally distinguished?}\
3.;&\text{Do causal intervals form neighborhoods?}\
4.;&\text{Does a topology emerge?}\
5.;&\text{Does a finite dimension emerge?}\
6.;&\text{Does a causal cone structure emerge?}\
7.;&\text{Does a conformal metric exist?}\
8.;&\text{What fixes its scale?}\
9.;&\text{Does curvature emerge?}\
10.;&\text{Does a dynamical law emerge?}
\end{aligned}
}
]

This sequence defines the core research program.

⸻

97. The Causal Geometrogenesis Equation

The central conceptual equation of the framework is

[
\boxed{
\mathcal C
\overset{\rm consistency}{\longrightarrow}
\mathcal T_{\mathcal C}
\overset{\rm scaling}{\longrightarrow}
d_{\mathcal C}
\overset{\rm reconstruction}{\longrightarrow}
[g_{\mathcal C}]
\overset{\rm volume}{\longrightarrow}
g_{\mathcal C}
\overset{\nabla}{\longrightarrow}
R_{\mathcal C}
\overset{\rm dynamics}{\longrightarrow}
\mathcal D_{\mathcal C}.
}
]

The arrows are not assumptions of equivalence.

They are mathematical emergence problems.

⸻

98. Fundamental Questions

The theory identifies the following foundational questions.

Q1. What is the minimum structure required for causal order?

Q2. When does a partial order possess a physically meaningful topology?

Q3. When does order determine dimension?

Q4. When does causal order determine conformal geometry?

Q5. What additional information fixes metric scale?

Q6. Can spatial geometry be reconstructed from causal neighborhoods?

Q7. Can curvature be calculated directly from order invariants?

Q8. What causal structures admit Lorentzian continuum limits?

Q9. Which microscopic causal structures belong to the same geometric universality class?

Q10. Can Einstein dynamics emerge from a causal action?

Q11. Can quantum dynamics emerge from causal structure?

Q12. Is causal order fundamentally classical, or itself emergent from a deeper algebraic structure?

⸻

99. Research Program

A rigorous development should proceed through the following stages.

Phase I — Order

Classify admissible primitive causal structures.

Phase II — Topology

Determine sufficient conditions for order-induced topology.

Phase III — Dimension

Develop order-only dimension estimators and prove convergence.

Phase IV — Geometry

Classify Lorentzian-representable causal structures.

Phase V — Scale

Determine the minimal additional data required for metric reconstruction.

Phase VI — Curvature

Construct order-theoretic curvature invariants.

Phase VII — Dynamics

Define actions and evolution laws over causal structures.

Phase VIII — Continuum Limit

Establish convergence to smooth Lorentzian manifolds.

Phase IX — Physical Dynamics

Determine whether Einstein or other field equations emerge.

Phase X — Observation

Derive experimentally distinguishable consequences.

⸻

100. Open Mathematical Problems

Several deep problems remain.

Problem 1 — Universal causal dimension

Find an intrinsic dimension functional

[
D:\mathbf{Caus}\rightarrow\mathbb R
]

with strong continuum compatibility.

Problem 2 — Causal curvature

Construct

[
R_{\mathcal C}
]

directly from relational order.

Problem 3 — Metric reconstruction

Characterize precisely when

[
(\mathcal C,\mu)
]

uniquely determines a Lorentzian metric.

Problem 4 — Continuum convergence

Define a mathematically robust topology on the space of causal structures such that

[
\mathcal C_n\rightarrow(M,g).
]

Problem 5 — Dynamics

Find causal actions whose stable large-scale solutions are Lorentzian.

Problem 6 — Quantum extension

Determine whether quantum causal structures reduce to classical partial orders in an appropriate limit.

⸻

101. A General No-Go Hierarchy

The framework imposes the following logical restrictions:

[
\boxed{
\mathcal C
\not\Rightarrow
\mathcal T
}
]

without regularity;

[
\boxed{
\mathcal T
\not\Rightarrow
g
}
]

without metric data;

[
\boxed{
\mathcal C
\not\Rightarrow
g
}
]

without scale information;

[
\boxed{
g
\not\Rightarrow
\text{Einstein dynamics}
}
]

without a dynamical law;

and

[
\boxed{
\mathcal C
\not\Rightarrow
\text{quantum mechanics}
}
]

without an additional quantum structure.

These constraints prevent the foundational hypothesis from becoming an uncontrolled chain of identifications.

⸻

102. Causal Order as a Candidate Primitive of Spacetime

The strongest conceptual conclusion is therefore not that spacetime has already been derived from causality.

Rather:

[
\boxed{
\text{causal order is mathematically capable of carrying a substantial portion of spacetime structure}.
}
]

In sufficiently regular continuum settings:

[
\text{causal order}
\rightarrow
\text{conformal structure},
]

while

[
\text{causal order}
+
\text{volume}
\rightarrow
\text{full metric structure}.
]

This gives causal order a particularly privileged position among possible pre-geometric structures.

⸻

103. The Foundational Reversal

The conventional conceptual sequence is

[
\boxed{
\text{spacetime}
\rightarrow
\text{metric}
\rightarrow
\text{light cones}
\rightarrow
\text{causality}.
}
]

The proposed foundational sequence reverses the dependency:

[
\boxed{
\text{causality}
\rightarrow
\text{light-cone structure}
\rightarrow
\text{topology}
\rightarrow
\text{conformal geometry}
\rightarrow
\text{metric}
\rightarrow
\text{spacetime}.
}
]

The distinction between these two sequences is the central philosophical and mathematical motivation for the theory.

⸻

104. Final Synthesis

The Mathematics of Causality proposed here treats causal precedence as a primitive relational object:

[
\boxed{x\prec y.}
]

From this starting point, the theory asks whether increasingly rich mathematical structures can emerge:

[
\boxed{
\begin{aligned}
\mathcal C
&=(X,\prec)
\
&\downarrow
\
\mathcal T_{\mathcal C}
&=\text{causal topology}
\
&\downarrow
\
d_{\mathcal C}
&=\text{emergent dimension}
\
&\downarrow
\
[g_{\mathcal C}]
&=\text{conformal geometry}
\
&\downarrow
\
g_{\mathcal C}
&=\text{metric geometry}
\
&\downarrow
\
\nabla_{\mathcal C}
&=\text{connection}
\
&\downarrow
\
R_{\mathcal C}
&=\text{curvature}
\
&\downarrow
\
\mathcal D_{\mathcal C}
&=\text{dynamics}.
\end{aligned}
}
]

The crucial lesson is that these arrows have different logical status.

Some are established under known mathematical hypotheses.

Some are conditional reconstruction results.

Some are open research problems.

None should be silently promoted from possibility to theorem.

The deepest structure is therefore not

[
\text{metric}\rightarrow\text{causality},
]

but the possibility of

[
\boxed{
\text{causal order}
\rightarrow
\text{geometry}.
}
]

The theory identifies a precise mathematical program for investigating that possibility.

Its central object is not a coordinate.

It is not a distance.

It is not a probability distribution.

It is not initially a manifold.

It is the relation

[
\boxed{x\prec y.}
]

If a sufficiently constrained family of such relations can generate topology, stable dimension, Lorentzian conformal structure, metric scale, curvature, and ultimately dynamical laws, then spacetime can be interpreted as an emergent geometric representation of a deeper causal organization.

The resulting foundational hierarchy is:

[
\boxed{
\text{CAUSAL ORDER}
\rightarrow
\text{TOPOLOGY}
\rightarrow
\text{DIMENSION}
\rightarrow
\text{CONFORMAL GEOMETRY}
\rightarrow
\text{METRIC}
\rightarrow
\text{CURVATURE}
\rightarrow
\text{DYNAMICS}
\rightarrow
\text{PHYSICAL SPACETIME}.
}
]

This is the central mathematical thesis of the proposed Mathematics of Causality: not that causality has already been proven to be the primitive of reality, but that causal order provides a mathematically precise candidate substrate from which substantial portions of geometry—and potentially spacetime itself—can be investigated as emergent structures.

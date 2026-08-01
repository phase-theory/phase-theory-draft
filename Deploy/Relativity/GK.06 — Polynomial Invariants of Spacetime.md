General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part VI — Polynomial Invariants of Spacetime

⸻

37. Introduction: From Spectra to Algebraic Invariants

Parts I–V introduced the geometric and statistical structure of closed-null topology.

The construction:

[
(M,g)
\rightarrow
\mathcal N_c
\rightarrow
\mathfrak N
\rightarrow
\mathcal L(M,g)
]

produced a spacetime-dependent spectrum of null links.

A spectrum alone, however, is not yet an efficient invariant.

Knot theory achieves compression through polynomial invariants.

The objective of this part is therefore to define algebraic invariants of null geodesic flow.

The central object introduced here is:

[
\boxed{
\mathcal J[g]
}
]

the spacetime knot polynomial.

⸻

38. Jones-Type Invariant of Null Flows

38.1 Classical Motivation

For an oriented link:

[
L\subset\mathbb R^3,
]

the Jones polynomial:

[
V_L(q)
]

is characterized recursively by the skein relation:

[
q^{-1}V(L_+)

qV(L_-)

(q^{1/2}-q^{-1/2})
V(L_0).
]

Its power lies in distinguishing links sharing identical linking numbers.

The present construction replaces embedded Euclidean curves with closed null geodesics.

⸻

38.2 Null-Link Projection

Let:

[
L

{
\gamma_1,\ldots,\gamma_n
}
\subset
\mathcal N_c.
]

Choose admissible projection:

[
\pi:
M\rightarrow\Sigma.
]

Define:

[
D(L)

\pi(L).
]

Crossings inherit orientation from future-directed null transport.

Assign crossing sign:

[
\epsilon(c)\in{+1,-1}.
]

⸻

38.3 Null Bracket Functional

Define generalized bracket:

[
\langle D\rangle_N.
]

Recursive rule:

[
\boxed{
\langle
\raisebox{-0.1cm}{(\times)}
\rangle_N

A
\left\langle
\raisebox{-0.1cm}{(\smile)}
\right\rangle_N
+
A^{-1}
\left\langle
\raisebox{-0.1cm}{(\frown)}
\right\rangle_N
}
]

with normalization:

[
\langle\emptyset\rangle_N=1.
]

Loop removal:

[
\langle
L\cup\bigcirc
\rangle_N

(-A^2-A^{-2})
\langle L\rangle_N.
]

Curvature enters through weighted crossings.

⸻

38.4 Curvature-Corrected Crossing Weight

Define local optical curvature:

[
\kappa_c

R_{\mu\nu\rho\sigma}
u^\mu
v^\nu
u^\rho
v^\sigma.
]

Modify crossing factor:

[
A
\rightarrow
A
e^{-\eta\kappa_c}.
]

Thus crossings become geometry-sensitive.

⸻

Definition 12 (Null Jones Polynomial)

Define:

[
\boxed{
J_N(L;q)

(-A^3)^{-w(L)}
\langle D(L)\rangle_N
}
]

where:

[
q=A^{-4}.
]

This reduces to the ordinary Jones polynomial in flat-space limits.

⸻

39. Polynomial Structure of Null Flow Ensembles

Individual links are insufficient.

We seek an invariant of the entire null spectrum.

⸻

39.1 Ensemble Averaging

For:

[
\mathcal L(M,g)

{
[L_i]
},
]

define weighted average:

[
\mathbb J(q)

\sum_i
P_i
J_N(L_i;q).
]

Weights:

[
P_i=P([L_i]).
]

⸻

39.2 Orbit-Length Weighting

Introduce suppression:

[
P_i

\frac{
m_i
e^{-\beta\lambda_i}
}{
Z_N
}.
]

Partition function:

[
Z_N

\sum_i
m_i
e^{-\beta\lambda_i}.
]

Shorter optical cycles contribute more strongly.

⸻

Definition 13 (Null Flow Polynomial)

Define:

[
\boxed{
\Phi_N(M,g;q)

\sum_i
P_i
J_N(L_i;q)
}
]

This is the first polynomial observable of null topology.

⸻

40. HOMFLY Extensions

Jones invariants detect limited topology.

To classify richer null-link families, additional variables are introduced.

⸻

40.1 Generalized Skein Equation

Define polynomial:

[
P_N(L;a,z).
]

Require:

[
\boxed{
aP_N(L_+)

a^{-1}P_N(L_-)

zP_N(L_0)
}
]

Normalization:

[
P_N(\bigcirc)=1.
]

⸻

40.2 Curvature Coupling

Introduce effective variables:

[
a

a_0
e^{-\alpha R},
]

[
z

z_0
e^{-\beta K},
]

where:

[
R
]

is scalar curvature and

[
K
]

a null-topological density.

Thus:

[
P_N

P_N(a(R),z(K)).
]

⸻

40.3 Seifert Expansion

For each link:

[
L
]

construct generalized Seifert surfaces:

[
S_i.
]

Then:

[
P_N

\sum
c_i
a^{m_i}
z^{g_i},
]

where:

[
g_i
]

is Seifert genus.

Topology and geometry become coencoded.

⸻

Definition 14 (Generalized Null HOMFLY Polynomial)

Define:

[
\boxed{
\mathcal H_N(M,g)

\sum_i
P_i
P_N(L_i;a,z)
}
]

This invariant captures higher-order structure absent from (J_N).

⸻

41. Skein Relations for Null Geodesic Reconnection

Polynomial invariants require local transformation laws.

⸻

41.1 Null Crossing Events

Consider a critical metric:

[
g_c.
]

At:

[
g=g_c,
]

two null trajectories approach:

[
\gamma_1\cap\gamma_2.
]

Topology changes.

⸻

41.2 Geometric Resolution

Three local states:

Positive crossing:

[
L_+.
]

Negative crossing:

[
L_-.
]

Resolved orbit:

[
L_0.
]

⸻

Definition 15 (Null Skein Operator)

Define:

[
\boxed{
\mathcal S

\alpha T_+
+
\beta T_-
+
\gamma T_0
}
]

acting on local reconnection sectors.

⸻

41.3 Dynamical Skein Equation

Introduce curvature-dependent coefficients:

[
\alpha

e^{-\chi_+},
]

[
\beta

e^{-\chi_-},
]

[
\gamma

e^{-\chi_0}.
]

Then:

[
\boxed{
e^{-\chi_+}
P(L_+)

e^{-\chi_-}
P(L_-)

e^{-\chi_0}
P(L_0)
}
]

where:

[
\chi
]

depends on optical stability.

⸻

Theorem 5 (Polynomial Continuity Across Reconnection)

Suppose reconnection occurs through a finite critical region.

Then polynomial evolution satisfies the null skein equation.

Proof.

Local topology changes only within compact neighborhoods.

Recursive smoothing preserves invariant continuity.

∎

⸻

42. Construction of the Spacetime Knot Polynomial

We now define the principal invariant.

⸻

42.1 Local Polynomial Density

Associate to each null link:

[
J_N(L;q).
]

Define spectral measure:

[
d\Omega_L.
]

Construct density:

[
\rho_J(q,L)

J_N(L;q)
d\Omega_L.
]

⸻

42.2 Global Construction

Integrate over all closed-null classes.

Define:

[
\boxed{
\mathcal Jg

\int_{\mathcal L(M,g)}
J_N(L;q)
,d\Omega_L
}
]

Equivalent discrete form:

[
\boxed{
\mathcal Jg

\sum_i
m_i
e^{-\beta\lambda_i}
J_N(L_i;q)
}
]

This object assigns a polynomial directly to spacetime.

⸻

42.3 Coefficient Interpretation

Write:

[
\mathcal J[g]

\sum_n
c_nq^n.
]

Interpretation:

[
c_n
]

measures weighted abundance of null topology at complexity scale (n).

⸻

42.4 Functional Derivative

Define:

[
\frac{\delta\mathcal J}{\delta g_{\mu\nu}}.
]

Interpretation:

response of null topology to geometry.

Large derivative indicates topological instability.

⸻

Theorem 6 (Diffeomorphism Covariance)

For:

[
g\rightarrow\varphi^\ast g,
]

the spacetime knot polynomial satisfies:

[
\boxed{
\mathcal J[g]

\mathcal J[\varphi^\ast g]
}
]

provided null-link classes are preserved.

Proof.

Each contributing term is isotopy invariant.

Measure and multiplicity remain unchanged.

∎

⸻

43. Polynomial Hierarchy of Spacetime

We collect the algebraic observables.

Level 0:

[
\mathfrak L
]

linking numbers

Level 1:

[
J_N
]

null Jones invariants

Level 2:

[
P_N
]

null HOMFLY invariants

Level 3:

[
\Phi_N
]

ensemble flow polynomial

Level 4:

[
\boxed{
\mathcal J[g]
}
]

complete spacetime knot polynomial

⸻

44. Fourth Structural Principle

Principle IV — Polynomial Encoding of Causal Topology

The topology of closed null geodesic flow admits finite algebraic compression.

For an admissible spacetime:

[
(M,g)
\longrightarrow
\mathcal J[g]
]

where:

[
\mathcal J[g]
]

encodes the weighted topology of all closed-null link sectors.

Spacetime becomes representable by a polynomial object.

⸻

Transition to Part VII

Part VII develops the geometric substrate underlying these invariants:

Seifert Geometry and Null Homology

including:

* Seifert surfaces for null loops,
* genus of null-link families,
* homological decomposition,
* cobordism of closed null geodesics.

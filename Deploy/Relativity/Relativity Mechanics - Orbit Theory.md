# Orbit Theory: The Primitive Ontology of Relativity Mechanics

## Abstract

Orbit Theory is the first derived theory of Relativity Mechanics. It answers the primitive ontological question:

\[
\boxed{\text{What is a physical object?}}
\]

Within Relativity Mechanics, the answer is:

\[
\boxed{[\omega]=G\cdot\omega.}
\]

A physical object is not an individual description \(\omega\in\Omega\). It is the equivalence class of all admissible descriptions related by the admissibility group \(G\). The orbit is therefore the minimal ontological unit of Relativity Mechanics.

This paper develops Orbit Theory as a rigorous mathematical discipline. Starting from the relativity schema

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

we define orbit equivalence, quotient spaces, stabilizers, orbit types, stratifications, principal bundles, groupoids, and stacky refinements. We show how physical objecthood is mathematically constituted by orbit structure. We further demonstrate that the principal objects of Newtonian mechanics, general relativity, gauge theory, quantum theory, and string theory are naturally understood as orbits under appropriate admissibility groups.

Orbit Theory does not yet specify observables, observers, dynamics, information, quantum structure, geometry, gauge fields, or frames. It establishes the prior ontological ground: before a theory can say what can be measured, how things evolve, or what geometry they inhabit, it must first say what counts as a physical object. In Relativity Mechanics, that object is an orbit.

---

## 1. Introduction

Every physical theory distinguishes, explicitly or implicitly, between those features of a description that are physically significant and those that are artifacts of presentation. Coordinates, gauge choices, reference frames, phases, bases, parametrizations, and trivializations are standard examples of descriptive structures that do not, by themselves, constitute physical content.

Relativity Mechanics makes this distinction foundational. It begins with a space of admissible descriptions \(\Omega\), a group \(G\) of transformations that preserve physical content, and the quotient map

\[
I:\Omega\to\Omega/G.
\]

The central claim of Relativity Mechanics is that physical reality is not represented by individual descriptions but by equivalence classes of descriptions.

Orbit Theory is the theory of this equivalence-class ontology. Its primitive question is:

\[
\text{What is a physical object?}
\]

Its answer is:

\[
\boxed{
\text{A physical object is an orbit }[\omega]=G\cdot\omega.
}
\]

This is not a metaphor. It is an ontological definition. A physical object is mathematically constituted by the totality of admissible descriptions related by the admissibility group. The individual description \(\omega\) is a presentation of the object; the orbit \([\omega]\) is the object itself.

Everything else in Relativity Mechanics builds upon this orbit ontology. Invariant Theory asks what can be predicated of orbits. Observer Theory asks how orbits are accessed by observational structures. Constraint Mechanics asks how admissible orbits are selected. Relativistic Dynamics asks how orbits evolve. Relativistic Quantum Theory asks how orbits appear in Hilbert space. Gauge Theory and Frame Theory arise when admissibility groups become local and frame-like.

But the first step is ontological. Orbit Theory provides it.

---

## 2. The Relativity Schema

A Relativity Mechanics theory is specified by a quadruple

\[
\boxed{
\mathcal R=(\Omega,G,\triangleright,I)
}
\]

where:

1. \(\Omega\) is a description space,
2. \(G\) is an admissibility group,
3. \(\triangleright:G\times\Omega\to\Omega\) is a group action,
4. \(I:\Omega\to\Omega/G\) is the invariant projection.

The action satisfies

\[
e\triangleright\omega=\omega,
\]

\[
g_1\triangleright(g_2\triangleright\omega)
=
(g_1g_2)\triangleright\omega,
\]

for all \(g_1,g_2\in G\), \(\omega\in\Omega\).

For notational simplicity, we write

\[
g\cdot\omega:=g\triangleright\omega.
\]

The orbit of \(\omega\) is

\[
[\omega]
=
G\cdot\omega
=
\{g\cdot\omega\mid g\in G\}.
\]

The quotient space is

\[
\Omega/G
=
\{[\omega]\mid \omega\in\Omega\}.
\]

The projection is

\[
I(\omega)=[\omega].
\]

Orbit Theory is the study of the structure of the orbits of \(G\curvearrowright\Omega\) and their ontological interpretation.

---

## 3. Axioms of Orbit Theory

Orbit Theory introduces no new primitive ontology beyond Relativity Mechanics. It makes the ontology explicit through the following axioms.

### Axiom I: Description

A physical system is accessible only through admissible descriptions.

\[
\omega\in\Omega.
\]

### Axiom II: Admissibility

Descriptions related by \(G\) represent the same physical content.

\[
\omega\sim g\cdot\omega.
\]

### Axiom III: Orbit Identity

Two descriptions represent the same physical object if and only if they lie on the same orbit:

\[
\omega\sim\omega'
\iff
\exists g\in G:\omega'=g\cdot\omega.
\]

### Axiom IV: Objecthood

A physical object is an orbit:

\[
\boxed{
\text{Object} = [\omega]=G\cdot\omega.
}
\]

### Axiom V: Type Structure

The type or species of a physical object is determined by the orbit structure, including stabilizer type, orbit dimension, and quotient stratum.

These axioms define the orbit ontology of Relativity Mechanics.

---

## 4. Orbit Equivalence

The relation

\[
\omega\sim\omega'
\iff
\exists g\in G:\omega'=g\cdot\omega
\]

is an equivalence relation.

### Proposition 4.1: Orbit equivalence is an equivalence relation

**Proof.**

1. **Reflexivity.**  
   Since \(e\in G\) and \(e\cdot\omega=\omega\),

   \[
   \omega\sim\omega.
   \]

2. **Symmetry.**  
   If \(\omega'\!=g\cdot\omega\), then

   \[
   g^{-1}\cdot\omega'=\omega,
   \]

   so \(\omega\sim\omega'\).

3. **Transitivity.**  
   If \(\omega'\!=g\cdot\omega\) and \(\omega''\!=h\cdot\omega'\), then

   \[
   \omega''=h\cdot(g\cdot\omega)=(hg)\cdot\omega,
   \]

   so \(\omega\sim\omega''\).

Therefore \(\sim\) is an equivalence relation.

\(\square\)

The equivalence classes are precisely the orbits:

\[
[\omega]=\{\omega'\in\Omega\mid \omega'\sim\omega\}.
\]

Thus the quotient \(\Omega/G\) is the space of physical objects, at least at the level of the given description schema.

---

## 5. The Ontological Primacy of Orbits

In ordinary representational thinking, one treats a particular description as the object. For example, one may treat a coordinate expression \(g_{\mu\nu}(x)\) as the gravitational field itself, or a wavefunction \(\psi(x)\) as the quantum state itself.

Orbit Theory reverses this order.

A description \(\omega\) is not the object. It is a presentation of the object. The object is the full admissibility class

\[
[\omega].
\]

Thus:

\[
\boxed{
\omega \text{ is a description; } [\omega] \text{ is the object.}
}
\]

This has several consequences.

### 5.1 No privileged representative

Unless additional structure is introduced, there is no physically privileged representative of an orbit. A gauge choice, coordinate system, basis, or frame may be pragmatically useful, but it does not select the object more truly than any other representative.

### 5.2 Object identity is relational

Two descriptions represent the same object not because they resemble one another in a bare sense, but because they are connected by an admissibility transformation.

Identity is therefore not primitive. It is generated by \(G\).

### 5.3 Objecthood is theory-relative

If the admissibility group is enlarged, formerly distinct descriptions may become descriptions of the same object. If the admissibility group is reduced, an orbit may split into several distinct objects.

Thus objecthood is relative to the relativity schema \(\mathcal R\).

---

## 6. Infinitesimal Orbit Structure

When \(G\) is a Lie group and \(\Omega\) is a smooth manifold or infinite-dimensional smooth space, the orbit structure can be studied infinitesimally.

Let

\[
\mathfrak g=\operatorname{Lie}(G).
\]

For each \(\xi\in\mathfrak g\), define the fundamental vector field

\[
\xi_\Omega(\omega)
=
\left.\frac{d}{dt}\right|_{t=0}
\exp(t\xi)\cdot\omega.
\]

The tangent space to the orbit at \(\omega\) is

\[
T_\omega(G\cdot\omega)
=
\{\xi_\Omega(\omega)\mid \xi\in\mathfrak g\}.
\]

Define the infinitesimal action map

\[
\rho_\omega:\mathfrak g\to T_\omega\Omega,
\]

\[
\rho_\omega(\xi)=\xi_\Omega(\omega).
\]

Then

\[
T_\omega(G\cdot\omega)=\operatorname{im}\rho_\omega.
\]

The stabilizer of \(\omega\) is

\[
G_\omega
=
\{g\in G\mid g\cdot\omega=\omega\}.
\]

Its Lie algebra is

\[
\mathfrak g_\omega
=
\operatorname{Lie}(G_\omega)
=
\ker\rho_\omega.
\]

Therefore

\[
\boxed{
\dim(G\cdot\omega)
=
\dim G-\dim G_\omega.
}
\]

This formula is fundamental. It says that the dimension of the descriptive redundancy at \(\omega\) is reduced by the residual symmetry of \(\omega\).

---

## 7. Stabilizers and Residual Symmetry

The stabilizer \(G_\omega\) is the subgroup of admissibility transformations that leave a particular description fixed.

Physically, \(G_\omega\) represents residual symmetry of the object as presented by \(\omega\). If \(G_\omega\) is trivial, the orbit is free at \(\omega\). If \(G_\omega\) is nontrivial, the object possesses internal or geometric symmetry.

### Proposition 7.1: Stabilizers on the same orbit are conjugate

If

\[
\omega'=g\cdot\omega,
\]

then

\[
G_{\omega'}=gG_\omega g^{-1}.
\]

**Proof.**

Let \(h\in G_{\omega'}\). Then

\[
h\cdot\omega'=\omega'.
\]

Substituting \(\omega'=g\cdot\omega\),

\[
h\cdot(g\cdot\omega)=g\cdot\omega.
\]

Using the group action property,

\[
(hg)\cdot\omega=g\cdot\omega.
\]

Acting by \(g^{-1}\),

\[
(g^{-1}hg)\cdot\omega=\omega.
\]

Thus

\[
g^{-1}hg\in G_\omega.
\]

Therefore

\[
h\in gG_\omega g^{-1}.
\]

The reverse inclusion follows identically.

\(\square\)

Thus stabilizer type is an orbit invariant, not a representative-dependent accident.

---

## 8. Orbit Types and Stratification

Let \(H\subset G\) be a subgroup. Define the orbit-type subset

\[
\Omega_{(H)}
=
\{\omega\in\Omega\mid G_\omega \text{ is conjugate to } H\}.
\]

The corresponding quotient stratum is

\[
(\Omega/G)_{(H)}
=
\Omega_{(H)}/G.
\]

The quotient space decomposes as

\[
\Omega/G
=
\bigsqcup_{(H)}
(\Omega/G)_{(H)},
\]

where the union is taken over conjugacy classes of stabilizer subgroups.

For compact Lie group actions on smooth manifolds, the orbit-type stratification is well behaved. There exists a principal orbit type \((H_{\rm princ})\) such that

\[
\Omega_{(H_{\rm princ})}
\]

is open and dense in \(\Omega\). The corresponding stratum

\[
(\Omega/G)_{(H_{\rm princ})}
\]

is the generic part of the physical object space.

Highly symmetric objects correspond to smaller orbits with larger stabilizers. They usually lie in lower-dimensional singular strata of the quotient.

### Physical interpretation

- Generic objects have principal stabilizer.
- Symmetric objects have enlarged stabilizer.
- Singular quotient points correspond not to mathematical failure but to enhanced symmetry.
- Object classification requires orbit-type data, not merely orbit points.

Thus Orbit Theory distinguishes between:

\[
\boxed{
\text{individual object} = \text{orbit}
}
\]

and

\[
\boxed{
\text{object type} = \text{orbit type or stratum}.
}
\]

---

## 9. Free Actions, Proper Actions, and Principal Bundles

If the action of \(G\) on \(\Omega\) is free, then

\[
G_\omega=\{e\}
\]

for all \(\omega\). Every orbit is diffeomorphic to \(G\):

\[
G\cdot\omega\cong G.
\]

If the action is also proper, then the quotient map

\[
I:\Omega\to\Omega/G
\]

is a principal \(G\)-bundle.

In that case, locally, one may choose a section

\[
s:U\subset\Omega/G\to\Omega.
\]

Such a section is a gauge fixing or a choice of representative. It is not the physical object. The object remains the orbit.

A global section may not exist. When it does not, one must cover \(\Omega/G\) by local gauge choices and transition functions. This is precisely the geometric situation underlying gauge theory and frame theory.

Thus even before introducing connections or curvature, Orbit Theory already contains the conceptual origin of gauge structure:

\[
\boxed{
\text{Gauge freedom is local representative choice over an orbit space.}
}
\]

---

## 10. Singular Orbits and Stacky Refinement

When the action is not free, the quotient \(\Omega/G\) may be singular. Points with nontrivial stabilizer possess residual automorphisms that the naive quotient forgets.

A refined ontological structure is given by the action groupoid

\[
\Omega//G.
\]

Its objects are points \(\omega\in\Omega\). Its morphisms are

\[
\omega\to\omega'
\]

given by elements \(g\in G\) such that

\[
\omega'=g\cdot\omega.
\]

The automorphism group of \(\omega\) in this groupoid is precisely

\[
\operatorname{Aut}(\omega)=G_\omega.
\]

The corresponding quotient stack

\[
[\Omega/G]
\]

retains stabilizer information. In many physical contexts, especially gauge theory and string theory, the stacky quotient is more faithful than the coarse orbit space.

Thus Orbit Theory admits three levels of ontological refinement:

1. **Bare orbit set:**

   \[
   \Omega/G.
   \]

2. **Stratified orbit space:**

   \[
   \Omega/G=\bigsqcup_{(H)}(\Omega/G)_{(H)}.
   \]

3. **Orbit stack:**

   \[
   [\Omega/G].
   \]

The appropriate level depends on the physical theory.

---

## 11. Orbit Theory as Ontology

Orbit Theory replaces substance ontology with equivalence-class ontology.

In classical substance ontology, one imagines an object underlying its descriptions. In Orbit Theory, the object is the equivalence class of descriptions itself.

The ontological dictionary is:

| Traditional notion | Orbit-theoretic counterpart |
|---|---|
| Object | Orbit \([\omega]\) |
| Description | Representative \(\omega\in[\omega]\) |
| Identity condition | Orbit equivalence |
| Intrinsic property | Orbit invariant |
| Symmetry of object | Stabilizer \(G_\omega\) |
| Object type | Orbit-type stratum |
| Relation between objects | Equivariant map between orbit spaces |
| State space | Quotient \(\Omega/G\) |
| Gauge choice | Local section of \(I:\Omega\to\Omega/G\) |

This is the primitive ontology of Relativity Mechanics.

---

## 12. Physical Predicates and Orbit Constancy

Although Invariant Theory is the dedicated theory of observables, Orbit Theory already determines the condition for a predicate to be physically meaningful.

A predicate \(P\) on descriptions is physically meaningful only if it is constant on orbits:

\[
P(g\cdot\omega)=P(\omega).
\]

If \(P\) is not orbit-constant, then it distinguishes between descriptions of the same object and therefore does not predicate something about the object itself.

Thus:

\[
\boxed{
\text{Physical predicates are orbit predicates.}
}
\]

Equivalently, a physically meaningful predicate descends to a predicate on \(\Omega/G\).

---

## 13. Orbit Theory in Newtonian Mechanics

Consider \(N\) Newtonian particles described in an inertial frame by trajectories

\[
\omega=\{\mathbf x_i(t)\}_{i=1}^N.
\]

The Galilei group \(G_{\rm Gal}\) acts by

\[
t'=t+s,
\]

\[
\mathbf x_i'=R\mathbf x_i+\mathbf v t+\mathbf a,
\]

where:

- \(s\) is a time translation,
- \(\mathbf a\) is a spatial translation,
- \(R\in SO(3)\) is a rotation,
- \(\mathbf v\) is a boost velocity.

The orbit of a trajectory is

\[
[\{\mathbf x_i(t)\}]_{\rm Gal}.
\]

The physical Newtonian object is not the absolute coordinate trajectory. It is the Galilean orbit of trajectories related by changes of inertial frame.

The invariant content includes relative separations

\[
\mathbf r_{ij}=\mathbf x_i-\mathbf x_j,
\]

relative velocities

\[
\dot{\mathbf r}_{ij},
\]

and relative accelerations

\[
\ddot{\mathbf r}_{ij}.
\]

Thus the Newtonian physical object is already an orbit structure, even when historically it was presented as motion in absolute space.

---

## 14. Orbit Theory in Special Relativity and Particle Classification

In special relativity, the Poincaré group acts on momentum space. For a massive particle, the mass-shell condition

\[
p^\mu p_\mu=-m^2
\]

defines an orbit of the Lorentz group in momentum space.

For \(m>0\), the orbit of a future-directed timelike momentum is determined by the invariant mass \(m\). The stabilizer of a standard momentum

\[
p^\mu=(m,0,0,0)
\]

is the rotation group \(SO(3)\). Spin arises from representations of this stabilizer.

In the coadjoint orbit formulation, one considers the dual Lie algebra \(\mathfrak s^*\) of a symmetry group \(S\). For \(\mu\in\mathfrak s^*\), the coadjoint orbit is

\[
\mathcal O_\mu
=
\{\operatorname{Ad}^*_g\mu\mid g\in S\}.
\]

The tangent space at \(\nu\in\mathcal O_\mu\) is

\[
T_\nu\mathcal O_\mu
=
\{\operatorname{ad}^*_\xi\nu\mid \xi\in\mathfrak s\}.
\]

The Kirillov symplectic form is

\[
\omega_\nu
(
\operatorname{ad}^*_\xi\nu,
\operatorname{ad}^*_\eta\nu
)
=
\nu([\xi,\eta]).
\]

Thus elementary classical systems can themselves be understood as orbits. This is a powerful confirmation of the orbit ontology: even particles are naturally classified by orbit structure.

---

## 15. Orbit Theory in General Relativity

Let \(M\) be a smooth manifold. Let

\[
\Omega_{\rm met}
=
\{g_{\mu\nu}\}
\]

be the space of Lorentzian metrics on \(M\), possibly together with matter fields.

The diffeomorphism group acts by pullback:

\[
\phi\cdot g=\phi^*g.
\]

Infinitesimally, for a vector field \(\xi^\mu\),

\[
\delta_\xi g_{\mu\nu}
=
\mathcal L_\xi g_{\mu\nu}
=
\nabla_\mu\xi_\nu+\nabla_\nu\xi_\mu.
\]

The orbit of a metric is

\[
[g_{\mu\nu}]
=
\{\phi^*g_{\mu\nu}\mid \phi\in\operatorname{Diff}(M)\}.
\]

The physical gravitational field is not the coordinate representation \(g_{\mu\nu}(x)\). It is the diffeomorphism orbit \([g_{\mu\nu}]\).

The stabilizer of a metric is its isometry group:

\[
\operatorname{Iso}(g)
=
\{\phi\in\operatorname{Diff}(M)\mid \phi^*g=g\}.
\]

Infinitesimally,

\[
\mathcal L_\xi g_{\mu\nu}=0
\]

defines Killing vector fields. Highly symmetric spacetimes, such as Minkowski, de Sitter, or Schwarzschild spacetime, have nontrivial stabilizers and therefore correspond to singular or special strata in the quotient space

\[
\operatorname{Met}(M)/\operatorname{Diff}(M).
\]

Thus general relativity is a paradigmatic orbit theory, even when formulated without explicitly using the language of Relativity Mechanics.

---

## 16. Orbit Theory in Tetrad and Frame Descriptions

In tetrad gravity, the description space includes coframe fields

\[
e^I=e^I_\mu dx^\mu
\]

and possibly spin connections

\[
\omega^{IJ}=-\omega^{JI}.
\]

The metric is an invariant of the coframe:

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

The local Lorentz group acts by

\[
e^I\mapsto \Lambda^I{}_J e^J,
\]

with

\[
\Lambda\in SO(1,3).
\]

The metric is invariant:

\[
\eta_{IJ}e'^I_\mu e'^J_\nu
=
\eta_{IJ}\Lambda^I{}_K\Lambda^J{}_L e^K_\mu e^L_\nu
=
\eta_{KL}e^K_\mu e^L_\nu.
\]

Thus the physical geometry is not a particular tetrad but the local Lorentz orbit of tetrads, further quotiented by diffeomorphisms.

The object is therefore an orbit under

\[
\operatorname{Diff}(M)\ltimes SO(1,3)_{\rm local}.
\]

This foreshadows Frame Theory, but the ontological point is already orbit-theoretic: the tetrad is a description; the orbit is the object.

---

## 17. Orbit Theory in Gauge Theory

Let \(P\to M\) be a principal \(H\)-bundle. Let

\[
\mathcal A
\]

be the space of connections on \(P\). The gauge group

\[
\mathcal G=\operatorname{Aut}(P)
\]

acts on \(\mathcal A\).

Locally, a connection is written

\[
A=A_\mu dx^\mu,
\]

with

\[
A_\mu\in\mathfrak h.
\]

An infinitesimal gauge transformation with parameter \(\alpha\in\mathfrak h\) acts as

\[
\delta_\alpha A_\mu
=
D_\mu\alpha
=
\partial_\mu\alpha+[A_\mu,\alpha],
\]

up to convention.

The curvature is

\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\nu+[A_\mu,A_\nu].
\]

More invariantly,

\[
F=dA+\frac12[A,A].
\]

The gauge orbit of a connection is

\[
[A]
=
\{A^u\mid u\in\mathcal G\}.
\]

The physical gauge field is not \(A_\mu(x)\). It is the gauge orbit \([A]\).

The stabilizer of a connection consists of gauge transformations leaving it invariant. Reducible connections have nontrivial stabilizers. The quotient

\[
\mathcal A/\mathcal G
\]

is the space of physical gauge-field configurations.

Thus Yang–Mills theory, electromagnetism, and the gauge sectors of the Standard Model are orbit theories.

---

## 18. Orbit Theory in Quantum Mechanics

Let \(\mathcal H\) be a Hilbert space. A pure quantum state is often represented by a nonzero vector

\[
|\psi\rangle\in\mathcal H.
\]

However, the phase transformation

\[
|\psi\rangle\mapsto e^{i\theta}|\psi\rangle
\]

does not change the physical state.

The admissibility group is

\[
G=U(1),
\]

or more generally \(\mathbb C^*\) if normalization is not imposed.

The orbit of \(|\psi\rangle\) is

\[
[|\psi\rangle]
=
\{e^{i\theta}|\psi\rangle\mid \theta\in\mathbb R\}.
\]

The physical pure state is the ray

\[
[\psi]\in\mathbb P(\mathcal H).
\]

Thus

\[
\mathbb P(\mathcal H)
=
(\mathcal H\setminus\{0\})/\mathbb C^*.
\]

The quantum state is therefore not a vector. It is an orbit of vectors under phase admissibility.

If basis transformations are included in the description space, then the relevant admissibility group may be enlarged to include unitary changes of basis. In that case, the physical state is the orbit of basis-dependent presentations of the same abstract state.

Thus quantum state space itself is an orbit space.

---

## 19. Orbit Theory in Quantum Gauge Systems

In quantum gauge theory, the kinematical Hilbert space \(\mathcal H_{\rm kin}\) contains states that are not gauge-invariant. The gauge group acts by unitary operators

\[
U(g):\mathcal H_{\rm kin}\to\mathcal H_{\rm kin}.
\]

The physical Hilbert space is often defined by invariance:

\[
\mathcal H_{\rm phys}
=
\{|\psi\rangle\in\mathcal H_{\rm kin}
\mid
U(g)|\psi\rangle=|\psi\rangle,\ \forall g\in G\}.
\]

Equivalently, in constraint quantization,

\[
\hat C_a|\psi_{\rm phys}\rangle=0.
\]

The physical quantum object is not a representative vector in the kinematical Hilbert space. It is an equivalence class or invariant sector under the gauge admissibility action.

Thus orbit ontology persists in quantum gauge theory.

---

## 20. Orbit Theory in String Theory

In string theory, a worldsheet description consists of:

1. a two-dimensional manifold \(\Sigma\),
2. a worldsheet metric \(h_{ab}\),
3. an embedding \(X:\Sigma\to M\).

The worldsheet diffeomorphism group acts by reparametrization:

\[
\sigma^a\mapsto f^a(\sigma).
\]

The Weyl group acts by local rescaling:

\[
h_{ab}\mapsto e^{2\omega(\sigma)}h_{ab}.
\]

The admissibility group is

\[
G_{\rm ws}
=
\operatorname{Diff}(\Sigma)\ltimes\operatorname{Weyl}(\Sigma).
\]

The physical string configuration is not a particular embedding and metric in a chosen worldsheet coordinate system. It is the orbit

\[
[X,h_{ab}]_{G_{\rm ws}}.
\]

After quotienting by diffeomorphisms and Weyl transformations, the worldsheet metric determines a point in the moduli space of Riemann surfaces.

Thus string theory is also an orbit theory, with a particularly rich admissibility group.

---

## 21. Orbit Spaces as Moduli Spaces

In many physical theories, the quotient

\[
\Omega/G
\]

is called a moduli space.

Examples include:

| Theory | \(\Omega\) | \(G\) | Quotient |
|---|---|---|---|
| Newtonian mechanics | Inertial-frame trajectories | Galilei group | Relative trajectory space |
| General relativity | Metrics | \(\operatorname{Diff}(M)\) | Superspace |
| Tetrad gravity | Coframes and connections | \(\operatorname{Diff}(M)\ltimes SO(1,3)\) | Geometrical orbit space |
| Yang–Mills theory | Connections | Gauge group | Gauge orbit space |
| Flat connections | Flat connections | Gauge group | Character variety |
| Quantum pure states | Nonzero vectors | \(U(1)\) or \(\mathbb C^*\) | Projective Hilbert space |
| String worldsheets | Metrics and embeddings | \(\operatorname{Diff}\ltimes\operatorname{Weyl}\) | Moduli of Riemann surfaces |

In each case, the moduli space is the space of physical objects or physical configurations.

---

## 22. Orbit Dimension and Descriptive Redundancy

For a Lie group action, the dimension formula

\[
\dim(G\cdot\omega)
=
\dim G-\dim G_\omega
\]

quantifies descriptive redundancy.

If \(G\) is large and \(G_\omega\) is trivial, the orbit is large. Most descriptions of the object are gauge or frame artifacts.

If \(G_\omega\) is large, the object has high symmetry and the orbit is smaller.

Thus the dimension of the orbit measures how much of the description space is occupied by redundant presentations of the same object.

The dimension of the physical object space near a generic point is

\[
\dim(\Omega/G)
=
\dim\Omega-\dim G+\dim G_\omega.
\]

For principal orbits,

\[
\dim(\Omega/G)
=
\dim\Omega-\dim G+\dim H_{\rm princ}.
\]

This is the basic dimension theory of orbit spaces.

---

## 23. Orbit Theory and Gauge Fixing

A gauge fixing is a local section

\[
s:U\subset\Omega/G\to\Omega.
\]

It chooses one representative from each orbit in a local region.

However, global gauge fixing is often impossible. In non-Abelian gauge theory, this is reflected in the Gribov ambiguity. In geometry, it corresponds to the absence of global coordinate or frame choices.

Orbit Theory gives the conceptual resolution:

\[
\boxed{
\text{Gauge fixing is a choice of local presentation, not a discovery of the object.}
}
\]

The object remains the orbit.

---

## 24. Orbit Theory and Individuation

A classical problem in metaphysics and physics is individuation: what makes an object this object?

Orbit Theory gives a mathematical answer.

An object is individuated by:

1. its orbit \([\omega]\),
2. its orbit type \((G_\omega)\),
3. its invariant relations to other orbits,
4. its position in the quotient structure \(\Omega/G\).

There is no additional hidden substrate beneath the orbit.

Thus two descriptions are not two objects if they are connected by \(G\). Conversely, two descriptions not connected by \(G\) are distinct relative to the given admissibility structure.

Individuation is therefore not absolute. It is determined by the admissibility group.

---

## 25. Enlargement and Reduction of Admissibility Groups

Orbit Theory explains how physical ontology changes when a theory is refined.

If one passes from a smaller group \(G_1\) to a larger group \(G_2\supset G_1\), then orbits merge:

\[
[\omega]_{G_1}\subseteq[\omega]_{G_2}.
\]

More descriptions become descriptions of the same object.

If one passes from a larger group to a smaller group, orbits split. Formerly identical objects become distinct because some transformations are no longer regarded as admissible.

Thus scientific progress often consists in enlarging the admissibility group:

1. From absolute position to Galilean equivalence.
2. From Galilean equivalence to Lorentz equivalence.
3. From Lorentz equivalence to diffeomorphism equivalence.
4. From global phase to local gauge equivalence.
5. From fixed background to background-independent relational descriptions.

Orbit Theory provides the mathematics of this ontological refinement.

---

## 26. Orbit Theory and Object Types

An individual object is an orbit. An object type is an orbit-type stratum.

For example:

- In general relativity, a generic geometry has no Killing vectors. Its orbit type is principal.
- A spherically symmetric spacetime has larger stabilizer and belongs to a special stratum.
- In gauge theory, irreducible connections have trivial stabilizer, while reducible connections have nontrivial stabilizer.
- In quantum theory, singlet states are invariant under the relevant symmetry group and therefore occupy special orbit types.

Thus Orbit Theory naturally distinguishes generic objects from symmetric objects without introducing separate ontological categories.

---

## 27. Orbit Theory and Relations

Relations between physical objects should also be orbit-invariant.

Suppose we have two description spaces \(\Omega_1,\Omega_2\) with admissibility groups \(G_1,G_2\). A relation between objects is represented by a map

\[
F:\Omega_1\to\Omega_2
\]

that descends to orbits.

A sufficient condition is equivariance: there exists a group homomorphism

\[
\alpha:G_1\to G_2
\]

such that

\[
F(g\cdot\omega)=\alpha(g)\cdot F(\omega).
\]

Then \(F\) induces a map

\[
\bar F:\Omega_1/G_1\to\Omega_2/G_2
\]

by

\[
\bar F([\omega])=[F(\omega)].
\]

Thus relations between objects are morphisms of orbit structures.

---

## 28. Orbit Theory and Physical Equivalence

Orbit Theory provides a precise criterion of physical equivalence:

\[
\boxed{
\omega\text{ and }\omega'
\text{ are physically equivalent}
\iff
\exists g\in G:\omega'=g\cdot\omega.
}
\]

This criterion is stronger than mere similarity. It requires an explicit admissibility transformation connecting the descriptions.

It also avoids ambiguity: if no such \(g\) exists, then within the given relativity schema the descriptions are physically distinct.

This makes physical equivalence mathematically decidable in principle, once \(\Omega\) and \(G\) are specified.

---

## 29. Orbit Theory and the Absence of Absolute Descriptions

Orbit Theory implies that no description is absolute.

A coordinate system is not absolute. A gauge is not absolute. A basis is not absolute. A phase convention is not absolute. A frame is not absolute. A parametrization is not absolute.

What remains after all admissible transformations is the orbit.

Thus Orbit Theory may be summarized by the principle:

\[
\boxed{
\text{The absolute is the orbit; the relative is the representative.}
}
\]

This is the ontological inversion at the heart of Relativity Mechanics.

---

## 30. Orbit Theory and Subsequent Relativity Mechanics

Orbit Theory is only the first part of Relativity Mechanics. It does not yet provide:

1. observables,
2. dynamics,
3. measurement,
4. information,
5. quantum structure,
6. geometry,
7. gauge interactions,
8. frame dynamics.

But it provides the necessary ontological ground for all of them.

The subsequent theories build as follows:

| Derived theory | Built upon |
|---|---|
| Invariant Theory | Functions on orbits |
| Observer Theory | Maps from orbits to observer descriptions |
| Reference Transformation Theory | Morphisms between orbit spaces |
| Constraint Mechanics | Selection of admissible orbits |
| Relativistic Dynamics | Curves in orbit spaces |
| Relativistic Information Theory | Distinguishability of orbits |
| Relativistic Quantum Theory | Hilbert-space orbit structures |
| Relativity Geometry | Geometry on orbit spaces |
| Gauge Theory of Admissibility | Local internal orbit structures |
| Frame Theory | Local spacetime frame orbits |

Thus every later theory presupposes orbit ontology.

---

## 31. Philosophical Consequences

Orbit Theory transforms several traditional concepts.

### 31.1 Object

An object is not a substance behind appearances. It is the equivalence class of admissible presentations.

### 31.2 Identity

Identity is not primitive. It is generated by admissibility equivalence.

### 31.3 Symmetry

Symmetry is not merely a property of laws. It is constitutive of objecthood.

### 31.4 Reality

Physical reality is not identified with any one representation. It is the invariant orbit structure under admissible re-description.

### 31.5 Objectivity

Objectivity is not the absence of perspective. It is invariance across admissible perspectives.

Thus Orbit Theory gives a precise mathematical form to relational philosophy.

---

## 32. Summary of the Orbit Ontology

The core definitions may be summarized as follows.

Given

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

define:

\[
\omega\sim\omega'
\iff
\exists g\in G:\omega'=g\cdot\omega.
\]

Then:

\[
[\omega]=G\cdot\omega.
\]

The physical object is:

\[
\boxed{
[\omega].
}
\]

The stabilizer is:

\[
G_\omega=\{g\in G\mid g\cdot\omega=\omega\}.
\]

The orbit tangent space is:

\[
T_\omega(G\cdot\omega)
=
\{\xi_\Omega(\omega)\mid \xi\in\mathfrak g\}.
\]

The orbit dimension is:

\[
\dim(G\cdot\omega)
=
\dim G-\dim G_\omega.
\]

The object type is determined by the conjugacy class of \(G_\omega\).

The physical object space is:

\[
\Omega/G.
\]

For singular or automorphism-rich systems, the refined object space is:

\[
[\Omega/G].
\]

---

## 33. Conclusion

Orbit Theory answers the first question any physical theory must answer:

\[
\boxed{
\text{What is a physical object?}
}
\]

Relativity Mechanics answers:

\[
\boxed{
\text{A physical object is an orbit }[\omega]=G\cdot\omega.
}
\]

This answer is not an interpretation added after the fact. It is the primitive ontology of the framework.

Individual descriptions are not objects. They are presentations. The object is the totality of admissible presentations related by the admissibility group. Stabilizers encode residual symmetry. Orbit types encode object classes. Quotient spaces encode physical state spaces. Stacky refinements encode residual automorphisms.

General relativity, gauge theory, quantum mechanics, and string theory all confirm this structure. Metrics are diffeomorphism orbits. Gauge fields are gauge orbits. Quantum states are phase or basis orbits. String worldsheets are diffeomorphism-Weyl orbits.

Everything else in Relativity Mechanics builds upon this foundation. Observables become invariants on orbits. Dynamics becomes motion on orbit spaces. Quantum theory becomes orbit structure in Hilbert space. Geometry becomes geometry of quotients. Gauge theory becomes local admissibility. Frame theory becomes local frame admissibility.

Orbit Theory is therefore not one theory among many. It is the ontological ground of Relativity Mechanics.

\[
\boxed{
\text{In Relativity Mechanics, to be physical is to be orbital.}
}
\]

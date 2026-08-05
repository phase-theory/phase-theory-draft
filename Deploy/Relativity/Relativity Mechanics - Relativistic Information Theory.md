# Relativistic Information Theory: Information as Invariant Orbit Distinguishability

## Abstract

Relativistic Information Theory is the seventh derived theory of Relativity Mechanics. It answers the primitive informational question:

\[
\boxed{
\text{What is physical information?}
}
\]

Within Relativity Mechanics, the answer is:

\[
\boxed{
\mathcal I(\Omega/G).
}
\]

Physical information is not stored in raw configurations, coordinate values, gauge representatives, basis choices, phase conventions, or frame presentations. It is stored in invariant orbit structure. Nature does not store configurations; nature stores orbit information.

Given a description space \(\Omega\), an admissibility group \(G\), and the invariant projection

\[
I:\Omega\to\Omega/G,
\]

the physical information space is the quotient

\[
Q=\Omega/G.
\]

A physical state of information is a probability measure, distinguishability structure, or quantum state on \(Q\). Self-information, entropy, relative entropy, Fisher information, mutual information, channel capacity, and records are all defined on the orbit space, not on the redundant description space.

This paper develops Relativistic Information Theory as the theory of information on admissibility quotients. We define invariant measures, orbit entropy, orbit distinguishability, observer-limited information, relational records, quantum invariant information, decoherence-free subspaces, and information channels between reference frameworks. We then show how Relativistic Information Theory provides the natural mathematical foundation for Framet Theory, in which elementary frame-like carriers store invariant relational information rather than bare frame variables.

The central principle is:

\[
\boxed{
\text{Information is invariant orbit distinguishability.}
}
\]

Equivalently:

\[
\boxed{
\text{Nature stores orbits, not representatives.}
}
\]

---

## 1. Introduction

Classical information theory usually begins with configurations: symbols, states, messages, or physical degrees of freedom. But in fundamental physics, most configurations contain redundant descriptive structure. Coordinates, gauge choices, phases, bases, reference frames, and parametrizations are not themselves physical content. They are presentations.

Relativity Mechanics identifies physical reality with orbits:

\[
[\omega]=G\cdot\omega.
\]

Orbit Theory establishes the ontology. Invariant Theory establishes what can be measured. Observer Theory establishes how observers access descriptions. Reference Transformation Theory establishes how frameworks are related.

Relativistic Information Theory now asks:

\[
\boxed{
\text{Where is physical information stored?}
}
\]

The answer is not in \(\omega\), but in

\[
[\omega].
\]

Thus information becomes a structure on the quotient:

\[
\boxed{
\mathcal I(\Omega/G).
}
\]

If two descriptions lie on the same orbit, then no physical measurement can distinguish them. Therefore they carry the same physical information. Any information assigned to the difference between them is descriptive information, not physical information.

This leads to the foundational principle of Relativistic Information Theory:

\[
\boxed{
\text{Physical information is distinguishability of admissibility orbits.}
}
\]

---

## 2. The Information Space of a Relativity Schema

A Relativity Mechanics theory is specified by

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

where

\[
I:\Omega\to\Omega/G
\]

is the invariant projection.

The physical information space is

\[
\boxed{
Q=\Omega/G.
}
\]

A point

\[
q\in Q
\]

is an orbit

\[
q=[\omega].
\]

Physical information is defined on \(Q\), not on \(\Omega\).

We therefore define the informational structure of a Relativity Mechanics theory as

\[
\boxed{
\mathcal I(Q)
=
\mathcal I(\Omega/G).
}
\]

Depending on context, \(\mathcal I(Q)\) may mean:

1. a probability measure on \(Q\),
2. an entropy functional on \(Q\),
3. a distinguishability metric on \(Q\),
4. an invariant observable algebra,
5. a quantum state space over an invariant algebra,
6. a channel or functor between orbit spaces.

The unifying idea is that information is orbit-theoretic.

---

## 3. Axioms of Relativistic Information Theory

Relativistic Information Theory is governed by the following axioms.

### Axiom I: Orbit distinguishability

Two descriptions contain the same physical information if and only if they lie on the same admissibility orbit:

\[
\omega\sim\omega'
\iff
\exists g\in G:\omega'=g\cdot\omega.
\]

Thus:

\[
\boxed{
\mathcal I(\omega)=\mathcal I(\omega')
\quad
\text{whenever}
\quad
[\omega]=[\omega'].
}
\]

### Axiom II: Information lives on the quotient

Physical information is a structure on

\[
Q=\Omega/G.
\]

It is not a structure on individual representatives.

### Axiom III: Invariant measures

Probability assignments must be invariant or descend to the quotient. If \(\mu\) is a measure on \(\Omega\), then physical probabilities are given by the pushforward

\[
\nu=I_*\mu
\]

on \(Q\).

### Axiom IV: Observational restriction

An observer can access only a subalgebra or subset of invariant information determined by its observation map.

### Axiom V: Records are stable orbits

A physical record is a stable, distinguishable orbit in a memory subsystem.

### Axiom VI: Channels are reference transformations

Information transfer between frameworks is described by maps between orbit spaces:

\[
\Phi:Q_1\to Q_2.
\]

---

## 4. Probability Measures on Orbit Spaces

Let

\[
Q=\Omega/G.
\]

A physical probability assignment is a measure

\[
\nu
\]

on \(Q\).

If \(\mu\) is a \(G\)-invariant measure on \(\Omega\), then its pushforward is defined by

\[
\boxed{
\nu(B)=\mu(I^{-1}(B))
}
\]

for every measurable set \(B\subset Q\).

Equivalently, for an invariant function \(f\),

\[
\int_\Omega f(\omega)\,d\mu(\omega)
=
\int_Q
\left(
\int_{[\omega]} f\,d\lambda_q
\right)
d\nu(q),
\]

where \(\lambda_q\) is a measure along the orbit \(q=[\omega]\).

This disintegration expresses the central informational fact:

\[
\boxed{
\text{Integration along orbits is descriptive averaging; integration over orbits is physical information.}
}
\]

---

## 5. Self-Information of an Orbit

Suppose \(Q\) is finite or discrete. Let

\[
p(q)=\nu(\{q\})
\]

be the probability of the orbit \(q\).

The self-information of the orbit is

\[
\boxed{
\mathcal I(q)
=
-\log p(q).
}
\]

If \(q=[\omega]\), we may write

\[
\boxed{
\mathcal I([\omega])
=
-\log p([\omega]).
}
\]

This is the basic unit of Relativistic Information Theory.

The information content of a description \(\omega\) is not assigned to \(\omega\) itself, but to its orbit:

\[
\boxed{
\mathcal I(\omega):=\mathcal I([\omega]).
}
\]

Thus two gauge-equivalent, coordinate-equivalent, phase-equivalent, or frame-equivalent descriptions carry identical physical information.

---

## 6. Entropy of an Orbit Space

For a discrete orbit space \(Q\), the Shannon entropy is

\[
\boxed{
H(Q)
=
-\sum_{q\in Q} p(q)\log p(q).
}
\]

For a continuous orbit space with invariant volume form \(dq\) and density \(p(q)\), the differential entropy is

\[
\boxed{
H(Q)
=
-\int_Q p(q)\log p(q)\,dq.
}
\]

This entropy measures uncertainty over physical orbits, not over redundant descriptions.

In contrast, the entropy of \(\Omega\) would include gauge, coordinate, phase, and frame redundancy. That entropy is not physical unless quotiented.

Thus:

\[
\boxed{
\text{Physical entropy is orbit entropy.}
}
\]

---

## 7. Relative Entropy and Distinguishability

Given two probability measures \(\nu_1,\nu_2\) on \(Q\), their relative entropy is

\[
\boxed{
D_{\rm KL}(\nu_1\|\nu_2)
=
\int_Q
\log\left(
\frac{d\nu_1}{d\nu_2}
\right)
d\nu_1.
}
\]

Relative entropy measures distinguishability between physical information states.

If two distributions differ only on gauge representatives but agree on \(Q\), then

\[
D_{\rm KL}=0.
\]

They are physically indistinguishable.

Thus relative entropy on \(Q\) is the natural measure of informational distance between physical states.

---

## 8. Fisher Information on the Quotient

Let \(p(q|\theta)\) be a family of probability densities on \(Q\), parameterized by physical parameters

\[
\theta=(\theta^1,\dots,\theta^n).
\]

The Fisher information metric is

\[
\boxed{
F_{ab}
=
\int_Q
p(q|\theta)
\partial_a\log p(q|\theta)
\partial_b\log p(q|\theta)
\,dq.
}
\]

This is a Riemannian metric on the physical parameter space, provided the parameters label genuine orbit distinctions.

The Fisher metric is invariant under reparametrization of \(Q\) and insensitive to representative redundancy.

Thus:

\[
\boxed{
\text{Fisher information is the infinitesimal geometry of orbit distinguishability.}
}
\]

---

## 9. Mutual Information Between Physical Variables

Let \(X:Q\to\mathcal X\) and \(Y:Q\to\mathcal Y\) be invariant random variables. That is, they factor through the quotient:

\[
X=\bar X\circ I,
\qquad
Y=\bar Y\circ I.
\]

Their joint distribution is defined on \(Q\). The mutual information is

\[
\boxed{
I(X;Y)
=
H(X)+H(Y)-H(X,Y).
}
\]

Equivalently,

\[
I(X;Y)
=
D_{\rm KL}(p_{XY}\|p_Xp_Y).
\]

This measures invariant correlation between physical observables.

If \(X\) or \(Y\) depends on gauge or frame representatives, it is not a physical random variable and its mutual information is not physically meaningful until quotiented.

---

## 10. Observer-Limited Information

An observer is a map

\[
O:\Omega\to D_O.
\]

If \(O\) is admissible, it descends to

\[
\bar O:Q\to D_O/\rho(G).
\]

The observer accesses only the subalgebra

\[
\mathcal A_O
=
O^*\bigl(C^\infty(D_O)^{\rho(G)}\bigr)
\subset
C^\infty(Q).
\]

Thus the observer’s accessible information is generally less than the full information on \(Q\).

Let \(X\) be a physical random variable on \(Q\). The observer-limited information is the information contained in the observable subalgebra \(\mathcal A_O\). In probabilistic terms, it is the entropy of the coarse-grained variable

\[
X_O=\bar X\circ\bar O.
\]

The information loss due to observational restriction is

\[
\boxed{
\Delta H_O
=
H(X)-H(X_O).
}
\]

This is not gauge redundancy. It is genuine observer limitation.

Thus Relativistic Information Theory distinguishes:

1. descriptive redundancy,
2. physical information,
3. observer-accessible information.

---

## 11. Information Channels as Reference Transformations

A communication channel between physical frameworks is a reference transformation

\[
\Phi:Q_1\to Q_2.
\]

If the channel is deterministic and noiseless, an input orbit \(q_1\in Q_1\) is mapped to

\[
q_2=\Phi(q_1).
\]

If the channel is stochastic, it is a Markov kernel

\[
K(q_1,dq_2).
\]

For an input distribution \(\nu_1\) on \(Q_1\), the output distribution is

\[
\nu_2(dq_2)
=
\int_{Q_1} K(q_1,dq_2)\,d\nu_1(q_1).
\]

The mutual information between input and output is

\[
I(Q_1;Q_2).
\]

The channel capacity is

\[
\boxed{
C(\Phi)
=
\sup_{\nu_1} I(Q_1;Q_2).
}
\]

Thus information transmission between frameworks is governed by Reference Transformation Theory.

---

## 12. Dynamics and Information Conservation

Let physical dynamics be a flow on the quotient:

\[
\varphi_t:Q\to Q.
\]

If \(\varphi_t\) preserves the physical measure \(\nu\), then

\[
(\varphi_t)_*\nu=\nu.
\]

In that case, the entropy is conserved:

\[
H(\nu_t)=H(\nu).
\]

More generally, if the flow is measure-preserving but mixing, fine-grained entropy is conserved while coarse-grained entropy may increase.

Thus information conservation is not defined on raw configuration space. It is defined on the orbit space.

\[
\boxed{
\text{Physical information conservation is measure preservation on } \Omega/G.
}
\]

---

## 13. Constraint Reduction and Information

In constrained systems, the admissible state space is

\[
\Sigma\subset\Omega,
\]

defined by constraints

\[
C_a(\omega)=0.
\]

The physical space is

\[
Q_{\rm phys}
=
\Sigma/G_C,
\]

where \(G_C\) is the group generated by first-class constraints.

Physical information lives on

\[
\boxed{
Q_{\rm phys}.
}
\]

The Liouville or path-integral measure must be reduced to \(Q_{\rm phys}\). In gauge theory, this produces Faddeev–Popov determinants, BRST measures, or symplectic reduction.

Gauge degrees of freedom do not contribute physical entropy. They are quotiented out.

Thus:

\[
\boxed{
\text{Constraint reduction removes non-physical information.}
}
\]

---

## 14. Quantum Relativistic Information Theory

In quantum theory, information is encoded in states and operator algebras.

Let \(\mathcal A\) be the algebra of quantum observables and let \(G\) act by automorphisms

\[
\alpha_g:\mathcal A\to\mathcal A.
\]

The physical observable algebra is

\[
\boxed{
\mathcal A_{\rm phys}
=
\mathcal A^G.
}
\]

A quantum information state is a positive normalized functional on \(\mathcal A_{\rm phys}\), or equivalently a density matrix restricted to the invariant algebra.

If the action is implemented unitarily on a Hilbert space \(\mathcal H\),

\[
\alpha_g(A)=U(g)AU(g)^\dagger,
\]

then physical density matrices are considered modulo

\[
\rho\sim U(g)\rho U(g)^\dagger.
\]

The von Neumann entropy

\[
\boxed{
S(\rho)
=
-\operatorname{Tr}(\rho\log\rho)
}
\]

is invariant under admissibility transformations:

\[
S(U(g)\rho U(g)^\dagger)=S(\rho).
\]

Thus quantum information is also orbit information.

---

## 15. Quantum Orbit Spaces

For pure quantum states, the description space is

\[
\mathcal H\setminus\{0\}.
\]

Phase admissibility gives

\[
Q_{\rm pure}
=
\mathbb P(\mathcal H).
\]

If an additional admissibility group \(G\) acts, the physical quantum state space is

\[
\boxed{
Q_{\rm quantum}
=
\mathbb P(\mathcal H)/G.
}
\]

Quantum information is then defined on this quotient.

For gauge theories, one often imposes constraints:

\[
\hat C_a|\Psi_{\rm phys}\rangle=0.
\]

The physical Hilbert space is

\[
\mathcal H_{\rm phys}
=
\mathcal H^G
\]

or the BRST cohomology.

Quantum information is stored in \(\mathcal H_{\rm phys}\), not in the kinematical Hilbert space.

---

## 16. Decoherence-Free Subspaces and Logical Information

Suppose \(G\) acts unitarily on \(\mathcal H\). For compact \(G\), one has a decomposition

\[
\boxed{
\mathcal H
\cong
\bigoplus_\lambda
\mathcal H_\lambda\otimes \mathcal M_\lambda,
}
\]

where

\[
U(g)
=
\bigoplus_\lambda
\rho_\lambda(g)\otimes \mathbf 1_{\mathcal M_\lambda}.
\]

The group acts nontrivially on \(\mathcal H_\lambda\) but trivially on \(\mathcal M_\lambda\).

Therefore the multiplicity spaces \(\mathcal M_\lambda\) are protected from noise that couples only through \(G\).

Logical quantum information may be stored in these multiplicity spaces:

\[
\boxed{
\text{Logical qubits live in invariant multiplicity sectors.}
}
\]

Singlet states correspond to trivial representations:

\[
\rho_\lambda(g)=1.
\]

They are fully invariant.

Thus decoherence-free subspaces, noiseless subsystems, and gauge-invariant quantum memories are natural consequences of Relativistic Information Theory.

---

## 17. Quantum Channels and Equivariance

A quantum channel between admissibility frameworks should respect the admissibility structure.

Let

\[
\mathcal E:\mathcal A_1\to\mathcal A_2
\]

be a completely positive trace-preserving map. It is admissible if

\[
\boxed{
\mathcal E\circ\alpha_g^{(1)}
=
\alpha_{\alpha(g)}^{(2)}
\circ\mathcal E.
}
\]

If the channel maps physical algebras to physical algebras, then it defines a channel between orbit information spaces.

Its capacity must be computed using only invariant inputs and outputs.

Thus quantum information theory becomes relational: channels transmit orbit information, not gauge representatives.

---

## 18. Information in Newtonian Mechanics

In Newtonian mechanics, the admissibility group is the Galilei group. Absolute position, absolute orientation, absolute uniform velocity, and absolute time origin are not physical information.

The physical information is carried by relative quantities:

\[
\mathbf r_{ij}
=
\mathbf x_i-\mathbf x_j,
\]

\[
\dot{\mathbf r}_{ij},
\]

\[
m_i/m_j,
\]

\[
\Delta t.
\]

A probability distribution over Galilean orbits defines Newtonian physical information.

Thus Newtonian information is not the full configuration entropy of particle positions. It is the entropy of relative configurations modulo Galilean transformations.

---

## 19. Information in General Relativity

In general relativity, the admissibility group includes diffeomorphisms:

\[
G_{\rm GR}
=
\operatorname{Diff}(M).
\]

Coordinate information is not physical. The physical information space is

\[
\operatorname{Met}(M)/\operatorname{Diff}(M),
\]

possibly including matter fields.

Physical information is encoded in diffeomorphism-invariant relational observables such as

\[
\mathcal O_{\phi,T}(\tau)
=
\phi\big|_{T=\tau}.
\]

Local coordinate values carry no physical information. Relational correlations carry physical information.

Black hole entropy, holographic bounds, and gravitational entropy must therefore be interpreted as measures on diffeomorphism-invariant orbit spaces, not as counts of coordinate configurations.

Thus:

\[
\boxed{
\text{Gravitational information is relational orbit information.}
}
\]

---

## 20. Information in Gauge Theory

In gauge theory, the physical quotient is

\[
\mathcal A/\mathcal G.
\]

Gauge potentials \(A_\mu\) are not physical information carriers by themselves. Physical information is stored in gauge-invariant structures such as:

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}),
\]

\[
\operatorname{tr}(F\wedge F),
\]

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

Color-charged states that are not gauge singlets are not physical information carriers in the asymptotic spectrum. Physical information is carried by gauge-invariant states: mesons, baryons, glueballs, and Wilson-loop correlations.

Thus:

\[
\boxed{
\text{Gauge information is singlet information.}
}
\]

---

## 21. Information in Quantum Mechanics

In ordinary quantum mechanics, global phase carries no information. Basis choice carries no information. The physical pure-state space is

\[
\mathbb P(\mathcal H).
\]

The information content of a pure state is defined on the ray:

\[
[\psi].
\]

Probabilities

\[
p(a)=\operatorname{Tr}(\rho P_a)
\]

are invariant under admissible transformations.

The eigenvalues of \(\rho\) are invariant information. The von Neumann entropy

\[
S(\rho)
\]

is invariant under unitary basis changes.

Thus quantum information is already orbit information, even before gauge or gravitational admissibility is considered.

---

## 22. Information in String Theory

In string theory, the worldsheet admissibility group includes

\[
\operatorname{Diff}(\Sigma)\ltimes\operatorname{Weyl}(\Sigma).
\]

Physical string information is not stored in a particular worldsheet coordinate system or metric representative. It is stored in the quotient by diffeomorphisms and Weyl transformations.

The physical data include:

1. conformal structure,
2. moduli,
3. BRST cohomology classes,
4. vertex-operator correlations,
5. duality-invariant background data.

String dualities further identify apparently distinct backgrounds. From the perspective of Relativistic Information Theory, dualities enlarge the admissibility equivalence relation, thereby merging information spaces that were previously thought distinct.

Thus:

\[
\boxed{
\text{Duality identifies information spaces.}
}
\]

---

## 23. Physical Records and Memory

A memory is a physical subsystem whose states can store distinguishable orbits.

Let \(M\) be a memory description space. Its physical memory space is

\[
Q_M=M/G_M.
\]

Writing information corresponds to selecting an orbit

\[
q\in Q_M.
\]

Reading information corresponds to an observer map

\[
O_M:M\to D_O
\]

that reports the orbit or a coarse-grained invariant of it.

The storage capacity of a finite memory is

\[
\boxed{
C_M=\log |Q_M|.
}
\]

For continuous memory spaces, capacity is defined relative to a measure and resolution.

Crucially, gauge or coordinate degrees of freedom inside the memory do not increase capacity. They are descriptive redundancy.

Thus:

\[
\boxed{
\text{Memory stores orbits, not configurations.}
}
\]

---

## 24. Erasure, Redundancy, and Thermodynamics

Erasing gauge redundancy costs no physical information, because gauge redundancy was not physical information to begin with.

Erasing an invariant record, however, changes the orbit state of a memory and therefore has physical thermodynamic consequences.

In Landauer-like terms, the minimal thermodynamic cost is associated with loss of distinguishable orbit states, not with loss of representative detail.

Thus Relativistic Information Theory refines the notion of information erasure:

\[
\boxed{
\text{Only orbit distinguishability is thermodynamically physical.}
}
\]

---

## 25. Framet Theory and Orbit Information

Relativistic Information Theory connects naturally to Framet Theory.

A framet is an elementary frame-like carrier of relational information. Instead of storing a bare frame variable, a framet stores an orbit of frame descriptions.

Let \(\Gamma=(V,E)\) be a relational graph or discrete substrate. Assign to each edge \(e\in E\) a frame-transition element

\[
h_e\in G,
\]

where \(G\) is the relevant frame or gauge group.

The Framet configuration space is

\[
\Omega_{\rm Fr}
=
G^E.
\]

Local frame admissibility transformations are given by

\[
k_v\in G
\]

at each vertex \(v\in V\). They act by

\[
h_e
\mapsto
k_{s(e)}h_e k_{t(e)}^{-1},
\]

where \(s(e)\) and \(t(e)\) are the source and target vertices of \(e\).

The Framet admissibility group is therefore

\[
\mathcal G_{\rm Fr}
=
G^V.
\]

The physical Framet information space is

\[
\boxed{
Q_{\rm Fr}
=
G^E/G^V.
}
\]

A framet does not store \(h_e\) itself. It stores the orbit

\[
[h_e]\in Q_{\rm Fr}.
\]

Thus Framet Theory is a discrete realization of Relativistic Information Theory.

---

## 26. Framet Information

For a finite Framet system with finite group \(G\), the number of physical Framet orbits is finite. The maximal Framet information capacity is

\[
\boxed{
C_{\rm Fr}
=
\log |Q_{\rm Fr}|.
}
\]

If a probability distribution \(p(q)\) is assigned to Framet orbits \(q\in Q_{\rm Fr}\), the Framet entropy is

\[
\boxed{
H_{\rm Fr}
=
-\sum_{q\in Q_{\rm Fr}}p(q)\log p(q).
}
\]

The self-information of a Framet orbit is

\[
\boxed{
\mathcal I_{\rm Fr}(q)
=
-\log p(q).
}
\]

Thus the elementary informational unit in Framet Theory is not a frame variable but a distinguishable frame orbit.

---

## 27. Framet Holonomies as Information Carriers

The fundamental gauge-invariant Framet observables are loop holonomies.

For a closed loop \(\gamma\) in \(\Gamma\), the holonomy is

\[
H_\gamma
=
\prod_{e\in\gamma}h_e.
\]

Under local frame transformations, \(H_\gamma\) transforms by conjugation:

\[
H_\gamma
\mapsto
k_v H_\gamma k_v^{-1}.
\]

Therefore its conjugacy class is invariant.

A natural Framet observable is

\[
\boxed{
W_R(\gamma)
=
\operatorname{Tr}_R(H_\gamma).
}
\]

These loop invariants store physical Framet information.

In the continuum limit, Framet holonomies become gauge or frame holonomies, and Framet information becomes the invariant information of connections and curvature.

---

## 28. Framet Dynamics as Information Geometry

A Framet dynamics may be defined by an invariant action on orbit space. For example, a plaquette action may be written as

\[
S_{\rm Fr}
=
\sum_{p}
f\bigl(H_p\bigr),
\]

where \(p\) labels closed plaquettes and \(H_p\) is the plaquette holonomy.

A Gibbs measure on Framet orbits is then

\[
p(q)
\propto
e^{-S_{\rm Fr}(q)}.
\]

The corresponding information is

\[
\mathcal I_{\rm Fr}(q)
=
S_{\rm Fr}(q)
+
\log Z.
\]

Thus Framet dynamics may be interpreted as the statistical geometry of orbit information.

In the continuum limit, this approaches Yang–Mills or frame-gravity measures on quotient spaces.

---

## 29. Framets, Frames, and Relational Memory

Framet Theory suggests that elementary physical memory is frame-orbit memory.

A framet remembers not an absolute orientation, but a relational orientation. It stores not a coordinate, but a relation. It carries not a gauge potential, but an invariant holonomy or orbit class.

Thus Framet Theory realizes the principle:

\[
\boxed{
\text{Nature stores relational frame orbits, not frame variables.}
}
\]

This is precisely Relativistic Information Theory applied to discrete frame structures.

---

## 30. Information and the Hierarchy of Relativity Mechanics

Relativistic Information Theory integrates with the other derived theories of Relativity Mechanics.

### 30.1 Orbit Theory

Orbit Theory provides the objects of information:

\[
q=[\omega].
\]

### 30.2 Invariant Theory

Invariant Theory provides the measurable distinctions:

\[
f(q).
\]

### 30.3 Observer Theory

Observer Theory provides access channels:

\[
O:\Omega\to D_O.
\]

### 30.4 Reference Transformation Theory

Reference Transformation Theory provides information channels between frameworks:

\[
\Phi:Q_1\to Q_2.
\]

### 30.5 Constraint Mechanics

Constraint Mechanics provides the admissible orbit space:

\[
Q_{\rm phys}=\Sigma/G_C.
\]

### 30.6 Relativistic Dynamics

Relativistic Dynamics provides flows on \(Q\), governing information evolution.

### 30.7 Relativistic Quantum Theory

Relativistic Quantum Theory provides invariant operator algebras and quantum orbit states.

### 30.8 Relativity Geometry

Relativity Geometry provides information metrics, symplectic measures, and curvature on quotient spaces.

### 30.9 Gauge Theory of Admissibility

Gauge Theory provides internal orbit information and singlet constraints.

### 30.10 Frame Theory and Framet Theory

Frame Theory provides continuum frame orbits. Framet Theory provides discrete frame-orbit carriers.

Thus Relativistic Information Theory is the informational layer of the entire architecture.

---

## 31. The Core Formal Structure

The essential definitions may be summarized as follows.

Given

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

the physical information space is

\[
\boxed{
Q=\Omega/G.
}
\]

A physical probability state is a measure

\[
\boxed{
\nu\in\operatorname{Prob}(Q).
}
\]

The self-information of an orbit is

\[
\boxed{
\mathcal I(q)=-\log \nu(q)
}
\]

in the discrete case, or

\[
\boxed{
\mathcal I(q)=-\log p(q)
}
\]

in the continuous case.

The entropy is

\[
\boxed{
H(Q)=-\int_Q p(q)\log p(q)\,dq.
}
\]

Distinguishability is measured by relative entropy,

\[
\boxed{
D_{\rm KL}(\nu_1\|\nu_2),
}
\]

or by Fisher information,

\[
\boxed{
F_{ab}
=
\int_Q
p\,\partial_a\log p\,\partial_b\log p\,dq.
}
\]

Observer-accessible information is determined by

\[
\boxed{
\mathcal A_O
=
O^*\bigl(C^\infty(D_O)^{\rho(G)}\bigr).
}
\]

Quantum information is defined on

\[
\boxed{
\mathcal A_{\rm phys}
=
\mathcal A^G.
}
\]

Framet information is defined on

\[
\boxed{
Q_{\rm Fr}
=
G^E/G^V.
}
\]

In all cases:

\[
\boxed{
\mathcal I=\mathcal I(\Omega/G).
}
\]

---

## 32. Conclusion

Relativistic Information Theory answers the primitive question:

\[
\boxed{
\text{What is physical information?}
}
\]

The answer is:

\[
\boxed{
\text{Physical information is invariant orbit distinguishability.}
}
\]

Information is not stored in configurations, coordinates, gauge representatives, phases, bases, or frame variables. It is stored in orbits.

The informational structure of a physical theory is therefore

\[
\boxed{
\mathcal I(\Omega/G).
}
\]

Probabilities, entropy, relative entropy, Fisher information, mutual information, records, memories, channels, and quantum information are all defined on the quotient space of admissibility orbits.

This principle reshapes the interpretation of physical information:

\[
\boxed{
\text{Nature stores orbit information, not configuration information.}
}
\]

Framet Theory follows naturally from this insight. Framets are elementary carriers of frame-orbit information. Their physical states are not frame variables but frame orbits. Their observables are invariant holonomies and relational frame correlations. In the continuum limit, they recover the invariant information structures of gauge theory and frame gravity.

Thus Relativistic Information Theory provides both the informational foundation of Relativity Mechanics and the mathematical bridge to Framet Theory.

# Relativistic Quantum Theory: Quantum States as Admissibility Orbits and the Emergence of Logical Qubits, Decoherence-Free Subspaces, Singlets, and Framets

## Abstract

Relativistic Quantum Theory is the quantum specialization of Relativity Mechanics. It answers the primitive question:

\[
\boxed{
\text{What is a quantum state when descriptions are relational?}
}
\]

The answer is:

\[
\boxed{
|\psi\rangle/G.
}
\]

A quantum state is not a vector in Hilbert space taken literally. It is an equivalence class of Hilbert-space descriptions under admissibility transformations: phase conventions, basis choices, reference frames, gauge frames, and quantum reference systems. When a Hilbert space \(\mathcal H\) carries a projective unitary representation of an admissibility group \(G\), the physical pure-state space is the projective quotient

\[
\boxed{
\mathcal Q_{\rm RQT}
=
\mathbb P(\mathcal H)/G.
}
\]

For gauge theories and quantum reference frames, the perspective-neutral formulation requires physical states to be invariant under a diagonal admissibility action. Relative states, obtained by conditioning on a reference system, transform covariantly and therefore appear as \(G\)-orbits. This single structure unifies quantum reference frames with gauge symmetry.

Representation theory then explains the emergence of protected quantum information. For compact \(G\), the Hilbert space decomposes as

\[
\mathcal H
\cong
\bigoplus_\lambda
\mathcal V_\lambda\otimes\mathcal M_\lambda,
\]

where \(G\) acts nontrivially on \(\mathcal V_\lambda\) and trivially on \(\mathcal M_\lambda\). The multiplicity spaces \(\mathcal M_\lambda\) are natural decoherence-free subsystems. Logical qubits may be encoded in them. Singlet states correspond to trivial representations. In discrete frame theories, the same structure produces framets: elementary quantum frame tokens whose physical states are spin-network-like invariant orbits.

Thus Relativistic Quantum Theory unifies quantum states, quantum reference frames, gauge constraints, logical qubits, decoherence-free subspaces, singlets, and framets under one principle:

\[
\boxed{
\text{Quantum reality is represented by admissibility orbits, not by bare Hilbert-space vectors.}
}
\]

---

## 1. Introduction

Quantum theory is already relational at the level of description. A state vector depends on:

1. a global phase convention,
2. a basis choice,
3. a reference frame,
4. a gauge trivialization,
5. a clock or reference system,
6. a coordinate or internal frame.

None of these choices is physically absolute. The physical content of a quantum state is what remains after all admissible re-descriptions have been quotiented out.

Relativistic Quantum Theory formalizes this by applying the relativity schema to quantum Hilbert spaces.

Let \(\mathcal H\) be a Hilbert space. Let \(G\) be an admissibility group represented projectively by unitary operators:

\[
U:G\to PU(\mathcal H).
\]

Equivalently, up to phases,

\[
U(g)U(h)=e^{i\alpha(g,h)}U(gh).
\]

A quantum description is a nonzero vector

\[
|\psi\rangle\in\mathcal H.
\]

The admissibility group acts by

\[
|\psi\rangle\mapsto U(g)|\psi\rangle.
\]

The physical quantum state is not \(|\psi\rangle\). It is the orbit

\[
\boxed{
[|\psi\rangle]_G
=
\{e^{i\theta}U(g)|\psi\rangle
\mid
g\in G,\ \theta\in\mathbb R
\}.
}
\]

Thus the physical pure-state space is

\[
\boxed{
\mathcal Q_{\rm RQT}
=
\mathbb P(\mathcal H)/G.
}
\]

This is the quantum orbit principle.

---

## 2. The Relativity Schema of Relativistic Quantum Theory

Relativistic Quantum Theory is specified by the schema

\[
\boxed{
\mathcal R_{\rm RQT}
=
(\Omega_{\rm RQT},G,\triangleright,I_{\rm RQT}).
}
\]

The ingredients are:

1. **Description space:**

   \[
   \Omega_{\rm RQT}
   =
   \mathcal H\setminus\{0\},
   \]

   or, for mixed states, the space of density operators \(\mathcal D(\mathcal H)\).

2. **Admissibility group:**

   \[
   G,
   \]

   represented projectively or unitarily on \(\mathcal H\).

3. **Action:**

   \[
   |\psi\rangle\mapsto U(g)|\psi\rangle.
   \]

4. **Invariant projection:**

   \[
   I_{\rm RQT}(|\psi\rangle)
   =
   [|\psi\rangle]_G.
   \]

For mixed states,

\[
\rho\mapsto U(g)\rho U(g)^\dagger,
\]

and the physical mixed-state space is

\[
\mathcal D(\mathcal H)/G.
\]

---

## 3. Quantum Observables as Invariant Operators

A quantum observable is physically meaningful only if it is invariant under admissibility transformations.

Let \(\mathcal B(\mathcal H)\) be the algebra of bounded operators. The admissibility action on operators is

\[
A\mapsto U(g)AU(g)^\dagger.
\]

The physical observable algebra is the invariant subalgebra:

\[
\boxed{
\mathcal A_{\rm phys}
=
\mathcal B(\mathcal H)^G
=
\{
A\in\mathcal B(\mathcal H)
\mid
U(g)AU(g)^\dagger=A,\ \forall g\in G
\}.
}
\]

Equivalently, for the Lie algebra generators \(\hat Q_a\),

\[
\boxed{
[A,\hat Q_a]=0.
}
\]

Expectation values of invariant operators are orbit-independent:

\[
\langle A\rangle_{U(g)\psi}
=
\langle\psi|U(g)^\dagger A U(g)|\psi\rangle
=
\langle\psi|A|\psi\rangle.
\]

Thus measurable quantum facts are invariant orbital facts.

---

## 4. Descent of Quantum Dynamics

Let the kinematical Schrödinger equation be

\[
i\hbar\frac{d}{dt}|\psi(t)\rangle
=
\hat H|\psi(t)\rangle.
\]

The Hamiltonian flow is

\[
|\psi(t)\rangle
=
e^{-i\hat H t/\hbar}|\psi(0)\rangle.
\]

For the dynamics to be physically well defined on the quotient \(\mathbb P(\mathcal H)/G\), it must commute with the admissibility action:

\[
U(g)e^{-i\hat H t/\hbar}
=
e^{-i\hat H t/\hbar}U(g).
\]

This holds if

\[
\boxed{
[\hat H,U(g)]=0,
\qquad
\forall g\in G.
}
\]

Infinitesimally,

\[
\boxed{
[\hat H,\hat Q_a]=0.
}
\]

Then the Hamiltonian vector field on projective Hilbert space descends to the quotient.

The projective space \(\mathbb P(\mathcal H)\) carries the Fubini–Study symplectic form \(\omega_{\rm FS}\). The expectation value

\[
h([\psi])
=
\frac{\langle\psi|\hat H|\psi\rangle}{\langle\psi|\psi\rangle}
\]

generates a Hamiltonian flow on \(\mathbb P(\mathcal H)\). If \(\hat H\) is \(G\)-invariant, this flow descends to

\[
\mathbb P(\mathcal H)/G.
\]

Thus:

\[
\boxed{
\text{Quantum evolution is a flow on the space of quantum admissibility orbits.}
}
\]

---

## 5. Gauge Symmetry and the Physical Hilbert Space

In gauge theories, \(G\) is a local admissibility group. Physical states must be invariant under gauge transformations.

Let the gauge group be

\[
\mathcal G=C^\infty(M,G).
\]

The kinematical Hilbert space \(\mathcal H_{\rm kin}\) carries a unitary representation \(U(\mathcal G)\). The Gauss constraints are the generators

\[
\hat{\mathcal G}_a(x).
\]

Dirac quantization imposes

\[
\boxed{
\hat{\mathcal G}_a(x)|\Psi_{\rm phys}\rangle=0.
}
\]

Equivalently,

\[
\boxed{
U(g)|\Psi_{\rm phys}\rangle
=
|\Psi_{\rm phys}\rangle,
\qquad
\forall g\in\mathcal G.
}
\]

The physical Hilbert space is the invariant subspace:

\[
\boxed{
\mathcal H_{\rm phys}
=
\mathcal H_{\rm kin}^{\mathcal G}.
}
\]

For compact gauge groups, the projector onto the physical subspace is the group average:

\[
\boxed{
P_{\mathcal G}
=
\int_{\mathcal G}\mathcal Dg\,U(g).
}
\]

Then

\[
\mathcal H_{\rm phys}
=
P_{\mathcal G}\mathcal H_{\rm kin}.
\]

For open or anomalous gauge theories, one uses BRST cohomology. The BRST charge \(Q_{\rm BRST}\) satisfies

\[
Q_{\rm BRST}^2=0,
\]

and

\[
\boxed{
\mathcal H_{\rm phys}
=
H^\bullet(Q_{\rm BRST}).
}
\]

Thus gauge-invariant quantum states are singlets of the local admissibility group.

---

## 6. Relative Quantum States and the Orbit Principle

There are two equivalent presentations of Relativistic Quantum Theory.

### 6.1 Perspective-neutral presentation

The total physical state is invariant:

\[
U(g)|\Psi_{\rm phys}\rangle=|\Psi_{\rm phys}\rangle.
\]

This is the gauge-invariant or reference-neutral description.

### 6.2 Frame-relative presentation

A relative description is obtained by conditioning the total invariant state on a reference system. The resulting relative state transforms covariantly:

\[
|\psi(g)\rangle
\mapsto
U(h)|\psi(h^{-1}g)\rangle.
\]

Thus relative descriptions form orbits:

\[
\boxed{
|\psi\rangle/G.
}
\]

The two presentations are related by conditioning and dressing. The invariant total state contains all frame-relative orbits without privileging any one frame.

This is the key unification:

\[
\boxed{
\text{Gauge invariance is perspective-neutral; relative frames are orbital.}
}
\]

---

## 7. Quantum Reference Frames

A quantum reference frame is a physical system used to define relational descriptions.

Let

\[
\mathcal H_{\rm tot}
=
\mathcal H_S\otimes\mathcal H_R,
\]

where \(S\) is the system and \(R\) is the reference system.

Suppose \(G\) acts diagonally:

\[
U_{\rm tot}(g)
=
U_S(g)\otimes U_R(g).
\]

A physical state satisfies

\[
\boxed{
U_S(g)\otimes U_R(g)|\Psi\rangle
=
|\Psi\rangle.
}
\]

This is the quantum relational constraint.

If the reference system has a covariant basis \(\{|g\rangle_R\}\), one may condition on the reference reading \(g\):

\[
|\psi_S(g)\rangle
=
{}_R\langle g|\Psi\rangle.
\]

The conditional state transforms as

\[
|\psi_S(g)\rangle
\mapsto
U_S(h)|\psi_S(h^{-1}g)\rangle.
\]

Therefore the relative state of \(S\) with respect to \(R\) is not a bare vector. It is a \(G\)-orbit of vectors.

Thus:

\[
\boxed{
\text{Quantum reference frames produce orbit-valued relative states.}
}
\]

Changing the quantum reference frame is a Reference Transformation between quotient descriptions.

---

## 8. Quantum Reference Frames and Gauge Symmetry Unified

Quantum reference frames and gauge symmetry have the same mathematical structure.

In a gauge theory, the gauge frame is an internal reference system. A local gauge transformation changes the internal frame. A gauge-invariant state is perspective-neutral. A gauge-covariant field is a frame-relative description.

Let \(\psi(x)\) be a matter field transforming under a local gauge transformation \(u(x)\) as

\[
\psi(x)\mapsto u(x)\psi(x).
\]

A dressed or relational field may be constructed by attaching a Wilson line or gauge frame:

\[
\psi_{\rm dressed}(x)
=
W(x,x_0)\psi(x),
\]

where

\[
W(x,x_0)
=
\mathcal P
\exp
\left(
\int_{x_0}^x A
\right).
\]

Under a gauge transformation, the dressing transforms oppositely, making suitable combinations invariant.

This is exactly analogous to constructing relational observables using a quantum reference frame.

Thus:

\[
\boxed{
\text{Gauge frames and quantum reference frames are both admissibility frames.}
}
\]

The unifying structure is:

\[
\boxed{
\text{Total invariant state }+\text{ conditional relative orbits}.
}
\]

---

## 9. Representation Theory and the Emergence of Protected Quantum Information

For compact \(G\), the Hilbert space decomposes into irreducible representations:

\[
\boxed{
\mathcal H
\cong
\bigoplus_\lambda
\mathcal V_\lambda\otimes\mathcal M_\lambda.
}
\]

The admissibility group acts as

\[
U(g)
=
\bigoplus_\lambda
\rho_\lambda(g)\otimes \mathbf 1_{\mathcal M_\lambda}.
\]

Here:

- \(\mathcal V_\lambda\) carries the representation \(\rho_\lambda\),
- \(\mathcal M_\lambda\) is the multiplicity space,
- \(G\) acts trivially on \(\mathcal M_\lambda\).

This decomposition is the mathematical origin of singlets, logical qubits, and decoherence-free subspaces.

---

## 10. Singlets

A singlet is a state transforming in the trivial representation:

\[
U(g)|\Psi_{\rm singlet}\rangle
=
|\Psi_{\rm singlet}\rangle.
\]

Singlets live in the trivial-representation sector:

\[
\mathcal H_{\lambda=0}.
\]

They are invariant under the full admissibility group.

### Example: Two spin-\(\frac12\) particles

For \(G=SU(2)\),

\[
\frac12\otimes\frac12
=
0\oplus1.
\]

The singlet is

\[
\boxed{
|\Psi^-\rangle
=
\frac{1}{\sqrt2}
\left(
|\uparrow\downarrow\rangle
-
|\downarrow\uparrow\rangle
\right).
}
\]

It satisfies

\[
\left(
\vec J_1+\vec J_2
\right)|\Psi^-\rangle=0.
\]

Thus it is invariant under collective rotations.

Singlets are the simplest gauge-invariant or frame-independent quantum states.

---

## 11. Logical Qubits from Multiplicity Spaces

Logical quantum information can be stored in the multiplicity spaces \(\mathcal M_\lambda\).

Choose a representation sector \(\lambda\) with

\[
\dim\mathcal M_\lambda\geq2.
\]

Select a fiducial vector \(|v_0\rangle\in\mathcal V_\lambda\). Encode logical basis states as

\[
|0_L\rangle
=
|v_0\rangle\otimes|m_0\rangle,
\]

\[
|1_L\rangle
=
|v_0\rangle\otimes|m_1\rangle,
\]

where \(|m_0\rangle,|m_1\rangle\in\mathcal M_\lambda\).

Under \(G\),

\[
U(g)(|v_0\rangle\otimes|m\rangle)
=
(\rho_\lambda(g)|v_0\rangle)\otimes|m\rangle.
\]

The logical label \(|m\rangle\) is unaffected.

Thus:

\[
\boxed{
\text{Logical qubits live in admissibility multiplicity spaces.}
}
\]

---

## 12. Decoherence-Free Subspaces and Noiseless Subsystems

Suppose environmental noise couples only through the admissibility group \(G\). The noise algebra is generated by operators of the form

\[
U(g),\qquad g\in G.
\]

In the representation decomposition,

\[
U(g)=\bigoplus_\lambda\rho_\lambda(g)\otimes\mathbf 1_{\mathcal M_\lambda}.
\]

The commutant of the noise algebra contains

\[
\mathbf 1_{\mathcal V_\lambda}\otimes\mathcal B(\mathcal M_\lambda).
\]

Therefore operations on \(\mathcal M_\lambda\) commute with the noise.

A general noise channel covariant under \(G\) acts as

\[
\mathcal E(\rho)
=
\int_G dg\,\mu(g)\,U(g)\rho U(g)^\dagger.
\]

On each sector,

\[
\mathcal E:
\mathcal B(\mathcal V_\lambda\otimes\mathcal M_\lambda)
\to
\mathcal B(\mathcal V_\lambda\otimes\mathcal M_\lambda),
\]

the action on \(\mathcal M_\lambda\) is trivial up to preservation of the logical state.

Thus \(\mathcal M_\lambda\) is a decoherence-free subsystem.

\[
\boxed{
\text{Decoherence-free subspaces are representation-theoretic orbit invariants.}
}
\]

---

## 13. Quantum Error Correction as Orbit Protection

Quantum error-correcting codes may be understood as engineered admissibility orbit structures.

For a stabilizer code, the stabilizer group \(S\) is an Abelian admissibility group. The code space is the invariant subspace:

\[
\mathcal C
=
\{
|\psi\rangle
\mid
s|\psi\rangle=|\psi\rangle,\ \forall s\in S
\}.
\]

Errors move the state into different syndrome sectors, which are orbits under the error algebra. Recovery maps syndrome orbits back to the code orbit.

In non-Abelian codes, the same idea holds with representation sectors and multiplicity spaces.

Thus:

\[
\boxed{
\text{Quantum error correction is the stabilization of logical orbit information.}
}
\]

---

## 14. Framets as Quantum Frame Orbits

Framet Theory is the discrete quantum realization of Relativistic Quantum Theory.

Let \(\Gamma=(V,E)\) be a graph. Assign to each edge \(e\) a group element

\[
h_e\in G.
\]

The kinematical Hilbert space is

\[
\mathcal H_{\rm Fr}
=
\bigotimes_{e\in E}L^2(G).
\]

Local frame admissibility transformations are given by

\[
k_v\in G,\qquad v\in V.
\]

They act on edge variables by

\[
h_e
\mapsto
k_{s(e)}h_e k_{t(e)}^{-1}.
\]

The quantum gauge action is

\[
U_k|\{h_e\}\rangle
=
|\{k_{s(e)}h_e k_{t(e)}^{-1}\}\rangle.
\]

Physical Framet states satisfy the vertex constraints:

\[
\boxed{
\hat{\mathcal G}_v|\Psi_{\rm Fr}\rangle=0,
\qquad
\forall v\in V.
}
\]

Equivalently,

\[
|\Psi_{\rm Fr}\rangle
\in
\mathcal H_{\rm Fr}^{G^V}.
\]

By the Peter–Weyl theorem,

\[
L^2(G)
\cong
\bigoplus_j
\mathcal V_j\otimes\mathcal V_j^*.
\]

Thus a basis of the physical Hilbert space is given by spin-network-like states:

\[
\boxed{
|\Gamma,\{j_e\},\{\iota_v\}\rangle.
}
\]

Here:

- \(j_e\) labels irreducible representations on edges,
- \(\iota_v\) are intertwiners at vertices.

The intertwiner spaces are invariant multiplicity spaces:

\[
\iota_v
\in
\operatorname{Inv}
\left(
\bigotimes_{e\supset v}\mathcal V_{j_e}
\right).
\]

These intertwiner spaces are natural carriers of logical quantum information.

Thus:

\[
\boxed{
\text{Framets are quantum frame tokens whose physical states are admissibility orbits.}
}
\]

---

## 15. Framets, Logical Qubits, and Quantum Geometry

In Framet Theory, the physical information is not stored in the bare edge variables \(h_e\). It is stored in the gauge-invariant orbit data:

1. representation labels \(j_e\),
2. intertwiner states \(\iota_v\),
3. loop holonomies,
4. spin-network correlations.

Logical qubits may be encoded in the intertwiner spaces:

\[
\mathcal Q_{\rm logical}
\subset
\operatorname{Inv}
\left(
\bigotimes_{e\supset v}\mathcal V_{j_e}
\right).
\]

Because these spaces are invariant under local frame admissibility, they are protected against local frame noise.

In the continuum limit, Framet networks recover:

1. lattice gauge theory,
2. spin networks,
3. discrete frame theory,
4. quantum geometry,
5. gauge-invariant quantum field states.

Thus Framet Theory provides the discrete microstructure of Relativistic Quantum Theory.

---

## 16. Measurement in Relativistic Quantum Theory

A quantum measurement is described by a POVM

\[
E(\Delta),
\]

where \(\Delta\) is a measurable set of outcomes.

For the measurement to be admissibility-invariant, one requires

\[
\boxed{
U(g)E(\Delta)U(g)^\dagger
=
E(\Delta).
}
\]

Then for any state \(\rho\),

\[
p(\Delta)
=
\operatorname{Tr}(\rho E(\Delta))
\]

is invariant:

\[
\operatorname{Tr}(U(g)\rho U(g)^\dagger E(\Delta))
=
\operatorname{Tr}(\rho E(\Delta)).
\]

If the outcome space itself transforms under \(G\), one uses a covariant POVM:

\[
\boxed{
U(g)E(\Delta)U(g)^\dagger
=
E(g\Delta).
}
\]

In that case, the measurement outcome is frame-relative, and the invariant fact is the relational correlation between system, apparatus, and reference frame.

Thus quantum measurement is also orbital:

\[
\boxed{
\text{Measurement records are stable admissibility orbits.}
}
\]

---

## 17. Relational Observables in Relativistic Quantum Theory

In constrained quantum systems, physical observables must commute with the constraints:

\[
[\hat O,\hat C_a]=0.
\]

For systems with a Hamiltonian constraint, evolution is relational.

Let \(\hat T\) be a clock observable. The relational value of an observable \(\hat A\) when the clock reads \(\tau\) is

\[
\boxed{
\hat A(\tau)
=
\hat A\big|_{\hat T=\tau}.
}
\]

In the Heisenberg picture, one may write formally

\[
\hat A(\tau)
=
\int dt\,
e^{i\hat H t/\hbar}
\hat A
e^{-i\hat H t/\hbar}
\delta(\hat T(t)-\tau).
\]

Such relational observables are Dirac observables. They commute with the total constraint algebra and are invariant under admissibility transformations.

Thus quantum evolution is not external flow but relational correlation between invariant observables.

---

## 18. Example: Phase Admissibility in Quantum Mechanics

The simplest quantum admissibility group is

\[
G=U(1).
\]

It acts by

\[
|\psi\rangle\mapsto e^{i\theta}|\psi\rangle.
\]

The physical pure-state space is

\[
\mathbb P(\mathcal H)
=
(\mathcal H\setminus\{0\})/U(1).
\]

The global phase carries no physical information.

Expectation values,

\[
\langle\psi|A|\psi\rangle,
\]

are invariant under phase transformations.

Thus ordinary quantum mechanics already satisfies the orbit principle.

---

## 19. Example: Collective Rotation Noise and SU(2) Singlets

Suppose several qubits are subject to collective rotation noise:

\[
U(R)=R^{\otimes N},
\qquad
R\in SU(2).
\]

The Hilbert space decomposes as

\[
(\mathbb C^2)^{\otimes N}
\cong
\bigoplus_j
\mathcal V_j\otimes\mathcal M_j.
\]

The noise acts only on \(\mathcal V_j\). The multiplicity spaces \(\mathcal M_j\) are decoherence-free.

For \(N=2\), the singlet sector \(j=0\) is one-dimensional. For larger \(N\), the multiplicity spaces can encode logical qubits.

This is the standard mechanism of decoherence-free subspaces, now understood as a consequence of Relativistic Quantum Theory.

---

## 20. Example: Translational Quantum Reference Frames

Let a system \(S\) and a reference particle \(R\) move on a line. The translation group \(G=\mathbb R\) acts diagonally:

\[
U(a)
=
e^{-ia\hat P_S/\hbar}
\otimes
e^{-ia\hat P_R/\hbar}.
\]

Physical states satisfy

\[
(\hat P_S+\hat P_R)|\Psi\rangle=0.
\]

Conditioning on the reference position \(X_R=x\) yields a relative state of \(S\) at position relative to \(R\). Under a translation, the relative state transforms covariantly.

The physical content is not the absolute position of \(S\). It is the relative position orbit.

Thus quantum reference frames are naturally described by quotient orbits.

---

## 21. Example: Gauge-Invariant Quantum Information

In a lattice gauge theory, the physical Hilbert space satisfies Gauss constraints at every vertex:

\[
\hat{\mathcal G}_v|\Psi\rangle=0.
\]

Local gauge transformations are admissibility transformations. Physical information cannot be stored in gauge-noninvariant local charged variables. It must be stored in gauge-invariant structures:

1. Wilson loops,
2. electric flux lines,
3. intertwiners,
4. singlet matter combinations.

Thus gauge-invariant quantum information is automatically protected against local gauge noise, because local gauge transformations are not physical disturbances but changes of description.

---

## 22. Relativistic Quantum Information

Relativistic Quantum Theory redefines quantum information as orbit information.

A quantum information state is not a bare density matrix \(\rho\). It is an equivalence class

\[
[\rho]_G
=
\{
U(g)\rho U(g)^\dagger
\mid
g\in G
\}.
\]

One may always twirl a state:

\[
\bar\rho
=
\int_G dg\,U(g)\rho U(g)^\dagger.
\]

The twirled state is invariant, but it may discard frame-relative information. If the reference frame is included, the full relational information is preserved in the invariant total state.

Quantum information is therefore divided into:

1. **Frame-relative information**, carried by orbits,
2. **Perspective-neutral information**, carried by invariant states,
3. **Logical information**, carried by multiplicity spaces,
4. **Gauge information**, carried by singlet sectors.

This is the informational structure of Relativistic Quantum Theory.

---

## 23. Relativistic Quantum Theory and the RM Architecture

Relativistic Quantum Theory integrates with the other derived theories of Relativity Mechanics.

### Orbit Theory

Quantum states are orbits:

\[
[|\psi\rangle]_G.
\]

### Invariant Theory

Quantum observables are invariant operators:

\[
\mathcal A_{\rm phys}=\mathcal B(\mathcal H)^G.
\]

### Observer Theory

Quantum measurements are observer maps into outcome spaces.

### Reference Transformation Theory

Changes of quantum reference frame are maps between quotient descriptions.

### Constraint Mechanics

Gauge constraints select invariant physical states.

### Relativistic Dynamics

Schrödinger evolution descends to the projective quotient.

### Relativistic Information Theory

Quantum information is distinguishability of quantum orbits.

### Relativity Geometry

Projective Hilbert space and its quotient carry Fubini–Study geometry.

### Gauge Theory of Admissibility

Local internal frame transformations become gauge constraints.

### Frame Theory and Framet Theory

Continuous and discrete frame descriptions are unified by quantum admissibility orbits.

Thus Relativistic Quantum Theory is the quantum core of the Relativity Mechanics architecture.

---

## 24. Summary of the Formal Structure

The central structure of Relativistic Quantum Theory is:

\[
\boxed{
\mathcal R_{\rm RQT}
=
(\mathcal H,G,U,I_{\rm RQT}).
}
\]

The quantum state orbit is

\[
\boxed{
[|\psi\rangle]_G
=
\{e^{i\theta}U(g)|\psi\rangle\}.
}
\]

The physical pure-state space is

\[
\boxed{
\mathcal Q_{\rm RQT}
=
\mathbb P(\mathcal H)/G.
}
\]

The physical observable algebra is

\[
\boxed{
\mathcal A_{\rm phys}
=
\mathcal B(\mathcal H)^G.
}
\]

For gauge systems, the physical Hilbert space is

\[
\boxed{
\mathcal H_{\rm phys}
=
\mathcal H^G.
}
\]

For compact \(G\), the Hilbert space decomposes as

\[
\boxed{
\mathcal H
\cong
\bigoplus_\lambda
\mathcal V_\lambda\otimes\mathcal M_\lambda.
}
\]

Logical qubits live in \(\mathcal M_\lambda\).

Singlets live in the trivial representation sector.

Decoherence-free subspaces arise because \(G\) acts trivially on \(\mathcal M_\lambda\).

Framets arise as discrete quantum frame orbits, with physical states given by spin-network-like invariant intertwiners.

Quantum reference frames arise by conditioning invariant total states on quantum reference systems.

Gauge symmetry and quantum reference frames are unified by the same admissibility orbit structure.

---

## 25. Conclusion

Relativistic Quantum Theory answers the primitive question:

\[
\boxed{
\text{What is a quantum state in a relational universe?}
}
\]

The answer is:

\[
\boxed{
|\psi\rangle/G.
}
\]

A quantum state is not a bare vector. It is an equivalence class of vectors under admissibility transformations. Phase, basis, gauge, and reference-frame choices are descriptive redundancies. The physical quantum state is the orbit.

This orbit principle explains the emergence of protected quantum information. Representation theory decomposes Hilbert space into sectors where the admissibility group acts nontrivially on one factor and trivially on another. The trivial or multiplicity factors become singlets, decoherence-free subspaces, and logical qubits.

The same principle unifies quantum reference frames with gauge symmetry. A gauge-invariant total state is perspective-neutral. Conditioning on a quantum reference system yields relative states that transform covariantly and therefore form orbits. Framets are the discrete realization of this structure: elementary quantum frame tokens whose physical states are invariant spin-network orbits.

Thus Relativistic Quantum Theory establishes the quantum foundation of Relativity Mechanics:

\[
\boxed{
\text{Quantum reality is not a vector in Hilbert space. It is an admissibility orbit in projective Hilbert space.}
}
\]

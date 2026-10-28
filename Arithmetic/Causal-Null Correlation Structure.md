# Causal-Null Correlation Structure (CNCS)

A mathematical classification program for nonvanishing correlations under identically vanishing remote intervention response

## Abstract

We formulate the Causal-Null Correlation Structure (CNCS) as a candidate framework for classifying joint-state correlations that remain nonzero while every intervention permitted by a specified operational theory produces zero response at a designated remote subsystem. The central distinction is between the statistical structure of a joint state and the causal sensitivity of observable outcomes to interventions. These are mathematically different properties: correlations characterize joint distributions or joint-state functionals, whereas intervention response characterizes changes in outcome statistics under controlled transformations.

The basic condition is

\\[ K\_\rho(A,B)>0,\qquad R\_{A\rightarrow B}^{\rho}=0, \\]

where \\(K\_\rho\\) is a nonnegative correlation witness and \\(R\_{A\rightarrow B}^{\rho}\\) is an operationally defined response functional. This pair of conditions alone is not a new physical discovery. Quantum theory already admits entangled states with nonfactorizing correlations and no superluminal signaling. The proposed contribution is instead a classification of equivalence classes of joint-state structures under a fixed family of zero-response constraints, together with invariants capable of distinguishing states that are indistinguishable by remote-response experiments.

We construct the framework using operational state spaces, local completely positive trace-preserving maps, correlation tensors, intervention families, and quotient spaces of admissible states. We distinguish exact causal-nullity from approximate causal-nullity, derive the relationship between local intervention invariance and no-signaling, establish elementary classification results, and identify the additional hypotheses required for stronger theorems. A concrete two-qubit model illustrates why identical remote response does not imply identical correlation structure. We then formulate a classification theorem schema, a stability problem, and an experimental program involving Bell witnesses, process tomography, intervention-response bounds, and spacelike-separated measurement arrangements.

The framework is presented as a research program with explicitly delimited results. The mathematical definitions and elementary propositions below are derivable within standard quantum theory; the existence of a useful, nontrivial, representation-independent CNCS classification remains an open research objective.

## 1. Introduction

### 1.1 The structural question

Consider two subsystems, \\(A\\) and \\(B\\), whose joint state is represented by \\(\rho\_{AB}\\). Measurements on the subsystems may exhibit correlations even when an intervention performed at \\(A\\) cannot alter the local outcome statistics available at \\(B\\).

The problem is not simply to establish that correlations can coexist with no-signaling. That coexistence is well established. The deeper question is:

Which physically distinct joint-state structures belong to the same causal-null class, and what invariant data distinguish those classes without introducing a remote causal influence?

This question requires three separate objects:

1. A state space describing the possible joint configurations.
2. A correlation map extracting joint-state structure.
3. An intervention-response map testing how that structure behaves under operationally permitted interventions.

A classification must preserve these distinctions. Otherwise, one risks confusing correlation with causation, statistical independence with causal independence, or a vanishing measured response with a proof that all possible responses vanish.

### 1.2 Scope and epistemic status

Throughout this paper, statements fall into four categories.

- Established: consequences of standard quantum mechanics, completely positive quantum operations, and the usual operational definition of no-signaling.
- Derived here: elementary propositions following from the definitions and assumptions explicitly stated.
- Proposed: the CNCS classification, invariants, and experimental witnesses that require further development.
- Conjectural: possible new structural relations whose validity has not been established.

No claim is made that a new fundamental interaction, a nonspatiotemporal ontology, or a previously unknown physical correlation has been demonstrated. CNCS is initially a mathematical framework for organizing and classifying known and potentially new correlation structures.

### 1.3 Central hypothesis

Let \\(\mathcal S\\) denote a state space, \\(\mathcal I_A\\) an allowed intervention family at \\(A\\), and \\(\mathcal O_B\\) a family of accessible observables at \\(B\\). For a state \\(\rho\in\mathcal S\\), define a response map

\\[ \mathscr R\_{\rho}: \mathcal I_A\times\mathcal O_B\longrightarrow\mathbb R. \\]

The causal-null sector is the set of states for which this map vanishes identically over the specified domain:

\\[ \mathcal N\_{\mathrm{CNCS}} = \left\\{\rho\in\mathcal S: \mathscr R\_{\rho}(I,O)=0 \\;\\;\forall I\in\mathcal I_A,\\; \forall O\in\mathcal O_B \right\\}. \\]

The classification problem is to understand the fibers of this constraint map: which states lie in \\(\mathcal N\_{\mathrm{CNCS}}\\), which are physically equivalent under a declared equivalence relation, and which correlation invariants vary across those equivalence classes.

This formulation makes the intervention family part of the theory rather than an implicit experimental detail.

## 2. Mathematical preliminaries and operational assumptions

### 2.1 Bipartite state space

Let \\(\mathcal H_A\\) and \\(\mathcal H_B\\) be finite-dimensional Hilbert spaces associated with subsystems \\(A\\) and \\(B\\). The joint state space is

\\[ \mathcal S\_{AB} = \\{\rho\_{AB}\mid \rho\_{AB}\geq0,\\; \operatorname{Tr}\rho\_{AB}=1\\}. \\]

The reduced states are

\\[ \rho_A=\operatorname{Tr}\_B\rho\_{AB}, \qquad \rho_B=\operatorname{Tr}\_A\rho\_{AB}. \\]

The joint state need not factorize:

\\[ \rho\_{AB}\ne\rho_A\otimes\rho_B. \\]

This nonfactorization is a state-level property. It does not, by itself, establish that an intervention at \\(A\\) can influence the local statistics at \\(B\\).

For a measurement described by positive-operator-valued measures (POVMs) \\(\\{M_a^x\\}\_a\\) and \\(\\{N_b^y\\}\_b\\), the joint outcome distribution is

\\[ p(a,b\mid x,y) = \operatorname{Tr} \left[ \rho\_{AB} \left(M_a^x\otimes N_b^y\right) \right]. \\]

The marginal distribution at \\(B\\) is

\\[ p(b\mid x,y) = \sum_a p(a,b\mid x,y). \\]

Operational no-signaling from \\(A\\) to \\(B\\) requires that this marginal be independent of the freely selected measurement setting \\(x\\):

\\[ p(b\mid x,y)=p(b\mid x',y) \\]

for all allowed \\(x,x',y,b\\). The corresponding condition in the opposite direction must be imposed separately. This is the standard operational condition used in analyses of Bell experiments and quantum causal networks.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

PRX Quantum

+1



### 2.2 Intervention families

An intervention at \\(A\\) will be represented initially by a completely positive trace-preserving (CPTP) map

\\[ \mathcal E_A:\mathcal L(\mathcal H_A) \longrightarrow\mathcal L(\mathcal H_A). \\]

The transformed joint state is

\\[ \rho\_{AB}^{\mathcal E} = (\mathcal E_A\otimes\operatorname{id}\_B)(\rho\_{AB}). \\]

Let \\(\mathfrak I_A\\) denote the permitted family of interventions. It may be the set of all CPTP maps, a physically implementable subset, or a context-specific family constrained by localization, energy, timing, or apparatus limitations.

This choice matters. A classification theorem is meaningful only if the allowed intervention domain is specified.

We distinguish three cases:

1. Unrestricted local quantum operations: every CPTP map on \\(A\\) is permitted.
2. Operationally restricted interventions: only a subset \\(\mathfrak I_A\\) is available.
3. Relativistically localized interventions: interventions must arise from interactions supported in a specified spacetime region and satisfy the relevant field-theoretic admissibility conditions.

These cases should not be conflated. In relativistic quantum field theory, an abstract operation on a Hilbert space need not automatically correspond to a physically implementable operation localized in a spacetime region. Recent work on relativistic measurement theory makes this distinction explicit.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. D

+1



### 2.3 The response functional

For each intervention \\(\mathcal E_A\in\mathfrak I_A\\), define the remote reduced state

\\[ \rho_B^{\mathcal E} = \operatorname{Tr}\_A \left[ (\mathcal E_A\otimes\operatorname{id}\_B)(\rho\_{AB}) \right]. \\]

The operational response to that intervention is quantified by trace distance:

\\[ r_B(\mathcal E_A;\rho) = \frac12 \left\\| \rho_B^{\mathcal E}-\rho_B \right\\|\_1, \\]

where \\(\\|X\\|\_1=\operatorname{Tr}\sqrt{X^\dagger X}\\).

This distance is operationally meaningful: it quantifies how distinguishable the remote states are using measurements on \\(B\\) alone.

Define the worst-case response

\\[ \boxed{ R\_{A\rightarrow B}(\rho;\mathfrak I_A) = \sup\_{\mathcal E_A\in\mathfrak I_A} \frac12 \left\\| \rho_B^{\mathcal E}-\rho_B \right\\|\_1 } \\]

with

\\[ 0\le R\_{A\rightarrow B}\le1. \\]

The exact causal-null condition is

\\[ R\_{A\rightarrow B}(\rho;\mathfrak I_A)=0. \\]

It means that every permitted intervention produces the same local reduced state at \\(B\\). It does not mean that every conditional state at \\(B\\), conditioned on a particular outcome observed at \\(A\\), is unchanged. Conditional steering and controllable signaling are distinct operational questions.

### 2.4 The correlation functional

A correlation measure should satisfy four requirements:

- It should be zero for a product state, if it is intended to quantify connected correlations.
- It should be positive for at least some nonfactorizing states.
- It should be invariant under changes of local coordinate basis.
- It should not be defined by the intervention response itself, since the objective is to compare independent correlation and response measures.

One suitable choice is a connected correlation tensor.

Choose orthonormal bases of traceless Hermitian operators \\(\\{F_i\\}\\) on \\(A\\) and \\(\\{G_j\\}\\) on \\(B\\), normalized so that

\\[ \operatorname{Tr}(F_iF_k)=\delta\_{ik}, \qquad \operatorname{Tr}(G_jG\_\ell)=\delta\_{j\ell}. \\]

Define

\\[ T\_{ij}(\rho) = \operatorname{Tr}[\rho(F_i\otimes G_j)] - \operatorname{Tr}(\rho_A F_i) \operatorname{Tr}(\rho_B G_j). \\]

The CNCS correlation witness is

\\[ \boxed{ K\_{\mathrm{CNCS}}(\rho) = \left( \sum\_{i,j}|T\_{ij}(\rho)|^2 \right)^{1/2} } \\]

This is the Frobenius norm of the connected correlation tensor. It is nonnegative, vanishes on product states, and is invariant under local unitary changes of basis. It is a witness of connected correlation, not a universal measure of entanglement: nonzero values may arise from either classical or quantum correlations.

A second useful diagnostic is quantum mutual information,

\\[ I(A:B)\_\rho = S(\rho_A)+S(\rho_B)-S(\rho\_{AB}), \\]

where \\(S(\rho)=-\operatorname{Tr}(\rho\log\rho)\\). It quantifies total correlations in the quantum-information sense, whereas \\(K\_{\mathrm{CNCS}}\\) emphasizes a chosen family of connected observables. Neither should be treated as a substitute for the other.

### 2.5 The defining relation

The proposed causal-null correlation relation is therefore

\\[ \boxed{ K\_{\mathrm{CNCS}}(\rho)>0, \qquad R\_{A\rightarrow B}(\rho;\mathfrak I_A)=0. } \\]

For a bidirectional causal-null relation, we require

\\[ R\_{A\rightarrow B}=R\_{B\rightarrow A}=0. \\]

The pair of conditions is mathematically well-defined once the state space, observable family, and intervention family are fixed. The important question is what additional structure can be classified beyond this initial definition.

## 3. The elementary causal-null theorem

### 3.1 Statement

Theorem 1 — Local trace-preserving operations preserve the remote reduced state.

Let \\(\rho\_{AB}\\) be any bipartite density operator and let \\(\mathcal E_A\\) be any CPTP map acting only on subsystem \\(A\\). Then

\\[ \operatorname{Tr}\_A \left[ (\mathcal E_A\otimes\operatorname{id}\_B)(\rho\_{AB}) \right] = \operatorname{Tr}\_A\rho\_{AB}. \\]

Consequently,

\\[ R\_{A\rightarrow B}(\rho;\mathfrak I_A)=0 \\]

whenever \\(\mathfrak I_A\\) consists of local CPTP maps and the response is defined by the nonselective reduced state at \\(B\\).

### 3.2 Proof

Let \\(\\{K\_\alpha\\}\\) be Kraus operators for \\(\mathcal E_A\\), so that

\\[ \mathcal E_A(X) = \sum\_\alpha K\_\alpha X K\_\alpha^\dagger, \qquad \sum\_\alpha K\_\alpha^\dagger K\_\alpha=I_A. \\]

For any observable \\(O_B\\) on \\(B\\),

\\[ \begin{aligned} &\operatorname{Tr} \left[ O_B\\, \operatorname{Tr}\_A \left( (\mathcal E_A\otimes\operatorname{id}\_B)(\rho\_{AB}) \right) \right]\\\ &= \operatorname{Tr} \left[ (I_A\otimes O_B) \sum\_\alpha (K\_\alpha\otimes I_B) \rho\_{AB} (K\_\alpha^\dagger\otimes I_B) \right]\\\ &= \operatorname{Tr} \left[ \rho\_{AB} \left( \sum\_\alpha K\_\alpha^\dagger K\_\alpha \otimes O_B \right) \right]\\\ &= \operatorname{Tr} \left[ \rho\_{AB}(I_A\otimes O_B) \right]\\\ &= \operatorname{Tr}(O_B\rho_B). \end{aligned} \\]

Since this holds for every observable \\(O_B\\), the two reduced density operators are equal. Therefore their trace distance is zero, and taking the supremum over the allowed local CPTP maps gives the result. \\(\square\\)

The theorem is an established quantum-information result expressed in the present notation. It does not establish a new physical law. The usual no-signaling theorem likewise allows entangled initial states; a product-state assumption is unnecessary.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC

+1



### 3.3 The critical implication for CNCS

Theorem 1 reveals an important structural fact:

> If all local CPTP maps are allowed and the response is defined only by changes in the remote nonselective marginal, causal-nullity is universal across the entire bipartite quantum state space.

Thus, under unrestricted quantum operations,

\\[ \mathcal N\_{\mathrm{CNCS}}=\mathcal S\_{AB}. \\]

The condition \\(R\_{A\rightarrow B}=0\\) alone cannot distinguish entangled from separable states, weakly correlated from strongly correlated states, or states with different higher-order joint structure.

This is not a defect in the theorem. It identifies where the proposed research contribution must lie. A useful CNCS theory cannot claim that the zero-response property itself identifies a novel subset of ordinary quantum states. Instead, it must classify the correlation structures that coexist with the same operational null constraint.

If a more selective causal-null sector is desired, one must introduce additional physical restrictions, such as localized interventions in quantum field theory, restricted observables, particular intervention sequences, or constraints on admissible channels. Such restrictions must be justified independently; they cannot be chosen merely to manufacture apparent novelty.

## 4. Classification of joint-state structure

### 4.1 Why the response condition is not a complete invariant

Suppose \\(\rho\\) and \\(\sigma\\) satisfy

\\[ R\_{A\rightarrow B}(\rho) = R\_{A\rightarrow B}(\sigma)=0. \\]

This equality does not imply

\\[ \rho=\sigma, \qquad K\_{\mathrm{CNCS}}(\rho) = K\_{\mathrm{CNCS}}(\sigma), \\]

or that the two states have the same entanglement, mutual information, or multipartite extensions.

The response functional identifies a common operational property, not a unique joint-state structure. This motivates a family-based classification.

Let \\(\mathcal N\subseteq\mathcal S\_{AB}\\) be a causal-null sector under a fixed intervention model. Define a classification map

\\[ \mathfrak C:\mathcal N\longrightarrow\mathcal X, \\]

where \\(\mathcal X\\) is a space of structural descriptors. The map may contain correlation tensors, spectra, entanglement witnesses, mutual information, or other invariants. The central challenge is to identify a descriptor that is both operationally meaningful and sufficiently discriminating.

### 4.2 Equivalence relations

Several inequivalent notions of “same structure” are possible.

State identity:

\\[ \rho\equiv\_{\mathrm{state}}\sigma \iff \rho=\sigma. \\]

Local-unitary equivalence:

\\[ \rho\equiv\_{\mathrm{LU}}\sigma \iff \sigma=(U_A\otimes U_B)\rho (U_A^\dagger\otimes U_B^\dagger). \\]

Operational equivalence relative to an experiment family \\(\mathfrak M\\):

\\[ \rho\equiv\_{\mathfrak M}\sigma \iff p\_\rho(\mathbf a\mid\mathbf x) = p\_\sigma(\mathbf a\mid\mathbf x) \quad \forall\\,(\mathbf x,\mathbf a)\in\mathfrak M. \\]

The final relation depends on the measurements included in \\(\mathfrak M\\). Two states may be operationally equivalent for a restricted measurement family but distinguishable by a tomographically complete one.

The proposed CNCS classification should therefore specify which equivalence relation it uses. Without this specification, statements about “physically distinct correlations” are ambiguous.

### 4.3 The causal-null quotient

Given an equivalence relation \\(\sim\\) on \\(\mathcal N\\), define the quotient space

\\[ \boxed{ \mathcal Q\_{\mathrm{CNCS}} = \mathcal N/\\!\sim } \\]

Each element \\([\rho]\_\sim\\) represents a class of states equivalent under the chosen operational or physical criterion.

A classification program should determine:

1. Whether \\(\mathcal Q\_{\mathrm{CNCS}}\\) has a finite or manageable set of invariants.
2. Whether those invariants distinguish all classes, or only selected subclasses.
3. Whether the invariants are stable under small perturbations and measurement noise.
4. Whether the classification is preserved under local channels, composition with ancillary systems, and changes of representation.
5. Whether the resulting classes have empirically distinguishable signatures.

The quotient construction is a standard mathematical technique. The prospective contribution is the identification of a useful CNCS-specific equivalence relation and a classification theorem for its classes.

### 4.4 A necessary distinction: invariant versus complete invariant

A function \\(J:\mathcal N\to\mathbb R\\) is an invariant under an equivalence relation \\(\sim\\) if

\\[ \rho\sim\sigma\implies J(\rho)=J(\sigma). \\]

It is a complete invariant if the converse also holds:

\\[ J(\rho)=J(\sigma)\implies\rho\sim\sigma. \\]

A correlation norm such as \\(K\_{\mathrm{CNCS}}\\) is generally not complete. Distinct states can have the same norm while differing in tensor orientation, spectrum, entanglement properties, or higher-order correlations.

Consequently, a scalar CNCS witness can identify the presence or magnitude of one class of connected correlations, but a full classification will generally require a vector or hierarchy of invariants.

## 5. A two-qubit model: identical causal-nullity, different correlations

The simplest useful test of the framework is a pair of two-qubit states with different connected correlations but identical zero-response properties.

### 5.1 A continuously parameterized state family

Consider the two-qubit Werner family

\\[ \rho_W(p) = (1-p)\frac{I_4}{4} + p\\,|\psi^-\rangle\langle\psi^-|, \qquad 0\le p\le1, \\]

where

\\[ |\psi^-\rangle = \frac{|01\rangle-|10\rangle}{\sqrt2} \\]

is the singlet state.

The state has maximally mixed local marginals:

\\[ \rho_A=\rho_B=\frac{I_2}{2}. \\]

Its Pauli correlation tensor is

\\[ T\_{ij} = \operatorname{Tr} \left[ \rho_W(p)(\sigma_i\otimes\sigma_j) \right] = -p\\,\delta\_{ij}. \\]

With the Pauli-basis convention, the corresponding connected-correlation norm is

\\[ K\_{\mathrm{Pauli}}(\rho_W(p)) = \sqrt{\sum\_{i,j}T\_{ij}^2} = \sqrt3\\,p. \\]

If the operator basis is normalized by \\(\operatorname{Tr}(F_iF_j)=\delta\_{ij}\\), the numerical value rescales by a fixed convention-dependent factor. The classification is unaffected by that normalization choice.

By Theorem 1,

\\[ R\_{A\rightarrow B}(\rho_W(p))=0 \\]

for every \\(p\\) under local nonselective CPTP interventions. The reverse response is also zero.

Thus the entire family satisfies the same causal-null condition, while the correlation witness varies continuously from zero at \\(p=0\\) to its maximal value within this family at \\(p=1\\).

### 5.2 Classical and quantum structure within the same null sector

At \\(p=0\\),

\\[ \rho_W(0)=\frac{I_4}{4} =\frac{I_2}{2}\otimes\frac{I_2}{2}, \\]

so the state is a product state and has no connected correlations.

At \\(p=1\\), the state is the pure singlet and is maximally entangled.

For the standard two-qubit Werner family, the state is separable for \\(p\le 1/3\\) and entangled for \\(p>1/3\\). Hence the same operational causal-null property includes product, separable-correlated, and entangled states. The separation between nonzero correlations and zero remote signaling is therefore not restricted to a single correlation type.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://link.springer.com\&sz=32)

Springer Nature Link

+1



The family provides a basic classification result:

Proposition 2 — Nonuniqueness of the causal-null state structure.

There exist states \\(\rho,\sigma\in\mathcal S\_{AB}\\) such that

\\[ R\_{A\rightarrow B}(\rho) = R\_{A\rightarrow B}(\sigma)=0, \\]

but

\\[ K\_{\mathrm{CNCS}}(\rho) \ne K\_{\mathrm{CNCS}}(\sigma). \\]

Proof. Take \\(\rho=I_4/4\\) and \\(\sigma=|\psi^-\rangle\langle\psi^-|\\). Both have zero response under local CPTP interventions by Theorem 1. Their connected-correlation norms differ: the former has zero connected correlation, while the latter has a nonzero correlation tensor. \\(\square\\)

This proposition is a direct consequence of established quantum theory, not a new discovery. Its importance for CNCS is methodological: it proves that response-nullity cannot serve as a complete classifier of joint-state structure.

### 5.3 An explicit classical-correlation control

To ensure that the framework does not merely rename entanglement, consider

\\[ \rho\_{\mathrm{cl}}(c) = \frac14 \left( I\otimes I+c\\,\sigma_z\otimes\sigma_z \right), \qquad |c|\le1. \\]

Its marginals are maximally mixed, and its only nonzero connected Pauli correlation is

\\[ T\_{zz}=c. \\]

Therefore,

\\[ K\_{\mathrm{Pauli}}(\rho\_{\mathrm{cl}}(c))=|c|. \\]

For every nonzero \\(c\\), this state is correlated, yet it is separable: it is a convex mixture of product states diagonal in the computational basis. It also satisfies the same zero-response condition under local nonselective CPTP operations.

The comparison between \\(\rho\_{\mathrm{cl}}(c)\\) and \\(\rho_W(p)\\) shows that a CNCS classification must distinguish at least three different questions:

- Is the joint state correlated?
- Is the correlation entangled or otherwise nonclassical?
- Can a permitted remote intervention change the other subsystem's local marginal?

These questions are related but not interchangeable.

## 6. The correlation-response map

### 6.1 From a binary property to a family-level object

The basic pair \\((K,R)\\) is too coarse to classify the internal structure of a joint state. We therefore introduce a richer map.

Let \\(\mathfrak A_A\\) and \\(\mathfrak A_B\\) denote the allowed local observable families. For each state \\(\rho\\), define its connected-correlation functional

\\[ C\_\rho(A,B) = \operatorname{Tr}(\rho\\,A\otimes B) - \operatorname{Tr}(\rho_A A) \operatorname{Tr}(\rho_B B), \\]

for \\(A\in\mathfrak A_A\\), \\(B\in\mathfrak A_B\\).

Define the intervention-response functional

\\[ D\_\rho(\mathcal E_A;B) = \operatorname{Tr} \left[ \rho\_{AB}^{\mathcal E}(I_A\otimes B) \right] - \operatorname{Tr} \left[ \rho\_{AB}(I_A\otimes B) \right]. \\]

The family-level CNCS descriptor is

\\[ \boxed{ \mathfrak F\_{\mathrm{CNCS}}(\rho) = \left( C\_\rho,\\; D\_\rho \right). } \\]

The state is causal-null relative to the specified intervention and observable families precisely when

\\[ D\_\rho(\mathcal E_A;B)=0 \\]

for every permitted \\(\mathcal E_A\\) and every \\(B\in\mathfrak A_B\\).

This functional formulation preserves more information than a single correlation norm. The correlation component records joint-state structure; the response component records intervention sensitivity.

### 6.2 A response-null fiber

Define the response map

\\[ \mathscr D:\mathcal S\_{AB}\to\mathcal Y, \qquad \rho\mapsto D\_\rho, \\]

where \\(\mathcal Y\\) is a suitable space of real-valued functionals over the intervention-observable domain.

The response-null set is the zero fiber

\\[ \mathcal N=\mathscr D^{-1}(0). \\]

If all local CPTP maps and all local observables are allowed, Theorem 1 implies that this fiber is the entire bipartite state space. Under restricted physical interventions, the fiber may be more selective, but that must be established for the specific model.

The classification question becomes:

\\[ \text{How does the correlation map }C \text{ vary over the fiber }\mathscr D^{-1}(0)? \\]

Equivalently, for a prescribed correlation descriptor \\(c\\), one may investigate the constrained set

\\[ \mathcal F_c = \\{\rho\in\mathcal N:C\_\rho=c\\}. \\]

The geometry, connected components, and invariant structure of these fibers are possible mathematical targets. Their properties will depend on the state space, the observable family, and the intervention constraints.

### 6.3 A hierarchy of distinguishability

A useful classification should distinguish several levels:

| Level                       | Data retained                              | What it can establish                                        |
| --------------------------- | ------------------------------------------ | ------------------------------------------------------------ |
| I. Nullity                  | \\(R=0\\)                                  | No detectable response under the defined intervention family |
| II. Scalar correlation      | \\(K\\) or \\(I(A:B)\\)                    | Correlation strength under a chosen measure                  |
| III. Tensor structure       | \\(T\_{ij}\\) and local moments            | Orientation and component structure of correlations          |
| IV. Spectral structure      | State spectrum and entanglement invariants | Further distinctions between joint states                    |
| V. Operational class        | Full statistics for a measurement family   | Indistinguishability relative to that family                 |
| VI. Complete classification | A proven complete invariant set            | Equivalence-class identification under the chosen relation   |

The levels are not a universal ordering of physical importance. They describe increasing amounts of information in a particular classification scheme. In particular, a full state spectrum alone does not determine the operational equivalence class of a bipartite state, and local-unitary equivalence is not identical to equality of measurement statistics under a restricted measurement family.

## 7. The proposed CNCS classification theorem

### 7.1 The theorem sought

The main research objective is not to prove that correlations can coexist with zero signaling. Theorem 1 already establishes a standard version of that result in finite-dimensional quantum theory.

The substantive objective is to find conditions under which the causal-null sector admits a useful classification by structural invariants.

Let \\(\mathcal N\subseteq\mathcal S\\) be the causal-null sector of a specified operational theory. Let \\(\sim\\) be a declared physical equivalence relation, and let

\\[ J:\mathcal N\longrightarrow\mathcal J \\]

be a candidate invariant map.

CNCS Classification Conjecture. For a suitably chosen nontrivial intervention model and correlation descriptor, there exists an invariant map \\(J\\) such that

\\[ J(\rho)=J(\sigma) \quad\Longleftrightarrow\quad \rho\sim\sigma \\]

for all \\(\rho,\sigma\in\mathcal N\\), or for a clearly identified restricted subclass of \\(\mathcal N\\).

This is a conjectural research target, not an established theorem. In unrestricted bipartite quantum theory, it would be misleading to present the mere existence of a complete invariant for a finite-dimensional state space as novel. The potential contribution must come from a nontrivial physically motivated equivalence relation, a new invariant with explanatory or predictive value, or a classification theorem that is not already implied by standard state-classification methods.

### 7.2 Required hypotheses

A rigorous theorem would need to specify at least the following.

H1 — Operational completeness. The intervention family \\(\mathfrak I_A\\), observable family \\(\mathfrak A_B\\), and the state space \\(\mathcal S\\) are fixed explicitly.

H2 — Physical equivalence. The relation \\(\sim\\) is defined independently of the desired classification result.

H3 — Invariance. The proposed \\(J\\) is constant on each equivalence class.

H4 — Separation. If \\(J(\rho)=J(\sigma)\\), then \\(\rho\sim\sigma\\), at least on the target domain.

H5 — Stability. Small changes in measured statistics do not produce uncontrolled changes in the inferred class, except at specified singular or boundary cases.

H6 — Nontriviality. The classification distinguishes physically meaningful structures that are not already completely distinguished by a standard, readily available invariant set under the same assumptions.

Without H6, the framework may remain mathematically consistent but contribute little beyond a change of notation.

### 7.3 A useful alternative: partial classification

A complete invariant may be unnecessary or impractical. One can instead seek a hierarchy

\\[ J_1(\rho),J_2(\rho),\ldots,J_m(\rho) \\]

that successively refines equivalence classes. Define

\\[ \rho\sim_m\sigma \iff J_k(\rho)=J_k(\sigma) \quad \text{for every }k\le m. \\]

This generates a sequence of increasingly fine partitions. The research question becomes whether the sequence stabilizes, whether its invariants can be measured efficiently, and whether the stable partition has a natural physical interpretation.

This approach is especially relevant for many-body states, where a complete global description may be exponentially expensive to obtain. Recent work on local tomography illustrates the broader problem of reconstructing global state or channel properties from local measurements under additional assumptions.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nature.com\&sz=32)

npj Quantum Information

+1



## 8. Exact causal-nullity versus approximate causal-nullity

### 8.1 Why exact zero is not an experimental observation

In a mathematical model, one may prove

\\[ R\_{A\rightarrow B}=0. \\]

In a laboratory, finite sample sizes, detector inefficiency, imperfect isolation, timing uncertainty, and calibration error prevent an experiment from establishing exact zero response solely from data.

The empirical problem is therefore to bound the response:

\\[ R\_{A\rightarrow B}\le\varepsilon, \\]

where \\(\varepsilon\\) is an experimentally justified upper confidence bound or a theoretically derived error tolerance.

This motivates an approximate causal-null sector:

\\[ \mathcal N\_\varepsilon = \left\\{ \rho: R\_{A\rightarrow B}(\rho;\mathfrak I_A) \le\varepsilon \right\\}. \\]

For exact mathematical quantum theory with local CPTP interventions, \\(\varepsilon=0\\) follows from Theorem 1. In a physical experiment, a small observed response is evidence of consistency with a null model, not proof of exact causal-nullity.

### 8.2 A measurement-level response statistic

Suppose \\(x\\) and \\(x'\\) denote alternative intervention settings at \\(A\\), while \\(b\\) labels outcomes at \\(B\\). Define

\\[ \Delta\_{\mathrm{NS}} = \sup\_{x,x',y} \frac12 \sum_b \left| p(b\mid x,y)-p(b\mid x',y) \right|. \\]

This is a classical total-variation measure of the dependence of the remote outcome distribution on the remote setting. It vanishes precisely when the tested conditional marginals are independent of the selected setting.

The experiment samples only a finite set of settings, so the empirical quantity is a restricted estimate of the supremum. To claim a bound over a larger intervention family, the experiment needs either a justified finite reduction, a structural theorem, or an independently validated model for the untested operations.

For quantum systems with full access to the relevant local channels and output states, trace-distance bounds can be related to distinguishability. In an ordinary Bell experiment, the measurement-level statistic is usually the directly estimable quantity.

### 8.3 Stability of response-nullity

A proposed classification should not depend on distinguishing an exactly zero response from an arbitrarily small nonzero one without accounting for experimental precision.

Let \\(d\_{\mathcal S}\\) be a distance on states and suppose the response map satisfies a continuity bound

\\[ |R(\rho)-R(\sigma)| \le L\\,d\_{\mathcal S}(\rho,\sigma) \\]

for some constant \\(L\\) on the domain of interest. Then

\\[ R(\rho)\le\varepsilon \quad\Longrightarrow\quad R(\sigma)\le\varepsilon+L\\,d\_{\mathcal S}(\rho,\sigma). \\]

This follows directly from the assumed Lipschitz condition. The nontrivial problem is to obtain useful values of \\(L\\) for the chosen intervention family and response norm.

For the unrestricted finite-dimensional CPTP model, the response is identically zero, so this stability question is trivial. It becomes important in restricted-intervention models, in relativistic field theories with physical localization constraints, and in experiments testing deviations from the standard operational assumptions.

### 8.4 A correlation-response phase diagram

For exploratory purposes, one may plot a family of states in the plane

\\[ \big(K\_{\mathrm{CNCS}},R\_{A\rightarrow B}\big). \\]

The standard quantum model with local nonselective CPTP operations occupies the axis \\(R=0\\), while different states can have different values of \\(K\_{\mathrm{CNCS}}\\). A hypothetical model allowing controllable remote signaling could populate points with \\(R>0\\).

Such a diagram is a visualization of two independent diagnostics, not evidence that the underlying state space has a new phase transition. A genuine phase diagram would require an independently justified control parameter, an appropriate thermodynamic or dynamical limit, and a demonstrated nonanalyticity or other meaningful transition criterion.

## 9. Correlation, signaling, and relativistic causality

### 9.1 Three distinct notions

CNCS requires a strict separation of three claims:

Statistical correlation: joint outcome probabilities do not factorize.

\\[ p(a,b\mid x,y) \ne p(a\mid x)p(b\mid y) \\]

for at least some allowed settings and outcomes.

No-signaling: the marginal outcome distribution at one subsystem is independent of the remote freely selected setting.

\\[ p(b\mid x,y)=p(b\mid x',y). \\]

Bell local causality: conditional on a sufficiently complete specification of relevant common-cause variables \\(\lambda\\), the joint distribution factorizes:

\\[ p(a,b\mid x,y,\lambda) = p(a\mid x,\lambda)p(b\mid y,\lambda). \\]

The third condition is stronger than no-signaling. Bell-inequality violations show that quantum predictions cannot generally be represented by a model satisfying the relevant Bell-local assumptions. They do not, by themselves, demonstrate controllable superluminal signaling.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://plato.stanford.edu\&sz=32)

Stanford Encyclopedia of Philosophy

+1



CNCS is designed to describe a compatibility between correlation and operational causal-nullity. It does not supply a hidden-variable explanation of Bell correlations, nor does it resolve every philosophical interpretation of Bell's theorem.

### 9.2 Local observables in quantum field theory

In relativistic quantum field theory, local observables associated with spacelike-separated regions are commonly required to satisfy microcausality:

\\[ [A(x),B(y)]=0 \qquad \text{when }(x-y)^2<0, \\]

with the sign convention for the spacetime metric understood.

For a suitable state \\(\omega\\), this commutativity does not imply statistical factorization:

\\[ \omega(AB) \ne \omega(A)\omega(B) \\]

may still hold.

The distinction is central to the CNCS interpretation: commutativity constrains the algebraic relation between spacelike-separated observables, while the state determines their joint expectation values.

However, one must not assume that every abstract quantum operation can be implemented in a compact spacetime region. A relativistic analysis must define the local interactions, include the measurement apparatus, and establish the required causal properties of the resulting operation. This is an active technical issue in rigorous treatments of local measurements in quantum field theory.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://qft.org\&sz=32)

QFT .org

+2



### 9.3 What a spacelike experiment can establish

A spacelike-separated experiment can test whether the measured distribution at \\(B\\) depends on a setting selected at \\(A\\), while also estimating correlation witnesses from the joint data.

It cannot directly establish that correlations are ontologically timeless, that no deeper causal explanation exists, or that no hidden mediator of any kind is possible. Those claims require assumptions beyond the observed no-signaling statistics.

The experimentally defensible statement is narrower: within a stated experimental arrangement and intervention family, the measured joint statistics are correlated while the remote response is bounded by a specified tolerance.

## 10. Selective interventions and the steering distinction

A frequent source of confusion is the difference between a nonselective operation and conditioning on one of its outcomes.

Let an instrument at \\(A\\) consist of completely positive maps \\(\\{\mathcal I_a\\}\_a\\) such that their sum

\\[ \mathcal E_A=\sum_a\mathcal I_a \\]

is trace-preserving. The unnormalized conditional state of \\(B\\) associated with outcome \\(a\\) is

\\[ \widetilde\rho_B^{\\,a} = \operatorname{Tr}\_A \left[ (\mathcal I_a\otimes\operatorname{id}\_B)(\rho\_{AB}) \right]. \\]

Its probability is

\\[ p(a)=\operatorname{Tr}\widetilde\rho_B^{\\,a}, \\]

and, when \\(p(a)>0\\), the normalized conditional state is

\\[ \rho_B^a=\frac{\widetilde\rho_B^{\\,a}}{p(a)}. \\]

The conditional state \\(\rho_B^a\\) may depend on \\(a\\). But \\(a\\) is a random outcome, and an observer at \\(B\\) cannot use that outcome to receive a controllable message unless the outcome information is transmitted through an ordinary communication channel.

When the outcomes are averaged without conditioning,

\\[ \sum_a\widetilde\rho_B^{\\,a}=\rho_B, \\]

by Theorem 1. Thus the ensemble state at \\(B\\) remains unchanged even when its decomposition into conditional states depends on the measurement performed at \\(A\\).

This distinction is essential to any proposed CNCS classification. A theory that uses conditional states as its response measure must explicitly account for the conditioning information. Otherwise it risks treating steering as signaling.

The general no-signaling and steering conditions are widely studied in multipartite quantum correlations.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nature.com\&sz=32)

npj Quantum Information

+1



## 11. A stronger research target: classification under constrained interventions

The unrestricted quantum result is mathematically clean but leaves the response-null set trivial. A more ambitious CNCS program should identify a physically justified intervention model under which the classification is both nontrivial and useful.

### 11.1 Localized operational constraints

Let \\(\mathfrak I_A^{\mathrm{loc}}\\) denote a family of interventions whose implementation is localized to a spacetime region \\(\mathcal O_A\\), with the receiver's observables supported in a spacelike-separated region \\(\mathcal O_B\\).

The response functional becomes

\\[ R^{\mathrm{loc}}\_{A\rightarrow B}(\rho) = \sup\_{\mathcal E\in\mathfrak I_A^{\mathrm{loc}}} \frac12 \left\\| \rho_B^{\mathcal E}-\rho_B \right\\|\_1. \\]

If the localization assumptions are physically consistent with the field theory, one expects no-signaling for admissible operations across spacelike-separated regions. But the exact admissibility conditions must be part of the model. They cannot be replaced by the unqualified assertion that every abstract channel is physically localizable.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. D

+1



The potential research objective is then not merely to show that \\(R^{\mathrm{loc}}=0\\), but to classify the correlations that remain invariant under a specified set of localized operations, including their dependence on region size, accessible observables, and experimental resolution.

### 11.2 Intervention-invariant correlation profiles

Define the profile of a state under an intervention family as

\\[ \mathcal P\_\rho: \mathfrak I_A\times\mathfrak A_A\times\mathfrak A_B \longrightarrow\mathbb R, \\]

where, for example,

\\[ \mathcal P\_\rho(\mathcal E;A,B) = C\_{(\mathcal E\otimes\operatorname{id})(\rho)}(A,B). \\]

One can then ask whether the entire profile, or a finite set of its invariants, distinguishes physically inequivalent states.

This is a stronger problem than evaluating one correlation before and after one intervention. It compares the state’s full correlation response surface over an admissible family of operations.

A possible classification strategy is:

1. Specify the physically realizable intervention family.
2. Identify a generating set of local observables.
3. Construct the correlation profile over the allowed operations.
4. Quotient states by a physically motivated equivalence relation.
5. Search for invariant functionals that separate the quotient classes.
6. Prove completeness on a finite-dimensional or otherwise controlled subclass.
7. Extend the result only where the proof assumptions remain valid.

The central obstacle is completeness. A rich profile can still fail to distinguish states if the allowed observables are not tomographically complete or if the intervention family has symmetries that erase relevant information.

### 11.3 A possible classification hierarchy

For a finite-dimensional bipartite system, the first candidate descriptors could be

\\[ J_1(\rho)=K\_{\mathrm{CNCS}}(\rho), \\]

\\[ J_2(\rho)=\operatorname{spec}(\rho\_{AB}), \\]

\\[ J_3(\rho)=\operatorname{spec}(\rho_A),\\; \operatorname{spec}(\rho_B), \\]

\\[ J_4(\rho)=I(A:B)\_\rho, \\]

together with selected entanglement witnesses and higher-order correlation tensors.

These quantities are not claimed to form a complete invariant set. They are candidate diagnostics whose redundancy, sufficiency, and stability must be analyzed under the chosen equivalence relation.

A genuinely new result would require proving that a proposed combination separates a meaningful family of CNCS classes, or that it reveals a structural constraint not captured by existing classification methods.

## 12. Experimental program

### 12.1 Objective

The experiment should estimate two quantities independently:

\\[ \text{correlation strength} \qquad\text{and}\qquad \text{remote intervention response}. \\]

A correlation witness must not be used as evidence of a causal response, and a null response must not be treated as proof that the joint state is uncorrelated.

The core protocol is a controlled comparison between joint outcome statistics and the local outcome distribution under alternative remote settings.

### 12.2 Experimental sequence

1\. Prepare a bipartite state

Prepare a family of states \\(\rho\_{AB}(\lambda)\\) with a controlled correlation parameter \\(\lambda\\), including an uncorrelated baseline and one or more correlated states.

2\. Randomize the intervention

Select the intervention setting at \\(A\\) independently of the measurement setting at \\(B\\). Include the appropriate control trials and randomization checks.

3\. Estimate correlation witnesses

Reconstruct the relevant connected-correlation tensor or estimate a prespecified witness from joint outcome counts.

4\. Estimate response bounds

Compare the receiver's outcome distributions across intervention settings and calculate a confidence region for the maximum tested response.

5\. Audit the causal interpretation

Check for ordinary communication leakage, shared timing signals, detector cross-talk, setting-dependent loss, postselection bias, and imperfections in the claimed intervention localization.

### 12.3 Correlation witness

For qubits, estimate

\\[ T\_{ij} = \langle\sigma_i\otimes\sigma_j\rangle - \langle\sigma_i\otimes I\rangle \langle I\otimes\sigma_j\rangle. \\]

Then compute

\\[ K\_{\mathrm{Pauli}} = \sqrt{\sum\_{i,j}T\_{ij}^2}. \\]

This witness is zero for product states and positive for states with nonzero connected Pauli correlations. It does not by itself distinguish classical from quantum correlations.

Where the scientific question concerns Bell nonlocality, an appropriate Bell inequality should be included as a separate witness. Where it concerns entanglement, an entanglement witness or a suitable state-reconstruction procedure should be included. These are distinct experimental questions.

### 12.4 Intervention-response bound

For each receiver setting \\(y\\), estimate the conditional distributions

\\[ \widehat p(b\mid x,y), \qquad \widehat p(b\mid x',y). \\]

Compute

\\[ \widehat\Delta\_{\mathrm{NS}} = \max\_{x,x',y} \frac12\sum_b \left| \widehat p(b\mid x,y) - \widehat p(b\mid x',y) \right|. \\]

The point estimate is not sufficient. The experiment should report a statistical confidence region that accounts for finite samples and relevant systematic uncertainty. If many settings are tested, the procedure must also control the error associated with searching over multiple comparisons.

A result consistent with zero should be reported as an upper bound on the tested response, not as a proof that no possible intervention can ever produce a response.

### 12.5 Spacelike separation and timing

For a specifically relativistic test, the intervention and measurement events must be arranged so that their relevant spacetime regions are spacelike separated, with a timing margin that accounts for uncertainty in event localization and apparatus latency.

The analysis should distinguish:

- Spacelike-separated intervention: the causal relation is constrained by the experimental spacetime arrangement.
- Delayed statistical comparison: data may be compared after the experiment without changing the causal status of the original events.
- Ordinary classical communication: information exchanged after the events can support data analysis but cannot retroactively make the original spacelike events causally connected.

A convincing experiment should document the causal geometry and the operational meaning of each intervention rather than relying on a statement that the detectors were merely far apart.

### 12.6 What would count as a result?

A basic result would be a statistically significant nonzero correlation witness accompanied by a well-calibrated upper bound on remote intervention response.

That would demonstrate consistency with the CNCS pattern in the tested regime. It would not, on its own, demonstrate a new correlation class.

A stronger result would identify two or more states that:

1. Satisfy the same declared causal-null constraints.
2. Are inequivalent under a stated physical or operational criterion.
3. Have different values of a proposed CNCS invariant.
4. Cannot be distinguished by a specified lower-level set of conventional diagnostics, but can be distinguished by the new invariant.
5. Exhibit the predicted behavior under a prespecified family of interventions.

The fifth condition is important. A classification that predicts only data already used to define its classes may be mathematically valid but experimentally uninformative.

## 13. Falsifiability and failure conditions

CNCS should be treated as a mathematical research program with explicit failure conditions, not as an interpretive label that can accommodate every possible outcome.

### 13.1 Failure of a proposed invariant

Suppose a proposed invariant \\(J\\) is claimed to distinguish two classes of causal-null states. The claim fails if there exist states \\(\rho\not\sim\sigma\\) such that

\\[ J(\rho)=J(\sigma), \\]

unless the theorem is explicitly limited to a narrower domain.

This would not refute the general coexistence of correlation and no-signaling. It would refute the completeness claim for that invariant.

### 13.2 Failure of stability

If arbitrarily small changes in experimentally accessible statistics lead to uncontrolled changes in the inferred classification, the proposed classification may be unsuitable for experimental use.

The remedy could be a weaker equivalence relation, a coarser classification, a regularized estimator, or an explicit statement that the result is valid only away from singular boundaries.

### 13.3 Failure of operational closure

A proposed intervention family may omit physically implementable operations or include operations that cannot be implemented under the stated physical constraints. If the classification depends on such an omission or inclusion, its physical interpretation fails.

The intervention domain must therefore be justified independently of the result it is used to obtain.

### 13.4 An observed nonzero remote response

A statistically reliable remote response in a spacelike-separated experiment would require careful investigation. Potential explanations include ordinary leakage, incorrect localization assumptions, postselection, detector cross-talk, or a genuine departure from the assumed operational theory.

It would not immediately establish superluminal causation. The analysis would need to exclude conventional channels and verify that the observed dependence is controllable, reproducible, and consistent with the experimental causal geometry.

### 13.5 No novelty after classification

A final failure condition is intellectual rather than experimental: if the proposed classification is shown to be equivalent to an established state classification or to a direct consequence of known results under the same assumptions, then the novelty claim must be withdrawn.

A useful framework can still be valuable as a synthesis or a more efficient representation. It must simply be presented as such rather than as a newly discovered physical structure.

## 14. Novelty assessment

### 14.1 What is already established

The following elements are established within standard quantum theory or related operational frameworks:

- Nonzero joint correlations can coexist with no-signaling.
- Local trace-preserving quantum operations leave the remote reduced state unchanged.
- Bell correlations can violate Bell-local factorization without enabling controllable superluminal communication.
- Correlation witnesses, state tomography, and quantum-information invariants can distinguish different joint-state structures.
- Relativistic localization imposes additional constraints on which abstract operations can be regarded as physically implementable in spacetime.

These points are documented in the standard literature on Bell nonlocality, quantum correlations, tomography, and relativistic quantum operations.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://plato.stanford.edu\&sz=32)

Stanford Encyclopedia of Philosophy

+3



### 14.2 What the present framework contributes

The framework makes three useful methodological contributions.

First, it defines correlation and intervention response as separate mathematical objects, avoiding the common error of treating nonfactorization as proof of causal influence.

Second, it makes the allowed intervention family explicit and shows why that specification matters: unrestricted local CPTP operations produce a universal zero-response condition, whereas a nontrivial classification may require a more physically specific operational model.

Third, it formulates the proposed discovery target as a family-level classification problem over the response-null set, with explicit requirements for invariance, completeness, stability, and operational meaning.

These are legitimate components of a research framework. They do not, by themselves, establish that CNCS is a previously undiscovered physical structure.

### 14.3 What would constitute a substantive discovery?

The strongest prospective contributions are:

A. A nontrivial classification theorem. Prove that a physically motivated causal-null sector admits a set of invariants that is complete under a clearly defined equivalence relation.

B. A new structural invariant. Construct a correlation invariant that captures physically meaningful information not captured by existing diagnostics under the same assumptions.

C. A sharp correlation-response bound. Derive a nontrivial inequality constraining correlation structure and response under a specified theory, rather than merely restating the no-signaling condition.

D. A new operational signature. Identify a family of experiments whose outcomes distinguish proposed CNCS classes and demonstrate why the signature cannot be reduced to an already-known classification.

Each contribution would require a literature audit before being described as novel. The names of the proposed framework and its invariants are provisional research terminology, not evidence of prior absence from the literature.

## 15. Limitations

Several limitations are fundamental to the present formulation.

Dependence on the operational model. The response functional depends on which interventions and observables are allowed. Two models with different operational domains can assign different causal-null sectors to the same underlying state space.

Dependence on the correlation witness. A nonzero connected-correlation norm is not equivalent to entanglement, Bell nonlocality, or any particular causal interpretation. Different witnesses answer different questions.

No ontological conclusion from no-signaling alone. A vanishing operational response does not prove that correlations have no deeper causal explanation or that the universe contains no underlying mediator.

Finite-dimensional starting point. The explicit theorem and examples above use finite-dimensional quantum systems. Extending the classification to quantum fields, infinite-dimensional Hilbert spaces, algebraic quantum field theory, or generalized probabilistic theories requires appropriate domain, topology, and localization assumptions.

Classification remains open. No complete CNCS invariant set is established here. The proposed classification conjecture is a target for subsequent mathematical work, not a theorem proved by the present paper.

No claim of empirical discovery. The paper defines a framework and derives elementary consequences of standard quantum mechanics. It reports no new experimental observation.

These limitations are not peripheral qualifications. They determine what CNCS can validly claim and what work remains necessary.

## 16. Conclusion

The Causal-Null Correlation Structure framework begins with a precise distinction: the existence of a correlation is a property of a joint-state distribution, whereas causal response is a property of how observable statistics change under a specified family of interventions.

The formal condition

\\[ K\_{\mathrm{CNCS}}(\rho)>0, \qquad R\_{A\rightarrow B}(\rho;\mathfrak I_A)=0 \\]

captures this distinction, but the condition alone does not define a new physical phenomenon. Under standard quantum mechanics, every bipartite state has zero remote response to local nonselective CPTP operations. The resulting causal-null sector is therefore universal in that model.

The meaningful research problem is the classification of correlation structures within that sector. Such a classification must specify its equivalence relation, establish its invariants, prove their separating power, and demonstrate that the resulting classes possess operational or physical significance beyond existing state-classification methods.

The immediate mathematical program is consequently:

1. Fix a physically justified intervention family.
2. Construct the associated response-null sector.
3. Define a precise equivalence relation on that sector.
4. Search for correlation invariants that separate its equivalence classes.
5. Prove completeness or explicitly characterize the unresolved degeneracies.
6. Derive stability bounds for finite-precision measurements.
7. Design experiments that test predictions not already built into the definitions.

The principal conjecture is that some physically constrained operational models may admit a useful classification of correlation structures that remain invariant under all interventions in the permitted family. Whether such a classification yields genuinely new invariants, sharp bounds, or experimentally distinguishable classes remains to be determined.

The central result of this paper is therefore a precise formulation of the research problem, together with its elementary quantum-theoretic foundation and the identification of the triviality obstruction that any substantive classification must overcome. The next advance must be a theorem or experimentally testable bound—not merely a new name for the established coexistence of quantum correlation and no-signaling.

## References and further reading

1\. J. S. Bell, “On the Einstein Podolsky Rosen Paradox,” Physics Physique Fizika 1, 195–200 (1964). [Original paper](https://doi.org/10.1103/PhysicsPhysiqueFizika.1.195?utm_source=chatgpt.com).

2\. J. F. Clauser, M. A. Horne, A. Shimony, and R. A. Holt, “Proposed Experiment to Test Local Hidden-Variable Theories,” Physical Review Letters 23, 880–884 (1969). [Original paper](https://doi.org/10.1103/PhysRevLett.23.880?utm_source=chatgpt.com).

3\. N. Brunner et al., “Bell nonlocality,” Reviews of Modern Physics 86, 419–478 (2014). [Review](https://doi.org/10.1103/RevModPhys.86.419?utm_source=chatgpt.com).

4\. C. Brukner and collaborators, “Relativistic Consistency of Nonlocal Quantum Correlations.” [Open-access article](https://pmc.ncbi.nlm.nih.gov/articles/PMC11275346/?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC



5\. “Causal Networks and Freedom of Choice in Bell's Theorem,” PRX Quantum. [Article](https://doi.org/10.1103/PRXQuantum.2.040323?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

PRX Quantum



6\. “Nonlocality, Steering, and Quantum State Tomography in a Single Experiment,” Physical Review Letters 127, 020401 (2021). [Article](https://doi.org/10.1103/PhysRevLett.127.020401?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. Lett.



7\. “Factorization conditions and causality for local measurements in QFT,” Physical Review D 114, 085013 (2026). [Article](https://doi.org/10.1103/sxkx-sy9g?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. D

+1



8\. “Efficiently Learning Global Quantum Channels with Local Tomography,” PRX Quantum (2026). [Article](https://doi.org/10.1103/51mt-ghpn?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

PRX Quantum



The references provide background for the established results and adjacent research areas. They do not constitute an exhaustive novelty audit of the proposed CNCS classification.

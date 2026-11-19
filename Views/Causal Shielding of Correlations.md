# Causal Shielding of Correlations (CSC)

## A Mathematical Framework for Intervention-Invariant Relational Structure in Composite Quantum Systems

Research classification: Foundational mathematical physics; quantum information; operational theory of correlations; symmetry and invariant dynamics.

Central thesis: A composite system may possess joint correlation structures that remain invariant under a specified family of local interventions, even though those structures remain distinguishable through joint measurements. Such invariance is stronger than ordinary no-signaling, but it is not, by itself, evidence of a new nonlocal mechanism or an absolute prohibition against local control.

The proposed framework, Causal Shielding of Correlations (CSC), seeks to classify these structures by three related questions:

1. Which joint correlation functionals are invariant under a given family of local transformations?
2. Which transformations preserve, destroy, or expose those invariants?
3. Under what conditions can invariant correlation structure coexist with operationally distinguishable global states?

The decisive mathematical distinction is between invariance of a relational quantity and invariance of the entire joint state. A functional may be shielded while the state changes substantially. Conversely, a state may remain distinguishable under joint measurements even when every locally accessible marginal remains unchanged.

A rigorous CSC theory must therefore specify its transformation class, its correlation functional, its measurement algebra, and the equivalence relation under which shielding is asserted. Without those specifications, the word shielding would merely rename familiar symmetry invariance.

## Abstract

We formulate Causal Shielding of Correlations as an operational and mathematical classification problem for composite systems subject to local transformations. Let \\(\mathcal H=\mathcal H_A\otimes\mathcal H_B\\) be a bipartite Hilbert space and let \\(\mathfrak G\\) be a specified family of admissible local quantum channels. A correlation functional \\(K\\) is said to be shielded relative to \\(\mathfrak G\\) on a state domain \\(\mathcal D\\) if

\\[ K\\!\left[ (\mathcal E_A\otimes\mathcal E_B)(\rho) \right] = K(\rho) \\]

for every \\(\rho\in\mathcal D\\) and every \\((\mathcal E_A,\mathcal E_B)\in\mathfrak G\\).

We distinguish this property from no-signaling, which constrains changes in remote marginal statistics, and from ordinary symmetry invariance, which generally concerns a specified group representation. We introduce exact, approximate, directional, conditional, and measurement-relative forms of shielding; characterize their algebraic structure; and derive conditions under which local transformations preserve, degrade, or erase relational information.

Several established mathematical results provide the foundation. Local-unitary invariance of entanglement measures, invariance of mutual information under local unitaries, and decoherence-free subspaces are known. We show how these results fit within a common operational classification, while identifying the additional conditions required for a genuinely new CSC invariant family.

A particularly important result is that invariance under all independent local unitary transformations is extremely restrictive for a scalar functional on the full bipartite state space. Such a functional can depend only on the local-unitary orbit of the state. Invariance under a larger family of local channels is more restrictive still. This yields a natural hierarchy of shielding classes and an obstruction to claims of universal correlation protection.

We propose a falsifiable experimental programme based on controlled local channels, joint correlation measurements, intervention families, and independently calibrated residual interactions. The framework's principal research target is a nontrivial classification theorem identifying the maximal local transformation families that preserve a given relational invariant, together with the transformations that break or reveal it.

Keywords: quantum correlations; local interventions; invariant functionals; no-signaling; local channels; symmetry; decoherence-free structures; operational distinguishability; correlation robustness.

# Part I — Conceptual and operational foundations

## 1. Introduction

A composite physical system can exhibit joint properties that are not reducible to the properties of its individual components. Quantum entanglement is the most familiar example, but the broader class includes classical correlations, mutual information, multipartite constraints, and network-dependent relational quantities.

The central question addressed here is not whether correlations can exist without continuous communication. That issue is already addressed by quantum no-signaling and the theory of local operations.

The question is more specific:

Can a joint correlation functional remain invariant under a broad and explicitly defined family of local transformations, even when the joint state remains globally distinguishable?

This question introduces a distinction between three forms of stability:

- Marginal stability: local operations on one subsystem do not change the unconditioned marginal statistics of the other.
- State stability: the joint density operator remains unchanged.
- Relational stability: a specified functional of the joint state remains unchanged, even if the density operator itself changes.

CSC concerns the third category.

A correlation may survive an intervention without the state being preserved. A state may change under local operations while retaining a particular invariant. Conversely, a correlation may be destroyed without producing any detectable remote signal.

The proposed framework treats these possibilities as distinct mathematical objects.

### 1.1 The central research question

Let \\(A\\) and \\(B\\) be subsystems, and let \\(\mathcal E_A\\) and \\(\mathcal E_B\\) be local transformations. The transformed state is

\\[ \rho'\_{AB} = (\mathcal E_A\otimes\mathcal E_B)(\rho\_{AB}). \\]

We seek functionals \\(K\\) satisfying

\\[ \boxed{ K(\rho'\_{AB})=K(\rho\_{AB}) } \\]

for a nontrivial family of local interventions.

The word nontrivial matters. The identity transformation preserves every functional. A useful shielding theorem must identify a family containing physically meaningful transformations beyond the identity and characterize what makes preservation possible.

### 1.2 What CSC does not assume

The framework does not assume:

1. that correlations constitute a physical substance;
2. that all correlations are quantum entanglement;
3. that local transformations are incapable of changing global relational structure;
4. that invariance implies a hidden mediator;
5. that no-signaling proves absolute causal independence;
6. that every symmetry invariant is a new physical discovery.

The intended contribution is a classification of operationally defined invariant correlation structures, not a new ontology of correlation.

## 2. Mathematical setting

Let the composite system be

\\[ \mathcal H\_{AB} = \mathcal H_A\otimes\mathcal H_B, \\]

with

\\[ \dim\mathcal H_A=d_A,\qquad \dim\mathcal H_B=d_B. \\]

A physical state is represented by a density operator

\\[ \rho\_{AB}\in\mathcal D(\mathcal H\_{AB}), \\]

where

\\[ \rho\_{AB}\geq0,\qquad \operatorname{Tr}\rho\_{AB}=1. \\]

The reduced states are

\\[ \rho_A=\operatorname{Tr}\_B\rho\_{AB}, \qquad \rho_B=\operatorname{Tr}\_A\rho\_{AB}. \\]

The space of Hermitian operators on \\(\mathcal H\_{AB}\\) is denoted

\\[ \operatorname{Herm}(\mathcal H\_{AB}). \\]

The set of completely positive trace-preserving maps on subsystem \\(A\\) is

\\[ \operatorname{CPTP}(A), \\]

and similarly for \\(B\\).

A local product channel is

\\[ \mathcal E\_{AB} = \mathcal E_A\otimes\mathcal E_B. \\]

The restriction to product channels is deliberate. It excludes, at the level of the stipulated intervention model, a direct joint operation implemented by a shared entangling gate.

It does not automatically exclude common environmental influence or correlated noise. Those require separate treatment.

### 2.1 Correlation functionals

A correlation functional is a map

\\[ K:\mathcal D(\mathcal H\_{AB})\rightarrow\mathcal K, \\]

where \\(\mathcal K\\) may be \\(\mathbb R\\), \\(\mathbb C\\), a vector space, or a structured set of invariants.

Examples include:

- mutual information;
- quantum discord;
- concurrence;
- negativity;
- covariance;
- Bell-inequality violation;
- correlation tensors;
- multipartite polynomial invariants;
- network correlation functionals.

The definition of \\(K\\) must include its measurement and optimization conventions. A quantity optimized over measurement settings is not generally equivalent to the same quantity evaluated at fixed settings.

## 3. Definition of causal shielding

Let \\(\mathfrak G\\) be a specified family of local intervention pairs:

\\[ \mathfrak G \subseteq \operatorname{CPTP}(A)\times \operatorname{CPTP}(B). \\]

Let \\(\mathcal D\subseteq\mathcal D(\mathcal H\_{AB})\\) be the domain of states under consideration.

Definition 1 — Exact causal shielding.

A correlation functional \\(K\\) is exactly shielded relative to \\(\mathfrak G\\) on \\(\mathcal D\\) if

\\[ \boxed{ K\\!\left[ (\mathcal E_A\otimes\mathcal E_B)(\rho) \right] = K(\rho) } \\]

for all

\\[ \rho\in\mathcal D,\qquad (\mathcal E_A,\mathcal E_B)\in\mathfrak G. \\]

We write

\\[ K\in\operatorname{Inv}(\mathfrak G;\mathcal D). \\]

The dependence on \\(\mathfrak G\\) and \\(\mathcal D\\) is essential. A functional may be invariant under local unitaries but not under local dephasing. It may be invariant on a decoherence-free subspace but not on the full state space.

Accordingly, the expression

\\[ K(\mathcal E_A,\mathcal E_B;\rho)=K(\rho) \\]

must be interpreted as shorthand for evaluation on the transformed state, not as an independent three-variable physical law.

### 3.1 Shielding is relative, not absolute

The adjective causal refers to the operational setting in which interventions are applied locally and their effects are examined in joint relational observables.

It does not establish that the invariant is protected from every possible causal influence.

The correct statement is:

\\[ \text{Invariant relative to a specified intervention family.} \\]

Not:

\\[ \text{Invariant under all conceivable physical processes.} \\]

### 3.2 The identity requirement

If \\(\mathfrak G\\) contains only identity channels, every functional is shielded. This is mathematically valid but scientifically empty.

A meaningful CSC result should satisfy at least one of the following:

1. \\(\mathfrak G\\) contains a continuous family of nonidentity channels;
2. \\(\mathfrak G\\) contains experimentally realizable transformations;
3. \\(\mathfrak G\\) contains a physically motivated symmetry group;
4. \\(\mathfrak G\\) contains a noise class with independently measurable parameters;
5. \\(\mathfrak G\\) is maximal among transformations preserving \\(K\\).

The fifth criterion is especially important because it turns shielding into a classification problem.

# Part II — The hierarchy of shielding

## 4. Intervention families and their algebraic structure

Different intervention families generate different notions of invariance.

We distinguish:

\\[ \mathfrak G_U \subseteq \mathfrak G\_{\mathrm{LO}} \subseteq \mathfrak G\_{\mathrm{CPTP}}, \\]

where:

- \\(\mathfrak G_U\\) contains independent local unitary channels;
- \\(\mathfrak G\_{\mathrm{LO}}\\) contains a specified family of local operations;
- \\(\mathfrak G\_{\mathrm{CPTP}}\\) contains all independent local CPTP channels.

These are conceptual classes, not a claim that every experimental local operation is represented by a single deterministic channel. Selective measurements and postselection require an instrument-level formulation.

### 4.1 Group actions

If the allowed transformations are reversible, they form or represent a group \\(G\\).

For a unitary representation,

\\[ g=(U_A,U_B), \\]

with action

\\[ \alpha_g(\rho) = (U_A\otimes U_B)\rho (U_A^\dagger\otimes U_B^\dagger). \\]

The orbit of \\(\rho\\) is

\\[ \mathcal O_G(\rho) = \\{\alpha_g(\rho):g\in G\\}. \\]

A functional is invariant under \\(G\\) precisely when it is constant on every orbit:

\\[ K(\alpha_g(\rho))=K(\rho). \\]

Thus a group-invariant functional factors through the orbit space:

\\[ \mathcal D/G. \\]

This is the standard mathematical meaning of symmetry invariance.

### 4.2 Semigroups of channels

General CPTP maps are not invertible. They therefore do not generally form a group.

The appropriate structure is a semigroup under composition.

If

\\[ \mathcal E_1,\mathcal E_2\in\mathfrak S, \\]

then closure requires

\\[ \mathcal E_2\circ\mathcal E_1\in\mathfrak S. \\]

For bipartite product channels,

\\[ (\mathcal E_A^{(2)}\circ\mathcal E_A^{(1)}) \otimes (\mathcal E_B^{(2)}\circ\mathcal E_B^{(1)}) \\]

is again a product channel.

A semigroup-invariant functional is constant along the reachable state trajectories generated by the semigroup.

This is stronger than invariance under one particular channel but need not imply invariance under the inverse transformation, which may not exist.

## 5. A strict hierarchy of shielding conditions

We define five useful levels.

### Level I — Unitary shielding

\\[ K[(U_A\otimes U_B)\rho(U_A^\dagger\otimes U_B^\dagger)] = K(\rho). \\]

This is familiar for many entanglement measures.

### Level II — Symmetry-restricted shielding

The equality holds for a subgroup

\\[ G\subseteq U(d_A)\times U(d_B). \\]

This permits invariants associated with restricted local symmetries, including conserved charges and representation-theoretic structure.

### Level III — Noise-class shielding

The equality holds for a physically specified class of nonunitary local channels, such as dephasing within a protected subspace.

### Level IV — Semigroup shielding

The equality holds for every finite composition of transformations in a specified local channel semigroup.

### Level V — Universal local-channel shielding

\\[ K[(\mathcal E_A\otimes\mathcal E_B)(\rho)] = K(\rho) \\]

for all local CPTP channels.

This is an exceptionally strong condition. For most nontrivial correlation measures, it is false.

The hierarchy implies that every proposed CSC invariant must be reported together with its shielding level. A result at Level II must not be described as universal local shielding.

## 6. Approximate causal shielding

Physical experiments have finite precision. Exact equality is therefore not the only useful condition.

Definition 2 — Approximate shielding.

For a metric \\(d\_{\mathcal K}\\) on the range of \\(K\\), \\(K\\) is \\(\varepsilon\\)-shielded relative to \\(\mathfrak G\\) on \\(\mathcal D\\) if

\\[ \boxed{ d\_{\mathcal K} \left( K[(\mathcal E_A\otimes\mathcal E_B)(\rho)], K(\rho) \right) \leq\varepsilon } \\]

for all admissible states and interventions.

For scalar real-valued functionals,

\\[ |K(\rho')-K(\rho)|\leq\varepsilon. \\]

We define the shielding defect

\\[ \boxed{ \Delta_K(\mathfrak G;\mathcal D) = \sup\_{\substack{\rho\in\mathcal D\\\ (\mathcal E_A,\mathcal E_B)\in\mathfrak G}} \left| K[(\mathcal E_A\otimes\mathcal E_B)(\rho)] -K(\rho) \right|. } \\]

Exact shielding corresponds to

\\[ \Delta_K=0. \\]

This definition is operationally useful because it provides a single quantity for comparing candidate invariants.

### 6.1 Relative shielding defect

When \\(K\\) can be small or vanish, an absolute defect may obscure relative changes. For a domain where \\(|K(\rho)|\\) is bounded away from zero, define

\\[ \Delta_K^{\mathrm{rel}} = \sup\_{\rho,\mathcal E} \frac{|K(\mathcal E(\rho))-K(\rho)|} {|K(\rho)|}. \\]

The domain restriction is necessary to avoid division by zero.

### 6.2 State-dependent shielding

A functional may be shielded only on a subset

\\[ \mathcal D_0\subset\mathcal D. \\]

For example, a decoherence-free subspace can preserve encoded information under a restricted noise model, while states outside that subspace decay.

Such a result is legitimate CSC, provided the protected domain and noise model are stated explicitly.

# Part III — The relation to no-signaling and joint distinguishability

## 7. No-signaling is not correlation shielding

The distinction between no-signaling and CSC is foundational.

For a local trace-preserving operation \\(\mathcal E_A\\),

\\[ \rho'\_{AB} = (\mathcal E_A\otimes\mathcal I_B)(\rho\_{AB}). \\]

The remote marginal is

\\[ \rho'\_B = \operatorname{Tr}\_A [(\mathcal E_A\otimes\mathcal I_B)(\rho\_{AB})]. \\]

Using a Kraus representation,

\\[ \mathcal E_A(X) = \sum\_\alpha K\_\alpha X K\_\alpha^\dagger, \\]

with

\\[ \sum\_\alpha K\_\alpha^\dagger K\_\alpha=I_A, \\]

we obtain

\\[ \begin{aligned} \rho'\_B &= \sum\_\alpha \operatorname{Tr}\_A[ (K\_\alpha\otimes I) \rho\_{AB} (K\_\alpha^\dagger\otimes I) ]\\\ &= \operatorname{Tr}\_A[ \rho\_{AB} (\sum\_\alpha K\_\alpha^\dagger K\_\alpha\otimes I) ]\\\ &= \operatorname{Tr}\_A(\rho\_{AB})\\\ &=\rho_B. \end{aligned} \\]

Therefore,

\\[ \boxed{\rho'\_B=\rho_B.} \\]

This is the usual no-signaling result for deterministic local operations.

However, it does not imply

\\[ K(\rho'\_{AB})=K(\rho\_{AB}). \\]

A local channel may alter entanglement, mutual information, discord, or joint covariance while leaving the remote marginal unchanged.

Hence:

\\[ \boxed{ \text{No-signaling}\not\Rightarrow\text{correlation shielding}. } \\]

### 7.1 Explicit counterexample: local dephasing

Consider the Bell state

\\[ |\Phi^+\rangle = \frac{|00\rangle+|11\rangle}{\sqrt2}, \\]

with density operator

\\[ \rho\_{\Phi^+} = |\Phi^+\rangle\langle\Phi^+|. \\]

Apply complete dephasing to subsystem \\(A\\):

\\[ \mathcal D_A(\rho) = \sum\_{j=0}^1 (|j\rangle\langle j|\otimes I) \rho (|j\rangle\langle j|\otimes I). \\]

Then

\\[ \rho'\_{AB} = \frac12|00\rangle\langle00| + \frac12|11\rangle\langle11|. \\]

The initial and final local marginals are identical:

\\[ \rho_A=\rho'\_A=\frac{I}{2}, \qquad \rho_B=\rho'\_B=\frac{I}{2}. \\]

But the entanglement changes:

\\[ C(\rho\_{\Phi^+})=1, \qquad C(\rho'\_{AB})=0. \\]

The mutual information also changes:

\\[ I(A:B)\_{\rho\_{\Phi^+}}=2\ \text{bits}, \\]

whereas

\\[ I(A:B)\_{\rho'\_{AB}}=1\ \text{bit}. \\]

Thus the local operation changes the joint correlation structure without changing either subsystem's unconditioned marginal.

This is a direct demonstration of why CSC is not merely a restatement of no-signaling.

## 8. Joint distinguishability and local indistinguishability

Let \\(\rho\\) and \\(\sigma\\) be two bipartite states.

They are locally indistinguishable by measurements on \\(A\\) alone if

\\[ \rho_A=\sigma_A. \\]

Likewise for \\(B\\).

But they may be distinguishable by a joint measurement \\(M\\):

\\[ \operatorname{Tr}(M\rho) \neq \operatorname{Tr}(M\sigma). \\]

The trace distance provides the optimal single-copy distinguishability:

\\[ D\_{\mathrm{tr}}(\rho,\sigma) = \frac12\\|\rho-\sigma\\|\_1. \\]

If

\\[ D\_{\mathrm{tr}}(\rho,\sigma)>0, \\]

then there exists a joint POVM that distinguishes them with nonzero bias.

### 8.1 A canonical example

Consider

\\[ \rho\_+ = |\Phi^+\rangle\langle\Phi^+|, \qquad \rho\_- = |\Phi^-\rangle\langle\Phi^-|, \\]

where

\\[ |\Phi^-\rangle = \frac{|00\rangle-|11\rangle}{\sqrt2}. \\]

Both states have the same reduced states:

\\[ (\rho\_+)\_A=(\rho\_-)\_A=\frac I2, \\]

\\[ (\rho\_+)\_B=(\rho\_-)\_B=\frac I2. \\]

Yet they are orthogonal:

\\[ \langle\Phi^+|\Phi^-\rangle=0. \\]

A joint measurement in the Bell basis distinguishes them perfectly.

This demonstrates that local marginal equality does not imply joint-state equality.

However, this example alone does not establish CSC. Under some local transformations the two states may cease to retain their original distinction, and a chosen invariant must be specified.

### 8.2 The correct CSC criterion

A candidate shielded functional \\(K\\) should be evaluated alongside a joint measurement family \\(\mathfrak M\_{AB}\\).

The relevant condition is not merely

\\[ K(\rho')=K(\rho), \\]

but the conjunction:

\\[ \boxed{ K(\rho')=K(\rho) \quad\text{and}\quad \exists M\in\mathfrak M\_{AB}: \operatorname{Tr}(M\rho)\neq \operatorname{Tr}(M\sigma). } \\]

The first condition establishes relational invariance. The second establishes that the global state space has not become operationally trivial.

The two conditions concern different comparisons: invariance of a functional along an intervention trajectory and distinguishability between states. They must not be conflated.

# Part IV — Established invariant families

## 9. Local-unitary invariants

Local unitary transformations have the form

\\[ \rho' = (U_A\otimes U_B)\rho (U_A^\dagger\otimes U_B^\dagger). \\]

Many established correlation measures are invariant under these transformations.

### 9.1 Entanglement measures

For a bipartite pure state, the Schmidt decomposition is

\\[ |\psi\rangle = \sum\_{i=1}^{r} \sqrt{\lambda_i} |a_i\rangle|b_i\rangle, \\]

where

\\[ \lambda_i\geq0,\qquad \sum_i\lambda_i=1. \\]

Local unitaries alter the Schmidt vectors but not the Schmidt coefficients.

Therefore, any entanglement functional depending only on the Schmidt spectrum is locally unitary invariant.

For example, the entropy of entanglement is

\\[ E(|\psi\rangle) = -\sum_i\lambda_i\log_2\lambda_i. \\]

Hence

\\[ E[(U_A\otimes U_B)|\psi\rangle] = E(|\psi\rangle). \\]

For mixed states, standard entanglement measures such as negativity and concurrence are also invariant under local unitaries.

This is an established result, not a new CSC discovery.

### 9.2 Mutual information

Quantum mutual information is

\\[ I(A:B)\_\rho = S(\rho_A)+S(\rho_B)-S(\rho\_{AB}), \\]

where

\\[ S(\rho)=-\operatorname{Tr}(\rho\log_2\rho). \\]

Under local unitaries, the spectra of \\(\rho_A\\), \\(\rho_B\\), and \\(\rho\_{AB}\\) are unchanged. Therefore,

\\[ \boxed{ I(A:B)\_{\rho'}=I(A:B)\_\rho. } \\]

Again, this is established local-unitary invariance.

### 9.3 Correlation tensors

For two qubits, write

\\[ \rho = \frac14 \left[ I\otimes I+ \mathbf a\cdot\boldsymbol\sigma\otimes I+ I\otimes\mathbf b\cdot\boldsymbol\sigma+ \sum\_{ij}T\_{ij}\sigma_i\otimes\sigma_j \right]. \\]

The correlation tensor is

\\[ T\_{ij} = \operatorname{Tr} (\rho\\,\sigma_i\otimes\sigma_j). \\]

Local unitaries induce rotations

\\[ \mathbf a\mapsto R_A\mathbf a, \qquad \mathbf b\mapsto R_B\mathbf b, \\]

and

\\[ T\mapsto R_A T R_B^{\mathsf T}, \\]

with \\(R_A,R_B\in SO(3)\\).

Consequently, the singular values of \\(T\\) are invariant under local unitaries.

The quantities

\\[ \operatorname{Tr}(TT^{\mathsf T}), \qquad \det T, \qquad \operatorname{Tr}[(TT^{\mathsf T})^2] \\]

are examples of local-unitary invariants, subject to the usual algebraic dependencies and state-positivity constraints.

These quantities offer a natural starting point for CSC because they are explicitly computable and experimentally reconstructible.

## 10. Invariance under nonunitary local channels

Local-unitary invariance is relatively weak. Nonunitary channels can erase correlations.

For example, a completely depolarizing channel on \\(A\\) is

\\[ \mathcal R_A(\rho) = \frac{I_A}{d_A}\otimes\operatorname{Tr}\_A(\rho). \\]

For any bipartite state,

\\[ (\mathcal R_A\otimes\mathcal I_B)(\rho) = \frac{I_A}{d_A}\otimes\rho_B. \\]

The output is a product state.

Thus every entanglement measure vanishes after this channel.

If a functional is claimed to be invariant under all local CPTP channels, it cannot be an ordinary entanglement measure on the full state space.

This observation leads to a useful obstruction theorem.

### Theorem 1 — Universal local replacement obstruction

Let \\(K\\) be a functional on the full bipartite state space. Suppose it is invariant under all product CPTP channels. Then \\(K\\) is constant on the full state space.

Proof.

Choose any two states \\(\rho,\sigma\\).

Apply the local replacement channel

\\[ \mathcal R\_{AB}^{\tau}(\cdot) = \tau_A\otimes\tau_B\\, \operatorname{Tr}(\cdot), \\]

where \\(\tau_A,\tau_B\\) are fixed density operators. This is a product of local replacement channels:

\\[ \mathcal R\_{AB}^{\tau} = \mathcal R_A^{\tau_A}\otimes \mathcal R_B^{\tau_B}. \\]

For every input state,

\\[ \mathcal R\_{AB}^{\tau}(\rho) = \tau_A\otimes\tau_B = \mathcal R\_{AB}^{\tau}(\sigma). \\]

By universal invariance,

\\[ K(\rho) = K(\tau_A\otimes\tau_B) = K(\sigma). \\]

Since \\(\rho,\sigma\\) were arbitrary,

\\[ \boxed{K(\rho)=\text{constant}.} \\]

\\(\square\\)

This theorem is decisive: universal local-channel shielding cannot support a nontrivial scalar correlation functional on the entire state space.

Any useful CSC invariant must therefore restrict the allowed intervention family, the state domain, or the functional's meaning.

## 11. A maximal local-unitary shielding theorem

We can make the local-unitary case precise.

Let

\\[ G\_{\mathrm{LU}} = U(d_A)\times U(d_B). \\]

### Theorem 2 — Local-unitary orbit characterization

A scalar functional \\(K\\) is invariant under all independent local unitaries if and only if it is constant on every local-unitary orbit.

Equivalently, there exists a function \\(f\\) on the orbit space such that

\\[ K(\rho)=f([\rho]\_{\mathrm{LU}}). \\]

Proof.

If \\(K\\) is invariant, then for any two states in the same orbit,

\\[ \sigma = (U_A\otimes U_B)\rho (U_A^\dagger\otimes U_B^\dagger), \\]

we have

\\[ K(\sigma)=K(\rho). \\]

Thus \\(K\\) is constant on each orbit and descends to the quotient space.

Conversely, if \\(K\\) depends only on the orbit class, local unitaries do not change that class, so \\(K\\) is invariant.

\\(\square\\)

This is a classification principle, not a new physical law. Its practical importance is that it constrains the form of every exact local-unitary CSC invariant.

A proposed invariant must either be expressible through local-unitary orbit data or demonstrate that the intervention family is smaller than the full local-unitary group.

# Part V — Candidate invariant constructions

## 12. Candidate I: Correlation-tensor spectral invariants

For a two-qubit state, the singular values of \\(T\\) are unchanged under local unitaries.

Let

\\[ s_1,s_2,s_3 \\]

be the singular values of the correlation tensor.

Define

\\[ K_T(\rho) = \operatorname{Tr}(TT^{\mathsf T}) = s_1^2+s_2^2+s_3^2. \\]

Then

\\[ K_T(\rho')=K_T(\rho) \\]

under all local unitaries.

A second invariant is

\\[ K\_{\det}(\rho)=\det T. \\]

These are straightforward candidates for a baseline CSC classification.

Their limitation is equally clear: they are generally not invariant under local nonunitary channels.

A useful discovery would not consist of rediscovering these invariants, but determining their maximal nonunitary stabilizer classes and experimentally relevant robustness bounds.

## 13. Candidate II: Protected-subspace invariants

Let \\(P\\) be a projector onto a protected subspace

\\[ \mathcal H\_{\mathrm{DFS}} \subseteq\mathcal H\_{AB}. \\]

A noise generator \\(\mathcal L\\) preserves the subspace if

\\[ \mathcal L(PXP) = P\mathcal L(PXP)P \\]

for all operators \\(X\\) supported on that subspace.

A stronger noiseless-subsystem condition may be expressed as an encoded factorization:

\\[ \mathcal H\_{\mathrm{DFS}} \simeq \mathcal H_L\otimes\mathcal H_G, \\]

where the noise acts trivially on the logical subsystem:

\\[ \mathcal E(\rho_L\otimes\rho_G) = \rho_L\otimes\mathcal E_G(\rho_G). \\]

Then every logical-state invariant remains preserved under the stipulated noise class.

This is established decoherence-free-subspace and noiseless-subsystem theory.

CSC may contribute a broader classification if it identifies relational functionals preserved even when no full noiseless logical subsystem exists.

That is a genuine research question, not a result assumed here.

## 14. Candidate III: Relative entropy of correlation

Define

\\[ I(A:B)\_\rho = D(\rho\_{AB}\\| \rho_A\otimes\rho_B), \\]

where

\\[ D(\rho\\|\sigma) = \operatorname{Tr}[\rho(\log\rho-\log\sigma)]. \\]

This is quantum mutual information.

For local CPTP maps,

\\[ I(A:B)\_{(\mathcal E_A\otimes\mathcal E_B)(\rho)} \leq I(A:B)\_\rho \\]

by the data-processing inequality.

Therefore, mutual information is generally not shielded under arbitrary local channels. It is instead a monotone.

This suggests a broader CSC classification:

- invariants: unchanged under a transformation class;
- monotones: constrained to move in one direction;
- covariants: transform according to a known representation;
- destructible quantities: can be driven to zero by an allowed intervention.

A framework that treats all these categories separately is more informative than one that labels every robust quantity “shielded.”

## 15. Candidate IV: Stabilizer-based relational functionals

Let \\(\mathfrak G\\) be a transformation group acting on the state space.

Define the stabilizer of a state:

\\[ \operatorname{Stab}\_{\mathfrak G}(\rho) = \\{g\in\mathfrak G:\alpha_g(\rho)=\rho\\}. \\]

A relational invariant may depend on the stabilizer structure rather than directly on the state.

For example,

\\[ K\_{\mathrm{stab}}(\rho) = \dim\operatorname{Stab}\_{\mathfrak G}(\rho) \\]

is invariant under conjugation within the group action when the appropriate representation and regularity conditions hold.

However, this is primarily a state-symmetry invariant, not automatically a correlation measure.

To qualify as a CSC correlation invariant, one must show that it distinguishes relational structure rather than merely local symmetry or degeneracy.

A stronger candidate is the dimension or structure of the subgroup preserving a chosen correlation tensor:

\\[ \operatorname{Stab}\_{\mathfrak G}(T) = \\{g\in\mathfrak G:\alpha_g(T)=T\\}. \\]

This can distinguish correlation patterns with identical scalar norms but different symmetry structures.

Its novelty depends on whether the resulting classification exceeds known tensor-orbit and representation-theoretic classifications.

## 16. Candidate V: Intervention-spectrum invariants

We now introduce a possible research construction.

Let \\(\mathfrak G=\\{\mathcal E\_\lambda\\}\\) be a parameterized family of local channels. For a fixed state \\(\rho\\) and correlation functional \\(K\\), define the intervention response function

\\[ \kappa\_\rho(\lambda) = K[\mathcal E\_\lambda(\rho)]. \\]

This is the intervention profile of the correlation functional.

Two states \\(\rho,\sigma\\) are intervention-equivalent with respect to \\(K\\) and \\(\mathfrak G\\) if

\\[ \kappa\_\rho(\lambda) = \kappa\_\sigma(\lambda) \qquad \forall\lambda. \\]

This is stronger than equality at the identity transformation.

The profile can be characterized by moments or derivatives when the channel family is differentiable:

\\[ m_n(\rho) = \left. \frac{d^n}{d\lambda^n} K[\mathcal E\_\lambda(\rho)] \right|\_{\lambda=0}. \\]

A state may have a nonzero correlation functional but vanish under all first-order intervention responses:

\\[ m_1(\rho)=0. \\]

This is a form of first-order robustness, not exact shielding.

A candidate intervention-spectrum invariant is

\\[ K\_{\mathrm{spec}}(\rho) = \\{m_0(\rho),m_1(\rho),m_2(\rho),\ldots\\}. \\]

This object records the local response profile rather than merely the value of a correlation functional.

It may be useful for classifying correlations that are indistinguishable under a chosen intervention family.

Novelty status: Proposed construction. Its independent novelty has not been established. Functional response spectra and derivatives of parameterized channels are related to established process characterization and perturbation theory.

# Part VI — Theorems and structural results

## 17. The shielding algebra

Let

\\[ \mathcal I(\mathfrak G;\mathcal D) = \\{K:K(\mathcal E(\rho))=K(\rho) \text{ for all }\rho\in\mathcal D,\mathcal E\in\mathfrak G\\}. \\]

This is the set of exact invariant functionals.

### Theorem 3 — Closure under functional composition

If \\(K\in\mathcal I(\mathfrak G;\mathcal D)\\) and \\(f\\) is any well-defined function on the range of \\(K\\), then

\\[ f\circ K\in\mathcal I(\mathfrak G;\mathcal D). \\]

Proof.

For every admissible transformation,

\\[ f(K(\mathcal E(\rho))) = f(K(\rho)). \\]

Therefore \\(f\circ K\\) is invariant.

\\(\square\\)

This means the invariant family is generally not unique. Arbitrary reparameterizations generate further invariants. Novelty must therefore be assessed at the level of independent generators, orbit structure, or operational content—not by counting formulas.

### Theorem 4 — Closure under algebraic operations

If \\(K_1,K_2\\) are invariant scalar functionals, then for any constants \\(a,b\\),

\\[ aK_1+bK_2 \\]

is invariant. If the product is defined,

\\[ K_1K_2 \\]

is also invariant.

This gives the invariant family a natural algebraic structure.

## 18. Nested intervention classes

Suppose

\\[ \mathfrak G_1\subseteq\mathfrak G_2. \\]

Then

\\[ \boxed{ \mathcal I(\mathfrak G_2;\mathcal D) \subseteq \mathcal I(\mathfrak G_1;\mathcal D). } \\]

Proof.

A functional invariant under every transformation in the larger family is necessarily invariant under every transformation in the smaller family.

\\(\square\\)

This theorem formalizes the shielding hierarchy.

As the intervention family expands, the invariant space can only shrink.

A candidate invariant that survives a larger intervention family is therefore more robust in a precise operational sense.

## 19. The maximal preserving semigroup

For a given functional \\(K\\), define its preserving local-channel set:

\\[ \operatorname{Pres}(K) = \left\\{ (\mathcal E_A,\mathcal E_B): K[(\mathcal E_A\otimes\mathcal E_B)(\rho)] =K(\rho) \quad\forall\rho\in\mathcal D \right\\}. \\]

### Theorem 5 — Semigroup closure of the preserving set

If the state domain is stable under the allowed transformations, then \\(\operatorname{Pres}(K)\\) is closed under composition.

Proof.

Let \\(\mathcal E,\mathcal F\in\operatorname{Pres}(K)\\). Then

\\[ K(\mathcal E(\rho))=K(\rho) \\]

and

\\[ K(\mathcal F(\sigma))=K(\sigma) \\]

for all admissible states.

Since the domain is stable, \\(\mathcal E(\rho)\\) is admissible. Therefore,

\\[ K(\mathcal F(\mathcal E(\rho))) = K(\mathcal E(\rho)) = K(\rho). \\]

Thus \\(\mathcal F\circ\mathcal E\in\operatorname{Pres}(K)\\).

\\(\square\\)

This provides a direct route to the proposed maximality theorem: identify the preserving semigroup and characterize its boundary.

## 20. Infinitesimal shielding condition

Consider a differentiable one-parameter family of local channels generated by a local Lindbladian:

\\[ \frac{d\rho}{dt} = (\mathcal L_A+\mathcal L_B)(\rho). \\]

For a differentiable functional \\(K\\), exact infinitesimal shielding requires

\\[ \boxed{ D K\_\rho[ (\mathcal L_A+\mathcal L_B)(\rho) ]=0 } \\]

for all \\(\rho\\) in the specified domain and all allowed generators.

Here \\(DK\_\rho\\) is the Fréchet derivative of \\(K\\) at \\(\rho\\).

If \\(K\\) is differentiable and this condition holds along every trajectory in a connected domain, then \\(K\\) is constant along those trajectories.

This is the infinitesimal form of shielding.

### 20.1 Linear functionals

For a linear functional

\\[ K_O(\rho)=\operatorname{Tr}(O\rho), \\]

the derivative is

\\[ \frac{dK_O}{dt} = \operatorname{Tr}[O(\mathcal L_A+\mathcal L_B)(\rho)]. \\]

Using the adjoint generator,

\\[ \frac{dK_O}{dt} = \operatorname{Tr}[ (\mathcal L_A^\dagger+\mathcal L_B^\dagger)(O)\rho ]. \\]

For invariance over every state, a sufficient and, on the full operator domain, necessary condition is

\\[ \boxed{ (\mathcal L_A^\dagger+\mathcal L_B^\dagger)(O)=0. } \\]

This connects CSC to the theory of conserved observables and fixed points of adjoint quantum dynamical generators.

It is a promising route to explicit classification.

## 21. A local-generator obstruction

Suppose the allowed generator family includes arbitrary local Hamiltonians:

\\[ \mathcal L_A(\rho) = -i[H_A\otimes I,\rho], \\]

\\[ \mathcal L_B(\rho) = -i[I\otimes H_B,\rho]. \\]

For a linear observable \\(O\\), infinitesimal invariance under all such generators requires

\\[ [O,H_A\otimes I+I\otimes H_B]=0 \\]

for every Hermitian \\(H_A,H_B\\).

This implies that \\(O\\) commutes with the full local matrix algebra.

For finite-dimensional bipartite systems, the commutant of

\\[ \mathcal B(\mathcal H_A)\otimes I \quad\text{and}\quad I\otimes\mathcal B(\mathcal H_B) \\]

is the scalar algebra.

Therefore,

\\[ O=cI. \\]

Consequently, no nontrivial linear expectation-value functional is invariant under all independent local Hamiltonians on the full state space.

This is an important restriction. Nontrivial local-unitary invariants must generally be nonlinear functionals of the state or functions of the orbit data.

## 22. Shielding versus monotonicity

Exact invariance is only one possible response to local interventions.

For a functional \\(K\\), consider:

\\[ K(\mathcal E(\rho))=K(\rho) \\]

for invariance,

\\[ K(\mathcal E(\rho))\leq K(\rho) \\]

for monotonicity, and

\\[ K(\mathcal E(\rho))\geq K(\rho) \\]

for nondecreasing behavior.

For mutual information under local CPTP maps,

\\[ I(A:B)\_{\rho'}\leq I(A:B)\_\rho. \\]

For entanglement monotones under suitable local operations and classical communication, analogous nonincrease results apply.

These are not shielding theorems. They are directional constraints.

We therefore propose the classification:

| Class                 | Transformation response                          |
| --------------------- | ------------------------------------------------ |
| Exact invariant       | Unchanged                                        |
| Approximate invariant | Changes by at most \\(\varepsilon\\)             |
| Monotone              | Changes in a prescribed direction                |
| Covariant             | Changes according to a known representation      |
| Fragile               | Can be strongly reduced by allowed interventions |
| Erasable              | Can be mapped to a state with zero value         |

A complete CSC theory should classify functionals by this response structure rather than restricting itself to binary invariant/non-invariant labels.

# Part VII — Revealing and breaking shielded correlations

## 23. Preservation is not the same as revealability

A functional can remain invariant under local operations yet be difficult to measure.

Conversely, a functional can be altered by an intervention but become easier to measure afterward.

We therefore distinguish:

- preservation: \\(K\\) remains unchanged;
- revelation: an intervention enables a measurement that distinguishes previously operationally equivalent states;
- destruction: an intervention drives \\(K\\) to zero or removes the property it represents;
- conversion: one type of correlation is transformed into another.

The distinction between preservation and revelation is central to the proposed research programme.

## 24. Operational distinguishability

Let \\(\mathfrak M\\) be a measurement family.

Define the distinguishability of two states relative to \\(\mathfrak M\\):

\\[ D\_{\mathfrak M}(\rho,\sigma) = \sup\_{M\in\mathfrak M} \left| \operatorname{Tr}[M(\rho-\sigma)] \right|. \\]

For a complete joint measurement family, this can recover trace-distance distinguishability up to the conventional normalization.

A measurement-relative shielding condition may require

\\[ D\_{\mathfrak M}(\rho,\sigma)>0 \\]

while the chosen functional remains invariant along the relevant intervention trajectories.

A candidate CSC discovery would identify a family of states for which a robust invariant survives a broad intervention class, while joint measurement remains capable of resolving state differences that local marginal measurements cannot detect.

## 25. Breaking transformations

For a given functional \\(K\\), define the breaking set

\\[ \operatorname{Break}(K) = \left\\{ \mathcal E: \exists\rho\in\mathcal D,\\; K(\mathcal E(\rho))\neq K(\rho) \right\\}. \\]

The preserving set and breaking set partition the intervention family, except where domain or measurement qualifications apply.

A stronger quantity is the maximal breaking strength:

\\[ B_K(\mathfrak G;\mathcal D) = \sup\_{\rho,\mathcal E} |K(\mathcal E(\rho))-K(\rho)|. \\]

For a normalized functional, this may be bounded and directly comparable across implementations.

### 25.1 Minimal breaking distance

If the channel space has a metric \\(d\_{\mathrm{ch}}\\), define

\\[ \delta_K(\rho) = \inf\_{\mathcal E\in\operatorname{Break}\_\rho(K)} d\_{\mathrm{ch}}(\mathcal E,\mathcal I), \\]

where

\\[ \operatorname{Break}\_\rho(K) = \\{\mathcal E:K(\mathcal E(\rho))\neq K(\rho)\\}. \\]

This measures how close an intervention can be to the identity while still changing the invariant.

The channel metric must be specified; a natural choice in finite dimensions is the diamond norm:

\\[ \\|\mathcal E-\mathcal F\\|\_\diamond. \\]

A positive lower bound on \\(\delta_K\\) would indicate finite robustness against small local perturbations, although it would not imply protection against arbitrary large transformations.

## 26. Approximate shielding and continuity bounds

Suppose \\(K\\) is Lipschitz continuous with respect to trace distance:

\\[ |K(\rho)-K(\sigma)| \leq L_K\\|\rho-\sigma\\|\_1. \\]

Then

\\[ \begin{aligned} |K(\mathcal E(\rho))-K(\rho)| &\leq L_K\\|\mathcal E(\rho)-\rho\\|\_1. \end{aligned} \\]

Thus

\\[ \boxed{ \Delta_K \leq L_K \sup\_{\rho,\mathcal E} \\|\mathcal E(\rho)-\rho\\|\_1. } \\]

This is a generic robustness bound.

It is useful but not sufficient to establish a new invariant. It converts a state-displacement bound into a functional-displacement bound.

For entropy-based functionals, continuity bounds such as Fannes–Audenaert-type inequalities may be used, with dimension and trace-distance assumptions stated explicitly.

# Part VIII — Measurement theory and experimental observables

## 27. Correlation observables

For observables \\(A_i\\) and \\(B_j\\), define

\\[ C\_{ij} = \operatorname{Tr}(\rho\_{AB}A_i\otimes B_j). \\]

The connected correlation is

\\[ \Gamma\_{ij} = C\_{ij} - \operatorname{Tr}(\rho_AA_i) \operatorname{Tr}(\rho_BB_j). \\]

A candidate invariant may be a scalar combination

\\[ K(\rho) = F(\\{\Gamma\_{ij}\\}). \\]

If the local measurement frames are transformed by known rotations, tensorial quantities such as singular values can remain invariant even though individual correlation components change.

This is experimentally attractive because it separates coordinate-dependent correlations from frame-independent relational structure.

### 27.1 Fixed versus optimized observables

For a fixed measurement family \\(\mathfrak M_0\\),

\\[ K\_{\mathrm{fixed}}(\rho) = K(\rho;\mathfrak M_0). \\]

For an optimized family,

\\[ K\_{\mathrm{opt}}(\rho) = \sup\_{\mathfrak M\in\mathfrak M\_{\mathrm{allowed}}} K(\rho;\mathfrak M). \\]

These can have different invariance properties.

For example, a local unitary may change a correlation component measured along a fixed axis while leaving an optimized entanglement or Bell quantity unchanged.

An experiment must therefore specify whether it measures a fixed-setting functional or a reoptimized functional.

## 28. Measurement disturbance

Repeated measurement of a single evolving system can disturb the correlations being studied.

A valid experimental protocol should use one of the following:

1. identically prepared ensembles measured at different intervention times;
2. weak measurements with a validated disturbance model;
3. nondestructive measurement where experimentally justified;
4. quantum process tomography combined with independently validated state preparation.

The measurement protocol itself must not be treated as an inert observer outside the physical model.

A measurement channel \\(\mathcal M\\) may alter the state:

\\[ \rho\mapsto\mathcal M(\rho). \\]

If the experiment measures \\(K\\) after the measurement operation has already changed the state, the measured quantity may not equal the premeasurement invariant.

# Part IX — Proposed CSC research laws

## 29. The shielding response function

Let a family of interventions be parameterized by

\\[ \boldsymbol\lambda = (\lambda_1,\ldots,\lambda_n). \\]

Define

\\[ K\_\rho(\boldsymbol\lambda) = K[\mathcal E\_{\boldsymbol\lambda}(\rho)]. \\]

The shielding response function is

\\[ \boxed{ \mathcal S_K(\rho;\boldsymbol\lambda) = K\_\rho(\boldsymbol\lambda)-K\_\rho(\mathbf0). } \\]

Exact shielding corresponds to

\\[ \mathcal S_K=0 \\]

throughout the intervention domain.

The response derivatives are

\\[ \chi_i^{(K)} = \left. \frac{\partial K\_\rho} {\partial\lambda_i} \right|\_{\boldsymbol\lambda=0}, \\]

and

\\[ \chi\_{ij}^{(K)} = \left. \frac{\partial^2 K\_\rho} {\partial\lambda_i\partial\lambda_j} \right|\_{\boldsymbol\lambda=0}. \\]

These quantities provide a local perturbative characterization.

A first-order shielded functional satisfies

\\[ \chi_i^{(K)}=0 \\]

for all allowed intervention directions.

A second-order shielded functional additionally satisfies

\\[ \chi\_{ij}^{(K)}=0. \\]

Vanishing derivatives to finite order do not imply exact invariance. Analyticity and domain assumptions would be required to infer stronger results.

## 30. Candidate universal scaling relation

A possible research target is a normalized shielding law relating functional stability to intervention strength.

Let

\\[ \epsilon\_{\mathrm{int}} \\]

measure the effective strength of the local intervention, and let

\\[ \Delta_K \\]

be the shielding defect.

One may test a scaling relation

\\[ \boxed{ \Delta_K \sim A_K\epsilon\_{\mathrm{int}}^{\\,p_K} } \\]

in a controlled weak-intervention regime.

Here \\(A_K\\) and \\(p_K\\) depend on the functional, state family, and transformation class.

A universal law would require a nontrivial collapse of normalized data across different systems or implementations.

No such law is established by the definition of CSC. It is a conjectural empirical target.

### 30.1 Symmetry-protected exponent

If a functional is stationary under first-order perturbations, then the leading change may be quadratic:

\\[ \Delta_K=O(\epsilon\_{\mathrm{int}}^2). \\]

This follows from a Taylor expansion when the first derivative vanishes and sufficient smoothness holds.

It is not universal. Nonanalytic channel dependence, boundary states, or nonsmooth functionals can violate the quadratic scaling.

## 31. Candidate invariant hierarchy

For each functional \\(K\\), define its maximal preserving family:

\\[ \mathfrak G_K^{\max} = \left\\{ \mathcal E: K(\mathcal E(\rho))=K(\rho) \\;\forall\rho\in\mathcal D \right\\}. \\]

The collection

\\[ \mathfrak H\_{\mathrm{CSC}} = \\{\mathfrak G_K^{\max}:K\in\mathcal K\\} \\]

is a candidate shielding hierarchy.

A central mathematical objective is to classify:

1. the maximal preserving groups or semigroups;
2. their invariant functional algebras;
3. the state domains on which invariance holds;
4. the minimal transformations that break each invariant;
5. the joint measurements that distinguish states within the same invariant class.

The last point is important. Equal values of a scalar invariant do not imply equal states.

# Part X — Experimental programme

## 32. Experimental objective

The experiment should determine whether a selected relational functional remains invariant under a specified local intervention family while joint-state measurements retain discriminatory power.

The experimental claim must be restricted to the intervention family actually implemented and calibrated.

## 33. Proposed architecture

[File:Alice and Bob Setup in a Polarization Quantum Entanglement Experiment.jpg - Wikimedia Commons](https://images.openai.com/static-rsc-4/pVqo_40aSsE2XGUzTGUr5ANFHYBPZrDogbl3WD-viTJXRznjVOmBr7oA9cNOgUQqH1auzCu4Stk30BduF0ofTqMyBUnK9OuMc4U5bCbJ-NPP1mz7b5l1xAA0efbTS5EcdILovKCpET_Pn288BOR7nuU1A4ywjL_Ocwl4O_d_fcw?purpose=inline)

[Experimental investigation of the information entropic Bell inequality | Scientific Reports](https://images.openai.com/static-rsc-4/nZZwXGQk-wcprTqhlAU4Hsa9OKooQF4k589hRZWFGgXBcj-ZeMOnN1DV4m2wWpCg18wn4kHzXb3XgTkk1-A8txWs-94QwIM49yEjeLd5uoTAXjNdCtLxPmVR5apuOP7TawhIFQA8sGypcDkCqlx3GH_NvUsd0b1zAyb7Lxhh6EU?purpose=inline)

[Priority Choice Experimental Two-Qubit Tomography: Measuring One by One All Elements of Density Matrices | Scientific Reports](https://images.openai.com/static-rsc-4/3sWNrZFIM5GIb2U0LZDAII91cqvAb2Wh-inCf4ptVm2HiqExlPXfiQsICzIn4nI3mudrbqQC8Q-la9Rh9LVjSBSzaRNY4fgZnIhps0B8L7hEUY49M-C89dkyCKdv_ZpIHAlYcF8WK7jTG3HNiGdBoETrBXqIyV2cL4nCpa2m4HY?purpose=inline)

11

The architecture contains:

- a bipartite state-preparation stage;
- independently addressable subsystems \\(A\\) and \\(B\\);
- calibrated local unitary controls;
- controlled local noise channels;
- joint measurement apparatus;
- local marginal measurement apparatus;
- environmental monitoring;
- synchronized data acquisition.

A photonic polarization experiment offers spatially separated subsystems and flexible local rotations. A superconducting-qubit platform offers controlled channels and high-fidelity tomography. The optimal platform depends on whether spatial separation or intervention precision is the primary experimental objective.

## 34. Experimental sequence

Stage 1 — State preparation

Prepare a set of states with known correlation properties:

\\[ \rho_1,\rho_2,\ldots,\rho_N. \\]

Include entangled, separable-but-correlated, and product states.

Stage 2 — Baseline characterization

Measure:

\\[ K(\rho_i), \\]

the reduced states, and selected joint observables.

Stage 3 — Local intervention

Apply independently controlled channels:

\\[ \mathcal E_A(\lambda_A), \qquad \mathcal E_B(\lambda_B). \\]

Candidate operations include:

- local unitary rotations;
- phase shifts;
- dephasing;
- amplitude damping;
- depolarization;
- restricted symmetry-preserving channels.

Stage 4 — Joint-state reconstruction

Estimate

\\[ \rho'\_{AB} = (\mathcal E_A\otimes\mathcal E_B)(\rho\_{AB}) \\]

using validated tomography or a smaller witness-specific measurement set.

Stage 5 — Invariant evaluation

Compute

\\[ K(\rho'\_{AB}) \\]

and compare it with the baseline.

Stage 6 — Joint distinguishability

For selected pairs \\(\rho_i,\rho_j\\), evaluate

\\[ D\_{\mathfrak M\_{AB}}(\rho_i,\rho_j). \\]

Stage 7 — Breaking-boundary search

Expand the intervention strength until the candidate invariant changes beyond the predetermined tolerance.

Stage 8 — Replication

Repeat across independently prepared states and, where possible, a different physical implementation.

## 35. Primary observables

| Quantity                | Purpose                                  |
| ----------------------- | ---------------------------------------- |
| \\(I(A:B)\\)            | Total correlation                        |
| Concurrence             | Two-qubit entanglement                   |
| Negativity              | Entanglement across a bipartition        |
| \\(S\_{\max}\\)         | Optimized CHSH value                     |
| \\(T\\) singular values | Local-unitary correlation invariants     |
| \\(D\_{\mathrm{tr}}\\)  | Joint-state distinguishability           |
| \\(\Delta_K\\)          | Shielding defect                         |
| \\(\delta_K\\)          | Minimum breaking distance, where defined |

The experiment should not rely on a single witness. A correlation functional can remain unchanged while another measure of the same state changes.

For example, a local dephasing operation can preserve a classical \\(ZZ\\) covariance while destroying entanglement.

## 36. Statistical treatment

For a measured estimator \\(\widehat K\\), define

\\[ \widehat\Delta_K = |\widehat K\_{\mathrm{after}} -\widehat K\_{\mathrm{before}}|. \\]

Uncertainty must include:

- finite sampling;
- state-preparation error;
- measurement calibration;
- channel calibration;
- reconstruction bias;
- drift;
- correlated errors between before/after measurements.

A confidence interval for \\(\Delta_K\\) should be constructed using an estimator appropriate to the measured data.

For a claim of approximate shielding, the correct statistical objective is an equivalence test:

\\[ \Delta_K<\varepsilon \\]

with a predeclared tolerance and confidence criterion.

Failure to reject a difference from zero is not proof of equivalence.

This is a critical methodological requirement.

# Part XI — Falsifiability and failure conditions

## 37. Falsification criteria

A candidate invariant is falsified relative to a specified intervention family if any reliably characterized transformation produces

\\[ |K(\rho')-K(\rho)|>\varepsilon \\]

with statistical confidence exceeding the predeclared threshold.

A proposed maximal preserving-family theorem is falsified by a counterexample channel within its claimed domain.

A proposed universal scaling law is falsified if independently calibrated implementations fail its predicted normalized collapse within stated uncertainties.

A claimed joint-distinguishability result is falsified if the prescribed measurement family cannot distinguish the target states at the predicted resolution.

## 38. Common false positives

### 38.1 Inadequate intervention coverage

Testing only local unitaries does not establish invariance under local CPTP maps.

### 38.2 Measurement-frame artifacts

A correlation component may appear to change merely because the local measurement axes rotate.

### 38.3 Optimization artifacts

An optimized functional may remain constant even though every fixed-setting correlation changes.

### 38.4 State-preparation drift

Apparent invariance may result from correlated preparation and calibration errors.

### 38.5 Unmodeled shared environments

Nominally local operations may be correlated through a shared bath.

### 38.6 Postselection bias

Selective outcomes can change conditional remote states. The experiment must distinguish conditional and unconditional statistics.

### 38.7 Insufficient precision

A small but nonzero defect may be hidden below the measurement resolution. Approximate shielding must always state \\(\varepsilon\\).

# Part XII — Relation to established theories

## 39. Symmetry and invariant theory

The mathematical foundations of CSC overlap strongly with invariant theory.

Group actions partition state spaces into orbits, and invariant functions are constant on those orbits.

The proposed CSC language does not make these established mathematical results novel.

Its potential contribution is to identify physically meaningful local intervention families and classify correlation functionals relative to them.

## 40. Decoherence-free subspaces and noiseless subsystems

A decoherence-free subspace is preserved by a specified noise model. Noiseless subsystems protect encoded information despite nontrivial noise acting on other degrees of freedom.

These are established structures.

CSC may generalize the question from protection of encoded quantum information to preservation of selected relational functionals, including cases where the entire state is not protected.

This generalization is a research direction, not an established theorem.

## 41. Quantum resource theories

Entanglement and other correlation properties are studied through resource theories. Free operations define which transformations are permitted, and monotones quantify resource behavior.

CSC is naturally compatible with this framework.

The key difference is its focus on exact or approximate invariance under a specified operation class, rather than merely monotonicity.

A CSC invariant can be a resource monotone that happens to remain constant on a restricted domain, but the two properties are not identical.

## 42. Quantum error correction

Quantum error-correcting codes protect logical information against specified noise channels.

A code projector \\(P\\) satisfies the Knill–Laflamme condition for an error set \\(\\{E_i\\}\\):

\\[ PE_i^\dagger E_jP = c\_{ij}P. \\]

This permits correction of errors without necessarily preventing physical changes to the underlying state.

CSC's relation to error correction is therefore conceptual but not identical. Error correction restores encoded information after an error; shielding concerns invariance of a specified functional under the transformation itself.

## 43. No-signaling and causal models

No-signaling constrains the dependence of remote marginal probabilities on local settings.

CSC constrains a joint functional under local interventions.

The distinction is formal:

\\[ \operatorname{Tr}\_A[ (\mathcal E_A\otimes\mathcal I_B)(\rho) ] = \rho_B \\]

does not entail

\\[ K[(\mathcal E_A\otimes\mathcal I_B)(\rho)] = K(\rho). \\]

No-signaling is a marginal constraint. CSC is a joint-state invariance condition.

# Part XIII — Novelty audit

## 44. Established results

The following are established and should not be claimed as new:

1. Local-unitary invariance of standard entanglement measures.
2. Local-unitary invariance of quantum mutual information.
3. Correlation-tensor invariants under local rotations.
4. No-signaling under local trace-preserving operations.
5. Monotonicity of mutual information under local channels.
6. Monotonicity of entanglement measures under appropriate local operations.
7. Decoherence-free subspaces and noiseless subsystems.
8. Stabilizer and orbit classifications under group actions.
9. Quantum error correction and protected logical subsystems.
10. Fixed points and conserved observables of quantum dynamical semigroups.

## 45. Potentially novel contributions

The following are plausible research targets:

A. Maximal local-channel preserving-family classification

For a selected class of nonlinear correlation functionals, derive the maximal local channel semigroup that preserves them.

B. Relational invariants beyond state protection

Identify functionals that remain invariant even when the full state changes and no noiseless subsystem exists.

C. Intervention-spectrum classification

Classify states by the response profiles of relational functionals under a complete, experimentally meaningful intervention family.

D. Joint distinguishability within invariant classes

Determine when states with equal values of a CSC invariant remain distinguishable by joint measurements and identify the minimal measurement family required.

E. Quantitative breaking thresholds

Derive sharp lower bounds on the strength of local interventions required to change a specified relational invariant.

F. Cross-platform universality

Test whether normalized shielding defects or breaking exponents are shared by different physical implementations.

## 46. The principal novelty obstacle

The central obstacle is that invariance is always relative to a chosen transformation family.

A functional may appear novel because the intervention family has been artificially restricted.

For example, a local-unitary invariant is not automatically a new physical structure. Nor does preservation under one dephasing channel imply protection under a general local noise model.

A genuine result must therefore establish one of two things:

1. a mathematically new invariant family with a complete characterization; or
2. a physically significant invariance theorem under a broad, independently justified intervention class.

The first is primarily mathematical. The second is potentially experimental.

# Part XIV — Research propositions and conjectures

## 47. Proposition: intervention-family monotonicity

Established theorem. If

\\[ \mathfrak G_1\subseteq\mathfrak G_2, \\]

then

\\[ \operatorname{Inv}(\mathfrak G_2) \subseteq \operatorname{Inv}(\mathfrak G_1). \\]

This provides the mathematical basis for the shielding hierarchy.

## 48. Conjecture: nontrivial relational protection beyond noiseless subsystems

There may exist physically realizable channel semigroups \\(\mathfrak G\\) and nonconstant correlation functionals \\(K\\) such that

\\[ K(\mathcal E(\rho))=K(\rho) \\]

for all \\(\mathcal E\in\mathfrak G\\) and \\(\rho\in\mathcal D_0\\), while no nontrivial subsystem of \\(\mathcal H\_{AB}\\) is noiseless under the same dynamics.

This conjecture requires a precise definition of “no nontrivial noiseless subsystem” and an explicit example.

A proof would be a meaningful CSC contribution.

## 49. Conjecture: intervention-response completeness

For a sufficiently rich intervention family \\(\mathfrak G\\), the full intervention profile

\\[ \kappa\_\rho(\mathcal E) = K[\mathcal E(\rho)] \\]

may distinguish correlation structures that are indistinguishable by a finite collection of conventional scalar invariants.

This is not guaranteed. If \\(K\\) is too coarse, no intervention family can recover information discarded by \\(K\\).

The conjecture should therefore be tested only for a specified family of functionals and channels.

## 50. Conjecture: robust breaking boundary

For finite-dimensional systems and a compact intervention family, a normalized functional may admit a nonzero minimum intervention distance to its breaking set on a restricted compact state domain.

Such a result would quantify finite robustness.

However, the existence of a positive distance depends on continuity, compactness, the chosen metric, and whether the initial state lies in the interior of the preserving region.

It cannot be assumed universally.

# Part XV — Limitations and unresolved questions

## 51. Ontological limitation

CSC does not establish that a correlation is a fundamental physical object independent of the underlying state.

A functional invariant under local transformations is a mathematical property of a state and an action on the state space.

Any stronger ontological claim requires independent physical argument.

## 52. Intervention dependence

The intervention family is part of the definition. Two researchers may obtain different shielding classifications by choosing different allowed transformations.

The family must be specified before the data are analyzed.

## 53. Functional dependence

A state may be shielded with respect to one functional and unshielded with respect to another.

For example, a dephasing channel may preserve a classical covariance while destroying entanglement.

There is no reason to expect a single scalar to capture all correlation structure.

## 54. State-domain dependence

An invariant may hold on a protected subspace or state manifold but fail on the full density-operator space.

This restriction must be explicit.

## 55. Correlated noise

The product-channel model

\\[ \mathcal E_A\otimes\mathcal E_B \\]

does not represent every physically local-looking implementation.

Shared environments can generate correlated channels that are not products.

A complete theory must distinguish local controls from independent reduced dynamics.

## 56. Conditional transformations

Postselected measurement outcomes are described by trace-nonincreasing completely positive maps.

Their conditional states can change remote conditional statistics without violating no-signaling.

CSC must distinguish deterministic channels from selective instruments.

## 57. Infinite-dimensional systems

In infinite-dimensional Hilbert spaces, domain, continuity, and compactness issues become more subtle.

Entropy may be infinite or discontinuous without energy constraints. A finite-dimensional theorem cannot automatically be extended to field-theoretic systems.

# Part XVI — A concrete programme for a first CSC theorem

## 58. Recommended initial target

The most tractable starting point is the two-qubit correlation tensor.

Write

\\[ \rho = \frac14 \left[ I\otimes I+ \mathbf a\cdot\boldsymbol\sigma\otimes I+ I\otimes\mathbf b\cdot\boldsymbol\sigma+ T\_{ij}\sigma_i\otimes\sigma_j \right]. \\]

Under independent local unitaries,

\\[ T\mapsto R_A T R_B^{\mathsf T}. \\]

The singular values

\\[ s_1,s_2,s_3 \\]

are invariant.

The first theorem should identify the complete independent scalar invariants of \\(T\\) under this action, subject to physical-state constraints and the role of local Bloch vectors.

A second theorem should determine which local nonunitary channels preserve each invariant.

A third should characterize the minimal intervention family that breaks each invariant.

This yields a rigorous sequence:

\\[ \boxed{ \text{Orbit classification} \longrightarrow \text{preserving semigroup} \longrightarrow \text{breaking boundary}. } \\]

The work should not begin by claiming universal causal shielding. It should begin with an exact low-dimensional classification.

## 59. Proposed theorem sequence

Theorem A — Local-unitary invariant completeness

Determine a complete generating set of scalar invariants for the chosen bipartite state class.

Theorem B — Channel stabilizer classification

For each generator \\(K_i\\), characterize

\\[ \operatorname{Pres}(K_i). \\]

Theorem C — Nonunitary breaking

Identify the smallest local channel families that violate each invariant.

Theorem D — Approximate shielding

Derive explicit bounds on

\\[ |K_i(\mathcal E(\rho))-K_i(\rho)| \\]

in terms of a physically measurable channel parameter.

Theorem E — Joint distinguishability

Characterize pairs of states with equal invariant vectors

\\[ \mathbf K(\rho)=\mathbf K(\sigma) \\]

but positive joint trace distance.

This final theorem prevents the invariant classification from being mistaken for complete state tomography.

# Part XVII — Final synthesis

## 60. Central mathematical statement

Causal Shielding of Correlations is defined relative to a state domain \\(\mathcal D\\), a family of local transformations \\(\mathfrak G\\), and a specified correlation functional \\(K\\):

\\[ \boxed{ K[(\mathcal E_A\otimes\mathcal E_B)(\rho)] = K(\rho) } \\]

for every admissible state and intervention pair.

The associated shielding defect is

\\[ \boxed{ \Delta_K(\mathfrak G;\mathcal D) = \sup\_{\rho,\mathcal E} \left| K[(\mathcal E_A\otimes\mathcal E_B)(\rho)] -K(\rho) \right|. } \\]

Exact shielding is the condition

\\[ \boxed{\Delta_K=0.} \\]

But the strength of the result depends on the intervention family.

Universal invariance under all local CPTP channels forces a scalar functional on the full bipartite state space to be constant. Nontrivial shielding must therefore arise from restricted transformation classes, restricted state domains, or carefully defined relational quantities.

## 61. Central conceptual distinction

\\[ \boxed{ \text{No-signaling} \neq \text{correlation shielding} \neq \text{state preservation}. } \\]

No-signaling protects remote marginal statistics against deterministic local operations.

Correlation shielding protects a specified joint functional against a specified local intervention family.

State preservation protects the full density operator.

These are mathematically different properties.

## 62. Central research objective

The most important unresolved problem is to find and classify nontrivial relational invariants that survive physically meaningful local transformations even when the joint state itself changes.

A successful result would provide:

- a complete invariant family;
- a maximal preserving semigroup;
- a theorem identifying its breaking transformations;
- a quantitative robustness bound;
- a joint measurement protocol demonstrating operational distinguishability;
- experimental replication under independently calibrated interventions.

## 63. Conclusion

Causal Shielding of Correlations is a potentially useful framework for organizing the stability of joint-state properties under local interventions. Its mathematical foundation is not wholly new: symmetry invariants, quantum channel fixed points, decoherence-free structures, and resource monotones already describe important parts of the problem.

The distinctive research opportunity lies in bringing these elements into a single intervention-relative classification of relational functionals.

The strongest version of the proposal is not that correlations are immune to local causation. That claim would be false for many familiar correlation measures. It is that certain relational quantities may possess a precisely characterizable domain of invariance, even when the state carrying them remains globally distinguishable and locally transformable.

The appropriate mathematical object is therefore not an absolute shield, but a maximal preserving transformation semigroup associated with a specified relational invariant.

\\[ \boxed{ K \\;\longmapsto\\; \operatorname{Pres}(K) \\;\longmapsto\\; \operatorname{Break}(K) \\;\longmapsto\\; \Delta_K } \\]

This sequence provides the foundation for a falsifiable theory.

The first decisive result should be a complete classification of local-unitary correlation-tensor invariants and their nonunitary stabilizers for two-qubit states. Only after that classification should the framework advance toward more general multipartite, network, or field-theoretic systems.

The proposal is mathematically coherent as a research programme. Its novelty remains conditional: it will be established only if the classification yields invariant families, preservation theorems, or quantitative breaking laws that cannot be reduced to existing symmetry, channel, and decoherence-free-subspace results.

## References

1\. Nielsen, M. A., & Chuang, I. L. (2010). Quantum Computation and Quantum Information. Cambridge University Press.

2\. Horodecki, R., Horodecki, P., Horodecki, M., & Horodecki, K. (2009). Quantum entanglement. Reviews of Modern Physics, 81, 865–942. [https://doi.org/10.1103/RevModPhys.81.865](https://doi.org/10.1103/RevModPhys.81.865?utm_source=chatgpt.com)

3\. Watrous, J. (2018). The Theory of Quantum Information. Cambridge University Press.

4\. Lindblad, G. (1976). On the generators of quantum dynamical semigroups. Communications in Mathematical Physics, 48, 119–130. [https://doi.org/10.1007/BF01608499](https://doi.org/10.1007/BF01608499?utm_source=chatgpt.com)

5\. Gorini, V., Kossakowski, A., & Sudarshan, E. C. G. (1976). Completely positive dynamical semigroups of N-level systems. Journal of Mathematical Physics, 17, 821–825. [https://doi.org/10.1063/1.522979](https://doi.org/10.1063/1.522979?utm_source=chatgpt.com)

6\. Knill, E., Laflamme, R., & Viola, L. (2000). Theory of quantum error correction for general noise. Physical Review Letters, 84, 2525–2528. [https://doi.org/10.1103/PhysRevLett.84.2525](https://doi.org/10.1103/PhysRevLett.84.2525?utm_source=chatgpt.com)

7\. Lidar, D. A., & Whaley, K. B. (2003). Decoherence-free subspaces and subsystems. In Irreversible Quantum Dynamics. Springer.

8\. Ruskai, M. B. (2002). Inequalities for quantum entropy: A review with conditions for equality. Journal of Mathematical Physics, 43, 4358–4375. [https://doi.org/10.1063/1.1497384](https://doi.org/10.1063/1.1497384?utm_source=chatgpt.com)

9\. Vidal, G. (2000). Entanglement monotones. Journal of Modern Optics, 47, 355–376. [https://doi.org/10.1080/09500340008244048](https://doi.org/10.1080/09500340008244048?utm_source=chatgpt.com)

10\. Baumgratz, T., Cramer, M., & Plenio, M. B. (2014). Quantifying coherence. Physical Review Letters, 113, 140401. [https://doi.org/10.1103/PhysRevLett.113.140401](https://doi.org/10.1103/PhysRevLett.113.140401?utm_source=chatgpt.com)

11\. Makhlin, Y. (2002). Nonlocal properties of two-qubit gates and mixed states, and the optimization of quantum computations. Quantum Information Processing, 1, 243–252. [https://doi.org/10.1023/A:1022144002391](https://doi.org/10.1023/A:1022144002391?utm_source=chatgpt.com)

12\. Fannes, M. (1973). A continuity property of the entropy density for spin lattice systems. Communications in Mathematical Physics, 31, 291–294. [https://doi.org/10.1007/BF01646490](https://doi.org/10.1007/BF01646490?utm_source=chatgpt.com)

13\. Audenaert, K. M. R. (2007). A sharp continuity estimate for the von Neumann entropy. Journal of Physics A: Mathematical and Theoretical, 40, 8127–8136. [https://doi.org/10.1088/1751-8113/40/28/S18](https://doi.org/10.1088/1751-8113/40/28/S18?utm_source=chatgpt.com)

14\. Bennett, C. H., DiVincenzo, D. P., Smolin, J. A., & Wootters, W. K. (1996). Mixed-state entanglement and quantum error correction. Physical Review A, 54, 3824–3851. [https://doi.org/10.1103/PhysRevA.54.3824](https://doi.org/10.1103/PhysRevA.54.3824?utm_source=chatgpt.com)

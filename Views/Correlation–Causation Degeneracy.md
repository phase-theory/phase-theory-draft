# Correlation–Causation Degeneracy (CCD)

An operational and mathematical theory of relational information invisible to causal-response measurements

## Abstract

We formulate Correlation–Causation Degeneracy (CCD) as the problem of determining how much physically distinguishable joint-state information can remain inaccessible to a specified family of causal-response measurements. The central possibility is that two distinct physical states exhibit identical local causal-response behavior while possessing different joint correlation structures.

Let \\(\rho\\) and \\(\sigma\\) be candidate states of a composite system. For a declared family of response experiments \\(\mathfrak P\\), suppose that

\\[ R\_\rho(X,Y)=R\_\sigma(X,Y) \qquad \forall (X,Y)\in\mathfrak P, \\]

while there exists at least one joint correlation functional for which

\\[ K\_\rho(A,B)\ne K\_\sigma(A,B). \\]

The two states are then indistinguishable under the specified response protocol but distinguishable by an appropriate joint measurement. This is not a contradiction: response measurements and joint-correlation measurements interrogate different mathematical properties of a physical state.

The principal objective of CCD is to characterize the equivalence classes induced by causal-response data and to identify the correlation information that varies within each class. We define response-equivalence relations, response maps, correlation signatures, degeneracy fibers, and operationally invisible relational information. We derive conditions under which local response data are informationally incomplete, construct explicit two-qubit examples, distinguish several increasingly strong notions of causal-response equivalence, and formulate a classification theorem program.

A central result is that, for a restricted response protocol, equality of all measured response functions need not imply equality of joint states or equality of their correlations. Conversely, if the response protocol includes a tomographically complete set of joint-state measurements, the degeneracy disappears. The existence and extent of CCD therefore depend on the operational content of the response experiment, not merely on the mathematical distinction between correlation and causation.

The proposed contribution is a classification of the fibers of the response map: a theorem identifying precisely which joint-state features are reconstructible from causal-response data, which remain invisible, and which additional measurements are sufficient to resolve the ambiguity. State distinguishability, operational equivalence, quantum tomography, and causal inference are established areas. CCD, as developed here, is a proposed synthesis and classification program; no claim is made that its general classification theorem has already been proved.

## 1. Introduction

### 1.1 The inverse problem of causal-response physics

Physical theories frequently infer structure from responses. A system is perturbed, an observable is measured, and the resulting change is used to infer properties of the underlying state or dynamics.

This procedure is powerful, but it raises a fundamental inverse problem:

Does complete knowledge of a specified family of causal responses uniquely determine the correlation structure of the physical state?

The answer is not generally yes.

A response experiment records how selected observables change under selected interventions. A joint-correlation experiment records statistical relationships between observables. These data can overlap, but they are not identical in general.

The distinction becomes particularly important in composite quantum systems. Two states may produce the same local marginal statistics, the same response to a selected class of local operations, or even the same entire response profile for a specified protocol, while differing in their joint-state correlations.

The issue is not simply experimental imprecision. Even with exact data and noiseless instruments, a response map can fail to be injective. If two states map to the same response data, no inference procedure using only those data can distinguish them.

This is the phenomenon investigated here.

### 1.2 Definition of the CCD problem

Let \\(\mathcal S\\) be a physical state space. Let \\(\mathfrak P\\) be a specified family of causal-response experiments. Each experiment \\(p\in\mathfrak P\\) produces a response datum \\(R\_\rho(p)\\) when the system is in state \\(\rho\\).

The complete response profile is the map

\\[ \mathscr R:\mathcal S\longrightarrow\mathcal Y, \\]

defined by

\\[ \mathscr R(\rho) = \big(R\_\rho(p)\big)\_{p\in\mathfrak P}, \\]

where \\(\mathcal Y\\) is the response-data space.

Two states are response-equivalent if

\\[ \boxed{ \rho\sim\_{\mathscr R}\sigma \iff \mathscr R(\rho)=\mathscr R(\sigma). } \\]

Now let

\\[ \mathscr K:\mathcal S\longrightarrow\mathcal Z \\]

be a joint-correlation signature map. It may include connected correlation tensors, correlation functions, joint probability distributions, or selected higher-order correlation invariants.

The CCD condition is

\\[ \boxed{ \rho\sim\_{\mathscr R}\sigma, \qquad \mathscr K(\rho)\ne\mathscr K(\sigma). } \\]

The two states belong to the same response-equivalence class but occupy different positions in correlation space.

### 1.3 The central research question

The fundamental question is not whether such pairs can exist in a restricted experiment. They can.

The deeper problem is:

> Given a response protocol \\(\mathfrak P\\), characterize the full set of physically distinct correlation structures compatible with each possible response profile.

In mathematical terms, determine the correlation structure of the fibers

\\[ \boxed{ \mathscr R^{-1}(r) = \\{\rho\in\mathcal S:\mathscr R(\rho)=r\\}. } \\]

A complete theory would establish which correlation functionals are constant on every fiber, which can vary, and what additional observations are necessary to make the state identifiable.

### 1.4 Epistemic status

The paper distinguishes four levels of claim.

- Established results: operational equivalence, state distinguishability, quantum tomography, and the nonuniqueness of states under incomplete measurement families.
- Derived results: explicit CCD examples and algebraic conditions for response-map degeneracy.
- Proposed structures: CCD fibers, relational invisibility classes, and the associated classification hierarchy.
- Conjectural results: general theorems identifying all correlation features invisible to a given physically constrained response protocol.

The aim is not to claim that correlation and causation have been newly separated. The aim is to derive a precise theory of what causal-response measurements can and cannot reconstruct.

## 2. Operational foundations

### 2.1 Physical state space

Begin with a finite-dimensional composite quantum system

\\[ \mathcal H=\mathcal H_A\otimes\mathcal H_B, \\]

with dimensions \\(d_A\\) and \\(d_B\\). Its state space is

\\[ \mathcal S(\mathcal H) = \left\\{ \rho\in\mathcal L(\mathcal H): \rho=\rho^\dagger,\\; \rho\ge0,\\; \operatorname{Tr}\rho=1 \right\\}. \\]

A state is a positive, unit-trace operator. For a bipartite state,

\\[ \rho_A=\operatorname{Tr}\_B\rho, \qquad \rho_B=\operatorname{Tr}\_A\rho. \\]

The joint state contains information that need not be recoverable from the reduced states. In particular,

\\[ \rho\_{AB}\ne\rho_A\otimes\rho_B \\]

may hold even when the two reduced states are maximally mixed.

This distinction is the mathematical starting point of CCD: local state data and joint-state data are different levels of description.

### 2.2 Response experiments as measurement maps

A response protocol may involve an intervention, a subsequent evolution, and an observable measurement. We represent one such experiment by a quantum instrument or, for a nonselective experiment, a quantum channel followed by a measurement.

For experiment \\(p\\), let \\(\mathcal E_p\\) denote the allowed state transformation and let \\(\\{M\_{p,y}\\}\_y\\) be the measurement effects. The outcome probabilities are

\\[ P\_\rho(y\mid p) = \operatorname{Tr} \left[ M\_{p,y}\mathcal E_p(\rho) \right]. \\]

By the adjoint-channel identity,

\\[ P\_\rho(y\mid p) = \operatorname{Tr} \left[ \mathcal E_p^\dagger(M\_{p,y})\rho \right]. \\]

Define the effective response effect

\\[ F\_{p,y} = \mathcal E_p^\dagger(M\_{p,y}). \\]

Then

\\[ P\_\rho(y\mid p) = \operatorname{Tr}(F\_{p,y}\rho). \\]

This representation is important because it converts the response-identification problem into a question about which operators are probed by the experiment.

The response protocol may record the full outcome distribution, selected moments, susceptibilities, or differences between intervention settings. Each choice corresponds to a particular set of linear or nonlinear functions of the underlying probabilities.

### 2.3 Response functions

For a pair of accessible observables \\(X,Y\\), write a general response function as

\\[ R\_\rho(X,Y;\mathcal E) = \operatorname{Tr} \left[ Y\\,\mathcal E(\rho;X) \right] - \operatorname{Tr}(Y\rho), \\]

where \\(\mathcal E(\rho;X)\\) denotes the state resulting from an intervention parameterized by \\(X\\). The precise form depends on the physical experiment.

For a small perturbation generated by a parameter \\(\epsilon\\), define the linear response

\\[ \chi\_\rho(X,Y) = \left. \frac{\partial}{\partial\epsilon} \langle Y\rangle\_{\rho,\epsilon X} \right|\_{\epsilon=0}. \\]

In a dynamical theory, this may be a susceptibility or a retarded response function. For a protocol involving finite interventions, the response may instead be a finite difference:

\\[ R\_\rho(X,Y) = \langle Y\rangle\_{\rho,\mathcal E_X} - \langle Y\rangle\_{\rho,\mathcal E_0}. \\]

These definitions are not interchangeable. A CCD classification must declare which one is being used.

For the general theory, let \\(\mathfrak P\\) denote the complete collection of permitted experiments and let

\\[ \mathscr R(\rho) = \left( R\_\rho(p) \right)\_{p\in\mathfrak P} \\]

be the full response profile.

### 2.4 Correlation functionals

For local observables \\(A\\) and \\(B\\), define the connected correlation

\\[ \boxed{ K\_\rho(A,B) = \operatorname{Tr}(\rho\\,A\otimes B) - \operatorname{Tr}(\rho_A A) \operatorname{Tr}(\rho_B B). } \\]

This subtracts the product of local means and vanishes for product states.

For a chosen operator basis \\(\\{F_i\\}\\) on \\(A\\) and \\(\\{G_j\\}\\) on \\(B\\), define

\\[ T\_{ij}(\rho) = K\_\rho(F_i,G_j). \\]

The tensor \\(T(\rho)\\) records the connected two-point correlation structure in the selected basis. A scalar diagnostic is

\\[ K_2(\rho) = \left(\sum\_{i,j}|T\_{ij}(\rho)|^2\right)^{1/2}. \\]

For a full CCD classification, the tensor is generally more informative than its norm: different correlation tensors can have the same norm.

Higher-order correlations can be included through connected cumulants. For example, for three observables \\(A,B,C\\),

\\[ \begin{aligned} K\_\rho^{(3)}(A,B,C) ={}&\langle ABC\rangle\_\rho -\langle AB\rangle\_\rho\langle C\rangle\_\rho\\\ &-\langle AC\rangle\_\rho\langle B\rangle\_\rho -\langle BC\rangle\_\rho\langle A\rangle\_\rho\\\ &+2\langle A\rangle\_\rho \langle B\rangle\_\rho \langle C\rangle\_\rho. \end{aligned} \\]

Here the product ordering must be specified for noncommuting observables. One may use symmetrized moments or an ordered correlation convention appropriate to the physical protocol.

### 2.5 Response equivalence

Definition 1 — CCD response equivalence.

Two states \\(\rho,\sigma\in\mathcal S\\) are equivalent relative to the response protocol \\(\mathfrak P\\) if

\\[ \boxed{ \rho\sim\_{\mathfrak P}\sigma \iff R\_\rho(p)=R\_\sigma(p) \quad\forall p\in\mathfrak P. } \\]

This is an equivalence relation:

- Reflexivity follows from \\(R\_\rho(p)=R\_\rho(p)\\).
- Symmetry follows from equality being symmetric.
- Transitivity follows from equality being transitive.

The equivalence classes are the fibers of \\(\mathscr R\\):

\\[ [\rho]\_{\mathfrak P} = \mathscr R^{-1}(\mathscr R(\rho)). \\]

Definition 2 — CCD pair.

A pair \\((\rho,\sigma)\\) is a CCD pair relative to \\((\mathfrak P,\mathfrak K)\\) if

\\[ \rho\sim\_{\mathfrak P}\sigma \\]

but

\\[ \exists K\in\mathfrak K: \quad K\_\rho\ne K\_\sigma, \\]

where \\(\mathfrak K\\) is the selected family of correlation functionals.

This definition makes the relative nature of CCD explicit. A pair can be degenerate for one response protocol and distinguishable under a richer one.

## 3. The linear-algebraic structure of CCD

### 3.1 The response operator span

Suppose the response protocol consists of a collection of outcome probabilities that are linear in the state:

\\[ p\_\rho(\alpha) = \operatorname{Tr}(F\_\alpha\rho), \qquad \alpha\in\Omega\_{\mathfrak P}. \\]

Let \\(\mathcal V\_{\mathfrak P}\\) be the real linear span of all effective response operators:

\\[ \mathcal V\_{\mathfrak P} = \operatorname{span}\_{\mathbb R} \\{F\_\alpha:\alpha\in\Omega\_{\mathfrak P}\\}. \\]

Two states are response-equivalent precisely when

\\[ \operatorname{Tr} \left[ F\_\alpha(\rho-\sigma) \right]=0 \qquad \forall\alpha. \\]

Writing

\\[ \Delta=\rho-\sigma, \\]

we obtain

\\[ \boxed{ \Delta\in\mathcal V\_{\mathfrak P}^{\perp}, } \\]

where orthogonality is with respect to the Hilbert–Schmidt inner product

\\[ \langle X,Y\rangle\_{\mathrm{HS}} = \operatorname{Tr}(XY) \\]

for Hermitian operators.

Since \\(\rho\\) and \\(\sigma\\) are normalized,

\\[ \operatorname{Tr}\Delta=0. \\]

Thus the response-invisible perturbations lie in

\\[ \boxed{ \mathcal D\_{\mathfrak P} = \mathcal V\_{\mathfrak P}^{\perp} \cap \\{X=X^\dagger,\operatorname{Tr}X=0\\}. } \\]

We call \\(\mathcal D\_{\mathfrak P}\\) the response-invisible operator subspace.

It is the central mathematical object of the linear CCD theory.

### 3.2 The basic degeneracy theorem

Theorem 1 — Response equivalence and the invisible subspace.

Let \\(\mathfrak P\\) be a response protocol whose data consist of expectation values of a family of effective Hermitian operators \\(\\{F\_\alpha\\}\\). Let \\(\mathcal V\_{\mathfrak P}\\) be their real linear span. Then two density operators \\(\rho,\sigma\\) produce identical response data if and only if

\\[ \rho-\sigma\in\mathcal D\_{\mathfrak P}. \\]

Proof.

By definition, identical response data mean

\\[ \operatorname{Tr}(F\_\alpha\rho) = \operatorname{Tr}(F\_\alpha\sigma) \\]

for every \\(\alpha\\). Subtracting gives

\\[ \operatorname{Tr}(F\_\alpha\Delta)=0 \qquad\forall\alpha. \\]

By linearity, \\(\Delta\\) is orthogonal to the entire span \\(\mathcal V\_{\mathfrak P}\\). Since both states are Hermitian and normalized, \\(\Delta\\) is Hermitian and traceless. Hence \\(\Delta\in\mathcal D\_{\mathfrak P}\\).

Conversely, if \\(\Delta\in\mathcal D\_{\mathfrak P}\\), then \\(\operatorname{Tr}(F\_\alpha\Delta)=0\\) for every response operator. Therefore all response probabilities agree. \\(\square\\)

This theorem is an operator-space characterization of incomplete response information. Its ingredients are standard linear algebra and quantum measurement theory. The CCD research program applies this structure specifically to the relation between causal-response data and joint correlation observables.

### 3.3 Correlations invisible to response data

Let \\(C\\) be a Hermitian joint observable. Its expectation-value difference between two response-equivalent states is

\\[ \Delta\langle C\rangle = \operatorname{Tr}(C\Delta). \\]

If \\(C\in\mathcal V\_{\mathfrak P}\\), then

\\[ \operatorname{Tr}(C\Delta)=0 \\]

for every response-equivalent pair. Such an observable is fixed by the response data.

If \\(C\\) has a nonzero component orthogonal to \\(\mathcal V\_{\mathfrak P}\\), then there may exist response-equivalent states with different values of \\(\langle C\rangle\\).

More precisely, decompose

\\[ C=C\_{\parallel}+C\_{\perp}, \\]

where

\\[ C\_{\parallel}\in\mathcal V\_{\mathfrak P}, \qquad C\_{\perp}\in\mathcal V\_{\mathfrak P}^{\perp}. \\]

Then

\\[ \operatorname{Tr}(C\Delta) = \operatorname{Tr}(C\_{\perp}\Delta). \\]

The component \\(C\_{\parallel}\\) is reconstructible from response data; the component \\(C\_{\perp}\\) is invisible to the response protocol.

This leads to the principal theorem target.

Theorem 2 — Correlation visibility criterion.

For a linear response protocol, a linear observable \\(C\\) has the same expectation value on every state in every response-equivalence class if and only if its traceless component belongs to the response-operator span, subject to the physical state-space constraints.

In particular, if \\(C\\) has a nonzero component along an admissible response-invisible direction, then there exist response-equivalent states with different values of \\(C\\).

The qualification concerning admissibility is necessary: an arbitrary traceless Hermitian perturbation need not connect two positive density operators. For a full-rank state \\(\rho_0\\), however, sufficiently small perturbations \\(\epsilon\Delta\\) preserve positivity:

\\[ \rho\_\pm=\rho_0\pm\epsilon\Delta, \\]

provided

\\[ 0<\epsilon< \frac{\lambda\_{\min}(\rho_0)}{\\|\Delta\\|\_\infty}. \\]

If \\(\Delta\ne0\\) is traceless and \\(C\\) has nonzero overlap with \\(\Delta\\), then

\\[ \operatorname{Tr}(C\rho\_+) - \operatorname{Tr}(C\rho\_-) = 2\epsilon\operatorname{Tr}(C\Delta)\ne0. \\]

This establishes the existence of a physical CCD pair whenever the response-invisible subspace contains a direction detected by the correlation observable.

### 3.4 Dimensional criterion

For a \\(d\\)-dimensional Hilbert space, the real vector space of Hermitian operators has dimension \\(d^2\\). The trace-one affine state space has dimension \\(d^2-1\\).

If the response operators span a subspace of dimension \\(m\\), then

\\[ \dim\mathcal D\_{\mathfrak P} \ge d^2-m, \\]

with the precise dimension depending on whether the identity is included and how normalization constraints are counted.

If the response effects span the full Hermitian operator space, the protocol is informationally complete and

\\[ \mathcal D\_{\mathfrak P}=\\{0\\}. \\]

Then response-equivalent states must be identical.

If the span is incomplete, a nonzero invisible subspace exists. Whether it contains physically admissible directions that alter a particular correlation depends on the chosen state and correlation observable.

This is the exact algebraic form of the CCD question: which directions in state space are erased by the response map, and which correlation observables detect those directions?

### 3.5 Nonlinear response data

Some response protocols record nonlinear quantities, such as ratios, normalized susceptibilities, or functions of multiple outcome probabilities. In that case, the simple operator-span theorem applies to the underlying probability data, not necessarily to the nonlinear summary itself.

Let

\\[ \mathscr R(\rho)=f(\mathscr P(\rho)), \\]

where \\(\mathscr P\\) is the vector of underlying linear probabilities and \\(f\\) is a data-processing map. Then

\\[ \mathscr R(\rho)=\mathscr R(\sigma) \\]

may occur even when

\\[ \mathscr P(\rho)\ne\mathscr P(\sigma). \\]

Nonlinear compression can therefore introduce additional degeneracy. A complete CCD analysis should distinguish:

1. Degeneracy due to an incomplete physical measurement family.
2. Degeneracy due to the mathematical response observable.
3. Degeneracy due to post-processing or loss of recorded information.

These mechanisms have different physical interpretations and different remedies.

## 4. Explicit construction: identical local response, different joint correlations

### 4.1 The two-qubit states

We now construct a concrete CCD pair.

Let

\\[ |\Phi^+\rangle = \frac{|00\rangle+|11\rangle}{\sqrt2} \\]

and define the entangled state

\\[ \rho\_{\mathrm E} = |\Phi^+\rangle\langle\Phi^+|. \\]

Compare it with the separable state

\\[ \rho\_{\mathrm C} = \frac12|00\rangle\langle00| + \frac12|11\rangle\langle11|. \\]

Both have identical local reduced states:

\\[ \operatorname{Tr}\_B\rho\_{\mathrm E} = \operatorname{Tr}\_B\rho\_{\mathrm C} = \frac{I_2}{2}, \\]

\\[ \operatorname{Tr}\_A\rho\_{\mathrm E} = \operatorname{Tr}\_A\rho\_{\mathrm C} = \frac{I_2}{2}. \\]

Thus neither local subsystem, considered alone, contains enough information to distinguish the two joint states.

### 4.2 Equality under local response protocols

Consider a response protocol consisting of arbitrary local CPTP operations applied separately to \\(A\\) or \\(B\\), followed by local measurements on the same subsystem, with no joint measurement and no interaction coupling the two subsystems.

For any local CPTP map \\(\mathcal E_A\\),

\\[ \rho_A^{\mathcal E} = \mathcal E_A(\rho_A). \\]

Since the initial reduced states are equal,

\\[ \mathcal E_A \left( \operatorname{Tr}\_B\rho\_{\mathrm E} \right) = \mathcal E_A \left( \operatorname{Tr}\_B\rho\_{\mathrm C} \right). \\]

Therefore all local outcome probabilities at \\(A\\) agree. The same argument applies at \\(B\\).

Hence

\\[ \boxed{ \rho\_{\mathrm E} \sim\_{\mathfrak P\_{\mathrm{local}}} \rho\_{\mathrm C}. } \\]

This equality holds for the entire family of such independent local operations, not merely for one selected measurement.

The restriction is essential. If the protocol permits a joint measurement, a shared interaction, or a suitable entangling operation followed by joint readout, the states can be distinguished.

### 4.3 Different joint correlation structure

For both states,

\\[ \langle\sigma_z\otimes\sigma_z\rangle=1. \\]

But their \\(x\\)-axis correlations differ.

For the entangled state,

\\[ \langle\Phi^+| \sigma_x\otimes\sigma_x |\Phi^+\rangle=1. \\]

For the classical mixture,

\\[ \operatorname{Tr} \left[ \rho\_{\mathrm C} (\sigma_x\otimes\sigma_x) \right]=0. \\]

Thus

\\[ \boxed{ K\_{\rho\_{\mathrm E}}(\sigma_x,\sigma_x)=1, \qquad K\_{\rho\_{\mathrm C}}(\sigma_x,\sigma_x)=0. } \\]

Their Pauli correlation tensors are

\\[ T(\rho\_{\mathrm E}) = \begin{pmatrix} 1&0&0\\\ 0&-1&0\\\ 0&0&1 \end{pmatrix}, \\]

and

\\[ T(\rho\_{\mathrm C}) = \begin{pmatrix} 0&0&0\\\ 0&0&0\\\ 0&0&1 \end{pmatrix}. \\]

Consequently,

\\[ \\|T(\rho\_{\mathrm E})\\|\_F=\sqrt3, \qquad \\|T(\rho\_{\mathrm C})\\|\_F=1. \\]

The first state is entangled; the second is separable. Yet the prescribed local response protocol cannot distinguish them.

### 4.4 Proposition: existence of CCD pairs

Proposition 3 — Local-response degeneracy of distinct joint states.

There exist two bipartite quantum states with identical local reduced states and identical outcome statistics under every independent local quantum operation, but with different joint correlation tensors and different entanglement properties.

Proof. The states \\(\rho\_{\mathrm E}\\) and \\(\rho\_{\mathrm C}\\) above have identical maximally mixed local marginals. Any local CPTP operation followed by a local measurement depends only on the relevant reduced state, so all local response statistics coincide. Their \\(xx\\) correlation values differ, and one state is entangled while the other is separable. \\(\square\\)

This is a direct demonstration of CCD under the stated protocol. The result relies on the familiar distinction between local and joint measurements; it is not claimed as a new quantum phenomenon.

### 4.5 What resolves the degeneracy?

A joint measurement of

\\[ M\_{xx}=\sigma_x\otimes\sigma_x \\]

immediately distinguishes the two states:

\\[ \langle M\_{xx}\rangle\_{\rho\_{\mathrm E}}=1, \qquad \langle M\_{xx}\rangle\_{\rho\_{\mathrm C}}=0. \\]

Thus the degeneracy is not absolute. It is relative to the response protocol.

This distinction is essential to the CCD interpretation. The claim is not that correlation structure is fundamentally unknowable. It is that a particular family of causal-response data may be insufficient to reconstruct it.

## 5. The geometry of response-equivalence classes

### 5.1 Fibers as regions of indistinguishable physical states

The response map partitions the state space into equivalence classes:

\\[ \mathcal S = \bigcup\_{r\in\mathscr R(\mathcal S)} \mathscr R^{-1}(r). \\]

Each fiber contains all states that generate the same response profile.

The geometry of these fibers determines the extent of CCD. A singleton fiber means the response protocol uniquely identifies the state. A multidimensional fiber means that multiple states remain consistent with exactly the same response data.

For linear response probabilities, the fibers are intersections of the quantum state space with affine subspaces:

\\[ \mathscr R^{-1}(r) = \left( \rho_0+\mathcal D\_{\mathfrak P} \right) \cap\mathcal S, \\]

where \\(\rho_0\\) is any state producing response profile \\(r\\).

The positivity constraint makes the fiber a convex, generally compact subset of the state space.

### 5.2 Degeneracy dimension

Define the local dimension of a response-equivalence fiber at a full-rank state \\(\rho\\) as

\\[ d\_{\mathrm{CCD}}(\rho) = \dim T\_\rho \left( \mathscr R^{-1}(\mathscr R(\rho)) \right), \\]

where \\(T\_\rho\\) denotes the tangent space of the fiber at \\(\rho\\).

For a linear response map, away from positivity-boundary complications,

\\[ d\_{\mathrm{CCD}} = \dim\mathcal D\_{\mathfrak P}. \\]

This quantity measures the number of independent infinitesimal state variations that preserve all response data.

It is a proposed CCD structural index. It should not be confused with the number of independent correlations: a single invisible operator direction can change several correlation observables, while many invisible directions may affect only one restricted sector of correlation space.

### 5.3 Correlation-space projection

Let \\(\mathcal C\\) denote a real vector space of selected correlation descriptors. For a linear family of correlation observables \\(\\{C\_\mu\\}\\), define

\\[ \mathscr K(\rho) = \left( \operatorname{Tr}(C\_\mu\rho) \right)\_\mu. \\]

The image of a response fiber in correlation space is

\\[ \mathcal K_r = \left\\{ \mathscr K(\rho): \rho\in\mathscr R^{-1}(r) \right\\}. \\]

If \\(\mathcal K_r\\) is a single point, the correlation descriptor is determined by response data.

If \\(\mathcal K_r\\) contains more than one point, correlation information varies while the response profile remains fixed.

The geometry of \\(\mathcal K_r\\) is potentially more informative than the scalar dimension of the state-space fiber. It identifies which correlation configurations are compatible with the same response behavior.

### 5.4 A correlation-degeneracy measure

For a chosen metric \\(d\_{\mathcal C}\\) on correlation space, define the diameter of the correlation image of a response fiber:

\\[ \boxed{ \Delta\_{\mathrm{CCD}}(r) = \sup\_{\rho,\sigma\in\mathscr R^{-1}(r)} d\_{\mathcal C} \left( \mathscr K(\rho),\mathscr K(\sigma) \right). } \\]

If

\\[ \Delta\_{\mathrm{CCD}}(r)=0, \\]

the chosen correlation descriptor is fixed by the response profile \\(r\\).

If

\\[ \Delta\_{\mathrm{CCD}}(r)>0, \\]

the response data leave a nonzero range of possible correlation structures unresolved.

For a correlation tensor with Frobenius metric,

\\[ d\_{\mathcal C}(T\_\rho,T\_\sigma) = \\|T\_\rho-T\_\sigma\\|\_F. \\]

This yields a quantitative measure of the maximum correlation ambiguity compatible with a response record.

The measure depends on the selected correlation descriptor and on the physical state constraints. It is not a universal measure of unknowability.

### 5.5 Operationally invisible relational information

We define the response-invisible relational information of a state as the portion of its joint-state structure that can vary among states in the same response-equivalence class.

A simple pairwise measure is

\\[ \mathcal I\_{\mathrm{rel}}(\rho\mid\mathfrak P,\mathscr K) = \sup\_{\sigma\sim\_{\mathfrak P}\rho} d\_{\mathcal C} \left( \mathscr K(\rho),\mathscr K(\sigma) \right). \\]

This quantity is zero when the correlation descriptor is uniquely determined by the response profile. It is positive when another response-equivalent state has a different correlation signature.

It should be interpreted as an ambiguity measure relative to an experiment family, not as an intrinsic entropy of the physical state.

A more information-theoretic construction is possible if one introduces a prior distribution over states in a response fiber. Let \\(\mu_r\\) be a probability measure on \\(\mathscr R^{-1}(r)\\). The conditional uncertainty in a correlation descriptor could then be expressed as

\\[ H\_\mu(\mathscr K\mid\mathscr R=r), \\]

where the entropy definition must be adapted to whether the descriptor is discrete, continuous, or operator-valued.

This alternative depends on the chosen prior and coarse-graining. The geometric diameter above avoids that additional dependence.

## 6. The CCD classification theorem program

### 6.1 The central classification problem

The primary objective is to determine the maximal correlation information that is constant on each response-equivalence class.

Let \\(\mathfrak K\\) be a family of correlation observables. Define the response-invariant correlation subspace

\\[ \mathfrak K\_{\mathrm{vis}} = \left\\{ C\in\mathfrak K: \operatorname{Tr}(C\rho) = \operatorname{Tr}(C\sigma) \\;\text{whenever}\\; \rho\sim\_{\mathfrak P}\sigma \right\\}. \\]

The complementary family consists of correlation observables that may vary within at least one response-equivalence class.

For a linear response map, the natural operator-space condition is

\\[ C\in\mathcal V\_{\mathfrak P} \\]

up to identity components and the state-normalization constraint.

This suggests a classification theorem based on the relationship between two spaces:

\\[ \mathcal V\_{\mathfrak P} \quad\text{and}\quad \mathcal V\_{\mathfrak K}. \\]

Their intersection contains correlation information accessible to the response protocol. Correlation directions outside the response span are potential sources of CCD.

### 6.2 The response–correlation decomposition theorem

Theorem 4 — Linear decomposition of reconstructible and invisible observables.

Let \\(\mathcal V\_{\mathfrak P}\\) be the real span of the effective response operators of a linear response protocol. Let \\(C\\) be any Hermitian observable. Then there exists a unique Hilbert–Schmidt orthogonal decomposition

\\[ C=C\_{\mathrm{vis}}+C\_{\mathrm{inv}}, \\]

where

\\[ C\_{\mathrm{vis}}\in\mathcal V\_{\mathfrak P}, \qquad C\_{\mathrm{inv}}\in\mathcal V\_{\mathfrak P}^{\perp}. \\]

For every response-equivalent pair \\(\rho,\sigma\\),

\\[ \operatorname{Tr} \left[ C(\rho-\sigma) \right] = \operatorname{Tr} \left[ C\_{\mathrm{inv}}(\rho-\sigma) \right]. \\]

Therefore the response-visible component is fixed by the response data, while only the response-invisible component can contribute to differences in the observable expectation value.

Proof. The decomposition exists and is unique because every finite-dimensional inner-product space admits an orthogonal projection onto a subspace and its orthogonal complement. For response-equivalent states, \\(\Delta=\rho-\sigma\\) lies in \\(\mathcal V\_{\mathfrak P}^{\perp}\\). Hence

\\[ \operatorname{Tr}(C\_{\mathrm{vis}}\Delta)=0, \\]

which gives the stated result. \\(\square\\)

This theorem is elementary linear algebra. Its CCD significance is that it identifies the precise operator-space location of the information inaccessible to the response protocol.

### 6.3 The complete CCD classification conjecture

The central conjectural result concerns correlation structures rather than individual observables.

CCD Classification Conjecture. For a fixed physical theory, state domain, and response protocol \\(\mathfrak P\\), there exists a minimal family of correlation invariants

\\[ \mathscr J\_{\mathrm{CCD}} = \\{J_1,J_2,\ldots,J_m\\} \\]

such that:

1. Every \\(J_k\\) is well-defined on the response-equivalence fibers.
2. The family separates the physically relevant correlation classes within each fiber.
3. Equality of all \\(J_k\\) is equivalent to the selected physical equivalence relation.
4. The classification is stable under the admissible perturbations of the experimental model.
5. The invariant family is minimal relative to the stated equivalence relation and observable domain.

Formally, if \\(\sim\_{\mathrm{phys}}\\) is the chosen equivalence relation on states, the target is

\\[ \boxed{ \mathscr R(\rho)=\mathscr R(\sigma) \\;\land\\; J_k(\rho)=J_k(\sigma)\\;\forall k \iff \rho\sim\_{\mathrm{phys}}\sigma. } \\]

This conjecture is deliberately relative to the physical equivalence relation. If \\(\sim\_{\mathrm{phys}}\\) is equality of density operators, full state tomography already supplies a complete reconstruction. The interesting problem is whether a compact, physically meaningful set of correlation invariants can classify the residual structures without reconstructing every detail of the state.

### 6.4 Minimality and irreducible relational information

A classification is not minimal merely because it contains a finite number of invariants. Some invariants may be redundant or derivable from others.

A family \\(\mathscr J\\) is minimal if removal of any invariant \\(J_k\\) causes two physically inequivalent structures to become indistinguishable, within the stated classification domain.

For example, in a restricted two-qubit model, local marginal data and a single \\(zz\\) correlation do not distinguish the two states in Section 4. Adding an \\(xx\\) correlation resolves that particular degeneracy. But this does not establish that \\(xx\\) is a universally minimal invariant; a different state family may require other observables.

The general problem is to determine a minimal generating set of correlation invariants for each physically motivated response-equivalence class.

### 6.5 A hierarchy of CCD classifications

A useful program would proceed through increasingly demanding classifications:

| Classification level         | Mathematical target                          | Required result                          |
| ---------------------------- | -------------------------------------------- | ---------------------------------------- |
| I. Existence                 | Find \\(\rho\ne\sigma\\) with equal response | Explicit CCD pair                        |
| II. Correlation separation   | Find \\(K\\) with \\(K\_\rho\ne K\_\sigma\\) | Joint witness                            |
| III. Fiber geometry          | Characterize \\(\mathscr R^{-1}(r)\\)        | Dimension and structure                  |
| IV. Invariant classification | Find separating \\(J_k\\)                    | Completeness theorem                     |
| V. Stability                 | Bound changes in inferred class              | Robustness theorem                       |
| VI. Physical universality    | Extend across models and domains             | Model-independent or universality result |

The first two levels are already demonstrated by elementary quantum examples. The higher levels contain the principal open research.

## 7. Relationship to established theories

### 7.1 Quantum state tomography

Quantum state tomography asks whether a state can be reconstructed from measurement statistics. A measurement family is informationally complete if distinct states always produce distinguishable outcome distributions.

CCD asks a more targeted question: whether a family of causal-response statistics is informationally complete with respect to joint correlation structure.

The mathematical connection is direct. Incomplete measurements admit sets of states compatible with the same data; these are often described as compatible-state sets or non-identifiable state families. The existence of such sets is established in quantum tomography.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PubMed Central (PMC)+2



CCD differs in its intended emphasis: the measurement family is not arbitrary. It is selected to represent a causal-response protocol, and the unresolved information is analyzed specifically in terms of relational correlations.

### 7.2 Operational equivalence

Operational equivalence is a general concept: two physical descriptions are equivalent relative to an experiment if every allowed operation and measurement in that experiment yields the same statistics.

CCD uses this principle to define equivalence classes under response-only experiments.

The important restriction is the word response-only. If joint correlation measurements are included in the protocol, the equivalence classes may become much smaller or disappear altogether.

Thus CCD is not a replacement for operational equivalence. It is a proposed classification of the correlation structure inside the equivalence classes generated by a specific family of causal-response experiments.

### 7.3 Causal inference and intervention data

Classical causal inference distinguishes observational distributions from interventional distributions. Different causal models can reproduce the same observational data, while interventions may separate them. Quantum causal inference generalizes this issue to quantum systems, where measurements and interventions can disturb the systems under study.

Experimental work has demonstrated the use of quantum causal tomography to infer causal structures, while other work has examined how quantum causal influences can be identified from process data.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC+2



CCD investigates a complementary inverse problem. Even after a response protocol has been specified, distinct joint-state correlations may remain indistinguishable to that protocol. The issue is not only whether interventions reveal causal structure, but also what relational information remains outside their reach.

### 7.4 Local tomography and composite-state reconstruction

In standard finite-dimensional complex quantum theory, a sufficiently rich collection of local measurement settings combined through coordinated joint outcome records can reconstruct a bipartite state. The distinction is between performing local measurements separately and collecting their joint statistics.

The CCD example in Section 4 deliberately restricts the response protocol to local marginals. It does not claim that the joint state is unreconstructible by all local measurement apparatuses. Coordinated local measurements with joint outcome recording can measure correlations such as

\\[ \langle\sigma_x\otimes\sigma_x\rangle. \\]

Thus the distinction is not simply between local and nonlocal instruments. It is between response data that preserve only local statistics and data that retain the joint outcome relationships.

This distinction is essential when comparing CCD to local tomography and informational completeness.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.quantuminformation.it\&sz=32)

quantuminformation.it+1



### 7.5 Process tomography

A response protocol may probe not only a state but also a dynamical process. In that case, the unknown object may be a quantum channel, process tensor, or higher-order transformation.

The CCD problem can be generalized by replacing the state space \\(\mathcal S\\) with a process space \\(\mathcal Q\\) and defining

\\[ \mathscr R\_{\mathrm{proc}}:\mathcal Q\to\mathcal Y. \\]

Two processes are response-equivalent if they produce identical response profiles under the allowed input states and interventions. Their internal memory, temporal correlations, or multi-time process structure may nevertheless differ.

This extension is potentially important, but it should not be conflated with the state-based theory developed in the present paper.

## 8. Extension to dynamical and causal-response theories

The state-based formulation is the simplest realization of CCD. A more general framework should accommodate physical systems whose response depends on both an initial state and a dynamical law.

### 8.1 State–dynamics degeneracy

Let a physical model be specified by

\\[ \mathfrak M=(\rho,\mathcal G), \\]

where \\(\rho\\) is an initial state and \\(\mathcal G\\) is a dynamical generator, channel, or evolution law.

The measured response is then

\\[ R\_{\mathfrak M}(p) = R\_{\rho,\mathcal G}(p). \\]

Two models may satisfy

\\[ R\_{\rho,\mathcal G}(p) = R\_{\sigma,\mathcal H}(p) \qquad\forall p\in\mathfrak P \\]

even when

\\[ \rho\ne\sigma, \qquad \mathcal G\ne\mathcal H. \\]

This is a stronger degeneracy: the same response data may be compatible with differences in both initial correlation structure and dynamical organization.

It introduces a second inverse problem:

\\[ \text{Can state structure and dynamical structure be separately identified?} \\]

Without independent preparation and process calibration, the two may be confounded. A response difference attributed to a state may instead arise from a change in dynamics, or vice versa.

### 8.2 Linear-response formulation

For a system with Hamiltonian

\\[ H(t)=H_0-\epsilon(t)X, \\]

the linear response of an observable \\(Y\\) is conventionally expressed through a susceptibility,

\\[ \delta\langle Y(t)\rangle = \int\_{-\infty}^{t} \chi\_{YX}(t,t')\epsilon(t')\\,dt'. \\]

For an equilibrium state under standard assumptions, the Kubo response function takes the form

\\[ \chi\_{YX}(t,t') = \frac{i}{\hbar} \theta(t-t') \langle[Y_H(t),X_H(t')]\rangle. \\]

This expression depends on the state and the dynamical evolution. It is therefore possible in principle for different states to produce identical selected response functions while differing in other expectation values.

A CCD analysis in this setting would ask whether the family of measured commutator expectations determines the joint correlation functions of interest.

The answer depends on the observable algebra, state domain, symmetries, and completeness of the measured response functions. The Kubo expression itself does not establish a new degeneracy theorem; it supplies a familiar physical setting in which the inverse problem can be investigated.

### 8.3 Response functions and correlation functions

In equilibrium statistical mechanics, response and correlation functions can be related by fluctuation–dissipation relations under specific assumptions. This creates an important boundary condition for CCD.

If a complete family of response functions, together with temperature, equilibrium assumptions, and the relevant dynamics, determines the corresponding correlation functions, then those correlations are not CCD-invisible within that model.

Conversely, if the response protocol measures only a restricted set of susceptibilities, or if the system is out of equilibrium, nonstationary, or subject to incomplete observation, the relationship may be insufficient to reconstruct all correlations.

Therefore CCD should not be interpreted as asserting a universal separation between response and correlation. It asks when, and under which assumptions, the response data fail to determine the correlation structure.

### 8.4 Multi-time correlation degeneracy

For temporally extended systems, define a multi-time correlation

\\[ C\_\rho(t_1,\ldots,t_n) = \langle A_1(t_1)\cdots A_n(t_n) \rangle\_\rho. \\]

A response protocol may access only selected derivatives of expectation values with respect to applied perturbations. It may not determine all multi-time moments.

This motivates a temporal CCD classification:

\\[ \mathscr R\_{\mathrm{multi}}(\mathfrak M) = \left( R\_{\mathfrak M}(p) \right)\_{p\in\mathfrak P}, \\]

with multi-time correlation signature

\\[ \mathscr K\_{\mathrm{multi}}(\mathfrak M) = \left( C\_{\mathfrak M}(t_1,\ldots,t_n) \right)\_{n,\\{t_i\\}}. \\]

The corresponding classification would identify which temporal correlation structures remain invariantly undetermined by the accessible response functions.

This extension is especially relevant to open quantum systems, non-Markovian dynamics, quantum memories, and process-tensor approaches. It requires a separate treatment of temporal ordering and intervention placement.

## 9. Experimental program

### 9.1 Experimental objective

The primary experiment should establish three facts:

1. Two candidate preparations produce indistinguishable response profiles under a declared response protocol.
2. Their joint correlation structures differ.
3. A specified joint measurement resolves the difference.

The experiment must not define the response protocol so narrowly that the result becomes tautological. Its restrictions should correspond to a physically meaningful class of measurements or interventions.

### 9.2 Proposed two-qubit implementation

A natural implementation uses two entangled-photon polarization qubits, trapped-ion qubits, or another controllable bipartite platform.

Prepare two states:

\\[ \rho\_{\mathrm E} = |\Phi^+\rangle\langle\Phi^+|, \\]

\\[ \rho\_{\mathrm C} = \frac12|00\rangle\langle00| + \frac12|11\rangle\langle11|. \\]

The protocol has two stages.

Stage A: response-only characterization

- Measure the local marginal statistics of subsystem \\(A\\).
- Measure the local marginal statistics of subsystem \\(B\\).
- Apply a prespecified collection of local operations independently to either subsystem.
- Compare all local output distributions.
- Establish whether the response profiles are statistically indistinguishable within the specified precision.

Stage B: joint correlation characterization

- Measure \\(\sigma_x\otimes\sigma_x\\).
- Measure \\(\sigma_y\otimes\sigma_y\\).
- Measure \\(\sigma_z\otimes\sigma_z\\).
- Reconstruct the connected correlation tensor.
- Compare the correlation signatures of the two preparations.

The predicted result is that Stage A cannot distinguish the states under the restricted protocol, whereas Stage B can.

Predicted state comparison

| Observable                                  | Entangled \\(\rho\_{\mathrm E}\\) | Classical \\(\rho\_{\mathrm C}\\) |
| ------------------------------------------- | --------------------------------- | --------------------------------- |
| Local \\(A\\) marginal                      | \\(I/2\\)                         | \\(I/2\\)                         |
| Local \\(B\\) marginal                      | \\(I/2\\)                         | \\(I/2\\)                         |
| \\(\langle\sigma_x\otimes\sigma_x\rangle\\) | \\(1\\)                           | \\(0\\)                           |
| \\(\langle\sigma_y\otimes\sigma_y\rangle\\) | \\(-1\\)                          | \\(0\\)                           |
| \\(\langle\sigma_z\otimes\sigma_z\rangle\\) | \\(1\\)                           | \\(1\\)                           |
| Entanglement                                | Entangled                         | Separable                         |

The comparison is exact in the ideal model. Experimental implementation will require state-preparation verification and statistical confidence bounds.

### 9.3 Quantifying response equivalence

Let \\(p_A(a\mid x,\rho)\\) denote the local outcome distribution at \\(A\\) for response setting \\(x\\). A direct measure of response-profile difference between candidate states is

\\[ D\_{\mathrm{resp}}(\rho,\sigma) = \sup\_{x\in\mathfrak P_A} \frac12\sum_a \left| p_A(a\mid x,\rho)-p_A(a\mid x,\sigma) \right| + \sup\_{y\in\mathfrak P_B} \frac12\sum_b \left| p_B(b\mid y,\rho)-p_B(b\mid y,\sigma) \right|. \\]

The exact equality condition is

\\[ D\_{\mathrm{resp}}(\rho,\sigma)=0. \\]

In experiments, one instead seeks a confidence upper bound

\\[ D\_{\mathrm{resp}}(\rho,\sigma)\le\epsilon_R. \\]

The value \\(\epsilon_R\\) must incorporate finite-sample uncertainty and relevant systematic errors. It is not enough to report that a statistical test failed to reject equality. The protocol should use an equivalence-testing criterion with a prespecified tolerance.

### 9.4 Quantifying correlation separation

For the same pair of states, define

\\[ D\_{\mathrm{corr}}(\rho,\sigma) = \\|T(\rho)-T(\sigma)\\|\_F. \\]

The proposed CCD experimental signature is

\\[ D\_{\mathrm{resp}}(\rho,\sigma)\le\epsilon_R, \qquad D\_{\mathrm{corr}}(\rho,\sigma)\ge\delta_C, \\]

where \\(\delta_C\\) is a prespecified positive separation threshold supported by a confidence interval.

The two inequalities should be evaluated independently. The correlation estimate should not be used to define or tune the response-equivalence tolerance after observing the data.

### 9.5 The importance of controls

A credible test should include:

- Independent calibration of the local measurement devices.
- Verification that local operations do not accidentally create a joint interaction.
- Randomization of preparation and measurement order.
- Control experiments with known product states.
- Repeated preparation of both candidate states.
- An independent joint-correlation measurement.
- An audit of detection efficiency and setting-dependent loss.
- A prespecified statistical equivalence margin.

If the response protocol is supposed to contain every local operation in a specified class, the experiment must explain how its finite set of tested operations represents that larger class. A finite experiment cannot establish equality for an unbounded continuum of operations without additional theoretical assumptions.

### 9.6 General experimental strategy

The two-qubit example is a proof of principle. More ambitious CCD tests should search for response-equivalent pairs whose joint structures differ in ways not captured by elementary correlation tensors.

Potential targets include:

1. States with identical one- and two-body marginals but different multipartite correlations.
2. States with identical selected susceptibilities but different higher-order cumulants.
3. Quantum states with identical response profiles under a restricted intervention algebra but different entanglement spectra.
4. Dynamical processes with identical selected linear responses but different memory kernels.
5. Many-body states with identical local response functions but distinct long-range correlation structure.

The most significant experiment would not merely repeat the two-qubit demonstration. It would validate a predicted CCD invariant or classification that is not already determined by standard tomography of the measured observables.

## 10. Falsifiability and decisive tests

### 10.1 Falsification of a proposed CCD pair

For a proposed pair \\((\rho,\sigma)\\), the CCD claim fails under protocol \\(\mathfrak P\\) if there exists an allowed response experiment \\(p\\) such that

\\[ R\_\rho(p)\ne R\_\sigma(p). \\]

The states are then not response-equivalent under the declared protocol.

This does not refute CCD as a general classification problem. It refutes the specific candidate pair.

### 10.2 Falsification of an invisible-correlation claim

Suppose a correlation observable \\(C\\) is claimed to be invisible to the response protocol. The claim is false if there exist response-equivalent states for which its expectation is not constant, or, conversely, if the proposed classification asserts variability but the physical constraints force

\\[ \operatorname{Tr}(C\rho) = \operatorname{Tr}(C\sigma) \\]

throughout the relevant fiber.

The appropriate test is an analytic characterization of the fiber, not merely a finite numerical search.

### 10.3 Falsification of a completeness theorem

Suppose a family of invariants \\(\\{J_k\\}\\) is claimed to classify the correlation structures inside every response-equivalence class.

A counterexample consists of two physically inequivalent states satisfying

\\[ \mathscr R(\rho)=\mathscr R(\sigma) \\]

and

\\[ J_k(\rho)=J_k(\sigma) \qquad\forall k, \\]

while

\\[ \rho\not\sim\_{\mathrm{phys}}\sigma. \\]

One such pair falsifies the completeness claim.

### 10.4 Falsification of a claimed irreducible structure

A proposed CCD invariant is not a substantive new invariant if it can be expressed as a function of an already-established complete set of invariants under the same physical equivalence relation.

The novelty claim would then fail, even if the invariant remains convenient or pedagogically useful.

### 10.5 Identifiability restored by additional measurements

A particularly important test is whether a proposed degeneracy disappears when additional observables are added.

Let \\(\mathfrak P_1\subset\mathfrak P_2\\) be two response protocols, with the second containing all experiments in the first plus additional measurements. Then

\\[ \rho\sim\_{\mathfrak P_2}\sigma \implies \rho\sim\_{\mathfrak P_1}\sigma. \\]

The reverse implication need not hold.

Thus adding experiments can only refine or preserve the equivalence partition; it cannot merge states that were already distinguishable.

A useful CCD classification should predict which minimal additions to the response protocol resolve a particular degeneracy.

## 11. Limitations and unresolved mathematical questions

### 11.1 Dependence on protocol definition

CCD is relative to a chosen experiment family. Without specifying the allowed interventions, measurements, readout channels, and post-processing, the phrase “same causal-response behavior” is incomplete.

### 11.2 Distinguishability is not necessarily causal explanation

Two states that generate identical response data may still differ in their causal organization. Conversely, two states that differ in correlation structure do not necessarily differ in causal influence.

CCD classifies an information deficit in the response protocol. It does not automatically identify an underlying causal ontology.

### 11.3 State-space positivity

The response-invisible subspace is a linear-algebraic object, but physical density operators occupy a convex positive subset of the Hermitian operator space.

Not every invisible direction connects two admissible states at every point. Boundary states, such as pure states, require special care because positivity may prevent perturbations in otherwise mathematically allowed directions.

### 11.4 Correlation descriptors may be incomplete

A scalar correlation measure can fail to distinguish different tensors or higher-order structures. A complete classification may require an infinite hierarchy for continuous-variable or field-theoretic systems.

### 11.5 Model dependence

The state-based CCD theory assumes a fixed measurement and dynamical model. If the apparatus itself is unknown, state and measurement ambiguities can become coupled. Joint state-and-measurement tomography demonstrates that incomplete measurement information can prevent unique state identification and instead leave a compatible set of density operators.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nist.gov\&sz=32)

NIST+1



### 11.6 No general theorem of universal causal blindness

The present analysis does not establish that causal-response measurements are fundamentally incapable of reconstructing correlations. Informationally complete measurement families can reconstruct the state. Equilibrium response relations can also connect particular response functions to correlation functions under additional assumptions.

The claim is conditional: a specified response protocol may be incomplete with respect to a specified correlation structure.

### 11.7 No ontological conclusion

The fact that a response protocol cannot distinguish two states does not prove that the states are indistinguishable in reality. It proves only that the chosen data are insufficient to distinguish them.

This distinction separates epistemic non-identifiability from physical identity.

## 12. Novelty assessment

### 12.1 Established components

The following elements are established:

- Operational equivalence under a restricted family of experiments.
- Informational incompleteness and non-identifiability in quantum-state tomography.
- The characterization of measurement indistinguishability through operator-space orthogonality.
- The use of compatible-state sets when measurement data do not uniquely identify a state.
- The distinction between observational and interventional data in causal inference.
- The use of interventions and quantum causal tomography to identify causal structure.

These are not new discoveries of CCD. They provide its mathematical foundations.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC+3



### 12.2 What is proposed here

The proposed CCD contribution is a unified classification problem with four linked objects:

\\[ \boxed{ \text{response map} \longrightarrow \text{equivalence fibers} \longrightarrow \text{correlation images} \longrightarrow \text{invariant classification}. } \\]

The response map defines what the experiment can see. Its fibers identify the states that it cannot distinguish. The correlation images show how joint structure varies inside those fibers. The invariant classification determines which variations are physically meaningful and how they can be distinguished.

This provides a precise mathematical program for answering how much relational information can vary while causal-response behavior remains fixed.

### 12.3 What would count as genuine novelty?

A substantive new result would require at least one of the following:

1\. A new complete classification theorem. Establish a nontrivial, physically motivated equivalence relation and derive a minimal complete set of correlation invariants within its response fibers.

2\. A new correlation-invisibility theorem. Prove that a specified class of correlation functions cannot be reconstructed from a broad, precisely defined class of causal-response measurements.

3\. A new minimal-completion theorem. Determine the smallest additional family of joint measurements needed to eliminate a given response degeneracy.

4\. A nontrivial stability theorem. Establish sharp bounds on how much correlation structure can vary among states whose response profiles agree within a finite experimental tolerance.

5\. A dynamical CCD theorem. Identify physically inequivalent states or processes with identical full response profiles under a meaningful class of interventions, while proving that a new invariant distinguishes their relational structure.

The strongest initial target is the correlation-invisibility theorem: a theorem that characterizes the exact subspace of joint-state information invisible to a specified response protocol and identifies the minimal measurement extensions that recover it.

### 12.4 Novelty verdict



Mathematical formulation established

Classification open



The existence of CCD pairs under restricted measurement protocols is straightforward to establish and is closely related to established quantum tomography and operational-equivalence theory. The broad classification proposed here is not established by the examples or elementary theorems in this paper.

The potential novelty lies in a new classification of response-equivalence fibers, especially one that yields a minimal and physically interpretable description of the correlation structures invisible to causal-response data.

The name Correlation–Causation Degeneracy is a proposed label for this research program, not evidence that the underlying mathematical phenomenon has never been studied.

## 13. Research program and priority sequence

The next stage should not begin by proposing more correlation names. It should begin with a precise classification theorem in a controlled model.

### Phase I — Finite-dimensional state classification

1. Fix a bipartite or multipartite Hilbert space.
2. Define the response protocol as a finite or algebraically generated family of operations and measurements.
3. Compute its effective operator span.
4. Determine the response-invisible subspace.
5. Characterize its intersection with the physical state space.
6. Identify correlation observables that vary on each response fiber.

Deliverable: an exact characterization of response-invisible correlation directions.

### Phase II — Minimal correlation invariants

1. Construct a hierarchy of connected correlation tensors.
2. Determine which tensor components lie in the response-visible span.
3. Identify redundant invariants.
4. Prove a separation theorem for the selected state family.
5. Determine whether the classification is complete under local-unitary, operational, or another explicitly declared equivalence relation.

Deliverable: a minimal or provably sufficient CCD invariant set.

### Phase III — Robust classification

1. Replace exact response equality by a tolerance condition.
2. Bound the diameter of the compatible correlation set.
3. Derive confidence regions for the correlation invariants.
4. Analyze stability near pure-state and rank-deficient boundaries.
5. Determine the number of measurements required to achieve a prescribed correlation resolution.

Deliverable: finite-precision CCD bounds.

### Phase IV — Dynamical extension

1. Replace states with quantum channels or process tensors.
2. Specify intervention sequences and temporal measurement domains.
3. Characterize process-equivalence fibers.
4. Identify hidden memory or multi-time correlation structure.
5. Establish whether the state-level invariants extend to the process setting.

Deliverable: a dynamical CCD classification.

### Phase V — Experimental validation

1. Demonstrate a response-equivalent pair.
2. Verify distinct joint correlations.
3. Add the predicted minimal resolving measurement.
4. Compare observed degeneracy with the theoretical fiber.
5. Test robustness under realistic noise.

Deliverable: experimental validation of a classification prediction, rather than merely another demonstration that local and joint measurements differ.

## 14. Conclusion

Correlation–Causation Degeneracy identifies a fundamental inverse problem in the reconstruction of physical reality.

A response experiment does not necessarily reveal the entire joint state. It reveals the information encoded in the particular operations, observables, and readout procedures that constitute the experiment. Distinct states can therefore produce identical response profiles while retaining different relational structures.

The mathematical architecture developed here is

\\[ \boxed{ \begin{aligned} &\mathcal S \xrightarrow{\\;\mathscr R\\;} \mathcal Y,\\\\[2mm] &\mathscr R^{-1}(r) = \text{response-equivalence fiber},\\\\[2mm] &\mathscr K\big(\mathscr R^{-1}(r)\big) = \text{compatible correlation structures}. \end{aligned} } \\]

The central result is that response equivalence is governed, for linear protocols, by the orthogonal complement of the effective response-operator span. This provides an exact algebraic description of the directions in state space that remain invisible to the selected response measurements.

The two-qubit construction demonstrates that identical local response behavior can coexist with different joint correlations and different entanglement properties. The more ambitious objective is to determine whether the complete correlation structure inside a response-equivalence class can be classified by a minimal family of invariants.

The most important unresolved question is therefore:

\\[ \boxed{ \text{What is the maximal relational information that remains undetermined by a complete specified causal-response protocol?} } \\]

A successful answer would establish more than the familiar fact that correlations and causal responses are different. It would provide a rigorous boundary between what a response-based physical theory can reconstruct and what remains underdetermined until joint relational measurements are introduced.

The decisive mathematical achievement would be a theorem that identifies the complete correlation-invisibility structure of a physically meaningful response class, together with the minimal additional observations required to resolve it.

That is the substantive research target of CCD.

## References and foundational literature

1\. M. Christandl and R. Renner, “Reliable quantum state tomography,” Physical Review Letters 109, 120403 (2012). [DOI](https://doi.org/10.1103/PhysRevLett.109.120403?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pubmed.ncbi.nlm.nih.gov\&sz=32)

PubMed



2\. A. C. Keith, C. H. Baldwin, S. Glancy, and E. Knill, “Joint Quantum State and Measurement Tomography with Incomplete Measurements,” Physical Review A 98, 042318 (2018). [DOI](https://doi.org/10.1103/PhysRevA.98.042318?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nist.gov\&sz=32)

NIST+1



3\. “Probing quantum state space: does one have to learn everything to learn something?” Philosophical Transactions of the Royal Society A (2017). [Article](https://pmc.ncbi.nlm.nih.gov/articles/PMC5454349/?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC



4\. “Experimental test of quantum causal influences,” Nature Physics (2022). [Article](https://pmc.ncbi.nlm.nih.gov/articles/PMC8880765/?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC



5\. “A quantum advantage for inferring causal structure,” Nature Physics (2015). [Article](https://www.nature.com/articles/nphys3266?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nature.com\&sz=32)

Nature Physics



6\. I. Friend and A. Kissinger, “Identification of causal influences in quantum processes,” Physical Review A 109, 042214 (2024). [DOI](https://doi.org/10.1103/PhysRevA.109.042214?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A



7\. “Quantum tomography protocols with positivity are compressed sensing protocols,” npj Quantum Information (2015). [Article](https://www.nature.com/articles/npjqi201518?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.nature.com\&sz=32)

npj Quantum Information



8\. “Quantum Measurements in the Light of Quantum State Estimation,” PRX Quantum 3, 030306 (2022). [DOI](https://doi.org/10.1103/PRXQuantum.3.030306?utm_source=chatgpt.com).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

PRX Quantum



These references establish relevant foundations in tomography, state identifiability, and causal inference. They are not an exhaustive literature review or a certification of novelty for the proposed CCD classification.

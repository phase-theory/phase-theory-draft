Nonlocal Correlation and Local Causation: A Mathematical Framework for a Universe Whose Correlations Transcend Spacetime

Foundations, relativistic causality, quantum entanglement, and the distinction between correlation structure and physical influence

Abstract

The universe may possess a correlation structure that is nonlocal with respect to spacetime while preserving the locality of causal influence. These properties are not contradictory. They refer to different mathematical structures: correlations characterize joint probability distributions across subsystems, whereas causal influence characterizes whether a controllable intervention in one spacetime region changes the observable statistics available in another.

This paper develops a precise framework for the proposition that some physical correlations are not mediated by anything propagating through time, even though every controllable causal influence remains local. The central distinction is between a correlation relation and a dynamical transmission process. A correlation may be irreducible to independent local statistics without constituting a signal, force, particle, or message traveling between the correlated events.

The framework begins with relativistic spacetime and local algebras of observables, derives the operational criterion for causal influence, and examines how quantum entanglement satisfies that criterion while violating classical factorizability. It then introduces a relational representation in which joint correlations are fundamental mathematical data, while spacetime-local dynamics govern interventions, records, and signal transmission. The resulting picture separates three notions that are frequently conflated: geometric separation, statistical nonseparability, and causal propagation.

The analysis establishes several results within clearly specified assumptions. Quantum correlations can violate Bell inequalities without permitting faster-than-light communication. Relativistic microcausality constrains local observables without requiring every joint correlation to factorize. A correlation that is independent of any temporal transmission mechanism need not imply a backward-in-time cause, instantaneous force, or hidden communication channel. Conversely, neither Bell inequality violation nor no-signaling alone proves that correlations are ontologically outside spacetime or that no deeper dynamical mechanism exists.

The final objective is a testable theoretical architecture: a universe in which spacetime constrains the propagation of influence, while the structure of physically admissible correlations need not be exhausted by spacetime-local mediation.

Keywords: quantum nonlocality; relativistic causality; Bell inequalities; no-signaling; microcausality; entanglement; causal structure; relational ontology; spacetime emergence.

1. Introduction

Modern physics contains a fundamental asymmetry between what can be correlated and what can causally influence something else.

Two spacelike-separated quantum systems can exhibit correlations that cannot be reproduced by a broad class of classical models in which each subsystem’s response is determined by local information and shared hidden variables. Nevertheless, an observer controlling one subsystem cannot use those correlations to transmit a freely chosen message to the other observer faster than light.

This distinction is not an incidental feature of quantum mechanics. It exposes a conceptual separation between the statistical structure of a physical state and the dynamical structure of interventions upon that state.

Let and denote two physical subsystems, associated with spacetime regions and . Suppose the regions are spacelike separated. Their joint statistics are represented by

P(a,b\mid x,y),

where specify measurement settings and denote outcomes.

The distribution can be nonfactorizable:

P(a,b\mid x,y)
\neq
P(a\mid x)P(b\mid y),

while still satisfying the no-signaling conditions

\sum_b P(a,b\mid x,y)=P(a\mid x),\sum_a P(a,b\mid x,y)=P(b\mid y).

The first relation expresses statistical dependence. The latter two express the absence of operational influence through the remote measurement setting.

The central thesis of this paper is that these relations permit a coherent physical description in which the correlation structure is not modeled as a signal or physical carrier traveling between the correlated events.

However, three distinctions are essential.

* Mathematical nonseparability is not automatically proof of ontological nonlocality.
* Operational no-signaling does not, by itself, prove that every conceivable notion of causal influence is local.
* Absence of a required propagating mediator does not prove that no underlying mechanism exists.

The theory developed here therefore begins with established mathematical results and proceeds toward a more general relational interpretation without confusing interpretation with derivation.

1.1 The principal hypothesis

We consider the hypothesis

\boxed{
\text{Nonlocal correlation structure}
\quad+\quad
\text{local causal influence}.
}

The expression is meaningful only if its two components are defined independently.

Nonlocality concerns the failure of a correlation structure to admit a specified decomposition into independent local contributions. Locality of causal influence concerns the restriction that interventions cannot produce controllable effects outside the allowed causal domain.

The proposed framework does not assert that all correlations are nonlocal, that spacetime is unreal, or that quantum mechanics is incomplete. It asks whether physical theory can consistently treat correlations as relational constraints rather than as products of messages exchanged between events.

1.2 Scope of the argument

The paper distinguishes four levels of claim.

* Established theorem: a result derived within standard mathematical or physical assumptions.
* Framework result: a consequence of the definitions and axioms introduced here.
* Interpretive proposal: an ontological reading consistent with the formalism but not uniquely selected by it.
* Open conjecture: a proposed extension requiring additional proof or empirical support.

This distinction is necessary because the formalism of quantum mechanics establishes nonclassical correlations and no-signaling, but does not uniquely determine the metaphysical interpretation of those correlations.

2. Mathematical Foundations: Spacetime, Correlation, and Influence

2.1 Spacetime as a causal structure

Let spacetime be a four-dimensional differentiable manifold equipped with a Lorentzian metric of signature . The metric defines the infinitesimal interval

ds^2=g_{\mu\nu}\,dx^\mu dx^\nu.

For two events , their separation determines whether a future-directed causal curve can connect them. We write

p\preceq q

if lies in the causal future of , including the case of null separation. Otherwise, if neither event lies in the causal future of the other, the events are spacelike separated.

The causal future and past of a region are denoted by

J^+(\mathcal O),\qquad J^-(\mathcal O).

In relativistic local field theory, physical influences carried by ordinary local dynamical fields propagate within the causal structure defined by the theory. The precise propagation speed and causal cone depend on the dynamical equations and the background geometry.

This geometric restriction does not itself determine the joint probability distribution of measurements performed in spacelike-separated regions.

That distinction is the starting point of the present analysis.

2.2 Correlation is a property of a joint state

Let and denote the observable algebras associated with two subsystems. A state assigns expectation values to admissible observables. For local observables and , define the connected correlation

C_\omega(A,B)

\omega(AB)-\omega(A)\omega(B).

When

C_\omega(A,B)\neq 0,

the observables are statistically correlated in the state .

This condition says nothing by itself about whether dynamically influences . The correlation may result from a shared preparation, an entangled state, a common causal past, or other structure permitted by the model.

A factorized state satisfies

\omega(AB)=\omega(A)\omega(B)

for the observables under consideration. A nonfactorizing state does not satisfy this identity for all such pairs.

Factorization is therefore a property of a state relative to a chosen division into subsystems. It is not synonymous with causal independence.

A crucial qualification follows: a nonzero correlation is not sufficient to establish Bell nonlocality. Classical common causes also generate correlations. Stronger conditions are required to distinguish quantum nonseparability from correlations reproducible by local hidden-variable models.

2.3 Causal influence as an intervention-dependent quantity

Statistical dependence is observational. Causal influence is counterfactual: it asks what changes when one intervention is altered while the relevant background conditions are held fixed.

Let be a controllable intervention in region , and let be an observable recorded in region . Define the influence of the intervention by

\Delta_{X\rightarrow Y}

P(Y\mid \operatorname{do}(X=x_1))

P(Y\mid \operatorname{do}(X=x_0)).

Here, denotes an intervention that sets to , rather than merely conditioning on an observed value of .

For a continuous observable, the analogous response can be expressed as a functional derivative,

\chi_{Y X}

\frac{\delta \langle Y\rangle}{\delta J_X},

where is an externally controlled source coupled to the system in region .

If the response vanishes whenever lies outside the permitted causal future of , then the theory has local causal influence in the operational response sense:

\boxed{
\chi_{YX}=0
\quad
\text{for causally forbidden interventions}.
}

This is a response criterion, not a claim that every conceivable definition of causality has been exhausted. A theory might satisfy operational no-signaling while violating a stronger causal principle.

2.4 The fundamental non-equivalence

The two quantities

C_\omega(A,B)
\quad\text{and}\quad
\chi_{YX}

answer different questions.

The first measures dependence within a state. The second measures sensitivity to an intervention.

There is no general identity requiring

C_\omega(A,B)=0
\quad\Longleftrightarrow\quad
\chi_{YX}=0.

Indeed, an entangled state can have nonzero connected correlations while the local marginal statistics remain invariant under remote measurement-setting changes.

This separation is the mathematical basis for the entire framework.

3. Bell’s Theorem: Why Classical Local Factorization Fails

3.1 The local hidden-variable hypothesis

Consider two spacelike-separated measurement stations. Each station independently selects a setting or and records an outcome or .

A Bell-local hidden-variable model represents the joint statistics as

P(a,b\mid x,y)

\int_\Lambda d\lambda\,
\rho(\lambda)
P(a\mid x,\lambda)
P(b\mid y,\lambda).

Here:

* represents the hidden variables associated with the shared preparation.
* is their probability distribution.
* and are the local response probabilities.

The factorization states that, conditional on a sufficiently complete specification of , the two outcomes are independent and each local response depends only on its own setting and the shared variable.

This is a stronger condition than no-signaling. It also includes assumptions about the adequacy of the hidden-variable description and, in the standard Bell experiment, the statistical independence of measurement settings from .

3.2 Derivation of the CHSH inequality

Suppose the measurement outcomes are . Define the conditional local means

A_x(\lambda)

\sum_a aP(a\mid x,\lambda),B_y(\lambda)

\sum_b bP(b\mid y,\lambda).

Because the outcomes lie in ,

|A_x(\lambda)|\leq 1,
\qquad
|B_y(\lambda)|\leq 1.

Under Bell factorization, the correlation for settings is

E(x,y)

\int_\Lambda d\lambda\,
\rho(\lambda)A_x(\lambda)B_y(\lambda).

Consider the CHSH combination

S=E(x,y)+E(x,y’)
+E(x’,y)-E(x’,y’).

Substitution yields

\begin{aligned}
S
=\int_\Lambda d\lambda\,\rho(\lambda)
\big&A_x(B_y+B_{y'})\\\\
&+A_{x'}(B_y-B_{y'})
\\big.
\end{aligned}

For each , the triangle inequality gives

\begin{aligned}
|S_\lambda|
&\leq |B_y+B_{y’}|
+|B_y-B_{y’}|\\
&\leq 2.
\end{aligned}

The last inequality follows because . Averaging over the normalized distribution gives

\boxed{|S|\leq 2.}

This is the CHSH inequality. It follows from the stated local hidden-variable factorization and the specified outcome bounds.

3.3 Quantum violation

For a pair of qubits in the singlet state,

|\psi^-\rangle

\frac{1}{\sqrt 2}
\left(
|0\rangle_A|1\rangle_B

|1\rangle_A|0\rangle_B
\right),

the joint state is entangled. For spin measurements along unit vectors and , quantum mechanics predicts

E(\mathbf a,\mathbf b)

-\mathbf a\cdot\mathbf b.

Choose measurement directions such that the relative angles yield the standard optimal CHSH configuration. The resulting value is

|S|=2\sqrt 2.

Thus quantum theory violates the Bell-local bound while respecting the no-signaling constraints.

The bound is the Tsirelson bound for the CHSH expression in quantum theory.

The conclusion is precise:

The observed quantum correlations cannot be reproduced by a Bell-local hidden-variable model satisfying the assumptions used in the derivation.

This conclusion does not prove that physical information travels instantaneously between the measurement stations. Bell’s theorem excludes a class of explanatory models; it does not uniquely select a replacement ontology.

3.4 What Bell’s theorem does and does not establish

Bell inequality violations establish a conflict between observed quantum statistics and the conjunction of assumptions entering Bell-local models.

They do not, by themselves, establish that:

* a signal travels faster than light;
* a physical force acts instantaneously;
* spacetime is unreal;
* the correlations are necessarily ontologically timeless;
* every possible hidden-variable theory is impossible;
* every nonlocal ontology must be interpreted in the same way.

The present framework takes the experimentally supported statistical result as its starting point, then asks whether a theory can represent the correlations without introducing a propagating mediator between the spacelike-separated outcomes.

That is a legitimate theoretical question, but its answer is not uniquely determined by Bell’s theorem alone.

4. Quantum No-Signaling: Local Marginals from a Joint State

4.1 Bipartite quantum mechanics

Let the joint system have Hilbert space

\mathcal H=\mathcal H_A\otimes\mathcal H_B

and density operator .

A local measurement at , with setting and outcome , is described by positive operators satisfying

\sum_b M_{b|y}=I_B.

The unnormalized conditional state at , given the outcome , is

\widetilde{\rho}_{A|b,y}

\operatorname{Tr}_B
\left(I_A\\otimes M_{b|y})\\rho_{AB}
\\right

for the corresponding measurement convention, with the usual instrument formulation used when outcome-dependent state updates require greater generality.

The probability of outcome is

p(b\mid y)

\operatorname{Tr}
\left(I_A\\otimes M_{b|y})\\rho_{AB}
\\right.

When , the normalized conditional state is

\rho_{A|b,y}

\frac{\widetilde{\rho}_{A|b,y}}{p(b\mid y)}.

The conditional state at can depend on which measurement was performed at and which outcome was obtained. This dependence is central to quantum steering and to the interpretation of entanglement.

However, cannot generally identify the remote outcome from its local data alone.

4.2 Derivation of the no-signaling identity

Suppose the observer at performs a complete measurement but does not communicate which outcome occurred. The local state available at is obtained by averaging over the outcomes:

\begin{aligned}
\rho’A
&=\sum_b \widetilde{\rho}{A|b,y}\\
&=\operatorname{Tr}_B
\left\\left(I_A\\otimes\\sum_b M_{b|y}\\right)
\\rho_{AB}
\\right\\
&=\operatorname{Tr}_B
\left(I_A\\otimes I_B)\\rho_{AB}
\\right\\
&=\operatorname{Tr}B(\rho{AB})\\
&=\rho_A.
\end{aligned}

Therefore,

\boxed{\rho’_A=\rho_A}

for every choice of the complete measurement at .

Consequently, for any local observable ,

\operatorname{Tr}(O_A\rho’_A)

\operatorname{Tr}(O_A\rho_A).

The unconditioned local statistics at are independent of the remote measurement setting.

The argument extends to any local trace-preserving quantum operation at . If is a completely positive trace-preserving map, then

\operatorname{Tr}_B
\left(I_A\\otimes\\mathcal E_B)(\\rho_{AB})
\\right

\operatorname{Tr}B(\rho{AB}).

This is the operational basis of quantum no-signaling for local quantum operations on a shared state.

4.3 Why conditioning does not create a signal

The conditional state may depend on , but exploiting that dependence requires knowing the remote outcome . That information must be transmitted through an ordinary communication channel if the observer at is to use it.

Without the remote outcome record, the observer sees the unchanged reduced state .

Thus the quantum formalism distinguishes:

\text{conditional dependence}
\neq
\text{unconditioned remote control}.

The distinction resolves the apparent paradox. Entanglement can constrain joint outcomes without providing a controllable mechanism for manipulating the remote marginal distribution.

4.4 Scope of the derivation

The result depends on the quantum operational framework: a shared state, local operations, and the appropriate completeness and trace-preservation conditions.

It does not show that every imaginable extension of quantum mechanics is no-signaling. Nor does it establish a unique ontology for the quantum state.

It establishes something more specific and sufficient for the present argument: quantum correlations do not require a controllable signal to pass between the subsystems during the measurements.

5. Relativistic Quantum Field Theory: Local Observables Without Statistical Separability

Quantum field theory supplies a second, independent mathematical realization of the distinction between correlations and influence.

5.1 Local algebras of observables

In algebraic quantum field theory, a spacetime region is assigned an algebra of observables . The assignment encodes which observables are localized in which regions.

For spacelike-separated regions and , relativistic microcausality requires

A,B=0,
\qquad
A\in\mathcal A(\mathcal O_A),
\quad
B\in\mathcal A(\mathcal O_B),

with the appropriate graded commutation relation for fermionic fields and the corresponding observable algebras.

For ordinary bosonic observables, this means that the operators commute.

Microcausality is not the assertion that all spacelike-separated observables are statistically independent. It is a statement about their algebraic compatibility.

The distinction can be expressed as

A,B=0
\centernot\implies
\omega(AB)=\omega(A)\omega(B).

Commutativity and statistical factorization are logically different conditions.

5.2 Deriving the distinction

Let be a state on the observable algebra. For commuting observables and , the expectation value of their product is well-defined as a joint observable.

The connected correlation is

C_\omega(A,B)

\omega(AB)-\omega(A)\omega(B).

Microcausality imposes

A,B=0,

but it does not impose

C_\omega(A,B)=0.

A correlated quantum state can therefore assign nonfactorizing joint statistics to spacelike-separated observables even though the local observable algebras commute.

This is a formal demonstration that the algebraic structure required for relativistic locality does not, by itself, eliminate nonlocal statistical correlations.

5.3 Local response and commutators

Consider a field operator and a local perturbation coupled to an operator . In linear response theory, the change in the expectation of an observable can be expressed in terms of a retarded response function.

For a perturbation with interaction Hamiltonian

H_{\mathrm{int}}(t)

-\int d^3y\,J(y,t)\mathcal O(y,t),

the first-order response has the schematic form

\delta\langle \phi(x)\rangle

\int d^4y\,
G_R(x,y)J(y),

where, up to the sign convention for the interaction,

G_R(x,y)

i\theta(x^0-y^0)
\langle\\phi(x),\\mathcal O(y)\rangle.

In a relativistic theory satisfying microcausality, the commutator vanishes for spacelike separation. Consequently, the retarded response vanishes there as well:

G_R(x,y)=0
\qquad
\text{if }x-y\text{ is spacelike}.

This is a direct dynamical expression of local causal influence.

The correlation function

G^{(1)}(x,y)

\langle\phi(x)\phi(y)\rangle

\langle\phi(x)\rangle
\langle\phi(y)\rangle

is a different object. It need not vanish at spacelike separation.

Therefore, the relativistic field-theoretic distinction is:

\boxed{
\begin{aligned}
\text{State correlation:}\quad&
G^{(1)}(x,y)\neq 0
\ \text{is permitted},\\2mm
\text{Retarded response:}\quad&
G_R(x,y)=0
\ \text{for spacelike separation}.
\end{aligned}
}

This is the most direct mathematical expression of the paper’s central thesis.

5.4 An important limitation

Microcausality is a constraint on observable commutators. Its interpretation as local causal influence is well motivated in relativistic quantum field theory, but a full causal analysis also depends on the interaction, state preparation, measurement procedure, and operational definition of the intervention.

Likewise, a nonzero field correlation at spacelike separation does not by itself imply Bell nonlocality. Vacuum correlations, common preparation, and quantum entanglement are related but distinct phenomena.

The result establishes a structural compatibility, not a universal ontology: relativistic locality of observable response can coexist with nontrivial spacelike correlations.

6. The Universe as a Relational Correlation Structure

The preceding sections establish the physical possibility of correlations that are not equivalent to signals. We now formulate an explicit relational framework for representing them.

The framework is a proposed organization of physical theory, not a claim that standard physics has already proved spacetime to be emergent or that all correlations are fundamentally timeless.

6.1 Primitive mathematical objects

Let a physical model be represented by

\mathfrak U=(\mathcal M,\mathcal A,\omega,\mathcal C),

where:

* is the spacetime structure;
* is the assignment of observable algebras to regions;
* is the physical state;
* is the causal admissibility structure governing allowed interventions and responses.

The ordinary local description identifies physical events and their causal relations within . The state , meanwhile, determines joint expectations and correlation functions across the observable algebra.

The key structural proposal is that the correlation data should not be presumed to decompose into a network of physical transmissions merely because they connect observables associated with separated regions.

Define a correlation functional

\mathfrak K_\omega:
(A,B)\longmapsto
\omega(AB)-\omega(A)\omega(B).

The functional records state-dependent relationships among observables. It does not encode a time-of-flight, a carrier, or a trajectory unless additional structure is explicitly introduced.

6.2 Two different mathematical graphs

For conceptual clarity, define two graphs over a set of physical events .

The causal graph is

G_{\mathrm c}=(V,E_{\mathrm c}),

where a directed edge represents an admissible causal influence from to .

The correlation graph is

G_{\mathrm k}=(V,E_{\mathrm k}),

where an undirected edge indicates that a chosen correlation measure between the corresponding observables is nonzero or exceeds a specified threshold.

These graphs encode different relations.

A correlation edge does not imply a causal edge:

\{p,q\}\in E_{\mathrm k}
\centernot\implies
(p,q)\in E_{\mathrm c}.

Nor does the existence of a causal edge guarantee nonzero correlation in every state:

(p,q)\in E_{\mathrm c}
\centernot\implies
\{p,q\}\in E_{\mathrm k}.

A physical interaction can occur in a state whose relevant connected correlation vanishes. Conversely, correlations can persist between subsystems that are no longer interacting.

The two-graph representation is a useful abstraction, but it is not a complete mathematical model of quantum nonlocality. Ordinary pairwise correlation graphs cannot encode all multipartite correlations, Bell inequalities, or the contextual structure of quantum measurements. Those require richer state and observable data.

6.3 Correlation without a trajectory

A conventional mediated interaction is represented schematically as

A \longrightarrow M \longrightarrow B,

where is a physical mediator that propagates between the relevant regions.

The relational alternative does not introduce a hidden object merely to account for the existence of a correlation. Instead, it specifies the joint state directly:

\omega_{AB}
\quad\longrightarrow\quad
P(a,b\mid x,y).

The arrow here denotes mathematical evaluation of the state under measurement, not a physical process traveling from to .

This distinction matters because a joint state can encode dependencies without describing a sequence of intermediate physical events.

However, a joint state alone does not explain why the state has its particular structure. It provides a predictive representation. A deeper theory might explain the state through a preparation process, a global constraint, a hidden-variable ontology, a boundary condition, or another mechanism.

The relational proposal therefore makes a restricted claim:

A propagating mediator is not mathematically required to represent every correlation, and its existence should not be inferred solely from the presence of correlation.

6.4 A global state with local dynamical accessibility

A state can be globally defined while local operations remain restricted to their own regions.

In a bipartite model, the joint state specifies the available joint statistics. Local observers access reduced states,

\rho_A=\operatorname{Tr}B\rho{AB},
\qquad
\rho_B=\operatorname{Tr}A\rho{AB},

and perform local operations on their respective subsystems.

The global state need not be decomposable as

\rho_{AB}=\rho_A\otimes\rho_B.

Yet local trace-preserving operations do not allow either observer to alter the other’s reduced state by choice.

This provides a minimal mathematical model of global relational structure together with local operational control.

The word global here refers to the domain of the mathematical state. It does not establish that the universe is a single substance outside spacetime, that a global consciousness coordinates events, or that a physical influence operates from outside the universe. Such interpretations require separate premises.

7. Temporal Mediation and the Meaning of “Not Propagating Through Time”

The statement that a correlation is not mediated by anything propagating through time can be interpreted in several ways. Only some are directly supported by the formal results above.

7.1 Four distinct claims

Let us distinguish four propositions.

Proposition A — No required transmission model. A joint distribution can be specified without positing a message or particle traveling between the measurement events.

Proposition B — No operationally usable superluminal signal. A local observer cannot control remote marginal statistics by choosing a measurement setting.

Proposition C — No fundamental dynamical mediator exists. There is no deeper physical entity or process responsible for the correlation.

Proposition D — Correlations are ontologically outside time. The correlation is a timeless primitive, rather than a relation arising within any temporal physical process.

Propositions A and B are supported by the mathematical structures already developed. Propositions C and D do not follow from them.

A model can satisfy A and B while leaving C and D unresolved.

7.2 A precise operational definition

For this paper, call a correlation non-signaling and unmediated in the model if:

* the joint statistics are specified by the model’s state and local measurement rules;
* no additional transmission variable connecting the spacelike-separated measurements is required in that model;
* all allowed local operations preserve the remote marginal statistics;
* the local response functions obey the stipulated causal restrictions.

This is a model-relative definition. It does not prove that every deeper theory must lack a mediator.

The distinction between not required by the model and does not exist in reality is essential. The former is a statement about mathematical representation; the latter is an ontological claim.

7.3 Why “instantaneous influence” is not the correct default interpretation

If two spacelike-separated outcomes are correlated, describing one as instantly influencing the other risks introducing a preferred temporal ordering where relativity supplies none.

For spacelike-separated events, different inertial frames can disagree about which event occurred first. If a physical influence were literally transmitted from one event to the other, a complete theory would need to explain how that transmission avoids conflict with the relativistic causal structure or how its preferred structure is hidden from observation.

The relational framework avoids introducing this problem at the outset. It does not order the two outcomes by an assumed transmission event. It treats their joint statistics as properties of the state and measurement arrangement.

This is a conceptual advantage, not a proof that a relational ontology is uniquely correct.

7.4 Why “timeless” is stronger than “non-signaling”

A correlation can be generated by an ordinary common cause in the shared past. It can also arise from a previously prepared entangled state that persists across time. Neither case requires a signal between the two final measurement events.

But neither case is necessarily timeless.

To establish that the correlation is ontologically independent of temporal evolution would require a theory specifying what time-independent existence means, how the state is defined, and how observed temporal dynamics emerge from or coexist with that structure.

The present framework therefore uses nonmediated correlation in a carefully restricted sense: no inter-event transmission is required to explain the formal joint statistics. It leaves the deeper ontological status of the correlation open.

8. Axiomatic Framework for Nonlocal Correlation with Local Causal Influence

We now formalize the proposed architecture as a set of axioms. The axioms are not all new laws of nature: some restate established properties of relativistic quantum theory, while others define the intended scope of the relational interpretation.

Axiom 1. Localized observables

Each admissible spacetime region is assigned an observable algebra .

Observables localized in spacelike-separated regions satisfy the appropriate microcausality relations.

Axiom 2. A globally defined physical state

A state assigns joint expectation values to compatible observables. It is not required to factorize across every division into spacetime regions.

For some spacelike-separated pairs,

\omega(AB)\neq\omega(A)\omega(B).

This axiom permits nontrivial correlations. It does not require every pair of observables to be correlated.

Axiom 3. Local intervention structure

A physical intervention in region is represented by an admissible local operation . Its effects on observables are evaluated according to the dynamics and causal structure of the model.

An intervention is not identified with the mere acquisition of information about an outcome.

Axiom 4. Operational no-signaling

For spacelike-separated regions, the marginal outcome statistics at one station are invariant under the freely chosen local measurement setting at the other:

P(a\mid x,y)=P(a\mid x).

Similarly,

P(b\mid x,y)=P(b\mid y).

These equations constrain the operational statistics of the model.

Axiom 5. Causal admissibility

Controllable changes in a local source cannot generate a detectable response outside the causal domain permitted by the theory.

For relativistic quantum field theory, this requirement is implemented through the dynamics and local commutativity properties of the relevant observables. In a more general theory, it must be imposed and verified independently.

Axiom 6. No inferred mediator

A nonzero correlation does not, by itself, warrant the introduction of a propagating mediator between the correlated events.

Any proposed mediator must be justified by additional theoretical or empirical evidence.

8.1 Structural theorem

Theorem 1 — Compatibility of nonfactorizing correlations and local causal response.

Let a bipartite quantum system have a joint state . Assume:

* local measurements are described by normalized quantum measurement operations;
* operations at and act locally on the respective subsystems;
* local operations are trace-preserving when their outcomes are ignored;
* the relevant dynamics and observable algebras satisfy the stipulated relativistic causal restrictions.

Then the joint state may exhibit nonfactorizing correlations while the unconditioned marginal statistics remain invariant under remote local operations. Consequently, nonfactorizing joint statistics do not, by themselves, imply operationally usable superluminal signaling.

Proof.

Choose a joint state for which

\rho_{AB}\neq\rho_A\otimes\rho_B.

Such states exist; the singlet state is an explicit example.

Let the observer at apply a local trace-preserving operation . The resulting joint state is

\rho’_{AB}

(I_A\otimes\mathcal E_B)(\rho_{AB}).

The reduced state at is

\rho’_A

\operatorname{Tr}_B
\left(I_A\\otimes\\mathcal E_B)(\\rho_{AB})
\\right.

Trace preservation implies

\rho’_A=\operatorname{Tr}B(\rho{AB})=\rho_A.

Therefore, for every local observable ,

\operatorname{Tr}(O_A\rho’_A)

\operatorname{Tr}(O_A\rho_A).

Thus the remote operation does not change the local statistics at when the remote outcome is ignored.

Since the initial state can be nonfactorizing, the existence of such correlations is compatible with the stated no-signaling property. The assumed causal restrictions govern the permitted dynamical response. Therefore, within the specified model, nonfactorizing correlation and local causal influence are compatible.

8.2 What the theorem establishes

The theorem establishes compatibility, not uniqueness.

It does not prove that every nonfactorizing state exhibits Bell inequality violations. It does not prove that every no-signaling theory is quantum mechanical. It does not prove that the joint state is timeless or that no hidden causal mechanism exists.

Its significance is narrower and more rigorous: the two properties at the center of this paper can coexist in one mathematically consistent framework.

9. Causal Influence as a Response Constraint

To clarify the dynamical content, we distinguish state correlations from responses to externally controlled sources.

9.1 Linear response

Consider a system with an observable and an external source coupled to an observable . In a regime where linear response is valid, the change in the expectation of is

\delta\langle Y(x)\rangle

\int d^4y\,
G_R^{YX}(x,y)\,\delta J_X(y).

The retarded response kernel is

G_R^{YX}(x,y)

i\theta(x^0-y^0)
\langleY(x),X(y)\rangle

for a common interaction-sign convention, with the overall sign depending on the convention adopted for the perturbing Hamiltonian.

For local relativistic fields satisfying microcausality, the commutator vanishes at spacelike separation. Thus the response kernel vanishes there.

This is stronger than merely observing that a particular experiment failed to transmit a message. It identifies a structural reason why the perturbation cannot alter the remote observable’s expectation in the specified theory.

9.2 State dependence versus source dependence

Compare the two functions:

G_C(x,y)

\langle Y(x)X(y)\rangle

\langle Y(x)\rangle\langle X(y)\rangle

and

G_R(x,y)

i\theta(x^0-y^0)
\langleY(x),X(y)\rangle.

The connected correlation describes dependence in the state. The retarded function describes the linear response of to a perturbation coupled to .

They are not interchangeable. At thermal equilibrium, for example, they are related by fluctuation-dissipation relations under suitable assumptions, but those relations do not identify the two functions. Their mathematical roles remain distinct.

The universe can therefore have a nontrivial correlation structure without every correlation representing a response channel.

9.3 Nonlinear and operational causality

Linear response is only one level of causal analysis. A complete theory must also address finite interventions, nonlinear dynamics, measurement instruments, and any constraints on the allowed preparation of states.

The strongest defensible requirement is therefore not simply for spacelike separation. It is that the entire operational theory prevent interventions in one region from producing controllable changes in forbidden regions.

This distinction becomes especially important in theories with nonstandard dynamics, indefinite causal structures, gravitational constraints, or emergent spacetime.

10. The Bell–Causal Separation Principle

We can now state the central conceptual result in a form that is independent of any particular metaphysical interpretation.

Principle. The existence of a statistical relation between two physical events does not establish the existence of a dynamical transmission process between them.

This principle has three components.

10.1 Correlation is not a trajectory

A joint distribution

P(a,b\mid x,y)

contains information about the relationship between outcomes. It does not specify a trajectory connecting the outcome events.

A dynamical model can add such a trajectory, but it must supply additional variables, equations of motion, boundary conditions, or interaction terms.

10.2 Correlation is not a controllable intervention

A measurement outcome may be correlated with a remote outcome without allowing an observer to control the remote result.

The observer’s inability to control the remote marginal is expressed by no-signaling. The correlation becomes operationally useful for certain tasks only when additional information or coordination is available.

10.3 Causal structure is not identical to correlation structure

A causal graph and a correlation graph answer different questions. The first encodes allowed influence; the second encodes dependence in a specified state.

A complete physical theory must explain how both structures coexist, but it need not identify them.

The principle is not that correlations are uncaused, nor that all correlations are fundamental. It is that the inference from correlation exists to something traveled between the correlated events is not logically valid without additional premises.

11. Objections, Countermodels, and Limits of the Framework

A rigorous account must address interpretations that reproduce some or all of the same observable facts.

11.1 Objection: The correlation was created by a common cause

Two systems may interact in the past and then separate. Their later outcomes can remain correlated because the preparation establishes a joint state.

This is correct. Common-cause explanations are compatible with the present framework.

However, Bell inequality violations show that a common cause represented by a Bell-local hidden-variable model cannot reproduce all the relevant quantum statistics when the standard assumptions hold.

The relational proposal does not rule out common causes in general. It rejects the inference that all correlations can be explained by a Bell-local factorization.

11.2 Objection: A hidden nonlocal mechanism might exist

A theory such as de Broglie–Bohm pilot-wave mechanics can reproduce standard quantum predictions while adopting an explicitly nonlocal ontology. Certain formulations involve a preferred foliation or other structure that is not manifest in the usual Lorentz-covariant operational predictions.

Such theories demonstrate that nonlocal hidden mechanisms are not logically excluded merely by no-signaling.

The relational framework therefore cannot claim that no nonlocal mechanism exists. It claims only that one need not introduce such a mechanism to calculate the joint probabilities of standard quantum mechanics.

11.3 Objection: No-signaling is weaker than local causation

This objection is decisive against any argument that equates the two concepts without qualification.

A generalized probabilistic theory can satisfy no-signaling while violating other constraints associated with quantum theory. No-signaling alone does not establish that every causal relation is local, that all interventions have a spacetime-local representation, or that the theory admits a conventional relativistic causal model.

For this reason, the framework includes both an operational no-signaling condition and a separate causal-admissibility requirement.

The latter must be established from the dynamics or explicitly imposed as a postulate. It cannot be inferred from no-signaling alone.

11.4 Objection: Entanglement may have a temporal origin

Entanglement is often generated through ordinary local interactions and then preserved during subsequent evolution. The resulting state can exhibit correlations even when the subsystems are far apart.

This does not contradict the central thesis. The claim is not that entanglement never has a temporal history. It is that the observed correlation between the final measurements need not be mediated by a new transmission between those measurement events.

A theory that makes the stronger claim that correlations have no temporal origin would require a separate derivation.

11.5 Objection: Gravity may complicate the subsystem decomposition

In gauge theories and theories of gravity, the physical Hilbert space may fail to factorize naively across spatial regions. Gauss-law constraints, gravitational constraints, and boundary degrees of freedom can complicate the definition of independent subsystems.

This means that the simple bipartite tensor-product representation is not universally available in its elementary form.

The general framework must therefore be formulated in terms of physical observable algebras, operationally defined subsystems, and the relevant constraint structure. The tensor-product derivations remain valid for the standard bipartite quantum systems to which their assumptions apply, but their direct extension to quantum gravity is not automatic.

11.6 Objection: The correlations might be merely epistemic

One interpretation treats the quantum state as a representation of an observer’s information rather than as an ontologically real object.

Another treats it as a real physical state. Others adopt relational, operational, or hidden-variable interpretations.

The mathematical results discussed here do not uniquely decide among these positions. The relational correlation structure can be understood as a property of the physical state, an operational representation, or a candidate primitive of a deeper theory.

A claim of fundamental ontology requires further argument.

12. A Minimal Relational Model

To make the proposed architecture explicit, consider a minimal model with two qubits, and , in the singlet state.

Let the measurement observables be

A_{\mathbf a}

\boldsymbol{\sigma}\cdot\mathbf a,
\qquad
B_{\mathbf b}

\boldsymbol{\sigma}\cdot\mathbf b,

where denotes the vector of Pauli operators and are unit vectors specifying measurement directions.

The joint probabilities are

P(a,b\mid\mathbf a,\mathbf b)

\frac14
\left(
1-ab\,\mathbf a\cdot\mathbf b
\right),

where .

Summing over gives

\begin{aligned}
P(a\mid\mathbf a,\mathbf b)
&=
\sum_{b=\pm1}
\frac14
\left(
1-ab\,\mathbf a\cdot\mathbf b
\right)\\
&=\frac12.
\end{aligned}

Similarly,

P(b\mid\mathbf a,\mathbf b)=\frac12.

Thus neither marginal depends on the remote setting.

The joint correlation is

E(\mathbf a,\mathbf b)

\sum_{a,b}abP(a,b\mid\mathbf a,\mathbf b)

-\mathbf a\cdot\mathbf b.

This example has all the features needed for the minimal construction:

* The joint distribution is not generally a product of independent local outcome distributions.
* The correlations depend on the relative measurement settings.
* The local marginal distributions remain unchanged under remote setting choices.
* The model does not require a signal sent between the two measurement stations to calculate the joint probabilities.

The fourth point is a statement about the formal model. It does not establish that the singlet state itself has no physical preparation history, or that every interpretation of quantum mechanics must adopt a mediator-free ontology.

12.1 The role of shared structure

The model’s joint state is the mathematical object from which the probabilities are calculated. The state determines the correlation between outcomes even though the individual outcomes are not specified as a deterministic local function of the measurement setting alone.

One may interpret this as a primitive relation, a physically real quantum state, or an operational probability assignment. Each interpretation preserves the mathematical predictions but assigns different ontological significance to the state.

The relational proposal favors the first two possibilities as conceptual options, but it does not derive either one uniquely from the probability formula.

12.2 Why a correlation is not a hidden message

Suppose the observer at changes the measurement direction from to . The joint distribution changes:

P(a,b\mid\mathbf a,\mathbf b)
\neq
P(a,b\mid\mathbf a,\mathbf b’)

in general.

But the marginal at remains

P(a\mid\mathbf a)=\frac12.

The change in the joint distribution is therefore not a change in the remote observer’s locally accessible outcome statistics.

The two observers can verify the correlations by comparing their records through an ordinary communication channel. That later comparison reveals a pattern in the joint data; it does not show that the pattern was transmitted between the stations at the time of measurement.

This is the operational content of nonlocal correlation without superluminal signaling.

13. Experimental Program: Distinguishing Correlation from Causal Transmission

The framework must be connected to measurable quantities. Its immediate empirical content overlaps with established quantum theory, so it is important to distinguish tests of the underlying quantum phenomena from tests of the stronger relational interpretation.

13.1 Test I: Bell inequality violation under spacelike separation

Objective: Establish correlations incompatible with Bell-local hidden-variable models under the assumptions of the experimental protocol.

Measure the four correlations entering the CHSH expression and compute

S=E_{00}+E_{01}+E_{10}-E_{11}.

A statistically significant result satisfying

|S|>2

violates the Bell-local bound.

A loophole-resistant implementation should address:

* detection efficiency and postselection;
* independence of the measurement-setting choices;
* spacelike separation between the relevant setting choices and remote outcomes;
* timing and synchronization uncertainty;
* statistical analysis and finite-sample corrections.

Interpretation: A violation rules out the specified class of Bell-local models. It does not, by itself, demonstrate the absence of every possible underlying mediator.

13.2 Test II: Remote-setting invariance

Objective: Test whether a local observer can infer the remote measurement setting from local outcome statistics.

For each local setting , estimate

P(a\mid x,y)

for multiple remote settings .

The no-signaling prediction is

P(a\mid x,y_0)

P(a\mid x,y_1)

within statistical uncertainty.

For a binary outcome, one can compare the corresponding conditional frequencies using a prespecified statistical test, accounting for finite-sample fluctuations and multiple comparisons.

Interpretation: Agreement with no-signaling supports the operational claim that the remote setting does not control the local marginal. It cannot establish an exact zero response from finite data, and it cannot exclude every hidden mechanism consistent with the same statistics.

13.3 Test III: Retarded-response measurements

Objective: Distinguish spontaneous or state-dependent correlations from the response to a controlled local perturbation.

Apply a calibrated source in region , and measure the response of a suitable observable in region .

In a linear regime, estimate the retarded response function

G_R^{YX}(x,y)

i\theta(x^0-y^0)
\langleY(x),X(y)\rangle.

The local relativistic field-theory prediction is a vanishing retarded response for spacelike-separated supports, subject to the theory’s microcausality and operational assumptions.

An experiment must control ordinary electromagnetic leakage, common-clock errors, detector cross-talk, environmental coupling, and any unintended communication channels.

Interpretation: This test probes the dynamical response structure, not merely the existence of correlations. A null result is consistent with locality but does not establish that the correlation has no deeper physical origin.

13.4 Test IV: Correlations after the interaction has ceased

Objective: Establish that nontrivial correlations can persist after the systems cease interacting directly.

Prepare an entangled state, separate the subsystems, and perform measurements after the preparation interaction has ended. Vary the separation and delay while controlling decoherence and other environmental effects.

Measure the joint correlation and the corresponding local marginal distributions.

A successful experiment can demonstrate that a new interaction between the final measurement stations is unnecessary to reproduce the observed correlation within the standard quantum model.

It cannot show that the correlation has no temporal origin: the preparation process is itself part of the physical history.

13.5 Test V: Compare candidate causal models

Objective: Determine whether distinct models with the same quantum predictions can be distinguished by additional assumptions or observables.

Candidate models may include:

* relativistic quantum field theory;
* hidden-variable theories with explicit nonlocal structure;
* operational models in which quantum states encode predictive information;
* relational models that treat joint state structure as fundamental.

Where two models make identical predictions for every accessible observable, no experiment within that shared domain can distinguish their ontologies.

A successful empirical program must therefore identify a concrete divergence in predictions before claiming that an experiment tests whether correlations are fundamentally timeless or mediator-free.

13.6 Summary of empirical status

Claim	Status
Quantum correlations violate Bell-local bounds	Experimentally established
Standard quantum mechanics obeys no-signaling for local operations	Mathematically established
Relativistic microcausality permits nonzero spacelike correlations	Established within the applicable field-theoretic framework
A propagating signal is required to calculate every quantum correlation	False as a claim about the formalism
No underlying mediator exists in reality	Not established by these results
Correlations are ontologically outside time	Not established by these results
A unified theory can derive both correlation structure and local causal dynamics from deeper principles	Open theoretical objective

The empirical program supports the separation between statistical dependence and controllable causal influence. The stronger ontological thesis remains a research question.

14. Relation to Thermodynamics, Information, and Emergent Spacetime

The distinction developed here has consequences beyond elementary entanglement experiments, although those consequences must be treated as research directions rather than established deductions.

14.1 Correlation and information

For a bipartite quantum state, the quantum mutual information is

I(A:B)

S(\rho_A)+S(\rho_B)-S(\rho_{AB}),

where

S(\rho)=-\operatorname{Tr}(\rho\ln\rho)

is the von Neumann entropy.

Mutual information measures total correlations, including both classical and quantum contributions. It does not, by itself, quantify causal influence or establish that information has been transmitted.

For a pure entangled state, the reduced states can be mixed even though the joint state is pure. This demonstrates that local uncertainty and joint-state structure need not coincide.

The interpretation of mutual information as a resource for communication, computation, or metrology depends on the allowed operations and communication constraints. Correlation is not identical to a usable communication channel.

14.2 Thermodynamic and statistical constraints

A globally specified state can impose joint constraints on subsystems even when those subsystems do not directly interact during the measurement interval.

This is familiar in statistical mechanics, where ensembles encode constraints and probability distributions over many degrees of freedom. Quantum mechanics extends the space of admissible correlations beyond what classical local hidden-variable models can reproduce.

The relational framework suggests a general methodological principle: before introducing a dynamical carrier, determine whether the observed structure is already represented by the state, constraints, or boundary conditions of the theory.

This does not eliminate the need for dynamical explanations. It prevents the category error of treating every statistical relationship as a transported physical object.

14.3 Entanglement and geometry

Some approaches to quantum gravity investigate relationships between entanglement structure and geometric properties of spacetime. Holographic theories, tensor-network models, and quantum-information-inspired approaches to geometry provide concrete settings in which this question can be studied.

However, the inference

\text{entanglement}
\Longrightarrow
\text{emergent spacetime}

is not a universal theorem. The relationship depends on the particular model, its state, its dynamical equations, and its geometric reconstruction procedure.

The present framework is compatible with the possibility that spacetime geometry and causal propagation emerge from a deeper relational structure, but it does not derive that emergence.

A complete theory would need to specify:

* the primitive relational data;
* the rule for constructing effective spacetime regions;
* the mechanism that produces a Lorentzian causal structure;
* the conditions under which local propagation emerges;
* the relation between entanglement measures and geometric observables;
* a regime in which known relativistic quantum field theory is recovered.

Without these steps, emergent spacetime remains an interpretive possibility rather than a result of the nonlocal-correlation argument.

15. A Candidate Reconstruction Principle

We can formulate a more ambitious research objective: derive effective spacetime-local dynamics from a theory whose primitive data include relational correlations and admissible operations.

Let denote a space of relational states and let denote the set of allowed transformations. A candidate theory would supply maps

\mathcal R
\xrightarrow{\ \mathcal G\ }
(\mathcal M,g_{\mu\nu}),

and

(\mathcal R,\mathcal T)
\xrightarrow{\ \mathcal D\ }
\text{effective local dynamics}.

Here, is a geometric reconstruction map and is a dynamical reconstruction map. These maps are schematic placeholders for structures that a concrete theory would have to define.

The desired output is a theory in which:

* the reconstructed metric determines an effective causal cone;
* local operations generate retarded responses consistent with that cone;
* the global state reproduces observed quantum correlations;
* local marginals obey the appropriate no-signaling constraints;
* the theory reduces to established physics in its tested regime.

15.1 Necessary consistency conditions

Any proposed reconstruction must satisfy at least four conditions.

Condition 1: Operational equivalence. In the regime where standard quantum theory is successful, the reconstructed probabilities must agree with its predictions within the model’s domain.

Condition 2: Causal consistency. The effective dynamics must not introduce observable violations of the stipulated causal restrictions.

Condition 3: Geometric consistency. The reconstructed geometry must have well-defined mathematical properties and must reproduce the observed relativistic limit where applicable.

Condition 4: Independent explanatory content. The relational theory must explain something not already assumed in the input data, such as the origin of a causal structure, the emergence of a metric, or a quantitative relationship between correlation and geometry.

The fourth condition prevents circular reconstruction. If the primitive data already encode the full spacetime metric and its causal structure, then recovering the same metric does not explain its origin.

15.2 A possible research program

A concrete development could proceed through the following stages:

* Specify a mathematically well-defined relational state space.
* Define the allowed transformations and their composition rules.
* Establish which observables are locally accessible.
* Derive the no-signaling constraints from the transformation structure.
* Identify conditions under which a causal partial order emerges.
* Construct an effective metric or causal cone.
* Derive the low-energy field equations.
* Recover known quantum correlations and relativistic response functions.
* Identify a quantitative prediction not shared by the baseline theory.
* Test that prediction independently.

This program is ambitious. Its value is methodological: it converts the broad idea of a relational universe into a sequence of explicit mathematical obligations.

16. Falsifiability and Failure Conditions

A theory that claims to describe physical reality must specify what would count against it.

The minimal relational framework, as developed here, is compatible with standard quantum mechanics and relativistic quantum field theory. It therefore inherits their tested predictions rather than introducing a distinct empirical model.

The stronger claim that correlations are fundamentally nonmediated or ontologically timeless is not yet independently falsifiable in the present formulation. It lacks a unique mathematical law whose predictions differ from those of competing interpretations.

To become an independently testable theory, it must introduce additional structure and derive a novel prediction.

Possible failure conditions for a proposed extension include:

* No-signaling failure: if the extension predicts controllable remote-setting dependence in a regime where its own assumptions require no-signaling, the extension is internally inconsistent with that requirement.
* Microcausality failure: if the model claims relativistic local dynamics but predicts nonzero spacelike commutators of ordinary local observables, it fails its stated microcausality condition.
* Quantum-statistical failure: if the model purports to reproduce standard quantum mechanics but predicts different joint probabilities in an already tested regime, it must confront the corresponding experimental evidence.
* Reconstruction failure: if the proposed relational data cannot produce a consistent causal structure or the known relativistic limit, the proposed emergent-spacetime mechanism fails.
* Explanatory redundancy: if every desired result is inserted into the primitive assumptions, the theory may be formally consistent but has not derived the claimed emergence.
* Lack of discriminating predictions: if the extension makes no distinct empirical prediction, its stronger ontology remains underdetermined by the experiments considered here.

These criteria separate the successful mathematical coexistence result from the more speculative ambition to explain why the universe has this structure.

17. Discussion: What the Universe Must Not Be Assumed to Contain

The distinction between nonlocal correlation and local causal influence imposes a constraint on how physical explanations should be constructed.

A theory should not assume that every relationship between distant events must be implemented by an object traveling between them. That assumption is stronger than the requirement that physical interventions obey a causal structure.

Three explanatory strategies are possible.

Strategy A — Mediated interaction

A physical carrier travels between events and dynamically generates their relationship. The carrier’s dynamics, propagation law, and interactions must be specified.

Strategy B — Common-state explanation

A shared preparation or global state determines joint probabilities. No new transmission between the final measurement events is required.

Strategy C — Fundamental relational structure

Joint relations are treated as primitive physical data, while local causal dynamics describe the accessible evolution and response of subsystems. This requires an independent theory of the relational state and its admissible transformations.

These strategies are not mutually exclusive in every theory. A physical model may use a common state created by mediated interactions, and a deeper theory might derive both the state and the causal structure from more primitive principles.

The decisive question is not whether a model uses the word local or nonlocal. It is which mathematical relations the model treats as primitive, which it derives, and which observable consequences distinguish it from alternatives.

17.1 Correlation does not require an extra signal

Standard quantum mechanics already calculates the joint probabilities of entangled systems without inserting an additional message between spacelike-separated measurement events.

Consequently, adding a hidden transmission process solely to restate the existence of the correlations does not improve the predictive model unless it provides further explanatory or empirical content.

This is a principle of theoretical economy, not proof that no deeper mechanism exists.

17.2 Locality does not imply separability

A universe whose observable dynamics obey local causal restrictions need not be representable as a collection of statistically independent parts.

The assumption that the universe must be both causally local and statistically separable is therefore unwarranted. Quantum theory demonstrates that these properties must be distinguished.

17.3 Nonseparability does not abolish spacetime

The opposite inference is equally unjustified. Nonlocal correlations do not establish that spacetime is unreal or that all physical relations exist outside time.

Spacetime remains essential to the localization of observables, the definition of causal domains, the specification of interventions, and the dynamics of relativistic fields.

The more defensible possibility is that spacetime constrains one aspect of physical structure—causal propagation—without exhaustively determining every relation encoded in a quantum state.

18. Conclusions

This paper has developed a mathematical framework for a universe in which nonlocal correlations coexist with local causal influence.

The principal results are as follows.

First, statistical dependence and causal influence are different mathematical objects. A nonzero connected correlation measures dependence in a state; a response function measures how an observable changes under an intervention. Neither quantity can generally be substituted for the other.

Second, Bell inequality violations exclude Bell-local hidden-variable models under their defining assumptions. They establish that quantum correlations cannot be explained by the standard local factorization of shared hidden variables, but they do not establish that a signal travels between the measurement events.

Third, quantum no-signaling follows from the structure of local quantum operations. For a shared quantum state, a local trace-preserving operation at one subsystem leaves the reduced state of the other subsystem unchanged when remote outcomes are ignored.

Fourth, relativistic microcausality is compatible with nonzero spacelike correlations. The commutation relations of local observables constrain dynamical response without requiring the state to factorize across spacelike-separated regions.

Fifth, a relational description can represent joint correlations without introducing a propagating mediator. The joint state and the measurement rules suffice to calculate the relevant probabilities. Whether the state is ontologically fundamental, emergent, or epistemic remains a separate question.

The strongest conclusion is not that correlations have been proved to exist outside time. It is that a correlation need not be a transmission event.

A more ambitious theory may ultimately derive spacetime, causal propagation, and quantum correlations from a common relational structure. Such a theory would need to define its primitive variables, derive its causal restrictions, recover known physics, and make independently testable predictions.

Until that development is completed, the distinction established here remains the firm foundation:

\boxed{
\text{Nonlocal correlation}
\;\not\Rightarrow\;
\text{nonlocal causal influence}.
}

And conversely,

\boxed{
\text{Local causal influence}
\;\not\Rightarrow\;
\text{statistical separability}.
}

The universe need not be understood as a collection of isolated events connected only by things traveling between them. Its physical description can contain global relational structure while preserving local restrictions on what observers can cause, control, and measure.

The central research question is therefore not simply how a signal travels between correlated events. It is whether the observed correlation structure can be derived from a deeper physical principle that also explains why causal influence remains constrained by spacetime.

That question remains open—and it is precisely where the next stage of the theory must begin.

References

1. Bell, J. S. (1964). “On the Einstein Podolsky Rosen Paradox.” Physics Physique Fizika, 1, 195–200.

2. Clauser, J. F., Horne, M. A., Shimony, A., & Holt, R. A. (1969). “Proposed Experiment to Test Local Hidden-Variable Theories.” Physical Review Letters, 23, 880–884.

3. Tsirelson, B. S. (1980). “Quantum Generalizations of Bell’s Inequality.” Letters in Mathematical Physics, 4, 93–100.

4. Haag, R. (1996). Local Quantum Physics: Fields, Particles, Algebras (2nd ed.). Springer.

5. Summers, S. J., & Werner, R. (1987). “Bell’s Inequalities and Quantum Field Theory. I. General Setting.” Journal of Mathematical Physics, 28, 2440–2447.

6. Werner, R. F. (1989). “Quantum States with Einstein-Podolsky-Rosen Correlations Admitting a Hidden-Variable Model.” Physical Review A, 40, 4277–4281.

7. Gisin, N. (1991). “Bell’s Inequality Holds for All Non-Product States.” Physics Letters A, 154, 201–202.

8. Popescu, S., & Rohrlich, D. (1994). “Quantum Nonlocality as an Axiom.” Foundations of Physics, 24, 379–385.

9. Maudlin, T. (2011). Quantum Non-Locality and Relativity: Metaphysical Intimations of Modern Physics (3rd ed.). Wiley-Blackwell.

10. Brunner, N., Cavalcanti, D., Pironio, S., Scarani, V., & Wehner, S. (2014). “Bell Nonlocality.” Reviews of Modern Physics, 86, 419–478.

11. Wiseman, H. M., Jones, S. J., & Doherty, A. C. (2007). “Steering, Entanglement, Nonlocality, and the Einstein-Podolsky-Rosen Paradox.” Physical Review Letters, 98, 140402.

12. Oreshkov, O., Costa, F., & Brukner, Č. (2012). “Quantum Correlations with No Causal Order.” Nature Communications, 3, 1092.

13. Sorkin, R. D. (1993). “Impossible Measurements on Quantum Fields.” In Directions in General Relativity, Vol. 2. Cambridge University Press.

14. Reeh, H., & Schlieder, S. (1961). “Bemerkungen zur Unitäräquivalenz von Lorentzinvarianten Feldern.” Il Nuovo Cimento, 22, 1051–1068.

15. Van Raamsdonk, M. (2010). “Building Up Spacetime with Quantum Entanglement.” General Relativity and Gravitation, 42, 2323–2329.

16. Einstein, A., Podolsky, B., & Rosen, N. (1935). “Can Quantum-Mechanical Description of Physical Reality Be Considered Complete?” Physical Review, 47, 777–780.

# The Admissible Excitation Spectrum

## A Constraint-Theoretic Framework for the Classification, Stability, and Transition Structure of Physical Excitations

A foundational theoretical preprint

Author: Marlon Hanks

## Abstract

The observed particle spectrum presents a fundamental classification problem: why do only particular excitations occur, why do they possess particular stability properties, and why are transitions among them restricted? Conventional quantum field theory describes particles through representations of spacetime and internal symmetries, while their masses and interactions are encoded in the dynamical structure of the theory. Yet a deeper question remains: can the existence and organization of an excitation spectrum be formulated as a problem of admissibility, independently of assuming a particle ontology at the outset?

This paper develops the Admissible Excitation Spectrum (AES) as a constraint-theoretic framework for classifying physically admissible excitations of a background phase configuration. The central object is not an assumed list of particles, but a structured space of perturbations compatible with a global admissibility condition. Excitations are defined through the linearized and, where necessary, nonlinear consistency conditions of the underlying configuration space. Redundancies are removed through an equivalence relation, while boundary conditions, regularity, normalizability, and stability determine which mathematical candidates qualify as physical excitation sectors.

The framework begins with a nonlinear admissibility equation,

\\[ \mathcal F[\Phi;\lambda]=0, \\]

where \\(\Phi\\) denotes the underlying phase configuration and \\(\lambda\\) collects parameters and structural data. Its linearization,

\\[ L\_\Phi=D\_\Phi\mathcal F, \\]

determines the first-order admissible perturbation space. The resulting candidate excitation space is then reduced by gauge and structural equivalences,

\\[ \mathscr E\_\Phi/G\_\Phi. \\]

A crucial distinction is established between four questions that are often conflated: whether a perturbation is kinematically admissible, whether it defines a distinct excitation sector, whether it is dynamically stable, and whether it can participate in a physical transition. The paper develops these as separate mathematical tests.

A generalized spectral construction is introduced without assuming that the linearized consistency operator is automatically a Hamiltonian, a self-adjoint operator, or a quantum-mechanical observable. Where a suitable dynamical generator exists, its spectrum can classify excitation modes. Where it does not, the admissible perturbation space remains meaningful, but a conventional energy spectrum cannot yet be claimed.

The paper further develops a hierarchy of excitation classification, nonlinear continuation, stability, transition admissibility, and response. It identifies the response kernel

\\[ K^\Phi\_{fi} = \mathcal P_f\\,\chi\_\Phi\\,\mathcal J_i, \qquad \chi\_\Phi=L\_\Phi^{-1}, \\]

as a candidate bridge between admissible sectors, while emphasizing that an amplitude map, probability measure, Born-rule derivation, and quantum interference structure remain unresolved.

The principal result is therefore a mathematical architecture for determining what may count as an excitation before assigning it the status of a particle. The framework does not yet derive the Standard Model spectrum, particle masses, quantum numbers, flavor mixing, or numerical rare-decay rates. Instead, it specifies the mathematical conditions under which such results would have to be obtained, and establishes a program of falsifiable tests through which the proposed spectrum could be compared with observed physics.

Keywords: admissible excitation spectrum; phase configuration; constraint operator; linearized consistency; spectral classification; excitation sectors; stability; gauge equivalence; transition admissibility; response kernel; emergent particle ontology.

# 1. Introduction

## 1.1 The problem of the excitation spectrum

The particle spectrum is among the most restrictive empirical structures in fundamental physics. The known elementary particles do not form an arbitrary collection of possible field disturbances. They occupy a highly organized set of states with characteristic masses, charges, spins, interaction channels, lifetimes, and selection rules.

The Standard Model provides an extraordinarily successful account of this structure. Nevertheless, the mathematical organization of its particle content does not by itself answer every foundational question concerning the origin of the spectrum.

A theory may specify fields and symmetries, then determine which excitations those fields support. But a more primitive formulation would ask:

1. What constitutes an admissible excitation of a physical background?
2. Which perturbations represent distinct physical sectors rather than redundant descriptions?
3. Under what conditions does an admissible perturbation persist as a nonlinear solution?
4. Which admissible sectors are dynamically stable?
5. Which transitions between sectors are consistent with the global constraints?
6. What additional structure is required to assign masses, quantum numbers, amplitudes, and probabilities?

The Admissible Excitation Spectrum is intended to organize these questions into a single mathematical hierarchy.

Its starting point is not a predetermined particle list. It is a background configuration satisfying a global consistency condition. Excitations are then classified according to their compatibility with that condition.

The central conceptual shift is:

\\[ \boxed{ \text{Particle spectrum} \quad\longrightarrow\quad \text{Admissible excitation structure} } \\]

The particle spectrum, if successfully recovered, would be a physical realization of this deeper structure.

## 1.2 Relation to Phase-Admissible Particle Dynamics

The present framework is a continuation of Phase-Admissible Particle Dynamics (PAPD). PAPD introduces a background admissibility equation, a linearized consistency operator, candidate excitation sectors, and a transition functional.

The Admissible Excitation Spectrum isolates and develops the classification problem implicit in that construction.

The relationship is:

\\[ \text{PAPD} \supset \text{Admissible Excitation Spectrum} \supset \text{Excitation Classification}. \\]

PAPD supplies the broader dynamical setting. AES addresses the question of which excitation sectors are mathematically available within that setting and what additional conditions are necessary before those sectors can be interpreted as physical particles.

This distinction is important. A classification framework is not itself a derivation of the observed particle spectrum. The latter requires additional mathematical structures and empirical matching.

## 1.3 The ontology-neutral requirement

No particular particle ontology is assumed.

An excitation need not initially be identified with:

- a point particle;
- a quantized field mode;
- a topological defect;
- a soliton;
- a knot;
- a geometric singularity;
- a localized energy concentration;
- or a representation of a prescribed internal symmetry group.

Any of these could emerge as a useful description of a particular class of admissible solutions. None is imposed as a foundational requirement.

The appropriate starting object is a perturbation of a background configuration, subject to the condition that the perturbed configuration remains admissible.

This makes the framework ontology-neutral while retaining the possibility of recovering conventional particle descriptions.

## 1.4 Main objectives

The paper develops six objectives:

1. Define the admissible perturbation space.
2. Construct a quotient classification of physically distinct excitation sectors.
3. Distinguish linearized modes from nonlinear excitation branches.
4. Formulate stability as an independent dynamical condition.
5. Define admissible transitions between excitation sectors.
6. Identify the additional structures required to recover a physical mass and quantum spectrum.

The paper also establishes explicit limits on what follows from the foundational equations alone.

# 2. Foundational Mathematical Structure

## 2.1 Configuration space

Let \\(\mathcal C\\) denote a configuration space whose elements are admissible candidates for the underlying physical configuration.

Let

\\[ \Phi\in\mathcal C \\]

denote a phase configuration.

The space \\(\mathcal C\\) may be modeled, depending on the eventual theory, as a differentiable manifold, a Banach manifold, a space of sections of a bundle, or a suitably regularized function space.

No specific choice is required at the abstract level, but the analytical properties of the operators introduced below depend on this choice.

The configuration is constrained by a nonlinear functional equation,

\\[ \boxed{ \mathcal F[\Phi;\lambda]=0. } \tag{2.1} \\]

Here:

- \\(\Phi\\) is the underlying configuration;
- \\(\lambda\\) denotes structural parameters;
- \\(\mathcal F\\) is a consistency or admissibility functional.

The equation defines the admissible configuration set,

\\[ \mathscr A\_\lambda = \left\\{ \Phi\in\mathcal C: \mathcal F[\Phi;\lambda]=0 \right\\}. \tag{2.2} \\]

The physical background is a distinguished solution,

\\[ \Phi_0\in\mathscr A\_\lambda. \tag{2.3} \\]

The existence of such a solution is an assumption of the construction. Its existence, uniqueness, regularity, and physical interpretation must be established in any concrete realization.

## 2.2 The admissibility manifold

If the derivative

\\[ D\_\Phi\mathcal F\big|\_{\Phi_0} \\]

has suitable regularity and constant-rank properties, the admissible set may locally possess the structure of a submanifold of \\(\mathcal C\\).

The tangent space to this submanifold is then

\\[ T\_{\Phi_0}\mathscr A\_\lambda = \ker D\_\Phi\mathcal F\big|\_{\Phi_0}. \tag{2.4} \\]

This relation is the first fundamental result of the AES construction.

It says that infinitesimal admissible changes of a background are precisely those perturbations lying in the kernel of the linearized consistency condition.

Define

\\[ \boxed{ L\_{\Phi_0} = D\_\Phi\mathcal F\big|\_{\Phi_0}. } \tag{2.5} \\]

Then

\\[ \boxed{ T\_{\Phi_0}\mathscr A\_\lambda = \ker L\_{\Phi_0}. } \tag{2.6} \\]

This equation is a local geometric statement, subject to the differentiability and regularity assumptions above. It does not yet establish a particle spectrum.

## 2.3 Perturbative expansion

Consider a perturbed configuration,

\\[ \Phi\_\epsilon = \Phi_0+\epsilon\eta, \tag{2.7} \\]

where \\(\eta\\) is a perturbation and \\(\epsilon\\) is a small real parameter.

Expanding the admissibility functional,

\\[ \mathcal F[\Phi\_\epsilon;\lambda] = \mathcal F[\Phi_0;\lambda] + \epsilon L\_{\Phi_0}\eta + \frac{\epsilon^2}{2} D\_\Phi^2\mathcal F\big|\_{\Phi_0} [\eta,\eta] + O(\epsilon^3). \tag{2.8} \\]

Since the background satisfies

\\[ \mathcal F[\Phi_0;\lambda]=0, \\]

first-order admissibility requires

\\[ \boxed{ L\_{\Phi_0}\eta=0. } \tag{2.9} \\]

The first-order candidate excitation space is therefore

\\[ \mathscr E\_{\Phi_0}^{(1)} = \ker L\_{\Phi_0}. \tag{2.10} \\]

However, a perturbation satisfying (2.9) need not extend to a finite nonlinear family of admissible configurations. Higher-order consistency imposes additional conditions.

This distinction will be central throughout the paper.

# 3. Definition of the Admissible Excitation Spectrum

## 3.1 Candidate excitation space

Let \\(\mathcal V\_{\Phi_0}\\) be the space of perturbations around the background \\(\Phi_0\\), with regularity and boundary conditions specified by the chosen model.

The linearized admissible perturbation space is

\\[ \mathscr E\_{\Phi_0}^{\mathrm{lin}} = \left\\{ \eta\in\mathcal V\_{\Phi_0}: L\_{\Phi_0}\eta=0 \right\\}. \tag{3.1} \\]

This space contains all perturbations that satisfy the first-order admissibility condition.

It may contain:

- physical excitation directions;
- gauge directions;
- infinitesimal coordinate or relational redundancies;
- parameter variations;
- non-normalizable perturbations;
- zero modes associated with continuous families of backgrounds;
- perturbations obstructed at higher order.

Consequently, the kernel alone is not the final excitation spectrum.

## 3.2 Physical equivalence

Suppose a group \\(G\_{\Phi_0}\\) acts on the perturbation space and preserves the physical configuration represented by \\(\Phi_0\\).

Two perturbations may then represent the same physical excitation if they are related by an allowed redundancy.

Write

\\[ \eta_1\sim\eta_2 \\]

when they belong to the same equivalence class under the prescribed redundancy structure.

The quotient candidate space is

\\[ \boxed{ \mathscr E\_{\Phi_0}^{\mathrm{quot}} = \mathscr E\_{\Phi_0}^{\mathrm{lin}}/G\_{\Phi_0}. } \tag{3.2} \\]

More generally, if the action is infinitesimal, let

\\[ \mathscr G\_{\Phi_0} \subseteq \mathcal V\_{\Phi_0} \\]

denote the tangent space to the gauge or redundancy orbit. If

\\[ \mathscr G\_{\Phi_0} \subseteq \ker L\_{\Phi_0}, \\]

then the linearized physical perturbation space can be represented formally as

\\[ \boxed{ \mathscr E\_{\Phi_0}^{\mathrm{phys}} = \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}. } \tag{3.3} \\]

The inclusion condition is essential: the redundancy directions must themselves preserve the linearized admissibility equation.

If the group action has singular or non-free orbits, the quotient may be stratified rather than a smooth manifold. This possibility cannot be ignored in a complete mathematical treatment.

## 3.3 Definition

Definition 3.1 — Admissible excitation candidate.

An admissible excitation candidate of a background \\(\Phi_0\\) is an equivalence class

\\[ [\eta]\in \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0} \\]

whose representative satisfies the regularity, boundary, and integrability conditions specified by the model.

Definition 3.2 — Admissible excitation sector.

An admissible excitation sector is a physically distinct class of admissible perturbations that is stable under the relevant structural equivalences and can be consistently distinguished by the available invariant data.

Definition 3.3 — Admissible Excitation Spectrum.

The Admissible Excitation Spectrum is the collection of physically distinct excitation sectors associated with a background configuration, together with the structural, spectral, stability, and transition data required to classify them:

\\[ \boxed{ \mathfrak S\_{\mathrm{AES}}(\Phi_0) = \left( \mathscr E\_{\Phi_0}^{\mathrm{phys}}, \mathcal D\_{\Phi_0}, \mathcal Z\_{\Phi_0}, \mathcal T\_{\Phi_0} \right). } \tag{3.4} \\]

Here:

- \\(\mathscr E\_{\Phi_0}^{\mathrm{phys}}\\) is the physical excitation space;
- \\(\mathcal D\_{\Phi_0}\\) is the set of available spectral data;
- \\(\mathcal Z\_{\Phi_0}\\) denotes stability and persistence information;
- \\(\mathcal T\_{\Phi_0}\\) denotes transition-admissibility information.

This definition deliberately allows the spectral data to be incomplete. A theory may define admissible sectors before it has derived a conventional energy operator or probability interpretation.

# 4. The Spectral Problem

## 4.1 Why the consistency operator is not automatically a Hamiltonian

A central mathematical caution is required.

The operator

\\[ L\_{\Phi_0}=D\_\Phi\mathcal F\big|\_{\Phi_0} \\]

is a linearized consistency operator. It is not automatically:

- a Hamiltonian;
- a mass operator;
- a self-adjoint operator;
- a time-evolution generator;
- a positive operator;
- or an energy observable.

Its kernel identifies first-order admissible perturbations. Its nonzero spectrum, if defined, describes properties of the linearized consistency map, not necessarily the physical energy spectrum.

A physical spectral interpretation requires additional structure.

## 4.2 Introduction of a dynamical generator

Suppose the theory supplies a dynamical generator

\\[ \mathcal H\_{\Phi_0}: \mathcal D(\mathcal H\_{\Phi_0}) \subseteq \mathscr E\_{\Phi_0}^{\mathrm{phys}} \rightarrow \mathscr E\_{\Phi_0}^{\mathrm{phys}}. \tag{4.1} \\]

The operator may be obtained from a well-defined evolution law, a variational principle, a constrained Hamiltonian construction, or another independently justified dynamical structure.

A spectral problem may then be written as

\\[ \boxed{ \mathcal H\_{\Phi_0}\eta = \omega\eta. } \tag{4.2} \\]

The spectral values \\(\omega\\) classify modes of the generator.

Only if the generator has a justified physical interpretation may these values be identified with energy, frequency, mass-related parameters, or another observable.

For a relativistic theory, the relation between frequency and invariant mass would require additional spacetime and representation structure. It cannot be inferred from (4.2) alone.

## 4.3 Generalized operator pencils

In many systems, the natural spectral problem is not an ordinary eigenvalue equation.

A more general formulation is

\\[ \boxed{ \mathcal P\_{\Phi_0}(\omega)\eta=0, } \tag{4.3} \\]

where \\(\mathcal P\_{\Phi_0}(\omega)\\) is an operator-valued function of the spectral parameter.

For example, a second-order evolution equation may generate

\\[ \mathcal P\_{\Phi_0}(\omega) = \mathcal K\_{\Phi_0} - \omega^2\mathcal M\_{\Phi_0}, \tag{4.4} \\]

with \\(\mathcal K\_{\Phi_0}\\) a stiffness-like operator and \\(\mathcal M\_{\Phi_0}\\) an inertia-like operator.

The spectrum is then determined by

\\[ \left( \mathcal K\_{\Phi_0} - \omega^2\mathcal M\_{\Phi_0} \right)\eta=0. \tag{4.5} \\]

This generalized formulation is preferable to assuming a particular Hamiltonian structure prematurely.

## 4.4 Spectral classification

When a suitable operator exists, its spectrum may contain:

\\[ \sigma(\mathcal H\_{\Phi_0}) = \sigma\_{\mathrm p} \cup \sigma\_{\mathrm c} \cup \sigma\_{\mathrm r}, \tag{4.6} \\]

where:

- \\(\sigma\_{\mathrm p}\\) is the point spectrum;
- \\(\sigma\_{\mathrm c}\\) is the continuous spectrum;
- \\(\sigma\_{\mathrm r}\\) is the residual spectrum, where applicable.

A discrete spectrum may describe isolated modes. A continuous spectrum may describe extended or scattering-like excitations. Embedded eigenvalues and threshold states may require separate treatment.

The AES framework does not require the spectrum to be purely discrete.

Nor does it require every spectral mode to correspond to an independently observable particle.

## 4.5 The physical spectrum as a filtered spectrum

The mathematical spectrum may contain modes that fail physical admissibility conditions.

Let \\(\mathcal Q\_{\Phi_0}\\) denote a collection of physical filters, including boundary conditions, regularity, normalizability, gauge reduction, and stability requirements.

Then the physical candidate spectrum is

\\[ \boxed{ \mathfrak S\_{\mathrm{phys}} = \left\\{ [\eta,\omega]: \mathcal P\_{\Phi_0}(\omega)\eta=0,\\; \mathcal Q\_{\Phi_0}[\eta]=\mathrm{true} \right\\}. } \tag{4.7} \\]

This is a classification principle, not yet a numerical prediction.

# 5. Higher-Order Admissibility and Nonlinear Continuation

## 5.1 The limitation of linearized modes

A perturbation may satisfy

\\[ L\_{\Phi_0}\eta=0 \\]

without corresponding to any actual family of nearby admissible configurations.

To test this, consider a formal expansion,

\\[ \Phi\_\epsilon = \Phi_0 + \epsilon\eta + \epsilon^2\xi + O(\epsilon^3). \tag{5.1} \\]

Substitution into the nonlinear admissibility equation gives, at first order,

\\[ L\_{\Phi_0}\eta=0, \tag{5.2} \\]

and at second order,

\\[ L\_{\Phi_0}\xi + \frac12 D\_\Phi^2\mathcal F\big|\_{\Phi_0} [\eta,\eta] = 0. \tag{5.3} \\]

Thus, the second-order correction \\(\xi\\) exists only if the quadratic source term can be balanced by the range of \\(L\_{\Phi_0}\\).

If \\(L\_{\Phi_0}\\) is Fredholm, a solvability condition can be formulated using its adjoint kernel.

Let

\\[ L\_{\Phi_0}^{\*}\psi=0. \\]

Then a necessary second-order condition is

\\[ \boxed{ \left\langle \psi, D\_\Phi^2\mathcal F\big|\_{\Phi_0} [\eta,\eta] \right\rangle = 0 \quad \text{for every } \psi\in\ker L\_{\Phi_0}^{\*}. } \tag{5.4} \\]

The pairing depends on the function spaces and duality structure of the model.

Equation (5.4) is an obstruction test. It determines whether a first-order admissible perturbation can be continued at second order under the stated Fredholm assumptions.

## 5.2 Higher-order obstruction hierarchy

At higher orders, one obtains a sequence of equations,

\\[ L\_{\Phi_0}\eta_n = S_n(\eta_1,\ldots,\eta\_{n-1}), \tag{5.5} \\]

where \\(S_n\\) is constructed from the higher derivatives of \\(\mathcal F\\).

Each order introduces a new solvability condition.

The perturbation is formally integrable only if the hierarchy can be solved consistently.

This yields the distinction:

\\[ \boxed{ \text{Linearized admissibility} \not\Rightarrow \text{Nonlinear integrability}. } \tag{5.6} \\]

The nonlinear excitation space is therefore a subset of the linearized candidate space:

\\[ \mathscr E\_{\Phi_0}^{\mathrm{nl}} \subseteq \mathscr E\_{\Phi_0}^{\mathrm{lin}}, \tag{5.7} \\]

where the inclusion may be strict.

## 5.3 Nonlinear excitation branches

If an admissible perturbation integrates to a finite family, one obtains a branch

\\[ \Phi(s)\in\mathscr A\_\lambda, \qquad \Phi(0)=\Phi_0. \tag{5.8} \\]

The tangent vector is

\\[ \eta = \left. \frac{d\Phi(s)}{ds} \right|\_{s=0}. \tag{5.9} \\]

The branch may represent a family of nearby configurations, a moduli direction, a bifurcating solution, or a nonlinear excitation.

These interpretations are not equivalent. A moduli direction may connect degenerate backgrounds rather than represent a localized particle-like state.

A concrete model must distinguish these possibilities.

# 6. Classification Invariants

## 6.1 The need for invariant classification

A physically meaningful excitation classification cannot depend on arbitrary choices of representative.

If two perturbations differ only by an allowed redundancy, their physical classification must agree.

Let

\\[ I_a: \mathscr E\_{\Phi_0}^{\mathrm{phys}} \rightarrow \mathcal I_a \\]

denote invariant quantities used to distinguish excitation sectors.

The collection

\\[ \mathbf I([\eta]) = \left( I_1([\eta]), I_2([\eta]), \ldots \right) \tag{6.1} \\]

defines an invariant signature.

Possible invariant classes include:

- spectral values;
- conserved charges;
- topological indices;
- symmetry representation labels;
- boundary data;
- asymptotic behavior;
- stability indices;
- relational or geometric invariants.

None is assumed to exist in a particular form until derived from the underlying theory.

## 6.2 Equivalence and completeness

A classification by invariants is complete only if

\\[ \mathbf I([\eta_1]) = \mathbf I([\eta_2]) \quad\Longrightarrow\quad [\eta_1]=[\eta_2]. \tag{6.2} \\]

If this implication fails, the invariants do not distinguish all physical sectors.

The classification may still be useful, but it is incomplete.

This provides a direct mathematical criterion for evaluating whether a proposed set of excitation labels is sufficient.

## 6.3 Degeneracy

Two or more linearly independent physical modes may share the same spectral value.

For an eigenvalue \\(\omega\\), define the physical eigenspace

\\[ \mathscr V\_\omega = \left\\{ [\eta]: \mathcal H\_{\Phi_0}\eta=\omega\eta \right\\}. \tag{6.3} \\]

Its dimension, when well-defined, determines the degeneracy,

\\[ d\_\omega = \dim\mathscr V\_\omega. \tag{6.4} \\]

Degeneracy may arise from symmetry, topology, accidental spectral coincidence, or structural constraints.

A degeneracy is not automatically a particle generation or an internal degree of freedom. Such identifications require additional representation-theoretic derivations.

# 7. Stability and Persistence

## 7.1 Admissibility is not stability

An admissible configuration need not be dynamically stable.

The equation

\\[ \mathcal F[\Phi_0;\lambda]=0 \\]

establishes consistency with the specified constraint. It does not establish persistence under perturbations.

Stability requires a dynamical law.

Let the evolution of a perturbation be described schematically by

\\[ \frac{d\eta}{dt} = \mathcal A\_{\Phi_0}\eta, \tag{7.1} \\]

where \\(\mathcal A\_{\Phi_0}\\) is a generator derived from the theory's actual dynamics.

The linear evolution is formally

\\[ \eta(t) = e^{t\mathcal A\_{\Phi_0}}\eta(0), \tag{7.2} \\]

when the semigroup or group generated by \\(\mathcal A\_{\Phi_0}\\) exists.

## 7.2 Linear stability

A background is linearly stable under the chosen norm if sufficiently small perturbations remain bounded for the relevant evolution interval.

For a time-independent generator, the spectrum of \\(\mathcal A\_{\Phi_0}\\) provides information about linear stability.

For example, a mode

\\[ \eta(t)=e^{st}\eta_0 \\]

grows exponentially when

\\[ \operatorname{Re}(s)>0. \tag{7.3} \\]

The absence of exponentially growing eigenmodes is not always sufficient for bounded evolution, especially for non-normal operators. Transient growth, continuous spectrum, and nonlinear effects must also be considered.

## 7.3 Nonlinear stability

Nonlinear stability requires control of the full evolution, not merely its linearization.

A standard Lyapunov formulation seeks a functional \\(V\\) such that

\\[ V[\eta]\geq 0, \qquad V[0]=0, \\]

and

\\[ \frac{d}{dt}V[\eta(t)]\leq 0. \tag{7.4} \\]

If suitable coercivity and regularity conditions hold, such a functional can establish persistence of a background or excitation.

The existence of such a functional is model-dependent. It is not supplied by the admissibility equation alone.

## 7.4 Stability classification

AES therefore distinguishes:

\\[ \mathscr E\_{\Phi_0}^{\mathrm{lin}}, \qquad \mathscr E\_{\Phi_0}^{\mathrm{nl}}, \qquad \mathscr E\_{\Phi_0}^{\mathrm{stable}}. \\]

These denote, respectively:

- first-order admissible candidates;
- candidates integrable into nonlinear admissible configurations;
- nonlinear excitations satisfying the chosen stability criterion.

A particle interpretation would require additional evidence that a sector corresponds to a localized, persistent, and physically distinguishable excitation.

# 8. Transition Admissibility

## 8.1 Why transitions require a separate condition

The existence of two admissible excitation sectors does not establish that a transition between them is possible.

Let

\\[ [\eta_i],\\;[\eta_f] \in \mathscr E\_{\Phi_0}^{\mathrm{phys}} \\]

denote initial and final sectors.

A transition must preserve the global consistency conditions and satisfy the dynamical restrictions of the theory.

Introduce a transition functional,

\\[ \boxed{ \mathcal T\_{\Phi_0} [\eta_i,\eta_f;\lambda] = 0. } \tag{8.1} \\]

This equation defines a candidate transition-admissibility condition.

The functional may depend on conserved quantities, boundary conditions, background structure, and the dynamics of the underlying configuration.

Its explicit form is not determined by the abstract AES construction.

## 8.2 Three transition classes

Define a relation

\\[ [\eta_i]\rightsquigarrow[\eta_f] \\]

when the transition satisfies the required admissibility conditions.

Three classes are useful.

Allowed transitions

\\[ \mathcal T\_{\Phi_0} [\eta_i,\eta_f;\lambda]=0 \\]

with no additional obstruction under the specified conditions.

Forbidden transitions

The transition fails an exact admissibility or conservation condition.

Suppressed transitions

The transition is not prohibited by the exact constraints but is dynamically small under a separately defined quantitative measure.

The third category must be treated carefully. A transition cannot be called suppressed merely because its amplitude is unknown or expected to be small.

A suppression factor requires a defined dynamical or response structure.

## 8.3 Transition graphs

The excitation structure may be represented by a directed graph,

\\[ \mathcal G\_{\mathrm{AES}} = (\mathcal V,\mathcal E), \tag{8.2} \\]

where:

- vertices represent physically distinct excitation sectors;
- directed edges represent admissible transitions.

If transitions are reversible under the model's dynamics, the corresponding graph may possess additional symmetry. If the theory contains irreversible processes or asymmetric boundary conditions, it need not.

The graph provides a structural representation of selection rules without presupposing a probabilistic interpretation.

## 8.4 Conservation constraints

Suppose a quantity \\(Q\\) is conserved by the underlying dynamics.

Then an allowed transition must satisfy

\\[ Q([\eta_i])=Q([\eta_f]). \tag{8.3} \\]

More generally, for a family of conserved quantities \\(Q_a\\),

\\[ Q_a([\eta_i]) = Q_a([\eta_f]), \qquad a\in\mathcal A. \tag{8.4} \\]

This gives necessary transition restrictions.

It does not establish that conservation laws such as electric charge, baryon number, lepton number, or angular momentum have already been derived by AES. Their appearance and precise form must follow from a concrete realization.

# 9. The Response Kernel

## 9.1 Linear response

The transition relation classifies whether a transition is structurally admissible. It does not yet quantify how a perturbation in one sector influences another.

For this purpose, introduce a source \\(\mathcal J_i\\) associated with an initial sector and a projection \\(\mathcal P_f\\) associated with a final sector.

Where the linearized operator is invertible on an appropriately restricted subspace, define

\\[ \chi\_{\Phi_0} = L\_{\Phi_0}^{-1}. \tag{9.1} \\]

A candidate response kernel is then

\\[ \boxed{ K^{\Phi_0}\_{fi} = \mathcal P_f \chi\_{\Phi_0} \mathcal J_i. } \tag{9.2} \\]

This expression is a proposed response construction, not a derived quantum transition amplitude.

It is meaningful only after specifying:

1. the function spaces on which \\(L\_{\Phi_0}\\) acts;
2. the domain and range of \\(L\_{\Phi_0}\\);
3. the treatment of gauge and zero modes;
4. the source map \\(\mathcal J_i\\);
5. the projection \\(\mathcal P_f\\);
6. the boundary conditions;
7. the relevant inverse or generalized inverse.

## 9.2 The zero-mode problem

If

\\[ \ker L\_{\Phi_0}\neq\\{0\\}, \\]

then \\(L\_{\Phi_0}\\) is not invertible on the full perturbation space.

One must therefore either:

- restrict the operator to a complementary subspace;
- project out the relevant zero modes;
- impose gauge-fixing conditions;
- use a suitable generalized inverse;
- or formulate the response problem through a constrained system.

A formal inverse without these steps is not mathematically justified.

## 9.3 The amplitude gap

Even if the kernel \\(K^{\Phi_0}\_{fi}\\) is well-defined, it is not automatically a transition amplitude.

To identify it with an amplitude, the theory must establish an amplitude space, a composition law, a normalization structure, and a correspondence between response quantities and physical transition events.

To derive probabilities, it must further establish a measure or norm whose operational interpretation is justified.

In particular, the Born rule cannot be inserted as an assumption and then presented as a consequence of the phase framework.

The unresolved problem is:

\\[ \boxed{ K^{\Phi_0}\_{fi} \quad\not\Rightarrow\quad \mathcal A\_{fi} \quad\not\Rightarrow\quad P\_{fi} } \tag{9.3} \\]

without additional derivations.

This is a foundational gap, not a notational inconvenience.

# 10. Excitation Sectors and Particle Interpretation

## 10.1 From sectors to particles

An admissible excitation sector is a mathematical classification object. A particle is a stronger physical claim.

A particle interpretation typically requires some combination of:

- a localized or asymptotically identifiable excitation;
- persistence or stability;
- a well-defined energy-momentum relation;
- appropriate transformation properties;
- operational distinguishability;
- consistent interaction and scattering behavior.

AES does not assume these properties at the outset.

Instead, they become tests that a candidate excitation sector must pass.

## 10.2 Localization

Let \\(\rho\_\eta(x)\\) denote a suitable density associated with a perturbation, if such a density exists in the model.

A localized excitation might satisfy a finiteness condition such as

\\[ \int\_{\Sigma} \rho\_\eta(x)\\,d\mu(x)<\infty. \tag{10.1} \\]

A stronger localization condition could require spatial decay,

\\[ \rho\_\eta(x)\rightarrow 0 \quad \text{as} \quad d(x,x_0)\rightarrow\infty. \tag{10.2} \\]

The measure \\(d\mu\\), distance function, and density must be derived from the model's geometric and dynamical structure.

No localization measure is universal across all possible realizations.

## 10.3 Asymptotic particle states

In theories admitting scattering descriptions, particle-like sectors may be associated with asymptotic states.

The relevant question is whether the admissible excitation structure supports well-defined incoming and outgoing sectors and a consistent scattering map.

An asymptotic state construction would require suitable limits of the full dynamics. Such limits cannot be assumed merely because the linearized perturbation space contains discrete modes.

## 10.4 Ontological neutrality

A sector may ultimately be represented as a field quantum, a stable nonlinear configuration, a geometric excitation, or another structure.

The AES framework does not select among these possibilities.

The mathematical criterion is not whether a candidate resembles a familiar particle model, but whether it satisfies the complete set of admissibility, classification, dynamical, and empirical requirements.

# 11. Relation to the Standard Model

## 11.1 The Standard Model as an empirical benchmark

The Standard Model supplies the primary empirical reference for a particle-spectrum theory.

A successful AES realization would have to reproduce, or explain deviations from, the observed structure of:

- quarks;
- charged leptons;
- neutrinos;
- gauge bosons;
- the Higgs sector;
- color and electroweak interactions;
- particle masses;
- flavor mixing;
- decay channels;
- scattering observables.

The framework does not presently derive this list.

The list is therefore a benchmark against which a concrete realization must be tested, not an output of the abstract definitions.

## 11.2 Gauge representations

Suppose the underlying configuration space admits an action of a group \\(G\\).

A candidate excitation sector may transform under a representation

\\[ \rho: G\rightarrow\mathrm{GL}(V). \tag{11.1} \\]

For this to recover a Standard Model gauge representation, the group, representation space, and action must be derived or independently justified.

The existence of an equivalence group \\(G\_{\Phi_0}\\) in the quotient construction does not automatically establish the gauge group

\\[ SU(3)\_C\times SU(2)\_L\times U(1)\_Y. \\]

Nor does it establish the observed chiral representation content.

These are separate derivation problems.

## 11.3 Mass spectrum

If a suitable relativistic dynamical structure is recovered, one may seek an invariant mass operator or mass-shell relation.

For a state carrying four-momentum \\(p^\mu\\), the conventional relation is

\\[ p\_\mu p^\mu=m^2 \\]

in units with \\(c=1\\), with metric-signature conventions understood.

AES would need to derive the relevant spacetime structure, momentum observable, and dynamical representation before assigning \\(m\\) to an excitation sector.

The eigenvalues of \\(L\_{\Phi_0}\\) cannot simply be relabeled as particle masses.

## 11.4 Flavor and generations

The existence of multiple excitation sectors does not automatically explain the observed fermion generations.

A generation structure would require a derived internal classification, such as a multiplicity of equivalent or related sectors, together with a mechanism explaining their distinct masses and interactions.

Flavor mixing would require a derived map between the relevant interaction and propagation bases.

For example, a mixing matrix \\(U\\) would need to arise from the underlying excitation and interaction structure, rather than being inserted as an empirical parameter and declared emergent.

The CKM and PMNS structures are therefore unresolved targets.

## 11.5 Standard Model matching criterion

A concrete AES realization must establish a mapping

\\[ \mathfrak S\_{\mathrm{AES}} \longrightarrow \mathfrak S\_{\mathrm{SM}} \tag{11.2} \\]

that preserves the relevant observable structure.

At minimum, the map must address:

- state multiplicities;
- quantum numbers;
- mass parameters;
- gauge interactions;
- flavor structure;
- selection rules;
- decay behavior;
- scattering predictions.

A partial match is not a derivation of the Standard Model.

# 12. Rare Processes and Forbidden Channels

## 12.1 Selection rules as structural restrictions

The transition graph introduced in Section 8 provides a natural setting for rare and forbidden processes.

A process may be excluded if its transition violates an exact admissibility condition.

For example, if a conserved quantity \\(Q\\) is established, a transition with

\\[ Q_i\neq Q_f \\]

is forbidden under dynamics preserving \\(Q\\).

This is a structural statement.

It differs from a process that is allowed but dynamically suppressed.

## 12.2 Suppression requires quantitative dynamics

A suppression estimate requires a quantitative transition measure.

If a justified amplitude map \\(\mathcal A\\) is eventually constructed, one might obtain a rate proportional to an appropriate squared amplitude and phase-space factor.

But the relation between amplitude and rate depends on the underlying theory and its normalization.

Until that structure exists, AES can classify exact obstructions and formulate candidate response questions, but cannot provide numerical rare-decay predictions.

## 12.3 A falsifiable rare-process program

A concrete realization could proceed by:

1. identifying a transition predicted to be forbidden by the admissibility structure;
2. identifying a separate transition predicted to be allowed;
3. deriving a quantitative suppression mechanism where one exists;
4. calculating the relevant observable without importing the desired result;
5. comparing with experimental limits and measurements.

A theory that classifies every process as merely “admissible” or “not yet understood” has no predictive advantage.

The transition structure must eventually constrain measurable outcomes.

# 13. Mathematical Propositions

The following results are conditional mathematical statements. They establish properties of the proposed architecture under explicit assumptions; they do not establish the physical existence of any particular particle.

## Proposition 13.1 — Tangent-space characterization

Let \\(\mathcal C\\) be a differentiable configuration manifold, let \\(\mathcal F:\mathcal C\rightarrow\mathcal Y\\) be differentiable, and let \\(\Phi_0\\) satisfy

\\[ \mathcal F(\Phi_0)=0. \\]

If the zero set of \\(\mathcal F\\) is locally a regular submanifold at \\(\Phi_0\\), then

\\[ T\_{\Phi_0}\mathscr A = \ker D\mathcal F\_{\Phi_0}. \\]

Proof.

A tangent vector \\(\eta\\) to a curve \\(\Phi(s)\\) in the admissible set satisfies

\\[ \mathcal F(\Phi(s))=0. \\]

Differentiating at \\(s=0\\),

\\[ D\mathcal F\_{\Phi_0} \left[ \frac{d\Phi}{ds}(0) \right] =0. \\]

Hence every tangent vector lies in the kernel.

Conversely, under the regular-level-set hypothesis, the implicit function theorem identifies the tangent space of the level set with the kernel of the derivative. Therefore the two spaces coincide. \\(\square\\)

## Proposition 13.2 — Gauge-reduced excitation space

Suppose a group \\(G\\) acts smoothly on \\(\mathcal C\\), preserves \\(\mathscr A\\), and the orbit through \\(\Phi_0\\) is regular. Then infinitesimal orbit directions lie in \\(\ker L\_{\Phi_0}\\).

If the action is locally free, the local physical tangent space is represented by

\\[ \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}. \\]

Proof.

Because the group action preserves the admissible set, the orbit through \\(\Phi_0\\) lies in that set. Its tangent vectors are therefore tangent to the admissible set. Proposition 13.1 places these vectors in \\(\ker L\_{\Phi_0}\\). The quotient removes the orbit directions. \\(\square\\)

## Proposition 13.3 — Second-order integrability obstruction

Assume \\(\mathcal F\\) is twice differentiable and \\(L\_{\Phi_0}\\) is Fredholm. If a first-order perturbation \\(\eta\\) extends to a second-order admissible curve, then

\\[ \left\langle \psi, D^2\mathcal F\_{\Phi_0}[\eta,\eta] \right\rangle=0 \\]

for every \\(\psi\in\ker L\_{\Phi_0}^{\*}\\).

Proof.

The second-order expansion requires

\\[ L\_{\Phi_0}\xi = -\frac12D^2\mathcal F\_{\Phi_0}[\eta,\eta]. \\]

The Fredholm alternative requires the right-hand side to be orthogonal to the kernel of the adjoint. The stated condition follows. \\(\square\\)

## Proposition 13.4 — Admissibility does not imply dynamical stability

The equation

\\[ \mathcal F[\Phi_0]=0 \\]

alone cannot establish linear or nonlinear dynamical stability.

Argument.

Stability is a property of an evolution law and a perturbation norm. The admissibility equation specifies a constraint set but does not, by itself, specify how perturbations evolve in time. Distinct evolution laws can preserve the same constraint set while having different stability properties. Therefore stability requires additional dynamical information. \\(\square\\)

## Proposition 13.5 — A complete invariant classifier separates physical sectors

Let \\(\mathbf I\\) be a family of invariants on the quotient excitation space. If

\\[ \mathbf I([\eta_1])=\mathbf I([\eta_2]) \\]

implies

\\[ [\eta_1]=[\eta_2], \\]

then \\(\mathbf I\\) separates all physically distinct sectors.

Proof.

This is precisely the injectivity condition for the invariant map on the quotient space. \\(\square\\)

# 14. A Canonical AES Construction

The preceding sections can be assembled into a sequence of mathematical operations.

## 14.1 Stage I — Background admissibility

Find a background satisfying

\\[ \mathcal F[\Phi_0;\lambda]=0. \tag{14.1} \\]

Establish its existence, regularity, and relevant boundary conditions.

## 14.2 Stage II — Linearized candidate space

Compute

\\[ L\_{\Phi_0} = D\_\Phi\mathcal F\big|\_{\Phi_0} \\]

and determine

\\[ \mathscr E\_{\Phi_0}^{\mathrm{lin}} = \ker L\_{\Phi_0}. \tag{14.2} \\]

This is the first-order candidate space.

## 14.3 Stage III — Redundancy reduction

Determine the symmetry and gauge directions,

\\[ \mathscr G\_{\Phi_0}, \\]

and construct

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} = \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}. \tag{14.3} \\]

## 14.4 Stage IV — Nonlinear integrability

Apply the higher-order solvability conditions to determine which candidate directions extend to actual admissible branches.

Denote the resulting subset by

\\[ \mathscr E\_{\Phi_0}^{\mathrm{nl}}. \tag{14.4} \\]

## 14.5 Stage V — Spectral construction

Derive a dynamical generator or operator pencil from the actual dynamics:

\\[ \mathcal P\_{\Phi_0}(\omega)\eta=0. \tag{14.5} \\]

Determine the spectrum and its functional-analytic properties.

## 14.6 Stage VI — Stability

Analyze the evolution of the nonlinear excitation branches and identify stable, metastable, and unstable sectors under explicitly defined criteria.

## 14.7 Stage VII — Transition structure

Construct

\\[ \mathcal T\_{\Phi_0} [\eta_i,\eta_f;\lambda] \\]

and determine the transition graph.

## 14.8 Stage VIII — Response and observables

Define the response problem, projections, source maps, and any justified observable correspondence.

Only after these steps may the theory attempt to derive particle masses, quantum numbers, transition amplitudes, or rates.

The AES hierarchy

Background consistency

\\(\mathcal F[\Phi_0;\lambda]=0\\)

Linearized admissibility

\\(\ker L\_{\Phi_0}\\)

Physical quotient

\\(\ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}\\)

Nonlinear continuation

Higher-order obstruction tests

Dynamics and stability

Spectral generator and persistence

Transition admissibility

\\(\mathcal T\_{\Phi_0}[\eta_i,\eta_f]=0\\)

Physical spectrum and observables

Requires additional derivations and empirical matching

# 15. Structural Consequences of the Framework

## 15.1 The spectrum is background-dependent

The admissible excitation space is defined relative to a background configuration:

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} = \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}. \\]

A different admissible background \\(\Phi_1\\) generally produces a different linearized operator,

\\[ L\_{\Phi_1} = D\_\Phi\mathcal F\big|\_{\Phi_1}, \\]

and therefore a different candidate excitation space.

Consequently,

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} \neq \mathscr E\_{\Phi_1}^{\mathrm{phys}} \\]

in general.

This is not a defect. It is a structural feature: the excitation spectrum may depend on the phase configuration in which excitations are embedded.

The theory must determine whether observed particle species correspond to universal sectors, background-dependent sectors, or stable sectors shared by a class of backgrounds.

## 15.2 Spectral bifurcation

Suppose the admissibility equation depends on a parameter \\(\lambda\\). A family of backgrounds may satisfy

\\[ \mathcal F[\Phi_0(\lambda);\lambda]=0. \tag{15.1} \\]

The linearized operator then becomes a parameter-dependent family,

\\[ L(\lambda) = D\_\Phi\mathcal F \big|\_{\Phi_0(\lambda)}. \tag{15.2} \\]

At certain parameter values, the dimension of the kernel may change:

\\[ \dim\ker L(\lambda\_-) \neq \dim\ker L(\lambda\_+). \tag{15.3} \\]

Such a change signals a possible bifurcation or degeneracy transition in the admissible configuration space.

If a dynamical spectral operator is also defined, its eigenvalues may undergo crossings, splitting, or the emergence of additional modes.

This suggests a possible mechanism for changes in excitation structure across different admissible backgrounds. It does not, by itself, explain particle generations or cosmological particle production.

## 15.3 Spectral gaps

If a self-adjoint dynamical generator exists and possesses a discrete spectrum, one may define a spectral gap above a reference state:

\\[ \Delta = \inf\_{\omega\in\sigma(\mathcal H\_{\Phi_0})\setminus\\{\omega_0\\}} |\omega-\omega_0|. \tag{15.4} \\]

A nonzero gap can be relevant to stability, persistence, and low-energy effective descriptions.

But the existence of a gap is not guaranteed. It depends on the operator, its domain, boundary conditions, and the geometry of the configuration space.

A gap in the spectrum of the linearized consistency operator would not automatically be a physical mass gap.

## 15.4 Spectral accumulation and infinite sectors

The excitation spectrum need not contain finitely many sectors.

Possible structures include:

- finite discrete collections;
- countably infinite discrete spectra;
- continuous families;
- mixed discrete-continuous spectra;
- accumulation points;
- parameterized families of inequivalent sectors.

A theory predicting an infinite collection must establish whether the sectors are physically distinguishable and whether their observable consequences are consistent with experiment.

An infinite mathematical spectrum is not automatically an infinite set of observable particles.

# 16. The Admissibility–Dynamics Distinction

A recurring danger in foundational spectrum theories is the conflation of consistency with evolution.

AES separates the two.

The admissibility functional determines which configurations satisfy the structural constraint:

\\[ \mathcal F[\Phi;\lambda]=0. \tag{16.1} \\]

The dynamical law determines how configurations change:

\\[ \frac{d\Phi}{dt} = \mathcal X[\Phi;\lambda], \tag{16.2} \\]

or, in a more general formulation, through a relational or variational evolution rule.

The two structures may be related. For example, a consistent evolution may preserve the admissible set:

\\[ \Phi(0)\in\mathscr A\_\lambda \quad\Longrightarrow\quad \Phi(t)\in\mathscr A\_\lambda. \tag{16.3} \\]

But this preservation property must be demonstrated.

A necessary infinitesimal condition for a smooth flow to remain tangent to the admissible set is

\\[ D\_\Phi\mathcal F[\Phi] \big[ \mathcal X[\Phi] \big] =0 \qquad \text{whenever } \mathcal F[\Phi]=0. \tag{16.4} \\]

This equation expresses tangency of the dynamical vector field to the admissible configuration manifold.

It is a useful compatibility condition between the constraint and the dynamics.

It does not uniquely determine the dynamics.

## 16.1 Constraint preservation proposition

Suppose \\(\mathscr A\_\lambda\\) is a regular constraint manifold and \\(\mathcal X\\) is a sufficiently smooth vector field tangent to it at every point. Then the local flow generated by \\(\mathcal X\\), for as long as it exists, preserves \\(\mathscr A\_\lambda\\).

The proposition follows from the invariance of a regular submanifold under a vector field tangent to that submanifold.

The result provides a consistency test for a future PAPD realization: its proposed dynamics must preserve the admissibility condition, or explicitly account for controlled departures from it.

## 16.2 Why this distinction matters for particles

A perturbation may be:

1. admissible but dynamically unstable;
2. admissible and stable but not localized;
3. localized but not independently distinguishable;
4. distinguishable but unable to participate in a specified transition;
5. dynamically persistent but not associated with an isolated spectral value.

Only a subset of admissible perturbations may satisfy all the requirements for a particle interpretation.

The spectrum must therefore be filtered through independent mathematical tests rather than inferred directly from the kernel of the consistency operator.

# 17. Relation to Established Spectral and Geometric Methods

AES is a proposed organizational framework, not a replacement for established spectral theory. Its mathematical development must use established tools where applicable.

## 17.1 Linear stability and normal-mode analysis

Linearized perturbation analysis is standard in differential equations, continuum mechanics, field theory, and mathematical physics.

AES adopts the general structure of linearization around a background, but gives the kernel of the consistency operator a specific role in classifying admissible perturbations.

The novelty claim cannot rest on linearization itself.

The potentially distinctive contribution is the explicit organization of excitation classification around a global admissibility condition, followed by quotient reduction, nonlinear integrability, stability, and transition admissibility.

Whether this organization yields new theorems or predictions remains to be established.

## 17.2 Constrained Hamiltonian systems

In constrained Hamiltonian mechanics, physical states are obtained by imposing constraints and reducing redundant degrees of freedom.

The AES quotient construction has a formal resemblance to this procedure.

However, no symplectic form, Poisson bracket, canonical variables, first-class constraint algebra, or Hamiltonian constraint structure has yet been derived here.

It would therefore be premature to identify the AES quotient with a Dirac constraint reduction.

A concrete realization may eventually admit such a formulation, but that is an open construction.

## 17.3 Gauge theory

Gauge theories distinguish physical degrees of freedom from redundant descriptions. AES similarly requires a quotient by transformations that leave the physical configuration unchanged.

But the existence of a quotient group does not establish a local gauge field, a connection, a curvature, or a gauge boson spectrum.

Those structures require their own derivation.

## 17.4 Soliton and defect theory

Nonlinear field theories can support localized stable solutions, including solitons and topological defects.

Such solutions may be candidate realizations of excitation sectors.

AES does not privilege them. A particle-like sector might instead arise through another mechanism.

The relevant question is whether a candidate solution satisfies the admissibility, stability, localization, and empirical conditions—not whether it belongs to a familiar solution class.

## 17.5 Operator theory

The spectral component of AES requires functional analysis: closed operators, domains, resolvents, self-adjoint extensions, Fredholm properties, and spectral stability.

These are not optional mathematical details.

For example, an unbounded operator is not specified by a differential expression alone. Its domain and boundary conditions are part of its definition.

Any concrete AES model that reports eigenvalues without specifying these structures has not fully defined its spectral problem.

# 18. A Concrete Research Program

The abstract framework becomes physically meaningful only through a sequence of explicit constructions.

## 18.1 Problem A: Specify the configuration space

A complete model must define:

\\[ \mathcal C,\qquad \Phi,\qquad \lambda,\qquad \mathcal F. \\]

It must state whether \\(\Phi\\) is a scalar, a multiplet, a section of a bundle, a geometric object, or another mathematical entity.

It must also specify the topology, differentiable structure, regularity class, and boundary conditions.

## 18.2 Problem B: Derive the linearized operator

The operator

\\[ L\_\Phi=D\_\Phi\mathcal F \\]

must be calculated explicitly.

Its domain, codomain, kernel, range, adjoint, and Fredholm properties must be established where relevant.

The calculation must not rely on treating a formal functional derivative as a fully defined operator.

## 18.3 Problem C: Determine the redundancy structure

The model must identify transformations that leave the physical configuration unchanged.

It must demonstrate that these transformations preserve admissibility and characterize their infinitesimal action.

Only then can the quotient excitation space be constructed.

## 18.4 Problem D: Solve the nonlinear continuation problem

For every proposed excitation direction, the model must determine whether higher-order obstructions vanish.

The result should classify perturbations into:

- integrable branches;
- obstructed directions;
- gauge or moduli directions;
- unresolved cases.

## 18.5 Problem E: Derive the dynamical operator

A dynamical law must be obtained independently of the desired spectrum.

The model must show how its generator acts on the physical excitation space and whether it preserves the admissibility constraints.

If a variational structure is proposed, the action, variation, boundary terms, and resulting equations must be supplied.

## 18.6 Problem F: Compute the spectrum

A concrete calculation must produce spectral data rather than merely define a spectral equation.

It must include:

- operator domains;
- boundary conditions;
- eigenvalue or continuous-spectrum analysis;
- degeneracy;
- convergence and numerical error estimates where applicable;
- stability under changes in the background and parameters.

## 18.7 Problem G: Establish physical interpretation

The model must demonstrate how spectral data correspond to measurable quantities.

This includes identifying the relevant observables, establishing their transformation properties, and deriving the relationship between theoretical quantities and experimental measurements.

## 18.8 Problem H: Derive transition structure

The transition functional must be calculated.

The theory must then determine which transitions are forbidden, which are allowed, and which are quantitatively suppressed.

A response kernel alone is not sufficient.

## 18.9 Problem I: Recover known physics

The model must recover the empirically established particle spectrum and interaction structure to the accuracy demanded by current measurements.

Only after this step can deviations be treated as novel predictions.

# 19. Falsifiability and Experimental Tests

## 19.1 The minimum requirement for prediction

A theoretical framework is not empirically predictive merely because it can accommodate observed phenomena.

AES must eventually produce restrictions that could have been otherwise.

The strongest tests are those in which the admissibility structure excludes a possibility or fixes a quantitative relation without using the experimental result as an input.

## 19.2 Test class I: Missing or forbidden sectors

If a concrete model predicts that certain candidate sectors cannot satisfy the admissibility condition, then the discovery of a corresponding physical excitation would challenge that model.

This requires an unambiguous correspondence between the theoretical sector and the observed state.

A vague assertion that a state is “inadmissible” is not testable without a defined observable signature.

## 19.3 Test class II: Unexpected excitation multiplicity

If the theory derives a fixed number of distinct excitation sectors in a specified energy or parameter range, the discovery of additional sectors—or the absence of predicted ones—can test the construction.

The predicted multiplicity must be derived rather than chosen to reproduce the known particle count.

## 19.4 Test class III: Spectral relations

If the theory derives a parameter-independent or parameter-constrained relation among spectral values, that relation can be tested against measured masses or resonance frequencies after the physical identification has been established.

The relation must not be obtained by fitting the same measurements it is subsequently claimed to predict.

## 19.5 Test class IV: Transition restrictions

A derived transition graph may exclude certain processes.

Observation of a robust process that the theory proves impossible would falsify the relevant realization, subject to the validity of the experimental identification and the theory's stated domain.

## 19.6 Test class V: Background dependence

If the excitation spectrum depends on an environmental or background parameter, the theory may predict a corresponding change in measurable spectral properties.

The predicted dependence must be quantitatively specified.

## 19.7 Test class VI: Rare processes

A concrete realization may predict a suppression pattern among rare transitions.

Such a claim requires a complete dynamical calculation, not merely a qualitative selection rule.

## 19.8 Experimental discipline

A successful test program must distinguish:

- a prediction fixed before measurement;
- a postdiction derived after observing the data;
- a parameter fitted to measurements;
- a structural possibility;
- a conjecture;
- an experimentally excluded result.

These categories must not be conflated.

# 20. Limitations and Unresolved Problems

The present framework establishes a mathematical organization for the admissible excitation problem. It does not yet establish a complete physical theory.

The following gaps are fundamental.

## 20.1 The admissibility functional is unspecified

The general equation

\\[ \mathcal F[\Phi;\lambda]=0 \\]

defines the framework but does not determine its physical content.

A concrete functional must be constructed and justified.

Without it, the excitation space cannot be calculated.

## 20.2 The configuration space is not fixed

The mathematical nature of \\(\Phi\\) and the configuration space \\(\mathcal C\\) remain model-dependent.

The function spaces, topology, differentiability, and boundary conditions must be specified before rigorous operator analysis is possible.

## 20.3 No physical Hamiltonian has been derived

The linearized consistency operator is not a Hamiltonian.

A dynamical generator must be derived from an independent evolution law or variational structure.

## 20.4 No mass spectrum has been derived

The framework does not yet produce the masses of quarks, leptons, gauge bosons, or other physical excitations.

A mass operator and its connection to observables remain to be established.

## 20.5 No Standard Model representation content has been derived

The gauge group, representation assignments, chirality, and quantum numbers remain unresolved.

## 20.6 The response-to-amplitude map is unresolved

The response kernel does not automatically define an amplitude.

A mathematical construction of amplitudes, normalization, composition, and probabilities is still required.

## 20.7 The Born rule is not derived

No probability law follows from the present equations.

A valid derivation would require a justified measure, response structure, and operational correspondence. Assuming the Born rule would not constitute deriving it.

## 20.8 Flavor physics remains unresolved

The framework does not yet derive:

- the number of fermion generations;
- the CKM matrix;
- the PMNS matrix;
- observed flavor hierarchies;
- CP-violating parameters.

These require explicit calculations.

## 20.9 Lorentzian causality remains unresolved

The framework has not derived a Lorentzian spacetime metric or established relativistic causal propagation.

A particle-spectrum construction must not silently assume these results.

## 20.10 No numerical rare-decay predictions exist

Without a derived transition amplitude and dynamical normalization, numerical decay rates cannot be claimed.

## 20.11 Novelty remains conditional

The individual mathematical tools used here—linearization, quotient spaces, Fredholm solvability, spectral operators, stability analysis, and transition graphs—are established.

The proposed contribution is their organization into a constraint-first excitation classification program within the PAPD setting.

A stronger novelty claim would require a theorem, invariant, or experimentally discriminating result not already obtainable from established methods.

# 21. Central Theorem Program: From Admissibility to a Physical Spectrum

The framework suggests a sequence of theorems that a complete realization should attempt to establish.

These are research targets, not results already proved by the abstract construction.

### Theorem target I — Existence of the physical excitation manifold

Establish conditions under which

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} = \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0} \\]

has a well-defined local manifold or stratified-space structure.

The main difficulties are regularity, singular gauge orbits, changing kernel dimension, and nontrivial stabilizers.

### Theorem target II — Nonlinear integrability classification

Determine necessary and sufficient conditions under which a linearized admissible perturbation extends to a nonlinear admissible branch.

The second-order Fredholm condition is only the first obstruction. A complete result must control all relevant orders or establish convergence of the perturbative construction.

### Theorem target III — Spectral completeness

For a derived dynamical generator \\(\mathcal H\_{\Phi_0}\\), establish whether the physical excitation sectors admit a complete spectral decomposition.

This requires an appropriate operator domain, spectral measure where applicable, and control over continuous and residual spectrum.

### Theorem target IV — Stability classification

Determine which nonlinear excitation branches are stable under the actual dynamics and whether their stability persists under admissible changes in the background.

### Theorem target V — Transition closure

Establish conditions under which the admissible transition relation is closed under composition.

If

\\[ [\eta_1]\rightsquigarrow[\eta_2], \qquad [\eta_2]\rightsquigarrow[\eta_3], \\]

one must determine whether

\\[ [\eta_1]\rightsquigarrow[\eta_3] \\]

necessarily follows, or whether intermediate dynamics, conserved quantities, and boundary conditions can obstruct the composite transition.

This is not automatic. A transition relation need not be transitive.

### Theorem target VI — Observable correspondence

Construct a map from the physical excitation space to operationally defined observables and establish the conditions under which the map preserves physically relevant distinctions.

Only with this result could the abstract excitation classification become an empirically interpretable particle spectrum.

# 22. Conjectures and Research Hypotheses

The following statements are conjectural directions. They are not established consequences of the equations developed above.

Conjecture 22.1 — Admissibility selection.

For a sufficiently restrictive global admissibility functional, the physically realizable excitation sectors form a proper subset of the mathematically available perturbation space:

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} \subsetneq \mathcal V\_{\Phi_0}. \\]

The significance of this conjecture depends on whether the excluded directions can be characterized independently and whether the resulting restrictions correspond to physical observations.

Conjecture 22.2 — Nonlinear selection.

The nonlinear obstruction hierarchy may remove a substantial subset of perturbations that appear admissible at first order.

If so, the physical excitation spectrum may be more restrictive than the linearized kernel suggests.

Conjecture 22.3 — Background-dependent spectral organization.

Changes in admissible background configurations may alter excitation multiplicities, degeneracies, and spectral gaps.

This could provide a general mathematical mechanism for phase-dependent changes in the available excitation structure.

It does not yet imply that known particle generations originate in such changes.

Conjecture 22.4 — Transition selection from global consistency.

Some transition restrictions may follow from global admissibility conditions rather than from independently imposed conservation rules.

To establish this conjecture, a concrete model must derive the relevant conserved quantities or selection rules from its own structure.

Conjecture 22.5 — Emergent particle ontology.

A particle interpretation may arise as a special class of admissible excitation sectors satisfying localization, persistence, spectral distinguishability, and consistent interaction requirements.

This would make particle ontology a derived property rather than a foundational assumption.

Conjecture 22.6 — Spectral economy.

A sufficiently restrictive admissibility structure may generate a smaller physical spectrum than the unrestricted perturbation theory would permit.

A successful realization would need to quantify this economy and show that it is not merely an artifact of arbitrary constraints.

# 23. Novelty Assessment and Epistemic Status

A foundational proposal must distinguish its mathematical content from its physical claims.

| Component                        | Status                          | Assessment                                                       |
| -------------------------------- | ------------------------------- | ---------------------------------------------------------------- |
| Nonlinear admissibility equation | Foundational assumption         | General framework; requires a concrete functional                |
| Linearized consistency operator  | Established mathematics         | Standard functional differentiation                              |
| Kernel as tangent space          | Conditional theorem             | Follows under regularity assumptions                             |
| Quotient by redundancies         | Established mathematical method | Requires an explicitly derived action                            |
| Nonlinear obstruction hierarchy  | Established method              | Application to the proposed framework remains to be performed    |
| Dynamical spectral operator      | Unresolved construction         | Cannot be identified with the consistency operator by assumption |
| Stability classification         | Unresolved construction         | Requires an evolution law                                        |
| Transition functional            | Proposed structure              | Explicit form remains unknown                                    |
| Response kernel                  | Candidate construction          | Requires domain, inverse, sources, and projections               |
| Response-to-amplitude map        | Unresolved                      | Not established                                                  |
| Born-rule derivation             | Unresolved                      | Not established                                                  |
| Standard Model spectrum          | Unresolved                      | No particle roster derived                                       |
| Masses and quantum numbers       | Unresolved                      | No numerical or representation-theoretic derivation              |
| Flavor mixing                    | Unresolved                      | No CKM or PMNS derivation                                        |
| Rare-decay predictions           | Unresolved                      | No numerical rates derived                                       |

## 23.1 What is potentially new

The potentially distinctive contribution is the separation and ordering of five problems that are often treated together:

\\[ \boxed{ \begin{aligned} &\text{Admissibility}\\\ &\downarrow\\\ &\text{Physical equivalence}\\\ &\downarrow\\\ &\text{Nonlinear integrability}\\\ &\downarrow\\\ &\text{Dynamical stability}\\\ &\downarrow\\\ &\text{Transition admissibility}. \end{aligned} } \\]

The ordering prevents a first-order perturbation from being automatically identified as a particle, a mathematical eigenvalue from being automatically identified as a mass, or a response coefficient from being automatically identified as a probability amplitude.

The framework's strongest immediate contribution is therefore methodological and structural.

Its physical novelty remains unproven.

## 23.2 The decisive obstacle

The central obstacle is not the definition of an admissible perturbation space. That can be accomplished abstractly.

The decisive obstacle is the construction of a concrete admissibility functional and a compatible dynamical theory that yield a nontrivial, calculable, empirically successful spectrum.

Without those structures, AES remains a classification architecture.

With them, it could become a predictive theory of excitation organization.

# 24. Conclusion

The Admissible Excitation Spectrum formulates the particle-spectrum problem as a sequence of constrained mathematical constructions.

Its foundational object is an admissible background configuration,

\\[ \mathcal F[\Phi_0;\lambda]=0. \\]

The first-order admissible perturbations are determined by

\\[ L\_{\Phi_0}\eta=0, \qquad L\_{\Phi_0}=D\_\Phi\mathcal F\big|\_{\Phi_0}. \\]

Physical distinctions are then introduced through a quotient by the appropriate redundancy structure:

\\[ \mathscr E\_{\Phi_0}^{\mathrm{phys}} = \ker L\_{\Phi_0}/\mathscr G\_{\Phi_0}. \\]

But this is only the beginning of the spectrum problem.

The theory must determine which perturbations extend to nonlinear admissible branches, which are dynamically stable, which possess a well-defined spectral characterization, and which can participate in consistent transitions.

The resulting hierarchy is:

\\[ \boxed{ \begin{aligned} \text{Configuration} &\rightarrow \text{Admissibility}\\\ &\rightarrow \text{Linearized perturbations}\\\ &\rightarrow \text{Physical equivalence classes}\\\ &\rightarrow \text{Nonlinear excitation sectors}\\\ &\rightarrow \text{Dynamical spectrum}\\\ &\rightarrow \text{Stability}\\\ &\rightarrow \text{Transition structure}\\\ &\rightarrow \text{Physical observables}. \end{aligned} } \\]

The distinction between these levels is essential. It prevents mathematical possibilities from being mistaken for physical particles and prevents unresolved dynamical assumptions from being hidden inside spectral notation.

The framework does not yet derive the Standard Model, particle masses, quantum numbers, flavor structure, or transition probabilities. It does not establish a Born-rule derivation, a Lorentzian causal structure, or a numerical prediction for rare processes. These are not minor omissions: they are the central tasks required to turn the framework into a physical theory.

Nevertheless, the formulation establishes a precise research direction. Rather than beginning with an assumed particle inventory and asking how to accommodate it, one begins with the admissibility structure of the underlying configuration and asks which excitation sectors can actually exist.

The central hypothesis is that the physical spectrum is not an arbitrary list of fundamental entities, but a restricted structure selected by consistency, equivalence, nonlinear integrability, and dynamics.

The decisive test is whether that restriction can be calculated.

\\[ \boxed{ \text{A physical excitation is not merely a permitted perturbation.} } \\]

\\[ \boxed{ \text{It must be a distinct, integrable, dynamically meaningful, and empirically identifiable sector.} } \\]

That is the defining principle of the Admissible Excitation Spectrum.

## 25. Final Research Position

The current theory should be regarded as a foundational mathematical program, not a completed particle theory.

Its next decisive milestone is a worked model in which the abstract construction is replaced by explicit mathematics:

\\[ \mathcal F[\Phi;\lambda] \quad\longrightarrow\quad L\_\Phi \quad\longrightarrow\quad \ker L\_\Phi \quad\longrightarrow\quad \mathscr E\_\Phi^{\mathrm{phys}} \quad\longrightarrow\quad \mathcal H\_\Phi \quad\longrightarrow\quad \sigma(\mathcal H\_\Phi). \\]

That model must calculate at least one nontrivial excitation sector, establish its nonlinear status, determine its stability, and derive a measurable spectral quantity.

Only then will the theory have crossed from an admissibility-based classification framework into a demonstrated physical spectrum construction.

The governing research question is therefore:

Can the observed organization of physical excitations be derived as the restricted spectrum of globally admissible phase configurations, rather than imposed as a fundamental particle inventory?

The Admissible Excitation Spectrum provides a mathematical architecture in which that question can be addressed without assuming its answer.

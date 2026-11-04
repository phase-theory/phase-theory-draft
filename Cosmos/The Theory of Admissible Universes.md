# The Theory of Admissible Universes
## A Mathematical Framework for Classifying Consistent Physical Models and Deriving Restrictions on Low-Energy Structure

### Abstract

The Theory of Admissible Universes (TAU) investigates whether physically meaningful restrictions on the possible structure of a universe can be derived from a sufficiently precise collection of mathematical and physical consistency conditions, without assuming at the outset that the universe must obey one predetermined set of laws.

The fundamental object is not a single dynamical theory but a space of candidate models,
\[
\mathscr U=\{U\},
\]
equipped with a consistency functional
\[
\mathfrak F:\mathscr U\longrightarrow [0,\infty].
\]
The admissible class is defined by
\[
\mathscr U_{\mathrm{adm}}
=
\{U\in\mathscr U:\mathfrak F[U]=0\}.
\]
The central question is whether independently motivated requirements—stability, symmetry, locality, unitarity, causal consistency, and the existence of a controlled low-energy limit—jointly restrict this class sufficiently to force nontrivial structural conclusions.

A central distinction is maintained throughout: mathematical consistency is not equivalent to physical realization, and physical admissibility is not equivalent to uniqueness. A nonempty admissible class may contain many inequivalent models. Consequently, the theory does not assume that consistency alone selects our universe. It seeks classification and exclusion theorems that establish what structures are necessary, forbidden, or left undetermined within explicitly defined model families.

The paper develops a general variational and logical framework for admissibility, defines equivalence classes of candidate universes, distinguishes exact constraints from approximate consistency conditions, and formulates a hierarchy of admissibility tests. It then establishes a concrete exclusion result using a family of one-dimensional quantum lattice systems with finite-range interactions, translation symmetry, and conserved \(U(1)\) charge. At noninteger filling, the Lieb–Schultz–Mattis flux-insertion argument excludes a unique, translation-invariant, symmetry-preserving, gapped ground state under the stated assumptions. This result demonstrates the form of a genuine admissibility theorem: the joint constraints do not select a unique Hamiltonian, but they eliminate an entire class of otherwise plausible low-energy structures.

The resulting framework is intended as a research program for the classification of physically admissible theories. Its strongest prospective objective is to determine whether increasingly general consistency requirements constrain the low-energy universality classes of candidate universes, and under what additional assumptions those constraints become predictive.

**Keywords:** admissible universes; consistency functionals; model classification; quantum consistency; locality; stability; symmetry; effective field theory; exclusion theorems; universality classes; anomaly constraints; mathematical physics.

---

## 1. Introduction

### 1.1 The inverse problem of physical law

Conventional theoretical physics usually begins with a selected mathematical structure and investigates its consequences. A theory specifies some combination of:

- a state space;
- dynamical variables;
- equations of motion;
- symmetries;
- interaction terms;
- boundary or initial conditions;
- a prescription for observables.

The resulting mathematical system is then tested for internal consistency and empirical adequacy.

The Theory of Admissible Universes reverses the order of the initial question.

Rather than beginning with one presumed set of physical laws, it asks:

> What classes of mathematical structures could support coherent, stable, and physically interpretable dynamics while satisfying a specified collection of independent consistency requirements?

This is an inverse problem. Its unknown is not initially a trajectory, a field configuration, or a coupling constant. Its unknown is the admissible structure of the theory itself.

The distinction is important. If a particular physical theory is assumed at the beginning, its structural possibilities are already heavily constrained by the assumptions used to construct it. A classification approach attempts to make those assumptions explicit and investigate their combined consequences.

The ambition is not to derive arbitrary physical laws from the word *consistency*. The ambition is to identify a sufficiently restrictive set of physically motivated conditions for which mathematical classification becomes possible.

### 1.2 The three levels of the problem

Let \(\mathscr U\) denote a specified class of candidate models. Three questions must be separated.

**Level I — Internal consistency**

Does the model define a mathematically coherent structure? Are its state spaces, operators, constraints, and evolution maps well-defined?

**Level II — Physical admissibility**

Does the model support stable states, coherent dynamics, acceptable causal structure, and a controlled interpretation of observables?

**Level III — Structural selection**

Do the admissibility conditions restrict the possible models sufficiently to imply nontrivial properties of their low-energy behavior?

The third level is the principal objective. It is also the most difficult.

A consistency condition may exclude inconsistent models without selecting a unique model. Even a large collection of constraints may leave a continuous family of solutions. Therefore, uniqueness must be established as a theorem, not introduced as an implicit assumption.

### 1.3 The central hypothesis

The working hypothesis of TAU is:

\[
\boxed{
\text{Independent physical consistency requirements can jointly constrain the structure of admissible dynamics.}
}
\]

A stronger hypothesis is:

\[
\boxed{
\text{For certain model families, admissibility conditions imply restricted low-energy universality classes.}
}
\]

The stronger hypothesis is not assumed to hold universally. It is a research objective to be tested model family by model family.

The distinction between these statements is essential. The first concerns the existence of restrictions. The second concerns the power of those restrictions to determine emergent physical structure.

### 1.4 What this theory is not claiming

TAU does not claim that:

1. every mathematically consistent structure is physically realizable;
2. consistency alone determines the constants of nature;
3. all admissible universes must share one spacetime dimension;
4. locality, unitarity, and stability uniquely determine a quantum field theory;
5. the universe is necessarily the global minimum of a universal functional;
6. a formal classification of models establishes which model is empirically realized.

Each of these would require additional premises and independent arguments.

The appropriate standard is narrower and more rigorous: define a candidate family, define the admissibility conditions, prove the resulting classification or exclusion theorem, and identify precisely what remains free.

---

## 2. Mathematical Definition of the Candidate Universe Space

### 2.1 Candidate models as structured objects

A candidate universe must be specified by enough mathematical data to determine what counts as a model and what it means for two models to be equivalent.

We write a candidate model as

\[
U=
(\mathcal S,\mathcal A,\mathcal D,\mathcal G,
\mathcal O,\mathcal B),
\]

where:

- \(\mathcal S\) is the state-space structure;
- \(\mathcal A\) is the algebra of physical or kinematic observables;
- \(\mathcal D\) is the dynamical structure;
- \(\mathcal G\) is the symmetry structure;
- \(\mathcal O\) is the prescription for physical observables and their interpretation;
- \(\mathcal B\) denotes boundary, initial-state, and global structural data.

This is a schematic decomposition. Particular model families may require additional components.

For a quantum theory, one possible realization is

\[
U=
(\mathcal H,\mathcal A,H,\mathcal G,\omega),
\]

with Hilbert space \(\mathcal H\), observable algebra \(\mathcal A\), Hamiltonian \(H\), symmetry group \(\mathcal G\), and state or state-selection prescription \(\omega\).

For a classical field theory, a candidate may instead take the form

\[
U=
(M,\mathcal E,\mathcal L,\mathcal G,\mathcal B),
\]

where \(M\) is a spacetime or configuration manifold, \(\mathcal E\) a field bundle, \(\mathcal L\) a dynamical or variational structure, \(\mathcal G\) a symmetry group, and \(\mathcal B\) the relevant boundary data.

The framework does not identify these two constructions. It supplies a common classification language while allowing the underlying mathematical categories to differ.

### 2.2 The model space

Let \(\mathscr U_{\mathfrak C}\) denote a class of candidate models satisfying a set of preliminary structural assumptions \(\mathfrak C\).

The subscript is important. A model space cannot be defined independently of its category, regularity conditions, dimensionality, and allowed structures.

For example, the class of all finite-dimensional Hamiltonian systems is different from the class of local quantum field theories on globally hyperbolic spacetimes. A theorem proved for the former cannot automatically be transferred to the latter.

We therefore define

\[
\mathscr U_{\mathfrak C}
=
\{U:U\text{ satisfies the defining conditions of }\mathfrak C\}.
\]

The classification problem is always relative to a specified \(\mathfrak C\).

### 2.3 Equivalence and redundancy

Distinct mathematical descriptions may represent the same physical model.

Let \(\sim\) be an equivalence relation on \(\mathscr U_{\mathfrak C}\). Its meaning must be specified for each model family.

Possible equivalences include:

- unitary equivalence of quantum representations;
- gauge equivalence;
- diffeomorphism equivalence;
- isomorphism of observable algebras preserving the relevant dynamics;
- equivalence under an explicitly permitted field redefinition.

The physical model space is then represented by the quotient

\[
\widehat{\mathscr U}_{\mathfrak C}
=
\mathscr U_{\mathfrak C}/\sim.
\]

A consistency functional should be invariant under this equivalence:

\[
U\sim V
\quad\Longrightarrow\quad
\mathfrak F[U]=\mathfrak F[V].
\]

Otherwise, the functional may distinguish descriptions rather than physical structures.

This requirement is not automatic. In particular, field redefinitions that are harmless at one level of description may alter the interpretation of observables or boundary conditions. Only transformations proven to preserve the chosen physical content should be included in \(\sim\).

---

## 3. The Consistency Functional

### 3.1 General definition

The central formal object is a nonnegative functional

\[
\mathfrak F:
\mathscr U_{\mathfrak C}
\longrightarrow
[0,\infty].
\]

The exactly admissible class is

\[
\boxed{
\mathscr U_{\mathrm{adm}}
=
\{U\in\mathscr U_{\mathfrak C}:
\mathfrak F[U]=0\}.
}
\]

The value \(\mathfrak F[U]=0\) means that every condition encoded by the functional is satisfied exactly.

The functional is not itself a physical law. It is a mathematical encoding of a specified collection of conditions.

Its usefulness depends entirely on the precision and justification of those conditions.

### 3.2 Decomposition into independent constraints

A useful construction is

\[
\mathfrak F[U]
=
\sum_{a=1}^{N}w_a\,\mathfrak F_a[U],
\qquad
w_a>0,
\]

where each component represents a distinct requirement.

A prospective decomposition is

\[
\begin{aligned}
\mathfrak F[U]
={}&
w_{\mathrm{mat}}\mathfrak F_{\mathrm{mat}}[U]
+w_{\mathrm{stab}}\mathfrak F_{\mathrm{stab}}[U]\\
&+w_{\mathrm{sym}}\mathfrak F_{\mathrm{sym}}[U]
+w_{\mathrm{loc}}\mathfrak F_{\mathrm{loc}}[U]\\
&+w_{\mathrm{q}}\mathfrak F_{\mathrm{q}}[U]
+w_{\mathrm{caus}}\mathfrak F_{\mathrm{caus}}[U]\\
&+w_{\mathrm{IR}}\mathfrak F_{\mathrm{IR}}[U].
\end{aligned}
\]

Here:

- \(\mathfrak F_{\mathrm{mat}}\) measures failures of mathematical well-definedness;
- \(\mathfrak F_{\mathrm{stab}}\) measures violations of the chosen stability criterion;
- \(\mathfrak F_{\mathrm{sym}}\) measures violations of required symmetry relations;
- \(\mathfrak F_{\mathrm{loc}}\) measures violations of the specified locality condition;
- \(\mathfrak F_{\mathrm q}\) measures violations of the selected quantum consistency conditions;
- \(\mathfrak F_{\mathrm{caus}}\) measures violations of the causal requirements;
- \(\mathfrak F_{\mathrm{IR}}\) measures failures of the required low-energy limit.

The terms need not be numerical in every application. A component can be a nonnegative extended-real functional, an indicator functional, or a norm of a mathematically defined residual.

For an exact constraint \(C_a[U]=0\), a simple choice is

\[
\mathfrak F_a[U]=\|C_a[U]\|^2.
\]

For a forbidden condition, one may use an indicator:

\[
I_{\mathcal K}(U)=
\begin{cases}
0,&U\notin\mathcal K,\\
+\infty,&U\in\mathcal K,
\end{cases}
\]

where \(\mathcal K\) is the forbidden subset.

The latter is useful when a violation is categorical rather than naturally measured by a continuous residual.

### 3.3 Why positive weights matter

If every term is nonnegative and every weight is strictly positive, then

\[
\mathfrak F[U]=0
\quad\Longleftrightarrow\quad
\mathfrak F_a[U]=0
\quad\text{for all }a.
\]

This property prevents one condition from compensating numerically for a violation of another.

A functional that permits cancellations,

\[
\mathfrak F[U]
=
\mathfrak F_1[U]-\mathfrak F_2[U],
\]

would not, in general, encode simultaneous consistency. A zero could arise from two incompatible defects.

The nonnegativity requirement is therefore structural, not merely aesthetic.

### 3.4 Exact constraints versus penalty functions

A common mathematical temptation is to replace every constraint by a penalty term and then minimize the sum. This can be useful computationally, but it changes the problem unless the zero set is preserved.

Suppose

\[
\mathfrak F_\epsilon[U]
=
\sum_a w_a\|C_a[U]\|^2.
\]

A sequence \(U_n\) may satisfy

\[
\mathfrak F_\epsilon[U_n]\to0
\]

without converging to any model in the candidate space. This can occur when the space is noncompact or the constraint maps fail to be closed.

Consequently, the existence of approximate solutions does not prove the existence of an exactly admissible model.

A rigorous theory must distinguish:

\[
\mathscr U_{\mathrm{adm}}
=
\{U:\mathfrak F[U]=0\}
\]

from the approximate sublevel sets

\[
\mathscr U_{\epsilon}
=
\{U:\mathfrak F[U]\leq\epsilon\}.
\]

The latter are useful for effective theories and numerical investigations, but they do not replace the former.

### 3.5 The zero-set principle

**Definition 3.1 — Exact admissibility.**

A candidate model \(U\in\mathscr U_{\mathfrak C}\) is exactly admissible if and only if

\[
\mathfrak F[U]=0.
\]

**Definition 3.2 — Nontrivial admissibility.**

The admissible class is nontrivial if

\[
\mathscr U_{\mathrm{adm}}/\sim
\]

contains more than one equivalence class.

**Definition 3.3 — Structural restriction.**

A property \(P\) is an admissibility consequence in the model family \(\mathfrak C\) if

\[
\forall U\in\mathscr U_{\mathrm{adm}},
\qquad P(U).
\]

The third definition is the one most relevant to the theory's predictive ambitions. It identifies a property shared by every admissible model without assuming that all such models are identical.

---

## 4. The Admissibility Conditions

The consistency functional is only as meaningful as its components. Each condition must be defined in a way that is independent of the desired conclusion.

### 4.1 Mathematical well-definedness

A candidate model must possess a mathematically coherent formulation.

Depending on the theory, this can require:

- existence of the state space;
- appropriate operator domains;
- well-defined composition of dynamical maps;
- existence of the relevant observables;
- consistency of constraints;
- suitable regularity of fields or distributions;
- existence of a meaningful solution space.

For a quantum Hamiltonian \(H\), for example, one generally requires a self-adjoint realization on a specified Hilbert space:

\[
H=H^\dagger
\]

with the domain of \(H\) explicitly addressed.

A formal expression for \(H\) is not sufficient if it does not define a self-adjoint operator or an appropriate self-adjoint extension.

### 4.2 Dynamical stability

Stability is not one universal condition.

At least four notions must be distinguished.

**Energetic stability**

A Hamiltonian is bounded below:

\[
\inf\operatorname{spec}(H)>-\infty.
\]

**Spectral stability**

The linearized evolution has no forbidden exponentially growing modes.

**Lyapunov stability**

Small perturbations of a state remain controlled under evolution.

**Metastability**

A state may persist for a long time even when it is not the global ground state.

These notions are related but not interchangeable.

For a Hamiltonian theory, a bounded-below spectrum is often necessary for a stable equilibrium interpretation. It does not establish that every state is dynamically stable or that the system has a unique ground state.

The admissibility functional must specify which stability notion is required.

### 4.3 Symmetry consistency

Let \(G\) be a symmetry group with a representation \(U(g)\) on the relevant state space.

For an exact symmetry of the dynamics,

\[
U(g)HU(g)^{-1}=H,
\qquad g\in G.
\]

Equivalently,

\[
[H,U(g)]=0.
\]

For a continuous group with generators \(Q_a\),

\[
[H,Q_a]=0.
\]

The existence of a symmetry of the equations does not imply that the selected state preserves that symmetry. A ground state may break the symmetry spontaneously.

Therefore, one must distinguish:

1. symmetry of the model;
2. symmetry of the state;
3. symmetry of the observables;
4. symmetry of the effective low-energy description.

A classification theorem must state which of these is required.

### 4.4 Locality

Locality must be specified relative to an underlying structure.

For a lattice model, one may define locality through finite-range interactions or sufficiently rapid decay of interaction terms.

For a relativistic field theory, locality may be encoded by microcausality:

\[
[\mathcal O(x),\mathcal O(y)]=0
\]

for spacelike-separated points \(x\) and \(y\), for bosonic observables, with the corresponding graded relation for fermionic fields.

For a general quantum system, locality can instead be expressed through a net of local observable algebras.

These formulations are not identical. A theorem about finite-range lattice Hamiltonians cannot be applied to arbitrary nonlocal systems without a separate argument.

### 4.5 Quantum consistency

Quantum consistency can include several logically distinct conditions:

- positivity of states;
- positivity of expectation values;
- complete positivity of physical quantum channels;
- preservation of normalization;
- unitarity of closed-system evolution;
- compatibility of constraints and observables;
- consistency of superselection sectors;
- absence of specified gauge or gravitational anomalies.

For a density operator,

\[
\rho\geq0,
\qquad
\operatorname{Tr}\rho=1.
\]

For a quantum channel \(\mathcal E\),

\[
\mathcal E
\]

must be completely positive and trace-preserving when it represents deterministic evolution of a normalized state.

For a closed quantum system,

\[
\rho(t)=U(t)\rho(0)U(t)^\dagger,
\qquad
U(t)^\dagger U(t)=I.
\]

The phrase *quantum consistency* should never be used as a substitute for specifying which of these conditions is imposed.

### 4.6 Causal consistency

In relativistic settings, causal consistency may require that the dynamical structure respect an appropriate causal order.

For a Lorentzian spacetime \((M,g)\), the causal structure is determined by the light cones of \(g\). A local relativistic theory must specify how its fields and observables behave relative to that structure.

However, causal consistency is not equivalent to the absence of all correlations between spacelike-separated systems. Quantum entanglement provides correlations that cannot be represented by local hidden-variable models, while operational no-signalling remains compatible with relativistic causal constraints.

Thus the admissibility conditions must distinguish:

\[
\text{correlation}
\neq
\text{controllable causal influence}.
\]

A framework that treats every nonlocal correlation as a causal violation would incorrectly exclude ordinary quantum theory.

### 4.7 A controlled low-energy limit

A candidate theory intended to describe physical dynamics must often possess a meaningful effective description at accessible scales.

Let \(\Lambda\) denote an ultraviolet scale and \(\mu\) a lower energy scale. A coarse-graining or renormalization map may be represented schematically by

\[
\mathcal R_{\Lambda\to\mu}:U_\Lambda\longmapsto U_\mu.
\]

A controlled low-energy limit requires that the relevant observables and dynamics at scale \(\mu\) be well-defined and that the approximation errors be controlled.

The existence of a formal expansion is not sufficient. One must identify its regime of validity and the parameters governing corrections.

An effective field theory can be predictive without being fundamental. TAU therefore does not require every admissible candidate to be ultraviolet complete unless that requirement is explicitly included in the candidate class.

---

## 5. Logical Structure: Consistency, Existence, and Selection

### 5.1 The nonemptiness problem

Before classifying admissible models, one must establish that the admissible class is nonempty:

\[
\mathscr U_{\mathrm{adm}}\neq\varnothing.
\]

This is not automatic.

An inconsistent collection of requirements may imply

\[
\mathscr U_{\mathrm{adm}}=\varnothing.
\]

Such a result would not identify a universe. It would demonstrate that the candidate class or the imposed conditions are mutually incompatible.

The first theorem in any concrete TAU construction should therefore establish existence or prove a meaningful obstruction.

### 5.2 The uniqueness problem

Suppose

\[
\mathscr U_{\mathrm{adm}}\neq\varnothing.
\]

This does not imply

\[
|\mathscr U_{\mathrm{adm}}/\sim|=1.
\]

There may be infinitely many admissible models.

Three distinct classification outcomes are possible:

**Uniqueness**
\[
|\mathscr U_{\mathrm{adm}}/\sim|=1.
\]

**Finite classification**
\[
1<
|\mathscr U_{\mathrm{adm}}/\sim|
<\infty.
\]

**Infinite classification**
\[
|\mathscr U_{\mathrm{adm}}/\sim|=\infty.
\]

A fourth possibility is that the quotient has continuous moduli, so that the admissible theories form families parameterized by continuous data.

The existence of continuous moduli is particularly important for physical constants. If admissibility leaves a parameter \(\lambda\) free, then the theory has not derived its value.

### 5.3 Structural selection without uniqueness

The strongest useful result may be a theorem of the form

\[
\forall U\in\mathscr U_{\mathrm{adm}},
\qquad
P(U),
\]

where \(P\) is a nontrivial structural property.

For example, all admissible models in a defined class may be required to possess:

- a gapless excitation;
- a protected degeneracy;
- a conserved charge;
- a particular symmetry representation;
- a restricted scaling behavior;
- a specified class of low-energy effective descriptions.

This is structural selection without model uniqueness.

It is often more realistic and scientifically valuable than an attempt to derive every microscopic detail from general principles.

### 5.4 The danger of circular admissibility

A condition is circular if it is defined so that the desired conclusion is already contained in its premise.

For example, if one defines the admissible class to consist only of models with a particular low-energy spectrum, then proving that every admissible model has that spectrum establishes nothing.

The conditions must be independently motivated.

A useful audit question is:

> Could the condition have been proposed before knowing the low-energy conclusion that the theory is intended to derive?

If not, the classification may be tautological.

---

## 6. A Concrete Model Family: One-Dimensional Quantum Lattice Universes

A general theory of admissibility requires concrete examples in which its conditions can be formulated and tested. We now define a model family sufficiently restrictive to admit a nontrivial exclusion theorem.

### 6.1 The lattice model

Consider a one-dimensional periodic lattice with \(L\) sites. Each site has a finite-dimensional Hilbert space \(\mathcal H_j\), and the total Hilbert space is

\[
\mathcal H_L
=
\bigotimes_{j=1}^{L}\mathcal H_j.
\]

The Hamiltonian is

\[
H_L=\sum_{j=1}^{L}h_{j,j+1},
\]

with periodic identification \(L+1\equiv1\).

More generally, finite-range interactions may be included:

\[
H_L=\sum_{X\subset\Lambda_L}\Phi(X),
\]

where \(\Phi(X)\) vanishes whenever the diameter of \(X\) exceeds a fixed range \(R\), independent of \(L\).

We impose the following structural assumptions.

**A1 — Finite local dimension.**

\[
\dim\mathcal H_j<\infty.
\]

**A2 — Translation invariance.**

There exists a unitary translation operator \(T\) such that

\[
T H_L T^{-1}=H_L.
\]

**A3 — Conserved integer-valued charge.**

There exists a total charge

\[
Q_L=\sum_{j=1}^{L}q_j,
\]

where the local charges have integer eigenvalues, and

\[
[H_L,Q_L]=0.
\]

**A4 — Locality.**

The interactions have finite range or satisfy a sufficiently strong locality condition for the flux-insertion argument.

**A5 — Fixed filling.**

The charge sector is chosen so that

\[
\nu=\frac{Q_L}{L}
\]

approaches a fixed noninteger rational filling,

\[
\nu=\frac{p}{q},
\qquad
\gcd(p,q)=1,
\qquad
q>1,
\]

along a sequence of compatible system sizes.

**A6 — Exact \(U(1)\) symmetry.**

The Hamiltonian is invariant under

\[
U(\theta)=e^{i\theta Q_L}.
\]

These assumptions define a specific candidate family. They do not define every possible universe.

### 6.2 The low-energy question

The relevant question is whether a model satisfying A1–A6 can possess a ground state that is simultaneously:

1. unique;
2. gapped in the thermodynamic limit;
3. translation invariant;
4. \(U(1)\)-symmetric.

At first glance, these properties may seem mutually compatible. A local Hamiltonian can be bounded below, have exact symmetries, and possess a well-defined quantum evolution.

However, the joint constraints at fractional filling impose a stronger restriction.

The obstruction is a version of the Lieb–Schultz–Mattis theorem.

---

## 7. The Flux-Insertion Exclusion Theorem

### 7.1 Boundary twist

Introduce a \(U(1)\) flux \(\theta\) through the periodic ring.

For a charge-conserving hopping model, the flux can be introduced by twisting the boundary condition or, equivalently, by distributing a uniform gauge phase across the links.

For a general finite-range \(U(1)\)-invariant lattice Hamiltonian, the corresponding twist is implemented by coupling the local charge transport terms to a background \(U(1)\) gauge field.

Write the resulting Hamiltonian as

\[
H_L(\theta),
\qquad
0\leq\theta\leq2\pi.
\]

At zero flux,

\[
H_L(0)=H_L.
\]

At \(2\pi\) flux, the Hamiltonian is gauge-equivalent to the original Hamiltonian.

For a unique, gapped ground state maintained throughout the insertion, adiabatic evolution would transport the ground state into a ground state of \(H_L(2\pi)\).

The crucial point is that the final state need not have the same crystal momentum as the initial state.

### 7.2 Large gauge transformation

Define the unitary operator

\[
\mathcal U
=
\exp\left(
\frac{2\pi i}{L}
\sum_{j=1}^{L}j\,q_j
\right).
\]

This is the large gauge transformation that removes the \(2\pi\) flux.

Under translation, its transformation is

\[
T\mathcal U T^{-1}
=
\mathcal U
\exp\left(-\frac{2\pi i}{L}Q_L\right),
\]

up to a convention-dependent boundary factor that is trivial when the local charge eigenvalues are integers.

The sign of the exponent depends on the convention for translation and the direction of flux insertion. The momentum shift modulo \(2\pi\) is the invariant content.

If \(|\Psi_0\rangle\) is a translation eigenstate,

\[
T|\Psi_0\rangle=e^{iP_0}|\Psi_0\rangle,
\]

then the gauge-transformed state has momentum

\[
P_1
=
P_0+2\pi\nu
\pmod{2\pi},
\]

with the sign reversed under the opposite convention.

Since \(\nu=p/q\) is noninteger,

\[
2\pi\nu\not\equiv0\pmod{2\pi}.
\]

Thus the flux-transformed state lies in a different crystal-momentum sector.

### 7.3 Contradiction with a unique symmetric gapped ground state

Suppose the system had a unique ground state separated from all excitations by a nonzero gap in the thermodynamic limit, and suppose this state remained unique and gapped under the flux insertion.

Adiabatic insertion of \(2\pi\) flux would produce a ground state that, after applying the large gauge transformation, is a ground state of the original Hamiltonian.

But its momentum differs by

\[
\Delta P=2\pi\nu
\pmod{2\pi}.
\]

The original Hamiltonian is translation invariant, so momentum sectors are distinct symmetry sectors.

The transformed state is therefore orthogonal to the original state when the momentum difference is nonzero modulo \(2\pi\).

This contradicts uniqueness of the ground state.

The assumptions cannot all hold simultaneously.

### 7.4 Theorem

**Theorem 7.1 — Fractional-filling exclusion theorem (Lieb–Schultz–Mattis type).**

Let \(H_L\) be a sequence of one-dimensional, finite-range, translation-invariant quantum lattice Hamiltonians with finite-dimensional local Hilbert spaces and an exact conserved integer-valued \(U(1)\) charge \(Q_L\). Suppose the thermodynamic sequence has a fixed rational noninteger filling

\[
\nu=\frac{p}{q},
\qquad
\gcd(p,q)=1,
\qquad
q>1.
\]

Under the standard locality and flux-insertion regularity assumptions, the system cannot have a unique, translation-invariant, \(U(1)\)-symmetric ground state separated from all excitations by a nonzero thermodynamic spectral gap.

Equivalently, at least one of the following must occur:

1. the system is gapless;
2. translation symmetry is spontaneously broken;
3. the \(U(1)\) symmetry is spontaneously broken;
4. the ground-state structure is degenerate in a manner that invalidates the assumed uniqueness.

In the specified one-dimensional setting, the theorem excludes a unique, fully symmetric, gapped ground state at fractional filling.

**Proof.**

Assume, for contradiction, that the ground state is unique, symmetric, and separated by a nonzero gap that remains open during adiabatic flux insertion.

Insert \(2\pi\) flux through the ring. By the assumed gap and uniqueness, adiabatic evolution transports the ground state into a ground state of the flux-threaded Hamiltonian.

Apply the large gauge transformation \(\mathcal U\) to return to the original Hamiltonian. The transformed state is then a ground state of \(H_L(0)\).

Its translation eigenvalue differs from that of the original state by the phase

\[
e^{\pm2\pi i\nu}
=
e^{\pm2\pi ip/q}
\neq1.
\]

Therefore, the transformed state belongs to a distinct momentum sector and is orthogonal to the original state.

The original Hamiltonian consequently has at least two orthogonal ground states, contradicting uniqueness.

Hence the assumed combination of a unique, symmetric, gapped ground state is impossible. \(\square\)

### 7.5 Scope of the theorem

The theorem is an established Lieb–Schultz–Mattis-type obstruction, not a new theorem of quantum mechanics and not a proof of a universal law governing all possible universes.

Its value here is methodological.

It demonstrates that independently specified properties—locality, translation symmetry, conserved charge, and fractional filling—can jointly exclude an entire low-energy phase.

The exclusion does not depend on choosing a particular microscopic Hamiltonian. It holds across the defined family.

This is precisely the type of result that a theory of admissible models should seek.

---

## 8. Translating the Exclusion Result into the Admissibility Functional

### 8.1 Model-specific functional

For the lattice family, define a functional with components representing the imposed conditions:

\[
\begin{aligned}
\mathfrak F_{\mathrm{lat}}[U]
={}&
w_1\mathfrak F_{\mathrm{finite}}[U]
+w_2\mathfrak F_{\mathrm{local}}[U]\\
&+w_3\mathfrak F_{\mathrm{trans}}[U]
+w_4\mathfrak F_{U(1)}[U]\\
&+w_5\mathfrak F_{\mathrm{charge}}[U]
+w_6\mathfrak F_{\mathrm{fill}}[U].
\end{aligned}
\]

Each term is zero precisely when the corresponding assumption is satisfied.

For example, if \(T\) is the translation operator,

\[
\mathfrak F_{\mathrm{trans}}[U]
=
\|THT^{-1}-H\|^2.
\]

For charge conservation,

\[
\mathfrak F_{\mathrm{charge}}[U]
=
\|[H,Q]\|^2.
\]

The norms must be defined on the finite system or in an appropriate thermodynamic-limit topology.

Locality can be encoded by a finite-range condition or by a decay bound on the interaction norm. A hard finite-range condition is more naturally represented by an indicator functional than by an arbitrary numerical penalty.

### 8.2 The target phase as an additional constraint

Let \(\mathscr U_{\mathrm{triv}}\) denote the subset of models with:

- a unique ground state;
- a nonzero thermodynamic spectral gap;
- unbroken translation symmetry;
- unbroken \(U(1)\) symmetry.

The exclusion theorem establishes

\[
\boxed{
\mathscr U_{\mathrm{adm}}
\cap
\mathscr U_{\mathrm{triv}}
=
\varnothing
}
\]

for the fractional-filling model family and the stated assumptions.

This is a classification statement.

It does not establish that every admissible model is gapless. Some admissible models may be gapped with symmetry breaking or ground-state degeneracy. Others may be gapless and preserve the full symmetry.

### 8.3 The classification is not a unique selection

The theorem gives an exclusion, not a unique Hamiltonian.

The admissible class may contain many inequivalent models:

\[
|\mathscr U_{\mathrm{adm}}/\sim|>1.
\]

The theorem restricts the allowed low-energy structures but does not determine all coupling constants, excitation spectra, or microscopic interactions.

This distinction is central to TAU.

A successful admissibility theory need not select a unique universe to produce meaningful physical consequences. It must, however, derive restrictions that are not already assumed in the definition of admissibility.

---

## 9. Anomaly Interpretation

### 9.1 Symmetry and obstruction

The flux-insertion argument has a deeper interpretation in terms of an obstruction between symmetry, locality, and the assumed infrared phase.

At fractional filling, the microscopic symmetry structure cannot be represented by a unique, symmetric, short-range-entangled, gapped ground state under the theorem's assumptions.

This is often described as a Lieb–Schultz–Mattis anomaly or an anomaly-matching constraint.

The word *anomaly* here does not mean that the microscopic model is inconsistent. Rather, it means that the symmetry and filling data obstruct a particular type of low-energy realization.

### 9.2 Ultraviolet data constrain infrared structure

The important structural implication is that certain microscopic data constrain the possible low-energy theories.

Schematically,

\[
\text{microscopic symmetry data}
+
\text{filling}
+
\text{locality}
\Longrightarrow
\text{infrared obstruction}.
\]

This is an especially promising pattern for TAU.

It shows how consistency conditions can impose low-energy restrictions without specifying a unique microscopic Hamiltonian.

### 9.3 Generalization beyond the lattice example

Related anomaly constraints appear in:

- quantum field theories with global symmetries;
- gauge theories;
- topological phases of matter;
- systems with projective symmetry representations;
- higher-dimensional lattice models;
- theories with mixed anomalies.

However, each setting has its own assumptions and mathematical formulation. The one-dimensional flux-insertion theorem cannot simply be generalized by replacing the lattice with an arbitrary spacetime manifold.

A broader TAU classification would need a systematic treatment of symmetry groups, representations, anomalies, and the allowed infrared realizations.

---

## 10. From Exclusion to Low-Energy Classification

### 10.1 The admissible infrared set

Let \(\mathscr I(U)\) denote the low-energy structure associated with a candidate model \(U\).

This might include:

- the effective field content;
- the symmetry realization;
- the spectrum of gapless excitations;
- the scaling dimensions of operators;
- the renormalization-group fixed point;
- topological response data;
- protected degeneracies.

The induced infrared classification is

\[
\mathscr I_{\mathrm{adm}}
=
\{\mathscr I(U):U\in\mathscr U_{\mathrm{adm}}\}.
\]

The objective is to determine whether

\[
\mathscr I_{\mathrm{adm}}
\subsetneq
\mathscr I(\mathscr U_{\mathfrak C}),
\]

that is, whether admissibility excludes some otherwise mathematically definable infrared structures.

The lattice theorem supplies an explicit example of such a strict restriction.

### 10.2 Universality classes

Different microscopic Hamiltonians may flow to the same low-energy fixed point.

Let

\[
U_1\sim_{\mathrm{IR}}U_2
\]

if their long-distance behavior is described by the same universality class, according to a specified set of observables and scaling data.

The admissible infrared quotient is

\[
\mathscr I_{\mathrm{adm}}/\sim_{\mathrm{IR}}.
\]

A particularly strong result would show that this quotient contains only a small number of universality classes, even when the microscopic admissible class is large.

That would constitute structural selection at the effective level.

### 10.3 Renormalization-group formulation

Let \(g=(g_1,\ldots,g_n)\) denote effective couplings. A renormalization-group flow is represented schematically by

\[
\frac{dg_i}{d\ell}
=
\beta_i(g).
\]

A fixed point satisfies

\[
\beta_i(g_*)=0.
\]

The admissibility problem can then be recast as a restriction on allowed fixed points:

\[
g_*\in\mathscr G_{\mathrm{adm}}
\subseteq
\mathscr G_{\mathrm{all}}.
\]

The question becomes whether consistency conditions eliminate certain fixed points or require certain relevant operators, conserved quantities, or scaling relations.

This is a natural bridge between model classification and effective physical structure.

However, an RG fixed point is not automatically a physically admissible universe. Its existence must be supplemented by a valid microscopic completion or an explicitly stated effective-theory interpretation.

---

## 11. Stability and the Geometry of the Admissible Set

### 11.1 Why existence is insufficient

A model may satisfy exact constraints but be unstable under arbitrarily small perturbations.

If the goal is to identify physically robust structures, admissibility should be supplemented by a stability notion.

Let \(d_{\mathscr U}\) be a metric or topology on the model space. For an admissible model \(U\), define its perturbation neighborhood

\[
B_\epsilon(U)
=
\{V\in\mathscr U_{\mathfrak C}:d_{\mathscr U}(U,V)<\epsilon\}.
\]

One can ask whether nearby models remain admissible, or whether a physically meaningful deformation preserves the relevant low-energy properties.

Exact symmetry constraints are often not stable under arbitrary perturbations. The appropriate question is therefore stability within the symmetry-preserving subspace or under a specified class of perturbations.

### 11.2 Structural stability

Let \(P\) be a property of the low-energy theory.

A model \(U\) is structurally stable with respect to \(P\) if there exists \(\epsilon>0\) such that

\[
d_{\mathscr U}(U,V)<\epsilon,
\quad
V\in\mathscr U_{\mathrm{adm}},
\]

implies

\[
P(V)=P(U).
\]

This definition must be adapted if \(P\) is continuous rather than discrete.

For instance, a spectral gap may vary continuously while remaining nonzero, whereas a topological invariant may remain exactly quantized within a gapped phase.

### 11.3 Robust admissibility

A stronger condition is that the admissible structure persists under a specified family of perturbations:

\[
\mathscr P\subset\operatorname{End}(\mathscr U_{\mathfrak C}),
\]

where each \(p\in\mathscr P\) is an allowed deformation.

One can define

\[
\mathscr U_{\mathrm{rob}}
=
\left\{
U\in\mathscr U_{\mathrm{adm}}:
P(pU)=P(U)
\text{ for all permitted }p
\right\}.
\]

This is a conditional definition: the physical significance depends on the perturbation class.

Robustness should not be imposed as a vague universal requirement. It must be tied to physically relevant deformations.

### 11.4 Topology of the admissible class

If the model space carries a suitable topology, the admissible set may have meaningful geometric properties:

- connected components;
- singular strata;
- isolated solutions;
- continuous moduli;
- boundary points;
- bifurcation loci.

A classification theorem could determine the topology of

\[
\mathscr U_{\mathrm{adm}}/\sim.
\]

Such a result would be stronger than merely finding individual solutions.

But the topology of the model space is itself part of the mathematical setup. It cannot be presumed without specifying the model category and the convergence notion.

---

## 12. Symmetry as a Restriction on Admissible Models

### 12.1 Symmetry groups as classification data

A symmetry group does not uniquely determine dynamics, but it constrains the form of allowed interactions.

If a group \(G\) acts on the state space, the admissible Hamiltonians lie in the commutant of that representation:

\[
H\in\operatorname{Comm}(G)
=
\{A:[A,U(g)]=0,\ \forall g\in G\}.
\]

This can substantially reduce the number of independent couplings.

The amount of reduction depends on the representation and the operator content.

### 12.2 Symmetry representations

For a state space decomposing into irreducible representations,

\[
\mathcal H
=
\bigoplus_\lambda
\mathcal H_\lambda\otimes\mathbb C^{m_\lambda},
\]

an operator commuting with the group action has a constrained block structure.

In finite dimensions, Schur's lemma implies that on an irreducible representation an operator commuting with the full group action is proportional to the identity, with additional freedom possible on multiplicity spaces.

Thus symmetry can constrain the operator algebra.

It does not, by itself, determine the coefficients of all allowed terms.

### 12.3 Symmetry breaking

The classification must include both symmetric and symmetry-broken phases unless symmetry preservation is explicitly part of the target class.

A theory that excludes all symmetry-broken states merely because the equations possess a symmetry would discard familiar and physically relevant phases.

The correct distinction is between:

\[
\text{symmetry of the laws}
\quad\text{and}\quad
\text{symmetry of the state}.
\]

### 12.4 Gauge redundancy

Gauge transformations require special care. They are not ordinary global symmetries acting on physically distinct states in the same way.

Gauge-related configurations generally represent redundant descriptions of the same physical state. Therefore, they should be quotiented or treated through an appropriate constrained formalism.

A gauge anomaly, by contrast, can obstruct the consistency of the quantum theory itself.

TAU must not confuse gauge redundancy, global symmetry, and anomalous symmetry realization.

---

## 13. Quantum Consistency and Positivity

### 13.1 Positivity as a structural constraint

Quantum theory imposes strong positivity conditions.

For every physical state \(\omega\) and positive observable \(A\),

\[
\omega(A)\geq0.
\]

For a density matrix,

\[
\rho\geq0.
\]

For a quantum channel, complete positivity is required to ensure that positivity is preserved even when the system is extended by an arbitrary ancillary space.

If

\[
\mathcal E:\mathcal B(\mathcal H_A)\to
\mathcal B(\mathcal H_B),
\]

then complete positivity means

\[
(\operatorname{id}_R\otimes\mathcal E)(X)\geq0
\]

for every finite ancillary system \(R\) and every \(X\geq0\).

This is stronger than positivity on the system alone.

### 13.2 Why positivity can constrain interactions

In field theory, positivity of spectral densities, norm positivity, and analyticity can restrict scattering amplitudes and effective interaction coefficients.

For example, under specified assumptions of unitarity, analyticity, crossing symmetry, and suitable high-energy boundedness, dispersion relations can imply positivity bounds on certain Wilson coefficients.

Such results provide a natural application of TAU:

\[
\text{unitarity}
+
\text{analyticity}
+
\text{causal assumptions}
\Longrightarrow
\text{restrictions on effective couplings}.
\]

The exact assumptions are essential. Positivity bounds do not follow from an informal appeal to consistency.

### 13.3 The limits of the quantum-consistency principle

Not every quantum theory admits the same simple Hilbert-space formulation. Gauge constraints, infrared sectors, quantum field theory in curved spacetime, and algebraic quantum field theory require more careful constructions.

A general admissibility theory must accommodate these distinctions rather than impose one finite-dimensional quantum formalism universally.

---

## 14. Locality, Causality, and the Structure of Dynamics

### 14.1 Locality as a quantitative condition

For a lattice system, one can impose a bound on interaction terms such as

\[
\|\Phi(X)\|
\leq
C e^{-\operatorname{diam}(X)/\xi},
\]

where \(C\) and \(\xi\) are finite constants.

Finite-range interactions are a special case.

For such systems, Lieb–Robinson bounds provide an effective finite propagation speed for the influence of local perturbations.

A representative form is

\[
\|[A_X(t),B_Y]\|
\leq
C'\|A_X\|\|B_Y\|
e^{-\mu(d(X,Y)-v_{\mathrm{LR}}|t|)}.
\]

This is not an exact relativistic light cone. It is a bound on the propagation of commutators in a local lattice model.

### 14.2 Locality can imply emergent causal structure

In suitable many-body systems, locality constrains how quickly information and perturbations can spread.

This provides a possible route toward effective causal structure.

However, deriving a Lorentzian spacetime metric from locality alone is a much stronger task. A Lieb–Robinson velocity is not automatically the physical speed of light, and a lattice metric is not automatically a spacetime metric.

Any such identification would require an additional derivation.

### 14.3 Nonlocal theories

TAU should not define all nonlocal models as inadmissible by default.

A nonlocal model may be mathematically consistent and physically meaningful in an appropriate regime. The question is whether it satisfies the specific causal, operational, and stability requirements of the intended application.

The model family must therefore specify the locality class being studied.

---

## 15. A General Classification Program

### 15.1 The classification map

For a specified candidate family \(\mathfrak C\), define the classification map

\[
\Pi:
\mathscr U_{\mathfrak C}
\longrightarrow
\mathscr K,
\]

where \(\mathscr K\) is a space of structural invariants.

Possible invariants include:

- symmetry representations;
- anomaly classes;
- spectral gaps;
- topological indices;
- renormalization-group fixed points;
- scaling dimensions;
- causal-cone structures;
- algebraic relations among observables.

The admissible classification is

\[
\Pi(\mathscr U_{\mathrm{adm}}).
\]

The goal is to determine this image, not merely to exhibit a few admissible examples.

### 15.2 Existence, exclusion, and completeness

A complete classification program has three stages.

**Existence theorem**

Prove that at least one admissible model exists.

**Exclusion theorem**

Prove that a specified structural class cannot be admissible.

**Completeness theorem**

Prove that all remaining admissible models belong to the listed classes, up to the declared equivalence relation.

The exclusion theorem in Section 7 is an example of the second stage.

A complete TAU result would need all three stages for a chosen model family.

### 15.3 Classification by invariants

Suppose a set of invariants

\[
I(U)=\big(I_1(U),\ldots,I_m(U)\big)
\]

is constant under the equivalence relation.

If the invariants are complete, then

\[
I(U)=I(V)
\quad\Longleftrightarrow\quad
U\sim V.
\]

Completeness is difficult. A collection of invariants may distinguish many models while failing to distinguish all inequivalent ones.

A classification theorem must state whether the invariants are complete or merely necessary descriptors.

### 15.4 The admissibility hierarchy

A practical hierarchy of results is:

| Level | Mathematical result | What it establishes |
|---|---|---|
| I | Well-definedness | The candidate model exists mathematically |
| II | Consistency | The specified constraints are satisfied |
| III | Stability | The relevant dynamics or states are stable |
| IV | Exclusion | A defined class of structures is impossible |
| V | Classification | All admissible models in the family are characterized |
| VI | Low-energy restriction | Admissibility forces a restricted infrared structure |
| VII | Quantitative prediction | The framework determines a measurable value or relation |
| VIII | Empirical validation | The predicted structure is supported by observation |

A result at one level should not be presented as if it establishes a higher level.

---

## 16. Can Admissibility Determine Physical Constants?

### 16.1 The parameter problem

Suppose a candidate model contains parameters

\[
\lambda=(\lambda_1,\ldots,\lambda_n).
\]

The consistency conditions define equations

\[
C_a(\lambda)=0.
\]

Collectively,

\[
C(\lambda)=0.
\]

If the Jacobian

\[
J_{ai}
=
\frac{\partial C_a}{\partial\lambda_i}
\]

has rank \(r\) at a regular solution, then the local solution set has dimension

\[
n-r.
\]

Thus, if \(r<n\), continuous parameter freedom generally remains.

This is a basic but important obstruction to deriving physical constants from consistency.

### 16.2 Necessary conditions for parameter selection

To determine a parameter uniquely, one needs enough independent constraints to eliminate the corresponding freedom, together with conditions ensuring that the solution is isolated and physically meaningful.

Even if the solution is isolated, uniqueness does not follow globally without ruling out other disconnected solutions.

A parameter derivation should therefore establish:

1. the complete constraint system;
2. independence or rank of the constraints;
3. existence of a solution;
4. isolation of the solution;
5. uniqueness within the stated domain;
6. stability of the solution under allowed changes in formulation;
7. an observable consequence.

### 16.3 Why minimizing the consistency functional is not enough

One might attempt to select a universe by minimizing

\[
\mathfrak F[U].
\]

But if admissible models satisfy

\[
\mathfrak F[U]=0,
\]

then every admissible model is already a global minimizer.

The functional cannot distinguish among its zeroes.

One could introduce a second functional,

\[
\mathfrak S[U],
\]

and select a minimizer over the admissible set:

\[
U_*
\in
\operatorname*{arg\,min}_{U\in\mathscr U_{\mathrm{adm}}}
\mathfrak S[U].
\]

But this introduces a new selection principle. Its physical justification must be independent.

It is not legitimate to claim that consistency selected \(U_*\) when the selection was actually performed by \(\mathfrak S\).

### 16.4 The selection problem as a hierarchy

A more honest formulation is:

\[
\text{candidate models}
\longrightarrow
\text{consistent models}
\longrightarrow
\text{stable models}
\longrightarrow
\text{empirically viable models}.
\]

A further selection mechanism may exist, but it must be separately established.

---

## 17. The Relation to Existing Physical Frameworks

TAU is not introduced in a conceptual vacuum. Several established areas already perform parts of the classification problem.

### 17.1 Effective field theory

Effective field theory classifies interactions compatible with a chosen set of degrees of freedom, symmetries, and scale assumptions.

Its strength is controlled low-energy prediction.

Its limitation for the present program is that the degrees of freedom and much of the symmetry structure are usually supplied at the beginning.

TAU asks whether some of these structural inputs can themselves be restricted by broader admissibility requirements.

### 17.2 The S-matrix bootstrap

The S-matrix bootstrap constrains scattering amplitudes through principles such as unitarity, analyticity, crossing symmetry, and locality assumptions.

It is a close methodological relative of TAU because it attempts to constrain physical theories from consistency requirements rather than from a fully specified Lagrangian.

However, the bootstrap is formulated for particular scattering settings and assumptions. Its results do not automatically classify all possible universes.

### 17.3 Anomaly matching

Anomaly matching constrains the possible infrared realization of microscopic symmetries.

The fractional-filling theorem developed above is an example of this general pattern.

This is one of the strongest existing sources of structural restrictions for a theory of admissible models.

### 17.4 Renormalization-group classification

Renormalization-group methods classify fixed points and the deformations that flow toward or away from them.

They provide the mathematical language for universality classes.

TAU can use these methods to ask which fixed points are compatible with a specified set of ultraviolet consistency conditions.

### 17.5 Quantum information constraints

Positivity, complete positivity, entanglement constraints, and information-theoretic inequalities can restrict the possible structure of quantum dynamics.

However, the existence of a quantum-information inequality does not automatically establish a spacetime or cosmological principle.

The relevant model category and physical interpretation must be supplied.

### 17.6 The distinctive objective of TAU

The distinctive ambition is to place these partial classification mechanisms within a common framework:

\[
\boxed{
\text{Model space}
+
\text{independent constraints}
+
\text{equivalence}
+
\text{classification}
}
\]

The framework is not a replacement for effective field theory, bootstrap methods, anomaly analysis, or renormalization-group theory.

It is a proposed organizing program for asking whether their constraints, when formulated within a common candidate family, imply broader structural restrictions.

Its novelty would have to reside in new classification theorems or a genuinely new synthesis that produces results unavailable from the existing methods.

---

## 18. A General Theorem Schema for Admissible Universes

The lattice theorem suggests a general pattern.

Let \(\mathfrak C\) be a specified class of candidate models. Let

\[
C_1,\ldots,C_n
\]

be independent constraints, and let

\[
P_1,\ldots,P_m
\]

be proposed structural properties.

The admissible class is

\[
\mathscr U_{\mathrm{adm}}
=
\{U\in\mathfrak C:C_a(U)=0,\ a=1,\ldots,n\}.
\]

A classification theorem would establish

\[
\mathscr U_{\mathrm{adm}}/\sim
=
\bigcup_{\alpha\in A}\mathscr U_\alpha,
\]

where the \(\mathscr U_\alpha\) are explicitly characterized equivalence classes or families.

An exclusion theorem would establish

\[
\mathscr U_{\mathrm{adm}}
\cap
\mathscr K
=
\varnothing
\]

for a forbidden class \(\mathscr K\).

A structural consequence theorem would establish

\[
\forall U\in\mathscr U_{\mathrm{adm}},
\qquad
P(U).
\]

A predictive theorem would go further and establish

\[
\mathcal O(U)=\mathcal O_*
\]

or a bounded relation

\[
\mathcal O(U)\in\mathcal R
\]

for an observable \(\mathcal O\), with \(\mathcal O_*\) or \(\mathcal R\) determined independently of the data used to fit the model.

These theorem forms should be regarded as the central mathematical targets of TAU.

---

## 19. Failure Modes and No-Go Conditions

### 19.1 Empty admissible set

If the conditions are mutually inconsistent,

\[
\mathscr U_{\mathrm{adm}}=\varnothing.
\]

This may indicate that the candidate family is too restrictive, that a condition has been incorrectly formulated, or that the intended physical interpretation is incompatible with the assumptions.

### 19.2 Trivial admissibility

If every candidate satisfies the functional,

\[
\mathfrak F[U]=0
\quad\forall U\in\mathscr U_{\mathfrak C},
\]

then admissibility imposes no restriction.

### 19.3 Tautological admissibility

If the functional is constructed from the desired conclusion itself, the classification is circular.

### 19.4 Representation dependence

If the result changes under a physically harmless reparameterization, the classification may be describing the formal representation rather than the model.

### 19.5 Hidden selection assumptions

A supposedly unique result may depend on an unacknowledged minimization rule, measure, prior, boundary condition, or regularization prescription.

Each must be identified explicitly.

### 19.6 Excessive universality

A theorem proved for one model family cannot be elevated to a statement about all physical theories without a separate universality argument.

### 19.7 Underdetermined parameters

A nonempty admissible set may retain continuous moduli. These must be reported rather than assigned arbitrary preferred values.

### 19.8 Approximate consistency mistaken for exact consistency

A numerical solution with small residuals is not necessarily an exact solution. The stability of the numerical approximation and the existence of a true limiting model must be established.

---

## 20. Falsifiability and Empirical Contact

### 20.1 Mathematical falsifiability

A classification framework is mathematically falsifiable if it makes claims that can be contradicted by a counterexample.

For a theorem asserting

\[
\mathscr U_{\mathrm{adm}}\cap\mathscr K=\varnothing,
\]

a single valid model in the intersection would disprove the theorem or demonstrate that one of its assumptions was not satisfied.

The assumptions must be sufficiently explicit to identify which possibility occurred.

### 20.2 Physical falsifiability

A general mathematical classification does not automatically make a prediction about our universe.

Physical falsifiability requires a bridge between the candidate model family and measurable observables.

For example, if admissibility requires a certain symmetry realization or excludes a class of infrared phases, then an observed system violating the derived restriction could falsify the proposed application.

The interpretation must be specific enough that the experiment tests the actual theorem assumptions.

### 20.3 A prospective experimental program

The following are possible research directions, not predictions already derived by the general framework.

**A. Symmetry and filling constraints in quantum simulators**

Construct one-dimensional systems with controlled fractional filling and test the alternatives required by the Lieb–Schultz–Mattis obstruction: gaplessness, symmetry breaking, or ground-state degeneracy.

**B. Positivity bounds in scattering experiments**

Compare measured or bounded effective interactions with positivity constraints derived under explicit analyticity and unitarity assumptions.

**C. Infrared universality in programmable quantum systems**

Vary microscopic Hamiltonian parameters while preserving selected symmetries and locality conditions. Test whether the resulting low-energy behavior remains within the predicted admissible universality classes.

**D. Stability of emergent phases**

Introduce controlled symmetry-preserving perturbations and determine whether the predicted protected properties remain stable.

**E. Anomaly-sensitive phase transitions**

Investigate whether observed phase transitions are consistent with the anomaly constraints associated with the microscopic symmetry data.

These experiments test specific model families and theorems. They do not directly test a universal consistency functional over all conceivable universes.

---

## 21. Research Program

The theory should be developed through a sequence of increasingly ambitious classification problems.

### Phase I — Formal foundations

1. Specify the mathematical categories of candidate models.
2. Define physically meaningful equivalence relations.
3. Construct exact nonnegative consistency functionals.
4. Distinguish exact and approximate admissibility.
5. Establish existence and nonemptiness criteria.

### Phase II — Model-family classification

1. Finite-dimensional quantum systems.
2. Local quantum lattice systems.
3. Quantum field theories with global symmetries.
4. Gauge theories and anomaly constraints.
5. Effective field theories with controlled ultraviolet assumptions.
6. Classical Hamiltonian and field-theoretic systems.

Each family requires its own definitions and theorems.

### Phase III — Structural restrictions

1. Identify constraints that independently restrict the infrared spectrum.
2. Determine which symmetries can be realized in unique gapped phases.
3. Classify allowed topological and gapless phases.
4. Establish stability under specified perturbations.
5. Determine whether admissibility restricts the relevant operators and universality classes.

### Phase IV — Quantitative selection

1. Identify continuous moduli in the admissible class.
2. Determine whether additional independent constraints eliminate them.
3. Derive isolated solutions where possible.
4. Establish bounds on observables.
5. Separate derived values from fitted parameters.

### Phase V — Physical application

1. Identify a concrete physical system or cosmological model family.
2. Define the observable map.
3. Derive a falsifiable consequence.
4. Compare with independent measurements.
5. Revise or reject the admissibility assumptions when contradicted.

---

## 22. Open Mathematical Problems

The following problems define the principal research agenda.

**Problem 1 — General existence criterion.**

Under what conditions on the candidate model space and the constraint maps does

\[
\mathscr U_{\mathrm{adm}}\neq\varnothing
\]

follow?

For infinite-dimensional model spaces, compactness, weak lower semicontinuity, and coercivity may be relevant. Their applicability must be demonstrated for the chosen model category.

**Problem 2 — Completeness of admissibility invariants.**

Can one construct a complete set of invariants for a nontrivial family of local quantum theories, up to a physically justified equivalence relation?

**Problem 3 — Constraint independence.**

Given constraints \(C_a\), when are they genuinely independent rather than redundant consequences of one another?

A differential-rank test can help near regular finite-dimensional solutions, but infinite-dimensional and singular cases require more general tools.

**Problem 4 — Infrared classification.**

Which ultraviolet symmetry, locality, and quantum-consistency conditions force a finite or restricted set of infrared universality classes?

**Problem 5 — Robust admissibility.**

When do structural consequences persist under all perturbations in a physically meaningful class?

**Problem 6 — Quantitative parameter determination.**

Can independent consistency constraints determine a dimensionless coupling or observable relation without fitting it to the value being predicted?

**Problem 7 — Cross-category equivalence.**

Can a classical, quantum, and effective description be shown to represent the same admissible physical structure under a precisely defined correspondence?

**Problem 8 — Cosmological candidate spaces.**

Can the admissibility program be applied to cosmological models without assuming the spacetime dimension, matter content, or gravitational equations that the program is intended to constrain?

This final problem is especially difficult. It requires a mathematically defined candidate space broad enough to permit genuine alternatives while still supporting meaningful notions of locality, stability, and observables.

---

## 23. Limitations and Epistemic Status

The present framework contains results of different logical strengths.

### 23.1 Established mathematical and physical structures

The following are established components of the mathematical physics literature:

- self-adjointness and spectral conditions for quantum Hamiltonians;
- symmetry representations and commutant structures;
- complete positivity of quantum channels;
- locality conditions and Lieb–Robinson bounds;
- renormalization-group fixed-point methods;
- the Lieb–Schultz–Mattis obstruction and its extensions;
- anomaly constraints on infrared realizations;
- positivity bounds under specified scattering assumptions.

TAU does not claim to have originated these results.

### 23.2 Formal definitions introduced here

The candidate model space, quotient by physical equivalence, admissibility functional, and hierarchy of classification results provide a common formal architecture for the proposed theory.

These definitions are not, by themselves, physical discoveries.

Their value depends on whether they facilitate new theorems or clarify relations among existing ones.

### 23.3 Derived result

The principal concrete result is the application of the fractional-filling Lieb–Schultz–Mattis obstruction to the admissibility framework:

\[
\mathscr U_{\mathrm{adm}}
\cap
\mathscr U_{\mathrm{triv}}
=
\varnothing
\]

for the specified one-dimensional quantum lattice family.

This is a rigorous exclusion statement under the theorem's assumptions.

It demonstrates structural restriction without unique model selection.

### 23.4 Conjectural research direction

The broader conjecture is that sufficiently restrictive combinations of locality, symmetry, stability, and quantum consistency may constrain the low-energy structure of substantially broader model families.

This remains a research hypothesis.

No general theorem currently follows from the abstract definition of \(\mathfrak F\) alone.

### 23.5 The principal unresolved obstacle

The deepest difficulty is not defining a functional that vanishes on a desired class of models.

It is constructing conditions that are simultaneously:

1. mathematically precise;
2. physically motivated;
3. independent of the desired conclusion;
4. stable under legitimate changes of representation;
5. strong enough to exclude nontrivial alternatives;
6. broad enough to retain physically relevant models.

The theory succeeds only to the extent that it meets these requirements in concrete model families.

---

## 24. Conclusion

The Theory of Admissible Universes formulates a classification problem for physical law.

Its starting point is a structured space of candidate models,

\[
\mathscr U_{\mathfrak C},
\]

together with a nonnegative consistency functional,

\[
\mathfrak F:\mathscr U_{\mathfrak C}\to[0,\infty].
\]

The admissible class is

\[
\boxed{
\mathscr U_{\mathrm{adm}}
=
\{U\in\mathscr U_{\mathfrak C}:
\mathfrak F[U]=0\}.
}
\]

The fundamental objective is not to assume that this class contains one preferred universe. It is to determine its mathematical structure and establish which physical properties are shared by all of its members.

The fractional-filling quantum lattice example demonstrates the program in a concrete setting. Locality, translation symmetry, conserved \(U(1)\) charge, and noninteger filling jointly exclude a unique, symmetric, gapped ground state. The theorem does not select a unique Hamiltonian. It restricts the admissible low-energy possibilities.

This distinction defines the central epistemic discipline of the theory:

\[
\boxed{
\text{Consistency can exclude; classification can restrict; uniqueness requires proof.}
}
\]

A universal theory of admissible universes would need to go much further. It would have to define candidate structures broad enough to include genuine alternatives, formulate independent and physically justified consistency conditions, and prove that these conditions constrain the allowed infrared physics.

The most promising route is not an immediate attempt to derive every law or constant of nature. It is a sequence of rigorous classification theorems, each demonstrating that a precisely specified set of physical requirements excludes a precisely specified class of alternatives.

If these results accumulate into a coherent and representation-independent structure, then admissibility may become more than a criterion for rejecting inconsistent models. It may become a mathematical route toward understanding why the space of physically possible laws is narrower than the space of mathematically writable ones.

The theory's ultimate success will be measured not by the breadth of its philosophical claim, but by the strength, completeness, and empirical relevance of the classification theorems it can establish.

---

## References

1. Lieb, E. H., Schultz, T., and Mattis, D. C. (1961). “Two Soluble Models of an Antiferromagnetic Chain.” *Annals of Physics* **16**, 407–466.
2. Affleck, I. (1986). “The Quantum Hall Effect, \(\sigma\)-Models at \(\theta=\pi\) and Quantum Spin Chains.” *Nuclear Physics B* **257**, 397–406.
3. Oshikawa, M. (2000). “Commensurability, Excitation Gap, and Topology in Quantum Many-Particle Systems on a Periodic Lattice.” *Physical Review Letters* **84**, 1535–1538.
4. Hastings, M. B. (2004). “Lieb-Schultz-Mattis in Higher Dimensions.” *Physical Review B* **69**, 104431.
5. Lieb, E. H., and Robinson, D. W. (1972). “The Finite Group Velocity of Quantum Spin Systems.” *Communications in Mathematical Physics* **28**, 251–257.
6. Bravyi, S., Hastings, M. B., and Verstraete, F. (2006). “Lieb-Robinson Bounds and the Generation of Correlations and Topological Quantum Order.” *Physical Review Letters* **97**, 050401.
7. Wilson, K. G., and Kogut, J. (1974). “The Renormalization Group and the \(\epsilon\) Expansion.” *Physics Reports* **12**, 75–199.
8. Polchinski, J. (1984). “Renormalization and Effective Lagrangians.” *Nuclear Physics B* **231**, 269–295.
9. Weinberg, S. (1979). “Phenomenological Lagrangians.” *Physica A* **96**, 327–340.
10. Witten, E. (1982). “An SU(2) Anomaly.” *Physics Letters B* **117**, 324–328.
11. ’t Hooft, G. (1980). “Naturalness, Chiral Symmetry, and Spontaneous Chiral Symmetry Breaking.” In *Recent Developments in Gauge Theories*, Plenum Press.
12. Seiberg, N. (2010). “The Power of Holomorphy: Exact Results in 4D SUSY Field Theory.” In *Theoretical Advanced Study Institute in Elementary Particle Physics*.
13. Adams, A., Arkani-Hamed, N., Dubovsky, S., Nicolis, A., and Rattazzi, R. (2006). “Causality, Analyticity and an IR Obstruction to UV Completion.” *Journal of High Energy Physics* **10**, 014.
14. Komargodski, Z., and Schwimmer, A. (2011). “On Renormalization Group Flows in Four Dimensions.” *Journal of High Energy Physics* **12**, 099.
15. Aharony, O., Bergman, O., Jafferis, D. L., and Maldacena, J. (2008). “\( \mathcal N=6 \) Superconformal Chern–Simons-Matter Theories, M2-Branes and Their Gravity Duals.” *Journal of High Energy Physics* **10**, 091.


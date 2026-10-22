The Arithmetic of Black-Hole Microstates

Exact State Counting, Modular Structures, and the Asymptotic Reconstruction of Black-Hole Entropy

Research preprint · October 22, 2026

Abstract

The Bekenstein–Hawking entropy formula,

S_{\mathrm{BH}}

\frac{k_Bc^3A}{4G\hbar},

relates the entropy of a black hole to the area of its horizon. Its simplicity conceals a fundamental microscopic question: what precisely is being counted, and why should the logarithm of that count scale as one quarter of the horizon area in Planck units?

This paper develops the Arithmetic of Black-Hole Microstates (ABHM) as a mathematical research program for constructing microscopic state-counting models whose exact degeneracies possess arithmetic structure and whose asymptotics reproduce a specified black-hole entropy formula. The central hypothesis is that, in suitable quantum-gravitational models, the degeneracies of states at fixed conserved charges may be encoded by generating functions with integer coefficients, modular or automorphic transformation properties, and coefficient asymptotics governed by singularities or saddle points.

The paper constructs a precise model architecture based on a graded microscopic state space, an independently defined Hamiltonian or charge operator, a microcanonical degeneracy function, and a partition-generating function. It then develops a conditional theorem connecting a coefficient asymptotic of the form

\log d(N)

\alpha\sqrt{N}
+\beta\log N
+\gamma+o(1)

to a specified entropy law under an independently defined relation between the charge label and the macroscopic horizon area. A second construction shows how a Cardy-type asymptotic can reproduce a leading entropy proportional to the square root of a conserved charge, while making explicit the assumptions about the two-dimensional conformal field theory that are required.

The arithmetic machinery is not presented as a universal explanation of black-hole entropy. Exact integer degeneracies, modular forms, Rademacher expansions, and the Cardy formula are established mathematical or physical tools in particular settings. The proposed advance is a unified audit of what must be demonstrated before those tools constitute a microscopic black-hole model: a defined Hilbert space, a specified dynamics, a justified identification of counted states with black-hole microstates, a controlled thermodynamic limit, and a derivation of both leading entropy and subleading corrections.

The decisive criterion is therefore stronger than reproducing the Bekenstein–Hawking formula. A successful model must count independently defined physical states, explain the map from their conserved charges to the black-hole geometry, and derive the entropy asymptotics without choosing degeneracies merely to fit the desired answer.

1. Introduction: Why count black-hole microstates?

Black-hole thermodynamics connects gravitational geometry, quantum theory, and statistical mechanics. The entropy associated with a horizon is proportional to its area rather than its volume. This suggests that the microscopic degrees of freedom responsible for black-hole entropy are organized in a way that differs from ordinary extensive matter.

The semiclassical entropy is

S_{\mathrm{BH}}

\frac{k_Bc^3A}{4G\hbar}

\frac{k_BA}{4\ell_P^2},
\qquad
\ell_P^2=\frac{G\hbar}{c^3},

where is the Planck length. The associated dimensionless entropy is

s_{\mathrm{BH}}
\equiv
\frac{S_{\mathrm{BH}}}{k_B}

\frac{A}{4\ell_P^2}.

If a microcanonical ensemble contains physically distinct states at fixed macroscopic charges, the statistical-mechanical relation is

S_{\mathrm{micro}}

k_B\log d_{\mathrm{BH}}.

Consequently, reproducing the leading semiclassical entropy requires

\log d_{\mathrm{BH}}

\frac{A}{4\ell_P^2}
+o(A/\ell_P^2),

in the appropriate large-area limit.

This is a statement about the growth of a degeneracy, not yet a theory of what the degeneracy counts.

A proposed arithmetic model must answer four independent questions:

* State definition: What are the microscopic states, and what distinguishes two states physically?
* Dynamics: What Hamiltonian, charge operators, constraints, or equivalent dynamical structure determines the spectrum?
* Geometric identification: Why does a given microscopic charge sector correspond to a black hole with a specified area, mass, angular momentum, or gauge charge?
* Counting theorem: Why do the independently defined degeneracies possess the claimed arithmetic structure and asymptotics?

The fourth question cannot replace the first three. A generating function engineered to have coefficients demonstrates that a desired asymptotic can be encoded mathematically. It does not demonstrate that those coefficients count black-hole microstates.

The purpose of ABHM is to formulate a stricter construction in which exact counting and arithmetic structure are derived from a microscopic model and then connected to macroscopic geometry.

2. Microscopic state spaces and exact counting

2.1 Definition of a microstate

Let be a microscopic Hilbert space, and let denote a family of mutually compatible conserved charges. A microcanonical sector at charge value is defined by the joint spectral conditions

\mathcal H_{\mathbf q}

\bigcap_{a}
\ker(\widehat Q_a-q_a I),

when the charges have discrete spectra and the joint eigenspace is well defined. For continuous spectra, a finite-width spectral window or an appropriate spectral measure must replace the exact eigenspace.

The exact degeneracy is

d(\mathbf q)

\dim\mathcal H_{\mathbf q}.

This definition makes a crucial distinction between a list of candidate configurations and a set of independent quantum states. If proposed states are linearly dependent, counting them separately overestimates the Hilbert-space dimension. If gauge-related configurations represent the same physical state, they must not be counted as distinct microstates.

A complete microscopic model must therefore specify:

* the Hilbert space and its inner product;
* the operators defining the conserved charges;
* the physical constraints and gauge identifications;
* the domain in which the state count is finite;
* the rule that determines when two state vectors represent independent physical states.

Only after these structures are supplied does become a well-defined counting function.

2.2 Exact degeneracy versus an index

In supersymmetric theories, an indexed degeneracy often takes the form

\Omega(\mathbf q)

\operatorname{Tr}{\mathcal H{\mathbf q}}
(-1)^F,

possibly with additional charge insertions to regulate fermion zero modes. Here is fermion number.

The index can be easier to calculate than the absolute degeneracy , because bosonic and fermionic contributions may cancel in pairs. But generally,

|\Omega(\mathbf q)|
\leq d(\mathbf q),

and equality need not hold. An index can remain unchanged under deformations even when the individual degeneracies of states change.

Thus an indexed count reproduces the full microcanonical entropy only when a separate argument establishes that the index captures the relevant degeneracy to the required asymptotic accuracy. This distinction is especially important in supersymmetric black-hole counting, where exact indices and the absolute number of states are related but not universally identical.

2.3 Entropy from a microscopic count

For an equally weighted microcanonical ensemble of independent states,

S_{\mathrm{micro}}(\mathbf q)

k_B\log d(\mathbf q).

The logarithm is natural because independent state counts multiply under independent composition while entropies add. This relation is standard statistical mechanics; the difficult question is how to determine from a quantum theory whose states and dynamics are independently specified.

A black-hole count must also fix its ensemble. Holding mass fixed is not the same as holding temperature fixed; holding angular momentum fixed differs from summing over angular-momentum sectors. A canonical partition function and a microcanonical degeneracy are related by a transform, but they should not be identified without specifying the transform, ensemble, and convergence conditions.

3. The arithmetic hypothesis

The arithmetic proposal begins with a discrete charge lattice and an integer-valued degeneracy function,

d:\Lambda\longrightarrow\mathbb Z_{\geq0},

where is the set of allowed charge labels. For a single nonnegative integer charge , introduce the generating function

Z(q)

\sum_{N\geq0}d(N)q^N,
\qquad |q|<1.

Here is a formal counting variable or a complex variable in the convergence domain. It is not automatically a physical position or a spacetime coordinate.

The arithmetic hypothesis is that , or a related function with additional charge variables, may possess exact structures that constrain its coefficients:

* Integrality: coefficients are exact state counts or indices.
* Product structure: factors encode independent oscillator modes or other microscopic excitations.
* Congruence structure: coefficients obey arithmetic restrictions, selection rules, or divisibility identities.
* Modular covariance: the function transforms predictably under transformations of the complex modulus.
* Automorphic structure: a multivariable generating function transforms under a larger discrete symmetry group.
* Exact coefficient reconstruction: the coefficients can be recovered from analytic or modular data rather than estimated only from a leading saddle point.

These properties have different logical strengths. Integer coefficients alone do not imply modularity. A product formula alone does not imply a black-hole interpretation. Modular covariance constrains coefficient growth, but it does not by itself identify the coefficients with physical black-hole microstates.

3.1 A product representation

A common structure in oscillator models is

Z(q)

\prod_{m=1}^{\infty}
(1-q^m)^{-a_m},

where counts the independent bosonic oscillator species at level . For a finite number of bosonic species at each level, the product is a well-defined formal power series; analytic convergence holds for under standard growth assumptions on .

The product has a microscopic interpretation only if the oscillator modes and their occupation rules are specified independently. Once that interpretation is supplied, the coefficient counts allowed occupation configurations at total level .

The product is therefore not merely a convenient generating function. In a complete model, it follows from a defined Fock space, a level operator, and a rule for composing excitations.

3.2 A precise toy model: integer partitions

Take one bosonic oscillator mode at every positive integer frequency. Let the level operator be

\widehat N

\sum_{m=1}^{\infty}m\,\widehat n_m,
\qquad
\widehat n_m\in\mathbb Z_{\geq0}.

A state is specified by the occupation sequence with finitely many nonzero entries. The exact degeneracy at level is the number of integer partitions of :

Z(q)

\prod_{m=1}^{\infty}\frac{1}{1-q^m}

\sum_{N=0}^{\infty}p(N)q^N.

This is an independently defined mathematical microstate model: the states are occupation-number configurations, and the dynamics of the counting problem are encoded by the level operator. No black-hole interpretation has yet been assumed.

The Hardy–Ramanujan asymptotic formula gives

p(N)
\sim
\frac{1}{4N\sqrt3}
\exp\!\left(
\pi\sqrt{\frac{2N}{3}}
\right).

Taking the logarithm,

\log p(N)

\pi\sqrt{\frac{2N}{3}}
-\log N
-\log(4\sqrt3)
+o(1).

This result demonstrates how a microscopic count can yield an entropy with a leading square-root growth and a logarithmic correction.

However, this toy model does not derive black-hole entropy. It contains no independently specified black-hole metric, gravitational coupling, horizon area, or map between and a black-hole charge. Declaring an area proportional to could force agreement with the leading term, but that would be an imposed identification rather than a derivation of black-hole microphysics.

The model is valuable because it separates the exact combinatorial counting problem from the additional physical work required to interpret that count gravitationally.

4. Modular structure and the transformation of counting functions

4.1 The modular parameter

Write

q=e^{2\pi i\tau},
\qquad
\operatorname{Im}\tau>0.

A modular transformation acts on the upper half-plane by

\tau\longmapsto
\frac{a\tau+b}{c\tau+d},
\qquad
a,b,c,d\in\mathbb Z,
\qquad
ad-bc=1.

A modular form of weight , schematically, obeys

f\!\left(\frac{a\tau+b}{c\tau+d}\right)

(c\tau+d)^k f(\tau),

subject to the relevant conditions at cusps and any multiplier system. More general modular objects may be weakly holomorphic, meromorphic, vector-valued, or transform with a nontrivial representation.

The modular transformation relates the behavior of the generating function in different regions of its domain. Since the coefficients are extracted by a contour integral,

d(N)

\frac{1}{2\pi i}
\oint
\frac{Z(q)}{q^{N+1}}\,dq,

the transformation properties can constrain the asymptotic behavior of the coefficients.

The essential point is that modularity links global analytic structure to local coefficient growth. It is this link—not the mere presence of a product expansion—that makes modular forms useful for exact state counting.

4.2 Partition functions of two-dimensional conformal field theories

In a two-dimensional conformal field theory (CFT), the torus partition function takes the schematic form

Z_{\mathrm{CFT}}(\tau,\bar\tau)

\operatorname{Tr}
\left\[
q^{L_0-c_L/24}
\\bar q^{\\,\\bar L_0-c_R/24}
\\right\].

Here are the left- and right-moving Virasoro zero modes, while are the corresponding central charges. The coefficient of a specified pair of excitation levels encodes the degeneracy of states with those conformal weights, with conventions depending on the spectrum and boundary conditions.

Modular invariance of the torus partition function is a consequence of the consistency requirements of an appropriate CFT on the torus. In suitable high-energy regimes, it constrains the asymptotic density of states.

The Cardy formula is one of the most important consequences of this structure. It has been used to reproduce black-hole entropy in well-defined holographic settings, notably for black holes in three-dimensional anti-de Sitter gravity and for certain supersymmetric black holes in string theory. These successes are established results in their respective regimes, not evidence that every black-hole microstate spectrum must arise from a modular CFT.

4.3 Modularity is not a universal assumption

A proposed black-hole model must derive or justify the relevant modular property. It is insufficient to select a modular function because its coefficients have the desired exponential growth.

For example, a function might have a modular transformation law but count states of an auxiliary mathematical system unrelated to the black hole. To establish a physical interpretation, one must show why the microscopic Hilbert space has the required CFT or automorphic structure and why the coefficient labels correspond to the black hole’s conserved charges.

The arithmetic hypothesis is thus conditional:

If a microscopic black-hole sector is independently shown to admit a suitable modular generating function, modularity may constrain its exact degeneracies and their asymptotic corrections.

This is a mathematically meaningful statement without asserting that modularity has been established for all black holes.

5. The Cardy asymptotic and black-hole entropy

The most direct established bridge between modular state counting and black-hole entropy is the asymptotic density of states in a two-dimensional conformal field theory.

5.1 Cardy growth

Consider a unitary two-dimensional CFT with left- and right-moving central charges . Let denote excitation levels measured relative to the appropriate vacuum shifts. In the Cardy regime, the leading logarithm of the degeneracy is

\boxed{
\log d(\Delta_L,\Delta_R)
\sim
2\pi\sqrt{\frac{c_L\Delta_L}{6}}
+
2\pi\sqrt{\frac{c_R\Delta_R}{6}}
}

in units where .

The formula follows from modular properties of the partition function under appropriate assumptions. Its precise regime of validity depends on the spectrum, the treatment of vacuum contributions, and the scaling of the central charges and excitation levels. For fixed CFT data, it gives the familiar high-energy asymptotic. In large-central-charge holographic systems, additional spectral assumptions can be needed to justify the desired regime.

The important structure is exponential growth:

d(\Delta_L,\Delta_R)
\sim
\exp\!\left\[
2\\pi\\sqrt{\\frac{c_L\\Delta_L}{6}}
+
2\\pi\\sqrt{\\frac{c_R\\Delta_R}{6}}
\\right\].

Thus a microscopic spectrum defined by a CFT can yield an entropy that is the sum of two square-root terms. Whether this equals a gravitational entropy depends on an independent relation between the CFT charges and the black-hole parameters.

5.2 A concrete gravitational realization: the BTZ black hole

The Bañados–Teitelboim–Zanelli (BTZ) black hole is a particularly clear setting because three-dimensional anti-de Sitter gravity admits a well-understood asymptotic symmetry structure.

In standard conventions with , the Brown–Henneaux central charges are

c_L=c_R=\frac{3\ell}{2G_3},

where is the anti-de Sitter radius and is the three-dimensional Newton constant. The black-hole mass and angular momentum determine the left- and right-moving excitation levels through the gravitational charge dictionary.

For the BTZ solution, the Bekenstein–Hawking entropy is

S_{\mathrm{BH}}

\frac{A_H}{4G_3}

\frac{2\pi r_+}{4G_3},

where is the horizon circumference. With the Brown–Henneaux central charges and the corresponding charge assignments, the Cardy entropy agrees with this expression in the appropriate regime.

This is not an arbitrary matching of functions. The CFT structure, its central charge, and the relation between asymptotic gravitational charges and CFT excitation levels are independently specified by the theory. The entropy agreement is a consequence of those structures.

The example provides an important benchmark for ABHM: a new arithmetic model should explain what it adds beyond an already established microscopic or holographic counting construction.

5.3 What the BTZ example establishes

The BTZ case establishes that, in a specific gravitational setting, a modularly constrained density of states can reproduce a black-hole area entropy. It does not establish that:

* every four-dimensional or astrophysical black hole has an exact dual CFT of the same type;
* every integer-valued generating function with Cardy-like growth counts black-hole microstates;
* modularity alone determines the microscopic Hamiltonian;
* the full nonperturbative spectrum and all corrections follow from the leading Cardy term.

The correct generalization is methodological: first define the microscopic system and its charge dictionary; then derive the coefficient asymptotics; finally compare the result with the macroscopic entropy.

6. Exact coefficients and Rademacher reconstruction

Leading asymptotics discard information. A stronger arithmetic approach seeks an exact or convergent reconstruction of the coefficients themselves.

6.1 Why the leading saddle is insufficient

Suppose

\log d(N)

\alpha\sqrt N
+
\beta\log N
+
\gamma
+
O(N^{-\delta}),
\qquad \delta>0.

The leading term determines the dominant exponential growth, but it does not uniquely determine , or the inverse-power corrections. Distinct microscopic spectra can share the same leading asymptotic.

If the generating function belongs to a suitable class of modular forms, its coefficients may admit a Rademacher-type expansion. In broad terms, such expansions express Fourier coefficients as convergent sums involving arithmetic Kloosterman sums and modified Bessel functions, with details depending on the modular weight, multiplier system, polar data, and other defining features of the modular object.

For suitable weakly holomorphic modular forms, the polar part and modular transformation law determine the positive-index coefficients through an exact expansion. This converts modular data into coefficient-level information rather than only a leading entropy estimate.

Rademacher expansions have been applied to black-hole entropy problems in CFT frameworks, including calculations of subleading corrections to the Bekenstein–Hawking term.

6.2 Schematic form

For a suitable modular object with Fourier coefficients , a Rademacher-type formula has the general structure

d(N)

\sum_{c=1}^{\infty}
\mathcal K_c(N)\,
\mathcal B_c(N),

where denotes arithmetic sums determined by the modular transformation data and contains Bessel-function contributions with arguments that grow roughly as .

This expression is schematic rather than a universal formula: the exact prefactors, Bessel order, allowed values of , and treatment of polar coefficients depend on the modular object. Those details must be derived for each model.

The dominant contribution often comes from the first term in the expansion, giving the leading exponential entropy. Subsequent terms encode additional arithmetic information and can produce exponentially suppressed corrections, oscillatory contributions, or other subleading structure.

6.3 Exactness is model-dependent

An exact Rademacher expansion does not mean that every black-hole degeneracy is known exactly. The expansion applies only when the generating function belongs to a class for which the required modular reconstruction theorem holds.

A black-hole model must therefore prove or justify:

* the existence of its generating function;
* its modular or automorphic transformation law;
* the required analytic conditions;
* the correct polar data or equivalent seed information;
* the identification of its Fourier coefficients with the intended physical degeneracies or indices.

Only then does exact coefficient reconstruction become a physical counting result.

7. The target theorem: entropy from an independently defined count

The central mathematical objective of ABHM is to establish a clean theorem connecting exact microscopic degeneracies to a specified black-hole entropy law, while keeping the geometric charge dictionary independent of the desired entropy.

Definition 1 — Microscopic counting model

A microscopic counting model is a tuple

\mathfrak M

(\mathcal H,\widehat{\mathbf Q},
\mathcal C,\mathcal Z,\mathfrak D),

where:

* is a defined microscopic Hilbert space;
* is a specified family of conserved charge operators;
* is the set of physical constraints and gauge identifications;
* is a generating function derived from the charge-resolved spectrum;
* is an independently established dictionary mapping the microscopic charges to macroscopic black-hole parameters.

The model is counting-complete for a specified sector if the coefficients of equal the dimensions of the corresponding physical charge sectors, or equal a specified protected index whose relation to the absolute degeneracy has been established.

The phrase “independently established” is essential: the map must come from the dynamics or a controlled duality, not from fitting the desired entropy.

Theorem 1 — Asymptotic microstate entropy matching

Let be a discrete microscopic charge label, and let be the exact degeneracy of a counting-complete microscopic model. Suppose the following conditions hold.

(A1) Independent state definition. The states counted by are defined by the microscopic Hilbert space, charge operators, and physical constraints, independently of the black-hole entropy formula.

(A2) Exact generating function. The coefficients are the coefficients of a well-defined generating function

\mathcal Z(q)=\sum_{N\geq0}d(N)q^N.

(A3) Derived coefficient asymptotics. The microscopic model implies

\log d(N)

F(N)+o(1)

as , where is derived from the counting theory, for example by a justified modular asymptotic or coefficient theorem.

(A4) Independent geometric dictionary. The macroscopic area associated with the charge sector is , determined independently from the model’s gravitational charges or duality map.

(A5) Asymptotic compatibility. For a specified target entropy,

\frac{A(N)}{4\ell_P^2}

F(N)+o(1).

Then the microcanonical entropy satisfies

\boxed{
S_{\mathrm{micro}}(N)

\frac{k_B A(N)}{4\ell_P^2}
+
o(k_B)
}

in the stated large- limit, provided the error term in (A5) is measured in the same dimensionless asymptotic regime.

Proof

By definition of the microcanonical entropy,

S_{\mathrm{micro}}(N)

k_B\log d(N).

By (A3),

S_{\mathrm{micro}}(N)

k_BF(N)+o(k_B).

By (A5),

F(N)

\frac{A(N)}{4\ell_P^2}+o(1).

Substituting yields

S_{\mathrm{micro}}(N)

\frac{k_BA(N)}{4\ell_P^2}+o(k_B).

Since , the leading term is

\frac{k_BA(N)}{4\ell_P^2}

\frac{k_Bc^3A(N)}{4G\hbar}.

This is the Bekenstein–Hawking entropy for the specified area .

7.1 What the theorem contributes

The theorem is deliberately conditional. It is a logically precise matching criterion, not a claim that a new universal microstate count has already been found.

Its value is to prevent a common circular construction. If one first defines

d(N)

\left\lfloor
\exp\!\left(\frac{A(N)}{4\ell_P^2}\right)
\right\rfloor

and then observes that approximately reproduces the entropy, the result is built into the definition. It does not explain the microscopic origin of the count.

The theorem becomes a substantive physical result only when (A1)–(A4) are established by an independently specified microscopic theory and (A5) follows as a derived consequence.

7.2 A stronger correction-matching criterion

A model that reproduces only the leading term remains underconstrained. Suppose the target entropy has an expansion

\frac{S_{\mathrm{target}}}{k_B}

\frac{A}{4\ell_P^2}
+
\alpha_{\log}\log\!\left(\frac{A}{\ell_P^2}\right)
+
\alpha_0
+
\sum_{r\geq1}
\alpha_r
\left(\frac{\ell_P^2}{A}\right)^r.

This expression is schematic: the allowed terms and coefficients depend on the black-hole family, ensemble, quantum fields, and approximation regime.

A refined matching theorem requires the microscopic logarithm to reproduce the corresponding terms under the independent dictionary , with an error smaller than the last term claimed to be controlled. A fit to the leading area term cannot be presented as a derivation of the logarithmic coefficient.

This is a stronger test because subleading terms contain information about the microscopic spectrum and the quantum fields that the leading exponential often obscures.

8. A concrete modular model: the CFT counting construction

The preceding theorem gives the general target. A more concrete construction uses a two-dimensional CFT whose spectrum and modular properties are independently defined.

8.1 Microscopic data

Let be the Hilbert space of a unitary two-dimensional CFT with left- and right-moving Virasoro algebras. Define the charge-resolved degeneracy

d(h,\bar h)

\dim\left\{
|\psi\rangle:
L_0|\psi\rangle=h|\psi\rangle,\;
\bar L_0|\psi\rangle=\bar h|\psi\rangle
\right\},

with the appropriate vacuum shifts and any additional symmetry-sector restrictions included in the definition.

The microscopic counting function is the torus partition function

Z_{\mathrm{CFT}}(\tau,\bar\tau)

\sum_{h,\bar h}
d(h,\bar h)\,
q^{h-c_L/24}
\bar q^{\,\bar h-c_R/24}.

This is not merely a postulated generating series. It is the trace over the independently defined CFT Hilbert space. Its coefficients are constrained by the operator content, unitarity, and modular consistency of that CFT.

8.2 Counting theorem in the Cardy regime

Assume the CFT has a modular-invariant torus partition function, an appropriate discrete spectrum, and a regime in which the Cardy asymptotic is valid. Then

\log d(h,\bar h)

2\pi\sqrt{\frac{c_L\Delta_L}{6}}
+
2\pi\sqrt{\frac{c_R\Delta_R}{6}}
+
o\!\left(\sqrt{\Delta_L}+\sqrt{\Delta_R}\right),

where are the correctly shifted excitation levels.

The microscopic model has now supplied the entropy asymptotics from a state count. To obtain a black-hole result, one must independently establish that:

* the CFT is the appropriate microscopic description of the gravitational sector;
* the charge dictionary identifies with the black hole’s mass, angular momentum, and other conserved charges;
* the gravitational horizon area is given by the corresponding classical solution;
* the CFT regime is the same regime in which the semiclassical black-hole entropy formula applies.

When these conditions hold, the Cardy growth can reproduce the leading Bekenstein–Hawking entropy. The BTZ/CFT correspondence provides a canonical example.

8.3 What is new in the ABHM formulation?

The CFT construction itself is established. ABHM does not claim to have discovered the Cardy formula or the microscopic counting of known supersymmetric black holes. Its proposed contribution is an explicit arithmetic audit that tracks each step:

\begin{aligned}
&\text{defined microscopic Hilbert space}\\
&\Downarrow\\
&\text{exact charge-resolved degeneracies}\\
&\Downarrow\\
&\text{modular or automorphic constraints}\\
&\Downarrow\\
&\text{asymptotic coefficient theorem}\\
&\Downarrow\\
&\text{independent gravitational charge dictionary}\\
&\Downarrow\\
&\text{entropy matching and correction tests}.
\end{aligned}

The audit is designed to expose where a proposed model uses an unproved duality, assumes modularity without derivation, or fits the geometric charge dictionary to the desired entropy.

A new physical result would require applying this architecture to a specified model for which the microstates, dynamics, and area dictionary are not already known to yield the desired result.

9. Beyond the leading term: logarithmic entropy corrections

The leading area term is necessary but not sufficient. Quantum corrections can contain logarithms of the horizon scale, constants, and inverse-area terms. These corrections are useful because they can depend on the low-energy field content and on the ensemble, boundary conditions, and treatment of zero modes.

9.1 Generic asymptotic expansion

Let

x=\frac{A}{\ell_P^2}.

A candidate microscopic degeneracy may have the asymptotic form

\log d(N)

a_1 x
+
a_{\log}\log x
+
a_0
+
\frac{a_{-1}}{x}
+
O(x^{-2}),

after applying an independently derived relation between and . For Bekenstein–Hawking matching, the leading coefficient must be in the dimensionless entropy .

The remaining coefficients are not universal across all black-hole systems. They depend on the microscopic model and on which ensemble and physical sector are being counted. In particular, logarithmic corrections have been calculated from low-energy quantum fields and matched against microscopic constructions in several settings.

9.2 Why logarithms are discriminating

Suppose two microscopic models satisfy

\log d_1(N)

\frac{x}{4}+a_{\log}^{(1)}\log x+O(1)

and

\log d_2(N)

\frac{x}{4}+a_{\log}^{(2)}\log x+O(1).

Both reproduce the leading area law, but they disagree at the logarithmic order if

a_{\log}^{(1)}\neq a_{\log}^{(2)}.

If the target black-hole system has an independently calculated logarithmic correction, this difference can falsify one of the proposed microscopic models. Conversely, agreement at the logarithmic order is stronger evidence than leading-order matching, though it is still not a complete derivation of the microscopic dynamics.

9.3 The role of zero modes and ensemble choice

A logarithmic term can be sensitive to the treatment of zero modes, collective coordinates, and the difference between canonical and microcanonical ensembles. A calculation that ignores these distinctions may obtain a coefficient that disagrees with the correct physical ensemble.

The arithmetic model must therefore state exactly what is counted: absolute degeneracy, a protected index, a canonical partition function, a fixed-charge microcanonical sector, or a relative count. Corrections cannot be compared responsibly until the ensemble and the counted object are aligned.

10. Exact counting identities and arithmetic constraints

The arithmetic program is broader than modular invariance. Several types of exact identities can constrain a degeneracy sequence.

10.1 Recurrences

A generating function may imply a recurrence

\sum_{j=0}^{r}a_j(N)\,d(N-j)=0

for specified coefficients , with suitable initial data. Such recurrences can make an exact sequence computable without enumerating every state individually.

A recurrence is physically meaningful only when it is derived from the microscopic construction or its generating function. A recurrence inferred from a finite list of numerical degeneracies may be accidental.

10.2 Congruences and divisibility

An arithmetic sequence may satisfy congruences such as

d(N)\equiv d’(N)\pmod m

for specified integers and , or possess divisibility properties. In a physical model, such identities can reflect hidden symmetries, protected indices, or special product formulas.

But congruences are not automatically physical selection rules. The model must explain whether they arise from a symmetry, a representation-theoretic identity, a modular transformation, or a property of the chosen index.

10.3 Multiplicative structure

Some generating functions possess Euler products, Dirichlet-series representations, or product expansions with coefficients related to arithmetic functions. Such structures can encode independent sectors, partitions, or protected excitation modes.

The interpretation depends on the microscopic system. A product factor may represent an oscillator, a species of excitation, a charge sector, or a mathematical factorization with no direct physical interpretation. The model must justify the chosen interpretation before the product can be treated as a count of physical constituents.

10.4 Multiple charges and multivariable generating functions

Black holes generally carry more information than a single integer label. A refined counting function may take the form

Z(\mathbf z)

\sum_{\mathbf q}
d(\mathbf q)\,
\mathbf z^{\mathbf q},

where can include energy, angular momentum, gauge charges, or other conserved quantities.

For complex variables , the monomial notation means

\mathbf z^{\mathbf q}

\prod_i z_i^{q_i},

with appropriate conventions for negative or fractional charges.

A multivariable generating function can distinguish sectors that would be merged in a single-variable count. This matters whenever different charge assignments correspond to different black-hole geometries or when an index cancels contributions differently in different sectors.

An exact single-variable formula may be insufficient if the target entropy depends on angular momentum or gauge charges that have been summed over.

11. The distinction between absolute degeneracies and protected indices

Supersymmetry can make microscopic counting tractable by protecting an index against continuous deformations. But the index is a signed count, not automatically the dimension of the full state space.

Let

d(N)=n_B(N)+n_F(N)

denote the total number of bosonic and fermionic states in a sector, while

\Omega(N)=n_B(N)-n_F(N)

denotes a simple supersymmetric index. Then

|\Omega(N)|\leq d(N).

If bosonic and fermionic degeneracies nearly cancel, can be exponentially smaller than . In that case,

\log|\Omega(N)|

does not equal the absolute microcanonical entropy.

A protected index can still reproduce the leading black-hole entropy when a physical argument establishes that cancellations are sufficiently controlled, or when the index is the relevant quantity for the supersymmetric sector being studied. Such a result must be stated in its correct scope.

11.1 A counting audit for supersymmetric models

A rigorous paper should state:

* the supercharge or supersymmetry algebra;
* the sector in which the index is defined;
* the regularization of zero modes;
* the charges held fixed;
* whether the result is an absolute degeneracy or an index;
* the argument connecting the index to the macroscopic entropy.

Without these statements, an exact arithmetic identity may be mathematically valid but physically ambiguous.

11.2 Why exactness does not remove interpretation

An exact index can be computed without knowing every state explicitly. That is a major mathematical advantage. But exact evaluation does not automatically settle which states correspond to a particular semiclassical black-hole solution, whether the index equals the absolute degeneracy, or whether the ensemble matches the macroscopic entropy calculation.

The model must separate computational exactness from physical completeness.

12. The microscopic dynamics cannot be inferred from the entropy

A central danger in arithmetic state counting is to confuse a formula for the number of states with a microscopic theory of those states.

12.1 The required dynamical data

A complete model should provide at least one of the following equivalent or complementary descriptions:

* a Hamiltonian and its charge-resolved spectrum;
* a quantum field theory with a defined operator algebra and physical Hilbert space;
* a constrained quantum system with a specified physical-state construction;
* a string-theoretic or other quantum-gravitational construction with defined branes, charges, and admissible bound states;
* a well-defined dual theory together with a justified dictionary to the gravitational sector.

The model must explain how the counted states are created, distinguished, and organized. The generating function should be a consequence of that structure.

12.2 Spectrum and dynamics are not identical

Even if two systems have the same degeneracy function,

d_1(N)=d_2(N)

for every , they need not have the same matrix elements of observables, interaction rules, or time evolution. State counts constrain a spectrum, but generally do not uniquely determine the dynamics.

This observation has a direct implication for ABHM. A successful entropy count is evidence about the microscopic state space, but it does not uniquely identify the microscopic theory. To claim a dynamical explanation, the model must also specify how its states interact and how its conserved charges are realized.

12.3 Independent derivation of the generating function

A strong microscopic derivation would proceed in the order

\text{microscopic degrees of freedom}
\longrightarrow
\text{physical state constraints}
\longrightarrow
\text{charge operator}
\longrightarrow
\text{exact degeneracy}
\longrightarrow
\text{generating function}.

The reverse direction can be useful mathematically: a generating function may reveal a hidden product structure or a candidate symmetry. But discovering a generating function with a desirable asymptotic does not, by itself, establish that the corresponding microscopic degrees of freedom exist in the physical system.

13. The independent geometry dictionary

The arithmetic count becomes a black-hole result only after a microscopic charge sector is identified with a macroscopic geometry.

Let the black-hole solution be labeled by parameters

\mathbf p=(M,J,Q_1,\ldots,Q_s),

where is mass, angular momentum, and additional conserved charges. Let its horizon area be .

A microscopic theory supplies a charge map

\mathbf q=\Phi(\mathbf p)

or, inversely, a relation

\mathbf p=\Psi(\mathbf q)

on the appropriate physical sector. The area in microscopic variables is then

A_{\mathrm{micro}}(\mathbf q)

A\bigl(\Psi(\mathbf q)\bigr),

provided the map is well defined and the microscopic and macroscopic charge conventions are compatible.

13.1 What makes the map independent?

The charge dictionary should be derived from the theory’s conserved quantities, asymptotic symmetries, duality map, or semiclassical limit. It must not be selected merely to make

\log d(\mathbf q)

\frac{A_{\mathrm{micro}}(\mathbf q)}{4\ell_P^2}

hold.

For example, in a holographic construction, the relation between CFT excitation levels and black-hole mass and angular momentum is fixed by the gravitational charge dictionary. The entropy agreement then tests the microscopic counting. It is not legitimate to reverse-engineer arbitrary charge assignments for a generic integer sequence and present the resulting agreement as a derivation.

13.2 Dimensional consistency

The dimensionless entropy is

s_{\mathrm{BH}}

\frac{A}{4\ell_P^2}.

Any arithmetic expression claimed to reproduce it must therefore be dimensionless. If a charge label is dimensionless, a relation between and must come from the microscopic theory; it cannot be inferred from dimensional analysis alone.

A common structural possibility is

\frac{A}{\ell_P^2}
\sim \kappa N^\gamma

for constants and . If a microscopic count satisfies , the leading entropy can match if the coefficients agree. But the exponent and coefficient must arise independently on the two sides for the match to be explanatory.

13.3 The area law does not identify the microscopic variables

Many microscopic models can be arranged to have degeneracies growing as . The area law constrains the asymptotic count; it does not uniquely determine whether the underlying states are oscillator excitations, brane bound states, spin-network states, horizon degrees of freedom, or another structure.

The microscopic theory must identify its own state variables before the entropy match can be interpreted as a physical explanation.

14. A no-fit criterion for arithmetic black-hole models

To prevent circularity, ABHM proposes a no-fit criterion for candidate microscopic constructions.

A model passes this criterion only if the following elements are fixed before the target entropy is used to tune the count:

* State space: the microscopic Hilbert space and physical constraints.
* Dynamics: the Hamiltonian, charge operators, or equivalent dynamical structure.
* Counting rule: the exact definition of degeneracy or index.
* Arithmetic structure: the product, recurrence, modular transformation, or other identity.
* Geometric dictionary: the relation between microscopic charges and black-hole parameters.
* Target observable: the entropy formula and the ensemble in which it is to be tested.

The model may then be tested against the target entropy. It should not be allowed to redefine the state count, adjust the charge dictionary, or change the ensemble after the discrepancy is known, except through a new model whose changes are independently justified.

14.1 Why this is stricter than curve fitting

Suppose a model has a free parameter and predicts

\log d_\lambda(N)

\alpha(\lambda)\sqrt N
+
\beta(\lambda)\log N
+\cdots.

Matching the leading entropy by selecting is not necessarily illegitimate. Physical models often contain parameters fixed by independent measurements or consistency conditions. The problem arises when has no independent meaning and is chosen solely to force the entropy coefficient to .

The stronger test is whether is fixed by independent dynamics and whether the same value then reproduces the leading term, logarithmic correction, and other charge-dependent predictions.

14.2 A hierarchy of evidence

The evidential strength of a proposed count can be ordered as follows:

* Level 0: a degeneracy formula is chosen to reproduce the entropy.
* Level 1: a mathematically defined counting problem produces the desired asymptotic.
* Level 2: a microscopic Hilbert space and charge operator independently produce the counting function.
* Level 3: a justified arithmetic or modular structure yields exact or controlled coefficient asymptotics.
* Level 4: an independently derived gravitational dictionary yields the area law and specified corrections.
* Level 5: the model also reproduces independent observables or dynamical properties of the black-hole sector.

Level 1 is a mathematical existence demonstration. Levels 2–4 are needed for a credible microscopic entropy derivation. Level 5 provides stronger evidence that the construction captures more than the state count.

15. The relation to established black-hole microstate counting

The arithmetic program must be situated alongside existing microscopic derivations.

15.1 Supersymmetric D-brane counting

Strominger and Vafa derived the Bekenstein–Hawking entropy for a class of five-dimensional extremal black holes by counting BPS bound states in string theory. Their result demonstrated that the area entropy can emerge from a microscopic degeneracy in a controlled setting.

The lesson for ABHM is that the microscopic degrees of freedom and the relation to the black-hole charges are essential. The entropy agreement is meaningful because the count is not defined by inserting the area formula into the degeneracy.

15.2 CFT and asymptotic symmetries

The Cardy formula provides a second established route. In appropriate two-dimensional CFTs, modular invariance constrains the high-energy density of states. In gravitational settings where the relevant conformal structure and charge dictionary are justified, the resulting count can reproduce black-hole entropy.

ABHM should therefore not claim a new universal entropy derivation merely by invoking modular invariance. A new result must either establish the necessary CFT structure in a previously unresolved setting or derive additional exact information beyond the existing Cardy analysis.

15.3 Logarithmic corrections as a microscopic test

Quantum corrections to black-hole entropy can be computed from low-energy gravitational data in several settings. These corrections provide a nontrivial comparison with microscopic state counts, because the logarithmic coefficient can depend on the massless field spectrum and the treatment of zero modes.

An arithmetic model that reproduces the leading area term but fails an independently established logarithmic correction is not a complete account of the entropy in that regime.

15.4 Recent state-counting constructions

Other approaches attempt to define black-hole microstates through families of semiclassical states and compute the dimension of their span using overlap matrices or gravitational path-integral methods. These approaches emphasize that candidate states must be linearly independent to count as separate microstates.

This is directly relevant to arithmetic counting: coefficients in a generating function must represent independent physical states, not merely a formal enumeration of semiclassical configurations that may be overcomplete.

16. Failure modes and mathematical obstructions

A robust research program must identify situations in which arithmetic structure fails to deliver the claimed physical result.

16.1 Correct growth, incorrect states

A sequence may satisfy

\log d(N)\sim \frac{A(N)}{4\ell_P^2}

but count states of a mathematical model unrelated to the target black hole. The asymptotic match is then numerically correct but physically uninformative.

Resolution: require an independently specified microscopic Hilbert space and a justified geometric dictionary.

16.2 Index cancellations

An exact protected index may have the desired growth in one regime while the absolute degeneracy behaves differently because of cancellations.

Resolution: prove a relation between the index and the relevant absolute or coarse-grained entropy, or state explicitly that the result concerns an indexed entropy.

16.3 Incorrect modular assumptions

A generating function may be modular only after a nontrivial multiplier, vector-valued transformation, or additional charge dependence is included. Treating it as an ordinary scalar modular form can produce incorrect coefficient formulas.

Resolution: specify the precise modular object and use a coefficient theorem valid for its transformation law.

16.4 Nonuniform asymptotics

An asymptotic formula may hold for fixed central charge and large excitation level but fail in a simultaneous limit where the central charge also grows. This matters when a semiclassical gravitational limit requires large charges and a large number of degrees of freedom at the same time.

Resolution: state the scaling regime and prove uniform error estimates or use a theorem appropriate to the simultaneous limit.

16.5 Wrong ensemble

A canonical partition function can produce an entropy different from the microcanonical logarithm if the ensemble equivalence assumptions fail, especially near extremality or in sectors with unusual fluctuations.

Resolution: define the ensemble, specify the charge constraints, and perform the appropriate inverse transform or direct microcanonical count.

16.6 Missing corrections

A leading asymptotic may match while the logarithmic term or exact coefficient sequence disagrees with the independently defined target theory.

Resolution: treat subleading terms as mandatory tests when the model claims control over them.

16.7 Overcounting semiclassical configurations

A family of geometric configurations may contain linearly dependent quantum states. Counting configurations rather than the dimension of their span can overestimate the entropy.

Resolution: construct the physical inner product or overlap matrix and establish the rank or an equivalent independent-state count. Recent approaches to black-hole state counting explicitly emphasize this issue.

17. A falsifiable research program

ABHM should be developed through a sequence of tests with explicit failure criteria.

Test 1 — Independent state construction

Specify the microscopic degrees of freedom, Hilbert space, constraints, and charge operators.

Failure condition: the state labels or degeneracies are introduced only to reproduce the desired entropy.

Test 2 — Exact counting identity

Derive the generating function or recurrence from the microscopic construction. Verify its coefficients in regimes where direct counting is feasible.

Failure condition: the asserted counting identity fails, or the coefficients do not equal the defined physical degeneracies.

Test 3 — Arithmetic structure

Prove the claimed product formula, congruence, modular transformation, or automorphic property.

Failure condition: the transformation law or arithmetic identity does not hold for the defined counting function.

Test 4 — Coefficient asymptotics

Derive the leading and subleading coefficient behavior with a stated error estimate and scaling regime.

Failure condition: the asymptotic theorem’s hypotheses fail, or the calculated coefficients disagree with the claimed approximation within the controlled regime.

Test 5 — Independent area dictionary

Derive the relation between microscopic charges and the macroscopic horizon area.

Failure condition: the dictionary can be fixed only by fitting the entropy coefficient.

Test 6 — Leading entropy

Compare the microscopic entropy with

S_{\mathrm{BH}}

\frac{k_Bc^3A}{4G\hbar}.

Failure condition: the leading coefficient or scaling disagrees in the declared regime.

Test 7 — Logarithmic correction

Compare the microscopic logarithmic term with the independently established correction for the same theory, ensemble, and field content.

Failure condition: the coefficient disagrees beyond the stated theoretical uncertainty.

Test 8 — Charge dependence

Test the degeneracy as a function of angular momentum, gauge charges, and other parameters, rather than checking only a single one-parameter sequence.

Failure condition: the count matches one sector but fails the independently predicted dependence on other conserved charges.

Test 9 — Physical independence of counted states

Establish that the counted states are linearly independent after imposing gauge constraints and physical equivalences.

Failure condition: the count includes redundant or overcomplete configurations as independent states.

Test 10 — Independent observable

Where the model makes further predictions, test an observable not used to tune the entropy match, such as a protected index, a charge-resolved degeneracy, or a controlled dynamical property.

Failure condition: the model fails the prediction in the regime where its derivation claims validity.

These tests distinguish a mathematically interesting sequence from a physically credible microscopic theory.

18. A proposed research architecture: Arithmetic Microstate Reconstruction

The preceding analysis suggests a more concrete research architecture. The goal is not to posit a universal arithmetic law for black holes, but to construct a sequence of independently testable mathematical objects.

18.1 The model tuple

Define an Arithmetic Microstate Reconstruction model by

\mathfrak A

(\mathcal H_{\mathrm{phys}},
\widehat{\mathbf Q},
\mathcal Z,
\mathfrak M,
\mathfrak G),

where:

* is the physical microscopic Hilbert space;
* is the family of conserved charge operators;
* is the charge-resolved generating function;
* is the arithmetic structure and the theorem that controls its coefficients;
* is the independently derived geometric charge dictionary.

For a single discrete charge, the central relation is

\mathcal Z(q)

\operatorname{Tr}{\mathcal H{\mathrm{phys}}}
q^{\widehat N}

\sum_{N\geq0}d(N)q^N,

provided has nonnegative integer spectrum and the trace is well defined in the intended domain. In a supersymmetric or refined model, the trace may include insertions, and the resulting coefficients must be interpreted accordingly.

This construction makes the generating function a consequence of the microscopic theory. Its arithmetic properties are then mathematical facts to be proved about .

18.2 Reconstruction pipeline

The intended workflow is:

1. Microscopic definition

Specify the physical Hilbert space, charge operators, constraints, and equivalence relations.

2. Exact generating function

Derive coefficients from the trace or independent-state count.

3. Arithmetic theorem

Prove modularity, a recurrence, an exact product, or another coefficient constraint.

4. Asymptotic reconstruction

Calculate the leading growth, logarithmic terms, and controlled residual corrections.

5. Independent gravitational test

Use the charge dictionary to compare with horizon area and other black-hole observables.

The order matters. If the geometric dictionary is adjusted after the asymptotics are known, the reconstruction loses much of its explanatory force.

18.3 Exact count versus asymptotic count

The framework should report three levels of result separately:

d(N)\quad\text{(exact degeneracy)},d(N)\sim e^{F(N)}
\quad\text{(leading asymptotic)},\log d(N)=F(N)+R(N)
\quad\text{(controlled remainder)}.

The first is the exact microscopic quantity. The second is a growth statement. The third is needed to establish the accuracy of a claimed correction. An exact generating function may coexist with an asymptotic formula that is insufficiently precise for logarithmic entropy matching.

19. A stronger theorem target: arithmetic rigidity of entropy

The asymptotic matching theorem in Section 7 provides a precise criterion, but it does not yet establish a new arithmetic constraint on black-hole spectra. A stronger research target would show that the microscopic arithmetic structure restricts the allowed entropy corrections more tightly than the leading area law does.

Conjecture 1 — Arithmetic rigidity

Let be the charge-generating function of a physically defined microscopic model. Suppose it satisfies a specified modular or automorphic transformation law, with independently determined polar data and a coefficient reconstruction theorem.

Then the asymptotic expansion of its degeneracies may be fixed, to a stated order, by those arithmetic data. If the model also has an independently derived gravitational charge dictionary, the same data constrain the allowed black-hole entropy corrections.

The conjecture is conditional on the modular object and coefficient theorem. In appropriate classes of modular forms, exact coefficient reconstruction is already established; the open research task is to establish the required structure for a new physical black-hole model and connect its coefficients to the intended states.

19.1 What would count as a new theorem?

A meaningful new theorem should do at least one of the following:

* derive a modular or automorphic property from a microscopic gravitational construction;
* establish an exact coefficient identity for a previously unresolved physical spectrum;
* prove a uniform asymptotic expansion in a relevant semiclassical limit;
* constrain a logarithmic or inverse-area correction from arithmetic data;
* establish that the counted coefficients represent the independent physical degeneracies rather than an index or overcomplete family;
* prove a new relation between charge-resolved degeneracies and gravitational observables.

A theorem that merely assumes the Cardy formula and substitutes the standard BTZ charge dictionary would be a useful derivation exercise, but not a new result in black-hole microstate counting.

19.2 A possible rigidity test

Suppose two candidate models have the same leading entropy,

\log d_1(N)

\alpha\sqrt N+o(\sqrt N),\log d_2(N)

\alpha\sqrt N+o(\sqrt N).

If their arithmetic structures differ, one can ask whether they necessarily disagree at some subleading order, or whether they can have identical asymptotic expansions while differing in exact degeneracies.

There is no universal answer. Distinct generating functions can share many asymptotic coefficients, and exact coefficient reconstruction depends on the class of functions and the information supplied. The research objective is to determine what arithmetic data, if any, make the entropy expansion rigid within a specified physical model class.

20. Limits of universality

The Bekenstein–Hawking area law is broadly applicable to semiclassical black holes, but the microscopic explanation need not be identical in every theory.

Different settings may have different:

* microscopic degrees of freedom;
* symmetry algebras;
* charge lattices;
* modular structures;
* ensembles and boundary conditions;
* protected indices versus absolute degeneracies;
* quantum corrections and zero-mode contributions.

Therefore, ABHM does not posit that a single generating function or modular form governs all black holes.

A more defensible hypothesis is:

In a specified class of quantum-gravitational models, exact arithmetic structure in a physically defined microscopic spectrum may determine the asymptotic degeneracies strongly enough to reproduce the black-hole entropy and constrain its corrections.

This claim can be tested model by model. Its success in one setting would not automatically establish it for another.

21. Research milestones

A credible program should proceed through milestones that separate mathematical achievement from physical interpretation.

* Milestone I — Exact finite model. Define a microscopic Hilbert space and charge operator with a directly verifiable degeneracy function. Establish the generating function and its exact coefficients.
* Milestone II — Arithmetic theorem. Prove the claimed product, recurrence, modular law, or coefficient identity. Identify which information determines the exact count.
* Milestone III — Controlled asymptotics. Derive the leading entropy and at least the first subleading term, including a stated domain of validity and error estimate.
* Milestone IV — Independent black-hole dictionary. Specify the gravitational solution and derive the relation between its charges, horizon area, and microscopic labels.
* Milestone V — Entropy and correction matching. Compare the microscopic count with the Bekenstein–Hawking term and the appropriate quantum corrections in the same ensemble.
* Milestone VI — Independence and dynamics. Verify that the counted states are physically independent and that the model has a defined dynamical structure beyond its state count.
* Milestone VII — Additional predictions. Derive and test at least one charge-dependent or dynamical consequence not used to tune the entropy match.

The earliest milestones can yield substantial mathematics. The later milestones are what elevate that mathematics into a credible black-hole microstate theory.

22. Final epistemic audit

Proposition	Status
Black-hole entropy is related semiclassically to horizon area	Established
Microcanonical entropy is the logarithm of the dimension of the counted physical state space	Established statistical mechanics
Some supersymmetric black holes admit microscopic state-counting derivations	Established in specified string-theory settings
Modular CFT state counts can reproduce entropy for particular black holes	Established in specified holographic regimes
Rademacher-type expansions can reconstruct coefficients of suitable modular objects	Established mathematics
Logarithmic corrections provide additional tests of microscopic entropy models	Established in multiple settings
Any integer degeneracy sequence with the right leading growth counts black-hole microstates	False as a general inference
Every black-hole microstate generating function must be modular	Not established
A universal arithmetic law uniquely determines all black-hole microstates	Not established
The conditional asymptotic matching theorem above proves the existence of a new physical model	No; it specifies the conditions a model must satisfy
A new model with independently defined states, dynamics, arithmetic structure, and geometric dictionary could yield a new entropy theorem	Open research target

The central distinction is between a valid counting identity and a physical explanation. The first may be exact and mathematically elegant; the second requires an independently justified account of what is being counted and why those states correspond to the black hole.

23. Conclusion: arithmetic must explain the count, not merely its growth

The Arithmetic of Black-Hole Microstates is built around a demanding principle: the microscopic states must be defined before their entropy can explain the horizon area.

An arithmetic generating function can encode an enormous degeneracy in a compact expression. Modular transformations can relate its behavior across the upper half-plane. Exact coefficient formulas can recover individual degeneracies, while asymptotic theorems can reveal the exponential growth that becomes entropy after taking a logarithm. These are powerful mathematical tools, and their application to black-hole physics has already produced important results.

But the physical explanation lies in the chain connecting those tools to a gravitational system:

\boxed{
\begin{gathered}
\text{microscopic Hilbert space}\\
\Downarrow\\
\text{physical constraints and dynamics}\\
\Downarrow\\
\text{exact charge-resolved degeneracies}\\
\Downarrow\\
\text{arithmetic and modular structure}\\
\Downarrow\\
\text{controlled entropy asymptotics}\\
\Downarrow\\
\text{independent gravitational charge dictionary}\\
\Downarrow\\
\text{Bekenstein–Hawking entropy and corrections}.
\end{gathered}
}

The proposed asymptotic matching theorem formalizes the final part of this chain. It shows exactly which mathematical statements are sufficient for the microcanonical entropy to reproduce the area law. It does not claim that those statements have been established for a new universal black-hole model.

The most important next step is to identify a specific microscopic system whose states and dynamics are independently defined, prove an exact counting identity for that system, derive its coefficient asymptotics, and establish the gravitational charge dictionary without fitting it to the desired entropy. A successful model should then reproduce not only the leading area term but also the logarithmic correction and additional charge-dependent properties wherever those quantities are independently known.

The decisive research question is therefore:

Can the arithmetic structure of an independently defined quantum-gravitational spectrum determine the black-hole entropy, including controlled subleading corrections, without inserting the horizon-area law into the microscopic count?

A positive answer in a new, well-defined class of black-hole systems would constitute genuine progress. A failure would be equally useful if it revealed that the proposed arithmetic structure is insufficient or that additional dynamical information is necessary.

The area law is the target. The microscopic count is the explanation. The arithmetic must connect them without confusing one for the other.

Selected references

1. Bekenstein, J. D. “Black Holes and Entropy.” Physical Review D 7 (1973): 2333–2346.

2. Hawking, S. W. “Particle Creation by Black Holes.” Communications in Mathematical Physics 43 (1975): 199–220.

3. Strominger, A., and Vafa, C. “Microscopic Origin of the Bekenstein-Hawking Entropy.” Physics Letters B 379 (1996): 99–104. arXiv:hep-th/9601029⁠￼.

4. Cardy, J. L. “Operator Content of Two-Dimensional Conformally Invariant Theories.” Nuclear Physics B 270 (1986): 186–204. Publisher record⁠￼.

5. Brown, J. D., and Henneaux, M. “Central Charges in the Canonical Realization of Asymptotic Symmetries: An Example from Three-Dimensional Gravity.” Communications in Mathematical Physics 104 (1986): 207–226.

6. Birmingham, D., and Sen, S. “Exact Black Hole Entropy Bound in Conformal Field Theory.” Physical Review D 63 (2001): 047501. Publisher record⁠￼.

7. Sen, A. “Logarithmic Corrections to N=2 Black Hole Entropy: An Infrared Window into the Microstates.” General Relativity and Gravitation 44 (2012): 1207–1266. arXiv:1108.3842⁠￼.

8. Pathak, A., Porfyriadis, A. P., Strominger, A., and Varela, O. “Logarithmic Corrections to Black Hole Entropy from Kerr/CFT.” Journal of High Energy Physics (2017), 090. arXiv:1612.04833⁠￼.

9. Iliesiu, L. V., Murthy, S., and Turiaci, G. J. “Revisiting the Logarithmic Corrections to the Black Hole Entropy.” Journal of High Energy Physics (2025), 058. Publisher record⁠￼.

10. Hardy, G. H., and Ramanujan, S. “Asymptotic Formulae in Combinatory Analysis.” Proceedings of the London Mathematical Society 17 (1918): 75–115.

11. Rademacher, H. “On the Partition Function .” Proceedings of the London Mathematical Society 43 (1937): 241–254.

12. Sasieta, M. “Interior Microstates and Black Hole Entropy.” Entropy 28 (2026): 408. Publisher record⁠￼.

The literature establishes important pieces of the arithmetic and microscopic-counting program. The remaining task for any new ABHM model is to establish its own physical state space, dynamics, exact counting identity, and independently derived gravitational dictionary—and then prove that the entropy agreement follows from them.

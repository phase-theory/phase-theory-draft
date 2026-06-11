# Quantum Field Theory on Curved Spacetime as an Incomplete Theory

## A Constructive Completion — Interacting Fields, an Intrinsic Local Stress–Energy Operator, and a Dynamical-Spacetime Framework Between QFT and General Relativity

---

## Abstract

Quantum field theory on curved spacetime (QFTCS), in the algebraic formulation developed by Wald and collaborators and validated by the Unruh and Hawking effects, is a mature theory of *free* fields on *fixed* globally hyperbolic backgrounds. As a physical theory it is incomplete in three respects: (i) interacting fields are nearly intractable beyond formal perturbation theory; (ii) the stress–energy tensor, the central observable coupling matter to geometry, is conventionally constructed by state-dependent subtractions and appears to demand new, state-dependent counterterms at every order; (iii) there is no satisfactory theory of quantum fields on *dynamical* spacetimes — the regime in which geometry responds to quantum matter without itself being fully quantized. This white paper develops a single coherent framework, **Dynamically Covariant Quantum Field Theory (DC–QFT)**, addressing all three.

For (i) we promote locally covariant perturbative algebraic QFT (pAQFT), Epstein–Glaser renormalization, and the operator product expansion (OPE) from computational tools to the *definition* of the interacting theory, and we formulate a constructive program (the "constructive triad") combining covariant flow equations, OPE associativity, and Euclidean–Lorentzian gluing.

For (ii) we prove — assembling and extending results of Wald, Hollands, Moretti, and Fewster — that the stress–energy tensor *is* a well-defined local and covariant quantum field: an operator-valued distribution affiliated with the enlarged Wick algebra, whose renormalization freedom is exhausted by a *finite, state-independent, universal* set of local curvature terms fixed once for all spacetimes and all orders of perturbation theory; the apparent state-dependence of counterterms is shown to be an artifact of normal ordering with respect to a state rather than the Hadamard parametrix. We give an intrinsic, background-independent characterization of $\mathbf{T}_{ab}$ through the OPE and through relative Cauchy evolution, and we elevate quantum energy inequalities to axioms.

For (iii) we formalize the intermediate regime — **semiclassical gravitational dynamics (SGD)** — as a constrained dynamical system for a triple $(\mathcal{M}, g, \omega)$: spacetime, metric, and quantum state, governed by a reduced-order semiclassical Einstein equation, supplemented by an Einstein–Langevin equation controlling fluctuations, with an initial-value formulation, quantitative validity criteria, and an explicit error budget locating SGD between QFTCS and quantum gravity. We state which results are established theorems, which are theorem schemas with proof strategies, and which are conjectures, and we close with falsifiable predictions and a ten-year research roadmap.

---

**Status convention.** Throughout, results are tagged:

- **[T: established]** — established in the literature (citation given)
- **[TS: theorem schema]** — a precise statement with a proof strategy we regard as within reach
- **[C: conjecture]** — a conjecture
- **[N: new in this paper]** — a definition, synthesis, or statement first formulated in this document

---

## Table of Contents

1. [Introduction: Three Incompletenesses of QFTCS](#1-introduction-three-incompletenesses-of-qftcs)
2. [Preliminaries: The Locally Covariant Framework](#2-preliminaries-the-locally-covariant-framework)
3. [Completion I: Interacting Quantum Fields on Curved Spacetime](#3-completion-i-interacting-quantum-fields-on-curved-spacetime)
4. [Completion II: The Stress–Energy Tensor as a Local Operator](#4-completion-ii-the-stressenergy-tensor-as-a-local-operator)
5. [Completion III: Quantum Fields in Dynamical Spacetimes — Semiclassical Gravitational Dynamics (SGD)](#5-completion-iii-quantum-fields-in-dynamical-spacetimes--semiclassical-gravitational-dynamics-sgd)
6. [Predictions, Tests, and Falsifiability](#6-predictions-tests-and-falsifiability)
7. [Research Roadmap and Concluding Assessment](#7-research-roadmap-and-concluding-assessment)
- [Appendix A: Hadamard Coefficients and the Conservation Anomaly](#appendix-a-hadamard-coefficients-and-the-conservation-anomaly)
- [Appendix B: The Four-Parameter Ambiguity is Exactly Four](#appendix-b-the-four-parameter-ambiguity-is-exactly-four)
- [Appendix C: Glossary for the Three Definitions of the Stress Tensor](#appendix-c-glossary-for-the-three-definitions-of-the-stress-tensor)
- [Appendix D: SGD Error Budget — Worked Schematic](#appendix-d-sgd-error-budget--worked-schematic)
- [References](#references)

---

# 1. Introduction: Three Incompletenesses of QFTCS

Quantum field theory on curved spacetime occupies a peculiar position in fundamental physics. It is responsible for the two most celebrated theoretical discoveries at the interface of quantum theory and gravitation — Hawking radiation [Hawking 1975] and the Unruh effect [Unruh 1976; Fulling 1973; Davies 1975] — and, through the theory of cosmological perturbations, for the only quantum-gravitational predictions that have plausibly been *observed* (the primordial power spectrum imprinted on the cosmic microwave background). In the algebraic formulation matured by Wald and collaborators [Wald 1994; Wald 2009; Hollands–Wald 2015], it possesses a degree of mathematical rigor unusual even by the standards of flat-space QFT: free fields on arbitrary globally hyperbolic spacetimes are under complete control, the class of physically admissible (Hadamard) states is sharply characterized, and the locally covariant framework of Brunetti–Fredenhagen–Verch [BFV 2003] elevates general covariance to a functorial principle.

And yet QFTCS, as it stands, is not a complete physical theory. We identify three structural incompletenesses, each of which this paper addresses with a concrete framework, and — where honestly possible — with theorems.

## 1.1 Incompleteness I: interactions

The free Klein–Gordon, Dirac, Maxwell and Proca fields on a globally hyperbolic spacetime $(\mathcal{M},g)$ are rigorously constructed objects. By contrast, an *interacting* field — even $\lambda\varphi^4$ — exists on curved spacetime only as a formal power series in the coupling. The obstructions are not merely technical:

**(a) No vacuum, no spectrum condition, no Wick rotation.** A generic curved spacetime has no timelike Killing field, hence no preferred vacuum, no energy positivity, no Osterwalder–Schrader reconstruction from a Euclidean section. The entire constructive arsenal of the 1970s [Glimm–Jaffe] is unavailable in its original form.

**(b) No momentum space.** Translation invariance is absent; renormalization must be performed in position space, locally and covariantly, so that counterterms at a point depend only on the metric and its derivatives at that point.

**(c) State-space ambiguity.** Even after the algebra of interacting fields is constructed, the selection of physically relevant states (the analogue of the interacting vacuum) is unresolved.

Section 3 develops our response: *the interacting theory should be defined, not approximated*, by the triple of (1) locally covariant Epstein–Glaser renormalization in the functional formalism of pAQFT [Brunetti–Fredenhagen 2000; Hollands–Wald 2001, 2002; Fredenhagen–Rejzner 2016], (2) the operator product expansion as the carrier of dynamical content [Hollands 2007; Hollands–Wald 2010], and (3) a constructive program — the **constructive triad** — combining Polchinski-type flow equations adapted to Lorentzian backgrounds [Duch], OPE associativity/recursion, and Euclidean–Lorentzian gluing on real-analytic and asymptotically static spacetimes. We prove convergence statements where they are available and state precisely what remains conjectural.

## 1.2 Incompleteness II: the stress–energy tensor

The stress–energy tensor $T_{ab}$ is the most important observable of QFTCS: it is the source in Einstein's equation, the generator of deformations of the dynamics, and the carrier of energy conditions. Yet the textbook presentation leaves the impression — widespread and, we shall argue, *incorrect in a precise sense* — that $T_{ab}$ is not well defined as a local operator and that its renormalization requires *new, state-dependent counterterms at every order*.

The origin of this impression is the historical "point-splitting" procedure: one computes $\langle \varphi(x)\varphi(x')\rangle_\omega$ in a state $\omega$, subtracts a divergent piece, and takes $x'\to x$. If the subtraction is taken to be the two-point function of a fiducial *state*, the subtraction is state-dependent, non-covariant, and must be re-engineered order by order in perturbation theory. The cure — known in principle since Wald's axioms [Wald 1977, 1978] and completed technically by the Hadamard parametrix subtraction [Moretti 2003; Hollands–Wald 2005; Décanini–Folacci 2008] and the Hollands–Wald uniqueness theorems [Hollands–Wald 2001, 2002] — is to subtract a *parametrix*, a purely local geometric object, not a state. What survives is a *finite-dimensional*, *state-independent* renormalization freedom consisting of conserved local curvature tensors.

Section 4 assembles this into a single theorem (Theorem 4.2) and then goes further, in three ways that we believe are new in emphasis or in substance:

**(a)** we *redefine* $\mathbf{T}_{ab}$ intrinsically — without reference to any state or parametrix — as the unique local covariant field appearing in a specified singular sector of the operator product expansion and, equivalently, as the generator of relative Cauchy evolution (Definitions 4.5 and 4.6), proving the equivalence of the three definitions for free fields and giving the proof schema for interacting fields;

**(b)** we explain, as a no-go result (Proposition 4.4), *why* a fully unique prescription is impossible — the residual c-number ambiguity is forced by locality and covariance and is the exact analogue of the renormalization-scheme ambiguity of flat-space QFT — and why this is a *feature* to be absorbed into gravitational couplings, not a pathology;

**(c)** we elevate quantum energy inequalities [Fewster–Eveson 1998; Fewster 2012] and the anomaly structure to *axioms* that cut down the residual freedom, and we show that in the interacting case the freedom remains finite-dimensional at every order, with *no state-dependence ever entering* (Theorem 4.8).

## 1.3 Incompleteness III: dynamical spacetimes

QFTCS is a theory of quantum fields on a *fixed* background. But the physical situations that motivate it — black hole evaporation, inflationary fluctuations, the chronology horizon — are precisely those in which the background is *not* fixed: the geometry responds to the quantum matter. The naive response, the semiclassical Einstein equation

$$G_{ab}[g] + \Lambda g_{ab} = 8\pi G\,\langle \mathbf{T}_{ab} \rangle_\omega , \tag{1.1}$$

is notoriously problematic: it is of fourth differential order in $g$ (the counterterms $I_{ab}, J_{ab}$ of Section 4 contain four derivatives of the metric), it admits runaway solutions [Horowitz–Wald 1978; Simon 1991; Flanagan–Wald 1996; Parker–Simon 1993], the right-hand side requires the state $\omega$ which itself lives on the solution spacetime (a fixed-point problem), and it discards fluctuations: $\langle T T\rangle - \langle T\rangle\langle T\rangle \neq 0$.

This regime — geometry dynamically sourced by quantum matter, with gravity itself treated classically or stochastically — is *not* quantum gravity. It is an autonomous layer of physical law, in the same sense that the Vlasov–Maxwell system is an autonomous layer between classical electrodynamics of point charges and QED. At present it has no satisfactory general treatment: existing results are either formal (stochastic gravity [Hu–Verdaguer 2008, 2020]), perturbative about highly symmetric backgrounds, or restricted to cosmology [Pinamonti 2011; Pinamonti–Siemssen 2015; Meda–Pinamonti–Siemssen 2021; Sanders 2022; Gottschalk–Siemssen 2021].

Section 5 formalizes this regime as **semiclassical gravitational dynamics (SGD)**: a constrained evolution problem for triples $(\mathcal{M},g,\omega)$, built on (1) a *reduced-order* semiclassical Einstein equation that eliminates runaways by construction (Definition 5.2), (2) a rigorous initial-value formulation with constraints, gauge structure, and a well-posedness theorem schema (Theorem 5.5), (3) the Einstein–Langevin equation as the first-order fluctuation theory with the noise kernel as a bona fide locally covariant bidistribution, and (4) sharp *validity criteria* — dimensionless functionals of $(\mathcal{M},g,\omega)$ whose smallness delimits the SGD regime from below (classical GR + QFTCS) and above (quantum gravity). We prove well-posedness in the cosmological sector by synthesizing the Pinamonti–Siemssen–Meda line of work, and we state the general case as a theorem schema with an explicit proof strategy.

## 1.4 The unifying structure

The three repairs are not independent. The logical spine of the paper is:

> **DC–QFT in one paragraph.** A quantum field theory is a functor $\mathcal{A}:\mathsf{Loc}\to\mathsf{Alg}$ from globally hyperbolic spacetimes to *-algebras (Brunetti–Fredenhagen–Verch), equipped with (i) a local S-matrix / time-ordered product structure satisfying the Hollands–Wald axioms, which *defines the interacting theory* to all orders with finite state-independent ambiguity (Sec. 3); (ii) a distinguished local field $\mathbf{T}_{ab}\in\mathcal{A}$, intrinsically characterized by the OPE and by relative Cauchy evolution, conserved, anomalous in a controlled way, satisfying quantum energy inequalities (Sec. 4); and (iii) a *back-reaction flow* on the space of triples $(\mathcal{M},g,\omega)$ generated by setting the reduced-order Einstein tensor equal to $8\pi G\,\omega(\mathbf{T}_{ab})$, with fluctuations governed by the induced Einstein–Langevin structure, valid precisely when the dimensionless SGD-criteria of Sec. 5 are small. The same object $\mathbf{T}_{ab}$ of (ii) is what makes (iii) well defined, and the functorial covariance of (i) is what makes the counterterm freedom of (ii) finite and state-independent.

## 1.5 Relation to prior work and claims of novelty

Nothing in physics is created *ex nihilo*. Our debt to the algebraic school — Wald, Kay, Fredenhagen, Brunetti, Hollands, Verch, Fewster, Moretti, Pinamonti, Rejzner, and their collaborators — is total and will be visible on every page. What we claim as contributions of this white paper are:

1. the **intrinsic OPE/RCE redefinition** of the stress–energy operator (Definitions 4.5, 4.6; Theorem 4.7) and the systematic refutation, in theorem form, of the "state-dependent counterterms at every order" folklore (Theorem 4.8);
2. the **constructive triad** for interacting QFTCS (Sec. 3.4) with the conditional convergence theorem 3.5;
3. the axiomatization of **semiclassical gravitational dynamics** as an autonomous theory with its own state space, dynamics, gauge structure, validity functionals and error budget (Axioms SGD1–SGD6, Sec. 5), including the reduced-order formulation and the fixed-point existence schema beyond cosmological symmetry;
4. a list of falsifiable consequences and internal consistency tests (Sec. 6) and a structured research roadmap (Sec. 7).

Where a statement is a synthesis of known results we say so; where it is new we tag it **[N]**; where it is open we tag it **[C]**. A physics white paper that blurs these lines does damage; we have tried not to.

---

# 2. Preliminaries: The Locally Covariant Framework

We fix conventions and recall, in compressed but precise form, the structures on which the rest of the paper is built. Experts may skim; the definitions of $\mathsf{Loc}$, Hadamard states, the Wick algebra $\mathcal{W}(\mathcal{M})$, and relative Cauchy evolution are used essentially later. Signature is $(-,+,+,+)$; units $\hbar=c=1$, with $G$ and $\ell_{\mathrm{P}}=\sqrt{G\hbar/c^3}$ kept explicit when dimensional analysis matters. $R^{a}{}_{bcd}$ and $R_{ab}=R^{c}{}_{acb}$ follow Wald [Wald 1984].

## 2.1 The category of backgrounds and the QFT functor

**Definition 2.1 (Background category $\mathsf{Loc}$) [T].** Objects of $\mathsf{Loc}$ are quadruples $\mathcal{M}=(M,g,\mathfrak{o},\mathfrak{t})$: a smooth four-manifold $M$ with metric $g$ such that $(M,g)$ is globally hyperbolic, with orientation $\mathfrak{o}$ and time-orientation $\mathfrak{t}$. Morphisms $\psi:\mathcal{M}_1\to\mathcal{M}_2$ are isometric embeddings preserving orientations whose image is causally convex in $\mathcal{M}_2$.

**Definition 2.2 (Locally covariant QFT [BFV 2003]) [T].** A locally covariant QFT is a functor $\mathcal{A}:\mathsf{Loc}\to\mathsf{Alg}$ into unital *-algebras (or C*-algebras), $\psi\mapsto\alpha_\psi$, satisfying:

(i) **Einstein causality**: if $\psi_1(\mathcal{M}_1)$ and $\psi_2(\mathcal{M}_2)$ are spacelike separated in $\mathcal{M}$, then $[\alpha_{\psi_1}(\mathcal{A}(\mathcal{M}_1)),\alpha_{\psi_2}(\mathcal{A}(\mathcal{M}_2))]=\{0\}$;

(ii) **Timeslice axiom**: if $\psi(\mathcal{M}_1)$ contains a Cauchy surface of $\mathcal{M}_2$, then $\alpha_\psi$ is an isomorphism.

A *locally covariant quantum field* $\Phi$ is a natural transformation from the functor of test sections to $\mathcal{A}$: a family $\Phi_\mathcal{M}: C^\infty_0(\mathcal{M})\to\mathcal{A}(\mathcal{M})$ with $\alpha_\psi\circ\Phi_{\mathcal{M}_1}=\Phi_{\mathcal{M}_2}\circ\psi_*$.

The timeslice axiom encodes the existence of dynamics; it is what allows the definition of *relative Cauchy evolution*, the central tool of Sections 4 and 5.

**Definition 2.3 (Relative Cauchy evolution [BFV 2003]) [T].** Let $\mathcal{M}=(M,g,\ldots)\in\mathsf{Loc}$ and let $h$ be a compactly supported symmetric tensor with $g+h$ still globally hyperbolic. Choose Cauchy surfaces $\Sigma^\pm$ to the future/past of $\mathrm{supp}\, h$ and let $\imath^{\pm}_{g}$, $\imath^{\pm}_{g+h}$ denote the corresponding neighborhood embeddings into $\mathcal{M}$ and $\mathcal{M}[h]:=(M,g+h,\ldots)$. The *relative Cauchy evolution* is the automorphism

$$\mathrm{rce}_\mathcal{M}[h] = \alpha_{\imath^-_{g}}\circ\alpha_{\imath^-_{g+h}}^{-1}\circ\alpha_{\imath^+_{g+h}}\circ\alpha_{\imath^+_{g}}^{-1} \in \mathrm{Aut}\bigl(\mathcal{A}(\mathcal{M})\bigr). \tag{2.1}$$

It measures the response of the theory to a compactly supported metric perturbation: "scatter the dynamics off the bump $h$."

## 2.2 Free fields, Hadamard states, microlocal spectrum condition

For the Klein–Gordon operator $P=\Box_g-m^2-\xi R$ on $\mathcal{M}\in\mathsf{Loc}$, global hyperbolicity yields unique retarded/advanced Green operators $E^{\pm}$ and the causal propagator $E=E^- - E^+$. The CCR algebra $\mathcal{A}(\mathcal{M})$ is generated by symbols $\varphi(f)$, $f\in C_0^\infty(M)$, with relations: linearity, $\varphi(Pf)=0$, $\varphi(f)^*=\varphi(\bar f)$, and $[\varphi(f),\varphi(f')]=\mathrm{i} E(f,f')\mathbf{1}$.

**Definition 2.4 (Hadamard state, microlocal form [Radzikowski 1996; BFK 1996]) [T].** A state $\omega$ on $\mathcal{A}(\mathcal{M})$ with two-point function $\omega_2\in\mathcal{D}'(M\times M)$ is *Hadamard* iff

$$\mathrm{WF}(\omega_2) = \Bigl\{(x,k;x',-k')\in T^*M^{\times 2}\setminus 0 \,:\, (x,k)\sim(x',k'),\ k\in \overline{V}{}^+_x\Bigr\},$$

where $(x,k)\sim(x',k')$ means the points are joined by a null geodesic to which $k$ is cotangent and $k'$ is its parallel transport, and $\overline{V}{}^+$ is the closed future light cone.

Radzikowski's theorem **[T]** establishes equivalence with the older Hadamard series form: locally,

$$\omega_2(x,x') = H_\ell(x,x') + w_\omega(x,x'), \qquad H_\ell(x,x')=\frac{1}{4\pi^2}\Bigl[\frac{\Delta^{1/2}(x,x')}{\sigma_\epsilon(x,x')} + v(x,x')\,\ln\frac{\sigma_\epsilon(x,x')}{\ell^2}\Bigr], \tag{2.2}$$

with $\sigma$ the signed squared geodesic distance (Synge's world function), $\Delta$ the van Vleck–Morette determinant, $v=\sum_n v_n \sigma^n$ determined *recursively and purely locally* by the Hadamard recursion relations (transport equations along geodesics), and $w_\omega$ *smooth*. All state dependence resides in the smooth remainder $w_\omega$; all singularities are carried by the universal, geometric parametrix $H_\ell$. The length scale $\ell$ in the logarithm is the unique genuine ambiguity of $H_\ell$ and will reappear as the renormalization scale of Section 4.

Three classical facts we use repeatedly **[T]**:

**(a)** Hadamard states exist on every globally hyperbolic spacetime (deformation argument of Fulling–Narcowich–Wald [FNW 1981]).

**(b)** Any two Hadamard states are locally quasi-equivalent; the set of Hadamard states is preserved under Cauchy evolution (propagation of the wavefront set, Hörmander).

**(c)** On stationary spacetimes, ground and KMS states are Hadamard; the Bunch–Davies state on de Sitter, the Unruh and Hartle–Hawking states on Schwarzschild (the latter on the eternal hole) are Hadamard, while the Boulware state fails at the horizon — the microlocal condition is doing physical work.

## 2.3 The enlarged Wick algebra

Products of fields at a point, $\varphi^2(x)$, $T_{ab}(x)$, do not live in the CCR algebra. The correct home is the *enlarged Wick algebra* $\mathcal{W}(\mathcal{M})$ of Hollands–Wald [Hollands–Wald 2001] (anticipated in [BF 2000; BFK 1996]): formally, the algebra generated by smeared Wick monomials ${:}\varphi^k{:}_{H}(f)$ *normal-ordered with respect to the Hadamard parametrix* (not a state), with product given by a Hadamard-type Wick theorem whose contractions use $H$; microlocal analysis (wavefront calculus) shows all products are well defined. Hadamard states extend continuously to $\mathcal{W}(\mathcal{M})$, and $\mathcal{W}$ is again a functor on $\mathsf{Loc}$. The notation ${:}\cdot{:}_H$ is canonical for this paper:

$$ {:}\varphi^2{:}_H(x) := \lim_{x'\to x}\bigl[\varphi(x)\varphi(x') - H_\ell(x,x')\,\mathbf{1}\bigr], \tag{2.3}$$

the limit existing as an operator-valued distribution on $\mathcal{W}(\mathcal{M})$ after smearing, because in any Hadamard state the difference has a smooth kernel. *No state was consulted in (2.3)*; this single displayed equation already contains the resolution of Incompleteness II in embryonic form.

## 2.4 Unruh and Hawking effects as theorems

For later use (validity tests of SGD, Sec. 5) we record the two benchmark results in their sharp forms.

**Theorem 2.5 (Unruh effect; Bisognano–Wichmann form) [T].** In the Minkowski vacuum, the restriction of the field algebra to a Rindler wedge $W$ is a KMS state at inverse temperature $2\pi$ with respect to the boost flow; a uniformly accelerated detector with proper acceleration $a$ coupled via a monopole interaction thermalizes at $T_U = a/2\pi$ ($= \hbar a / 2\pi c k_B$). [Unruh 1976; Bisognano–Wichmann 1976; Sewell 1982]

**Theorem 2.6 (Hawking effect, collapse form) [T].** Let $(\mathcal{M},g)$ describe the formation of a Schwarzschild black hole of mass $M$ by collapse, and let $\omega$ be any state that is vacuum-like at past null infinity and Hadamard across the horizon. Then at late retarded times the flux at future null infinity is thermal at $T_H = \kappa/2\pi = 1/8\pi GM$, with greybody factors given by the classical transmission coefficients. [Hawking 1975; Fredenhagen–Haag 1990; Dimock–Kay 1987]

The Fredenhagen–Haag derivation matters to us structurally: it shows that the Hawking flux is fixed by the *short-distance (Hadamard) structure of the state at the horizon*, i.e. by exactly the universal geometric data that Sections 4–5 place at the center of the theory. The robustness of $T_H$ is a robustness theorem for the Hadamard condition.

## 2.5 Notation table

| Symbol | Meaning |
|---|---|
| $\mathcal{M}=(M,g,\mathfrak o,\mathfrak t)$ | object of $\mathsf{Loc}$ |
| $E^\pm,\ E$ | retarded/advanced/causal propagators of $P=\Box-m^2-\xi R$ |
| $H_\ell$ | Hadamard parametrix at scale $\ell$, eq. (2.2) |
| $\mathcal{W}(\mathcal{M})$ | enlarged Wick algebra; ${:}\cdot{:}_H$ parametrix normal ordering |
| $\mathcal{F}_{\mathrm{loc}},\ \mathcal{F}_{\mu c}$ | local / microcausal functionals (Sec. 3) |
| $\star_H,\ \cdot_{T}$ | deformation-quantized product / time-ordered product |
| $T_n,\ \mathcal S$ | time-ordered products, local S-matrix |
| $\mathbf{T}_{ab}$, $\Theta_{ab}$ | quantum stress tensor; its classical kernel |
| $\mathrm{rce}_\mathcal{M}[h]$ | relative Cauchy evolution, Def. 2.3 |
| $N_{abc'd'}$ | noise kernel (Sec. 5) |
| $\varepsilon_{\mathrm{fluc}},\varepsilon_{\mathrm{grad}},\varepsilon_{\mathrm{P}},\varepsilon_{\mathrm{dec}}$ | SGD validity functionals, Def. 5.7 |

---

# 3. Completion I: Interacting Quantum Fields on Curved Spacetime

**Thesis.** The interacting theory on curved spacetime should not be regarded as "free QFTCS plus an intractable perturbation series." It should be *defined* by a finite list of axioms on time-ordered products — axioms that are known to admit solutions, unique up to a finite-dimensional, state-independent, local ambiguity at each order — and then *constructed* nonperturbatively by the constructive triad of Sec. 3.4. The first half of this program is a theorem; the second half is a program with partial theorems, and we are explicit about the boundary.

## 3.1 The functional/pAQFT formalism

Following Brunetti–Dütsch–Fredenhagen–Rejzner [Fredenhagen–Rejzner 2016; Rejzner 2016; BDF 2009], observables of the scalar theory are functionals $F:C^\infty(M)\to\mathbb{C}$ of the off-shell field configuration. Define:

- $\mathcal{F}_{\mathrm{loc}}$: local functionals $F(\phi)=\int_M \mathcal L(j_x^k\phi)\,\mathrm{d}\mathrm{vol}_g$;
- $\mathcal{F}_{\mu c}$: microcausal functionals, those whose functional derivatives $F^{(n)}(\phi)\in\mathcal{D}'(M^n)$ have wavefront sets avoiding the closed cones $\overline V^{+n}\cup\overline V^{-n}$.

On $\mathcal{F}_{\mu c}$ one defines the $\star_H$ product by deformation along the Hadamard bidistribution $H^+ := H + \tfrac{\mathrm{i}}{2}E$ (any choice of smooth-equivalent Hadamard $W$ gives an isomorphic algebra):

$$(F\star_H G)(\phi) = \sum_{n\ge 0}\frac{1}{n!}\Bigl\langle F^{(n)}(\phi),\, (H^+)^{\otimes n}\, G^{(n)}(\phi)\Bigr\rangle .$$

This reproduces $\mathcal{W}(\mathcal{M})$ of Sec. 2.3 **[T]**. The *time-ordered product* $\cdot_T$ is, formally, deformation along the Feynman parametrix $H_F=H+\tfrac{\mathrm{i}}{2}(E^-+E^+)$; it is well defined on regular functionals and *requires renormalization* on local ones — this is where all the difficulty of QFT lives, now sharply localized.

## 3.2 Axioms for time-ordered products; existence and uniqueness

**Axiom 3.1 (T1–T10, Hollands–Wald axioms for $T_n$) [T].** The multilinear maps $T_n:\mathcal{F}_{\mathrm{loc}}^{\otimes n}\to\mathcal{W}(\mathcal{M})$ shall satisfy:

- **T1** locality & covariance (naturality under $\mathsf{Loc}$-morphisms);
- **T2** scaling: poly-homogeneous behavior under $g\mapsto\lambda^2 g$, with at most logarithmic violations;
- **T3** microlocal spectrum condition for the total wavefront set;
- **T4** smooth/analytic dependence on the metric and parameters;
- **T5** symmetry;
- **T6** unitarity;
- **T7** causal factorization: $T_n(A_1\cdots A_n)=T_k(A_{i_1}\cdots)\star T_{n-k}(\cdots)$ when the first group's supports do not intersect the past of the second's;
- **T8** commutator/field equation axiom (Schwinger–Dyson);
- **T9** $T_1 =$ parametrix normal ordering on Wick monomials;
- **T10** action Ward identity: $T_n(\ldots,\tfrac{\delta S_0}{\delta\phi}\Psi,\ldots)$ consistent with the free equation of motion.

**Theorem 3.2 (Existence and uniqueness; Hollands–Wald [2001, 2002, 2005]) [T].** On every $\mathcal{M}\in\mathsf{Loc}$ there exist time-ordered products satisfying T1–T10 to all orders $n$. If $\{T_n\}$ and $\{\tilde T_n\}$ both satisfy the axioms, they are related by

$$\tilde T_n = T_n + \sum_{\text{partitions}} T_{<n}\circ\bigl(D_{k_1}\otimes\cdots\bigr),$$

where the $D_k:\mathcal{F}_{\mathrm{loc}}^{\otimes k}\to\mathcal{F}_{\mathrm{loc}}$ are *local, covariant, real, symmetric maps supported on the total diagonal*, given at each order by curvature polynomials of bounded scaling dimension. In particular: the renormalization ambiguity at every order is *finite-dimensional* and *state-independent*.

**Remark.** The proof proceeds by Epstein–Glaser induction in position space: causal factorization T7 determines $T_n$ on $M^n\setminus\Delta_n$ from lower orders; the inductive step is the *extension of a distribution to the diagonal* with prescribed scaling degree, performed covariantly via the curvature expansion at the diagonal of [Hollands–Wald 2002]. The Stora–Popineau / Epstein–Glaser splitting and Steinmann scaling-degree calculus replace momentum-space subtraction; no momentum space is ever needed. This is Incompleteness I(b) discharged.

**Definition 3.3 (The interacting theory) [T].** For $V\in\mathcal{F}_{\mathrm{loc}}$ (e.g. $V=\frac{\lambda}{4!}\int f\varphi^4$, with $f\in C_0^\infty$ an adiabatic cutoff), the local S-matrix and Bogoliubov's interacting fields are

$$\mathcal S(V) = \sum_{n\ge0}\frac{\mathrm{i}^n}{n!}T_n(V^{\otimes n}), \qquad F_{\mathrm{int}} = \mathcal S(V)^{-1}\star\frac{\mathrm{d}}{\mathrm{d}\tau}\Big|_{\tau=0}\mathcal S(V+\tau F) =: R_V(F).$$

The interacting algebra $\mathcal{A}_V(\mathcal{O})$ is generated by $\{R_V(F): \mathrm{supp}\, F\subset\mathcal{O}\}$. The *algebraic adiabatic limit* [BF 2000] **[T]** removes the cutoff $f\to1$ at the level of the algebra (not of states): for $\mathcal{O}$ fixed, changing $f$ outside a neighborhood of $J^-(\mathcal{O})\cap J^+(\Sigma)$ acts by inner automorphisms, so the net $\mathcal{O}\mapsto\mathcal{A}_V(\mathcal{O})$ is cutoff-independent. *The interacting theory exists as a net of \*-algebras on every globally hyperbolic spacetime, to all orders of formal perturbation theory.*

This already refutes the strongest form of intractability: there is no conceptual obstruction, no infrared catastrophe of principle, and no state-dependence in the construction. What remains open is *convergence/summability* and *state selection*, addressed next.

## 3.3 The operator product expansion as the carrier of dynamics

**Theorem 3.4 (Existence of OPE in perturbation theory; Hollands [2007]; Hollands–Kopper [2012]) [T].** In perturbatively constructed QFTCS, for every finite set of composite fields there exist OPE coefficients — distributions $C^{B}_{A_1\cdots A_k}(x_1,\ldots,x_k;y)$, locally and covariantly constructed from the metric, real-analytic in the coupling at each order — such that for any Hadamard state $\omega$ of the interacting theory,

$$\omega\bigl(A_1(x_1)\cdots A_k(x_k)\bigr) \sim \sum_{[B]\le\Delta} C^{B}_{A_1\cdots A_k}(x_1,\ldots,x_k;y)\;\omega\bigl(B(y)\bigr)$$

asymptotically as $x_i\to y$, to any prescribed scaling accuracy $\Delta$. In flat space the expansion converges at finite separation order by order in perturbation theory. Moreover the coefficients satisfy the *associativity/factorization* conditions when points merge at different rates.

**Remark (Why the OPE is the right backbone).** The OPE coefficients are (i) state-independent, (ii) local and covariant, (iii) determined by the dynamics, and (iv) sufficient to reconstruct all correlation functions of all composite fields once one-point functions $\omega(B(y))$ are known. Hollands–Wald propose, and we adopt, the view that *the OPE coefficient system IS the theory*; states are secondary data constrained by positivity and the microlocal condition. This inversion is what makes the intrinsic definition of $\mathbf{T}_{ab}$ in Sec. 4 possible, and what replaces "the vacuum" as the invariant content of the theory on backgrounds with no symmetry. It is the curved-spacetime analogue of the conformal-bootstrap inversion in CFT.

## 3.4 The constructive triad

We now state the nonperturbative program. It rests on three legs, chosen because each compensates a weakness of the others.

### Leg A: Lorentzian flow equations

Polchinski-type renormalization group flow equations have been adapted to Lorentzian signature and position space; Dütsch–Fredenhagen, Brunetti–Dütsch–Fredenhagen–Rejzner, and most relevantly Duch's rigorous treatment show that Epstein–Glaser renormalization is equivalent to a Wilsonian flow with a regulator that deforms $H^+$ at scale $\Lambda$ while preserving the microlocal spectrum condition. The flow equation for the effective interaction $V_\Lambda$,

$$\partial_\Lambda V_\Lambda = \frac{1}{2}\Bigl\langle \partial_\Lambda H^+_\Lambda,\; \frac{\delta^2 V_\Lambda}{\delta\phi^2}\Bigr\rangle - \frac{1}{2}\Bigl\langle \partial_\Lambda H^+_\Lambda,\; \frac{\delta V_\Lambda}{\delta\phi}\otimes\frac{\delta V_\Lambda}{\delta\phi}\Bigr\rangle, \tag{3.1}$$

is an ordinary differential equation in $\Lambda$ on a scale of Banach spaces of functional kernels with wavefront-set-adapted norms.

**Theorem 3.5 (Conditional convergence for $\varphi^4_3$-type models) [TS] [N].** Let $\mathcal{M}$ be a globally hyperbolic spacetime of bounded geometry (bounded curvature and derivatives, injectivity radius bounded below), and consider the $P(\varphi)_2$ or $\varphi^4_3$ interaction on $\mathcal{M}\times$(compact Cauchy data support). Suppose the regulated flow (3.1) is controlled by norms $\|F\|_{s,\delta} = \sup_n \delta^{-n}(n!)^{-s}\|F^{(n)}\|_{\mathrm{WF}}$ with $s<1$ on scale intervals $[\Lambda,2\Lambda]$, with constants depending only on the geometry bounds (this is the inductive hypothesis, established in the Euclidean analogues by Glimm–Jaffe and in the flow form by Duch in flat space). Then $V_{\Lambda\to0}$ exists, is unique given the finite renormalization conditions of Theorem 3.2, and the interacting net of Definition 3.3 is the Borel sum of its perturbation series in a neighborhood of $\lambda=0$.

**Proof strategy.** (1) Establish the scale-interval bounds on ultrastatic spacetimes of bounded geometry by transplanting the Euclidean cluster/phase-cell bounds through the Cauchy-data analyticity of Glimm–Jaffe and finite propagation speed; (2) use the deformation argument of [FNW 1981] to move from ultrastatic to general bounded-geometry $\mathcal{M}$, controlling the deformation by the timeslice axiom — the algebra "upstream" of the deformation region is isomorphic to the ultrastatic one; (3) Borel summability follows from the $s<1$ Gevrey bounds exactly as in flat-space $\varphi^4_3$ (Magnen–Sénéor). Steps (1) and (3) are adaptations of existing technology; step (2) is new but structurally identical to the existence proof for Hadamard states. The genuinely open point is uniformity of constants in step (1) under Lorentzian, rather than Euclidean, phase-cell decompositions; partial results in this direction exist for $P(\varphi)_2$ on static spacetimes. ∎

**Remark.** For four-dimensional $\varphi^4$ the flat-space theory is expected trivial in the continuum limit (Aizenman–Duminil-Copin **[T]**); the constructive target in $d=4$ is therefore asymptotically free or asymptotically safe matter (Yang–Mills, Gross–Neveu-type sectors), for which the triad is formulated but no convergence theorem is claimed **[C]**. We regard honest effective-field-theoretic semiconvergence — Borel summability with controlled remainder at scale $\Lambda_{\mathrm{cutoff}}$ — as the physically complete statement in $d=4$.

### Leg B: OPE bootstrap/recursion

Hollands' recursion expresses perturbations of OPE coefficients in the coupling through integrals of lower-order coefficients — a bootstrap that never mentions a state or a vacuum.

**Conjecture 3.6 (OPE reconstruction) [C].** Let $\{C^B_{A_1\cdots A_k}\}$ be a system of locally covariant distributions on a real-analytic $\mathcal{M}\in\mathsf{Loc}$ satisfying: (i) the associativity conditions; (ii) the microlocal spectrum condition; (iii) Hermitian conjugation and unit-operator relations; (iv) local commutativity in the germ sense; (v) a positivity condition: the Hermitian forms induced on coefficient spaces at asymptotically short distances are positive semidefinite. Then there exists a locally covariant QFT $\mathcal{A}$ on the sub-category of real-analytic spacetimes with a separating family of Hadamard states whose correlators have the prescribed OPE, unique up to net isomorphism.

Partial result **[T]**: in flat space, Hollands–Kopper convergence plus Wightman positivity reconstructs the perturbative theory; on analytic spacetimes the analytic microlocal condition of Strohmaier–Verch–Wollenberg provides the needed edge-of-the-wedge machinery. We consider Conjecture 3.6 the central structural open problem of interacting QFTCS, playing the role Osterwalder–Schrader reconstruction played in constructive QFT.

### Leg C: Euclidean–Lorentzian gluing

On spacetimes possessing a suitable analytic continuation (static, asymptotically static, or complex-metric backgrounds admissible in the sense of Kontsevich–Segal/Witten), construct the Euclidean interacting theory by reflection-positive functional integration, then continue. The Kontsevich–Segal allowability criterion $\sum_i |\arg \lambda_i| < \pi$ (on complex metric eigenvalues $\lambda_i$) delimits which complex sections may be used; this gives, for the first time, a principled domain for "Wick rotation" on curved backgrounds. Gluing supplies nonperturbative *anchor points* (e.g. interacting thermal states on the Euclidean Schwarzschild cigar, giving an interacting Hartle–Hawking state [Sanders 2015; Gérard 2018]) against which Legs A–B are calibrated.

**Proposition 3.7 (Division of labor) [N].** Leg A furnishes existence and quantitative control near $\lambda=0$ but is tied to bounded geometry; Leg B is background-blind and state-independent but presently lacks an existence theorem; Leg C is nonperturbative but tied to analyticity. The triad's consistency condition — that all three produce identical OPE coefficient systems where domains overlap — is a falsifiable internal test of the framework (Sec. 6, Test P5).

## 3.5 State selection for interacting fields

The free-field notion "Hadamard" generalizes: an interacting state is admissible iff its one-point functions $\omega(B(y))$ of all composite fields, inserted in the OPE, produce correlators satisfying the microlocal spectrum condition; equivalently, iff $\omega$ is in the folium generated from a free Hadamard state by the (cutoff) interacting dynamics. On stationary spacetimes, interacting KMS states exist order-by-order and, in the $P(\varphi)_2$ class, nonperturbatively [Fredenhagen–Lindner 2014]. On cosmological backgrounds, the states of low energy of Olbermann and their interacting deformations provide a workable preferred class **[T]**. We adopt:

**Axiom 3.8 (State admissibility, interacting) [N].** Admissible states of the interacting theory on $\mathcal{M}$ are exactly those normalized positive functionals on $\mathcal{A}_V(\mathcal{M})$ that are locally quasi-equivalent to Bogoliubov-induced Hadamard states and whose composite-field one-point functions are smooth. The set of admissible states is nonempty (by construction from free Hadamard states), closed under local operations, and preserved by relative Cauchy evolution.

With Axiom 3.8, Incompleteness I(c) is reduced from a conceptual gap to a classification problem. This completes the structural repair of Incompleteness I; quantitative control beyond Theorem 3.5 is roadmap material (Sec. 7, Milestones M1–M3).

---

# 4. Completion II: The Stress–Energy Tensor as a Local Operator

**Thesis.** The claim "the stress–energy tensor is not well defined as a local operator in QFTCS, and its renormalization requires new state-dependent counterterms at every order" is false as stated, and the precise sense in which it is false is itself a theorem. The correct statements are: (a) $\mathbf{T}_{ab}$ *is* a well-defined local, covariant operator-valued distribution on the enlarged Wick algebra; (b) its construction involves *no* state-dependent subtraction — the subtraction is the Hadamard *parametrix*, a purely geometric object; (c) the residual ambiguity is a *finite-dimensional, state-independent* space of local conserved curvature tensors, the same at every order of perturbation theory, absorbable into the gravitational couplings $(\Lambda, G, c_1, c_2)$; (d) what is genuinely impossible is a *canonically unique* prescription — and we prove this is forced, not pathological. We then give an *intrinsic redefinition* of $\mathbf{T}_{ab}$, independent even of the parametrix, via the OPE and via relative Cauchy evolution.

## 4.1 Diagnosis: where the folklore comes from

The classical stress tensor of the scalar field is

$$\Theta_{ab}[\phi] = \nabla_a\phi\nabla_b\phi - \tfrac12 g_{ab}\bigl(\nabla^c\phi\nabla_c\phi+m^2\phi^2\bigr) + \xi\bigl(g_{ab}\Box-\nabla_a\nabla_b - G_{ab}\bigr)\phi^2 .$$

Naively, $\mathbf{T}_{ab}={:}\Theta_{ab}[\varphi]{:}$ requires squaring an operator-valued distribution at a point. The historical procedure — normal-order with respect to a chosen "vacuum" state $\omega_0$:

$${:}\varphi^2{:}_{\omega_0}(x) := \lim_{x'\to x}\bigl[\varphi(x)\varphi(x')-\omega_0(\varphi(x)\varphi(x'))\mathbf{1}\bigr] \tag{4.1}$$

— is the source of all the folklore. Because $\omega_0$ does not exist canonically on a generic spacetime, and differs from spacetime to spacetime, (4.1) is (i) state-dependent by construction, (ii) not locally covariant — it violates the naturality of Definition 2.2, since $\omega_0$ on $\mathcal{M}$ does not restrict to $\omega_0$ on a sub-spacetime; and (iii) when carried into perturbation theory, requires re-subtraction against the (interacting, order-dependent) state at every order: the "new state-dependent counterterms at every order." The defect is in (4.1), not in $\mathbf{T}_{ab}$.

**Proposition 4.1 (No-go for state normal ordering; Hollands–Wald [2001]) [T].** There is no assignment $\mathcal{M}\mapsto\omega_0^\mathcal{M}$ of states such that (4.1) defines a locally covariant quantum field. Indeed, a locally covariant choice would, on Minkowski space, be invariant under all isometries of every subregion, forcing it to coincide with the Minkowski vacuum on every causal diamond, which is inconsistent (the Minkowski vacuum restricted to a diamond is a thermal-like (KMS) state, not the diamond's own "vacuum").

The repair replaces the state by the parametrix (2.2): $H_\ell$ is built from $\sigma$, $\Delta^{1/2}$, $v_n$ — functionals of the local geometry only, the same formula on every spacetime, restricting naturally to subregions.

## 4.2 The construction theorem

**Definition 4.2′ (Parametrix-renormalized stress tensor) [T].** On $\mathcal{M}\in\mathsf{Loc}$, define the operator-valued distribution $\mathbf{T}_{ab}\in\mathcal{W}(\mathcal{M})$ by point-split parametrix subtraction:

$$\mathbf{T}_{ab}(f) = \int_M f^{ab}(x)\,\lim_{x'\to x}\,\mathcal D_{ab}(x,x')\Bigl[\varphi(x)\varphi(x') - H_\ell(x,x')\,\mathbf{1}\Bigr]\mathrm{d}\mathrm{vol}_g + \int_M f^{ab}\,\Theta^{\mathrm{loc}}_{ab}\,\mathbf{1}\,\mathrm{d}\mathrm{vol}_g, \tag{4.2}$$

where $\mathcal D_{ab}(x,x')$ is the point-split form of the classical kernel $\Theta_{ab}$ (with primed derivatives parallel-transported), and $\Theta^{\mathrm{loc}}_{ab}$ is the unique local correction term (built from $v_1$) enforcing $\nabla^a\mathbf{T}_{ab}=0$, as determined by Moretti [2003].

**Theorem 4.2 (The stress tensor is a local covariant quantum field) [T] (synthesis).** $\mathbf{T}_{ab}$ as in (4.2) has the following properties.

1. **Existence as a local operator.** For each real $f^{ab}\in C_0^\infty$, $\mathbf{T}_{ab}(f)$ is a well-defined element of the enlarged Wick algebra $\mathcal{W}(\mathcal{M})$; in the GNS representation of any Hadamard state it is a symmetric operator with dense invariant domain (self-adjointness known for spatially smeared densities in static cases, expected generally **[C]**); its commutators with all smeared fields are finite and local.
2. **Local covariance.** $\mathcal{M}\mapsto\mathbf{T}_{ab}^\mathcal{M}$ is a natural transformation in the sense of Definition 2.2: the *same* construction on all spacetimes, compatible with causal embeddings.
3. **Covariant conservation.** $\nabla^a\mathbf{T}_{ab}=0$ exactly, as an operator equation [Moretti 2003].
4. **Hadamard expectation values.** For every Hadamard state $\omega$, $\omega(\mathbf{T}_{ab}(x))$ is a *smooth* tensor field given by the classical-looking formula applied to the smooth remainder $w_\omega = \omega_2 - H_\ell$: $\omega(\mathbf{T}_{ab}) = [\mathcal D_{ab} w_\omega]_{x'=x} + \Theta^{\mathrm{loc}}_{ab}$. State dependence enters *only* here, through $w_\omega$ — i.e. exactly where physics demands it (different states have different energy), never in the subtraction.
5. **Wald axioms.** It satisfies Wald's axioms [1977, 1978]: causality/locality; agreement of matrix elements between orthogonal one-particle states with the point-split formula; in Minkowski space, $\langle 0|\mathbf{T}_{ab}|0\rangle=0$ for a suitable choice of the finite renormalization; $\nabla^a\mathbf{T}_{ab}=0$.
6. **Uniqueness up to local curvature terms.** If $\tilde{\mathbf T}_{ab}$ is any other construction satisfying (1)–(5) and the Hollands–Wald scaling and analyticity requirements, then

$$\tilde{\mathbf T}_{ab} = \mathbf{T}_{ab} + \Bigl[\alpha\, m^4\, g_{ab} + \beta\, m^2\, G_{ab} + c_1\, I_{ab} + c_2\, J_{ab}\Bigr]\mathbf{1}, \tag{4.3}$$

with real constants $\alpha,\beta,c_1,c_2$ (functions of $\ell$ only through the trade-off $\ell\to\ell'$), where $I_{ab}=\frac{1}{\sqrt{-g}}\frac{\delta}{\delta g^{ab}}\int\sqrt{-g}\,R^2$ and $J_{ab}=\frac{1}{\sqrt{-g}}\frac{\delta}{\delta g^{ab}}\int\sqrt{-g}\,R_{cd}R^{cd}$ are the two independent conserved local curvature tensors of dimension four ($\Box R$- and Gauss–Bonnet-related redundancies removed). The ambiguity is a *four-parameter, state-independent, c-number* freedom — nothing more, on any spacetime, ever [Hollands–Wald 2001, 2005; Wald].

7. **Trace anomaly.** For the conformally coupled massless field, $g^{ab}\mathbf{T}_{ab} = \bigl(a\,E_4 + b\, C_{abcd}C^{abcd} + c\,\Box R\bigr)\mathbf{1}$ with the known coefficients; the anomaly is a theorem of the construction, not an input [Wald 1978; Duff 1994].

**Remark (What "well-defined local operator" does and does not mean).** $\mathbf{T}_{ab}(x)$ at a sharp point is not an operator — but neither is $\varphi(x)$ in *flat* space; both are operator-valued distributions, and by the Gårding–Wightman standards that is what "local operator" has always meant. The correct comparison is: $\mathbf{T}_{ab}$ on curved spacetime has exactly the same mathematical status as ${:}\varphi^4{:}$ in Minkowski space. The folklore conflates the (real) absence of a preferred *state* with a (nonexistent) absence of a preferred *operator*.

## 4.3 Why uniqueness fails, and why it must

**Proposition 4.4 (Forced ambiguity) [T] (Wald); formulation [N].** There is no prescription assigning to every $\mathcal{M}\in\mathsf{Loc}$ a conserved, locally covariant $\mathbf{T}_{ab}$ with correct scaling that is invariant under $\ell\to\lambda\ell$ rescalings of the parametrix logarithm: the logarithmic scaling violation $\partial_{\ln\ell}\,\mathbf{T}_{ab} = \frac{1}{16\pi^2}\bigl[\text{(local curvature tensor)}\bigr]\mathbf{1} \neq0$ is computable and nonzero whenever $v_1\neq0$. Hence the four-parameter freedom (4.3) cannot be reduced to zero by any local covariant convention; it can only be *fixed by experiment*, i.e. by measuring the effective gravitational couplings $(\Lambda_{\mathrm{eff}}, G_{\mathrm{eff}}, c_1, c_2)$ in

$$G_{ab}+\Lambda_{\mathrm{eff}}g_{ab}+c_1 I_{ab}+c_2 J_{ab} = 8\pi G_{\mathrm{eff}}\,\omega\bigl(\mathbf{T}^{(\ell_0)}_{ab}\bigr).$$

This is the precise curved-space analogue of the renormalization-scheme ambiguity of flat-space QFT ($\overline{\mathrm{MS}}$ vs. on-shell): nobody says the flat-space stress tensor "is not well defined" because $\mu$ must be chosen. The ambiguity is physical input, with finite content, located exactly in the gravitational action — where effective field theory says higher-curvature couplings live anyway.

## 4.4 The intrinsic redefinition: three equivalent characterizations

Definition 4.2′ still *mentions* the parametrix. We now redefine $\mathbf{T}_{ab}$ so that no auxiliary object appears at all: the stress tensor is pinned down by its position inside the algebraic skeleton of the theory. This is, to our knowledge, the first place the three characterizations are assembled as a single equivalence **[N]**.

**Definition 4.5 (OPE characterization) [N] (ingredients [T] from Hollands–Wald).** Let $\{C^B_{A_1 A_2}\}$ be the OPE system of the theory. Consider the product of two fundamental fields; its OPE has the universal form

$$\varphi(x)\varphi(x') \sim C^{\mathbf 1}(x,x')\,\mathbf{1} + C^{\varphi^2}(x,x')\,{:}\varphi^2{:}(y) + \cdots + C^{ab}(x,x')\,\mathbf{t}_{ab}(y) + \cdots,$$

where $\mathbf t_{ab}$ is the lowest-dimension symmetric 2-tensor field appearing. Define $\mathbf{T}_{ab}^{\mathrm{OPE}}$ as the *unique* (up to (4.3)) local covariant symmetric 2-tensor field $B$ in the OPE algebra such that: (i) $B$ appears in the $\varphi\times\varphi$ OPE at second order in geodesic separation ($[B]=4$); (ii) $\nabla^a B$ lies in the OPE ideal generated by the field equation; (iii) the charges $\int_\Sigma B_{ab}\,\zeta^a \mathrm{d}\Sigma^b$ implement, in the OPE coefficient system, the derivations induced by any Killing vector $\zeta$ where one exists; (iv) the $\mathbf 1$-coefficient normalization matches the free-field $C^{\mathbf 1}=H_\ell$ at leading singular orders (Hadamard normalization of the OPE).

**Definition 4.6 (RCE characterization) (ingredients [T] from BFV 2003; formulation as a definition [N]).** Define $\mathbf{T}_{ab}^{\mathrm{rce}}$ as the generator of relative Cauchy evolution: for $A\in\mathcal{W}(\mathcal{M})$ and compactly supported metric perturbations $h$,

$$\bigl[\mathbf{T}^{\mathrm{rce}}(h), A\bigr] := 2\mathrm{i}\,\frac{\mathrm{d}}{\mathrm{d} s}\Big|_{s=0} \mathrm{rce}_\mathcal{M}[s h](A), \qquad \mathbf{T}^{\mathrm{rce}}(h)\;\text{“}=\text{”} \int_M \mathbf{T}_{ab}\, h^{ab}\,\mathrm{d}\mathrm{vol}_g . \tag{4.4}$$

That the functional derivative of $\mathrm{rce}$ exists and is implemented by a symmetric tensor field was established for the free field in [BFV 2003] and for perturbative interacting fields by Brunetti–Fredenhagen–Rejzner [2016]. Equation (4.4) determines $\mathbf{T}^{\mathrm{rce}}$ up to central (c-number) terms — precisely the freedom (4.3).

**Theorem 4.7 (Trinity theorem for the stress tensor) [T] for free fields; [TS] for interacting fields [N].** For the free scalar field on any $\mathcal{M}\in\mathsf{Loc}$:

$$\mathbf{T}^{\mathrm{parametrix}}_{ab} \equiv \mathbf{T}^{\mathrm{OPE}}_{ab} \equiv \mathbf{T}^{\mathrm{rce}}_{ab} \pmod{\text{the ambiguity (4.3)}}.$$

*Proof.* (parametrix = RCE): direct computation of $\frac{\mathrm{d}}{\mathrm{d} s}\mathrm{rce}[sh]$ on generators using the perturbed propagators $E^\pm_{g+sh}$; the derivative acts by commutator with the point-split quadratic form whose kernel is $\mathcal D_{ab}[\varphi\varphi]$, and central terms are unconstrained — this is BFV Thm. 4.3 adapted. (parametrix = OPE): the free OPE is the Hadamard/Wick expansion; conditions (i)–(iv) of Definition 4.5 select the Wick square sector and fix the improvement terms; conservation (ii) fixes Moretti's $\Theta^{\mathrm{loc}}$ term up to (4.3). (Interacting case): RCE differentiability is [BFR 2016]; matching to the OPE tensor sector reduces, via Theorem 3.2, to a cohomological statement — that the local covariant conserved 2-tensor fields of dimension 4 modulo field-equation terms form exactly the space (4.3) plus $\Theta_{ab}$-multiples — which is the same finite classification used in the Hollands–Wald uniqueness proof. We assess the remaining gap (operator, not just expectation-value, matching at all perturbative orders) as technical. ∎

**Remark (Conceptual payoff).** Definition 4.6 says: *the stress tensor is the functional derivative of the dynamics with respect to the metric* — the exact quantum image of $T_{ab}=\frac{2}{\sqrt{-g}}\frac{\delta S_{\mathrm{matter}}}{\delta g^{ab}}$ — formulated without an action, without a path integral, without a parametrix, and without a state. This is the definition that survives into the dynamical-background regime of Sec. 5, because it is the definition that *couples*: the object sourcing geometry is, tautologically, the object measuring sensitivity to geometry.

## 4.5 The interacting stress tensor: state-independence at every order

**Theorem 4.8 (No state-dependent counterterms, to all orders) [T] (assembled from Hollands–Wald 2001, 2002, 2005); formulation [N].** Let the interacting theory be defined as in Definition 3.3 with interaction $V$, and define the interacting stress tensor by Bogoliubov's formula $\mathbf{T}_{ab}^{V} := R_V\bigl(\mathbf{T}_{ab} + g_{ab}\,\mathcal L_V\text{-terms}\bigr)$ with $T_n$ satisfying T1–T10 and the additional conservation Ward identity (which can be satisfied: the obstruction cohomology is trivial for scalar interactions [Hollands–Wald 2005]). Then, at every order $n$ in $\lambda$:

1. the counterterms required are local covariant curvature polynomials — elements of the finite-dimensional spaces $D_k$ of Theorem 3.2 — fixed once per order, identical for all spacetimes and *all states*;
2. $\nabla^a\mathbf{T}_{ab}^{V}=0$ holds as an operator identity in $\mathcal{A}_V(\mathcal{M})$;
3. the total renormalization freedom of $\mathbf{T}_{ab}^{V}$ remains a finite-parameter family: (4.3) plus reparametrizations of $(\lambda, m^2,\xi, Z)$ — i.e. precisely the freedom of the classical action extended by the four gravitational c-numbers;
4. for every admissible state $\omega$ (Axiom 3.8), $\omega(\mathbf{T}_{ab}^V(x))$ is smooth, and the map $\omega\mapsto\omega(\mathbf{T}_{ab}^V)$ is affine and continuous in the relevant topology — the state enters *linearly through expectation, never through renormalization*.

**Remark (Autopsy of the folklore) [N].** Where, then, did "new state-dependent counterterms at every order" come from? From three identifiable practices: (a) normal ordering w.r.t. a state, Proposition 4.1; (b) mode-sum/adiabatic regularization in cosmology, where subtractions are organized w.r.t. a particular vacuum family and *look* state-dependent though their covariant content is not; (c) "in–out" effective-action calculations, where the in/out vacua are states and their divergences mix with genuine counterterms. Each practice is a *gauge choice* on top of the invariant construction (4.2); the invariant content is Theorem 4.8. The theory was never sick; some of its coordinate systems were.

## 4.6 Constraints beyond construction: quantum energy inequalities and self-adjointness

**Theorem 4.9 (Quantum energy inequalities) [T] [Fewster–Eveson 1998; Fewster 2012; Fewster–Verch 2002].** For the free scalar field on $\mathcal{M}\in\mathsf{Loc}$, for every timelike worldline $\gamma$ and real $q\in C_0^\infty$, there is a finite, state-independent constant $\mathcal Q(\gamma,q;g)$, computable from the geometry and the parametrix, with

$$\int \mathrm{d}\tau\, q(\tau)^2\, \omega\bigl(\mathbf{T}_{ab} u^a u^b\bigr)(\gamma(\tau)) \ge -\,\mathcal Q(\gamma, q; g) \qquad\text{for all Hadamard }\omega .$$

Analogous bounds hold for Dirac and Maxwell fields; for interacting theories, QEIs hold in 2d CFTs and (in adiabatic regimes) for $P(\varphi)_2$ [Fewster–Hollands 2005; Bostelmann–Cadamuro–Fewster 2013].

**Axiom 4.10 (QEI axiom) [N].** In DC–QFT we *require* of the pair (theory, stress tensor) that worldline QEIs of the above form hold on the admissible state space, with $\mathcal Q$ locally covariant and scaling correctly. Within the four-parameter freedom (4.3) this is a nontrivial constraint linking $(c_1,c_2)$ to the matter content when combined with SGD stability (Sec. 5.7); together with the flat-space normalization $\langle0|\mathbf{T}_{ab}|0\rangle_{\mathrm{Mink}}=0$ (fixing $\alpha,\beta$ at $\ell=\ell_0$), it reduces the practical ambiguity to the two higher-curvature couplings that gravitational experiment bounds anyway ($|c_i|\lesssim 10^{61}$ from sub-millimeter tests; any $|c_i|\gtrsim 1$ is radiatively natural).

**Conjecture 4.11 (Self-adjointness) [C].** For every Hadamard state GNS representation and every real test density $f^{ab}$, the symmetric operator $\mathbf{T}_{ab}(f)$ is essentially self-adjoint on the Wick-polynomial core. (Known: free fields, spatial smearings on static spacetimes; quadratic forms always. Sanders' results on ${:}\varphi^2{:}$ [Sanders 2012] mark the frontier.)

**Summary of Completion II.** The stress–energy tensor is hereby (re)defined as the local covariant quantum field $\mathbf{T}_{ab}\in\mathcal{W}(\mathcal{M})$, equivalently characterized by parametrix subtraction (4.2), by its OPE position (Definition 4.5), and as the generator of relative Cauchy evolution (Definition 4.6); it is conserved, anomalous in the known controlled way, satisfies QEIs, carries a four-parameter state-independent c-number ambiguity absorbed into gravitational couplings, and in interacting theories renormalizes with state-independent local counterterms drawn from the same finite spaces at every order. It is, in every sense in which the phrase has meaning in quantum field theory, *a well-defined local operator*.

---

# 5. Completion III: Quantum Fields in Dynamical Spacetimes — Semiclassical Gravitational Dynamics (SGD)

**Thesis.** Between QFTCS (fixed background) and quantum gravity (quantized metric) lies an autonomous regime in which classical geometry is *dynamically driven* by quantum matter. We formalize it as a self-contained theory — **semiclassical gravitational dynamics** — with its own kinematics (a state space of triples), its own dynamics (a reduced-order semiclassical Einstein flow plus an Einstein–Langevin fluctuation layer), its own gauge structure, its own initial-value problem, and, crucially, its own *quantitatively delimited domain of validity*. The claim is not that SGD is fundamental; it is that SGD is a *theory* — closed, predictive, and falsifiable within its domain — in exactly the way Navier–Stokes is a theory though molecules exist.

## 5.1 Kinematics: the state space of the coupled system

**Definition 5.1 (SGD configurations) [N].** An *SGD configuration* is a triple $\mathcal C=(\mathcal{M}, g, \omega)$ where $(M,g)\in\mathsf{Loc}$, and $\omega$ is an admissible (Hadamard; in the interacting case Axiom 3.8) state on the DC–QFT matter net $\mathcal{A}(\mathcal{M})$ *constructed on that same* $(M,g)$. Two configurations are *gauge-equivalent* if related by an orientation-preserving diffeomorphism acting simultaneously on $g$ and (functorially, via $\mathcal{A}$) on $\omega$. The *SGD phase space* $\Gamma_{\mathrm{SGD}}$ is the space of gauge classes of Cauchy data $(\Sigma; h_{ij}, K_{ij}; \varpi)$ where $(h,K)$ are standard GR data and $\varpi$ is a state on the boundary (Cauchy-surface) algebra, subject to the constraints (5.3) below.

The essential subtlety — absent from both parent theories — is the *entanglement of the two sectors at the level of definitions*: the algebra on which $\omega$ lives depends on $g$. Functoriality (Definition 2.2) is what renders this circularity benign: a solution is a *fixed point* of the map (geometry → algebra → stress expectation → geometry), and the timeslice axiom transports states between infinitesimally neighboring metrics via relative Cauchy evolution — which is, by Theorem 4.7, generated by the very stress tensor doing the sourcing. The conceptual loop closes; this is why Completion II had to precede Completion III.

## 5.2 Dynamics I: the reduced-order semiclassical Einstein equation

The naive equation (1.1) is fourth-order in $g$ (through $I_{ab}$, $J_{ab}$) and possesses Ostrogradsky-type runaway solutions with Planck-frequency instabilities even around flat space [Horowitz–Wald 1978; Simon 1991; Flanagan–Wald 1996]. Following the logic of order reduction in effective field theory (Parker–Simon; cf. the Landau–Lifshitz treatment of radiation reaction), we *define* SGD by the reduced equation:

**Definition 5.2 (Reduced-order semiclassical Einstein flow) [N], building on [T] [Parker–Simon 1993; Flanagan–Wald 1996].** Fix the renormalization point: scale $\ell_0$, constants $(\Lambda, G)$ measured, $(c_1,c_2)$ given. The SGD field equation is

$$G_{ab}[g] + \Lambda g_{ab} = 8\pi G\;\omega\bigl(\mathbf{T}_{ab}[g]\bigr) - c_1\,\mathcal I_{ab}^{\mathrm{red}}[g,\omega] - c_2\,\mathcal J_{ab}^{\mathrm{red}}[g,\omega], \tag{5.1}$$

where $\mathcal I^{\mathrm{red}},\mathcal J^{\mathrm{red}}$ are the *order-reduced* curvature terms: $I_{ab}, J_{ab}$ evaluated with all second-and-higher time derivatives of curvature eliminated iteratively using the lower-order equation $G_{ab}+\Lambda g_{ab}=8\pi G\,\omega(\mathbf{T}_{ab})$ and its derivatives, truncated at first order in $(c_1, c_2, \hbar)$. The result is a system of *second differential order in time* for $g$, coupled to the state transport described below.

**Proposition 5.3 (Properties of order reduction) [T]/[N].** (i) Equation (5.1) has the same formal accuracy in $\hbar$ as (1.1): solutions differ at $O(\hbar^2)$, beyond the warrant of either equation. (ii) Its solution set contains no Planck-scale runaways: around Minkowski with $\omega$ the vacuum, the linearization is the ordinary massless spin-2 equation plus $O(\hbar)$-bounded corrections [Flanagan–Wald 1996]. (iii) Reduction commutes with the gauge action and preserves Bianchi-compatibility: $\nabla^a(\text{RHS})=0$ on shell by Theorem 4.2(3) and construction of the reduced terms. (iv) Reduction is the unique prescription, to this order, that is local, covariant, analytic in the couplings, and agrees with minimal coupling at $c_1{=}c_2{=}0$ **[N]** (proof: classify local covariant second-order reductions; the field-redefinition freedom $g\to g+\hbar(a R g + b\,\mathrm{Ric})$ exhausts the difference between any two).

**State transport.** Along a one-parameter family of metrics $g(s)$, the state is transported by infinitesimal relative Cauchy evolution: $\dot\omega = \omega\circ\frac{\mathrm{d}}{\mathrm{d} s}\mathrm{rce}[g(s)]$, which by Theorem 4.7 is generated by $\mathbf{T}_{ab}$ itself. Thus SGD is the *closed* system:

$$\boxed{\;G_{ab}[g]+\Lambda g_{ab} = 8\pi G\,\omega_s(\mathbf{T}_{ab}[g]) - c_i\,\mathcal X^{\mathrm{red}}_{ab}, \qquad \partial_s \omega_s = \tfrac{\mathrm{i}}{2}\,\omega_s\bigl([\,\mathbf{T}(\dot g\,),\;\cdot\;]\bigr).\;} \tag{5.2}$$

**Constraints.** Pulling (5.1) back to $\Sigma$ gives the SGD Hamiltonian and momentum constraints

$$\mathcal H[h,K] = 16\pi G\,\varpi\bigl(\mathbf{T}_{ab}\, n^a n^b\bigr) + O(c_i), \qquad \mathcal H_i[h,K] = -8\pi G\,\varpi\bigl(\mathbf{T}_{ab}\, n^a e^b_i\bigr) + O(c_i), \tag{5.3}$$

which are *conditions jointly on geometric data and the state*: not every pair $(h,K;\varpi)$ is an allowed beginning. The QEIs (Theorem 4.9) then bound how negative the effective energy density entering $\mathcal H$ can be — the first place quantum inequalities feed directly into geometric dynamics, with the known consequences (singularity-theorem extensions [Fewster–Kontou 2020; Fewster–Galloway 2011], wormhole/warp exclusions in the small-$G\hbar$ regime).

## 5.3 Well-posedness

**Theorem 5.4 (Cosmological sector) [T] [Pinamonti 2011; Pinamonti–Siemssen 2015; Meda–Pinamonti–Siemssen 2021; Gottschalk–Siemssen 2021; Sanders 2022].** For conformally/generally coupled free scalars in flat FLRW symmetry, the system (5.2) (in its symmetry-reduced form, with the state a homogeneous-isotropic Hadamard state and the dynamical variable the scale factor) admits: local existence and uniqueness of solutions for given initial data $(a,\dot a; \varpi)$ (Pinamonti–Siemssen; Meda–Pinamonti–Siemssen for general $\xi$ including the trace-anomaly-driven sector); global existence results and null big-bang asymptotics in classes of states (Gottschalk–Siemssen); and uniqueness/maximality statements (Sanders for $\xi=1/6$ with moment conditions). Order reduction selects the stable branch (e.g. discarding the Starobinsky-ghost branch while retaining the physical quasi-de-Sitter solutions at their consistent order).

**Theorem 5.5 (General well-posedness — schema) [TS] [N].** Let $(\Sigma; h, K; \varpi)$ satisfy (5.3), with $(h,K)$ in Sobolev class $H^{s}\times H^{s-1}$, $s>5/2$, and $\varpi$ a Hadamard state datum whose two-point Cauchy kernel lies within $H^{s'}$-bounded distance of a reference parametrix kernel. Then there exists $T>0$ and a unique-up-to-gauge SGD solution $(M,g,\omega)$ on $\Sigma\times[0,T)$, depending continuously on the data; $T$ is bounded below by inverse powers of the data norms and of $\varepsilon_{\mathrm{fluc}},\varepsilon_{\mathrm{grad}}$ (Definition 5.7).

**Proof strategy, and assessment.** Iterate the decoupled map: (1) given $g_n$, solve the linear QFT on $(M,g_n)$ and transport $\varpi$ by RCE to obtain $\omega_n$; standard Hadamard propagation gives tame estimates on $\omega_n(\mathbf{T}_{ab}[g_n])$ in terms of $g_n$-norms (the key technical input: *parametrix-difference estimates*, i.e. Lipschitz dependence of $H_\ell[g]$ and of $w_{\omega}$ on $g$ in Sobolev norms — established in the cosmological case by Meda–Pinamonti, in general a quantitative refinement of known smooth dependence [T]/[TS]); (2) solve the quasilinear hyperbolic system $G_{ab}[g_{n+1}]+\Lambda g_{n+1}=$ (source from step 1) in harmonic gauge — standard energy estimates, the source being one order smoother than the worst allowed by the iteration thanks to the conservation identity; (3) contract: the composed map is a contraction on a small time interval in $C^0([0,T];H^s)$ by the Lipschitz estimates of (1) and the gain of (2). Banach fixed point gives existence and uniqueness; gauge covariance follows from naturality of every ingredient. The single genuinely hard estimate is the Lipschitz dependence in (1) at the level of the *fourth* parametrix coefficient ($v_1$), which is where we locate the frontier; in symmetry-reduced settings it is precisely the estimate Meda–Pinamonti–Siemssen prove. We therefore present Theorem 5.5 as a schema whose cosmological instance is a theorem and whose general instance is, in our assessment, a finite-effort target (Roadmap M4). ∎

## 5.4 Dynamics II: fluctuations — the Einstein–Langevin layer

The mean-field equation (5.1) ignores $\Delta\mathbf{T}_{ab} := \mathbf{T}_{ab} - \omega(\mathbf{T}_{ab})\mathbf{1}$. The leading correction is captured by the *noise kernel*, which by Completion II is a well-defined, state-dependent but *counterterm-free* bidistribution:

$$N_{abc'd'}(x,x') = \tfrac12\,\omega\bigl(\{\Delta\mathbf{T}_{ab}(x), \Delta\mathbf T_{c'd'}(x')\}\bigr),$$

finite for Hadamard $\omega$ at $x\neq x'$, with a coincidence singularity of well-characterized degree — no new renormalization is needed beyond Sec. 4 **[T]** [Hu–Verdaguer 2008; Phillips–Hu 2001].

**Definition 5.6 (SGD fluctuation layer) [T] (form); [N] (status within SGD).** Linearize $g\to g+\gamma$ about an SGD solution. The metric fluctuation obeys the Einstein–Langevin equation

$$\mathcal E_{ab}^{(1)}[\gamma] = 8\pi G\,\Bigl(\omega\bigl(\mathbf{T}_{ab}^{(1)}[\gamma]\bigr)_{\mathrm{red}} + \xi_{ab}\Bigr), \qquad \mathbb E[\xi_{ab}(x)\,\xi_{c'd'}(x')] = N_{abc'd'}(x,x'), \quad \mathbb E[\xi]=0, \tag{5.4}$$

with $\mathcal E^{(1)}$ the linearized reduced-order operator and the dissipation kernel inside $\omega(\mathbf{T}^{(1)})$ related to $N$ by a fluctuation–dissipation relation in stationary states **[T]** [Hu–Verdaguer 2020]. Within SGD, (5.4) is *defined* as the second-cumulant truncation of the influence functional of the matter on the geometry; its solutions $\mathbb E[\gamma\gamma]$ reproduce the symmetrized two-point function of gravitons sourced by matter loops in the $1/N$ expansion **[T]** [Hu–Verdaguer 2008], which is the precise sense in which SGD's upper boundary touches quantum gravity.

**Interpretation discipline [N].** SGD treats (5.4) as a *stochastic effective description of decohered fluctuations*: it is valid only when the matter state's stress fluctuations decohere on timescales short compared to the back-reaction time (a condition expressible through the decoherence functional of the stress tensor and *checkable within SGD*). Where the matter state sustains macroscopic superpositions of stress distributions (Page–Geilker-type situations [Page–Geilker 1981]), the mean-field layer is declared *invalid* by the criteria below — SGD fails gracefully, by its own diagnostics, rather than predicting falsely.

## 5.5 The validity functionals: delimiting the regime

**Definition 5.7 (SGD validity functionals) [N].** For a configuration $(\mathcal{M},g,\omega)$ and a spacetime region $\mathcal{O}$ of characteristic curvature radius $L(\mathcal{O})$ (with $L^{-2}=\sup_\mathcal{O} \|\mathrm{Riem}\|^{1/2}$, together with state scales), define:

| Functional | Definition | Meaning |
|---|---|---|
| $\varepsilon_{\mathrm{P}}(\mathcal{O})$ | $\ell_{\mathrm{P}} / L(\mathcal{O})$ | Planckian curvature parameter |
| $\varepsilon_{\mathrm{fluc}}(\mathcal{O})$ | $\displaystyle\sup_{f}\frac{\bigl\|\omega\bigl((\Delta\mathbf{T}(f))^2\bigr)\bigr\|^{1/2}}{\bigl\|\omega(\mathbf{T}(f))\bigr\| + L^{-4} V_f}$ | relative stress fluctuation |
| $\varepsilon_{\mathrm{grad}}(\mathcal{O})$ | $L\,\bigl\|\nabla \ln \|\omega(\mathbf{T})\| \bigr\|_{C^0(\mathcal{O})}\cdot \lambda_\omega/L$ | state-gradient / adiabaticity |
| $\varepsilon_{\mathrm{dec}}(\mathcal{O})$ | $\tau_{\mathrm{dec}}(\mathcal{O})\,/\,\tau_{\mathrm{BR}}(\mathcal{O})$ | decoherence vs. back-reaction time |

where $f$ ranges over normalized sampling tensors supported in $\mathcal{O}$ at scales $\ge$ the matter correlation length $\lambda_\omega$, $V_f$ is the sampling 4-volume, $\tau_{\mathrm{dec}}$ is the stress-decoherence time and $\tau_{\mathrm{BR}} = (G\,\|\omega(\mathbf{T})\|)^{-1/2}$.

**Axiom 5.8 (Domain axiom SGD6) [N].** SGD claims validity on $\mathcal{O}$ iff

$$\max\{\varepsilon_{\mathrm{P}}^2,\;\varepsilon_{\mathrm{fluc}},\;\varepsilon_{\mathrm{grad}},\;\varepsilon_{\mathrm{dec}}\}\;\ll\;1,$$

with error bounds on any SGD prediction $\mathcal P$ of the schematic form $\delta\mathcal P/\mathcal P \lesssim C_1\varepsilon_{\mathrm{fluc}}^2|_{\text{beyond EL}} + C_2\,\varepsilon_{\mathrm{P}}^2 + C_3\,\varepsilon_{\mathrm{grad}}^2$, the first controlled by the Einstein–Langevin layer, the second by the unknown UV completion (quantum gravity), the third by state-preparation data. Below the domain (all $\varepsilon$'s negligible) SGD degenerates to QFTCS on the self-consistent background; above it ($\varepsilon_{\mathrm{P}}\to1$ or $\varepsilon_{\mathrm{fluc}}\to 1$ persistently) SGD abstains.

**Example 5.9 (Calibration on the benchmarks) [N].**

**(i) Evaporating solar-mass black hole:** near the horizon, $\varepsilon_{\mathrm{P}}\sim10^{-38}$, and $\varepsilon_{\mathrm{fluc}}$ is small for the Unruh state on horizon scales; SGD validates the adiabatic mass-loss picture $\dot M\sim -\hbar/G^2M^2$ for the entire macroscopic phase, while its own functionals blow up at $M\sim M_{\mathrm P}$ — the theory predicts the location of its own death, as a good effective theory must. (The information-flow question is deliberately outside: SGD computes $\omega(\mathbf{T}_{ab})$ and correlations on its domain and is agnostic about Planckian endpoint physics.)

**(ii) Slow-roll inflation:** $\varepsilon_{\mathrm{P}}\sim H/M_{\mathrm P}\lesssim10^{-5}$; the Einstein–Langevin layer *reproduces* the standard scalar/tensor power spectra in the decohered regime, embedding inflationary phenomenology inside SGD **[T]** (form) [Roura–Verdaguer 2008].

**(iii) Page–Geilker superposed mass:** $\varepsilon_{\mathrm{dec}}\gtrsim 1$ — SGD self-excludes, correctly.

## 5.6 Axiomatic summary of SGD

**Axioms SGD1–SGD6 [N].**

- **SGD1 (Kinematics).** States of the theory are gauge classes of constrained triples per Definition 5.1.
- **SGD2 (Matter sector).** Matter is a DC–QFT: a locally covariant net with time-ordered structure (Sec. 3) and distinguished stress field $\mathbf{T}_{ab}$ characterized by Theorem 4.7.
- **SGD3 (Mean dynamics).** Evolution is the reduced-order coupled flow (5.2), with constraints (5.3) preserved.
- **SGD4 (Fluctuation dynamics).** Decohered fluctuations obey the Einstein–Langevin layer (5.4) with noise kernel $N$; predictions carry the induced variances.
- **SGD5 (Energy conditions).** Admissible states satisfy the QEI axiom 4.10; consequently SGD inherits the quantum singularity theorems and exotic-geometry exclusions on its domain.
- **SGD6 (Domain).** Validity is self-diagnosed by Axiom 5.8; all SGD predictions are emitted with the error budget attached.

## 5.7 Stability, and the fixing of $(c_1,c_2)$

**Proposition 5.10 (Stability of flat space within SGD) [T] (core), [N] (formulation).** Minkowski space with the vacuum state is a solution of (5.2); its linearization within SGD has no exponentially growing modes for any $(c_1,c_2)$, because order reduction has removed the Ostrogradsky sector — in contrast to the unreduced equation, where flat space is unstable for generic $(c_1,c_2)$ [Horowitz–Wald 1978]. Residual $(c_1,c_2)$-dependence enters SGD observables only through curvature-squared terms, suppressed by $\varepsilon_{\mathrm{P}}^2$; consistency of the SGD expansion therefore *requires* treating $c_i$-terms perturbatively, and any phenomenology that hinges on them at $O(1)$ lies outside the domain. This resolves the long debate about semiclassical instabilities by *relocating* it: the instabilities are artifacts of taking the unreduced equation seriously beyond its accuracy.

## 5.8 What SGD is not

SGD is not quantum gravity: it assigns no amplitude to superpositions of geometries, no entropy to horizons beyond what matter states carry, and no prediction at $\varepsilon_{\mathrm P}\sim1$. It is also not "gravitating QFTCS rhetoric": it is a definite dynamical system — (5.2), (5.3), (5.4) — with an initial-value formulation, theorems in its symmetric sectors, a falsifiable benchmark suite (Sec. 6), and explicit ignorance bounds. Its relation to quantum gravity is that of a boundary layer: any UV completion must reduce to SGD where Axiom 5.8 holds — this *reduction requirement* is itself a nontrivial constraint we offer to quantum-gravity programs as a test (P7 below).

---

# 6. Predictions, Tests, and Falsifiability

A framework paper must say how it can fail. We list internal consistency tests (mathematical falsifiers: a theorem proved false kills the framework) and external tests (empirical falsifiers within the SGD domain).

## 6.1 Internal falsifiers

**P1. Trinity failure.** If, at some perturbative order for $\lambda\varphi^4$, the RCE generator and the OPE-characterized tensor field differ by a term *not* of the form (4.3) (plus field-equation terms), Theorem 4.7 fails and the intrinsic redefinition of $\mathbf{T}_{ab}$ collapses. This is checkable at $O(\lambda^2)$ by finite computation.

**P2. State-dependent counterterm discovery.** Exhibiting any admissible interaction and order at which the conservation Ward identity is obstructed by a non-removable, state-dependent local term would falsify Theorem 4.8. The cohomological argument of [Hollands–Wald 2005] says this cannot happen for scalars; gauge sectors at higher loops are the place to attack it.

**P3. QEI violation in an interacting model.** A rigorous interacting model (e.g. $P(\varphi)_2$ on a static spacetime) violating every QEI of the form in Theorem 4.9 (with state-independent bound) would falsify Axiom 4.10 as a general axiom. Current evidence (CFT₂, $P(\varphi)_2$ adiabatic regimes) is supportive but the nonperturbative $d=4$ question is genuinely open.

**P4. Cosmological well-posedness breakdown.** If the maximal SGD solutions of Theorem 5.4 generically terminate in finite proper time with all validity functionals small (a "mid-domain" breakdown), Axiom 5.8's error budget is wrong.

**P5. Triad inconsistency.** If flow-equation construction (Leg A) and Euclidean gluing (Leg C) yield *different* OPE coefficient systems for $\varphi^4_3$ on an ultrastatic spacetime where both converge, the constructive triad — hence our definition of the interacting theory — is internally inconsistent.

**P6. Reduction-scheme dependence.** If two admissible order reductions in Definition 5.2 yield SGD predictions differing at $O(\varepsilon_{\mathrm P}^0)$ for some observable in domain, Proposition 5.3(iv) is false and SGD is not well defined.

**P7. Quantum-gravity reduction test.** Any candidate quantum gravity (strings, LQG, asymptotic safety, causal sets) that, in the regime $\max\varepsilon\ll1$, fails to reproduce (5.2)–(5.4) with the *same* noise kernel $N$ is either wrong or SGD is; the comparison is sharp because $N$ is counterterm-free. (For $1/N$ matter this matching is already verified **[T]** [Hu–Verdaguer 2008].)

## 6.2 External (empirical) consequences

Within its domain SGD inherits and sharpens phenomenology:

**E1. Inflationary consistency.** SGD reproduces the standard single-field power spectra and predicts specific $O(\varepsilon_{\mathrm{fluc}})$ stochastic corrections to long-mode statistics (non-Gaussian tails from the Einstein–Langevin layer); these are correlated with, and bounded by, the validity functionals, giving a clean target: *any* detected primordial signal requiring $\varepsilon_{\mathrm{fluc}}\gtrsim1$ dynamics (e.g. certain strongly coupled spectator scenarios) lies outside SGD and would locate new physics above it.

**E2. Black-hole adiabatic phase.** SGD commits to the standard quasi-stationary evaporation law with computable greybody and backreaction corrections at relative order $\hbar/(GM^2)$; deviations at macroscopic $M$ (e.g. echoes, horizon-scale structure at $\varepsilon_{\mathrm P}\ll1$) would falsify the SGD domain axiom rather than merely surprise it.

**E3. Exotic geometry exclusion.** Macroscopic traversable wormholes, warp drives, and time machines require stress configurations violating the QEI-constrained constraints (5.3) on SGD's domain; observing one at $\varepsilon_{\mathrm P}\ll1$ falsifies SGD5.

**E4. Gravitationally induced decoherence/noise.** The Einstein–Langevin layer implies a minimum gravitational noise floor sourced by matter stress fluctuations, in principle relevant to optomechanical and atom-interferometric tests of semiclassical-vs-quantized gravity; SGD makes the *semiclassical side* of such experiments precise, so a confirmed gravity-mediated entanglement signal (which SGD cannot produce) would empirically locate the boundary $\varepsilon_{\mathrm{dec}}\sim1$ and falsify any claim that SGD is fundamental — exactly the kind of clean kill-condition an in-between theory should offer.

---

# 7. Research Roadmap and Concluding Assessment

## 7.1 Milestones (ordered by dependency, with effort estimates)

**M1 (1–2 yrs).** Complete the operator-level Trinity theorem (Theorem 4.7) for interacting fields at all perturbative orders: RCE differentiability ⟹ OPE tensor-sector matching via the cohomological classification. Deliverable: a uniqueness theorem making Definition 4.6 the standard definition of $\mathbf{T}_{ab}$.

**M2 (2–4 yrs).** Theorem 3.5 in full: Lorentzian phase-cell estimates for $P(\varphi)_2$ and $\varphi^4_3$ on bounded-geometry ultrastatic spacetimes; then the deformation step. First nonperturbative interacting QFT on a curved 4-manifold ($\varphi^4_3$ counts: 3 spacetime dimensions, curved).

**M3 (3–6 yrs).** OPE reconstruction (Conjecture 3.6) on analytic spacetimes — the curved-space Osterwalder–Schrader. Key tool: analytic microlocal edge-of-the-wedge plus Hollands–Kopper convergence transplanted by the analytic deformation trick.

**M4 (2–5 yrs).** Theorem 5.5 beyond symmetry: the parametrix-Lipschitz estimate in general Sobolev classes; local well-posedness of SGD in harmonic gauge for free matter, then order-by-order interacting matter.

**M5 (3–6 yrs).** QEIs for interacting fields in $d=4$ at the level of the OPE: derive QEI-type bounds directly from positivity of the OPE coefficient system (this would make Axiom 4.10 a theorem of DC–QFT and discharge P3).

**M6 (4–8 yrs).** SGD black-hole evaporation as a mathematical initial-value problem: spherically symmetric SGD with an Unruh-class state, proving the quasi-stationary mass-loss law with controlled errors until $\varepsilon_{\mathrm P}\sim1$ — the semiclassical evaporation theorem.

**M7 (continuous).** Numerical SGD: a code stack for (5.2) in symmetry-reduced and 3+1 settings (Hadamard subtraction implemented via the $v_n$ transport equations; state evolution by RCE discretization), validated against Theorem 5.4.

## 7.2 Concluding assessment

The three reputed incompletenesses of QFTCS have different statuses, and the honest summary is asymmetric:

- **Interactions (Completion I):** the *conceptual* problem is solved — the perturbative interacting theory exists on all globally hyperbolic spacetimes with finite state-independent ambiguity, and the OPE supplies an invariant, state-free notion of dynamical content. What is genuinely open is analysis, not principle: convergence, summability, and reconstruction. We have organized that analysis into a triad with identified hard estimates rather than a fog.

- **The stress tensor (Completion II):** the problem is, in our assessment, *solved*, and has been in essence since Hollands–Wald and Moretti; what was missing was the assembly, the intrinsic (OPE/RCE) redefinition freeing the object from the parametrix scaffolding, the no-go explaining the irreducible four parameters, and the explicit refutation of the state-dependent-counterterm folklore. $\mathbf{T}_{ab}$ is a local covariant quantum field, full stop.

- **Dynamical spacetimes (Completion III):** here the gap was real, and what we have provided is a *theory-shaped* object — axioms SGD1–SGD6, a closed evolution system, theorems in the cosmological sector, a schema with an identified key estimate in general, a fluctuation layer, and self-diagnosing validity — rather than a finished mathematical edifice. We regard SGD as the correct formalization target for the regime between QFT and GR, and its well-posedness program (M4, M6) as the most consequential open mathematics in gravitational physics short of quantum gravity itself.

If the twentieth century's lesson was that quantum field theory and general relativity are each non-negotiable, the present paper's claim is that the territory between them is not a no-man's-land but a country with laws — laws that can be written down, proved about, computed with, and falsified. We have tried to draw its map.

### Acknowledgments

This synthesis stands on the work of the algebraic QFT and semiclassical gravity communities cited throughout; errors of formulation, emphasis, and conjecture are the present document's alone.

---

# Appendix A: Hadamard Coefficients and the Conservation Anomaly

For $P=\Box-m^2-\xi R$ in $d=4$, with $\sigma(x,x')$ Synge's world function and $\Delta^{1/2}$ the van Vleck–Morette determinant, the Hadamard coefficients $v_n$ solve the transport equations

$$2\nabla^a\sigma\,\nabla_a v_{n+1} + \bigl(\Box\sigma + 2n - 2\bigr)v_{n+1} = -\,\frac{1}{n+1}\,P\,v_n, \qquad v_0 = -\tfrac12 P\,\Delta^{1/2}\big|_{\text{transported}},$$

along the geodesic from $x'$ to $x$; each $v_n[g](x,x')$ is a *local, covariant, analytic-in-$g$* functional — the technical fact underlying every state-independence claim in the main text. The diagonal value relevant to $\mathbf{T}_{ab}$:

$$[v_1] = \frac{1}{8}m^4 + \frac{1}{4}\Bigl(\xi-\tfrac16\Bigr)m^2 R + \frac{1}{8}\Bigl(\xi-\tfrac16\Bigr)^2R^2 - \frac{1}{24}\Bigl(\xi-\tfrac15\Bigr)\Box R + \frac{1}{720}\bigl(R_{abcd}R^{abcd} - R_{ab}R^{ab}\bigr).$$

Moretti's correction term in (4.2) is $\Theta^{\mathrm{loc}}_{ab} = \frac{1}{4\pi^2}\,[v_1]\,g_{ab}\cdot\frac{1}{3}$ (in the conventions of [Moretti 2003; Hollands–Wald 2005]); with it, $\nabla^a\mathbf{T}_{ab}=0$ exactly and the trace anomaly emerges as $g^{ab}\langle\mathbf{T}_{ab}\rangle_\omega = \frac{1}{4\pi^2}[v_1] - m^2\langle{:}\varphi^2{:}_H\rangle_\omega - \ldots$, reproducing for the conformal field ($m=0,\ \xi=\frac16$):

$$g^{ab}\mathbf{T}_{ab} = \frac{1}{2880\pi^2}\Bigl(C_{abcd}C^{abcd} + R_{ab}R^{ab} - \tfrac13 R^2 + \Box\text{-terms}\Bigr)\mathbf{1}.$$

# Appendix B: The Four-Parameter Ambiguity is Exactly Four

**Claim.** The space of symmetric, conserved, local covariant 2-tensors $U_{ab}[g]$, of mass dimension ≤ 4, depending analytically on $g$ and polynomially on $m^2$, scaling almost-homogeneously, is spanned by $\{m^4 g_{ab},\ m^2 G_{ab},\ I_{ab},\ J_{ab}\}$.

*Sketch.* Dimension counting allows $m^4 g_{ab}$, $m^2 g_{ab}R$-type terms, and four-derivative terms. Conservation eliminates $m^2(R_{ab}+\alpha Rg_{ab})$ except the Einstein combination. At dimension four, the local conserved tensors derive from variations of $\int\sqrt{-g}\,\{R^2, R_{ab}R^{ab}, R_{abcd}R^{abcd}, \Box R\}$; the Gauss–Bonnet density makes the Riemann-squared variation dependent (the $E_4$ variation vanishes in $d=4$), and the $\Box R$ variation is proportional to a combination already counted, leaving $I_{ab}, J_{ab}$. This classification is the kernel of the uniqueness proofs of [Hollands–Wald 2001; Wald] and of the interacting step in Theorem 4.7. ∎

# Appendix C: Glossary for the Three Definitions of the Stress Tensor

| Definition | Input data | Output | Ambiguity |
|---|---|---|---|
| Parametrix (Def. 4.2′) | local geometry ($\sigma,\Delta^{1/2},v_n$), scale $\ell$ | element of $\mathcal{W}(\mathcal{M})$ | $\alpha,\beta,c_1,c_2$ ($\ell$-trade) |
| OPE (Def. 4.5) | OPE coefficient system; no parametrix, no state | field label + coefficients | same four, via $C^{\mathbf 1}$ normalization |
| RCE (Def. 4.6) | the functor $\mathcal{A}$ and its dynamics; nothing else | derivation-valued distribution; operator mod center | central terms = same four |

The migration of the ambiguity to the same four-dimensional space in all three pictures is the content of the Trinity theorem; its *irreducibility* is Proposition 4.4.

# Appendix D: SGD Error Budget — Worked Schematic

For an SGD prediction $\mathcal P$ on region $\mathcal{O}$ (e.g. the quadrupole waveform correction from stress fluctuations of a matter cloud):

$$\mathcal P_{\mathrm{true}} = \mathcal P_{\mathrm{SGD}}\Bigl[1 + a_1\,\varepsilon_{\mathrm{fluc}}^2\big|_{>\mathrm{EL}} + a_2\,\varepsilon_{\mathrm P}^2 + a_3\,\varepsilon_{\mathrm{grad}}^2 + O(\varepsilon^3)\Bigr],$$

with: the $a_1$-term = third-and-higher stress cumulants beyond the Langevin truncation, estimable *within* DC–QFT from the OPE of $\mathbf{T}\mathbf{T}\mathbf{T}$; the $a_2$-term = unknown UV completion, *not* estimable within SGD — this is the declared ignorance, bounded only by the domain axiom; the $a_3$-term = state-preparation uncertainty, estimable from the data topology of Theorem 5.5. The discipline of attaching this budget to every output is what distinguishes SGD-as-theory from semiclassical gravity as folklore.

---

# References

1. S. W. Hawking, "Particle creation by black holes," *Commun. Math. Phys.* **43** (1975) 199–220.
2. W. G. Unruh, "Notes on black-hole evaporation," *Phys. Rev. D* **14** (1976) 870.
3. S. A. Fulling, "Nonuniqueness of canonical field quantization in Riemannian space-time," *Phys. Rev. D* **7** (1973) 2850; P. C. W. Davies, *J. Phys. A* **8** (1975) 609.
4. R. M. Wald, *Quantum Field Theory in Curved Spacetime and Black Hole Thermodynamics*, University of Chicago Press, 1994.
5. R. M. Wald, "The formulation of quantum field theory in curved spacetime," in *Einstein and the Changing Worldviews of Physics*, arXiv:0907.0416.
6. S. Hollands and R. M. Wald, "Quantum fields in curved spacetime," *Phys. Rept.* **574** (2015) 1–35.
7. R. Brunetti, K. Fredenhagen, R. Verch, "The generally covariant locality principle — A new paradigm for local quantum physics," *Commun. Math. Phys.* **237** (2003) 31–68.
8. J. Glimm and A. Jaffe, *Quantum Physics: A Functional Integral Point of View*, 2nd ed., Springer, 1987.
9. R. Brunetti and K. Fredenhagen, "Microlocal analysis and interacting quantum field theories: renormalization on physical backgrounds," *Commun. Math. Phys.* **208** (2000) 623–661.
10. S. Hollands and R. M. Wald, "Local Wick polynomials and time-ordered products of quantum fields in curved spacetime," *Commun. Math. Phys.* **223** (2001) 289–326.
11. S. Hollands and R. M. Wald, "Existence of local covariant time-ordered products of quantum fields in curved spacetime," *Commun. Math. Phys.* **231** (2002) 309–345.
12. S. Hollands and R. M. Wald, "Conservation of the stress tensor in perturbative interacting quantum field theory in curved spacetimes," *Rev. Math. Phys.* **17** (2005) 227–311.
13. K. Fredenhagen and K. Rejzner, "Quantum field theory on curved spacetimes: Axiomatic framework and examples," *J. Math. Phys.* **57** (2016) 031101.
14. K. Rejzner, *Perturbative Algebraic Quantum Field Theory*, Springer, 2016.
15. R. Brunetti, M. Dütsch, K. Fredenhagen, "Perturbative algebraic quantum field theory and the renormalization groups," *Adv. Theor. Math. Phys.* **13** (2009) 1541–1599.
16. S. Hollands, "The operator product expansion for perturbative quantum field theory in curved spacetime," *Commun. Math. Phys.* **273** (2007) 1–36.
17. S. Hollands and C. Kopper, "The operator product expansion converges in perturbative field theory," *Commun. Math. Phys.* **313** (2012) 257–290.
18. S. Hollands and R. M. Wald, "Quantum field theory in curved spacetime, the operator product expansion, and dark energy," *Gen. Rel. Grav.* **40** (2008) 2051–2059; "Axiomatic quantum field theory in curved spacetime," *Commun. Math. Phys.* **293** (2010) 85–125.
19. P. Duch, "Renormalization of singular elliptic stochastic PDEs using flow equation," arXiv:2201.05031; P. Duch, M. Gubinelli, P. Rinaldi, and related rigorous flow-equation work; M. Dütsch and K. Fredenhagen for the Lorentzian setting.
20. R. M. Wald, "The back reaction effect in particle creation in curved spacetime," *Commun. Math. Phys.* **54** (1977) 1–19.
21. R. M. Wald, "Trace anomaly of a conformally invariant quantum field in curved spacetime," *Phys. Rev. D* **17** (1978) 1477.
22. V. Moretti, "Comments on the stress-energy tensor operator in curved spacetime," *Commun. Math. Phys.* **232** (2003) 189–221.
23. Y. Décanini and A. Folacci, "Hadamard renormalization of the stress-energy tensor for a quantized scalar field in a general spacetime of arbitrary dimension," *Phys. Rev. D* **78** (2008) 044025.
24. C. J. Fewster and S. P. Eveson, "Bounds on negative energy densities in flat spacetime," *Phys. Rev. D* **58** (1998) 084010.
25. C. J. Fewster, "Lectures on quantum energy inequalities," arXiv:1208.5399.
26. C. J. Fewster and R. Verch, "A quantum weak energy inequality for Dirac fields in curved spacetime," *Commun. Math. Phys.* **225** (2002) 331–359.
27. G. T. Horowitz and R. M. Wald, "Dynamics of Einstein's equation modified by a higher-order derivative term," *Phys. Rev. D* **17** (1978) 414.
28. J. Z. Simon, "Higher-derivative Lagrangians, nonlocality, problems, and solutions," *Phys. Rev. D* **41** (1990) 3720; "The stability of flat space, semiclassical gravity, and higher derivatives," *Phys. Rev. D* **43** (1991) 3308.
29. É. É. Flanagan and R. M. Wald, "Does back reaction enforce the averaged null energy condition in semiclassical gravity?" *Phys. Rev. D* **54** (1996) 6233–6283.
30. L. Parker and J. Z. Simon, "Einstein equation with quantum corrections reduced to second order," *Phys. Rev. D* **47** (1993) 1339–1355.
31. B. L. Hu and E. Verdaguer, "Stochastic gravity: Theory and applications," *Living Rev. Rel.* **11** (2008) 3.
32. B. L. Hu and E. Verdaguer, *Semiclassical and Stochastic Gravity: Quantum Field Effects on Curved Spacetime*, Cambridge University Press, 2020.
33. N. Pinamonti, "On the initial conditions and solutions of the semiclassical Einstein equations in a cosmological scenario," *Commun. Math. Phys.* **305** (2011) 563–604.
34. N. Pinamonti and D. Siemssen, "Global existence of solutions of the semiclassical Einstein equation for cosmological spacetimes," *Commun. Math. Phys.* **334** (2015) 171–191.
35. P. Meda, N. Pinamonti, D. Siemssen, "Existence and uniqueness of solutions of the semiclassical Einstein equation in cosmological models," *Ann. Henri Poincaré* **22** (2021) 3965–4015.
36. K. Sanders, "Static symmetric solutions of the semi-classical Einstein–Klein–Gordon system," *Ann. Henri Poincaré* **23** (2022) 1321–1358.
37. H. Gottschalk and D. Siemssen, "The cosmological semiclassical Einstein equation as an infinite-dimensional dynamical system," *Ann. Henri Poincaré* **22** (2021) 3915–3964.
38. R. M. Wald, *General Relativity*, University of Chicago Press, 1984.
39. M. J. Radzikowski, "Micro-local approach to the Hadamard condition in quantum field theory on curved space-time," *Commun. Math. Phys.* **179** (1996) 529–553.
40. R. Brunetti, K. Fredenhagen, M. Köhler, "The microlocal spectrum condition and Wick polynomials of free fields on curved spacetimes," *Commun. Math. Phys.* **180** (1996) 633–652.
41. S. A. Fulling, F. J. Narcowich, R. M. Wald, "Singularity structure of the two-point function in quantum field theory in curved spacetime, II," *Ann. Phys.* **136** (1981) 243–272.
42. J. J. Bisognano and E. H. Wichmann, "On the duality condition for quantum fields," *J. Math. Phys.* **17** (1976) 303–321.
43. G. L. Sewell, "Quantum fields on manifolds: PCT and gravitationally induced thermal states," *Ann. Phys.* **141** (1982) 201–224.
44. K. Fredenhagen and R. Haag, "On the derivation of Hawking radiation associated with the formation of a black hole," *Commun. Math. Phys.* **127** (1990) 273–284.
45. J. Dimock and B. S. Kay, "Classical and quantum scattering theory for linear scalar fields on the Schwarzschild metric," *Ann. Phys.* **175** (1987) 366–426.
46. M. Kontsevich and G. Segal, "Wick rotation and the positivity of energy in quantum field theory," *Quart. J. Math.* **72** (2021) 673–699.
47. E. Witten, "A note on complex spacetime metrics," arXiv:2111.06514.
48. K. Sanders, "On the construction of Hartle–Hawking–Israel states across a static bifurcate Killing horizon," *Lett. Math. Phys.* **105** (2015) 575–640.
49. C. Gérard, "The Hartle–Hawking–Israel state on stationary black hole spacetimes," arXiv:1806.07645.
50. K. Fredenhagen and F. Lindner, "Construction of KMS states in perturbative QFT and renormalized Hamiltonian dynamics," *Commun. Math. Phys.* **332** (2014) 895–932.
51. J. Dimock, "$P(\varphi)_2$ models on static space-times," *Rev. Math. Phys.*; and constructive results on two-dimensional curved backgrounds.
52. C. Gérard, *Microlocal Analysis of Quantum Fields on Curved Spacetimes*, ESI Lectures, EMS, 2019.
53. R. Brunetti, K. Fredenhagen, K. Rejzner, "Quantum gravity from the point of view of locally covariant quantum field theory," *Commun. Math. Phys.* **345** (2016) 741–779.
54. M. J. Duff, "Twenty years of the Weyl anomaly," *Class. Quant. Grav.* **11** (1994) 1387–1404.
55. C. J. Fewster and S. Hollands, "Quantum energy inequalities in two-dimensional conformal field theory," *Rev. Math. Phys.* **17** (2005) 577–612.
56. H. Bostelmann, D. Cadamuro, C. J. Fewster, "Quantum energy inequality for the massive Ising model," *Phys. Rev. D* **88** (2013) 025019.
57. K. Sanders, "Essential self-adjointness of Wick squares in quasi-free Hadamard representations on curved spacetimes," *J. Math. Phys.* **53** (2012) 042502.
58. C. J. Fewster and E.-A. Kontou, "A new derivation of singularity theorems with weakened energy hypotheses," *Class. Quant. Grav.* **37** (2020) 065010.
59. C. J. Fewster and G. J. Galloway, "Singularity theorems from weakened energy hypotheses," *Class. Quant. Grav.* **28** (2011) 125009.
60. N. G. Phillips and B. L. Hu, "Noise kernel in stochastic gravity and stress energy bitensor of quantum fields in curved spacetimes," *Phys. Rev. D* **63** (2001) 104001.
61. D. N. Page and C. D. Geilker, "Indirect evidence for quantum gravity," *Phys. Rev. Lett.* **47** (1981) 979.
62. A. Roura and E. Verdaguer, "Cosmological perturbations from stochastic gravity," *Phys. Rev. D* **78** (2008) 064010.

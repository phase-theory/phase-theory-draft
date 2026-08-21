Photon Non-Paradox Theorem (PNPT)

0. Context and intent

This theorem formalizes why “photon paradoxes” (wave/particle duality, self-interference, delayed choice, collapse, “which-path” contradictions) do not arise within Phase Theory, LPST, or LST, and why any apparent paradox is a representational artifact of importing object-ontology into a phase-primitive framework.

⸻

1. Primitives and definitions

Definition 1 (Phase substrate)

Let \Phi denote the total physical state as a phase field / phase configuration on a substrate domain \mathcal{M} (spacetime may be emergent; \mathcal{M} can be taken as the effective domain used for predictions).

Definition 2 (Admissible configurations)

Let \mathcal{A}\subseteq \{\Phi\} be the set of admissible phase configurations, defined by the theory’s global constraints:
	•	Topological admissibility (allowed sector / winding / defect class),
	•	Coherence bounds (finite coherence length/time; allowable phase noise),
	•	Boundary consistency (compatibility with preparation and apparatus constraints).

Definition 3 (Phase action / consistency functional)

Let \mathcal{I}[\Phi]\ge 0 be a functional measuring global phase inconsistency (or equivalently, negative log weight), such that physical realizations concentrate on configurations minimizing \mathcal{I} subject to constraints:
\Phi_{\text{phys}} \in \arg\min_{\Phi\in \mathcal{A}} \mathcal{I}[\Phi].

Definition 4 (Photon event)

A “photon” is not an object but an equivalence class of phase excitations:
	•	A localized, metastable excitation [\Phi]_\gamma lying in a specified admissible sector,
	•	Capable of transporting a quantized exchange \hbar\omega as a consequence of sector quantization / boundary matching.

Formally: a photon is a label for a family \Gamma\subset\mathcal{A} of configurations whose restriction to the apparatus region produces a single quantized detection event.

Definition 5 (Detection event)

A detection event at detector D_k is a boundary satisfaction / termination condition:
E_k \equiv \{\Phi\in\mathcal{A} \;:\; \Phi \text{ satisfies } \mathcal{B}_k \text{ (detector matching) and terminates coherence in } D_k\}.

Definition 6 (Which-path predicate)

A “which-path” statement W is a predicate on \Phi requiring that the configuration factorize into mutually exclusive subdomains consistent with a definite path record:
W \equiv \{\Phi\in\mathcal{A}:\ \text{there exists a stable record selecting one path subdomain}\}.

⸻

2. The theorem

Theorem (Photon Non-Paradox Theorem)

In Phase Theory / LPST / LST, under Definitions 1–6:

For any experimental arrangement \mathcal{E} involving preparation \mathcal{P}, propagation region \mathcal{R}, and measurement boundary conditions \{\mathcal{B}_k\}, there exists no logically consistent set of predicates that simultaneously requires:
	1.	object-like photon trajectory identity,
	2.	phase-coherent global admissibility across \mathcal{R}, and
	3.	detection as a boundary termination event,
while preserving the admissibility constraints \mathcal{A}.

Therefore, any “photon paradox” is a contradiction introduced by adding non-primitive object predicates to a phase-primitive theory, not a contradiction in the theory’s physical content.

⸻

3. Proof sketch (constructive, phase-first)

Lemma 1 (No photon-object identity map)

There is no injective map
f:\Gamma \to \text{Trajectories}
that assigns each admissible “photon” phase class \Gamma a unique classical trajectory while preserving \mathcal{A}, because admissibility is global and generally non-factorizable across \mathcal{R}.

Reason: In interferometric geometries, admissible configurations are constrained by boundary conditions on both arms; attempting to assign a single-arm trajectory corresponds to restricting \Phi to a subset \mathcal{A}'\subset\mathcal{A} that is not closed under the consistency minimization, i.e. it generally increases \mathcal{I} and fails admissibility.

⸻

Lemma 2 (Which-path records are incompatible with interference sector)

If an apparatus introduces stable which-path records W, then the admissible set collapses to a decohered sector \mathcal{A}_W in which cross-terms (phase-linking constraints between arms) are disallowed by coherence bounds:
\mathcal{A}_W \cap \mathcal{A}_{\text{int}} = \varnothing,
where \mathcal{A}_{\text{int}} denotes the interference-admissible sector.

Interpretation: You don’t “destroy interference by observing”; you select a different admissible sector by adding record constraints.

⸻

Lemma 3 (Detection is boundary termination, not propagation collapse)

Detection E_k is a boundary condition satisfaction event: \Phi must match \mathcal{B}_k. There is no additional axiom of collapse; rather, post-detection states are conditioned on E_k:
\Phi \mid E_k.
This conditioning is not a physical discontinuity in \Phi’s ontology; it is a constraint update reflecting that coherence cannot extend past the termination boundary.

⸻

Lemma 4 (Delayed-choice is boundary reclassification, not retrocausality)

Changing measurement context alters the set of admissible boundaries \{\mathcal{B}_k\}, hence changes \mathcal{A} for the experiment as defined. The theory evaluates \Phi_{\text{phys}} by minimizing \mathcal{I} subject to the actual boundaries.

Thus, “paradoxical” narratives arise only if you assume the photon carried a pre-existing object property (“went left”) independent of boundaries—an assumption rejected by Definition 4.

⸻

Conclusion

Assume a “photon paradox” exists. Then one must jointly assert:
	•	(O) photon is an object with a definite path predicate W,
	•	(I) interference sector admissibility \mathcal{A}_{\text{int}},
	•	(D) detection as termination conditioning E_k without collapse.

By Lemma 2, W implies \Phi \in \mathcal{A}_W and \mathcal{A}_W \cap \mathcal{A}_{\text{int}}=\varnothing, contradicting (I). Therefore, the paradox arises from adding (O), an illicit predicate in a phase-primitive theory.

Hence no photon paradox exists within the theory; it exists only in a mixed ontology.

\blacksquare

⸻

4. Corollaries (how this “explains the classics”)

Corollary 1 (Wave/particle duality is a false dichotomy)

“Wave” = phase coherence constraints; “particle” = boundary termination quantization. They are not competing ontologies, but different aspects of admissible phase dynamics.

Corollary 2 (Self-interference is global admissibility, not self-action)

A “single photon interfering with itself” is re-described as: configurations in \mathcal{A}_{\text{int}} are globally constrained by the full geometry; there is no indivisible object to be in two places.

Corollary 3 (Complementarity is sector exclusivity)

Which-path and interference correspond to disjoint admissible sets, not mutually exclusive “properties” of a thing.

Corollary 4 (No collapse postulate needed)

Conditioning on E_k suffices; collapse is an interpretive overlay from non-primitive wavefunction ontology.

⸻

5. Compact statement (paper-ready)

Photon Non-Paradox Theorem.
In phase-primitive frameworks (Phase Theory, LPST, LST), a photon is an equivalence class of admissible phase excitations rather than an object. Interference arises from global phase admissibility; detection is quantized boundary termination; and which-path information corresponds to additional record constraints selecting a decohered admissible sector. Since interference-admissible and record-admissible sectors are disjoint, the standard “photon paradoxes” result only from illicitly importing object-trajectory predicates into a phase-first ontology. Therefore no intrinsic photon paradox exists within these theories.

⸻

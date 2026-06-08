The S-Matrix Bootstrap and the Viability of a Non-Perturbative Theory of the Strong Force Without Quantum Fields

White Paper
June 8, 2026

---

Abstract

In the 1960s, Geoffrey Chew, Stanley Mandelstam, and others launched the S-matrix bootstrap program: a radical attempt to construct a complete theory of hadronic interactions using only the principles of analyticity, unitarity, and crossing symmetry. No Lagrangian, no quantum fields, no microscopic constituents—only the physical S-matrix was admissible. The program generated deep insights—Regge trajectories, duality, finite-energy sum rules, and the Veneziano amplitude—yet it was effectively abandoned after the rise of quantum chromodynamics (QCD). This white paper re-examines whether a complete non-perturbative S-matrix theory of the strong force is logically and mathematically consistent without QCD as an underlying field-theoretic scaffolding. We argue that the bootstrap was not refuted by QCD; it was displaced by a technically more tractable framework that answered pressing phenomenological questions faster. Modern developments—the amplituhedron, the conformal bootstrap, and the understanding of string theory as a consistent S-matrix theory—demonstrate that the original vision of a self-determining S-matrix is alive and well. We conclude that a complete non-perturbative S-matrix theory of the strong force is indeed consistent, but that the historical program’s technical assumptions were too restrictive, and the uniqueness it sought is not a requirement for physical viability. The bootstrap was not wrong; it was an unfinished symphony.

---

1. Introduction

Quantum field theory (QFT) has been the dominant language of particle physics since the quantization of electrodynamics. Yet by the early 1960s, field theory seemed powerless in the face of the strong nuclear force. The proliferation of hadrons, the apparent absence of a small coupling constant, and the failure of perturbative expansions drove a number of leading theorists to seek an alternative foundation. The S-matrix bootstrap, championed by Geoffrey Chew, proposed a radical departure: dispense with fields, Lagrangians, and even spacetime in the small, and instead construct the theory directly in terms of on-shell scattering amplitudes constrained only by the most general and rigorous principles of quantum mechanics and relativity.

For over a decade, the bootstrap program dominated the theory of strong interactions. It discovered Regge poles, realized the profound implications of crossing symmetry, and gave birth to dual resonance models—the direct ancestors of modern string theory. Yet by the mid-1970s, QCD, with its partonic constituents and asymptotic freedom, had swept the field. The bootstrap was largely set aside, often caricatured as a failed philosophical dogma. This white paper asks a question that has lingered unasked for five decades: If history had taken a different turn, could a complete non-perturbative S-matrix theory of the strong force have succeeded without QCD as scaffolding?

We will show that the answer is a qualified but firm yes. The original bootstrap was not wrong in its core insight; it was unfinished, technically overconstrained, and ultimately outcompeted by an extremely successful field theory. But the physical content of a self-consistent S-matrix theory of hadrons is not only consistent—it is realized in the very string theories that the bootstrap inadvertently spawned. Moreover, modern amplitude programs, from the amplituhedron in \mathcal{N}=4 SYM to the numerical S-matrix bootstrap, vindicate the idea that physical observables can be determined entirely by unitarity, analyticity, and symmetry, with no reference to an off-shell formulation.

---

2. Historical Genesis of the S-Matrix Bootstrap

The S-matrix bootstrap emerged from a deep dissatisfaction with Lagrangian quantum field theory. In the 1950s, renormalized QED was a triumph, but attempts to apply similar methods to meson-nucleon interactions encountered a seemingly insurmountable problem: the coupling was large, and there was no indication of a manageable perturbation expansion. The proliferation of strongly interacting particles—pions, kaons, nucleons, hyperons, and a growing zoo of resonances—suggested that none was more elementary than another. Chew’s “nuclear democracy” proposed that every hadron is a bound state of others, generated self-consistently by the exchange of the same particles that appear as bound states.

In this picture, the S-matrix—the unitary operator connecting asymptotic initial and final states—was the only legitimate observable. Field operators, local commutativity, and off-shell Green’s functions were deemed unphysical, a classical prejudice inherited from electrodynamics. The bootstrap program aimed to determine the entire S-matrix from a set of general axioms:

1. Unitarity – S^\dagger S = 1, which implies non-linear relations between amplitudes, in particular that the imaginary part of a forward amplitude equals a sum over all possible intermediate states.
2. Analyticity – The amplitude is the boundary value of an analytic function of the Mandelstam invariants, with singularities only dictated by unitarity (thresholds, poles at bound states and resonances). The crucial assumption was the Mandelstam representation, positing that double dispersion relations hold in all channels.
3. Crossing symmetry – The same analytic function describes all three channels (s, t, u) related by particle–antiparticle exchange. This is a direct consequence of local field theory, but in the bootstrap it was elevated to an independent postulate.

To these, one added the principle of maximal analyticity—that the amplitude has no singularities beyond those required by unitarity. The goal was to find self-consistent solutions: amplitudes that, when inserted into the unitarity relations, reproduced their own singularities, including bound-state poles on the Regge trajectories.

---

3. Core Principles: Analyticity, Unitarity, and Crossing

At the technical heart of the bootstrap were the Mandelstam double dispersion relations. For a process like \pi\pi \to \pi\pi, the amplitude A(s,t,u) was expressed as a sum of single- and double-dispersion integrals:

A(s,t) = \frac{1}{\pi}\int \frac{ds' \, \rho_s(s')}{s'-s} + \frac{1}{\pi}\int \frac{dt' \, \rho_t(t')}{t'-t} + \frac{1}{\pi^2}\iint \frac{ds' dt' \, \sigma(s',t')}{(s'-s)(t'-t)} + \text{subtractions},

with similar terms for the u-channel. The spectral functions \rho_s, \rho_t, and the double-spectral density \sigma were determined by elastic and inelastic unitarity in the three channels. For example, in the s-channel physical region, the unitarity condition for the partial-wave amplitude f_\ell(s) gives

\operatorname{Im} f_\ell(s) = \sqrt{\frac{s-4m^2}{s}} \, |f_\ell(s)|^2 + \text{inelastic contributions}.

This non-linear constraint ties the low-energy spectrum to the high-energy behavior. The bootstrap program attempted to solve these equations with the input that the force in a given channel is generated by the exchange of resonances and Regge trajectories in the crossed channels. The “strip approximation” kept only the nearest singularities in the double-dispersion relation, leading to a closed set of equations for the widths and masses of resonances.

The program achieved notable qualitative successes. The \rho meson emerged as a self-consistent resonance in \pi\pi scattering, with mass and width roughly in agreement with experiment. Regge trajectories, which summarize infinite families of resonances, appeared naturally from the analytic continuation of partial-wave amplitudes to complex angular momentum. The bootstrap framework explained why mesons and baryons lie on linear Regge trajectories and why the high-energy behavior of cross sections is governed by the leading Regge pole exchange.

---

4. The Bootstrap Equations and Hadronic Spectrum

The most concrete implementation of the bootstrap was the narrow resonance approximation, later formalized through duality and finite energy sum rules (FESR). The idea was that the sum of s-channel resonances reproduces the smooth high-energy Regge behavior from crossed channels, and vice versa. This led to the celebrated Veneziano amplitude in 1968:

A(s,t) = \frac{\Gamma(-\alpha(s)) \Gamma(-\alpha(t))}{\Gamma(-\alpha(s)-\alpha(t))},

which satisfies crossing symmetry, has only poles on linear Regge trajectories \alpha(s) = \alpha_0 + \alpha' s, and exhibits Regge asymptotics. The Veneziano amplitude was the first concrete realization of a completely crossing-symmetric, Regge-behaved S-matrix. It was the bootstrap’s greatest triumph—an explicit function that satisfied all the postulates exactly, at tree level. Its generalization to multi-particle amplitudes gave birth to dual resonance models, which we now interpret as the scattering of strings.

The physical content of the bootstrap at this stage was clear: a self-consistent S-matrix of the strong force would necessarily contain an infinite spectrum of particles lying on linear trajectories, with interactions that obey duality. The spectrum and couplings were largely determined, up to a few parameters (the slope \alpha' and intercepts). This looked remarkably like the real hadronic world.

Yet the bootstrap never succeeded in producing a fully consistent, unitary amplitude at the loop level. The narrow resonance approximation was a tree-level concept; unitarity corrections (Regge cuts, absorption) were difficult to incorporate while preserving crossing. The program’s equations became technically intractable.

---

5. The Challenge of the Pomeron and Rising Cross Sections

The most stubborn obstacle for the bootstrap was the Pomeron—the vacuum Regge pole responsible for the near-constant behavior of total hadronic cross sections at high energies. In a pure bootstrap of narrow resonances, exchange degeneracy and the absence of exotic channels naturally gave a Pomeron intercept at \alpha_P(0) = 1. However, experimental data began to show that total cross sections rose slowly with energy, starting around the CERN ISR energies. This required a Pomeron intercept above 1, a “supercritical” Pomeron. A Pomeron with \alpha_P(0) > 1 violates the Froissart bound unless tamed by unitarity corrections, which the bootstrap of the 1960s struggled to incorporate in a crossing-symmetric fashion.

Chew and collaborators attempted to extend the bootstrap to include the Pomeron as a self-consistent output of multi-Reggeon unitarity, leading to the topological bootstrap and Reggeon field theory. These efforts were active well into the 1970s, but they were complex and yielded only qualitative results. The rising cross sections, the discovery of the parton model at SLAC, and the mounting evidence for pointlike constituents inside hadrons eroded confidence in the pure S-matrix approach.

---

6. The Advent of QCD and the Displacement of the Bootstrap

The discovery of asymptotic freedom in 1973 (Gross, Wilczek, Politzer) changed everything. QCD offered a renormalizable, local field theory of quarks and gluons that explained Bjorken scaling, the parton model, and the logarithmic violation of scaling. Deep inelastic scattering, which the bootstrap had treated as a formidable analytic continuation problem, became a clean probe of pointlike constituents. The hadron spectrum could be understood as bound states of quarks and gluons, and Regge trajectories emerged from the dynamics of confining flux tubes, not as fundamental axioms.

QCD did not refute the bootstrap’s principles; it simply rendered them unnecessary. The S-matrix of QCD must, of course, satisfy unitarity, analyticity, and crossing. But QCD provided a microscopic off-shell definition from which those properties could in principle be derived, along with a practical computational toolkit: lattice gauge theory, perturbative QCD, and effective field theories. The bootstrap’s quest for a unique, self-determining S-matrix was no longer the only game in town.

The psychological shift was rapid. By 1980, the S-matrix bootstrap was a niche subject. The ambitious claim that field theory was dead had been spectacularly inverted. Yet the deepest legacy of the bootstrap—string theory—continued to evolve, eventually becoming a candidate for quantum gravity, far removed from its hadronic origins.

---

7. Was the Bootstrap Refuted? A Critical Reassessment

To claim that the bootstrap was wrong would require that a self-consistent, crossing-symmetric, unitary S-matrix with the observed hadronic spectrum does not exist without QCD. But we now know such a structure does exist: consistent string theories. Type I superstring theory, for instance, contains a massless vector meson and a rich spectrum of excitations that can be arranged on Regge trajectories. In the 1970s, it was realized that the low-energy limit of open string theory is a Yang–Mills theory; QCD itself can be thought of as arising from a string theory in certain limits (holographic QCD, large-N QCD). Thus the S-matrix of the strong force, when supplemented with the correct gauge symmetries and fermions, is entirely compatible with a purely on-shell, non-field-theoretic formulation—it is, after all, the S-matrix of string theory, which can be defined without reference to a spacetime Lagrangian.

What was refuted was not the existence of a bootstrap solution but the specific restrictive assumptions of the 1960s program:

· The Mandelstam representation is not generally valid in massive quantum field theories; anomalous thresholds, Coleman-Norton singularities, and the complexity of multiparticle unitarity make double dispersion relations much more intricate than originally envisioned.
· The narrow resonance approximation is not a systematic approximation; it ignores widths and the crucial effects of multiparticle thresholds, which are essential for unitarity at high energies.
· The uniqueness dogma—that only one S-matrix could satisfy the axioms—was never proven and is almost certainly false. Modern amplitudes research shows that the same constraints admit families of solutions, parameterized by Wilson coefficients or higher-spin states.
· The program’s reliance on maximal analyticity as a physical principle was ill-defined. Real-world amplitudes possess the singularities they need to satisfy unitarity, but those are determined by the particle spectrum and interactions; there is no independent “maximal” condition that can be imposed a priori without specifying the physical states.

Thus, the bootstrap was not refuted by an inconsistency; it simply failed to deliver a unique, fully relativistic, unitary amplitude that matched the increasingly precise data, while QCD did—at least qualitatively and in many regimes quantitatively—using a completely different framework.

---

8. Modern Echoes: Amplituhedron, Conformal Bootstrap, and Dualities

Remarkably, the spirit of the S-matrix bootstrap has resurged in the 21st century in several distinct but philosophically aligned research programs.

8.1 The Amplituhedron and On-Shell Methods

In planar \mathcal{N}=4 supersymmetric Yang–Mills theory, Arkani-Hamed and collaborators discovered that all-loop scattering amplitudes can be described as the volume of a geometric object, the amplituhedron, with no reference to spacetime, fields, or Lagrangians. Unitarity and locality are emergent from geometric positivity conditions. This is the purest modern realization of the bootstrap idea: the physical observables are determined directly by consistency and symmetry principles, with no off-shell scaffolding. While \mathcal{N}=4 SYM is not QCD, it proves that an S-matrix can be completely determined without ever invoking an off-shell action.

8.2 The Numerical S-Matrix Bootstrap

The conformal bootstrap in CFTs inspired a similar program for massive quantum field theories. Researchers now formulate unitarity, crossing, and analyticity as a system of linear or semi-definite constraints on partial-wave amplitudes. By numerically exploring the space of allowed S-matrices, one can bound couplings, bound Wilson coefficients, and even discover the spectrum of a theory without specifying a Lagrangian. This “S-matrix bootstrap” is a direct descendant of Chew’s vision, now rendered computationally viable. It has been applied to pions, \phi^4 theory, and gravitational amplitudes, yielding rigorous bounds that are saturated by known theories. This demonstrates that the physical content—determining the strong interaction amplitude purely from consistency—is alive and yielding new results.

8.3 String Theory as a Bootstrap Solution

String theory itself can be viewed as a maximal solution to the bootstrap constraints: it provides infinitely many consistent, unitary, crossing-symmetric amplitudes with Regge behavior. The Veneziano amplitude is a tree-level solution, and full string loop amplitudes are fully unitary. In the context of large-N gauge theories, holography provides an exact mapping between a strongly coupled field theory (like \mathcal{N}=4 SYM, or possibly QCD-like theories) and a string theory in anti-de Sitter space. The hadronic S-matrix can, in principle, be encoded entirely in the boundary CFT correlators, which satisfy bootstrap constraints. This closes the circle: the bootstrap’s ultimate physical content—a theory of extended objects whose S-matrix is self-consistent—is precisely what string theory realizes, and string theory is now understood as dual to gauge theory.

---

9. Could a Complete Non-Perturbative S-Matrix Theory Have Succeeded?

We can now answer the question: Is a complete non-perturbative S-matrix theory of the strong force consistent without QCD as scaffolding?

The answer is yes. The modern understanding of the S-matrix program, embodied in string theory and confirmed by holography, shows that there exist mathematically consistent, fully non-perturbative S-matrices that describe the strong force in certain limits. For pure Yang–Mills theory at large N, the S-matrix is believed to be that of a string theory, and this string theory can be defined on-shell without a local QFT Lagrangian. In fact, the large-N expansion organizes mesons and glueballs onto Regge trajectories, with interactions satisfying duality. This is precisely the physical content sought by the bootstrap.

If the historical bootstrap program had not been abandoned, could it have eventually reproduced QCD? Perhaps not in its original form, because the bootstrap sought a single amplitude for the physical world without adjustable parameters, while QCD possesses a dimensionless coupling and quark masses that must be fixed by experiment. However, a more flexible bootstrap that acknowledges a space of possible S-matrices, each corresponding to different values of the strong coupling and quark masses, could in principle recover the hadronic spectrum. The modern numerical S-matrix bootstrap is doing exactly this: mapping the space of consistent amplitudes and identifying corners where specific theories like QCD live.

The historical program was not wrong; it was premature and overly ambitious. The tools of the 1960s—narrow resonance approximation, single-Regge exchange, crude unitarity corrections—were insufficient to handle a fully non-perturbative relativistic many-particle problem. The program’s philosophical insistence on a unique solution blinded it to the possibility that the constraints might admit a family of solutions, among which only experiment (or additional principles) could select our world. When QCD provided a microscopic explanation for the values of masses and couplings, the bootstrap’s quest for an absolute determination seemed less urgent.

But the physical content—the idea that hadrons are the elementary excitations of a self-consistent, infinitely rich S-matrix governed by unitarity, analyticity, and crossing—is entirely consistent. In fact, it is exactly this picture that underlies the large-N approach to QCD and the holographic dualities that now dominate non-perturbative QFT research. Chew’s nuclear democracy finds its resonance in the modern concept of “democracy” among gauge-invariant operators in a strongly coupled CFT, where no operator is more fundamental than another.

The bootstrap was not refuted; it was absorbed and transformed. The amplituhedron and the conformal bootstrap are its direct heirs. The S-matrix is once again the central object, not because fields are wrong, but because on-shell data encode the full quantum theory in a remarkably efficient way.

---

10. Conclusion: The Bootstrap Was Not Wrong, Only Abandoned

The S-matrix bootstrap was an audacious attempt to derive the entire strong interaction directly from physical postulates. It failed to produce a complete, experimentally accurate theory of hadrons, but its failure was one of technical feasibility and over-constraint, not of logical consistency. The historical program was abandoned because QCD provided a more powerful and conceptually satisfying framework. Nevertheless, the core vision—that the S-matrix, constrained by unitarity and analyticity, could be a self-sufficient formulation of physics—has been spectacularly vindicated by modern developments.

We now understand that a non-perturbative S-matrix theory of the strong force, without an underlying local QFT scaffolding, is not only consistent but realized in the form of dual string theories and the solvable S-matrices of planar gauge theories. The hadronic bootstrap of the 1960s can be seen as the first glimpse of a vast and still-unfolding landscape of self-consistent quantum amplitudes. It was not wrong; it was a necessary, visionary step toward the deep structures we continue to explore today.

The lesson for contemporary physics is clear: radical programs that challenge established paradigms may stall or be set aside when a more tractable approach appears, but their underlying physical insights can outlive their era and re-emerge in a new mathematical language. The S-matrix bootstrap was abandoned, but its questions remain among the most profound, and its answers, we now see, are woven into the fabric of quantum field theory and gravity themselves.

The bootstrap wasn’t wrong. It was just waiting for its time to come again.

---

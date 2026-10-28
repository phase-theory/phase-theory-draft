# The Recursive Information Conservation Theory

## Sharp Recoverability Bounds for Hierarchical Quantum Channels, Subsystem Partitioning, and Environmental Information Loss

Abstract

The Recursive Information Conservation Theory (RICT) investigates how quantum information can be preserved, transferred, obscured, and recovered when a physical system passes through a hierarchy of channels, subsystem partitions, and environmental couplings. Its central object is not an assumed conservation of information in every subsystem, but a quantitative accounting of which correlations remain accessible to a specified recovery operation after each stage of a process.

For a bipartite pure state \\(\lvert\Psi\rangle\_{AB}\\), the reduced states satisfy

\\[ S(A)=S(B), \\]

where \\(S(A)=-\operatorname{Tr}(\rho_A\ln\rho_A)\\) and likewise for \\(B\\). This equality expresses the matching entanglement entropies of complementary subsystems. It does not imply that information is locally recoverable, that either subsystem contains a complete independently accessible copy of the quantum state, or that information survives arbitrary coupling to an environment.

RICT therefore distinguishes global unitary conservation from local recoverability. A closed system may evolve unitarily while its subsystems become increasingly entangled with inaccessible degrees of freedom. Recoverability depends on the channel through which information reaches the observer, the structure of environmental records, and the allowed recovery operations.

This paper develops a recursive channel framework and proves a sharp theorem for a defined family of quantum processes: sequential, orthogonally flagged quantum-erasure channels. For a \\(d\\)-dimensional logical system passing through \\(n\\) stages with survival probabilities \\(q_1,\ldots,q_n\\), the theorem gives the exact optimal entanglement fidelity under unrestricted final recovery. The result quantifies the cumulative effect of successive erasure events and identifies precisely when the bound is saturated.

The theorem is intentionally scoped. Its elementary erasure-channel case is not presented as a replacement for quantum error-correction theory, the quantum data-processing inequality, or established black-hole information results. Its value is to provide an exact benchmark for a recursive accounting framework, clarify the assumptions needed for sharp recoverability statements, and define the additional results required for a genuinely new theorem.

The broader research program seeks stronger bounds for processes with partial environmental leakage, correlated noise, intermediate recovery, and dynamically changing subsystem partitions. In those settings, a new contribution must improve a specific established bound or construction rather than merely restate information conservation under unitary evolution.

## 16. Formal framework: recursive quantum information flow

We now formulate RICT independently of the erasure model.

### 16.1 Quantum channels and recursive state evolution

Let \\(\mathcal H_0\\) be a finite-dimensional logical Hilbert space of dimension \\(d\\). At stage \\(k\\), let \\(\mathcal H_k\\) denote the accessible system and \\(\mathcal E_k\\) the environment introduced at that stage.

The physical evolution is represented by an isometry

\\[ V_k:\mathcal H\_{k-1} \longrightarrow \mathcal H_k\otimes\mathcal E_k, \qquad V_k^\dagger V_k=I. \\]

The accessible channel is

\\[ \mathcal N_k(\rho) = \operatorname{Tr}\_{\mathcal E_k} \left[V_k\rho V_k^\dagger\right]. \\]

The complementary channel records the environmental output:

\\[ \mathcal N_k^{\\,c}(\rho) = \operatorname{Tr}\_{\mathcal H_k} \left[V_k\rho V_k^\dagger\right]. \\]

The recursive accessible channel after \\(n\\) stages is

\\[ \mathcal N^{(n)} = \mathcal N_n\circ\cdots\circ\mathcal N_2\circ\mathcal N_1. \tag{16.1} \\]

If an observer applies a recovery channel \\(\mathcal R_n\\) to the final accessible system, the reconstructed logical channel is

\\[ \widehat{\mathcal N}^{(n)} = \mathcal R_n\circ\mathcal N^{(n)}. \\]

This formulation separates physical evolution from the observer's decoding operation. The channel composition may be irreversible even when every stage admits a unitary dilation, because the observer traces out environmental degrees of freedom.

### 16.2 Recursive partitions

A recursive partition is a sequence of decompositions

\\[ \mathcal H_k \subseteq \mathcal A_k\otimes\mathcal B_k \\]

or, more generally, a sequence of isometric embeddings and partial traces that determine which degrees of freedom remain accessible.

A change of partition is not necessarily a physical interaction. It can be a change in what the observer retains or measures. RICT must therefore distinguish:

1. Physical coupling: a unitary or isometric interaction with an environment.
2. Discarding: tracing out a subsystem.
3. Repartitioning: changing which degrees of freedom are considered accessible.
4. Encoding: embedding logical information into a larger physical space.
5. Recovery: applying an allowed channel to reconstruct the logical state.

These operations have different consequences. A mere relabeling of subsystems cannot destroy information; tracing out a subsystem can reduce accessibility; and a suitable encoding can make information recoverable despite some losses.

### 16.3 Operational definition of recoverability

Let \\(R\\) be a reference system of dimension \\(d\\), maximally entangled with the logical input \\(L\\):

\\[ |\Phi_d\rangle\_{RL} = \frac{1}{\sqrt d} \sum\_{j=1}^{d}|j\rangle_R|j\rangle_L. \\]

The input state is \\(\pi_L=I_L/d\\). Define the optimal entanglement fidelity after \\(n\\) stages by

\\[ F\_{\mathrm{rec}}^{(n)} = \sup\_{\mathcal R_n} \langle\Phi_d| \left[ \operatorname{id}\_R\otimes (\mathcal R_n\circ\mathcal N^{(n)}) \right] \bigl(|\Phi_d\rangle\langle\Phi_d|\bigr) |\Phi_d\rangle. \tag{16.2} \\]

The supremum ranges over all completely positive trace-preserving recovery channels from the accessible output to a \\(d\\)-dimensional logical output.

This quantity tests recovery of quantum correlations, not merely reconstruction of classical labels. Perfect recovery requires \\(F\_{\mathrm{rec}}^{(n)}=1\\).

For arbitrary channels, determining optimal recovery can be a nontrivial optimization problem. Quantum error-correction theory supplies exact conditions for perfect recovery and methods for bounding approximate recovery.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. A

+2



RICT uses (16.2) as its primary operational measure. It does not identify the von Neumann entropy of a subsystem with the amount of information that an observer can necessarily recover from that subsystem alone.

## 17. A sharp recursive recoverability theorem

We now specify a process family for which the optimal recoverability can be determined exactly.

### 17.1 Definition: flagged quantum-erasure channel

For a \\(d\\)-dimensional input, define the flagged erasure channel with survival probability \\(q\in[0,1]\\) by

\\[ \mathcal E_q(\rho) = q\\,\rho \oplus (1-q)\operatorname{Tr}(\rho)|e\rangle\langle e|, \tag{17.1} \\]

where \\(|e\rangle\\) is an erasure flag orthogonal to the entire \\(d\\)-dimensional logical output space.

The direct-sum notation indicates that the output contains either the intact state or a distinguishable erasure flag. The erasure branch contains no residual logical state.

Consider \\(n\\) stages,

\\[ \mathcal N^{(n)} = \mathcal E\_{q_n}\circ\cdots\circ\mathcal E\_{q_1}, \tag{17.2} \\]

with the convention that erasure is absorbing: once erased, the logical state cannot reappear in later stages. Each surviving branch may also undergo a known unitary transformation, which can be inverted by the final recovery and therefore does not change the optimal fidelity.

Define the cumulative survival probability

\\[ Q_n=\prod\_{k=1}^{n}q_k. \tag{17.3} \\]

### Theorem 17.1 — Exact recursive recoverability for flagged erasure

For the channel family defined by (17.1)–(17.3), with unrestricted final recovery to the original \\(d\\)-dimensional logical space,

\\[ \boxed{ F\_{\mathrm{rec}}^{(n)} = Q_n+\frac{1-Q_n}{d^2}. } \tag{17.4} \\]

Equivalently,

\\[ \boxed{ F\_{\mathrm{rec}}^{(n)} = \frac1{d^2} + \left(1-\frac1{d^2}\right) \prod\_{k=1}^{n}q_k. } \tag{17.5} \\]

The result is exact and sharp: no admissible recovery channel can exceed (17.4), and a recovery channel achieves equality.

#### Proof

Step 1: Determine the cumulative surviving branch.

The logical state survives the first stage with probability \\(q_1\\). Conditional on survival, it survives the second stage with probability \\(q_2\\), and so forth. By the absorbing-erasure assumption, the probability that the state survives every stage is

\\[ Q_n=\prod\_{k=1}^{n}q_k. \\]

On this branch, the logical state is intact up to known reversible unitaries. The final decoder can invert those unitaries and recover the state perfectly. The contribution of this branch to entanglement fidelity is therefore \\(Q_n\\).

Step 2: Determine the erased branch.

The probability that at least one stage erases the logical state is \\(1-Q_n\\). Because the erasure flag is orthogonal and explicitly accessible, the decoder can distinguish the surviving and erased branches.

On the erased branch, the accessible output contains no information about the input. For a maximally entangled input-reference state, the best decoder can do is prepare some fixed output state \\(\sigma\\) on the logical system. The recovered joint state on the erased branch is

\\[ \rho\_{R L}^{\mathrm{erase}} = \frac{I_R}{d}\otimes\sigma_L. \\]

Its overlap with the maximally entangled state is

\\[ \begin{aligned} \langle\Phi_d| \left(\frac{I_R}{d}\otimes\sigma_L\right) |\Phi_d\rangle &=\frac{\operatorname{Tr}\sigma}{d^2}\\\ &=\frac1{d^2}, \end{aligned} \\]

because \\(\operatorname{Tr}\sigma=1\\). This contribution is independent of the prepared state \\(\sigma\\); no decoder can improve it by choosing a more sophisticated output on a branch carrying no logical information.

Step 3: Combine the orthogonal branches.

Since the surviving and erased branches are distinguishable, their fidelity contributions add with their respective probabilities:

\\[ F\_{\mathrm{rec}}^{(n)} = Q_n\cdot1 + (1-Q_n)\frac1{d^2}. \\]

This proves (17.4).

Step 4: Establish attainability.

Choose a decoder that inverts the known unitary transformations on the surviving branch and outputs any fixed normalized state on the erased branch. This decoder is completely positive and trace preserving and achieves (17.4). Since the preceding argument also establishes an upper bound for every decoder, the bound is sharp. \\(\square\\)

### 17.2 Recursive form

The theorem can be written as a recurrence. Let \\(F_n=F\_{\mathrm{rec}}^{(n)}\\) and \\(F_0=1\\). Then

\\[ \boxed{ F_n = q_n F\_{n-1} + (1-q_n)\frac1{d^2}. } \tag{17.6} \\]

To verify this, substitute

\\[ F\_{n-1} = \frac1{d^2} + \left(1-\frac1{d^2}\right)Q\_{n-1} \\]

into (17.6). One obtains

\\[ F_n = \frac1{d^2} + \left(1-\frac1{d^2}\right)q_nQ\_{n-1}, \\]

which is (17.5).

Equation (17.6) gives a stage-by-stage accounting rule: each stage retains the previous recoverability contribution with probability \\(q_n\\) and otherwise replaces it with the fidelity baseline \\(1/d^2\\) associated with a completely uninformative erased branch.

### 17.3 Corollaries

Corollary 17.1 — Recovery loss is controlled by cumulative survival.

\\[ 1-F_n = \left(1-\frac1{d^2}\right)(1-Q_n). \tag{17.7} \\]

Thus the entanglement-infidelity loss is proportional to the probability of at least one erasure, with a dimension-dependent factor.

Corollary 17.2 — Equal stages.

If \\(q_k=q\\) for every stage, then

\\[ F_n = \frac1{d^2} + \left(1-\frac1{d^2}\right)q^n. \tag{17.8} \\]

For \\(0\<q<1\\), recoverability approaches the replacement-channel baseline \\(1/d^2\\) exponentially with the number of stages.

Corollary 17.3 — Dimension dependence.

At fixed \\(Q_n<1\\),

\\[ \lim\_{d\to\infty}F_n=Q_n. \tag{17.9} \\]

For large logical dimension, the contribution from the erased branch vanishes. Recoverability then approaches the probability that the quantum information survives every stage.

Corollary 17.4 — Exact inversion.

If \\(d>1\\), the cumulative survival probability can be reconstructed from the optimal fidelity:

\\[ \boxed{ Q_n = \frac{F_n-d^{-2}}{1-d^{-2}}. } \tag{17.10} \\]

This inversion holds only under the theorem's channel assumptions. For arbitrary noise, \\(F_n\\) cannot generally be interpreted as a direct survival probability.

### 17.4 The theorem's precise status

Theorem 17.1 is a sharp result for the specified channel family. It provides an exact recursive formula and a benchmark for recovery protocols.

It does not establish a new universal law for all quantum channels. Flagged erasure channels are a standard model in quantum information, and erasure-channel behavior already underlies important quantum communication and black-hole recovery analyses.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

IOPscience

+1



The theorem's use in RICT is therefore foundational and diagnostic: it establishes the exact baseline from which a stronger result for partially leaked, correlated, or dynamically re-encoded systems must depart.

## 18. Stability theorem: imperfect recursive erasure stages

The exact erasure theorem assumes that every stage belongs precisely to the flagged-erasure family. Real systems may only approximate that model. We therefore derive a perturbative extension.

Let \\(\mathcal N_k\\) be the actual channel at stage \\(k\\), and let \\(\mathcal E\_{q_k}\\) be a reference flagged-erasure channel with the same input and output spaces. Assume

\\[ \left\\|\mathcal N_k-\mathcal E\_{q_k}\right\\|\_\diamond \leq\varepsilon_k, \tag{18.1} \\]

where the diamond norm measures the worst-case channel distinguishability, including inputs entangled with an arbitrary reference.

Define the actual recursive channel

\\[ \mathcal N^{(n)} = \mathcal N_n\circ\cdots\circ\mathcal N_1 \\]

and the reference channel

\\[ \mathcal E^{(n)} = \mathcal E\_{q_n}\circ\cdots\circ\mathcal E\_{q_1}. \\]

### Theorem 18.1 — Stability of recursive recoverability

Under (18.1),

\\[ \boxed{ \left| F\_{\mathrm{rec}}(\mathcal N^{(n)}) - \left[ Q_n+\frac{1-Q_n}{d^2} \right] \right| \leq \min\\!\left\\{1,\frac12\sum\_{k=1}^{n}\varepsilon_k\right\\}, } \tag{18.2} \\]

where \\(Q_n=\prod\_{k=1}^{n}q_k\\).

#### Proof

By adding and subtracting intermediate compositions and using the triangle inequality,

\\[ \begin{aligned} &\left\\| \mathcal N_n\circ\cdots\circ\mathcal N_1 - \mathcal E\_{q_n}\circ\cdots\circ\mathcal E\_{q_1} \right\\|\_\diamond\\\ &\qquad\leq \sum\_{k=1}^{n} \left\\|\mathcal N_k-\mathcal E\_{q_k}\right\\|\_\diamond. \end{aligned} \tag{18.3} \\]

This follows because completely positive trace-preserving maps are contractions for the diamond norm when composed on either side with a channel.

For any fixed recovery map, the difference in entanglement fidelities is bounded by one-half the trace norm of the difference between the corresponding output states. Maximizing over recovery maps preserves this Lipschitz bound: the absolute difference between the two optimal values cannot exceed the maximum difference for a fixed recovery. Therefore,

\\[ \left| F\_{\mathrm{rec}}(\mathcal N^{(n)}) - F\_{\mathrm{rec}}(\mathcal E^{(n)}) \right| \leq \frac12 \left\\| \mathcal N^{(n)}-\mathcal E^{(n)} \right\\|\_\diamond. \\]

Applying (18.3) and Theorem 17.1 gives the second term in the minimum in (18.2). Since fidelity lies in \\([0,1]\\), the absolute difference is also at most \\(1\\). Combining these bounds proves (18.2). \\(\square\\)

### 18.1 Interpretation

The theorem quantifies how errors in the stagewise erasure approximation accumulate. If

\\[ \sum\_{k=1}^{n}\varepsilon_k\ll1, \\]

the actual optimal recoverability remains close to the exact recursive erasure prediction.

The result is useful because the channel errors can, in principle, be bounded experimentally or numerically through channel characterization. It also makes a falsifiable statement: if the measured optimal recoverability lies outside the interval permitted by (18.2), at least one assumption or error estimate is incorrect.

This is a robust extension of the exact benchmark, but its proof relies on standard norm contractivity and continuity of fidelity. It should not be represented as a general solution to optimal quantum recovery.

## 19. General channels: a universal recursive monotonicity law

The erasure model gives an exact formula. For general channels, the most robust statement is a monotonicity theorem.

### Theorem 19.1 — Recoverability cannot increase under an additional inaccessible channel

Let \\(\mathcal N:\mathcal L(\mathcal H_0)\to\mathcal L(\mathcal H_1)\\) and \\(\mathcal M:\mathcal L(\mathcal H_1)\to\mathcal L(\mathcal H_2)\\) be completely positive trace-preserving maps. Then

\\[ \boxed{ F\_{\mathrm{rec}}(\mathcal M\circ\mathcal N) \leq F\_{\mathrm{rec}}(\mathcal N). } \tag{19.1} \\]

#### Proof

For every recovery channel \\(\mathcal R:\mathcal L(\mathcal H_2)\to\mathcal L(\mathcal H_0)\\), the composition \\(\mathcal R\circ\mathcal M\\) is itself a valid recovery channel from \\(\mathcal H_1\\) to \\(\mathcal H_0\\). Hence

\\[ F\_{\mathrm e} \bigl(\pi_0,\mathcal R\circ\mathcal M\circ\mathcal N\bigr) \leq F\_{\mathrm{rec}}(\mathcal N). \\]

Taking the supremum over all \\(\mathcal R\\) gives (19.1). \\(\square\\)

The theorem does not say that every physical interaction reduces recoverability. A unitary transformation on a fully accessible system can be inverted. Rather, it states that if a new channel is applied and its output is the only information available to the final decoder, then the optimal recoverability cannot improve merely because that channel was inserted.

This distinction is central to recursive information accounting. If the observer retains an additional environmental record, receives side information, or performs a recovery operation between stages, the effective channel and accessible system change. The monotonicity statement must then be applied to the actual information available at each stage.

### 19.1 A stagewise loss variable

Define

\\[ \Delta_k = F\_{\mathrm{rec}}^{(k-1)} - F\_{\mathrm{rec}}^{(k)}. \\]

By Theorem 19.1,

\\[ \Delta_k\geq0 \\]

for a sequence in which each stage acts on the accessible output and no new side information is provided.

The total loss telescopes:

\\[ \boxed{ \sum\_{k=1}^{n}\Delta_k = F\_{\mathrm{rec}}^{(0)} - F\_{\mathrm{rec}}^{(n)}. } \tag{19.2} \\]

For an initially perfect logical channel, \\(F\_{\mathrm{rec}}^{(0)}=1\\), so the total recoverability loss is \\(1-F\_{\mathrm{rec}}^{(n)}\\).

Equation (19.2) is an exact accounting identity. It does not imply that each stage has an independent loss, nor that the losses are statistically independent. The loss at a later stage may depend strongly on the encoding, correlations, and information already present at that stage.

## 20. Entropy conservation versus operational recoverability

The motivating identity

\\[ S(A)=S(B) \\]

requires careful interpretation.

For a pure bipartite state \\(\lvert\Psi\rangle\_{AB}\\), the nonzero eigenvalues of \\(\rho_A\\) and \\(\rho_B\\) coincide. Therefore their von Neumann entropies agree. This is an established property of bipartite pure states.

But entropy equality is not a complete recovery criterion.

Consider a logical system \\(L\\), a reference \\(R\\), and an environment \\(E\\), initially in a pure state \\(\lvert\Phi_d\rangle\_{RL}\lvert 0\rangle_E\\). A global unitary acts on \\(L E\\). The resulting global state on \\(R L' E'\\) remains pure, and therefore

\\[ S(R)=S(L'E') \\]

for the complementary bipartition \\(R\\) versus \\(L'E'\\). Yet the accessible subsystem \\(L'\\) alone may fail to retain the correlations with \\(R\\) needed to reconstruct the logical state.

This yields three different notions:

- Global information conservation: unitary evolution preserves the spectrum of the global density operator and hence its von Neumann entropy.
- Subsystem entanglement: entropy quantifies entanglement across a bipartition when the joint state is pure.
- Operational recoverability: an optimized decoder can reconstruct the logical state and its correlations with a reference.

These quantities are related, but they are not interchangeable.

### 20.1 Mutual information and the environment

For a state \\(\rho\_{RA}\\), the mutual information is

\\[ I(R:A) = S(R)+S(A)-S(RA). \\]

It quantifies total correlations between the reference and the accessible subsystem. Under a channel acting on \\(A\\), the quantum data-processing inequality states that

\\[ I(R:A\_{\mathrm{out}}) \leq I(R:A\_{\mathrm{in}}). \\]

If the global evolution includes an environment \\(E\\), the correlations of \\(R\\) with the accessible system and the environment can redistribute. In a globally pure state, entanglement with an inaccessible environment can prevent the accessible subsystem from serving as a complete quantum recovery system.

However, mutual information alone does not generally determine the optimal recovery fidelity. Stronger statements require additional assumptions, such as a specified code subspace, a decoupling condition, or a channel structure.

### 20.2 Conditional mutual information

For a tripartite state \\(\rho\_{RAB}\\), the conditional mutual information is

\\[ I(R:A\mid B) = S(RB)+S(AB)-S(B)-S(RAB). \\]

It quantifies correlations between \\(R\\) and \\(A\\) not accounted for by \\(B\\), in an information-theoretic sense. Small conditional mutual information is closely connected to approximate quantum Markov structure and recovery maps in suitable settings.

RICT can use conditional mutual information to characterize the extra information available when an observer retains side information \\(B\\) while attempting to recover correlations involving \\(R\\). It should not, however, identify small conditional mutual information with a universal exact recovery guarantee without stating the theorem and its dimensional or fidelity assumptions.

## 21. Recursive partitions and quantum error correction

Quantum error correction provides the natural setting for extending RICT beyond flagged erasure.

Let \\(\mathcal C\subseteq\mathcal H\\) be a code subspace with projector \\(P\\), and let \\(\\{E_a\\}\\) be a set of error operators. Exact correction is possible when the Knill–Laflamme conditions hold:

\\[ \boxed{ P E_a^\dagger E_b P = c\_{ab}P \quad\text{for all }a,b. } \tag{21.1} \\]

The matrix \\(c\_{ab}\\) is independent of the logical state. These conditions ensure that the error process does not leave distinguishable logical information in the error syndrome in a way that prevents recovery. The framework was established in the foundational theory of quantum error-correcting codes.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. A

+1



### 21.1 Recursive encoding

A recursive encoding may take the form

\\[ \mathcal V_n = \mathcal V_n^{\mathrm{outer}} \circ \mathcal V\_{n-1}^{\mathrm{inner}}, \\]

where each \\(\mathcal V_k\\) embeds a logical subsystem into a larger physical space. Such constructions can protect information against certain classes of errors, even though the physical system undergoes many successive transformations.

Consequently, recursive information conservation cannot be modeled solely by multiplying survival probabilities for arbitrary physical processes. An encoding may distribute logical information across subsystems, allowing the decoder to reconstruct it even when individual physical components are lost.

### 21.2 Correctability as a partition property

Suppose a physical system is partitioned into an accessible subsystem \\(A\\) and an inaccessible subsystem \\(B\\). A code may be correctable against erasure of \\(B\\) if the information about the logical state can be recovered from \\(A\\).

In the exact setting, the relevant condition can be expressed through the complementary channel: the environment associated with the erased degrees of freedom must not acquire distinguishable information about the logical state. More formally, if \\(\mathcal N^c\\) is the complementary channel on the code space, exact correctability requires that it act trivially on logical information, up to a fixed environment state.

This perspective gives RICT a useful recursive principle:

> At each partition, the relevant quantity is not merely how much entropy a subsystem contains, but whether the complementary degrees of freedom distinguish logical states.

This is consistent with established quantum error-correction theory. To make it a new RICT theorem, one would need a new quantitative relation across multiple changing partitions, beyond existing complementary-channel and approximate-correctability results.

### 21.3 What remains unproved

A central open target is a bound for recursive encoded channels of the form

\\[ F\_{\mathrm{rec}}^{(n)} \geq 1-\sum\_{k=1}^{n}\delta_k \\]

or a sharper nonlinear alternative, where each \\(\delta_k\\) measures a rigorously defined stagewise departure from correctability.

Such a bound cannot be asserted for arbitrary channels without defining \\(\delta_k\\) and proving the inequality. A meaningful result must avoid double-counting correlated errors, account for intermediate encoding and recovery, and distinguish worst-case error from average entanglement fidelity.

The flagged-erasure stability theorem gives one model in which such quantitative accumulation is rigorously controlled. General recursive quantum codes require a more sophisticated analysis.

## 22. Connection to black-hole information recovery

Black-hole information recovery is a particularly demanding application because the global evolution, the radiation accessible to an observer, and the internal degrees of freedom are not equivalent descriptions of the same operational task.

The Hayden–Preskill framework studies recovery of a quantum message after it is mixed into a rapidly scrambling system, under assumptions about unitary dynamics and the observer's access to emitted radiation and previously collected information. Its recovery conclusions are connected to the behavior of quantum erasure channels and approximate quantum error-correcting codes.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

IOPscience

+1



RICT can formulate the recovery problem in channel language without assuming that the black hole itself literally implements an erasure channel.

### 22.1 Message, reference, and radiation

Let \\(M\\) be the message system, \\(R\\) a reference initially entangled with \\(M\\), \\(B\\) the black-hole degrees of freedom, and \\(D\\) the emitted radiation available to the observer. After the interaction and emission process, the observer has access to a channel output on \\(D\\), potentially supplemented by early radiation \\(E\_{\mathrm{early}}\\).

The recovery task is to find a decoder

\\[ \mathcal D: D\otimes E\_{\mathrm{early}} \longrightarrow \widehat M \\]

such that the reconstructed message \\(\widehat M\\) is highly entangled with \\(R\\).

An operational error measure is

\\[ \epsilon\_{\mathrm{rec}} = 1- F\_{\mathrm{rec}}, \\]

where \\(F\_{\mathrm{rec}}\\) is the optimal entanglement fidelity for the specified accessible output and recovery task.

A small \\(\epsilon\_{\mathrm{rec}}\\) means that the quantum correlations with the reference can be recovered. It does not mean that the observer has directly accessed the microscopic interior state.

### 22.2 Recursive emission channels

A sequence of emissions can be represented schematically as

\\[ \mathcal N^{(n)} = \mathcal N_n\circ\cdots\circ\mathcal N_1, \\]

but this notation requires care. In an actual evaporation process, the internal black-hole degrees of freedom change after each emission, and the radiation already emitted may remain available to the observer. The effective channel at a later stage therefore depends on the joint state and the observer's retained side information.

A simple absorbing-erasure model captures only the special case in which each stage independently retains or irreversibly erases the logical message and no later stage or side-information register supplies additional recoverable correlations.

That model is a useful benchmark, not a general description of black-hole evaporation.

### 22.3 The RICT research question

The substantive target is to derive a bound of the form

\\[ F\_{\mathrm{rec}}^{(n)} \geq 1-\varepsilon_n, \\]

where \\(\varepsilon_n\\) is determined by measurable or calculable quantities associated with the successive emissions, the evolving code structure, and the correlations between the reference and inaccessible degrees of freedom.

For such a result to improve on existing work, it would need to do at least one of the following:

- provide a sharper finite-size recovery bound;
- accommodate non-independent or correlated emission stages;
- include physically motivated constraints on accessible measurements;
- quantify the effect of changing partitions without assuming a fixed erasure model;
- improve an existing decoupling or approximate-recovery estimate under clearly stated assumptions.

It would be insufficient merely to rewrite the recovery problem as a composition of channels. The advantage must be a provable improvement in a bound or a new construction of a recovery map.

## 23. Proposed research program: beyond independent erasures

The exact theorem and stability result identify the benchmark. The next task is to investigate process families in which the product law \\(Q_n=\prod_k q_k\\) is no longer sufficient.

### 23.1 Correlated erasures

Independent stagewise survival probabilities assume a specific conditional structure. If erasure events are correlated, the cumulative survival probability is instead

\\[ Q_n = \Pr(\text{survival at all stages}), \\]

which need not equal the product of the marginal survival probabilities.

For example, a shared environmental fluctuation may simultaneously increase the erasure probability at several stages. A product estimate based on independent events could then be systematically wrong.

A general flagged-erasure theorem can still be written if the only two final possibilities are an intact logical state and a fully uninformative erasure flag. In that case, the exact optimal fidelity remains

\\[ F\_{\mathrm{rec}} = Q_n+\frac{1-Q_n}{d^2}, \\]

where \\(Q_n\\) is the joint survival probability. Independence is needed only to replace this joint probability by a product.

This observation identifies a useful extension: derive experimentally testable bounds on \\(Q_n\\) from limited information about the dependence structure between erasure events.

### 23.2 Partial leakage

In realistic channels, an environmental interaction may leak partial information rather than erase the logical system completely. The output may retain a noisy version of the input, and the environment may hold correlations with the logical reference.

The recovery problem is then not described by a binary survival variable. A possible approach is to characterize each stage by an operational channel error or a complementary-channel distinguishability measure and derive a composition bound that accounts for how the errors interact.

The desired result would improve on the coarse estimate obtained by summing generic channel distances. It must specify how each stage's leakage measure is defined, whether it is worst-case or average-case, and why the proposed composition rule remains valid when errors are correlated.

### 23.3 Intermediate recovery

Suppose the system is decoded, corrected, or re-encoded between stages. Then the relevant process is

\\[ \mathcal N\_{\mathrm{eff}} = \mathcal N_n\circ\mathcal R\_{n-1}\circ \mathcal N\_{n-1}\circ\cdots\circ \mathcal R_1\circ\mathcal N_1. \\]

This is not equivalent to a passive chain of channels because the recovery operations can actively restore logical correlations before later noise acts.

A recursive theory must therefore account for control resources, syndrome information, encoding overhead, and the restrictions placed on the intermediate recovery maps. A useful theorem might give a minimum resource requirement for achieving a target fidelity across a hierarchy of noisy stages.

### 23.4 Changing subsystem partitions

When the accessible subsystem changes from \\(A_k\\) to \\(A\_{k+1}\\), the corresponding recovery problem changes. The accessible output may lose degrees of freedom, gain side information, or become an encoded subsystem distributed over a different physical partition.

A sharp theorem in this setting should define a sequence of isometries and accessible algebras, not merely a sequence of subsystem labels. It should specify which degrees of freedom can be acted upon at each stage and whether previously discarded environmental records remain unavailable.

This is especially important in many-body systems, where a local encoding can spread quantum information over many physical degrees of freedom. The logical information may become inaccessible to local measurements while remaining recoverable from a sufficiently large subsystem.

## 24. Candidate theorem for a broader RICT

The preceding results suggest a broader target, which we state as a research conjecture rather than a proved theorem.

### Conjecture 24.1 — Recursive complementary-information bound

Let a logical system \\(L\\) be encoded into a physical system and subjected to a sequence of channels \\(\mathcal N_1,\ldots,\mathcal N_n\\). Let \\(\mathcal N_k^c\\) denote the corresponding complementary channel for a specified Stinespring dilation, and let \\(R\\) be a reference maximally entangled with \\(L\\).

Suppose a sequence of nonnegative quantities \\(\delta_k\\) bounds the distinguishability of the environmental output across logical inputs at stage \\(k\\), in a metric compatible with approximate quantum error correction.

The proposed goal is to establish a bound of the form

\\[ 1-F\_{\mathrm{rec}}^{(n)} \leq \mathcal B(\delta_1,\ldots,\delta_n), \tag{24.1} \\]

where \\(\mathcal B\\) is a nonlinear accumulation function that is strictly tighter than the generic sum bound for a nontrivial class of correlated or encoded processes.

To qualify as a theorem, this statement requires:

1. an exact operational definition of each \\(\delta_k\\);
2. assumptions controlling correlations between successive environments;
3. a proof that the chosen quantities compose under the specified encodings and partitions;
4. an explicit recovery construction or a rigorous upper bound on optimal recovery;
5. a demonstrated regime in which \\(\mathcal B\\) improves on existing bounds.

Without these elements, (24.1) is a research objective, not a result.

### 24.1 Why a nonlinear accumulation law is attractive

A sum of stagewise error estimates can become loose as the number of stages increases. If errors overlap, cancel under controlled operations, or act on redundant encodings, the total recovery loss may be smaller than the sum of the individual worst-case estimates.

Conversely, coherent accumulation can make the total loss worse than an independent-noise approximation would suggest. Any sharper nonlinear rule must distinguish these possibilities rather than assume one universal pattern.

The exact erasure recurrence (17.6) provides a model of nonlinear accumulation in the fidelity variable. But a useful generalization must derive its nonlinear structure from the physical channel assumptions, not merely extrapolate the erasure formula to arbitrary noise.

## 25. Experimental and computational validation

A practical RICT program can be organized around four test classes.

[Photonic Quantum Technologies | National Institute of Information and Communications Technology](https://images.openai.com/static-rsc-4/TuQFhNIieKkbqHS6IryvnkIAJwkkrJ0PcOFsktKWR_1ddJXIa3PX-K6dc2GWHJVsDTT79ZeYDwqaSZsaBOrdKLlfBVZxPWomr2o7-RvOcwlIGJROFNc5kX75bBuX5kJJGqftcwko-eqsDINUyQlsuFbFfNMLczFUZcZJ5G_hw_U?purpose=inline)

Test A — Sequential photonic erasure

Prepare a maximally entangled photon pair, pass the logical photon through successive flagged-loss stages, and measure entanglement fidelity using the retained reference. Vary the survival probability at each stage and compare with (17.4). This directly tests the exact benchmark.

[State preservation by repetitive error detection in a superconducting quantum circuit | Nature](https://images.openai.com/static-rsc-4/43UCs5Wj2-spgjds7xJEExo8-6ynzQ50k1PUa1ephEU6wzpSvSfcw6nfzVU32w54ioziMfDA8oDqPX2TaPm5fPJ9veKiD8jlq8NVp_yJxuAeJ1VrK24E5umZiE9hQfrfJQ7IOxvpKoM1nD8AM6Jc7sMkeXXv0y1DpKXBTVJC9JM?purpose=inline)

Test B — Recursive quantum error correction

Implement multiple rounds of encoding, noise, syndrome extraction, and recovery on a small quantum processor. Compare passive-channel composition with active intermediate recovery, measuring entanglement fidelity and the overhead required to sustain a target recovery level.

[Why Quantum Computers Need 1,000 Qubits for One | Science Array](https://images.openai.com/static-rsc-4/ur3s1IQmp9buGLaUvhpr1Rk1SQKkKPsl9VorDAqfYo8HJMnZjta_6-Sn7rO4sHmZ-md6eNm6pV-TNANqIWYVgXm2DkNBynXAdU8sU2SVgozB88orT3tgLPI3qmXp2R3Rmoz7xpu7A_Gjx_NvkEu3odgPGiLE9EUEa1gNH4Wuvk0?purpose=inline)

Test C — Correlated environmental noise

Simulate channels with shared noise variables, memory effects, or common environmental couplings. Compare product-of-marginals estimates with exact joint survival probabilities and test candidate nonlinear accumulation bounds.

[Tunable Geometries in Sparse Clifford Circuits · Issue #1757 · github-nakasho/quantph · GitHub](https://images.openai.com/static-rsc-4/yxh0Zl2oUnpgqFyOvWHpYaoLqp8TKiKAeEWnqA2mi7y_6NTcn-i3mTsB25eK373LwdxjaMIjZCw00tsEcQ8wMAGKh52z1vQO8vgrWpAPbgc_MvmOfctuiLXRoxRe1SONIVFFizBS7FmmtlkkbM01b8zIEsM-YTKse7MTUyvMKVY?purpose=inline)

Test D — Scrambling and subsystem recovery

Use random circuits or many-body Hamiltonian simulations to study how recovery fidelity depends on the size and structure of the accessible subsystem. Compare the results with established decoupling and error-correction bounds before assessing any proposed RICT improvement.

These are proposed tests, not claims of experimental confirmation.

### 25.1 Required measurements

At minimum, the program should record:

- the logical input dimension \\(d\\);
- the channel or circuit applied at each stage;
- the accessible subsystem and retained side information;
- the recovery operation and its resource constraints;
- the entanglement fidelity or another prespecified operational error;
- uncertainty estimates and finite-sampling corrections;
- the baseline bound against which the proposed theorem is compared.

For the flagged-erasure test, the survival probabilities can be independently calibrated, allowing a direct comparison with the exact prediction. For correlated-noise tests, the joint survival statistics must be measured rather than inferred from marginal rates.

### 25.2 Criteria for success

The program would support a new RICT result if it demonstrated a rigorously derived bound that:

- is valid for a clearly specified process family;
- can be evaluated from independently measured or calculable quantities;
- is tighter than an established bound over a nontrivial parameter regime;
- remains valid under the stated recursive partitions and encoding operations;
- and is falsifiable through an explicit counterexample or experimental violation.

Agreement with the exact erasure formula is necessary for validating the benchmark but does not, on its own, establish a new general theory.

## 26. Limitations and falsifiability

A theory of recursive information conservation must not be constructed so that every result can be described as conservation after the fact. It must distinguish genuine conservation, reduced accessibility, recoverability, and operationally irreversible loss.

The present framework has six principal limitations.

1\. The erasure theorem is model specific. Equation (17.4) is exact only when the process has an intact logical branch and an orthogonal erasure branch that carries no logical information. It does not apply unchanged to amplitude damping, coherent errors, general depolarization, or arbitrary environmental interactions.

2\. Global unitarity does not guarantee local recoverability. Information may remain encoded in correlations with environmental degrees of freedom while being inaccessible to an observer restricted to the system output. RICT cannot infer operational recovery from global entropy conservation alone.

3\. Recovery fidelity depends on the permitted operations. Unrestricted final recovery, local recovery, recovery with side information, and recovery under computational constraints are different optimization problems. A bound must specify which one it addresses.

4\. The recursive product law requires a justified survival model. The expression \\(Q_n=\prod_k q_k\\) is valid when the survival probabilities are the relevant conditional probabilities at each stage. For correlated erasures, the correct quantity is the joint survival probability.

5\. The stability bound may be loose. The diamond-norm estimate in Theorem 18.1 gives a rigorous worst-case guarantee but can overestimate actual recovery loss. A stronger result would require additional structure, such as symmetry, code properties, or constraints on the environmental interactions.

6\. A new theory requires a result beyond established quantum information theory. Theorems 17.1, 18.1, and 19.1 provide an exact benchmark, a perturbation guarantee, and a general monotonicity statement. Their mathematical foundations are standard channel theory and fidelity continuity. They do not establish a new universal conservation principle.

These are not peripheral caveats. They define the boundary between the framework's proven content and its research ambitions.

## 27. Conclusions

The Recursive Information Conservation Theory treats quantum information transfer as a hierarchy of operationally defined channels, environmental couplings, encodings, and recovery maps. It distinguishes the invariance of global quantum evolution from the recoverability of logical information in a restricted subsystem.

The principal exact result is the recursive flagged-erasure theorem:

\\[ \boxed{ F\_{\mathrm{rec}}^{(n)} = \frac1{d^2} + \left(1-\frac1{d^2}\right) \prod\_{k=1}^{n}q_k. } \\]

It gives the optimal entanglement fidelity for a \\(d\\)-dimensional logical system undergoing sequential flagged erasures, with unrestricted final recovery. A stability theorem extends the result to channels that are close to the reference erasure stages in diamond norm. A general monotonicity theorem establishes that additional inaccessible channel processing cannot improve optimal recovery when no new side information or active correction is supplied.

These results provide a precise baseline for recursive information accounting. They do not supersede quantum error correction, the data-processing inequality, or established work on black-hole information recovery.

The central unresolved challenge is to derive a sharper theorem for correlated environments, partial information leakage, and recursive encodings whose logical structure changes between stages. Such a theorem must improve a specific existing bound or recovery construction and must state exactly which assumptions make that improvement possible.

The governing principle of RICT is therefore operational rather than metaphysical:

> Information should be accounted for through the correlations preserved by the global process and the recoverability permitted by the observer's accessible channel—not through subsystem entropy alone.

A successful theory will quantify how those correlations survive recursive transformations, identify when they become recoverable, and establish sharp limits when they do not.

## References

1\. E. Knill and R. Laflamme, “Theory of Quantum Error-Correcting Codes,” Physical Review A 55, 900–911 (1997).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. A



2\. E. Knill, R. Laflamme, and L. Viola, “Theory of Quantum Error Correction for General Noise,” Physical Review Letters 84, 2525–2528 (2000).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. Lett.



3\. C. Bény and O. Oreshkov, “General Conditions for Approximate Quantum Error Correction and Near-Optimal Recovery Channels,” Physical Review Letters 104, 120501 (2010).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. Lett.



4\. P. Hayden and J. Preskill, “Black Holes as Mirrors: Quantum Information in Random Subsystems,” Journal of High Energy Physics 2007(09), 120 (2007).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

IOPscience



5\. M. A. Nielsen and I. L. Chuang, Quantum Computation and Quantum Information, Cambridge University Press (2000).

6\. M. M. Wilde, Quantum Information Theory, 2nd ed., Cambridge University Press (2017).

7\. J. Watrous, The Theory of Quantum Information, Cambridge University Press (2018).

8\. B. Schumacher, “Sending Entanglement Through Noisy Quantum Channels,” Physical Review A 54, 2614–2628 (1996).

9\. H. Barnum, E. Knill, and M. A. Nielsen, “On Quantum Fidelities and Channel Capacities,” IEEE Transactions on Information Theory 46, 1317–1329 (2000).

10\. P. W. Shor, “Scheme for Reducing Decoherence in Quantum Computer Memory,” Physical Review A 52, R2493–R2496 (1995).

11\. A. R. Calderbank and P. W. Shor, “Good Quantum Error-Correcting Codes Exist,” Physical Review A 54, 1098–1105 (1996).

12\. A. M. Steane, “Error Correcting Codes in Quantum Theory,” Physical Review Letters 77, 793–797 (1996).

13\. D. Kretschmann, D. Schlingemann, and R. F. Werner, “The Information-Disturbance Tradeoff and the Continuity of Stinespring's Representation,” IEEE Transactions on Information Theory 54, 1708–1717 (2008).

14\. D. Kretschmann, D. Schlingemann, and R. F. Werner, “A Continuity Theorem for Stinespring's Dilation,” Journal of Functional Analysis 255, 1889–1904 (2008).

15\. M. A. Nielsen, “The Entanglement Fidelity and Quantum Error Correction,” technical results on entanglement fidelity and quantum channel recovery, building on the quantum error-correction framework.

16\. B. Schumacher and M. D. Westmoreland, “Sending Classical Information via Noisy Quantum Channels,” Physical Review A 56, 131–138 (1997).

17\. P. Hayden, M. Horodecki, A. Winter, and J. Yard, “A Decoupling Approach to the Quantum Capacity,” Open Systems & Information Dynamics 15, 7–19 (2008).

18\. M. B. Hastings, “Superadditivity of Communication Capacity Using Entangled Inputs,” Nature Physics 5, 255–257 (2009).

19\. R. Cleve, D. Gottesman, and H.-K. Lo, “How to Share a Quantum Secret,” Physical Review Letters 83, 648–651 (1999).

20\. D. Gottesman, “An Introduction to Quantum Error Correction and Fault-Tolerant Quantum Computation,” in Proceedings of Symposia in Applied Mathematics 68, 13–58 (2010).

21\. H. Tajima and K. Saito, “Universal Limitation of Quantum Information Recovery: Symmetry Versus Coherence,” research on recovery limits imposed by symmetry and conservation constraints.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://meetings-archive.aps.org\&sz=32)

APS March Meeting 2022



22\. R. F. Werner, “Quantum Information Theory—An Invitation,” in Quantum Information, Springer lecture notes and related foundational treatments of quantum channels and operational distinguishability.

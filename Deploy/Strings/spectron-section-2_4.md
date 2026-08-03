## 2.4 The Spectron: Elementary Spectral Constituent

### 2.4.1 Motivation

Sections 2.1–2.3 introduced the resonance operator \(\mathfrak{D}^I(\sigma,\tau)\) and its diagonal eigenvalue sector as the origin of the emergent coordinate field \(X^I(\sigma,\tau)\). It is useful, both for physical intuition and for the mechanics developed in Sections 3–5, to isolate the truly elementary object of the theory: not the matrix \(\mathfrak{D}^I\), not the continuum field \(X^I\), but the single quantized eigenvalue-mode from which both are built. We call this object the **Spectron**.

Where conventional string theory takes the embedding coordinate \(X^\mu(\sigma,\tau)\) as fundamental, and matrix string theory takes the matrix element as fundamental, SRSM takes neither as fundamental. The Spectron is one level more primitive than either: it is a single eigenvalue of \(\mathfrak{D}^I\), together with its conjugate momentum, bound to a discrete resonance lattice. Collections of Spectrons, in the continuum limit, are what *become* the coordinate field. In this sense the Spectron plays for SRSM the role the qubit plays for quantum information theory: the elementary carrier of the theory's data, prior to any continuum or geometric interpretation.

### 2.4.2 Definition

Fix a worldsheet point \((\sigma,\tau)\) and diagonalize the commuting sector of \(\mathfrak{D}^I\),
\[
\mathfrak{D}^I(\sigma,\tau) = U(\sigma,\tau)\,\Lambda^I(\sigma,\tau)\,U^\dagger(\sigma,\tau),
\qquad
\Lambda^I = {\rm diag}\big(\lambda_1^I,\dots,\lambda_N^I\big).
\]
The **Spectron** \(\sigma_a\), \(a=1,\dots,N\), is the elementary spectral constituent
\[
\sigma_a(\sigma,\tau) \;=\; \Big(\lambda_a^I(\sigma,\tau),\ \pi_a^I(\sigma,\tau)\Big),
\]
where \(\pi_a^I\) is the momentum canonically conjugate to \(\lambda_a^I\), inherited from the matrix momentum \(\Pi_I\) of Section 3 by restriction to the diagonal gauge. A Spectron is thus a single point-particle degree of freedom moving in the emergent target space, but — crucially — it is not itself a spacetime point; it is a *label on the spectrum* of \(\mathfrak{D}^I\) that becomes a spacetime point only after the continuum limit of Section 5 is taken.

The full matrix field \(\mathfrak{D}^I\) is recovered as
\[
\mathfrak{D}^I = \sum_{a=1}^N \lambda_a^I\,|a\rangle\langle a| \;+\; (\text{off-diagonal coherences}),
\]
i.e. as a collection of \(N\) Spectrons dressed by their mutual off-diagonal couplings (Section 2.4.5).

### 2.4.3 Lattice quantization number

The resonance (gap) potential
\[
V_{\rm gap}(\slashed{\mathfrak{D}})
=
\frac{\rho}{2}\,{\rm Tr}\Big[1-\cos\Big(\tfrac{2\pi\slashed{\mathfrak{D}}}{\Delta}\Big)\Big]
\]
energetically confines each Spectron to the resonance lattice,
\[
\lambda_a^I \;\simeq\; n_a^I\,\Delta, \qquad n_a^I \in \mathbb{Z}.
\]
The integer \(n_a^I\) is the Spectron's fundamental quantum number — the discrete address it occupies on the resonance lattice in direction \(I\). This is the sense in which \(\Delta\) is not merely a parameter but the grain size of the theory: it is the spacing between adjacent admissible Spectron states, exactly as the qubit's two-dimensional Hilbert space is the "grain" of quantum information. Since \(\alpha'=\Delta^{-2}\), the string scale is nothing but the inverse-square lattice spacing between Spectrons.

### 2.4.4 Canonical algebra

At fixed \((\sigma,\tau)\), a single Spectron obeys the canonical commutation relation
\[
\big[\lambda_a^I,\pi_b^J\big] = i\,\delta_{ab}\,\delta^{IJ},
\]
inherited directly from the matrix algebra
\[
\big[{\rm Tr}(\mathfrak{D}^I T^A),\,{\rm Tr}(\Pi_J T^B)\big] = i\,\delta^I_J\,\delta^{AB}\,\delta(\sigma-\sigma')
\]
of Section 6.1, restricted to the Cartan (diagonal) subalgebra. This restriction is exact only in the strictly commuting sector; away from it, Spectrons are dressed by coherences, discussed next.

### 2.4.5 Spectron coherence and off-diagonal entanglement

An off-diagonal matrix element \(\mathfrak{D}_{ab}^I\) with \(a\neq b\) is interpreted as a **coherence** between Spectron \(a\) and Spectron \(b\) — a spectral analogue of entanglement between two qubits. When this coherence is populated, the pair \((\sigma_a,\sigma_b)\) is not resolvable into two independent, sharply-defined lattice points; the pair instead contributes jointly to the non-commutativity tensor of Section 2.3,
\[
\Theta^{IJ} = -\frac{i}{N}\,{\rm Tr}\,[\mathfrak{D}^I,\mathfrak{D}^J]
= -\frac{i}{N}\sum_{a\neq b}\Big(\mathfrak{D}_{ab}^I\mathfrak{D}_{ba}^J - \mathfrak{D}_{ab}^J\mathfrak{D}_{ba}^I\Big).
\]
Thus \(\Theta^{IJ}\), the emergent spacetime non-commutativity, is entirely sourced by inter-Spectron coherence. A theory of "free," uncoupled Spectrons (\(\mathfrak{D}_{ab}^I=0\) for \(a\neq b\)) has \(\Theta^{IJ}=0\) and describes ordinary commuting coordinates; turning on coherence is what makes the emergent geometry non-commutative. This gives coherence a direct physical meaning: it is not a bookkeeping device but the microscopic origin of spacetime fuzziness.

The interaction energy of a coherence bond between Spectrons \(a\) and \(b\) is set, as shown in Section 10, by their spectral separation,
\[
M_{ab}^2 \;\sim\; \frac{1}{\alpha'}\,\big|\lambda_a-\lambda_b\big|^2,
\]
so coherence is energetically cheap between nearby Spectrons and costly between distant ones — the microscopic statement that strings interact when their eigenvalue supports overlap and decouple when they separate (Section 10).

### 2.4.6 Statistics: Spectron repulsion

Off the coherence sector, Spectrons interact through the Vandermonde measure inherited from the change of variables of Section 5.1,
\[
\mathcal{D}\mathfrak{D}^I \;=\; \mathcal{D}U \prod_{a=1}^N d\lambda_a^I \prod_{a<b}\big|\lambda_a^I-\lambda_b^I\big|^2.
\]
After integrating out the angular (gauge) degrees of freedom, this measure generates an effective potential between any two Spectrons (Appendix A),
\[
V_{ab} \;=\; \frac{1}{2\big(\lambda_a^I-\lambda_b^I\big)^2},
\]
the rational Calogero-Moser interaction. Two Spectrons therefore cannot occupy the same lattice site: the theory has a built-in exclusion principle, not imposed by hand but derived from the geometry of the matrix measure. This is the mechanism by which a discrete set of \(N\) mutually repelling Spectrons becomes, at large \(N\), an incompressible eigenvalue fluid with equilibrium density \(\rho_0\) — and it is this repulsion, not an externally posited tension, that produces the string tension
\[
T_{\rm eff} = \frac{1}{2\pi\alpha'} = \frac{\Delta^2}{2\pi}
\]
of Section 9.

A Spectron is therefore best classified operationally rather than by an exchange symmetry: it is a point charge in eigenvalue space subject to (i) confinement to the resonance lattice, and (ii) inverse-square repulsion from every other Spectron.

### 2.4.7 Continuum limit: from Spectron gas to string

The passage from discrete Spectrons to the emergent string proceeds exactly as in Section 5.2. Define the Spectron density
\[
\rho(x,\sigma,\tau) = \frac{1}{N}\sum_{a=1}^N \delta\big(x-\lambda_a(\sigma,\tau)\big),
\]
with conjugate collective field \(\Pi(x,\sigma,\tau)\). The collective Hamiltonian
\[
H_{\rm coll} = \int dx\,\Big[\tfrac{1}{2}\rho(\partial_x\Pi)^2 + \tfrac{\pi^2}{6}\rho^3 + V_{\rm res}(x)\rho\Big] + H_{\rm nonlocal}
\]
governs the hydrodynamics of the Spectron gas; the cubic term is the direct continuum remnant of Spectron repulsion. Fluctuations of the Spectron density about equilibrium,
\[
X^I(\sigma,\tau) = x_0^I + \frac{1}{\rho_0}\,\delta\rho^I(\sigma,\tau),
\]
obey the free wave equation and reproduce the Polyakov kinetic term (Section 5.2). The hierarchy of description is thus
\[
\text{Spectron}
\;\longrightarrow\;
\text{Spectron gas (Calogero-Moser system)}
\;\longrightarrow\;
\text{eigenvalue hydrodynamics}
\;\longrightarrow\;
\text{Polyakov string}.
\]
Each arrow is a genuine coarse-graining, not a reinterpretation: a single Spectron carries a lattice index and a momentum, and nothing else; "position in spacetime," "string tension," and "graviton" are all properties of a collective Spectron configuration, not of any individual Spectron.

### 2.4.8 Mass, spin, and the Spectron content of physical states

Because mass and spin are collective properties, a single free Spectron is massless and spinless in the target-space sense; it acquires physical meaning only in a bound configuration. The rotating two-eigenvalue (or continuum) configuration of Section 9,
\[
X^1+iX^2 = r(\sigma)e^{i\omega\tau}, \qquad r(\sigma)=r_0\sin\sigma,
\]
is a coherent state of many Spectrons whose collective angular momentum and energy reproduce the Regge relation
\[
J = \alpha' E^2 + a_{\rm spec}.
\]
Likewise, the oscillator modes \(\alpha_n^I\) of Section 6.1 are recovered as Fourier components of the Spectron density fluctuation \(\delta\rho^I\); the level number \(N=\sum_{n>0}\alpha_{-n}\cdot\alpha_n\) counts units of collective Spectron excitation, not individual Spectrons. In particular:

- the **tachyon/ground state** is the unperturbed, uniform Spectron density \(\rho_0\);
- **massless states** (graviton, gauge bosons) are the lowest collective density waves of the Spectron fluid, consistent with the vertex operators of Section 7.3;
- the **spectral form factor** \(\mathcal{F}_{\rm spec}(s,t,u)=\exp[-(s^2+t^2+u^2)/16\Lambda_N^2]\) of Section 8.2, with \(\Lambda_N=\Delta\sqrt{N}\), is a direct finite-\(N\) (finite Spectron-number) effect: it vanishes smoothly as \(N\to\infty\), i.e. as the discreteness of the Spectron gas is erased.

### 2.4.9 Comparison across frameworks

| Framework | Elementary unit | Discreteness source | Continuum object recovered |
|---|---|---|---|
| Quantum mechanics | Qubit | Hilbert space dimension | Continuous wavefunction |
| Phase Theory | Phaset | phase-admissibility | Phase field |
| Mₜ Theory | Framet | \(S^1_t\) structure | Frame field |
| SRSM | **Spectron** | resonance lattice spacing \(\Delta\) | Emergent coordinate field \(X^I(\sigma,\tau)\) / Polyakov string |

### 2.4.10 Summary

The Spectron is the elementary spectral constituent of SRSM: a single eigenvalue of the resonance operator, confined to a discrete resonance lattice of spacing \(\Delta\), subject to Calogero-Moser repulsion from every other Spectron, and capable of forming coherence bonds with other Spectrons that source the emergent non-commutative geometry of spacetime. Individually, a Spectron carries no mass, spin, or spacetime position in the conventional sense — these are all collective properties of a Spectron configuration. It is only in the large-\(N\) hydrodynamic limit that a Spectron gas condenses into the familiar objects of string theory: the coordinate field \(X^I\), the string tension \(T_{\rm eff}\), the Virasoro algebra, and ultimately the graviton. In this sense SRSM is, at the most fundamental level, a theory of interacting Spectrons, of which strings, spacetime, and gravity are emergent, collective phenomena.

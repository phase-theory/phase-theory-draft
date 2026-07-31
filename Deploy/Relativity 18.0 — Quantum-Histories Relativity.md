# Relativity 18.0 — Quantum-Histories Relativity  
## Reality as a Quantum Measure over Histories

**White paper / academic preprint**

---

## Abstract

Quantum-Histories Relativity is the formulation of physics in which the fundamental object is not a state evolving in time, not a single spacetime trajectory, and not even a single classical universe. The fundamental object is a space of histories equipped with a quantum measure. A history is a complete fine-grained account of a physical process: a path, a field configuration, a causal set, a spin foam, a geometry, or an entire cosmological spacetime. The quantum measure assigns weights not to individual histories in the classical probabilistic sense, but to sets of histories through interference-sensitive rules. Schematically,

\[
\mu(A)
=
\left|
\sum_{\gamma\in A}
e^{iS[\gamma]/\hbar}
\right|^2,
\]

where \(A\) is a set of histories and \(S[\gamma]\) is the action of history \(\gamma\). Classical spacetime is not fundamental. It is a decoherent realm: a coarse-grained family of histories whose mutual interference is negligible and whose members obey approximately classical equations. Quantum-Histories Relativity therefore replaces the classical ontology of a single world-line or single spacetime with a deeper structure:

\[
\boxed{
\text{Reality is a quantum measure over histories, not a single classical trajectory.}
}
\]

This framework unifies the path-integral formulation of quantum theory, the consistent-histories approach, causal-set quantum growth, spin-foam quantum gravity, group field theory, and cosmological no-boundary proposals. It is a natural completion of the relational and informational versions of relativity: if spacetime is relational, holographic, thermodynamic, causal, computational, categorical, and entropic, then its most primitive description may be a quantum measure over possible histories.

---

## 1. Introduction

The path integral changed the conceptual foundations of physics.

In canonical quantum mechanics, one begins with a state \(\ket{\psi(t)}\) evolving according to the Schrödinger equation. In the path-integral formulation, one instead sums over all possible histories connecting boundary data:

\[
\langle x_f,t_f|x_i,t_i\rangle
=
\int_{x(t_i)=x_i}^{x(t_f)=x_f}
\mathcal{D}x(t)\,
e^{iS[x]/\hbar}.
\]

The amplitude is not attached to one trajectory. It is attached to a set of trajectories.

Quantum-Histories Relativity takes this insight seriously and elevates it to a foundational principle.

The basic question is not:

\[
\text{What is the state of the universe at time } t?
\]

The basic question is:

\[
\text{What is the quantum measure over complete histories of the universe?}
\]

A history may be:

1. a particle trajectory,
2. a field configuration over spacetime,
3. a sequence of quantum events,
4. a causal set growth process,
5. a spin foam interpolating spin networks,
6. a four-geometry with matter fields,
7. an entire cosmological spacetime.

Classical reality is then not the fundamental history. It is a decoherent coarse-graining of the quantum measure.

This is Relativity 18.0.

---

## 2. From States to Histories

In ordinary quantum mechanics, the central object is the state vector,

\[
\ket{\psi(t)}.
\]

Time is external. Dynamics is evolution.

In the histories formulation, the central object is a space of histories \(\Omega\). A history \(\gamma\in\Omega\) is a complete description of a process.

For a particle, a history is a path

\[
\gamma: t\mapsto x(t).
\]

For a field, a history is a configuration

\[
\gamma: x^\mu \mapsto \phi(x).
\]

For gravity, a history is a spacetime geometry and matter configuration,

\[
\gamma = (M,g_{\mu\nu},\Phi).
\]

The quantum theory assigns an amplitude functional to sets of histories. The fundamental object is not \(\ket{\psi(t)}\), but

\[
\mathcal{A}(A)
=
\sum_{\gamma\in A}
e^{iS[\gamma]/\hbar},
\]

or, in the continuum,

\[
\mathcal{A}(A)
=
\int_A
\mathcal{D}\gamma\,
e^{iS[\gamma]/\hbar}.
\]

The quantum measure is then

\[
\mu(A)
=
|\mathcal{A}(A)|^2.
\]

This is the foundational equation of Quantum-Histories Relativity.

---

## 3. Quantum Measure Theory

Classical probability theory is based on a measure

\[
P:\mathcal{E}\rightarrow [0,1],
\]

defined on an event algebra \(\mathcal{E}\), satisfying countable additivity:

\[
P(A\cup B)
=
P(A)+P(B)
\]

for disjoint \(A,B\).

Quantum measure theory, developed by Sorkin, generalizes this.

A quantum measure \(\mu\) is a map

\[
\mu:\mathcal{E}\rightarrow \mathbb{R}_{\geq 0}
\]

satisfying:

1. positivity,

\[
\mu(A)\geq 0;
\]

2. null empty set,

\[
\mu(\varnothing)=0;
\]

3. normalization,

\[
\mu(\Omega)=1;
\]

4. grade-2 additivity.

Grade-2 additivity means that for three disjoint sets \(A,B,C\),

\[
\mu(A\cup B\cup C)
=
\mu(A\cup B)
+
\mu(A\cup C)
+
\mu(B\cup C)
-
\mu(A)
-
\mu(B)
-
\mu(C).
\]

Equivalently, the third-order interference functional vanishes:

\[
I_3(A,B,C)
=
\mu(A\cup B\cup C)
-
\mu(A\cup B)
-
\mu(A\cup C)
-
\mu(B\cup C)
+
\mu(A)
+
\mu(B)
+
\mu(C)
=
0.
\]

Classical probability is grade-1 additive. Quantum theory is grade-2 additive.

This is the mathematical signature of interference.

---

## 4. Interference and the Double-Slit Lesson

The double-slit experiment illustrates why a classical probability measure is insufficient.

Let \(A\) be the set of histories passing through slit \(A\), and \(B\) the set passing through slit \(B\).

Classically,

\[
P(A\cup B)
=
P(A)+P(B).
\]

Quantum mechanically,

\[
\mu(A\cup B)
=
\mu(A)+\mu(B)+I(A,B),
\]

where the interference term is

\[
I(A,B)
=
\mathcal{A}(A)\mathcal{A}^*(B)
+
\mathcal{A}^*(A)\mathcal{A}(B).
\]

Thus,

\[
\mu(A\cup B)
=
|\mathcal{A}(A)+\mathcal{A}(B)|^2.
\]

The quantum measure is not additive over alternatives because histories interfere.

The central lesson is:

\[
\boxed{
\text{Sets of histories, not individual histories, carry physical weight.}
}
\]

---

## 5. Consistent Histories and Decoherence

The consistent-histories formulation gives a precise criterion for when probabilities may be assigned to histories.

Let a history \(\alpha\) be a sequence of alternatives at times \(t_1,\ldots,t_n\):

\[
\alpha
=
(\alpha_1,\alpha_2,\ldots,\alpha_n).
\]

Each alternative is represented by a projection operator \(P_{\alpha_k}^{(k)}\).

The class operator for the history \(\alpha\) is

\[
C_\alpha
=
P_{\alpha_n}^{(n)}
\cdots
P_{\alpha_2}^{(2)}
P_{\alpha_1}^{(1)}.
\]

Given an initial density matrix \(\rho\), the decoherence functional is

\[
D(\alpha,\beta)
=
\operatorname{Tr}
\left(
C_\alpha
\rho
C_\beta^\dagger
\right).
\]

The diagonal elements are candidate probabilities:

\[
p(\alpha)
=
D(\alpha,\alpha).
\]

But probabilities are meaningful only if the off-diagonal elements vanish or are negligible:

\[
D(\alpha,\beta)
\approx
0
\quad
\text{for}
\quad
\alpha\neq\beta.
\]

This is the decoherence condition.

When it holds, the set of histories is called a consistent or decoherent set.

Only within a decoherent set may one say:

\[
\text{History } \alpha \text{ occurred with probability } p(\alpha).
\]

---

## 6. Realms and Quasiclassicality

A realm is a complete, exclusive, decoherent set of coarse-grained histories.

Different realms may be mutually incompatible. One realm may describe particle trajectories. Another may describe wave interference. Another may describe hydrodynamic variables.

A quasiclassical realm is a realm whose histories follow approximately classical equations for coarse-grained variables such as:

1. density,
2. momentum,
3. temperature,
4. electromagnetic fields,
5. metric geometry.

The emergence of classical spacetime is the emergence of a quasiclassical realm from the quantum measure.

Thus:

\[
\boxed{
\text{Classical reality is a decoherent realm of histories.}
}
\]

There is no need to select one fine-grained history as “the real one.” The physical content is the quantum measure plus the structure of decoherent realms.

---

## 7. Path Integrals as Quantum Measures

The path integral provides the most familiar realization of a quantum measure.

For a scalar field \(\phi\), the amplitude for a set of field histories \(A\) is

\[
\mathcal{A}(A)
=
\int_A
\mathcal{D}\phi\,
e^{iS[\phi]/\hbar}.
\]

The action is

\[
S[\phi]
=
\int d^4x\,
\sqrt{-g}
\left[
-
\frac{1}{2}
g^{\mu\nu}
\partial_\mu\phi
\partial_\nu\phi
-
V(\phi)
\right].
\]

The quantum measure is

\[
\mu(A)
=
|\mathcal{A}(A)|^2.
\]

For gravity, the histories include metrics:

\[
\mathcal{A}(A)
=
\int_A
\mathcal{D}g_{\mu\nu}
\mathcal{D}\Phi
\,
e^{iS[g,\Phi]/\hbar},
\]

with

\[
S[g,\Phi]
=
\frac{1}{16\pi G}
\int d^4x\,
\sqrt{-g}
\left(
R-2\Lambda
\right)
+
S_{\text{matter}}[g,\Phi].
\]

Thus a quantum-gravitational history is not a field on spacetime. It is a spacetime itself.

---

## 8. Classical Limit: Stationary Phase and Decoherence

Classical equations emerge in two steps.

First, when the action is large compared with \(\hbar\), the path integral is dominated by stationary points:

\[
\delta S[\gamma]=0.
\]

For a field theory, this gives the Euler–Lagrange equations.

For gravity,

\[
\delta S[g]=0
\]

gives the Einstein equation,

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
8\pi G T_{\mu\nu}.
\]

Second, decoherence suppresses interference between alternative coarse-grained histories.

When both conditions hold, the quantum measure concentrates on histories satisfying classical equations.

Thus:

\[
\boxed{
\text{Classical spacetime is a stationary, decohered sector of the quantum measure.}
}
\]

---

## 9. Histories Without External Time

One of the deepest advantages of the histories formulation is that it does not require an external time parameter.

In canonical quantum gravity, the Wheeler–DeWitt equation,

\[
\hat{\mathcal{H}}\Psi=0,
\]

suggests a timeless quantum state.

The histories formulation avoids the problem by treating entire histories as primary.

A history is not “the universe at time \(t\).” It is the whole four-dimensional process.

Time appears only as an internal ordering within a coarse-grained history.

This makes the histories formulation naturally compatible with general covariance.

The principle is:

\[
\boxed{
\text{The fundamental description is time-neutral. Time emerges inside decoherent histories.}
}
\]

---

## 10. Quantum Cosmology and the Wavefunction of the Universe

In quantum cosmology, one applies the path integral to the universe as a whole.

The Hartle–Hawking no-boundary proposal defines the wavefunction of the universe by a Euclidean path integral:

\[
\Psi[h_{ij},\phi_0]
=
\int_{\substack{
g|_{\partial M}=h\\
\Phi|_{\partial M}=\phi_0
}}
\mathcal{D}g\,\mathcal{D}\Phi\,
e^{-I_E[g,\Phi]/\hbar},
\]

where \(I_E\) is the Euclidean action.

The Lorentzian version is

\[
\Psi[h_{ij},\phi_0]
=
\int
\mathcal{D}g\,\mathcal{D}\Phi\,
e^{iS[g,\Phi]/\hbar}.
\]

The wavefunction is not a state in external time. It is an amplitude over histories matching boundary data.

Classical cosmological histories emerge as WKB branches:

\[
\Psi[h,\phi]
\sim
A[h,\phi]
e^{iS[h,\phi]/\hbar}.
\]

The phase \(S\) satisfies the Hamilton–Jacobi equation, from which classical Friedmann dynamics follows.

Thus the universe is not a single classical solution. It is a quantum measure over cosmological histories.

---

## 11. Decoherence of Cosmological Perturbations

Inflationary cosmology provides a concrete example.

Quantum fluctuations of the inflaton field begin in a nearly Gaussian vacuum state. Their modes are stretched beyond the Hubble radius. Interaction with unobserved environmental degrees of freedom, or with short-wavelength modes, causes decoherence.

The reduced density matrix for long-wavelength perturbations becomes approximately diagonal in the field-amplitude basis:

\[
\rho[\phi,\phi']
\rightarrow
\rho[\phi,\phi]
\delta[\phi-\phi'].
\]

The corresponding histories decohere.

The result is a stochastic classical distribution of primordial perturbations:

\[
P[\phi]
\sim
\exp
\left[
-
\frac{1}{2}
\int d^3k\,
\frac{|\phi_{\mathbf{k}}|^2}{P(k)}
\right].
\]

Thus the observed cosmic microwave background anisotropies are records of decohered quantum histories.

---

## 12. Causal Sets as Quantum Histories

Causal-set theory provides a discrete version of Quantum-Histories Relativity.

A causal set is a locally finite partially ordered set,

\[
(C,\prec).
\]

A history is a growth process in which elements are added one by one while preserving causal order.

In classical sequential growth models, one assigns transition probabilities to growth steps. The resulting measure over completed causal sets is classical.

In quantum sequential growth, one assigns amplitudes instead of probabilities:

\[
\mathcal{A}(C)
=
\sum_{\text{growth paths to }C}
e^{iS[\text{path}]/\hbar}.
\]

The quantum measure is

\[
\mu(A)
=
\left|
\sum_{C\in A}
\mathcal{A}(C)
\right|^2.
\]

Classical spacetime emerges when a decoherent family of causal sets approximates a Lorentzian manifold.

Thus:

\[
\boxed{
\text{Spacetime is a decoherent sector of a quantum measure over causal sets.}
}
\]

---

## 13. Spin Foams as Histories of Quantum Geometry

In loop quantum gravity, spatial geometry is represented by spin networks.

A spin network is a graph \(\Gamma\) with:

- edges labeled by representations \(j_e\),
- vertices labeled by intertwiners \(i_v\).

A spin foam is a history of spin networks.

It is a two-complex with:

- faces \(f\),
- edges \(e\),
- vertices \(v\).

The spin-foam amplitude is

\[
Z
=
\sum_{\{j_f,i_e\}}
\prod_f A_f(j_f)
\prod_e A_e(j_f,i_e)
\prod_v A_v(j_f,i_e).
\]

Each spin foam represents a quantum spacetime history.

The boundary amplitude between initial and final spin networks \(s_i,s_f\) is

\[
W(s_i,s_f)
=
\sum_{\text{foams }F:\partial F=s_i\cup s_f}
A(F).
\]

Thus spin-foam theory is a concrete realization of Quantum-Histories Relativity:

\[
\boxed{
\text{Quantum gravity is a sum over histories of quantum geometry.}
}
\]

---

## 14. Group Field Theory and Histories of Universes

Group field theory provides a field-theoretic framework for spin foams.

A group field is a function

\[
\varphi:
G^d
\rightarrow
\mathbb{C},
\]

where \(G\) is a Lie group such as \(SU(2)\), \(Spin(4)\), or \(SL(2,\mathbb{C})\).

The partition function is

\[
Z_{\text{GFT}}
=
\int \mathcal{D}\varphi\,
e^{-S[\varphi]}.
\]

Its Feynman expansion generates spin foams:

\[
Z_{\text{GFT}}
=
\sum_{\Gamma}
\frac{\lambda^{N_\Gamma}}{\mathrm{sym}(\Gamma)}
Z_\Gamma.
\]

Each Feynman diagram \(\Gamma\) is a quantum spacetime history.

Because group field theory is a second-quantized theory of spin networks, it can describe processes in which spatial topology changes. It is therefore a theory of histories of universes.

The principle becomes:

\[
\boxed{
\text{Spacetimes are quanta; universes are histories; reality is their quantum measure.}
}
\]

---

## 15. Causal Dynamical Triangulations

Causal dynamical triangulations, or CDT, provide another histories-based approach.

The gravitational path integral is approximated by a sum over piecewise-linear Lorentzian geometries:

\[
Z
=
\sum_{\mathcal{T}}
\frac{1}{C_{\mathcal{T}}}
e^{iS_{\text{Regge}}[\mathcal{T}]/\hbar}.
\]

After a Wick rotation, one obtains a statistical sum over causal triangulations.

Numerical simulations show that, at large scales, an emergent four-dimensional de Sitter-like geometry appears.

Thus classical spacetime arises as a collective phase in a quantum measure over triangulated histories.

---

## 16. Histories and the Problem of Measurement

In standard quantum mechanics, measurement is often treated as a special process involving collapse.

In the histories formulation, measurement is just another physical interaction within a history.

A measurement apparatus is a subsystem whose macroscopic pointer states decohere.

A measurement outcome corresponds to a coarse-grained set of histories in which the pointer variable takes a definite value.

When the relevant histories decohere, probabilities may be assigned:

\[
p(\text{outcome }a)
=
D(a,a).
\]

There is no fundamental collapse postulate.

The appearance of collapse is the restriction to a decoherent branch of the quantum measure.

---

## 17. Co-Events and Anhomic Logic

Quantum measure theory raises an ontological question:

\[
\text{If the measure is over sets of histories, what actually happens?}
\]

One answer is the co-event interpretation.

A co-event is a map

\[
\phi:
\mathcal{E}
\rightarrow
\mathbb{Z}_2,
\]

assigning truth values to events.

A co-event is preclusive if

\[
\mu(A)=0
\quad
\Rightarrow
\quad
\phi(A)=0.
\]

It is multiplicative if

\[
\phi(A\cap B)
=
\phi(A)\phi(B).
\]

The actual world is represented by a single co-event.

But the logic is not classical Boolean logic. It is an anhomic logic adapted to quantum interference.

Thus one may say:

\[
\boxed{
\text{Reality is a single co-event compatible with the quantum measure.}
}
\]

This provides a realist interpretation of Quantum-Histories Relativity without selecting a single fine-grained history.

---

## 18. Histories and Categorical Relativity

Quantum-Histories Relativity is closely related to Relativity 15.0, Categorical Relativity.

In categorical terms:

- objects are boundary data,
- morphisms are histories or cobordisms,
- amplitudes are functors to vector spaces,
- composition is gluing of histories.

The path integral becomes a functor,

\[
Z:
\mathbf{Hist}
\rightarrow
\mathbf{Hilb},
\]

or more generally,

\[
Z:
\mathbf{Bord}_n
\rightarrow
\mathbf{Vect}.
\]

The quantum measure is then the squared norm of the amplitude assigned to a set of morphisms.

Thus histories are morphisms, and reality is the categorical quantum measure over them.

---

## 19. Histories and Entropic Relativity

Quantum-Histories Relativity also connects to Relativity 17.0, Entropic Relativity.

The decoherence functional defines an information geometry on the space of coarse-grained histories.

Relative entropy between decoherent history distributions measures distinguishability:

\[
D[p\|q]
=
\sum_\alpha
p(\alpha)
\ln
\frac{p(\alpha)}{q(\alpha)}.
\]

The Fisher information metric on the space of history probabilities is

\[
g_{ij}
=
\left\langle
\partial_i \ln p(\alpha)
\partial_j \ln p(\alpha)
\right\rangle.
\]

Classical realms are then approximately geodesic flows on this information manifold.

Thus inference, entropy, and histories are unified.

---

## 20. Axioms of Quantum-Histories Relativity

The framework may be organized around eight axioms.

### Axiom 1: Histories Are Fundamental

The primitive objects are complete histories \(\gamma\), not instantaneous states.

### Axiom 2: Sets of Histories Carry Amplitude

Physical amplitudes are assigned to sets \(A\subset\Omega\):

\[
\mathcal{A}(A)
=
\int_A
\mathcal{D}\gamma\,
e^{iS[\gamma]/\hbar}.
\]

### Axiom 3: The Quantum Measure Is Grade-2

The measure

\[
\mu(A)=|\mathcal{A}(A)|^2
\]

is grade-2 additive and permits pairwise interference but no third-order interference.

### Axiom 4: Probabilities Require Decoherence

Probabilities are assigned only within decoherent sets of histories satisfying

\[
D(\alpha,\beta)\approx 0
\quad
\text{for}
\quad
\alpha\neq\beta.
\]

### Axiom 5: Classical Spacetime Is a Realm

A classical spacetime is a quasiclassical decoherent realm of the quantum measure.

### Axiom 6: Time Is Internal

Time is not fundamental. It is an ordering variable within histories.

### Axiom 7: Gravity Is Summed Over Geometries

Quantum gravity is a measure over histories of geometry, topology, and causal structure.

### Axiom 8: Reality Is Measure plus Co-Event

If a realist interpretation is desired, reality is a preclusive co-event compatible with the quantum measure.

---

## 21. Relation to Previous Versions of Relativity

Quantum-Histories Relativity integrates earlier versions.

| Version | Histories interpretation |
|---|---|
| Relativity 3.0: Effective Quantum Relativity | Low-energy histories of metric perturbations |
| Relativity 4.0: Background-Independent Quantum Geometry | Histories of spin networks and discrete geometries |
| Relativity 5.0: Holographic Relativity | Boundary histories encoding bulk histories |
| Relativity 6.0: Thermodynamic Relativity | Decoherent thermodynamic histories |
| Relativity 11.0: Celestial Relativity | Asymptotic histories at null infinity |
| Relativity 13.0: Causal-Informational Relativity | Histories of causal-informational events |
| Relativity 15.0: Categorical Relativity | Histories as morphisms/cobordisms |
| Relativity 17.0: Entropic Relativity | Decoherent history probabilities as inference |
| Relativity 18.0: Quantum-Histories Relativity | Fundamental quantum measure over all histories |

The conceptual progression is:

\[
\text{states}
\rightarrow
\text{histories}
\rightarrow
\text{measures over histories}
\rightarrow
\text{decoherent realms}.
\]

---

## 22. Observational and Experimental Relevance

Quantum-Histories Relativity is not a single phenomenological model. It is a foundational framework underlying many calculational methods.

Its empirical relevance appears through:

1. path-integral predictions in quantum field theory,
2. inflationary perturbation spectra,
3. decoherence of cosmological fluctuations,
4. quantum interference experiments,
5. spin-foam amplitudes,
6. causal-set phenomenology,
7. group-field-theory cosmology,
8. no-boundary and tunneling cosmological proposals.

Direct tests of the full histories ontology are difficult. But the framework is indispensable for quantum cosmology and quantum gravity, where no external observer or external time is available.

---

## 23. Open Problems

Several major problems remain.

### 23.1 Mathematical Rigor

Continuum path integrals over fields and geometries are not fully rigorous.

### 23.2 Lorentzian Quantum Gravity

Most well-defined path integrals are Euclidean. The Lorentzian theory remains difficult.

### 23.3 Realm Selection

Many decoherent realms may exist. What selects the quasiclassical realm we observe?

### 23.4 Probability Interpretation

The meaning of probability in a single universe remains subtle.

### 23.5 Co-Event Dynamics

The co-event interpretation is promising but not yet fully developed for realistic quantum field theories.

### 23.6 Continuum Limit of Discrete Histories

Causal sets, spin foams, and triangulations must reproduce continuum general relativity in the appropriate limit.

### 23.7 Relation to Observers

Observers are histories within the measure. A complete account of self-locating probability and observational conditioning remains open.

---

## 24. What Einstein Would Think

Einstein would find Quantum-Histories Relativity both powerful and unsettling.

He would appreciate its covariance and its time-neutral structure. The idea that the fundamental description is a four-dimensional whole rather than an evolving three-dimensional slice is compatible with the spirit of general relativity.

He would also appreciate the path-integral emphasis on invariant action principles.

But Einstein resisted irreducible probability. The idea that reality is a quantum measure over histories, rather than a single deterministic geometry, would trouble him.

Still, he would recognize the central lesson:

\[
\boxed{
\text{The physical world is not a sequence of instantaneous states. It is a structured whole.}
}
\]

Quantum-Histories Relativity generalizes that whole into a quantum measure over all possible wholes.

---

## 25. Summary of Core Equations

### History amplitude

\[
\mathcal{A}(A)
=
\int_A
\mathcal{D}\gamma\,
e^{iS[\gamma]/\hbar}.
\]

### Quantum measure

\[
\mu(A)
=
|\mathcal{A}(A)|^2.
\]

### Grade-2 additivity

\[
\mu(A\cup B\cup C)
=
\mu(A\cup B)
+
\mu(A\cup C)
+
\mu(B\cup C)
-
\mu(A)
-
\mu(B)
-
\mu(C).
\]

### Vanishing third-order interference

\[
I_3(A,B,C)=0.
\]

### Class operator

\[
C_\alpha
=
P_{\alpha_n}^{(n)}
\cdots
P_{\alpha_1}^{(1)}.
\]

### Decoherence functional

\[
D(\alpha,\beta)
=
\operatorname{Tr}
\left(
C_\alpha
\rho
C_\beta^\dagger
\right).
\]

### Decoherence condition

\[
D(\alpha,\beta)
\approx
0
\quad
\text{for}
\quad
\alpha\neq\beta.
\]

### History probability

\[
p(\alpha)
=
D(\alpha,\alpha).
\]

### Gravitational path integral

\[
Z
=
\int
\mathcal{D}g_{\mu\nu}
\mathcal{D}\Phi
\,
e^{iS[g,\Phi]/\hbar}.
\]

### Einstein action

\[
S[g,\Phi]
=
\frac{1}{16\pi G}
\int d^4x
\sqrt{-g}
\left(
R-2\Lambda
\right)
+
S_{\text{matter}}.
\]

### Spin-foam amplitude

\[
Z
=
\sum_{\{j_f,i_e\}}
\prod_f A_f
\prod_e A_e
\prod_v A_v.
\]

### Hartle–Hawking wavefunction

\[
\Psi[h,\phi]
=
\int_{\partial M=(h,\phi)}
\mathcal{D}g\,\mathcal{D}\Phi\,
e^{-I_E[g,\Phi]/\hbar}.
\]

---

## 26. Conclusion

Relativity 18.0, Quantum-Histories Relativity, proposes that the fundamental object of physics is not a state, not a trajectory, and not a single spacetime. It is a quantum measure over histories.

The central equation is

\[
\mu(A)
=
\left|
\sum_{\gamma\in A}
e^{iS[\gamma]/\hbar}
\right|^2.
\]

The central principle is

\[
\boxed{
\text{Reality is a quantum measure over histories, not a single classical trajectory.}
}
\]

Classical spacetime is not denied. It is explained. It is a decoherent realm: a coarse-grained family of histories whose interference is negligible and whose stationary-phase structure obeys Einstein’s equations.

Causal sets, spin foams, group field theory, causal dynamical triangulations, consistent histories, and cosmological path integrals are all partial realizations of this framework.

Quantum-Histories Relativity is therefore one of the most general formulations of quantum gravity and quantum cosmology. It says that the universe is not a single story. It is a quantum measure over all possible stories, from which classical reality emerges as a decoherent chapter.

This is Relativity 18.0.

---

## Appendix A: Grade-2 Additivity from Path Integrals

Let \(A,B,C\) be disjoint sets of histories. Define

\[
\mathcal{A}(A)
=
\sum_{\gamma\in A}
e^{iS[\gamma]/\hbar}.
\]

Then

\[
\mu(A\cup B)
=
|\mathcal{A}(A)+\mathcal{A}(B)|^2
=
\mu(A)+\mu(B)
+
\mathcal{A}(A)\mathcal{A}^*(B)
+
\mathcal{A}^*(A)\mathcal{A}(B).
\]

For three sets,

\[
\mu(A\cup B\cup C)
=
|\mathcal{A}(A)+\mathcal{A}(B)+\mathcal{A}(C)|^2.
\]

Expanding and combining terms gives

\[
I_3(A,B,C)
=
\mu(A\cup B\cup C)
-
\mu(A\cup B)
-
\mu(A\cup C)
-
\mu(B\cup C)
+
\mu(A)
+
\mu(B)
+
\mu(C)
=
0.
\]

Thus standard quantum theory has pairwise interference but no third-order interference.

---

## Appendix B: Decoherence Functional from Path Integrals

For histories \(x(t)\) and \(y(t)\), the decoherence functional may be written as

\[
D(\alpha,\beta)
=
\int_{\alpha}\mathcal{D}x
\int_{\beta}\mathcal{D}y
\,
e^{i(S[x]-S[y])/\hbar}
\rho(x_i,y_i).
\]

The diagonal term is

\[
D(\alpha,\alpha)
=
\int_{\alpha}\mathcal{D}x
\int_{\alpha}\mathcal{D}y
\,
e^{i(S[x]-S[y])/\hbar}
\rho(x_i,y_i).
\]

When off-diagonal terms vanish,

\[
D(\alpha,\beta)\approx 0,
\]

the histories \(\alpha\) decohere and may be assigned probabilities.

---

## Appendix C: Semiclassical Histories

Suppose the wavefunction has WKB form,

\[
\Psi
\sim
A
e^{iS/\hbar}.
\]

The phase \(S\) satisfies the Hamilton–Jacobi equation.

For gravity,

\[
\mathcal{H}
\left(
h_{ij},
\frac{\delta S}{\delta h_{ij}}
\right)
=
0.
\]

The trajectories orthogonal to surfaces of constant \(S\) satisfy the classical Einstein equations.

Thus semiclassical histories are stationary-phase histories of the gravitational path integral.

---

## Appendix D: Spin-Foam Histories

A spin foam \(F\) has faces \(f\), edges \(e\), and vertices \(v\).

Its amplitude is

\[
A(F)
=
\prod_f A_f(j_f)
\prod_e A_e(j_f,i_e)
\prod_v A_v(j_f,i_e).
\]

The transition amplitude between spin networks \(s_i\) and \(s_f\) is

\[
W(s_i,s_f)
=
\sum_{F:\partial F=s_i\cup s_f}
A(F).
\]

Each foam is a quantum spacetime history.

---

## Appendix E: Causal-Set Quantum Measure

Let \(\Omega\) be the space of completed causal sets generated by a quantum growth process.

For a set \(A\subset\Omega\), define

\[
\mathcal{A}(A)
=
\sum_{C\in A}
\sum_{\text{growth paths to }C}
e^{iS[\text{path}]/\hbar}.
\]

The quantum measure is

\[
\mu(A)
=
|\mathcal{A}(A)|^2.
\]

Classical spacetime corresponds to a decoherent family of causal sets whose order-plus-number structure approximates a Lorentzian manifold.

---

## Selected References

1. R. P. Feynman and A. R. Hibbs, *Quantum Mechanics and Path Integrals* (McGraw-Hill, 1965).  
2. L. S. Schulman, *Techniques and Applications of Path Integration* (Wiley, 1981).  
3. R. B. Griffiths, “Consistent Histories and the Interpretation of Quantum Mechanics,” *Journal of Statistical Physics* **36**, 219 (1984).  
4. R. Omnès, *The Interpretation of Quantum Mechanics* (Princeton University Press, 1994).  
5. M. Gell-Mann and J. B. Hartle, “Quantum Mechanics in the Light of Quantum Cosmology,” in *Complexity, Entropy, and the Physics of Information* (Addison-Wesley, 1990).  
6. M. Gell-Mann and J. B. Hartle, “Classical Equations for Quantum Systems,” *Physical Review D* **47**, 3345 (1993).  
7. J. B. Hartle, “Spacetime Quantum Mechanics and the Quantum Mechanics of Spacetime,” in *Gravitation and Quantizations* (Elsevier, 1995).  
8. C. J. Isham, “Quantum Logic and the Histories Approach to Quantum Theory,” *Journal of Mathematical Physics* **35**, 2157 (1994).  
9. C. J. Isham and N. Linden, “Continuous Temporal Schema Theories,” *Journal of Mathematical Physics* **36**, 5392 (1995).  
10. R. D. Sorkin, “Quantum Mechanics as Quantum Measure Theory,” *Modern Physics Letters A* **9**, 3119 (1994).  
11. R. D. Sorkin, “Quantum Measure Theory and Its Interpretation,” in *Quantum Classical Correspondence* (International Press, 1997).  
12. F. Dowker, “Causal Sets and the Deep Structure of Spacetime,” in *100 Years of Relativity* (World Scientific, 2005).  
13. D. P. Rideout and R. D. Sorkin, “A Classical Sequential Growth Dynamics for Causal Sets,” *Physical Review D* **61**, 024002 (1999).  
14. R. D. Sorkin, “Causal Sets: Discrete Gravity,” in *Lectures on Quantum Gravity* (World Scientific, 2005).  
15. C. Rovelli, “Spin Networks,” *Physical Review D* **43**, 442 (1991).  
16. J. C. Baez, “Spin Foam Models,” *Classical and Quantum Gravity* **15**, 1827 (1998).  
17. A. Perez, “The Spin-Foam Approach to Quantum Gravity,” *Living Reviews in Relativity* **16**, 3 (2013).  
18. D. Oriti, ed., *Approaches to Quantum Gravity: Toward a New Understanding of Space, Time and Matter* (Cambridge University Press, 2009).  
19. D. Oriti, “Group Field Theory and Loop Quantum Gravity,” *Reports on Progress in Physics* **82**, 124001 (2019).  
20. J. Ambjørn, J. Jurkiewicz, and R. Loll, “The Emergence of Spacetime from Quantum Gravity,” *Physical Review Letters* **93**, 131301 (2004).  
21. J. B. Hartle and S. W. Hawking, “Wave Function of the Universe,” *Physical Review D* **28**, 2960 (1983).  
22. A. Vilenkin, “Creation of Universes from Nothing,” *Physics Letters B* **117**, 25 (1982).  
23. B. S. DeWitt, “Quantum Theory of Gravity. I–III,” *Physical Review* **160**, 1113; **162**, 1195; **162**, 1239 (1967).  
24. J. J. Halliwell, “Decoherent Histories and the Interpretation of Quantum Cosmology,” *Physical Review D* **39**, 2912 (1989).  
25. F. Dowker and S. Surya, “Quantum Measure Theory and the Histories Approach to Quantum Gravity,” *Classical and Quantum Gravity* (various articles).

# Relativity 29.0 — Vacuum Relativity  
## The Observer-, Horizon-, and Code-Subspace-Dependence of Empty Space

**White paper / academic preprint**

---

## Abstract

Vacuum Relativity is the hypothesis that the quantum vacuum is not an absolute state of nature but a relational structure defined relative to observers, horizons, acceleration, causal access, and code subspaces. The Minkowski vacuum, which an inertial observer calls empty space, appears to a uniformly accelerated Rindler observer as a thermal bath with the Unruh temperature,

\[
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
\]

The relation between inertial and accelerated particle interpretations is given by a Bogoliubov transformation,

\[
a_k^{R}
=
\cosh r\, a_k^{M}
-
\sinh r\, a_{-k}^{M\dagger},
\]

showing that the notion of a particle, and therefore the notion of emptiness, is frame-dependent. Analogous phenomena occur in de Sitter space, where static observers detect a Gibbons–Hawking temperature,

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}},
\]

and near black holes, where different observers naturally associate different vacua: Boulware, Unruh, Hartle–Hawking, and infalling vacua. In holographic quantum gravity, the vacuum is further relativized by code subspaces: different effective bulk vacua correspond to different sectors of the boundary Hilbert space. The central principle is:

\[
\boxed{
\text{The vacuum is not a universal state. It is an observer- and horizon-relative state.}
}
\]

What one observer calls empty space, another may call a thermal bath, a squeezed state, a false vacuum, or an encoded interior. Vacuum Relativity unifies the Unruh effect, Hawking radiation, de Sitter thermality, algebraic quantum field theory, and holographic code-subspace reconstruction into a single relativistic framework.

---

## 1. Introduction

In classical physics, the vacuum is simple.

It is the absence of matter. It is the state with no particles. It is the lowest-energy configuration of fields. It is absolute.

Quantum field theory complicates this picture.

The vacuum is not mere nothingness. It is a highly structured quantum state with fluctuations, correlations, entanglement, and observer-dependent particle content.

The most striking demonstration is the Unruh effect. An inertial observer in Minkowski spacetime describes the quantum field as being in the vacuum state \(\ket{0_M}\). A uniformly accelerated observer describes the same state as a thermal density matrix at temperature

\[
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
\]

Thus the statement “there are no particles” is not invariant.

Vacuum Relativity generalizes this lesson.

The vacuum is not a global absolute state. It is defined relative to:

1. an observer’s worldline,
2. a choice of time evolution,
3. a causal horizon,
4. an accessible algebra of observables,
5. a mode decomposition,
6. a code subspace,
7. a cosmological boundary condition,
8. a holographic reconstruction frame.

The invariant is not the vacuum itself. The invariant is the full relational structure connecting all observer-relative vacua.

---

## 2. The Classical Vacuum and Its Limits

In classical field theory, a vacuum is a field configuration minimizing the energy.

For a scalar field with potential \(V(\phi)\), the vacuum satisfies

\[
\frac{dV}{d\phi}=0,
\]

and stability requires

\[
\frac{d^2V}{d\phi^2}\geq 0.
\]

If the potential has multiple minima, there may be several classical vacua.

But even here, the vacuum is not purely local. In gauge theory, vacua may be labeled by topological sectors, holonomies, winding numbers, and boundary conditions.

In quantum field theory, the vacuum becomes a state in Hilbert space:

\[
\ket{0}.
\]

It is usually defined as the state annihilated by all annihilation operators:

\[
a_k\ket{0}=0.
\]

But the operators \(a_k\) depend on a choice of modes. Different observers naturally choose different modes.

Therefore different observers define different annihilation operators, different particles, and different vacua.

---

## 3. Mode Decompositions and Particle Relativity

Consider a quantum field \(\phi(x)\).

One observer expands it in modes \(u_k\):

\[
\phi
=
\sum_k
\left(
a_k u_k
+
a_k^\dagger u_k^*
\right).
\]

Another observer expands the same field in modes \(v_j\):

\[
\phi
=
\sum_j
\left(
b_j v_j
+
b_j^\dagger v_j^*
\right).
\]

The two sets of modes are related by a Bogoliubov transformation:

\[
v_j
=
\sum_k
\left(
\alpha_{jk}u_k
+
\beta_{jk}u_k^*
\right).
\]

The corresponding annihilation operators satisfy

\[
b_j
=
\sum_k
\left(
\alpha_{jk}^* a_k
-
\beta_{jk}^* a_k^\dagger
\right).
\]

If \(\beta_{jk}\neq 0\), the two observers disagree about particles.

The vacuum of the \(a\)-modes satisfies

\[
a_k\ket{0_a}=0.
\]

But the expected number of \(b\)-particles in that state is

\[
\langle 0_a|
b_j^\dagger b_j
|0_a\rangle
=
\sum_k
|\beta_{jk}|^2.
\]

Thus:

\[
\boxed{
\text{Particles are not absolute. They are relative to a mode decomposition.}
}
\]

Since the vacuum is defined as “no particles,” the vacuum is also relative.

---

## 4. Rindler Coordinates and Accelerated Observers

Minkowski spacetime in \(1+1\) dimensions has metric

\[
ds^2
=
-c^2dt^2+dx^2.
\]

A uniformly accelerated observer naturally uses Rindler coordinates \((\eta,\xi)\), defined by

\[
ct
=
\xi\sinh\eta,
\]

\[
x
=
\xi\cosh\eta,
\]

with \(\xi>0\).

The metric becomes

\[
ds^2
=
-\xi^2 d\eta^2
+
d\xi^2.
\]

Restoring acceleration units, one often writes

\[
ds^2
=
-
\left(
1+\frac{a\chi}{c^2}
\right)^2
c^2d\tau^2
+
d\chi^2
+
dy^2+dz^2.
\]

The surface \(\xi=0\) is a horizon. The right Rindler wedge is causally inaccessible to certain accelerated observers beyond that horizon.

The time coordinate \(\eta\) is generated not by ordinary time translations but by Lorentz boosts.

Thus the Hamiltonian of the accelerated observer is a boost generator.

This is the geometric origin of the Unruh effect.

---

## 5. The Unruh Effect

Let \(\ket{0_M}\) be the Minkowski vacuum.

An inertial observer defines particles using positive-frequency modes with respect to Minkowski time \(t\).

A Rindler observer defines particles using positive-frequency modes with respect to Rindler time \(\eta\).

The two mode decompositions are related by a Bogoliubov transformation. Schematically,

\[
a_k^{R}
=
\cosh r_k\, a_k^{M}
-
\sinh r_k\, a_{-k}^{M\dagger}.
\]

The parameter \(r_k\) is a squeezing parameter satisfying

\[
e^{-2\pi\omega_k/a}
=
\tanh^2 r_k.
\]

The Minkowski vacuum can be written as a two-mode squeezed state entangling right and left Rindler modes:

\[
\ket{0_M}
=
\prod_k
\left(
1-e^{-2\pi\omega_k/a}
\right)^{1/2}
\sum_{n=0}^{\infty}
e^{-\pi n\omega_k/a}
\ket{n_k}_R
\ket{n_k}_L.
\]

An accelerated observer confined to the right Rindler wedge cannot access the left wedge. Tracing over the left wedge gives

\[
\rho_R
=
\operatorname{Tr}_L
\ket{0_M}\bra{0_M}.
\]

The result is thermal:

\[
\rho_R
=
\frac{e^{-\beta H_R}}{Z},
\]

with

\[
\beta
=
\frac{2\pi}{a}
\]

in natural units.

Restoring constants,

\[
k_{\text{B}}T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi c}.
\]

Thus:

\[
\boxed{
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
}
\]

The Minkowski vacuum is empty for an inertial observer but thermal for an accelerated observer.

---

## 6. Detector Response and Operational Meaning

The Unruh effect is not merely a formal statement about modes. It is operationally measurable by an accelerated detector.

An Unruh–DeWitt detector couples to a field along a worldline \(x(\tau)\):

\[
H_{\text{int}}
=
c\,m(\tau)\phi(x(\tau)),
\]

where \(m(\tau)\) is the detector monopole moment.

The transition probability from ground state to excited state is proportional to

\[
\mathcal{F}(E)
=
\int_{-\infty}^{\infty}
d\tau
\int_{-\infty}^{\infty}
d\tau'
\,
e^{-iE(\tau-\tau')}
W(x(\tau),x(\tau')),
\]

where \(W\) is the Wightman function.

For an inertial detector in the Minkowski vacuum, the excitation rate vanishes.

For a uniformly accelerated detector in the same vacuum, the response is thermal:

\[
\frac{\Gamma(E)}{\Gamma(-E)}
=
e^{-2\pi E/a}.
\]

This is a Planck distribution at temperature

\[
T=\frac{a}{2\pi}
\]

in natural units.

Thus the vacuum’s particle content is observer-dependent in an operational sense.

---

## 7. Bisognano–Wichmann Theorem and Modular Thermality

The Unruh effect has a deep algebraic formulation.

Let \(\mathcal{A}(W)\) be the algebra of observables in the right Rindler wedge \(W\).

The Minkowski vacuum state \(\omega_0\) restricted to \(\mathcal{A}(W)\) satisfies the Bisognano–Wichmann theorem:

\[
\rho_W
\propto
e^{-2\pi K},
\]

where \(K\) is the generator of Lorentz boosts preserving the wedge.

Thus the vacuum restricted to a wedge is a thermal state with respect to boost time.

In modular theory, the modular Hamiltonian is

\[
K_W
=
-\ln\rho_W.
\]

For the Rindler wedge,

\[
K_W
=
2\pi K.
\]

This shows that the thermality of the vacuum is not an artifact of particle language. It is a property of the vacuum’s entanglement structure.

---

## 8. Vacuum Entanglement and the Reeh–Schlieder Theorem

The Minkowski vacuum is highly entangled across spatial regions.

The Reeh–Schlieder theorem states that, under broad conditions, the set of states obtained by acting on the vacuum with operators localized in any open region \(\mathcal{O}\) is dense in the full Hilbert space:

\[
\overline{
\mathcal{A}(\mathcal{O})\ket{0}
}
=
\mathcal{H}.
\]

This means the vacuum contains nonlocal correlations so strong that local operations can approximate arbitrary global states.

Thus the vacuum is not empty. It is a densely structured entangled state.

Vacuum Relativity interprets this entanglement as the invariant structure underlying observer-relative particle descriptions.

---

## 9. Horizons and Traced-Out Degrees of Freedom

The thermality of the vacuum arises because an observer has access only to a subregion.

Let the full vacuum be \(\ket{0}\). Let the Hilbert space factor approximately as

\[
\mathcal{H}
\approx
\mathcal{H}_A
\otimes
\mathcal{H}_{\bar A}.
\]

An observer restricted to region \(A\) describes the state by

\[
\rho_A
=
\operatorname{Tr}_{\bar A}
\ket{0}\bra{0}.
\]

Even if the global state is pure, the reduced state is mixed:

\[
\rho_A
\neq
\ket{0}\bra{0}.
\]

The entropy

\[
S_A
=
-\operatorname{Tr}\rho_A\ln\rho_A
\]

is entanglement entropy.

In quantum field theory, this entropy is ultraviolet divergent and obeys an area law:

\[
S_A
\sim
\frac{\operatorname{Area}(\partial A)}{\epsilon^{d-2}},
\]

where \(\epsilon\) is a short-distance cutoff.

In gravity, the area law becomes the Bekenstein–Hawking entropy:

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3}.
\]

Thus horizons convert vacuum entanglement into thermodynamic entropy.

---

## 10. de Sitter Vacuum Relativity

De Sitter space provides another example.

In static coordinates, de Sitter space has metric

\[
ds^2
=
-
\left(
1-H^2r^2
\right)c^2dt^2
+
\frac{dr^2}{1-H^2r^2}
+
r^2d\Omega^2.
\]

A static observer at \(r=0\) has a cosmological horizon at

\[
r=\frac{1}{H}.
\]

The associated Gibbons–Hawking temperature is

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

The natural Euclidean or Bunch–Davies vacuum appears thermal to a static observer.

Thus:

\[
\boxed{
\text{The de Sitter vacuum is horizon-relative.}
}
\]

Different choices of vacuum, such as \(\alpha\)-vacua, correspond to different boundary conditions and observer interpretations.

In an expanding Friedmann–Lemaître–Robertson–Walker universe, there may be no global timelike Killing vector. Then there is no unique global vacuum. One instead uses adiabatic vacua, instantaneous vacua, or cosmological boundary conditions.

Thus vacuum becomes cosmology-relative.

---

## 11. Black-Hole Vacua

Black holes reveal the full richness of Vacuum Relativity.

For a Schwarzschild black hole,

\[
ds^2
=
-
\left(
1-\frac{2GM}{c^2r}
\right)c^2dt^2
+
\left(
1-\frac{2GM}{c^2r}
\right)^{-1}dr^2
+
r^2d\Omega^2.
\]

The surface gravity is

\[
\kappa
=
\frac{c^4}{4GM}.
\]

The Hawking temperature is

\[
T_{\text{H}}
=
\frac{\hbar\kappa}{2\pi k_{\text{B}}c}
=
\frac{\hbar c^3}{8\pi G M k_{\text{B}}}.
\]

Different physically natural vacua exist.

### 11.1 Boulware Vacuum

The Boulware vacuum is empty at spatial infinity but singular on the horizon.

It is natural for a static star but not for a black hole horizon.

### 11.2 Unruh Vacuum

The Unruh vacuum describes a collapsing black hole.

It is regular on the future horizon and contains outgoing Hawking radiation at infinity.

### 11.3 Hartle–Hawking Vacuum

The Hartle–Hawking vacuum describes a black hole in thermal equilibrium with its radiation.

It is regular on both past and future horizons and thermal at infinity.

### 11.4 Infalling Vacuum

A freely falling observer crossing the horizon sees no high-energy particles in the Unruh or Hartle–Hawking states, at least semiclassically.

Thus different observers associate different vacua with the same spacetime.

A static observer outside the horizon sees a thermal atmosphere.

An infalling observer sees approximately empty space near the horizon.

Thus:

\[
\boxed{
\text{The black-hole vacuum is observer-dependent.}
}
\]

---

## 12. Hawking Radiation as Vacuum Relativity

Hawking radiation arises because the notion of positive frequency changes between past and future infinity.

Modes that are positive frequency on \(\mathscr{I}^-\) become mixtures of positive and negative frequency modes on \(\mathscr{I}^+\).

The Bogoliubov coefficients satisfy approximately

\[
\left|
\frac{\beta_\omega}{\alpha_\omega}
\right|^2
=
e^{-2\pi\omega/\kappa}.
\]

The expected particle number is

\[
\langle N_\omega\rangle
=
\frac{1}{e^{2\pi\omega/\kappa}-1}.
\]

This is a thermal spectrum at temperature

\[
T_{\text{H}}
=
\frac{\kappa}{2\pi}.
\]

Thus Hawking radiation is a gravitational analogue of the Unruh effect.

The vacuum defined by the distant past is not the vacuum seen by the distant future.

---

## 13. Equivalence Principle and Local Vacuum

The equivalence principle says that locally, in a freely falling frame, physics reduces to special relativity.

Thus a freely falling observer near a black-hole horizon should see the local vacuum as approximately Minkowskian.

A static observer, however, is accelerated. To remain at fixed radius outside the horizon, the observer must accelerate with proper acceleration

\[
a(r)
=
\frac{GM}{r^2}
\left(
1-\frac{2GM}{c^2r}
\right)^{-1/2}.
\]

As \(r\) approaches the horizon, \(a(r)\to\infty\).

The local Unruh temperature is

\[
T_{\text{loc}}
=
\frac{\hbar a(r)}{2\pi k_{\text{B}}c}.
\]

Redshifted to infinity, this becomes the Hawking temperature.

Thus the black-hole thermal atmosphere can be understood as the accelerated observer’s perception of the local vacuum.

Vacuum Relativity is therefore deeply compatible with the equivalence principle.

---

## 14. Algebraic Quantum Field Theory and Observer Algebras

Algebraic quantum field theory provides the most precise language for Vacuum Relativity.

To each spacetime region \(\mathcal{O}\), one assigns an algebra of observables:

\[
\mathcal{O}
\mapsto
\mathcal{A}(\mathcal{O}).
\]

A state \(\omega\) is a positive linear functional:

\[
\omega:
\mathcal{A}
\rightarrow
\mathbb{C}.
\]

An observer with access only to region \(\mathcal{O}\) sees the restricted state:

\[
\omega_{\mathcal{O}}
=
\omega|_{\mathcal{A}(\mathcal{O})}.
\]

The same global state may look pure globally but mixed locally.

In local quantum field theory, local algebras are typically type III von Neumann algebras, meaning there is no ordinary density matrix. Nevertheless, modular theory provides a generalized notion of modular Hamiltonian and thermal behavior.

Thus the vacuum is not a state “in space.” It is a state relative to an algebra of accessible observables.

---

## 15. KMS States and Thermal Vacuum

A state is thermal at inverse temperature \(\beta\) if it satisfies the Kubo–Martin–Schwinger, or KMS, condition:

\[
\langle A(t)B\rangle
=
\langle B A(t+i\beta)\rangle.
\]

The Minkowski vacuum restricted to the Rindler wedge satisfies the KMS condition with respect to boost time at

\[
\beta
=
2\pi.
\]

Thus thermality is not merely a particle-counting artifact. It is an intrinsic property of the restricted vacuum state.

Vacuum Relativity says:

\[
\boxed{
\text{Thermal vacua are KMS restrictions of more global pure states.}
}
\]

---

## 16. Holographic Vacua and Code Subspaces

In holography, the vacuum is further relativized.

A boundary conformal field theory has a vacuum state

\[
\ket{0_{\text{CFT}}}.
\]

The bulk dual contains an effective vacuum

\[
\ket{0_{\text{bulk}}}.
\]

But bulk locality is valid only inside a code subspace:

\[
\mathcal{C}
\subset
\mathcal{H}_{\text{CFT}}.
\]

Different code subspaces can define different effective bulk geometries and different effective vacua.

A bulk operator \(\phi_{\text{bulk}}\) may be represented by different boundary operators in different boundary regions:

\[
\phi_{\text{bulk}}
\cong
\phi_A
\cong
\phi_B
\cong
\phi_C.
\]

These representations agree only on the code subspace:

\[
P_{\mathcal{C}}\phi_A P_{\mathcal{C}}
=
P_{\mathcal{C}}\phi_B P_{\mathcal{C}}.
\]

Thus the bulk vacuum is not a single absolute state in the full boundary Hilbert space. It is a code-subspace-relative effective state.

---

## 17. Entanglement Wedge Reconstruction and Vacuum Structure

In holography, a boundary region \(A\) reconstructs bulk physics in its entanglement wedge \(E(A)\).

The Ryu–Takayanagi formula gives

\[
S(A)
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}
+
S_{\text{bulk}}(\Sigma_A).
\]

The vacuum entanglement of the boundary state determines the bulk geometry.

Changing the boundary state changes the bulk geometry.

Thus the vacuum is not merely a state on a fixed geometry. The vacuum helps constitute the geometry.

Vacuum Relativity therefore becomes geometric:

\[
\boxed{
\text{Different vacua correspond to different emergent spacetimes.}
}
\]

---

## 18. ER = EPR and Vacuum Connectivity

The ER=EPR conjecture relates entanglement to geometric connectivity.

A pair of entangled black holes in the thermofield double state,

\[
\ket{\text{TFD}}
=
Z^{-1/2}
\sum_n
e^{-\beta E_n/2}
\ket{n}_L
\ket{n}_R,
\]

is dual to two exterior regions connected by a nontraversable wormhole.

The state is entangled, but the geometry is connected.

Thus vacuum entanglement can be interpreted as geometric connectivity.

In Vacuum Relativity, the question “Are these regions connected?” may depend on the description:

- in the boundary description, the systems are entangled,
- in the bulk description, they are connected by a wormhole,
- in a code-subspace description, interior operators are reconstructible relative to certain observers.

Connectivity itself becomes vacuum-relative.

---

## 19. False Vacua and Cosmological Relativity

Vacuum Relativity also applies to false vacua.

A scalar field potential may have multiple minima:

\[
V(\phi_i)=\text{local minima}.
\]

A false vacuum is metastable. It can decay by bubble nucleation.

The decay rate is approximately

\[
\Gamma
\sim
A e^{-B/\hbar},
\]

where \(B\) is the Euclidean bounce action.

In a cosmological landscape, different regions may occupy different vacua.

Thus the observed vacuum may be environment-relative:

\[
P(\text{vacuum}\mid \text{observers})
\propto
\mu(\text{vacuum})
P(\text{observers}\mid \text{vacuum}).
\]

This connects Vacuum Relativity to Cosmological Ensemble Relativity.

The vacuum we observe may be conditional on our cosmic environment.

---

## 20. Vacuum Energy and the Cosmological Constant

The vacuum energy density contributes to the stress-energy tensor as

\[
T_{\mu\nu}^{(\text{vac})}
=
-
\rho_{\text{vac}} g_{\mu\nu}.
\]

This is equivalent to a cosmological constant:

\[
\Lambda
=
8\pi G\rho_{\text{vac}}.
\]

But vacuum energy is notoriously ambiguous in quantum field theory. It depends on regularization, renormalization, boundary conditions, and observer frame.

In curved spacetime, the expectation value

\[
\langle T_{\mu\nu}\rangle
\]

is state-dependent.

Different vacua yield different stress-energy tensors.

Thus even the gravitational effect of the vacuum is vacuum-relative.

---

## 21. Vacuum Relativity and Quantum Reference Frames

Quantum reference frames show that observers themselves are quantum systems.

If the observer is quantum, then the observer’s acceleration, horizon, and causal access may be indefinite or entangled.

A quantum observer may be in a superposition of accelerated and inertial trajectories.

Then the vacuum state relative to that observer may also be indefinite.

This suggests a further generalization:

\[
\boxed{
\text{The vacuum may be relative to quantum reference frames.}
}
\]

The Unruh effect may become a quantum-controlled effect: if the observer’s acceleration is in superposition, the perceived temperature may be entangled with the observer’s state.

---

## 22. Formal Framework of Vacuum Relativity

Let an observer \(O\) have access to a causal region \(W_O\).

Let \(\mathcal{A}(W_O)\) be the algebra of observables accessible to \(O\).

Let \(\omega\) be a global state.

The observer-relative vacuum is the restricted state

\[
\omega_O
=
\omega|_{\mathcal{A}(W_O)}.
\]

If the restriction is thermal, then

\[
\omega_O(A)
=
\frac{
\operatorname{Tr}
\left(
e^{-\beta H_O}A
\right)
}{
\operatorname{Tr}
e^{-\beta H_O}
},
\]

for \(A\in\mathcal{A}(W_O)\).

The modular Hamiltonian is

\[
K_O
=
-\ln\rho_O.
\]

Different observers \(O\) and \(O'\) have different algebras, Hamiltonians, and modular structures:

\[
K_O
\neq
K_{O'}.
\]

The invariant content is the full global state or, more generally, the equivalence class of observer-relative descriptions.

Thus:

\[
\boxed{
\text{Vacuum} = \text{state relative to an observer algebra}.
}
\]

---

## 23. Axioms of Vacuum Relativity

The framework may be organized around ten axioms.

### Axiom 1: The Vacuum Is Observer-Relative

The vacuum is defined relative to an observer’s time evolution and accessible algebra.

### Axiom 2: Particles Are Mode-Relative

Particles are excitations relative to a chosen mode decomposition.

### Axiom 3: Bogoliubov Transformations Relate Vacua

Different observers’ modes are related by Bogoliubov transformations.

### Axiom 4: Horizons Produce Thermality

Restricting a pure vacuum to a causally inaccessible region yields a mixed thermal state.

### Axiom 5: Acceleration Defines Temperature

Uniform acceleration through the vacuum produces the Unruh temperature.

### Axiom 6: Cosmological Horizons Define Vacua

De Sitter and expanding universes have horizon-relative or adiabatic vacua.

### Axiom 7: Black-Hole Vacua Are Plural

Boulware, Unruh, Hartle–Hawking, and infalling vacua correspond to different observer conditions.

### Axiom 8: Holographic Vacua Are Code-Subspace-Relative

Bulk vacua are effective states inside boundary code subspaces.

### Axiom 9: Vacuum Entanglement Is Invariant Structure

Observer-relative particle content arises from invariant vacuum entanglement.

### Axiom 10: Empty Space Is Relational

What one observer calls empty space, another may call thermal, squeezed, false, or encoded.

---

## 24. Observational and Experimental Relevance

The Unruh temperature is extremely small for achievable accelerations.

For acceleration \(a\),

\[
T_{\text{Unruh}}
\approx
4\times 10^{-21}
\left(
\frac{a}{1\,\text{m/s}^2}
\right)
\text{K}.
\]

Thus direct detection is difficult.

Nevertheless, related effects are experimentally relevant.

### 24.1 Analog Gravity

Analog systems in Bose–Einstein condensates, optical fibers, and fluid systems can simulate horizons and thermal radiation.

### 24.2 Accelerated Detectors

Proposals exist to detect Unruh radiation using highly accelerated electrons or circuit QED analogues.

### 24.3 Hawking Radiation Analogues

Analog black holes exhibit Hawking-like phonon radiation.

### 24.4 Entanglement Harvesting

Localized detectors can extract entanglement from the vacuum, demonstrating its nontrivial structure.

### 24.5 Black-Hole Astrophysics

Hawking radiation is too weak for astrophysical black holes, but black-hole thermodynamics is central to quantum gravity.

### 24.6 de Sitter Cosmology

The Gibbons–Hawking temperature is tiny but conceptually central to inflation and late-time acceleration.

Thus Vacuum Relativity is empirically indirect but theoretically indispensable.

---

## 25. Relation to Previous Versions of Relativity

Vacuum Relativity connects to earlier versions.

| Version | Relation to Vacuum Relativity |
|---|---|
| Special Relativity | Inertial frames define positive frequency |
| General Relativity | Horizons and acceleration define local vacua |
| Thermodynamic Relativity | Vacuum restriction is thermal |
| Holographic Relativity | Vacuum entanglement builds geometry |
| Code-Subspace Relativity | Bulk vacua are code-subspace states |
| Participatory Relativity | Measurement contexts define particle facts |
| Contextuality Relativity | Particle properties are context-relative |
| Topological Relativity | Vacuum sectors may be topological |
| Vacuum Relativity | The vacuum itself is observer-relative |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative particles}
\rightarrow
\text{relative vacuum}.
\]

---

## 26. Open Problems

Several major problems remain.

### 26.1 Interacting Fields

A complete treatment of Unruh and Hawking effects in strongly interacting quantum field theories remains difficult.

### 26.2 Quantum Gravity

The vacuum in full quantum gravity is not yet understood.

### 26.3 de Sitter Vacuum

The correct vacuum and Hilbert space for de Sitter space remain subtle.

### 26.4 Black-Hole Interior

How the infalling vacuum is encoded in exterior radiation remains an active problem.

### 26.5 Quantum Observers

Vacuum relativity for quantum superpositions of accelerated observers requires further development.

### 26.6 Vacuum Energy

The cosmological constant problem shows that vacuum energy is not yet understood.

### 26.7 Type III Algebras

Local algebras in QFT lack ordinary density matrices, requiring modular theory and regularization.

### 26.8 Experimental Access

Direct observation of Unruh radiation remains challenging.

---

## 27. What Einstein Would Think

Einstein would find Vacuum Relativity both beautiful and disturbing.

It would be beautiful because it extends the equivalence principle. A freely falling observer sees vacuum; an accelerated observer sees heat. This is precisely the kind of observer-dependence Einstein valued.

It would be disturbing because the vacuum is no longer a simple objective state of empty space. The distinction between empty and full becomes observer-relative.

But Einstein would recognize the central lesson:

\[
\boxed{
\text{Physical reality must be formulated in terms of invariant relations, not observer-dependent appearances.}
}
\]

The invariant is not “the vacuum.” It is the full relational structure connecting all observer-relative vacua.

---

## 28. Summary of Core Equations

### Bogoliubov transformation

\[
b_j
=
\sum_k
\left(
\alpha_{jk}^* a_k
-
\beta_{jk}^* a_k^\dagger
\right).
\]

### Particle production

\[
\langle 0_a|
b_j^\dagger b_j
|0_a\rangle
=
\sum_k
|\beta_{jk}|^2.
\]

### Rindler metric

\[
ds^2
=
-\xi^2 d\eta^2
+
d\xi^2.
\]

### Minkowski vacuum as squeezed state

\[
\ket{0_M}
=
\prod_k
\left(
1-e^{-2\pi\omega_k/a}
\right)^{1/2}
\sum_{n=0}^{\infty}
e^{-\pi n\omega_k/a}
\ket{n_k}_R
\ket{n_k}_L.
\]

### Reduced Rindler state

\[
\rho_R
=
\operatorname{Tr}_L
\ket{0_M}\bra{0_M}
=
\frac{e^{-\beta H_R}}{Z}.
\]

### Unruh temperature

\[
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
\]

### Bisognano–Wichmann modular state

\[
\rho_W
\propto
e^{-2\pi K}.
\]

### Gibbons–Hawking temperature

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

### Hawking temperature

\[
T_{\text{H}}
=
\frac{\hbar c^3}{8\pi G M k_{\text{B}}}.
\]

### KMS condition

\[
\langle A(t)B\rangle
=
\langle B A(t+i\beta)\rangle.
\]

### Ryu–Takayanagi formula

\[
S(A)
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}
+
S_{\text{bulk}}(\Sigma_A).
\]

### Central principle

\[
\boxed{
\text{The vacuum is not a universal state. It is an observer- and horizon-relative state.}
}
\]

---

## 29. Conclusion

Relativity 29.0, Vacuum Relativity, asserts that the vacuum is not absolute.

The Minkowski vacuum is empty for an inertial observer but thermal for an accelerated observer. The de Sitter vacuum is thermal for static observers. Black-hole vacua depend on whether one is static, infalling, past-oriented, or future-oriented. Holographic vacua depend on code subspaces and boundary reconstructions.

The basic object is not

\[
\ket{0},
\]

but

\[
\ket{0}_O,
\]

the vacuum relative to observer \(O\).

The central equations are the Bogoliubov transformation,

\[
a_k^{R}
=
\cosh r\, a_k^{M}
-
\sinh r\, a_{-k}^{M\dagger},
\]

and the Unruh temperature,

\[
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
\]

The central principle is:

\[
\boxed{
\text{The vacuum is not a universal state. It is an observer- and horizon-relative state.}
}
\]

Empty space is not empty. It is a relational quantum structure whose appearance depends on the observer’s motion, horizon, causal access, and code subspace.

What one observer calls vacuum, another may call heat.

What one observer calls nothing, another may call geometry.

This is Vacuum Relativity.

---

## Appendix A: Rindler Coordinates

In \(1+1\) dimensions, Minkowski coordinates \((t,x)\) are related to Rindler coordinates \((\eta,\xi)\) by

\[
ct
=
\xi\sinh\eta,
\]

\[
x
=
\xi\cosh\eta.
\]

Then

\[
ds^2
=
-c^2dt^2+dx^2
=
-\xi^2d\eta^2+d\xi^2.
\]

The right Rindler wedge is

\[
x>|ct|.
\]

The horizon is at \(\xi=0\).

The Rindler time \(\eta\) is generated by Lorentz boosts.

---

## Appendix B: Bogoliubov Particle Number

Given

\[
b_j
=
\sum_k
\left(
\alpha_{jk}^*a_k
-
\beta_{jk}^*a_k^\dagger
\right),
\]

and

\[
a_k\ket{0_a}=0,
\]

one finds

\[
b_j^\dagger b_j
=
\sum_{k,l}
\left(
\alpha_{jk}a_k^\dagger
-
\beta_{jk}a_k
\right)
\left(
\alpha_{jl}^*a_l
-
\beta_{jl}^*a_l^\dagger
\right).
\]

Taking the vacuum expectation value gives

\[
\langle 0_a|b_j^\dagger b_j|0_a\rangle
=
\sum_k
|\beta_{jk}|^2.
\]

Thus nonzero \(\beta\)-coefficients imply particle creation.

---

## Appendix C: Thermofield Double Form of the Minkowski Vacuum

For each Rindler mode frequency \(\omega\), define

\[
q
=
e^{-2\pi\omega/a}.
\]

Then

\[
\ket{0_M}
=
\prod_\omega
(1-q)^{1/2}
\sum_{n=0}^{\infty}
q^{n/2}
\ket{n_\omega}_R
\ket{n_\omega}_L.
\]

Tracing over the left wedge gives

\[
\rho_R
=
\prod_\omega
(1-q)
\sum_{n=0}^{\infty}
q^n
\ket{n_\omega}_R
\bra{n_\omega}_R.
\]

This is a thermal density matrix with

\[
\beta
=
\frac{2\pi}{a}.
\]

---

## Appendix D: Hawking Temperature from Surface Gravity

For a static black hole, the surface gravity is defined by

\[
\kappa^2
=
-
\frac{1}{2}
(\nabla^\mu\xi^\nu)
(\nabla_\mu\xi_\nu)
\]

evaluated on the horizon, where \(\xi^\mu\) is the horizon-generating Killing vector.

The Hawking temperature is

\[
T_{\text{H}}
=
\frac{\hbar\kappa}{2\pi k_{\text{B}}c}.
\]

For Schwarzschild,

\[
\kappa
=
\frac{c^4}{4GM},
\]

so

\[
T_{\text{H}}
=
\frac{\hbar c^3}{8\pi G M k_{\text{B}}}.
\]

---

## Appendix E: Modular Hamiltonian for the Rindler Wedge

Let \(\mathcal{A}(W)\) be the algebra of the right Rindler wedge.

The Minkowski vacuum restricted to \(\mathcal{A}(W)\) satisfies

\[
\rho_W
=
Z^{-1}e^{-2\pi K},
\]

where \(K\) is the boost generator.

The modular Hamiltonian is

\[
K_W
=
-\ln\rho_W
=
2\pi K
+
\ln Z.
\]

Thus the vacuum restricted to a wedge is thermal with respect to boost time.

---

## Selected References

1. W. G. Unruh, “Notes on Black-Hole Evaporation,” *Physical Review D* **14**, 870 (1976).  
2. S. W. Hawking, “Particle Creation by Black Holes,” *Communications in Mathematical Physics* **43**, 199 (1975).  
3. G. W. Gibbons and S. W. Hawking, “Cosmological Event Horizons, Thermodynamics, and Particle Creation,” *Physical Review D* **15**, 2738 (1977).  
4. J. J. Bisognano and E. H. Wichmann, “On the Duality Condition for a Hermitian Scalar Field,” *Journal of Mathematical Physics* **16**, 985 (1975).  
5. S. A. Fulling, “Nonuniqueness of Canonical Field Quantization in Riemannian Space-Time,” *Physical Review D* **7**, 2850 (1973).  
6. P. C. W. Davies, “Scalar Particle Production in Schwarzschild and Rindler Metrics,” *Journal of Physics A* **8**, 609 (1975).  
7. N. D. Birrell and P. C. W. Davies, *Quantum Fields in Curved Space* (Cambridge University Press, 1982).  
8. R. M. Wald, *Quantum Field Theory in Curved Spacetime and Black Hole Thermodynamics* (University of Chicago Press, 1994).  
9. H. Reeh and S. Schlieder, “Bemerkungen zur Unitäräquivalenz von Lorentz-invarianten Feldern,” *Nuovo Cimento* **22**, 1051 (1961).  
10. R. Haag, *Local Quantum Physics* (Springer, 1996).  
11. B. S. DeWitt, “Quantum Gravity: The New Synthesis,” in *General Relativity: An Einstein Centenary Survey* (Cambridge University Press, 1979).  
12. S. Ryu and T. Takayanagi, “Holographic Derivation of Entanglement Entropy from AdS/CFT,” *Physical Review Letters* **96**, 181602 (2006).  
13. M. Van Raamsdonk, “Building Up Spacetime with Quantum Entanglement,” *General Relativity and Gravitation* **42**, 2323 (2010).  
14. A. Almheiri, X. Dong, and D. Harlow, “Bulk Locality and Quantum Error Correction in AdS/CFT,” *Journal of High Energy Physics* **1504**, 163 (2015).  
15. D. Harlow, “The Ryu-Takayanagi Formula from Quantum Error Correction,” *Communications in Mathematical Physics* **354**, 865 (2017).  
16. J. Maldacena and L. Susskind, “Cool Horizons for Entangled Black Holes,” *Fortschritte der Physik* **61**, 781 (2013).  
17. S. R. Coleman, “Fate of the False Vacuum: Semiclassical Theory,” *Physical Review D* **15**, 2929 (1977).  
18. S. R. Coleman and F. De Luccia, “Gravitational Effects on and of Vacuum Decay,” *Physical Review D* **21**, 3305 (1980).  
19. T. S. Bunch and P. C. W. Davies, “Quantum Field Theory in de Sitter Space: Renormalization by Point-Splitting,” *Proceedings of the Royal Society A* **360**, 117 (1978).  
20. W. Rindler, “Kruskal Space and the Uniformly Accelerated Frame,” *American Journal of Physics* **34**, 1174 (1966).  
21. L. C. B. Crispino, A. Higuchi, and G. E. A. Matsas, “The Unruh Effect and Its Applications,” *Reviews of Modern Physics* **80**, 787 (2008).  
22. E. Witten, “Notes on Some Entanglement Properties of Quantum Field Theory,” *Reviews of Modern Physics* **90**, 045003 (2018).  
23. P. Gao, D. L. Jafferis, and A. C. Wall, “Traversable Wormholes via a Double Trace Deformation,” *Journal of High Energy Physics* **1712**, 151 (2017).  
24. R. M. Wald, *General Relativity* (University of Chicago Press, 1984).  
25. V. P. Frolov and I. D. Novikov, *Black Hole Physics: Basic Concepts and New Developments* (Kluwer, 1998).

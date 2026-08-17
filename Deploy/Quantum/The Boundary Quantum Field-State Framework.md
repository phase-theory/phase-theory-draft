# The Boundary Quantum Field-State Framework

## A Post-Schrödinger Implementation Specification for Quantum Dynamics, Measurement, and Emergent Classicality

**White Paper — Draft 1.0**

---

## Abstract

The Schrödinger wave function is one of the most successful mathematical structures in physics, but it is not a complete implementation of quantum reality. It is a nonrelativistic, fixed-particle-number, single-time-slice approximation. It does not natively handle particle creation and annihilation, relativistic causality, gauge constraints, quantum fields, detectors, decoherence, open systems, or dynamical spacetime.

This white paper proposes a more complete implementation architecture: the **Boundary Quantum Field-State Framework**, or **BQFS**.

BQFS replaces the elementary object

\[
\psi(\mathbf x,t)
\]

with a more general structure:

\[
\Psi[\Phi;\Sigma]
\]

or, more operationally,

\[
Z_M[b],
\]

where:

- \(\Phi\) denotes all physical fields,
- \(\Sigma\) is a spatial hypersurface or boundary,
- \(M\) is a spacetime region,
- \(b\) is field data on \(\partial M\),
- \(Z_M[b]\) is the quantum amplitude associated with that boundary data.

The framework combines:

1. quantum field theory,
2. path-integral boundary amplitudes,
3. algebraic locality,
4. density-operator states,
5. quantum instruments for measurement,
6. decoherence and consistent histories,
7. gauge-constraint handling,
8. an extensible gravity module,
9. computational regularization schemes.

BQFS does not claim to be a final experimentally verified theory of quantum gravity. Rather, it specifies the architecture that a complete implementation must have if it is to supersede the Schrödinger wave function while recovering all of its known successes.

---

# 1. Executive Summary

The Schrödinger equation,

\[
i\hbar \frac{\partial \psi}{\partial t}
=
\hat H \psi,
\]

was an extraordinary breakthrough. It correctly describes a vast domain of atomic, molecular, and condensed-matter physics in the nonrelativistic limit. However, if the intended task is a universal implementation of quantum physics, the Schrödinger wave function is incomplete.

The incompleteness is not a moral failure of Schrödinger’s theory. It is a scope limitation.

A complete implementation must support:

- relativity,
- variable particle number,
- spin,
- gauge symmetry,
- field locality,
- particle creation and annihilation,
- entanglement across arbitrary subsystems,
- open-system dynamics,
- measurement records,
- decoherence,
- classical emergence,
- and, at least as a module, dynamical spacetime.

The Boundary Quantum Field-State Framework proposes that the correct fundamental object is not a particle wave function but a **state functional over field configurations on boundaries**, together with rules for composing spacetime regions and extracting observational probabilities.

The core formal object is:

\[
\boxed{
Z_M[b]
=
\int_{\Phi|_{\partial M}=b}
\mathcal D\Phi\,
e^{iS_M[\Phi]/\hbar}
}
\]

with measurement probabilities given by quantum instruments:

\[
\boxed{
p(r)
=
\operatorname{Tr}[\mathcal I_r(\rho)]
}
\]

and state update given by conditionalization:

\[
\boxed{
\rho_r
=
\frac{\mathcal I_r(\rho)}{p(r)}.
}
\]

In this architecture, the Schrödinger wave function becomes a derived low-energy representation, not the foundational substrate.

---

# 2. Problem Statement

## 2.1 The original Schrödinger implementation

The ordinary Schrödinger wave function assigns a complex amplitude to a configuration of particles:

\[
\psi(\mathbf x_1,\dots,\mathbf x_N,t).
\]

For a single particle:

\[
\psi(\mathbf x,t).
\]

Its evolution is governed by:

\[
i\hbar \frac{\partial \psi}{\partial t}
=
\left(
-\frac{\hbar^2}{2m}\nabla^2
+
V
\right)\psi.
\]

This implementation is extremely effective when:

- velocities are small compared with \(c\),
- particle number is fixed,
- relativistic pair creation is negligible,
- spin can be added externally or ignored,
- measurement can be treated as an external postulate,
- spacetime is fixed and classical.

But these assumptions fail in high-energy physics, cosmology, quantum optics, particle physics, quantum information, and quantum gravity.

---

## 2.2 Failure modes of the Schrödinger wave function

The Schrödinger implementation is incomplete in at least ten major respects.

### 1. Fixed particle number

The Schrödinger wave function assumes a fixed number of particles. It cannot naturally describe:

\[
e^- + e^+ \to \gamma + \gamma,
\]

or photon emission and absorption, or vacuum fluctuations.

### 2. Preferred global time

Schrödinger evolution uses a universal time parameter \(t\). Relativity has no preferred global simultaneity.

### 3. Insufficient treatment of spin

Spin can be inserted by hand through the Pauli equation, but the fully relativistic treatment requires spinor fields and the Dirac equation.

### 4. No intrinsic field locality

The wave function over particle coordinates does not make locality manifest. Fundamental physics is better expressed through local fields and local algebras of observables.

### 5. Gauge symmetry is not automatic

Electromagnetism, the weak interaction, and the strong interaction are gauge theories. A complete implementation must impose gauge constraints or integrate over gauge orbits.

### 6. Measurement is external

Textbook quantum mechanics imposes a special measurement postulate:

\[
\psi \to \frac{P_r \psi}{\sqrt{p_r}}.
\]

A complete implementation should describe measurement as a physical interaction, not as an exceptional rule.

### 7. Decoherence is not intrinsic

The Schrödinger equation alone does not explain why macroscopic records become stable and effectively classical.

### 8. Open systems are not fundamental

Most real systems interact with environments. The pure-state Schrödinger equation is insufficient for dissipative, thermal, noisy, or measurement-like processes.

### 9. No particle creation or annihilation

Relativistic physics requires variable particle number. Quantum field theory solves this by promoting fields to operators acting on Fock space.

### 10. No gravity

The Schrödinger equation assumes a fixed background time and space. A complete implementation must at least provide an interface to dynamical spacetime.

---

## 2.3 Requirements for a complete implementation

A complete post-Schrödinger implementation should satisfy the following requirements.

| ID | Requirement |
|---|---|
| R1 | Recover nonrelativistic quantum mechanics in the appropriate limit |
| R2 | Support relativistic covariance |
| R3 | Respect locality and microcausality |
| R4 | Support variable particle number |
| R5 | Include spin and statistics |
| R6 | Implement gauge symmetry correctly |
| R7 | Represent mixed states and open systems |
| R8 | Describe measurement without primitive collapse |
| R9 | Explain classical records through decoherence |
| R10 | Provide an extensible module for gravity |

BQFS is designed to satisfy these requirements.

---

# 3. Design Principles

The BQFS architecture is built on the following principles.

## 3.1 Fields before particles

Particles are not primary. They are excitations or quanta of fields.

Therefore the basic state must be a functional of fields, not merely of particle coordinates.

---

## 3.2 Boundaries before global time

Instead of assuming a global time coordinate, the framework assigns amplitudes to spacetime regions and their boundaries.

This makes the implementation compatible with relativity and with arbitrary foliations of spacetime.

---

## 3.3 Compositionality

If a spacetime region is built by gluing smaller regions, the amplitude for the whole must be obtained by composing the amplitudes of the parts.

This is the quantum analogue of modular software design.

---

## 3.4 Operational measurement

Measurements are represented by quantum instruments, not by magical collapse.

An instrument maps an input density operator to an outcome-conditioned output density operator.

---

## 3.5 Emergent classicality

Classical reality is not assumed. It emerges through:

- coarse graining,
- decoherence,
- stable pointer states,
- redundant records,
- and thermodynamic irreversibility.

---

## 3.6 Effective reduction

The framework must reproduce known physics as limiting cases:

- Schrödinger mechanics,
- Pauli theory,
- Dirac theory,
- quantum electrodynamics,
- the Standard Model,
- quantum statistical mechanics,
- semiclassical gravity.

---

# 4. Ontology and Primitive Objects

The BQFS framework uses the following primitive entities.

---

## 4.1 Spacetime region

Let \(M\) be a spacetime region. It may be bounded by one or more hypersurfaces.

Its boundary is:

\[
\partial M.
\]

The boundary may be decomposed as:

\[
\partial M = \Sigma_i \cup \Sigma_f \cup B_{\text{side}},
\]

where:

- \(\Sigma_i\) is an initial hypersurface,
- \(\Sigma_f\) is a final hypersurface,
- \(B_{\text{side}}\) contains side boundaries or asymptotic conditions.

---

## 4.2 Field bundle

Let \(\mathcal F\) be the bundle of physical fields over spacetime.

A field configuration is:

\[
\Phi \in \Gamma(\mathcal F).
\]

Depending on the theory, \(\Phi\) may include:

- scalar fields \(\phi\),
- spinor fields \(\psi\),
- gauge fields \(A_\mu^a\),
- metric fields \(g_{\mu\nu}\),
- ghost fields,
- auxiliary fields.

---

## 4.3 Boundary data

Let \(b\) denote the restriction of the fields to the boundary:

\[
b = \Phi|_{\partial M}.
\]

The boundary data specify what is prepared, what is detected, or what is held fixed at the boundary of the region.

---

## 4.4 Boundary Hilbert space

To each boundary \(\Sigma\), the framework assigns a Hilbert space:

\[
\mathcal H_\Sigma.
\]

In a field-representation picture, a pure state may be written as:

\[
\Psi_\Sigma[b].
\]

More generally, a state is a density operator:

\[
\rho_\Sigma \in \mathcal D(\mathcal H_\Sigma).
\]

---

## 4.5 Local observable algebra

For each spacetime region \(\mathcal O\), assign an algebra of observables:

\[
\mathcal A(\mathcal O).
\]

A state assigns expectation values:

\[
\omega(A) = \langle A \rangle.
\]

This algebraic formulation avoids overcommitting to a particular representation and is well suited to relativistic quantum field theory.

---

# 5. Core Mathematical Specification

## 5.1 Action functional

Let the dynamics be specified by an action:

\[
S[\Phi]
=
\int_M d^4x\,
\mathcal L(\Phi,\partial \Phi).
\]

For the Standard Model:

\[
S = S_{\text{SM}}.
\]

For effective gravity plus matter:

\[
S = S_{\text{EH}} + S_{\text{matter}}.
\]

where:

\[
S_{\text{EH}}
=
\frac{1}{16\pi G}
\int d^4x\,
\sqrt{-g}\,R.
\]

---

## 5.2 Boundary amplitude functional

The fundamental amplitude associated with region \(M\) and boundary data \(b\) is:

\[
\boxed{
Z_M[b]
=
\int_{\Phi|_{\partial M}=b}
\mathcal D\Phi\,
e^{iS_M[\Phi]/\hbar}
}
\]

This is the central object of BQFS.

If the boundary is split into initial and final parts, the amplitude becomes a kernel:

\[
K(b_f,b_i)
=
\int_{b_i}^{b_f}
\mathcal D\Phi\,
e^{iS[\Phi]/\hbar}.
\]

Given an initial boundary state \(\Psi_i[b_i]\), the final state is:

\[
\boxed{
\Psi_f[b_f]
=
\int \mathcal D b_i\,
K(b_f,b_i)\Psi_i[b_i].
}
\]

---

## 5.3 Composition rule

If a region \(M\) is formed by gluing two regions \(M_1\) and \(M_2\) along an internal boundary \(\Sigma_{\text{int}}\), then the total amplitude is obtained by integrating over the shared boundary data:

\[
\boxed{
Z_M[b_{\text{ext}}]
=
\int \mathcal D b_{\text{int}}\,
Z_{M_1}[b_{\text{int}},b_1]
Z_{M_2}[b_2,b_{\text{int}}].
}
\]

This rule makes the theory compositional.

In operator language:

\[
Z_{M_2 \circ M_1}
=
Z_{M_2} \circ Z_{M_1}.
\]

This is the replacement for global time-slicing.

---

## 5.4 Hypersurface evolution: Tomonaga-Schwinger form

Instead of evolution in a global time \(t\), BQFS can use local deformations of a spacelike hypersurface \(\Sigma\).

Let \(|\Psi_\Sigma\rangle\) be the state associated with \(\Sigma\). An infinitesimal deformation of \(\Sigma\) at point \(x\) satisfies schematically:

\[
\boxed{
i\hbar
\frac{\delta}{\delta \Sigma(x)}
|\Psi_\Sigma\rangle
=
\hat{\mathcal H}(x)
|\Psi_\Sigma\rangle.
}
\]

Here \(\hat{\mathcal H}(x)\) is a Hamiltonian density or interaction density.

A more covariant expression uses the stress-energy tensor:

\[
i\hbar\,\delta_\xi |\Psi_\Sigma\rangle
=
\int_\Sigma d\Sigma_\mu\,
T^{\mu\nu}\xi_\nu
|\Psi_\Sigma\rangle,
\]

where \(\xi^\mu\) is the infinitesimal deformation vector.

This generalizes Schrödinger evolution to arbitrary spacelike hypersurfaces.

---

## 5.5 Field Schrödinger functional

In a fixed foliation, one may write a wave functional:

\[
\Psi[\phi,t].
\]

For a real scalar field with potential \(V(\phi)\), the Schrödinger functional equation is:

\[
\boxed{
i\hbar \frac{\partial}{\partial t}\Psi[\phi,t]
=
\int d^3x
\left[
-\frac{\hbar^2}{2}
\frac{\delta^2}{\delta \phi(\mathbf x)^2}
+
\frac{1}{2}(\nabla\phi)^2
+
V(\phi)
\right]
\Psi[\phi,t].
}
\]

This is the direct field-theoretic generalization of the Schrödinger equation.

For multiple fields:

\[
\Psi[\phi_1,\phi_2,\psi,A_\mu,\dots;t].
\]

---

## 5.6 Density functional representation

Because realistic systems are open and entangled, the more general object is a density functional:

\[
\rho[\phi,\phi';t]
=
\langle \phi|\rho(t)|\phi'\rangle.
\]

For closed systems:

\[
i\hbar \frac{\partial \rho}{\partial t}
=
[H,\rho].
\]

For open systems:

\[
\boxed{
\frac{d\rho}{dt}
=
-\frac{i}{\hbar}[H,\rho]
+
\sum_k
\left(
L_k\rho L_k^\dagger
-
\frac{1}{2}
\{L_k^\dagger L_k,\rho\}
\right).
}
\]

This is the Lindblad form.

---

# 6. Spin, Fermions, and Gauge Fields

## 6.1 Fermions

Fermionic fields require anticommutation relations:

\[
\{\hat\psi_a(\mathbf x),\hat\psi_b^\dagger(\mathbf y)\}
=
\delta_{ab}\delta^3(\mathbf x-\mathbf y).
\]

In path-integral form, fermions are represented using Grassmann variables:

\[
\psi,\bar\psi.
\]

The fermionic path integral is:

\[
\int \mathcal D\bar\psi\,\mathcal D\psi\,
e^{iS[\bar\psi,\psi]/\hbar}.
\]

The corresponding wave functional may be Grassmann-valued.

---

## 6.2 Gauge fields

Gauge fields require redundancy removal. Physical states must satisfy constraints such as Gauss’s law:

\[
\boxed{
\hat G^a(\mathbf x)
|\Psi_{\text{phys}}\rangle
=
0.
}
\]

Equivalently, the path integral is gauge-fixed:

\[
Z
=
\int \mathcal D A\,
\Delta_{\text{FP}}[A]\,
\delta(G[A])\,
e^{iS[A]/\hbar},
\]

where \(\Delta_{\text{FP}}\) is the Faddeev-Popov determinant.

In BRST language, physical states are cohomology classes of the BRST operator \(Q\):

\[
Q|\Psi_{\text{phys}}\rangle = 0.
\]

---

## 6.3 Standard Model module

For known non-gravitational physics, the action is the Standard Model action:

\[
S_{\text{SM}}
=
\int d^4x\,
\mathcal L_{\text{SM}}.
\]

The fields include:

- quark fields,
- lepton fields,
- gluon fields,
- electroweak gauge fields,
- Higgs field,
- ghost and gauge-fixing terms.

The boundary amplitude becomes:

\[
Z_M[b]
=
\int_{\text{SM fields}|_{\partial M}=b}
\mathcal D(\text{SM fields})\,
e^{iS_{\text{SM}}/\hbar}.
\]

This provides the known-physics completion of the Schrödinger implementation.

---

# 7. Measurement and Records

## 7.1 The measurement problem as an implementation gap

Textbook quantum mechanics has two incompatible-looking rules:

1. smooth unitary evolution,
2. discontinuous collapse during measurement.

A complete implementation should remove this discontinuity by treating measurement as an ordinary physical interaction whose outcomes are stable records.

BQFS does this operationally using quantum instruments.

---

## 7.2 Quantum instruments

A measurement device is represented by a set of completely positive, trace-nonincreasing maps:

\[
\{\mathcal I_r\},
\]

where \(r\) labels possible records.

The probability of record \(r\) is:

\[
\boxed{
p(r)
=
\operatorname{Tr}[\mathcal I_r(\rho)].
}
\]

The normalized post-measurement state is:

\[
\boxed{
\rho_r
=
\frac{\mathcal I_r(\rho)}{p(r)}.
}
\]

The total instrument is trace-preserving:

\[
\sum_r \operatorname{Tr}[\mathcal I_r(\rho)]
=
\operatorname{Tr}[\rho].
\]

---

## 7.3 POVM special case

A simpler measurement model uses measurement operators \(M_r\), with effects:

\[
E_r = M_r^\dagger M_r.
\]

Then:

\[
p(r)
=
\operatorname{Tr}(E_r\rho),
\]

and:

\[
\rho_r
=
\frac{M_r\rho M_r^\dagger}{p(r)}.
\]

The completeness condition is:

\[
\sum_r E_r = I.
\]

---

## 7.4 Decoherence and stable records

A measurement record becomes classical when it is robust against environmental monitoring.

Let \(S\) be the system, \(A\) the apparatus, and \(E\) the environment.

The total state evolves unitarily:

\[
|\Psi_{SAE}\rangle
=
U|\Psi_{SAE,0}\rangle.
\]

The reduced state of system plus apparatus is:

\[
\rho_{SA}
=
\operatorname{Tr}_E
|\Psi_{SAE}\rangle
\langle\Psi_{SAE}|.
\]

Decoherence occurs when off-diagonal terms in the apparatus pointer basis are suppressed:

\[
\rho_{SA}
\approx
\sum_r p_r |r\rangle\langle r|.
\]

The record \(r\) is then effectively classical.

---

## 7.5 Consistent histories

For sequences of events, define class operators:

\[
C_\alpha
=
P_{\alpha_n}(t_n)\cdots P_{\alpha_1}(t_1).
\]

The decoherence functional is:

\[
D(\alpha,\beta)
=
\operatorname{Tr}
\left(
C_\alpha \rho C_\beta^\dagger
\right).
\]

If off-diagonal terms are negligible,

\[
D(\alpha,\beta)\approx 0
\quad
\text{for }
\alpha\neq\beta,
\]

then probabilities may be assigned:

\[
p(\alpha)
=
D(\alpha,\alpha).
\]

This provides a history-based account of classical narratives emerging from quantum processes.

---

# 8. Open Systems and Thermodynamics

## 8.1 Reduced states

For a total Hilbert space:

\[
\mathcal H = \mathcal H_S \otimes \mathcal H_E,
\]

the system state is:

\[
\rho_S
=
\operatorname{Tr}_E \rho_{SE}.
\]

This is essential because no realistic system is perfectly isolated.

---

## 8.2 Influence functional

If the environment is integrated out, the system’s effective dynamics can be represented by an influence functional:

\[
F[\phi^+,\phi^-]
=
\operatorname{Tr}_E
\left[
U_E[\phi^+]
\rho_E
U_E^\dagger[\phi^-]
\right].
\]

The reduced density matrix evolves as:

\[
\rho_S[\phi_f^+,\phi_f^-]
=
\int
\mathcal D\phi_i^+
\mathcal D\phi_i^-\,
J[\phi_f^+,\phi_f^-;\phi_i^+,\phi_i^-]
\rho_S[\phi_i^+,\phi_i^-],
\]

where \(J\) includes the influence functional.

---

## 8.3 Entropy and irreversibility

The von Neumann entropy is:

\[
S(\rho)
=
-\operatorname{Tr}(\rho\log\rho).
\]

For closed systems:

\[
S(\rho)
\]

is constant under unitary evolution.

For subsystems, entropy can increase because information leaks into inaccessible environmental degrees of freedom.

This gives the framework a natural route to thermodynamic behavior.

---

# 9. Gravity Module

## 9.1 Effective quantum field theory on curved spacetime

At energies below the Planck scale, gravity can be treated as an effective quantum field theory.

The action is:

\[
S
=
\int d^4x\sqrt{-g}
\left[
\frac{1}{16\pi G}R
+
c_1 R^2
+
c_2 R_{\mu\nu}R^{\mu\nu}
+
\cdots
\right]
+
S_{\text{matter}}.
\]

For semiclassical gravity, one may use:

\[
G_{\mu\nu}
=
8\pi G
\langle \hat T_{\mu\nu}\rangle.
\]

This is not final, but it is useful as an effective module.

---

## 9.2 Quantum geometry placeholder

A more complete gravitational implementation would sum over geometries:

\[
\boxed{
Z[b]
=
\int
\mathcal Dg\,
\mathcal D\Phi\,
e^{i(S_{\text{grav}}[g]+S_{\text{matter}}[g,\Phi])/\hbar}.
}
\]

In canonical language, the state becomes:

\[
\Psi[g_{ij},\Phi;\Sigma],
\]

and must satisfy constraints:

\[
\hat H_\perp(\mathbf x)\Psi = 0,
\]

\[
\hat H_i(\mathbf x)\Psi = 0.
\]

These are the Hamiltonian and diffeomorphism constraints.

BQFS does not pretend that the final quantum gravity implementation is known. Instead, it defines the interface that such a theory must satisfy.

---

# 10. Computational Implementation

A complete theory must be implementable computationally, at least approximately.

## 10.1 Regularization

The path integral is formal. A runnable implementation requires regularization.

Common choices:

- lattice regularization,
- momentum cutoff,
- dimensional regularization,
- spectral truncation,
- tensor-network discretization,
- causal-set or spin-foam discretization for quantum gravity research.

For numerical simulation, a spatial lattice \(\Lambda\) is often appropriate.

---

## 10.2 Lattice field-state representation

On a lattice:

- bosonic fields live on sites or links,
- gauge fields live on links as group elements \(U_\ell \in G\),
- fermions live on sites or staggered degrees of freedom,
- constraints are imposed locally.

The Hilbert space becomes:

\[
\mathcal H_\Lambda
=
\bigotimes_{x\in\Lambda}
\mathcal H_x.
\]

Physical states satisfy:

\[
\hat G_x |\Psi_{\text{phys}}\rangle = 0.
\]

---

## 10.3 Hamiltonian simulation

For lattice gauge theory, one may use a Hamiltonian:

\[
H = H_E + H_B + H_F,
\]

where:

- \(H_E\) is the electric-field energy,
- \(H_B\) is the magnetic plaquette energy,
- \(H_F\) is the fermion hopping and mass term.

Time evolution is:

\[
U(t)
=
e^{-iHt/\hbar}.
\]

For simulation, use Trotterization:

\[
e^{-iHt}
\approx
\left(
e^{-iH_1\Delta t}
e^{-iH_2\Delta t}
\cdots
\right)^N.
\]

---

## 10.4 Tensor networks and variational methods

For low-entanglement states, tensor networks provide efficient approximations:

- matrix product states,
- projected entangled-pair states,
- multiscale entanglement renormalization ansatz.

For high-energy scattering, other methods are needed:

- perturbation theory,
- Monte Carlo in Euclidean signature,
- variational quantum eigensolvers,
- quantum simulation.

---

## 10.5 Algorithmic specification

A minimal software architecture for BQFS would look like this:

```python
class BQFSImplementation:
    def __init__(self, field_spec, action, constraints):
        self.field_spec = field_spec
        self.action = action
        self.constraints = constraints

    def prepare_boundary_state(self, boundary_data):
        return BoundaryState(boundary_data)

    def region_amplitude(self, region, boundary_data):
        return path_integral(
            action=self.action,
            region=region,
            boundary=boundary_data,
            constraints=self.constraints
        )

    def propagate(self, state, region):
        K = self.region_amplitude(region, state.boundary)
        return K.apply(state)

    def glue(self, amplitude_A, amplitude_B):
        return integrate_shared_boundary(amplitude_A, amplitude_B)

    def impose_gauge_constraints(self, state):
        return project_physical_subspace(state, self.constraints)

    def measure(self, rho, instrument):
        probabilities = []
        for r in instrument.outcomes:
            probabilities.append(trace(instrument.map(r, rho)))

        r = sample(probabilities)
        rho_r = instrument.map(r, rho) / probabilities[r]

        return r, rho_r

    def effective_limit(self, state, regime):
        if regime == "nonrelativistic_one_particle":
            return schrodinger_limit(state)
        elif regime == "semiclassical_field":
            return classical_field_limit(state)
        elif regime == "thermal":
            return statistical_limit(state)
        else:
            raise NotImplementedError
```

This is not a small program. It is an architecture for a physics engine.

---

# 11. Recovery of Known Physics

A complete implementation must recover known successful theories.

## 11.1 Recovery of the Schrödinger equation

Consider a scalar field with mass \(m\). In the nonrelativistic one-particle sector, write:

\[
\Phi(\mathbf x,t)
\approx
\frac{1}{\sqrt{2m}}
e^{-imc^2t/\hbar}
\psi(\mathbf x,t).
\]

Substituting into the relativistic field equation and dropping high-frequency antiparticle contributions yields:

\[
\boxed{
i\hbar\frac{\partial \psi}{\partial t}
=
\left(
-\frac{\hbar^2}{2m}\nabla^2
+
V(\mathbf x)
\right)\psi.
}
\]

Thus Schrödinger mechanics is recovered as an effective module.

---

## 11.2 Recovery of Pauli theory

Including spin and coupling to electromagnetism yields the Pauli equation:

\[
i\hbar\frac{\partial \psi}{\partial t}
=
\left[
\frac{1}{2m}
(\boldsymbol\sigma\cdot(\mathbf p - q\mathbf A))^2
+
q\phi
\right]\psi.
\]

---

## 11.3 Recovery of Dirac theory

The relativistic electron is described by the Dirac field:

\[
(i\gamma^\mu D_\mu - m)\psi = 0.
\]

This emerges naturally from the fermionic field module.

---

## 11.4 Recovery of quantum electrodynamics

For electrons and photons:

\[
\mathcal L_{\text{QED}}
=
-\frac{1}{4}F_{\mu\nu}F^{\mu\nu}
+
\bar\psi(i\gamma^\mu D_\mu - m)\psi.
\]

Boundary amplitudes built from this action reproduce scattering amplitudes, radiative corrections, Lamb shifts, and anomalous magnetic moments.

---

## 11.5 Recovery of the Standard Model

Using the full Standard Model action, BQFS recovers:

- electroweak interactions,
- quantum chromodynamics,
- Higgs physics,
- scattering amplitudes,
- decay rates,
- bound-state effective theories.

---

# 12. Validation Plan

A complete implementation must be validated against known physics.

## 12.1 Nonrelativistic validation

The framework must reproduce:

- hydrogen spectrum,
- harmonic oscillator spectrum,
- tunneling rates,
- interference fringes,
- Berry phases,
- Aharonov-Bohm effect.

---

## 12.2 Relativistic validation

It must reproduce:

- Dirac spectrum,
- positron prediction,
- relativistic scattering,
- spin-statistics connection,
- Klein paradox resolution via field theory.

---

## 12.3 Quantum field validation

It must reproduce:

- electron anomalous magnetic moment,
- Lamb shift,
- Casimir effect,
- photon emission and absorption,
- particle decay rates,
- cross sections.

---

## 12.4 Quantum information validation

It must reproduce:

- Bell inequality violations,
- no-signaling constraints,
- quantum teleportation,
- entanglement entropy scaling,
- quantum error correction thresholds.

---

## 12.5 Decoherence validation

It must reproduce:

- pointer-state selection,
- environment-induced suppression of interference,
- quantum-to-classical transition in measurement models,
- thermalization in closed many-body systems.

---

# 13. Interpretation Neutrality

BQFS is designed to be interpretation-neutral.

It can be read in several ways:

- as an Everettian universal wave functional with branching records,
- as an operationalinstrumentalist framework for predicting observations,
- as a sum-over-histories formulation,
- as an algebraic quantum field theory with states on local algebras.

The framework does not require a unique metaphysical interpretation in order to function as an implementation.

The core operational commitments are:

1. states assign amplitudes or probabilities,
2. dynamics is given by boundary composition,
3. measurements are physical instruments,
4. records are decohered macroscopic variables.

---

# 14. Limitations and Open Problems

BQFS is an architecture, not a magical final theory. Several deep problems remain.

---

## 14.1 Rigorous path integrals

The formal expression

\[
\int \mathcal D\Phi\,e^{iS[\Phi]/\hbar}
\]

is not always mathematically rigorous, especially in Lorentzian signature.

Workarounds include:

- Wick rotation,
- lattice regularization,
- constructive field theory,
- Osterwalder-Schrader reconstruction,
- perturbative renormalization.

But a fully rigorous nonperturbative formulation for all physically relevant theories remains an open problem.

---

## 14.2 Quantum gravity

The gravity module is incomplete. Candidate approaches include:

- effective field theory,
- asymptotic safety,
- loop quantum gravity,
- spin foams,
- causal dynamical triangulations,
- string theory,
- group field theory.

BQFS provides an interface but does not yet provide the final quantum gravity backend.

---

## 14.3 Measurement ontology

The framework removes the practical need for a primitive collapse postulate by using instruments and decoherence. However, the ontological status of outcomes remains interpretation-dependent.

---

## 14.4 Computational complexity

Exact simulation of generic quantum field states is exponentially hard. Practical implementations require approximations:

- perturbation theory,
- lattice Monte Carlo,
- tensor networks,
- variational methods,
- quantum simulation.

---

## 14.5 Cosmology and initial conditions

A complete implementation must eventually address:

- cosmological boundary conditions,
- inflationary fluctuations,
- vacuum selection,
- arrow of time,
- horizon entropy.

BQFS can accommodate these as boundary-condition problems, but it does not solve them by itself.

---

# 15. Roadmap

## Phase 1: Formal specification

Define the minimal mathematical kernel:

- spacetime regions,
- boundary data,
- field action,
- amplitude functional,
- composition rule,
- measurement instruments.

Deliverable: a formal specification document.

---

## Phase 2: Nonrelativistic reduction

Show explicitly that the framework reduces to:

- Schrödinger mechanics,
- Pauli theory,
- many-body quantum mechanics.

Deliverable: reduction proofs and numerical examples.

---

## Phase 3: Field-theoretic implementation

Implement simple field theories:

- scalar \(\phi^4\) theory,
- lattice gauge theory,
- Yukawa theory,
- quantum electrodynamics in truncated spaces.

Deliverable: simulation engine prototypes.

---

## Phase 4: Measurement and decoherence module

Implement detector models:

- spin measurement,
- photon detection,
- environment-induced decoherence,
- quantum instruments.

Deliverable: measurement simulation library.

---

## Phase 5: Effective gravity interface

Add modules for:

- quantum fields on curved spacetime,
- semiclassical Einstein equation,
- perturbative quantum gravity corrections.

Deliverable: effective gravity interface.

---

## Phase 6: Candidate quantum gravity integration

Evaluate possible backends:

- spin foams,
- lattice quantum gravity,
- asymptotic safety,
- holographic duals,
- string-inspired amplitudes.

Deliverable: plug-in architecture for quantum gravity candidates.

---

# 16. Why BQFS Is More Complete Than Schrödinger’s Implementation

The Schrödinger wave function is a special case of BQFS.

The relationship is:

\[
\boxed{
\psi(\mathbf x,t)
\quad
\text{is an effective one-particle projection of}
\quad
\Psi[\Phi;\Sigma].
}
\]

BQFS adds the missing layers:

| Feature | Schrödinger implementation | BQFS implementation |
|---|---:|---:|
| Nonrelativistic quantum mechanics | Yes | Yes, as limit |
| Relativistic covariance | No | Yes |
| Variable particle number | No | Yes |
| Quantum fields | No | Yes |
| Spin | Partial | Yes |
| Gauge theories | Incomplete | Yes |
| Measurement | External collapse | Quantum instruments |
| Decoherence | Not intrinsic | Intrinsic |
| Open systems | Limited | Density operators/Lindblad |
| Classical emergence | Not explained | Decoherence/histories |
| Gravity | Absent | Extensible module |

---

# 17. Conclusion

The Schrödinger wave function is not wrong. It is incomplete if taken as the final implementation of quantum physics.

A complete implementation must be based on:

\[
\boxed{
\text{field states}
+
\text{boundary amplitudes}
+
\text{local observables}
+
\text{quantum instruments}
+
\text{decoherence}
+
\text{effective reduction}.
}
\]

The Boundary Quantum Field-State Framework proposes exactly this architecture.

Its core equation is:

\[
\boxed{
Z_M[b]
=
\int_{\Phi|_{\partial M}=b}
\mathcal D\Phi\,
e^{iS_M[\Phi]/\hbar}.
}
\]

Its operational rule is:

\[
\boxed{
p(r)
=
\operatorname{Tr}[\mathcal I_r(\rho)].
}
\]

Its composition rule is:

\[
\boxed{
Z_{M_1\cup M_2}
=
\int_{\text{shared boundary}}
Z_{M_1}Z_{M_2}.
}
\]

Its recovery rule is:

\[
\boxed{
\text{Schrödinger mechanics}
=
\text{low-energy, fixed-particle-number limit of BQFS}.
}
\]

In this sense, BQFS does not discard Schrödinger’s achievement. It embeds it inside a larger and more complete implementation.

---

# Appendix A: Minimal Formal Kernel

A minimal BQFS kernel can be stated in five axioms.

## Axiom 1: Fields

There exists a set of fields \(\Phi\).

## Axiom 2: Action

There exists an action:

\[
S[\Phi].
\]

## Axiom 3: Boundary amplitude

For each region \(M\) and boundary data \(b\):

\[
Z_M[b]
=
\int_{\Phi|_{\partial M}=b}
\mathcal D\Phi\,
e^{iS_M[\Phi]/\hbar}.
\]

## Axiom 4: Composition

If \(M=M_1\cup M_2\), then:

\[
Z_M
=
\int Z_{M_1}Z_{M_2}
\]

over shared boundary data.

## Axiom 5: Measurement

For each detector record \(r\), there is a quantum instrument \(\mathcal I_r\), and:

\[
p(r)
=
\operatorname{Tr}[\mathcal I_r(\rho)].
\]

---

# Appendix B: Implementation Pseudocode

```python
class BoundaryQuantumFieldState:
    def __init__(self, boundary, data):
        self.boundary = boundary
        self.data = data

class Action:
    def evaluate(self, field_configuration):
        raise NotImplementedError

class Region:
    def __init__(self, geometry, action):
        self.geometry = geometry
        self.action = action

def path_integral(region, boundary_conditions):
    # Formal expression:
    # integral DPhi exp(i S[Phi] / hbar)
    # Actual implementation requires regularization.
    return compute_amplitude(region, boundary_conditions)

def compose_amplitudes(A1, A2, shared_boundary):
    return integrate_over(A1, A2, shared_boundary)

def quantum_instrument_measurement(rho, instrument):
    probabilities = []

    for r in instrument.outcomes:
        probabilities.append(trace(instrument.map(r, rho)))

    r = sample(probabilities)
    rho_r = instrument.map(r, rho) / probabilities[r]

    return r, rho_r

def schrodinger_limit(state):
    return project_to_nonrelativistic_one_particle_sector(state)
```

---

# Appendix C: Glossary

**Boundary amplitude**  
The quantum amplitude associated with field data on the boundary of a spacetime region.

**Boundary data**  
The values or constraints imposed on fields at the boundary of a spacetime region.

**Density operator**  
A positive, trace-one operator representing a possibly mixed quantum state.

**Decoherence**  
The suppression of interference between macroscopically distinct alternatives due to entanglement with an environment.

**Fock space**  
A Hilbert space allowing variable particle number.

**Gauge constraint**  
A condition removing unphysical gauge redundancy.

**Instrument**  
A completely positive map representation of a measurement process.

**Path integral**  
A sum over field histories weighted by \(e^{iS/\hbar}\).

**POVM**  
A positive operator-valued measure used to compute measurement probabilities.

**Tomonaga-Schwinger evolution**  
Hypersurface-local generalization of Schrödinger time evolution.

**Wave functional**  
A quantum amplitude functional over field configurations rather than particle positions.

---

# Final Statement

The complete implementation of quantum physics is not a single wave function. It is a composable boundary-amplitude architecture for quantum fields, measurement instruments, and emergent classical records.

The Schrödinger equation remains one of the most important effective modules inside that architecture, but it is not the operating system itself.

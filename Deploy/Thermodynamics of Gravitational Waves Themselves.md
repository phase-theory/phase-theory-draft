# Thermodynamics of Gravitational Waves Themselves: Isaacson Energy, Graviton Entropy, and the Equation of State of a GW Radiation Bath

## Abstract

We develop a thermodynamic framework for gravitational waves as a field in general relativity, emphasizing the distinction between energy transport, coarse-grained thermodynamic behavior, and intrinsic entropy. In the short-wavelength limit, gravitational waves admit an effective stress-energy tensor due to Isaacson, which supports a radiation-fluid description with equation of state \(p=\rho/3\) after averaging. Entropy is not a property of a classical waveform alone; for a pure coherent gravitational-wave state it is zero under the standard field-theoretic entropy assignment, while mixed, thermal, or decohered graviton ensembles carry nonzero entropy. We present a formal derivation of the energy, pressure, entropy, and equilibrium thermodynamics of a gravitational-wave bath in a closed spacetime volume, and we specify precisely the regime in which the derivation is valid.

## 1. Introduction

Black-hole thermodynamics is well established, but the thermodynamics of the gravitational-wave field itself remains only partially formalized. The difficulty is conceptual: general relativity defines the geometry that gravitational waves perturb, but a thermodynamic description requires a state space, coarse-graining, and a notion of entropy that are not intrinsic to classical field configurations. Still, gravitational waves do carry energy and momentum in the effective sense captured by the Isaacson tensor, so a consistent field-theoretic thermodynamics is within reach in the high-frequency approximation. The purpose of this paper is to make that structure explicit.

A key point is that the entropy of a gravitational wave is not determined by its amplitude alone. A monochromatic classical wave corresponds, in quantum language, to a coherent state, and coherent states have vacuum-like entanglement entropy under the usual bipartition arguments. By contrast, a thermal graviton gas or a decohered stochastic background is genuinely mixed and therefore thermodynamic in the standard sense. The result is a clean but subtle answer: gravitational waves have a thermodynamics, but not every gravitational wave has entropy.

## 2. Regime of Validity

We work in the Isaacson short-wavelength regime, where the GW wavelength is much smaller than the curvature radius of the background spacetime. The metric is decomposed as \(g_{\mu\nu}=\bar g_{\mu\nu}+h_{\mu\nu}\), with \(h_{\mu\nu}\) rapidly varying and \(\bar g_{\mu\nu}\) slowly varying. Averaging over several wavelengths produces a gauge-invariant effective stress-energy tensor for the wave field, and that averaged tensor is the starting point for any thermodynamic interpretation. Outside this regime, local gravitational-wave energy and entropy remain coordinate-dependent or state-dependent in ways that prevent a universal equation of state from being defined.

This paper therefore addresses the thermodynamics of a gravitational-wave gas, not arbitrary nonlinear spacetime dynamics. The distinction matters because the field-theoretic limit is precisely where statistical mechanics can be applied cleanly. The formalism below should be understood as a controlled effective theory.

## 3. Effective Energy of Gravitational Waves

In the high-frequency limit, the effective GW stress-energy is given by the Isaacson tensor,
\[
T^{\mathrm{GW}}_{\alpha\beta}
=
\frac{1}{32\pi G}
\left\langle
\bar\nabla_\alpha h^{\mathrm{TT}}_{\mu\nu}\,
\bar\nabla_\beta h_{\mathrm{TT}}^{\mu\nu}
\right\rangle,
\]
where the average is taken over scales large compared with the wavelength but small compared with the background curvature scale. This expression is the gravitational analogue of the stress-energy tensor for radiation, and it captures the fact that gravitational waves transport energy and momentum. In the transverse-traceless gauge and in nearly flat regions, the energy density scales quadratically in wave amplitude and time derivatives, as expected for a radiation field.

Define the coarse-grained energy density by
\[
\rho_{\mathrm{GW}} \equiv \langle T^{\mathrm{GW}}_{00}\rangle.
\]
Then for a closed volume \(V\), the total wave energy is
\[
U_{\mathrm{GW}} = \int_V \rho_{\mathrm{GW}}\, d^3x.
\]
This quantity is well-defined in the averaged regime and is the energy that appears in the thermodynamic treatment.

## 4. Pressure and Equation of State

For an isotropic bath of massless excitations, the pressure is one third of the energy density. The same result applies to the gravitational-wave gas in the averaged geometric-optics limit because the effective stress-energy is traceless and the excitations propagate null-like. Thus,
\[
p_{\mathrm{GW}} = \frac{1}{3}\rho_{\mathrm{GW}}.
\]
This is the gravitational-wave analogue of the photon-gas equation of state.

More generally, the pressure can be obtained from the spatial trace of the stress-energy tensor in the local rest frame:
\[
p_{\mathrm{GW}} = \frac{1}{3}\sum_{i=1}^3 \langle T^{\mathrm{GW}}_{ii} \rangle.
\]
Any departure from \(p=\rho/3\) requires anisotropy, strong curvature corrections, mode correlations, or nonlinear self-interaction beyond the simplest Isaacson limit. Therefore, the equation of state of a gravitational-wave gas is radiation-like to leading order, but not universally fixed beyond that approximation.

## 5. Quantum-State Description

To discuss entropy, we must move from classical fields to quantum states. In the linearized theory, the gravitational-wave field may be expanded in graviton creation and annihilation operators, and the state is represented by a density operator \(\rho\) over the corresponding Fock space. A classical waveform corresponds most naturally to a coherent state, while thermalized or stochastic backgrounds correspond to mixed states.

A coherent state is the gravitational analogue of a laser field: it has well-defined phase, nonzero energy, and minimal quantum uncertainty, but it is not thermodynamically disordered in the usual sense. This makes coherent gravitational radiation the correct state associated with deterministic astrophysical waveforms in the leading approximation. Entropy enters only after coarse-graining, environmental tracing, detector averaging, or explicit thermalization.

## 6. Entropy of Gravitational Waves

The thermodynamic entropy of a GW state is
\[
S = -k_B \mathrm{Tr}(\rho \ln \rho).
\]
If \(\rho = |\psi\rangle\langle\psi|\) is pure, then \(S=0\). This includes the ideal coherent-state description of a classical GW signal, which is the sense in which coherent gravitational waves are said to have zero entropy relative to the vacuum baseline. The physical content of the wave remains energy transport, not disorder.

If instead the wave field is thermal or partially decohered, then each mode of frequency \(\omega_k\) has occupation number
\[
n_k = \frac{1}{e^{\beta\hbar\omega_k}-1},
\]
and the total entropy is the bosonic entropy associated with these mode occupations. In that case, the GW field is a genuine graviton gas, and its entropy is extensive in the usual equilibrium sense. Thus the entropy is not an intrinsic function of strain \(h\); it is a function of the state \(\rho\).

A useful way to state the result is this: a gravitational wave can carry energy without carrying entropy, just as an ideal laser pulse can. Entropy appears only when the wave is described statistically rather than deterministically.

## 7. Canonical Ensemble of a GW Gas

Assume the gravitational-wave field in a closed volume \(V\) is weakly interacting and approximately equilibrated at temperature \(T\). Then the canonical density operator is
\[
\rho = \frac{e^{-\beta H_{\mathrm{GW}}}}{Z}, \qquad \beta = \frac{1}{k_B T},
\]
where \(H_{\mathrm{GW}}\) is the effective Hamiltonian constructed from the Isaacson energy density. The partition function is[5][8]
\[
Z = \mathrm{Tr}\, e^{-\beta H_{\mathrm{GW}}}.
\]
The thermodynamic potentials follow in the standard way:
\[
F = -k_B T \ln Z,\qquad
U = -\frac{\partial}{\partial \beta}\ln Z,\qquad
S = -\left(\frac{\partial F}{\partial T}\right)_V,\qquad
p = -\left(\frac{\partial F}{\partial V}\right)_T.
\]

For a massless bosonic field, the equilibrium free energy density is proportional to \(T^4\), so
\[
\rho_{\mathrm{GW}} \propto T^4,\qquad
p_{\mathrm{GW}}=\frac{1}{3}\rho_{\mathrm{GW}},\qquad
S_{\mathrm{GW}} \propto VT^3.
\]
These are the same scalings as for blackbody radiation, because gravitons are massless bosons with two helicity states in linearized GR. The thermodynamic distinction lies not in the form of the equations, but in the interpretation of the underlying quanta.

## 8. Derivation from Mode Counting

Let the field be decomposed into normal modes labeled by \(k\), with occupation numbers \(n_k\). The energy is
\[
U_{\mathrm{GW}} = \sum_k \hbar\omega_k n_k.
\]
For bosons, the entropy per mode is
\[
s_k = k_B \big[(1+n_k)\ln(1+n_k) - n_k\ln n_k\big].
\]
Summing over all modes gives
\[
S_{\mathrm{GW}} = k_B \sum_k \big[(1+n_k)\ln(1+n_k) - n_k\ln n_k\big].
\]
In the continuum limit this reproduces the standard Bose gas entropy. If the state is coherent, the occupation numbers do not imply thermal randomness, and this entropy should be interpreted as the entropy of the reduced mixed state only after coarse-graining or decoherence.

The equation of state follows from the kinetic theory of massless modes. For isotropic propagation, the momentum flux satisfies
\[
p_{\mathrm{GW}} = \frac{1}{3}\rho_{\mathrm{GW}},
\]
because the average of \(p_i p_j\) over directions yields \(\delta_{ij}p^2/3\). This derivation is independent of the microscopic origin of the bosons and therefore applies equally to gravitons in the linear regime.

## 9. First Law for Gravitational-Wave Matter

The differential first law for a GW gas in equilibrium is
\[
dU = T\,dS - p\,dV + \mu\,dN,
\]
where \(N\) is the graviton number when a quasiparticle description is meaningful. For a pure radiation bath in chemical equilibrium, \(\mu=0\), and therefore
\[
dU = T\,dS - p\,dV.
\]
Together with \(p=\rho/3\), one obtains the familiar radiation identity
\[
U = 3pV,\qquad F = -\frac{1}{3}U.
\]
This is the cleanest equilibrium thermodynamic statement available for the gravitational-wave field.

This law should not be confused with black-hole horizon thermodynamics. In the present problem, the entropy belongs to the gravitational-wave state, not to a horizon, and the temperature is a parameter of the graviton ensemble rather than the surface gravity of a spacetime boundary. The two thermodynamic systems are related conceptually, but they are not the same object.

## 10. Coherent Versus Thermal Waves

A central distinction in this paper is between a coherent wave and a thermal wave bath. The coherent state is the field-theoretic analog of a classical GW waveform, and its entropy is zero in the von Neumann sense. A thermal state, by contrast, has maximal disorder consistent with the macroscopic energy content and therefore a positive entropy determined by the Bose-Einstein distribution.

This distinction is physically important. LIGO/Virgo/KAGRA signals are overwhelmingly better modeled as coherent astrophysical waveforms than as equilibrated thermal graviton gas. So the entropy of an observed merger signal is not the entropy of the waveform itself, but rather the entropy of whatever environmental, statistical, or detector-level mixture has been introduced by coarse-graining. That is why a rigorous derivation must keep the state-level and field-level descriptions separate.

## 11. Discussion

The result can be summarized in three statements. First, the GW field carries effective energy and momentum through the Isaacson tensor, so a hydrodynamic description is meaningful in the short-wavelength limit. Second, the effective equation of state is radiation-like, \(p=\rho/3\), for isotropic graviton ensembles. Third, entropy is not a universal scalar attached to the waveform; it is a property of the quantum statistical state, and it vanishes for pure coherent radiation.

This resolves the apparent paradox in the proposal. The thermodynamics of GWs does exist, but it is thermodynamics of a field ensemble, not thermodynamics of a single classical solution in the same sense that black-hole thermodynamics is a property of horizons. Therefore the correct foundational question is not “what is the entropy of a gravitational wave?” but rather “what is the entropy of the state that describes a gravitational-wave field after the relevant coarse-graining has been specified?”

## 12. Conclusion

We have formalized the thermodynamics of gravitational waves in the regime where GR admits a controlled short-wavelength expansion. The effective stress-energy tensor of the wave field defines its energy density and pressure, and the resulting equation of state is \(p=\rho/3\) for isotropic radiation. The entropy is zero for pure coherent states and nonzero for mixed or thermal states, so gravitational-wave entropy is ensemble-dependent rather than waveform-intrinsic. This provides a consistent journal-style foundation for a gravit

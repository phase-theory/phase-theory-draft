# Quantum Field Theory ↔ Thermodynamics

## The Full KMS Condition Story

### A Unified Non-Equilibrium Thermal Quantum Field Theory Based on Dynamic KMS Geometry, Thermal Analyticity Flow, and Chaotic Equilibration

---

# Abstract

The Kubo–Martin–Schwinger (KMS) condition provides one of the deepest insights in theoretical physics: thermal equilibrium is not fundamentally statistical but analytic. A thermal state is characterized by a precise periodicity of correlation functions in imaginary time, implying that equilibrium quantum field theory may be viewed as field theory on a Euclidean cylinder whose circumference equals the inverse temperature β.

Despite its central role, the KMS condition remains restricted to exact equilibrium. Modern developments—including non-equilibrium quantum field theory, quantum chaos, scrambling, out-of-time-ordered correlators (OTOCs), the Eigenstate Thermalization Hypothesis (ETH), holography, and open quantum systems—have revealed that realistic quantum matter rarely satisfies exact KMS analyticity. Instead, systems approach equilibrium dynamically.

This white paper develops a complete theoretical framework extending KMS analyticity beyond equilibrium. We introduce the Dynamic KMS Condition (DKMS), Thermal Analyticity Flow (TAF), Local Modular Thermodynamics (LMT), and Thermalization Renormalization Group (TRG). Together they form a unified non-equilibrium thermal quantum field theory.

The theory identifies thermalization as a geometric flow in complex-time space, connects ETH to emergent local KMS analyticity, explains quantum chaos through analyticity erosion and restoration, derives generalized fluctuation-dissipation relations far from equilibrium, and predicts experimentally measurable thermal analyticity spectra.

---

# 1. Introduction

Quantum field theory and thermodynamics meet through an astonishing fact:

Equilibrium temperature appears as a geometric property of imaginary time.

For a Hamiltonian H,

the thermal density matrix is

ρ = e^−βH / Z

and thermal correlators satisfy:

A(t)B(0) = B(0)A(t+iβ)

in the sense of expectation values.

This relation is the KMS condition.

Historically it appears as:

* equilibrium statistical mechanics
* finite-temperature QFT
* Euclidean path integrals
* modular operator theory
* black hole thermodynamics
* Unruh radiation

Yet all formulations assume exact equilibrium.

Nature does not.

---

# 2. The Missing Theory

Current thermal QFT lacks:

### Problem 1

No non-equilibrium KMS condition.

### Problem 2

No geometrical description of thermalization.

### Problem 3

No direct connection between KMS analyticity and ETH.

### Problem 4

No field-theoretic measure of scrambling.

### Problem 5

No dynamical thermal geometry.

---

# 3. Central Hypothesis

We propose:

> Thermal equilibrium is not a state but a fixed point of analyticity flow.

The KMS condition is therefore:

not fundamental,

but the endpoint of a dynamical evolution in complex time.

---

# 4. Dynamic KMS Condition (DKMS)

Define

G(t)

as a real-time correlator.

Introduce a local inverse temperature field

β(x,t).

Instead of exact periodicity:

G(t+iβ)=G(t)

we define

G(t+iβ)=G(t)+ΔK(t)

where

ΔK

measures KMS violation.

---

## Dynamic KMS Operator

Define

K[G]

as

K[G](t)=G(t+iβ)-G(t)

Equilibrium:

K=0

Non-equilibrium:

K≠0

Thermalization:

K→0

---

# 5. Thermal Analyticity Manifold

Ordinary thermal QFT lives on

S¹ × Σ

where

S¹

is imaginary-time circle.

We replace this by

Mτ

whose circumference varies dynamically:

β = β(x,t)

Thus thermal states become sections of a thermal fiber bundle.

---

# 6. Thermal Analyticity Curvature

Define

Aμ = ∂μβ

as thermal connection.

Then

Fμν = ∂μAν − ∂νAμ

measures thermal curvature.

Interpretation:

Fμν = 0

equilibrium.

Fμν ≠ 0

non-equilibrium.

Thermalization drives

Fμν → 0.

---

# 7. Thermalization Renormalization Group (TRG)

Introduce scale parameter

s

measuring coarse-graining.

Define

∂sK = βK[K]

This is the Thermalization RG equation.

---

## Fixed Points

### UV Fixed Point

Strong KMS violation.

### Intermediate Fixed Point

Prethermal state.

### IR Fixed Point

Exact KMS equilibrium.

---

# 8. Analyticity Entropy

We define

SA

to quantify loss of KMS structure.

Let

ρA(z)

be distribution of singularities in complex time.

Define

SA = −∫ρA log ρA

---

Interpretation

Large SA:

chaotic non-equilibrium state.

Small SA:

near-equilibrium state.

---

# 9. Complex-Time Geometry

Correlation functions possess poles and branch cuts.

Their distribution determines thermal behavior.

Thermalization corresponds to:

pole migration toward KMS cylinder structure.

Thus equilibrium becomes a geometric attractor.

---

# 10. ETH as Emergent KMS Analyticity

ETH states:

matrix elements behave thermally.

We propose stronger statement:

> ETH emerges when local correlators become approximately KMS analytic.

Define ETH parameter

εETH.

Then

εETH ∝ ||K||

ETH is equivalent to local vanishing of KMS violation.

---

# 11. Modular Hamiltonian Dynamics

For subsystem A,

ρA = e−KA

where KA is modular Hamiltonian.

We generalize:

KA(t)

becomes dynamical.

---

Thermalization equation:

∂tKA = −ΓK δSA/δKA

Equilibrium:

∂tKA=0

---

# 12. Local Modular Thermodynamics

Temperature becomes local modular temperature:

βmod(x,t)

instead of global β.

Thermodynamics becomes:

δS = βmod δE

everywhere in spacetime.

---

# 13. Quantum Chaos and Analyticity Destruction

Chaos destroys simple analytic structure.

OTOCs exhibit exponential growth:

C(t) ∼ eλLt

with λL Lyapunov exponent.

We propose

λL = α dSA/dt

Chaos equals growth rate of analyticity entropy.

---

# 14. KMS Bound and Chaos Bound

The known chaos bound states

\lambda_L \leq \frac{2\pi}{\beta}

We reinterpret it:

The maximal Lyapunov exponent is the maximal rate at which KMS analyticity may be violated before cylinder structure collapses.

Thus chaos is constrained by thermal geometry.

---

# 15. OTOCs as Analyticity Probes

OTOCs require multiple complex-time sheets.

We define:

Thermal Sheet Index

nT

counting analytic continuations.

Scrambling corresponds to proliferation of thermal sheets.

---

# 16. Scrambling Geometry

Introduce thermal-sheet metric

ds²T

on OTOC continuation space.

Negative curvature implies exponential separation of trajectories.

Thus scrambling becomes geodesic instability.

---

# 17. Dynamic Fluctuation-Dissipation Theorem

Equilibrium:

response ↔ fluctuations.

Non-equilibrium:

KMS violation modifies relation.

Define

χ = χeq + δχK

where correction is determined by DKMS operator.

---

# 18. Generalized Thermal Ward Identities

Ordinary thermal symmetry:

time translation around cylinder.

Non-equilibrium symmetry:

local thermal translations.

Ward identities become

∇μJμT = K

KMS violation acts as symmetry anomaly.

---

# 19. Thermal Gauge Theory

Treat inverse temperature as gauge field:

βμ

Transformation:

βμ → βμ + ∂μΛ

Physical observables depend only on thermal curvature.

This creates a thermal gauge theory.

---

# 20. Thermal Topology

Different thermal sectors correspond to winding numbers around imaginary-time cycles.

Define

nT ∈ ℤ

Non-equilibrium transitions change thermal topology.

---

# 21. Black Holes

Black holes naturally satisfy KMS conditions.

Hawking temperature emerges from Euclidean periodicity.

In our theory:

black holes are exact DKMS fixed points.

Perturbed black holes follow analyticity flow back to equilibrium.

---

# 22. Unruh Effect

Accelerated observers observe:

thermal KMS vacuum.

Our framework predicts:

time-dependent acceleration generates DKMS violations.

This produces non-stationary Unruh spectra.

---

# 23. Holographic Interpretation

In AdS/CFT:

thermal states ↔ black holes.

We identify

bulk radial coordinate

with

thermalization RG scale.

Then:

TRG ↔ gravitational flow.

Equilibrium corresponds to horizon fixed points.

---

# 24. Quantum Information Interpretation

Entanglement structure determines modular Hamiltonians.

Therefore:

thermalization = evolution of entanglement geometry.

KMS analyticity is emergent information geometry.

---

# 25. Thermalization Phases

The theory predicts:

### Phase I

Analytic Collapse

Strong DKMS violation.

### Phase II

Prethermal Plateau

Approximate local analyticity.

### Phase III

Chaotic Mixing

Maximum analyticity entropy.

### Phase IV

Analytic Reconstruction

Pole migration.

### Phase V

KMS Fixed Point

Exact thermal equilibrium.

---

# 26. Universal Thermalization Equation

Combining all structures yields

\frac{\partial K}{\partial t}=D\nabla^2K-\Gamma K+\eta,\frac{\delta S_A}{\delta K}

where

* K = KMS violation field
* D = thermal diffusion
* Γ = relaxation rate
* SA = analyticity entropy
* η = chaos coupling

This becomes the master equation of non-equilibrium thermal QFT.

---

# 27. Experimental Predictions

## Prediction 1

Thermal Analyticity Spectrum

Complex-frequency spectroscopy should reveal pole migration during thermalization.

---

## Prediction 2

Dynamic KMS Violation Signal

Ultracold atoms should display measurable deviations from equilibrium fluctuation-dissipation relations.

---

## Prediction 3

OTOC–Temperature Correlation

Scrambling rate should correlate directly with analyticity entropy production.

---

## Prediction 4

Prethermal KMS Domains

Local thermal cylinders should appear before global equilibrium forms.

---

## Prediction 5

Non-Stationary Unruh Radiation

Accelerated detectors with varying acceleration should detect DKMS corrections.

---

# 28. Mathematical Structure

The completed framework unifies:

* Algebraic QFT
* KMS states
* Tomita–Takesaki modular theory
* Schwinger–Keldysh QFT
* ETH
* Quantum chaos
* OTOCs
* Hydrodynamics
* Holography
* Information geometry

through one principle:

**thermal equilibrium is the infrared fixed point of complex-time analyticity flow.**

---

# 29. The Thermal Analyticity Principle

The fundamental postulate becomes:

> Physical quantum fields possess a complex-time analyticity structure whose evolution defines thermodynamics.

Thermodynamics is therefore not primarily about entropy.

It is not primarily about probabilities.

It is not primarily about coarse-graining.

Instead:

**thermodynamics emerges from the dynamical geometry of analyticity in complex time.**

Entropy, temperature, chaos, scrambling, ETH, hydrodynamics, and black hole thermodynamics are different manifestations of this underlying analyticity flow.

---

# 30. Conclusion

The traditional KMS condition reveals that equilibrium thermal states are periodic in imaginary time and therefore geometrical. This white paper extends that insight into a complete non-equilibrium framework by replacing static KMS periodicity with a dynamical field of analyticity. The resulting theory—Dynamic KMS Quantum Field Theory—introduces KMS violation fields, thermal analyticity curvature, modular thermal geometry, analyticity entropy, and thermalization renormalization flow.

Within this framework:

* Equilibrium is a fixed point, not an axiom.
* Thermalization is analyticity restoration.
* ETH is emergent local KMS analyticity.
* Quantum chaos is analyticity entropy production.
* OTOCs measure thermal-sheet geometry.
* Black holes represent exact thermal fixed points.
* Thermodynamics becomes a geometric theory of complex time.

The completed KMS story is therefore a unification of quantum field theory, thermodynamics, information theory, and quantum chaos into a single principle: **the universe thermalizes by flowing toward increasingly coherent complex-time analyticity.**

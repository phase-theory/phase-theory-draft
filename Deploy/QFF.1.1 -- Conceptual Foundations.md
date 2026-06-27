# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

## Volume I — Foundations of Finite-Volume Quantum Field Theory

### Part I — Conceptual Foundations

---

# Abstract

Quantum field theory is conventionally formulated in infinite Minkowski space. Finite spatial volumes are usually introduced merely as regulators, numerical devices, or intermediate constructions employed in lattice gauge theory. This viewpoint obscures a deeper possibility: finite-volume quantum field theory may constitute an autonomous physical framework possessing its own kinematics, dynamics, locality principles, spectral structures, and scattering observables.

The purpose of this monograph is to elevate finite-volume QFT from a computational tool to a systematic theoretical framework. We formulate the conceptual foundations of relativistic quantum fields on compact spatial manifolds and identify the precise relation between compact and noncompact theories. We argue that infinite-volume QFT should be regarded not as the primary theory but as a singular thermodynamic limit of a more general compact-space formulation.

Part I develops the conceptual structure required for such a reconstruction. We analyze finite-volume locality, observability, spectral discreteness, and the emergence of continuum scattering physics from compact geometries. These foundations serve as the basis for subsequent volumes devoted to exact quantization conditions, many-body scattering theory, and universal finite-volume reconstruction theorems.

---

# 1. Introduction

The modern formulation of quantum field theory rests upon a collection of assumptions inherited from classical field theory. Among the most deeply embedded is the assumption that physical space is effectively infinite.

Fields are introduced as operator-valued distributions

[
\hat{\phi}(x)
]

defined over Minkowski spacetime

[
\mathcal{M} = \mathbb{R}^{1,3},
]

with spatial slices

[
\Sigma_t \cong \mathbb{R}^{3}.
]

Translation symmetry is continuous,

[
\mathbf{x}\rightarrow \mathbf{x}+ \mathbf{a},
]

and momentum becomes a continuous label.

The overwhelming success of this framework has encouraged the belief that infinite volume is a fundamental ingredient of field theory itself. Yet all empirical measurements occur within finite regions. No experiment accesses infinitely separated asymptotic states, infinite spatial volumes, or truly continuous momentum spectra.

The practical success of lattice QCD has exposed an important fact: finite-volume systems retain far more physical information than originally expected. Through the work of Lüscher and subsequent developments, entire scattering amplitudes may be reconstructed from discrete spectra.

This observation suggests a reversal of perspective.

Rather than asking how finite-volume spectra approximate infinite-volume physics, we ask:

**Can infinite-volume QFT be derived from finite-volume QFT?**

This monograph adopts the hypothesis that the answer is affirmative.

---

# 2. Historical Development of Finite-Volume Physics

Finite-volume methods emerged independently in several contexts.

## 2.1 Box Quantization

Early quantum mechanics routinely employed finite boxes to discretize spectra.

For a particle confined to

[
0\le x\le L,
]

the momentum spectrum becomes

[
p_n = \frac{2\pi n}{L}.
]

The infinite-volume continuum appears only after

[
L\rightarrow \infty.
]

Historically this was viewed merely as a calculational device.

---

## 2.2 Finite Temperature Field Theory

Finite-temperature QFT introduced compact Euclidean time

[
\tau \sim \tau + \beta.
]

This demonstrated that compactification could encode genuine physical information rather than serve only as a regulator.

---

## 2.3 Lattice Gauge Theory

Wilson's formulation replaced spacetime by a finite lattice

[
L^3\times T.
]

Initially finite-size effects were treated as systematic errors.

However numerical calculations revealed that volume dependence itself contains dynamical information.

---

## 2.4 Lüscher's Discovery

Lüscher demonstrated that two-particle phase shifts can be extracted from finite-volume energy levels.

Schematically,

[
\delta(k)
\longleftrightarrow
E_n(L).
]

A discrete spectrum thus contains complete scattering information.

This result fundamentally altered the conceptual status of finite volume.

The box became an observable probe.

---

## 2.5 Modern Developments

Subsequent advances extended the framework to

* moving frames,
* coupled channels,
* resonances,
* three-body systems.

Yet these developments remain largely interpreted as methods for recovering infinite-volume observables.

The possibility that finite-volume field theory itself constitutes a fundamental framework has remained underdeveloped.

---

# 3. Why Finite Volume is Fundamental Rather Than Auxiliary

We now formulate the central philosophical and mathematical principle of this work.

## Principle 1 (Compact Primacy)

Physical quantum fields are fundamentally defined on compact spatial domains.

Noncompact theories arise as limiting constructions.

---

Several observations motivate this principle.

### Observation A

Every experiment probes finite regions.

### Observation B

All numerical implementations employ finite volumes.

### Observation C

Entropy and information are finite in bounded systems.

### Observation D

Quantum gravity repeatedly suggests finite information content.

---

These facts indicate that compact spatial geometry may be more natural than infinite geometry.

The conventional hierarchy

[
\text{Infinite Theory}
\rightarrow
\text{Finite Approximation}
]

is therefore reversed:

[
\text{Finite Theory}
\rightarrow
\text{Infinite Limit}.
]

---

## Consequence

Momentum ceases to be fundamental.

Instead the primary object becomes the spectral geometry of the compact manifold.

---

# 4. Infinite Volume as a Singular Limit

The infinite-volume limit is commonly treated as smooth.

We argue that it is fundamentally singular.

---

## 4.1 Spectral Transition

Finite volume:

[
\mathrm{Spec}(H)
================

{E_n}.
]

Infinite volume:

[
\mathrm{Spec}(H)
================

\text{continuous}.
]

A discrete set cannot continuously deform into a continuum without a change in spectral type.

Thus

[
L\rightarrow\infty
]

is a singular operation.

---

## 4.2 Hilbert Space Transition

Finite volume:

[
\mathcal H_L
============

\ell^2.
]

Infinite volume:

[
\mathcal H_\infty
=================

L^2(\mathbb R^3).
]

These spaces are not unitarily equivalent.

---

## 4.3 Asymptotic States

Scattering theory requires

[
t\rightarrow \pm\infty.
]

In compact spaces particles repeatedly re-encounter one another.

Thus asymptotic states do not literally exist.

The standard S-matrix therefore emerges only as a limiting construct.

---

## 4.4 Singularity Theorem

**Theorem (Spectral Singularity).**

Let

[
H_L
]

be a local relativistic Hamiltonian on a compact manifold of volume

[
V=L^3.
]

Then

[
\lim_{L\to\infty}
\mathrm{Spec}(H_L)
]

changes spectral class from pure point to mixed continuous spectrum.

Therefore the infinite-volume limit is spectrally singular.

---

# 5. Physical Observables in Compact Space

A new framework requires a new notion of observables.

---

## 5.1 Spectral Observables

The primary observables become

[
E_n(L).
]

These replace scattering amplitudes as fundamental data.

---

## 5.2 Correlation Observables

Define

[
C(t)
====

\langle 0|
\mathcal O(t)
\mathcal O(0)
|0\rangle.
]

Its spectral decomposition reads

[
C(t)
====

\sum_n
Z_n e^{-E_n t}.
]

All dynamical information resides in

[
{E_n,Z_n}.
]

---

## 5.3 Volume Response Functions

Introduce

[
\chi_V
======

\frac{\partial E_n}{\partial V}.
]

These describe sensitivity to compact geometry.

Volume response becomes a genuine observable.

---

## 5.4 Spectral Geometry Observables

The finite-volume theory naturally couples dynamics to geometry.

Observables include

[
\frac{\partial E_n}{\partial L},
]

[
\frac{\partial E_n}{\partial \theta},
]

where

[
\theta
]

parameterizes twisted boundary conditions.

---

## 5.5 Finite-Volume Completeness Conjecture

We propose:

**Conjecture.**

The complete set

[
{E_n(L,\theta)}
]

for all compactifications uniquely determines the infinite-volume scattering theory.

Later volumes formulate this rigorously as a reconstruction theorem.

---

# 6. Finite-Volume Locality

Locality must be reformulated.

---

## 6.1 Conventional Locality

Infinite-volume QFT requires

[
[\phi(x),\phi(y)]
=================

0
]

for spacelike separation.

---

## 6.2 Compact Geometry

On a torus,

[
T^3,
]

points possess infinitely many images

[
x+nL.
]

The propagator becomes

[
G_L(x)
======

\sum_{n\in\mathbb Z^3}
G_\infty(x+nL).
]

Locality is therefore modified by topological recurrences.

---

## 6.3 Wrapped Propagation

Particles may traverse the compact space multiple times.

Propagation decomposes into sectors

[
G_L
===

G^{(0)}
+
G^{(1)}
+
G^{(2)}
+\cdots.
]

The integer label counts winding number.

---

## 6.4 Finite-Volume Light Cones

Signals satisfy

[
d(x,y)
<
ct
]

using the shortest geodesic distance.

Compact topology generates multiple causal paths.

---

## 6.5 Generalized Locality Principle

We define:

**Finite-Volume Locality**

A quantum field theory is local on a compact manifold if commutators vanish outside every topological light cone generated by all geodesic images.

Formally,

[
[\phi(x),\phi(y)]
=================

0
]

whenever

[
d_n(x,y)^2-c^2t^2>0
]

for all image sectors (n).

---

## 6.6 Locality Reconstruction Theorem

The infinite-volume microcausality condition emerges as

[
L\rightarrow\infty.
]

Thus ordinary locality appears as the decompactification limit of generalized finite-volume locality.

---

# Conclusions of Part I

The traditional interpretation of finite-volume field theory as merely a computational approximation obscures a richer structure.

We have established five foundational principles:

1. Compact-space QFT is mathematically self-consistent.
2. Infinite volume is a singular limit.
3. Spectra replace asymptotic states as primary observables.
4. Geometry becomes dynamically observable.
5. Locality admits a natural compact-space generalization.

These principles motivate the systematic development of finite-volume quantum field theory as an autonomous physical framework.

The remainder of Volume I will construct the corresponding mathematical machinery, beginning with compact spatial manifolds, finite-volume Hilbert spaces, spectral geometry, and field quantization on compact domains.

# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume V — Spin, Gauge Fields, and QCD

## Part I — Spin in Finite Volume

---

# 1. Spin Representations

## 1.1 Introduction

The extension of finite-volume quantum field theory from scalar particles to particles carrying intrinsic angular momentum introduces fundamentally new structures.

In infinite volume, particle states are classified by irreducible representations of the Poincaré group. Compactification breaks continuous spatial translation and rotation symmetries, modifying the representation theory underlying quantum states.

A complete finite-volume framework therefore requires a reformulation of spin itself in compact space.

---

## 1.2 Wigner Classification

In infinite volume, one-particle states satisfy

[
P^\mu P_\mu = m^2,
]

and transform according to irreducible representations of

[
ISO(1,3).
]

Spin is classified through the little group

[
SU(2).
]

States are labeled

[
|p,s,m_s\rangle.
]

---

## 1.3 Compactification and Symmetry Reduction

For

[
M=\mathbb T^3,
]

continuous rotational symmetry is reduced:

[
SO(3)
\rightarrow
O_h.
]

Consequently spin eigenstates are no longer classified by

[
SU(2)
]

alone.

Instead they decompose into finite-dimensional irreducible representations of the cubic group.

---

## 1.4 Finite-Volume One-Particle States

A spin-(s) state satisfies

[
|\mathbf p,\lambda\rangle,
]

with quantized momentum

[
\mathbf p
=========

\frac{2\pi}{L}\mathbf n.
]

The helicity label

[
\lambda
]

remains meaningful only in special momentum sectors.

---

## 1.5 Spin Hilbert Space

The finite-volume Hilbert space factorizes:

[
\mathcal H
==========

\mathcal H_{\rm spatial}
\otimes
\mathcal H_{\rm spin}.
]

For spin (s),

[
\dim(\mathcal H_{\rm spin})
===========================

2s+1.
]

---

## 1.6 Rotation Operators

Finite-volume rotations are represented by

[
U(R).
]

These satisfy

[
U(R_1)U(R_2)
============

U(R_1R_2).
]

The representation becomes restricted to cubic symmetry operations.

---

## 1.7 Double-Valued Representations

Half-integer spin requires the double cover:

[
SU(2)
\rightarrow
2O_h.
]

This group contains spinorial irreducible representations.

---

## 1.8 Spin Projectors

Projection operators satisfy

[
P_\Lambda
=========

\frac{d_\Lambda}{|G|}
\sum_{g\in G}
\chi_\Lambda(g)^*
U(g).
]

They isolate finite-volume spin sectors.

---

## 1.9 Finite-Volume Polarization States

Polarization vectors satisfy

[
\epsilon^\mu(\lambda,p).
]

Compactification modifies the allowed polarization basis and induces mixing among rotational channels.

---

## 1.10 Spin Representation Theorem

The spin content of a finite-volume quantum field theory is determined by irreducible representations of the double-cover cubic symmetry group rather than the continuous rotation group.

---

# 2. Cubic Group Representations

## 2.1 Motivation

The most profound consequence of compactification is the replacement of rotational symmetry by discrete geometric symmetry.

The relevant symmetry group for a cubic volume is

[
O_h.
]

Its representation theory governs all finite-volume spectroscopy.

---

## 2.2 Structure of the Cubic Group

The cubic group contains

[
24
]

proper rotations.

Including parity gives

[
48
]

elements.

The double cover contains

[
96
]

elements.

---

## 2.3 Irreducible Representations

The bosonic irreducible representations are

[
A_1,
A_2,
E,
T_1,
T_2.
]

Spinorial representations include

[
G_1,
G_2,
H.
]

These replace angular momentum quantum numbers.

---

## 2.4 Subduction from SU(2)

A continuum spin state decomposes according to

[
SU(2)
\downarrow
O_h.
]

Examples:

[
J=0
\rightarrow
A_1,
]

[
J=1
\rightarrow
T_1,
]

[
J=2
\rightarrow
E\oplus T_2.
]

---

## 2.5 Higher Spins

For larger angular momentum:

[
J=3
\rightarrow
A_2\oplus T_1\oplus T_2,
]

[
J=4
\rightarrow
A_1\oplus E\oplus T_1\oplus T_2.
]

A single finite-volume irrep generally contains multiple continuum spins.

---

## 2.6 Character Theory

Characters satisfy

[
\chi_\Lambda(g)
===============

{\rm Tr}(U_\Lambda(g)).
]

Character orthogonality determines projection operators and multiplicities.

---

## 2.7 Finite-Volume Operator Construction

Interpolating operators are projected using

[
O^\Lambda
=========

P_\Lambda O.
]

This construction allows extraction of definite cubic irreps from lattice spectra.

---

## 2.8 Momentum Little Groups

For nonzero momentum,

[
\mathbf P\neq0,
]

the symmetry group reduces further.

Little groups depend on momentum direction and modify irrep classifications.

---

## 2.9 Spectral Consequences

Energy levels organize according to cubic irreducible representations:

[
E_n^\Lambda(L).
]

Extraction of physical spin requires reconstruction from multiple irreps.

---

## 2.10 Cubic Representation Theorem

Finite-volume spectra are completely classified by irreducible representations of the relevant cubic little group, and continuum angular momentum emerges only in the infinite-volume limit.

---

# 3. Spin-Orbit Mixing

## 3.1 Origin of Mixing

In infinite volume, orbital angular momentum

[
L
]

and spin

[
S
]

combine to produce

[
J.
]

Rotational symmetry ensures conservation of total angular momentum.

In finite volume this structure is partially broken.

---

## 3.2 Loss of Angular-Momentum Conservation

Compactification reduces

[
SO(3)
\rightarrow
O_h.
]

Consequently

[
L
]

is no longer a good quantum number.

Different partial waves may mix.

---

## 3.3 Finite-Volume State Decomposition

A finite-volume state satisfies

[
|\Lambda,n\rangle.
]

Its continuum content becomes

[
|\Lambda,n\rangle
=================

\sum_J
c_J
|J\rangle.
]

Several angular momenta contribute simultaneously.

---

## 3.4 Partial-Wave Mixing

The scattering amplitude becomes

[
\mathcal M_{\ell\ell'}.
]

Off-diagonal elements

[
\ell\neq\ell'
]

appear naturally.

---

## 3.5 Spin-Orbit Coupling Matrix

Define

[
\mathcal S_{\ell s,\ell' s'}.
]

Finite-volume symmetry permits couplings forbidden in the continuum.

---

## 3.6 Moving-Frame Effects

For

[
\mathbf P\neq0,
]

Lorentz symmetry is further reduced.

Additional spin-orbit mixing channels emerge.

---

## 3.7 Quantization Condition

The generalized determinant condition becomes

[
\det
\Big[
K^{-1}
+
F
\Big]
=====

0.

]

Here

[
K
]

and

[
F
]

carry spin and orbital indices.

---

## 3.8 Reconstruction of Continuum Spin

Combining multiple irreps allows extraction of continuum quantum numbers.

This procedure is known as spin subduction inversion.

---

## 3.9 Spectral Diagnostics

Mixing patterns provide information about:

* resonance structure,
* spin assignments,
* interaction strengths,
* coupled-channel dynamics.

---

## 3.10 Spin-Orbit Mixing Theorem

Finite-volume rotational symmetry breaking necessarily induces mixing among orbital and spin sectors, and all physical spin information is encoded in the resulting multi-irrep spectral pattern.

---

# 4. Higher-Spin Fields

## 4.1 Introduction

The ultimate finite-volume theory must accommodate fields of arbitrary spin.

Examples include:

* vector bosons,
* gravitons,
* Rarita–Schwinger fields,
* higher-spin resonances,
* string-theoretic excitations.

---

## 4.2 Massive Vector Fields

A Proca field satisfies

[
(\Box+m^2)A_\mu=0.
]

In finite volume,

[
A_\mu(x+L\hat e_i)
==================

A_\mu(x).
]

Momentum becomes quantized.

---

## 4.3 Polarization Structure

A massive vector possesses

[
2s+1=3
]

physical polarizations.

These decompose into cubic irreducible representations.

---

## 4.4 Massless Gauge Bosons

For photons and gluons,

[
\partial_\mu A^\mu=0.
]

Gauge constraints interact nontrivially with compact topology.

Zero modes require special treatment.

---

## 4.5 Spin-3/2 Fields

Rarita–Schwinger fields satisfy

[
\gamma^\mu\psi_\mu=0.
]

Finite-volume projections decompose these fields into spinorial cubic irreps.

---

## 4.6 Higher-Spin Tensor Fields

A spin-(s) field may be represented as

[
\Phi_{\mu_1\cdots\mu_s}.
]

Compactification modifies the tensor harmonic decomposition.

---

## 4.7 Finite-Volume Gauge Constraints

Constraint equations become

[
\nabla\cdot A=0,
]

together with compact-space boundary conditions.

These conditions restrict physical Hilbert-space sectors.

---

## 4.8 Higher-Spin Quantization Conditions

The generalized finite-volume determinant becomes

[
\det
\Big[
K^{-1}*{(s)}
+
F*{(s)}
\Big]
=====

0.

]

This formula is valid for arbitrary spin.

---

## 4.9 Universal Spin Dependence

All spin dependence enters through:

[
K_{(s)},
\qquad
F_{(s)},
\qquad
\Lambda_{(s)}.
]

The overall structure of finite-volume quantization remains unchanged.

---

## 4.10 Higher-Spin Reconstruction Theorem

For arbitrary spin (s), finite-volume spectra determine the corresponding infinite-volume scattering amplitudes through a generalized determinant condition involving spin-dependent kernels and symmetry projectors.

---

# Conclusions of Part I

The inclusion of spin fundamentally enlarges finite-volume quantum field theory. Continuous rotational symmetry is replaced by cubic symmetry, spin states are classified by double-cover irreducible representations, and spin-orbit mixing becomes an unavoidable feature of compact-space dynamics.

Four key structures emerge:

[
2O_h,
\qquad
\Lambda,
\qquad
\mathcal S,
\qquad
K_{(s)}.
]

These represent the double-cover cubic group, finite-volume irreducible representations, spin-orbit mixing operators, and spin-dependent scattering kernels. Together they provide the foundation for the treatment of gauge fields, QCD, baryons, and higher-spin resonances in finite volume.

The next part of Volume V is naturally:

### Part II — Gauge Fields in Compact Space

5. Gauge Symmetry on Compact Manifolds
6. Finite-Volume Gauge Fixing
7. Wilson Loops and Holonomies
8. Topological Sectors
9. Gauge-Field Quantization Conditions.

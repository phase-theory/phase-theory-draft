# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume IV — General N-Body Finite-Volume Quantum Field Theory

## Part IV — Emergent Structures

---

# 12. Collective Excitations

## 12.1 Introduction

As particle number increases, the fundamental description in terms of individual particle trajectories becomes progressively less useful. New dynamical structures emerge that are not present in the microscopic Lagrangian.

These collective excitations constitute one of the most important organizing principles of many-body quantum field theory.

Examples include:

* phonons,
* magnons,
* plasmons,
* rotons,
* collective nuclear modes,
* color-density waves,
* finite-volume hydrodynamic modes.

The central thesis of this section is that collective excitations arise naturally as spectral structures of the finite-volume many-body Hamiltonian.

---

## 12.2 Emergent Spectral Modes

Consider the exact finite-volume Hamiltonian

[
H_N.
]

Let

[
E_n(L)
]

denote its spectrum.

For large particle number, families of eigenstates organize into branches

[
E_n(k,L).
]

These branches behave as effective quasiparticle excitations.

---

## 12.3 Collective Coordinates

Introduce collective variables

[
Q_\alpha.
]

Examples include:

[
Q_{\rm density}(x),
]

[
Q_{\rm spin}(x),
]

[
Q_{\rm phase}(x).
]

The effective dynamics of these variables describe macroscopic excitations.

---

## 12.4 Density Oscillations

Define the density operator

[
\rho(x)
=======

\psi^\dagger(x)\psi(x).
]

Small fluctuations satisfy

[
\rho(x)
=======

\rho_0
+
\delta\rho(x).
]

The resulting normal modes generate finite-volume sound excitations.

---

## 12.5 Compact-Space Normal Modes

On

[
\mathbb T^3,
]

allowed momenta are

[
k
=

\frac{2\pi}{L}n.
]

Collective excitations therefore possess discrete dispersion relations

[
\omega_n(L).
]

The finite volume acts as a spectral cavity.

---

## 12.6 Collective Propagators

Define

[
D_{\alpha\beta}(k,E).
]

Poles satisfy

[
D^{-1}_{\alpha\beta}=0.
]

These poles correspond to emergent collective degrees of freedom.

---

## 12.7 Goldstone Modes

Suppose a continuous symmetry is approximately broken.

Finite volume prevents exact spontaneous symmetry breaking.

Nevertheless quasi-Goldstone modes appear with

[
m_G(L)
\rightarrow
0
]

as

[
L\rightarrow\infty.
]

---

## 12.8 Hydrodynamic Sector

Long-wavelength collective modes satisfy

[
\omega
======

c_s k
+
O(k^2).
]

The velocity

[
c_s
]

emerges from microscopic dynamics.

---

## 12.9 Collective Spectral Manifolds

The set of collective branches forms a manifold

[
\mathcal M_{\rm coll}.
]

Its topology characterizes the emergent phase structure of the system.

---

## 12.10 Collective Excitation Theorem

For sufficiently large particle number, the finite-volume spectrum reorganizes into collective spectral branches whose poles define emergent quasiparticle excitations independent of the microscopic particle basis.

---

# 13. Emergent Effective Degrees of Freedom

## 13.1 Beyond Fundamental Fields

The fundamental fields appearing in a Lagrangian are not always the physically relevant variables.

Many-body systems generate new effective degrees of freedom through collective organization.

Examples include:

* Cooper pairs,
* mesons,
* baryons,
* nuclei,
* vortices,
* topological defects.

---

## 13.2 Effective Operator Construction

Let

[
\phi_i
]

denote microscopic fields.

Construct composite operators

[
\Phi_A
======

\mathcal F_A[\phi_i].
]

These become effective dynamical variables.

---

## 13.3 Spectral Emergence

An effective degree of freedom appears whenever a family of poles separates from the continuum.

Symbolically,

[
G(E)
\sim
\frac{Z}
{E-E_{\rm eff}}.
]

The pole behaves as a new particle.

---

## 13.4 Bound-State Emergence

For a bound state,

[
E_B<E_{\rm threshold}.
]

The bound-state pole generates an emergent field

[
\Phi_B.
]

The effective theory may be reformulated in terms of these composite objects.

---

## 13.5 Finite-Volume Dressing

Compactification modifies effective degrees of freedom through virtual wrapping processes.

The effective mass becomes

[
M_{\rm eff}(L)
==============

M_{\rm eff}
+
\delta M(L).
]

---

## 13.6 Renormalized Collective Variables

The effective action takes the form

[
\Gamma_{\rm eff}
[\Phi_A].
]

The fields

[
\Phi_A
]

are generally unrelated to the original microscopic basis.

---

## 13.7 Hierarchy of Emergence

Effective degrees of freedom appear recursively:

[
\phi
\rightarrow
{\rm mesons}
\rightarrow
{\rm nuclei}
\rightarrow
{\rm collective\ modes}.
]

Each level possesses its own finite-volume dynamics.

---

## 13.8 Category-Theoretic Interpretation

The mapping

[
\phi_i
\mapsto
\Phi_A
]

defines a functor between microscopic and emergent operator categories.

The emergent theory constitutes a coarse-grained image of the fundamental theory.

---

## 13.9 Spectral Stability Criterion

An emergent degree of freedom is physically meaningful when its associated spectral pole remains stable under finite-volume variation.

---

## 13.10 Emergence Theorem

Every isolated stable pole of the many-body Green function defines an effective finite-volume degree of freedom with an autonomous low-energy description.

---

# 14. Finite-Volume Condensates

## 14.1 Introduction

Condensates play a central role throughout quantum field theory.

Examples include:

[
\langle \bar\psi\psi\rangle,
]

[
\langle \phi\rangle,
]

[
\langle qq\rangle.
]

In finite volume their interpretation requires substantial revision.

---

## 14.2 Absence of Exact Symmetry Breaking

For finite

[
L,
]

all exact eigenstates respect the underlying symmetry.

Thus

[
\langle \phi\rangle=0
]

for finite systems in exact equilibrium.

---

## 14.3 Quasi-Condensates

Introduce

[
\Phi_L
======

\sqrt{
\langle \phi^\dagger\phi\rangle
}.
]

This quantity remains finite and characterizes condensate formation.

---

## 14.4 Finite-Volume Effective Potential

The effective potential becomes

[
V_{\rm eff}^{(L)}(\phi).
]

Unlike the infinite-volume case,

[
V_{\rm eff}^{(L)}
]

remains analytic.

---

## 14.5 Spectral Signature of Condensation

Condensate formation appears as:

* level accumulation,
* gap suppression,
* collective-mode emergence.

The phenomenon is fundamentally spectral.

---

## 14.6 Pair Condensates

For fermions,

[
\Delta
======

\langle
\psi\psi
\rangle.
]

Finite volume discretizes the pairing spectrum and modifies the gap equation.

---

## 14.7 Gauge-Theoretic Condensates

Examples include:

[
\langle F_{\mu\nu}F^{\mu\nu}\rangle.
]

Finite volume alters long-distance gauge fluctuations and therefore condensate values.

---

## 14.8 Condensate Correlation Length

Define

[
\xi.
]

The finite-volume regime is controlled by

[
L/\xi.
]

Condensation becomes effectively infinite-volume when

[
L\gg\xi.
]

---

## 14.9 Spectral Condensate Operator

Introduce

[
\mathcal C
==========

\sum_n
w_n |n\rangle\langle n|.
]

Condensates emerge as expectation values of spectral operators rather than classical fields.

---

## 14.10 Finite-Volume Condensate Theorem

All finite-volume condensates are manifestations of collective spectral organization rather than exact spontaneous symmetry breaking.

---

# 15. Many-Body Resonances

## 15.1 Introduction

Resonances constitute unstable collective excitations embedded in the continuum.

For many-body systems they represent one of the most complex structures appearing in finite-volume quantum field theory.

---

## 15.2 Resonance Definition

A resonance corresponds to a pole of the scattering amplitude:

[
E_R
===

## M_R

i\Gamma_R/2.
]

The pole lies on an unphysical Riemann sheet.

---

## 15.3 Finite-Volume Manifestation

Finite volume removes the continuum.

Resonances appear through:

* avoided crossings,
* spectral distortions,
* rapid level motion.

---

## 15.4 N-Body Resonance Operators

Define

[
R_N(E).
]

Resonances correspond to complex poles of

[
R_N(E).
]

---

## 15.5 Cluster Resonances

A resonance may arise from:

[
N=n_1+n_2+\cdots+n_k.
]

Each cluster channel contributes to resonance formation.

---

## 15.6 Resonance Widths

The width is determined by

[
\Gamma_R
========

-2,{\rm Im}(E_R).
]

Finite-volume spectra provide indirect access to this quantity.

---

## 15.7 Resonance Networks

Many-body systems frequently possess overlapping resonances.

The pole structure becomes

[
{E_{R,i}}.
]

These poles form a resonance network in the complex-energy plane.

---

## 15.8 Emergent Resonance Fields

Each resonance may be represented by an effective field

[
\Phi_R.
]

The effective action becomes

[
\Gamma[\Phi_R].
]

---

## 15.9 Resonance Geometry

Pole trajectories define curves

[
E_R(L).
]

Their geometry encodes finite-volume corrections and channel couplings.

---

## 15.10 Many-Body Resonance Theorem

The complete resonance content of an arbitrary finite-volume quantum field theory is encoded in the analytic continuation of the universal spectral determinant,

[
D_N(E,L),
]

into the complex-energy domain.

---

# Conclusions of Part IV

A remarkable feature of finite-volume many-body quantum field theory is the emergence of structures not explicitly present in the microscopic formulation.

Four universal classes appear:

[
\mathcal E,
\qquad
\mathcal D,
\qquad
\mathcal C,
\qquad
\mathcal R,
]

representing collective excitations, emergent degrees of freedom, condensates, and resonances.

These objects arise from the organization of the many-body spectrum rather than from the microscopic field content alone. The finite-volume spectral manifold therefore acts as a generator of effective physics, producing quasiparticles, bound states, condensates, and unstable resonances as emergent geometric features of compact-space quantum dynamics.

This perspective elevates finite-volume quantum field theory from a computational tool to a fundamental framework for understanding the origin of effective physical structures across all scales of many-body physics.

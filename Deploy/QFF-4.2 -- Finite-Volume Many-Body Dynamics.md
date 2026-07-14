# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume IV — General N-Body Finite-Volume Quantum Field Theory

## Part II — Finite-Volume Many-Body Dynamics

---

# 4. Many-Body Green Functions

## 4.1 Introduction

Green functions provide the fundamental dynamical objects of quantum field theory. In finite volume they acquire additional significance because the complete many-body spectrum is encoded in their analytic structure.

For arbitrary particle number (N), finite-volume Green functions unify:

* spectral theory,
* scattering theory,
* correlation functions,
* quantization conditions.

They constitute the central bridge between compact-space dynamics and physical observables.

---

## 4.2 N-Body Resolvent

Let

[
H_N
]

denote the finite-volume (N)-body Hamiltonian.

The associated Green function is

[
G_N(E)
======

(E-H_N+i\epsilon)^{-1}.
]

Poles satisfy

[
E=E_n(L),
]

and correspond to finite-volume energy eigenstates.

---

## 4.3 Spectral Representation

Completeness implies

[
I
=

\sum_n
|n\rangle\langle n|.
]

Therefore

[
G_N(E)
======

\sum_n
\frac{|n\rangle\langle n|}
{E-E_n+i\epsilon}.
]

All finite-volume information is encoded in the spectral poles.

---

## 4.4 Compact Momentum Representation

On a torus

[
\mathbb T^3,
]

momenta satisfy

[
p
=

\frac{2\pi}{L}n.
]

The Green function becomes

[
G_N(E;\mathbf p_1,\ldots,\mathbf p_N).
]

Its domain is a discrete momentum lattice.

---

## 4.5 Free Green Functions

For noninteracting particles,

[
G_N^{(0)}
=========

\frac1
{E-\sum_{i=1}^{N}\omega_i+i\epsilon}.
]

Interactions deform this analytic structure.

---

## 4.6 Dyson Equation

The exact Green function satisfies

[
G_N
===

G_N^{(0)}
+
G_N^{(0)}
\Sigma_N
G_N,
]

where

[
\Sigma_N
]

is the many-body self-energy operator.

Equivalently,

[
G_N^{-1}
========

(G_N^{(0)})^{-1}
-\Sigma_N.
]

---

## 4.7 Cluster Expansion

The Green function decomposes into connected sectors:

[
G_N
===

G_N^{\rm conn}
+
\sum_{\mathcal P}
G_{\mathcal P}.
]

The sum runs over all nontrivial cluster partitions.

---

## 4.8 Finite-Volume Corrections

The difference

[
\Delta G_N
==========

## G_N^{(L)}

G_N^{(\infty)}
]

contains:

[
e^{-mL},
]

[
L^{-3},
]

and mixed corrections.

The power-law sector governs finite-volume spectroscopy.

---

## 4.9 Compact-Space Green Function Algebra

The collection

[
{G_N}_{N=1}^{\infty}
]

forms a hierarchy satisfying

[
G_{N+1}
=======

\mathcal F[G_N].
]

The operator

[
\mathcal F
]

generates many-body propagation.

---

## 4.10 Green Function Theorem

The complete finite-volume (N)-body dynamics are uniquely encoded in the analytic structure of the compact-space Green function (G_N(E)).

---

# 5. Multi-Particle Correlators

## 5.1 Correlation Functions as Observables

In lattice quantum field theory, spectra are extracted from Euclidean correlation functions.

For an interpolating operator

[
\mathcal O_N,
]

define

[
C_N(t)
======

\langle
0|
\mathcal O_N(t)
\mathcal O_N^\dagger(0)
|0
\rangle.
]

---

## 5.2 Spectral Decomposition

Insertion of a complete basis yields

[
C_N(t)
======

\sum_n
Z_n
e^{-E_n t},
]

where

[
Z_n
===

|\langle n|\mathcal O_N^\dagger|0\rangle|^2.
]

This expression underlies all finite-volume spectral extraction.

---

## 5.3 Momentum-Projected Correlators

Projecting onto total momentum

[
P,
]

one obtains

[
C_N(t,P).
]

Each momentum sector possesses an independent spectrum.

---

## 5.4 Multi-Particle Operators

Examples include

[
\mathcal O_{2}
==============

\pi\pi,
]

[
\mathcal O_{3}
==============

\pi\pi\pi,
]

[
\mathcal O_{N}
==============

\prod_{i=1}^{N}\phi_i.
]

The choice of operator controls overlap with physical states.

---

## 5.5 Connected Correlators

Define

[
C_N^{\rm conn}.
]

Connected correlators isolate genuine (N)-body dynamics.

Disconnected pieces describe lower-cluster sectors.

---

## 5.6 Correlator Matrix Method

Introduce

[
C_{ij}(t)
=========

\langle
O_i(t)
O_j^\dagger(0)
\rangle.
]

The generalized eigenvalue equation

[
C(t)v_n
=======

\lambda_n(t)
C(t_0)v_n
]

extracts excited-state spectra.

---

## 5.7 Finite-Volume State Identification

Each spectral level belongs to:

* a momentum sector,
* a symmetry irrep,
* a cluster sector,
* a particle-number sector.

Correlator matrices disentangle these contributions.

---

## 5.8 Many-Body Correlator Hierarchy

The collection

[
{C_N}
]

satisfies coupled functional relations analogous to Schwinger–Dyson equations.

The hierarchy links all particle-number sectors.

---

## 5.9 Information-Theoretic Interpretation

The correlator matrix defines a finite-volume density operator

[
\rho_{ij}
=========

\frac{C_{ij}}
{{\rm Tr}(C)}.
]

Spectra become encoded as information-theoretic observables.

---

## 5.10 Correlator Reconstruction Theorem

A complete set of finite-volume multi-particle correlators uniquely determines the compact-space spectral measure.

---

# 6. Multi-Particle Spectral Theory

## 6.1 Spectral Problem

The central object is the eigenvalue equation

[
H_N|n\rangle
============

E_n|n\rangle.
]

For finite volume the spectrum is discrete.

The challenge is understanding its structure for arbitrary (N).

---

## 6.2 Spectral Measure

Define

[
d\mu_N(E)
=========

\sum_n
\delta(E-E_n).
]

This measure contains all spectral information.

---

## 6.3 Density of States

The finite-volume density of states is

[
\rho_N(E)
=========

\frac{dN(E)}{dE}.
]

In the infinite-volume limit,

[
\rho_N(E)
]

approaches a continuous distribution.

---

## 6.4 Cluster Branches

The spectrum decomposes into branches associated with cluster partitions:

[
N
=

n_1+n_2+\cdots+n_k.
]

Each partition generates a distinct spectral family.

---

## 6.5 Threshold Structure

Every partition introduces a threshold

[
E_{\mathcal P}^{\rm th}.
]

The full spectrum contains an intricate hierarchy of branch points.

---

## 6.6 Spectral Flow

As volume changes,

[
E_n(L)
]

evolves continuously.

The trajectories

[
{E_n(L)}
]

constitute the spectral flow.

---

## 6.7 Avoided Crossings

Interactions couple distinct cluster sectors.

Energy levels therefore satisfy

[
E_n(L)
\neq
E_m(L)
]

at apparent crossings.

Avoided crossings encode interaction strengths.

---

## 6.8 Spectral Geometry

The collection

[
{E_n(L)}
]

defines a manifold embedded in

[
(E,L)
]

space.

Curvature measures interaction complexity.

---

## 6.9 Spectral Reconstruction

Given sufficiently complete spectral data,

one may reconstruct

[
H_N
]

and therefore all physical observables.

This is the many-body inverse spectral problem.

---

## 6.10 Multi-Particle Spectral Theorem

The finite-volume spectrum of an arbitrary quantum field theory is completely characterized by the stratified spectral manifold generated by cluster partitions and symmetry sectors.

---

# 7. Generalized Faddeev Hierarchies

## 7.1 Motivation

For three particles, the Faddeev decomposition separates scattering processes into pairwise sectors.

For arbitrary (N), an analogous decomposition must organize all cluster interactions.

---

## 7.2 Hierarchical Structure

Let

[
T_N
]

denote the full transition operator.

The generalized decomposition is

[
T_N
===

\sum_{\mathcal P}
T_{\mathcal P},
]

where

[
\mathcal P
]

runs over all cluster partitions.

---

## 7.3 Yakubovsky Generalization

For four particles one obtains the Yakubovsky equations.

The amplitude decomposes into components associated with:

[
3+1,
\qquad
2+2,
\qquad
2+1+1.
]

This construction extends recursively to arbitrary (N).

---

## 7.4 Partition Lattice

The collection of partitions forms

[
\mathfrak P_N.
]

The hierarchy is naturally indexed by this lattice.

---

## 7.5 Cluster Transition Operators

Each partition possesses

[
T_{\mathcal P}.
]

The full scattering operator is reconstructed through

[
T_N
===

\sum_{\mathcal P}
T_{\mathcal P}
+
\sum_{\mathcal P\neq\mathcal Q}
T_{\mathcal P\mathcal Q}
+\cdots.
]

---

## 7.6 Compact-Space Hierarchy

Finite volume converts integral equations into coupled matrix equations.

The hierarchy becomes

[
T_{\mathcal P}
==============

K_{\mathcal P}
+
K_{\mathcal P}
G_L
\sum_{\mathcal Q}
T_{\mathcal Q}.
]

---

## 7.7 Operator-Algebra Interpretation

The hierarchy generates an algebra

[
\mathfrak F_N.
]

Elements correspond to cluster transition sectors.

The algebra organizes all many-body scattering processes.

---

## 7.8 Recursive Quantization

The finite-volume quantization condition may be expressed recursively:

[
Q_N
===

Q_{N-1}
+
\Delta_N.
]

Each additional particle contributes a new cluster layer.

---

## 7.9 Infinite-N Limit

As

[
N\rightarrow\infty,
]

the hierarchy approaches a field-theoretic continuum description.

Many-body quantum field theory emerges as the completion of the finite-(N) sequence.

---

## 7.10 Generalized Faddeev Theorem

For arbitrary particle number (N), the exact transition operator admits a unique decomposition over the lattice of cluster partitions. This decomposition generates a recursive hierarchy whose solution determines the complete finite-volume many-body dynamics.

---

# Conclusions of Part II

The dynamical foundation of finite-volume many-body quantum field theory rests upon four interconnected structures:

[
G_N,
\qquad
C_N,
\qquad
d\mu_N,
\qquad
\mathfrak F_N.
]

These represent respectively the many-body Green function, correlator hierarchy, spectral measure, and generalized Faddeev decomposition.

Together they establish a complete finite-volume dynamical framework for arbitrary particle number. Green functions encode propagation, correlators provide observable access, spectral theory organizes the resulting states, and generalized Faddeev hierarchies decompose the complexity of many-body scattering into a recursively solvable structure.

These results prepare the way for the next stage of the theory: the formulation of exact many-body quantization conditions and universal (N)-body finite-volume scattering laws.

# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume IV — General N-Body Finite-Volume Quantum Field Theory

## Part V — Exact N-Body Reconstruction

---

# 16. Universal Reconstruction Theorem

## 16.1 Introduction

The central objective of finite-volume quantum field theory is not merely the computation of compact-space spectra but the reconstruction of the complete physical content of the underlying quantum field theory.

For two-body systems, Lüscher theory reconstructs infinite-volume scattering amplitudes from finite-volume energy levels.

For three-body systems, the Hansen–Sharpe framework extends this reconstruction to relativistic three-particle scattering.

The present section establishes the general theorem for arbitrary particle number.

---

## 16.2 Statement of the Reconstruction Problem

Suppose the complete finite-volume spectrum is known:

[
\mathcal S_L
============

{
E_n(L)
}.
]

The inverse problem asks whether one can reconstruct:

[
\mathcal M_N,
]

[
S_N,
]

[
K_N,
]

and ultimately the microscopic quantum field theory itself.

---

## 16.3 Spectral Completeness

Let

[
D_N(E,L)
========

\det
\bigl[
I-G_N(E,L)K_N(E)
\bigr].
]

Knowledge of all finite-volume energy levels determines the zero locus of

[
D_N(E,L).
]

Hence the spectrum determines the spectral determinant.

---

## 16.4 Reconstruction Operator

Define the inverse map

[
\mathcal R:
\mathcal S_L
\rightarrow
K_N.
]

The reconstruction operator extracts interaction kernels from spectral data.

Formally,

[
K_N
===

\mathcal R[\mathcal S_L].
]

---

## 16.5 Injectivity

Suppose

[
K_N^{(1)}
]

and

[
K_N^{(2)}
]

produce identical spectra for all volumes.

Then

[
D_N^{(1)}
=========

D_N^{(2)}.
]

Analytic continuation implies

[
K_N^{(1)}
=========

K_N^{(2)}.
]

Therefore the inverse map is injective.

---

## 16.6 Surjectivity

Every admissible interaction kernel defines a spectral determinant and therefore a finite-volume spectrum.

The map is therefore surjective onto the physical kernel space.

---

## 16.7 Reconstruction Hierarchy

The reconstruction proceeds recursively:

[
\mathcal S_L
\rightarrow
D_N
\rightarrow
K_N
\rightarrow
T_N
\rightarrow
S_N.
]

The hierarchy terminates at the physical scattering matrix.

---

## 16.8 Cluster Reconstruction

The partition lattice

[
\mathfrak P_N
]

permits independent reconstruction of cluster sectors.

One obtains

[
K_{\mathcal P}
]

for every partition

[
\mathcal P.
]

The full kernel is then assembled from cluster data.

---

## 16.9 Reconstruction Stability

Let

[
\delta E_n
]

represent spectral uncertainties.

Then

[
\delta K_N
==========

\mathcal O(\delta E_n).
]

The reconstruction is stable under sufficiently dense spectral sampling.

---

## 16.10 Universal Reconstruction Theorem

**Theorem.**

Given complete finite-volume spectral data for all admissible volumes,

[
{E_n(L)},
]

the full (N)-body scattering theory is uniquely reconstructible.

Specifically,

[
\boxed{
{E_n(L)}
\Longleftrightarrow
D_N(E,L)
\Longleftrightarrow
K_N(E)
\Longleftrightarrow
\mathcal M_N(E).
}
]

Finite-volume spectra therefore constitute complete physical observables.

---

# 17. Inverse Spectral Problem

## 17.1 Formulation

The inverse spectral problem seeks to determine the underlying dynamics from the observed spectrum.

The direct problem is

[
H_N
\rightarrow
{E_n}.
]

The inverse problem is

[
{E_n}
\rightarrow
H_N.
]

---

## 17.2 Spectral Data Space

Define

[
\Sigma_N
========

{
E_n(L)
}_{n,L}.
]

This infinite collection forms the complete spectral dataset.

---

## 17.3 Spectral Measures

The spectral measure is

[
d\mu_N(E)
=========

\sum_n
\delta(E-E_n).
]

Knowledge of

[
d\mu_N
]

is equivalent to knowledge of the spectrum.

---

## 17.4 Inverse Resolvent Theory

The Green function satisfies

[
G_N(E)
======

\int
\frac{d\mu_N(\lambda)}
{E-\lambda+i\epsilon}.
]

The spectral measure determines the resolvent.

---

## 17.5 Recovery of the Hamiltonian

Using the spectral theorem,

[
H_N
===

\int
\lambda
,dP(\lambda),
]

where

[
P(\lambda)
]

is the spectral projector.

The Hamiltonian is uniquely determined by the spectral measure.

---

## 17.6 Compact-Space Gel'fand Theory

The inverse problem generalizes classical Gel'fand spectral reconstruction.

Finite-volume quantum field theory may be viewed as a relativistic extension of inverse spectral geometry.

---

## 17.7 Cluster Inversion

Each partition

[
\mathcal P
]

possesses its own spectral branch.

The inverse problem decomposes into independent cluster inversions.

---

## 17.8 Resonance Reconstruction

Analytic continuation of spectral determinants yields complex poles

[
E_R
===

## M_R

i\Gamma_R/2.
]

Thus resonances are recoverable from finite-volume spectra.

---

## 17.9 Uniqueness Principle

Two self-adjoint finite-volume Hamiltonians with identical spectra for all admissible volumes must be physically equivalent.

---

## 17.10 Inverse Spectral Theorem

**Theorem.**

The complete finite-volume spectral measure uniquely determines the compact-space Hamiltonian and therefore all observable dynamics of the quantum field theory.

---

# 18. Recovery of Infinite-Volume Observables

## 18.1 Introduction

Physical experiments occur effectively in infinite volume.

The purpose of finite-volume reconstruction is therefore the recovery of infinite-volume observables.

---

## 18.2 Infinite-Volume Limit

Consider

[
L
\rightarrow
\infty.
]

The discrete spectrum approaches a continuum:

[
\sum_n
\rightarrow
\int dE,\rho(E).
]

Finite-volume eigenvalues become scattering states.

---

## 18.3 Reconstruction of Scattering Amplitudes

Once

[
K_N
]

has been reconstructed, one solves

[
T_N
===

K_N
+
K_N G_\infty T_N.
]

This yields the physical scattering amplitude.

---

## 18.4 Recovery of Cross Sections

The amplitude determines

[
\sigma_N.
]

Schematically,

[
\sigma_N
\propto
|\mathcal M_N|^2.
]

Thus measurable cross sections are recovered from finite-volume spectra.

---

## 18.5 Resonance Parameters

Pole locations determine:

[
M_R,
]

[
\Gamma_R.
]

Both quantities emerge directly from analytic continuation of reconstructed amplitudes.

---

## 18.6 Bound-State Observables

Bound-state energies satisfy

[
E_B
<
E_{\rm threshold}.
]

Wavefunctions and form factors may be extracted from residue data.

---

## 18.7 Matrix Elements

Generalized finite-volume matrix elements satisfy

[
\langle f|J|i\rangle_L.
]

The infinite-volume matrix elements are recovered through normalization corrections and spectral reconstruction.

---

## 18.8 Many-Body LSZ Reconstruction

The generalized LSZ formula yields

[
\mathcal M_N
============

\lim_{\text{on-shell}}
\prod_i
Z_i^{-1/2}
G_N^{\rm amputated}.
]

The reconstructed Green functions therefore determine all scattering amplitudes.

---

## 18.9 Complete Observable Recovery

The reconstruction hierarchy becomes

[
{E_n(L)}
\rightarrow
D_N
\rightarrow
K_N
\rightarrow
T_N
\rightarrow
\mathcal M_N
\rightarrow
\mathcal O_{\rm phys}.
]

Every observable is contained within the finite-volume spectrum.

---

## 18.10 Infinite-Volume Recovery Theorem

**Theorem.**

All infinite-volume observables of an arbitrary relativistic quantum field theory—including scattering amplitudes, resonance parameters, bound-state properties, matrix elements, and cross sections—are uniquely recoverable from complete finite-volume spectral information.

---

# Conclusions of Part V

The reconstruction program developed in this part establishes the fundamental equivalence between finite-volume spectra and physical quantum field theory.

Three major results emerge:

1. **Universal Reconstruction Theorem**

[
{E_n(L)}
\Longleftrightarrow
\mathcal M_N.
]

2. **Inverse Spectral Theorem**

[
{E_n(L)}
\Longleftrightarrow
H_N.
]

3. **Infinite-Volume Recovery Theorem**

[
{E_n(L)}
\Longrightarrow
\mathcal O_{\rm phys}.
]

Together these results complete the conceptual extraction of finite-volume quantum field theory from its origins in lattice spectroscopy. Finite volume is not merely a regulator nor a numerical device. Rather, it provides a complete spectral representation of quantum field dynamics. The entire infinite-volume theory is encoded within compact-space observables and can be reconstructed exactly through the universal spectral determinant framework.

This concludes the main development of **Volume IV — General N-Body Finite-Volume Quantum Field Theory**, establishing a unified theory of arbitrary-particle-number quantum fields in compact spatial geometries.

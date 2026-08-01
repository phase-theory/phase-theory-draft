# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume II — Two-Body Scattering and the Generalized Lüscher Framework

## Part II — Relativistic Generalizations

---

# 7. Moving Frames

## 7.1 Motivation

The original Lüscher formalism was formulated in the center-of-mass frame

[
P=0.
]

However, finite-volume spectra contain states with nonzero total momentum

[
P\neq0.
]

These moving-frame states provide additional spectral information and greatly improve amplitude reconstruction.

The extension of finite-volume scattering theory to moving frames constitutes one of the major advances in modern lattice field theory.

---

## 7.2 Quantized Total Momentum

For periodic boundary conditions,

[
P
=

\frac{2\pi}{L}d,
\qquad
d\in\mathbb Z^3.
]

The integer vector

[
d
=

(d_x,d_y,d_z)
]

labels momentum sectors.

---

## 7.3 Two-Body Kinematics

Consider particles with momenta

[
p_1,
\qquad
p_2.
]

The total momentum is

[
P=p_1+p_2.
]

The laboratory-frame energy satisfies

[
E
=

\sqrt{m_1^2+p_1^2}
+
\sqrt{m_2^2+p_2^2}.
]

---

## 7.4 Center-of-Mass Energy

Define

[
s
=

E^2-P^2.
]

The invariant center-of-mass energy becomes

[
E^\ast
======

\sqrt{s}.
]

This quantity remains unchanged by boosts.

---

## 7.5 Lorentz Factor

The finite-volume boost parameter is

[
\gamma
======

\frac{E}{E^\ast}.
]

The corresponding velocity is

[
\beta
=====

\frac{|P|}{E}.
]

---

## 7.6 Boosted Relative Momentum

The center-of-mass momentum satisfies

[
k^\ast
======

\frac{
\sqrt{
\left[s-(m_1+m_2)^2\right]
\left[s-(m_1-m_2)^2\right]
}
}
{2\sqrt{s}}.
]

This quantity replaces the rest-frame momentum appearing in ordinary Lüscher theory.

---

## 7.7 Moving-Frame Principle

Every finite-volume energy level is naturally associated with a specific momentum sector

[
P=\frac{2\pi}{L}d.
]

The full spectrum is obtained only after combining all momentum sectors simultaneously.

---

# 8. Lorentz Symmetry Breaking by Compactification

## 8.1 Infinite-Volume Symmetry

Relativistic quantum field theory possesses Poincaré invariance:

[
ISO(1,3).
]

Scattering amplitudes depend only upon Lorentz invariants.

---

## 8.2 Compactification Effects

Introducing periodic boundaries

[
x_i
\sim
x_i+L
]

selects preferred spatial directions.

The continuous Lorentz group is no longer preserved.

---

## 8.3 Residual Symmetry

The symmetry becomes

[
\mathbb R_t
\times
T^3
\times
O_h.
]

Continuous boosts are broken.

Continuous rotations are reduced to cubic rotations.

---

## 8.4 Spectral Consequences

Energy eigenvalues depend separately upon

[
E
]

and

[
P.
]

Finite-volume spectra therefore distinguish frames that would be equivalent in infinite volume.

---

## 8.5 Lorentz-Violating Corrections

Finite-volume observables satisfy

[
\mathcal O_L
============

\mathcal O_\infty
+
\Delta_L.
]

The correction

[
\Delta_L
]

contains explicit Lorentz-breaking contributions.

For massive theories,

[
\Delta_L
\sim
e^{-mL}.
]

---

## 8.6 Group-Theoretic Reduction

For

[
P=0,
]

the symmetry group is

[
O_h.
]

For moving frames, the symmetry reduces further to momentum little groups.

Examples include:

[
C_{4v},
]

[
C_{2v},
]

[
C_{3v}.
]

These replace ordinary angular momentum classification.

---

## 8.7 Emergent Lorentz Symmetry

As

[
L\rightarrow\infty,
]

the momentum lattice becomes dense.

The discrete symmetry groups converge toward

[
SO(3),
]

and eventually toward full Lorentz invariance.

---

## 8.8 Compactification Theorem

Lorentz symmetry is not fundamental in finite-volume QFT.

It emerges continuously through decompactification.

---

# 9. Relativistic Dispersion Relations

## 9.1 Free-Particle Dispersion

For a relativistic particle,

[
E^2
===

m^2+p^2.
]

This remains valid in compact space.

The distinction lies in the quantization of momentum.

---

## 9.2 Quantized Spectrum

Allowed energies satisfy

[
E_n
===

\sqrt{
m^2+
\left(
\frac{2\pi}{L}
\right)^2n^2
}.
]

The spectrum is discrete.

---

## 9.3 Interacting Dispersion Relations

Interactions modify the energy levels:

[
E_n
===

E_n^{(0)}
+
\Delta E_n.
]

The shift contains scattering information.

---

## 9.4 Relativistic Two-Body Energy

For identical particles,

[
E^\ast
======

2\sqrt{
m^2+k^{\ast2}
}.
]

The center-of-mass momentum is therefore

[
k^\ast
======

\sqrt{
\frac{E^{\ast2}}4
-----------------

m^2
}.
]

---

## 9.5 Finite-Volume Effective Dispersion

Exact spectral levels define a generalized dispersion relation

[
E_n(P,L).
]

This quantity simultaneously encodes:

* particle masses,
* interactions,
* finite-volume geometry.

---

## 9.6 Spectral Dispersion Principle

The finite-volume spectrum itself is the observable relativistic dispersion relation.

Ordinary mass-shell relations emerge only in the infinite-volume limit.

---

# 10. Boosted Quantization Conditions

## 10.1 Need for Generalization

The original Lüscher relation applies only to

[
P=0.
]

Moving frames require a modified geometric function.

---

## 10.2 Boosted Finite-Volume Geometry

The relative coordinate transforms under Lorentz contraction.

The cubic box appears distorted in the center-of-mass frame.

Consequently the zeta functions must be modified.

---

## 10.3 Rummukainen–Gottlieb Construction

For moving frames the quantization condition becomes

[
\delta_\ell(k^\ast)
+
\phi_d(q^\ast)
==============

n\pi.
]

The function

[
\phi_d
]

depends explicitly upon the momentum sector

[
d.
]

---

## 10.4 Generalized Zeta Functions

Define

[
Z_{lm}^{d}(s;q^2)
=================

\sum_{r\in P_d}
\frac{
\mathcal Y_{lm}(r)
}{
(r^2-q^2)^s
}.
]

The summation domain

[
P_d
]

incorporates boost geometry.

---

## 10.5 Matrix Quantization Condition

Including partial-wave mixing yields

[
\det
\left[
\mathcal M^{-1}(E^\ast)
+
F_d(E^\ast,L)
\right]
=======

0.

]

This is the exact relativistic finite-volume quantization condition for two-body scattering.

---

## 10.6 Coupled Irreducible Representations

Because moving-frame little groups possess fewer symmetries,

[
\ell=0
]

and

[
\ell=1
]

may mix.

More generally,

[
\ell
\leftrightarrow
\ell'
]

mixing becomes unavoidable.

---

## 10.7 Relativistic Reconstruction Formula

Given

[
E_n(L,P),
]

one determines

[
k^\ast,
]

constructs

[
F_d,
]

and solves

[
\det
\left[
\mathcal M^{-1}
+
F_d
\right]
=======

0.

]

The scattering amplitude follows directly.

---

## 10.8 Generalized Moving-Frame Theorem

All finite-volume two-body spectra, regardless of momentum sector, are determined by a universal determinant equation

[
\det
\left[
\mathcal M^{-1}
+
F_d
\right]
=======

0,
]

where

[
F_d
]

depends only on geometry and kinematics, while

[
\mathcal M
]

contains the infinite-volume dynamics.

---

# Conclusions of Part II

Relativistic finite-volume scattering theory extends far beyond the original center-of-mass formulation. Compactification breaks continuous Lorentz symmetry, replacing it with discrete momentum-sector symmetries and little groups. Nevertheless, Lorentz-invariant scattering information remains encoded within the finite-volume spectrum through the invariant center-of-mass energy

[
E^\ast=\sqrt{E^2-P^2}.
]

Moving frames dramatically increase the information content of spectral data, allowing a dense reconstruction of scattering amplitudes. The resulting boosted quantization conditions unify all momentum sectors into a single determinant framework in which geometry and dynamics are cleanly separated.

The key result of Part II is that finite-volume spectra from arbitrary moving frames obey universal relativistic quantization conditions. These relations provide the essential bridge between lattice spectra and physical scattering amplitudes and form the foundation for coupled-channel and resonance analyses developed in subsequent parts of Volume II.

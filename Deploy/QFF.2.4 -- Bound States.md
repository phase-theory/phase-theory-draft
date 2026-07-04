# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume II — Two-Body Scattering and the Generalized Lüscher Framework

## Part IV — Bound States

---

# 16. Finite-Volume Bound States

## 16.1 Introduction

Bound states occupy a unique position in finite-volume quantum field theory.

Unlike scattering states, which become dense in the infinite-volume limit, bound states remain isolated spectral objects. Their energies converge to finite values as

[
L\rightarrow\infty.
]

Examples include:

[
\pi^+\pi^-,
]

[
\text{deuteron},
]

[
J/\psi,
]

and hadronic molecules.

The purpose of this chapter is to establish the finite-volume theory of bound states from first principles.

---

## 16.2 Bound-State Pole Condition

Consider the infinite-volume scattering amplitude

[
\mathcal M(E).
]

A bound state corresponds to a pole below threshold:

[
\mathcal M(E)
\sim
\frac{g_B^2}{E_B-E}.
]

The pole position satisfies

[
E_B
<
E_{\rm th}.
]

---

## 16.3 Imaginary Momentum

For a two-body system,

[
E
=

2\sqrt{m^2-k^2}.
]

Below threshold,

[
k=i\kappa,
]

with

[
\kappa>0.
]

The wavefunction decays exponentially:

[
\psi(r)
\sim
e^{-\kappa r}.
]

---

## 16.4 Finite-Volume Quantization

The determinant condition

[
\det
\Big[
\mathcal M^{-1}
+
F_L
\Big]
=====

0
]

remains valid below threshold.

Bound states appear as isolated solutions.

---

## 16.5 Spectral Signature

Unlike scattering levels,

[
E_B(L)
]

changes only weakly with volume.

As

[
L\rightarrow\infty,
]

[
E_B(L)
\rightarrow
E_B.
]

This volume stability provides a powerful diagnostic.

---

## 16.6 Finite-Volume Pole Theorem

**Theorem.**

Every infinite-volume bound-state pole corresponds to a sequence of finite-volume energy levels converging exponentially toward the pole energy.

---

### Proof Sketch

Below threshold,

[
k=i\kappa.
]

Finite-volume corrections arise from winding trajectories around the compact volume.

Each winding contributes

[
e^{-\kappa L}.
]

Summing all windings produces exponentially suppressed corrections.

∎

---

## 16.7 Spectral Bound-State Principle

Bound states are identified through exponentially convergent finite-volume spectral trajectories.

---

# 17. Exponential Corrections

## 17.1 Origin

Finite-volume corrections to scattering states typically scale as inverse powers of volume.

Bound states behave differently.

The localization length

[
\xi
===

\kappa^{-1}
]

creates exponential suppression.

---

## 17.2 Method of Images

The finite-volume wavefunction can be written as

[
\psi_L(r)
=========

\sum_{n\in\mathbb Z^3}
\psi_\infty(r+nL).
]

The additional terms correspond to images of the bound state.

---

## 17.3 Leading Correction

For large volumes,

[
\Delta E_B(L)
=============

E_B(L)-E_B
]

satisfies

[
\Delta E_B(L)
\propto
\frac{e^{-\kappa L}}{L}.
]

This is the universal finite-volume bound-state correction.

---

## 17.4 Wrapped Propagation

Physically, the correction arises because a constituent particle may travel around the periodic volume and interact with the original bound state.

Such processes are absent in infinite volume.

---

## 17.5 General Multi-Winding Expansion

The correction admits the expansion

[
\Delta E_B(L)
=============

\sum_{n\neq0}
A_n
e^{-\kappa |n|L}.
]

The coefficients

[
A_n
]

encode internal structure.

---

## 17.6 Extraction of Binding Momentum

Measurement of

[
E_B(L)
]

at multiple volumes allows determination of

[
\kappa.
]

Hence the spatial size of the bound state can be extracted directly from finite-volume data.

---

## 17.7 Exponential Universality Theorem

All finite-volume corrections to isolated bound states are governed by the binding momentum

[
\kappa.
]

No additional long-distance scales appear.

---

# 18. Composite Particles

## 18.1 Elementary versus Composite States

Finite-volume spectra do not directly distinguish elementary particles from composites.

Both appear as discrete energy levels.

The distinction lies in their internal structure.

---

## 18.2 Composite Bound States

Consider two constituents interacting through a short-range potential.

The bound-state wavefunction satisfies

[
H\psi
=====

E_B\psi.
]

The state occupies a finite spatial region.

---

## 18.3 Compositeness Parameter

Introduce the field-renormalization factor

[
Z.
]

The probability of a composite structure is

[
X
=

1-Z.
]

For purely molecular states,

[
X\rightarrow1.
]

For elementary states,

[
X\rightarrow0.
]

---

## 18.4 Finite-Volume Diagnostics

Composite particles exhibit characteristic volume dependence:

[
E_B(L)
======

E_B
+
A
e^{-\kappa L}
+\cdots.
]

The coefficient

[
A
]

depends on the constituent wavefunction.

---

## 18.5 Weinberg Criterion

Near threshold,

[
a
=

\frac{2(1-Z)}{2-Z}
\frac1{\kappa},
]

where

[
a
]

is the scattering length.

Finite-volume measurements therefore constrain compositeness.

---

## 18.6 Spectral Structure Function

Define

[
S(L)
====

\frac{\partial E_B}{\partial L}.
]

The asymptotic behavior of

[
S(L)
]

provides a direct measure of internal size and composition.

---

## 18.7 Composite Reconstruction Principle

The internal structure of a bound state is encoded in the volume dependence of its spectral trajectory.

---

# 19. Halo States

## 19.1 Definition

Halo states are weakly bound systems whose spatial extent greatly exceeds the range of the underlying interaction.

Examples include:

* Deuteron,
* Halo nuclei,
* Hadronic molecules,
* Near-threshold exotic hadrons.

---

## 19.2 Separation of Scales

Let

[
R
]

denote the interaction range.

Halo systems satisfy

[
\kappa^{-1}
\gg
R.
]

The wavefunction extends far beyond the interaction region.

---

## 19.3 Universal Wavefunction

At large distances,

[
\psi(r)
\sim
\frac{e^{-\kappa r}}{r}.
]

This form is independent of microscopic dynamics.

---

## 19.4 Halo Effective Theory

Low-energy observables depend only upon

[
\kappa,
]

rather than detailed short-distance physics.

Finite-volume spectra become especially predictive.

---

## 19.5 Finite-Volume Sensitivity

Because

[
\kappa
]

is small,

[
e^{-\kappa L}
]

falls slowly.

Halo states therefore exhibit unusually large finite-volume effects.

This property allows precise extraction of their structure.

---

## 19.6 Universal Finite-Volume Formula

For halo systems,

[
\Delta E_B(L)
\approx
A
\frac{e^{-\kappa L}}{L}.
]

The coefficient is determined primarily by long-range physics.

---

## 19.7 Halo Radius

The root-mean-square radius satisfies

[
r_{\rm rms}
\sim
\frac1{\kappa}.
]

Thus finite-volume spectroscopy directly measures halo size.

---

## 19.8 Halo Universality Theorem

All sufficiently shallow bound states belong to a universal finite-volume class determined by the single scale

[
\kappa.
]

Microscopic dynamics become irrelevant at leading order.

---

# Conclusions of Part IV

Bound states represent the first genuinely nonperturbative sector of finite-volume quantum field theory. Unlike scattering states, they remain isolated under decompactification and are characterized by exponentially suppressed finite-volume corrections. Their spectral trajectories converge toward pole energies according to universal laws governed by the binding momentum

[
\kappa.
]

The finite-volume spectrum contains far more information than merely the existence of a bound state. Through its volume dependence one may extract binding energies, spatial sizes, compositeness fractions, constituent structure, and halo properties. Weakly bound systems are especially informative because their large spatial extent amplifies finite-volume effects and reveals universal infrared dynamics.

The central result of Part IV is that finite-volume spectroscopy provides a complete geometric probe of bound-state structure. Bound-state poles, compositeness, molecular content, and halo universality all emerge directly from the spectral dependence on compactification, reinforcing the broader theme that geometry and dynamics are inseparable within finite-volume quantum field theory.

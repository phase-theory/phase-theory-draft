# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

## Volume I — Foundations of Finite-Volume Quantum Field Theory

# Part II — Mathematical Structure

---

# 7. Compact Spatial Manifolds

## 7.1 Motivation

The conventional formulation of quantum field theory assumes spatial slices

[
\Sigma \cong \mathbb R^3.
]

In finite-volume quantum field theory the fundamental object is instead a compact Riemannian manifold

[
(\Sigma,g).
]

The spacetime manifold becomes

[
\mathcal M=\mathbb R\times\Sigma,
]

where time remains noncompact while spatial sections possess finite measure

[
\operatorname{Vol}(\Sigma)<\infty.
]

Compactification fundamentally alters the spectral structure of all differential operators and thereby modifies the foundations of quantum field theory.

---

## 7.2 Admissible Compact Geometries

A finite-volume theory may be defined on any compact manifold satisfying:

1. Smoothness.
2. Global hyperbolicity of spacetime.
3. Existence of a positive-definite spatial metric.

Examples include

### Three-Torus

[
T^3=\mathbb R^3/L\mathbb Z^3.
]

### Rectangular Torus

[
T^3(L_x,L_y,L_z).
]

### Three-Sphere

[
S^3.
]

### Lens Spaces

[
L(p,q).
]

### Compact Hyperbolic Manifolds

[
H^3/\Gamma.
]

The torus remains the most useful case because it preserves translational structure.

---

## 7.3 Geodesic Structure

The geodesic distance

[
d(x,y)
]

replaces Euclidean separation.

For

[
T^3
]

one obtains

[
d(x,y)
======

\min_{n\in\mathbb Z^3}
|x-y+nL|.
]

Thus infinitely many image points contribute to propagation.

---

## 7.4 Compactification Scale

The geometry introduces a fundamental infrared scale

[
\Lambda_V
=========

\frac{2\pi}{L}.
]

Unlike ultraviolet regulators, this scale is physical.

The finite-volume hierarchy becomes

[
m
\quad,\quad
\Lambda_V
\quad,\quad
\Lambda_{\rm UV}.
]

---

## 7.5 Geometry as a Dynamical Parameter

In finite-volume QFT the geometry itself becomes observable.

Energy levels become functions

[
E_n[g].
]

This dependence defines spectral geometry.

---

## 7.6 Compact Geometry Principle

**Principle.**

The spatial manifold is part of the dynamical specification of a quantum field theory.

The pair

[
(\mathcal L,\Sigma)
]

rather than merely

[
\mathcal L
]

defines the theory.

---

# 8. Hilbert Spaces on Compact Domains

## 8.1 Finite-Volume State Space

For compact spatial manifold

[
\Sigma,
]

the one-particle Hilbert space is

[
\mathcal H_1
============

L^2(\Sigma).
]

Because

[
\operatorname{Vol}(\Sigma)<\infty,
]

all normalizable wavefunctions satisfy

[
\int_\Sigma |\psi|^2,dV <\infty.
]

---

## 8.2 Orthonormal Eigenbasis

Let

[
\Delta
]

denote the Laplace-Beltrami operator.

Compactness implies

[
-\Delta u_n=\lambda_n u_n.
]

The eigenfunctions satisfy

[
\langle u_n,u_m\rangle=\delta_{nm}.
]

The spectrum is discrete:

[
0\le\lambda_0\le\lambda_1\le\cdots.
]

---

## 8.3 Fock Space Construction

Bosonic Fock space:

[
\mathcal F_B
============

\bigoplus_{N=0}^{\infty}
\operatorname{Sym}
(\mathcal H_1^{\otimes N}).
]

Fermionic Fock space:

[
\mathcal F_F
============

\bigoplus_{N=0}^{\infty}
\operatorname{Alt}
(\mathcal H_1^{\otimes N}).
]

No continuum momentum labels appear.

Everything is indexed by discrete spectral modes.

---

## 8.4 Vacuum Structure

The vacuum remains

[
a_n|0\rangle=0.
]

However vacuum fluctuations now depend explicitly on volume:

[
\langle0|\phi^2|0\rangle_L.
]

Finite geometry modifies the vacuum itself.

---

## 8.5 Spectral Basis Principle

The natural basis of finite-volume QFT is not momentum space but eigenmode space.

This distinction becomes crucial in interacting theories.

---

# 9. Spectral Theory of Compact Operators

## 9.1 Fundamental Theorem

Let

[
K:\mathcal H\rightarrow\mathcal H
]

be compact.

Then

[
K u_n=\mu_n u_n,
]

with

[
\mu_n\to0.
]

The spectrum is purely discrete.

---

## 9.2 Application to Field Theory

Finite-volume Hamiltonians can be represented through compact resolvents

[
(H-z)^{-1}.
]

Consequently:

**Theorem.**

Local relativistic QFT on compact spatial manifolds possesses a discrete energy spectrum.

---

## 9.3 Spectral Resolution

The Hamiltonian admits

[
H
=

\sum_n E_n |n\rangle\langle n|.
]

No branch cuts appear at finite volume.

All singular structures become poles.

---

## 9.4 Correlation Functions

Euclidean correlators satisfy

[
C(t)
====

\sum_n
Z_n e^{-E_n t}.
]

The spectral data

[
{E_n,Z_n}
]

completely determine finite-volume dynamics.

---

## 9.5 Spectral Geometry Theorem

The entire quantum field theory may be encoded in the spectral family

[
\mathcal S=
{E_n(L,\theta,g)}.
]

This family serves as the primary observable object of finite-volume physics.

---

# 10. Momentum Quantization

## 10.1 Translation Group

For a cubic torus

[
T^3,
]

periodicity requires

[
\psi(x+L\hat e_i)=\psi(x).
]

---

## 10.2 Quantized Momenta

Plane-wave solutions

[
\psi=e^{ik\cdot x}
]

obey

[
e^{ik_iL}=1.
]

Hence

[
k_i
===

\frac{2\pi n_i}{L}.
]

The momentum lattice is

[
\Gamma^*
========

\frac{2\pi}{L}
\mathbb Z^3.
]

---

## 10.3 Dispersion Relations

Free scalar energies satisfy

[
E_n
===

\sqrt{
m^2
+
\left(\frac{2\pi}{L}\right)^2
n^2}.
]

Momentum becomes countable.

---

## 10.4 Infrared Gap

The smallest nonzero momentum is

[
p_{\min}
========

\frac{2\pi}{L}.
]

Thus compactification naturally regulates infrared divergences.

---

## 10.5 Momentum Quantization Theorem

Compact translational symmetry implies that all irreducible representations are finite-volume momentum modes indexed by

[
\mathbb Z^3.
]

---

# 11. Harmonic Analysis on Tori

## 11.1 Fourier Basis

The functions

[
u_n(x)
======

\frac1{\sqrt V}
e^{i2\pi n\cdot x/L}
]

form a complete basis.

---

## 11.2 Fourier Expansion

Any field admits

[
\phi(x)
=======

\sum_n
\phi_n
u_n(x).
]

The integral transform becomes a sum.

---

## 11.3 Parseval Identity

[
\int_{T^3}
|\phi|^2
========

\sum_n |\phi_n|^2.
]

---

## 11.4 Poisson Summation

A central relation is

[
\sum_{n\in\mathbb Z^3}
f(n)
====

\sum_{m\in\mathbb Z^3}
\hat f(m).
]

This identity underlies nearly all finite-volume corrections.

---

## 11.5 Finite-Volume Propagators

The scalar propagator becomes

[
G_L(x)
======

\frac1V
\sum_k
\frac{
e^{ikx}
}
{k^2+m^2}.
]

This replaces the infinite-volume integral.

---

## 11.6 Harmonic Reconstruction Principle

Finite-volume effects arise entirely from replacing momentum integrals by spectral sums.

---

# 12. Boundary Conditions and Their Classification

## 12.1 General Form

Boundary conditions specify

[
\phi(x+L\hat e_i)
=================

B_i\phi(x).
]

The operators

[
B_i
]

define the topology experienced by the field.

---

## 12.2 Periodic Conditions

[
\phi(x+L)
=========

\phi(x).
]

Most lattice QCD calculations employ this choice.

---

## 12.3 Antiperiodic Conditions

[
\phi(x+L)
=========

-\phi(x).
]

Common for fermions.

---

## 12.4 Dirichlet Conditions

[
\phi|_{\partial\Sigma}=0.
]

---

## 12.5 Neumann Conditions

[
\partial_n\phi|_{\partial\Sigma}=0.
]

---

## 12.6 Robin Conditions

[
a\phi+b\partial_n\phi=0.
]

---

## 12.7 Classification Theorem

Self-adjoint extensions of the Laplacian are in one-to-one correspondence with admissible quantum boundary conditions.

---

# 13. Twisted and Generalized Boundary Conditions

## 13.1 Twisted Periodicity

Allow

[
\phi(x+L\hat e_i)
=================

e^{i\theta_i}
\phi(x).
]

---

## 13.2 Modified Momentum Spectrum

One obtains

[
k_i
===

\frac{2\pi n_i+\theta_i}{L}.
]

Continuous momentum interpolation becomes possible.

---

## 13.3 Flavor Twisting

For multiplets

[
\Phi
====

(\phi_1,\ldots,\phi_N),
]

the twist becomes matrix-valued:

[
\Phi(x+L)
=========

U\Phi(x).
]

---

## 13.4 Gauge Twisting

Gauge theories admit

[
A_\mu(x+L)
==========

\Omega
A_\mu
\Omega^{-1}.
]

Such conditions probe topological sectors.

---

## 13.5 Holonomy Interpretation

Twists correspond to background flat connections

[
\theta_i
========

\oint A_i dx^i.
]

Thus boundary conditions acquire geometric meaning.

---

## 13.6 Twisting Principle

Twisted compactifications enlarge finite-volume parameter space and reveal hidden dynamical information inaccessible through periodic boundaries alone.

---

# 14. Symmetry Groups in Finite Volume

## 14.1 Broken Continuous Symmetry

Infinite-volume rotational symmetry

[
SO(3)
]

is generally broken.

---

## 14.2 Cubic Symmetry

For a cubic torus:

[
SO(3)
\rightarrow
O_h.
]

Irreducible representations become

[
A_1,A_2,E,T_1,T_2.
]

---

## 14.3 Momentum Little Groups

For moving frames the relevant symmetry is the little group preserving the momentum class.

---

## 14.4 Translational Symmetry

Continuous translations become compact translations:

[
T^3.
]

The dual group is the momentum lattice.

---

## 14.5 Internal Symmetries

Gauge and flavor symmetries remain intact provided the compactification respects them.

---

## 14.6 Finite-Volume Representation Theory

Physical states organize into irreducible representations of

[
G_{\rm FV}
==========

\text{Spatial Symmetry}
\times
\text{Internal Symmetry}.
]

---

## 14.7 Symmetry Reconstruction Theorem

As

[
L\rightarrow\infty,
]

the discrete group sequence

[
O_h
]

reconstructs the continuous group

[
SO(3).
]

Thus ordinary rotational invariance emerges from finite-volume representation theory.

---

# Conclusions of Part II

The mathematical foundation of finite-volume quantum field theory rests upon four pillars:

1. Compact spatial geometry.
2. Discrete spectral Hilbert spaces.
3. Harmonic analysis on compact manifolds.
4. Boundary-condition-dependent symmetry structures.

Unlike conventional QFT, where geometry serves as a passive stage, finite-volume QFT elevates geometry to an active component of physical dynamics. The resulting theory is naturally formulated in terms of spectral data, compact group representations, and geometric response functions.

These structures prepare the ground for Part III, where quantum fields themselves will be constructed on compact manifolds and the finite-volume versions of propagators, Green functions, effective actions, and renormalization theory will be developed from first principles.

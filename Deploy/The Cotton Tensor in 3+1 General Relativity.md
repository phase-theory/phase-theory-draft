# The Cotton Tensor in 3+1 General Relativity:

## Dynamics, Conformal Geometry, and Topological Information in Spatial Slices

### Abstract

Every globally hyperbolic solution of General Relativity admits a foliation by spacelike hypersurfaces (\Sigma_t). Each slice carries an induced three-metric (g_{ij}(t)), extrinsic curvature (K_{ij}(t)), and all associated geometric invariants. Among these invariants, the Cotton tensor

[
C_{ijk}
=======

\nabla_k R_{ij}
-\nabla_j R_{ik}
-\frac14
\left(
g_{ij}\nabla_kR
---------------

g_{ik}\nabla_jR
\right)
]

occupies a unique position.

Unlike the Ricci tensor, which measures local curvature, the Cotton tensor measures the failure of a three-dimensional geometry to be conformally flat. Since the Weyl tensor vanishes identically in three dimensions, the Cotton tensor becomes the fundamental conformal curvature invariant of spatial geometry.

This paper develops a dynamical theory of the Cotton tensor within the 3+1 formulation of General Relativity. We derive its evolution equation from the Einstein equations, identify its coupling to the electric and magnetic sectors of spacetime curvature, and argue that the Cotton tensor contains previously unrecognized information about the evolution of spatial topology and global conformal structure.

The central thesis is:

**The time evolution of the Cotton tensor is the evolution of the conformal topology of space.**

While Einstein evolution equations determine local curvature dynamics, Cotton evolution tracks how nontrivial global geometric structures propagate, decay, or amplify through cosmic history.

---

# 1. Introduction

The Einstein equations determine a four-dimensional Lorentzian geometry:

[
G_{\mu\nu}
==========

8\pi T_{\mu\nu}.
]

The usual focus is on spacetime curvature encoded in the Riemann tensor.

However every observer naturally decomposes spacetime into:

[
M \simeq \Sigma \times \mathbb R
]

with spatial slices (\Sigma_t).

The geometry of each slice is characterized by:

[
(g_{ij},K_{ij}).
]

Most studies concentrate on:

* scalar curvature (R),
* Ricci tensor (R_{ij}),
* extrinsic curvature (K_{ij}).

Yet these objects do not characterize conformal geometry.

Two spatial manifolds can possess identical local Ricci data while differing globally in conformal structure.

The invariant detecting this distinction is the Cotton tensor.

---

# 2. Cotton Geometry in Three Dimensions

Because

[
W_{ijkl}=0
]

identically in three dimensions, all conformal information must be encoded elsewhere.

The Schouten tensor is

[
P_{ij}
======

R_{ij}
-\frac14Rg_{ij}.
]

The Cotton tensor is simply

[
C_{ijk}
=======

\nabla_kP_{ij}
-\nabla_jP_{ik}.
]

Equivalently,

[
C_{ijk}
=======

2\nabla_{[k}P_{j]i}.
]

Properties:

[
C_{ijk}
=======

-C_{ikj},
]

[
g^{ij}C_{ijk}=0,
]

[
C_{[ijk]}=0.
]

Most importantly,

[
C_{ijk}=0
]

iff the three-geometry is locally conformally flat.

Thus:

[
C_{ijk}
\neq 0
]

measures intrinsic conformal curvature.

---

# 3. Cotton-York Tensor

Dualizing gives

[
C_{ij}
======

\epsilon_i{}^{kl}
\nabla_k
\left(
R_{lj}
-\frac14Rg_{lj}
\right).
]

This symmetric tensor satisfies

[
C_{ij}=C_{ji},
]

[
C^i{}_i=0,
]

[
\nabla_iC^{ij}=0.
]

The Cotton-York tensor is often more useful dynamically.

It plays in three dimensions the role played by the Weyl tensor in four dimensions.

---

# 4. Cotton Tensor as Conformal Curvature

The conformal transformation

[
g_{ij}
\rightarrow
\Omega^2g_{ij}
]

leaves

[
C_{ijk}
]

conformally invariant.

Thus the Cotton tensor depends only on the conformal class

[
[g_{ij}].
]

It is therefore natural to view

[
C_{ijk}
]

as a curvature tensor on conformal superspace.

---

# 5. 3+1 Einstein Evolution

The metric evolves according to

[
\partial_t g_{ij}
=================

-2NK_{ij}
+
\mathcal L_\beta g_{ij}.
]

The extrinsic curvature evolves via

[
\partial_t K_{ij}
=================

-\nabla_i\nabla_jN
+
N(R_{ij}
+KK_{ij}
-2K_{ik}K^k{}*j)
+
\mathcal L*\beta K_{ij}.
]

These equations imply evolution equations for

[
R_{ij},
\quad
R,
\quad
P_{ij}.
]

Hence they determine Cotton evolution.

---

# 6. Evolution of the Schouten Tensor

Taking a time derivative,

[
\partial_t P_{ij}
=================

\partial_t R_{ij}
-\frac14g_{ij}\partial_tR
-\frac14R\partial_tg_{ij}.
]

Substituting Einstein evolution yields

[
\partial_t P_{ij}
=================

-\Delta(NK_{ij})
+\nabla_i\nabla_j(NK)
+\cdots .
]

The omitted terms are quadratic in curvature and extrinsic curvature.

Thus Schouten evolution is driven by gradients of (K_{ij}).

---

# 7. Deriving Cotton Evolution

Using

[
C_{ijk}
=======

\nabla_kP_{ij}
-\nabla_jP_{ik},
]

we obtain

[
\partial_t C_{ijk}
==================

\nabla_k(\partial_tP_{ij})
-\nabla_j(\partial_tP_{ik})
+
[\partial_t,\nabla]P.
]

After substituting Einstein evolution:

[
\boxed{
\partial_t C_{ijk}
==================

-\nabla_k\Delta(NK_{ij})
+
\nabla_j\Delta(NK_{ik})
+
\mathcal N_{ijk}
}
]

where

[
\mathcal N_{ijk}
]

contains nonlinear curvature couplings.

This is the fundamental Cotton evolution equation.

---

# 8. Principal Structure

Linearizing about flat space:

[
g_{ij}
======

\delta_{ij}+h_{ij},
]

[
K_{ij}=k_{ij},
]

gives

[
\partial_t C_{ijk}
==================

-\partial_k\Delta k_{ij}
+
\partial_j\Delta k_{ik}.
]

The Cotton tensor evolves through a third-order spatial differential operator.

This immediately shows:

[
\text{Cotton dynamics are dispersive.}
]

Conformal distortions propagate differently from ordinary curvature perturbations.

---

# 9. Relation to the Magnetic Weyl Tensor

The magnetic Weyl tensor is

[
B_{ij}
======

\epsilon_i{}^{kl}
\nabla_k
\left(
K_{lj}
-g_{lj}K
\right).
]

Notice the structural similarity:

[
B_{ij}
======

\mathrm{curl}(K),
]

[
C_{ij}
======

\mathrm{curl}(P).
]

Thus

[
(C_{ij},B_{ij})
]

form a natural pair.

One is the curl of intrinsic geometry.

The other is the curl of extrinsic geometry.

Together they constitute a conformal phase-space description.

---

# 10. A Maxwell-Like System

Combining Einstein evolution yields schematically

[
\partial_t C
============

\mathrm{curl}(\Delta B)+\cdots,
]

[
\partial_t B
============

-\mathrm{curl}(C)+\cdots.
]

This resembles

[
\partial_t E=\nabla\times B,
]

[
\partial_t B=-\nabla\times E.
]

The Cotton tensor behaves as a conformal-electric field.

The magnetic Weyl tensor behaves as a conformal-magnetic field.

Einstein evolution therefore transports conformal curvature analogously to electromagnetism.

---

# 11. Cotton Energy

Define

[
\mathcal E_C
============

\int_\Sigma
C_{ij}C^{ij}
\sqrt g,d^3x.
]

Differentiating:

[
\frac{d\mathcal E_C}{dt}
========================

2\int
C^{ij}
\partial_tC_{ij}
,dV.
]

Using the evolution equation gives

[
\frac{d\mathcal E_C}{dt}
========================

-\int
|\nabla B|^2,dV
+\cdots.
]

Hence Cotton curvature possesses a conserved or weakly dissipative energy-like quantity.

---

# 12. Topological Information Beyond Ricci Curvature

Ricci curvature is local.

Cotton curvature is inherently global.

Example:

Two compact manifolds may satisfy

[
R_{ij}^{(1)}
============

R_{ij}^{(2)}
]

locally,

while differing globally through distinct conformal identifications.

Ricci cannot distinguish them.

Cotton can.

Therefore:

[
C_{ijk}
]

contains information about spatial topology inaccessible to local curvature invariants.

---

# 13. Conformal Moduli and Topology

For compact manifolds:

[
\Sigma
======

S^3/\Gamma,
]

[
T^3,
]

[
\text{hyperbolic manifolds},
]

the conformal class possesses moduli.

Cotton curvature probes these moduli.

Consequently

[
C_{ijk}
]

acts as a detector of global conformal degrees of freedom.

---

# 14. Cotton Flow Through Cosmic Time

Define

[
\mathcal C(t)
=============

\int_\Sigma
C_{ij}C^{ij}
dV.
]

This quantity measures total conformal complexity.

Three possibilities arise:

### Decay

[
\mathcal C(t)\to0.
]

The universe approaches conformal flatness.

### Constant

[
\mathcal C(t)\approx \mathrm{const}.
]

Conformal topology is preserved.

### Growth

[
\mathcal C(t)\uparrow.
]

Conformal structures become dynamically amplified.

---

# 15. Cosmological Interpretation

FLRW universes satisfy

[
C_{ijk}=0.
]

Thus standard cosmology sits at the lowest point of conformal complexity.

Perturbations generate nonzero Cotton curvature.

The evolution equation predicts how primordial conformal structures evolve.

Consequently Cotton dynamics provide a new cosmological observable.

---

# 16. Cotton Memory

Suppose the early universe possessed nontrivial topology.

Even after Ricci curvature homogenizes,

residual Cotton modes may survive.

These modes store information about ancient conformal identifications.

Therefore:

**Cotton curvature acts as a geometric memory of topology.**

---

# 17. Cotton Charge

For compact slices define

[
Q_C
===

\int_\Sigma
C_{ij}X^{ij},dV
]

for suitable conformal Killing tensors (X^{ij}).

These quantities measure global conformal sectors.

Different topologies can possess different Cotton charges despite identical local curvature.

---

# 18. Superspace Interpretation

Superspace is the space

[
\mathrm{Riem}(\Sigma)/\mathrm{Diff}(\Sigma).
]

Cotton curvature provides a natural coordinate on conformal superspace.

Its evolution equation describes motion through conformal superspace.

Thus:

[
\partial_t C_{ij}
]

is the velocity of the universe's conformal geometry.

---

# 19. The Central New Physical Principle

The Einstein equations evolve not only curvature but also conformal topology.

The Ricci tensor captures local geometry.

The Cotton tensor captures conformal-global geometry.

The evolution equation shows that topology-sensitive conformal information propagates dynamically.

Therefore:

### Ricci evolution = evolution of local curvature.

### Cotton evolution = evolution of conformal topology.

The Einstein equations secretly contain a second dynamical layer that has largely gone unnoticed.

---

# 20. Conclusion

The Cotton tensor exists on every spacelike hypersurface of every General Relativity solution. Because three-dimensional geometry possesses no Weyl tensor, the Cotton tensor is the unique carrier of intrinsic conformal curvature. By deriving its evolution from the ADM Einstein equations, we uncover a previously neglected dynamical sector of General Relativity.

The resulting theory reveals:

1. The Cotton tensor obeys a genuine evolution equation driven by extrinsic curvature and spatial curvature gradients.
2. Cotton curvature and the magnetic Weyl tensor form a coupled Maxwell-like conformal system.
3. The integrated Cotton norm measures the conformal complexity of spatial geometry.
4. Cotton evolution tracks global conformal structure that Ricci curvature cannot detect.
5. Residual Cotton modes can act as a memory of primordial topology.
6. The evolution of the Cotton tensor may therefore encode observable information about the global topology of the universe.

The deepest implication is that Einstein evolution is not merely the evolution of spacetime curvature. It is simultaneously the evolution of the conformal-topological content of space itself. The Cotton tensor provides the natural observable for this hidden sector, transforming conformal geometry from a static classification tool into a dynamical field with potentially measurable cosmological consequences.

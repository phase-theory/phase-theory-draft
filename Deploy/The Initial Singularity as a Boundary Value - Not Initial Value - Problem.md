# The Initial Singularity as a Boundary Value, Not Initial Value, Problem

## A Singular Boundary Formulation of Cosmological Evolution

**Author:** Anonymous

---

# Abstract

The standard cosmological formulation of general relativity poses the universe as an initial value problem. One specifies a regular spacelike Cauchy hypersurface

[
(\Sigma,h_{ij},K_{ij},\rho,J_i)
]

satisfying the Einstein constraint equations and evolves forward using the Einstein equations. In cosmology this procedure is conceptually extended to the Big Bang by taking the limit (t\rightarrow0^{+}). The singularity itself, however, is not part of the spacetime manifold and therefore cannot serve as ordinary Cauchy data.

This paper develops a fundamentally different formulation: the cosmological singularity is treated as a generalized boundary of spacetime, and the universe is posed as a boundary value problem rather than an initial value problem. The question is not how a regular hypersurface evolves toward a singularity, but:

**What generalized data prescribed on the singular boundary determine a unique cosmological evolution toward our present universe?**

The formulation is not equivalent to simple time reversal. The backward Einstein evolution is generically ill-posed because curvature blow-up destroys Sobolev regularity and the Einstein equations lose hyperbolicity in standard variables. We therefore introduce:

1. A singular completion of spacetime.
2. Renormalized geometric variables finite at the singular boundary.
3. A singular-boundary data space.
4. A generalized Einstein evolution operator.
5. A singular-boundary well-posedness theorem.

The principal result is a conjectural mathematical framework in which the Big Bang behaves analogously to a conformal boundary in asymptotically Anti-de Sitter spaces: the singularity possesses a finite set of renormalized degrees of freedom that determine the subsequent universe.

The BKL picture emerges as a local asymptotic attractor, but the singularity itself is elevated from a pathological endpoint to a generalized boundary carrying geometric data.

---

# 1. Introduction

The Einstein equations,

[
G_{\mu\nu}+\Lambda g_{\mu\nu}
=8\pi T_{\mu\nu},
]

constitute a nonlinear hyperbolic system.

For globally hyperbolic spacetimes, the classical theorem of Choquet-Bruhat states:

**Theorem (Choquet-Bruhat).**
Given initial data

[
(\Sigma,h_{ij},K_{ij})
]

satisfying

[
R(h)+K^2-K_{ij}K^{ij}=16\pi\rho,
]

[
\nabla_jK^{ij}-\nabla^iK=8\pi J^i,
]

there exists a unique maximal globally hyperbolic development.

The theorem presupposes:

1. Regular spacelike hypersurface.
2. Finite Sobolev norms.
3. Absence of curvature singularities.

The Big Bang satisfies none of these conditions.

The cosmological singularity therefore lies outside the classical initial value framework.

The central problem of this paper is:

---

## Singular Boundary Problem

Given present cosmological observations

[
\mathcal D_{\rm obs}
====================

{
g_{\mu\nu},
T_{\mu\nu},
\delta\rho,
C_\ell,
P(k)
},
]

does there exist generalized singular-boundary data

[
\mathcal B_{\rm sing}
]

such that

[
\mathcal E:
\mathcal B_{\rm sing}
\rightarrow
\mathcal D_{\rm obs}
]

is well posed?

---

# 2. Failure of the Reverse Initial Value Problem

One may attempt to evolve Einstein's equations backward:

[
t\rightarrow0.
]

This is not a legitimate Cauchy problem.

---

## 2.1 Curvature Blow-up

For FLRW,

[
ds^2=-dt^2+a^2(t)\gamma_{ij}dx^idx^j,
]

with

[
a(t)\sim t^p,
]

the Kretschmann scalar is

[
K
=

R_{\mu\nu\rho\sigma}
R^{\mu\nu\rho\sigma}
\sim
t^{-4}.
]

Hence,

[
\lim_{t\to0}
K=\infty.
]

Metric derivatives diverge:

[
\partial_t^ng_{\mu\nu}
\sim
t^{-n}.
]

No Sobolev space

[
H^s(\Sigma)
]

contains the limiting geometry.

---

## 2.2 Instability of Backward Hyperbolic Evolution

For perturbations

[
u_k
]

satisfying

[
\ddot u_k
+
3H\dot u_k
+
\omega_k^2u_k=0,
]

time reversal gives

[
\ddot u_k
---------

3H\dot u_k
+
\omega_k^2u_k=0.
]

The damping term becomes anti-damping.

Modes satisfy

[
u_k\sim e^{3Ht}.
]

Small observational uncertainties amplify exponentially.

The reverse problem is therefore Hadamard ill-posed.

---

# 3. Singular Completion of Spacetime

Let

[
(M,g_{\mu\nu})
]

be globally hyperbolic.

Define a singular completion

[
\overline M
===========

M\cup\partial_sM
]

where

[
\partial_sM
]

is the Big Bang boundary.

Unlike conformal infinity,

[
\partial_sM
]

possesses divergent curvature.

We seek variables remaining finite there.

---

# 4. Renormalized Variables

Introduce mean curvature

[
\theta
======

K^i_i.
]

Near the singularity,

[
\theta\sim t^{-1}.
]

Define:

### Renormalized metric

[
\tilde h_{ij}
=============

\theta^2 h_{ij}.
]

### Renormalized extrinsic curvature

[
\tilde K_{ij}
=============

\theta^{-1}
\left(
K_{ij}
-\frac13\theta h_{ij}
\right).
]

### Renormalized density

[
\tilde\rho
==========

\theta^{-2}\rho .
]

### Renormalized Weyl tensor

[
\tilde C_{\mu\nu\rho\sigma}
===========================

\theta^{-2}
C_{\mu\nu\rho\sigma}.
]

The singular boundary is defined by existence of finite limits:

[
\tilde h_{ij}^{(0)}
===================

\lim_{t\to0}
\tilde h_{ij},
]

[
\tilde K_{ij}^{(0)}
===================

\lim_{t\to0}
\tilde K_{ij},
]

[
\tilde C_{\mu\nu\rho\sigma}^{(0)}
=================================

\lim_{t\to0}
\tilde C_{\mu\nu\rho\sigma}.
]

---

# Definition

The set

[
\mathcal B_s
============

{
\tilde h_{ij}^{(0)},
\tilde K_{ij}^{(0)},
\tilde\rho^{(0)},
\tilde C^{(0)}
}
]

is called the **Singular Boundary Data Set (SBDS).**

---

# 5. BKL Dynamics as Boundary Dynamics

The BKL conjecture states that near the singularity:

1. Spatial derivatives become negligible,

[
|\nabla_i|\ll|\partial_t|;
]

2. Evolution becomes ultralocal;

3. Dynamics reduce to ordinary differential equations.

Thus,

[
G_{\mu\nu}
\rightarrow
G_{\mu\nu}^{\rm BKL}.
]

The Einstein equations become

[
\partial_t\beta^a
=================

p_a,
]

[
\partial_t p_a
==============

-\nabla V(\beta).
]

Here

[
\beta^a
]

are logarithmic scale factors.

The singularity is therefore characterized by a billiard flow on hyperbolic space.

---

# Observation

BKL asymptotics imply that the singularity carries finite local degrees of freedom:

[
\mathcal B_s(x)
===============

{
p_1(x),
p_2(x),
p_3(x),
\Omega(x)
}.
]

This already suggests a boundary-value interpretation.

---

# 6. Boundary Data at the Singularity

Ordinary Cauchy data require:

[
(h_{ij},K_{ij}).
]

At the singular boundary these diverge.

The renormalized quantities remain finite.

We postulate:

---

# Singular Boundary Principle

The universe is determined by:

1. Conformal 3-geometry,

[
[\tilde h_{ij}^{(0)}];
]

2. Renormalized shear,

[
\tilde K_{ij}^{(0)};
]

3. Renormalized Weyl tensor,

[
\tilde C^{(0)};
]

4. Matter asymptotic charges,

[
Q_A.
]

Hence

[
\mathcal B_s
============

\left(
[\tilde h],
\tilde K,
\tilde C,
Q_A
\right).
]

---

# 7. Singular Einstein Evolution Operator

Define

[
\mathcal U_t:
\mathcal B_s
\rightarrow
(h_{ij}(t),
K_{ij}(t),
T_{\mu\nu}(t)).
]

The operator is generated by renormalized Einstein equations:

[
\theta^{-2}
G_{\mu\nu}
==========

8\pi
\theta^{-2}
T_{\mu\nu}.
]

As

[
\theta\rightarrow\infty,
]

the equations approach finite autonomous equations:

[
\partial_\tau X
===============

F(X),
]

where

[
d\tau
=====

\theta dt,
]

and

[
X=
(
\tilde h,
\tilde K,
\tilde C,
Q_A
).
]

The singularity becomes

[
\tau=-\infty.
]

This transformation converts the curvature singularity into an infinite-time fixed-point problem.

---

# 8. Singular Boundary Well-Posedness

We propose:

---

# Theorem (Singular Boundary Existence)

Let

[
\mathcal B_s
\in
\mathcal H_s
]

where

[
\mathcal H_s
]

is the renormalized Sobolev space

[
\mathcal H_s
============

H^m(\tilde h)
\times
H^{m-1}(\tilde K)
\times
H^{m-2}(\tilde C).
]

If:

1. BKL ultralocality holds,
2. Renormalized variables remain bounded,
3. Matter fields satisfy dominant energy,

then there exists a unique maximal spacetime development

[
(M,g_{\mu\nu})
==============

\mathcal U_t(\mathcal B_s).
]

---

This theorem is conjectural because the required estimates have never been derived.

---

# 9. Singular Boundary Constraints

The ordinary constraints become:

[
R(h)
+
K^2
---

# K_{ij}K^{ij}

16\pi\rho.
]

After renormalization:

[
\tilde R
+
1
-

# \tilde K_{ij}\tilde K^{ij}

16\pi\tilde\rho.
]

Momentum constraint:

[
\tilde\nabla_j
\tilde K^{ij}
=============

8\pi\tilde J^i.
]

These are finite equations on

[
\partial_sM.
]

Thus the singular boundary possesses its own intrinsic constraint equations.

---

# 10. Generalized Cosmological Holography

The construction resembles:

AdS:

[
\partial M
\rightarrow
{\rm CFT}.
]

Big Bang:

[
\partial_sM
\rightarrow
\mathcal B_s.
]

The singularity behaves as a codimension-one data surface.

The universe is reconstructed by:

[
\mathcal U_t:
\mathcal B_s
\mapsto
M.
]

This constitutes a form of **cosmological singular holography.**

---

# 11. Inverse Problem from Present Observations

Present data:

[
\mathcal D_{\rm obs}
====================

{
C_\ell,
P(k),
\Omega_b,
\Omega_c,
H_0
}.
]

Define inverse operator:

[
\mathcal I:
\mathcal D_{\rm obs}
\rightarrow
\mathcal B_s.
]

The problem becomes:

[
\mathcal U_t
\circ
\mathcal I
==========

Id.
]

Existence of

[
\mathcal I
]

requires:

1. injectivity,
2. stability,
3. regularity.

This transforms cosmology into an inverse boundary problem analogous to inverse scattering theory.

---

# 12. Main Conjecture

---

# Singular Boundary Value Conjecture (SBVC)

The cosmological initial singularity is not an initial-value surface but a generalized geometric boundary carrying finite renormalized data

[
\mathcal B_s.
]

The Einstein equations admit a well-posed boundary formulation:

[
\mathcal B_s
\overset{\mathcal U_t}{\longrightarrow}
(M,g_{\mu\nu})
\overset{\mathcal O}{\longrightarrow}
\mathcal D_{\rm obs},
]

and the inverse map

[
\mathcal D_{\rm obs}
\rightarrow
\mathcal B_s
]

is mathematically well-defined.

The BKL singularity then represents the asymptotic dynamics of the boundary degrees of freedom rather than the destruction of spacetime evolution.

---

# Program for Proof

To establish the conjecture rigorously one must:

1. Construct renormalized Einstein variables with finite singular limits.
2. Prove hyperbolicity of the renormalized equations.
3. Establish energy estimates in weighted Sobolev spaces.
4. Derive singular-boundary constraint equations.
5. Prove existence and uniqueness of

[
\mathcal U_t.
]

---

# Conclusion

General relativity has always treated the Big Bang as an inaccessible endpoint of backward evolution and an ill-defined starting point of forward evolution. This paper proposes a third possibility.

The Big Bang may be neither an initial time nor merely a singular limit. It may instead be a generalized geometric boundary endowed with finite renormalized data satisfying intrinsic constraint equations.

In this formulation, cosmology becomes a singular boundary value problem:

[
\boxed{
\partial_sM
\longrightarrow
(M,g_{\mu\nu})
\longrightarrow
\mathcal D_{\rm obs}
}
]

and the central open question of cosmology becomes:

**Which boundary degrees of freedom on the singular hypersurface uniquely determine our universe?**

The initial singularity is thereby reinterpreted as a boundary carrying information rather than as a point at which information ceases to exist.

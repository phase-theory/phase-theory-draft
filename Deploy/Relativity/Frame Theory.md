# Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity

**Preprint — August 2, 2026**

**Keywords:** frame theory, tetrad, vierbein, Palatini formalism, Einstein–Cartan theory, local Lorentz invariance, spin connection, torsion, frame bundle, framet, admissibility structure

---

## Abstract

Frame Theory is an extension of general relativity in which the local frame, rather than the metric alone, is taken as the fundamental dynamical object. Standard general relativity is ordinarily formulated as a metric theory: a spacetime manifold \(M\) carries a Lorentzian metric \(g_{\mu\nu}(x)\), and the Einstein field equations are written as equations for \(g_{\mu\nu}\). However, general relativity also admits an equivalent and in several respects more primitive formulation in terms of a local orthonormal frame, or tetrad,

\[
e^a{}_\mu(x),
\]

satisfying

\[
g_{\mu\nu}(x)=\eta_{ab}\,e^a{}_\mu(x)\,e^b{}_\nu(x),
\]

together with an independent Lorentz connection,

\[
\omega^{ab}{}_\mu(x)=-\omega^{ba}{}_\mu(x),
\]

which governs the parallel transport of the frame. The collection of all admissible orthonormal frames over \(M\) is the frame bundle \(FM\), a principal bundle with structure group \(SO(1,3)\), or its double cover \(\mathrm{Spin}(1,3)\) when spinorial matter is present. The local Lorentz freedom

\[
e^a{}_\mu(x)\longmapsto \Lambda^a{}_b(x)\,e^b{}_\mu(x),
\qquad
\Lambda(x)\in SO(1,3),
\]

is usually treated as a gauge redundancy to be eliminated on the way to the metric. Frame Theory instead regards this freedom as the admissibility structure of gravitation: it determines which quantities are frame-relative, which are invariant, and which subgroups become physically relevant once observers, boundary conditions, or material reference systems are specified.

The dynamical framework is the Palatini, or Einstein–Cartan, first-order formulation. The tetrad \(e^a{}_\mu\) and spin connection \(\omega^{ab}{}_\mu\) are varied independently. The gravitational action is

\[
S_{\mathrm{grav}}[e,\omega]
=
\frac{1}{16\pi G}
\int
e\,e_a{}^\mu e_b{}^\nu
R^{ab}{}_{\mu\nu}[\omega]\,
d^4x,
\qquad
e=\det(e^a{}_\mu),
\]

or, in differential-form notation,

\[
S_{\mathrm{grav}}[e,\omega]
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}\,
e^a\wedge e^b\wedge R^{cd},
\qquad
\kappa=8\pi G.
\]

The torsion two-form,

\[
T^a
=
de^a+\omega^a{}_b\wedge e^b,
\]

is not assumed to vanish. In the absence of microscopic spin, the connection equation imposes \(T^a=0\), the spin connection reduces to the Levi-Civita spin connection \(\mathring{\omega}^{ab}(e)\), and the tetrad equation reduces exactly to the Einstein field equations. In the presence of spinorial matter, torsion becomes an algebraic field determined by the spin current, yielding Einstein–Cartan theory. Frame Theory therefore contains ordinary general relativity as its torsion-free sector while exposing the local Lorentz frame structure that the metric formulation suppresses.

The central claim is:

\[
\boxed{
\text{The frame, not the metric, is fundamental.}
}
\]

General relativity is what Frame Theory becomes after the local Lorentz freedom has been fixed, quotiented, and forgotten.

---

## 1. Introduction

General relativity is conventionally presented as a theory of a Lorentzian metric \(g_{\mu\nu}\). The metric determines lengths, causal structure, volumes, and the Levi-Civita connection. The Einstein-Hilbert action,

\[
S_{\mathrm{EH}}[g]
=
\frac{1}{2\kappa}
\int
\sqrt{-g}\,R[g]\,d^4x,
\]

produces the vacuum Einstein equations,

\[
G_{\mu\nu}[g]=0,
\]

and, with matter,

\[
G_{\mu\nu}[g]=\kappa T_{\mu\nu}.
\]

This metric formulation is powerful, compact, and geometrically transparent. Yet it obscures a fact that has been clear since the work of Cartan, Weyl, Fock, Ivanenko, and later Kibble, Sciama, Trautman, and others: the metric is not the most primitive gravitational variable. The metric is a composite object built from a local frame.

At each spacetime point \(x\in M\), one may choose an orthonormal basis of the tangent space,

\[
e_a=e_a{}^\mu \partial_\mu,
\qquad
g(e_a,e_b)=\eta_{ab},
\]

or, in coframe form,

\[
e^a=e^a{}_\mu dx^\mu,
\qquad
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
\]

The tetrad \(e^a{}_\mu\) contains ten metric degrees of freedom plus six additional local Lorentz degrees of freedom. In the usual treatment, those six degrees are regarded as pure gauge. One fixes a frame, computes the metric, and discards the frame as scaffolding.

Frame Theory reverses this order of explanation. The fundamental object is not the metric but the frame bundle together with its soldering form and connection. The metric is the first and most basic Lorentz invariant constructed from the frame. The local Lorentz freedom is not a piece of disposable redundancy; it is the structural arena in which frame-relative quantities, spinorial matter, observer congruences, and admissibility conditions are defined.

The purpose of this paper is to develop Frame Theory as a complete classical field theory. Its field variables are

\[
(e^a{}_\mu,\omega^{ab}{}_\mu).
\]

Its gauge group is the local Lorentz group, or its spin cover. Its torsion-free sector is exactly general relativity. Its spin-coupled sector is Einstein–Cartan theory. Its conceptual novelty is the interpretation of local Lorentz symmetry as an admissibility structure: a rule for deciding which frame-dependent quantities may enter physical predictions and which must be quotiented out.

This interpretation is what connects Frame Theory to the notion of a **framet**. A framet is a local-frame system equipped with an admissibility group \(G\subseteq \mathrm{Spin}(1,3)\) and an invariant state subspace under \(G\). In the full theory, \(G=\mathrm{Spin}(1,3)\). In a terrestrial or laboratory setting, once a timelike observer field is chosen, the relevant admissibility group reduces to the spatial rotation group,

\[
G\simeq SU(2)\subset \mathrm{Spin}(1,3).
\]

The invariant subspace of the framet is then precisely the space of states invariant under the local frame freedom identified by Frame Theory as fundamental.

The thesis of the paper is therefore threefold:

1. **Dynamical thesis.** The fundamental gravitational variables are the tetrad \(e^a{}_\mu\) and the independent spin connection \(\omega^{ab}{}_\mu\).

2. **Equivalence thesis.** In the torsion-free sector, Frame Theory is exactly equivalent to metric general relativity.

3. **Admissibility thesis.** The local Lorentz group is not merely a redundancy to be eliminated; it is the structure that defines frame-relative quantities, physical invariants, and the admissible state spaces of framed physical systems.

---

## 2. Geometric Foundations

### 2.1 The frame bundle

Let \(M\) be a smooth, oriented, time-oriented four-manifold. In the metric formulation, one begins with a Lorentzian metric \(g_{\mu\nu}\) of signature \((-+++)\). The metric reduces the full linear frame bundle \(GL(M)\), with structure group \(GL(4,\mathbb{R})\), to the orthonormal frame bundle \(FM\), with structure group \(SO(1,3)\).

Frame Theory reverses this logical order. One begins with a principal Lorentz bundle

\[
\pi:P\to M,
\]

with structure group \(SO(1,3)\), or, when spinors are admitted, a principal spin bundle

\[
\pi:P_{\mathrm{Spin}}\to M,
\]

with structure group \(\mathrm{Spin}(1,3)\). The existence of a spin bundle requires the vanishing of the second Stiefel-Whitney class,

\[
w_2(M)=0.
\]

The metric is not presupposed. It is constructed from a soldering form.

### 2.2 The soldering form and the tetrad

The fundamental frame field is the soldering form, or tetrad,

\[
e^a=e^a{}_\mu dx^\mu,
\]

where \(a=0,1,2,3\) is an internal Lorentz index and \(\mu=0,1,2,3\) is a spacetime coordinate index. The tetrad is required to be invertible:

\[
\det(e^a{}_\mu)\neq 0.
\]

Its inverse is denoted

\[
e_a{}^\mu,
\]

and satisfies

\[
e^a{}_\mu e_a{}^\nu=\delta_\mu^\nu,
\qquad
e^a{}_\mu e_b{}^\mu=\delta^a_b.
\]

The spacetime metric is the Lorentz-invariant composite

\[
g_{\mu\nu}
=
\eta_{ab}e^a{}_\mu e^b{}_\nu,
\]

with

\[
\eta_{ab}=\operatorname{diag}(-1,+1,+1,+1).
\]

Thus the metric is not fundamental; it is the first invariant of the frame.

The determinant of the tetrad is

\[
e=\det(e^a{}_\mu)=\sqrt{-g}.
\]

The oriented volume form is

\[
\boldsymbol{\epsilon}
=
e\,d^4x
=
\frac{1}{4!}\epsilon_{abcd}e^a\wedge e^b\wedge e^c\wedge e^d.
\]

### 2.3 Local Lorentz transformations

A local Lorentz transformation is a smooth map

\[
\Lambda:M\to SO(1,3),
\]

or, in the spin cover,

\[
S:M\to \mathrm{Spin}(1,3).
\]

The tetrad transforms in the vector representation:

\[
e^a{}_\mu
\longmapsto
e'^a{}_\mu
=
\Lambda^a{}_b(x)e^b{}_\mu.
\]

The inverse tetrad transforms as

\[
e_a{}^\mu
\longmapsto
e'_a{}^\mu
=
(\Lambda^{-1})^b{}_a(x)e_b{}^\mu.
\]

The metric is invariant:

\[
g'_{\mu\nu}
=
\eta_{ab}e'^a{}_\mu e'^b{}_\nu
=
\eta_{cd}e^c{}_\mu e^d{}_\nu
=
g_{\mu\nu},
\]

because

\[
\eta_{ab}\Lambda^a{}_c\Lambda^b{}_d=\eta_{cd}.
\]

Thus the metric is the orbit invariant of the tetrad under local Lorentz transformations.

### 2.4 The spin connection

The spin connection is a Lie-algebra-valued one-form,

\[
\omega^{ab}
=
\omega^{ab}{}_\mu dx^\mu,
\]

satisfying

\[
\omega^{ab}=-\omega^{ba}.
\]

It defines the Lorentz-covariant exterior derivative acting on internal vector indices:

\[
D V^a
=
dV^a+\omega^a{}_b\wedge V^b.
\]

Under a local Lorentz transformation,

\[
\omega
\longmapsto
\omega'
=
\Lambda\omega\Lambda^{-1}
-
d\Lambda\,\Lambda^{-1},
\]

or, in components,

\[
\omega'^{ab}{}_\mu
=
\Lambda^a{}_c\Lambda^b{}_d\omega^{cd}{}_\mu
-
(\partial_\mu \Lambda^a{}_c)\Lambda^{bc}.
\]

The curvature two-form is

\[
R^{ab}
=
d\omega^{ab}
+
\omega^a{}_c\wedge \omega^{cb}.
\]

In components,

\[
R^{ab}{}_{\mu\nu}
=
2\partial_{[\mu}\omega^{ab}{}_{\nu]}
+
2\omega^a{}_{c[\mu}\omega^{cb}{}_{\nu]}.
\]

The curvature transforms covariantly:

\[
R^{ab}
\longmapsto
R'^{ab}
=
\Lambda^a{}_c\Lambda^b{}_d R^{cd}.
\]

### 2.5 Torsion

The torsion two-form is the covariant exterior derivative of the tetrad:

\[
T^a
=
De^a
=
de^a+\omega^a{}_b\wedge e^b.
\]

In components,

\[
T^a{}_{\mu\nu}
=
2\partial_{[\mu}e^a{}_{\nu]}
+
2\omega^a{}_{b[\mu}e^b{}_{\nu]}.
\]

The spacetime torsion tensor is

\[
T^\rho{}_{\mu\nu}
=
e_a{}^\rho T^a{}_{\mu\nu}.
\]

In standard metric general relativity, torsion is set to zero by assumption. In Frame Theory, torsion is a genuine field variable. Its vanishing is a consequence of the connection equation in the absence of spin current, not an a priori restriction.

### 2.6 Bianchi identities

The curvature and torsion satisfy the Cartan Bianchi identities:

\[
DT^a
=
R^a{}_b\wedge e^b,
\]

\[
DR^{ab}
=
0.
\]

In components,

\[
D_{[\mu}T^a{}_{\nu\rho]}
=
R^a{}_{b[\mu\nu}e^b{}_{\rho]},
\]

\[
D_{[\mu}R^{ab}{}_{\nu\rho]}
=
0.
\]

These identities are the geometric backbone of the conservation laws of Frame Theory.

---

## 3. The Palatini-Cartan Action

### 3.1 Gravitational action

The fundamental gravitational action of Frame Theory is the first-order Palatini action written in tetrad variables:

\[
S_{\mathrm{grav}}[e,\omega]
=
\frac{1}{2\kappa}
\int
e\,e_a{}^\mu e_b{}^\nu
R^{ab}{}_{\mu\nu}[\omega]\,
d^4x,
\]

where

\[
\kappa=8\pi G.
\]

Equivalently, in differential-form notation,

\[
S_{\mathrm{grav}}[e,\omega]
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}\,
e^a\wedge e^b\wedge R^{cd}.
\]

The relative normalization of these two expressions assumes

\[
R^{ab}
=
\frac{1}{2}R^{ab}{}_{\mu\nu}dx^\mu\wedge dx^\nu,
\]

and

\[
\epsilon_{0123}=+1.
\]

The essential point is that \(e^a{}_\mu\) and \(\omega^{ab}{}_\mu\) are independent variables. The connection is not initially assumed to be the Levi-Civita connection of the metric constructed from \(e^a{}_\mu\).

### 3.2 Independent variations

The total action is

\[
S[e,\omega,\Psi]
=
S_{\mathrm{grav}}[e,\omega]
+
S_{\mathrm{m}}[e,\omega,\Psi],
\]

where \(\Psi\) denotes matter fields. We require

\[
\delta S=0
\]

under independent variations

\[
\delta e^a{}_\mu,
\qquad
\delta \omega^{ab}{}_\mu,
\qquad
\delta \Psi.
\]

Boundary terms are assumed to vanish, or else appropriate boundary terms are added.

The matter action defines the energy-momentum three-form \(\Sigma_a\) and the spin three-form \(\sigma_{ab}\) by

\[
\delta S_{\mathrm{m}}
=
\int
\left(
\Sigma_a\wedge \delta e^a
+
\frac{1}{2}\sigma_{ab}\wedge \delta\omega^{ab}
+
\frac{\delta S_{\mathrm{m}}}{\delta\Psi}\delta\Psi
\right).
\]

The fields \(\Sigma_a\) and \(\sigma_{ab}\) are the canonical sources for the tetrad and the Lorentz connection.

---

## 4. Field Equations

### 4.1 Variation with respect to the tetrad

Varying the gravitational action with respect to \(e^a\) gives

\[
\delta_e S_{\mathrm{grav}}
=
\frac{1}{2\kappa}
\int
\epsilon_{abcd}\,
\delta e^a\wedge e^b\wedge R^{cd}.
\]

Including matter, the tetrad field equation is

\[
\frac{1}{2\kappa}
\epsilon_{abcd}\,
e^b\wedge R^{cd}
+
\Sigma_a
=
0.
\]

Equivalently,

\[
\epsilon_{abcd}\,
e^b\wedge R^{cd}
=
2\kappa\,\tau_a,
\]

where \(\tau_a=-\Sigma_a\) is the matter energy-momentum three-form.

In component form, this equation becomes

\[
G_{\mu\nu}(e,\omega)
=
\kappa T_{\mu\nu},
\]

where

\[
G_{\mu\nu}
=
R_{\mu\nu}
-
\frac{1}{2}g_{\mu\nu}R
\]

is the Einstein tensor constructed from the full connection, and \(T_{\mu\nu}\) is the matter stress-energy tensor.

In vacuum,

\[
\Sigma_a=0,
\]

and the tetrad equation reduces to

\[
\epsilon_{abcd}\,
e^b\wedge R^{cd}
=
0.
\]

This is the tetrad form of the vacuum Einstein equation.

### 4.2 Variation with respect to the connection

Varying the gravitational action with respect to \(\omega^{ab}\) gives

\[
\delta_\omega S_{\mathrm{grav}}
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}\,
e^a\wedge e^b\wedge D(\delta\omega^{cd}).
\]

Integrating by parts,

\[
\delta_\omega S_{\mathrm{grav}}
=
-\frac{1}{4\kappa}
\int
\epsilon_{abcd}\,
D(e^a\wedge e^b)
\wedge
\delta\omega^{cd}
+
\text{boundary}.
\]

Using

\[
D(e^a\wedge e^b)
=
T^a\wedge e^b
-
e^a\wedge T^b,
\]

the connection equation becomes

\[
\epsilon_{abcd}\,
e^c\wedge T^d
=
\kappa\,\sigma_{ab},
\]

up to the sign convention used in the definition of \(\sigma_{ab}\).

In vacuum, or for matter whose spin current vanishes,

\[
\sigma_{ab}=0,
\]

and therefore

\[
\epsilon_{abcd}\,
e^c\wedge T^d
=
0.
\]

Because the tetrad is invertible, this implies

\[
T^a=0.
\]

Thus the connection equation enforces vanishing torsion in the absence of spin.

### 4.3 Recovery of the Levi-Civita connection

The torsion-free condition,

\[
T^a=de^a+\omega^a{}_b\wedge e^b=0,
\]

determines the spin connection uniquely in terms of the tetrad. Denote this solution by

\[
\mathring{\omega}^{ab}(e).
\]

It is the spin connection compatible with the tetrad,

\[
\mathring{D}e^a=0,
\]

and with the Minkowski internal metric,

\[
\mathring{D}\eta_{ab}=0.
\]

It induces the Levi-Civita connection \(\mathring{\Gamma}^\rho{}_{\mu\nu}\) of the metric

\[
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
\]

Thus, in the torsion-free sector,

\[
\omega^{ab}=\mathring{\omega}^{ab}(e),
\]

and the independent connection ceases to be independent. The Palatini action reduces to the Einstein-Hilbert action:

\[
S_{\mathrm{grav}}[e,\mathring{\omega}(e)]
=
\frac{1}{2\kappa}
\int
e\,R(e)\,d^4x
=
\frac{1}{2\kappa}
\int
\sqrt{-g}\,R[g]\,d^4x.
\]

The tetrad equation then becomes the Einstein equation.

### 4.4 Component form of the connection equation

The connection equation may be written in tensor components as

\[
T^\rho{}_{\mu\nu}
+
\delta^\rho{}_\nu T^\sigma{}_{\mu\sigma}
-
\delta^\rho{}_\mu T^\sigma{}_{\nu\sigma}
=
\kappa s^\rho{}_{\mu\nu},
\]

where \(s^\rho{}_{\mu\nu}\) is the spin density of matter.

If

\[
s^\rho{}_{\mu\nu}=0,
\]

then contraction gives

\[
T^\sigma{}_{\mu\sigma}=0,
\]

and therefore

\[
T^\rho{}_{\mu\nu}=0.
\]

Thus the absence of spin implies the absence of torsion.

---

## 5. Matter Coupling and Einstein-Cartan Theory

### 5.1 Scalar fields

A scalar field \(\phi\) couples to the frame through the metric and the volume form:

\[
S_\phi
=
-\int
e
\left(
\frac{1}{2}g^{\mu\nu}\partial_\mu\phi\partial_\nu\phi
+
V(\phi)
\right)
d^4x.
\]

Since the scalar field does not couple directly to \(\omega^{ab}{}_\mu\), its spin current vanishes:

\[
\sigma_{ab}=0.
\]

Therefore scalar matter does not source torsion in the minimal Einstein-Cartan framework.

### 5.2 Electromagnetic fields

The Maxwell action is

\[
S_{\mathrm{EM}}
=
-\frac{1}{4}
\int
e\,
F_{\mu\nu}F^{\mu\nu}
d^4x.
\]

In form notation,

\[
S_{\mathrm{EM}}
=
-\frac{1}{2}
\int
F\wedge \star F.
\]

The Hodge star depends on the tetrad, so the electromagnetic field contributes to the energy-momentum three-form \(\Sigma_a\), but it carries no intrinsic Lorentz spin current in the minimal theory. Hence,

\[
\sigma_{ab}=0.
\]

Maxwell fields do not source torsion.

### 5.3 Dirac fields

Spinor fields require the spin bundle. The Dirac action in curved spacetime is

\[
S_{\mathrm{D}}
=
\int
e
\left[
\frac{i}{2}
\left(
\bar\psi\gamma^a D_a\psi
-
D_a\bar\psi\,\gamma^a\psi
\right)
-
m\bar\psi\psi
\right]
d^4x.
\]

Here

\[
D_a=e_a{}^\mu D_\mu,
\]

and the spinor covariant derivative is

\[
D_\mu\psi
=
\partial_\mu\psi
+
\frac{1}{4}\omega_{ab\mu}\gamma^{ab}\psi,
\]

with

\[
\gamma^{ab}
=
\frac{1}{2}[\gamma^a,\gamma^b].
\]

The gamma matrices satisfy

\[
\{\gamma^a,\gamma^b\}=2\eta^{ab}.
\]

The Dirac field carries a nonzero spin current. Varying the Dirac action with respect to \(\omega^{ab}\) gives a spin three-form proportional to the axial current,

\[
j_5^a
=
\bar\psi\gamma^a\gamma^5\psi.
\]

In components, one may write

\[
s_{ab}{}^\mu
=
\frac{1}{4}
\epsilon_{ab}{}^{cd}
e_c{}^\mu
j_{5d},
\]

up to conventional signs and factors.

The torsion equation then gives an algebraic relation between torsion and the axial current:

\[
T_{abc}
=
-\frac{\kappa}{4}
\epsilon_{abcd}
j_5^d.
\]

Thus torsion is completely antisymmetric:

\[
T_{abc}=T_{[abc]}.
\]

Because the torsion equation contains no derivatives of torsion, torsion does not propagate in the minimal Einstein-Cartan-Dirac theory. It is nonzero only where spinorial matter is present.

Substituting the algebraic torsion solution back into the action produces an effective four-fermion axial-axial interaction. Schematically,

\[
\mathcal{L}_{\mathrm{int}}
\sim
\kappa
\left(
\bar\psi\gamma^a\gamma^5\psi
\right)
\left(
\bar\psi\gamma_a\gamma^5\psi
\right).
\]

The precise coefficient depends on conventions, but the structural result is invariant: spin generates torsion, and torsion mediates a contact interaction among spin currents.

---

## 6. Equivalence to Metric General Relativity

We now state the central equivalence theorem.

### Theorem: Torsion-free equivalence

Let \(e^a{}_\mu\) be an invertible tetrad on a four-manifold \(M\), and let \(\omega^{ab}{}_\mu\) be an independent Lorentz connection. Suppose the matter spin current vanishes,

\[
\sigma_{ab}=0.
\]

Then the Palatini-Cartan field equations imply

\[
T^a{}_{\mu\nu}=0,
\]

so that

\[
\omega^{ab}{}_\mu=\mathring{\omega}^{ab}{}_\mu(e),
\]

and the tetrad equation reduces to

\[
G_{\mu\nu}[g]=\kappa T_{\mu\nu},
\]

where

\[
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
\]

Conversely, any solution of the metric Einstein equations lifts locally to a tetrad \(e^a{}_\mu\) and Levi-Civita spin connection \(\mathring{\omega}^{ab}(e)\) solving the Frame Theory equations.

### Proof sketch

1. The connection variation gives

   \[
   \epsilon_{abcd}e^c\wedge T^d=0.
   \]

2. Since the tetrad is invertible, the three-forms \(e^a\wedge e^b\wedge e^c\) form a basis. The above equation implies

   \[
   T^a=0.
   \]

3. The torsion-free condition determines the unique Lorentz connection compatible with the tetrad:

   \[
   \omega^{ab}=\mathring{\omega}^{ab}(e).
   \]

4. The curvature \(R^{ab}[\mathring{\omega}]\) is then the curvature of the Levi-Civita connection of \(g_{\mu\nu}\).

5. The tetrad variation becomes

   \[
   \epsilon_{abcd}e^b\wedge R^{cd}[\mathring{\omega}]
   =
   2\kappa\tau_a,
   \]

   which is equivalent to

   \[
   G_{\mu\nu}=\kappa T_{\mu\nu}.
   \]

6. Conversely, given a metric solution \(g_{\mu\nu}\), choose any local tetrad satisfying

   \[
   g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
   \]

   The Levi-Civita connection of \(g\) induces a spin connection \(\mathring{\omega}^{ab}(e)\). The pair \((e,\mathring{\omega})\) solves the Frame Theory equations.

Thus Frame Theory does not modify general relativity in the torsion-free sector. It re-expresses it in terms of the frame and exposes the local Lorentz structure that the metric formulation quotients out.

---

## 7. Local Lorentz Symmetry as Admissibility Structure

### 7.1 Gauge redundancy versus admissibility

In standard treatments, local Lorentz transformations are called gauge transformations. Two tetrads related by

\[
e'^a{}_\mu=\Lambda^a{}_b(x)e^b{}_\mu
\]

are said to represent the same physical geometry because they yield the same metric.

This is correct as far as the metric is concerned. But it is too narrow a view once spinors, observers, boundary structures, and framed measurement systems are included. The local Lorentz group is not merely a redundancy to be removed; it is the group that organizes the relation between frame-relative descriptions and invariant physical content.

Frame Theory therefore distinguishes two notions:

1. **Invariance under local Lorentz transformations.**  
   A quantity is invariant if it is unchanged by the full local Lorentz group.

2. **Admissibility under a subgroup \(G\subseteq SO(1,3)\).**  
   Once a physical setting selects a subgroup \(G\), the relevant physical states or observables may be required to be invariant under \(G\), or to transform in a specified representation of \(G\).

The metric is invariant under the full local Lorentz group. But many physically meaningful structures are not metric alone: spin frames, observer triads, laboratory axes, angular momentum decompositions, and fermionic states depend on the frame bundle.

### 7.2 Frame-relative quantities

A quantity with uncontracted internal Lorentz indices is frame-relative. For example,

\[
e^a{}_\mu,
\qquad
T^a{}_{\mu\nu},
\qquad
\omega^{ab}{}_\mu,
\qquad
\psi
\]

are frame-relative. Their transformation laws are

\[
e^a{}_\mu\mapsto \Lambda^a{}_b e^b{}_\mu,
\]

\[
T^a{}_{\mu\nu}\mapsto \Lambda^a{}_b T^b{}_{\mu\nu},
\]

\[
R^{ab}{}_{\mu\nu}\mapsto
\Lambda^a{}_c\Lambda^b{}_d R^{cd}{}_{\mu\nu},
\]

\[
\psi\mapsto S(\Lambda)\psi,
\]

where \(S(\Lambda)\in \mathrm{Spin}(1,3)\).

Frame-relative quantities are not unphysical. They are the components of geometric objects with respect to a chosen frame. Their physical use requires either contraction to invariants or specification of the admissibility group under which they are to be classified.

### 7.3 Invariant quantities

Examples of local Lorentz invariants include

\[
g_{\mu\nu}
=
\eta_{ab}e^a{}_\mu e^b{}_\nu,
\]

\[
R
=
e_a{}^\mu e_b{}^\nu R^{ab}{}_{\mu\nu},
\]

\[
T^a{}_{\mu\nu}T_a{}^{\mu\nu},
\]

\[
R^{ab}{}_{\mu\nu}R_{ab}{}^{\mu\nu},
\]

and spinor bilinears such as

\[
\bar\psi\psi,
\qquad
\bar\psi\gamma^a\psi\,\bar\psi\gamma_a\psi,
\qquad
\bar\psi\gamma^a\gamma^5\psi\,\bar\psi\gamma_a\gamma^5\psi.
\]

Nonlocal invariants include holonomies of the spin connection,

\[
\mathcal{H}[\gamma]
=
\mathcal{P}
\exp
\left(
\oint_\gamma \omega
\right),
\]

taken in a suitable representation, and Wilson-loop-type traces,

\[
W[\gamma]
=
\operatorname{Tr}
\mathcal{P}
\exp
\left(
\oint_\gamma \omega
\right).
\]

These objects depend on the frame bundle and connection, not merely on the metric.

### 7.4 The admissibility group

Let \(G\subseteq \mathrm{Spin}(1,3)\) be a subgroup selected by the physical situation. We call \(G\) the **admissibility group** of the framed system.

A state \(\Phi\) is \(G\)-admissible if it is invariant under the vertical action of \(G\):

\[
U(g)\Phi=\Phi,
\qquad
\forall g\in G.
\]

Equivalently, the physical state space is the invariant subspace

\[
\mathcal{H}_{\mathrm{phys}}^{(G)}
=
\left\{
\Phi\in\mathcal{H}
\;\middle|\;
U(g)\Phi=\Phi,\;\forall g\in G
\right\}.
\]

At the level of observables, an operator \(A\) is \(G\)-admissible if

\[
U(g)AU(g)^{-1}=A,
\qquad
\forall g\in G.
\]

Thus the admissibility group determines which frame-relative data are physically meaningful and which must be averaged, constrained, or quotiented out.

---

## 8. The Framet

### 8.1 Definition

A **framet** is a local-frame gravitational system equipped with an admissibility structure. Formally, a framet may be specified as a tuple

\[
\mathfrak{F}
=
\left(
M,
P,
G,
e,
\omega,
\mathcal{S},
\mathcal{I}_G
\right),
\]

where:

1. \(M\) is an oriented, time-oriented spacetime manifold.

2. \(P\to M\) is a principal \(\mathrm{Spin}(1,3)\) bundle, or an \(SO(1,3)\) bundle if spinors are excluded.

3. \(G\subseteq \mathrm{Spin}(1,3)\) is the admissibility group.

4. \(e^a{}_\mu\) is an invertible tetrad, or soldering form.

5. \(\omega^{ab}{}_\mu\) is a Lorentz connection.

6. \(\mathcal{S}\) is the state space of the system, classical or quantum.

7. \(\mathcal{I}_G\subseteq \mathcal{S}\) is the invariant subspace under the action of \(G\).

The physical content of the framet is carried not by arbitrary frame variables but by the \(G\)-invariant sector.

### 8.2 Full relativistic framet

For the full local Lorentz theory,

\[
G=\mathrm{Spin}(1,3).
\]

The invariant sector consists of quantities unchanged under arbitrary local Lorentz transformations. The metric,

\[
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu,
\]

is the primary invariant. Curvature scalars, torsion scalars, and properly contracted spinor bilinears are also invariant.

The full framet thus contains metric general relativity as its invariant quotient, but it retains the frame bundle and spin connection as fundamental structure.

### 8.3 Terrestrial framet and the \(SU(2)\) reduction

In a terrestrial or laboratory setting, one typically introduces a timelike observer field

\[
u^\mu,
\qquad
g_{\mu\nu}u^\mu u^\nu=-1.
\]

Choose the tetrad so that

\[
e_0{}^\mu=u^\mu.
\]

The internal timelike vector is then

\[
n^a=(1,0,0,0).
\]

The subgroup of \(\mathrm{Spin}(1,3)\) preserving \(n^a\) is

\[
\mathrm{Stab}(n^a)
\simeq
\mathrm{Spin}(3)
\simeq
SU(2).
\]

Thus the admissibility group reduces to

\[
G=SU(2).
\]

The spatial triad

\[
e^i{}_\mu,
\qquad
i=1,2,3,
\]

is defined only up to local spatial rotations:

\[
e^i{}_\mu
\mapsto
R^i{}_j(x)e^j{}_\mu,
\qquad
R(x)\in SO(3),
\]

or, in the spin cover,

\[
R(x)\in SU(2).
\]

The terrestrial framet is therefore the structure

\[
\mathfrak{F}_{\mathrm{terr}}
=
\left(
M,
P_{SU(2)},
SU(2),
e^i{}_\mu,
\omega^{ij}{}_\mu,
\mathcal{S},
\mathcal{I}_{SU(2)}
\right).
\]

Physical laboratory states must be invariant under arbitrary rotations of the local spatial triad, or else must transform in a specified representation of \(SU(2)\) with all magnetic sublevels properly accounted for.

This is the geometric meaning of the terrestrial construction developed in *Relativity Mechanics: The Framet*, §§11–13. The \(SU(2)\) used there is not an independent internal symmetry imposed by hand. It is precisely the stabilizer of a timelike frame direction inside the local Lorentz group identified by Frame Theory as fundamental.

### 8.4 Invariant subspace of the framet

Let \(U(g)\) be the representation of \(G\) on the state space \(\mathcal{S}\). The framet invariant subspace is

\[
\mathcal{I}_G
=
\left\{
\Phi\in\mathcal{S}
\;\middle|\;
U(g)\Phi=\Phi,\;\forall g\in G
\right\}.
\]

For the full theory,

\[
\mathcal{I}_{\mathrm{Spin}(1,3)}
\]

contains states invariant under arbitrary local Lorentz transformations.

For the terrestrial theory,

\[
\mathcal{I}_{SU(2)}
\]

contains states invariant under local spatial rotations of the laboratory triad.

Thus the framet invariant subspace is nothing external to general relativity. It is the invariant sector of general relativity’s own local frame gauge structure.

---

## 9. Degrees of Freedom and Constraint Structure

### 9.1 Field components

The tetrad has

\[
4\times 4=16
\]

components. The spin connection has

\[
6\times 4=24
\]

components, because \(\omega^{ab}{}_\mu\) is antisymmetric in \(a,b\).

Naively, the first-order theory has \(40\) configuration variables per spacetime point. Most are gauge or constrained.

### 9.2 Gauge freedoms

The theory has two types of gauge freedom:

1. **Spacetime diffeomorphisms**, generated by vector fields \(\xi^\mu(x)\). There are four local gauge parameters.

2. **Local Lorentz transformations**, generated by \(\lambda^{ab}(x)=-\lambda^{ba}(x)\). There are six local gauge parameters.

Together, these give ten local gauge freedoms.

### 9.3 Torsion-free reduction

In the torsion-free sector, the connection equation solves \(\omega^{ab}\) algebraically in terms of \(e^a\):

\[
\omega^{ab}=\mathring{\omega}^{ab}(e).
\]

The independent configuration variable is then the tetrad alone. The tetrad has sixteen components. Six are removed by local Lorentz gauge freedom, and four are removed by diffeomorphism freedom, leaving six configuration degrees of freedom per point before imposing the dynamical constraints.

In the Hamiltonian formulation, the physical phase space of general relativity has two propagating degrees of freedom per point, corresponding to the two polarizations of the gravitational field.

### 9.4 Hamiltonian perspective

In Ashtekar-Barbero variables, one introduces an \(SU(2)\) connection \(A_a^i\) and a densitized triad \(E^a_i\). The canonical pair satisfies

\[
\{A_a^i(x),E^b_j(y)\}
=
\kappa\gamma\,
\delta_a^b\delta^i_j\delta^3(x,y),
\]

where \(\gamma\) is the Barbero-Immirzi parameter.

The constraints are:

1. **Gauss constraint**:

   \[
   \mathcal{G}_i
   =
   D_a E^a_i
   \approx 0.
   \]

2. **Vector, or diffeomorphism, constraint**:

   \[
   \mathcal{V}_a
   =
   E^b_i F^i_{ab}
   \approx 0.
   \]

3. **Scalar, or Hamiltonian, constraint**:

   \[
   \mathcal{H}
   \approx 0.
   \]

The Gauss constraint generates local \(SU(2)\) rotations of the triad. In Frame Theory, this is the terrestrial reduction of the full local Lorentz admissibility group.

The counting is:

\[
18
\text{ phase-space variables}
-
2\times 7
\text{ first-class constraints}
=
4
\text{ physical phase-space dimensions},
\]

or two configuration degrees of freedom per point.

---

## 10. Conservation Laws and Noether Identities

### 10.1 Bianchi identities

The geometric Bianchi identities are

\[
DT^a=R^a{}_b\wedge e^b,
\]

\[
DR^{ab}=0.
\]

When the field equations hold, these imply differential identities among the matter sources.

### 10.2 Local Lorentz Noether identity

Local Lorentz invariance implies

\[
D\sigma_{ab}
+
e_{[a}\wedge \Sigma_{b]}
=
0,
\]

on shell. In components, this relates the antisymmetric part of the canonical energy-momentum tensor to the divergence of the spin current.

If the spin current vanishes, the canonical energy-momentum tensor becomes symmetric on shell, as expected in metric general relativity.

### 10.3 Diffeomorphism Noether identity

Diffeomorphism invariance gives a generalized conservation law. In the presence of torsion and spin, the covariant divergence of the stress-energy tensor is not simply zero but is balanced by spin-curvature couplings. Schematically,

\[
\nabla_\mu T^{\mu\nu}
=
\text{torsion terms}
+
\text{spin-curvature terms}.
\]

In the torsion-free limit, this reduces to the usual identity

\[
\nabla_\mu T^{\mu\nu}=0.
\]

Thus the conservation laws of general relativity are recovered as a special case of the broader Cartan-Noether structure of Frame Theory.

---

## 11. Contortion and the Decomposition of the Connection

It is useful to decompose the full spin connection into its Levi-Civita part and its contortion:

\[
\omega^{ab}
=
\mathring{\omega}^{ab}
+
K^{ab}.
\]

The contortion \(K^{ab}\) is determined by torsion:

\[
K^a{}_b
=
\omega^a{}_b-\mathring{\omega}^a{}_b.
\]

In internal components,

\[
K_{abc}
=
\frac{1}{2}
\left(
T_{abc}
+
T_{cab}
-
T_{bca}
\right),
\]

with appropriate index positions and sign conventions.

The curvature decomposes as

\[
R^{ab}(\omega)
=
R^{ab}(\mathring{\omega})
+
\mathring{D}K^{ab}
+
K^a{}_c\wedge K^{cb}.
\]

Thus the full curvature contains the ordinary Riemannian curvature plus torsional contributions.

In the Einstein-Cartan theory with minimal matter, torsion is algebraic, so \(K^{ab}\) may be eliminated in favor of the spin current. The resulting theory is general relativity plus contact spin-spin interactions.

---

## 12. Extensions of the Basic Theory

### 12.1 Holst term

One may add the Holst term,

\[
S_{\mathrm{Holst}}
=
-\frac{1}{2\kappa\gamma}
\int
e^a\wedge e^b\wedge R_{ab},
\]

where \(\gamma\) is the Barbero-Immirzi parameter.

The total action becomes

\[
S
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}e^a\wedge e^b\wedge R^{cd}
-
\frac{1}{2\kappa\gamma}
\int
e^a\wedge e^b\wedge R_{ab}
+
S_{\mathrm{m}}.
\]

In the torsion-free vacuum sector, the Holst term does not alter the Einstein equations. In the presence of fermionic torsion, it modifies the effective spin-spin interaction.

The Holst term is central in loop quantum gravity and related canonical formulations. From the standpoint of Frame Theory, it is a natural Lorentz-covariant functional of the frame and connection.

### 12.2 Nieh-Yan term

The Nieh-Yan four-form is

\[
N
=
d(e^a\wedge T_a)
=
T^a\wedge T_a
-
e^a\wedge e^b\wedge R_{ab}.
\]

It is a topological invariant on compact manifolds without boundary, up to boundary terms. Its coefficient may be related to the Immirzi parameter in quantum theory.

### 12.3 Quadratic torsion and curvature invariants

The minimal Palatini-Cartan action is linear in curvature. Consequently, torsion is nonpropagating. To obtain propagating torsion, one may add quadratic invariants such as

\[
\int
T^a\wedge \star T_a,
\]

\[
\int
R^{ab}\wedge \star R_{ab},
\]

\[
\int
R^{ab}\wedge R_{ab}.
\]

Such terms lead to Poincaré gauge theories or metric-affine extensions. Frame Theory is compatible with these extensions, but its minimal form already suffices to establish the conceptual and dynamical primacy of the frame.

---

## 13. Relation to Other Frame-Based Formulations

### 13.1 Tetrad general relativity

Standard tetrad general relativity takes the tetrad as a variable but usually imposes the Levi-Civita connection from the outset. Frame Theory instead treats the connection independently and regards the torsion-free condition as a field equation.

### 13.2 Einstein-Cartan theory

Einstein-Cartan theory is the historical first-order theory of gravity with torsion and spin. Frame Theory contains Einstein-Cartan theory as its minimal dynamical sector but adds the admissibility interpretation: the local Lorentz group is the structure defining framed physical states.

### 13.3 Teleparallel gravity

Teleparallel gravity uses a curvature-free Weitzenböck connection and attributes gravitational effects to torsion. It also uses the tetrad as a fundamental variable. Frame Theory is not committed to teleparallelism. It allows both curvature and torsion, and it regards the choice of connection as part of the dynamical and gauge structure rather than as a global gauge fixing.

### 13.4 Gauge theories of the Poincaré group

Gauge theories of translations and Lorentz rotations treat the tetrad as the gauge field of translations and the spin connection as the gauge field of Lorentz rotations. Frame Theory is closely related to this tradition, but its emphasis is not merely group-theoretic. It is concerned with the admissibility structure induced by the frame bundle on physical states and observables.

---

## 14. What Frame Theory Adds to General Relativity

Frame Theory does not replace general relativity. In the torsion-free sector, it is general relativity. Its additions are conceptual, structural, and extensional.

### 14.1 Conceptual addition

The metric is no longer the primitive object. It is the invariant shadow of the frame. The local Lorentz freedom is not discarded but interpreted as the admissibility structure of framed physics.

### 14.2 Structural addition

The fundamental arena is the principal frame bundle,

\[
P\to M,
\]

with soldering form \(e^a\) and connection \(\omega^{ab}\). This structure is necessary for spinors, for observer frames, and for a clean definition of frame-relative versus invariant quantities.

### 14.3 Dynamical addition

Torsion is not forbidden by assumption. It is governed by a field equation. In the absence of spin, torsion vanishes. In the presence of spin, torsion becomes an algebraic mediator of spin-spin contact interactions.

### 14.4 Admissibility addition

The framet formalism becomes possible. A physical system may be associated with a subgroup

\[
G\subseteq \mathrm{Spin}(1,3),
\]

and its physical states are the \(G\)-invariant states,

\[
\mathcal{I}_G
=
\left\{
\Phi
\mid
U(g)\Phi=\Phi,\;\forall g\in G
\right\}.
\]

In terrestrial physics, \(G=SU(2)\). In full relativistic physics, \(G=\mathrm{Spin}(1,3)\). In null or partially framed settings, other stabilizer subgroups may appear.

---

## 15. Interpretation of the Central Claim

The central claim of Frame Theory is:

\[
\boxed{
\text{The frame, not the metric, is fundamental.}
}
\]

This does not mean that the metric is unreal. The metric is the primary local Lorentz invariant constructed from the frame. It is the object that survives after quotienting by the full local Lorentz group.

What it means is that the metric alone is insufficient to describe the full structure of gravitational physics once spin, observers, and framed measurements are included. The frame bundle is required. The spin connection is required. The local Lorentz group is required. These are not auxiliary devices; they are the natural variables of gravitation.

General relativity, in its usual metric form, is therefore a quotient theory. It is the theory obtained from Frame Theory by imposing torsion-free dynamics and then forgetting the frame orbit over each metric.

Equivalently:

\[
\boxed{
\text{General relativity is Frame Theory after local Lorentz freedom has been fixed and forgotten.}
}
\]

---

## 16. Conclusion

Frame Theory formulates gravitation in terms of the local frame \(e^a{}_\mu\) and the spin connection \(\omega^{ab}{}_\mu\). Its action is the Palatini-Cartan action. Its field equations imply vanishing torsion in the absence of spin and reduce exactly to the Einstein equations. In the presence of spin, torsion appears as an algebraic field sourced by the spin current. The local Lorentz group, far from being a mere redundancy, is the admissibility structure that determines which frame-relative quantities may enter physical predictions.

The framet is the natural object built from this structure. It consists of a frame bundle, an admissibility group \(G\subseteq \mathrm{Spin}(1,3)\), and an invariant state subspace under \(G\). In the full theory, \(G=\mathrm{Spin}(1,3)\). In the terrestrial setting, \(G=SU(2)\), the stabilizer of a timelike observer direction. The invariant subspace of the framet is therefore grounded directly in the gauge structure of general relativity itself.

Frame Theory does not overthrow general relativity. It reveals the deeper frame structure that general relativity has always possessed.

---

# Appendix A: Conventions

Spacetime indices are Greek:

\[
\mu,\nu,\rho,\dots=0,1,2,3.
\]

Internal Lorentz indices are Latin:

\[
a,b,c,\dots=0,1,2,3.
\]

The internal metric is

\[
\eta_{ab}=\operatorname{diag}(-1,+1,+1,+1).
\]

The spacetime metric is

\[
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
\]

The determinant of the tetrad is

\[
e=\det(e^a{}_\mu)=\sqrt{-g}.
\]

The Levi-Civita symbol is normalized by

\[
\epsilon_{0123}=+1.
\]

The gravitational coupling is

\[
\kappa=8\pi G.
\]

Curvature and torsion forms are

\[
R^{ab}=d\omega^{ab}+\omega^a{}_c\wedge\omega^{cb},
\]

\[
T^a=de^a+\omega^a{}_b\wedge e^b.
\]

The Bianchi identities are

\[
DT^a=R^a{}_b\wedge e^b,
\]

\[
DR^{ab}=0.
\]

---

# Appendix B: Variation of the Palatini-Cartan Action

The gravitational action is

\[
S_{\mathrm{grav}}
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}
e^a\wedge e^b\wedge R^{cd}.
\]

Varying with respect to \(e^a\),

\[
\delta_e S_{\mathrm{grav}}
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}
\left(
\delta e^a\wedge e^b\wedge R^{cd}
+
e^a\wedge \delta e^b\wedge R^{cd}
\right).
\]

The two terms are equal after relabeling dummy indices and using antisymmetry. Hence,

\[
\delta_e S_{\mathrm{grav}}
=
\frac{1}{2\kappa}
\int
\epsilon_{abcd}
\delta e^a\wedge e^b\wedge R^{cd}.
\]

The tetrad equation is therefore

\[
\epsilon_{abcd}e^b\wedge R^{cd}
=
2\kappa\tau_a,
\]

where \(\tau_a\) is the matter energy-momentum three-form.

Varying with respect to \(\omega^{ab}\),

\[
\delta_\omega S_{\mathrm{grav}}
=
\frac{1}{4\kappa}
\int
\epsilon_{abcd}
e^a\wedge e^b\wedge D(\delta\omega^{cd}).
\]

Integrating by parts,

\[
\delta_\omega S_{\mathrm{grav}}
=
-\frac{1}{4\kappa}
\int
\epsilon_{abcd}
D(e^a\wedge e^b)
\wedge
\delta\omega^{cd}.
\]

Since

\[
D(e^a\wedge e^b)
=
T^a\wedge e^b
-
e^a\wedge T^b,
\]

the connection equation becomes

\[
\epsilon_{abcd}e^c\wedge T^d
=
\kappa\sigma_{ab},
\]

where \(\sigma_{ab}\) is the matter spin three-form.

In vacuum,

\[
\sigma_{ab}=0,
\]

so

\[
\epsilon_{abcd}e^c\wedge T^d=0.
\]

Because the tetrad is invertible, this implies

\[
T^a=0.
\]

---

# Appendix C: Torsion-Free Limit and the Levi-Civita Connection

The torsion-free condition is

\[
de^a+\omega^a{}_b\wedge e^b=0.
\]

This equation uniquely determines the spin connection \(\mathring{\omega}^{ab}(e)\). In components,

\[
\mathring{\omega}_{ab\mu}
=
e_{a\nu}\mathring{\nabla}_\mu e_b{}^\nu,
\]

where \(\mathring{\nabla}\) is the Levi-Civita covariant derivative of

\[
g_{\mu\nu}=\eta_{ab}e^a{}_\mu e^b{}_\nu.
\]

Equivalently, define the anholonomy coefficients by

\[
de^a
=
-\frac{1}{2}C^a{}_{bc}e^b\wedge e^c.
\]

Then

\[
\mathring{\omega}_{abc}
=
\frac{1}{2}
\left(
C_{abc}
+
C_{cab}
-
C_{bca}
\right).
\]

The curvature of \(\mathring{\omega}^{ab}\) is the Riemann curvature of \(g_{\mu\nu}\). Therefore, in the torsion-free sector,

\[
R^{ab}[\mathring{\omega}]
=
\frac{1}{2}
R^{ab}{}_{\mu\nu}[g]
dx^\mu\wedge dx^\nu,
\]

and the tetrad field equation becomes

\[
G_{\mu\nu}[g]=\kappa T_{\mu\nu}.
\]

---

# Appendix D: Summary of Field Equations

The fundamental variables are

\[
e^a{}_\mu,
\qquad
\omega^{ab}{}_\mu.
\]

The gravitational action is

\[
S_{\mathrm{grav}}
=
\frac{1}{16\pi G}
\int
e\,e_a{}^\mu e_b{}^\nu
R^{ab}{}_{\mu\nu}
d^4x.
\]

The torsion is

\[
T^a{}_{\mu\nu}
=
2\partial_{[\mu}e^a{}_{\nu]}
+
2\omega^a{}_{b[\mu}e^b{}_{\nu]}.
\]

The curvature is

\[
R^{ab}{}_{\mu\nu}
=
2\partial_{[\mu}\omega^{ab}{}_{\nu]}
+
2\omega^a{}_{c[\mu}\omega^{cb}{}_{\nu]}.
\]

The field equations are

\[
G_{\mu\nu}(e,\omega)
=
\kappa T_{\mu\nu},
\]

\[
T^\rho{}_{\mu\nu}
+
\delta^\rho{}_\nu T^\sigma{}_{\mu\sigma}
-
\delta^\rho{}_\mu T^\sigma{}_{\nu\sigma}
=
\kappa s^\rho{}_{\mu\nu}.
\]

If

\[
s^\rho{}_{\mu\nu}=0,
\]

then

\[
T^\rho{}_{\mu\nu}=0,
\]

and

\[
\omega^{ab}{}_\mu=\mathring{\omega}^{ab}{}_\mu(e).
\]

The theory then reduces exactly to metric general relativity.

---

# Appendix E: Framet Data

A framet is

\[
\mathfrak{F}
=
\left(
M,
P,
G,
e,
\omega,
\mathcal{S},
\mathcal{I}_G
\right).
\]

The admissibility group satisfies

\[
G\subseteq \mathrm{Spin}(1,3).
\]

The invariant subspace is

\[
\mathcal{I}_G
=
\left\{
\Phi\in\mathcal{S}
\;\middle|\;
U(g)\Phi=\Phi,\;\forall g\in G
\right\}.
\]

For full local Lorentz admissibility,

\[
G=\mathrm{Spin}(1,3).
\]

For a terrestrial observer field \(u^\mu=e_0{}^\mu\),

\[
G=\mathrm{Stab}(e_0)
\simeq
SU(2).
\]

The invariant subspace then consists of states invariant under local spatial rotations of the triad.

---

## Selected References

1. É. Cartan, *Leçons sur la géométrie des espaces de Riemann*, Gauthier-Villars, Paris.

2. A. Einstein, *The Meaning of Relativity*, Princeton University Press.

3. A. Palatini, “Deduzione invariantiva delle equazioni gravitazionali dal principio di Hamilton,” *Rendiconti del Circolo Matematico di Palermo*.

4. T. W. B. Kibble, “Lorentz invariance and the gravitational field,” *Journal of Mathematical Physics*.

5. D. W. Sciama, “The physical structure of general relativity,” *Reviews of Modern Physics*.

6. A. Trautman, “Spin and torsion in gravitation,” in *General Relativity and Gravitation*.

7. F. W. Hehl, P. von der Heyde, G. D. Kerlick, J. M. Nester, “General relativity with spin and torsion: Foundations and prospects,” *Reviews of Modern Physics*.

8. A. Ashtekar, “New variables for classical and quantum gravity,” *Physical Review Letters*.

9. G. Barbero, “Real Ashtekar variables for Lorentzian signature space-times,” *Physical Review D*.

10. C. Rovelli, *Quantum Gravity*, Cambridge University Press.

11. M. Blagojević, *Gravitation and Gauge Symmetries*, Institute of Physics Publishing.

12. Companion construction: *Relativity Mechanics: The Framet*, §§11–13.

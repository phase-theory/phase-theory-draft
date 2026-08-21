# Structural Potential Theory

**A Generative Calculus of Mathematical Structures**

---

## Abstract

We develop **Structural Potential Theory** (SPT), a generalization of classical potential theory in which scalar potentials on a base space are replaced by **structural potentials**
\[
\Pi:\mathcal S\longrightarrow \mathbb P,
\]
where \(\mathcal S\) is a space of mathematical structures and \(\mathbb P\) is a space of generative potentials. A structural potential assigns to each structure an object measuring its capacity to generate, transform, constrain, or stabilize other structures. We introduce the differential calculus of structural potentials, define the potential-gradient tensor, the capacity tensor, equilibrium manifolds, and potential flows, and derive the associated variational identities, second variation formulas, and stability criteria. The theory yields a unified analytical language for geometric analysis, optimization, network science, and complex systems. In particular, classical notions of harmonic balance, capacity, and gradient descent are lifted from scalar fields on physical domains to structure-valued generative fields on moduli spaces of mathematical objects.

**Keywords:** structural potential theory, generative potentials, capacity tensor, equilibrium manifolds, gradient flows, geometric analysis, inverse problems, spectral graph theory.

---

## 1. Introduction

Classical potential theory studies scalar potentials
\[
\phi:M\longrightarrow \mathbb R
\]
on a domain \(M\), together with operators such as the Laplacian, Dirichlet energies, Green’s functions, capacities, and harmonic measures. Its central analytic objects are equations of the form
\[
\Delta \phi = \rho,
\]
energy functionals
\[
\mathcal E(\phi)=\frac12\int_M |\nabla \phi|^2\,d\mathrm{vol},
\]
and variational principles governing equilibrium states.

Many modern mathematical structures are not naturally modeled by scalar fields on a fixed background space. Instead, one studies **spaces of structures themselves**: Riemannian metrics, graphs, algebraic operations, dynamical systems, optimization landscapes, probability kernels, neural architectures, or interaction networks. In such settings, the relevant “potential” is not a scalar value assigned to a point of a fixed manifold, but a quantity measuring the **generative capacity** of a structure: its ability to produce solutions, support flows, stabilize dynamics, encode information, or deform into other structures.

We therefore replace the classical scalar potential
\[
\phi:M\to\mathbb R
\]
by a **structural potential**
\[
\Pi:\mathcal S\to\mathbb P,
\]
where:

- \(\mathcal S\) is a space, usually a smooth infinite-dimensional manifold or stack, whose points represent mathematical structures;
- \(\mathbb P\) is a space of **generative potentials**, often a Banach or Hilbert manifold, encoding capacities, constraints, spectral data, curvature defects, residuals, or stability margins;
- \(\Pi(s)\in\mathbb P\) measures the generative potential of the structure \(s\in\mathcal S\).

The central analytic questions of Structural Potential Theory are:

1. **Potential assignment.** What is the map \(\Pi\) and what geometric information does it encode?
2. **Potential gradients.** How does the potential change under infinitesimal deformations of structure?
3. **Equilibrium manifolds.** Which structures are critical, balanced, or optimal with respect to a potential?
4. **Potential flows.** How do structures evolve under descent or ascent of structural potential?
5. **Capacity.** What is the minimal energetic cost for a class of structures to realize a target potential?

The purpose of this paper is to lay the foundations of SPT as a rigorous analytical framework. We introduce the basic differential calculus, derive the principal variational identities, define equilibrium manifolds, and formulate potential flows. We then show how the theory specializes to geometric analysis, optimization, network science, and complex systems.

---

## 2. Foundations of Structural Potential Theory

### 2.1 Structural spaces

Let \(\mathcal S\) denote a space of mathematical structures. For analytic purposes, we assume that \(\mathcal S\) is a smooth manifold modeled on a Hilbert, Banach, or Fréchet space, possibly after Sobolev completion. We write local coordinates on \(\mathcal S\) as
\[
s=(s^a)_{a\in A},
\]
where the index set \(A\) may be finite or infinite.

We equip \(\mathcal S\) with a Riemannian or weak Riemannian metric
\[
g = g_{ab}(s)\,ds^a\otimes ds^b.
\]
The metric \(g\) measures the cost of infinitesimal structural deformations. If \(v,w\in T_s\mathcal S\), their inner product is
\[
g_s(v,w)=g_{ab}(s)v^a w^b.
\]

Examples of structural spaces include:

- \(\mathcal S=\mathrm{Met}(M)\), the space of Riemannian metrics on a smooth manifold \(M\);
- \(\mathcal S=\mathcal G_n\), the space of weighted graphs on \(n\) vertices;
- \(\mathcal S=\mathcal P(\Omega)\), a space of probability measures or Markov kernels;
- \(\mathcal S=\mathbb R^d\), a parameter space in optimization;
- \(\mathcal S\) a moduli space of dynamical systems, algebras, or interaction kernels.

The tangent space \(T_s\mathcal S\) is interpreted as the space of infinitesimal deformations of the structure \(s\).

---

### 2.2 Potential spaces

Let \(\mathbb P\) be a space of generative potentials. We assume \(\mathbb P\) is a smooth manifold, often a vector space, with local coordinates
\[
p=(p^\alpha)_{\alpha\in I}.
\]
We equip \(\mathbb P\) with a metric
\[
h=h_{\alpha\beta}(p)\,dp^\alpha\otimes dp^\beta.
\]
When \(\mathbb P\) is a Hilbert space, \(h_{\alpha\beta}\) may be taken constant.

The metric \(h\) measures distances between potentials. If \(q_1,q_2\in T_p\mathbb P\), then
\[
h_p(q_1,q_2)=h_{\alpha\beta}(p)q_1^\alpha q_2^\beta.
\]

In many applications, \(\mathbb P\) carries additional structure:

- a convex cone \(\mathbb P_+\subset \mathbb P\) of positive capacities;
- a monoid or tensor operation encoding composition of potentials;
- a partial order \(p\le q\) expressing dominance of capacity;
- a distinguished origin \(0\in\mathbb P\) representing neutral or vanishing generative capacity.

For the local differential theory, however, the essential data are \((\mathbb P,h)\).

---

### 2.3 Structural potentials

A **structural potential** is a smooth map
\[
\Pi:\mathcal S\longrightarrow \mathbb P.
\]
In local coordinates,
\[
\Pi^\alpha=\Pi^\alpha(s).
\]

The value \(\Pi(s)\) is interpreted as the generative potential of the structure \(s\). Depending on context, \(\Pi(s)\) may represent:

- a curvature defect;
- a residual vector in an inverse problem;
- a spectral signature;
- a stability margin;
- an entropy-production vector;
- a capacity distribution;
- a loss or feature embedding.

The image
\[
\mathcal R_\Pi:=\Pi(\mathcal S)\subset \mathbb P
\]
is the **realizable potential set**. A central inverse problem in SPT is:

> Given a target potential \(p_0\in\mathbb P\), find \(s\in\mathcal S\) such that
> \[
> \Pi(s)=p_0.
> \]

When exact realization is impossible, one seeks critical points of an energy measuring the defect \(\Pi(s)-p_0\).

---

### 2.4 Primitive objects

The primitive objects of SPT are the following.

1. **Structural potentials**
   \[
   \Pi:\mathcal S\to\mathbb P.
   \]

2. **Potential gradients**
   \[
   D\Pi:T\mathcal S\to T\mathbb P,
   \]
   or, in tensor notation,
   \[
   J^\alpha{}_a:=\nabla_a\Pi^\alpha.
   \]

3. **Equilibrium manifolds**
   \[
   \mathcal E_{\Pi,p_0}:=\{s\in\mathcal S:\text{the structural potential is balanced relative to }p_0\}.
   \]

4. **Potential flows**
   \[
   \frac{d s}{dt}=V_\Pi(s),
   \]
   where \(V_\Pi\) is a vector field constructed from \(\Pi\), usually by gradient descent of a potential energy.

These four objects form the core of the theory.

---

## 3. Differential Calculus of Structural Potentials

### 3.1 The potential-gradient tensor

Let \(s^a\) be local coordinates on \(\mathcal S\), and \(p^\alpha\) local coordinates on \(\mathbb P\). The differential of \(\Pi\) is
\[
D\Pi_s:T_s\mathcal S\longrightarrow T_{\Pi(s)}\mathbb P.
\]
In coordinates,
\[
(D\Pi_s(v))^\alpha = J^\alpha{}_a v^a,
\]
where
\[
J^\alpha{}_a := \partial_a \Pi^\alpha
\]
in flat coordinates, or more invariantly
\[
J^\alpha{}_a := \nabla_a\Pi^\alpha
\]
when connections on \(\mathcal S\) and \(\mathbb P\) are chosen.

We call
\[
J^\alpha{}_a
\]
the **potential-gradient tensor** of \(\Pi\). It measures the first-order change of generative potential under an infinitesimal structural deformation.

If \(v=v^a\partial_a\in T_s\mathcal S\), then
\[
\delta_v \Pi^\alpha = J^\alpha{}_a v^a.
\]

---

### 3.2 The capacity tensor

The pullback of the metric \(h\) by \(\Pi\) defines a symmetric positive semidefinite tensor on \(\mathcal S\):
\[
C_{ab}:= \Pi^*h_{ab}
      = h_{\alpha\beta}(\Pi(s))\,J^\alpha{}_a J^\beta{}_b.
\]
We call \(C_{ab}\) the **capacity tensor** of the structural potential.

For \(v,w\in T_s\mathcal S\),
\[
C(v,w)=h_{\Pi(s)}\bigl(D\Pi_s(v),D\Pi_s(w)\bigr).
\]

The capacity tensor measures how distinguishable two infinitesimal structural deformations are at the level of generated potentials. If \(C\) is positive definite at \(s\), then \(\Pi\) is an immersion at \(s\), and the structure is locally identifiable from its potential. If \(C\) is degenerate, then
\[
\ker C_s = \ker D\Pi_s
\]
is the space of infinitesimal structural deformations invisible to the potential.

The operator
\[
\mathcal C := D\Pi^\dagger D\Pi:T\mathcal S\to T\mathcal S
\]
has components
\[
\mathcal C^a{}_b = g^{ac}C_{cb}.
\]
This is the **structural capacity operator**.

---

### 3.3 The adjoint potential-gradient

The adjoint of \(D\Pi\) with respect to \(g\) and \(h\) is the bundle map
\[
D\Pi^\dagger:T\mathbb P\longrightarrow T\mathcal S
\]
defined by
\[
g_s(D\Pi_s^\dagger q,v)=h_{\Pi(s)}(q,D\Pi_s v)
\]
for all \(q\in T_{\Pi(s)}\mathbb P\), \(v\in T_s\mathcal S\).

In coordinates,
\[
(D\Pi^\dagger q)^a
=
g^{ab}J^\alpha{}_b h_{\alpha\beta} q^\beta.
\]

This adjoint is fundamental. It converts a potential discrepancy into a structural deformation direction.

---

### 3.4 Structural energy functionals

Let
\[
\Phi:\mathbb P\to\mathbb R
\]
be a smooth potential-energy functional on the potential space. The associated **structural energy** is
\[
E_\Phi(s):=\Phi(\Pi(s)).
\]

Its differential is
\[
dE_\Phi
=
d\Phi\circ D\Pi.
\]
In coordinates,
\[
\partial_a E_\Phi
=
\partial_\alpha\Phi(\Pi(s))\,J^\alpha{}_a.
\]

The gradient of \(E_\Phi\) with respect to the structural metric \(g\) is
\[
(\operatorname{grad}_g E_\Phi)^a
=
g^{ab}J^\alpha{}_b\,\partial_\alpha\Phi(\Pi(s)).
\]

This vector field is the **energy-gradient field** on the space of structures.

---

### 3.5 Quadratic target potentials

The most important case is the quadratic target energy. Fix \(p_0\in\mathbb P\), and define the residual
\[
r^\alpha(s):=\Pi^\alpha(s)-p_0^\alpha.
\]
Set
\[
\Phi_{p_0}(p):=\frac12 h_{\alpha\beta}(p)(p^\alpha-p_0^\alpha)(p^\beta-p_0^\beta).
\]
Then
\[
E_{p_0}(s)
=
\frac12 h_{\alpha\beta}(\Pi(s))\,r^\alpha(s)r^\beta(s).
\]

Assuming for simplicity that \(h\) is flat, or using covariant differentiation, we obtain
\[
\partial_a E_{p_0}
=
h_{\alpha\beta}r^\alpha J^\beta{}_a.
\]
Thus
\[
(\operatorname{grad}_g E_{p_0})^a
=
g^{ab}J^\alpha{}_b h_{\alpha\beta}r^\beta.
\]
Equivalently,
\[
\operatorname{grad}_g E_{p_0}
=
D\Pi^\dagger(\Pi-p_0).
\]

The **potential-gradient field toward the target** is therefore
\[
\mathcal G_{p_0}(s)
:=
D\Pi_s^\dagger(p_0-\Pi(s))
=
-\operatorname{grad}_g E_{p_0}(s).
\]

This vector field drives the structure \(s\) toward realization of the target potential \(p_0\).

---

### 3.6 Second variation and structural Hessian

Let \(\nabla^{\mathcal S}\) and \(\nabla^{\mathbb P}\) be metric-compatible connections. The covariant derivative of the potential-gradient tensor is
\[
\nabla_b J^\alpha{}_a
=
\partial_b J^\alpha{}_a
-
\Gamma^c_{ba}J^\alpha{}_c
+
\Gamma^\alpha_{\beta\gamma}J^\beta{}_b J^\gamma{}_a.
\]

For a general energy \(E_\Phi=\Phi\circ\Pi\), the Hessian is
\[
\nabla^2 E_\Phi(v,w)
=
\nabla^2\Phi(D\Pi v,D\Pi w)
+
d\Phi\bigl(\nabla^2_{v,w}\Pi\bigr),
\]
where
\[
\nabla^2_{v,w}\Pi
=
\nabla^{\mathbb P}_v(D\Pi(w))
-
D\Pi(\nabla^{\mathcal S}_v w).
\]

For the quadratic target energy, this becomes
\[
\nabla^2 E_{p_0}(v,w)
=
h(D\Pi v,D\Pi w)
+
h(r,\nabla^2_{v,w}\Pi).
\]

In coordinates,
\[
(\nabla^2 E_{p_0})_{ab}
=
h_{\alpha\beta}J^\alpha{}_aJ^\beta{}_b
+
h_{\alpha\beta}r^\alpha\nabla_a J^\beta{}_b.
\]

At an exact realization \(\Pi(s)=p_0\), the residual vanishes and the Hessian reduces to the capacity tensor:
\[
(\nabla^2 E_{p_0})_{ab}
=
C_{ab}.
\]

This identity is fundamental: near exact realization, the local geometry of the structural energy is governed by the capacity tensor.

---

## 4. Equilibrium Manifolds

### 4.1 Normal equations

Given a target \(p_0\in\mathbb P\), define the equilibrium set
\[
\mathcal E_{\Pi,p_0}
:=
\left\{
s\in\mathcal S:
\operatorname{grad}_g E_{p_0}(s)=0
\right\}.
\]
Using the adjoint, this is
\[
\mathcal E_{\Pi,p_0}
=
\left\{
s\in\mathcal S:
D\Pi_s^\dagger(\Pi(s)-p_0)=0
\right\}.
\]

In coordinates,
\[
g^{ab}J^\alpha{}_b h_{\alpha\beta}
\bigl(\Pi^\beta-p_0^\beta\bigr)
=
0.
\]

This is the **structural normal equation**. It says that the residual potential
\[
r=\Pi(s)-p_0
\]
is \(h\)-orthogonal to the image of \(D\Pi_s\):
\[
r\perp_h \operatorname{im} D\Pi_s.
\]

Thus an equilibrium structure is one for which no infinitesimal structural deformation can reduce the quadratic potential defect to first order.

If \(\Pi(s)=p_0\), then \(s\) is an exact realization and automatically an equilibrium. However, equilibrium may also occur when \(p_0\notin\Pi(\mathcal S)\), in which case \(s\) is a best approximation in the sense of the structural energy.

---

### 4.2 Linearization of the equilibrium equation

Define the equilibrium vector field
\[
F(s):=\operatorname{grad}_g E_{p_0}(s)
=
D\Pi_s^\dagger(\Pi(s)-p_0).
\]

In coordinates,
\[
F^a
=
g^{ab}J^\alpha{}_b h_{\alpha\beta}r^\beta.
\]

Let \(v\in T_s\mathcal S\). The linearization of \(F\) is
\[
DF_s(v)^a
=
g^{ab}
\left[
(\nabla_v J^\alpha{}_b)h_{\alpha\beta}r^\beta
+
J^\alpha{}_b h_{\alpha\beta}J^\beta{}_c v^c
\right].
\]

At an exact realization \(r=0\), this simplifies to
\[
DF_s(v)^a
=
g^{ab}C_{bc}v^c.
\]
Thus
\[
DF_s = g^{-1}C.
\]

Consequently,
\[
\ker DF_s=\ker C_s=\ker D\Pi_s.
\]

This shows that infinitesimal non-uniqueness of exact realization is governed by the kernel of the potential-gradient tensor.

---

### 4.3 Regular equilibrium manifolds

We now state a regularity theorem.

**Theorem 4.1.**  
Assume \(F:\mathcal S\to T\mathcal S\) defined by
\[
F(s)=D\Pi_s^\dagger(\Pi(s)-p_0)
\]
is a smooth section and is transverse to the zero section at \(s_0\). Then \(\mathcal E_{\Pi,p_0}=F^{-1}(0)\) is a smooth submanifold of \(\mathcal S\) near \(s_0\), with tangent space
\[
T_{s_0}\mathcal E_{\Pi,p_0}
=
\ker DF_{s_0}.
\]

If moreover \(s_0\) is an exact realization, \(\Pi(s_0)=p_0\), and \(C\) has constant rank near \(s_0\), then
\[
T_{s_0}\mathcal E_{\Pi,p_0}
=
\ker D\Pi_{s_0}.
\]

**Proof.**  
Transversality of \(F\) to the zero section implies by the implicit function theorem that \(F^{-1}(0)\) is a submanifold with tangent kernel \(DF_{s_0}\). At an exact realization, \(r=0\), and we computed
\[
DF_{s_0}=g^{-1}C.
\]
Since \(g^{-1}\) is an isomorphism, \(\ker DF_{s_0}=\ker C_{s_0}\). But
\[
C_{ab}=h_{\alpha\beta}J^\alpha{}_aJ^\beta{}_b,
\]
so \(\ker C=\ker D\Pi\). ∎

---

### 4.4 Stability of equilibria

Let \(s_*\in\mathcal E_{\Pi,p_0}\). The second variation of \(E_{p_0}\) at \(s_*\) determines stability.

**Proposition 4.2.**  
If
\[
\nabla^2 E_{p_0}(s_*)
\]
is positive definite on a complement to the tangent space of the equilibrium manifold, then \(s_*\) is a local minimum of \(E_{p_0}\) modulo equilibrium degeneracies. If it is positive definite on all of \(T_{s_*}\mathcal S\), then \(s_*\) is an isolated strict local minimum.

At an exact realization \(r=0\),
\[
\nabla^2 E_{p_0}(s_*)=C_{s_*}.
\]
Hence local stability of exact realization is governed by the positive definiteness of the capacity tensor.

---

## 5. Potential Flows

### 5.1 Gradient potential flow

The fundamental potential flow is the negative gradient flow of the structural energy:
\[
\frac{ds}{dt}
=
-\operatorname{grad}_g E_{p_0}(s).
\]

For the quadratic target energy,
\[
\frac{ds^a}{dt}
=
-
g^{ab}J^\alpha{}_b h_{\alpha\beta}
\bigl(\Pi^\beta-p_0^\beta\bigr).
\]

Equivalently,
\[
\frac{ds}{dt}
=
D\Pi^\dagger(p_0-\Pi(s)).
\]

This is the **structural potential flow toward \(p_0\)**.

---

### 5.2 Energy dissipation identity

Let \(s(t)\) solve the gradient flow. Then
\[
\frac{d}{dt}E_{p_0}(s(t))
=
g\bigl(\operatorname{grad}_g E_{p_0},\dot s\bigr)
=
-\|\operatorname{grad}_g E_{p_0}\|_g^2.
\]

Thus
\[
\boxed{
\frac{d}{dt}E_{p_0}(s(t))
=
-\|\operatorname{grad}_g E_{p_0}(s(t))\|_g^2
\le 0.
}
\]

The energy is a Lyapunov function for the flow.

---

### 5.3 Residual dynamics in potential space

Let
\[
r(t)=\Pi(s(t))-p_0.
\]
Differentiating,
\[
\frac{dr^\alpha}{dt}
=
J^\alpha{}_a\frac{ds^a}{dt}.
\]
Using the gradient flow,
\[
\frac{dr^\alpha}{dt}
=
-
J^\alpha{}_a g^{ab}J^\beta{}_b h_{\beta\gamma}r^\gamma.
\]
Define the potential-space operator
\[
P^\alpha{}_\gamma
:=
J^\alpha{}_a g^{ab}J^\beta{}_b h_{\beta\gamma}.
\]
Then
\[
\frac{dr}{dt}
=
-P r.
\]

When \(D\Pi^\dagger\) is interpreted as the Moore–Penrose adjoint, \(P\) is the \(h\)-orthogonal projection onto the infinitesimally realizable subspace
\[
\operatorname{im}D\Pi_s\subset T_{\Pi(s)}\mathbb P.
\]
Thus the flow eliminates the component of the residual lying in the infinitesimal image of the structural potential, while leaving invariant the component orthogonal to all infinitesimally realizable directions.

The residual energy satisfies
\[
\frac{d}{dt}\frac12\|r\|_h^2
=
-h(r,Pr)
=
-\|Pr\|_h^2.
\]

This identity provides a precise sense in which potential flow performs maximal local reduction of realizable defect.

---

### 5.4 Constrained potential flows

Often structures must satisfy constraints
\[
C^I(s)=0,\qquad I=1,\dots,m.
\]
We define the constrained gradient flow by
\[
\frac{ds^a}{dt}
=
-\operatorname{grad}_g E_{p_0}^a
-
\lambda_I g^{ab}\partial_b C^I,
\]
where the multipliers \(\lambda_I\) are chosen so that
\[
\frac{d}{dt}C^I(s(t))=0.
\]

Differentiating the constraints gives
\[
0
=
\partial_a C^I \frac{ds^a}{dt}
=
-\partial_a C^I\operatorname{grad}_g E_{p_0}^a
-
\lambda_J \partial_a C^I g^{ab}\partial_b C^J.
\]
Define the constraint Gram matrix
\[
A^{IJ}:=
\partial_a C^I g^{ab}\partial_b C^J.
\]
If \(A^{IJ}\) is invertible, then
\[
\lambda_I
=
-(A^{-1})_{IJ}
\partial_a C^J\operatorname{grad}_g E_{p_0}^a.
\]

This gives the orthogonal projection of the unconstrained potential flow onto the constraint manifold.

---

### 5.5 Long-time behavior

A standard convergence principle follows from the energy identity.

**Proposition 5.1.**  
Assume:

1. \(E_{p_0}\) is bounded below;
2. the gradient flow exists for all \(t\ge 0\);
3. \(\operatorname{grad}_g E_{p_0}\) is precompact along the trajectory.

Then
\[
\int_0^\infty \|\operatorname{grad}_g E_{p_0}(s(t))\|_g^2\,dt
<
\infty.
\]
Every limit point of \(s(t)\) as \(t\to\infty\) belongs to \(\mathcal E_{\Pi,p_0}\).

If the equilibrium manifold is discrete and the energy satisfies a local Łojasiewicz–Simon inequality, then the trajectory converges to a single equilibrium.

---

## 6. Structural Field Equations

### 6.1 Forced equilibrium equations

Classical potential theory studies equations of the form
\[
-\Delta \phi = \rho.
\]
In SPT, the analogue is a forced structural equilibrium equation.

Let \(Y\in \Gamma(T\mathcal S)\) be a structural source or forcing field. The forced equilibrium equation is
\[
D\Pi_s^\dagger(\Pi(s)-p_0)=Y(s).
\]

In weak form, for all \(v\in T_s\mathcal S\),
\[
h_{\Pi(s)}(\Pi(s)-p_0,D\Pi_s v)
=
g_s(Y(s),v).
\]

When \(Y=0\), one recovers the unforced equilibrium equation.

---

### 6.2 Structural Laplacians

Let \(p:\mathcal S\to\mathbb P\) be a smooth potential field. Its covariant Hessian is
\[
\nabla^2 p
\in
\Gamma(T^*\mathcal S\otimes T^*\mathcal S\otimes \Pi^*T\mathbb P).
\]
The structural Laplacian is the trace
\[
\Delta_{\mathcal S}p
:=
\operatorname{tr}_g \nabla^2 p.
\]

In coordinates,
\[
(\Delta_{\mathcal S}p)^\alpha
=
g^{ab}
\left(
\partial_a\partial_b p^\alpha
-
\Gamma^c_{ab}\partial_c p^\alpha
+
\Gamma^\alpha_{\beta\gamma}
\partial_a p^\beta \partial_b p^\gamma
\right).
\]

A structural Poisson equation may be written as
\[
-\Delta_{\mathcal S}p^\alpha
+
V^\alpha{}_\beta p^\beta
=
J^\alpha,
\]
where \(J\) is a source term and \(V\) is a potential interaction tensor.

This equation is not merely a scalar Laplace equation lifted to a vector bundle; it is a field equation on the space of structures. Its solutions describe how generative potentials diffuse, equilibrate, or respond to sources over the structural space.

---

### 6.3 Structural capacity

Classical capacity measures the energetic cost of enforcing boundary values of a scalar potential. In SPT, we define capacity in two related ways.

First, for a subset \(\mathcal K\subset\mathcal S\) and a target potential \(p_0\), define the **realization capacity**
\[
\operatorname{Cap}_\Pi(\mathcal K;p_0)
:=
\inf_{s\in\mathcal K}
\frac12\|\Pi(s)-p_0\|_h^2.
\]
This is the minimal energetic defect required for structures in \(\mathcal K\) to approximate \(p_0\).

Second, if one considers potential fields \(p:\mathcal S\to\mathbb P\) satisfying boundary conditions \(p|_{\partial\Omega}=p_\partial\), define the Dirichlet structural capacity
\[
\operatorname{Cap}_D(\Omega,p_\partial)
:=
\inf_{p}
\int_\Omega
\frac12\|\nabla p\|_{g,h}^2\,d\mathrm{vol}_g,
\]
where the infimum is taken over admissible fields with the prescribed boundary value. This is the direct structural analogue of classical electrostatic capacity.

---

## 7. Functorial Formulation

Although the differential formulation is sufficient for most analytic purposes, SPT admits a categorical refinement.

Let \(\mathbf{Str}\) be a category whose objects are structures and whose morphisms are structure-preserving transformations. Let \(\mathbf{Pot}\) be a category whose objects are generative potentials and whose morphisms encode transformations of capacity.

A structural potential is a functor
\[
\Pi:\mathbf{Str}\longrightarrow \mathbf{Pot}.
\]
For a morphism \(f:s\to s'\) of structures, the functor assigns a morphism
\[
\Pi(f):\Pi(s)\to\Pi(s')
\]
of potentials.

A **natural equivalence** of structural potentials corresponds to a change of potential coordinates preserving all generative relations. A **potential flow** may be viewed as a one-parameter family of endomorphisms
\[
T_t:\mathbf{Str}\to\mathbf{Str}
\]
such that \(\Pi(T_t(s))\) evolves by contraction toward a target object in \(\mathbf{Pot}\).

This functorial viewpoint is useful when the objects of interest are not manifolds but categories of algebraic, logical, or computational structures.

---

## 8. Applications

We now show how SPT specializes to several central mathematical domains.

---

## 8.1 Geometric analysis

Let \(M\) be a compact smooth manifold, and let
\[
\mathcal S=\mathrm{Met}(M)
\]
be the space of Riemannian metrics on \(M\). A point \(g\in\mathcal S\) is a metric tensor \(g_{ij}\).

Define a structural potential by the Einstein defect
\[
\Pi(g):=\operatorname{Ric}(g)-\lambda g,
\]
where \(\lambda\in\mathbb R\) is fixed. The target is
\[
p_0=0.
\]
Exact realizations satisfy
\[
\operatorname{Ric}(g)=\lambda g,
\]
i.e. \(g\) is an Einstein metric.

Equip \(\mathrm{Met}(M)\) with the \(L^2\) metric
\[
\|h\|_g^2
=
\int_M
h_{ij}h_{kl}g^{ik}g^{jl}\,d\mathrm{vol}_g.
\]

The structural energy is
\[
E(g)
=
\frac12
\int_M
\left|
\operatorname{Ric}(g)-\lambda g
\right|_g^2
d\mathrm{vol}_g.
\]

Let \(D\Pi_g\) denote the linearization of the Ricci tensor at \(g\). The gradient flow is
\[
\frac{\partial g}{\partial t}
=
-(D\Pi_g)^*\Pi(g),
\]
where \((D\Pi_g)^*\) is the \(L^2\)-adjoint of the linearized Ricci operator.

In index notation,
\[
\frac{\partial g_{ij}}{\partial t}
=
-
\bigl((D\Pi_g)^*\Pi(g)\bigr)_{ij}.
\]

This is a higher-order geometric flow driven by the structural potential. Its equilibria include Einstein metrics and, more generally, critical metrics of the squared Einstein-defect functional.

The capacity tensor on \(\mathrm{Met}(M)\) is
\[
C_g(h,k)
=
\int_M
\left\langle D\Pi_g(h),D\Pi_g(k)\right\rangle_g
d\mathrm{vol}_g.
\]
It measures the infinitesimal sensitivity of the curvature defect to metric deformations.

If instead one chooses the first-order flow
\[
\frac{\partial g}{\partial t}
=
-2\Pi(g)
=
-2(\operatorname{Ric}(g)-\lambda g),
\]
one obtains a Ricci-type potential flow. Thus classical and generalized geometric flows can be interpreted as potential flows in SPT.

---

## 8.2 Optimization

Let \(\Theta\) be a parameter manifold with coordinates \(\theta^a\). Suppose an optimization problem is represented by a residual map
\[
r:\Theta\to\mathbb R^m,
\]
with components \(r^\alpha(\theta)\). Set
\[
\mathcal S=\Theta,
\qquad
\mathbb P=\mathbb R^m,
\qquad
\Pi(\theta)=r(\theta).
\]

The quadratic structural energy is
\[
E(\theta)
=
\frac12
\sum_{\alpha=1}^m
r^\alpha(\theta)^2.
\]

The potential-gradient tensor is the Jacobian
\[
J^\alpha{}_a
=
\partial_a r^\alpha.
\]

The capacity tensor is
\[
C_{ab}
=
\sum_\alpha
\partial_a r^\alpha \partial_b r^\alpha
=
J^T J.
\]

The equilibrium equation is
\[
J^T r=0,
\]
the classical normal equation for nonlinear least squares.

If \(g_{ab}\) is a metric on parameter space, the potential flow is
\[
\frac{d\theta^a}{dt}
=
-
g^{ab}J^\alpha{}_b r^\alpha.
\]

When \(g_{ab}=\delta_{ab}\), this is ordinary gradient descent. When \(g\) is the Fisher information metric, this is natural gradient descent. When \(g=C=J^TJ\), one obtains a Gauss–Newton-type flow in which the parameter update is shaped by the local capacity tensor.

At a solution \(r=0\), the Hessian is
\[
\nabla^2E
=
J^T J,
\]
so local convexity and identifiability are governed by the capacity tensor. Flat directions correspond to
\[
\ker J,
\]
i.e. parameter deformations that do not alter the residual.

Thus SPT provides a coordinate-invariant formulation of optimization landscapes, natural gradient methods, and local identifiability.

---

## 8.3 Network science

Let \(G=(V,E,w)\) be a weighted graph with vertex set \(V=\{1,\dots,n\}\) and edge weights \(w_{ij}\ge 0\). The graph Laplacian is
\[
L(w)
=
\sum_{i<j} w_{ij} b_{ij}b_{ij}^T,
\]
where
\[
b_{ij}=e_i-e_j.
\]

Take
\[
\mathcal S=\{w_{ij}\}
\]
to be the space of edge weights. Let the structural potential be the spectrum of the Laplacian:
\[
\Pi(w)
=
\lambda(L(w))
=
(\lambda_1(w),\dots,\lambda_n(w)).
\]
Locally, away from eigenvalue crossings, \(\Pi\) is smooth.

Let \(\lambda_k\) be a simple eigenvalue with normalized eigenvector \(u_k\). Since
\[
L u_k=\lambda_k u_k,
\qquad
\|u_k\|=1,
\]
we have
\[
\frac{\partial \lambda_k}{\partial w_{ij}}
=
u_k^T
\frac{\partial L}{\partial w_{ij}}
u_k.
\]
But
\[
\frac{\partial L}{\partial w_{ij}}
=
b_{ij}b_{ij}^T.
\]
Therefore
\[
\frac{\partial \lambda_k}{\partial w_{ij}}
=
(u_k^T b_{ij})^2
=
\bigl(u_k(i)-u_k(j)\bigr)^2.
\]

Given a target spectrum \(\lambda^*=(\lambda_1^*,\dots,\lambda_n^*)\), define
\[
E(w)
=
\frac12
\sum_{k=1}^n
(\lambda_k(w)-\lambda_k^*)^2.
\]

The potential flow on edge weights is
\[
\frac{d w_{ij}}{dt}
=
-
\frac{\partial E}{\partial w_{ij}}
=
-
\sum_{k=1}^n
(\lambda_k-\lambda_k^*)
\bigl(u_k(i)-u_k(j)\bigr)^2.
\]

If nonnegativity or total-weight constraints are imposed, the flow is replaced by its projected or constrained version.

The capacity tensor on graph space is
\[
C_{ij,kl}
=
\sum_{m=1}^n
\frac{\partial \lambda_m}{\partial w_{ij}}
\frac{\partial \lambda_m}{\partial w_{kl}}
=
\sum_{m=1}^n
\bigl(u_m(i)-u_m(j)\bigr)^2
\bigl(u_m(k)-u_m(l)\bigr)^2.
\]

This tensor measures the ability of edge-weight deformations to modify spectral potentials. Equilibrium graphs satisfy
\[
\sum_{k=1}^n
(\lambda_k-\lambda_k^*)
\bigl(u_k(i)-u_k(j)\bigr)^2
=
0
\]
for every admissible edge direction.

Thus spectral graph design becomes an instance of structural potential realization.

---

## 8.4 Complex systems

Consider a dynamical system depending on an interaction structure \(A\), for example
\[
\dot x = F_A(x).
\]
Let \(\mathcal S\) be the space of admissible interaction structures \(A\). A structural potential may encode stability, responsiveness, or entropy production.

For a linear system
\[
\dot x = A x,
\]
one natural structural potential is the spectral abscissa
\[
\Pi(A):=\alpha(A):=\max_{\lambda\in\sigma(A)}\operatorname{Re}\lambda.
\]
Suppose \(\lambda(A)\) is a simple eigenvalue attaining \(\alpha(A)\), with right and left eigenvectors \(v,w\) normalized by
\[
w^*v=1.
\]
Then
\[
\frac{\partial \lambda}{\partial A_{ij}}
=
w_i v_j.
\]
Hence
\[
\frac{\partial \alpha}{\partial A_{ij}}
=
\operatorname{Re}(w_i v_j).
\]

For a target stability level \(\alpha_*<0\), define
\[
E(A)
=
\frac12(\alpha(A)-\alpha_*)^2.
\]
The potential flow is
\[
\frac{dA_{ij}}{dt}
=
-
(\alpha-\alpha_*)
\operatorname{Re}(w_i v_j).
\]

With constraints on sparsity, sign, or conservation laws, one uses the constrained potential flow from Section 5.4. Equilibria are interaction structures for which the stability defect is orthogonal to all admissible structural perturbations.

More generally, one may define a vector-valued structural potential
\[
\Pi(A)
=
\bigl(
\alpha(A),
\beta(A),
\Sigma(A),
\Gamma(A)
\bigr),
\]
where \(\beta\) may encode spectral gap, \(\Sigma\) entropy production, and \(\Gamma\) response susceptibility. SPT then provides a unified calculus for designing or analyzing complex systems that must simultaneously generate, transform, and stabilize collective behavior.

---

## 9. Conclusion

Structural Potential Theory generalizes classical potential theory by replacing scalar potentials on a fixed domain with structure-valued generative potentials on spaces of mathematical objects. The central map
\[
\Pi:\mathcal S\to\mathbb P
\]
assigns to each structure its capacity to generate, transform, or stabilize other structures. The differential calculus developed here introduces the potential-gradient tensor \(J^\alpha{}_a\), the capacity tensor \(C_{ab}\), equilibrium manifolds defined by normal equations, and potential flows governed by energy dissipation.

The theory provides a common analytical language for several domains:

- in geometric analysis, structural potentials encode curvature defects and generate geometric flows;
- in optimization, they recover Jacobian-based landscapes, natural gradients, and Gauss–Newton geometry;
- in network science, they describe spectral design and capacity of graph deformations;
- in complex systems, they formalize stability margins and adaptive structural evolution.

The central insight is that many variational problems are not fundamentally about scalar fields on spaces, but about the capacity of structures to realize potentials. SPT makes this insight precise.

---

## Appendix A. Notation

| Symbol | Meaning |
|---|---|
| \(\mathcal S\) | Space of structures |
| \(\mathbb P\) | Space of generative potentials |
| \(g_{ab}\) | Metric on \(\mathcal S\) |
| \(h_{\alpha\beta}\) | Metric on \(\mathbb P\) |
| \(\Pi:\mathcal S\to\mathbb P\) | Structural potential |
| \(J^\alpha{}_a\) | Potential-gradient tensor |
| \(C_{ab}\) | Capacity tensor |
| \(D\Pi^\dagger\) | Adjoint of \(D\Pi\) |
| \(E_{p_0}\) | Quadratic structural energy |
| \(r=\Pi-p_0\) | Potential residual |
| \(\mathcal E_{\Pi,p_0}\) | Equilibrium manifold |
| \(\operatorname{Cap}_\Pi\) | Structural capacity |

---

## Selected References

1. L. C. Evans, *Partial Differential Equations*, AMS, 2010.  
2. J. Milnor, *Morse Theory*, Princeton University Press, 1963.  
3. R. S. Hamilton, “Three-manifolds with positive Ricci curvature,” *J. Differential Geom.* 17 (1982), 255–306.  
4. S.-I. Amari, “Natural gradient works efficiently in learning,” *Neural Computation* 10 (1998), 251–276.  
5. F. R. K. Chung, *Spectral Graph Theory*, AMS, 1997.  
6. J. Jost, *Riemannian Geometry and Geometric Analysis*, Springer, 2017.

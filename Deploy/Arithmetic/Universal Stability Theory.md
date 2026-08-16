# Universal Stability Theory

**A Unified Axiomatic and Geometric Framework for Stability in Differential Equations, Optimization, Dynamical Systems, and Machine Learning**

**Preprint**

---

## Abstract

We develop **Universal Stability Theory (UST)**, an axiomatic framework that treats stability as a branch-independent mathematical invariant. Rather than defining stability separately as Lyapunov stability, coercivity, spectral gap, conditioning, or algorithmic robustness, UST postulates that every mathematical system is represented as a point in a metrized moduli space \(\mathcal{M}\), equipped with a distinguished instability locus \(\mathcal{I}\subset \mathcal{M}\). Stability is then measured by a universal functional
\[
\Sigma:\mathcal{M}\rightarrow \mathbb{R}_{\ge 0}\cup\{+\infty\},
\]
satisfying a small collection of structural axioms: calibration, invariance, perturbation Lipschitz continuity, calibrated escape, and smooth tensorial response. We prove a representation theorem showing that, under the UST axioms, the universal stability functional is precisely the metric distance to the instability locus:
\[
\Sigma(m)=\operatorname{dist}(m,\mathcal{I}).
\]
This yields a common geometric language for stability across mathematical disciplines. We develop the Riemannian differential geometry of \(\Sigma\), including the eikonal equation, stability one-form, Hessian stability tensor, Riccati-type curvature evolution, and gradient escape flow. We then specialize the theory to four domains: differential equations, optimization, dynamical systems, and machine learning. In each case, classical stability quantities—spectral abscissa, Lyapunov margins, Hessian curvature, contraction rates, spectral gaps, and uniform stability coefficients—are shown to arise as computable realizations or lower bounds of the universal functional. The result is a single formal architecture for comparing, estimating, and propagating stability across mathematical structures.

**Keywords:** stability, moduli space, Lyapunov theory, spectral gap, optimization, dynamical systems, algorithmic stability, Riemannian geometry.

---

## 1. Introduction

Stability is one of the most pervasive concepts in mathematics. It appears in the qualitative analysis of differential equations, the convergence theory of dynamical systems, the conditioning of optimization problems, the robustness of statistical estimators, and the generalization behavior of learning algorithms. Despite this ubiquity, the language of stability remains fragmented. In ordinary differential equations, stability is formulated through Lyapunov functions and spectral properties of Jacobians. In optimization, stability is expressed through strong convexity, Hessian positive definiteness, and sensitivity of minimizers. In ergodic theory and stochastic processes, stability is quantified by contraction, mixing, and spectral gaps. In machine learning, stability is often formulated as insensitivity of an algorithm to perturbations of the training sample.

These formulations are not unrelated, but they are rarely treated as manifestations of a single abstract invariant. The purpose of this paper is to provide such a treatment.

The central claim of **Universal Stability Theory (UST)** is the following:

> Stability is not primarily a property of a specific equation, algorithm, or dynamical law. It is a property of the location of a mathematical object inside a space of admissible objects, measured relative to the locus where a required structural property fails.

Accordingly, we model a mathematical system as a point \(m\) in a moduli space \(\mathcal{M}\). The space \(\mathcal{M}\) carries a perturbation metric \(d\), encoding the cost of moving from one mathematical object to another. A closed subset \(\mathcal{I}\subset\mathcal{M}\) represents the instability locus: the set of systems where the relevant property fails. The universal stability functional is then
\[
\Sigma:\mathcal{M}\rightarrow \mathbb{R}_{\ge 0}\cup\{+\infty\}.
\]
The larger \(\Sigma(m)\) is, the more perturbation the system \(m\) can absorb before reaching instability.

The central structural result is that, under natural axioms, \(\Sigma\) is uniquely represented as distance to instability:
\[
\Sigma(m)=\inf_{u\in\mathcal{I}} d(m,u).
\]
Thus UST replaces branch-specific criteria by a universal geometry of failure.

The contributions of this paper are as follows.

1. **Axiomatic foundation.** We introduce a minimal axiom system for universal stability functionals.
2. **Representation theorem.** We prove that any calibrated, perturbation-Lipschitz functional with calibrated escape paths is exactly distance to the instability locus.
3. **Tensorial differential geometry.** We develop the local geometry of \(\Sigma\), including the stability one-form, stability Hessian, eikonal equation, Riccati evolution, and quadratic stability tensor.
4. **Applications.** We show how classical stability constructs in differential equations, optimization, dynamical systems, and machine learning appear as concrete specializations or computable bounds of \(\Sigma\).
5. **Composition laws.** We derive stability of composite systems from product geometry.

The remainder of the paper is organized as follows. Section 2 develops the abstract axioms and proves the representation theorem. Section 3 develops the Riemannian tensor calculus of stability. Sections 4 through 7 apply the theory to differential equations, optimization, dynamical systems, and machine learning. Section 8 discusses computational estimation. Section 9 concludes.

---

## 2. Axiomatic Foundation of Universal Stability Theory

### 2.1 Stability structures

Let \(\mathcal{M}\) denote a moduli space of mathematical systems. The term “moduli space” is used broadly: \(\mathcal{M}\) may be a finite-dimensional parameter space, an infinite-dimensional function space, a space of vector fields, a space of objective functions, a space of stochastic processes, or a more categorical moduli stack. For the axiomatic theory, we require only that \(\mathcal{M}\) carry a metric structure.

#### Definition 2.1: Stability structure

A **stability structure** is a tuple
\[
\mathfrak{S}=(\mathcal{M},d,\Gamma,\mathcal{I}),
\]
where:

1. \(\mathcal{M}\) is a set or topological space of mathematical systems;
2. \(d:\mathcal{M}\times\mathcal{M}\to \mathbb{R}_{\ge 0}\cup\{+\infty\}\) is a perturbation metric;
3. \(\Gamma\) is a group of structure-preserving equivalences acting on \(\mathcal{M}\);
4. \(\mathcal{I}\subseteq \mathcal{M}\) is a closed instability locus.

The stable region is
\[
\mathcal{S}:=\mathcal{M}\setminus \mathcal{I}.
\]

The metric \(d\) measures the size of a perturbation. If \(m,n\in\mathcal{M}\), then \(d(m,n)\) is the cost of transforming system \(m\) into system \(n\). The group \(\Gamma\) encodes invariances: isomorphic systems must have identical stability.

#### Examples of moduli spaces

1. **Differential equations.**  
   Let
   \[
   \dot{x}^{i}=f^{i}(x;\theta),
   \]
   where \(\theta\in\Theta\). Then \(\mathcal{M}\) may be the space of parameterized vector fields \(f_\theta\).

2. **Optimization.**  
   Let
   \[
   F:\mathbb{R}^{n}\times \Theta\to \mathbb{R}.
   \]
   Then \(\mathcal{M}\) may be the space of objective functions \(F_\theta\).

3. **Dynamical systems.**  
   Let \(\varphi_t:X\to X\) be a flow. Then \(\mathcal{M}\) may be a space of flows, vector fields, or transition operators.

4. **Machine learning.**  
   Let \(A\) be a learning algorithm mapping datasets \(S\) to parameters \(\theta_S\). Then \(\mathcal{M}\) may be the space of algorithm-data configurations \((A,S)\), or the induced risk landscape.

The branch-specific notion of stability enters only through the choice of \(\mathcal{I}\). The universal functional form is independent of that choice.

---

### 2.2 Universal stability functionals

We now introduce the central object.

#### Definition 2.2: Universal stability functional

A map
\[
\Sigma:\mathcal{M}\to \mathbb{R}_{\ge 0}\cup\{+\infty\}
\]
is called a **universal stability functional** on \(\mathfrak{S}=(\mathcal{M},d,\Gamma,\mathcal{I})\) if it satisfies the following axioms.

#### Axiom U1: Calibration

\[
\Sigma(m)\ge 0,
\]
and
\[
\Sigma(m)=0 \quad \Longleftrightarrow \quad m\in \mathcal{I}.
\]

Thus \(\Sigma\) vanishes exactly on the instability locus.

#### Axiom U2: Equivalence invariance

For every \(\gamma\in\Gamma\),
\[
\Sigma(\gamma m)=\Sigma(m).
\]

Stability is invariant under admissible changes of coordinates, representation, or isomorphism class.

#### Axiom U3: Perturbation Lipschitz continuity

For all \(m,n\in\mathcal{M}\),
\[
|\Sigma(m)-\Sigma(n)|\le d(m,n).
\]

This axiom formalizes the principle that stability cannot change faster than the perturbation that produces the change.

#### Axiom U4: Calibrated escape

For every \(m\in\mathcal{M}\) with \(\Sigma(m)<+\infty\), there exists a unit-speed curve
\[
\gamma:[0,\Sigma(m)]\to \mathcal{M}
\]
such that
\[
\gamma(0)=m,\qquad \gamma(\Sigma(m))\in\mathcal{I},
\]
and
\[
\Sigma(\gamma(t))=\Sigma(m)-t.
\]

Thus from every stable state there exists an optimally destabilizing path along which stability decreases at unit rate.

#### Axiom U5: Smooth tensorial response

On the regular stable part
\[
\mathcal{S}_{\mathrm{reg}}\subseteq \mathcal{S},
\]
the functional \(\Sigma\) is at least \(C^{2}\), and infinitesimal perturbations admit a tensorial expansion. In local coordinates \(\theta^{i}\),
\[
\Sigma(\theta+\delta\theta)
=
\Sigma(\theta)
+
\partial_{i}\Sigma\,\delta\theta^{i}
+
\frac12 \partial_{i}\partial_{j}\Sigma\,\delta\theta^{i}\delta\theta^{j}
+
o(\|\delta\theta\|^{2}).
\]

This axiom is used when \(\mathcal{M}\) carries a smooth or Riemannian structure.

---

### 2.3 Representation theorem

The central theorem of UST identifies \(\Sigma\) with distance to instability.

Define the distance to the instability locus by
\[
d_{\mathcal{I}}(m):=\inf_{u\in\mathcal{I}} d(m,u).
\]

#### Theorem 2.1: Universal representation theorem

Let \(\mathfrak{S}=(\mathcal{M},d,\Gamma,\mathcal{I})\) be a stability structure. If \(\Sigma\) satisfies Axioms U1, U3, and U4, then
\[
\Sigma(m)=d_{\mathcal{I}}(m)
\]
for all \(m\in\mathcal{M}\).

**Proof.**

First, by Axiom U3 and Axiom U1, for any \(u\in\mathcal{I}\),
\[
\Sigma(m)\le \Sigma(u)+d(m,u)=d(m,u).
\]
Taking the infimum over \(u\in\mathcal{I}\) gives
\[
\Sigma(m)\le d_{\mathcal{I}}(m).
\]

Conversely, by Axiom U4, there exists a unit-speed curve \(\gamma:[0,\Sigma(m)]\to\mathcal{M}\) with \(\gamma(0)=m\), \(\gamma(\Sigma(m))\in\mathcal{I}\), and length equal to \(\Sigma(m)\). Since \(d_{\mathcal{I}}(m)\) is the infimal distance from \(m\) to \(\mathcal{I}\),
\[
d_{\mathcal{I}}(m)\le \operatorname{length}(\gamma)=\Sigma(m).
\]

Combining the two inequalities yields
\[
\Sigma(m)=d_{\mathcal{I}}(m).
\]

∎

#### Corollary 2.1: Robustness radius

If
\[
d(m,n)<\Sigma(m),
\]
then
\[
n\notin\mathcal{I}.
\]

**Proof.**

By Axiom U3,
\[
\Sigma(n)\ge \Sigma(m)-d(m,n)>0.
\]
By Axiom U1, \(n\notin\mathcal{I}\). ∎

Thus \(\Sigma(m)\) is precisely the radius of the largest open perturbation ball around \(m\) that remains inside the stable region.

---

### 2.4 Invariance

The representation theorem is compatible with Axiom U2.

#### Proposition 2.1

If \(d\) is \(\Gamma\)-invariant and \(\mathcal{I}\) is \(\Gamma\)-invariant, then
\[
d_{\mathcal{I}}(\gamma m)=d_{\mathcal{I}}(m)
\]
for all \(\gamma\in\Gamma\).

**Proof.**

Since \(\gamma\) is an isometry,
\[
d(\gamma m,\gamma u)=d(m,u).
\]
Since \(\gamma\mathcal{I}=\mathcal{I}\),
\[
\inf_{v\in\mathcal{I}}d(\gamma m,v)
=
\inf_{u\in\mathcal{I}}d(\gamma m,\gamma u)
=
\inf_{u\in\mathcal{I}}d(m,u).
\]
∎

Therefore the universal stability functional is automatically invariant under the symmetry group of the moduli space.

---

### 2.5 Composition of systems

UST also yields stability laws for composite systems.

Let
\[
\mathcal{M}=\mathcal{M}_1\times\mathcal{M}_2
\]
with product metric
\[
d^{2}\bigl((m_1,m_2),(n_1,n_2)\bigr)
=
d_1^2(m_1,n_1)+d_2^2(m_2,n_2).
\]

#### Theorem 2.2: Composition laws

Let \(\Sigma_i(m_i)=d_i(m_i,\mathcal{I}_i)\).

1. **Serial failure law.** If the composite system fails when either component fails, then
   \[
   \mathcal{I}=(\mathcal{I}_1\times\mathcal{M}_2)\cup(\mathcal{M}_1\times\mathcal{I}_2),
   \]
   and
   \[
   \Sigma(m_1,m_2)=\min\{\Sigma_1(m_1),\Sigma_2(m_2)\}.
   \]

2. **Joint failure law.** If the composite system fails only when both components fail, then
   \[
   \mathcal{I}=\mathcal{I}_1\times\mathcal{I}_2,
   \]
   and
   \[
   \Sigma(m_1,m_2)
   =
   \sqrt{\Sigma_1(m_1)^2+\Sigma_2(m_2)^2}.
   \]

**Proof.**

For serial failure,
\[
\operatorname{dist}\bigl((m_1,m_2),\mathcal{I}_1\times\mathcal{M}_2\bigr)
=
\operatorname{dist}(m_1,\mathcal{I}_1)=\Sigma_1(m_1),
\]
and similarly for the second component. The distance to a union is the minimum of the distances, hence
\[
\Sigma(m_1,m_2)=\min\{\Sigma_1(m_1),\Sigma_2(m_2)\}.
\]

For joint failure,
\[
\operatorname{dist}\bigl((m_1,m_2),\mathcal{I}_1\times\mathcal{I}_2\bigr)^2
=
\operatorname{dist}(m_1,\mathcal{I}_1)^2
+
\operatorname{dist}(m_2,\mathcal{I}_2)^2.
\]
Therefore
\[
\Sigma(m_1,m_2)=\sqrt{\Sigma_1(m_1)^2+\Sigma_2(m_2)^2}.
\]
∎

These laws are universal consequences of product geometry.

---

## 3. Riemannian Geometry of the Stability Functional

We now assume that \(\mathcal{M}\) is a smooth Riemannian manifold with metric tensor
\[
g=g_{ij}\,d\theta^{i}d\theta^{j}.
\]
Let
\[
r(\theta):=\Sigma(\theta).
\]
We work locally on the regular stable region away from cut loci.

---

### 3.1 Stability one-form and eikonal equation

Define the stability one-form
\[
\sigma_i:=\nabla_i r.
\]
Its raised version is
\[
\sigma^{i}=g^{ij}\sigma_j.
\]

Because \(r\) is the distance to \(\mathcal{I}\), its gradient has unit norm along minimizing geodesics.

#### Proposition 3.1: Eikonal equation

On the regular part of \(\mathcal{S}\),
\[
g^{ij}\nabla_i r\nabla_j r=1.
\]

Equivalently,
\[
\|\nabla r\|_g=1.
\]

**Proof.**

Let \(\gamma(s)\) be a unit-speed minimizing geodesic from \(u\in\mathcal{I}\) to \(m\). Then
\[
r(\gamma(s))=s.
\]
Differentiating,
\[
\frac{d}{ds}r(\gamma(s))
=
\nabla_i r\,\dot{\gamma}^{i}
=
1.
\]
Since \(\|\dot{\gamma}\|_g=1\), equality in the Cauchy–Schwarz inequality implies
\[
\nabla r=\dot{\gamma},
\]
and therefore
\[
\|\nabla r\|_g=1.
\]
∎

The eikonal equation is the differential expression of the UST representation theorem.

---

### 3.2 Stability Hessian and quadratic response

Define the stability Hessian
\[
S_{ij}:=\nabla_i\nabla_j r.
\]
For a small perturbation \(\delta\theta^{i}\),
\[
r(\theta+\delta\theta)
=
r(\theta)
+
\sigma_i\delta\theta^{i}
+
\frac12 S_{ij}\delta\theta^{i}\delta\theta^{j}
+
O(\|\delta\theta\|^{3}).
\]

The first-order loss of stability under a unit perturbation \(v^{i}\) is
\[
\delta^{(1)}r=\sigma_i v^{i}.
\]
Since \(\|\sigma\|_g=1\), the most destabilizing unit perturbation satisfies
\[
v^{i}=-\sigma^{i}.
\]
Thus the critical perturbation direction is the negative stability gradient.

---

### 3.3 Quadratic stability potential

It is often useful to work with the squared stability potential
\[
\Phi(\theta):=\frac12 r(\theta)^2.
\]
Then
\[
\nabla_i\Phi=r\sigma_i,
\]
and
\[
K_{ij}:=\nabla_i\nabla_j\Phi
=
\sigma_i\sigma_j+rS_{ij}.
\]

We call \(K_{ij}\) the **quadratic stability tensor**.

If \(K_{ij}\) is positive definite in a neighborhood, then the stability basin is locally quadratically robust. The eigenvalues of
\[
K^{i}{}_{j}=g^{ik}K_{kj}
\]
measure principal directions of second-order stability.

---

### 3.4 Riccati evolution of the stability Hessian

Let
\[
n^{i}:=\sigma^{i}
\]
be the unit normal field to level sets of \(r\). The shape operator of the level sets is
\[
S_{ij}=\nabla_i n_j.
\]

Along normal geodesics, \(S_{ij}\) satisfies a Riccati-type equation:
\[
n^{k}\nabla_k S_{ij}
+
S_{i}{}^{k}S_{kj}
+
R_{ikj\ell}n^{k}n^{\ell}
=
0,
\]
where \(R_{ikj\ell}\) is the Riemann curvature tensor of \((\mathcal{M},g)\).

This equation shows that the local nonlinear response of stability is governed by both the curvature of the instability locus and the intrinsic curvature of the moduli space.

---

### 3.5 Universal destabilization flow

Consider the gradient flow
\[
\dot{\theta}^{i}=-g^{ij}\nabla_j r.
\]
Then
\[
\frac{d}{dt}r(\theta(t))
=
\nabla_i r\,\dot{\theta}^{i}
=
-\|\nabla r\|_g^{2}
=
-1.
\]
Therefore
\[
r(\theta(t))=r(\theta(0))-t.
\]
The flow reaches the instability locus in time
\[
T=r(\theta(0))=\Sigma(\theta(0)).
\]

Thus \(\Sigma\) is not merely a static margin; it is the time-to-instability under the canonical destabilization flow.

---

## 4. Differential Equations

We now apply UST to differential equations. Consider a parameterized system
\[
\dot{x}^{i}=f^{i}(x;\theta),
\]
where \(x\in\mathbb{R}^{n}\) and \(\theta\in\Theta\). Let \(x_{*}(\theta)\) be an equilibrium:
\[
f^{i}(x_{*}(\theta);\theta)=0.
\]

The local behavior near \(x_{*}\) is governed by the Jacobian tensor
\[
J^{i}{}_{j}(\theta)
=
\left.\frac{\partial f^{i}}{\partial x^{j}}\right|_{x=x_{*}(\theta)}.
\]

---

### 4.1 Spectral stability margin

The equilibrium is locally asymptotically stable if all eigenvalues \(\lambda\) of \(J\) satisfy
\[
\operatorname{Re}\lambda<0.
\]
Define the spectral abscissa
\[
\alpha(\theta):=\max_{\lambda\in\operatorname{spec}(J(\theta))}\operatorname{Re}\lambda.
\]

The instability locus contains
\[
\mathcal{I}_{\mathrm{spec}}
=
\{\theta:\alpha(\theta)=0\}.
\]

A natural branch-specific stability margin is
\[
\Sigma_{\mathrm{spec}}(\theta):=\max\{0,-\alpha(\theta)\}.
\]

In UST, the universal functional is the distance to \(\mathcal{I}_{\mathrm{spec}}\), but \(\Sigma_{\mathrm{spec}}\) is often a computable surrogate.

---

### 4.2 Local distance to spectral instability

Assume \(\alpha\) is smooth near \(\theta\) and \(\alpha(\theta)<0\). The instability boundary is locally the hypersurface
\[
\alpha(\vartheta)=0.
\]

The closest point on this hypersurface is approximated by moving along the negative normalized gradient:
\[
v^{a}=-\frac{g^{ab}\partial_b\alpha}{\|\nabla\alpha\|_g}.
\]
Let \(t\) be the step size. To first order,
\[
\alpha(\theta+t v)
=
\alpha(\theta)+t\,\partial_a\alpha\,v^{a}.
\]
Since
\[
\partial_a\alpha\,v^{a}
=
-\|\nabla\alpha\|_g,
\]
the crossing time is
\[
t=\frac{-\alpha(\theta)}{\|\nabla\alpha\|_g}.
\]

Therefore
\[
d_{\mathcal{I}_{\mathrm{spec}}}(\theta)
=
\frac{-\alpha(\theta)}{\|\nabla\alpha\|_g}
+
O(\alpha^2).
\]

This gives a universal first-order approximation to the UST stability margin.

---

### 4.3 Eigenvalue sensitivity tensor

Assume \(\lambda\) is a simple eigenvalue of \(J\). Let \(v^{j}\) be a right eigenvector and \(w_i\) a left eigenvector:
\[
J^{i}{}_{j}v^{j}=\lambda v^{i},
\]
\[
w_i J^{i}{}_{j}=\lambda w_j,
\]
normalized by
\[
w_i v^{i}=1.
\]

Differentiating the eigenvalue equation gives
\[
\delta\lambda
=
w_i\,\delta J^{i}{}_{j}\,v^{j}.
\]

For parameter perturbations \(\delta\theta^{a}\),
\[
\delta J^{i}{}_{j}
=
\partial_a J^{i}{}_{j}\,\delta\theta^{a}.
\]
Hence
\[
\partial_a\lambda
=
w_i\,\partial_a J^{i}{}_{j}\,v^{j}.
\]

If \(\lambda\) is the active eigenvalue attaining the spectral abscissa, then formally
\[
\partial_a\alpha
=
\operatorname{Re}\!\left(
w_i\,\partial_a J^{i}{}_{j}\,v^{j}
\right).
\]

When several eigenvalues are active, \(\alpha\) is generally nonsmooth and its subdifferential is the convex hull of the corresponding eigenvalue gradients.

---

### 4.4 Lyapunov robustness bound

Let \(J\) be Hurwitz. Choose a positive definite tensor \(Q_{ij}=Q_{ji}>0\). The Lyapunov equation
\[
J^{k}{}_{i}P_{kj}+J^{k}{}_{j}P_{ik}
=
-Q_{ij}
\]
has a unique positive definite solution \(P_{ij}=P_{ji}>0\).

Define the quadratic Lyapunov function
\[
V(x)=x^{i}P_{ij}x^{j}.
\]

For the unperturbed system,
\[
\dot V=-x^{i}Q_{ij}x^{j}.
\]

Now perturb the Jacobian:
\[
J^{i}{}_{j}\mapsto J^{i}{}_{j}+\Delta^{i}{}_{j}.
\]
Then
\[
\dot V
=
-x^{i}Q_{ij}x^{j}
+
x^{i}\bigl(\Delta^{k}{}_{i}P_{kj}+P_{ik}\Delta^{k}{}_{j}\bigr)x^{j}.
\]

Using the operator norm \(\|\cdot\|\),
\[
x^{i}\bigl(\Delta^{k}{}_{i}P_{kj}+P_{ik}\Delta^{k}{}_{j}\bigr)x^{j}
\le
2\|P\|\,\|\Delta\|\,\|x\|^{2}.
\]

Therefore
\[
\dot V
\le
-\bigl(\lambda_{\min}(Q)-2\|P\|\|\Delta\|\bigr)\|x\|^{2}.
\]

Stability is preserved whenever
\[
\|\Delta\|<\frac{\lambda_{\min}(Q)}{2\|P\|}.
\]

Thus a concrete lower bound for the universal stability radius is
\[
\Sigma_{\mathrm{ODE}}
\ge
\rho(J)
:=
\sup_{Q>0}\frac{\lambda_{\min}(Q)}{2\|P_Q\|}.
\]

For parameter perturbations,
\[
\Delta^{i}{}_{j}
=
\partial_a J^{i}{}_{j}\,\delta\theta^{a}.
\]
If
\[
\|\Delta\|\le \|\partial J\|\,\|\delta\theta\|,
\]
then the parameter stability radius satisfies
\[
\|\delta\theta\|
<
\frac{1}{\|\partial J\|}
\sup_{Q>0}\frac{\lambda_{\min}(Q)}{2\|P_Q\|}.
\]

This provides a rigorous differential-equation realization of the UST functional.

---

## 5. Optimization

Consider a parameterized optimization problem
\[
\min_{x\in\mathbb{R}^{n}} F(x;\theta).
\]
Let \(x_{*}(\theta)\) be a local minimizer satisfying
\[
\partial_i F(x_{*}(\theta);\theta)=0.
\]

Define the Hessian tensor
\[
H_{ij}(\theta):=\partial_i\partial_j F(x_{*}(\theta);\theta).
\]

A nondegenerate local minimum requires
\[
H_{ij}>0
\]
in the positive-definite sense.

---

### 5.1 Curvature stability margin

Let
\[
\lambda_{\min}(\theta)
\]
be the smallest eigenvalue of \(H_{ij}\). The curvature stability margin is
\[
\Sigma_{\mathrm{curv}}(\theta):=\lambda_{\min}(\theta).
\]

The instability locus is
\[
\mathcal{I}_{\mathrm{opt}}
=
\{\theta:\lambda_{\min}(H(\theta))=0\}.
\]

By Weyl’s inequality, if \(E_{ij}\) is a symmetric Hessian perturbation, then
\[
\lambda_{\min}(H+E)
\ge
\lambda_{\min}(H)-\|E\|.
\]

Therefore positive definiteness is preserved whenever
\[
\|E\|<\lambda_{\min}(H).
\]

Thus
\[
\Sigma_{\mathrm{curv}}=\lambda_{\min}(H)
\]
is exactly the operator-norm radius of curvature stability.

---

### 5.2 Sensitivity tensor of the minimizer

Let \(p^{a}\) be external parameters. The first-order condition is
\[
\partial_i F(x_{*}(p),p)=0.
\]

Differentiating with respect to \(p^{a}\),
\[
\partial_j\partial_i F\,\partial_a x_{*}^{j}
+
\partial_a\partial_i F
=
0.
\]

Thus
\[
H_{ij}\partial_a x_{*}^{j}
=
-\partial_a\partial_i F.
\]

Assuming \(H\) is invertible,
\[
\partial_a x_{*}^{i}
=
-H^{ij}\partial_a\partial_j F,
\]
where \(H^{ij}\) is the inverse Hessian tensor:
\[
H^{ik}H_{kj}=\delta^{i}_{j}.
\]

For a perturbation of the objective
\[
F\mapsto F+\varepsilon g,
\]
the minimizer changes by
\[
\delta x^{i}
=
-\varepsilon H^{ij}\partial_j g
+
O(\varepsilon^{2}).
\]

Hence
\[
\|\delta x\|
\le
\frac{\varepsilon\|\nabla g\|}{\lambda_{\min}(H)}.
\]

This shows that the inverse curvature margin controls sensitivity.

---

### 5.3 Gradient-flow stability

Consider gradient flow
\[
\dot{x}^{i}=-g^{ij}\partial_j F.
\]
Near \(x_{*}\),
\[
\dot{\xi}^{i}
=
-H^{i}{}_{j}\xi^{j}.
\]

If \(H\) is positive definite, perturbations decay. In an orthonormal eigenbasis,
\[
\xi^{i}(t)=e^{-\lambda_i t}\xi^{i}(0).
\]

The slowest decay rate is
\[
\lambda_{\min}(H).
\]
Thus the dynamical stability margin of the optimizer is again governed by the minimum Hessian eigenvalue.

---

### 5.4 Stochastic optimization

Suppose
\[
F(x)=\mathbb{E}_{z}[f(z,x)]
\]
and the empirical objective is
\[
F_S(x)=\frac{1}{n}\sum_{k=1}^{n}f(z_k,x).
\]

At the minimizer,
\[
\partial_i F_S(x_{*})=0.
\]

The Hessian is
\[
H_{ij}=\partial_i\partial_j F(x_{*}).
\]

Sampling noise induces a gradient perturbation with covariance
\[
C_{ij}
=
\mathbb{E}\bigl[\partial_i f(z,x_{*})\,\partial_j f(z,x_{*})\bigr].
\]

To first order,
\[
H_{ij}\delta x^{j}
=
-\delta g_i,
\]
so
\[
\delta x^{i}
=
-H^{ij}\delta g_j.
\]

Therefore
\[
\operatorname{Cov}(\delta x)
=
\frac{1}{n}H^{-1}CH^{-1}.
\]

In tensor notation,
\[
\operatorname{Cov}(\delta x)^{i\ell}
=
\frac{1}{n}H^{ij}C_{jk}H^{k\ell}.
\]

Thus stability of statistical optimization is controlled by the inverse Hessian and the noise covariance.

---

## 6. Dynamical Systems

Let \(X\) be a Riemannian manifold with metric \(g_{ij}\). Consider a smooth vector field \(f^{i}\) generating a flow \(\varphi_t\):
\[
\dot{x}^{i}=f^{i}(x).
\]

Let \(\xi^{i}\) be an infinitesimal perturbation. Its evolution is
\[
\frac{D\xi^{i}}{dt}
=
\nabla_j f^{i}\,\xi^{j}.
\]

The squared norm is
\[
\|\xi\|^{2}=g_{ij}\xi^{i}\xi^{j}.
\]

Differentiating along the flow gives
\[
\frac{d}{dt}\|\xi\|^{2}
=
(\nabla_i f_j+\nabla_j f_i)\xi^{i}\xi^{j}.
\]

Define the deformation tensor
\[
B_{ij}:=\nabla_i f_j+\nabla_j f_i.
\]

---

### 6.1 Contraction stability

If there exists \(\sigma>0\) such that
\[
B_{ij}\le -2\sigma g_{ij}
\]
as symmetric tensors, then
\[
\frac{d}{dt}\|\xi\|^{2}
\le
-2\sigma\|\xi\|^{2}.
\]

Therefore
\[
\|\xi(t)\|
\le
e^{-\sigma t}\|\xi(0)\|.
\]

The contraction stability margin is
\[
\Sigma_{\mathrm{contr}}:=\sigma.
\]

Equivalently,
\[
\sigma
=
-\lambda_{\max}\!\left(\frac{1}{2}B^{i}{}_{j}\right),
\]
when the right-hand side is positive.

---

### 6.2 Lyapunov exponent margin

For nonuniform systems, define the maximal Lyapunov exponent
\[
\lambda_{\max}
=
\limsup_{t\to\infty}
\frac{1}{t}
\log \|D\varphi_t\|.
\]

If
\[
\lambda_{\max}<0,
\]
the system is asymptotically stable in the Lyapunov sense. The corresponding UST margin is
\[
\Sigma_{\mathrm{Lyap}}:=-\lambda_{\max}.
\]

The instability locus is
\[
\mathcal{I}_{\mathrm{Lyap}}
=
\{f:\lambda_{\max}(f)=0\}.
\]

Thus UST recovers classical Lyapunov stability as distance to the zero-Lyapunov-exponent locus.

---

### 6.3 Lyapunov function formulation

Suppose there exists a scalar function \(V:X\to\mathbb{R}_{\ge 0}\) such that
\[
V(x)=0
\]
on an attractor \(A\), and
\[
\dot V\le -cV
\]
outside \(A\). Then
\[
V(\varphi_t(x))\le e^{-ct}V(x).
\]

The decay rate \(c\) is a stability margin:
\[
\Sigma_V\ge c.
\]

Under a perturbation \(f\mapsto f+\delta f\), if
\[
\dot V\le -(c-L\|\delta f\|)V,
\]
then stability persists whenever
\[
\|\delta f\|<\frac{c}{L}.
\]

Again, stability is distance to the locus where the decay rate vanishes.

---

### 6.4 Stochastic dynamical systems and spectral gaps

Let \(L\) be the generator of a Markov process with invariant measure \(\pi\). Assume \(L\) is self-adjoint on \(L^{2}(\pi)\) and nonpositive.

Define the Dirichlet form
\[
\mathcal{E}(h)
=
-\langle h,Lh\rangle_{L^{2}(\pi)}.
\]

The spectral gap is
\[
\gamma
=
\inf_{\substack{h\perp 1\\ h\ne 0}}
\frac{\mathcal{E}(h)}{\|h\|^{2}_{L^{2}(\pi)}}.
\]

Then
\[
\|P_t h-\pi(h)\|_{L^{2}(\pi)}
\le
e^{-\gamma t}\|h-\pi(h)\|_{L^{2}(\pi)}.
\]

Thus the universal stability functional is
\[
\Sigma_{\mathrm{gap}}=\gamma.
\]

For a perturbation \(L\mapsto L+\varepsilon V\), a min-max estimate gives
\[
\gamma_\varepsilon
\ge
\gamma-\varepsilon\|V\|.
\]

Therefore the stability radius is at least
\[
\frac{\gamma}{\|V\|}.
\]

---

## 7. Machine Learning

We now apply UST to statistical learning. Let \(z\in\mathcal{Z}\) be a data point, \(\theta\in\Theta\) parameters, and
\[
\ell(z,\theta)
\]
a loss function. The population risk is
\[
R(\theta)=\mathbb{E}_{z}[\ell(z,\theta)].
\]
Given a sample
\[
S=(z_1,\dots,z_n),
\]
the empirical risk is
\[
R_S(\theta)=\frac{1}{n}\sum_{k=1}^{n}\ell(z_k,\theta).
\]

A learning algorithm is a map
\[
A:S\mapsto \theta_S.
\]

---

### 7.1 Algorithmic stability as inverse sensitivity

Let \(S\) and \(S'\) differ in one example. Define the Hamming data distance
\[
d_H(S,S')=\frac{1}{n}\#\{k:z_k\ne z'_k\}.
\]

Uniform stability is traditionally measured by
\[
\beta
=
\sup_{S\sim S'}
\sup_{z}
\left|
\ell(z,A(S))-\ell(z,A(S'))
\right|.
\]

Smaller \(\beta\) means greater stability. In UST, where larger \(\Sigma\) means greater stability, we define
\[
\Sigma_{\mathrm{ML}}:=\beta^{-1},
\]
or, with a target tolerance \(\tau>0\),
\[
\Sigma_{\mathrm{ML},\tau}:=\frac{\tau}{\beta}.
\]

This is consistent with the universal representation theorem if the instability locus is taken to be the set of algorithm-data configurations for which the generalization gap exceeds \(\tau\).

---

### 7.2 Stability from strong convexity

Assume each loss \(\ell(z,\cdot)\) is \(\mu\)-strongly convex and has \(G\)-bounded gradients:
\[
\|\nabla_\theta \ell(z,\theta)\|\le G.
\]
Assume also that \(\ell(z,\cdot)\) is \(L\)-Lipschitz.

Let \(\theta_S\) minimize \(R_S\), and let \(\theta_{S'}\) minimize \(R_{S'}\), where \(S\) and \(S'\) differ by one example.

Since \(R_S\) is \(\mu\)-strongly convex,
\[
\langle \nabla R_S(\theta_S)-\nabla R_S(\theta_{S'}),\theta_S-\theta_{S'}\rangle
\ge
\mu\|\theta_S-\theta_{S'}\|^{2}.
\]

Because \(\nabla R_S(\theta_S)=0\),
\[
\mu\|\theta_S-\theta_{S'}\|^{2}
\le
\|\nabla R_S(\theta_{S'})\|\,\|\theta_S-\theta_{S'}\|.
\]

Now
\[
\nabla R_S(\theta_{S'})
=
\nabla R_{S'}(\theta_{S'})
+
\frac{1}{n}
\left(
\nabla\ell(z_{\mathrm{old}},\theta_{S'})
-
\nabla\ell(z_{\mathrm{new}},\theta_{S'})
\right).
\]

Since \(\nabla R_{S'}(\theta_{S'})=0\),
\[
\|\nabla R_S(\theta_{S'})\|
\le
\frac{2G}{n}.
\]

Therefore
\[
\|\theta_S-\theta_{S'}\|
\le
\frac{2G}{n\mu}.
\]

Using \(L\)-Lipschitzness of the loss,
\[
\left|
\ell(z,\theta_S)-\ell(z,\theta_{S'})
\right|
\le
L\|\theta_S-\theta_{S'}\|
\le
\frac{2LG}{n\mu}.
\]

Thus
\[
\beta
\le
\frac{2LG}{n\mu}.
\]

Consequently,
\[
\Sigma_{\mathrm{ML}}
\ge
\frac{n\mu}{2LG}.
\]

This is a universal stability lower bound for empirical risk minimization.

---

### 7.3 Tensorial influence functions

Let \(\theta_{*}\) be the population minimizer. Define the risk Hessian
\[
H_{ij}
=
\nabla_i\nabla_j R(\theta_{*}),
\]
and the sample gradient
\[
g_i(z)
=
\nabla_i \ell(z,\theta_{*}).
\]

The first-order influence of sample \(z_k\) on the empirical minimizer is
\[
\delta\theta^{i}_k
=
-\frac{1}{n}H^{ij}g_j(z_k),
\]
where
\[
H^{ij}H_{jk}=\delta^{i}_{k}.
\]

The corresponding change in predictions is
\[
\delta \ell(z,\theta_{*})
\approx
\nabla_i\ell(z,\theta_{*})\,\delta\theta^{i}
=
-\frac{1}{n}\nabla_i\ell(z,\theta_{*})H^{ij}g_j(z_k).
\]

Thus the influence tensor is
\[
\mathcal{I}^{i}{}_{j}(z)
=
-\frac{1}{n}H^{ik}\nabla_k\nabla_j\ell(z,\theta_{*}),
\]
for perturbations of the objective, and the sample influence vector is
\[
I^{i}(z_k)
=
-\frac{1}{n}H^{ij}g_j(z_k).
\]

The norm of \(H^{-1}\) again controls stability. If the smallest eigenvalue of \(H\) is \(\mu\), then
\[
\|I(z_k)\|
\le
\frac{\|g(z_k)\|}{n\mu}.
\]

Thus strong convexity produces a large universal stability margin.

---

### 7.4 Generalization consequence

For a \(\beta\)-uniformly stable algorithm with bounded loss, one has the standard expectation bound
\[
\mathbb{E}\bigl[R(A(S))-R_S(A(S))\bigr]
\le
\beta.
\]

Using the bound above,
\[
\mathbb{E}\bigl[R(\theta_S)-R_S(\theta_S)\bigr]
\le
\frac{2LG}{n\mu}.
\]

In UST language, the generalization gap is controlled by the inverse stability functional:
\[
\text{generalization gap}
\lesssim
\Sigma_{\mathrm{ML}}^{-1}.
\]

Thus stability, distance to instability, and generalization are unified.

---

## 8. Unified Correspondence

The following table summarizes the specialization of UST to the four domains.

| Domain | Moduli space \(\mathcal{M}\) | Instability locus \(\mathcal{I}\) | Stability functional \(\Sigma\) |
|---|---|---|---|
| Differential equations | Parameterized vector fields \(f_\theta\) | Nonhyperbolic equilibrium, \(\alpha(\theta)=0\) | Spectral margin, Lyapunov robustness radius |
| Optimization | Objective functions \(F_\theta\) | Singular or indefinite Hessian | Minimum Hessian eigenvalue, curvature margin |
| Dynamical systems | Flows or generators | Zero Lyapunov exponent or zero spectral gap | Contraction rate, \(-\lambda_{\max}\), spectral gap |
| Machine learning | Algorithms and datasets | Excessive generalization gap | Inverse uniform stability, \(1/\beta\) |

The universal object is always distance to the relevant failure locus.

---

## 9. Computational Estimation of \(\Sigma\)

Exact computation of
\[
\Sigma(m)=\inf_{u\in\mathcal{I}}d(m,u)
\]
is often as hard as solving the underlying stability problem. However, UST provides systematic approximation schemes.

### 9.1 Boundary-linearization approximation

If the instability locus is locally described by a smooth constraint
\[
\Phi(m)=0,
\]
with stable region \(\Phi(m)<0\), then
\[
\Sigma(m)
\approx
\frac{-\Phi(m)}{\|\nabla\Phi(m)\|_g}.
\]

Examples:

- Differential equations: \(\Phi=\alpha\), the spectral abscissa.
- Optimization: \(\Phi=-\lambda_{\min}(H)\).
- Dynamical systems: \(\Phi=\lambda_{\max}\).
- Machine learning: \(\Phi=\beta-\tau\).

### 9.2 Hessian-based approximation

If \(\Phi\) is smooth and \(\nabla\Phi(m)=0\) at a critical point, a second-order approximation is needed:
\[
\Sigma(m)
\approx
\sqrt{\frac{-2\Phi(m)}{\lambda_{\max}(\nabla^2\Phi)}}.
\]

This is common near bifurcation points, saddle-node transitions, and loss-landscape degeneracies.

### 9.3 Adversarial projection

One may estimate \(\Sigma\) by solving
\[
\min_{u\in\mathcal{M}} d(m,u)
\quad\text{subject to}\quad
u\in\mathcal{I}.
\]

In finite dimensions, this becomes a constrained optimization problem:
\[
\min_{\vartheta}
\frac12 g_{ab}(\vartheta-\theta)^{a}(\vartheta-\theta)^{b}
\]
subject to
\[
\Phi(\vartheta)=0.
\]

The Lagrange multiplier equation is
\[
g_{ab}(\vartheta-\theta)^{b}
+
\lambda\,\partial_a\Phi(\vartheta)=0.
\]

This identifies the closest instability direction.

---

## 10. Conclusion

Universal Stability Theory provides a single axiomatic and geometric framework for stability across mathematics. By representing a system as a point in a metrized moduli space and stability as distance to an instability locus, UST unifies apparently disparate concepts: Lyapunov stability, spectral margins, Hessian conditioning, contraction rates, spectral gaps, and algorithmic robustness.

The central representation theorem shows that the universal stability functional is not an arbitrary heuristic. Under calibration, invariance, perturbation Lipschitz continuity, and calibrated escape, it is forced to be the distance to failure:
\[
\Sigma(m)=\operatorname{dist}(m,\mathcal{I}).
\]

The resulting geometry is rich. The stability one-form satisfies an eikonal equation. Its Hessian governs quadratic response. Riccati evolution describes nonlinear focusing of instability. Gradient descent in the stability functional gives a canonical path to failure whose travel time equals the stability margin.

The applications demonstrate that UST does not erase the distinctions between mathematical domains. Rather, it organizes them. Branch-specific stability criteria become local coordinates, computable surrogates, or rigorous lower bounds for a single universal invariant.

Future developments will extend UST to categorical moduli spaces, stochastic partial differential equations, non-metric topological stability, and adaptive learning systems where the moduli space itself evolves in time.

---

## References

1. A. M. Lyapunov, *The General Problem of the Stability of Motion*, Taylor & Francis, 1992. Original work published 1892.

2. J. Guckenheimer and P. Holmes, *Nonlinear Oscillations, Dynamical Systems, and Bifurcations of Vector Fields*, Springer, 1983.

3. S. Boyd and L. Vandenberghe, *Convex Optimization*, Cambridge University Press, 2004.

4. O. Bousquet and A. Elisseeff, “Stability and Generalization,” *Journal of Machine Learning Research*, vol. 2, pp. 499–526, 2002.

5. P. L. Lions, *Generalized Solutions of Hamilton–Jacobi Equations*, Pitman, 1982.

# Probabilistic Geometry: Intrinsic Uncertainty, Expected Metrics, and Expectation-Valued Curvature

**Preprint**

---

## Abstract

We develop a foundational framework for **Probabilistic Geometry** (PG), a geometric theory in which uncertainty is not an external perturbation of classical geometry but an intrinsic primitive. In PG, a point is not a coordinate \(x\in M\) but a probability law \(P\in \mathcal P(M)\) on a base geometric space. Distances are optimal expected base distances,

\[
d(P,Q)=\inf_{\pi\in\Pi(P,Q)}\mathbb E_{(X,Y)\sim\pi}[\rho(X,Y)],
\]

where \(\rho\) is the underlying metric and the infimum is taken over all couplings of \(P\) and \(Q\). Curvature is promoted to an expectation-valued tensor by parallel transport to a probabilistic barycenter. The resulting theory synthesizes optimal transport, Riemannian geometry, and stochastic analysis. We establish metric axioms, geodesic interpolation, a differential calculus, an expected Riemann curvature tensor,

\[
\mathcal R^{a}{}_{bcd}(P)
=
\int_M
\Lambda^{a}{}_{i}(x)
\Lambda^{j}{}_{b}(x)
\Lambda^{k}{}_{c}(x)
\Lambda^{l}{}_{d}(x)
R^{i}{}_{jkl}(x)
\,dP(x),
\]

and a decomposition of intrinsic PG sectional curvature into an expected base curvature term plus a nonnegative transport term. Applications are developed in machine learning, robotics, statistics, and quantum theory.

**Keywords:** probabilistic geometry, optimal transport, Wasserstein distance, curvature, Fréchet mean, geometric uncertainty, quantum geometry.

---

## 1. Introduction

Classical geometry assumes that its primitives are exact. A point is an element \(x\in M\), a curve is a map \(\gamma:[0,1]\to M\), and curvature is a tensor field evaluated at \(x\). This assumption is increasingly inadequate in settings where the primitive object is not a location but a **state of uncertainty**: a posterior distribution in statistics, a belief state in robotics, a latent distribution in machine learning, or a mixed quantum state.

Probabilistic Geometry begins from a different axiom.

### Axiom 1: Probabilistic locality

The fundamental geometric object is not a point \(x\), but a probability law \(P\) over possible points.

Thus the classical embedding

\[
x\longmapsto \delta_x
\]

is not the definition of a point but a degenerate limit. Geometry itself becomes distributional.

### Axiom 2: Coupled expected distance

The distance between probabilistic points is an expected base distance under an optimal coupling:

\[
d(P,Q)=\mathbb E_{\pi^\ast}[\rho(X,Y)].
\]

The expectation is not taken with respect to an arbitrary product measure; it is taken with respect to a coupling \(\pi^\ast\) minimizing expected cost. This identifies the primary PG distance with the first Wasserstein distance.

### Axiom 3: Expectation-valued curvature

Geometric tensors are no longer pointwise fields. They become expectation-valued objects obtained by transporting local tensors to a common probabilistic barycenter and integrating.

The purpose of this paper is to develop this framework as a self-contained geometric theory.

The theory is related to, but conceptually distinct from, classical Wasserstein geometry. Wasserstein geometry studies the geometry of the space \(\mathcal P_2(M)\) of probability measures. Probabilistic Geometry takes the further step of treating probability laws themselves as **points of the geometry**, and then re-expressing metric, tangent, geodesic, and curvature notions in terms of expected geometric quantities. In PG, curvature is not merely a synthetic condition on measure spaces; it becomes an explicit tensorial expectation.

The paper is organized as follows. Section 2 defines probabilistic points and the expected distance metric. Section 3 develops the differential structure and geodesic equations. Section 4 introduces expectation-valued curvature tensors and proves a probabilistic Gauss–Bonnet-type excess formula. Section 5 collects structural theorems. Section 6 develops applications. Section 7 concludes.

---

## 2. Metric Foundations of Probabilistic Geometry

### 2.1 Base space and probabilistic points

Let \((M,g)\) be a complete connected Riemannian manifold of dimension \(n\), with geodesic distance \(\rho\), volume measure \(d\operatorname{vol}_g\), Levi-Civita connection \(\nabla\), and Riemann curvature tensor \(R\). In local coordinates \(x^i\),

\[
g=g_{ij}\,dx^i\otimes dx^j,
\]

\[
R^{i}{}_{jkl}
=
\partial_k\Gamma^{i}_{lj}
-
\partial_l\Gamma^{i}_{kj}
+
\Gamma^{i}_{km}\Gamma^{m}_{lj}
-
\Gamma^{i}_{lm}\Gamma^{m}_{kj}.
\]

For \(p\ge 1\), let

\[
\mathcal P_p(M)
=
\left\{
P\in \mathcal P(M):
\int_M \rho(x,x_0)^p\,dP(x)<\infty
\text{ for some, hence any, }x_0\in M
\right\}.
\]

A **probabilistic point** is an element \(P\in\mathcal P_p(M)\). A deterministic point \(x\in M\) is recovered as \(\delta_x\).

---

### 2.2 Couplings and expected distance

For \(P,Q\in\mathcal P(M)\), let \(\Pi(P,Q)\) denote the set of couplings:

\[
\Pi(P,Q)
=
\left\{
\pi\in\mathcal P(M\times M):
(\operatorname{pr}_1)_\#\pi=P,\;
(\operatorname{pr}_2)_\#\pi=Q
\right\}.
\]

The primary Probabilistic Geometry distance is

\[
\boxed{
d(P,Q)
=
\inf_{\pi\in\Pi(P,Q)}
\mathbb E_{(X,Y)\sim\pi}
\bigl[\rho(X,Y)\bigr].
}
\]

Equivalently,

\[
d(P,Q)
=
\inf_{\pi\in\Pi(P,Q)}
\int_{M\times M}
\rho(x,y)\,d\pi(x,y).
\]

This is the first Wasserstein distance \(W_1(P,Q)\). More generally, for \(p\ge 1\), define

\[
d_p(P,Q)
=
\left(
\inf_{\pi\in\Pi(P,Q)}
\int_{M\times M}
\rho(x,y)^p\,d\pi(x,y)
\right)^{1/p}.
\]

The case \(p=1\) is the direct formalization of

\[
d(P,Q)=\mathbb E[\rho].
\]

The expectation is canonical only after optimal coupling. If a particular coupling \(\pi\) is fixed, we write

\[
d_\pi(P,Q)=\mathbb E_\pi[\rho(X,Y)].
\]

Then

\[
d(P,Q)=\inf_\pi d_\pi(P,Q).
\]

---

### 2.3 Kantorovich–Rubinstein dual representation

For \(P,Q\in\mathcal P_1(M)\),

\[
\boxed{
d(P,Q)
=
\sup_{\operatorname{Lip}(f)\le 1}
\left(
\int_M f\,dP-\int_M f\,dQ
\right).
}
\]

This dual form is often the most useful analytical representation. It exhibits PG distance as the maximal difference of expected observations over all unit-Lipschitz observables \(f\).

---

### 2.4 Metric axioms

We prove that \(d\) is a metric on \(\mathcal P_1(M)\).

#### Proposition 2.1

Let \((M,\rho)\) be a complete separable metric space. Then \(d=W_1\) is a metric on \(\mathcal P_1(M)\).

**Proof.**

Nonnegativity is immediate:

\[
d(P,Q)\ge 0.
\]

Symmetry follows from symmetry of \(\rho\):

\[
d(P,Q)
=
\inf_{\pi\in\Pi(P,Q)}
\int \rho(x,y)\,d\pi
=
\inf_{\pi\in\Pi(Q,P)}
\int \rho(y,x)\,d\pi
=
d(Q,P).
\]

For identity of indiscernibles, suppose \(d(P,Q)=0\). By the dual representation,

\[
\int f\,dP=\int f\,dQ
\]

for every \(1\)-Lipschitz function \(f\). Since bounded Lipschitz functions are convergence determining on a separable metric space, \(P=Q\).

For the triangle inequality, let \(P,Q,R\in\mathcal P_1(M)\). Choose \(\varepsilon>0\). Let \(\pi_{PQ}\in\Pi(P,Q)\) and \(\pi_{QR}\in\Pi(Q,R)\) be \(\varepsilon\)-optimal:

\[
\int \rho(x,y)\,d\pi_{PQ}(x,y)
\le d(P,Q)+\varepsilon,
\]

\[
\int \rho(y,z)\,d\pi_{QR}(y,z)
\le d(Q,R)+\varepsilon.
\]

By the gluing lemma, there exists \(\pi\in\mathcal P(M\times M\times M)\) with marginals \((X,Y)\sim\pi_{PQ}\) and \((Y,Z)\sim\pi_{QR}\). Then the marginal \((X,Z)_\#\pi\) couples \(P\) and \(R\). Hence

\[
\begin{aligned}
d(P,R)
&\le
\mathbb E[\rho(X,Z)]
\\
&\le
\mathbb E[\rho(X,Y)+\rho(Y,Z)]
\\
&=
\mathbb E[\rho(X,Y)]
+
\mathbb E[\rho(Y,Z)]
\\
&\le
d(P,Q)+d(Q,R)+2\varepsilon.
\end{aligned}
\]

Letting \(\varepsilon\to 0\) gives

\[
d(P,R)\le d(P,Q)+d(Q,R).
\]

Thus \(d\) is a metric. \(\square\)

---

### 2.5 Geodesic interpolation of probabilistic points

Assume now that \(M\) is a proper geodesic space. For each pair \((x,y)\in M\times M\), choose a constant-speed minimizing geodesic

\[
\gamma_{xy}:[0,1]\to M,
\qquad
\gamma_{xy}(0)=x,
\quad
\gamma_{xy}(1)=y,
\]

with

\[
\rho(\gamma_{xy}(s),\gamma_{xy}(t))
=
|t-s|\rho(x,y).
\]

Let \(\pi^\ast\in\Pi(P,Q)\) be an optimal coupling for \(d(P,Q)\). Define the interpolation map

\[
e_t(x,y)=\gamma_{xy}(t),
\]

and set

\[
P_t=(e_t)_\#\pi^\ast.
\]

Then \(P_0=P\), \(P_1=Q\).

#### Theorem 2.2

The curve \(t\mapsto P_t\) is a constant-speed geodesic in \((\mathcal P_1(M),d)\):

\[
d(P_s,P_t)=|t-s|d(P,Q).
\]

**Proof.**

For \(0\le s\le t\le 1\), the map

\[
(x,y)\longmapsto
(\gamma_{xy}(s),\gamma_{xy}(t))
\]

pushes \(\pi^\ast\) forward to a coupling of \(P_s\) and \(P_t\). Therefore

\[
\begin{aligned}
d(P_s,P_t)
&\le
\int
\rho(\gamma_{xy}(s),\gamma_{xy}(t))
\,d\pi^\ast(x,y)
\\
&=
(t-s)
\int
\rho(x,y)\,d\pi^\ast(x,y)
\\
&=
(t-s)d(P,Q).
\end{aligned}
\]

On the other hand, by the triangle inequality,

\[
d(P,Q)
\le
d(P,P_t)+d(P_t,Q)
\le
t d(P,Q)+(1-t)d(P,Q)
=
d(P,Q).
\]

Hence equality holds throughout, and

\[
d(P_s,P_t)=|t-s|d(P,Q).
\]

\(\square\)

This theorem formalizes the PG principle that a motion between probabilistic points is a **displacement interpolation** of possible pointwise motions.

---

## 3. Differential Structure

The metric \(d=d_1\) is Finsler-like. For a smooth tensorial calculus, it is convenient to use the quadratic theory \(d_2=W_2\) as the infinitesimal model while retaining \(d_1\) as the primary expected distance.

---

### 3.1 The \(L^2\) quotient picture

Let \((\Omega,\mathcal F,\mathbb P)\) be a standard probability space. Consider the space

\[
L^2(\Omega;M)
=
\left\{
X:\Omega\to M:
\mathbb E[\rho(X,x_0)^2]<\infty
\right\}.
\]

Two random variables \(X,Y\) represent the same probabilistic point if they have the same law:

\[
X\sim Y
\iff
X_\#\mathbb P=Y_\#\mathbb P.
\]

Thus

\[
\mathcal P_2(M)
\cong
L^2(\Omega;M)/\operatorname{MP}(\Omega),
\]

where \(\operatorname{MP}(\Omega)\) denotes the group of measure-preserving transformations of \(\Omega\).

A probabilistic point is therefore an equivalence class \([X]\). The distance is

\[
d_2([X],[Y])
=
\inf_{\varphi\in\operatorname{MP}(\Omega)}
\left(
\mathbb E[\rho(X,Y\circ\varphi)^2]
\right)^{1/2}.
\]

This quotient viewpoint explains the appearance of optimal transport: minimizing over couplings is equivalent to minimizing over measure-preserving rearrangements.

---

### 3.2 Tangent spaces

Let \(P\in\mathcal P_2(M)\) be absolutely continuous with respect to \(d\operatorname{vol}_g\). A tangent vector at \(P\) may be represented by a vector field \(v\) on \(M\), interpreted as an infinitesimal velocity of mass. The continuity equation governs admissible curves \(P_t\):

\[
\boxed{
\partial_t P_t+\nabla_i(P_t v_t^i)=0.
}
\]

In weak form,

\[
\frac{d}{dt}\int_M f\,dP_t
=
\int_M df(v_t)\,dP_t
\]

for all \(f\in C_c^\infty(M)\).

For the quadratic PG structure, the tangent space is the \(L^2(P)\)-closure of gradient fields:

\[
T_P\mathcal P_2(M)
=
\overline{
\left\{
\nabla \phi:\phi\in C_c^\infty(M)
\right\}
}^{L^2(P)}.
\]

The PG Riemannian metric tensor is

\[
\boxed{
G_P(v,w)
=
\int_M g_{ij}(x)v^i(x)w^j(x)\,dP(x).
}
\]

For \(v=\nabla\phi\) and \(w=\nabla\psi\),

\[
G_P(v,w)
=
\int_M
g^{ij}\partial_i\phi\,\partial_j\psi
\,dP.
\]

---

### 3.3 Benamou–Brenier dynamical formulation

The quadratic distance admits the dynamical variational formula

\[
\boxed{
d_2(P_0,P_1)^2
=
\inf_{\substack{
\partial_t P_t+\nabla_i(P_t v_t^i)=0\\
P_0=P,\;P_1=Q
}}
\int_0^1
\int_M
|v_t(x)|^2\,dP_t(x)\,dt.
}
\]

The corresponding first-order distance is

\[
\boxed{
d(P_0,P_1)
=
\inf
\int_0^1
\int_M
|v_t(x)|\,dP_t(x)\,dt.
}
\]

This is the dynamical form of \(d=\mathbb E[\rho]\). It exhibits \(d\) as the minimal expected length of a stochastic flow of points.

---

### 3.4 Geodesic equations

Introduce the action

\[
S[P,v]
=
\frac12
\int_0^1
\int_M
|v_t|^2\,dP_t\,dt
\]

subject to

\[
\partial_t P_t+\nabla_i(P_t v_t^i)=0.
\]

Using a Lagrange multiplier \(\phi_t\), consider

\[
\mathcal L
=
\frac12
\int_0^1\int_M
|v_t|^2\,dP_t\,dt
+
\int_0^1\int_M
\phi_t
\bigl(
\partial_t P_t+\nabla_i(P_t v_t^i)
\bigr)
\,dt.
\]

Variation with respect to \(v\) gives

\[
v_t^i=g^{ij}\partial_j\phi_t.
\]

Variation with respect to \(\phi\) gives the continuity equation:

\[
\partial_t P_t+\nabla_i(P_t\nabla^i\phi_t)=0.
\]

The characteristics of this system are geodesics in \(M\). The potential satisfies the Hamilton–Jacobi equation

\[
\boxed{
\partial_t\phi_t
+
\frac12
|\nabla\phi_t|^2
=
0.
}
\]

Thus a PG geodesic is a continuity-equation flow driven by a Hamilton–Jacobi potential. In coordinates,

\[
\partial_t P_t
+
g^{ij}\partial_i P_t\,\partial_j\phi_t
+
P_t\nabla_i\nabla^i\phi_t
=
0.
\]

For the primary expected distance \(d=d_1\), the corresponding variational problem yields the eikonal constraint

\[
|\nabla\phi|\le 1,
\]

and optimal potentials are Kantorovich potentials satisfying the dual Lipschitz constraint.

---

### 3.5 Probabilistic barycenters

For \(P\in\mathcal P_2(M)\), define the Fréchet functional

\[
F_P(y)
=
\frac12
\int_M
\rho(x,y)^2\,dP(x).
\]

A **probabilistic barycenter** is a minimizer

\[
b(P)\in\operatorname*{argmin}_{y\in M}F_P(y).
\]

If \(M\) is Hadamard, i.e. complete, simply connected, and of nonpositive sectional curvature, then \(b(P)\) exists and is unique.

The first variation gives the Karcher equation:

\[
\boxed{
\int_M
\exp_{b}^{-1}(x)\,dP(x)=0.
}
\]

In normal coordinates centered at \(b\), writing \(x=\exp_b(z)\), this becomes

\[
\int_M z^i\,dP(z)
+
\frac12
\Gamma^i_{jk}(b)
\int_M z^jz^k\,dP(z)
+
O(|z|^3)
=
0.
\]

Thus the barycenter is not merely the coordinate mean; it is the mean corrected by the connection.

The barycentric tangent covariance is

\[
\Sigma_P
=
\int_M
\exp_b^{-1}(x)\otimes \exp_b^{-1}(x)
\,dP(x).
\]

In components,

\[
(\Sigma_P)^{ij}
=
\int_M z^i z^j\,dP(z).
\]

This covariance will control curvature corrections.

---

## 4. Expectation-Valued Curvature

Classical curvature is pointwise:

\[
R_x:T_xM\times T_xM\times T_xM\to T_xM.
\]

In PG, a probabilistic point \(P\) has no single tangent space. We therefore transport local curvature tensors to a common barycentric tangent space and integrate.

---

### 4.1 Parallel transport to the barycenter

Assume \(P\) is supported in a strongly convex normal neighborhood of its barycenter \(b=b(P)\). For each \(x\) in the support of \(P\), let

\[
\tau_{x\to b}:T_xM\to T_bM
\]

denote parallel transport along the unique minimizing geodesic from \(x\) to \(b\). Let

\[
\Lambda^{a}{}_{i}(x)
\]

be the components of \(\tau_{x\to b}\), and let

\[
\Lambda^{i}{}_{a}(x)
\]

be the components of the inverse transport \(\tau_{b\to x}\). Thus

\[
\Lambda^{a}{}_{i}\Lambda^{i}{}_{b}=\delta^{a}_{b},
\qquad
\Lambda^{i}{}_{a}\Lambda^{a}{}_{j}=\delta^{i}_{j}.
\]

Parallel transport preserves the metric:

\[
g_{ab}(b)
=
\Lambda^{i}{}_{a}\Lambda^{j}{}_{b}g_{ij}(x).
\]

---

### 4.2 The probabilistic Riemann tensor

Define the **expected Riemann curvature tensor** at \(P\) by

\[
\boxed{
\mathcal R^{a}{}_{bcd}(P)
=
\int_M
\Lambda^{a}{}_{i}(x)
\Lambda^{j}{}_{b}(x)
\Lambda^{k}{}_{c}(x)
\Lambda^{l}{}_{d}(x)
R^{i}{}_{jkl}(x)
\,dP(x).
}
\]

Equivalently, as an operator on \(T_bM\),

\[
\mathcal R_P(U,V)W
=
\int_M
\tau_{x\to b}
\left[
R_x
\left(
\tau_{b\to x}U,
\tau_{b\to x}V
\right)
\tau_{b\to x}W
\right]
\,dP(x).
\]

The fully covariant tensor is

\[
\mathcal R_{abcd}(P)
=
g_{ae}(b)\mathcal R^{e}{}_{bcd}(P).
\]

Because parallel transport is an isometry, the algebraic symmetries of \(R\) are preserved under integration:

\[
\mathcal R_{abcd}=-\mathcal R_{bacd},
\]

\[
\mathcal R_{abcd}=-\mathcal R_{abdc},
\]

\[
\mathcal R_{abcd}=\mathcal R_{cdab},
\]

\[
\mathcal R_{a[bcd]}=0.
\]

Thus \(\mathcal R_P\) is a genuine curvature tensor at the probabilistic point \(P\).

---

### 4.3 Expected Ricci and scalar curvature

Contracting the expected Riemann tensor gives the **expected Ricci tensor**:

\[
\boxed{
\mathcal{Ric}_{ab}(P)
=
\mathcal R^{c}{}_{acb}(P).
}
\]

Equivalently,

\[
\mathcal{Ric}_{ab}(P)
=
\int_M
\Lambda^{i}{}_{a}(x)
\Lambda^{j}{}_{b}(x)
\operatorname{Ric}_{ij}(x)
\,dP(x).
\]

The **expected scalar curvature** is

\[
\boxed{
\mathcal S(P)
=
g^{ab}(b)\mathcal{Ric}_{ab}(P)
=
\int_M S(x)\,dP(x),
}
\]

where \(S=g^{ij}\operatorname{Ric}_{ij}\) is the scalar curvature of \(M\).

Thus scalar curvature becomes the ordinary expectation of scalar curvature under the probabilistic point.

---

### 4.4 Expected sectional curvature

For a two-plane \(\sigma=\operatorname{span}\{U,V\}\subset T_bM\), define

\[
|U\wedge V|^2
=
g(U,U)g(V,V)-g(U,V)^2.
\]

The **expected sectional curvature** is

\[
\boxed{
\mathcal K_P(U,V)
=
\frac{
\mathcal R_{abcd}(P)U^aV^bV^cU^d
}{
|U\wedge V|^2
}.
}
\]

Equivalently,

\[
\mathcal K_P(U,V)
=
\int_M
K_x
\left(
\tau_{b\to x}U,
\tau_{b\to x}V
\right)
\,dP(x),
\]

where \(K_x\) is the sectional curvature of the transported plane at \(x\).

This is the direct curvature analogue of

\[
d(P,Q)=\mathbb E[\rho].
\]

Distance is expected distance; curvature is expected curvature.

---

### 4.5 Intrinsic curvature of the probabilistic geometry

The preceding tensor measures the expected curvature of the base manifold as seen by \(P\). The space \(\mathcal P_2(M)\) itself also possesses intrinsic curvature. We now relate the two.

Let \(U=\nabla\phi\) and \(V=\nabla\psi\) be horizontal tangent vectors at \(P\). Their global PG inner product is

\[
G_P(U,V)
=
\int_M g(U,V)\,dP.
\]

Define the global wedge norm

\[
\|U\wedge V\|_{G}^2
=
G_P(U,U)G_P(V,V)-G_P(U,V)^2.
\]

The \(L^2\) lift of the base curvature gives

\[
K^{L^2}(U,V)
=
\frac{
\int_M
K_M(U,V)
|U\wedge V|_x^2
\,dP(x)
}{
\|U\wedge V\|_{G}^2
}.
\]

The quotient by measure-preserving transformations contributes a vertical correction. Let

\[
A_UV
=
\left(
\nabla^{L^2}_U V
\right)^{\mathrm{vert}}
\]

be the vertical part of the \(L^2\) covariant derivative. In the Wasserstein quotient, this is the O’Neill tensor. Then the intrinsic PG sectional curvature satisfies the formal decomposition

\[
\boxed{
K_{\mathrm{PG}}(U,V)
=
K^{L^2}(U,V)
+
3
\frac{
G_P(A_UV,A_UV)
}{
\|U\wedge V\|_{G}^2
}.
}
\]

The second term is nonnegative. Therefore the intrinsic curvature of probabilistic geometry contains:

1. an **expected base curvature** term;
2. a **transport curvature** term generated by rearrangement of probability mass.

In particular, even when \(M=\mathbb R^n\) has zero curvature, \(\mathcal P_2(\mathbb R^n)\) has nonnegative intrinsic curvature due to transport.

---

### 4.6 Probabilistic Gauss–Bonnet excess

Let \(X_1,X_2,X_3\) be random points with laws \(P_1,P_2,P_3\), coupled by a measure \(\pi\) on \(M^3\). For each realization \((x_1,x_2,x_3)\), assume the points lie in a strongly convex ball and form a geodesic triangle \(\Delta(x_1,x_2,x_3)\). Let \(\alpha_i\) be its interior angles. The classical Gauss–Bonnet theorem gives

\[
\alpha_1+\alpha_2+\alpha_3-\pi
=
\int_{\Delta(x_1,x_2,x_3)}
K\,dA.
\]

Taking expectation,

\[
\boxed{
\mathbb E
\left[
\alpha_1+\alpha_2+\alpha_3-\pi
\right]
=
\int_M
K(x)\,\nu_\Delta(dx),
}
\]

where the **expected area measure** is

\[
\nu_\Delta(A)
=
\mathbb E
\left[
\operatorname{Area}
\bigl(
\Delta(X_1,X_2,X_3)\cap A
\bigr)
\right].
\]

If the triangle is small and its expected area measure satisfies

\[
\nu_\Delta
=
A_0\,\overline P
+
O(\varepsilon^3),
\]

where

\[
\overline P
=
\frac13(P_1+P_2+P_3),
\]

then

\[
\boxed{
\mathbb E
\left[
\alpha_1+\alpha_2+\alpha_3-\pi
\right]
=
A_0\,
\mathcal K_{\overline P}(\sigma)
+
O(\varepsilon^3).
}
\]

Thus angle excess becomes expected angle excess, controlled by expected sectional curvature.

---

### 4.7 Synthetic Ricci curvature and displacement convexity

Let \(M\) be complete and let \(P_t\) be a \(W_2\)-geodesic in \(\mathcal P_2(M)\), absolutely continuous with respect to volume:

\[
P_t=\rho_t\,d\operatorname{vol}_g.
\]

Define the Boltzmann entropy

\[
H(P)
=
\int_M
\rho\log\rho\,d\operatorname{vol}_g.
\]

If the base manifold satisfies

\[
\operatorname{Ric}_M\ge \kappa g,
\]

then along every \(W_2\)-geodesic,

\[
\boxed{
H(P_t)
\le
(1-t)H(P_0)+tH(P_1)
-
\frac{\kappa}{2}
t(1-t)
d_2(P_0,P_1)^2.
}
\]

This is the synthetic expression of expectation-valued Ricci curvature. Positive Ricci lower bounds make entropy displacement-convex; negative bounds quantify displacement concavity.

---

## 5. Structural Results

### 5.1 Completeness

#### Theorem 5.1

If \((M,\rho)\) is complete and separable, then \((\mathcal P_p(M),d_p)\) is complete for every \(p\ge 1\). If \(M\) is proper and geodesic, then \((\mathcal P_p(M),d_p)\) is geodesic.

For \(p=1\), this gives completeness and geodesicity of the primary PG metric space.

---

### 5.2 Convergence

A sequence \(P_k\in\mathcal P_p(M)\) converges to \(P\) in \(d_p\) if and only if:

1. \(P_k\) converges weakly to \(P\);
2. the \(p\)-th moments converge:

\[
\int_M \rho(x,x_0)^p\,dP_k(x)
\to
\int_M \rho(x,x_0)^p\,dP(x).
\]

Thus PG convergence is narrow convergence plus moment convergence.

---

### 5.3 Small-covariance curvature expansion

Let \(P\) be concentrated near \(b\) and write

\[
P=(\exp_b)_\# Q,
\]

where \(Q\) is a probability measure on \(T_bM\) with mean zero and covariance

\[
\Sigma^{ij}
=
\int_{T_bM} z^i z^j\,dQ(z).
\]

Assume \(\Sigma=O(\varepsilon^2)\). Then the expected curvature tensor admits an expansion

\[
\boxed{
\mathcal R_{abcd}(P)
=
R_{abcd}(b)
+
\frac12
\Sigma^{ij}
\nabla_i\nabla_j R_{abcd}(b)
+
\Sigma^{ij}
C_{abcd,ij}(R_b)
+
O(\varepsilon^3).
}
\]

Here \(C_{abcd,ij}(R_b)\) is a universal algebraic expression quadratic in the curvature tensor, arising from the Taylor expansion of parallel transport. Schematically,

\[
C(R)\sim R\ast R.
\]

Thus a probabilistic point sees not only the curvature at its barycenter but also curvature gradients and curvature fluctuations weighted by its covariance.

For scalar curvature,

\[
\boxed{
\mathcal S(P)
=
S(b)
+
\frac12
\Sigma^{ij}
\nabla_i\nabla_j S(b)
+
O(\varepsilon^3).
}
\]

---

### 5.4 Expected distance between nearby probabilistic points

Let \(P\) and \(Q\) be concentrated near \(b\), with barycentric tangent means \(m_P,m_Q\in T_bM\) and covariances \(\Sigma_P,\Sigma_Q\). To leading order,

\[
d_2(P,Q)^2
=
\|m_P-m_Q\|^2
+
\operatorname{tr}
\left(
\Sigma_P+\Sigma_Q
-
2(\Sigma_P^{1/2}\Sigma_Q\Sigma_P^{1/2})^{1/2}
\right)
+
O(\varepsilon^3).
\]

This is the Bures–Wasserstein local expansion. For the primary expected distance \(d=d_1\), one has the comparison

\[
d(P,Q)\le d_2(P,Q),
\]

and in one dimension or for comonotone couplings the two are closely related through moment data.

---

## 6. Applications

---

### 6.1 Machine learning

In classical representation learning, a model maps inputs to points:

\[
f_\theta:\mathcal X\to M.
\]

In Probabilistic Geometry, one instead learns a distribution-valued map

\[
F_\theta:\mathcal X\to \mathcal P(M).
\]

For example,

\[
F_\theta(x)=\mathcal N(m_\theta(x),\Sigma_\theta(x))
\]

on a Riemannian feature manifold.

A PG training loss may be written as

\[
\boxed{
\mathcal L(\theta)
=
\mathbb E_{(x,y)}
\left[
d\bigl(F_\theta(x),F_\theta(y)\bigr)
\right]
+
\lambda
\mathbb E_x
\left[
D_{\mathrm{KL}}
\bigl(
F_\theta(x)\,\|\,\Pi
\bigr)
\right]
+
\mu
\Omega_{\mathrm{curv}}(\theta).
}
\]

Here \(d\) is the expected PG distance, \(\Pi\) is a prior distribution on \(\mathcal P(M)\), and \(\Omega_{\mathrm{curv}}\) is a curvature regularizer.

A natural curvature regularizer is

\[
\Omega_{\mathrm{curv}}(\theta)
=
\mathbb E_x
\left[
\max
\left(
0,
-\mathcal{Ric}_{F_\theta(x)}(v,v)
\right)
\right],
\]

which penalizes regions of negative expected Ricci curvature that can cause exponential volume expansion and instability.

The PG natural gradient is defined by

\[
\dot\theta
=
-
\mathcal G_{\mathrm{PG}}(\theta)^{-1}
\nabla_\theta \mathcal L,
\]

where the PG parameter metric is

\[
\mathcal G_{\mathrm{PG},ab}
=
\mathbb E_{z\sim F_\theta(x)}
\left[
g_{ij}(z)
\frac{\partial m^i}{\partial\theta^a}
\frac{\partial m^j}{\partial\theta^b}
\right]
+
\mathcal G^{\Sigma}_{ab}
+
\mathcal G^{\mathrm{trans}}_{ab}.
\]

The term \(\mathcal G^{\Sigma}\) measures covariance uncertainty, while \(\mathcal G^{\mathrm{trans}}\) accounts for optimal-transport rearrangement.

For Gaussian probabilistic embeddings in Euclidean space, the quadratic PG distance has the explicit Bures form

\[
d_2(P,Q)^2
=
\|m_P-m_Q\|^2
+
\operatorname{tr}
\left(
\Sigma_P+\Sigma_Q
-
2(\Sigma_P^{1/2}\Sigma_Q\Sigma_P^{1/2})^{1/2}
\right).
\]

This provides a principled uncertainty-aware metric for latent variables.

---

### 6.2 Robotics

In robotics, the configuration space is often a Lie group such as

\[
C=SE(3).
\]

A robot belief is not a configuration \(q\in C\), but a distribution \(B\in\mathcal P(C)\). PG provides a geometric theory of belief-space planning.

The expected length of a belief trajectory \(B_t\) is

\[
L_{\mathrm{PG}}(B_t)
=
\int_0^T
\int_C
|v_t(x)|\,dB_t(x)\,dt,
\]

subject to

\[
\partial_t B_t+\nabla_i(B_t v_t^i)=0.
\]

A risk-sensitive planning problem is

\[
\boxed{
\inf_{B_t,v_t}
\int_0^T
\left[
\int_C
\left(
\frac12|v_t(x)|^2
+
V_{\mathrm{obs}}(x)
\right)
dB_t(x)
\right]dt.
}
\]

The Euler–Lagrange equations are

\[
\partial_t B_t+\nabla_i(B_t\nabla^i\phi_t)=0,
\]

\[
\partial_t\phi_t
+
\frac12|\nabla\phi_t|^2
+
V_{\mathrm{obs}}
=
0.
\]

Thus belief-space geodesics are Hamilton–Jacobi flows over probability.

Uncertainty propagation is governed by Jacobi fields. If \(J\) is a separation vector between nearby trajectories, then

\[
\frac{D^2J}{dt^2}
+
R(J,\dot\gamma)\dot\gamma
=
0.
\]

Taking expectations gives the PG Jacobi equation

\[
\boxed{
\mathbb E
\left[
\frac{D^2J}{dt^2}
\right]
+
\mathcal R_P(\mathbb E[J],\dot\gamma)\dot\gamma
+
\text{covariance corrections}
=
0.
}
\]

Thus expected curvature controls the focusing or dispersion of belief trajectories.

---

### 6.3 Statistics

Let \(X_1,\dots,X_N\in M\) be manifold-valued data. The Fréchet mean is

\[
\bar x
=
\operatorname*{argmin}_{y\in M}
\frac1N
\sum_{r=1}^N
\rho(X_r,y)^2.
\]

In PG language, the empirical probabilistic point is

\[
P_N
=
\frac1N
\sum_{r=1}^N
\delta_{X_r}.
\]

Its barycenter is \(b(P_N)=\bar x\). The empirical expected curvature tensor is

\[
\boxed{
\widehat{\mathcal R}^{a}{}_{bcd}
=
\frac1N
\sum_{r=1}^N
\Lambda^{a}{}_{i}(X_r)
\Lambda^{j}{}_{b}(X_r)
\Lambda^{k}{}_{c}(X_r)
\Lambda^{l}{}_{d}(X_r)
R^{i}{}_{jkl}(X_r).
}
\]

This estimator is tensorially coherent because all summands live in \(T_{\bar x}M\).

The tangent covariance is

\[
\widehat\Sigma^{ij}
=
\frac1N
\sum_{r=1}^N
z_r^i z_r^j,
\qquad
z_r=\exp_{\bar x}^{-1}(X_r).
\]

For small variance, the expected squared distance between two independent draws \(X,Y\sim P\) satisfies

\[
\boxed{
\mathbb E[\rho(X,Y)^2]
=
2\operatorname{tr}\Sigma
-
\frac13
R_{ikjl}
\Sigma^{ij}\Sigma^{kl}
+
O(\|\Sigma\|^3).
}
\]

Thus curvature produces a second-order correction to statistical dispersion. Positive sectional curvature reduces expected pairwise distance; negative curvature increases it.

This yields curvature-corrected confidence regions. The volume of a small PG ball of radius \(r\) around \(P\) has expansion

\[
\operatorname{Vol}_{\mathrm{PG}}(B_r(P))
=
\omega_N r^N
\left(
1
-
\frac{\mathcal S(P)}{6(N+2)}
r^2
+
O(r^4)
\right).
\]

Thus expected scalar curvature directly controls local probabilistic volume growth.

---

### 6.4 Quantum theory

Let \(\mathcal H\) be a finite-dimensional Hilbert space. Pure quantum states form the complex projective space

\[
\mathbb{CP}^{n-1},
\]

equipped with the Fubini–Study metric \(g_{\mathrm{FS}}\). With standard normalization, its sectional curvature is constant:

\[
K_{\mathrm{FS}}=4.
\]

A mixed state is a density matrix

\[
\rho\ge 0,
\qquad
\operatorname{Tr}\rho=1.
\]

In PG, \(\rho\) may be interpreted as a probabilistic point over pure states. One possible induced measure is the normalized Husimi-type distribution

\[
q_\rho([\psi])
=
n\langle\psi|\rho|\psi\rangle
\,d\mu_{\mathrm{FS}}([\psi]).
\]

The expected Fubini–Study curvature is then

\[
\mathcal K_Q(\rho)
=
\int_{\mathbb{CP}^{n-1}}
K_{\mathrm{FS}}
\,q_\rho([\psi])
=
4.
\]

However, mixedness contributes additional geometric structure through the Bures–Wasserstein metric. For density matrices \(\rho,\sigma\), define

\[
\boxed{
d_{\mathrm{BW}}(\rho,\sigma)^2
=
\operatorname{Tr}\rho
+
\operatorname{Tr}\sigma
-
2\operatorname{Tr}
\left[
(\rho^{1/2}\sigma\rho^{1/2})^{1/2}
\right].
}
\]

If \(\rho\) has spectral decomposition

\[
\rho=\sum_i\lambda_i |i\rangle\langle i|,
\]

the infinitesimal Bures metric is

\[
\boxed{
g_B(\delta\rho,\delta\rho)
=
\frac12
\sum_{i,j:\lambda_i+\lambda_j>0}
\frac{
|\langle i|\delta\rho|j\rangle|^2
}{
\lambda_i+\lambda_j
}.
}
\]

This metric combines:

1. unitary motion on pure-state fibers;
2. classical probability motion on the eigenvalue simplex.

The corresponding quantum PG curvature decomposes as

\[
\boxed{
\mathcal R_Q(\rho)
=
\mathcal R_{\mathrm{FS}}(\rho)
+
\mathcal R_{\mathrm{spec}}(\rho)
+
\mathcal R_{\mathrm{hol}}(\rho).
}
\]

Here:

- \(\mathcal R_{\mathrm{FS}}\) is the expected Fubini–Study curvature;
- \(\mathcal R_{\mathrm{spec}}\) is the curvature of the eigenvalue distribution;
- \(\mathcal R_{\mathrm{hol}}\) is a holonomy term arising from the Uhlmann connection.

Quantum natural gradient descent uses the Bures metric:

\[
\dot\rho
=
-
G_B(\rho)^{-1}
\nabla_\rho \mathcal L.
\]

PG interprets this as gradient flow on the space of quantum probabilistic points, where uncertainty is geometric rather than merely statistical.

---

## 7. Conclusion

Probabilistic Geometry replaces the classical point \(x\) by a law \(P\), the classical distance \(\rho(x,y)\) by an optimal expected distance \(\mathbb E[\rho]\), and the pointwise curvature tensor \(R_x\) by an expectation-valued tensor \(\mathcal R_P\). The resulting framework is not a mere probabilization of geometry; it is a new geometric category in which uncertainty is constitutive.

The central objects are:

\[
\boxed{
\text{point} \leadsto P\in\mathcal P(M),
}
\]

\[
\boxed{
\text{distance} \leadsto d(P,Q)=\inf_{\pi}\mathbb E_\pi[\rho],
}
\]

\[
\boxed{
\text{curvature} \leadsto
\mathcal R_P
=
\int_M
\tau_{x\to b}R_x\tau_{b\to x}\,dP(x).
}
\]

The theory unifies several domains:

- optimal transport provides the metric and geodesic structure;
- Riemannian geometry provides curvature and parallel transport;
- statistics provides barycenters and covariance;
- machine learning provides distributional representations;
- robotics provides belief-space dynamics;
- quantum theory provides noncommutative probabilistic geometry.

The central thesis is therefore:

\[
\boxed{
\text{Geometry under uncertainty is not geometry plus noise; it is geometry itself.}
}
\]

---

## References

1. Ambrosio, L., Gigli, N., & Savaré, G. (2005). *Gradient Flows in Metric Spaces and in the Space of Probability Measures*. Birkhäuser.

2. Bengtsson, I., & Życzkowski, K. (2006). *Geometry of Quantum States: An Introduction to Quantum Entanglement*. Cambridge University Press.

3. Bures, D. (1969). An extension of Kakutani’s theorem on infinite product measures to the non-commutative case. *Transactions of the American Mathematical Society*, 135, 199–212.

4. Fréchet, M. (1948). Les éléments aléatoires de nature quelconque dans un espace distancé. *Annales de l’Institut Henri Poincaré*, 10, 215–310.

5. Kantorovich, L. V., & Rubinstein, G. S. (1958). On a space of totally additive functions. *Vestnik Leningrad University*, 13, 52–59.

6. Karcher, H. (1977). Riemannian center of mass and mollifier smoothing. *Communications on Pure and Applied Mathematics*, 30, 509–541.

7. Lott, J. (2008). Some geometric calculations based on the Wasserstein metric. *Journal of Functional Analysis*, 255, 285–320.

8. McCann, R. J. (1995). Polar factorization of maps on Riemannian manifolds. *Geometric and Functional Analysis*, 5, 589–608.

9. Otto, F. (2001). The geometry of dissipative evolution equations: The porous medium equation. *Communications in Partial Differential Equations*, 26, 101–174.

10. Sturm, K.-T. (2006). On the geometry of metric measure spaces I. *Acta Mathematica*, 196, 65–131.

11. Sturm, K.-T. (2006). On the geometry of metric measure spaces II. *Acta Mathematica*, 196, 133–177.

12. Villani, C. (2003). *Topics in Optimal Transportation*. American Mathematical Society.

13. Villani, C. (2009). *Optimal Transport: Old and New*. Springer.

14. Villani, C. (2016). Synthetic Theory of Ricci Curvature Bounds. In *Optimal Transportation and its Applications*. Springer.

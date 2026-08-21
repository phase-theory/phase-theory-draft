# Recursive Information Geometry II  
## Information Operators and the Evolution of Statistical Manifolds

**Preprint**

---

## Abstract

We develop **Recursive Information Geometry II (RIG-II)**, a framework in which statistical manifolds are not fixed background structures but evolve through discrete information flows. In classical information geometry, a statistical model is equipped with a Fisher–Rao metric, dual connections, and higher-order tensors. RIG-II promotes these objects to dynamical variables. The central recursion is

\[
g_{n+1}=\mathcal{I}(g_n),
\]

where \(\mathcal{I}\) is an information operator acting on the space of Riemannian metrics compatible with statistical structure. We formulate axioms for such operators, construct canonical probabilistic and intrinsic geometric realizations, analyze fixed points and stability, derive the continuous limit as an information-geometric flow, and study the induced recursion for curvature, dual connections, and cubic tensors. Applications are developed in Bayesian inference, machine learning, quantum information, and statistical physics. In particular, we show how recursive information geometry provides a unifying language for adaptive natural gradient descent, posterior concentration, quantum channel contraction, and renormalization-group flow.

**Keywords:** information geometry, Fisher metric, recursive learning, statistical manifolds, renormalization, quantum information, natural gradient, Bayesian inference.

---

## 1. Introduction

Classical information geometry studies a parametric statistical model as a differentiable manifold \(M\) endowed with canonical geometric structures. Given a family of probability densities or mass functions \(p(x;\theta)\), \(\theta=(\theta^1,\dots,\theta^d)\), one obtains the Fisher metric

\[
g_{ij}(\theta)
=
\mathbb{E}_{p(\cdot;\theta)}
\left[
\partial_i \log p(X;\theta)\,
\partial_j \log p(X;\theta)
\right],
\]

together with a family of dual affine connections \(\nabla^{(\alpha)}\) and a cubic tensor \(C_{ijk}\). These structures encode the infinitesimal distinguishability of nearby probability distributions and provide a coordinate-invariant language for statistical inference.

In most treatments, however, the statistical manifold is regarded as fixed. The parameters may move, estimators may evolve, and distributions may be updated, but the underlying information geometry is static. This is insufficient for many modern problems in which the model itself is transformed by the flow of information:

1. In machine learning, repeated optimization changes not only the parameter estimate but also the local curvature and conditioning of the statistical model.
2. In Bayesian inference, sequential updating changes posterior geometry, often converting a diffuse prior into a sharply concentrated posterior.
3. In quantum information, noisy channels and measurements monotonically contract distinguishability metrics.
4. In statistical physics, coarse-graining produces a sequence of effective theories whose information geometry changes under renormalization.

RIG-II formalizes this phenomenon by allowing the statistical manifold to evolve recursively. The fundamental object is a sequence of metrics

\[
g_0,\; g_1,\; g_2,\;\dots
\]

satisfying

\[
g_{n+1}=\mathcal{I}(g_n),
\]

where \(\mathcal{I}\) is an information operator. More generally, the full recursive system may involve connections and higher tensors,

\[
(g_{n+1},\nabla_{n+1},C_{n+1})
=
\mathcal{I}(g_n,\nabla_n,C_n),
\]

but when the recursion closes on metrics one obtains the pure RIG-II equation above.

The purpose of this paper is to give a systematic foundation for RIG-II. We introduce axioms for information operators, construct canonical examples, derive the associated continuous flows, analyze fixed points, and develop applications.

---

## 2. Preliminaries: Statistical Manifolds and Fisher Geometry

Let \((\mathcal{X},\mu)\) be a measure space and let

\[
p_\theta(x)=p(x;\theta),\qquad \theta\in M\subset \mathbb{R}^d,
\]

be a smooth parametric statistical model. We assume regularity conditions permitting interchange of differentiation and integration. Define the log-likelihood

\[
\ell(\theta;x)=\log p(x;\theta).
\]

The score vector field is

\[
s_i(\theta;x)=\partial_i \ell(\theta;x).
\]

Because \(\int p(x;\theta)\,d\mu(x)=1\), one has

\[
\mathbb{E}_\theta[s_i]=0.
\]

The Fisher metric is the covariance of the score:

\[
g_{ij}(\theta)
=
\mathbb{E}_\theta[s_i s_j]
=
\int p(x;\theta)\,
\partial_i \ell\,\partial_j \ell\,
d\mu(x).
\]

Equivalently, under standard regularity,

\[
g_{ij}(\theta)
=
-\mathbb{E}_\theta[\partial_i\partial_j \ell].
\]

The Fisher metric is the unique monotone Riemannian metric on statistical manifolds up to scale, in the sense of Chentsov.

The cubic tensor is

\[
C_{ijk}(\theta)
=
\mathbb{E}_\theta[s_i s_j s_k].
\]

It measures the skewness of the score and governs the departure from Euclidean behavior. The \(\alpha\)-connections are given by

\[
\Gamma^{(\alpha)}_{ij,k}
=
\mathbb{E}_\theta
[
\partial_i\partial_j \ell\,
\partial_k \ell
]
+
\frac{\alpha}{2}
C_{ijk}.
\]

The connections \(\nabla^{(\alpha)}\) and \(\nabla^{(-\alpha)}\) are dual with respect to \(g\). The Levi-Civita connection corresponds to \(\alpha=0\).

A statistical manifold is therefore a tuple

\[
(M,g,\nabla^{(\alpha)},C),
\]

with compatibility conditions between the metric, connections, and cubic tensor. RIG-II studies recursive transformations of this structure.

---

## 3. Recursive Information Geometry: Basic Definitions

### 3.1 RIG-II systems

Let \(\operatorname{Met}_+(M)\) denote the space of smooth positive-definite symmetric \((0,2)\)-tensor fields on \(M\). A **recursive information geometry of type II** is a sequence of statistical structures

\[
\mathcal{S}_n=(M,g^{(n)},\nabla^{(n)},C^{(n)})
\]

together with an information operator

\[
\mathcal{I}_n:
\operatorname{Met}_+(M)\times \mathcal{A}(M)\times \mathcal{T}^3(M)
\to
\operatorname{Met}_+(M)
\]

such that

\[
g^{(n+1)}=\mathcal{I}_n(g^{(n)},\nabla^{(n)},C^{(n)}).
\]

When the recursion is autonomous and closes on metrics, we write

\[
g^{(n+1)}=\mathcal{I}(g^{(n)}).
\]

This is the central RIG-II equation.

### 3.2 Information operators

An information operator should not be an arbitrary map on metrics. To be information-geometrically meaningful, it should satisfy several structural principles.

Let \(\phi:M\to M\) be a diffeomorphism. The pullback metric is

\[
(\phi^*g)_{ij}
=
\frac{\partial \phi^a}{\partial \theta^i}
\frac{\partial \phi^b}{\partial \theta^j}
g_{ab}\circ \phi.
\]

We impose the following axioms.

#### Axiom 1: Positivity

\[
g\in \operatorname{Met}_+(M)
\quad\Longrightarrow\quad
\mathcal{I}(g)\in \operatorname{Met}_+(M).
\]

The recursion must preserve positive definiteness.

#### Axiom 2: Diffeomorphism covariance

\[
\mathcal{I}(\phi^*g)=\phi^*\mathcal{I}(g).
\]

The recursion is coordinate invariant.

#### Axiom 3: Markov monotonicity

Let \(\kappa:\mathcal{X}\to \mathcal{Y}\) be a Markov kernel. It induces a statistical map \(F_\kappa\) on Fisher metrics. Chentsov monotonicity gives

\[
F_\kappa(g)\le g
\]

in the Loewner order. An information operator compatible with data processing should satisfy

\[
\mathcal{I}(F_\kappa(g))
\le
F_\kappa(\mathcal{I}(g))
\]

or, in coarse-graining models,

\[
\mathcal{I}(g)=F_\kappa(g).
\]

This expresses the principle that information cannot increase under stochastic forgetting.

#### Axiom 4: Dissipation of an information potential

There should exist a functional \(\Phi\) on metrics such that

\[
\Phi(g_{n+1})\le \Phi(g_n).
\]

Typical candidates include relative entropy, Fisher trace, scalar curvature functionals, or cubic-norm functionals.

#### Axiom 5: Local smoothness

For small step size \(\varepsilon>0\),

\[
\mathcal{I}_\varepsilon(g)
=
g+\varepsilon D[g]+O(\varepsilon^2),
\]

where \(D[g]\) is a symmetric \((0,2)\)-tensor depending locally or semi-locally on \(g\) and its derivatives.

This axiom allows a continuous limit.

---

## 4. Probabilistic Information Operators

A natural class of RIG-II operators arises by deforming the statistical model itself.

Let \(p_n(x;\theta)\) be the model at step \(n\). Choose a potential \(V_n(x)\) and define

\[
p_{n+1}(x;\theta)
=
\frac{
p_n(x;\theta)\,
e^{-\varepsilon V_n(x)}
}{
Z_n(\theta)
},
\]

where

\[
Z_n(\theta)
=
\int p_n(x;\theta)e^{-\varepsilon V_n(x)}\,d\mu(x).
\]

The corresponding Fisher metric defines the information operator

\[
g^{(n+1)}
=
\mathcal{I}^{V_n}_\varepsilon(g^{(n)}).
\]

This is an exponential information deformation.

### 4.1 First variation

Assume for simplicity that \(V_n\) does not depend on \(\theta\). Let

\[
s_i^{(n)}=\partial_i \log p_n
\]

and define the centered potential

\[
\widetilde V_n
=
V_n-\mathbb{E}_n[V_n].
\]

The score of \(p_{n+1}\) is

\[
s_i^{(n+1)}
=
\partial_i \log p_{n+1}
=
s_i^{(n)}-\partial_i \log Z_n.
\]

Expanding in \(\varepsilon\),

\[
\partial_i \log Z_n
=
-\varepsilon
\operatorname{Cov}_n(s_i^{(n)},V_n)
+
O(\varepsilon^2).
\]

Therefore, to first order,

\[
s_i^{(n+1)}
=
s_i^{(n)}
+
\varepsilon
\operatorname{Cov}_n(s_i^{(n)},V_n)
+
O(\varepsilon^2).
\]

The metric is

\[
g_{ij}^{(n+1)}
=
\mathbb{E}_{n+1}
[
s_i^{(n+1)}s_j^{(n+1)}
].
\]

Since

\[
\mathbb{E}_{n+1}[\cdot]
=
\mathbb{E}_n[(\cdot)(1-\varepsilon \widetilde V_n)]
+
O(\varepsilon^2),
\]

one obtains

\[
g_{ij}^{(n+1)}
=
g_{ij}^{(n)}
-
\varepsilon
\operatorname{Cov}_n
\left(
s_i^{(n)}s_j^{(n)},
V_n
\right)
+
O(\varepsilon^2).
\]

Thus the infinitesimal deformation tensor is

\[
D^{V}_{ij}[g_n]
=
-
\operatorname{Cov}_n
\left(
s_i s_j,
V_n
\right).
\]

Hence

\[
\boxed{
g_{ij}^{(n+1)}
=
g_{ij}^{(n)}
-
\varepsilon
\operatorname{Cov}_n
\left(
s_i s_j,
V_n
\right)
+
O(\varepsilon^2)
}
\]

for the probabilistic information operator.

### 4.2 Relative entropy deformation

A particularly important case is obtained by choosing a target distribution \(q(x)\) and setting

\[
V_n(x)
=
\log \frac{p_n(x;\theta)}{q(x)}.
\]

Then

\[
p_{n+1}(x;\theta)
\propto
p_n(x;\theta)^{1-\varepsilon}
q(x)^\varepsilon.
\]

This is a geometric interpolation between the current model and the target. If \(\varepsilon=1\), one obtains \(p_{n+1}=q\) whenever the normalization is well-defined. For \(0<\varepsilon<1\), the recursion performs incremental information contraction toward \(q\).

This construction is useful for variational inference, distillation, and adaptive sampling.

---

## 5. Intrinsic Geometric Information Operators

The probabilistic operator above depends on the embedding of the statistical manifold into a space of probability distributions. In many settings one wants an operator expressed purely in terms of intrinsic tensors.

Let \(R_{ij}\) be the Ricci tensor of \(g\), \(R\) its scalar curvature, and let

\[
C_{ijk}
\]

be the Amari–Chentsov cubic tensor. Raise indices with \(g\) and define the quadratic information tensor

\[
S_{ij}
=
C_{ik\ell}C_j{}^{k\ell}.
\]

This tensor is symmetric and positive semidefinite. Its trace is

\[
g^{ij}S_{ij}
=
|C|^2
=
C_{ijk}C^{ijk}.
\]

Let \(\Phi\) be a scalar information potential, for example a curvature functional, log-volume potential, or entropy proxy. Define the trace-adjusted deformation tensor

\[
D_{ij}^{\mathrm{RIG}}
=
a\left(
R_{ij}-\frac{1}{d}R g_{ij}
\right)
+
b\left(
S_{ij}-\frac{1}{d}|C|^2 g_{ij}
\right)
+
c\left(
\nabla_i\nabla_j\Phi
-
\frac{1}{d}(\Delta \Phi)g_{ij}
\right),
\]

where \(a,b,c\in\mathbb{R}\) are constants and \(d=\dim M\).

The intrinsic recursive information operator is

\[
\boxed{
\mathcal{I}_{\varepsilon}(g)_{ij}
=
g_{ij}
+
\varepsilon D_{ij}^{\mathrm{RIG}}.
}
\]

Because \(D_{ij}^{\mathrm{RIG}}\) is trace-adjusted,

\[
g^{ij}D_{ij}^{\mathrm{RIG}}=0,
\]

so the volume form is preserved to first order.

### 5.1 Continuous limit

If

\[
g_{n+1}=g_n+\varepsilon D^{\mathrm{RIG}}[g_n]+O(\varepsilon^2),
\]

and \(t=n\varepsilon\), then as \(\varepsilon\to 0\) one obtains the continuous RIG flow

\[
\boxed{
\partial_t g_{ij}
=
a\left(
R_{ij}-\frac{1}{d}R g_{ij}
\right)
+
b\left(
C_{ik\ell}C_j{}^{k\ell}
-
\frac{1}{d}|C|^2g_{ij}
\right)
+
c\left(
\nabla_i\nabla_j\Phi
-
\frac{1}{d}(\Delta\Phi)g_{ij}
\right).
}
\]

This is a statistical analogue of a curvature flow with an additional cubic information term. When \(b=c=0\) and \(a=-2\), the flow reduces to the normalized Ricci flow.

### 5.2 Fixed points

A fixed metric satisfies

\[
D_{ij}^{\mathrm{RIG}}[g_*]=0.
\]

Equivalently,

\[
a\left(
R_{ij}-\frac{1}{d}R g_{ij}
\right)
+
b\left(
S_{ij}-\frac{1}{d}|C|^2g_{ij}
\right)
+
c\left(
\nabla_i\nabla_j\Phi
-
\frac{1}{d}(\Delta\Phi)g_{ij}
\right)
=0.
\]

When \(c=0\), this becomes a statistical Einstein-type equation:

\[
a\,\operatorname{Ric}_0
+
b\,S_0
=0,
\]

where \(\operatorname{Ric}_0\) and \(S_0\) denote the trace-free parts. Such metrics are informationally critical: curvature and higher-order statistical tension balance exactly.

---

## 6. Existence, Positivity, and Contraction

### 6.1 Local positivity

Let \(g\in \operatorname{Met}_+(M)\) and let \(D[g]\) be a smooth symmetric tensor field. Suppose \(M\) is compact and

\[
\|D[g]\|_{g,\infty}<\infty.
\]

Then for

\[
0<\varepsilon<
\frac{\lambda_{\min}(g)}{\|D[g]\|_{g,\infty}},
\]

the tensor

\[
g+\varepsilon D[g]
\]

remains positive definite.

**Proof sketch.** Let \(\lambda_{\min}(g)\) be the smallest eigenvalue of \(g\) with respect to a background metric. For any nonzero vector \(v\),

\[
(g+\varepsilon D)(v,v)
\ge
\lambda_{\min}(g)\|v\|^2
-
\varepsilon \|D\|\,\|v\|^2.
\]

Thus positivity holds when

\[
\varepsilon<
\frac{\lambda_{\min}(g)}{\|D\|}.
\]

Hence sufficiently small recursive steps preserve Riemannian structure.

### 6.2 Contraction and fixed points

Let \((\mathcal{K},d)\) be a complete metric space of metrics, for example a closed subset of \(C^{k,\alpha}\) metrics satisfying uniform equivalence bounds

\[
\Lambda^{-1}g_0\le g\le \Lambda g_0.
\]

Suppose

\[
\mathcal{I}:\mathcal{K}\to \mathcal{K}
\]

is a contraction:

\[
d(\mathcal{I}(g),\mathcal{I}(h))
\le
q\,d(g,h),
\qquad
0\le q<1.
\]

Then by the Banach fixed-point theorem, there exists a unique \(g_*\in\mathcal{K}\) such that

\[
\mathcal{I}(g_*)=g_*.
\]

Moreover, for every initial \(g_0\in\mathcal{K}\),

\[
g_n\to g_*
\]

geometrically:

\[
d(g_n,g_*)
\le
q^n d(g_0,g_*).
\]

This gives a general convergence criterion for RIG-II recursions.

### 6.3 Linear stability

Let \(g_*\) be a fixed point and write

\[
g_n=g_*+h_n.
\]

If \(\mathcal{I}\) is differentiable at \(g_*\), then

\[
h_{n+1}
=
L_* h_n
+
O(\|h_n\|^2),
\]

where

\[
L_*=D\mathcal{I}_{g_*}
\]

is the linearized information operator. The fixed point is linearly stable if the spectral radius satisfies

\[
\rho(L_*)<1.
\]

The eigentensors of \(L_*\) determine the local modes of information deformation. This is directly analogous to linearized renormalization-group analysis.

---

## 7. Curvature Recursion

Given

\[
g_{n+1}=g_n+h_n,
\]

with \(h_n\) small, the induced change in curvature can be computed explicitly.

Let \(\nabla\) be the Levi-Civita connection of \(g_n\). The first variation of the Christoffel symbols is

\[
\delta \Gamma^k_{ij}
=
\frac{1}{2}
g^{k\ell}
\left(
\nabla_i h_{j\ell}
+
\nabla_j h_{i\ell}
-
\nabla_\ell h_{ij}
\right).
\]

The corresponding variation of the Riemann tensor is

\[
\delta R^\ell{}_{ijk}
=
\nabla_j \delta\Gamma^\ell_{ik}
-
\nabla_k \delta\Gamma^\ell_{ij}.
\]

The Ricci tensor varies as

\[
\delta R_{ij}
=
\nabla_k \delta\Gamma^k_{ij}
-
\nabla_j \delta\Gamma^k_{ik}.
\]

The scalar curvature variation is

\[
\delta R
=
-\Delta(\operatorname{tr}_g h)
+
\nabla^i\nabla^j h_{ij}
-
h^{ij}R_{ij}.
\]

Therefore, for a RIG-II recursion,

\[
R_{ij}^{(n+1)}
=
R_{ij}^{(n)}
+
\delta R_{ij}[h_n]
+
O(\|h_n\|^2),
\]

and

\[
R^{(n+1)}
=
R^{(n)}
+
\delta R[h_n]
+
O(\|h_n\|^2).
\]

This shows that recursive information geometry induces a recursive curvature flow. In the continuous limit, the curvature evolves according to the corresponding parabolic or geometric PDE.

---

## 8. Recursive Dual Connections and Cubic Tensors

A full RIG-II theory should update not only \(g\) but also the dual connections and the cubic tensor.

For a statistical manifold with metric \(g_n\) and cubic tensor \(C_n\), the \(\alpha\)-connection coefficients are

\[
\Gamma^{(\alpha,n)}_{ij,k}
=
\Gamma^{LC(g_n)}_{ij,k}
+
\frac{\alpha}{2}C^{(n)}_{ijk}.
\]

If the metric evolves by

\[
g_{n+1}=\mathcal{I}(g_n),
\]

and the cubic tensor evolves by

\[
C_{n+1}=\mathcal{J}(g_n,C_n),
\]

then the connection recursion is

\[
\Gamma^{(\alpha,n+1)}_{ij,k}
=
\Gamma^{LC(g_{n+1})}_{ij,k}
+
\frac{\alpha}{2}C^{(n+1)}_{ijk}.
\]

Thus the RIG-II recursion on connections is determined once the metric and cubic tensor recursions are specified.

For exponential deformations

\[
p_{n+1}\propto p_n e^{-\varepsilon V_n},
\]

one obtains, to first order,

\[
C^{(n+1)}_{ijk}
=
C^{(n)}_{ijk}
-
\varepsilon
\operatorname{Cov}_n
\left(
s_i s_j s_k,
V_n
\right)
+
O(\varepsilon^2),
\]

provided \(V_n\) is independent of \(\theta\). This gives a recursive flow for the skewness structure of the model.

---

## 9. Bayesian Recursive Information Geometry

Bayesian inference is naturally recursive. Let \(\pi_0(\theta)\) be a prior and let observations \(x_1,x_2,\dots\) arrive sequentially. The posterior after \(n\) observations is

\[
\pi_n(\theta)
\propto
\pi_0(\theta)
\prod_{a=1}^n
p(x_a\mid \theta).
\]

Define the log-posterior

\[
\ell_n(\theta)
=
\log \pi_n(\theta).
\]

A local information metric is the observed information tensor

\[
g^{(n)}_{ij}(\theta)
=
-\partial_i\partial_j \ell_n(\theta).
\]

Then

\[
g^{(n+1)}_{ij}(\theta)
=
g^{(n)}_{ij}(\theta)
-
\partial_i\partial_j
\log p(x_{n+1}\mid \theta).
\]

Thus Bayesian updating induces an exact additive recursion on local information metrics:

\[
\boxed{
g_{n+1}
=
g_n
+
J_{n+1},
}
\]

where

\[
J_{ij}(x;\theta)
=
-\partial_i\partial_j \log p(x\mid \theta)
\]

is the observed likelihood information.

Taking expectation with respect to the model gives

\[
\mathbb{E}_\theta[J_{ij}(X;\theta)]
=
F_{ij}(\theta),
\]

the Fisher information of the likelihood. Thus the expected Bayesian recursion is

\[
\mathbb{E}[g_{n+1}\mid \theta]
=
g_n+F.
\]

In online or discounted inference, one often uses

\[
g_{n+1}
=
(1-\varepsilon)g_n
+
\varepsilon J_{n+1}.
\]

This is a RIG-II recursion of exponential-moving-average type.

### 9.1 Laplace approximation and posterior concentration

Near a posterior mode \(\hat\theta_n\), the posterior is approximately Gaussian:

\[
\pi_n(\theta)
\approx
\mathcal{N}
\left(
\hat\theta_n,
(g^{(n)}(\hat\theta_n))^{-1}
\right).
\]

The recursive update

\[
g_{n+1}=g_n+J_{n+1}
\]

therefore describes posterior concentration. As \(n\to\infty\), under standard regularity,

\[
\frac{1}{n}g_n
\to
F(\theta_*)
\]

and the posterior covariance shrinks as

\[
\Sigma_n
\sim
\frac{1}{n}F(\theta_*)^{-1}.
\]

RIG-II gives a geometric formulation of this classical asymptotic phenomenon.

---

## 10. Machine Learning and Adaptive Natural Gradients

Consider a parametric model \(p_\theta\) and a loss function

\[
L(\theta)
=
\mathbb{E}_{q}[\ell(x;\theta)].
\]

Standard natural gradient descent uses the Fisher metric \(F(\theta)\):

\[
\theta_{n+1}
=
\theta_n
-
\eta F(\theta_n)^{-1}\nabla L(\theta_n).
\]

In RIG-II, the metric itself evolves:

\[
g_{n+1}
=
\mathcal{I}(g_n).
\]

The adaptive natural gradient descent becomes

\[
\boxed{
\theta_{n+1}
=
\theta_n
-
\eta g_n^{-1}\nabla L(\theta_n),
}
\]

together with

\[
\boxed{
g_{n+1}
=
\mathcal{I}(g_n;\theta_n,\nabla L,\nabla^2 L).
}
\]

Several choices of \(\mathcal{I}\) are natural.

### 10.1 Fisher tracking

Let \(F_n\) be the empirical Fisher matrix at step \(n\). Define

\[
g_{n+1}
=
(1-\varepsilon)g_n
+
\varepsilon F_n.
\]

This makes \(g_n\) track the empirical Fisher information.

### 10.2 Curvature tracking

Let \(H_n=\nabla^2 L(\theta_n)\). Define

\[
g_{n+1}
=
(1-\varepsilon)g_n
+
\varepsilon H_n.
\]

This approximates Newton-type geometry while preserving positive definiteness if appropriately regularized.

### 10.3 Riemannian exponential stabilization

To ensure positive definiteness, use the symmetric positive-definite exponential:

\[
g_{n+1}
=
g_n^{1/2}
\exp
\left(
\varepsilon
g_n^{-1/2}
D_n
g_n^{-1/2}
\right)
g_n^{1/2},
\]

where \(D_n\) is a symmetric direction such as \(F_n-g_n\) or \(H_n-g_n\). For small \(\varepsilon\),

\[
g_{n+1}
=
g_n
+
\varepsilon D_n
+
O(\varepsilon^2).
\]

This guarantees \(g_{n+1}\succ 0\).

### 10.4 Conditioning and convergence

Suppose the loss is \(\mu\)-strongly convex and \(L\)-smooth with respect to the true Fisher metric. If the recursive metric satisfies uniform equivalence

\[
\kappa^{-1}F(\theta)
\le
g_n(\theta)
\le
\kappa F(\theta),
\]

then the condition number of the preconditioned gradient is bounded by \(\kappa\). The RIG-II recursion can therefore stabilize optimization by reducing ill-conditioning.

A typical convergence estimate takes the form

\[
L(\theta_{n+1})-L(\theta_*)
\le
\left(
1-\frac{\mu}{\kappa L}
\right)
\left(
L(\theta_n)-L(\theta_*)
\right),
\]

up to stochastic error terms. The essential point is that recursive adaptation of \(g_n\) can reduce \(\kappa\) dynamically.

---

## 11. Quantum Recursive Information Geometry

In quantum information, statistical manifolds are replaced by manifolds of density matrices \(\rho(\theta)\). The quantum analogue of the Fisher metric is given by monotone metrics, most notably the Bures metric.

Let \(\rho(\theta)\) be a smooth family of density operators. The symmetric logarithmic derivatives \(L_i\) are defined by

\[
\partial_i \rho
=
\frac{1}{2}
(L_i\rho+\rho L_i).
\]

The Bures metric is

\[
g_{ij}^{B}
=
\frac{1}{2}
\operatorname{Tr}
\left(
\rho(L_iL_j+L_jL_i)
\right).
\]

Equivalently,

\[
g_{ij}^{B}
=
\operatorname{Tr}
\left(
\partial_i\rho\, L_j
\right).
\]

Let \(\mathcal{E}\) be a completely positive trace-preserving map. Quantum data processing implies

\[
g^B(\mathcal{E}(\rho))
\le
g^B(\rho).
\]

Thus quantum channels are information-contraction operators.

A quantum RIG-II recursion may be written as

\[
\rho_{n+1}
=
\mathcal{E}_n(\rho_n),
\]

and

\[
g_{n+1}
=
\mathcal{I}_Q(g_n).
\]

For example, if

\[
\rho_{n+1}
=
\frac{
e^{-\varepsilon K/2}
\rho_n
e^{-\varepsilon K/2}
}{
\operatorname{Tr}
\left(
e^{-\varepsilon K/2}
\rho_n
e^{-\varepsilon K/2}
\right)
},
\]

where \(K\) is a quantum information potential or Hamiltonian, then the Bures metric evolves recursively. Fixed points include thermal states

\[
\rho_*
=
\frac{e^{-K}}{\operatorname{Tr}(e^{-K})}
\]

when the deformation is chosen appropriately.

Quantum RIG-II provides a geometric foundation for quantum natural gradient methods, variational quantum eigensolvers, and recursive channel discrimination.

---

## 12. Statistical Physics and Renormalization

Recursive information geometry is closely related to the renormalization group.

Let \(\sigma\) denote microscopic degrees of freedom and let \(K=(K^1,\dots,K^d)\) be coupling constants. A Gibbs measure is

\[
p_K(\sigma)
=
\frac{
e^{-H_K(\sigma)}
}{
Z(K)
}.
\]

Define observables

\[
O_a(\sigma)
=
\frac{\partial H_K(\sigma)}{\partial K^a}.
\]

The Fisher metric on the space of couplings is

\[
g_{ab}
=
\operatorname{Cov}_K(O_a,O_b).
\]

If the Hamiltonian is multiplied by inverse temperature \(\beta\), then

\[
g_{ab}
=
\beta^2
\left(
\langle O_aO_b\rangle
-
\langle O_a\rangle\langle O_b\rangle
\right).
\]

A real-space renormalization transformation is a Markov kernel

\[
K_{\mathrm{RG}}(\sigma'\mid \sigma)
\]

mapping microscopic configurations to coarse-grained configurations. The coarse-grained distribution is

\[
p_{n+1}(\sigma')
=
\sum_\sigma
K_{\mathrm{RG}}(\sigma'\mid \sigma)
p_n(\sigma).
\]

The induced metric recursion is

\[
g_{n+1}
=
\mathcal{I}_{\mathrm{RG}}(g_n).
\]

Because coarse-graining is a stochastic map, Chentsov monotonicity gives

\[
g_{n+1}
\le
g_n
\]

in the appropriate Fisher sense.

### 12.1 Critical fixed points

A critical theory corresponds to a fixed metric

\[
g_*=\mathcal{I}_{\mathrm{RG}}(g_*).
\]

Linearizing around \(g_*\),

\[
\delta g_{n+1}
=
L_*\delta g_n.
\]

If \(\lambda\) is an eigenvalue of \(L_*\) associated with a scaling operator, then under length rescaling by factor \(b\),

\[
\lambda=b^{y},
\]

where \(y\) is the scaling dimension. The correlation-length exponent is

\[
\nu=\frac{1}{y}.
\]

Thus the spectrum of the linearized information operator encodes universal critical exponents.

---

## 13. Numerical Realization

In practical computation, metrics are often represented by positive-definite matrices. A stable recursive scheme should preserve positive definiteness.

Given a current metric matrix \(G_n\) and a symmetric update direction \(D_n\), define

\[
G_{n+1}
=
G_n^{1/2}
\exp
\left(
\varepsilon
G_n^{-1/2}
D_n
G_n^{-1/2}
\right)
G_n^{1/2}.
\]

This is the Riemannian exponential on the cone of positive-definite matrices with the affine-invariant metric. It satisfies

\[
G_{n+1}
=
G_n+\varepsilon D_n+O(\varepsilon^2)
\]

and guarantees

\[
G_{n+1}\succ 0.
\]

### Algorithm: Recursive Information Geometry

**Input:** initial metric \(G_0\), step size \(\varepsilon\), number of steps \(N\), direction operator \(D\).

For \(n=0,\dots,N-1\):

1. Compute the information direction  
   \[
   D_n=D(G_n).
   \]

2. Symmetrize:  
   \[
   D_n\leftarrow \frac{1}{2}(D_n+D_n^\top).
   \]

3. Update by SPD exponential:  
   \[
   G_{n+1}
   =
   G_n^{1/2}
   \exp
   \left(
   \varepsilon
   G_n^{-1/2}
   D_n
   G_n^{-1/2}
   \right)
   G_n^{1/2}.
   \]

**Output:** sequence \(G_0,\dots,G_N\).

For large-scale problems, the matrix exponential may be approximated by first-order or quasi-Newton updates.

---

## 14. Example: Gaussian Models

Let

\[
p_n(x)=\mathcal{N}(x;\mu_n,\Sigma_n)
\]

and let the target be

\[
q(x)=\mathcal{N}(x;\nu,\Gamma).
\]

Define the geometric mixture

\[
p_{n+1}
\propto
p_n^{1-\varepsilon}
q^\varepsilon.
\]

Because products of Gaussians are Gaussian, the updated distribution remains Gaussian. The precision matrices satisfy

\[
\Sigma_{n+1}^{-1}
=
(1-\varepsilon)\Sigma_n^{-1}
+
\varepsilon \Gamma^{-1}.
\]

The means satisfy

\[
\mu_{n+1}
=
\Sigma_{n+1}
\left(
(1-\varepsilon)\Sigma_n^{-1}\mu_n
+
\varepsilon \Gamma^{-1}\nu
\right).
\]

For a Gaussian location model, the Fisher metric with respect to the mean is the precision matrix:

\[
g^{(\mu)}_n
=
\Sigma_n^{-1}.
\]

Hence the RIG-II recursion becomes

\[
\boxed{
g^{(\mu)}_{n+1}
=
(1-\varepsilon)g^{(\mu)}_n
+
\varepsilon \Gamma^{-1}.
}
\]

This is a linear contraction toward the target precision.

For the scalar variance parameter, if

\[
p_n=\mathcal{N}(\mu,\sigma_n^2),
\]

then the Fisher metric component for \(\mu\) is

\[
g_{\mu\mu}^{(n)}
=
\frac{1}{\sigma_n^2}.
\]

Writing \(\lambda_n=\sigma_n^{-2}\), the recursion is

\[
\lambda_{n+1}
=
(1-\varepsilon)\lambda_n
+
\varepsilon \lambda_*.
\]

Thus

\[
\lambda_n-\lambda_*
=
(1-\varepsilon)^n(\lambda_0-\lambda_*).
\]

This provides an explicit exactly solvable RIG-II system.

---

## 15. Example: Bernoulli Model

Let \(p_\theta\) be a Bernoulli distribution with parameter \(\theta\in(0,1)\). The Fisher metric is

\[
g(\theta)
=
\frac{1}{\theta(1-\theta)}.
\]

Suppose the parameter evolves by recursive Bayesian contraction toward a target \(q\in(0,1)\):

\[
\theta_{n+1}
=
(1-\varepsilon)\theta_n
+
\varepsilon q.
\]

The pulled-back metric at step \(n\) is

\[
g_n^{\mathrm{pull}}
=
g(\theta_{n+1})
\left(
\frac{d\theta_{n+1}}{d\theta_n}
\right)^2.
\]

Since

\[
\frac{d\theta_{n+1}}{d\theta_n}
=
1-\varepsilon,
\]

we obtain

\[
g_n^{\mathrm{pull}}
=
\frac{(1-\varepsilon)^2}
{\theta_{n+1}(1-\theta_{n+1})}.
\]

This simple example illustrates how parameter-space contractions induce metric deformations.

---

## 16. Categorical Perspective

RIG-II may also be formulated categorically. Let \(\mathbf{Stat}\) be the category whose objects are statistical manifolds and whose morphisms are statistical maps, Markov kernels, or sufficient statistics. An information operator is an endofunctor

\[
\mathcal{I}:\mathbf{Stat}\to \mathbf{Stat}.
\]

A RIG-II system is then a discrete dynamical system in \(\mathbf{Stat}\):

\[
\mathcal{S}_{n+1}
=
\mathcal{I}(\mathcal{S}_n).
\]

Fixed points are coalgebras or invariant objects satisfying

\[
\mathcal{S}\cong \mathcal{I}(\mathcal{S}).
\]

This viewpoint clarifies the relation between recursion, sufficient statistics, and data processing. It also suggests extensions to probabilistic programming semantics and categorical probability.

---

## 17. Open Problems

Several directions arise from the RIG-II framework.

1. **Classification of fixed information operators.**  
   For canonical operators, classify fixed metrics satisfying
   \[
   D_{ij}^{\mathrm{RIG}}=0.
   \]

2. **Infinite-dimensional RIG-II.**  
   Extend the theory to manifolds of probability measures, Gaussian processes, and neural tangent kernels.

3. **Non-Markovian recursion.**  
   Allow memory-dependent operators
   \[
   g_{n+1}=\mathcal{I}(g_n,g_{n-1},\dots).
   \]

4. **Quantum information operators.**  
   Develop a complete theory of completely positive information operators acting on monotone quantum metrics.

5. **Learning-theoretic generalization bounds.**  
   Relate contraction rates of \(g_n\) to generalization error and PAC-Bayes complexity.

6. **Renormalization-group interpretation.**  
   Make precise the correspondence between RIG-II fixed points and conformal field theories.

---

## 18. Conclusion

Recursive Information Geometry II introduces a dynamical layer into information geometry. Instead of treating the Fisher metric and related structures as fixed, RIG-II allows them to evolve through information operators:

\[
g_{n+1}=\mathcal{I}(g_n).
\]

This simple recursion unifies several phenomena: Bayesian posterior concentration, adaptive natural gradient descent, quantum data processing, and renormalization-group flow. By formulating axioms for information operators, constructing canonical probabilistic and intrinsic geometric realizations, and analyzing fixed points and curvature recursion, we obtain a coherent theory of evolving statistical manifolds.

The central insight is that information is not merely a quantity computed on a static geometric background. In many fundamental statistical systems, information actively reshapes the geometry in which future inference, learning, and physical evolution occur. RIG-II provides the mathematical language for this recursive phenomenon.

---

## References

1. S.-I. Amari, *Information Geometry and Its Applications*, Springer, 2016.  
2. S.-I. Amari and H. Nagaoka, *Methods of Information Geometry*, AMS, 2000.  
3. N. N. Chentsov, *Statistical Decision Rules and Optimal Inference*, AMS, 1982.  
4. J. Ay, J. Jost, H. V. Lê, and L. Schwachhöfer, *Information Geometry*, Springer, 2017.  
5. D. Bures, “An extension of Kakutani’s theorem on infinite product measures to the Hilbert space case,” *Transactions of the AMS*, 1969.  
6. K. G. Wilson, “Renormalization group and critical phenomena,” *Physical Review B*, 1971.  
7. M. Nielsen and I. Chuang, *Quantum Computation and Quantum Information*, Cambridge University Press, 2000.

# Information Metric Dynamics

**Preprint — August 1, 2026**

**Keywords:** information geometry, Fisher metric, Ricci flow, Bayesian inference, statistical physics, natural gradient, complex systems, metric evolution

---

## Abstract

We develop a general theoretical framework called **Information Metric Dynamics** (IMD), in which Riemannian metrics on statistical manifolds are not fixed background structures but dynamical fields driven by information flow. The central postulate is

\[
\frac{\partial g_{ij}}{\partial t}=\mathcal I_{ij},
\]

or, in diffeomorphism-covariant form,

\[
\mathcal D_t g_{ij}
:=
\partial_t g_{ij}-\mathcal L_{\beta}g_{ij}
=
\mathcal I_{ij},
\]

where \(g_{ij}\) is a Fisher-type information metric, \(\mathcal I_{ij}\) is a symmetric information tensor, \(\beta^i\) is a gauge field encoding the motion of the coordinate frame, and \(\mathcal L_\beta\) denotes the Lie derivative. In this framework, geometry is the accumulated memory of statistical distinguishability. Curvature, volume, and geodesic structure become dynamical consequences of information accumulation, forgetting, diffusion, and Bayesian contraction.

We give a tensorial formulation of IMD, derive the fundamental evolution equation from the time dependence of Fisher information, propose natural constitutive closures for \(\mathcal I_{ij}\), and analyze the resulting flows. We show that several known structures appear as special cases: Fisher-Rao geometry, natural gradient flow, Bayesian posterior contraction, thermodynamic metric evolution, and Ricci-type geometric smoothing. We then develop applications to statistical physics, artificial intelligence, complex adaptive systems, and Bayesian geometry.

The central thesis is that the metric of a statistical manifold should be understood not as a static measure of distinguishability, but as a dynamical field whose evolution is governed by the flux, production, and relaxation of information.

---

## 1. Introduction

Classical information geometry studies a parametric family of probability distributions

\[
\mathcal S=\{p(x;\theta)\mid \theta=(\theta^1,\dots,\theta^n)\in M\}
\]

as a differentiable manifold \(M\) equipped with the Fisher-Rao metric

\[
g_{ij}(\theta)
=
\mathbb E_{\theta}
\left[
\partial_i \log p(X;\theta)\,
\partial_j \log p(X;\theta)
\right].
\]

This metric measures infinitesimal statistical distinguishability:

\[
ds^2
=
g_{ij}(\theta)\,d\theta^i d\theta^j.
\]

Two nearby parameter values \(\theta\) and \(\theta+d\theta\) are statistically distinguishable to second order according to \(ds^2\). The Fisher metric is canonical: by the Čencov uniqueness theorem, it is essentially the only Riemannian metric invariant under sufficient statistics and Markov morphisms.

However, in many physical, biological, and computational systems, the relevant statistical geometry is not static. A learning system accumulates data. A thermodynamic system is driven out of equilibrium. A complex adaptive network reorganizes its effective interactions. A Bayesian agent updates its posterior. In each case, the underlying notion of statistical distinguishability changes with time.

The usual treatment keeps the metric fixed and allows the probability distribution or parameter estimate to evolve. This is often inadequate. If the system’s effective degrees of freedom, correlations, or resolution scale change, then the metric itself must evolve.

Information Metric Dynamics proposes the following shift:

\[
\text{static geometry:}
\qquad
g_{ij}
\]

\[
\Downarrow
\]

\[
\text{dynamic geometry:}
\qquad
\frac{\partial g_{ij}}{\partial t}
=
\mathcal I_{ij}.
\]

The object \(\mathcal I_{ij}\) is the **information tensor**. It encodes the local rate at which information modifies statistical distinguishability. The metric is no longer a passive stage; it is a dynamical record of information processed by the system.

This idea is analogous to the passage from Newtonian mechanics on a fixed configuration space to general relativity, where geometry itself becomes dynamical. Here, however, the source of geometry is not mass-energy but information.

The guiding principles of IMD are:

1. **Statistical distinguishability is physical.**  
   The metric measures the cost of discriminating between nearby states.

2. **Information flow deforms distinguishability.**  
   When information is acquired, forgotten, transported, or dissipated, the metric changes.

3. **Geometry stores information history.**  
   Curvature and volume encode accumulated constraints, correlations, and uncertainties.

4. **Metric evolution should be covariant.**  
   The theory must be invariant under reparametrization of the statistical manifold.

5. **The Fisher metric is the equilibrium or reference metric.**  
   More general metrics arise as dynamical deformations of Fisher-Rao geometry.

The present paper develops this program systematically.

---

## 2. Statistical Manifolds and Fisher Geometry

Let \((X,\mu)\) be a measure space and let

\[
p(x;\theta)>0,
\qquad
\theta\in M,
\]

be a smooth parametric family of probability densities with respect to \(\mu\). The score fields are

\[
s_i(x;\theta)
:=
\partial_i \log p(x;\theta).
\]

They satisfy

\[
\mathbb E_\theta[s_i]=0.
\]

The Fisher-Rao metric is

\[
g_{ij}(\theta)
=
\mathbb E_\theta[s_i s_j]
=
\int_X p(x;\theta)
\partial_i \log p(x;\theta)
\partial_j \log p(x;\theta)
\,d\mu(x).
\]

Equivalently,

\[
g_{ij}
=
-\mathbb E_\theta[\partial_i\partial_j \log p],
\]

assuming regularity and vanishing boundary terms.

The Fisher metric induces:

- a line element

  \[
  ds^2=g_{ij}d\theta^i d\theta^j,
  \]

- a volume form

  \[
  d\mu_g=\sqrt{\det g}\,d\theta^1\wedge\cdots\wedge d\theta^n,
  \]

- a Levi-Civita connection

  \[
  \Gamma^k_{ij}
  =
  \frac12 g^{k\ell}
  \left(
  \partial_i g_{j\ell}
  +
  \partial_j g_{i\ell}
  -
  \partial_\ell g_{ij}
  \right),
  \]

- curvature tensors \(R^i{}_{jkl}\), \(R_{ij}\), and scalar curvature \(R\).

In information geometry one also introduces dual connections, the exponential connection, the mixture connection, and the \(\alpha\)-connections. For the present paper, the Levi-Civita connection of the evolving metric is the primary geometric object, although the framework is compatible with dual-connection structures.

---

## 3. The Fundamental IMD Postulate

Let \(g_{ij}(t)\) be a smooth one-parameter family of Riemannian metrics on \(M\). The basic IMD equation is

\[
\boxed{
\frac{\partial g_{ij}}{\partial t}
=
\mathcal I_{ij}.
}
\]

Here

\[
\mathcal I_{ij}=\mathcal I_{ji}
\]

is a symmetric covariant 2-tensor called the **information tensor**.

Because \(g_{ij}\) is a tensor, its partial time derivative is tensorial only when the spatial coordinates are fixed. If the coordinate system itself evolves by a time-dependent diffeomorphism, one must use a gauge-covariant material derivative. Let \(\beta^i(t,\theta)\) be the velocity field of the moving frame. Define

\[
\mathcal D_t g_{ij}
:=
\partial_t g_{ij}
-
\mathcal L_\beta g_{ij},
\]

where

\[
\mathcal L_\beta g_{ij}
=
\nabla_i\beta_j+\nabla_j\beta_i.
\]

The covariant IMD equation is therefore

\[
\boxed{
\mathcal D_t g_{ij}
=
\mathcal I_{ij}.
}
\]

In a fixed coordinate gauge, \(\beta^i=0\), this reduces to

\[
\partial_t g_{ij}=\mathcal I_{ij}.
\]

The trace of the information tensor,

\[
\mathcal I:=g^{ij}\mathcal I_{ij},
\]

controls the local evolution of volume. Since

\[
\partial_t \log\sqrt{\det g}
=
\frac12 g^{ij}\partial_t g_{ij},
\]

we have, in a fixed gauge,

\[
\partial_t d\mu_g
=
\frac12 \mathcal I\,d\mu_g.
\]

Thus:

- \(\mathcal I>0\): local expansion of statistical volume;
- \(\mathcal I<0\): local contraction of statistical volume;
- \(\mathcal I=0\): information-volume preservation.

The trace-free part,

\[
\mathcal I^{\mathrm{tf}}_{ij}
=
\mathcal I_{ij}
-
\frac1n \mathcal I g_{ij},
\]

controls anisotropic deformation of statistical distinguishability.

---

## 4. Information Tensor from Time-Dependent Statistical Models

Suppose the statistical model itself depends on time:

\[
p=p(x;\theta,t).
\]

Define

\[
s_i:=\partial_i\log p,
\qquad
q:=\partial_t\log p.
\]

The time-dependent Fisher metric is

\[
g_{ij}(t)
=
\mathbb E_t[s_i s_j].
\]

Differentiating under the integral gives the exact identity

\[
\boxed{
\partial_t g_{ij}
=
\mathbb E_t
\left[
q\,s_i s_j
+
s_i\,\partial_j q
+
s_j\,\partial_i q
\right].
}
\]

This identity provides a microscopic definition of the information tensor:

\[
\mathcal I_{ij}^{(p)}
:=
\mathbb E_t
\left[
q\,s_i s_j
+
s_i\,\partial_j q
+
s_j\,\partial_i q
\right].
\]

Here \(q\) is the **logarithmic information velocity** of the model. It measures how the log-likelihood changes in time at fixed parameter. The tensor \(\mathcal I_{ij}^{(p)}\) is therefore the rate at which statistical distinguishability changes because the underlying probability law changes.

This formula is exact but generally not closed in terms of \(g_{ij}\) alone. A macroscopic IMD theory requires a constitutive relation

\[
\mathcal I_{ij}
=
\mathcal F_{ij}[g,\Phi,J,F,\dots],
\]

where \(\Phi\) is an information potential, \(J^i\) an information current, and \(F_{ij}\) an external or observed Fisher information source.

---

## 5. Natural Constitutive Laws for the Information Tensor

A physically reasonable information tensor should be:

1. symmetric;
2. covariant under reparametrization;
3. local or weakly nonlocal;
4. compatible with positivity of \(g_{ij}\);
5. reducible to Fisher-Rao geometry in equilibrium.

By naturality arguments similar to those appearing in Riemannian geometry and Lovelock-type theorems, the lowest-order symmetric 2-tensors available are

\[
g_{ij},
\qquad
R_{ij},
\qquad
\nabla_i\nabla_j\Phi,
\qquad
(\Delta\Phi)g_{ij},
\qquad
\mathcal L_J g_{ij}.
\]

We therefore propose the general IMD constitutive equation

\[
\boxed{
\mathcal I_{ij}
=
\lambda F_{ij}
+
\nabla_i J_j+\nabla_j J_i
+
2\gamma \nabla_i\nabla_j\Phi
+
\alpha (\Delta\Phi)g_{ij}
-
2\beta R_{ij}
-
\kappa g_{ij}.
}
\]

Each term has a distinct interpretation.

### 5.1 Information source term

\[
\lambda F_{ij}
\]

represents injection of Fisher information from observations, measurements, or environmental signals. Here

\[
F_{ij}
=
\mathbb E[u_i u_j]
\]

is an observed or empirical Fisher tensor, with

\[
u_i=\partial_i \log \ell
\]

the score of the likelihood rate.

### 5.2 Information advection

\[
\nabla_i J_j+\nabla_j J_i
=
\mathcal L_J g_{ij}
\]

describes transport of geometry by an information current \(J^i\). If this is the only term, then

\[
\partial_t g_{ij}
=
\mathcal L_J g_{ij},
\]

and the solution is a pullback by the flow of \(J\):

\[
g(t)=\varphi_t^*g(0).
\]

Thus positivity of the metric is automatically preserved.

### 5.3 Potential information strain

\[
2\gamma \nabla_i\nabla_j\Phi
\]

describes deformation generated by an information potential \(\Phi\). If

\[
J_i=-\nabla_i\Phi,
\]

then this term is related to gradient flow of information.

### 5.4 Isotropic information pressure

\[
\alpha(\Delta\Phi)g_{ij}
\]

produces uniform expansion or contraction depending on the Laplacian of the information potential.

### 5.5 Geometric relaxation

\[
-2\beta R_{ij}
\]

is a Ricci-type smoothing term. For \(\beta>0\), this resembles Ricci flow:

\[
\partial_t g_{ij}
=
-2\beta R_{ij}.
\]

It tends to homogenize curvature and diffuse geometric irregularities. In IMD, Ricci flow is interpreted as intrinsic information diffusion: curvature measures the failure of local statistical distinguishability to integrate consistently around infinitesimal loops.

### 5.6 Forgetting or regularization

\[
-\kappa g_{ij}
\]

represents exponential forgetting, decay of memory, or regularization. If \(F_{ij}=0\), then

\[
\partial_t g_{ij}=-\kappa g_{ij},
\]

so

\[
g_{ij}(t)=e^{-\kappa t}g_{ij}(0).
\]

This shrinks statistical volume and models finite memory.

---

## 6. Canonical IMD Models

The general constitutive law contains many important special cases.

### 6.1 Pure information transport

\[
\partial_t g_{ij}
=
\nabla_i J_j+\nabla_j J_i.
\]

This is metric evolution by Lie dragging along the information current. It preserves positivity and represents reversible information flow.

### 6.2 Potential information flow

\[
\partial_t g_{ij}
=
2\nabla_i\nabla_j\Phi.
\]

The volume evolves as

\[
\partial_t d\mu_g
=
(\Delta\Phi)d\mu_g.
\]

If \(\Phi\) is an entropy or free-energy potential, this describes metric deformation by thermodynamic or Bayesian forces.

### 6.3 Bayesian accumulation with forgetting

\[
\partial_t g_{ij}
=
\lambda F_{ij}
-
\kappa(g_{ij}-g^0_{ij}).
\]

Here \(g^0_{ij}\) is a prior or reference metric. This equation says that the metric relaxes toward prior geometry while being driven by observed Fisher information.

### 6.4 Information-Ricci flow

\[
\partial_t g_{ij}
=
-2\beta R_{ij}
+
2\gamma \nabla_i\nabla_j\Phi.
\]

This combines geometric smoothing with information potential forcing. It is the closest geometric analogue of a heat equation for statistical distinguishability.

### 6.5 Full IMD flow

A useful default model is

\[
\boxed{
\partial_t g_{ij}
=
\lambda F_{ij}
+
\nabla_i J_j+\nabla_j J_i
-
2\beta R_{ij}
+
2\gamma \nabla_i\nabla_j\Phi
-
\kappa g_{ij}.
}
\]

This equation will be used as the standard working form of IMD.

---

## 7. Variational Formulation

IMD may be formulated as a gradient flow on the space of Riemannian metrics. Let \(\mathrm{Met}(M)\) denote the space of smooth positive-definite metrics. A natural supermetric on \(T_g\mathrm{Met}(M)\) is the DeWitt metric

\[
\mathbb G^{ijkl}
=
\frac12
\left(
g^{ik}g^{jl}+g^{il}g^{jk}
\right)
-
\lambda g^{ij}g^{kl},
\]

with inverse, when defined,

\[
\mathbb G_{ijkl}
=
\frac12
\left(
g_{ik}g_{jl}+g_{il}g_{jk}
\right)
-
\frac{\lambda}{1-n\lambda}g_{ij}g_{kl}.
\]

Given an information functional

\[
\mathcal F[g]
=
\int_M f(g,\nabla g,\dots)\,d\mu_g,
\]

define the gradient flow

\[
\partial_t g_{ij}
=
-2\,\mathbb G_{ijkl}
\frac{\delta \mathcal F}{\delta g_{kl}}.
\]

A particularly important functional is the weighted information energy

\[
\mathcal F[g,\Phi]
=
\int_M
\left(
R+|\nabla\Phi|^2
\right)
e^{-\Phi}
\,d\mu_g.
\]

This is analogous to Perelman’s \(\mathcal F\)-functional. Its gradient flow produces a coupled system of the form

\[
\partial_t g_{ij}
=
-2R_{ij}
-2\nabla_i\nabla_j\Phi
+
\text{lower-order terms},
\]

which we interpret as an information-Ricci flow with potential.

More generally, one may define an action over metric paths:

\[
S[g]
=
\frac12
\int_0^T
\int_M
\mathbb G^{ijkl}
\left(
\partial_t g_{ij}-\mathcal A_{ij}
\right)
\left(
\partial_t g_{kl}-\mathcal A_{kl}
\right)
\,d\mu_g\,dt,
\]

where \(\mathcal A_{ij}\) is a prescribed information strain. Minimizing \(S\) yields the most probable metric trajectory under the constraint that the system follow the information source \(\mathcal A_{ij}\). This provides a maximum-caliber derivation of IMD.

---

## 8. Bayesian Information Metric Dynamics

Let \(\pi_t(\theta)\) be a posterior distribution over parameters \(\theta\in M\), updated continuously from data. Define the posterior Fisher metric

\[
g_{ij}(t)
=
\mathbb E_{\pi_t}
\left[
\partial_i \log \pi_t(\theta)
\partial_j \log \pi_t(\theta)
\right].
\]

Suppose data arrive as a continuous likelihood stream with log-likelihood rate \(\ell_t(\theta)\). Then the posterior evolves formally as

\[
\partial_t \log \pi_t(\theta)
=
\ell_t(\theta)
-
\mathbb E_{\pi_t}[\ell_t].
\]

Let

\[
q_t(\theta)
=
\partial_t\log\pi_t(\theta).
\]

The exact Fisher derivative identity gives

\[
\partial_t g_{ij}
=
\mathbb E_{\pi_t}
\left[
q_t s_i s_j
+
s_i\partial_j q_t
+
s_j\partial_i q_t
\right].
\]

In many Bayesian regimes, especially when the posterior is sharply concentrated, the dominant contribution is the observed Fisher information:

\[
F^{\mathrm{obs}}_{ij}
=
\mathbb E_{\pi_t}
\left[
\partial_i\ell_t\,\partial_j\ell_t
\right].
\]

Thus one obtains the approximate Bayesian IMD equation

\[
\boxed{
\partial_t g_{ij}
=
\lambda F^{\mathrm{obs}}_{ij}
-
\kappa(g_{ij}-g^0_{ij}).
}
\]

The first term increases distinguishability where data are informative. The second term regularizes toward the prior metric.

### 8.1 Gaussian example

Consider a scalar Gaussian mean model

\[
x\sim \mathcal N(\mu,\sigma^2),
\]

with known \(\sigma\). Suppose observations arrive at constant rate \(\lambda\), each with observation variance \(\sigma_{\mathrm{obs}}^2\). The posterior precision for \(\mu\) is

\[
g_{\mu\mu}(t)
=
\frac{1}{\tau^2(t)},
\]

where

\[
\frac{1}{\tau^2(t)}
=
\frac{1}{\tau_0^2}
+
\frac{\lambda t}{\sigma_{\mathrm{obs}}^2}.
\]

Therefore

\[
\boxed{
\frac{d}{dt}g_{\mu\mu}
=
\frac{\lambda}{\sigma_{\mathrm{obs}}^2}.
}
\]

With forgetting rate \(\kappa\),

\[
\frac{d}{dt}g_{\mu\mu}
=
\frac{\lambda}{\sigma_{\mathrm{obs}}^2}
-
\kappa(g_{\mu\mu}-g^0_{\mu\mu}).
\]

The equilibrium precision is

\[
g_{\mu\mu}^{\infty}
=
g^0_{\mu\mu}
+
\frac{\lambda}{\kappa\sigma_{\mathrm{obs}}^2}.
\]

Thus the metric equilibrates at a value determined by the balance between information acquisition and forgetting.

### 8.2 Bernoulli example

Let

\[
p(x=1\mid \theta)=\theta,
\qquad
0<\theta<1.
\]

The Fisher metric is

\[
g_{\theta\theta}
=
\frac{1}{\theta(1-\theta)}.
\]

If Bernoulli observations arrive at rate \(\lambda\), then locally

\[
\partial_t g_{\theta\theta}
\approx
\frac{\lambda}{\theta(1-\theta)}.
\]

As \(\theta\to 0\) or \(\theta\to 1\), the metric diverges. This divergence corresponds to posterior concentration and increasing certainty. IMD interprets Bayesian certainty as a geometric singularity or near-singularity of the information metric.

---

## 9. Information Geodesics in a Dynamic Metric

Given a time-dependent metric \(g_{ij}(t)\), the length of a curve \(\theta(t)\) is

\[
L[\theta]
=
\int
\sqrt{
g_{ij}(\theta(t),t)
\dot\theta^i\dot\theta^j
}
\,dt.
\]

The energy functional is

\[
E[\theta]
=
\frac12
\int
g_{ij}(\theta(t),t)
\dot\theta^i\dot\theta^j
\,dt.
\]

The Euler-Lagrange equations are

\[
g_{ij}\ddot\theta^j
+
\Gamma_{i,jk}\dot\theta^j\dot\theta^k
+
\partial_t g_{ij}\dot\theta^j
=
0,
\]

where

\[
\Gamma_{i,jk}
=
\frac12
\left(
\partial_j g_{ik}
+
\partial_k g_{ij}
-
\partial_i g_{jk}
\right).
\]

Multiplying by \(g^{\ell i}\), we obtain

\[
\boxed{
\ddot\theta^\ell
+
\Gamma^\ell_{jk}\dot\theta^j\dot\theta^k
=
-
g^{\ell i}\mathcal I_{ij}\dot\theta^j.
}
\]

Thus the information tensor produces an effective force on statistical geodesics. In IMD, geodesics are not merely shortest paths in a fixed statistical manifold; they are trajectories acted upon by information flow.

---

## 10. Curvature Evolution Under IMD

Let

\[
h_{ij}:=\partial_t g_{ij}=\mathcal I_{ij}.
\]

The variation of the Levi-Civita connection is

\[
\partial_t \Gamma^k_{ij}
=
\frac12 g^{k\ell}
\left(
\nabla_i h_{j\ell}
+
\nabla_j h_{i\ell}
-
\nabla_\ell h_{ij}
\right).
\]

The variation of the Ricci tensor is

\[
\partial_t R_{ij}
=
\frac12
\left(
-\Delta_L h_{ij}
+
\nabla_i\nabla^k h_{kj}
+
\nabla_j\nabla^k h_{ki}
-
\nabla_i\nabla_j \operatorname{tr}_g h
\right),
\]

where \(\Delta_L\) is the Lichnerowicz Laplacian.

For the pure Ricci-information flow

\[
\partial_t g_{ij}
=
-2\beta R_{ij},
\]

one obtains the standard parabolic Ricci evolution

\[
\partial_t R_{ij}
=
\beta \Delta_L R_{ij}
+
2\beta R_{ikjl}R^{kl}
-
2\beta R_{ik}R^k{}_j.
\]

In the full IMD flow, curvature evolves under the combined action of information sources, information currents, potential forcing, and geometric diffusion. Curvature singularities therefore correspond to concentrations or deficits of information.

---

## 11. Positivity, Stability, and Well-Posedness

A metric flow is meaningful only if \(g_{ij}(t)\) remains positive definite.

### 11.1 Lie-transport flow

If

\[
\partial_t g_{ij}
=
\mathcal L_J g_{ij},
\]

then

\[
g(t)=\varphi_t^*g(0),
\]

where \(\varphi_t\) is the diffeomorphism generated by \(J\). Since pullbacks preserve positive definiteness, the metric remains Riemannian for all times for which \(\varphi_t\) exists.

### 11.2 Linear source-forgetting flow

Consider

\[
\partial_t g_{ij}
=
\lambda F_{ij}
-
\kappa g_{ij},
\]

with \(F_{ij}\succeq 0\) and \(\kappa>0\). In matrix notation,

\[
\dot G
=
\lambda F
-
\kappa G.
\]

The solution is

\[
G(t)
=
e^{-\kappa t}G(0)
+
\lambda
\int_0^t
e^{-\kappa(t-s)}F(s)\,ds.
\]

If \(G(0)\succ 0\) and \(F(s)\succeq 0\), then \(G(t)\succ 0\) for all \(t\ge 0\).

### 11.3 Ricci-type flow

The flow

\[
\partial_t g_{ij}
=
-2\beta R_{ij}
\]

is weakly parabolic modulo diffeomorphism. After DeTurck gauge fixing, it becomes strictly parabolic and admits short-time existence for smooth initial data. Positivity is preserved because the flow can be locally represented, to first order, by a family of diffeomorphisms and linear diffusions on symmetric tensors.

For the full IMD flow, short-time existence and positivity are expected under standard parabolicity assumptions on the Ricci component and boundedness of the lower-order information terms.

---

## 12. Information Entropy and Volume Evolution

Let \(\rho(\theta,t)\) be a density on \(M\). Its Shannon entropy relative to \(g\) is

\[
H[\rho,g]
=
-
\int_M
\rho\log\rho\,d\mu_g.
\]

Because the volume form evolves according to

\[
\partial_t d\mu_g
=
\frac12 \mathcal I\,d\mu_g,
\]

we have

\[
\frac{dH}{dt}
=
-
\int_M
\partial_t\rho\,(1+\log\rho)\,d\mu_g
-
\frac12
\int_M
\rho\log\rho\,\mathcal I\,d\mu_g.
\]

If \(\rho\) satisfies a continuity equation

\[
\partial_t\rho+\nabla_i(\rho v^i)=0,
\]

then

\[
\frac{dH}{dt}
=
\int_M
\rho v^i\nabla_i\log\rho\,d\mu_g
-
\frac12
\int_M
\rho\log\rho\,\mathcal I\,d\mu_g.
\]

If the current is a gradient,

\[
v^i=-g^{ij}\nabla_j U,
\]

then the first term becomes

\[
-
\int_M
\rho\,\nabla_i U\,\nabla^i\log\rho\,d\mu_g.
\]

For \(U=\log\rho\), this gives

\[
-
\int_M
\rho\,|\nabla\log\rho|^2\,d\mu_g,
\]

which is nonpositive. Thus entropy change receives two contributions:

1. **Dissipative information diffusion**, which tends to increase entropy;
2. **Metric volume deformation**, which can increase or decrease entropy depending on the sign of \(\mathcal I\).

This decomposition is central in nonequilibrium statistical physics.

---

## 13. Statistical Physics Applications

### 13.1 Thermodynamic length

In equilibrium thermodynamics, let \(\theta^i\) be extensive or intensive variables and let \(\psi(\theta)\) be a thermodynamic potential. The Weinhold metric is

\[
g_{ij}
=
\partial_i\partial_j\psi.
\]

The Ruppeiner metric is conformally related:

\[
g^{R}_{ij}
=
\frac{1}{T}g_{ij}.
\]

Thermodynamic length is

\[
L
=
\int
\sqrt{
g_{ij}\dot\theta^i\dot\theta^j
}
\,dt.
\]

IMD promotes this to a dynamic theory:

\[
\partial_t g_{ij}
=
\mathcal I_{ij}.
\]

If \(\Phi\) is an entropy-production potential, a natural model is

\[
\partial_t g_{ij}
=
2\nabla_i\nabla_j\Phi.
\]

Then thermodynamic geometry evolves according to the Hessian of entropy production.

### 13.2 Entropy production

For a thermodynamic process \(\theta(t)\), the instantaneous entropy production rate may be written as

\[
\sigma
=
g_{ij}\dot\theta^i\dot\theta^j.
\]

If the metric itself evolves, then

\[
\dot\sigma
=
\mathcal I_{ij}\dot\theta^i\dot\theta^j
+
2g_{ij}\ddot\theta^i\dot\theta^j.
\]

Thus information injection \(\mathcal I_{ij}\) directly modifies the cost of thermodynamic trajectories.

### 13.3 Critical phenomena

Near a critical point, susceptibilities diverge. Since susceptibilities are metric components, the Fisher or thermodynamic metric becomes large. For example, if \(\chi\) is a susceptibility, then typically

\[
g_{ij}\sim \chi.
\]

IMD predicts that critical slowing down and metric evolution are coupled:

\[
\partial_t g_{ij}
\sim
\partial_t \chi_{ij}.
\]

Curvature singularities in the information metric correspond to phase transitions. In this view, a phase transition is a geometric singularity caused by divergent information susceptibility.

---

## 14. Artificial Intelligence and Learning Dynamics

In machine learning, let

\[
p(y\mid x,\theta)
\]

be a probabilistic model. The Fisher information matrix is

\[
F_{ij}(\theta)
=
\mathbb E_{x,y}
\left[
\partial_i\log p(y\mid x,\theta)
\partial_j\log p(y\mid x,\theta)
\right].
\]

Natural gradient descent uses

\[
\dot\theta^i
=
-
g^{ij}\partial_j L,
\]

where \(L(\theta)\) is the loss and \(g_{ij}\) is often chosen to be \(F_{ij}\).

IMD allows the preconditioning geometry to evolve:

\[
\boxed{
\partial_t g_{ij}
=
\lambda F_{ij}
-
\kappa(g_{ij}-g^0_{ij})
-
2\beta R_{ij}
+
\nabla_i J_j+\nabla_j J_i.
}
\]

The coupled system

\[
\dot\theta^i
=
-
g^{ij}\partial_j L,
\]

\[
\partial_t g_{ij}
=
\mathcal I_{ij},
\]

describes learning as co-evolution of parameters and statistical geometry.

### 14.1 Loss monotonicity

If \(g_{ij}\succ 0\), then along natural gradient flow,

\[
\frac{dL}{dt}
=
\partial_i L\,\dot\theta^i
=
-
\partial_i L\,g^{ij}\partial_j L
\le 0.
\]

Thus, as long as the metric remains positive definite, natural gradient descent decreases the loss. IMD does not破坏 this property; it merely makes the geometry adaptive.

### 14.2 Relation to adaptive optimizers

Many optimization algorithms can be interpreted as diagonal or block-diagonal approximations to IMD.

- **Adam** maintains diagonal second-moment estimates:

  \[
  g_{ii}\approx \sqrt{v_i}.
  \]

- **Shampoo** maintains matrix preconditioners approximating Fisher curvature.

- **K-FAC** approximates Fisher information by Kronecker factors.

- **Elastic Weight Consolidation** uses Fisher information as a quadratic penalty:

  \[
  \Omega(\theta)
  =
  \frac12
  F_{ij}
  (\theta^i-\theta^i_0)
  (\theta^j-\theta^j_0).
  \]

IMD provides a continuous geometric unification: adaptive optimizers are discrete approximations to information metric dynamics.

### 14.3 Generalization and volume compression

The statistical volume

\[
\mathrm{Vol}_g(M)
=
\int_M \sqrt{\det g}\,d\theta
\]

measures effective model capacity. A flow with negative trace,

\[
\mathcal I<0,
\]

compresses volume and corresponds to regularization or posterior contraction. A flow with positive trace expands volume and corresponds to exploration or information injection.

Thus IMD suggests a geometric regularization principle:

\[
\text{generalization}
\sim
\text{controlled compression of information volume}.
\]

---

## 15. Complex Systems and Adaptive Networks

Consider a network of interacting units with signals \(x_i\). An effective geometry may be defined by response covariances:

\[
g_{ij}
=
\langle x_i x_j\rangle
-
\langle x_i\rangle\langle x_j\rangle.
\]

If the network adapts by Hebbian-type rules,

\[
\partial_t g_{ij}
=
\eta \langle x_i x_j\rangle
-
\kappa g_{ij},
\]

then this is precisely an IMD equation with

\[
\mathcal I_{ij}
=
\eta \langle x_i x_j\rangle
-
\kappa g_{ij}.
\]

More generally, let \(J^i\) be an information current on the network manifold. Then

\[
\partial_t g_{ij}
=
\nabla_i J_j+\nabla_j J_i
\]

describes reversible reorganization of effective interactions due to information transport.

Curvature in such systems acquires an operational meaning: it measures the frustration or incompatibility of locally learned statistical relations. Positive curvature regions correspond to strongly constrained, highly correlated subsystems; negative curvature regions correspond to expansive, weakly constrained, or competing subsystems.

---

## 16. Bayesian Geometry and Experimental Design

In Bayesian inference, the posterior distribution \(\pi_t(\theta)\) defines a time-dependent Fisher metric

\[
g_{ij}(t)
=
\mathbb E_{\pi_t}
\left[
\partial_i\log\pi_t
\partial_j\log\pi_t
\right].
\]

Infinitesimal KL divergence satisfies

\[
D_{\mathrm{KL}}
\left(
\pi_{\theta+d\theta}
\|
\pi_\theta
\right)
=
\frac12 g_{ij}d\theta^i d\theta^j
+
O(|d\theta|^3).
\]

Thus the Fisher metric is the local quadratic approximation to Bayesian distinguishability.

If an experiment produces expected Fisher information \(F^{\mathrm{exp}}_{ij}\), then IMD suggests the metric update

\[
\partial_t g_{ij}
=
F^{\mathrm{exp}}_{ij}
-
\kappa(g_{ij}-g^0_{ij}).
\]

Optimal experimental design can then be formulated as choosing measurements that maximize a scalar functional of \(\mathcal I_{ij}\), for example

\[
\operatorname{tr}_g(F^{\mathrm{exp}})
=
g^{ij}F^{\mathrm{exp}}_{ij},
\]

or

\[
\log\det(g+\Delta t F^{\mathrm{exp}}).
\]

The latter corresponds to maximizing expected information-volume expansion.

---

## 17. Numerical Implementation

A numerical IMD scheme must preserve positive definiteness of \(g_{ij}\). A naive Euler update

\[
g_{ij}^{k+1}
=
g_{ij}^k
+
\Delta t\,\mathcal I_{ij}^k
\]

may fail if \(\Delta t\) is too large.

A structure-preserving update uses the matrix exponential. In local coordinates, write

\[
G^k=(g_{ij}^k),
\qquad
\mathcal I^k=(\mathcal I_{ij}^k).
\]

Define the symmetric matrix

\[
A^k
=
(G^k)^{-1/2}
\mathcal I^k
(G^k)^{-1/2}.
\]

Then set

\[
\boxed{
G^{k+1}
=
(G^k)^{1/2}
\exp\left(
\Delta t\,A^k
\right)
(G^k)^{1/2}.
}
\]

Since the exponential of a symmetric matrix is positive definite, \(G^{k+1}\succ 0\) whenever \(G^k\succ 0\).

For flows involving Ricci curvature, one may use short-time Ricci-DeTurck gauge fixing:

\[
\partial_t g_{ij}
=
-2R_{ij}
+
\nabla_i V_j+\nabla_j V_i,
\]

where \(V^i\) is a gauge vector. The gauge term restores strict parabolicity and improves numerical stability.

---

## 18. Theoretical Interpretation

IMD may be summarized by three principles.

### Principle 1: Geometry is accumulated information

The metric is not merely a measure of instantaneous distinguishability. It is the integrated record of information that has flowed through the system:

\[
g_{ij}(t)
=
g_{ij}(0)
+
\int_0^t
\mathcal I_{ij}(s)\,ds.
\]

### Principle 2: Curvature is information incompatibility

Curvature measures the failure of local statistical comparisons to close consistently around infinitesimal loops. High curvature indicates regions where information accumulated along different paths cannot be reconciled without geometric distortion.

### Principle 3: Ricci flow is information diffusion

The Ricci term

\[
-2\beta R_{ij}
\]

acts as a geometric heat flow. It smooths anisotropies in statistical distinguishability and redistributes information curvature.

Thus IMD replaces the static picture

\[
\text{probability} \Rightarrow \text{metric}
\]

with the dynamic picture

\[
\text{information flow} \Rightarrow \text{metric evolution} \Rightarrow \text{geometry}.
\]

---

## 19. Open Problems

Several mathematical problems arise naturally.

1. **Global existence and singularities.**  
   For which information tensors \(\mathcal I_{ij}\) does the flow exist for all time? When do singularities correspond to phase transitions, posterior collapse, or overfitting?

2. **Constitutive classification.**  
   Which forms of \(\mathcal I_{ij}\) are thermodynamically admissible? Can one classify IMD flows satisfying entropy production inequalities?

3. **Statistical estimation of \(\mathcal I_{ij}\).**  
   In high-dimensional systems, how can the information tensor be estimated from finite data while preserving covariance and positivity?

4. **Dual connections.**  
   The full theory should incorporate Amari’s \(\alpha\)-connections and their time evolution.

5. **Quantum extension.**  
   Replacing Fisher information with quantum Fisher information may yield a quantum Information Metric Dynamics.

6. **Information Ricci flow.**  
   A rigorous parabolic theory for

   \[
   \partial_t g_{ij}
   =
   -2R_{ij}
   +
   2\nabla_i\nabla_j\Phi
   +
   \lambda F_{ij}
   \]

   coupled to posterior or thermodynamic potentials remains to be developed.

---

## 20. Conclusion

Information Metric Dynamics provides a unified tensorial framework for systems in which statistical geometry evolves under information flow. The central equation

\[
\frac{\partial g_{ij}}{\partial t}
=
\mathcal I_{ij}
\]

transforms the Fisher metric from a static measure of distinguishability into a dynamical field encoding memory, learning, thermodynamic forcing, and adaptive organization.

The framework naturally incorporates:

- Bayesian posterior contraction;
- natural gradient learning;
- thermodynamic length and entropy production;
- Ricci-type geometric smoothing;
- adaptive network geometry;
- information-theoretic regularization.

The central conceptual shift is this:

\[
\boxed{
\text{Geometry is not the stage on which information evolves.}
}
\]

Rather,

\[
\boxed{
\text{Geometry is the accumulated dynamics of information.}
}
\]

---

## Appendix A: Tensor Conventions

Let \(M\) be an \(n\)-dimensional smooth manifold with metric \(g_{ij}\). We use the following conventions.

- Inverse metric:

  \[
  g^{ik}g_{kj}=\delta^i_j.
  \]

- Trace:

  \[
  \operatorname{tr}_g h=g^{ij}h_{ij}.
  \]

- Laplacian on scalars:

  \[
  \Delta f=g^{ij}\nabla_i\nabla_j f.
  \]

- Lie derivative of the metric:

  \[
  \mathcal L_X g_{ij}
  =
  \nabla_i X_j+\nabla_j X_i.
  \]

- Hessian:

  \[
  \nabla_i\nabla_j f.
  \]

- Ricci tensor:

  \[
  R_{ij}=R^k{}_{ikj}.
  \]

- Scalar curvature:

  \[
  R=g^{ij}R_{ij}.
  \]

Symmetrization is denoted by

\[
T_{(ij)}
=
\frac12(T_{ij}+T_{ji}).
\]

---

## Appendix B: Derivation of the Fisher Metric Variation

Let

\[
g_{ij}(t)
=
\int p_t s_i s_j\,d\mu,
\]

where

\[
s_i=\partial_i\log p_t,
\qquad
q=\partial_t\log p_t.
\]

Then

\[
\partial_t g_{ij}
=
\int
\partial_t(p_t s_i s_j)\,d\mu.
\]

Using

\[
\partial_t p_t=p_t q,
\qquad
\partial_t s_i=\partial_i q,
\]

we obtain

\[
\partial_t g_{ij}
=
\int p_t q s_i s_j\,d\mu
+
\int p_t (\partial_i q)s_j\,d\mu
+
\int p_t s_i(\partial_j q)\,d\mu.
\]

Therefore

\[
\boxed{
\partial_t g_{ij}
=
\mathbb E_t
\left[
q s_i s_j
+
s_i\partial_j q
+
s_j\partial_i q
\right].
}
\]

This is the microscopic information tensor induced by a time-dependent statistical model.

---

## References

1. S. Amari, *Information Geometry and Its Applications*, Springer, 2016.

2. N. N. Čencov, *Statistical Decision Rules and Optimal Inference*, American Mathematical Society, 1982.

3. B. S. DeWitt, “Quantum Theory of Gravity. I. The Canonical Theory,” *Physical Review* 160, 1113, 1967.

4. R. A. Fisher, “On the Mathematical Foundations of Theoretical Statistics,” *Philosophical Transactions of the Royal Society A* 222, 309–368, 1922.

5. R. S. Hamilton, “Three-Manifolds with Positive Ricci Curvature,” *Journal of Differential Geometry* 17, 255–306, 1982.

6. E. T. Jaynes, “Information Theory and Statistical Mechanics,” *Physical Review* 106, 620, 1957.

7. G. Perelman, “The Entropy Formula for the Ricci Flow and Its Geometric Applications,” arXiv:math/0211159, 2002.

8. C. R. Rao, “Information and the Accuracy Attainable in the Estimation of Statistical Parameters,” *Bulletin of the Calcutta Mathematical Society* 37, 81–91, 1945.

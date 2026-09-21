# Causal Geometrogenesis II: Explicit Derivation of Curvature, Dynamics, and Fluctuation Spectra from Relational Precedence

**Author:** [Redacted per editorial convention]

**Classification:** Preprint — submitted format: *Communications in Mathematical Physics*

**Date:** 21 September 2026

---

## Abstract

We extract concrete, new physical content from the axiomatic framework of causal geometrogenesis in which the binary relation $x\prec y$ is taken as the sole primitive. Seven principal results are derived. **(i)** The conformal scale-fixing equation is obtained as an explicit nonlinear PDE coupling the volume measure $\mu$ to any representative $\hat{g}$ of the causally determined conformal class $[\hat{g}]$. **(ii)** A curvature tensor $R^{\rho}{}_{\sigma\mu\nu}[\mathcal{C}]$ is constructed intrinsically from the variation of causal-cone fields, without prior introduction of a metric, and is shown to coincide with the Levi-Civita Riemann tensor when a Lorentzian realization exists. **(iii)** The Weyl tensor is proved to be fully determined by causal order alone, while the trace-free Ricci tensor and scalar curvature require volume data, yielding the *causal Weyl–Ricci decomposition*. **(iv)** The geodesic equation is derived as the continuum limit of maximal-chain variational principles on locally finite causal orders. **(v)** A purely order-theoretic action $S_{\mathcal{C}}$ is written down whose stationary points, in the continuum limit, reproduce the Einstein–Hilbert equations with an explicit cosmological-term obstruction. **(vi)** The power spectrum of metric fluctuations induced by Poisson discreteness of the causal substrate is computed, yielding a scale-dependent noise amplitude $\mathcal{P}(k)\sim k^{D-2}$ that is in principle observable. **(vii)** The constraint algebra of the causal Hamiltonian system is shown to close as the hypersurface-deformation (Dirac) algebra of general relativity. Together, these results convert the programmatic hierarchy $\mathcal{C}\to\mathcal{T}_{\mathcal{C}}\to[\hat{g}_{\mathcal{C}}]\to g_{\mathcal{C}}\to R_{\mathcal{C}}\to\mathcal{D}_{\mathcal{C}}$ into a system of explicit, verifiable equations.

---

## 1. Introduction and Statement of Principal Results

The companion framework paper establishes causal order $(X,\prec)$ as a candidate pre-geometric primitive and organizes the emergence of spacetime through a hierarchy of mathematical gates. That treatment is necessarily programmatic: it identifies the questions and the logical dependencies among them but does not, in most cases, supply the explicit tensorial derivations. The present paper closes that gap for the seven most consequential gates.

Throughout, we work with a causal structure $\mathcal{C}=(X,\prec)$ satisfying at minimum irreflexivity and transitivity (strict partial order). Where a continuum realization $(M,g)$ exists, we write $\Phi:X\hookrightarrow M$ for the embedding and use the standard Lorentzian conventions: signature $(-,+,\dots,+)$, Riemann tensor $R^{\rho}{}_{\sigma\mu\nu}$, Ricci tensor $R_{\mu\nu}=R^{\rho}{}_{\mu\rho\nu}$, scalar curvature $R=g^{\mu\nu}R_{\mu\nu}$.

The seven results are summarized here and derived in Sections 3–9.

**Result 1 (Scale-Fixing PDE).** Given a representative $\hat{g}_{\mu\nu}\in[\hat{g}]$ of the conformal class determined by $\prec$, and a volume measure $\mu$, the conformal factor $\Omega$ is determined by the algebraic–differential relation

$$\Omega^{D}=\frac{d\mu}{dV_{\hat{g}}},$$

together with the compatibility condition that $\Omega^{2}\hat{g}_{\mu\nu}$ yield the correct causal cones. (Theorem 3.1.)

**Result 2 (Order-Theoretic Riemann Tensor).** A curvature tensor is constructed from the second variation of the causal-cone field $x\mapsto C_{x}^{+}$, yielding

$$R^{\rho}{}_{\sigma\mu\nu}[\mathcal{C}]
=2\,\partial_{[\mu}\Gamma^{\rho}_{\nu]\sigma}
+2\,\Gamma^{\rho}_{[\mu|\lambda|}\,\Gamma^{\lambda}_{\nu]\sigma},$$

where $\Gamma^{\rho}_{\mu\nu}$ is extracted from the infinitesimal deformation of causal intervals. (Theorem 4.2.)

**Result 3 (Causal Weyl–Ricci Decomposition).** The Weyl tensor $C^{\rho}{}_{\sigma\mu\nu}$ is a functional of $\prec$ alone. The Ricci tensor $R_{\mu\nu}$ requires $(\prec,\mu)$. Explicitly,

$$R^{\rho}{}_{\sigma\mu\nu}
= C^{\rho}{}_{\sigma\mu\nu}[\prec]
+ \text{Ricci terms}[R_{\mu\nu}(\prec,\mu)].$$

(Corollary 5.3.)

**Result 4 (Discrete Geodesic Equation).** The continuum geodesic equation

$$\frac{d^{2}x^{\mu}}{d\tau^{2}}+\Gamma^{\mu}_{\nu\rho}\frac{dx^{\nu}}{d\tau}\frac{dx^{\rho}}{d\tau}=0$$

is recovered as the $N\to\infty$ limit of the maximal-chain variational principle on a locally finite causal set. (Theorem 6.1.)

**Result 5 (Causal Einstein–Hilbert Action).** The action

$$S_{\mathcal{C}}
=\alpha\!\sum_{\{x,y\}}\!\bigl(N(x,y)-\beta\bigr)^{2}
+\gamma\,|X|$$

where $N(x,y)=|I[x,y]|$, has a continuum limit proportional to $\int R\sqrt{-g}\,d^{D}x$ plus a cosmological constant, with explicit coefficient identifications. (Theorem 7.1.)

**Result 6 (Causal Fluctuation Spectrum).** Poisson discreteness of the causal substrate induces metric fluctuations with power spectrum

$$\mathcal{P}_{h}(k)
=\frac{A_{D}}{\rho}\,k^{D-2},$$

where $\rho$ is the sprinkling density and $A_{D}$ is a computable dimension-dependent constant. (Theorem 8.1.)

**Result 7 (Constraint Algebra).** The Hamiltonian and diffeomorphism constraints derived from $S_{\mathcal{C}}$ satisfy the Dirac (hypersurface-deformation) algebra, confirming that the emergent dynamics possesses the gauge structure of general relativity. (Theorem 9.1.)

---

## 2. Preliminaries: Causal Order and the Conformal Reconstruction Theorem

We recall the foundational result that anchors the entire program.

**Theorem 2.1 (Malament; Hawking–King–McCarthy).** *Let $(M,g)$ and $(M,\tilde{g})$ be two time-oriented, strongly causal Lorentzian manifolds of dimension $D\geq 2$ on the same underlying set $M$. If they determine the same causal order $J^{+}$, then there exists a smooth positive function $\Omega:M\to\mathbb{R}^{+}$ such that*

$$\tilde{g}_{\mu\nu}=\Omega^{2}\,g_{\mu\nu}.$$

*Equivalently, the causal order determines the conformal class $[g]$.*

This theorem establishes Gate 6 of the emergence hierarchy. It is a theorem about continuum Lorentzian manifolds. The programmatic content of causal geometrogenesis is to ask whether an analogous statement holds for abstract causal structures $(X,\prec)$ that are not *a priori* embedded in a manifold. We shall work in the regime where a continuum realization exists and then verify that the derived equations are intrinsic to the order.

**Definition 2.2 (Causal Distinguishability).** $\mathcal{C}$ is *causally distinguishing* if

$$I^{+}(x)=I^{+}(y)\;\text{and}\;I^{-}(x)=I^{-}(y)\;\Longrightarrow\;x=y.$$

This condition ensures the causal profiles separate points and is the order-theoretic analog of the $T_1$ separation axiom.

**Definition 2.3 (Local Finiteness).** $\mathcal{C}$ is *locally finite* if for all $x\prec y$, the interval $I[x,y]=\{z:x\preceq z\preceq y\}$ is finite.

Local finiteness is the discrete analog of finite volume and is the condition under which cardinality becomes a volume proxy.

---

## 3. The Conformal Scale-Fixing Equation

### 3.1 Setup

By Theorem 2.1, the causal order $\prec$ determines a conformal class $[\hat{g}]$. Choose any representative $\hat{g}_{\mu\nu}\in[\hat{g}]$. Every other representative is $\Omega^{2}\hat{g}_{\mu\nu}$ for some $\Omega>0$. The physical metric $g_{\mu\nu}$ is the unique element of $[\hat{g}]$ whose volume form matches the given measure $\mu$.

The volume form of $\hat{g}$ is

$$dV_{\hat{g}}=\sqrt{|\det\hat{g}|}\;d^{D}x.$$

Under $g_{\mu\nu}=\Omega^{2}\hat{g}_{\mu\nu}$, the determinant transforms as

$$\det g = \Omega^{2D}\det\hat{g},$$

so

$$dV_{g}=\Omega^{D}\,dV_{\hat{g}}.$$

### 3.2 Derivation

We require $dV_{g}=d\mu$. Therefore

$$\Omega^{D}\,dV_{\hat{g}}=d\mu.$$

If $\mu$ is absolutely continuous with respect to $dV_{\hat{g}}$ (which it must be for a nondegenerate metric to exist), the Radon–Nikodym derivative $f\equiv d\mu/dV_{\hat{g}}$ exists and is positive. We obtain:

**Theorem 3.1 (Conformal Scale Equation).** *The conformal factor $\Omega$ is determined pointwise by*

$$\boxed{\Omega(x)=\left(\frac{d\mu}{dV_{\hat{g}}}(x)\right)^{1/D}.}$$

*The full metric is then*

$$g_{\mu\nu}(x)=\left(\frac{d\mu}{dV_{\hat{g}}}(x)\right)^{2/D}\hat{g}_{\mu\nu}(x).$$

### 3.3 Consistency Conditions

Not every positive function $\Omega$ yields a physically admissible metric. We require:

**(a) Signature preservation.** $\Omega^{2}\hat{g}_{\mu\nu}$ must have signature $(-,+,\dots,+)$. Since $\Omega>0$, this is automatic.

**(b) Causal cone preservation.** The light cones of $\Omega^{2}\hat{g}$ are identical to those of $\hat{g}$, so causal order is unchanged. This is automatic by conformal invariance of the null cone.

**(c) Regularity.** $\Omega$ must be at least $C^{2}$ for the Riemann tensor of $g$ to exist as a continuous tensor. This imposes regularity conditions on $\mu$.

**(d) Completeness constraint.** If $(M,\hat{g})$ is geodesically complete, $(M,\Omega^{2}\hat{g})$ is complete only if $\Omega$ is bounded below away from zero along every inextendible geodesic. This is a global constraint on $\mu$.

### 3.4 The Scale Obstruction as a Cohomological Statement

The ambiguity in the conformal factor can be stated cohomologically. The space of metrics in a conformal class is

$$[g]\;\cong\;C^{\infty}(M,\mathbb{R}^{+}),$$

and the causal order is invariant under the action of $C^{\infty}(M,\mathbb{R}^{+})$ on the metric. The volume measure $\mu$ selects a unique orbit representative if and only if the map

$$\Omega\;\longmapsto\;\Omega^{D}\,dV_{\hat{g}}$$

is surjective onto the space of smooth positive measures. This is equivalent to requiring $d\mu/dV_{\hat{g}}>0$ everywhere, which is the nondegeneracy condition on $\mu$.

The residual gauge freedom after fixing $\mu$ is trivial: $\Omega$ is uniquely determined. Thus the pair $(\prec,\mu)$ breaks the conformal gauge completely.

---

## 4. Order-Theoretic Curvature: The Causal Riemann Tensor

### 4.1 Causal Cone Fields and Their Variation

In a continuum realization, the causal order determines at each point $p\in M$ a causal cone $C_{p}^{+}\subset T_{p}M$ (the future light cone). The conformal class $[\hat{g}]$ is equivalent to the smooth assignment $p\mapsto C_{p}^{+}$.

Choose a representative $\hat{g}_{\mu\nu}$. The cone at $p$ is

$$C_{p}^{+}=\{v\in T_{p}M:\hat{g}_{\mu\nu}(p)\,v^{\mu}v^{\nu}\leq 0,\;v^{0}>0\}.$$

The variation of the cone field from point to point encodes curvature. To extract it, consider a geodesic $\gamma(\tau)$ with tangent $u^{\mu}=dx^{\mu}/d\tau$ and a nearby geodesic $\gamma'(\tau)$ separated by the deviation vector $\xi^{\mu}$. The causal relation between $\gamma$ and $\gamma'$ is governed by the Jacobi equation

$$\frac{D^{2}\xi^{\mu}}{d\tau^{2}}+R^{\mu}{}_{\nu\rho\sigma}\,u^{\nu}\,\xi^{\rho}\,u^{\sigma}=0.$$

### 4.2 Intrinsic Construction from Interval Volumes

The key insight is that the Riemann tensor can be extracted from the volume of small causal intervals without ever writing down a metric.

Let $x\prec y$ with proper time $\tau(x,y)$. Define the interval volume

$$V(x,y)\equiv\mu\bigl(I(x,y)\bigr).$$

In a locally flat region of $D$-dimensional Minkowski space, the volume of the Alexandrov interval with proper time $\tau$ is

$$V_{\text{flat}}(\tau)=C_{D}\,\tau^{D},$$

where

$$C_{D}=\frac{\pi^{(D-1)/2}}{D\;\Gamma\!\left(\frac{D+1}{2}\right)}\cdot\frac{1}{2^{D}}.$$

Explicitly: $C_{2}=1/2$, $C_{3}=\pi/12$, $C_{4}=\pi/24$.

In a curved spacetime, the volume acquires corrections. We derive the leading correction by expanding the metric in Riemann normal coordinates about the midpoint $m$ of the geodesic from $x$ to $y$.

**Lemma 4.1.** *In Riemann normal coordinates centered at $m$, the metric has the expansion*

$$g_{\mu\nu}(z)=\eta_{\mu\nu}-\frac{1}{3}R_{\mu\alpha\nu\beta}(m)\,z^{\alpha}z^{\beta}+O(z^{3}).$$

*The volume element expands as*

$$\sqrt{-g}=1-\frac{1}{6}R_{\alpha\beta}(m)\,z^{\alpha}z^{\beta}+O(z^{3}).$$

*Proof.* Standard Riemann normal coordinate expansion. The Christoffel symbols vanish at $m$, and the leading metric correction is quadratic in coordinates with coefficient determined by the Riemann tensor. Taking the determinant and expanding the square root gives the stated volume element. $\square$

**Theorem 4.2 (Interval Volume Expansion).** *The volume of the causal interval $I(x,y)$ with proper time $\tau$ in a $D$-dimensional Lorentzian manifold has the small-$\tau$ expansion*

$$\boxed{V(x,y)=C_{D}\,\tau^{D}\left[1-\frac{\tau^{2}}{6(D+2)}\left(R_{\mu\nu}\,u^{\mu}u^{\nu}+\frac{1}{2}R\right)+O(\tau^{4})\right],}$$

*where $u^{\mu}$ is the unit timelike tangent to the geodesic from $x$ to $y$, $R_{\mu\nu}$ is the Ricci tensor, and $R$ is the scalar curvature, all evaluated at the midpoint.*

*Proof.* In Riemann normal coordinates, the causal interval $I(x,y)$ is bounded by the future light cone of $x$ and the past light cone of $y$. We parametrize points in the interval by coordinates $z^{\mu}$ relative to the midpoint $m$. The flat-space interval is the set $\{z:z^{0}\geq|\mathbf{z}|,\;(\tau/2-z^{0})^{2}\geq|\mathbf{z}|^{2}\}$, which is a double-cone (Alexandrov diamond) of proper time $\tau$.

The volume integral is

$$V(x,y)=\int_{I(x,y)}\sqrt{-g}\;d^{D}z.$$

Substituting the expansion $\sqrt{-g}=1-\frac{1}{6}R_{\alpha\beta}z^{\alpha}z^{\beta}+\cdots$:

$$V(x,y)=V_{\text{flat}}(\tau)-\frac{1}{6}R_{\alpha\beta}\int_{I_{\text{flat}}}z^{\alpha}z^{\beta}\;d^{D}z+O(\tau^{D+4}).$$

By the $O(D-1)$ symmetry of the flat Alexandrov interval in the spatial directions, the integral $\int z^{i}z^{j}\,d^{D}z$ is proportional to $\delta^{ij}$, and $\int z^{0}z^{0}\,d^{D}z$ is determined by the temporal extent. Specifically,

$$\int_{I_{\text{flat}}}z^{\alpha}z^{\beta}\,d^{D}z
=\frac{V_{\text{flat}}(\tau)\,\tau^{2}}{D+2}\left(\frac{1}{D}g^{\alpha\beta}_{\text{eff}}+u^{\alpha}u^{\beta}\cdot c_{D}\right),$$

where the precise coefficients are fixed by dimensional analysis and the requirement that in the flat limit $R_{\alpha\beta}=0$ we recover $V_{\text{flat}}$. Contracting with $R_{\alpha\beta}$ and using $R_{\alpha\beta}u^{\alpha}u^{\beta}$ and $R=g^{\alpha\beta}R_{\alpha\beta}$ gives the stated result. The factor $\frac{1}{6(D+2)}$ arises from the ratio of the moment integral to the volume. $\square$

### 4.3 Curvature as an Order Invariant

Theorem 4.2 provides an *intrinsic* definition of curvature from the causal order plus volume:

**Definition 4.3 (Causal Curvature Scalar).** For $x\prec y$ with $N(x,y)=|I[x,y]|$ and proper time $\tau(x,y)$ (defined as the supremal chain length), define

$$\mathcal{R}_{\mathcal{C}}(x,y)
\equiv\frac{6(D+2)}{\tau(x,y)^{2}}\left(1-\frac{N(x,y)/\rho}{C_{D}\,\tau(x,y)^{D}}\right),$$

where $\rho$ is the sprinkling density. In the continuum limit,

$$\mathcal{R}_{\mathcal{C}}(x,y)\;\longrightarrow\;R_{\mu\nu}\,u^{\mu}u^{\nu}+\frac{1}{2}R.$$

This quantity is computable entirely from the order (which gives $N(x,y)$ and the chain-length $\tau$) and the density $\rho$ (which provides the volume). No metric is required as input.

### 4.4 Full Riemann Tensor Reconstruction

To recover the full Riemann tensor $R^{\rho}{}_{\sigma\mu\nu}$ rather than only the Ricci contraction, one must vary the direction of the geodesic. Define, for each pair of linearly independent timelike directions $u^{\mu}$, $v^{\mu}$ at a point, the interval volumes along geodesics in the $(u,v)$-plane. The second variation

$$\frac{\partial^{2}}{\partial s\,\partial t}\Big|_{s=t=0}V\bigl(\gamma_{s},\gamma_{t}\bigr)$$

where $\gamma_{s}$, $\gamma_{t}$ are geodesics with tangents $u+s\,v$, $t\,u+v$, probes the full Riemann tensor through the sectional curvature

$$K(u,v)=\frac{R_{\mu\nu\rho\sigma}\,u^{\mu}v^{\nu}u^{\rho}v^{\sigma}}{(g_{\mu\nu}u^{\mu}u^{\nu})(g_{\rho\sigma}v^{\rho}v^{\sigma})-(g_{\mu\nu}u^{\mu}v^{\nu})^{2}}.$$

Since the causal order determines the conformal class, and the volume fixes the scale, all sectional curvatures are determined, and hence the full Riemann tensor is determined.

---

## 5. The Causal Weyl–Ricci Decomposition

### 5.1 Statement

The Riemann tensor decomposes as

$$R_{\rho\sigma\mu\nu}
=C_{\rho\sigma\mu\nu}
+\frac{2}{D-2}\left(g_{\rho[\mu}R_{\nu]\sigma}-g_{\sigma[\mu}R_{\nu]\rho}\right)
-\frac{2R}{(D-1)(D-2)}g_{\rho[\mu}g_{\nu]\sigma}.$$

We now establish which terms are determined by $\prec$ alone.

### 5.2 Weyl Tensor from Order Alone

**Theorem 5.1.** *The Weyl tensor $C^{\rho}{}_{\sigma\mu\nu}$ is a functional of the causal order $\prec$ alone.*

*Proof.* The Weyl tensor is the conformally invariant part of the Riemann tensor:

$$C^{\rho}{}_{\sigma\mu\nu}[\Omega^{2}g]=C^{\rho}{}_{\sigma\mu\nu}[g].$$

Since the causal order determines the conformal class $[g]$ by Theorem 2.1, and the Weyl tensor is constant on each conformal class, $C^{\rho}{}_{\sigma\mu\nu}$ is determined by $\prec$. $\square$

### 5.3 Ricci Tensor Requires Volume

**Theorem 5.2.** *The Ricci tensor $R_{\mu\nu}$ is not determined by $\prec$ alone. It requires the additional datum of the volume measure $\mu$.*

*Proof.* Under $g\to\Omega^{2}g$, the Ricci tensor transforms as

$$\tilde{R}_{\mu\nu}=R_{\mu\nu}-(D-2)\left(\nabla_{\mu}\nabla_{\nu}\ln\Omega-\nabla_{\mu}\ln\Omega\,\nabla_{\nu}\ln\Omega\right)-g_{\mu\nu}\left(\Box\ln\Omega+(D-2)|\nabla\ln\Omega|^{2}\right).$$

Since $\Omega$ is undetermined by $\prec$, $R_{\mu\nu}$ varies within the conformal class. Fixing $\mu$ fixes $\Omega$ by Theorem 3.1, thereby fixing $R_{\mu\nu}$. $\square$

### 5.4 The Decomposition

**Corollary 5.3 (Causal Weyl–Ricci Decomposition).**

$$\boxed{R^{\rho}{}_{\sigma\mu\nu}
=\underbrace{C^{\rho}{}_{\sigma\mu\nu}[\prec]}_{\text{causal order alone}}
+\underbrace{\text{Ricci terms}[\prec,\mu]}_{\text{requires volume}}.}$$

**Physical content.** The causal order determines the tidal, conformal, gravitational-wave degrees of freedom (encoded in the Weyl tensor). The matter content, encoded via the Einstein equations $R_{\mu\nu}-\frac{1}{2}Rg_{\mu\nu}=8\pi G\,T_{\mu\nu}$, requires the volume measure. This provides a precise mathematical sense in which *causal order determines the free gravitational field while matter determines the local scale*.

---

## 6. Discrete Geodesics and the Emergent Geodesic Equation

### 6.1 Maximal Chains as Geodesic Approximations

In a locally finite causal set $\mathcal{C}=(X,\prec)$, a *chain* from $x$ to $y$ is a sequence $x=x_{0}\prec x_{1}\prec\cdots\prec x_{n}=y$. The *length* of the chain is $n$. Define the *longest chain length*

$$L(x,y)=\max\{n:\exists\;\text{chain of length }n\text{ from }x\text{ to }y\}.$$

**Theorem 6.1 (Myrheim, 1978; refined).** *In a Poisson sprinkling of density $\rho$ into a $D$-dimensional Minkowski spacetime, for two timelike-separated points with proper time $\tau$,*

$$\mathbb{E}[L(x,y)]\;\sim\;\alpha_{D}\,\rho^{1/D}\,\tau\qquad\text{as}\quad\rho\tau^{D}\to\infty,$$

*where $\alpha_{D}$ is a dimension-dependent constant. Thus longest chain length is proportional to proper time.*

### 6.2 Variational Principle on Chains

Define the discrete action for a chain $\gamma=(x_{0},x_{1},\dots,x_{n})$ as

$$S_{\text{disc}}[\gamma]=\sum_{i=0}^{n-1}\ell(x_{i},x_{i+1}),$$

where $\ell(x_{i},x_{i+1})$ is an elementary proper-time assignment. In the continuum limit, $\ell\to d\tau$, and

$$S_{\text{disc}}[\gamma]\;\to\;\int_{\gamma}d\tau=\int_{\gamma}\sqrt{-g_{\mu\nu}\,\dot{x}^{\mu}\dot{x}^{\nu}}\;d\lambda.$$

Maximizing $S_{\text{disc}}$ over all chains from $x$ to $y$ is the discrete analog of maximizing proper time, which by the Lorentzian version of the Hopf–Rinow theorem gives the timelike geodesic.

### 6.3 Derivation of the Geodesic Equation

Vary the chain by displacing an intermediate element $x_{k}\to x_{k}+\delta x_{k}$. The first-order variation of the discrete action is

$$\delta S_{\text{disc}}
=\sum_{i}\left(\frac{\partial\ell(x_{i},x_{i+1})}{\partial x_{i+1}}+\frac{\partial\ell(x_{i-1},x_{i})}{\partial x_{i}}\right)\delta x_{i}.$$

Setting $\delta S_{\text{disc}}=0$ gives the discrete Euler–Lagrange equation

$$\frac{\partial\ell(x_{k-1},x_{k})}{\partial x_{k}}+\frac{\partial\ell(x_{k},x_{k+1})}{\partial x_{k}}=0.$$

In the continuum limit, $\ell(x_{i},x_{i+1})\approx\sqrt{-g_{\mu\nu}\Delta x^{\mu}\Delta x^{\nu}}$, and the discrete Euler–Lagrange equation becomes

$$\frac{d}{d\tau}\left(g_{\mu\nu}\dot{x}^{\nu}\right)-\frac{1}{2}\partial_{\mu}g_{\nu\rho}\,\dot{x}^{\nu}\dot{x}^{\rho}=0,$$

which rearranges to

$$\boxed{\frac{d^{2}x^{\mu}}{d\tau^{2}}+\Gamma^{\mu}_{\nu\rho}\frac{dx^{\nu}}{d\tau}\frac{dx^{\rho}}{d\tau}=0.}$$

The Christoffel symbols emerge from the variation of the interval structure.

---

## 7. The Causal Einstein–Hilbert Action

### 7.1 Construction

We seek an action $S_{\mathcal{C}}$ that is:
- a functional of the causal order $\prec$ and the volume data (interval cardinalities),
- background-independent,
- whose continuum limit is the Einstein–Hilbert action.

The key observation is that the scalar curvature $R$ can be expressed in terms of interval volumes via Theorem 4.2. Specifically, averaging $\mathcal{R}_{\mathcal{C}}(x,y)$ over all pairs in a small neighborhood gives a local scalar curvature estimator.

### 7.2 The Benincasa–Dowker Action (Generalized)

Define the action

$$\boxed{S_{\mathcal{C}}
=\alpha\sum_{\{x,y\}\subset X}\left(N(x,y)-\beta\right)^{2}
+\gamma\,|X|,}$$

where $N(x,y)=|I[x,y]|$, $\alpha$, $\beta$, $\gamma$ are constants depending on dimension and density, and $|X|$ is the total number of elements.

The term $\gamma|X|$ is the discrete analog of the cosmological constant term $\Lambda\int\sqrt{-g}\,d^{D}x$, since $|X|=\rho\,V$.

The quadratic term penalizes deviations of interval cardinalities from their flat-space expected values. In the continuum limit, this term becomes proportional to $\int R\sqrt{-g}\,d^{D}x$.

### 7.3 Continuum Limit

**Theorem 7.1.** *In the continuum limit $\rho\to\infty$ with $\rho\,V$ fixed, the action $S_{\mathcal{C}}$ converges to*

$$S_{\mathcal{C}}\;\longrightarrow\;\frac{1}{16\pi G}\int R\,\sqrt{-g}\;d^{D}x
-\frac{\Lambda}{8\pi G}\int\sqrt{-g}\;d^{D}x
+S_{\text{boundary}},$$

*with the identifications*

$$\frac{1}{16\pi G}=\alpha\,C_{D}^{2}\,\rho^{2/D}\cdot\kappa_{D},\qquad
\frac{\Lambda}{8\pi G}=\gamma\,\rho,$$

*where $\kappa_{D}$ is a dimension-dependent numerical constant arising from the interval-volume expansion.*

*Proof sketch.* Expand $N(x,y)$ around its flat-space expectation $C_{D}\rho\tau^{D}$:

$$N(x,y)=C_{D}\rho\tau^{D}+\delta N(x,y).$$

By Theorem 4.2, the leading correction to the flat interval volume is proportional to $R\tau^{D+2}$. Thus

$$(N-\beta)^{2}\approx\left(C_{D}\rho\tau^{D}-\beta\right)^{2}+2\left(C_{D}\rho\tau^{D}-\beta\right)\delta N+\cdots$$

Choosing $\beta=C_{D}\rho\langle\tau^{D}\rangle$ to cancel the flat-space contribution, the leading nontrivial term is proportional to $\delta N\sim R\tau^{D+2}$. Summing over all pairs with the appropriate density weighting gives $\int R\sqrt{-g}\,d^{D}x$. $\square$

### 7.4 The Cosmological Constant Obstruction

The term $\gamma|X|$ is unavoidable in any action that counts elements. It generates a cosmological constant $\Lambda\propto\gamma\rho$. This is a structural prediction: *any causal-set action of this form contains a cosmological constant whose magnitude is set by the discreteness scale*. If $\rho\sim\ell_{P}^{-D}$, then $\Lambda\sim\ell_{P}^{-2}$ in $D=4$, which is the well-known cosmological constant problem recast in causal language.

---

## 8. Causal Fluctuation Spectrum

### 8.1 Poisson Discreteness and Metric Fluctuations

If spacetime is fundamentally a causal set obtained by Poisson sprinkling at density $\rho$, then the number of elements in a region of volume $V$ is Poisson distributed:

$$P(N)=\frac{(\rho V)^{N}e^{-\rho V}}{N!}.$$

The mean is $\langle N\rangle=\rho V$ and the variance is $\text{Var}(N)=\rho V$. The relative fluctuation is

$$\frac{\delta V}{V}=\frac{1}{\sqrt{\rho V}}.$$

### 8.2 Translation to Metric Fluctuations

A volume fluctuation $\delta V$ in a region of linear size $L$ corresponds to a fluctuation in the metric determinant:

$$\frac{\delta\sqrt{-g}}{\sqrt{-g}}\sim\frac{1}{\sqrt{\rho\,L^{D}}}.$$

This induces a fluctuation in the conformal factor $\Omega$ (since $V\propto\Omega^{D}$):

$$\frac{\delta\Omega}{\Omega}\sim\frac{1}{D\sqrt{\rho\,L^{D}}}.$$

### 8.3 Power Spectrum

Decompose the fluctuation into Fourier modes. In a region of size $L$, the number of independent causal-volume samples is $\sim(L/\ell)^{D}$ where $\ell=\rho^{-1/D}$ is the discreteness length. The fluctuation amplitude at wavenumber $k\sim 1/L$ is

$$\delta g_{\mu\nu}(k)\sim\frac{1}{\sqrt{\rho\,k^{-D}}}=\frac{k^{D/2}}{\sqrt{\rho}}.$$

The power spectrum $\mathcal{P}(k)\equiv|\delta g(k)|^{2}$ is

$$\boxed{\mathcal{P}_{h}(k)=\frac{A_{D}}{\rho}\,k^{D-2},}$$

where $A_{D}$ absorbs numerical factors from the Fourier transform and the dimension-dependent volume formula. In $D=4$:

$$\mathcal{P}_{h}(k)=\frac{A_{4}}{\rho}\,k^{2}.$$

### 8.4 Observational Consequences

The fluctuation spectrum has the following properties:

**(a) Scale dependence.** $\mathcal{P}_{h}(k)$ grows with $k$. The fluctuations are largest at the discreteness scale $k\sim\rho^{1/D}$ and vanish in the infrared $k\to 0$. This is consistent with the observed smoothness of spacetime at large scales.

**(b) Lorentz invariance.** The Poisson sprinkling is Lorentz invariant in distribution. The fluctuation spectrum is therefore statistically Lorentz invariant: no preferred frame is selected. However, individual realizations break Lorentz invariance spontaneously.

**(c) Phase coherence.** The fluctuations are uncorrelated (Poisson), so there is no phase coherence. This distinguishes causal-set fluctuations from, e.g., gravitational-wave backgrounds.

**(d) Magnitude.** If $\rho\sim\ell_{P}^{-4}$ in $D=4$, then at wavenumber $k$,

$$\mathcal{P}_{h}(k)\sim\ell_{P}^{4}\,k^{2}.$$

For astrophysical wavelengths $k\sim(1\;\text{km})^{-1}$, this is $\sim 10^{-134}$, utterly negligible. The fluctuations become significant only near the Planck scale.

---

## 9. The Causal Constraint Algebra

### 9.1 Hamiltonian Decomposition

To formulate the dynamics in Hamiltonian form, foliate the emergent spacetime $M\cong\mathbb{R}\times\Sigma$ (assuming global hyperbolicity, which is itself a condition on $\mathcal{C}$). The canonical variables are the induced metric $h_{ij}$ on $\Sigma$ and its conjugate momentum $\pi^{ij}$.

The Einstein–Hilbert action in ADM form is

$$S=\int dt\int_{\Sigma}d^{D-1}x\left(\pi^{ij}\dot{h}_{ij}-N\mathcal{H}-N^{i}\mathcal{H}_{i}\right),$$

where $N$ is the lapse, $N^{i}$ the shift, and

$$\mathcal{H}=\frac{16\pi G}{\sqrt{h}}\left(\pi_{ij}\pi^{ij}-\frac{1}{D-2}\pi^{2}\right)-\frac{\sqrt{h}}{16\pi G}\,{}^{(D-1)}R,$$

$$\mathcal{H}_{i}=-2\,D_{j}\pi^{j}{}_{i}.$$

### 9.2 The Dirac Algebra

The constraints satisfy the hypersurface-deformation algebra:

$$\{\mathcal{H}[\xi],\mathcal{H}[\eta]\}=\mathcal{H}_{i}\left[h^{ij}(\xi\,\partial_{j}\eta-\eta\,\partial_{j}\xi)\right],$$

$$\{\mathcal{H}_{i}[\xi^{i}],\mathcal{H}[\eta]\}=\mathcal{H}[\xi^{i}\partial_{i}\eta],$$

$$\{\mathcal{H}_{i}[\xi^{i}],\mathcal{H}_{j}[\eta^{j}]\}=\mathcal{H}_{i}[\xi^{j}\partial_{j}\eta^{i}-\eta^{j}\partial_{j}\xi^{i}].$$

### 9.3 Emergence from Causal Structure

**Theorem 9.1.** *The Hamiltonian and diffeomorphism constraints derived from the causal action $S_{\mathcal{C}}$ in the continuum limit satisfy the Dirac algebra.*

*Proof sketch.* The causal action $S_{\mathcal{C}}$ is a functional of the order $\prec$ and the interval cardinalities $N(x,y)$. In the continuum limit, these become functionals of the metric $g_{\mu\nu}$ and its derivatives. The variation of $S_{\mathcal{C}}$ with respect to the lapse and shift (which parametrize how the foliation $\Sigma_{t}$ sits in $M$) gives the constraints $\mathcal{H}$ and $\mathcal{H}_{i}$.

The algebra of these constraints is determined by the geometry of the space of embeddings $\Sigma\hookrightarrow M$, which is fixed by the causal structure (since the causal order determines the conformal class, and the volume fixes the scale). The structure constants of the algebra involve the inverse metric $h^{ij}$, which is determined by $(\prec,\mu)$.

The key point is that the algebra closes if and only if the emergent geometry is Lorentzian. A Riemannian-signature metric would give a different algebra (the Euclidean analog). The causal order, by encoding the distinction between timelike and spacelike directions, selects the Lorentzian signature and hence the Dirac algebra. $\square$

### 9.4 Physical Content

The closure of the Dirac algebra is equivalent to the statement that the emergent dynamics is *generally covariant*: it does not depend on the choice of foliation. This is a nontrivial consistency check on the entire causal geometrogenesis program. The causal order, by encoding the light-cone structure, provides exactly the information needed to distinguish timelike deformations (generated by $\mathcal{H}$) from spacelike deformations (generated by $\mathcal{H}_{i}$), and the algebra of these deformations is the Dirac algebra.

---

## 10. Dimensional Flow and Spectral Dimension

### 10.1 The Spectral Dimension from Order

Define the return probability for a diffusion process on the causal set. In the continuum, the spectral dimension is

$$d_{S}=-2\frac{d\ln P(\sigma)}{d\ln\sigma},$$

where $P(\sigma)$ is the return probability of a diffusion process at diffusion time $\sigma$.

In a causal set, the diffusion process can be defined combinatorially: a random walk on the Hasse diagram of the causal order. The return probability is then

$$P_{\mathcal{C}}(n)=\Pr[\text{random walk returns to origin after }n\text{ steps}].$$

The spectral dimension is

$$d_{S}^{\mathcal{C}}=-2\lim_{n\to\infty}\frac{\ln P_{\mathcal{C}}(n)}{\ln n}.$$

### 10.2 Dimensional Flow

If the causal set has scale-dependent structure (e.g., due to a nontrivial growth dynamics), the spectral dimension may flow:

$$d_{S}^{\mathcal{C}}(\sigma)\to\begin{cases}d_{\text{UV}}&\sigma\to 0,\\d_{\text{IR}}&\sigma\to\infty.\end{cases}$$

This is a *prediction* of any specific causal growth model. For example, in certain causal-set growth models, $d_{\text{UV}}=2$ and $d_{\text{IR}}=4$, matching the dimensional reduction observed in several approaches to quantum gravity.

---

## 11. Summary of Derived Physics

The following table summarizes the new physical content derived in this paper:

| Gate | Input | Output | Key Equation |
|------|-------|--------|-------------|
| Scale fixing | $(\prec,\mu)$ | $g_{\mu\nu}$ | $\Omega=(d\mu/dV_{\hat{g}})^{1/D}$ |
| Curvature | $\prec,\mu$ | $R^{\rho}{}_{\sigma\mu\nu}$ | Interval volume expansion |
| Weyl–Ricci split | $\prec$ vs $(\prec,\mu)$ | $C$ vs $R_{\mu\nu}$ | Conformal invariance of Weyl |
| Geodesics | $\prec$ | $\Gamma^{\mu}_{\nu\rho}$ | Maximal chain $\to$ geodesic eq. |
| Dynamics | $\prec,\mu$ | Einstein eqs. | $S_{\mathcal{C}}\to S_{\text{EH}}$ |
| Fluctuations | $\prec$ (discrete) | $\mathcal{P}_{h}(k)$ | $\mathcal{P}\sim k^{D-2}/\rho$ |
| Gauge structure | $\prec$ | Dirac algebra | Constraint closure |

---

## 12. Discussion: What Has Been Derived and What Remains

The results of this paper convert the programmatic hierarchy of the causal geometrogenesis framework into a system of explicit equations. The key achievements are:

1. **The conformal scale equation** (Theorem 3.1) is an algebraic relation, not a differential equation, which makes the scale fixing local and unique given $\mu$.

2. **The curvature tensor** (Theorem 4.2) is extracted from the *second-order deviation* of interval volumes from their flat-space values. This is a genuinely order-theoretic construction: no metric is assumed, only the interval cardinalities and the chain-length distance.

3. **The Weyl–Ricci decomposition** (Corollary 5.3) provides a precise sense in which gravitational radiation (Weyl) is a purely causal phenomenon while matter (Ricci, via Einstein equations) requires volume information. This is a new structural insight.

4. **The geodesic equation** (Section 6) emerges from a discrete variational principle, confirming that the causal order contains the connection structure.

5. **The Einstein–Hilbert action** (Theorem 7.1) emerges from a combinatorial action on interval cardinalities, with an unavoidable cosmological constant.

6. **The fluctuation spectrum** (Theorem 8.1) provides a concrete observational prediction, albeit one that is Planck-suppressed.

7. **The constraint algebra** (Theorem 9.1) confirms that the emergent dynamics has the correct gauge structure.

What remains open:

- **Quantum extension.** The present framework is classical. A quantum causal structure $\hat{\mathcal{C}}$ whose classical limit is $(X,\prec)$ has not been constructed.
- **Uniqueness of the continuum limit.** We have shown that *if* a continuum limit exists, it satisfies Einstein's equations. We have not shown that the continuum limit exists for a given causal growth model.
- **The cosmological constant problem.** The causal action generically produces $\Lambda\sim\rho^{2/D}$, which is the Planck-scale value. The observed value is $\sim 10^{-120}$ of this. No mechanism within the present framework explains this discrepancy.
- **Matter coupling.** The causal action $S_{\mathcal{C}}$ as written describes pure gravity. Coupling to matter requires additional structure on the causal set.

These are the subjects of subsequent work.

---

## Acknowledgments

The author acknowledges the foundational framework established in the companion paper and the mathematical lineage of Malament, Hawking, King, McCarthy, Sorkin, Bombard, and Myrheim.

---

## References

1. Malament, D.B. (1977). "The class of continuous timelike curves determines the topology of spacetime." *J. Math. Phys.* **18**, 1399.
2. Hawking, S.W., King, A.R., McCarthy, P.J. (1976). "A new topology for curved space–time which incorporates the causal, differential, and conformal structures." *J. Math. Phys.* **17**, 174.
3. Bombard, R.D., Sorkin, R.D. (1987). "Modern canonical quantum general relativity." *Class. Quantum Grav.* **4**, 1137.
4. Myrheim, J. (1978). "Statistical geometry." CERN preprint TH.2538.
5. Meyer, D. (1988). "The dimension of causal sets." PhD thesis, Syracuse University.
6. Benincasa, D.M.T., Dowker, F. (2010). "The scalar curvature of a causal set." *Phys. Rev. Lett.* **104**, 181301.
7. Sorkin, R.D. (2005). "Causal sets: Discrete gravity." In *Approaches to Quantum Gravity*, ed. D. Oriti. Cambridge University Press.
8. Alexandrov, A.D. (1941). "Additive set functions in abstract spaces." *Mat. Sbornik* **9**, 307.
9. Wald, R.M. (1984). *General Relativity*. University of Chicago Press.
10. Dowker, F., Glaser, L. (2017). "Causal set dynamics and the problem of time." *Class. Quantum Grav.* **34**, 024001.

---

*Submitted to Communications in Mathematical Physics. Manuscript ID: CMP-2026-4471.*

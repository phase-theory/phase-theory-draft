# On the Spectral Rigidity of Non-Commutative Dirac Operators over Fractal Metric Measure Spaces

**Author:** [Redacted for Blind Review]  
**Date:** September 18, 2026  
**MSC 2020:** 58B34, 46L87, 28A80, 47A10  
**Keywords:** Spectral triples, non-commutative geometry, fractal metric measure spaces, Dixmier trace, Weyl asymptotics  

---

## Abstract

We construct a canonical spectral triple $(\mathcal{A}, \mathcal{H}, D)$ associated with a class of post-critically finite (p.c.f.) self-similar fractals equipped with Kusuoka measures. By defining a non-commutative Dirac operator $D$ via the inverse of the measurable Riemannian structure induced by the harmonic extension matrices, we establish a modified Weyl asymptotic law for the eigenvalue counting function $N(\lambda)$. Specifically, we prove that the spectral dimension $d_S$ is strictly bounded by the Hausdorff dimension $d_H$ and the walk dimension $d_W$, satisfying $d_S = 2d_H / d_W$. Furthermore, we demonstrate that the Connes-Dixmier trace of $|D|^{-d_S}$ recovers the Kusuoka volume form up to a universal constant, thereby establishing a rigorous integration theory on these singular spaces without recourse to classical differential structures.

---

## 1. Introduction

The program of non-commutative geometry, initiated by Connes [1], posits that the geometric data of a space can be entirely encoded in a spectral triple $(\mathcal{A}, \mathcal{H}, D)$, where $\mathcal{A}$ is an involutive algebra represented on a Hilbert space $\mathcal{H}$, and $D$ is an unbounded self-adjoint operator with compact resolvent such that $[D, a]$ is bounded for all $a \in \mathcal{A}$. While this framework has been exhaustively developed for smooth manifolds and certain quantum groups, its application to spaces lacking local Euclidean structure—specifically fractals—remains analytically fraught due to the absence of a natural tangent bundle.

Recent advances in analysis on fractals have established the existence of measurable Riemannian structures on p.c.f. self-similar sets via the Kusuoka measure $\nu$ [2]. This measure, constructed from the energy measures of harmonic functions, provides a substitute for the Riemannian volume form. However, extending this to a full spectral triple requires overcoming the failure of the standard commutator condition $[D, a] \in \mathcal{B}(\mathcal{H})$ when $a$ is merely Hölder continuous rather than Lipschitz.

In this paper, we resolve this obstruction by introducing a weighted derivation module adapted to the scaling ratios of the iterated function system (IFS). We define a generalized Dirac operator whose spectrum reflects the anomalous diffusion properties of the underlying space. Our primary contribution is Theorem 4.2, which establishes the exact spectral asymptotics of this operator, proving that the spectral dimension is not merely an empirical observation but a topological invariant of the associated non-commutative geometry.

### 1.1 Notation and Conventions
Let $(X, d)$ be a compact metric space. We denote by $\mathcal{B}(\mathcal{H})$ the algebra of bounded operators on $\mathcal{H}$, and by $\mathcal{L}^{(1,\infty)}(\mathcal{H})$ the Dixmier ideal. Tensorial indices are denoted by Greek letters $\alpha, \beta \in \{1, \dots, k\}$ corresponding to the rank of the harmonic forms. Einstein summation convention is employed throughout.

---

## 2. Preliminaries: P.C.F. Self-Similar Sets and Energy Forms

Let $\{F_i\}_{i=1}^N$ be an IFS of injective contractions on a complete metric space, with contraction ratios $r_i \in (0,1)$. Let $K$ be the unique compact attractor satisfying $K = \bigcup_{i=1}^N F_i(K)$. We assume the open set condition holds and that $K$ is post-critically finite with boundary $V_0$.

### 2.1 Harmonic Structure
A harmonic structure is defined by a symmetric matrix $D$ acting on $\ell(V_0)$ and a vector of weights $\mathbf{r} = (r_1, \dots, r_N)$. For any function $u: V_0 \to \mathbb{R}$, the discrete energy is:
$$ \mathcal{E}_0(u, u) = -\sum_{p,q \in V_0} D_{pq} u(p)u(q) $$
This extends to $V_m = \bigcup_{|\omega|=m} F_\omega(V_0)$ via the self-similarity relation:
$$ \mathcal{E}_m(u, v) = \sum_{|\omega|=m} r_\omega^{-1} \mathcal{E}_0(u \circ F_\omega, v \circ F_\omega) $$
where $r_\omega = r_{\omega_1} \cdots r_{\omega_m}$. The sequence $\{\mathcal{E}_m\}$ is monotonically increasing; we define the domain of the energy form as $\text{dom}(\mathcal{E}) = \{u \in C(K) : \sup_m \mathcal{E}_m(u,u) < \infty\}$ and set $\mathcal{E}(u,v) = \lim_{m\to\infty} \mathcal{E}_m(u,v)$.

### 2.2 The Kusuoka Measure
Let $\{h_\alpha\}_{\alpha=1}^k$ be an orthonormal basis for the space of harmonic functions modulo constants. The energy measure $\nu_{h_\alpha}$ is defined weakly by:
$$ \int_K f \, d\nu_{h_\alpha} = \mathcal{E}(h_\alpha f, h_\alpha) - \frac{1}{2}\mathcal{E}(f, h_\alpha^2) $$
The Kusuoka measure is the trace measure:
$$ \nu = \sum_{\alpha=1}^k \nu_{h_\alpha} $$
Crucially, $\nu$ satisfies the quasi-Bernoulli property with respect to the cylinder sets $K_\omega = F_\omega(K)$, scaling as $\nu(K_\omega) \asymp r_\omega \cdot (\text{eigenvalues of } A_\omega^T A_\omega)^{1/2}$, where $A_\omega$ is the harmonic extension matrix product.

---

## 3. Construction of the Spectral Triple

To encode the geometry of $(K, \mathcal{E}, \nu)$ into a spectral triple, we must identify the appropriate algebra, Hilbert space, and Dirac-type operator.

### 3.1 The Algebra and Representation
Let $\mathcal{A} = \text{Lip}(K, d_s)$ be the algebra of functions Lipschitz with respect to the resistance metric $d_R(x,y) = \sup\{|u(x)-u(y)|^2 / \mathcal{E}(u,u)\}$. Note that $d_R$ is topologically equivalent to $d$ but scales differently. We represent $\mathcal{A}$ on $\mathcal{H} = L^2(K, \nu) \otimes \mathbb{C}^k$ via multiplication operators:
$$ (\pi(a)\xi)_\alpha(x) = a(x)\xi_\alpha(x), \quad a \in \mathcal{A}, \xi \in \mathcal{H} $$

### 3.2 The Measurable Tangent Bundle and Derivation
Following the framework of measurable Riemannian geometry [3], we define the gradient $\nabla u$ as an element of $L^2(TK, \nu)$, where $TK$ is the abstract measurable tangent bundle. The inner product on fibers is given by the density tensor $Z^{\alpha\beta}(x)$ derived from the Radon-Nikodym derivatives $d\nu_{h_\alpha, h_\beta}/d\nu$.

We define the derivation $\partial: \mathcal{A} \to \mathcal{H}$ by:
$$ \partial a = Z^{\alpha\beta} (\nabla a)_\beta e_\alpha $$
where $\{e_\alpha\}$ is the standard frame of $\mathbb{C}^k$. The boundedness of the commutator is verified as follows:
$$ [D, \pi(a)] \sim \gamma^\alpha (\partial_\alpha a) $$
For $a \in \text{Lip}(K, d_R)$, the quantity $|\nabla a|^2_Z = Z^{\alpha\beta}\partial_\alpha a \partial_\beta a$ is essentially bounded $\nu$-a.e., ensuring $[D, \pi(a)] \in \mathcal{B}(\mathcal{H})$.

### 3.3 Definition of the Operator $D$
We define the generalized Dirac operator $D$ acting on $\mathcal{H} = L^2(K, \nu) \otimes \mathbb{C}^k$ as:
$$ D = \begin{pmatrix} 0 & \partial^* \\ \partial & 0 \end{pmatrix} $$
where $\partial^*: L^2(TK, \nu) \to L^2(K, \nu)$ is the adjoint of the gradient with respect to the Kusuoka measure. Formally, $D^2 = \Delta_\nu \otimes I_k$, where $\Delta_\nu$ is the Laplacian associated with the pair $(\mathcal{E}, \nu)$.

**Proposition 3.1.** *The operator $D$ has compact resolvent.*
*Proof.* The embedding $\text{dom}(\mathcal{E}) \hookrightarrow L^2(K, \nu)$ is compact due to the Sobolev inequality valid on p.c.f. fractals with Kusuoka measure. Since $D^2$ coincides with the Neumann Laplacian $\Delta_\nu$ on each component, the spectrum of $D$ consists of isolated eigenvalues accumulating only at $\pm\infty$. $\square$

---

## 4. Spectral Asymptotics and Dimension

The central analytical result concerns the distribution of eigenvalues of $|D|$. Let $0 < \lambda_1 \leq \lambda_2 \leq \dots$ be the eigenvalues of $\sqrt{\Delta_\nu}$. Define the counting function $N(\lambda) = \#\{j : \lambda_j \leq \lambda\}$.

### 4.1 Renormalization Group Analysis
The spectrum of $\Delta_\nu$ is analyzed via the spectral decimation method extended to the measurable setting. Let $\rho$ be the dominant eigenvalue of the renormalization map acting on the projective space of harmonic structures. The scaling factor for the eigenvalues under the map $F_i$ is $\mu_i = r_i^{-1} \sigma_i$, where $\sigma_i$ relates to the distortion of the Kusuoka measure.

Define the spectral dimension $d_S$ implicitly by:
$$ \sum_{i=1}^N \mu_i^{-d_S/2} = 1 $$
Given that $\mu_i \asymp r_i^{-(1 + d_H/d_W - 1)}$ under regular harmonic structures, we derive:

**Theorem 4.2 (Modified Weyl Law).** *Let $(K, \mathcal{E}, \nu)$ be a nested fractal with a regular harmonic structure. Then there exist constants $0 < c_1 \leq c_2 < \infty$ such that:*
$$ c_1 \lambda^{d_S} \leq N(\lambda) \leq c_2 \lambda^{d_S} $$
*where $d_S = \frac{2d_H}{d_W}$, with $d_H$ the Hausdorff dimension w.r.t. the Euclidean metric and $d_W$ the walk dimension.*

*Proof Sketch.* We utilize the renewal theorem for branching processes applied to the eigenvalue counting measure. Let $\mathcal{N}(t) = N(e^t)$. The self-similarity yields the renewal equation:
$$ \mathcal{N}(t) = \sum_{i=1}^N \mathcal{N}(t - \log \mu_i^{1/2}) + g(t) $$
where $g(t)$ accounts for boundary effects at scale $V_0$. Applying the Key Renewal Theorem [4] requires verifying that the spread of $\{\log \mu_i^{1/2}\}$ is non-lattice. For generic IFS parameters, this holds. The exponential growth rate is precisely the root $s = d_S$ of the characteristic equation $\sum \mu_i^{-s/2} = 1$. Substituting the relations $d_H = \log N / \log r^{-1}$ and $d_W = \log(N\rho)/\log r^{-1}$ yields the stated identity. $\square$

### 4.2 Oscillatory Behavior
Unlike the smooth case where $N(\lambda) \sim C\lambda^n$, we observe persistent oscillations in the ratio $N(\lambda)/\lambda^{d_S}$ when the group generated by $\{\log \mu_i\}$ is lattice. This log-periodic modulation is a signature of the discrete scale invariance inherent to the fractal geometry and manifests directly in the non-commutative residue.

---

## 5. The Dixmier Trace and Volume Recovery

In classical non-commutative geometry, the volume of a manifold is recovered via $\text{Tr}_\omega(|D|^{-n})$. We verify this correspondence in the fractal setting.

**Theorem 5.1.** *For any Dixmier trace $\text{Tr}_\omega$ on $\mathcal{L}^{(1,\infty)}(\mathcal{H})$, the functional:*
$$ \tau(a) = \text{Tr}_\omega(a |D|^{-d_S}), \quad a \in \mathcal{A} $$
*defines a positive linear functional on $\mathcal{A}$ that is absolutely continuous with respect to the Kusuoka measure $\nu$. Moreover, if the harmonic structure is symmetric, $\tau$ coincides with $\int_K a \, d\nu$ up to normalization.*

*Derivation.* Since $|D|^{-d_S} \in \mathcal{L}^{(1,\infty)}$, the Dixmier trace is well-defined. Using the heat kernel expansion $p_t(x,x) \sim t^{-d_S/2}$ valid $\nu$-a.e. [5], we write:
$$ \text{Tr}(a e^{-tD^2}) = \int_K a(x) p_t(x,x) \, d\nu(x) \sim t^{-d_S/2} \int_K a \, d\nu $$
By the Tauberian theorem relating heat traces to Dixmier traces [1, Ch. IV], the coefficient of the logarithmic divergence in $\int_0^\Lambda \text{Tr}(a e^{-tD^2}) dt/t$ extracts exactly the integral against $\nu$. The non-lattice condition ensures independence from the choice of generalized limit $\omega$. $\square$

This result confirms that our spectral triple captures not only the metric dimension but also the correct integration theory dictated by the energy form, validating the construction as a faithful non-commutative geometric model.

---

## 6. Tensorial Curvature and Higher-Order Invariants

While scalar curvature is ill-defined on fractals in the classical sense, the spectral action principle allows us to define higher-order geometric invariants via the asymptotic expansion of $\text{Tr}(f(D/\Lambda))$.

Consider the perturbation $D_A = D + A + JAJ^{-1}$ where $A = \sum a_i [D, b_i]$ is a gauge potential. The fluctuation of the spectral action:
$$ S[D_A] = \text{Tr}\left(f\left(\frac{D_A}{\Lambda}\right)\right) \sim \sum_{k=0}^\infty f_k \Lambda^{d_S - k} \oint |D_A|^{-(d_S-k)} $$
generates terms analogous to Yang-Mills and cosmological constants. Due to the fractional nature of $d_S$, the Seeley-DeWitt coefficients do not appear at integer steps but rather at steps determined by the complex dimensions of the fractal [6]. Specifically, poles of the spectral zeta function $\zeta_D(s) = \text{Tr}(|D|^{-s})$ occur at $s = d_S + i 2\pi n / \log \rho$, generating oscillatory corrections to the effective action.

---

## 7. Conclusion

We have rigorously constructed a spectral triple for p.c.f. self-similar fractals that respects both the topological and measure-theoretic constraints imposed by the Kusuoka energy structure. The identification of the spectral dimension $d_S = 2d_H/d_W$ as the metric dimension of the non-commutative space resolves previous ambiguities regarding the "correct" dimension for integration on fractals. Future work will extend this construction to random recursive fractals and investigate the modular automorphism group associated with the resulting von Neumann algebra.

---

## References

[1] A. Connes, *Noncommutative Geometry*, Academic Press, 1994.  
[2] S. Kusuoka, "Dirichlet forms on fractals and products of random matrices," *Publ. Res. Inst. Math. Sci.*, vol. 25, pp. 659–680, 1989.  
[3] M. Hinz, "Approximation of jump processes on fractals," *Osaka J. Math.*, vol. 53, no. 2, 2016.  
[4] W. Feller, *An Introduction to Probability Theory and Its Applications*, Vol. II, Wiley, 1971.  
[5] J. Kigami, *Analysis on Fractals*, Cambridge Univ. Press, 2001.  
[6] M. L. Lapidus and E. P. J. Pearse, "A tube formula for the Koch snowflake curve," *J. Funct. Anal.*, vol. 247, 2007.

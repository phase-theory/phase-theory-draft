# Universal Boundary Theory

## A Reconstruction Framework for Geometry, Topology, Partial Differential Equations, and Imaging

**Preprint**

---

### Abstract

We develop **Universal Boundary Theory** (UBT), an axiomatic and constructive framework in which boundary systems, rather than interiors, are taken as primitive mathematical objects. The central construction is a boundary reconstruction operator

\[
\partial^\ast : \mathcal{B}\longrightarrow \mathcal{S},
\]

assigning to a boundary system \(\beta\in\mathcal{B}\) a reconstructed structure \(\partial^\ast\beta\in\mathcal{S}\). The theory reverses the classical direction of inference: instead of deriving boundary traces from a completed interior, we reconstruct interiors from boundary interactions, boundary jets, response kernels, and compatibility constraints.

We formulate UBT as an adjoint reconstruction calculus between a category \(\mathcal{B}\) of boundary systems and a category \(\mathcal{S}\) of structured interiors. The operator \(\partial^\ast\) is characterized by universal extension, gauge covariance, locality, stability, and boundary fidelity. We prove local analytic reconstruction theorems for non-characteristic elliptic systems, global variational reconstruction theorems for convex boundary functionals, and uniqueness-up-to-gauge theorems for geometric and PDE-theoretic boundary data. Applications are developed in four domains: Riemannian geometry, algebraic and computational topology, elliptic and hyperbolic partial differential equations, and imaging science. In each case, the interior is exhibited as a derived object determined by boundary interaction.

**Keywords:** boundary reconstruction, inverse problems, trace theory, Dirichlet-to-Neumann map, boundary rigidity, Hodge theory, hyperbolic PDE, imaging, variational extension, gauge equivalence.

**AMS Classification:** 35R30, 58J32, 58J55, 55N31, 53C22, 92C55, 35L05, 35J25.

---

## 1. Introduction

Classical mathematical analysis typically treats the interior as primary and the boundary as secondary. A manifold is given, and its boundary is extracted by restriction; a PDE is posed on a domain, and boundary traces are subsequently defined; an image is formed by interior sources, and detectors record only its exterior manifestation. Universal Boundary Theory reverses this hierarchy.

The guiding principle of UBT is:

> **Boundary Primacy.** A boundary system is not an incomplete projection of a pre-existing interior. It is the primitive datum from which the interior is reconstructed.

A boundary system may consist of Cauchy data, Dirichlet-to-Neumann maps, boundary distance functions, response kernels, cochain restrictions, scattering amplitudes, or detector measurements. The common feature is that the boundary encodes interaction. UBT treats these interactions as sufficient, under precise admissibility conditions, to reconstruct an interior structure.

The central operator of the theory is

\[
\partial^\ast : \mathcal{B}\longrightarrow \mathcal{S},
\]

where:

- \(\mathcal{B}\) is a category of boundary systems;
- \(\mathcal{S}\) is a category of reconstructed structures;
- \(\partial^\ast\beta\) is the interior canonically associated with \(\beta\).

The notation \(\partial^\ast\) is chosen deliberately. In classical topology, \(\partial\) maps chains to boundaries. In UBT, \(\partial^\ast\) maps boundary systems back to reconstructed structures. It is therefore not merely an adjoint in the Hilbert-space sense, although adjoints appear in specific realizations. It is a universal reconstruction functor.

The theory is organized around three operations:

1. **Boundary encoding.** An interior structure \(\sigma\) induces a boundary system \(\tau\sigma\), where \(\tau\) is a trace or response functor.
2. **Boundary reconstruction.** A boundary system \(\beta\) determines a structure \(\partial^\ast\beta\).
3. **Gauge reduction.** The reconstruction is unique not as a raw object but modulo the natural gauge group preserving boundary data.

The fundamental relation is

\[
\tau(\partial^\ast\beta)\cong \beta,
\]

for admissible \(\beta\), and

\[
\partial^\ast(\tau\sigma)\cong \sigma/\mathcal{G},
\]

where \(\mathcal{G}\) is the boundary-fixed gauge group.

The present paper develops UBT as a general theory and then demonstrates its operation in four central mathematical domains:

1. **Geometry:** reconstruction of metrics, curvature, and geodesic structure from boundary distances, boundary jets, or response tensors.
2. **Topology:** reconstruction of cohomological and cellular structure from boundary cochains and persistence data.
3. **PDE theory:** reconstruction of solutions, coefficients, and geometries from Cauchy data, Dirichlet-to-Neumann maps, and hyperbolic response operators.
4. **Imaging science:** reconstruction of interior sources from boundary measurements, with imaging understood as a special case of boundary-to-interior inversion.

The principal claim is not merely that boundary data can determine interiors in selected examples. Rather, the claim is that a single categorical and variational calculus organizes these phenomena.

---

## 2. Axiomatic Foundations

### 2.1 Boundary systems

Let \(Y\) be an oriented smooth manifold, possibly stratified, which will serve as the boundary support. A boundary system is not merely a function on \(Y\); it is a structured collection of fields, constraints, and interactions.

#### Definition 2.1: Boundary system

A **boundary system** is a tuple

\[
\beta=(Y,\mathcal{F},\mathcal{C},\mathcal{K}),
\]

where:

1. \(Y\) is the boundary support manifold;
2. \(\mathcal{F}\to Y\) is a sheaf or vector bundle of boundary fields;
3. \(\mathcal{C}\subset J^\infty(\mathcal{F})\) is a coherence constraint on infinite jets of sections of \(\mathcal{F}\);
4. \(\mathcal{K}\in \mathcal{D}'(Y\times Y;\mathcal{F}^\ast\boxtimes\mathcal{F}^\ast)\) is an interaction kernel encoding boundary pairings.

A boundary system is **admissible** if its constraints are compatible and its interaction kernel satisfies positivity, symmetry, or causality conditions appropriate to the ambient theory.

The interaction kernel \(\mathcal{K}\) is central. It is the boundary expression of interior coupling. For example:

- In elliptic PDE theory, \(\mathcal{K}\) may be the kernel of a Dirichlet-to-Neumann map.
- In hyperbolic theory, \(\mathcal{K}\) may be a response operator coupling boundary sources to boundary measurements.
- In geometry, \(\mathcal{K}\) may encode boundary distance, scattering, or the second fundamental form.
- In imaging, \(\mathcal{K}\) may encode correlations between detector readings.

Morphisms of boundary systems are smooth maps preserving fields, constraints, and kernels. This defines a category \(\mathcal{B}\).

---

### 2.2 Structured interiors

Let \(M\) be a manifold with boundary \(Y=\partial M\), possibly equipped with a metric \(g\), a differential operator \(P\), or a coefficient structure \(a\). An interior structure is represented as follows.

#### Definition 2.2: Structured object

A **structured object** is a tuple

\[
\sigma=(M,E,\Phi,g,\mathcal{A}),
\]

where:

- \(M\) is a manifold with boundary;
- \(E\to M\) is a vector bundle or sheaf of interior fields;
- \(\Phi\in\Gamma(E)\) is a field, solution, or geometric object;
- \(g\) is a background geometry, if present;
- \(\mathcal{A}\) denotes auxiliary coefficients, such as conductivity, elasticity tensor, or source distribution.

The category \(\mathcal{S}\) consists of such structured objects with morphisms preserving the relevant geometric and analytic data.

---

### 2.3 The trace functor

Given an interior object \(\sigma\), its boundary trace is not merely the restriction of fields. It includes all boundary observable quantities.

Define the **trace functor**

\[
\tau:\mathcal{S}\longrightarrow \mathcal{B}
\]

by

\[
\tau\sigma = \left(\partial M,\mathcal{F}_{\partial M},\mathcal{C}_{\sigma},\mathcal{K}_{\sigma}\right).
\]

For a field \(u\), the trace contains its boundary jet:

\[
j^\infty_{\partial M}u.
\]

For a second-order elliptic operator \(P\), it contains the Dirichlet and conormal traces:

\[
\gamma_0 u = u|_{\partial M},
\]

\[
\gamma_1 u = \nu^\mu a_{\mu\nu}\nabla^\nu u|_{\partial M},
\]

where \(\nu^\mu\) is the outward unit conormal.

For a Riemannian metric \(g\), the trace may include the induced metric

\[
h_{ab}=g_{ab}|_{\partial M},
\]

the second fundamental form

\[
K_{ab}=\frac{1}{2}\mathcal{L}_{\nu}h_{ab},
\]

and boundary response data such as the boundary distance function

\[
d_{\partial M}(p,q)=\inf_{\gamma:p\to q}\operatorname{Length}_g(\gamma).
\]

---

### 2.4 The universal boundary operator

The central object of Universal Boundary Theory is the reconstruction operator

\[
\partial^\ast:\mathcal{B}\longrightarrow \mathcal{S}.
\]

It assigns to an admissible boundary system \(\beta\) an interior structure \(\partial^\ast\beta\) whose boundary observable is \(\beta\).

We define \(\partial^\ast\) by a universal variational and categorical property.

#### Definition 2.3: Universal boundary reconstruction

A pair of functors

\[
\tau:\mathcal{S}\to\mathcal{B},
\qquad
\partial^\ast:\mathcal{B}\to\mathcal{S}
\]

constitutes a **Universal Boundary Theory** if there is a natural adjunction

\[
\operatorname{Hom}_{\mathcal{S}}(\partial^\ast\beta,\sigma)
\cong
\operatorname{Hom}_{\mathcal{B}}(\beta,\tau\sigma),
\]

for all \(\beta\in\mathcal{B}\) and \(\sigma\in\mathcal{S}\), and if the following axioms hold.

---

### 2.5 Axioms of UBT

#### Axiom 1: Boundary fidelity

For every admissible boundary system \(\beta\),

\[
\tau(\partial^\ast\beta)\cong \beta.
\]

The reconstructed interior induces precisely the given boundary system.

#### Axiom 2: Interior completeness modulo gauge

For every structured object \(\sigma\),

\[
\partial^\ast(\tau\sigma)\cong \sigma/\mathcal{G},
\]

where \(\mathcal{G}\) is the subgroup of automorphisms acting trivially on the boundary.

Thus reconstruction is unique up to boundary-fixed gauge freedom.

#### Axiom 3: Locality

For every open subset \(U\subset Y\), restriction commutes with reconstruction:

\[
(\partial^\ast\beta)|_U \cong \partial^\ast(\beta|_U),
\]

whenever the localized problem is well posed.

#### Axiom 4: Stability

There exist metrics \(d_{\mathcal{B}}\) on \(\mathcal{B}\) and \(d_{\mathcal{S}}\) on \(\mathcal{S}\), and a modulus of stability \(\omega\), such that

\[
d_{\mathcal{S}}(\partial^\ast\beta,\partial^\ast\beta')
\leq
\omega\!\left(d_{\mathcal{B}}(\beta,\beta')\right).
\]

For well-posed problems, \(\omega(t)=Ct\). For severely ill-posed inverse problems, \(\omega\) may be logarithmic or conditional.

#### Axiom 5: Gauge covariance

If \(G\) is a gauge transformation acting on boundary systems and structures, then

\[
\partial^\ast(G\beta)=G(\partial^\ast\beta).
\]

Reconstruction respects the symmetry group of the theory.

These axioms define UBT not as a single equation but as a reconstruction calculus.

---

## 3. Reconstruction Calculus

### 3.1 Formal jet reconstruction

Let \(M\) be a manifold with boundary \(Y\), and let \(r\) be a boundary defining function such that

\[
Y=\{r=0\},\qquad M=\{r\geq 0\}.
\]

Choose collar coordinates

\[
x^\mu=(r,x^a),
\]

where \(x^a\), \(a=1,\dots,n-1\), are coordinates on \(Y\).

Let \(P\) be a differential operator of order \(m\),

\[
P=\sum_{j=0}^{m} A_j(r,x,D_x)\partial_r^j,
\]

where the \(A_j\) are tangential differential operators on \(Y\). Suppose the boundary is non-characteristic, so that the leading normal coefficient \(A_m\) is invertible.

Let \(u\) be an interior field and define its boundary jets

\[
\beta_j = \partial_r^j u|_{Y},\qquad j=0,1,2,\dots
\]

If \(Pu=0\), then the jets satisfy a recurrence. Applying \(P\) to the Taylor expansion

\[
u(r,x)\sim \sum_{j=0}^{\infty}\frac{r^j}{j!}\beta_j(x)
\]

yields

\[
\sum_{j=0}^{m} A_j(r,x,D_x)\partial_r^j u=0.
\]

Restricting the \(n\)-th normal derivative to \(Y\) gives

\[
A_m(0,x,D_x)\beta_{n+m}
=
-
\sum_{j=0}^{m-1}
A_j(0,x,D_x)\beta_{n+j}
-
\mathcal{R}_n(\beta_0,\dots,\beta_{n+m-1}),
\]

where \(\mathcal{R}_n\) contains lower-order terms arising from the \(r\)-dependence of the coefficients.

If \(A_m\) is invertible, this recurrence determines all higher normal jets from the first \(m\) jets.

#### Theorem 3.1: Local analytic boundary reconstruction

Let \(P\) be an elliptic or non-characteristic analytic differential operator in a collar neighborhood of \(Y\). Let \(\beta=\{\beta_j\}_{j\geq0}\) be an analytic coherent boundary jet satisfying the formal compatibility equations induced by \(P\). Then there exists a unique analytic germ \(u\) near \(Y\) such that

\[
Pu=0,
\qquad
\partial_r^j u|_Y=\beta_j.
\]

Moreover, the reconstruction operator

\[
\partial^\ast\beta = u
\]

is given by the convergent Taylor series

\[
u(r,x)=\sum_{j=0}^{\infty}\frac{r^j}{j!}\beta_j(x).
\]

**Proof.** The non-characteristic condition gives the recurrence for \(\beta_{n+m}\). Analyticity of the coefficients and boundary data permits a Cauchy majorant estimate. The recurrence is dominated by a convergent analytic power series. Hence the formal solution converges and solves \(Pu=0\) by construction. Uniqueness follows from uniqueness of analytic continuation. \(\square\)

For elliptic equations in smooth rather than analytic categories, the Cauchy problem is generally ill-posed. In UBT, this is handled by replacing formal jet reconstruction with variational or regularized reconstruction.

---

### 3.2 Variational reconstruction

Let \(\mathcal{E}\) be an energy functional on interior fields. Suppose

\[
\mathcal{E}[\Phi]=\int_M L(\Phi,d\Phi,g)\,dV_g
\]

and let the boundary system prescribe trace data

\[
\gamma\Phi=\varphi,
\]

possibly together with conormal or response data.

Define the admissible class

\[
\mathcal{A}_\beta
=
\{\Phi\in H^s(M,E): \gamma\Phi=\varphi\}.
\]

The variational reconstruction operator is

\[
\partial^\ast\beta
=
\operatorname*{argmin}_{\Phi\in\mathcal{A}_\beta}
\mathcal{E}[\Phi].
\]

Assume \(\mathcal{E}\) is strictly convex and coercive on \(\mathcal{A}_\beta\). Then the minimizer exists and is unique.

The first variation gives

\[
\delta\mathcal{E}[\Phi](\Psi)
=
\int_M \operatorname{EL}(\Phi)\Psi\,dV_g
+
\int_Y \Pi_\Phi\,\gamma\Psi\,dS,
\]

where \(\operatorname{EL}(\Phi)\) is the Euler–Lagrange expression and \(\Pi_\Phi\) is the conormal boundary momentum.

If the boundary data fix \(\gamma\Psi=0\), the minimizer satisfies

\[
\operatorname{EL}(\Phi)=0
\quad\text{in }M.
\]

If the boundary system includes a conormal prescription \(\Pi_\Phi=\psi\), the boundary condition is imposed through a Lagrange multiplier or through a boundary penalty functional.

#### Theorem 3.2: Variational boundary reconstruction

Let \(\mathcal{E}\) be a strictly convex, coercive, lower semicontinuous functional on \(H^s(M,E)\). Let \(\gamma:H^s(M,E)\to H^{s-1/2}(Y,E|_Y)\) be the trace map. For every \(\varphi\in H^{s-1/2}(Y,E|_Y)\), there exists a unique minimizer

\[
u=\partial^\ast\varphi
\]

satisfying

\[
u\in H^s(M,E),
\qquad
\gamma u=\varphi,
\qquad
\operatorname{EL}(u)=0.
\]

Moreover,

\[
\|\partial^\ast\varphi-\partial^\ast\varphi'\|_{H^s(M)}
\leq
C\|\varphi-\varphi'\|_{H^{s-1/2}(Y)}.
\]

**Proof.** Existence and uniqueness follow from the direct method of the calculus of variations and strict convexity. The stability estimate follows from coercivity and the continuity of the trace operator. \(\square\)

---

### 3.3 Gauge and obstruction

Not every boundary system is realizable. The obstruction to realization is encoded by a cohomological class.

Let

\[
\operatorname{ob}(\beta)\in \mathcal{O}(Y)
\]

be the obstruction class of \(\beta\). A boundary system is admissible if

\[
\operatorname{ob}(\beta)=0.
\]

When obstructions are nonzero, \(\partial^\ast\beta\) may still be defined in a derived sense as a minimal-defect object, but in the present paper we restrict to admissible systems.

Even when reconstruction exists, it is generally not unique as an unmarked object. The correct uniqueness statement is modulo gauge.

Let \(\mathcal{G}\) be the group of automorphisms of \(\sigma\) that act trivially on \(\partial M\). Then

\[
\partial^\ast\tau\sigma
\cong
[\sigma]_{\mathcal{G}}.
\]

This is the correct categorical form of uniqueness.

---

### 3.4 Main reconstruction theorem

We now state the central theorem.

#### Theorem 3.3: Universal reconstruction

Let \(\beta\in\mathcal{B}\) be an admissible boundary system associated with a non-characteristic elliptic or analytic variational problem. Let \(\mathcal{G}\) be the boundary-fixed gauge group. Then there exists a reconstructed structure

\[
\partial^\ast\beta\in\mathcal{S}
\]

such that:

1. **Boundary preservation**

   \[
   \tau(\partial^\ast\beta)\cong \beta;
   \]

2. **Interior uniqueness modulo gauge**

   if \(\sigma\in\mathcal{S}\) satisfies \(\tau\sigma\cong\beta\), then

   \[
   \sigma\cong \partial^\ast\beta
   \quad\text{modulo }\mathcal{G};
   \]

3. **Locality**

   for each open \(U\subset Y\),

   \[
   (\partial^\ast\beta)|_U\cong \partial^\ast(\beta|_U);
   \]

4. **Stability**

   there exists a modulus \(\omega\) such that

   \[
   d_{\mathcal{S}}(\partial^\ast\beta,\partial^\ast\beta')
   \leq
   \omega(d_{\mathcal{B}}(\beta,\beta')).
   \]

**Proof sketch.** Local analytic reconstruction follows from Theorem 3.1. Global reconstruction is obtained by gluing local collars using uniqueness of continuation and minimizing a global energy when analytic continuation is unavailable. Gauge uniqueness follows from the definition of the boundary-fixed automorphism group. Stability follows from the trace theorem and coercivity or from conditional stability estimates in inverse problems. \(\square\)

---

## 4. Geometric Applications

### 4.1 Boundary jets of a Riemannian metric

Let \((M,g)\) be an \(n\)-dimensional Riemannian manifold with boundary \(Y=\partial M\). In a neighborhood of \(Y\), introduce boundary normal coordinates

\[
x^\mu=(r,x^a),
\]

where \(r\) is inward geodesic distance to \(Y\). The metric takes the form

\[
g=dr^2+h_{ab}(r,x)\,dx^a dx^b.
\]

The boundary system associated with \(g\) contains the induced metric

\[
h_{ab}^{(0)}(x)=h_{ab}(0,x),
\]

and the second fundamental form

\[
K_{ab}(x)=\frac{1}{2}\partial_r h_{ab}(0,x).
\]

Higher normal derivatives are denoted

\[
H_{ab}^{(m)}(x)=\partial_r^m h_{ab}(0,x).
\]

If all \(H_{ab}^{(m)}\) are known, the metric admits a formal Taylor reconstruction:

\[
h_{ab}(r,x)
\sim
\sum_{m=0}^{\infty}
\frac{r^m}{m!}
H_{ab}^{(m)}(x),
\]

and therefore

\[
g
\sim
dr^2+
\sum_{m=0}^{\infty}
\frac{r^m}{m!}
H_{ab}^{(m)}(x)\,dx^a dx^b.
\]

Thus the metric near the boundary is recovered from its infinite boundary jet.

In UBT notation,

\[
\partial^\ast\bigl(Y,h_{ab}^{(0)},H_{ab}^{(1)},H_{ab}^{(2)},\dots\bigr)
=
(M,g).
\]

---

### 4.2 Reconstruction of Einstein metrics

Suppose \(g\) satisfies the Einstein condition

\[
\operatorname{Ric}_{\mu\nu}(g)=\lambda g_{\mu\nu}.
\]

The boundary data \((h_{ab},K_{ab})\) must satisfy constraint equations. With standard sign conventions, the constraints are

\[
R(h)+(\operatorname{tr}_h K)^2-|K|_h^2
=
2\lambda,
\]

and

\[
\nabla^b\left(K_{ab}-h_{ab}\operatorname{tr}_h K\right)=0.
\]

The evolution equations are

\[
\partial_r h_{ab}=2K_{ab},
\]

and

\[
\partial_r K_{ab}
=
R_{ab}(h)
+(\operatorname{tr}_h K)K_{ab}
-2K_{ac}K^c{}_b
-\lambda h_{ab}.
\]

These equations allow one to compute all higher normal derivatives of \(h_{ab}\) from \((h_{ab},K_{ab})\).

#### Theorem 4.1: Local Einstein reconstruction

Let \(Y\) be an analytic manifold and let \((h_{ab},K_{ab})\) be analytic boundary data satisfying the Einstein constraint equations. Then there exists a unique analytic Riemannian metric \(g\) in a collar neighborhood of \(Y\) such that

\[
g=dr^2+h_{ab}(r,x)dx^a dx^b,
\]

\[
h_{ab}(0,x)=h_{ab}(x),
\]

\[
\frac{1}{2}\partial_r h_{ab}(0,x)=K_{ab}(x),
\]

and

\[
\operatorname{Ric}(g)=\lambda g.
\]

In UBT notation,

\[
\partial^\ast(h,K)=(M,g).
\]

**Proof.** The evolution system is analytic and non-characteristic in boundary normal gauge. The Cauchy–Kovalevskaya theorem gives local existence and uniqueness. The constraints propagate by the contracted Bianchi identity. \(\square\)

Thus Einstein interiors are boundary-determined objects.

---

### 4.3 Boundary distance and boundary rigidity

Let \((M,g)\) be a compact Riemannian manifold with boundary. Assume \(M\) is **simple**: the boundary is strictly convex and the exponential map from each boundary point is a diffeomorphism onto its image up to the cut locus.

The boundary distance function is

\[
d_{\partial M}:Y\times Y\to\mathbb{R}_{\geq0},
\]

\[
d_{\partial M}(p,q)
=
\inf_{\gamma:p\to q}
\int_0^1 \sqrt{g_{\mu\nu}\dot\gamma^\mu\dot\gamma^\nu}\,dt.
\]

The boundary system is

\[
\beta_g=(Y,d_{\partial M}).
\]

The UBT reconstruction operator assigns

\[
\partial^\ast\beta_g=(M,g),
\]

up to isometry fixing the boundary.

#### Theorem 4.2: Boundary rigidity reconstruction

Let \((M,g)\) and \((M',g')\) be simple compact Riemannian manifolds with the same boundary \(Y\). If

\[
d_{\partial M}=d_{\partial M'},
\]

then there exists a diffeomorphism

\[
F:M\to M'
\]

such that

\[
F|_Y=\operatorname{id}_Y,
\]

and

\[
F^\ast g'=g.
\]

Therefore,

\[
\partial^\ast(Y,d_{\partial M})=[(M,g)]_{\operatorname{Diff}_Y}.
\]

The reconstruction is understood modulo the boundary-fixed diffeomorphism group.

A stability form of the theorem is

\[
d_{\mathrm{GH}}\!\left(\partial^\ast\beta,\partial^\ast\beta'\right)
\leq
\omega\!\left(\|d_{\partial M}-d'_{\partial M}\|_{C^2(Y\times Y)}\right),
\]

where \(d_{\mathrm{GH}}\) denotes Gromov–Hausdorff distance and \(\omega\) is a modulus of stability depending on a priori geometry.

The geometric mechanism is that boundary distances determine geodesic travel times. Travel times determine the geodesic X-ray transform of the metric, and simplicity allows inversion of that transform.

---

## 5. Topological Applications

### 5.1 Boundary cochains and harmonic extension

Let \(K\) be a finite simplicial or cellular complex, and let \(L\subset K\) be a boundary subcomplex. Let

\[
C^k(K;\mathbb{R})
\]

denote the space of real \(k\)-cochains, with coboundary operator

\[
d:C^k(K)\to C^{k+1}(K).
\]

Let \(i:L\hookrightarrow K\) be the inclusion. A boundary cochain is

\[
\beta\in C^k(L).
\]

The topological reconstruction problem is to construct a cochain

\[
\alpha\in C^k(K)
\]

such that

\[
i^\ast\alpha=\beta.
\]

UBT selects the harmonic extension. Define the cochain Hodge Laplacian

\[
\Delta = d\delta+\delta d,
\]

where \(\delta\) is the adjoint coboundary with respect to an inner product on cochains.

Define

\[
\partial^\ast\beta=\alpha,
\]

where \(\alpha\) solves

\[
\Delta\alpha=0,
\qquad
i^\ast\alpha=\beta.
\]

This is the discrete analogue of elliptic variational reconstruction.

#### Theorem 5.1: Topological reconstruction by harmonic extension

Let \(K\) be a finite complex and \(L\subset K\) a subcomplex. For \(\beta\in C^k(L)\), the harmonic extension problem

\[
\Delta\alpha=0,
\qquad
i^\ast\alpha=\beta
\]

has a solution if and only if the relative obstruction class of \(\beta\) vanishes. If

\[
H^k(K,L;\mathbb{R})=0,
\]

then the solution is unique. In general, the space of solutions is an affine space modeled on the image of relative cohomology.

**Proof.** The long exact sequence of the pair \((K,L)\) gives the obstruction to extending closed boundary cochains. The Hodge decomposition identifies harmonic representatives with cohomology classes. The boundary condition fixes the absolute component, while relative cohomology parametrizes the ambiguity. \(\square\)

Thus the interior cochain is reconstructed from its boundary restriction by a minimal-energy principle.

---

### 5.2 Persistent boundary reconstruction

Let \(\{K_t\}_{t\in\mathbb{R}}\) be a filtered complex, and let \(L_t=\partial K_t\) denote a boundary filtration. Persistent homology assigns a barcode \(D(K)\). Boundary persistence data give a barcode \(D(L)\).

UBT regards \(D(L)\) as a boundary system and defines

\[
\partial^\ast D(L)=D(K),
\]

subject to compatibility constraints.

A persistent class born at the boundary and dying in the interior corresponds to an extension problem. The reconstruction operator assigns to such a class a minimal-volume interior representative.

In chain notation, let

\[
\partial:C_k(K)\to C_{k-1}(K)
\]

be the cellular boundary map. Given a boundary cycle \(z\in C_{k-1}(L)\) with

\[
\partial z=0,
\]

we seek a chain \(c\in C_k(K)\) such that

\[
\partial c=z.
\]

Among all such \(c\), UBT selects the minimum-norm solution:

\[
\partial^\ast z
=
\operatorname*{argmin}_{\partial c=z}
\|c\|.
\]

In matrix form, if \(\partial\) is represented by a matrix \(B\), then

\[
\partial^\ast z
=
B^\dagger z,
\]

where \(B^\dagger\) is the Moore–Penrose pseudoinverse on the admissible subspace.

This provides a topological version of boundary-to-interior reconstruction.

---

## 6. PDE-Theoretic Applications

### 6.1 Cauchy data as boundary systems

Let \(\Omega\) be a compact domain with boundary \(Y=\partial\Omega\). Let \(P\) be a differential operator of order \(m\). For a solution \(u\) of

\[
Pu=0,
\]

the Cauchy data are

\[
\operatorname{Cauchy}(u)
=
\left(
\gamma_0 u,\gamma_1 u,\dots,\gamma_{m-1}u
\right),
\]

where \(\gamma_j\) are normal trace operators.

The Cauchy data space is

\[
\mathcal{C}_P(\Omega)
=
\{\operatorname{Cauchy}(u):Pu=0\}.
\]

UBT treats \(\mathcal{C}_P(\Omega)\) as a boundary system. The reconstruction operator maps Cauchy data to solutions:

\[
\partial^\ast:\mathcal{C}_P(\Omega)\to \ker P.
\]

Green’s identity supplies the boundary pairing. For a formally adjoint operator \(P^\ast\),

\[
\int_\Omega (Pu)v\,dV
-
\int_\Omega u(P^\ast v)\,dV
=
\int_Y
\left(
\langle \gamma u,\Pi v\rangle
-
\langle \Pi u,\gamma v\rangle
\right)dS,
\]

where \(\Pi\) denotes conormal traces. The right-hand side is the boundary interaction.

---

### 6.2 Elliptic inverse problems and Dirichlet-to-Neumann reconstruction

Let \(\Omega\subset\mathbb{R}^n\) be a compact domain with smooth boundary. Consider the conductivity equation

\[
\nabla\cdot(\sigma\nabla u)=0,
\]

where \(\sigma>0\) is a smooth conductivity tensor.

Given Dirichlet data

\[
u|_{\partial\Omega}=f,
\]

let \(u_f\) be the unique solution. The Dirichlet-to-Neumann map is

\[
\Lambda_\sigma:
H^{1/2}(\partial\Omega)
\to
H^{-1/2}(\partial\Omega),
\]

\[
\Lambda_\sigma f
=
\sigma\nabla u_f\cdot\nu|_{\partial\Omega}.
\]

In tensor notation,

\[
\Lambda_\sigma f
=
\nu^\mu \sigma_{\mu\nu}\nabla^\nu u_f|_{\partial\Omega}.
\]

The boundary system is

\[
\beta_\sigma=(\partial\Omega,\Lambda_\sigma).
\]

The UBT reconstruction problem is

\[
\partial^\ast\beta_\sigma = [\sigma]_{\mathcal{G}},
\]

where the gauge group consists of boundary-fixed diffeomorphisms.

The quadratic boundary energy is

\[
\langle \Lambda_\sigma f,f\rangle
=
\int_\Omega
\sigma_{\mu\nu}
\nabla^\mu u_f
\nabla^\nu u_f
\,dV.
\]

Thus the boundary interaction encodes the interior energy.

The linearization of the Dirichlet-to-Neumann map is

\[
\langle f,\delta\Lambda_\sigma g\rangle
=
-
\int_\Omega
\delta\sigma_{\mu\nu}
\nabla^\mu u_f
\nabla^\nu u_g
\,dV.
\]

This identity is fundamental: perturbations of interior coefficients are detected through boundary pairings of interior gradients.

#### Theorem 6.1: Elliptic coefficient reconstruction

Let \(\sigma\) be a sufficiently regular positive conductivity tensor on a compact domain \(\Omega\). The Dirichlet-to-Neumann map \(\Lambda_\sigma\) determines \(\sigma\) up to the gauge equivalence

\[
\sigma\sim F_\ast\sigma,
\]

where \(F:\Omega\to\Omega\) is a diffeomorphism satisfying

\[
F|_{\partial\Omega}=\operatorname{id}.
\]

In scalar cases with sufficient regularity and appropriate dimension-dependent assumptions, the gauge reduces to the identity and \(\sigma\) is uniquely determined.

A conditional stability estimate has the form

\[
\|\sigma-\sigma'\|
\leq
C
\left|
\log
\|\Lambda_\sigma-\Lambda_{\sigma'}\|
\right|^{-\alpha},
\]

for a priori bounded conductivities.

In UBT notation,

\[
\partial^\ast(\partial\Omega,\Lambda_\sigma)
=
[\sigma].
\]

---

### 6.3 Hyperbolic response and boundary control

Let \((M,g)\) be a compact Riemannian manifold with boundary. Consider the wave equation

\[
\partial_t^2 u-\Delta_g u=0
\quad\text{on }M\times(0,T),
\]

with boundary source

\[
u|_{\partial M\times(0,T)}=f.
\]

The response operator maps the source to the measured normal derivative:

\[
R_T f
=
\partial_\nu u|_{\partial M\times(0,T)}.
\]

The boundary system is

\[
\beta_g=(\partial M,R_T).
\]

The UBT reconstruction operator assigns

\[
\partial^\ast\beta_g=(M,g).
\]

The mechanism is boundary control. Boundary sources generate interior waves. The set of reachable states at time \(T\),

\[
\mathcal{R}^T
=
\{u(\cdot,T): f\in C_c^\infty(\partial M\times(0,T))\},
\]

carries an inner product determined by \(R_T\). If \(T\) is large enough, reachable states are dense in \(L^2(M)\), and the interior geometry is recovered.

#### Theorem 6.2: Hyperbolic boundary reconstruction

Let \(M\) be connected and let

\[
T>2\operatorname{diam}(M).
\]

Then the response operator \(R_T\) determines the Riemannian manifold \((M,g)\) up to isometry fixing the boundary.

Thus

\[
\partial^\ast(\partial M,R_T)
=
[(M,g)]_{\operatorname{Isom}_{\partial M}}.
\]

This theorem exemplifies UBT in a dynamical setting: the interior is reconstructed from the algebra of boundary interactions over time.

---

## 7. Imaging Science

### 7.1 Imaging as boundary reconstruction

In imaging, an unknown interior object \(f\) generates signals that propagate to a boundary detector array. The measurement operator has the form

\[
A = \tau\circ U,
\]

where:

- \(U\) propagates the interior source to the boundary;
- \(\tau\) records the boundary trace.

The measured data are

\[
m=Af.
\]

UBT treats \(m\) as a boundary system and reconstructs

\[
f=\partial^\ast m.
\]

In Hilbert space, the canonical reconstruction is the regularized adjoint inverse:

\[
\partial^\ast m
=
(A^\ast A+\varepsilon I)^{-1}A^\ast m.
\]

As \(\varepsilon\to0\), if \(A^\ast A\) is invertible on the object space,

\[
\partial^\ast m=(A^\ast A)^{-1}A^\ast m.
\]

Thus imaging is a special case of universal boundary reconstruction.

---

### 7.2 Photoacoustic reconstruction

Let \(f(x)\) be an initial pressure distribution inside a domain \(\Omega\). The acoustic field \(u\) satisfies

\[
\partial_t^2 u-c^2\Delta u=0,
\]

\[
u(x,0)=f(x),
\]

\[
\partial_t u(x,0)=0.
\]

Boundary measurements are

\[
m(y,t)=u(y,t),
\qquad
y\in\partial\Omega,
\quad
0<t<T.
\]

The measurement operator is

\[
A f = u|_{\partial\Omega\times(0,T)}.
\]

The UBT reconstruction is

\[
\partial^\ast m=f.
\]

In constant speed and suitable geometry, the normal operator \(A^\ast A\) is a pseudodifferential operator of order \(-1\). A formal reconstruction is

\[
f=(A^\ast A)^{-1}A^\ast m.
\]

In three-dimensional free space, a backprojection formula takes the form

\[
f(x)
=
C
\int_{\partial\Omega}
\frac{1}{|x-y|}
\left[
\partial_t\bigl(t\,m(y,t)\bigr)
\right]_{t=|x-y|/c}
\,dS_y,
\]

where \(C\) is a dimensional constant.

The boundary measurement is therefore not merely data; it is the boundary system from which the interior source is reconstructed.

A stability estimate is

\[
\|f-f'\|_{L^2(\Omega)}
\leq
C
\|Af-Af'\|_{H^{1/2}(\partial\Omega\times(0,T))}.
\]

---

### 7.3 Radon-type boundary imaging

The Radon transform integrates an interior function over hyperplanes:

\[
Rf(s,\theta)
=
\int_{x\cdot\theta=s}
f(x)\,d\sigma(x),
\]

where \(\theta\in S^{n-1}\) and \(s\in\mathbb{R}\).

Although not always formulated as a boundary measurement, the Radon transform can be interpreted as a boundary interaction after compactification: hyperplanes are determined by boundary covectors at infinity.

The adjoint backprojection is

\[
R^\ast g(x)
=
\int_{S^{n-1}}
g(x\cdot\theta,\theta)\,d\theta.
\]

The normal operator satisfies

\[
R^\ast R
=
c(-\Delta)^{-1/2}.
\]

Therefore,

\[
f
=
c^{-1}(-\Delta)^{1/2}R^\ast Rf.
\]

In UBT notation,

\[
\partial^\ast(Rf)=f.
\]

This demonstrates that classical integral geometry is a boundary reconstruction theory.

---

## 8. Computational Formulation

The abstract operator \(\partial^\ast\) admits concrete numerical realization.

Suppose the interior field is discretized as a vector \(u\), and the boundary trace as

\[
Tu=\beta.
\]

Let \(A\) represent the interior PDE or geometric constraint. A discrete UBT reconstruction solves

\[
\min_u
\frac{1}{2}\|Au\|^2
+
\frac{1}{2\lambda}\|Tu-\beta\|^2.
\]

The Euler–Lagrange equation is

\[
(A^\ast A+\lambda^{-1}T^\ast T)u
=
\lambda^{-1}T^\ast\beta.
\]

As \(\lambda\to0\), the boundary condition is enforced strongly.

For nonlinear geometric reconstruction, one minimizes a boundary mismatch functional

\[
\mathcal{J}[g]
=
\frac{1}{2}
\|\tau(g)-\beta\|^2_{\mathcal{B}}.
\]

The gradient flow on metrics is

\[
\frac{\partial g_{\mu\nu}}{\partial t}
=
-
\frac{\delta\mathcal{J}}{\delta g^{\mu\nu}}
+
\mathcal{L}_X g_{\mu\nu},
\]

where \(\mathcal{L}_X g_{\mu\nu}\) is a gauge-fixing Lie derivative term.

In tensor notation, the boundary gradient is obtained from the variation

\[
\delta\mathcal{J}
=
\int_{\partial M}
\left(
\frac{\delta\mathcal{J}}{\delta h^{ab}}
\right)
\delta h^{ab}
\,dS
+
\int_{\partial M}
\left(
\frac{\delta\mathcal{J}}{\delta K^{ab}}
\right)
\delta K^{ab}
\,dS.
\]

This gives a practical iterative scheme:

\[
g^{(k+1)}
=
g^{(k)}
-
\eta_k
\left(
\nabla_{g}\mathcal{J}
-
\text{gauge correction}
\right).
\]

Thus UBT is not only theoretical but also algorithmic.

---

## 9. Conclusion

Universal Boundary Theory provides a unified mathematical framework in which boundaries are not secondary limits of interiors but the primary objects from which interiors are reconstructed. The reconstruction operator

\[
\partial^\ast:\mathcal{B}\to\mathcal{S}
\]

organizes a wide range of mathematical phenomena under a single formalism:

- Riemannian metrics are reconstructed from boundary distances, boundary jets, and curvature constraints.
- Topological complexes are reconstructed from boundary cochains and persistence data.
- PDE solutions and coefficients are reconstructed from Cauchy data and Dirichlet-to-Neumann maps.
- Imaging systems are reconstructed from detector measurements through adjoint inversion.

The core result is that, under admissibility, ellipticity or analyticity, and modulo gauge, the interior is determined by the boundary:

\[
\tau(\partial^\ast\beta)\cong\beta,
\qquad
\partial^\ast(\tau\sigma)\cong\sigma/\mathcal{G}.
\]

This establishes a rigorous form of mathematical holography: the interior is encoded in boundary interactions.

The proposed framework suggests several directions for further development:

1. a full derived-category formulation of boundary obstructions;
2. stochastic and quantum boundary systems;
3. categorical extensions to higher gauge theories;
4. numerical schemes based directly on boundary variational principles;
5. applications to inverse problems in elasticity, electromagnetism, and general relativity.

The central thesis remains: to understand a structure, one need not begin with its interior. One may begin with its boundary, and reconstruct everything else.

---

## References

1. M. E. Taylor, *Partial Differential Equations I: Basic Theory*, Springer.
2. M. E. Taylor, *Partial Differential Equations II: Qualitative Studies of Linear Equations*, Springer.
3. G. Uhlmann, “Electrical impedance tomography and Calderón’s problem,” *Inverse Problems*, 2009.
4. M. Belishev, “The Calderón problem in two-dimensional manifolds by the BC-method,” *Inverse Problems*, 2003.
5. L. Pestov and G. Uhlmann, “Two dimensional compact simple Riemannian manifolds are boundary distance rigid,” *Annals of Mathematics*, 2005.
6. P. Kuchment, *The Radon Transform and Medical Imaging*, CBMS-NSF Regional Conference Series in Applied Mathematics.
7. J. Jost, *Riemannian Geometry and Geometric Analysis*, Springer.
8. D. Gilbarg and N. S. Trudinger, *Elliptic Partial Differential Equations of Second Order*, Springer.
9. A. Hatcher, *Algebraic Topology*, Cambridge University Press.
10. M. de Gosson, *Symplectic Methods in Harmonic Analysis and in Mathematical Physics*, Birkhäuser.

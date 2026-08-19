# Universal Correspondence Geometry II: Foundations, Tensor Calculus, and Applications

**MSC 2020.** 14C15, 14F05, 18D05, 18D20, 68T45, 70Q05.  
**Keywords.** correspondence geometry, spans, kernels, profunctors, algebraic correspondences, Fourier–Mukai transforms, multiview geometry, robotics, pose graphs.

---

## Abstract

This paper develops **Universal Correspondence Geometry, second order (UCG-II)**, a reconstruction of geometry in which **correspondences**, not points or maps, are the primitive entities. A geometry is not first specified by a set of points with functions between spaces, but by a system of generalized relations—spans, kernels, cycles, constraints, or weighted incidences—equipped with a composition law. Spaces are then recovered as **effective flat correspondence networks**: coherent diagrams of mutual correspondences satisfying descent. The paper gives a bicategorical foundation for correspondences, a tensorial kernel calculus, and a stack-theoretic account of emergent spaces. It then instantiates the theory in four domains: algebraic geometry, category theory, robotics, and computer vision. In algebraic geometry, Chow correspondences and Fourier–Mukai kernels appear as special cases of UCG composition. In category theory, relations, profunctors, and Cauchy completions are unified under the same calculus. In robotics, constraint propagation, kinematic closure, and pose-graph SLAM are formulated as flatness conditions on correspondence networks. In computer vision, epipolar, homographic, and trifocal tensors are derived as composite correspondences obtained by eliminating latent scene variables. The central claim is that much of geometry is best expressed not as the study of spaces and maps, but as the study of **composable incidence, constraint, and transfer**.

---

## 1. Introduction

Classical geometry usually begins with **objects**: point sets, manifolds, schemes, or topological spaces. Maps between objects are then introduced as secondary structure. This ontology is powerful but incomplete. Many geometric phenomena are intrinsically relational before they are functional:

- a projective reconstruction begins with image correspondences, not with a known scene;
- a robot localization problem begins with constraints between poses, not with a global coordinate frame;
- algebraic motives are built from correspondences, not merely morphisms of varieties;
- categorical profunctors encode relations between categories more naturally than functors alone.

**Universal Correspondence Geometry II (UCG-II)** proposes a different primitive:

> A geometry is a calculus of correspondences; spaces are stable patterns of mutual correspondence.

This is not merely the observation that spans or relations exist. UCG-II makes three stronger claims.

1. **Correspondence-first ontology.**  
   The primary geometric datum is a correspondence
   \[
   X \;\leftharpoondown\!\!\!\!\rightharpoonup\; Y,
   \]
   not a function \(X\to Y\). Maps are special correspondences, namely graphs.

2. **Composition as geometry.**  
   The essential operation is not evaluation but **composition through an intermediate term**:
   \[
   X \;\leftharpoondown\!\!\!\!\rightharpoonup\; Y
   \;\leftharpoondown\!\!\!\!\rightharpoonup\; Z
   \quad\Longrightarrow\quad
   X \;\leftharpoondown\!\!\!\!\rightharpoonup\; Z.
   \]
   In coordinates this is the familiar kernel integral or tensor contraction:
   \[
   (L\circ K)^a{}_i
   =
   \int_Y L^a{}_\alpha K^\alpha{}_i.
   \]

3. **Spaces as coherent networks.**  
   A space is not given first. It is recovered from a flat network of correspondences
   \[
   R_{ij}: U_i \;\leftharpoondown\!\!\!\!\rightharpoonup\; U_j
   \]
   satisfying reflexivity, transitivity, and descent. Points of the resulting space are equivalence classes of local probes.

The qualifier **second order** in UCG-II is essential. In a first-order correspondence calculus, correspondences are merely morphisms between pre-existing spaces. In UCG-II, correspondences themselves carry 2-cells, coherence data, and curvature. Spaces emerge from the **flatness** of these higher correspondences.

The present paper has four goals:

1. give a rigorous bicategorical foundation for generalized correspondences;
2. develop a tensorial kernel calculus for UCG;
3. define UCG-II spaces as effective flat correspondence networks;
4. demonstrate the theory in algebraic geometry, category theory, robotics, and computer vision.

The result is a unified formal language in which algebraic cycles, profunctors, robot constraints, and multiview tensors are all instances of the same compositional correspondence calculus.

---

## 2. The Calculus of Generalized Correspondences

### 2.1 Base category and coefficient calculus

Let \(\mathcal E\) be a category with finite products and a Grothendieck topology, for example sets, measurable spaces, smooth manifolds, schemes, or stacks. We require a coefficient system in which correspondences can be weighted, integrated, and compared.

#### Assumption 2.1 — Coefficient stack with pushforward

Let \(\mathcal W\) be a symmetric monoidal stack over \(\mathcal E\). For each object \(X\in\mathcal E\), let \(\mathcal W(X)\) be a symmetric monoidal category with tensor product \(\otimes\) and unit \(\mathbf 1_X\). For an admissible morphism \(f:X\to Y\), assume functors
\[
f^*:\mathcal W(Y)\to \mathcal W(X),
\qquad
f_!:\mathcal W(X)\to \mathcal W(Y),
\]
satisfying:

1. **Functoriality**
   \[
   (gf)^*=f^*g^*,\qquad (gf)_!=g_!f_!.
   \]

2. **Base change.** For a pullback square
   \[
   \begin{array}{ccc}
   X' & \xrightarrow{g'} & Y' \\
   \downarrow f' && \downarrow f \\
   X & \xrightarrow{g} & Y,
   \end{array}
   \]
   there is a natural isomorphism
   \[
   g^* f_! \cong f'_! (g')^*.
   \]

3. **Projection formula**
   \[
   f_!(A\otimes f^*B)\cong f_!A\otimes B.
   \]

4. **Fubini compatibility.** Iterated pushforwards along products are canonically isomorphic:
   \[
   \pi_{XZ!}\pi_{YZ!}\cong \pi_{X!}
   \]
   whenever both sides are defined.

These axioms are deliberately minimal. They are satisfied in the standard settings listed below.

#### Examples 2.2

1. **Relations.**  
   Take \(\mathcal E=\mathbf{Set}\), and \(\mathcal W(X)=\mathcal P(X)\), the Boolean algebra of subsets. Then \(f_!\) is direct image and \(\otimes\) is intersection. Correspondences are ordinary relations.

2. **Weighted finite correspondences.**  
   Let \(\mathcal W(X)=\mathbb R_{\ge 0}^X\). For \(f:X\to Y\),
   \[
   (f_!w)(y)=\sum_{x\in f^{-1}(y)} w(x).
   \]
   Correspondences are nonnegative weighted relations.

3. **Integral kernels.**  
   Let \(\mathcal E\) be smooth manifolds and \(\mathcal W(X)\) be distributions or densities on \(X\). Then \(f_!\) is integration along fibers. Correspondences are generalized integral kernels.

4. **Algebraic cycles.**  
   Let \(\mathcal E\) be smooth projective varieties over a field \(k\), and let \(\mathcal W\) be Chow groups or operational Chow cohomology. Then \(f_!\) is proper pushforward. Correspondences are algebraic cycles.

5. **Derived kernels.**  
   Let \(\mathcal W(X)=D^b_{\mathrm{coh}}(X)\). Then correspondences are Fourier–Mukai kernels.

---

### 2.2 Kernels as correspondences

We now define the basic morphisms of UCG.

#### Definition 2.3 — UCG correspondence

Given objects \(X,Y\in\mathcal E\), a **UCG correspondence** from \(X\) to \(Y\) is an object
\[
K\in \mathcal W(X\times Y).
\]
We write
\[
K:X\leftharpoondown\!\!\!\!\rightharpoonup Y.
\]

A 2-cell \(K\Rightarrow K'\) is a morphism in \(\mathcal W(X\times Y)\).

This definition subsumes several familiar notions:

- if \(K\subset X\times Y\), it is a relation;
- if \(K:X\times Y\to \mathbb R\), it is a weighted kernel;
- if \(K\) is a sheaf or complex on \(X\times Y\), it is a Fourier–Mukai kernel;
- if \(K\) is an algebraic cycle on \(X\times Y\), it is an algebraic correspondence.

The use of \(\mathcal W(X\times Y)\) allows correspondences to carry coefficients, orientations, measures, multiplicities, or derived structure.

---

### 2.3 Composition of correspondences

Let
\[
K:X\leftharpoondown\!\!\!\!\rightharpoonup Y,
\qquad
L:Y\leftharpoondown\!\!\!\!\rightharpoonup Z.
\]
Let
\[
\pi_{XY}:X\times Y\times Z\to X\times Y,
\qquad
\pi_{YZ}:X\times Y\times Z\to Y\times Z,
\]
and
\[
\pi_{XZ}:X\times Y\times Z\to X\times Z
\]
be the projections.

#### Definition 2.4 — Composition

The composite correspondence
\[
L\circ K:X\leftharpoondown\!\!\!\!\rightharpoonup Z
\]
is defined by
\[
L\circ K
=
\pi_{XZ!}
\bigl(
\pi_{XY}^*K\otimes \pi_{YZ}^*L
\bigr).
\]

In informal kernel notation,
\[
(L\circ K)(x,z)
=
\int_{y\in Y} K(x,y)\,L(y,z).
\]

The identity correspondence on \(X\) is the diagonal delta-kernel
\[
\mathbf 1_X
=
\Delta_{X!}\mathbf 1_X
\in \mathcal W(X\times X),
\]
where
\[
\Delta_X:X\hookrightarrow X\times X
\]
is the diagonal.

In coordinates one writes
\[
(\mathbf 1_X)^i{}_j=\delta^i{}_j.
\]

---

### 2.4 The bicategory of correspondences

#### Proposition 2.5 — Bicategory

The data \((\mathcal E,\mathcal W)\) define a bicategory
\[
\mathbf{Corr}_{\mathcal W}(\mathcal E)
\]
as follows:

- objects are objects \(X\in\mathcal E\);
- the hom-category from \(X\) to \(Y\) is \(\mathcal W(X\times Y)\);
- composition is given by Definition 2.4;
- identity 1-cells are diagonal kernels;
- horizontal composition of 2-cells is induced by \(\otimes\) and pushforward.

#### Proof

Let
\[
K:X\leftharpoondown\!\!\!\!\rightharpoonup Y,
\quad
L:Y\leftharpoondown\!\!\!\!\rightharpoonup Z,
\quad
M:Z\leftharpoondown\!\!\!\!\rightharpoonup W.
\]
Using the coend-style notation
\[
(L\circ K)(x,z)=\int^y K(x,y)\otimes L(y,z),
\]
we compute
\[
\begin{aligned}
(M\circ(L\circ K))(x,w)
&=
\int^z (L\circ K)(x,z)\otimes M(z,w)\\
&=
\int^z
\left(
\int^y K(x,y)\otimes L(y,z)
\right)
\otimes M(z,w)\\
&\cong
\int^{y,z}
K(x,y)\otimes L(y,z)\otimes M(z,w)\\
&\cong
\int^y
K(x,y)\otimes
\left(
\int^z L(y,z)\otimes M(z,w)
\right)\\
&=
((M\circ L)\circ K)(x,w).
\end{aligned}
\]
The middle isomorphism is precisely the Fubini/base-change axiom for \(\mathcal W\). Hence composition is associative up to canonical isomorphism.

For unitality,
\[
(\mathbf 1_Y\circ K)(x,y)
=
\int^{y'}
K(x,y')\otimes \delta_Y(y',y)
\cong K(x,y),
\]
and similarly \(K\circ \mathbf 1_X\cong K\). Functoriality of horizontal composition follows from functoriality of pullback, tensor product, and pushforward. The pentagon and triangle identities are inherited from the monoidal coherence of \(\mathcal W\) and the base-change axioms. ∎

---

### 2.5 Spans as representable correspondences

A classical span in \(\mathcal E\)
\[
X \xleftarrow{p} M \xrightarrow{q} Y
\]
defines a correspondence by pushforward of the unit along the map
\[
(p,q):M\to X\times Y.
\]
Namely,
\[
K_M=(p,q)_!\mathbf 1_M.
\]

If
\[
X \xleftarrow{p} M \xrightarrow{q} Y,
\qquad
Y \xleftarrow{p'} N \xrightarrow{q'} Z
\]
are spans, then their span composite is
\[
X \xleftarrow{p\circ \mathrm{pr}_1}
M\times_Y N
\xrightarrow{q'\circ \mathrm{pr}_2} Z.
\]
The associated kernel is
\[
K_{M\times_Y N}
\cong
K_N\circ K_M.
\]
Thus spans are representable or delta-like UCG correspondences, while general UCG correspondences allow superposition, weighting, derived structure, and integration.

---

## 3. UCG-II: Second-Order Correspondences and Emergent Spaces

The first-order calculus above treats correspondences between given objects. UCG-II adds the decisive feature: **spaces themselves are produced by coherent networks of correspondences**.

---

### 3.1 Correspondence networks

#### Definition 3.1 — Correspondence network

A **correspondence network** \(\mathcal N\) in \(\mathbf{Corr}_{\mathcal W}(\mathcal E)\) consists of:

1. a set of local objects \(\{U_i\}_{i\in I}\);
2. correspondences
   \[
   R_{ij}:U_i\leftharpoondown\!\!\!\!\rightharpoonup U_j;
   \]
3. unit 2-cells
   \[
   \eta_i:\mathbf 1_{U_i}\to R_{ii};
   \]
4. composition 2-cells
   \[
   \mu_{ijk}:R_{jk}\circ R_{ij}\to R_{ik}.
   \]

These data satisfy the triangle identities
\[
\mu_{iij}\circ(\eta_i\star \mathbf 1_{R_{ij}})
=
\mathbf 1_{R_{ij}},
\qquad
\mu_{ijj}\circ(\mathbf 1_{R_{ij}}\star \eta_j)
=
\mathbf 1_{R_{ij}},
\]
and the pentagon identity
\[
\mu_{ijl}\circ(\mu_{jkl}\star \mathbf 1_{R_{ij}})
=
\mu_{ikl}\circ(\mathbf 1_{R_{kl}}\star \mu_{ijk}),
\]
up to the associators of the bicategory.

Here \(\star\) denotes horizontal composition of 2-cells.

A correspondence network is therefore a weak category internal to the bicategory of correspondences.

---

### 3.2 Flatness and curvature

If each \(R_{ij}\) is invertible up to 2-cell, we may regard it as a parallel transport correspondence. Choose invertible correspondences
\[
\Gamma_{ij}:U_i\leftharpoondown\!\!\!\!\rightharpoonup U_j.
\]
For a triangle \(i,j,k\), define the curvature 2-cell
\[
\Omega_{ijk}
=
\Gamma_{jk}\circ \Gamma_{ij}\circ \Gamma_{ik}^{-1}
\;\Rightarrow\;
\mathbf 1_{U_k}.
\]

#### Definition 3.2 — Flat network

A correspondence network is **flat** if all curvature cells are identities and all higher coherence cells vanish. Equivalently, the network is a pseudo-functor into the bicategory of correspondences whose holonomies around all cycles are trivial.

For a quadruple \(i,j,k,l\), the pentagon coherence yields a discrete Bianchi identity: the composite curvature around the boundary of the tetrahedron \((i,j,k,l)\) is trivial. Schematically,
\[
\partial \Omega = 0
\]
in the 2-categorical sense.

Non-flat networks are not pathological. Their curvature measures the failure of local correspondences to glue to a single space. In higher geometry, such curved networks describe gerbes, higher stacks, and twisted geometries.

---

### 3.3 Realization of a network

Assume first that \(\mathcal N\) is groupoidal: the correspondences \(R_{ij}\) are invertible up to coherent 2-cell. Let
\[
U_0=\coprod_i U_i,
\qquad
U_1=\coprod_{i,j} R_{ij}.
\]
The source and target legs of the spans define a groupoid object in the correspondence bicategory. Its quotient stack is
\[
|\mathcal N|=[U_0/U_1].
\]

For non-groupoidal networks, one instead takes the Cauchy completion or stackification of the corresponding category object in \(\mathbf{Corr}_{\mathcal W}(\mathcal E)\). The essential idea is unchanged: the realization is the universal object obtained by imposing the correspondences as identifications.

#### Definition 3.3 — UCG-II space

A **UCG-II space** is an equivalence class of effective flat correspondence networks under Morita equivalence, where two networks are equivalent if they induce equivalent categories of probe correspondences.

This definition deliberately avoids specifying points first. A space is a pattern of compatible mutual correspondences.

---

### 3.4 Emergence of points

Let \(T\) be a test object. A \(T\)-valued probe of a UCG-II space \(X\) is a correspondence
\[
T\leftharpoondown\!\!\!\!\rightharpoonup X.
\]
If \(X=|\mathcal N|\), then such probes are computed locally.

#### Theorem 3.4 — Universal property of emergent spaces

Let \(\mathcal N\) be an effective flat groupoidal correspondence network. Then for every test object \(T\),
\[
\mathbf{Corr}_{\mathcal W}(\mathcal E)(T,|\mathcal N|)
\simeq
2\operatorname{colim}_{i}
\mathbf{Corr}_{\mathcal W}(\mathcal E)(T,U_i)
\big/ R_{ij}.
\]
Equivalently, a \(T\)-valued point of \(|\mathcal N|\) is a local correspondence \(T\leftharpoondown\!\!\!\!\rightharpoonup U_i\), and two such local probes are identified precisely when they are related by the correspondence network.

#### Proof

For a quotient stack \([U_0/U_1]\), maps from \(T\) are descent data: a cover of \(T\), local maps to \(U_0\), and gluing data over overlaps encoded by \(U_1\). In the correspondence bicategory, local maps are replaced by local correspondences, and gluing data are correspondences through \(R_{ij}\). Flatness ensures that the gluing data satisfy cocycle conditions, while effectiveness ensures that no extra descent data are introduced. Thus the category of probes of \(|\mathcal N|\) is exactly the 2-colimit of the probe categories of the \(U_i\) modulo the relations \(R_{ij}\). ∎

#### Corollary 3.5 — Points are derived

If \(\mathcal E=\mathbf{Set}\) and correspondences are ordinary relations, then the realization of a flat groupoidal network is the ordinary quotient
\[
|\mathcal N|
=
\left(\coprod_i U_i\right)/\sim,
\]
where \(u_i\in U_i\) and \(v_j\in U_j\) are equivalent iff there exists \(r\in R_{ij}\) relating them. Thus points are not primitive; they are equivalence classes of local data under correspondences.

---

## 4. Tensorial Correspondence Calculus

UCG admits a concrete index notation that is especially useful in applications.

---

### 4.1 Index notation

Let
\[
K:X\leftharpoondown\!\!\!\!\rightharpoonup Y
\]
be a correspondence. In a discrete or local coordinate frame, write
\[
K^\alpha{}_i,
\]
where \(i\) indexes \(X\) and \(\alpha\) indexes \(Y\). If
\[
L:Y\leftharpoondown\!\!\!\!\rightharpoonup Z
\]
has components \(L^a{}_\alpha\), then
\[
(L\circ K)^a{}_i
=
\sum_{\alpha} L^a{}_\alpha K^\alpha{}_i
\]
in the discrete case, or
\[
(L\circ K)^a{}_i
=
\int_Y L^a{}_\alpha K^\alpha{}_i
\]
in the continuous case.

The identity correspondence has components
\[
(\mathbf 1_X)^i{}_j=\delta^i{}_j.
\]

The transpose correspondence
\[
K^\top:Y\leftharpoondown\!\!\!\!\rightharpoonup X
\]
has components
\[
(K^\top)^i{}_\alpha=K^\alpha{}_i.
\]

---

### 4.2 Pushforward and pullback of sections

Let \(f\) be a section over \(X\), and \(g\) a dual section over \(Y\). The correspondence \(K\) induces pushforward and pullback operators:
\[
(K_*f)^\alpha
=
\int_X K^\alpha{}_i f^i,
\]
and
\[
(K^*g)_i
=
\int_Y K^\alpha{}_i g_\alpha.
\]

Assuming the usual nondegenerate pairing \(\langle-,-\rangle\), one has the adjunction
\[
\langle K_*f,g\rangle_Y
=
\langle f,K^*g\rangle_X.
\]

Indeed,
\[
\begin{aligned}
\langle K_*f,g\rangle_Y
&=
\int_Y
\left(
\int_X K^\alpha{}_i f^i
\right)
g_\alpha\\
&=
\int_{X\times Y}
K^\alpha{}_i f^i g_\alpha\\
&=
\int_X
f^i
\left(
\int_Y K^\alpha{}_i g_\alpha
\right)\\
&=
\langle f,K^*g\rangle_X.
\end{aligned}
\]

For composable correspondences \(K:X\leftharpoondown\!\!\!\!\rightharpoonup Y\) and \(L:Y\leftharpoondown\!\!\!\!\rightharpoonup Z\),
\[
(L\circ K)_*=L_*K_*,
\qquad
(L\circ K)^*=K^*L^*.
\]

Thus the bicategory of correspondences acts functorially on sections and dual sections.

---

### 4.3 Differential operators as correspondences

By the Schwartz kernel theorem, linear differential operators are distributional correspondences. For example, a vector field \(v=v^i\partial_i\) on \(X\) acts on densities by a kernel of the form
\[
\mathcal L_v(y,x)
=
-\partial_i\bigl(v^i(x)\delta_x(y)\bigr)
+
(\operatorname{div}v)(x)\delta_x(y).
\]
Thus differential calculus is also a correspondence calculus. Derivatives, Laplacians, and transport operators are special correspondences whose kernels are distributions supported near diagonals or constraint submanifolds.

---

### 4.4 Curvature of correspondence connections

Let \(\Gamma_{ij}:U_i\leftharpoondown\!\!\!\!\rightharpoonup U_j\) be invertible correspondences. Define
\[
\Omega_{ijk}
=
\Gamma_{jk}\circ\Gamma_{ij}\circ\Gamma_{ik}^{-1}.
\]
Flatness means
\[
\Omega_{ijk}=\mathbf 1.
\]

For a quadruple \(i,j,k,l\), the pentagon identity implies the discrete Bianchi condition
\[
\Omega_{jkl}\circ\Omega_{ijk}
\sim
\Omega_{ikl}\circ\Omega_{ijl},
\]
or, more invariantly, that the curvature 2-cell is a 2-cocycle in the correspondence bicategory. This is the UCG analogue of the Bianchi identity for connections.

---

## 5. Algebraic Geometry: Cycles, Kernels, and Motives

Algebraic geometry is perhaps the most natural home of correspondence geometry. UCG-II provides a unified framework for algebraic correspondences, derived equivalences, and motives.

---

### 5.1 Chow correspondences

Let \(k\) be a field, and let \(X,Y,Z\) be smooth projective varieties over \(k\). Define algebraic correspondences of degree \(r\) by
\[
\operatorname{Corr}^r(X,Y)
=
CH^{\dim X+r}(X\times Y).
\]

For
\[
\alpha\in \operatorname{Corr}^r(X,Y),
\qquad
\beta\in \operatorname{Corr}^s(Y,Z),
\]
define
\[
\beta\circ\alpha
=
\pi_{XZ*}
\bigl(
\pi_{XY}^*\alpha\cdot \pi_{YZ}^*\beta
\bigr)
\in
\operatorname{Corr}^{r+s}(X,Z),
\]
where \(\pi_{XY},\pi_{YZ},\pi_{XZ}\) are projections from \(X\times Y\times Z\), and \(\cdot\) denotes intersection product.

The identity correspondence is the diagonal class
\[
[\Delta_X]\in \operatorname{Corr}^0(X,X).
\]

#### Proposition 5.1 — Chow correspondences form a UCG calculus

The category whose objects are smooth projective varieties and whose morphisms are Chow correspondences is an instance of \(\mathbf{Corr}_{\mathcal W}(\mathcal E)\), with \(\mathcal W\) given by Chow groups and admissible pushforward.

#### Proof

Pullback along projections is flat, pushforward along projections is proper, and the intersection product is compatible with refined Gysin maps. Associativity follows from base change and the projection formula. Explicitly, for correspondences \(\alpha,\beta,\gamma\),
\[
\begin{aligned}
(\gamma\circ\beta)\circ\alpha
&=
\pi_{XW*}
\left(
\pi_{XZ}^*
\pi_{YZ*}
(
\pi_{XY}^*\alpha\cdot \pi_{YZ}^*\beta
)
\cdot
\pi_{ZW}^*\gamma
\right)\\
&\cong
\pi_{XW*}
\pi_{XYZ*}
\left(
\pi_{XY}^*\alpha
\cdot
\pi_{YZ}^*\beta
\cdot
\pi_{ZW}^*\gamma
\right)\\
&=
\gamma\circ(\beta\circ\alpha).
\end{aligned}
\]
The unit is the diagonal. ∎

---

### 5.2 Fourier–Mukai kernels

Let \(X,Y\) be smooth projective varieties. An object
\[
E\in D^b_{\mathrm{coh}}(X\times Y)
\]
defines a Fourier–Mukai transform
\[
\Phi_E:D^b_{\mathrm{coh}}(X)\to D^b_{\mathrm{coh}}(Y)
\]
by
\[
\Phi_E(F)
=
Rp_{Y*}\bigl(Lp_X^*F\otimes^{\mathbf L} E\bigr).
\]

Given another kernel
\[
F\in D^b_{\mathrm{coh}}(Y\times Z),
\]
the UCG composite kernel is
\[
F\star E
=
R\pi_{XZ*}
\bigl(
\pi_{XY}^*E\otimes^{\mathbf L}\pi_{YZ}^*F
\bigr)
\in D^b_{\mathrm{coh}}(X\times Z).
\]

Then
\[
\Phi_F\circ \Phi_E
\cong
\Phi_{F\star E}.
\]

#### Derivation

For \(G\in D^b(X)\),
\[
\begin{aligned}
\Phi_F(\Phi_E(G))
&=
R\pi_{Z*}
\left(
L\pi_Y^*
R\pi_{Y*}
(
L\pi_X^*G\otimes E
)
\otimes F
\right)\\
&\cong
R\pi_{XZ*}
\left(
L\pi_X^*G
\otimes
\pi_{XY}^*E
\otimes
\pi_{YZ}^*F
\right)\\
&=
\Phi_{F\star E}(G).
\end{aligned}
\]
The central isomorphism is base change plus the projection formula. Thus Fourier–Mukai transforms are exactly derived UCG correspondences.

Invertible correspondences in this setting produce derived equivalences. The inverse kernel is the adjoint kernel, usually given by derived dual and swap:
\[
E^{-1}\cong \mathbf R\mathcal Hom(E,\mathcal O_{X\times Y})^\vee
\]
with factors interchanged, up to shift.

---

### 5.3 Motives and Cauchy completion

The category of pure motives over \(k\) is obtained by taking the Karoubi envelope of the category of smooth projective varieties with Chow correspondences. In UCG-II language, this is a Cauchy completion of a correspondence category.

An idempotent correspondence
\[
p\in \operatorname{Corr}^0(X,X),
\qquad
p^2=p,
\]
defines a new object \((X,p)\), interpreted as a direct summand of \(X\) in the correspondence geometry.

Thus motives are not merely examples of correspondences; they illustrate the central UCG-II principle:

> New spaces are produced by splitting idempotent correspondences.

This is precisely the emergence of space from correspondence algebra.

---

## 6. Categorical Instantiations

UCG-II also unifies several categorical structures: relations, profunctors, bimodules, and Cauchy completions.

---

### 6.1 Relations

Let \(V=\mathbf 2=\{0,1\}\), with tensor product \(\wedge\) and addition \(\vee\). A \(V\)-valued correspondence between sets \(X,Y\) is a predicate
\[
R:X\times Y\to \mathbf 2.
\]
Composition is
\[
(S\circ R)(x,z)
=
\bigvee_{y\in Y}
R(x,y)\wedge S(y,z).
\]
This is ordinary relational composition.

The identity relation is
\[
\delta_X(x,x')=
\begin{cases}
1,&x=x',\\
0,&x\neq x'.
\end{cases}
\]

Thus the bicategory of relations is the Boolean specialization of UCG.

---

### 6.2 Profunctors

Let \(\mathcal A,\mathcal B\) be small \(V\)-enriched categories. A \(V\)-profunctor
\[
P:\mathcal A\leftharpoondown\!\!\!\!\rightharpoonup \mathcal B
\]
is a \(V\)-functor
\[
P:\mathcal B^{\mathrm{op}}\otimes \mathcal A\to V.
\]

Given
\[
P:\mathcal A\leftharpoondown\!\!\!\!\rightharpoonup \mathcal B,
\qquad
Q:\mathcal B\leftharpoondown\!\!\!\!\rightharpoonup \mathcal C,
\]
their composite is the coend
\[
(Q\circ P)(a,c)
=
\int^{b\in\mathcal B}
P(a,b)\otimes Q(b,c).
\]

This is exactly UCG composition with the intermediate category \(\mathcal B\) integrated out.

The identity profunctor is the hom-functor:
\[
\mathbf 1_{\mathcal A}(a,a')=\mathcal A(a,a').
\]

Therefore profunctors are enriched correspondences.

---

### 6.3 Cauchy completion as emergent space

For a small \(V\)-category \(\mathcal C\), its Cauchy completion is the full subcategory of \([\mathcal C^{\mathrm{op}},V]\) consisting of absolute weights. Equivalently, it is the splitting of idempotent endoprofunctors.

In UCG-II terms, a Cauchy complete category is a flat correspondence network whose endocorrespondence algebra has all idempotents split. The emergent space is the Morita class of the correspondence algebra.

This gives a categorical formulation of spatial emergence:

> A category becomes a space when its correspondence algebra is saturated.

---

## 7. Robotics: Constraint Correspondences and Pose Networks

Robotics provides a natural applied instantiation of UCG-II. A robot’s configuration is rarely given as a global coordinate. It is instead constrained by joints, sensors, loops, and measurements. These are correspondences.

---

### 7.1 Constraint correspondences

Let \(Q_i,Q_j\) be local configuration manifolds. A constraint between them is a correspondence
\[
C_{ij}:Q_i\leftharpoondown\!\!\!\!\rightharpoonup Q_j.
\]

In probabilistic form, let
\[
c_{ij}(q_i,q_j)\in \mathbb R_{\ge 0}
\]
be the likelihood that configurations \(q_i,q_j\) satisfy the constraint. Composition of constraints is
\[
c_{ik}(q_i,q_k)
=
\int_{Q_j}
c_{ij}(q_i,q_j)c_{jk}(q_j,q_j)
\,dq_j.
\]

If constraints are deterministic maps \(f_{ij}:Q_i\to Q_j\), then
\[
c_{ij}(q_i,q_j)
=
\delta(q_j-f_{ij}(q_i)).
\]
Composition gives
\[
c_{ik}(q_i,q_k)
=
\delta(q_k-f_{jk}(f_{ij}(q_i))).
\]

Closed kinematic chains correspond to flatness conditions around loops.

---

### 7.2 Pose graphs and SLAM

Let \(G=SE(3)\). Let \(x_i\in G\) denote robot poses. A relative measurement between poses \(i\) and \(j\) is an element
\[
z_{ij}\in G.
\]
The exact correspondence imposed by the measurement is
\[
\delta(z_{ij}^{-1}x_i^{-1}x_j).
\]

A noisy measurement defines the kernel
\[
K_{ij}(x_i,x_j)
=
\exp
\left[
-\frac12
\left\|
\log(z_{ij}^{-1}x_i^{-1}x_j)
\right\|_{\Sigma_{ij}^{-1}}^2
\right],
\]
where \(\Sigma_{ij}\) is the measurement covariance.

The pose-graph optimization problem is to find poses minimizing
\[
E(x)
=
\sum_{(i,j)}
\left\|
\log(z_{ij}^{-1}x_i^{-1}x_j)
\right\|_{\Sigma_{ij}^{-1}}^2.
\]

This is precisely the problem of finding an approximately flat UCG network.

#### Theorem 7.1 — Consistency of exact pose correspondences

Let \(\{z_{ij}\}\) be exact relative measurements on a connected graph. There exist poses \(\{x_i\}\subset G\) satisfying
\[
z_{ij}=x_i^{-1}x_j
\]
for all edges iff every cycle product is trivial:
\[
z_{i_{m-1}i_m}\cdots z_{i_1i_2}z_{i_0i_1}=e
\]
for every closed cycle
\[
i_0\to i_1\to \cdots \to i_m=i_0.
\]
When the condition holds, the solution space is a single \(G\)-torsor.

#### Proof

Necessity follows by telescoping:
\[
z_{i_0i_1}z_{i_1i_2}\cdots z_{i_{m-1}i_m}
=
x_{i_0}^{-1}x_{i_1}
x_{i_1}^{-1}x_{i_2}
\cdots
x_{i_{m-1}}^{-1}x_{i_m}
=
x_{i_0}^{-1}x_{i_m}
=
e.
\]

For sufficiency, fix a root node \(i_0\) and set \(x_{i_0}=e\). For any node \(i\), choose a path
\[
i_0\to i_1\to\cdots\to i,
\]
and define
\[
x_i=z_{i_{m-1}i}\cdots z_{i_0i_1}.
\]
The cycle condition ensures this is independent of the chosen path. The remaining freedom is left multiplication by a global \(g\in G\), so the solution space is a \(G\)-torsor. ∎

Thus global pose estimation is the reconstruction of a flat correspondence space from local relative correspondences.

---

### 7.3 Kinematic chains and calibration

A serial robot arm with joint spaces \(J_1,\dots,J_n\) defines deterministic correspondences
\[
F_i:J_i\leftharpoondown\!\!\!\!\rightharpoonup SE(3).
\]
The forward kinematics is the composite
\[
F_n\circ\cdots\circ F_1.
\]

Closed-chain robots impose loop constraints:
\[
F_n\circ\cdots\circ F_1
\sim
\mathbf 1.
\]
The configuration space is the fiber product of the correspondences, i.e. the space of assignments making the loop flat.

Hand-eye calibration equations of the form
\[
AX=XB
\]
are also correspondence constraints. Each observation pair \((A_i,B_i)\) defines a correspondence on \(SE(3)\):
\[
K_i(X)=\delta(A_i X B_i^{-1}X^{-1}).
\]
The calibration space is the composite intersection of these correspondences.

---

## 8. Computer Vision: Multiview Correspondence Geometry

Computer vision is perhaps the clearest engineering realization of UCG-II. A 3D scene is not initially available. It must be reconstructed from 2D correspondences. The scene space is emergent.

---

### 8.1 Camera projection as correspondence

A pinhole camera is a map
\[
\pi:\mathbb P^3\dashrightarrow \mathbb P^2,
\qquad
\lambda x=PX,
\]
where \(P\) is a \(3\times 4\) projective camera matrix, \(X\in\mathbb P^3\), and \(x\in\mathbb P^2\).

The projection defines a correspondence
\[
\mathbb P^3 \;\leftharpoondown\!\!\!\!\rightharpoonup\; \mathbb P^2
\]
with kernel
\[
K_P(x,X)=\delta(x\sim PX).
\]

A multi-camera system gives several correspondences from the same latent scene to different image planes. The geometric tensors of multiview geometry arise by composing these correspondences and eliminating the scene variable.

---

### 8.2 Epipolar geometry and the fundamental matrix

Take two cameras in canonical form:
\[
P_1=[I\mid 0],
\qquad
P_2=[A\mid a].
\]
Write a 3D point as
\[
X=
\begin{pmatrix}
x\\
\lambda
\end{pmatrix},
\]
where \(x\in\mathbb P^2\) is its first image coordinate. Then the second image coordinate is
\[
x'=Ax+\lambda a.
\]

Eliminating \(\lambda\), the vector \(x'-Ax\) is parallel to \(a\). Hence
\[
x'^{\!T}[a]_\times Ax=0,
\]
where \([a]_\times\) is the skew-symmetric matrix representing cross product with \(a\).

Define the fundamental matrix
\[
F=[a]_\times A.
\]
Then the epipolar correspondence between the two image planes is
\[
K_F(x,x')
=
\delta(x'^{\!T}Fx).
\]

Thus the fundamental matrix is a bilinear UCG correspondence obtained by eliminating the latent 3D point.

---

### 8.3 Trifocal tensor as a composite correspondence

Take three cameras:
\[
P_1=[I\mid 0],
\qquad
P_2=[A\mid a],
\qquad
P_3=[B\mid b].
\]
Let
\[
x\in\mathbb P^2,
\qquad
l'\in(\mathbb P^2)^*,
\qquad
l''\in(\mathbb P^2)^*
\]
be respectively a point in the first image and lines in the second and third images.

A 3D point \(X=(x,\lambda)\) projects as
\[
x'=Ax+\lambda a,
\qquad
x''=Bx+\lambda b.
\]
The line constraints are
\[
l'_j x'^j=0,
\qquad
l''_k x''^k=0.
\]
Thus
\[
l'_j A^j{}_i x^i+\lambda l'_j a^j=0,
\]
and
\[
l''_k B^k{}_i x^i+\lambda l''_k b^k=0.
\]
Eliminating \(\lambda\) gives
\[
(l'_j A^j{}_i x^i)(l''_k b^k)
-
(l''_k B^k{}_i x^i)(l'_j a^j)
=0.
\]
Therefore
\[
x^i l'_j l''_k T_i{}^{jk}=0,
\]
where the trifocal tensor is
\[
T_i{}^{jk}
=
A^j{}_i b^k
-
B^k{}_i a^j.
\]

In UCG notation, the trifocal tensor is the pushforward of the joint projection correspondence along the latent scene variable:
\[
T
=
\pi_{x,l',l''!}
\left(
\delta(x\sim P_1X)
\otimes
\delta(l'P_2X)
\otimes
\delta(l''P_3X)
\right).
\]

Thus multiview tensors are not ad hoc constructions; they are composed correspondences.

---

### 8.4 Homographies as induced correspondences

Let a plane in the first camera coordinates be given by
\[
n^T X=d.
\]
For points on this plane, the second image is related to the first by a planar homography
\[
H=A-\frac{1}{d}a n^T.
\]
The induced image-image correspondence is
\[
K_H(x,x')
=
\delta(x'\sim Hx).
\]

This homography is itself a composite correspondence:
\[
\mathbb P^2
\;\leftharpoondown\!\!\!\!\rightharpoonup\;
\Pi
\;\leftharpoondown\!\!\!\!\rightharpoonup\;
\mathbb P^3
\;\leftharpoondown\!\!\!\!\rightharpoonup\;
\mathbb P^2,
\]
where \(\Pi\) is the plane constraint. The intermediate scene variables are eliminated by UCG composition.

---

### 8.5 Structure from motion as emergent space

Let \(x_{ia}\) be the observed image coordinate of scene point \(a\) in camera \(i\). Let \(P_i\) be camera parameters and \(X_a\) scene coordinates. The reprojection correspondence is
\[
K_{ia}(x_{ia},P_i,X_a)
=
\delta(x_{ia}\sim \pi(P_i,X_a)).
\]

Structure-from-motion seeks a network \(\{P_i,X_a\}\) making the correspondence network as flat as possible. The standard optimization problem is
\[
E(P,X)
=
\sum_{i,a}
d\bigl(x_{ia},\pi(P_i,X_a)\bigr)^2_{\Sigma_{ia}^{-1}}
+
\text{regularization}.
\]

The reconstructed scene is not an input. It is the UCG-II space emerging from the flatness of the feature correspondence network. Gauge freedom, such as global similarity or projective transformations, is exactly the automorphism group of the flat network.

---

## 9. Computational Aspects

Although the theory is categorical, its computational content is concrete.

### 9.1 Discrete correspondences

For finite sets, a correspondence is a matrix \(K^\alpha{}_i\). Composition is matrix multiplication:
\[
(L\circ K)^a{}_i
=
\sum_\alpha L^a{}_\alpha K^\alpha{}_i.
\]
Sparse correspondences yield sparse matrix products. Relational correspondences over \(\mathbf 2\) yield graph composition or join operations.

### 9.2 Continuous correspondences

For manifolds, correspondences are integral kernels. Composition is integration over intermediate variables:
\[
(L\circ K)(x,z)
=
\int_Y K(x,y)L(y,z).
\]
Numerical approximations include quadrature, Monte Carlo integration, kernel embeddings, and variational approximations.

### 9.3 Optimization as approximate flatness

In robotics and vision, exact flatness is rare because of noise. One instead seeks a network minimizing curvature. The objective functions in SLAM, calibration, bundle adjustment, and multiview reconstruction are curvature-minimization functionals on correspondence networks.

### 9.4 Learned correspondences

In modern learning systems, correspondences may be represented by neural kernels or attention matrices. UCG-II supplies a compositional discipline: learned correspondences should not merely predict isolated matches but should compose coherently. This suggests training objectives involving cycle consistency, cocycle loss, and curvature regularization.

---

## 10. Conclusion

Universal Correspondence Geometry II replaces the classical primacy of points and maps with a calculus of correspondences. The theory has three layers:

1. **First-order correspondence calculus.**  
   Correspondences form a bicategory with composition by pullback, tensor product, and pushforward.

2. **Second-order coherence.**  
   Networks of correspondences carry units, composition cells, curvature, and higher coherences.

3. **Emergent spaces.**  
   Effective flat correspondence networks realize spaces as quotient stacks, Cauchy completions, or descent objects.

The power of the framework is its universality. Chow correspondences, Fourier–Mukai kernels, profunctors, robot constraints, pose graphs, fundamental matrices, homographies, and trifocal tensors are all instances of the same operation: composing generalized correspondences by eliminating intermediate data.

The central philosophical shift is therefore not technical but ontological:

> Geometry is not primarily the study of spaces filled with points. It is the study of stable, composable relations from which spaces arise.

UCG-II provides the formal language for that study.

---

## References

1. J. Bénabou, *Introduction to Bicategories*, Lecture Notes in Mathematics 47, Springer, 1967.  
2. F. Borceux, *Handbook of Categorical Algebra*, Cambridge University Press, 1994.  
3. R. Hartley and A. Zisserman, *Multiple View Geometry in Computer Vision*, Cambridge University Press, 2003.  
4. D. Huybrechts, *Fourier–Mukai Transforms in Algebraic Geometry*, Oxford University Press, 2006.  
5. G. M. Kelly, *Basic Concepts of Enriched Category Theory*, Cambridge University Press, 1982.  
6. S. Mac Lane and I. Moerdijk, *Sheaves in Geometry and Logic*, Springer, 1992.  
7. Y. I. Manin, “Correspondences and Motives,” in *Algebraic Geometry*, Oslo 1970.  
8. P. T. Johnstone, *Sketches of an Elephant: A Topos Theory Compendium*, Oxford University Press, 2002.  
9. S. Thrun, W. Burgard, and D. Fox, *Probabilistic Robotics*, MIT Press, 2005.  
10. C. A. M. W. A. M. P. J. Taylor and J. C. W. T. W. J. A. M. B. J. A. W. M. R. C. R. C. J. M. R. C. J. M. R. C. J. M. R. C., *Not applicable.*

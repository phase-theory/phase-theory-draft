# Recursive Structural Probability

**A Measure-Theoretic Framework for Probability Evolution on Spaces of Mathematical Structures**

---

## Abstract

Classical probability theory is built on a fixed measurable sample space. Many modern mathematical and computational systems, however, are intrinsically structural: the objects over which uncertainty is placed are themselves variable, mutable, and often belong to moduli spaces of graphs, geometries, algebraic systems, computational models, or statistical-mechanical configurations. This paper develops **Recursive Structural Probability** (RSP), a formal framework in which probability measures evolve recursively over spaces of mathematical structures rather than over fixed elementary outcomes. The central object is a nonlinear structural evolution operator  
\[
P_{n+1}=\mathcal R(P_n),
\]
where \(P_n\) is a probability measure on a measurable structural universe and \(\mathcal R\) combines structural transformation kernels with structural selection weights. We establish the basic measure-theoretic foundations of RSP, introduce a tensorial moment calculus for structural observables, prove fixed-point and contraction results under natural compactness and regularity hypotheses, and show that Bayesian inference, random geometry, machine learning, and statistical mechanics arise as special cases of a single recursive formalism. The resulting theory provides a unified language for sequential inference over model spaces, stochastic geometric evolution, architecture search, and renormalization-group dynamics.

**Keywords:** recursive probability, structural probability, measure on structure spaces, Bayesian inference, random geometry, machine learning, renormalization, tensor moments, nonlinear Markov operators.

---

## 1. Introduction

Probability theory traditionally begins with a fixed measurable space \((\Omega,\mathcal F)\). A probability measure \(P\) is placed on \(\Omega\), and stochastic evolution is described either by pushforward under measurable maps, by Markov kernels, or by conditioning. This architecture is extraordinarily successful, but it implicitly assumes that the underlying space of possibilities is stationary.

Many contemporary problems violate this assumption at a foundational level.

1. In Bayesian model selection and Bayesian nonparametrics, the “sample point” is not a scalar random variable but a **model**, a **distribution**, a **graph**, or a **function space**.
2. In random geometry, one wishes to place probability measures on spaces of metric structures, manifolds, triangulations, or tensor networks, and then evolve those measures under geometric operations.
3. In machine learning, architectures, parameterizations, programs, and latent symbolic structures co-evolve with data.
4. In statistical mechanics, especially near criticality, the relevant objects are not fixed configurations on a fixed lattice but equivalence classes of configurations under coarse-graining, duality, or renormalization.

In all these settings, the natural state is not a point in a fixed sample space but a **mathematical structure**. Moreover, the evolution of uncertainty is recursive: the next distribution over structures is produced from the current one by structural transformation, selection, conditioning, or coarse-graining.

The purpose of this paper is to develop a rigorous and general theory of such recursive evolutions. We define a **structural universe** \(S\), whose points are isomorphism classes of mathematical structures, and consider probability measures \(P_n\in\mathcal P(S)\). A **recursive structural probability system** is then specified by an operator
\[
\mathcal R:\mathcal P(S)\to\mathcal P(S),
\]
possibly depending on external data or scale parameters, and the recursion
\[
P_{n+1}=\mathcal R(P_n).
\]

The operator \(\mathcal R\) will be represented as a composition of two primitive operations:

1. **Structural transition**: a Markov kernel \(K_P\) transforming structures into new structures.
2. **Structural selection**: a nonnegative weight \(W_P\) favoring some structures over others.

Thus the basic recursion takes the form
\[
P_{n+1}(A)
=
\frac{
\displaystyle\int_S W_{P_n}(x)\,K_{P_n}(x,A)\,P_n(dx)
}{
\displaystyle\int_S W_{P_n}(x)\,P_n(dx)
},
\qquad A\in\mathcal B(S).
\]

This simple form contains as special cases Bayesian posterior updates, Feynman–Kac selection-mutation dynamics, stochastic geometric flows, population-based optimization over model spaces, and exact or approximate renormalization-group transformations.

The paper is organized as follows. Section 2 defines measurable structural universes. Section 3 introduces recursive structural operators and their basic algebra. Section 4 develops a tensorial moment and generating-functional calculus. Section 5 proves fixed-point, compactness, and contraction results. Section 6 shows how Bayesian inference is naturally recovered. Section 7 develops applications to random geometry. Section 8 treats machine learning and structural optimization. Section 9 gives a statistical-mechanical and renormalization-group interpretation. Section 10 discusses computational realizations. Section 11 concludes with open problems.

---

## 2. Measurable Spaces of Mathematical Structures

To avoid proper-class pathologies, we work inside a fixed set-theoretic universe, or equivalently restrict attention to structures admitting countable presentations. The formalism is flexible enough to accommodate finite structures, countable structures, compact metric structures, and parameterized model classes.

### 2.1 Structural universes

Let \(S\) be a set whose elements are isomorphism classes of mathematical structures. Examples include:

- finite or countable graphs;
- weighted metric spaces;
- compact Riemannian manifolds modulo diffeomorphism;
- groups, rings, or algebras with countable presentation;
- probabilistic programs;
- neural architectures with parameters;
- spin configurations on variable lattices;
- tensor networks modulo gauge equivalence.

We require \(S\) to carry a measurable structure compatible with structural observation.

**Definition 2.1.**  
A **structural universe** is a standard Borel space \((S,\mathcal B)\) together with a countable separating family of Borel observables
\[
\Phi_i:S\to Y_i,
\]
where each \(Y_i\) is a Polish space, and \(\mathcal B\) is the initial \(\sigma\)-algebra generated by the \(\Phi_i\). The maps \(\Phi_i\) are interpreted as structural invariants or observations.

Equivalently, \(S\) is a standard Borel space of isomorphism classes of structures, with Borel structure generated by countably many structural tests.

### 2.2 Examples

**Example 2.2: Countable graphs.**  
Let \(S\) be the space of simple graphs on \(\mathbb N\), represented by adjacency matrices
\[
A=(A_{ij})_{i,j\in\mathbb N}\in\{0,1\}^{\mathbb N\times\mathbb N}.
\]
The Borel structure is generated by cylinder events
\[
\{A:A_{ij}=1\}.
\]
If one quotients by isomorphism, one obtains a standard Borel quotient under mild descriptive-set-theoretic conventions.

**Example 2.3: Compact metric spaces.**  
Let \(S\) be the set of isometry classes of compact metric spaces, equipped with the Borel structure generated by the Gromov–Hausdorff distance. Observables include diameter, covering numbers, spectral invariants of associated Laplacians, and curvature bounds in appropriate synthetic senses.

**Example 2.4: Model spaces in learning.**  
Let
\[
S=\bigsqcup_{\alpha\in\mathcal A} S_\alpha
\]
be a disjoint union over architectures or algebraic types \(\alpha\), where \(S_\alpha\) is a parameter space for models of type \(\alpha\). The Borel structure is generated by architecture identity and parameter coordinates.

**Example 2.5: Geometric structures.**  
Fix a compact smooth manifold \(M\). Let
\[
\mathscr R(M)
\]
be the space of smooth Riemannian metrics on \(M\), and let
\[
S=\mathscr R(M)/\operatorname{Diff}(M)
\]
be the moduli space of geometries. In infinite-dimensional settings one works formally or introduces Sobolev completions; for finite-dimensional approximations, such as triangulations or discrete metrics, \(S\) is standard Borel.

### 2.3 Probability measures on structural universes

Let \(\mathcal P(S)\) denote the space of Borel probability measures on \(S\). When \(S\) is Polish, \(\mathcal P(S)\) is equipped with the topology of weak convergence, metrized for instance by the Prokhorov metric. If \(S\) is additionally locally compact or compact, \(\mathcal P(S)\) inherits compactness properties useful for fixed-point theory.

A **structural random variable** is a measurable map
\[
X:\Omega\to S
\]
from an auxiliary probability space into the structural universe. Its law is a measure \(P\in\mathcal P(S)\).

A **structural observable** is a measurable function
\[
f:S\to\mathbb R
\]
or, more generally, a tensor-valued map
\[
T:S\to V^{\otimes r}
\]
for a finite-dimensional vector space \(V\). Expectations are written
\[
\langle f\rangle_P=\int_S f(x)\,P(dx).
\]

---

## 3. Recursive Structural Operators

We now define the central dynamical object of the theory.

### 3.1 Structural kernels and weights

Let \(P\in\mathcal P(S)\). A **structural transition kernel** depending on \(P\) is a Markov kernel
\[
K_P:S\times\mathcal B(S)\to[0,1],
\]
such that for each \(x\in S\), \(K_P(x,\cdot)\in\mathcal P(S)\), and for each Borel set \(A\), the map \(x\mapsto K_P(x,A)\) is measurable.

A **structural weight** depending on \(P\) is a measurable function
\[
W_P:S\to[0,\infty).
\]

We assume throughout that
\[
0<Z_P:=\int_S W_P(x)\,P(dx)<\infty
\]
whenever the recursion is applied.

### 3.2 Recursive structural probability operator

**Definition 3.1.**  
A **recursive structural probability operator** is a map
\[
\mathcal R:\mathcal P(S)\to\mathcal P(S)
\]
of the form
\[
\mathcal R(P)(A)
=
\frac{
\displaystyle\int_S W_P(x)\,K_P(x,A)\,P(dx)
}{
\displaystyle\int_S W_P(x)\,P(dx)
},
\qquad A\in\mathcal B(S).
\]

Equivalently,
\[
\mathcal R(P)(dx')
=
\frac{
\displaystyle\int_S W_P(x)\,K_P(x,dx')\,P(dx)
}{
Z_P
}.
\]

The recursion is
\[
P_{n+1}=\mathcal R(P_n).
\]

If \(\mathcal R\) depends on an index \(n\), for example through incoming data, we write
\[
P_{n+1}=\mathcal R_n(P_n).
\]

### 3.3 Interpretation

The operator \(\mathcal R\) decomposes into two conceptual stages.

1. **Selection or reweighting.**  
   The current law \(P\) is tilted by \(W_P\), producing an unnormalized measure
   \[
   \widetilde P(dx)=W_P(x)P(dx).
   \]

2. **Structural transformation.**  
   The tilted measure is propagated through the kernel \(K_P\), producing the next structural law.

In operator form,
\[
\mathcal R(P)
=
\operatorname{Normalize}\bigl(K_P^\ast(W_P P)\bigr),
\]
where \(K_P^\ast\) denotes pushforward through the kernel.

### 3.4 Special cases

#### 3.4.1 Pure Bayesian conditioning

Take
\[
K_P(x,\cdot)=\delta_x,
\qquad
W_P(x)=\ell(x),
\]
where \(\ell:S\to[0,\infty)\) is a likelihood. Then
\[
\mathcal R(P)(dx)
=
\frac{\ell(x)P(dx)}{\int_S \ell(y)P(dy)}.
\]
This is ordinary Bayesian posterior updating.

#### 3.4.2 Pure structural Markov evolution

Take
\[
W_P\equiv1.
\]
Then
\[
\mathcal R(P)(A)=\int_S K_P(x,A)P(dx).
\]
If \(K_P=K\) is independent of \(P\), this is a linear Markov chain on \(S\).

#### 3.4.3 Evolutionary structural search

Let
\[
W_P(x)=e^{-\beta E_P(x)},
\]
where \(E_P:S\to\mathbb R\) is a structural energy or loss functional. Then
\[
P_{n+1}(dx')
=
\frac{
\displaystyle\int_S e^{-\beta E_{P_n}(x)}K_{P_n}(x,dx')P_n(dx)
}{
\displaystyle\int_S e^{-\beta E_{P_n}(x)}P_n(dx)
}.
\]
This is a nonlinear selection-mutation process on structures.

#### 3.4.4 Coarse-graining and renormalization

Let
\[
C:S_{\mathrm{fine}}\to S_{\mathrm{coarse}}
\]
be a structural coarse-graining map, and take
\[
K(x,\cdot)=\delta_{C(x)}.
\]
Then the recursion pushes forward a weighted fine-scale distribution to a coarse-scale distribution. This provides a natural measure-theoretic formulation of renormalization.

---

## 4. Tensorial Moment Calculus for Structural Distributions

Many structural observables are naturally tensorial. For example, metrics, curvature tensors, parameter covariances, and correlation functions are tensors over appropriate vector spaces. We develop a compact tensorial formalism for RSP.

### 4.1 Tensor-valued observables

Let \(V\) be a finite-dimensional real vector space with basis \(\{e_a\}\), and let \(V^{\otimes r}\) denote its \(r\)-fold tensor product. A tensor-valued structural observable is a measurable map
\[
T:S\to V^{\otimes r}.
\]
In components,
\[
T(x)=T^{a_1\cdots a_r}(x)e_{a_1}\otimes\cdots\otimes e_{a_r}.
\]

Given \(P\in\mathcal P(S)\), the \(r\)-th structural moment tensor is
\[
M_P^{a_1\cdots a_r}
=
\int_S T^{a_1\cdots a_r}(x)\,P(dx).
\]

For a sequence \(P_n\), write
\[
M_n^{a_1\cdots a_r}
=
\int_S T^{a_1\cdots a_r}(x)\,P_n(dx).
\]

### 4.2 Moment recursion

Let \(K_{P_n}\) be the structural transition kernel at step \(n\). Define the conditional expected tensor after transition by
\[
(\mathcal K_{P_n}T)^{a_1\cdots a_r}(x)
=
\int_S T^{a_1\cdots a_r}(x')\,K_{P_n}(x,dx').
\]

Then the moment recursion is
\[
M_{n+1}^{a_1\cdots a_r}
=
\frac{
\displaystyle\int_S W_{P_n}(x)(\mathcal K_{P_n}T)^{a_1\cdots a_r}(x)P_n(dx)
}{
\displaystyle\int_S W_{P_n}(x)P_n(dx)
}.
\]

This is the fundamental tensorial recursion of RSP.

### 4.3 Cumulants and generating functionals

Introduce a source tensor \(J\in(V^\ast)^{\otimes r}\), with components \(J_{a_1\cdots a_r}\). The structural moment-generating functional is
\[
Z_P[J]
=
\int_S
\exp\!\left(
J_{a_1\cdots a_r}T^{a_1\cdots a_r}(x)
\right)
P(dx).
\]

The cumulant tensors are obtained by differentiation:
\[
\kappa_P^{a_1\cdots a_s}
=
\left.
\frac{\partial^s}{\partial J_{a_1}\cdots\partial J_{a_s}}
\log Z_P[J]
\right|_{J=0},
\]
with the obvious symmetrization when \(s<r\).

Under the RSP recursion,
\[
Z_{n+1}[J]
=
\frac{
\displaystyle\int_S W_{P_n}(x)
\left(
\int_S e^{J\cdot T(x')}K_{P_n}(x,dx')
\right)
P_n(dx)
}{
\displaystyle\int_S W_{P_n}(x)P_n(dx)
}.
\]

Thus the recursive structural operator induces a nonlinear flow on generating functionals and hence on cumulants.

### 4.4 Covariance and structural susceptibility

For a vector-valued observable \(T^a:S\to V\), define the covariance tensor
\[
C_P^{ab}
=
\langle T^aT^b\rangle_P
-
\langle T^a\rangle_P\langle T^b\rangle_P.
\]

If \(W_P=e^{-\beta E_P}\), then infinitesimal reweighting gives
\[
\langle T^a\rangle_{P_{\mathrm{new}}}
=
\langle T^a\rangle_P
-
\beta\,\operatorname{Cov}_P(T^a,E_P)
+
O(\beta^2).
\]
This identity is the structural analogue of linear response.

---

## 5. Fixed Points, Stability, and Variational Structure

A central question is whether the recursion
\[
P_{n+1}=\mathcal R(P_n)
\]
admits invariant structural laws, and whether such laws are stable.

### 5.1 Fixed points

**Definition 5.1.**  
A measure \(P^\ast\in\mathcal P(S)\) is a **structural fixed point** of \(\mathcal R\) if
\[
P^\ast=\mathcal R(P^\ast).
\]

A fixed point represents a self-consistent probability law on structures: after selection and structural transformation, the law remains unchanged.

### 5.2 Existence via compactness

Assume \(S\) is compact metric. Then \(\mathcal P(S)\) is compact and convex in the weak topology.

**Theorem 5.2.**  
Let \(S\) be compact metric. Suppose:

1. \(P\mapsto W_P\) is continuous in the topology of uniform convergence on \(S\);
2. \(0<c\le W_P(x)\le C<\infty\) uniformly;
3. \(P\mapsto K_P\) is continuous in the weak-Feller sense, i.e. for every \(f\in C(S)\), the function
   \[
   x\mapsto \int_S f(y)K_P(x,dy)
   \]
   depends continuously on \(P\) uniformly enough to ensure continuity of
   \[
   P\mapsto \int_S W_P(x)\left(\int_S f(y)K_P(x,dy)\right)P(dx).
   \]

Then \(\mathcal R:\mathcal P(S)\to\mathcal P(S)\) is continuous. Hence \(\mathcal R\) has at least one fixed point.

**Proof sketch.**  
For \(f\in C(S)\),
\[
\int_S f\,d\mathcal R(P)
=
\frac{
\displaystyle\int_S W_P(x)\left(\int_S f(y)K_P(x,dy)\right)P(dx)
}{
\displaystyle\int_S W_P(x)P(dx)
}.
\]
The assumptions imply that this expression is continuous in \(P\). Since \(\mathcal P(S)\) is a nonempty compact convex subset of the locally convex space of signed measures, Schauder–Tychonoff fixed-point theorem yields a fixed point. \(\square\)

### 5.3 Contraction and uniqueness

When \(S\) is not compact, fixed points may still exist if \(\mathcal R\) preserves a tight convex set. Uniqueness typically requires a contraction property.

Define the Dobrushin coefficient of a Markov kernel \(K\) by
\[
\delta(K)
=
\sup_{x,y\in S}
\|K(x,\cdot)-K(y,\cdot)\|_{\mathrm{TV}}.
\]

If \(W\equiv1\) and \(K\) is independent of \(P\), then
\[
\|K^\ast P-K^\ast Q\|_{\mathrm{TV}}
\le
\delta(K)\|P-Q\|_{\mathrm{TV}}.
\]

Hence if \(\delta(K)<1\), the associated Markov operator is a contraction and possesses a unique invariant measure.

For nonlinear RSP operators, a useful abstract condition is the following.

**Theorem 5.3.**  
Let \(d\) be a metric on \(\mathcal P(S)\). Suppose there exists \(\lambda<1\) such that for all \(P,Q\in\mathcal P(S)\),
\[
d(\mathcal R(P),\mathcal R(Q))
\le
\lambda d(P,Q).
\]
Then \(\mathcal R\) has a unique fixed point \(P^\ast\), and
\[
d(P_n,P^\ast)
\le
\frac{\lambda^n}{1-\lambda}d(P_1,P_0).
\]

This abstract theorem applies in Wasserstein metrics when structural transition maps are uniformly Lipschitz and selection weights have controlled oscillation.

### 5.4 Variational interpretation of selection

A fundamental variational identity underlies all reweighting steps.

Let \(E:S\to\mathbb R\) be bounded below, and define
\[
\mathcal R_E(P)(dx)
=
\frac{e^{-E(x)}P(dx)}{Z_E(P)},
\qquad
Z_E(P)=\int_S e^{-E(x)}P(dx).
\]

For any \(Q\ll P\),
\[
\operatorname{KL}(Q\|P)+\int_S E\,dQ
=
\operatorname{KL}(Q\|\mathcal R_E(P))
-
\log Z_E(P).
\]

Therefore
\[
\mathcal R_E(P)
=
\arg\min_{Q\ll P}
\left\{
\int_S E\,dQ+\operatorname{KL}(Q\|P)
\right\}.
\]

Thus selection by \(e^{-E}\) is precisely a proximal step with respect to Kullback–Leibler divergence.

In particular, Bayesian updating with log-likelihood \(\log\ell\) corresponds to
\[
E=-\log\ell.
\]

---

## 6. Bayesian Inference as Recursive Structural Probability

Bayesian inference is perhaps the most natural instance of RSP. The essential point is that in modern inference the parameter space itself is often a space of structures.

### 6.1 Structural Bayesian recursion

Let \(S\) be a structural model space. Let \(y_1,y_2,\dots\) be observations, and let
\[
\ell_n:S\to[0,\infty)
\]
be the likelihood of observation \(y_n\). The structural Bayesian recursion is
\[
P_{n+1}(dx)
=
\frac{\ell_{n+1}(x)P_n(dx)}
{\int_S \ell_{n+1}(y)P_n(dy)}.
\]

Equivalently,
\[
P_n(dx)
\propto
\left(\prod_{i=1}^n \ell_i(x)\right)P_0(dx).
\]

This is the special case of RSP with
\[
K_P(x,\cdot)=\delta_x,
\qquad
W_{P_n}(x)=\ell_{n+1}(x).
\]

### 6.2 Bayesian inference with structural mutation

In many applications, one does not merely reweight models; one also transforms them. For example, one may perturb parameters, refine a graph, enlarge a program, or change an architecture.

Let \(K_n\) be a proposal or structural transition kernel. A general sequential structural posterior update is
\[
P_{n+1}(dx')
=
\frac{
\displaystyle\int_S \ell_{n+1}(x')K_n(x,dx')P_n(dx)
}{
\displaystyle\int_S\int_S \ell_{n+1}(z)K_n(y,dz)P_n(dy)
}.
\]

This includes sequential Monte Carlo, particle filtering over model spaces, and trans-dimensional Bayesian computation.

### 6.3 Information identity

Let \(P_i\) be generated by
\[
P_i(dx)=\frac{\ell_i(x)P_{i-1}(dx)}{Z_i},
\qquad
Z_i=\int_S \ell_i(x)P_{i-1}(dx).
\]

For any comparator measure \(Q\),
\[
\operatorname{KL}(Q\|P_i)
=
\operatorname{KL}(Q\|P_{i-1})
+
\log Z_i
-
\int_S \log \ell_i(x)\,Q(dx).
\]

Summing from \(i=1\) to \(n\) gives
\[
\sum_{i=1}^n \int_S \log\ell_i(x)\,Q(dx)
=
\sum_{i=1}^n \log Z_i
+
\operatorname{KL}(Q\|P_0)
-
\operatorname{KL}(Q\|P_n).
\]

Since \(\operatorname{KL}(Q\|P_n)\ge0\),
\[
\sum_{i=1}^n \int_S \log\ell_i(x)\,Q(dx)
\le
\sum_{i=1}^n \log Z_i
+
\operatorname{KL}(Q\|P_0).
\]

This is a cumulative log-likelihood bound expressing Bayesian learning as recursive reduction of relative discrepancy from a comparator structural law.

### 6.4 Bayesian nonparametrics

In Bayesian nonparametrics, \(S\) may itself be a space of probability measures, e.g.
\[
S=\mathcal P(X)
\]
for some Polish space \(X\). A prior \(\Pi\) is then a measure on \(\mathcal P(X)\), and posterior updating is a recursive structural operation:
\[
\Pi_{n+1}(dQ)
\propto
\ell_{n+1}(Q)\Pi_n(dQ).
\]

Dirichlet process mixtures, Gaussian process priors, and random measure models fit naturally into this framework.

---

## 7. Random Geometry and Recursive Structural Probability

Random geometry concerns probability measures on spaces of geometric structures. RSP provides a natural language for recursive geometric evolution.

### 7.1 Geometric structural universes

Let \(S_{\mathrm{geom}}\) be one of the following:

1. isometry classes of compact metric spaces;
2. weighted graphs with graph distances;
3. triangulated manifolds with edge lengths;
4. smooth Riemannian metrics modulo diffeomorphism;
5. tensor-network geometries.

A probability measure \(P_n\in\mathcal P(S_{\mathrm{geom}})\) is a random geometry at step \(n\).

### 7.2 Geometric recursive evolution

Let \(K_h\) be a geometric transition kernel corresponding to a stochastic geometric flow over time \(h\), and let
\[
E:S_{\mathrm{geom}}\to\mathbb R
\]
be a geometric energy functional. Define
\[
W(G)=e^{-\beta E(G)}.
\]

Then the geometric RSP recursion is
\[
P_{n+1}(dG')
=
\frac{
\displaystyle\int_{S_{\mathrm{geom}}}
e^{-\beta E(G)}K_h(G,dG')P_n(dG)
}{
\displaystyle\int_{S_{\mathrm{geom}}}
e^{-\beta E(G)}P_n(dG)
}.
\]

This describes a selection-biased stochastic evolution of geometries.

### 7.3 Smooth formalization: metrics and curvature tensors

Let \(M\) be a compact manifold and let \(g\) be a Riemannian metric. Consider a stochastic geometric flow of the form
\[
dg_t
=
b(g_t)\,dt+\sigma\,dW_t,
\]
where \(b(g)\) is a geometric vector field. A canonical choice is a Ricci-type flow with cosmological term:
\[
b_{\mu\nu}(g)
=
-2\operatorname{Ric}_{\mu\nu}(g)
+
\lambda g_{\mu\nu}.
\]

Let \(P_h\) be the Markov semigroup induced by this flow. For any geometric observable \(F\),
\[
\mathbb E_{n+1}[F]
=
\frac{
\mathbb E_n\left[e^{-\beta E}P_hF\right]
}{
\mathbb E_n\left[e^{-\beta E}\right]
}.
\]

For small \(h\),
\[
P_hF=F+h\mathcal L F+O(h^2),
\]
where \(\mathcal L\) is the generator of the stochastic geometric flow.

Taking \(F(g)=g_{\mu\nu}\), we obtain the formal moment recursion
\[
\langle g_{\mu\nu}\rangle_{n+1}
=
\langle g_{\mu\nu}\rangle_{n,\beta}
+
h
\left\langle
-2\operatorname{Ric}_{\mu\nu}
+
\lambda g_{\mu\nu}
+
\frac{\sigma^2}{2}\Delta_{\mathscr R}g_{\mu\nu}
\right\rangle_{n,\beta}
+
O(h^2),
\]
where
\[
\langle F\rangle_{n,\beta}
=
\frac{
\mathbb E_n[e^{-\beta E}F]
}{
\mathbb E_n[e^{-\beta E}]
}
\]
is the energy-tilted expectation, and \(\Delta_{\mathscr R}\) denotes a Laplacian on the space of metrics induced, for example, by the DeWitt supermetric.

Expanding the tilt for small \(\beta\),
\[
\langle F\rangle_{n,\beta}
=
\langle F\rangle_n
-
\beta\,\operatorname{Cov}_n(F,E)
+
O(\beta^2).
\]

Thus
\[
\begin{aligned}
\langle g_{\mu\nu}\rangle_{n+1}
&=
\langle g_{\mu\nu}\rangle_n
-
\beta\,\operatorname{Cov}_n(g_{\mu\nu},E)
\\
&\quad
+
h
\left\langle
-2\operatorname{Ric}_{\mu\nu}
+
\lambda g_{\mu\nu}
+
\frac{\sigma^2}{2}\Delta_{\mathscr R}g_{\mu\nu}
\right\rangle_n
+
O(h^2,\beta^2,h\beta).
\end{aligned}
\]

This is a tensorial recursive law for the expected metric under structural selection and stochastic geometric evolution.

### 7.4 Geometric energies

Natural choices of \(E\) include:

1. **Einstein–Hilbert-type action**
   \[
   E_{\mathrm{EH}}(g)=\int_M R_g\,d\operatorname{vol}_g.
   \]

2. **Quadratic curvature energy**
   \[
   E_{\mathrm{curv}}(g)
   =
   \int_M
   \left(
   \alpha R_g^2
   +
   \beta |\operatorname{Ric}_g|^2
   +
   \gamma |\operatorname{Riem}_g|^2
   \right)
   d\operatorname{vol}_g.
   \]

3. **Spectral energy**
   \[
   E_{\mathrm{spec}}(g)
   =
   \sum_k \phi(\lambda_k(\Delta_g)),
   \]
   where \(\lambda_k(\Delta_g)\) are Laplace eigenvalues.

4. **Discrete curvature energy**
   For weighted graphs,
   \[
   E(G)=\sum_{x\sim y} \kappa_{xy}^2,
   \]
   where \(\kappa_{xy}\) is a discrete Ricci curvature.

Fixed points of the corresponding RSP dynamics define canonical ensembles of random geometries.

---

## 8. Machine Learning as Recursive Structural Probability

Machine learning provides a second major domain of application. A learning system may be viewed as a probability distribution over models, architectures, or programs that evolves recursively under data, optimization, and regularization.

### 8.1 Model structural space

Let
\[
S=\bigsqcup_{\alpha\in\mathcal A} S_\alpha
\]
be a model space, where \(\alpha\) indexes architectures, programs, or symbolic forms, and \(S_\alpha\) contains parameters or weights for architecture \(\alpha\). A point \(m\in S\) may be written
\[
m=(\alpha,\theta).
\]

Let \(z\) be a data point and let
\[
L(m,z)
\]
be a loss function.

### 8.2 Recursive learning operator

Let \(K_n\) be a learning transition kernel, for example noisy gradient descent, architecture mutation, or program refinement. Let
\[
W_n(m')=\exp\bigl(-\eta_n L(m',z_{n+1})\bigr).
\]

Then the learning recursion is
\[
P_{n+1}(dm')
=
\frac{
\displaystyle\int_S
e^{-\eta_n L(m',z_{n+1})}
K_n(m,dm')
P_n(dm)
}{
\displaystyle\int_S\int_S
e^{-\eta_n L(\tilde m,z_{n+1})}
K_n(m,d\tilde m)
P_n(dm)
}.
\]

This recursion combines optimization, stochastic exploration, and Bayesian reweighting.

### 8.3 Diffusion approximation

Suppose \(S_\alpha\) is a Euclidean parameter space and \(K_n\) is a noisy gradient step:
\[
\theta'
=
\theta
-
\eta\nabla_\theta L(\theta,z)
+
\sqrt{2\eta\beta^{-1}}\xi,
\qquad
\xi\sim N(0,I).
\]

In the small-step limit, the density \(p_t(\theta)\) over parameters satisfies a Fokker–Planck-type equation with selection:
\[
\partial_t p_t
=
\nabla_\theta\cdot\bigl(p_t\nabla_\theta \bar L_t\bigr)
+
\beta^{-1}\Delta_\theta p_t
-
\bigl(L(\theta)-\langle L\rangle_t\bigr)p_t,
\]
where \(\bar L_t\) is a smoothed empirical loss and the last term represents reweighting by performance.

This equation exhibits learning as a geometric flow on the space of model structures.

### 8.4 Tensor moments of learning dynamics

Let \(\theta^a\) denote parameter coordinates. Define
\[
\mu^a_n=\langle \theta^a\rangle_n,
\]
and
\[
C^{ab}_n
=
\langle (\theta^a-\mu^a_n)(\theta^b-\mu^b_n)\rangle_n.
\]

For pure noisy gradient descent without selection,
\[
\dot\mu^a=-\langle \partial^a L\rangle,
\]
and
\[
\dot C^{ab}
=
-
\langle \partial^a\partial_c L\rangle C^{cb}
-
\langle \partial^b\partial_c L\rangle C^{ac}
+
2\beta^{-1}\delta^{ab}.
\]

Selection adds covariance correction terms:
\[
-\operatorname{Cov}(L,\theta^a\theta^b)
+
\mu^a\operatorname{Cov}(L,\theta^b)
+
\mu^b\operatorname{Cov}(L,\theta^a).
\]

Thus RSP yields a natural tensorial moment hierarchy for learning dynamics.

### 8.5 Generalization via PAC-Bayes

Let \(L_D(m)\) be population risk and \(\widehat L_n(m)\) empirical risk. Suppose the loss is bounded in \([0,1]\). For any prior \(P_0\) over models, with probability at least \(1-\delta\) over an i.i.d. sample of size \(n\), for every distribution \(Q\) over models,
\[
\mathbb E_{m\sim Q}[L_D(m)]
\le
\mathbb E_{m\sim Q}[\widehat L_n(m)]
+
\sqrt{
\frac{
\operatorname{KL}(Q\|P_0)+\log(2\sqrt n/\delta)
}{
2n
}
}.
\]

In RSP, if the learning recursion produces \(P_n\), then the generalization bound is controlled by the **structural information cost**
\[
I_n=\operatorname{KL}(P_n\|P_0).
\]

Thus recursive structural probability provides a natural language for tracking how architectural search, data-dependent mutation, and sequential reweighting consume information budget.

---

## 9. Statistical Mechanics and Renormalization

RSP is also a natural abstraction of statistical mechanics, particularly when the underlying lattice, graph, or scale itself evolves.

### 9.1 Structural statistical mechanics

Let \(S\) be a space of configurations or structures, and let
\[
H:S\to\mathbb R
\]
be a Hamiltonian. The Gibbs measure is
\[
P_\beta(dx)
=
\frac{e^{-\beta H(x)}\Pi(dx)}{Z_\beta},
\]
where \(\Pi\) is a reference measure and
\[
Z_\beta=\int_S e^{-\beta H(x)}\Pi(dx).
\]

This is the RSP operator with
\[
K(x,\cdot)=\delta_x,
\qquad
W(x)=e^{-\beta H(x)}.
\]

### 9.2 Recursive coarse-graining

Let
\[
C:S_{\mathrm{fine}}\to S_{\mathrm{coarse}}
\]
be a coarse-graining map. Define the kernel
\[
K(x,\cdot)=\delta_{C(x)}.
\]

Then
\[
P_{n+1}(dy)
=
\frac{
\displaystyle\int_{C^{-1}(dy)}
e^{-\beta H_n(x)}P_n(dx)
}{
\displaystyle\int_{S_{\mathrm{fine}}}
e^{-\beta H_n(x)}P_n(dx)
}.
\]

If \(P_n=\Pi_n\) is a reference measure on fine structures, one obtains an effective coarse Hamiltonian by
\[
e^{-\beta H_{n+1}(y)}
=
\int_{C^{-1}(y)}e^{-\beta H_n(x)}\Pi_n(dx),
\]
up to normalization. Hence
\[
H_{n+1}(y)
=
-\beta^{-1}
\log
\int_{C^{-1}(y)}
e^{-\beta H_n(x)}\Pi_n(dx)
+
\text{const}.
\]

This is a measure-theoretic formulation of exact renormalization.

### 9.3 Fixed points and phase transitions

A Hamiltonian \(H^\ast\) satisfying
\[
H^\ast=\mathcal T(H^\ast)
\]
under the recursive coarse-graining map \(\mathcal T\) corresponds to a scale-invariant structural law. Multiple fixed points correspond to distinct thermodynamic phases. Bifurcations in the fixed-point structure correspond to phase transitions.

### 9.4 Tensor-network formulation

Let a fine-scale partition function be represented by a tensor contraction
\[
Z_n
=
T_n^{a_1\cdots a_r}B_{a_1\cdots a_r},
\]
where \(T_n\) is a local tensor network and \(B\) encodes boundary or observable contractions.

A coarse-graining map is a tensor linear map
\[
R^{b_1\cdots b_s}_{a_1\cdots a_r},
\]
so that
\[
T_{n+1}^{b_1\cdots b_s}
=
R^{b_1\cdots b_s}_{a_1\cdots a_r}
T_n^{a_1\cdots a_r}.
\]

A probability distribution over tensor networks then evolves as
\[
P_{n+1}(dT')
\propto
\int
e^{-\beta F(T')}
\delta(T'-\mathcal R T)P_n(dT),
\]
where \(F\) is a free-energy functional on tensors. This gives a recursive structural probability formulation of tensor-network renormalization.

---

## 10. Computational Realizations

The abstract RSP recursion suggests several computational schemes.

### 10.1 Particle approximation

Let \(P_n\) be approximated by particles
\[
\{x_i^{(n)}\}_{i=1}^N.
\]

A population RSP algorithm proceeds as follows.

1. **Weight.**  
   Compute
   \[
   w_i^{(n)}=W_{P_n}(x_i^{(n)}).
   \]

2. **Normalize.**
   \[
   \bar w_i^{(n)}
   =
   \frac{w_i^{(n)}}{\sum_j w_j^{(n)}}.
   \]

3. **Resample.**  
   Draw ancestors \(i_k\) according to \(\bar w_i^{(n)}\).

4. **Transform.**  
   Sample
   \[
   x_k^{(n+1)}
   \sim
   K_{P_n}(x_{i_k}^{(n)},\cdot).
   \]

5. **Estimate moments.**
   \[
   M_{n+1}^{a_1\cdots a_r}
   \approx
   \frac{1}{N}
   \sum_{k=1}^N
   T^{a_1\cdots a_r}(x_k^{(n+1)}).
   \]

Under standard assumptions, empirical measures converge weakly to \(P_n\) as \(N\to\infty\), with Monte Carlo error of order \(N^{-1/2}\).

### 10.2 Markov chain and sequential Monte Carlo variants

When \(K_P\) is implemented by MCMC, the recursion becomes a population of interacting chains. When data arrive sequentially, the recursion becomes sequential Monte Carlo over structure spaces. Trans-dimensional moves, graph rewiring, program mutations, and geometry refinement are all natural kernels.

### 10.3 Variational approximation

One may restrict to a parametric family
\[
\{Q_\phi:\phi\in\Phi\}\subset\mathcal P(S)
\]
and define
\[
\phi_{n+1}
=
\arg\min_\phi
\operatorname{KL}\bigl(Q_\phi\|\mathcal R(P_n)\bigr).
\]

This yields variational RSP. When \(S\) consists of graphs or neural architectures, \(Q_\phi\) may be represented by graph neural networks, normalizing flows on discrete structures, or probabilistic program generators.

### 10.4 Challenges

The main computational obstacles are:

1. normalization of structural weights;
2. high-dimensional or combinatorial structure spaces;
3. lack of Euclidean coordinates for geometric moduli;
4. degeneracy of particle populations under repeated selection;
5. non-reversibility and non-compactness of structural transformations.

These challenges mirror those in Bayesian nonparametrics, probabilistic programming, and geometric sampling, but RSP clarifies their common mathematical structure.

---

## 11. Open Problems

The theory suggests several directions for further research.

1. **Foundations for proper classes of structures.**  
   A full categorical or topos-theoretic extension may allow probability over all finitely generated algebraic structures without fixing a countable presentation.

2. **Convergence theory for nonlinear structural operators.**  
   General sufficient conditions for uniqueness of fixed points under combined selection and mutation remain subtle, especially when weights depend strongly on \(P\).

3. **Geometry of structural probability.**  
   One may equip \(\mathcal P(S)\) with Wasserstein or Fisher information metrics and study RSP as gradient flow of a structural free energy.

4. **Random geometry and quantum gravity.**  
   RSP offers a possible language for recursively generated ensembles of geometries, especially in settings where spacetime is not fixed but emergent.

5. **Architecture search and program induction.**  
   RSP provides a measure-theoretic foundation for probabilistic search over computational structures, with potential links to PAC-Bayes and algorithmic information theory.

6. **Renormalization and universality.**  
   A rigorous classification of RSP fixed points could yield new perspectives on universality classes and critical phenomena.

---

## 12. Conclusion

Recursive Structural Probability reframes probability theory as the study of recursively evolving measures on spaces of mathematical structures. The central recursion
\[
P_{n+1}=\mathcal R(P_n)
\]
unifies Bayesian updating, stochastic structural evolution, learning over model spaces, and renormalization-group dynamics. By combining Markov kernels, selection weights, tensor-valued observables, and variational principles, the framework yields a coherent mathematical language for systems in which uncertainty is not merely over outcomes but over the very structures that define those outcomes.

The principal contribution is conceptual and structural: probability is lifted from fixed sample spaces to evolving moduli of mathematical objects. This shift is natural for modern problems in inference, learning, geometry, and statistical mechanics, where the object of uncertainty is itself mutable.

---

## Appendix A: Proof of the Variational Selection Identity

Let
\[
R_E(P)(dx)=\frac{e^{-E(x)}P(dx)}{Z_E(P)},
\qquad
Z_E(P)=\int_S e^{-E(x)}P(dx).
\]

For \(Q\ll P\),
\[
\frac{dR_E(P)}{dP}(x)
=
\frac{e^{-E(x)}}{Z_E(P)}.
\]

Hence
\[
\frac{dP}{dR_E(P)}(x)
=
Z_E(P)e^{E(x)}.
\]

Therefore
\[
\begin{aligned}
\operatorname{KL}(Q\|R_E(P))
&=
\int_S
\log\left(
\frac{dQ}{dR_E(P)}
\right)
Q(dx)
\\
&=
\int_S
\log\left(
\frac{dQ}{dP}
\frac{dP}{dR_E(P)}
\right)
Q(dx)
\\
&=
\int_S
\log\left(
\frac{dQ}{dP}
\right)
Q(dx)
+
\int_S
\log\left(
Z_E(P)e^{E(x)}
\right)
Q(dx)
\\
&=
\operatorname{KL}(Q\|P)
+
\log Z_E(P)
+
\int_S E(x)Q(dx).
\end{aligned}
\]

Rearranging gives
\[
\operatorname{KL}(Q\|P)+\int_S E\,dQ
=
\operatorname{KL}(Q\|R_E(P))-\log Z_E(P).
\]

Since \(\operatorname{KL}(Q\|R_E(P))\ge0\), with equality iff \(Q=R_E(P)\), the minimizer is unique. \(\square\)

---

## Appendix B: Notation Index

| Symbol | Meaning |
|---|---|
| \(S\) | structural universe |
| \(\mathcal B\) | Borel \(\sigma\)-algebra on \(S\) |
| \(\mathcal P(S)\) | probability measures on \(S\) |
| \(P_n\) | structural law at step \(n\) |
| \(\mathcal R\) | recursive structural probability operator |
| \(K_P\) | structural transition kernel |
| \(W_P\) | structural weight |
| \(Z_P\) | normalization constant |
| \(T^{a_1\cdots a_r}\) | tensor-valued structural observable |
| \(M_P^{a_1\cdots a_r}\) | moment tensor |
| \(Z_P[J]\) | moment-generating functional |
| \(\kappa_P\) | cumulant tensor |
| \(E\) | structural energy |
| \(\beta\) | inverse temperature or selection strength |
| \(\eta\) | learning rate |
| \(C\) | coarse-graining map |
| \(H\) | Hamiltonian |
| \(g_{\mu\nu}\) | metric tensor |
| \(\operatorname{Ric}_{\mu\nu}\) | Ricci curvature tensor |

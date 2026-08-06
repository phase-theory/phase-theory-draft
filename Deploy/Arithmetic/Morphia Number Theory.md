# Morphic Number Theory: Invariant Evolution of Arithmetic States

**White paper / academic preprint**

---

## Abstract

Morphic Number Theory (MNT) is a framework in which numbers are not treated as fixed arithmetic atoms but as *arithmetic states possessing internal evolution*. A number is modeled as a point in an arithmetic state space together with a morphic evolution operator constrained to preserve an invariant identity. The basic object is therefore not a bare element \(a\), but a pointed morphic system
\[
(x,\Phi,\pi),
\]
where \(x\) is an arithmetic state, \(\Phi\) is an endomorphism describing internal evolution, and \(\pi\) is an invariant projection encoding the persistent identity of the number. The central condition is
\[
\pi\circ \Phi=\pi.
\]
Thus the number evolves internally while its invariant identity remains unchanged.

This paper develops the foundational definitions of MNT, gives a categorical formulation, introduces a tensorial formalism for morphic evolution, connects the theory to arithmetic dynamics through heights and periodic-point zeta functions, develops algebraic structures such as morphic rings and modules, presents computational algorithms for invariant and orbit calculations, and formulates cryptographic primitives based on hard morphic orbit problems. Concrete examples include congruence-preserving integer evolutions, norm-preserving unit actions in quadratic orders, and finite-field linear morphic systems. The result is a unified language for studying arithmetic objects as dynamically evolving entities constrained by invariant identities.

---

## 1. Introduction

Classical number theory usually treats numbers as static elements of algebraic structures: integers are elements of \(\mathbb Z\), algebraic integers are elements of rings of integers \(\mathcal O_K\), ideals are fixed submodules, and rational points are fixed solutions of equations. Arithmetic dynamics introduces iteration, but typically as an external process acting on otherwise static points.

Morphic Number Theory reverses this perspective.

The guiding principle of MNT is:

> A number is an arithmetic state equipped with an internal evolution law, and the identity of the number is carried by invariants preserved under that evolution.

Thus a number is not merely \(n\in\mathbb Z\), nor merely an orbit \(\{n,\Phi(n),\Phi^2(n),\dots\}\), but a structured object consisting of:

1. a state \(x\);
2. an evolution operator \(\Phi\);
3. an invariant identity \(\pi(x)\);
4. an equivalence relation identifying structurally identical morphic systems.

The fundamental axiom is that the evolution is internal to a fixed invariant fiber:
\[
x\longmapsto \Phi(x),\qquad \pi(\Phi(x))=\pi(x).
\]
The number changes internally while remaining the same number in the sense of its invariant identity.

This idea naturally connects several areas:

- **Arithmetic dynamics**, because morphic evolution is iteration of arithmetic endomorphisms;
- **Invariant theory**, because persistent identity is encoded by invariant functions or tensors;
- **Algebraic geometry**, because state spaces and invariant bases are naturally schemes or varieties;
- **Computational number theory**, because orbit computation, invariant computation, and lifting problems are algorithmic primitives;
- **Cryptography**, because morphic orbit problems provide natural candidates for one-way transformations.

The purpose of this paper is to give a systematic foundation for MNT. We define morphic systems, morphic numbers, invariant tensors, morphic heights, morphic zeta functions, morphic rings, and several hard computational problems suitable for cryptographic instantiation.

---

## 2. Foundations of Morphic Number Theory

### 2.1 Arithmetic state spaces

Let \(B\) be a base scheme, which we call the **invariant identity space**. Let \(X\) be a scheme over \(B\), with structure morphism
\[
\pi:X\longrightarrow B.
\]
The fiber over a point \(s\in B\) is
\[
X_s=\pi^{-1}(s).
\]
Points of \(X\) are interpreted as arithmetic states, while points of \(B\) are interpreted as invariant identities.

For a ring of arithmetic interest \(R\), an \(R\)-arithmetic state is a point
\[
x\in X(R).
\]
Its invariant identity is
\[
s=\pi(x)\in B(R).
\]

---

### 2.2 Morphic systems

**Definition 2.1.** A **morphic arithmetic system** over \(B\) is a triple
\[
(X/B,\Phi,\pi)
\]
where \(X\) is a scheme over \(B\), \(\pi:X\to B\) is the structure morphism, and
\[
\Phi:X\longrightarrow X
\]
is a \(B\)-endomorphism, i.e.
\[
\pi\circ\Phi=\pi.
\]

The map \(\Phi\) is called the **morphic evolution operator**.

For any state \(x\in X(R)\), define the **morphic evolution sequence**
\[
x_0=x,\qquad x_{n+1}=\Phi(x_n).
\]
Then
\[
x_n=\Phi^n(x).
\]

Because \(\Phi\) is a \(B\)-morphism, all states \(x_n\) lie in the same fiber:
\[
\pi(x_n)=\pi(x_0).
\]

---

### 2.3 Morphic numbers

**Definition 2.2.** A **pointed morphic state** over \(R\) is a quadruple
\[
(X/B,\Phi,x,R),
\]
where \(x\in X(R)\) and \(\Phi:X\to X\) is a \(B\)-endomorphism.

Two pointed morphic states
\[
(X/B,\Phi,x),\qquad (Y/B,\Psi,y)
\]
are called **morphic equivalent** if there exists a \(B\)-isomorphism
\[
F:X\overset{\sim}{\longrightarrow} Y
\]
such that
\[
F\circ\Phi=\Psi\circ F
\]
and
\[
F(x)=y.
\]

**Definition 2.3.** A **morphic number** is an equivalence class of pointed morphic states under morphic equivalence.

Thus, formally, a morphic number is not the value \(x\) alone, but the class
\[
[X/B,\Phi,x].
\]

The invariant identity of the morphic number is
\[
\pi(x)\in B(R).
\]

The internal evolution of the morphic number is the orbit
\[
x,\Phi(x),\Phi^2(x),\dots
\]
inside the fixed fiber \(X_{\pi(x)}\).

---

### 2.4 Invariant propagation

The most basic theorem of MNT is that invariant identities are preserved under morphic evolution.

**Proposition 2.4.** Let \((X/B,\Phi)\) be a morphic arithmetic system. For every \(x\in X(R)\) and every \(n\ge 0\),
\[
\pi(\Phi^n(x))=\pi(x).
\]

*Proof.* The case \(n=0\) is immediate. Suppose
\[
\pi(\Phi^n(x))=\pi(x).
\]
Then
\[
\pi(\Phi^{n+1}(x))
=
\pi(\Phi(\Phi^n(x)))
=
\pi(\Phi^n(x))
=
\pi(x),
\]
where the middle equality uses \(\pi\circ\Phi=\pi\). By induction, the result holds for all \(n\). \(\square\)

If \(I\) is a global function on \(B\), then \(I\circ\pi\) is an invariant function on \(X\). Hence
\[
I(\pi(\Phi^n(x)))=I(\pi(x)).
\]
Equivalently, every invariant identity observable is constant along the morphic evolution.

---

### 2.5 The category of morphic numbers

Let \(\mathbf{MNum}_B\) be the category whose objects are morphic systems
\[
(X/B,\Phi)
\]
and whose morphisms are \(B\)-morphisms commuting with evolution:
\[
F:(X,\Phi)\longrightarrow (Y,\Psi)
\]
such that
\[
F\circ\Phi=\Psi\circ F.
\]

A pointed morphic number is then an object of the coslice category under the terminal point, or equivalently a pair
\[
((X,\Phi),x)
\]
with \(x\in X(R)\).

This categorical formulation is useful because it allows standard constructions:

- products of morphic systems;
- fibered products over invariant bases;
- quotients by commuting group actions;
- limits and colimits of evolving arithmetic states;
- functors to dynamical systems, schemes, modules, or tensor categories.

---

## 3. Invariant Algebras and Morphic Cohomology

Suppose \(X=\operatorname{Spec} A\) and \(B=\operatorname{Spec} C\), with
\[
C\subseteq A.
\]
A morphic endomorphism \(\Phi:X\to X\) induces a ring endomorphism
\[
\Phi^*:A\longrightarrow A.
\]
The condition that \(\Phi\) is over \(B\) is equivalent to
\[
\Phi^*(c)=c,\qquad \forall c\in C.
\]

The invariant subring is
\[
A^\Phi=\{a\in A:\Phi^*(a)=a\}.
\]

Define the difference operator
\[
\Delta=\Phi^*-\operatorname{id}_A.
\]
Then
\[
A^\Phi=\ker \Delta.
\]

### 3.1 Finite-order morphic systems

Suppose \(\Phi\) has finite order \(m\), i.e.
\[
\Phi^m=\operatorname{id}.
\]
Assume that \(m\) is invertible in the coefficient field. Define the Reynolds averaging operator
\[
\mathcal R:A\longrightarrow A,
\qquad
\mathcal R(f)=\frac1m\sum_{j=0}^{m-1}(\Phi^*)^j(f).
\]

Then \(\mathcal R(f)\in A^\Phi\), because
\[
\Phi^*\mathcal R(f)
=
\frac1m\sum_{j=0}^{m-1}(\Phi^*)^{j+1}(f)
=
\frac1m\sum_{j=1}^{m}(\Phi^*)^j(f).
\]
Since \((\Phi^*)^m=\operatorname{id}\), this equals
\[
\frac1m\sum_{j=0}^{m-1}(\Phi^*)^j(f)
=
\mathcal R(f).
\]

Moreover, one has a direct-sum decomposition
\[
A=A^\Phi\oplus \operatorname{im}\Delta.
\]

Indeed, for any \(f\in A\), define
\[
g=\frac1m\sum_{j=1}^{m-1}j(\Phi^*)^j(f).
\]
Then a direct calculation gives
\[
\Delta g=f-\mathcal R(f).
\]
Thus
\[
f=\mathcal R(f)+\Delta g,
\]
with \(\mathcal R(f)\in A^\Phi\) and \(\Delta g\in\operatorname{im}\Delta\).

This decomposition formalizes the idea that, in finite-order morphic systems, functions split into an invariant identity part and a purely morphic variation part.

---

## 4. Tensorial Formalism for Morphic Evolution

In many arithmetic settings, the state of a number is naturally represented by a tensor. This section develops a tensorial notation for morphic evolution and invariant identities.

Let \(R\) be a commutative ring and let \(V\) be a finite free \(R\)-module. We use abstract index notation and the Einstein summation convention.

### 4.1 Arithmetic state tensors

Let an arithmetic state be represented by a tensor
\[
N\in T(V)=\bigoplus_{p,q\ge0} V^{\otimes p}\otimes (V^*)^{\otimes q}.
\]
In components, write
\[
N^A,
\]
where \(A\) is a multi-index appropriate to the tensor type.

A morphic evolution is a tensor-valued map
\[
N\longmapsto N'=\Phi(N).
\]

In the linear case,
\[
N'^A=M^A{}_B N^B,
\]
where
\[
M^A{}_B
\]
is the **morphic transfer tensor**.

In the polynomial case, one may write
\[
N'^A
=
\sum_{d\ge0}
C^A{}_{B_1\cdots B_d}
N^{B_1}\cdots N^{B_d},
\]
where the tensors \(C^A{}_{B_1\cdots B_d}\) encode nonlinear morphic structure.

---

### 4.2 Invariant tensors

Let \(G_{A_1\cdots A_r}\) be a covariant tensor. It defines a scalar functional
\[
J_G(N)=G_{A_1\cdots A_r}N^{A_1}\cdots N^{A_r}.
\]

We say that \(G\) is a **morphic invariant tensor** if
\[
J_G(\Phi(N))=J_G(N)
\]
for all states \(N\).

For a linear morphic operator \(M^A{}_B\), this becomes
\[
G_{A_1\cdots A_r}
M^{A_1}{}_{B_1}\cdots M^{A_r}{}_{B_r}
N^{B_1}\cdots N^{B_r}
=
G_{B_1\cdots B_r}
N^{B_1}\cdots N^{B_r}.
\]
Since this must hold for all \(N\), the tensor invariance condition is
\[
G_{A_1\cdots A_r}
M^{A_1}{}_{B_1}\cdots M^{A_r}{}_{B_r}
=
G_{B_1\cdots B_r}.
\]

Equivalently,
\[
(M^{\otimes r})^*G=G.
\]

---

### 4.3 Infinitesimal morphic transformations

Suppose the morphic operator is close to the identity:
\[
M^A{}_B=\delta^A{}_B+\varepsilon L^A{}_B+O(\varepsilon^2).
\]
Then
\[
N'^A=N^A+\varepsilon L^A{}_B N^B+O(\varepsilon^2).
\]

The invariant scalar becomes
\[
J_G(N')
=
G_{A_1\cdots A_r}
N'^{A_1}\cdots N'^{A_r}.
\]
Expanding to first order gives
\[
J_G(N')
=
J_G(N)
+
\varepsilon
\sum_{a=1}^r
G_{A_1\cdots A_{a-1} C A_{a+1}\cdots A_r}
L^C{}_{A_a}
N^{A_1}\cdots N^{A_r}
+
O(\varepsilon^2).
\]

Thus \(G\) is infinitesimally invariant precisely when
\[
\sum_{a=1}^r
G_{A_1\cdots A_{a-1} C A_{a+1}\cdots A_r}
L^C{}_{A_a}
=0.
\]

This is the discrete analogue of a Lie-derivative condition:
\[
\mathcal L_L G=0.
\]

---

### 4.4 Internal/external decomposition

A particularly important case occurs when the state tensor decomposes as
\[
V=U\otimes W,
\]
and the morphic operator has the form
\[
\Phi=\phi\otimes \operatorname{id}_W.
\]
Then the \(W\)-coordinates are invariant under evolution. In components,
\[
N^{i\alpha}
\]
with \(i\) indexing \(U\) and \(\alpha\) indexing \(W\), the evolution acts only on the \(i\)-index:
\[
N'^{i\alpha}=M^i{}_j N^{j\alpha}.
\]
The \(\alpha\)-structure is the invariant identity, while the \(i\)-structure undergoes internal morphic evolution.

This provides a tensorial model of the central MNT principle:

> The identity of a number is carried by invariant tensor directions; its internal state evolves along complementary tensor directions.

---

## 5. Morphic Arithmetic Dynamics

Morphic Number Theory is closely related to arithmetic dynamics, but with a different emphasis: the dynamical system is required to preserve an invariant base.

Let \(K\) be a number field and let \(X\) be a projective variety over \(K\). Let
\[
f:X\longrightarrow X
\]
be a morphism. Suppose there is a morphism
\[
\pi:X\longrightarrow S
\]
such that
\[
\pi\circ f=\pi.
\]
Then \(f\) is a morphic evolution over the invariant base \(S\).

---

### 5.1 Canonical heights and invariant identities

Assume that \(f\) is polarized by an ample line bundle \(L\), meaning
\[
f^*L\cong L^{\otimes d}
\]
for some integer \(d>1\). The Call–Silverman canonical height is
\[
\widehat h_f(x)
=
\lim_{n\to\infty}
\frac{h_L(f^n(x))}{d^n}.
\]

It satisfies
\[
\widehat h_f(f(x))=d\,\widehat h_f(x).
\]

Because \(f\) is over \(S\), the invariant identity is preserved:
\[
\pi(f^n(x))=\pi(x).
\]
Thus, even though the canonical height may grow under evolution, the base identity remains fixed.

If \(d=1\), i.e. \(f\) is an automorphism preserving an ample height, then
\[
\widehat h_f(f(x))=\widehat h_f(x),
\]
and the canonical height itself becomes an invariant of the morphic evolution.

If \(I\in K(X)\) is an invariant rational function,
\[
I\circ f=I,
\]
then along any orbit avoiding poles,
\[
I(f^n(x))=I(x).
\]
By functoriality of heights,
\[
h(I(f^n(x)))=h(I(x)).
\]

Thus invariant functions provide arithmetic identities that are exactly conserved by morphic evolution.

---

### 5.2 Preperiodic morphic numbers

For polarized morphisms over number fields, Northcott-type finiteness implies that the set of points of bounded height and bounded degree is finite. Consequently, for many standard systems,
\[
\widehat h_f(x)=0
\]
if and only if \(x\) is preperiodic under \(f\).

In MNT language:

> A morphic number has vanishing canonical dynamical height precisely when its internal evolution is eventually periodic.

Thus periodic and preperiodic morphic numbers are the analogues of torsion or bounded-complexity arithmetic states.

---

### 5.3 Morphic zeta functions over finite fields

Let \(X\) be a finite set, or let \(X(\mathbb F_q)\) be the set of rational points of a variety over a finite field. Suppose
\[
\Phi:X\longrightarrow X
\]
preserves an invariant map
\[
\pi:X\longrightarrow S.
\]
For each \(n\ge1\), define the fixed-point set
\[
\operatorname{Fix}(\Phi^n)=\{x\in X:\Phi^n(x)=x\}.
\]

The Artin–Mazur dynamical zeta function is
\[
\zeta_\Phi(t)
=
\exp\left(
\sum_{n=1}^{\infty}
\frac{|\operatorname{Fix}(\Phi^n)|}{n}
t^n
\right).
\]

Because \(\pi\circ\Phi=\pi\), fixed points decompose according to invariant identities:
\[
\operatorname{Fix}(\Phi^n)
=
\bigsqcup_{s\in S}
\operatorname{Fix}(\Phi^n|_{X_s}).
\]
Therefore
\[
\zeta_\Phi(t)
=
\prod_{s\in S}
\zeta_{\Phi,s}(t),
\]
where
\[
\zeta_{\Phi,s}(t)
=
\exp\left(
\sum_{n=1}^{\infty}
\frac{|\operatorname{Fix}(\Phi^n|_{X_s})|}{n}
t^n
\right).
\]

This factorization expresses the global periodic-point structure as a product of morphic periodic-point structures over invariant identities.

---

### 5.4 Cycle counting in finite bijective morphic systems

Suppose \(X_s\) is finite and \(\Phi|_{X_s}\) is a permutation of order \(m\). The number of cycles in the fiber \(X_s\) is given by Burnside’s lemma:
\[
\#\operatorname{Cycles}(\Phi|_{X_s})
=
\frac1m
\sum_{k=0}^{m-1}
|\operatorname{Fix}(\Phi^k)\cap X_s|.
\]

This formula gives the number of distinct morphic numbers in a finite fiber when morphic numbers are identified along cycles.

---

## 6. Algebraic Structures in Morphic Number Theory

### 6.1 Morphic rings

**Definition 6.1.** A **morphic ring** is a pair
\[
(R,\sigma)
\]
where \(R\) is a commutative ring and
\[
\sigma:R\longrightarrow R
\]
is a ring endomorphism.

The invariant subring is
\[
R^\sigma=\{r\in R:\sigma(r)=r\}.
\]

An element \(x\in R\) may be regarded as a morphic arithmetic state with evolution
\[
x_n=\sigma^n(x).
\]

The invariant identity of \(x\) is the collection of values of elements of \(R^\sigma\) evaluated at \(x\).

---

### 6.2 Morphic ideals and quotients

An ideal \(I\subset R\) is called \(\sigma\)-stable if
\[
\sigma(I)\subseteq I.
\]
If \(I\) is \(\sigma\)-stable, then \(\sigma\) induces a morphic endomorphism
\[
\overline{\sigma}:R/I\longrightarrow R/I.
\]

If one wants the quotient map \(R\to R/I\) to preserve invariant identities, one usually requires the stronger condition
\[
\sigma^{-1}(I)=I.
\]
Then the quotient is a morphic system over the same invariant base.

Thus morphic quotients correspond to stable arithmetic reductions.

---

### 6.3 Morphic modules

Let \((R,\sigma)\) be a morphic ring. A **morphic module** over \((R,\sigma)\) is an \(R\)-module \(M\) equipped with an additive map
\[
T:M\longrightarrow M
\]
such that
\[
T(rm)=\sigma(r)T(m).
\]

This is the natural module-theoretic analogue of a semilinear evolution.

If \(M\) is finite free with basis \(e_A\), then
\[
T(e_B)=M^A{}_B e_A,
\]
and the matrix \(M^A{}_B\) is again the morphic transfer tensor.

---

### 6.4 Galois-compatible morphic systems

Let \(L/K\) be a Galois extension with group \(G=\operatorname{Gal}(L/K)\). Suppose \(X\) is defined over \(K\), and \(\Phi:X\to X\) is a \(K\)-morphism. Then for every \(\tau\in G\),
\[
\tau(\Phi(x))=\Phi(\tau(x)).
\]

Therefore morphic evolution commutes with Galois conjugation:
\[
\Phi^n(\tau(x))=\tau(\Phi^n(x)).
\]

In MNT, this means that the internal evolution of an algebraic number is compatible with the evolution of all its conjugates. The invariant identity is necessarily \(K\)-rational.

---

## 7. Computational Morphic Number Theory

### 7.1 Orbit computation in finite morphic systems

Let \(X\) be finite and \(\Phi:X\to X\) deterministic. Given \(x_0\), the orbit
\[
x_0,x_1,x_2,\dots
\]
eventually becomes periodic:
\[
x_{\mu+\lambda}=x_\mu.
\]

Floyd’s cycle-finding algorithm computes \(\mu\) and \(\lambda\) using constant memory. Brent’s algorithm often gives better practical performance.

If \(\pi:X\to S\) is an invariant, computation can be restricted to the fiber
\[
X_{\pi(x_0)}.
\]

For large finite fields, distinguished-point methods allow parallel orbit computation and collision detection.

---

### 7.2 Computing polynomial invariants

Let \(k\) be a field and let
\[
F:k^d\longrightarrow k^d
\]
be a polynomial map. We seek polynomials \(f\in k[x_1,\dots,x_d]\) such that
\[
f\circ F=f.
\]

For a fixed degree bound \(D\), write
\[
f=\sum_{|\alpha|\le D} c_\alpha x^\alpha.
\]
Then
\[
f\circ F-f
\]
is a polynomial whose coefficients are linear forms in the unknowns \(c_\alpha\). Solving the resulting linear system gives all invariants of degree at most \(D\).

**Algorithm: invariant computation up to degree \(D\)**

1. Choose basis monomials \(x^\alpha\) with \(|\alpha|\le D\).
2. Form the generic polynomial \(f=\sum c_\alpha x^\alpha\).
3. Compute \(f(F(x))-f(x)\).
4. Collect coefficients in \(x\).
5. Solve the linear equations forcing all coefficients to vanish.
6. Output a basis of the solution space.

If \(F\) has finite order \(m\) and \(\operatorname{char}k\nmid m\), the Reynolds operator
\[
\mathcal R(f)=\frac1m\sum_{j=0}^{m-1}f\circ F^j
\]
projects polynomials onto the invariant ring.

---

### 7.3 Linear morphic systems

If \(F(v)=Av\) is linear, then the action on homogeneous polynomial functions of degree \(r\) is given by
\[
\rho_r(A)=\operatorname{Sym}^r(A^*).
\]
The degree-\(r\) polynomial invariants are the fixed subspace
\[
\ker(\rho_r(A)-I).
\]

Thus invariant computation reduces to linear algebra on symmetric powers.

---

### 7.4 \(p\)-adic lifting of morphic fixed points

Let \(F:\mathbb Z_p^d\to\mathbb Z_p^d\) be an analytic morphic map. We seek fixed points
\[
F(x)=x.
\]
Define
\[
G(x)=F(x)-x.
\]
Suppose \(\overline{x}\in\mathbb F_p^d\) satisfies
\[
G(\overline{x})\equiv0\pmod p
\]
and
\[
\det JG(\overline{x})\not\equiv0\pmod p.
\]
Equivalently,
\[
\det(I-JF(\overline{x}))\not\equiv0\pmod p.
\]

By Hensel’s lemma, there exists a unique \(x\in\mathbb Z_p^d\) such that
\[
F(x)=x
\]
and
\[
x\equiv\overline{x}\pmod p.
\]

Newton iteration is given by
\[
x_{r+1}
=
x_r+
\left(I-JF(x_r)\right)^{-1}
\left(F(x_r)-x_r\right),
\]
with increasing \(p\)-adic precision.

If \(F\) preserves an invariant \(\pi\), then the lifted fixed point remains in the lifted invariant fiber.

---

## 8. Hard Morphic Problems and Cryptographic Applications

Morphic systems naturally generate computational problems that are candidates for cryptographic hardness.

### 8.1 The Morphic Orbit Problem

Let \((X/S,\Phi)\) be a morphic system over a finite arithmetic state space. The **Morphic Orbit Problem** is:

> Given \(x,y\in X_s\) in the same invariant fiber, find \(n\ge0\) such that
> \[
> y=\Phi^n(x),
> \]
> or decide that no such \(n\) exists.

If the evolution is generated by several commuting morphisms \(\Phi_1,\dots,\Phi_r\), the problem becomes finding an exponent vector
\[
a=(a_1,\dots,a_r)
\]
such that
\[
y=\Phi_1^{a_1}\cdots \Phi_r^{a_r}(x).
\]

This is a direct generalization of discrete logarithm problems.

---

### 8.2 Reduction from discrete logarithms

Let \(G=\langle g\rangle\) be a cyclic group of order \(N\). Suppose there is an injective morphic representation
\[
\iota:G\hookrightarrow X_s
\]
into an invariant fiber such that
\[
\Phi(\iota(h))=\iota(gh).
\]

Then an oracle solving the Morphic Orbit Problem for \((X_s,\Phi)\) solves the discrete logarithm problem in \(G\).

Indeed, given \(u=g^a\), query the oracle on
\[
\iota(e),\qquad \iota(u).
\]
The oracle returns \(a\) such that
\[
\iota(u)=\Phi^a(\iota(e))=\iota(g^a).
\]

Therefore MOP is at least as hard as discrete logarithm in any group that admits a faithful morphic action.

---

### 8.3 The Morphic Inversion Problem

The **Morphic Inversion Problem** asks:

> Given \(y\in X_s\), find \(x\in X_s\) such that
> \[
> \Phi(x)=y.
> \]

If \(\Phi\) is non-invertible publicly but invertible using secret structure, this yields a one-way function.

---

### 8.4 The Morphic Linearization Problem

Suppose a public morphic operator is given by conjugation:
\[
\Phi=PDP^{-1},
\]
where \(D\) is a simple operator and \(P\) is secret. The **Morphic Linearization Problem** asks to recover \(P\) or an equivalent conjugacy.

If \(P\) is known, orbit and inversion problems become easy in the \(D\)-basis. Without \(P\), the problem may be difficult.

---

### 8.5 Morphic Diffie–Hellman-type exchange

Let \(\Phi_1,\dots,\Phi_r\) be commuting morphic endomorphisms preserving \(\pi\):
\[
\pi\circ\Phi_i=\pi,
\qquad
\Phi_i\Phi_j=\Phi_j\Phi_i.
\]

Public data:
\[
(X/S,\Phi_1,\dots,\Phi_r,x_0).
\]

Alice chooses a secret vector \(a=(a_1,\dots,a_r)\) and publishes
\[
x_A=\Phi_1^{a_1}\cdots \Phi_r^{a_r}(x_0).
\]

Bob chooses \(b=(b_1,\dots,b_r)\) and publishes
\[
x_B=\Phi_1^{b_1}\cdots \Phi_r^{b_r}(x_0).
\]

Because the operators commute, both can compute the shared morphic state
\[
x_{AB}
=
\Phi_1^{a_1+b_1}\cdots \Phi_r^{a_r+b_r}(x_0).
\]

A cryptographic key can then be derived by applying a key-extraction function to \(x_{AB}\).

Security relies on the difficulty of recovering the secret exponent vectors from public morphic states.

---

### 8.6 Finite-field linear morphic cryptography

Let \(q\) be a prime power and let
\[
V=\mathbb F_q^d.
\]
Identify \(V\) with the field extension \(\mathbb F_{q^d}\). Let
\[
\alpha\in \mathbb F_{q^d}^\times
\]
with norm
\[
N_{\mathbb F_{q^d}/\mathbb F_q}(\alpha)=1.
\]
Define
\[
\Phi(v)=\alpha v.
\]

The norm
\[
Q(v)=N_{\mathbb F_{q^d}/\mathbb F_q}(v)
\]
is invariant:
\[
Q(\Phi(v))=N(\alpha v)=N(\alpha)N(v)=Q(v).
\]

Thus \(\Phi\) is a morphic evolution on each norm fiber.

Given nonzero \(v,w\) in the same norm fiber with
\[
w=\alpha^n v,
\]
recovering \(n\) is equivalent to solving
\[
\alpha^n=w/v
\]
in \(\mathbb F_{q^d}^\times\). This is a discrete logarithm problem.

This gives a simple and explicit morphic cryptographic instantiation.

---

### 8.7 Quadratic-order and class-group morphic systems

Let \(\mathcal O\) be a quadratic order and let
\[
N:\mathcal O\longrightarrow \mathbb Z
\]
be the norm. Let \(\varepsilon\in\mathcal O^\times\) be a unit of norm \(1\). Define
\[
\Phi(z)=\varepsilon z.
\]
Then
\[
N(\Phi(z))=N(\varepsilon)N(z)=N(z).
\]

The invariant identity is the norm value. The orbits are infinite in real quadratic orders and finite in imaginary quadratic orders.

More generally, class groups act on suitable arithmetic objects while preserving invariants such as endomorphism rings or discriminants. Morphic orbit problems in these settings generalize group-action problems used in isogeny-based and class-group-based cryptography.

---

## 9. Examples of Morphic Number Systems

### 9.1 Congruence-preserving integer evolution

Fix \(m\ge1\). Let
\[
X=\mathbb A^1_{\mathbb Z},\qquad B=\mathbb Z/m\mathbb Z,
\]
and let
\[
\pi(n)=n\bmod m.
\]
For any integer polynomial \(f\), define
\[
\Phi(n)=n+m f(n).
\]
Then
\[
\Phi(n)\equiv n\pmod m,
\]
so
\[
\pi(\Phi(n))=\pi(n).
\]

Thus every residue class modulo \(m\) is an invariant fiber. The morphic evolution changes the integer internally while preserving its congruence identity.

If \(p\mid m\), then over \(\mathbb Z_p\) the derivative is
\[
\Phi'(n)=1+m f'(n)\equiv1\pmod p,
\]
which is a unit. Hence \(\Phi\) is locally a \(p\)-adic automorphism on each residue class. This provides a rich family of invertible morphic systems on congruence fibers.

---

### 9.2 Norm-preserving evolution in quadratic orders

Let \(d\) be a squarefree integer and let
\[
\mathcal O=\mathbb Z[\sqrt d].
\]
Write an element as
\[
z=x+y\sqrt d.
\]
Its norm is
\[
N(z)=x^2-dy^2.
\]

Let
\[
\varepsilon=a+b\sqrt d
\]
be a unit of norm \(1\):
\[
a^2-db^2=1.
\]
Define
\[
\Phi(z)=\varepsilon z.
\]
In coordinates,
\[
\begin{pmatrix}
x'\\
y'
\end{pmatrix}
=
\begin{pmatrix}
a & db\\
b & a
\end{pmatrix}
\begin{pmatrix}
x\\
y
\end{pmatrix}.
\]

Let
\[
J=
\begin{pmatrix}
1&0\\
0&-d
\end{pmatrix}.
\]
The norm is the quadratic form
\[
Q(x,y)=
\begin{pmatrix}
x&y
\end{pmatrix}
J
\begin{pmatrix}
x\\
y
\end{pmatrix}.
\]

A direct calculation gives
\[
M^T J M=J,
\]
where
\[
M=
\begin{pmatrix}
a & db\\
b & a
\end{pmatrix}.
\]
Therefore
\[
Q(x',y')=Q(x,y),
\]
so the norm is an invariant identity.

This example is a concrete tensorial morphic system: the invariant tensor is \(J\), the state is the vector \((x,y)\), and the morphic transfer tensor is multiplication by a norm-one unit.

---

### 9.3 Finite orthogonal morphic systems

Let \(Q\) be a nondegenerate quadratic form over \(\mathbb F_q\), and let
\[
M\in O(Q)(\mathbb F_q).
\]
Define
\[
\Phi(v)=Mv.
\]
Then
\[
Q(\Phi(v))=Q(Mv)=Q(v).
\]

The fibers
\[
X_c=\{v\in\mathbb F_q^d:Q(v)=c\}
\]
are invariant identity fibers.

If \(M\) has large order and acts irreducibly, orbit computation becomes a discrete logarithm-type problem in a finite classical group.

---

### 9.4 Elliptic-curve torsion translations

Let \(E\) be an elliptic curve over a field \(K\), and let \(T\in E[n]\) be an \(n\)-torsion point. Define
\[
\Phi(P)=P+T.
\]
The map \(\Phi\) preserves many structural invariants, such as the curve and the Weil-pairing relations with torsion structures. If one fixes a level structure or an invariant base parameterizing the torsion configuration, translation by \(T\) becomes a morphic evolution preserving that identity.

This connects MNT to torsion dynamics, Galois representations, and isogeny-based constructions.

---

## 10. Morphic Factorization and Arithmetic Identity

In ordinary arithmetic, factorization expresses an integer as a product of primes. In MNT, one may instead study factorization through morphic decompositions.

Suppose a state space decomposes as
\[
X\cong Y\times_S Z
\]
over the invariant base \(S\), and suppose the morphic operator has the form
\[
\Phi=(\phi_Y,\operatorname{id}_Z).
\]
Then the \(Z\)-coordinate is an invariant identity, while the \(Y\)-coordinate evolves.

A **morphic factorization** of a state \(x\) is such a decomposition into:

1. an evolving component;
2. an invariant identity component;
3. a coupling structure relating them.

For example, in the quadratic-unit system above, the norm value is the invariant component, while the orbit under the unit group is the evolving component.

This suggests a new form of arithmetic decomposition:

> Instead of decomposing a number only into prime factors, decompose it into invariant identities and morphic orbits.

---

## 11. Open Problems

Morphic Number Theory raises many foundational and computational questions.

### Problem 11.1: Classification of invariant rings

Given a polynomial morphic system
\[
\Phi:\mathbb A^d\to\mathbb A^d,
\]
classify the invariant ring
\[
k[x_1,\dots,x_d]^\Phi.
\]
In particular, determine when it is finitely generated and when it separates fibers.

---

### Problem 11.2: Morphic heights for non-polarized systems

For polarized dynamics, canonical heights are well understood. A general theory of morphic heights for non-polarized or partially invariant systems remains to be developed.

---

### Problem 11.3: Morphic \(L\)-functions

Given a morphic system over a number field, can one attach an \(L\)-function to its invariant fibers and periodic-point structure? A natural starting point is the factorization
\[
\zeta_\Phi(t)=\prod_s \zeta_{\Phi,s}(t).
\]
Understanding the arithmetic meaning of these factors is a promising direction.

---

### Problem 11.4: Post-quantum morphic cryptography

Finite-field discrete-logarithm morphic systems are vulnerable to quantum algorithms. It is therefore important to construct morphic systems whose orbit problems remain hard against quantum adversaries. Candidate directions include:

- class-group actions;
- isogeny graphs;
- module-isomorphism-conjugated morphic maps;
- nonlinear \(p\)-adic morphic systems;
- lattice-compatible morphic operators.

---

### Problem 11.5: Morphic Galois theory

Given a morphic system over a number field, develop a Galois theory of invariant fibers, periodic points, and orbit fields. The basic object would be the field generated by an orbit:
\[
K(x,\Phi(x),\Phi^2(x),\dots).
\]
The invariant identity should correspond to a base field of definition, while the morphic evolution should induce arithmetic constraints on the associated Galois group.

---

## 12. Conclusion

Morphic Number Theory proposes a shift in the ontology of arithmetic objects. Numbers are no longer treated as static elements of rings or fields. They are treated as evolving arithmetic states whose identity is carried by invariants.

The fundamental structure is a morphic system over an invariant base:
\[
\pi:X\to B,\qquad \Phi:X\to X,\qquad \pi\circ\Phi=\pi.
\]
A morphic number is a pointed equivalence class in this setting. Its internal state evolves, while its invariant identity remains unchanged.

This framework unifies invariant theory, arithmetic dynamics, tensorial algebra, computational number theory, and cryptographic hardness. It provides a language for discussing the internal evolution of numbers and suggests new objects of study: morphic heights, morphic zeta functions, morphic factorizations, morphic rings, and morphic orbit problems.

The central claim of MNT is simple:

> Arithmetic identity is not absence of change, but persistence under change.

---

## References

1. M. Artin, B. Mazur, *On periodic points*, Annals of Mathematics, 1965.  
2. G. S. Call, J. H. Silverman, *Canonical heights on varieties with a morphism*, Compositio Mathematica, 1993.  
3. D. A. Cox, *Primes of the Form \(x^2+ny^2\)*, Wiley, 1989.  
4. J. H. Silverman, *The Arithmetic of Dynamical Systems*, Springer, 2007.  
5. J. H. Silverman, *Arithmetic of Dynamical Systems*, Graduate Texts in Mathematics, Springer, 2007.  
6. L. C. Washington, *Introduction to Cyclotomic Fields*, Springer, 1997.

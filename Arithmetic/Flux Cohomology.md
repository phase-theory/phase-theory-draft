# Flux Cohomology: A Bigraded Tensorial Theory of Curved Cochain Systems

**Preprint — Inaugural Exposition**  
**Date:** July 29, 2026  
**Mathematics Subject Classification:** 55Nxx, 58A10, 53C05, 18Gxx, 55Uxx  

---

## Abstract

This paper introduces **flux cohomology**, a new cohomological theory for graded linear systems equipped with a **curved differential**, i.e. a degree-raising operator \(D\) for which \(D^{2}\neq 0\). Classical cohomology requires \(d^{2}=0\); when this fails, the usual quotient \(\ker d/\operatorname{im}d\) is not defined because \(\operatorname{im}d\not\subseteq\ker d\). The central construction of the present theory replaces the failed differential by a canonical **curvature-depth filtration**
\[
F^{r}C^{p}=\ker\bigl(K^{r}:C^{p}\to C^{p+2r}\bigr),\qquad K:=D^{2},
\]
and extracts from it a bona fide bigraded cochain complex
\[
\operatorname{Gr}_{r}^{p}=F^{r+1}C^{p}/F^{r}C^{p},
\]
on which the induced differential squares to zero. The resulting groups
\[
H^{p,r}_{\Phi}(C):=H^{p}\bigl(\operatorname{Gr}_{r},d_{r}\bigr)
\]
are the **flux cohomology groups** of the curved system. They measure, simultaneously, cohomological information and the depth to which curvature obstructs flatness.

The paper develops the algebraic foundations of flux cohomology on weighted incidence complexes, proves a Bianchi identity, establishes a finite-dimensional Hodge decomposition on each curvature stratum, derives a depth-refined Euler index theorem, and formulates a smooth tensor calculus on **flux manifolds**. The theory is illustrated by explicit computations and is proposed as a general framework for non-conservative discrete geometry, curved gauge-type deformations, and curvature-filtered topological invariants.

---

## 1. Introduction

Classical cohomology theories rest on a single structural miracle: a differential \(d\) of degree \(+1\) satisfying \(d^{2}=0\). This condition converts the image of \(d\) into a subspace of its kernel and thereby makes the quotient
\[
H^{p}=\ker(d:C^{p}\to C^{p+1})/\operatorname{im}(d:C^{p-1}\to C^{p})
\]
meaningful. The condition \(d^{2}=0\) is not merely technical; it is the algebraic expression of conservativity, integrability, flatness, or absence of curvature.

Many natural mathematical objects, however, are governed by operators that almost behave like differentials but fail by a controlled curvature term. In such situations one has a graded space
\[
C=\bigoplus_{p=0}^{N}C^{p}
\]
and a degree \(+1\) operator
\[
D:C^{p}\to C^{p+1}
\]
for which
\[
D^{2}=K\neq 0.
\]
The operator \(K\) has degree \(+2\) and is naturally interpreted as a **curvature**. In this case \(\operatorname{im}D\not\subseteq\ker D\), so the ordinary cohomology of \(D\) is undefined. The standard response is to impose flatness, \(K=0\), or to pass to auxiliary constructions. The purpose of this paper is to introduce a systematic cohomological theory that does not discard the curved case but instead organizes it by the nilpotent action of curvature.

The central new idea is the following. Since \(K=D^{2}\), associativity gives
\[
DK=KD.
\]
This identity, the **flux Bianchi identity**, implies that the kernels of powers of \(K\) are preserved by \(D\). Therefore the filtration
\[
0=F^{0}C^{p}\subseteq F^{1}C^{p}\subseteq F^{2}C^{p}\subseteq\cdots\subseteq C^{p},
\qquad
F^{r}C^{p}:=\ker K^{r},
\]
is a \(D\)-filtration. On the associated graded object, the curvature becomes zero, and \(D\) descends to an honest differential. The cohomology of this associated graded complex is the new invariant proposed here.

The theory is called **flux cohomology** because the operator \(D\) is viewed as a background coboundary \(d_{0}\) deformed by a **flux tensor** \(\Phi\):
\[
D=d_{0}+\Phi.
\]
The curvature
\[
K=D^{2}=d_{0}\Phi+\Phi d_{0}+\Phi^{2}
\]
measures the failure of the flux to be conservative. The integer \(r\) in \(H^{p,r}_{\Phi}\) is called the **curvature depth**. Depth zero consists of modes annihilated by curvature; higher depths record modes that survive repeated exposure to curvature before being extinguished.

The main results of this inaugural paper are:

1. **Construction of flux cohomology** for curved cochain systems.
2. **Bianchi identity and curvature filtration theorem.**
3. **Hodge decomposition on each curvature stratum.**
4. **Depth-refined Euler characteristic and index formula.**
5. **Gauge invariance under degree-zero conjugations.**
6. **Smooth tensorial formulation on flux manifolds.**
7. **Explicit computations demonstrating depth shift and curvature filtering.**

The theory is deliberately developed in a form that is simultaneously algebraic, tensorial, and geometric. It applies to finite weighted incidence complexes, to discrete geometric networks, and, in the smooth limit, to manifolds equipped with curved first-order operators.

---

## 2. Weighted Incidence Complexes and Tensor Conventions

We work over a field \(\mathbb K\) of characteristic zero, usually \(\mathbb R\) or \(\mathbb C\). Let
\[
C=\bigoplus_{p=0}^{N}C^{p}
\]
be a finite-dimensional graded vector space. Elements of \(C^{p}\) are called \(p\)-cochains.

### 2.1 Abstract index notation

We use abstract indices \(A,B,C,\dots\) to denote basis-independent tensor components. If \(\alpha\in C^{p}\), we write \(\alpha^{A}\), with the understanding that \(A\) ranges over indices of degree \(p\). Repeated upper and lower indices are summed according to the Einstein convention.

A degree \(+1\) linear map \(T:C^{p}\to C^{p+1}\) is written
\[
(T\alpha)^{A}=T^{A}{}_{B}\alpha^{B},
\]
where \(T^{A}{}_{B}=0\) unless \(|A|=|B|+1\).

### 2.2 Weighted incidence coboundary

A **weighted incidence complex** consists of:

1. finite-dimensional graded spaces \(C^{p}\);
2. a degree \(+1\) coboundary tensor \(\delta^{A}{}_{B}\);
3. a positive definite weight tensor \(g^{(p)}_{A\bar B}\) on each \(C^{p}\),

such that
\[
\delta^{A}{}_{B}\delta^{B}{}_{C}=0.
\tag{2.1}
\]

The operator
\[
d_{0}:C^{p}\to C^{p+1},
\qquad
(d_{0}\alpha)^{A}=\delta^{A}{}_{B}\alpha^{B},
\]
is therefore a genuine cochain differential.

The inner product on \(C^{p}\) is
\[
\langle \alpha,\beta\rangle_{p}
=
g^{(p)}_{A\bar B}\alpha^{A}\overline{\beta^{B}}.
\]
For real diagonal weights \(w_{A}>0\), this reduces to
\[
\langle \alpha,\beta\rangle_{p}
=
\sum_{A\in I_{p}}w_{A}\alpha^{A}\beta^{A}.
\]

The weighted adjoint \(d_{0}^{\dagger}\) is defined by
\[
\langle d_{0}\alpha,\beta\rangle_{p+1}
=
\langle \alpha,d_{0}^{\dagger}\beta\rangle_{p}.
\]
In real diagonal weights,
\[
(d_{0}^{\dagger}\beta)^{B}
=
w_{B}^{-1}\delta^{A}{}_{B}w_{A}\beta^{A}.
\]

The ordinary cohomology of the incidence complex is
\[
H^{p}(C,d_{0})
=
\frac{\ker(d_{0}:C^{p}\to C^{p+1})}
{\operatorname{im}(d_{0}:C^{p-1}\to C^{p})}.
\]

---

## 3. Flux Differentials and Curvature

### 3.1 Flux tensor

A **flux tensor** is a degree \(+1\) tensor
\[
\Phi^{A}{}_{B}
\]
not necessarily satisfying any nilpotency condition. It defines a deformed differential
\[
D=d_{0}+\Phi,
\]
with components
\[
D^{A}{}_{B}
=
\delta^{A}{}_{B}
+
\Phi^{A}{}_{B}.
\tag{3.1}
\]

Unlike \(d_{0}\), the operator \(D\) need not square to zero.

### 3.2 Curvature tensor

The **curvature** of the flux differential is
\[
K:=D^{2}.
\]
In components,
\[
K^{A}{}_{C}
=
D^{A}{}_{B}D^{B}{}_{C}.
\tag{3.2}
\]
Expanding,
\[
K^{A}{}_{C}
=
\delta^{A}{}_{B}\Phi^{B}{}_{C}
+
\Phi^{A}{}_{B}\delta^{B}{}_{C}
+
\Phi^{A}{}_{B}\Phi^{B}{}_{C}.
\tag{3.3}
\]

The tensor \(K\) has degree \(+2\):
\[
K:C^{p}\to C^{p+2}.
\]

If \(K=0\), the flux is called **flat**, and \(D\) is an ordinary differential.

### 3.3 Flux Bianchi identity

The fundamental algebraic identity of flux theory is the following.

**Proposition 3.1 (Bianchi identity).**  
The curvature \(K=D^{2}\) satisfies
\[
DK=KD.
\tag{3.4}
\]

In components,
\[
D^{A}{}_{B}K^{B}{}_{C}
=
K^{A}{}_{B}D^{B}{}_{C}.
\]

**Proof.**  
By associativity of composition,
\[
D^{3}=D(D^{2})=(D^{2})D.
\]
Since \(K=D^{2}\), this is precisely
\[
DK=KD.
\]
Equivalently, the graded commutator vanishes:
\[
[D,K]=DK-(-1)^{|D||K|}KD=DK-KD=0,
\]
because \(|D|=1\) and \(|K|=2\). ∎

This identity is the algebraic source of the entire curvature filtration.

---

## 4. Curvature Filtration and Flux Cohomology

The failure of \(D^{2}=0\) prevents the formation of ordinary cohomology. The replacement is to filter by the nilpotent action of curvature.

### 4.1 Curvature-depth filtration

For each integer \(r\ge 0\), define
\[
F^{r}C^{p}
:=
\ker\bigl(K^{r}:C^{p}\to C^{p+2r}\bigr).
\tag{4.1}
\]
Here \(K^{0}=\operatorname{id}\), so
\[
F^{0}C^{p}=0.
\]
Because \(K\) raises degree by \(2\) and the complex is bounded, \(K^{m}=0\) for sufficiently large \(m\). Hence the filtration is exhaustive:
\[
0=F^{0}C^{p}\subseteq F^{1}C^{p}\subseteq F^{2}C^{p}\subseteq\cdots\subseteq C^{p}.
\]

The first nontrivial stratum
\[
F^{1}C^{p}=\ker K
\]
is the space of **curvature-blind** or **flat-sector** cochains.

### 4.2 Preservation by the flux differential

**Proposition 4.1.**  
For every \(r\ge 0\),
\[
D(F^{r}C^{p})\subseteq F^{r}C^{p+1}.
\]

**Proof.**  
Let \(\alpha\in F^{r}C^{p}\), so \(K^{r}\alpha=0\). Using the Bianchi identity,
\[
K^{r}D\alpha
=
DK^{r}\alpha
=
D0
=
0.
\]
Therefore \(D\alpha\in F^{r}C^{p+1}\). ∎

Thus \(D\) is a filtered operator of filtration degree \(0\).

### 4.3 Associated graded flux complex

Define the associated graded spaces
\[
\operatorname{Gr}_{r}^{p}
:=
F^{r+1}C^{p}/F^{r}C^{p}.
\tag{4.2}
\]
For a class \([\alpha]\in \operatorname{Gr}_{r}^{p}\), define
\[
d_{r}[\alpha]:=[D\alpha].
\tag{4.3}
\]

This is well-defined: if \(\alpha'=\alpha+\beta\) with \(\beta\in F^{r}C^{p}\), then \(D\beta\in F^{r}C^{p+1}\), so \([D\alpha']=[D\alpha]\).

Moreover,
\[
d_{r}^{2}[\alpha]
=
[D^{2}\alpha]
=
[K\alpha].
\]
If \(\alpha\in F^{r+1}C^{p}\), then \(K\alpha\in F^{r}C^{p+2}\), hence \([K\alpha]=0\). Therefore
\[
d_{r}^{2}=0.
\tag{4.4}
\]

Thus each curvature stratum carries an honest cochain complex
\[
\cdots
\longrightarrow
\operatorname{Gr}_{r}^{p-1}
\xrightarrow{d_{r}}
\operatorname{Gr}_{r}^{p}
\xrightarrow{d_{r}}
\operatorname{Gr}_{r}^{p+1}
\longrightarrow
\cdots.
\]

### 4.4 Flux cohomology groups

The **flux cohomology groups** of \((C,D)\) are
\[
H^{p,r}_{\Phi}(C)
:=
\frac{
\ker\bigl(d_{r}:\operatorname{Gr}_{r}^{p}\to\operatorname{Gr}_{r}^{p+1}\bigr)
}{
\operatorname{im}\bigl(d_{r}:\operatorname{Gr}_{r}^{p-1}\to\operatorname{Gr}_{r}^{p}\bigr)
}.
\tag{4.5}
\]

The integer \(p\) is the **cohomological degree**, and \(r\) is the **curvature depth**.

The total flux cohomology is the bigraded vector space
\[
H_{\Phi}^{\bullet,\bullet}(C)
:=
\bigoplus_{p,r}H^{p,r}_{\Phi}(C).
\]

### 4.5 Flux Poincaré polynomial

Define the **flux Poincaré polynomial**
\[
P_{\Phi}(u,v)
:=
\sum_{p,r}
\dim H^{p,r}_{\Phi}(C)\,u^{p}v^{r}.
\tag{4.6}
\]

The variable \(u\) records cohomological degree, while \(v\) records curvature depth.

### 4.6 Flat limit

If \(K=0\), then
\[
F^{1}C^{p}=C^{p},
\qquad
F^{r}C^{p}=C^{p}\quad(r\ge 1),
\]
and
\[
\operatorname{Gr}_{0}^{p}=C^{p},
\qquad
\operatorname{Gr}_{r}^{p}=0\quad(r\ge 1).
\]
Therefore
\[
H^{p,0}_{\Phi}(C)
=
\frac{\ker D}{\operatorname{im}D},
\]
and all higher-depth groups vanish. Flux cohomology thus contains ordinary cohomology of a flat differential as its depth-zero sector.

---

## 5. Hodge Theory on Curvature Strata

Assume now that \(\mathbb K=\mathbb C\) and that each \(C^{p}\) carries a Hermitian inner product. Each quotient \(\operatorname{Gr}_{r}^{p}\) inherits a quotient Hermitian metric.

Let
\[
d_{r}^{\dagger}:\operatorname{Gr}_{r}^{p+1}\to\operatorname{Gr}_{r}^{p}
\]
be the Hilbert-space adjoint of \(d_{r}\). Define the **depth-\(r\) flux Laplacian**
\[
\Delta_{r}
:=
d_{r}d_{r}^{\dagger}
+
d_{r}^{\dagger}d_{r}.
\tag{5.1}
\]

A class \([\alpha]\in\operatorname{Gr}_{r}^{p}\) is called **harmonic** if
\[
\Delta_{r}[\alpha]=0.
\]

### 5.1 Finite-dimensional Hodge decomposition

**Theorem 5.1 (Stratified Hodge decomposition).**  
For each \(r,p\),
\[
\operatorname{Gr}_{r}^{p}
=
\operatorname{im}d_{r}
\oplus
\operatorname{im}d_{r}^{\dagger}
\oplus
\ker\Delta_{r},
\tag{5.2}
\]
and the sum is orthogonal. Moreover,
\[
H^{p,r}_{\Phi}(C)
\cong
\ker\Delta_{r}\cap \operatorname{Gr}_{r}^{p}.
\tag{5.3}
\]

**Proof.**  
Since \(d_{r}^{2}=0\), the pair \((\operatorname{Gr}_{r},d_{r})\) is a finite-dimensional Hilbert cochain complex. The standard Hodge argument applies.

Let
\[
\mathcal H^{p}_{r}
:=
\ker(d_{r}:\operatorname{Gr}_{r}^{p}\to\operatorname{Gr}_{r}^{p+1})
\cap
\ker(d_{r}^{\dagger}:\operatorname{Gr}_{r}^{p}\to\operatorname{Gr}_{r}^{p-1}).
\]
If \(\alpha\in\ker d_{r}\), decompose \(\alpha=\beta+\gamma\) with \(\beta\in\operatorname{im}d_{r}\) and \(\gamma\perp\operatorname{im}d_{r}\). Then \(\gamma\in\ker d_{r}\), and for all \(\eta\),
\[
0=\langle \gamma,d_{r}\eta\rangle
=
\langle d_{r}^{\dagger}\gamma,\eta\rangle,
\]
so \(d_{r}^{\dagger}\gamma=0\). Thus \(\gamma\in\mathcal H^{p}_{r}\). Hence
\[
\ker d_{r}
=
\operatorname{im}d_{r}
\oplus
\mathcal H^{p}_{r}.
\]
Also,
\[
\operatorname{Gr}_{r}^{p}
=
\ker d_{r}
\oplus
\operatorname{im}d_{r}^{\dagger},
\]
because \((\ker d_{r})^{\perp}=\operatorname{im}d_{r}^{\dagger}\). Combining these gives the orthogonal decomposition. Finally,
\[
\ker\Delta_{r}
=
\ker d_{r}\cap\ker d_{r}^{\dagger}
=
\mathcal H^{p}_{r},
\]
and harmonic representatives are unique in each cohomology class. ∎

### 5.2 Heat supertrace

Define the depth-\(r\) heat supertrace
\[
Z_{r}(t)
:=
\sum_{p}(-1)^{p}
\operatorname{Tr}\bigl(e^{-t\Delta_{r}}\mid \operatorname{Gr}_{r}^{p}\bigr).
\tag{5.4}
\]
Then
\[
Z_{r}(t)
=
\sum_{p}(-1)^{p}\dim H^{p,r}_{\Phi}(C).
\tag{5.5}
\]

This is the finite-dimensional McKean–Singer-type identity for flux strata.

---

## 6. Index Theorems and Invariance Properties

### 6.1 Depth-refined Euler characteristic

For each depth \(r\), define
\[
\chi_{r}
:=
\sum_{p}(-1)^{p}\dim H^{p,r}_{\Phi}(C).
\tag{6.1}
\]

**Theorem 6.1 (Depth Euler formula).**  
For each \(r\),
\[
\chi_{r}
=
\sum_{p}(-1)^{p}\dim \operatorname{Gr}_{r}^{p}.
\tag{6.2}
\]

Consequently, the total flux Euler characteristic satisfies
\[
\chi_{\Phi}
:=
\sum_{r}\chi_{r}
=
\sum_{p}(-1)^{p}\dim C^{p}.
\tag{6.3}
\]

**Proof.**  
For any finite-dimensional cochain complex, the alternating sum of cohomology dimensions equals the alternating sum of chain-space dimensions. Applying this to \((\operatorname{Gr}_{r},d_{r})\) gives (6.2). Since the filtration is exhaustive,
\[
\sum_{r}\dim\operatorname{Gr}_{r}^{p}
=
\dim C^{p}.
\]
Summing with sign \((-1)^{p}\) gives (6.3). ∎

Thus the total Euler characteristic is unchanged by curvature, but curvature redistributes it among depths.

### 6.2 Refined polynomial index identity

Evaluating the flux Poincaré polynomial at \(u=-1\) gives
\[
P_{\Phi}(-1,v)
=
\sum_{r}\chi_{r}v^{r}.
\tag{6.4}
\]
Moreover,
\[
P_{\Phi}(-1,v)
=
\sum_{p}(-1)^{p}
\sum_{r}
v^{r}\dim\operatorname{Gr}_{r}^{p}.
\tag{6.5}
\]
At \(v=1\),
\[
P_{\Phi}(-1,1)
=
\sum_{p}(-1)^{p}\dim C^{p}.
\tag{6.6}
\]

This is the refined index theorem of flux cohomology.

### 6.3 Gauge invariance

Let \(U:C\to C\) be a degree-preserving automorphism, so
\[
U(C^{p})=C^{p}.
\]
Define a gauge-transformed flux differential
\[
D^{U}:=U^{-1}DU.
\tag{6.7}
\]
Then
\[
K^{U}
=
(D^{U})^{2}
=
U^{-1}KU.
\tag{6.8}
\]

**Theorem 6.2 (Gauge invariance).**  
For every \(p,r\),
\[
H^{p,r}_{\Phi}(C,D)
\cong
H^{p,r}_{\Phi}(C,D^{U}).
\]

**Proof.**  
Since
\[
(K^{U})^{r}=U^{-1}K^{r}U,
\]
the map \(U^{-1}\) sends \(F^{r}C^{p}\) isomorphically onto the corresponding filtered subspace for \(D^{U}\). It therefore induces isomorphisms
\[
\operatorname{Gr}_{r}^{p}(D)
\cong
\operatorname{Gr}_{r}^{p}(D^{U}).
\]
Moreover,
\[
d_{r}^{U}[U^{-1}\alpha]
=
[U^{-1}D\alpha],
\]
so the isomorphism commutes with the induced differentials. Hence the cohomology groups are isomorphic. ∎

### 6.4 Exact flux trivialization

Suppose there exists a degree-zero automorphism \(U\) such that
\[
D=U^{-1}d_{0}U.
\tag{6.9}
\]
Then \(K=0\), and \(D\) is flat.

**Theorem 6.3.**  
If \(D\) is gauge-equivalent to \(d_{0}\), then
\[
H^{p,0}_{\Phi}(C,D)
\cong
H^{p}(C,d_{0}),
\]
and
\[
H^{p,r}_{\Phi}(C,D)=0
\qquad
(r\ge 1).
\]

Thus exact fluxes produce no higher-depth cohomology.

### 6.5 Stability under constant-rank deformations

Let \(D_{s}=d_{0}+\Phi_{s}\) be a smooth family of flux differentials, with curvatures \(K_{s}=D_{s}^{2}\).

**Theorem 6.4 (Constant-rank stability).**  
If, in a neighborhood of \(s=s_{0}\), the ranks of all curvature powers \(K_{s}^{r}\) and all induced differentials \(d_{r,s}\) remain constant, then the flux Betti numbers
\[
\beta^{p,r}_{\Phi}(s)
:=
\dim H^{p,r}_{\Phi}(C,D_{s})
\]
are locally constant near \(s_{0}\).

This follows from elementary finite-dimensional linear algebra: constant rank implies constant kernel and image dimensions.

---

## 7. Smooth Tensor Calculus on Flux Manifolds

The algebraic theory admits a natural smooth tensorial formulation.

### 7.1 Flux manifolds

Let \(M\) be a smooth \(n\)-dimensional manifold, and let \(E\to M\) be a complex vector bundle with Hermitian metric. Let
\[
\Omega^{p}(M,E)
\]
denote \(E\)-valued \(p\)-forms.

A **smooth flux** is an \(\operatorname{End}(E)\)-valued one-form
\[
A\in \Omega^{1}(M,\operatorname{End}(E)).
\]
Define
\[
D=d+A\wedge,
\tag{7.1}
\]
so that for \(\alpha\in\Omega^{p}(M,E)\),
\[
D\alpha
=
d\alpha+A\wedge\alpha.
\]

In local coordinates and a local frame of \(E\), write
\[
\alpha^{a}
=
\alpha^{a}_{\mu_{1}\dots\mu_{p}}dx^{\mu_{1}}\wedge\cdots\wedge dx^{\mu_{p}},
\]
and
\[
A^{a}{}_{b}
=
A^{a}{}_{b\mu}dx^{\mu}.
\]
Then
\[
(D\alpha)^{a}{}_{\mu_{1}\dots\mu_{p+1}}
=
(p+1)
\partial_{[\mu_{1}}
\alpha^{a}{}_{\mu_{2}\dots\mu_{p+1}]}
+
(p+1)
A^{a}{}_{b[\mu_{1}}
\alpha^{b}{}_{\mu_{2}\dots\mu_{p+1}]}.
\tag{7.2}
\]

### 7.2 Smooth curvature tensor

The curvature is
\[
K=D^{2}=dA+A\wedge A.
\tag{7.3}
\]
In components,
\[
K^{a}{}_{b\mu\nu}
=
2\partial_{[\mu}A^{a}{}_{|b|\nu]}
+
2A^{a}{}_{c[\mu}A^{c}{}_{|b|\nu]}.
\tag{7.4}
\]

The Bianchi identity becomes
\[
D_{[\lambda}{}^{a}{}_{c}
K^{c}{}_{|b|\mu\nu]}
=
0.
\tag{7.5}
\]

### 7.3 Smooth curvature-depth filtration

Define wedge powers
\[
K^{\wedge r}
=
\underbrace{K\wedge\cdots\wedge K}_{r\text{ times}}.
\]
Since \(K\) has form degree \(2\), \(K^{\wedge r}\) has form degree \(2r\). For \(p+2r>n\), the map
\[
K^{\wedge r}:\Omega^{p}(M,E)\to\Omega^{p+2r}(M,E)
\]
vanishes for degree reasons.

Define
\[
\mathcal F^{r}\Omega^{p}(M,E)
:=
\ker\bigl(K^{\wedge r}:\Omega^{p}(M,E)\to\Omega^{p+2r}(M,E)\bigr).
\tag{7.6}
\]

By the Bianchi identity, \(D\) preserves this filtration. The associated graded sheaves
\[
\operatorname{Gr}_{r}^{p}
:=
\mathcal F^{r+1}\Omega^{p}/\mathcal F^{r}\Omega^{p}
\]
carry induced differentials \(d_{r}\) satisfying \(d_{r}^{2}=0\).

The smooth flux cohomology groups are
\[
\mathcal H^{p,r}_{A}(M,E)
:=
H^{p}\bigl(\Gamma(\operatorname{Gr}_{r}),d_{r}\bigr).
\tag{7.7}
\]

When the filtration has constant rank and the induced quotient complex is elliptic, each stratum admits a Hodge decomposition analogous to the finite-dimensional case.

---

## 8. Examples and Computations

### 8.1 A three-dimensional curved complex

Let
\[
C^{0}=\mathbb K\langle x\rangle,
\qquad
C^{1}=\mathbb K\langle e\rangle,
\qquad
C^{2}=\mathbb K\langle f\rangle.
\]
Let the background differential vanish:
\[
d_{0}=0.
\]
Define a flux by
\[
\Phi^{e}{}_{x}=b,
\qquad
\Phi^{f}{}_{e}=a,
\]
with all other components zero. Then
\[
Dx=be,
\qquad
De=af,
\qquad
Df=0.
\]

The curvature satisfies
\[
Kx=D^{2}x=abf,
\qquad
Ke=0,
\qquad
Kf=0.
\]
Thus
\[
K^{2}=0.
\]

Assume \(ab\neq 0\). Then
\[
F^{1}C^{0}=0,
\qquad
F^{1}C^{1}=C^{1},
\qquad
F^{1}C^{2}=C^{2}.
\]
Also
\[
F^{2}C^{p}=C^{p}.
\]

The depth-zero graded pieces are
\[
\operatorname{Gr}_{0}^{0}=0,
\qquad
\operatorname{Gr}_{0}^{1}=C^{1},
\qquad
\operatorname{Gr}_{0}^{2}=C^{2}.
\]
The induced differential satisfies
\[
d_{0}e=af.
\]
Since \(a\neq 0\),
\[
H^{1,0}_{\Phi}=0,
\qquad
H^{2,0}_{\Phi}=0.
\]

The depth-one graded pieces are
\[
\operatorname{Gr}_{1}^{0}=C^{0},
\qquad
\operatorname{Gr}_{1}^{1}=0,
\qquad
\operatorname{Gr}_{1}^{2}=0.
\]
Hence
\[
H^{0,1}_{\Phi}\cong\mathbb K.
\]

Thus the flux Poincaré polynomial is
\[
P_{\Phi}(u,v)=v.
\]

The class that would have appeared in degree zero in a flat theory has been shifted to curvature depth one.

### 8.2 Conservative graph flux

Let \(G=(V,E)\) be a finite oriented graph. Let
\[
C^{0}=\mathbb R^{V},
\qquad
C^{1}=\mathbb R^{E},
\]
and let \(d_{0}:C^{0}\to C^{1}\) be the usual incidence coboundary:
\[
(d_{0}f)_{ij}=f_{j}-f_{i}
\]
for an oriented edge \(i\to j\).

Let \(\psi:V\to\mathbb R\) be a vertex potential, and let \(U\) be the diagonal automorphism
\[
(Uf)_{i}=e^{\psi_{i}}f_{i}.
\]
Extend \(U\) to edges in any degree-preserving invertible manner. The conjugated differential
\[
D=U^{-1}d_{0}U
\]
has curvature
\[
K=D^{2}=0.
\]
Therefore the flux is flat, and
\[
H^{p,0}_{\Phi}(C,D)\cong H^{p}(C,d_{0}),
\qquad
H^{p,r}_{\Phi}(C,D)=0\quad(r\ge 1).
\]

This example shows that conservative fluxes merely reweight ordinary cohomology without generating higher depth.

### 8.3 Symplectic scalar flux on a smooth manifold

Let \(M=\mathbb R^{2m}\) with coordinates \((x^{1},\dots,x^{m},y^{1},\dots,y^{m})\), and let
\[
A=\frac12\sum_{i=1}^{m}(x^{i}dy^{i}-y^{i}dx^{i}).
\]
Then
\[
K=dA
=
\sum_{i=1}^{m}dx^{i}\wedge dy^{i}
=:\omega,
\]
the standard symplectic form.

The flux differential is
\[
D=d+A\wedge,
\]
and the curvature operator is
\[
K=\omega\wedge.
\]
The depth filtration is
\[
\mathcal F^{r}\Omega^{p}
=
\ker\bigl(\omega^{r}\wedge:\Omega^{p}\to\Omega^{p+2r}\bigr).
\]
This filtration is closely related to primitive-form theory, but the differential on the associated graded is not the ordinary de Rham differential; it is the curvature-projected flux differential \(d_{r}\). Thus flux cohomology produces a curvature-filtered refinement of primitive cohomological structures.

---

## 9. Conceptual Interpretation

Flux cohomology may be interpreted as a theory of **cohomology under non-conservative transport**.

In ordinary cohomology, a cocycle is a mode that is closed, and a coboundary is a mode that is exact. The condition \(d^{2}=0\) expresses that exact modes are automatically closed. In the presence of flux, this conservativity fails:
\[
D^{2}=K\neq 0.
\]
A mode may fail to be closed precisely because curvature acts on it.

The curvature-depth filtration separates modes according to how much curvature they can absorb before vanishing:

- **Depth \(0\):** modes annihilated by curvature.
- **Depth \(1\):** modes not annihilated by curvature, but annihilated by \(K^{2}\).
- **Depth \(r\):** modes annihilated by \(K^{r+1}\) but not by \(K^{r}\).

Thus \(r\) measures the curvature memory of a cohomological mode. The total theory does not ignore curvature; it stratifies cohomology by curvature persistence.

This is the central analytical framing of flux theory:

> **Curvature is not an obstruction to be removed, but a grading to be resolved.**

---

## 10. Applications and Research Program

The present paper establishes the foundational algebraic and geometric structure of flux cohomology. Several directions follow naturally.

### 10.1 Non-conservative networks

Weighted directed graphs often carry cycle affinities that cannot be represented by a global potential. Flux cohomology provides a depth-resolved invariant of such non-conservative transport.

### 10.2 Topological data analysis

Filtered simplicial and cubical complexes with asymmetric weights can be studied using flux differentials. The depth parameter supplies a new persistence coordinate: curvature persistence.

### 10.3 Discrete gauge theory

Flat discrete connections satisfy \(D^{2}=0\). Curved discrete connections do not. Flux cohomology gives a natural cohomological invariant of curved discrete gauge fields without requiring flatness.

### 10.4 Deformation theory

A deformation of a differential often produces a curved operator \(D=d+\Phi\) with \(D^{2}\neq 0\). Flux cohomology provides a systematic way to extract cohomological information from such curved deformations.

### 10.5 Smooth geometric analysis

On flux manifolds, the curvature-depth filtration interacts with Hodge theory, symplectic primitive forms, and gauge curvature. Elliptic flux complexes and analytic index theory constitute a natural next stage.

---

## 11. Conclusion

This paper has introduced flux cohomology as a new bigraded cohomological theory for curved cochain systems. Starting from a degree \(+1\) operator \(D\) with nonzero curvature \(K=D^{2}\), the theory constructs a canonical filtration by kernels of curvature powers and obtains an associated graded complex on which the induced differential squares to zero. The resulting groups \(H^{p,r}_{\Phi}\) are well-defined, gauge-invariant, Hodge-decomposable in finite dimensions, and governed by a depth-refined Euler index theorem.

The theory generalizes ordinary cohomology: flat fluxes recover standard cohomological structures, while curved fluxes generate higher-depth invariants. The smooth tensorial formulation shows that the same principles apply to manifolds equipped with curved first-order operators.

Flux cohomology is therefore proposed as a general framework for the study of non-conservative, curved, or irreversible cochain structures across algebra, geometry, and applied mathematics.

---

## Appendix A: Core Proofs

### A.1 Proof that \(D\) preserves the curvature filtration

Let \(\alpha\in F^{r}C^{p}\). Then \(K^{r}\alpha=0\). Since \(DK^{r}=K^{r}D\),
\[
K^{r}D\alpha
=
DK^{r}\alpha
=
0.
\]
Thus \(D\alpha\in F^{r}C^{p+1}\).

### A.2 Proof that the induced differential squares to zero

Let \([\alpha]\in\operatorname{Gr}_{r}^{p}\), with \(\alpha\in F^{r+1}C^{p}\). Then
\[
d_{r}^{2}[\alpha]
=
[D^{2}\alpha]
=
[K\alpha].
\]
Since \(\alpha\in F^{r+1}\), we have \(K^{r+1}\alpha=0\). Hence
\[
K^{r}(K\alpha)=K^{r+1}\alpha=0,
\]
so \(K\alpha\in F^{r}C^{p+2}\). Therefore \([K\alpha]=0\), and \(d_{r}^{2}=0\).

### A.3 Proof of the refined Euler identity

For each fixed \(r\), \((\operatorname{Gr}_{r},d_{r})\) is a finite cochain complex. Therefore
\[
\sum_{p}(-1)^{p}\dim H^{p}(\operatorname{Gr}_{r})
=
\sum_{p}(-1)^{p}\dim \operatorname{Gr}_{r}^{p}.
\]
By definition,
\[
H^{p}(\operatorname{Gr}_{r})=H^{p,r}_{\Phi}(C).
\]
Summing over \(r\) and using exhaustiveness of the filtration gives
\[
\sum_{r,p}(-1)^{p}\dim H^{p,r}_{\Phi}(C)
=
\sum_{p}(-1)^{p}\dim C^{p}.
\]

---

## Appendix B: Notation Summary

\[
\begin{aligned}
C &= \bigoplus_{p} C^{p} && \text{graded cochain space},\\
\delta^{A}{}_{B} &&& \text{background incidence coboundary},\\
\Phi^{A}{}_{B} &&& \text{flux tensor},\\
D^{A}{}_{B} &= \delta^{A}{}_{B}+\Phi^{A}{}_{B} && \text{flux differential},\\
K^{A}{}_{C} &= D^{A}{}_{B}D^{B}{}_{C} && \text{curvature tensor},\\
F^{r}C^{p} &= \ker K^{r} && \text{curvature-depth filtration},\\
\operatorname{Gr}_{r}^{p} &= F^{r+1}C^{p}/F^{r}C^{p} && \text{associated graded stratum},\\
d_{r} &&& \text{induced differential on }\operatorname{Gr}_{r},\\
H^{p,r}_{\Phi} &&& \text{flux cohomology},\\
P_{\Phi}(u,v) &&& \text{flux Poincaré polynomial},\\
\Delta_{r} &&& \text{depth-}r\text{ flux Laplacian}.
\end{aligned}
\]

---

## Final Remark

The defining principle of flux cohomology is that a curved differential is not a failed differential. It is a filtered differential whose curvature determines a canonical depth stratification. The passage
\[
D^{2}=K
\quad\longmapsto\quad
F^{r}=\ker K^{r}
\quad\longmapsto\quad
H^{p,r}_{\Phi}
\]
is the foundational operation of the theory.

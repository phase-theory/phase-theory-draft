# Stratified Number Theory  
## A Tensorial Arithmetic of Second-Order Integers

**Author:** Marlon Hanks  
Independent Researcher, Dust LLC  

**Preprint.**  

---

## Abstract

We introduce a new numbers theory: **stratified number theory**, the arithmetic of **second-order stratified integers**. A stratified integer is not merely a scalar but a triple  
\[
\mathfrak a=(a,u^i,T^{ij}),
\]
where \(a\in\mathbb Z\) is the scalar body, \(u^i\in\mathbb Z^d\) is a first-order vector stratum, and \(T^{ij}=T^{ji}\in\operatorname{Sym}^2(\mathbb Z^d)\) is a second-order symmetric tensor stratum. We define a closed addition and multiplication law under which the tensor strata interact through a symmetrized tensor product. The resulting structure
\[
\mathfrak S_d=\mathbb Z\oplus \mathbb Z^d\oplus \operatorname{Sym}^2(\mathbb Z^d)
\]
is a commutative unital ring with a nilpotent stratification ideal satisfying \(\mathcal N^3=0\). Ordinary integers embed as \((n,0,0)\), but the arithmetic of \(\mathfrak S_d\) is substantially richer: divisibility is governed by tensorial congruences, irreducibility is controlled not only by the scalar part but also by the \(p\)-adic primitivity of the vector stratum, and the prime spectrum is organized into **prime strata** rather than classical prime elements alone.

We develop the basic algebra of \(\mathfrak S_d\), prove explicit divisibility criteria, classify several families of irreducibles, analyze unit normal forms, and introduce a **principal stratified zeta function**. In rank one we compute the zeta function exactly:
\[
\zeta_{\mathfrak S_1}^{\mathrm{prin}}(s)
=
\frac{1}{1-2^{-s}}\,
\frac{\zeta(s-1)^2}{\zeta(s)},
\qquad \Re(s)>2.
\]
This establishes a self-contained arithmetic framework for tensor-carrying integers and opens a program for higher-order stratified number theory.

**Keywords:** stratified integers, tensor arithmetic, nilpotent number systems, divisibility, irreducibles, arithmetic zeta functions.

---

## 1. Introduction

Classical number theory treats integers as scalar objects. Even when one studies valuations, ideals, or factorization, the integer itself remains a single element of \(\mathbb Z\). This paper introduces a different foundational premise:

> A number may carry internal arithmetic strata, organized tensorially, and the arithmetic operations must act simultaneously on all strata.

The simplest nontrivial realization is the theory of **second-order stratified integers**. Such an integer has three layers:

1. a scalar body \(a\in\mathbb Z\);
2. a first-order vector stratum \(u^i\);
3. a second-order symmetric tensor stratum \(T^{ij}=T^{ji}\).

The multiplication law is designed so that the first-order strata interact to produce second-order strata, while all higher products truncate. This yields a finite, integral, purely algebraic number system with a well-defined divisibility theory.

The resulting objects are not “integers with decorations” in a passive sense. The tensor strata affect divisibility, irreducibility, unit equivalence, and analytic counting functions. For example, an element
\[
\mathfrak a=(p^2,u,T)
\]
with scalar part \(p^2\) may be irreducible if the vector stratum \(u\) is not divisible by \(p\), despite the composite scalar part. This phenomenon has no analogue in ordinary integer arithmetic.

The contributions of this paper are the following.

1. We define the ring \(\mathfrak S_d\) of second-order stratified integers.
2. We prove its fundamental algebraic properties: associativity, commutativity, unit group, nilradical, regular elements, and prime strata.
3. We derive explicit divisibility criteria in tensorial form.
4. We introduce and analyze stratified irreducibles, including scalar-prime, prime-power, and nilpotent irreducibles.
5. We define unit normal forms and compute the number of principal ideals of a given scalar norm.
6. We introduce the principal stratified zeta function and compute it exactly in rank one.

The paper is organized as follows. Section 2 constructs \(\mathfrak S_d\). Section 3 analyzes units, zero divisors, and prime strata. Section 4 develops divisibility. Section 5 treats irreducibility and factorization. Section 6 describes unit normal forms and principal ideals. Section 7 introduces the \(p\)-adic stratified completion. Section 8 defines and computes the principal stratified zeta function. Section 9 gives examples. Section 10 discusses extensions and future directions.

---

## 2. The Ring of Second-Order Stratified Integers

### 2.1. Basic objects

Fix an integer \(d\ge 1\). Let
\[
V=\mathbb Z^d
\]
be a free \(\mathbb Z\)-module with basis indexed by \(i=1,\dots,d\). Let
\[
\operatorname{Sym}^2(V)
\]
denote the module of symmetric contravariant rank-two tensors with integer components.

A **second-order stratified integer** is a triple
\[
\mathfrak a=(a,u^i,T^{ij}),
\]
where
\[
a\in\mathbb Z,\qquad u^i\in V,\qquad T^{ij}=T^{ji}\in\operatorname{Sym}^2(V).
\]

We denote the underlying set by
\[
\mathfrak S_d
=
\mathbb Z\oplus V\oplus \operatorname{Sym}^2(V).
\]

The scalar \(a\) is called the **body** of \(\mathfrak a\). The tensor \(u^i\) is the **first stratum**, and \(T^{ij}\) is the **second stratum**.

---

### 2.2. Addition

Addition is componentwise:
\[
(a,u^i,T^{ij})+(b,v^i,S^{ij})
=
(a+b,\;u^i+v^i,\;T^{ij}+S^{ij}).
\]

This makes \(\mathfrak S_d\) into a free abelian group of rank
\[
1+d+\frac{d(d+1)}2.
\]

---

### 2.3. Symmetrized tensor product

For \(u^i,v^i\in V\), define the symmetrized tensor product
\[
(u\odot v)^{ij}
=
u^i v^j+u^j v^i.
\]

This is a symmetric tensor:
\[
(u\odot v)^{ij}=(u\odot v)^{ji}.
\]

We deliberately use the unnormalized symmetrization. Thus, in rank one,
\[
u\odot v=2uv.
\]

---

### 2.4. Multiplication

Define multiplication by
\[
\boxed{
(a,u^i,T^{ij})(b,v^i,S^{ij})
=
\bigl(
ab,\;
a v^i+b u^i,\;
a S^{ij}+b T^{ij}+(u\odot v)^{ij}
\bigr).
}
\]

Explicitly,
\[
(a,u,T)(b,v,S)
=
\left(
ab,\;
a v^i+b u^i,\;
a S^{ij}+b T^{ij}+u^i v^j+u^j v^i
\right).
\]

The multiplicative identity is
\[
\mathbf 1=(1,0,0).
\]

The zero element is
\[
\mathbf 0=(0,0,0).
\]

Ordinary integers embed by
\[
n\longmapsto (n,0,0).
\]

---

### 2.5. Ring axioms

**Theorem 2.1.**  
\(\mathfrak S_d\) with the above addition and multiplication is a commutative unital ring.

**Proof.**  
Bilinearity of addition and multiplication follows directly from the formula. Commutativity is immediate because
\[
ab=ba,\qquad av^i+bu^i=bv^i+au^i,
\]
and
\[
u\odot v=v\odot u.
\]

It remains to check associativity. Let
\[
\mathfrak a=(a,u,T),\quad
\mathfrak b=(b,v,S),\quad
\mathfrak c=(c,w,R).
\]

The scalar part of both \((\mathfrak a\mathfrak b)\mathfrak c\) and \(\mathfrak a(\mathfrak b\mathfrak c)\) is \(abc\).

The first-stratum part of \((\mathfrak a\mathfrak b)\mathfrak c\) is
\[
(ab)w+c(av+bu)
=
abw+acv+bcu.
\]
The first-stratum part of \(\mathfrak a(\mathfrak b\mathfrak c)\) is
\[
a(bw+cv)+(bc)u
=
abw+acv+bcu.
\]

For the second-stratum part, \((\mathfrak a\mathfrak b)\mathfrak c\) gives
\[
abR+c(aS+bT+u\odot v)+(av+bu)\odot w,
\]
which expands to
\[
abR+acS+bcT+c(u\odot v)+a(v\odot w)+b(u\odot w).
\]

Similarly, \(\mathfrak a(\mathfrak b\mathfrak c)\) gives
\[
a(bR+cS+v\odot w)+bcT+u\odot(bw+cv),
\]
which expands to
\[
abR+acS+bcT+a(v\odot w)+b(u\odot w)+c(u\odot v).
\]

The two expressions coincide. Hence multiplication is associative. \(\square\)

---

### 2.6. Stratification ideal

Define the **stratification ideal**
\[
\mathcal N
=
\{(0,u^i,T^{ij})\}
=
0\oplus V\oplus \operatorname{Sym}^2(V).
\]

If \(\mathfrak n=(0,u,T)\), then
\[
\mathfrak n^2=(0,0,u\odot u),
\]
and
\[
\mathfrak n^3=0.
\]

Therefore
\[
\mathcal N^3=0.
\]

Thus \(\mathfrak S_d\) is a scalar extension of \(\mathbb Z\) by a square-cubed nilpotent tensor ideal.

---

## 3. Units, Regular Elements, and Prime Strata

### 3.1. Units

**Theorem 3.1.**  
An element
\[
\mathfrak a=(a,u,T)\in\mathfrak S_d
\]
is a unit if and only if
\[
a=\pm 1.
\]

When \(a=\pm1\), its inverse is
\[
\boxed{
\mathfrak a^{-1}
=
\left(
a^{-1},\;
-a^{-2}u^i,\;
-a^{-2}T^{ij}+a^{-3}(u\odot u)^{ij}
\right).
}
\]

**Proof.**  
If \(\mathfrak a\mathfrak b=\mathbf 1\), then the scalar parts satisfy \(ab=1\), hence \(a=\pm1\).

Conversely, suppose \(a=\pm1\). Let
\[
\mathfrak n=(0,u,T).
\]
Then
\[
\mathfrak a=a\mathbf 1+\mathfrak n,
\]
with \(\mathfrak n^3=0\). Therefore
\[
(a\mathbf 1+\mathfrak n)^{-1}
=
a^{-1}\mathbf 1-a^{-2}\mathfrak n+a^{-3}\mathfrak n^2.
\]

Since
\[
\mathfrak n^2=(0,0,u\odot u),
\]
the stated formula follows. \(\square\)

In rank one, writing an element as
\[
a+u\varepsilon+T\eta,
\]
with
\[
\varepsilon^2=2\eta,\qquad \varepsilon\eta=0,\qquad \eta^2=0,
\]
we have
\[
(1+u\varepsilon+T\eta)^{-1}
=
1-u\varepsilon+(2u^2-T)\eta.
\]

---

### 3.2. Zero divisors and regular elements

**Theorem 3.2.**  
An element \(\mathfrak a=(a,u,T)\) is a zero divisor if and only if \(a=0\). Equivalently, every element with nonzero scalar body is a non-zero-divisor.

**Proof.**  
If \(a=0\), then \(\mathfrak a\in\mathcal N\), and \(\mathcal N\) is nilpotent. Hence \(\mathfrak a\) is nilpotent and therefore a zero divisor.

Conversely, suppose \(a\neq0\) and
\[
(a,u,T)(b,v,S)=0.
\]
The scalar part gives \(ab=0\), hence \(b=0\). The first-stratum part gives
\[
a v^i=0,
\]
so \(v^i=0\). The second-stratum part gives
\[
a S^{ij}=0,
\]
so \(S^{ij}=0\). Thus the second factor is zero. Hence \(\mathfrak a\) is not a zero divisor. \(\square\)

We call elements with nonzero scalar body **regular stratified integers**.

---

### 3.3. Prime strata

Let
\[
\pi:\mathfrak S_d\to\mathbb Z
\]
be the scalar projection
\[
\pi(a,u,T)=a.
\]

Its kernel is \(\mathcal N\). Since \(\mathfrak S_d/\mathcal N\cong\mathbb Z\), and since \(\mathcal N\) is nilpotent, every prime ideal of \(\mathfrak S_d\) contains \(\mathcal N\).

**Theorem 3.3.**  
The prime ideals of \(\mathfrak S_d\) are precisely
\[
\mathfrak p_0=\mathcal N
\]
and
\[
\mathfrak p_p=\mathcal N+p\mathfrak S_d,
\]
where \(p\) ranges over the ordinary rational primes.

The residue fields are
\[
\mathfrak S_d/\mathfrak p_0\cong\mathbb Z,
\qquad
\mathfrak S_d/\mathfrak p_p\cong\mathbb F_p.
\]

**Proof.**  
Since \(\mathcal N\) is nilpotent, it is contained in every prime ideal. Prime ideals of \(\mathfrak S_d\) therefore correspond to prime ideals of \(\mathfrak S_d/\mathcal N\cong\mathbb Z\). The prime ideals of \(\mathbb Z\) are \((0)\) and \((p)\). Their preimages are \(\mathcal N\) and \(\mathcal N+p\mathfrak S_d\). \(\square\)

We call the ideals \(\mathfrak p_p\) the **prime strata**.

This shows that the classical theory of prime elements is not the correct primary language for \(\mathfrak S_d\). The nilpotent strata create prime ideals that are not naturally represented by ordinary scalar primes alone.

---

## 4. Divisibility in \(\mathfrak S_d\)

### 4.1. Divisibility criterion for regular elements

Let
\[
\mathfrak x=(a,u^i,T^{ij}),\qquad
\mathfrak y=(b,v^i,S^{ij}),
\]
with \(a\neq0\).

We say that \(\mathfrak x\) divides \(\mathfrak y\), written
\[
\mathfrak x\mid \mathfrak y,
\]
if there exists
\[
\mathfrak q=(c,w^i,R^{ij})
\]
such that
\[
\mathfrak x\mathfrak q=\mathfrak y.
\]

Multiplying gives the system
\[
ac=b,
\]
\[
a w^i+c u^i=v^i,
\]
\[
a R^{ij}+c T^{ij}+(u\odot w)^{ij}=S^{ij}.
\]

This proves the following theorem.

**Theorem 4.1.**  
Let \(\mathfrak x=(a,u,T)\) with \(a\neq0\). Then \(\mathfrak x\mid\mathfrak y=(b,v,S)\) if and only if the following three conditions hold.

1. Scalar divisibility:
   \[
   a\mid b.
   \]
   Let
   \[
   c=\frac ba\in\mathbb Z.
   \]

2. First-stratum congruence:
   \[
   v^i\equiv c u^i\pmod a
   \]
   for every \(i\). Define
   \[
   w^i=\frac{v^i-c u^i}{a}.
   \]

3. Second-stratum congruence:
   \[
   S^{ij}\equiv cT^{ij}+(u\odot w)^{ij}\pmod a
   \]
   for every \(i,j\).

When these conditions hold, a quotient is
\[
\mathfrak q=
\left(
c,\;
w^i,\;
\frac{S^{ij}-cT^{ij}-(u\odot w)^{ij}}{a}
\right).
\]

---

### 4.2. Consequences

The theorem shows that divisibility in \(\mathfrak S_d\) is not controlled by the scalar part alone. Even if \(a\mid b\), the vector and tensor strata must satisfy congruence conditions.

For ordinary integers embedded as \((a,0,0)\), the conditions reduce to ordinary divisibility:
\[
(a,0,0)\mid(b,0,0)
\iff
a\mid b.
\]

But for tensor-carrying elements, new obstructions appear.

For example, the scalar prime element
\[
p=(p,0,0)
\]
does not divide a pure first-stratum element
\[
\theta_i=(0,e_i,0)
\]
unless \(p\mid 1\), which is false. Nevertheless,
\[
p\mid 0=\theta_i^3,
\]
because \(\theta_i^3=0\). This illustrates why prime strata, rather than classical prime elements alone, are the natural objects.

---

### 4.3. Divisibility by nilpotent elements

Let
\[
\mathfrak x=(0,u,T).
\]
If
\[
\mathfrak q=(c,w,R),
\]
then
\[
\mathfrak x\mathfrak q=(0,c u^i,cT^{ij}+(u\odot w)^{ij}).
\]

Thus \(\mathfrak x\mid\mathfrak y=(b,v,S)\) if and only if

1. \(b=0\);
2. there exists \(c\in\mathbb Z\) such that
   \[
   v^i=c u^i;
   \]
3. there exists \(w^i\) such that
   \[
   S^{ij}=cT^{ij}+u^i w^j+u^j w^i.
   \]

Nilpotent divisibility is therefore governed by linear and tensorial decomposability conditions.

---

## 5. Irreducibility and Stratified Factorization

### 5.1. Definitions

A nonunit \(\mathfrak a\in\mathfrak S_d\) is called **irreducible** if whenever
\[
\mathfrak a=\mathfrak b\mathfrak c,
\]
either \(\mathfrak b\) or \(\mathfrak c\) is a unit.

Because the unit group is large, irreducibility is sensitive to the tensor strata.

---

### 5.2. Scalar-prime irreducibles

**Theorem 5.1.**  
Let
\[
\mathfrak a=(p,u,T)
\]
where \(p\) is an ordinary rational prime. Then \(\mathfrak a\) is irreducible.

**Proof.**  
Suppose
\[
\mathfrak a=\mathfrak b\mathfrak c.
\]
Let the scalar parts of \(\mathfrak b,\mathfrak c\) be \(r,s\in\mathbb Z\). Then
\[
rs=p.
\]
Thus one of \(r,s\) is \(\pm1\). The corresponding factor is a unit by Theorem 3.1. Hence \(\mathfrak a\) is irreducible. \(\square\)

Thus every tensorial lift of an ordinary prime is irreducible.

---

### 5.3. Composite scalar parts with distinct prime factors

**Theorem 5.2.**  
Let
\[
\mathfrak a=(a,u,T)
\]
with \(|a|>1\). If \(a\) is not a prime power, then \(\mathfrak a\) is reducible.

**Proof.**  
Since \(a\) is not a prime power, we may write
\[
a=bc
\]
with
\[
|b|>1,\quad |c|>1,\quad \gcd(b,c)=1.
\]

We seek a factorization
\[
\mathfrak a=(b,v,S)(c,w,R).
\]

The first-stratum equation is
\[
b w^i+c v^i=u^i.
\]
Because \(\gcd(b,c)=1\), this has integer solutions \(v^i,w^i\) for each \(i\).

The second-stratum equation is
\[
bR^{ij}+cS^{ij}
=
T^{ij}-(v\odot w)^{ij}.
\]
Again, since \(\gcd(b,c)=1\), this has integer solutions \(R^{ij},S^{ij}\).

Thus \(\mathfrak a\) factors into two nonunits. \(\square\)

Therefore, nontrivial irreducibles with nonzero scalar body must have scalar part equal to \(\pm p^e\) for some prime \(p\) and exponent \(e\ge1\).

---

### 5.4. Prime-power scalar parts and primitive vector strata

Let
\[
\mathfrak a=(p^e,u,T),
\]
with \(e\ge1\).

Define the \(p\)-adic valuation of the vector stratum by
\[
\nu_p(u)=\min_i \nu_p(u^i),
\]
with the convention \(\nu_p(0)=+\infty\).

**Theorem 5.3.**  
Let
\[
\mathfrak a=(\pm p^e,u,T)
\]
with \(e\ge2\). If
\[
\nu_p(u)=0,
\]
that is, at least one component of \(u\) is not divisible by \(p\), then \(\mathfrak a\) is irreducible.

**Proof.**  
Suppose
\[
\mathfrak a=\mathfrak b\mathfrak c
\]
with nonunits \(\mathfrak b,\mathfrak c\). Let the scalar parts be
\[
\pm p^r,\quad \pm p^{e-r},
\]
with \(1\le r\le e-1\).

The first-stratum equation has the form
\[
u^i=p^r w^i+p^{e-r}v^i.
\]
Both terms on the right are divisible by \(p\). Hence every \(u^i\) must be divisible by \(p\), contradicting \(\nu_p(u)=0\). Thus no such factorization exists. \(\square\)

This is a genuinely stratified phenomenon: a composite scalar part can be arithmetically protected by a primitive vector stratum.

---

### 5.5. A second-order factorization criterion

Let
\[
\mathfrak a=(p^2,u,T)
\]
and assume
\[
p\mid u^i
\]
for all \(i\). Define
\[
U^i=\frac{u^i}{p}\in\mathbb Z.
\]

We ask whether \(\mathfrak a\) factors as
\[
\mathfrak a=(p,v,S)(p,w,R).
\]

The first-stratum equation is
\[
p w^i+p v^i=u^i=pU^i,
\]
so
\[
w^i+v^i=U^i.
\]

The second-stratum equation is
\[
pR^{ij}+pS^{ij}+v^i w^j+v^j w^i=T^{ij}.
\]

Reducing modulo \(p\), we obtain the necessary and sufficient congruence
\[
T^{ij}\equiv v^i w^j+v^j w^i\pmod p.
\]
Using \(w^i=U^i-v^i\), we get the following corollary.

**Corollary 5.4.**  
Let
\[
\mathfrak a=(p^2,u,T)
\]
with \(p\mid u\). Put \(U=u/p\). Then \(\mathfrak a\) is reducible if and only if there exists a vector
\[
v^i\in\mathbb F_p^d
\]
such that
\[
\boxed{
T^{ij}\equiv
v^i(U^j-v^j)+v^j(U^i-v^i)
\pmod p.
}
\]

If no such \(v^i\) exists, then \(\mathfrak a\) is irreducible.

This gives a finite field criterion for the factorization of prime-square stratified integers.

---

### 5.6. Higher prime powers

For
\[
\mathfrak a=(p^e,u,T),\qquad e\ge3,
\]
assume again \(p\mid u\), and let \(U=u/p\). A factorization with first scalar factor \(p\),
\[
\mathfrak a=(p,v,S)(p^{e-1},w,R),
\]
requires
\[
w^i+p^{e-2}v^i=U^i.
\]

Modulo \(p\), this gives
\[
w^i\equiv U^i\pmod p
\]
for \(e\ge3\). The second-stratum equation reduces modulo \(p\) to
\[
T^{ij}\equiv v^iU^j+v^jU^i\pmod p.
\]

Thus a first-stratum factorization exists if and only if the reduction of \(T\) lies in the image of the linear map
\[
\phi_U:\mathbb F_p^d\to \operatorname{Sym}^2(\mathbb F_p^d),
\]
defined by
\[
\phi_U(v)^{ij}=v^iU^j+v^jU^i.
\]

This condition is only the first layer of a recursive factorization theory. Higher splits
\[
p^e=p^r p^{e-r}
\]
produce analogous congruences at deeper \(p\)-adic strata.

---

### 5.7. Nilpotent irreducibles

Elements with scalar body \(0\) also possess arithmetic significance.

Let
\[
\mathfrak n=(0,u,0).
\]

If the integer gcd of the components of \(u\) is \(1\), then \(\mathfrak n\) is irreducible. Indeed, any factorization
\[
(0,u,0)=\mathfrak b\mathfrak c
\]
with one factor having nonzero scalar body \(m\) would force \(m\mid u^i\) for all \(i\). If \(\gcd(u^i)=1\), then \(m=\pm1\), so that factor is a unit. If both scalar bodies vanish, the first-stratum part of the product is zero.

Thus primitive first-stratum nilpotents behave as stratified primes of a purely infinitesimal kind.

---

## 6. Unit Normal Forms and Principal Ideals

### 6.1. Unit action on regular elements

Let
\[
\mathfrak a=(a,u,T)
\]
with \(a>0\). Units with scalar body \(1\) have the form
\[
\mathfrak u=(1,\alpha^i,A^{ij}).
\]

Multiplication gives
\[
\mathfrak a\mathfrak u
=
\left(
a,\;
u^i+a\alpha^i,\;
T^{ij}+aA^{ij}+u^i\alpha^j+u^j\alpha^i
\right).
\]

Therefore, modulo \(a\), the first stratum is invariant:
\[
u^i\mapsto u^i+a\alpha^i.
\]

Thus the class
\[
\bar u^i\in(\mathbb Z/a\mathbb Z)^d
\]
is an invariant of the principal ideal \((\mathfrak a)\).

For fixed \(\bar u\), the second stratum transforms by
\[
T^{ij}\mapsto T^{ij}+u^i\alpha^j+u^j\alpha^i
\pmod a.
\]

Hence the remaining invariant is the class of \(T^{ij}\) in the cokernel of the map
\[
\phi_{u,a}:(\mathbb Z/a\mathbb Z)^d
\longrightarrow
\operatorname{Sym}^2(\mathbb Z/a\mathbb Z),
\]
defined by
\[
\phi_{u,a}(\alpha)^{ij}
=
u^i\alpha^j+u^j\alpha^i.
\]

---

### 6.2. Counting principal ideals of fixed norm

For a regular stratified integer \(\mathfrak a=(a,u,T)\), define its norm by
\[
N(\mathfrak a)=|a|.
\]

For a principal regular ideal \(I=(\mathfrak a)\), set
\[
N(I)=N(\mathfrak a).
\]

Two regular elements generate the same principal ideal if and only if they differ by a unit. Therefore the number of principal ideals of norm \(a>0\) is

\[
\boxed{
C_d(a)
=
\sum_{\bar u\in(\mathbb Z/a\mathbb Z)^d}
\left|
\operatorname{coker}\phi_{\bar u,a}
\right|.
}
\]

This formula will be the basis of the analytic theory.

---

## 7. \(p\)-Adic Stratified Integers

For each rational prime \(p\), define the \(p\)-adic completion
\[
\mathfrak S_{d,p}
=
\mathbb Z_p\oplus \mathbb Z_p^d\oplus \operatorname{Sym}^2(\mathbb Z_p^d),
\]
with the same multiplication law.

If
\[
\mathfrak a=(a,u,T)
\]
with \(p\nmid a\), then multiplication by \(\mathfrak a\) is an automorphism of \(\mathfrak S_{d,p}\). The inverse is given by the finite nilpotent expansion
\[
\mathfrak a^{-1}
=
a^{-1}\mathbf 1
-
a^{-2}(0,u,T)
+
a^{-3}(0,0,u\odot u).
\]

Thus the local arithmetic at \(p\) is especially simple away from the prime stratum \(\mathfrak p_p\). The nontrivial local theory occurs precisely at the prime strata, where the tensor congruences of Sections 4 and 5 govern lifting and factorization.

---

## 8. The Principal Stratified Zeta Function

### 8.1. Definition

Define the **principal stratified zeta function** of \(\mathfrak S_d\) by
\[
\zeta_{\mathfrak S_d}^{\mathrm{prin}}(s)
=
\sum_{I}
N(I)^{-s},
\]
where the sum ranges over all principal ideals generated by regular stratified integers.

Using the counting function \(C_d(a)\), we have
\[
\boxed{
\zeta_{\mathfrak S_d}^{\mathrm{prin}}(s)
=
\sum_{a=1}^{\infty}
\frac{C_d(a)}{a^s}.
}
\]

---

### 8.2. Multiplicativity

Because the Chinese remainder theorem gives
\[
\mathbb Z/ab\mathbb Z
\cong
\mathbb Z/a\mathbb Z
\times
\mathbb Z/b\mathbb Z
\]
for \(\gcd(a,b)=1\), the maps \(\phi_{u,a}\) decompose componentwise. Hence
\[
C_d(ab)=C_d(a)C_d(b)
\]
whenever \(\gcd(a,b)=1\).

Therefore
\[
\zeta_{\mathfrak S_d}^{\mathrm{prin}}(s)
=
\prod_p
Z_{d,p}(p^{-s}),
\]
where
\[
Z_{d,p}(X)
=
\sum_{e=0}^{\infty}
C_d(p^e)X^e.
\]

---

### 8.3. Exact rank-one computation

Now set \(d=1\). Then
\[
\operatorname{Sym}^2(\mathbb Z)=\mathbb Z,
\]
and
\[
u\odot v=2uv.
\]

For \(a\ge1\),
\[
C_1(a)
=
\sum_{u\bmod a}
\gcd(a,2u).
\]

Indeed, \(\phi_{u,a}\) is multiplication by \(2u\) on \(\mathbb Z/a\mathbb Z\), whose cokernel has size \(\gcd(a,2u)\).

---

### 8.4. Odd prime local factors

Let \(p\) be odd. For \(e\ge1\), classify \(u\bmod p^e\) by \(t=\nu_p(u)\), with \(0\le t\le e-1\), and also include \(u=0\).

For \(u=0\),
\[
\gcd(p^e,0)=p^e.
\]

For \(0\le t\le e-1\), the number of residues with exact valuation \(t\) is
\[
p^{e-t}-p^{e-t-1},
\]
and
\[
\gcd(p^e,2u)=p^t.
\]

Therefore
\[
C_1(p^e)
=
p^e+
\sum_{t=0}^{e-1}
\left(p^{e-t}-p^{e-t-1}\right)p^t.
\]

The summand simplifies:
\[
\left(p^{e-t}-p^{e-t-1}\right)p^t
=
p^e-p^{e-1}.
\]

There are \(e\) such terms, so
\[
\boxed{
C_1(p^e)
=
p^{e-1}\bigl((e+1)p-e\bigr),
\qquad p\ \text{odd},\ e\ge1.
}
\]

Also \(C_1(1)=1\).

Let \(X=p^{-s}\). Then
\[
Z_{1,p}(X)
=
\sum_{e=0}^{\infty}C_1(p^e)X^e.
\]

Using the formula above,
\[
Z_{1,p}(X)
=
1+
\sum_{e=1}^{\infty}
p^{e-1}\bigl((e+1)p-e\bigr)X^e.
\]

A direct summation yields
\[
\boxed{
Z_{1,p}(X)
=
\frac{1-X}{(1-pX)^2},
\qquad p\ \text{odd}.
}
\]

---

### 8.5. The dyadic local factor

For \(p=2\), one obtains similarly
\[
\boxed{
C_1(2^e)=(e+1)2^e.
}
\]

Hence
\[
Z_{1,2}(X)
=
\sum_{e=0}^{\infty}(e+1)(2X)^e
=
\boxed{
\frac{1}{(1-2X)^2}.
}
\]

---

### 8.6. Closed form of the rank-one zeta function

Combining the Euler factors, we obtain
\[
\zeta_{\mathfrak S_1}^{\mathrm{prin}}(s)
=
\frac{1}{(1-2^{1-s})^2}
\prod_{p\ \text{odd}}
\frac{1-p^{-s}}{(1-p^{1-s})^2}.
\]

Using
\[
\zeta(s)=\prod_p(1-p^{-s})^{-1},
\]
and
\[
\zeta(s-1)=\prod_p(1-p^{1-s})^{-1},
\]
we get
\[
\boxed{
\zeta_{\mathfrak S_1}^{\mathrm{prin}}(s)
=
\frac{1}{1-2^{-s}}
\frac{\zeta(s-1)^2}{\zeta(s)}.
}
\]

The Dirichlet series converges absolutely for
\[
\Re(s)>2.
\]

This gives an exact analytic invariant of the rank-one stratified number system.

---

### 8.7. First-order local counts in higher rank

For general \(d\), let
\[
r_2=\frac{d(d+1)}2.
\]

At a prime \(p\), the count \(C_d(p)\) can be computed from the rank of
\[
\phi_u:\mathbb F_p^d\to \operatorname{Sym}^2(\mathbb F_p^d),
\]
\[
\phi_u(v)^{ij}=u^iv^j+u^jv^i.
\]

If \(p\) is odd and \(u\neq0\), then \(\phi_u\) has rank \(d\). If \(u=0\), its rank is \(0\). Therefore
\[
\boxed{
C_d(p)
=
p^{r_2}
+
(p^d-1)p^{r_2-d},
\qquad p\ \text{odd}.
}
\]

For \(p=2\), the diagonal contribution vanishes in characteristic two, and for \(u\neq0\) the rank is \(d-1\). Thus
\[
\boxed{
C_d(2)
=
2^{r_2}
+
(2^d-1)2^{r_2-d+1}.
}
\]

These formulas provide the first nontrivial coefficients of the higher-rank Euler factors.

---

## 9. Examples

### 9.1. Rank one

Let \(d=1\). Write elements as
\[
(a,u,T).
\]

Multiplication is
\[
(a,u,T)(b,v,S)
=
(ab,\;av+bu,\;aS+bT+2uv).
\]

Let
\[
\varepsilon=(0,1,0),\qquad \eta=(0,0,1).
\]

Then
\[
\varepsilon^2=2\eta,\qquad \varepsilon\eta=0,\qquad \eta^2=0.
\]

Thus an element may be written formally as
\[
a+u\varepsilon+T\eta.
\]

The inverse of a unit with scalar body \(1\) is
\[
(1+u\varepsilon+T\eta)^{-1}
=
1-u\varepsilon+(2u^2-T)\eta.
\]

The element
\[
\mathfrak a=(4,1,0)
\]
is irreducible because its scalar part is \(2^2\) but its vector stratum is not divisible by \(2\).

By contrast,
\[
\mathfrak b=(4,2,0)
\]
is reducible:
\[
(4,2,0)=(2,0,0)(2,1,0).
\]

---

### 9.2. Rank two

Let \(d=2\). Consider
\[
\mathfrak a=(9,u,T),
\]
with
\[
u=(3,0).
\]

Since the scalar part is \(3^2\) and \(3\mid u\), we set
\[
U=(1,0).
\]

The reducibility criterion asks whether there exists
\[
v=(v_1,v_2)\in\mathbb F_3^2
\]
such that
\[
T^{ij}\equiv v^i(U^j-v^j)+v^j(U^i-v^i)\pmod 3.
\]

For example, if \(T=0\), we may choose \(v=(0,0)\), and \(\mathfrak a\) is reducible. If \(T\) is chosen outside the image of this quadratic map, then \(\mathfrak a\) is irreducible despite the scalar part being \(9\).

This illustrates how tensor strata create new arithmetic classes invisible to ordinary integer theory.

---

## 10. Discussion and Future Directions

The construction in this paper is only the second-order layer of a broader program.

### 10.1. Higher-order stratified integers

For any \(r\ge1\), one may define
\[
\mathfrak S_{d,r}
=
\bigoplus_{k=0}^{r}\operatorname{Sym}^k(\mathbb Z^d),
\]
with multiplication given by symmetrized tensor product and truncation above degree \(r\). The case \(r=2\) studied here is the first nontrivial member of this family.

Higher-order strata will produce deeper factorization congruences and richer zeta functions.

---

### 10.2. Ideal theory

The present paper focused on principal ideals generated by regular elements. A complete theory of ideals in \(\mathfrak S_d\) should include nonprincipal stratified ideals, primary decomposition, and a full ideal zeta function.

Because \(\mathfrak S_d\) is a finite free \(\mathbb Z\)-module, it is Noetherian, and its prime spectrum is a nilpotent thickening of \(\operatorname{Spec}\mathbb Z\). The arithmetic geometry of this thickening is a natural next step.

---

### 10.3. Analytic theory

The principal stratified zeta function computed here suggests the existence of a broader family of arithmetic generating functions:

1. full ideal zeta functions;
2. sublattice zeta functions;
3. stratified divisor functions;
4. \(L\)-functions attached to representations of \(\mathfrak S_d\).

The rank-one closed form
\[
\zeta_{\mathfrak S_1}^{\mathrm{prin}}(s)
=
\frac{1}{1-2^{-s}}
\frac{\zeta(s-1)^2}{\zeta(s)}
\]
indicates that these functions may have elegant meromorphic continuations.

---

### 10.4. Computational number theory

The divisibility and irreducibility criteria in this paper are algorithmic. For fixed \(d\), one can implement:

- stratified divisibility tests;
- stratified factorization search;
- local reducibility tests over \(\mathbb F_p\);
- enumeration of principal ideals by norm.

The tensor congruences may also be useful in constructing algebraically structured cryptographic primitives, though that direction is outside the scope of the present paper.

---

## 11. Conclusion

We have introduced a new numbers theory based on **second-order stratified integers**
\[
(a,u^i,T^{ij}).
\]
The arithmetic is governed by a commutative ring structure in which vector strata generate tensor strata through symmetrized multiplication. This produces a genuinely tensorial extension of integer arithmetic.

The theory differs from ordinary number theory in essential ways:

- divisibility requires tensorial congruences;
- irreducibility depends on \(p\)-adic primitivity of vector strata;
- prime structure is naturally expressed through prime strata rather than prime elements alone;
- principal ideal counting leads to new zeta functions.

The rank-one zeta function was computed exactly:
\[
\zeta_{\mathfrak S_1}^{\mathrm{prin}}(s)
=
\frac{1}{1-2^{-s}}
\frac{\zeta(s-1)^2}{\zeta(s)}.
\]

These results establish the foundations of stratified number theory and open a path toward higher-order tensorial arithmetic, stratified algebraic geometry, and analytic number theory over nilpotent scalar-tensor rings.

--- 

**Marlon Hanks**  
Independent Researcher  
Dust LLC

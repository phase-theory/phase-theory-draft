# Carry Field Theory: A Tensorial Number Theory of Propagative Arithmetic

**Preprint — Full White Paper Draft**

---

## Abstract

This paper introduces **Carry Field Theory (CFT)**, a new number-theoretic framework in which the primary arithmetic objects are not merely integers as elements of a ring, but **digit fields**, **carry fields**, and **carry tensors**. In CFT, ordinary base-\(b\) arithmetic is reinterpreted as a gauge-fixing process: integer values are equivalence classes of digit fields modulo a discrete carry differential, and the familiar carry operation becomes a propagating tensorial field. The theory yields:

1. a homological description of integers as carry-homology classes;
2. tensorial transition laws for addition and multiplication;
3. exact conservation laws relating digit sums, carry mass, and value;
4. a cohomological interpretation of the elementary carry as a fundamental 2-cocycle;
5. probabilistic carry laws and a natural carry charge;
6. a multiplicative carry calculus, including a carry-defect invariant for products;
7. new arithmetic invariants: carry weight, carry spectrum, resonance polynomials, and multiplicative carry atoms.

The paper develops the formal foundations, proves the central identities, and proposes a research program for a number theory built from arithmetic propagation rather than from factorization alone.

---

## 1. Introduction

Classical number theory has traditionally organized integers around three dominant structures:

\[
(\mathbb Z,+,\times),\qquad \text{prime factorization},\qquad \text{congruence classes}.
\]

These structures are extraordinarily powerful, but they largely suppress the internal representational dynamics of arithmetic. When integers are written in a radix \(b\), addition and multiplication are not instantaneous algebraic acts; they are **propagative processes**. Digits interact locally, and local overflows generate carries that travel through digit positions. Despite the centrality of this process, carries have usually been treated as computational artifacts rather than as primary number-theoretic objects.

Carry Field Theory reverses this hierarchy.

The central thesis of this paper is:

> **Carries are not accidental features of representation; they are the tensorial gauge fields that bind digit fields into integers.**

In CFT, an integer is not merely an element of \(\mathbb Z\). It is a **value class** of digit fields modulo a carry differential. Addition is the operation of adding digit fields and then re-gauging to the canonical digit slice. Multiplication is a convolution of digit fields followed by carry normalization. The carry field is the mediator between raw local digit interactions and globally canonical arithmetic.

This produces a genuinely new number-theoretic viewpoint. Instead of beginning with divisibility, CFT begins with **propagation**. Instead of treating base representation as secondary, CFT treats the base-\(b\) digit lattice as an arithmetic spacetime on which carry fields evolve.

The present paper establishes the formal foundations of this theory.

---

## 2. Digit Fields and the Carry Differential

Fix an integer base

\[
b\ge 2.
\]

Let \(\mathbb N_0=\{0,1,2,\dots\}\). A **digit field** is a finitely supported sequence

\[
x=(x_0,x_1,x_2,\dots),\qquad x_k\in\mathbb Z,
\]

not necessarily constrained to the canonical digit range. The index \(k\) is the digit position. Let

\[
\mathcal D_b=\bigoplus_{k\ge 0}\mathbb Z
\]

denote the abelian group of all such finitely supported integer digit fields.

The **value map** is

\[
V_b:\mathcal D_b\to \mathbb Z,
\qquad
V_b(x)=\sum_{k\ge 0}x_k b^k.
\]

The canonical digit set is

\[
I_b=\{0,1,\dots,b-1\}.
\]

A digit field \(r\in\mathcal D_b\) is called **canonical** if

\[
r_k\in I_b
\]

for all \(k\), and only finitely many \(r_k\) are nonzero. For every \(n\in\mathbb N_0\), there is a unique canonical digit field \(r(n)\) with

\[
V_b(r(n))=n.
\]

CFT treats the passage from arbitrary digit fields to canonical digit fields as a gauge-fixing process.

---

### 2.1 The carry differential

Let

\[
\mathcal C_b=\{c=(c_0,c_1,c_2,\dots)\in\bigoplus_{k\ge 0}\mathbb Z : c_0=0\}
\]

be the group of finitely supported carry fields with vanishing initial carry.

Define the **carry differential**

\[
\partial_b:\mathcal C_b\to \mathcal D_b
\]

by

\[
(\partial_b c)_k = b c_{k+1}-c_k.
\]

In indexed notation,

\[
(\partial_b)^k{}_j c^j
=
b\,\delta^k_{j+1}c^j-\delta^k_j c^j.
\]

This operator measures the change in a digit field induced by a carry field.

---

### Theorem 2.1 — Carry homology of the integer value

The value map induces an isomorphism

\[
\mathcal D_b/\partial_b\mathcal C_b \cong \mathbb Z.
\]

Equivalently, two digit fields represent the same integer if and only if they differ by a carry differential.

#### Proof

First observe that for any \(c\in\mathcal C_b\),

\[
V_b(\partial_b c)
=
\sum_{k\ge 0}(b c_{k+1}-c_k)b^k.
\]

Thus

\[
V_b(\partial_b c)
=
\sum_{k\ge 0}c_{k+1}b^{k+1}
-
\sum_{k\ge 0}c_k b^k.
\]

Since \(c\) is finitely supported and \(c_0=0\), this telescopes to \(0\). Hence

\[
\partial_b\mathcal C_b\subseteq \ker V_b.
\]

Conversely, suppose \(x\in\mathcal D_b\) and \(V_b(x)=0\). Define partial sums

\[
P_k=\sum_{j=0}^k x_j b^j.
\]

Since \(V_b(x)=0\),

\[
P_k=-\sum_{j=k+1}^\infty x_j b^j,
\]

and the right-hand side is divisible by \(b^{k+1}\). Therefore

\[
c_{k+1}:=\frac{P_k}{b^{k+1}}
\]

is an integer. Because \(x\) is finitely supported, \(c_{k}=0\) for sufficiently large \(k\). Also \(c_0=0\). Then

\[
b c_{k+1}-c_k
=
\frac{P_k}{b^k}-\frac{P_{k-1}}{b^k}
=
x_k.
\]

Thus \(x=\partial_b c\), so \(\ker V_b\subseteq \partial_b\mathcal C_b\). Therefore

\[
\ker V_b=\partial_b\mathcal C_b.
\]

Since \(V_b\) is surjective, the induced map

\[
\mathcal D_b/\partial_b\mathcal C_b\to \mathbb Z
\]

is an isomorphism. ∎

---

### Interpretation

The theorem says that an integer is a **carry-homology class** of digit fields. The carry differential generates all digit rewritings that preserve value. Canonical base-\(b\) expansion is a choice of gauge slice.

Thus:

\[
\boxed{
\text{Integers are value classes of digit fields modulo carry gauge transformations.}
}
\]

This is the first foundational principle of Carry Field Theory.

---

## 3. Addition as Carry Gauge Fixing

Let \(a,b\in\mathcal D_b\) be canonical digit fields representing integers \(m,n\in\mathbb N_0\). Their pointwise sum

\[
x_k=a_k+b_k
\]

need not be canonical. The sum \(m+n\) is obtained by finding the unique canonical field \(r\) and carry field \(c\) such that

\[
r = x-\partial_b c,
\]

or componentwise,

\[
r_k = a_k+b_k+c_k-bc_{k+1}.
\]

Equivalently,

\[
a_k+b_k+c_k = r_k + b c_{k+1}.
\]

With \(c_0=0\), this gives the usual recurrence

\[
r_k \equiv a_k+b_k+c_k \pmod b,
\]

\[
c_{k+1}=\left\lfloor \frac{a_k+b_k+c_k}{b}\right\rfloor.
\]

For addition of two canonical nonnegative integers, one has

\[
c_k\in\{0,1\}.
\]

Thus the carry field is a binary propagation field.

---

## 4. Tensorial Addition Law

It is useful to encode addition by a local transition tensor.

For two operands, let

\[
\alpha,\beta,\lambda\in I_b,
\qquad
r,q\in\{0,1\},
\]

where \(r\) is the incoming carry and \(q\) is the outgoing carry. Define the **carry transition tensor**

\[
T^{q\lambda}_{r\alpha\beta}
=
\delta^{q}_{\left\lfloor \frac{\alpha+\beta+r}{b}\right\rfloor}
\,
\delta^{\lambda}_{(\alpha+\beta+r)\bmod b}.
\]

Here \(\delta\) is the Kronecker delta.

This tensor maps an incoming carry state and two input digits to an outgoing carry state and an output digit.

For digit sequences \(a_k,b_k\), the full addition process is the tensor contraction

\[
R^{\lambda_0\cdots \lambda_{L-1}}
C^{q_L}
=
T^{q_1\lambda_0}_{0 a_0 b_0}
T^{q_2\lambda_1}_{q_1 a_1 b_1}
\cdots
T^{q_L\lambda_{L-1}}_{q_{L-1}a_{L-1}b_{L-1}}.
\]

The carry field is thus a one-dimensional tensor network propagating through digit positions.

For \(m\)-fold addition, introduce operand indices \(\mu=1,\dots,m\). Let

\[
A_k^\mu
\]

be the \(k\)-th digit of the \(\mu\)-th operand, and define

\[
\sigma_k=\sum_{\mu=1}^m A_k^\mu+c_k.
\]

The result digit and outgoing carry are

\[
R_k\equiv \sigma_k\pmod b,
\]

\[
c_{k+1}=\left\lfloor \frac{\sigma_k}{b}\right\rfloor.
\]

For \(m\) operands, the carry state satisfies

\[
0\le c_k\le m-1.
\]

The corresponding transition tensor is

\[
T^{q\lambda}_{r\alpha_1\cdots\alpha_m}
=
\delta^q_{\left\lfloor \frac{\alpha_1+\cdots+\alpha_m+r}{b}\right\rfloor}
\,
\delta^\lambda_{(\alpha_1+\cdots+\alpha_m+r)\bmod b}.
\]

This is the general additive carry tensor.

---

## 5. Carry Conservation Laws

Carry Field Theory possesses exact conservation identities. These are among its central results.

Let \(A^\mu\), \(\mu=1,\dots,m\), be canonical digit fields. Let \(R\) be the canonical result of their addition, and let \(c\) be the associated carry field.

Define the **carry mass**

\[
\tau_b(A^1,\dots,A^m)=\sum_{k\ge 1} c_k.
\]

For two operands, \(\tau_b\) counts the number of carries.

---

### Theorem 5.1 — Value current conservation

For any addition,

\[
\sum_{\mu=1}^m V_b(A^\mu)=V_b(R).
\]

More locally,

\[
\sum_{\mu=1}^m A_k^\mu
=
R_k+\partial_b c_k,
\]

where

\[
\partial_b c_k=bc_{k+1}-c_k.
\]

Multiplying by \(b^k\) and summing yields telescoping cancellation:

\[
\sum_{k\ge 0}(\partial_b c_k)b^k=0.
\]

Thus value is conserved.

---

### Theorem 5.2 — Digit-sum carry conservation

Let \(S_b(n)\) denote the base-\(b\) digit sum of \(n\). Then

\[
\sum_{\mu=1}^m S_b(V_b(A^\mu))
-
S_b(V_b(R))
=
(b-1)\sum_{k\ge 1}c_k.
\]

Equivalently,

\[
\boxed{
\sum_{\mu=1}^m S_b(n_\mu)
-
S_b\!\left(\sum_{\mu=1}^m n_\mu\right)
=
(b-1)\tau_b(n_1,\dots,n_m).
}
\]

#### Proof

From

\[
R_k=\sum_{\mu=1}^m A_k^\mu+c_k-bc_{k+1},
\]

we get

\[
\sum_{\mu=1}^m A_k^\mu-R_k
=
bc_{k+1}-c_k.
\]

Summing over \(k\),

\[
\sum_k\left(\sum_{\mu=1}^m A_k^\mu-R_k\right)
=
\sum_k(bc_{k+1}-c_k).
\]

Because \(c_0=0\) and \(c_k=0\) eventually,

\[
\sum_k(bc_{k+1}-c_k)
=
(b-1)\sum_{k\ge 1}c_k.
\]

The left-hand side is exactly the difference of digit sums. ∎

---

### Corollary 5.3 — First law of additive carry

For two integers \(m,n\),

\[
\tau_b(m,n)
=
\frac{S_b(m)+S_b(n)-S_b(m+n)}{b-1}.
\]

In particular, the right-hand side is always a nonnegative integer.

---

## 6. Carry Weight and Subadditivity

Define the **carry weight**

\[
Q_b(n)=\frac{S_b(n)}{b-1}.
\]

Then the first law becomes

\[
Q_b(m)+Q_b(n)
=
Q_b(m+n)+\tau_b(m,n).
\]

Since \(\tau_b(m,n)\ge 0\),

\[
Q_b(m+n)\le Q_b(m)+Q_b(n).
\]

Thus \(Q_b\) is a subadditive arithmetic weight on \(\mathbb N_0\).

Equality holds precisely when the addition \(m+n\) is carry-free.

This gives a new monotone in additive number theory. The quantity \(Q_b(n)\) measures the expected carry activity induced by \(n\), as shown below.

---

## 7. Carry Cohomology

The elementary carry also has a cohomological interpretation.

Let

\[
G_b=\mathbb Z/b\mathbb Z.
\]

Choose representatives \(0,1,\dots,b-1\). Define

\[
\gamma:G_b\times G_b\to \mathbb Z
\]

by

\[
\gamma(x,y)=\left\lfloor \frac{x+y}{b}\right\rfloor.
\]

Thus \(\gamma(x,y)=1\) if addition of the representatives overflows, and \(0\) otherwise.

---

### Theorem 7.1 — The fundamental carry cocycle

The function \(\gamma\) is a normalized group 2-cocycle:

\[
\gamma(x,y)+\gamma(x+y,z)
=
\gamma(y,z)+\gamma(x,y+z),
\]

where additions inside \(\gamma\) on the left and right are taken modulo \(b\).

#### Proof

Write

\[
x+y=b\gamma(x,y)+(x+y\bmod b).
\]

Then

\[
x+y+z
=
b\gamma(x,y)+(x+y\bmod b)+z.
\]

Reducing the last two terms gives

\[
x+y+z
=
b\left[\gamma(x,y)+\gamma(x+y\bmod b,z)\right]
+
(x+y+z\bmod b).
\]

By symmetry,

\[
x+y+z
=
b\left[\gamma(y,z)+\gamma(x,y+z\bmod b)\right]
+
(x+y+z\bmod b).
\]

Uniqueness of the quotient upon division by \(b\) gives the desired identity. Normalization is immediate:

\[
\gamma(0,x)=\gamma(x,0)=0.
\]

∎

---

### Theorem 7.2 — Nontriviality of the carry class

The cocycle \(\gamma\) defines the extension

\[
0\to \mathbb Z \xrightarrow{i} \mathbb Z \xrightarrow{\pi} G_b\to 0,
\]

where

\[
i(t)=bt,
\qquad
\pi(n)=n\bmod b.
\]

With the section \(s(x)=x\), the associated cocycle is precisely \(\gamma\). This extension does not split, because a splitting would embed the finite cyclic group \(G_b\) into the torsion-free group \(\mathbb Z\). Therefore the cohomology class

\[
[\gamma]\in H^2(G_b;\mathbb Z)
\]

is nontrivial.

---

### Interpretation

The ordinary carry is a cohomological obstruction to lifting modular digit addition to integer addition without propagation.

Thus:

\[
\boxed{
\text{The carry is a fundamental 2-cocycle of radix arithmetic.}
}
\]

Higher arithmetic operations generate higher carry tensors. For \(m\) digits, define

\[
\gamma^{(m)}(x_1,\dots,x_m)
=
\left\lfloor \frac{x_1+\cdots+x_m}{b}\right\rfloor.
\]

Associativity of addition imposes a family of higher coherence identities on these tensors. These identities define what may be called the **carry operad** of the base \(b\).

---

## 8. Probabilistic Carry Law

Let \(n\in\mathbb N_0\) have canonical digits

\[
n=\sum_{k\ge 0}a_k b^k,
\qquad
a_k\in I_b.
\]

Let \(M\) be a random \(b\)-adic integer whose digits \(U_k\) are independent and uniformly distributed in \(I_b\).

Consider adding \(n\) and \(M\). Let \(p_k\) be the probability that the incoming carry at position \(k\) equals \(1\). Thus \(p_0=0\).

Given incoming carry \(r\in\{0,1\}\), the outgoing carry at position \(k\) is \(1\) precisely when

\[
a_k+U_k+r\ge b.
\]

For fixed \(a_k\) and \(r\), the number of digits \(U_k\) causing this is

\[
a_k+r.
\]

Therefore

\[
\mathbb P(c_{k+1}=1\mid c_k=r)
=
\frac{a_k+r}{b}.
\]

Taking expectations gives

\[
p_{k+1}
=
\frac{a_k+p_k}{b}.
\]

---

### Theorem 8.1 — Carry probability theorem

For every \(k\ge 0\),

\[
p_k=\frac{n\bmod b^k}{b^k}.
\]

#### Proof

The result is true for \(k=0\). Suppose it holds for \(k\). Then

\[
p_{k+1}
=
\frac{a_k}{b}+\frac{p_k}{b}
=
\frac{a_k b^k+(n\bmod b^k)}{b^{k+1}}
=
\frac{n\bmod b^{k+1}}{b^{k+1}}.
\]

∎

---

### Corollary 8.2 — Expected finite-window carry mass

For addition modulo \(b^L\), the expected total carry mass is

\[
\mathbb E[\tau_{b,L}(n,M)]
=
\sum_{k=1}^L \frac{n\bmod b^k}{b^k}.
\]

---

### Corollary 8.3 — Infinite carry charge

The expected total carry mass over the full \(b\)-adic extension is

\[
Q_b(n)
=
\sum_{k\ge 1}\frac{n\bmod b^k}{b^k}.
\]

Moreover,

\[
\boxed{
Q_b(n)=\frac{S_b(n)}{b-1}.
}
\]

#### Proof

Write

\[
n=\sum_{j\ge 0}a_j b^j.
\]

For each \(k\),

\[
n\bmod b^k=\sum_{j=0}^{k-1}a_j b^j.
\]

Therefore

\[
\sum_{k\ge 1}\frac{n\bmod b^k}{b^k}
=
\sum_{k\ge 1}\sum_{j=0}^{k-1}a_j b^{j-k}.
\]

Interchanging sums,

\[
=
\sum_{j\ge 0}a_j\sum_{k>j}b^{j-k}
=
\sum_{j\ge 0}a_j\sum_{\ell\ge 1}b^{-\ell}
=
\frac{1}{b-1}\sum_{j\ge 0}a_j.
\]

Thus

\[
Q_b(n)=\frac{S_b(n)}{b-1}.
\]

∎

---

### Connection with classical \(p\)-adic valuation

For a prime \(p\), Legendre’s formula gives

\[
v_p(n!)=
\frac{n-S_p(n)}{p-1}.
\]

Using the additive carry formula,

\[
\tau_p(m,n)
=
\frac{S_p(m)+S_p(n)-S_p(m+n)}{p-1}.
\]

Hence

\[
\tau_p(m,n)
=
v_p((m+n)!)-v_p(m!)-v_p(n!)
=
v_p\binom{m+n}{m}.
\]

Thus in prime bases, the additive carry mass recovers the Kummer carry valuation. Carry Field Theory, however, extends this structure to arbitrary bases, multiplicative operations, tensor networks, and carry cohomology.

---

## 9. Carry Spectra and Resonance Polynomials

For fixed \(L\), define the **carry polynomial** of \(n\) in base \(b\) by

\[
P_{b,L}(n;t)
=
\sum_{m=0}^{b^L-1}t^{\tau_{b,L}(n,m)}.
\]

The coefficient of \(t^r\) counts the number of \(L\)-digit addends \(m\) for which adding \(n\) produces total carry mass \(r\).

This polynomial is a new finite-window invariant of \(n\).

---

### 9.1 Transfer-matrix representation

Let the digits of \(n\) be \(a_0,\dots,a_{L-1}\). Define the \(2\times 2\) carry transfer matrix

\[
M_a(t)
=
\begin{pmatrix}
b-a & a t\\[2mm]
b-a-1 & (a+1)t
\end{pmatrix}.
\]

Rows correspond to incoming carry \(r=0,1\); columns correspond to outgoing carry \(q=0,1\). The factor \(t\) records the production of an outgoing carry.

Then

\[
\boxed{
P_{b,L}(n;t)
=
\begin{pmatrix}1&0\end{pmatrix}
M_{a_0}(t)M_{a_1}(t)\cdots M_{a_{L-1}}(t)
\begin{pmatrix}1\\1\end{pmatrix}.
}
\]

At \(t=1\),

\[
P_{b,L}(n;1)=b^L.
\]

Moreover,

\[
\frac{P'_{b,L}(n;1)}{b^L}
=
\mathbb E[\tau_{b,L}(n,M)].
\]

Thus the carry polynomial refines the expected carry charge.

---

### 9.2 Flexible digits and carry completeness

For \(b\ge 3\), call a digit \(a\) **flexible** if

\[
1\le a\le b-2.
\]

For a flexible digit, all four carry transitions

\[
0\to 0,\quad 0\to 1,\quad 1\to 0,\quad 1\to 1
\]

are possible with positive multiplicity.

---

### Theorem 9.1 — Carry completeness

Let \(b\ge 3\). If

\[
a_k\in\{1,2,\dots,b-2\}
\]

for all \(0\le k<L\), then every binary carry sequence

\[
(c_1,\dots,c_L)\in\{0,1\}^L
\]

is realizable by some \(m\in[0,b^L-1]\). Consequently,

\[
\{\tau_{b,L}(n,m):0\le m<b^L\}
=
\{0,1,\dots,L\}.
\]

#### Proof

For a flexible digit \(a\), the transfer matrix entries at \(t=1\) are all positive:

\[
b-a>0,\quad a>0,\quad b-a-1>0,\quad a+1>0.
\]

Thus any prescribed transition \(r\to q\) can be achieved by a suitable choice of the corresponding digit of \(m\). Proceeding from \(k=0\) to \(L-1\), any desired carry sequence can be constructed. Since there exist carry sequences with exactly \(r\) ones for each \(0\le r\le L\), every carry mass in that range occurs. ∎

This theorem identifies a large class of integers whose additive carry behavior is maximally rich in a finite window.

---

## 10. Multiplicative Carry Geometry

Carry Field Theory also applies to multiplication.

Let \(x,y\in\mathbb N_0\) have canonical digit fields \(x_i\) and \(y_j\). Define the convolution tensor

\[
C^k{}_{ij}=\delta^k_{i+j}.
\]

The raw product digit field is

\[
q^k=C^k{}_{ij}x^i y^j
=
\sum_{i+j=k}x_i y_j.
\]

The field \(q\) is generally noncanonical. Multiplication is the canonicalization of \(q\).

Let \(c\) be the multiplicative carry field, with \(c_0=0\). The canonical product digits \(z_k\) satisfy

\[
z_k = q_k+c_k-bc_{k+1}.
\]

Equivalently,

\[
q_k+c_k=z_k+bc_{k+1}.
\]

The multiplicative carry field is typically not binary; \(c_k\) may be larger than \(1\).

---

### Theorem 10.1 — Multiplicative carry conservation

Let

\[
\mathrm T_b(x,y)=\sum_{k\ge 1}c_k
\]

be the total multiplicative carry mass. Then

\[
\boxed{
S_b(x)S_b(y)-S_b(xy)
=
(b-1)\mathrm T_b(x,y).
}
\]

#### Proof

The raw convolution satisfies

\[
\sum_{k\ge 0}q_k
=
\sum_{k\ge 0}\sum_{i+j=k}x_i y_j
=
\left(\sum_i x_i\right)\left(\sum_j y_j\right)
=
S_b(x)S_b(y).
\]

Canonicalization gives

\[
z_k=q_k+c_k-bc_{k+1}.
\]

Thus

\[
q_k-z_k=bc_{k+1}-c_k.
\]

Summing over \(k\),

\[
S_b(x)S_b(y)-S_b(xy)
=
\sum_k(q_k-z_k)
=
(b-1)\sum_{k\ge 1}c_k.
\]

∎

---

### Definition 10.2 — Multiplicative carry defect

Define

\[
\mathrm T_b(x,y)
=
\frac{S_b(x)S_b(y)-S_b(xy)}{b-1}.
\]

This is a nonnegative integer.

---

### Proposition 10.3 — Carry-free multiplication criterion

The multiplication \(x\cdot y\) is carry-free if and only if

\[
\mathrm T_b(x,y)=0.
\]

Equivalently,

\[
\sum_{i+j=k}x_i y_j < b
\]

for every \(k\).

#### Proof

If all convolution coefficients are less than \(b\), no carries occur, so \(c_k=0\) for all \(k\), and \(\mathrm T_b=0\). Conversely, if \(\mathrm T_b=0\), then since all carries are nonnegative, every \(c_k=0\). The recurrence then forces \(z_k=q_k\), and canonicality requires \(q_k<b\). ∎

---

### Multiplicative carry atoms

A number \(n>1\) is called a **multiplicative carry atom** in base \(b\) if it cannot be written as

\[
n=xy
\]

with \(x,y>1\) and

\[
\mathrm T_b(x,y)=0.
\]

In other words, every nontrivial factorization of \(n\) produces at least one multiplicative carry.

This gives a new arithmetic classification distinct from primality. For example, in base \(10\):

- \(6=2\cdot 3\) is carry-free, so \(6\) is not a multiplicative carry atom.
- \(9=3\cdot 3\) is carry-free, so \(9\) is not a multiplicative carry atom.
- \(10=2\cdot 5\) produces a carry, and no nontrivial carry-free factorization exists, so \(10\) is a multiplicative carry atom in base \(10\).

Thus multiplicative carry atoms form a new family of radix-dependent arithmetic objects.

---

## 11. Carry Gauge Theory and Curvature

The homological formalism allows a gauge-theoretic interpretation.

Given a digit field \(x\), a carry field \(c\), and a candidate canonical field \(r\), define the **carry curvature**

\[
\Omega_k(x,c,r)
=
x_k+c_k-r_k-bc_{k+1}.
\]

The field is **flat** if

\[
\Omega_k=0
\]

for all \(k\). Flatness is exactly the condition that \(r\) is the canonicalization of \(x\) under the carry field \(c\).

In this language:

- digit fields are sections of a discrete arithmetic bundle;
- carry fields are gauge potentials;
- canonical digits are gauge-fixed sections;
- curvature measures failure of canonicalization;
- integer value is the gauge-invariant observable.

The carry differential \(\partial_b\) plays the role of a discrete covariant derivative. The identity

\[
V_b(\partial_b c)=0
\]

is the corresponding gauge invariance.

---

## 12. Structural Invariants in Carry Field Theory

CFT introduces several new invariants.

### 12.1 Additive invariants

For \(n,m\in\mathbb N_0\):

1. **Carry mass**

   \[
   \tau_b(n,m)
   =
   \frac{S_b(n)+S_b(m)-S_b(n+m)}{b-1}.
   \]

2. **Carry weight**

   \[
   Q_b(n)=\frac{S_b(n)}{b-1}.
   \]

3. **Finite-window carry polynomial**

   \[
   P_{b,L}(n;t)
   =
   \sum_{m=0}^{b^L-1}t^{\tau_{b,L}(n,m)}.
   \]

4. **Carry spectrum**

   The multiset of coefficients of \(P_{b,L}(n;t)\).

---

### 12.2 Multiplicative invariants

For \(x,y\in\mathbb N_0\):

1. **Multiplicative carry mass**

   \[
   \mathrm T_b(x,y)
   =
   \frac{S_b(x)S_b(y)-S_b(xy)}{b-1}.
   \]

2. **Multiplicative carry efficiency**

   \[
   \eta_b(x,y)
   =
   \frac{S_b(xy)}{S_b(x)S_b(y)}
   =
   1-\frac{(b-1)\mathrm T_b(x,y)}{S_b(x)S_b(y)}.
   \]

   Here \(\eta_b(x,y)=1\) exactly when multiplication is carry-free.

3. **Multiplicative carry atoms**

   Integers with no nontrivial carry-free factorization.

---

### 12.3 Cohomological invariants

1. **Fundamental carry class**

   \[
   [\gamma_b]\in H^2(\mathbb Z/b\mathbb Z;\mathbb Z).
   \]

2. **Higher carry tensors**

   \[
   \gamma_b^{(m)}(x_1,\dots,x_m)
   =
   \left\lfloor \frac{x_1+\cdots+x_m}{b}\right\rfloor.
   \]

3. **Carry operad**

   The coherence system generated by all associativity constraints among carry tensors.

---

## 13. Research Program and Open Directions

Carry Field Theory suggests a broad research program.

### 13.1 Classification of carry polynomials

Given \(b\) and \(L\), determine the image of the map

\[
n\mapsto P_{b,L}(n;t).
\]

In particular:

- Which polynomials arise?
- When do two integers have the same carry polynomial?
- How do carry polynomials behave under addition and multiplication?

---

### 13.2 Multiplicative carry atoms

Study the set

\[
\mathcal A_b
=
\{n>1:\text{ no nontrivial carry-free factorization in base }b\}.
\]

Basic questions:

1. Is \(\mathcal A_b\) infinite for every \(b\ge 2\)?
2. What is the density of \(\mathcal A_b\)?
3. How do multiplicative carry atoms relate to ordinary primes?
4. Are there bases in which \(\mathcal A_b\) has a simple characterization?

---

### 13.3 Carry zeta functions

Define the carry-weighted Dirichlet series

\[
\zeta_b^{\mathrm{car}}(s)
=
\sum_{n\ge 1}\frac{e^{-Q_b(n)}}{n^s}.
\]

Since \(Q_b(n)\sim \frac{1}{2}\log_b n\) on average, this series defines a new analytic object. Questions include:

- domain of convergence;
- meromorphic continuation;
- pole structure;
- relation to automatic sequences and Mahler functions.

More generally, one may define

\[
Z_b(x,t)
=
\sum_{n\ge 0}x^n t^{S_b(n)}
=
\prod_{k\ge 0}
\left(
1+t x^{b^k}+t^2 x^{2b^k}+\cdots+t^{b-1}x^{(b-1)b^k}
\right).
\]

This is the partition function of carry charge.

---

### 13.4 Carry cohomology operations

The fundamental carry class \([\gamma_b]\) should generate further operations. Possible directions include:

- higher cup products of carry classes;
- extensions to \(b\)-adic integer groups;
- carry cohomology for nonstandard digit sets;
- relations with formal group laws.

---

### 13.5 Carry geometry over negative integers

The present paper focused primarily on \(\mathbb N_0\). A complete theory over \(\mathbb Z\) requires choosing a symmetric digit gauge, for example balanced digits, or working with \(b\)-adic completions. The homological theorem extends naturally, but the canonical gauge requires additional conventions. Developing the signed and \(b\)-adic theories is a natural next step.

---

## 14. Conclusion

Carry Field Theory reframes number theory around the dynamics of arithmetic propagation. Its central principles are:

1. **Digit fields are primary variables.**
2. **Carry fields are gauge fields.**
3. **Integers are carry-homology classes.**
4. **Addition and multiplication are canonicalization processes.**
5. **Carry mass is an exact arithmetic defect.**
6. **The elementary carry is a cohomological cocycle.**
7. **Multiplication possesses its own carry geometry.**

The theory produces new invariants and new arithmetic objects: carry weight, carry polynomials, carry spectra, multiplicative carry defects, and multiplicative carry atoms. It also recovers known phenomena, such as Kummer’s carries in prime bases, as special shadows of a broader tensorial structure.

The present paper establishes the axiomatic and theorem-proving core of the subject. The resulting framework opens a new branch of number theory in which the propagation of arithmetic information, rather than static divisibility alone, becomes the central object of study.

---

## References

1. E. E. Kummer, *Über die Ergänzungssätze zu den allgemeinen Reciprocitätsgesetzen*, Journal für die reine und angewandte Mathematik **44** (1852).  
2. K. S. Brown, *Cohomology of Groups*, Springer, 1982.  
3. G. H. Hardy and E. M. Wright, *An Introduction to the Theory of Numbers*, 6th ed., Oxford University Press, 2008.

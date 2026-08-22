---
title: "Carry-Spectral Arithmetic: A Finite-State Theory of Digit-Resolved Integer Interactions"
author: "Marlon Hanks"
affiliation: "Independent Researcher, Dust LLC"
date: "22 August 2026"
status: "Research preprint"
---

# Carry-Spectral Arithmetic: A Finite-State Theory of Digit-Resolved Integer Interactions

**Marlon Hanks**  
*Independent Researcher, Dust LLC*  
**Research preprint — 22 August 2026**

> **Abstract.** This paper introduces **carry-spectral arithmetic**, a representation-sensitive enrichment of positive-integer arithmetic. For every radix \(b\ge 2\), an integer \(n\) is assigned a \((b-1)\)-component carry spectrum \(\Lambda_b(n)\). Its \(j\)-th component counts the weighted carries created when \(n\) is added to \(jn\). The central conservation theorem proves that the total spectral mass is exactly the base-\(b\) digit sum: \(\mathbf 1^\top\Lambda_b(n)=s_b(n)\). This identity supplies a canonical decomposition of a familiar scalar digit invariant into a finite carry-state field. We develop an associated tensor package, additive interaction tensor, factor defect, correlation kernel, and a hierarchy of carry classes. Exact theorems establish radial invariance under \(n\mapsto bn\), a componentwise interaction law, and a factorization-defect decomposition. The paper closes with explicit examples, an algorithmic procedure, and falsifiable conjectures concerning primes, spectrum collisions, and multiplicative carry defects. The construction is not a replacement for ordinary integer arithmetic: it is a new state-theoretic layer placed over it.

| Classification | Value |
|---|---|
| Primary objects | Positive integers equipped with base-\(b\) carry spectra |
| Primitive operation | Digitwise carrying under \(jn+n\) for \(1\le j<b\) |
| Fundamental invariant | \(\mathbf 1^\top\Lambda_b(n)=s_b(n)\) |
| Main exact results | Conservation, scale invariance, additive trace law, factor-defect decomposition |
| Principal open direction | Distribution of spectra and defects on primes and factorizations |

**Keywords.** positional arithmetic; digit sums; carry processes; integer factorization; finite-state invariants; arithmetic tensors.

**Mathematics Subject Classification (2020).** 11A63, 11A67, 11B85, 68Q45.

---

## 1. Introduction and conceptual position

Classical arithmetic treats an integer \(n\) as independent of a particular numeral representation, except when a representation is used as a computational device. Carry-spectral arithmetic takes the opposite operational stance: a positional representation is not discarded after evaluation, but is retained as a finite state field that records how \(n\) reacts to a prescribed family of self-additions. The objective is to extract structure from the motion of carries rather than from the numerical value alone.

The proposed structure is deliberately narrower than a new ordered field and deliberately richer than a digit sum. It does not seek to enlarge the universe of numbers, as do comprehensive ordered-field constructions such as Conway’s surreal numbers [1]. Nor is it a congruence-restricted multiplicative submonoid, as in the theory of arithmetic congruence monoids [2]. Instead, it is an **arithmetic enrichment of \(\mathbb N_{>0}\)**: each integer receives a finite vector of base-dependent carry observables.

Carrying itself is a classical object. In particular, the carry digit function has been interpreted cohomologically as a 2-cocycle [3]. The contribution proposed here is different in kind: it packages the entire self-addition family

\[
 n+n,\; 2n+n,\;\ldots,\;(b-1)n+n
\]

into a single vector \(\Lambda_b(n)\), proves an exact conservation law for that vector, and uses vector differences to define new additive and multiplicative diagnostics. The resulting framework has no claim to alter the truth of ordinary arithmetic. Its claim is that it exposes a structured, finite-state geometry that ordinary arithmetic leaves implicit.

> **Scope statement.** The definitions and proofs in this paper are self-contained. The theory is presented as a newly formulated framework, while a global claim of historical uniqueness would require a broader specialist literature review than any single preprint can supply. Statements explicitly marked *Conjecture* are not theorems.

The remainder of the paper is organized as follows. Section 2 fixes notation and derives the carry-weight identity. Section 3 defines the carry spectrum and proves the conservation and scale theorems. Section 4 supplies a tensorial representation. Sections 5 and 6 develop additive interaction and multiplicative factor defects. Section 7 provides explicit examples and an algorithm. Sections 8 and 9 state classifications, conjectures, and a research program.

---

## 2. Positional notation and the carry weight

Fix an integer base \(b\ge 2\). Every \(n\in\mathbb N_0\) has a unique finite expansion

\[
 n=\sum_{r\ge 0} d_r(n)b^r,\qquad d_r(n)\in\{0,1,\ldots,b-1\},
\tag{2.1}
\]

where all but finitely many digits vanish. Write

\[
 \mathbf d_b(n):=(d_0(n),d_1(n),\ldots)^\top\in\mathbb N_0^{(\mathbb N_0)}
\tag{2.2}
\]

for the zero-padded digit column, and define the digit sum

\[
 s_b(n):=\sum_{r\ge0}d_r(n).
\tag{2.3}
\]

The superscript-free symbol \(s_b\) always denotes the ordinary base-\(b\) digit sum, not a newly introduced operation.

### Definition 2.1 (carry chain and carry weight)

Let \(x,y\in\mathbb N_0\). In the usual base-\(b\) addition of \(x\) and \(y\), let \(\kappa_r(x,y)\in\{0,1\}\) be the carry from column \(r\) to column \(r+1\), with \(\kappa_{-1}=0\), and continue the zero-padded addition until the terminal carry is zero. The **carry weight** is

\[
 c_b(x,y):=\sum_{r\ge0}\kappa_r(x,y).
\tag{2.4}
\]

Thus \(c_b(x,y)\) counts carries with multiplicity over columns. It is symmetric in \(x,y\), nonnegative, and depends on the selected base.

### Lemma 2.2 (digit-sum carry identity)

For all \(x,y\in\mathbb N_0\),

\[
 s_b(x)+s_b(y)-s_b(x+y)=(b-1)c_b(x,y).
\tag{2.5}
\]

#### Proof

Let \(x_r,y_r,z_r\) be the digits of \(x,y,z=x+y\), respectively. Columnwise addition gives

\[
 x_r+y_r+\kappa_{r-1}=z_r+b\kappa_r.
\tag{2.6}
\]

Rearranging and summing over all columns, including the finitely many terminal zero columns required to make \(\kappa_r=0\) at the end, yields

\[
\begin{aligned}
 s_b(x)+s_b(y)-s_b(x+y)
 &=\sum_{r\ge0}(b\kappa_r-\kappa_{r-1})\\
 &=b\sum_{r\ge0}\kappa_r-\sum_{r\ge0}\kappa_r\\
 &=(b-1)c_b(x,y).
\end{aligned}
\]

This proves the claim. \(\square\)

Equation (2.5) is the bridge between local carry events and a global digit invariant. The theory below uses it as a conservation mechanism, not merely as a method for computing the number of carries.

### Corollary 2.3 (radix shift)

For every \(n\in\mathbb N_0\),

\[
 s_b(bn)=s_b(n),\qquad c_b(bx,by)=c_b(x,y).
\tag{2.7}
\]

#### Proof

Multiplication by \(b\) appends a zero least-significant digit. It shifts every digit and every carry column by one place without changing either total. \(\square\)

---

## 3. The carry spectrum

### Definition 3.1 (carry spectrum)

Let \(n\in\mathbb N_{>0}\). The **base-\(b\) carry spectrum** of \(n\) is the vector

\[
 \Lambda_b(n):=\bigl(\lambda_b^1(n),\lambda_b^2(n),\ldots,\lambda_b^{b-1}(n)\bigr)^\top\in\mathbb N_0^{b-1},
\tag{3.1}
\]

whose components are

\[
 \lambda_b^j(n):=c_b(jn,n)
 =\frac{s_b(jn)+s_b(n)-s_b((j+1)n)}{b-1},
 \qquad 1\le j\le b-1.
\tag{3.2}
\]

The component index \(j\) is a **multiplier channel**. It records the carry weight incurred in the transition from \(jn\) to \((j+1)n\) by adding one more copy of \(n\).

The notation makes the arithmetic source of each component transparent:

\[
 jn+n=(j+1)n.
\tag{3.3}
\]

The vector does not encode every digit of every multiple. Rather, it records the aggregate carry response along the finite multiplier path \(1\to2\to\cdots\to b\).

### Theorem 3.2 (spectral conservation theorem)

For every base \(b\ge2\) and every positive integer \(n\),

\[
 \boxed{\;\mathbf 1_{b-1}^{\top}\Lambda_b(n)=s_b(n).\;}
\tag{3.4}
\]

Here \(\mathbf 1_{b-1}\) denotes the all-ones vector in \(\mathbb R^{b-1}\).

#### Proof

Using (3.2) and summing in \(j\),

\[
\begin{aligned}
\sum_{j=1}^{b-1}\lambda_b^j(n)
&=\frac{1}{b-1}\sum_{j=1}^{b-1}
\bigl[s_b(jn)+s_b(n)-s_b((j+1)n)\bigr]\\
&=\frac{1}{b-1}
\bigl[s_b(n)+(b-1)s_b(n)-s_b(bn)\bigr]\\
&=\frac{b\,s_b(n)-s_b(n)}{b-1}\\
&=s_b(n),
\end{aligned}
\]

where the penultimate equality applies Corollary 2.3. \(\square\)

The theorem says that the digit sum is not merely adjacent to the carry spectrum: it is exactly the spectral mass. Thus a scalar positional invariant is canonically resolved into \(b-1\) multiplier channels.

### Corollary 3.3 (nontriviality and bounds)

For each \(n>0\), \(\Lambda_b(n)\neq0\). Moreover,

\[
0\le \lambda_b^j(n)\le s_b(n),
\qquad 1\le j<b.
\tag{3.5}
\]

#### Proof

Since \(s_b(n)\ge1\), (3.4) implies nontriviality. The bounds follow because the components are nonnegative integers summing to \(s_b(n)\). \(\square\)

### Definition 3.4 (spectral content and primitive spectrum)

The **spectral content** and **primitive carry spectrum** are, respectively,

\[
 g_b(n):=\gcd\bigl(\lambda_b^1(n),\ldots,\lambda_b^{b-1}(n)\bigr),
\tag{3.6}
\]

and

\[
 \widehat\Lambda_b(n):=g_b(n)^{-1}\Lambda_b(n).
\tag{3.7}
\]

The gcd is well-defined because \(\Lambda_b(n)\neq0\). A number is **spectrally primitive** in base \(b\) if \(g_b(n)=1\).

This is an internal arithmetical property of the carry vector, not a claim of primality of \(n\). For example, a composite number can be spectrally primitive and a prime can have nontrivial spectral content.

### Theorem 3.5 (radial scale invariance)

For all \(n>0\),

\[
 \boxed{\;\Lambda_b(bn)=\Lambda_b(n),\qquad g_b(bn)=g_b(n).\;}
\tag{3.8}
\]

#### Proof

For each channel \(j\), Corollary 2.3 gives

\[
 \lambda_b^j(bn)=c_b(jbn,bn)=c_b(jn,n)=\lambda_b^j(n).
\]

The equality for the content follows componentwise. \(\square\)

### Definition 3.6 (spectral rays and carry classes)

The **base-\(b\) spectral ray** through \(n\) is

\[
 \mathcal R_b(n):=\{b^kn:k\in\mathbb N_0\}.
\tag{3.9}
\]

Theorem 3.5 makes \(\Lambda_b\) constant on every spectral ray. More generally, the **carry class** of \(n\) is the fiber

\[
 \mathcal C_b(n):=\{m>0:\Lambda_b(m)=\Lambda_b(n)\}.
\tag{3.10}
\]

Every spectral ray is contained in a carry class, but equality need not hold. Classifying the fibers \(\mathcal C_b(n)\) is one of the central inverse problems of the theory.

---

## 4. Tensorial encoding of the carry state

The vector \(\Lambda_b(n)\) records a channel distribution but not the spatial disposition of the digits that generated it. A minimal tensorial package joins these two pieces of information.

### Definition 4.1 (carry-digit tensor)

Let the **carry-digit tensor** be the rank-one tensor

\[
 \mathsf T_b(n):=\Lambda_b(n)\otimes\mathbf d_b(n)
 \in\mathbb N_0^{b-1}\otimes\mathbb N_0^{(\mathbb N_0)}.
\tag{4.1}
\]

In components,

\[
 \mathsf T_b{}^j{}_{r}(n)=\lambda_b^j(n)d_r(n),
 \qquad 1\le j<b,\quad r\ge0.
\tag{4.2}
\]

The upper channel label and lower digit-position label are bookkeeping indices; no metric or implied summation over unlike index spaces is assumed. The tensor is a state descriptor, not an additional multiplication law.

Let \(S\) be the unilateral shift acting on digit columns by

\[
(S\mathbf d)_0=0,\qquad(S\mathbf d)_{r+1}=d_r.
\tag{4.3}
\]

### Proposition 4.2 (tensorial scale covariance)

For all \(n>0\),

\[
 \mathsf T_b{}^j{}_{r}(bn)=\mathsf T_b{}^j{}_{r-1}(n)
\quad(r\ge1),
\qquad
\mathsf T_b{}^j{}_{0}(bn)=0.
\tag{4.4}
\]

Equivalently, with the digit index viewed as a column index,

\[
 \mathsf T_b(bn)=\mathsf T_b(n)S^{\top}.
\tag{4.5}
\]

#### Proof

Theorem 3.5 fixes the carry-spectrum factor, while multiplication by \(b\) shifts the digit vector as \(\mathbf d_b(bn)=S\mathbf d_b(n)\). Taking their tensor product proves the result. \(\square\)

Equation (4.5) separates two kinds of behavior. The carry state is radially invariant, whereas the digit support translates one position outward. This makes the tensorial package suitable for studying scale orbits without identifying the underlying digit placements.

### Definition 4.3 (spectral correlation kernel)

For \(m,n>0\), define

\[
 K_b(m,n):=\Lambda_b(m)^{\top}\Lambda_b(n)
 =\sum_{j=1}^{b-1}\lambda_b^j(m)\lambda_b^j(n).
\tag{4.6}
\]

The normalized coefficient

\[
 \rho_b(m,n):=
 \frac{K_b(m,n)}{\|\Lambda_b(m)\|_2\,\|\Lambda_b(n)\|_2}
\in[0,1]
\tag{4.7}
\]

will be called the **carry resonance** of \(m\) and \(n\).

### Proposition 4.4 (kernel properties)

The kernel \(K_b\) is symmetric and positive semidefinite. It is scale invariant in the sense that

\[
 K_b(bm,bn)=K_b(m,n),
\qquad
 \rho_b(bm,bn)=\rho_b(m,n).
\tag{4.8}
\]

#### Proof

Symmetry and positive semidefiniteness are immediate from the Euclidean inner-product representation in (4.6). Scale invariance follows from Theorem 3.5. \(\square\)

The kernel is not intended as a probability model. It is an exact similarity measure for the response of two integers to the same finite set of multiplier channels.

---

## 5. Additive interaction geometry

The carry spectrum of a sum is generally not the sum of the spectra. The difference is itself a structured quantity.

### Definition 5.1 (additive interaction vector)

For \(m,n>0\), define

\[
 \Gamma_b(m,n):=\Lambda_b(m+n)-\Lambda_b(m)-\Lambda_b(n)
 \in\mathbb Z^{b-1}.
\tag{5.1}
\]

The \(j\)-th component is

\[
 \Gamma_b^j(m,n)
 =c_b(j(m+n),m+n)-c_b(jm,m)-c_b(jn,n).
\tag{5.2}
\]

Thus \(\Gamma_b\) measures the nonlinearity of the carry spectrum under ordinary addition. Negative components denote channelwise cancellation relative to the separated operands; positive components denote newly concentrated carry activity.

### Theorem 5.2 (additive trace law)

For all \(m,n>0\),

\[
 \boxed{\;\mathbf1_{b-1}^{\top}\Gamma_b(m,n)=-(b-1)c_b(m,n).\;}
\tag{5.3}
\]

#### Proof

Applying Theorem 3.2 to the three terms in (5.1),

\[
\begin{aligned}
\mathbf1^\top\Gamma_b(m,n)
&=s_b(m+n)-s_b(m)-s_b(n)\\
&=-(b-1)c_b(m,n)
\end{aligned}
\]

by Lemma 2.2. \(\square\)

The theorem provides a noteworthy interpretation. The ordinary carry count of the addition \(m+n\) is the negative trace of a much finer vector-valued interaction. In this sense, the classical carry weight is a scalar shadow of \(\Gamma_b\).

### Corollary 5.3 (carry-free trace and redistribution)

If \(c_b(m,n)=0\), then \(\mathbf1^\top\Gamma_b(m,n)=0\). Nevertheless, \(\Gamma_b(m,n)\) may be nonzero.

#### Proof

The trace condition is immediate from (5.3). Nonvanishing is demonstrated concretely in Section 7 by \((b,m,n)=(10,7,11)\). \(\square\)

This distinction is important. A carry-free addition at the operand level can still redistribute spectrum across multiplier channels. Carry-spectral arithmetic therefore distinguishes **macroscopic carry neutrality** from **microscopic channel neutrality**.

### Definition 5.4 (additive spectral neutrality)

A pair \((m,n)\) is **spectrally neutral** in base \(b\) if

\[
 \Gamma_b(m,n)=0.
\tag{5.4}
\]

It is **trace-neutral** if \(c_b(m,n)=0\). Spectral neutrality implies trace-neutrality, but the converse does not hold in general.

---

## 6. Multiplicative defects and factor transport

Addition determines the carry spectrum, but the most number-theoretic questions arise when spectra are compared across factorization. Ordinary multiplication has no reason to preserve digit-based states. The failure of preservation is therefore taken as a primary invariant rather than an inconvenience.

### Definition 6.1 (binary multiplicative interaction)

For \(x,y>0\), define

\[
 \Pi_b(x,y):=\Lambda_b(xy)-\Lambda_b(x)-\Lambda_b(y)
 \in\mathbb Z^{b-1}.
\tag{6.1}
\]

This is the **binary multiplicative interaction vector**. It records the carry-spectrum distortion created by forming a product.

### Definition 6.2 (factor defect)

Let

\[
 n=\prod_{p\in\mathcal P}p^{\nu_p(n)}
\tag{6.2}
\]

be the ordinary prime factorization of \(n>1\). The **base-\(b\) factor defect** of \(n\) is

\[
 \Phi_b(n):=\Lambda_b(n)-\sum_{p\mid n}\nu_p(n)\Lambda_b(p).
\tag{6.3}
\]

The sum is finite. It is defined using the usual unique factorization of \(n\); carry-spectral arithmetic does not posit an alternative factorization law.

### Theorem 6.3 (factor-defect trace formula)

For all \(n>1\),

\[
 \boxed{\;\mathbf1_{b-1}^{\top}\Phi_b(n)
 =s_b(n)-\sum_{p\mid n}\nu_p(n)s_b(p).\;}
\tag{6.4}
\]

#### Proof

Take the all-ones trace of (6.3) and apply Theorem 3.2 termwise. \(\square\)

The right-hand side is an exact digit-sum discrepancy between an integer and its prime factors. The vector \(\Phi_b(n)\) refines that discrepancy into multiplier channels.

### Theorem 6.4 (factor transport decomposition)

Let \(n=q_1q_2\cdots q_k\), where each \(q_r>1\), and put \(Q_r:=q_1\cdots q_r\). Then

\[
 \sum_{r=2}^{k}\Pi_b(Q_{r-1},q_r)
 =\Lambda_b(n)-\sum_{r=1}^{k}\Lambda_b(q_r).
\tag{6.5}
\]

In particular, if the \(q_r\) are the prime factors repeated with multiplicity, then the left-hand side equals \(\Phi_b(n)\).

#### Proof

By Definition 6.1,

\[
\Pi_b(Q_{r-1},q_r)=\Lambda_b(Q_r)-\Lambda_b(Q_{r-1})-\Lambda_b(q_r).
\]

Summing from \(r=2\) to \(k\), the first two terms telescope:

\[
\sum_{r=2}^{k}\bigl[\Lambda_b(Q_r)-\Lambda_b(Q_{r-1})\bigr]
=\Lambda_b(Q_k)-\Lambda_b(Q_1).
\]

Since \(Q_k=n\) and \(Q_1=q_1\), subtracting \(\sum_{r=2}^k\Lambda_b(q_r)\) yields (6.5). \(\square\)

The intermediate interactions in (6.5) depend on the order in which factors are assembled, but their total does not. This gives a useful distinction between a **factor-assembly path**, which is order sensitive, and the **net factor defect**, which is a well-defined property of \(n\).

### Definition 6.5 (laminar and resonant factorizations)

A positive integer \(n>1\) is **factor-laminar** in base \(b\) if

\[
 \Phi_b(n)=0.
\tag{6.6}
\]

It is **factor-resonant** if \(\Phi_b(n)\ne0\). The terminology is descriptive: laminarity means that the complete carry spectrum of \(n\) equals the multiplicity-weighted sum of the carry spectra of its prime factors.

Factor-laminarity is a strong equality of vectors. It is not implied by the scalar equality in (6.4), and factor resonance can remain even when the trace in (6.4) vanishes.

---

## 7. Explicit calculations and computational procedure

The definitions above are finite and computable by direct positional addition. Tables 1–3 give exact values, using the component order \(j=1,\ldots,b-1\). Digits in the second column are written least-significant first to align them with (2.2).

### Table 1. Selected base-10 carry spectra

| \(n\) | Base-10 digits, LSD first | \(\Lambda_{10}(n)\) | \(s_{10}(n)\) | \(g_{10}(n)\) |
|---:|---|---|---:|---:|
| 1 | \([1]\) | \((0,0,0,0,0,0,0,0,1)\) | 1 | 1 |
| 7 | \([7]\) | \((1,1,0,1,1,0,1,1,1)\) | 7 | 1 |
| 11 | \([1,1]\) | \((0,0,0,0,0,0,0,0,2)\) | 2 | 2 |
| 19 | \([9,1]\) | \((1,1,1,1,2,1,1,1,1)\) | 10 | 1 |
| 37 | \([7,3]\) | \((1,2,0,1,2,0,1,2,1)\) | 10 | 1 |
| 49 | \([9,4]\) | \((1,2,1,2,1,2,1,2,1)\) | 13 | 1 |
| 999 | \([9,9,9]\) | \((3,3,3,3,3,3,3,3,3)\) | 27 | 3 |

For \(n=19\), the fifth channel is enhanced: adding \(19\) to \(5\cdot19=95\) produces \(114\), which has two carries. This accounts for \(\lambda_{10}^5(19)=2\). The conservation theorem checks immediately:

\[
1+1+1+1+2+1+1+1+1=10=s_{10}(19).
\tag{7.1}
\]

The number \(999\) is carry-balanced: each channel has the same weight. In contrast, \(11\) has an extremely concentrated spectrum: all of its mass lies in the ninth channel. These two examples already show that equal or comparable digit sums need not imply comparable carry geometry.

### Example 7.1 (base-3 scale invariance)

In base \(3\),

\[
 \Lambda_3(7)=(1,2),\qquad \Lambda_3(21)=(1,2),
\tag{7.2}
\]

because \(21=3\cdot7\). The equality is an instance of Theorem 3.5, not a numerical coincidence. Both vectors have mass \(3\), agreeing with \(s_3(7)=s_3(21)=3\).

### Table 2. Additive interactions

| Base \(b\) | \((m,n)\) | \(\Gamma_b(m,n)\) | \(\mathbf1^\top\Gamma_b(m,n)\) | \(c_b(m,n)\) |
|---:|---|---|---:|---:|
| 10 | \((19,37)\) | \((0,-3,1,-1,-3,0,-1,-1,-1)\) | \(-9\) | 1 |
| 10 | \((7,11)\) | \((0,0,1,0,0,1,0,0,-2)\) | \(0\) | 0 |
| 3 | \((7,8)\) | \((-1,-3)\) | \(-4\) | 2 |

The pair \((7,11)\) is especially instructive. The addition \(7+11=18\) is carry-free in base 10, so its interaction trace vanishes. Yet the spectrum changes by a nonzero vector. There is no ordinary carry at the level of \(7+11\), but the self-addition responses of the sum differ from the superposition of the self-addition responses of the two summands.

For \((m,n)=(19,37)\), equation (5.3) predicts a trace of \(-9\), because \(19+37=56\) has one base-10 carry. The displayed vector indeed sums to \(-9\).

### Table 3. Factor defects

| Base \(b\) | \(n\) and factorization | \(\Phi_b(n)\) | Trace |
|---:|---|---|---:|
| 10 | \(21=3\cdot7\) | \((-1,-1,-1,0,-1,-1,-1,-1,0)\) | \(-7\) |
| 10 | \(49=7^2\) | \((-1,0,1,0,-1,2,-1,0,-1)\) | \(-1\) |
| 10 | \(999=3^3\cdot37\) | \((2,1,0,2,1,0,2,1,-1)\) | \(8\) |
| 3 | \(10=2\cdot5\) | \((-3,0)\) | \(-3\) |

For example, in base 10,

\[
\begin{aligned}
\Phi_{10}(49)
&=\Lambda_{10}(49)-2\Lambda_{10}(7)\\
&=(1,2,1,2,1,2,1,2,1)\\
&\quad-(2,2,0,2,2,0,2,2,2)\\
&=(-1,0,1,0,-1,2,-1,0,-1).
\end{aligned}
\tag{7.3}
\]

Its trace is \(-1\), exactly equal to \(s_{10}(49)-2s_{10}(7)=13-14\), as required by Theorem 6.3.

### Algorithm 7.2 (direct spectrum computation)

The following procedure computes \(\Lambda_b(n)\) without constructing any objects beyond ordinary digits and carries.

```text
INPUT: base b >= 2; integer n > 0
OUTPUT: carry spectrum Lambda[1..b-1]

for j = 1 to b-1:
    x <- j*n
    y <- n
    carry <- 0
    Lambda[j] <- 0
    while x > 0 or y > 0 or carry > 0:
        a <- x mod b
        d <- y mod b
        carry <- floor((a + d + carry)/b)
        Lambda[j] <- Lambda[j] + carry
        x <- floor(x/b)
        y <- floor(y/b)
return Lambda
```

For fixed \(b\), the running time is \(O(\log_b n)\), because there are \(b-1\) channels and each channel processes a digit string of length \(O(\log_b n)\). The accompanying verification script checks the carry identity, conservation theorem, and scale invariance exhaustively over finite test ranges; it is not a substitute for the proofs given above.

---

## 8. Structural classes and conjectures

The exact theory developed so far is elementary but already creates a natural taxonomy. The following definitions identify different modes of carry organization.

### Definition 8.1 (concentrated, balanced, and primitive states)

An integer \(n>0\) is:

| Class | Defining condition | Interpretation |
|---|---|---|
| **Channel-concentrated** | \(\Lambda_b(n)=s_b(n)\mathbf e_j\) for some \(j\) | All spectral mass occurs in one multiplier channel. |
| **Carry-balanced** | \(\Lambda_b(n)=q\mathbf1_{b-1}\) for some \(q\in\mathbb N\) | All channels have equal carry weight. |
| **Spectrally primitive** | \(g_b(n)=1\) | The components have no common integer divisor. |
| **Factor-laminar** | \(\Phi_b(n)=0\) | The prime-factor spectrum sums exactly to the spectrum of \(n\). |
| **Spectrally neutral pair** | \(\Gamma_b(m,n)=0\) | Addition superposes without a carry-spectral interaction. |

For a carry-balanced number, the conservation theorem forces

\[
 s_b(n)=(b-1)q.
\tag{8.1}
\]

Thus digit sum divisibility by \(b-1\) is necessary for balance. It is not asserted to be sufficient.

The following conjectures are offered as precise research targets. They are deliberately stated in a form that can be disproved by computation or proof.

### Conjecture 8.2 (positive primitive spectral density among primes)

For every fixed base \(b\ge2\), there exists \(\delta_b>0\) such that

\[
 \liminf_{X\to\infty}
 \frac{\#\{p\le X:\ p\text{ prime and }g_b(p)=1\}}
 {\#\{p\le X:\ p\text{ prime}\}}
 \ge\delta_b.
\tag{8.2}
\]

The conjecture does not assert density one. It only proposes that nontrivial common divisibility across all carry channels does not asymptotically dominate the primes.

### Conjecture 8.3 (unbounded prime-semiprime factor defect)

For every base \(b\ge2\), the set

\[
 \left\{\|\Phi_b(pq)\|_1:\ p,q\text{ prime}\right\}
\tag{8.3}
\]

is unbounded.

This predicts that multiplication of two primes can create arbitrarily large carry-spectrum distortion. A proof would require controlling digit carry behavior of products, rather than merely the factorization structure of integers.

### Conjecture 8.4 (nontrivial fibers beyond radial scale)

For each \(b\ge3\), infinitely many carry classes \(\mathcal C_b(n)\) contain two distinct integers that are not on the same spectral ray.

The theorem on radial scale invariance gives a universal source of collisions. This conjecture predicts genuinely distinct collisions that are not explained by appending zeros in base \(b\).

### Question 8.5 (factor-laminar infinitude)

Are there infinitely many factor-laminar composite integers in any fixed base? If so, do they occur with zero density, positive density, or in structured digit families?

The answer would clarify whether exact spectral compatibility with prime factors is exceptional or abundant.

---

## 9. Programmatic extensions

Carry-spectral arithmetic is most useful if it leads to questions unavailable from digit sums alone. This section outlines several such directions without elevating them to established results.

### 9.1 Cross-base profiles

For a finite base window \(2\le b\le B\), define the **multibase carry profile**

\[
 \mathcal M_B(n):=\bigl(\Lambda_2(n),\Lambda_3(n),\ldots,\Lambda_B(n)\bigr).
\tag{9.1}
\]

Its components live in different dimensions, so it is a tuple rather than a single vector. A scalar aggregate may be formed by choosing weights \(w_b>0\):

\[
 \mathcal E_{B,w}(n):=\sum_{b=2}^{B}w_b\,\|\Lambda_b(n)\|_2^2.
\tag{9.2}
\]

This defines a multiscale carry energy. Since the spectrum is finite in every base, \(\mathcal E_{B,w}\) is an elementary computable integer-valued statistic for integral weights. A meaningful theory would study its average order, its behavior on arithmetic progressions, and its relation to prime factorization.

### 9.2 Spectral graphs

For a fixed base and cutoff \(X\), form a weighted graph with vertices \(1,\ldots,X\) and edge weight \(K_b(m,n)\). A thresholded version joins \(m\) and \(n\) when \(\rho_b(m,n)\ge\tau\). Such graphs organize integers by similarity of carry response rather than by proximity or divisibility. The spectral-ray invariance implies that multiplication by \(b\) acts as a graph symmetry on the unrestricted positive-integer graph.

### 9.3 Factor-assembly paths

Although \(\Phi_b(n)\) is independent of the order of a fixed multiset of factors, equation (6.5) provides path-dependent intermediate states. For a permutation \(\sigma\) of the prime factors of \(n\), define

\[
 \mathcal A_{b,\sigma}(n):=
 \bigl(\Lambda_b(q_{\sigma(1)}),\Lambda_b(q_{\sigma(1)}q_{\sigma(2)}),\ldots,\Lambda_b(n)\bigr).
\tag{9.3}
\]

One may ask which factor orders minimize the maximum interaction norm \(\|\Pi_b(Q_{r-1},q_r)\|_1\), or whether different orders exhibit universal extremal patterns. This is a combinatorial optimization problem induced by ordinary factorization.

### 9.4 Automata and formal languages

Because every component of \(\Lambda_b(n)\) results from a finite carry automaton applied to the digits of \(n\), the sets

\[
 \{n:\Lambda_b(n)=\boldsymbol\ell\}
\tag{9.4}
\]

are natural candidates for finite-state or transducer-based analysis. The direct construction must carefully account for multiplication by each channel multiplier \(j\), but all carries remain bounded. This suggests a route to decidability results for fixed base and fixed target spectrum.

---

## 10. Discussion

The theory developed here rests on one simple observation: the familiar digit sum \(s_b(n)\) can be decomposed exactly into the carry weights generated by the chain \(n+n,2n+n,\ldots,(b-1)n+n\). The strength of that observation is not its computational difficulty, but its ability to turn a scalar positional invariant into a vector state.

The proposed framework has four formal pillars:

\[
\begin{array}{rcl}
\text{state assignment} &:& n\longmapsto\Lambda_b(n),\\[2mm]
\text{conservation} &:& \mathbf1^\top\Lambda_b(n)=s_b(n),\\[2mm]
\text{additive interaction} &:& \Gamma_b(m,n)=\Lambda_b(m+n)-\Lambda_b(m)-\Lambda_b(n),\\[2mm]
\text{factor defect} &:& \Phi_b(n)=\Lambda_b(n)-\sum_{p\mid n}\nu_p(n)\Lambda_b(p).
\end{array}
\tag{10.1}
\]

These objects are exact. They do not depend on probabilistic modeling, asymptotics, or unproved assumptions. What remains open is whether their distribution contains information about primes, factorization, or digit dynamics that is not reducible to already familiar digit-sum phenomena.

The construction also specifies its own limits. It is base dependent, it is not a ring homomorphism, and the factor defect does not furnish a new unique-factorization theorem. These are features of the object under study, not defects in its definition. The point is precisely to quantify how positional carry states fail to be additive or multiplicative while retaining exact trace laws.

> **Research thesis.** Integer arithmetic possesses a finite positional state geometry: not because the value of an integer changes with representation, but because its carry response under structured operations has representation-dependent organization. Carry spectra provide one exact coordinate system for that geometry.

---

## Appendix A. Compact proof register

For reference, the principal exact identities are collected here.

| Label | Identity | Source |
|---|---|---|
| Carry identity | \(s_b(x)+s_b(y)-s_b(x+y)=(b-1)c_b(x,y)\) | Lemma 2.2 |
| Spectrum definition | \(\lambda_b^j(n)=c_b(jn,n)\) | Definition 3.1 |
| Conservation | \(\sum_{j=1}^{b-1}\lambda_b^j(n)=s_b(n)\) | Theorem 3.2 |
| Scale invariance | \(\Lambda_b(bn)=\Lambda_b(n)\) | Theorem 3.5 |
| Additive trace | \(\mathbf1^\top\Gamma_b(m,n)=-(b-1)c_b(m,n)\) | Theorem 5.2 |
| Factor trace | \(\mathbf1^\top\Phi_b(n)=s_b(n)-\sum_p\nu_p(n)s_b(p)\) | Theorem 6.3 |
| Factor transport | \(\Phi_b(n)=\sum_{r=2}^k\Pi_b(Q_{r-1},q_r)\) | Theorem 6.4 |

---

## Appendix B. Reproducibility note

The accompanying scripts `verify_carry_spectrum.py` and `example_defects.py` implement Definitions 2.1, 3.1, 5.1, and 6.2 directly. They verify, over stated finite ranges, that the digit-sum formula agrees with explicit column-by-column carrying, that the spectral conservation theorem and radial scale invariance hold on the tested inputs, and that the examples in Tables 1–3 are reproduced exactly. The mathematical validity of the theorems rests on the proofs in the body of the paper rather than on finite computation.

---

## References

[1] [Philip Ehrlich, “The Absolute Arithmetic Continuum and the Unification of all Numbers Great and Small,” *Bulletin of Symbolic Logic* 18(1), 2012.](https://www.cambridge.org/core/journals/bulletin-of-symbolic-logic/article/abs/absolute-arithmetic-continuum-and-the-unification-of-all-numbers-great-and-small/E9C197F043F75776F0F32705185CC4DF)

[2] [Paul Baginski and Scott Chapman, “Arithmetic Congruence Monoids: A Survey,” in *Combinatorial and Additive Number Theory*, Springer Proceedings in Mathematics & Statistics 101, 2014.](https://link.springer.com/chapter/10.1007/978-1-4939-1601-6_2)

[3] [James Dolan, “Carrying Is a 2-Cocycle,” reposted 2023; original discussion dated 1994.](https://timothychow.net/mathstuff/jdolan.pdf)

---

### Artifact manifest

| File | Purpose |
|---|---|
| `carry_spectral_arithmetic_preprint.md` | Complete academic preprint |
| `verify_carry_spectrum.py` | Finite-range identity and example verification |
| `example_defects.py` | Exact additive-interaction and factor-defect calculations |
| `research_notes.md` | Literature-boundary notes used in framing |

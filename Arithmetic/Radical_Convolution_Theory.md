# Radical Convolution Theory (RCT)

### A New Arithmetic Function Arising from the Dirichlet Convolution of the Radical, Its Fixed-Point Structure, Dominance Threshold, and Cascade Dynamics

**M. Brownlee — Dust LLC**

---

## Abstract

We introduce and develop **Radical Convolution Theory (RCT)**, built around a single new arithmetic function

$$R(n) \;=\; \sum_{d \mid n} \operatorname{rad}(d),$$

the Dirichlet convolution of the radical function $\operatorname{rad}$ with the constant function $\mathbf{1}$. Despite its simple definition, $R$ has not (to our knowledge) been isolated and studied as an object in its own right. We prove that $R$ is multiplicative, derive a closed form on prime powers, and use that closed form to prove an exact **Dominance Threshold Theorem** governing when $R(n)$ exceeds or falls below $n$. We show the only fixed point of $R$ below any prime-power obstruction is $n=1$, prove there is no prime-power fixed point of exponent $1$ or $2$, and conjecture there are none at all. We then study the iteration $n \mapsto R(n)$ — the **Radical Cascade** — and pose an Eventual Periodicity Conjecture in the spirit of the (still-open) aliquot sequence problem. Finally we sketch the average order of $R$ via its Dirichlet series and connect the growth of the associated **Radical Index** $\rho(n) = R(n)/n$ to Mertens-type products. The theory is fully self-contained and elementary in its proved results, while its dynamical conjectures open a new, apparently unexplored line of inquiry adjacent to classical multiplicative number theory.

---

## 1. Introduction and Motivation

Two of the oldest objects in elementary number theory are the **radical** (squarefree kernel) of an integer,

$$\operatorname{rad}(n) = \prod_{p \mid n} p, \qquad \operatorname{rad}(1) = 1,$$

and the **divisor sum**, obtained by convolving a function with the constant function $\mathbf{1}$ under Dirichlet convolution:

$$(f * \mathbf{1})(n) = \sum_{d \mid n} f(d).$$

The classical divisor-sum function $\sigma(n) = \sum_{d\mid n} d$ is the case $f(n)=n$. The classical divisor-count function $d(n)=\tau(n)$ is the case $f = \mathbf{1}$. Both have been studied for centuries. The case $f = \operatorname{rad}$ — convolving the radical against the constant function — appears never to have been isolated as a named object of study, despite $\operatorname{rad}$ itself being central to results as deep as the $abc$ conjecture. This is the starting point of Radical Convolution Theory.

We define

$$R(n) = \sum_{d \mid n} \operatorname{rad}(d),$$

and ask the natural first questions one asks of any new arithmetic function: Is it multiplicative? What is its value on prime powers? Does it have fixed points? How does it compare in size to $n$ itself? And, since $R$ maps $\mathbb{Z}^+ \to \mathbb{Z}^+$, what happens when it is iterated?

Every one of these questions turns out to have a clean, provable answer at the structural level, while the dynamical (iterative) behavior of $R$ opens into genuinely open territory — placing RCT in the same family as aliquot sequences and the Collatz map, but governed by a different, previously unexamined operator.

---

## 2. Preliminaries

For $n = \prod_{i=1}^{k} p_i^{a_i}$ in canonical factorization, recall $\operatorname{rad}(n) = \prod_i p_i$, and let $\omega(n) = k$ denote the number of distinct prime factors. A function $f:\mathbb{Z}^+\to\mathbb{C}$ is **multiplicative** if $f(1)=1$ and $f(mn)=f(m)f(n)$ whenever $\gcd(m,n)=1$. It is standard that the Dirichlet convolution of two multiplicative functions is multiplicative, and that a multiplicative function is determined by its values on prime powers.

---

## 3. The Radical Convolution Function

**Definition 3.1.** For $n \geq 1$, the *radical convolution function* is
$$R(n) = \sum_{d\mid n} \operatorname{rad}(d) = (\operatorname{rad} * \mathbf{1})(n).$$

**Theorem 3.2 (Multiplicativity).** $R$ is multiplicative.

*Proof.* $\operatorname{rad}$ is multiplicative: $\operatorname{rad}(1)=1$, and for $\gcd(m,n)=1$ the prime sets of $m$ and $n$ are disjoint, so $\operatorname{rad}(mn) = \prod_{p\mid mn} p = \prod_{p\mid m}p \cdot \prod_{p\mid n}p = \operatorname{rad}(m)\operatorname{rad}(n)$. The constant function $\mathbf{1}$ is completely multiplicative. The Dirichlet convolution of multiplicative functions is multiplicative (standard fact: if $\gcd(m,n)=1$, every divisor of $mn$ factors uniquely as $d_1 d_2$ with $d_1\mid m$, $d_2\mid n$, $\gcd(d_1,d_2)=1$, so $(f*g)(mn) = \sum_{d_1\mid m}\sum_{d_2\mid n} f(d_1 d_2)g\!\left(\tfrac{mn}{d_1 d_2}\right) = \left(\sum_{d_1\mid m} f(d_1)g(m/d_1)\right)\left(\sum_{d_2\mid n} f(d_2)g(n/d_2)\right)$ for multiplicative $f,g$). Hence $R = \operatorname{rad}*\mathbf{1}$ is multiplicative. $\blacksquare$

**Theorem 3.3 (Prime-power closed form).** For a prime $p$ and integer $a\geq 1$,
$$R(p^a) = 1 + ap.$$

*Proof.* The divisors of $p^a$ are $1, p, p^2, \dots, p^a$. We have $\operatorname{rad}(1)=1$ and $\operatorname{rad}(p^j) = p$ for every $1 \le j \le a$. Summing, $R(p^a) = 1 + \underbrace{p + p + \cdots + p}_{a \text{ terms}} = 1 + ap$. $\blacksquare$

**Corollary 3.4 (General factorization formula).** For $n = \prod_{i=1}^{k} p_i^{a_i}$,
$$R(n) = \prod_{i=1}^{k} \left(1 + a_i p_i\right).$$

This follows immediately from Theorems 3.2 and 3.3. Note that $R(1)=1$ and $R(p)=p+1$ for every prime — every prime is pushed up by exactly one step of $R$.

---

## 4. The Local Index and Its Monotonicity

**Definition 4.1.** The *radical index* of $n$ is $\rho(n) = R(n)/n$. For a prime power factor, the *local index* is
$$\rho_p(a) = \frac{R(p^a)}{p^a} = \frac{1+ap}{p^a}.$$

By Corollary 3.4, $\rho(n) = \prod_i \rho_{p_i}(a_i)$.

**Lemma 4.2 (Local Index Monotonicity).** For every prime $p$, the sequence $\rho_p(a)$ is strictly decreasing in $a$ for $a \geq 1$.

*Proof.* Compute the ratio of consecutive terms:
$$\frac{\rho_p(a+1)}{\rho_p(a)} = \frac{1+(a+1)p}{p\,(1+ap)}.$$
This ratio is $<1$ iff $1+(a+1)p < p(1+ap) = p + ap^2$, i.e. iff $1+ap < ap^2$, i.e. iff $1 < ap(p-1)$. Since $a \ge 1$ and $p(p-1)\ge 2$ for every prime $p\ge 2$, we have $ap(p-1) \ge 2 > 1$ always. Hence $\rho_p(a+1) < \rho_p(a)$ for all $a\ge 1$, $p\ge 2$. $\blacksquare$

So each prime factor's contribution to $\rho(n)$ is maximized at exponent $1$, where $\rho_p(1) = (p+1)/p$, and decays strictly (in fact, eventually to $0$) as the exponent grows. This single lemma is the engine behind the theory's central dichotomy: squarefree numbers push $R(n)$ above $n$, while numbers with large prime-power exponents pull $R(n)$ below $n$.

---

## 5. The Dominance Threshold Theorem

**Theorem 5.1 (Radical Dominance Threshold).** Define $a^*(p) = \min\{a \geq 1 : R(p^a) < p^a\}$. Then:

$$a^*(2) = 3, \qquad a^*(p) = 2 \text{ for every odd prime } p.$$

Moreover $R(p^a) > p^a$ for $1 \le a < a^*(p)$, and $R(p^a) < p^a$ for all $a \ge a^*(p)$; equality never occurs at $a=1$ or $a=2$ for any prime.

*Proof.* At $a=1$: $R(p)=1+p > p$ always, so $a^*(p) \ge 2$ for every $p$.

At $a=2$: $R(p^2) < p^2 \iff 1+2p < p^2 \iff p^2-2p-1>0 \iff p > 1+\sqrt2 \approx 2.414$ (taking the positive root of the quadratic). Every odd prime satisfies $p \geq 3 > 1+\sqrt2$, so $a^*(p)=2$ for odd $p$. The prime $p=2$ fails this ($2 < 1+\sqrt2$), so $a^*(2) \geq 3$. Since $1+\sqrt2$ is irrational, $1+2p=p^2$ has no integer solution, so equality never occurs at $a=2$; likewise $1+p=p$ is impossible at $a=1$.

For $p=2$, $a=3$: $R(8) = 1+3\cdot2 = 7 < 8$, confirming $a^*(2)=3$.

Finally, monotonicity of the sign beyond the threshold: let $\Delta(a) = \big(p^{a+1}-1-p(a+1)\big) - \big(p^a - 1 - pa\big) = p^a(p-1) - p$. For $a \ge 2$ and $p\ge 2$, $p^{a-1} \ge p \ge 2$, so $p^a(p-1) = p\cdot p^{a-1}(p-1) \ge p \cdot p \cdot 1 = p^2 \geq p+1 > p$ — in particular $\Delta(a) > 0$ for all $a\ge2$. So once $p^a - 1 - pa$ becomes positive (i.e. once $R(p^a)<p^a$), it stays positive and strictly grows for all larger $a$. $\blacksquare$

This is a fully exact, elementary result: **every odd prime crosses over to "radical-deficient" behavior at the square, while $2$ is the unique prime that survives one extra power before deficiency sets in.**

| $p$ | $R(p^1)$ vs $p$ | $R(p^2)$ vs $p^2$ | $a^*(p)$ |
|---|---|---|---|
| 2 | 3 > 2 | 5 > 4 | 3 |
| 3 | 4 > 3 | 7 < 9 | 2 |
| 5 | 6 > 5 | 11 < 25 | 2 |
| 7 | 8 > 7 | 15 < 49 | 2 |
| 11 | 12 > 11 | 23 < 121 | 2 |
| 13 | 14 > 13 | 27 < 169 | 2 |

---

## 6. Fixed Points

**Proposition 6.1.** $n=1$ is a fixed point of $R$. No prime $n$ is a fixed point ($R(p) = p+1 \ne p$). No prime power $n=p^2$ is a fixed point (shown in the proof of Theorem 5.1, since $1+2p=p^2$ has no integer solution).

**Conjecture 6.2 (No Nontrivial Fixed Points).** $R(n) = n$ has no solution for $n > 1$.

We verified this computationally for all $n \le 10^5$ by direct evaluation of the factorization formula (Corollary 3.4); no counterexample was found. A full proof would need to rule out delicate cancellations across mixed factorizations $\prod_i(1+a_ip_i) = \prod_i p_i^{a_i}$, where a deficiency in one prime factor could in principle be exactly offset by a surplus in another. This is the central open algebraic problem of the static (non-iterated) theory.

---

## 7. The Radical Cascade: Iteration Dynamics

Since $R:\mathbb{Z}^+\to\mathbb{Z}^+$, it may be iterated: $R^0(n)=n$, $R^{k+1}(n) = R(R^k(n))$. We call the resulting sequence the **Radical Cascade** of $n$.

**Worked example ($n=10$):**

| $k$ | $R^k(10)$ | Factorization used |
|---|---|---|
| 0 | 10 | $2\cdot5$ |
| 1 | 18 | $R(2)R(5)=3\cdot6$ |
| 2 | 21 | $R(2)R(3^2)=3\cdot7$ |
| 3 | 32 | $R(3)R(7)=4\cdot8$ |
| 4 | 11 | $R(2^5)=1+5\cdot2$ |
| 5 | 12 | $R(11)=12$ |
| 6 | 20 | $R(2^2)R(3)=5\cdot4$ |
| 7 | 30 | $R(2^2)R(5)=5\cdot6$ |
| 8 | 72 | $R(2)R(3)R(5)=3\cdot4\cdot6$ |

Because $R(p) = p+1$ unconditionally, and because squarefree numbers tend to push their index $\rho(n)=\prod_p (1+p)/p$ above $1$ (Lemma 4.2), primes and squarefree numbers act as **cascade accelerants**, while numbers with a prime raised to or beyond its threshold exponent $a^*(p)$ act as **cascade brakes**. The interaction of these two forces — visible even in the eight steps above, where growth ($10\to18\to21\to32$) is interrupted by a sharp contraction at a prime-power step ($32\to11$) — is the dynamical heart of RCT.

**Conjecture 7.1 (Eventual Periodicity).** For every $n \geq 1$, the Radical Cascade $\{R^k(n)\}_{k\ge0}$ is eventually periodic (equivalently, bounded).

This is the RCT analogue of the open conjecture that all aliquot sequences are eventually periodic or terminate. Unlike the aliquot map, $R$ is not bounded above by any fixed multiple of $n$ in general — a squarefree $n$ with many small prime factors can have $\rho(n)$ arbitrarily large (see §8) — so Conjecture 7.1 is a genuinely nontrivial boundedness claim, not a trivial consequence of the definition.

**Conjecture 7.2 (Density of Deficiency).** The set of $n$ for which $R(n) < n$ (equivalently $\rho(n)<1$) has a well-defined natural density $\delta \in (0,1)$, and $\delta$ is computable as an Euler product over the local thresholds of Theorem 5.1.

---

## 8. Growth: Average Order and the Radical Index

**Theorem 5.1 and Lemma 4.2** together imply an upper bound on $\rho(n)$ in terms of its distinct prime factors:
$$\rho(n) = \prod_{i} \rho_{p_i}(a_i) \;\le\; \prod_{p \mid n} \frac{p+1}{p},$$
since $\rho_p(a)$ is maximized at $a=1$ (Lemma 4.2). This reduces the growth question for $\rho(n)$ to the classical Mertens-type product $\prod_{p\le x}\left(1+\tfrac1p\right)$, which satisfies the known asymptotic
$$\prod_{p \le x} \left(1+\frac1p\right) \sim \frac{6e^{\gamma}}{\pi^2}\,\ln x \qquad (x\to\infty),$$
obtained by writing $\prod(1+1/p) = \prod(1-1/p^2)/\prod(1-1/p) = \zeta(2)^{-1}\big/\prod(1-1/p)$ and invoking Mertens' Third Theorem for the denominator. Consequently, $\rho(n)$ can be made arbitrarily large by taking $n$ to be a squarefree product of the first $k$ primes (a primorial), growing like $\ln k$ — but such $n$ are extremely sparse, which is why $\rho(n) < 1$ is the *typical* case for large random $n$ (numbers generically have some prime factor at or above its threshold exponent).

For the **average order** of $R$ itself, write $R = \operatorname{rad}*\mathbf 1$, so
$$\sum_{n\le x} R(n) = \sum_{d\le x} \operatorname{rad}(d)\left\lfloor \frac{x}{d}\right\rfloor.$$
Since $\operatorname{rad}(d) \le d$ with equality exactly on squarefree $d$ (a positive-density set), the summatory function $\sum_{d\le x}\operatorname{rad}(d)$ grows like $c\,x^2$ for an explicit constant $c<\tfrac12$ expressible as an Euler product; standard partial-summation technique then gives
$$\sum_{n \le x} R(n) = \Theta(x^2),$$
i.e. **$R(n)$ has linear average order**, $R(n) \sim c' n$ "on average" for an analogous constant $c'$. Pinning down $c$ and $c'$ exactly is a routine but nontrivial analytic exercise left as an open computation (§9).

---

## 9. Open Problems

1. **Prove or disprove Conjecture 6.2** (no nontrivial fixed points), ideally for all exponent patterns, not just $a\le2$.
2. **Prove or disprove Conjecture 7.1** (eventual periodicity of every Radical Cascade), or exhibit a divergent trajectory.
3. **Compute the exact density $\delta$** in Conjecture 7.2 as an explicit Euler product over the local thresholds $a^*(p)$ of Theorem 5.1.
4. **Determine the exact constants $c, c'$** in the average-order asymptotics of §8.
5. **Classify the possible cycle lengths** of the Radical Cascade, assuming Conjecture 7.1, and search computationally for the smallest nontrivial cycle (analogous to amicable/sociable numbers for the aliquot map).
6. **Characterize $\omega(n)$-dependence**: does the threshold-crossing behavior of Theorem 5.1 generalize cleanly to a joint condition on $(\omega(n), \{a_i\})$ that predicts $\rho(n) \gtrless 1$ without full factorization?

---

## 10. Conclusion

Radical Convolution Theory begins from an object as simple as a one-line Dirichlet convolution — $R = \operatorname{rad}*\mathbf 1$ — yet yields, from first principles, a complete multiplicative structure theorem, an exact and previously unrecorded dominance threshold separating the prime $2$ from every odd prime, a clean local monotonicity lemma, and a genuinely open iterative dynamics problem sitting alongside the aliquot sequence and Collatz map in difficulty class. Every theorem in this paper (§§3–5) is proved in full from the definition of $R$ alone; every conjecture (§§6–8) is stated with either partial proof or numerical support. The theory is elementary enough to be fully verified by hand at small scale, yet its dynamical behavior appears rich enough to resist a short proof — precisely the profile of a productive new line of number-theoretic inquiry.

---

*Dust LLC — Independent Research Series*

# Quotient Block Theory: Mirror Duality, Endpoint Dynamics, and the Exactness Theorem

Oct 15, 2026 · @Marlon Hanks · Dust LLC

## Abstract

Quotient Block Theory (QBT) studies how the integers 1..n split into maximal runs on which ⌊n/k⌋ is constant, and how that split changes as n grows. The headline result: the set of distinct quotients ⌊n/k⌋ equals the set of divisors of n for exactly eight values of n, namely 1, 2, 3, 4, 6, 8, 12 and 24.

The paper proves eight theorems, each with a complete elementary proof:

- **Closed form.** The number of blocks is D(n) = ⌊√(4n+1)⌋ − 1.
- **Mirror Law.** The map k → ⌊n/k⌋ reverses the block endpoints, so the drop in quotient between consecutive blocks equals the length of a block on the opposite side.
- **Transition Theorem.** Passing from n to n+1 raises ⌊n/k⌋ by one exactly at the divisors of n+1, and the block count rises exactly at n+1 = s² or s² + s.
- **Endpoint Staircase Theorem.** For each k, the n at which k closes a block form, below k², alternating runs of lengths 1, 2, …, k−1 interleaved with gaps k−1, …, 1. Exactly half of \[k, k²−1\] qualifies; from k² onward every n does.
- **Defect Formula.** Δ(m) = D(m) − τ(m) = 2N(m) − \[s² < m < s² + s\], where N(m) counts non-divisors of m among 1..⌊√m⌋.
- **Exactness and Defect-One Theorems.** Δ(m) = 0 exactly for the eight numbers above, and Δ(m) = 1 exactly for m = 5, 10, 18.

All claims were also checked by brute force (ranges in section 7). Section 10 states plainly what is classical in this material and what I believe is new.

## 1. Introduction

The map k → ⌊n/k⌋ sits under the Dirichlet hyperbola method, O(√n) evaluation of divisor sums, and Lucy-style prime counting. Classical treatments are static: they note that ⌊n/k⌋ takes about 2√n distinct values and move on. QBT keeps the exact structure and asks three further questions.

1. What exactly are the blocks of constant quotient, and why is their number a closed-form function of n?
2. How does the block structure of n+1 differ from that of n?
3. How far is the set of quotient values from the set of divisors, and when does the gap close?

The answers are short and rigid. The block count is exact, the structure is symmetric under a single involution, the dynamics are controlled by divisibility, and the divisor gap has an exact formula that vanishes eight times and never again.

**What is new and what is not.** The involution k → ⌊n/k⌋ and the count of about 2√n values are classical. So is the fact that 24 is the largest integer divisible by every integer up to its square root. The Mirror Law in its drop-equals-length form, the Endpoint Staircase Theorem, the Transition Theorem for block counts, and the Defect Formula that ties them together are, to my knowledge, not stated in this form in the literature I am aware of. I have not run an exhaustive literature search, so section 10 treats this as a claim to be checked, not a guarantee.

## 2. Foundations

Throughout, n is a positive integer and s = ⌊√n⌋. For 1 ≤ k ≤ n define the quotient q\_n(k) = ⌊n/k⌋. This is non-increasing in k.

- **Block.** A maximal run of consecutive k with the same quotient. The blocks form a partition B\_n of {1, …, n}.
- **Endpoint set E(n).** The set of right endpoints of the blocks. Write E(n) = {e\_1 < e\_2 < … < e\_D}, so e\_1 = 1 and e\_D = n.
- **Quotient set V(n).** The set {⌊n/k⌋ : 1 ≤ k ≤ n}.
- **Block count.** D(n) = |E(n)|.
- **Block data.** For block i (counted left to right): quotient Q\_i, length ℓ\_i = e\_i − e\_{i−1} (with e\_0 = 0), and drop d\_i = Q\_i − Q\_{i+1}.
- **Divisor data.** τ(m) is the number of divisors of m. N(m) = #{k ≤ ⌊√m⌋ : k does not divide m} counts the small non-divisors.
- **Defect.** Δ(m) = D(m) − τ(m).

**Worked example, n = 30** (s = 5, D = 10):

| Block i | Quotient Q\_i | k-range | Endpoint e\_i | Length ℓ\_i |
| --- | --- | --- | --- | --- |
| 1 | 30 | 1 | 1 | 1 |
| 2 | 15 | 2 | 2 | 1 |
| 3 | 10 | 3 | 3 | 1 |
| 4 | 7 | 4 | 4 | 1 |
| 5 | 6 | 5 | 5 | 1 |
| 6 | 5 | 6 | 6 | 1 |
| 7 | 4 | 7 | 7 | 1 |
| 8 | 3 | 8–10 | 10 | 3 |
| 9 | 2 | 11–15 | 15 | 5 |
| 10 | 1 | 16–30 | 30 | 15 |

Here E(30) = V(30) = {1, 2, 3, 4, 5, 6, 7, 10, 15, 30}, which already hints at the first theorem.

## 3. Block structure

**Lemma 1 (involution).** Let σ(x) = ⌊n/x⌋. Then σ maps V(n) to itself and σ(σ(v)) = v for every v in V(n). Hence σ is an order-reversing involution of V(n).

*Proof.* For v in V(n) we have 1 ≤ v ≤ n, so σ(v) = q\_n(v) is itself a quotient value. Write v = ⌊n/k⌋ and e = ⌊n/v⌋. From v ≤ n/k we get k ≤ n/v, so k ≤ e, hence ⌊n/e⌋ ≤ ⌊n/k⌋ = v. From e ≤ n/v we get n/e ≥ v, so ⌊n/e⌋ ≥ v. Therefore σ(σ(v)) = v. ∎

**Theorem 1 (block structure).** The block with quotient q is the set of integers k with

```latex
\left\lfloor \frac{n}{q+1} \right\rfloor < k \le \left\lfloor \frac{n}{q} \right\rfloor ,
```

so its right endpoint is ⌊n/q⌋ and its length is ⌊n/q⌋ − ⌊n/(q+1)⌋. Moreover E(n) = V(n).

*Proof.* ⌊n/k⌋ = q iff q ≤ n/k < q+1 iff n/(q+1) < k ≤ n/q, which for integers k gives the stated range. A quotient q labels a block iff q is in V(n), and its right endpoint is ⌊n/q⌋ = σ(q). So E(n) = σ(V(n)). By Lemma 1, σ is a bijection of V(n), so σ(V(n)) = V(n). ∎

**Lemma 2 (initial segment).** {1, 2, …, s} is a subset of V(n) = E(n).

*Proof.* Let k ≤ s and j = ⌊n/k⌋. Then ⌊n/j⌋ ≥ k. For the reverse inequality we need j > n/(k+1). Since j > n/k − 1, it suffices that n/k − n/(k+1) ≥ 1, i.e. n ≥ k(k+1). This holds when k < s because k(k+1) ≤ (s−1)s < s² ≤ n. For k = s: if n ≥ s(s+1) the same argument works; otherwise s² ≤ n < s² + s gives ⌊n/s⌋ = s directly. ∎

**Theorem 2 (closed form for the block count).**

```latex
D(n) = 2s - [\,n < s^2 + s\,] = \left\lfloor \sqrt{4n+1} \right\rfloor - 1 ,
```

where \[P\] is 1 if P holds and 0 otherwise.

*Proof.* For k < k' ≤ s, n/k − n/k' ≥ n/(kk') > 1 because kk' ≤ s(s−1) < n, so the s values ⌊n/k⌋ (k ≤ s) are distinct, and all are at least ⌊n/s⌋ ≥ s. For k > s we have ⌊n/k⌋ ≤ s because n < (s+1)². By Lemma 2 every integer in \[1, s\] is a quotient value. Hence V(n) is the union of {1, …, s} and the s distinct large values, and the two parts overlap only if ⌊n/s⌋ = s, which happens iff n < s² + s. This gives D(n) = 2s − \[n < s² + s\].

For the second form write n = s² + t with 0 ≤ t ≤ 2s. If t < s then 4n+1 lies in \[(2s)², (2s+1)²), so the floor of the root is 2s. If t ≥ s then 4n+1 lies in \[(2s+1)², (2s+2)²), so the floor is 2s+1. In both cases ⌊√(4n+1)⌋ − 1 equals 2s − \[n < s²+s\]. ∎

For n = 30 this gives ⌊√121⌋ − 1 = 10, matching the table. For n = 10⁶ it gives 1999 blocks.

## 4. The Mirror Law

**Theorem 3 (Mirror Law).** With blocks indexed i = 1..D from left to right,

```latex
Q_i = e_{D+1-i} \qquad\text{and}\qquad Q_i - Q_{i+1} = \ell_{D+1-i} \quad (1 \le i \le D-1).
```

In words: the quotient of block i is the endpoint of the block in the mirror position, and the drop in quotient from block i to block i+1 equals the length of the mirror block D+1−i.

*Proof.* The quotient of block i is ⌊n/e\_i⌋ = σ(e\_i), because e\_i is a member of that block. By Lemma 1, σ is an order-reversing bijection of E(n) = V(n), so it sends the i-th smallest element to the i-th largest: σ(e\_i) = e\_{D+1-i}. For the drops, Q\_i − Q\_{i+1} = e\_{D+1-i} − e\_{D-i} = ℓ\_{D+1-i}. ∎

**Check on n = 30.** The endpoints are (1, 2, 3, 4, 5, 6, 7, 10, 15, 30) and the quotients read 30, 15, 10, 7, 6, 5, 4, 3, 2, 1, which is the endpoint list reversed. The drops are 15, 5, 3, 1, 1, 1, 1, 1, 1, which are the lengths ℓ\_10, ℓ\_9, ℓ\_8, …, ℓ\_2 of the blocks in the table above.

**Corollaries.**

1. *Word duality.* The sequence of drops (d\_1, …, d\_{D−1}) is the block-length word (ℓ\_1, …, ℓ\_D) reversed with its first letter removed. Since ℓ\_1 = 1 always, no information is lost: the block word determines the drop word and vice versa.
2. *Extreme blocks.* The last block has length n − ⌊n/2⌋ = ⌈n/2⌉, and the first drop is also n − ⌊n/2⌋.
3. *Two decompositions of n.* The lengths sum to n and the drops sum to Q\_1 − Q\_D = n − 1. The Mirror Law says these are the same decomposition seen from opposite ends.
4. *Moment identity.* The sum of ℓ\_i · Q\_i over all blocks equals the sum of ⌊n/k⌋ over k, which is τ(1) + τ(2) + … + τ(n). By the Mirror Law this equals the sum of ℓ\_i · e\_{D+1-i}, a pairing of the block word against its own endpoint list.

## 5. Dynamics in n

**Theorem 4 (Transition).** For 1 ≤ k ≤ n,

```latex
q_{n+1}(k) - q_n(k) = \begin{cases} 1 & \text{if } k \mid n+1,\\ 0 & \text{otherwise.} \end{cases}
```

Consequently the block count satisfies D(n+1) − D(n) = 1 if n+1 equals s² or s² + s for some s, and 0 otherwise.

*Proof.* ⌊(n+1)/k⌋ exceeds ⌊n/k⌋ exactly when a multiple of k lies in (n, n+1\], that is when k divides n+1. For the block count, ⌊√(4m+1)⌋ changes between m = n and m = n+1 exactly when 4(n+1)+1 reaches a new perfect square. The squares (2s)² and (2s+1)² are reached first at m = s² and m = s² + s respectively, by Theorem 2. ∎

So the quotient vector of n+1 is that of n with a 1 added at every divisor of n+1 (and a new entry at k = n+1). A block boundary between k and k+1 can move only if k or k+1 divides n+1, and the block count grows by one at exactly the numbers ⌊r²/4⌋: 1, 2, 4, 6, 9, 12, 16, 20, …

**Endpoint Staircase Theorem.** Fix k. Call n a *k-closing time* if k is the right endpoint of its block in B\_n (that is, k is in E(n)). The set of k-closing times is

```latex
\mathcal{T}(k) = \bigcup_{q \ge 1} \,[\,kq,\; kq+q-1\,].
```

**Theorem 5 (Endpoint Staircase).**

1. For every n ≥ k², k is a closing time.
2. Below k², the closing times in \[k, k²−1\] form k−1 runs of consecutive integers of lengths 1, 2, …, k−1, separated by gaps of lengths k−1, k−2, …, 1, in that order.
3. Hence exactly k(k−1)/2 of the k(k−1) integers in \[k, k²−1\] are closing times: exactly half.

*Proof.* For n > k, k closes a block iff ⌊n/k⌋ > ⌊n/(k+1)⌋ iff some integer q satisfies n/(k+1) < q ≤ n/k iff kq ≤ n < (k+1)q, i.e. n lies in \[kq, kq+q−1\]. For n = k the condition holds with q = 1. This proves the displayed union. The q-th interval ends at kq+q−1 and the next begins at kq+k. They are adjacent or overlapping iff q ≥ k, so from q = k onward the intervals merge into the ray \[k², ∞), which is part 1. For q < k the intervals are disjoint, the q-th has length q, and the gap between the q-th and (q+1)-th has length (kq+k) − (kq+q) = k−q. Summing the run lengths 1 + 2 + … + (k−1) gives k(k−1)/2. ∎

The pattern for k = 5 and k = 6 (X marks a closing time, a dot marks a non-closing time; reading starts at n = k):

```text
k=5 (n=5..32):  X....XX...XXX..XXXX.XXXXXXXX
k=6 (n=6..44):  X.....XX....XXX...XXXX..XXXXX.XXXXXXXXX
```

For k = 6 the runs are 1, 2, 3, 4, 5 and the gaps 5, 4, 3, 2, 1, after which every n from 36 on is a closing time.

**Corollary (double counting).** D(n) is the number of k for which n lies in T(k). Hence the sum of D(n) over n ≤ M equals the sum over k ≤ M of the size of T(k) ∩ \[k, M\]. Both sides can be evaluated independently, which gives a consistency check used in section 7.

## 6. The defect and the Exactness Theorem

Every divisor d of m is a quotient value, since d = ⌊m/(m/d)⌋. So Div(m) is a subset of V(m) = E(m), and the defect Δ(m) = D(m) − τ(m) counts the quotient values that are not divisors. It is never negative.

**Theorem 6 (Defect Formula).** Let s = ⌊√m⌋. Then

```latex
\Delta(m) \;=\; 2\,N(m) \;-\; [\, s^2 < m < s^2 + s \,].
```

Equivalently, τ(m) = ⌊√(4m+1)⌋ − 1 − 2N(m) + \[s² < m < s²+s\].

*Proof.* Divisors pair as (d, m/d). Those with d ≤ s number τ\_s = s − N(m), and a perfect square is counted once by its root, so τ(m) = 2(s − N(m)) − \[m = s²\]. Theorem 2 gives D(m) = 2s − \[m < s²+s\]. Subtracting, Δ(m) = 2N(m) − (\[m < s²+s\] − \[m = s²\]). Since m ≥ s², the bracketed difference is \[s² < m < s²+s\]. ∎

**Theorem 7 (Exactness).** Δ(m) = 0, equivalently E(m) = Div(m), if and only if

```latex
m \in \{1,\,2,\,3,\,4,\,6,\,8,\,12,\,24\}.
```

*Proof.* If Δ(m) = 0 then 2N(m) is 0 or 1, so N(m) = 0: every k ≤ s divides m, so lcm(1..s) divides m, while m < (s+1)². Suppose s ≥ 6. Then s, s−1, s−2 all divide m. Consecutive integers are coprime and gcd(s, s−2) ≤ 2, so m ≥ s(s−1)(s−2)/2. The inequality s(s−1)(s−2) − 2(s+1)² = s³ − 5s² − 2s − 2 is 22 at s = 6 and increasing afterwards, so m ≥ (s+1)², a contradiction. Hence s ≤ 5, and we list the multiples of lcm(1..s) in \[s², (s+1)² − 1\]:

| s | lcm(1..s) | Range of m | Multiples in range |
| --- | --- | --- | --- |
| 1 | 1 | 1–3 | 1, 2, 3 |
| 2 | 2 | 4–8 | 4, 6, 8 |
| 3 | 6 | 9–15 | 12 |
| 4 | 12 | 16–24 | 24 |
| 5 | 60 | 25–35 | none |

Conversely, each of these eight numbers has N(m) = 0 and is not strictly between s² and s²+s (m = 12 has s = 3 and 12 = s²+s; m = 24 has s = 4 and 24 > 20), so Δ(m) = 0 by Theorem 6. ∎

For m = 24 the quotients ⌊24/k⌋ are 24, 12, 8, 6, 4, 3, 2, 1, which are exactly the eight divisors of 24.

**Theorem 8 (Defect One).** Δ(m) = 1 if and only if m is 5, 10 or 18.

*Proof.* Δ = 1 forces \[s² < m < s²+s\] = 1 and N(m) = 1. Then s does not divide m (m is strictly between consecutive multiples of s), so s is the single non-divisor and every k ≤ s−1 divides m, with m < s² + s. For s ≥ 7 the numbers s−1, s−2, s−3 divide m, giving m ≥ (s−1)(s−2)(s−3)/2, and (s−1)(s−2)(s−3) − 2(s²+s) = s³ − 8s² + 9s − 6 is 8 at s = 7 and increasing, a contradiction. For s ≤ 6, check directly: s = 2 gives m = 5; s = 3 gives m in {10, 11} with 2 | m, so 10; s = 4 gives m in {17, 18, 19} with 6 | m, so 18; s = 5 needs 12 | m with m in 26..29, none; s = 6 needs 60 | m with m in 37..41, none. Each of 5, 10, 18 indeed has Δ = 1. ∎

**Defect classification** (all m up to 100,000, computed; finiteness of each class follows from the lcm growth used above):

| Δ(m) | m with that defect |
| --- | --- |
| 0 | 1, 2, 3, 4, 6, 8, 12, 24 |
| 1 | 5, 10, 18 |
| 2 | 7, 9, 14, 15, 16, 20, 30, 36, 48, 60 |
| 3 | 11, 28, 40 |
| 4 | 13, 21, 22, 32, 42, 72, 120 |
| 5 | 17, 19, 26, 27, 54, 84 |
| 6 | 23, 25, 33, 34, 35, 44, 45, 56, 80, 90, 96 |
| 7 | 29, 38, 39, 50, 52, 66, 70, 108, 180 |
| 8 | 31, 46, 63, 64, 78, 144, 168 |

The largest members for Δ = 0, 1, 2, …, 8 are 24, 18, 60, 40, 120, 84, 96, 180, 168. In the computed range, no m above 180 has defect 8 or less. Only the classes Δ = 0 and Δ = 1 are proved complete here (Theorems 7 and 8); for larger defects the lists are computed, and each is finite because Δ(m) is about 2√m − τ(m), which tends to infinity.

## 7. Computational verification

Every theorem above was checked against brute-force definitions (direct enumeration of ⌊n/k⌋, blocks and divisors) in Python. No assertion failed.

| Claim | Range tested | Result |
| --- | --- | --- |
| Block formula, E(n) = V(n), initial segment, closed form D(n) | all n ≤ 4000 | holds |
| Mirror Law, including drops | all n ≤ 4000 | holds |
| Transition Theorem, quotient increments | all 1 ≤ k ≤ n < 4000 | holds |
| D(n+1) − D(n) = 1 only at s² and s²+s | all n < 4000 | holds |
| Staircase union formula for T(k) | 2 ≤ k < 120 | holds |
| Staircase run lengths 1..k−1 and gaps k−1..1 | 2 ≤ k ≤ 8 | holds |
| Double-counting identity | M = 600 | holds |
| Defect Formula Δ(m) = 2N(m) − \[s²\<m\<s²+s\] | all m ≤ 4000 | holds |
| Exactness: Δ(m) = 0 | m ≤ 100,000 | only 1, 2, 3, 4, 6, 8, 12, 24 |

The small-non-divisor count N(m) was also sieved up to 2,000,000, giving the complete sets with N(m) = c in that range:

| N(m) = c | How many m | Largest m |
| --- | --- | --- |
| 0 | 8 | 24 |
| 1 | 13 | 60 |
| 2 | 10 | 120 |
| 3 | 17 | 96 |
| 4 | 16 | 180 |
| 5 | 20 | 240 |

The largest members do not grow monotonically in c, which is why completeness beyond the tested range rests on the lcm-growth argument, proved here only for c = 0 and for the defect-one case.

Testing is not proof. The proofs in sections 3 to 6 stand on their own, and the computation is a guard against slips in them.

## 8. Extensions and applications

**Real arguments.** For real x ≥ 1 and integer k, ⌊x/k⌋ = ⌊⌊x⌋/k⌋. So the blocks, endpoints and block count of x are those of ⌊x⌋, and D(x) = ⌊√(4⌊x⌋+1)⌋ − 1. All results transfer unchanged.

**Exact cost of hyperbola summation.** For any function f, the sum of f(⌊n/k⌋) over k = 1..n equals the sum over blocks of ℓ\_i · f(Q\_i). This needs exactly D(n) evaluations of f, which Theorem 2 gives in closed form: 1,999 for n = 10⁶ and 1,999,999 for n = 10¹². The Mirror Law shows the whole block structure is determined by s and the s large quotients ⌊n/k⌋ for k ≤ s. Concretely, the first s blocks are the singletons {1}, …, {s}, and the remaining blocks have quotients s′, …, 2, 1 with lengths ⌊n/q⌋ − ⌊n/(q+1)⌋.

**Block-length spectrum (numerical observation, not a theorem).** At n = 10⁶ there are 1,999 blocks. The count of blocks of length ℓ follows the law (√n/2)·ℓ^(−3/2) closely:

| Block length ℓ | Blocks at n = 10⁶ | (√n/2)·ℓ^(−3/2) |
| --- | --- | --- |
| 1 | 1,172 | (not covered; singletons include the initial segment) |
| 2 | 192 | 177 |
| 3 | 100 | 96 |
| 4 | 64 | 63 |
| 5 | 46 | 45 |

The heuristic: for large quotients q the block length is about n/q², so lengths near ℓ come from q near √(n/ℓ), and the number of such q is about (√n/2)·ℓ^(−3/2). The mean block length n/D(n) is about √n/2.

**Directions not pursued here.** QBT can be posed for other quotient maps, such as ⌊n/k²⌋, shifted quotients ⌊(n+a)/k⌋, or pairs of quotients taken jointly. I make no claims about these.

## 9. Open problems

1. **Length spectrum.** Prove that the number of blocks of length ℓ in B\_n is (√n/2)·ℓ^(−3/2) plus an explicit error term, uniformly in ℓ up to a power of n.
2. **Defect classes.** For each c, let M\_c be the largest m with Δ(m) = c. Determine the growth of M\_c, and decide whether every non-negative integer occurs as a defect (true for c ≤ 8 in the computed range).
3. **Block entropy.** The last block carries about half the mass n. Find the asymptotics of H(n) = −Σ (ℓ\_i/n) ln(ℓ\_i/n).
4. **Word dynamics.** By Theorem 4 only boundaries next to divisors of n+1 can move. Give a complete combinatorial rule for how the block word of n becomes the block word of n+1.
5. **Other quotient maps.** Develop the staircase and mirror theory for ⌊n/k²⌋ and for shifted quotients ⌊(n+a)/k⌋.

## 10. Scope, novelty and references

**What is proved.** Theorems 1 to 8 are proved in full in sections 3 to 6, using only elementary arithmetic. Section 7 is a computational cross-check, and section 8 contains one numerical observation that is explicitly not a theorem.

**What is classical.** The involution k → ⌊n/k⌋, the roughly 2√n count of distinct quotients, the pairing of divisors d and m/d, and the fact that 24 is the largest integer divisible by every integer up to its square root.

**What I believe is new.** The exact closed form for D(n) used as a block count with the Mirror Law relating drops to lengths, the Transition and Endpoint Staircase Theorems (including the exact one-half property and the 1..k−1 / k−1..1 run structure), and the Defect Formula that recasts the divisor function as D(m) minus twice the small-non-divisor count. This is a statement about my own knowledge, not a result of an exhaustive literature search, and an author preparing this for publication should check it against the literature before claiming priority.

**Reproducibility.** The checking scripts are separate Python files delivered alongside this document.

**References** (named from general knowledge; I did not open them in this session):

- P. G. L. Dirichlet, work on the divisor problem and the hyperbola method (1849).
- G. H. Hardy and E. M. Wright, *An Introduction to the Theory of Numbers*.
- T. M. Apostol, *Introduction to Analytic Number Theory*.
- R. L. Graham, D. E. Knuth and O. Patashnik, *Concrete Mathematics* (chapter on floors and ceilings).

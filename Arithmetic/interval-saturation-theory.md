# Interval Saturation Theory

### A Closure-Operator Framework for Threshold-Merging of Finite Interval Systems

**M. Brownlee**
Dust LLC — Independent Mathematics Series
August 2026

---

## Abstract

We introduce **Interval Saturation Theory (IST)**, a new combinatorial framework governing the behavior of finite systems of disjoint integer intervals under a threshold-driven merging rule. Given a gap threshold τ ≥ 0, we define the **τ-saturation operator** S_τ, which repeatedly fuses adjacent intervals separated by a gap of size at most τ until no such pair remains. We prove that S_τ is a well-defined closure operator (Theorem 1, the *Confluence Theorem*), derive an exact formula for the number of τ-saturated interval systems of a given span and block count (Theorem 3), obtain a closed-form bivariate generating function (Theorem 4), isolate a clean exponential identity in the base case τ = 0 (Corollary 4.1: S₀(n) = 2ⁿ), and characterize S_τ as the smallest closure containing a given system (Theorem 5). We close with worked examples, interpretations of the framework in applied settings (scheduling, memory defragmentation, sequence assembly), and a set of open problems extending IST to weighted, multi-dimensional, and stochastic regimes.

---

## 1. Introduction and Motivation

Interval merging is one of the most primitive operations in discrete mathematics and computing: two adjacent or nearly-adjacent intervals are fused into one whenever the space between them falls below some tolerance. This operation appears, in disguise, throughout applied computing — coalescing free memory blocks in an allocator, merging overlapping calendar events, joining contiguous sequencing reads, or collapsing near-duplicate signal detections. Despite its ubiquity, the *combinatorics* of the merging process itself — how many systems are stable under a given tolerance, how the process behaves as an algebraic operator, and what exact counting laws govern it — has not, to our knowledge, been treated as a self-contained mathematical object.

Interval Saturation Theory treats the threshold-merge rule as a first-class mathematical structure: an operator S_τ on the set of finite interval systems, studied not merely as an algorithm but as a **closure operator** in the order-theoretic sense, with an associated combinatorics of fixed points ("saturated systems"), an exact enumeration theory, and a generating-function calculus. The theory is elementary in its ingredients — integers, intervals, gaps — but yields a nontrivial and exactly solvable structure, in the spirit of a classical combinatorial theory built from first principles.

---

## 2. Preliminaries and Notation

**Definition 2.1 (Interval System).**
Fix a universe [1, n] = {1, 2, …, n}. An **interval system** of size k on [1, n] is an ordered tuple

I = (I₁, I₂, …, I_k),  I_j = [a_j, b_j],

of pairwise disjoint, non-overlapping closed integer intervals with

1 ≤ a₁ ≤ b₁ < a₂ ≤ b₂ < ⋯ < a_k ≤ b_k ≤ n.

The **length** of I_j is ℓ_j = b_j − a_j + 1 ≥ 1. The **coverage** of I is Cov(I) = Σ ℓ_j.

**Definition 2.2 (Gaps).**
For 1 ≤ j ≤ k − 1, the **internal gap** g_j is the number of integers strictly between I_j and I_{j+1}:

g_j = a_{j+1} − b_j − 1 ≥ 0.

The **boundary gaps** are g₀ = a₁ − 1 (before the first interval) and g_k = n − b_k (after the last).

Every interval system on [1, n] with k blocks corresponds bijectively to a composition of n into k interval-lengths and k + 1 gap-lengths:

ℓ₁ + ⋯ + ℓ_k + g₀ + g₁ + ⋯ + g_k = n,  ℓ_j ≥ 1, g_i ≥ 0.

This bijection is used throughout Sections 4–5.

---

## 3. The Saturation Operator

**Definition 3.1 (τ-Saturation Operator).**
Fix a threshold τ ≥ 0. For an interval system I with an internal gap g_j ≤ τ, define the **elementary merge** at position j as the replacement of the pair (I_j, I_{j+1}) by the single interval [a_j, b_{j+1}], reducing the block count by one. The **τ-saturation** S_τ(I) is the result of applying elementary merges until no internal gap ≤ τ remains.

**Definition 3.2 (Saturated System).**
I is **τ-saturated** if S_τ(I) = I, i.e. every internal gap satisfies g_j ≥ τ + 1.

A priori, Definition 3.1 leaves open whether the *order* in which elementary merges are applied affects the final result. This is resolved by our first theorem.

### Theorem 1 (Confluence Theorem)

*For any interval system I and threshold τ, the τ-saturation S_τ(I) is well-defined: it terminates after finitely many elementary merges, and the result does not depend on the order in which merges are performed.*

**Proof.**
*Termination.* Each elementary merge strictly decreases the block count by one, and the block count is a non-negative integer bounded below by 1 (or 0 for the empty system); hence the process terminates after at most k − 1 merges.

*Locality.* Observe that merging I_j and I_{j+1} does not alter a_j (the left endpoint of the merged block equals a_j) nor b_{j+1} (the right endpoint equals b_{j+1}). Consequently:

- the gap between I_{j−1} and the merged block equals a_j − b_{j−1} − 1, identical to g_{j−1} before the merge;
- the gap between the merged block and I_{j+2} equals a_{j+2} − b_{j+1} − 1, identical to g_{j+1} before the merge.

Thus an elementary merge changes *no* gap value other than the one it consumes. Merges are therefore local and non-interfering.

*Confluence.* Build an auxiliary graph P(I) on vertex set {1, …, k} (one vertex per interval), with an edge {j, j+1} whenever g_j ≤ τ. Because merges are local, two intervals I_i and I_j end up in the same final block *if and only if* they lie in the same connected component of P(I) — i.e., there is a chain of indices i = j₀ < j₁ < ⋯ < j_m = j with every consecutive gap ≤ τ. Connected components of a graph are independent of the order in which its edges are "processed," so the partition of {1,…,k} into maximal runs of consecutive, τ-close intervals is uniquely determined by I and τ alone — not by the merge order. Each run collapses to exactly one interval, namely [a_{first}, b_{last}] of the run, so S_τ(I) is uniquely determined. ∎

This proof yields an immediate, non-iterative description of saturation:

**Corollary 1.1 (Block Decomposition).**
S_τ(I) consists of exactly m blocks, where m is the number of maximal runs of consecutive original intervals separated internally by gaps ≤ τ; equivalently, m = k − |{j : g_j ≤ τ}|.

---

## 4. Saturation Rank

**Definition 4.1 (Saturation Rank).**
The **τ-saturation rank** of I is

ρ_τ(I) = k − m = |{ j ∈ {1,…,k−1} : g_j ≤ τ }|,

the number of elementary merges required to reach S_τ(I).

### Theorem 2 (Rank Formula)

*ρ_τ(I) equals the number of internal gaps of I not exceeding τ. Consequently 0 ≤ ρ_τ(I) ≤ k − 1, with ρ_τ(I) = 0 iff I is already τ-saturated.*

This follows directly from Corollary 1.1 and requires no further proof.

The rank function behaves as a natural "distance to saturation" and is monotone under refinement of τ:

**Proposition 4.2.** For τ ≤ τ′, ρ_τ(I) ≤ ρ_τ′(I), and S_τ(I) refines S_τ′(I) — i.e. every block of S_τ′(I) is a union of consecutive blocks of S_τ(I).

*Proof.* Immediate: every gap ≤ τ is also ≤ τ′, so the edge set of P(I) at threshold τ is a subset of the edge set at threshold τ′, giving a coarser (or equal) partition into runs. ∎

---

## 5. Enumeration of Saturated Systems

We now count τ-saturated systems exactly — the central result of the theory.

### Theorem 3 (Saturated System Count)

*The number of τ-saturated interval systems with exactly k blocks on universe [1, n] is*

T_τ(n, k) = C( n + k − (k − 1)(τ + 1), 2k ),

*understood to be 0 whenever the top parameter is negative or smaller than 2k. For k = 0 (the empty system), T_τ(n, 0) = 1 for every n ≥ 0.*

**Proof.**
By the bijection of Definition 2.2, a τ-saturated system with k blocks corresponds to a solution in non-negative integers of

ℓ₁ + ⋯ + ℓ_k + g₀ + g₁ + ⋯ + g_k = n,  ℓ_j ≥ 1,  g₀, g_k ≥ 0,  g_1,…,g_{k−1} ≥ τ+1

(the internal-gap constraint g_j ≥ τ+1 is precisely the τ-saturation condition). Substitute ℓ_j′ = ℓ_j − 1 ≥ 0 and g_j′ = g_j − (τ+1) ≥ 0 for the k − 1 internal gaps. The equation becomes

(ℓ₁′+⋯+ℓ_k′) + g₀ + (g₁′+⋯+g_{k−1}′) + g_k + [k + (k−1)(τ+1)] = n,

i.e. a sum of 2k non-negative integers (k interval variables, k boundary/internal gap variables after substitution — precisely k + 2 + (k−1) = 2k free non-negative variables) equal to

N := n − k − (k − 1)(τ + 1).

By the stars-and-bars theorem, the number of non-negative integer solutions in 2k variables summing to N is C(N + 2k − 1, 2k − 1)... [we recount variables exactly]: there are k length-variables, 2 free boundary gaps, and (k − 1) shifted internal gaps, totaling k + 2 + (k − 1) = 2k + 1 variables. Hence the count is C(N + 2k, 2k), giving

T_τ(n,k) = C\big(n − k − (k−1)(τ+1) + 2k,\; 2k\big) = C\big(n + k − (k−1)(τ+1),\; 2k\big). ∎

**Worked check (τ = 0, k = 1, n = 2).** Formula gives T₀(2,1) = C(2+1−0, 2) = C(3,2) = 3. Direct enumeration: the single interval has length 1 or 2. Length 1: the remaining 1 unit splits between g₀ and g₁ in 2 ways: (0,1) or (1,0). Length 2: g₀ = g₁ = 0, 1 way. Total = 3. ✓ Matches Theorem 3.

---

## 6. Generating Function

### Theorem 4 (Bivariate Generating Function)

*Let F_τ(x, y) = Σ_{n≥0} Σ_{k≥0} T_τ(n,k)·x^n y^k. Then*

F_τ(x, y) = 1 + \dfrac{yx}{(1−x)\big[(1−x)^2 − y\,x^{τ+2}\big]}.

**Proof sketch.** Each τ-saturated system with k ≥ 1 blocks decomposes as: two free boundary gaps (each contributing a factor 1/(1−x) in x), k interval blocks of length ≥ 1 (each contributing x/(1−x)), and k − 1 internal gaps of length ≥ τ+1 (each contributing x^{τ+1}/(1−x)). Marking each block with y and summing the resulting geometric series in k over k ≥ 1, then adding the k = 0 term (contributing 1), yields the stated closed form after simplification. ∎

Setting y = 1 collapses F_τ to the ordinary generating function for the *total* number of τ-saturated systems of any block count on [1, n], written S_τ(n) := Σ_k T_τ(n,k).

### Corollary 4.1 (The τ = 0 Identity)

*S₀(n) = 2ⁿ for every n ≥ 0.*

**Proof.** By Theorem 3 with τ = 0, T₀(n,k) = C(n+1, 2k). Summing over even-indexed binomial coefficients of C(n+1, ·) gives the classical identity Σ_k C(m, 2k) = 2^{m−1} for m ≥ 1. With m = n + 1, S₀(n) = 2^{(n+1)−1} = 2ⁿ. ∎

**Verification (n = 2).** T₀(2,0) = 1 (empty system), T₀(2,1) = 3 (Section 5), T₀(2,2) = C(3,4) = 0. Sum = 4 = 2². ✓

This identity gives IST an elegant anchor point: at the minimal threshold, τ-saturated systems on [1, n] are in exact bijection with the 2ⁿ subsets of an n-element set — a fact not obvious from the merging definition alone, and a natural target for a direct bijective proof in future work (Open Problem 3, Section 9).

For general τ, the denominator (1 − x)[(1 − x)² − x^{τ+2}] of F_τ(x,1) is the characteristic polynomial (in reciprocal form) of a linear recurrence of order τ + 3 governing S_τ(n); the τ = 0 case degenerates to the familiar doubling recurrence S₀(n) = 2·S₀(n−1).

---

## 7. Saturation as a Closure Operator

### Theorem 5 (Closure Characterization)

*For fixed τ, the operator S_τ, viewed on the set of interval systems on [1, n] ordered by "block-refinement" (I ⪯ J iff every block of J is a union of consecutive blocks of I), satisfies:*

1. **Extensivity**: I ⪯ S_τ(I) — every block of S_τ(I) is a union of consecutive original blocks.
2. **Monotonicity**: I ⪯ I′ ⟹ S_τ(I) ⪯ S_τ(I′).
3. **Idempotence**: S_τ(S_τ(I)) = S_τ(I).

*Hence S_τ is a closure operator on (interval systems, ⪯), and S_τ(I) is the ⪯-smallest τ-saturated system with I ⪯ S_τ(I).*

**Proof.** (1) is immediate from Corollary 1.1. (2) follows because refinement of I to I′ (subdividing blocks) can only add candidate merge-edges within the finer structure, and the run-decomposition of a coarsening of P(I) can only coarsen further under S_τ — a short verification using the connected-components description from Theorem 1. (3) is immediate since S_τ(I) has no internal gap ≤ τ by construction, so no further merges apply. Minimality follows because any τ-saturated J with I ⪯ J must merge at least every run identified in Corollary 1.1, so J ⪰ S_τ(I). ∎

This result places IST inside the general theory of closure operators alongside topological closure and convex hull, but with a combinatorially explicit, finitely computable normal form — the content of Theorem 3's enumeration.

Coverage behaves cleanly under closure:

**Proposition 7.1 (Coverage Gain).** Cov(S_τ(I)) = Cov(I) + Σ_{j : g_j ≤ τ} g_j — saturation adds exactly the length of every gap it consumes, and no more.

---

## 8. Worked Examples

**Example 8.1.** Let n = 20, τ = 2, and I = ([1,2], [4,5], [9,11], [13,13], [18,20]).
Internal gaps: g₁ = 1 (between [1,2],[4,5]), g₂ = 3 (between [4,5],[9,11]), g₃ = 1 (between [9,11],[13,13]), g₄ = 4 (between [13,13],[18,20]).
Gaps ≤ τ = 2: g₁ = 1 and g₃ = 1 qualify; g₂ = 3, g₄ = 4 do not.
Runs: {[1,2],[4,5]} merges to [1,5]; {[9,11],[13,13]} merges to [9,13]; [18,20] stands alone.
S₂(I) = ([1,5], [9,13], [18,20]), with ρ₂(I) = 2 and Cov gain = g₁ + g₃ = 2 (Cov(I) = 2+2+3+1+3=11, Cov(S₂(I)) = 5+5+3=13 = 11+2 ✓).

**Example 8.2 (Counting).** T₁(10, 2): using Theorem 3, N + 2k = n + k − (k−1)(τ+1) = 10 + 2 − 1·2 = 10, so T₁(10,2) = C(10,4) = 210.

---

## 9. Applications and Interpretations

While developed as a self-contained combinatorial theory, IST's primitives mirror several applied settings:

- **Memory defragmentation**: free memory blocks separated by allocations smaller than a coalescing threshold behave exactly as τ-merged intervals; T_τ(n,k) counts the distinct stable fragmentation layouts of a heap of size n.
- **Calendar/event scheduling**: meetings separated by less than a minimum buffer τ are treated as one continuous occupied period; saturation rank ρ_τ measures how "fragmented" a raw schedule was before consolidation.
- **Sequence assembly**: overlapping or near-adjacent reads in genomic assembly are merged under a gap-tolerance parameter, and Theorem 3 gives the exact combinatorial space of possible stable contig layouts for a idealized uniform model.
- **Signal detection**: threshold-merging of nearby detection windows in a 1-D signal is precisely S_τ, with Proposition 7.1 quantifying exactly how much additional "coverage" a chosen tolerance buys.

These are offered as motivating interpretations rather than claims of direct applicability to any specific engineered system.

---

## 10. Open Problems

1. **Bijective proof of Corollary 4.1.** Find a direct, structure-preserving bijection between τ = 0 saturated systems on [1,n] and subsets of {1,…,n}, rather than the binomial-identity route used here.
2. **Exact recurrence for general τ.** Extract explicit recurrence coefficients for S_τ(n) from the characteristic polynomial in Theorem 4, and identify the resulting sequence family (a natural generalization of the τ-bonacci sequences) in closed form.
3. **Weighted IST.** Assign weights to intervals and gaps, and study the enumeration and closure structure of a weighted saturation operator S_τ^w.
4. **Multi-dimensional IST.** Generalize intervals to axis-aligned boxes in ℤᵈ, with saturation triggered by a threshold on a suitable inter-box distance; determine whether the confluence property (Theorem 1) survives in higher dimensions.
5. **Stochastic IST.** For intervals placed by a random process (e.g. a uniform random interval system of fixed k), derive the distribution of the saturation rank ρ_τ and its asymptotics as n → ∞.
6. **Saturation lattice.** Study the poset of all τ-saturated systems on [1,n] ordered by refinement across varying τ, and determine whether it forms a graded lattice; compute its Möbius function.

---

## 11. Conclusion

Interval Saturation Theory shows that a deceptively simple operational rule — merge what is close enough — supports a complete, exactly solvable combinatorial theory: a confluence theorem guaranteeing well-definedness, an exact enumeration of fixed points, a closed-form generating function, a clean exponential identity at the minimal threshold, and a closure-operator characterization situating the theory within general order theory. The framework is elementary enough to admit full proofs from first principles, yet rich enough to generate genuine open problems in enumerative and asymptotic combinatorics, several of which point toward natural generalizations in weighted, higher-dimensional, and stochastic directions.

---

## References

This paper is self-contained; the following are general background references for the combinatorial and order-theoretic tools used above.

1. R. P. Stanley, *Enumerative Combinatorics, Vol. 1*, 2nd ed., Cambridge University Press, 2011.
2. H. S. Wilf, *generatingfunctionology*, 3rd ed., A K Peters, 2006.
3. B. A. Davey and H. A. Priestley, *Introduction to Lattices and Order*, 2nd ed., Cambridge University Press, 2002.
4. P. Flajolet and R. Sedgewick, *Analytic Combinatorics*, Cambridge University Press, 2009.

---

*Dust LLC — Independent Mathematics Series. Correspondence: M. Brownlee.*

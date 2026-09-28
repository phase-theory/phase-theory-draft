# Ultrafinitism and the Boundaries of Gödel’s Incompleteness Theorems

**A White Paper on Strict Finitism, Representability, Bounded Proof, and the Limit Character of Gödelian Incompleteness**

---

## Abstract

Ultrafinitism, or strict finitism, denies that the natural numbers constitute a completed infinite totality. It accepts only numbers that can be explicitly constructed, inscribed, or otherwise retained below an operative resource bound. This stance undercuts some of the assumptions ordinarily used in Gödel’s incompleteness theorems, especially the unbounded quantification over proofs and the global representability of syntactic operations. However, ultrafinitism does not automatically refute Gödel’s theorems. The theorems apply whenever a theory is recursively enumerable, consistent, and strong enough to internalize a sufficient amount of syntax, for example by containing or interpreting Robinson arithmetic \(Q\). The decisive boundary is not induction alone, but the combination of effective enumerability, syntactic coding, self-reference, and unbounded closure.

This paper develops a precise boundary analysis. We isolate the minimal Gödelian machinery, identify the points at which ultrafinitist restrictions can block it, and introduce a resource-bounded framework in which fixed finite proof bounds evade classical incompleteness while any uniform unbounded limit restores it. We show that bounded fragments may prove their own bounded consistency and may even be complete and decidable, but only by surrendering most of standard number theory. Gödel’s theorems emerge as limit theorems: they govern the passage from finite, bounded mathematical practice to a completed, recursively enumerable arithmetic theory.

**Keywords:** ultrafinitism, strict finitism, Gödel incompleteness, Robinson arithmetic, bounded arithmetic, representability, proof theory, feasible mathematics, diagonalization, bounded consistency.

---

## 1. Introduction

Classical arithmetic assumes that the natural numbers form a completed infinite totality:

\[
\mathbb{N}=\{0,1,2,3,\dots\}.
\]

Quantifiers such as

\[
\forall x\in\mathbb{N}\quad \text{and}\quad \exists x\in\mathbb{N}
\]

are interpreted as ranging over this totality. Gödel’s incompleteness theorems are theorems about theories that live inside, or at least simulate, this unbounded universe. They depend on the ability to code formulas, proofs, substitutions, and derivations by natural numbers, and then to reason about those codes without imposing a fixed upper bound.

Ultrafinitism rejects this background assumption. In its strict form, it denies that one is entitled to the totality of all natural numbers. One accepts only those numbers that can actually be constructed, written down, computed, or otherwise held within some resource bound. A typical ultrafinitist attitude is not merely that very large numbers are impractical, but that the assertion “there exists a natural number beyond every bound” lacks legitimate mathematical content unless tied to a concrete construction.

This has direct consequences for Gödel’s theorems. The Gödel sentence is usually a \(\Pi^0_1\) sentence of the form

\[
G_T \equiv \forall p\,\neg \operatorname{Prf}_T(p,\ulcorner G_T\urcorner),
\]

saying that no natural number \(p\) codes a proof of \(G_T\) in \(T\). The universal quantifier over all possible proof codes is precisely the kind of unbounded totality that strict finitism calls into question.

Nevertheless, the situation is subtle. Gödelian incompleteness does not require full Peano arithmetic. It does not even require induction in its strongest form. Robinson arithmetic \(Q\), which lacks induction entirely, is already essentially undecidable. Therefore, merely rejecting induction does not suffice to escape incompleteness. The real boundary lies in the theory’s ability to support an internal theory of syntax: coding, substitution, proof verification, and self-reference.

The central claim of this paper is the following.

> **Thesis.** Gödel’s incompleteness theorems are not invalidated by ultrafinitism; rather, they delineate the threshold at which ultrafinitist mathematics becomes strong enough to support effective self-reference. Fixed bounded fragments can evade classical incompleteness, but only by becoming local, non-uniform, and mathematically impoverished. Any strict finitist framework that uniformly recovers enough syntax and proof theory to form an unbounded recursively enumerable theory re-enters the domain of Gödelian incompleteness.

To make this precise, we proceed as follows. Section 2 isolates the Gödel apparatus. Section 3 analyzes the commitments of strict finitism. Section 4 formulates a Gödel-threshold criterion. Section 5 develops a resource-bounded incompleteness framework. Section 6 classifies escape routes and their costs. Section 7 presents a stratified, limit-theoretic interpretation of Gödel’s theorems. Section 8 discusses the consequences for number theory. Section 9 concludes.

---

## 2. The Gödel Apparatus

### 2.1 Syntax, coding, and proof predicates

Let \(L\) be a finite first-order language for arithmetic, for example

\[
L=\{0,S,+,\times\}.
\]

The standard numerals are

\[
\overline{0}=0,\qquad 
\overline{1}=S0,\qquad 
\overline{2}=SS0,\qquad 
\overline{n}=S^n0.
\]

A Gödel coding is an effective injection

\[
\ulcorner\cdot\urcorner:\operatorname{Expr}(L)\to\mathbb{N}
\]

assigning natural numbers to symbols, terms, formulas, sequences of formulas, and proofs. The precise coding is flexible. Classical Gödel coding uses prime factorization:

\[
\ulcorner a_0,a_1,\dots,a_{k-1}\urcorner
=
2^{a_0+1}3^{a_1+1}5^{a_2+1}\cdots p_{k-1}^{a_{k-1}+1}.
\]

More economical codings use binary strings, pairing functions, or sequence codings based on the Chinese remainder theorem. The important point is not the exact coding but that certain syntactic operations become primitive recursive functions on codes.

Typical primitive recursive syntactic functions include:

\[
\operatorname{Concat}(x,y)=\ulcorner \text{concatenation of expressions coded by }x,y\urcorner,
\]

\[
\operatorname{Sub}(e,n)=\ulcorner \varphi(\overline{n})\urcorner
\quad\text{if } e=\ulcorner \varphi(v)\urcorner,
\]

\[
\operatorname{Neg}(e)=\ulcorner \neg\varphi\urcorner
\quad\text{if } e=\ulcorner\varphi\urcorner.
\]

For a recursively enumerable theory \(T\), the proof predicate

\[
\operatorname{Prf}_T(p,x)
\]

holds iff \(p\) codes a valid \(T\)-proof of the formula with code \(x\). If \(T\) is recursively axiomatized, \(\operatorname{Prf}_T\) is primitive recursive or at least recursive. The usual provability predicate is

\[
\operatorname{Prov}_T(x)\equiv \exists p\,\operatorname{Prf}_T(p,x).
\]

The consistency of \(T\) can then be expressed as

\[
\operatorname{Con}(T)\equiv \neg \operatorname{Prov}_T(\ulcorner 0=1\urcorner).
\]

Equivalently,

\[
\operatorname{Con}(T)\equiv \forall p\,\neg \operatorname{Prf}_T(p,\ulcorner 0=1\urcorner).
\]

This is already an unbounded universal statement.

---

### 2.2 Representability and the diagonal lemma

A relation \(R\subseteq\mathbb{N}^k\) is representable in a theory \(T\) if there is a formula \(\rho(x_1,\dots,x_k)\) such that, for every tuple \(\vec n\in\mathbb{N}^k\),

\[
R(\vec n)\quad\Longrightarrow\quad T\vdash \rho(\overline{\vec n}),
\]

and, for decidable relations,

\[
\neg R(\vec n)\quad\Longrightarrow\quad T\vdash \neg\rho(\overline{\vec n}).
\]

A function \(f:\mathbb{N}^k\to\mathbb{N}\) is representable if there is a formula \(\varphi(\vec x,y)\) such that

\[
f(\vec n)=m
\quad\Longrightarrow\quad
T\vdash \varphi(\overline{\vec n},\overline m),
\]

and preferably

\[
T\vdash \exists!y\,\varphi(\overline{\vec n},y).
\]

Robinson arithmetic \(Q\) is weak, but it represents all primitive recursive functions in the numeralwise sense required for Gödel coding. This is one reason \(Q\) is already sufficient for essential undecidability.

The diagonal lemma is the formal mechanism producing self-reference.

Let \(\operatorname{Sub}(e,e)\) be the primitive recursive function that, given the code of a formula \(\varphi(v)\), returns the code of \(\varphi(\overline e)\). Define

\[
d(e)=\operatorname{Sub}(e,e).
\]

Given a formula \(\psi(x)\), form

\[
\theta(x)\equiv \psi(d(x)).
\]

Let

\[
m=\ulcorner \theta(x)\urcorner.
\]

Then the diagonal sentence is

\[
G\equiv \theta(\overline m).
\]

Its code is

\[
\ulcorner G\urcorner
=
d(m).
\]

Since \(d\) is representable, the base theory proves

\[
G\leftrightarrow \psi(\ulcorner G\urcorner).
\]

This is the diagonal lemma.

The crucial observation is that the diagonal lemma requires an internal representation of substitution. If a theory cannot represent substitution, or if the ultrafinitist refuses to accept the numbers produced by the substitution function, then the Gödel construction cannot be carried out inside that theory.

---

### 2.3 First incompleteness theorem in minimal form

A standard form of the first incompleteness theorem is the following.

**Theorem 2.1. Rosser–Gödel Incompleteness.**  
Let \(T\) be a consistent, recursively enumerable extension of Robinson arithmetic \(Q\). Then there is a sentence \(R_T\) such that

\[
T\nvdash R_T
\]

and

\[
T\nvdash \neg R_T.
\]

In particular, \(T\) is incomplete.

The original Gödel version required \(\omega\)-consistency and produced a sentence \(G_T\) satisfying informally

\[
G_T \equiv \text{“\(G_T\) is not provable in \(T\)”}.
\]

Rosser’s improvement requires only consistency by comparing least proofs of a sentence and its negation.

The theorem does not require full induction. It does require:

1. an effective proof system;
2. a coding of syntax;
3. representability of basic syntactic operations;
4. enough arithmetic to diagonalize;
5. consistency.

Thus, the first incompleteness theorem is not primarily a theorem about induction. It is a theorem about effective self-reference.

---

### 2.4 Second incompleteness theorem and derivability conditions

The second incompleteness theorem is more delicate. A common formulation uses the Hilbert–Bernays–Löb derivability conditions. Let

\[
\operatorname{Prov}_T(x)
\]

be a provability predicate for \(T\). The conditions are:

\[
\text{(D1)}\quad
T\vdash \varphi
\quad\Longrightarrow\quad
T\vdash \operatorname{Prov}_T(\ulcorner\varphi\urcorner),
\]

\[
\text{(D2)}\quad
T\vdash 
\operatorname{Prov}_T(\ulcorner\varphi\to\psi\urcorner)
\to
\bigl(
\operatorname{Prov}_T(\ulcorner\varphi\urcorner)
\to
\operatorname{Prov}_T(\ulcorner\psi\urcorner)
\bigr),
\]

\[
\text{(D3)}\quad
T\vdash
\operatorname{Prov}_T(\ulcorner\varphi\urcorner)
\to
\operatorname{Prov}_T(\ulcorner \operatorname{Prov}_T(\ulcorner\varphi\urcorner)\urcorner).
\]

If \(T\) is sufficiently strong, recursively enumerable, consistent, and satisfies these conditions, then

\[
T\nvdash \operatorname{Con}(T).
\]

The second theorem therefore depends not merely on the ability to express consistency, but on the theory’s ability to reason about its own provability predicate in a sufficiently coherent way.

Weak theories may fail the derivability conditions. Some may prove local or bounded consistency statements. Some carefully weakened systems may even prove formal statements resembling their own consistency because they do not satisfy the full Hilbert–Bernays–Löb framework. This is not a refutation of Gödel’s second theorem but an indication that its boundary lies in the derivability conditions.

---

## 3. Ultrafinitism as a Mathematical Position

### 3.1 Strict finitist commitments

Ultrafinitism is not a single formal theory. It is a family of positions united by the rejection of the completed infinite totality \(\mathbb{N}\). We can isolate several core commitments.

**SF1. Construction restriction.**  
A number is accepted only if it can be constructed, inscribed, computed, or otherwise made available within an operative resource bound.

**SF2. Bounded quantification.**  
Unbounded quantifiers over all natural numbers are not accepted as meaningful unless they can be reduced to bounded or explicitly constructible claims.

**SF3. Schemas are not completed totalities.**  
An axiom schema is not automatically accepted as a completed infinite set of axioms. One accepts particular instances, or instances below a bound, but not necessarily the schema as a finished object.

These commitments affect arithmetic in several ways.

First, the ordinary induction schema

\[
\bigl(\varphi(0)\wedge \forall x(\varphi(x)\to\varphi(Sx))\bigr)
\to
\forall x\,\varphi(x)
\]

is suspect because its conclusion ranges over all natural numbers. A strict finitist may accept bounded induction:

\[
\bigl(\varphi(0)\wedge \forall x<b\,(\varphi(x)\to\varphi(Sx))\bigr)
\to
\varphi(b),
\]

but only when \(b\) is itself accepted.

Second, functions whose values grow rapidly, such as exponentiation, factorial, or Ackermann-type functions, may not be accepted as total. One may accept particular values, for example

\[
2^{10}=1024,
\]

but reject the totality of the function

\[
n\mapsto 2^n.
\]

Third, semantic notions involving all models, all subsets of \(\mathbb{N}\), or all formulas are likewise suspect.

---

### 3.2 The feasibility predicate paradox

One natural way to formalize ultrafinitist intuition is to introduce a predicate

\[
F(x)
\]

meaning “\(x\) is feasible” or “\(x\) is constructible.” However, a serious difficulty appears immediately.

Suppose the theory proves:

\[
F(0)
\]

and

\[
\forall x\,(F(x)\to F(Sx)).
\]

If the theory also has induction for formulas involving \(F\), then by induction one obtains

\[
\forall x\,F(x).
\]

This collapses feasibility into the full set of natural numbers and defeats the ultrafinitist motivation.

Therefore, any coherent formal treatment of feasibility must reject at least one of the following:

1. \(F(0)\);
2. closure under successor;
3. induction for \(F\);
4. classical bivalence for feasibility;
5. the sharp definability of \(F\).

This is a formal version of the sorites problem for feasible numbers. It shows why ultrafinitism cannot simply be obtained by adding a feasibility predicate to ordinary arithmetic.

---

### 3.3 What strict finitism loses

Strict finitism avoids certain Gödelian assumptions, but the price is high. Much of standard number theory depends on unbounded principles.

For example:

1. **Total exponentiation.**  
   The statement

   \[
   \forall x\,\exists y\,(y=2^x)
   \]

   may be rejected.

2. **Unbounded induction.**  
   General induction over all natural numbers is unavailable.

3. **Infinitude of primes as a completed assertion.**  
   Euclid’s proof can be accepted locally: given a finite list of primes, one can construct another, provided the construction is feasible. But the completed assertion “there are infinitely many primes” may be rejected as a totality claim.

4. **Arbitrary sequence coding.**  
   Gödel coding of sequences often uses exponentiation or the Chinese remainder theorem. A strict finitist may accept finite instances but not the general coding theorem.

5. **The set of all formulas.**  
   Diagonalization presupposes that formulas form a completed enumerable domain. A strict finitist may instead treat formulas as concrete inscriptions available only up to some bound.

Thus, ultrafinitism does not merely weaken arithmetic. It changes the character of arithmetic from a global theory of \(\mathbb{N}\) to a collection of bounded, local practices.

---

## 4. The Gödel Threshold

### 4.1 The central criterion

We can now formulate the boundary condition.

**Gödel Threshold Criterion.**  
A theory \(T\) is subject to classical first incompleteness if it is recursively enumerable, consistent, and internally supports enough syntax to represent substitution and proof verification.

A robust sufficient condition is that \(T\) contain or interpret Robinson arithmetic \(Q\).

Robinson arithmetic \(Q\) is finitely axiomatized and contains, among others, the axioms

\[
\forall x\,Sx\neq 0,
\]

\[
\forall x\forall y\,(Sx=Sy\to x=y),
\]

\[
\forall x\,(x+0=x),
\]

\[
\forall x\forall y\,(x+Sy=S(x+y)),
\]

\[
\forall x\,(x\times 0=0),
\]

\[
\forall x\forall y\,(x\times Sy=x\times y+x),
\]

\[
\forall x\,(x=0\vee \exists y\,x=Sy).
\]

These axioms already force infinitely many distinct elements:

\[
0,\quad S0,\quad SS0,\quad SSS0,\quad \dots
\]

Thus, any strict finitist who denies the completed infinite totality has reason to reject \(Q\) as a theory of feasible numbers.

Nevertheless, if a strict finitist theory does accept \(Q\), or a theory interpreting \(Q\), then it cannot escape the first incompleteness theorem by philosophical fiat.

---

### 4.2 Interpretation of \(Q\) as a sufficient condition

The following result is standard but crucial.

**Theorem 4.1.**  
Let \(T\) be a consistent recursively enumerable theory. If \(T\) interprets Robinson arithmetic \(Q\), then \(T\) is incomplete.

Here, an interpretation of \(Q\) in \(T\) means that \(T\) defines a domain, together with formulas interpreting \(0,S,+,\times\), such that \(T\) proves the axioms of \(Q\) relativized to that interpretation.

**Proof sketch.**  
The theory \(Q\) is essentially undecidable: every consistent recursively enumerable extension of \(Q\) is incomplete. Essential undecidability is preserved under interpretation. If \(T\) were complete and recursively enumerable, then the interpreted theory of \(Q\) would yield a complete recursively enumerable extension of \(Q\), contradicting essential undecidability. Hence \(T\) is incomplete. \(\square\)

This theorem shows that the boundary is not tied to the literal language \(\{0,S,+,\times\}\). It is tied to the presence of a certain amount of arithmetical structure.

---

### 4.3 Induction is not the decisive issue

A common misconception is that Gödel’s theorem depends essentially on induction. It does not.

Robinson arithmetic \(Q\) has no induction schema, yet it is essentially undecidable. Therefore, rejecting induction alone does not avoid incompleteness.

What matters is the ability to represent enough primitive recursive syntax. Induction is one way to obtain such representability, but it is not the only way. \(Q\) obtains numeralwise representability by directly verifying finite computations.

Thus, ultrafinitism undercuts Gödel only if it blocks one of the following:

1. recursive enumerability of the theory;
2. existence of an unbounded proof predicate;
3. representability of substitution;
4. representability of proof checking;
5. acceptance of the diagonal sentence as a well-formed, meaningful statement.

If these remain, Gödel’s first theorem remains.

---

## 5. Resource-Bounded Incompleteness

### 5.1 Bounded provability

To analyze the ultrafinitist situation more finely, we introduce bounded proof predicates.

Let \(T\) be a recursively enumerable theory with proof predicate \(\operatorname{Prf}_T(p,x)\). For a standard natural number \(b\), define

\[
\operatorname{Prf}_{T,\le b}(p,x)
\equiv
\operatorname{Prf}_T(p,x)\wedge p\le \overline b.
\]

Define bounded provability by

\[
\operatorname{Prov}_{T,\le b}(x)
\equiv
\exists p\le \overline b\,\operatorname{Prf}_T(p,x).
\]

The bounded consistency statement is

\[
\operatorname{Con}_{\le b}(T)
\equiv
\neg \operatorname{Prov}_{T,\le b}(\ulcorner 0=1\urcorner).
\]

The unbounded consistency statement is

\[
\operatorname{Con}(T)
\equiv
\forall b\,\operatorname{Con}_{\le b}(T).
\]

This decomposition is important. Ultrafinitism may accept each finite statement

\[
\operatorname{Con}_{\le b}(T)
\]

while rejecting the completed universal quantification

\[
\forall b\,\operatorname{Con}_{\le b}(T).
\]

Thus, the second incompleteness theorem is not primarily an obstruction to verifying consistency locally; it is an obstruction to proving the unbounded totality of local consistency.

---

### 5.2 Bounded diagonal lemma

We now formulate a bounded version of diagonalization.

Let \(T\) be a recursively enumerable extension of \(Q\). Let \(\operatorname{Sub}(u,v)\) be a primitive recursive function giving the code of the formula obtained by substituting the numeral for \(v\) into the formula coded by \(u\).

Consider the formula schema

\[
\eta(u,x)\equiv
\neg \exists p\le x\,\operatorname{Prf}_T(p,\operatorname{Sub}(u,x)).
\]

By a parameterized form of the diagonal lemma, there is a formula \(H(x)\) such that

\[
T\vdash
H(x)\leftrightarrow
\neg \exists p\le x\,
\operatorname{Prf}_T(p,\ulcorner H(x)\urcorner).
\]

For each standard \(b\), let

\[
G_b\equiv H(\overline b).
\]

Then

\[
T\vdash
G_b\leftrightarrow
\neg \exists p\le \overline b\,
\operatorname{Prf}_T(p,\ulcorner G_b\urcorner).
\]

This is the bounded diagonal lemma.

The sentence \(G_b\) says:

> There is no proof of \(G_b\) in \(T\) whose code is bounded by \(b\).

---

### 5.3 Bounded incompleteness theorem

**Theorem 5.1. Bounded Incompleteness.**  
Let \(T\) be a consistent recursively enumerable extension of \(Q\). For each standard bound \(b\), let \(G_b\) be as above. Then \(G_b\) has no \(T\)-proof with code \(\le b\).

If, in addition, \(T\) is \(\Sigma^0_1\)-sound for bounded existential statements, then \(\neg G_b\) also has no \(T\)-proof with code \(\le b\).

**Proof.**  
Assume \(p\le b\) codes a \(T\)-proof of \(G_b\). Since \(\operatorname{Prf}_T\) represents proof checking, \(T\) proves

\[
\operatorname{Prf}_T(\overline p,\ulcorner G_b\urcorner).
\]

Since \(p\le b\), \(T\) also proves

\[
\overline p\le \overline b.
\]

Therefore \(T\) proves

\[
\exists q\le \overline b\,
\operatorname{Prf}_T(q,\ulcorner G_b\urcorner).
\]

But by the bounded diagonal equivalence,

\[
T\vdash
G_b\leftrightarrow
\neg \exists q\le \overline b\,
\operatorname{Prf}_T(q,\ulcorner G_b\urcorner).
\]

Hence \(T\) proves \(\neg G_b\). Since \(p\) is a proof of \(G_b\), \(T\) is inconsistent. This contradicts consistency. Therefore there is no \(T\)-proof of \(G_b\) with code \(\le b\).

Now suppose \(T\) proves \(\neg G_b\) by some proof with code \(q\le b\). Then \(T\) proves

\[
\neg G_b.
\]

By the bounded diagonal equivalence, \(T\) proves

\[
\exists p\le \overline b\,
\operatorname{Prf}_T(p,\ulcorner G_b\urcorner).
\]

This is a bounded \(\Sigma^0_1\) statement. If \(T\) is \(\Sigma^0_1\)-sound for such statements, then there really exists a standard \(p\le b\) such that

\[
\operatorname{Prf}_T(p,\ulcorner G_b\urcorner).
\]

Thus \(G_b\) has a \(T\)-proof with code \(\le b\), contradicting the first part. Hence, under bounded \(\Sigma^0_1\)-soundness, \(\neg G_b\) also has no proof with code \(\le b\). \(\square\)

A Rosser-style modification removes the \(\Sigma^0_1\)-soundness assumption, but the essential phenomenon is already visible: bounded proof fragments exhibit local independence phenomena.

---

### 5.4 Admissibility and the Gödel radius

The preceding theorem is external. It constructs \(G_b\) in the metatheory. For an ultrafinitist, however, the crucial question is whether \(G_b\) itself is admissible within the bound \(b\).

The problem is code blow-up. The sentence \(G_b\) contains, directly or indirectly, a name for the bound \(b\). Its Gödel code may be much larger than \(b\). If the ultrafinitist accepts only expressions whose codes lie below \(b\), then \(G_b\) may not be an acceptable sentence at all.

We therefore define an admissibility condition.

A bound \(B\) is **diagonally admissible** for \(T\), relative to a coding, if there exists a sentence \(G\) such that

\[
\ulcorner G\urcorner\le B
\]

and

\[
T\vdash
G\leftrightarrow
\neg \exists p\le \overline B\,
\operatorname{Prf}_T(p,\ulcorner G\urcorner).
\]

If no such \(B\) is accepted by the strict finitist, then the Gödel construction cannot be internally completed.

This motivates the notion of a **Gödel radius**.

For a theory \(T\) and coding \(c\), define

\[
\rho(T,c)
=
\min
\left\{
B:
\exists G\,
\left[
c(G)\le B
\wedge
T\vdash
G\leftrightarrow
\neg \exists p\le \overline B\,
\operatorname{Prf}_T(p,c(G))
\right]
\right\},
\]

if such a minimum exists.

The Gödel radius is the least resource bound at which bounded self-reference becomes possible. Below this radius, the ultrafinitist can avoid the Gödel sentence simply because the sentence cannot be formed or verified within the accepted resources. Above this radius, bounded incompleteness phenomena appear.

This gives a precise technical meaning to the idea that ultrafinitism undercuts Gödel by refusing the closure operations required for diagonalization.

---

### 5.5 Bounded consistency statements

The second incompleteness theorem also has a bounded analogue.

Let \(T\) be a consistent recursively enumerable extension of \(Q\). For each standard \(b\), if there is no \(T\)-proof of contradiction with code \(\le b\), then \(T\) can in principle prove

\[
\operatorname{Con}_{\le b}(T).
\]

The reason is that proof checking is primitive recursive. For each \(p\le b\), the statement

\[
\neg \operatorname{Prf}_T(\overline p,\ulcorner 0=1\urcorner)
\]

is a true decidable instance. A weak base theory can verify each such instance, and a finite conjunction yields

\[
\bigwedge_{p\le b}
\neg \operatorname{Prf}_T(\overline p,\ulcorner 0=1\urcorner).
\]

Hence

\[
T\vdash \operatorname{Con}_{\le b}(T).
\]

However, the proof may be enormous. More importantly, this does not yield

\[
T\vdash \forall b\,\operatorname{Con}_{\le b}(T).
\]

The unbounded consistency statement is

\[
\operatorname{Con}(T)
\equiv
\forall b\,\operatorname{Con}_{\le b}(T).
\]

Gödel’s second incompleteness theorem concerns precisely this unbounded universal statement, not each finite check taken separately.

Thus, an ultrafinitist may consistently maintain:

\[
\text{For each concrete bound } b,\text{ I can verify } \operatorname{Con}_{\le b}(T),
\]

while refusing to assert:

\[
\forall b\,\operatorname{Con}_{\le b}(T).
\]

This is one of the cleanest ways in which strict finitism changes the meaning of the second incompleteness theorem.

---

## 6. Escape Routes and Their Costs

Ultrafinitism can avoid classical Gödel incompleteness only by breaking one or more hypotheses of the Gödel apparatus. We now classify the main escape routes.

---

### 6.1 Finite or decidable fragments

If a theory is finite and describes a finite structure, it may be complete and decidable.

For example, fix a bound \(N\). Consider a finite structure with domain

\[
\{0,1,2,\dots,N\}.
\]

One may define truncated operations:

\[
x\oplus y=\min(x+y,N),
\]

\[
x\otimes y=\min(x\cdot y,N).
\]

The complete first-order theory of this finite structure is decidable. There is no Gödel incompleteness obstacle because the structure is finite and the theory can be complete.

But the cost is severe. Such a structure no longer satisfies the usual axioms of arithmetic globally. For instance, successor cannot behave like the standard successor everywhere if there is a largest element. Algebraic laws fail near the boundary. The theory is no longer standard number theory.

Similarly, Presburger arithmetic, which has addition but not multiplication, is complete and decidable. It escapes Gödelian arithmetic incompleteness, but only because it lacks the multiplicative structure needed for full arithmetization of syntax.

---

### 6.2 Failure of coding and sequence representation

Gödel’s proof requires coding of sequences, substitution, and proofs. Classical coding often uses exponentiation:

\[
\ulcorner a_0,\dots,a_{k-1}\urcorner
=
2^{a_0+1}3^{a_1+1}\cdots p_{k-1}^{a_{k-1}+1}.
\]

A strict finitist may reject the totality of exponentiation and therefore reject the general existence of such codes.

Alternative codings using binary strings are more economical, but they still require some theory of strings, concatenation, and bounded quantification. If the theory cannot prove enough about these operations, the diagonal lemma may fail internally.

The cost is that much of ordinary metamathematics becomes unavailable. One cannot generally speak of arbitrary finite sequences, arbitrary proofs, or arbitrary formulas. One can only discuss syntactic objects below a bound.

---

### 6.3 Non-effective axiom systems

Gödel’s theorem applies to recursively enumerable theories. If ultrafinitist acceptance is governed by a vague notion of “feasible” or “constructible,” the resulting set of accepted axioms may not be recursively enumerable.

In that case, there may be no effective proof predicate

\[
\operatorname{Prf}_T(p,x).
\]

Without such a predicate, the usual Gödel construction cannot be formed.

However, the cost is again high. The theory no longer has an effective proof system. One cannot in general decide whether a given argument is a valid proof. The resulting “theory” may be philosophically coherent as a practice, but it is not a formal theory in the Gödelian sense.

---

### 6.4 Partial terms and non-denoting numerals

Another approach is to use a logic of partial terms. A term such as

\[
2^{2^{2^{10}}}
\]

may be syntactically writable but semantically non-denoting if its value exceeds the accepted bound.

In such a system, equations involving large terms may lack truth values, or may be true only under feasibility conditions. This can block the usual proof that all numerals denote distinct objects, and it can block the internal formation of Gödel sentences.

The cost is that classical algebraic laws become conditional. One no longer has unrestricted equations such as

\[
x+y=y+x
\]

for all \(x,y\). Instead one has bounded versions:

\[
x,y,x+y\le B
\quad\Longrightarrow\quad
x+y=y+x.
\]

Standard number theory is replaced by a theory of locally valid computations.

---

### 6.5 Weakening logic

One might try to escape incompleteness by weakening classical logic, for example by moving to intuitionistic, minimal, or paraconsistent systems.

This does not usually suffice by itself. Gödel-style incompleteness can often be adapted to intuitionistic arithmetic, provided the theory remains recursively enumerable and sufficiently expressive. For example, Heyting arithmetic is also incomplete.

To escape incompleteness through logic alone, one must usually disrupt the interaction between negation, proof, and representability in a radical way. This often comes at the cost of losing ordinary mathematical reasoning.

---

## 7. Gödel’s Theorems as Limit Theorems

We now propose a unifying conceptual framework.

Let \(T_b\) denote a bounded approximation to arithmetic at resource bound \(b\). The bound \(b\) may restrict proof length, formula size, numeral size, or computational resources. The family

\[
(T_b)_{b\in\mathbb{N}}
\]

is monotone in the sense that larger bounds permit more theorems, more proofs, and more syntactic constructions.

At each finite stage \(b\), the theory \(T_b\) may be finite, decidable, or even complete relative to its language. There is no contradiction with Gödel because \(T_b\) does not contain the unbounded totality required for self-reference.

The classical theory \(T\) is the limit:

\[
T_\infty=\bigcup_{b\in\mathbb{N}}T_b.
\]

If this union is accepted as a completed recursively enumerable theory, and if it interprets \(Q\), then Gödel’s theorem applies.

Thus, Gödel’s theorem is a theorem about the limit.

This gives the following stratification.

| Regime | Accepted object | Gödel status | Cost |
|---|---|---|---|
| Finite static regime | A fixed finite fragment \(T_b\) | May be complete/decidable | Almost no global number theory |
| Bounded potential regime | Each \(T_b\) separately, but no completed union | Bounded independence phenomena; no single Gödel sentence | No uniform global consistency or induction |
| Unbounded classical regime | Completed union \(T_\infty\) | Classical incompleteness applies | Full arithmetic but incomplete |

The ultrafinitist rejects the passage from the bounded potential regime to the unbounded classical regime. Gödel’s theorems do not refute this rejection. Instead, they show what is lost by it: the ability to form a single, recursively enumerable, self-reflective arithmetic theory.

---

## 8. Consequences for Number Theory

### 8.1 What can be preserved

Ultrafinitist mathematics can preserve a substantial body of bounded mathematical practice.

It can preserve:

1. finite combinatorics below explicit bounds;
2. concrete computations;
3. polynomial-time or otherwise feasible algorithms, depending on the chosen bound;
4. bounded forms of induction;
5. local versions of algebraic identities;
6. finite proof verification;
7. explicit constructions of numbers and functions below accepted bounds.

For example, one may accept the statement

\[
\forall x\le 1000\,\exists y\le 2^{1000}\,(y=2^x)
\]

if the relevant bounds are considered feasible, while rejecting

\[
\forall x\,\exists y\,(y=2^x).
\]

Similarly, one may accept bounded prime search principles:

\[
\text{For every feasible list of primes, another prime can be constructed},
\]

without accepting the completed assertion that there are infinitely many primes.

---

### 8.2 What is lost

What is lost is the global unity of classical number theory.

In particular:

1. There is no single totality of all natural numbers.
2. There is no unrestricted induction schema.
3. There is no general theory of arbitrary finite sequences.
4. There is no unrestricted Gödel coding.
5. There is no unbounded consistency statement.
6. There is no completed set of all formulas or proofs.
7. There is no single theory that is simultaneously complete, consistent, recursively enumerable, and arithmetically expressive.

Thus, ultrafinitism does not merely weaken arithmetic. It transforms arithmetic into a family of bounded calculi.

---

### 8.3 The role of representability

The decisive issue is representability.

Classical Gödel theory requires that syntactic operations be representable inside arithmetic. For example, for substitution, one needs formulas representing

\[
\operatorname{Sub}(e,n)=m.
\]

In a bounded setting, one can define bounded representability:

A function \(f\) is \(B\)-representable in \(T\) if, for all \(n,m\le B\),

\[
f(n)=m
\quad\Longrightarrow\quad
T\vdash_{\le B}
\varphi(\overline n,\overline m),
\]

where \(\vdash_{\le B}\) means “provable by a proof whose code or length is bounded by \(B\).”

This bounded notion is often available even when global representability is not. But Gödel’s theorem requires uniform representability across all bounds. The passage from \(B\)-representability for each fixed \(B\) to unbounded representability is exactly the passage that strict finitism refuses.

---

## 9. Conclusion

Ultrafinitism does not refute Gödel’s incompleteness theorems. Rather, it exposes their hypotheses with unusual clarity.

Gödel’s first theorem applies to consistent, recursively enumerable theories that can internalize enough syntax to support diagonalization. This includes very weak systems such as extensions of Robinson arithmetic \(Q\). Induction is not the crucial ingredient. Effective self-reference is.

Gödel’s second theorem applies when a theory can reason about its own provability predicate in a way satisfying the derivability conditions. Bounded consistency statements may still be provable, but the unbounded consistency statement is precisely the kind of completed totality that strict finitism rejects.

The boundary is therefore not between “classical mathematics” and “ultrafinitism” as such. It is between bounded mathematical practice and unbounded, recursively enumerable, self-reflective theory.

Fixed finite fragments can be complete, decidable, and locally consistent. They can even prove their own bounded consistency. But they cannot recover standard number theory without reintroducing unbounded closure. Once a strict finitist framework accepts a uniform, effective, unbounded syntax and proof system strong enough to interpret \(Q\), Gödel’s theorems apply again.

Thus, Gödelian incompleteness should be understood as a limit phenomenon. It governs the moment at which finite, constructive practice is idealized into a completed infinite totality. Ultrafinitism avoids the theorem by refusing that idealization, but the price is the loss of arithmetic as a global, unified theory of the natural numbers.

---

## References

1. Gödel, K. *On Formally Undecidable Propositions of Principia Mathematica and Related Systems*, 1931.  
2. Rosser, J. B. “Extensions of Some Theorems of Gödel and Church,” *Journal of Symbolic Logic*, 1936.  
3. Tarski, A., Mostowski, A., Robinson, R. M. *Undecidable Theories*, North-Holland, 1953.  
4. Mendelson, E. *Introduction to Mathematical Logic*, multiple editions.  
5. Boolos, G., Burgess, J., Jeffrey, R. *Computability and Logic*, Cambridge University Press.  
6. Hájek, P., Pudlák, P. *Metamathematics of First-Order Arithmetic*, Springer, 1993.  
7. Buss, S. R. *Bounded Arithmetic*, Bibliopolis, 1986.  
8. Krajíček, J. *Bounded Arithmetic, Propositional Logic, and Complexity Theory*, Cambridge University Press, 1995.  
9. Pudlák, P. “The lengths of proofs,” in *Handbook of Proof Theory*, Elsevier, 1998.  
10. Dummett, M. *Elements of Intuitionism*, Oxford University Press.  
11. Shapiro, S. *Foundations without Certainty*, and related work on strict finitism and potential infinity.

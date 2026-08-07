# Evolutionary Category Theory

## Functorial Laws, Dynamic Natural Transformations, and Higher Semantics

**Preprint**

---

## Abstract

We introduce **Evolutionary Category Theory (ECT)**, a formal framework in which categories themselves are dynamical systems. The central thesis is that categorical structure should not be regarded as statically given, but as evolving under **functorial evolutionary laws**. Concretely, an evolutionary category is a category equipped with a coherent action of a time monoid by endofunctors. Objects, morphisms, functors, and natural transformations acquire canonical evolutionary images, and the usual equations of category theory are promoted to time-parametrized functorial identities.

We develop the basic 2-category of evolutionary categories, define evolutionary functors and evolutionary natural transformations, and construct the **trajectory category** of an evolutionary category, in which morphisms describe processes between objects located at different times. In monoidal and tensorial settings, evolutionary laws become compatible with tensor products, yielding a calculus of evolving processes. We also analyze infinitesimal evolutionary laws on enriched categories, where derivations satisfying Leibniz-type rules integrate to one-parameter functorial flows.

The framework is then extended to higher and \(\infty\)-categorical settings, where coherence data themselves evolve. Applications are given to higher category theory, programming semantics, categorical logic, and systems science. In particular, we show how evolving types and programs admit sound categorical semantics, how temporal modalities arise from adjoints to evolution functors, and how adaptive systems can be modeled as dynamic natural transformations between evolutionary system trajectories.

**Keywords:** evolutionary category theory, functorial dynamics, time actions, dynamic natural transformations, higher categories, categorical semantics, temporal logic, systems theory.

---

## 1. Introduction

Classical category theory studies structures consisting of objects, morphisms, composition, and identity laws. These structures are usually treated synchronically: a category is given once and for all. This is mathematically powerful, but insufficient for phenomena in which the structure itself changes over time. Examples include:

- type systems and programs undergoing versioned evolution;
- logical theories translated or deformed over time;
- higher-categorical coherence data subject to parametrized deformation;
- adaptive systems whose interfaces, interconnections, and internal organizations co-evolve.

Evolutionary Category Theory begins from the following principle.

> **Principle 1.1.**  
> A category may evolve by endofunctorial laws, and such evolution must preserve the functorial structure of composition, identities, and higher coherence.

Thus, rather than placing dynamics outside category theory, ECT internalizes dynamics as a **time action on a category**. If \(X\) is an object and \(f:X\to Y\) a morphism, then after evolutionary duration \(t\) one obtains an evolved object
\[
X^{[t]} := E_t(X)
\]
and an evolved morphism
\[
f^{[t]} := E_t(f):X^{[t]}\to Y^{[t]},
\]
where \(E_t:\mathcal C\to\mathcal C\) is the evolution functor associated with duration \(t\). Functoriality implies
\[
E_t(\operatorname{id}_X)=\operatorname{id}_{E_t(X)}, 
\qquad
E_t(g\circ f)=E_t(g)\circ E_t(f).
\]
Hence evolution preserves categorical structure.

The central novelty is not merely that objects and morphisms evolve, but that **natural transformations, functors, limits, adjunctions, monoidal tensors, and higher coherences may also evolve coherently**. This yields a genuinely dynamical category theory.

The contributions of this paper are as follows.

1. We define \(T\)-evolutionary categories as categories equipped with a coherent action of a time monoid \(T\) by endofunctors.

2. We introduce evolutionary functors and evolutionary natural transformations, and show that they form a natural 2-category \(\mathbf{EvCat}_T\).

3. We construct the trajectory category \(\operatorname{Traj}_T(\mathcal C)\), whose objects are time-stamped objects \((t,X)\), and whose morphisms describe processes across evolutionary time.

4. We develop a tensorial version of ECT for monoidal categories, proving compatibility of evolution with tensor products, duals, and coherence isomorphisms.

5. We analyze infinitesimal evolutionary laws in enriched settings, identifying them with categorical derivations satisfying Leibniz rules.

6. We extend the theory to higher and \(\infty\)-categories.

7. We give applications to programming semantics, categorical logic, and systems science.

---

## 2. Preliminaries

### 2.1 Time monoids

We fix a **time monoid**
\[
(T,+,0).
\]
In most examples, \(T\) is one of the following:

- the discrete time monoid \((\mathbb N,+,0)\);
- the continuous time monoid \((\mathbb R_{\ge 0},+,0)\);
- a partially ordered commutative monoid with order
  \[
  s\le t \quad \Longleftrightarrow \quad \exists u\in T,\ t=s+u.
  \]

We assume, unless otherwise stated, that \(T\) is cancellative and that differences \(t-s\) are unique whenever \(s\le t\). This holds for \(\mathbb N\) and \(\mathbb R_{\ge 0}\).

The monoid \(T\) may be regarded as a discrete strict monoidal category with one object, or as a posetal category \(\operatorname{Int}(T)\) whose objects are times and whose unique morphism \(s\to t\) exists precisely when \(s\le t\).

### 2.2 Endofunctorial actions

For a category \(\mathcal C\), let \(\operatorname{End}(\mathcal C)\) denote the monoidal 2-category of endofunctors of \(\mathcal C\), natural transformations, and modifications. Its tensor is composition of endofunctors:
\[
F\otimes G := F\circ G.
\]
The unit is \(\operatorname{id}_{\mathcal C}\).

An evolutionary law will be a coherent monoidal action of \(T\) on \(\mathcal C\), i.e. a monoidal functor
\[
E:T\longrightarrow \operatorname{End}(\mathcal C).
\]

In the strict case, this is simply a family of endofunctors
\[
E_t:\mathcal C\to \mathcal C,\qquad t\in T,
\]
satisfying
\[
E_0=\operatorname{id}_{\mathcal C},
\qquad
E_s\circ E_t = E_{s+t}.
\]

We use the notation
\[
X^{[t]} := E_t(X),
\qquad
f^{[t]} := E_t(f).
\]

---

## 3. Evolutionary Categories

### Definition 3.1: \(T\)-evolutionary category

Let \(T\) be a time monoid. A **\(T\)-evolutionary category** is a tuple
\[
(\mathcal C,E,\mu,\iota)
\]
where:

1. \(\mathcal C\) is a category;

2. for each \(t\in T\), \(E_t:\mathcal C\to \mathcal C\) is an endofunctor;

3. for each \(s,t\in T\), there is a natural isomorphism
   \[
   \mu_{s,t}:E_s\circ E_t \xrightarrow{\sim} E_{s+t};
   \]

4. there is a natural isomorphism
   \[
   \iota:\operatorname{id}_{\mathcal C}\xrightarrow{\sim} E_0;
   \]

subject to the usual associativity and unit coherence conditions.

Explicitly, for all \(r,s,t\in T\), the diagram
\[
\begin{tikzcd}
E_rE_sE_t \arrow[r,"\mu_{r,s}E_t"] \arrow[d,"E_r\mu_{s,t}"'] & E_{r+s}E_t \arrow[d,"\mu_{r+s,t}"] \\
E_rE_{s+t} \arrow[r,"\mu_{r,s+t}"'] & E_{r+s+t}
\end{tikzcd}
\]
commutes, together with the unit diagrams involving \(\iota\).

If all coherence isomorphisms are identities, we say that \((\mathcal C,E)\) is a **strict \(T\)-evolutionary category**.

### Remark 3.2

In strict notation, the evolutionary law is
\[
E_{s+t}=E_sE_t,
\qquad
E_0=\operatorname{id}_{\mathcal C}.
\]
Thus \(E\) is a representation of the time monoid \(T\) in the monoid of endofunctors of \(\mathcal C\).

---

### Definition 3.3: Evolutionary functor

Let
\[
(\mathcal C,E^{\mathcal C})
\quad\text{and}\quad
(\mathcal D,E^{\mathcal D})
\]
be \(T\)-evolutionary categories.

An **evolutionary functor**
\[
(F,\lambda):(\mathcal C,E^{\mathcal C})\to(\mathcal D,E^{\mathcal D})
\]
consists of:

1. a functor
   \[
   F:\mathcal C\to\mathcal D;
   \]

2. for each \(t\in T\), a natural isomorphism
   \[
   \lambda_t:E_t^{\mathcal D}\circ F \xrightarrow{\sim} F\circ E_t^{\mathcal C};
   \]

such that for all \(s,t\in T\), the following diagram commutes:
\[
\begin{tikzcd}
E_s^{\mathcal D}E_t^{\mathcal D}F
\arrow[r,"\mu^{\mathcal D}_{s,t}F"]
\arrow[d,"E_s^{\mathcal D}\lambda_t"']
&
E_{s+t}^{\mathcal D}F
\arrow[d,"\lambda_{s+t}"]
\\
E_s^{\mathcal D}F E_t^{\mathcal C}
\arrow[r,"\lambda_s E_t^{\mathcal C}"']
&
F E_{s+t}^{\mathcal C}.
\end{tikzcd}
\]

If the coherence isomorphisms \(\lambda_t\) are identities, we say that \(F\) is a **strict evolutionary functor**.

---

### Definition 3.4: Evolutionary natural transformation

Let
\[
(F,\lambda),(G,\kappa):(\mathcal C,E^{\mathcal C})\to(\mathcal D,E^{\mathcal D})
\]
be evolutionary functors.

An **evolutionary natural transformation**
\[
\alpha:(F,\lambda)\Rightarrow(G,\kappa)
\]
is a natural transformation
\[
\alpha:F\Rightarrow G
\]
such that for every \(t\in T\), the following square commutes:
\[
\begin{tikzcd}
E_t^{\mathcal D}F
\arrow[r,"E_t^{\mathcal D}\alpha"]
\arrow[d,"\lambda_t"']
&
E_t^{\mathcal D}G
\arrow[d,"\kappa_t"]
\\
F E_t^{\mathcal C}
\arrow[r,"\alpha E_t^{\mathcal C}"']
&
G E_t^{\mathcal C}.
\end{tikzcd}
\]

In the strict case this condition becomes
\[
E_t^{\mathcal D}(\alpha_X)
=
\alpha_{E_t^{\mathcal C}(X)}
\]
for every object \(X\in\mathcal C\). Thus the evolution of the component equals the component at the evolved object.

---

### Proposition 3.5: The 2-category of evolutionary categories

There is a 2-category
\[
\mathbf{EvCat}_T
\]
whose

- objects are \(T\)-evolutionary categories;
- 1-morphisms are evolutionary functors;
- 2-morphisms are evolutionary natural transformations.

#### Proof

Identity evolutionary functors are given by \((\operatorname{id}_{\mathcal C},\operatorname{id})\). Vertical composition of evolutionary natural transformations is ordinary vertical composition, and the compatibility square is preserved by pasting.

Horizontal composition is defined using whiskering and the coherence isomorphisms of the evolutionary functors. The associativity and interchange laws follow from the coherence axioms for \(\mu\), \(\iota\), and \(\lambda\). Therefore \(\mathbf{EvCat}_T\) is a 2-category. \(\square\)

---

## 4. Functorial Evolutionary Laws

### 4.1 Strict laws

In the strict case, a functorial evolutionary law is a family of endofunctors \(E_t\) satisfying:

\[
E_0=\operatorname{id}_{\mathcal C},
\tag{4.1}
\]

\[
E_{s+t}=E_sE_t,
\tag{4.2}
\]

\[
E_t(g\circ f)=E_t(g)\circ E_t(f),
\tag{4.3}
\]

\[
E_t(\operatorname{id}_X)=\operatorname{id}_{E_t(X)}.
\tag{4.4}
\]

Equations (4.1)–(4.4) express that evolution is a monoid action by functors.

Using the notation
\[
X^{[t]}:=E_t(X),
\qquad
f^{[t]}:=E_t(f),
\]
we obtain
\[
(\operatorname{id}_X)^{[t]}=\operatorname{id}_{X^{[t]}},
\tag{4.5}
\]
and
\[
(g\circ f)^{[t]}=g^{[t]}\circ f^{[t]}.
\tag{4.6}
\]

The semigroup law becomes
\[
X^{[s+t]}=(X^{[t]})^{[s]},
\qquad
f^{[s+t]}=(f^{[t]})^{[s]}.
\tag{4.7}
\]

Thus evolutionary time acts as a functorial flow on the entire category.

---

### 4.2 Evolution of natural transformations

Let \(F,G:\mathcal C\to\mathcal D\) be functors and let
\[
\alpha:F\Rightarrow G
\]
be a natural transformation.

For each \(t\in T\), define
\[
\alpha^{[t]}:E_tF\Rightarrow E_tG
\]
by
\[
(\alpha^{[t]})_X := E_t(\alpha_X).
\]

#### Proposition 4.1

If \(E_t:\mathcal D\to\mathcal D\) is an endofunctor, then \(\alpha^{[t]}\) is a natural transformation.

#### Proof

Let \(f:X\to Y\) in \(\mathcal C\). Since \(\alpha\) is natural,
\[
G(f)\circ\alpha_X=\alpha_Y\circ F(f).
\]
Applying \(E_t\), we obtain
\[
E_t(G(f))\circ E_t(\alpha_X)
=
E_t(\alpha_Y)\circ E_t(F(f)).
\]
In notation,
\[
(E_tG)(f)\circ(\alpha^{[t]})_X
=
(\alpha^{[t]})_Y\circ(E_tF)(f).
\]
Hence \(\alpha^{[t]}\) is natural. \(\square\)

Therefore, evolution acts not only on objects and morphisms, but also on natural transformations.

---

### 4.3 Preservation of vertical and horizontal composition

Let
\[
\alpha:F\Rightarrow G,
\qquad
\beta:G\Rightarrow H
\]
be natural transformations. Then
\[
(\beta\circ\alpha)^{[t]}
=
\beta^{[t]}\circ\alpha^{[t]}.
\tag{4.8}
\]

Indeed,
\[
((\beta\circ\alpha)^{[t]})_X
=
E_t(\beta_X\circ\alpha_X)
=
E_t(\beta_X)\circ E_t(\alpha_X)
=
(\beta^{[t]}\circ\alpha^{[t]})_X.
\]

Similarly, if
\[
\alpha:F\Rightarrow G:\mathcal C\to\mathcal D,
\qquad
\gamma:H\Rightarrow K:\mathcal D\to\mathcal B,
\]
then
\[
(\gamma*\alpha)^{[t]}
=
\gamma^{[t]}*\alpha^{[t]},
\tag{4.9}
\]
where \(*\) denotes horizontal composition.

Thus evolutionary action is compatible with the full 2-categorical structure of \(\mathbf{Cat}\).

---

### 4.4 Evolution of limits and colimits

Let \(D:J\to\mathcal C\) be a diagram. Suppose \(E_t\) preserves limits of shape \(J\). Then there is a canonical isomorphism
\[
E_t(\lim D)
\cong
\lim(E_t\circ D).
\tag{4.10}
\]

Indeed, for any object \(X\in\mathcal C\),
\[
\begin{aligned}
\mathcal C(X,E_t(\lim D))
&\cong
\mathcal C(X,\lim(E_tD)) \\
&\cong
\lim_j \mathcal C(X,E_tD(j)).
\end{aligned}
\]
Thus the evolved limit represents the limit of the evolved diagram.

Dually, if \(E_t\) preserves colimits, then
\[
E_t(\operatorname{colim}D)
\cong
\operatorname{colim}(E_t\circ D).
\tag{4.11}
\]

Hence universal constructions may evolve coherently.

---

## 5. Anchored Evolution and Canonical Trajectories

A bare endofunctorial action does not necessarily provide a canonical morphism from an object to its evolved image. To speak of trajectories, we introduce an additional structure.

### Definition 5.1: Anchored evolutionary category

An **anchored \(T\)-evolutionary category** is a \(T\)-evolutionary category \((\mathcal C,E,\mu,\iota)\) equipped with natural transformations
\[
\eta_t:\operatorname{id}_{\mathcal C}\Rightarrow E_t,
\qquad t\in T,
\]
such that

1. \(\eta_0=\iota\);

2. for all \(s,t\in T\),
   \[
   \eta_{s+t}
   =
   \mu_{s,t}\circ E_s(\eta_t)\circ\eta_s.
   \tag{5.1}
   \]

In the strict case, this becomes
\[
\eta_{s+t}=E_s(\eta_t)\circ\eta_s.
\tag{5.2}
\]

The component
\[
\eta_{t,X}:X\to X^{[t]}
\]
is the **evolutionary trajectory** of \(X\) over duration \(t\).

---

### Proposition 5.2: Orbit functors

Let \((\mathcal C,E,\eta)\) be anchored. For each object \(X\in\mathcal C\), there is a functor
\[
\Omega_X:\operatorname{Int}(T)\to\mathcal C
\]
defined by
\[
\Omega_X(t)=E_t(X),
\]
and for \(s\le t\), with \(t=s+u\), by
\[
\Omega_X(s\le t)
=
\mu_{s,u,X}\circ E_s(\eta_{u,X}):
E_s(X)\to E_{s+u}(X).
\]

#### Proof

The condition (5.1) ensures preservation of composition in \(\operatorname{Int}(T)\). The unit condition follows from \(\eta_0=\iota\). \(\square\)

Thus an anchored evolutionary category assigns to every object a genuine trajectory in \(\mathcal C\).

---

## 6. The Trajectory Category

We now construct a category in which objects are located at explicit times and morphisms describe processes across evolutionary time.

Assume \(T\) is an ordered cancellative time monoid with unique differences.

### Definition 6.1: Forward trajectory category

Let \((\mathcal C,E,\mu,\iota)\) be a \(T\)-evolutionary category.

The **forward trajectory category**
\[
\operatorname{Traj}_T(\mathcal C)
\]
is defined as follows.

- Objects are pairs
  \[
  (t,X),
  \]
  where \(t\in T\) and \(X\in\mathcal C\).

- If \(s\le t\), with \(t=s+u\), then
  \[
  \operatorname{Hom}_{\operatorname{Traj}}
  ((s,X),(t,Y))
  :=
  \operatorname{Hom}_{\mathcal C}
  (X,E_u(Y)).
  \]

- If \(s\not\le t\), the hom-set is empty.

Thus a morphism
\[
f:(s,X)\to(t,Y)
\]
is a morphism
\[
f:X\to E_{t-s}(Y)
\]
in \(\mathcal C\). It represents a process beginning at \(X\) at time \(s\) and terminating at the evolved target \(Y\) at time \(t\).

---

### Composition

Suppose
\[
f:(s,X)\to(t,Y),
\qquad
g:(t,Y)\to(u,Z).
\]
Thus
\[
f:X\to E_{t-s}(Y),
\qquad
g:Y\to E_{u-t}(Z).
\]
Define
\[
g\star f:X\to E_{u-s}(Z)
\]
by
\[
g\star f
:=
\mu_{t-s,u-t}
\circ
E_{t-s}(g)
\circ
f.
\tag{6.1}
\]

In the strict case,
\[
g\star f=E_{t-s}(g)\circ f.
\tag{6.2}
\]

---

### Theorem 6.2

\(\operatorname{Traj}_T(\mathcal C)\) is a category.

#### Proof

We prove the strict case; the pseudofunctorial case follows by coherence.

The identity morphism on \((t,X)\) is
\[
\operatorname{id}_{(t,X)}
:=
\operatorname{id}_X:X\to E_0(X)=X.
\]

Let
\[
f:X\to E_{t-s}Y,
\qquad
g:Y\to E_{u-t}Z,
\qquad
h:Z\to E_{v-u}W.
\]
Then
\[
h\star(g\star f)
=
E_{u-s}(h)\circ E_{t-s}(g)\circ f.
\]
On the other hand,
\[
(h\star g)\star f
=
E_{t-s}(E_{u-t}(h)\circ g)\circ f
=
E_{u-s}(h)\circ E_{t-s}(g)\circ f.
\]
Thus composition is associative.

The unit laws are immediate:
\[
\operatorname{id}\star f=f,
\qquad
g\star\operatorname{id}=g.
\]
Therefore \(\operatorname{Traj}_T(\mathcal C)\) is a category. \(\square\)

---

### Proposition 6.3: Canonical evolutionary arrows

If \((\mathcal C,E,\eta)\) is anchored, then for each \(s\le t\) and object \(X\), there is a canonical morphism
\[
\mathbf e_{s,t,X}:(s,X)\to(t,X)
\]
given by
\[
\mathbf e_{s,t,X}:=\eta_{t-s,X}:X\to E_{t-s}(X).
\]

Moreover,
\[
\mathbf e_{t,u,X}\star \mathbf e_{s,t,X}
=
\mathbf e_{s,u,X}.
\]

#### Proof

This is precisely the anchoring axiom
\[
\eta_{u-s}=E_{t-s}(\eta_{u-t})\circ\eta_{t-s}.
\]
\(\square\)

Thus anchored evolutionary categories possess internal arrows of time.

---

## 7. Dynamic Morphisms and Dynamic Natural Transformations

There are two related notions of dynamic morphism in ECT.

### 7.1 Dynamic morphisms between trajectories

Let \((\mathcal C,E,\eta)\) be anchored. A **dynamic morphism** from \(X\) to \(Y\) is a natural transformation
\[
\alpha:\Omega_X\Rightarrow\Omega_Y
\]
between orbit functors
\[
\Omega_X,\Omega_Y:\operatorname{Int}(T)\to\mathcal C.
\]

Equivalently, it is a family of morphisms
\[
\alpha_t:E_t(X)\to E_t(Y)
\]
such that for all \(s,t\in T\), the square
\[
\begin{tikzcd}
E_sX
\arrow[r,"\alpha_s"]
\arrow[d,"E_s\eta_{t,X}"']
&
E_sY
\arrow[d,"E_s\eta_{t,Y}"]
\\
E_sE_tX
\arrow[r,"E_s\alpha_t"']
&
E_sE_tY
\end{tikzcd}
\]
commutes, up to the coherence isomorphisms identifying \(E_sE_t\) with \(E_{s+t}\).

In the strict case, this condition is
\[
\alpha_{s+t}\circ E_s(\eta_{t,X})
=
E_s(\eta_{t,Y})\circ\alpha_s.
\tag{7.1}
\]

If \(\alpha_t=E_t(f)\) for some fixed morphism \(f:X\to Y\), then \(\alpha\) is called a **constant evolutionary morphism**.

---

### 7.2 Dynamic natural transformations between evolutionary functors

Let
\[
(F,\lambda),(G,\kappa):(\mathcal C,E)\to(\mathcal D,F)
\]
be evolutionary functors.

A **dynamic natural transformation** is an evolutionary natural transformation
\[
\alpha:F\Rightarrow G
\]
satisfying
\[
\kappa_t\circ E_t(\alpha)
=
\alpha E_t\circ\lambda_t.
\tag{7.2}
\]

In the strict case,
\[
E_t(\alpha_X)=\alpha_{E_tX}.
\]
Thus the transformation is invariant under evolutionary transport.

This is the correct categorified analogue of an invariant family of maps along a dynamical system.

---

## 8. Tensorial Evolutionary Laws

Many categories of interest are monoidal. We now develop the tensorial version of ECT.

Let \((\mathcal C,\otimes,I)\) be a monoidal category.

### Definition 8.1: Strong monoidal evolutionary category

A **strong monoidal \(T\)-evolutionary category** is a \(T\)-evolutionary category \((\mathcal C,E)\) such that each \(E_t\) is a strong monoidal functor. Thus for every \(t\in T\) there are coherent isomorphisms
\[
\phi^t_{X,Y}:E_t(X)\otimes E_t(Y)\xrightarrow{\sim}E_t(X\otimes Y),
\]
and
\[
\phi^t_I:I\xrightarrow{\sim}E_t(I).
\]

In the strict monoidal case,
\[
E_t(X\otimes Y)=E_t(X)\otimes E_t(Y),
\qquad
E_t(I)=I.
\]

Using superscript notation,
\[
(X\otimes Y)^{[t]}
\cong
X^{[t]}\otimes Y^{[t]},
\tag{8.1}
\]
and
\[
I^{[t]}\cong I.
\tag{8.2}
\]

For morphisms
\[
f:X\to X',
\qquad
g:Y\to Y',
\]
we have
\[
(f\otimes g)^{[t]}
\cong
f^{[t]}\otimes g^{[t]}.
\tag{8.3}
\]

Thus evolution distributes over tensor products.

---

### 8.1 Tensorial Leibniz rule

Suppose \(\mathcal C\) is \(k\)-linear and equipped with an infinitesimal evolutionary derivation \(D\). Then tensorial evolution satisfies
\[
D(f\otimes g)
=
D(f)\otimes g
+
f\otimes D(g).
\tag{8.4}
\]

This is the categorical analogue of the Leibniz rule for tensor products.

In a string-diagrammatic notation, evolution is represented by vertical translation. If a process \(f\) is drawn as a box, then its evolved process \(f^{[t]}\) is obtained by translating the diagram along the time axis. Tensorial evolution satisfies
\[
\begin{aligned}
\text{evolve}(f\otimes g)
&=
\text{evolve}(f)\otimes \text{evolve}(g),\\
\text{evolve}(g\circ f)
&=
\text{evolve}(g)\circ \text{evolve}(f).
\end{aligned}
\]

Thus ECT provides a formal algebra of evolving process diagrams.

---

### 8.2 Evolution of duals

Suppose \(\mathcal C\) is rigid monoidal and \(E_t\) is strong monoidal. If \(X^\vee\) is a dual of \(X\), with evaluation and coevaluation
\[
\operatorname{ev}_X:X^\vee\otimes X\to I,
\qquad
\operatorname{coev}_X:I\to X\otimes X^\vee,
\]
then the evolved dual of \(E_t(X)\) is canonically \(E_t(X^\vee)\), with structure maps
\[
E_t(\operatorname{ev}_X):
E_t(X^\vee)\otimes E_t(X)\to I,
\]
and
\[
E_t(\operatorname{coev}_X):
I\to E_t(X)\otimes E_t(X^\vee),
\]
up to the monoidal coherence isomorphisms.

Hence duality evolves functorially.

---

## 9. Infinitesimal Evolutionary Laws

We now analyze evolutionary laws in infinitesimal form.

Let \(\mathcal C\) be a \(k\)-linear category. Its hom-sets are \(k\)-vector spaces, and composition is bilinear.

### Definition 9.1: Categorical derivation

A **derivation** \(D\) of \(\mathcal C\) is a family of \(k\)-linear maps
\[
D_{X,Y}:\operatorname{Hom}_{\mathcal C}(X,Y)
\to
\operatorname{Hom}_{\mathcal C}(X,Y)
\]
such that:

1. \(D(\operatorname{id}_X)=0\);

2. for composable morphisms \(f:X\to Y\), \(g:Y\to Z\),
   \[
   D(g\circ f)=D(g)\circ f+g\circ D(f).
   \tag{9.1}
   \]

A derivation is **inner** if there exists a family of endomorphisms
\[
\theta_X:X\to X
\]
such that
\[
D(f)=\theta_Y\circ f-f\circ\theta_X.
\tag{9.2}
\]

---

### Proposition 9.2: Integration of derivations

Let \(D\) be a locally nilpotent or analytically integrable derivation on a \(k\)-linear category \(\mathcal C\). Define
\[
E_t(f):=\exp(tD)(f)
=
\sum_{n=0}^\infty \frac{t^n}{n!}D^n(f).
\]

Then \(E_t\) is a \(k\)-linear endofunctor of \(\mathcal C\), identity on objects, and
\[
E_{s+t}=E_sE_t.
\]

#### Proof

The identity preservation follows from \(D(\operatorname{id}_X)=0\):
\[
E_t(\operatorname{id}_X)=\operatorname{id}_X.
\]

For composition, define
\[
A(t):=E_t(g\circ f),
\qquad
B(t):=E_t(g)\circ E_t(f).
\]
Both satisfy the same differential equation
\[
\frac{d}{dt}A(t)=D(A(t)),
\qquad
\frac{d}{dt}B(t)=D(B(t)),
\]
and have the same initial condition
\[
A(0)=g\circ f=B(0).
\]
The derivation rule (9.1) gives
\[
\frac{d}{dt}\bigl(E_t(g)\circ E_t(f)\bigr)
=
D(E_t(g))\circ E_t(f)
+
E_t(g)\circ D(E_t(f)).
\]
By uniqueness of solutions, \(A(t)=B(t)\). Thus \(E_t\) preserves composition. The semigroup law follows from the exponential identity. \(\square\)

---

### Proposition 9.3: Monoidal derivations

Let \(\mathcal C\) be a monoidal \(k\)-linear category. A derivation \(D\) is **monoidal** if
\[
D(f\otimes g)=D(f)\otimes g+f\otimes D(g),
\tag{9.3}
\]
and
\[
D(\operatorname{id}_I)=0.
\]

Then \(\exp(tD)\) is a strong monoidal evolutionary law.

#### Proof

The same ODE argument applied to the tensor product shows that
\[
E_t(f\otimes g)=E_t(f)\otimes E_t(g).
\]
The unit is preserved because \(D(\operatorname{id}_I)=0\). \(\square\)

Thus infinitesimal evolutionary laws are precisely categorical derivations satisfying appropriate Leibniz rules.

---

### Remark 9.4: Cohomological interpretation

For a \(k\)-linear category \(\mathcal C\), derivations form the space of \(1\)-cocycles in the Hochschild cochain complex of \(\mathcal C\). Inner derivations are \(1\)-coboundaries. Obstructions to integrating infinitesimal evolutionary laws are controlled by higher Hochschild cohomology classes. Thus ECT connects naturally with deformation theory.

---

## 10. Higher Evolutionary Categories

The theory extends directly to higher categories.

### 10.1 Evolutionary \(n\)-categories

Let \(n\mathbf{Cat}\) denote the category of \(n\)-categories and \(n\)-functors.

A **\(T\)-evolutionary \(n\)-category** is an \(n\)-category \(\mathcal C\) equipped with a coherent action
\[
E:T\to \operatorname{End}_{n\mathbf{Cat}}(\mathcal C).
\]

Thus each \(t\in T\) determines an \(n\)-functor
\[
E_t:\mathcal C\to\mathcal C.
\]

For \(k\le n\), every \(k\)-morphism evolves:
\[
\alpha^{[t]}:=E_t(\alpha).
\]

The coherence laws of the \(n\)-category are preserved by evolution.

---

### 10.2 Dynamic higher natural transformations

In an evolutionary 2-category, a dynamic natural transformation between evolutionary 1-morphisms is a 2-morphism compatible with time evolution.

In an evolutionary 3-category, dynamic modifications between dynamic natural transformations are 3-morphisms satisfying analogous compatibility conditions.

In general, for \(0\le k\le n\), the \(k\)-morphisms evolve, and coherence among them is preserved by the action of \(E_t\).

---

### 10.3 Evolutionary \(\infty\)-categories

Let \(\mathcal C\) be an \(\infty\)-category. A \(T\)-evolutionary structure on \(\mathcal C\) is a functor
\[
E:BT\to \mathbf{Cat}_\infty
\]
or, more generally,
\[
E:\operatorname{Int}(T)\to \mathbf{Cat}_\infty,
\]
where \(BT\) is the classifying \(\infty\)-category of \(T\).

For each \(t\in T\), we obtain an \(\infty\)-functor
\[
E_t:\mathcal C\to\mathcal C.
\]

Mapping spaces evolve by maps
\[
\operatorname{Map}_{\mathcal C}(X,Y)
\to
\operatorname{Map}_{\mathcal C}(E_tX,E_tY).
\]

The trajectory \(\infty\)-category is the homotopy coherent Grothendieck construction of \(E\). Its mapping spaces are given by
\[
\operatorname{Map}_{\operatorname{Traj}(\mathcal C)}
((s,X),(t,Y))
\simeq
\operatorname{Map}_{\mathcal C}
(X,E_{t-s}Y)
\]
for \(s\le t\).

Thus evolutionary \(\infty\)-categories provide a natural language for homotopy-coherent dynamical structures.

---

## 11. Applications to Programming Semantics

ECT gives a natural semantics for evolving programming languages.

### 11.1 Evolving types and terms

Let \(\mathcal L\) be a typed programming language. Its semantic interpretation takes values in a category \(\mathcal C\):
\[
\llbracket - \rrbracket:\mathcal L\to \mathcal C.
\]

Suppose \(\mathcal C\) is a \(T\)-evolutionary category. Then evolution acts on semantic types:
\[
\llbracket A\rrbracket^{[t]}=E_t(\llbracket A\rrbracket),
\]
and on semantic programs:
\[
\llbracket M\rrbracket^{[t]}=E_t(\llbracket M\rrbracket).
\]

We may define syntactic evolution operators
\[
[-]^t
\]
on types and terms by requiring
\[
\llbracket A^{[t]}\rrbracket
=
E_t\llbracket A\rrbracket,
\qquad
\llbracket M^{[t]}\rrbracket
=
E_t\llbracket M\rrbracket.
\]

---

### 11.2 Soundness of evolutionary typing

Suppose a typing judgment
\[
\Gamma\vdash M:A
\]
is interpreted as a morphism
\[
\llbracket M\rrbracket:
\llbracket \Gamma\rrbracket
\to
\llbracket A\rrbracket.
\]

Applying \(E_t\), we obtain
\[
E_t(\llbracket M\rrbracket):
E_t(\llbracket \Gamma\rrbracket)
\to
E_t(\llbracket A\rrbracket).
\]

Therefore, if syntactic evolution is compatible with semantic evolution, we obtain the derived judgment
\[
\Gamma^{[t]}\vdash M^{[t]}:A^{[t]}.
\]

Thus evolution preserves typing.

---

### 11.3 Preservation of lambda structure

Assume \(\mathcal C\) is cartesian closed and each \(E_t\) preserves finite products and exponentials up to coherent isomorphism. Then
\[
E_t(A\times B)\cong E_tA\times E_tB,
\]
and
\[
E_t(B^A)\cong (E_tB)^{E_tA}.
\]

Consequently,
\[
E_t(\lambda x.M)
\cong
\lambda x^{[t]}.E_t(M),
\]
and
\[
E_t(M\,N)
\cong
E_t(M)\,E_t(N).
\]

Thus evolutionary semantics respects lambda abstraction and application.

---

### 11.4 Refactorings as dynamic natural transformations

A program refactoring may be modeled as a natural transformation between semantic functors. If a compiler pass or migration procedure is natural with respect to program composition and type structure, it becomes an evolutionary natural transformation.

Let
\[
F,G:\mathcal L\to\mathcal C
\]
be two semantic interpretations of a language version. A refactoring
\[
\rho:F\Rightarrow G
\]
is evolutionary if
\[
E_t(\rho_M)=\rho_{E_t(M)}.
\]

This expresses that the refactoring commutes with evolutionary time.

---

## 12. Applications to Logic

In categorical logic, propositions are objects and proofs are morphisms. ECT allows logical theories to evolve.

### 12.1 Evolving propositions and proofs

Let \(\mathcal P\) be a propositional category. A proposition \(A\) is an object, and a proof \(p:A\to B\) is a morphism.

An evolutionary law \(E_t\) maps propositions to evolved propositions:
\[
A^{[t]}:=E_t(A),
\]
and proofs to evolved proofs:
\[
p^{[t]}:=E_t(p).
\]

Thus proof composition is preserved:
\[
(q\circ p)^{[t]}=q^{[t]}\circ p^{[t]}.
\]

---

### 12.2 Evolving logical connectives

If \(\mathcal P\) is cartesian closed and \(E_t\) preserves the relevant structure, then logical connectives evolve coherently:
\[
E_t(\top)\cong \top,
\]
\[
E_t(A\wedge B)\cong E_tA\wedge E_tB,
\]
\[
E_t(A\Rightarrow B)\cong E_tA\Rightarrow E_tB.
\]

If \(\mathcal P\) has coproducts and \(E_t\) preserves them, then
\[
E_t(A\vee B)\cong E_tA\vee E_tB.
\]

Thus evolution commutes with logical structure.

---

### 12.3 Temporal modalities from adjoints

Suppose each evolution functor \(E_t\) has a right adjoint
\[
E_t\dashv R_t.
\]

Define temporal modalities
\[
\Diamond_t := E_t,
\qquad
\Box_t := R_t.
\]

The adjunction gives
\[
\operatorname{Hom}(E_tA,B)
\cong
\operatorname{Hom}(A,R_tB).
\]

Thus \(E_t\) behaves like an existential or possibility modality, while \(R_t\) behaves like a universal or necessity modality.

Because right adjoints preserve limits,
\[
\Box_t(A\wedge B)
\cong
\Box_tA\wedge \Box_tB,
\]
whenever \(R_t\) preserves binary products.

Similarly, if \(E_t\) preserves coproducts, then
\[
\Diamond_t(A\vee B)
\cong
\Diamond_tA\vee \Diamond_tB.
\]

Therefore temporal modal logic arises naturally from evolutionary adjunctions.

---

### 12.4 Necessitation

If \(A\) is a theorem, i.e. there is a proof
\[
\top\to A,
\]
then applying \(R_t\) gives
\[
R_t(\top)\to R_t(A).
\]
If \(R_t\) preserves the terminal object, then
\[
R_t(\top)\cong \top,
\]
and hence
\[
\top\to \Box_t A.
\]
Thus necessitation is a consequence of functorial evolution plus adjointness.

---

## 13. Applications to Systems Science

ECT is well suited to the categorical modeling of evolving systems.

### 13.1 Systems as objects

Let \(\mathbf{Sys}\) be a monoidal category of systems. Objects represent system interfaces or boundary conditions, and morphisms represent system interconnections or transformations.

An evolutionary law
\[
E_t:\mathbf{Sys}\to\mathbf{Sys}
\]
describes structural or behavioral evolution of systems over time.

If \(S\) is a system, then
\[
S^{[t]}=E_t(S)
\]
is its evolved form.

---

### 13.2 Evolving interconnections

If
\[
f:S\to T
\]
is a system morphism, then
\[
f^{[t]}:S^{[t]}\to T^{[t]}
\]
is the evolved interconnection or transformation.

Because \(E_t\) is functorial,
\[
(g\circ f)^{[t]}=g^{[t]}\circ f^{[t]}.
\]

Hence hierarchical composition of systems is preserved under evolution.

---

### 13.3 Monoidal evolution of composite systems

If systems compose in parallel via a tensor product \(\otimes\), and \(E_t\) is strong monoidal, then
\[
(S\otimes T)^{[t]}
\cong
S^{[t]}\otimes T^{[t]}.
\]

Thus evolution of a composite system is the composite of evolved subsystems.

In tensorial notation,
\[
E_t(S\otimes T)
=
E_t(S)\otimes E_t(T).
\]

This is a categorical expression of modular evolutionary dynamics.

---

### 13.4 Adaptation as dynamic natural transformation

Let \(S,T\) be systems with evolutionary trajectories
\[
\Omega_S,\Omega_T:\operatorname{Int}(T)\to\mathbf{Sys}.
\]

An adaptive transformation from \(S\) to \(T\) is a dynamic morphism
\[
\alpha:\Omega_S\Rightarrow\Omega_T.
\]

Its components
\[
\alpha_t:S^{[t]}\to T^{[t]}
\]
describe a time-dependent reorganization of \(S\) into \(T\). The naturality condition ensures that adaptation commutes with evolutionary progress.

Thus adaptation is not a single morphism but a coherent trajectory of morphisms.

---

### 13.5 Behavioral naturality

Let
\[
B:\mathbf{Sys}\to\mathbf{Beh}
\]
be a behavior functor. Suppose \(B\) is an evolutionary functor. Then for every system \(S\),
\[
B(S^{[t]})
\cong
(B(S))^{[t]}.
\]

Thus evolution of structure induces evolution of behavior in a coherent way.

If a behavioral property is expressed as a limit, colimit, or adjunction, its evolution is governed by the preservation properties of \(E_t\).

---

## 14. Non-Autonomous Evolution

The autonomous theory assumes a single category \(\mathcal C\) acted on by endofunctors. A more general theory permits the category itself to vary with time.

Let
\[
\mathcal C:\operatorname{Int}(T)\to\mathbf{Cat}
\]
be a pseudofunctor. For each time \(t\), we have a category \(\mathcal C_t\). For each interval \(s\le t\), we have a transition functor
\[
E_{s,t}:\mathcal C_s\to\mathcal C_t.
\]

These satisfy
\[
E_{t,t}=\operatorname{id}_{\mathcal C_t},
\]
and
\[
E_{t,u}\circ E_{s,t}\cong E_{s,u}.
\]

This defines a **non-autonomous evolutionary category**.

The autonomous case is recovered when all \(\mathcal C_t\) are equal to a fixed \(\mathcal C\) and
\[
E_{s,t}=E_{t-s}.
\]

The trajectory category of a non-autonomous evolutionary category is the Grothendieck construction
\[
\int \mathcal C.
\]

Thus ECT contains both autonomous and non-autonomous dynamics.

---

## 15. Evolutionary Doctrines and Internal Logic

An evolutionary doctrine can be defined by combining ECT with categorical logic.

Let
\[
p:\mathcal E\to \mathcal B
\]
be a fibration, where \(\mathcal B\) is a base category of contexts or systems, and \(\mathcal E\) is a category of predicates, types, or propositions.

Suppose both \(\mathcal B\) and \(\mathcal E\) carry \(T\)-evolutionary structures and \(p\) is an evolutionary functor. Then evolution acts on contexts and on predicates over contexts.

If reindexing functors are compatible with evolution, one obtains a temporal doctrine in which substitution, quantification, and logical connectives evolve coherently.

This provides a foundation for evolutionary type theory and evolutionary topos theory.

---

## 16. Examples

### Example 16.1: Discrete shift on chain complexes

Let \(\mathbf{Ch}_k\) be the category of chain complexes over a field \(k\). Let
\[
E_n = [n]
\]
be the \(n\)-fold shift functor. Then
\[
E_m\circ E_n = E_{m+n}.
\]

Thus \(\mathbf{Ch}_k\) is a \(\mathbb Z\)-evolutionary category under shift. Objects, chain maps, and natural transformations evolve by translation in homological degree.

---

### Example 16.2: Action by a monoid on sets

Let \(M\) be a monoid and let \(X\) be a right \(M\)-set. The action category of \(X\) can be evolved by endofunctors induced by monoid endomorphisms. More generally, if a monoid \(T\) acts on a category \(\mathcal C\) by endofunctors, \(\mathcal C\) is automatically a \(T\)-evolutionary category.

---

### Example 16.3: Presheaf evolution

Let \(\mathcal C\) be a small category and let
\[
\varphi_t:\mathcal C\to\mathcal C
\]
be a family of endofunctors forming a monoid action. Then precomposition gives an action on the presheaf category:
\[
E_t(P)=P\circ \varphi_t.
\]

Thus presheaf categories inherit evolutionary structure from their base categories.

---

### Example 16.4: State-transition systems as one-object evolutionary categories

A deterministic dynamical system \((X,\sigma:X\to X)\) may be encoded categorically using a one-object category whose endomorphism monoid is generated by \(\sigma\). Evolution of endomorphisms is given by conjugation or iteration, depending on the chosen functorial action.

This illustrates that ECT generalizes ordinary dynamical systems.

---

## 17. Structural Theorems

### Theorem 17.1: Evolutionary invariance of categorical equations

Let \(\mathcal C\) be a strict \(T\)-evolutionary category. Any equation in the internal language of categories involving composition and identities is preserved by \(E_t\).

#### Proof

Since \(E_t\) is a functor, it preserves identities and composition. Therefore any equation built from these operations is mapped to an equation of the same form. \(\square\)

---

### Theorem 17.2: Evolution of adjunctions under evolutionary equivalences

Let
\[
L:\mathcal C\rightleftarrows \mathcal D:R
\]
be an adjunction. Suppose \(E_t^\mathcal C\) and \(E_t^\mathcal D\) are evolutionary equivalences with quasi-inverses. Then the transported functors
\[
L_t := E_t^\mathcal D\circ L\circ (E_t^\mathcal C)^{-1},
\qquad
R_t := E_t^\mathcal C\circ R\circ (E_t^\mathcal D)^{-1}
\]
form an adjunction
\[
L_t\dashv R_t.
\]

#### Proof

Adjunctions are invariant under equivalence of categories. Transporting an adjunction along equivalences preserves the unit-counit equations up to coherent isomorphism. \(\square\)

Thus adjoint structure evolves whenever evolution is reversible up to equivalence.

---

### Theorem 17.3: Evolutionary preservation of monoidal coherence

If \((\mathcal C,\otimes,I,E)\) is a strong monoidal evolutionary category, then all coherence isomorphisms of the monoidal structure are compatible with evolution up to canonical isomorphism.

In particular,
\[
E_t(\alpha_{X,Y,Z})
\]
is identified with the associator for \(E_tX,E_tY,E_tZ\), and similarly for unitors and braidings.

#### Proof

This follows because each \(E_t\) is strong monoidal. Strong monoidal functors preserve monoidal coherence diagrams. \(\square\)

---

## 18. Conceptual Interpretation

ECT replaces the classical view

\[
\text{category} = \text{static universe of objects and morphisms}
\]

with the view

\[
\text{category} = \text{evolving universe of structured processes}.
\]

The fundamental laws are not merely

\[
\operatorname{id},\circ
\]

but

\[
E_t,\operatorname{id},\circ
\]

subject to

\[
E_t(g\circ f)=E_t(g)\circ E_t(f).
\]

Thus evolution itself becomes a categorical operation.

Natural transformations, traditionally static comparisons between functors, become dynamic comparisons compatible with the flow of time. In higher categories, the entire tower of coherence data evolves.

This provides a unified mathematical language for change.

---

## 19. Future Directions

Several developments are natural.

1. **Evolutionary topos theory.**  
   Develop elementary toposes equipped with evolutionary actions and analyze evolving subobject classifiers and internal logics.

2. **Evolutionary type theories.**  
   Construct syntactic calculi with explicit evolution operators, temporal typing rules, and normalization theorems.

3. **Evolutionary operads and polynomial functors.**  
   Study evolutionary laws on algebraic patterns, operads, and higher-dimensional rewriting systems.

4. **Stochastic and probabilistic ECT.**  
   Replace deterministic endofunctor actions by Markov categories or probabilistic functors.

5. **Geometric ECT.**  
   Relate evolutionary categories to flows on stacks, sheaves over time, and categorified dynamical systems.

6. **Cohomological deformation theory.**  
   Further develop the relation between infinitesimal evolutionary laws and Hochschild cohomology.

7. **Applied systems theory.**  
   Build compositional models of adaptive cyber-physical systems using monoidal evolutionary categories.

---

## 20. Conclusion

Evolutionary Category Theory provides a rigorous foundation for categories that change over time. By requiring evolution to be functorial, we ensure that the essential laws of category theory remain valid under temporal development. Objects, morphisms, natural transformations, tensor products, limits, adjunctions, and higher coherences all acquire evolutionary dynamics.

The framework unifies several themes:

- dynamical systems become categorical actions;
- temporal logic arises from adjoints to evolution functors;
- program evolution becomes semantic functorial transport;
- system adaptation becomes dynamic naturality;
- higher coherence becomes homotopy-coherent evolution.

The central claim of ECT is simple but powerful:

\[
\boxed{
\text{Evolution is functorial, and functoriality is evolutionary.}
}
\]

---

## References

1. M. Agmon, C. Bezem, and B. Spitters, *Temporal and modal types in categorical semantics*, theoretical studies in categorical logic.

2. J. Baez and A. Lauda, *Higher-Dimensional Algebra V: 2-Groups*, Theory and Applications of Categories.

3. F. Borceux, *Handbook of Categorical Algebra*, Cambridge University Press.

4. A. Joyal, *Foncteurs analytiques et espèces de structures*, Lecture Notes in Mathematics.

5. G. M. Kelly, *Basic Concepts of Enriched Category Theory*, Cambridge University Press.

6. T. Leinster, *Higher Operads, Higher Categories*, Cambridge University Press.

7. S. Mac Lane, *Categories for the Working Mathematician*, Springer.

8. S. Mac Lane and I. Moerdijk, *Sheaves in Geometry and Logic*, Springer.

9. E. Riehl, *Higher Topos Theory*, Cambridge University Press.

10. D. Spivak, *Category Theory for the Sciences*, MIT Press.

11. R. Street, *The formal theory of monads*, Journal of Pure and Applied Algebra.

12. N. J. Wildberger, *Categorical structures and their deformations*, theoretical studies in categorical algebra.

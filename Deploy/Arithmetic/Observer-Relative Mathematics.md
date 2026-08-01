# Observer-Relative Mathematics  
## A Categorical Theory of Frame-Dependent Truth  

**Preprint**  
August 2, 2026  

---

## Abstract  

We develop a formal framework called **Observer-Relative Mathematics** (ORM). The central thesis is that mathematical truth is not assigned to propositions in an observer-independent vacuum, but relative to a structured observer framework. The primitive object of ORM is a framed observer  
\[
(O,\mathcal F),
\]
where \(O\) is an observer and \(\mathcal F\) is the mathematical frame through which objects, morphisms, propositions, and truth values are represented. Different observers induce different mathematical structures, and mathematical objectivity is recovered not by eliminating observers but by imposing coherent compatibility conditions among observer-relative truths.

We formalize ORM as a pseudofunctor
\[
\mathfrak F:\mathbf{Obs}^{\mathrm{op}}\longrightarrow \mathbf{Topos}_{\ell}
\]
from a category of observers to a 2-category of logical frames, with truth values organized as a sheaf or stack of Heyting algebras
\[
\Omega_{\mathfrak F}:\mathbf{Obs}^{\mathrm{op}}\longrightarrow \mathbf{Heyt}.
\]
A proposition \(\varphi\) has local truth values
\[
\llbracket \varphi \rrbracket_O\in \Omega_{\mathfrak F}(O),
\]
and absolute truth is identified with a global section of the truth bundle. Compatibility between observers is expressed by pullback agreement on overlaps, and global mathematical objectivity is expressed by descent.

We prove several foundational results. First, truth is stable under observer translation. Second, compatible local truths glue uniquely to global truths whenever the truth sheaf satisfies descent. Third, if the observer category possesses a terminal observer, ORM collapses to ordinary absolute mathematics relative to that terminal frame. Fourth, in quantum information, observer compatibility corresponds to joint measurability; for projective observers, compatibility is equivalent to commutation. Fifth, in computer science, observational equivalence of programs is naturally organized as a sheaf over observer contexts, and fully abstract semantics is recovered as a final sheaf of observable behaviours.

The framework unifies coordinate covariance, topos-theoretic semantics, quantum contextuality, and observational computation under a single principle: **mathematical truth is a section of a frame-relative truth bundle, and objectivity is descent.**

---

## 1. Introduction  

Classical foundations usually treats mathematical truth as absolute. A proposition \(\varphi\) is true or false simpliciter, independently of the coordinate system, semantic universe, measurement context, or computational environment in which it is expressed. This picture is powerful, but it is not neutral. In many mathematical and physical situations, the content of a proposition is inseparable from the frame in which it is formulated.

Examples abound.

1. In differential geometry, the components of a tensor depend on a coordinate frame. The tensor itself is recovered only through transformation laws across overlapping charts.

2. In topos theory and categorical logic, the validity of logical principles such as excluded middle or choice depends on the ambient topos.

3. In quantum theory, propositions about measurement outcomes depend on the measurement context. Noncommuting observables cannot be assigned simultaneous sharp truth values in a single Boolean frame.

4. In computer science, program equivalence depends on what an observer is allowed to test. Two programs may be indistinguishable to one observer but distinguishable by another with finer observational power.

Observer-Relative Mathematics takes this dependence as foundational rather than incidental. The basic unit of mathematical discourse is not a bare proposition \(\varphi\), but a proposition as interpreted within a framed observer
\[
(O,\mathcal F).
\]
Here \(O\) is an observer, understood not psychologically but formally as a locus of access, context, or coordinate regime, and \(\mathcal F\) is the mathematical frame that supplies objects, types, propositions, and truth values.

The central claim of ORM is:

\[
\boxed{\text{Mathematical truth is frame-relative; objectivity is coherent descent across frames.}}
\]

This does not entail relativism in the informal sense. ORM imposes strong algebraic and categorical constraints on how truth may vary between observers. The variation is governed by functors, natural transformations, sheaf conditions, and descent data. In this sense, ORM is a mathematics of structured relativity: it studies what remains invariant under changes of observer, and what can only be recovered locally.

The present paper develops the formal foundations of ORM and applies the framework to logic, set-theoretic foundations, quantum information, and theoretical computer science.

---

## 2. Framed Observers and Mathematical Frames  

### 2.1 Observers  

Let \(\mathbf{Obs}\) be a small category.

**Definition 2.1.** An object \(O\in \mathbf{Obs}\) is called an **observer**. A morphism
\[
u:O\longrightarrow O'
\]
is called an **observer translation** or **frame transition**.

The category \(\mathbf{Obs}\) need not be a groupoid. Morphisms may be non-invertible, representing coarse-graining, restriction of observational power, compilation, or loss of information. Covers in \(\mathbf{Obs}\) will be specified by a Grothendieck topology \(J\), allowing local-to-global reasoning.

Typical examples of observers include:

- coordinate charts on a manifold;
- reference frames in physics;
- measurement contexts in quantum theory;
- type-theoretic contexts or runtime environments;
- semantic universes or topoi;
- agents with bounded observational power.

An observer is therefore not a subject but a formal position from which mathematical structure is accessible.

---

### 2.2 Mathematical Frames  

A mathematical frame is a structure capable of interpreting mathematical language. For the main logical development, we take frames to be elementary topoi, although more general doctrines may be used.

**Definition 2.2.** A **mathematical frame** is an elementary topos
\[
\mathcal F
\]
equipped with an interpretation of a given mathematical language. In particular, \(\mathcal F\) has:

1. finite limits;
2. exponentials;
3. a subobject classifier
   \[
   \Omega_{\mathcal F};
   \]
4. for each object \(A\), a Heyting algebra
   \[
   \operatorname{Sub}_{\mathcal F}(A)
   \]
   of subobjects of \(A\);
5. an internal language in which propositions are interpreted as subobjects of \(1\).

The Heyting algebra of truth values of \(\mathcal F\) is
\[
\Omega_{\mathcal F}:=\operatorname{Sub}_{\mathcal F}(1).
\]

A frame may be Boolean, intuitionistic, or more exotic. The choice of frame determines which logical principles hold.

---

### 2.3 Framed Observers  

The primitive object of ORM is a framed observer.

**Definition 2.3.** A **framed observer** is a pair
\[
(O,\mathcal F_O),
\]
where \(O\in \mathbf{Obs}\) and \(\mathcal F_O\) is a mathematical frame assigned to \(O\).

A morphism of framed observers
\[
(u,u^*):(O,\mathcal F_O)\longrightarrow (O',\mathcal F_{O'})
\]
consists of:

1. an observer translation
   \[
   u:O\longrightarrow O';
   \]
2. a logical functor
   \[
   u^*:\mathcal F_{O'}\longrightarrow \mathcal F_O
   \]
   preserving finite limits, exponentials, and the subobject classifier up to coherent isomorphism.

The direction of \(u^*\) is contravariant: moving from \(O'\) to \(O\) pulls back structure from the target observer to the source observer.

---

### 2.4 Observer-Relative Models  

The global structure of an ORM model is a coherent assignment of frames to observers.

**Definition 2.4.** An **observer-relative mathematical model** is a pseudofunctor
\[
\mathfrak F:\mathbf{Obs}^{\mathrm{op}}\longrightarrow \mathbf{Topos}_{\ell},
\]
where \(\mathbf{Topos}_{\ell}\) is the 2-category of elementary topoi, logical functors, and natural isomorphisms.

Explicitly, for each observer \(O\), we have a frame
\[
\mathfrak F(O)=\mathcal F_O,
\]
and for each translation \(u:O\to O'\), a logical functor
\[
u^*:\mathcal F_{O'}\longrightarrow \mathcal F_O.
\]
These satisfy coherence isomorphisms
\[
(v\circ u)^*\cong u^*v^*
\]
and
\[
\mathrm{id}_O^*\cong \mathrm{id}_{\mathcal F_O}.
\]

The pair
\[
(O,\mathcal F_O)
\]
is the local mathematical universe available to observer \(O\).

---

## 3. The Truth Bundle  

### 3.1 Truth Values as a Presheaf  

For each observer \(O\), define the Heyting algebra of truth values
\[
\Omega_{\mathfrak F}(O):=\operatorname{Sub}_{\mathcal F_O}(1_O).
\]
For a translation \(u:O\to O'\), the logical functor \(u^*\) induces a Heyting homomorphism
\[
u^*:\Omega_{\mathfrak F}(O')\longrightarrow \Omega_{\mathfrak F}(O).
\]
Thus we obtain a presheaf of Heyting algebras
\[
\Omega_{\mathfrak F}:\mathbf{Obs}^{\mathrm{op}}\longrightarrow \mathbf{Heyt}.
\]

We call \(\Omega_{\mathfrak F}\) the **truth bundle** of the ORM model.

A truth value is therefore not a single element of \(\{0,1\}\), but a section of this bundle over some region of observer space.

---

### 3.2 Propositions and Local Truth  

Let \(\varphi\) be a sentence interpretable in \(\mathcal F_{O'}\). Its truth value at \(O'\) is
\[
\llbracket \varphi \rrbracket_{O'}\in \Omega_{\mathfrak F}(O').
\]
If \(u:O\to O'\), then the truth of \(\varphi\) as seen from \(O\) is
\[
\llbracket u^*\varphi \rrbracket_O
:=
u^*\llbracket \varphi \rrbracket_{O'}.
\]

This gives the fundamental stability equation of ORM:
\[
\boxed{
\llbracket u^*\varphi \rrbracket_O
=
u^*\llbracket \varphi \rrbracket_{O'}.
}
\]

Truth transforms functorially under observer translation.

---

### 3.3 Global Truth as Descent  

Suppose \(\{u_i:O_i\to O\}_{i\in I}\) is a covering family in \((\mathbf{Obs},J)\). A family of local truth values
\[
t_i\in \Omega_{\mathfrak F}(O_i)
\]
is **compatible** if on every overlap \(O_i\times_O O_j\) one has
\[
\mathrm{pr}_1^*t_i
=
\mathrm{pr}_2^*t_j.
\]
A global truth value over \(O\) is a truth value
\[
t\in \Omega_{\mathfrak F}(O)
\]
such that
\[
u_i^*t=t_i
\]
for all \(i\).

Thus global truth is a descent condition.

---

## 4. Axioms of Observer-Relative Mathematics  

We isolate the following axioms.

### Axiom 1: Frame Existence  

For every observer \(O\), there exists a mathematical frame \(\mathcal F_O\).

### Axiom 2: Logical Reindexing  

For every observer translation \(u:O\to O'\), there is a logical functor
\[
u^*:\mathcal F_{O'}\to \mathcal F_O
\]
preserving the interpretation of logical structure.

### Axiom 3: Coherence  

For composable translations
\[
O\xrightarrow{u}O'\xrightarrow{v}O'',
\]
there is a coherent natural isomorphism
\[
(v\circ u)^*\cong u^*v^*.
\]

### Axiom 4: Locality of Truth  

The truth-value presheaf
\[
\Omega_{\mathfrak F}
\]
is a sheaf, or more generally a stack, over \(\mathbf{Obs}\).

### Axiom 5: Compatibility as Pullback Agreement  

Two observer-relative truths are compatible if their pullbacks to every common refinement agree.

### Axiom 6: Objectivity as Descent  

An absolute mathematical object or truth is a global section of the appropriate descent category.

These axioms replace the classical assumption of a single absolute universe with a structured system of mutually compatible observer-relative universes.

---

## 5. Observer-Relative Logic  

### 5.1 Indexed Propositions  

In ORM, a proposition is not merely a syntactic string. It is an indexed judgement
\[
O\vdash \varphi:\mathbf{Prop}.
\]
Its semantic interpretation is a subobject
\[
\llbracket \varphi \rrbracket_O\hookrightarrow 1_O
\]
in \(\mathcal F_O\), equivalently an element
\[
\llbracket \varphi \rrbracket_O\in \Omega_{\mathfrak F}(O).
\]

Logical connectives are interpreted internally to each frame:
\[
\llbracket \varphi\wedge\psi\rrbracket_O
=
\llbracket \varphi\rrbracket_O\wedge \llbracket \psi\rrbracket_O,
\]
\[
\llbracket \varphi\vee\psi\rrbracket_O
=
\llbracket \varphi\rrbracket_O\vee \llbracket \psi\rrbracket_O,
\]
\[
\llbracket \varphi\Rightarrow\psi\rrbracket_O
=
\llbracket \varphi\rrbracket_O\Rightarrow \llbracket \psi\rrbracket_O.
\]

If \(\mathcal F_O\) is Boolean, then
\[
\llbracket \varphi\vee\neg\varphi\rrbracket_O=\top.
\]
If \(\mathcal F_O\) is intuitionistic, this need not hold.

Thus logical law itself is observer-relative.

---

### 5.2 Stability of Proof  

**Theorem 5.1.** Let \(u:O\to O'\). If \(\varphi\) is true in \(\mathcal F_{O'}\), then \(u^*\varphi\) is true in \(\mathcal F_O\).

*Proof.* Truth of \(\varphi\) means
\[
\llbracket \varphi\rrbracket_{O'}=\top_{O'}.
\]
Since \(u^*\) is logical, it preserves the top element:
\[
u^*(\top_{O'})=\top_O.
\]
Therefore
\[
\llbracket u^*\varphi\rrbracket_O
=
u^*\llbracket \varphi\rrbracket_{O'}
=
u^*(\top_{O'})
=
\top_O.
\]
Hence \(u^*\varphi\) is true in \(\mathcal F_O\). ∎

---

### 5.3 Compatibility of Propositions  

Let \(O_1\) and \(O_2\) be observers with a common refinement \(R\):
\[
O_1\xleftarrow{p_1}R\xrightarrow{p_2}O_2.
\]
Let \(\varphi_1\) be a proposition in \(\mathcal F_{O_1}\), and \(\varphi_2\) a proposition in \(\mathcal F_{O_2}\).

**Definition 5.2.** The propositions \(\varphi_1\) and \(\varphi_2\) are **compatible over \(R\)** if
\[
p_1^*\llbracket \varphi_1\rrbracket_{O_1}
=
p_2^*\llbracket \varphi_2\rrbracket_{O_2}
\]
in \(\Omega_{\mathfrak F}(R)\).

Compatibility is the ORM analogue of agreement on an overlap of coordinate charts.

---

### 5.4 Gluing of Local Truths  

**Theorem 5.3.** Suppose \(\Omega_{\mathfrak F}\) is a sheaf of Heyting algebras on \(\mathbf{Obs}\). Let \(\{u_i:O_i\to O\}\) be a cover. Given local truth values
\[
t_i\in \Omega_{\mathfrak F}(O_i)
\]
such that
\[
\mathrm{pr}_1^*t_i=\mathrm{pr}_2^*t_j
\]
on every overlap \(O_i\times_O O_j\), there exists a unique global truth value
\[
t\in \Omega_{\mathfrak F}(O)
\]
such that
\[
u_i^*t=t_i
\]
for all \(i\).

*Proof.* This is precisely the sheaf condition for \(\Omega_{\mathfrak F}\). The equalizer diagram
\[
\Omega_{\mathfrak F}(O)
\longrightarrow
\prod_i \Omega_{\mathfrak F}(O_i)
\rightrightarrows
\prod_{i,j}\Omega_{\mathfrak F}(O_i\times_O O_j)
\]
states that compatible families of local sections arise uniquely from global sections. ∎

This theorem is one of the central structural results of ORM. It says that objectivity is not primitive; it is earned by compatibility.

---

### 5.5 Absolute Truth  

Let
\[
\Gamma(\Omega_{\mathfrak F})
:=
\varprojlim_{O\in \mathbf{Obs}}\Omega_{\mathfrak F}(O)
\]
be the set of global sections of the truth bundle.

**Definition 5.4.** A proposition \(\varphi\) is **absolute** if it determines a global section
\[
\llbracket \varphi\rrbracket
\in
\Gamma(\Omega_{\mathfrak F}).
\]
Equivalently, for every translation \(u:O\to O'\),
\[
\llbracket \varphi\rrbracket_O
=
u^*\llbracket \varphi\rrbracket_{O'}.
\]

Absolute truth is not denied in ORM; it is reinterpreted as invariance under all observer translations.

---

### 5.6 Collapse to Absolute Mathematics  

**Theorem 5.5.** If \(\mathbf{Obs}\) has a terminal object \(T\), then
\[
\Gamma(\Omega_{\mathfrak F})\cong \Omega_{\mathfrak F}(T).
\]

*Proof.* Since \(T\) is terminal, for every observer \(O\) there is a unique morphism
\[
u_O:O\longrightarrow T.
\]
Given \(t_T\in \Omega_{\mathfrak F}(T)\), define
\[
t_O:=u_O^*t_T.
\]
For any \(f:O\to O'\), coherence gives
\[
f^*t_{O'}
=
f^*u_{O'}^*t_T
=
(u_{O'}\circ f)^*t_T
=
u_O^*t_T
=
t_O.
\]
Thus \(t_T\) determines a global section.

Conversely, any global section \(t\) restricts to an element \(t_T\in \Omega_{\mathfrak F}(T)\), and the compatibility condition forces
\[
t_O=u_O^*t_T.
\]
Hence the correspondence is bijective. ∎

Thus, if there is a terminal observer, ORM collapses to the mathematics of that terminal frame. Absolute mathematics is the special case in which the observer category has a final object.

---

## 6. Observer-Relative Foundations  

### 6.1 Relative Set Theory  

Classical set theory assumes a single universe \(V\). Observer-relative set theory replaces this with a pseudofunctor
\[
\mathfrak V:\mathbf{Obs}^{\mathrm{op}}\longrightarrow \mathbf{Topos}_{\ell}.
\]
For each observer \(O\), there is a relative universe
\[
\mathfrak V(O)=\mathcal F_O.
\]

A **relative set** is not merely an object in one topos, but a descent datum.

**Definition 6.1.** A relative set \(X\) consists of:

1. for each observer \(O\), an object
   \[
   X_O\in \mathcal F_O;
   \]
2. for each translation \(u:O\to O'\), an isomorphism
   \[
   \alpha_u:X_O\overset{\cong}{\longrightarrow}u^*X_{O'};
   \]
3. coherence of the \(\alpha_u\) under composition.

Thus a relative set is an object of the 2-limit
\[
\mathfrak V\text{-Desc}
\simeq
\varprojlim_{O\in \mathbf{Obs}}\mathcal F_O.
\]

Equality is also relative. For \(x,y:X_O\), the equality proposition is
\[
\mathrm{Eq}_O(x,y)\in \Omega_{\mathfrak F}(O).
\]
Absolute equality requires descent of these equality truth values across all observer translations.

---

### 6.2 Relative Comprehension  

ORM retains comprehension internally to each frame.

**Axiom 7: Relative Comprehension.** For any formula \(\varphi(x)\) in the internal language of \(\mathcal F_O\), and any object \(A_O\in \mathcal F_O\), there exists a subobject
\[
\{x:A_O\mid \varphi(x)\}\hookrightarrow A_O
\]
classified by
\[
\llbracket \varphi\rrbracket_O:A_O\longrightarrow \Omega_{\mathcal F_O}.
\]

Comprehension is observer-local.

---

### 6.3 Relative Choice  

The axiom of choice may vary by observer.

Let \(\mathsf{AC}_O\) denote the internal axiom of choice in \(\mathcal F_O\). In ORM, one may have
\[
\llbracket \mathsf{AC}\rrbracket_O=\top
\]
for some observers and
\[
\llbracket \mathsf{AC}\rrbracket_{O'}=\bot
\]
for others.

A global axiom of choice corresponds to a global section
\[
\mathsf{AC}\in \Gamma(\Omega_{\mathfrak F}).
\]
Such a section exists only if choice is stable under all observer translations.

Thus ORM explains why choice can be independent of certain constructive or sheaf-theoretic universes: it is not absolute but frame-relative.

---

### 6.4 Independence as Frame Variation  

Let \(\varphi\) be a sentence such as the continuum hypothesis.

**Definition 6.2.** The sentence \(\varphi\) is **undecidable in ORM** if there is no global section
\[
\llbracket \varphi\rrbracket\in \Gamma(\Omega_{\mathfrak F})
\]
and no global section
\[
\llbracket \neg\varphi\rrbracket\in \Gamma(\Omega_{\mathfrak F}).
\]

It may still be decided locally:
\[
\llbracket \varphi\rrbracket_{O_1}=\top,
\qquad
\llbracket \varphi\rrbracket_{O_2}=\bot.
\]
This is not contradiction. It is failure of absoluteness.

In classical forcing models, one constructs different Boolean-valued universes in which \(\varphi\) has different truth values. ORM interprets this as variation across observers. The absolute question is not “Is \(\varphi\) true?” but:

\[
\text{Does } \varphi \text{ descend to a global section of } \Omega_{\mathfrak F}?
\]

---

## 7. Tensorial Structure and Coordinate Observers  

ORM generalizes the transformation theory of tensors.

Let \(O\) and \(O'\) be coordinate observers on a manifold, related by a change of frame
\[
\Lambda^\alpha{}_\mu.
\]
A contravariant tensor \(T\) has components
\[
T^{\mu\nu}_{(O)}
\]
in frame \(O\), and components
\[
T^{\alpha\beta}_{(O')}
=
\Lambda^\alpha{}_\mu
\Lambda^\beta{}_\nu
T^{\mu\nu}_{(O)}
\]
in frame \(O'\).

The tensor itself is not the component array. It is the compatible family of component arrays across all coordinate observers.

ORM abstracts this pattern. A mathematical object \(X\) has local representations
\[
X_{(O)}
\]
in each frame \(O\), and transition isomorphisms
\[
X_{(O')}
\cong
\Lambda_{O\to O'}X_{(O)}.
\]
Objectivity is the descent datum.

In this sense, ORM is the categorical theory of mathematical covariance.

---

## 8. Quantum Observers and Relative Truth  

### 8.1 Operational Frames  

Quantum theory requires a refinement of the topos-theoretic frame. A natural structure is an operational frame.

**Definition 8.1.** A **quantum observer frame** is a pair
\[
O=(\mathcal H_O,\mathcal E_O),
\]
where \(\mathcal H_O\) is a Hilbert space and \(\mathcal E_O\) is an effect algebra, typically
\[
\mathcal E_O=
\{E\in \mathcal B(\mathcal H_O):0\le E\le I\}.
\]

A state on \(O\) is a normalized positive linear functional
\[
\omega:\mathcal E_O\longrightarrow [0,1].
\]
In density-matrix form,
\[
\omega(E)=\operatorname{Tr}(\rho_O E).
\]

A proposition “effect \(E\) occurs” has probabilistic truth value
\[
\llbracket E\rrbracket_\omega
=
\omega(E)
=
\operatorname{Tr}(\rho_O E).
\]

Thus quantum truth is not Boolean but effect-valued and state-dependent.

---

### 8.2 Frame Changes as Channels  

A translation of quantum observers
\[
u:O\to O'
\]
is represented in the Heisenberg picture by a unital positive map
\[
u^*:\mathcal E_{O'}\longrightarrow \mathcal E_O.
\]
In finite dimensions, this is often the adjoint of a completely positive trace-preserving map
\[
u_*:\mathcal S(O)\longrightarrow \mathcal S(O'),
\]
where \(\mathcal S(O)\) is the convex set of states.

The Born pairing must be invariant:
\[
\boxed{
\langle u_*\rho,E'\rangle_{O'}
=
\langle \rho,u^*E'\rangle_O.
}
\]

In density-matrix notation,
\[
\operatorname{Tr}_{O'}\!\bigl(u_*(\rho)E'\bigr)
=
\operatorname{Tr}_O\!\bigl(\rho\,u^*(E')\bigr).
\]

This is the quantum analogue of functorial truth stability.

---

### 8.3 Tensor Notation for Quantum Frames  

Let \(\rho_{ab}\) be the components of a density operator and \(E^{ab}\) the components of an effect. The Born probability is the contraction
\[
p(E|\rho)
=
\rho_{ab}E^{ab}.
\]

Under an invertible frame transformation \(\Lambda\), the state and effect transform dually:
\[
\rho'_{\alpha\beta}
=
\Lambda^a{}_\alpha
\Lambda^b{}_\beta
\rho_{ab},
\]
\[
E'^{\alpha\beta}
=
(\Lambda^{-1})^\alpha{}_a
(\Lambda^{-1})^\beta{}_b
E^{ab}.
\]
Then
\[
\rho'_{\alpha\beta}E'^{\alpha\beta}
=
\Lambda^a{}_\alpha
\Lambda^b{}_\beta
\rho_{ab}
(\Lambda^{-1})^\alpha{}_c
(\Lambda^{-1})^\beta{}_d
E^{cd}
=
\delta^a_c\delta^b_d
\rho_{ab}E^{cd}
=
\rho_{ab}E^{ab}.
\]
Thus the probability is observer-invariant.

For non-invertible quantum channels, the same invariance is expressed by channel-state duality:
\[
\operatorname{Tr}(\Lambda(\rho)E)
=
\operatorname{Tr}(\rho\,\Lambda^*(E)).
\]

---

### 8.4 Composite Observers  

Given quantum observers \(O_A\) and \(O_B\), their composite is
\[
O_A\otimes O_B
=
(\mathcal H_A\otimes \mathcal H_B,
\mathcal E_A\overline\otimes \mathcal E_B).
\]

A joint state is
\[
\rho_{AB}\in \mathcal S(O_A\otimes O_B).
\]
The reduced state seen by observer \(O_A\) is
\[
\rho_A
=
\operatorname{Tr}_B(\rho_{AB}).
\]

For a local effect \(E_A\otimes I_B\), the local truth value is
\[
\llbracket E_A\rrbracket_{O_A}
=
\operatorname{Tr}_{AB}
\bigl(\rho_{AB}(E_A\otimes I_B)\bigr)
=
\operatorname{Tr}_A(\rho_A E_A).
\]

---

### 8.5 Locality of Relative Quantum Truth  

**Theorem 8.1.** Let \(U_B\) be a unitary transformation acting only on system \(B\). Define
\[
\rho'_{AB}
=
(I_A\otimes U_B)\rho_{AB}(I_A\otimes U_B^\dagger).
\]
Then the reduced state of \(A\) is unchanged:
\[
\operatorname{Tr}_B(\rho'_{AB})
=
\operatorname{Tr}_B(\rho_{AB}).
\]

*Proof.* For any observable \(A\) on \(\mathcal H_A\),
\[
\operatorname{Tr}_A\!\bigl(A\,\operatorname{Tr}_B\rho'_{AB}\bigr)
=
\operatorname{Tr}_{AB}\!\bigl((A\otimes I_B)\rho'_{AB}\bigr).
\]
Substituting \(\rho'_{AB}\),
\[
\operatorname{Tr}_{AB}\!\bigl((A\otimes I_B)(I\otimes U)\rho(I\otimes U^\dagger)\bigr)
=
\operatorname{Tr}_{AB}\!\bigl((A\otimes U^\dagger U)\rho\bigr)
=
\operatorname{Tr}_{AB}\!\bigl((A\otimes I)\rho\bigr).
\]
Since this holds for all \(A\), the reduced states are equal. ∎

This theorem expresses an observer-relative locality principle: a remote unitary change of frame does not alter local truth values accessible to \(O_A\).

---

### 8.6 Compatibility of Quantum Observers  

Let \(O_X\) and \(O_Z\) be quantum observers associated with projective measurements
\[
\{P_i^X\}_{i},
\qquad
\{P_j^Z\}_{j}.
\]

**Definition 8.2.** The observers \(O_X\) and \(O_Z\) are **compatible** if there exists a common refinement observer \(R\) and translations
\[
R\longrightarrow O_X,
\qquad
R\longrightarrow O_Z
\]
such that the truth values of \(X\)- and \(Z\)-propositions pull back to a joint probability distribution.

Equivalently, there exists a joint POVM
\[
\{R_{ij}\}_{i,j}
\]
with marginals
\[
\sum_j R_{ij}=P_i^X,
\qquad
\sum_i R_{ij}=P_j^Z.
\]

---

### 8.7 Commutation as Compatibility  

**Theorem 8.2.** For finite-dimensional projective observers \(O_X\) and \(O_Z\), compatibility holds if and only if
\[
[P_i^X,P_j^Z]=0
\]
for all \(i,j\).

*Proof.* Suppose a joint POVM \(\{R_{ij}\}\) exists. Since
\[
P_i^X=\sum_j R_{ij}
\]
and all \(R_{ij}\ge 0\), we have
\[
0\le R_{ij}\le P_i^X.
\]
Because \(P_i^X\) is a projection, this implies
\[
R_{ij}=P_i^X R_{ij}P_i^X.
\]
Similarly,
\[
R_{ij}=P_j^Z R_{ij}P_j^Z.
\]
For \(k\neq j\), since \(P_j^ZP_k^Z=0\),
\[
P_j^Z R_{ik}=0.
\]
Therefore
\[
P_j^Z P_i^X
=
P_j^Z\sum_k R_{ik}
=
P_j^Z R_{ij}.
\]
Similarly,
\[
P_i^X P_j^Z
=
R_{ij}P_j^Z
=
P_j^Z R_{ij}.
\]
Hence
\[
P_i^X P_j^Z=P_j^Z P_i^X.
\]

Conversely, if all projections commute, define
\[
R_{ij}=P_i^X P_j^Z.
\]
Then \(R_{ij}\ge 0\), and
\[
\sum_j R_{ij}
=
P_i^X\sum_j P_j^Z
=
P_i^X,
\]
\[
\sum_i R_{ij}
=
\sum_i P_i^X P_j^Z
=
P_j^Z.
\]
Thus \(\{R_{ij}\}\) is a joint POVM. ∎

Incompatible quantum observers therefore correspond to noncommuting frames. Their propositions cannot be glued into a single Boolean truth assignment.

---

### 8.8 Quantum Contextuality as Failure of Global Truth  

Let \(\mathcal C\) be a category of measurement contexts, with objects finite sets of compatible observables. An empirical model assigns to each context \(C\) a probability distribution
\[
e_C\in \operatorname{Prob}(\operatorname{Out}(C)).
\]
A noncontextual hidden-variable model is precisely a global section of the sheaf of probability distributions over \(\mathcal C\).

Thus Bell-Kochen-Specker contextuality says:

\[
\boxed{
\text{There is no global Boolean truth section compatible with the local quantum truths.}
}
\]

ORM interprets contextuality as the natural state of affairs in a non-Boolean observer category. Truth exists locally, but not absolutely.

---

## 9. Observer-Relative Computer Science  

### 9.1 Computational Observers  

In computation, an observer is an environment, tester, or runtime context with limited observational power.

**Definition 9.1.** A **computational observer frame** is a tuple
\[
\mathcal F_O=(\mathbf{Type}_O,\mathbf{Term}_O,\mathbf{Obs}_O),
\]
where:

1. \(\mathbf{Type}_O\) is a category of types;
2. \(\mathbf{Term}_O\) is a category of terms or programs;
3. \(\mathbf{Obs}_O\) is a set or category of observable tests.

A translation of computational observers
\[
u:O\to O'
\]
induces a reindexing functor
\[
u^*:\mathbf{Term}_{O'}\longrightarrow \mathbf{Term}_O
\]
and a map on observations.

---

### 9.2 Observational Equivalence  

For programs \(P,Q:A\) in frame \(O\), define observational equivalence by
\[
P\approx_O Q
\]
if for every test \(T\) available to \(O\),
\[
T(P)\equiv T(Q).
\]

This is observer-relative by definition.

**Theorem 9.1.** Let \(u:O\to O'\). If \(P\approx_{O'}Q\), then
\[
u^*P\approx_O u^*Q.
\]

*Proof.* Any test available to \(O\) after reindexing corresponds to a test pulled back from \(O'\). Since \(P\) and \(Q\) are indistinguishable by all \(O'\)-tests, their pullbacks are indistinguishable by all pulled-back \(O\)-tests. ∎

Observational equivalence is stable under observer translation.

---

### 9.3 Observer-Indexed Type Theory  

ORM suggests an observer-indexed dependent type theory.

A typing judgement has the form
\[
O;\Gamma\vdash t:A.
\]
A proposition is a type
\[
O;\Gamma\vdash \varphi:\mathbf{Prop}.
\]

Reindexing along \(u:O\to O'\) gives
\[
\frac{
O';\Gamma\vdash t:A
}{
O;u^*\Gamma\vdash u^*t:u^*A
}.
\]

Equality is also indexed:
\[
O;\Gamma\vdash \mathrm{Id}_A(s,t):\mathbf{Prop}.
\]
Its truth value lies in
\[
\Omega_{\mathfrak F}(O).
\]

Thus type theory becomes a local logic over observer space.

---

### 9.4 Fully Abstract Semantics as a Sheaf  

Let \(\mathbf{Syn}\) be the presheaf of raw syntax:
\[
O\longmapsto \mathbf{Term}_O.
\]
Let \(\approx\) be observational equivalence. Define the observational quotient presheaf
\[
\mathbf{Beh}^0(O)
=
\mathbf{Term}_O/\approx_O.
\]
In general, \(\mathbf{Beh}^0\) may fail to satisfy locality. We therefore sheafify:
\[
\mathbf{Beh}
=
\mathbf{a}(\mathbf{Beh}^0),
\]
where \(\mathbf{a}\) is sheafification with respect to the observer topology.

A denotational semantics is a natural transformation
\[
\llbracket -\rrbracket:
\mathbf{Syn}
\longrightarrow
\mathbf{Beh}.
\]

**Definition 9.2.** The semantics is **fully abstract** if for all \(P,Q\),
\[
\llbracket P\rrbracket_O=\llbracket Q\rrbracket_O
\quad\Longleftrightarrow\quad
P\approx_O Q.
\]

**Theorem 9.2.** If observational equivalence satisfies locality, then the sheaf \(\mathbf{Beh}\) is final among observational presheaves, and the induced semantics is fully abstract.

*Proof sketch.* Locality ensures that observational equivalence is compatible with covers. Sheafification imposes exactly the minimal gluing conditions required for local observational equivalence to determine global behaviour. Finality follows from the universal property of sheafification: any observational presheaf receiving a compatible interpretation of syntax factors uniquely through \(\mathbf{Beh}\). Equality in \(\mathbf{Beh}\) is therefore precisely observational indistinguishability. ∎

Thus full abstraction is a descent principle.

---

### 9.5 Parametricity as Naturality Across Observers  

A polymorphic program
\[
t:\forall O.\,F(O)
\]
is interpreted as a family
\[
t_O\in F(O)
\]
natural in \(O\). For every observer translation \(u:O\to O'\), parametricity requires
\[
F(u)(t_{O'})=t_O.
\]

This is exactly the ORM condition that a construction be independent of observer choice. Free theorems are naturality theorems over observer space.

---

## 10. Examples  

### 10.1 Coordinate Frames  

Let \(M\) be a smooth manifold. Observers are coordinate charts
\[
\phi:U\to \mathbb R^n.
\]
Frames are local trivializations of tensor bundles. A vector field \(X\) has components
\[
X^\mu_{(\phi)}.
\]
On overlaps \(U\cap V\), components satisfy
\[
X^\alpha_{(\psi)}
=
\frac{\partial y^\alpha}{\partial x^\mu}
X^\mu_{(\phi)}.
\]
The vector field is the global section obtained by descent from compatible local components.

ORM generalizes this from tensors to truth values.

---

### 10.2 Kripke Observers  

Let \(\mathbf{Obs}\) be a poset of possible worlds or stages of knowledge. Let
\[
\mathfrak F(O)=\mathbf{Set}^{\downarrow O}
\]
or another presheaf topos. Truth values are upward-closed subsets of futures. A proposition may become true at a later stage without being true earlier.

Here ORM recovers Kripke semantics as observer-relative truth.

---

### 10.3 Boolean and Intuitionistic Observers  

Let \(O_B\) be a classical observer with Boolean topos
\[
\mathcal F_{O_B}=\mathbf{Set}.
\]
Let \(O_I\) be a constructive observer with topos
\[
\mathcal F_{O_I}=\mathbf{Sh}(X)
\]
for a topological space \(X\). Then
\[
\llbracket \varphi\vee\neg\varphi\rrbracket_{O_B}=\top
\]
may hold, while
\[
\llbracket \varphi\vee\neg\varphi\rrbracket_{O_I}\neq \top.
\]
The law of excluded middle is not absolute; it is a property of the observer frame.

---

### 10.4 Quantum Measurement Observers  

Let \(O_X\) measure spin in the \(x\)-direction and \(O_Z\) measure spin in the \(z\)-direction. The corresponding projectors do not commute:
\[
[P^X_+,P^Z_+]\neq 0.
\]
There is no common Boolean refinement. ORM represents the propositions
\[
S_x=+1,
\qquad
S_z=+1
\]
as living in incompatible frames. Their simultaneous absolute truth is undefined, not merely unknown.

---

## 11. Philosophical and Mathematical Consequences  

ORM reorganizes several foundational distinctions.

### 11.1 Objectivity Is Not Absoluteness  

Classically, objectivity means independence from perspective. In ORM, objectivity means invariance under change of perspective. This is a gauge-theoretic notion.

### 11.2 Contradiction Is Descent Failure  

Local truths may differ without contradiction. Contradiction arises when a putative global section is forced by descent but cannot exist.

### 11.3 Independence Is Geometric  

Independence phenomena in set theory become statements about the geometry of observer space. A sentence is independent if its truth bundle has no global section deciding it.

### 11.4 Quantum Complementarity Is Categorical  

Complementarity is not a failure of knowledge but a failure of compatibility among observer frames.

### 11.5 Computational Abstraction Is Observer Quotienting  

Abstraction is the process of quotienting programs by the observations available to a chosen class of observers. Full abstraction is sheaf-theoretic descent.

---

## 12. Research Program  

The present framework suggests several directions.

1. **ORM Topos Theory.** Develop the 2-categorical theory of stacks of topoi over observer categories.

2. **ORM Type Theory.** Construct a full dependent type theory with explicit observer indices, observer elimination rules, and descent types.

3. **ORM Quantum Foundations.** Extend the effect-state formulation to infinite-dimensional von Neumann algebras and relativistic quantum field theory.

4. **ORM Homotopy Theory.** Replace topoi by \(\infty\)-topoi and truth values by spaces of proofs. Absolute truth becomes a homotopy-coherent global section.

5. **ORM Complexity Theory.** Study observer translations as resource-bounded reductions. Observational power becomes a complexity parameter.

6. **ORM Logic.** Develop proof theory for observer-indexed judgements
   \[
   O;\Gamma\vdash \varphi
   \]
   with explicit transport rules along observer morphisms.

7. **ORM and Gauge Theory.** Formalize mathematical gauge transformations as automorphisms of observer frames, with absolute objects as gauge-invariant sections.

---

## 13. Conclusion  

Observer-Relative Mathematics provides a rigorous categorical account of frame-dependent truth. The primitive object is the framed observer
\[
(O,\mathcal F),
\]
and mathematical truth is not a global scalar but a section of a truth bundle
\[
\Omega_{\mathfrak F}\to \mathbf{Obs}.
\]
Local truths are meaningful. Global truths are those local truths that satisfy descent.

The framework recovers classical mathematics as the special case of a terminal observer. It explains logical variation across topoi, independence phenomena in set theory, quantum incompatibility, and observational equivalence in computation as instances of a single principle:

\[
\boxed{
\text{Truth is local; objectivity is descent.}
}
\]

---

## References  

1. M. Artin, A. Grothendieck, J.-L. Verdier, *Théorie des topos et cohomologie étale des schémas*, Springer, 1972.

2. S. Awodey, *Category Theory*, Oxford University Press, 2010.

3. J. Baez, J. Dolan, “Higher-dimensional algebra and topological quantum field theory,” *Journal of Mathematical Physics*, 1995.

4. A. Abramsky, A. Brandenburger, “The sheaf-theoretic structure of non-locality and contextuality,” *New Journal of Physics*, 2011.

5. B. Coecke, A. Kissinger, *Picturing Quantum Processes*, Cambridge University Press, 2017.

6. P. T. Johnstone, *Sketches of an Elephant: A Topos Theory Compendium*, Oxford University Press, 2002.

7. F. W. Lawvere, “Adjointness in foundations,” *Dialectica*, 1969.

8. S. Mac Lane, I. Moerdijk, *Sheaves in Geometry and Logic*, Springer, 1992.

9. E. Moggi, “Notions of computation and monads,” *Information and Computation*, 1991.

10. A. M. Pitts, “Categorical logic,” in *Handbook of Logic in Computer Science*, Oxford University Press, 2000.

11. G. D. Plotkin, “LCF considered as a programming language,” *Theoretical Computer Science*, 1977.

12. P. Selinger, “Dagger compact closed categories and completely positive maps,” *Electronic Notes in Theoretical Computer Science*, 2007.

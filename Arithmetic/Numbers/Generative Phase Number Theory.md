# Generative Phase Number Theory  
## A Unified Calculus of Generative Arithmetic Structures and Unit-Complex Phase Invariants  

**Preprint — 2026**  

**Keywords:** generative number theory, phase number, unit circle, \(U(1)\), arithmetic phase, holonomy, winding number, gauge structure, fiber bundle, character theory, generative zeta function  

**MSC 2020:** 11A99, 11N99, 20C99, 22E67, 53C05, 55N99, 58J90, 81Q70  

---

## Abstract

This paper introduces **Generative Phase Number Theory** (GPNT), a unified mathematical framework combining two previously separated ideas:

1. **Generative Number Theory** (GNT), in which a number is not merely a value \(n\), but a structured object
   \[
   \mathfrak n=(n,\Gamma_n),
   \]
   where \(\Gamma_n\) encodes admissible generative histories, transformations, descendants, ancestors, and structural degrees of freedom;

2. **Phase-number calculus**, in which the primary phase object is the unit-complex scalar
   \[
   u\in \mathbb T \equiv U(1)=\{z\in\mathbb C:|z|=1\},
   \]
   rather than a real-valued angle \(\theta\), which exists only locally or modulo \(2\pi\).

GPNT assigns to generative arithmetic a \(U(1)\)-valued phase layer. The central object is the **generative phase number**
\[
\mathfrak u_{\mathfrak n}\in U(1),
\]
attached to a generative state \(\mathfrak n\), or more generally to a generative pathway, transformation, or cycle. The theory distinguishes sharply between:

- the **value** \(n=\pi(\mathfrak n)\),
- the **generative state** \(\mathfrak n=(n,\Gamma_n)\),
- the **phase number** \(u\in U(1)\),
- the **phase angle** \(\theta\), which is only a local coordinate satisfying \(u=e^{i\theta}\).

The central thesis is:

\[
\boxed{
\text{A generative number possesses not only value and structure, but also phase.}
}
\]

Equivalently,

\[
\boxed{
\text{Number}=\text{Value}+\text{Generative Structure}+\text{Phase Structure}.
}
\]

The paper develops the algebra, topology, differential geometry, harmonic analysis, dynamics, and analytic number-theoretic consequences of this extension. Generative phase numbers are shown to resolve path-dependence, encode structural holonomy, define arithmetic interference laws, produce phase-weighted zeta functions, and supply a natural language for quantum and computational phase phenomena.

---

## 1. Scope, Motivation, and Analytical Position

Classical arithmetic treats a number primarily as a value. The integer \(6\) is identified with its numerical magnitude, irrespective of whether it is obtained as
\[
6=2+4,\qquad 6=3+3,\qquad 6=2\cdot 3,
\]
or through some recursive history. Generative Number Theory retains these histories by replacing the bare integer \(n\) with a generative object
\[
\mathfrak n=(n,\Gamma_n).
\]
The ordinary integer is recovered by projection:
\[
\pi(\mathfrak n)=n.
\]

However, generative structure alone does not capture phase phenomena. In many mathematical and physical contexts, the relevant object is not merely a pathway or structure, but a **phase factor** accumulated along that pathway. Examples include:

- Fourier characters \(e^{in\theta}\),
- interference of complex amplitudes,
- winding numbers,
- gauge transformations,
- Berry phases,
- quantum phase gates,
- circular statistics,
- holonomy of connections.

GPNT therefore adds a phase-valued layer to generative arithmetic. The phase object is not an auxiliary angle. It is a globally defined element of the circle group \(U(1)\). Angles are local logarithms of phase numbers and are subject to branch ambiguity.

Thus GPNT proposes the hierarchy

\[
\boxed{
n
\quad\longleftarrow\quad
\mathfrak n=(n,\Gamma_n)
\quad\longleftarrow\quad
(\mathfrak n,u),\quad u\in U(1).
}
\]

The first arrow forgets generative structure. The second forgets phase.

The resulting framework is conservative: ordinary arithmetic is recovered by projection. But it is also richer: two generative states may have the same value and even isomorphic generative structure while differing by phase, holonomy, or phase curvature.

---

## 2. Phase-Number Preliminaries

We recall the essential facts about phase numbers.

Define the circle group
\[
\mathbb T=U(1)=\{u\in\mathbb C:u\bar u=1\}.
\]
The exponential map
\[
\operatorname{Exp}:\mathbb R\to U(1),\qquad
\theta\mapsto e^{i\theta}
\]
is a smooth surjective homomorphism with kernel \(2\pi\mathbb Z\). Hence
\[
U(1)\cong \mathbb R/(2\pi\mathbb Z).
\]

A **phase number** is an element \(u\in U(1)\). A **phase angle** is a class \([\theta]\in\mathbb R/(2\pi\mathbb Z)\). A **phase lift** is a local or chosen representative \(\theta\in\mathbb R\) such that
\[
u=e^{i\theta}.
\]

The crucial point is that \(u\) is globally defined, while a continuous global angle generally is not.

For \(z\in\mathbb C^\times\), the polar factorization is
\[
z=r u,
\qquad
r=|z|>0,
\qquad
u=\operatorname{ph}(z)=\frac{z}{|z|}\in U(1).
\]
Thus
\[
\mathbb C^\times\cong \mathbb R_{>0}\times U(1).
\]

For phase numbers \(u=e^{i\alpha}\), \(v=e^{i\beta}\),
\[
uv=e^{i(\alpha+\beta)},
\qquad
u^{-1}=\bar u=e^{-i\alpha},
\qquad
u^n=e^{in\alpha},\quad n\in\mathbb Z.
\]

The principal argument \(\operatorname{Arg}(u)\) is a branch-dependent coordinate. No continuous global argument exists on \(U(1)\).

---

## 3. Generative Number Preliminaries

In Generative Number Theory, the primitive object is the generative number
\[
\mathfrak n=(n,\Gamma_n),
\]
where

- \(n\in\mathbb N_0\) is the numerical value,
- \(\Gamma_n\) is a generative structure: graph, tree, network, recursive history, or transformation system associated with \(n\).

The evaluation map is
\[
\operatorname{val}(\mathfrak n)=n.
\]
Equivalently, we write
\[
\pi:\mathbb{GN}\to\mathbb N_0,
\qquad
\pi(\mathfrak n)=n.
\]

The fiber over \(n\) is
\[
\mathcal F_n=\pi^{-1}(n),
\]
the set of all generative states whose numerical value is \(n\).

Generative addition and multiplication, when defined, satisfy projection compatibility:
\[
\pi(\mathfrak a\oplus_G\mathfrak b)
=
\pi(\mathfrak a)+\pi(\mathfrak b),
\]
\[
\pi(\mathfrak a\otimes_G\mathfrak b)
=
\pi(\mathfrak a)\pi(\mathfrak b).
\]

Thus classical arithmetic is the shadow algebra obtained by forgetting generative structure.

---

## 4. Generative Phase Objects

### 4.1 Basic definition

A **generative phase number** is a pair
\[
\mathfrak z=(\mathfrak n,u),
\]
where

- \(\mathfrak n\in\mathbb{GN}\) is a generative number,
- \(u\in U(1)\) is a phase number.

The collection of such objects is the phase-extended generative space
\[
\widehat{\mathbb{GN}}
=
\mathbb{GN}\times U(1).
\]

There are three natural projections:
\[
\operatorname{val}:\widehat{\mathbb{GN}}\to\mathbb N_0,
\qquad
\operatorname{val}(\mathfrak z)=\pi(\mathfrak n),
\]
\[
\operatorname{gen}:\widehat{\mathbb{GN}}\to\mathbb{GN},
\qquad
\operatorname{gen}(\mathfrak z)=\mathfrak n,
\]
\[
\operatorname{ph}:\widehat{\mathbb{GN}}\to U(1),
\qquad
\operatorname{ph}(\mathfrak z)=u.
\]

A **generative phase angle** is a local lift \(\theta\) such that
\[
u=e^{i\theta}.
\]
It is not itself the primary object.

### 4.2 Phase fields on generative states

A phase assignment on a generative space is a map
\[
\Phi:\mathbb{GN}\to U(1),
\]
or, more generally, a section of a \(U(1)\)-bundle over \(\mathbb{GN}\).

For each generative state \(\mathfrak n\),
\[
\Phi(\mathfrak n)\in U(1)
\]
is its phase number.

If a local angle exists, one may write
\[
\Phi(\mathfrak n)=e^{i\theta_{\mathfrak n}},
\]
but \(\theta_{\mathfrak n}\) may fail to exist globally or may be multivalued modulo \(2\pi\).

### 4.3 Phase assignments on generative graphs

Let the generative structure be represented by a directed graph
\[
\Gamma=(V,E),
\]
where vertices are generative states and edges are admissible transformations.

A **transition phase number** is a function
\[
g:E\to U(1).
\]
For an edge
\[
e:\mathfrak a\to\mathfrak b,
\]
we write
\[
g_e\in U(1).
\]

For a directed path
\[
\gamma=e_1e_2\cdots e_k,
\]
the path phase number is
\[
\Phi(\gamma)
=
\prod_{j=1}^k g_{e_j}.
\]

This definition is branch-free and multiplicative.

### 4.4 Gauge rephasing

A local rephasing of vertices is a map
\[
\chi:V\to U(1).
\]
It transforms edge phases by
\[
g_e
\longmapsto
g_e'
=
\chi(\mathfrak b)\,g_e\,\chi(\mathfrak a)^{-1},
\qquad
e:\mathfrak a\to\mathfrak b.
\]

Since \(U(1)\) is abelian, this may also be written as
\[
g_e'
=
g_e\,\chi(\mathfrak b)\chi(\mathfrak a)^{-1}.
\]

The phase of a closed loop is invariant under such rephasing.

---

## 5. Axioms of Generative Phase Number Theory

We propose the following axioms.

### Axiom I — Numerical projection

Every generative phase object has a numerical value:
\[
\operatorname{val}(\mathfrak z)\in\mathbb N_0.
\]

### Axiom II — Generative multiplicity

A numerical value may correspond to multiple generative states:
\[
|\pi^{-1}(n)|\ge 1.
\]

### Axiom III — Phase existence

Every generative state admits a phase number
\[
\Phi(\mathfrak n)\in U(1).
\]

A phase angle is a coordinate choice and not a primitive object.

### Axiom IV — Multiplicative transport

Along composable generative transformations, phase numbers compose multiplicatively:
\[
\Phi(\gamma_2\circ\gamma_1)
=
\Phi(\gamma_2)\Phi(\gamma_1).
\]

### Axiom V — Gauge covariance

Local rephasing changes phase representatives but not relative phase numbers or closed-loop holonomies.

### Axiom VI — Projection compatibility

Phase structure does not alter numerical projection:
\[
\pi(\mathfrak n)=\operatorname{val}(\mathfrak n).
\]

### Axiom VII — Phase memory

The phase of a composite generative result may depend on the phases of its constituents and on the generative pathway by which it was obtained.

Thus GPNT is path-dependent at the phase level even when the numerical projection is path-independent.

---

## 6. Algebra of Generative Phase Numbers

### 6.1 Phase-extended operations

Assume \((\mathbb{GN},\oplus_G,\otimes_G)\) is a generative arithmetic system. We construct a \(U(1)\)-extension by introducing phase cocycles.

For generative states \(\mathfrak a,\mathfrak b\) and phase numbers \(u,v\in U(1)\), define
\[
(\mathfrak a,u)\oplus_P(\mathfrak b,v)
=
\left(
\mathfrak a\oplus_G\mathfrak b,
\,uv\,C_+(\mathfrak a,\mathfrak b)
\right),
\]
and
\[
(\mathfrak a,u)\otimes_P(\mathfrak b,v)
=
\left(
\mathfrak a\otimes_G\mathfrak b,
\,uv\,C_\times(\mathfrak a,\mathfrak b)
\right),
\]
where
\[
C_+:\mathbb{GN}\times\mathbb{GN}\to U(1),
\qquad
C_\times:\mathbb{GN}\times\mathbb{GN}\to U(1)
\]
are phase 2-cocycles.

The numerical projections satisfy
\[
\operatorname{val}\bigl((\mathfrak a,u)\oplus_P(\mathfrak b,v)\bigr)
=
\operatorname{val}(\mathfrak a)+\operatorname{val}(\mathfrak b),
\]
\[
\operatorname{val}\bigl((\mathfrak a,u)\otimes_P(\mathfrak b,v)\bigr)
=
\operatorname{val}(\mathfrak a)\operatorname{val}(\mathfrak b).
\]

Thus ordinary arithmetic is preserved at the level of values.

### 6.2 Associativity and cocycle conditions

For additive associativity, require
\[
\bigl((\mathfrak a,u)\oplus_P(\mathfrak b,v)\bigr)\oplus_P(\mathfrak c,w)
=
(\mathfrak a,u)\oplus_P\bigl((\mathfrak b,v)\oplus_P(\mathfrak c,w)\bigr).
\]

The phase on the left is
\[
uvw\,C_+(\mathfrak a,\mathfrak b)\,
C_+(\mathfrak a\oplus_G\mathfrak b,\mathfrak c).
\]

The phase on the right is
\[
uvw\,C_+(\mathfrak b,\mathfrak c)\,
C_+(\mathfrak a,\mathfrak b\oplus_G\mathfrak c).
\]

Therefore associativity holds if and only if
\[
\boxed{
C_+(\mathfrak a,\mathfrak b)
C_+(\mathfrak a\oplus_G\mathfrak b,\mathfrak c)
=
C_+(\mathfrak b,\mathfrak c)
C_+(\mathfrak a,\mathfrak b\oplus_G\mathfrak c).
}
\]

This is the additive phase cocycle condition.

Similarly, multiplicative associativity requires
\[
\boxed{
C_\times(\mathfrak a,\mathfrak b)
C_\times(\mathfrak a\otimes_G\mathfrak b,\mathfrak c)
=
C_\times(\mathfrak b,\mathfrak c)
C_\times(\mathfrak a,\mathfrak b\otimes_G\mathfrak c).
}
\]

### 6.3 Gauge transformations of cocycles

Let
\[
\chi:\mathbb{GN}\to U(1)
\]
be a rephasing. Define new phase representatives by
\[
u'=\chi(\mathfrak a)u.
\]

Then the additive cocycle transforms as
\[
C_+'(\mathfrak a,\mathfrak b)
=
\chi(\mathfrak a\oplus_G\mathfrak b)
C_+(\mathfrak a,\mathfrak b)
\chi(\mathfrak a)^{-1}\chi(\mathfrak b)^{-1}.
\]

Thus a change of phase trivialization changes the cocycle by a coboundary. The cohomology class of \(C_+\) is invariant.

The same holds for \(C_\times\).

### 6.4 Distributivity constraint

If the phase-extended arithmetic is required to be distributive, then the additive and multiplicative cocycles must satisfy a compatibility condition. Schematically,
\[
(\mathfrak a\oplus_G\mathfrak b)\otimes_G\mathfrak c
\]
and
\[
(\mathfrak a\otimes_G\mathfrak c)\oplus_G(\mathfrak b\otimes_G\mathfrak c)
\]
must acquire compatible phase factors.

The precise condition is
\[
C_\times(\mathfrak a\oplus_G\mathfrak b,\mathfrak c)
C_+(\mathfrak a\otimes_G\mathfrak c,\mathfrak b\otimes_G\mathfrak c)
=
C_+(\mathfrak a,\mathfrak b)
C_\times(\mathfrak a,\mathfrak c)
C_\times(\mathfrak b,\mathfrak c),
\]
up to the appropriate structural identifications. This is the phase-distributive coherence law.

---

## 7. Relative Phase and Arithmetic Interference

Phase numbers become observable through relative phase.

Given two generative phase states
\[
(\mathfrak a,u),\qquad(\mathfrak b,v),
\]
their relative phase number is
\[
u\bar v\in U(1).
\]

If \(u=e^{i\alpha}\) and \(v=e^{i\beta}\), then
\[
u\bar v=e^{i(\alpha-\beta)}.
\]

Let \(a,b\ge 0\). Consider the complex amplitude
\[
A=a u+b v.
\]
Then
\[
\begin{aligned}
|A|^2
&=(a u+b v)(a\bar u+b\bar v)\\
&=a^2+b^2+ab(u\bar v+\bar u v)\\
&=a^2+b^2+2ab\operatorname{Re}(u\bar v)\\
&=a^2+b^2+2ab\cos(\alpha-\beta).
\end{aligned}
\]

Thus interference depends only on the relative phase number. A common phase factor cancels:
\[
|a w u+b w v|^2
=
|a u+b v|^2,
\qquad w\in U(1).
\]

This is the algebraic foundation of generative phase interference.

---

## 8. Topology of Generative Phase

### 8.1 Closed generative loops

Let
\[
C:\mathfrak n_0\to\mathfrak n_1\to\cdots\to\mathfrak n_k=\mathfrak n_0
\]
be a closed generative path. Its holonomy phase number is
\[
\operatorname{Hol}(C)
=
\prod_{e\in C}g_e
\in U(1).
\]

Under vertex rephasing,
\[
g_e\mapsto \chi(\mathfrak b)g_e\chi(\mathfrak a)^{-1},
\]
the product around a closed loop is unchanged. Hence
\[
\operatorname{Hol}(C)
\]
is gauge invariant.

### 8.2 Global phase lifting criterion

A phase assignment is gauge-equivalent to a trivial phase assignment if and only if all closed-loop holonomies vanish.

**Theorem 1.**  
Let \(\Gamma\) be a connected generative graph with edge phases \(g_e\in U(1)\). There exists a vertex phase function
\[
\chi:V\to U(1)
\]
such that
\[
g_e=\chi(\mathfrak b)\chi(\mathfrak a)^{-1}
\]
for every edge \(e:\mathfrak a\to\mathfrak b\) if and only if
\[
\operatorname{Hol}(C)=1
\]
for every closed loop \(C\) in \(\Gamma\).

**Proof.**  
Choose a spanning tree \(T\) of \(\Gamma\). Fix a root vertex \(\mathfrak n_0\) and set \(\chi(\mathfrak n_0)=1\). Define \(\chi\) on all vertices by multiplying edge phases along the unique tree path from \(\mathfrak n_0\) to each vertex.

By construction,
\[
g_e=\chi(\mathfrak b)\chi(\mathfrak a)^{-1}
\]
for every tree edge.

For a non-tree edge \(e:\mathfrak a\to\mathfrak b\), adding \(e\) to the tree creates a loop \(C_e\). The holonomy of that loop is
\[
\operatorname{Hol}(C_e)
=
\chi(\mathfrak a)g_e\chi(\mathfrak b)^{-1}.
\]
If all holonomies are \(1\), then
\[
g_e=\chi(\mathfrak b)\chi(\mathfrak a)^{-1}.
\]
Conversely, if such a \(\chi\) exists globally, every closed-loop product telescopes to \(1\). \(\square\)

Thus nontrivial holonomy is the obstruction to a global phase trivialization.

### 8.3 Discrete curvature

Suppose the generative graph is augmented by 2-cells \(\sigma\). Define the discrete curvature of \(\sigma\) by
\[
F_\sigma
=
\prod_{e\in\partial\sigma}g_e
\in U(1).
\]

A phase structure is flat if
\[
F_\sigma=1
\]
for every 2-cell \(\sigma\).

This is the discrete analogue of gauge curvature.

### 8.4 Winding numbers

If a generative loop carries a phase-number field
\[
u:C\to U(1),
\]
its winding number is
\[
\operatorname{wind}(u)
=
\frac{1}{2\pi i}\oint_C u^{-1}du.
\]

Locally, if \(u=e^{i\theta}\), then
\[
u^{-1}du=i\,d\theta,
\]
so
\[
\operatorname{wind}(u)
=
\frac{1}{2\pi}
\oint_C d\theta
=
\frac{\Delta\widetilde\theta}{2\pi}
\in\mathbb Z,
\]
where \(\widetilde\theta\) is a lifted real phase coordinate along the loop.

Thus winding is an integer topological invariant, whereas holonomy is a general \(U(1)\)-valued invariant.

---

## 9. Differential Geometry of Generative Phase

When generative parameters vary smoothly, one may model generative space by a manifold
\[
\mathcal M_G.
\]

A generative phase structure is then naturally described by a complex line bundle
\[
L\to\mathcal M_G
\]
with structure group \(U(1)\).

### 9.1 Local frames and transition phase numbers

Choose local unit frames \(s_a\) over open sets \(U_a\). On overlaps,
\[
s_b=g_{ab}s_a,
\qquad
g_{ab}:U_a\cap U_b\to U(1).
\]

The functions \(g_{ab}\) are transition phase numbers. On triple overlaps,
\[
g_{ab}g_{bc}g_{ca}=1.
\]

This cocycle condition defines a \(U(1)\)-bundle.

### 9.2 Connection one-form

Let \(\nabla\) be a unitary connection. In a local unit frame,
\[
\nabla s_a=i\mathcal A_a\otimes s_a,
\]
where
\[
\mathcal A_a=A_{a\mu}\,dx^\mu.
\]

Under a local phase transformation
\[
s_a\mapsto s_a'=e^{i\chi_a}s_a,
\]
the connection transforms as
\[
\mathcal A_a'
=
\mathcal A_a+d\chi_a,
\]
or in components,
\[
A_{a\mu}'
=
A_{a\mu}+\partial_\mu\chi_a.
\]

### 9.3 Curvature tensor

The curvature two-form is
\[
\mathcal F
=
d\mathcal A.
\]

In components,
\[
\mathcal F
=
\frac12 F_{\mu\nu}\,dx^\mu\wedge dx^\nu,
\]
with
\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu.
\]

The curvature is antisymmetric:
\[
F_{\mu\nu}=-F_{\nu\mu}.
\]

It satisfies the Bianchi identity
\[
\partial_{[\lambda}F_{\mu\nu]}=0.
\]

In the abelian \(U(1)\) case, \(\mathcal F\) is gauge invariant:
\[
\mathcal F'
=
d\mathcal A'
=
d\mathcal A+d^2\chi
=
\mathcal F.
\]

### 9.4 Holonomy and Stokes’ theorem

For a closed loop \(C\subset\mathcal M_G\), the holonomy phase number is
\[
\operatorname{Hol}_C(\nabla)
=
\exp\left(i\oint_C\mathcal A\right).
\]

If \(C=\partial\Sigma\) and a single gauge chart covers \(\Sigma\), then by Stokes’ theorem,
\[
\operatorname{Hol}_C(\nabla)
=
\exp\left(i\int_\Sigma\mathcal F\right).
\]

Thus curvature integrates to a globally meaningful phase number.

### 9.5 Generative phase curvature

In GPNT, the coordinates \(x^\mu\) may represent generative parameters such as
\[
x^\mu\in\{V,D,W,H_G,K_G,F_G,\ldots\},
\]
where

- \(V\) is value,
- \(D\) is generative depth,
- \(W\) is generative width,
- \(H_G\) is generative entropy,
- \(K_G\) is generative complexity or curvature,
- \(F_G\) is fiber cardinality.

The connection
\[
\mathcal A=A_\mu dx^\mu
\]
then describes how arithmetic phase changes under variation of generative structure.

The curvature
\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu
\]
measures failure of phase integrability over generative parameter space.

---

## 10. Harmonic Analysis on Generative Phase Spaces

### 10.1 Characters of the circle group

For each integer \(m\in\mathbb Z\), define
\[
\chi_m:U(1)\to U(1),
\qquad
\chi_m(u)=u^m.
\]

If \(u=e^{i\theta}\), then
\[
\chi_m(e^{i\theta})=e^{im\theta}.
\]

These are the irreducible characters of \(U(1)\). They obey
\[
\frac{1}{2\pi}\int_0^{2\pi}e^{i(m-n)\theta}\,d\theta
=
\delta_{mn}.
\]

### 10.2 Generative phase characters

Let \(X\) be a finite generative phase space. A **generative phase character** is a homomorphism
\[
\chi:X\to U(1).
\]

For example, if a finite generative phase space carries a value coordinate modulo \(N\) and a phase coordinate in \(\mu_N\), then characters take the form
\[
\chi_{m,k}(n,u)
=
e^{2\pi i mn/N}u^k,
\qquad
m,k\in\mathbb Z/N\mathbb Z.
\]

The associated Fourier transform is
\[
\widehat f(m,k)
=
\sum_{n,u}f(n,u)\overline{\chi_{m,k}(n,u)}.
\]

Inversion follows from character orthogonality.

### 10.3 Finite phase alphabets

The \(N\)th roots of unity form the finite subgroup
\[
\mu_N
=
\{u\in U(1):u^N=1\}
=
\left\{
e^{2\pi i k/N}:k=0,\ldots,N-1
\right\}.
\]

This group is isomorphic to \(\mathbb Z/N\mathbb Z\). It supplies the natural phase alphabet for discrete generative phase systems, discrete Fourier analysis, and quantum phase gates.

---

## 11. Circular Statistics in Generative Fibers

Given a finite collection of phase numbers in a generative fiber,
\[
u_1,\ldots,u_N\in U(1),
\]
define the resultant
\[
\bar u=\frac1N\sum_{k=1}^N u_k.
\]

If \(\bar u\ne 0\), the circular mean phase number is
\[
\widehat u
=
\frac{\bar u}{|\bar u|}.
\]

The resultant length
\[
R=|\bar u|\in[0,1]
\]
measures phase concentration.

The circular variance is
\[
V_{\mathrm{circ}}=1-R.
\]

This construction is branch-independent. It avoids the error of averaging principal angles directly, which can produce artificial results near branch cuts.

For a probability distribution \(\{p_k\}\) on phase numbers \(\{u_k\}\), define
\[
\bar u
=
\sum_k p_k u_k,
\qquad
R=|\bar u|.
\]

The quantity \(R\) is the **generative phase coherence**.

---

## 12. Generative Phase Dynamics

### 12.1 Phaseful transformations

Let
\[
T_G:\mathbb{GN}\to\mathbb{GN}
\]
be a generative transformation. A phaseful lift of \(T_G\) is a map
\[
\widehat T_G:\widehat{\mathbb{GN}}\to\widehat{\mathbb{GN}}
\]
of the form
\[
\widehat T_G(\mathfrak n,u)
=
\left(
T_G\mathfrak n,
\tau_T(\mathfrak n)u
\right),
\]
where
\[
\tau_T:\mathbb{GN}\to U(1)
\]
is the phase multiplier associated with \(T_G\).

For two transformations \(S_G,T_G\), composition gives
\[
\widehat S_G\circ\widehat T_G(\mathfrak n,u)
=
\left(
S_G T_G\mathfrak n,
\tau_S(T_G\mathfrak n)\tau_T(\mathfrak n)u
\right).
\]

Thus phase multipliers obey the cocycle law
\[
\tau_{S\circ T}(\mathfrak n)
=
\tau_S(T_G\mathfrak n)\tau_T(\mathfrak n).
\]

### 12.2 Generative phase orbits

Starting from \((\mathfrak n_0,u_0)\), define
\[
(\mathfrak n_{k+1},u_{k+1})
=
\widehat T_G(\mathfrak n_k,u_k).
\]

Then
\[
u_k
=
u_0\prod_{j=0}^{k-1}\tau_T(\mathfrak n_j).
\]

If the generative orbit is periodic with period \(m\), then the phase multiplier over one period is
\[
\Lambda
=
\prod_{j=0}^{m-1}\tau_T(\mathfrak n_j).
\]

The orbit is phase-periodic if
\[
\Lambda=1.
\]

It is phase-resonant of order \(q\) if
\[
\Lambda^q=1.
\]

### 12.3 Phase conservation laws

A quantity
\[
Q:\widehat{\mathbb{GN}}\to X
\]
is a generative phase invariant under \(\widehat T_G\) if
\[
Q(\widehat T_G(\mathfrak z))=Q(\mathfrak z).
\]

Important invariants include:

- relative phase between comparable states,
- loop holonomy,
- discrete curvature,
- winding number,
- resultant length in a fiber,
- phase coherence.

---

## 13. Analytic Generative Phase Number Theory

### 13.1 Phase-weighted fiber sums

For each integer \(n\), define the phase sum of its generative fiber by
\[
A(n)
=
\sum_{\mathfrak n\in\mathcal F_n}
w(\mathfrak n)\Phi(\mathfrak n),
\]
where \(w(\mathfrak n)\) is a weight and \(\Phi(\mathfrak n)\in U(1)\) is the phase number.

The quantity \(A(n)\) is a complex amplitude. Its modulus squared contains interference terms:
\[
|A(n)|^2
=
\sum_{\mathfrak a,\mathfrak b\in\mathcal F_n}
w(\mathfrak a)w(\mathfrak b)
\Phi(\mathfrak a)\overline{\Phi(\mathfrak b)}.
\]

Thus the distribution of phases inside a generative fiber affects arithmetic observables.

### 13.2 Generative phase zeta function

Define the generative phase zeta function by
\[
\zeta_{GP}(s)
=
\sum_{n=1}^\infty
\frac{A(n)}{n^s}.
\]

Equivalently,
\[
\zeta_{GP}(s)
=
\sum_{n=1}^\infty
\frac{1}{n^s}
\sum_{\mathfrak n\in\mathcal F_n}
w(\mathfrak n)\Phi(\mathfrak n).
\]

If the phase assignment is multiplicative with respect to generative prime decomposition and generative factorization is sufficiently unique, one may obtain an Euler product of the form
\[
\zeta_{GP}(s)
=
\prod_{\mathfrak p\in\mathcal P_G}
\left(
1-
\Phi(\mathfrak p)N_G(\mathfrak p)^{-s}
\right)^{-1},
\]
where \(\mathcal P_G\) denotes generative primes and \(N_G(\mathfrak p)\) is a norm.

In general, nonunique factorization replaces the Euler product by a more intricate phase-weighted sum over generative factorization networks.

### 13.3 Generative phase \(L\)-functions

Let
\[
\chi_G:\mathbb{GN}\to U(1)
\]
be a generative character. Define
\[
L_{GP}(s,\chi_G)
=
\sum_{n=1}^\infty
\frac{1}{n^s}
\sum_{\mathfrak n\in\mathcal F_n}
w(\mathfrak n)
\chi_G(\mathfrak n)
\Phi(\mathfrak n).
\]

This combines generative characters and phase weights.

### 13.4 Phase Möbius inversion

If the generative divisibility relation \(\mid_G\) defines a locally finite poset, let
\[
\mu_G(\mathfrak a,\mathfrak b)
\]
be its Möbius function. For phase-weighted arithmetic functions
\[
F(\mathfrak n)=\sum_{\mathfrak d\mid_G\mathfrak n}f(\mathfrak d),
\]
one has a generative Möbius inversion
\[
f(\mathfrak n)
=
\sum_{\mathfrak d\mid_G\mathfrak n}
\mu_G(\mathfrak d,\mathfrak n)
F(\mathfrak d).
\]

If \(f\) carries phase values, this becomes phase-weighted inversion.

---

## 14. Generative Phase Entropy and Geometry

### 14.1 Phase entropy in a fiber

Let \(\mathcal F_n\) carry a probability distribution \(p(\mathfrak n)\). The phase distribution is the pushforward
\[
p_\Phi(u)
=
\sum_{\mathfrak n:\Phi(\mathfrak n)=u}p(\mathfrak n).
\]

A phase entropy may be defined by binning \(U(1)\) or, for continuous distributions, by
\[
H_\Phi
=
-\int_0^{2\pi}
p(\theta)\log p(\theta)\,d\theta.
\]

This measures phase diversity, while the resultant length
\[
R=\left|\sum_{\mathfrak n}p(\mathfrak n)\Phi(\mathfrak n)\right|
\]
measures phase concentration.

### 14.2 Phase-augmented generative distance

Let \(d_G(\mathfrak a,\mathfrak b)\) be a generative distance. Define a phase-augmented distance by
\[
d_{GP}\bigl((\mathfrak a,u),(\mathfrak b,v)\bigr)^2
=
d_G(\mathfrak a,\mathfrak b)^2
+
\lambda\, d_{U(1)}(u,v)^2,
\]
where \(\lambda>0\) and
\[
d_{U(1)}(u,v)=|u-v|
\]
or
\[
d_{U(1)}(u,v)=|\operatorname{Arg}(u\bar v)|.
\]

This metric measures both structural and phase separation.

### 14.3 Generative phase curvature

A schematic local curvature may be defined by comparing phase-augmented balls with flat model balls:
\[
K_{GP}(\mathfrak n)
=
1-
\lim_{r\to 0}
\frac{
|B_{GP}(\mathfrak n,r)|
}{
|B_{\mathrm{flat}}(r)|
}.
\]

This combines generative geometric curvature with phase holonomy effects.

---

## 15. Quantum Realization: Berry Phase as Generative Phase

Quantum mechanics provides a natural realization of GPNT.

A normalized state vector \(|\psi\rangle\) and its phase-rotated version
\[
e^{i\chi}|\psi\rangle
\]
represent the same pure state. Global phase is unobservable:
\[
|\psi\rangle\langle\psi|
\mapsto
e^{i\chi}|\psi\rangle\langle\psi|e^{-i\chi}
=
|\psi\rangle\langle\psi|.
\]

Relative phase is observable through interference.

Let a Hamiltonian depend on parameters \(R=(R^1,\ldots,R^d)\), with isolated eigenstate
\[
H(R)|n(R)\rangle
=
E_n(R)|n(R)\rangle.
\]

Under adiabatic transport around a closed loop \(C\) in parameter space, the geometric phase number is
\[
U_{\mathrm{geom}}(C)
=
\exp\left(i\gamma_n(C)\right),
\]
where
\[
\gamma_n(C)
=
\oint_C\mathcal A_n,
\]
and
\[
\mathcal A_n
=
i\langle n(R)|d n(R)\rangle.
\]

Under a local rephasing
\[
|n(R)\rangle\mapsto e^{i\chi(R)}|n(R)\rangle,
\]
one has
\[
\mathcal A_n\mapsto\mathcal A_n-d\chi.
\]

Thus \(\mathcal A_n\) is gauge-dependent, while
\[
U_{\mathrm{geom}}(C)
\]
is gauge-invariant.

The curvature is
\[
\mathcal F_n=d\mathcal A_n,
\]
and if \(C=\partial\Sigma\),
\[
U_{\mathrm{geom}}(C)
=
\exp\left(i\int_\Sigma\mathcal F_n\right).
\]

For a spin-\(\tfrac12\) system with Hamiltonian
\[
H=-\frac{\hbar\omega}{2}\widehat{\mathbf n}\cdot\boldsymbol\sigma,
\]
where
\[
\widehat{\mathbf n}
=
(\sin\theta\cos\phi,\sin\theta\sin\phi,\cos\theta),
\]
the positive eigenstate on the north-pole chart may be chosen as
\[
|+;\theta,\phi\rangle
=
\begin{pmatrix}
\cos(\theta/2)\\
e^{i\phi}\sin(\theta/2)
\end{pmatrix}.
\]

A direct calculation gives
\[
\mathcal A_+
=
-\frac{1-\cos\theta}{2}\,d\phi,
\]
and
\[
\mathcal F_+
=
-\frac12\sin\theta\,d\theta\wedge d\phi.
\]

If \(C\) encloses oriented solid angle \(\Omega(C)\), then
\[
U_{\mathrm{geom}}(C)
=
\exp\left(-\frac{i}{2}\Omega(C)\right).
\]

In GPNT, the parameter loop may be interpreted as a generative cycle. The Berry phase is then a holonomy phase number of a generative line bundle.

---

## 16. Computational Interpretation

### 16.1 Generative phase representation

A computational representation of a generative phase number should store
\[
(n,\Gamma_n,u),
\]
rather than merely \(n\).

For finite systems, one may store
\[
(n,D_G,W_G,H_G,\Phi),
\]
where \(\Phi\in U(1)\) is a phase number.

### 16.2 Phase gates

The elementary qubit phase gate is
\[
P(\varphi)
=
\begin{pmatrix}
1&0\\
0&e^{i\varphi}
\end{pmatrix}.
\]

It multiplies the \(|1\rangle\) component by a phase number. Since global phase is irrelevant, phase gates act on relative phase.

For \(d\)-level systems,
\[
D=\operatorname{diag}(e^{i\theta_1},\ldots,e^{i\theta_d}).
\]

Multiplication by a common phase \(e^{i\chi}\) leaves projective state unchanged. Thus only relative phase classes are operational.

### 16.3 Discrete Fourier kernel

The discrete Fourier transform kernel is
\[
\omega_N^{jk}
=
e^{2\pi i jk/N},
\]
where
\[
\omega_N=e^{2\pi i/N}
\]
is a primitive discrete phase number.

In GPNT, the integers \(j,k\) may be interpreted as labels of generative characters, while \(\omega_N^{jk}\) is the corresponding phase number.

---

## 17. Practical Calculus of Generative Phase Numbers

The following rules prevent category errors.

| Principle | Invariant formulation | Misleading shorthand |
|---|---|---|
| Separate object from coordinate | \(u\in U(1)\) is primary | “Phase is a real number” |
| Compare phases by relative phase | \(u\bar v\) | Subtract principal angles blindly |
| Compose transport multiplicatively | \(\prod u_j\) | Add angles while ignoring branch cuts |
| Detect topology by holonomy | \(\operatorname{Hol}(C)\in U(1)\) | Compare endpoint angles only |
| Average phases circularly | \(\widehat u=(\sum u_k)/|\sum u_k|\) | Arithmetic mean of angles |
| Distinguish gauge potential from observable | \(\exp(i\oint\mathcal A)\) | Treat \(\mathcal A\) as gauge invariant |
| Distinguish value from structure | \(\pi(\mathfrak n)=n\) | Identify \(n\) with \(\mathfrak n\) |
| Distinguish structure from phase | \(\Phi(\mathfrak n)\in U(1)\) | Identify structure with angle |

---

## 18. Examples

### 18.1 The number 6 as a phaseful generative object

The integer \(6\) may arise from multiple generative pathways:
\[
6=1+5,\qquad
6=2+4,\qquad
6=3+3,\qquad
6=2\cdot 3.
\]

In GNT, these are distinct elements or pathways in the generative fiber \(\mathcal F_6\).

In GPNT, assign phase numbers
\[
u_{1+5},\quad
u_{2+4},\quad
u_{3+3},\quad
u_{2\cdot 3}.
\]

The phaseful amplitude for \(6\) is
\[
A(6)
=
w_{1+5}u_{1+5}
+
w_{2+4}u_{2+4}
+
w_{3+3}u_{3+3}
+
w_{2\cdot 3}u_{2\cdot 3}.
\]

If all phases align,
\[
u_{1+5}=u_{2+4}=u_{3+3}=u_{2\cdot 3}=1,
\]
then interference is constructive.

If two dominant pathways have opposite phases,
\[
u_{1+5}=1,
\qquad
u_{2\cdot 3}=-1,
\]
and equal weights, their contributions cancel.

Thus the numerical value \(6\) does not determine the phaseful generative amplitude.

### 18.2 A closed generative cycle

Consider a generative graph with edges
\[
2\to4,\qquad 4\to2.
\]

Assign phases
\[
g_{2\to4}=e^{i\alpha},
\qquad
g_{4\to2}=e^{i\beta}.
\]

The closed-loop holonomy is
\[
\operatorname{Hol}(C)
=
e^{i\alpha}e^{i\beta}
=
e^{i(\alpha+\beta)}.
\]

If
\[
\alpha+\beta\not\equiv 0\pmod{2\pi},
\]
the cycle carries nontrivial phase memory.

The numerical projection returns to \(2\), but the phaseful generative state does not return trivially.

### 18.3 Phaseful Fibonacci recursion

Define a phaseful generative Fibonacci recurrence by
\[
\mathfrak F_{n+2}
=
\mathfrak F_{n+1}\oplus_G\mathfrak F_n,
\]
with phase cocycle
\[
C_F(\mathfrak F_{n+1},\mathfrak F_n)\in U(1).
\]

The numerical projection satisfies
\[
F_{n+2}=F_{n+1}+F_n,
\]
but the phaseful object satisfies
\[
\Phi(\mathfrak F_{n+2})
=
\Phi(\mathfrak F_{n+1})
\Phi(\mathfrak F_n)
C_F(\mathfrak F_{n+1},\mathfrak F_n).
\]

Thus the classical Fibonacci sequence is the numerical shadow of a richer phaseful generative sequence.

---

## 19. Non-Abelian Comparison

The phase group \(U(1)\) is abelian. Therefore all phase factors commute, and curvature is simply
\[
\mathcal F=d\mathcal A.
\]

For higher-rank generative structures, one may encounter matrix-valued holonomies in \(U(r)\). If
\[
\mathcal A=\mathcal A_\mu dx^\mu
\]
is \(\mathfrak u(r)\)-valued, then
\[
\mathcal F
=
d\mathcal A+i\mathcal A\wedge\mathcal A,
\]
or
\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu+i[A_\mu,A_\nu].
\]

Holonomy becomes path-ordered:
\[
U_C
=
\mathcal P\exp\left(i\oint_C\mathcal A\right).
\]

Scalar generative phase numbers are the rank-one abelian case. They are simpler but already possess nontrivial topology, winding, holonomy, and curvature.

---

## 20. Fundamental Conjectures

### Conjecture I — Generative phase fiber growth

There exist natural generative systems for which the phaseful fiber sum
\[
A(n)=\sum_{\mathfrak n\in\mathcal F_n}\Phi(\mathfrak n)
\]
exhibits asymptotic behavior not predictable from \(|\mathcal F_n|\) alone.

### Conjecture II — Phase coherence of generative primes

Under canonical generative rules, generatively prime states exhibit higher phase coherence than generatively composite states.

### Conjecture III — Phase zeta singularities

Singularities of
\[
\zeta_{GP}(s)
\]
encode structural phase transitions in generative arithmetic.

### Conjecture IV — Holonomic complexity

Arithmetic complexity correlates with nontrivial holonomy in generative phase space.

### Conjecture V — Phase universality

A sufficiently expressive generative phase system can encode arbitrary finite \(U(1)\)-valued computational histories.

---

## 21. Open Problems

1. **Minimal axiomatization.**  
   What is the weakest axiom system supporting a nontrivial GPNT?

2. **Classification of phase cocycles.**  
   Classify additive and multiplicative \(U(1)\)-cocycles over natural generative semirings.

3. **Generative phase cohomology.**  
   Develop a cohomology theory whose cocycles are arithmetic phase laws.

4. **Unique phase factorization.**  
   Determine conditions under which generative prime factorization admits unique phase decomposition.

5. **Phaseful prime distribution.**  
   Find asymptotic laws for phase-weighted generative prime counting functions.

6. **Generative phase curvature.**  
   Construct canonical metrics on generative phase spaces and relate curvature to arithmetic complexity.

7. **Computational databases.**  
   Compute phase invariants for finite-depth generative integer models.

8. **Quantum encodings.**  
   Determine whether generative phase holonomy can be used as a resource in quantum algorithms.

---

## 22. Conclusion

Generative Phase Number Theory extends Generative Number Theory by adding a phase-valued layer governed by the circle group \(U(1)\). The resulting object is not merely a number, nor merely a structured number, but a phaseful generative structure.

The fundamental hierarchy is

\[
\boxed{
\text{Value}
\quad\longrightarrow\quad
\text{Generative Structure}
\quad\longrightarrow\quad
\text{Phase Structure}.
}
\]

The central distinction is between:

\[
\boxed{
\text{phase number }u\in U(1)
}
\]

and

\[
\boxed{
\text{phase angle }\theta\in\mathbb R/(2\pi\mathbb Z).
}
\]

The phase number is globally meaningful. The phase angle is a local coordinate.

Generative transformations carry phase. Generative cycles possess holonomy. Generative fibers possess phase distributions. Generative primes may possess phase structure. Generative zeta functions acquire phase weights.

The classical integer is therefore not denied or replaced. It is recovered as a projection of a richer object:

\[
\boxed{
n=\pi(\mathfrak n)
}
\]

and the generative phase object itself satisfies

\[
\boxed{
\mathfrak z=(\mathfrak n,u),
\qquad
u\in U(1).
}
\]

The deepest formulation of GPNT is therefore:

\[
\boxed{
\text{Number}
=
\text{Value}
+
\text{Generative Structure}
+
\text{Phase Structure}.
}
\]

Equivalently,

\[
\boxed{
\text{A number is not only what it is, but also how it is generated, and with what phase.}
}
\]

---

## Appendix A. Derivation of Cocycle Gauge Transformation

Let
\[
(\mathfrak a,u)\oplus_P(\mathfrak b,v)
=
\left(
\mathfrak a\oplus_G\mathfrak b,
uvC_+(\mathfrak a,\mathfrak b)
\right).
\]

Define new phase representatives by
\[
u'=\chi(\mathfrak a)u,
\qquad
v'=\chi(\mathfrak b)v.
\]

We seek \(C_+'\\) such that
\[
(\mathfrak a,u')\oplus_P'(\mathfrak b,v')
=
\left(
\mathfrak a\oplus_G\mathfrak b,
\chi(\mathfrak a\oplus_G\mathfrak b)uvC_+(\mathfrak a,\mathfrak b)
\right).
\]

The left-hand side using \(C_+'\\\) is
\[
\left(
\mathfrak a\oplus_G\mathfrak b,
u'v'C_+'(\mathfrak a,\mathfrak b)
\right)
=
\left(
\mathfrak a\oplus_G\mathfrak b,
\chi(\mathfrak a)\chi(\mathfrak b)uvC_+'(\mathfrak a,\mathfrak b)
\right).
\]

Equating phases gives
\[
\chi(\mathfrak a)\chi(\mathfrak b)C_+'(\mathfrak a,\mathfrak b)
=
\chi(\mathfrak a\oplus_G\mathfrak b)C_+(\mathfrak a,\mathfrak b).
\]

Therefore
\[
C_+'(\mathfrak a,\mathfrak b)
=
\chi(\mathfrak a\oplus_G\mathfrak b)
C_+(\mathfrak a,\mathfrak b)
\chi(\mathfrak a)^{-1}\chi(\mathfrak b)^{-1}.
\]

This is the standard \(U(1)\) 2-coboundary transformation.

---

## Appendix B. Gauge Invariance of Loop Holonomy

Let
\[
C:\mathfrak n_0\to\mathfrak n_1\to\cdots\to\mathfrak n_k=\mathfrak n_0
\]
be a closed loop. Its holonomy is
\[
\operatorname{Hol}(C)
=
\prod_{j=0}^{k-1}g_{\mathfrak n_j\mathfrak n_{j+1}}.
\]

Under rephasing,
\[
g_{\mathfrak n_j\mathfrak n_{j+1}}
\mapsto
\chi(\mathfrak n_{j+1})
g_{\mathfrak n_j\mathfrak n_{j+1}}
\chi(\mathfrak n_j)^{-1}.
\]

Thus
\[
\begin{aligned}
\operatorname{Hol}'(C)
&=
\prod_{j=0}^{k-1}
\chi(\mathfrak n_{j+1})
g_{\mathfrak n_j\mathfrak n_{j+1}}
\chi(\mathfrak n_j)^{-1}\\
&=
\left(\prod_{j=0}^{k-1}\chi(\mathfrak n_{j+1})\chi(\mathfrak n_j)^{-1}\right)
\left(\prod_{j=0}^{k-1}g_{\mathfrak n_j\mathfrak n_{j+1}}\right).
\end{aligned}
\]

Because the loop is closed, the \(\chi\)-product telescopes to \(1\). Hence
\[
\operatorname{Hol}'(C)=\operatorname{Hol}(C).
\]

---

## Appendix C. Berry Connection Transformation

Let
\[
|n'\rangle=e^{i\chi}|n\rangle.
\]

Then
\[
d|n'\rangle
=
i\,d\chi\,e^{i\chi}|n\rangle
+
e^{i\chi}d|n\rangle.
\]

Therefore
\[
\begin{aligned}
\mathcal A_n'
&=
i\langle n'|dn'\rangle\\
&=
i\langle n|e^{-i\chi}
\left(
i\,d\chi\,e^{i\chi}|n\rangle
+
e^{i\chi}d|n\rangle
\right)\\
&=
i\langle n|
\left(
i\,d\chi\,|n\rangle+d|n\rangle
\right)\\
&=
-d\chi+i\langle n|dn\rangle\\
&=
\mathcal A_n-d\chi.
\end{aligned}
\]

For a closed loop,
\[
\oint_C\mathcal A_n'
=
\oint_C\mathcal A_n-\oint_Cd\chi.
\]

Since \(\oint_Cd\chi\in 2\pi\mathbb Z\) for single-valued rephasing up to winding, the phase number is unchanged:
\[
\exp\left(i\oint_C\mathcal A_n'\right)
=
\exp\left(i\oint_C\mathcal A_n\right).
\]

---

## References

1. M. Hanks, *Phase Numbers: An Intrinsic Calculus of Unit-Complex Scalars, Circular Coordinates, and Holonomy*, preprint, 2026.

2. M. Hanks, *Generative Number Theory: A Foundational Theory of Numbers as Self-Generating Arithmetic Structures*, preprint, 2026.

3. M. V. Berry, “Quantal phase factors accompanying adiabatic changes,” *Proceedings of the Royal Society A* **392**, 45–57 (1984).

4. B. Simon, “Holonomy, the quantum adiabatic theorem, and Berry’s phase,” *Physical Review Letters* **51**, 2167–2170 (1983).

5. A. Hatcher, *Algebraic Topology*, Cambridge University Press, 2002.

6. J. W. Milnor and J. D. Stasheff, *Characteristic Classes*, Princeton University Press, 1974.

7. M. Nakahara, *Geometry, Topology and Physics*, 2nd ed., CRC Press, 2003.

8. B. C. Hall, *Lie Groups, Lie Algebras, and Representations*, 2nd ed., Springer, 2015.

9. G. B. Folland, *A Course in Abstract Harmonic Analysis*, 2nd ed., CRC Press, 2016.

10. K. V. Mardia and P. E. Jupp, *Directional Statistics*, Wiley, 1999.

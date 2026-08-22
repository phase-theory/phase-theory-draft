# Phase Numbers: An Intrinsic Calculus of Unit-Complex Scalars, Circular Coordinates, and Holonomy

**Author:** Marlon Hanks  
**Affiliation:** Independent Researcher, Dust LLC  
**Document type:** Mathematical white paper / preprint  
**Date:** 22 August 2026  
**Keywords:** unit circle, complex phase, $U(1)$, argument, covering map, winding number, gauge theory, Berry phase, Fourier character, circular statistics  
**MSC 2020:** 30A99, 22E67, 53C05, 58J90, 81Q70, 42A16

## Abstract

This paper introduces **phase number** as a precise term for an intrinsic unit-modulus complex scalar,

\[
 u\in \mathbb T\equiv U(1)=\{z\in\mathbb C:|z|=1\},
\]

and develops a unified calculus around that object. The central distinction is between the phase number $u=e^{i\theta}$, which is globally defined, and a phase angle $\theta$, which is defined only modulo $2\pi$ and may fail to exist as a continuous global real-valued function. This distinction simultaneously resolves familiar ambiguities in polar decomposition, clarifies the origin of branch cuts and phase unwrapping, and exposes the common structure of wave interference, Fourier modes, gauge transformations, and quantum geometric phase.

Starting from the Lie-group identification $U(1)\cong\mathbb R/(2\pi\mathbb Z)$, the paper derives polar factorization, multiplicative composition, character theory, winding formulas, and a criterion for global phase lifting. It then places phase numbers in the geometry of complex line bundles: local phase factors are transition functions, connections are local one-forms, curvature is the gauge-invariant differential field, and holonomy is an observable phase number. The adiabatic quantum derivation is given explicitly and specialized to a two-level Hamiltonian, for which the geometric phase is the exponential of one-half the enclosed solid angle. The final sections formulate practical rules for signals, numerical data, circular averaging, and quantum computation. The resulting framework treats phase not as an auxiliary angle but as a compact-group-valued quantity with algebraic, topological, and operational content.

> **Thesis.** A phase number is the primary global object. A phase angle is a local coordinate on that object. Confusing the coordinate with the object is the source of most elementary and advanced phase ambiguities.

## 1. Scope, terminology, and analytical position

The word *phase* is used across mathematics, physics, engineering, and computation with several closely related meanings. It can denote an angle in polar coordinates, a factor multiplying a complex amplitude, a coordinate on a periodic orbit, a gauge degree of freedom, or a holonomy acquired by transport. These usages are compatible, but they become technically dangerous when the distinction between an **angle-valued representative** and a **unit-complex scalar** is suppressed.

This white paper adopts the following convention. A **phase number** is a member of the circle group $U(1)$; a **phase angle** is an element of the quotient $\mathbb R/2\pi\mathbb Z$; and a **phase lift** is a locally or globally selected real representative of that quotient class. Thus the notation

\[
\theta\ \mapsto\ u=e^{i\theta}
\tag{1}
\]

is not merely an identity between two interchangeable symbols. It is a surjective covering homomorphism with a discrete kernel. The phase number $u$ is unchanged by $\theta\mapsto\theta+2\pi k$, while a chosen lift is not. This is the basic structural fact from which branch cuts, winding, gauge covariance, and interference follow.

The term “phase number” is used here as a deliberate technical label rather than as a claim about universal terminology. It allows one to state arguments in an invariant way: instead of saying that an angle is “defined up to $2\pi$,” one says that the phase number is defined and an angle is a choice of coordinate. Complex numbers admit the usual polar representation with modulus and argument; the latter is conventionally called phase in this setting [1]. The present treatment refines that standard representation by assigning primary status to the unit-circle factor.

| Object | Mathematical type | Globally defined? | Composition law | Typical notation |
| --- | --- | --- | --- | --- |
| Complex amplitude | $z\in\mathbb C$ | Yes | Addition and multiplication | $z$ |
| Magnitude | $r\in\mathbb R_{\geq 0}$ | Yes | Multiplication for $r>0$ | $|z|$ |
| **Phase number** | $u\in U(1)$ | Yes | Multiplication | $e^{i\theta}$ |
| Phase angle | $[\theta]\in\mathbb R/2\pi\mathbb Z$ | Yes as a quotient class | Addition modulo $2\pi$ | $\arg z$ |
| Phase lift | $\theta\in\mathbb R$ | Generally only locally | Ordinary addition | $\widetilde\theta$ |
| Winding number | $n\in\mathbb Z$ | Yes for a closed loop | Addition | $\operatorname{wind}$ |

The paper proceeds from elementary complex algebra to topology, harmonic analysis, differential geometry, and quantum theory. No physical interpretation is imposed on the algebraic object in advance. Rather, the same compact abelian group is shown to organize all of these settings.

## 2. Algebraic foundation: the circle group as phase space

### 2.1 Definition and exponential parametrization

Define the **circle group**

\[
\mathbb T=U(1)=\{u\in\mathbb C:u\bar u=1\}.
\tag{2}
\]

Closure under multiplication follows immediately: if $u\bar u=v\bar v=1$, then $(uv)\overline{(uv)}=(u\bar u)(v\bar v)=1$. The identity is $1$, and $u^{-1}=\bar u$. The group is abelian because complex multiplication is abelian.

The exponential map

\[
\operatorname{Exp}:\mathbb R\longrightarrow U(1),\qquad \operatorname{Exp}(\theta)=e^{i\theta}=\cos\theta+i\sin\theta
\tag{3}
\]

is a smooth, surjective homomorphism. Its kernel is precisely $2\pi\mathbb Z$, because $e^{i\theta}=1$ if and only if $\theta=2\pi k$ for some $k\in\mathbb Z$. The first isomorphism theorem therefore yields

\[
U(1)\cong \mathbb R/(2\pi\mathbb Z).
\tag{4}
\]

Equation (4) is the exact content behind the informal assertion that phase is periodic. It says that a circle-valued phase is not a real number subject to an externally imposed identification; it is an element of a quotient group whose additive coordinate has a lattice of redundancies.

![Figure 1. The unit circle $U(1)$ with a selected phase number $u=e^{i\theta}$. The point $1$ simultaneously represents $e^{i0}$ and $e^{i2\pi}$, illustrating the quotient identification of phase angles.](https://private-us-east-1.manuscdn.com/sessionFile/J9CaYBXeQzJRuWHgg4ijyo/sandbox/6uebYAqb7EDQkq19WSyDrf-images_1787438236800_na1fn_L2hvbWUvdWJ1bnR1L3BoYXNlX3VuaXRfY2lyY2xl.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSjlDYVlCWGVRekpSdVdIZ2c0aWp5by9zYW5kYm94LzZ1ZWJZQXFiN0VEUWtxMTlXU3lEcmYtaW1hZ2VzXzE3ODc0MzgyMzY4MDBfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzQm9ZWE5sWDNWdWFYUmZZMmx5WTJ4bC5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3ODk0MzA0MDB9fX1dfQ__&Key-Pair-Id=K2QY5QTL8JSY6C&Signature=MEUCIQDhAUwCexD2VqRHhEAk9C~1eC4npg6pHD0KLf2RJsLi9wIgB7BrIJ4inzFelLQJwRmNbd4RzTJfsbqFwUcMotTuItk_)

**Figure 1.** The phase group as the unit circle. The ray has unit length; its coordinates are $(\cos\theta,\sin\theta)$. The endpoint is the phase number, whereas $\theta$ is a chosen circular coordinate.

### 2.2 Polar factorization and intrinsic phase extraction

Every nonzero complex number has a unique decomposition into a positive magnitude and a phase number.

**Proposition 1 (polar factorization).** For each $z\in\mathbb C^\times=\mathbb C\setminus\{0\}$, there exist unique $r\in\mathbb R_{>0}$ and $u\in U(1)$ such that

\[
 z=ru.
\tag{5}
\]

They are given by

\[
 r=|z|=(z\bar z)^{1/2},\qquad u=\operatorname{ph}(z)\equiv\frac{z}{|z|}.
\tag{6}
\]

**Proof.** Since $z\neq0$, one has $r=|z|>0$. Put $u=z/r$. Then

\[
 u\bar u=\frac{z\bar z}{r^2}=1,
\]

so $u\in U(1)$ and $z=ru$. If $z=r_1u_1=r_2u_2$ with $r_j>0$ and $u_j\in U(1)$, taking absolute values gives $r_1=r_2=|z|$; division then gives $u_1=u_2$. $\square$

The notation $\operatorname{ph}(z)$ is useful because it remains meaningful without selecting an argument. Whenever a local angle $\theta$ is chosen, $\operatorname{ph}(z)=e^{i\theta}$, but the right-hand side does not privilege one lift among $\theta+2\pi k$. Thus

\[
\mathbb C^\times\cong \mathbb R_{>0}\times U(1)
\tag{7}
\]

as abelian Lie groups. The radial factor records scale; the phase-number factor records direction in the complex plane.

### 2.3 Composition, inversion, and powers

For phase numbers $u=e^{i\alpha}$ and $v=e^{i\beta}$,

\[
uv=e^{i(\alpha+\beta)},\qquad u^{-1}=\bar u=e^{-i\alpha}.
\tag{8}
\]

Euler’s formula and the trigonometric addition laws give the first relation explicitly:

\[
\begin{aligned}
(\cos\alpha+i\sin\alpha)(\cos\beta+i\sin\beta)
&=\cos\alpha\cos\beta-\sin\alpha\sin\beta\\
&\quad+i(\sin\alpha\cos\beta+\cos\alpha\sin\beta)\\
&=\cos(\alpha+\beta)+i\sin(\alpha+\beta).
\end{aligned}
\tag{9}
\]

By induction and inversion, one obtains de Moivre’s law

\[
 u^n=e^{in\alpha},\qquad n\in\mathbb Z.
\tag{10}
\]

Multiplication therefore represents addition of angular classes without ever committing to a branch of the argument. The identity $(e^{i\alpha})^n=e^{in\alpha}$ is unambiguous even when neither $\alpha$ nor $n\alpha$ has been selected as a principal angle.

### 2.4 Roots of unity and finite phase subgroups

The $n$th roots of unity form the finite subgroup

\[
\mu_n=\{u\in U(1):u^n=1\}
=\left\{e^{2\pi i k/n}:k=0,\dots,n-1\right\}\cong\mathbb Z/n\mathbb Z.
\tag{11}
\]

These are the discrete phase alphabets underlying cyclic symmetry, the discrete Fourier transform, clock variables, and finite-dimensional quantum phase gates. The passage from $\mu_n$ to $U(1)$ is a passage from finite cyclic symmetry to continuous circular symmetry, not a change in the underlying multiplicative logic.

## 3. Topology of phase: covering maps, branches, and winding

### 3.1 The argument is not globally a function

The principal argument $\operatorname{Arg}:\mathbb C^\times\to(-\pi,\pi]$ is a convenient convention, but it is discontinuous along its branch cut. That discontinuity is not caused by a poor choice of interval. It follows from the topology of the circle.

**Theorem 1 (no global continuous argument).** There is no continuous map

\[
 a:U(1)\longrightarrow\mathbb R
\]

such that $e^{ia(u)}=u$ for every $u\in U(1)$.

**Proof.** Suppose such an $a$ exists. Let $h(t)=a(e^{it})$ for $t\in[0,2\pi]$. Then $e^{ih(t)}=e^{it}$, so $h(t)-t\in2\pi\mathbb Z$. The function $h(t)-t$ is continuous and has values in a discrete set; it is therefore constant: $h(t)=t+2\pi k$. Hence $h(0)=2\pi k$ and $h(2\pi)=2\pi(k+1)$. But $e^{i0}=e^{i2\pi}=1$, so both values must equal $a(1)$, a contradiction. $\square$

The theorem says that one cannot globally replace a phase number by a real angle while preserving continuity. A branch cut removes enough of the domain to make a continuous lift possible. In computational work, a phase-unwrapping algorithm does not abolish this theorem; it makes additional continuity or sampling assumptions to construct a lift along a particular path.

### 3.2 Lifted paths and the winding integer

Let $\gamma:[0,1]\to U(1)$ be a continuous path. Since $\operatorname{Exp}:\mathbb R\to U(1)$ is a covering map, a lift $\widetilde\gamma:[0,1]\to\mathbb R$ exists after an initial value is chosen such that

\[
\gamma(t)=e^{i\widetilde\gamma(t)}.
\tag{12}
\]

If $\gamma$ is closed, then $\gamma(1)=\gamma(0)$ and therefore

\[
\widetilde\gamma(1)-\widetilde\gamma(0)=2\pi n,
\qquad n\in\mathbb Z.
\tag{13}
\]

The integer $n$ is the **winding number**. It counts the net number of times the phase path winds around the origin. The difference is invariant under a continuous deformation of the closed path that avoids the origin, which is the elementary origin of its topological stability.

For a smooth loop $u:C\to U(1)$, the same invariant has the differential expression

\[
\operatorname{wind}(u;0)
=\frac{1}{2\pi i}\oint_C u^{-1}du.
\tag{14}
\]

To derive (14), locally write $u=e^{i\theta}$. Then $u^{-1}du=i\,d\theta$, so the integral is

\[
\frac{1}{2\pi i}\oint_C i\,d\theta
=\frac{\widetilde\theta(1)-\widetilde\theta(0)}{2\pi}
=n.
\tag{15}
\]

Although $\theta$ may not be globally defined, the one-form $u^{-1}du$ is. This is the first appearance of a general principle: **global phase information is naturally encoded by invariant differential forms or exponentiated quantities, not by a single global angle coordinate.**

### 3.3 Phase fields and the obstruction to global lifting

Let $X$ be a manifold or topological space, and let $u:X\to U(1)$ be a smooth phase-number field. Define its real Maurer–Cartan one-form by

\[
\alpha\equiv\frac{1}{i}u^{-1}du.
\tag{16}
\]

Locally, when $u=e^{i\theta}$, this is simply $\alpha=d\theta$. Since $U(1)$ is abelian,

\[
 d\alpha=\frac{1}{i}d(u^{-1}du)=0.
\tag{17}
\]

The form is closed, but it need not be exact. Its periods obey

\[
\frac{1}{2\pi}\oint_C\alpha\in\mathbb Z
\tag{18}
\]

for every closed loop $C$. A global real-valued lift $\theta:X\to\mathbb R$ with $u=e^{i\theta}$ exists precisely when all of these periods vanish, equivalently when the integral cohomology class represented by $\alpha/2\pi$ vanishes. This criterion separates a mere local coordinate issue from a genuine topological obstruction.

## 4. Harmonic analysis: phase numbers as irreducible characters

The circle group is compact and abelian. Its irreducible unitary representations are one-dimensional, hence are phase-number-valued characters. For every integer $n$, define

\[
\chi_n:U(1)\to U(1),\qquad \chi_n(e^{i\theta})=e^{in\theta}.
\tag{19}
\]

**Proposition 2.** Every continuous group homomorphism $\chi:U(1)\to U(1)$ is equal to $\chi_n$ for a unique $n\in\mathbb Z$.

**Proof.** The composition $\chi\circ\operatorname{Exp}:\mathbb R\to U(1)$ has a continuous lift $\widetilde\chi:\mathbb R\to\mathbb R$ after setting $\widetilde\chi(0)=0$. The homomorphism law implies that $\widetilde\chi(x+y)-\widetilde\chi(x)-\widetilde\chi(y)$ lies in $2\pi\mathbb Z$ and is continuous; it is therefore zero. Thus $\widetilde\chi(x)=cx$ for some real $c$. Periodicity, $\chi(e^{i(x+2\pi)})=\chi(e^{ix})$, requires $e^{i2\pi c}=1$, so $c=n\in\mathbb Z$. Therefore $\chi(e^{i\theta})=e^{in\theta}$. Uniqueness is immediate. $\square$

The characters obey the orthogonality relation

\[
\frac{1}{2\pi}\int_0^{2\pi}e^{i(n-m)\theta}\,d\theta=\delta_{nm}.
\tag{20}
\]

For $n=m$, the integrand is one. For $n\ne m$, direct integration gives

\[
\frac{1}{2\pi}\left[\frac{e^{i(n-m)\theta}}{i(n-m)}\right]_{0}^{2\pi}=0.
\tag{21}
\]

Equation (20) is the algebraic engine of Fourier analysis. A periodic signal is decomposed into integer powers of a basic phase number $e^{i\theta}$; the integers arise because only integral characters descend from the universal cover $\mathbb R$ to the quotient circle. In this sense, Fourier mode number is a representation-theoretic winding index.

| Setting | Basic phase number | Character or phase factor | Integer label |
| --- | --- | --- | --- |
| Fourier series | $e^{i\theta}$ | $e^{in\theta}$ | Harmonic $n$ |
| Periodic time signal | $e^{i\omega t}$ | $e^{in\omega t}$ | Harmonic order $n$ |
| Circle-valued field | $u(x)$ | $u(x)^n$ | Charge / winding mode $n$ |
| Discrete cyclic group | $e^{2\pi i/N}$ | $e^{2\pi i nk/N}$ | Discrete frequency $n$ |

## 5. Differential geometry: phase numbers, line bundles, and gauge fields

### 5.1 Local frames and transition phase numbers

A complex line bundle $L\to M$ is locally a product $U_a\times\mathbb C$, but its local trivializations may be glued with nontrivial phase data. Choose unit local frames $s_a$ over an open cover $\{U_a\}$. On overlaps,

\[
 s_b=g_{ab}s_a,
\qquad g_{ab}:U_a\cap U_b\to U(1).
\tag{22}
\]

The functions $g_{ab}$ are phase-number fields. Their cocycle description is the standard local-to-global formulation of a complex line bundle [8] [10]. Compatibility on triple overlaps requires the cocycle condition

\[
 g_{ab}g_{bc}g_{ca}=1.
\tag{23}
\]

Thus topology may be encoded entirely in how local phase numbers fail to be globally reducible to a single frame. This is the correct geometric formulation of a gauge phase: it is a transition function between local descriptions, not necessarily a globally meaningful scalar angle.

### 5.2 Connection, curvature, and tensor notation

Let $\nabla$ be a unitary connection on $L$. In a local unit frame $s_a$, define the real connection one-form $\mathcal A_a$ by

\[
\nabla s_a=i\mathcal A_a\otimes s_a,
\qquad
\mathcal A_a=A_{a\mu}\,dx^\mu.
\tag{24}
\]

A local phase transformation changes the frame according to

\[
 s_a\longmapsto s_a'=e^{i\chi_a}s_a.
\tag{25}
\]

A direct substitution into (24) gives

\[
\mathcal A_a' =\mathcal A_a+d\chi_a,
\qquad
A_{a\mu}'=A_{a\mu}+\partial_\mu\chi_a.
\tag{26}
\]

The curvature two-form is

\[
\mathcal F=d\mathcal A_a
=\frac12F_{\mu\nu}\,dx^\mu\wedge dx^\nu,
\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu.
\tag{27}
\]

Unlike the connection potential, $\mathcal F$ is gauge invariant in the abelian case. The tensor $F_{\mu\nu}$ is antisymmetric, $F_{\mu\nu}=-F_{\nu\mu}$, and satisfies the Bianchi identity

\[
\partial_{[\lambda}F_{\mu\nu]}=0.
\tag{28}
\]

The square brackets denote antisymmetrization over the enclosed indices. In four-dimensional electromagnetic notation, $\mathcal A$ is the gauge potential and $\mathcal F$ packages the electric and magnetic fields; the group of gauge transformations is $U(1)$.

### 5.3 Holonomy as the invariant phase outcome

Parallel transport around a closed loop $C$ returns a vector in the fiber to the same fiber, but it need not return the vector itself. In a local gauge, the resulting phase number is

\[
\operatorname{Hol}_C(\nabla)
=\exp\!\left(i\oint_C\mathcal A\right)\in U(1).
\tag{29}
\]

Under (26), the loop integral changes by $\oint_Cd\chi=0$ whenever $\chi$ is single-valued on the loop, so the exponentiated quantity is gauge invariant. If $C=\partial\Sigma$ and the bundle is trivialized over the spanning surface, Stokes’ theorem gives

\[
\operatorname{Hol}_C(\nabla)
=\exp\!\left(i\int_\Sigma\mathcal F\right).
\tag{30}
\]

The right-hand side converts a local gauge field into an observable global phase number. When no single spanning surface or no single trivialization is available, the holonomy remains defined but its expression must be patched by transition phase numbers. This is precisely where topology enters gauge theory.

The geometric interpretation of quantum phase as holonomy was articulated in foundational form by Simon, and Berry’s adiabatic result supplies the central physical realization [3] [4]. The relevant object is not a numerical angle in isolation, but a $U(1)$ element attached to transport around a loop.

## 6. Quantum mechanics: rays, relative phase, and the Berry holonomy

### 6.1 Global versus relative phase

A normalized quantum vector $|\psi\rangle\in\mathcal H$ represents the same pure state as

\[
 |\psi\rangle\sim e^{i\chi}|\psi\rangle,
\qquad e^{i\chi}\in U(1).
\tag{31}
\]

The space of pure states is therefore projective Hilbert space, not the unit sphere in Hilbert space itself [5]. Global phase cancels from the density operator:

\[
 |\psi\rangle\langle\psi|
\longmapsto
 e^{i\chi}|\psi\rangle\langle\psi|e^{-i\chi}
 =|\psi\rangle\langle\psi|.
\tag{32}
\]

By contrast, relative phase is operational. Let $a,b\geq0$ and $u=e^{i\alpha}$, $v=e^{i\beta}$. Then

\[
\begin{aligned}
|au+bv|^2
&=(au+bv)(a\bar u+b\bar v)\\
&=a^2+b^2+ab(u\bar v+\bar u v)\\
&=a^2+b^2+2ab\operatorname{Re}(u\bar v)\\
&=a^2+b^2+2ab\cos(\alpha-\beta).
\end{aligned}
\tag{33}
\]

The interference term depends only on the relative phase number $u\bar v=e^{i(\alpha-\beta)}$. Multiplying both amplitudes by a common phase number $w$ leaves (33) unchanged. This is the algebraic reason that global phase is unobservable for an isolated pure state while phase differences are measurable.

### 6.2 Adiabatic transport and geometric phase

Let a Hamiltonian depend smoothly on parameters $R=(R^1,\dots,R^d)$ and have an isolated normalized eigenstate

\[
 H(R)|n(R)\rangle=E_n(R)|n(R)\rangle.
\tag{34}
\]

For adiabatic evolution along $R(t)$, use the ansatz

\[
|\psi(t)\rangle=
 e^{i\alpha_n(t)}
 e^{-\frac{i}{\hbar}\int_0^tE_n(t')\,dt'}
 |n(R(t))\rangle.
\tag{35}
\]

Insert (35) into the Schrödinger equation $i\hbar\partial_t|\psi\rangle=H|\psi\rangle$. The energy terms cancel by (34); multiplying the remaining equation from the left by $\langle n|$ yields

\[
 \dot\alpha_n(t)=i\langle n(R(t))|\dot n(R(t))\rangle.
\tag{36}
\]

Thus the geometric contribution for a closed parameter curve $C$ is

\[
\gamma_n(C)=\oint_C\mathcal A_n,
\qquad
\mathcal A_n=i\langle n(R)|d n(R)\rangle,
\tag{37}
\]

and the corresponding physical phase number is

\[
U_{\mathrm{geom}}(C)=e^{i\gamma_n(C)}.
\tag{38}
\]

The Berry convention in (37) is the negative of the local connection coefficient in (24) when the eigenvector itself is used as a local frame; this conventional sign has no effect on the phase-number invariant once it is used consistently. Under the local rephasing $|n(R)\rangle\mapsto e^{i\chi(R)}|n(R)\rangle$,

\[
\mathcal A_n\mapsto\mathcal A_n-d\chi.
\tag{39}
\]

The connection one-form is gauge dependent, while the closed-loop phase number (38) is gauge invariant. Berry’s original analysis showed that an adiabatically transported eigenstate acquires such a geometric phase factor in addition to its dynamical phase [3]. Equation (37) places that result directly into the connection-holonomy formalism of Section 5.

The associated curvature is

\[
\mathcal F_n=d\mathcal A_n
=\frac12F^{(n)}_{\mu\nu}\,dR^\mu\wedge dR^\nu,
\tag{40}
\]

with

\[
F^{(n)}_{\mu\nu}
=\partial_\mu A^{(n)}_\nu-\partial_\nu A^{(n)}_\mu.
\tag{41}
\]

If the loop bounds a surface $\Sigma$ within one gauge chart, then

\[
U_{\mathrm{geom}}(C)=\exp\!\left(i\int_\Sigma\mathcal F_n\right).
\tag{42}
\]

### 6.3 Spin-$\tfrac12$ example and solid-angle law

Consider the two-level Hamiltonian

\[
H=-\frac{\hbar\omega}{2}\,\widehat{\mathbf n}\cdot\boldsymbol\sigma,
\qquad
\widehat{\mathbf n}=(\sin\theta\cos\phi,\sin\theta\sin\phi,\cos\theta),
\tag{43}
\]

where $\boldsymbol\sigma=(\sigma_x,\sigma_y,\sigma_z)$ are the Pauli matrices. On the north-pole chart, choose the positive eigenstate

\[
|+;\theta,\phi\rangle=
\begin{pmatrix}
\cos(\theta/2)\\
e^{i\phi}\sin(\theta/2)
\end{pmatrix}.
\tag{44}
\]

Differentiation gives

\[
 d|+\rangle=
\begin{pmatrix}
-\frac12\sin(\theta/2)d\theta\\
e^{i\phi}\left(i\sin(\theta/2)d\phi+\frac12\cos(\theta/2)d\theta\right)
\end{pmatrix}.
\tag{45}
\]

Contracting with $\langle+|$ cancels the $d\theta$ terms and yields

\[
\mathcal A_+=i\langle+|d+\rangle
=-\sin^2\!\left(\frac\theta2\right)d\phi
=-\frac{1-\cos\theta}{2}\,d\phi.
\tag{46}
\]

Therefore

\[
\mathcal F_+=d\mathcal A_+
=-\frac12\sin\theta\,d\theta\wedge d\phi.
\tag{47}
\]

If $C$ encloses oriented solid angle $\Omega(C)$ on the Bloch sphere, then

\[
U_{\mathrm{geom}}(C)
=\exp\!\left(-\frac{i}{2}\Omega(C)\right).
\tag{48}
\]

The geometric result is itself a phase number. Its logarithm is only locally defined modulo $2\pi$, but the exponential in (48) is globally unambiguous. The apparent singularity of (46) at the south pole is a gauge-chart feature; the curvature (47) is regular as a globally defined two-form on the appropriate bundle. This distinction mirrors the branch behavior of an ordinary argument, but now on parameter space rather than on the complex plane.

## 7. Signal processing, numerical analysis, and circular data

### 7.1 Phasors and linear systems

A harmonic real signal can be represented as the real part of a complex amplitude:

\[
 x(t)=\operatorname{Re}\{A e^{i\omega t}\},
\qquad A=|A|u,\quad u\in U(1).
\tag{49}
\]

The amplitude $A$ carries magnitude and phase number. In a linear time-invariant system with transfer function $H(\omega)$,

\[
Y(\omega)=H(\omega)X(\omega).
\tag{50}
\]

Polar factorization makes the two effects transparent:

\[
|Y|=|H||X|,
\qquad
\operatorname{ph}(Y)=\operatorname{ph}(H)\operatorname{ph}(X).
\tag{51}
\]

Thus gain composes multiplicatively in $\mathbb R_{>0}$ and phase composes multiplicatively in $U(1)$. An additive angle law is a coordinate expression of the latter statement.

### 7.2 Circular mean without branch artifacts

For sampled phases $u_k=e^{i\theta_k}$, define the complex resultant

\[
\bar u=\frac1N\sum_{k=1}^Nu_k.
\tag{52}
\]

If $\bar u\ne0$, the normalized circular mean phase number is

\[
\widehat u=\frac{\bar u}{|\bar u|}.
\tag{53}
\]

Any selected argument of $\widehat u$ is a mean angle. This construction is branch independent. For example, angles $1^\circ$ and $359^\circ$ have phase numbers that are close on $U(1)$; averaging their raw representatives as ordinary real numbers produces $180^\circ$, while (52) produces a resultant near $1$. The difference is not a numerical trick: the latter calculation respects the topology of the sample space.

The resultant length

\[
R=|\bar u|\in[0,1]
\tag{54}
\]

measures directional concentration. If $R=0$, no mean phase direction exists. In such a case, returning an arbitrary angle is mathematically less informative than reporting the vanishing resultant.

### 7.3 Phase unwrapping as controlled lifting

Suppose ordered samples $u_k\in U(1)$ are believed to arise from a slowly varying real phase lift. The branch-independent local increment is

\[
\Delta\theta_k=
\operatorname{Arg}(u_{k+1}\bar u_k)\in(-\pi,\pi].
\tag{55}
\]

Given a seed $\widetilde\theta_0$, set

\[
\widetilde\theta_{k+1}=\widetilde\theta_k+\Delta\theta_k.
\tag{56}
\]

This procedure is valid only when the true intersample phase advance is known, or assumed, to lie within the chosen branch interval. If phase advances can exceed $\pi$ between samples, aliasing occurs and the lift cannot be inferred from local phase numbers alone. The correct conclusion is underdetermination, not a defect in the definition of phase.

| Computational task | Intrinsic operation on phase numbers | Potentially misleading angle-only operation |
| --- | --- | --- |
| Compare two phases | $u\bar v$ | Subtract unwrapped angles without a convention |
| Average phases | Normalize $\sum_k u_k$ | Arithmetic mean of principal arguments |
| Accumulate transport | Multiply incremental factors | Add angles while silently crossing a cut |
| Detect circulation | $(2\pi i)^{-1}\oint u^{-1}du$ | Compare endpoint principal arguments |
| Apply a phase correction | $u\mapsto cu$, $c\in U(1)$ | Add a scalar angle without modular control |

## 8. Quantum computation and finite-dimensional phase structure

The elementary phase gate on a qubit has the form

\[
P(\varphi)=
\begin{pmatrix}
1&0\\
0&e^{i\varphi}
\end{pmatrix}.
\tag{57}
\]

It acts on a superposition $a|0\rangle+b|1\rangle$ by multiplying one component by a phase number. The effect is relative, because

\[
e^{i\chi}I\cdot P(\varphi)
\tag{58}
\]

has the same action on rays as $P(\varphi)$. Gate equivalence in the projective unitary group therefore removes a common $U(1)$ factor from all matrix entries, while controlled phase operations deliberately preserve relative factors.

For a $d$-level system, the diagonal unitary

\[
D=\operatorname{diag}(e^{i\theta_1},\dots,e^{i\theta_d})
\tag{59}
\]

contains $d$ phase numbers. Multiplication by a global $e^{i\chi}$ sends every $\theta_j$ to $\theta_j+\chi$, so only the $d-1$ independent relative phase classes are physically meaningful for a state vector. This quotient is the finite-dimensional counterpart of the projective-space statement in (31).

The discrete phase subgroup $\mu_N$ of (11) is especially important in digital settings. Its multiplication law corresponds to addition in $\mathbb Z/N\mathbb Z$, and its characters supply the kernel of the discrete Fourier transform:

\[
\omega_N^{jk}=e^{2\pi i jk/N}.
\tag{60}
\]

The complex number $\omega_N$ is a primitive discrete phase number, while $j$ and $k$ label exponentiated characters. The computational distinction between a modular exponent and a selected angle is the finite analogue of the continuous covering-space distinction.

## 9. Beyond scalar phase: non-abelian comparison and limits of the framework

The scalar phase group $U(1)$ is abelian. This makes its connection curvature simply $\mathcal F=d\mathcal A$ and allows all phase factors to commute. In systems with degeneracies, parallel transport may act on a multidimensional subspace, leading to a matrix-valued unitary holonomy in $U(r)$. If

\[
\mathcal A=\mathcal A_\mu dx^\mu
\]

is a $\mathfrak u(r)$-valued connection, then

\[
\mathcal F=d\mathcal A+i\mathcal A\wedge\mathcal A,
\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu+i[A_\mu,A_\nu].
\tag{61}
\]

The additional commutator is absent for a phase number because $\mathfrak u(1)$ is one-dimensional and commutative. Holonomy must then be path ordered:

\[
U_C=\mathcal P\exp\!\left(i\oint_C\mathcal A\right).
\tag{62}
\]

This comparison clarifies the boundary of the present theory. A scalar phase number is the rank-one, abelian case of unitary transport. It retains a privileged status because all local factors commute and because its topology is already nontrivial: even an abelian group supports winding, line bundles, and quantized flux. Matrix holonomies generalize phase factors, but they are not phase numbers in the strict sense adopted here.

## 10. A disciplined calculus of phase numbers

The preceding sections suggest a compact set of methodological rules. They are not merely stylistic preferences; each prevents a specific category error.

| Principle | Correct invariant statement | Common but incomplete shorthand | Consequence |
| --- | --- | --- | --- |
| Separate object from coordinate | $u\in U(1)$ is primary | “The phase is a real number” | Branches are recognized as coordinate choices |
| Separate global from relative phase | $u\bar v$ is observable in interference | “Each amplitude has an observable phase” | Common factors cancel |
| Treat transport multiplicatively | $u_{\rm tot}=\prod_j u_j$ | “Add all angles” | Composition remains branch independent |
| Use periods for topology | $(2\pi i)^{-1}\oint u^{-1}du\in\mathbb Z$ | “The angle returns changed” | Winding is quantized and coordinate free |
| Use holonomy for gauge phase | $\exp(i\oint_C\mathcal A)$ | “The gauge potential gives a phase” | Gauge-dependent potentials are distinguished from observables |
| Use circular statistics for directional data | $\widehat u=(\sum u_k)/|\sum u_k|$ | “Average the angles” | Artificial discontinuities are avoided |

The conceptual hierarchy can be summarized as follows. First, a complex amplitude splits uniquely into magnitude and phase number. Second, the phase number can be locally logarithmized to an angle but cannot generally be logarithmized globally. Third, the obstruction is measured by integral winding. Fourth, when phase numbers glue local frames or accumulate under transport, their global product is holonomy. Finally, measurable phase effects arise only through invariant combinations—relative phases, characters, winding integers, curvature fluxes, or holonomies.

## 11. Conclusion

Phase numbers constitute a small but structurally rich class of objects: the unit complex scalars $U(1)$. Their apparent simplicity can obscure the fact that they carry group structure, compact topology, a universal cover, integral character theory, and a natural role as the structure group of complex line bundles. The most effective analytical stance is to regard $e^{i\theta}$ as fundamental and $\theta$ as a local logarithmic coordinate.

From this stance, several phenomena become instances of one framework. Polar decomposition extracts a phase number from a nonzero amplitude. Fourier analysis uses integral characters of the circle group. Interference observes relative phase numbers. Phase unwrapping constructs a lift under sampling assumptions. Winding measures the failure of a closed lift to close. Gauge theory glues local frames through phase-number transition functions and records transport by holonomy. The Berry factor is a quantum realization of exactly such $U(1)$ holonomy.

The resulting calculus is both conservative and extensible. It preserves the familiar notation of complex analysis and physics, but it replaces branch-dependent prose with globally meaningful statements. It also identifies the correct route to generalization: scalar phase gives way to non-abelian unitary transport only when the relevant subspace has rank greater than one. In the scalar case, the full content of phase is already present in the circle group itself.

## Appendix A. Auxiliary derivations

### A.1 Gauge transformation of the connection

Starting from $\nabla s=i\mathcal A\otimes s$ and $s'=e^{i\chi}s$,

\[
\begin{aligned}
\nabla s'
&=d(e^{i\chi})\otimes s+e^{i\chi}\nabla s\\
&=ie^{i\chi}d\chi\otimes s+ie^{i\chi}\mathcal A\otimes s\\
&=i(\mathcal A+d\chi)\otimes s'.
\end{aligned}
\tag{A.1}
\]

Hence $\mathcal A'=\mathcal A+d\chi$. Applying $d$ gives $\mathcal F'=d\mathcal A'=d\mathcal A=\mathcal F$.

### A.2 Gauge invariance of Berry holonomy

For $|n'\rangle=e^{i\chi}|n\rangle$,

\[
\begin{aligned}
\mathcal A'_n
&=i\langle n'|dn'\rangle\\
&=i\langle n|e^{-i\chi}d(e^{i\chi}|n\rangle)\\
&=i\langle n|(i\,d\chi|n\rangle+d|n\rangle)\\
&=\mathcal A_n-d\chi.
\end{aligned}
\tag{A.2}
\]

For a closed loop, $\oint_Cd\chi=2\pi k$ may arise when comparing gauges with nontrivial patching, but the phase number is unchanged:

\[
\exp\!\left(i\oint_C\mathcal A'_n\right)
=
\exp\!\left(i\oint_C\mathcal A_n\right)e^{-i2\pi k}
=
\exp\!\left(i\oint_C\mathcal A_n\right).
\tag{A.3}
\]

### A.3 Logarithmic derivative of a complex amplitude

Let $z(t)=r(t)e^{i\theta(t)}$ with $r(t)>0$. Then

\[
\frac{\dot z}{z}
=\frac{\dot r}{r}+i\dot\theta.
\tag{A.4}
\]

Taking real and imaginary parts gives

\[
\frac{d}{dt}\log|z|=\operatorname{Re}\!\left(\frac{\dot z}{z}\right),
\qquad
\dot\theta=\operatorname{Im}\!\left(\frac{\dot z}{z}\right).
\tag{A.5}
\]

Equation (A.5) is valid locally on intervals avoiding $z=0$. Around a closed loop, its integral produces the winding formula:

\[
\frac{1}{2\pi}\int_0^T\operatorname{Im}\!\left(\frac{\dot z}{z}\right)dt
=\frac{1}{2\pi i}\oint\frac{dz}{z}\in\mathbb Z.
\tag{A.6}
\]

## References

[1] E. W. Weisstein, “Complex Number,” *Wolfram MathWorld*. The source defines the complex field, modulus, argument/phase, and polar representation used in Section 2. [https://mathworld.wolfram.com/ComplexNumber.html](https://mathworld.wolfram.com/ComplexNumber.html)

[2] A. Hatcher, *Algebraic Topology*, Cambridge University Press, 2002. See the author-hosted text for covering spaces and fundamental-group methods used in Section 3. [https://pi.math.cornell.edu/~hatcher/AT/AT.pdf](https://pi.math.cornell.edu/~hatcher/AT/AT.pdf)

[3] M. V. Berry, “Quantal phase factors accompanying adiabatic changes,” *Proceedings of the Royal Society A* **392** (1802), 45–57 (1984). [https://doi.org/10.1098/rspa.1984.0023](https://doi.org/10.1098/rspa.1984.0023)

[4] B. Simon, “Holonomy, the quantum adiabatic theorem, and Berry’s phase,” *Physical Review Letters* **51**, 2167–2170 (1983). [https://doi.org/10.1103/PhysRevLett.51.2167](https://doi.org/10.1103/PhysRevLett.51.2167)

[5] J. J. Sakurai and J. Napolitano, *Modern Quantum Mechanics*, 3rd ed., Cambridge University Press, 2021. [https://www.cambridge.org/highereducation/books/modern-quantum-mechanics/36B2AA24E70E6C892BFC7870C71AF1F1](https://www.cambridge.org/highereducation/books/modern-quantum-mechanics/36B2AA24E70E6C892BFC7870C71AF1F1)

[6] B. C. Hall, *Lie Groups, Lie Algebras, and Representations: An Elementary Introduction*, 2nd ed., Springer, 2015. [https://doi.org/10.1007/978-3-319-13467-3](https://doi.org/10.1007/978-3-319-13467-3)

[7] G. B. Folland, *A Course in Abstract Harmonic Analysis*, 2nd ed., CRC Press, 2016. [https://doi.org/10.1201/9781315272153](https://doi.org/10.1201/9781315272153)

[8] J. W. Milnor and J. D. Stasheff, *Characteristic Classes*, Princeton University Press, 1974. [https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes)

[9] K. V. Mardia and P. E. Jupp, *Directional Statistics*, Wiley, 1999. [https://doi.org/10.1002/9780470316979](https://doi.org/10.1002/9780470316979)

[10] M. Nakahara, *Geometry, Topology and Physics*, 2nd ed., CRC Press, 2003. [https://doi.org/10.1201/9780367808379](https://doi.org/10.1201/9780367808379)

<!-- Markdown reference-style citation links retained for interoperability. -->
[1]: https://mathworld.wolfram.com/ComplexNumber.html "Wolfram MathWorld: Complex Number"
[2]: https://pi.math.cornell.edu/~hatcher/AT/AT.pdf "Hatcher, Algebraic Topology"
[3]: https://doi.org/10.1098/rspa.1984.0023 "Berry (1984)"
[4]: https://doi.org/10.1103/PhysRevLett.51.2167 "Simon (1983)"
[5]: https://www.cambridge.org/highereducation/books/modern-quantum-mechanics/36B2AA24E70E6C892BFC7870C71AF1F1 "Sakurai and Napolitano"
[6]: https://doi.org/10.1007/978-3-319-13467-3 "Hall, Lie Groups"
[7]: https://doi.org/10.1201/9781315272153 "Folland, Abstract Harmonic Analysis"
[8]: https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes "Milnor and Stasheff"
[9]: https://doi.org/10.1002/9780470316979 "Mardia and Jupp"
[10]: https://doi.org/10.1201/9780367808379 "Nakahara"

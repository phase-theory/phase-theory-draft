# Invariant Theory: The Measurable Content of Relativity Mechanics

## Abstract

Invariant Theory is the second derived theory of Relativity Mechanics. It answers the primitive epistemic and operational question:

\[
\boxed{\text{What can be measured?}}
\]

Within Relativity Mechanics, the answer is:

\[
\boxed{
f(g\cdot\omega)=f(\omega).
}
\]

Only functions, quantities, probabilities, and records that are constant on admissibility orbits possess observer-independent physical meaning.

Orbit Theory establishes that a physical object is an orbit

\[
[\omega]=G\cdot\omega.
\]

Invariant Theory establishes what may be said about that object. A physical observable is not an arbitrary function on the description space \(\Omega\). It is a function on the quotient space \(\Omega/G\), or equivalently a \(G\)-invariant function on \(\Omega\). The algebra of physical observables is therefore

\[
\mathcal O_{\rm phys}
=
C^\infty(\Omega)^G
\cong
C^\infty(\Omega/G),
\]

with suitable generalizations to singular quotients, quantum operator algebras, and BRST cohomology.

This paper develops Invariant Theory as the formal theory of physical measurability. We define invariant functions, infinitesimal invariance, invariant algebras, separating invariant systems, relational observables, tensorial invariants, gauge-invariant functionals, quantum invariant operators, and measurement maps. We show that covariance alone is not sufficient for direct measurability; covariant structures become physically meaningful only when organized into invariant compounds or relational completions. Invariant Theory therefore provides the boundary condition for empirical content in Relativity Mechanics: whatever is not invariant under admissible re-description is not an observer-independent physical fact.

---

## 1. Introduction

Relativity Mechanics begins with the recognition that physical descriptions contain both physical content and descriptive redundancy. Coordinates, frames, bases, gauges, parametrizations, and reference conventions are part of the presentation of a system, but they are not themselves physical facts.

Orbit Theory identifies the physical object with the equivalence class of admissible descriptions:

\[
[\omega]=G\cdot\omega.
\]

Once this ontology is accepted, the next question is unavoidable:

\[
\boxed{
\text{What can be measured about such an object?}
}
\]

The answer must be expressed in terms of the orbit structure. A measurable quantity cannot depend on which representative \(\omega\) of the orbit is used. If it did, then the quantity would distinguish between descriptions of the same object and would therefore fail to be a property of the object itself.

Thus a measurable function \(f\) must satisfy

\[
\boxed{
f(g\cdot\omega)=f(\omega)
}
\]

for every admissibility transformation \(g\in G\).

This is the central principle of Invariant Theory:

\[
\boxed{
\text{Only invariants possess observer-independent meaning.}
}
\]

Everything that can be measured, recorded, predicted, or operationally verified must be expressible as an invariant of the admissibility action.

---

## 2. The Relativity Schema and the Role of Invariant Theory

A Relativity Mechanics theory is specified by

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

where:

- \(\Omega\) is the description space,
- \(G\) is the admissibility group,
- \(\triangleright:G\times\Omega\to\Omega\) is the action,
- \(I:\Omega\to\Omega/G\) is the invariant projection.

We write

\[
g\cdot\omega:=g\triangleright\omega.
\]

The orbit of \(\omega\) is

\[
[\omega]=G\cdot\omega.
\]

The quotient space is

\[
\Omega/G.
\]

Orbit Theory supplies the ontology:

\[
\text{Physical object} = [\omega].
\]

Invariant Theory supplies the measurable content:

\[
\text{Physical observable} = \text{function on }[\omega].
\]

Equivalently,

\[
\text{Physical observable}
=
\text{\(G\)-invariant function on }\Omega.
\]

Thus Invariant Theory is the theory of physical predication. It determines which functions on descriptions descend to functions on objects.

---

## 3. Axioms of Invariant Theory

Invariant Theory is governed by the following axioms.

### Axiom I: Measurability requires orbit constancy

A function \(f:\Omega\to\mathbb R\) is physically measurable only if it is constant on every admissibility orbit:

\[
f(g\cdot\omega)=f(\omega),
\qquad
\forall g\in G,\ \omega\in\Omega.
\]

### Axiom II: Observables form an invariant algebra

The set of physical observables is

\[
\mathcal O_{\rm phys}
=
C^\infty(\Omega)^G.
\]

This algebra is closed under pointwise addition, multiplication, scalar multiplication, and, where applicable, Poisson brackets or quantum commutators.

### Axiom III: Measurement outcomes are invariant facts

A measurement record is physically meaningful only if it is invariant under all admissible re-descriptions of the measured system and the measuring apparatus.

### Axiom IV: Covariant quantities are not directly observable

Tensorial, spinorial, or gauge-covariant quantities may enter the construction of observables, but they are not themselves observer-independent observables unless they are combined into invariant structures or relational completions.

### Axiom V: Empirical content is determined by the invariant algebra

The empirical content of a theory is determined by its invariant algebra, not by its redundant description space.

---

## 4. Invariant Functions and Descent to the Quotient

The fundamental theorem of Invariant Theory is simple but decisive.

### Theorem 4.1: Descent theorem

A function

\[
f:\Omega\to\mathbb R
\]

descends to a well-defined function

\[
\bar f:\Omega/G\to\mathbb R
\]

such that

\[
f=\bar f\circ I
\]

if and only if

\[
f(g\cdot\omega)=f(\omega)
\]

for all \(g\in G\), \(\omega\in\Omega\).

Moreover, if such \(\bar f\) exists, it is unique.

### Proof

Suppose first that \(f=\bar f\circ I\). Then

\[
f(g\cdot\omega)
=
\bar f(I(g\cdot\omega))
=
\bar f([\omega])
=
\bar f(I(\omega))
=
f(\omega).
\]

Thus \(f\) is invariant.

Conversely, suppose \(f\) is invariant. Define

\[
\bar f([\omega]) := f(\omega).
\]

We must check that this definition is independent of the representative. If

\[
\omega'=g\cdot\omega,
\]

then

\[
f(\omega')=f(g\cdot\omega)=f(\omega),
\]

so \(\bar f([\omega'])=\bar f([\omega])\). Hence \(\bar f\) is well defined. By construction,

\[
(\bar f\circ I)(\omega)
=
\bar f([\omega])
=
f(\omega).
\]

Uniqueness follows because \(I\) is surjective. If \(\bar f_1\circ I=\bar f_2\circ I\), then for every orbit \([\omega]\) there exists \(\omega\in\Omega\) with \(I(\omega)=[\omega]\), so

\[
\bar f_1([\omega])=\bar f_2([\omega]).
\]

Thus \(\bar f_1=\bar f_2\).

\(\square\)

This theorem identifies the observable algebra:

\[
\boxed{
\mathcal O_{\rm phys}
=
C^\infty(\Omega)^G
\cong
C^\infty(\Omega/G).
}
\]

In singular or quantum settings, this algebra may be replaced by an invariant ring, a \(C^*\)-algebra, a von Neumann algebra, or a BRST cohomology algebra, but the principle remains unchanged.

---

## 5. Infinitesimal Invariance

When \(G\) is a Lie group and \(\Omega\) is smooth, invariance may be expressed infinitesimally.

Let

\[
\mathfrak g=\operatorname{Lie}(G).
\]

For each \(\xi\in\mathfrak g\), define the fundamental vector field

\[
\xi_\Omega(\omega)
=
\left.\frac{d}{dt}\right|_{t=0}
\exp(t\xi)\cdot\omega.
\]

A smooth function \(f\) is invariant under the connected component of \(G\) if and only if

\[
\boxed{
\xi_\Omega(f)=0
}
\]

for all \(\xi\in\mathfrak g\).

Equivalently,

\[
\mathcal L_{\xi_\Omega}f=0.
\]

### Proof sketch

If \(f\) is invariant, then

\[
f(\exp(t\xi)\cdot\omega)=f(\omega)
\]

for all \(t\). Differentiating at \(t=0\) gives

\[
\xi_\Omega(f)(\omega)=0.
\]

Conversely, if \(\xi_\Omega(f)=0\) for all \(\xi\), then \(f\) is constant along all infinitesimal group directions. If \(G\) is connected, integration along one-parameter subgroups implies that \(f\) is constant along each orbit.

If \(G\) has disconnected components, one must also impose invariance under the discrete components.

---

## 6. The Algebra of Physical Observables

The invariant functions form an algebra. If

\[
f,h\in C^\infty(\Omega)^G,
\]

then

\[
(f+h)(g\cdot\omega)=f(g\cdot\omega)+h(g\cdot\omega)
=f(\omega)+h(\omega)
=(f+h)(\omega),
\]

and

\[
(fh)(g\cdot\omega)=f(g\cdot\omega)h(g\cdot\omega)
=f(\omega)h(\omega)
=(fh)(\omega).
\]

Thus

\[
C^\infty(\Omega)^G
\]

is a commutative algebra.

If \(\Omega\) is a symplectic phase space and the \(G\)-action preserves the symplectic form, then the invariant functions form a Poisson subalgebra:

\[
f,h\in C^\infty(\Omega)^G
\implies
\{f,h\}\in C^\infty(\Omega)^G.
\]

Indeed, for any \(g\in G\), symplectic equivariance gives

\[
\{f,h\}\circ g
=
\{f\circ g,h\circ g\}
=
\{f,h\}.
\]

In quantum theory, the corresponding structure is a noncommutative invariant algebra. If \(\mathcal A\) is an operator algebra and \(G\) acts by automorphisms \(\alpha_g\), then

\[
\mathcal A_{\rm phys}
=
\mathcal A^G
=
\{A\in\mathcal A\mid \alpha_g(A)=A,\ \forall g\in G\}.
\]

Thus the invariant algebra is the universal algebra of measurable physical content.

---

## 7. Constructing Invariants

Invariant Theory is not merely a restriction. It provides constructive methods for generating observables.

### 7.1 Averaging over compact groups

If \(G\) is compact, let \(dg\) be normalized Haar measure. Define the Reynolds operator

\[
\mathcal R_G:C^\infty(\Omega)\to C^\infty(\Omega)
\]

by

\[
\mathcal R_G(f)(\omega)
=
\int_G f(g\cdot\omega)\,dg.
\]

Then \(\mathcal R_G(f)\) is invariant.

For \(h\in G\),

\[
\mathcal R_G(f)(h\cdot\omega)
=
\int_G f(gh\cdot\omega)\,dg.
\]

By invariance of Haar measure, the change of variables \(g'=gh\) gives

\[
\mathcal R_G(f)(h\cdot\omega)
=
\int_G f(g'\cdot\omega)\,dg'
=
\mathcal R_G(f)(\omega).
\]

Moreover, if \(f\) is already invariant, then

\[
\mathcal R_G(f)(\omega)
=
\int_G f(\omega)\,dg
=
f(\omega).
\]

Thus \(\mathcal R_G\) is a projection onto the invariant subalgebra:

\[
\mathcal R_G^2=\mathcal R_G.
\]

This is one of the most important constructive tools in classical invariant theory.

---

### 7.2 Tensor contraction

In geometric theories, tensor fields often transform covariantly rather than invariantly. Scalar contractions of tensors yield diffeomorphism-invariant observables.

For example, let \(g_{\mu\nu}\) be a metric and \(R_{\mu\nu\rho\sigma}\) its Riemann curvature. The following are scalar invariants:

\[
R=g^{\mu\nu}R_{\mu\nu},
\]

\[
R_{\mu\nu}R^{\mu\nu},
\]

\[
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma},
\]

\[
{}^\ast RR
=
\frac12
\epsilon^{\mu\nu\rho\sigma}
R_{\mu\nu}{}^{ab}
R_{\rho\sigma ab}.
\]

Such scalars are invariant under diffeomorphisms because they are coordinate-independent contractions of tensorial geometry.

Similarly, in gauge theory, if

\[
F_{\mu\nu}
\]

is the curvature of a connection, then

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu})
\]

is gauge invariant because under a gauge transformation \(u\),

\[
F_{\mu\nu}\mapsto uF_{\mu\nu}u^{-1},
\]

and the trace is cyclic:

\[
\operatorname{tr}(uF_{\mu\nu}u^{-1}uF^{\mu\nu}u^{-1})
=
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}).
\]

Tensorial covariance is therefore not itself measurement; measurement arises when covariant structures are contracted, traced, integrated, or relationally completed into invariants.

---

### 7.3 Integration over invariantly defined domains

If \(F\) is a scalar density, then

\[
\int_M F
\]

is diffeomorphism invariant, provided the integration domain is the entire manifold or is itself defined invariantly.

If a region is specified by coordinate inequalities alone, the integral is generally not diffeomorphism invariant. The region must be defined by physical fields.

For scalar fields \(T^A\), one may define

\[
\mathcal O_F(D)
=
\int_M \chi_D(T(x)) F(x)\,\sqrt{-g}\,d^4x,
\]

where \(\chi_D\) is the characteristic function of a domain \(D\) in the space of \(T^A\)-values. This is invariant because both \(T\) and \(F\) transform as scalars.

Thus relational localization is essential for local or quasi-local observables in generally covariant theories.

---

### 7.4 Holonomies and Wilson loops

In gauge theory, a central class of nonlocal invariants is given by Wilson loops.

Let \(A\) be a connection on a principal bundle and let \(C\) be a closed loop. The holonomy of \(A\) around \(C\) is

\[
\operatorname{Hol}_C(A)
=
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

Under a gauge transformation \(u\), the holonomy transforms by conjugation:

\[
\operatorname{Hol}_C(A)
\mapsto
u(x_0)
\operatorname{Hol}_C(A)
u(x_0)^{-1},
\]

where \(x_0\) is the base point of the loop. The trace in a representation \(R\),

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right),
\]

is gauge invariant:

\[
W_R(C)\mapsto W_R(C).
\]

Wilson loops are therefore fundamental gauge-invariant observables.

In background-independent theories, the loop \(C\) itself must also be specified relationally, not by background coordinates.

---

### 7.5 Spectral invariants

Another powerful class of invariants arises from spectra of operators.

If \(L\) is an operator naturally associated with the description \(\omega\), and if \(L\) transforms covariantly under \(G\), then its spectrum is often invariant.

Examples include:

- eigenvalues of a density matrix \(\rho\),
- Casimir eigenvalues of symmetry representations,
- spectra of Laplace-type operators on compact geometries,
- monodromy eigenvalues in integrable systems,
- modular invariants in conformal field theory.

Spectral invariants are especially important in quantum theory, where measurement outcomes are eigenvalues of invariant operators.

---

## 8. Complete and Separating Invariants

A central task of Invariant Theory is to determine whether a set of invariants completely characterizes physical orbits.

Let

\[
\mathcal S\subset C^\infty(\Omega)^G
\]

be a set of invariant functions. We say that \(\mathcal S\) separates orbits if

\[
f(\omega)=f(\omega')
\quad
\forall f\in\mathcal S
\]

implies

\[
[\omega]=[\omega'].
\]

In singular or non-Hausdorff settings, one may only be able to separate orbit closures or generic strata.

A complete invariant system is a set of invariants from which every other invariant can be generated, at least locally or algebraically.

For compact group actions on reasonable spaces, invariant continuous functions often separate closed orbits. For reductive algebraic group actions on affine varieties, invariant polynomials provide a powerful algebraic classification.

In physical terms:

\[
\boxed{
\text{A complete invariant system gives a complete measurement-theoretic description of the object.}
}
\]

However, completeness is often difficult to achieve. In general relativity, curvature scalars and their covariant derivatives classify generic local geometries only up to subtle equivalence problems. In gauge theory, Wilson loops may generate the gauge-invariant algebra, but global and topological subtleties remain. In quantum theory, complete invariant descriptions may require superselection data, representation labels, and spectral information.

Invariant Theory therefore distinguishes sharply between:

1. local invariants,
2. global invariants,
3. relational invariants,
4. spectral invariants,
5. topological invariants.

A physically complete observable algebra may require several of these classes simultaneously.

---

## 9. Measurement in Invariant Theory

Invariant Theory provides the formal condition for measurement.

A measurement is a physical process that produces an outcome. Let \(Y\) be the outcome space. A classical deterministic measurement is a map

\[
M:\Omega\to Y.
\]

For the measurement result to be observer-independent, \(M\) must be invariant:

\[
M(g\cdot\omega)=M(\omega).
\]

If \(Y\) carries a nontrivial admissibility action, then the measurement may be equivariant:

\[
M(g\cdot\omega)=g\cdot M(\omega).
\]

But if the outcome is to be a physical fact independent of the descriptive frame, then the final record must be invariant or relationally completed.

Thus measurement is not the reading of a raw coordinate. It is the evaluation of an invariant.

### 9.1 Records

A physical record is a stable invariant. If an apparatus produces a value \(y\), then the total system-apparatus description \(\omega\) must satisfy

\[
y(\omega)=y(g\cdot\omega).
\]

Otherwise, the record would depend on the descriptive frame and would not qualify as an objective fact.

### 9.2 Measurement and Orbit Theory

Since the object is an orbit, a measurement is really a map

\[
\bar M:\Omega/G\to Y.
\]

The apparent measurement map \(M:\Omega\to Y\) is only its pullback:

\[
M=\bar M\circ I.
\]

Thus the apparatus may interact with a representative description, but the physical content of the outcome is a function of the orbit.

---

## 10. Covariance Is Not Direct Measurability

A persistent source of confusion in theoretical physics is the conflation of covariance with observability.

A tensor equation such as

\[
G_{\mu\nu}=8\pi G T_{\mu\nu}
\]

is covariant. Its form is preserved under diffeomorphisms. But the individual coordinate components

\[
G_{\mu\nu}(x)
\]

are not themselves diffeomorphism-invariant observables.

Similarly, in gauge theory,

\[
F_{\mu\nu}^a(x)
\]

is gauge-covariant, but the component field at a coordinate point is not gauge-invariant.

Covariant structures are essential. They encode how descriptions transform. But measurement requires invariant extraction.

For example, the metric components \(g_{\mu\nu}(x)\) are not directly observable. However, the proper time along a physical worldline \(\gamma\),

\[
\Delta\tau
=
\int_\gamma \sqrt{-g_{\mu\nu}dx^\mu dx^\nu},
\]

is invariant if \(\gamma\) is physically specified.

Likewise, the electromagnetic potential \(A_\mu\) is not gauge-invariant, but the Aharonov–Bohm phase

\[
\exp\left(iq\oint_C A\right)
\]

is gauge invariant for a closed loop \(C\).

Thus:

\[
\boxed{
\text{Covariance organizes descriptions; invariance constitutes measurement.}
}
\]

---

## 11. Invariant Theory in Newtonian Mechanics

Consider \(N\) Newtonian particles with trajectories

\[
\mathbf x_i(t).
\]

The Galilei group acts by

\[
t'=t+s,
\]

\[
\mathbf x_i'=R\mathbf x_i+\mathbf v t+\mathbf a.
\]

The invariant physical content consists of relative quantities:

\[
\mathbf r_{ij}
=
\mathbf x_i-\mathbf x_j,
\]

\[
\dot{\mathbf r}_{ij}
=
\dot{\mathbf x}_i-\dot{\mathbf x}_j,
\]

\[
\ddot{\mathbf r}_{ij}
=
\ddot{\mathbf x}_i-\ddot{\mathbf x}_j.
\]

The distances

\[
|\mathbf r_{ij}|
\]

are invariant under rotations and translations. Relative velocities are invariant under translations and boosts. Relative accelerations are invariant under the full Galilei group for inertial frames.

Mass ratios are also invariant. Time intervals

\[
\Delta t=t_2-t_1
\]

are invariant in Newtonian physics.

By contrast, absolute position, absolute orientation, absolute uniform velocity, and absolute time origin are not invariant and therefore are not physically measurable within the Galilean admissibility schema.

This example already illustrates the central lesson: what a theory permits one to measure is determined by its admissibility group.

---

## 12. Invariant Theory in Special Relativity

In special relativity, the admissibility group of inertial frames is the Poincaré group

\[
ISO(1,3).
\]

Invariant quantities include spacetime intervals,

\[
ds^2
=
\eta_{\mu\nu}dx^\mu dx^\nu,
\]

proper times,

\[
\Delta\tau^2
=
-\eta_{\mu\nu}\Delta x^\mu\Delta x^\nu,
\]

and scalar products of four-vectors,

\[
p_\mu p^\mu.
\]

For a free particle, the mass is the invariant

\[
m^2=-p_\mu p^\mu.
\]

The Pauli–Lubanski vector is

\[
W^\mu
=
\frac12\epsilon^{\mu\nu\rho\sigma}
P_\nu M_{\rho\sigma}.
\]

The spin invariant is

\[
W_\mu W^\mu.
\]

Thus particle identity in relativistic physics is largely encoded in Poincaré invariants.

---

## 13. Invariant Theory in General Relativity

General relativity provides the deepest classical example of Invariant Theory.

Let

\[
\Omega_{\rm GR}
=
\{g_{\mu\nu},\psi\}
\]

be the space of metrics and matter fields on a manifold \(M\). The admissibility group is

\[
G_{\rm GR}
=
\operatorname{Diff}(M).
\]

A diffeomorphism \(\phi\in\operatorname{Diff}(M)\) acts by pullback:

\[
g_{\mu\nu}\mapsto \phi^*g_{\mu\nu},
\]

\[
\psi\mapsto \phi^*\psi.
\]

Infinitesimally,

\[
\delta_\xi g_{\mu\nu}
=
\mathcal L_\xi g_{\mu\nu}
=
\nabla_\mu\xi_\nu+\nabla_\nu\xi_\mu.
\]

A scalar function \(S[g,\psi]\) is diffeomorphism-invariant if

\[
S[\phi^*g,\phi^*\psi]=S[g,\psi].
\]

Examples include curvature scalars:

\[
R,
\]

\[
R_{\mu\nu}R^{\mu\nu},
\]

\[
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}.
\]

The Kretschmann scalar,

\[
K=R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma},
\]

is a standard local invariant.

However, local scalar invariants are generally insufficient to capture the full physical content of a spacetime geometry. One also needs relational observables.

Let \(T^A\), \(A=0,1,2,3\), be scalar fields that serve as physical reference coordinates. Let \(\phi\) be another scalar field. Define

\[
\mathcal O_\phi(\tau)
=
\phi(p),
\]

where \(p\) is the unique point satisfying

\[
T^A(p)=\tau^A.
\]

Under a diffeomorphism, both \(T^A\) and \(\phi\) are pulled back, and the point \(p\) is mapped to \(\phi(p)\), but the value \(\phi(p)\) is unchanged. Therefore

\[
\mathcal O_\phi(\tau)
\]

is diffeomorphism invariant.

More generally, for a scalar density \(F\), one may define

\[
\mathcal O_F(D)
=
\int_M \chi_D(T(x))F(x)\,\sqrt{-g}\,d^4x.
\]

This is an invariant integral over a physically defined region.

Thus in general relativity, measurable observables are generally relational and often nonlocal.

---

## 14. Invariant Theory in Gauge Theories

Let \(P\to M\) be a principal \(H\)-bundle. Let

\[
\mathcal A
\]

be the space of connections. The gauge group

\[
\mathcal G=\operatorname{Aut}(P)
\]

acts on \(\mathcal A\).

A connection \(A\) transforms as

\[
A\mapsto A^u
=
uAu^{-1}
-
(du)u^{-1}.
\]

Its curvature is

\[
F=dA+\frac12[A,A],
\]

and transforms covariantly:

\[
F\mapsto uFu^{-1}.
\]

Local gauge-invariant observables can be formed by traces:

\[
\operatorname{tr}(F\wedge *F),
\]

\[
\operatorname{tr}(F\wedge F),
\]

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}).
\]

Nonlocal gauge-invariant observables include Wilson loops:

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

Matter fields \(\psi\) transform in representations of \(H\). Gauge-invariant matter observables are formed by contracting representation indices. For example, in a theory with fundamental fields \(q\) and antifundamental fields \(\bar q\),

\[
\bar q q
\]

may be gauge invariant, while \(q\) alone is not.

In Hamiltonian gauge theory, physical observables must commute with the Gauss constraints:

\[
\{O,\mathcal G^a(x)\}=0.
\]

In quantum gauge theory,

\[
[\hat O,\hat{\mathcal G}^a(x)]=0.
\]

Thus gauge invariance is the condition of measurability for internal admissibility symmetries.

---

## 15. Invariant Theory in Quantum Mechanics

In quantum theory, descriptions are vectors, rays, density matrices, or operator algebra states.

Let \(\mathcal H\) be a Hilbert space. A pure state vector \(|\psi\rangle\) is physically equivalent to

\[
e^{i\theta}|\psi\rangle.
\]

The admissibility group is \(U(1)\). The physical state is the ray

\[
[\psi]\in\mathbb P(\mathcal H).
\]

An expectation value

\[
\langle A\rangle_\psi
=
\frac{\langle\psi|A|\psi\rangle}{\langle\psi|\psi\rangle}
\]

is invariant under global phase:

\[
\langle A\rangle_{e^{i\theta}\psi}
=
\langle A\rangle_\psi.
\]

If a unitary basis change \(U\) is regarded as a change of description, then

\[
|\psi\rangle\mapsto U|\psi\rangle,
\]

\[
A\mapsto UAU^\dagger,
\]

and the expectation value remains invariant:

\[
\langle\psi|U^\dagger UAU^\dagger U|\psi\rangle
=
\langle\psi|A|\psi\rangle.
\]

Thus quantum measurement outcomes are invariant structures.

For mixed states, a density matrix \(\rho\) transforms under basis changes as

\[
\rho\mapsto U\rho U^\dagger.
\]

Invariant quantities include:

\[
\operatorname{Tr}(\rho A),
\]

\[
\operatorname{Tr}(\rho^n),
\]

\[
S(\rho)=-\operatorname{Tr}(\rho\log\rho),
\]

and the eigenvalues of \(\rho\).

Born probabilities,

\[
p(a)=\operatorname{Tr}(\rho P_a),
\]

are invariant when \(P_a\) and \(\rho\) transform consistently.

Thus quantum mechanics is already an invariant theory: measurable probabilities and expectation values are invariant under admissibility transformations.

---

## 16. Quantum Invariant Algebras

Let \(\mathcal A\) be the algebra of quantum observables. Suppose \(G\) acts by automorphisms

\[
\alpha_g:\mathcal A\to\mathcal A.
\]

The physical observable algebra is

\[
\mathcal A_{\rm phys}
=
\mathcal A^G
=
\{A\in\mathcal A\mid \alpha_g(A)=A,\ \forall g\in G\}.
\]

If the action is implemented unitarily on a Hilbert space,

\[
\alpha_g(A)=U(g)AU(g)^\dagger,
\]

then

\[
\mathcal A_{\rm phys}
=
\{A\mid U(g)AU(g)^\dagger=A,\ \forall g\in G\}.
\]

Equivalently,

\[
[A,U(g)]=0.
\]

For infinitesimal generators \(\hat Q_\xi\), this becomes

\[
[A,\hat Q_\xi]=0.
\]

In constrained quantum systems, the constraints \(\hat C_a\) generate admissibility transformations. Physical observables satisfy

\[
[\hat O,\hat C_a]=0,
\]

possibly weakly on the physical subspace.

In BRST quantization, physical observables are BRST-closed modulo BRST-exact operators:

\[
[Q_{\rm BRST},O\}=0,
\]

\[
O\sim O+[Q_{\rm BRST},\Lambda\}.
\]

Thus the quantum observable algebra is the invariant cohomology of the admissibility action.

---

## 17. Invariant Measurements in Quantum Theory

A quantum measurement with outcome space \(Y\) may be described by a positive operator-valued measure (POVM)

\[
E(\Delta),
\qquad
\Delta\subset Y.
\]

The probability of obtaining an outcome in \(\Delta\) when the system is in state \(\rho\) is

\[
p(\Delta|\rho)
=
\operatorname{Tr}(\rho E(\Delta)).
\]

If the outcome label is observer-independent, then the POVM must be invariant:

\[
U(g)E(\Delta)U(g)^\dagger=E(\Delta).
\]

Then for a transformed state

\[
\rho\mapsto U(g)\rho U(g)^\dagger,
\]

the probability is unchanged:

\[
\operatorname{Tr}(U(g)\rho U(g)^\dagger E(\Delta))
=
\operatorname{Tr}(\rho U(g)^\dagger E(\Delta)U(g))
=
\operatorname{Tr}(\rho E(\Delta)).
\]

If the outcome space itself transforms under \(G\), then one uses covariant POVMs:

\[
U(g)E(\Delta)U(g)^\dagger=E(g\Delta).
\]

In that case, the full measurement record includes the frame or observer variable, and the invariant fact is the relational correlation between system and reference.

Thus quantum measurement theory fits naturally into Invariant Theory.

---

## 18. Invariants, Conservation Laws, and Casimirs

Invariant Theory is related to, but distinct from, Noether theory.

Noether charges arise from continuous symmetries of the action. However, the individual components of a moment map

\[
\mu:\Omega\to\mathfrak g^*
\]

are not necessarily invariant. They often transform coadjointly:

\[
\mu(g\cdot\omega)=\operatorname{Ad}^*_g\mu(\omega).
\]

Invariant quantities are obtained by taking invariant functions on \(\mathfrak g^*\). For example, for the Poincaré group,

\[
P_\mu P^\mu
\]

and

\[
W_\mu W^\mu
\]

are invariant Casimir functions.

In gauge theories, the Gauss constraints generate gauge transformations. The individual gauge generators are not physical observables; physical observables must be invariant under them.

Thus:

\[
\boxed{
\text{Noether charges generate transformations; invariants are what can be measured.}
}
\]

Some conserved quantities are invariant, especially Casimirs, but conservation alone does not guarantee invariance under the full admissibility group.

---

## 19. Partial Observables and Relational Completion

In many physical situations, one encounters quantities that are not invariant by themselves but become meaningful when combined with other quantities.

For example, the value of a field at a coordinate point,

\[
\phi(x),
\]

is not diffeomorphism-invariant. But the value of \(\phi\) when a clock field \(T\) reads \(\tau\),

\[
\phi|_{T=\tau},
\]

is invariant.

Similarly, a gauge-dependent matter field \(\psi(x)\) may be made gauge-invariant by attaching a Wilson line to a physical reference point or to another charged field.

This process is called relational completion or dressing.

Formally, one starts with a partial observable \(f\) that is not invariant. One then introduces reference fields \(T^A\) and defines a complete observable

\[
O_{f,T}(\tau)
=
f\big|_{T=\tau}.
\]

The complete observable is invariant if the reference fields transform consistently with \(f\).

Thus Invariant Theory does not deny the usefulness of non-invariant quantities. It explains how they become physical through invariant completion.

---

## 20. Local, Nonlocal, and Relational Invariants

Invariant Theory distinguishes several classes of observables.

### 20.1 Local invariants

Local invariants are built at a point from tensorial or algebraic contractions. Examples include

\[
R,
\qquad
F_{\mu\nu}F^{\mu\nu},
\qquad
\bar\psi\psi.
\]

They are simple but often incomplete.

### 20.2 Integrated invariants

Integrated invariants are global quantities such as

\[
\int_M \operatorname{tr}(F\wedge F),
\]

\[
\int_M \sqrt{-g}R,
\]

or total charges defined at infinity.

### 20.3 Nonlocal invariants

Wilson loops and holonomies are nonlocal invariants:

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

### 20.4 Relational invariants

Relational invariants use physical fields to define locations, regions, or clocks:

\[
O_{\phi,T}(\tau)=\phi|_{T=\tau}.
\]

In background-independent theories, relational invariants are often the only genuinely local physical observables.

---

## 21. Invariant Theory and Observer Theory

Invariant Theory gives the formal condition for measurability. Observer Theory determines which invariants are accessible to a given observer.

An observer may be modeled by an observation map

\[
O:\Omega\to D_O,
\]

where \(D_O\) is the observer’s description space.

An observer report is a function

\[
m:D_O\to\mathbb R.
\]

The corresponding physical observable is

\[
m_O(\omega)=m(O(\omega)).
\]

For the report to be physically meaningful,

\[
m_O(g\cdot\omega)=m_O(\omega).
\]

Thus observer reports must themselves be invariant, or must be completed by including the observer’s frame in the total description.

Invariant Theory therefore supplies the criterion, while Observer Theory supplies the operational realization.

---

## 22. Invariant Theory and Information

Although Relativistic Information Theory is a separate derived theory, Invariant Theory already determines what can count as information.

Information is distinguishability. But only invariant distinctions are physical distinctions.

If two descriptions lie on the same orbit, then no invariant measurement can distinguish them. Therefore they carry the same physical information.

If two orbits are separated by some invariant function \(f\), then there exists in principle a measurement capable of distinguishing them:

\[
\exists f\in C^\infty(\Omega)^G
\quad
\text{such that}
\quad
f([\omega])\neq f([\omega']).
\]

Thus the invariant algebra determines the possible information content of a theory.

---

## 23. Invariant Theory and Anomalies

In quantum theory, a classical invariance may fail after quantization. This failure is called an anomaly.

If the quantum measure, operator algebra, or constraint algebra fails to preserve the classical admissibility symmetry, then the would-be invariant observables may not be well defined.

For gauge theories, gauge anomalies are fatal: they destroy the consistency of the quotient by the gauge group. For gravitational anomalies, diffeomorphism invariance is obstructed. For global anomalies, certain large admissibility transformations may fail to be represented consistently.

Invariant Theory therefore acquires a quantum consistency condition:

\[
\boxed{
\text{A quantum theory is admissible only if its physical invariant algebra is anomaly-free.}
}
\]

Anomaly cancellation is not an optional technicality. It is the condition that the quotient ontology of Relativity Mechanics survives quantization.

---

## 24. Invariant Theory and Effective Descriptions

In practical physics, one often works with non-invariant intermediate quantities: coordinates, gauge choices, bases, renormalization schemes, background structures.

This is permissible so long as final physical predictions are invariant.

A gauge-fixed calculation, for example, uses a non-invariant representative \(A\) but must produce invariant expectation values:

\[
\langle W_R(C)\rangle,
\qquad
\langle \operatorname{tr}(F^2)\rangle,
\qquad
S\text{-matrix elements}.
\]

Similarly, a coordinate calculation in general relativity may use \(g_{\mu\nu}(x)\), but observable predictions must be expressible in terms of proper times, redshifts, scattering amplitudes, relational field values, or other invariants.

Thus Invariant Theory does not forbid the use of non-invariant tools. It subordinates them to invariant final results.

---

## 25. Invariant Theory and the Reconstruction of the Quotient

In favorable cases, the invariant algebra determines the quotient space.

If

\[
\mathcal O_{\rm phys}=C^\infty(\Omega)^G
\]

separates orbits, then the orbit space may be reconstructed as the spectrum or maximal ideal space of the invariant algebra.

Schematically,

\[
\Omega/G
\cong
\operatorname{Spec}\bigl(C^\infty(\Omega)^G\bigr).
\]

In algebraic settings,

\[
\Omega//G
\cong
\operatorname{Spec}\bigl(\mathbb C[\Omega]^G\bigr).
\]

This expresses a deep fact: the measurable content of a theory can determine its physical state space.

If the invariant algebra fails to separate orbits, then either the quotient is singular, or additional invariant data — such as stacky stabilizer information, topological sectors, or superselection labels — is required.

---

## 26. Summary of the Invariant Observable Framework

The core structure of Invariant Theory is:

Given

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

a function \(f:\Omega\to\mathbb R\) is physically measurable if and only if

\[
\boxed{
f(g\cdot\omega)=f(\omega).
}
\]

Equivalently, there exists a unique function

\[
\bar f:\Omega/G\to\mathbb R
\]

such that

\[
f=\bar f\circ I.
\]

For a connected Lie group, the infinitesimal condition is

\[
\boxed{
\mathcal L_{\xi_\Omega}f=0,
\qquad
\forall \xi\in\mathfrak g.
}
\]

The physical observable algebra is

\[
\boxed{
\mathcal O_{\rm phys}
=
C^\infty(\Omega)^G.
}
\]

In quantum theory,

\[
\boxed{
\mathcal A_{\rm phys}
=
\mathcal A^G.
}
\]

In constrained systems,

\[
\boxed{
\{O,C_a\}=0
}
\]

or, quantum mechanically,

\[
\boxed{
[\hat O,\hat C_a]=0.
}
\]

In gauge theory, central invariants include

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}),
\]

\[
W_R(C)=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

In general relativity, central invariants include curvature scalars,

\[
R,
\qquad
R_{\mu\nu}R^{\mu\nu},
\qquad
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma},
\]

and relational observables,

\[
O_{\phi,T}(\tau)=\phi|_{T=\tau}.
\]

In quantum mechanics, measurable quantities include expectation values,

\[
\langle A\rangle_\psi
=
\frac{\langle\psi|A|\psi\rangle}{\langle\psi|\psi\rangle},
\]

Born probabilities,

\[
p(a)=\operatorname{Tr}(\rho P_a),
\]

and spectral invariants.

---

## 27. Relation to the Remaining Parts of Relativity Mechanics

Invariant Theory is the second part of the Relativity Mechanics architecture, but it is presupposed by nearly every later part.

- **Orbit Theory** provides the objects: orbits.
- **Invariant Theory** provides the measurable predicates on those objects.
- **Observer Theory** explains how observers access invariants.
- **Reference Transformation Theory** explains how invariant descriptions transform between frameworks.
- **Constraint Mechanics** identifies the constraints whose invariants are physical.
- **Relativistic Dynamics** requires evolution to preserve or consistently act on invariant algebras.
- **Relativistic Information Theory** defines information through invariant distinguishability.
- **Relativistic Quantum Theory** replaces invariant functions with invariant operator algebras.
- **Relativity Geometry** constructs invariant geometric structures on quotients.
- **Gauge Theory of Admissibility** studies local internal invariants.
- **Frame Theory** studies local frame invariants, culminating in gravitational physics.

Thus Invariant Theory is the epistemic bridge between orbit ontology and physical measurement.

---

## 28. Conclusion

Invariant Theory answers the primitive question:

\[
\boxed{
\text{What can be measured?}
}
\]

The answer is:

\[
\boxed{
\text{Only invariants of the admissibility action.}
}
\]

A measurable quantity is not an arbitrary feature of a description. It is a function on the orbit space. It must satisfy

\[
\boxed{
f(g\cdot\omega)=f(\omega).
}
\]

Only such functions possess observer-independent meaning.

Covariant structures are essential for organizing descriptions, but they become measurable only when contracted, traced, integrated, or relationally completed into invariants. Quantum observables are invariant operators. Gauge-invariant functionals are invariant on connection orbits. Diffeomorphism-invariant observables are relational structures on geometry orbits. Measurement records are stable invariants.

Invariant Theory therefore establishes the boundary of empirical content in Relativity Mechanics:

\[
\boxed{
\text{The measurable is the invariant.}
}
\]

Everything else is descriptive structure.

# Gauge Theory of Admissibility: Internal Frame Relativity and the Emergence of Yang–Mills Theory, Electromagnetism, the Weak Interaction, and Quantum Chromodynamics

## Abstract

Gauge Theory of Admissibility is the specialization of Relativity Mechanics obtained by replacing the spacetime frame group \(\mathrm{Spin}(1,3)\) with an arbitrary Lie group \(G\). The description space consists of internal frame presentations, connections, and matter fields. The admissibility group is the local gauge group

\[
\mathcal G = C^\infty(M,G),
\]

acting on connections and matter fields by internal re-framings. Physical configurations are not individual gauge potentials or matter components, but gauge orbits

\[
[A,\psi]=\mathcal G\cdot(A,\psi).
\]

The invariant projection maps a gauge presentation to its orbit:

\[
I:\Omega_{\rm gauge}\to \Omega_{\rm gauge}/\mathcal G.
\]

Within this framework, gauge fields are connections on principal \(G\)-bundles, gauge transformations are changes of internal admissible description, curvature is the invariant field strength, and gauge-invariant observables are the only measurable quantities.

Choosing different internal admissibility groups yields the principal gauge theories of physics:

\[
\begin{aligned}
G=U(1) &\quad\Rightarrow\quad \text{Electromagnetism},\\
G=SU(2) &\quad\Rightarrow\quad \text{Weak isospin gauge theory},\\
G=SU(3) &\quad\Rightarrow\quad \text{Quantum chromodynamics},\\
G=SU(3)\times SU(2)\times U(1) &\quad\Rightarrow\quad \text{Standard Model gauge sector}.
\end{aligned}
\]

Thus Yang–Mills theory is not an independent postulate added to Relativity Mechanics. It is the general theory of local internal admissibility. Electromagnetism, weak interactions, and QCD arise as special choices of the internal admissibility group, the associated representation content, and the invariant dynamics on the quotient space.

The central principle is:

\[
\boxed{
\text{Gauge symmetry is local admissibility.}
}
\]

---

## 1. Introduction

Frame Theory shows that gravitational geometry arises when the admissible descriptions are local spacetime frames and the admissibility group is

\[
\mathrm{Spin}(1,3).
\]

The metric is then the invariant of local frame orbits:

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

Gauge Theory of Admissibility generalizes this construction. Instead of restricting the local frame group to the spin group of spacetime, we allow an arbitrary Lie group \(G\) to act as the internal admissibility group.

The primitive question is:

\[
\boxed{
\text{What if admissible descriptions are internal frame presentations?}
}
\]

The answer is:

\[
\boxed{
\Omega=\{\text{internal frames, connections, matter fields}\},
\qquad
G=\text{arbitrary Lie group}.
}
\]

The resulting structure is gauge theory.

In this framework, a gauge potential \(A_\mu\) is not itself a physical field. It is a connection describing how internal frames are compared from point to point. A gauge transformation is not a physical deformation of the system. It is a change of internal description. The physical field is the gauge orbit. The physical observables are gauge invariants.

This perspective unifies electromagnetism, Yang–Mills theory, weak interactions, and QCD under a single foundational principle.

---

## 2. From Frame Theory to Gauge Theory of Admissibility

In Frame Theory, the relativity schema is

\[
\mathcal R_{\rm FT}
=
(\Omega_{\rm FT},G_{\rm FT},\triangleright,I_{\rm FT}),
\]

with

\[
\Omega_{\rm FT}=\{\text{local spacetime frames}\},
\]

\[
G_{\rm FT}=C^\infty(M,\mathrm{Spin}(1,3)).
\]

The invariant projection produces the metric:

\[
I_{\rm FT}(e)=g,
\qquad
g_{\mu\nu}=\eta_{IJ}e^I_\mu e^J_\nu.
\]

Gauge Theory of Admissibility replaces the structure group \(\mathrm{Spin}(1,3)\) by an arbitrary Lie group \(G\):

\[
\boxed{
\mathrm{Spin}(1,3)
\longrightarrow
G.
}
\]

The new schema is

\[
\boxed{
\mathcal R_{\rm GTA}
=
(\Omega_{\rm gauge},\mathcal G,\triangleright,I_{\rm gauge}),
}
\]

where

\[
\mathcal G=C^\infty(M,G)
\]

is the local gauge admissibility group.

The description space is

\[
\Omega_{\rm gauge}
=
\mathcal A\times\Gamma(E),
\]

where:

- \(\mathcal A\) is the affine space of connections on a principal \(G\)-bundle,
- \(E=P\times_G V\) is an associated matter bundle,
- \(\Gamma(E)\) is the space of matter fields.

The physical configuration space is the quotient

\[
\boxed{
\Omega_{\rm gauge}/\mathcal G
=
(\mathcal A\times\Gamma(E))/\mathcal G.
}
\]

This quotient is the space of gauge orbits.

---

## 3. Internal Frames and Local Admissibility

A gauge theory may be understood as a theory of internal reference frames.

At each spacetime point \(x\in M\), a matter field may be expressed relative to an internal basis. A change of that basis is a gauge transformation. If the internal basis is changed independently at each point, the admissibility group becomes local.

Thus:

\[
\boxed{
\text{A gauge transformation is a local change of internal frame.}
}
\]

The gauge potential \(A_\mu\) is the structure required to compare internal frames at neighboring points. It is the connection of internal admissibility.

This is directly analogous to Frame Theory:

| Frame Theory | Gauge Theory of Admissibility |
|---|---|
| Local spacetime frames | Internal frames |
| \(\mathrm{Spin}(1,3)\) | Arbitrary Lie group \(G\) |
| Spin connection \(\omega^{IJ}\) | Gauge connection \(A\) |
| Torsion and curvature | Curvature \(F\) |
| Metric invariant | Gauge-invariant observables |
| Local Lorentz redundancy | Local gauge redundancy |

The mathematical structure is the same: a principal bundle, a connection, a curvature, and a quotient by local admissibility transformations.

---

## 4. Principal Bundles and Gauge Connections

Let \(M\) be spacetime and let \(G\) be a Lie group with Lie algebra \(\mathfrak g\). A principal \(G\)-bundle is a fiber bundle

\[
\pi:P\to M
\]

with a free right action of \(G\) on \(P\).

A gauge connection is a \(\mathfrak g\)-valued one-form \(A\) on \(P\) satisfying the usual connection properties. Locally, after choosing a section, one writes

\[
A=A_\mu dx^\mu,
\]

with

\[
A_\mu=A_\mu^a T_a,
\]

where \(T_a\) are generators of \(\mathfrak g\).

The curvature is

\[
\boxed{
F=dA+A\wedge A.
}
\]

In components,

\[
F_{\mu\nu}
=
\partial_\mu A_\nu
-
\partial_\nu A_\mu
-
ig[A_\mu,A_\nu],
\]

or, in structure-constant form,

\[
F_{\mu\nu}^a
=
\partial_\mu A_\nu^a
-
\partial_\nu A_\mu^a
+
g f^a{}_{bc}A_\mu^b A_\nu^c,
\]

depending on convention.

The covariant derivative acting on a matter field \(\psi\) in representation \(\rho\) is

\[
\boxed{
D_\mu\psi
=
\partial_\mu\psi
+
\rho_*(A_\mu)\psi.
}
\]

In physics notation, for Hermitian generators,

\[
D_\mu
=
\partial_\mu
-
ig A_\mu^a T_a.
\]

---

## 5. Gauge Transformations as Admissibility Transformations

A gauge transformation is a smooth map

\[
u:M\to G.
\]

The local gauge group is

\[
\mathcal G=C^\infty(M,G).
\]

Under a finite gauge transformation, the connection transforms as

\[
\boxed{
A_\mu
\mapsto
A_\mu^u
=
u A_\mu u^{-1}
+
\frac{i}{g}(\partial_\mu u)u^{-1}.
}
\]

The curvature transforms covariantly:

\[
\boxed{
F_{\mu\nu}
\mapsto
F_{\mu\nu}^u
=
u F_{\mu\nu}u^{-1}.
}
\]

A matter field transforms as

\[
\psi\mapsto \psi^u=u\psi,
\]

or, in a representation \(\rho\),

\[
\psi\mapsto \rho(u)\psi.
\]

The covariant derivative transforms covariantly:

\[
D_\mu\psi\mapsto uD_\mu\psi.
\]

Thus gauge transformations preserve the relational structure of internal differentiation.

Infinitesimally, for

\[
u(x)=\exp(i\alpha^a(x)T_a),
\]

one has

\[
\delta_\alpha A_\mu^a
=
D_\mu\alpha^a,
\]

up to convention, and

\[
\delta_\alpha\psi
=
i\alpha^a T_a\psi.
\]

The infinitesimal generators of gauge transformations are the Gauss constraints of the canonical theory.

---

## 6. Gauge Orbits and Physical Objects

The central ontological claim of Gauge Theory of Admissibility is:

\[
\boxed{
\text{A physical gauge configuration is an orbit }[A,\psi].
}
\]

The orbit is

\[
[A,\psi]
=
\{
(A^u,\psi^u)
\mid
u\in\mathcal G
\}.
\]

Two gauge potentials related by a gauge transformation describe the same physical configuration.

The invariant projection is

\[
I_{\rm gauge}:
\mathcal A\times\Gamma(E)
\to
(\mathcal A\times\Gamma(E))/\mathcal G,
\]

\[
I_{\rm gauge}(A,\psi)=[A,\psi].
\]

Thus the gauge potential \(A_\mu\) is a description, while the gauge orbit \([A]\) is the physical object.

This is the gauge-theoretic analogue of the Frame Theory statement that the coframe \(e^I_\mu\) is a description while the metric \(g_{\mu\nu}\) is an invariant of the frame orbit.

---

## 7. Gauge-Invariant Observables

By Invariant Theory, a functional is physically measurable only if it is constant on gauge orbits.

A functional

\[
\mathcal O[A,\psi]
\]

is gauge invariant if

\[
\mathcal O[A^u,\psi^u]
=
\mathcal O[A,\psi]
\]

for all \(u\in\mathcal G\).

The observable algebra is

\[
\boxed{
\mathcal O_{\rm phys}
=
C^\infty(\mathcal A\times\Gamma(E))^\mathcal G.
}
\]

Examples include:

### 7.1 Local invariant polynomials

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}),
\]

\[
\operatorname{tr}(F\wedge *F),
\]

\[
\operatorname{tr}(F\wedge F).
\]

For matter fields, invariant contractions include

\[
\bar\psi\psi,
\]

\[
\bar\psi\gamma^\mu D_\mu\psi,
\]

\[
\phi^\dagger\phi,
\]

when the representation contractions are gauge singlets.

### 7.2 Wilson loops

For a closed loop \(C\), the Wilson loop is

\[
\boxed{
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
}
\]

Under a gauge transformation, the holonomy transforms by conjugation, and the trace is invariant.

Wilson loops are central nonlocal gauge invariants.

### 7.3 Topological invariants

For compact non-Abelian groups, characteristic classes such as

\[
\frac{1}{8\pi^2}
\int_M \operatorname{tr}(F\wedge F)
\]

are gauge-invariant topological quantities.

Thus measurable gauge content consists of invariant orbits, not gauge representatives.

---

## 8. Yang–Mills Theory as General Admissibility Dynamics

The universal invariant action for a gauge connection is the Yang–Mills action.

With a compact Lie group \(G\), the Yang–Mills action is

\[
\boxed{
S_{\rm YM}[A]
=
-\frac{1}{2g^2}
\int_M
\operatorname{tr}(F\wedge *F).
}
\]

In component notation,

\[
S_{\rm YM}[A]
=
-\frac14
\int d^4x\,
F_{\mu\nu}^aF^{a\mu\nu}.
\]

This action is gauge invariant because

\[
F\mapsto uFu^{-1}
\]

and the trace is cyclic:

\[
\operatorname{tr}(uFu^{-1}uFu^{-1})
=
\operatorname{tr}(F^2).
\]

The Hodge star requires a spacetime metric, but the gauge admissibility structure itself does not.

---

## 9. Yang–Mills Field Equations

Vary the action with respect to \(A\). Since

\[
\delta F
=
D\delta A,
\]

we have

\[
\delta S_{\rm YM}
=
-\frac{1}{g^2}
\int
\operatorname{tr}(\delta F\wedge *F)
=
-\frac{1}{g^2}
\int
\operatorname{tr}(D\delta A\wedge *F).
\]

Integrating by parts,

\[
\delta S_{\rm YM}
=
\frac{1}{g^2}
\int
\operatorname{tr}(\delta A\wedge D*F)
+
\text{boundary term}.
\]

Thus the vacuum Yang–Mills equation is

\[
\boxed{
D*F=0.
}
\]

In components,

\[
\boxed{
D_\mu F^{\mu\nu}=0.
}
\]

With matter sources,

\[
D_\mu F^{\mu\nu}
=
J^\nu,
\]

where \(J^\nu\) is the gauge current.

The Bianchi identity is

\[
\boxed{
DF=0,
}
\]

or in components,

\[
D_{[\mu}F_{\nu\rho]}=0.
\]

These are the universal structural equations of non-Abelian gauge admissibility.

---

## 10. Gauge Invariance and the Noether Identity

Gauge invariance of the action implies a differential identity among the field equations.

Let

\[
\frac{\delta S}{\delta A_\mu^a}
\]

denote the Euler–Lagrange derivative. Gauge invariance under

\[
\delta A_\mu^a=D_\mu\alpha^a
\]

implies

\[
0
=
\delta_\alpha S
=
\int d^4x\,
\frac{\delta S}{\delta A_\mu^a}
D_\mu\alpha^a.
\]

Integrating by parts gives

\[
\int d^4x\,
\alpha^a
D_\mu
\left(
\frac{\delta S}{\delta A_\mu^a}
\right)
=
0.
\]

Since \(\alpha^a\) is arbitrary,

\[
\boxed{
D_\mu
\left(
\frac{\delta S}{\delta A_\mu^a}
\right)
=
0.
}
\]

For Yang–Mills theory,

\[
\frac{\delta S}{\delta A_\mu^a}
\propto
D_\nu F^{\nu\mu}_a,
\]

and the identity reduces to the covariant conservation law

\[
D_\mu D_\nu F^{\nu\mu}=0.
\]

In the presence of matter, this gives the covariant current conservation law

\[
\boxed{
D_\mu J^\mu=0.
}
\]

This is the gauge-theoretic form of Noether consistency.

---

## 11. Canonical Structure and Gauss Constraints

In canonical gauge theory, one decomposes spacetime into space and time. The spatial gauge field is

\[
A_i(x),
\qquad i=1,2,3,
\]

and its conjugate momentum is the electric field

\[
E^i_a(x).
\]

The time component \(A_0^a\) is not dynamical. It enforces the Gauss constraint

\[
\boxed{
\mathcal G_a(x)
=
D_i E^i_a(x)-\rho_a(x)
\approx0.
}
\]

Here

\[
D_i E^i_a
=
\partial_i E^i_a
+
g f_a{}_{bc}A_i^b E^{ic},
\]

and \(\rho_a\) is the matter color charge density.

The Gauss constraints generate gauge transformations:

\[
\{A_i^a(x),\int d^3y\,\alpha^b(y)\mathcal G_b(y)\}
=
D_i\alpha^a(x).
\]

Thus gauge transformations are canonical admissibility transformations.

Physical states in the quantum theory satisfy

\[
\boxed{
\hat{\mathcal G}_a(x)
|\Psi_{\rm phys}\rangle
=
0.
}
\]

The physical Hilbert space is the gauge-invariant subspace:

\[
\mathcal H_{\rm phys}
=
\{
|\Psi\rangle\in\mathcal H_{\rm kin}
\mid
\hat{\mathcal G}_a(x)|\Psi\rangle=0
\}.
\]

Equivalently, physical states are constant along gauge orbits.

---

## 12. Electromagnetism as \(U(1)\) Admissibility

The simplest gauge theory is obtained by choosing

\[
\boxed{
G=U(1).
}
\]

The Lie algebra is Abelian:

\[
\mathfrak u(1)\cong i\mathbb R.
\]

The connection is the electromagnetic potential

\[
A=A_\mu dx^\mu.
\]

The curvature is

\[
\boxed{
F=dA.
}
\]

In components,

\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu.
\]

A local \(U(1)\) admissibility transformation is

\[
\psi\mapsto e^{iq\lambda(x)}\psi,
\]

\[
A_\mu\mapsto A_\mu+\partial_\mu\lambda.
\]

The covariant derivative is

\[
D_\mu\psi
=
(\partial_\mu-iqA_\mu)\psi.
\]

The Maxwell action is

\[
\boxed{
S_{\rm EM}[A]
=
-\frac14
\int d^4x\,
F_{\mu\nu}F^{\mu\nu}.
}
\]

The field equations are

\[
\boxed{
\partial_\mu F^{\mu\nu}=j^\nu,
}
\]

with current conservation

\[
\partial_\nu j^\nu=0.
\]

The Bianchi identity is

\[
\partial_{[\mu}F_{\nu\rho]}=0,
\]

equivalently,

\[
dF=0.
\]

The gauge-invariant observables include

\[
F_{\mu\nu}F^{\mu\nu},
\]

\[
F_{\mu\nu}\tilde F^{\mu\nu},
\]

and Wilson loops

\[
W_q(C)
=
\exp
\left(
iq\oint_C A
\right).
\]

Thus electromagnetism is the Abelian gauge theory of local phase admissibility.

\[
\boxed{
\text{Electromagnetism is }U(1)\text{ Gauge Theory of Admissibility.}
}
\]

---

## 13. Weak Interaction as \(SU(2)\) Admissibility

The weak interaction is naturally described by a non-Abelian internal admissibility group. At the level of weak isospin, one takes

\[
\boxed{
G=SU(2).
}
\]

Let \(T^a=\tau^a/2\), \(a=1,2,3\), be the generators of \(SU(2)\), where \(\tau^a\) are Pauli matrices.

The gauge fields are

\[
W_\mu^a.
\]

The field strength is

\[
W_{\mu\nu}^a
=
\partial_\mu W_\nu^a
-
\partial_\nu W_\mu^a
+
g\epsilon^a{}_{bc}W_\mu^b W_\nu^c.
\]

Matter fields transforming under \(SU(2)\) are grouped into doublets. For example, a left-handed lepton doublet is

\[
L=
\begin{pmatrix}
\nu_L\\
e_L
\end{pmatrix}.
\]

The covariant derivative is

\[
D_\mu L
=
\left(
\partial_\mu
-
ig W_\mu^a\frac{\tau^a}{2}
\right)L.
\]

The Yang–Mills action for the weak gauge fields is

\[
S_W
=
-\frac14
\int d^4x\,
W_{\mu\nu}^a W^{a\mu\nu}.
\]

The weak gauge symmetry acts only on the appropriate chiral sector. In the Standard Model, this is expressed by assigning left-handed fermions to \(SU(2)_L\) doublets and right-handed fermions to \(SU(2)_L\) singlets.

Thus the weak interaction is not introduced as a separate foundational structure. It is the gauge admissibility theory of local weak-isospin frames.

\[
\boxed{
\text{Weak isospin interactions are }SU(2)\text{ Gauge Theory of Admissibility.}
}
\]

---

## 14. Electroweak Theory and the Orbit of the Higgs Vacuum

The full electroweak gauge group is

\[
\boxed{
G_{\rm EW}
=
SU(2)_L\times U(1)_Y.
}
\]

The corresponding gauge fields are

\[
W_\mu^a,\qquad B_\mu.
\]

The covariant derivative acting on the Higgs doublet \(\Phi\) is

\[
D_\mu\Phi
=
\left(
\partial_\mu
-
ig W_\mu^a\frac{\tau^a}{2}
-
ig' Y B_\mu
\right)\Phi.
\]

The Higgs potential is

\[
V(\Phi)
=
\lambda
\left(
\Phi^\dagger\Phi-\frac{v^2}{2}
\right)^2.
\]

The vacuum manifold is

\[
\Phi^\dagger\Phi=\frac{v^2}{2}.
\]

A representative vacuum is

\[
\Phi_0
=
\frac{1}{\sqrt2}
\begin{pmatrix}
0\\
v
\end{pmatrix}.
\]

The unbroken subgroup is the stabilizer of this vacuum orbit:

\[
H_{\rm vac}
=
\{
g\in SU(2)_L\times U(1)_Y
\mid
g\Phi_0=\Phi_0
\}.
\]

This stabilizer is the electromagnetic group

\[
\boxed{
H_{\rm vac}=U(1)_{\rm em}.
}
\]

Thus spontaneous symmetry breaking is not the destruction of gauge admissibility. It is the selection of a vacuum orbit whose stabilizer defines the residual manifest symmetry.

The Higgs kinetic term,

\[
|D_\mu\Phi|^2,
\]

produces gauge-boson masses while preserving gauge invariance:

\[
M_W=\frac{gv}{2},
\]

\[
M_Z=\frac{v}{2}\sqrt{g^2+g'^2},
\]

\[
M_\gamma=0.
\]

Therefore the electroweak theory is a Gauge Theory of Admissibility with a nontrivial vacuum orbit and stabilizer structure.

---

## 15. Quantum Chromodynamics as \(SU(3)\) Admissibility

Quantum chromodynamics is obtained by choosing

\[
\boxed{
G=SU(3).
}
\]

The Lie algebra \(\mathfrak{su}(3)\) has eight generators, often written

\[
T^a=\frac{\lambda^a}{2},
\qquad a=1,\dots,8,
\]

where \(\lambda^a\) are the Gell-Mann matrices.

The gluon field is

\[
A_\mu^a,
\]

and the field strength is

\[
G_{\mu\nu}^a
=
\partial_\mu A_\nu^a
-
\partial_\nu A_\mu^a
+
g_s f^a{}_{bc}A_\mu^b A_\nu^c.
\]

Quark fields \(q_f\) carry color indices and transform in the fundamental representation:

\[
q_f\mapsto u(x)q_f,
\qquad
u(x)\in SU(3).
\]

The covariant derivative is

\[
D_\mu q_f
=
\left(
\partial_\mu
-
ig_s A_\mu^a T^a
\right)q_f.
\]

The QCD Lagrangian is

\[
\boxed{
\mathcal L_{\rm QCD}
=
-\frac14 G_{\mu\nu}^aG^{a\mu\nu}
+
\sum_f
\bar q_f
(i\gamma^\mu D_\mu-m_f)
q_f.
}
\]

This Lagrangian is invariant under local color admissibility transformations.

The physical observables are color singlets. Examples include:

\[
\bar q q,
\]

\[
\bar q\gamma^\mu q,
\]

\[
G_{\mu\nu}^aG^{a\mu\nu},
\]

\[
\epsilon^{ijk}q_i q_j q_k.
\]

The last operator corresponds to a baryon color singlet.

Thus QCD is the gauge admissibility theory of local color frames.

\[
\boxed{
\text{QCD is }SU(3)\text{ Gauge Theory of Admissibility.}
}
\]

---

## 16. The Standard Model as Product Admissibility

The gauge sector of the Standard Model is obtained by choosing the product group

\[
\boxed{
G_{\rm SM}
=
SU(3)_c\times SU(2)_L\times U(1)_Y.
}
\]

The corresponding connection is

\[
A_\mu
=
(A_\mu^{(c)},W_\mu^{(a)},B_\mu),
\]

where:

- \(A_\mu^{(c)}\) is the color connection for \(SU(3)_c\),
- \(W_\mu^{(a)}\) is the weak-isospin connection for \(SU(2)_L\),
- \(B_\mu\) is the hypercharge connection for \(U(1)_Y\).

Matter fields are assigned to representations of this product group.

The Standard Model Lagrangian is built from gauge-invariant contractions of:

1. Yang–Mills field strengths,
2. covariant derivatives of matter fields,
3. Yukawa couplings compatible with gauge admissibility,
4. Higgs potential and kinetic terms.

Thus the Standard Model is a single Gauge Theory of Admissibility with product structure group.

\[
\boxed{
\text{The Standard Model is a product admissibility theory.}
}
\]

---

## 17. Gauge Theory of Admissibility and Geometry

Gauge Theory of Admissibility is naturally geometric.

The principal bundle \(P\to M\) encodes the global structure of internal frames. The connection \(A\) defines horizontal transport. The curvature \(F\) measures the failure of internal frames to integrate consistently around closed loops.

The Wilson loop

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right)
\]

measures the holonomy of the connection around \(C\).

Thus curvature is not merely a force field. It is the geometric obstruction to path-independent internal admissibility.

In this sense, gauge forces are the relational geometry of internal frames.

---

## 18. Topological Sectors and Global Admissibility

Gauge Theory of Admissibility also includes global and topological structure.

Principal \(G\)-bundles over a spacetime manifold \(M\) may fall into distinct topological classes. These classes are characterized by characteristic classes constructed from the curvature.

For example, for \(SU(n)\),

\[
c_k(P)
=
\left[
\operatorname{tr}(F^k)
\right]
\in H^{2k}(M,\mathbb R)
\]

represent Chern classes.

In four-dimensional Euclidean Yang–Mills theory, the instanton number is

\[
\boxed{
k
=
\frac{1}{8\pi^2}
\int_M
\operatorname{tr}(F\wedge F).
}
\]

For suitable compactification, \(k\in\mathbb Z\).

Thus the physical configuration space is not merely local gauge potentials modulo local gauge transformations. It also includes global topological sectors.

These sectors are orbit-level invariants. They cannot be removed by local gauge transformations.

---

## 19. Quantum Gauge Theory of Admissibility

In quantum gauge theory, the path integral is formally an integral over gauge orbits:

\[
\boxed{
Z
=
\int_{\mathcal A/\mathcal G}
\mathcal D A\,
e^{iS_{\rm YM}[A]}.
}
\]

In practice, one fixes a gauge. One inserts a gauge-fixing condition \(G(A)=0\) and the corresponding Faddeev–Popov determinant.

The gauge-fixed path integral becomes

\[
Z
=
\int
\mathcal D A\,
\mathcal D c\,
\mathcal D\bar c\,
\mathcal D B\,
e^{iS_{\rm YM}+iS_{\rm gf}+iS_{\rm ghost}}.
\]

Here \(c\) and \(\bar c\) are ghost and antighost fields, and \(B\) is an auxiliary field.

The resulting BRST symmetry encodes the residual admissibility structure after gauge fixing.

---

## 20. BRST Cohomology and Physical Observables

The BRST transformations are

\[
sA_\mu
=
D_\mu c,
\]

\[
sc
=
-\frac12[c,c],
\]

\[
s\bar c
=
B,
\]

\[
sB
=
0.
\]

The BRST operator is nilpotent:

\[
s^2=0.
\]

Physical operators are BRST-closed modulo BRST-exact operators:

\[
s\mathcal O=0,
\]

\[
\mathcal O\sim \mathcal O+s\Lambda.
\]

Thus the physical observable algebra is the BRST cohomology:

\[
\boxed{
\mathcal O_{\rm phys}
=
H^\bullet(s).
}
\]

This is the quantum refinement of the invariant algebra

\[
C^\infty(\mathcal A)^\mathcal G.
\]

---

## 21. Gauge Anomalies and Admissibility Consistency

A quantum gauge theory is consistent only if gauge admissibility survives quantization.

If the quantum measure or effective action fails to be gauge invariant, the theory has a gauge anomaly. Such an anomaly destroys the quotient structure:

\[
\mathcal A/\mathcal G
\]

is no longer well defined at the quantum level.

Gauge anomaly cancellation is therefore not optional. It is the condition that the admissibility group remains a valid equivalence relation among quantum descriptions.

For the Standard Model, anomaly cancellation imposes precise constraints on the representation content of fermions. This is one of the deepest pieces of evidence that gauge admissibility is structurally fundamental.

---

## 22. Gauge Theory of Admissibility and the Standard Interactions

The four fundamental gauge interactions arise as special admissibility theories.

| Interaction | Internal admissibility group | Connection | Curvature |
|---|---|---|---|
| Electromagnetism | \(U(1)\) | \(A_\mu\) | \(F_{\mu\nu}\) |
| Weak isospin | \(SU(2)_L\) | \(W_\mu^a\) | \(W_{\mu\nu}^a\) |
| Quantum chromodynamics | \(SU(3)_c\) | \(A_\mu^a\) | \(G_{\mu\nu}^a\) |
| Standard Model gauge sector | \(SU(3)\times SU(2)\times U(1)\) | Combined connection | Combined curvature |

The pattern is universal:

\[
\boxed{
\text{Choose }G
\quad\Rightarrow\quad
\text{construct principal }G\text{-bundle}
\quad\Rightarrow\quad
\text{introduce connection}
\quad\Rightarrow\quad
\text{build invariant dynamics}.
}
\]

Thus gauge interactions are not separate laws imposed on nature. They are consequences of choosing different internal admissibility groups.

---

## 23. Comparison with Frame Theory

Frame Theory and Gauge Theory of Admissibility have the same structural form.

### Frame Theory

\[
\Omega_{\rm FT}=\{e^I_\mu\},
\]

\[
G_{\rm FT}=C^\infty(M,\mathrm{Spin}(1,3)),
\]

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

The metric is the invariant of local spacetime frame orbits.

### Gauge Theory of Admissibility

\[
\Omega_{\rm gauge}=\mathcal A\times\Gamma(E),
\]

\[
\mathcal G=C^\infty(M,G),
\]

\[
\mathcal O_{\rm phys}
=
C^\infty(\Omega_{\rm gauge})^\mathcal G.
\]

Gauge-invariant functionals are the invariants of internal frame orbits.

Thus Frame Theory is the special case in which the admissibility group is the spacetime spin group. Gauge Theory of Admissibility is the generalization to arbitrary internal groups.

---

## 24. Gauge Theory of Admissibility Within Relativity Mechanics

Gauge Theory of Admissibility is one of the central derived theories of Relativity Mechanics.

It presupposes:

1. **Orbit Theory:** physical configurations are gauge orbits.
2. **Invariant Theory:** measurable quantities are gauge-invariant functionals.
3. **Observer Theory:** internal frames are reference structures.
4. **Constraint Mechanics:** Gauss laws generate gauge admissibility.
5. **Relativistic Dynamics:** Yang–Mills equations descend to the quotient.
6. **Relativistic Quantum Theory:** physical states satisfy gauge constraints or BRST cohomology.
7. **Relativity Geometry:** connections and curvature are quotient geometry.
8. **Frame Theory:** the spin-group case is recovered as a special frame admissibility theory.

Thus Gauge Theory of Admissibility is not an independent addition to Relativity Mechanics. It is the result of replacing the frame group by an arbitrary Lie group.

---

## 25. Summary of the Gauge-Theoretic Schema

The Gauge Theory of Admissibility is specified by:

\[
\boxed{
\mathcal R_{\rm GTA}
=
(\Omega_{\rm gauge},\mathcal G,\triangleright,I_{\rm gauge}).
}
\]

Where:

\[
\Omega_{\rm gauge}
=
\mathcal A\times\Gamma(E),
\]

\[
\mathcal G
=
C^\infty(M,G),
\]

\[
A\mapsto A^u,
\qquad
\psi\mapsto u\psi,
\]

\[
I_{\rm gauge}(A,\psi)=[A,\psi].
\]

The curvature is

\[
F=dA+A\wedge A.
\]

The universal invariant action is

\[
S_{\rm YM}
=
-\frac{1}{2g^2}
\int
\operatorname{tr}(F\wedge *F).
\]

The field equation is

\[
D*F=J.
\]

The Bianchi identity is

\[
DF=0.
\]

The Gauss constraint is

\[
\mathcal G_a
=
D_i E^i_a-\rho_a
\approx0.
\]

Physical observables satisfy

\[
\mathcal O[A^u,\psi^u]
=
\mathcal O[A,\psi].
\]

Special choices of \(G\) yield:

\[
\begin{aligned}
G=U(1)
&\Rightarrow
\text{Electromagnetism},\\
G=SU(2)
&\Rightarrow
\text{Weak interaction},\\
G=SU(3)
&\Rightarrow
\text{QCD},\\
G=SU(3)\times SU(2)\times U(1)
&\Rightarrow
\text{Standard Model}.
\end{aligned}
\]

---

## 26. Conclusion

Gauge Theory of Admissibility provides the unified foundation of gauge physics. It arises from Relativity Mechanics by replacing the spacetime spin frame group

\[
\mathrm{Spin}(1,3)
\]

with an arbitrary Lie group \(G\). The resulting description space consists of internal frames, connections, and matter fields. The admissibility group is the local gauge group \(\mathcal G=C^\infty(M,G)\). Physical configurations are gauge orbits, and measurable quantities are gauge invariants.

Yang–Mills theory is the general dynamical theory of such admissibility structures. Electromagnetism is the \(U(1)\) case. Weak interactions arise from \(SU(2)_L\) admissibility. Quantum chromodynamics arises from \(SU(3)_c\) admissibility. The Standard Model is the product admissibility theory

\[
SU(3)\times SU(2)\times U(1).
\]

Thus gauge theory is not a collection of independent force laws. It is the mathematics of local internal admissibility.

The central principle is:

\[
\boxed{
\text{Gauge symmetry is local admissibility.}
}
\]

Equivalently:

\[
\boxed{
\text{Gauge fields are connections between internal frames; physical reality is the gauge orbit.}
}
\]

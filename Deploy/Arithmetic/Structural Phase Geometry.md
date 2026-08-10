# Structural Phase Geometry

## A White Paper on the Intrinsic Phase Coordinate of Mathematical Structures

---

## Abstract

This paper develops **Structural Phase Geometry (SPG)**, a geometric framework in which *phase* is treated not as a secondary attribute of oscillatory representations, but as an intrinsic geometric coordinate attached to mathematical structure itself. The fundamental object is a phase map

\[
\Phi:M\longrightarrow S,
\]

where \(M\) is the underlying structured manifold and \(S\) is a phase target, typically a circle, torus, or more general phase manifold equipped with a canonical connection. SPG promotes phase to a coordinate with its own differential calculus, gauge theory, metric deformation, curvature, variational principles, and global topological obstructions.

The central claim is that many seemingly distinct phase phenomena in harmonic analysis, wave propagation, complex geometry, and dynamical systems are manifestations of a single structural fact: mathematical structures induce natural phase coordinates. These phase coordinates may arise from determinant lines, character representations of structure groups, spectral asymmetry, oscillatory symbols, or invariant fibrations of flows.

We formulate an axiomatic foundation for SPG, develop the local and global differential geometry of phase fields, introduce phase metrics and phase connections, prove several core structural results, and apply the theory to Fourier integral operators, high-frequency wave propagation, complex canonical bundles, and dynamical phase coordinates. The result is a unified geometry in which phase becomes a first-class coordinate of mathematical structure.

---

## 1. Introduction

Phase appears throughout mathematics. In harmonic analysis it governs oscillation and cancellation. In wave theory it determines ray propagation and interference. In complex geometry it appears as the argument of holomorphic forms and sections. In dynamical systems it parametrizes rotation, recurrence, and asymptotic synchronization. Yet phase is usually treated as an auxiliary quantity: the argument of a complex amplitude, a bookkeeping variable in an asymptotic expansion, or a coordinate on an invariant torus.

**Structural Phase Geometry (SPG)** begins from a different premise:

> **Phase is an intrinsic geometric coordinate associated with mathematical structure.**

Rather than asking how phase appears inside a particular representation, SPG asks what geometry is induced once phase is admitted as a coordinate in its own right. The elementary object is a map

\[
\Phi:M\longrightarrow S,
\]

where \(M\) carries a mathematical structure and \(S\) is a phase space. In the simplest case \(S=S^{1}\), and \(\Phi\) assigns to each point of \(M\) an angle. More generally, \(S\) may be a torus \(T^{r}\), a projective phase space, a coadjoint orbit, or a stratified phase manifold.

The purpose of this paper is to develop SPG as a self-contained geometric theory. The framework is built around four principles.

1. **Phase is structural.**  
   Phase assignments arise naturally from the structure itself: from determinant lines, characters of structure groups, spectral data, oscillatory symbols, or invariant foliations.

2. **Phase is geometric.**  
   The phase map induces one-forms, connections, curvatures, metrics, and geodesic structures on \(M\).

3. **Phase is gauge-theoretic.**  
   Local phase functions are defined only up to additive constants or \(2\pi\)-periodic gauge transformations. Gauge-invariant information is carried by curvature, holonomy, and cohomology.

4. **Phase is variational.**  
   Natural energy functionals on phase fields produce harmonic phase equations, phase heat flows, phase vortices, and phase-calibrated submanifolds.

SPG is not merely a reinterpretation of known phase variables. It provides a unified differential-geometric language for phase across different domains. The same formal object — a phase field with connection and curvature — controls stationary phase asymptotics, eikonal propagation, canonical-bundle arguments, and rotation coordinates in dynamics.

---

## 2. Phase Targets and Structural Phase Fields

### 2.1 Phase targets

A **phase target** is a smooth manifold equipped with the data required to measure phase variation.

**Definition 2.1.** A phase target is a quadruple

\[
(S,\vartheta,h_S,\nabla^S),
\]

where

- \(S\) is a smooth manifold,
- \(\vartheta\in \Omega^1(S)\) or \(\vartheta\in \Omega^1(S;\mathfrak{u}(1))\) is a canonical phase one-form or connection form,
- \(h_S\) is a Riemannian metric on \(S\),
- \(\nabla^S\) is a compatible connection when required.

The fundamental examples are the following.

#### Example 2.2: The circle phase target

Let

\[
S=S^1=\mathbb{R}/2\pi\mathbb{Z}
\]

with angular coordinate \(\theta\). The canonical Maurer–Cartan form is

\[
\vartheta=d\theta.
\]

The standard metric is

\[
h_{S^1}=d\theta\otimes d\theta.
\]

A phase field \(\Phi:M\to S^1\) may be locally written as

\[
\Phi(x)=e^{i\varphi(x)},
\]

where \(\varphi:U\to \mathbb{R}\) is a local phase function.

#### Example 2.3: Toroidal phase targets

Let

\[
S=T^r=\mathbb{R}^r/(2\pi\mathbb{Z})^r
\]

with angular coordinates \(\theta^a\), \(a=1,\dots,r\). The canonical phase one-forms are

\[
\vartheta^a=d\theta^a.
\]

This target naturally appears in integrable dynamics, where the \(\theta^a\) are angle variables.

#### Example 2.4: Projective phase targets

Let \(S=\mathbb{C}P^{N-1}\). A normalized vector \(\psi\in \mathbb{C}^N\) defines a point \([\psi]\in \mathbb{C}P^{N-1}\). The Berry connection is locally represented by

\[
\mathcal{A}= \operatorname{Im}\langle \psi,d\psi\rangle,
\]

and the associated phase one-form is obtained by pullback along a map \(\Phi:M\to \mathbb{C}P^{N-1}\).

This target is relevant for structured families of eigenstates, spectral projections, and nonabelian phase phenomena.

---

### 2.2 Structural phase fields

Let \(M\) be a smooth manifold carrying some additional mathematical structure \(\mathscr{S}\). This structure may be a metric, complex structure, symplectic form, differential operator, dynamical system, oscillatory symbol, or sheaf of solutions.

**Definition 2.5.** A **structural phase field** on \((M,\mathscr{S})\) is a smooth map

\[
\Phi:M\longrightarrow S
\]

into a phase target \(S\).

The phase field induces a phase one-form

\[
\alpha := \Phi^{*}\vartheta \in \Omega^1(M).
\]

In local coordinates \(x^i\) on \(M\) and \(y^A\) on \(S\),

\[
\alpha_i
=
\partial_i \Phi^A \, \vartheta_A(\Phi),
\]

so that

\[
\alpha = \alpha_i\, dx^i.
\]

For the circle target \(S=S^1\), if \(\Phi=e^{i\varphi}\), then locally

\[
\alpha=d\varphi,
\]

or in components,

\[
\alpha_i=\partial_i\varphi.
\]

The phase field therefore equips \(M\) with a distinguished one-form. This one-form is the primary local differential object of SPG.

---

### 2.3 Gauge transformations

Phase is inherently gauge-dependent at the level of local functions. For \(S=S^1\), if

\[
\Phi=e^{i\varphi},
\]

then the local phase function \(\varphi\) is defined only modulo

\[
\varphi \mapsto \varphi + 2\pi k,
\qquad k\in \mathbb{Z}.
\]

More generally, for a smooth gauge transformation

\[
u:M\to S^1,
\qquad u=e^{i\chi},
\]

the phase field transforms as

\[
\Phi \mapsto u\Phi.
\]

The induced phase one-form transforms as

\[
\alpha \mapsto \alpha + d\chi.
\]

Thus \(\alpha\) is not gauge-invariant, but its exterior derivative

\[
F := d\alpha
\]

is gauge-invariant. In components,

\[
F_{ij}=\partial_i\alpha_j-\partial_j\alpha_i.
\]

The two-form \(F\) is the **phase curvature** or **phase field strength**.

If \(\Phi:M\to S^1\) is globally smooth and \(\alpha=\Phi^*d\theta\), then \(F=d\alpha=0\). Nontrivial curvature appears in SPG in three closely related ways:

1. through singular phase fields,
2. through phase connections on nontrivial phase bundles,
3. through phase targets with nontrivial Berry or Chern connections.

This is not a defect. It is the geometric source of the theory’s global content.

---

### 2.4 Phase bundles and global phase

A globally defined map \(\Phi:M\to S^1\) is often too restrictive. Many mathematical structures possess phase locally but not globally. The natural global object is a principal \(U(1)\)-bundle

\[
\pi:P\to M
\]

with connection \(A\in\Omega^1(P;i\mathbb{R})\). Locally, choosing a section \(\sigma_U:U\to P\), one obtains a local connection one-form

\[
A_U := \sigma_U^*A.
\]

Writing

\[
A_U = i\alpha_U,
\]

we interpret \(\alpha_U\) as the local structural phase one-form.

On overlaps \(U\cap V\), the local sections differ by a gauge transformation

\[
g_{UV}:U\cap V\to U(1),
\]

and the local phase forms transform as

\[
\alpha_V = \alpha_U + g_{UV}^* d\theta.
\]

The curvature

\[
F_A = dA
\]

descends to a globally defined two-form on \(M\). In local real notation,

\[
F_U = d\alpha_U.
\]

Thus the bundle formulation provides the global geometric home for structural phase.

The fundamental relation between curvature and topology is the following.

**Proposition 2.6.** Let \(P\to M\) be a principal \(U(1)\)-bundle with connection \(A\) and curvature \(F_A\). If

\[
\frac{1}{2\pi}[F_A]\in H^2(M;\mathbb{Z})
\]

is nonzero, then there is no global phase function \(\varphi\) such that

\[
A=i\,d\varphi.
\]

Equivalently, nonzero phase curvature obstructs global trivialization of phase.

This is the first global theorem of SPG: phase curvature measures the failure of a structure to admit a single-valued global phase coordinate.

---

## 3. Axiomatic Framework for SPG

We now formulate SPG axiomatically. The purpose is to isolate the properties that any reasonable structural phase assignment should satisfy.

Let \(\mathbf{Struct}\) be a category whose objects are structured manifolds

\[
(M,\mathscr{S})
\]

and whose morphisms are structure-preserving smooth maps.

Let \(\mathbf{PhaseGeom}\) be the category whose objects are phase geometries

\[
(M,\Phi,\alpha,F,g_\Phi)
\]

and whose morphisms preserve phase data.

A **phase assignment** is a functor

\[
\mathscr{P}:\mathbf{Struct}\longrightarrow \mathbf{PhaseGeom}.
\]

We impose the following axioms.

---

### Axiom I: Existence of structural phase

For every phase-admissible structured manifold \((M,\mathscr{S})\), there exists a phase geometry

\[
\mathscr{P}(M,\mathscr{S})=(M,\Phi_{\mathscr{S}},\alpha_{\mathscr{S}},F_{\mathscr{S}})
\]

possibly defined through a phase bundle.

---

### Axiom II: Naturality

If

\[
f:(M,\mathscr{S}_M)\longrightarrow (N,\mathscr{S}_N)
\]

is a structure-preserving map, then

\[
f^*\Phi_{\mathscr{S}_N}=\Phi_{\mathscr{S}_M}.
\]

Equivalently, phase is functorial with respect to structure-preserving maps.

---

### Axiom III: Locality

The phase field is determined locally by the structure. If two structures agree on an open set \(U\subset M\), then their phase fields agree on \(U\) up to gauge.

---

### Axiom IV: Gauge covariance

The local phase function is defined modulo \(U(1)\)-gauge transformations. Gauge-invariant content is carried by curvature, holonomy, and characteristic classes.

---

### Axiom V: Curvature obstruction

Nontrivial phase curvature represents an obstruction to the existence of a global phase trivialization.

---

### Axiom VI: Variational compatibility

Preferred phase fields arise as critical points of natural phase action functionals.

---

These axioms are intentionally broad. The power of SPG lies in the fact that many classical constructions satisfy them automatically.

---

## 4. Character Phases and \(G\)-Structures

A fundamental source of intrinsic phase is the representation theory of structure groups.

Let \(M\) carry a \(G\)-structure, represented by a principal \(G\)-bundle

\[
P_G\to M.
\]

Examples include:

- \(G=GL(n,\mathbb{R})\) for frame structures,
- \(G=O(n)\) for Riemannian structures,
- \(G=U(n)\) for Hermitian structures,
- \(G=Sp(2n,\mathbb{R})\) for symplectic structures,
- \(G=GL(n,\mathbb{C})\) for complex structures.

Suppose \(\chi:G\to U(1)\) is a smooth character. Then \(\chi\) defines an associated complex line bundle

\[
L_\chi := P_G\times_\chi \mathbb{C}.
\]

A principal connection \(\omega\) on \(P_G\) induces a connection \(\nabla^\chi\) on \(L_\chi\). Locally, over a section \(\sigma:U\to P_G\), the induced connection one-form is

\[
A_\chi := \chi_*(\sigma^*\omega)\in i\Omega^1(U).
\]

Writing

\[
A_\chi = i\alpha_\chi,
\]

we obtain a local phase one-form \(\alpha_\chi\).

The curvature of \(L_\chi\) is

\[
F_\chi = dA_\chi.
\]

Since \(A_\chi=i\alpha_\chi\), we have

\[
F_\chi=i\,d\alpha_\chi.
\]

Thus the real phase curvature is

\[
f_\chi := d\alpha_\chi = -iF_\chi.
\]

This proves the following fundamental result.

---

### Theorem 4.1: Character-Phase Theorem

Let \(P_G\to M\) be a \(G\)-structure with connection \(\omega\), and let \(\chi:G\to U(1)\) be a character. Then \(\chi\) induces a canonical structural phase sheaf with local phase one-forms

\[
\alpha_\chi = -i\,\chi_*(\sigma^*\omega).
\]

On overlaps these phase one-forms differ by gauge transformations, and their curvature is the globally defined two-form

\[
f_\chi = \chi_*(\Omega^\omega),
\]

where \(\Omega^\omega\) is the curvature of \(\omega\).

---

### Proof

Let \(\sigma_U:U\to P_G\) and \(\sigma_V:V\to P_G\) be local sections. On \(U\cap V\),

\[
\sigma_V = \sigma_U g_{UV},
\]

where \(g_{UV}:U\cap V\to G\). The principal connection transforms as

\[
\sigma_V^*\omega
=
\operatorname{Ad}_{g_{UV}^{-1}}\sigma_U^*\omega
+
g_{UV}^*\theta_G,
\]

where \(\theta_G\) is the Maurer–Cartan form on \(G\). Applying the Lie algebra homomorphism \(\chi_*:\mathfrak{g}\to i\mathbb{R}\), and using that \(U(1)\) is abelian, we obtain

\[
\chi_*(\sigma_V^*\omega)
=
\chi_*(\sigma_U^*\omega)
+
g_{UV}^*\chi_*(\theta_G).
\]

Since \(\chi_*(\theta_G)\) is the Maurer–Cartan form on \(U(1)\), the corresponding real phase forms satisfy

\[
\alpha_V = \alpha_U + d\chi_{UV},
\]

where \(e^{i\chi_{UV}}=\chi(g_{UV})\). Therefore the local phase forms define a \(U(1)\)-gauge equivalence class.

The curvature is

\[
F_\chi = dA_\chi
=
i\,d\alpha_\chi
=
\chi_*(d\omega)
=
\chi_*(\Omega^\omega),
\]

because \(\chi_*\) kills commutator terms. Hence

\[
f_\chi=d\alpha_\chi=-iF_\chi
\]

is globally defined. ∎

---

### Corollary 4.2

Every unitary character of a structure group produces an intrinsic phase geometry.

This provides a rigorous interpretation of the slogan:

> Mathematical structure carries phase.

The phase is not imposed externally. It is induced by the character theory of the structure group.

---

## 5. Differential Geometry of Phase

We now develop the local differential geometry of a phase field.

Let \((M,g)\) be a Riemannian or pseudo-Riemannian manifold, and let \(\alpha\in\Omega^1(M)\) be a structural phase one-form.

In local coordinates,

\[
\alpha=\alpha_i\,dx^i.
\]

The phase curvature is

\[
F=d\alpha,
\]

with components

\[
F_{ij}=\partial_i\alpha_j-\partial_j\alpha_i.
\]

It satisfies the Bianchi identity

\[
dF=0,
\]

or in components,

\[
\partial_{[i}F_{jk]}=0.
\]

If \(\alpha\) is a connection one-form rather than an exact form, the same local expression defines the phase field strength.

---

### 5.1 Phase holonomy

Given a closed curve \(\gamma:S^1\to M\), the phase holonomy is

\[
\operatorname{Hol}_\gamma(\alpha)
=
\exp\left(i\oint_\gamma \alpha\right).
\]

If \(\gamma=\partial\Sigma\), then by Stokes’ theorem,

\[
\operatorname{Hol}_\gamma(\alpha)
=
\exp\left(i\int_\Sigma F\right).
\]

Thus phase curvature controls the failure of phase to be globally path-independent.

This is the geometric mechanism behind interference, Berry-type phases, and topological phase obstructions.

---

### 5.2 Phase covariant derivative

Let \(\psi\) be a complex-valued field charged under phase transformations. Define the phase-covariant derivative

\[
D_i\psi := \nabla_i\psi - i\alpha_i\psi.
\]

Under a gauge transformation

\[
\psi\mapsto e^{i\chi}\psi,
\qquad
\alpha\mapsto \alpha+d\chi,
\]

the derivative \(D_i\psi\) transforms covariantly:

\[
D_i\psi \mapsto e^{i\chi}D_i\psi.
\]

The commutator is

\[
[D_i,D_j]\psi
=
-iF_{ij}\psi.
\]

Thus phase curvature is precisely the obstruction to commuting phase-covariant derivatives.

The phase Laplacian is

\[
\Delta_\alpha\psi
=
g^{ij}D_iD_j\psi.
\]

Expanding,

\[
\Delta_\alpha\psi
=
\Delta\psi
-
i\left(
2\alpha^i\nabla_i\psi
+
(\nabla_i\alpha^i)\psi
\right)
-
|\alpha|^2\psi.
\]

This operator governs phase-twisted diffusion, phase-modulated spectral problems, and gauge-covariant phase evolution.

---

### 5.3 Phase metrics

A central construction in SPG is the deformation of the base metric by phase.

Let \(g_{ij}\) be a metric on \(M\), and let \(\alpha_i\) be a phase one-form. Define the **phase metric**

\[
G_{ij}
=
g_{ij}
+
\kappa^2 \alpha_i\alpha_j,
\]

where \(\kappa\) is a coupling constant measuring the geometric weight of phase.

This metric increases lengths in directions of strong phase variation. If \(v=v^i\partial_i\), then

\[
G(v,v)=g(v,v)+\kappa^2\alpha(v)^2.
\]

Let

\[
|\alpha|_g^2=g^{ij}\alpha_i\alpha_j.
\]

Then the inverse phase metric is

\[
G^{ij}
=
g^{ij}
-
\frac{\kappa^2\alpha^i\alpha^j}
{1+\kappa^2|\alpha|_g^2},
\]

where \(\alpha^i=g^{ij}\alpha_j\).

The determinant satisfies

\[
\det(G_{ij})
=
\det(g_{ij})
\left(
1+\kappa^2|\alpha|_g^2
\right).
\]

Therefore the phase-deformed volume form is

\[
d\operatorname{vol}_G
=
\sqrt{1+\kappa^2|\alpha|_g^2}\,
d\operatorname{vol}_g.
\]

This construction provides a literal geometric interpretation of phase as a coordinate that modifies distance, volume, and geodesic motion.

---

### 5.4 Kaluza–Klein interpretation

The phase metric arises naturally as the pullback of a metric on an extended phase bundle.

Let

\[
\widehat{M}=M\times S^1
\]

with coordinate \(\theta\) on \(S^1\). Let \(A=A_i dx^i\) be a phase connection on \(M\). Define

\[
\widehat{g}
=
g_{ij}dx^idx^j
+
\kappa^2(d\theta + A_i dx^i)^2.
\]

A phase section

\[
s:M\to \widehat{M},
\qquad
s(x)=(x,\varphi(x)),
\]

pulls back \(\widehat{g}\) to

\[
s^*\widehat{g}
=
\left(
g_{ij}
+
\kappa^2(\partial_i\varphi + A_i)(\partial_j\varphi + A_j)
\right)
dx^idx^j.
\]

Thus phase geometry may be understood as the geometry of sections of an extended space in which phase is an explicit coordinate.

This is one of the core conceptual moves of SPG: phase is not a function attached to fields; phase is a coordinate in an enlarged geometric arena.

---

### 5.5 Phase stress-energy

For the pure phase energy

\[
E[\alpha]
=
\frac12\int_M |\alpha|_g^2\,d\operatorname{vol}_g,
\]

the associated stress-energy tensor is

\[
T_{ij}
=
\alpha_i\alpha_j
-
\frac12 g_{ij}|\alpha|_g^2.
\]

If \(\alpha=d\varphi\) and \(\varphi\) is harmonic, then

\[
\nabla^i T_{ij}=0.
\]

For a curved phase connection with field strength \(F_{ij}\), the Maxwell-type phase stress tensor is

\[
T_{ij}
=
F_{ik}F_j{}^k
-
\frac14 g_{ij}F_{kl}F^{kl}.
\]

Its divergence satisfies

\[
\nabla^i T_{ij}
=
F_{ji}J^i,
\]

where

\[
J^i=\nabla_kF^{ki}
\]

is the phase current.

Thus phase geometry possesses its own conservation laws.

---

## 6. Variational Theory of Phase Fields

SPG admits a natural variational formulation.

Let \((M,g)\) be a Riemannian manifold and let \(S\) be a phase target with metric \(h_S\). The phase energy is the harmonic-map functional

\[
E[\Phi]
=
\frac12\int_M |d\Phi|_{g,h_S}^2\,d\operatorname{vol}_g.
\]

For \(S=S^1\), locally \(\Phi=e^{i\varphi}\), and

\[
E[\varphi]
=
\frac12\int_M g^{ij}\partial_i\varphi\,\partial_j\varphi\,d\operatorname{vol}_g.
\]

The Euler–Lagrange equation is

\[
\Delta_g\varphi=0,
\]

where

\[
\Delta_g\varphi
=
\frac{1}{\sqrt{\det g}}
\partial_i
\left(
\sqrt{\det g}\,g^{ij}\partial_j\varphi
\right).
\]

Thus free structural phase fields are harmonic functions modulo periods.

---

### 6.1 Phase with potential

If the phase is subject to a potential \(V:S\to\mathbb{R}\), the action is

\[
E_V[\Phi]
=
\int_M
\left(
\frac12|d\Phi|^2
+
V(\Phi)
\right)
d\operatorname{vol}_g.
\]

For \(S=S^1\), the Euler–Lagrange equation becomes

\[
\Delta_g\varphi = V'(\varphi).
\]

This includes sine-Gordon-type phase equations, Josephson-type models, and phase-locking equations.

---

### 6.2 Phase heat flow

The gradient flow of the phase energy is

\[
\partial_t\varphi = \Delta_g\varphi.
\]

For general phase targets,

\[
\partial_t\Phi = \tau(\Phi),
\]

where \(\tau(\Phi)\) is the tension field of \(\Phi\).

In local coordinates on \(S\),

\[
\tau^A(\Phi)
=
g^{ij}
\left(
\partial_i\partial_j\Phi^A
+
\Gamma^A_{BC}(\Phi)
\partial_i\Phi^B
\partial_j\Phi^C
-
\Gamma^k_{ij}(g)
\partial_k\Phi^A
\right).
\]

This is the intrinsic heat equation for structural phase.

---

### 6.3 Singular phase fields and vortices

Many important phase fields are not globally smooth. A canonical example is a phase with point vortices.

Let \(M\) be two-dimensional and suppose \(\varphi\) has isolated singularities \(p_a\) with integer winding numbers \(n_a\). Then locally around \(p_a\),

\[
\oint_{\partial U_a} d\varphi = 2\pi n_a.
\]

In the sense of currents,

\[
d\alpha
=
2\pi\sum_a n_a\,\delta_{p_a}\,d\operatorname{vol}_M.
\]

Thus phase singularities are curvature concentrations.

This provides a geometric interpretation of vortices, zeros of sections, branch points, and wavefront dislocations.

---

## 7. Canonical Constructions of Structural Phase

We now exhibit several canonical sources of SPG phase.

---

## 7.1 Determinant-line phase

Let \(E\to M\) be a complex vector bundle with connection \(\nabla^E\). Its determinant line is

\[
\det E := \Lambda^{\operatorname{rank}E}E.
\]

The induced connection on \(\det E\) has curvature

\[
F_{\det E}=\operatorname{tr}F_E.
\]

A local nonvanishing section \(s\) of \(\det E\) may be written as

\[
s=|s|e^{i\varphi}.
\]

The phase one-form is

\[
\alpha=d\varphi.
\]

The curvature satisfies

\[
d\alpha = -i\,\operatorname{tr}F_E
\]

up to convention-dependent signs.

Thus every complex vector bundle with connection induces a canonical phase geometry through its determinant line.

This is one of the most general sources of structural phase.

---

## 7.2 Complex geometry and the canonical bundle

Let \((X,J)\) be a complex \(n\)-manifold with Hermitian metric \(g\). The canonical bundle is

\[
K_X := \Lambda^{n,0}X.
\]

Locally, choose a holomorphic volume form

\[
\Omega_U = f_U(z)\,dz^1\wedge\cdots\wedge dz^n.
\]

Write

\[
\Omega_U = |\Omega_U|e^{i\varphi_U}.
\]

Then

\[
\Phi_U=e^{i\varphi_U}
\]

is a local phase field.

The Hermitian metric on \(K_X\) induces a Chern connection. Its imaginary part defines a phase connection \(\alpha\). The curvature of this phase connection is related to the Ricci form \(\rho\) of \(X\):

\[
d\alpha = \pm \rho,
\]

with sign depending on conventions.

Thus the argument of the canonical bundle is a structural phase field whose curvature measures complex geometric curvature.

---

### Special Lagrangian phase condition

Let \((X,\omega,\Omega)\) be a Calabi–Yau manifold with holomorphic volume form \(\Omega\). A Lagrangian submanifold \(L\subset X\) is special Lagrangian with phase \(e^{i\theta}\) if

\[
\omega|_L=0
\]

and

\[
\operatorname{Im}\left(e^{-i\theta}\Omega|_L\right)=0.
\]

Equivalently, the phase of \(\Omega|_L\) is constant:

\[
\arg(\Omega|_L)=\theta.
\]

SPG interprets special Lagrangian submanifolds as phase-calibrated submanifolds: they are geometric loci on which the intrinsic structural phase is constant.

---

## 7.3 Symplectic prequantum phase

Let \((M,\omega)\) be a symplectic manifold such that

\[
[\omega/2\pi]\in H^2(M;\mathbb{Z}).
\]

Then there exists a prequantum line bundle \(L\to M\) with connection \(\nabla\) satisfying

\[
F_\nabla = -i\omega.
\]

A local unit section \(u\) defines a phase one-form \(\alpha\) by

\[
\nabla u = i\alpha\otimes u.
\]

Then

\[
d\alpha = -\omega.
\]

Thus symplectic geometry itself may be viewed as a phase curvature geometry.

This gives SPG a direct bridge to geometric quantization, Hamiltonian mechanics, and prequantum theory.

---

## 7.4 Spectral phase

Let \(D\) be a self-adjoint elliptic operator depending on parameters \(p\in M\). The determinant line of the family \(\{D_p\}\) carries a natural Quillen-type metric and connection. Its phase is a spectral phase.

In odd dimensions, the eta invariant \(\eta(D_p)\) provides a canonical phase

\[
\Phi(p)=\exp(i\pi\eta(D_p)).
\]

The curvature of the associated determinant-line connection is given by local index densities. Thus spectral asymmetry generates an intrinsic phase geometry over parameter space.

This construction links SPG to global analysis, index theory, and analytic torsion.

---

## 8. Application I: Harmonic Analysis and Oscillatory Integrals

One of the most natural domains of phase is harmonic analysis. SPG provides a geometric language for phase functions, stationary phase, and Fourier integral operators.

---

### 8.1 Oscillatory integrals

Consider an oscillatory integral

\[
I(\lambda)
=
\int_M a(x)e^{i\lambda\varphi(x)}\,dx,
\]

where

- \(a\in C_c^\infty(M)\) is an amplitude,
- \(\varphi:M\to\mathbb{R}\) is a real phase function,
- \(\lambda\gg 1\) is a large frequency parameter.

The phase one-form is

\[
\alpha=d\varphi.
\]

The critical set of the phase is

\[
C_\varphi = \{x\in M: d\varphi(x)=0\}.
\]

Geometrically, \(C_\varphi\) is the zero locus of the phase one-form.

---

### 8.2 Stationary phase theorem in SPG form

Suppose \(C_\varphi\) consists of isolated nondegenerate critical points. Let

\[
H_x = \operatorname{Hess}_x\varphi
\]

be the Hessian of \(\varphi\) at \(x\). Then as \(\lambda\to\infty\),

\[
I(\lambda)
\sim
\left(\frac{2\pi}{\lambda}\right)^{n/2}
\sum_{x\in C_\varphi}
a(x)
\frac{
e^{i\lambda\varphi(x)+i\frac{\pi}{4}\operatorname{sgn}H_x}
}{
\sqrt{|\det H_x|}
}
+
O(\lambda^{-\infty}).
\]

SPG interprets this as a local curvature expansion of phase geometry. The Hessian \(H_x\) is the local transverse phase curvature. The signature \(\operatorname{sgn}H_x\) is a phase Maslov-type invariant.

For a critical submanifold \(C\subset M\) with nondegenerate normal Hessian, the stationary phase expansion becomes

\[
I(\lambda)
\sim
\left(\frac{2\pi}{\lambda}\right)^{(n-\dim C)/2}
\int_C
a(x)
e^{i\lambda\varphi(x)+i\frac{\pi}{4}\operatorname{ind}H_x}
\frac{d\operatorname{vol}_C(x)}
{\sqrt{|\det H_x^\perp|}}
+
\cdots.
\]

Thus stationary phase is a theorem about the local geometry of phase critical sets.

---

### 8.3 Fourier integral operators

Let \(X,Y\) be manifolds. A Fourier integral operator has the local form

\[
(Au)(x)
=
\int_{\mathbb{R}^N}
\int_Y
e^{i\varphi(x,\theta)-iy\cdot\theta}
a(x,y,\theta)
u(y)\,dy\,d\theta,
\]

where \(\varphi(x,\theta)\) is a phase function.

The phase one-form in the \(x\)-variables is

\[
\alpha_x = d_x\varphi.
\]

The canonical relation associated with \(A\) is

\[
C_A
=
\{
(x,d_x\varphi(x,\theta)):
d_\theta\varphi(x,\theta)=0
\}
\subset T^*X.
\]

Under suitable nondegeneracy, \(C_A\) is a Lagrangian submanifold. Thus the phase function generates a Lagrangian geometry.

SPG regards the phase \(\varphi\) as a structural coordinate whose differential determines the canonical relation. The geometry of the operator is encoded in the geometry of phase.

---

## 9. Application II: Wave Mathematics and High-Frequency Propagation

Wave propagation is governed by phase at high frequency. SPG gives a coordinate-free formulation of eikonal and transport equations.

---

### 9.1 Scalar high-frequency ansatz

Let \(u\) solve the Helmholtz-type equation

\[
(\Delta_g + \omega^2 n^2)u=0,
\]

where \(n(x)\) is a refractive index and \(\omega\gg1\).

Use the ansatz

\[
u(x)=a(x)e^{i\omega\Phi(x)}.
\]

Then

\[
\nabla u
=
e^{i\omega\Phi}
\left(
i\omega a\nabla\Phi+\nabla a
\right),
\]

and

\[
\Delta u
=
e^{i\omega\Phi}
\left[
-\omega^2 a|\nabla\Phi|^2
+
i\omega(2\nabla\Phi\cdot\nabla a + a\Delta\Phi)
+
\Delta a
\right].
\]

Substitution gives

\[
-\omega^2 a|\nabla\Phi|^2
+
\omega^2 n^2 a
+
i\omega(2\nabla\Phi\cdot\nabla a+a\Delta\Phi)
+
\Delta a
=0.
\]

Equating powers of \(\omega\) yields the leading equations.

---

### 9.2 Eikonal equation

At order \(\omega^2\),

\[
|\nabla\Phi|_g^2=n^2.
\]

In components,

\[
g^{ij}\partial_i\Phi\,\partial_j\Phi=n^2.
\]

This is the eikonal equation. The phase gradient defines wave covectors

\[
p_i = \partial_i\Phi.
\]

The associated Hamiltonian is

\[
H(x,p)=\frac12\left(g^{ij}p_ip_j-n^2(x)\right).
\]

Phase rays are the Hamiltonian trajectories

\[
\dot{x}^i = \frac{\partial H}{\partial p_i}
=
g^{ij}p_j,
\]

\[
\dot{p}_i = -\frac{\partial H}{\partial x^i}
=
\frac12\partial_i n^2
-
\frac12\partial_i g^{jk}p_jp_k.
\]

Thus phase geometry produces ray geometry.

---

### 9.3 Transport equation

At order \(\omega\),

\[
2\nabla\Phi\cdot\nabla a + a\Delta\Phi=0.
\]

Equivalently,

\[
\nabla_i(a^2\nabla^i\Phi)=0.
\]

This is the conservation of phase flux. SPG interprets it as a continuity equation for the phase current

\[
J^i=a^2\nabla^i\Phi.
\]

---

### 9.4 Lorentzian wave equations

For a Lorentzian metric \(g\), consider the wave equation

\[
\square_g u=0.
\]

With

\[
u=a e^{i\omega\Phi},
\]

the leading eikonal equation is

\[
g^{ij}\partial_i\Phi\,\partial_j\Phi=0.
\]

The phase hypersurfaces

\[
\Phi=\text{constant}
\]

are null hypersurfaces. The transport equation is

\[
2\nabla^i\Phi\nabla_i a + a\square_g\Phi=0.
\]

Thus in geometric wave propagation, phase is the coordinate whose level sets define characteristic surfaces.

---

### 9.5 Phase curvature along rays

Let

\[
B_{ij}=\nabla_j\alpha_i
\]

be the phase deformation tensor, where \(\alpha=d\Phi\). Along a ray with tangent vector

\[
k^i=\nabla^i\Phi,
\]

one obtains a Riccati-type evolution equation of the form

\[
k^k\nabla_k B_{ij}
+
B_i{}^k B_{kj}
+
R_{ikj\ell}k^k k^\ell
=
0
\]

in appropriate geometric settings. This equation governs caustics, focusing, and phase-front curvature.

SPG therefore treats wavefront propagation as the geometry of phase congruences.

---

## 10. Application III: Complex Geometry and Phase Vortices

Complex geometry is saturated with intrinsic phase.

---

### 10.1 Argument of holomorphic functions

Let \(f\) be a holomorphic function on a domain \(U\subset\mathbb{C}\). Away from zeros,

\[
f=|f|e^{i\varphi}.
\]

The phase one-form is

\[
\alpha=d\varphi.
\]

For a small loop \(\gamma\) enclosing a zero of order \(m\),

\[
\oint_\gamma \alpha = 2\pi m.
\]

In the sense of currents,

\[
d\alpha = 2\pi\sum_{p\in Z(f)} m_p\delta_p.
\]

If \(f\) is meromorphic, zeros contribute positively and poles negatively:

\[
d\alpha
=
2\pi
\left(
\sum_{p\in Z(f)}m_p\delta_p
-
\sum_{q\in P(f)}n_q\delta_q
\right).
\]

This is the differential-geometric form of the argument principle.

SPG interprets zeros and poles as phase vortices.

---

### 10.2 Holomorphic line bundles

Let \(L\to X\) be a Hermitian holomorphic line bundle with Chern connection \(\nabla\). A local holomorphic section \(s\) has phase

\[
s=|s|e^{i\varphi}.
\]

The connection one-form in the unit frame is

\[
\nabla \frac{s}{|s|}
=
i\alpha\otimes \frac{s}{|s|}.
\]

The curvature satisfies

\[
F_\nabla=i\,d\alpha.
\]

Thus the Chern curvature is the curvature of the intrinsic phase connection.

The first Chern class is

\[
c_1(L)=\left[\frac{i}{2\pi}F_\nabla\right].
\]

Hence phase curvature represents the topology of the holomorphic line bundle.

---

### 10.3 Phase of the canonical bundle and Ricci curvature

As noted above, on a complex manifold \(X\), the canonical bundle \(K_X\) carries a natural phase. Its curvature is related to the Ricci form.

If \(X\) is Calabi–Yau, then \(K_X\) is holomorphically trivial. A global holomorphic volume form \(\Omega\) determines a global phase field

\[
\Phi(x)=\arg\Omega_x
\]

after choosing a reference phase. The condition that a Lagrangian submanifold be special Lagrangian is precisely the condition that the phase of \(\Omega\) restrict to a constant.

Thus calibrated geometry may be formulated as phase rigidity.

---

## 11. Application IV: Dynamical Systems and Phase Coordinates

Dynamical systems provide another canonical source of structural phase.

---

### 11.1 Phase of a periodic orbit

Let \(X\) be a vector field on \(M\) with a stable periodic orbit \(\Gamma\) of period \(T\). A phase coordinate is a function

\[
\varphi:U\to S^1
\]

defined on a neighborhood \(U\) of \(\Gamma\), satisfying

\[
X\varphi = \omega,
\]

where

\[
\omega=\frac{2\pi}{T}.
\]

On the orbit,

\[
\varphi(\gamma(t)) = \omega t \pmod{2\pi}.
\]

The level sets of \(\varphi\) are called isochrons.

SPG regards \(\varphi\) as a structural phase coordinate induced by the flow.

---

### 11.2 Invariant tori and angle variables

For an integrable Hamiltonian system with action-angle coordinates \((I_a,\theta^a)\), the symplectic form is

\[
\Omega = dI_a\wedge d\theta^a.
\]

The Hamiltonian \(H(I)\) yields

\[
\dot{\theta}^a = \frac{\partial H}{\partial I_a} = \omega^a(I).
\]

The angles \(\theta^a\) are phase coordinates on the invariant torus

\[
T^r = \mathbb{R}^r/(2\pi\mathbb{Z})^r.
\]

The phase map is

\[
\Phi:M\to T^r,
\qquad
\Phi=(\theta^1,\dots,\theta^r).
\]

Thus integrable dynamics naturally produces toroidal phase geometry.

---

### 11.3 Koopman eigenfunctions

Let \(\varphi_t\) be a flow and let \(U_t\) be the Koopman operator,

\[
(U_t f)(x)=f(\varphi_t(x)).
\]

Suppose \(\psi\) is a Koopman eigenfunction:

\[
U_t\psi=e^{i\lambda t}\psi.
\]

Writing

\[
\psi=|\psi|e^{i\varphi},
\]

we obtain

\[
X\varphi=\lambda,
\]

where \(X\) is the generator of the flow.

Thus Koopman eigenfunctions induce structural phase coordinates.

---

### 11.4 Phase response geometry

For a perturbed oscillator

\[
\dot{x}=F(x)+\varepsilon p(x,t),
\]

the phase evolution satisfies, to first order,

\[
\dot{\varphi}
=
\omega
+
\varepsilon Z(\varphi)\cdot p(\gamma(\varphi),t),
\]

where

\[
Z(\varphi)=\nabla_x\varphi|_{x=\gamma(\varphi)}
\]

is the phase response curve.

Geometrically, \(Z\) is the dual one-form to the phase foliation. SPG treats phase response as the differential geometry of the phase coordinate.

---

## 12. Phase Unwrapping and Cohomology

A common analytic problem is to recover a global phase function from a phase one-form. SPG gives a clean Hodge-theoretic formulation.

Let \(\alpha\in\Omega^1(M)\) be a measured or induced phase one-form. We seek \(\varphi\) such that

\[
\alpha \approx d\varphi.
\]

The obstruction is the cohomology class

\[
[\alpha]\in H^1(M;\mathbb{R})
\]

or, for circle-valued phase,

\[
[\alpha/2\pi]\in H^1(M;\mathbb{Z}).
\]

If \(M\) is compact Riemannian, the Hodge decomposition gives

\[
\alpha = d\varphi + \delta\beta + h,
\]

where \(h\) is harmonic. The best \(L^2\)-phase unwrap is obtained by solving

\[
\Delta_g\varphi = d^*\alpha.
\]

The residual

\[
\alpha-d\varphi
\]

contains the harmonic and cohomological phase content.

Thus phase unwrapping is not merely an algorithmic task; it is a problem in Hodge theory and geometric topology.

---

## 13. Nonlinear Phase Equations

SPG naturally supports nonlinear phase field equations.

---

### 13.1 Sine-Gordon phase equation

For \(S=S^1\) with potential

\[
V(\varphi)=1-\cos\varphi,
\]

the Euler–Lagrange equation is

\[
\Delta_g\varphi = \sin\varphi.
\]

In Lorentzian signature,

\[
\square_g\varphi = \sin\varphi.
\]

This is a geometric phase equation with solitonic solutions.

---

### 13.2 Ginzburg–Landau phase vortices

Let \(\psi:M\to\mathbb{C}\) be an order parameter. The Ginzburg–Landau energy is

\[
E_\varepsilon[\psi]
=
\int_M
\left(
\frac12|d\psi|^2
+
\frac{1}{4\varepsilon^2}(1-|\psi|^2)^2
\right)
d\operatorname{vol}_g.
\]

Writing

\[
\psi=|\psi|e^{i\varphi},
\]

the phase \(\varphi\) becomes singular at zeros of \(\psi\). As \(\varepsilon\to0\), vortices concentrate and the phase curvature converges to a sum of delta currents.

SPG provides the geometric limit:

\[
d\alpha \longrightarrow 2\pi\sum_a n_a\delta_{p_a}.
\]

Thus topological defects are curvature singularities of structural phase.

---

## 14. Phase Curvature and Topology

The topology of phase is encoded in characteristic classes.

For a \(U(1)\)-phase bundle with curvature \(F\),

\[
c_1 = \left[\frac{F}{2\pi}\right]\in H^2(M;\mathbb{Z}).
\]

If \(c_1\neq0\), no global phase function exists.

For circle-valued phase maps \(\Phi:M\to S^1\), the pullback of the generator of \(H^1(S^1;\mathbb{Z})\) gives

\[
[\Phi]\in H^1(M;\mathbb{Z}).
\]

Thus SPG has both degree-one phase topology, associated with winding, and degree-two phase curvature topology, associated with bundle curvature.

These two levels correspond to:

- phase winding around loops,
- phase curvature through surfaces.

Both are geometric invariants of structure.

---

## 15. Phase Geometry and Interference

Interference is the physical phenomenon most commonly associated with phase, but SPG reveals it as a purely geometric operation.

Let two phase fields \(\Phi_1,\Phi_2:M\to S^1\) have amplitudes \(a_1,a_2\). The squared magnitude of their sum is

\[
|a_1e^{i\varphi_1}+a_2e^{i\varphi_2}|^2
=
a_1^2+a_2^2+2a_1a_2\cos(\varphi_1-\varphi_2).
\]

The interference term depends only on the relative phase

\[
\Delta\varphi=\varphi_1-\varphi_2.
\]

The relative phase one-form is

\[
\Delta\alpha = \alpha_1-\alpha_2.
\]

Thus interference is governed by the geometry of phase differences.

In SPG, the relative phase is itself a phase field

\[
\Delta\Phi:M\to S^1.
\]

Its curvature is

\[
\Delta F = F_1-F_2.
\]

Therefore interference patterns are curvature-sensitive geometric objects.

---

## 16. Structural Phase Flow

We may define a geometric flow on phase metrics.

Given

\[
G_{ij}=g_{ij}+\kappa^2\alpha_i\alpha_j,
\]

one can evolve the base metric by phase-deformed Ricci flow:

\[
\partial_t g_{ij}
=
-2\operatorname{Ric}_{ij}(G).
\]

Alternatively, one can evolve the phase one-form by phase heat flow:

\[
\partial_t\alpha = d\Delta_g\varphi
\]

when \(\alpha=d\varphi\), or more generally by Yang–Mills phase flow:

\[
\partial_t A = -d^*F_A.
\]

These flows suggest a broader program: **phase geometric flows**, in which phase curvature and phase metric coevolve.

---

## 17. Nonabelian Phase Geometry

The present paper has focused on \(U(1)\)-phase. The nonabelian extension is natural.

Let \(G\) be a compact Lie group and let

\[
\Phi:M\to G
\]

or

\[
\Phi:M\to G/H
\]

be a nonabelian phase field. The Maurer–Cartan form

\[
\Theta = \Phi^{-1}d\Phi
\]

is a \(\mathfrak{g}\)-valued one-form. It satisfies

\[
d\Theta + \frac12[\Theta,\Theta]=0.
\]

The curvature of a nonabelian phase connection \(A\) is

\[
F_A=dA+\frac12[A,A].
\]

Nonabelian SPG is relevant for:

- Wilczek–Zee phases,
- holonomy in vector bundles,
- nonabelian Berry connections,
- gauge-theoretic moduli spaces.

The abelian theory developed above is the first layer of this broader structure.

---

## 18. Computational Phase Geometry

SPG suggests computational methods based on phase geometry.

### 18.1 Phase curvature estimation

Given a discrete phase field on a mesh or graph, one may estimate curvature by computing discrete holonomies around elementary loops:

\[
\operatorname{Hol}_{\partial\sigma}
=
\exp\left(i\sum_{e\in\partial\sigma}\alpha_e\right).
\]

The logarithm gives discrete curvature flux.

### 18.2 Phase unwrapping by Hodge decomposition

On a discrete manifold, solve

\[
\Delta\varphi = d^*\alpha
\]

to obtain the curl-free component of phase. The harmonic remainder detects topological phase content.

### 18.3 Phase geodesics

Given a phase metric

\[
G_{ij}=g_{ij}+\kappa^2\alpha_i\alpha_j,
\]

one can compute geodesics of \(G\) to identify paths that are natural with respect to phase variation.

These methods may be useful in signal processing, image analysis, wavefront reconstruction, and dynamical-systems data.

---

## 19. Research Program and Open Problems

SPG suggests several directions for further development.

### Problem 19.1: Classification of phase functors

Classify natural phase assignments

\[
\mathscr{P}:\mathbf{Struct}\to\mathbf{PhaseGeom}
\]

for standard categories of geometric structures.

The Character-Phase Theorem provides one class. The full classification likely involves determinant functors, index-theoretic invariants, and higher categorical characters.

---

### Problem 19.2: Phase Ricci flow

Develop the flow

\[
\partial_t g_{ij}=-2\operatorname{Ric}_{ij}(G)
\]

for phase metrics

\[
G_{ij}=g_{ij}+\kappa^2\alpha_i\alpha_j.
\]

Does phase curvature regularize singularities? Are there canonical phase-calibrated limits?

---

### Problem 19.3: Singular phase geometry

Give a systematic theory of phase currents, phase vortices, and phase stratifications.

The fundamental equation is

\[
d\alpha = J_\Phi,
\]

where \(J_\Phi\) is a current supported on phase defects.

---

### Problem 19.4: Nonabelian SPG

Extend the abelian theory to nonabelian phase targets and classify nonabelian phase obstructions.

---

### Problem 19.5: Spectral phase geometry

Develop a comprehensive theory of phase induced by families of operators, including determinant-line connections, eta invariants, and analytic torsion phases.

---

### Problem 19.6: Phase geometry in harmonic analysis

Characterize Fourier integral operators and oscillatory integral operators through intrinsic phase geometries. Develop phase-invariant symbol classes and phase curvature estimates for \(L^p\) bounds.

---

### Problem 19.7: Phase coordinates in dynamical systems

Construct global phase coordinates for attractors, normally hyperbolic invariant manifolds, and quasiperiodic systems. Relate phase curvature to phase response and synchronization.

---

## 20. Conclusion

Structural Phase Geometry proposes a fundamental reorganization of the role of phase in mathematics. Phase is not an aftereffect of representation, nor a mere argument of a complex number. It is a geometric coordinate induced by structure.

The central object is the phase field

\[
\Phi:M\to S,
\]

together with its pullback phase one-form,

\[
\alpha=\Phi^*\vartheta,
\]

its curvature,

\[
F=d\alpha,
\]

and its associated phase metric,

\[
G_{ij}=g_{ij}+\kappa^2\alpha_i\alpha_j.
\]

Through phase bundles, gauge transformations, and characteristic classes, SPG captures global obstructions to phase trivialization. Through variational principles, it yields harmonic phase fields, phase heat flows, and phase vortices. Through applications, it unifies stationary phase in harmonic analysis, eikonal propagation in wave mathematics, argument geometry in complex manifolds, and angle coordinates in dynamical systems.

The theory suggests a broad principle:

> **Wherever mathematical structure admits a natural oscillatory, complex, spectral, or rotational interpretation, it also admits an intrinsic phase geometry.**

Structural Phase Geometry is the study of that phase as a coordinate of structure itself.

---

## References

1. M. F. Atiyah, V. K. Patodi, and I. M. Singer, *Spectral asymmetry and Riemannian geometry*, Bulletin of the London Mathematical Society, 1973.

2. V. I. Arnold, *Mathematical Methods of Classical Mechanics*, Springer.

3. M. V. Berry, *Quantal phase factors in adiabatic changes*, Proceedings of the Royal Society A, 1984.

4. S. Kobayashi, *Differential Geometry of Complex Vector Bundles*, Princeton University Press.

5. L. Hörmander, *The Analysis of Linear Partial Differential Operators IV*, Springer.

6. J. J. Duistermaat, *Fourier Integral Operators*, Birkhäuser.

7. D. McDuff and D. Salamon, *Introduction to Symplectic Topology*, Oxford University Press.

8. J. Jost, *Riemannian Geometry and Geometric Analysis*, Springer.

9. A. Hatcher, *Algebraic Topology*, Cambridge University Press.

10. F. R. Harvey and H. B. Lawson, *Calibrated geometries*, Acta Mathematica, 1982.

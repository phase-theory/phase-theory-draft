# Relativity 11.0 — Celestial and Asymptotic Relativity  
## Scattering, Infinite Symmetries, and Holography at Null Infinity

**White paper / academic preprint**

---

## Abstract

Celestial and Asymptotic Relativity is the reformulation of gravitational scattering in terms of observables defined at null infinity. In asymptotically flat spacetimes, the natural boundary of spacetime is not spatial infinity but future and past null infinity, \(\mathscr{I}^+\) and \(\mathscr{I}^-\). At null infinity, the asymptotic symmetry group of general relativity is not merely the Poincaré group. It is the Bondi–Metzner–Sachs group, enlarged by supertranslations and superrotations. These infinite-dimensional symmetries are not mathematical curiosities. They are equivalent to soft graviton theorems, gravitational memory effects, and Ward identities of a holographic theory living on the celestial sphere.

In the celestial formulation, ordinary momentum-space scattering amplitudes,

\[
\mathcal{A}(p_i),
\]

are Mellin transformed into boost eigenamplitudes,

\[
\widetilde{\mathcal{A}}
=
\int
\prod_i d\omega_i\,
\omega_i^{\Delta_i-1}
\mathcal{A}(\omega_i,z_i,\bar z_i),
\]

which transform as correlation functions of a two-dimensional conformal field theory on the celestial sphere,

\[
\widetilde{\mathcal{A}}
=
\left\langle
\prod_i
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle.
\]

The Lorentz group acts as the global conformal group of the celestial sphere. Soft gravitons become conformally soft operators. The infrared structure of gravity becomes an infinite-dimensional symmetry algebra. The gravitational memory effect becomes a transition between degenerate vacua. The resulting framework may be summarized by the infrared triangle:

\[
\boxed{
\text{soft theorems}
\quad
\leftrightarrow
\quad
\text{asymptotic symmetries}
\quad
\leftrightarrow
\quad
\text{memory effects}.
}
\]

Relativity 11.0 is therefore a holographic relativity of asymptotically flat spacetime: the S-matrix is recast as celestial correlators, locality in the bulk is encoded in conformal data on the sphere, and Einstein’s theory reveals an infinite symmetry structure hidden at null infinity.

---

## 1. Introduction

The S-matrix has long been the central observable of scattering theory. In Minkowski spacetime, one prepares incoming particles at past infinity, evolves them through an interaction region, and measures outgoing particles at future infinity. The amplitude is usually written as a function of asymptotic momenta,

\[
\mathcal{A}(p_1,\ldots,p_n).
\]

This formulation is natural for particle physics, but it obscures deep structures of gravity.

Gravitational scattering is qualitatively different from nongravitational scattering. Because the graviton is massless, every scattering process emits infinitely many arbitrarily soft gravitons. The conventional S-matrix between bare Fock states is infrared divergent. More profoundly, gravity possesses an infinite-dimensional asymptotic symmetry group at null infinity. These symmetries act on the gravitational vacuum and are responsible for universal soft behavior and permanent memory effects.

Celestial and Asymptotic Relativity reorganizes scattering theory around these facts.

Instead of using momentum eigenstates, one uses boost eigenstates. Instead of amplitudes as functions of energies and angles, one uses celestial amplitudes as functions of conformal dimensions and points on the celestial sphere. Instead of treating soft gravitons as infrared nuisances, one treats them as symmetry generators.

The central claim is:

\[
\boxed{
\text{Flat-space quantum gravity is holographically encoded on the celestial sphere.}
}
\]

This is Relativity 11.0.

---

## 2. Null Infinity and the Asymptotic Structure of Spacetime

In asymptotically flat spacetime, the natural boundary for radiation is null infinity.

Introduce retarded time

\[
u = t-r,
\]

and spherical coordinates on the celestial sphere. A convenient complex coordinate is

\[
z = e^{i\phi}\cot\frac{\theta}{2}.
\]

The metric on the unit sphere is

\[
d\Omega^2
=
2\gamma_{z\bar z}dz d\bar z,
\]

with

\[
\gamma_{z\bar z}
=
\frac{2}{(1+z\bar z)^2}.
\]

Future null infinity, \(\mathscr{I}^+\), is the hypersurface approached by outgoing light rays as

\[
r\to\infty
\quad
\text{with}
\quad
u
\quad
\text{fixed}.
\]

Its coordinates are

\[
(u,z,\bar z).
\]

Similarly, past null infinity \(\mathscr{I}^-\) is described by advanced time

\[
v=t+r.
\]

Null infinity is not a timelike boundary, as in anti-de Sitter space. It is a null boundary. This makes flat-space holography structurally different from AdS/CFT.

---

## 3. Bondi Gauge and the Radiative Data

In Bondi gauge, the asymptotically flat metric near \(\mathscr{I}^+\) takes the form

\[
ds^2
=
-du^2
-
2du\,dr
+
r^2
2\gamma_{z\bar z}dz d\bar z
+
\frac{2m_B}{r}du^2
+
r C_{zz}dz^2
+
r C_{\bar z\bar z}d\bar z^2
+
\cdots .
\]

The leading radiative degree of freedom is the shear tensor

\[
C_{zz}(u,z,\bar z).
\]

Its retarded-time derivative is the Bondi news tensor,

\[
N_{zz}
=
\partial_u C_{zz}.
\]

The news measures gravitational radiation. When

\[
N_{zz}=0,
\]

no gravitational waves are present at leading order.

The function

\[
m_B(u,z,\bar z)
\]

is the Bondi mass aspect. Its evolution is governed by the mass-loss formula,

\[
\partial_u m_B
=
-
\frac{1}{4}
N_{zz}N^{zz}
-
4\pi G T_{uu}^{\text{matter}}.
\]

This equation says that gravitational radiation carries away energy.

The Einstein equations near null infinity become evolution equations and constraint equations on the celestial sphere. Thus the dynamics of bulk gravity is encoded in data living at \(\mathscr{I}^+\).

---

## 4. The BMS Group

The asymptotic symmetry group of asymptotically flat gravity is the Bondi–Metzner–Sachs group.

The BMS group contains:

1. ordinary Lorentz transformations,
2. supertranslations,
3. superrotations.

A general BMS transformation acts asymptotically as

\[
u'
=
K(z,\bar z)
\left[
u+\alpha(z,\bar z)
\right],
\]

\[
z'
=
f(z),
\]

where:

- \(\alpha(z,\bar z)\) is an arbitrary smooth function on the sphere,
- \(f(z)\) is a conformal transformation of the sphere,
- \(K(z,\bar z)\) is the conformal factor associated with \(f\).

### 4.1 Supertranslations

Supertranslations are angle-dependent translations along null infinity:

\[
u \to u+\alpha(z,\bar z).
\]

Ordinary time translations are the \(\ell=0\) mode. Spatial translations are the \(\ell=1\) modes. The higher spherical harmonics are genuine supertranslations.

Thus the translation group is enlarged from four dimensions to an infinite-dimensional function space on \(S^2\).

### 4.2 Superrotations

Superrotations extend the Lorentz group. Locally, they are generated by meromorphic conformal vector fields on the sphere,

\[
Y^z(z)\partial_z
+
Y^{\bar z}(\bar z)\partial_{\bar z}.
\]

The global subset with

\[
Y^z(z)=a+bz+cz^2
\]

generates the ordinary Lorentz group \(SL(2,\mathbb{C})\). The full local algebra is two copies of the Witt algebra, or, quantum mechanically, the Virasoro algebra.

Thus the Lorentz group is enlarged to an infinite-dimensional conformal symmetry on the celestial sphere.

---

## 5. BMS Algebra

Let \(T_\alpha\) denote a supertranslation and \(L_Y\) a superrotation. The algebra has the schematic form

\[
[T_\alpha,T_\beta]
=
0,
\]

\[
[L_Y,T_\alpha]
=
T_{Y(\alpha)},
\]

\[
[L_Y,L_Z]
=
L_{[Y,Z]}
+
\text{central extension}.
\]

The supertranslations form an abelian ideal. The superrotations act on them. Quantum mechanically, the superrotation algebra may acquire a central charge.

The appearance of a Virasoro-like structure is one of the central clues behind celestial holography.

---

## 6. Asymptotic Charges and Flux Laws

Every asymptotic symmetry has an associated conserved charge.

For a supertranslation parameter \(\alpha(z,\bar z)\) and a superrotation parameter \(Y^z(z)\), the BMS charge at \(\mathscr{I}^+\) takes the schematic form

\[
Q_{\alpha,Y}
=
\frac{1}{4\pi G}
\int d^2z\,
\gamma_{z\bar z}
\left[
\alpha m_B
+
Y^z
\left(
N_z+u\partial_z m_B
\right)
+
Y^{\bar z}
\left(
N_{\bar z}+u\partial_{\bar z}m_B
\right)
\right].
\]

Here \(N_z\) is the angular momentum aspect.

The charges are not absolutely conserved in the presence of radiation. They satisfy flux-balance laws:

\[
Q_{\alpha,Y}(u=+\infty)
-
Q_{\alpha,Y}(u=-\infty)
=
\text{radiative flux}.
\]

The flux is built from the Bondi news \(N_{zz}\).

Thus asymptotic symmetries relate early-time and late-time gravitational data through the radiation emitted during scattering.

---

## 7. Soft Graviton Theorems

Soft theorems describe the universal behavior of scattering amplitudes when a graviton becomes soft.

Let \(\mathcal{M}_{n+1}\) be an amplitude with \(n\) hard particles and one additional graviton of momentum \(q^\mu\) and polarization \(\varepsilon_{\mu\nu}\). In the soft limit,

\[
q^\mu \to 0,
\]

one has

\[
\mathcal{M}_{n+1}
=
\left[
S^{(0)}
+
S^{(1)}
+
S^{(2)}
+
\mathcal{O}(q^2)
\right]
\mathcal{M}_n.
\]

The leading soft factor is

\[
S^{(0)}
=
\frac{\kappa}{2}
\sum_{k=1}^n
\eta_k
\frac{
\varepsilon_{\mu\nu}
p_k^\mu p_k^\nu
}{
p_k\cdot q
},
\]

where

\[
\kappa=\sqrt{32\pi G},
\]

and \(\eta_k=+1\) for outgoing particles and \(-1\) for incoming particles.

The subleading soft factor is

\[
S^{(1)}
=
-
\frac{i\kappa}{2}
\sum_{k=1}^n
\eta_k
\frac{
\varepsilon_{\mu\nu}
q_\rho
J_k^{\rho\mu}
p_k^\nu
}{
p_k\cdot q
},
\]

where \(J_k^{\rho\mu}\) is the total angular momentum operator acting on particle \(k\).

The subsubleading soft factor is

\[
S^{(2)}
=
-
\frac{\kappa}{4}
\sum_{k=1}^n
\eta_k
\frac{
\varepsilon_{\mu\nu}
q_\rho q_\sigma
J_k^{\rho\mu}
J_k^{\sigma\nu}
}{
p_k\cdot q
}.
\]

These soft factors are universal. They do not depend on the detailed dynamics of the hard scattering.

---

## 8. Soft Theorems as Ward Identities

The central discovery of asymptotic relativity is that soft graviton theorems are Ward identities of BMS symmetry.

Schematically,

\[
\boxed{
\text{soft graviton theorem}
=
\text{BMS Ward identity}.
}
\]

The charge associated with an asymptotic symmetry may be decomposed into a soft part and a hard part:

\[
Q
=
Q_{\text{soft}}
+
Q_{\text{hard}}.
\]

The soft charge creates or annihilates zero-energy gravitons. The hard charge acts on finite-energy particles.

The Ward identity is

\[
\langle \text{out}|
\left(
Q_{\text{soft}}^+
+
Q_{\text{hard}}^+
\right)
S
|\text{in}\rangle
=
0.
\]

When evaluated, this identity reproduces Weinberg’s leading soft graviton theorem.

The subleading soft graviton theorem is related to superrotation symmetry. The precise status of subsubleading soft theorems is more subtle, but they are also connected to extended asymptotic structures.

Thus the infrared behavior of gravity is not accidental. It is symmetry-controlled.

---

## 9. Gravitational Memory

The gravitational memory effect is the physical observable associated with soft gravitons and BMS supertranslations.

Suppose a burst of gravitational radiation passes through a detector. The relative displacement of freely falling test masses changes permanently.

Let \(C_{zz}\) be the Bondi shear. The memory is

\[
\Delta C_{zz}
=
C_{zz}(u=+\infty)
-
C_{zz}(u=-\infty).
\]

Using

\[
N_{zz}
=
\partial_u C_{zz},
\]

one has

\[
\Delta C_{zz}
=
\int_{-\infty}^{+\infty}
du\,
N_{zz}.
\]

This integral is controlled by the zero-frequency limit of the radiative gravitational field.

For two nearby test masses separated by a vector \(s^A\) on the sphere, the permanent displacement is schematically

\[
\Delta s^A
=
\frac{1}{2}
\Delta C^A{}_B
s^B.
\]

Thus spacetime does not return to its original configuration after radiation passes.

The vacuum is not unique. It remembers.

---

## 10. Degenerate Gravitational Vacua

In ordinary field theory, the vacuum is usually unique. In asymptotically flat gravity, the situation is different.

A vacuum state at null infinity is a configuration with no news:

\[
N_{zz}=0.
\]

But there are infinitely many such configurations, labeled by supertranslation fields \(C(z,\bar z)\). Under a supertranslation,

\[
C_{zz}
\to
C_{zz}
-
2D_z^2\alpha.
\]

Thus supertranslations move one vacuum into another physically distinct vacuum.

The gravitational vacuum is therefore degenerate:

\[
\boxed{
\text{BMS supertranslations generate a family of degenerate vacua.}
}
\]

Soft gravitons are the Goldstone modes associated with this vacuum degeneracy.

The memory effect is a transition between vacua:

\[
|0_{\text{in}}\rangle
\to
|0_{\text{out}}\rangle.
\]

This gives the infrared triangle a physical interpretation:

\[
\text{soft graviton}
=
\text{Goldstone boson}
=
\text{memory}.
\]

---

## 11. The Infrared Triangle

The three corners of the infrared triangle are:

1. soft theorems,
2. asymptotic symmetries,
3. memory effects.

They are equivalent descriptions of the same physics.

\[
\begin{array}{ccc}
\text{soft theorems} & \longleftrightarrow & \text{asymptotic symmetries} \\
\downarrow & & \downarrow \\
\text{memory effects} & \longleftrightarrow & \text{vacuum transitions}
\end{array}
\]

The soft theorem is the momentum-space statement.

The asymptotic symmetry is the charge-based statement.

The memory effect is the observable spacetime statement.

The vacuum transition is the quantum-state statement.

Together they define the infrared structure of quantum gravity.

---

## 12. Celestial Sphere and Momentum Parametrization

To formulate celestial amplitudes, one parametrizes null momenta using coordinates on the celestial sphere.

For a massless particle, write

\[
p^\mu
=
\varepsilon \omega q^\mu(z,\bar z),
\]

where:

- \(\omega>0\) is the energy,
- \(\varepsilon=+1\) for outgoing and \(-1\) for incoming,
- \(q^\mu(z,\bar z)\) is a null vector pointing toward \((z,\bar z)\).

A convenient parametrization is

\[
q^\mu(z,\bar z)
=
\frac{1}{1+z\bar z}
\left(
1+z\bar z,
z+\bar z,
-i(z-\bar z),
1-z\bar z
\right).
\]

The celestial sphere is therefore the space of null directions.

The Lorentz group \(SL(2,\mathbb{C})\) acts on \(z\) by Möbius transformations:

\[
z
\to
\frac{az+b}{cz+d},
\qquad
ad-bc=1.
\]

Thus Lorentz transformations are global conformal transformations of the celestial sphere.

---

## 13. Mellin Transform to the Celestial Basis

Ordinary scattering amplitudes are functions of energies and directions:

\[
\mathcal{M}_n
=
\mathcal{M}_n(\omega_i,z_i,\bar z_i).
\]

The celestial amplitude is obtained by Mellin transforming each external energy:

\[
\widetilde{\mathcal{M}}_n
=
\prod_{i=1}^n
\int_0^\infty
d\omega_i\,
\omega_i^{\Delta_i-1}
\mathcal{M}_n(\omega_i,z_i,\bar z_i).
\]

The parameter \(\Delta_i\) is the conformal dimension of the corresponding celestial operator.

For a particle of helicity \(J_i\), the celestial operator has conformal weights

\[
h_i
=
\frac{\Delta_i+J_i}{2},
\]

\[
\bar h_i
=
\frac{\Delta_i-J_i}{2}.
\]

Thus the celestial amplitude transforms as a correlator of two-dimensional conformal primaries:

\[
\widetilde{\mathcal{M}}_n
=
\left\langle
\prod_{i=1}^n
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle.
\]

This is the central formula of celestial holography.

---

## 14. Lorentz Symmetry as Celestial Conformal Symmetry

Under a Lorentz transformation corresponding to

\[
z
\to
w(z)
=
\frac{az+b}{cz+d},
\]

a celestial primary transforms as

\[
\mathcal{O}_{\Delta,J}(z,\bar z)
\to
(cz+d)^{2h}
(\bar c\bar z+\bar d)^{2\bar h}
\mathcal{O}_{\Delta,J}(w,\bar w).
\]

Equivalently,

\[
\left\langle
\prod_i
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle
\]

transforms covariantly under \(SL(2,\mathbb{C})\).

Thus the four-dimensional Lorentz group becomes the global conformal group of the celestial sphere.

The infinite-dimensional extension of this symmetry is provided by superrotations, which generate a Virasoro-like algebra.

---

## 15. Conformal Primary Wavefunctions

The celestial basis is not merely a change of variables. It corresponds to a different basis of one-particle states.

Instead of momentum eigenstates \(|p\rangle\), one uses boost eigenstates \(|\Delta,J,z,\bar z\rangle\).

A scalar conformal primary wavefunction is obtained by Mellin transforming a plane wave:

\[
\Phi_\Delta^\pm(X;q)
=
\int_0^\infty
d\omega\,
\omega^{\Delta-1}
e^{\pm i\omega q\cdot X}.
\]

These wavefunctions solve the massless wave equation and transform under Lorentz transformations as conformal primaries of dimension \(\Delta\) on the celestial sphere.

For spinning fields, one includes polarization tensors and helicity labels.

Thus bulk fields are reconstructed from celestial boundary data.

---

## 16. Celestial Operator Product Expansion

In an ordinary two-dimensional CFT, local operators have an operator product expansion. Celestial amplitudes also exhibit OPE-like behavior.

When two insertion points approach one another,

\[
z_1\to z_2,
\]

the corresponding particles become collinear. The celestial amplitude develops singularities governed by collinear limits of the original scattering amplitude.

Schematically,

\[
\mathcal{O}_{\Delta_1,J_1}(z_1,\bar z_1)
\mathcal{O}_{\Delta_2,J_2}(z_2,\bar z_2)
\sim
\sum_{\Delta,J}
C_{12}^{\Delta,J}
(z_{12})^{h-h_1-h_2}
(\bar z_{12})^{\bar h-\bar h_1-\bar h_2}
\mathcal{O}_{\Delta,J}(z_2,\bar z_2).
\]

For gravitons, the OPE contains the graviton operator itself, reflecting the universal self-interaction of gravity.

The OPE coefficients encode the collinear structure of the S-matrix.

---

## 17. Conformally Soft Operators

Soft limits of scattering amplitudes correspond to special values of the conformal dimension.

For gravitons, the leading soft theorem is associated with a conformally soft graviton operator at

\[
\Delta=1,
\qquad
J=\pm 2.
\]

The subleading soft theorem is associated with

\[
\Delta=0,
\qquad
J=\pm 2.
\]

These operators generate asymptotic symmetries.

Their OPEs realize the BMS algebra, including supertranslations and superrotations.

Thus the symmetry algebra of asymptotically flat gravity is embedded in the operator algebra of the celestial theory.

---

## 18. Celestial Stress Tensor and Virasoro Structure

In a two-dimensional CFT, the stress tensor \(T(z)\) generates conformal transformations. In celestial holography, certain soft graviton modes play the role of celestial stress tensors.

The subleading soft graviton theorem is related to Virasoro symmetry. The corresponding Ward identities take the form

\[
\langle
T(z)
\prod_i
\mathcal{O}_i(z_i,\bar z_i)
\rangle
=
\sum_i
\left[
\frac{h_i}{(z-z_i)^2}
+
\frac{1}{z-z_i}
\partial_{z_i}
\right]
\langle
\prod_i
\mathcal{O}_i
\rangle.
\]

This is precisely the conformal Ward identity of a two-dimensional CFT.

Quantum effects may introduce a central extension,

\[
[L_m,L_n]
=
(m-n)L_{m+n}
+
\frac{c}{12}m(m^2-1)\delta_{m+n,0}.
\]

The precise value and interpretation of the celestial central charge remain active research topics.

---

## 19. Gauge Theory and Celestial Currents

Celestial methods also apply to gauge theory.

In Yang–Mills theory, the leading soft gluon theorem is equivalent to a Ward identity for an infinite-dimensional large gauge symmetry. The corresponding celestial operators are conformally soft gluons with

\[
\Delta=1,
\qquad
J=\pm 1.
\]

They generate Kac–Moody currents on the celestial sphere:

\[
J^a(z)
J^b(w)
\sim
\frac{f^{ab}{}_c J^c(w)}{z-w}
+
\frac{k\delta^{ab}}{(z-w)^2}.
\]

Thus gauge theory also possesses a celestial holographic description.

Gravity extends this structure from finite-dimensional internal symmetries to spacetime symmetries themselves.

---

## 20. Flat-Space Holography

Celestial Relativity provides a candidate formulation of flat-space holography.

In AdS/CFT, the bulk spacetime has a timelike boundary, and bulk physics is encoded in a CFT on that boundary.

In asymptotically flat space, the natural boundary is null infinity. The holographic data live on

\[
\mathscr{I}^+
\cong
\mathbb{R}_u \times S^2.
\]

The celestial sphere is the \(S^2\) factor. The Mellin transform conjugates the null time \(u\) to the conformal dimension \(\Delta\).

Thus the bulk S-matrix is recast as a celestial correlator:

\[
\boxed{
\text{S-matrix}
\quad
\longleftrightarrow
\quad
\text{celestial CFT correlator}.
}
\]

This is not yet as complete as AdS/CFT, but it provides a precise dictionary between scattering amplitudes and conformal correlators.

---

## 21. Carrollian Geometry at Null Infinity

Null infinity has a Carrollian geometric structure.

A Carrollian manifold has a degenerate spatial metric and a preferred time direction. At \(\mathscr{I}^+\), the coordinates are \((u,z,\bar z)\). The sphere metric is

\[
2\gamma_{z\bar z}dz d\bar z,
\]

but there is no inverse metric in the \(u\) direction.

The Bondi fields \(C_{zz}\), \(N_{zz}\), and \(m_B\) may be interpreted as Carrollian fields living on null infinity.

In this view, celestial holography may be formulated either as:

1. a two-dimensional CFT on the celestial sphere after Mellin transform,
2. a three-dimensional Carrollian field theory on \(\mathscr{I}^+\).

These perspectives are complementary.

---

## 22. Infrared Divergences and Gravitational Dressings

The conventional gravitational S-matrix is infrared divergent. This is not a technical defect. It reflects the infinite degeneracy of the gravitational vacuum.

Bare Fock states are not proper asymptotic states in gravity. Physical asymptotic states must be dressed with clouds of soft gravitons.

Faddeev–Kulish-type dressings construct infrared-finite states:

\[
|\psi\rangle_{\text{dressed}}
=
e^{R}
|\psi\rangle_{\text{bare}},
\]

where \(R\) creates a coherent cloud of soft gravitons.

These dressings carry BMS charges. Different dressings correspond to different supertranslation sectors.

Thus the infrared problem of gravity is solved not by discarding soft modes, but by recognizing that they are physical symmetry data.

---

## 23. Memory Observables

Gravitational memory is, in principle, observable.

There are several types.

### 23.1 Displacement Memory

A burst of gravitational waves permanently changes the relative separation of freely falling detectors:

\[
\Delta s^A
=
\frac{1}{2}
\Delta C^A{}_B
s^B.
\]

This is the ordinary Christodoulou memory effect.

### 23.2 Spin Memory

Spin memory is a relative time delay accumulated by counter-rotating light beams around a closed loop. It is associated with subleading soft gravitons and superrotations.

### 23.3 Center-of-Mass Memory

Center-of-mass memory is associated with changes in the center-of-mass aspect of the gravitational field.

Together, these memories provide observable probes of the infrared triangle.

---

## 24. Celestial Amplitudes and Unitarity

A major open question is how unitarity of the bulk S-matrix is encoded in celestial correlators.

Celestial amplitudes are distributions in the conformal dimensions \(\Delta_i\). For unitary representations of \(SL(2,\mathbb{C})\), one often takes

\[
\Delta
=
1+i\lambda,
\qquad
\lambda\in\mathbb{R}.
\]

This is the principal continuous series.

The analytic structure of celestial amplitudes in \(\Delta\) encodes information about:

1. soft limits,
2. collinear limits,
3. infrared divergences,
4. crossing symmetry,
5. unitarity cuts.

Developing a nonperturbative celestial bootstrap remains an important goal.

---

## 25. Relation to Earlier Versions of Relativity

Celestial and Asymptotic Relativity is deeply connected to the preceding versions.

| Version | Central Idea |
|---|---|
| Relativity 3.0 | Gravity as effective quantum field theory |
| Relativity 4.0 | Background-independent quantum geometry |
| Relativity 5.0 | Holographic spacetime from entanglement |
| Relativity 6.0 | Einstein equations as thermodynamics |
| Relativity 7.0 | Quantum reference frames |
| Relativity 8.0 | de Sitter horizon-centered observables |
| Relativity 9.0 | Unified geometric interactions |
| Relativity 10.0 | Noncommutativity and relative locality |
| Relativity 11.0 | Celestial holography and asymptotic symmetries |

The conceptual progression is:

\[
\text{relative simultaneity}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative quantum frames}
\rightarrow
\text{relative horizons}
\rightarrow
\text{relative locality}
\rightarrow
\text{relative celestial holography}.
\]

Relativity 11.0 says that even the S-matrix is not fundamental. It is a representation of celestial correlators and asymptotic symmetry data.

---

## 26. Axioms of Celestial Relativity

The framework may be organized around six axioms.

### Axiom 1: Null Infinity Is Fundamental

The natural observables of asymptotically flat gravity live on \(\mathscr{I}^\pm\).

### Axiom 2: The S-Matrix Is Celestial

Momentum-space amplitudes are equivalent to celestial correlators on the sphere.

\[
\mathcal{M}(p_i)
\quad
\longleftrightarrow
\quad
\left\langle
\prod_i
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle.
\]

### Axiom 3: Lorentz Is Global Conformal

The four-dimensional Lorentz group acts as the global conformal group of the celestial sphere.

### Axiom 4: Asymptotic Symmetries Are Exact

BMS supertranslations and superrotations are exact symmetries of quantum gravity.

### Axiom 5: Soft Theorems Are Ward Identities

Universal soft behavior is controlled by asymptotic symmetry Ward identities.

### Axiom 6: Memory Is Vacuum Transition

Gravitational memory measures transitions between degenerate BMS vacua.

---

## 27. What Einstein Would Recognize

Einstein would be fascinated by Celestial Relativity.

General relativity was built on the insight that coordinates are not physical. Celestial Relativity deepens this by showing that even the asymptotic structure of spacetime contains an infinite redundancy and an infinite symmetry.

The BMS group reveals that the vacuum of general relativity is not a single state but a vast family of physically distinct states. The gravitational field carries memory. Soft gravitons are not negligible. They are the carriers of asymptotic symmetry.

Einstein might initially find the celestial CFT viewpoint strange. He was not trained in modern conformal field theory or holography. But he would recognize the central lesson:

\[
\boxed{
\text{The physical content of gravity is encoded in invariant boundary structure.}
}
\]

This is the same instinct that led him from coordinates to geometry.

Celestial Relativity extends that instinct from geometry to holography.

---

## 28. Open Problems

Several major problems remain.

### 28.1 Nonperturbative Celestial Theory

A complete nonperturbative definition of the celestial theory is lacking.

### 28.2 Unitarity and Analyticity

The precise encoding of bulk unitarity in celestial correlators is not fully understood.

### 28.3 Central Charges and Algebra

The full asymptotic symmetry algebra, including quantum central extensions and higher-spin-like structures, is still being clarified.

### 28.4 Massive Particles

Celestial methods are most natural for massless particles. Massive states require hyperboloid bases and more elaborate constructions.

### 28.5 Curved Spacetimes

Extension beyond asymptotically flat spacetimes, especially to cosmological spacetimes, remains incomplete.

### 28.6 Observational Memory

Direct detection of gravitational memory is challenging but may become possible with next-generation detectors.

---

## 29. Summary of Core Equations

### Null infinity coordinates

\[
(u,z,\bar z).
\]

### Bondi news

\[
N_{zz}
=
\partial_u C_{zz}.
\]

### Bondi mass loss

\[
\partial_u m_B
=
-
\frac{1}{4}
N_{zz}N^{zz}
-
4\pi G T_{uu}.
\]

### Supertranslation

\[
u \to u+\alpha(z,\bar z).
\]

### Soft graviton theorem

\[
\mathcal{M}_{n+1}
=
\left[
S^{(0)}
+
S^{(1)}
+
S^{(2)}
+
\cdots
\right]
\mathcal{M}_n.
\]

### Leading soft factor

\[
S^{(0)}
=
\frac{\kappa}{2}
\sum_k
\eta_k
\frac{
\varepsilon_{\mu\nu}
p_k^\mu p_k^\nu
}{
p_k\cdot q
}.
\]

### Memory

\[
\Delta C_{zz}
=
\int_{-\infty}^{+\infty}
du\,
N_{zz}.
\]

### Celestial amplitude

\[
\widetilde{\mathcal{M}}_n
=
\prod_i
\int_0^\infty
d\omega_i\,
\omega_i^{\Delta_i-1}
\mathcal{M}_n(\omega_i,z_i,\bar z_i).
\]

### Celestial correlator

\[
\widetilde{\mathcal{M}}_n
=
\left\langle
\prod_i
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle.
\]

### Conformal weights

\[
h
=
\frac{\Delta+J}{2},
\qquad
\bar h
=
\frac{\Delta-J}{2}.
\]

### Infrared triangle

\[
\text{soft theorems}
\quad
\leftrightarrow
\quad
\text{asymptotic symmetries}
\quad
\leftrightarrow
\quad
\text{memory effects}.
\]

---

## 30. Conclusion

Relativity 11.0, Celestial and Asymptotic Relativity, reveals that the infrared structure of gravity is a holographic structure.

The S-matrix is not merely a collection of momentum-space amplitudes. It is a celestial conformal correlator. Soft gravitons are not infrared accidents. They are symmetry generators. Gravitational memory is not a minor observational effect. It is a transition between degenerate vacua.

The asymptotic symmetry group of gravity is infinite-dimensional. The Lorentz group is only its global conformal subgroup. The full structure includes supertranslations, superrotations, Virasoro-like algebras, and celestial operator product expansions.

The central equation of Celestial Relativity is

\[
\widetilde{\mathcal{M}}_n
=
\left\langle
\prod_i
\mathcal{O}_{\Delta_i,J_i}(z_i,\bar z_i)
\right\rangle.
\]

The central physical statement is

\[
\boxed{
\text{Flat-space gravity is encoded on the celestial sphere.}
}
\]

Einstein’s general relativity, when examined at null infinity, reveals an infinite symmetry structure that he did not explicitly anticipate but that follows directly from the covariance and masslessness of his theory.

This is Celestial Relativity.

---

## Appendix A: Bondi Metric Expansion

The asymptotically flat metric in Bondi gauge near \(\mathscr{I}^+\) is

\[
ds^2
=
-du^2
-
2du\,dr
+
r^2
2\gamma_{z\bar z}dz d\bar z
+
\frac{2m_B}{r}du^2
+
r C_{zz}dz^2
+
r C_{\bar z\bar z}d\bar z^2
+
\cdots .
\]

The sphere metric is

\[
2\gamma_{z\bar z}dz d\bar z
=
\frac{4 dz d\bar z}{(1+z\bar z)^2}.
\]

The radiative data are contained in

\[
C_{zz}(u,z,\bar z).
\]

The Bondi news is

\[
N_{zz}
=
\partial_u C_{zz}.
\]

---

## Appendix B: BMS Transformations

A BMS transformation acts as

\[
u'
=
K(z,\bar z)
\left[
u+\alpha(z,\bar z)
\right],
\]

\[
z'
=
f(z),
\]

where \(f(z)\) is a conformal transformation of the sphere and

\[
K(z,\bar z)
=
\frac{1+z\bar z}{1+z'\bar z'}
\left|
\frac{\partial z'}{\partial z}
\right|.
\]

For global Lorentz transformations,

\[
f(z)
=
\frac{az+b}{cz+d},
\qquad
ad-bc=1.
\]

For supertranslations,

\[
f(z)=z,
\qquad
\alpha(z,\bar z)
\neq
\text{constant}.
\]

---

## Appendix C: Soft Graviton Factors

For an amplitude with one soft graviton of momentum \(q\),

\[
\mathcal{M}_{n+1}
=
\left[
S^{(0)}
+
S^{(1)}
+
S^{(2)}
+
\mathcal{O}(q^2)
\right]
\mathcal{M}_n.
\]

The leading factor is

\[
S^{(0)}
=
\frac{\kappa}{2}
\sum_k
\eta_k
\frac{
\varepsilon_{\mu\nu}
p_k^\mu p_k^\nu
}{
p_k\cdot q
}.
\]

The subleading factor is

\[
S^{(1)}
=
-
\frac{i\kappa}{2}
\sum_k
\eta_k
\frac{
\varepsilon_{\mu\nu}
q_\rho
J_k^{\rho\mu}
p_k^\nu
}{
p_k\cdot q
}.
\]

The subsubleading factor is

\[
S^{(2)}
=
-
\frac{\kappa}{4}
\sum_k
\eta_k
\frac{
\varepsilon_{\mu\nu}
q_\rho q_\sigma
J_k^{\rho\mu}
J_k^{\sigma\nu}
}{
p_k\cdot q
}.
\]

---

## Appendix D: Celestial Conformal Weights

A massless particle of helicity \(J\) and Mellin parameter \(\Delta\) corresponds to a celestial primary with weights

\[
h
=
\frac{\Delta+J}{2},
\qquad
\bar h
=
\frac{\Delta-J}{2}.
\]

Under a Möbius transformation,

\[
z
\to
\frac{az+b}{cz+d},
\]

the operator transforms as

\[
\mathcal{O}_{\Delta,J}(z,\bar z)
\to
(cz+d)^{2h}
(\bar c\bar z+\bar d)^{2\bar h}
\mathcal{O}_{\Delta,J}
\left(
\frac{az+b}{cz+d},
\frac{\bar a\bar z+\bar b}{\bar c\bar z+\bar d}
\right).
\]

---

## Appendix E: Memory and Vacuum Transition

The gravitational memory is

\[
\Delta C_{zz}
=
C_{zz}(+\infty)
-
C_{zz}(-\infty)
=
\int_{-\infty}^{+\infty}
du\,
N_{zz}.
\]

A supertranslation by \(\alpha(z,\bar z)\) shifts the shear as

\[
C_{zz}
\to
C_{zz}
-
2D_z^2\alpha.
\]

Thus a scattering process with nonzero memory connects two different BMS vacua:

\[
|0_{\text{in}}\rangle
\to
|0_{\text{out}}\rangle.
\]

The soft graviton is the quantum of this vacuum transition.

---

## Selected References

1. H. Bondi, M. G. J. van der Burg, and A. W. K. Metzner, “Gravitational Waves in General Relativity. VII. Waves from Axi-Symmetric Isolated Systems,” *Proceedings of the Royal Society A* **269**, 21 (1962).  
2. R. K. Sachs, “Gravitational Waves in General Relativity. VIII. Waves in Asymptotically Flat Space-Time,” *Proceedings of the Royal Society A* **270**, 103 (1962).  
3. R. Penrose, “Asymptotic Properties of Fields and Space-Times,” *Physical Review Letters* **10**, 66 (1963).  
4. S. Weinberg, “Infrared Photons and Gravitons,” *Physical Review* **140**, B516 (1965).  
5. A. Strominger, “Asymptotic Symmetries of Yang–Mills Theory,” *Journal of High Energy Physics* **1407**, 152 (2014).  
6. A. Strominger, “On BMS Invariance of Gravitational Scattering,” *Journal of High Energy Physics* **1407**, 152 (2014).  
7. T. He, V. Lysov, P. Mitra, and A. Strominger, “BMS Supertranslations and Weinberg’s Soft Graviton Theorem,” *Journal of High Energy Physics* **1505**, 151 (2015).  
8. F. Cachazo and A. Strominger, “Evidence for a New Soft Graviton Theorem,” arXiv:1404.4091.  
9. A. Strominger and A. Zhiboedov, “Gravitational Memory, BMS Supertranslations and Soft Theorems,” *Journal of High Energy Physics* **1601**, 086 (2016).  
10. S. W. Hawking, M. J. Perry, and A. Strominger, “Soft Hair on Black Holes,” *Physical Review Letters* **116**, 231301 (2016).  
11. D. Kapec, P. Mitra, A.-M. Raclariu, and A. Strominger, “Celestial Holography,” *Annual Review of Nuclear and Particle Science* **73**, 169 (2023).  
12. S. Pasterski, S.-H. Shao, and A. Strominger, “Flat Space Amplitudes and Conformal Symmetry of the Celestial Sphere,” *Physical Review D* **96**, 065026 (2017).  
13. S. Pasterski and S.-H. Shao, “Conformal Basis for Flat Space Amplitudes,” *Physical Review D* **96**, 065022 (2017).  
14. S. Stieberger and T. R. Taylor, “Symmetries of Celestial Amplitudes,” *Physics Letters B* **793**, 141 (2019).  
15. A. Puhm, “Conformally Soft Theorem in Gravity,” *Journal of High Energy Physics* **2009**, 130 (2020).  
16. T. Adamo, L. Mason, and A. Sharma, “Celestial Amplitudes from UV to IR,” *Journal of High Energy Physics* **2108**, 062 (2021).  
17. A. Guevara, E. Himwich, M. Pate, and A. Strominger, “Holographic Symmetry Algebras for Gauge Theory and Gravity,” *Journal of High Energy Physics* **2111**, 152 (2021).  
18. R. Gonzo, T. McLoughlin, and A. Puhm, “Celestial Holography,” *Lecture Notes in Physics* (2023).  
19. A. Raclariu, “Lectures on Celestial Holography,” arXiv:2107.02075.  
20. A. Strominger, *Lectures on the Infrared Structure of Gravity and Gauge Theory* (Princeton University Press, 2018).

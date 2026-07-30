# Relativity 10.0 — Noncommutative and Relative-Locality Relativity  
## Planck-Scale Geometry, Deformed Kinematics, and the Relativity of Locality

**White paper / academic preprint**

---

## Abstract

Relativity 10.0 is the extension of relativistic physics into the regime where the classical assumptions of pointlike locality and commuting spacetime coordinates fail. At the Planck scale,

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}},
\qquad
E_{\text{Pl}}
=
\sqrt{\frac{\hbar c^5}{G}},
\]

the simultaneous localization of events with arbitrary precision becomes physically and conceptually untenable. A natural mathematical expression of this limitation is noncommutative spacetime,

\[
[\hat{x}^\mu,\hat{x}^\nu]
=
i\theta^{\mu\nu},
\]

or, in Lie-algebraic forms such as \(\kappa\)-Minkowski spacetime,

\[
[\hat{x}^0,\hat{x}^i]
=
i\ell_{\text{P}}\hat{x}^i.
\]

In such theories, spacetime is no longer a manifold of commuting points but an algebra of noncommuting observables. Closely related is the hypothesis that momentum space is curved at the Planck scale. This leads to modified dispersion relations,

\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta\frac{E^3}{E_{\text{Pl}}}
+
\cdots,
\]

nonlinear Lorentz transformations, and deformed momentum composition laws. The resulting framework is relative locality: the coincidence of events is not absolute but depends on the observer and on the momenta of the particles involved. Special relativity made simultaneity observer-dependent. General relativity made geometry dynamical. Noncommutative and relative-locality relativity makes locality itself energy- and observer-dependent. This is a direct continuation of Einstein’s operational insight: the concepts of space, time, and event must be defined by physical measurement, and at the Planck scale those measurements impose irreducible limits.

---

## 1. Introduction

Classical relativity assumes that events are points of a smooth manifold. An event is specified by coordinates

\[
x^\mu = (ct,x,y,z),
\]

and different observers relate their coordinates through Lorentz transformations or diffeomorphisms. The coordinates may change, but the assumption that events are sharply, commuting points is retained.

Quantum gravity challenges this assumption.

To localize an event within a distance \(\Delta x\), one needs a probe with momentum uncertainty

\[
\Delta p
\sim
\frac{\hbar}{\Delta x}.
\]

The corresponding energy is approximately

\[
E
\sim
c\Delta p
\sim
\frac{\hbar c}{\Delta x}.
\]

If \(\Delta x\) becomes too small, the energy concentrated in the measurement region becomes large enough to form a black hole. The Schwarzschild radius associated with energy \(E\) is

\[
R_s
\sim
\frac{GE}{c^4}.
\]

Equating \(R_s\) with \(\Delta x\) gives

\[
\Delta x
\sim
\sqrt{\frac{G\hbar}{c^3}}
=
\ell_{\text{P}}.
\]

Thus operational localization appears to fail below the Planck length.

This suggests that the classical concept of a spacetime point is not fundamental. At the Planck scale, coordinates may become noncommuting operators,

\[
[\hat{x}^\mu,\hat{x}^\nu]
\neq 0.
\]

Equivalently, the geometry of momentum space may become nontrivial, leading to modified energy-momentum relations and observer-dependent locality.

These ideas define Relativity 10.0:

\[
\boxed{
\text{Noncommutative and Relative-Locality Relativity.}
}
\]

Its central claim is that locality is not an absolute background structure. It is a relational, energy-dependent, observer-dependent concept.

---

## 2. Planck Scale and the Breakdown of Classical Locality

The Planck length is

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}
\approx
1.616\times 10^{-35}\,\text{m}.
\]

The Planck time is

\[
t_{\text{P}}
=
\frac{\ell_{\text{P}}}{c}
=
\sqrt{\frac{G\hbar}{c^5}}.
\]

The Planck energy is

\[
E_{\text{Pl}}
=
\sqrt{\frac{\hbar c^5}{G}}
\approx
1.22\times 10^{19}\,\text{GeV}.
\]

In natural units,

\[
c=\hbar=1,
\]

one has

\[
\ell_{\text{P}}
=
\frac{1}{E_{\text{Pl}}}.
\]

The appearance of \(G\), \(\hbar\), and \(c\) together signals that quantum mechanics, relativity, and gravity are simultaneously relevant.

Classical spacetime is expected to be valid when

\[
\Delta x \gg \ell_{\text{P}},
\qquad
E \ll E_{\text{Pl}}.
\]

At Planckian scales, the continuum description may be replaced by:

1. noncommutative coordinate algebras,
2. discrete spectra of geometric operators,
3. curved momentum space,
4. deformed symmetry algebras,
5. relational locality.

Relativity 10.0 is the kinematical and phenomenological framework for this regime.

---

## 3. Noncommutative Spacetime

The simplest noncommutative deformation of spacetime is

\[
[\hat{x}^\mu,\hat{x}^\nu]
=
i\theta^{\mu\nu},
\]

where \(\theta^{\mu\nu}\) is a constant antisymmetric tensor with dimensions of length squared.

This implies uncertainty relations of the form

\[
\Delta x^\mu \Delta x^\nu
\geq
\frac{1}{2}
|\theta^{\mu\nu}|.
\]

If

\[
\theta^{\mu\nu}
\sim
\ell_{\text{P}}^2,
\]

then spacetime coordinates cannot be simultaneously localized below the Planck scale.

The continuum manifold is replaced by a noncommutative algebra of functions.

---

## 4. Moyal–Weyl Star Product

A convenient realization of constant noncommutativity is the Moyal–Weyl star product.

For ordinary functions \(f(x)\) and \(g(x)\), define

\[
(f*g)(x)
=
f(x)
\exp
\left[
\frac{i}{2}
\theta^{\mu\nu}
\overleftarrow{\partial}_\mu
\overrightarrow{\partial}_\nu
\right]
g(x).
\]

Explicitly,

\[
f*g
=
fg
+
\frac{i}{2}\theta^{\mu\nu}
\partial_\mu f\,\partial_\nu g
-
\frac{1}{8}
\theta^{\mu\nu}\theta^{\rho\sigma}
\partial_\mu\partial_\rho f\,
\partial_\nu\partial_\sigma g
+
\cdots.
\]

The coordinate functions satisfy

\[
x^\mu * x^\nu
-
x^\nu * x^\mu
=
i\theta^{\mu\nu}.
\]

Thus the algebra of functions becomes noncommutative while the underlying coordinate labels remain formal parameters.

---

## 5. Noncommutative Field Theory

A scalar field theory on Moyal spacetime has action

\[
S
=
\int d^4x
\left[
\frac{1}{2}
\partial_\mu\phi * \partial^\mu\phi
-
\frac{m^2}{2}
\phi * \phi
-
\frac{\lambda}{4!}
\phi * \phi * \phi * \phi
\right].
\]

Because the star product is associative but noncommutative, interaction terms acquire momentum-dependent phase factors.

For example, a quartic vertex carries phases of the form

\[
\exp
\left[
-\frac{i}{2}
\sum_{i<j}
p_i\wedge p_j
\right],
\]

where

\[
p\wedge q
=
p_\mu\theta^{\mu\nu}q_\nu.
\]

These phases modify scattering amplitudes and lead to novel ultraviolet-infrared mixing.

### 5.1 Noncommutative Gauge Theory

For a noncommutative \(U(1)\) gauge field \(A_\mu\), the field strength is

\[
F_{\mu\nu}
=
\partial_\mu A_\nu
-
\partial_\nu A_\mu
-
ig
[A_\mu,A_\nu]_*,
\]

where

\[
[A_\mu,A_\nu]_*
=
A_\mu * A_\nu
-
A_\nu * A_\mu.
\]

Thus even abelian gauge theory becomes self-interacting in noncommutative spacetime.

This is a striking geometric consequence:

\[
\boxed{
\text{Noncommutativity turns abelian gauge fields into nonabelian-like fields.}
}
\]

---

## 6. Lorentz Symmetry and Twisted Poincaré Covariance

A constant \(\theta^{\mu\nu}\) appears to select preferred directions, threatening Lorentz invariance.

There are two broad responses.

### 6.1 Broken Lorentz Invariance

One may treat \(\theta^{\mu\nu}\) as a fixed background tensor. Then ordinary Lorentz symmetry is spontaneously or explicitly broken. This leads to strong phenomenological constraints.

### 6.2 Twisted Lorentz Symmetry

Alternatively, one may deform the action of the Poincaré group using a Drinfeld twist,

\[
\mathcal{F}
=
\exp
\left[
-\frac{i}{2}
\theta^{\mu\nu}
P_\mu\otimes P_\nu
\right].
\]

The coproduct of the Poincaré algebra is twisted:

\[
\Delta_\mathcal{F}(X)
=
\mathcal{F}
\Delta(X)
\mathcal{F}^{-1}.
\]

The theory then possesses a deformed, or twisted, Poincaré symmetry. The coordinates transform covariantly under this twisted symmetry.

Thus noncommutativity need not imply naive Lorentz violation. It may instead imply a deformed realization of relativity.

---

## 7. \(\kappa\)-Minkowski Spacetime

A more radical deformation is Lie-algebraic noncommutativity. The \(\kappa\)-Minkowski algebra is

\[
[\hat{x}^0,\hat{x}^i]
=
\frac{i}{\kappa}\hat{x}^i,
\qquad
[\hat{x}^i,\hat{x}^j]
=
0,
\]

where \(\kappa\) is an energy scale, usually identified with the Planck energy.

If \(x^0=ct\), then \(1/\kappa\) has dimensions of length, and one may write

\[
[\hat{x}^0,\hat{x}^i]
=
i\ell_{\text{P}}\hat{x}^i.
\]

This algebra treats time differently from space. It is naturally associated with a deformed Poincaré symmetry known as \(\kappa\)-Poincaré.

The corresponding uncertainty relation is not simply constant. It implies that temporal and spatial localization become interdependent at Planckian scales.

---

## 8. \(\kappa\)-Poincaré and Modified Dispersion Relations

The \(\kappa\)-Poincaré algebra is a Hopf algebra deformation of the ordinary Poincaré algebra. Its Casimir invariant replaces the usual mass-shell condition.

In a common bicrossproduct basis, the Casimir is

\[
\mathcal{C}_\kappa(p)
=
4\kappa^2
\sinh^2
\left(
\frac{p_0}{2\kappa}
\right)
-
e^{p_0/\kappa}
\mathbf{p}^2.
\]

The mass-shell condition is

\[
\mathcal{C}_\kappa(p)
=
m^2.
\]

For \(p_0\ll \kappa\), expansion gives

\[
p_0^2
-
\mathbf{p}^2
+
\frac{1}{\kappa}p_0\mathbf{p}^2
+
\mathcal{O}\left(\frac{1}{\kappa^2}\right)
=
m^2.
\]

Restoring \(c\) and writing \(E=p_0c\), one obtains a modified dispersion relation of the generic form

\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta
\frac{E p^2 c^2}{E_{\text{Pl}}}
+
\cdots.
\]

For ultrarelativistic particles, \(pc\approx E\), this becomes

\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta
\frac{E^3}{E_{\text{Pl}}}
+
\cdots.
\]

The coefficient \(\eta\) is model-dependent and may be positive, negative, or zero.

The key point is not the precise coefficient. It is the structural possibility:

\[
\boxed{
\text{Planck-scale kinematics may deform the relativistic dispersion relation.}
}
\]

---

## 9. Doubly Special Relativity

Modified dispersion relations motivated the program of Doubly Special Relativity, or DSR.

Ordinary special relativity has one observer-independent scale:

\[
c.
\]

DSR proposes a second observer-independent scale:

\[
\ell_{\text{P}}
\quad
\text{or equivalently}
\quad
E_{\text{Pl}}.
\]

The relativity principle is preserved, but Lorentz transformations become nonlinear in momentum space.

A DSR transformation preserves both \(c\) and \(\kappa\). Schematically,

\[
p_\mu
\rightarrow
p'_\mu(p,\Lambda,\kappa),
\]

with

\[
\mathcal{C}_\kappa(p')
=
\mathcal{C}_\kappa(p).
\]

At low energies,

\[
E\ll \kappa,
\]

the transformations reduce to ordinary Lorentz transformations.

Thus DSR is not Lorentz violation. It is Lorentz deformation.

---

## 10. Deformed Momentum Composition

In ordinary relativity, total momentum is additive:

\[
P_{\text{tot}}
=
p+q.
\]

In \(\kappa\)-deformed theories, momentum composition may be nonabelian and nonlinear.

For example, one possible composition law is

\[
(p\oplus q)_0
=
p_0+q_0,
\]

\[
(p\oplus q)_i
=
p_i
+
e^{-p_0/\kappa}q_i.
\]

This law is associative but not commutative:

\[
p\oplus q
\neq
q\oplus p.
\]

The noncommutativity of momentum addition is dual to the noncommutativity of spacetime coordinates.

This deformed composition law is central to relative locality.

---

## 11. Relative Locality

Relative locality is the physical interpretation of curved momentum space.

In ordinary special relativity, momentum space is flat. The conservation law at an interaction vertex is

\[
p+q+k=0.
\]

The interaction is local: all particles meet at a single spacetime point \(z^\mu\).

In relative locality, momentum space has nontrivial geometry. Conservation is written using a deformed composition law:

\[
p\oplus q\oplus k
=
0.
\]

Because the composition law is nonlinear, the spacetime coordinates associated with the interaction become momentum-dependent.

The result is:

\[
\boxed{
\text{The coincidence of events is not absolute.}
}
\]

Two particles may interact at the same spacetime point according to one observer, while a distant observer describes the interaction as nonlocal.

Locality becomes relative.

---

## 12. Relative-Locality Action Principle

A compact formulation of relative locality uses a phase-space action.

For a set of particles \(n\), one writes

\[
S
=
\sum_n
\int ds
\left[
x^{(n)}_\mu
\dot p_{(n)}^\mu
-
N^{(n)}
\mathcal{C}(p_{(n)})
\right]
+
\sum_I
z_I^\mu
\left(
\bigoplus_{n\in v_I}
p^{(n)}
\right)_\mu.
\]

Here:

- \(x^{(n)}_\mu\) are spacetime coordinates conjugate to momenta,
- \(p_{(n)}^\mu\) are particle momenta,
- \(\mathcal{C}(p)\) is the deformed mass-shell constraint,
- \(N^{(n)}\) are Lagrange multipliers,
- \(z_I^\mu\) enforce momentum conservation at interaction vertices \(v_I\),
- \(\oplus\) denotes the deformed momentum composition law.

Variation with respect to \(z_I^\mu\) gives deformed conservation:

\[
\bigoplus_{n\in v_I}
p^{(n)}
=
0.
\]

Variation with respect to momenta gives the spacetime coordinates of the interaction as

\[
x^{(n)}_\mu(s_I)
=
\frac{\partial}{\partial p^{(n)\mu}}
\left[
z_I^\nu
\left(
\bigoplus_{m\in v_I}
p^{(m)}
\right)_\nu
\right].
\]

Because \(\oplus\) is nonlinear, different particles at the same vertex acquire different coordinate assignments.

This is the mathematical origin of relative locality.

---

## 13. Curved Momentum Space

Relative locality is naturally described using the geometry of momentum space.

Let momentum space have metric

\[
g^{\mu\nu}(p).
\]

The dispersion relation may be viewed as a geodesic distance from the origin:

\[
\mathcal{C}(p)
=
d^2(0,p).
\]

The composition law defines a connection on momentum space. Near the origin,

\[
(p\oplus q)^\mu
=
p^\mu
+
q^\mu
-
\Gamma^\mu_{\nu\rho}
p^\nu q^\rho
+
\cdots.
\]

The coefficients \(\Gamma^\mu_{\nu\rho}\) define an affine connection.

The curvature of momentum space is then

\[
R^\mu{}_{\nu\rho\sigma}
=
\partial_\rho\Gamma^\mu_{\nu\sigma}
-
\partial_\sigma\Gamma^\mu_{\nu\rho}
+
\Gamma^\mu_{\lambda\rho}\Gamma^\lambda_{\nu\sigma}
-
\Gamma^\mu_{\lambda\sigma}\Gamma^\lambda_{\nu\rho}.
\]

For \(\kappa\)-Poincaré, momentum space is approximately de Sitter space with radius \(\kappa\):

\[
R
\sim
\frac{1}{\kappa^2}.
\]

Thus Planck-scale physics may be encoded not in curved spacetime alone, but in curved momentum space.

---

## 14. Observer-Dependent Locality

In ordinary relativity, translations are generated by total momentum:

\[
P_\mu
=
\sum_n p^{(n)}_\mu.
\]

A translation by \(a^\mu\) acts as

\[
x^{(n)}_\mu
\rightarrow
x^{(n)}_\mu
+
a_\mu.
\]

All particles at a vertex remain coincident.

In relative locality, total momentum is deformed:

\[
P_\mu
=
\left(
\bigoplus_n p^{(n)}
\right)_\mu.
\]

Translations generated by this total momentum act nonlinearly on individual particle coordinates.

The relative separation between two particles at the same vertex can be of order

\[
\Delta x
\sim
\frac{p}{\kappa}L,
\]

where \(L\) is the distance between observer and interaction.

Thus an interaction that is local for an observer at the vertex may appear nonlocal for a distant observer.

The effect is tiny for laboratory distances but can become relevant over cosmological baselines.

---

## 15. Energy-Dependent Propagation

Modified dispersion relations imply energy-dependent propagation speeds.

For a massless particle, the group velocity is

\[
v
=
\frac{\partial E}{\partial p}.
\]

If

\[
E^2
=
p^2c^2
+
\eta\frac{E^3}{E_{\text{Pl}}}
+
\cdots,
\]

then to leading order,

\[
v
\approx
c
\left[
1
+
\xi
\frac{E}{E_{\text{Pl}}}
+
\cdots
\right],
\]

where \(\xi\) is a model-dependent coefficient.

A photon of energy \(E\) traveling a distance \(L\) may experience a time delay relative to a low-energy photon:

\[
\Delta t
\sim
\xi
\frac{E}{E_{\text{Pl}}}
\frac{L}{c}.
\]

For astrophysical sources,

\[
L\sim \text{Gpc},
\]

this effect can be phenomenologically relevant even though \(E/E_{\text{Pl}}\) is extremely small.

---

## 16. Snyder Noncommutativity

Historically, the first Lorentz-invariant noncommutative spacetime was proposed by Hartland Snyder in 1947.

Snyder’s algebra is

\[
[\hat{x}_\mu,\hat{x}_\nu]
=
i a^2 \hat{M}_{\mu\nu},
\]

where \(a\) is a fundamental length and \(\hat{M}_{\mu\nu}\) are Lorentz generators.

This construction preserves Lorentz covariance because the noncommutativity tensor is itself an operator transforming under Lorentz transformations.

Snyder’s model anticipated modern ideas:

1. minimal length,
2. noncommuting coordinates,
3. deformed momentum space,
4. modified locality.

It is a precursor of both \(\kappa\)-Minkowski theory and relative locality.

---

## 17. Noncommutative Geometry and Spectral Triples

A mathematically rigorous approach to noncommutative geometry is provided by Connes’ spectral triples.

A spectral triple consists of:

1. an algebra \(\mathcal{A}\),
2. a Hilbert space \(\mathcal{H}\),
3. a Dirac operator \(D\).

Classical geometry is recovered when

\[
\mathcal{A}=C^\infty(M).
\]

Noncommutative geometry replaces this by a noncommutative algebra.

The spectral action is

\[
S
=
\operatorname{Tr}
f\left(
\frac{D}{\Lambda}
\right).
\]

Its asymptotic expansion produces gravitational and gauge-theoretic terms.

While spectral noncommutative geometry is not identical to relative locality, both share a central idea:

\[
\boxed{
\text{Geometry is algebraic rather than pointwise.}
}
\]

---

## 18. Relation to Quantum Gravity

Noncommutative and relative-locality relativity are not complete quantum gravity theories. They are kinematical frameworks motivated by quantum gravity.

They appear in several contexts.

### 18.1 String Theory

String theory introduces a fundamental length \(\ell_s\). In certain backgrounds with a \(B\)-field, the effective spacetime coordinates become noncommutative:

\[
[\hat{x}^\mu,\hat{x}^\nu]
=
i\theta^{\mu\nu}.
\]

This was made explicit by Seiberg and Witten.

### 18.2 Loop Quantum Gravity

Loop quantum gravity predicts discrete spectra for area and volume. While not necessarily noncommutative in the Moyal sense, it undermines the classical continuum at the Planck scale.

### 18.3 Group Field Theory and Spin Foams

Spin-foam amplitudes and group field theories naturally involve noncommutative flux variables and deformed geometric structures.

### 18.4 Holography

Holography suggests that bulk locality is emergent and approximate. Relative locality provides a complementary perspective: locality is not fundamental but observer- and momentum-dependent.

---

## 19. Causality and Unitarity

Noncommutative field theories face serious consistency constraints.

If time-space noncommutativity is present,

\[
\theta^{0i}\neq 0,
\]

unitarity and causality can become problematic. Purely spatial noncommutativity,

\[
\theta^{ij}\neq 0,
\qquad
\theta^{0i}=0,
\]

is better behaved.

In \(\kappa\)-Minkowski theory, the deformation is time-space, so careful treatment of causality is required.

Relative locality also raises causal questions. If event coincidence is observer-dependent, what replaces the invariant causal order?

A plausible answer is that causal structure is preserved not at the level of sharp events, but at the level of phase-space interactions and invariant momentum-space geometry.

Thus:

\[
\boxed{
\text{Causality becomes a relational structure in phase space.}
}
\]

---

## 20. Phenomenology

Planck-scale deformations are extremely small, but astrophysical observations can amplify them through large propagation distances.

### 20.1 Gamma-Ray Bursts

High-energy photons from gamma-ray bursts may exhibit energy-dependent arrival times.

The expected delay is

\[
\Delta t
\sim
\xi
\frac{E}{E_{\text{Pl}}}
\frac{L}{c}.
\]

Observations of short gamma-ray bursts, especially by the Fermi telescope, place strong bounds on linear energy-dependent delays. In some cases, the effective quantum-gravity scale is constrained to be near or above the Planck scale.

### 20.2 TeV Astrophysics

TeV photons from blazars provide another probe. Energy-dependent propagation and absorption thresholds may reveal Planck-scale effects.

### 20.3 Threshold Anomalies

Modified dispersion relations alter reaction thresholds.

Examples include:

1. photon decay,

\[
\gamma \rightarrow e^+ + e^-,
\]

2. vacuum Cherenkov radiation,

\[
e^- \rightarrow e^- + \gamma,
\]

3. modifications to the Greisen–Zatsepin–Kuzmin cutoff.

The absence of such anomalies strongly constrains Lorentz-violating dispersion relations.

### 20.4 Relative-Locality Effects

Relative locality predicts not merely modified propagation, but momentum-dependent event localization. Possible signatures include:

1. energy-dependent time delays without Lorentz violation,
2. observer-dependent interaction vertices,
3. modified conservation laws in high-energy collisions,
4. nonlocal correlations over cosmological baselines.

No confirmed signal has yet been observed.

---

## 21. Distinguishing Lorentz Violation from Lorentz Deformation

It is important to distinguish three possibilities.

### 21.1 Exact Lorentz Invariance

The dispersion relation remains

\[
E^2=p^2c^2+m^2c^4.
\]

No Planck-scale kinematic deformation occurs.

### 21.2 Broken Lorentz Invariance

A preferred frame exists. Modified dispersion relations are frame-dependent. This is tightly constrained experimentally.

### 21.3 Deformed Lorentz Invariance

The relativity principle is preserved, but Lorentz transformations are nonlinear. The Planck scale is invariant. This is the DSR and relative-locality scenario.

Relativity 10.0 is most naturally formulated in the third category.

---

## 22. Born Reciprocity and Phase-Space Geometry

Relative locality is closely related to Born reciprocity.

Max Born suggested that position and momentum should be treated symmetrically. In ordinary quantum mechanics,

\[
[\hat{x}^\mu,\hat{p}_\nu]
=
i\hbar\delta^\mu_\nu.
\]

But position space and momentum space are treated asymmetrically: position space is curved in general relativity, while momentum space is usually flat.

A reciprocal theory would allow both to be curved:

\[
\text{curved spacetime}
\quad
\leftrightarrow
\quad
\text{curved momentum space}.
\]

Relative locality focuses on the latter.

A full Planck-scale relativity may require a geometry of phase space itself, with metric structure

\[
ds^2
=
g_{\mu\nu}(x,p)dx^\mu dx^\nu
+
h^{\mu\nu}(x,p)dp_\mu dp_\nu
+
\cdots.
\]

This would generalize both general relativity and relative locality.

---

## 23. Axioms of Relativity 10.0

The framework may be organized around six axioms.

### Axiom 1: Planck Scale Is Invariant

There exists an invariant length or energy scale,

\[
\ell_{\text{P}},
\qquad
E_{\text{Pl}}.
\]

### Axiom 2: Coordinates May Be Noncommutative

At the Planck scale,

\[
[\hat{x}^\mu,\hat{x}^\nu]
\neq 0.
\]

### Axiom 3: Momentum Space May Be Curved

The geometry of momentum space is not necessarily flat.

### Axiom 4: Symmetries Are Deformed, Not Necessarily Broken

Lorentz and translation symmetries may be realized nonlinearly through Hopf-algebraic or quantum-group structures.

### Axiom 5: Locality Is Relational

Event coincidence is observer- and momentum-dependent.

### Axiom 6: Classical Spacetime Emerges

For

\[
E\ll E_{\text{Pl}},
\qquad
L\gg \ell_{\text{P}},
\]

ordinary commuting spacetime and absolute locality are recovered.

---

## 24. Relation to Earlier Versions of Relativity

Relativity 10.0 continues the historical extension of relativity.

| Version | Relativized Structure |
|---|---|
| Special Relativity | Simultaneity and inertial frames |
| General Relativity | Geometry and gravitation |
| Effective Quantum Relativity | Metric as quantum effective field |
| Background-Independent Quantum Geometry | Continuum geometry itself |
| Holographic Relativity | Bulk locality and spatial geometry |
| Thermodynamic Relativity | Gravitational dynamics as thermodynamics |
| Quantum Reference Frames | Observers and frames |
| de Sitter Relativity | Cosmological horizons and observables |
| Unified Geometric Relativity | Gauge and gravitational geometry |
| Noncommutative / Relative-Locality Relativity | Locality and spacetime commutativity |

The progression is:

\[
\text{relative simultaneity}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative quantum frames}
\rightarrow
\text{relative horizons}
\rightarrow
\text{relative locality}.
\]

Each stage removes an assumed absolute structure.

Relativity 10.0 removes the absoluteness of the event.

---

## 25. Conceptual Interpretation

In classical physics, an event is primitive. It simply happens at a point.

In special relativity, the time and place of an event depend on the inertial observer, but the event itself remains invariant.

In general relativity, coordinates are arbitrary, but local coincidences of fields remain meaningful.

In relative-locality relativity, even the coincidence of events becomes observer- and momentum-dependent.

The new ontology is not a manifold of points. It is a network of interactions in phase space.

The fundamental statement is:

\[
\boxed{
\text{Events are not absolute. Interactions are relational.}
}
\]

Spacetime points are approximations valid when momenta are small compared with the Planck scale and observers are close compared with the induced nonlocality scale.

---

## 26. What Einstein Would Think

Einstein would be cautious.

He valued sharp operational definitions, but he also believed in an objective physical reality. Observer-dependent locality might initially appear to threaten objectivity.

However, Einstein’s own work began by analyzing which quantities are operationally meaningful. He showed that simultaneity is not absolute because it depends on the observer’s state of motion. He showed that geometry is not absolute because it is dynamical.

Relative locality applies the same method to the concept of an event.

If Planck-scale measurements cannot define absolute coincidence, then locality itself must become relational.

Einstein might resist the specific models. But he would recognize the conceptual lineage:

\[
\text{special relativity}
\quad
\rightarrow
\quad
\text{general relativity}
\quad
\rightarrow
\quad
\text{relative locality}.
\]

Each extends the principle that physical law must not depend on arbitrary, unobservable structures.

---

## 27. Open Problems

Several major problems remain.

### 27.1 Full Quantum Field Theory

A complete, unitary, causal quantum field theory on noncommutative or relative-locality spacetime is not yet established.

### 27.2 Coupling to Gravity

Relative locality is usually formulated in flat spacetime with curved momentum space. Its merger with dynamical curved spacetime remains incomplete.

### 27.3 Multi-Particle Consistency

Deformed conservation laws and nonlocal vertices must satisfy cluster decomposition and macroscopic locality.

### 27.4 Experimental Discrimination

It is difficult to distinguish true relative-locality effects from ordinary astrophysical delays or Lorentz-violating models.

### 27.5 Derivation from Quantum Gravity

A final theory should derive noncommutativity or momentum-space curvature from deeper principles, not merely postulate them.

### 27.6 Causal Structure

A fully satisfactory causal theory for relative locality is still under development.

---

## 28. Summary of Core Equations

### Planck length

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}.
\]

### Planck energy

\[
E_{\text{Pl}}
=
\sqrt{\frac{\hbar c^5}{G}}.
\]

### Canonical noncommutativity

\[
[\hat{x}^\mu,\hat{x}^\nu]
=
i\theta^{\mu\nu}.
\]

### Coordinate uncertainty

\[
\Delta x^\mu \Delta x^\nu
\geq
\frac{1}{2}|\theta^{\mu\nu}|.
\]

### Moyal star product

\[
(f*g)(x)
=
f(x)
\exp
\left[
\frac{i}{2}
\theta^{\mu\nu}
\overleftarrow{\partial}_\mu
\overrightarrow{\partial}_\nu
\right]
g(x).
\]

### \(\kappa\)-Minkowski algebra

\[
[\hat{x}^0,\hat{x}^i]
=
i\ell_{\text{P}}\hat{x}^i.
\]

### Modified dispersion relation

\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta\frac{E^3}{E_{\text{Pl}}}
+
\cdots.
\]

### Deformed momentum composition

\[
p\oplus q
\neq
p+q.
\]

### Relative-locality action

\[
S
=
\sum_n
\int ds
\left[
x^{(n)}_\mu
\dot p_{(n)}^\mu
-
N^{(n)}
\mathcal{C}(p_{(n)})
\right]
+
\sum_I
z_I^\mu
\left(
\bigoplus_{n\in v_I}
p^{(n)}
\right)_\mu.
\]

### Momentum-space curvature scale

\[
R_{\text{momentum}}
\sim
\frac{1}{E_{\text{Pl}}^2}.
\]

### Energy-dependent time delay

\[
\Delta t
\sim
\xi
\frac{E}{E_{\text{Pl}}}
\frac{L}{c}.
\]

---

## 29. Conclusion

Relativity 10.0, Noncommutative and Relative-Locality Relativity, is the extension of Einstein’s principle into the Planck regime.

It begins from the failure of absolute localization. It replaces commuting coordinates with noncommutative algebras. It replaces flat momentum space with curved momentum geometry. It replaces absolute event coincidence with observer-dependent locality.

Its central equations are

\[
[\hat{x}^\mu,\hat{x}^\nu]
=
i\theta^{\mu\nu},
\]

and

\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta\frac{E^3}{E_{\text{Pl}}}
+
\cdots.
\]

Its central principle is

\[
\boxed{
\text{Locality is relative.}
}
\]

Special relativity taught that simultaneity is observer-dependent. General relativity taught that geometry is dynamical. Relativity 10.0 teaches that the very locality of events may depend on the observer, the energy, and the curvature of momentum space.

This is not the final theory of quantum gravity. But it is one of its most direct kinematical consequences.

It is the relativity of the event itself.

---

## Appendix A: Star-Product Expansion

The Moyal star product is

\[
f*g
=
f
\exp
\left[
\frac{i}{2}
\theta^{\mu\nu}
\overleftarrow{\partial}_\mu
\overrightarrow{\partial}_\nu
\right]
g.
\]

To second order,

\[
f*g
=
fg
+
\frac{i}{2}\theta^{\mu\nu}
\partial_\mu f\partial_\nu g
-
\frac{1}{8}
\theta^{\mu\nu}\theta^{\rho\sigma}
\partial_\mu\partial_\rho f
\partial_\nu\partial_\sigma g
+
\cdots.
\]

The commutator is

\[
[f,g]_*
=
f*g-g*f
=
i\theta^{\mu\nu}
\partial_\mu f\partial_\nu g
+
\mathcal{O}(\theta^3).
\]

For coordinate functions,

\[
[x^\mu,x^\nu]_*
=
i\theta^{\mu\nu}.
\]

---

## Appendix B: Expansion of the \(\kappa\)-Poincaré Casimir

The \(\kappa\)-deformed Casimir is

\[
\mathcal{C}_\kappa(p)
=
4\kappa^2
\sinh^2
\left(
\frac{p_0}{2\kappa}
\right)
-
e^{p_0/\kappa}
\mathbf{p}^2.
\]

Using

\[
\sinh x
=
x+\frac{x^3}{6}+\cdots,
\]

one finds

\[
4\kappa^2
\sinh^2
\left(
\frac{p_0}{2\kappa}
\right)
=
p_0^2
+
\frac{p_0^4}{12\kappa^2}
+
\cdots.
\]

Also,

\[
e^{p_0/\kappa}
=
1+\frac{p_0}{\kappa}
+
\frac{p_0^2}{2\kappa^2}
+
\cdots.
\]

Therefore,

\[
\mathcal{C}_\kappa(p)
=
p_0^2
-
\mathbf{p}^2
+
\frac{p_0}{\kappa}\mathbf{p}^2
+
\mathcal{O}\left(\frac{1}{\kappa^2}\right).
\]

Setting \(\mathcal{C}_\kappa(p)=m^2\) gives the modified mass-shell condition.

---

## Appendix C: Relative-Locality Vertex Variation

Consider a vertex with conservation law

\[
\mathcal{K}_\mu
=
(p\oplus q)_\mu
=
0.
\]

The vertex term in the action is

\[
S_v
=
z^\mu \mathcal{K}_\mu.
\]

Variation with respect to \(p_\mu\) gives the coordinate of particle \(p\) at the vertex:

\[
x^{(p)}_\mu
=
\frac{\partial S_v}{\partial p^\mu}
=
z^\nu
\frac{\partial \mathcal{K}_\nu}{\partial p^\mu}.
\]

Similarly,

\[
x^{(q)}_\mu
=
z^\nu
\frac{\partial \mathcal{K}_\nu}{\partial q^\mu}.
\]

If the composition law is nonlinear,

\[
\frac{\partial \mathcal{K}_\nu}{\partial p^\mu}
\neq
\frac{\partial \mathcal{K}_\nu}{\partial q^\mu}.
\]

Therefore,

\[
x^{(p)}_\mu
\neq
x^{(q)}_\mu.
\]

The two particles do not share the same spacetime coordinate assignment, even though they participate in the same interaction.

This is relative locality.

---

## Appendix D: Time Delay from Modified Dispersion

Assume

\[
E^2
=
p^2c^2
+
\xi\frac{E^3}{E_{\text{Pl}}}.
\]

For massless particles, the group velocity is

\[
v
=
\frac{\partial E}{\partial p}.
\]

To leading order,

\[
v
\approx
c
\left[
1
+
\alpha
\frac{E}{E_{\text{Pl}}}
\right],
\]

where \(\alpha\) is model-dependent.

The arrival-time difference between two photons of energies \(E_1\) and \(E_2\) traveling distance \(L\) is

\[
\Delta t
\approx
\alpha
\frac{E_1-E_2}{E_{\text{Pl}}}
\frac{L}{c}.
\]

This is the standard leading-order quantum-gravity time-of-flight signature.

---

## Selected References

1. H. S. Snyder, “Quantized Space-Time,” *Physical Review* **71**, 38 (1947).  
2. A. Connes, *Noncommutative Geometry* (Academic Press, 1994).  
3. A. Connes, M. R. Douglas, and A. Schwarz, “Noncommutative Geometry and Matrix Theory,” *Journal of High Energy Physics* **9802**, 003 (1998).  
4. N. Seiberg and E. Witten, “String Theory and Noncommutative Geometry,” *Journal of High Energy Physics* **9909**, 032 (1999).  
5. J. Lukierski, H. Ruegg, A. Nowicki, and V. N. Tolstoy, “\(q\)-Deformation of Poincaré Algebra,” *Physics Letters B* **264**, 331 (1991).  
6. S. Majid and H. Ruegg, “Bicrossproduct Structure of the \(\kappa\)-Poincaré Group and Noncommutative Geometry,” *Physics Letters B* **334**, 348 (1994).  
7. G. Amelino-Camelia, “Relativity in Spacetimes with Short-Distance Structure Governed by an Observer-Independent Length Scale,” *International Journal of Modern Physics D* **11**, 35 (2002).  
8. G. Amelino-Camelia, “Testable Scenario for Relativity with Minimum Length,” *Physics Letters B* **510**, 255 (2001).  
9. J. Magueijo and L. Smolin, “Lorentz Invariance with an Invariant Energy Scale,” *Physical Review Letters* **88**, 190403 (2002).  
10. G. Amelino-Camelia, L. Freidel, J. Kowalski-Glikman, and L. Smolin, “The Principle of Relative Locality,” *Physical Review D* **84**, 084010 (2011).  
11. L. Freidel and L. Smolin, “Gamma Ray Burst Constraints on Relative Locality,” *Physical Review D* **85**, 084052 (2012).  
12. J. Kowalski-Glikman, “Introduction to Doubly Special Relativity,” *Lecture Notes in Physics* **669**, 131 (2005).  
13. S. Hossenfelder, “Minimal Length Scale Scenarios for Quantum Gravity,” *Living Reviews in Relativity* **16**, 2 (2013).  
14. T. Jacobson, S. Liberati, and D. Mattingly, “Lorentz Violation at High Energy: Concepts, Phenomena and Astrophysical Constraints,” *Annals of Physics* **321**, 150 (2006).  
15. D. Mattingly, “Modern Tests of Lorentz Invariance,” *Living Reviews in Relativity* **8**, 5 (2005).  
16. G. Amelino-Camelia, “Quantum-Spacetime Phenomenology,” *Living Reviews in Relativity* **16**, 5 (2013).  
17. M. Born, “A Suggestion for Unifying Quantum Theory and Relativity,” *Reviews of Modern Physics* **21**, 463 (1949).  
18. L. Freidel, J. Kowalski-Glikman, and L. Smolin, “2+1 Gravity and Doubly Special Relativity,” *Physical Review D* **69**, 044001 (2004).  
19. S. Majid, *Foundations of Quantum Group Theory* (Cambridge University Press, 1995).  
20. R. J. Szabo, “Quantum Field Theory on Noncommutative Spaces,” *Physics Reports* **378**, 207 (2003).

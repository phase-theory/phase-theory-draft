# Relativity 8.0 — de Sitter Relativity  
## Horizon-Centered Physics in a Universe with Positive Cosmological Constant

**White paper / academic preprint**

---

## Abstract

Modern cosmology has restored the cosmological constant to the center of relativistic physics. Observations indicate that the universe contains a positive vacuum energy density and is approaching an asymptotically de Sitter state. In such a universe, the fundamental spacetime is not Minkowski space, but de Sitter space, the maximally symmetric solution of Einstein’s equations with positive cosmological constant,

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
0,
\qquad
\Lambda>0.
\]

De Sitter space possesses a cosmological horizon, a finite entropy,

\[
S_{\text{dS}}
=
\frac{k_{\text{B}} A_{\text{horizon}}}{4G\hbar}
=
\frac{3\pi k_{\text{B}} c^3}{G\hbar \Lambda},
\]

and a Gibbons–Hawking temperature,

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}},
\qquad
H^2=\frac{\Lambda c^2}{3}.
\]

Unlike Minkowski space, de Sitter space does not admit a global S-matrix in the usual asymptotic sense. Every observer is confined within a cosmological horizon. The observable universe is therefore not the whole universe. Relativity must become horizon-centered:

\[
\boxed{
\text{physical observables}
=
\text{horizon-relative observables}.
}
\]

Relativity 8.0, de Sitter Relativity, is the formulation of gravitational physics in which the positive cosmological constant is not an optional term, not a perturbative correction, and not a historical embarrassment, but a foundational structural constant. It implies that spacetime has a finite information capacity, that cosmology is not merely an application of general relativity but a basic sector of relativistic theory, and that the ultimate observables of physics are those accessible within an observer’s causal diamond. Einstein introduced \(\Lambda\) in 1917 to make the universe static. A century later, \(\Lambda\) appears instead as one of the first clues to quantum spacetime.

---

## 1. Introduction

For most of the twentieth century, the cosmological constant occupied an ambiguous position. Einstein introduced it in 1917 to allow a static universe. After the discovery of cosmic expansion, it was often regarded as unnecessary. In the late twentieth century, it was treated by many as a parameter that could be set to zero without conceptual loss.

Modern cosmology has overturned that judgment.

Observations of Type Ia supernovae, the cosmic microwave background, baryon acoustic oscillations, and large-scale structure indicate that the universe is dominated by a component with negative pressure, consistent with a positive cosmological constant. The standard cosmological model, \(\Lambda\)CDM, contains a small but nonzero \(\Lambda\). If dark energy is truly a cosmological constant, the universe will asymptotically approach de Sitter space.

This changes the conceptual foundation of relativity.

In special relativity, the vacuum spacetime is Minkowski space. In general relativity, the vacuum with \(\Lambda=0\) is again Minkowski space, at least locally and asymptotically in many solutions. But if \(\Lambda>0\), the natural vacuum is not Minkowski space. It is de Sitter space.

This has profound consequences:

1. There is a cosmic length scale,

\[
\alpha
=
\sqrt{\frac{3}{\Lambda}}.
\]

2. Every observer has a cosmological horizon.

3. The horizon has finite entropy.

4. There is no global asymptotic S-matrix.

5. Physical observables are observer- and horizon-relative.

6. The Hilbert space accessible to a single observer may be finite-dimensional.

7. Cosmology becomes foundational rather than applied.

These consequences define de Sitter Relativity.

---

## 2. Einstein’s Equations with a Cosmological Constant

The Einstein field equations with cosmological constant are

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
\frac{8\pi G}{c^4}
T_{\mu\nu}.
\]

In vacuum,

\[
T_{\mu\nu}=0,
\]

they reduce to

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
0.
\]

Taking the trace in four dimensions,

\[
R - 4\Lambda = 0,
\]

so

\[
R = 4\Lambda.
\]

The vacuum equations then imply

\[
R_{\mu\nu}
=
\Lambda g_{\mu\nu}.
\]

Thus a positive cosmological constant produces a spacetime of constant positive curvature.

Equivalently, one may move the cosmological term to the right-hand side and interpret it as vacuum stress-energy:

\[
G_{\mu\nu}
=
\frac{8\pi G}{c^4}
T_{\mu\nu}^{(\Lambda)},
\]

with

\[
T_{\mu\nu}^{(\Lambda)}
=
-
\frac{\Lambda c^4}{8\pi G}
g_{\mu\nu}.
\]

This has the form of a Lorentz-invariant perfect fluid with energy density

\[
\rho_\Lambda c^2
=
\frac{\Lambda c^4}{8\pi G},
\]

and pressure

\[
p_\Lambda
=
-
\rho_\Lambda c^2.
\]

The equation of state is therefore

\[
w
=
\frac{p}{\rho c^2}
=
-1.
\]

This is the defining thermodynamic signature of vacuum energy.

---

## 3. de Sitter Space as the Vacuum of Positive \(\Lambda\)

De Sitter space is the maximally symmetric solution of the vacuum Einstein equations with \(\Lambda>0\). It may be represented as a hyperboloid embedded in five-dimensional Minkowski space.

Let \(X^A\), \(A=0,1,2,3,4\), be coordinates in \(\mathbb{R}^{1,4}\) with metric

\[
ds_5^2
=
-dX_0^2
+
dX_1^2
+
dX_2^2
+
dX_3^2
+
dX_4^2.
\]

De Sitter space is the hypersurface

\[
-X_0^2
+
X_1^2
+
X_2^2
+
X_3^2
+
X_4^2
=
\alpha^2,
\]

where

\[
\alpha
=
\sqrt{\frac{3}{\Lambda}}
\]

is the de Sitter radius.

The isometry group is

\[
SO(1,4),
\]

the de Sitter group. This replaces the Poincaré group of Minkowski space as the symmetry group of the vacuum.

The curvature tensor takes the maximally symmetric form

\[
R_{\mu\nu\rho\sigma}
=
\frac{1}{\alpha^2}
\left(
g_{\mu\rho}g_{\nu\sigma}
-
g_{\mu\sigma}g_{\nu\rho}
\right).
\]

The Ricci tensor is

\[
R_{\mu\nu}
=
\frac{3}{\alpha^2}
g_{\mu\nu}
=
\Lambda g_{\mu\nu},
\]

and the scalar curvature is

\[
R
=
\frac{12}{\alpha^2}
=
4\Lambda.
\]

Thus de Sitter space is the natural vacuum of a universe with positive cosmological constant.

---

## 4. Coordinate Systems and Horizons

De Sitter space can be covered by several coordinate systems, each revealing different physical aspects.

### 4.1 Global Coordinates

Global coordinates cover the entire de Sitter manifold:

\[
ds^2
=
-c^2 d\tau^2
+
\alpha^2
\cosh^2\left(\frac{c\tau}{\alpha}\right)
d\Omega_3^2,
\]

where \(d\Omega_3^2\) is the metric on the unit three-sphere.

The spatial sections are compact three-spheres. The universe contracts to a minimum size and re-expands. There is no global timelike Killing vector.

### 4.2 Flat Cosmological Coordinates

The expanding flat patch is written as

\[
ds^2
=
-c^2 dt^2
+
e^{2Ht}
\left(
dr^2+r^2d\Omega^2
\right),
\]

where

\[
H
=
\frac{c}{\alpha}
=
c\sqrt{\frac{\Lambda}{3}}.
\]

This is the coordinate system most natural for inflation and late-time accelerated expansion.

In conformal time \(\eta\), with

\[
\eta
=
-\frac{1}{aH},
\qquad
a(t)=e^{Ht},
\]

the metric becomes

\[
ds^2
=
\frac{1}{H^2\eta^2}
\left(
-c^2 d\eta^2
+
d\mathbf{x}^2
\right),
\qquad
\eta<0.
\]

Future infinity corresponds to

\[
\eta \to 0^-.
\]

### 4.3 Static Coordinates

The static patch is

\[
ds^2
=
-
\left(
1-H^2r^2/c^2
\right)
c^2dt^2
+
\left(
1-H^2r^2/c^2
\right)^{-1}
dr^2
+
r^2d\Omega^2.
\]

Equivalently, using \(\alpha=c/H\),

\[
ds^2
=
-
\left(
1-\frac{r^2}{\alpha^2}
\right)
c^2dt^2
+
\left(
1-\frac{r^2}{\alpha^2}
\right)^{-1}
dr^2
+
r^2d\Omega^2.
\]

The static patch covers only the region accessible to an observer at \(r=0\). The cosmological horizon lies at

\[
r=\alpha
=
\sqrt{\frac{3}{\Lambda}}.
\]

Inside the horizon, \(\partial_t\) is timelike. Outside, it becomes spacelike.

This is the observer-centered geometry that defines de Sitter Relativity.

---

## 5. Cosmological Horizon and Gibbons–Hawking Temperature

The static-patch horizon is a causal horizon. An observer at \(r=0\) cannot receive signals from beyond \(r=\alpha\).

The surface gravity of the de Sitter horizon is

\[
\kappa
=
cH
=
\frac{c^2}{\alpha}.
\]

The associated Gibbons–Hawking temperature is

\[
T_{\text{dS}}
=
\frac{\hbar \kappa}{2\pi k_{\text{B}} c}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

For the observed cosmological constant, this temperature is extraordinarily small:

\[
T_{\text{dS}}
\sim
10^{-30}\,\text{K}.
\]

Nevertheless, it is conceptually decisive. De Sitter space is thermal.

The Euclidean continuation of the static metric,

\[
t \to -i\tau_E,
\]

requires periodicity

\[
\tau_E \sim \tau_E + \beta,
\]

with

\[
\beta
=
\frac{1}{k_{\text{B}}T_{\text{dS}}}
=
\frac{2\pi}{H}.
\]

This periodicity is the geometric origin of the horizon temperature.

---

## 6. de Sitter Entropy

The horizon area is

\[
A_{\text{horizon}}
=
4\pi \alpha^2
=
\frac{12\pi}{\Lambda}.
\]

The Bekenstein–Hawking entropy is

\[
S_{\text{dS}}
=
\frac{k_{\text{B}} A_{\text{horizon}}}{4G\hbar/c^3}
=
\frac{k_{\text{B}} c^3 A_{\text{horizon}}}{4G\hbar}.
\]

Substituting the area gives

\[
S_{\text{dS}}
=
\frac{3\pi k_{\text{B}} c^3}{G\hbar \Lambda}.
\]

In natural units,

\[
c=\hbar=k_{\text{B}}=1,
\]

this becomes

\[
S_{\text{dS}}
=
\frac{3\pi}{G\Lambda}.
\]

For the observed value of \(\Lambda\),

\[
S_{\text{dS}}
\sim
10^{122} k_{\text{B}}.
\]

This is finite but enormous.

The finiteness of de Sitter entropy suggests that the number of independent quantum states accessible to a single observer is bounded:

\[
\dim \mathcal{H}_{\text{observer}}
\lesssim
\exp
\left(
S_{\text{dS}}/k_{\text{B}}
\right).
\]

This is one of the most profound clues to quantum gravity.

---

## 7. The Absence of a Global S-Matrix

In Minkowski space, scattering theory is formulated using asymptotic particle states at past and future infinity. One defines an S-matrix,

\[
S_{fi}
=
\langle f_{\text{out}} | i_{\text{in}} \rangle.
\]

In anti-de Sitter space, although there is no global S-matrix in the same sense, boundary correlators provide a precise holographic observable.

De Sitter space is more difficult.

It has no spatial infinity where asymptotic particle states can be prepared and measured by a single observer. Its future and past infinities are spacelike. Every observer is surrounded by a cosmological horizon. No observer can access the entire spacetime.

Therefore:

\[
\boxed{
\text{De Sitter space does not admit a conventional global S-matrix.}
}
\]

This is not a technical limitation. It is a structural feature of positive cosmological constant.

The observable universe is not the whole universe.

Physical questions must be reformulated in terms of:

1. horizon-relative observables,
2. static-patch correlation functions,
3. cosmological boundary correlators,
4. conditional probabilities within a causal diamond,
5. observer-dependent thermal ensembles.

This is the central methodological shift of de Sitter Relativity.

---

## 8. Horizon-Centered Observables

In de Sitter Relativity, the basic observational unit is the causal diamond of an observer.

Let \(\gamma\) be the worldline of an observer at \(r=0\) in the static patch. The observer’s accessible region is

\[
\mathcal{D}_\gamma
=
J^+(\gamma_{\text{past}})
\cap
J^-(\gamma_{\text{future}}),
\]

where \(J^\pm\) denote causal future and past.

Physical observables are associated with this region:

\[
\mathcal{O}
\in
\mathcal{A}(\mathcal{D}_\gamma),
\]

where \(\mathcal{A}(\mathcal{D}_\gamma)\) is the algebra of observables in the causal diamond.

Global observables, if they exist, are not directly accessible to a single observer.

The principle of de Sitter Relativity is therefore:

\[
\boxed{
\text{Observables are defined relative to an observer’s horizon.}
}
\]

This is the cosmological generalization of relational observables.

---

## 9. Static-Patch Thermodynamics

The static patch is naturally described by a thermal density matrix.

The timelike Killing vector inside the horizon is

\[
\xi^\mu
=
\left(
\frac{\partial}{\partial t}
\right)^\mu.
\]

The associated Hamiltonian generates time translations for the static observer. The equilibrium state is thermal:

\[
\rho
=
\frac{e^{-\beta H_\xi}}{Z},
\]

with

\[
\beta
=
\frac{2\pi}{H}.
\]

The entropy of this thermal state is the de Sitter entropy.

This suggests that the static patch behaves like a finite thermodynamic system.

The analogy may be summarized as:

\[
\text{static patch}
\sim
\text{thermal cavity},
\]

\[
\text{cosmological horizon}
\sim
\text{heat bath boundary},
\]

\[
S_{\text{dS}}
\sim
\text{maximum entropy}.
\]

This thermodynamic structure is not optional. It follows from quantum field theory in de Sitter space and from horizon geometry.

---

## 10. Quantum Fields in de Sitter Space

Quantum field theory in de Sitter space already reveals the horizon-centered nature of the theory.

A scalar field \(\phi\) satisfies

\[
\left(
\Box - m^2 - \xi R
\right)
\phi
=
0,
\]

where \(\xi\) is the curvature coupling.

In flat slicing, the mode functions obey

\[
\phi_k''
+
2\mathcal{H}\phi_k'
+
\left(
k^2 + a^2 m^2 + \xi a^2 R
\right)
\phi_k
=
0,
\]

where primes denote derivatives with respect to conformal time and

\[
\mathcal{H}
=
a'/a.
\]

The Bunch–Davies vacuum is selected by requiring regularity on the Euclidean de Sitter sphere and positive-frequency behavior at early times.

For a light scalar field, quantum fluctuations are stretched beyond the horizon. Their power spectrum freezes at

\[
\mathcal{P}_\phi(k)
\sim
\left(
\frac{H}{2\pi}
\right)^2.
\]

This is the mechanism underlying inflationary perturbations.

A static observer detects the Bunch–Davies vacuum as a thermal state with temperature

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

Thus the horizon is not merely geometric. It is thermodynamic and quantum-informational.

---

## 11. Infrared Issues and de Sitter Instability

De Sitter space contains subtle infrared phenomena.

Massless minimally coupled scalar fields do not possess a fully de Sitter-invariant vacuum. Their variance grows secularly:

\[
\langle \phi^2 \rangle
\sim
\frac{H^3 t}{4\pi^2}.
\]

This infrared growth is central to stochastic inflation.

It also raises the question of whether exact de Sitter space is stable over arbitrarily long times. Possible interpretations include:

1. exact de Sitter is an idealization,
2. infrared effects are gauge artifacts,
3. backreaction modifies the asymptotic state,
4. quantum gravity does not admit stable eternal de Sitter space.

This remains an open problem.

Nevertheless, for observational cosmology, quasi-de Sitter states are well defined and empirically successful.

---

## 12. Inflation as Quasi-de Sitter Physics

The early universe appears to have undergone a quasi-de Sitter phase.

During inflation,

\[
H \approx \text{constant},
\]

but not exactly. The slow-roll parameter is

\[
\epsilon
=
-\frac{\dot H}{H^2}
\ll 1.
\]

The scale factor grows approximately as

\[
a(t)
\propto
e^{Ht}.
\]

Quantum fluctuations of the inflaton and metric generate primordial perturbations.

The scalar power spectrum is

\[
\mathcal{P}_{\mathcal{R}}
=
\frac{H^2}{8\pi^2 \epsilon M_{\text{Pl}}^2},
\]

where

\[
M_{\text{Pl}}
=
\sqrt{\frac{\hbar c}{8\pi G}}
\]

is the reduced Planck mass in natural units.

The tensor power spectrum is

\[
\mathcal{P}_t
=
\frac{2H^2}{\pi^2 M_{\text{Pl}}^2}.
\]

The tensor-to-scalar ratio is

\[
r
=
16\epsilon.
\]

The scalar spectral index is

\[
n_s - 1
=
-6\epsilon + 2\eta,
\]

where

\[
\eta
=
\frac{\dot \epsilon}{H\epsilon}.
\]

These observables are relics of quasi-de Sitter geometry.

Thus de Sitter Relativity is not only about the late universe. It is also about the earliest observable epoch.

---

## 13. Late-Time Cosmology and the Approach to de Sitter Space

In \(\Lambda\)CDM, the Friedmann equation is

\[
H^2
=
\frac{8\pi G}{3}\rho
+
\frac{\Lambda c^2}{3}
-
\frac{kc^2}{a^2}.
\]

Matter density scales as

\[
\rho_m \propto a^{-3},
\]

radiation as

\[
\rho_r \propto a^{-4},
\]

while vacuum energy remains constant:

\[
\rho_\Lambda = \text{constant}.
\]

Therefore, at late times,

\[
\rho_\Lambda
\gg
\rho_m,
\rho_r.
\]

The universe approaches

\[
H^2
\to
\frac{\Lambda c^2}{3},
\]

and the scale factor behaves as

\[
a(t)
\propto
e^{Ht}.
\]

This is asymptotic de Sitter expansion.

The cosmic no-hair theorem supports this picture: in the presence of a positive cosmological constant, many anisotropies and inhomogeneities decay, and the universe approaches de Sitter space.

Thus, if dark energy is a true cosmological constant, de Sitter space is the future attractor of our universe.

---

## 14. The Cosmological Constant Problem

The observed value of \(\Lambda\) is tiny in Planck units.

The dimensionless quantity is approximately

\[
\Lambda \ell_{\text{P}}^2
\sim
10^{-122}.
\]

Equivalently, the vacuum energy density is

\[
\rho_\Lambda c^2
\sim
(2.3\,\text{meV})^4.
\]

Quantum field theory suggests vacuum contributions of order

\[
\rho_{\text{vac}}
\sim
M^4,
\]

where \(M\) is a cutoff scale. If \(M\sim M_{\text{Pl}}\), the discrepancy is roughly

\[
10^{120}.
\]

This is the cosmological constant problem.

De Sitter Relativity does not solve this problem. But it makes the problem unavoidable.

A universe with positive \(\Lambda\) forces us to confront:

1. vacuum energy,
2. horizon entropy,
3. finite observational access,
4. quantum gravity in cosmological spacetime,
5. the measure problem in eternal expansion.

The cosmological constant is not a minor parameter. It is a window into quantum spacetime.

---

## 15. Black Holes in de Sitter Space

De Sitter Relativity also modifies black-hole physics.

The Schwarzschild–de Sitter metric is

\[
ds^2
=
-
f(r)c^2dt^2
+
f(r)^{-1}dr^2
+
r^2d\Omega^2,
\]

with

\[
f(r)
=
1
-
\frac{2GM}{c^2 r}
-
H^2 r^2.
\]

There are two horizons:

1. a black-hole horizon at small \(r\),
2. a cosmological horizon at large \(r\).

The horizons are roots of

\[
f(r)=0.
\]

There is a maximum black-hole mass compatible with de Sitter space. When the black-hole and cosmological horizons coincide, one reaches the Nariai solution.

The condition is approximately

\[
GMH
\leq
\frac{1}{3\sqrt{3}}.
\]

This bound reflects the finite size of the de Sitter static patch.

Black holes in de Sitter space are therefore not isolated asymptotic objects. They exist inside a finite cosmological cavity.

---

## 16. de Sitter Holography

The finite entropy of de Sitter space strongly suggests a holographic description.

However, de Sitter holography is less developed than AdS/CFT.

Several proposals exist.

### 16.1 dS/CFT

The dS/CFT proposal relates quantum gravity in de Sitter space to a Euclidean conformal field theory on future infinity:

\[
\text{Gravity on } \text{dS}_{d+1}
\quad
\longleftrightarrow
\quad
\text{Euclidean CFT}_d.
\]

The future boundary is spacelike. Bulk wavefunctionals are related to boundary partition functions:

\[
\Psi_{\text{dS}}[\phi_0]
=
Z_{\text{CFT}}[\phi_0].
\]

For de Sitter space, the Euclidean continuation is a sphere \(S^{d+1}\), suggesting a connection with Euclidean CFT correlators.

However, candidate dual CFTs are often nonunitary, and a complete microscopic model remains lacking.

### 16.2 Static-Patch Holography

Another approach assigns fundamental degrees of freedom to the cosmological horizon of a static observer.

The entropy bound,

\[
S_{\text{dS}}
=
\frac{A}{4G\hbar},
\]

suggests that the Hilbert space of the static patch has dimension

\[
\dim \mathcal{H}_{\text{SP}}
\sim
e^{S_{\text{dS}}}.
\]

Observables are then horizon-relative.

This approach is naturally observer-centered and compatible with the absence of a global S-matrix.

### 16.3 dS/dS Correspondence

The dS/dS correspondence relates de Sitter space in \(d+1\) dimensions to a lower-dimensional de Sitter space in \(d\) dimensions, often through domain-wall constructions.

This reflects the idea that holography with positive cosmological constant may involve lower-dimensional cosmologies rather than ordinary non-gravitational field theories.

---

## 17. Algebraic Observables and the Static Patch

A rigorous formulation of de Sitter Relativity benefits from algebraic quantum field theory.

Let \(\mathcal{A}(\mathcal{O})\) be the algebra of observables associated with a region \(\mathcal{O}\). In ordinary local quantum field theory, local algebras are typically type III von Neumann algebras. Type III algebras do not possess a normalizable trace and cannot describe finite entropy states in the usual way.

When gravity is included, and when one restricts to a gravitating observer’s causal diamond, the algebra may be modified. Recent work suggests that the algebra of observables in a de Sitter static patch may become type II\(_1\), allowing a finite trace and a natural notion of entropy.

This is conceptually important because de Sitter entropy is finite.

A type II\(_1\) algebra can support a density matrix with finite entropy while retaining infinitely many degrees of freedom in a regulated sense.

Thus the mathematical structure of horizon-centered observables may be fundamentally different from ordinary quantum field theory.

---

## 18. Finite Hilbert Space and Quantum Cosmology

If de Sitter entropy is interpreted literally, the Hilbert space accessible to a single observer is finite-dimensional:

\[
\dim \mathcal{H}_{\text{dS}}
\sim
\exp
\left(
\frac{3\pi}{G\Lambda}
\right).
\]

This leads to a radical possibility:

\[
\boxed{
\text{Quantum gravity in de Sitter space may be finite-dimensional.}
}
\]

A finite-dimensional Hilbert space would imply:

1. no exact continuous global symmetries,
2. Poincaré recurrences,
3. thermalization,
4. limitations on eternal inflation,
5. a discrete spectrum of cosmological observables.

However, finite-dimensional quantum gravity in de Sitter space is difficult to reconcile with exact de Sitter symmetry and with conventional quantum field theory. The issue remains unresolved.

De Sitter Relativity treats the finite entropy bound as fundamental data, while leaving the precise microscopic interpretation open.

---

## 19. de Sitter Relativity as a Kinematic Framework

There is also a more direct sense in which de Sitter space can define a new relativity.

Special relativity is based on the Poincaré group. If the cosmological constant is fundamental, the vacuum symmetry group is instead

\[
SO(1,4).
\]

One may formulate a de Sitter-invariant kinematics in which the de Sitter radius \(\alpha\) is a universal length scale, alongside \(c\).

In the limit

\[
\alpha \to \infty,
\]

or equivalently

\[
\Lambda \to 0,
\]

the de Sitter group contracts to the Poincaré group, and ordinary special relativity is recovered.

In this view, Minkowski space is not the fundamental vacuum. It is the zero-curvature limit of de Sitter space.

This kinematic interpretation is not required for cosmological de Sitter Relativity, but it reinforces the conceptual point:

\[
\boxed{
\Lambda \text{ may be as fundamental as } c.
}
\]

---

## 20. Observational Status

The observational evidence for a positive cosmological constant is strong.

The standard \(\Lambda\)CDM model fits:

1. Type Ia supernova luminosity distances,
2. cosmic microwave background anisotropies,
3. baryon acoustic oscillations,
4. large-scale structure growth,
5. weak gravitational lensing.

Current observations are consistent with a dark-energy equation of state

\[
w \approx -1.
\]

The Hubble tension and possible hints of evolving dark energy remain active research topics, but the simplest interpretation remains a positive cosmological constant.

If future observations confirm \(w=-1\) with high precision, de Sitter Relativity becomes not merely a theoretical framework but an empirical necessity.

---

## 21. Relation to Earlier Versions of Relativity

De Sitter Relativity is deeply connected to the preceding versions.

| Version | Central Idea |
|---|---|
| Relativity 3.0: Effective Quantum Relativity | Gravity is a low-energy quantum effective field theory |
| Relativity 4.0: Background-Independent Quantum Geometry | Geometry itself is quantum |
| Relativity 5.0: Holographic Relativity | Bulk geometry emerges from boundary entanglement |
| Relativity 6.0: Thermodynamic Relativity | Einstein equations are equations of state |
| Relativity 7.0: Quantum Reference Frames | Observers and frames are quantum systems |
| Relativity 8.0: de Sitter Relativity | Positive \(\Lambda\) and horizons define physical observables |

The conceptual progression is:

\[
\text{relativity of inertial frames}
\rightarrow
\text{relativity of coordinates}
\rightarrow
\text{relativity of quantum geometry}
\rightarrow
\text{relativity of entanglement}
\rightarrow
\text{relativity of thermodynamic horizons}
\rightarrow
\text{relativity of quantum observers}
\rightarrow
\text{relativity of cosmological horizons}.
\]

De Sitter Relativity is the cosmological culmination of this sequence.

---

## 22. Axioms of de Sitter Relativity

The theory may be organized around six axioms.

### Axiom 1: Positive \(\Lambda\) Is Fundamental

The cosmological constant is not an optional addition. It defines the vacuum structure:

\[
\Lambda > 0.
\]

### Axiom 2: The Vacuum Is de Sitter Space

The maximally symmetric vacuum is de Sitter space, not Minkowski space.

### Axiom 3: Observers Are Horizon-Bounded

Every observer has access only to a static patch or causal diamond.

### Axiom 4: Observables Are Horizon-Relative

Physical observables belong to the algebra of the observer’s accessible region:

\[
\mathcal{O}
\in
\mathcal{A}(\mathcal{D}_\gamma).
\]

### Axiom 5: Horizon Entropy Bounds Information

The number of accessible states is bounded by

\[
S_{\text{dS}}
=
\frac{A_{\text{horizon}}}{4G\hbar}.
\]

### Axiom 6: Cosmology Is Foundational

Cosmology is not an application of relativity to the universe. It is the sector of relativity that defines the observable arena.

---

## 23. Conceptual Interpretation

De Sitter Relativity changes the meaning of spacetime observables.

In Minkowski space, one imagines ideal observers extending to infinity. Scattering experiments can be defined globally. The universe is, in principle, observable without limit.

In de Sitter space, this picture fails.

Every observer is enclosed by a horizon. The observable region is finite. The entropy is finite. The thermal temperature is nonzero. The global state is not fully accessible.

The new principle is:

\[
\boxed{
\text{Physics is the theory of what can be observed within a cosmological horizon.}
}
\]

This does not imply solipsism. Different observers have overlapping causal diamonds, and their descriptions must be mutually consistent where they overlap. But no observer has access to a God’s-eye view.

In this sense, de Sitter Relativity is the cosmological version of relational physics.

---

## 24. What Einstein Would Think

Einstein introduced the cosmological constant in 1917 to construct a static universe. The attempt failed observationally, and the term was later often dismissed.

If Einstein were alive today, he would see that \(\Lambda\) did not disappear. It returned as the dominant component of the universe.

He would likely regard the cosmological constant not as a blunder, but as a clue.

The clue is threefold:

1. vacuum energy gravitates,
2. horizons carry entropy,
3. the universe has a finite information capacity.

Einstein’s own work laid the foundations for all three: general relativity, black-hole-like horizon structure through the equivalence principle, and statistical thermodynamics.

He might resist the idea that physics is fundamentally observer-bound. His realism sought objective laws independent of observers. But de Sitter Relativity does not abandon objectivity. It redefines it as invariance under changes of horizon-relative description.

The laws remain objective. The observables are relational.

This is a deeply Einsteinian conclusion.

---

## 25. Open Problems

De Sitter Relativity is not complete. Major open problems remain.

### 25.1 Microscopic Origin of de Sitter Entropy

What are the degrees of freedom counted by

\[
S_{\text{dS}}
=
\frac{A}{4G\hbar}?
\]

### 25.2 Exact de Sitter in Quantum Gravity

Does stable, eternal de Sitter space exist in a complete theory of quantum gravity?

### 25.3 Holographic Dual

What is the precise holographic description of de Sitter space?

### 25.4 Finite-Dimensional Hilbert Space

Is the static-patch Hilbert space finite-dimensional? If so, how does approximate quantum field theory emerge?

### 25.5 Cosmological Constant Problem

Why is \(\Lambda\) so small but nonzero?

### 25.6 Measure Problem

How are probabilities defined in eternally inflating or asymptotically de Sitter spacetimes?

### 25.7 Observational Dark Energy

Is dark energy exactly \(\Lambda\), or does it evolve?

These questions define the research frontier of Relativity 8.0.

---

## 26. Summary of Core Equations

### Einstein equation with cosmological constant

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
\frac{8\pi G}{c^4}T_{\mu\nu}.
\]

### Vacuum curvature

\[
R_{\mu\nu}
=
\Lambda g_{\mu\nu},
\qquad
R=4\Lambda.
\]

### de Sitter radius

\[
\alpha
=
\sqrt{\frac{3}{\Lambda}}.
\]

### Hubble parameter

\[
H
=
c\sqrt{\frac{\Lambda}{3}}.
\]

### Static-patch metric

\[
ds^2
=
-
\left(
1-\frac{r^2}{\alpha^2}
\right)
c^2dt^2
+
\left(
1-\frac{r^2}{\alpha^2}
\right)^{-1}
dr^2
+
r^2d\Omega^2.
\]

### Horizon area

\[
A_{\text{horizon}}
=
4\pi\alpha^2
=
\frac{12\pi}{\Lambda}.
\]

### Gibbons–Hawking temperature

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

### de Sitter entropy

\[
S_{\text{dS}}
=
\frac{k_{\text{B}} c^3 A_{\text{horizon}}}{4G\hbar}
=
\frac{3\pi k_{\text{B}} c^3}{G\hbar\Lambda}.
\]

### Vacuum energy density

\[
\rho_\Lambda c^2
=
\frac{\Lambda c^4}{8\pi G}.
\]

### Equation of state

\[
w=-1.
\]

### Friedmann equation

\[
H^2
=
\frac{8\pi G}{3}\rho
+
\frac{\Lambda c^2}{3}
-
\frac{kc^2}{a^2}.
\]

---

## 27. Conclusion

Relativity 8.0, de Sitter Relativity, is the relativistic framework appropriate to a universe with positive cosmological constant.

Its central facts are:

1. the vacuum is de Sitter space,
2. every observer has a cosmological horizon,
3. the horizon has finite entropy,
4. the static patch is thermal,
5. global S-matrix observables are unavailable,
6. physical observables are horizon-relative,
7. cosmology is foundational.

The cosmological constant is no longer an optional term. It defines the geometry, thermodynamics, and information structure of the observable universe.

The defining equation of de Sitter Relativity is not merely the Einstein equation with \(\Lambda\). It is the horizon-entropy relation:

\[
S_{\text{dS}}
=
\frac{A_{\text{horizon}}}{4G\hbar}.
\]

The defining principle is:

\[
\boxed{
\text{The observable universe is a finite, horizon-bounded, thermodynamic quantum system.}
}
\]

Einstein introduced \(\Lambda\) to hold the universe still. Modern physics has discovered that \(\Lambda\) instead drives the universe toward a horizon-dominated quantum state.

This is de Sitter Relativity.

---

## Appendix A: de Sitter Embedding and Curvature

De Sitter space is the hyperboloid

\[
-X_0^2
+
X_1^2
+
X_2^2
+
X_3^2
+
X_4^2
=
\alpha^2
\]

in \(\mathbb{R}^{1,4}\).

The induced metric is maximally symmetric. Its Riemann tensor is

\[
R_{\mu\nu\rho\sigma}
=
\frac{1}{\alpha^2}
\left(
g_{\mu\rho}g_{\nu\sigma}
-
g_{\mu\sigma}g_{\nu\rho}
\right).
\]

Contracting gives

\[
R_{\mu\nu}
=
\frac{3}{\alpha^2}g_{\mu\nu},
\]

and

\[
R
=
\frac{12}{\alpha^2}.
\]

Since

\[
\alpha^2
=
\frac{3}{\Lambda},
\]

one obtains

\[
R_{\mu\nu}
=
\Lambda g_{\mu\nu},
\qquad
R=4\Lambda.
\]

---

## Appendix B: Static-Patch Temperature from Euclidean Regularity

The static metric is

\[
ds^2
=
-
f(r)c^2dt^2
+
f(r)^{-1}dr^2
+
r^2d\Omega^2,
\]

with

\[
f(r)
=
1-\frac{r^2}{\alpha^2}.
\]

Near the horizon \(r=\alpha\), let

\[
r=\alpha-\epsilon.
\]

Then

\[
f(r)
\approx
\frac{2\epsilon}{\alpha}.
\]

The Euclidean near-horizon metric becomes approximately

\[
ds_E^2
\approx
\frac{2\epsilon}{\alpha}c^2dt_E^2
+
\frac{\alpha}{2\epsilon}d\epsilon^2
+
\alpha^2 d\Omega^2.
\]

Defining a radial coordinate \(\rho\) by

\[
\epsilon
=
\frac{\rho^2}{2\alpha},
\]

one obtains

\[
ds_E^2
\approx
d\rho^2
+
\left(
\frac{c}{\alpha}\rho
\right)^2
dt_E^2
+
\alpha^2 d\Omega^2.
\]

Regularity at \(\rho=0\) requires

\[
t_E
\sim
t_E
+
\frac{2\pi\alpha}{c}.
\]

Thus

\[
\beta
=
\frac{2\pi}{H},
\]

and

\[
T_{\text{dS}}
=
\frac{\hbar H}{2\pi k_{\text{B}}}.
\]

---

## Appendix C: Friedmann Equation with Vacuum Energy

The Friedmann equation is

\[
H^2
=
\frac{8\pi G}{3}\rho
+
\frac{\Lambda c^2}{3}
-
\frac{kc^2}{a^2}.
\]

The acceleration equation is

\[
\frac{\ddot a}{a}
=
-
\frac{4\pi G}{3}
\left(
\rho+\frac{3p}{c^2}
\right)
+
\frac{\Lambda c^2}{3}.
\]

For vacuum energy,

\[
p_\Lambda
=
-\rho_\Lambda c^2,
\]

so

\[
\rho_\Lambda+\frac{3p_\Lambda}{c^2}
=
-2\rho_\Lambda.
\]

Thus vacuum energy produces accelerated expansion:

\[
\frac{\ddot a}{a}
>
0.
\]

At late times, matter and radiation dilute, leaving

\[
H^2
\to
\frac{\Lambda c^2}{3}.
\]

---

## Appendix D: de Sitter Entropy in Planck Units

The Planck length is

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}.
\]

The de Sitter entropy is

\[
S_{\text{dS}}
=
\frac{k_{\text{B}} A}{4\ell_{\text{P}}^2}.
\]

Since

\[
A
=
4\pi\alpha^2,
\]

one has

\[
S_{\text{dS}}
=
\pi k_{\text{B}}
\frac{\alpha^2}{\ell_{\text{P}}^2}.
\]

Using

\[
\alpha^2
=
\frac{3}{\Lambda},
\]

this becomes

\[
S_{\text{dS}}
=
\frac{3\pi k_{\text{B}}}{\Lambda \ell_{\text{P}}^2}
=
\frac{3\pi k_{\text{B}} c^3}{G\hbar\Lambda}.
\]

The dimensionless entropy is therefore

\[
\frac{S_{\text{dS}}}{k_{\text{B}}}
=
\frac{3\pi}{\Lambda \ell_{\text{P}}^2}.
\]

---

## Selected References

1. A. Einstein, “Kosmologische Betrachtungen zur allgemeinen Relativitätstheorie,” *Sitzungsberichte der Königlich Preussischen Akademie der Wissenschaften* (1917).  
2. W. de Sitter, “On the Relativity of Rotation in Einstein’s Theory,” *Proceedings of the Royal Netherlands Academy of Arts and Sciences* **19**, 1217 (1917).  
3. G. Lemaître, “A Homogeneous Universe of Constant Mass and Increasing Radius Accounting for the Radial Velocity of Extra-Galactic Nebulae,” *Annales de la Société Scientifique de Bruxelles* **A47**, 49 (1927).  
4. G. W. Gibbons and S. W. Hawking, “Cosmological Event Horizons, Thermodynamics, and Particle Creation,” *Physical Review D* **15**, 2738 (1977).  
5. S. W. Hawking, “Particle Creation by Black Holes,” *Communications in Mathematical Physics* **43**, 199 (1975).  
6. J. D. Bekenstein, “Black Holes and Entropy,” *Physical Review D* **7**, 2333 (1973).  
7. T. S. Bunch and P. C. W. Davies, “Quantum Field Theory in de Sitter Space: Renormalization by Point-Splitting,” *Proceedings of the Royal Society A* **360**, 117 (1978).  
8. A. A. Starobinsky, “Stochastic de Sitter Inflationary Model,” *Lecture Notes in Physics* **246**, 107 (1986).  
9. A. G. Riess et al., “Observational Evidence from Supernovae for an Accelerating Universe and a Cosmological Constant,” *Astronomical Journal* **116**, 1009 (1998).  
10. S. Perlmutter et al., “Measurements of \(\Omega\) and \(\Lambda\) from 42 High-Redshift Supernovae,” *Astrophysical Journal* **517**, 565 (1999).  
11. Planck Collaboration, “Planck 2018 Results. VI. Cosmological Parameters,” *Astronomy & Astrophysics* **641**, A6 (2020).  
12. A. Strominger, “The dS/CFT Correspondence,” *Journal of High Energy Physics* **0110**, 034 (2001).  
13. E. Witten, “Quantum Gravity in de Sitter Space,” in *Strings 2001* (2002).  
14. T. Banks and W. Fischler, “M-Theory Observables for Cosmological Space-Times,” arXiv:hep-th/0102077.  
15. T. Banks, “Cosmological Breaking of Supersymmetry?” *International Journal of Modern Physics A* **16**, 910 (2001).  
16. R. Bousso, “Adventures in de Sitter Space,” in *Future Directions in Superconductor Electronics* (2002).  
17. R. Bousso, “Holography in General Space-Times,” *Journal of High Energy Physics* **9906**, 028 (1999).  
18. V. Chandrasekaran, R. Longo, G. Penington, and E. Witten, “An Algebra of Observables for de Sitter Space,” *Journal of High Energy Physics* **2023**, 082 (2023).  
19. G. W. Gibbons, “Aspects of Supergravity Theories,” in *Supersymmetry, Supergravity and Related Topics* (1985).  
20. R. M. Wald, “Asymptotic Behavior of Homogeneous Cosmological Models in the Presence of a Positive Cosmological Constant,” *Physical Review D* **28**, 2118 (1983).

# Relativity 42.0 — Scale Relativity  
## Covariance Under Changes of Resolution and the Relativity of Scale

**White paper / academic preprint**

---

## Abstract

Scale Relativity is the hypothesis that scale is not absolute. Physical laws should be formulated covariantly under changes of resolution. It extends renormalization-group thinking into a full relativistic principle: no resolution is privileged, and physical objectivity lies in invariance under scale transformations. Under a scale transformation,

\[
x
\rightarrow
\lambda x,
\]

fields transform with scaling dimensions,

\[
\phi(x)
\rightarrow
\lambda^{-\Delta}\phi(\lambda x),
\]

and couplings flow according to beta functions,

\[
\frac{dg_i}{d\ln\mu}
=
\beta_i(g).
\]

The central principle is:

\[
\boxed{
\text{No scale is privileged; physics is covariance under changes of resolution.}
}
\]

Scale Relativity unifies Wilsonian renormalization, effective field theory, critical phenomena, conformal field theory, trace anomalies, asymptotic safety, dimensional reduction in quantum gravity, fractal geometry, and scale-dependent spacetime into a single framework. It implies that what we call “the laws of physics” are often effective laws valid within a scale regime. The invariant is not a law at one scale but the flow of laws across scales. Spacetime itself may be fractal, scale-dependent, or effectively different at different resolutions.

---

## 1. Introduction

Physics has repeatedly discovered that what seemed absolute is frame-relative.

Special relativity made simultaneity frame-relative. General relativity made geometry coordinate-relative. Quantum reference frames made observers relative. Holography made locality relative. Logical relativity made logic internal to structure. Signature relativity made Euclidean and Lorentzian descriptions regime-relative.

Scale Relativity adds another fundamental relativization:

\[
\boxed{
\text{Scale is relative.}
}
\]

A description at one resolution is not the same as a description at another resolution.

Atoms are not planets. Quarks are not nuclei. Hydrodynamics is not molecular mechanics. Infrared physics is not ultraviolet physics.

Yet these descriptions are not unrelated. They are connected by scale transformations and renormalization-group flows.

The central insight is due largely to Kenneth Wilson: physical theories are not fixed equations valid at all scales. They are scale-dependent effective descriptions connected by flows in theory space.

Scale Relativity elevates this insight to a principle:

\[
\boxed{
\text{Physical law must be covariant under changes of resolution.}
}
\]

This does not mean that all scales are physically identical. It means that no scale is metaphysically privileged.

The invariant is the structure preserved under scale transformations.

---

## 2. Scale Transformations

A scale transformation rescales lengths:

\[
x
\rightarrow
x'
=
\lambda x.
\]

Equivalently, momenta rescale inversely:

\[
k
\rightarrow
k'
=
\lambda^{-1}k.
\]

Long distances correspond to small momenta. Short distances correspond to large momenta.

A field \(\phi(x)\) transforms with a scaling dimension \(\Delta\):

\[
\phi(x)
\rightarrow
\phi'(x')
=
\lambda^{-\Delta}\phi(x).
\]

Equivalently,

\[
\phi'(x)
=
\lambda^{-\Delta}\phi(\lambda^{-1}x).
\]

The scaling dimension \(\Delta\) determines how the field behaves under changes of resolution.

For a free scalar field in \(d\) spacetime dimensions, the canonical scaling dimension is

\[
\Delta_0
=
\frac{d-2}{2}.
\]

For a free fermion,

\[
\Delta_0
=
\frac{d-1}{2}.
\]

For a gauge field,

\[
\Delta_0
=
\frac{d-2}{2}.
\]

Interactions modify these dimensions through anomalous dimensions:

\[
\Delta
=
\Delta_0
+
\gamma(g).
\]

Thus scale behavior is dynamical.

---

## 3. Scaling of Correlation Functions

The meaning of scaling dimension is clearest in correlation functions.

At a scale-invariant fixed point, a two-point function behaves as

\[
\langle \phi(x)\phi(0)\rangle
\sim
\frac{1}{|x|^{2\Delta}}.
\]

Under

\[
x\rightarrow\lambda x,
\]

this transforms as

\[
\langle \phi(\lambda x)\phi(0)\rangle
\sim
\lambda^{-2\Delta}
\langle \phi(x)\phi(0)\rangle.
\]

More generally, an \(n\)-point function scales as

\[
\langle
\phi(x_1)\cdots\phi(x_n)
\rangle
\rightarrow
\lambda^{-\sum_i\Delta_i}
\langle
\phi(x_1)\cdots\phi(x_n)
\rangle.
\]

Thus scale invariance is not the statement that correlations are unchanged pointwise. It is the statement that they transform covariantly.

This is the first lesson of Scale Relativity:

\[
\boxed{
\text{Scale covariance replaces scale absoluteness.}
}
\]

---

## 4. Renormalization and the Flow of Couplings

In an interacting quantum field theory, couplings depend on the energy scale \(\mu\).

Let \(g_i(\mu)\) be dimensionless couplings. Their scale dependence is governed by beta functions:

\[
\frac{dg_i}{d\ln\mu}
=
\beta_i(g).
\]

This equation is the dynamical core of Scale Relativity.

It says that the laws at one scale are related to the laws at another scale by a flow.

A theory is not a point in theory space. It is a trajectory.

---

## 5. Derivation of the Beta Function

Consider a bare coupling \(g_0\), a renormalized coupling \(g(\mu)\), and a renormalization constant \(Z_g\):

\[
g_0
=
\mu^\epsilon
Z_g(g,\epsilon)
g.
\]

Here \(\epsilon=4-d\) in dimensional regularization.

The bare coupling is independent of the arbitrary renormalization scale \(\mu\):

\[
\mu\frac{d g_0}{d\mu}
=
0.
\]

Applying this condition gives

\[
0
=
\epsilon g
+
\beta(g)
+
g\beta(g)
\frac{\partial}{\partial g}
\ln Z_g.
\]

Solving for \(\beta(g)\) yields the beta function.

At one loop, many theories have beta functions of the form

\[
\beta(g)
=
-b_0 g^3
+
\mathcal{O}(g^5).
\]

For QCD,

\[
b_0
=
\frac{1}{16\pi^2}
\left(
\frac{11}{3}N_c
-
\frac{2}{3}N_f
\right).
\]

For \(N_c=3\) and sufficiently small \(N_f\), \(b_0>0\), so the coupling decreases at high energy:

\[
\alpha_s(\mu)
\sim
\frac{1}{b_0\ln(\mu^2/\Lambda_{\text{QCD}}^2)}.
\]

This is asymptotic freedom.

Thus the strong force is weak at short distances and strong at long distances.

The law is scale-relative.

---

## 6. Fixed Points and Universality

A fixed point satisfies

\[
\beta_i(g_*)=0.
\]

At a fixed point, the theory is scale-invariant.

Near a fixed point,

\[
g_i
=
g_{i*}
+
\delta g_i.
\]

Linearizing the beta functions gives

\[
\frac{d\delta g_i}{d\ln\mu}
=
M_{ij}\delta g_j,
\]

where

\[
M_{ij}
=
\left.
\frac{\partial\beta_i}{\partial g_j}
\right|_{g_*}.
\]

The eigenvalues classify operators:

1. relevant: eigenvalue positive, grows toward infrared,
2. irrelevant: eigenvalue negative, dies toward infrared,
3. marginal: eigenvalue zero, requires higher-order analysis.

This classification explains universality.

Many microscopic theories flow to the same infrared fixed point.

Their microscopic details are irrelevant in the technical renormalization-group sense.

Thus:

\[
\boxed{
\text{Universality is the covariance of physics under changes of microscopic resolution.}
}
\]

---

## 7. Effective Field Theory as Scale Relativity

Effective field theory is the practical embodiment of Scale Relativity.

At energies \(E\ll M\), one writes

\[
\mathcal{L}_{\text{eff}}
=
\mathcal{L}_{\text{ren}}
+
\sum_i
\frac{c_i}{M^{\Delta_i-4}}
\mathcal{O}_i.
\]

Here:

- \(\mathcal{O}_i\) are higher-dimensional operators,
- \(c_i\) are Wilson coefficients,
- \(M\) is the cutoff or heavy scale.

The effective theory does not need to know the ultraviolet details. Their effects are encoded in coefficients.

Predictions are organized as expansions in

\[
\frac{E}{M}.
\]

Thus the law at low energy is not the final law. It is the scale-covariant projection of a larger structure.

This is Scale Relativity in practice.

---

## 8. The Wilsonian Picture

Wilson’s renormalization group provides the deepest formulation.

Start with an action at cutoff \(\Lambda\):

\[
S_\Lambda[\phi].
\]

Integrate out modes in a momentum shell,

\[
\Lambda/b
<
|k|
<
\Lambda,
\]

and rescale:

\[
x\rightarrow x'=x/b,
\]

\[
\phi\rightarrow \phi'=b^{\Delta}\phi.
\]

The result is a new action,

\[
S_{\Lambda/b}[\phi'].
\]

This defines a transformation,

\[
\mathcal{R}_b:
S_\Lambda
\rightarrow
S_{\Lambda/b}.
\]

Repeated application generates a flow in theory space.

The invariant physical content is not one action. It is the orbit under renormalization-group transformations.

Thus:

\[
\boxed{
\text{A physical theory is an equivalence class of scale-related effective actions.}
}
\]

---

## 9. Exact Renormalization Group

The exact renormalization group gives a continuous formulation.

Let \(\Gamma_k\) be the effective average action at scale \(k\).

It satisfies the Wetterich equation,

\[
\partial_t\Gamma_k
=
\frac{1}{2}
\operatorname{Tr}
\left[
\left(
\Gamma_k^{(2)}
+
R_k
\right)^{-1}
\partial_t R_k
\right],
\]

where

\[
t=\ln k,
\]

\(\Gamma_k^{(2)}\) is the second functional derivative, and \(R_k\) is an infrared regulator.

This equation describes how the effective action changes as modes are integrated out.

It is a precise mathematical expression of Scale Relativity.

---

## 10. Callan–Symanzik Equation

In perturbative renormalized quantum field theory, scale covariance is expressed by the Callan–Symanzik equation.

For an \(n\)-point Green function \(G^{(n)}\),

\[
\left[
\mu\frac{\partial}{\partial\mu}
+
\beta(g)\frac{\partial}{\partial g}
+
n\gamma(g)
\right]
G^{(n)}
=
0.
\]

Here:

- \(\beta(g)\) is the beta function,
- \(\gamma(g)\) is the anomalous dimension.

This equation says that changes in renormalization scale are compensated by changes in couplings and field normalizations.

Thus physical correlation functions are scale-covariant.

---

## 11. Scale Covariance as a Relativity Principle

A relativity principle has three components:

1. a class of frames,
2. transformations between frames,
3. invariant quantities.

For Scale Relativity:

1. frames are resolutions \(\mu\),
2. transformations are renormalization-group flows,
3. invariants are physical observables along RG orbits.

A scale frame may be represented as

\[
F_\mu
=
\left(
\mu,
\mathcal{C}_\mu,
T_\mu
\right),
\]

where:

- \(\mu\) is the resolution,
- \(\mathcal{C}_\mu\) is a coarse-graining map,
- \(T_\mu\) is the effective theory at that scale.

A transformation between frames is

\[
F_\mu
\rightarrow
F_{\mu'}.
\]

Scale covariance requires that physical predictions satisfy

\[
P(O\mid F_\mu)
=
P(O'\mid F_{\mu'}).
\]

Thus:

\[
\boxed{
\text{Physical objectivity is invariance under changes of scale frame.}
}
\]

---

## 12. Scale Relativity and Conformal Symmetry

Scale transformations are a subgroup of conformal transformations.

A conformal transformation preserves angles:

\[
g_{\mu\nu}(x)
\rightarrow
\Omega^2(x)g_{\mu\nu}(x).
\]

A scale transformation is the special case,

\[
\Omega(x)=\lambda.
\]

At a renormalization-group fixed point, theories often become conformally invariant.

Conformal field theory is the mathematics of exact scale covariance.

Primary operators transform as

\[
\mathcal{O}(x)
\rightarrow
\lambda^{-\Delta}
\mathcal{O}(\lambda x).
\]

Their correlation functions are fixed by symmetry up to constants.

Thus conformal field theory is the limiting case of Scale Relativity where scale covariance becomes exact.

---

## 13. Trace Anomaly and Scale Breaking

Classical scale invariance is often broken by quantization.

The stress-energy tensor of a scale-invariant classical theory satisfies

\[
T^\mu{}_\mu=0.
\]

Quantum mechanically,

\[
T^\mu{}_\mu
=
\beta^i(g)\mathcal{O}_i
+
\text{curvature anomalies}.
\]

In four dimensions, the trace anomaly includes

\[
T^\mu{}_\mu
=
\beta^i\mathcal{O}_i
+
cW_{\mu\nu\rho\sigma}W^{\mu\nu\rho\sigma}
-
aE_4
+
b\square R.
\]

Here:

- \(W_{\mu\nu\rho\sigma}\) is the Weyl tensor,
- \(E_4\) is the Euler density,
- \(R\) is the scalar curvature.

Thus scale invariance can be anomalous.

Scale Relativity does not require exact scale invariance. It requires covariance under scale changes, including anomalies.

Anomalies are themselves scale-covariant invariants.

---

## 14. Local Scale Relativity and Weyl Covariance

Global scale transformations use constant \(\lambda\).

Local scale transformations use position-dependent \(\lambda(x)\), or equivalently,

\[
g_{\mu\nu}(x)
\rightarrow
e^{2\sigma(x)}g_{\mu\nu}(x).
\]

Fields transform as

\[
\phi(x)
\rightarrow
e^{-\Delta\sigma(x)}\phi(x).
\]

This is Weyl covariance.

A fully local Scale Relativity would formulate physics covariantly under local changes of scale.

This idea appears in:

1. conformal gravity,
2. Weyl geometry,
3. local renormalization group,
4. trace anomaly physics,
5. scale-invariant cosmology,
6. induced gravity models.

Whether local scale symmetry is fundamental or emergent remains open.

But the principle is clear:

\[
\boxed{
\text{Scale may be a gauge-like frame variable.}
}
\]

---

## 15. Fractal Geometry and Scale-Dependent Dimension

If scale is relative, spacetime itself may be scale-dependent.

Fractal geometry provides a model.

A fractal set has non-integer Hausdorff dimension,

\[
d_H
=
\lim_{\epsilon\to0}
\frac{\ln N(\epsilon)}
{\ln(1/\epsilon)},
\]

where \(N(\epsilon)\) is the number of boxes of size \(\epsilon\) needed to cover the set.

In quantum gravity, several approaches suggest that the effective dimension of spacetime runs with scale.

The spectral dimension is defined through a diffusion process.

Let \(K(x,x';s)\) be the heat kernel satisfying

\[
\partial_s K(x,x';s)
=
\Delta K(x,x';s).
\]

The return probability is

\[
P(s)
=
\int d^dx\sqrt{g}
K(x,x;s).
\]

The spectral dimension is

\[
d_s(s)
=
-2
\frac{d\ln P(s)}{d\ln s}.
\]

In many quantum-gravity models,

\[
d_s(s)
\rightarrow
4
\quad
\text{at large scales},
\]

but

\[
d_s(s)
\rightarrow
2
\quad
\text{at short scales}.
\]

Thus spacetime may be effectively four-dimensional in the infrared and effectively two-dimensional in the ultraviolet.

This is Scale Relativity applied to dimension itself.

---

## 16. Scale-Dependent Metrics

In asymptotic safety and related approaches, the effective action depends on scale:

\[
\Gamma_k[g,\Phi].
\]

The scale-dependent field equations may be written as

\[
\frac{\delta\Gamma_k}{\delta g_{\mu\nu}}
=
0.
\]

This yields scale-dependent couplings:

\[
G=G(k),
\]

\[
\Lambda=\Lambda(k).
\]

One may define a scale-dependent effective metric,

\[
g_{\mu\nu}(k).
\]

Thus geometry itself becomes scale-relative.

The line element,

\[
ds^2
=
g_{\mu\nu}(k)dx^\mu dx^\nu,
\]

depends on the resolution at which spacetime is probed.

This does not necessarily mean that spacetime is literally fractal. It means that its effective geometry is resolution-dependent.

---

## 17. Asymptotic Safety

Asymptotic safety proposes that quantum gravity possesses a nontrivial ultraviolet fixed point:

\[
\beta_G=0,
\]

\[
\beta_\Lambda=0,
\]

at high energy.

If so, gravity is nonperturbatively renormalizable.

The ultraviolet behavior is controlled by the fixed point, not by perturbation theory around a free theory.

Scale Relativity is central to asymptotic safety.

The theory is not defined at one scale. It is defined by its trajectory through theory space.

Thus:

\[
\boxed{
\text{Quantum gravity may be a scale-covariant fixed-point structure.}
}
\]

---

## 18. Scale Relativity and Critical Phenomena

Critical phenomena are the experimental triumph of Scale Relativity.

Near a continuous phase transition, correlation length diverges:

\[
\xi
\rightarrow
\infty.
\]

The system becomes scale-invariant.

Critical exponents describe scaling:

\[
C\sim |T-T_c|^{-\alpha},
\]

\[
M\sim |T-T_c|^{\beta},
\]

\[
\chi\sim |T-T_c|^{-\gamma},
\]

\[
G(r)\sim r^{-(d-2+\eta)}.
\]

Different microscopic systems share the same critical exponents if they belong to the same universality class.

Thus the microscopic details are irrelevant.

The invariant is the fixed-point structure.

Scale Relativity explains why universality exists.

---

## 19. Scale Relativity and Turbulence

Classical turbulence also exhibits scale relativity.

In Kolmogorov’s theory of turbulence, energy cascades from large scales to small scales.

In the inertial range, the energy spectrum scales as

\[
E(k)
\sim
\epsilon^{2/3}
k^{-5/3},
\]

where \(\epsilon\) is the energy dissipation rate.

This scaling law is approximately universal.

Turbulence is not exactly scale-invariant, but it is scale-covariant over a range of scales.

Thus Scale Relativity applies beyond quantum field theory.

---

## 20. Scale Relativity and Cosmology

Cosmology introduces another scale: the cosmic scale factor,

\[
a(t).
\]

This is not identical to renormalization-group scale, but the two are related in subtle ways.

Inflation produces nearly scale-invariant primordial fluctuations:

\[
\mathcal{P}_{\mathcal{R}}(k)
\sim
k^{n_s-1},
\]

with

\[
n_s
\approx
0.965.
\]

The slight departure from exact scale invariance encodes the dynamics of the early universe.

Cosmological observations therefore measure scale covariance in the primordial universe.

Scale Relativity also raises the question of whether the large-scale structure of the universe is fractal or homogeneous. Current evidence supports large-scale homogeneity, but scale-dependent structure remains important in galaxy clustering, turbulence, and cosmic web formation.

---

## 21. Scale Frames and Observers

Observers have finite resolution.

An observer is not a pointlike entity with access to all scales. An observer is a physical system with:

1. finite energy,
2. finite size,
3. finite measurement resolution,
4. finite memory,
5. finite computational capacity.

Thus every observation is scale-framed.

A measurement at resolution \(\mu\) accesses an effective theory \(T_\mu\).

The observer’s description is not the final description. It is the description relative to a scale frame.

Thus:

\[
\boxed{
\text{Observation is resolution-relative.}
}
\]

---

## 22. Scale Relativity and Effective Laws

Scale Relativity changes the meaning of law.

A law is not necessarily a fundamental equation valid at all scales.

It may be an effective invariant within a scale regime.

Examples:

1. Newtonian gravity is valid at low velocities and weak fields.
2. Fermi theory is valid below the electroweak scale.
3. Hydrodynamics is valid at long wavelengths.
4. Phonons are valid in lattice media.
5. Quasiparticles are valid in condensed matter systems.
6. Classical spacetime may be valid at large scales.

Thus:

\[
\boxed{
\text{Laws are scale-relative projections of deeper flows.}
}
\]

This connects Scale Relativity to Nomological Relativity.

---

## 23. Scale Relativity and Dimensional Relativity

Scale Relativity and Dimensional Relativity are closely related.

Dimensional Relativity says that dimension may be scale-dependent.

Scale Relativity says that laws, fields, couplings, and geometries are scale-dependent.

Together they imply:

\[
\boxed{
\text{Spacetime may have no absolute dimension or geometry independent of resolution.}
}
\]

The invariant is the flow of effective structures across scales.

---

## 24. Scale Relativity and Probability / Measure Relativity

Probability measures may also be scale-dependent.

Coarse-graining changes the space of events.

A microscopic probability distribution,

\[
P_{\text{micro}}(x),
\]

becomes a macroscopic distribution,

\[
P_{\text{macro}}(X),
\]

through coarse-graining:

\[
P_{\text{macro}}(X)
=
\int d x\,
\delta(X-C(x))
P_{\text{micro}}(x).
\]

Thus probability itself is scale-relative.

This connects Scale Relativity to Probability / Measure Relativity.

---

## 25. Formal Framework of Scale Relativity

Let \(\mathcal{T}\) be theory space.

Let \(\mu\) be a scale.

A scale frame is a point in an extended space,

\[
(\mu,T_\mu).
\]

The renormalization group defines a vector field on theory space:

\[
\beta
=
\beta^i(g)
\frac{\partial}{\partial g^i}.
\]

The flow is

\[
\frac{dg^i}{d\ln\mu}
=
\beta^i(g).
\]

Physical observables are functions on theory space that are invariant along RG orbits:

\[
\beta^i
\frac{\partial \mathcal{O}_{\text{phys}}}{\partial g^i}
=
0.
\]

Equivalently, physical quantities are functions of RG invariants.

Thus:

\[
\boxed{
\text{Reality is the invariant content of RG orbits.}
}
\]

---

## 26. Axioms of Scale Relativity

The framework may be organized around twelve axioms.

### Axiom 1: Scale Is a Frame

Resolution is not absolute. It is a frame variable.

### Axiom 2: Laws Are Scale-Dependent

Effective laws depend on resolution.

### Axiom 3: Couplings Flow

Couplings obey beta functions.

### Axiom 4: Fields Have Scaling Dimensions

Fields transform covariantly under scale transformations.

### Axiom 5: Fixed Points Define Scale Invariance

At fixed points, physics becomes scale-covariant or conformal.

### Axiom 6: Universality Is RG Invariance

Different microscopic theories may share infrared physics.

### Axiom 7: Effective Field Theory Is Fundamental Practice

Low-energy physics is organized by scale expansions.

### Axiom 8: Anomalies Are Invariants

Scale anomalies are physical and covariant.

### Axiom 9: Geometry May Be Scale-Dependent

Metrics and dimensions may run with scale.

### Axiom 10: Observers Are Resolution-Limited

Observation is always scale-framed.

### Axiom 11: Physical Objectivity Is RG Invariance

Objectivity is invariance under changes of scale frame.

### Axiom 12: Reflexivity Is Required

Scale relativity applies to its own scale of description.

---

## 27. Relation to Previous Relativities

Scale Relativity integrates earlier relativities.

| Relativity | Relation |
|---|---|
| Special Relativity | Frames of motion |
| General Relativity | Frames of geometry |
| Quantum Reference Frames | Quantum observers |
| Nomological Relativity | Laws may be effective |
| Dimensional Relativity | Dimension may be scale-dependent |
| Signature / Regime Relativity | Regimes are analytic frames |
| Probability / Measure Relativity | Measures may be coarse-grained |
| Scale Relativity | Resolution is relative |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative frames}
\rightarrow
\text{relative laws}
\rightarrow
\text{relative dimension}
\rightarrow
\text{relative scale}.
\]

---

## 28. Experimental and Observational Relevance

Scale Relativity is experimentally grounded.

### 28.1 Critical Exponents

Universality and scaling exponents are measured in magnets, fluids, superconductors, and cold atoms.

### 28.2 QCD Running

The running of the strong coupling \(\alpha_s(\mu)\) is measured across energies.

### 28.3 Electroweak Precision

Running couplings are tested in collider physics.

### 28.4 Effective Field Theory

Precision tests of the Standard Model use EFT expansions.

### 28.5 Cosmological Perturbations

The near-scale-invariance of primordial fluctuations is observed in the cosmic microwave background.

### 28.6 Quantum Gravity Hints

Dimensional reduction remains theoretical but may have indirect consequences for black holes, early-universe physics, and high-energy scattering.

Thus Scale Relativity is not speculative in its core. Its quantum-gravitational extensions are speculative, but its renormalization-group foundation is established.

---

## 29. Open Problems

Several major problems remain.

### 29.1 Local Scale Covariance

Can Scale Relativity be formulated as a fully local gauge principle?

### 29.2 Quantum Gravity Fixed Point

Does asymptotic safety provide a complete ultraviolet fixed point?

### 29.3 Fractal Spacetime

Is spacetime literally fractal, or only effectively scale-dependent?

### 29.4 Measure over Scales

Is there a natural measure over scale frames?

### 29.5 Observer Resolution

How should finite-resolution observers be formally incorporated?

### 29.6 Scale and Time

How does renormalization-group scale relate to cosmological time?

### 29.7 Anomalies and Emergence

How do scale anomalies constrain emergent spacetime?

### 29.8 Nonperturbative Definitions

Can exact RG flows be solved for realistic theories?

---

## 30. What Einstein Would Think

Einstein would appreciate Scale Relativity.

He sought invariant laws under transformations. Scale Relativity generalizes this demand to changes of resolution.

He might be cautious about fractal spacetime and quantum-gravity speculation.

But he would recognize the central principle:

\[
\boxed{
\text{Physical law must not depend on arbitrary choices of description.}
}
\]

If scale is an arbitrary choice of resolution, then physical law must be covariant under changes of scale.

This is a natural extension of general covariance.

Einstein might not have formulated renormalization-group theory, but he would respect its lesson.

---

## 31. Summary of Core Equations

### Scale transformation

\[
x\rightarrow\lambda x.
\]

### Field scaling

\[
\phi(x)
\rightarrow
\lambda^{-\Delta}\phi(\lambda x).
\]

### Two-point scaling

\[
\langle\phi(x)\phi(0)\rangle
\sim
|x|^{-2\Delta}.
\]

### Beta function

\[
\frac{dg_i}{d\ln\mu}
=
\beta_i(g).
\]

### Fixed point

\[
\beta_i(g_*)=0.
\]

### Callan–Symanzik equation

\[
\left[
\mu\frac{\partial}{\partial\mu}
+
\beta(g)\frac{\partial}{\partial g}
+
n\gamma(g)
\right]
G^{(n)}
=
0.
\]

### Wetterich equation

\[
\partial_t\Gamma_k
=
\frac{1}{2}
\operatorname{Tr}
\left[
\left(
\Gamma_k^{(2)}
+
R_k
\right)^{-1}
\partial_t R_k
\right].
\]

### Trace anomaly

\[
T^\mu{}_\mu
=
\beta^i\mathcal{O}_i
+
\text{anomalies}.
\]

### Spectral dimension

\[
d_s(s)
=
-2
\frac{d\ln P(s)}{d\ln s}.
\]

### Central principle

\[
\boxed{
\text{No scale is privileged; physics is covariance under changes of resolution.}
}
\]

---

## 32. Conclusion

Relativity 42.0, Scale Relativity, asserts that scale is not absolute.

Physical laws are not fixed equations valid identically at all resolutions. They are effective descriptions connected by renormalization-group flows.

Fields transform with scaling dimensions. Couplings flow. Fixed points define universality. Effective theories emerge at each scale. Geometry itself may run with resolution.

The central principle is:

\[
\boxed{
\text{No scale is privileged; physics is covariance under changes of resolution.}
}
\]

The invariant is not a law at one scale. It is the structure preserved across scales.

Scale Relativity completes another stage of the relativistic program.

Motion became relative. Geometry became relative. Frames became relative. Logic became relative. Signature became relative.

Now scale becomes relative.

What remains is not a privileged resolution, but the covariant flow of structure through all resolutions.

This is Scale Relativity.

---

## Appendix A: Scaling of a Free Scalar Field

The action for a free scalar in \(d\) dimensions is

\[
S
=
\int d^dx
\left[
\frac{1}{2}
\partial_\mu\phi\partial^\mu\phi
\right].
\]

Under

\[
x\rightarrow\lambda x,
\]

the measure transforms as

\[
d^dx\rightarrow\lambda^d d^dx.
\]

The derivative transforms as

\[
\partial_\mu\rightarrow\lambda^{-1}\partial_\mu.
\]

If

\[
\phi(x)\rightarrow\lambda^{-\Delta}\phi(\lambda x),
\]

then the kinetic term is invariant when

\[
\Delta=\frac{d-2}{2}.
\]

Thus the canonical scaling dimension is

\[
\Delta_0=\frac{d-2}{2}.
\]

---

## Appendix B: Beta Function from Bare Coupling Independence

Let

\[
g_0
=
\mu^\epsilon Z_g(g,\epsilon)g.
\]

Since \(g_0\) is independent of \(\mu\),

\[
0
=
\mu\frac{d g_0}{d\mu}.
\]

This gives

\[
0
=
\epsilon g
+
\beta(g)
+
g\beta(g)
\frac{\partial}{\partial g}
\ln Z_g.
\]

Solving for \(\beta(g)\) yields the renormalization-group beta function.

---

## Appendix C: Callan–Symanzik Equation

For a renormalized \(n\)-point function,

\[
G^{(n)}(x_i;g,\mu),
\]

scale covariance requires

\[
\left[
\mu\frac{\partial}{\partial\mu}
+
\beta(g)\frac{\partial}{\partial g}
+
n\gamma(g)
\right]
G^{(n)}
=
0.
\]

This expresses the fact that changes in \(\mu\) are compensated by changes in \(g\) and field normalization.

---

## Appendix D: Exact RG Equation

The effective average action \(\Gamma_k\) includes modes with momenta above \(k\).

Its flow is

\[
\partial_t\Gamma_k
=
\frac{1}{2}
\operatorname{Tr}
\left[
\left(
\Gamma_k^{(2)}
+
R_k
\right)^{-1}
\partial_t R_k
\right],
\]

with

\[
t=\ln k.
\]

This equation interpolates between microscopic action and full quantum effective action.

---

## Appendix E: Spectral Dimension

The heat kernel satisfies

\[
\partial_s K(x,x';s)
=
\Delta K(x,x';s).
\]

The return probability is

\[
P(s)
=
\int d^dx\sqrt{g}
K(x,x;s).
\]

The spectral dimension is

\[
d_s(s)
=
-2
\frac{d\ln P(s)}{d\ln s}.
\]

If

\[
P(s)\sim s^{-d_s/2},
\]

then \(d_s\) is the effective dimension probed by diffusion at scale \(s\).

---

## Selected References

1. K. G. Wilson, “Renormalization Group and Critical Phenomena,” *Physical Review B* **4**, 3174 (1971).  
2. K. G. Wilson and J. Kogut, “The Renormalization Group and the \(\epsilon\) Expansion,” *Physics Reports* **12**, 75 (1974).  
3. L. P. Kadanoff, “Scaling Laws for Ising Models near \(T_c\),” *Physics* **2**, 263 (1966).  
4. M. E. Fisher, “Renormalization Group Theory: Its Basis and Formulation in Statistical Physics,” *Reviews of Modern Physics* **70**, 653 (1998).  
5. J. Cardy, *Scaling and Renormalization in Statistical Physics* (Cambridge University Press, 1996).  
6. J. Zinn-Justin, *Quantum Field Theory and Critical Phenomena* (Oxford University Press, 2002).  
7. C. G. Callan, “Broken Scale Invariance in Scalar Field Theories,” *Physical Review D* **2**, 1541 (1970).  
8. K. Symanzik, “Small Distance Behaviour in Field Theory and Power Counting,” *Communications in Mathematical Physics* **18**, 227 (1970).  
9. D. J. Gross and F. Wilczek, “Ultraviolet Behavior of Non-Abelian Gauge Theories,” *Physical Review Letters* **30**, 1343 (1973).  
10. H. D. Politzer, “Reliable Perturbative Results for Strong Interactions?” *Physical Review Letters* **30**, 1346 (1973).  
11. S. Weinberg, “Ultraviolet Divergences in Quantum Theories of Gravitation,” in *General Relativity: An Einstein Centenary Survey* (Cambridge University Press, 1979).  
12. M. Reuter, “Nonperturbative Evolution Equation for Quantum Gravity,” *Physical Review D* **57**, 971 (1998).  
13. C. Wetterich, “Exact Evolution Equation for the Effective Potential,” *Physics Letters B* **301**, 90 (1993).  
14. J. Polchinski, “Renormalization and Effective Lagrangians,” *Nuclear Physics B* **231**, 269 (1984).  
15. H. Georgi, “Effective Field Theory,” *Annual Review of Nuclear and Particle Science* **43**, 209 (1993).  
16. S. Weinberg, *The Quantum Theory of Fields*, Vol. 2 (Cambridge University Press, 1996).  
17. P. Di Francesco, P. Mathieu, and D. Sénéchal, *Conformal Field Theory* (Springer, 1997).  
18. A. N. Kolmogorov, “The Local Structure of Turbulence in Incompressible Viscous Fluid for Very Large Reynolds Numbers,” *Doklady Akademii Nauk SSSR* **30**, 301 (1941).  
19. U. Frisch, *Turbulence: The Legacy of A. N. Kolmogorov* (Cambridge University Press, 1995).  
20. B. B. Mandelbrot, *The Fractal Geometry of Nature* (Freeman, 1982).  
21. L. Nottale, *Fractal Space-Time and Microphysics: Towards a Theory of Scale Relativity* (World Scientific, 1993).  
22. G. Calcagni, “Fractal Universe and Quantum Gravity,” *Physical Review Letters* **104**, 251301 (2010).  
23. J. Ambjørn, J. Jurkiewicz, and R. Loll, “Spectral Dimension of the Universe,” *Physical Review Letters* **95**, 171301 (2005).  
24. R. Loll, “Quantum Gravity from Causal Dynamical Triangulations: A Review,” *Classical and Quantum Gravity* **37**, 013001 (2020).  
25. M. Niedermaier and M. Reuter, “The Asymptotic Safety Scenario in Quantum Gravity,” *Living Reviews in Relativity* **9**, 5 (2006).

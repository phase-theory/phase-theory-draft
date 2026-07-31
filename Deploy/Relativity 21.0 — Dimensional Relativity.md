# Relativity 21.0 — Dimensional Relativity  
## The Scale-, State-, and Observer-Dependence of Spacetime Dimension

**White paper / academic preprint**

---

## Abstract

Dimensional Relativity is the hypothesis that the dimension of spacetime is not an absolute, fixed background parameter but an emergent, scale-dependent, state-dependent, and in some contexts observer-dependent quantity. In classical general relativity, spacetime is a four-dimensional Lorentzian manifold. In quantum gravity, however, different operational notions of dimension need not agree. Topological dimension, Hausdorff dimension, spectral dimension, causal-set dimension, entanglement dimension, thermodynamic dimension, and holographic dimension can all differ, especially near the Planck scale. A recurring result in several quantum-gravity approaches is that the spectral dimension runs from approximately four in the infrared to approximately two in the ultraviolet:

\[
d_s(k)
\rightarrow
4
\quad
\text{at large scales},
\]

\[
d_s(k)
\rightarrow
2
\quad
\text{at short scales}.
\]

This suggests that spacetime does not merely curve. Its effective dimensionality changes. The central principle is:

\[
\boxed{
\text{Dimension is scale-dependent, observer-dependent, and emergent.}
\]

Dimensional Relativity generalizes the relativistic program once more. Special relativity made simultaneity relative. General relativity made geometry relative. Quantum reference frames made observers relative. Holography made bulk locality relative. Dimensional Relativity makes the number of dimensions itself relative to the probe, the scale, the state, and the causal access of the observer.

---

## 1. Introduction

In ordinary physics, dimension is treated as a fixed integer. We say that spacetime is four-dimensional. Space is three-dimensional. Time is one-dimensional.

But what does “dimension” mean?

There is not one notion of dimension. There are many.

A topologist defines dimension by covering properties. A fractal geometer defines it by scaling of volume. A spectral analyst defines it by diffusion. A quantum information theorist defines it by entanglement scaling. A thermodynamicist defines it by density of states. A holographer defines it by boundary degrees of freedom. A causal-set theorist defines it by order-interval growth.

In classical smooth spacetime, all these notions agree. A four-dimensional Lorentzian manifold has topological dimension four, Hausdorff dimension four, spectral dimension four, and so on.

But in quantum gravity, spacetime may not be smooth. It may be discrete, fractal, causal, holographic, entanglement-generated, or code-subspace emergent. In such a regime, the different notions of dimension can separate.

Dimensional Relativity is the study of that separation.

Its central claim is:

\[
\boxed{
\text{There is no absolute dimension of spacetime. There are operational dimensions relative to probes and scales.}
}
\]

---

## 2. Why Dimension Might Not Be Fundamental

There are several reasons to expect dimension to be emergent.

First, quantum gravity likely modifies spacetime at the Planck length,

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}.
\]

At such scales, the manifold concept may fail.

Second, black-hole entropy scales with area, not volume:

\[
S_{\text{BH}}
=
\frac{k_{\text{B}}A}{4G\hbar}.
\]

This suggests that the effective number of degrees of freedom scales as if spacetime had one fewer dimension.

Third, several independent quantum-gravity approaches show dimensional reduction in the ultraviolet.

Fourth, holography shows that a bulk dimension can emerge from boundary renormalization-group structure.

Fifth, causal-set theory shows that dimension can be extracted from order-theoretic data rather than assumed.

Thus dimension may be like temperature: meaningful macroscopically, but emergent microscopically.

---

## 3. Topological Dimension

Topological dimension is the most classical notion.

For a manifold \(M\), the topological dimension is an integer \(d_{\text{top}}\) characterizing local coordinate charts:

\[
M \cong \mathbb{R}^{d_{\text{top}}}.
\]

For ordinary spacetime,

\[
d_{\text{top}}=4.
\]

Topological dimension is robust under continuous deformations. But it is also crude. It does not detect fractal structure, quantum fluctuations, or spectral behavior.

If spacetime is not a manifold at short distances, topological dimension may be ill-defined.

Thus topological dimension is useful in the classical regime but insufficient for quantum gravity.

---

## 4. Hausdorff Dimension

Hausdorff dimension measures how volume scales with distance.

Let \(V(r)\) be the volume of a ball of radius \(r\). If

\[
V(r)
\sim
r^{d_H},
\]

then \(d_H\) is the Hausdorff dimension.

Equivalently, if the number of boxes of size \(\epsilon\) needed to cover a set scales as

\[
N(\epsilon)
\sim
\epsilon^{-d_H},
\]

then \(d_H\) is the box-counting or Hausdorff dimension.

For a smooth four-dimensional manifold,

\[
d_H=4.
\]

For a fractal quantum geometry, \(d_H\) may be non-integer and scale-dependent:

\[
d_H=d_H(r).
\]

In causal dynamical triangulations, the large-scale Hausdorff dimension is approximately four, while the short-scale behavior may differ.

Thus:

\[
\boxed{
\text{Hausdorff dimension measures the scaling of geometric volume.}
}
\]

---

## 5. Spectral Dimension

The most important quantum-gravitational notion of dimension is spectral dimension.

Consider a diffusion process on a geometry. Let \(K(x,x';\sigma)\) be the heat kernel satisfying

\[
\frac{\partial}{\partial \sigma}
K(x,x';\sigma)
=
\Delta_x
K(x,x';\sigma),
\]

where \(\Delta\) is the Laplacian and \(\sigma\) is diffusion time.

The return probability is

\[
P(\sigma)
=
\frac{1}{V}
\int d^Dx\sqrt{g}\,
K(x,x;\sigma).
\]

On a smooth \(D\)-dimensional manifold,

\[
P(\sigma)
\sim
\sigma^{-D/2}.
\]

The spectral dimension is defined by

\[
d_s
=
-2
\frac{d\ln P(\sigma)}{d\ln\sigma}.
\]

More generally, one allows scale dependence:

\[
d_s(\sigma)
=
-2
\frac{d\ln P(\sigma)}{d\ln\sigma}.
\]

Equivalently, in terms of a momentum scale \(k\sim \sigma^{-1/2}\),

\[
d_s(k)
=
-2
\frac{d\ln P(k)}{d\ln k}.
\]

The spectral dimension measures how a quantum particle explores the geometry.

It is not necessarily equal to topological or Hausdorff dimension.

---

## 6. Spectral Dimension from Modified Kinetics

The spectral dimension can be computed from the scaling of the kinetic operator.

Suppose the effective Laplacian has eigenvalues scaling as

\[
\lambda(k)
\sim
k^\alpha.
\]

Then the return probability behaves as

\[
P(\sigma)
\sim
\int d^Dk\,
e^{-\sigma k^\alpha}.
\]

Scaling \(k\rightarrow \sigma^{-1/\alpha}q\) gives

\[
P(\sigma)
\sim
\sigma^{-D/\alpha}.
\]

Therefore,

\[
d_s
=
\frac{2D}{\alpha}.
\]

For an ordinary Laplacian,

\[
\alpha=2,
\]

so

\[
d_s=D.
\]

For a higher-derivative ultraviolet kinetic term,

\[
\alpha=4,
\]

in \(D=4\),

\[
d_s
=
\frac{2\cdot 4}{4}
=
2.
\]

Thus ultraviolet modification of the propagator from

\[
\frac{1}{k^2}
\quad
\rightarrow
\quad
\frac{1}{k^4}
\]

produces spectral dimensional reduction from four to two.

This simple calculation explains a recurring pattern in quantum gravity.

---

## 7. Dimensional Reduction in Quantum Gravity

Several independent approaches find

\[
d_s
\rightarrow
4
\quad
\text{in the infrared},
\]

\[
d_s
\rightarrow
2
\quad
\text{in the ultraviolet}.
\]

This is one of the most intriguing hints of universality in quantum gravity.

### 7.1 Causal Dynamical Triangulations

In causal dynamical triangulations, spacetime is approximated by simplicial geometries with a causal foliation.

Numerical simulations of the return probability show

\[
d_s(\sigma)
\approx
4
\quad
\text{at large diffusion time},
\]

and

\[
d_s(\sigma)
\approx
2
\quad
\text{at small diffusion time}.
\]

Thus the emergent large-scale universe is four-dimensional, while the microscopic quantum geometry behaves as if it were two-dimensional.

### 7.2 Asymptotic Safety

In the asymptotic-safety program, gravity possesses a nontrivial ultraviolet fixed point.

Near the fixed point, the effective average action acquires anomalous scaling. The graviton propagator and kinetic operator scale differently from their classical form.

The resulting spectral dimension runs from four to two.

This suggests that dimensional reduction is tied to ultraviolet completeness.

### 7.3 Hořava–Lifshitz Gravity

Hořava–Lifshitz gravity introduces anisotropic scaling between space and time:

\[
t\rightarrow b^z t,
\qquad
x\rightarrow b x.
\]

In \(3+1\) dimensions, the ultraviolet critical exponent is often taken to be

\[
z=3.
\]

The spectral dimension is then

\[
d_s
=
1+\frac{D_{\text{space}}}{z}
=
1+\frac{3}{3}
=
2.
\]

Thus dimensional reduction follows from anisotropic ultraviolet scaling.

### 7.4 Noncommutative Geometry and Other Approaches

Noncommutative geometries, loop quantum gravity inspired models, group field theory, multifractional spacetimes, and certain spin-foam models also exhibit effective dimensional reduction.

The recurrence of \(d_s\approx 2\) in the ultraviolet suggests that two-dimensional behavior may be a universal feature of quantum spacetime.

---

## 8. Why Two Dimensions?

Why does the ultraviolet spectral dimension so often approach two?

There are several possible explanations.

### 8.1 Power-Counting Renormalizability

Gravity is power-counting renormalizable in two dimensions. If the effective dimension becomes two at short distances, ultraviolet divergences may be softened.

### 8.2 Propagator Improvement

A \(1/k^4\) propagator improves ultraviolet behavior. In four topological dimensions, this corresponds to spectral dimension two.

### 8.3 Fixed-Point Structure

At a nontrivial renormalization-group fixed point, anomalous dimensions can force the effective kinetic operator to scale as \(k^4\).

### 8.4 Holographic Scaling

Two-dimensional behavior is also natural in holographic and conformal systems, where entropy and correlation structure are controlled by lower-dimensional degrees of freedom.

Thus the number two may be a convergence point of renormalizability, holography, and causal structure.

---

## 9. Walk Dimension and Fractal Geometry

For fractal or quantum geometries, one also introduces the walk dimension \(d_w\).

The mean-square displacement of a diffusing particle scales as

\[
\langle r^2(\sigma)\rangle
\sim
\sigma^{2/d_w}.
\]

On a smooth manifold,

\[
d_w=2.
\]

On anomalous geometries, \(d_w\neq 2\).

The spectral dimension, Hausdorff dimension, and walk dimension are related by

\[
d_s
=
\frac{2d_H}{d_w}.
\]

Thus spectral dimensional reduction can arise from fractal volume scaling, anomalous diffusion, or both.

This relation is useful in causal dynamical triangulations, causal sets, and multifractional models.

---

## 10. Causal-Set Dimension

In causal-set theory, spacetime is a locally finite partially ordered set,

\[
(C,\prec).
\]

Dimension must be extracted from causal order and counting.

One method is the Myrheim–Meyer dimension.

In \(d\)-dimensional Minkowski spacetime, the expected number of elements in a causal interval of proper time \(\tau\) is

\[
N
=
\rho V_d \tau^d,
\]

where \(\rho\) is the sprinkling density and \(V_d\) is the volume of the unit causal interval.

The number of causal relations inside the interval also scales with \(d\). By comparing the number of order relations to the number of elements, one can estimate \(d\).

Another method uses the longest chain. The length \(L\) of the longest chain between two causally related events scales as

\[
L
\sim
c_d
\rho^{1/d}
\tau.
\]

Solving for \(d\) gives a causal-set dimension estimator.

Thus:

\[
\boxed{
\text{In causal-set theory, dimension is order-theoretic and statistical.}
}
\]

It is not imposed. It is measured from causal structure.

---

## 11. Entanglement Dimension

Quantum information provides another notion of dimension.

Consider a spatial region \(A\) of linear size \(L\). In many local quantum field theories, the entanglement entropy obeys an area law:

\[
S(A)
\sim
L^{d-1}.
\]

One may define an entanglement scaling dimension by

\[
d_E
=
1+
\frac{d\ln S(A)}{d\ln L}.
\]

For an area law in \(d\) spatial dimensions,

\[
d_E=d.
\]

Including time, the corresponding spacetime dimension is

\[
d_E+1.
\]

In critical systems, logarithmic corrections appear. In holographic systems, the entanglement entropy is controlled by minimal surfaces:

\[
S(A)
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

The scaling of entanglement then encodes the emergent bulk dimension.

Tensor networks provide another entanglement dimension. In MERA, the network geometry is hyperbolic. The radial direction corresponds to scale. The effective dimension of the tensor network may differ from the physical boundary dimension.

Thus:

\[
\boxed{
\text{Entanglement structure defines an effective dimension.}
}
\]

---

## 12. Holographic Dimension

Holography suggests that the number of independent degrees of freedom in a gravitational region scales with boundary area.

For a region of radius \(R\) in \(D\)-dimensional spacetime, the boundary area scales as

\[
A
\sim
R^{D-2}.
\]

The entropy bound is

\[
S
\leq
\frac{k_{\text{B}}A}{4G\hbar/c^3}.
\]

Thus the entropy scales as

\[
S
\sim
R^{D-2}.
\]

One may define a holographic dimension by

\[
d_{\text{holo}}
=
\frac{d\ln S}{d\ln R}+1.
\]

For ordinary area scaling,

\[
d_{\text{holo}}
=
D-1.
\]

This is one less than the bulk spacetime dimension.

In AdS/CFT,

\[
\text{gravity in } \mathrm{AdS}_{d+1}
\quad
\cong
\quad
\mathrm{CFT}_d.
\]

The bulk has dimension \(d+1\), but the fundamental boundary theory has dimension \(d\). The extra radial dimension emerges from renormalization-group scale.

Thus:

\[
\boxed{
\text{Holographic dimension is the dimension of the independent information-carrying boundary.}
}
\]

---

## 13. Thermodynamic Dimension

Thermodynamic dimension is defined through the density of states.

If the density of states scales as

\[
\rho(E)
\sim
E^{d_{\text{th}}-1},
\]

then the partition function at inverse temperature \(\beta\) scales as

\[
Z(\beta)
\sim
\beta^{-d_{\text{th}}}.
\]

Equivalently,

\[
d_{\text{th}}
=
-
\frac{d\ln Z}{d\ln\beta}.
\]

For blackbody radiation in \(D\) spacetime dimensions, the energy density scales as

\[
u(T)
\sim
T^D.
\]

Thus thermodynamic measurements can infer an effective dimension.

In quantum gravity, the density of states may receive corrections from fractal geometry, holography, or dimensional reduction. The thermodynamic dimension may then differ from the topological dimension.

Black holes are especially important. Their entropy scales as area, suggesting a thermodynamic dimension lower than the naive bulk dimension.

---

## 14. Operator Dimension and Conformal Field Theory

In conformal field theory, fields have scaling dimensions \(\Delta\). These are not spacetime dimensions, but they are deeply related to geometry.

A scalar operator satisfies

\[
\langle
\mathcal{O}(x)
\mathcal{O}(0)
\rangle
\sim
\frac{1}{|x|^{2\Delta}}.
\]

The spectrum of operator dimensions encodes the geometry of the theory space.

In holography, bulk mass determines boundary scaling dimension:

\[
\Delta(\Delta-d)
=
m^2L^2.
\]

Thus the emergence of bulk geometry is tied to the scaling dimensions of boundary operators.

This provides another sense in which dimension is relational: bulk geometric dimension is encoded in the scaling structure of non-gravitational operators.

---

## 15. Observer-Dependent Dimension

Dimension may also depend on the observer.

An observer’s accessible region is limited by causal horizons. A Rindler observer, a black-hole exterior observer, and an infalling observer have different causal access to degrees of freedom.

The effective dimension of the accessible Hilbert space may therefore differ.

For example, a de Sitter static-patch observer has finite entropy,

\[
S_{\text{dS}}
=
\frac{3\pi}{G\Lambda}.
\]

The accessible Hilbert space has dimension roughly

\[
\dim\mathcal{H}_{\text{dS}}
\sim
e^{S_{\text{dS}}}.
\]

This finite information capacity suggests that the effective dimensionality of observable physics is horizon-relative.

Similarly, a high-energy probe may access ultraviolet spectral dimension two, while a low-energy probe sees infrared spectral dimension four.

Thus:

\[
\boxed{
\text{Dimension is relative to the causal and energetic access of the observer.}
}
\]

---

## 16. Scale-Dependent Dimension as a Running Quantity

The most useful formulation treats dimension as a running quantity.

Define a scale-dependent spectral dimension,

\[
d_s(k)
=
-2
\frac{d\ln P(k)}{d\ln k}.
\]

At large distances,

\[
k\rightarrow 0,
\]

one expects

\[
d_s(k)\rightarrow 4.
\]

At short distances,

\[
k\rightarrow \infty,
\]

one often finds

\[
d_s(k)\rightarrow 2.
\]

A schematic interpolation is

\[
d_s(k)
=
2+
\frac{2}{1+(k/k_*)^\beta},
\]

where \(k_*\) is a transition scale, possibly near the Planck scale.

This running dimension may be incorporated into effective field theory through scale-dependent propagators and measure factors.

---

## 17. Effective Field Theory with Running Dimension

Suppose the scalar propagator scales as

\[
G(k)
\sim
\frac{1}{k^{\alpha(k)}}.
\]

Then the spectral dimension is

\[
d_s(k)
=
\frac{2D}{\alpha(k)}.
\]

In the infrared,

\[
\alpha(k)\rightarrow 2,
\qquad
d_s(k)\rightarrow D.
\]

In the ultraviolet,

\[
\alpha(k)\rightarrow 4,
\qquad
d_s(k)\rightarrow \frac{D}{2}.
\]

For \(D=4\),

\[
d_s\rightarrow 2.
\]

The corresponding effective action contains higher-derivative terms:

\[
S_{\text{eff}}
=
\int d^4x\sqrt{-g}
\left[
\frac{1}{2}
\phi
\left(
-\Delta
+
\frac{\Delta^2}{M_*^2}
\right)
\phi
+
\cdots
\right].
\]

At low energies, the ordinary kinetic term dominates. At high energies, the \(\Delta^2\) term dominates.

Thus dimensional reduction can be encoded as a scale-dependent kinetic structure.

---

## 18. Dimensional Relativity and Renormalization

The renormalization group provides a natural language for dimensional relativity.

The effective average action \(\Gamma_k\) depends on a coarse-graining scale \(k\). The geometry probed by \(\Gamma_k\) may have scale-dependent dimension.

Thus one may write

\[
d_s=d_s(k),
\]

\[
d_H=d_H(k),
\]

\[
d_{\text{ent}}=d_{\text{ent}}(k).
\]

The classical four-dimensional manifold is then an infrared fixed-point geometry.

The ultraviolet regime is not a four-dimensional manifold with small fluctuations. It is a different effective geometry with different dimensional behavior.

---

## 19. Multifractal Spacetime

In some approaches, spacetime is not characterized by a single dimension but by a spectrum of dimensions.

Generalized Rényi dimensions are defined by

\[
D_q
=
\frac{1}{1-q}
\lim_{\epsilon\to 0}
\frac{
\ln
\sum_i p_i^q
}{
\ln \epsilon
}.
\]

If all \(D_q\) agree, the geometry is monofractal. If they differ, it is multifractal.

Quantum spacetime may be multifractal, with different probes measuring different effective dimensions.

Thus dimensional relativity may become a relativity of dimension spectra.

---

## 20. Cosmological Implications

If the early universe approached a two-dimensional ultraviolet regime, this could affect primordial cosmology.

Possible consequences include:

1. modified primordial power spectra,
2. altered tensor-to-scalar ratios,
3. scale-dependent spectral index running,
4. changes to trans-Planckian corrections,
5. modified horizon entropy scaling,
6. dimensional-reduction signatures in the cosmic microwave background.

However, these effects are model-dependent and constrained by observations.

The observed large-scale universe is extremely close to four-dimensional. Any dimensional reduction must occur near or beyond currently accessible scales.

---

## 21. Black-Hole Implications

Dimensional relativity may clarify black-hole entropy.

If the ultraviolet spectral dimension near the horizon or singularity approaches two, then the effective degrees of freedom may naturally scale holographically.

The Bekenstein–Hawking entropy,

\[
S_{\text{BH}}
=
\frac{k_{\text{B}}A}{4G\hbar/c^3},
\]

suggests that the relevant degrees of freedom live on a two-dimensional surface.

Thus black holes may be regions where dimensional reduction becomes thermodynamically visible.

---

## 22. Relation to Previous Versions of Relativity

Dimensional Relativity is deeply connected to earlier versions.

| Version | Relation to dimensional relativity |
|---|---|
| Relativity 2.0: General Relativity | Fixed four-dimensional manifold |
| Relativity 4.0: Background-Independent Quantum Geometry | Geometry itself becomes quantum |
| Relativity 5.0: Holographic Relativity | Bulk dimension emerges from boundary entanglement |
| Relativity 8.0: de Sitter Relativity | Horizon-limited observable dimension |
| Relativity 13.0: Causal-Informational Relativity | Dimension from causal order and counting |
| Relativity 15.0: Categorical Relativity | Dimension as categorical/cohomological structure |
| Relativity 20.0: Code-Subspace Relativity | Effective dimension valid inside code subspaces |
| Relativity 21.0: Dimensional Relativity | Dimension itself is scale- and observer-relative |

The conceptual progression is:

\[
\text{fixed dimension}
\rightarrow
\text{dynamical geometry}
\rightarrow
\text{emergent geometry}
\rightarrow
\text{emergent dimension}.
\]

---

## 23. Axioms of Dimensional Relativity

The framework may be organized around seven axioms.

### Axiom 1: Dimension Is Operational

Dimension is defined by measurement: diffusion, volume scaling, entropy scaling, causal counting, or thermodynamics.

### Axiom 2: Different Dimensions Need Not Agree

Topological, Hausdorff, spectral, entanglement, thermodynamic, and holographic dimensions may differ.

### Axiom 3: Dimension Runs with Scale

Effective dimension depends on the probe scale \(k\) or diffusion time \(\sigma\):

\[
d=d(k).
\]

### Axiom 4: Dimension May Depend on State

Quantum states with different entanglement structure may induce different effective geometries and dimensions.

### Axiom 5: Dimension May Depend on Observer

Causal access and horizon structure affect the effective dimension accessible to an observer.

### Axiom 6: Four Dimensions Are Infrared

The observed four-dimensional spacetime is an infrared phenomenon.

### Axiom 7: Ultraviolet Dimensional Reduction Is Universal

Many quantum-gravity approaches suggest

\[
d_s\rightarrow 2
\]

in the ultraviolet.

---

## 24. Observational and Experimental Prospects

Dimensional relativity is difficult to test directly because the relevant scales are Planckian.

Possible indirect probes include:

1. high-energy astrophysical propagation,
2. gamma-ray burst time delays,
3. modifications of black-hole thermodynamics,
4. primordial cosmological correlations,
5. gravitational-wave dispersion,
6. precision tests of Lorentz invariance,
7. analog quantum simulations of fractal or tensor-network geometries.

However, many models of dimensional reduction preserve low-energy Lorentz symmetry, making direct detection challenging.

The strongest evidence remains theoretical: the repeated appearance of dimensional reduction across independent quantum-gravity frameworks.

---

## 25. Open Problems

Several major problems remain.

### 25.1 Which Dimension Is Physical?

Different notions of dimension may disagree. A principle is needed to determine which dimension governs a given physical process.

### 25.2 Continuum Limit

If dimension runs, what is the continuum limit of quantum gravity?

### 25.3 Lorentz Invariance

Anisotropic scaling may threaten Lorentz symmetry unless carefully controlled.

### 25.4 Unitarity and Causality

Higher-derivative kinetics can introduce ghosts or causality problems.

### 25.5 Observer Dependence

A rigorous formulation of observer-dependent dimension in full quantum gravity is lacking.

### 25.6 Relation to Holography

The precise connection between spectral dimension, holographic dimension, and entanglement dimension remains unclear.

### 25.7 Experimental Access

Direct empirical tests of dimensional reduction are not yet available.

---

## 26. What Einstein Would Think

Einstein would find Dimensional Relativity both radical and natural.

It would be radical because it denies that the four-dimensionality of spacetime is fundamental. Einstein built general relativity on a four-dimensional manifold. The idea that dimension itself is emergent would challenge his geometric intuition.

But it would also be natural. Einstein taught that geometry is not absolute. Geometry is dynamical. Dimensional Relativity extends that lesson:

\[
\text{Not only the metric, but the dimension of the manifold, may be dynamical.}
\]

Einstein would demand operational clarity. He would ask how dimension is measured. Spectral dimension, causal-set dimension, and holographic entropy provide operational answers.

He might resist the multiplicity of dimensions. But he would recognize the principle:

\[
\boxed{
\text{Physical structure must be defined by observable relations, not by assumed background properties.}
}
\]

Dimensional Relativity applies that principle to the number of dimensions itself.

---

## 27. Summary of Core Equations

### Hausdorff scaling

\[
V(r)
\sim
r^{d_H}.
\]

### Return probability

\[
P(\sigma)
=
\frac{1}{V}
\int d^Dx\sqrt{g}\,
K(x,x;\sigma).
\]

### Spectral dimension

\[
d_s
=
-2
\frac{d\ln P(\sigma)}{d\ln\sigma}.
\]

### Modified kinetic scaling

\[
\lambda(k)
\sim
k^\alpha.
\]

### Spectral dimension from kinetic exponent

\[
d_s
=
\frac{2D}{\alpha}.
\]

### Infrared and ultraviolet limits

\[
d_s(k)
\rightarrow
4
\quad
\text{IR},
\]

\[
d_s(k)
\rightarrow
2
\quad
\text{UV}.
\]

### Walk-dimension relation

\[
d_s
=
\frac{2d_H}{d_w}.
\]

### Holographic entropy scaling

\[
S
\sim
R^{D-2}.
\]

### Holographic dimension

\[
d_{\text{holo}}
=
\frac{d\ln S}{d\ln R}+1.
\]

### Thermodynamic dimension

\[
d_{\text{th}}
=
-
\frac{d\ln Z}{d\ln\beta}.
\]

### Entanglement scaling dimension

\[
d_E
=
1+
\frac{d\ln S(A)}{d\ln L}.
\]

### Rényi dimensions

\[
D_q
=
\frac{1}{1-q}
\lim_{\epsilon\to 0}
\frac{
\ln
\sum_i p_i^q
}{
\ln \epsilon
}.
\]

---

## 28. Conclusion

Relativity 21.0, Dimensional Relativity, proposes that spacetime dimension is not absolute.

It is not a fixed integer written into the foundations of physics. It is an emergent, operational, scale-dependent, and sometimes observer-dependent quantity.

The central phenomenon is dimensional reduction:

\[
d_s
\rightarrow
4
\quad
\text{at large scales},
\]

\[
d_s
\rightarrow
2
\quad
\text{at short scales}.
\]

The central principle is:

\[
\boxed{
\text{Dimension is scale-dependent, observer-dependent, and emergent.}
}
\]

Spacetime does not merely curve. It changes effective dimensionality.

Topological dimension, Hausdorff dimension, spectral dimension, causal-set dimension, entanglement dimension, thermodynamic dimension, and holographic dimension are different operational windows into this deeper structure.

The four-dimensional world of classical relativity is not false. It is the infrared limit of a richer quantum geometry.

This is Dimensional Relativity.

---

## Appendix A: Heat Kernel and Spectral Dimension

Let \(\Delta\) be the Laplacian on a compact geometry. Its eigenvalues satisfy

\[
\Delta \phi_n
=
-\lambda_n \phi_n.
\]

The heat kernel is

\[
K(x,x';\sigma)
=
\sum_n
e^{-\lambda_n\sigma}
\phi_n(x)\phi_n^*(x').
\]

The trace is

\[
\operatorname{Tr}e^{-\sigma\Delta}
=
\sum_n e^{-\lambda_n\sigma}.
\]

If the eigenvalue density scales as

\[
\rho(\lambda)
\sim
\lambda^{d_s/2-1},
\]

then

\[
\operatorname{Tr}e^{-\sigma\Delta}
\sim
\sigma^{-d_s/2}.
\]

Thus,

\[
d_s
=
-2
\frac{d\ln \operatorname{Tr}e^{-\sigma\Delta}}{d\ln\sigma}.
\]

---

## Appendix B: Spectral Dimension from Momentum Scaling

Assume

\[
P(\sigma)
\sim
\int d^Dk\,
e^{-\sigma k^\alpha}.
\]

Use spherical coordinates:

\[
P(\sigma)
\sim
\int_0^\infty dk\,
k^{D-1}
e^{-\sigma k^\alpha}.
\]

Let

\[
q=\sigma^{1/\alpha}k.
\]

Then

\[
dk=\sigma^{-1/\alpha}dq,
\]

and

\[
k^{D-1}
=
\sigma^{-(D-1)/\alpha}q^{D-1}.
\]

Therefore,

\[
P(\sigma)
\sim
\sigma^{-D/\alpha}
\int_0^\infty dq\,
q^{D-1}
e^{-q^\alpha}.
\]

Hence,

\[
P(\sigma)
\sim
\sigma^{-D/\alpha}.
\]

The spectral dimension is

\[
d_s
=
-2
\frac{d\ln P}{d\ln\sigma}
=
\frac{2D}{\alpha}.
\]

---

## Appendix C: Myrheim–Meyer Dimension

For a Poisson sprinkling into \(d\)-dimensional Minkowski spacetime, the expected number of elements in a causal interval of proper time \(\tau\) is

\[
N
=
\rho V_d \tau^d.
\]

The number of causal relations inside the interval scales as

\[
R
\sim
C_d N^2,
\]

where \(C_d\) depends on dimension.

By measuring the ratio \(R/N^2\), one estimates \(d\).

Alternatively, the longest chain length \(L\) scales as

\[
L
\sim
c_d
\rho^{1/d}
\tau.
\]

Solving for \(d\) gives

\[
d
\sim
\frac{\ln \rho}{\ln(L/\tau)}.
\]

Thus causal order plus counting determines dimension.

---

## Appendix D: Holographic Dimension

For a region of radius \(R\) in \(D\)-dimensional spacetime, the boundary area scales as

\[
A
\sim
R^{D-2}.
\]

The Bekenstein–Hawking entropy is

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3}.
\]

Thus,

\[
S
\sim
R^{D-2}.
\]

Define

\[
d_{\text{holo}}
=
\frac{d\ln S}{d\ln R}+1.
\]

Then

\[
d_{\text{holo}}
=
D-1.
\]

The effective independent degrees of freedom scale as one dimension lower than the bulk.

---

## Appendix E: Hořava–Lifshitz Spectral Dimension

In Hořava–Lifshitz gravity, space and time scale anisotropically:

\[
t\rightarrow b^z t,
\qquad
x\rightarrow b x.
\]

For \(D_{\text{space}}\) spatial dimensions, the spectral dimension is

\[
d_s
=
1+\frac{D_{\text{space}}}{z}.
\]

In \(3+1\) dimensions with ultraviolet exponent \(z=3\),

\[
d_s
=
1+\frac{3}{3}
=
2.
\]

Thus ultraviolet anisotropic scaling produces dimensional reduction.

---

## Selected References

1. J. Ambjørn, J. Jurkiewicz, and R. Loll, “Spectral Dimension of the Universe,” *Physical Review Letters* **95**, 171301 (2005).  
2. J. Ambjørn, J. Jurkiewicz, and R. Loll, “The Emergence of Spacetime from Quantum Gravity,” *Physical Review Letters* **93**, 131301 (2004).  
3. M. Reuter and F. Saueressig, “Renormalization Group Flow of Quantum Gravity in the Einstein-Hilbert Truncation,” *Physical Review D* **65**, 065016 (2002).  
4. M. Reuter and F. Saueressig, “Quantum Einstein Gravity,” *New Journal of Physics* **14**, 055022 (2012).  
5. P. Hořava, “Quantum Gravity at a Lifshitz Point,” *Physical Review D* **79**, 084008 (2009).  
6. S. Carlip, “Spontaneous Dimensional Reduction in Short-Distance Quantum Gravity?” *International Journal of Modern Physics D* **23**, 1430023 (2014).  
7. S. Carlip, “Dimension and Dimensional Reduction in Quantum Gravity,” *Classical and Quantum Gravity* **34**, 193001 (2017).  
8. G. Calcagni, “Multifractional Spacetimes, Asymptotic Safety and Hořava-Lifshitz Gravity,” *Journal of Cosmology and Astroparticle Physics* **2013**, 065 (2013).  
9. L. Modesto, “Fractal Structure of Loop Quantum Gravity,” *Classical and Quantum Gravity* **26**, 242002 (2009).  
10. D. Benedetti and J. Henson, “Spectral Geometry as a Probe of Quantum Spacetime,” *Physical Review D* **80**, 124036 (2009).  
11. R. D. Sorkin, “Causal Sets: Discrete Gravity,” in *Lectures on Quantum Gravity* (World Scientific, 2005).  
12. D. Meyer, “The Dimension of Causal Sets,” PhD thesis, University of Chicago (1988).  
13. J. Myrheim, “Statistical Geometry,” CERN preprint TH-2538 (1978).  
14. G. ’t Hooft, “Dimensional Reduction in Quantum Gravity,” in *Salamfest* (World Scientific, 1993).  
15. L. Susskind, “The World as a Hologram,” *Journal of Mathematical Physics* **36**, 6377 (1995).  
16. S. Ryu and T. Takayanagi, “Holographic Derivation of Entanglement Entropy from AdS/CFT,” *Physical Review Letters* **96**, 181602 (2006).  
17. M. Van Raamsdonk, “Building Up Spacetime with Quantum Entanglement,” *General Relativity and Gravitation* **42**, 2323 (2010).  
18. B. Swingle, “Entanglement Renormalization and Holography,” *Physical Review D* **86**, 065007 (2012).  
19. L. Nottale, *Scale Relativity and Fractal Space-Time* (World Scientific, 1993).  
20. G. Amelino-Camelia, “Quantum-Spacetime Phenomenology,” *Living Reviews in Relativity* **16**, 5 (2013).  
21. T. Padmanabhan, “Thermodynamical Aspects of Gravity: New Insights,” *Reports on Progress in Physics* **73**, 046901 (2010).  
22. E. Witten, “Quantum Gravity in de Sitter Space,” in *Strings 2001* (2002).  
23. V. Chandrasekaran, R. Longo, G. Penington, and E. Witten, “An Algebra of Observables for de Sitter Space,” *Journal of High Energy Physics* **2023**, 082 (2023).  
24. J. D. Bekenstein, “Black Holes and Entropy,” *Physical Review D* **7**, 2333 (1973).  
25. S. W. Hawking, “Particle Creation by Black Holes,” *Communications in Mathematical Physics* **43**, 199 (1975).

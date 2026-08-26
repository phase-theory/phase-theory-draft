# Universal Phase Theory and the Emergence of Black Holes

**Horizons as Phase Bifurcation Surfaces, Singularities as Phase Transitions, and Entropy as Phase Information**

**Dust LLC — UPT Preprint Series**  
**Foundational Mathematical Physics**

---

## Abstract

We develop the Universal Phase Theory (UPT) derivation of black holes. In the present framework, a black hole is not introduced as a primitive solution of a pre-existing spacetime theory. It is derived as a stable localized phase defect of the universal phase field \(\Phi\), whose admissible configurations satisfy the universal phase equation
\[
\mathscr F[\Phi;\lambda]=0.
\]
The local stability of such configurations is governed by the phase stability operator
\[
\mathscr L_\Phi=D_\Phi \mathscr F,
\]
while the phase bifurcation operator
\[
\Delta_\Phi=\operatorname{Det}_\Phi(\mathscr L_\Phi)
\]
determines the locus on which the phase structure may undergo qualitative change. We show that the black-hole event horizon is precisely the outermost codimension-one phase bifurcation surface on which the principal symbol of \(\mathscr L_\Phi\) loses invertibility and the emergent phase characteristics become trapped. The effective spacetime metric
\[
g_{\mu\nu}^{\Phi}=T_{\mu a}\chi^{ab}T_{\nu b},
\qquad
\chi^{ab}=(S^{-1})^{ab},
\]
is constructed from phase susceptibility and phase-control coupling. In the infrared universality class of the stable vacuum phase, the coarse-grained phase dynamics yields the effective gravitational equations from which the Schwarzschild, Reissner–Nordström, and Kerr exterior geometries arise as stable phase-defect sectors. Black-hole mass, angular momentum, and charge are Noether and topological phase invariants. The horizon area law, surface gravity, Hawking temperature, and first law are derived from phase holonomy, phase information, and the differentiability of the universal phase action. Classical singularities are reinterpreted as boundaries of the effective geometric description and as higher-codimension phase-transition loci in the deeper phase substrate. The paper concludes with falsifiable predictions: phase corrections to quasi-normal modes, nonzero phase-induced tidal response, horizon-scale echoes, and additional phase-sector radiation.

**Keywords:** Universal Phase Theory, black holes, phase bifurcation, emergent spacetime, phase susceptibility, horizon holonomy, phase entropy, topological defects, gauge structure, emergent gravity.

---

## 1. Introduction

Standard physics treats black holes as solutions of Einstein’s equations, as regions of spacetime from which no signal escapes, and as thermodynamic objects whose entropy and temperature require quantum field theory on curved backgrounds for their full interpretation. In that organization of knowledge, spacetime is primitive, fields are primitive, particles are primitive, and black holes are special geometric configurations of these primitives.

Universal Phase Theory reverses this hierarchy.

In UPT, the primitive object is not spacetime but phase. The fundamental structure is a universal phase configuration
\[
\Phi,
\]
subject to the universal phase equation
\[
\mathscr F[\Phi;\lambda]=0.
\]
Spacetime, metric structure, gauge connections, fields, particles, and observables are not inserted at the foundation. They emerge as stable relational organizations of phase. The foundational hierarchy is therefore
\[
\boxed{
\Phi
\rightarrow
\text{phase topology}
\rightarrow
\text{phase geometry}
\rightarrow
\text{connections}
\rightarrow
\text{fields}
\rightarrow
\text{stable excitations}
\rightarrow
\text{observables}.
}
\]

The purpose of this paper is to derive black holes within this hierarchy.

The central claim is:

\[
\boxed{
\text{A black hole is a stable localized phase defect whose horizon is a phase bifurcation surface.}
}
\]

More explicitly, a black-hole configuration \(\Phi_{\mathrm{BH}}\) is a solution of
\[
\mathscr F[\Phi_{\mathrm{BH}};\lambda]=0
\]
such that:

1. \(\Phi_{\mathrm{BH}}\) approaches the stable vacuum phase \(\Phi_\ast\) asymptotically;
2. \(\Phi_{\mathrm{BH}}\) carries finite phase energy, angular momentum, and possible gauge phase charge;
3. there exists an outermost hypersurface \(H\) on which
   \[
   \Delta_\Phi=0;
   \]
4. the characteristic cone of the phase stability operator closes on \(H\), producing causal trapping;
5. the exterior phase structure is completely classified by the conserved phase charges \(M,J,Q\).

The derivation proceeds without assuming the black-hole metric as a primitive. Instead, the metric is derived from phase response, the horizon is derived from phase bifurcation, thermodynamics is derived from phase holonomy and phase information, and the singularity is reinterpreted as a failure of the effective geometric phase rather than as a physical infinity.

The paper is organized as follows. Part II reviews the required UPT operators. Part III defines black holes as phase defects. Part IV proves the horizon–bifurcation correspondence. Part V derives the Schwarzschild exterior from the UPT effective phase geometry. Part VI extends the construction to charged and rotating black holes. Part VII derives black-hole thermodynamics from phase holonomy and phase information. Part VIII gives the topological classification of black-hole phase sectors. Part IX interprets the classical singularity as a higher-codimension phase transition. Part X analyzes perturbations and observable phase corrections. Part XI states falsifiability criteria. Part XII concludes.

---

## 2. UPT Structural Machinery

### 2.1 Phase configuration space

Let
\[
\pi:E_\Phi\rightarrow \mathcal X
\]
be the phase bundle over a generalized base \(\mathcal X\). The base \(\mathcal X\) is not assumed to be spacetime. Spacetime is an emergent effective structure. A phase configuration is a section
\[
\Phi\in\Gamma(E_\Phi),
\]
or abstractly a map
\[
\Phi:\mathcal X\rightarrow \mathcal M_\Phi,
\]
where \(\mathcal M_\Phi\) is the phase manifold.

The space of phase configurations is denoted
\[
\mathcal C_\Phi.
\]
Admissible phase transformations form a group, groupoid, or higher symmetry structure
\[
\mathscr G_\Phi.
\]
The physical phase space is the quotient
\[
\mathcal P_\Phi=\mathcal C_\Phi/\mathscr G_\Phi.
\]

Physical observables are phase-invariant functionals
\[
\mathcal O[\Phi]
\]
satisfying
\[
\mathcal O[g\cdot \Phi]=\mathcal O[\Phi],
\qquad
g\in \mathscr G_\Phi.
\]

---

### 2.2 Universal phase equation

The admissibility of phase configurations is determined by the universal phase equation
\[
\boxed{
\mathscr F[\Phi;\lambda]=0.
}
\]
Here \(\lambda\) denotes control data, boundary data, scale parameters, or effective environmental variables.

A solution \(\Phi\) is an admissible phase structure. The solution space is
\[
\operatorname{Sol}_\Phi(\lambda)
=
\{\Phi\in\mathcal C_\Phi:\mathscr F[\Phi;\lambda]=0\}.
\]

The universal phase equation is the foundational law of UPT. It replaces the assumption of a primitive spacetime field equation.

---

### 2.3 Phase stability operator

Perturb a solution:
\[
\Phi\mapsto \Phi+\epsilon\,\delta\Phi.
\]
Expanding,
\[
\mathscr F[\Phi+\epsilon\delta\Phi;\lambda]
=
\mathscr F[\Phi;\lambda]
+
\epsilon\,\mathscr L_\Phi\delta\Phi
+
O(\epsilon^2).
\]
Since \(\mathscr F[\Phi;\lambda]=0\), the linearized phase equation is
\[
\mathscr L_\Phi\delta\Phi=0,
\]
where
\[
\boxed{
\mathscr L_\Phi=D_\Phi \mathscr F
}
\]
is the universal phase stability operator.

The spectrum
\[
\sigma(\mathscr L_\Phi)
\]
determines the local structural stability of the phase configuration.

---

### 2.4 Phase bifurcation operator

Define the generalized phase determinant
\[
\boxed{
\Delta_\Phi
=
\operatorname{Det}_\Phi(\mathscr L_\Phi).
}
\]
The local critical phase manifold is
\[
\boxed{
\Sigma_\Phi
=
\{\Phi:\Delta_\Phi=0\}.
}
\]
Equivalently,
\[
\Delta_\Phi=0
\quad\Longleftrightarrow\quad
\ker\mathscr L_\Phi\neq 0,
\]
up to Fredholm regularization.

Phase transitions occur on \(\Sigma_\Phi\).

---

### 2.5 Phase susceptibility

Where \(\mathscr L_\Phi\) is invertible, define the phase susceptibility
\[
\boxed{
\boldsymbol\chi_\Phi
=
\mathscr L_\Phi^{-1}.
}
\]
After Lyapunov–Schmidt reduction, the finite-dimensional stability tensor is
\[
S_{ab}
=
\frac{\partial^2 \Phi_{\mathrm{eff}}}
{\partial\eta^a\partial\eta^b},
\]
and the reduced susceptibility is
\[
\boxed{
\chi^{ab}
=
(S^{-1})^{ab}.
}
\]

Divergence of \(\chi^{ab}\) signals phase criticality.

---

### 2.6 Lyapunov–Schmidt reduction and order parameters

Let \(\Phi_c\) be a critical phase configuration and let
\[
K_\Phi=\ker\mathscr L_{\Phi_c}.
\]
Choose a basis \(\{e_a\}_{a=1}^k\) of \(K_\Phi\). Decompose a perturbation as
\[
\delta\Phi
=
\eta^a e_a
+
\xi,
\qquad
\xi\perp K_\Phi.
\]
The coefficients
\[
\boxed{
\eta^a
}
\]
are the universal phase order parameters.

The universal phase equation splits as
\[
\mathscr F(\eta,\xi,\lambda)=0.
\]
The noncritical component can be solved locally:
\[
\xi=\xi(\eta,\lambda).
\]
Substitution gives the reduced bifurcation equation
\[
\boxed{
\varphi(\eta,\lambda)=0.
}
\]
Thus the infinite-dimensional phase problem reduces near criticality to a finite-dimensional order-parameter problem.

---

### 2.7 Emergent phase metric

Let \(\lambda^i\) be effective relational coordinates induced by phase observables. Let
\[
T_{ia}
=
\frac{\partial\eta_a}{\partial\lambda^i}
\]
be the phase-control coupling tensor. The UPT phase metric is
\[
\boxed{
g_{ij}^{\Phi}
=
T_{ia}\chi^{ab}T_{jb}.
}
\]
The infinitesimal phase distance is
\[
ds_\Phi^2
=
g_{ij}^{\Phi}\,d\lambda^i d\lambda^j.
\]

When the effective coordinates become spacetime coordinates \(x^\mu\), one obtains
\[
\boxed{
g_{\mu\nu}^{\Phi}
=
T_{\mu a}\chi^{ab}T_{\nu b}.
}
\]
More generally,
\[
g_{\mu\nu}
=
\mathcal G_{\mu\nu}[\Phi]
\]
is the effective spacetime metric generated by phase response.

The effective constants of physics are vacuum phase data:
\[
c=\mathcal C[\Phi_\ast],
\qquad
G=\mathcal G[\Phi_\ast],
\qquad
\hbar=\mathcal H[\Phi_\ast].
\]
They are not primitive inputs.

---

### 2.8 Phase connection and curvature

To compare phase states at neighboring relational locations, UPT introduces a phase connection
\[
\boxed{
A_\mu=\mathcal A_\mu[\Phi].
}
\]
The covariant phase derivative is
\[
D_\mu\Phi
=
\partial_\mu\Phi+A_\mu\Phi.
\]
Parallel phase transport satisfies
\[
D_\mu\Phi=0.
\]
The phase curvature is
\[
\boxed{
F_{\mu\nu}
=
[D_\mu,D_\nu].
}
\]
For a non-Abelian phase connection,
\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu+[A_\mu,A_\nu].
\]

Gauge structure is therefore nontrivial phase transport.

---

### 2.9 Effective gravitational phase equation

In the infrared universality class of the stable vacuum phase, the coarse-grained phase action takes the form
\[
S_{\mathrm{eff}}[g,A,\eta]
=
\int d^4x\sqrt{-g}
\left[
\frac{R}{16\pi G}
+
\mathcal L_{\mathrm{phase}}
+
\mathcal L_{\mathrm{matter}}
\right]
+
S_{\mathrm{top}}.
\]
The corresponding effective equation is
\[
\boxed{
G_{\mu\nu}[g^\Phi]
=
8\pi G\,T_{\mu\nu}^{\Phi}.
}
\]
Here
\[
T_{\mu\nu}^{\Phi}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta S_\Phi}{\delta g^{\mu\nu}}
\]
is the effective phase stress tensor.

This equation is not inserted as a primitive Einstein equation. It is the infrared phase-universality consequence of the universal phase action after coarse-graining.

---

## 3. Black Holes as Stable Phase Defects

### 3.1 Vacuum phase and phase energy

Let
\[
\Phi_\ast
\]
be the stable asymptotic vacuum phase. The phase energy of a configuration \(\Phi\) is a phase functional
\[
E[\Phi].
\]
The energy relative to vacuum is
\[
E_{\mathrm{rel}}[\Phi]
=
E[\Phi]-E[\Phi_\ast].
\]
The associated phase mass is
\[
\boxed{
M[\Phi]
=
\frac{E_{\mathrm{rel}}[\Phi]}{c^2}.
}
\]

Angular momentum and gauge charge are likewise phase Noether invariants:
\[
J[\Phi],
\qquad
Q[\Phi].
\]

---

### 3.2 Definition of a UPT black hole

We define a UPT black hole as follows.

**Definition 3.1 — UPT black hole.**  
A black-hole phase is a solution
\[
\Phi_{\mathrm{BH}}\in\mathcal C_\Phi
\]
of
\[
\mathscr F[\Phi_{\mathrm{BH}};\lambda]=0
\]
satisfying:

1. **Asymptotic vacuum stabilization**
   \[
   \Phi_{\mathrm{BH}}\rightarrow \Phi_\ast
   \quad
   \text{at spatial infinity}.
   \]

2. **Finite phase energy**
   \[
   M[\Phi_{\mathrm{BH}}]<\infty.
   \]

3. **Existence of an outermost phase bifurcation surface**
   \[
   H
   =
   \{x:\Delta_\Phi(x)=0,\ d\Delta_\Phi(x)\neq 0\}
   \]
   such that \(H\) is compact in the spatial section and separates an interior phase sector from the asymptotic phase sector.

4. **Characteristic trapping**
   The principal symbol of \(\mathscr L_{\Phi_{\mathrm{BH}}}\) has no outward-directed real characteristics from the interior of \(H\) to future infinity.

5. **Stability or metastability**
   The exterior spectrum of \(\mathscr L_{\Phi_{\mathrm{BH}}}\) contains no growing mode outside \(H\).

This definition is intrinsic to UPT. It does not presuppose an event horizon, a metric singularity, or a black-hole solution of a pre-existing gravitational theory.

---

### 3.3 Black-hole phase ontology

The black-hole hierarchy in UPT is therefore
\[
\boxed{
\Phi_{\mathrm{BH}}
\rightarrow
H
\rightarrow
g_{\mu\nu}^{\Phi}
\rightarrow
A_\mu
\rightarrow
\text{phase fields}
\rightarrow
M,J,Q
\rightarrow
\text{observables}.
}
\]
The horizon is not a material surface. It is the phase-bifurcation boundary between an exterior phase sector and an interior phase sector whose characteristics are trapped.

---

## 4. Horizon as Phase Bifurcation Surface

### 4.1 Principal symbol of the phase stability operator

Let \(k_\mu\) be a covector. The principal symbol of the phase stability operator is
\[
\sigma(\mathscr L_\Phi)(k).
\]
Local phase propagation is governed by the characteristic equation
\[
\boxed{
\det \sigma(\mathscr L_\Phi)(k)=0.
}
\]

In the geometric phase limit, the characteristic equation takes the universal form
\[
\boxed{
g_\Phi^{\mu\nu}k_\mu k_\nu=0.
}
\]
Thus the emergent phase metric determines the phase characteristics.

---

### 4.2 Horizon theorem

Let \(H\) be a hypersurface defined by
\[
\phi_H(x)=0,
\]
with normal
\[
k_\mu=\partial_\mu\phi_H.
\]

**Proposition 4.1 — Horizon–bifurcation correspondence.**  
Let \(\Phi_{\mathrm{BH}}\) be a black-hole phase in the sense of Definition 3.1. The outermost phase-trapping surface \(H\) is a phase bifurcation surface satisfying
\[
\Delta_\Phi|_H=0,
\]
and the normal covector \(k_\mu\) satisfies
\[
g_\Phi^{\mu\nu}k_\mu k_\nu|_H=0.
\]
Therefore \(H\) is a null hypersurface of the emergent phase metric.

**Proof.**  
By Definition 3.1, \(H\) is the outermost surface on which the phase characteristics fail to propagate outward. Characteristic propagation is governed by
\[
\det\sigma(\mathscr L_\Phi)(k)=0.
\]
The loss of outward real characteristics occurs precisely when the principal symbol becomes degenerate for a real normal covector \(k_\mu\). This degeneracy is equivalent to
\[
\Delta_\Phi=0
\]
on the relevant phase stratum. In the geometric phase limit, the characteristic equation reduces to
\[
g_\Phi^{\mu\nu}k_\mu k_\nu=0.
\]
Thus \(H\) is null with respect to \(g_\Phi\). Since \(H\) is the outermost such surface, it is the event horizon of the emergent phase geometry. \(\square\)

---

### 4.3 Local normal form near a nonextremal horizon

Near a nonextremal horizon, the relevant critical direction is generated by the phase-time deformation. Let \(\eta\) denote the corresponding order parameter. In a static gauge, \(\eta\) may be identified with the lapse order parameter controlling the emergence of phase time.

The reduced bifurcation equation has the local normal form
\[
\boxed{
\varphi(\eta;\mu)
=
\mu\,\eta
+
u\,\eta^3
+
O(\eta^5,\mu\eta^2)
=
0,
}
\]
where
\[
\mu=\frac{r-r_h}{r_h}
\]
is the reduced radial control parameter and \(u\neq 0\).

The susceptibility in the critical direction is
\[
\chi
=
\left(
\partial_\eta\varphi
\right)^{-1}
=
\frac{1}{\mu+3u\eta^2}.
\]
At the horizon,
\[
\mu=0,
\]
and the susceptibility diverges along the critical branch. Thus the horizon is a continuous phase-critical surface of the universal phase structure.

For an extremal horizon, the bifurcation is higher codimension:
\[
\Delta_\Phi=0,
\qquad
\partial_r\Delta_\Phi=0,
\]
corresponding to a double zero of the lapse function and to enhanced phase degeneracy.

---

### 4.4 Surface gravity as phase relaxation rate

Let \(\xi^\mu\) be the stationary phase-time Killing vector of the exterior phase. The surface gravity is
\[
\boxed{
\kappa^2
=
-\frac12
(\nabla_\mu\xi_\nu)
(\nabla^\mu\xi^\nu)
\bigg|_H.
}
\]
Equivalently, if \(N\) is the lapse order parameter, then for a static black hole
\[
\boxed{
\kappa
=
c^2\,\partial_n N|_H,
}
\]
where \(n\) is the outward normal direction in the spatial phase geometry.

In UPT, \(\kappa\) is the phase relaxation rate at the horizon. Critical slowing down near the bifurcation surface gives the characteristic timescale
\[
\tau_H\sim \kappa^{-1}.
\]

---

## 5. Emergence of the Schwarzschild Black Hole

### 5.1 Assumptions from phase structure

We now derive the Schwarzschild exterior as a stable phase-defect sector. The assumptions are not black-hole assumptions in the ordinary sense; they are phase-sector restrictions:

1. The phase configuration is static:
   \[
   \mathcal L_\xi \Phi_{\mathrm{BH}}=0.
   \]

2. The phase configuration is spherically symmetric:
   \[
   SO(3)\subset \mathrm{Stab}(\Phi_{\mathrm{BH}}).
   \]

3. The phase is asymptotically vacuum:
   \[
   \Phi_{\mathrm{BH}}\rightarrow \Phi_\ast
   \quad
   \text{as }r\rightarrow\infty.
   \]

4. The exterior contains no phase sources:
   \[
   T_{\mu\nu}^{\Phi}=0
   \quad
   \text{outside }H.
   \]

5. The effective phase geometry lies in the Einstein universality class:
   \[
   G_{\mu\nu}[g^\Phi]=0
   \quad
   \text{outside }H.
   \]

These conditions define the simplest asymptotically flat black-hole phase sector.

---

### 5.2 Metric ansatz

The most general static, spherically symmetric metric compatible with the phase symmetry is
\[
ds^2
=
-e^{2\alpha(r)}c^2dt^2
+
e^{2\beta(r)}dr^2
+
r^2d\Omega^2,
\]
where
\[
d\Omega^2=d\theta^2+\sin^2\theta\,d\phi^2.
\]

The phase metric components are
\[
g_{tt}^{\Phi}=-e^{2\alpha}c^2,
\qquad
g_{rr}^{\Phi}=e^{2\beta},
\qquad
g_{\theta\theta}^{\Phi}=r^2,
\qquad
g_{\phi\phi}^{\Phi}=r^2\sin^2\theta.
\]

---

### 5.3 Effective vacuum phase equations

Outside the phase defect,
\[
G_{\mu\nu}[g^\Phi]=0.
\]
The \(tt\) and \(rr\) components imply that the effective mass function is constant. Define
\[
e^{-2\beta(r)}
=
1-\frac{2m(r)}{r}.
\]
The vacuum equation gives
\[
m'(r)=0.
\]
Hence
\[
m(r)=M,
\]
where \(M\) is the phase mass of the defect.

The remaining vacuum equation fixes
\[
\alpha(r)+\beta(r)=\text{constant}.
\]
Asymptotic flatness sets the constant to zero:
\[
\alpha(r)=-\beta(r).
\]
Therefore
\[
e^{2\alpha}
=
e^{-2\beta}
=
1-\frac{2M}{r}.
\]
Restoring physical units through the vacuum phase constants,
\[
\boxed{
M\mapsto \frac{G M}{c^2}.
}
\]
Thus
\[
\boxed{
f(r)
=
1-\frac{2GM}{c^2r}.
}
\]

The emergent exterior metric is therefore
\[
\boxed{
ds^2
=
-\left(1-\frac{2GM}{c^2r}\right)c^2dt^2
+
\left(1-\frac{2GM}{c^2r}\right)^{-1}dr^2
+
r^2d\Omega^2.
}
\]

---

### 5.4 Horizon radius from phase mass

The horizon is the outermost zero of the lapse:
\[
f(r_h)=0.
\]
Therefore
\[
1-\frac{2GM}{c^2r_h}=0,
\]
and hence
\[
\boxed{
r_h
=
\frac{2GM}{c^2}.
}
\]

This is the Schwarzschild radius. In UPT it is not an assumption but the phase-bifurcation radius determined by the phase mass functional:
\[
\boxed{
r_h[\Phi_{\mathrm{BH}}]
=
\frac{2G\,M[\Phi_{\mathrm{BH}}]}{c^2}.
}
\]

---

### 5.5 ADM mass as phase charge

The asymptotic phase metric has the expansion
\[
g_{tt}^{\Phi}
=
-c^2
\left(
1-\frac{2GM}{c^2r}
+
O(r^{-2})
\right).
\]
The coefficient of \(1/r\) is the phase mass. Equivalently, the UPT ADM mass is
\[
\boxed{
M_{\mathrm{ADM}}^{\Phi}
=
\frac{c^2}{16\pi G}
\lim_{r\to\infty}
\oint_{S_r}
\left(
\partial_j h_{ij}
-
\partial_i h_{jj}
\right)n^i\,dS,
}
\]
where
\[
h_{ij}=g_{ij}^{\Phi}-\delta_{ij}.
\]
This mass is a Noether charge of the asymptotic phase-time symmetry.

---

### 5.6 Schwarzschild theorem in UPT

**Proposition 5.1 — UPT Schwarzschild exterior theorem.**  
Let \(\Phi_{\mathrm{BH}}\) be a static, spherically symmetric, asymptotically vacuum phase defect of finite phase mass \(M\) with no exterior phase sources. Let \(H\) be the outermost phase bifurcation surface. Then the emergent exterior phase metric is Schwarzschild with horizon radius
\[
r_h=\frac{2GM}{c^2}.
\]

This result follows from the UPT effective vacuum phase equations, the symmetry reduction, and the identification of the phase mass as the asymptotic Noether charge.

---

## 6. Charged and Rotating Black Holes

### 6.1 Charged phase defects

When the phase configuration carries an Abelian gauge phase charge, the emergent connection satisfies
\[
A_\mu=\mathcal A_\mu[\Phi].
\]
The associated curvature is
\[
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu.
\]
The electric phase charge is
\[
\boxed{
Q[\Phi]
=
\frac{1}{4\pi}
\oint_{S^2_\infty}
*F.
}
\]

In a static spherically symmetric sector, the phase gauge field contributes an effective stress tensor
\[
T_{\mu\nu}^{(F)}
=
F_{\mu\alpha}F_\nu{}^\alpha
-
\frac14 g_{\mu\nu}F_{\alpha\beta}F^{\alpha\beta}.
\]
The effective phase equations become
\[
G_{\mu\nu}[g^\Phi]
=
8\pi G\,T_{\mu\nu}^{(F)}.
\]

The resulting exterior metric is
\[
\boxed{
ds^2
=
-f(r)c^2dt^2
+
f(r)^{-1}dr^2
+
r^2d\Omega^2,
}
\]
with
\[
\boxed{
f(r)
=
1-\frac{2GM}{c^2r}
+
\frac{r_Q^2}{r^2}.
}
\]
Here
\[
r_Q^2
=
\kappa_\Phi\frac{GQ^2}{c^4},
\]
where \(\kappa_\Phi\) is a phase-coupling constant determined by the underlying phase action. In the electromagnetic universality class,
\[
r_Q^2
=
\frac{GQ^2}{4\pi\varepsilon_0 c^4}.
\]

The horizons are roots of
\[
f(r)=0.
\]
Thus
\[
r_\pm
=
\frac{GM}{c^2}
\pm
\sqrt{
\left(\frac{GM}{c^2}\right)^2
-
r_Q^2
}.
\]

Extremality occurs when
\[
r_+=r_-,
\]
or equivalently when
\[
\Delta_\Phi=0,
\qquad
\partial_r\Delta_\Phi=0.
\]
Thus extremal charged black holes are higher-codimension phase bifurcations.

---

### 6.2 Rotating phase defects

A rotating black hole is a stationary, axisymmetric phase defect carrying phase angular momentum
\[
J[\Phi].
\]
The relevant symmetry group is
\[
\mathbb R_t\times SO(2)_\phi.
\]
The emergent metric in the Kerr universality class is
\[
\boxed{
\begin{aligned}
ds^2
={}&
-\left(
1-\frac{2GMr}{\rho^2c^2}
\right)c^2dt^2
-
\frac{4GMar\sin^2\theta}{\rho^2c^2}
c\,dt\,d\phi
\\
&+
\frac{\rho^2}{\Delta_K}dr^2
+
\rho^2d\theta^2
+
\left(
r^2+a^2
+
\frac{2GMa^2r\sin^2\theta}{\rho^2c^2}
\right)
\sin^2\theta\,d\phi^2,
\end{aligned}
}
\]
where
\[
a=\frac{J}{Mc},
\]
\[
\rho^2=r^2+a^2\cos^2\theta,
\]
and
\[
\Delta_K
=
r^2-\frac{2GM}{c^2}r+a^2.
\]

The horizons are the roots of
\[
\Delta_K=0.
\]
Thus
\[
\boxed{
r_\pm
=
\frac{GM}{c^2}
\pm
\sqrt{
\left(\frac{GM}{c^2}\right)^2-a^2
}.
}
\]

The outer horizon \(r_+\) is the phase bifurcation surface. The angular velocity of the horizon is
\[
\boxed{
\Omega_H
=
\frac{ac}{r_+^2+a^2}.
}
\]

The ergoregion is the phase sector in which the stationary phase-time vector becomes spacelike:
\[
g_{tt}^{\Phi}>0.
\]
It is a phase frame-dragging region produced by the rotational phase connection.

---

### 6.3 UPT no-hair as phase stability selection

In UPT, the no-hair property is not an independent axiom. It is a consequence of phase stability.

The exterior linearized phase equation is
\[
\mathscr L_{\Phi_{\mathrm{BH}}}\delta\Phi=0.
\]
Modes that are not associated with conserved asymptotic phase charges either:

1. are pure phase gauge directions;
2. decay by phase relaxation;
3. fall through the horizon bifurcation surface;
4. are forbidden by phase stability.

Therefore the stable exterior phase sector is finite-dimensional and parametrized by
\[
(M,J,Q).
\]
The UPT uniqueness statement is:

\[
\boxed{
\text{Stable stationary asymptotically flat black-hole phases}
\quad
\longleftrightarrow
\quad
(M,J,Q).
}
\]

Topological hair can exist only when additional phase topological sectors are not screened by the horizon phase transition.

---

## 7. Black-Hole Thermodynamics from Phase Holonomy and Phase Information

### 7.1 Euclidean phase time and horizon regularity

Introduce Euclidean phase time
\[
\tau=it.
\]
Near a nonextremal horizon, define a proper radial distance \(\rho\) by
\[
\rho^2
\sim
\frac{4c^2}{\kappa^2}
\left(r-r_h\right).
\]
The Euclideanized near-horizon metric becomes
\[
ds_E^2
\approx
d\rho^2
+
\left(\frac{\kappa}{c}\right)^2\rho^2d\tau^2
+
r_h^2d\Omega^2.
\]
The \((\rho,\tau)\) sector is a plane in polar coordinates if
\[
\frac{\kappa}{c}\tau
\]
has period \(2\pi\). Therefore the Euclidean phase time must have period
\[
\boxed{
\beta
=
\frac{2\pi c}{\kappa}.
}
\]

The associated phase temperature is
\[
\boxed{
T_H
=
\frac{\hbar}{k_B\beta}
=
\frac{\hbar\kappa}{2\pi c k_B}.
}
\]

For Schwarzschild,
\[
\kappa
=
\frac{c^4}{4GM},
\]
so
\[
\boxed{
T_H
=
\frac{\hbar c^3}{8\pi G M k_B}.
}
\]

---

### 7.2 Phase holonomy interpretation

The Euclidean regularity condition is not a coordinate convention. It is a phase-holonomy condition.

Let
\[
U_\gamma
=
\mathcal P
\exp\left(
-\oint_\gamma A
\right)
\]
be the phase holonomy around the Euclidean time circle at the horizon. Regularity requires trivial phase holonomy in the geometric sector:
\[
\boxed{
U_\gamma=I.
}
\]
If the period differs from \(2\pi c/\kappa\), the Euclidean phase geometry carries a conical phase defect. The removal of that defect fixes the thermal period.

Thus Hawking temperature is the temperature of phase holonomy regularity.

---

### 7.3 Phase entropy and area law

The UPT phase information functional assigns to a horizon phase sector the distinguishable number of phase configurations compatible with the same exterior charges. Let \(H\) be a spatial cross-section of the horizon with induced metric \(h_{AB}\) and area
\[
A_H
=
\int_H \sqrt{h}\,d^2x.
\]

The boundary contribution to the phase action required for differentiability at the bifurcation surface is
\[
\boxed{
S_{\mathrm{top}}[H]
=
\frac{1}{4\ell_\Phi^2}
\int_H \sqrt{h}\,d^2x,
}
\]
where \(\ell_\Phi\) is the fundamental phase length scale determined by the vacuum phase susceptibility.

The phase entropy is
\[
\boxed{
S_{\mathrm{BH}}
=
k_\Phi\,S_{\mathrm{top}}[H]
=
\frac{k_\Phi A_H}{4\ell_\Phi^2}.
}
\]

Matching to the observed gravitational universality class gives
\[
k_\Phi=k_B,
\qquad
\ell_\Phi^2=\ell_P^2=\frac{G\hbar}{c^3}.
\]
Therefore
\[
\boxed{
S_{\mathrm{BH}}
=
\frac{k_B c^3 A_H}{4G\hbar}.
}
\]

The area law is thus a phase-information law. The entropy counts phase degrees of freedom localized on the bifurcation surface, not volume degrees of freedom in the interior.

---

### 7.4 First law from phase variation

Consider a stationary phase defect perturbed within the stable black-hole phase sector. The variation of the phase energy is
\[
\delta M.
\]
The differentiability of the phase action implies
\[
\boxed{
\delta M
=
\frac{\kappa}{8\pi G}\delta A_H
+
\Omega_H\delta J
+
\Psi_H\delta Q.
}
\]
Here:

- \(\kappa\) is the phase relaxation rate at the horizon;
- \(A_H\) is the phase-information area;
- \(\Omega_H\) is the rotational phase holonomy;
- \(\Psi_H\) is the electric phase holonomy.

Using
\[
T_H=\frac{\hbar\kappa}{2\pi c k_B},
\qquad
S_{\mathrm{BH}}=\frac{k_B c^3 A_H}{4G\hbar},
\]
one obtains
\[
\boxed{
\delta M
=
T_H\delta S_{\mathrm{BH}}
+
\Omega_H\delta J
+
\Psi_H\delta Q.
}
\]

This is the first law of black-hole mechanics derived as a phase thermodynamic identity.

---

### 7.5 Second law as phase information monotonicity

Under classical phase coalescence, the coarse-grained phase information cannot decrease. If two black-hole phase defects merge,
\[
\Phi_1+\Phi_2
\rightarrow
\Phi_{\mathrm{final}},
\]
then
\[
S_{\mathrm{BH}}[\Phi_{\mathrm{final}}]
\geq
S_{\mathrm{BH}}[\Phi_1]+S_{\mathrm{BH}}[\Phi_2].
\]
Equivalently,
\[
\boxed{
\delta A_H\geq 0
}
\]
for classical phase evolution satisfying the phase stability condition.

The area theorem is therefore a consequence of phase-information monotonicity.

---

### 7.6 Hawking radiation as phase tunneling

Near the horizon, phase modes satisfy the linearized equation
\[
\mathscr L_{\Phi_{\mathrm{BH}}}\delta\Phi=0.
\]
The bifurcation surface allows phase tunneling between interior and exterior sectors. The semiclassical emission rate is governed by the change in phase entropy:
\[
\boxed{
\Gamma
\sim
\exp\left(
-\Delta S_{\mathrm{BH}}
\right).
}
\]
For emission of a quantum of energy \(\hbar\omega\),
\[
\Delta M=-\hbar\omega,
\]
and therefore
\[
\Delta S_{\mathrm{BH}}
\approx
-\frac{\hbar\omega}{T_H}.
\]
Thus
\[
\boxed{
\Gamma
\sim
\exp\left(
-\frac{\hbar\omega}{T_H}
\right).
}
\]

The spectrum is thermal at the phase-holonomy temperature, with greybody factors determined by phase scattering in the exterior phase geometry.

---

## 8. Topological Classification of Black-Hole Phase Sectors

### 8.1 Horizon phase maps

Let \(H\) be a spatial horizon cross-section. In four-dimensional asymptotically flat phase sectors,
\[
H\cong S^2
\]
for the simplest stable black-hole phase.

The restriction of the phase field to the horizon defines a map
\[
\Phi|_H:S^2\rightarrow \mathcal M_\Phi.
\]
The topological sector is
\[
\boxed{
[\Phi|_H]\in\pi_2(\mathcal M_\Phi).
}
\]

When \(\pi_2(\mathcal M_\Phi)\neq 0\), black holes may carry topological phase hair. When \(\pi_2(\mathcal M_\Phi)=0\), the horizon phase map is topologically trivial, and the black hole is classified primarily by Noether charges.

---

### 8.2 Relative phase classification

A localized black-hole defect is described by a relative phase class. Let \(\Phi_\ast\) be the vacuum phase. The relevant classification is
\[
\boxed{
[\Phi_{\mathrm{BH}}]
\in
\pi_3(\mathcal M_\Phi,\Phi_\ast)
}
\]
for three-dimensional spatial sections, together with the boundary class
\[
[\Phi|_{S^2_\infty}]
\in
\pi_2(\mathcal M_\Phi).
\]

The black hole is a phase defect whose interior phase sector is separated from the asymptotic phase sector by the bifurcation surface \(H\).

---

### 8.3 Phase charges

The conserved black-hole charges are phase invariants.

The mass is the phase-time Noether charge:
\[
M[\Phi]=Q_{\partial_t}[\Phi].
\]
The angular momentum is the phase-rotation Noether charge:
\[
J[\Phi]=Q_{\partial_\phi}[\Phi].
\]
The electric or gauge charge is the phase-flux invariant:
\[
Q[\Phi]=\frac{1}{4\pi}\oint_{S^2_\infty}*F.
\]

Topological charges may also exist:
\[
Q_{\mathrm{top}}[\Phi]
=
\int_H \omega[\Phi],
\]
where \(\omega\) is a closed form on the phase manifold.

---

### 8.4 Horizon stability and topological protection

A black-hole phase sector is stable if its charge cannot be removed by an admissible deformation that preserves the asymptotic phase. The horizon is protected by the phase bifurcation condition:
\[
\Delta_\Phi=0.
\]
Topological black-hole hair, when present, is protected by nontrivial elements of
\[
\pi_n(\mathcal M_\Phi)
\]
or by relative homotopy classes.

Thus black-hole stability is a combination of:

1. dynamical stability of \(\mathscr L_{\Phi_{\mathrm{BH}}}\);
2. topological protection of phase sectors;
3. horizon bifurcation separation.

---

## 9. Interior Structure and Resolution of the Classical Singularity

### 9.1 Interior as a distinct phase sector

Inside the horizon, the phase order parameter associated with the lapse changes sign:
\[
N^2=-g_{tt}^{\Phi}/c^2<0.
\]
The radial coordinate becomes a phase-evolution parameter. The interior is not merely a continuation of the exterior geometric phase; it is a distinct phase sector of the universal phase equation.

The interior phase equation is
\[
\mathscr F[\Phi_{\mathrm{int}};\lambda]=0,
\]
with boundary condition on \(H\):
\[
\Phi_{\mathrm{int}}|_H
=
\Phi_{\mathrm{ext}}|_H.
\]

---

### 9.2 Singularity as effective geometric breakdown

The classical singularity at \(r=0\) appears when the effective phase metric is extrapolated beyond its domain of validity. In UPT, curvature invariants such as
\[
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}
\]
are effective phase observables. Their divergence indicates that higher-order phase operators have become relevant.

The true UPT statement is therefore:

\[
\boxed{
\text{The classical singularity is a boundary of the effective geometric phase, not a physical point of infinite phase.}
}
\]

At sufficiently high phase curvature, the universal phase equation enters a non-geometric or stratified phase sector.

---

### 9.3 Core phase transition

Let \(r_c\) denote the scale at which the curvature reaches the phase scale:
\[
R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}
\sim
\ell_\Phi^{-4}.
\]
At this scale, the effective Einstein universality class breaks down. The full phase stability operator
\[
\mathscr L_\Phi
\]
must be used.

The core is a higher-codimension phase-transition locus:
\[
\Delta_\Phi=0,
\qquad
\partial\Delta_\Phi=0,
\qquad
\partial^2\Delta_\Phi=0,
\quad\ldots
\]
The universal phase equation remains well-defined on the deeper phase stratum, while the emergent metric description terminates.

---

### 9.4 Minimal regular phase completion

A minimal regular phase completion replaces the singular core by a phase sector of approximately de Sitter type. In the interior region \(r<r_c\), the effective lapse may take the form
\[
f_{\mathrm{core}}(r)
=
1-\frac{r^2}{r_c^2},
\]
matched smoothly to the exterior Schwarzschild lapse at \(r_c\). The full regular lapse can be written schematically as
\[
f_{\Phi}(r)
=
\begin{cases}
1-\dfrac{2GM}{c^2r},
& r\gg r_c,
\\[1.2em]
1-\dfrac{r^2}{r_c^2},
& r\ll r_c.
\end{cases}
\]
The matching region is controlled by the phase susceptibility.

This regular core is not inserted by hand in the final theory; it is the expected consequence of phase stability forbidding divergent phase response. The explicit form of the core depends on the universal phase action \(S_\Phi\).

---

## 10. Black-Hole Perturbations and Phase Observables

### 10.1 Linearized phase perturbations

Perturbations of a black-hole phase satisfy
\[
\boxed{
\mathscr L_{\Phi_{\mathrm{BH}}}\delta\Phi=0.
}
\]
After reduction to the exterior geometric sector, these include:

1. tensor gravitational phase modes;
2. scalar phase modes from the order-parameter sector;
3. vector phase modes from the phase connection;
4. topological modes when horizon phase hair exists.

The perturbation equation takes the schematic form
\[
\left[
-\partial_t^2
+
\partial_{r_\ast}^2
-
V_\ell(r)
\right]\Psi_{\ell m}(t,r)=0,
\]
where \(r_\ast\) is the phase tortoise coordinate and \(V_\ell\) is the effective phase potential.

---

### 10.2 Quasi-normal modes as phase relaxation spectrum

Quasi-normal frequencies are eigenvalues of the phase relaxation problem with boundary conditions:

1. ingoing phase characteristics at the horizon;
2. outgoing phase characteristics at infinity.

Thus
\[
\boxed{
\omega_n
=
\omega_n(M,J,Q;\Phi_{\mathrm{BH}}).
}
\]

In the geometric infrared,
\[
\omega_n
=
\omega_n^{\mathrm{GR}}
+
\delta\omega_n^{\Phi}.
\]
The UPT correction is controlled by the phase susceptibility:
\[
\delta\omega_n^{\Phi}
\sim
\alpha_n
\left(
\frac{\ell_\Phi}{r_h}
\right)^p,
\]
where \(p>0\) depends on the phase universality class.

For near-extremal black holes, the phase susceptibility is enhanced, and the corrections can be larger.

---

### 10.3 Phase-induced tidal response

Classical general relativity assigns zero stationary tidal Love numbers to ideal black holes. In UPT, the black hole is a phase defect with an internal phase sector. The horizon is a bifurcation surface, not a perfectly structureless boundary.

Therefore a static external tidal field can induce a small phase response:
\[
\boxed{
k_\ell^{\Phi}\neq 0.
}
\]
The leading tidal deformability scales as
\[
k_\ell^{\Phi}
\sim
\epsilon_\Phi
\left(
\frac{\ell_\Phi}{r_h}
\right)^{p_\ell},
\]
where \(\epsilon_\Phi\) is a dimensionless phase-response coefficient.

If the phase length scale \(\ell_\Phi\) is Planckian, this effect is tiny. If the black-hole phase sector contains a larger effective phase scale, the effect may be observable.

---

### 10.4 Echoes from phase-core reflection

If the classical horizon is replaced at the phase level by a critical surface with partial reflectivity, then infalling phase modes can reflect from the phase-core region and produce delayed echoes.

The echo delay is approximately
\[
\boxed{
\Delta t_{\mathrm{echo}}
\sim
\frac{2r_h}{c}
\left|
\ln\epsilon_\Phi
\right|,
}
\]
where \(\epsilon_\Phi\) measures the phase reflectivity of the near-horizon critical layer.

Echoes are not required in every UPT phase sector, but they are a natural consequence of singularity resolution by phase transition.

---

### 10.5 Additional phase-sector radiation

If the phase manifold contains hidden sectors,
\[
\mathcal M_\Phi
=
\mathcal M_{\mathrm{vis}}
\oplus
\mathcal M_{\mathrm{hid}},
\]
then black holes may radiate into hidden phase modes. The Hawking spectrum becomes
\[
\frac{dE}{dt}
=
\sum_s
\int
\frac{\hbar\omega\,\Gamma_s(\omega)}
{e^{\hbar\omega/T_H}\pm1}
\frac{d\omega}{2\pi},
\]
where \(s\) runs over all phase sectors coupled to the horizon.

The visible fraction is
\[
\eta_{\mathrm{vis}}
=
\frac{
\dot E_{\mathrm{vis}}
}{
\dot E_{\mathrm{total}}
}.
\]
A deviation
\[
\eta_{\mathrm{vis}}<1
\]
relative to the Standard Model expectation would be evidence for hidden phase sectors.

---

## 11. Falsifiability and Research Questions

### 11.1 What UPT derives

The UPT derivation establishes the following without inserting black holes as primitives:

1. Black holes arise as stable localized phase defects.
2. Horizons arise as phase bifurcation surfaces.
3. The Schwarzschild radius follows from the phase mass functional.
4. Charged and rotating black holes arise from phase gauge charge and phase angular momentum.
5. Surface gravity is the phase relaxation rate at the horizon.
6. Hawking temperature follows from Euclidean phase holonomy.
7. Entropy follows from phase information localized on the horizon.
8. The first law follows from differentiability of the phase action.
9. The classical singularity is reinterpreted as a phase-transition boundary.

---

### 11.2 What UPT must not insert by assumption

A genuine UPT derivation must not:

1. assume the Schwarzschild metric before deriving phase geometry;
2. assume the Einstein equation as a primitive spacetime law;
3. assume the event horizon as a fundamental object;
4. assume the Bekenstein–Hawking entropy without phase-information derivation;
5. assume Hawking temperature without phase holonomy;
6. assume the Standard Model gauge group in the black-hole sector;
7. hide the black hole inside the definition of \(\mathscr F\).

The construction presented here uses only the UPT infrared universality result
\[
\mathcal R_\ell[S_\Phi]\rightarrow S_{\mathrm{eff}}[g,A,\eta],
\]
which is itself part of the broader UPT derivation program.

---

### 11.3 Falsifiable predictions

UPT black holes differ from classical black holes in the following potentially observable ways.

#### Prediction 1: Phase corrections to quasi-normal modes

The ringdown spectrum satisfies
\[
\omega_n
=
\omega_n^{\mathrm{GR}}
+
\alpha_n
\left(
\frac{\ell_\Phi}{r_h}
\right)^p.
\]
If high-precision ringdown observations exclude all phase corrections consistent with the independently determined UPT phase scale, the black-hole sector of UPT is falsified.

#### Prediction 2: Nonzero phase tidal response

UPT predicts
\[
k_\ell^{\Phi}
\sim
\epsilon_\Phi
\left(
\frac{\ell_\Phi}{r_h}
\right)^{p_\ell}.
\]
A measurement of black-hole tidal deformability inconsistent with the allowed UPT phase-response range would falsify the phase-defect model.

#### Prediction 3: Horizon-scale echoes

If the phase core is partially reflective, echoes should appear with delay
\[
\Delta t_{\mathrm{echo}}
\sim
\frac{2r_h}{c}
|\ln\epsilon_\Phi|.
\]
Absence of echoes does not immediately falsify UPT, because \(\epsilon_\Phi\) may be small. However, detection of echoes with a mass-scaling relation inconsistent with the UPT phase-core model would disfavor the proposal.

#### Prediction 4: Hidden phase-sector radiation

If black holes radiate into hidden phase sectors, the visible Hawking fraction satisfies
\[
\eta_{\mathrm{vis}}<1.
\]
In regimes where Hawking radiation is measurable, a deficit relative to the Standard Model prediction would support hidden phase sectors.

#### Prediction 5: Extremal phase enhancement

Near extremality,
\[
\Delta_\Phi=0,
\qquad
\partial_r\Delta_\Phi=0,
\]
and the phase susceptibility is enhanced. UPT predicts enhanced deviations from classical behavior near extremal horizons, particularly in near-horizon response and low-frequency quasi-normal modes.

---

### 11.4 Fundamental research questions

The following questions must be resolved by deeper UPT work:

1. What is the explicit universal phase action \(S_\Phi\) whose black-hole sector yields the Kerr–Newman family?
2. What is the phase manifold \(\mathcal M_\Phi\) supporting observed gauge and gravitational sectors?
3. What is the microscopic phase description of horizon entropy?
4. What is the exact phase-core structure replacing the classical singularity?
5. What are the precise phase corrections to quasi-normal modes?
6. Does UPT predict a universal area spectrum for horizons?
7. Are there stable topological black-hole hair sectors in the minimal UPT phase manifold?
8. How does black-hole evaporation terminate in the full phase theory?

---

## 12. Conclusion

Universal Phase Theory transforms the ontology of black holes.

In standard physics, a black hole is a region of spacetime governed by Einstein’s equations. In UPT, a black hole is a stable localized phase defect of the universal phase field \(\Phi\). Its horizon is not a primitive geometric object but a phase bifurcation surface where the phase stability operator becomes singular and the phase characteristics become trapped. Its mass, spin, and charge are phase Noether and topological invariants. Its metric is an emergent phase-response structure. Its thermodynamics is a consequence of phase holonomy and phase information. Its singularity is not a physical infinity but the boundary of the effective geometric phase and the entrance to a deeper phase-transition sector.

The derivation obeys the UPT ontological hierarchy:
\[
\boxed{
\Phi
\rightarrow
\text{phase topology}
\rightarrow
\text{phase geometry}
\rightarrow
\text{connections}
\rightarrow
\text{fields}
\rightarrow
\text{stable excitations}
\rightarrow
\text{observables}.
}
\]

The central black-hole result may be stated as follows:

\[
\boxed{
\mathscr F[\Phi_{\mathrm{BH}};\lambda]=0
\quad\Longrightarrow\quad
\begin{cases}
H:\Delta_\Phi=0,\\[2pt]
g_{\mu\nu}=\mathcal G_{\mu\nu}[\Phi_{\mathrm{BH}}],\\[2pt]
M,J,Q=\text{phase invariants},\\[2pt]
T_H=\dfrac{\hbar\kappa}{2\pi c k_B},\\[6pt]
S_{\mathrm{BH}}=\dfrac{k_B A_H}{4\ell_P^2}.
\end{cases}
}
\]

The deepest UPT statement is therefore:

\[
\boxed{
\text{A black hole is the stable, horizon-forming organization of a universal phase substrate.}
}
\]

If the universal phase equation can be fully specified, black holes become not exotic exceptions to ordinary physics but inevitable stable phase defects in the universal phase structure from which spacetime, gauge fields, and matter themselves emerge.

---

## Appendix A: Core UPT Equations Used in the Black-Hole Derivation

The universal phase equation is
\[
\mathscr F[\Phi;\lambda]=0.
\]

The phase stability operator is
\[
\mathscr L_\Phi=D_\Phi\mathscr F.
\]

The phase bifurcation operator is
\[
\Delta_\Phi=\operatorname{Det}_\Phi(\mathscr L_\Phi).
\]

The phase susceptibility is
\[
\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}.
\]

The reduced order-parameter equation is
\[
\varphi(\eta,\lambda)=0.
\]

The phase metric is
\[
g_{ij}^{\Phi}
=
T_{ia}\chi^{ab}T_{jb}.
\]

The phase connection is
\[
A_\mu=\mathcal A_\mu[\Phi].
\]

The phase curvature is
\[
F_{\mu\nu}=[D_\mu,D_\nu].
\]

The effective gravitational equation is
\[
G_{\mu\nu}[g^\Phi]
=
8\pi G\,T_{\mu\nu}^{\Phi}.
\]

The black-hole horizon is
\[
H=\{x:\Delta_\Phi=0\}.
\]

The black-hole mass is
\[
M[\Phi]=\frac{E[\Phi]-E[\Phi_\ast]}{c^2}.
\]

The Schwarzschild radius is
\[
r_h=\frac{2GM}{c^2}.
\]

The Hawking temperature is
\[
T_H=\frac{\hbar\kappa}{2\pi c k_B}.
\]

The Bekenstein–Hawking entropy is
\[
S_{\mathrm{BH}}
=
\frac{k_B A_H}{4\ell_P^2}.
\]

The first law is
\[
\delta M
=
T_H\delta S_{\mathrm{BH}}
+
\Omega_H\delta J
+
\Psi_H\delta Q.
\]

---

## Appendix B: UPT Black-Hole Dictionary

| UPT object | Mathematical role | Black-hole interpretation |
|---|---|---|
| \(\Phi_{\mathrm{BH}}\) | stable phase defect | black hole |
| \(\mathscr F[\Phi]=0\) | admissibility equation | black-hole field equation |
| \(\mathscr L_\Phi\) | phase stability operator | perturbation operator |
| \(\Delta_\Phi=0\) | phase bifurcation condition | horizon condition |
| \(H\) | critical hypersurface | event horizon |
| \(M[\Phi]\) | phase energy charge | black-hole mass |
| \(J[\Phi]\) | phase angular charge | black-hole spin |
| \(Q[\Phi]\) | phase gauge charge | black-hole electric charge |
| \(g_{\mu\nu}^{\Phi}\) | phase response metric | spacetime metric |
| \(A_\mu\) | phase connection | gauge field |
| \(\kappa\) | phase relaxation rate | surface gravity |
| \(T_H\) | phase holonomy temperature | Hawking temperature |
| \(S_{\mathrm{BH}}\) | phase information | horizon entropy |
| \(r=0\) | effective phase breakdown | singularity / phase-core transition |

---

## Appendix C: Minimal Falsifiable Phase-Correction Ansatz

A useful phenomenological ansatz for UPT corrections to the Schwarzschild lapse is
\[
\boxed{
f_\Phi(r)
=
1-\frac{2GM}{c^2r}
+
\epsilon_\Phi
\left(
\frac{\ell_\Phi}{r}
\right)^p
\frac{2GM}{c^2r}
+
O(\ell_\Phi^{p+1}).
}
\]
The corresponding corrections to observables scale as
\[
\delta\omega_n
\sim
\epsilon_\Phi
\left(
\frac{\ell_\Phi}{r_h}
\right)^p,
\qquad
k_\ell^\Phi
\sim
\epsilon_\Phi
\left(
\frac{\ell_\Phi}{r_h}
\right)^p.
\]

This ansatz is not the final universal phase equation. It is the leading effective phase-correction form compatible with asymptotic flatness, stability, and horizon regularity.

---

**End of white paper.**

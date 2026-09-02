# Universal Phase Theory and the Photon

## Massless Phase Excitations, Invariant Light Speed, and Null Propagation Without Proper Time

**Dust LLC Preprint Series — UPT-001**  
**Foundational White Paper**

---

## Abstract

We develop the Universal Phase Theory (UPT) derivation of the photon as a massless, stable, transverse phase excitation of an emergent \(U(1)\) phase connection. The derivation does not begin with Maxwell theory, special relativity, or a pre-existing spacetime. It begins from the universal phase field \(\Phi\), the universal phase equation
\[
\mathscr F[\Phi;\lambda]=0,
\]
the phase stability operator
\[
\mathscr L_\Phi=D_\Phi\mathscr F,
\]
the phase bifurcation operator
\[
\Delta_\Phi=\operatorname{Det}_\Phi(\mathscr L_\Phi),
\]
and the phase susceptibility
\[
\boldsymbol{\chi}_\Phi=\mathscr L_\Phi^{-1}.
\]
Spacetime geometry is constructed as a response geometry of phase, with emergent metric
\[
g^{\Phi}_{ij}=T_{ia}\chi^{ab}T_{jb}.
\]
Phase transport produces a connection
\[
A_\mu=\mathcal A_\mu[\Phi],
\]
whose curvature
\[
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu
\]
measures the nontriviality of comparing phase frames. In a stable UPT vacuum \(\Phi_*\) whose phase isotropy contains an unbroken central \(U(1)\), the low-energy phase connection supports transverse massless modes. These modes are identified as photons.

The central results are fourfold. First, the constancy of the speed of light follows from the vacuum phase metric and its invariant null cone. Second, the photon is massless because the unbroken \(U(1)\) phase-frame redundancy forbids a mass term in the phase stability operator. Third, photon propagation follows null geodesics of the emergent phase metric, so the proper time along a photon trajectory vanishes:
\[
d\tau_\Phi^2=-\frac{1}{c^2}g^\Phi_{\mu\nu}dx^\mu dx^\nu=0.
\]
Fourth, a photon does not possess an internal temporal evolution. Its phase is not an aging variable but a relational holonomy. Along a null phase ray with wave covector \(k_\mu=\partial_\mu\theta\),
\[
k^\mu\partial_\mu\theta=g^{\mu\nu}k_\mu k_\nu=0,
\]
so the phase is constant along its own ray. Observed frequency is an observer-dependent projection of the null phase covector, not a photon-internal clock.

The paper establishes the UPT ontological chain for the photon:
\[
\Phi
\rightarrow
\text{phase topology}
\rightarrow
\text{phase geometry}
\rightarrow
U(1)\text{ phase connection}
\rightarrow
F_{\mu\nu}
\rightarrow
\gamma
\rightarrow
\text{optical observables}.
\]
The photon is therefore not an object moving through time. It is a stable null phase relation of the universal phase substrate.

**Keywords:** Universal Phase Theory, photon, massless phase excitation, emergent spacetime, phase metric, phase connection, null propagation, proper time, holonomy, phase holonomy, invariant light speed.

---

# Part I. Foundational Framework

## 1. Phase as the Primitive Substrate

Universal Phase Theory is organized by the principle of phase primacy:

\[
\boxed{
\text{Phase is not a property of a pre-existing physical system.}
}
\]

Rather,

\[
\boxed{
\text{Physical systems are stable organizations of phase.}
}
\]

The primitive object is the universal phase field

\[
\Phi:\mathcal X\rightarrow\mathcal M_\Phi,
\]

where \(\mathcal X\) is a generalized base domain and \(\mathcal M_\Phi\) is the phase manifold. The base \(\mathcal X\) is not assumed to be spacetime. Spacetime is an emergent phase structure,

\[
M_{\mathrm{eff}}=\mathcal E[\Phi].
\]

The generative hierarchy of UPT is

\[
\boxed{
\Phi
\rightarrow
\text{topology}
\rightarrow
\text{geometry}
\rightarrow
\text{connections}
\rightarrow
\text{fields}
\rightarrow
\text{particles}
\rightarrow
\text{observables}.
}
\]

The photon must therefore be derived not as an elementary field inserted into spacetime, but as a stable excitation of phase itself.

---

## 2. The Universal Phase Equation

The admissible configurations of phase are determined by the universal phase equation

\[
\boxed{
\mathscr F[\Phi;\lambda]=0.
}
\]

Here \(\lambda^i\) denotes control parameters, scale variables, boundary data, or effective phase constraints. The solution space is

\[
\operatorname{Sol}(\lambda)
=
\{\Phi\in\Gamma(E_\Phi):\mathscr F[\Phi;\lambda]=0\}.
\]

The phase stability operator is the functional derivative

\[
\boxed{
\mathscr L_\Phi
=
D_\Phi\mathscr F.
}
\]

For a solution \(\Phi_0\), a perturbation \(\Phi=\Phi_0+\epsilon\delta\Phi\) gives

\[
\mathscr F[\Phi_0+\epsilon\delta\Phi]
=
\mathscr F[\Phi_0]
+
\epsilon\mathscr L_{\Phi_0}\delta\Phi
+
O(\epsilon^2).
\]

Since \(\mathscr F[\Phi_0]=0\), the linearized phase equation is

\[
\boxed{
\mathscr L_{\Phi_0}\delta\Phi=0.
}
\]

The kernel

\[
K_{\Phi_0}=\ker\mathscr L_{\Phi_0}
\]

defines the soft phase directions.

---

## 3. Bifurcation, Criticality, and Susceptibility

The phase bifurcation operator is

\[
\boxed{
\Delta_\Phi
=
\operatorname{Det}_\Phi(\mathscr L_\Phi).
}
\]

The critical phase manifold is

\[
\boxed{
\Sigma_\Phi
=
\{\Phi:\Delta_\Phi=0\}.
}
\]

Where \(\mathscr L_\Phi\) is invertible, the phase susceptibility is

\[
\boxed{
\boldsymbol{\chi}_\Phi
=
\mathscr L_\Phi^{-1}.
}
\]

Near critical directions, \(\boldsymbol{\chi}_\Phi\) develops poles. These poles correspond to massless or nearly massless phase excitations.

For the photon, the relevant pole occurs in the \(U(1)\) phase-connection sector and lies on the null cone of the emergent phase metric.

---

## 4. Lyapunov–Schmidt Reduction and Order Parameters

Let the phase configuration space decompose as

\[
\mathcal C_\Phi
=
K_\Phi\oplus R_\Phi,
\]

where

\[
K_\Phi=\ker\mathscr L_\Phi
\]

is the critical phase subspace and \(R_\Phi\) is its complement.

A perturbation near criticality may be written

\[
\delta\Phi
=
\eta^a e_a
+
\xi,
\]

where \(\{e_a\}\) spans \(K_\Phi\) and \(\xi\in R_\Phi\).

The noncritical component is locally solvable:

\[
\xi=\xi(\eta,\lambda).
\]

Substitution into the universal phase equation yields the reduced bifurcation equation

\[
\boxed{
\varphi(\eta,\lambda)=0.
}
\]

The coordinates \(\eta^a\) are the order parameters of the phase transition.

For the photon, the relevant order parameter is not a scalar symmetry-breaking amplitude but a transverse phase-connection mode

\[
\eta^a\rightarrow a_\mu(x).
\]

The photon is therefore a critical phase-connection excitation.

---

# Part II. Emergent Phase Geometry and the Invariant Speed \(c\)

## 5. Phase Metric from Susceptibility

Let \(\eta^a(\lambda^i)\) denote the equilibrium order parameters as functions of control directions \(\lambda^i\). Define the control-coupling tensor

\[
T_{ia}
=
\frac{\partial \eta_a}{\partial\lambda^i}.
\]

Let the stability tensor be

\[
S_{ab}
=
\frac{\partial^2\Phi_{\mathrm{eff}}}{\partial\eta^a\partial\eta^b},
\]

and define the susceptibility tensor

\[
\chi^{ab}
=
(S^{-1})^{ab}.
\]

The UPT phase metric on control space is

\[
\boxed{
g^\Phi_{ij}
=
T_{ia}\chi^{ab}T_{jb}.
}
\]

This metric is not assumed. It measures the distinguishability of neighboring phase configurations.

The phase line element is

\[
\boxed{
ds_\Phi^2
=
g^\Phi_{ij}d\lambda^i d\lambda^j.
}
\]

When the stable vacuum phase selects four effective macroscopic directions, these directions become the coordinates of emergent spacetime:

\[
x^\mu=\mathcal E^\mu[\Phi_*].
\]

The effective spacetime metric is then

\[
\boxed{
g_{\mu\nu}
=
g^\Phi_{\mu\nu}[\Phi_*].
}
\]

---

## 6. Homogeneous Vacuum and the Emergence of \(c\)

Let \(\Phi_*\) be a stable UPT vacuum satisfying

\[
\mathscr F[\Phi_*;\lambda_*]=0,
\]

and suppose the vacuum is homogeneous and isotropic in its effective macroscopic phase directions.

Choose effective coordinates

\[
x^\mu=(t,x^1,x^2,x^3).
\]

Homogeneity and isotropy imply that the vacuum phase metric takes the form

\[
g^\Phi_{00}=-\alpha^2,
\qquad
g^\Phi_{ij}=\beta^2\delta_{ij},
\qquad
g^\Phi_{0i}=0,
\]

where \(\alpha\) and \(\beta\) are positive vacuum phase-response constants.

Thus

\[
ds_\Phi^2
=
-\alpha^2dt^2
+
\beta^2\delta_{ij}dx^i dx^j.
\]

Define

\[
\boxed{
c
=
\frac{\alpha}{\beta}.
}
\]

Then

\[
ds_\Phi^2
=
-c^2dt^2
+
d\mathbf x^2.
\]

Equivalently, using \(x^0=ct\),

\[
\boxed{
ds_\Phi^2
=
-(dx^0)^2+d\mathbf x^2.
}
\]

The invariant speed \(c\) is therefore not inserted as a property of light. It is the invariant slope of the null cone of the vacuum phase metric.

---

## 7. Null Cone and Lorentz Structure

The null cone of the emergent phase metric is defined by

\[
\boxed{
g^{\mu\nu}k_\mu k_\nu=0.
}
\]

In vacuum coordinates,

\[
-(k^0)^2+\mathbf k^2=0.
\]

Hence

\[
|\mathbf k|=k^0.
\]

Restoring \(c\),

\[
|\mathbf k|=\frac{\omega}{c}.
\]

Phase transformations preserving the vacuum phase metric satisfy

\[
\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma g_{\mu\nu}
=
g_{\rho\sigma}.
\]

In local inertial phase coordinates, this is the Lorentz group

\[
SO(1,3),
\]

or its double cover

\[
SL(2,\mathbb C).
\]

Thus Lorentz symmetry is the symmetry of the stable phase metric, not a background assumption.

The constancy of the speed of light follows because the null cone is a geometric property of the vacuum phase metric. All massless phase excitations coupled to the same phase metric propagate on that cone.

---

# Part III. Phase Connection and the Electromagnetic Field

## 8. Phase Frames and Phase Transport

At each point of the effective base, phase states are compared using phase frames. Let

\[
P_\Phi\rightarrow M_{\mathrm{eff}}
\]

be the phase frame bundle with structure group \(\mathscr G_\Phi\).

A local phase frame is a section

\[
s:U\subset M_{\mathrm{eff}}\rightarrow P_\Phi.
\]

The Maurer–Cartan form on the phase frame bundle is

\[
\omega
=
s^{-1}ds.
\]

Its vertical projection defines the phase connection

\[
\boxed{
A_\mu
=
\mathcal A_\mu[\Phi].
}
\]

The connection is not introduced as an independent electromagnetic field. It is the structure required to compare phase frames at neighboring points.

Under a local phase-frame transformation

\[
s\mapsto sg(x),
\]

the connection transforms as

\[
A_\mu
\mapsto
gA_\mu g^{-1}
+
g\partial_\mu g^{-1}.
\]

For an Abelian \(U(1)\) factor,

\[
g(x)=e^{i\alpha(x)},
\]

and, up to convention,

\[
\boxed{
A_\mu\mapsto A_\mu+\partial_\mu\alpha.
}
\]

The curvature is

\[
\boxed{
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu.
}
\]

It is invariant under Abelian phase-frame transformations.

UPT therefore identifies

\[
\boxed{
\text{electromagnetic gauge structure}
=
U(1)\text{ phase-frame redundancy}.
}
\]

---

## 9. Vacuum Isotropy and the Unbroken \(U(1)\) Sector

Let \(\Phi_*\) be a vacuum phase whose stabilizer contains a central Abelian factor:

\[
G_{\Phi_*}\supset U(1).
\]

The corresponding phase connection is denoted

\[
A_\mu^{(U(1))}.
\]

Because this factor is unbroken, the phase action is invariant under

\[
A_\mu\mapsto A_\mu+\partial_\mu\alpha.
\]

This invariance forbids a mass term

\[
m^2 A_\mu A^\mu.
\]

Thus the photon masslessness is not assumed. It is a consequence of unbroken \(U(1)\) phase-frame redundancy.

---

## 10. Quadratic Phase Action for the \(U(1)\) Connection

The effective phase functional for slowly varying phase connections is expanded in phase invariants. The leading local, gauge-invariant, two-derivative term is

\[
\boxed{
\Gamma_2[A]
=
\frac12
\int d^4x\sqrt{-g}\,
F_{\mu\nu}
\Upsilon^{\mu\nu\rho\sigma}
F_{\rho\sigma}.
}
\]

The tensor \(\Upsilon^{\mu\nu\rho\sigma}\) is the inverse susceptibility in the connection sector:

\[
\Upsilon
=
\boldsymbol{\chi}_{A}^{-1}.
\]

Vacuum Lorentz invariance forces

\[
\boxed{
\Upsilon^{\mu\nu\rho\sigma}
=
\frac{1}{4Z}
\left(
g^{\mu\rho}g^{\nu\sigma}
-
g^{\mu\sigma}g^{\nu\rho}
\right),
}
\]

where \(Z=Z[\Phi_*]\) is the vacuum phase stiffness.

Therefore

\[
\boxed{
\Gamma_2[A]
=
-\frac{1}{4Z}
\int d^4x\sqrt{-g}\,
F_{\mu\nu}F^{\mu\nu}.
}
\]

This is the UPT derivation of the free electromagnetic action. The Maxwell structure is the universal infrared effective action of an unbroken Abelian phase connection.

---

## 11. Maxwell Equations as Phase Stability Equations

Varying \(\Gamma_2[A]\) with respect to \(A_\mu\) gives

\[
\delta\Gamma_2
=
-\frac{1}{2Z}
\int d^4x\sqrt{-g}\,
F^{\mu\nu}\delta F_{\mu\nu}.
\]

Since

\[
\delta F_{\mu\nu}
=
\partial_\mu\delta A_\nu-\partial_\nu\delta A_\mu,
\]

integration by parts yields

\[
\delta\Gamma_2
=
\frac{1}{Z}
\int d^4x\sqrt{-g}\,
(\nabla_\mu F^{\mu\nu})\delta A_\nu.
\]

The stationary phase condition is therefore

\[
\boxed{
\nabla_\mu F^{\mu\nu}=0.
}
\]

The curvature identity

\[
F=dA
\]

implies the Bianchi identity

\[
\boxed{
\nabla_{[\alpha}F_{\beta\gamma]}=0.
}
\]

Thus the source-free Maxwell equations are the linearized phase stability equations of the unbroken \(U(1)\) phase connection.

---

# Part IV. The Photon as a Massless Phase Excitation

## 12. Linearized Phase Stability Operator for the Connection

Let

\[
A_\mu=a_\mu
\]

be a small phase-connection perturbation around the vacuum. The linearized phase equation is

\[
\boxed{
\nabla_\mu f^{\mu\nu}=0,
}
\]

where

\[
f_{\mu\nu}
=
\partial_\mu a_\nu-\partial_\nu a_\mu.
\]

In flat vacuum phase coordinates,

\[
\partial_\mu
\left(
\partial^\mu a^\nu-\partial^\nu a^\mu
\right)
=
0.
\]

Thus

\[
\boxed{
\Box a^\nu-\partial^\nu(\partial_\mu a^\mu)=0.
}
\]

The phase stability operator in momentum space is

\[
\boxed{
K^{\mu\nu}(k)
=
Z
\left(
k^2 g^{\mu\nu}-k^\mu k^\nu
\right).
}
\]

The equation for modes is

\[
K^{\mu\nu}(k)a_\nu(k)=0.
\]

---

## 13. Gauge Redundancy and the Absence of Photon Mass

The most general local quadratic stability tensor for a vector phase mode is

\[
K^{\mu\nu}(k)
=
Z(k^2)
\left(
k^2 g^{\mu\nu}-k^\mu k^\nu
\right)
+
m^2g^{\mu\nu}.
\]

Phase-frame redundancy requires invariance under

\[
a_\mu(k)\mapsto a_\mu(k)+\alpha(k)k_\mu.
\]

Therefore the stability operator must annihilate pure gauge directions:

\[
K^{\mu\nu}(k)k_\nu=0.
\]

But

\[
\left(
m^2g^{\mu\nu}
\right)k_\nu
=
m^2k^\mu.
\]

Thus

\[
\boxed{
m^2=0.
}
\]

The photon is massless because a mass term would violate the unbroken \(U(1)\) phase-frame redundancy.

---

## 14. Bifurcation Operator and the Photon Pole

The bifurcation operator in the connection sector is the determinant of the stability operator restricted to physical modes. Gauge directions are removed by gauge fixing.

In a covariant gauge,

\[
K^{\mu\nu}_\xi(k)
=
Z
\left[
k^2 g^{\mu\nu}
-
\left(1-\frac{1}{\xi}\right)k^\mu k^\nu
\right].
\]

The physical determinant is proportional to

\[
\boxed{
\Delta_A(k)
\propto
(k^2)^2.
}
\]

Hence the critical manifold is

\[
\boxed{
k^2=0.
}
\]

The susceptibility is the inverse stability operator. In gauge-fixed form,

\[
\boxed{
\chi^{\mu\nu}(k)
=
\frac{1}{Z}
\frac{1}{k^2+i0}
\left[
g^{\mu\nu}
-
(1-\xi)\frac{k^\mu k^\nu}{k^2}
\right].
}
\]

The pole at

\[
k^2=0
\]

is the UPT signature of a massless phase excitation. That excitation is the photon.

---

## 15. Plane-Wave Solutions and Transversality

Take a plane phase mode

\[
a_\mu(x)
=
\varepsilon_\mu e^{i\theta(x)},
\]

with wave covector

\[
k_\mu=\partial_\mu\theta.
\]

The linearized equation gives

\[
k^2\varepsilon^\mu
-
(k\cdot\varepsilon)k^\mu
=
0.
\]

Choose Lorenz phase gauge

\[
\partial_\mu a^\mu=0,
\]

so that

\[
k\cdot\varepsilon=0.
\]

Then a nonzero transverse polarization requires

\[
\boxed{
k^2=0.
}
\]

Thus photon wave covectors are null.

The residual gauge freedom is

\[
\varepsilon_\mu
\mapsto
\varepsilon_\mu+\alpha k_\mu.
\]

This removes longitudinal gauge components, leaving two physical transverse polarizations.

---

## 16. Photon Helicity from Phase Holonomy

Let \(\mathbf e_1,\mathbf e_2\) span the transverse polarization plane. Define circular polarization vectors

\[
\mathbf e_\pm
=
\frac{1}{\sqrt2}
\left(
\mathbf e_1\pm i\mathbf e_2
\right).
\]

A spatial rotation by angle \(\phi\) in the transverse plane acts as

\[
\mathbf e_\pm
\mapsto
e^{\pm i\phi}\mathbf e_\pm.
\]

Thus the phase holonomy of the transverse phase connection gives helicity

\[
\boxed{
h=\pm1.
}
\]

The photon is therefore a spin-one phase excitation with two helicity states.

---

# Part V. Constant Light Speed and Null Propagation Without Time

## 17. Eikonal Limit of the Phase Equation

In the high-frequency phase limit, write

\[
a_\mu(x)
=
\operatorname{Re}
\left[
\mathcal a_\mu(x)e^{i\theta(x)/\epsilon}
\right],
\]

with \(\epsilon\to0\). The wave covector is

\[
\boxed{
k_\mu=\partial_\mu\theta.
}
\]

The leading phase equation gives

\[
\boxed{
g^{\mu\nu}k_\mu k_\nu=0.
}
\]

This is the eikonal equation of UPT. It states that phase fronts of the photon are null hypersurfaces of the emergent phase metric.

---

## 18. Photon Rays Are Null Geodesics

Define phase rays by

\[
\boxed{
\frac{dx^\mu}{ds}
=
k^\mu
=
g^{\mu\nu}k_\nu.
}
\]

Using

\[
k_\mu=\partial_\mu\theta,
\]

one finds

\[
k^\nu\nabla_\nu k_\mu
=
k^\nu\nabla_\mu k_\nu
=
\frac12\nabla_\mu(k^\nu k_\nu).
\]

Since

\[
k^\nu k_\nu=0,
\]

it follows that

\[
\boxed{
k^\nu\nabla_\nu k^\mu=0.
}
\]

Thus photon rays are geodesics of the emergent phase metric.

Because

\[
g_{\mu\nu}k^\mu k^\nu=0,
\]

they are null geodesics.

---

## 19. Constancy of the Speed of Light

In local vacuum phase coordinates,

\[
ds_\Phi^2
=
-c^2dt^2+d\mathbf x^2.
\]

For a null ray,

\[
ds_\Phi^2=0.
\]

Therefore

\[
c^2dt^2=d\mathbf x^2,
\]

and hence

\[
\boxed{
\frac{d|\mathbf x|}{dt}=c.
}
\]

The speed \(c\) is constant because it is the invariant slope of the vacuum phase null cone.

In a curved phase geometry, the same statement holds locally. In local inertial phase frames,

\[
g_{\mu\nu}\to\eta_{\mu\nu},
\qquad
\partial_\rho g_{\mu\nu}\to0,
\]

and all photons propagate locally with speed \(c\).

---

## 20. Zero Proper Time Along Photon Trajectories

The proper time associated with a curve \(\gamma\) in the emergent phase geometry is

\[
\boxed{
d\tau_\Phi^2
=
-\frac{1}{c^2}
g^\Phi_{\mu\nu}dx^\mu dx^\nu
}
\]

for timelike curves.

For a photon ray,

\[
g^\Phi_{\mu\nu}dx^\mu dx^\nu=0.
\]

Therefore

\[
\boxed{
d\tau_\Phi=0.
}
\]

The photon accumulates no proper time between emission and absorption.

This is not a statement about coordinate time. Coordinate time may elapse between emission and detection. But the phase interval along the photon worldline is null.

---

## 21. The Photon Has No Internal Clock

For a massive phase excitation, the phase oscillation may be associated with proper time:

\[
\psi\sim e^{-imc^2\tau/\hbar}.
\]

For the photon,

\[
m=0.
\]

There is no rest frame and no proper-time phase oscillation.

Equivalently, let \(\theta\) be the photon eikonal phase. Along a photon ray,

\[
\frac{d\theta}{ds}
=
\frac{dx^\mu}{ds}\partial_\mu\theta
=
k^\mu k_\mu
=
0.
\]

Thus

\[
\boxed{
k^\mu\partial_\mu\theta=0.
}
\]

The photon phase is constant along its own ray.

The photon does not age. It does not traverse spacetime by evolving through an internal temporal parameter. It is a null phase relation connecting emission and absorption events.

---

## 22. Observer Time Versus Photon Time

Let an observer have timelike four-velocity \(u^\mu\), normalized by

\[
g_{\mu\nu}u^\mu u^\nu=-c^2.
\]

The frequency measured by that observer is

\[
\boxed{
\omega
=
-u^\mu k_\mu.
}
\]

This is a projection of the photon null covector onto the observer’s phase frame. It is not an internal photon frequency.

The photon four-momentum is

\[
\boxed{
p_\mu=\hbar k_\mu.
}
\]

Since

\[
g^{\mu\nu}k_\mu k_\nu=0,
\]

we have

\[
p^\mu p_\mu=0.
\]

Thus

\[
\boxed{
E=pc.
}
\]

The observed energy is

\[
\boxed{
E=\hbar\omega.
}
\]

But \(\omega\) is observer-dependent phase rate, not photon proper-time evolution.

---

# Part VI. Photon Ontology in Universal Phase Theory

## 23. The Photon as a Stable Phase Excitation

UPT defines a particle as a stable localized phase excitation:

\[
\boxed{
\text{particle}
=
\text{stable localized phase excitation}.
}
\]

For the photon, the phase excitation is a finite-energy wave packet of the massless \(U(1)\) phase connection.

Let

\[
\Phi
=
\Phi_*
+
\Phi_\gamma
+
\cdots,
\]

where \(\Phi_\gamma\) denotes the photon phase perturbation. The corresponding field strength is

\[
F_{\mu\nu}[\Phi_\gamma]
\neq0.
\]

The photon is not the gauge-dependent potential \(A_\mu\). Its invariant content is carried by the curvature \(F_{\mu\nu}\), its helicity, its energy-momentum, and its phase holonomy.

---

## 24. Photon Energy-Momentum as Phase Stress

The effective phase stress tensor is

\[
\boxed{
T_{\mu\nu}^{\Phi}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta\Gamma_\Phi}{\delta g^{\mu\nu}}.
}
\]

For the quadratic \(U(1)\) phase action,

\[
T_{\mu\nu}
=
\frac{1}{Z}
\left(
F_{\mu\alpha}F_\nu{}^\alpha
-
\frac14 g_{\mu\nu}F_{\alpha\beta}F^{\alpha\beta}
\right).
\]

For a high-frequency wave packet,

\[
\boxed{
\langle T_{\mu\nu}\rangle
=
\mathcal E\, k_\mu k_\nu,
}
\]

with \(\mathcal E\) a positive phase-energy density. This is the stress tensor of null phase flow.

Thus photon energy propagates along the same null direction as the phase covector.

---

## 25. Photon Identity Without Temporal Aging

In ordinary metaphysics, an object persisting through time is imagined to possess an internal history. UPT replaces this with phase persistence.

For the photon, persistence is not internal aging but phase continuity:

\[
\boxed{
\text{photon persistence}
=
\text{phase holonomy along null structure}.
}
\]

For a closed loop \(\gamma\), the phase holonomy is

\[
\boxed{
U_\gamma
=
\exp
\left(
i\oint_\gamma A
\right).
}
\]

For two alternative phase paths \(\gamma_1,\gamma_2\) connecting the same events, the relative phase is

\[
\Delta\theta
=
\oint_{\gamma_1-\gamma_2}A.
\]

By Stokes’ theorem,

\[
\Delta\theta
=
\int_{\Sigma}F.
\]

Interference is therefore a measurement of phase curvature and phase holonomy, not of photon-internal time.

---

## 26. Traversal Without Time

The phrase “the photon traverses spacetime without time” receives a precise UPT meaning.

A photon path \(\gamma\) between emission event \(p\) and absorption event \(q\) satisfies

\[
\int_\gamma ds_\Phi^2=0.
\]

Thus

\[
\boxed{
\Delta\tau_\Phi[\gamma]=0.
}
\]

The photon does not experience a phase interval. It does not occupy a sequence of internal moments. The relation between \(p\) and \(q\) is a null phase relation established by the geometry of \(\Phi\).

The ordering of emission and absorption is supplied by the causal structure of the emergent phase metric, not by an internal photon clock.

Thus UPT replaces the picture

\[
\text{photon moves through time}
\]

with

\[
\boxed{
\text{photon is a null phase relation of the universal phase substrate}.
}
\]

---

# Part VII. Formal Propositions

## Proposition 1: Emergence of the Light Cone

Let \(\Phi_*\) be a homogeneous UPT vacuum whose phase response metric is nondegenerate with signature \((-+++)\). Then the characteristic surfaces of massless phase perturbations satisfy

\[
g^{\mu\nu}k_\mu k_\nu=0.
\]

Therefore there exists an invariant speed

\[
c=\sqrt{-g_{00}/g_{ij}\hat n^i\hat n^j},
\]

which is constant in homogeneous vacuum.

**Proof.** The phase metric is

\[
g^\Phi_{ij}=T_{ia}\chi^{ab}T_{jb}.
\]

The principal symbol of the phase stability operator determines characteristic propagation. For a massless phase mode, nontrivial solutions require the principal symbol to vanish:

\[
\det\sigma(\mathscr L_\Phi)(k)=0.
\]

In the unbroken \(U(1)\) sector,

\[
\sigma(K)(k)
=
Z(k^2g^{\mu\nu}-k^\mu k^\nu).
\]

Nonzero transverse modes require

\[
k^2=g^{\mu\nu}k_\mu k_\nu=0.
\]

In homogeneous coordinates,

\[
g^\Phi_{00}=-\alpha^2,
\qquad
g^\Phi_{ij}=\beta^2\delta_{ij},
\]

so null propagation gives

\[
|\dot{\mathbf x}|=\alpha/\beta=c.
\]

Hence the light cone and invariant speed are geometric consequences of the vacuum phase metric. \(\square\)

---

## Proposition 2: Photon Masslessness from Phase Redundancy

Let the vacuum phase stabilizer contain an unbroken central \(U(1)\) factor. Then the corresponding phase connection \(A_\mu\) admits no mass term.

**Proof.** The phase-frame redundancy requires invariance under

\[
A_\mu\mapsto A_\mu+\partial_\mu\alpha.
\]

A mass term

\[
m^2A_\mu A^\mu
\]

transforms as

\[
m^2(A_\mu+\partial_\mu\alpha)(A^\mu+\partial^\mu\alpha),
\]

which is not invariant for arbitrary \(\alpha\). Therefore stability of the unbroken phase requires

\[
m^2=0.
\]

Equivalently, the stability operator must satisfy

\[
K^{\mu\nu}k_\nu=0,
\]

which excludes a longitudinal mass term. \(\square\)

---

## Proposition 3: Null Geodesic Propagation

Let \(k_\mu=\partial_\mu\theta\) be the wave covector of a photon phase front satisfying

\[
g^{\mu\nu}k_\mu k_\nu=0.
\]

Then the integral curves of

\[
k^\mu=g^{\mu\nu}k_\nu
\]

satisfy

\[
k^\nu\nabla_\nu k^\mu=0.
\]

Therefore photon rays are null geodesics.

**Proof.** Since \(k_\mu\) is a gradient,

\[
\nabla_\mu k_\nu=\nabla_\nu k_\mu.
\]

Then

\[
k^\nu\nabla_\nu k_\mu
=
k^\nu\nabla_\mu k_\nu
=
\frac12\nabla_\mu(k^\nu k_\nu).
\]

But \(k^\nu k_\nu=0\). Hence

\[
k^\nu\nabla_\nu k_\mu=0.
\]

Raising the index gives

\[
k^\nu\nabla_\nu k^\mu=0.
\]

Thus the phase rays are geodesics, and because \(k^2=0\), they are null. \(\square\)

---

## Proposition 4: Zero Photon Proper Time

Let \(\gamma\) be a photon trajectory. Then

\[
g_{\mu\nu}dx^\mu dx^\nu=0
\]

along \(\gamma\). Therefore

\[
d\tau_\Phi
=
\frac{1}{c}
\sqrt{-g_{\mu\nu}dx^\mu dx^\nu}
=
0.
\]

Thus the photon accumulates no proper time.

**Proof.** Direct from the null condition. \(\square\)

---

## Proposition 5: Phase Constancy Along Photon Rays

Let \(\theta\) be the photon eikonal phase and let

\[
k_\mu=\partial_\mu\theta.
\]

Then along the ray,

\[
\frac{d\theta}{ds}
=
k^\mu\partial_\mu\theta
=
k^\mu k_\mu
=
0.
\]

Thus the photon phase is constant along its own ray.

**Proof.** Direct substitution of the null condition. \(\square\)

---

# Part VIII. What UPT Derives and What Remains to Be Derived

## 27. Derived in This Paper

The following photon properties are derived from UPT phase structure:

1. **Existence of a massless \(U(1)\) phase excitation.**  
   Derived from unbroken phase-frame redundancy.

2. **Maxwellian field equations.**  
   Derived as the leading gauge-invariant phase stability equations.

3. **Two transverse polarizations.**  
   Derived from gauge redundancy and transversality.

4. **Helicity \(\pm1\).**  
   Derived from phase holonomy of the transverse phase plane.

5. **Invariant local speed \(c\).**  
   Derived from the null cone of the emergent phase metric.

6. **Null geodesic propagation.**  
   Derived from the eikonal limit of the phase equation.

7. **Zero proper time along photon trajectories.**  
   Derived from the null phase interval.

8. **Observer-dependent frequency.**  
   Derived as projection of the photon wave covector onto observer phase frames.

9. **Interference as phase holonomy.**  
   Derived from phase transport and curvature.

---

## 28. Not Derived Here and Required for Completion

The following are not inserted by assumption and remain required UPT derivations:

1. **Unique emergence of the \(U(1)\) factor from the full phase manifold.**  
   The present derivation assumes a vacuum whose phase isotropy contains an unbroken central \(U(1)\).

2. **Numerical value of \(c\).**  
   The invariance of \(c\) is derived. Its measured numerical value requires phase-scale selection and unit fixing.

3. **Numerical value of \(\hbar\).**  
   The phase-quantum correspondence \(p_\mu=\hbar k_\mu\) requires derivation of the quantum scale from phase structure.

4. **Electric charge quantization.**  
   Charge must arise from phase topology and bundle invariants.

5. **Full interacting quantum electrodynamics.**  
   The free photon is derived here. Photon-matter interactions require derivation from coupled phase sectors.

6. **Born rule for photon detection.**  
   Phase measure and probability must be derived from UPT, not assumed.

These are not defects of the photon derivation. They define the next required stages of the UPT program.

---

# Part IX. Falsifiability Criteria

A UPT photon derivation must be experimentally distinguishable. The following criteria apply.

## Criterion 1: Photon Masslessness

UPT with unbroken \(U(1)\) phase redundancy predicts

\[
m_\gamma=0.
\]

Observation of a nonzero photon rest mass in vacuum would falsify the minimal UPT photon sector.

---

## Criterion 2: Two Propagating Polarizations

The minimal UPT phase connection predicts exactly two transverse photon polarizations.

Observation of a propagating longitudinal photon mode in vacuum would imply either broken \(U(1)\) phase structure or additional phase sectors.

---

## Criterion 3: Vacuum Light-Cone Propagation

The leading UPT photon satisfies

\[
k^2=0.
\]

Thus vacuum propagation is nondispersive:

\[
\omega=c|\mathbf k|.
\]

Detection of energy-dependent vacuum light speed not attributable to known media, gravitational effects, or higher-order quantum corrections would constrain the minimal UPT vacuum.

---

## Criterion 4: Universal Coupling to Phase Metric

All massless phase excitations coupled to the same vacuum phase metric share the same null cone.

Violation of universality between photon propagation and other massless modes would falsify the common phase-metric assumption.

---

## Criterion 5: Holonomy-Based Interference

UPT predicts that electromagnetic interference is governed by phase holonomy:

\[
\Delta\theta
=
\oint A
=
\int F.
\]

Deviations from gauge-invariant holonomy dependence would falsify the phase-connection interpretation.

---

# Part X. Research Questions

The UPT photon program generates the following required research questions.

### Q1. What is the minimal phase manifold \(\mathcal M_\Phi\) that yields an unbroken \(U(1)\) phase connection?

The goal is to derive electromagnetism from phase topology rather than assume a \(U(1)\) factor.

---

### Q2. How does the universal phase equation select a Lorentzian vacuum?

The present paper uses a vacuum phase metric with signature \((-+++)\). The full UPT program must derive this signature from phase stability.

---

### Q3. How is the numerical value of \(c\) fixed?

The invariant speed is derived geometrically. Its observed value requires a vacuum-selection principle.

---

### Q4. How does phase quantization produce photon number states?

The classical phase mode must be promoted to a quantized phase excitation through the UPT phase symplectic structure.

---

### Q5. How do matter phase sectors couple to the \(U(1)\) connection?

Photon interactions must emerge from coupling between phase defects and the \(U(1)\) phase connection.

---

### Q6. How is the Born rule derived for photon detection?

Photon probabilities must arise from phase measure, phase distinguishability, and branch stability.

---

# Part XI. Conclusion

Universal Phase Theory reinterprets the photon not as a fundamental particle moving through spacetime, but as a stable massless excitation of phase itself.

The derivation proceeds through the UPT operator hierarchy:

\[
\mathscr F[\Phi]=0
\quad\Rightarrow\quad
\mathscr L_\Phi
\quad\Rightarrow\quad
\Delta_\Phi
\quad\Rightarrow\quad
\boldsymbol{\chi}_\Phi.
\]

From the phase susceptibility emerges the metric

\[
g^\Phi_{\mu\nu}.
\]

From phase transport emerges the connection

\[
A_\mu=\mathcal A_\mu[\Phi].
\]

From the unbroken \(U(1)\) phase sector emerges the curvature

\[
F_{\mu\nu}.
\]

The photon is the stable massless excitation of this curvature.

The constancy of the speed of light is not imposed. It is the invariant slope of the null cone of the vacuum phase metric:

\[
g^{\mu\nu}k_\mu k_\nu=0.
\]

Photon propagation is null geodesic propagation:

\[
k^\nu\nabla_\nu k^\mu=0.
\]

The photon accumulates no proper time:

\[
d\tau_\Phi=0.
\]

Its phase is constant along its own ray:

\[
k^\mu\partial_\mu\theta=0.
\]

Observed frequency is an observer-dependent projection:

\[
\omega=-u^\mu k_\mu.
\]

Thus the photon does not possess an internal temporal history. It does not age. It does not move through time in the manner of a massive object. It is a null phase relation, stabilized by phase topology, transported by phase connection, and observed through phase holonomy.

The final UPT statement of the photon is therefore:

\[
\boxed{
\gamma
=
\text{stable massless }U(1)\text{ phase excitation}
}
\]

with

\[
\boxed{
k^2=0,
\qquad
d\tau_\Phi=0,
\qquad
h=\pm1,
\qquad
c=\text{invariant phase-cone speed}.
}
\]

The photon is not an object traversing time. It is a stable null organization of the universal phase substrate.

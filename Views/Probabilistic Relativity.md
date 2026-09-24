# Probabilistic Relativity: Expected Curvature, Uncertainty Stress, and the Gravitational Physics of Probability Laws

**Preprint**

---

## Abstract

We derive a physical theory from the axioms of Probabilistic Geometry (PG). The central move is to replace the classical spacetime event \(x\in M\) by a probability law \(P\in\mathcal P(M)\), and to promote gravitational curvature from a pointwise tensor \(R^{a}{}_{bcd}(x)\) to an expectation-valued tensor \(\mathcal R^{a}{}_{bcd}(P)\) obtained by parallel transport to a probabilistic barycenter. From this replacement we construct **Probabilistic General Relativity** (PGR): a Lorentzian extension of PG in which the Einstein tensor is replaced by an expected Einstein tensor, and in which the covariance of a probabilistic point appears as a new gravitational charge.

The main results are:

1. **A barycentric Einstein equation**
   \[
   G_{ab}
   -
   \frac12\Sigma^{ij}\nabla_i\nabla_j G_{ab}
   +
   Q_{ab}[\Sigma,R]
   +
   \Lambda g_{ab}
   =
   8\pi G\,T^{\mathrm{bare}}_{ab},
   \]
   where \(\Sigma^{ij}\) is the barycentric covariance of the probabilistic source and \(Q_{ab}\) contains curvature-quadratic and transport-curvature corrections.

2. **An uncertainty stress-energy tensor**
   \[
   \Theta_{ab}
   =
   \frac{1}{8\pi G}
   \left[
   \frac12\Sigma^{ij}\nabla_i\nabla_jG_{ab}
   +
   Q_{ab}[\Sigma,R]
   \right],
   \]
   which obeys an exchange law with ordinary matter and is required by the contracted Bianchi identity.

3. **A screened Newtonian limit**
   \[
   \nabla^2\Phi-\ell^2\nabla^4\Phi=4\pi G\rho,
   \qquad
   \ell^2=\frac{\sigma^2}{2},
   \]
   giving a scale-dependent gravitational constant
   \[
   G_{\mathrm{eff}}(k)=\frac{G}{1+\ell^2k^2}
   \]
   and finite-core gravitational potentials.

4. **A covariance-dependent force on probabilistic bodies**
   \[
   a^i
   =
   -\partial^i\Phi
   -
   \frac12\Sigma^{jk}\partial^i\partial_j\partial_k\Phi
   +
   O(\Sigma^2),
   \]
   or, covariantly,
   \[
   a^\mu
   =
   -\frac12\Sigma^{\alpha\beta}
   P^{\mu\nu}
   \nabla_\nu
   \left(
   R_{\alpha\rho\beta\sigma}u^\rho u^\sigma
   \right)
   +
   O(\Sigma R^2,\nabla^2R).
   \]
   This is a violation of the strong equivalence principle for extended probabilistic bodies, while preserving the weak equivalence principle for deterministic points.

5. **A cosmological perturbation law**
   \[
   \ddot\delta_k+2H\dot\delta_k
   -
   \frac{4\pi G\bar\rho}{1+\ell^2k^2}\delta_k
   =
   0,
   \]
   suppressing small-scale structure growth.

6. **Quantum-interferometric signatures**, including a tidal phase shift for a delocalized mass,
   \[
   \delta\varphi_{\mathrm{PG}}
   =
   -\frac{mT}{2\hbar}\Sigma^{ij}E_{ij},
   \qquad
   E_{ij}=R_{i0j0},
   \]
   and a curvature-variance decoherence rate
   \[
   \Gamma_{\mathrm{curv}}
   \sim
   \frac{m}{\hbar}
   \left(
   \frac12
   \Sigma^{ij}\Sigma^{kl}
   E_{ik}E_{jl}
   \right)^{1/2}.
   \]

The resulting framework treats uncertainty not as noise added to geometry but as a source of gravitational physics.

**Keywords:** probabilistic geometry, optimal transport, general relativity, expected curvature, uncertainty stress-energy, modified gravity, quantum geometry.

---

## 1. Physical Postulates

Classical general relativity is built on the assumption that events are points \(x\in M\), that matter follows worldlines \(x^\mu(\tau)\), and that curvature is evaluated pointwise:

\[
G_{ab}(x)=8\pi G T_{ab}(x)-\Lambda g_{ab}(x).
\]

Probabilistic Geometry replaces the point by a law. To obtain physics, we promote this replacement to four physical postulates.

### Postulate 1: Probabilistic events

A physical event is not a point \(x\in M\) but a probability law \(P\in\mathcal P(M)\). A deterministic event is the degenerate case \(P=\delta_x\).

### Postulate 2: Expected proper time

For two timelike-separated probabilistic events \(P,Q\), the physical proper time is an optimal expected proper time over causal couplings:

\[
\tau_{\mathrm{PG}}(P,Q)
=
\sup_{\pi\in\Pi_c(P,Q)}
\int_{M\times M}
\tau(x,y)\,d\pi(x,y),
\]

where \(\Pi_c(P,Q)\) denotes the set of causally admissible couplings and \(\tau(x,y)\) is the Lorentzian proper time between \(x\) and \(y\). In the spacelike or Riemannianized regime this reduces to the Wasserstein expected distance

\[
d(P,Q)
=
\inf_{\pi\in\Pi(P,Q)}
\int \rho(x,y)\,d\pi(x,y).
\]

### Postulate 3: Expected curvature

Curvature at a probabilistic event \(P\) is not evaluated at a single point. It is transported to a barycenter and averaged:

\[
\boxed{
\mathcal R^{a}{}_{bcd}(P)
=
\int_M
\Lambda^{a}{}_{i}(x)
\Lambda^{j}{}_{b}(x)
\Lambda^{k}{}_{c}(x)
\Lambda^{l}{}_{d}(x)
R^{i}{}_{jkl}(x)
\,dP(x).
}
\]

Here \(b=b(P)\) is the Fréchet barycenter and \(\Lambda\) denotes parallel transport along the unique geodesic from \(x\) to \(b\).

### Postulate 4: Covariance is gravitational charge

The second moment of a probabilistic event,

\[
\Sigma^{ij}(P)
=
\int_M z^i z^j\,dQ(z),
\qquad
z=\exp_b^{-1}(x),
\]

is not merely statistical information. It sources corrections to the gravitational field and to the motion of bodies. In the weak-field limit, \(\Sigma^{ij}\) behaves as a gravitational polarizability.

These postulates imply that the gravitational field equations cannot remain purely local pointwise equations when expressed in barycentric variables. They become equations involving expectation operators, covariance, and transport curvature.

---

## 2. Lorentzian Probabilistic Calculus

### 2.1 Spacetime and probabilistic points

Let \((M,g_{\mu\nu})\) be a globally hyperbolic spacetime of dimension \(4\), with signature \((- + + +)\), Levi-Civita connection \(\nabla\), and Riemann tensor \(R^\mu{}_{\nu\rho\sigma}\). Let \(\Sigma_t\) be a Cauchy hypersurface with induced Riemannian metric \(h_{ij}\). A **spacelike probabilistic event** at time \(t\) is a probability law

\[
P\in \mathcal P_2(\Sigma_t).
\]

Its barycenter \(b(P)\in\Sigma_t\) is defined by the Karcher equation

\[
\boxed{
\int_{\Sigma_t}
\exp_b^{-1}(x)\,dP(x)=0.
}
\]

In local normal coordinates centered at \(b\), writing \(z^i=\exp_b^{-1}(x)^i\), the covariance is

\[
\Sigma^{ij}
=
\int z^i z^j\,dP(z),
\qquad
\int z^i\,dP(z)=0.
\]

For a full spacetime treatment one may equivalently use the Lorentzian squared geodesic interval \(2\sigma(x,y)\) in a strongly convex normal neighborhood and define barycenters by extremizing expected proper time. The local tensorial formulas below are unaffected by this choice.

---

### 2.2 Expected proper time and causal couplings

For timelike-separated probabilistic events, define the set of causal couplings

\[
\Pi_c(P,Q)
=
\left\{
\pi\in\Pi(P,Q):
\pi\{(x,y): y\in J^+(x)\}=1
\right\}.
\]

Then

\[
\boxed{
\tau_{\mathrm{PG}}(P,Q)
=
\sup_{\pi\in\Pi_c(P,Q)}
\mathbb E_\pi[\tau(X,Y)].
}
\]

For deterministic events \(P=\delta_x\), \(Q=\delta_y\), this reduces to

\[
\tau_{\mathrm{PG}}(\delta_x,\delta_y)=\tau(x,y).
\]

For narrow probabilistic events with barycenters \(b_P,b_Q\) and covariances \(\Sigma_P,\Sigma_Q\), one obtains the expansion

\[
\tau_{\mathrm{PG}}(P,Q)^2
=
\tau(b_P,b_Q)^2
+
\Delta\tau^2[\Sigma_P,\Sigma_Q]
+
O(\Sigma^{3/2}),
\]

where \(\Delta\tau^2\) depends on the tidal tensor along the barycentric geodesic. Thus probability spread modifies proper time at second order.

---

### 2.3 Expected Riemann, Ricci, and Einstein tensors

Let \(b=b(P)\). Define parallel transport from \(x\) to \(b\) by

\[
\tau_{x\to b}:T_xM\to T_bM,
\]

with components \(\Lambda^{a}{}_{i}(x)\). The expected Riemann tensor is

\[
\mathcal R^{a}{}_{bcd}(P)
=
\int_M
\Lambda^{a}{}_{i}
\Lambda^{j}{}_{b}
\Lambda^{k}{}_{c}
\Lambda^{l}{}_{d}
R^{i}{}_{jkl}(x)
\,dP(x).
\]

The expected Ricci tensor is

\[
\boxed{
\mathcal{Ric}_{ab}(P)
=
\mathcal R^{c}{}_{acb}(P)
=
\int_M
\Lambda^{i}{}_{a}(x)
\Lambda^{j}{}_{b}(x)
\operatorname{Ric}_{ij}(x)
\,dP(x).
}
\]

The expected scalar curvature is

\[
\boxed{
\mathcal S(P)
=
g^{ab}(b)\mathcal{Ric}_{ab}(P)
=
\int_M S(x)\,dP(x).
}
\]

Therefore the expected Einstein tensor is

\[
\boxed{
\mathcal G_{ab}(P)
=
\mathcal{Ric}_{ab}(P)
-
\frac12 g_{ab}(b)\mathcal S(P).
}
\]

Because parallel transport is metric-compatible, the algebraic symmetries of the Riemann tensor are preserved. Thus \(\mathcal R(P)\) is a genuine curvature tensor at the probabilistic point \(P\).

---

### 2.4 Covariance expansion of expected curvature

Let \(T\) denote any tensor field transported to \(T_bM\). In Riemannian normal coordinates about \(b\),

\[
T(x)
=
T(b)
+
z^i\nabla_iT(b)
+
\frac12z^iz^j\nabla_i\nabla_jT(b)
+
O(|z|^3).
\]

Parallel transport itself has the expansion

\[
\Lambda^{a}{}_{i}(z)
=
\delta^{a}_{i}
-
\frac16 R^{a}{}_{kil}(b)z^kz^l
+
O(|z|^3).
\]

Applying this to the Riemann tensor and integrating against \(P\), the first moment vanishes by the barycenter condition:

\[
\int z^i\,dP(z)=0.
\]

The second moment gives the covariance \(\Sigma^{ij}\). Hence

\[
\boxed{
\mathcal R^{a}{}_{bcd}(P)
=
R^{a}{}_{bcd}(b)
+
\frac12\Sigma^{ij}\nabla_i\nabla_jR^{a}{}_{bcd}(b)
+
\Sigma^{ij}C^{a}{}_{bcd,ij}(b)
+
O(\varepsilon^3).
}
\]

Here \(C^{a}{}_{bcd,ij}\) is a universal algebraic expression quadratic in curvature, coming from the expansion of parallel transport:

\[
C(R)\sim R*R.
\]

Contracting gives

\[
\boxed{
\mathcal{Ric}_{ab}(P)
=
\operatorname{Ric}_{ab}(b)
+
\frac12\Sigma^{ij}\nabla_i\nabla_j\operatorname{Ric}_{ab}(b)
+
\Sigma^{ij}C^{\mathrm{Ric}}_{ab,ij}(b)
+
O(\varepsilon^3).
}
\]

Similarly,

\[
\boxed{
\mathcal G_{ab}(P)
=
G_{ab}(b)
+
\frac12\Sigma^{ij}\nabla_i\nabla_jG_{ab}(b)
+
\Sigma^{ij}Q_{ab,ij}(b)
+
O(\varepsilon^3).
}
\]

This is the key local expansion: a probabilistic event sees not only the curvature at its barycenter, but also curvature gradients and curvature fluctuations weighted by its covariance.

---

## 3. Probabilistic General Relativity

### 3.1 Transport curvature

The expected tensors above describe the average curvature of the base spacetime. But the space of probability laws itself has intrinsic curvature. For \(U,V\in T_P\mathcal P_2(M)\), represented by gradient vector fields on \(M\), the PG sectional curvature decomposes as

\[
K_{\mathrm{PG}}(U,V)
=
K^{L^2}(U,V)
+
3\frac{G_P(A_UV,A_UV)}{\|U\wedge V\|_G^2},
\]

where \(A\) is the O’Neill tensor of the quotient

\[
L^2(M)\longrightarrow \mathcal P_2(M).
\]

The second term is nonnegative. Even if \(M=\mathbb R^n\), so that base curvature vanishes, \(\mathcal P_2(M)\) has nonnegative intrinsic curvature. Physically, this means that probability mass rearrangement carries geometric inertia.

We define the transport Ricci contribution by polarization:

\[
\boxed{
\mathcal{Ric}^{\mathrm{tr}}_{ab}(P)U^aU^b
=
3\sum_{r=1}^{n-1}
G_P(A_{U,E_r},A_{U,E_r}),
}
\]

for \(U\) unit and \(\{E_r\}\) an orthonormal basis of the orthogonal complement of \(U\). The trace-adjusted transport Einstein tensor is

\[
\mathcal G^{\mathrm{tr}}_{ab}
=
\mathcal{Ric}^{\mathrm{tr}}_{ab}
-
\frac12g_{ab}\operatorname{tr}\mathcal{Ric}^{\mathrm{tr}}.
\]

The total expected Einstein tensor is therefore

\[
\boxed{
\mathfrak G_{ab}(P)
=
\mathcal G_{ab}(P)
+
\mathcal G^{\mathrm{tr}}_{ab}(P).
}
\]

---

### 3.2 Barycentric Einstein equation

The operational PG field equation is not a pointwise equation but an expectation-valued equation:

\[
\boxed{
\mathfrak G_{ab}[g;P_x]
=
8\pi G\,T^{\mathrm{bare}}_{ab}(x),
}
\]

where \(P_x\) is the probabilistic event associated with the barycentric event \(x\).

For a narrow probabilistic source,

\[
\mathfrak G_{ab}[g;P_x]
=
G_{ab}(x)
+
\frac12\Sigma^{ij}(x)\nabla_i\nabla_jG_{ab}(x)
+
Q_{ab}[\Sigma,R](x)
+
\mathcal G^{\mathrm{tr}}_{ab}(x)
+
O(\Sigma^{3/2}).
\]

Solving this equation for the barycentric metric to first order gives the **barycentric Einstein equation**

\[
\boxed{
G_{ab}
-
\frac12\Sigma^{ij}\nabla_i\nabla_jG_{ab}
-
Q_{ab}[\Sigma,R]
-
\mathcal G^{\mathrm{tr}}_{ab}
+
\Lambda g_{ab}
=
8\pi G\,T^{\mathrm{bare}}_{ab}.
}
\]

Equivalently, moving the covariance and transport terms to the right-hand side,

\[
\boxed{
G_{ab}+\Lambda g_{ab}
=
8\pi G
\left(
T^{\mathrm{bare}}_{ab}
+
\Theta_{ab}
\right),
}
\]

where

\[
\boxed{
\Theta_{ab}
=
\frac{1}{8\pi G}
\left[
\frac12\Sigma^{ij}\nabla_i\nabla_jG_{ab}
+
Q_{ab}[\Sigma,R]
+
\mathcal G^{\mathrm{tr}}_{ab}
\right].
}
\]

We call \(\Theta_{ab}\) the **uncertainty stress-energy tensor**.

The contracted Bianchi identity,

\[
\nabla^aG_{ab}=0,
\]

implies

\[
\nabla^a
\left(
T^{\mathrm{bare}}_{ab}
+
\Theta_{ab}
\right)
=
0.
\]

Thus ordinary matter need not be separately conserved; it exchanges energy-momentum with the uncertainty sector. This is the gravitational analogue of Reynolds stress in averaged fluid dynamics.

---

## 4. Weak-Field Limit and Screened Gravity

### 4.1 Linearized metric

Take a weak static metric

\[
ds^2
=
-(1+2\Phi)dt^2
+
(1-2\Phi)\delta_{ij}dx^idx^j,
\]

with \(|\Phi|\ll1\). Then

\[
G_{00}=2\nabla^2\Phi,
\]

and the bare Newtonian source is

\[
T^{\mathrm{bare}}_{00}=\rho.
\]

Assume an isotropic covariance

\[
\Sigma^{ij}=\sigma^2\delta^{ij}.
\]

The barycentric Einstein equation gives

\[
2\nabla^2\Phi
-
\sigma^2\nabla^4\Phi
=
8\pi G\rho.
\]

Therefore

\[
\boxed{
\nabla^2\Phi-\ell^2\nabla^4\Phi=4\pi G\rho,
\qquad
\ell^2=\frac{\sigma^2}{2}.
}
\]

Equivalently,

\[
(1-\ell^2\nabla^2)\nabla^2\Phi=4\pi G\rho.
\]

---

### 4.2 Fourier-space screening

In Fourier space,

\[
-k^2(1+\ell^2k^2)\Phi_k
=
4\pi G\rho_k.
\]

Hence

\[
\boxed{
\Phi_k
=
-\frac{4\pi G\rho_k}{k^2(1+\ell^2k^2)}.
}
\]

The effective gravitational coupling becomes scale dependent:

\[
\boxed{
G_{\mathrm{eff}}(k)
=
\frac{G}{1+\ell^2k^2}.
}
\]

For \(k\ell\ll1\), general relativity is recovered. For \(k\ell\gg1\), gravity is screened.

For an exactly Gaussian probabilistic source of width \(\sigma\), the Fourier suppression is more accurately

\[
G_{\mathrm{eff}}(k)
=
G e^{-k^2\sigma^2/2},
\]

whose Taylor expansion agrees with the local covariance equation when \(\ell^2=\sigma^2/2\).

---

### 4.3 Finite-core potentials

For a Gaussian mass distribution,

\[
\rho_\sigma(r)
=
\frac{m}{(2\pi\sigma^2)^{3/2}}
\exp\left(
-\frac{r^2}{2\sigma^2}
\right),
\]

the Newtonian potential is

\[
\boxed{
\Phi_\sigma(r)
=
-\frac{Gm}{r}
\operatorname{erf}
\left(
\frac{r}{\sqrt{2}\sigma}
\right).
}
\]

Near \(r=0\),

\[
\Phi_\sigma(r)
=
-\frac{Gm}{\sigma}\sqrt{\frac{2}{\pi}}
+
\frac{Gm}{3\sigma^3}
\sqrt{\frac{2}{\pi}}\,r^2
+
O(r^4).
\]

Thus the central singularity is replaced by a harmonic core. The force satisfies

\[
g(r)=-\partial_r\Phi_\sigma(r)
\propto r
\qquad
(r\ll\sigma).
\]

This is a direct physical consequence of treating the source as a probabilistic point rather than a deterministic point.

---

## 5. Motion of Probabilistic Bodies

### 5.1 Action for a probability cloud

For a probabilistic body of mass \(m\), let its world-tube be described by a curve of probability laws \(P_\tau\). The natural action is the expected proper-time action

\[
\boxed{
S[P]
=
-mc
\int d\lambda
\int_M
\sqrt{
-g_{\mu\nu}(x)\dot x^\mu\dot x^\nu
}
\,dP_\lambda.
}
\]

In the nonrelativistic limit, for a cloud moving with barycenter \(b(t)\),

\[
S
=
\int dt
\left[
\frac{m}{2}|\dot b|^2
-
m\int \Phi(x)\,dP(x)
\right].
\]

Write \(x=b+\xi\), with \(\langle\xi\rangle=0\), \(\langle\xi^i\xi^j\rangle=\Sigma^{ij}\). Expanding the potential,

\[
\Phi(b+\xi)
=
\Phi(b)
+
\xi^i\partial_i\Phi(b)
+
\frac12\xi^i\xi^j\partial_i\partial_j\Phi(b)
+
O(\xi^3).
\]

Averaging,

\[
\int\Phi(x)\,dP(x)
=
\Phi(b)
+
\frac12\Sigma^{ij}\partial_i\partial_j\Phi(b)
+
O(\Sigma^{3/2}).
\]

Thus

\[
L
=
\frac{m}{2}|\dot b|^2
-
m\Phi(b)
-
\frac{m}{2}\Sigma^{ij}\partial_i\partial_j\Phi(b)
+
\cdots.
\]

The Euler–Lagrange equation gives

\[
\boxed{
\ddot b^i
=
-\partial^i\Phi(b)
-
\frac12\Sigma^{jk}\partial^i\partial_j\partial_k\Phi(b)
+
O(\Sigma^2).
}
\]

The first term is the usual Newtonian acceleration. The second term is a new covariance force.

---

### 5.2 Covariant form

Define the tidal tensor relative to the barycentric four-velocity \(u^\mu\):

\[
E_{\alpha\beta}
=
R_{\alpha\rho\beta\sigma}u^\rho u^\sigma.
\]

In the weak-field limit,

\[
E_{ij}=\partial_i\partial_j\Phi.
\]

The covariance force can be written covariantly as

\[
\boxed{
a^\mu
=
u^\nu\nabla_\nu u^\mu
=
-\frac12
\Sigma^{\alpha\beta}
P^{\mu\nu}
\nabla_\nu E_{\alpha\beta}
+
O(\Sigma R^2,\nabla^2R),
}
\]

where

\[
P^{\mu\nu}=g^{\mu\nu}+u^\mu u^\nu
\]

projects orthogonal to \(u^\mu\).

This equation has a clear physical meaning: a probabilistic body does not merely fall according to the local gravitational field; it responds to the gradient of the tidal field, weighted by its own covariance.

---

### 5.3 Isotropic covariance and density-gradient force

For isotropic covariance \(\Sigma^{ij}=\sigma^2\delta^{ij}\),

\[
a^i_{\Sigma}
=
-\frac{\sigma^2}{2}
\partial^i\nabla^2\Phi.
\]

Using the Newtonian Poisson equation,

\[
\nabla^2\Phi=4\pi G\rho,
\]

one obtains

\[
\boxed{
a^i_{\Sigma}
=
-2\pi G\sigma^2\partial^i\rho.
}
\]

Thus a probabilistic body feels an additional force directed against density gradients. In a spherical halo where \(\rho\) decreases outward, \(\partial_r\rho<0\), so the covariance force points outward. This provides a geometric mechanism for core formation and puffing of dark halos.

---

### 5.4 Probabilistic equivalence principle

The classical equivalence principle states that pointlike test bodies follow geodesics. In PGR this becomes a limiting statement:

\[
\Sigma^{ij}\to0
\quad\Longrightarrow\quad
a^\mu\to0
\]

in a local inertial frame.

However, for finite covariance,

\[
\Sigma^{ij}\neq0,
\]

the body acquires a tidal-gradient acceleration. Therefore:

\[
\boxed{
\text{Deterministic points obey the equivalence principle; probabilistic bodies do not.}
}
\]

More precisely, the weak equivalence principle survives in uniform fields, because \(\nabla E_{\alpha\beta}=0\), but fails in inhomogeneous tidal fields.

---

## 6. Probabilistic Geodesic Deviation

Let two probabilistic bodies have barycentric separation \(\eta^\mu\). The usual geodesic deviation equation is

\[
\frac{D^2\eta^\mu}{d\tau^2}
=
-
R^\mu{}_{\nu\rho\sigma}
u^\nu\eta^\rho u^\sigma.
\]

In PGR, the curvature is replaced by expected curvature and the covariance force contributes an additional term. To leading covariance order,

\[
\boxed{
\frac{D^2\eta^\mu}{d\tau^2}
=
-
R^\mu{}_{\nu\rho\sigma}
u^\nu\eta^\rho u^\sigma
-
\frac12
\Sigma^{\alpha\beta}
\nabla_\alpha\nabla_\beta
\left(
R^\mu{}_{\nu\rho\sigma}
u^\nu\eta^\rho u^\sigma
\right)
+
\cdots.
}
\]

For a plane gravitational wave,

\[
R^\mu{}_{\nu\rho\sigma}(x)
\sim
\mathcal R^\mu{}_{\nu\rho\sigma}
e^{ik\cdot x},
\]

a Gaussian probabilistic detector with covariance \(\Sigma\) averages the curvature with the characteristic function

\[
\int e^{ik\cdot x}\,dP(x)
=
e^{-\frac12 k_i k_j\Sigma^{ij}}.
\]

Thus the tidal response is multiplied by the form factor

\[
\boxed{
F(k)=e^{-\frac12 k_i k_j\Sigma^{ij}}.
}
\]

High-frequency tidal fields are suppressed for delocalized detectors. This is a concrete PG correction to gravitational-wave response, atom interferometry, and resonant-mass detectors.

---

## 7. Cosmological Consequences

### 7.1 Modified Poisson equation on subhorizon scales

In a perturbed Friedmann–Lemaître–Robertson–Walker universe, the subhorizon gravitational potential satisfies the PG-modified Poisson equation

\[
\nabla^2\Phi-\ell^2\nabla^4\Phi
=
4\pi G a^2\bar\rho\delta.
\]

In Fourier space,

\[
-k^2(1+\ell^2k^2)\Phi_k
=
4\pi G a^2\bar\rho\delta_k.
\]

Therefore

\[
\Phi_k
=
-
\frac{4\pi G a^2\bar\rho\delta_k}
{k^2(1+\ell^2k^2)}.
\]

The effective gravitational constant is

\[
\boxed{
G_{\mathrm{eff}}(k)
=
\frac{G}{1+\ell^2k^2}.
}
\]

---

### 7.2 Linear growth equation

The density contrast obeys

\[
\boxed{
\ddot\delta_k
+
2H\dot\delta_k
-
\frac{4\pi G\bar\rho}{1+\ell^2k^2}
\delta_k
=
0.
}
\]

For modes with \(k\ell\ll1\), standard growth is recovered. For \(k\ell\gg1\), gravitational collapse is suppressed.

Thus PG introduces a new scale

\[
\boxed{
\lambda_{\mathrm{PG}}=2\pi\ell
}
\]

which plays the role of a probabilistic Jeans length.

---

### 7.3 Expected Raychaudhuri equation

For a congruence of probabilistic worldlines with barycentric tangent \(u^\mu\), the Raychaudhuri equation becomes

\[
\frac{d\theta}{d\tau}
=
-\frac13\theta^2
-\sigma_{\mu\nu}\sigma^{\mu\nu}
+\omega_{\mu\nu}\omega^{\mu\nu}
-
\mathfrak R_{\mu\nu}u^\mu u^\nu,
\]

where

\[
\mathfrak R_{\mu\nu}
=
\mathcal R_{\mu\nu}
+
\mathcal R^{\mathrm{tr}}_{\mu\nu}.
\]

Using the field equation,

\[
\mathfrak R_{\mu\nu}u^\mu u^\nu
=
4\pi G(\rho+3p)
-
\Lambda
+
8\pi G\Theta_{\mu\nu}u^\mu u^\nu.
\]

Thus uncertainty stress contributes directly to focusing or defocusing. In perturbation theory it behaves as a scale-dependent negative-pressure component. In a fully homogeneous treatment, transport curvature may contribute an effective background term, suggesting a possible PG origin for dark-energy-like behavior. We leave the detailed cosmological model-building to subsequent work.

---

## 8. Quantum and Interferometric Signatures

### 8.1 Mixed states as probabilistic points

Let \(\rho\) be a density matrix on a finite-dimensional Hilbert space. Its Husimi-type measure on complex projective space,

\[
q_\rho([\psi])
=
n\langle\psi|\rho|\psi\rangle
\,d\mu_{\mathrm{FS}}([\psi]),
\]

identifies \(\rho\) with a probabilistic point on \(\mathbb{CP}^{n-1}\). The Bures–Wasserstein distance,

\[
d_{\mathrm{BW}}(\rho,\sigma)^2
=
\operatorname{Tr}\rho
+
\operatorname{Tr}\sigma
-
2\operatorname{Tr}
\left[
(\rho^{1/2}\sigma\rho^{1/2})^{1/2}
\right],
\]

is the natural quantum PG metric.

The PG curvature of a mixed state decomposes schematically as

\[
\mathcal R_Q(\rho)
=
\mathcal R_{\mathrm{FS}}(\rho)
+
\mathcal R_{\mathrm{spec}}(\rho)
+
\mathcal R_{\mathrm{hol}}(\rho),
\]

where the three terms represent expected Fubini–Study curvature, eigenvalue-simplex curvature, and Uhlmann-holonomy curvature.

---

### 8.2 Tidal phase of a delocalized quantum body

Consider a nonrelativistic quantum body of mass \(m\) in a spatial probability distribution \(P\) with covariance \(\Sigma^{ij}\). The gravitational phase accumulated over time \(T\) is

\[
\varphi
=
-\frac{mc^2}{\hbar}\tau.
\]

In the weak-field limit,

\[
d\tau
\approx
\left(
1+\frac{\Phi}{c^2}
\right)dt.
\]

Averaging over \(P\),

\[
\langle\Phi\rangle_P
=
\Phi(b)
+
\frac12\Sigma^{ij}\partial_i\partial_j\Phi(b).
\]

Therefore the covariance-dependent phase shift is

\[
\boxed{
\delta\varphi_{\mathrm{PG}}
=
-\frac{mT}{2\hbar}
\Sigma^{ij}
\partial_i\partial_j\Phi(b).
}
\]

In tensorial language,

\[
\boxed{
\delta\varphi_{\mathrm{PG}}
=
-\frac{mT}{2\hbar}
\Sigma^{ij}E_{ij},
\qquad
E_{ij}=R_{i0j0}.
}
\]

This is a tidal phase shift controlled by the covariance of the quantum state. It is distinct from the usual center-of-mass gravitational phase and vanishes for a pointlike state.

---

### 8.3 Curvature-variance decoherence

The variance of the gravitational potential across the probability cloud is

\[
\operatorname{Var}_P(\Phi)
=
\int \Phi^2\,dP
-
\left(
\int \Phi\,dP
\right)^2.
\]

Expanding to second order,

\[
\operatorname{Var}_P(\Phi)
\approx
\frac12
\Sigma^{ij}\Sigma^{kl}
\partial_i\partial_k\Phi
\partial_j\partial_l\Phi.
\]

Using \(E_{ij}=\partial_i\partial_j\Phi\),

\[
\operatorname{Var}_P(\Phi)
\approx
\frac12
\Sigma^{ij}\Sigma^{kl}
E_{ik}E_{jl}.
\]

The corresponding dephasing rate is therefore

\[
\boxed{
\Gamma_{\mathrm{curv}}
\sim
\frac{m}{\hbar}
\left(
\frac12
\Sigma^{ij}\Sigma^{kl}
E_{ik}E_{jl}
\right)^{1/2}.
}
\]

This predicts environment-free gravitational decoherence scaling with mass, spatial covariance, and tidal curvature.

---

## 9. Transport Curvature as Flat-Space Uncertainty Pressure

Even when the base spacetime is flat, the space \(\mathcal P_2(\mathbb R^n)\) has nonnegative intrinsic curvature. The PG sectional curvature in flat space is

\[
K_{\mathrm{PG}}(U,V)
=
3\frac{G_P(A_UV,A_UV)}{\|U\wedge V\|_G^2}
\ge0.
\]

This has a physical interpretation: probability clouds resist rearrangement. The transport curvature acts as an intrinsic rigidity of uncertain states.

For an isotropic probabilistic fluid, we define the transport pressure by

\[
p_{\mathrm{tr}}
=
\frac{1}{3}\mathcal{Ric}^{\mathrm{tr}}_{ab}u^au^b.
\]

Because \(\mathcal{Ric}^{\mathrm{tr}}\) is built from the nonnegative O’Neill tensor, one expects

\[
p_{\mathrm{tr}}\ge0.
\]

Thus even in Minkowski spacetime, a gas of probabilistic points carries an effective pressure purely from the geometry of probability space. This is a new kind of geometric pressure, distinct from thermal pressure and quantum degeneracy pressure.

A detailed kinetic theory of this transport pressure will be developed elsewhere.

---

## 10. Summary of New Physical Effects

The transition from classical geometry to Probabilistic Geometry produces the following new physics:

| Classical object | PG replacement | New physical effect |
|---|---|---|
| Point event \(x\) | Probability law \(P\) | Event uncertainty becomes primitive |
| Distance \(\rho(x,y)\) | Optimal expected distance \(d(P,Q)\) | Motion of belief states |
| Curvature \(R(x)\) | Expected curvature \(\mathcal R(P)\) | Curvature seen by extended probabilistic bodies |
| Einstein tensor \(G_{ab}\) | Expected Einstein tensor \(\mathfrak G_{ab}\) | Higher-derivative barycentric field equations |
| Stress-energy \(T_{ab}\) | \(T_{ab}+\Theta_{ab}\) | Uncertainty stress-energy |
| Geodesic motion | PG geodesic in \(\mathcal P(M)\) | Covariance-dependent acceleration |
| Point source potential \(-Gm/r\) | Screened/cored potential | Finite cores, scale-dependent \(G\) |
| Pointlike quantum phase | Expected proper-time phase | Tidal covariance phase and decoherence |

The central physical principle is:

\[
\boxed{
\text{Covariance is a gravitational charge.}
}
\]

Equivalently,

\[
\boxed{
\text{Uncertainty is not a perturbation of gravitational physics; it is a source of gravitational physics.}
}
\]

---

## 11. Conclusion

Starting from the axioms of Probabilistic Geometry, we have derived a gravitational theory in which probability laws are the elementary events of spacetime. The distance between events is an optimal expected distance, curvature is an expectation-valued tensor, and the Einstein field equations become barycentric equations containing covariance corrections and transport-curvature contributions.

The most important consequences are:

1. **Modified field equations.**  
   The Einstein tensor is corrected by a covariance operator,
   \[
   G_{ab}\mapsto
   G_{ab}
   -
   \frac12\Sigma^{ij}\nabla_i\nabla_jG_{ab}.
   \]

2. **Uncertainty stress-energy.**  
   The covariance of matter generates an effective stress tensor \(\Theta_{ab}\), required by Bianchi conservation.

3. **Screened gravity and finite cores.**  
   In the Newtonian limit,
   \[
   \nabla^2\Phi-\ell^2\nabla^4\Phi=4\pi G\rho,
   \]
   giving scale-dependent gravity and regularized potentials.

4. **Covariance force.**  
   Probabilistic bodies accelerate according to tidal gradients,
   \[
   a^\mu
   =
   -\frac12\Sigma^{\alpha\beta}P^{\mu\nu}\nabla_\nu E_{\alpha\beta}.
   \]

5. **Cosmological suppression of small-scale structure.**  
   The growth equation acquires
   \[
   G_{\mathrm{eff}}(k)=\frac{G}{1+\ell^2k^2}.
   \]

6. **Quantum tidal phases and decoherence.**  
   Delocalized quantum states acquire covariance-dependent gravitational phases and curvature-variance decoherence.

The resulting theory is not merely a probabilistic reformulation of known physics. It predicts new couplings between geometry and uncertainty. The next tasks are to develop exact Lorentzian causal transport, compute transport-curvature tensors explicitly, couple PGR to quantum field theory, and constrain the length scale \(\ell\) using astrophysical, cosmological, and interferometric data.

The guiding conclusion is:

\[
\boxed{
\text{Geometry under uncertainty is not geometry plus noise; it is gravitational physics itself.}
}
\]

---

## References

1. Ambrosio, L., Gigli, N., & Savaré, G. (2005). *Gradient Flows in Metric Spaces and in the Space of Probability Measures*. Birkhäuser.

2. Karcher, H. (1977). Riemannian center of mass and mollifier smoothing. *Communications on Pure and Applied Mathematics*, 30, 509–541.

3. Lott, J. (2008). Some geometric calculations based on the Wasserstein metric. *Journal of Functional Analysis*, 255, 285–320.

4. McCann, R. J. (1995). Polar factorization of maps on Riemannian manifolds. *Geometric and Functional Analysis*, 5, 589–608.

5. Otto, F. (2001). The geometry of dissipative evolution equations: The porous medium equation. *Communications in Partial Differential Equations*, 26, 101–174.

6. Sturm, K.-T. (2006). On the geometry of metric measure spaces I. *Acta Mathematica*, 196, 65–131.

7. Sturm, K.-T. (2006). On the geometry of metric measure spaces II. *Acta Mathematica*, 196, 133–177.

8. Villani, C. (2003). *Topics in Optimal Transportation*. American Mathematical Society.

9. Villani, C. (2009). *Optimal Transport: Old and New*. Springer.

10. Wald, R. M. (1984). *General Relativity*. University of Chicago Press.

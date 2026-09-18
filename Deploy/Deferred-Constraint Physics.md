# Deferred-Constraint Physics: A Field Theory of Unresolved Structure

**Preprint**  
September 2026

---

## Abstract

This paper develops a physical theory from Deferred-Constraint Mathematics (DCM). The central move is to promote deferred constraint mass from a bookkeeping quantity to a physical degree of freedom. A physical state is no longer represented solely by spacetime points, fields, particles, or density matrices, but by a section of a deferred bundle carrying resolved variables, unresolved constraint variables, and a history-dependent transport structure. The resulting framework, called Deferred-Constraint Physics (DCP), introduces a local balance law for unresolved structure,

\[
\nabla_\mu J_D^\mu = \Gamma - \mathcal R,
\]

where \(J_D^\mu\) is the deferred current, \(\Gamma\) is constraint generation, and \(\mathcal R\) is constraint resolution. From a variational principle, one obtains modified field equations in which gradients of unresolved constraint mass generate physical forces. In the gravitational sector, the Einstein equations acquire a deferred stress-energy tensor. In the point-particle limit, matter experiences an additional resolution force,

\[
m a^\mu = -\lambda P^{\mu\nu}\nabla_\nu \mu,
\]

where \(\mu\) is deferred mass and \(P^{\mu\nu}=g^{\mu\nu}+u^\mu u^\nu\) projects orthogonal to the four-velocity. In quantum theory, constraint resolution appears as a structural jump process; in cosmology, residual deferred structure behaves as an effective dark sector. The theory predicts new phenomena: resolution forces, deferred radiation, constraint-wave propagation, path-dependent resolution phases, modified gravitational potentials, and horizon entropy corrections. The core physical principle is:

\[
\boxed{\text{Unresolved structure is physically active structure.}}
\]

---

## 1. Introduction: Physics Beyond Resolved States

Conventional physics represents systems by resolved variables: positions \(x^\mu\), fields \(\phi^a(x)\), momenta \(p_\mu\), density operators \(\rho\), or quantum states \(|\Psi\rangle\). Incompleteness is usually treated epistemically, through ignorance, coarse-graining, uncertainty, or hidden variables.

Deferred-Constraint Mathematics suggests a different ontology. A state may contain unresolved structural obligations that are not merely unknown values but active constraints awaiting resolution. The primitive DCM object is

\[
\mathfrak D = (X,\mathcal C,\mu,\rho,\sigma),
\]

where \(X\) is a state space, \(\mathcal C\) is a constraint family, \(\mu\) is unresolved constraint mass, \(\rho\) denotes resolution pathways, and \(\sigma\) records history.

The physical hypothesis developed here is:

\[
\boxed{
\text{Physical reality contains unresolved constraint structure that gravitates, propagates, couples, and resolves.}
}
\]

This does not merely reinterpret known physics. It enlarges the state space of physical systems. The ordinary state becomes a projection of a deferred state.

Let \(M\) be spacetime. A conventional field configuration is a section

\[
\phi: M \to \mathcal F,
\]

where \(\mathcal F\) is the field bundle. In Deferred-Constraint Physics, the physical configuration is a section

\[
\mathfrak Z: M \to \mathfrak E_D,
\]

where

\[
\mathfrak E_D \cong \mathcal F \times \mathcal C \times \mathcal H.
\]

Here:

- \(\mathcal F\) is the resolved field bundle,
- \(\mathcal C\) is the constraint bundle,
- \(\mathcal H\) is the history or transport bundle.

The central scalar is the deferred mass density \(\mu(x)\), a nonnegative functional of unresolved constraints.

The fundamental DCM relation

\[
\Delta \mu = \Gamma - \mathcal R
\]

becomes a physical conservation law for unresolved structure.

---

## 2. Deferred Kinematics

Let \(M\) be a \(d\)-dimensional Lorentzian manifold with metric \(g_{\mu\nu}\), signature \((- + \cdots +)\). Let resolved fields be denoted by

\[
\phi^a(x), \qquad a=1,\dots,N_R.
\]

Let constraint coordinates be

\[
c^\alpha(x), \qquad \alpha=1,\dots,N_C.
\]

The local deferred configuration is

\[
z^A(x) = (\phi^a(x),c^\alpha(x)).
\]

The full deferred state also includes a history-dependent transport structure. Locally, this can be represented by a connection

\[
\mathscr A^\alpha{}_{\beta\mu}(x)
\]

on the constraint bundle. This connection transports unresolved constraints along spacetime paths.

The deferred covariant derivative of a constraint vector \(c^\alpha\) is

\[
D_\mu c^\alpha
=
\nabla_\mu c^\alpha
+
\mathscr A^\alpha{}_{\beta\mu} c^\beta.
\]

The corresponding curvature is

\[
\mathscr F^\alpha{}_{\beta\mu\nu}
=
\partial_\mu \mathscr A^\alpha{}_{\beta\nu}
-
\partial_\nu \mathscr A^\alpha{}_{\beta\mu}
+
\mathscr A^\alpha{}_{\gamma\mu}\mathscr A^\gamma{}_{\beta\nu}
-
\mathscr A^\alpha{}_{\gamma\nu}\mathscr A^\gamma{}_{\beta\mu}.
\]

This curvature measures path-dependent transport of unresolved structure.

The deferred mass density is a scalar functional

\[
\mu = \mu(\phi,c,Dc;\sigma),
\]

where \(\sigma\) denotes history. In local field theory, one often uses the first-jet approximation

\[
\mu = \mu(\phi,c,D_\mu c).
\]

A completely resolved physical state satisfies

\[
\mu = 0.
\]

A structurally burdened state satisfies

\[
\mu>0.
\]

The resolved projection is

\[
\pi_D:\mathfrak E_D \to \mathcal F,
\qquad
\pi_D(\phi,c,\sigma)=\phi.
\]

Ordinary physics is the projection

\[
\mu\to 0.
\]

---

## 3. The Local Balance Law of Unresolved Structure

The fundamental DCM equation is

\[
\Delta\mu = \Gamma - \mathcal R.
\]

In continuum form, this becomes a local balance law. Define the deferred current

\[
J_D^\mu = \mu u^\mu + q_D^\mu,
\]

where \(u^\mu\) is the local transport velocity of the medium or field configuration, and \(q_D^\mu\) is a non-advective deferred flux satisfying

\[
u_\mu q_D^\mu=0.
\]

The simplest constitutive law is deferred diffusion,

\[
q_D^\mu = -D_D P^{\mu\nu}\nabla_\nu \mu,
\]

with

\[
P^{\mu\nu}=g^{\mu\nu}+u^\mu u^\nu.
\]

The local balance law is

\[
\boxed{
\nabla_\mu J_D^\mu = \Gamma - \mathcal R.
}
\]

In the rest frame of \(u^\mu\), this becomes

\[
\dot \mu + \theta \mu + \nabla_\mu q_D^\mu = \Gamma - \mathcal R,
\]

where

\[
\dot\mu = u^\mu\nabla_\mu\mu,
\qquad
\theta=\nabla_\mu u^\mu.
\]

If deferred flux is negligible and the background volume is fixed, one obtains

\[
\dot\mu = \Gamma - \mathcal R.
\]

This is the continuous form of the DCM conservation principle.

### Theorem 1: Deferred No-Free Resolution

Let \(\Sigma_t\) be a Cauchy surface and define the total deferred charge

\[
M_D(t) = \int_{\Sigma_t} \mu \, d\Sigma.
\]

Assume no boundary flux. Then

\[
\frac{dM_D}{dt}
=
\int_{\Sigma_t}(\Gamma-\mathcal R)\,d\Sigma.
\]

If the system is closed and \(\Gamma=0\), then

\[
M_D(t_f)-M_D(t_i)
=
-\int_{t_i}^{t_f}dt\int_{\Sigma_t}\mathcal R\,d\Sigma.
\]

Therefore, if \(M_D(t_i)>0\) and \(M_D(t_f)=0\), then

\[
\int_{t_i}^{t_f}dt\int_{\Sigma_t}\mathcal R\,d\Sigma
=
M_D(t_i).
\]

Thus unresolved structure cannot vanish without an explicit resolution process.

**Proof.** Integrate the balance law over a spacetime slab and apply Stokes’ theorem. With vanishing boundary flux, only the source and sink terms remain. \(\square\)

This theorem is the physical version of the DCM Deferred Conservation Principle.

---

## 4. Variational Principle

The dynamics of DCP is generated by a deferred action. The minimal form is

\[
\boxed{
S_D[\phi,c,\mathscr A,g]
=
\int_M d^dx\sqrt{-g}
\left[
\mathcal L_R(\phi,\nabla\phi)
+
\mathcal L_C(c,Dc)
-
\lambda \mu(\phi,c,Dc)
\right].
}
\]

Here \(\lambda\ge 0\) is the deferred-cost coupling. The constraint Lagrangian is taken as

\[
\mathcal L_C
=
\frac12 H_{\alpha\beta}(c)
D_\mu c^\alpha D^\mu c^\beta
-
V(c),
\]

where \(H_{\alpha\beta}\) is a metric on constraint space and \(V(c)\) is a constraint potential.

The total action may include gravity:

\[
S_{\text{tot}}
=
\frac{1}{16\pi G}
\int_M d^dx\sqrt{-g}\,R
+
S_D.
\]

The resolved fields obey

\[
E_R^a(\phi)
=
\lambda
\frac{\delta \mu}{\delta \phi^a},
\]

where

\[
E_R^a(\phi)
=
\frac{1}{\sqrt{-g}}
\frac{\delta S_R}{\delta \phi_a}.
\]

Thus unresolved structure acts as a source for ordinary fields.

The constraint fields obey

\[
\boxed{
\mathcal E_\alpha(c)
-
\lambda
\frac{\delta\mu}{\delta c^\alpha}
=
0,
}
\]

with

\[
\mathcal E_\alpha(c)
=
D_\mu\left(
H_{\alpha\beta}D^\mu c^\beta
\right)
-
\frac12
\partial_\alpha H_{\beta\gamma}
D_\mu c^\beta D^\mu c^\gamma
+
\partial_\alpha V.
\]

If \(\mu\) depends on \(D_\mu c^\alpha\), the Euler–Lagrange equations acquire additional derivative contributions:

\[
\mathcal E_\alpha(c)
-
\lambda
\left(
\frac{\partial\mu}{\partial c^\alpha}
-
D_\mu
\frac{\partial\mu}{\partial(D_\mu c^\alpha)}
\right)
=
0.
\]

The central physical consequence is that the constraint sector is not auxiliary. It backreacts on resolved physics through the term

\[
\lambda \frac{\delta\mu}{\delta\phi^a}.
\]

---

## 5. Deferred Stress-Energy and Modified Gravitation

Varying the action with respect to \(g_{\mu\nu}\) gives

\[
G_{\mu\nu}
=
8\pi G
\left(
T^R_{\mu\nu}
+
T^D_{\mu\nu}
\right),
\]

where \(T^R_{\mu\nu}\) is the ordinary resolved stress-energy tensor and \(T^D_{\mu\nu}\) is the deferred stress-energy tensor.

For the minimal constraint Lagrangian,

\[
\boxed{
T^D_{\mu\nu}
=
H_{\alpha\beta}
\left(
D_\mu c^\alpha D_\nu c^\beta
-
\frac12 g_{\mu\nu}
D_\rho c^\alpha D^\rho c^\beta
\right)
-
g_{\mu\nu}V(c)
-
\lambda g_{\mu\nu}\mu
+
T^{(\mu)}_{\mu\nu}.
}
\]

The term \(T^{(\mu)}_{\mu\nu}\) appears if \(\mu\) depends explicitly on spacetime gradients. In the simplest case where \(\mu=\mu(\phi,c)\), it vanishes.

The deferred contribution has two distinct pieces:

1. **Constraint kinetic and potential energy:**

\[
T^{(C)}_{\mu\nu}
=
H_{\alpha\beta}
D_\mu c^\alpha D_\nu c^\beta
-
\frac12 g_{\mu\nu}
H_{\alpha\beta}
D_\rho c^\alpha D^\rho c^\beta
-
g_{\mu\nu}V(c).
\]

2. **Deferred-mass pressure:**

\[
T^{(\mu)}_{\mu\nu}
=
-\lambda g_{\mu\nu}\mu.
\]

The latter behaves like a negative-pressure contribution when \(\mu\) varies slowly.

Because the total action is diffeomorphism invariant,

\[
\nabla^\mu
\left(
T^R_{\mu\nu}
+
T^D_{\mu\nu}
\right)
=
0.
\]

However, the resolved and deferred sectors need not be separately conserved. In general,

\[
\nabla^\mu T^R_{\mu\nu}=Q_\nu,
\]

\[
\nabla^\mu T^D_{\mu\nu}=-Q_\nu.
\]

The exchange current is

\[
\boxed{
Q_\nu
=
-\lambda
\frac{\delta\mu}{\delta\phi^a}
\nabla_\nu\phi^a
-
\lambda
\frac{\delta\mu}{\delta c^\alpha}
\nabla_\nu c^\alpha
+
\cdots
}
\]

where the ellipsis denotes derivative-coupling contributions. Physically, \(Q_\nu\) is the four-force density by which unresolved structure exchanges energy-momentum with resolved matter.

Thus DCP predicts a new class of gravitational phenomena: geometry sourced not only by energy density, pressure, and momentum flux, but also by unresolved constraint mass.

---

## 6. Point-Particle Limit and the Resolution Force

Consider a point particle with worldline \(x^\mu(\tau)\), four-velocity

\[
u^\mu = \frac{dx^\mu}{d\tau},
\qquad
u^\mu u_\mu = -1,
\]

and an internal deferred variable \(c(\tau)\). The effective mass is

\[
m(c)=m_0+\lambda \mu(c).
\]

The point-particle action is

\[
S_p
=
-\int m(c)\,ds
=
-\int m(c)\sqrt{-g_{\mu\nu}\dot x^\mu\dot x^\nu}\,d\tau.
\]

Varying with respect to \(x^\mu\) gives

\[
\delta S_p
=
-\int
\left[
m(c)\delta(ds)
+
\delta m(c)\,ds
\right].
\]

Using

\[
\delta(ds)
=
-u_\mu \frac{D\delta x^\mu}{d\tau}ds
\]

and integrating by parts yields

\[
m(c)a^\mu
+
P^{\mu\nu}\nabla_\nu m(c)
=
0,
\]

where

\[
a^\mu = u^\nu\nabla_\nu u^\mu
\]

and

\[
P^{\mu\nu}=g^{\mu\nu}+u^\mu u^\nu.
\]

Since

\[
\nabla_\nu m(c)=\lambda \nabla_\nu\mu,
\]

one obtains the resolution-force law:

\[
\boxed{
m(c)a^\mu
=
-\lambda P^{\mu\nu}\nabla_\nu\mu.
}
\]

This is one of the central new physical laws derived from DCM.

A particle may have zero ordinary acceleration in the resolved metric while still undergoing deferred acceleration if

\[
P^{\mu\nu}\nabla_\nu\mu\neq 0.
\]

Conversely, a particle may appear dynamically stationary in ordinary coordinates while its constraint mass evolves nontrivially:

\[
\frac{dx^\mu}{d\tau}=0,
\qquad
\frac{d\mu}{d\tau}\neq 0.
\]

This is the particle-level realization of the DCM principle:

\[
\text{static value}
\not\Rightarrow
\text{static structure}.
\]

---

## 7. A Minimal Empirical Model: Yukawa-Type Deferred Gravity

To obtain concrete predictions, suppose the deferred mass field obeys a massive propagation equation sourced by ordinary matter:

\[
\boxed{
(\Box - m_D^2)\mu = \beta T^R,
}
\]

where

\[
\Box = g^{\mu\nu}\nabla_\mu\nabla_\nu,
\]

\(m_D\) is the inverse deferred length scale,

\[
\ell_D = m_D^{-1},
\]

and \(\beta\) is a coupling constant.

In the weak-field static limit,

\[
(\nabla^2 - m_D^2)\mu = -\beta \rho.
\]

For a point mass \(M\),

\[
\mu(r)
=
\frac{\beta M}{4\pi}
\frac{e^{-r/\ell_D}}{r}.
\]

The resolution acceleration is

\[
\mathbf a_D
=
-\frac{\lambda}{m_0}\nabla\mu.
\]

Thus

\[
\mathbf a_D
=
\frac{\lambda\beta M}{4\pi m_0}
\left(
\frac{1}{r^2}
+
\frac{1}{\ell_D r}
\right)
e^{-r/\ell_D}
\hat{\mathbf r}.
\]

The Newtonian acceleration is

\[
\mathbf a_N
=
-\frac{GM}{r^2}\hat{\mathbf r}.
\]

Define

\[
\alpha_D
=
\frac{\lambda\beta}{4\pi G m_0}.
\]

Then the total radial acceleration is

\[
\boxed{
\mathbf a(r)
=
-\frac{GM}{r^2}
\left[
1
+
\alpha_D
\left(
1+\frac{r}{\ell_D}
\right)
e^{-r/\ell_D}
\right]
\hat{\mathbf r}.
}
\]

This is a Yukawa-type modification of gravity generated not by an ordinary scalar field but by unresolved constraint mass.

If \(\lambda\) is universal, the theory preserves the weak equivalence principle but modifies gravitational attraction. If \(\lambda\) depends on composition, DCP predicts composition-dependent accelerations:

\[
\frac{\Delta a}{a}
\sim
\frac{\Delta\lambda}{m_0}
\frac{\beta}{4\pi G}
\left(
1+\frac{r}{\ell_D}
\right)
e^{-r/\ell_D}.
\]

This provides a clean experimental signature.

---

## 8. Deferred Geodesics in Extended State Space

The DCM deferred metric can be promoted to a physical extended metric. Let

\[
z^A = (x^\mu,c^\alpha).
\]

Define the extended line element

\[
d s_D^2
=
G_{AB} dz^A dz^B,
\]

with

\[
G_{AB}
=
\begin{pmatrix}
g_{\mu\nu} + k_{\mu\alpha}k_\nu{}^\alpha
&
k_{\mu\beta}
\\[2mm]
k_{\alpha\nu}
&
h_{\alpha\beta}
\end{pmatrix}.
\]

Equivalently,

\[
d s_D^2
=
g_{\mu\nu}dx^\mu dx^\nu
+
2k_{\mu\alpha}dx^\mu dc^\alpha
+
h_{\alpha\beta}dc^\alpha dc^\beta.
\]

Here \(h_{\alpha\beta}\) is the metric on constraint space and \(k_{\mu\alpha}\) couples resolved motion to constraint motion.

The extended geodesic equation is

\[
\boxed{
\frac{d^2 z^A}{ds_D^2}
+
\Gamma^A{}_{BC}
\frac{dz^B}{ds_D}
\frac{dz^C}{ds_D}
=
0.
}
\]

Projecting onto spacetime gives

\[
\frac{d^2x^\mu}{ds_D^2}
+
\Gamma^\mu{}_{\rho\sigma}
\frac{dx^\rho}{ds_D}
\frac{dx^\sigma}{ds_D}
=
F_D^\mu,
\]

where

\[
F_D^\mu
=
-
\Gamma^\mu{}_{\rho\alpha}
\frac{dx^\rho}{ds_D}
\frac{dc^\alpha}{ds_D}
-
\Gamma^\mu{}_{\alpha\beta}
\frac{dc^\alpha}{ds_D}
\frac{dc^\beta}{ds_D}
-
\Gamma^\mu{}_{\alpha\rho}
\frac{dc^\alpha}{ds_D}
\frac{dx^\rho}{ds_D}.
\]

Thus an ordinary geodesic in \(M\) may appear curved because the system is moving through constraint space.

If the constraint coordinates relax according to a resolution law,

\[
\frac{dc^\alpha}{ds_D}
=
-\kappa h^{\alpha\beta}\partial_\beta \mu,
\]

then the projected motion contains a force proportional to \(\nabla\mu\). This geometrically derives the resolution force from extended geodesic motion.

The key result is:

\[
\boxed{
\text{Apparent forces may be projections of deferred geodesic motion.}
}
\]

---

## 9. Deferred Curvature, Memory, and Path Dependence

DCM defines resolution operators \(R_i\). In the continuum limit, these become vector fields or differential operators acting on constraint space. Define

\[
R_i = R_i^\alpha(\phi,c)\frac{\partial}{\partial c^\alpha}.
\]

Their commutator is

\[
\boxed{
\mathcal K_{ij}
=
[R_i,R_j].
}
\]

If

\[
[R_i,R_j]=0,
\]

then resolution paths commute. If

\[
[R_i,R_j]\neq 0,
\]

then resolution is path-dependent.

For two small resolution flows of parameters \(\epsilon\) and \(\delta\), one has

\[
\Phi_{R_j}^{-\delta}
\Phi_{R_i}^{-\epsilon}
\Phi_{R_j}^{\delta}
\Phi_{R_i}^{\epsilon}
(z)
=
z
+
\epsilon\delta [R_i,R_j](z)
+
\mathcal O(\epsilon^2,\delta^2).
\]

Therefore the leading path-dependence of resolution is governed by deferred curvature.

In the presence of a history connection \(\mathscr A\), a closed path \(\gamma\) in spacetime or constraint space produces a holonomy

\[
U_D(\gamma)
=
\mathcal P
\exp
\left(
\oint_\gamma \mathscr A
\right).
\]

For a quantum system, this produces a measurable phase,

\[
\boxed{
\Delta\varphi_D
=
q_D
\oint_\gamma \mathscr A.
}
\]

Equivalently, by Stokes’ theorem,

\[
\Delta\varphi_D
=
q_D
\int_\Sigma \mathscr F,
\]

where \(\Sigma\) is a surface bounded by \(\gamma\).

This is a physical memory effect: two processes with identical initial and final resolved states can differ by a deferred phase if their constraint histories enclose nonzero deferred curvature.

The corresponding theorem is:

### Theorem 2: Deferred Path-Independence Theorem

A deferred system is resolution-order independent if and only if its resolution curvature vanishes:

\[
[R_i,R_j]=0
\quad
\forall i,j
\]

if and only if finite resolution sequences are equivalent up to DCM equivalence,

\[
R_{\pi(1)}\cdots R_{\pi(n)}
\sim_D
R_1\cdots R_n
\]

for every permutation \(\pi\).

This theorem translates the DCM curvature principle into physical memory and phase effects.

---

## 10. Quantum Deferred Dynamics

In quantum theory, the Hilbert space is enlarged:

\[
\mathcal H_D
=
\mathcal H_X \otimes \mathcal H_C.
\]

Here \(\mathcal H_X\) is the ordinary physical Hilbert space and \(\mathcal H_C\) is the constraint Hilbert space.

A deferred quantum state is

\[
|\Psi_D\rangle
\in
\mathcal H_D.
\]

Let \(\hat N_C\) be the constraint-number operator. For discrete DCM,

\[
\hat N_C |n\rangle = n|n\rangle,
\]

and

\[
\mu = \mu_0 \langle \hat N_C\rangle.
\]

The deferred Hamiltonian is

\[
\boxed{
\hat H_D
=
\hat H_X\otimes I_C
+
I_X\otimes \hat H_C
+
\hat K_{XC}.
}
\]

The interaction \(\hat K_{XC}\) couples ordinary observables to unresolved structure.

Resolution is represented by jump operators

\[
\hat L_r:
|n\rangle
\mapsto
|n-k_r\rangle,
\qquad
k_r>0.
\]

The master equation is

\[
\boxed{
\frac{d\rho}{dt}
=
-i[\hat H_D,\rho]
+
\sum_r
\gamma_r
\left(
\hat L_r\rho \hat L_r^\dagger
-
\frac12
\{\hat L_r^\dagger\hat L_r,\rho\}
\right)
+
\mathcal G[\rho].
}
\]

Here \(\mathcal G[\rho]\) is a generation superoperator. The expected deferred mass is

\[
\langle \mu\rangle
=
\mu_0\operatorname{Tr}(\rho \hat N_C).
\]

Its evolution satisfies

\[
\boxed{
\frac{d}{dt}\langle \hat N_C\rangle
=
\operatorname{Tr}(\hat N_C\mathcal G[\rho])
-
\sum_r
\gamma_r k_r
\langle \hat L_r^\dagger\hat L_r\rangle.
}
\]

Identifying

\[
\Gamma
=
\operatorname{Tr}(\hat N_C\mathcal G[\rho]),
\]

\[
\mathcal R
=
\sum_r
\gamma_r k_r
\langle \hat L_r^\dagger\hat L_r\rangle,
\]

one obtains

\[
\frac{d}{dt}\langle \mu\rangle
=
\Gamma-\mathcal R.
\]

Thus quantum jumps can be interpreted as resolution events when they reduce constraint number.

### Measurement as Constraint Resolution

A measurement interaction may be written as

\[
|\psi\rangle\otimes |C_0\rangle
\longrightarrow
\sum_i
\alpha_i
|\psi_i\rangle\otimes |C_i\rangle,
\]

where \(|C_i\rangle\) are unresolved measurement constraints. A resolution event acts as

\[
\hat R_i
\left(
|\psi_i\rangle\otimes |C_i\rangle
\right)
=
|\psi_i\rangle\otimes |0_C\rangle.
\]

The Born weight of branch \(i\) is

\[
p_i
=
|\alpha_i|^2.
\]

In DCP, collapse is not primitive randomness alone; it is the discharge of a deferred obligation. The apparent nonunitarity of measurement corresponds to a transition

\[
\mu>0
\quad\longrightarrow\quad
\mu=0
\]

in the constraint sector.

### Deferred Decoherence

If the coupling is

\[
\hat K_{XC}
=
g
\hat A_X\otimes \hat N_C,
\]

then off-diagonal coherences between states with different constraint numbers decay as

\[
\rho_{nn'}(t)
\sim
\rho_{nn'}(0)
\exp
\left[
-\Gamma_{\text{dec}}(n-n')^2 t
\right].
\]

Thus deferred structure induces decoherence even when ordinary energy exchange is negligible.

---

## 11. Deferred Cosmology

Apply DCP to a spatially flat FLRW universe,

\[
ds^2
=
-dt^2
+
a(t)^2 d\mathbf x^2.
\]

Assume homogeneous constraint fields

\[
c^\alpha=c^\alpha(t),
\qquad
\mu=\mu(t).
\]

The deferred energy density is

\[
\boxed{
\rho_D
=
\frac12 H_{\alpha\beta}
\dot c^\alpha \dot c^\beta
+
V(c)
+
\lambda \mu.
}
\]

The deferred pressure is

\[
\boxed{
p_D
=
\frac12 H_{\alpha\beta}
\dot c^\alpha \dot c^\beta
-
V(c)
-
\lambda \mu.
}
\]

The Friedmann equations become

\[
3H^2
=
8\pi G
\left(
\rho_R+\rho_D
\right),
\]

\[
-2\dot H - 3H^2
=
8\pi G
\left(
p_R+p_D
\right).
\]

The deferred equation-of-state parameter is

\[
w_D
=
\frac{p_D}{\rho_D}
=
\frac{
\frac12 H_{\alpha\beta}\dot c^\alpha\dot c^\beta
-
V
-
\lambda\mu
}{
\frac12 H_{\alpha\beta}\dot c^\alpha\dot c^\beta
+
V
+
\lambda\mu
}.
\]

If the kinetic term is small,

\[
\frac12 H_{\alpha\beta}\dot c^\alpha\dot c^\beta
\ll
V+\lambda\mu,
\]

then

\[
w_D\approx -1.
\]

Thus a slowly resolving deferred sector behaves as dark energy.

The balance law gives

\[
\dot\mu + 3H J_D = \Gamma-\mathcal R.
\]

For a homogeneous universe with negligible flux,

\[
\dot\mu = \Gamma-\mathcal R.
\]

If constraint generation has ceased,

\[
\Gamma\approx 0,
\]

then

\[
\dot\mu = -\mathcal R.
\]

The released deferred energy can feed the resolved sector:

\[
\dot\rho_R+3H(\rho_R+p_R)=+\mathcal R_E,
\]

\[
\dot\rho_D+3H(\rho_D+p_D)=-\mathcal R_E,
\]

where \(\mathcal R_E\) is the energy equivalent of resolution.

This yields a physical interpretation of late-time acceleration:

\[
\boxed{
\text{Dark energy may be residual unresolved structure approaching a slow-resolution regime.}
}
\]

Similarly, long-lived persistent constraint modes with

\[
|\lambda_i|\approx 1
\]

in the DCM spectrum can behave as pressureless or nearly pressureless components, providing a structural dark-matter candidate.

---

## 12. Deferred Waves and Radiation

If deferred mass possesses inertia and propagation speed \(v_D\), its continuum dynamics may obey

\[
\boxed{
\frac{\partial^2\mu}{\partial t^2}
+
\gamma_D
\frac{\partial\mu}{\partial t}
=
v_D^2\nabla^2\mu
-
m_D^2\mu
+
S_D.
}
\]

In covariant form,

\[
\boxed{
\Box\mu
+
\gamma_D u^\alpha\nabla_\alpha\mu
+
m_D^2\mu
=
S_D.
}
\]

Plane-wave modes satisfy

\[
\omega^2
+
i\gamma_D\omega
=
v_D^2 k^2
+
m_D^2.
\]

For weak damping,

\[
\omega
\approx
\sqrt{v_D^2k^2+m_D^2}
-
\frac{i\gamma_D}{2}.
\]

Thus DCP predicts a new class of physical waves: constraint waves, or deferred radiation.

If \(m_D=0\), the waves are long-range. If \(m_D\neq 0\), they are short-range with Compton length

\[
\ell_D = m_D^{-1}.
\]

These modes are not ordinary scalar radiation. They are propagating disturbances in unresolved structure.

---

## 13. Deferred Thermodynamics and Horizon Entropy

Define the resolution-pathway entropy

\[
H_D
=
-\sum_i \nu_i\log\nu_i,
\]

where \(\nu_i\) is the probability weight of resolution pathway \(i\). The total generalized entropy is

\[
\boxed{
S_{\text{gen}}
=
S_R
+
H_D
+
\frac{A}{4G}
+
S_{\text{corr}}.
}
\]

Here \(S_R\) is ordinary thermodynamic entropy and \(A/(4G)\) is Bekenstein–Hawking entropy.

DCP predicts an additional horizon contribution

\[
\boxed{
S_D
=
\eta_D
\int_{\mathcal H}
\mu\, dA,
}
\]

where \(\mathcal H\) is a horizon and \(\eta_D\) is a deferred-entropy coefficient.

The generalized second law becomes

\[
\boxed{
\frac{d}{dt}
\left(
S_R
+
H_D
+
\frac{A}{4G}
+
S_D
\right)
\ge 0.
}
\]

For a black hole, the first law is modified to

\[
dM
=
T_H
d
\left(
\frac{A}{4G}
+
S_D
\right)
+
\text{work terms}.
\]

Thus unresolved structure contributes to horizon entropy.

A resolution horizon is defined by

\[
\tau_R(\mathfrak x)
=
\inf
\{
t\ge 0:
\mu(t)=0
\}.
\]

If

\[
\tau_R\to\infty,
\]

the state is permanently deferred. Black-hole horizons may be interpreted geometrically as surfaces beyond which constraint resolution is infinitely delayed for external observers.

---

## 14. Deferred Stability and Singularities

A conventional dynamical system is stable if perturbations in resolved variables remain bounded. DCP introduces deferred stability.

Define the deferred perturbation norm

\[
|\delta\mathfrak x|_D^2
=
|\delta x|^2
+
\alpha_D(\delta\mu)^2.
\]

A system is D-stable if

\[
|\delta\mathfrak x(t)|_D
\le
K e^{\gamma t}
|\delta\mathfrak x(0)|_D,
\qquad
\gamma\le 0.
\]

It is possible that

\[
\delta x(t)
\]

remains bounded while

\[
\delta\mu(t)
\]

grows without bound. Such a system is conventionally stable but deferred-unstable.

A deferred singularity occurs when

\[
x(t)\to x^\ast,
\qquad
\mu(t)\to\infty.
\]

Thus resolved observables remain finite while unresolved structural obligation diverges. This gives a new class of singularities invisible to ordinary variables.

The criterion is

\[
\boxed{
\text{singularity}
\quad
\text{iff}
\quad
\mu\to\infty
\quad
\text{or}
\quad
\tau_R\to\infty.
}
\]

---

## 15. Observable Consequences

The theory becomes physically meaningful only if it yields observables distinguishable from conventional physics. The primary signatures are the following.

### 15.1 Resolution Force

A test body experiences

\[
\mathbf a_D
=
-\frac{\lambda}{m_0}
\nabla\mu.
\]

If \(\mu\) is sourced by matter, this gives a Yukawa correction:

\[
\mathbf a(r)
=
-\frac{GM}{r^2}
\left[
1+
\alpha_D
\left(
1+\frac{r}{\ell_D}
\right)
e^{-r/\ell_D}
\right]
\hat{\mathbf r}.
\]

Experimental targets:

- torsion-balance tests,
- lunar laser ranging,
- planetary ephemerides,
- galaxy rotation curves,
- weak-lensing profiles.

### 15.2 Composition Dependence

If \(\lambda\) is not universal,

\[
\Delta a_{12}
=
-\left(
\frac{\lambda_1}{m_1}
-
\frac{\lambda_2}{m_2}
\right)
\nabla\mu.
\]

This violates the weak equivalence principle.

### 15.3 Constraint Waves

Deferred radiation obeys

\[
\omega^2
+
i\gamma_D\omega
=
v_D^2k^2+m_D^2.
\]

Observable effects include:

- anomalous dispersion,
- damping without ordinary thermal loss,
- polarization-independent excess propagation modes,
- resonant excitation of constraint degrees of freedom.

### 15.4 Quantum Resolution Events

In quantum systems, DCP predicts deviations from purely unitary evolution when constraint mass is nonzero. The master equation contains resolution jumps. Possible signatures:

- non-energy decoherence,
- delayed-choice memory effects,
- path-dependent phases \(\Delta\varphi_D=q_D\oint\mathscr A\),
- statistics of quantum jumps correlated with constraint load.

### 15.5 Cosmological Signatures

The deferred sector modifies the background expansion:

\[
H^2
=
\frac{8\pi G}{3}
(\rho_R+\rho_D).
\]

Observables include:

- effective equation of state \(w_D\neq -1\),
- energy transfer between dark and resolved sectors,
- scale-dependent growth from deferred perturbations,
- modified Integrated Sachs–Wolfe effect,
- altered matter power spectrum.

### 15.6 Horizon Entropy Corrections

Black-hole entropy becomes

\[
S_{\text{BH}}
=
\frac{A}{4G}
+
\eta_D
\int_{\mathcal H}\mu\,dA.
\]

Possible signatures:

- corrections to black-hole thermodynamics,
- modified evaporation rates,
- echoes or memory effects associated with delayed resolution near horizons.

---

## 16. Relation to Known Physics

DCP contains ordinary physics as the zero-deferred sector:

\[
\mu=0,
\qquad
\Gamma=0,
\qquad
\mathcal R=0.
\]

In this limit,

\[
J_D^\mu=0,
\]

\[
T^D_{\mu\nu}=0,
\]

and the usual field equations are recovered.

The theory is not merely a scalar-tensor extension, although it can reduce to one. The essential difference is that the additional degrees of freedom represent unresolved obligations, not ordinary substances. Their dynamics is governed by generation, transport, and resolution rather than solely by Hamiltonian evolution.

DCP also differs from hidden-variable theories. Hidden variables supply missing values. Deferred variables supply missing resolutions.

The distinction is:

\[
\boxed{
\text{hidden variable}
\neq
\text{unresolved constraint}.
}
\]

A hidden variable asks: what is the value?

A deferred constraint asks: what must still be discharged?

---

## 17. Principal Equations of Deferred-Constraint Physics

The theory is organized by the following equations.

### Deferred state

\[
\mathfrak Z=(\phi,c,\mathscr A,\sigma).
\]

### Deferred mass

\[
\mu=\mu(\phi,c,Dc;\sigma)\ge 0.
\]

### Balance law

\[
\nabla_\mu J_D^\mu=\Gamma-\mathcal R.
\]

### Action

\[
S_D
=
\int d^dx\sqrt{-g}
\left[
\mathcal L_R
+
\frac12 H_{\alpha\beta}D_\mu c^\alpha D^\mu c^\beta
-
V(c)
-
\lambda\mu
\right].
\]

### Field equations

\[
E_R^a
=
\lambda
\frac{\delta\mu}{\delta\phi^a},
\]

\[
\mathcal E_\alpha(c)
-
\lambda
\frac{\delta\mu}{\delta c^\alpha}
=
0.
\]

### Gravitational equations

\[
G_{\mu\nu}
=
8\pi G
\left(
T^R_{\mu\nu}
+
T^D_{\mu\nu}
\right).
\]

### Particle force law

\[
m a^\mu
=
-\lambda P^{\mu\nu}\nabla_\nu\mu.
\]

### Quantum balance

\[
\frac{d}{dt}\langle\mu\rangle
=
\Gamma-\mathcal R.
\]

### Curvature and memory

\[
\mathcal K_{ij}=[R_i,R_j],
\]

\[
\Delta\varphi_D
=
q_D
\oint \mathscr A.
\]

### Cosmological effective fluid

\[
\rho_D
=
\frac12 H_{\alpha\beta}\dot c^\alpha\dot c^\beta
+
V+\lambda\mu,
\]

\[
p_D
=
\frac12 H_{\alpha\beta}\dot c^\alpha\dot c^\beta
-
V-\lambda\mu.
\]

These equations define the core of DCP.

---

## 18. Conclusion

Deferred-Constraint Physics promotes unresolved structure from a bookkeeping artifact to a physical entity. The primitive physical state is not merely a value, field configuration, or wavefunction. It is a deferred state carrying resolved content, unresolved constraints, and history.

The central physical consequences are:

1. Unresolved constraint mass obeys a local balance law.
2. Gradients of deferred mass generate real forces.
3. Gravity couples to deferred stress-energy.
4. Quantum measurement can be modeled as constraint resolution.
5. Noncommuting resolution produces physical memory and phase.
6. Cosmological residual deferred structure can mimic dark energy or dark matter.
7. Horizons acquire entropy contributions from unresolved structure.
8. Singularities may be purely deferred, with finite resolved variables but divergent constraint mass.

The governing principle is

\[
\boxed{
\text{Structure that has not yet resolved is still physically active structure.}
}
\]

The decisive next step is to constrain the parameters

\[
\lambda,\quad \beta,\quad m_D,\quad v_D,\quad \gamma_D,\quad \eta_D
\]

through experiment. If resolution forces, constraint waves, deferred phases, or cosmological resolution transfer are detected, the theory becomes an empirical extension of standard physics. If they are excluded across all admissible parameter ranges, the framework remains a powerful formal language for constrained and history-dependent systems, but not a physical theory of nature.

The central equation of the new physics is therefore

\[
\boxed{
\frac{D_D\mathfrak X}{Dt}
=
\mathcal T(\mathfrak X)
+
\mathcal G(\mathfrak X)
-
\mathcal R(\mathfrak X),
}
\]

with the physical conservation law

\[
\boxed{
\nabla_\mu J_D^\mu
=
\Gamma-\mathcal R.
}
\]

From this law, the physics of unresolved structure follows.

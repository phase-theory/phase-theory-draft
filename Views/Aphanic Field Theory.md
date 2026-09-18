# Aphanic Field Theory: Structured Absence as a Physical Interaction

**Preprint**

## Abstract

Aphanics provides a formal mathematics in which absence is not a mere complement of presence but a structured image of presence under an evocation operator. In this paper I derive a physical theory from that mathematics. The central move is to promote the aphanon  
\[
A=(U,P,H,\varepsilon)
\]
to a dynamical field theory on spacetime. Present degrees of freedom are described by fields \(\phi^i(x)\), absent degrees of freedom by fields \(\psi^\alpha(x)\), and the evocation operator becomes an evocation tensor \(E^\alpha{}_i(\phi)\). The resulting theory contains a new geometric object, the aphanic effective metric
\[
\gamma_{ij}=G_{ij}+H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j,
\]
which shows that structured absence modifies inertia, propagation, and gravitational sourcing. I develop the continuum limit of finite aphanons, construct the aphanic action, derive field equations, stress-energy, homological zero modes, quantum propagator corrections, threshold activation dynamics, and cosmological reductions. The theory predicts environment-dependent inertia, aphanic holonomy, absence-mediated forces, topologically protected silent and mute modes, and possible dark-sector behavior arising from latent absence.

---

## 1. Introduction: From Structured Absence to Physical Law

Classical physics, like classical mathematics, is usually organized around presence. Particles are present excitations, fields are present degrees of freedom, and even the vacuum is treated as a background of present operators. Absence appears indirectly: as vacuum, holes, negative charge, missing energy, unoccupied states, or boundary conditions.

Aphanics reverses this order. It begins with the question:

\[
\text{What is absent, and how is that absence structurally generated?}
\]

The primitive operation is not membership but evocation:

\[
\text{Presence}\longrightarrow \text{Evocation}\longrightarrow \text{Structured Absence}.
\]

The purpose of this paper is to convert that formal structure into physics.

I shall use the following physical postulates.

### Postulate P1 — Presence and absence are physical sectors

A physical system possesses present variables \(\phi^i\) and absent variables \(\psi^\alpha\). The distinction is structural, not merely linguistic.

### Postulate P2 — Presence evokes absence

There exists an evocation tensor
\[
E^\alpha{}_i(\phi,\psi)
\]
such that changes in presence generate structured changes in absence.

### Postulate P3 — Evoked absence contributes to dynamics

The absent sector is not inert. It contributes to kinetic terms, stress-energy, and gravitational coupling.

### Postulate P4 — Absence may activate

Under suitable thresholds, latent absence may become manifest presence. This yields nonequilibrium cascade dynamics.

These postulates lead to a new class of field theories, which I call aphanic field theories.

---

## 2. Statistical Mechanics of Finite Aphanons

Before passing to continuum fields, the finite aphanic formalism already yields a statistical mechanics.

Let \(A=(U,P,H,\varepsilon)\) be a finite aphanon. The aphanic polynomial is

\[
\Phi_A(x,y)=\sum_{S\subseteq P}x^{|S|}y^{|\varepsilon(S)|}.
\]

This object is naturally interpreted as a partition function.

### 2.1 Aphanic partition function

Assign an energy cost \(\epsilon_P\) to each present element and an energy cost \(\epsilon_H\) to each evoked absent element. For a present configuration \(S\subseteq P\), define

\[
\mathcal H(S)=\epsilon_P |S|+\epsilon_H|\varepsilon(S)|.
\]

Then the canonical partition function is

\[
Z(\beta)=\sum_{S\subseteq P}e^{-\beta\mathcal H(S)}
=\Phi_A\!\left(e^{-\beta\epsilon_P},e^{-\beta\epsilon_H}\right).
\]

More generally, if present elements carry chemical potential \(\mu_P\), one writes

\[
x=e^{-\beta(\epsilon_P-\mu_P)},
\qquad
y=e^{-\beta\epsilon_H},
\]

so that

\[
Z(x,y)=\Phi_A(x,y).
\]

The multiplicativity theorem for disjoint aphanic sums,

\[
\Phi_{A\oplus B}(x,y)=\Phi_A(x,y)\Phi_B(x,y),
\]

becomes the physical statement that independent aphanic systems have additive free energies:

\[
F_{A\oplus B}=F_A+F_B.
\]

Thus the aphanic polynomial is the generating function of an aphanic thermodynamics.

### 2.2 Observables

Define the present-number operator

\[
N_P(S)=|S|
\]

and the evoked-absence operator

\[
K_A(S)=|\varepsilon(S)|.
\]

Their expectation values in the ensemble \(Z(x,y)\) are

\[
\langle N_P\rangle
=
x\frac{\partial}{\partial x}\ln \Phi_A(x,y),
\]

\[
\langle K_A\rangle
=
y\frac{\partial}{\partial y}\ln \Phi_A(x,y).
\]

The variance of evoked absence is

\[
\operatorname{Var}(K_A)
=
\left(y\frac{\partial}{\partial y}\right)^2
\ln\Phi_A(x,y).
\]

The corresponding aphanic susceptibility is

\[
\chi_H
=
\beta\,\operatorname{Var}(K_A).
\]

This is a fluctuation-dissipation relation for structured absence.

For the uniform ensemble \(x=y=1\), one recovers the expectation identity from the basic theory:

\[
\mathbb E[K_A]
=
2^{-|P|}
\left.
\frac{\partial\Phi_A}{\partial y}
\right|_{(1,1)}
=
\sum_{h\in H}\left(1-2^{-d(h)}\right),
\]

where \(d(h)\) is the contact degree of the absent element \(h\).

Thus the expected amount of evoked absence is a thermodynamic observable.

### 2.3 Aphanic intensity as order parameter

The aphanic intensity

\[
\operatorname{Int}(A)
=
\frac{1}{|H|}
\sum_{h\in H}
\left(1-2^{-d(h)}\right)
\]

is the expected fraction of the absent sector evoked by a uniformly random present configuration.

In a physical ensemble, this becomes an order parameter:

\[
\operatorname{Int}_q(A)
=
\frac{1}{|H|}
\sum_{h\in H}
\left[
1-\prod_{p\in C(h)}(1-q_p)
\right],
\]

where \(q_p\) is the probability that present element \(p\) is active, and

\[
C(h)=\{p\in P:h\in\varepsilon(\{p\})\}.
\]

The uniform case \(q_p=1/2\) gives the original intensity. More generally, \(\operatorname{Int}_q\) measures the fraction of absence activated by a physical probe.

### 2.4 Aphanic entropy

Let \(K_A=|\varepsilon(S)|\). The probability that a random present configuration evokes exactly \(k\) absent elements is

\[
p_k
=
\frac{1}{Z}
\sum_{\substack{S\subseteq P\\|\varepsilon(S)|=k}}
x^{|S|}y^k.
\]

The aphanic entropy

\[
\mathcal H_{\mathrm{aph}}(A)
=
-\sum_{k=0}^{|H|}p_k\log p_k
\]

becomes a thermodynamic entropy of evoked absence. It measures uncertainty not in the present configuration itself, but in the amount of absence generated.

The full sector entropy,

\[
\mathcal H_{\mathrm{sector}}(A)=H(\varepsilon(S)),
\]

measures uncertainty in the actual absent configuration. Since cardinality is a coarse-graining,

\[
\mathcal H_{\mathrm{aph}}(A)
\le
\mathcal H_{\mathrm{sector}}(A).
\]

This is a precise information-theoretic inequality for physical absence.

---

## 3. Continuum Limit: Evocation Kernels and Fields

Finite aphanics becomes physical when the contact relation is replaced by a continuum response kernel.

### 3.1 Linear response from Bernoulli probes

For a finite weighted aphanon, the probability that an absent element \(h\) is evoked under independent present probes \(q_p\) is

\[
\mathbb P(h\in\varepsilon(S))
=
1-
\prod_{p\in C(h)}(1-q_p).
\]

For weak present probabilities \(q_p\ll 1\),

\[
\mathbb P(h\in\varepsilon(S))
\approx
\sum_{p\in C(h)}q_p.
\]

Thus the basic additive aphanon produces a linear-response law.

Passing to a continuum, let \(x\) label present degrees of freedom and \(y\) absent degrees of freedom. Replace \(q_p\) by a present density \(\rho_P(x)\), and replace the contact matrix by an evocation kernel \(K(y,x)\). Then

\[
\rho_H(y)
=
\int K(y,x)\rho_P(x)\,d\mu_P(x).
\]

This is the continuum linear evocation law.

A thresholded version is

\[
\rho_H(y)
=
F_y\!\left(
\int K(y,x)\rho_P(x)\,d\mu_P(x)
\right),
\]

where \(F_y\) is an activation function. The step-function limit gives collective threshold evocation.

### 3.2 Differentiable evocation tensors

Let \(\mathcal P\) be a differentiable present manifold with coordinates \(\phi^i\), and let \(\mathcal H\) be an absent manifold with coordinates \(\psi^\alpha\).

In the integrable case, evocation is generated by a smooth map

\[
\varepsilon:\mathcal P\to\mathcal H,
\]

and the infinitesimal evocation tensor is

\[
E^\alpha{}_i(\phi)
=
\frac{\partial\varepsilon^\alpha}{\partial\phi^i}.
\]

A small present displacement \(d\phi^i\) evokes an absent displacement

\[
d\psi^\alpha_{\mathrm{evoked}}
=
E^\alpha{}_i\,d\phi^i.
\]

In the nonintegrable case, \(E^\alpha{}_i\) is not necessarily the derivative of a global potential. One then defines the evocation curvature

\[
F^\alpha{}_{ij}
=
2\partial_{[i}E^\alpha{}_{j]}.
\]

If \(F^\alpha{}_{ij}\neq0\), evocation is path-dependent.

For a closed curve \(C\) in present space,

\[
\Delta\psi^\alpha
=
\oint_C E^\alpha{}_i\,d\phi^i
=
\int_\Sigma F^\alpha,
\]

by Stokes’ theorem. This is an aphanic holonomy: a closed cycle of presence evokes a net displacement in absence.

This is one of the first genuinely new physical effects arising from Aphanics.

---

## 4. Aphanic Field Theory

Let spacetime be a \(D\)-dimensional Lorentzian manifold \((M,g_{\mu\nu})\), with mostly-plus signature. Let present fields be

\[
\phi^i(x),\qquad i=1,\dots,n,
\]

and absent fields be

\[
\psi^\alpha(x),\qquad \alpha=1,\dots,m.
\]

Let \(G_{ij}(\phi)\) be a positive metric on the present field space and \(H_{\alpha\beta}(\psi)\) a positive metric on the absent field space.

Define the evocation mismatch one-form

\[
\mathcal M^\alpha{}_\mu
=
\nabla_\mu\psi^\alpha
-
E^\alpha{}_i(\phi,\psi)\nabla_\mu\phi^i.
\]

The mismatch measures the failure of the absent field to track the evocation generated by the present field.

### 4.1 Aphanic action

The minimal aphanic action is

\[
S
=
\int_M d^Dx\sqrt{-g}
\left[
\frac{1}{2\kappa}R
+
\mathcal L_{\mathrm{aph}}
+
\mathcal L_{\mathrm{mat}}
\right],
\]

with

\[
\mathcal L_{\mathrm{aph}}
=
-\frac12 G_{ij}(\phi)
\nabla_\mu\phi^i\nabla^\mu\phi^j
-\frac12 H_{\alpha\beta}(\psi)
\nabla_\mu\psi^\alpha\nabla^\mu\psi^\beta
-\frac{1}{2\lambda^2}
H_{\alpha\beta}
\mathcal M^\alpha{}_\mu
\mathcal M^{\beta\mu}
-
V(\phi,\psi).
\]

Here \(\lambda\) is an evocation length. The limit

\[
\lambda\to0
\]

is the stiff-evocation limit, in which the absent field is forced to follow the evocation dictated by presence.

The potential \(V(\phi,\psi)\) governs self-interactions and possible absence-matter coupling.

### 4.2 Stiff evocation and the effective metric

Assume for simplicity that \(E^\alpha{}_i\) is integrable:

\[
E^\alpha{}_i=\partial_i\varepsilon^\alpha.
\]

In the stiff limit \(\lambda\to0\), the mismatch vanishes:

\[
\mathcal M^\alpha{}_\mu=0.
\]

Hence

\[
\nabla_\mu\psi^\alpha
=
E^\alpha{}_i\nabla_\mu\phi^i.
\]

Substituting into the absent kinetic term gives

\[
-\frac12 H_{\alpha\beta}
\nabla_\mu\psi^\alpha\nabla^\mu\psi^\beta
=
-\frac12
H_{\alpha\beta}
E^\alpha{}_iE^\beta{}_j
\nabla_\mu\phi^i\nabla^\mu\phi^j.
\]

Therefore the present field acquires an effective metric

\[
\boxed{
\gamma_{ij}
=
G_{ij}
+
H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j.
}
\]

The effective action becomes

\[
S_{\mathrm{eff}}
=
\int d^Dx\sqrt{-g}
\left[
\frac{1}{2\kappa}R
-\frac12\gamma_{ij}(\phi)
\nabla_\mu\phi^i\nabla^\mu\phi^j
-
V_{\mathrm{eff}}(\phi)
+
\mathcal L_{\mathrm{mat}}
\right],
\]

where

\[
V_{\mathrm{eff}}(\phi)
=
V(\phi,\varepsilon(\phi)).
\]

This is the central physical result.

Structured absence modifies the kinetic geometry of presence.

### 4.3 Interpretation

The term

\[
H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j
\]

is the inertial contribution of evoked absence.

If \(E=0\), absence is mute and does not affect present propagation.

If \(E\) is nonzero but constant, presence propagates as if in a rescaled field-space metric.

If \(E\) varies with \(\phi\), presence experiences additional forces.

Thus absence becomes physically measurable through its effect on present motion.

---

## 5. Field Equations

For clarity, take flat target metrics,

\[
G_{ij}=\delta_{ij},
\qquad
H_{\alpha\beta}=\delta_{\alpha\beta},
\]

and assume \(E^\alpha{}_i=E^\alpha{}_i(\phi)\) is independent of \(\psi\). The general curved-target case adds the usual target-space connection terms.

The mismatch is

\[
\mathcal M^\alpha{}_\mu
=
\partial_\mu\psi^\alpha
-
E^\alpha{}_i\partial_\mu\phi^i.
\]

The flat-spacetime field equations are obtained by varying \(\psi^\alpha\) and \(\phi^i\).

### 5.1 Absence field equation

Variation with respect to \(\psi^\alpha\) gives

\[
\boxed{
\square\psi^\alpha
+
\frac{1}{\lambda^2}
\partial_\mu\mathcal M^{\alpha\mu}
-
\frac{\partial V}{\partial\psi^\alpha}
=0.
}
\]

This is the dynamical equation for the absent sector. The term involving \(\mathcal M\) measures the relaxation of absence toward the evoked configuration.

### 5.2 Presence field equation

Variation with respect to \(\phi^i\) gives

\[
\boxed{
\square\phi^i
-
\frac{1}{\lambda^2}
\partial_\mu
\left(
E^\alpha{}_i\mathcal M^{\alpha\mu}
\right)
+
\frac{1}{\lambda^2}
\left(
\partial_iE^\alpha{}_j
\right)
\mathcal M^{\alpha\mu}
\partial_\mu\phi^j
-
\frac{\partial V}{\partial\phi^i}
=0.
}
\]

The second and third terms are backreaction terms from structured absence. They vanish in the naive absence-free limit \(E=0\), but not in a reduced or strict aphanon.

### 5.3 Stiff-limit equation

In the stiff integrable limit, one should eliminate \(\psi\) rather than set \(\mathcal M=0\) after variation. The resulting equation is

\[
\boxed{
\nabla_\mu
\left(
\gamma_{ij}\nabla^\mu\phi^j
\right)
-
\frac12
\partial_i\gamma_{jk}
\nabla_\mu\phi^j\nabla^\mu\phi^k
-
\partial_iV_{\mathrm{eff}}
=
J_i^{\mathrm{mat}},
}
\]

where \(J_i^{\mathrm{mat}}\) is the force density induced by matter coupling.

Equivalently,

\[
\square_\gamma\phi^i
-
\partial^iV_{\mathrm{eff}}
=
J^i_{\mathrm{mat}},
\]

where \(\square_\gamma\) is the wave operator associated with the effective metric \(\gamma_{ij}\).

Thus absence changes the propagation operator for presence.

---

## 6. Stress-Energy and Gravitational Coupling

The aphanic stress-energy tensor follows from metric variation:

\[
T_{\mu\nu}^{\mathrm{aph}}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta S_{\mathrm{aph}}}{\delta g^{\mu\nu}}.
\]

One obtains

\[
\begin{aligned}
T_{\mu\nu}^{\mathrm{aph}}
={}&
G_{ij}
\nabla_\mu\phi^i\nabla_\nu\phi^j
+
H_{\alpha\beta}
\nabla_\mu\psi^\alpha\nabla_\nu\psi^\beta
\\
&+
\frac{1}{\lambda^2}
H_{\alpha\beta}
\mathcal M^\alpha{}_\mu\mathcal M^\beta{}_\nu
\\
&-
g_{\mu\nu}
\left[
\frac12
G_{ij}
\nabla_\rho\phi^i\nabla^\rho\phi^j
+
\frac12
H_{\alpha\beta}
\nabla_\rho\psi^\alpha\nabla^\rho\psi^\beta
\right.
\\
&\hspace{3.2cm}
\left.
+
\frac{1}{2\lambda^2}
H_{\alpha\beta}
\mathcal M^\alpha{}_\rho\mathcal M^{\beta\rho}
+
V(\phi,\psi)
\right].
\end{aligned}
\]

In the stiff limit,

\[
T_{\mu\nu}^{\mathrm{aph}}
=
\gamma_{ij}
\nabla_\mu\phi^i\nabla_\nu\phi^j
-
g_{\mu\nu}
\left[
\frac12\gamma_{ij}
\nabla_\rho\phi^i\nabla^\rho\phi^j
+
V_{\mathrm{eff}}
\right].
\]

The Einstein equations become

\[
\boxed{
G_{\mu\nu}
=
\kappa
\left(
T_{\mu\nu}^{\mathrm{mat}}
+
T_{\mu\nu}^{\mathrm{aph}}
\right).
}
\]

Therefore structured absence gravitates.

This gives a natural mechanism by which an apparently absent sector can contribute to gravitational dynamics without appearing as ordinary present matter.

---

## 7. Particle Mechanics and the Aphanic Force

Consider a localized present excitation whose internal state follows a trajectory \(\phi^i(\tau)\). Its worldline action is

\[
S_{\mathrm{particle}}
=
-m\int d\tau
\sqrt{
\gamma_{ij}(\phi)
\dot\phi^i\dot\phi^j
}.
\]

Variation gives the geodesic equation

\[
\ddot\phi^k
+
\Gamma^k_{ij}(\gamma)
\dot\phi^i\dot\phi^j
=0.
\]

If the bare present metric \(G_{ij}\) is flat, the deviation from inertial motion is determined by

\[
h_{ij}
=
H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j,
\]

so that

\[
\gamma_{ij}=G_{ij}+h_{ij}.
\]

The aphanic contribution to the Christoffel symbols is

\[
C^k{}_{ij}
=
\frac12 G^{k\ell}
\left(
\nabla_i h_{j\ell}
+
\nabla_j h_{i\ell}
-
\nabla_\ell h_{ij}
\right),
\]

where \(\nabla\) is the connection of \(G\).

The physical acceleration relative to the bare present geometry is

\[
\boxed{
a^k_{\mathrm{aph}}
=
-
C^k{}_{ij}
\dot\phi^i\dot\phi^j.
}
\]

This is the aphanic force.

It is not produced by a conventional potential. It is produced by the geometry of evoked absence.

### 7.1 Constant evocation

If \(E^\alpha{}_i\) is constant, then \(h_{ij}\) is constant and

\[
C^k{}_{ij}=0.
\]

There is no aphanic force, but the inertial metric is rescaled:

\[
\gamma_{ij}=G_{ij}+H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j.
\]

Thus constant evocation renormalizes inertia.

### 7.2 Spatially varying evocation

If \(E^\alpha{}_i\) depends on \(\phi\), then

\[
\partial_k h_{ij}
=
H_{\alpha\beta}
\left[
(\partial_kE^\alpha{}_i)E^\beta{}_j
+
E^\alpha{}_i(\partial_kE^\beta{}_j)
\right],
\]

and a nonzero aphanic force appears.

Thus gradients of evocation generate forces.

### 7.3 Aphanic holonomy

If the evocation tensor is nonintegrable,

\[
F^\alpha{}_{ij}
=
2\partial_{[i}E^\alpha{}_{j]}
\neq0,
\]

then a closed loop \(C\) in present configuration space evokes a net absent displacement

\[
\Delta\psi^\alpha
=
\oint_C E^\alpha{}_i\,d\phi^i
=
\int_\Sigma F^\alpha.
\]

In a quantum theory, such holonomies produce phase shifts analogous to Aharonov-Bohm phases, but here the phase is produced by structured absence.

---

## 8. Homological Zero Modes and Topological Protection

The finite aphanic homology constructed from the incidence operator

\[
\partial_A:\mathbb Z^P\to\mathbb Z^H
\]

has direct physical meaning.

Let \(M_{\alpha i}\) be the contact matrix,

\[
M_{\alpha i}
=
\begin{cases}
1,&h_\alpha\in\varepsilon(\{p_i\}),\\
0,&\text{otherwise}.
\end{cases}
\]

In a linearized theory, \(M\) becomes the infinitesimal evocation operator.

The aphanic homology groups are

\[
H_1^{\mathrm{aph}}(A)=\ker M,
\]

\[
H_0^{\mathrm{aph}}(A)=\operatorname{coker}M.
\]

Thus:

- \(\ker M\) describes silent presences: present perturbations that evoke no absence.
- \(\operatorname{coker}M\) describes mute absences: absent directions not reachable by present evocation.

These become physical zero modes.

### 8.1 Aphanic Dirac operator

Define the aphanic Dirac operator

\[
\mathsf D_A
=
\begin{pmatrix}
0 & M^\dagger\\
M & 0
\end{pmatrix}.
\]

It acts on the doubled space

\[
\mathbb R^P\oplus\mathbb R^H.
\]

Its square is

\[
\mathsf D_A^2
=
\begin{pmatrix}
M^\dagger M & 0\\
0 & MM^\dagger
\end{pmatrix}.
\]

The zero modes satisfy

\[
M\phi=0,
\qquad
M^\dagger\psi=0.
\]

Therefore

\[
\dim\ker\mathsf D_A
=
\dim\ker M+\dim\ker M^\dagger.
\]

But

\[
\dim\ker M=\beta_1^{\mathrm{aph}},
\]

and

\[
\dim\ker M^\dagger=\beta_0^{\mathrm{aph}}.
\]

Hence

\[
\boxed{
\dim\ker\mathsf D_A
=
\beta_1^{\mathrm{aph}}+\beta_0^{\mathrm{aph}}.
}
\]

The chiral index is

\[
\operatorname{ind}\mathsf D_A
=
\beta_1^{\mathrm{aph}}-\beta_0^{\mathrm{aph}}
=
|P|-|H|
=
-\chi_{\mathrm{aph}}(A).
\]

Thus the aphanic Euler characteristic becomes an index.

### 8.2 Physical meaning

The zero modes are topologically protected:

- Silent present modes cannot be lifted by perturbations that preserve the evocation class.
- Mute absent modes cannot be generated by any present perturbation.

In a quantum field theory, these become protected massless modes or superselection sectors.

If the incidence matrix is taken over \(\mathbb Z\), torsion in

\[
H_0^{\mathrm{aph}}(A)
\]

produces discrete absence charges. These are not captured by real-valued linearization and represent genuinely topological physical sectors.

---

## 9. Quantum Aphanic Fields and Propagator Mixing

Consider a quadratic theory around a background where \(E^\alpha{}_i\) is constant. For simplicity take

\[
G_{ij}=\delta_{ij},
\qquad
H_{\alpha\beta}=\delta_{\alpha\beta},
\]

and ignore potentials. The Euclidean quadratic action is

\[
S_E^{(2)}
=
\frac12\int_p
\left[
p^2\phi_i\phi_i
+
p^2\psi_\alpha\psi_\alpha
+
\frac{1}{\lambda^2}
p^2
(\psi_\alpha-E_{\alpha i}\phi_i)^2
\right].
\]

In momentum space, the inverse propagator matrix is

\[
\mathcal K(p)
=
\begin{pmatrix}
p^2\delta_{ij}
+
\lambda^{-2}p^2 E^\mathrm{T}_{i\alpha}E_{\alpha j}
&
-\lambda^{-2}p^2E^\mathrm{T}_{j\beta}
\\[4pt]
-\lambda^{-2}p^2E_{\alpha i}
&
p^2\delta_{\alpha\beta}
+
\lambda^{-2}p^2\delta_{\alpha\beta}
\end{pmatrix}.
\]

Integrating out the absent field gives an effective present inverse propagator equal to the Schur complement:

\[
K^{\mathrm{eff}}_{ij}(p)
=
p^2\delta_{ij}
+
\lambda^{-2}p^2E^\mathrm{T}_{i\alpha}E_{\alpha j}
-
\lambda^{-4}p^4
E^\mathrm{T}_{i\alpha}
\left[
p^2(1+\lambda^{-2})\delta_{\alpha\beta}
\right]^{-1}
E_{\beta j}.
\]

This simplifies to

\[
\boxed{
K^{\mathrm{eff}}_{ij}(p)
=
p^2
\left[
\delta_{ij}
+
\frac{\lambda^{-2}}{1+\lambda^{-2}}
E^\mathrm{T}_{i\alpha}E_{\alpha j}
\right].
}
\]

In the stiff-evocation limit \(\lambda\to0\),

\[
\frac{\lambda^{-2}}{1+\lambda^{-2}}\to1,
\]

and therefore

\[
K^{\mathrm{eff}}_{ij}(p)
=
p^2
\left[
\delta_{ij}
+
E^\mathrm{T}_{i\alpha}E_{\alpha j}
\right].
\]

Thus the quantum propagator confirms the classical result:

\[
\gamma_{ij}
=
\delta_{ij}
+
E^\mathrm{T}_{i\alpha}E_{\alpha j}.
\]

For finite \(\lambda\), absence only partially dresses presence. The dressing coefficient

\[
\frac{\lambda^{-2}}{1+\lambda^{-2}}
\]

interpolates between weak evocation and stiff evocation.

If the absent field has a mass \(\mu\), the denominator becomes \(p^2+\mu^2+\lambda^{-2}p^2\), and the effective inertia becomes scale-dependent. This yields running inertial renormalization controlled by the absence mass and evocation stiffness.

---

## 10. Threshold Aphanics and Nonequilibrium Activation

The basic additive theory evokes absence by single contact. Threshold aphanics generalizes this to collective evocation.

For an absent element \(h\), define

\[
d_S(h)=|\{p\in S:h\in\varepsilon(\{p\})\}|.
\]

Let \(\tau(h)\) be an activation threshold. Then

\[
h\in\varepsilon_\tau(S)
\iff
d_S(h)\ge\tau(h).
\]

This distinguishes evocation by contact from evocation by coherence.

### 10.1 Probabilistic threshold activation

If each present element is independently active with probability \(q\), then for an absent element of degree \(d\),

\[
\mathbb P_\tau(h)
=
\sum_{k=\tau}^{d}
\binom{d}{k}
q^k(1-q)^{d-k}.
\]

For \(\tau=1\), this reduces to

\[
\mathbb P_1(h)=1-(1-q)^d.
\]

For \(\tau>1\), activation is nonlinear and cooperative.

### 10.2 Continuum activation dynamics

Let \(a(y,t)\) be the activation density of absent modes at absent coordinate \(y\). Let \(\rho_P(x,t)\) be the present density. A continuum activation equation is

\[
\partial_t a(y,t)
=
-\Gamma a(y,t)
+
\Gamma
\sigma
\left(
\int K(y,x)\rho_P(x,t)\,dx
-
\tau(y)
\right),
\]

where \(\sigma\) is a smooth activation function and \(\Gamma\) is a relaxation rate.

Fixed points satisfy

\[
a(y)
=
\sigma
\left(
\int K(y,x)\rho_P(x)\,dx
-
\tau(y)
\right).
\]

Linearizing around a fixed point gives

\[
\delta a
=
\Gamma\sigma' K*\delta\rho_P
-
\Gamma\delta a.
\]

Cascade instability occurs when the spectral radius of the linear operator

\[
\mathcal T=\Gamma\sigma' K
\]

exceeds unity.

Thus aphanic systems can undergo absence activation phase transitions.

### 10.3 Monotone activation

For finite \(U\), the activation operator

\[
\mathcal A_\tau(P)
=
P
\cup
\{h\in U\setminus P:d_P(h)\ge\tau(h)\}
\]

is monotone:

\[
P\subseteq\mathcal A_\tau(P).
\]

Therefore the sequence

\[
P_0\subseteq P_1\subseteq P_2\subseteq\cdots
\]

stabilizes. The same monotonicity gives fixed-point theorems in continuum settings under suitable compactness assumptions.

Physically, latent absence can become manifest presence through cumulative evocation.

---

## 11. Cosmological Reduction

Assume a spatially homogeneous cosmological background. Let \(\phi^i=\phi^i(t)\), and suppose stiff evocation has eliminated \(\psi^\alpha\). The effective aphanic energy density and pressure are

\[
\rho_{\mathrm{aph}}
=
\frac12\gamma_{ij}(\phi)\dot\phi^i\dot\phi^j
+
V_{\mathrm{eff}}(\phi),
\]

\[
p_{\mathrm{aph}}
=
\frac12\gamma_{ij}(\phi)\dot\phi^i\dot\phi^j
-
V_{\mathrm{eff}}(\phi).
\]

The equation-of-state parameter is

\[
w_{\mathrm{aph}}
=
\frac{p_{\mathrm{aph}}}{\rho_{\mathrm{aph}}}
=
\frac{
\frac12\gamma_{ij}\dot\phi^i\dot\phi^j
-
V_{\mathrm{eff}}
}{
\frac12\gamma_{ij}\dot\phi^i\dot\phi^j
+
V_{\mathrm{eff}}
}.
\]

If the effective potential dominates,

\[
V_{\mathrm{eff}}\gg
\frac12\gamma_{ij}\dot\phi^i\dot\phi^j,
\]

then

\[
w_{\mathrm{aph}}\approx -1.
\]

Thus a slowly varying absence potential behaves like a dark-energy component.

If the evoked kinetic term dominates,

\[
\frac12\gamma_{ij}\dot\phi^i\dot\phi^j
\gg
V_{\mathrm{eff}},
\]

then

\[
w_{\mathrm{aph}}\approx +1,
\]

a stiff absence fluid.

Intermediate regimes yield evolving equation-of-state parameters. Threshold activation can induce sudden transitions between latent and manifest absence, producing cosmological phase transitions.

---

## 12. Physical Consequences and Potential Signatures

The theory predicts several qualitative effects.

### 12.1 Environment-dependent inertia

Because

\[
\gamma_{ij}=G_{ij}+H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j,
\]

the effective inertia of present excitations depends on the local evocation tensor. If \(E^\alpha{}_i\) depends on environmental fields, masses or propagation speeds become environment-dependent.

### 12.2 Aphanic forces

Gradients of \(E^\alpha{}_i\) produce forces:

\[
a^k_{\mathrm{aph}}
=
-
C^k{}_{ij}
\dot\phi^i\dot\phi^j.
\]

These are not ordinary potential forces. They arise from the geometry of evoked absence.

### 12.3 Aphanic holonomy and memory

If

\[
F^\alpha{}_{ij}\neq0,
\]

then closed cycles in present configuration space produce net evoked absence:

\[
\Delta\psi^\alpha
=
\oint_C E^\alpha{}_i d\phi^i.
\]

This yields path-dependent memory effects.

### 12.4 Silent and mute modes

The homological Betti numbers count protected modes:

\[
\beta_1^{\mathrm{aph}}=\dim H_1^{\mathrm{aph}},
\qquad
\beta_0^{\mathrm{aph}}=\dim H_0^{\mathrm{aph}}.
\]

Silent modes are present perturbations that do not evoke absence.

Mute modes are absent perturbations that cannot be reached by presence.

These may appear as hidden sectors, missing-energy channels, or protected zero modes.

### 12.5 Absence-driven dark-sector behavior

The stress-energy of the absent sector gravitates. In cosmology, a dominated evoked absence potential can mimic dark energy, while spatial gradients and kinetic terms can contribute effective dark-sector clustering.

### 12.6 Threshold cascades

Thresholded evocation predicts nonlinear activation cascades:

\[
\text{latent absence}
\to
\text{evocation}
\to
\text{threshold crossing}
\to
\text{manifest presence}.
\]

Such dynamics could model avalanche phenomena, phase transitions, or sudden vacuum reconfiguration.

---

## 13. Conclusion

Aphanics provides more than a formal mathematics of absence. When its structures are dynamized, they generate a new physical framework.

The essential derivation is as follows.

1. Finite aphanons give a partition function through the aphanic polynomial.
2. Bernoulli probes give probabilistic evocation laws.
3. The continuum limit produces evocation kernels and tensors.
4. Differentiable evocation defines an aphanic geometry.
5. Stiff evocation modifies the effective metric of present fields:
   \[
   \gamma_{ij}=G_{ij}+H_{\alpha\beta}E^\alpha{}_iE^\beta{}_j.
   \]
6. The absent sector contributes stress-energy and gravitates.
7. Homology groups classify protected silent and mute modes.
8. Threshold evocation produces nonlinear activation and phase transitions.

The resulting principle is:

\[
\boxed{
\text{Structured absence is not physically inert.}
}
\]

It modifies inertia, sources gravity, carries entropy, supports topology, and can dynamically become manifest presence.

Thus the central claim of Aphanics becomes a physical law:

\[
\boxed{
\text{What is absent can exert structured physical influence.}
}
\]

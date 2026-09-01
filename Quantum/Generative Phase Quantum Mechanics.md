# Generative Phase Quantum Mechanics  
## A Real Geometric Derivation of Quantum Theory from Generative Phase Number Theory and Its Relativistic Foundation  

**White paper / preprint — 2026**  

**Keywords:** Generative Phase Number Theory, phase number, real quantum mechanics, Schrödinger wave function, \(SO(2)\), circle group, relativistic quantum mechanics, Klein–Gordon phase field, Dirac phaseor, gauge connection, spacetime geometry  

**MSC 2020:** 81P99, 81Q05, 81R20, 81R25, 83A05, 53C05, 70H05  

---

## Abstract

This paper develops a formulation of quantum mechanics in which **Generative Phase Number Theory** (GPNT) is the foundational mathematical substrate. The theory is constructed without the use of imaginary numbers. The phase number is not treated as a complex scalar. It is treated as a real geometric object: an oriented rotation in a real two-dimensional phase plane, equivalently an element of the circle group represented by \(SO(2)\).

The Schrödinger wave function is reformulated as a real two-component section of an oriented Euclidean phase bundle. Its norm gives probability density. Its direction in the phase plane gives the physical phase number. The dynamical law is written as a real phase-rotation equation,
\[
\hbar \frac{\partial \Psi}{\partial t}
+
\mathsf Q \widehat H \Psi
=
0,
\]
where \(\mathsf Q\) is the real quarter-turn generator of the phase plane and \(\widehat H\) is a real self-adjoint Hamiltonian operator.

The missing relativistic foundation is supplied by lifting the phase bundle to a Lorentzian spacetime manifold. Quantum mechanics is derived from relativistic phase transport over generative histories. The Klein–Gordon phase field, the Dirac phaseor, electromagnetic gauge structure, spin connection, and gravitational coupling all arise as geometric consequences of the same phase-number substrate. The ordinary nonrelativistic Schrödinger equation is recovered as the low-velocity limit of relativistic generative phase dynamics.

The central result is:

\[
\boxed{
\text{Quantum mechanics is the geometry of generative phase rotations.}
}
\]

Equivalently,

\[
\boxed{
\text{Wave function}
=
\text{real phase vector},
\qquad
\text{quantum dynamics}
=
\text{phase transport},
\qquad
\text{relativity}
=
\text{spacetime geometry of phase}.
}
\]

No imaginary number is used. The formalism is entirely real, tensorial, and geometric.

---

## 1. Introduction

Ordinary quantum mechanics is usually formulated using complex amplitudes. The wave function is taken to be complex-valued, and the dynamical equation contains a scalar imaginary unit. This works computationally, but it creates conceptual obscurity. The imaginary unit is often treated as fundamental, while the physical meaning of phase is left secondary.

Generative Phase Number Theory provides a different starting point. In GPNT, a number or state is not merely a value. It is a generative structure equipped with a phase number. A phase number is a global circular object. A phase angle is only a local coordinate on that object.

The present paper develops this principle into a complete physical foundation:

\[
\boxed{
\text{Physical states are generative phase objects.}
}
\]

The purpose is threefold.

1. **Derive quantum mechanics from phase geometry.**  
   Quantum amplitudes are replaced by real phase-vector resultants over generative histories.

2. **Reformulate the Schrödinger wave function without imaginary numbers.**  
   The wave function becomes a real two-component phase field.

3. **Supply the missing relativistic foundation.**  
   Quantum mechanics is embedded in Lorentzian spacetime geometry. The nonrelativistic Schrödinger equation is obtained as a limit of a relativistic phase equation.

The resulting framework is not a decorative replacement of one notation by another. The primitive object is not a scalar extension of the real numbers. The primitive object is a real oriented phase plane and the group of rotations acting on it.

---

## 2. Phase Numbers Without Imaginary Numbers

### 2.1 The circle group as real rotations

Let the phase group be the real rotation group of an oriented Euclidean plane,
\[
\mathbb T \equiv SO(2).
\]

An element of \(SO(2)\) is a real \(2\times 2\) matrix
\[
R(\theta)
=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}.
\]

The group law is
\[
R(\alpha)R(\beta)=R(\alpha+\beta).
\]

A phase number is an element
\[
u\in SO(2).
\]

A phase vector is a unit vector in the oriented phase plane. Choosing the reference vector
\[
e_1=
\begin{pmatrix}
1\\
0
\end{pmatrix},
\]
a phase vector may be written as
\[
u e_1
=
\begin{pmatrix}
\cos\theta\\
\sin\theta
\end{pmatrix}.
\]

The angle \(\theta\) is a local coordinate. The phase number is the rotation itself.

### 2.2 The quarter-turn generator

Define the real quarter-turn operator
\[
\mathsf Q
=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}.
\]

It acts on a phase vector by rotating it through one quarter of a full turn. Its square is the half-turn,
\[
\mathsf Q^2
=
-
\mathsf I,
\]
where \(\mathsf I\) is the \(2\times2\) identity. This is not an imaginary scalar. It is a real rotation by \(\pi\).

Every phase rotation may be written as
\[
R(\theta)
=
\cos\theta\,\mathsf I
+
\sin\theta\,\mathsf Q.
\]

Thus the entire phase calculus can be expressed using real matrices, real vectors, and trigonometric functions.

### 2.3 Relative phase

Given two phase vectors
\[
u=\begin{pmatrix}\cos\alpha\\ \sin\alpha\end{pmatrix},
\qquad
v=\begin{pmatrix}\cos\beta\\ \sin\beta\end{pmatrix},
\]
their relative phase rotation is
\[
R_{\mathrm{rel}}
=
R(\beta)^{-1}R(\alpha)
=
R(\alpha-\beta).
\]

The scalar interference product is the Euclidean inner product,
\[
u\cdot v
=
\cos(\alpha-\beta).
\]

Thus relative phase is expressed without invoking imaginary quantities.

---

## 3. Generative Phase Substrate

### 3.1 Generative states

In Generative Number Theory, a number is replaced by a generative state
\[
\mathfrak n=(n,\Gamma_n),
\]
where \(n\) is the numerical projection and \(\Gamma_n\) is a generative structure: a network of admissible histories, transformations, ancestors, and descendants.

In the physical theory, configurations of a system are similarly generative states. A configuration is not merely a point in space. It carries a generative structure encoding how it may arise and how it may evolve.

Let \(\mathcal C\) denote the generative configuration space.

### 3.2 Generative histories and phase transport

A generative history is a directed pathway
\[
\gamma:\mathfrak x_i\to\mathfrak x_f
\]
in \(\mathcal C\). To each history is assigned an action functional
\[
S[\gamma]\in\mathbb R.
\]

The phase number associated with that history is the rotation
\[
U_\gamma
=
R\!\left(\frac{S[\gamma]}{\hbar}\right)
\in SO(2).
\]

The constant \(\hbar\) is the quantum of action-phase. It converts action into phase angle.

### 3.3 Resultant phase principle

The physical phase state at a final generative configuration is the vector resultant of all contributing generative histories:
\[
\Psi(\mathfrak x_f)
=
\sum_{\gamma:\mathfrak x_i\to\mathfrak x_f}
w_\gamma
U_\gamma
\Psi(\mathfrak x_i),
\]
where \(w_\gamma\) is a real weight determined by the generative measure.

This is the generative replacement for a complex amplitude sum. The sum is an ordinary sum of real two-component phase vectors.

In the continuum limit, the sum becomes a functional integral over generative paths:
\[
\Psi(x_f,t_f)
=
\int_{\mathcal P(x_i,t_i;x_f,t_f)}
\mathcal D\gamma\,
\mu[\gamma]\,
R\!\left(\frac{S[\gamma]}{\hbar}\right)
\Psi(x_i,t_i).
\]

No imaginary number appears. Interference arises because phase vectors add geometrically in a real plane.

---

## 4. Axioms of Generative Phase Quantum Mechanics

The theory is defined by the following axioms.

### Axiom I — Generative histories are primary

Physical propagation occurs along generative histories. A state at a final configuration is obtained by summing phase transports over admissible histories.

### Axiom II — Phase numbers are real rotations

A phase number is an element of \(SO(2)\), represented as a real rotation of an oriented phase plane.

### Axiom III — The state is a real phase vector

A quantum state is a section of a real oriented rank-two phase bundle. Locally it is a vector
\[
\Psi=
\begin{pmatrix}
\Psi^1\\
\Psi^2
\end{pmatrix}
\in\mathbb R^2.
\]

### Axiom IV — Probability is squared phase-vector norm

The probability density is
\[
\rho
=
\|\Psi\|^2
=
(\Psi^1)^2+(\Psi^2)^2.
\]

### Axiom V — Dynamics is phase transport

Time evolution is a continuous phase rotation generated by a real self-adjoint Hamiltonian.

### Axiom VI — Relativistic covariance is fundamental

The phase bundle is defined over Lorentzian spacetime. Nonrelativistic quantum mechanics is a limiting case.

### Axiom VII — Gauge fields are phase connections

Local changes of phase frame are compensated by an \(SO(2)\) connection. Electromagnetism is the curvature of this connection.

---

## 5. The Real Phase Bundle and the Reformulated Wave Function

### 5.1 Phase bundle

Let \(M\) be a spacetime or spacelike configuration manifold. Over \(M\) define a real oriented rank-two vector bundle
\[
\pi:E\to M.
\]

Each fiber \(E_x\) is a real Euclidean plane with metric
\[
h_{AB}=\delta_{AB},
\qquad
A,B=1,2.
\]

The bundle is equipped with a fiberwise quarter-turn tensor
\[
\mathsf Q^A{}_{B}
=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}.
\]

It satisfies
\[
\mathsf Q^A{}_{C}\mathsf Q^C{}_{B}
=
-\delta^A{}_B.
\]

This tensor is geometric. It is not a scalar imaginary unit.

### 5.2 The wave function as a phase section

The Schrödinger wave function is reformulated as a real section
\[
\Psi:M\to E,
\]
with components
\[
\Psi^A(x),
\qquad
A=1,2.
\]

The probability density is
\[
\rho(x)
=
h_{AB}\Psi^A(x)\Psi^B(x).
\]

If \(\rho>0\), the local phase number is the unique rotation \(U_\Psi(x)\in SO(2)\) such that
\[
\Psi(x)
=
\sqrt{\rho(x)}\,U_\Psi(x)e_1.
\]

Thus the wave function contains two real fields:

1. a magnitude \(\sqrt{\rho}\),
2. a phase number \(U_\Psi\in SO(2)\).

The phase angle is only a local coordinate on \(U_\Psi\).

### 5.3 Local phase rotations

A local change of phase frame is a map
\[
\chi:M\to\mathbb R/(2\pi\mathbb Z),
\]
acting by
\[
\Psi(x)\mapsto \Psi'(x)=R(\chi(x))\Psi(x).
\]

Physical predictions depend only on phase-invariant quantities such as \(\rho\), relative phase rotations, and holonomies.

---

## 6. Derivation of the Schrödinger Equation

### 6.1 Infinitesimal generative propagation

Let the state at time \(t\) be \(\Psi(t)\). For a small time step \(\varepsilon\), generative phase propagation gives
\[
\Psi(t+\varepsilon)
=
K_\varepsilon \Psi(t),
\]
where \(K_\varepsilon\) is a phase-preserving propagator.

Because phase propagation preserves the fiber metric, \(K_\varepsilon\) must be an orthogonal operator. Because it is generated by phase rotations, its infinitesimal generator must lie in the Lie algebra of \(SO(2)\). The Lie algebra is generated by \(\mathsf Q\).

Therefore, to first order,
\[
K_\varepsilon
=
\mathsf I
-
\frac{\varepsilon}{\hbar}
\mathsf Q\widehat H
+
O(\varepsilon^2),
\]
where \(\widehat H\) is a real self-adjoint operator representing energy.

Thus
\[
\Psi(t+\varepsilon)-\Psi(t)
=
-
\frac{\varepsilon}{\hbar}
\mathsf Q\widehat H\Psi(t)
+
O(\varepsilon^2).
\]

Taking the limit \(\varepsilon\to0\) yields the generative phase Schrödinger equation:

\[
\boxed{
\hbar\frac{\partial\Psi}{\partial t}
+
\mathsf Q\widehat H\Psi
=
0.
}
\]

This is the real, geometric reformulation of the Schrödinger equation.

### 6.2 Hamiltonian for a scalar nonrelativistic particle

For a particle of mass \(m\) in a scalar potential \(V(x)\), Galilean invariance and the classical energy relation
\[
E=\frac{p^2}{2m}+V
\]
require the Hamiltonian operator
\[
\widehat H
=
-\frac{\hbar^2}{2m}\Delta + V(x).
\]

Therefore the Schrödinger wave function obeys

\[
\boxed{
\hbar\frac{\partial\Psi}{\partial t}
+
\mathsf Q
\left(
-\frac{\hbar^2}{2m}\Delta + V
\right)
\Psi
=
0.
}
\]

This is the central nonrelativistic equation of the theory.

### 6.3 Component form

Write
\[
\Psi=
\begin{pmatrix}
\Psi^1\\
\Psi^2
\end{pmatrix}.
\]

Since
\[
\mathsf Q
\begin{pmatrix}
a\\
b
\end{pmatrix}
=
\begin{pmatrix}
-b\\
a
\end{pmatrix},
\]
the equation becomes
\[
\hbar\frac{\partial\Psi^1}{\partial t}
=
\widehat H\Psi^2,
\]
\[
\hbar\frac{\partial\Psi^2}{\partial t}
=
-\widehat H\Psi^1.
\]

These are two coupled real field equations. Together they encode the full quantum dynamics.

---

## 7. Probability Conservation

### 7.1 Continuity equation

Define
\[
\rho
=
(\Psi^1)^2+(\Psi^2)^2.
\]

Using the component equations,
\[
\frac{\partial\rho}{\partial t}
=
2\Psi^1\frac{\partial\Psi^1}{\partial t}
+
2\Psi^2\frac{\partial\Psi^2}{\partial t}.
\]

Substitution gives
\[
\frac{\partial\rho}{\partial t}
=
\frac{2}{\hbar}
\left(
\Psi^1\widehat H\Psi^2
-
\Psi^2\widehat H\Psi^1
\right).
\]

The potential terms cancel because \(V\) is multiplicative and symmetric. Only the Laplacian contributes:
\[
\frac{\partial\rho}{\partial t}
=
-\frac{\hbar}{m}
\left(
\Psi^1\Delta\Psi^2
-
\Psi^2\Delta\Psi^1
\right).
\]

Define the probability current
\[
\mathbf j
=
\frac{\hbar}{m}
\left(
\Psi^1\nabla\Psi^2
-
\Psi^2\nabla\Psi^1
\right).
\]

Then
\[
\nabla\cdot\mathbf j
=
\frac{\hbar}{m}
\left(
\Psi^1\Delta\Psi^2
-
\Psi^2\Delta\Psi^1
\right).
\]

Therefore
\[
\boxed{
\frac{\partial\rho}{\partial t}
+
\nabla\cdot\mathbf j
=
0.
}
\]

Probability conservation is a direct consequence of phase-rotation dynamics.

---

## 8. Observables and Expectation Values

### 8.1 Real inner product

The phase Hilbert space is a real Hilbert space of square-integrable phase sections. The inner product is
\[
\langle \Phi,\Psi\rangle
=
\int_M
h_{AB}\Phi^A\Psi^B\,d\mu.
\]

### 8.2 Momentum operator

The generator of spatial translations is the real phase-momentum operator
\[
\widehat{\mathbf p}
=
-\hbar\,\mathsf Q\nabla.
\]

Its expectation value is
\[
\langle \mathbf p\rangle
=
\int
\Psi^T(-\hbar\mathsf Q\nabla)\Psi\,d^3x.
\]

In components,
\[
\langle \mathbf p\rangle
=
\hbar\int
\left(
\Psi^1\nabla\Psi^2
-
\Psi^2\nabla\Psi^1
\right)d^3x.
\]

Thus
\[
\langle \mathbf p\rangle
=
m\int \mathbf j\,d^3x.
\]

### 8.3 General observables

A physical observable is represented by a real self-adjoint operator \(\widehat A\) acting on phase sections, compatible with the phase structure. Its expectation value in a normalized state is
\[
\langle A\rangle
=
\int
\Psi^T\widehat A\Psi\,d^3x.
\]

Observables involving phase rotation explicitly may contain \(\mathsf Q\). The quarter-turn is part of the geometric operator algebra.

---

## 9. Interference Without Imaginary Numbers

Let two generative alternatives produce phase vectors \(\Psi_a\) and \(\Psi_b\). The resultant state is
\[
\Psi
=
\Psi_a+\Psi_b.
\]

The probability density is
\[
\rho
=
\|\Psi_a+\Psi_b\|^2.
\]

Expanding,
\[
\rho
=
\|\Psi_a\|^2
+
\|\Psi_b\|^2
+
2\Psi_a\cdot\Psi_b.
\]

If the two alternatives have phase directions separated by \(\Delta\theta\), then
\[
\Psi_a\cdot\Psi_b
=
\sqrt{\rho_a\rho_b}\cos\Delta\theta.
\]

Therefore
\[
\boxed{
\rho
=
\rho_a+\rho_b
+
2\sqrt{\rho_a\rho_b}\cos\Delta\theta.
}
\]

Interference is thus ordinary Euclidean vector addition in the phase plane.

---

## 10. Gauge Fields as Generative Phase Connections

### 10.1 Local phase covariance

Because the phase frame may be chosen locally, the derivative of \(\Psi\) must be replaced by a covariant derivative. Let
\[
D_\mu\Psi
=
\partial_\mu\Psi
+
\Omega_\mu\Psi,
\]
where \(\Omega_\mu\) is an \(SO(2)\) connection.

For an abelian phase connection,
\[
\Omega_\mu
=
\frac{q}{\hbar}A_\mu\,\mathsf Q,
\]
where \(A_\mu\) is a real gauge potential and \(q\) is the charge coupling.

### 10.2 Gauge transformation

Under a local phase rotation
\[
\Psi\mapsto R(\chi)\Psi,
\]
the connection must transform so that
\[
D_\mu\Psi\mapsto R(\chi)D_\mu\Psi.
\]

This requires
\[
\Omega_\mu
\mapsto
\Omega_\mu
-
(\partial_\mu\chi)\mathsf Q.
\]

Equivalently,
\[
A_\mu
\mapsto
A_\mu
-
\frac{\hbar}{q}\partial_\mu\chi.
\]

### 10.3 Electromagnetic curvature

The curvature of the phase connection is
\[
\mathcal F_{\mu\nu}
=
\partial_\mu\Omega_\nu
-
\partial_\nu\Omega_\mu.
\]

Since \(SO(2)\) is abelian, there is no commutator term. Thus
\[
\mathcal F_{\mu\nu}
=
\frac{q}{\hbar}
F_{\mu\nu}\mathsf Q,
\]
where
\[
F_{\mu\nu}
=
\partial_\mu A_\nu
-
\partial_\nu A_\mu.
\]

The electromagnetic field is therefore the curvature of the generative phase connection.

### 10.4 Gauge-coupled Schrödinger equation

The gauge-covariant nonrelativistic equation is
\[
\boxed{
\hbar\frac{\partial\Psi}{\partial t}
+
\mathsf Q
\left[
\frac{1}{2m}
\left(
-\hbar\mathsf Q\nabla
-
q\mathbf A
\right)^2
+
q\varphi
\right]
\Psi
=
0.
}
\]

Here \(\varphi\) is the electric scalar potential and \(\mathbf A\) is the magnetic vector potential.

This equation is entirely real.

---

## 11. Relativistic Foundation of the Universe

The nonrelativistic theory is not fundamental. The fundamental setting is a Lorentzian spacetime manifold
\[
(M,g),
\]
with metric
\[
g_{\mu\nu}
\]
and signature
\[
(+,-,-,-).
\]

Coordinates are
\[
x^\mu=(ct,\mathbf x).
\]

The invariant interval is
\[
ds^2
=
g_{\mu\nu}dx^\mu dx^\nu.
\]

The phase bundle is now a bundle over spacetime:
\[
E\to M.
\]

The universe’s relativistic foundation is therefore the pair
\[
(M,g,E),
\]
a Lorentzian spacetime equipped with a generative phase bundle.

---

## 12. Relativistic Generative Phase Action

For a free relativistic particle of mass \(m\), the action is
\[
S[\gamma]
=
-mc\int_\gamma ds.
\]

For a charged particle coupled to a gauge potential \(A_\mu\),
\[
S[\gamma]
=
-mc\int_\gamma ds
+
q\int_\gamma A_\mu dx^\mu.
\]

The phase number associated with the history is
\[
U_\gamma
=
R\!\left(\frac{S[\gamma]}{\hbar}\right).
\]

The rest energy produces a universal internal phase rotation frequency
\[
\omega_c
=
\frac{mc^2}{\hbar}.
\]

This is the relativistic phase clock of the particle.

---

## 13. Klein–Gordon Phase Field

### 13.1 Real phase doublet

The simplest relativistic phase field is a real phase doublet
\[
\Phi:M\to\mathbb R^2.
\]

It is a section of the phase bundle. Its dynamics is obtained from a Lorentz-invariant phase-action density.

### 13.2 Lagrangian density

Let
\[
\mu=\frac{mc}{\hbar}.
\]

The free Klein–Gordon phase Lagrangian is
\[
\mathcal L
=
\frac12
g^{\mu\nu}
(D_\mu\Phi)^T(D_\nu\Phi)
-
\frac12
\mu^2
\Phi^T\Phi.
\]

For the free field,
\[
D_\mu\Phi=\partial_\mu\Phi.
\]

### 13.3 Field equation

Variation with respect to \(\Phi\) gives
\[
\boxed{
D_\mu D^\mu\Phi
+
\mu^2\Phi
=
0.
}
\]

In flat spacetime without gauge coupling,
\[
\left(
\frac{1}{c^2}\frac{\partial^2}{\partial t^2}
-
\Delta
+
\frac{m^2c^2}{\hbar^2}
\right)
\Phi
=
0.
\]

This is a pair of real Klein–Gordon equations coupled only by phase symmetry.

### 13.4 Phase current

The global \(SO(2)\) phase symmetry yields a conserved Noether current. Define
\[
J^\mu
=
\Phi^T\mathsf Q D^\mu\Phi.
\]

The field equation implies
\[
D_\mu J^\mu=0.
\]

After appropriate normalization, the time component gives probability density in the nonrelativistic limit.

---

## 14. Nonrelativistic Limit: Derivation of the Schrödinger Equation

### 14.1 Rest-phase extraction

Let
\[
\omega_c=\frac{mc^2}{\hbar}.
\]

Write the relativistic phase field as a rapidly rotating rest phase times a slowly varying phase field:
\[
\Phi(t,\mathbf x)
=
R(-\omega_c t)\psi(t,\mathbf x).
\]

Here \(\psi\) varies slowly compared with \(\omega_c\).

### 14.2 Time derivatives

Since
\[
\frac{d}{dt}R(-\omega_c t)
=
-\omega_c\mathsf Q R(-\omega_c t),
\]
we have
\[
\partial_t\Phi
=
R(-\omega_c t)
\left(
\partial_t\psi
-
\omega_c\mathsf Q\psi
\right),
\]
and
\[
\partial_t^2\Phi
=
R(-\omega_c t)
\left(
\partial_t^2\psi
-
2\omega_c\mathsf Q\partial_t\psi
-
\omega_c^2\psi
\right).
\]

### 14.3 Substitution into the Klein–Gordon equation

The free Klein–Gordon equation is
\[
\left(
\frac{1}{c^2}\partial_t^2
-
\Delta
+
\frac{m^2c^2}{\hbar^2}
\right)
\Phi
=
0.
\]

Substituting the ansatz and canceling the common rotation gives
\[
\frac{1}{c^2}
\left(
\partial_t^2\psi
-
2\omega_c\mathsf Q\partial_t\psi
-
\omega_c^2\psi
\right)
-
\Delta\psi
+
\frac{m^2c^2}{\hbar^2}\psi
=
0.
\]

Since
\[
\frac{\omega_c^2}{c^2}
=
\frac{m^2c^2}{\hbar^2},
\]
the rest-mass terms cancel:
\[
\frac{1}{c^2}\partial_t^2\psi
-
\frac{2\omega_c}{c^2}\mathsf Q\partial_t\psi
-
\Delta\psi
=
0.
\]

In the nonrelativistic limit, the second time derivative term is negligible compared with the first time derivative term. Therefore,
\[
-
\frac{2\omega_c}{c^2}\mathsf Q\partial_t\psi
-
\Delta\psi
=
0.
\]

Using
\[
\frac{2\omega_c}{c^2}
=
\frac{2m}{\hbar},
\]
we obtain
\[
\mathsf Q\partial_t\psi
=
-\frac{\hbar}{2m}\Delta\psi.
\]

Multiplying by \(-\mathsf Q\) gives
\[
\partial_t\psi
=
\frac{\hbar}{2m}\mathsf Q\Delta\psi.
\]

Equivalently,
\[
\hbar\partial_t\psi
+
\mathsf Q
\left(
-\frac{\hbar^2}{2m}\Delta
\right)
\psi
=
0.
\]

Adding a scalar potential \(V\) gives
\[
\boxed{
\hbar\partial_t\psi
+
\mathsf Q
\left(
-\frac{\hbar^2}{2m}\Delta+V
\right)
\psi
=
0.
}
\]

Thus the Schrödinger equation is the nonrelativistic limit of relativistic generative phase dynamics.

---

## 15. Dirac Phaseors: Relativistic Spin Without Imaginary Numbers

### 15.1 Spin and the relativistic phase bundle

A complete geometric implementation must include spin. Spin is not an internal scalar phase. It is the action of the Lorentz group’s double cover on a spinor bundle.

Let \(S\to M\) be a real spinor bundle associated with
\[
\mathrm{Spin}(1,3)
\]
or the appropriate real Clifford representation. A charged spin phaseor is a real doublet
\[
\Psi=
\begin{pmatrix}
\psi_1\\
\psi_2
\end{pmatrix},
\]
where \(\psi_1\) and \(\psi_2\) are real spinor fields. The quarter-turn \(\mathsf Q\) rotates the doublet and provides the electromagnetic phase structure.

### 15.2 Real gamma matrices

Choose real gamma matrices satisfying the Clifford relation
\[
\{\Gamma^\mu,\Gamma^\nu\}
=
2g^{\mu\nu}\mathsf I.
\]

In signatures where a strictly real matrix representation is not globally available, one may equivalently use the real Clifford algebra itself or a pair of real Majorana-type spinors organized as an \(SO(2)\) doublet. The physical theory remains real because the phase rotation is represented by \(\mathsf Q\), not by a scalar imaginary unit.

### 15.3 Spin connection

Let \(e^a{}_\mu\) be a tetrad field, with Latin indices \(a,b\) denoting local Lorentz frames. The spin connection is
\[
\omega_\mu{}^{ab}.
\]

The Lorentz generators in the spin representation are
\[
\Sigma_{ab}.
\]

The full covariant derivative acting on a Dirac phaseor is
\[
D_\mu\Psi
=
\partial_\mu\Psi
+
\frac14\omega_\mu{}^{ab}\Sigma_{ab}\Psi
+
\frac{q}{\hbar}A_\mu\mathsf Q\Psi.
\]

### 15.4 Dirac phase equation

The relativistic first-order phase equation is

\[
\boxed{
\hbar c\,\Gamma^\mu D_\mu\Psi
+
mc^2\Psi
=
0.
}
\]

This is the Dirac equation reformulated as a real phaseor equation. It is Lorentz covariant, gauge covariant, and free of scalar imaginary numbers.

Squaring this operator yields the Klein–Gordon phase equation with spin-curvature corrections, as expected.

### 15.5 Pauli limit

In the nonrelativistic limit, the Dirac phaseor reduces to a two-component spin phaseor. The resulting equation contains the Pauli magnetic coupling:
\[
\hbar\frac{\partial\psi}{\partial t}
+
\mathsf Q
\left[
\frac{1}{2m}
\left(
-\hbar\mathsf Q\nabla-q\mathbf A
\right)^2
+
q\varphi
-
\frac{q\hbar}{2m}\mathbf B\cdot\mathbf S
\right]
\psi
=
0,
\]
where \(\mathbf S\) denotes the real spin generators.

Thus spin-magnetic coupling arises geometrically from the relativistic phase connection.

---

## 16. Gravity and the Geometry of the Universe

### 16.1 Phase fields on curved spacetime

In curved spacetime, the phase bundle is coupled to the metric through tetrads and spin connections. For scalar phase fields, the covariant Klein–Gordon equation is
\[
\left(
D_\mu D^\mu
+
\frac{m^2c^2}{\hbar^2}
\right)
\Phi
=
0.
\]

For spin phaseors,
\[
\hbar c\,\Gamma^\mu D_\mu\Psi
+
mc^2\Psi
=
0.
\]

Gravity enters through \(g_{\mu\nu}\), \(e^a{}_\mu\), and \(\omega_\mu{}^{ab}\).

### 16.2 Phase holonomy and gravitational time dilation

A particle at rest along a worldline accumulates rest phase
\[
\theta
=
\frac{mc^2}{\hbar}\int d\tau,
\]
where \(d\tau\) is proper time.

The phase number is
\[
R(\theta).
\]

Gravitational time dilation is therefore a difference in phase accumulation between worldlines. The gravitational field changes the geometry of phase transport.

### 16.3 Stress-energy and Einstein coupling

The matter Lagrangian for phase fields defines a stress-energy tensor
\[
T_{\mu\nu}
=
-\frac{2}{\sqrt{|g|}}
\frac{\delta S_{\mathrm{matter}}}{\delta g^{\mu\nu}}.
\]

For the Klein–Gordon phase doublet, a symmetric stress-energy tensor is obtained from
\[
\mathcal L
=
\frac12
g^{\mu\nu}
(D_\mu\Phi)^T(D_\nu\Phi)
-
\frac12
\mu^2\Phi^T\Phi.
\]

Schematically,
\[
T_{\mu\nu}
=
(D_\mu\Phi)^T(D_\nu\Phi)
-
\frac12 g_{\mu\nu}
\left[
g^{\alpha\beta}(D_\alpha\Phi)^T(D_\beta\Phi)
-
\mu^2\Phi^T\Phi
\right].
\]

The spacetime geometry then satisfies Einstein’s equation,
\[
G_{\mu\nu}
=
\frac{8\pi G}{c^4}T_{\mu\nu},
\]
possibly with semiclassical expectation values when quantum matter is treated statistically.

Thus the relativistic foundation of the universe is not added after quantum mechanics. It is part of the primitive geometric structure.

---

## 17. Classical Limit

### 17.1 Stationary phase over generative histories

The resultant phase vector is
\[
\Psi
=
\int\mathcal D\gamma\,
\mu[\gamma]\,
R\!\left(\frac{S[\gamma]}{\hbar}\right).
\]

In the limit where the action is large compared with \(\hbar\), neighboring histories produce rapidly varying phase rotations. Their vector resultants cancel except near histories for which
\[
\delta S=0.
\]

These are the classical trajectories.

Thus classical mechanics emerges from stationary generative phase.

### 17.2 Ehrenfest behavior

For the real Schrödinger equation,
\[
\hbar\partial_t\Psi+\mathsf Q\widehat H\Psi=0,
\]
the expectation values obey the usual correspondence laws. For position,
\[
\frac{d}{dt}\langle \mathbf x\rangle
=
\frac{1}{m}\langle \mathbf p\rangle,
\]
and
\[
\frac{d}{dt}\langle \mathbf p\rangle
=
-\langle \nabla V\rangle.
\]

Therefore,
\[
m\frac{d^2}{dt^2}\langle \mathbf x\rangle
=
-\langle \nabla V\rangle.
\]

The classical limit is recovered without imaginary numbers.

---

## 18. Measurement and the Born Rule

In this framework, the Born rule is not introduced as a mysterious complex modulus. It is the squared length of a real phase vector.

For a normalized state,
\[
\int_M \rho\,d\mu=1,
\]
the probability that a measurement finds the system in a region \(U\subset M\) is
\[
P(U)
=
\int_U
h_{AB}\Psi^A\Psi^B\,d\mu.
\]

If a measurement corresponds to an orthogonal decomposition of the phase Hilbert space,
\[
\mathcal H
=
\bigoplus_k \mathcal H_k,
\]
with orthogonal projectors \(P_k\), the probability of outcome \(k\) is
\[
p_k
=
\|P_k\Psi\|^2.
\]

Measurement is therefore a geometric projection in real phase space.

---

## 19. Conceptual Consequences

### 19.1 The wave function is real

The wave function is not a complex scalar. It is a real phase vector field.

### 19.2 Phase is rotation, not imaginary multiplication

The phase number is an \(SO(2)\) rotation. The quarter-turn \(\mathsf Q\) is a real geometric operator.

### 19.3 Interference is vector addition

Quantum interference is the Euclidean addition of phase vectors. Relative phase is the rotation separating two phase directions.

### 19.4 Relativity is not optional

Quantum mechanics is not fundamentally nonrelativistic. Its natural home is a Lorentzian spacetime phase bundle. The Schrödinger equation is a low-velocity limit.

### 19.5 Gauge fields are phase geometry

Electromagnetism is the curvature of the local phase connection. Charge is coupling to phase rotation.

### 19.6 Gravity is phase geometry over curved spacetime

Proper time controls rest-phase accumulation. Curvature affects phase holonomy. The universe’s relativistic structure is built into the substrate.

---

## 20. Summary of Core Equations

### Phase group

\[
R(\theta)
=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}.
\]

### Quarter-turn

\[
\mathsf Q
=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}.
\]

### Real wave function

\[
\Psi=
\begin{pmatrix}
\Psi^1\\
\Psi^2
\end{pmatrix}.
\]

### Probability density

\[
\rho
=
(\Psi^1)^2+(\Psi^2)^2.
\]

### Probability current

\[
\mathbf j
=
\frac{\hbar}{m}
\left(
\Psi^1\nabla\Psi^2
-
\Psi^2\nabla\Psi^1
\right).
\]

### Real Schrödinger equation

\[
\boxed{
\hbar\frac{\partial\Psi}{\partial t}
+
\mathsf Q\widehat H\Psi
=
0.
}
\]

### Free nonrelativistic Hamiltonian

\[
\widehat H
=
-\frac{\hbar^2}{2m}\Delta+V.
\]

### Gauge-covariant Schrödinger equation

\[
\boxed{
\hbar\frac{\partial\Psi}{\partial t}
+
\mathsf Q
\left[
\frac{1}{2m}
\left(
-\hbar\mathsf Q\nabla-q\mathbf A
\right)^2
+
q\varphi
\right]
\Psi
=
0.
}
\]

### Klein–Gordon phase field

\[
\boxed{
D_\mu D^\mu\Phi
+
\frac{m^2c^2}{\hbar^2}\Phi
=
0.
}
\]

### Dirac phaseor equation

\[
\boxed{
\hbar c\,\Gamma^\mu D_\mu\Psi
+
mc^2\Psi
=
0.
}
\]

---

## 21. Conclusion

This paper has formulated quantum mechanics as a real geometric theory derived from Generative Phase Number Theory. The phase number is not an imaginary scalar. It is a rotation in a real oriented phase plane. The Schrödinger wave function is not a complex-valued amplitude. It is a real two-component phase section. Quantum dynamics is phase transport generated by a real Hamiltonian and the quarter-turn operator.

The missing relativistic foundation is supplied by placing the phase bundle over Lorentzian spacetime. Relativistic phase transport yields the Klein–Gordon phase field and the Dirac phaseor. The ordinary Schrödinger equation appears as the nonrelativistic limit of a deeper relativistic phase geometry. Electromagnetism arises as phase connection curvature. Gravity enters through spacetime geometry and proper-time phase accumulation.

The resulting framework may be summarized by three principles:

\[
\boxed{
\text{Phase is rotation.}
}
\]

\[
\boxed{
\text{Quantum mechanics is phase geometry.}
}
\]

\[
\boxed{
\text{Relativity is the spacetime structure of phase.}
}
\]

The deepest reformulation of the wave function is therefore:

\[
\boxed{
\Psi
=
\sqrt{\rho}\,U,
\qquad
U\in SO(2),
}
\]

where \(\rho\) is probability density and \(U\) is a real phase number.

Quantum mechanics, in this substrate, is not fundamentally a theory of imaginary amplitudes. It is a theory of generative phase rotations over the geometry of the universe.

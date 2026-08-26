# Deriving the Schrödinger Wave Function from Phase Numbers

## A phase-first construction of position amplitudes, free-particle dynamics, gauge coupling, and quantum flow without a primitive imaginary scalar

**Author:** Marlon Hanks  
**Affiliation:** Independent Researcher, Dust LLC  
**Document type:** Mathematical physics white paper / preprint  
**Date:** 26 August 2026  
**Keywords:** Schrödinger wave function, phase numbers, complex structure, real Hilbert space, Galilei covariance, Born density, quantum Hamilton–Jacobi equation, gauge holonomy  
**MSC 2020:** 81P05, 81Q05, 81Q10, 81Q70, 46C15

---

## Abstract

This paper derives the form of the nonrelativistic Schrödinger wave function and its evolution equation from a phase-number formulation of quantum kinematics. The primitive scalar structure is not an imaginary number but an orthogonal quarter-turn operator \(J\) on a real Hilbert space, satisfying \(J^2=-I\) and \(J^*=-J\). The real algebra \(\mathbb C_J=\{aI+bJ:a,b\in\mathbb R\}\) is thereby obtained, and its unit-norm elements \(\operatorname{Ph}_J(\theta)=e^{\theta J}\) are **phase numbers**. A wave function is then a position amplitude valued in \(\mathbb C_J\), with pointwise factorization \(\psi=\sqrt\rho\,u\), where \(\rho\) is the Born density and \(u\) is a phase-number field.

The derivation proceeds by explicit structural postulates. A phase-valued inner product gives the Born transition law and demonstrates why the wave function requires two real quadratures. Continuous reversible dynamics that preserve both the real metric and the phase structure have generator \(-JH/\hbar\), with \(H\) self-adjoint; this yields the general Schrödinger equation \(J\hbar\partial_t\psi=H\psi\). Translation covariance, locality, parity, isotropy, and Galilei covariance then select the free-particle Hamiltonian \(H_0=P^2/(2m)\), where \(P=-J\hbar\nabla\). The resulting position-space wave equation is

\[
J\hbar\partial_t\psi(x,t)
=-\frac{\hbar^2}{2m}\nabla^2\psi(x,t)+V(x,t)\psi(x,t).
\]

Minimal coupling extends the construction to electromagnetic fields. The polar phase-number decomposition yields the continuity equation and the quantum Hamilton–Jacobi equation, while nodes reveal the topological distinction between a globally defined phase number and a locally chosen action angle. Plane waves, packets, stationary states, and the two-real-quadrature form are derived explicitly. The final equivalence theorem proves that the phase-number construction is an exact representation of standard complex Schrödinger wave mechanics, with the analytical advantage that phase is treated globally as a compact-group-valued object rather than as an angle or a primitive notation.

> **Central claim.** The Schrödinger wave function is a density amplitude endowed with an intrinsic phase-number field. The operator \(J\) is the quarter-turn that generates its phase evolution; conventional complex notation is a faithful coordinate representation of that structure.

---

## 1. Scope, derivational standard, and physical postulates

The Schrödinger wave function is often written as a complex scalar \(\psi(x,t)\), and the time-dependent Schrödinger equation is correspondingly written with the scalar \(i\). This standard notation is efficient, but it combines several distinct ideas into one symbol: a two-dimensional real amplitude plane, its orientation, the compact group of unit phase factors, and a chosen local real angle. The purpose of this paper is to separate those structures and to derive the wave function in a language in which unit phase factors are primary.

The word *derive* is used in a precise structural sense. The present analysis does not infer empirical quantum mechanics from group topology alone. It begins with explicit quantum-kinematic and symmetry postulates, then proves the form of the wave function and its free-particle dynamics. This is the appropriate standard for a mathematical reconstruction: assumptions are stated openly; the consequences are developed without importing a primitive imaginary scalar. Schrödinger’s wave-mechanics program supplied the original differential equation and its stationary-state interpretation; the phase-number construction reorganizes the same nonrelativistic theory around intrinsic phase geometry.[1]

The physical postulates are collected below.

| Postulate | Mathematical statement | Physical role |
| --- | --- | --- |
| P1: amplitude geometry | \((\mathcal H_\mathbb R,g,J)\), with \(J^2=-I\), \(J^*=-J\) | Two real quadratures with a distinguished phase rotation |
| P2: ray equivalence | \(\psi\sim u\psi\), \(u\in\mathsf P_J\) | Global phase is unobservable for an isolated pure state |
| P3: position measurement | A position PVM resolves \(\mathcal H\) into a configuration amplitude \(\psi(x)\) | Defines the wave-function representation |
| P4: Born rule | \(\rho(x)=N_J(\psi(x))\) | Probability density in configuration space |
| P5: reversible evolution | \(U_t\) is strongly continuous, metric preserving, and commutes with \(J\) | Fixes the general Schrödinger form |
| P6: free-particle symmetry | Translations, rotations, parity, locality, and Galilei boosts | Selects \(H_0=P^2/(2m)\) |

The framework is compatible with the standard projective Hilbert-space formulation of quantum theory. Physical pure states are rays, and probability-preserving symmetries lift to linear or antilinear Hilbert-space isometries.[2] The analysis below focuses on the phase-linear, continuously connected branch relevant to ordinary time evolution.

---

## 2. Phase numbers and the scalar structure of a wave function

### 2.1 The quarter-turn operator

Let \(\mathcal H_\mathbb R\) be a real Hilbert space with real inner product \(g(\cdot,\cdot)\). A **phase structure** is a bounded real-linear operator

\[
J:\mathcal H_\mathbb R\to\mathcal H_\mathbb R
\]

such that

\[
J^2=-I,
\qquad J^*=-J,
\qquad J^*J=I.
\tag{2.1}
\]

Thus \(J\) acts as an orthogonal quarter turn in every phase plane. The relations imply

\[
g(J\phi,J\psi)=g(\phi,\psi),
\qquad
g(J\phi,\psi)=-g(\phi,J\psi).
\tag{2.2}
\]

No real vector can be an eigenvector of \(J\), because \(J^2=-I\). Each nonzero amplitude therefore belongs to a two-dimensional real plane spanned by \(\psi\) and \(J\psi\). This is the geometric content conventionally compressed into multiplication by \(i\).

Define the phase scalar algebra

\[
\mathbb C_J\equiv\{aI+bJ\mid a,b\in\mathbb R\}.
\tag{2.3}
\]

For \(a,b,c,d\in\mathbb R\), the product is

\[
(aI+bJ)(cI+dJ)=(ac-bd)I+(ad+bc)J.
\tag{2.4}
\]

The conjugation-like involution and multiplicative norm are

\[
(aI+bJ)^\sharp=aI-bJ,
\qquad
N_J(aI+bJ)=(aI+bJ)^\sharp(aI+bJ)=a^2+b^2.
\tag{2.5}
\]

The map \(aI+bJ\mapsto a+ib\) is an algebra isomorphism. The point of the present formulation is not to deny this equivalence, but to avoid treating the coordinate symbol \(i\) as more fundamental than the quarter-turn structure it represents.

### 2.2 Phase numbers

The unit-norm elements of \(\mathbb C_J\) form the phase-number group

\[
\mathsf P_J\equiv\{u\in\mathbb C_J:N_J(u)=1\}.
\tag{2.6}
\]

For every \(\theta\in\mathbb R\), define

\[
\operatorname{Ph}_J(\theta)
\equiv e^{\theta J}
=\cos\theta\,I+\sin\theta\,J.
\tag{2.7}
\]

These factors multiply as

\[
\operatorname{Ph}_J(\alpha)\operatorname{Ph}_J(\beta)
=\operatorname{Ph}_J(\alpha+\beta),
\qquad
\operatorname{Ph}_J(\theta)^\sharp
=\operatorname{Ph}_J(-\theta).
\tag{2.8}
\]

The map \(\theta\mapsto\operatorname{Ph}_J(\theta)\) is surjective with kernel \(2\pi\mathbb Z\). Accordingly, a phase number is a global element of a circle group, whereas a real angle is only a lift defined modulo \(2\pi\). This distinction becomes indispensable for nodal wave fields, gauge transport, and geometric phase.

---

## 3. The phase-number wave function

### 3.1 Position representation

Let the configuration space be \(Q=\mathbb R^d\). The one-particle amplitude space is the phase Hilbert module

\[
\mathcal H_J=L^2(\mathbb R^d,\mathbb C_J),
\tag{3.1}
\]

viewed equivalently as the real Hilbert space \(L^2(\mathbb R^d,\mathbb R^2)\) with the pointwise action of \(J\). An abstract normalized state \(\lvert\Psi\rangle\) has a position amplitude

\[
\psi(x,t)=\langle x\mid\Psi(t)\rangle_J,
\tag{3.2}
\]

where \(\lvert x\rangle\) denotes the usual generalized position eigenvector. Mathematically, \(\psi\) is an \(L^2\) equivalence class; when a representative is continuous, the pointwise notation in (3.2) is literal.

Write the amplitude in two real quadratures,

\[
\psi(x,t)=q(x,t)+Jp(x,t),
\qquad q,p:\mathbb R^d\times\mathbb R\to\mathbb R.
\tag{3.3}
\]

The wave function is therefore not a single real wave. It is an ordered phase plane of real amplitudes. The phase structure rotates the quadratures according to

\[
J\psi=-p+Jq.
\tag{3.4}
\]

A global phase number \(u\in\mathsf P_J\) acts pointwise by \(\psi\mapsto u\psi\), rotating \((q,p)\) without changing the density. This is the wave-function realization of ray equivalence.

### 3.2 Phase-valued overlap and Born density

The phase-valued Hilbert inner product is

\[
\langle\phi,\psi\rangle_J
=\int_{\mathbb R^d}
\left[g\big(\phi(x),\psi(x)\big)I+
 g\big(J\phi(x),\psi(x)\big)J\right]d^dx.
\tag{3.5}
\]

It satisfies

\[
\langle\phi,\psi\rangle_J^\sharp
=\langle\psi,\phi\rangle_J,
\qquad
\langle a\phi,b\psi\rangle_J
=a^\sharp\langle\phi,\psi\rangle_Jb.
\tag{3.6}
\]

The **Born density** is the pointwise phase norm

\[
\rho(x,t)
=N_J\big(\psi(x,t)\big)
=\psi(x,t)^\sharp\psi(x,t)
=q(x,t)^2+p(x,t)^2.
\tag{3.7}
\]

For a Borel region \(\Omega\subseteq\mathbb R^d\), the probability of finding the particle in \(\Omega\) is

\[
\mathbb P_\psi(\Omega)
=\int_\Omega\rho(x,t)\,d^dx.
\tag{3.8}
\]

Normalization is \(\int\rho\,d^dx=1\). Equation (3.7) gives the direct derivation of the position-space probability law from the phase scalar norm. A phase multiplication leaves it invariant:

\[
N_J(u\psi)=u^\sharp u\,N_J(\psi)=N_J(\psi).
\tag{3.9}
\]

The two-quadrature character is essential. A real amplitude \(q\) has density \(q^2\), but it does not support a continuous internal rotation that preserves all interference relations. The phase-number wave function contains both quadratures, and their relative orientation is operationally accessible through interference.

### 3.3 Interference and the need for phase structure

Let two contributions to a position amplitude be \(\psi_1=R_1u_1\) and \(\psi_2=R_2u_2\), where \(R_a\ge0\) and \(u_a\in\mathsf P_J\). Then

\[
\begin{aligned}
N_J(\psi_1+\psi_2)
&=R_1^2+R_2^2
+2R_1R_2\operatorname{Re}_J(u_1^\sharp u_2).
\end{aligned}
\tag{3.10}
\]

Only the relative phase number \(u_1^\sharp u_2\) enters. A common phase factor cancels:

\[
(wu_1)^\sharp(wu_2)=u_1^\sharp u_2.
\tag{3.11}
\]

Thus the wave function’s phase is neither an absolute angle nor a dispensable decoration. It is the algebraic structure that controls the cross term in probability density.

---

## 4. General derivation of Schrödinger evolution

### 4.1 Continuous phase-preserving flow

Let \(U_t\) be the evolution of an isolated system. Reversibility and conservation of transition probabilities require

\[
U_{t+s}=U_tU_s,
\qquad U_0=I,
\qquad g(U_t\phi,U_t\psi)=g(\phi,\psi),
\qquad U_tJ=JU_t.
\tag{4.1}
\]

Assume strong continuity. On the domain of its generator, define

\[
G\psi=\left.\frac{d}{dt}U_t\psi\right|_{t=0}.
\tag{4.2}
\]

Differentiating the metric-preservation condition yields

\[
G^*=-G.
\tag{4.3}
\]

Differentiating the phase-covariance relation gives \([G,J]=0\). Define the Hamiltonian by

\[
H\equiv\hbar JG.
\tag{4.4}
\]

Then

\[
H^*=(\hbar JG)^*=\hbar G^*J^*=\hbar(-G)(-J)=\hbar GJ=\hbar JG=H.
\tag{4.5}
\]

Consequently \(G=-JH/\hbar\), and every such reversible phase-preserving evolution obeys

\[
\boxed{\;J\hbar\,\partial_t\psi=H\psi.\;}
\tag{4.6}
\]

This is the general Schrödinger equation in phase-number notation. Stone’s theorem gives the infinite-dimensional operator-theoretic form of this statement: a strongly continuous unitary group is generated by a self-adjoint operator once the phase generator is identified.[3]

The solution for time-independent \(H\) is

\[
U_t=\exp\!\left(-\frac{t}{\hbar}JH\right).
\tag{4.7}
\]

For an eigenstate \(H\phi_E=E\phi_E\),

\[
\psi_E(t)=
\operatorname{Ph}_J\!\left(-\frac{Et}{\hbar}\right)\phi_E.
\tag{4.8}
\]

Energy is therefore the angular frequency of phase-number transport, measured in units of \(\hbar\).

### 4.2 Coupled real form

For a Hamiltonian \(H\) that commutes with \(J\), substitute (3.3) into (4.6). Equating the two real quadratures gives

\[
-\hbar\,\partial_t p=Hq,
\qquad
\hbar\,\partial_t q=Hp.
\tag{4.9}
\]

These coupled real equations are not an approximation to wave mechanics. They are precisely the Schrödinger wave function expressed in real phase-plane coordinates. The operator \(J\) packages the mutual quarter-turn coupling of the two fields into the compact equation (4.6).

### 4.3 Hamiltonian flow

The real Hilbert space carries the symplectic form

\[
\Omega(\phi,\psi)=g(J\phi,\psi).
\tag{4.10}
\]

For the energy functional

\[
\mathcal E[\psi]=\frac12g(\psi,H\psi),
\tag{4.11}
\]

its Hamiltonian vector field \(X_\mathcal E\), defined by

\[
\Omega(X_\mathcal E,\delta\psi)
=\frac{1}{\hbar}d\mathcal E_\psi(\delta\psi),
\tag{4.12}
\]

is \(X_\mathcal E=-JH\psi/\hbar\). Therefore the Schrödinger equation is Hamilton’s equation on an infinite-dimensional real symplectic space. The phase-number formulation makes this geometry explicit instead of hiding it inside scalar notation.

---

## 5. Deriving the free Schrödinger wave equation

### 5.1 Translation generators and momentum

A spatial translation by \(a\in\mathbb R^d\) acts on a wave function by

\[
(T(a)\psi)(x)=\psi(x-a).
\tag{5.1}
\]

The generator \(P_j\) is defined by

\[
T(a)=\exp\!\left(-\frac{J}{\hbar}a^jP_j\right).
\tag{5.2}
\]

Differentiating (5.1) at \(a=0\) gives

\[
P_j=-J\hbar\partial_j.
\tag{5.3}
\]

The canonical position operator is \((X_j\psi)(x)=x_j\psi(x)\). On a suitable common domain,

\[
[X_j,P_k]=J\hbar\delta_{jk}I.
\tag{5.4}
\]

This shows that the canonical commutator is a phase-plane relation: translations are generated by a derivative multiplied by the quarter-turn \(J\).

### 5.2 Symmetry selection of the free Hamiltonian

For a free particle, the Hamiltonian must commute with translations. Hence, in momentum representation, it is multiplication by a real function \(E(p)\). Rotational invariance and parity require

\[
E(p)=F(|p|^2).
\tag{5.5}
\]

Locality and the requirement that the leading nontrivial free generator be a second-order scalar differential operator select

\[
H_0=-\kappa\nabla^2+E_0,
\qquad \kappa>0.
\tag{5.6}
\]

The additive constant \(E_0\) generates a spatially uniform phase number and may be set to zero by an energy-origin convention. The remaining coefficient \(\kappa\) is fixed by Galilei covariance.

### 5.3 Galilei covariance fixes the kinetic coefficient

Start from

\[
J\hbar\partial_t\psi=-\kappa\nabla^2\psi.
\tag{5.7}
\]

Let \(v\) be a constant boost velocity. Seek a transformed solution of the form

\[
\psi'(x,t)=
\operatorname{Ph}_J\!\left(a\,v\cdot x+b\,|v|^2t\right)
\psi(x-vt,t).
\tag{5.8}
\]

Insertion of (5.8) into (5.7) and matching the terms proportional to \(v\cdot\nabla\psi\) and \(|v|^2\psi\) yields

\[
a=\frac{\hbar}{2\kappa},
\qquad
b=-\frac{\hbar}{4\kappa}.
\tag{5.9}
\]

Define the mass parameter by

\[
m\equiv\frac{\hbar^2}{2\kappa}.
\tag{5.10}
\]

The boost law becomes

\[
\psi'(x,t)=
\operatorname{Ph}_J\!\left(
\frac{m\,v\cdot x-\tfrac12m|v|^2t}{\hbar}
\right)
\psi(x-vt,t),
\tag{5.11}
\]

and the free Hamiltonian is

\[
H_0=-\frac{\hbar^2}{2m}\nabla^2
=\frac{P^2}{2m}.
\tag{5.12}
\]

The complete free-particle Schrödinger wave equation is therefore

\[
\boxed{
J\hbar\partial_t\psi(x,t)
=-\frac{\hbar^2}{2m}\nabla^2\psi(x,t).
}
\tag{5.13}
\]

Equation (5.13) is not postulated as an isolated differential equation. It is selected by the phase structure, continuous reversible flow, translation symmetry, local isotropic second-order dynamics, and Galilei covariance. The mass is the central parameter in the projective representation of Galilei boosts, appearing here as the coefficient that determines the boost phase number.

---

## 6. Potentials, local phase symmetry, and electromagnetic coupling

### 6.1 Scalar potentials

A real scalar potential \(V(x,t)\) acts by multiplication and is self-adjoint. The wave equation becomes

\[
J\hbar\partial_t\psi=
\left(-\frac{\hbar^2}{2m}\nabla^2+V\right)\psi.
\tag{6.1}
\]

This is the phase-number form of the ordinary time-dependent Schrödinger equation. A constant shift \(V\mapsto V+C\) multiplies the total state by the global phase number \(\operatorname{Ph}_J(-Ct/\hbar)\) and does not alter position probabilities.

### 6.2 Gauge-covariant derivative

Let \(q\) be the particle charge and \(A_\mu=(\varphi,-\mathbf A)\) an electromagnetic potential. Under a local phase-frame change,

\[
\psi'(x,t)=
\operatorname{Ph}_J\!\left(\frac{q\chi(x,t)}{\hbar}\right)\psi(x,t),
\tag{6.2}
\]

the potentials transform as

\[
\mathbf A'=\mathbf A+\nabla\chi,
\qquad
\varphi'=\varphi-\partial_t\chi.
\tag{6.3}
\]

Define

\[
\mathbf D=\nabla-\frac{Jq}{\hbar}\mathbf A,
\qquad
\boldsymbol\Pi=-J\hbar\mathbf D=-J\hbar\nabla-q\mathbf A.
\tag{6.4}
\]

Then

\[
\mathbf D'\psi'
=
\operatorname{Ph}_J\!\left(\frac{q\chi}{\hbar}\right)\mathbf D\psi.
\tag{6.5}
\]

The gauge-covariant Schrödinger wave equation is

\[
J\hbar\partial_t\psi=
\left[\frac{\boldsymbol\Pi^2}{2m}+q\varphi+V\right]\psi.
\tag{6.6}
\]

The phase-number field in (6.2) is the local transition function of the amplitude frame. This is the exact rank-one \(U(1)\) geometry underlying electromagnetic gauge covariance.

### 6.3 Aharonov–Bohm phase number

Around a closed loop \(C\), the gauge connection contributes the holonomy

\[
U_{\mathrm{AB}}(C)=
\operatorname{Ph}_J\!\left(
\frac{q}{\hbar}\oint_C\mathbf A\cdot d\mathbf x
\right).
\tag{6.7}
\]

The Aharonov–Bohm effect demonstrates that this closed-loop phase factor can shift interference even when the magnetic field vanishes along the particle paths.[4] Its natural observable form is the phase number \(U_{\mathrm{AB}}\), not an unqualified phase angle.

---

## 7. Probability current and conservation of the wave function

### 7.1 Free-particle continuity equation

For the scalar-potential equation (6.1), define

\[
\rho=\psi^\sharp\psi,
\qquad
\mathbf j=\frac{\hbar}{m}\,g(J\psi,\nabla\psi).
\tag{7.1}
\]

The current \(\mathbf j\) is real. Using (6.1) and its \(\sharp\)-conjugate gives

\[
\partial_t\rho
=2g(\psi,\partial_t\psi)
=-\frac{\hbar}{m}\nabla\cdot g(J\psi,\nabla\psi).
\tag{7.2}
\]

Hence

\[
\boxed{\;\partial_t\rho+\nabla\cdot\mathbf j=0.\;}
\tag{7.3}
\]

The total probability \(\int\rho\,d^dx\) is conserved when the surface flux vanishes at infinity or on the boundary. The derivation shows that probability conservation is the local form of metric preservation under Schrödinger evolution.

### 7.2 Gauge-covariant current

With vector potential \(\mathbf A\), define

\[
\mathbf j
=\frac{1}{m}\,g\big(\psi,\boldsymbol\Pi\psi\big)
=\frac{\hbar}{m}g(J\psi,\nabla\psi)-\frac{q}{m}\mathbf A\rho.
\tag{7.4}
\]

The gauge-covariant equation (6.6) again yields (7.3). The current is frame invariant because the connection term compensates the local phase rotation.

### 7.3 Expectation flow

For a normalized wave function and a sufficiently regular potential, the expectation of position obeys

\[
\frac{d}{dt}\langle X_j\rangle
=\frac{1}{m}\langle\Pi_j\rangle.
\tag{7.5}
\]

In the absence of electromagnetic fields,

\[
\frac{d}{dt}\langle P_j\rangle
=-\langle\partial_jV\rangle.
\tag{7.6}
\]

These are the Ehrenfest relations in phase-number notation. The phase generator \(J\) enters the underlying commutator structure but cancels from the real expectation-value equations.

---

## 8. Polar phase-number decomposition and quantum Hamilton–Jacobi theory

### 8.1 Amplitude times phase number

Away from zeros of \(\psi\), every scalar amplitude has a unique factorization

\[
\psi(x,t)=R(x,t)u(x,t),
\qquad R=\sqrt\rho>0,
\qquad u(x,t)\in\mathsf P_J.
\tag{8.1}
\]

On a simply connected nodal-free region, choose a local action lift \(S\) such that

\[
u(x,t)=
\operatorname{Ph}_J\!\left(\frac{S(x,t)}{\hbar}\right).
\tag{8.2}
\]

The phase number \(u\) is global on the nodal-free domain; the real function \(S\) is only a local logarithmic coordinate. Its derivatives satisfy

\[
u^{-1}\partial_\mu u=
\frac{J}{\hbar}\partial_\mu S.
\tag{8.3}
\]

### 8.2 Separation of the wave equation

Insert \(\psi=Ru\) into (6.1). The time derivative and Laplacian are

\[
\partial_t\psi
=u\left(\partial_tR+\frac{J}{\hbar}R\partial_tS\right),
\tag{8.4}
\]

\[
\nabla^2\psi
=u\left[
\nabla^2R-\frac{R}{\hbar^2}|\nabla S|^2
+\frac{J}{\hbar}\big(2\nabla R\cdot\nabla S+R\nabla^2S\big)
\right].
\tag{8.5}
\]

Separating the real and \(J\)-components yields

\[
\partial_t\rho+
\nabla\cdot\left(\rho\frac{\nabla S}{m}\right)=0,
\tag{8.6}
\]

and

\[
\partial_tS+
\frac{|\nabla S|^2}{2m}+V+Q=0,
\qquad
Q=-\frac{\hbar^2}{2m}\frac{\nabla^2\sqrt\rho}{\sqrt\rho}.
\tag{8.7}
\]

Equation (8.6) is the continuity equation, while (8.7) is the quantum Hamilton–Jacobi equation. The quantum potential \(Q\) is generated by the curvature of the amplitude modulus under the Laplacian. Together, (8.6) and (8.7) are locally equivalent to the Schrödinger equation wherever \(\rho>0\).

### 8.3 Classical limit and phase-number persistence

When the amplitude-curvature term \(Q\) is negligible compared with the remaining terms in (8.7), the equation reduces to the classical Hamilton–Jacobi equation. The phase-number expression remains well defined throughout: it is the local action lift that becomes rapidly varying, not the underlying unit phase factor. This distinction clarifies why semiclassical interference is governed by phases even when a classical action description becomes useful.

---

## 9. Wave modes: plane waves, packets, stationary states, and bound states

### 9.1 Phase-number plane waves

For the free Hamiltonian, let \(p\in\mathbb R^d\), \(E=|p|^2/(2m)\), and \(R\) be constant. The phase-number plane wave is

\[
\psi_{p,E}(x,t)=
R\operatorname{Ph}_J\!\left(
\frac{p\cdot x-Et}{\hbar}
\right).
\tag{9.1}
\]

It satisfies

\[
P_j\psi_{p,E}=p_j\psi_{p,E},
\qquad
H_0\psi_{p,E}=E\psi_{p,E}.
\tag{9.2}
\]

The de Broglie relations appear as the phase-number gradient identities

\[
\nabla S=p,
\qquad
-\partial_tS=E.
\tag{9.3}
\]

The plane wave’s phase is globally represented by \(\operatorname{Ph}_J((p\cdot x-Et)/\hbar)\), while the affine action \(S=p\cdot x-Et\) is one selected lift.

### 9.2 Wave packets

A general free wave function can be represented by the phase-number Fourier integral

\[
\psi(x,t)=
\frac{1}{(2\pi\hbar)^{d/2}}
\int_{\mathbb R^d}
\widetilde\psi(p)
\operatorname{Ph}_J\!\left(
\frac{p\cdot x-|p|^2t/(2m)}{\hbar}
\right)d^dp.
\tag{9.4}
\]

The coefficients \(\widetilde\psi(p)\in\mathbb C_J\) encode the momentum-space phase and amplitude. The integral is a superposition of phase numbers weighted by phase scalars. Dispersion arises because different momentum components rotate at different energy frequencies.

### 9.3 Stationary states

For a time-independent potential, solve the eigenvalue equation

\[
H\phi_n=E_n\phi_n.
\tag{9.5}
\]

The corresponding wave function is

\[
\psi_n(x,t)=
\operatorname{Ph}_J\!\left(-\frac{E_nt}{\hbar}\right)\phi_n(x).
\tag{9.6}
\]

Because the time factor is a unit phase number,

\[
N_J\big(\psi_n(x,t)\big)=N_J\big(\phi_n(x)\big),
\tag{9.7}
\]

so the position density of an energy eigenstate is stationary. Energy eigenstates are therefore phase rotors in Hilbert space, not static amplitude vectors.

### 9.4 Harmonic oscillator

For \(V(x)=m\omega^2x^2/2\), define

\[
a=\sqrt{\frac{m\omega}{2\hbar}}X+
\frac{J}{\sqrt{2m\hbar\omega}}P,
\qquad
a^\sharp=\sqrt{\frac{m\omega}{2\hbar}}X-
\frac{J}{\sqrt{2m\hbar\omega}}P.
\tag{9.8}
\]

Then \([a,a^\sharp]=I\) and

\[
H=\hbar\omega\left(a^\sharp a+\frac12I\right).
\tag{9.9}
\]

The oscillator energies are \(E_n=\hbar\omega(n+\tfrac12)\), and each eigenfunction evolves through the phase number in (9.6). The ladder formalism is unchanged; the symbol convention for the phase generator is the only alteration.

---

## 10. Nodes, winding, and the global wave-function phase

At a nodal point or nodal set, \(\rho=0\) and the normalized phase number \(u=\psi/\sqrt\rho\) is undefined. This is not a defect of the theory. It is the exact location at which a local phase angle cannot be assigned because the amplitude has no direction in the phase plane.

For a closed loop \(C\) in a nodal-free region, the phase field has the integer winding

\[
\operatorname{wind}(u;C)
=\frac{1}{2\pi}
\oint_C -J\,u^{-1}du
\in\mathbb Z.
\tag{10.1}
\]

Locally \(u=\operatorname{Ph}_J(S/\hbar)\), so (10.1) gives

\[
\oint_C dS=2\pi n\hbar,
\qquad n\in\mathbb Z.
\tag{10.2}
\]

The exponentiated phase field is globally meaningful even when a single action function \(S\) does not exist globally. This is the wave-function counterpart of the general distinction between phase numbers and phase angles.

In gauge-coupled systems, the gauge-invariant circulation is built from \(\nabla S-q\mathbf A\). The phase-number language therefore unifies nodal circulation, electromagnetic holonomy, and the global topology of quantum amplitude fields.

---

## 11. Equivalence theorem and interpretation

### 11.1 Exact representation equivalence

**Theorem 11.1.** Let \((\mathcal H_\mathbb R,g,J)\) be a real Hilbert space with an orthogonal complex structure. Define multiplication by a conventional complex scalar through

\[
(a+ib)\psi\equiv(aI+bJ)\psi.
\tag{11.1}
\]

Then \(\mathcal H_\mathbb R\) is canonically a complex Hilbert space, and the phase-number Schrödinger equation (4.6) maps exactly to the standard complex Schrödinger equation. Conversely, every complex Schrödinger wave function determines a phase-number wave function by restriction of scalars and identification of multiplication by the conventional phase generator with \(J\).

**Proof.** The algebra map \(aI+bJ\mapsto a+ib\) preserves addition, multiplication, involution, and norm by (2.4)–(2.5). The inner product (3.5) is positive, complete, conjugate symmetric, and linear over \(\mathbb C_J\). Under the map, \(J\) becomes multiplication by the conventional imaginary unit. Equation (4.6) then becomes the standard Schrödinger equation, while (3.7), (5.3), (6.6), and all phase-number products become their standard complex counterparts. The reverse construction is immediate by forgetting the complex scalar notation and retaining its real action \(J\). \(\square\)

The theorem fixes the empirical interpretation. This white paper does not propose a deviation from nonrelativistic quantum predictions. It gives an intrinsic re-expression of their phase structure. Analyses of real-Hilbert-space formulations likewise demonstrate that an appropriate invariant complex structure recovers standard complex quantum theory.[5]

### 11.2 What is genuinely clarified

The phase-number form distinguishes objects that conventional notation often merges. The table gives the principal dictionary.

| Conventional notation | Phase-number notation | Structural meaning |
| --- | --- | --- |
| \(i\) | \(J\) | Orthogonal quarter-turn |
| \(a+ib\) | \(aI+bJ\) | Two-dimensional real phase scalar |
| \(e^{i\theta}\) | \(\operatorname{Ph}_J(\theta)\) | Global unit phase number |
| \(i\hbar\partial_t\psi=H\psi\) | \(J\hbar\partial_t\psi=H\psi\) | Hamiltonian phase rotation |
| \(-i\hbar\nabla\) | \(-J\hbar\nabla\) | Translation generator |
| \(e^{iS/\hbar}\) | \(\operatorname{Ph}_J(S/\hbar)\) | Local action lift exponentiated to phase |
| \(e^{i(q/\hbar)\oint A}\) | \(\operatorname{Ph}_J((q/\hbar)\oint A)\) | Gauge holonomy |

The central clarification is global. A phase angle may be unavailable around a node or on a topologically nontrivial configuration; the phase-number field remains well defined away from the node and its holonomy remains observable. The formalism therefore replaces branch-dependent language with invariant statements.

---

## 12. Conclusion

The Schrödinger wave function has been derived as a phase-number-valued position amplitude. Its amplitude modulus produces the Born density, while its unit phase factor carries the second real quadrature required for interference, reversible evolution, translation generators, and gauge transport. The intrinsic quarter-turn operator \(J\) generates the phase circle and produces the Schrödinger form \(J\hbar\partial_t\psi=H\psi\) from metric-preserving, phase-covariant continuous evolution.

For a free particle, translation symmetry identifies momentum as \(P=-J\hbar\nabla\). Locality, rotational symmetry, parity, and Galilei covariance select the kinetic Hamiltonian \(P^2/(2m)\), yielding the free wave equation. Scalar and electromagnetic potentials extend the construction by self-adjoint multiplication and phase connection, respectively. The polar decomposition then reveals probability conservation and the quantum Hamilton–Jacobi system, while nodal winding demonstrates why phase numbers are globally primary and phase angles are not.

> **Final statement.** The Schrödinger wave function is not a real amplitude decorated by a conventional imaginary symbol. It is a two-quadrature density amplitude whose intrinsic quarter-turn \(J\) generates phase numbers. Standard complex wave mechanics is the coordinate representation of that phase geometry.

---

## Appendix A. Detailed Galilei-boost calculation

Let

\[
\psi'(x,t)=u_f(x,t)\psi(y,t),
\qquad y=x-vt,
\qquad u_f=\operatorname{Ph}_J(f),
\tag{A.1}
\]

with \(f=a\,v\cdot x+b|v|^2t\). Then

\[
\partial_t\psi'
=u_f\left[J(\partial_tf)\psi+\partial_t\psi-v\cdot\nabla\psi\right],
\tag{A.2}
\]

and

\[
\nabla^2\psi'
=u_f\left[\nabla^2\psi+2J(\nabla f)\cdot\nabla\psi-|\nabla f|^2\psi\right].
\tag{A.3}
\]

Using \(J\hbar\partial_t\psi=-\kappa\nabla^2\psi\) for \(\psi\), the transformed equation is satisfied when

\[
-J\hbar v\cdot\nabla\psi-
\hbar b|v|^2\psi
=-2\kappa Ja\,v\cdot\nabla\psi+
\kappa a^2|v|^2\psi.
\tag{A.4}
\]

Matching the linearly independent terms gives

\[
2\kappa a=\hbar,
\qquad
-\hbar b=\kappa a^2.
\tag{A.5}
\]

Hence \(a=\hbar/(2\kappa)\) and \(b=-\hbar/(4\kappa)\). With \(m=\hbar^2/(2\kappa)\), equation (5.11) follows.

## Appendix B. Direct derivation of probability conservation

Starting from the scalar-potential equation,

\[
\partial_t\psi=
\frac{J\hbar}{2m}\nabla^2\psi-
\frac{J}{\hbar}V\psi,
\tag{B.1}
\]

one finds

\[
\begin{aligned}
\partial_t\rho
&=2g(\psi,\partial_t\psi)\\
&=\frac{\hbar}{m}g(\psi,J\nabla^2\psi)\\
&=-\frac{\hbar}{m}g(J\psi,\nabla^2\psi)\\
&=-\nabla\cdot\left[\frac{\hbar}{m}g(J\psi,\nabla\psi)\right].
\end{aligned}
\tag{B.2}
\]

The potential term vanishes because \(g(\psi,J\psi)=0\). This proves equation (7.3).

## Appendix C. Polar-derivative identities

With \(\psi=Ru\) and \(u=\operatorname{Ph}_J(S/\hbar)\),

\[
\partial_\mu u=\frac{J}{\hbar}(\partial_\mu S)u.
\tag{C.1}
\]

The product rule gives (8.4) and (8.5). Separating their \(I\) and \(J\) components in the Schrödinger equation gives (8.6) and (8.7). The calculation is valid on every connected region where \(R>0\); global reconstruction is controlled by the phase number and its winding, not by a single globally defined \(S\).

## Appendix D. Notation dictionary

| Symbol | Meaning |
| --- | --- |
| \(\mathcal H_\mathbb R\) | Underlying real Hilbert space of amplitudes |
| \(g\) | Real Hilbert inner product |
| \(J\) | Orthogonal quarter-turn, \(J^2=-I\) |
| \(\mathbb C_J\) | Phase scalar algebra \(\{aI+bJ\}\) |
| \(\mathsf P_J\) | Unit phase-number group |
| \(\operatorname{Ph}_J(\theta)\) | \(e^{\theta J}\), a phase number |
| \(\psi=q+Jp\) | Position wave function in two real quadratures |
| \(\rho\) | Born density \(N_J(\psi)\) |
| \(P\) | Momentum \(-J\hbar\nabla\) |
| \(H\) | Self-adjoint Hamiltonian |
| \(S\) | Local real action lift of a phase-number field |

---

## References

[1] E. Schrödinger, “Quantisierung als Eigenwertproblem,” *Annalen der Physik* **384** (4), 361–376 (1926). [https://doi.org/10.1002/andp.19263840404](https://doi.org/10.1002/andp.19263840404)

[2] D. D. Spiegel, “A Simple Constructive Proof of Wigner’s Theorem,” *arXiv:1810.10111* (2022). [https://arxiv.org/html/1810.10111](https://arxiv.org/html/1810.10111)

[3] M. H. Stone, “On One-Parameter Unitary Groups in Hilbert Space,” *Annals of Mathematics* **33**, 643–648 (1932). [https://doi.org/10.2307/1968538](https://doi.org/10.2307/1968538)

[4] Y. Aharonov and D. Bohm, “Significance of Electromagnetic Potentials in the Quantum Theory,” *Physical Review* **115**, 485–491 (1959). [https://doi.org/10.1103/PhysRev.115.485](https://doi.org/10.1103/PhysRev.115.485)

[5] V. Moretti and M. Oppio, “Quantum theory in real Hilbert space: How the complex Hilbert space structure emerges from Poincaré symmetry,” *Reviews in Mathematical Physics* **29**, 1750021 (2017). [https://arxiv.org/abs/1611.09029](https://arxiv.org/abs/1611.09029)

[6] M. Hanks, *Phase Numbers: An Intrinsic Calculus of Unit-Complex Scalars, Circular Coordinates, and Holonomy*, unpublished foundational manuscript supplied by the author (22 August 2026).

[7] J. von Neumann, *Mathematical Foundations of Quantum Mechanics*, Princeton University Press (1955). [https://archive.org/details/mathematicalfoun0613vonn](https://archive.org/details/mathematicalfoun0613vonn)

[8] R. P. Feynman and A. R. Hibbs, *Quantum Mechanics and Path Integrals*, McGraw-Hill (1965). [https://archive.org/details/quantummechanics0000feyn](https://archive.org/details/quantummechanics0000feyn)

[1]: https://doi.org/10.1002/andp.19263840404 "Schrödinger (1926)"
[2]: https://arxiv.org/html/1810.10111 "Spiegel (2022)"
[3]: https://doi.org/10.2307/1968538 "Stone (1932)"
[4]: https://doi.org/10.1103/PhysRev.115.485 "Aharonov and Bohm (1959)"
[5]: https://arxiv.org/abs/1611.09029 "Moretti and Oppio (2017)"
[7]: https://archive.org/details/mathematicalfoun0613vonn "von Neumann (1955)"
[8]: https://archive.org/details/quantummechanics0000feyn "Feynman and Hibbs (1965)"

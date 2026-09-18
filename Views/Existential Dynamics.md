# Existential Dynamics: A Physical Theory Derived from Dynamic Mathematical Ontology

**Preprint**

---

## Abstract

We derive a physical theory from the axioms of Dynamic Mathematical Ontology (DMO). In this theory, existence operators become physical actualization projectors on Hilbert bundles, ontological transitions become dynamical evolution maps, structural persistence becomes the origin of conservation laws, and creation/annihilation maps become quantum-field creation and destruction operators. The resulting framework, called **Existential Dynamics**, yields: a derivation of Schrödinger and von Neumann dynamics from actuality compatibility; a gauge principle in which connections are precisely the local transitions preserving existence; a generalized Fock algebra controlled by a creation–annihilation yield \(\theta\); an existential stress tensor and field equation; a scalar existence sector coupled to gravity; and concrete modifications of standard physics, including existence-nonconserving decay, variable field-strength residues, actuality-forbidden transitions, and cosmological particle production. The paper is self-contained and gives tensorial derivations throughout.

**Keywords:** dynamic ontology, existence operator, quantum theory, gauge fields, creation and annihilation, Noether theorem, cosmology, existential dynamics.

---

## 1. Introduction

Dynamic Mathematical Ontology (DMO) replaces the classical assumption that existence is a static predicate with the hypothesis that existence is an operator-governed dynamical process. The primitive notions are:

1. existence operators \(\mathfrak{E}\);
2. ontological transitions \(f\);
3. structural persistence;
4. creation and annihilation maps.

We show that, when instantiated in linear categories, these notions generate physical law. The central claim is:

> Physical reality is the actual sector of a structural space, selected by an existence operator, transported by existence-preserving transitions, and modified by creation and annihilation processes.

From this claim we derive a physical theory with the following structure:

- States are vectors or density operators in a Hilbert bundle.
- Existence is represented by a self-adjoint idempotent \(E\).
- Physical transitions satisfy \(E_s T = T E_t\).
- Continuous transitions generate Hamiltonian dynamics.
- Local existence preservation generates gauge connections.
- Persistence under transitions generates conserved charges.
- Creation and annihilation generate quantum fields and particle production.
- Coarse-grained existence density behaves as a physical scalar coupled to geometry.

The resulting theory conservatively contains ordinary quantum mechanics and quantum field theory when the existence operator is the identity, \(E=I\). It extends them by adding explicit actualization sectors, existence currents, creation yields, and persistence constraints.

---

## 2. Physical Instantiation of DMO

### 2.1 Ontological quantale for physics

We take the ontological quantale to be

\[
Q=[0,1],\qquad a\otimes b=ab,
\]

or, for unnormalized amplitudes,

\[
Q=\mathbb{R}_{\ge 0},\qquad a\otimes b=ab.
\]

In either case:

- \(1\) is full actualization;
- \(0\) is nonexistence;
- multiplication represents conjunctive existence strength;
- joins represent alternative actualization channels.

For quantum physics, the relevant existence degrees are expectation values of projectors, so \(Q=[0,1]\) is the natural choice.

### 2.2 Structural category

Let the structural category be a category of complex Hilbert spaces and linear maps. For finite-dimensional systems, let \(\mathcal{H}\) be a complex Hilbert space with inner product \(\langle-|-\rangle\). For field theory, let

\[
\pi:\mathcal{H}\to M
\]

be a Hilbert bundle over a stage manifold \(M\), which we later identify with spacetime.

A physical object is represented by a fiber \(\mathcal{H}_x\), and a staged object is a pair \((\mathcal{H}_x,x)\).

### 2.3 Existence operators

A physical existence operator is a self-adjoint idempotent

\[
E_x:\mathcal{H}_x\to\mathcal{H}_x,
\]

satisfying

\[
E_x^2=E_x,\qquad E_x^\dagger=E_x.
\]

Thus \(E_x\) is an orthogonal projector. Its image

\[
\mathcal{A}_x=\operatorname{im}E_x
\]

is the **actual subspace** at stage \(x\).

The rank

\[
r(x)=\operatorname{rank}E_x
\]

measures the dimension of the actual sector. The coarse-grained existence density is

\[
\varepsilon(x)=\frac{1}{N}\operatorname{Tr}E_x,
\]

where \(N=\dim\mathcal{H}_x\), assuming constant finite dimension.

For a state vector \(\psi\in\mathcal{H}_x\), the existence degree is

\[
e_x(\psi)
=
\frac{\langle\psi|E_x|\psi\rangle}{\langle\psi|\psi\rangle}.
\]

A state is actual iff

\[
E_x\psi=\psi.
\]

### 2.4 Ontological transitions

An ontological transition from stage \(t\) to stage \(s\) is a linear map

\[
T_{s,t}:\mathcal{H}_t\to\mathcal{H}_s
\]

satisfying the DMO actuality condition

\[
T_{s,t}=E_sT_{s,t}E_t.
\]

Equivalently,

\[
E_sT_{s,t}=T_{s,t},\qquad T_{s,t}E_t=T_{s,t},
\]

and therefore

\[
E_sT_{s,t}=T_{s,t}E_t.
\]

In tensor notation,

\[
(E_s)^i{}_j (T_{s,t})^j{}_k
=
(T_{s,t})^i{}_j (E_t)^j{}_k.
\]

This is the fundamental kinematic constraint of Existential Dynamics.

---

## 3. Tensorial Kinematics

Let \(\psi^i\) be components of a state vector and let \(\psi_i^\ast\) denote the conjugate covector. The existence operator has components

\[
(E)^i{}_j.
\]

Actuality is

\[
(E)^i{}_j\psi^j=\psi^i.
\]

The existence scalar of \(\psi\) is

\[
e(\psi)
=
\frac{\psi_i^\ast (E)^i{}_j\psi^j}{\psi_k^\ast\psi^k}.
\]

For composite systems,

\[
\mathcal{H}_{AB}=\mathcal{H}_A\otimes\mathcal{H}_B,
\]

and the composite existence operator is

\[
(E_{AB})^{ik}{}_{jl}
=
(E_A)^i{}_j(E_B)^k{}_l.
\]

For product states,

\[
\psi_{AB}^{ik}=\psi_A^i\psi_B^k,
\]

we obtain

\[
e_{AB}(\psi_A\otimes\psi_B)
=
e_A(\psi_A)e_B(\psi_B).
\]

This is the physical form of the DMO theorem

\[
e(A\otimes B)=e(A)\otimes e(B).
\]

### 3.1 Born rule as existence valuation

Let \(\{|a\rangle\}\) be an orthonormal basis of detector records, and let

\[
E_a=|a\rangle\langle a|.
\]

If a system is in state

\[
|\psi\rangle=\sum_a c_a|a\rangle,
\]

then the existence degree of the record \(a\) is

\[
e_a(\psi)
=
\langle\psi|E_a|\psi\rangle
=
|c_a|^2.
\]

Thus the Born probability is not an independent measurement postulate but the existence valuation of an actualization projector.

More generally, if a detector record is created by a creation map

\[
c_a:V\to \mathcal{H}_a,
\]

then the transition strength is

\[
\rho(c_a)=\langle\psi|E_a|\psi\rangle,
\]

and the DMO propagation law

\[
e(\text{record }a)\ge e(\psi)\otimes\rho(c_a)
\]

gives the same result.

---

## 4. Continuous Dynamics and the Schrödinger Equation

Let stages form a continuous parameter \(t\in\mathbb{R}\). Let

\[
T_{t+dt,t}=I+L_t\,dt+o(dt)
\]

be an infinitesimal ontological transition. The compatibility condition

\[
E_{t+dt}T_{t+dt,t}=T_{t+dt,t}E_t
\]

gives

\[
(E_t+\dot E_tdt)(I+L_tdt)
=
(I+L_tdt)E_t+o(dt).
\]

Expanding to first order,

\[
E_t+\dot E_tdt+E_tL_tdt
=
E_t+L_tE_tdt.
\]

Hence

\[
\dot E_t=L_tE_t-E_tL_t,
\]

or

\[
\boxed{\dot E_t=[L_t,E_t].}
\]

This is the infinitesimal law of existence evolution.

### 4.1 Existence-conserving dynamics

A transition is existence-conserving if it preserves the existence scalar of every actual state. For a closed system this forces \(L_t\) to be anti-Hermitian on the actual sector. We therefore write

\[
L_t=-iH_t,
\]

with

\[
H_t^\dagger=H_t.
\]

Then

\[
\boxed{\dot E_t=-i[H_t,E_t].}
\]

This is the Heisenberg equation for the existence projector.

If \(E_t\) is constant, then

\[
[H,E_t]=0.
\]

The actual subspace is invariant, and the state equation is

\[
\boxed{i\frac{d}{dt}|\psi_t\rangle=H_t|\psi_t\rangle.}
\]

Thus the Schrödinger equation is derived from existence-preserving ontological transitions.

### 4.2 Conservation of existence degree

Let

\[
|\dot\psi\rangle=-iH|\psi\rangle,
\]

and let

\[
\dot E=-i[H,E].
\]

Then

\[
\frac{d}{dt}\langle\psi|E|\psi\rangle
=
\langle\dot\psi|E|\psi\rangle
+
\langle\psi|\dot E|\psi\rangle
+
\langle\psi|E|\dot\psi\rangle.
\]

Substituting,

\[
\frac{d}{dt}\langle\psi|E|\psi\rangle
=
i\langle\psi|HE|\psi\rangle
-i\langle\psi|[H,E]|\psi\rangle
-i\langle\psi|EH|\psi\rangle.
\]

Using

\[
[H,E]=HE-EH,
\]

the terms cancel:

\[
\frac{d}{dt}\langle\psi|E|\psi\rangle=0.
\]

Therefore existence is conserved under closed existence-preserving evolution.

In density-matrix form, if

\[
\dot\rho=-i[H,\rho],
\]

then

\[
\frac{d}{dt}\operatorname{Tr}(E\rho)
=
\operatorname{Tr}(\dot E\rho)+\operatorname{Tr}(E\dot\rho)
=
-i\operatorname{Tr}([H,E]\rho)-i\operatorname{Tr}(E[H,\rho])
=
0.
\]

Thus

\[
\boxed{\frac{d}{dt}\operatorname{Tr}(E\rho)=0.}
\]

---

## 5. Nonconservative Transitions and Annihilation

Not all transitions conserve existence. Let

\[
T_{t+dt,t}
=
I-iHdt-\frac12\Gamma dt,
\]

where

\[
H^\dagger=H,
\qquad
\Gamma^\dagger=\Gamma\ge 0.
\]

For fixed \(E\), actuality compatibility requires

\[
E\Gamma=\Gamma E=\Gamma.
\]

Thus \(\Gamma\) acts only on the actual sector. The existence degree evolves as

\[
\frac{d}{dt}\langle\psi|E|\psi\rangle
=
-\langle\psi|\Gamma|\psi\rangle.
\]

The effective generator is

\[
\boxed{H_{\mathrm{eff}}=H-\frac{i}{2}\Gamma.}
\]

This describes decay, absorption, or annihilation of actual structure into the vacuum.

In density form,

\[
\dot\rho
=
-i[H,\rho]
-\frac12\{\Gamma,\rho\}
+\mathcal{C}(\rho),
\]

where \(\mathcal{C}\) is a creation superoperator. The corresponding existence balance law is

\[
\boxed{
\frac{d}{dt}\operatorname{Tr}(E\rho)
=
-\operatorname{Tr}(\Gamma\rho)
+
\operatorname{Tr}(E\mathcal{C}(\rho)).
}
\]

This is the physical form of creation–annihilation balance.

---

## 6. Open Existential Dynamics

A general existence-preserving open evolution is given by a completely positive generator whose jump operators are actual:

\[
L_\alpha=E L_\alpha E.
\]

The ontological master equation is

\[
\boxed{
\dot\rho
=
-i[H,\rho]
+
\sum_\alpha
\left(
L_\alpha\rho L_\alpha^\dagger
-\frac12\{L_\alpha^\dagger L_\alpha,\rho\}
\right)
+
\mathcal{C}(\rho)
-
\mathcal{A}(\rho).
}
\]

Here:

- \(H\) generates coherent actual evolution;
- \(L_\alpha\) generate actual decoherence channels;
- \(\mathcal{C}\) creates actual excitations from the vacuum;
- \(\mathcal{A}\) annihilates actual excitations into the vacuum.

The condition

\[
L_\alpha=E L_\alpha E
\]

is the DMO constraint that transitions act only on actual structure. It forbids unphysical leakage from nonactual sectors.

The existence degree satisfies

\[
\frac{d}{dt}\operatorname{Tr}(E\rho)
=
\operatorname{Tr}\!\left(
E\mathcal{C}(\rho)
\right)
-
\operatorname{Tr}\!\left(
E\mathcal{A}(\rho)
\right)
+
\operatorname{Tr}(\dot E\rho).
\]

When \(\dot E=0\) and \(\mathcal{C}=\mathcal{A}=0\), existence is conserved.

---

## 7. Gauge Fields from Local Existence Preservation

Let the stage manifold be spacetime \(M\). Let \(\mathcal{H}_x\) be a Hilbert bundle with existence projector \(E(x)\). A local transition from \(x\) to \(x+dx\) is written

\[
U(x+dx,x)=I+A_\mu(x)dx^\mu.
\]

Actuality compatibility gives

\[
E(x+dx)U(x+dx,x)=U(x+dx,x)E(x).
\]

Expanding,

\[
(E+\partial_\mu E dx^\mu)(I+A_\nu dx^\nu)
=
(I+A_\mu dx^\mu)E.
\]

Thus

\[
\partial_\mu E=A_\mu E-EA_\mu,
\]

or

\[
\boxed{
D_\mu E:=\partial_\mu E-[A_\mu,E]=0.
}
\]

Therefore gauge connections arise as the infinitesimal ontological transitions that preserve local existence.

If transitions are existence-conserving, then to first order \(U\) is unitary, so

\[
A_\mu^\dagger=-A_\mu.
\]

The curvature is

\[
F_{\mu\nu}
=
\partial_\mu A_\nu-\partial_\nu A_\mu+[A_\mu,A_\nu].
\]

Because \(D_\mu E=0\),

\[
[D_\mu,D_\nu]E=[F_{\mu\nu},E]=0.
\]

Thus the curvature must preserve the existence projector:

\[
\boxed{[F_{\mu\nu},E]=0.}
\]

This is a new field equation derived directly from DMO.

### 7.1 Stabilizer gauge group

The subgroup of local unitaries preserving \(E\) is

\[
G_E=\{U:UEU^{-1}=E\}.
\]

If \(E\) has rank \(r\) in an \(N\)-dimensional fiber, then locally

\[
G_E\cong U(r)\times U(N-r).
\]

In a frame where

\[
E=
\begin{pmatrix}
I_r&0\\
0&0
\end{pmatrix},
\]

write

\[
A_\mu=
\begin{pmatrix}
a_\mu&b_\mu\\
c_\mu&d_\mu
\end{pmatrix}.
\]

Then

\[
D_\mu E=0
\]

implies

\[
b_\mu=-\partial_\mu E_{12},
\qquad
c_\mu=\partial_\mu E_{21}.
\]

The diagonal blocks \(a_\mu\) and \(d_\mu\) remain free gauge fields. Thus variations of the existence projector induce off-diagonal gauge components, while the persistent actual sector carries the usual gauge freedom.

### 7.2 Existential Yang–Mills equation

Consider the gauge action

\[
S[A,E]
=
\int d^4x\sqrt{-g}
\left[
-\frac{1}{4g^2}\operatorname{Tr}(F_{\mu\nu}F^{\mu\nu})
+
\operatorname{Tr}(\Lambda^\mu D_\mu E)
\right].
\]

Varying \(A_\nu\) gives

\[
\boxed{
\frac{1}{g^2}D_\mu F^{\mu\nu}
+
[\Lambda^\nu,E]
+
J^\nu_{\mathrm{matter}}
=
0.
}
\]

Projecting onto the stabilizer of \(E\) gives the physical Yang–Mills equation with source:

\[
D_\mu F^{\mu\nu}=J^\nu_{\mathrm{phys}}.
\]

The term \([\Lambda^\nu,E]\) enforces the DMO constraint that gauge transport preserves existence.

---

## 8. Persistence and Conservation Laws

Structural persistence in DMO becomes Noether conservation in physics.

Let \(G\) be a structural symmetry generator. Suppose

\[
[G,E]=0
\]

and the action is invariant under

\[
\delta\psi=i\epsilon G\psi.
\]

Then the existential Noether current is

\[
\boxed{
j^\mu_G
=
i\left[
(D^\mu\psi)^\dagger E G\psi
-
\psi^\dagger E G D^\mu\psi
\right].
}
\]

If the field equations hold and \(D_\mu E=0\), then

\[
\boxed{
\nabla_\mu j^\mu_G=0.
}
\]

Thus conserved charges are precisely persistent structures under ontological transitions.

### 8.1 Energy as persistence under time translation

If \(E\) and \(H\) are time-independent, then energy is a persistent invariant:

\[
\frac{d}{dt}\langle\psi|H|\psi\rangle=0.
\]

If \(E\) varies, energy need not be conserved inside the actual sector. Define the existential energy

\[
\mathcal{E}
=
\langle\psi|EHE|\psi\rangle.
\]

Then

\[
\frac{d\mathcal{E}}{dt}
=
\frac12\langle\psi|\{\dot E,H\}|\psi\rangle
+
\langle\psi|E\dot H E|\psi\rangle.
\]

The first term is the **existential power**

\[
P_E=
\frac12\langle\psi|\{\dot E,H\}|\psi\rangle.
\]

Thus

\[
\boxed{
\frac{d\mathcal{E}}{dt}
=
P_E
+
\langle E\dot H E\rangle.
}
\]

Energy exchange with the vacuum is therefore governed by the motion of the existence projector.

---

## 9. Creation, Annihilation, and Quantum Fields

We now derive field-theoretic physics from the DMO vacuum and creation/annihilation maps.

Let \(|\Omega\rangle\) be the vacuum. For each mode \(i\), let

\[
C_i:V\to\mathcal{H}_i,
\qquad
A_i:\mathcal{H}_i\to V
\]

be creation and annihilation maps. The vacuum return law is

\[
A_iC_j=\theta_i\delta_{ij}I_V,
\]

where \(\theta_i\) is the creation–annihilation yield.

We impose the generalized exchange relation

\[
\boxed{
A_iC_j
=
\theta_i\delta_{ij}I
+
\sigma C_jA_i,
}
\]

with

\[
\sigma=
\begin{cases}
+1,&\text{bosonic/accumulative ontology},\\
-1,&\text{fermionic/exclusive ontology},\\
0,&\text{strict resource ontology}.
\end{cases}
\]

When \(\theta_i=1\), this recovers the canonical commutation or anticommutation relations.

Define normalized operators

\[
c_i=\theta_i^{-1/2}C_i,
\qquad
a_i=\theta_i^{-1/2}A_i.
\]

Then

\[
a_ic_j=\delta_{ij}I+\sigma c_ja_i.
\]

The single-mode existence projector is

\[
P_i=\theta_i^{-1}C_iA_i.
\]

Using \(A_iC_i=\theta_i I\),

\[
P_i^2
=
\theta_i^{-2}C_iA_iC_iA_i
=
\theta_i^{-2}C_i(\theta_i I)A_i
=
\theta_i^{-1}C_iA_i
=
P_i.
\]

Thus

\[
\boxed{P_i^2=P_i.}
\]

This is the physical projector onto the created one-particle sector of mode \(i\).

### 9.1 Field expansion and propagator

For a scalar field, write

\[
\Phi(x)=\sum_i\left(A_i u_i(x)+C_i u_i^\ast(x)\right),
\]

where \(u_i(x)\) are mode functions. The vacuum two-point function is

\[
\langle\Omega|\Phi(x)\Phi(y)|\Omega\rangle
=
\sum_i
\langle\Omega|A_iC_i|\Omega\rangle
u_i(x)u_i^\ast(y).
\]

Using the vacuum return law,

\[
\langle\Omega|A_iC_i|\Omega\rangle=\theta_i.
\]

Hence

\[
\boxed{
G(x,y)
=
\sum_i\theta_i u_i(x)u_i^\ast(y).
}
\]

If \(\theta_i=\theta\) is constant, then

\[
G(x,y)=\theta\,\Delta^{(+)}(x,y).
\]

Thus \(\theta\) appears physically as the field-strength residue of the propagator.

If \(\theta=\theta(x)\) varies, the free field action becomes

\[
S
=
\int d^4x\sqrt{-g}
\left[
\theta(x)g^{\mu\nu}\partial_\mu\phi^\ast\partial_\nu\phi
-
\theta(x)m^2\phi^\ast\phi
\right].
\]

The field equation is

\[
\boxed{
\partial_\mu\!\left(\theta\,\partial^\mu\phi\right)
+
\theta m^2\phi
=
0.
}
\]

Thus spacetime variation of the creation yield produces particle production and modifies propagation.

---

## 10. Existential Field Equations

Let \(\phi^A(x)\) be a matter field and let \(E^A{}_B(x)\) be an existence projector. Let \(D_\mu\) be the gauge-covariant derivative. The existential matter action is

\[
\boxed{
S_m[\phi,E]
=
\int d^4x\sqrt{-g}
\left[
g^{\mu\nu}(D_\mu\phi)^\dagger_A E^A{}_B D_\nu\phi^B
-
m^2\phi^\dagger_A E^A{}_B\phi^B
-
V(\phi^\dagger E\phi)
\right].
}
\]

The projector constraint

\[
E^2=E,
\qquad
E^\dagger=E
\]

is imposed either explicitly by Lagrange multipliers or by restricting variations to the manifold of projectors.

### 10.1 Matter equation

Varying \(\phi^\dagger\) gives

\[
\boxed{
-D_\mu\left(E D^\mu\phi\right)
-
m^2E\phi
-
V'(\phi^\dagger E\phi)E\phi
=
0.
}
\]

If

\[
D_\mu E=0,
\]

then

\[
\boxed{
E\left(
D_\mu D^\mu
+
m^2
+
V'(\phi^\dagger E\phi)
\right)\phi
=
0.
}
\]

Thus the field equation holds on the actual sector.

### 10.2 Existence equation

Let

\[
S^A{}_B
=
\frac{\delta S_m}{\delta E^B{}_A}.
\]

Explicitly,

\[
S^A{}_B
=
(D_\mu\phi)^A(D^\mu\phi)^\ast_B
-
m^2\phi^A\phi^\ast_B
-
V'(\phi^\dagger E\phi)\phi^A\phi^\ast_B.
\]

Allowed variations of a projector are tangent to the unitary orbit of projectors and may be written

\[
\delta E=[E,X]
\]

for some anti-Hermitian \(X\). Stationarity requires

\[
\operatorname{Tr}(S\delta E)=0
\]

for all such \(X\). Hence

\[
\operatorname{Tr}(S[E,X])=0
\]

for all \(X\), which implies

\[
\boxed{
[S,E]=0.
}
\]

This is the **existential field equation**:

> The existence projector must diagonalize the matter source.

In physical terms, the actual sector is precisely the sector in which the matter source is dynamically compatible.

For a free scalar field, this condition selects the on-shell actual modes. Nonactual modes are those for which the source has off-diagonal support relative to \(E\).

### 10.3 Existential stress tensor

Varying the metric gives the existential stress tensor

\[
\boxed{
T_{\mu\nu}^{(E)}
=
(D_\mu\phi)^\dagger E D_\nu\phi
+
(D_\nu\phi)^\dagger E D_\mu\phi
-
g_{\mu\nu}\mathcal{L}_m.
}
\]

Only the actual part of the field gravitates. Potential but nonactual components do not contribute to \(T_{\mu\nu}^{(E)}\) until actualized.

---

## 11. Dirac Existential Fields

For fermions, the existential action is

\[
S_D
=
\int d^4x\sqrt{-g}
\,
\bar\psi E
\left(
i\gamma^\mu D_\mu-m
\right)
\psi.
\]

Varying \(\bar\psi\) gives

\[
\boxed{
E(i\gamma^\mu D_\mu-m)\psi=0.
}
\]

Varying \(E\) gives the existence equation

\[
\boxed{
[E,\bar\psi(i\gamma^\mu D_\mu-m)\psi]=0,
}
\]

understood as an internal-endomorphism equation. Thus the Dirac equation is imposed on the actual sector, while the existence projector is determined by compatibility with the Dirac source.

---

## 12. Existential Gravity

The coarse-grained existence density

\[
\varepsilon(x)=\frac{1}{N}\operatorname{Tr}E(x)
\]

behaves as a physical scalar. We call its quanta **ontons**.

The gravitational action is

\[
\boxed{
S
=
\int d^4x\sqrt{-g}
\left[
\frac{R}{2\kappa}
+
\frac{\beta}{2}\nabla_\mu\varepsilon\nabla^\mu\varepsilon
-
U(\varepsilon)
\right]
+
S_m[\phi,E].
}
\]

Varying \(g^{\mu\nu}\) gives

\[
\boxed{
G_{\mu\nu}
=
\kappa
\left(
T_{\mu\nu}^{(m)}
+
T_{\mu\nu}^{(\varepsilon)}
\right),
}
\]

where

\[
T_{\mu\nu}^{(\varepsilon)}
=
\beta
\left(
\nabla_\mu\varepsilon\nabla_\nu\varepsilon
-
\frac12 g_{\mu\nu}\nabla_\alpha\varepsilon\nabla^\alpha\varepsilon
\right)
-
g_{\mu\nu}U(\varepsilon).
\]

Varying \(\varepsilon\) gives

\[
\boxed{
\beta\square\varepsilon
-
U'(\varepsilon)
=
\Sigma,
}
\]

where \(\Sigma\) is the matter source obtained from variation of \(S_m\) with respect to \(\varepsilon\).

Thus DMO predicts a new scalar sector coupled to geometry and matter.

---

## 13. Cosmological Existential Dynamics

In a spatially flat FLRW universe,

\[
ds^2=-dt^2+a(t)^2d\mathbf{x}^2,
\]

the Friedmann equation becomes

\[
\boxed{
H^2
=
\frac{\kappa}{3}
\left(
\rho_m+\rho_\varepsilon
\right),
}
\]

with

\[
\rho_\varepsilon
=
\frac{\beta}{2}\dot\varepsilon^2
+
U(\varepsilon).
\]

The onton equation is

\[
\boxed{
\ddot\varepsilon
+
3H\dot\varepsilon
+
\frac{1}{\beta}U'(\varepsilon)
=
\frac{1}{\beta}\Sigma.
}
\]

Creation and annihilation give a source term. For mode occupation numbers \(n_k\), the existential kinetic equation is

\[
\boxed{
\dot n_k+3Hn_k
=
\Gamma_k(\theta_k+\sigma_k n_k)
-
\alpha_k n_k.
}
\]

Here:

- \(\Gamma_k\) is the creation rate;
- \(\alpha_k\) is the annihilation rate;
- \(\theta_k\) is the vacuum creation yield;
- \(\sigma_k=+1\) gives bosonic stimulation;
- \(\sigma_k=-1\) gives Pauli blocking;
- \(\sigma_k=0\) gives linear resource creation.

This equation is a direct physical consequence of the DMO creation–annihilation algebra.

In the early universe, a large vacuum yield \(\theta_k\) can drive rapid particle production. If \(U(\varepsilon)\) has a plateau, the existence sector can also drive inflation or late-time acceleration.

---

## 14. Thermodynamic Arrow from Existence Closure

The DMO closure operator is

\[
(\Phi e)(B,s)
=
e(B,s)
\vee
\bigvee_{f:(A,t)\to(B,s)}
\left(
e(A,t)\otimes\rho(f)
\right).
\]

It is monotone and inflationary. Its least fixed point is the dynamically closed existence valuation.

In a stochastic physical representation, let \(p_i\) be existence degrees of discrete sectors and let \(K_{ij}\ge0\) be transition weights. The closure becomes

\[
p_i'
=
p_i
\vee
\sum_j K_{ij}p_j.
\]

For a smooth probabilistic limit,

\[
\dot p_i=\sum_j\left(K_{ij}p_j-K_{ji}p_i\right).
\]

If \(K\) satisfies detailed balance, the relative entropy to the fixed point decreases:

\[
\frac{d}{dt}D(p\|p_\ast)\le0.
\]

Thus the thermodynamic arrow arises from monotone ontological closure.

The physical entropy associated with the created sector is

\[
S_{\mathrm{ex}}
=
-k_B\sum_k
\left[
n_k\ln n_k
-
(1+\sigma_k n_k)\ln(1+\sigma_k n_k)
\right],
\]

with the usual bosonic, fermionic, or linear limits.

---

## 15. Observable Consequences

Existential Dynamics reduces to standard physics when

\[
E=I,
\qquad
\theta=1,
\qquad
\Gamma=0,
\qquad
\varepsilon=\text{constant}.
\]

Its new predictions are deviations from these limits.

### 15.1 Existence decay and apparent nonunitarity

If \(\Gamma\ne0\), then an initially normalized state loses actual existence:

\[
\frac{d}{dt}\langle\psi|\psi\rangle_{\mathrm{actual}}
=
-\langle\psi|\Gamma|\psi\rangle.
\]

In an interferometer, visibility decays as

\[
V(t)=\exp\left(-\frac12\int_0^t\langle\Gamma\rangle dt'\right).
\]

This mimics decoherence but is caused by annihilation into the vacuum sector.

### 15.2 Variable field-strength residue

The propagator residue is

\[
Z_i=\theta_i.
\]

If \(\theta_i\) varies slowly in time, cross sections acquire corrections

\[
\frac{\delta\sigma}{\sigma}
\approx
\delta\theta_i
\]

for external legs of species \(i\). Spectral lines, decay rates, and scattering amplitudes can therefore acquire species-dependent secular drifts.

### 15.3 Actuality-forbidden transitions

A transition operator \(T\) is physical only if

\[
E_sT=TE_t.
\]

If a candidate interaction violates the persistent core projector \(P_\Pi\), its amplitude is suppressed by

\[
\mathcal{M}_{\mathrm{forbidden}}
\sim
\langle f|(1-P_\Pi)T(1-P_\Pi)|i\rangle.
\]

Thus rare processes such as forbidden flavor transitions may be suppressed not by energy conservation alone but by persistence constraints.

### 15.4 Fifth force from the existence scalar

The onton \(\varepsilon\) mediates a Yukawa correction to Newtonian gravity:

\[
V(r)
=
-\frac{Gm_1m_2}{r}
\left(
1+\alpha e^{-m_\varepsilon r}
\right),
\]

where \(m_\varepsilon^2=U''(\varepsilon_{\mathrm{vac}})/\beta\) and \(\alpha\) depends on the matter coupling to \(\varepsilon\).

### 15.5 Cosmological particle production

The kinetic equation

\[
\dot n_k+3Hn_k
=
\Gamma_k(\theta_k+\sigma_k n_k)-\alpha_k n_k
\]

predicts nonthermal particle production from vacuum yield. In the bosonic case \(\sigma=+1\), this can lead to amplification instabilities. In the fermionic case \(\sigma=-1\), production saturates by Pauli blocking.

---

## 16. Summary of Derived Physical Laws

From DMO we have derived the following core laws.

### Law 1: Actuality constraint

Physical transitions satisfy

\[
\boxed{
E_sT=TE_t.
}
\]

### Law 2: Existence evolution

For infinitesimal transitions,

\[
\boxed{
\dot E=[L,E].
}
\]

For closed conservative systems,

\[
\boxed{
\dot E=-i[H,E].
}
\]

### Law 3: Schrödinger dynamics

On invariant actual sectors,

\[
\boxed{
i\partial_t\psi=H\psi.
}
\]

### Law 4: Gauge preservation

Local existence preservation implies

\[
\boxed{
D_\mu E=0,
\qquad
[F_{\mu\nu},E]=0.
}
\]

### Law 5: Persistence conservation

If

\[
[G,E]=0,
\]

then the associated Noether current is conserved:

\[
\boxed{
\nabla_\mu j^\mu_G=0.
}
\]

### Law 6: Creation–annihilation yield

Field residues and production rates are governed by

\[
\boxed{
A_iC_j=\theta_i\delta_{ij}+\sigma C_jA_i.
}
\]

### Law 7: Existential field equation

The existence projector diagonalizes the matter source:

\[
\boxed{
[S,E]=0.
}
\]

### Law 8: Existential gravity

The existence density obeys

\[
\boxed{
\beta\square\varepsilon-U'(\varepsilon)=\Sigma,
}
\]

and contributes to the Einstein equation.

---

## 17. Conclusion

Dynamic Mathematical Ontology is not merely a formal metaphysical framework. When interpreted in linear physical categories, its primitive notions generate a complete physical dynamics. Existence operators become projectors selecting actual sectors. Ontological transitions become Hamiltonian, gauge, and open-system evolutions. Structural persistence becomes Noether conservation. Creation and annihilation maps become quantum-field operators with a physically measurable yield \(\theta\). Coarse-grained existence density becomes a scalar sector coupled to gravity.

The resulting theory, Existential Dynamics, contains ordinary quantum mechanics and quantum field theory as the special case \(E=I\), \(\theta=1\), and no existence source. Beyond that limit, it predicts existence decay, variable propagator residues, persistence-forbidden transitions, an onton scalar, and vacuum-driven cosmological particle production.

The central physical principle is therefore:

> What exists physically is the actual sector selected by an existence operator; what evolves is that sector under existence-preserving transitions; what is created or annihilated is governed by vacuum yield laws; and what persists is the source of conservation.

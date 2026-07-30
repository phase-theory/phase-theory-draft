# Relativity 7.0 — Relativity of Quantum Reference Frames  
## Covariance for Quantum Observers and Quantum Frames

**White paper / academic preprint**

---

## Abstract

Classical relativity assumes that reference frames can be idealized as classical coordinate systems. Special relativity made the laws of physics invariant under transformations between inertial classical frames. General relativity extended this invariance to arbitrary smooth coordinate transformations. Relativity of Quantum Reference Frames extends the principle once more: the frames themselves are quantum systems, capable of superposition, entanglement, fluctuation, and backreaction. A quantum reference frame is not a coordinate chart \(x^\mu\), but a physical quantum system \(Q\) — a clock, rod, gyroscope, detector, or material reference field — relative to which other systems are described. The resulting principle of relativity is:

\[
\boxed{
\text{The laws of physics must be invariant under transformations between quantum reference frames.}
}
\]

Physical states of a closed universe satisfy constraints,

\[
\hat C_a \ket{\Psi_{\text{phys}}} = 0,
\]

and physical observables are relational,

\[
O_{A|B},
\]

meaning “the value of observable \(A\) relative to quantum system \(B\).” Coordinates, times, velocities, and localizations are no longer absolute labels. They are correlations between systems. In the classical limit, quantum reference frames decohere and become the classical frames of Einsteinian relativity. In the quantum regime, however, changes of reference frame can map ordinary states into superpositions of transformed states, alter apparent subsystem decompositions, and reveal that even the observer must be included inside the physical system. Relativity 7.0 is therefore the quantum completion of general covariance: not merely coordinate independence, but independence from any assumed classical observer or classical frame.

---

## 1. Introduction

Every relativistic theory is defined by its invariances.

Special relativity asserts that the laws of physics are invariant under Lorentz transformations between inertial frames. General relativity asserts that the laws are invariant under arbitrary smooth coordinate transformations. In both cases, however, the reference frame is treated as classical. It is a coordinate chart, a lattice of rods and clocks, or an idealized observer whose state is not itself part of the quantum system.

Quantum theory forces a deeper question:

> What happens when the reference frame is itself a quantum system?

A real observer is made of matter. A clock is a quantum system with finite energy and finite accuracy. A rod has quantum fluctuations. A gyroscope has quantum spin uncertainty. A laboratory can be placed in a superposition of positions or velocities. A gravitational detector can become entangled with the field it measures.

If the frame is quantum, then the description of a system relative to that frame must also be quantum. A transformation between frames is no longer merely a passive coordinate transformation. It is a transformation between quantum perspectives.

This motivates Relativity 7.0:

\[
\boxed{
\text{Relativity of Quantum Reference Frames.}
}
\]

Its central claim is that the covariance principle of relativity must be extended from classical frames to quantum frames. The laws of physics should not depend on which quantum system is chosen as the reference frame, just as they do not depend on which coordinate chart is chosen in general relativity.

The conceptual structure is:

\[
\text{classical coordinate frame}
\quad
\longrightarrow
\quad
\text{quantum reference system}.
\]

Accordingly,

\[
x^\mu
\quad
\longrightarrow
\quad
Q,
\]

where \(Q\) is a quantum clock, rod, or material reference field.

The resulting theory is not merely a modification of quantum mechanics. It is the synthesis of quantum theory, relationalism, and general covariance.

---

## 2. Classical Reference Frames in Relativity

### 2.1 Frames in Special Relativity

In special relativity, an inertial frame is usually represented by coordinates

\[
x^\mu = (ct, x, y, z).
\]

Two inertial frames are related by a Poincaré transformation,

\[
x'^\mu
=
\Lambda^\mu{}_\nu x^\nu
+
a^\mu,
\]

where \(\Lambda^\mu{}_\nu\) is a Lorentz transformation and \(a^\mu\) is a spacetime translation.

Physical laws are required to be covariant:

\[
\mathcal{L}[\phi(x)]
=
0
\quad
\Longleftrightarrow
\quad
\mathcal{L}'[\phi'(x')]
=
0.
\]

The frame is treated as an abstract coordinate system. It has no quantum state.

### 2.2 Frames in General Relativity

In general relativity, coordinates are arbitrary. A diffeomorphism

\[
x^\mu \mapsto x'^\mu(x)
\]

has no direct physical meaning. Physical observables must be diffeomorphism-invariant.

The metric transforms as

\[
g'_{\mu\nu}(x')
=
\frac{\partial x^\alpha}{\partial x'^\mu}
\frac{\partial x^\beta}{\partial x'^\nu}
g_{\alpha\beta}(x).
\]

But the coordinates themselves are gauge. The physical content lies in relations among fields.

General relativity therefore already contains a relational insight:

\[
\boxed{
\text{Coordinates are not physical. Relations are physical.}
}
\]

Relativity of Quantum Reference Frames radicalizes this insight. It says that even the physical systems used to define relations — clocks, rods, observers — are quantum.

---

## 3. Quantum Reference Frames

A quantum reference frame is a physical quantum system used to define relational quantities.

Examples include:

1. a quantum clock defining time,
2. a quantum rod defining position,
3. a quantum gyroscope defining orientation,
4. a quantum particle defining an origin,
5. a quantum field defining a material coordinate system,
6. a quantum detector defining a local frame.

Instead of saying:

\[
\text{the particle is at position } x,
\]

one says:

\[
\text{the particle is at position } x \text{ relative to quantum rod } Q.
\]

Instead of saying:

\[
\text{the event occurs at time } t,
\]

one says:

\[
\text{the event occurs when quantum clock } C \text{ reads } t.
\]

The frame is no longer external. It is part of the total quantum system.

Let the total Hilbert space be

\[
\mathcal{H}
=
\mathcal{H}_Q
\otimes
\mathcal{H}_S,
\]

where \(Q\) is the quantum reference frame and \(S\) is the system described relative to it.

A state relative to \(Q\) is not simply a state of \(S\). It is a conditional or relational state of \(S\) given a state of \(Q\).

Schematically,

\[
\rho_S^{(Q)}
=
\rho_{S|Q}.
\]

The superscript \((Q)\) emphasizes that the description is perspectival: it is the description from the perspective of, or relative to, the quantum frame \(Q\).

---

## 4. The Principle of Quantum Reference Frame Covariance

The central principle of Relativity 7.0 is:

\[
\boxed{
\text{Physical predictions are invariant under changes of quantum reference frame.}
}
\]

Let \(Q\) and \(Q'\) be two quantum reference frames. Let \(\rho_S^{(Q)}\) be the description of a system relative to \(Q\), and let \(\rho_{S'}^{(Q')}\) be the description relative to \(Q'\). Then there exists a transformation

\[
\mathcal{S}_{Q\to Q'}
\]

such that

\[
\rho_{S'}^{(Q')}
=
\mathcal{S}_{Q\to Q'}
\left[
\rho_S^{(Q)}
\right].
\]

For ideal frames, \(\mathcal{S}_{Q\to Q'}\) is unitary:

\[
\rho_{S'}^{(Q')}
=
\hat S_{Q\to Q'}
\rho_S^{(Q)}
\hat S_{Q\to Q'}^\dagger.
\]

For finite, noisy, or imperfect frames, it may be a more general completely positive map.

The covariance condition is:

\[
\operatorname{Tr}
\left[
\rho_S^{(Q)}
E_o^{(Q)}
\right]
=
\operatorname{Tr}
\left[
\rho_{S'}^{(Q')}
E_{o'}^{(Q')}
\right],
\]

where \(E_o^{(Q)}\) and \(E_{o'}^{(Q')}\) are the corresponding measurement operators in the two descriptions.

This is the quantum analog of classical coordinate covariance.

In classical relativity:

\[
x^\mu \to x'^\mu(x).
\]

In quantum reference frame relativity:

\[
Q \to Q'.
\]

The invariant content is not the description relative to a particular frame, but the network of relational probabilities among physical systems.

---

## 5. Constraints and the Absence of Absolute Frames

In a closed physical system, there is no external frame. The total system must be described relationally.

This is naturally expressed through constraints. Let \(\hat C_a\) be first-class constraints generating gauge transformations associated with absolute translations, rotations, boosts, or time reparametrizations. Physical states satisfy

\[
\hat C_a
\ket{\Psi_{\text{phys}}}
=
0.
\]

For example, if absolute spatial position is unphysical, the total momentum constraint is

\[
\hat C
=
\sum_i \hat P_i
\approx 0.
\]

Physical states are translationally invariant:

\[
e^{-i a \hat C/\hbar}
\ket{\Psi_{\text{phys}}}
=
\ket{\Psi_{\text{phys}}}.
\]

Absolute positions are gauge. Only relative positions are physical.

Similarly, if absolute time is unphysical, the total Hamiltonian constraint is

\[
\hat C_H
=
\hat H_{\text{total}}
\approx 0,
\]

so physical states satisfy

\[
\hat H_{\text{total}}
\ket{\Psi_{\text{phys}}}
=
0.
\]

This is the Wheeler–DeWitt-type condition familiar from canonical quantum gravity.

The appearance of constraints is not a technical inconvenience. It is the mathematical expression of relationalism.

There is no God’s-eye frame.

---

## 6. Relational Observables

If absolute coordinates are gauge, physical observables must be relational.

A relational observable has the form

\[
O_{A|B},
\]

meaning:

\[
\text{the value of } A \text{ relative to } B.
\]

For example:

\[
X_{S|R}
=
X_S - X_R
\]

is the position of system \(S\) relative to rod \(R\).

This operator commutes with the total momentum constraint:

\[
[\hat X_S - \hat X_R, \hat P_S + \hat P_R]
=
0.
\]

Thus it is a Dirac observable.

More generally, given a partial observable \(T\), such as a clock reading, and another observable \(O\), one defines a complete observable

\[
O_{(\tau)}
=
O \big|_{T=\tau}.
\]

This means:

\[
\text{the value of } O \text{ when the clock } T \text{ reads } \tau.
\]

In quantum theory, one may define conditional probabilities:

\[
P(o|\tau)
=
\frac{
\bra{\Psi_{\text{phys}}}
\left(
\ket{\tau}\bra{\tau}_T
\otimes
\Pi_o^S
\right)
\ket{\Psi_{\text{phys}}}
}{
\bra{\Psi_{\text{phys}}}
\left(
\ket{\tau}\bra{\tau}_T
\otimes
I_S
\right)
\ket{\Psi_{\text{phys}}}
},
\]

where \(\Pi_o^S\) is the projector onto outcome \(o\) of system \(S\).

This is the operational meaning of relational observables.

---

## 7. Quantum Time: The Page–Wootters Mechanism

The most important quantum reference frame is a clock.

Let the total system consist of a clock \(C\) and a system \(S\). Suppose the total Hamiltonian constraint is

\[
\left(
\hat H_C
+
\hat H_S
\right)
\ket{\Psi_{\text{phys}}}
=
0.
\]

The total state is stationary. There is no external time.

Let the clock possess states \(\ket{t}\) satisfying

\[
\hat H_C
\ket{t}
=
i\hbar
\frac{\partial}{\partial t}
\ket{t}.
\]

A physical state may be written as

\[
\ket{\Psi_{\text{phys}}}
=
\int dt\,
\ket{t}_C
\otimes
\ket{\psi(t)}_S,
\]

where

\[
i\hbar
\frac{d}{dt}
\ket{\psi(t)}_S
=
\hat H_S
\ket{\psi(t)}_S.
\]

Thus, relative to the clock reading \(t\), the system evolves according to the Schrödinger equation.

The conditional state of \(S\) given clock reading \(t\) is

\[
\rho_S(t)
=
\frac{
\operatorname{Tr}_C
\left[
\left(
\ket{t}\bra{t}_C
\otimes
I_S
\right)
\ket{\Psi_{\text{phys}}}\bra{\Psi_{\text{phys}}}
\right]
}{
P(t)
},
\]

with

\[
P(t)
=
\bra{\Psi_{\text{phys}}}
\left(
\ket{t}\bra{t}_C
\otimes
I_S
\right)
\ket{\Psi_{\text{phys}}}.
\]

For an ideal clock, this yields ordinary unitary evolution.

Thus:

\[
\boxed{
\text{Time evolution is evolution relative to a quantum clock.}
}
\]

There is no absolute time. There is only correlation between clock and system.

---

## 8. Imperfect Quantum Clocks

Real clocks are not ideal. They have finite energy, finite size, and finite accuracy.

An ideal clock would require an unbounded Hamiltonian and perfectly distinguishable time states. Real clocks approximate this only within limits.

If a clock has uncertainty \(\Delta t\), then the conditional evolution of a system may acquire decoherence or timing noise. Schematically,

\[
\rho_S(t)
\rightarrow
\int dt'\,
f(t-t')
U(t')
\rho_S(0)
U^\dagger(t'),
\]

where \(f(t-t')\) is the clock’s temporal resolution function.

The sharper the clock, the closer the evolution is to unitary Schrödinger evolution.

Quantum limits on clock accuracy include Salecker–Wigner-type bounds. A clock of mass \(M\) used for a time \(t\) has a minimum uncertainty roughly of the form

\[
\Delta t
\gtrsim
\left(
\frac{\hbar t^2}{M c^2}
\right)^{1/3}.
\]

Gravitational considerations introduce further bounds involving the Planck time,

\[
t_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^5}}.
\]

Thus, quantum reference frames are not merely conceptual. They impose physical limits on localization, synchronization, and measurement.

---

## 9. Quantum Rods and Spatial Frames

Spatial reference frames are also quantum.

Consider two particles \(S\) and \(R\), where \(R\) is used as a spatial origin. The relative position operator is

\[
\hat X_{S|R}
=
\hat X_S - \hat X_R.
\]

If \(R\) is localized with uncertainty \(\Delta X_R\), then the relative position uncertainty satisfies, for uncorrelated systems,

\[
(\Delta X_{S|R})^2
=
(\Delta X_S)^2
+
(\Delta X_R)^2.
\]

A classical rod corresponds to the limit

\[
\Delta X_R \to 0
\]

relative to the scale of interest. But this limit requires large mass, decoherence, and environmental stabilization.

A quantum rod can be in a superposition of positions. If the rod is in

\[
\ket{R}
=
\frac{1}{\sqrt{2}}
\left(
\ket{x_1}
+
\ket{x_2}
\right),
\]

then the position of \(S\) relative to \(R\) is not a single classical displacement. It is a superposition of relational configurations.

Thus, spatial coordinates become quantum relational variables.

---

## 10. Transformations Between Quantum Reference Frames

The central mathematical task is to construct transformations between descriptions relative to different quantum frames.

### 10.1 Three-Particle Example

Consider three particles \(A\), \(B\), and \(C\) on a line. Let \(A\) be used as the reference frame. The relative coordinates are

\[
q_B
=
x_B - x_A,
\]

\[
q_C
=
x_C - x_A.
\]

The Hilbert space from \(A\)’s perspective is spanned by

\[
\ket{q_B, q_C}_{BC}.
\]

Now change the reference frame from \(A\) to \(C\). The new relative coordinates are

\[
q'_A
=
x_A - x_C
=
-q_C,
\]

\[
q'_B
=
x_B - x_C
=
q_B - q_C.
\]

The quantum reference frame transformation is the unitary map

\[
\hat S_{A\to C}
=
\int dq_B\,dq_C\,
\ket{-q_C,\,q_B-q_C}_{AB}
{}_{BC}\bra{q_B,q_C}.
\]

It acts as

\[
\hat S_{A\to C}
\ket{q_B,q_C}_{BC}
=
\ket{-q_C,\,q_B-q_C}_{AB}.
\]

This is a quantum coordinate transformation.

It is not merely a relabeling of classical coordinates. It acts on quantum states and can change the apparent entanglement structure between the systems labeled as “frame” and “system.”

### 10.2 Superpositions of Frames

Suppose that in \(A\)’s frame, particle \(C\) is in a superposition:

\[
\ket{\psi}_{BC}
=
\frac{1}{\sqrt{2}}
\left(
\ket{0}_B \ket{1}_C
+
\ket{1}_B \ket{0}_C
\right).
\]

Applying \(\hat S_{A\to C}\), one obtains a state in the \(C\)-frame:

\[
\hat S_{A\to C}
\ket{\psi}_{BC}
=
\frac{1}{\sqrt{2}}
\left(
\ket{-1}_A \ket{-1}_B
+
\ket{0}_A \ket{1}_B
\right).
\]

Thus, a change of quantum reference frame can map a state into a superposition of transformed relational configurations.

This is impossible in classical relativity. Classical frames cannot be in superposition.

---

## 11. Quantum Reference Frames and Symmetry Groups

A general theory of quantum reference frames is naturally formulated using symmetry groups.

Let \(G\) be a symmetry group, such as translations, rotations, Galilean boosts, or Poincaré transformations. A system \(S\) transforms under a unitary representation

\[
U_S(g),
\qquad
g\in G.
\]

A reference frame \(Q\) is a quantum system carrying another representation

\[
U_Q(g).
\]

A classical frame corresponds to a sharply peaked state in \(Q\). A quantum frame may be in a superposition of frame orientations.

If the total state is invariant under \(G\), then

\[
\left(
U_Q(g)
\otimes
U_S(g)
\right)
\ket{\Psi_{\text{phys}}}
=
\ket{\Psi_{\text{phys}}}.
\]

The physical state contains no absolute orientation, position, or velocity.

A description relative to frame \(Q\) is obtained by conditioning on a state of \(Q\). A description relative to another frame \(Q'\) is obtained by conditioning on \(Q'\). The two descriptions are related by a quantum reference frame transformation.

The covariance condition is:

\[
P(o|Q)
=
P(o'|Q').
\]

This is the group-theoretic expression of quantum reference frame relativity.

---

## 12. Superselection Rules and Reference Frames as Resources

Quantum reference frames are closely related to superselection rules.

A superselection rule forbids coherent superpositions of different charge sectors unless a suitable reference frame is available.

For example, without a phase reference, superpositions of different particle numbers may be operationally inaccessible. With a phase reference, they become observable.

Similarly, without a spatial reference frame, superpositions of different positions relative to an external origin are not meaningful. With a quantum rod, relative superpositions become physical.

This leads to the resource-theoretic view of reference frames.

Given a symmetry group \(G\), the group-average map is

\[
\mathcal{G}(\rho)
=
\int_G dg\,
U(g)
\rho
U^\dagger(g).
\]

States invariant under this twirl contain no asymmetry and cannot serve as reference frames.

A useful reference frame must possess asymmetry:

\[
\mathcal{G}(\rho_Q)
\neq
\rho_Q.
\]

Perfect reference frames require idealized infinite resources. Finite quantum frames introduce noise and limitations.

Thus:

\[
\boxed{
\text{A reference frame is a physical resource that breaks symmetry relationally.}
}
\]

---

## 13. Quantum Reference Frames in General Relativity

In general relativity, coordinates are already understood to be unphysical. But practical calculations often introduce coordinate conditions or reference fields.

A fully relational formulation uses physical fields as coordinates.

Let \(T^A(x)\), with \(A=0,1,2,3\), be four scalar fields used as material coordinates. These may be dust fields, clock fields, or other reference matter.

One defines relational observables by

\[
\Phi(X)
=
\int d^4x\,
\sqrt{-g}
\,
\Phi(x)
\prod_{A=0}^{3}
\delta
\left(
T^A(x)-X^A
\right).
\]

This observable means:

\[
\text{the value of } \Phi \text{ at the event where the reference fields read } X^A.
\]

Classically, \(T^A(x)\) are ordinary fields. Quantum mechanically, they are operators.

Thus the coordinates \(X^A\) become quantum reference frame readings.

The metric itself may be expressed in relational coordinates. If \(x^\mu(X)\) is the inverse map defined by the reference fields, then

\[
G_{AB}(X)
=
g_{\mu\nu}(x(X))
\frac{\partial x^\mu}{\partial X^A}
\frac{\partial x^\nu}{\partial X^B}.
\]

In quantum gravity, \(G_{AB}(X)\) becomes an operator-valued relational metric.

This is the field-theoretic version of quantum reference frames.

---

## 14. Brown–Kuchař Dust and Quantum Material Frames

A particularly useful realization of material reference frames is provided by Brown–Kuchař dust.

One introduces four dust fields:

\[
T(x), \qquad Z^j(x), \quad j=1,2,3.
\]

These fields define physical coordinates:

\[
X^0 = T,
\qquad
X^j = Z^j.
\]

The dust momenta allow one to solve the Hamiltonian and diffeomorphism constraints. The true Hamiltonian generates evolution with respect to the dust time \(T\).

In the quantum theory, the dust fields become quantum reference systems. Evolution is then relational:

\[
\text{geometry evolves relative to quantum dust time } T.
\]

If the dust clock is imperfect or fluctuating, the effective evolution of geometry acquires quantum uncertainty.

This provides a concrete bridge between canonical quantum gravity and quantum reference frame theory.

---

## 15. Quantum Reference Frames and the Problem of Time

The problem of time arises because the Hamiltonian constraint of general relativity implies

\[
\hat{\mathcal{H}}
\ket{\Psi_{\text{phys}}}
=
0.
\]

There is no external time parameter.

Quantum reference frame theory resolves this by treating time as relational.

One chooses a physical clock system \(C\). The total state is stationary:

\[
\hat H_{\text{total}}
\ket{\Psi_{\text{phys}}}
=
0.
\]

But relative to the clock, subsystems evolve.

Thus:

\[
\text{global stationarity}
\quad
+
\quad
\text{relational conditioning}
\quad
\Longrightarrow
\quad
\text{local evolution}.
\]

The Schrödinger equation is not fundamental in this view. It is an emergent equation describing correlations between a quantum clock and the rest of the universe.

This is one of the deepest consequences of Relativity 7.0.

---

## 16. Quantum Lorentz Frames

Special relativity uses inertial frames related by Lorentz transformations. Quantum reference frame theory asks what happens when an inertial frame is itself quantum.

A quantum inertial frame may be in a superposition of velocities:

\[
\ket{Q}
=
\alpha \ket{v_1}
+
\beta \ket{v_2}.
\]

Relative to such a frame, another system may appear in a superposition of Lorentz-transformed states.

For scalar systems, a Lorentz transformation acts as

\[
U(\Lambda)
\ket{p}
=
\ket{\Lambda p}.
\]

For particles with spin,

\[
U(\Lambda)
\ket{p,\sigma}
=
\sum_{\sigma'}
D_{\sigma'\sigma}
\left(
W(\Lambda,p)
\right)
\ket{\Lambda p,\sigma'},
\]

where \(W(\Lambda,p)\) is the Wigner rotation.

If the boost \(\Lambda\) is controlled by a quantum frame, the Wigner rotation becomes operator-valued:

\[
W(\Lambda_Q,p).
\]

Thus spin and momentum can become entangled through a change of quantum reference frame.

This shows that quantum reference frame transformations are not merely coordinate changes. They can have genuine physical-informational consequences.

---

## 17. Quantum Reference Frames and Gravity

In gravitational physics, quantum reference frames acquire additional significance.

A local inertial frame is operationally defined by freely falling rods and clocks. If those rods and clocks are quantum, then the local inertial frame is quantum.

Consider a clock in a superposition of two heights in a gravitational field. The proper time along each branch differs:

\[
\tau_1 \neq \tau_2.
\]

If the clock has internal energy \(H_{\text{int}}\), its phase evolves as

\[
e^{-i H_{\text{int}} \tau/\hbar}.
\]

The total state becomes

\[
\frac{1}{\sqrt{2}}
\left(
\ket{\text{path}_1}
e^{-i H_{\text{int}} \tau_1/\hbar}
+
\ket{\text{path}_2}
e^{-i H_{\text{int}} \tau_2/\hbar}
\right).
\]

The path and internal clock degrees of freedom become entangled.

This is gravitational time dilation acting on a quantum reference frame.

It implies that even proper time is not a classical parameter when the clock is quantum. Proper time becomes a relational quantum variable.

---

## 18. Quantum Equivalence Principle

The equivalence principle states that locally, in a freely falling frame, physics reduces to special relativity.

Quantum reference frame theory suggests a quantum extension:

\[
\boxed{
\text{Local inertial frames may be quantum, and the laws must be covariant under transformations between them.}
}
\]

If an observer is in a superposition of free-fall trajectories, then the local inertial frame is in a superposition. Tidal effects, accelerations, and horizons may become frame-dependent quantum relational phenomena.

A full theory of quantum gravity should therefore be invariant not only under classical diffeomorphisms, but under transformations between quantum material frames.

This is the quantum generalization of Einstein’s equivalence principle.

---

## 19. Perspective-Neutral Physics

A subtle point is that quantum reference frame descriptions are perspectival, but the underlying physical state is not.

One may distinguish:

1. the perspective-neutral physical state,
2. a description relative to a chosen quantum frame.

The physical state satisfies the constraints:

\[
\hat C_a
\ket{\Psi_{\text{phys}}}
=
0.
\]

It contains all relational information.

Choosing a quantum reference frame is like choosing a gauge. It produces a description from a particular perspective.

Changing the frame changes the description but not the invariant physical content.

Thus:

\[
\boxed{
\text{Physics is perspective-neutral; descriptions are perspectival.}
}
\]

This resolves the apparent tension between observer-dependence and objectivity.

Objectivity is not agreement with a God’s-eye view. It is invariance of relational predictions under changes of quantum perspective.

---

## 20. Quantum Reference Frames and Measurement

Measurement devices are reference frames.

A measurement apparatus \(M\) records outcomes relative to its own pointer states. If \(M\) is quantum, then the measurement interaction is an interaction between systems, not between a system and an external classical observer.

A simple measurement model is

\[
\ket{\psi}_S
\ket{0}_M
\rightarrow
\sum_i c_i
\ket{a_i}_S
\ket{M_i}_M.
\]

The pointer states \(\ket{M_i}\) define a reference frame for the outcome.

If another observer \(W\) treats the combined system \(S+M\) quantum mechanically, then from \(W\)’s perspective the state may remain coherent:

\[
\sum_i c_i
\ket{a_i}_S
\ket{M_i}_M.
\]

Quantum reference frame theory provides the language for relating the friend’s description and Wigner’s description.

The consistency condition is that when the frames are compared, the relational probabilities agree.

This connects Relativity 7.0 to Wigner’s friend scenarios and relational quantum mechanics.

---

## 21. Classical Limit: Emergence of Classical Frames

Classical frames emerge when quantum reference systems become effectively classical.

This occurs when:

1. the frame has large mass or large quantum numbers,
2. its state is narrowly peaked in the relevant variables,
3. decoherence suppresses superpositions of frame orientations,
4. backreaction on the system is negligible,
5. the frame remains stable over the relevant timescale.

For a quantum rod with wavepacket width \(\Delta X_R\), the classical limit is

\[
\Delta X_R
\ll
L,
\]

where \(L\) is the length scale of interest.

For a quantum clock with timing uncertainty \(\Delta t\), the classical limit is

\[
\Delta t
\ll
T,
\]

where \(T\) is the dynamical timescale.

In this limit, the quantum reference frame behaves as a classical coordinate system.

Thus:

\[
\boxed{
\text{Classical frames are decohered, sharply peaked quantum reference systems.}
}
\]

Special and general relativity are recovered as limiting cases of Relativity 7.0.

---

## 22. Relation to Earlier Versions of Relativity

Relativity of Quantum Reference Frames is deeply connected to the preceding versions.

| Version | Central Idea |
|---|---|
| Relativity 3.0: Effective Quantum Relativity | Gravity is a low-energy quantum effective field theory |
| Relativity 4.0: Background-Independent Quantum Geometry | Geometry itself is quantum and discrete |
| Relativity 5.0: Holographic Relativity | Bulk geometry emerges from boundary entanglement |
| Relativity 6.0: Thermodynamic Relativity | Einstein equations are equations of state |
| Relativity 7.0: Quantum Reference Frames | Observers and frames are quantum systems |

The conceptual progression is:

\[
\text{relativity of inertial frames}
\rightarrow
\text{relativity of coordinates}
\rightarrow
\text{relativity of quantum geometry}
\rightarrow
\text{relativity of quantum observers}.
\]

In Relativity 7.0, the observer is no longer outside the theory. The observer is a quantum subsystem inside the universe.

This is the final operational completion of Einstein’s insight:

\[
\boxed{
\text{All physical quantities are relational.}
}
\]

---

## 23. Formal Axioms of Relativity 7.0

The theory may be organized around five axioms.

### Axiom 1: Physical Frames Are Quantum Systems

Every reference frame is represented by a quantum system \(Q\) with Hilbert space \(\mathcal{H}_Q\).

### Axiom 2: Closed Systems Are Constrained

For a closed universe, physical states satisfy

\[
\hat C_a \ket{\Psi_{\text{phys}}} = 0.
\]

### Axiom 3: Observables Are Relational

Physical observables take the form

\[
O_{A|B},
\]

meaning the value of \(A\) relative to \(B\).

### Axiom 4: Descriptions Are Perspectival

A description of the world is always relative to a chosen quantum frame \(Q\):

\[
\rho_S^{(Q)}.
\]

### Axiom 5: Physics Is Frame-Covariant

For any two quantum frames \(Q\) and \(Q'\), there exists a transformation

\[
\mathcal{S}_{Q\to Q'}
\]

such that all physical probabilities are invariant:

\[
P(o|Q)
=
P(o'|Q').
\]

These axioms define Relativity 7.0.

---

## 24. Operational Consequences

Relativity of Quantum Reference Frames has several operational consequences.

### 24.1 Frame-Dependent Superpositions

A state that is not in a superposition relative to one frame may be in a superposition relative to another.

Superposition is not absolute. It is relational.

### 24.2 Frame-Dependent Entanglement

Because changing quantum frames can change the partition between “frame” and “system,” the apparent entanglement between labeled subsystems may change.

Entanglement is not always frame-independent when the frame itself is quantum.

### 24.3 Finite-Frame Noise

Finite quantum frames introduce uncertainty. A finite clock produces timing noise. A finite rod produces localization noise. A finite gyroscope produces orientation noise.

### 24.4 Reference-Frame-Independent Encoding

Quantum information can be encoded in relational degrees of freedom that are invariant under changes of frame.

For example, spin singlets,

\[
\frac{1}{\sqrt{2}}
\left(
\ket{\uparrow}_A\ket{\downarrow}_B
-
\ket{\downarrow}_A\ket{\uparrow}_B
\right),
\]

are invariant under global rotations and can be used for communication without a shared orientation reference.

### 24.5 Quantum Communication Without Shared Frames

Protocols can be designed to be invariant under unknown translations, rotations, or phase references. This is practically important in satellite quantum communication, distributed quantum sensing, and relativistic quantum information.

---

## 25. Experimental Prospects

Relativity of Quantum Reference Frames is not merely philosophical. It is testable in regimes where reference systems are genuinely quantum.

Possible experimental arenas include:

1. matter-wave interferometry with massive clocks,
2. quantum satellites with moving reference frames,
3. entanglement distribution without shared time or phase references,
4. tests of gravitational time dilation in quantum superpositions,
5. quantum-limited clocks and rods,
6. reference-frame-independent quantum cryptography,
7. Wigner’s friend-type experiments with quantum observers,
8. quantum sensors in superposed accelerations.

No experiment has yet confirmed a breakdown of standard quantum theory due to quantum reference frames. Rather, the framework clarifies how standard quantum theory and relativity coexist when observers and frames are treated as physical quantum systems.

---

## 26. Open Problems

Several major problems remain.

### 26.1 Relativistic Quantum Reference Frames

A complete theory of quantum reference frames compatible with full relativistic quantum field theory is still under development.

### 26.2 Quantum Frames in Curved Spacetime

Local frames in curved spacetime must be defined by quantum tetrads, quantum gyroscopes, and quantum clocks. Their fluctuations may affect local measurements.

### 26.3 Quantum Gravity Constraints

In quantum gravity, the constraint algebra is complicated. Relational observables must be constructed in a way that respects the full Dirac constraint structure.

### 26.4 Infinite-Dimensional Frames

Field-theoretic reference frames involve infinite-dimensional Hilbert spaces and type-III local algebras. Standard notions of tracing over subsystems require refinement.

### 26.5 Self-Reference and Observers

A complete theory must handle observers who model themselves and other observers. This connects to Wigner’s friend scenarios, consistency of narratives, and quantum causal structure.

### 26.6 Emergence of Classical Spacetime

Classical spacetime must emerge not only from quantum geometry, but from stable networks of quantum reference frames.

---

## 27. Einsteinian Interpretation

Einstein would likely take Relativity of Quantum Reference Frames very seriously.

His entire career was guided by operational clarity. Special relativity began by analyzing what clocks and rods actually measure. General relativity deepened this by showing that coordinates have no intrinsic physical meaning.

Quantum reference frames continue this program.

They say:

\[
\text{Clocks and rods are not ideal classical objects. They are quantum systems.}
\]

Therefore, the relational lesson of general relativity must be applied to the measuring devices themselves.

Einstein would likely resist the idea that physical reality is perspectival. He sought an observer-independent reality. But Relativity 7.0 does not deny objectivity. It relocates objectivity.

Objectivity is not attachment to a preferred frame. It is invariance under changes of frame.

In that sense, Relativity 7.0 is profoundly Einsteinian.

It extends the central lesson of relativity:

\[
\boxed{
\text{The laws of physics must not depend on arbitrary choices of description.}
}
\]

The arbitrary choice is no longer merely a coordinate chart. It is a quantum observer.

---

## 28. Summary of Core Structures

### Quantum reference frame

A quantum system \(Q\) relative to which other systems are described.

### Physical constraint

\[
\hat C_a \ket{\Psi_{\text{phys}}} = 0.
\]

### Relational observable

\[
O_{A|B}
=
\text{value of } A \text{ relative to } B.
\]

### Conditional probability

\[
P(o|\tau)
=
\frac{
\bra{\Psi_{\text{phys}}}
\left(
\ket{\tau}\bra{\tau}_B
\otimes
\Pi_o^A
\right)
\ket{\Psi_{\text{phys}}}
}{
\bra{\Psi_{\text{phys}}}
\left(
\ket{\tau}\bra{\tau}_B
\otimes
I_A
\right)
\ket{\Psi_{\text{phys}}}
}.
\]

### Quantum frame transformation

\[
\rho_{S'}^{(Q')}
=
\mathcal{S}_{Q\to Q'}
\left[
\rho_S^{(Q)}
\right].
\]

### Covariance condition

\[
P(o|Q)
=
P(o'|Q').
\]

### Classical limit

\[
\Delta Q
\ll
\text{relevant physical scale},
\]

with decoherence suppressing frame superpositions.

---

## 29. Conclusion

Relativity 7.0, the Relativity of Quantum Reference Frames, is the extension of covariance to quantum observers.

It begins from a simple but radical fact: real reference frames are physical systems, and physical systems are quantum. Therefore, reference frames can be in superposition, can become entangled, can fluctuate, and can fail to be sharply defined.

The resulting theory replaces classical coordinates with quantum relational systems:

\[
x^\mu
\quad
\longrightarrow
\quad
Q.
\]

It replaces absolute observables with relational observables:

\[
O
\quad
\longrightarrow
\quad
O_{A|B}.
\]

It replaces external time with clock-relative evolution:

\[
i\hbar \frac{d}{dt}\ket{\psi(t)}
=
H\ket{\psi(t)}
\quad
\Longrightarrow
\quad
\text{evolution relative to quantum clock } C.
\]

It replaces classical covariance with quantum frame covariance:

\[
x^\mu \to x'^\mu
\quad
\Longrightarrow
\quad
Q \to Q'.
\]

The deepest statement of Relativity 7.0 is:

\[
\boxed{
\text{There is no external classical frame. Even the observer is part of the quantum system.}
}
\]

This is the quantum completion of general covariance.

It is Relativity 7.0.

---

## Appendix A: Translation-Invariant Example

Consider two particles \(S\) and \(R\) on a line. The total momentum constraint is

\[
\hat C
=
\hat P_S + \hat P_R
\approx 0.
\]

Physical states satisfy

\[
\hat C \ket{\Psi_{\text{phys}}} = 0.
\]

The relative position operator

\[
\hat X_{S|R}
=
\hat X_S - \hat X_R
\]

commutes with the constraint:

\[
[\hat X_{S|R}, \hat C]
=
[\hat X_S-\hat X_R, \hat P_S+\hat P_R]
=
i\hbar - i\hbar
=
0.
\]

Thus \(\hat X_{S|R}\) is a physical observable.

The absolute position

\[
\hat X_S
\]

does not commute with the constraint and is therefore gauge-dependent.

This simple example captures the essence of quantum reference frames: only relational quantities are physical.

---

## Appendix B: Page–Wootters Conditional Dynamics

Let

\[
\hat H_{\text{total}}
=
\hat H_C + \hat H_S.
\]

The physical state satisfies

\[
(\hat H_C+\hat H_S)
\ket{\Psi_{\text{phys}}}
=
0.
\]

Let clock states \(\ket{t}\) satisfy

\[
\hat H_C \ket{t}
=
i\hbar \partial_t \ket{t}.
\]

Expand

\[
\ket{\Psi_{\text{phys}}}
=
\int dt\,
\ket{t}_C
\otimes
\ket{\psi(t)}_S.
\]

The constraint implies

\[
i\hbar \partial_t \ket{\psi(t)}_S
=
\hat H_S \ket{\psi(t)}_S.
\]

Thus ordinary Schrödinger evolution appears conditionally, relative to the clock reading \(t\).

---

## Appendix C: Quantum Reference Frame Transformation for Three Particles

Let particles \(A,B,C\) have positions \(x_A,x_B,x_C\).

In the \(A\)-frame:

\[
q_B = x_B-x_A,
\qquad
q_C = x_C-x_A.
\]

In the \(C\)-frame:

\[
q'_A = x_A-x_C = -q_C,
\qquad
q'_B = x_B-x_C = q_B-q_C.
\]

The transformation is

\[
\hat S_{A\to C}
=
\int dq_B dq_C\,
\ket{-q_C,\,q_B-q_C}_{AB}
{}_{BC}\bra{q_B,q_C}.
\]

It satisfies

\[
\hat S_{A\to C}
\ket{q_B,q_C}_{BC}
=
\ket{-q_C,\,q_B-q_C}_{AB}.
\]

This is a unitary change of quantum reference frame.

---

## Appendix D: Relational Field Observables in General Relativity

Let \(T^A(x)\) be four scalar reference fields. Define

\[
\Phi(X)
=
\int d^4x\,
\sqrt{-g}
\,
\Phi(x)
\prod_{A=0}^{3}
\delta
\left(
T^A(x)-X^A
\right).
\]

Under a diffeomorphism, both \(\Phi(x)\) and \(T^A(x)\) transform as scalars. The composite observable \(\Phi(X)\) is diffeomorphism-invariant.

In quantum gravity, \(T^A(x)\) become quantum reference fields. The coordinates \(X^A\) are then readings of quantum material frames.

---

## Selected References

1. A. Einstein, “Zur Elektrodynamik bewegter Körper,” *Annalen der Physik* **17**, 891 (1905).  
2. A. Einstein, “Die Grundlage der allgemeinen Relativitätstheorie,” *Annalen der Physik* **49**, 769 (1916).  
3. P. A. M. Dirac, *Lectures on Quantum Mechanics* (Yeshiva University, 1964).  
4. D. N. Page and W. K. Wootters, “Evolution Without Evolution,” *Physical Review D* **27**, 2885 (1983).  
5. C. Rovelli, “Time in Quantum Gravity: An Hypothesis,” *Physical Review D* **43**, 442 (1991).  
6. C. Rovelli, “Relational Quantum Mechanics,” *International Journal of Theoretical Physics* **35**, 1637 (1996).  
7. C. Rovelli, “Partial Observables,” *Physical Review D* **65**, 124013 (2002).  
8. D. Marolf, “Observables and a Hilbert Space for Quantum Gravity,” *Classical and Quantum Gravity* **12**, 1199 (1995).  
9. J. D. Brown and K. V. Kuchař, “Dust as a Standard of Space and Time in Canonical Quantum Gravity,” *Physical Review D* **51**, 5600 (1995).  
10. S. D. Bartlett, T. Rudolph, and R. W. Spekkens, “Reference Frames, Superselection Rules, and Quantum Information,” *Reviews of Modern Physics* **79**, 555 (2007).  
11. G. Giacomini, E. Castro-Ruiz, and Č. Brukner, “Quantum Mechanics and the Covariance of Physical Laws in Quantum Reference Frames,” *Nature Communications* **10**, 494 (2019).  
12. A. Vanrietvelde, P. A. Höhn, G. Giacomini, and E. Castro-Ruiz, “A Change of Perspective: Switching Quantum Reference Frames via a Minimal Auxiliary System,” *Quantum* **4**, 225 (2020).  
13. P. A. Höhn, “The Trinity of Relational Quantum Dynamics,” *Physical Review D* **96**, 066001 (2017).  
14. R. Gambini, R. A. Porto, and J. Pullin, “A Relational Solution to the Problem of Time in Quantum Gravity,” *Foundations of Physics* **35**, 1023 (2005).  
15. H. Salecker and E. P. Wigner, “Quantum Limitations of the Measurement of Space-Time Distances,” *Physical Review* **109**, 571 (1958).  
16. Y. J. Ng and H. van Dam, “Limitation to Quantum Measurements of Space-Time Distances,” *Physical Review Letters* **72**, 3972 (1994).  
17. M. Zych, F. Costa, I. Pikovski, and Č. Brukner, “Quantum Interferometric Visibility as a Witness of General Relativistic Proper Time,” *Nature Communications* **2**, 505 (2011).  
18. I. Pikovski, M. Zych, F. Costa, and Č. Brukner, “Universal Decoherence Due to Gravitational Time Dilation,” *Nature Physics* **11**, 668 (2015).  
19. E. Wigner, “Remarks on the Mind-Body Question,” in *The Scientist Speculates*, ed. I. J. Good (1961).  
20. Č. Brukner, “On the Quantum Measurement Problem,” in *Quantum [Un]Speakables II*, ed. R. Bertlmann and A. Zeilinger (2017).

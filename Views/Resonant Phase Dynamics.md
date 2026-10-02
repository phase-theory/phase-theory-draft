# Resonant Phase Dynamics: Field Equations, Cohomological Charges, and Physical Consequences of Phase Idempotents

**Preprint — October 1, 2026**

---

## Abstract

We derive a physical theory from the cohomological framework of Resonance Theory. The central geometric datum is a phase idempotent \(P\) on a vector bundle \(E\to M\) with connection \(\nabla\). Writing \(Q=1-P\), the connection splits into a phase-preserving part \(\nabla^0\) and an odd transition one-form

\[
A=P\nabla Q+Q\nabla P.
\]

The resonance condition

\[
A\wedge A=0
\]

is promoted to a physical field equation: phase transitions are coherent precisely when their infinitesimal square vanishes. The curvature decomposition

\[
F_\nabla=F_{\nabla^0}+\Phi+\mathcal T,
\qquad
\Phi=\nabla^0 A,
\qquad
\mathcal T=A\wedge A
\]

then defines three physical fields: an even gauge field \(F_{\nabla^0}\), an odd transition field strength \(\Phi\), and a diagonal phase curvature \(\mathcal T\) measuring nonresonance. We construct a gauge-invariant action, derive the associated field equations, obtain Bianchi identities and conservation laws, analyze the linearized wave spectrum, and couple the theory to matter. The resulting framework predicts:

1. a new class of odd gauge fields mediating transitions between phases;
2. a resonance constraint \([A_\mu,A_\nu]=0\) forbidding noncommuting phase transitions;
3. cohomologically protected zero modes governed by resonance cohomology;
4. a phase Bianchi identity implying a new conservation law in resonant backgrounds;
5. a geometric obstruction to topological band structures, with the resonance defect proportional to Berry-curvature density.

In particular, for a two-band projector

\[
P=\frac12(1+\mathbf n\cdot\boldsymbol\sigma),
\qquad
|\mathbf n|=1,
\]

we show explicitly that

\[
\mathcal T_{ij}
=
-\frac{i}{2}
\bigl(\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n)\bigr)
\,\mathbf n\cdot\boldsymbol\sigma,
\]

so that the resonance defect is precisely the skyrmion/Chern density of the occupied phase. Resonance Theory therefore yields a concrete physical mechanism by which topology, phase coherence, and transition dynamics are controlled by the vanishing or nonvanishing of \(A\wedge A\).

---

## Contents

1. Phase Idempotents as Physical Variables  
2. Curvature Decomposition and Physical Interpretation  
3. Resonant Field Equations from an Action Principle  
4. Bianchi Identities and Phase Conservation Laws  
5. Linearized Resonance Waves  
6. Matter Coupling and Phase-Changing Currents  
7. Cohomological Quantization and Protected States  
8. Topological Phases and the Resonance Defect  
9. Phenomenological Consequences  
10. Conclusion  

---

## 1. Phase Idempotents as Physical Variables

Let \(M\) be a smooth \(n\)-dimensional manifold, interpreted either as spacetime or as a parameter manifold such as a Brillouin zone. Let

\[
E\to M
\]

be a complex Hermitian vector bundle with structure group \(G\subset U(r)\), and let

\[
\nabla
\]

be a connection on \(E\). Let

\[
P\in\Gamma(\operatorname{End}E)
\]

be a smooth idempotent of constant rank:

\[
P^2=P.
\]

We assume, when a Hermitian metric is fixed, that \(P\) is orthogonal:

\[
P^\dagger=P.
\]

Set

\[
Q=1-P.
\]

Then \(Q^2=Q\), \(PQ=QP=0\), and \(E\) splits as

\[
E=E_P\oplus E_Q,
\qquad
E_P=\operatorname{im}P,
\qquad
E_Q=\operatorname{im}Q.
\]

The operator \(P\) is the phase selector. Sections of \(E_P\) and \(E_Q\) represent two physical phases, sectors, or internal states: occupied/unoccupied bands, chiral/antichiral sectors, stable/unstable modes, or any other binary decomposition of the field space.

Define the phase-grading operator

\[
\tau=P-Q=2P-1.
\]

Then

\[
\tau^2=1,
\qquad
P=\frac{1+\tau}{2},
\qquad
Q=\frac{1-\tau}{2}.
\]

An endomorphism \(X\) of \(E\) is called even if it preserves phases and odd if it exchanges them:

\[
[\tau,X]=0
\quad\Longleftrightarrow\quad
X \text{ even},
\]

\[
\{\tau,X\}=0
\quad\Longleftrightarrow\quad
X \text{ odd}.
\]

The physical content of Resonance Theory begins with the decomposition of the connection into even and odd parts.

Define

\[
\nabla^0=P\nabla P+Q\nabla Q,
\]

and

\[
A=P\nabla Q+Q\nabla P.
\]

Then

\[
\nabla=\nabla^0+A.
\]

The operator \(\nabla^0\) preserves \(E_P\) and \(E_Q\), while \(A\) exchanges them. In components, relative to a local frame,

\[
A^a{}_{b\mu}
=
P^a{}_c\nabla_\mu Q^c{}_b
+
Q^a{}_c\nabla_\mu P^c{}_b.
\]

Equivalently, since \(Q=1-P\),

\[
A=-\tau\nabla P.
\]

Using \(\tau=2P-1\), one may also write

\[
A=-\frac12\tau\,d\tau
\]

when \(\nabla=d\) is the trivial connection.

The physical interpretation is:

- \(P\): phase selector or order parameter;
- \(\nabla^0\): phase-preserving gauge potential;
- \(A\): phase-transition potential;
- \(E_P,E_Q\): physical phase sectors;
- \(A\wedge A\): obstruction to coherent successive phase transitions.

The central physical postulate is that the resonant regime

\[
A\wedge A=0
\]

defines coherent phase dynamics. Nonresonance, \(A\wedge A\neq0\), measures genuine geometric frustration of phase transitions.

---

## 2. Curvature Decomposition and Physical Interpretation

Let

\[
F_\nabla=\nabla^2
\]

be the curvature of \(\nabla\). From

\[
\nabla=\nabla^0+A
\]

we obtain

\[
F_\nabla
=
(\nabla^0)^2+\nabla^0 A+A\wedge A.
\]

Define

\[
F_{\nabla^0}:=(\nabla^0)^2,
\]

\[
\Phi:=\nabla^0 A,
\]

\[
\mathcal T:=A\wedge A.
\]

Then

\[
F_\nabla
=
F_{\nabla^0}+\Phi+\mathcal T.
\]

The three terms have distinct phase parity:

- \(F_{\nabla^0}\) is even and preserves phases;
- \(\Phi\) is odd and exchanges phases;
- \(\mathcal T\) is even and measures the curvature generated by phase transitions.

In local coordinates,

\[
F_{\nabla^0}
=
\frac12 F^0_{\mu\nu}\,dx^\mu\wedge dx^\nu,
\]

\[
\Phi
=
\frac12 \Phi_{\mu\nu}\,dx^\mu\wedge dx^\nu,
\]

\[
\mathcal T
=
\frac12 \mathcal T_{\mu\nu}\,dx^\mu\wedge dx^\nu.
\]

The components are

\[
F^0_{\mu\nu}
=
\partial_\mu \Gamma^0_\nu-\partial_\nu\Gamma^0_\mu
+
[\Gamma^0_\mu,\Gamma^0_\nu],
\]

\[
\Phi_{\mu\nu}
=
\nabla^0_\mu A_\nu-\nabla^0_\nu A_\mu,
\]

\[
\mathcal T_{\mu\nu}
=
[A_\mu,A_\nu].
\]

Thus the resonance condition is

\[
\mathcal T_{\mu\nu}=0
\quad\Longleftrightarrow\quad
[A_\mu,A_\nu]=0
\quad
\forall \mu,\nu.
\]

This is a strong tensorial constraint: the phase-transition potentials must commute pointwise in their spacetime indices.

We call

\[
\Phi=\nabla^0 A
\]

the odd curvature or transition field strength, and

\[
\mathcal T=A\wedge A
\]

the phase curvature or resonance defect.

The physical meaning is as follows.

1. \(F_{\nabla^0}\) governs holonomy inside each phase.  
2. \(\Phi\) governs the failure of phase-transition fields to be locally pure gauge.  
3. \(\mathcal T\) governs the failure of two successive phase transitions to compose coherently.

The equation

\[
\mathcal T=0
\]

therefore states that phase transitions square to zero at the infinitesimal level. This is precisely the geometric condition under which the phase-changing operator defines a differential.

---

## 3. Resonant Field Equations from an Action Principle

We now derive dynamics. Let \(M\) carry a metric \(g_{\mu\nu}\), and let \(\langle\cdot,\cdot\rangle\) denote an invariant inner product on \(\operatorname{End}E\), for example

\[
\langle X,Y\rangle=-\operatorname{tr}(XY)
\]

for anti-Hermitian fields, or \(\operatorname{tr}(X^\dagger Y)\) in a unitary frame.

Consider the action

\[
S[\nabla^0,A]
=
\int_M
\left[
\frac{1}{4}\langle F_{\nabla^0},F_{\nabla^0}\rangle
+
\frac{\alpha}{4}\langle \Phi,\Phi\rangle
+
\frac{\beta}{4}\langle \mathcal T,\mathcal T\rangle
+
\frac{m^2}{2}\langle A,A\rangle
\right]
\,\mathrm{vol}_g
+
S_{\mathrm{matter}}.
\]

Here \(\alpha,\beta\ge0\) are coupling constants and \(m\) is a possible mass parameter for the transition field. In components,

\[
S
=
\int d^nx\sqrt{|g|}
\left[
\frac14 F^0_{\mu\nu}F^{0\mu\nu}
+
\frac{\alpha}{4}\Phi_{\mu\nu}\Phi^{\mu\nu}
+
\frac{\beta}{4}\mathcal T_{\mu\nu}\mathcal T^{\mu\nu}
+
\frac{m^2}{2}A_\mu A^\mu
\right]
+
S_{\mathrm{matter}},
\]

suppressing the trace or inner-product notation.

The term \(\langle\Phi,\Phi\rangle\) is the kinetic term for the odd transition field. The term \(\langle\mathcal T,\mathcal T\rangle\) penalizes nonresonance. The resonance limit may be obtained either by taking \(\beta\to\infty\) or by imposing \(\mathcal T=0\) as a constraint.

### 3.1 Variation with respect to \(A\)

Let \(A\mapsto A+\delta A\). Then

\[
\delta\Phi_{\mu\nu}
=
\nabla^0_\mu\delta A_\nu-\nabla^0_\nu\delta A_\mu,
\]

and

\[
\delta\mathcal T_{\mu\nu}
=
[\delta A_\mu,A_\nu]+[A_\mu,\delta A_\nu].
\]

The variation of the \(\Phi\)-term is

\[
\delta S_\Phi
=
\frac{\alpha}{2}
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
\Phi^{\mu\nu}\delta\Phi_{\mu\nu}
\right)
\]

\[
=
\alpha
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
\Phi^{\mu\nu}\nabla^0_\mu\delta A_\nu
\right).
\]

Integrating by parts,

\[
\delta S_\Phi
=
-\alpha
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
(\nabla^{0\mu}\Phi_{\mu\nu})\delta A^\nu
\right),
\]

assuming suitable boundary conditions.

The variation of the \(\mathcal T\)-term is

\[
\delta S_{\mathcal T}
=
\frac{\beta}{2}
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
\mathcal T^{\mu\nu}\delta\mathcal T_{\mu\nu}
\right).
\]

Using cyclicity of the trace,

\[
\delta S_{\mathcal T}
=
\beta
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
[A_\mu,\mathcal T^{\mu\nu}]\delta A_\nu
\right),
\]

up to the sign convention for the inner product.

The mass term gives

\[
\delta S_m
=
m^2
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
A^\nu\delta A_\nu
\right).
\]

If matter is present, its variation defines the odd transition current

\[
J_A^\nu
\]

by

\[
\delta S_{\mathrm{matter}}
=
\int
\sqrt{|g|}
\,\operatorname{tr}
\left(
J_A^\nu\delta A_\nu
\right).
\]

Thus the \(A\)-field equation is

\[
\boxed{
\alpha\nabla^{0\mu}\Phi_{\mu\nu}
+
\beta[A^\mu,\mathcal T_{\mu\nu}]
+
m^2 A_\nu
=
J_{A\nu}.
}
\]

In resonance,

\[
\mathcal T_{\mu\nu}=0,
\]

so the cubic self-interaction vanishes and the equation reduces to

\[
\boxed{
\alpha\nabla^{0\mu}\Phi_{\mu\nu}
+
m^2 A_\nu
=
J_{A\nu}.
}
\]

This is the dynamical equation for a coherent phase-transition field.

### 3.2 Variation with respect to \(\nabla^0\)

Let \(\nabla^0\mapsto\nabla^0+\theta\), where \(\theta\) is an even one-form. Then

\[
\delta F^0_{\mu\nu}
=
\nabla^0_\mu\theta_\nu-\nabla^0_\nu\theta_\mu,
\]

and

\[
\delta\Phi_{\mu\nu}
=
[\theta_\mu,A_\nu]-[\theta_\nu,A_\mu].
\]

The variation of the \(F_{\nabla^0}\)-term gives the usual Yang–Mills expression

\[
-\nabla^{0\mu}F^0_{\mu\nu}.
\]

The variation of the \(\Phi\)-term gives an even current generated by the odd field:

\[
\alpha[A^\mu,\Phi_{\mu\nu}].
\]

Including an even matter current \(J^0_\nu\), the phase-preserving field equation is

\[
\boxed{
\nabla^{0\mu}F^0_{\mu\nu}
+
\alpha[A^\mu,\Phi_{\mu\nu}]
=
J^0_\nu.
}
\]

Thus the odd transition field acts as a source for the even gauge field. This is a crucial physical consequence: phase transitions back-react on the internal gauge dynamics of each phase.

### 3.3 Resonant field equations

The resonant physical system is therefore

\[
\boxed{
\mathcal T_{\mu\nu}=[A_\mu,A_\nu]=0,
}
\]

\[
\boxed{
\alpha\nabla^{0\mu}\Phi_{\mu\nu}
+
m^2 A_\nu
=
J_{A\nu},
}
\]

\[
\boxed{
\nabla^{0\mu}F^0_{\mu\nu}
+
\alpha[A^\mu,\Phi_{\mu\nu}]
=
J^0_\nu.
}
\]

These equations define what we call **resonant phase dynamics**.

---

## 4. Bianchi Identities and Phase Conservation Laws

The curvature decomposition yields refined Bianchi identities.

First, since \(\Phi=\nabla^0 A\),

\[
(\nabla^0)^2A
=
F_{\nabla^0}\wedge A-A\wedge F_{\nabla^0}.
\]

Thus

\[
\boxed{
\nabla^0\Phi
=
F_{\nabla^0}\wedge A-A\wedge F_{\nabla^0}.
}
\]

In components,

\[
\nabla^0_{[\lambda}\Phi_{\mu\nu]}
=
F^0_{[\lambda\mu}A_{\nu]}
-
A_{[\lambda}F^0_{\mu\nu]}.
\]

Second, since \(\mathcal T=A\wedge A\),

\[
\nabla^0\mathcal T
=
\nabla^0(A\wedge A)
=
(\nabla^0 A)\wedge A-A\wedge(\nabla^0 A).
\]

Therefore

\[
\boxed{
\nabla^0\mathcal T
=
\Phi\wedge A-A\wedge\Phi.
}
\]

In components,

\[
\boxed{
\nabla^0_{[\lambda}\mathcal T_{\mu\nu]}
=
\Phi_{[\lambda\mu}A_{\nu]}
-
A_{[\lambda}\Phi_{\mu\nu]}.
}
\]

This is the **phase Bianchi identity**.

In a resonant background,

\[
\mathcal T=0,
\]

so

\[
\nabla^0\mathcal T=0.
\]

Hence

\[
\boxed{
\Phi\wedge A
=
A\wedge\Phi.
}
\]

In components,

\[
\boxed{
\Phi_{[\lambda\mu}A_{\nu]}
=
A_{[\lambda}\Phi_{\mu\nu]}.
}
\]

This is a new physical constraint: in a resonant phase, the odd field strength \(\Phi\) and the transition potential \(A\) commute in the wedge-matrix sense. It expresses the compatibility of phase transitions with their own field strength.

### 4.1 Gauge currents

Let \(\lambda\) be an infinitesimal phase-preserving gauge parameter:

\[
\delta_\lambda\nabla^0=-\nabla^0\lambda,
\qquad
\delta_\lambda A=[A,\lambda].
\]

The full current decomposes as

\[
J=J^0+J^A,
\]

where \(J^0\) is even and \(J^A\) is odd. Gauge invariance implies covariant conservation with respect to the full connection:

\[
\nabla^\mu J_\mu=0.
\]

Decomposing into even and odd parts gives

\[
\boxed{
\nabla^{0\mu}J^0_\mu+[A^\mu,J^A_\mu]=0,
}
\]

\[
\boxed{
\nabla^{0\mu}J^A_\mu+[A^\mu,J^0_\mu]=0.
}
\]

Thus the phase-changing current is not independently conserved; it is conserved only up to exchange with the phase-preserving sector. This is the local conservation law associated with phase dynamics.

---

## 5. Linearized Resonance Waves

Consider a trivial background

\[
\nabla^0=d,
\qquad
F_{\nabla^0}=0,
\qquad
A=0.
\]

Let

\[
A=a
\]

be small. Then

\[
\Phi_{\mu\nu}
=
\partial_\mu a_\nu-\partial_\nu a_\mu,
\]

and

\[
\mathcal T_{\mu\nu}
=
[a_\mu,a_\nu]
=
O(a^2).
\]

The linearized field equation in vacuum is

\[
\alpha\partial^\mu
\left(
\partial_\mu a_\nu-\partial_\nu a_\mu
\right)
+
m^2 a_\nu
=
0.
\]

Imposing the Lorenz-type gauge

\[
\partial^\mu a_\mu=0,
\]

we obtain

\[
\boxed{
(\Box+m^2/\alpha)a_\nu=0.
}
\]

Thus the odd transition field propagates as a massive wave when \(m\neq0\), or as a massless wave when \(m=0\).

The resonance condition is nonlinear:

\[
[a_\mu,a_\nu]=0.
\]

At linear order it is automatic, but at quadratic order it imposes a nontrivial polarization constraint.

Take a plane wave

\[
a_\mu(x)=\varepsilon_\mu e^{ik\cdot x},
\]

with constant matrix polarization \(\varepsilon_\mu\). The resonance condition gives

\[
[a_\mu,a_\nu]
=
[\varepsilon_\mu,\varepsilon_\nu]e^{2ik\cdot x}.
\]

Therefore exact resonant plane waves must satisfy

\[
\boxed{
[\varepsilon_\mu,\varepsilon_\nu]=0.
}
\]

This is a sharp physical prediction:

> Coherent phase-transition waves must have commuting internal polarizations. Noncommuting phase waves carry nonzero phase curvature \(\mathcal T\) and therefore represent nonresonant excitations.

The nonresonant energy density is

\[
\mathcal E_{\mathcal T}
=
\frac{\beta}{4}
\operatorname{tr}
\left(
[a_\mu,a_\nu][a^\mu,a^\nu]
\right).
\]

For a plane wave,

\[
\mathcal E_{\mathcal T}
\sim
\frac{\beta}{4}
\operatorname{tr}
\left(
[\varepsilon_\mu,\varepsilon_\nu]
[\varepsilon^\mu,\varepsilon^\nu]
\right)
|e^{ik\cdot x}|^4.
\]

Thus noncommuting phase polarizations are energetically penalized by the resonance defect.

---

## 6. Matter Coupling and Phase-Changing Currents

Let \(\psi\in\Gamma(E)\) be a matter field. Decompose

\[
\psi=\psi_P+\psi_Q,
\qquad
\psi_P=P\psi,
\qquad
\psi_Q=Q\psi.
\]

The covariant derivative is

\[
\nabla\psi
=
\nabla^0\psi+A\psi.
\]

Since \(A\) is odd,

\[
A\psi_P\in\Omega^1(E_Q),
\qquad
A\psi_Q\in\Omega^1(E_P).
\]

Thus \(A\) mediates transitions between the two phases.

For a scalar matter field, take

\[
S_\psi
=
\int_M
\left(
\langle\nabla\psi,\nabla\psi\rangle
-
V(\psi)
\right)
\mathrm{vol}_g.
\]

Expanding,

\[
\langle\nabla\psi,\nabla\psi\rangle
=
|\nabla^0\psi_P|^2
+
|\nabla^0\psi_Q|^2
+
|A\psi_P|^2
+
|A\psi_Q|^2
\]

\[
+
2\operatorname{Re}
\langle\nabla^0\psi_P,A\psi_Q\rangle
+
2\operatorname{Re}
\langle\nabla^0\psi_Q,A\psi_P\rangle.
\]

The last two terms are phase-transition interactions. The odd current sourced by matter is schematically

\[
J_A^\mu
=
(\nabla^{0\mu}\psi_P)^\dagger\psi_Q
+
(\nabla^{0\mu}\psi_Q)^\dagger\psi_P
+
\text{Hermitian conjugate}
+
O(A).
\]

For fermions, let

\[
S_\psi
=
\int_M
\bar\psi\,i\gamma^\mu\nabla_\mu\psi\,\mathrm{vol}_g.
\]

Then

\[
\bar\psi\,i\gamma^\mu\nabla_\mu\psi
=
\bar\psi_P i\gamma^\mu\nabla^0_\mu\psi_P
+
\bar\psi_Q i\gamma^\mu\nabla^0_\mu\psi_Q
\]

\[
+
\bar\psi_P i\gamma^\mu A_\mu\psi_Q
+
\bar\psi_Q i\gamma^\mu A_\mu\psi_P.
\]

Thus the phase-changing fermionic current is

\[
\boxed{
J_A^\mu
=
\bar\psi_P\gamma^\mu\psi_Q
+
\bar\psi_Q\gamma^\mu\psi_P.
}
\]

The resonant field equation becomes

\[
\alpha\nabla^{0\mu}\Phi_{\mu\nu}
+
m^2 A_\nu
=
g J_{A\nu},
\]

where \(g\) is a coupling constant.

This has the physical interpretation of a Proca or Maxwell-type equation for phase transitions:

> Phase-changing matter currents generate odd curvature; in the resonant regime, that curvature propagates without generating phase curvature \(\mathcal T\).

---

## 7. Cohomological Quantization and Protected States

The resonance condition \(A\wedge A=0\) implies that the operator

\[
Q_R:=A\wedge
\]

is nilpotent:

\[
Q_R^2
=
A\wedge A\wedge
=
\mathcal T\wedge
=
0.
\]

Thus \((\Omega^\bullet(M,E),Q_R)\) is a cochain complex. Its cohomology is the resonance cohomology

\[
H_R^\bullet(M,E,P)
=
\frac{\ker Q_R}{\operatorname{im}Q_R}.
\]

On a compact Riemannian manifold, assuming ellipticity of the relevant resonance complex, choose the formal adjoint \(Q_R^\dagger\) and define the resonance Hamiltonian

\[
\boxed{
H_R
=
Q_RQ_R^\dagger+Q_R^\dagger Q_R.
}
\]

This is the resonance Laplacian. Its zero modes are harmonic resonance forms:

\[
\ker H_R
\cong
H_R^\bullet(M,E,P).
\]

Therefore resonance cohomology classes correspond to physical zero-energy states.

This yields a cohomological quantum mechanics:

1. physical states are \(Q_R\)-closed;
2. trivial states are \(Q_R\)-exact;
3. protected ground states are resonance cohomology classes.

Define the resonance Witten index

\[
\boxed{
\chi_R
=
\sum_k(-1)^k\dim H_R^k(M,E,P).
}
\]

Equivalently,

\[
\chi_R
=
\operatorname{Str}e^{-tH_R}.
\]

Because \(\chi_R\) is cohomological, it is invariant under smooth deformations preserving resonance. Thus:

> Resonance cohomology produces topologically protected phase modes.

Nonresonance breaks this cohomological structure. If

\[
\mathcal T\neq0,
\]

then

\[
Q_R^2=\mathcal T\wedge\neq0.
\]

The operator \(Q_R\) no longer defines a differential, and the protected zero modes can be lifted. In physical language, \(\mathcal T\) is a coherence-destroying potential.

This suggests a general principle:

\[
\text{phase coherence}
\quad\Longleftrightarrow\quad
\mathcal T=0
\quad\Longleftrightarrow\quad
\text{cohomological protection}.
\]

---

## 8. Topological Phases and the Resonance Defect

We now derive an explicit physical consequence for two-band systems. Let \(M\) be a Brillouin zone or parameter space, and let \(E=M\times\mathbb C^2\) be the trivial rank-two bundle with trivial connection \(d\). Let

\[
P(k)=\frac12(1+\mathbf n(k)\cdot\boldsymbol\sigma),
\qquad
|\mathbf n|=1,
\]

be a rank-one projector, where \(\boldsymbol\sigma=(\sigma_1,\sigma_2,\sigma_3)\) are the Pauli matrices.

Then

\[
Q=\frac12(1-\mathbf n\cdot\boldsymbol\sigma),
\]

and

\[
\tau=2P-1=\mathbf n\cdot\boldsymbol\sigma.
\]

For the trivial connection,

\[
A=-\frac12\tau\,d\tau.
\]

Since

\[
d\tau=(\partial_i\mathbf n\cdot\boldsymbol\sigma)\,dk^i,
\]

and \(\mathbf n\cdot\partial_i\mathbf n=0\), we have

\[
A_i
=
-\frac12
(\mathbf n\cdot\boldsymbol\sigma)
(\partial_i\mathbf n\cdot\boldsymbol\sigma)
=
-\frac{i}{2}
(\mathbf n\times\partial_i\mathbf n)\cdot\boldsymbol\sigma.
\]

Now compute

\[
\mathcal T_{ij}=[A_i,A_j].
\]

Using

\[
[\mathbf a\cdot\boldsymbol\sigma,\mathbf b\cdot\boldsymbol\sigma]
=
2i(\mathbf a\times\mathbf b)\cdot\boldsymbol\sigma,
\]

we obtain

\[
\mathcal T_{ij}
=
-\frac{i}{2}
\left(
(\mathbf n\times\partial_i\mathbf n)
\times
(\mathbf n\times\partial_j\mathbf n)
\right)
\cdot\boldsymbol\sigma.
\]

The vector identity

\[
(\mathbf n\times\mathbf a)\times(\mathbf n\times\mathbf b)
=
\bigl(\mathbf n\cdot(\mathbf a\times\mathbf b)\bigr)\mathbf n
\]

gives

\[
\boxed{
\mathcal T_{ij}
=
-\frac{i}{2}
\bigl(
\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n)
\bigr)
\,\mathbf n\cdot\boldsymbol\sigma.
}
\]

The scalar density

\[
\chi_{ij}
=
\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n)
\]

is the skyrmion density. In two dimensions, its integral is proportional to the degree of the map \(\mathbf n:M\to S^2\).

Thus:

\[
\boxed{
\mathcal T=0
\quad\Longleftrightarrow\quad
\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n)=0.
}
\]

Resonance is equivalent to the local vanishing of the skyrmion density.

Moreover, the Berry curvature of the occupied line bundle \(E_P\) is proportional to the same density. With standard conventions,

\[
F_P
\sim
\frac{i}{2}
\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n)
\,dk^i\wedge dk^j.
\]

Therefore

\[
\boxed{
\operatorname{tr}(P\mathcal T)
\propto
\mathbf n\cdot(\partial_i\mathbf n\times\partial_j\mathbf n).
}
\]

The resonance defect is precisely the local Chern density of the occupied phase.

Consequently:

1. If \(P\) is globally resonant with respect to the trivial connection, then the occupied band has vanishing local Berry curvature.  
2. A nonzero Chern number obstructs resonance.  
3. Topological phase transitions correspond to the appearance or disappearance of resonance defects.

This gives a new geometric interpretation of topological phases:

> Topological band obstruction is a nonresonance defect of the phase idempotent.

Equivalently, a system can restore resonance only by introducing a compensating phase-transition gauge field or by closing the gap so that \(P\) becomes singular.

---

## 9. Phenomenological Consequences

The preceding derivations imply several physical effects.

### 9.1 Phase decoherence from nonresonance

Let a state initially lie in \(E_P\). Transport around an infinitesimal loop with area element \(dx^\mu\wedge dx^\nu\) produces an even holonomy in the \(P\)-sector proportional to

\[
\mathcal T^P_{\mu\nu}
=
P\mathcal T_{\mu\nu}P.
\]

If \(\mathcal T^P\neq0\), repeated phase transitions generate an internal geometric phase. The corresponding decoherence rate is controlled by

\[
\Gamma_{\mathrm{dephase}}
\sim
\|\mathcal T^P\|.
\]

Thus resonance protects phase coherence.

### 9.2 Selection rule for phase-transition waves

Exact resonant waves satisfy

\[
[\varepsilon_\mu,\varepsilon_\nu]=0.
\]

Therefore, in a resonant medium, only commuting phase-transition polarizations propagate without generating phase curvature. Noncommuting polarizations produce a nonzero resonance defect and are expected to scatter into even curvature modes or decay into resonant harmonics.

### 9.3 Protected zero modes

If

\[
H_R^k(M,E,P)\neq0,
\]

then the theory possesses protected zero modes. These modes cannot be removed by perturbations preserving the resonance condition. The integer

\[
\chi_R=\sum_k(-1)^k\dim H_R^k
\]

is a physical invariant of the resonant phase.

### 9.4 Topological obstruction in band systems

For a two-band Bloch projector,

\[
\mathcal T\neq0
\]

precisely where the skyrmion density is nonzero. Hence resonance flow,

\[
\frac{\partial P}{\partial t}
=
-\operatorname{grad}\int_M |\mathcal T|^2,
\]

can reduce local curvature but cannot remove a nonzero Chern number without singularities. Topological phase transitions are therefore accompanied by resonance defects or gap closings.

### 9.5 Odd gauge bosons

The field \(A_\mu\) behaves as an odd gauge boson mediating transitions between phases. Its resonant self-interaction is governed by

\[
\beta[A^\mu,\mathcal T_{\mu\nu}].
\]

In a resonant background this term vanishes. Thus resonant phase-transition bosons are weakly self-interacting, while nonresonant excitations acquire cubic and quartic self-couplings.

---

## 10. Conclusion

Starting from the cohomological structure of Resonance Theory, we have derived a physical framework in which phase idempotents define dynamical sectors of a field theory. The connection decomposes into a phase-preserving gauge field and an odd phase-transition field. The resonance condition

\[
A\wedge A=0
\]

becomes a physical law demanding coherent phase transitions.

The resulting theory predicts a new tensorial field equation,

\[
[A_\mu,A_\nu]=0,
\]

a refined Bianchi identity,

\[
\nabla^0\mathcal T=\Phi\wedge A-A\wedge\Phi,
\]

and a cohomological classification of protected states through resonance cohomology. In two-band systems, the resonance defect is exactly the Berry-curvature density, showing that topological obstruction is a manifestation of nonresonance.

The central physical principle is therefore:

\[
\boxed{
\text{Coherent phase dynamics}
\quad\Longleftrightarrow\quad
\text{nilpotent phase transitions}
\quad\Longleftrightarrow\quad
A\wedge A=0.
}
\]

Resonance Theory thus provides a unified geometric language for phase transitions, topological obstruction, gauge dynamics, and cohomologically protected physical states.

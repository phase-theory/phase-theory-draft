# CONSTRAINT MECHANICS  
## The General Mathematics of Admissible Constraints in Relativity Mechanics

---

## 1. CORE PRINCIPLE

In Relativity Mechanics, physical descriptions contain redundant structure.  
Constraints are the mathematical expressions of that redundancy.

\[
\boxed{
\text{Every admissibility theory contains constraints.}
}
\]

A constraint does not merely restrict the state space.  
It also generates the admissibility transformations that relate physically equivalent descriptions.

\[
\boxed{
C_a(z)\approx 0
}
\]

Here \(z\) denotes a point in phase space, and \(\approx\) means equality on the physical constraint surface.

---

## 2. GENERAL CONSTRAINT SCHEMA

Given a phase space

\[
(\Gamma,\omega),
\]

a constraint system is a collection of functions

\[
C_a:\Gamma\to\mathbb R.
\]

The constraint surface is

\[
\boxed{
\Sigma=\{z\in\Gamma\mid C_a(z)=0\}.
}
\]

If the constraints are first-class, their Hamiltonian flows generate admissibility transformations.

For a smeared constraint

\[
G[\epsilon]=\int d^dx\,\epsilon^a(x)C_a(x),
\]

the infinitesimal admissibility transformation of any phase-space function \(F\) is

\[
\boxed{
\delta_\epsilon F=\{F,G[\epsilon]\}.
}
\]

The physical phase space is the quotient of the constraint surface by these gauge orbits:

\[
\boxed{
\Gamma_{\rm phys}=\Sigma/G.
}
\]

Physical observables are functions constant along the constraint orbits:

\[
\boxed{
\{O,C_a\}\approx 0.
}
\]

These are Dirac observables.

---

## 3. CONSTRAINT PIPELINE

\[
\boxed{
\text{Description space } \Gamma
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Constraints } C_a\approx 0
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Constraint surface } \Sigma
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Quotient by admissibility orbits } \Sigma/G
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Physical phase space } \Gamma_{\rm phys}
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Dirac observables } \{O,C_a\}\approx 0
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Physical dynamics on } \Gamma_{\rm phys}
}
\]

---

## 4. FIRST-CLASS AND SECOND-CLASS CONSTRAINTS

### First-Class Constraints

A constraint is first-class if its Poisson bracket with all constraints vanishes on the constraint surface:

\[
\boxed{
\{C_a,C_b\}=f_{ab}{}^{c}C_c.
}
\]

First-class constraints generate admissibility transformations.

Examples:

\[
\text{Gauss constraint},
\quad
\text{diffeomorphism constraint},
\quad
\text{Hamiltonian constraint}.
\]

---

### Second-Class Constraints

A constraint is second-class if the constraint matrix

\[
\Delta_{\alpha\beta}=\{\chi_\alpha,\chi_\beta\}
\]

is invertible on the constraint surface.

Second-class constraints do not generate gauge transformations. They reduce the phase space directly.

Quantization requires the Dirac bracket:

\[
\boxed{
\{F,G\}_D
=
\{F,G\}
-
\{F,\chi_\alpha\}
\Delta^{\alpha\beta}
\{\chi_\beta,G\}.
}
\]

After imposing

\[
\chi_\alpha=0,
\]

the Dirac bracket becomes the physical bracket.

---

## 5. CONSTRAINTS AS ADMISSIBILITY GENERATORS

In Relativity Mechanics, constraints are the infinitesimal form of admissibility.

If \(G\) is the admissibility group with Lie algebra \(\mathfrak g\), then the constraints may be understood as components of a moment map

\[
\mu:\Gamma\to\mathfrak g^*.
\]

For each \(\xi\in\mathfrak g\),

\[
C_\xi=\langle\mu,\xi\rangle.
\]

The physical phase space is the symplectic reduction

\[
\boxed{
\Gamma_{\rm phys}=\mu^{-1}(0)/G.
}
\]

Thus:

\[
\boxed{
\text{Constraints are the local generators of admissibility orbits.}
}
\]

---

## 6. GENERAL DYNAMICS WITH CONSTRAINTS

The total Hamiltonian is

\[
\boxed{
H_T=H_c+\lambda^a C_a,
}
\]

where \(H_c\) is the canonical Hamiltonian and \(\lambda^a\) are Lagrange multipliers.

Evolution is

\[
\dot F=\{F,H_T\}.
\]

For gauge-invariant observables \(O\),

\[
\{O,C_a\}\approx 0,
\]

so the arbitrary multipliers drop out:

\[
\boxed{
\dot O\approx\{O,H_c\}.
}
\]

Thus physical evolution is independent of gauge choice.

---

# 7. MAJOR EXAMPLES OF ADMISSIBILITY CONSTRAINTS

---

## 7.1 GAUSS CONSTRAINT

### Theory

Electromagnetism and Yang–Mills gauge theory.

### Electromagnetic Gauss Law

Canonical variables:

\[
A_i,\quad E^i.
\]

The Gauss constraint is

\[
\boxed{
\mathcal G(x)=\partial_i E^i(x)-\rho(x)\approx 0.
}
\]

It generates \(U(1)\) gauge transformations.

For a gauge parameter \(\alpha(x)\),

\[
G[\alpha]=\int d^3x\,\alpha(x)\mathcal G(x).
\]

Then

\[
\boxed{
\delta A_i=\{A_i,G[\alpha]\}=\partial_i\alpha,
}
\]

\[
\boxed{
\delta E^i=\{E^i,G[\alpha]\}=0.
}
\]

---

### Non-Abelian Gauss Law

For Yang–Mills theory with gauge group \(G\),

\[
\boxed{
\mathcal G^a(x)=D_i E^{ia}(x)-\rho^a(x)\approx 0.
}
\]

Here

\[
D_i E^{ia}
=
\partial_i E^{ia}
+
g f^a{}_{bc}A_i^b E^{ic}.
\]

The Gauss constraint generates local gauge transformations:

\[
\boxed{
\delta A_i^a=D_i\alpha^a.
}
\]

Physical states must be gauge singlets.

\[
\boxed{
\hat{\mathcal G}^a(x)|\Psi_{\rm phys}\rangle=0.
}
\]

---

### Physical Meaning

The Gauss constraint enforces that local internal frame rotations are admissibility transformations.

\[
\boxed{
\text{Gauss constraint }=\text{ internal gauge admissibility.}
}
\]

---

## 7.2 DIFFEOMORPHISM CONSTRAINT

### Theory

General relativity, canonical gravity, geometrodynamics.

### ADM Variables

Spatial metric:

\[
h_{ij}.
\]

Conjugate momentum:

\[
\pi^{ij}.
\]

The diffeomorphism or momentum constraint is

\[
\boxed{
\mathcal H_i(x)=-2D_j\pi_i{}^j(x)\approx 0.
}
\]

Smeared with a shift vector \(N^i\),

\[
\boxed{
D[\vec N]=\int d^3x\,N^i(x)\mathcal H_i(x).
}
\]

It generates spatial diffeomorphisms on the hypersurface.

For any spatial tensor field \(F\),

\[
\boxed{
\delta F=\{F,D[\vec N]\}=\mathcal L_{\vec N}F.
}
\]

In particular,

\[
\boxed{
\delta h_{ij}=\mathcal L_{\vec N}h_{ij},
}
\]

\[
\boxed{
\delta\pi^{ij}=\mathcal L_{\vec N}\pi^{ij}.
}
\]

---

### Physical Meaning

The diffeomorphism constraint says that spatial coordinate transformations are not physical changes. They are changes of description.

\[
\boxed{
\text{Diffeomorphism constraint }=\text{ spatial coordinate admissibility.}
}
\]

---

## 7.3 HAMILTONIAN CONSTRAINT

### Theory

Reparametrization-invariant systems, general relativity, canonical quantum gravity.

### Relativistic Particle Example

For a relativistic particle, the canonical Hamiltonian vanishes, and the dynamics is generated by the constraint

\[
\boxed{
C=\frac12(p^\mu p_\mu+m^2)\approx 0.
}
\]

This constraint generates reparametrizations of the worldline.

The physical trajectory is independent of the arbitrary proper-time parameter.

---

### General Relativity

In ADM gravity, the Hamiltonian or scalar constraint is

\[
\boxed{
\mathcal H_\perp
=
16\pi G\,G_{ijkl}\pi^{ij}\pi^{kl}
-
\frac{\sqrt{h}}{16\pi G}R^{(3)}
+
\mathcal H_{\rm matter}
\approx 0.
}
\]

The DeWitt supermetric is

\[
\boxed{
G_{ijkl}
=
\frac{1}{2\sqrt{h}}
\left(
h_{ik}h_{jl}
+
h_{il}h_{jk}
-
h_{ij}h_{kl}
\right).
}
\]

Smeared with a lapse function \(N\),

\[
\boxed{
H[N]=\int d^3x\,N(x)\mathcal H_\perp(x).
}
\]

The Hamiltonian constraint generates normal deformations of the spatial hypersurface, corresponding to refoliations of spacetime.

---

### Physical Meaning

The Hamiltonian constraint says that the choice of time slicing is not physical.

\[
\boxed{
\text{Hamiltonian constraint }=\text{ temporal refoliation admissibility.}
}
\]

---

# 8. GENERAL RELATIVITY CONSTRAINT ALGEBRA

The full set of gravitational constraints is

\[
\boxed{
\mathcal H_\perp(x)\approx 0,
\qquad
\mathcal H_i(x)\approx 0.
}
\]

Define smeared constraints:

\[
H[N]=\int d^3x\,N\mathcal H_\perp,
\]

\[
D[\vec N]=\int d^3x\,N^i\mathcal H_i.
\]

Their algebra is the hypersurface deformation algebra:

\[
\boxed{
\{D[\vec N],D[\vec M]\}
=
D[\mathcal L_{\vec N}\vec M].
}
\]

\[
\boxed{
\{D[\vec N],H[M]\}
=
H[\mathcal L_{\vec N}M].
}
\]

\[
\boxed{
\{H[N],H[M]\}
=
D\left[
h^{ij}(N\partial_jM-M\partial_jN)
\right].
}
\]

This algebra encodes the admissibility structure of four-dimensional spacetime diffeomorphisms.

\[
\boxed{
\text{Gravity is the theory whose admissibility algebra is spacetime diffeomorphism invariance.}
}
\]

---

# 9. CONSTRAINTS AND OBSERVABLES

A physical observable must be constant along admissibility orbits.

For first-class constraints \(C_a\),

\[
\boxed{
\{O,C_a\}\approx 0.
}
\]

Such observables are called Dirac observables.

Examples:

\[
\text{Wilson loops},
\quad
\text{relational field values},
\quad
\text{diffeomorphism-invariant correlators},
\quad
\text{gauge-invariant charges}.
\]

In gauge theory:

\[
\boxed{
W_R(C)=\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right)
}
\]

is a Dirac observable because it is gauge invariant.

In gravity, local fields are not Dirac observables by themselves. They must be relationally completed.

For example, using scalar clock fields \(T^A\),

\[
\boxed{
O_{\phi,T}(\tau)=\phi\big|_{T=\tau}.
}
\]

This is invariant under diffeomorphisms.

\[
\boxed{
\text{Relational observables are Dirac observables in generally covariant theories.}
}
\]

---

# 10. CONSTRAINTS AND THE PROBLEM OF TIME

In generally covariant theories, the Hamiltonian is a constraint:

\[
\boxed{
H[N,N^i]
=
\int d^3x
\left(
N\mathcal H_\perp
+
N^i\mathcal H_i
\right)
\approx 0.
}
\]

For a Dirac observable \(O\),

\[
\dot O=\{O,H\}\approx 0.
\]

This appears to imply that nothing evolves.

Relativity Mechanics resolves this by interpreting evolution relationally.

Physical evolution is not flow with respect to an external coordinate time. It is correlation between physical observables.

\[
\boxed{
O(\tau)=O\big|_{T=\tau}.
}
\]

The physical trajectory is an orbit trajectory in the reduced phase space.

\[
\boxed{
\text{Time emerges from relational change among Dirac observables.}
}
\]

---

# 11. QUANTUM CONSTRAINT MECHANICS

In quantum theory, constraints become operator conditions.

## 11.1 Dirac Quantization

Promote constraints to operators:

\[
C_a\mapsto \hat C_a.
\]

Physical states satisfy

\[
\boxed{
\hat C_a|\Psi_{\rm phys}\rangle=0.
}
\]

Physical observables satisfy

\[
\boxed{
[\hat O,\hat C_a]\approx 0.
}
\]

The physical Hilbert space is

\[
\boxed{
\mathcal H_{\rm phys}
=
\ker \hat C_a
\big/
\text{null states}.
}
\]

---

## 11.2 Anomaly Freedom

The quantum constraint algebra must close:

\[
\boxed{
[\hat C_a,\hat C_b]|\Psi_{\rm phys}\rangle
=
i\hbar f_{ab}{}^{c}\hat C_c|\Psi_{\rm phys}\rangle.
}
\]

If an anomalous term appears,

\[
[\hat C_a,\hat C_b]
=
i\hbar f_{ab}{}^{c}\hat C_c
+
\mathcal A_{ab},
\]

then the admissibility structure is broken at the quantum level.

\[
\boxed{
\text{Anomaly cancellation is quantum constraint consistency.}
}
\]

---

## 11.3 BRST Quantization

For gauge theories, introduce ghosts \(c^a\), antighosts \(\bar c_a\), and a BRST charge \(Q_{\rm BRST}\).

The BRST operator satisfies

\[
\boxed{
Q_{\rm BRST}^2=0.
}
\]

Physical states are BRST cohomology classes:

\[
\boxed{
Q_{\rm BRST}|\Psi_{\rm phys}\rangle=0,
}
\]

with equivalence

\[
\boxed{
|\Psi\rangle\sim|\Psi\rangle+Q_{\rm BRST}|\Lambda\rangle.
}
\]

Physical observables are BRST-closed modulo BRST-exact terms:

\[
\boxed{
[Q_{\rm BRST},\hat O\}=0,
\qquad
\hat O\sim\hat O+[Q_{\rm BRST},\hat\Lambda\}.
}
\]

Thus the physical observable algebra is

\[
\boxed{
\mathcal O_{\rm phys}=H^\bullet(Q_{\rm BRST}).
}
\]

---

# 12. CONSTRAINT MECHANICS IN RELATIVITY MECHANICS

Constraint Mechanics is the general theory of admissible state selection.

In Relativity Mechanics:

\[
\mathcal R=(\Omega,G,\triangleright,I).
\]

Constraints appear when the admissibility group \(G\) is generated locally.

The general structure is:

\[
\boxed{
\text{Admissibility group }G
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Lie algebra }\mathfrak g
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Constraints }C_\xi,\ \xi\in\mathfrak g
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Constraint surface }\Sigma
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Gauge orbits generated by }C_\xi
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Physical phase space }\Sigma/G.
}
\]

Thus:

\[
\boxed{
\text{Constraint Mechanics is the infinitesimal mathematics of admissibility.}
}
\]

---

# 13. SUMMARY TABLE OF MAJOR CONSTRAINTS

| Constraint | Theory | Equation | Generates | Physical Meaning |
|---|---|---|---|---|
| Gauss constraint | Electromagnetism / Yang–Mills | \(\partial_iE^i-\rho\approx0\) or \(D_iE^{ia}-\rho^a\approx0\) | Local gauge transformations | Internal frame admissibility |
| Diffeomorphism constraint | General relativity | \(\mathcal H_i=-2D_j\pi_i{}^j\approx0\) | Spatial diffeomorphisms | Spatial coordinate admissibility |
| Hamiltonian constraint | General relativity / reparametrization-invariant systems | \(\mathcal H_\perp\approx0\) | Refoliations / time reparametrizations | Temporal admissibility |
| Supersymmetry constraint | Supergravity | \(\mathcal S_\alpha\approx0\) | Local supersymmetry transformations | Fermionic frame admissibility |
| Conformal constraint | Conformal gravity / shape dynamics | Trace/ conformal constraint | Local scale transformations | Scale admissibility |

---

# 14. KEY TAKEAWAYS

\[
\boxed{
\text{Constraints define the admissible state space.}
}
\]

\[
\boxed{
\text{First-class constraints generate admissibility transformations.}
}
\]

\[
\boxed{
\text{Physical observables are constant on constraint orbits.}
}
\]

\[
\boxed{
\text{The physical phase space is the quotient } \Sigma/G.
}
\]

\[
\boxed{
\text{Hamiltonian, Gauss, and diffeomorphism constraints are special cases of one general structure.}
}
\]

\[
\boxed{
\text{Constraint Mechanics is the universal mathematics of admissible constraints in Relativity Mechanics.}
}
\]

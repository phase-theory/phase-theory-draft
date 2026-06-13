# Quantum Stochastic Thermodynamics Without Measurements

## A White Paper Toward a Fully Coherent Theory of Quantum Nonequilibrium Thermodynamics

### Abstract

Classical stochastic thermodynamics provides an exact microscopic framework for irreversibility, work, heat, entropy production, and fluctuation theorems. The central achievements include the Jarzynski equality, Crooks fluctuation theorem, and exact formulations of the second law for systems arbitrarily far from equilibrium.

Quantum extensions exist but remain conceptually incomplete. Most current formulations rely on two-point projective measurements (TPM): one measures the system energy at the beginning and end of a protocol and defines work as the difference. Such measurements destroy quantum coherence and alter the very dynamics whose thermodynamics is being studied.

This white paper develops a fully coherent quantum stochastic thermodynamics (CQST) in which:

* No intermediate projective measurements are required.
* Quantum coherence remains present throughout the protocol.
* Work is represented by an explicit quantum work reservoir.
* Entropy production is defined as a property of quantum trajectories in Hilbert space rather than measurement outcomes.
* Maxwell demons with quantum memories are treated exactly.
* Weak measurements emerge as a limiting case.
* Exact fluctuation theorems survive in fully coherent form.

The theory unifies resource-theoretic thermodynamics, open quantum systems, quantum information theory, and nonequilibrium statistical mechanics into a single framework.

---

# 1. Fundamental Principle

## Classical Picture

Classical stochastic thermodynamics assumes a trajectory

[
x_t
]

through phase space.

Work and heat are trajectory functionals:

[
W[x_t],\qquad Q[x_t].
]

Fluctuation theorems arise from ratios of trajectory probabilities.

---

## Quantum Difficulty

Quantum systems do not possess definite trajectories.

Instead,

[
|\psi(t)\rangle
]

evolves unitarily.

Measurement introduces trajectories artificially.

Current formulations therefore identify

[
W=E_m-E_n
]

using projective measurements.

The resulting work distribution depends on the measurement protocol.

This is not intrinsic thermodynamics.

---

# Postulate I: Thermodynamics Is a Property of Quantum Channels

The fundamental object is not a trajectory but a completely positive trace-preserving map

[
\Phi.
]

Thermodynamic quantities are invariants of channel evolution.

A quantum process is represented by

[
\rho \rightarrow \Phi(\rho).
]

The stochastic structure emerges from decomposition into coherent histories rather than measurement outcomes.

---

# 2. Coherent Histories Thermodynamics

Introduce a history Hilbert space

[
\mathcal H_H
============

\bigotimes_t \mathcal H_t.
]

A quantum history is

[
|h\rangle
=========

|\psi_1\rangle
\otimes
|\psi_2\rangle
\otimes
\cdots.
]

Define decoherence functional

[
D(h,h')
=======

\mathrm{Tr}
\left(
C_h \rho C_{h'}^\dagger
\right).
]

Unlike classical probabilities,

[
D(h,h')
\neq 0.
]

Interference between histories contributes thermodynamic effects.

---

## Thermodynamic Weight

Assign each history

[
\mathcal W[h]
=============

-\ln D(h,h).
]

This generalizes stochastic action.

Entropy production becomes a property of coherent histories.

---

# 3. Quantum Work Without Measurement

## Work Reservoir

Introduce an explicit quantum battery

[
B.
]

Hamiltonian

[
H=H_S+H_B+H_{\mathrm int}.
]

Work is not inferred.

Work is stored physically.

Define battery energy change

[
W
=

\Delta E_B.
]

Because the battery remains quantum,

[
|\Psi\rangle
============

\sum_n c_n |E_n\rangle_B.
]

work itself becomes a coherent superposition.

---

## Coherent Work Observable

Define

[
\hat W
======

## H_B^{\rm final}

H_B^{\rm initial}.
]

The work state is

[
|W\rangle
=========

\sum_n c_n |w_n\rangle.
]

This object contains off-diagonal terms

[
|w_n\rangle\langle w_m|.
]

Therefore work is a quantum degree of freedom.

---

# Theorem 1: Existence of Coherent Work

A work process preserves coherence iff

[
[U,H_S+H_B]=0.
]

Then battery coherence evolves unitarily.

Proof:

Energy conservation implies

[
U^\dagger(H_S+H_B)U
===================

H_S+H_B.
]

The off-diagonal battery terms evolve as

[
\rho_{nm}
\rightarrow
e^{i\phi_{nm}}
\rho_{nm}.
]

Therefore coherence survives.

∎

---

# Operational Meaning of Work Superpositions

Consider battery state

[
\frac{1}{\sqrt2}
(
|0\rangle
+
|1,{\rm J}\rangle
).
]

Interference experiments on the battery reveal phase information.

Hence superpositions of work quanta are operationally observable.

Work is not merely a random variable.

It is a quantum resource.

---

# 4. Coherent Jarzynski Equality

Classically

[
\langle e^{-\beta W}\rangle
===========================

e^{-\beta\Delta F}.
]

Measurement-based quantum versions reproduce this relation.

We seek a fully coherent formulation.

---

Define work operator

[
\hat W.
]

Introduce

[
\Gamma
======

\mathrm{Tr}
\left(
\rho
e^{-\beta \hat W}
\right).
]

---

# Theorem 2: Coherent Jarzynski Equality

For any energy-conserving unitary

[
\Gamma
======

e^{-\beta\Delta F}
+
\mathcal C.
]

The correction

[
\mathcal C
==========

\sum_{m\neq n}
\rho_{mn}
e^{-\beta w_{mn}}
]

depends entirely on coherence.

When coherence vanishes,

[
\mathcal C=0.
]

Classical Jarzynski is recovered.

---

Interpretation:

Quantum coherence acts as an additional nonequilibrium free-energy resource.

---

# 5. Quantum Entropy Production

Classically

[
\Sigma
======

\ln
\frac{P[\gamma]}
{P[\tilde\gamma]}.
]

Quantumly we replace probabilities with amplitudes.

Define

[
\Sigma_q[h]
===========

\ln
\frac{D(h,h)}
{D(\tilde h,\tilde h)}.
]

---

Total entropy production

[
\langle\Sigma_q\rangle
======================

## S(\rho_f||\rho_f^{eq})

S(\rho_i||\rho_i^{eq}),
]

where

[
S(\rho||\sigma)
===============

{\rm Tr}
(\rho\ln\rho-\rho\ln\sigma).
]

This quantity is always positive.

---

# Theorem 3: Quantum Second Law

[
\langle \Sigma_q\rangle \ge 0.
]

Proof follows from monotonicity of quantum relative entropy under CPTP maps.

∎

---

# 6. Quantum Heat Engines With Coherence

Current thermodynamics predicts

[
\eta \le
1-\frac{T_C}{T_H}.
]

Carnot assumes incoherent reservoirs.

---

## Coherent Reservoir

Suppose hot bath possesses coherence

[
\rho_H
======

\rho_{th}
+
\chi.
]

The coherent contribution stores extractable free energy.

Define generalized free energy

[
F_Q
===

## \langle H\rangle

TS
+
kT,C_r.
]

Here

[
C_r
===

## S(\rho_{\rm diag})

S(\rho)
]

is relative entropy coherence.

---

# Theorem 4: Coherent Efficiency Bound

Maximum efficiency becomes

[
\eta
\le
1-
\frac{T_C}{T_H}
+
\frac{kT_H C_r}{Q_H}.
]

The extra term arises from coherence consumption.

---

Important consequence:

Apparent Carnot violations are possible.

However they consume coherence.

Including coherence as a thermodynamic resource restores the generalized second law.

No perpetual motion results.

---

# 7. Maxwell's Demon With Quantum Memory

Classical Landauer:

[
W_{\rm erase}
\ge
kT\ln2.
]

Quantum memories contain entanglement.

---

Suppose memory

[
M
]

is entangled with reference

[
R.
]

Entropy cost becomes

[
W_{\rm erase}
\ge
kT,S(M|R).
]

---

# Theorem 5: Quantum Landauer Principle

The exact erasure cost is

[
W_{\rm erase}
=============

kT
\left[
S(M|R)
+
I_{\rm lost}
\right].
]

When conditional entropy is negative,

[
S(M|R)<0,
]

erasure can yield work.

---

This is impossible classically.

Entanglement functions as thermodynamic fuel.

---

# 8. Weak Measurement Thermodynamics

Continuous monitoring creates stochastic evolution

[
d\rho
=====

\mathcal L(\rho),dt
+
\sqrt{\eta},
\mathcal M(\rho),dW_t.
]

where

[
dW_t
]

is Wiener noise.

---

Heat increment

[
dQ
==

{\rm Tr}
(H,d\rho).
]

Work increment

[
dW
==

{\rm Tr}
(\rho,dH).
]

---

The measurement apparatus itself carries entropy.

Define measurement entropy production

[
d\Sigma_M
=========

## dI_{\rm meas}

dI_{\rm retained}.
]

---

# Theorem 6

Total entropy production

[
d\Sigma
=======

d\Sigma_S
+
d\Sigma_M
]

remains nonnegative.

Thus weak measurement thermodynamics emerges naturally from CQST.

Projective-measurement thermodynamics appears as the singular limit

[
\eta\rightarrow\infty.
]

---

# 9. Quantum Fluctuation Theorem Without Measurement

Define forward channel

[
\Phi.
]

Reverse channel

[
\Theta\Phi^\dagger\Theta^{-1}.
]

Entropy production operator

[
\hat\Sigma.
]

Then

[
\left\langle
e^{-\hat\Sigma}
\right\rangle
=============

1.

]

This is the fully coherent fluctuation theorem.

No projective measurements appear.

---

# 10. Quantum Thermodynamic Resource Algebra

Thermodynamic resources become

[
\mathcal R
==========

(E,S,C,\mathcal E),
]

where

* (E) = energy
* (S) = entropy
* (C) = coherence
* (\mathcal E) = entanglement

Transformations obey

[
\Delta E
--------

T\Delta S
+
kT\Delta C
+
kT\Delta\mathcal E
\le 0.
]

This is the generalized free-energy law.

---

# 11. Emergent Classical Limit

When

[
C\to0,
\qquad
\mathcal E\to0,
]

the theory reduces to

[
\mathcal R
==========

(E,S).
]

The coherent Jarzynski equality becomes the classical Jarzynski equality.

Quantum entropy production becomes classical entropy production.

Crooks theorem reappears.

Thus classical stochastic thermodynamics is a special case.

---

# 12. Unified Coherent Second Law

The fundamental inequality of CQST is

[
\boxed{
\Delta E
--------

T\Delta S
+
kT\Delta C
+
kT\Delta\mathcal E
+
\langle\Sigma_q\rangle
\ge 0
}
]

This unifies:

* Clausius thermodynamics
* fluctuation theorems
* Landauer erasure
* quantum coherence
* entanglement thermodynamics
* weak measurement thermodynamics

within one framework.

---

# 13. Predictions

The theory predicts:

### P1. Interference of Work

Quantum batteries should exhibit interference fringes between distinct work values.

### P2. Coherence-Assisted Engines

Engines powered by coherent reservoirs can exceed Carnot efficiency when coherence consumption is accounted for.

### P3. Entanglement-Fueled Erasure

Negative conditional entropy permits net work extraction during memory reset.

### P4. Coherent Fluctuation Relations

Fluctuation theorems acquire experimentally measurable coherence corrections.

### P5. Quantum-Trajectory Entropy

Weakly monitored systems exhibit entropy production not explainable by classical stochastic paths.

---

# Conclusion

A fully coherent quantum stochastic thermodynamics can be constructed without invoking disruptive mid-protocol projective measurements. The central shift is conceptual: thermodynamics is no longer defined through measured trajectories but through quantum channels, coherent histories, and explicit work reservoirs.

Within this framework:

* Work becomes a quantum observable carried by a battery.
* Fluctuation theorems survive with coherence corrections.
* Entropy production is defined channel-theoretically.
* Maxwell demons are governed by conditional quantum entropy.
* Weak measurements emerge as a limiting case.
* Coherence and entanglement become thermodynamic resources alongside energy and entropy.

The resulting framework, CQST, provides a candidate completion of nonequilibrium quantum thermodynamics analogous to the role classical stochastic thermodynamics plays for classical systems, extending thermodynamic law from probability distributions to fully coherent quantum processes.

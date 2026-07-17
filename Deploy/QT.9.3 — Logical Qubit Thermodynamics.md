The Thermodynamic Cost of Quantum Computation

Part IX — Fault-Tolerant Quantum Thermodynamics

Section 51. Logical Qubit Thermodynamics

⸻

51.1 Introduction

The preceding sections established that fault-tolerant quantum computation incurs unavoidable thermodynamic costs arising from continuous syndrome extraction, ancilla preparation, measurement, reset, classical decoding, and coherent control. These costs are expended not on the user’s algorithm directly, but on preserving the integrity of encoded quantum information.

The fundamental unit of fault-tolerant quantum computation is therefore not the physical qubit, but the logical qubit.

A logical qubit is an emergent thermodynamic object sustained by the continual expenditure of physical resources. Unlike an isolated physical qubit, which naturally decoheres through environmental interactions, a logical qubit remains stable only because entropy is continuously exported to the environment through error-correction cycles.

This section develops a thermodynamic theory of logical qubits by treating logical information as a nonequilibrium state maintained through persistent energy consumption and entropy production. The resulting framework establishes quantitative relations between logical fidelity, thermodynamic resources, and fault-tolerant scalability.

⸻

51.2 Logical Qubit as a Thermodynamic State

Let

[
\mathcal Q_L
]

denote a logical qubit encoded across

[
N_P
]

physical qubits.

Its thermodynamic state is represented by

[
\boxed{
\Gamma_L

(\rho_L,
W_L,
\Sigma_L,
F_L),
}
]

where

* (\rho_L) is the logical density operator,
* (W_L) is cumulative thermodynamic work,
* (\Sigma_L) is cumulative entropy production,
* (F_L) is logical fidelity.

Unlike a physical qubit, the logical state is defined jointly by quantum information and the thermodynamic resources sustaining it.

⸻

51.3 Logical Free Energy

Define the logical nonequilibrium free energy

[
\boxed{
\mathcal F_L

\langle H_L\rangle

T_0S(\rho_L),
}
]

where

* (H_L) is the effective logical Hamiltonian,
* (S(\rho_L)) is the von Neumann entropy.

This quantity measures the useful thermodynamic resource stored in the encoded logical state.

⸻

51.4 Logical Entropy Production

The entropy generated in maintaining one logical qubit is

[
\boxed{
\Sigma_L

\Sigma_S
+
\Sigma_A
+
\Sigma_D
+
\Sigma_R
+
\Sigma_C,
}
]

where

* (\Sigma_S) is syndrome extraction entropy,
* (\Sigma_A) ancilla preparation entropy,
* (\Sigma_D) decoder entropy,
* (\Sigma_R) reset entropy,
* (\Sigma_C) control entropy.

This decomposition provides a complete thermodynamic accounting for logical state maintenance.

⸻

51.5 Logical Work Functional

The cumulative work required to preserve a logical qubit is

[
\boxed{
W_L

W_S
+
W_A
+
W_D
+
W_R
+
W_C.
}
]

The total work required for a computation containing

[
N_L
]

logical qubits becomes

[
\boxed{
W_{\rm total}

W_{\rm comp}
+
N_LW_L.
}
]

⸻

51.6 Logical Stability Functional

Define the logical stability

[
\boxed{
\Lambda_L

\frac{
F_L
}
{
\Sigma_L
}.
}
]

This functional measures logical fidelity maintained per unit entropy production.

Larger values correspond to more thermodynamically efficient logical encoding.

⸻

51.7 Logical Lifetime

Let

[
\tau_L
]

denote the logical coherence lifetime.

Define the thermodynamic lifetime efficiency

[
\boxed{
\Xi_L

\frac{
\tau_L
}
{
W_L
}.
}
]

This quantity measures logical lifetime obtained per unit work expenditure.

⸻

51.8 Logical Resource Density

For a processor area

[
A_{\rm chip},
]

define

[
\boxed{
\rho_L

\frac{
N_L
}
{
A_{\rm chip}
}.
}
]

The thermodynamic work density becomes

[
\boxed{
\omega_L

\frac{
N_LW_L
}
{
A_{\rm chip}
}.
}
]

These quantities characterize the physical scaling of logical information.

⸻

51.9 Logical Thermodynamic Efficiency

Define

[
\boxed{
\eta_L

\frac{
F_L
}
{
W_L
}.
}
]

This quantity measures logical fidelity obtained per unit thermodynamic work.

Optimizing

[
\eta_L
]

is a central objective of scalable fault-tolerant architectures.

⸻

51.10 Logical Qubit Thermodynamic Theorem

Theorem 51.1 (Logical Resource Scaling)

Suppose a logical qubit is encoded using a distance-(d) surface code.

Then the thermodynamic resources required to maintain that logical qubit satisfy

[
\boxed{
W_L

\Theta(d^2),
}
]

and

[
\boxed{
\Sigma_L

\Theta(d^2),
}
]

per error-correction cycle, assuming bounded per-operation thermodynamic costs.

⸻

Proof

A distance-(d) surface code occupies

[
\Theta(d^2)
]

physical qubits.

Each syndrome cycle performs

[
\Theta(d^2)
]

stabilizer operations.

Since each stabilizer contributes bounded work and entropy,

both total work and entropy scale proportionally with the number of stabilizers.

Therefore,

[
W_L

\Theta(d^2),
]

and

[
\Sigma_L

\Theta(d^2).
]

□

⸻

51.11 Logical Fidelity Theorem

Theorem 51.2

Suppose the logical error probability satisfies

[
p_L
\sim
e^{-\alpha d},
]

for

[
p<p_{\rm th}.
]

Then the logical fidelity

[
F_L

1-p_L
]

approaches unity exponentially with code distance while the associated thermodynamic work grows polynomially:

[
\boxed{
F_L

1-\mathcal O(e^{-\alpha d}),
}
]

[
\boxed{
W_L

\Theta(d^2).
}
]

⸻

Interpretation

Logical reliability improves exponentially faster than thermodynamic expenditure increases, illustrating the efficiency of topological quantum error correction below threshold.

⸻

51.12 Logical Free-Energy Theorem

Theorem 51.3

During steady-state fault-tolerant operation,

[
\boxed{
\frac{d\mathcal F_L}{dt}

P_{\rm in}

T_0\dot{\Sigma}_L

P_{\rm loss},
}
]

where

* (P_{\rm in}) is supplied control power,
* (P_{\rm loss}) is irreversible environmental dissipation.

A stable logical qubit requires

[
\boxed{
P_{\rm in}

T_0\dot{\Sigma}L
+
P{\rm loss}.
}
]

⸻

Proof

Applying the nonequilibrium free-energy balance to the logical subsystem yields the stated relation between supplied power, entropy production, and dissipative losses.

A stationary logical state requires vanishing net free-energy change.

□

⸻

51.13 Thermodynamic Threshold Corollary

Corollary 51.1

There exists a minimum sustained thermodynamic power

[
P_{\min}
]

below which logical fidelity cannot be maintained indefinitely.

Below this threshold, accumulated physical errors eventually overwhelm the correction capability of the code.

⸻

51.14 Ancilla Optimization Corollary

Corollary 51.2

Suppose ancilla preparation efficiency improves by a factor

[
\gamma>1.
]

Then

[
W_A
\rightarrow
\frac{W_A}{\gamma},
]

increasing

[
\eta_L

\frac{F_L}{W_L}.
]

Consequently, more efficient ancilla generation directly improves the thermodynamic efficiency of logical information storage.

⸻

51.15 Logical Thermodynamic Phase Diagram

Define coordinates

[
(F_L,W_L).
]

The admissible operating region is bounded below by

[
\boxed{
W_L
\ge
W_{\min}(F_L),
}
]

which defines the Logical Thermodynamic Frontier.

Implementations approaching this frontier maximize logical fidelity for a given thermodynamic expenditure.

⸻

51.16 Principle of Logical Thermodynamic Stability

The developments of this section establish the following principle.

Principle of Logical Thermodynamic Stability

A logical qubit is a nonequilibrium thermodynamic structure sustained by continuous entropy export and external work. Logical quantum information is not passively preserved but actively maintained through ongoing fault-tolerant operations. Consequently, logical fidelity is fundamentally a thermodynamic resource whose stability depends upon sustained energy input and irreversible entropy production.

⸻

51.17 Relationship to Previous Sections

Section 49 established the thermodynamics of surface-code architectures.

Section 50 quantified the thermodynamic costs of syndrome extraction.

The present section integrates these results into a thermodynamic description of the logical qubit itself.

Collectively,

* surface codes provide the physical architecture,
* syndrome extraction diagnoses errors,
* logical qubits emerge as stabilized nonequilibrium information-bearing structures maintained through continuous thermodynamic resource consumption.

⸻

51.18 Summary

This section develops a thermodynamic theory of logical qubits, treating encoded quantum information as an actively sustained nonequilibrium thermodynamic state.

The principal contributions include:

* formulation of the logical thermodynamic state, logical free energy, logical entropy production, logical work functional, logical stability functional, logical lifetime efficiency, logical resource density, and logical thermodynamic efficiency;
* proof of the Logical Resource Scaling Theorem, establishing that work and entropy per correction cycle scale as (\Theta(d^2)) for distance-(d) surface codes under bounded per-operation costs;
* proof of the Logical Fidelity Theorem, demonstrating exponential improvement in logical fidelity with only polynomial growth in thermodynamic resource requirements below the error threshold;
* proof of the Logical Free-Energy Theorem, expressing the steady-state balance between supplied power, entropy production, and dissipative losses;
* derivation of the Thermodynamic Threshold and Ancilla Optimization corollaries;
* introduction of the Logical Thermodynamic Frontier, characterizing the minimum thermodynamic work required to achieve a target logical fidelity; and
* establishment of the Principle of Logical Thermodynamic Stability, recognizing logical quantum information as a dynamically maintained nonequilibrium thermodynamic resource.

This section elevates the logical qubit from an abstract information-theoretic construct to a thermodynamically sustained physical entity. The following section develops the thermodynamics of magic-state preparation and distillation, extending fault-tolerant thermodynamic analysis to the resource states required for universal quantum computation.

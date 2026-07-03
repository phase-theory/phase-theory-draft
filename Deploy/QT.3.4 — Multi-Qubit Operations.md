The Thermodynamic Cost of Quantum Computation

Part III — Thermodynamics of Quantum Gates

Section 16. Multi-Qubit Operations

⸻

16.1 Introduction

While single-qubit gates govern the local evolution of individual quantum degrees of freedom, the computational advantage of quantum algorithms arises primarily from multi-qubit operations that generate nonclassical correlations. Controlled operations, entangling gates, and collective interactions enable interference across exponentially large Hilbert spaces, but they also introduce additional thermodynamic costs absent from isolated qubit dynamics.

Unlike single-qubit gates, multi-qubit operations require interaction Hamiltonians that couple distinct quantum subsystems. These interactions generate correlated energy exchange, collective entropy production, synchronization overhead, and control complexity. Consequently, the thermodynamic cost of a multi-qubit gate cannot generally be expressed as the sum of independent single-qubit costs.

This section develops a general thermodynamic theory of multi-qubit operations, establishing energetic accounting rules for interacting quantum systems and introducing interaction-specific thermodynamic invariants.

⸻

16.2 Composite Hilbert Space

Consider a register of

[
N
]

qubits.

The computational Hilbert space is

[
\boxed{
\mathcal H_N

\bigotimes_{i=1}^{N}
\mathbb C^2,
}
]

with dimension

[
\boxed{
\dim(\mathcal H_N)

2^N.
}
]

The computational state is

[
\rho_N
\in
\mathcal D(\mathcal H_N).
]

As

[
N
]

increases, the thermodynamic resource landscape grows exponentially.

⸻

16.3 Multi-Qubit Hamiltonian

The total Hamiltonian is decomposed as

[
\boxed{
H

\sum_{i=1}^{N}
H_i
+
H_{\mathrm{int}},
}
]

where

* (H_i) denotes local qubit Hamiltonians,
* (H_{\mathrm{int}}) describes inter-qubit coupling.

The interaction Hamiltonian generates correlated quantum dynamics and constitutes the principal source of additional thermodynamic cost.

⸻

16.4 Controlled Interaction Gates

A general two-qubit gate is represented by

[
\boxed{
U

e^{-iH\tau/\hbar}.
}
]

Representative examples include

* Controlled-NOT (CNOT),
* Controlled-Z (CZ),
* iSWAP,
* Controlled-Phase,
* Mølmer–Sørensen gates,
* Cross-resonance gates.

Although logically unitary,

their implementation requires simultaneous control of multiple quantum subsystems.

⸻

16.5 Interaction Energy

The interaction energy is

[
\boxed{
E_{\mathrm{int}}

\operatorname{Tr}
(\rho
H_{\mathrm{int}}).
}
]

Unlike single-qubit gates,

[
E_{\mathrm{int}}
\neq
0.
]

This quantity measures the energy temporarily stored in quantum correlations during gate execution.

⸻

16.6 Work of Collective Control

The external work supplied is

[
\boxed{
W_N

\int_0^\tau
\operatorname{Tr}
\left(
\rho
\frac{\partial H}{\partial t}
\right)
dt.
}
]

Substituting

[
H

\sum_i
H_i
+
H_{\mathrm{int}},
]

gives

[
\boxed{
W_N

\sum_i
W_i
+
W_{\mathrm{int}},
}
]

where

[
W_{\mathrm{int}}
]

is the additional work required to establish inter-qubit coupling.

⸻

16.7 Interaction Free Energy

The computational free energy becomes

[
F

E

TS.
]

Separating interaction contributions,

[
\boxed{
F

\sum_i
F_i
+
F_{\mathrm{int}}.
}
]

The interaction free energy represents computational resources stored in collective quantum dynamics.

⸻

16.8 Correlation Entropy

For two subsystems,

define

[
\boxed{
I(A:B)

S(A)
+
S(B)

S(AB),
}
]

the quantum mutual information.

This quantity measures total correlations established during gate execution.

The associated entropy production is

[
\boxed{
\Sigma_{\mathrm{corr}}

\Delta I(A:B).
}
]

Correlation entropy is unique to multi-qubit computation.

⸻

16.9 Cooperative Thermodynamic Cost

The total thermodynamic cost of a multi-qubit gate is

[
\boxed{
\mathcal C_N

\sum_i
\mathcal C_i
+
\mathcal C_{\mathrm{coop}},
}
]

where

[
\mathcal C_{\mathrm{coop}}
]

is the cooperative interaction cost.

This term includes

* synchronization,
* interaction control,
* correlated noise,
* timing overhead,
* collective calibration.

It has no analogue in isolated qubit operations.

⸻

16.10 Interaction Efficiency

Define

[
\boxed{
\eta_{\mathrm{int}}

\frac{F_{\mathrm{int}}}
{W_{\mathrm{int}}}.
}
]

Properties include

[
0
<
\eta_{\mathrm{int}}
\le
1.
]

Higher interaction efficiency corresponds to greater utilization of supplied work in generating useful quantum correlations.

⸻

16.11 Scaling with Register Size

For an

[
N
]

-qubit interaction,

the implementation work scales as

[
\boxed{
W_N

N W_1
+
W_{\mathrm{pair}}
+
W_{\mathrm{global}},
}
]

where

* (W_1) is local gate work,
* (W_{\mathrm{pair}}) represents pairwise interactions,
* (W_{\mathrm{global}}) accounts for collective synchronization.

This decomposition separates local and cooperative energetic contributions.

⸻

16.12 Interaction Heat

Heat generated during multi-qubit operations is

[
\boxed{
Q_N

\sum_i
Q_i
+
Q_{\mathrm{corr}},
}
]

where

[
Q_{\mathrm{corr}}
]

originates from irreversible interaction processes.

Examples include

* correlated dephasing,
* cross-talk,
* imperfect decoupling,
* residual coupling.

⸻

16.13 Interaction Entropy

The entropy generated by a multi-qubit gate is

[
\boxed{
\Sigma_N

\sum_i
\Sigma_i
+
\Sigma_{\mathrm{corr}}.
}
]

Correlation entropy represents a genuinely many-body thermodynamic contribution.

Its magnitude increases with interaction complexity.

⸻

16.14 Interaction Exergy

The useful computational resource stored in interactions is

[
\boxed{
X_{\mathrm{int}}

F_{\mathrm{int}}

F_{\mathrm{eq}}.
}
]

The irreversible destruction of interaction exergy is

[
\Delta X_{\mathrm{int}}

T
\Sigma_{\mathrm{corr}}.
]

Thus every dissipative interaction reduces future computational capability.

⸻

16.15 Multi-Qubit Thermodynamic Tensor

We introduce the Interaction Thermodynamic Tensor

[
\boxed{
\Lambda_{\mu\nu}

\begin{pmatrix}
W_N &
J_i\
J_i &
\Pi_{ij}
\end{pmatrix},
}
]

where

* (W_N) is interaction work density,
* (J_i) denotes correlated energy flux,
* (\Pi_{ij}) represents interaction entropy stress.

The tensor describes the transport of thermodynamic resources through interacting quantum subsystems.

⸻

16.16 Cooperative Cost Theorem

Theorem 16.1

For every nontrivial interacting quantum gate,

[
\boxed{
W_N
\ge
\sum_i
W_i.
}
]

Equality holds if and only if

[
H_{\mathrm{int}}

]

Proof

The total Hamiltonian satisfies

[
H

\sum_i
H_i
+
H_{\mathrm{int}}.
]

Since

[
W_N

\int
\operatorname{Tr}
\left(
\rho
\frac{\partial H}{\partial t}
\right)
dt,
]

we obtain

[
W_N

\sum_i
W_i
+
W_{\mathrm{int}}.
]

Physical interaction control requires non-negative supplied work,

[
W_{\mathrm{int}}
\ge
0.
]

Therefore

[
W_N
\ge
\sum_i
W_i.
]

Equality occurs only when interaction control is absent,

[
H_{\mathrm{int}}=0.
]

□

⸻

16.17 Interaction Complexity Vector

Define

[
\boxed{
\mathbf I_N

(
W_N,
Q_N,
\Sigma_N,
F_{\mathrm{int}},
X_{\mathrm{int}},
I(A:B)
).
}
]

This vector completely characterizes the thermodynamic resources associated with interacting quantum gates.

Unlike circuit depth,

it captures the energetic consequences of many-body quantum dynamics.

⸻

16.18 Generalized Energy Accounting Law

The first law for multi-qubit gates becomes

[
\boxed{
W_N

\Delta F
+
T\Sigma_N
+
Q_{\mathrm{parasitic}}
+
W_{\mathrm{coop}},
}
]

where

* (\Delta F) is useful computational free-energy change,
* (T\Sigma_N) is irreversible entropy production,
* (Q_{\mathrm{parasitic}}) represents implementation losses,
* (W_{\mathrm{coop}}) denotes cooperative interaction work.

This equation extends the single-qubit accounting law to correlated quantum systems.

⸻

16.19 Summary

This section generalizes the thermodynamic theory of quantum gates from isolated qubits to interacting quantum registers. Multi-qubit operations introduce fundamentally new energetic phenomena arising from interaction Hamiltonians, collective control, correlated entropy production, and cooperative resource consumption.

The principal developments include:

* formulation of composite Hilbert-space thermodynamics;
* decomposition of the total Hamiltonian into local and interaction components;
* derivation of interaction work, heat, free energy, exergy, and correlation entropy;
* definition of cooperative thermodynamic cost and interaction efficiency;
* construction of the Interaction Thermodynamic Tensor and Interaction Complexity Vector;
* proof of the Cooperative Cost Theorem, demonstrating that interacting quantum gates require thermodynamic resources beyond the sum of their constituent single-qubit operations;
* and establishment of the generalized first law for multi-qubit gate implementations.

These results reveal that the thermodynamic cost of quantum computation is intrinsically collective. Interaction energy and correlated resource flows become dominant contributors as quantum processors scale, laying the groundwork for the next section, which develops a quantitative theory of the thermodynamic cost of entanglement generation and its implications for quantum computational advantage.

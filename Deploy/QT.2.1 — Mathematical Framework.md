The Thermodynamic Cost of Quantum Computation

Part II — Mathematical Framework

Section 7. Hilbert-Space Thermodynamics

⸻

7.1 Introduction

Quantum computation is conventionally formulated entirely within the framework of Hilbert space. A computational state is represented by a vector

[
|\psi\rangle \in \mathcal H,
]

or, more generally, by a density operator

[
\rho\in\mathcal D(\mathcal H),
]

where

[
\mathcal D(\mathcal H)

{\rho\ge0,;
\operatorname{Tr}\rho=1}.
]

While this mathematical structure completely specifies the logical state of a quantum computer, it does not uniquely determine its thermodynamic state.

Two quantum computers may occupy identical logical states while differing in

* internal energy,
* heat exchanged,
* entropy generated,
* free energy,
* work extracted,
* exergy remaining.

Consequently, Hilbert space alone is insufficient for describing physical computation.

We therefore construct an enlarged mathematical framework called Hilbert-Space Thermodynamics, in which every computational trajectory possesses both informational and thermodynamic coordinates.

This framework serves as the mathematical foundation for Quantum Computational Thermodynamics (QCT).

⸻

7.2 Computational Hilbert Space

Let

[
\mathcal H

\bigotimes_{i=1}^{N}\mathcal H_i
]

denote the Hilbert space of an (N)-qubit quantum computer.

For qubits,

[
\mathcal H_i
\simeq
\mathbb C^2,
]

thus

[
\dim(\mathcal H)=2^N.
]

A pure computational state is

[
|\psi\rangle

\sum_{k=0}^{2^N-1}
c_k|k\rangle,
]

with

[
\sum_k|c_k|^2=1.
]

The corresponding density operator is

[
\rho

|\psi\rangle\langle\psi|.
]

For mixed states,

[
\rho

\sum_i
p_i
|\psi_i\rangle
\langle\psi_i|.
]

These objects describe logical information only.

No thermodynamic observable appears explicitly.

⸻

7.3 Physical Hamiltonian

Every quantum computer possesses a physical Hamiltonian

[
H.
]

Unlike conventional computational complexity theory, QCT treats

[
H
]

as an intrinsic computational object.

The total Hamiltonian decomposes into

[
\boxed{
H

H_C
+
H_G
+
H_E
+
H_I.
}
]

where

[
H_C
]

is the computational Hamiltonian,

[
H_G
]

the control Hamiltonian,

[
H_E
]

the environmental Hamiltonian,

and

[
H_I
]

the interaction Hamiltonian.

Each component contributes differently to energy consumption.

⸻

Definition 7.1

The computational Hamiltonian is

[
H_C

\sum_i
\epsilon_i
|i\rangle\langle i|,
]

where

[
\epsilon_i
]

are logical energy eigenvalues.

⸻

The control Hamiltonian describes externally applied gate operations,

[
H_G(t)

\sum_k
u_k(t)
H_k,
]

with

[
u_k(t)
]

representing experimentally controlled pulses.

⸻

Interaction with the environment is represented by

[
H_I

\sum_\alpha
A_\alpha
\otimes
B_\alpha,
]

where

[
A_\alpha
]

acts on the processor,

and

[
B_\alpha
]

acts on the thermal bath.

⸻

7.4 Thermodynamic Hilbert Bundle

We now extend ordinary Hilbert space.

⸻

Definition 7.2

The Thermodynamic Hilbert Bundle is

[
\boxed{
\mathfrak H

\mathcal H
\times
\mathcal E
\times
\mathcal S
\times
\mathcal W
\times
\mathcal X.
}
]

where

* (\mathcal H) is Hilbert space,
* (\mathcal E) energy space,
* (\mathcal S) entropy space,
* (\mathcal W) work space,
* (\mathcal X) exergy space.

Every computational state is therefore

[
\boxed{
\Psi

(\rho,E,S,W,X).
}
]

Unlike conventional quantum mechanics,

two identical density matrices may occupy distinct thermodynamic fibers.

⸻

Interpretation

The projection

[
\pi:
\mathfrak H
\rightarrow
\mathcal H
]

forgets thermodynamic information,

whereas

[
\pi^{-1}(\rho)
]

contains every thermodynamic realization of the same logical state.

This fiber-bundle viewpoint distinguishes logical equivalence from physical equivalence.

⸻

7.5 Thermodynamic Observables

Every observable is represented by a Hermitian operator.

Besides conventional observables,

QCT introduces thermodynamic operators.

⸻

Energy Operator

[
\hat E

H.
]

Expectation value

[
E

\operatorname{Tr}(\rho H).
]

⸻

Entropy Operator

Entropy is nonlinear in

[
\rho,
]

therefore define

[
\boxed{
\hat S

-k_B\ln\rho.
}
]

Then

[
S

\operatorname{Tr}(\rho\hat S)

-k_B
\operatorname{Tr}
(\rho\ln\rho).
]

⸻

Heat Operator

Define

[
\boxed{
\delta\hat Q

dH.
}
]

Its expectation satisfies

[
\delta Q

\operatorname{Tr}
(\rho,dH).
]

⸻

Work Operator

Define

[
\boxed{
\delta\hat W

Hd\rho.
}
]

Thus

[
\delta W

\operatorname{Tr}
(H,d\rho).
]

Together,

[
dE

\delta Q
+
\delta W,
]

recovering the quantum first law.

⸻

7.6 Computational Thermodynamic Trajectories

A quantum algorithm

[
A

(U_1,U_2,\ldots,U_m)
]

defines a trajectory

[
\rho_0
\rightarrow
\rho_1
\rightarrow
\cdots
\rightarrow
\rho_m.
]

QCT extends this to

[
(\rho,E,S,W)
_0
\rightarrow
(\rho,E,S,W)_1
\rightarrow
\cdots.
]

Hence computation becomes a curve on

[
\mathfrak H.
]

⸻

Definition 7.3

A Thermodynamic Computational Trajectory is

[
\gamma:
[0,T]
\rightarrow
\mathfrak H.
]

Algorithmic complexity becomes the geometry of

[
\gamma.
]

⸻

7.7 Thermodynamic Metric

To compare algorithms physically, a metric is required.

Define

[
ds^2

\alpha
,ds_H^2
+
\beta
,dE^2
+
\gamma
,dS^2
+
\delta
,dW^2.
]

The Hilbert contribution is

[
ds_H^2

4
\left(
1-
|\langle\psi|\phi\rangle|^2
\right),
]

equivalent to the Fubini–Study metric for pure states.

The coefficients

[
(\alpha,\beta,\gamma,\delta)
]

weight informational and thermodynamic distances.

Algorithms with identical logical outputs may possess different thermodynamic lengths.

⸻

7.8 Thermodynamic Action Functional

Inspired by classical mechanics, define

[
\boxed{
\mathcal A_T

\int_0^T
L_T
dt.
}
]

where

[
L_T

L_Q

TS

\lambda_QQ

\lambda_WW.
]

Stationary computation satisfies

[
\delta
\mathcal A_T

]

⸻

Principle of Least Thermodynamic Computation

Among all physically realizable implementations,

nature favors trajectories minimizing

[
\mathcal A_T.
]

This generalizes the principle of least action to computation.

⸻

7.9 Thermodynamic Curvature

The computational manifold possesses curvature induced by thermodynamic gradients.

Define

[
g_{ij}

\frac{\partial^2F}
{\partial x_i\partial x_j},
]

where

[
F

E

TS.
]

This Hessian defines a thermodynamic metric tensor.

Its associated curvature tensor

[
R^i{}_{jkl}
]

quantifies sensitivity of computational trajectories to perturbations.

Large curvature indicates thermodynamically fragile algorithms.

Flat regions correspond to stable reversible computation.

⸻

7.10 Computational Geodesics

Given the metric,

algorithms satisfy geodesic equations

[
\boxed{
\frac{d^2x^\mu}{dt^2}
+
\Gamma^\mu_{\alpha\beta}
\frac{dx^\alpha}{dt}
\frac{dx^\beta}{dt}

F^\mu_{\rm diss}.
}
]

The right-hand side represents dissipative forces introduced by

* decoherence,
* measurement,
* control noise,
* thermalization.

Ideal reversible computation satisfies

[
F^\mu_{\rm diss}=0.
]

⸻

7.11 Thermodynamic Invariants

Several quantities remain invariant under unitary evolution.

⸻

Proposition 7.1

If

[
\rho’

U\rho U^\dagger,
]

then

[
S(\rho’)

S(\rho).
]

Proof

Since

[
\ln(U\rho U^\dagger)

U(\ln\rho)U^\dagger,
]

we obtain

[
\begin{aligned}
S(\rho’)
&=
-k_B
\operatorname{Tr}
(U\rho U^\dagger
U(\ln\rho)U^\dagger)
\
&=
-k_B
\operatorname{Tr}
(\rho\ln\rho)
\
&=
S(\rho).
\end{aligned}
]

□

⸻

Proposition 7.2

For isolated computation,

[
\Sigma=0.
]

Hence

[
Q=0.
]

Thus ideal unitary algorithms possess zero intrinsic entropy production.

Irreversibility arises only from non-unitary processes.

⸻

7.12 Computational Thermodynamic Tensor

We now introduce the central geometric object of QCT.

⸻

Definition 7.4

The Computational Thermodynamic Tensor is

[
\boxed{
\Theta_{\mu\nu}

\begin{pmatrix}
E & J_i\
J_i & \Pi_{ij}
\end{pmatrix},
}
]

where

* (E) is computational energy density,
* (J_i) is computational energy flux,
* (\Pi_{ij}) is entropy–work stress.

This tensor plays a role analogous to the stress–energy tensor in field theory.

Its divergence determines irreversible resource flow,

[
\nabla_\mu
\Theta^{\mu\nu}

\mathcal D^\nu,
]

where

[
\mathcal D^\nu
]

represents dissipation.

⸻

7.13 Fundamental Axioms of Hilbert-Space Thermodynamics

The mathematical framework rests on the following axioms.

Axiom H1 (Thermodynamic Realization). Every logical quantum state admits one or more thermodynamic realizations distinguished by energy, entropy, work, and exergy coordinates.

Axiom H2 (Bundle Structure). Physical computation evolves on the Thermodynamic Hilbert Bundle (\mathfrak H), not on Hilbert space alone.

Axiom H3 (Energy Accounting). Every computational trajectory satisfies the quantum first law
[
dE=\delta Q+\delta W.
]

Axiom H4 (Entropy Accounting). Total entropy production is non-negative,
[
\Sigma\ge0,
]
with equality if and only if the evolution is perfectly reversible.

Axiom H5 (Geometric Optimality). Physically optimal implementations correspond to geodesics that extremize the thermodynamic action functional subject to computational constraints.

⸻

7.14 Main Results of Section 7

The Hilbert-Space Thermodynamics framework developed in this section extends conventional quantum computation into a geometric thermodynamic theory. The principal mathematical results are:

* The introduction of the Thermodynamic Hilbert Bundle (\mathfrak H), augmenting Hilbert space with energy, entropy, work, and exergy coordinates.
* The definition of thermodynamic observables as operator-valued quantities compatible with quantum expectation values.
* A geometric description of quantum algorithms as thermodynamic trajectories on (\mathfrak H).
* A thermodynamic metric and action principle that allow computational implementations to be compared by physical resource consumption rather than gate count alone.
* The formulation of the Computational Thermodynamic Tensor, encoding energy density, resource flux, and entropy-work stresses in a unified geometric object.
* A set of foundational axioms establishing Quantum Computational Thermodynamics as a proposed extension of standard quantum information theory.

These constructions provide the mathematical infrastructure required for the subsequent development of entropy functionals, open-system dynamics, quantum channels, resource theories, and ultimately a complete thermodynamic complexity theory for quantum computation.

The Thermodynamic Cost of Quantum Computation

Part X — Applications to Major Quantum Algorithms

Section 59. Variational Algorithms

⸻

59.1 Introduction

The preceding sections analyzed four major computational paradigms:

[
\boxed{
\text{Shor}
\rightarrow
\text{Grover}
\rightarrow
\text{HHL}
\rightarrow
\text{Quantum Simulation}.
}
]

These algorithms derive their computational power from fundamentally different mechanisms:

[
\begin{array}{c}
\text{Period Finding}\
\text{Amplitude Amplification}\
\text{Spectral Inversion}\
\text{Many-Body Quantum Evolution}.
\end{array}
]

The next major class is the family of variational quantum algorithms.

Variational algorithms differ fundamentally from the algorithms previously studied.

They do not generally implement one fixed, analytically specified quantum circuit.

Instead, they construct a parameterized family of states

[
\boxed{
|\psi(\boldsymbol\theta)\rangle

U(\boldsymbol\theta)|\psi_0\rangle
}
]

and optimize the parameters

[
\boxed{
\boldsymbol\theta

(\theta_1,\ldots,\theta_p)
}
]

using repeated interaction between a quantum processor and a classical optimizer.

The computational process is therefore inherently hybrid:

[
\boxed{
\text{Quantum State Preparation}
\rightarrow
\text{Measurement}
\rightarrow
\text{Classical Optimization}
\rightarrow
\text{Parameter Update}
\rightarrow
\text{Quantum State Preparation}.
}
]

The thermodynamic cost is correspondingly different from that of a single coherent quantum circuit.

The complete cost is

[
\boxed{
W_{\rm VAR}

\sum_{k=1}^{K}
\left[
W_{\rm prep}^{(k)}
+
W_{\rm circuit}^{(k)}
+
W_{\rm measurement}^{(k)}
+
W_{\rm reset}^{(k)}
+
W_{\rm classical}^{(k)}
\right].
}
]

The central result of this section is:

The thermodynamic cost of a variational quantum algorithm is controlled not primarily by circuit depth alone, but by the product of optimization iterations, circuit execution cost, measurement precision, parameter dimension, and reset entropy.

A variational algorithm can therefore possess shallow quantum circuits while having a very large total thermodynamic cost.

⸻

59.2 General Variational Formulation

Let the parameterized quantum state be

[
\boxed{
|\psi(\boldsymbol\theta)\rangle

U(\boldsymbol\theta)|\psi_0\rangle.
}
]

Let the objective function be

[
\boxed{
C(\boldsymbol\theta)

\langle\psi(\boldsymbol\theta)|
O
|\psi(\boldsymbol\theta)\rangle.
}
]

The optimization problem is

[
\boxed{
\boldsymbol\theta^\star

\arg\min_{\boldsymbol\theta}
C(\boldsymbol\theta).
}
]

The algorithm alternates between:

[
\boxed{
\boldsymbol\theta_k
\rightarrow
|\psi(\boldsymbol\theta_k)\rangle
\rightarrow
\widehat C(\boldsymbol\theta_k)
\rightarrow
\boldsymbol\theta_{k+1}.
}
]

The quantum system therefore acts as an objective-function oracle.

⸻

59.3 The Variational Principle

For a Hamiltonian

[
H,
]

the ground-state energy is

[
\boxed{
E_0

\min_{|\psi|=1}
\langle\psi|H|\psi\rangle.
}
]

For any normalized trial state

[
|\psi(\boldsymbol\theta)\rangle,
]

the variational principle gives

[
\boxed{
E(\boldsymbol\theta)

\langle\psi(\boldsymbol\theta)|
H
|\psi(\boldsymbol\theta)\rangle
\ge
E_0.
}
]

The objective function is therefore

[
\boxed{
C(\boldsymbol\theta)

E(\boldsymbol\theta).
}
]

The algorithm seeks

[
\boxed{
C(\boldsymbol\theta)
\rightarrow
E_0.
}
]

⸻

59.4 Hamiltonian Decomposition

Suppose

[
\boxed{
H

\sum_{\mu=1}^{L}
h_\mu P_\mu,
}
]

where

[
P_\mu
]

are Pauli strings.

Then

[
\boxed{
E(\boldsymbol\theta)

\sum_{\mu=1}^{L}
h_\mu
\langle P_\mu\rangle_{\boldsymbol\theta}.
}
]

Each expectation value must be estimated experimentally.

The total measurement cost is therefore

[
\boxed{
W_{\rm meas}

\sum_{\mu=1}^{L}
M_\mu
W_{\rm shot},
}
]

where

[
M_\mu
]

is the number of shots used to estimate

[
\langle P_\mu\rangle.
]

⸻

59.5 Measurement Variance

For an observable

[
P_\mu
]

with eigenvalues

[
\pm1,
]

the estimator variance is

[
\boxed{
\operatorname{Var}
(\widehat{\langle P_\mu\rangle})

\frac{
1-\langle P_\mu\rangle^2
}
{
M_\mu
}.
}
]

To obtain precision

[
\epsilon_\mu,
]

one requires

[
\boxed{
M_\mu

O
\left(
\frac{
1-\langle P_\mu\rangle^2
}
{
\epsilon_\mu^2
}
\right).
}
]

Therefore,

[
\boxed{
W_{\rm meas}
\propto
\epsilon^{-2}.
}
]

⸻

59.6 The Variational Thermodynamic Cost Functional

Let

[
K
]

be the number of optimization iterations.

Let

[
G(\boldsymbol\theta_k)
]

be the quantum circuit gate count at iteration

[
k.
]

Let

[
M_k
]

be the number of measurement shots.

The total work is

[
\boxed{
W_{\rm VAR}

\sum_{k=1}^{K}
\left[
G(\boldsymbol\theta_k)
\epsilon_{\rm gate}
+
M_k
W_{\rm shot}
+
W_{\rm reset}^{(k)}
\right]
+
W_{\rm classical}.
}
]

If the average iteration cost is approximately constant,

[
\boxed{
W_{\rm VAR}
\approx
K
\left(
W_{\rm circuit}
+
W_{\rm measurement}
+
W_{\rm reset}
\right).
}
]

⸻

59.7 VQE

The Variational Quantum Eigensolver solves

[
\boxed{
E_0

\min_{\boldsymbol\theta}
\langle\psi(\boldsymbol\theta)|H|\psi(\boldsymbol\theta)\rangle.
}
]

The thermodynamic cost is

[
\boxed{
W_{\rm VQE}

K_{\rm opt}
\left[
W_{\rm ansatz}
+
W_{\rm measurement}
+
W_{\rm reset}
\right].
}
]

The algorithm’s central thermodynamic problem is therefore:

[
\boxed{
\text{low-depth circuit}
\not\Rightarrow
\text{low total dissipation}.
}
]

⸻

59.8 Ansatz Expressibility

Let

[
\mathcal M

{
|\psi(\boldsymbol\theta)\rangle
:
\boldsymbol\theta\in\Theta
}
]

be the variational manifold.

The approximation error is

[
\boxed{
\delta_{\rm ansatz}

\min_{\boldsymbol\theta}
\left[
E(\boldsymbol\theta)-E_0
\right].
}
]

If

[
\delta_{\rm ansatz}>0,
]

no amount of optimization can reach the exact ground state.

Thus,

[
\boxed{
\text{expressibility}
\rightarrow
\text{thermodynamic resource}.
}
]

An insufficient ansatz wastes energy on optimization iterations without reducing the physical error below

[
\delta_{\rm ansatz}.
]

⸻

59.9 Ansatz Depth

Suppose the ansatz contains

[
D
]

layers.

The circuit work is

[
\boxed{
W_{\rm circuit}

D
N_{\rm gate}
\epsilon_{\rm gate}.
}
]

Increasing

[
D
]

may reduce

[
\delta_{\rm ansatz},
]

but increases

[
W_{\rm circuit}.
]

The thermodynamic optimization is

[
\boxed{
\min_D
\left[
K(D)
W_{\rm iteration}(D)
\right].
}
]

⸻

59.10 The Ansatz Thermodynamic Tradeoff

Increasing ansatz expressibility produces

[
\boxed{
\delta_{\rm ansatz}\downarrow
}
]

but may produce

[
\boxed{
W_{\rm circuit}\uparrow
}
]

and

[
\boxed{
K_{\rm opt}\uparrow.
}
]

Therefore,

[
\boxed{
\text{expressibility}
\neq
\text{thermodynamic efficiency}.
}
]

The thermodynamically optimal ansatz minimizes

[
\boxed{
W_{\rm total}
}
]

subject to

[
\boxed{
\delta_{\rm total}
\le
\epsilon.
}
]

⸻

59.11 Classical Optimization Cost

The classical optimizer receives

[
C(\boldsymbol\theta_k)
]

and computes an update

[
\boxed{
\boldsymbol\theta_{k+1}

\boldsymbol\theta_k

\eta_k
\nabla C(\boldsymbol\theta_k).
}
]

The classical work is

[
\boxed{
W_{\rm class}

\sum_{k=1}^{K}
W_{\rm optimizer}^{(k)}.
}
]

The complete algorithm is therefore not purely quantum.

The thermodynamic cost must satisfy

[
\boxed{
W_{\rm total}

W_Q
+
W_C.
}
]

⸻

59.12 Parameter-Shift Gradients

For a parameter

[
\theta_j,
]

the gradient may be obtained using

[
\boxed{
\frac{\partial C}{\partial\theta_j}

\frac12
\left[
C\left(
\theta_j+\frac\pi2
\right)

C\left(
\theta_j-\frac\pi2
\right)
\right].
}
]

For

[
p
]

parameters, a full gradient requires approximately

[
\boxed{
2p
}
]

additional quantum evaluations.

Therefore,

[
\boxed{
W_{\rm gradient}

O(p)
W_{\rm evaluation}.
}
]

⸻

59.13 Gradient Thermodynamic Cost

The total gradient-based cost is

[
\boxed{
W_{\rm grad}

2pK
W_{\rm evaluation}.
}
]

Thus,

[
\boxed{
p\uparrow
\quad\Longrightarrow\quad
W_{\rm grad}\uparrow.
}
]

This creates a fundamental tradeoff:

[
\boxed{
\text{more parameters}
\rightarrow
\text{greater expressibility}
\rightarrow
\text{greater thermodynamic cost}.
}
]

⸻

59.14 Measurement Frugality

Suppose the objective function is estimated with uncertainty

[
\sigma_C.
]

Excessive measurement precision produces unnecessary thermodynamic cost.

The optimal strategy is to choose

[
\boxed{
\sigma_C
\sim
\text{optimization uncertainty}.
}
]

Therefore,

[
\boxed{
\text{measurement precision should track optimization progress}.
}
]

Early iterations require low precision.

Late iterations require higher precision.

⸻

59.15 Adaptive Measurement Thermodynamics

Let

[
\epsilon_k
]

be the measurement precision at iteration

[
k.
]

Then

[
\boxed{
M_k
\propto
\epsilon_k^{-2}.
}
]

The optimal schedule satisfies

[
\boxed{
\epsilon_k
\downarrow
\quad\text{as}\quad
k\uparrow.
}
]

This yields

[
\boxed{
W_{\rm meas}^{\rm adaptive}
<
W_{\rm meas}^{\rm fixed}
}
]

for optimization trajectories in which early low-precision estimates are sufficient.

⸻

59.16 Barren Plateaus

A major obstacle is the exponential suppression of gradients.

Let

[
g_j

\frac{\partial C}{\partial\theta_j}.
]

A barren plateau occurs when

[
\boxed{
\operatorname{Var}(g_j)

O(2^{-n}).
}
]

To resolve a gradient of magnitude

[
O(2^{-n/2}),
]

the number of measurements may scale as

[
\boxed{
M

O(2^n).
}
]

Therefore,

[
\boxed{
W_{\rm measurement}

O(2^n).
}
]

A shallow quantum circuit can therefore possess an exponentially large thermodynamic cost.

⸻

59.17 Barren-Plateau Thermodynamic Law

If

[
\operatorname{Var}
\left(
\frac{\partial C}{\partial\theta}
\right)

O(2^{-n}),
]

then the thermodynamic cost of resolving the gradient satisfies

[
\boxed{
W_{\rm grad}

\Omega(2^n).
}
]

This establishes the Barren-Plateau Thermodynamic Law:

Exponentially vanishing gradients generate exponentially growing measurement entropy and can destroy the thermodynamic advantage of variational quantum computation.

⸻

59.18 Optimization as Thermodynamic Search

The parameter space has dimension

[
p.
]

The optimizer explores

[
\Theta\subseteq\mathbb R^p.
]

Each objective evaluation requires physical quantum evolution.

Therefore, the optimization trajectory

[
\boldsymbol\theta_0
\rightarrow
\boldsymbol\theta_1
\rightarrow
\cdots
\rightarrow
\boldsymbol\theta_K
]

has total thermodynamic cost

[
\boxed{
W_{\rm trajectory}

\sum_{k=0}^{K-1}
W
\left(
\boldsymbol\theta_k
\rightarrow
\boldsymbol\theta_{k+1}
\right).
}
]

The optimization path itself is therefore a thermodynamic object.

⸻

59.19 Optimization Dissipation

Let

[
\Sigma_k
]

be the entropy produced during iteration

[
k.
]

Then

[
\boxed{
\Sigma_{\rm VAR}

\sum_{k=1}^{K}
\Sigma_k.
}
]

The total dissipated heat satisfies

[
\boxed{
Q_{\rm diss}
\ge
T\Sigma_{\rm VAR}.
}
]

Thus,

[
\boxed{
K\uparrow
\quad\Longrightarrow\quad
\Sigma_{\rm VAR}\uparrow
}
]

unless the per-iteration dissipation decreases sufficiently rapidly.

⸻

59.20 Reset Cost of Variational Algorithms

Each iteration generally requires

[
\boxed{
\text{measurement}
\rightarrow
\text{classical processing}
\rightarrow
\text{state reset}.
}
]

If the measured quantum state has entropy

[
S(\rho),
]

then reset satisfies

[
\boxed{
W_{\rm reset}
\ge
k_BT S(\rho).
}
]

For

[
K
]

iterations,

[
\boxed{
W_{\rm reset,total}
\ge
Kk_BT S(\rho).
}
]

This is the Iterative Reset Law.

⸻

59.21 Variational Reset Scaling Theorem

Theorem 59.1

For a variational algorithm requiring

[
K
]

independent quantum-state preparation and reset cycles, with average reset entropy

[
\bar S,
]

the minimum reset work satisfies

[
\boxed{
W_{\rm reset}
\ge
Kk_BT\bar S.
}
]

⸻

Proof

Each iteration requires resetting the entropy-bearing computational state.

The generalized Landauer bound gives

[
W_{{\rm reset},k}
\ge
k_BT S_k.
]

Summing over

[
K
]

iterations gives

[
W_{\rm reset}
\ge
k_BT
\sum_{k=1}^{K}S_k.
]

Defining

[
\bar S

\frac1K
\sum_{k=1}^{K}S_k
]

yields

[
W_{\rm reset}
\ge
Kk_BT\bar S.
]

□

⸻

59.22 VQE Thermodynamic Cost

The complete VQE cost is

[
\boxed{
W_{\rm VQE}

K
\left[
W_{\rm ansatz}
+
L
M
W_{\rm shot}
+
W_{\rm reset}
\right]
+
W_{\rm optimizer}.
}
]

If gradient estimation is used,

[
\boxed{
W_{\rm VQE}

K
\left[
2p
+
1
\right]
L
M
W_{\rm shot}
+
W_{\rm reset}
+
W_{\rm optimizer}.
}
]

The dominant cost may therefore be measurement rather than coherent quantum evolution.

⸻

59.23 QAOA

The Quantum Approximate Optimization Algorithm uses

[
\boxed{
|\boldsymbol\gamma,\boldsymbol\beta\rangle

\prod_{j=1}^{p}
e^{-i\beta_j B}
e^{-i\gamma_j C}
|+\rangle^{\otimes n}.
}
]

The objective is

[
\boxed{
F_p(\boldsymbol\gamma,\boldsymbol\beta)

\langle C\rangle.
}
]

The thermodynamic cost is

[
\boxed{
W_{\rm QAOA}

K_{\rm opt}
\left[
W_{\rm layer}(p)
+
W_{\rm measurement}
+
W_{\rm reset}
\right].
}
]

Increasing the QAOA depth

[
p
]

may improve approximation quality but increases

[
W_{\rm layer}.
]

⸻

59.24 QAOA Depth Thermodynamics

Let

[
\epsilon_p
]

be the approximation error at depth

[
p.
]

Then

[
\boxed{
p\uparrow
\quad\Longrightarrow\quad
\epsilon_p\downarrow
}
]

but

[
\boxed{
W_p\uparrow.
}
]

The optimal depth satisfies

[
\boxed{
p^\star

\arg\min_p
\left[
W_{\rm total}(p)
\right]
}
]

subject to

[
\boxed{
\epsilon_p
\le
\epsilon_{\rm target}.
}
]

⸻

59.25 Variational Quantum Advantage

Define the thermodynamic advantage ratio

[
\boxed{
\mathcal A_{\rm VAR}

\frac{
W_{\rm classical}
}
{
W_{\rm VAR}
}.
}
]

A variational algorithm has thermodynamic advantage if

[
\boxed{
\mathcal A_{\rm VAR}>1.
}
]

Asymptotic advantage requires

[
\boxed{
\lim_{n\to\infty}
\frac{
W_{\rm VAR}(n)
}
{
W_{\rm classical}(n)
}

}
]

However, because

[
W_{\rm VAR}
]

contains an optimization loop, this condition is substantially more difficult to satisfy than for a fixed-depth quantum algorithm.

⸻

59.26 The Variational Advantage Condition

A variational algorithm can retain thermodynamic advantage only if

[
\boxed{
K_{\rm opt}
,
M_{\rm meas}
,
p
,
W_{\rm shot}
\ll
W_{\rm classical}.
}
]

The quantum circuit depth alone is insufficient.

The correct resource product is

[
\boxed{
\text{optimization iterations}
\times
\text{measurements}
\times
\text{quantum execution cost}.
}
]

⸻

59.27 Variational Thermodynamic Complexity

Define the variational thermodynamic complexity

[
\boxed{
\mathcal C_{\rm VT}

K
\left(
G
+
M
+
R
\right),
}
]

where

[
G
]

is gate complexity,

[
M
]

is measurement complexity, and

[
R
]

is reset complexity.

The energy-weighted form is

[
\boxed{
\mathcal C_{\rm VT}^{(E)}

K
\left(
E_G
+
E_M
+
E_R
\right).
}
]

The entropy-weighted form is

[
\boxed{
\mathcal C_{\rm VT}^{(S)}

K
\left(
S_G
+
S_M
+
S_R
\right).
}
]

⸻

59.28 Variational Thermodynamic Complexity Class

Define

[
\boxed{
\mathrm{VQTC}(f)
}
]

as the class of variational quantum algorithms satisfying

[
\boxed{
W_{\rm VAR}(n)

O(f(n)).
}
]

A polynomially bounded variational algorithm belongs to

[
\boxed{
\mathrm{VQTC}
\left(
\operatorname{poly}(n)
\right).
}
]

An algorithm with exponentially suppressed gradients may instead satisfy

[
\boxed{
W_{\rm VAR}

\Omega(2^n).
}
]

Thus,

[
\boxed{
\mathrm{VQTC}
}
]

contains both thermodynamically efficient and thermodynamically inefficient variational algorithms.

⸻

59.29 The Optimization–Dissipation Principle

The complete variational process is

[
\boxed{
\text{parameter exploration}
\rightarrow
\text{quantum evaluation}
\rightarrow
\text{measurement}
\rightarrow
\text{reset}
\rightarrow
\text{parameter exploration}.
}
]

Each loop exports entropy.

Therefore:

Variational quantum computation converts optimization complexity into repeated thermodynamic cycles.

The total dissipation is determined by

[
\boxed{
\Sigma_{\rm total}

\sum_{k=1}^{K}
\left[
\Sigma_{\rm control}^{(k)}
+
\Sigma_{\rm meas}^{(k)}
+
\Sigma_{\rm reset}^{(k)}
\right].
}
]

⸻

59.30 Thermodynamic Variational Uncertainty Relation

Let

[
\Delta C
]

be the uncertainty of the objective estimate.

Let

[
\Sigma_{\rm VAR}
]

be total entropy production.

Then

[
\boxed{
\frac{
(\Delta C)^2
}
{
\langle C\rangle^2
}
\Sigma_{\rm VAR}
\ge
2k_B.
}
]

Therefore,

[
\boxed{
\Delta C\downarrow
\quad\Longrightarrow\quad
\Sigma_{\rm VAR}\uparrow.
}
]

The precision of the objective function cannot be increased without thermodynamic cost.

⸻

59.31 The Variational Thermodynamic Scaling Theorem

Theorem 59.2

Let a variational quantum algorithm have:

* (K(n)) optimization iterations;
* (p(n)) variational parameters;
* (M(n)) measurement shots per objective evaluation;
* (G(n)) gates per quantum circuit;
* reset entropy (S(n)) per iteration.

Then

[
\boxed{
W_{\rm VAR}(n)
\ge
K(n)
\left[
G(n)\epsilon_{\rm gate}
+
M(n)W_{\rm shot}
+
k_BT S(n)
\right].
}
]

If

[
K(n),p(n),M(n),G(n)

\operatorname{poly}(n),
]

then

[
\boxed{
W_{\rm VAR}(n)

\operatorname{poly}(n).
}
]

If gradient variance satisfies

[
\operatorname{Var}(\nabla C)

O(2^{-n}),
]

then

[
\boxed{
M(n)

\Omega(2^n)
}
]

and consequently

[
\boxed{
W_{\rm VAR}(n)

\Omega(2^n).
}
]

⸻

59.32 Proof

The lower bound follows from the additive costs of circuit execution, measurement, and reset.

For polynomially bounded

[
K,G,M,S,
]

the total is polynomial.

For a gradient whose variance decays as

[
2^{-n},
]

the signal-to-noise ratio requires exponentially many samples.

Therefore,

[
M=\Omega(2^n),
]

which produces

[
W_{\rm VAR}=\Omega(2^n).
]

□

⸻

59.33 Thermodynamic Optimization Theorem

Theorem 59.3

For a variational quantum algorithm, minimizing quantum circuit depth alone does not minimize total thermodynamic cost.

The thermodynamic optimum satisfies

[
\boxed{
\frac{\partial W_{\rm total}}
{\partial D}
+
\frac{\partial W_{\rm total}}
{\partial K}
+
\frac{\partial W_{\rm total}}
{\partial M}
+
\frac{\partial W_{\rm total}}
{\partial R}

0
}
]

subject to

[
\boxed{
\epsilon_{\rm total}
\le
\epsilon_{\rm target}.
}
]

⸻

Interpretation

A deeper circuit may reduce

[
K.
]

A larger measurement budget may reduce

[
K.
]

More aggressive reset strategies may increase

[
W_{\rm reset}
]

but reduce noise.

Therefore, the optimal architecture is determined by the complete thermodynamic objective:

[
\boxed{
W_{\rm total}

W_{\rm circuit}
+
W_{\rm measurement}
+
W_{\rm optimization}
+
W_{\rm reset}.
}
]

⸻

59.34 Variational Algorithm Thermodynamic Advantage Theorem

Theorem 59.4

A variational quantum algorithm possesses asymptotic thermodynamic advantage over a classical algorithm only if

[
\boxed{
K(n)
\left[
G(n)
+
M(n)
+
R(n)
\right]

o
\left(
W_{\rm classical}(n)
\right).
}
]

If any of the following scales exponentially,

[
\boxed{
K(n),
\qquad
M(n),
\qquad
R(n),
}
]

then the asymptotic thermodynamic advantage may disappear even when

[
G(n)

\operatorname{poly}(n).
]

⸻

59.35 Proof

The total variational cost is bounded below by

[
W_{\rm VAR}
\ge
K(G+M+R).
]

If this quantity is not asymptotically smaller than

[
W_{\rm classical},
]

then

[
\frac{
W_{\rm VAR}
}
{
W_{\rm classical}
}
\not\rightarrow0.
]

Therefore, asymptotic thermodynamic advantage requires the stated condition.

□

⸻

59.36 Variational Algorithms and Quantum Advantage

Variational algorithms reveal a central distinction:

[
\boxed{
\text{quantum circuit advantage}
\neq
\text{algorithmic thermodynamic advantage}.
}
]

A quantum circuit may be shallow:

[
G=\operatorname{poly}(n),
]

while the total optimization process satisfies

[
K M

\Omega(2^n).
]

Then

[
\boxed{
W_{\rm VAR}

\Omega(2^n).
}
]

The thermodynamic cost of the algorithm is therefore determined by the entire computational loop.

⸻

59.37 The Thermodynamic Variational Principle

The preceding results establish the following principle.

Thermodynamic Variational Principle

The optimal variational quantum algorithm is not the algorithm with the shallowest circuit, the smallest parameter count, or the fewest measurements individually. It is the algorithm that minimizes total energy and entropy production over the complete optimization trajectory while satisfying the required computational precision.

Formally,

[
\boxed{
\mathcal A^\star

\arg\min_{\mathcal A}
\left[
W_{\rm circuit}
+
W_{\rm measurement}
+
W_{\rm optimization}
+
W_{\rm reset}
\right].
}
]

⸻

59.38 Summary

This section developed a thermodynamic theory of variational quantum algorithms.

The principal results include:

* formulation of variational computation as a thermodynamic optimization trajectory;
* derivation of the complete VQE cost functional;
* analysis of Hamiltonian measurement overhead;
* derivation of parameter-shift gradient costs;
* formulation of adaptive measurement thermodynamics;
* derivation of the Barren-Plateau Thermodynamic Law;
* formulation and proof of the Iterative Reset Law;
* analysis of QAOA depth and thermodynamic scaling;
* definition of variational thermodynamic complexity;
* introduction of the class

[
\boxed{
\mathrm{VQTC};
}
]

* derivation of the Variational Thermodynamic Scaling Theorem;
* derivation of the Thermodynamic Optimization Theorem;
* proof of the Variational Algorithm Thermodynamic Advantage Theorem; and
* formulation of the Thermodynamic Variational Principle.

The central result is

[
\boxed{
W_{\rm VAR}
\sim
K_{\rm opt}
\left[
W_{\rm circuit}
+
W_{\rm measurement}
+
W_{\rm reset}
\right].
}
]

Therefore:

[
\boxed{
\text{shallow quantum circuits}
\not\Rightarrow
\text{low thermodynamic cost}.
}
]

The thermodynamic cost of variational quantum computation is governed by the full optimization loop:

[
\boxed{
\text{Ansatz}
\rightarrow
\text{Measurement}
\rightarrow
\text{Optimization}
\rightarrow
\text{Reset}
\rightarrow
\text{Repeat}.
}
]

When the optimization trajectory, measurement precision, and reset requirements remain polynomially bounded, variational quantum algorithms may retain thermodynamic advantage.

When barren plateaus, exponentially precise gradients, or exponentially many optimization iterations arise, the thermodynamic cost can become exponential and erase the apparent advantage of shallow quantum circuits.

The next section applies the framework to Quantum Machine Learning, where variational quantum circuits, parameter training, data encoding, and repeated measurement create an even more complex thermodynamic optimization structure.

The Thermodynamic Cost of Quantum Computation

Part X — Applications to Major Quantum Algorithms

Section 60. Quantum Machine Learning

⸻

60.1 Introduction

The preceding section established the thermodynamic theory of variational quantum algorithms.

The principal result was

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

Quantum machine learning extends this structure by introducing a second layer of computational complexity.

A quantum machine-learning algorithm does not merely optimize a quantum circuit.

It must also process a dataset.

The complete computational process becomes

[
\boxed{
\text{Data}
\rightarrow
\text{Encoding}
\rightarrow
\text{Quantum Processing}
\rightarrow
\text{Measurement}
\rightarrow
\text{Classical Training}
\rightarrow
\text{Parameter Update}
\rightarrow
\text{Repeat}.
}
]

The thermodynamic cost is therefore

[
\boxed{
W_{\rm QML}

W_{\rm data}
+
W_{\rm encode}
+
W_{\rm quantum}
+
W_{\rm measure}
+
W_{\rm reset}
+
W_{\rm train}.
}
]

The central question is:

Can quantum machine learning retain computational or statistical advantage after the thermodynamic cost of data loading, repeated quantum execution, measurement, optimization, and reset is included?

This question is particularly important because quantum machine learning contains a potentially severe thermodynamic asymmetry:

[
\boxed{
\text{Quantum processing may be efficient}
}
]

while

[
\boxed{
\text{data encoding may dominate the entire cost}.
}
]

The fundamental result of this section is:

The thermodynamic advantage of quantum machine learning is bounded by the cost of converting classical information into quantum states and extracting useful information from them.

⸻

60.2 General Quantum Machine-Learning Model

Let the training dataset be

[
\boxed{
\mathcal D

{(x_i,y_i)}_{i=1}^{N}.
}
]

The input features are

[
x_i\in\mathbb R^d,
]

and the labels are

[
y_i.
]

A quantum model is defined by

[
\boxed{
f_{\boldsymbol\theta}(x)

\mathcal M
\left[
U(\boldsymbol\theta,x)
|\psi_0\rangle
\right],
}
]

where:

* (x) is the classical input;
* (U(\boldsymbol\theta,x)) is a parameterized quantum circuit;
* (\boldsymbol\theta) is the trainable parameter vector;
* (\mathcal M) is a measurement map.

The loss function is

[
\boxed{
\mathcal L(\boldsymbol\theta)

\frac1N
\sum_{i=1}^{N}
\ell
\left(
f_{\boldsymbol\theta}(x_i),
y_i
\right).
}
]

Training seeks

[
\boxed{
\boldsymbol\theta^\star

\arg\min_{\boldsymbol\theta}
\mathcal L(\boldsymbol\theta).
}
]

⸻

60.3 The Complete Thermodynamic Learning Cycle

One training iteration consists of

[
\boxed{
x_i
\rightarrow
\rho_i
\rightarrow
U(\boldsymbol\theta)
\rightarrow
\rho_i’
\rightarrow
\mathcal M
\rightarrow
\widehat y_i
\rightarrow
\mathcal L
\rightarrow
\boldsymbol\theta’.
}
]

The thermodynamic cost is

[
\boxed{
W_{\rm iter}

W_{\rm encode}
+
W_{\rm process}
+
W_{\rm measure}
+
W_{\rm reset}
+
W_{\rm update}.
}
]

For

[
K
]

training iterations and batch size

[
B,
]

the total cost is

[
\boxed{
W_{\rm QML}

K B
\left(
W_{\rm encode}
+
W_{\rm process}
+
W_{\rm measure}
+
W_{\rm reset}
\right)
+
K W_{\rm update}.
}
]

⸻

60.4 Data Encoding as a Thermodynamic Resource

Classical data must be mapped to a quantum state.

Let

[
x

(x_1,\ldots,x_d).
]

The encoding map is

[
\boxed{
\mathcal E:
x
\mapsto
\rho_x.
}
]

The thermodynamic cost of encoding is

[
\boxed{
W_{\rm encode}

W_{\rm preparation}
+
W_{\rm control}
+
W_{\rm verification}.
}
]

The quantum algorithm cannot use classical information before it has been physically transferred into the quantum computational substrate.

Therefore,

[
\boxed{
W_{\rm QML}
\ge
W_{\rm encode}.
}
]

⸻

60.5 Amplitude Encoding

Amplitude encoding attempts to represent

[
x\in\mathbb R^d
]

as

[
\boxed{
|x\rangle

\frac1{|x|}
\sum_{j=0}^{d-1}
x_j|j\rangle.
}
]

The number of qubits required is

[
\boxed{
n

\lceil\log_2d\rceil.
}
]

This appears exponentially efficient in memory.

However, state preparation is not free.

The physical transformation

[
|0\rangle^{\otimes n}
\rightarrow
|x\rangle
]

requires a preparation circuit.

The thermodynamic cost is

[
\boxed{
W_{\rm amp}

W
\left(
|0\rangle^{\otimes n}
\rightarrow
|x\rangle
\right).
}
]

⸻

60.6 The Data-Loading Thermodynamic Principle

A compressed quantum representation does not eliminate the physical cost of data transfer.

The total cost satisfies

[
\boxed{
W_{\rm data}

W_{\rm classical\ source}
+
W_{\rm quantum\ encoding}.
}
]

Thus,

[
\boxed{
\text{qubit compression}
\neq
\text{thermodynamic compression}.
}
]

If the classical data must be individually read, processed, and loaded, then the encoding cost may scale as

[
\boxed{
W_{\rm encode}

\Omega(d).
}
]

Consequently, an algorithm with

[
O(\log d)
]

quantum memory may still require

[
O(d)
]

thermodynamic work to prepare its input.

⸻

60.7 Basis Encoding

A simpler encoding maps classical features to computational basis states.

For a binary vector

[
x\in{0,1}^n,
]

the encoding is

[
\boxed{
x
\mapsto
|x_1x_2\cdots x_n\rangle.
}
]

The state-preparation cost is approximately

[
\boxed{
W_{\rm basis}

N_1(x)
W_{X},
}
]

where

[
N_1(x)
]

is the number of bit flips required.

Basis encoding therefore has a direct thermodynamic interpretation:

[
\boxed{
\text{classical bit}
\rightarrow
\text{physical quantum excitation}.
}
]

⸻

60.8 Angle Encoding

For feature vector

[
x=(x_1,\ldots,x_n),
]

angle encoding uses

[
\boxed{
|\psi(x)\rangle

\bigotimes_{j=1}^{n}
R_y(x_j)|0\rangle.
}
]

The gate count is

[
\boxed{
G_{\rm enc}

O(n).
}
]

The encoding work is therefore

[
\boxed{
W_{\rm enc}

O(n\epsilon_{\rm gate}).
}
]

Angle encoding trades memory compression for direct control complexity.

⸻

60.9 Feature Maps

A general quantum feature map is

[
\boxed{
|\phi(x)\rangle

U_\phi(x)|0\rangle^{\otimes n}.
}
]

The induced quantum kernel is

[
\boxed{
K(x,x’)

\left|
\langle\phi(x)|\phi(x’)\rangle
\right|^2.
}
]

The feature map creates a nonlinear embedding

[
\boxed{
\mathbb R^d
\rightarrow
\mathcal H_Q.
}
]

Its thermodynamic cost is

[
\boxed{
W_\phi

W
\left[
U_\phi(x)
\right].
}
]

⸻

60.10 Quantum Kernel Methods

The kernel matrix is

[
\boxed{
K_{ij}

\left|
\langle\phi(x_i)
|
\phi(x_j)\rangle
\right|^2.
}
]

For a dataset of size

[
N,
]

constructing the complete kernel matrix requires

[
\boxed{
O(N^2)
}
]

pairwise evaluations.

If each kernel estimate requires

[
M
]

measurement shots, then

[
\boxed{
W_{\rm kernel}

O(N^2M W_{\rm shot}).
}
]

Thus, a quantum kernel can possess a complex feature space while the thermodynamic cost of evaluating the kernel matrix becomes the dominant resource.

⸻

60.11 Quantum Neural Networks

A quantum neural network is a parameterized map

[
\boxed{
U(\boldsymbol\theta)

U_L(\theta_L)
\cdots
U_2(\theta_2)
U_1(\theta_1).
}
]

The model output is

[
\boxed{
f_{\boldsymbol\theta}(x)

\langle
\psi_0
|
U^\dagger(\boldsymbol\theta,x)
O
U(\boldsymbol\theta,x)
|\psi_0
\rangle.
}
]

Training requires

[
\boxed{
\nabla_{\boldsymbol\theta}
\mathcal L.
}
]

The total gradient cost scales approximately as

[
\boxed{
W_{\rm gradient}

O(p)
W_{\rm model\ evaluation},
}
]

where

[
p
]

is the number of trainable parameters.

⸻

60.12 The QML Thermodynamic Cost Functional

For a training set of size

[
N,
]

batch size

[
B,
]

iterations

[
K,
]

parameters

[
p,
]

and measurement shots

[
M,
]

the total thermodynamic cost is

[
\boxed{
W_{\rm QML}

K
\left[
B
\left(
W_{\rm enc}
+
W_{\rm circuit}
+
W_{\rm measure}
+
W_{\rm reset}
\right)
+
W_{\rm gradient}
+
W_{\rm classical}
\right].
}
]

For parameter-shift training,

[
\boxed{
W_{\rm gradient}

O(pBM W_{\rm shot}).
}
]

Therefore,

[
\boxed{
W_{\rm QML}

O
\left[
KB
\left(
W_{\rm enc}
+
W_{\rm circuit}
+
MW_{\rm shot}
+
W_{\rm reset}
\right)
+
KpBM W_{\rm shot}
\right].
}
]

⸻

60.13 Quantum Machine Learning as Repeated State Preparation

Unlike a fixed quantum algorithm, QML repeatedly prepares states

[
\boxed{
|\psi(x_i,\boldsymbol\theta_k)\rangle.
}
]

The number of state preparations is approximately

[
\boxed{
N_{\rm prep}

K B M.
}
]

The cumulative reset cost is

[
\boxed{
W_{\rm reset}
\ge
K B M k_BT\bar S.
}
]

Thus,

[
\boxed{
N_{\rm prep}\uparrow
\quad\Longrightarrow\quad
W_{\rm reset}\uparrow.
}
]

⸻

60.14 Quantum Machine Learning and Landauer Irreversibility

The training process produces classical information:

[
\boxed{
\mathcal L_1,
\mathcal L_2,
\ldots,
\mathcal L_K.
}
]

The optimizer transforms this information into updated parameters.

If the optimization memory is repeatedly overwritten, the information-erasure cost satisfies

[
\boxed{
W_{\rm erase}
\ge
k_BT\ln2
\cdot
N_{\rm erased}.
}
]

Therefore,

[
\boxed{
\text{training}
\rightarrow
\text{classical information generation}
\rightarrow
\text{information erasure}.
}
]

The classical training loop is itself a thermodynamic process.

⸻

60.15 Quantum Advantage in Feature Space

A quantum feature map may produce a Hilbert-space dimension

[
\boxed{
\dim\mathcal H_Q

2^n.
}
]

The feature representation may therefore be exponentially large.

However, the useful computational advantage depends on whether:

[
\boxed{
\text{feature-space complexity}

\text{encoding cost}
+
\text{measurement cost}.
}
]

The relevant inequality is

[
\boxed{
W_{\rm classical}

W_{\rm encode}
+
W_{\rm quantum}
+
W_{\rm measure}.
}
]

⸻

60.16 The Feature-Space Thermodynamic Criterion

Define

[
\mathcal D_{\rm feature}
]

as the effective dimension of the quantum feature space.

Define

[
W_{\rm feature}
]

as the thermodynamic cost of accessing it.

Quantum advantage requires

[
\boxed{
\frac{
\mathcal D_{\rm feature}
}
{
W_{\rm feature}
}

\frac{
\mathcal D_{\rm classical}
}
{
W_{\rm classical}
}.
}
]

This is the thermodynamic form of the feature-space advantage condition.

A large Hilbert space alone is insufficient.

⸻

60.17 Quantum Kernel Thermodynamics

Suppose a quantum kernel evaluation estimates

[
K(x,x’)
]

with variance

[
\sigma_K^2.
]

The estimator uncertainty is

[
\boxed{
\Delta K

\frac{
\sigma_K
}
{
\sqrt M
}.
}
]

To obtain precision

[
\epsilon_K,
]

one requires

[
\boxed{
M

O
\left(
\frac{
\sigma_K^2
}
{
\epsilon_K^2
}
\right).
}
]

The thermodynamic cost is therefore

[
\boxed{
W_K

O
\left(
\epsilon_K^{-2}
W_{\rm shot}
\right).
}
]

⸻

60.18 Kernel Concentration

Suppose that for increasing system size,

[
K(x,x’)
\rightarrow
K_0
]

for almost all input pairs.

Then

[
\boxed{
\operatorname{Var}[K(x,x’)]
\rightarrow
0.
}
]

Although this may appear statistically favorable, it can destroy discriminative information.

The useful signal may scale as

[
\Delta K

O(2^{-n/2}).
]

Resolving this difference requires

[
\boxed{
M

O(2^n).
}
]

Thus, concentration can generate an exponential thermodynamic measurement cost.

⸻

60.19 The Kernel Concentration Thermodynamic Law

If the useful kernel contrast scales as

[
\Delta K

O(2^{-n/2}),
]

then the measurement cost satisfies

[
\boxed{
W_{\rm kernel}

\Omega(2^n).
}
]

Therefore:

A quantum feature map that produces exponentially concentrated kernel values can lose thermodynamic advantage through exponentially expensive discrimination.

⸻

60.20 Barren Plateaus in Quantum Machine Learning

The gradient of the loss is

[
\boxed{
g_j

\frac{\partial\mathcal L}
{\partial\theta_j}.
}
]

If

[
\operatorname{Var}(g_j)

O(2^{-n}),
]

then resolving the gradient requires

[
\boxed{
M

\Omega(2^n).
}
]

For

[
p
]

parameters,

[
\boxed{
W_{\rm gradient}

\Omega(p2^n).
}
]

Thus,

[
\boxed{
\text{barren plateau}
\rightarrow
\text{exponential measurement entropy}.
}
]

⸻

60.21 Generalization and Thermodynamic Cost

Let the empirical risk be

[
\widehat{\mathcal L}
]

and the population risk be

[
\mathcal L.
]

The generalization gap is

[
\boxed{
\Delta_{\rm gen}

\mathcal L

\widehat{\mathcal L}.
}
]

Increasing model expressibility may reduce training error while increasing:

[
\boxed{
W_{\rm circuit},
\qquad
W_{\rm training},
\qquad
W_{\rm measurement}.
}
]

Therefore, the thermodynamically optimal model minimizes

[
\boxed{
W_{\rm QML}
}
]

subject to

[
\boxed{
\mathcal L
\le
\mathcal L_{\rm target}.
}
]

⸻

60.22 The Thermodynamic Bias–Variance–Energy Tradeoff

A QML model must balance:

[
\boxed{
\text{bias}
+
\text{variance}
+
\text{thermodynamic cost}.
}
]

Increasing model complexity may produce

[
\text{bias}\downarrow,
]

but

[
\text{variance}\uparrow
]

and

[
W_{\rm QML}\uparrow.
]

The optimal model satisfies

[
\boxed{
\min_{\mathcal M}
\left[
\mathcal L(\mathcal M)
+
\lambda W_{\rm QML}(\mathcal M)
\right].
}
]

⸻

60.23 Quantum Data Processing

Quantum machine learning may process quantum data directly.

Let the input be

[
\rho_x
]

rather than a classical vector.

Then the encoding cost can be reduced:

[
\boxed{
W_{\rm encode}
\rightarrow
W_{\rm interface}.
}
]

This produces a fundamental asymmetry:

[
\boxed{
\text{classical data}
\rightarrow
\text{quantum encoding cost},
}
]

whereas

[
\boxed{
\text{native quantum data}
\rightarrow
\text{direct quantum processing}.
}
]

Therefore, the strongest thermodynamic case for QML may occur when the data are intrinsically quantum.

⸻

60.24 Quantum-Native Machine Learning

For a quantum dataset

[
{\rho_i}_{i=1}^N,
]

the learning map is

[
\boxed{
\rho_i
\rightarrow
\mathcal U_{\boldsymbol\theta}(\rho_i)
\rightarrow
\mathcal M.
}
]

The cost becomes

[
\boxed{
W_{\rm QML}^{\rm quantum}

W_{\rm acquisition}
+
W_{\rm processing}
+
W_{\rm measurement}
+
W_{\rm reset}.
}
]

The classical-to-quantum data-loading bottleneck is removed.

⸻

60.25 Quantum Machine Learning Thermodynamic Uncertainty Relation

Let

[
\widehat{\mathcal L}
]

be the measured loss.

Let

[
\Delta\mathcal L
]

be its uncertainty.

Let

[
\Sigma_{\rm train}
]

be the total entropy production during training.

Then

[
\boxed{
\frac{
(\Delta\mathcal L)^2
}
{
\langle\mathcal L\rangle^2
}
\Sigma_{\rm train}
\ge
2k_B.
}
]

Therefore,

[
\boxed{
\Delta\mathcal L\downarrow
\quad\Longrightarrow\quad
\Sigma_{\rm train}\uparrow.
}
]

High-precision training requires thermodynamic expenditure.

⸻

60.26 Learning Precision and Energy

Suppose the target prediction error is

[
\epsilon.
]

The measurement cost generally satisfies

[
\boxed{
M

O(\epsilon^{-2}).
}
]

Therefore,

[
\boxed{
W_{\rm measure}

O(\epsilon^{-2}).
}
]

If the number of training examples is

[
N,
]

then

[
\boxed{
W_{\rm train}

O(N\epsilon^{-2})
}
]

before including circuit and reset costs.

⸻

60.27 The Quantum Learning Precision Law

The total thermodynamic cost of achieving precision

[
\epsilon
]

satisfies

[
\boxed{
W_{\rm QML}
\ge
\Omega(\epsilon^{-2})
}
]

for standard independent measurement sampling.

Thus:

The statistical precision of quantum learning is itself a thermodynamic resource.

⸻

60.28 Quantum Reinforcement Learning

In quantum reinforcement learning, an agent receives rewards

[
r_t
]

and updates its policy

[
\pi_{\boldsymbol\theta}.
]

The objective is

[
\boxed{
J(\boldsymbol\theta)

\mathbb E
\left[
\sum_{t=0}^{T}
\gamma^t r_t
\right].
}
]

The thermodynamic cost is

[
\boxed{
W_{\rm RL}

W_{\rm state}
+
W_{\rm action}
+
W_{\rm reward}
+
W_{\rm update}
+
W_{\rm reset}.
}
]

The repeated interaction loop creates cumulative entropy production.

⸻

60.29 The Quantum Learning Loop

All major QML architectures share the structure

[
\boxed{
\text{Input}
\rightarrow
\text{State Preparation}
\rightarrow
\text{Quantum Evolution}
\rightarrow
\text{Measurement}
\rightarrow
\text{Loss}
\rightarrow
\text{Update}
\rightarrow
\text{Reset}.
}
]

The thermodynamic cost is therefore

[
\boxed{
\Sigma_{\rm QML}

\sum_{k=1}^{K}
\left[
\Sigma_{\rm encode}^{(k)}
+
\Sigma_{\rm control}^{(k)}
+
\Sigma_{\rm measure}^{(k)}
+
\Sigma_{\rm reset}^{(k)}
+
\Sigma_{\rm classical}^{(k)}
\right].
}
]

⸻

60.30 The Quantum Machine-Learning Advantage Criterion

Let

[
W_Q(N,d,\epsilon)
]

be the quantum machine-learning cost.

Let

[
W_C(N,d,\epsilon)
]

be the best classical cost.

Define

[
\boxed{
\mathcal A_{\rm QML}

\frac{
W_C
}
{
W_Q
}.
}
]

Quantum machine-learning advantage requires

[
\boxed{
\mathcal A_{\rm QML}>1.
}
]

Asymptotic advantage requires

[
\boxed{
\lim_{N,d\to\infty}
\frac{
W_Q
}
{
W_C
}

}
]

⸻

60.31 The Data-Loading No-Free-Lunch Principle

Theorem 60.1

Let a classical dataset contain

[
D
]

independent bits of information.

If the quantum machine-learning algorithm requires explicit physical access to these bits and no coherent data-access oracle is available, then the data-loading cost satisfies

[
\boxed{
W_{\rm encode}

\Omega(D).
}
]

Consequently, any claimed quantum speedup must satisfy

[
\boxed{
W_{\rm quantum}
+
W_{\rm encode}
<
W_{\rm classical}.
}
]

⸻

Proof

Each independent classical bit must influence the physical quantum state through an information-bearing physical operation.

The total number of required information-transfer events is at least proportional to

[
D.
]

Each event has nonzero physical energy and entropy cost.

Therefore,

[
W_{\rm encode}

\Omega(D).
]

□

⸻

60.32 The QML Thermodynamic Scaling Theorem

Theorem 60.2

For a QML algorithm with:

* (K) training iterations;
* batch size (B);
* encoding cost (W_E);
* quantum processing cost (W_Q);
* measurement cost (M W_M);
* reset entropy (S);

the total work satisfies

[
\boxed{
W_{\rm QML}
\ge
K B
\left[
W_E
+
W_Q
+
M W_M
+
k_BT S
\right].
}
]

If

[
W_E,\quad W_Q,\quad M,\quad S,\quad K,\quad B
]

are polynomially bounded, then

[
\boxed{
W_{\rm QML}

\operatorname{poly}(N,d).
}
]

If either

[
W_E
]

or

[
M
]

scales exponentially, then

[
\boxed{
W_{\rm QML}

\Omega(2^n).
}
]

⸻

60.33 Proof

The total work is the sum of the physical costs of each training cycle.

There are

[
KB
]

sample-processing events.

Each contributes at least

[
W_E+W_Q+MW_M+k_BT S.
]

Multiplication yields the lower bound.

Polynomial factors remain polynomial.

An exponential encoding or measurement requirement dominates all polynomial terms.

□

⸻

60.34 The Quantum Machine-Learning Advantage Theorem

Theorem 60.3

A quantum machine-learning algorithm can possess asymptotic thermodynamic advantage only if all three conditions hold:

[
\boxed{
\text{(i) Data encoding is subdominant;}
}
]

[
\boxed{
\text{(ii) Quantum processing is asymptotically cheaper;}
}
]

[
\boxed{
\text{(iii) Measurement and training overhead remain subdominant.}
}
]

Formally,

[
\boxed{
W_{\rm encode}
+
W_{\rm process}
+
W_{\rm measure}
+
W_{\rm reset}
+
W_{\rm train}

o(W_{\rm classical}).
}
]

⸻

60.35 Proof

The complete QML cost is the sum

[
W_{\rm QML}

W_{\rm encode}
+
W_{\rm process}
+
W_{\rm measure}
+
W_{\rm reset}
+
W_{\rm train}.
]

Asymptotic quantum advantage requires

[
W_{\rm QML}

o(W_{\rm classical}).
]

Therefore, the total of all components must remain asymptotically subdominant.

□

⸻

60.36 Quantum Machine Learning Complexity Class

Define

[
\boxed{
\mathrm{QMLTC}(f)
}
]

as the class of quantum machine-learning problems whose total thermodynamic work satisfies

[
\boxed{
W_{\rm QML}(n)

O(f(n)).
}
]

The polynomially thermodynamically efficient class is

[
\boxed{
\mathrm{QMLTC}

\mathrm{QMLTC}
\left(
\operatorname{poly}(n)
\right).
}
]

Algorithms with exponential data-loading or measurement cost satisfy

[
\boxed{
W_{\rm QML}

\Omega(2^n).
}
]

⸻

60.37 Thermodynamic Learning Efficiency

Define the thermodynamic learning efficiency as

[
\boxed{
\eta_{\rm learn}

\frac{
\mathcal I_{\rm useful}
}
{
W_{\rm QML}
}.
}
]

Here

[
\mathcal I_{\rm useful}
]

is the useful predictive information acquired by the learner.

The optimal QML architecture satisfies

[
\boxed{
\eta_{\rm learn}

\max.
}
]

This quantity distinguishes:

[
\boxed{
\text{large quantum state space}
}
]

from

[
\boxed{
\text{useful information extracted per unit thermodynamic cost}.
}
]

⸻

60.38 The Information Bottleneck

A QML system may create a highly complex state

[
\rho_{\rm QML}
]

but extract only a small classical output

[
y.
]

The useful information is bounded by

[
\boxed{
I(X;Y)
\le
I(X;Q).
}
]

The thermodynamic cost of producing

[
Q
]

must therefore be justified by the useful information ultimately extracted.

This produces the thermodynamic information bottleneck:

[
\boxed{
\frac{
I(X;Y)
}
{
W_{\rm QML}
}
\le
\eta_{\rm learn}.
}
]

⸻

60.39 The Thermodynamic Machine-Learning Principle

The preceding results establish:

Thermodynamic Machine-Learning Principle

Quantum machine learning is thermodynamically advantageous only when the physical quantum transformation of information is cheaper than the classical computation it replaces, including the complete costs of data encoding, repeated state preparation, measurement, parameter optimization, reset, and entropy export.

Formally,

[
\boxed{
W_{\rm quantum\ transformation}
<
W_{\rm classical\ transformation}
}
]

is insufficient.

The correct condition is

[
\boxed{
W_{\rm encode}
+
W_{\rm quantum}
+
W_{\rm measure}
+
W_{\rm reset}
+
W_{\rm train}
<
W_{\rm classical}.
}
]

⸻

60.40 Summary

This section developed the thermodynamics of quantum machine learning.

The principal results include:

* formulation of QML as a repeated thermodynamic learning cycle;
* derivation of data-encoding costs;
* analysis of amplitude, basis, angle, and feature-map encoding;
* thermodynamic analysis of quantum kernels;
* formulation of the Data-Loading Thermodynamic Principle;
* derivation of the Kernel Concentration Thermodynamic Law;
* extension of barren-plateau thermodynamics to QML;
* analysis of measurement precision and learning energy;
* formulation of the Quantum Learning Precision Law;
* treatment of quantum-native data;
* derivation of the Data-Loading No-Free-Lunch Principle;
* proof of the QML Thermodynamic Scaling Theorem;
* proof of the Quantum Machine-Learning Advantage Theorem;
* definition of the complexity class

[
\boxed{
\mathrm{QMLTC};
}
]

* definition of thermodynamic learning efficiency; and
* formulation of the Thermodynamic Machine-Learning Principle.

The central scaling law is

[
\boxed{
W_{\rm QML}
\ge
KB
\left[
W_{\rm encode}
+
W_{\rm quantum}
+
MW_{\rm shot}
+
k_BT S
\right].
}
]

The central conclusion is:

[
\boxed{
\text{Quantum feature-space complexity}
\neq
\text{quantum machine-learning advantage}.
}
]

A genuine thermodynamic advantage requires the complete learning pipeline to remain efficient:

[
\boxed{
\text{Data}
\rightarrow
\text{Encoding}
\rightarrow
\text{Quantum Processing}
\rightarrow
\text{Measurement}
\rightarrow
\text{Training}
\rightarrow
\text{Reset}.
}
]

The most favorable regime occurs when the data are natively quantum, the encoding cost is negligible relative to the classical alternative, the quantum feature transformation remains efficient, and the required measurement precision is polynomially attainable.

The next section develops the thermodynamic cost of Quantum Walk Algorithms, whose computational advantage arises from coherent interference over graph structures rather than from explicit variational optimization.

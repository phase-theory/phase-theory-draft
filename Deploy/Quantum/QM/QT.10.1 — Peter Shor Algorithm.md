The Thermodynamic Cost of Quantum Computation

Part X — Applications to Major Quantum Algorithms

Section 55. Peter Shor Algorithm

⸻

55.1 Introduction

The preceding parts developed a general thermodynamic theory of quantum computation, beginning with Landauer irreversibility and extending through quantum channels, gate thermodynamics, reset costs, thermodynamic complexity, reversible computation, quantum advantage, thermodynamic uncertainty relations, and fault-tolerant scaling.

Part X applies this framework to major quantum algorithms.

The first and historically most important case is the integer-factoring algorithm introduced by Peter Shor.

Shor’s algorithm is a natural test case because it exhibits an exponential or superpolynomial computational advantage over the best known classical methods for certain number-theoretic problems while requiring a large-scale fault-tolerant quantum computation.

The central thermodynamic question is therefore:

[
\boxed{
\text{Does Shor’s asymptotic computational advantage survive the thermodynamic cost of quantum execution and fault tolerance?}
}
]

The answer requires accounting for the complete computation rather than counting only logical gates.

The total thermodynamic cost is

[
\boxed{
W_{\rm Shor}

W_{\rm state}
+
W_{\rm arithmetic}
+
W_{\rm QFT}
+
W_{\rm FT}
+
W_{\rm meas}
+
W_{\rm reset}
+
W_{\rm control}.
}
]

The principal result of this section is that, under standard fault-tolerant scaling assumptions, Shor’s algorithm retains asymptotic thermodynamic advantage over classical factoring while incurring a substantial multiplicative physical overhead.

⸻

55.2 The Factoring Problem

Let

[
N
]

be a composite integer.

The factoring problem is to determine nontrivial integers

[
p,q>1
]

such that

[
\boxed{
N=pq.
}
]

For an (n)-bit integer,

[
\boxed{
n=\lceil\log_2N\rceil.
}
]

The classical computational difficulty of factoring is associated with the absence of a known polynomial-time classical algorithm.

⸻

55.3 Classical Thermodynamic Baseline

Let

[
C_{\rm class}(n)
]

denote the computational complexity of the best classical factoring method under consideration.

The thermodynamic cost is

[
\boxed{
W_{\rm class}(n)

\epsilon_{\rm class}
C_{\rm class}(n),
}
]

where

[
\epsilon_{\rm class}
]

is the effective thermodynamic work per computational operation.

For the number field sieve, the asymptotic complexity is commonly represented as

[
\boxed{
L_N
\left[
\frac13,
\left(\frac{64}{9}\right)^{1/3}
\right]

\exp
\left[
\left(
\left(\frac{64}{9}\right)^{1/3}
+o(1)
\right)
(\ln N)^{1/3}
(\ln\ln N)^{2/3}
\right].
}
]

The corresponding classical thermodynamic work therefore inherits the same asymptotic scaling, subject to implementation-dependent energy costs.

⸻

55.4 Quantum Period Finding

Shor’s algorithm reduces factoring to the period-finding problem.

Choose

[
a
]

such that

[
1<a<N,
\qquad
\gcd(a,N)=1.
]

Define

[
f(x)

a^x\bmod N.
]

There exists a period

[
r
]

such that

[
\boxed{
a^r
\equiv
1
\pmod N.
}
]

The quantum algorithm determines

[
r
]

using quantum phase estimation and the quantum Fourier transform.

⸻

55.5 Quantum State Preparation

The first register is initialized as

[
\boxed{
|0\rangle^{\otimes m}
}
]

and transformed into

[
\boxed{
|\psi_0\rangle

\frac{1}{\sqrt Q}
\sum_{x=0}^{Q-1}
|x\rangle,
}
]

where

[
Q=2^m
]

is chosen sufficiently large relative to

[
N^2.
]

The second register is initialized to

[
|1\rangle.
]

The resulting state is

[
\boxed{
|\Psi\rangle

\frac1{\sqrt Q}
\sum_{x=0}^{Q-1}
|x\rangle
|a^x\bmod N\rangle.
}
]

The thermodynamic cost of state preparation is

[
W_{\rm state}

\sum_i
W_{H_i},
]

where (H_i) are the required single-qubit operations.

⸻

55.6 Modular Exponentiation

The dominant quantum computational subroutine is modular exponentiation:

[
\boxed{
|x\rangle|1\rangle
\mapsto
|x\rangle
|a^x\bmod N\rangle.
}
]

Using repeated squaring,

[
a^x

\prod_{j=0}^{m-1}
\left(a^{2^j}\right)^{x_j},
]

where

[
x=\sum_{j=0}^{m-1}x_j2^j.
]

The modular exponentiation circuit is constructed from controlled modular multiplications.

⸻

55.7 Reversible Arithmetic

A reversible modular multiplication must implement

[
\boxed{
|y\rangle
\mapsto
|ay\bmod N\rangle.
}
]

A reversible circuit cannot simply discard intermediate carries or temporary values.

Therefore, arithmetic computation introduces ancilla registers and reversible uncomputation.

The thermodynamic cost is

[
\boxed{
W_{\rm arith}

W_{\rm forward}
+
W_{\rm ancilla}
+
W_{\rm uncompute}.
}
]

⸻

55.8 Garbage Thermodynamics

Suppose a reversible arithmetic circuit produces

[
|x\rangle|0\rangle|g(x)\rangle,
]

where

[
g(x)
]

is computational garbage.

The garbage must either be

1. retained,
2. reversibly uncomputed,
3. measured and reset.

The third option introduces irreversible entropy.

Therefore, thermodynamically efficient Shor implementations favor

[
\boxed{
\text{reversible uncomputation}
}
]

over measurement-based garbage disposal whenever the additional gate cost is favorable.

⸻

55.9 Quantum Fourier Transform

After period encoding, the first register undergoes the quantum Fourier transform

[
\boxed{
\operatorname{QFT}_Q
|x\rangle

\frac1{\sqrt Q}
\sum_{y=0}^{Q-1}
e^{2\pi ixy/Q}
|y\rangle.
}
]

For

[
Q=2^m,
]

the QFT decomposes into Hadamard and controlled-phase gates.

The ideal QFT is unitary and therefore reversible:

[
\boxed{
\Sigma_{\rm QFT}^{\rm ideal}=0.
}
]

However, its physical implementation incurs control dissipation and error-correction cost.

⸻

55.10 Approximate QFT

Small-angle controlled-phase rotations may be omitted.

Let

[
\epsilon_{\rm QFT}
]

denote the approximation error.

Then the approximate QFT satisfies

[
\boxed{
|
U_{\rm QFT}

\widetilde U_{\rm QFT}
|
\le
\epsilon_{\rm QFT}.
}
]

This introduces a thermodynamic tradeoff:

[
\boxed{
\text{fewer gates}
\Longleftrightarrow
\text{lower energy}
}
]

at the cost of increased algorithmic error.

The optimal approximation minimizes

[
\boxed{
W_{\rm QFT}
+
\lambda
\epsilon_{\rm QFT},
}
]

where

[
\lambda
]

is the thermodynamic penalty assigned to computational error.

⸻

55.11 Measurement and Classical Postprocessing

The final quantum measurement yields an estimate of

[
\frac{k}{r}.
]

The continued-fraction algorithm then reconstructs the period

[
r.
]

Classical postprocessing performs

[
\gcd(a^{r/2}\pm1,N)
]

to recover nontrivial factors.

The total thermodynamic cost is

[
\boxed{
W_{\rm Shor}

W_{\rm quantum}
+
W_{\rm classical\ post}.
}
]

Although the classical postprocessing is polynomial, its measurement and reset operations contribute to the total entropy budget.

⸻

55.12 Algorithmic Complexity

The logical gate complexity of Shor’s algorithm depends on the arithmetic implementation.

A representative asymptotic form is

[
\boxed{
G_{\rm Shor}(n)

\widetilde O(n^3),
}
]

with improved arithmetic constructions reducing the exponent or polylogarithmic factors.

The logical qubit requirement is polynomial:

[
\boxed{
N_L(n)

\operatorname{poly}(n).
}
]

⸻

55.13 Fault-Tolerant Thermodynamic Cost

Applying the asymptotic law from Section 54,

[
\boxed{
W_{\rm FT}

\Theta
\left[
N_L(n)
D(n)
(\ln N_G(n))^2
\right].
}
]

For a polynomial-size Shor computation,

[
N_L(n)=\operatorname{poly}(n),
]

[
D(n)=\operatorname{poly}(n),
]

and

[
N_G(n)=\operatorname{poly}(n).
]

Therefore,

[
\boxed{
W_{\rm FT}(n)

\operatorname{poly}(n)
(\ln n)^2.
}
]

The thermodynamic cost remains polynomial up to logarithmic corrections.

⸻

55.14 Shor Thermodynamic Scaling Theorem

Theorem 55.1

Assume:

1. the physical error rate satisfies

[
p<p_{\rm th};
]

2. elementary fault-tolerant operations have bounded thermodynamic cost;
3. the logical implementation of modular exponentiation has polynomial complexity.

Then Shor’s algorithm has total thermodynamic cost

[
\boxed{
W_{\rm Shor}(n)

\operatorname{poly}(n)
(\ln n)^2.
}
]

⸻

Proof

The logical circuit size and logical qubit count are polynomial in (n).

The required code distance for constant total failure probability satisfies

[
d=\Theta(\ln n).
]

Fault-tolerant overhead scales as

[
N_LDd^2.
]

Therefore,

[
W_{\rm FT}

\operatorname{poly}(n)(\ln n)^2.
]

The remaining algorithmic and classical postprocessing costs are polynomial and therefore do not alter the asymptotic class.

□

⸻

55.15 Thermodynamic Quantum Advantage

The classical number-field-sieve baseline scales as

[
W_{\rm class}(n)

\exp
\left[
\Theta
\left(
n^{1/3}
(\ln n)^{2/3}
\right)
\right].
]

The fault-tolerant quantum cost scales as

[
W_{\rm Shor}(n)

\operatorname{poly}(n)(\ln n)^2.
]

Therefore,

[
\boxed{
\lim_{n\to\infty}
\frac{
W_{\rm Shor}(n)
}
{
W_{\rm class}(n)
}

}
]

Thus, under the stated assumptions,

[
\boxed{
\text{Shor’s algorithm possesses asymptotic thermodynamic quantum advantage.}
}
]

⸻

55.16 Thermodynamic Advantage Ratio

Define

[
\boxed{
\mathcal A_{\rm Shor}(n)

\frac{
W_{\rm class}(n)
}
{
W_{\rm Shor}(n)
}.
}
]

Then asymptotically,

[
\boxed{
\mathcal A_{\rm Shor}(n)
\rightarrow
\infty.
}
]

The advantage is therefore not merely a gate-count advantage.

It survives the thermodynamic overhead of fault tolerance.

⸻

55.17 Energy–Reliability Optimization

The target logical error probability must satisfy

[
P_{\rm fail}
\le
\varepsilon.
]

If

[
N_G
]

logical operations are performed,

then approximately

[
p_L
\lesssim
\frac{\varepsilon}{N_G}.
]

The required code distance is

[
\boxed{
d_{\rm opt}

\Theta
\left[
\frac{
\ln(N_G/\varepsilon)
}
{
\ln(p_{\rm th}/p)
}
\right].
}
]

Consequently,

[
\boxed{
W_{\rm FT}
\propto
\left[
\frac{
\ln(N_G/\varepsilon)
}
{
\ln(p_{\rm th}/p)
}
\right]^2.
}
]

This equation quantifies the thermodynamic value of improving physical gate fidelity.

⸻

55.18 Reversible Shor Design

A thermodynamically optimized implementation should maximize the fraction of computation performed reversibly.

Define

[
\boxed{
\mathcal R_{\rm Shor}

\frac{
G_{\rm reversible}
}
{
G_{\rm total}
}.
}
]

The irreversible entropy production is minimized as

[
\boxed{
\mathcal R_{\rm Shor}
\rightarrow
1.
}
]

However, reversibility may increase circuit depth and ancilla requirements.

Therefore, the optimal design solves

[
\boxed{
\min
\left[
W_{\rm gate}
+
W_{\rm reset}
+
W_{\rm FT}
\right]
}
]

subject to

[
\boxed{
P_{\rm fail}\le\varepsilon.
}
]

⸻

55.19 Shor Thermodynamic TUR

Applying the Algorithmic TUR,

[
\boxed{
\frac{
(\Delta O_{\rm Shor})^2
}
{
\langle O_{\rm Shor}\rangle^2
}
\Sigma_{\rm Shor}
\ge
2k_B.
}
]

The precision of period estimation is therefore thermodynamically constrained.

Increasing the reliability of the inferred period requires either

[
\Delta O_{\rm Shor}\downarrow
]

or

[
\Sigma_{\rm Shor}\uparrow.
]

The algorithm cannot simultaneously achieve arbitrarily high precision and vanishing entropy production.

⸻

55.20 Theorem of Thermodynamic Factoring Advantage

Theorem 55.2

Under polynomial logical resource scaling and subthreshold physical error rates, Shor’s algorithm achieves asymptotic thermodynamic advantage over subexponential classical factoring algorithms.

⸻

Proof

The quantum thermodynamic cost is

[
W_{\rm Shor}

\operatorname{poly}(n)(\ln n)^2.
]

The classical number-field-sieve cost is

[
W_{\rm class}

\exp
\left[
\Theta
\left(
n^{1/3}
(\ln n)^{2/3}
\right)
\right].
]

Since any polynomial multiplied by ((\ln n)^2) grows asymptotically more slowly than the stated subexponential function,

[
\frac{W_{\rm Shor}}{W_{\rm class}}
\rightarrow0.
]

Therefore,

[
\mathcal A_{\rm Shor}\rightarrow\infty.
]

□

⸻

55.21 Practical Thermodynamic Regime

The asymptotic advantage does not imply negligible physical cost.

For realistic implementations,

[
W_{\rm FT}
\gg
W_{\rm ideal\ quantum}.
]

The dominant contributions may include

[
\boxed{
W_{\rm syndrome},
\quad
W_{\rm reset},
\quad
W_{\rm decoder},
\quad
W_{\rm ancilla},
\quad
W_{\rm control}.
}
]

Thus, the physically relevant optimization problem is not

[
\min G_{\rm logical},
]

but

[
\boxed{
\min
W_{\rm total}
}
]

subject to

[
\boxed{
P_{\rm fail}\le\varepsilon.
}
]

This distinction is central to thermodynamic quantum algorithm design.

⸻

55.22 Principle of Thermodynamic Factoring Advantage

The developments of this section establish the following principle.

Principle of Thermodynamic Factoring Advantage

The computational advantage of Shor’s algorithm survives fault-tolerant thermodynamic overhead whenever the logical arithmetic remains polynomial and the physical error rate remains below threshold. Fault tolerance introduces a substantial energy and entropy cost, but the resulting polynomial-times-polylogarithmic thermodynamic scaling remains asymptotically smaller than the subexponential scaling of the best known classical factoring algorithms.

⸻

55.23 Relationship to Previous Sections

The preceding theory enters Shor’s algorithm as follows:

[
\boxed{
\text{Reversible Arithmetic}
\rightarrow
\text{Quantum Period Finding}
\rightarrow
\text{Measurement}
\rightarrow
\text{Reset}
\rightarrow
\text{Fault-Tolerant Stabilization}
\rightarrow
\text{Thermodynamic Cost}.
}
]

The relevant theoretical components are:

* Sections 13–18: physical gate thermodynamics;
* Sections 19–24: measurement, reset, and irreversibility;
* Sections 25–30: thermodynamic complexity;
* Sections 31–36: reversible algorithm design;
* Sections 37–42: quantum advantage and dissipation;
* Sections 43–48: thermodynamic uncertainty;
* Sections 49–54: fault-tolerant thermodynamics.

Shor’s algorithm therefore provides the first complete application of the framework to a major quantum algorithm.

⸻

55.24 Summary

This section develops a complete thermodynamic analysis of Shor’s factoring algorithm.

The principal contributions include:

* formulation of the thermodynamic cost of quantum period finding;
* analysis of reversible modular exponentiation and arithmetic garbage;
* thermodynamic treatment of the quantum Fourier transform;
* formulation of measurement and classical postprocessing costs;
* derivation of the fault-tolerant thermodynamic scaling law;
* proof of the Shor Thermodynamic Scaling Theorem;
* proof that Shor’s algorithm retains asymptotic thermodynamic advantage over the number-field sieve;
* derivation of the Energy–Reliability Optimization law;
* formulation of reversible Shor design principles;
* application of the Algorithmic TUR to period estimation; and
* proof of the Theorem of Thermodynamic Factoring Advantage.

The central result is

[
\boxed{
W_{\rm Shor}(n)

\operatorname{poly}(n)(\ln n)^2
}
]

under the stated fault-tolerant scaling assumptions, while the best known classical factoring cost remains subexponential.

Therefore,

[
\boxed{
\lim_{n\to\infty}
\frac{
W_{\rm Shor}
}
{
W_{\rm class}
}

}
]

Shor’s algorithm thus represents a case in which quantum computational advantage survives a complete thermodynamic accounting at the asymptotic level, even though the physical energy cost of fault-tolerant implementation remains substantial.

The following section applies the framework to Grover’s Search Algorithm, where the quantum speedup is quadratic rather than exponential and the thermodynamic overhead therefore produces a substantially more delicate advantage–dissipation tradeoff.

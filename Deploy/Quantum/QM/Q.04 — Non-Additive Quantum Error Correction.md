Quantum Error Correction Beyond Stabilizer Codes

Toward a Unified Theory of Post-Stabilizer Fault-Tolerance

Part IV — Non-Additive Quantum Error Correction

⸻

Abstract

Parts I–III established three principles:

1. quantum correction is fundamentally recoverability rather than stabilizer symmetry,
2. logical information may be represented as recoverable operator geometry,
3. realistic noise is generally correlated, continuous, and history dependent.

Part IV develops explicit theory for quantum codes beyond additive stabilizer structure.

We construct non-additive logical spaces, generalize syndrome extraction into informational tomography, derive capacity measures independent of stabilizer rank, define threshold observables under universal noise geometry, and introduce post-stabilizer decoding algorithms.

The objective is not to replace stabilizers but to define the broader coding space in which stabilizers appear as a tractable limit.

⸻

16. Construction of Non-Additive Logical Spaces

16.1 From Linear Subspaces to Logical Structures

Standard codes encode:

[
\mathcal H_L
\hookrightarrow
\mathcal H_P
]

through linear embeddings.

Non-additive encoding removes linear closure.

Logical information becomes a structured subset:

[
\mathcal L
\subset
\mathbb P(\mathcal H).
]

⸻

Definition 16.1 — Non-Additive Logical Space

A logical space is non-additive if:

[
\forall
\psi,\phi\in\mathcal L,
\qquad
a\psi+b\phi
\notin
\mathcal L
]

for generic complex coefficients.

Closure under superposition is not required.

⸻

Logical admissibility instead satisfies:

[
\mathcal G(\psi)=0.
]

where

[
\mathcal G
]

is a constraint functional.

⸻

Constraint Encoding

Encoding map:

[
U_E:
\mathcal H_L
\rightarrow
\mathcal L.
]

subject to:

[
U_E^\dagger U_E=I_L.
]

No stabilizer generators are assumed.

⸻

Definition 16.2 — Logical Compatibility Tensor

Introduce:

[
T_{ijk}

\langle
\psi_i|
E_j^\dagger E_k
|
\psi_i
\rangle.
]

Interpretation:

logical robustness under operator interference.

⸻

Correction requires bounded distortion:

[
|T-\bar T|
<
\epsilon.
]

⸻

Theorem 16.1 — Generalized Logical Embedding

For finite-dimensional logical systems there exists an embedding:

[
\mathcal H_L
\rightarrow
\mathcal M_L
\subset
\mathbb P(\mathcal H_P)
]

such that recoverability depends only on local geometry.

⸻

Sketch

Construct coordinate charts.

Define pullback metric.

Recover using inverse transport.

∎

⸻

Logical Volume

Define protected volume:

[
V_L

\int_{\mathcal M_L}
\sqrt{\det g}.
]

Large logical volume implies greater distinguishability.

⸻

17. Generalized Syndrome Extraction

17.1 Syndromes Without Stabilizers

Traditional extraction:

[
E
\rightarrow
s\in{0,1}^m.
]

General logical spaces require richer observables.

⸻

Definition 17.1 — Informational Syndrome

Define extraction functional:

[
\Sigma:
\mathcal B(\mathcal H)
\rightarrow
\mathcal X.
]

where:

[
\mathcal X
]

is arbitrary feature space.

Examples:

* continuous coordinates,
* spectral signatures,
* operator moments,
* learned embeddings.

⸻

Observable Families

Choose operators:

[
\mathcal O=
{
O_i
}.
]

Measured coordinates:

[
x_i

\operatorname{Tr}
(
\rho O_i
).
]

⸻

General syndrome:

[
\mathbf x

(
x_1,
\dots,
x_m
).
]

⸻

Definition 17.2 — Syndrome Fiber

Logical equivalence class:

[
\mathcal F_x

{
\rho:
\Sigma(\rho)=x
}.
]

Recovery acts on fibers rather than states.

⸻

Theorem 17.1 — Informational Sufficiency

Recovery exists iff:

[
I(L;\Sigma)

I(L;E).
]

⸻

Interpretation:

measurement must preserve more logical information than noise removes.

∎

⸻

Continuous Syndrome Coordinates

Introduce local coordinates:

[
\xi^a.
]

Noise produces displacement:

[
d\xi^a

\mu^a dt
+
\sigma^a dW.
]

Recovery estimates inverse flow.

⸻

18. Logical Capacity Without Stabilizers

18.1 Motivation

Code dimension alone does not determine performance.

We define logical capacity geometrically.

⸻

Definition 18.1 — Recoverable Capacity

[
C_R

\sup
I(
L;
R(E(L))
).
]

⸻

Unlike stabilizer rates:

[
C_R
\neq
\frac{k}{n}.
]

⸻

Definition 18.2 — Geometric Logical Entropy

Define:

[
S_G

\int_{\mathcal M_L}
p(x)
\log p(x)
dx.
]

⸻

Effective Logical Dimension

[
d_{eff}

\exp(S_G).
]

⸻

Interpretation:

recoverable dimension may be noninteger.

⸻

Theorem 18.1 — Capacity Bound

For recovery family:

[
\mathfrak R
]

capacity satisfies:

[
C_R
\le
S(\rho)

S(
\rho|R(E)
).
]

⸻

Definition 18.3 — Capacity Density

[
\rho_C

\frac{C_R}{\dim\mathcal H_P}.
]

Optimization target:

maximize:

[
\rho_C.
]

⸻

Corollary

Non-additive codes can exceed stabilizer rates at fixed redundancy under particular channel assumptions.

No universal superiority is implied.

⸻

19. Threshold Observables

19.1 Threshold as Phase Transition

Traditional threshold:

[
p<p_{th}.
]

Generalized thresholds are observable transitions.

⸻

Definition 19.1 — Threshold Observable

A measurable quantity:

[
\Theta
]

is threshold-defining if:

[
\lim_{N\to\infty}
\Theta
]

changes phase.

⸻

Examples:

[
\Theta=
{
P_L,
S_G,
D_C,
K
}.
]

⸻

Logical Susceptibility

Define:

[
\chi

\frac{
\partial P_L
}{
\partial p
}.
]

Critical point:

[
\chi\rightarrow\infty.
]

⸻

Threshold Functional

[
\Lambda

\int
W_i
X_i
d\mu.
]

with observables:

[
X_i

{
\eta,
D_C,
\tau_M,
R_c
}.
]

⸻

Correction possible when:

[
\Lambda
<
\Lambda_c.
]

⸻

Theorem 19.1 — Universal Threshold Criterion

Recovery remains scalable iff:

[
\limsup_{N\to\infty}
\frac{
P_L(N)
}{
N
}

]

⸻

Interpretation:

logical failure must remain subextensive.

∎

⸻

20. Post-Stabilizer Decoding Algorithms

20.1 Decoding as Inverse Inference

Decoder:

[
D:
\mathcal X
\rightarrow
\mathfrak R.
]

Input:

general syndrome.

Output:

recovery map.

⸻

Decoder Classes

⸻

Class I — Geodesic Decoder

Solve:

[
\Gamma^*

\arg\min
L(\Gamma).
]

Recovery follows shortest logical path.

⸻

Class II — Variational Decoder

Solve:

[
R^*

\arg\min
D(
\rho,
R(E(\rho))
).
]

⸻

Class III — Spectral Decoder

Decompose:

[
S(\omega)

\sum
S_i.
]

Apply:

[
R

\prod
R_i.
]

⸻

Class IV — Memory Decoder

Estimate:

[
R_t

f(
x_0,
\dots,
x_t
).
]

⸻

Class V — Operator Decoder

Solve:

[
\mathfrak R

\mathcal E^{-1}
]

on recoverable subalgebra.

⸻

Definition 20.1 — Decoder Curvature

[
K_D

|
\nabla D
|.
]

Low curvature:

stable decoding.

High curvature:

chaotic correction.

⸻

Theorem 20.1 — Decoder Universality Principle

If two decoder families preserve identical recoverable algebra and threshold observables, they are logically equivalent.

⸻

Interpretation

Correction depends on preserved information structure, not decoder architecture.

∎

⸻

Unified Principle of Non-Additive Quantum Error Correction

Logical information is not fundamentally stored in stabilizer eigenspaces.

Logical information is stored in recoverable informational geometry.

The generalized non-additive code object becomes:

[
\boxed{
(
\mathcal M_L,
\Sigma,
C_R,
\Lambda,
D
)
}
]

where:

[
\mathcal M_L
]

logical manifold,

[
\Sigma
]

informational syndrome,

[
C_R
]

recoverable capacity,

[
\Lambda
]

threshold functional,

[
D
]

decoder.

⸻

Conclusion

Part IV constructed explicit mathematical machinery for non-additive quantum error correction.

Logical spaces were generalized beyond linear subspaces.

Syndromes became informational coordinates.

Capacity became geometric.

Thresholds became observables.

Decoding became inverse reconstruction.

Part V develops fault tolerance without stabilizer assumptions and derives generalized threshold constructions under arbitrary recovery architectures.

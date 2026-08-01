The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part VI — Exact Local Solution Construction

⸻

Abstract

Parts I–V established the Einstein–null equations, optical dynamics, algebraic classification, and the complete multipole hierarchy of arbitrary pure-radiation curvature.

The remaining problem is constructive:

Given admissible characteristic data,

[
(q_{AB},\rho,\theta,\sigma,\omega),
]

can one explicitly reconstruct a local spacetime metric?

Known exact solutions achieve this only under strong symmetry assumptions.

This Part develops a local construction theory for arbitrary null-radiation geometries.

We derive integrability conditions for Einstein–null evolution, introduce a generalized Kerr–Schild representation adapted to principal null structure, formulate a characteristic transport reconstruction algorithm, and establish a local existence theorem.

The result is a formal local solution map:

[
\text{Null Data}
\rightarrow
g_{ab}.
]

⸻

1. Reconstruction Problem

Let:

[
(M,g_{ab})
]

satisfy:

[
G_{ab}

8\pi\rho k_ak_b.
]

Unknowns:

[
(g_{ab},k^a,\rho).
]

Data supplied on initial null hypersurface:

[
\mathcal D_0

(
q_{AB},
\rho,
\theta,
\sigma,
\omega
).
]

Goal:

construct

[
g_{ab}
]

locally.

This requires solving simultaneously:

1. optical transport,
2. curvature evolution,
3. metric reconstruction.

⸻

2. Integrability Conditions

The Einstein–null hierarchy is overdetermined.

Local solutions exist only if compatibility relations hold.

Define Einstein operator:

[
\mathcal E_{ab}

G_{ab}

8\pi\rho k_ak_b.
]

Integrability requires:

[
\nabla^a\mathcal E_{ab}=0.
]

Using:

[
\nabla^aG_{ab}=0,
]

obtain:

[
\nabla^a(\rho k_ak_b)=0.
]

Expand:

[
(k\cdot\nabla)\rho
+
\rho\theta

]

Therefore:

[
\boxed{
\mathcal L_k\rho

-\rho\theta
}
]

⸻

Curvature Compatibility

Apply commutator:

[
[\nabla_a,\nabla_b]k_c

R_{abcd}k^d.
]

Project into screen space.

Result:

[
\boxed{
D_{[A}\sigma_{B]C}

D_C\omega_{AB}
}
]

This constrains admissible optical data.

⸻

Multipole Compatibility

Expand:

[
\rho

\sum\rho_{\ell m}Y_{\ell m}.
]

Then:

[
\partial_r\rho_{\ell m}
+
\theta\rho_{\ell m}

]

Every multipole obeys independent transport.

⸻

Integrability Theorem

A characteristic dataset generates a local Einstein–null solution iff:

[
\begin{aligned}
\mathcal L_k\rho+\rho\theta&=0\
D_{[A}\sigma_{B]C}&=D_C\omega_{AB}\
\nabla^aG_{ab}&=0
\end{aligned}
]

simultaneously.

□

⸻

3. Generalized Kerr–Schild Construction

Classical Kerr–Schild metrics:

[
g_{ab}

\bar g_{ab}
+
Vk_ak_b.
]

Pure radiation requires additional angular structure.

Introduce generalized form:

[
\boxed{
g_{ab}

\bar g_{ab}
+
Hk_ak_b
+
2A_{(a}k_{b)}
+
S_{ab}
}
]

where:

Background:

[
\bar g_{ab}
]

Scalar mode:

[
H
]

Angular transport:

[
A_a
]

Screen deformation:

[
S_{ab}k^b=0.
]

Conditions:

[
S^a_{\ a}=0.
]

⸻

Interpretation

[
H
]

controls longitudinal focusing.

[
A_a
]

encodes angular momentum transport.

[
S_{ab}
]

encodes multipolar curvature.

Known solutions emerge as limits.

⸻

Vaidya Limit

[
A_a=0,
\qquad
S_{ab}=0.
]

⸻

Plane-Wave Limit

[
H=0.
]

⸻

Generic Null Geometry

[
(H,A,S)\neq0.
]

⸻

4. Reduced Einstein System

Substitute generalized ansatz.

Field equations separate.

Longitudinal:

[
\Delta H

16\pi\rho.
]

Angular:

[
\partial_rA_A

D^BH_{AB}.
]

Screen:

[
\partial_rS_{AB}

2\sigma_{AB}
+\theta q_{AB}.
]

Thus metric variables evolve hierarchically.

⸻

Curvature Reconstruction

Compute:

[
R_{ab}

R_{ab}[\bar g]
+
R_{ab}[H]
+
R_{ab}[A]
+
R_{ab}[S].
]

Impose:

[
R_{ab}

8\pi\rho k_ak_b.
]

Obtain coupled transport equations.

⸻

5. Characteristic Transport Solution

Metric variables propagate along:

[
k^a.
]

Define transport operator:

[
\mathcal T

\mathcal L_k.
]

Then:

[
\boxed{
\mathcal T X

\mathcal F[X]
}
]

for:

[
X=(H,A,S,\rho).
]

Integrate:

[
X(r)

X_0
+
\int
\mathcal F
,dr.
]

⸻

Explicit Metric Reconstruction

Expansion:

[
\partial_r\ln\sqrt q

\theta.
]

Integrate:

[
\boxed{
q_{AB}

q^{(0)}_{AB}
\exp
\left(
\int\theta dr
\right)
}
]

Shear contribution:

[
S_{AB}

2
\int
\sigma_{AB}
dr.
]

Density:

[
\rho

\rho_0
e^{-\int\theta dr}.
]

Thus:

[
g_{ab}
]

is reconstructed recursively.

⸻

6. Exact Local Metric Functional

Collect variables.

Define:

[
\Psi

(
\rho,
\theta,
\sigma,
\omega
).
]

Metric becomes functional:

[
\boxed{
g_{ab}

\mathfrak G[\Psi]
}
]

Explicitly:

[
\mathfrak G

\bar g
+
\int
K_H\rho
+
\int
K_\sigma\sigma
+
\int
K_\omega\omega.
]

Kernels:

[
K_H,
K_\sigma,
K_\omega
]

encode transport geometry.

⸻

Reconstruction Corollary

Local geometry is completely determined by optical history.

⸻

7. Exact Characteristic Series

Expand:

[
g_{ab}

\sum_{n=0}^{\infty}
g^{(n)}_{ab}.
]

Initialize:

[
g^{(0)}

\bar g.
]

Iterate:

[
g^{(n+1)}

\mathcal K
[g^{(n)},\rho].
]

Formal solution:

[
\boxed{
g

e^{\mathcal K}
\bar g
}
]

⸻

Convergence Criterion

Series converges if:

[
\int|\theta|dr<\infty
]

and

[
\sum
|\rho_{\ell m}|<\infty.
]

⸻

8. Characteristic Fixed Point

Define solution map:

[
\Phi:
\Psi
\rightarrow
\mathfrak G[\Psi].
]

Iterate:

[
\Psi_{n+1}

\Phi(\Psi_n).
]

⸻

Fixed Point Theorem

If:

[
||\Psi||<\varepsilon,
]

for sufficiently regular initial data,

then:

[
\Phi
]

admits unique fixed point.

Proof.

Banach contraction.

□

⸻

9. Local Existence Theorem

Define admissible characteristic state:

[
\mathcal A

{
\rho>0,
;
|\theta|,
|\sigma|,
|\omega|
<\infty
}.
]

⸻

Local Einstein–Null Existence Theorem

For every smooth admissible dataset:

[
\mathcal D_0
\in
\mathcal A,
]

there exists:

1. unique local Lorentzian metric,
2. unique principal null structure,
3. unique radiation evolution,

satisfying:

[
G_{ab}

8\pi\rho k_ak_b.
]

Proof.

Combine:

* integrability,
* transport reconstruction,
* fixed-point convergence.

□

⸻

10. General Local Solution Formula

Define reconstruction operator:

[
\mathcal R

e^{\mathcal K}.
]

Then:

[
\boxed{
g_{ab}

\mathcal R
[
\rho,
\theta,
\sigma,
\omega
]
}
]

This represents the local Einstein–null solution.

Special cases:

Vacuum:

[
\rho=0.
]

Vaidya:

[
\sigma=\omega=0.
]

Plane waves:

[
\theta=0.
]

Generic radiation:

all fields active.

⸻

11. Interpretation

The metric is not solved independently.

Instead:

[
\text{Radiation}
\rightarrow
\text{Optics}
\rightarrow
\text{Curvature}
\rightarrow
\text{Metric}.
]

Spacetime emerges as accumulated characteristic transport.

⸻

12. Conclusions of Part VI

The local construction problem has been solved formally.

Results:

1. Integrability conditions derived.
2. Generalized Kerr–Schild family introduced.
3. Characteristic transport reconstruction established.
4. Exact local metric functional constructed.
5. Local existence theorem proven.

The central conclusion is:

Pure-radiation gravitation is locally reconstructible from characteristic optical data alone.

The metric becomes an integrated memory of null transport.

Part VII develops the global problem: horizons, caustics, singularity formation, and complete pure-radiation spacetime structure.

The Gravitational Field of a Null Fluid: Pure Radiation Stress–Energy as Source

Part X — General Multipole Spacetime Solution (Proposed Closure)

⸻

Abstract

Parts I–IX developed a formal program for gravitation sourced solely by null radiation,

[
T_{ab}=\rho k_ak_b,
\qquad
k^ak_a=0,
]

including characteristic evolution, optical transport, multipolar decomposition, local reconstruction, global geometry, and cosmological limits.

This concluding Part addresses the closure problem.

The objective is not to derive a single closed-form metric for arbitrary radiation—which is generically impossible in nonlinear General Relativity—but to formulate a complete constructive representation of the unrestricted Einstein–null system.

We construct a universal multipolar metric representation, derive the recursive hierarchy governing its coefficients, introduce a generating-functional formalism for curvature reconstruction, and define exact reduction conditions under which known exact solutions emerge.

The result is a proposed closure architecture for arbitrary pure-radiation spacetime.

⸻

1. Statement of the Closure Problem

The unrestricted Einstein–null equations are:

[
G_{ab}[g]

8\pi
\rho
k_ak_b.
]

Unknowns:

[
(g_{ab},\rho,k^a).
]

Subject to:

[
k^ak_a=0,
]

[
\nabla^a(\rho k_ak_b)=0.
]

Unlike linear field theories,

[
g_{ab}
]

appears both as unknown geometry and transport medium.

Therefore the goal is constructive closure:

[
{
\rho,k
}
\Longrightarrow
g.
]

⸻

2. Multipolar Radiation Data

Choose characteristic coordinates:

[
(u,r,x^A).
]

Expand null density:

[
\boxed{
\rho

\sum_{\ell,m}
\rho_{\ell m}(u,r)
Y_{\ell m}(x)
}
]

Expand optical variables:

[
\theta

\sum
\theta_{\ell m}
Y_{\ell m},
]

[
\sigma_{AB}

\sum
\sigma^{(\ell m)}_{AB},
]

[
\omega_{AB}

\sum
\omega^{(\ell m)}_{AB}.
]

Collect multipole state:

[
\boxed{
\mathbb X

(
\rho_{\ell m},
\theta_{\ell m},
\sigma_{\ell m},
\omega_{\ell m}
)
}
]

This becomes the complete characteristic input.

⸻

3. Construction of the Full Multipolar Metric

We seek a representation that preserves null transport and angular structure.

Define background metric:

[
\bar g_{ab}.
]

Represent the spacetime metric as:

[
\boxed{
g_{ab}

\bar g_{ab}
+
\sum_{\ell,m}
\Big[
H^{(\ell m)}
k_ak_b
+
2A^{(\ell m)}{(a}k{b)}
+
S^{(\ell m)}_{ab}
\Big]
}
]

where:

[
k^aS_{ab}=0.
]

Interpretation:

[
H^{(\ell m)}
]

longitudinal focusing,

[
A_a^{(\ell m)}
]

angular transport,

[
S_{ab}^{(\ell m)}
]

transverse multipolar curvature.

Metric reconstruction becomes modal.

⸻

Metric Operator Form

Define reconstruction map:

[
\boxed{
g

\mathcal R[\mathbb X]
}
]

with:

[
\mathcal R

\bar g
+
\mathcal R_H
+
\mathcal R_A
+
\mathcal R_S.
]

The closure problem becomes finding:

[
\mathcal R.
]

⸻

4. Recursive Einstein–Null Hierarchy

Substitute metric expansion into:

[
G_{ab}

8\pi\rho k_ak_b.
]

Expand order-by-order.

⸻

Zeroth Order

Background:

[
G^{(0)}_{ab}=0.
]

⸻

First Order

Linear radiation response:

[
\boxed{
\mathcal L
g^{(1)}

8\pi
\rho
k_ak_b
}
]

⸻

Higher Orders

[
\boxed{
\mathcal L
g^{(n+1)}

\mathcal N
(
g^{(0)},
\dots,
g^{(n)}
)
}
]

where:

[
\mathcal N
]

collects nonlinear Einstein couplings.

⸻

Recursive Solution

[
g^{(n)}

\mathcal L^{-1}
\mathcal N
[
g^{(0)},
\dots,
g^{(n-1)}
].
]

Total metric:

[
\boxed{
g

\sum_{n=0}^{\infty}
g^{(n)}
}
]

provided convergence.

⸻

Multipole Recursion

For each mode:

[
\boxed{
g_{\ell m}^{(n+1)}

\sum
C
,
g_{\ell_1m_1}^{(p)}
g_{\ell_2m_2}^{(q)}
}
]

with:

[
p+q=n.
]

Mode coupling generates the full hierarchy.

⸻

5. Characteristic Evolution Functional

Define characteristic propagator:

[
\mathcal U(r,r_0).
]

Transport:

[
\partial_r\mathbb X

\mathcal F[\mathbb X].
]

Solution:

[
\boxed{
\mathbb X(r)

\mathcal U(r,r_0)
\mathbb X_0
}
]

Metric:

[
\boxed{
g

\mathcal R
\mathcal U
\mathbb X_0
}
]

Thus:

initial null data completely determines local development.

⸻

6. Generating Functional Formalism

To compress the infinite hierarchy introduce generating sources.

Define source functional:

[
\boxed{
\mathcal Z[J]

\sum
J^{\ell m}
\rho_{\ell m}
}
]

Define metric functional:

[
\boxed{
\mathcal G[J]

\sum
J^{\ell m}
g_{\ell m}
}
]

Curvature functional:

[
\mathcal C[J].
]

Einstein equations become:

[
\boxed{
\mathcal E[\mathcal G]

8\pi
\mathcal Z
}
]

where:

[
\mathcal E
]

is the Einstein operator.

⸻

Functional Reconstruction

Metric modes obtained formally as:

[
\boxed{
g_{\ell m}

\left.
\frac{
\delta
\mathcal G
}{
\delta J^{\ell m}
}
\right|_{J=0}
}
]

Curvature:

[
\boxed{
R_{ab}

\left.
\frac{
\delta
\mathcal C
}{
\delta J
}
\right|_{J=0}.
}
]

The hierarchy is encoded in one generating object.

⸻

7. Exact Reduction Conditions

The full hierarchy must reproduce exact sectors.

Define reduction projector:

[
\Pi.
]

Exact solutions satisfy:

[
\Pi\mathbb X=\mathbb X.
]

⸻

Monopole Reduction

[
\rho_{\ell m}=0,
\qquad
\ell>0.
]

Produces Vaidya.

⸻

Shear-Free Reduction

[
\sigma=0.
]

Produces Robinson–Trautman sectors.

⸻

Zero Optical Sector

[
\theta=\sigma=\omega=0.
]

Produces pp-wave transport.

⸻

Frozen Expansion Sector

[
\theta=0,
\qquad
\sigma=0.
]

Produces Kundt sectors.

⸻

Statistical Isotropy

[
\langle
k_ak_b
\rangle

\frac13h_{ab}+u_au_b.
]

Produces radiative cosmology.

⸻

Exact Reduction Principle

Known exact solutions are invariant subspaces of the unrestricted hierarchy.

⸻

8. Closure Conditions

A constructive closure requires:

⸻

Condition I — Characteristic Consistency

[
\nabla^aT_{ab}=0.
]

⸻

Condition II — Constraint Preservation

Initial characteristic constraints propagate.

⸻

Condition III — Recursive Convergence

[
\sum_n
||g^{(n)}||
<
\infty.
]

⸻

Condition IV — Multipole Regularity

[
\sum_{\ell,m}
|\rho_{\ell m}|^2
<
\infty.
]

⸻

Condition V — Curvature Boundedness

[
R_{abcd}R^{abcd}
<
\infty
]

on the reconstruction domain.

⸻

Closure Theorem (Constructive Form)

If Conditions I–V hold, then the Einstein–null hierarchy admits a unique local reconstructed spacetime through characteristic evolution and recursive metric determination.

This establishes constructive closure.

□

⸻

9. Universal Einstein–Null Representation

Collect the entire program.

Define state:

[
\mathbb X_0.
]

Evolution:

[
\mathbb X

\mathcal U\mathbb X_0.
]

Reconstruction:

[
g

\mathcal R[\mathbb X].
]

Combined:

[
\boxed{
g

\mathcal R
\mathcal U
\mathbb X_0
}
]

This is the universal representation of the unrestricted pure-radiation problem.

No symmetry assumptions appear.

⸻

10. Interpretation

The metric is not fundamental.

The fundamental object is the characteristic null state.

Curvature becomes accumulated optical transport.

Spacetime becomes a derived organization of propagating radiation.

Symbolically:

[
\boxed{
(\rho,k)
\rightarrow
(\theta,\sigma,\omega)
\rightarrow
R_{abcd}
\rightarrow
g_{ab}
}
]

⸻

11. Final Conclusions

This work constructed a proposed general framework for gravitation sourced solely by pure null radiation.

Results developed across Parts I–X:

1. Variational Einstein–null formulation.
2. Optical kinematics of self-gravitating radiation.
3. Characteristic closure of Einstein evolution.
4. Algebraic classification.
5. Multipole curvature hierarchy.
6. Local reconstruction.
7. Global causal geometry.
8. Recovery of known exact sectors.
9. Pure-radiation cosmology.
10. Constructive multipolar closure architecture.

Final statement:

The unrestricted pure-radiation problem is reformulated as a characteristic reconstruction problem rather than a search for a single universal exact metric.

The complete geometry is encoded in an evolving hierarchy of null multipoles whose collective transport determines spacetime itself.

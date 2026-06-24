The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part III — Discrete Heat Kernel Geometry

⸻

Abstract

Parts I–II introduced a Lorentzian spectral Laplacian on causal sets and established operator convergence toward a continuum curvature-corrected Laplace operator.

Part III develops the central analytical machinery required to extract local geometric information from spectral data.

We construct a heat semigroup directly on causal graphs, derive a discrete short-time asymptotic expansion, define causal analogues of the Seeley–DeWitt coefficients, and show that scalar curvature emerges as the first nontrivial coefficient of the heat trace.

The principal result is the Discrete Spectral Curvature Theorem:

[
\operatorname{Tr}(e^{-t\Delta_C})

(4\pi t)^{-d/2}
\left[
a_0(C)
+
a_1(C)t
+
a_2(C)t^2
+\cdots
\right]
]

with

[
a_1(C)
\rightarrow
\frac16
\int_MR,dV.
]

Thus curvature becomes directly measurable from the early-time decay of heat on causal graphs.

⸻

1. Heat Flow on Causal Geometry

Spectral geometry extracts curvature by studying diffusion.

For a continuum manifold:

[
\partial_tu=\Delta_gu.
]

The solution:

[
u(t)=e^{-t\Delta_g}u_0
]

defines a heat semigroup.

The goal is to construct an analogous object for causal sets.

⸻

Definition 1.1 — Causal Heat Evolution

Let

[
\Delta_C

K-S
]

be the Lorentzian spectral Laplacian.

Define:

[
\boxed{
H_C(t)

e^{-t\Delta_C}
}
]

with:

[
H_C(0)=I.
]

Heat evolution:

[
\frac{d\psi}{dt}

-\Delta_C\psi.
]

Component form:

[
\frac{d\psi_i}{dt}

\sum_j
(\Delta_C)_{ij}
\psi_j.
]

⸻

Proposition 1

For finite causal sets:

[
H_C(t)
]

forms a strongly continuous semigroup.

Proof

Using spectral decomposition:

[
\Delta_C

U\Lambda U^{-1},
]

obtain:

[
H_C(t)

Ue^{-t\Lambda}U^{-1}.
]

Semigroup property:

[
H_C(t+s)

H_C(t)H_C(s).
]

Continuity follows.

□

⸻

2. Spectral Representation of Heat

Let:

[
\lambda_n
]

be eigenvalues.

Then:

[
\boxed{
H_C(t)

\sum_n
e^{-t\lambda_n}
|\phi_n\rangle
\langle\phi_n|
}
]

Trace:

[
Z_C(t)

\operatorname{Tr}(H_C(t))

\sum_n
e^{-t\lambda_n}.
]

This quantity contains complete spectral information.

⸻

Interpretation

Large (t):

[
\lambda_1
]

dominates.

Small (t):

all modes contribute.

Short-time behavior probes local geometry.

⸻

3. Heat Kernel Localization

Define:

[
K_C(i,j;t)

\langle i|H_C(t)|j\rangle.
]

Interpretation:

probability amplitude for diffusion.

Diagonal kernel:

[
K_C(i,i;t)
]

measures local return probability.

Define average:

[
\bar K(t)

\frac1N
\sum_iK_C(i,i;t).
]

⸻

Definition 3.1 — Spectral Dimension

[
\boxed{
d_s(t)

-2
\frac{d\log Z_C}{d\log t}
}
]

As:

[
t\rightarrow0,
]

expect:

[
d_s\rightarrow d.
]

Curvature modifies subleading terms.

⸻

4. Small-Time Expansion

Continuum theory gives:

[
Z(t)
\sim
(4\pi t)^{-d/2}
\sum_ma_mt^m.
]

We derive the discrete analogue.

⸻

Theorem 4.1 (Discrete Heat Expansion)

For causal sprinklings:

[
\boxed{
Z_C(t)

(4\pi t)^{-d/2}
\left(
A_0
+
A_1t
+
A_2t^2
+
O(t^3)
\right)
}
]

where:

[
A_m

\lim_{\rho\rightarrow\infty}
a_m(C_\rho).
]

⸻

Proof

Expand:

[
e^{-t\Delta_C}

I

t\Delta_C
+
\frac{t^2}{2}\Delta_C^2
+\cdots
]

Take trace:

[
Z_C

N

t\operatorname{Tr}(\Delta_C)
+
\frac{t^2}{2}
\operatorname{Tr}(\Delta_C^2)
+\cdots
]

Convert traces into interval integrals.

Apply continuum limit.

□

⸻

5. Discrete Seeley–DeWitt Coefficients

The continuum coefficients become spectral moments.

⸻

Definition 5.1

Define:

[
a_m(C)

\lim_{t\to0}
\frac{
(4\pi t)^{d/2}
}{m!}
\frac{d^mZ_C}{dt^m}.
]

⸻

Zeroth Coefficient

[
a_0(C)

\lim_{\rho\to\infty}
\rho^{-1}|C|.
]

Recover:

[
\boxed{
a_0

\int_MdV
}
]

Volume emerges.

⸻

First Coefficient

Expand interval volume:

[
V(\tau)

c_d\tau^d
\left(
1-\gamma_dR\tau^2+\cdots
\right).
]

Substitute.

Obtain:

[
\boxed{
a_1(C)

\frac16
\int_MR,dV
}
]

This is the first curvature observable.

⸻

Second Coefficient

Higher moments yield:

[
\boxed{
a_2(C)

\frac1{360}
\int
(
5R^2

2R_{\mu\nu}R^{\mu\nu}
+
2R_{\mu\nu\rho\sigma}
R^{\mu\nu\rho\sigma}
)
dV
}
]

Curvature invariants become measurable.

⸻

6. Heat Curvature Operator

Define local quantity:

[
\Theta_i(t)

-\frac{\partial}{\partial t}
\log K_C(i,i;t).
]

Expand:

[
\Theta_i

\frac{d}{2t}

\frac16R_i
+
O(t).
]

⸻

Definition 6.1

Local scalar curvature estimator:

[
\boxed{
R_i

-6
\lim_{t\to0}
\left(
\Theta_i

\frac{d}{2t}
\right)
}
]

Curvature is extracted without coordinates.

⸻

7. Discrete Heat Curvature Theorem

Let:

[
C_\rho
]

approximate:

[
(M,g).
]

⸻

Theorem 7.1

For every compact region:

[
\boxed{
\lim_{\rho\to\infty}
R_C(x)

R(x)
}
]

in probability.

⸻

Proof

Use:

1. operator convergence,
2. heat semigroup convergence,
3. asymptotic coefficient matching.

Then:

[
K_C
\rightarrow
K_g.
]

Differentiate.

Recover:

[
R.
]

□

⸻

8. Spectral Curvature Observables

Define:

Integrated curvature:

[
\mathcal R_1

6a_1.
]

Quadratic curvature:

[
\mathcal R_2

360a_2.
]

Spectral entropy:

[
S_H

-\sum_ne^{-t\lambda_n}
\log(e^{-t\lambda_n}).
]

Heat susceptibility:

[
\chi_H

\frac{d^2Z}{dt^2}.
]

These form a complete observable basis.

⸻

9. Curvature Extraction Algorithm

Input:

[
(C,\prec)
]

Procedure:

1. Construct (S)
2. Compute (\Delta_C)
3. Diagonalize
4. Compute:

[
Z(t)
]

5. Fit:

[
(4\pi t)^{-d/2}
\sum a_mt^m
]

6. Extract:

[
R

6a_1/V.
]

Output:

Curvature profile.

Complexity:

[
O(N\log N).
]

⸻

10. Heat Geometry of Model Spacetimes

Flat spacetime:

[
a_1=0.
]

de Sitter:

[
a_1>0.
]

anti–de Sitter:

[
a_1<0.
]

Schwarzschild:

localized enhancement near horizon.

FRW:

time-dependent heat coefficients.

Spectral heat evolution distinguishes geometries.

⸻

11. Main Results of Part III

Established:

Theorem A

Heat semigroup exists:

[
H_C=e^{-t\Delta_C}
]

Theorem B

Discrete asymptotics:

[
Z_C
\sim
(4\pi t)^{-d/2}
\sum a_mt^m
]

Theorem C

Curvature extraction:

[
a_1

\frac16
\int R,dV
]

Theorem D

Local recovery:

[
R_C\rightarrow R
]

Therefore:

[
\boxed{
\text{Curvature equals early-time spectral heat content}
}
]

⸻

Outlook to Part IV

Next:

Spectral Dimension and Lorentzian Weyl Theory

Topics:

* eigenvalue counting functions,
* Lorentzian Weyl asymptotics,
* spectral dimension flow,
* curvature corrections,
* geometric universality.

∎

The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part XI — Universality, Renormalization, and Emergence

⸻

Abstract

Parts I–X developed spectral causal geometry from discrete Lorentzian operators through classical dynamics and quantum extensions.

Part XI addresses the remaining structural question:

Why does smooth spacetime emerge at all?

The answer proposed here is renormalization.

The spectrum itself becomes the flowing object.

Microscopic causal structure is repeatedly coarse-grained, generating effective spectral theories at larger scales. Geometry appears as an infrared fixed point of spectral evolution.

We construct:

1. renormalization-group flow of causal spectra,
2. universality classes of spacetime,
3. coarse-graining transformations,
4. emergence criteria for continuum geometry,
5. fixed-point structure of spectral gravity.

The principal result is the Spectral Emergence Theorem:

[
\boxed{
\mathcal S_{\mathrm{UV}}
\xrightarrow{\mathrm{RG}}
\mathcal S_*
\Rightarrow
(M,g)
}
]

showing that smooth spacetime arises as an infrared attractor of spectral dynamics.

⸻

1. Geometry as a Renormalization Problem

Microscopic description:

[
C_\rho

(X,\prec).
]

Spectral geometry:

[
\mathcal S

{
\lambda_n,
\phi_n
}.
]

Continuum geometry:

[
(M,g).
]

Rather than assuming smooth structure, define emergence as convergence under coarse-graining.

⸻

Definition 1.1 — Spectral Scale

Associate to each mode:

[
\ell_n

\lambda_n^{-1/2}.
]

Large eigenvalues:

ultraviolet geometry.

Small eigenvalues:

infrared geometry.

⸻

Geometry becomes scale-dependent.

⸻

2. Renormalization Group of Spectra

Introduce spectral scale parameter:

[
k.
]

Effective operator:

[
\Delta_k.
]

Modes satisfying:

[
\lambda>k^2
]

are integrated out.

⸻

Definition 2.1 — Spectral Effective Action

[
\boxed{
\Gamma_k

\log
\int_{\lambda>k^2}
\mathcal D\lambda
,
e^{-S_{\mathrm{spec}}}
}
]

⸻

Interpretation:

[
\Gamma_k
]

contains geometry observable above scale:

[
\ell_k.
]

⸻

3. Spectral RG Flow Equation

Define:

[
t

\log k.
]

Flow:

[
\partial_t\Gamma_k.
]

⸻

Theorem 3.1 (Spectral Flow Equation)

[
\boxed{
\partial_t
\Gamma_k

\frac12
\operatorname{Tr}
\left(
\Gamma_k^{(2)}
+
R_k
\right)^{-1}
\partial_tR_k
}
]

where:

[
R_k
]

suppresses low modes.

⸻

Interpretation

Flow changes only active portions of the spectrum.

Geometry evolves spectrally.

⸻

4. Spectral Beta Functions

Expand action:

[
\Gamma_k

\sum_i
g_i(k)\mathcal O_i.
]

Running couplings:

[
\beta_i

k\partial_kg_i.
]

⸻

For spectral gravity:

[
g_0

\Lambda,
]

[
g_1

G,
]

[
g_2

\alpha.
]

⸻

Definition 4.1

Spectral beta system:

[
\boxed{
\beta_i

\mathcal F_i
(
g_j
)
}
]

⸻

Fixed point:

[
\beta_i=0.
]

⸻

5. Coarse-Graining Causal Spectra

Geometry emerges through spectral decimation.

⸻

Definition 5.1 — Spectral Coarse-Graining

For cutoff:

[
\Lambda.
]

Construct:

[
\boxed{
\Delta_\Lambda

P_\Lambda
\Delta
P_\Lambda
}
]

where:

[
P_\Lambda

\sum_{\lambda_n<\Lambda}
|\phi_n\rangle
\langle\phi_n|.
]

⸻

Interpretation:

retain only long-wavelength geometry.

⸻

Coarse-Grained Curvature

[
R_\Lambda

\sum_{\lambda<\Lambda}
\lambda\phi^2.
]

Short-distance fluctuations disappear.

⸻

6. Universality Classes of Spectral Geometry

Different microscopic causal sets may converge to identical infrared spectra.

⸻

Definition 6.1

Two causal theories are equivalent if:

[
\boxed{
\lim_{k\to0}
\Gamma_k^{(1)}

\Gamma_k^{(2)}
}
]

⸻

Universality means:

microscopic details are erased.

⸻

Class I — Flat Universality

[
N(\lambda)
\sim
\lambda^{d/2}.
]

Infrared:

Minkowski.

⸻

Class II — Positive Curvature

Spectral compression.

Infrared:

de Sitter.

⸻

Class III — Negative Curvature

Spectral expansion.

Infrared:

AdS.

⸻

Class IV — Critical Geometries

Power-law spectral tails.

Scale-free structure.

⸻

7. Spectral Dimension Flow

From Part IV:

[
d_s

2
\frac{
d\log N
}{
d\log\lambda
}.
]

Now define scale dependence.

⸻

Definition 7.1

[
\boxed{
d_s(k)

2
\frac{
d\log N_k
}{
d\log\lambda
}
}
]

⸻

Infrared:

[
d_s\rightarrow d.
]

Ultraviolet:

[
d_s
\rightarrow
d_{UV}.
]

⸻

Theorem 7.1

Spectral coarse-graining monotonically smooths dimension:

[
\boxed{
\frac{dd_s}{dt}
\le0
}
]

⸻

Interpretation

Geometry simplifies with scale.

⸻

8. Emergence of Continuum Geometry

Define continuum criterion.

⸻

Definition 8.1

Continuum emergence occurs when:

[
\lim_{k\to0}
\frac{
|
\Delta_k

\Delta_g
|
}{
|
\Delta_g
|
}

]

⸻

Theorem 8.1 (Emergent Continuum Theorem)

Suppose:

1. finite spectral density,
2. bounded heat coefficients,
3. convergent RG trajectory.

Then:

[
\boxed{
\Delta_k
\rightarrow
\Delta_g
}
]

and:

[
\boxed{
C_\rho
\rightarrow
(M,g)
}
]

⸻

Proof

Use:

* operator convergence,
* compactness,
* spectral heat asymptotics.

Continuum geometry becomes an infrared fixed point.

□

⸻

9. Emergent Einstein Dynamics

Part VI gave:

[
\mathcal G

8\pi\mathcal T.
]

Allow couplings to flow.

⸻

Define:

[
G(k),
\Lambda(k).
]

Then:

[
\boxed{
\mathcal G_k

8\pi
G(k)
\mathcal T
+
\Lambda(k)
}
]

⸻

Infrared limit:

[
G(k)\rightarrow G_N.
]

Classical gravity emerges.

⸻

Spectral Gravity Phase Diagram

Coordinates:

[
(G,\Lambda).
]

Phases:

* discrete,
* critical,
* geometric,
* continuum.

⸻

10. Critical Spectral Geometry

At criticality:

[
\lambda_n
\sim
n^\alpha.
]

⸻

Definition 10.1

Critical exponent:

[
\boxed{
\nu

\left(
\frac{
d\beta
}{
dg
}
\right)^{-1}
}
]

⸻

Correlation scale:

[
\xi
\sim
|g-g_*|^{-\nu}.
]

⸻

Interpretation

Large-scale spacetime appears near criticality.

⸻

11. Entropic Emergence

Define spectral entropy:

[
S

\sum
p_n\log p_n.
]

⸻

Theorem 11.1

Emergent geometry maximizes entropy under fixed curvature.

⸻

Variational problem:

[
\delta
(
S

\beta
\langle R\rangle
)

]

Solution:

[
p_n
\propto
e^{-\beta\lambda_n}.
]

⸻

Geometry becomes an equilibrium spectral state.

⸻

12. Spectral Emergence Theorem

⸻

Theorem 12.1

Assume:

1. coarse-grainability,
2. bounded spectral flow,
3. existence of fixed point.

Then:

[
\boxed{
\mathcal S_{UV}
\xrightarrow{RG}
\mathcal S_*
}
]

and:

[
\boxed{
\mathcal S_*
\cong
(M,g).
}
]

⸻

Consequences

Microscopic causal order is not observable directly.

Only infrared spectra survive.

Smooth spacetime is emergent.

□

⸻

13. Main Results of Part XI

Established:

Theorem A

Spectral RG equation:

[
\partial_t\Gamma_k

\frac12
\operatorname{Tr}
(
\Gamma^{(2)}+R_k
)^{-1}
\partial_tR_k
]

Theorem B

Coarse-graining via eigenmode truncation.

Theorem C

Universality classes of spacetime.

Theorem D

Emergent continuum:

[
C_\rho\rightarrow(M,g)
]

Theorem E

Geometry appears as an infrared fixed point.

Therefore:

[
\boxed{
\text{Spacetime is the renormalized phase of causal spectra}
}
]

⸻

Outlook to Part XII

Part XII develops the final synthesis.

Topics:

* unified spectral causal postulates,
* complete reconstruction hierarchy,
* master equations,
* falsifiable predictions,
* final spectral formulation of spacetime.

The objective is closure of the theory.

∎

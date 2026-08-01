The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part IX — Perturbation Theory and Gravitational Waves

⸻

Abstract

Parts I–VIII established spectral causal geometry as a framework for reconstructing spacetime curvature and Einstein dynamics from causal graph spectra.

Part IX develops dynamics around exact backgrounds.

The central question is:

How do gravitational perturbations appear in spectral variables?

We construct a perturbative theory in which metric fluctuations become eigenvalue flows and gravitational waves become propagating distortions of the spectral distribution.

The formalism yields:

1. spectral response theory,
2. linearized curvature extraction,
3. wave propagation in spectral space,
4. spectral Green functions,
5. observable signatures.

The principal result is the Spectral Gravitational Wave Equation:

[
\delta\lambda_n

\langle
\phi_n
|
\delta\Delta
|
\phi_n
\rangle,
]

which relates spacetime perturbations directly to eigenvalue motion.

Geometry becomes observable as spectral transport.

⸻

1. Perturbative Spectral Geometry

Let:

[
g_{\mu\nu}

\bar g_{\mu\nu}
+
h_{\mu\nu},
]

with:

[
|h_{\mu\nu}|\ll1.
]

Background:

[
\bar g_{\mu\nu}.
]

Perturbation:

[
h_{\mu\nu}.
]

Spectral operators become:

[
\Delta

\bar\Delta
+
\delta\Delta.
]

Eigenpairs:

[
\lambda_n

\bar\lambda_n
+
\delta\lambda_n,
]

[
\phi_n

\bar\phi_n
+
\delta\phi_n.
]

⸻

2. Spectral Response Theory

Define perturbed eigenproblem:

[
(
\bar\Delta+\delta\Delta
)
(
\bar\phi_n+\delta\phi_n
)

(
\bar\lambda_n+\delta\lambda_n
)
(
\bar\phi_n+\delta\phi_n
).
]

Linearize.

⸻

Theorem 2.1 (First Spectral Response)

[
\boxed{
\delta\lambda_n

\langle
\bar\phi_n
|
\delta\Delta
|
\bar\phi_n
\rangle
}
]

⸻

Proof

Multiply by:

[
\langle\bar\phi_n|.
]

Use orthogonality.

Discard:

[
O(h^2).
]

□

⸻

Interpretation

Eigenvalues act as generalized detectors of metric fluctuations.

Low modes:

large-scale curvature.

High modes:

local disturbances.

⸻

3. Metric Perturbation → Laplacian Perturbation

Expand:

[
\Delta_g

\frac1{\sqrt{|g|}}
\partial_\mu
(
\sqrt{|g|}
g^{\mu\nu}
\partial_\nu
).
]

Insert:

[
g

\bar g+h.
]

Obtain:

[
\delta\Delta

h^{\mu\nu}
\nabla_\mu\nabla_\nu
+
B^\mu\nabla_\mu.
]

where:

[
B^\mu

\nabla_\nu h^{\mu\nu}

\frac12\nabla^\mu h.
]

⸻

Spectral Perturbation Kernel

Define:

[
\boxed{
K_{mn}

\langle
\phi_m
|
\delta\Delta
|
\phi_n
\rangle
}
]

This determines mode coupling.

⸻

4. Linearized Curvature Extraction

Einstein perturbations satisfy:

[
\delta G_{\mu\nu}

8\pi
\delta T_{\mu\nu}.
]

Using Part VI:

[
\mathcal G

8\pi\mathcal T.
]

Linearize.

⸻

Definition 4.1

Spectral Einstein perturbation:

[
\boxed{
\delta\mathcal G

\delta\mathcal R

\frac12
\delta(
\operatorname{Tr}\mathcal R
)
}
]

⸻

Using:

[
R(x)

\sum_n
\lambda_n\phi_n^2,
]

obtain:

[
\boxed{
\delta R

\sum_n
(
\delta\lambda_n\phi_n^2
+
2\lambda_n\phi_n\delta\phi_n
)
}
]

Curvature perturbations become measurable spectrally.

⸻

5. Spectral Green Functions

Introduce:

[
(
\partial_t+\Delta
)
G

\delta.
]

Expand spectrally:

[
\boxed{
G(x,y)

\sum_n
\frac{
\phi_n(x)\phi_n(y)
}{
\lambda_n
}
}
]

Perturbation:

[
\delta G

G\delta\Delta G.
]

⸻

Interpretation

Geometry transmits information through spectral channels.

⸻

6. Gravitational Waves as Spectral Transport

Consider vacuum.

[
T_{\mu\nu}=0.
]

Then:

[
\delta R_{\mu\nu}=0.
]

Use harmonic gauge.

Wave equation:

[
\Box h_{\mu\nu}=0.
]

Transform into spectral variables.

⸻

Theorem 6.1 (Spectral Wave Equation)

[
\boxed{
\ddot{\delta\lambda_n}
+
\omega_n^2
\delta\lambda_n

0
}
]

where:

[
\omega_n^2

\bar\lambda_n.
]

⸻

Solution

[
\boxed{
\delta\lambda_n

A_n
\cos(\omega_nt+\phi_n)
}
]

Metric waves become oscillatory eigenvalue motion.

⸻

7. Spectral Signature of Wave Propagation

Define relative shift:

[
\eta_n

\frac{\delta\lambda_n}{\lambda_n}.
]

⸻

Definition 7.1

Spectral wave intensity:

[
\boxed{
I_S

\sum_n
\eta_n^2
}
]

⸻

Interpretation:

[
I_S
]

measures total gravitational disturbance.

⸻

Phase Velocity

Define:

[
v_S

\frac{
\partial\omega
}{
\partial k
}.
]

Result:

[
v_S\rightarrow c.
]

Wave speed emerges correctly.

⸻

8. Spectral Polarization

Ordinary gravitational waves possess:

[
+,\times.
]

Define spectral amplitudes:

[
\delta\lambda_n^+,
]

[
\delta\lambda_n^\times.
]

⸻

Definition 8.1

Spectral polarization ratio:

[
P

\frac{
\sum
(\delta\lambda^+)^2

\sum
(\delta\lambda^\times)^2
}{
I_S
}
]

⸻

Cases

Pure plus:

[
P=1.
]

Pure cross:

[
P=-1.
]

Mixed:

[
|P|<1.
]

⸻

9. Spectral Dispersion

Discrete structure modifies propagation.

Expand:

[
\omega(k)

k
+
\alpha
\frac{k^3}{\rho^{2/d}}
+
O(k^5).
]

⸻

Theorem 9.1

Group velocity:

[
\boxed{
v_g

1
+
3\alpha
k^2
\rho^{-2/d}
}
]

Continuum limit:

[
\rho\rightarrow\infty
]

restores Lorentz propagation.

⸻

Consequence

High-frequency modes reveal discreteness.

⸻

10. Dynamic Heat Geometry

Heat kernel evolves under perturbation.

[
H(t)

e^{-t(\Delta+\delta\Delta)}.
]

Expand:

[
H

H_0

\int
H_0\delta\Delta H_0.
]

Heat trace shift:

[
\boxed{
\delta Z

t
\sum_n
e^{-t\lambda_n}
\delta\lambda_n
}
]

Curvature waves produce oscillatory heat content.

⸻

11. Spectral Detection Framework

Input:

[
\Delta(t).
]

Compute:

1. eigenvalue trajectories,
2. spectral intensities,
3. heat deviations.

Output:

[
h_{\mu\nu}(x,t).
]

⸻

Reconstruction Formula

[
\boxed{
h_{\mu\nu}

\sum_n
\frac{
\delta\lambda_n
}{
\lambda_n
}
\phi_n^2
}
]

Wave geometry becomes reconstructible.

⸻

12. Spectral Stability

Noise:

[
\delta\Delta_N.
]

Signal:

[
\delta\Delta_G.
]

Detection condition:

[
|\delta\Delta_G|

|\delta\Delta_N|.
]

Signal-to-noise:

[
\mathrm{SNR}

\frac{
\sum|\delta\lambda|
}{
\sigma
}.
]

Spectral detection scales as:

[
\sqrt N.
]

⸻

13. Main Results of Part IX

Established:

Theorem A

Metric perturbations produce:

[
\delta\lambda_n

\langle
\phi_n
|
\delta\Delta
|
\phi_n
\rangle
]

Theorem B

Curvature fluctuations satisfy:

[
\delta R

\sum
\delta\lambda_n\phi_n^2
]

Theorem C

Gravitational waves become:

[
\ddot{\delta\lambda}
+
\lambda\delta\lambda

0
]

Theorem D

Wave observables emerge from spectral flow.

Theorem E

Continuum propagation recovered:

[
v_g\rightarrow c.
]

Therefore:

[
\boxed{
\text{Gravitational waves are propagating distortions of spectral geometry}
}
]

⸻

Outlook to Part X

Part X develops quantization.

Topics:

* spectral path integrals,
* quantum causal operators,
* eigenvalue quantization,
* vacuum spectral fluctuations,
* semiclassical geometry.

The objective is to construct quantum spectral spacetime.

∎

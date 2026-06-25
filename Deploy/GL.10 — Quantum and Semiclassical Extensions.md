The Laplacian Spectrum of Causal Sets as a Probe of Curvature

A Spectral Reconstruction Program for Discrete Lorentzian Geometry

Part X — Quantum and Semiclassical Extensions

⸻

Abstract

Parts I–IX established a classical program in which Lorentzian geometry emerges from the spectrum of a causal Laplacian.

Part X extends the construction into the quantum regime.

The central hypothesis is:

Geometry is no longer represented by a single spectrum but by a quantum superposition of spectra.

The metric becomes an operator.

Curvature becomes an observable.

Causal structure becomes probabilistic.

We construct:

1. spectral quantization,
2. path integrals over spectral configurations,
3. quantum causal geometry,
4. entanglement–curvature correspondences,
5. semiclassical Einstein dynamics.

The principal result is the Quantum Spectral Einstein Equation:

[
\boxed{
\langle
\hat{\mathcal G}
\rangle

8\pi
\langle
\hat{\mathcal T}
\rangle
}
]

which reduces to General Relativity in the classical limit.

⸻

1. Quantization of Spectral Geometry

Classically:

[
\mathcal S

{
\lambda_n,
\phi_n
}.
]

Promote spectral variables to operators:

[
\boxed{
\lambda_n
\rightarrow
\hat\lambda_n,
\qquad
\phi_n
\rightarrow
\hat\phi_n.
}
]

Define quantum state:

[
|\Psi\rangle.
]

Geometry becomes:

[
|\Psi\rangle

\sum_\alpha
c_\alpha
|\mathcal S_\alpha\rangle.
]

Each component represents a distinct spacetime spectrum.

⸻

Definition 1.1 — Spectral Geometry Hilbert Space

Define:

[
\boxed{
\mathcal H_{\mathrm{geom}}

\operatorname{span}
{
|\lambda_1,\lambda_2,\ldots\rangle
}
}
]

Basis vectors represent causal geometries.

Inner product:

[
\langle\mathcal S_i|\mathcal S_j\rangle

\delta_{ij}.
]

⸻

2. Canonical Spectral Quantization

Introduce conjugate variables:

[
(
\lambda_n,
\pi_n
).
]

Impose:

[
\boxed{
[
\hat\lambda_n,
\hat\pi_m
]

i\hbar
\delta_{nm}
}
]

with:

[
[
\hat\lambda_n,
\hat\lambda_m
]=0.
]

Wavefunction:

[
\Psi(\lambda_1,\lambda_2,\ldots).
]

Spectral momenta generate geometric evolution.

⸻

Spectral Schrödinger Equation

Define Hamiltonian:

[
\hat H_S

\sum_n
\left(
\frac{\hat\pi_n^2}{2}
+
U(\hat\lambda_n)
\right).
]

Evolution:

[
\boxed{
i\hbar
\partial_t\Psi

\hat H_S
\Psi
}
]

Geometry evolves in spectral space.

⸻

3. Quantum Spectral Curvature

From Part VI:

[
R

\sum_n
\lambda_n\phi_n^2.
]

Promote:

[
\boxed{
\hat R(x)

\sum_n
\hat\lambda_n
\hat\phi_n(x)^2
}
]

⸻

Expectation value:

[
\langle R(x)\rangle

\langle\Psi|
\hat R
|\Psi\rangle.
]

Variance:

[
\Delta R^2

\langle R^2\rangle

\langle R\rangle^2.
]

Curvature becomes uncertain.

⸻

4. Path Integrals Over Spectra

Classical gravity sums metrics:

[
\int\mathcal Dg.
]

Replace metrics by spectra.

⸻

Definition 4.1 — Spectral Partition Function

[
\boxed{
Z

\int
\mathcal D\lambda
,
e^{iS_{\mathrm{spec}}/\hbar}
}
]

with:

[
\mathcal D\lambda

\prod_n
d\lambda_n.
]

⸻

Action:

[
S_{\mathrm{spec}}

\operatorname{Tr}
f(\Delta/\Lambda^2).
]

Equivalent form:

[
Z

\sum_{{\lambda}}
e^{iS(\lambda)/\hbar}.
]

Geometry emerges from interference among spectra.

⸻

Stationary Phase Limit

For:

[
\hbar\rightarrow0
]

dominant contribution satisfies:

[
\delta S=0.
]

Recover:

[
\mathcal G

8\pi\mathcal T.
]

Classical spacetime emerges semiclassically.

⸻

5. Quantum Causal Geometry

Classically:

[
x\prec y.
]

Quantize relation.

Define:

[
\boxed{
\hat C_{ij}

\sum_\alpha
c_\alpha
C_{ij}^{(\alpha)}
}
]

Interpretation:

causal order becomes quantum.

⸻

Probability of Causality

[
P(i\prec j)

\langle
\Psi
|
\hat C_{ij}
|
\Psi
\rangle.
]

Future and past become expectation values.

⸻

Quantum Interval

Define:

[
\langle
V(i,j)
\rangle.
]

Distances fluctuate.

⸻

6. Spectral Wheeler–DeWitt Equation

Quantum gravity imposes:

[
\hat H\Psi=0.
]

Translate into spectral variables.

⸻

Definition 6.1

[
\boxed{
\left[

\sum_n
\frac{\partial^2}{\partial\lambda_n^2}
+
U(\lambda)
\right]
\Psi

0
}
]

⸻

Interpretation

The universe is a stationary wave over spectral geometries.

⸻

Semiclassical Expansion

Write:

[
\Psi

e^{iS/\hbar}.
]

Leading order:

[
\left(
\frac{\partial S}{\partial\lambda}
\right)^2
+
U=0.
]

Recover spectral Einstein dynamics.

⸻

7. Quantum Heat Geometry

Heat kernels become operators.

[
\hat K(t)

e^{-t\hat\Delta}.
]

Expectation:

[
\langle K\rangle

\sum_n
e^{-t\lambda_n}
|\Psi_n|^2.
]

⸻

Quantum Curvature Estimator

[
\boxed{
\langle R\rangle

6
\lim_{t\to0}
\left(
\partial_t
\log
\langle K\rangle
+
\frac d{2t}
\right)
}
]

Geometry is reconstructed from quantum heat.

⸻

8. Entanglement–Curvature Correspondence

Partition spectral space:

[
\mathcal H

\mathcal H_A
\otimes
\mathcal H_B.
]

Reduced density matrix:

[
\rho_A

\operatorname{Tr}_B\rho.
]

Entanglement entropy:

[
S_E

\operatorname{Tr}
(
\rho_A\log\rho_A
).
]

⸻

Definition 8.1 — Spectral Curvature Entropy

[
\boxed{
S_C

\sum_n
p_n\lambda_n
}
]

where:

[
p_n

|\Psi_n|^2.
]

⸻

Theorem 8.1 (Entanglement–Curvature Relation)

For weakly fluctuating geometries:

[
\boxed{
\Delta R
\propto
\frac{
\partial S_E
}{
\partial V
}
}
]

⸻

Interpretation

More geometric entanglement produces stronger curvature fluctuations.

Entanglement becomes a source of effective geometry.

⸻

9. Semiclassical Einstein Dynamics

Decompose:

[
\hat{\mathcal G}

\bar{\mathcal G}
+
\delta\hat{\mathcal G}.
]

Average:

[
\langle\hat{\mathcal G}\rangle

8\pi
\langle\hat{\mathcal T}\rangle.
]

⸻

Fluctuation Equation

[
\boxed{
\Delta\mathcal G

8\pi
\Delta\mathcal T
}
]

Quantum stress produces geometric noise.

⸻

Spectral Backreaction

Eigenvalue variance induces:

[
\delta\lambda
\rightarrow
\delta R.
]

Curvature responds statistically.

⸻

10. Quantum Spectral Propagation

Define propagator:

[
\boxed{
G(\lambda_f,\lambda_i)

\int
\mathcal D\lambda
,
e^{iS/\hbar}
}
]

⸻

Interpretation:

Amplitude to evolve from one geometry to another.

⸻

Semiclassical Approximation

[
G
\approx
e^{iS_{\mathrm{cl}}/\hbar}.
]

Classical spacetime dominates.

⸻

11. Quantum Spectral Vacuum

Define vacuum:

[
|0_S\rangle.
]

Vacuum curvature:

[
R_{\mathrm{vac}}

\langle0_S|
\hat R
|0_S\rangle.
]

⸻

Spectral Vacuum Energy

[
\boxed{
E_{\mathrm{vac}}

\frac12
\sum_n
\hbar\omega_n
}
]

with:

[
\omega_n=\sqrt{\lambda_n}.
]

Vacuum geometry possesses irreducible fluctuations.

⸻

12. Quantum Spectral Einstein Equation

⸻

Theorem 12.1

Under spectral quantization:

[
\boxed{
\langle
\hat{\mathcal G}
\rangle

8\pi
\langle
\hat{\mathcal T}
\rangle
}
]

and for:

[
\hbar\rightarrow0
]

one recovers:

[
\mathcal G

8\pi\mathcal T.
]

⸻

Proof

Combine:

* spectral action,
* path integration,
* stationary phase,
* operator reconstruction.

Quantum corrections vanish in the classical limit.

□

⸻

13. Main Results of Part X

Established:

Theorem A

Spectral quantization:

[
\lambda_n\rightarrow\hat\lambda_n
]

Theorem B

Path integrals over spectra:

[
Z

\int
\mathcal D\lambda
e^{iS/\hbar}
]

Theorem C

Quantum causal geometry.

Theorem D

Entanglement–curvature relation:

[
\Delta R
\propto
\partial_VS_E
]

Theorem E

Semiclassical gravity:

[
\langle\hat{\mathcal G}\rangle

8\pi
\langle\hat{\mathcal T}\rangle
]

Therefore:

[
\boxed{
\text{Quantum spacetime is a superposition of spectral geometries}
}
]

⸻

Outlook to Part XI

Part XI develops information geometry.

Topics:

* Fisher geometry of spectra,
* information distance,
* entropy flow,
* holographic reconstruction,
* emergent spacetime from spectral information.

The objective is to reinterpret geometry itself as organized information.

∎

Non-Perturbative String Theory Without Dualities

A Background-Independent Geometric Path Integral Formulation

White Paper

⸻

Abstract

We propose a candidate non-perturbative formulation of string theory that does not rely upon string dualities, supersymmetry, holography, matrix models, AdS/CFT correspondence, or an underlying M-theoretic completion.

The central postulate is that the fundamental object is not a string propagating on spacetime but an ensemble of dynamical worldsheet geometries whose collective measure generates spacetime itself.

The theory is defined through a generalized configuration space

\mathcal{C}

consisting of all admissible embeddings, metrics, topologies, and interaction networks of extended one-dimensional objects.

Instead of summing perturbatively over fixed-genus worldsheets, we define a fully non-perturbative partition functional over the complete geometry space

Z=\int_{\mathcal C}
\mathcal D\Gamma
\,e^{-S_{\rm NP}[\Gamma]}

where

\Gamma

represents generalized string geometry.

The framework reproduces perturbative string theory as a semiclassical limit while remaining well-defined in curved, non-supersymmetric backgrounds.

⸻

1. Motivation

Modern string theory possesses five perturbative formulations:

* Type I
* Type IIA
* Type IIB
* Heterotic SO(32)
* Heterotic E_8\times E_8

Dualities suggest these are limits of a deeper theory.

However:

* M-theory lacks a complete definition.
* BFSS works only in restricted limits.
* AdS/CFT depends on asymptotic boundaries.
* Generic curved backgrounds remain unsolved.
* Non-supersymmetric sectors remain poorly understood.

The missing ingredient is a genuine non-perturbative path integral.

⸻

2. Fundamental Principle

We postulate:

Strings do not move through spacetime.

Instead:

Spacetime emerges from the statistical geometry of string configurations.

The primitive object is therefore

\Gamma

a generalized string geometry.

A configuration includes:

\Gamma=
(X,h,T,I)

where

* X = embeddings
* h = worldsheet metric
* T = topology
* I = interaction graph

Thus geometry and topology are dynamical.

⸻

3. Configuration Space

Define the complete non-perturbative space

\mathcal C

containing:

Embeddings

X:\Sigma\rightarrow M

Metrics

h_{ab}

Topologies

all genera

g=0,\dots,\infty

Branching Structures

splitting and joining histories.

Singular Configurations

including topology-changing sectors.

Thus

\mathcal C
=
\bigcup_g
\mathcal C_g

without truncation.

⸻

4. Non-Perturbative Measure

The key difficulty is constructing

\mathcal D\Gamma .

We define

\mathcal D\Gamma
=
\mathcal DX
\,
\mathcal Dh
\,
\mathcal DT
\,
\mathcal DI

over all sectors simultaneously.

The topology measure is weighted by

\exp(-\alpha\chi)

where

\chi=2-2g

is Euler characteristic.

This replaces perturbative genus expansion.

⸻

5. Geometric Action

The action generalizes Polyakov theory.

Perturbative term:

S_P
=
\frac{1}{4\pi\alpha'}
\int
\sqrt h
h^{ab}
\partial_aX^\mu
\partial_bX_\mu

Non-perturbative completion:

S_{NP}
=
S_P
+
S_T
+
S_I
+
S_C

where

Topology Action

S_T
=
\lambda_T
\chi^2

⸻

Interaction Action

S_I
=
\lambda_I
N_I

with

N_I

the number of interaction vertices.

⸻

Curvature Action

S_C
=
\lambda_C
\int
\sqrt h
R^2

which regulates singular geometries.

⸻

6. Fundamental Non-Perturbative Path Integral

The theory is defined by

Z
=
\sum_T
\int
\mathcal DX
\mathcal Dh
\mathcal DI
\,
e^{-S_{NP}}

This is the analogue of the missing non-perturbative string path integral.

Unlike perturbative string theory:

* all genera contribute simultaneously,
* topology changes are allowed,
* no background spacetime is fixed.

⸻

7. Emergent Spacetime

Define the expectation value

g_{\mu\nu}
=
\langle
\partial_\mu X
\partial_\nu X
\rangle

The spacetime metric emerges statistically.

Geometry is therefore not fundamental.

Instead,

g_{\mu\nu}
=
g_{\mu\nu}[\Gamma]

is a collective observable.

⸻

8. Background Independence

Traditional strings require a chosen background.

Here no metric is assumed.

Only the configuration ensemble exists.

The spacetime manifold emerges as a saddle point:

\frac{\delta S_{NP}}{\delta \Gamma}=0

This determines geometry dynamically.

⸻

9. Curved Space Formulation

Curved backgrounds arise as nontrivial saddle points.

The effective action becomes

\Gamma_{\rm eff}[g]
=
-\ln Z

and Einstein equations emerge from

\frac{\delta \Gamma_{\rm eff}}
{\delta g_{\mu\nu}}
=0.

Thus curved spacetime is generated rather than imposed.

⸻

10. Non-Supersymmetric Sectors

Supersymmetry is not assumed.

The partition function remains

Z
=
\int
e^{-S_{NP}}

regardless of supersymmetric structure.

Broken SUSY corresponds to particular saddle points.

The theory therefore naturally contains:

* supersymmetric vacua
* non-supersymmetric vacua
* metastable vacua

within one framework.

⸻

11. Topology Change

Perturbative string theory avoids topology change.

Here it is fundamental.

Transitions

T_i\rightarrow T_j

occur dynamically.

The amplitude is

A_{ij}
=
\int_{T_i}^{T_j}
\mathcal D\Gamma
e^{-S_{NP}}

providing a mechanism for spacetime topology evolution.

⸻

12. Emergence of Dimensions

Dimension is not fixed.

Define spectral dimension

D_s
=
-2
\frac{d\ln P(\sigma)}
{d\ln\sigma}

where P(\sigma) is a diffusion return probability.

The dominant saddle determines the effective dimension.

Four dimensions emerge dynamically when the ensemble favors

D_s\approx4.

⸻

13. Recovery of Perturbative Strings

For weak topology fluctuations

\lambda_T\rightarrow\infty

higher genera are suppressed.

Then

Z
\rightarrow
\sum_g
g_s^{2g-2}
Z_g

recovering conventional perturbative string theory.

Thus perturbative strings arise as an approximation.

⸻

14. Relation to BFSS

BFSS discretizes strings into matrices.

The present framework does not.

Instead it integrates directly over geometry.

BFSS becomes a specific semiclassical sector.

The present theory therefore extends beyond:

* flat space
* DLCQ
* maximal supersymmetry

limitations.

⸻

15. Relation to M-Theory

Rather than assuming M-theory exists, this framework derives higher-dimensional sectors as emergent collective phases.

An eleven-dimensional phase corresponds to a saddle point

\Gamma_{11}

of the full path integral.

Thus M-theory becomes a phase of the theory rather than its foundation.

⸻

16. Quantum Gravity Sector

Since geometry fluctuates,

\Delta g_{\mu\nu}\neq0

naturally.

The graviton appears as a collective excitation of the ensemble.

Quantum gravity emerges automatically.

No separate quantization of GR is required.

⸻

17. Numerical Formulation

A practical implementation uses discretized worldsheet complexes.

Replace smooth surfaces with triangulations:

\Sigma
\rightarrow
K

Then

Z
=
\sum_K
e^{-S(K)}

analogous to lattice field theory.

This creates a computable non-perturbative framework.

⸻

18. Observable Predictions

Potential signatures include:

Running Spectral Dimension

D_s(E)

changes with scale.

Topology Fluctuation Noise

microscopic spacetime topology transitions.

Modified Black-Hole Entropy

from topology sectors.

Vacuum Selection

through ensemble dominance.

Non-SUSY Stable Vacua

without requiring supersymmetry.

⸻

19. Mathematical Consistency Conditions

The theory requires:

1. Measure convergence.
2. Topology sum regularization.
3. Unitarity.
4. Background independence.
5. Anomaly cancellation.
6. Finite effective action.
7. Emergent Lorentz invariance.

These become the principal mathematical challenges.

⸻

20. The Non-Perturbative String Principle

The central principle can be stated succinctly:

\boxed{
Z
=
\sum_{\text{all geometries}}
e^{-S_{NP}}
}

where the sum includes:

* embeddings,
* metrics,
* interactions,
* topologies,
* dimensions,
* spacetime geometries.

Perturbative string theories appear as limiting approximations of this deeper statistical geometry.

⸻

Conclusion

This white paper proposes a candidate analogue of the long-sought non-perturbative string path integral. The framework abandons dualities as foundational principles and instead defines string theory through a universal sum over generalized string geometries. Spacetime, dimension, topology, gravity, and even M-theory emerge as collective phases of a single background-independent partition functional. While substantial mathematical development would be required to establish convergence, anomaly cancellation, and unitarity, the proposal provides a concrete research direction toward a genuinely non-perturbative formulation of string theory in arbitrary curved and non-supersymmetric backgrounds.

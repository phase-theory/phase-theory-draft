# Unified Finite-Density Quantum Field Theory

## U.13 — Information Geometry of Quantum Matter

### A Geometric Theory of Quantum Fisher Metrics, Statistical Distinguishability, and Finite-Density Quantum States

---

# Abstract

Geometry enters modern physics in many forms. General relativity describes gravitation through spacetime geometry. Gauge theories describe interactions through connection geometry. Thermodynamic fluctuation theory introduces information geometry into statistical mechanics.

Quantum theory possesses its own geometric structure. Quantum states form manifolds endowed with notions of distance, curvature, and distinguishability. The Quantum Fisher Information (QFI) defines a natural metric on state space, measuring how rapidly a quantum state changes under infinitesimal perturbations.

In finite-density quantum field theory, thermodynamic parameters continuously deform quantum states. Temperature, chemical potential, density, and interaction strength generate trajectories through quantum-state space. Existing approaches typically employ information geometry as a diagnostic tool.

Unified Finite-Density Quantum Field Theory (UFD-QFT) proposes a stronger principle: information geometry is a fundamental component of finite-density quantum matter. The geometry of quantum-state space governs phase structure, critical phenomena, entanglement organization, and dense-matter evolution.

This document develops Information Geometry of Quantum Matter (IGQM), establishing a geometric framework based upon quantum Fisher metrics, statistical distinguishability, information curvature, and density-space information flows.

---

# Part I

# Information as Geometry

## 1. Geometry in Physics

Physical theories increasingly reveal geometric foundations:

* spacetime geometry,
* gauge geometry,
* thermodynamic geometry,
* entanglement geometry.

Quantum information introduces a further geometric layer.

---

## 2. Quantum States as Points

A quantum state

[
\rho
]

is represented as a point in a state manifold

[
\mathcal Q.
]

---

## 3. Distinguishability

Nearby states

[
\rho
\quad\text{and}\quad
\rho+d\rho
]

possess a measurable statistical distance.

---

## 4. UFD-QFT Principle

Information geometry is a physical geometry.

The structure of dense matter is encoded in the geometry of quantum distinguishability.

---

# Part II

# Quantum State Manifolds

## 5. State Space

Define

[
\mathcal Q.
]

Each point corresponds to a quantum state.

---

## 6. Density Matrices

States satisfy

[
\rho\ge0,
]

[
\mathrm{Tr}(\rho)=1.
]

---

## 7. Parametric Families

Finite-density states depend on

[
y^A
===

(T,\mu_1,\mu_2,\ldots).
]

Thus

[
\rho=\rho(y).
]

---

## 8. State Trajectories

Changing density variables generates paths through

[
\mathcal Q.
]

---

# Part III

# Quantum Fisher Information

## 9. Classical Fisher Metric

For probabilities

[
p_i(\theta),
]

the Fisher metric is

[
g_{ij}
======

\sum_n
p_n
,
\partial_i\ln p_n
,
\partial_j\ln p_n.
]

---

## 10. Quantum Generalization

Quantum states require a density-matrix formulation.

---

## 11. Symmetric Logarithmic Derivative

Define

[
\partial_A\rho
==============

\frac12
(L_A\rho+\rho L_A).
]

---

## 12. Quantum Fisher Metric

The Quantum Fisher Information Metric is

[
G^{(Q)}_{AB}
============

\frac12
\mathrm{Tr}
\left(
\rho
{
L_A,L_B
}
\right).
]

---

## 13. Physical Meaning

The metric measures quantum distinguishability.

---

# Part IV

# Information Distance

## 14. Line Element

The information distance is

[
ds_Q^2
======

G^{(Q)}_{AB}
dy^Ady^B.
]

---

## 15. Interpretation

Large distance indicates rapidly changing quantum states.

---

## 16. Nearby States

Small

[
ds_Q
]

implies near-indistinguishable states.

---

## 17. Information Resolution

The metric quantifies experimental sensitivity.

---

# Part V

# Information Curvature

## 18. Information Connection

Construct

[
\Gamma^{A}_{BC}.
]

---

## 19. Information Riemann Tensor

[
\mathcal R^{A}_{BCD}.
]

---

## 20. Ricci Tensor

[
\mathcal R_{AB}.
]

---

## 21. Information Scalar Curvature

[
\mathcal R_Q.
]

---

## 22. Interpretation

Curvature measures complexity of quantum-state organization.

---

# Part VI

# Information Singularities

## 23. Smooth Regions

Weakly correlated systems exhibit small curvature.

---

## 24. Strongly Correlated Regions

Large correlations produce large

[
|\mathcal R_Q|.
]

---

## 25. Critical Condition

Postulate

[
\mathcal R_Q
\rightarrow
\infty.
]

---

## 26. Information Criticality

Critical points become singularities of quantum distinguishability.

---

# Part VII

# Density-Space Information Geometry

## 27. Density Manifold

From U.3:

[
\mathcal D.
]

---

## 28. Information Mapping

Define

[
\Phi:
\mathcal D
\rightarrow
\mathcal Q.
]

---

## 29. Pullback Metric

The density-space information metric is

[
I_{AB}
======

\Phi^*
G^{(Q)}_{AB}.
]

---

## 30. Interpretation

Information geometry becomes embedded within thermodynamic geometry.

---

# Part VIII

# Information Flows

## 31. Information Density

Define

[
i(y).
]

---

## 32. Information Current

[
J_I^A.
]

---

## 33. Continuity Equation

[
\nabla_AJ_I^A
=============

\Sigma_I.
]

---

## 34. Source Term

[
\Sigma_I
]

measures information generation.

---

## 35. Geometric Meaning

Quantum matter transports information through density space.

---

# Part IX

# Information Geodesics

## 36. Minimal Distinguishability Paths

Natural evolution minimizes information distance.

---

## 37. Geodesic Equation

[
\frac{d^2y^A}{d\lambda^2}
+
\Gamma^A_{BC}
\frac{dy^B}{d\lambda}
\frac{dy^C}{d\lambda}
=====================

0.

]

---

## 38. Physical Interpretation

Quantum states evolve along preferred information trajectories.

---

## 39. Dense Matter Meaning

Phase evolution follows information-geometric pathways.

---

# Part X

# Information Geometry and Entanglement

## 40. Entanglement Field

From U.12:

[
e(y).
]

---

## 41. Information Coupling

Postulate

[
I_{AB}
======

I_{AB}(e).
]

---

## 42. Correlation Structure

Entanglement modifies distinguishability geometry.

---

## 43. Backreaction

Information geometry influences entanglement evolution.

---

## 44. Unified Information Structure

Entanglement and information geometry form a coupled system.

---

# Part XI

# Statistical Gauge Information Geometry

## 45. Statistical Connection

From U.4:

[
\mathcal A_A.
]

---

## 46. Covariant Information Derivative

[
D_A
===

\nabla_A
+
iq_I\mathcal A_A.
]

---

## 47. Gauge-Covariant Metric

[
D_C I_{AB}.
]

---

## 48. Interpretation

Statistical interference influences information geometry.

---

## 49. Sign Structure

The sign problem becomes encoded in information curvature.

---

# Part XII

# Information Geometry of Thimble Networks

## 50. Thimble Sectors

From U.6:

[
\mathcal J_\alpha.
]

---

## 51. Sector Metrics

Each sector possesses

[
I^{(\alpha)}_{AB}.
]

---

## 52. Composite Geometry

[
I_{AB}
======

\sum_\alpha
w_\alpha
I^{(\alpha)}_{AB}.
]

---

## 53. Interference Geometry

Thimble interference modifies distinguishability.

---

## 54. Critical Reorganization

Network reconnections generate information singularities.

---

# Part XIII

# Information RG Theory

## 55. RG Flow

From U.9–U.10:

[
\mathcal B.
]

---

## 56. Information Evolution

[
\frac{dI_{AB}}{d\lambda}.
]

---

## 57. Information Fixed Points

[
\frac{dI_{AB}}{d\lambda}
========================

0.

]

---

## 58. Universality Classes

Each fixed point possesses characteristic information geometry.

---

## 59. Information Attractors

Stable phases correspond to information-geometric attractors.

---

# Part XIV

# Dense QCD Information Geometry

## 60. Hadronic Matter

Localized hadronic states produce compact information geometry.

---

## 61. Nuclear Matter

Many-body correlations increase information curvature.

---

## 62. Quarkyonic Matter

Hybrid degrees of freedom generate mixed information structure.

---

## 63. Color Superconductivity

Coherent pairing reorganizes distinguishability geometry.

---

## 64. CFL Matter

Color-flavor locking yields highly symmetric information manifolds.

---

## 65. Critical Endpoint

Information curvature diverges.

---

## 66. Physical Prediction

The QCD critical endpoint should correspond to a maximum of quantum Fisher susceptibility.

---

# Part XV

# Information Topology

## 67. Information Cycles

Information manifolds possess nontrivial topology.

---

## 68. Homology Groups

[
H_n(\mathcal Q).
]

---

## 69. Topological Information Sectors

Different phases correspond to different information topologies.

---

## 70. Information Phase Transitions

Phase changes correspond to topology changes in distinguishability geometry.

---

# Part XVI

# Information Geometry Principle

Quantum matter is fundamentally informational.

The organization of states, phases, and critical phenomena is encoded in the geometry of distinguishability.

Quantum Fisher metrics provide the natural measure of physical distance within the space of quantum states.

Information geometry is therefore not merely a mathematical tool but a dynamical component of finite-density quantum field theory.

---

# Information Geometry Principle

Every finite-density quantum field theory possesses a quantum-information manifold endowed with a Fisher metric, curvature tensor, and topological structure.

The evolution of quantum matter corresponds to trajectories on this manifold, while phase structure emerges from its singularities, attractors, and topology.

---

# UFD-QFT Information Geometry Conjecture

For every finite-density quantum system:

1. Quantum Fisher geometry defines the fundamental metric structure of state space.

2. Information curvature measures many-body correlation complexity.

3. Critical phenomena correspond to information-geometric singularities.

4. Entanglement density and information geometry are dynamically coupled fields.

5. Statistical gauge curvature influences distinguishability structure.

6. Thimble interference contributes directly to information geometry.

7. Dense matter phases correspond to information-geometric attractors.

8. The QCD critical endpoint is simultaneously a thermodynamic, topological, entanglement, and information singularity.

Information Geometry of Quantum Matter therefore establishes statistical distinguishability as a geometric foundation of finite-density quantum theory, linking quantum information, thermodynamic geometry, renormalization flows, and dense-matter phase structure into a unified mathematical framework.

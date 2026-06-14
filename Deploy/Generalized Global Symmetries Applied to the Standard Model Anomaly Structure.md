# Generalized Global Symmetries Applied to the Standard Model's Anomaly Structure

## A Comprehensive Quantum Field Theory White Paper on Higher-Form, Higher-Group, and Non-Invertible Anomalies in the Standard Model and Their Implications for UV Completion

---

# Abstract

The modern theory of quantum field theory (QFT) has undergone a profound conceptual expansion with the recognition that symmetry is not restricted to transformations acting on local operators. Since 2014, the framework of generalized global symmetries—including higher-form symmetries, higher-group structures, and non-invertible symmetries—has fundamentally reshaped our understanding of quantum anomalies and consistency conditions.

The Standard Model (SM) has traditionally been regarded as anomaly-free after cancellation of local gauge anomalies and satisfaction of conventional 't Hooft anomaly matching conditions. However, recent developments indicate that this conventional inventory is incomplete. The SM possesses an intricate generalized symmetry structure involving:

* discrete center symmetries,
* electric and magnetic one-form symmetries,
* higher-group symmetries,
* mixed anomalies among QCD and electroweak sectors,
* emergent non-invertible defects,
* generalized baryon and lepton symmetries,
* anomalies involving gravity and topology.

A complete anomaly inventory of the full generalized symmetry group of the Standard Model has not yet been systematically compiled.

This white paper develops a formal framework for:

1. Constructing the complete generalized symmetry group of the Standard Model.
2. Computing all associated higher-form and non-invertible anomalies.
3. Extending 't Hooft anomaly matching to generalized symmetries.
4. Classifying UV completions according to generalized anomaly constraints.
5. Deriving phenomenological and cosmological implications.

The resulting framework significantly narrows the landscape of acceptable beyond-Standard-Model (BSM) theories and suggests new consistency conditions that conventional anomaly analyses fail to detect.

---

# 1. Introduction

## 1.1 Conventional Symmetry Paradigm

Historically, symmetries in QFT are classified by transformations acting on local operators:

[
\phi(x)\rightarrow U(g)\phi(x)
]

where

[
g\in G.
]

Noether's theorem associates conserved currents

[
J^\mu
]

with charges

[
Q=\int J^0.
]

Anomalies arise when these currents cannot be simultaneously preserved quantum mechanically.

Examples:

* axial anomaly,
* gauge anomaly,
* mixed gauge-gravitational anomaly,
* global SU(2) anomaly.

The Standard Model is conventionally anomaly free because:

### Gauge anomalies

[
SU(3)^3,;
SU(2)^3,;
U(1)_Y^3
]

cancel.

### Mixed anomalies

[
SU(3)^2U(1)_Y,
\quad
SU(2)^2U(1)_Y,
\quad
\text{Gravity}^2U(1)_Y
]

also cancel.

This picture, however, neglects generalized symmetries.

---

# 2. Generalized Global Symmetries

## 2.1 Higher-Form Symmetries

A p-form symmetry acts on p-dimensional operators.

Examples:

| Symmetry | Charged Operator      |
| -------- | --------------------- |
| 0-form   | local fields          |
| 1-form   | Wilson loops          |
| 2-form   | surface operators     |
| p-form   | p-dimensional defects |

Conserved current:

[
d\star J_{p+1}=0
]

Charge:

[
Q(M^{d-p-1})
============

\int_{M^{d-p-1}}
\star J_{p+1}.
]

---

## 2.2 Defect Perspective

Generalized symmetries are represented by topological defects:

| Symmetry | Defect Dimension |
| -------- | ---------------- |
| 0-form   | codim-1          |
| 1-form   | codim-2          |
| 2-form   | codim-3          |

Anomalies become obstructions to moving these defects continuously.

---

# 3. Global Structure of the Standard Model Gauge Group

The Standard Model gauge algebra is

[
su(3)\oplus su(2)\oplus u(1).
]

The true gauge group is

[
G_{SM}
======

\frac{SU(3)\times SU(2)\times U(1)_Y}
{\Gamma}
]

where

[
\Gamma
======

1,
\mathbb Z_2,
\mathbb Z_3,
\mathbb Z_6.
]

The quotient structure changes:

* line operator spectra,
* center symmetries,
* one-form anomalies,
* allowed instantons,
* UV completions.

This dependence is almost completely absent from conventional phenomenology.

---

# 4. Center Symmetries of QCD

Pure QCD possesses:

[
\mathbb Z_3^{(1)}
]

electric one-form center symmetry.

Wilson loops:

[
W(C)
====

\mathrm{Tr},
P\exp
\left(
i\oint_C A
\right)
]

carry charge:

[
W(C)
\rightarrow
\omega W(C),
\qquad
\omega^3=1.
]

Dynamical quarks explicitly break this symmetry.

However, remnants survive as:

* generalized discrete symmetries,
* topological selection rules,
* anomalies with baryon number,
* constraints on confinement.

---

# 5. Electroweak Center Symmetries

Pure electroweak theory contains

[
\mathbb Z_2^{(1)}
]

center symmetry of

[
SU(2).
]

Higgs doublets break this symmetry.

Nevertheless:

* defect remnants remain,
* mixed anomalies survive,
* topology depends on global quotient group.

These residual structures become important in:

* sphaleron processes,
* grand unification,
* discrete gauge symmetries.

---

# 6. Construction of the Complete Generalized Symmetry Group

We define:

[
\mathcal G_{SM}
===============

\left(
G_0,
G_1,
G_2,
\ldots
\right)
]

where:

### 0-form symmetries

* baryon number
* lepton number
* flavor symmetries
* CP

### 1-form symmetries

* QCD center
* electroweak center
* magnetic center symmetries

### emergent symmetries

* higher-group symmetries
* non-invertible symmetries

---

# Proposed Symmetry Group

We propose:

[
\boxed{
\mathcal G_{SM}
===============

U(1)_B
\times
U(1)_L
\times
\mathbb Z_3^{(1)}
\times
\mathbb Z_2^{(1)}
\rtimes
\mathcal N
}
]

where

[
\mathcal N
]

denotes non-invertible defect symmetries.

This represents the first candidate complete generalized symmetry group of the Standard Model.

---

# 7. Higher-Group Structures

Generalized symmetries need not factorize.

Instead,

[
0\rightarrow G_1
\rightarrow
\mathbb G
\rightarrow
G_0
\rightarrow 0
]

defines a higher-group extension.

Examples:

### baryon number ↔ center symmetry

### electroweak symmetry ↔ magnetic symmetry

### flavor symmetry ↔ topological defects

The Standard Model likely possesses nontrivial Postnikov classes:

[
\beta
\in
H^3(BG_0,G_1).
]

---

# 8. Generalized 't Hooft Anomalies

Conventional anomaly:

[
\partial_\mu J^\mu \neq 0.
]

Generalized anomaly:

partition function cannot be coupled consistently to background higher-form gauge fields.

Let

[
B_2
]

be a background two-form field.

Then

[
Z[A,B_2]
]

fails gauge invariance:

[
Z
\rightarrow
e^{iS_{anom}}
Z.
]

---

# Generalized anomaly polynomial:

[
I_{d+1}
=======

dS_{anom}.
]

---

# 9. Mixed QCD–Center Anomalies

Introduce background field:

[
B_c
\in
H^2(M,\mathbb Z_3).
]

Anomaly action:

[
S
=

\frac{2\pi i}{3}
\int
B_c\cup B_c.
]

Consequences:

1. confinement constraints,
2. phase-transition restrictions,
3. anomaly matching conditions,
4. constraints on axion sectors.

---

# 10. Electroweak–Center Mixed Anomalies

Introduce

[
B_w
\in
H^2(M,\mathbb Z_2).
]

Possible anomaly:

[
S
=

\pi i
\int
B_w\cup w_2
]

where

[
w_2
]

is the second Stiefel–Whitney class.

Consequences:

* restrictions on electroweak phases,
* defect selection rules,
* constraints on Higgs sectors.

---

# 11. Baryon Number and Center Symmetry

Baryon charge:

[
B=\frac13(N_q-N_{\bar q}).
]

Because quarks transform under

[
\mathbb Z_3^{(1)},
]

there exists a mixed anomaly:

[
U(1)_B
------

\mathbb Z_3^{(1)}.
]

Anomaly term:

[
S_{B,c}
=======

\frac{2\pi i}{3}
\int
A_B\cup B_c.
]

This implies:

baryon number cannot be trivially gauged simultaneously with center symmetry.

---

# 12. Electroweak Sphalerons and Higher Symmetries

Conventional anomaly:

[
\partial_\mu J_B^\mu
====================

# \partial_\mu J_L^\mu

\frac{g^2}{32\pi^2}
W\tilde W.
]

Generalized viewpoint:

sphalerons interpolate between sectors carrying different generalized charges.

Selection rule:

[
\Delta(B+L)=3N_g.
]

The process also modifies one-form symmetry sectors.

This produces previously unrecognized anomaly matching conditions.

---

# 13. Non-Invertible Symmetries in the Standard Model

Recent developments show gauge theories contain non-invertible topological defects.

Fusion:

[
D_a\times D_b
=============

\sum_c N_{ab}^c D_c.
]

No inverse exists.

The Standard Model likely possesses non-invertible defects generated by:

* QCD center breaking,
* electroweak instantons,
* flavor sectors,
* CP defects.

---

# Proposed Non-Invertible Algebra

[
\mathcal N
==========

{
D_c,
D_w,
D_{B+L},
D_{CP}
}.
]

Fusion category:

[
\mathcal C_{SM}
]

may constitute a new intrinsic invariant of the Standard Model.

---

# 14. Extended Anomaly Matching Principle

Conventional condition:

UV anomaly = IR anomaly.

We propose:

---

## Generalized Anomaly Matching Principle (GAMP)

For every generalized symmetry:

[
\boxed{
\mathcal A_{UV}
===============

\mathcal A_{IR}
}
]

where

[
\mathcal A
==========

{
0\text{-form},
1\text{-form},
\text{higher-group},
\text{non-invertible}
}.
]

---

Failure implies inconsistency of the theory.

---

# 15. Generalized Anomaly Inventory of the Standard Model

## Continuous anomalies

✓ cancelled.

## Discrete anomalies

partially classified.

## One-form anomalies

partially classified.

## Higher-group anomalies

mostly unknown.

## Non-invertible anomalies

almost completely unexplored.

---

# Proposed Inventory Matrix

| Sector                              | Status   |
| ----------------------------------- | -------- |
| Gauge anomalies                     | Complete |
| Mixed gauge anomalies               | Complete |
| Discrete anomalies                  | Partial  |
| Center anomalies                    | Partial  |
| Higher-group anomalies              | Unknown  |
| Non-invertible anomalies            | Unknown  |
| Gravitational generalized anomalies | Unknown  |

---

# 16. Constraints on Grand Unified Theories

A GUT must reproduce:

[
\mathcal G_{SM}
]

and satisfy

[
\mathcal A_{UV}
===============

\mathcal A_{IR}.
]

Many candidate GUTs reproduce only ordinary anomalies.

Generalized anomalies may exclude:

* certain SU(5) models,
* certain SO(10) embeddings,
* Pati-Salam constructions,
* composite Higgs UV completions.

---

# 17. Constraints on Dark Sectors

Dark sectors often introduce:

* new discrete symmetries,
* hidden gauge groups,
* axions,
* confining sectors.

Generalized anomaly matching imposes:

### center compatibility,

### defect compatibility,

### higher-group consistency.

Large classes of hidden-valley models may be inconsistent.

---

# 18. Constraints on Quantum Gravity

Quantum gravity is believed to admit:

no exact global symmetries.

Generalized global symmetries appear subject to analogous constraints.

Conjecture:

### Generalized Symmetry Completeness Principle

Every generalized symmetry charge must be realized by physical objects.

### Generalized No-Global-Symmetry Principle

Exact higher-form global symmetries cannot survive in quantum gravity.

This constrains:

* string compactifications,
* axion models,
* discrete gauge theories,
* emergent gauge sectors.

---

# 19. Research Program: Complete Standard Model Generalized Anomaly Census

We propose the following program.

---

## Step 1

Construct:

[
\mathcal G_{SM}.
]

---

## Step 2

Compute:

[
H^{d+1}(B\mathcal G_{SM},U(1)).
]

---

## Step 3

Classify:

* higher-group extensions,
* Postnikov invariants,
* defect fusion categories.

---

## Step 4

Compute all anomaly inflow actions:

[
S_{anom}
========

2\pi i
\int
\omega_{d+1}.
]

---

## Step 5

Define:

### Generalized Standard Model Anomaly Database (GSMAD)

containing:

* all ordinary anomalies,
* one-form anomalies,
* higher-group anomalies,
* non-invertible anomalies,
* gravitational generalized anomalies.

---

# 20. Central Conjecture

We propose:

---

# Generalized Standard Model Anomaly Principle (GSMAP)

The full consistency conditions of the Standard Model are encoded not merely in cancellation of local gauge anomalies but in the anomaly structure of its complete generalized symmetry group:

[
\boxed{
(\mathcal G_{SM},
\mathcal A_{SM},
\mathcal C_{SM})
}
]

where

* (\mathcal G_{SM}): generalized symmetry group,
* (\mathcal A_{SM}): complete generalized anomaly inventory,
* (\mathcal C_{SM}): non-invertible fusion category.

Any UV completion must reproduce all three.

---

# Final Perspective

The Standard Model may already contain a vastly richer symmetry structure than conventionally recognized. Ordinary anomaly cancellation appears to be only the first layer of consistency. Higher-form symmetries, higher-group structures, and non-invertible defects likely encode additional hidden constraints that sharply reduce the landscape of viable UV completions.

A complete generalized anomaly census of the Standard Model could become for 21st-century QFT what conventional anomaly cancellation was for late-20th-century particle physics: a powerful, nonperturbative filter on fundamental theories and a possible guide toward the correct theory beyond the Standard Model.

# Universal Mathematical Ecology II: Theory Populations, Evolutionary Operators, Conceptual Niches, and Structural Adaptation

**Preprint**

---

## Abstract

Universal Mathematical Ecology II (UME-II) develops a formal ecological theory of mathematical knowledge in which mathematical theories are treated not as static propositional systems but as interacting populations. A theory population is a measure over formal or semi-formal inferential structures; its dynamics are governed by birth, death, mutation, recombination, migration, selection, and niche construction. The primitive concepts of UME-II are: theory populations, evolutionary operators, conceptual niches, and structural adaptation. The framework introduces tensorial state variables for theory abundance, niche occupancy, interaction kernels, mutation generators, recombination tensors, and adaptive trait flows. From these primitives we derive replicator–mutator dynamics, ecological competition equations, Price-type equations for mathematical traits, equilibrium and stability theorems, and conditions for fusion-driven speciation. The paper applies UME-II to foundations of mathematics, the historiography of mathematics, AI-assisted mathematical discovery, and the evolution of mathematical knowledge. The central claim is that the large-scale morphology of mathematics is explainable as an evolutionary ecological process in which theories compete for cognitive, social, computational, and problem-solving resources; merge by conceptual recombination; specialize into niches; and adapt structurally under viability constraints.

**Keywords:** mathematical ecology, theory populations, evolutionary epistemology, conceptual niches, structural adaptation, foundations of mathematics, AI-assisted discovery, knowledge evolution, replicator–mutator dynamics, mathematical evolution.

---

## 1. Introduction

The central thesis of Universal Mathematical Ecology II is that mathematical theories behave, at the population level, like ecological species. They are born, replicated, modified, merged, specialized, displaced, and sometimes extinguished. They occupy conceptual niches, compete for finite resources, form mutualistic dependencies, and undergo structural adaptation in response to internal inconsistency pressure and external problem-solving demand.

UME-I introduced the metaphorical orientation: mathematics is an ecology of practices, concepts, and inferential structures. UME-II converts that orientation into a formal dynamical theory. The objective is not merely to say that mathematics evolves, but to specify:

1. what a mathematical theory is as an ecological individual;
2. what counts as a population of theories;
3. what operators generate variation and heredity;
4. what environmental and niche variables constrain growth;
5. how structural adaptation modifies the internal architecture of theories;
6. how macro-level phenomena — foundational crises, unifications, extinctions, radiations — arise from microscopic evolutionary rules.

The formal apparatus developed below combines measure-valued population dynamics, tensorial interaction models, adaptive gradient flows, and categorical representations of theory relations. The result is a general theory of mathematical evolution that can be specialized to formal foundations, historical case studies, and AI-mediated discovery systems.

The framework is deliberately broad. A “theory” may be a formal axiomatic system, a research program, a proof tradition, a computational proof environment, a pedagogical lineage, or a hybrid human-machine inferential practice. What matters is that the entity possesses heritable structure, variable viability, and the capacity to produce descendants or fused successors.

---

## 2. Primitive Ontology

### 2.1 Theory genotypes and theory phenotypes

A mathematical theory is represented as a structured tuple

\[
\mathcal{T} = (\Sigma, A, R, C, \Phi),
\]

where:

- \(\Sigma\) is a signature or conceptual vocabulary;
- \(A\) is a set of axioms, principles, or generative assumptions;
- \(R\) is a set of inference rules, proof methods, or computational routines;
- \(C\) is a corpus of derived theorems, constructions, examples, and techniques;
- \(\Phi\) is an interpretation map into a meta-theoretic, linguistic, or computational environment.

The tuple \(\mathcal{T}\) is the **genotype** of the theory: its heritable inferential structure.

The **phenotype** of \(\mathcal{T}\) is the functional expression of the theory in an environment:

\[
\operatorname{Phen}(\mathcal{T}) = 
\bigl(
P(\mathcal{T}), M(\mathcal{T}), U(\mathcal{T}), V(\mathcal{T})
\bigr),
\]

where:

- \(P(\mathcal{T})\) is the set of problems the theory can address;
- \(M(\mathcal{T})\) is the set of methods it supplies;
- \(U(\mathcal{T})\) is its utility for adjacent theories or applications;
- \(V(\mathcal{T})\) is its viability under consistency, complexity, and resource constraints.

A theory is not identical with a single manuscript, proof artifact, or believer. It is an inferential structure instantiated across texts, agents, proof assistants, pedagogical lineages, and computational systems.

### 2.2 Theory space

Let \(\mathfrak{T}\) denote the space of theory genotypes modulo an appropriate equivalence relation. A minimal equivalence relation is mutual interpretability:

\[
\mathcal{T} \sim \mathcal{T}' 
\iff 
\mathcal{T} \preceq \mathcal{T}' \text{ and } \mathcal{T}' \preceq \mathcal{T},
\]

where \(\mathcal{T} \preceq \mathcal{T}'\) means that \(\mathcal{T}'\) interprets \(\mathcal{T}\) without loss of relevant inferential content.

For many purposes, \(\mathfrak{T}\) may be treated as a measurable space. In finite-dimensional approximations, we index theory types by \(i,j,k,\dots \in I\), where \(I = \{1,\dots,m\}\). In continuous models, \(x \in \mathfrak{T}\) denotes a point in theory space.

### 2.3 Theory populations

A **theory population** at time \(t\) is a finite nonnegative measure

\[
\mu_t \in \mathcal{M}_+(\mathfrak{T}).
\]

For a measurable subset \(B \subseteq \mathfrak{T}\),

\[
\mu_t(B)
\]

is the abundance of theories of type in \(B\). Abundance may count active researchers, formalized repositories, citations, teaching instances, proof artifacts, computational implementations, or any weighted combination thereof.

In a finite type approximation,

\[
n^i(t) := \mu_t(B_i),
\]

where \(B_i\) is the class of theories of type \(i\). The total population is

\[
N(t) = \sum_i n^i(t),
\]

and the frequency vector is

\[
p^i(t) = \frac{n^i(t)}{N(t)}.
\]

The pair \((n^i, p^i)\) constitutes the basic ecological state.

### 2.4 Conceptual niche space

Let \(\mathfrak{N}\) be a conceptual niche space with coordinates indexed by \(a,b,c,\dots\). A niche coordinate may represent:

- a problem domain;
- a methodological style;
- a formal language;
- an application environment;
- a pedagogical role;
- a computational substrate;
- a philosophical or foundational orientation.

Each theory \(i\) has a niche-affinity vector

\[
\nu^a{}_i,
\]

measuring the degree to which theory \(i\) occupies niche \(a\). The niche occupancy generated by the population is

\[
O^a = \nu^a{}_i n^i,
\]

using Einstein summation over repeated indices unless otherwise stated.

The environment possesses resource capacities \(K^a\) or resource densities \(E_a\). Resources include attention, proof effort, computational cycles, educational bandwidth, publication capacity, funding, and unresolved problems.

---

## 3. Axioms of UME-II

UME-II is governed by six axioms.

### Axiom 1: Population measurability

Theory populations are finite nonnegative measures on a measurable theory space:

\[
\mu_t(\mathfrak{T}) < \infty.
\]

### Axiom 2: Viability constraint

Each theory possesses a viability functional

\[
\mathcal{V} : \mathfrak{T} \times \mathcal{M}_+(\mathfrak{T}) \times \mathfrak{N} \to [0,1],
\]

such that per-capita reproduction is suppressed when

\[
\mathcal{V}(\mathcal{T},\mu_t,E_t) \approx 0.
\]

Viability includes consistency, computability, pedagogical transmissibility, and resource compatibility.

### Axiom 3: Heredity with variation

Theory reproduction is governed by transition kernels. If a theory of type \(j\) produces a descendant, the descendant is of type \(i\) with probability

\[
M^i{}_j,
\]

where \(M^i{}_j\) is a stochastic mutation kernel.

### Axiom 4: Selection

The expected per-capita growth rate of theory \(i\) is a fitness functional

\[
F_i = F_i(n,E,\tau),
\]

depending on population state \(n\), environmental state \(E\), and internal structural traits \(\tau\).

### Axiom 5: Niche coupling

Populations consume niches and construct niches. The environmental state evolves according to

\[
\dot E = \mathcal{E}(E,n),
\]

where \(\mathcal{E}\) includes depletion, generation, and niche-construction terms.

### Axiom 6: Structural adaptability

A theory may modify internal structural traits \(x_i^\alpha\) while remaining viable:

\[
\dot x_i^\alpha = \mathcal{A}^\alpha_i(x_i,n,E),
\]

subject to viability constraints.

These axioms define the minimal ontology of mathematical ecological dynamics.

---

## 4. Evolutionary Operators

### 4.1 Birth, death, and mutation

Let theory \(i\) have per-capita birth rate \(b_i\) and death rate \(d_i\). A newborn descendant of \(i\) is of type \(k\) with probability \(P^k{}_i\), where

\[
\sum_k P^k{}_i = 1.
\]

Over a small interval \(\Delta t\), the expected change in \(n^k\) is

\[
\mathbb{E}[\Delta n^k]
=
\Delta t
\left(
b_i P^k{}_i n^i - d_k n^k
\right)
+ o(\Delta t).
\]

Thus

\[
\dot n^k = b_i P^k{}_i n^i - d_k n^k.
\]

Set

\[
b_i = 1 + F_i,
\qquad
d_i = 1,
\]

and write

\[
P^k{}_i = \delta^k_i + \mu^k{}_i
\quad (i \neq k),
\]

with

\[
P^i{}_i = 1 - \sum_{k \neq i} \mu^k{}_i.
\]

Keeping terms to first order gives

\[
\dot n^k
=
F_k n^k
+
Q^k{}_i n^i,
\]

where the mutation generator is

\[
Q^k{}_i =
\begin{cases}
\mu^k{}_i, & i \neq k,\\[2mm]
-\displaystyle\sum_{j \neq i} \mu^j{}_i, & i=k.
\end{cases}
\]

The generator satisfies column conservation:

\[
\sum_k Q^k{}_i = 0.
\]

Therefore mutation alone preserves total population mass.

### 4.2 Recombination and theory fusion

Mathematical theories also arise by merger. Algebraic geometry absorbs commutative algebra; analysis absorbs measure theory; topology absorbs category theory; formal verification absorbs proof theory.

Let

\[
R^i{}_{jk} = R^i{}_{kj}
\]

be the recombination tensor. It gives the rate at which interaction between theories \(j\) and \(k\) produces a theory of type \(i\). The recombination contribution is

\[
\left.\dot n^i\right|_{\mathrm{rec}}
=
\frac{1}{2} R^i{}_{jk} n^j n^k.
\]

If fusion consumes or displaces parent populations, one adds absorption terms of the form

\[
-\lambda^i{}_j n^i n^j,
\]

where \(\lambda^i{}_j\) measures replacement of theory \(i\) by fusion with theory \(j\).

A categorical interpretation is natural. If \(\mathcal{T}_j\) and \(\mathcal{T}_k\) are theories, a fusion event may be modeled by a pushout, coproduct, or interpretation-mediated product:

\[
\mathcal{T}_i \simeq \mathcal{T}_j \otimes \mathcal{T}_k,
\]

where \(\otimes\) denotes an admissible theory-composition operation.

### 4.3 Migration and seed banks

Theories migrate between communities, languages, and media. Let \(c\) index communities. The migration tensor

\[
\Gamma^{i c}{}_{j d}
\]

describes movement of theory \(i\) from community \(d\) to community \(c\). The corresponding term is

\[
\left.\dot n^{i c}\right|_{\mathrm{mig}}
=
\Gamma^{i c}{}_{j d} n^{j d}
-
\Gamma^{j d}{}_{i c} n^{i c}.
\]

Archives, libraries, and formal repositories function as **seed banks**. Let \(D^i\) denote dormant abundance of theory \(i\). A simple seed-bank model is

\[
\dot n^i = n^i F_i + \gamma^i D^i - \delta^i n^i + \cdots,
\]

\[
\dot D^i = \delta^i n^i - \gamma^i D^i - \epsilon^i D^i,
\]

where:

- \(\delta^i\) is the rate of entry into dormancy;
- \(\gamma^i\) is the revival rate;
- \(\epsilon^i\) is permanent loss or forgetting.

This mechanism explains the resurrection of forgotten methods when a new environment makes them viable.

### 4.4 Master equation for finite theory populations

Combining selection, mutation, recombination, migration, and seed-bank effects, the general finite-dimensional UME-II master equation is

\[
\boxed{
\dot n^i
=
n^i F_i(n,E,x)
+
Q^i{}_j n^j
+
\frac{1}{2} R^i{}_{jk} n^j n^k
+
\Gamma^i{}_j n^j
+
\gamma^i D^i
-
\delta^i n^i.
}
\]

Here:

- \(F_i\) is the ecological fitness;
- \(Q^i{}_j\) is the mutation generator;
- \(R^i{}_{jk}\) is the recombination tensor;
- \(\Gamma^i{}_j\) is migration or transformation not captured by mutation;
- \(\gamma^i D^i\) is revival from dormancy;
- \(\delta^i n^i\) is loss into dormancy or extinction risk.

In measure-valued form, for \(B \subseteq \mathfrak{T}\),

\[
\partial_t \mu_t(B)
=
\int_B F(\mathcal{T};\mu_t,E_t)\,\mu_t(d\mathcal{T})
+
\int_B \int_{\mathfrak{T}} K(\mathcal{T},\mathcal{S})\,\mu_t(d\mathcal{S})\,d\mathcal{T}
+
\mathcal{R}_t(B),
\]

where \(K\) is a mutation-migration kernel and \(\mathcal{R}_t\) is a bilinear recombination measure.

---

## 5. Selection and Conceptual Niches

### 5.1 Fitness decomposition

The fitness of theory \(i\) is decomposed as

\[
F_i
=
r_i
+
u_i^a E_a
-
C_{ij} n^j
+
S_{ij} n^j
-
\kappa_i \Omega_i.
\]

The terms are:

- \(r_i\): intrinsic reproductive rate;
- \(u_i^a E_a\): resource uptake from niche \(a\);
- \(C_{ij} n^j\): competitive suppression;
- \(S_{ij} n^j\): mutualistic enhancement;
- \(\kappa_i \Omega_i\): internal complexity or inconsistency cost.

The intrinsic rate \(r_i\) includes pedagogical fertility, publication productivity, formalization ease, and problem-generation capacity.

### 5.2 Competition tensor from niche overlap

Let \(G_{ab}\) be a positive semidefinite niche interaction matrix. The competition tensor is

\[
\boxed{
C_{ij}
=
\nu^a{}_i G_{ab} \nu^b{}_j.
}
\]

If \(G_{ab}\) is positive semidefinite, then \(C_{ij}\) is positive semidefinite as a matrix over theory indices. This expresses the fact that competition is mediated by shared niche occupancy.

When mutualism is negligible and the environment is absorbed into \(r_i\), the ecological dynamics reduce to

\[
\dot n^i
=
n^i
\left(
r_i - C_{ij} n^j
\right).
\]

This is a generalized Lotka–Volterra competition system on theory space.

### 5.3 Mutualism and symbiosis

The mutualism tensor \(S_{ij}\) captures cases in which the presence of one theory increases the viability of another. Examples include:

- logic supporting computer science;
- category theory supporting algebraic geometry;
- probability theory supporting statistical physics;
- formal proof assistants supporting foundations;
- analysis supporting differential geometry.

If \(S_{ij}\) is large and \(C_{ij}\) moderate, theories form stable symbiotic clusters.

Define the net interaction tensor

\[
A_{ij} = C_{ij} - S_{ij}.
\]

Then

\[
\dot n^i
=
n^i
\left(
r_i - A_{ij} n^j
\right).
\]

The sign structure of \(A_{ij}\) determines coexistence, exclusion, or unbounded mutualistic amplification.

### 5.4 Niche saturation

Let \(K^a\) be the carrying capacity of niche \(a\). Niche saturation is

\[
\sigma^a
=
\frac{O^a}{K^a}
=
\frac{\nu^a{}_i n^i}{K^a}.
\]

A saturation penalty can be written as

\[
F_i^{\mathrm{sat}}
=
-
\eta_a \nu^a{}_i \sigma^a,
\]

or, more generally,

\[
F_i^{\mathrm{sat}}
=
-
\eta_a \nu^a{}_i f(\sigma^a),
\]

where \(f\) is increasing. This yields density-dependent suppression of theories that overoccupy a niche.

### 5.5 Open-problem ecology

Mathematical theories feed on open problems. Let \(P^a\) denote the density of open problems in niche \(a\). Theory \(i\) solves problems at rate \(\rho^a{}_i\). The problem-solving contribution to fitness is

\[
F_i^{\mathrm{prob}}
=
\rho^a{}_i P^a.
\]

The problem density evolves according to

\[
\dot P^a
=
\eta^a
+
\theta^{a i} n_i
-
\rho^a{}_i n^i P^a
-
\delta_P^a P^a.
\]

Here:

- \(\eta^a\) is exogenous problem generation;
- \(\theta^{a i} n_i\) is problem generation caused by theory \(i\);
- \(\rho^a{}_i n^i P^a\) is problem consumption;
- \(\delta_P^a\) is decay of relevance.

This is a central feedback loop: successful theories solve problems but also generate new problems, thereby constructing new niches.

---

## 6. Structural Adaptation

### 6.1 Structural traits

Let \(x_i^\alpha\) denote the structural traits of theory \(i\), with trait indices \(\alpha,\beta,\gamma,\dots\). Traits may include:

- abstraction level;
- axiom independence;
- proof modularity;
- formalizability;
- computational tractability;
- pedagogical accessibility;
- expressive power;
- consistency strength;
- interoperability with other theories.

The fitness functional becomes

\[
F_i = F_i(n,E,x).
\]

### 6.2 Adaptive gradient flow

A basic structural adaptation law is

\[
\boxed{
\dot x_i^\alpha
=
\eta_i \Pi_i^{\alpha\beta}
\frac{\partial F_i}{\partial x_i^\beta}
+
I_i^\alpha.
}
\]

Here:

- \(\eta_i\) is the adaptation rate;
- \(\Pi_i^{\alpha\beta}\) is a plasticity tensor;
- \(I_i^\alpha\) is innovation noise or directed invention.

If \(\Pi_i^{\alpha\beta}\) is positive semidefinite and \(I_i^\alpha=0\), then along the trait flow,

\[
\frac{\partial F_i}{\partial x_i^\alpha}
\dot x_i^\alpha
=
\eta_i
\frac{\partial F_i}{\partial x_i^\alpha}
\Pi_i^{\alpha\beta}
\frac{\partial F_i}{\partial x_i^\beta}
\geq 0.
\]

Thus structural adaptation locally increases fitness with respect to the theory’s own trait geometry.

### 6.3 Epistemic metric and covariant adaptation

If trait space carries an epistemic metric \(g_{\alpha\beta}\), adaptation may be written as gradient ascent with respect to that metric:

\[
\dot x_i^\alpha
=
\eta_i g^{\alpha\beta}
\frac{\partial F_i}{\partial x_i^\beta}.
\]

For curved trait spaces, the covariant form is

\[
\frac{D x_i^\alpha}{Dt}
=
\eta_i g^{\alpha\beta}
\nabla_\beta F_i,
\]

where \(\nabla_\beta\) is the covariant derivative associated with \(g_{\alpha\beta}\). This is appropriate when conceptual traits are not linearly parameterized.

### 6.4 Conservative and revolutionary adaptation

Let \(\mathcal{T}'\) be a structural modification of \(\mathcal{T}\). We say \(\mathcal{T}'\) is a **conservative adaptation** over language \(L(\mathcal{T})\) if

\[
L(\mathcal{T}) \subseteq L(\mathcal{T}')
\]

and for every sentence \(\varphi \in L(\mathcal{T})\),

\[
\mathcal{T}' \vdash \varphi
\iff
\mathcal{T} \vdash \varphi.
\]

Conservative adaptations preserve established corpus while increasing expressive or organizational capacity. Examples include definitional extensions, notation systems, categorical reformulations, and proof-theoretic normalization.

A **revolutionary adaptation** violates conservativity. It may solve anomalies but risks invalidating prior results. Revolutionary adaptations have high potential fitness but high viability risk.

### 6.5 Viability-constrained adaptation

Structural adaptation is constrained by

\[
\mathcal{V}(\mathcal{T}_i,x_i) \geq v_{\min}.
\]

The constrained adaptive flow may be written as a projected gradient:

\[
\dot x_i^\alpha
=
\Pi^{\alpha\beta}_i
\left(
\frac{\partial F_i}{\partial x_i^\beta}
-
\lambda_i
\frac{\partial \mathcal{V}_i}{\partial x_i^\beta}
\right),
\]

where \(\lambda_i\) is a Lagrange multiplier enforcing viability. This captures the tension between fruitfulness and foundational safety.

---

## 7. Analytical Results

### 7.1 Positivity and mass balance

**Proposition 1.**  
Let \(Q^i{}_j\) satisfy \(\sum_i Q^i{}_j=0\). Suppose \(F_i, R^i{}_{jk}, \Gamma^i{}_j\) are locally Lipschitz and preserve nonnegativity on the boundary. Then nonnegative initial data remain nonnegative. Moreover, in the absence of recombination, migration, and seed-bank exchange,

\[
\frac{d}{dt} N
=
F_i n^i.
\]

**Proof.**  
Summing the master equation over \(i\),

\[
\frac{d}{dt} n^i
=
n^i F_i
+
Q^i{}_j n^j
+
\frac{1}{2}R^i{}_{jk}n^j n^k
+
\cdots.
\]

If recombination and migration are omitted,

\[
\frac{dN}{dt}
=
\sum_i n^i F_i
+
\sum_i Q^i{}_j n^j.
\]

But

\[
\sum_i Q^i{}_j = 0,
\]

hence

\[
\frac{dN}{dt}
=
F_i n^i.
\]

Nonnegativity follows from the standard tangent condition for ecological systems: at \(n^i=0\), all endogenous terms except mutation and recombination inflow vanish or are nonnegative. ∎

### 7.2 Competitive equilibrium and niche packing

Consider the pure competition system

\[
\dot n^i
=
n^i
\left(
r_i - A_{ij} n^j
\right),
\]

with \(A_{ij}\) symmetric positive definite and \(r_i>0\).

An interior equilibrium satisfies

\[
r_i = A_{ij} n^{*j}.
\]

If \(A_{ij}\) is invertible,

\[
n^{*i}
=
(A^{-1})^{ij} r_j.
\]

**Theorem 1 (Global stability of positive equilibrium).**  
If \(n^{*i}>0\) for all \(i\), then \(n^*\) is globally asymptotically stable in the positive orthant.

**Proof.**  
Define the Goh-type Lyapunov function

\[
V(n)
=
\sum_i
\left(
n^i - n^{*i}
-
n^{*i}\log \frac{n^i}{n^{*i}}
\right).
\]

Then

\[
\dot V
=
\sum_i
\left(
1-\frac{n^{*i}}{n^i}
\right)
\dot n^i.
\]

Substitute the dynamics:

\[
\dot V
=
\sum_i
(n^i-n^{*i})
\left(
r_i - A_{ij}n^j
\right).
\]

Using

\[
r_i = A_{ij} n^{*j},
\]

we obtain

\[
\dot V
=
-\sum_i
(n^i-n^{*i})
A_{ij}
(n^j-n^{*j}).
\]

Since \(A_{ij}\) is positive definite,

\[
\dot V \leq 0,
\]

with equality only at \(n=n^*\). Hence \(n^*\) is globally asymptotically stable. ∎

Ecologically, this means that stable coexistence is possible when the net interaction tensor is stabilizing and the niche structure permits a positive equilibrium abundance vector.

### 7.3 Price equation for mathematical traits

Let \(z_i\) be a scalar trait associated with theory \(i\). Let \(W_i\) be discrete-time absolute fitness, so that

\[
p_i' = \frac{p_i W_i}{\overline{W}},
\]

where

\[
\overline{W} = p_i W_i.
\]

Allow the trait to change by \(\Delta z_i\) during transmission. The mean trait is

\[
\overline{z} = p_i z_i.
\]

Then

\[
\overline{z}'
=
\frac{p_i W_i (z_i+\Delta z_i)}{\overline{W}}.
\]

Therefore

\[
\Delta \overline{z}
=
\frac{p_i W_i z_i}{\overline{W}}
-
p_i z_i
+
\frac{p_i W_i \Delta z_i}{\overline{W}}.
\]

The first difference is

\[
\frac{p_i W_i z_i}{\overline{W}}
-
p_i z_i
=
\frac{p_i (W_i-\overline{W}) z_i}{\overline{W}}
=
\frac{\operatorname{Cov}(W_i,z_i)}{\overline{W}}.
\]

Hence

\[
\boxed{
\Delta \overline{z}
=
\frac{\operatorname{Cov}(W_i,z_i)}{\overline{W}}
+
\frac{\mathbb{E}[W_i \Delta z_i]}{\overline{W}}.
}
\]

This is the Price equation for theory populations. The first term describes selection on existing variation; the second describes transmission bias, structural adaptation, mutation, or directed innovation.

In continuous time, with fitness \(F_i\) and trait velocity \(\dot z_i\),

\[
\boxed{
\frac{d}{dt}\overline{z}
=
\operatorname{Cov}(F_i,z_i)
+
p_i \dot z_i.
}
\]

This separates ecological selection from internal conceptual change.

### 7.4 Invasion condition for a mutant theory

Suppose a rare mutant theory \(m\) enters a resident equilibrium \(n_R\). Its initial growth satisfies

\[
\frac{\dot n^m}{n^m}
\approx
F_m(n_R).
\]

The mutant invades if

\[
F_m(n_R) > 0.
\]

If mutation from resident \(j\) produces \(m\) at rate \(Q^m{}_j\), then even a non-growing mutant can be maintained by mutation pressure. With recombination, a novel fused theory \(k\) appears at rate

\[
\frac{1}{2}R^k{}_{ij}n^i n^j.
\]

It establishes if, after appearance, its invasion fitness satisfies

\[
F_k(n_R) > 0.
\]

Thus fusion-driven speciation requires both production and post-fusion viability.

### 7.5 Fusion advantage theorem

Let theories \(i\) and \(j\) possess complementary traits. Suppose their fusion produces theory \(k\) with trait vector

\[
x_k = \Theta(x_i,x_j),
\]

where \(\Theta\) is a composition operator. Define the complementarity functional

\[
\Delta_{ij}
=
F_k(x_k,n)
-
\max\{F_i(x_i,n),F_j(x_j,n)\}.
\]

If

\[
\Delta_{ij} > 0
\]

and

\[
R^k{}_{ij} n^i n^j > 0,
\]

then fusion creates a theory with selective advantage over both parents. In the deterministic limit, if \(F_k>0\) at the resident equilibrium, \(k\) will invade.

This formalizes mathematical unification: a merger is ecologically successful when it produces higher problem-solving capacity, lower redundancy, or access to new niches.

### 7.6 Disruptive selection and speciation

Let theory space be parameterized by a continuous trait \(x\). Let \(n(x,t)\) be a density over trait space. Consider

\[
\partial_t n(x,t)
=
n(x,t)
\left[
r(x)
-
\int C(x,y)n(y,t)\,dy
\right]
+
\text{mutation}.
\]

A monomorphic resident at \(x^*\) has equilibrium density approximately

\[
n^*(x^*)
=
\frac{r(x^*)}{C(x^*,x^*)}.
\]

The invasion fitness of a rare mutant \(y\) is

\[
s_{x^*}(y)
=
r(y)
-
C(y,x^*)n^*(x^*).
\]

An evolutionary singular point satisfies

\[
\left.
\frac{\partial s_{x^*}(y)}{\partial y}
\right|_{y=x^*}
=0.
\]

If

\[
\left.
\frac{\partial^2 s_{x^*}(y)}{\partial y^2}
\right|_{y=x^*}
>0,
\]

the singular point is convergence-stable but evolutionarily unstable, producing disruptive selection. This is the formal condition for adaptive branching of mathematical theories into specialized subpopulations.

---

## 8. Categorical Formulation

A theory population may also be described categorically.

Let \(\mathbf{Th}\) be a category whose objects are theories and whose morphisms are interpretations, translations, or conservative extensions:

\[
f : \mathcal{T} \to \mathcal{T}'.
\]

A population is a presheaf-like assignment

\[
\mu_t : \operatorname{Ob}(\mathbf{Th}) \to \mathbb{R}_{\geq 0},
\]

or, more generally, a measure on a suitable topological realization of \(\mathbf{Th}\).

Evolutionary operators become natural transformations or kernels on \(\mathbf{Th}\):

- mutation: a Markov kernel \(Q\) on objects;
- recombination: a bifunctorial operation
  \[
  \otimes : \mathbf{Th} \times \mathbf{Th} \to \mathbf{Th};
  \]
- selection: a weighting functor
  \[
  W_t : \mathbf{Th} \to \mathbb{R}_{>0};
  \]
- structural adaptation: a flow on the space of objects generated by viability-preserving morphisms.

This categorical layer clarifies the relationship between formal equivalence and ecological identity. Two theories may be ecologically distinct even if formally intertranslatable, because they may differ in cost of use, pedagogical accessibility, or computational implementation.

---

## 9. Applications

### 9.1 Foundations of mathematics

UME-II reframes foundational disputes as ecological competition among axiom populations.

A foundational theory \(\mathcal{F}\) has fitness components:

\[
F_{\mathcal{F}}
=
\alpha_{\mathrm{con}} V_{\mathrm{con}}
+
\alpha_{\mathrm{exp}} V_{\mathrm{exp}}
+
\alpha_{\mathrm{fruit}} V_{\mathrm{fruit}}
+
\alpha_{\mathrm{simp}} V_{\mathrm{simp}}
-
\alpha_{\mathrm{cost}} V_{\mathrm{cost}}.
\]

Here:

- \(V_{\mathrm{con}}\) is consistency confidence;
- \(V_{\mathrm{exp}}\) is expressive power;
- \(V_{\mathrm{fruit}}\) is theorem-generation capacity;
- \(V_{\mathrm{simp}}\) is simplicity or elegance;
- \(V_{\mathrm{cost}}\) is learning and verification cost.

Classical set theory, constructive type theory, category-theoretic foundations, and paraconsistent systems occupy different niches. UME-II predicts stable pluralism when niche overlap is low:

\[
C_{ij} = \nu^a{}_i G_{ab}\nu^b{}_j
\]

is small for \(i \neq j\). Foundational crises occur when a dominant theory saturates its niche while failing to solve newly generated problems. The crisis creates selection pressure for mutant or fused theories.

For example, naive set theory suffered a viability shock from paradoxes. The adaptive response was structural: axiomatization, type restrictions, separation principles, and later proof-theoretic and model-theoretic safeguards. The population did not merely reject inconsistent objects; it reorganized internal structure to restore viability.

Paraconsistent theories occupy a specialized niche in which local inconsistency is tolerated. Their viability is lower in classical environments but may be higher in niches requiring reasoning under contradiction, such as certain semantic, computational, or dialectical contexts.

### 9.2 History of mathematics

UME-II provides a quantitative grammar for historical transitions.

#### 9.2.1 Greek geometry and algebraic recombination

Greek geometry occupied a high-prestige niche of rigorous spatial reasoning. Its limitations in calculation and symbolic manipulation created open problems. Algebraic methods entered through Arabic and later European populations. The fusion of algebra and geometry produced analytic geometry. In UME-II terms, this is a recombination event:

\[
\mathcal{T}_{\mathrm{analytic}}
\sim
\mathcal{T}_{\mathrm{geometry}}
\otimes
\mathcal{T}_{\mathrm{algebra}}.
\]

The new theory accessed a broader niche:

\[
\nu^a_{\mathrm{analytic}}
=
\nu^a_{\mathrm{geometry}}
+
\nu^a_{\mathrm{algebra}}
+
\Delta^a_{\mathrm{syn}},
\]

where \(\Delta^a_{\mathrm{syn}}\) is a synergy term. The fusion increased fitness by enabling coordinate methods, calculation, and later dynamical modeling.

#### 9.2.2 Calculus and rigorization

Early calculus had high fruitfulness but low formal viability due to ambiguous infinitesimals. The fitness landscape can be represented as

\[
F_{\mathrm{calc}}
=
\text{high problem-solving yield}
-
\text{high consistency cost}.
\]

The nineteenth-century rigorization program was structural adaptation:

\[
x^\alpha_{\mathrm{calc}}
\longrightarrow
x^\alpha_{\mathrm{analysis}},
\]

where traits such as \(\epsilon\)-\(\delta\) definitions, completeness, and limit formalism increased \(V_{\mathrm{con}}\). This adaptation preserved much of the corpus while increasing viability. It was largely conservative with respect to established results.

Nonstandard analysis later reoccupied the infinitesimal niche. Its emergence illustrates seed-bank dynamics: the infinitesimal concept persisted in dormant form and became viable again after model theory provided a new environmental support.

#### 9.2.3 Algebraic geometry and categorical unification

Modern algebraic geometry arose through repeated fusion:

\[
\mathcal{T}_{\mathrm{AG}}
\leftarrow
\mathcal{T}_{\mathrm{geometry}}
\otimes
\mathcal{T}_{\mathrm{algebra}}
\otimes
\mathcal{T}_{\mathrm{number\ theory}}
\otimes
\mathcal{T}_{\mathrm{category}}.
\]

The Grothendieck revolution can be modeled as a high-abstraction structural adaptation. It increased modularity and generality but also increased complexity cost:

\[
\Delta F
=
\Delta F_{\mathrm{fruit}}
-
\Delta F_{\mathrm{cost}}.
\]

The population succeeded because the fruitfulness gain exceeded the pedagogical and computational cost in relevant niches.

### 9.3 AI-assisted mathematical discovery

UME-II is particularly suited to analyzing AI-assisted mathematics.

Large language models, automated conjecture generators, proof assistants, and formal verification systems alter the evolutionary operators.

#### 9.3.1 AI as mutation amplifier

An AI conjecture generator increases the mutation rate:

\[
Q^i{}_j
=
Q^{i,\mathrm{human}}{}_j
+
Q^{i,\mathrm{AI}}{}_j.
\]

The AI contribution may be several orders of magnitude larger in raw candidate production.

#### 9.3.2 AI as recombination engine

Retrieval systems and embedding models increase the probability that distant theories are combined:

\[
R^i{}_{jk}
=
R^{i,\mathrm{human}}{}_{jk}
+
R^{i,\mathrm{AI}}{}_{jk}.
\]

If semantic similarity embeddings identify latent analogies, then AI raises the recombination tensor for cross-domain fusions.

#### 9.3.3 Formal verification as selection filter

Proof assistants impose a strong viability filter. Let

\[
\chi_i =
\begin{cases}
1, & \text{if theory artifact } i \text{ is formally verified},\\
0, & \text{otherwise}.
\end{cases}
\]

Then verified artifacts have higher survival:

\[
d_i^{\mathrm{verified}} < d_i^{\mathrm{unverified}}.
\]

This produces selection toward formalizable mathematics.

#### 9.3.4 Expected corpus growth

Let \(C_i(t)\) be the corpus size of theory \(i\). A simple AI-mediated growth model is

\[
\dot C_i
=
\beta_i n^i
+
\theta_i^{\mathrm{AI}} n^i
-
\delta_i C_i,
\]

where \(\theta_i^{\mathrm{AI}}\) is AI-assisted theorem production. The average quality of generated theorems depends on the verification survival probability \(s_i\):

\[
\dot C_i^{\mathrm{verified}}
=
s_i
\left(
\beta_i n^i
+
\theta_i^{\mathrm{AI}} n^i
\right)
-
\delta_i C_i^{\mathrm{verified}}.
\]

If \(\theta_i^{\mathrm{AI}}\) grows faster than verification capacity \(s_i\), the system accumulates unverified noise. If verification capacity scales, AI can generate rapid adaptive radiation.

#### 9.3.5 Diversity metrics

Define the conceptual entropy of a mathematical ecosystem by

\[
H
=
-
\sum_i p^i \log p^i.
\]

Define niche diversity by

\[
H_N
=
-
\sum_a q^a \log q^a,
\qquad
q^a = \frac{O^a}{\sum_b O^b}.
\]

AI systems that maximize only theorem throughput may reduce \(H\) by overconcentrating production in easily formalized niches. A healthy mathematical ecology should optimize both productivity and diversity.

### 9.4 Knowledge evolution and epistemic resilience

UME-II also models mathematical knowledge as an evolving ecosystem of texts, curricula, and communities.

#### 9.4.1 Education as reproduction

Teaching is the primary birth process. If \(T_i\) is the number of teachers or texts supporting theory \(i\), then

\[
b_i \propto T_i.
\]

A theory with high pedagogical viability has high \(b_i\) and low learning cost \(\Omega_i\).

#### 9.4.2 Citation as mutualism

Citation networks approximate mutualism. If theory \(i\) cites theory \(j\), then

\[
S_{ij} > 0.
\]

Highly interconnected clusters are robust to local extinction but may become cognitively expensive.

#### 9.4.3 Extinction and revival

A theory becomes extinct when

\[
n^i < n_{\min}^i
\]

and its seed bank \(D^i\) decays below recoverability. However, digitization and formal archives increase seed-bank persistence:

\[
\epsilon^i \downarrow.
\]

Thus modern mathematical ecosystems should exhibit lower irreversible extinction rates but higher competition for attention.

#### 9.4.4 Epistemic resilience

The resilience of a mathematical ecosystem can be measured by the ability to maintain viable theory populations under shocks. A candidate resilience functional is

\[
\mathcal{R}
=
H_N
+
\lambda_1 \bar V
-
\lambda_2 C_{\mathrm{overlap}}
-
\lambda_3 \Omega_{\mathrm{complexity}},
\]

where \(\bar V\) is mean viability and \(C_{\mathrm{overlap}}\) is average niche overlap. Resilience increases with diversity and viability but decreases with excessive redundancy and complexity.

---

## 10. Computational and Empirical Operationalization

UME-II is not only formal but also empirically tractable.

### 10.1 Data sources

Theory populations can be estimated from:

- arXiv categories;
- MathSciNet and zbMATH metadata;
- citation networks;
- formal proof repositories;
- textbooks and curricula;
- conference communities;
- AI-generated conjecture logs;
- proof assistant libraries.

### 10.2 Niche embedding

Each mathematical document can be embedded into a vector space:

\[
d \mapsto \mathbf{e}_d \in \mathbb{R}^D.
\]

A theory cluster \(i\) has centroid \(\mu_i\). The niche affinity may be estimated by

\[
\nu^a{}_i
=
\frac{1}{|B_i|}
\sum_{d \in B_i}
\pi^a(\mathbf{e}_d),
\]

where \(\pi^a\) projects onto niche coordinate \(a\).

### 10.3 Fitness estimation

Fitness proxies include:

- growth rate of publications;
- citation growth;
- number of active researchers;
- theorem output;
- formalization rate;
- course adoption;
- software implementation;
- conjecture survival rate.

A statistical model may be written as

\[
\log \frac{n^i(t+\Delta t)}{n^i(t)}
=
F_i(t) + \varepsilon_i(t).
\]

The components of \(F_i\) can then be regressed against niche occupancy, competition, mutualism, and structural traits.

### 10.4 Parameter inference

The finite-dimensional system

\[
\dot n^i
=
n^i(r_i - A_{ij}n^j)
+
Q^i{}_j n^j
+
\frac12 R^i{}_{jk}n^j n^k
\]

can be fit using state-space methods. If observations are noisy,

\[
y^i_t = n^i_t + \eta^i_t,
\]

then Bayesian filtering or maximum likelihood estimation may infer \(r_i, A_{ij}, Q^i{}_j, R^i{}_{jk}\).

---

## 11. Conceptual Consequences

UME-I proposed that mathematics is ecological. UME-II makes the claim technically productive. Several consequences follow.

### 11.1 Theories are not chosen solely by truth

Theory choice is constrained by viability, fruitfulness, cost, and niche structure. A theory may persist despite the existence of a formally superior competitor because it occupies an entrenched pedagogical or computational niche.

### 11.2 Pluralism is ecologically expected

If niche space is heterogeneous, multiple theories can coexist. Pluralism is not merely philosophical; it is an equilibrium phenomenon.

### 11.3 Unification is recombination, not elimination

Unification does not necessarily reduce mathematics to one theory. It creates fused populations that may open new niches. Successful unification increases total niche capacity.

### 11.4 Inconsistency is ecological, not merely logical

Inconsistent or partially inconsistent structures can persist if they occupy niches where paraconsistent, heuristic, or local reasoning provides utility. Their survival depends on viability functions specific to those niches.

### 11.5 AI changes the evolutionary regime

AI does not merely assist mathematics; it modifies the mutation, recombination, and selection operators. The future structure of mathematics will depend on how AI balances candidate generation against verification capacity.

---

## 12. Limitations and Open Problems

The framework leaves several open problems.

1. **Individuation of theories.**  
   The boundary between one theory and another is scale-dependent. A robust theory of coarse-graining over \(\mathfrak{T}\) is needed.

2. **Parameter identifiability.**  
   Ecological parameters may be only partially observable. Inference methods must handle sparse and biased historical data.

3. **Normativity.**  
   UME-II describes evolutionary success, not necessarily mathematical correctness or value. A separate axiological layer is required to relate fitness to epistemic goodness.

4. **Infinite and continuous theory spaces.**  
   Measure-valued equations on infinite-dimensional theory spaces require careful well-posedness analysis.

5. **Cultural and institutional coupling.**  
   Mathematical populations are coupled to human institutions. Future work should integrate sociology, economics, and education into the ecological tensors.

---

## 13. Conclusion

Universal Mathematical Ecology II provides a formal theory of mathematical evolution. Its central construction is the treatment of mathematical theories as populations governed by ecological dynamics. The paper introduced the primitive concepts of theory populations, evolutionary operators, conceptual niches, and structural adaptation. It derived birth-death-mutation dynamics, recombination tensors, niche competition equations, Price-type trait equations, and stability results. It applied the framework to foundations, historical transitions, AI-assisted discovery, and knowledge evolution.

The main conclusion is that the global structure of mathematics is not the result of a linear accumulation of truths. It is an evolving ecological formation: a population of inferential structures competing for problems, agents, proof resources, and conceptual space; merging through recombination; specializing into niches; and adapting structurally under the pressure of consistency, utility, and transmission cost.

UME-II thus provides a foundation for a quantitative science of mathematical knowledge evolution.

---

## Appendix A: Notation

\[
\begin{array}{ll}
\mathfrak{T} & \text{Theory space} \\
\mathcal{T} & \text{A theory genotype} \\
\mu_t & \text{Population measure at time } t \\
n^i & \text{Abundance of theory type } i \\
p^i & \text{Frequency of theory type } i \\
N & \text{Total population} \\
F_i & \text{Fitness of theory } i \\
Q^i{}_j & \text{Mutation generator} \\
R^i{}_{jk} & \text{Recombination tensor} \\
\nu^a{}_i & \text{Niche affinity of theory } i \text{ for niche } a \\
O^a & \text{Occupancy of niche } a \\
K^a & \text{Carrying capacity of niche } a \\
C_{ij} & \text{Competition tensor} \\
S_{ij} & \text{Mutualism tensor} \\
A_{ij} & \text{Net interaction tensor} \\
x_i^\alpha & \text{Structural trait } \alpha \text{ of theory } i \\
\Pi_i^{\alpha\beta} & \text{Plasticity tensor} \\
P^a & \text{Open problem density in niche } a \\
D^i & \text{Dormant abundance of theory } i \\
H & \text{Conceptual entropy} \\
H_N & \text{Niche diversity entropy}
\end{array}
\]

---

## Appendix B: Summary of Core Equations

**Master population equation:**

\[
\dot n^i
=
n^i F_i(n,E,x)
+
Q^i{}_j n^j
+
\frac{1}{2} R^i{}_{jk} n^j n^k
+
\Gamma^i{}_j n^j
+
\gamma^i D^i
-
\delta^i n^i.
\]

**Niche occupancy:**

\[
O^a = \nu^a{}_i n^i.
\]

**Competition tensor:**

\[
C_{ij}
=
\nu^a{}_i G_{ab} \nu^b{}_j.
\]

**Pure competition dynamics:**

\[
\dot n^i
=
n^i
\left(
r_i - A_{ij} n^j
\right).
\]

**Structural adaptation:**

\[
\dot x_i^\alpha
=
\eta_i \Pi_i^{\alpha\beta}
\frac{\partial F_i}{\partial x_i^\beta}
+
I_i^\alpha.
\]

**Continuous Price equation:**

\[
\frac{d}{dt}\overline{z}
=
\operatorname{Cov}(F_i,z_i)
+
p_i \dot z_i.
\]

**Open-problem ecology:**

\[
\dot P^a
=
\eta^a
+
\theta^{a i} n_i
-
\rho^a{}_i n^i P^a
-
\delta_P^a P^a.
\]

**Seed-bank dynamics:**

\[
\dot n^i
=
n^i F_i + \gamma^i D^i - \delta^i n^i + \cdots,
\]

\[
\dot D^i
=
\delta^i n^i - \gamma^i D^i - \epsilon^i D^i.
\]

---

## Appendix C: Proposed Research Program

1. Develop measure-theoretic well-posedness theory for infinite-dimensional UME-II dynamics.
2. Construct categorical models of theory fusion using pushouts, profunctors, and interpretation categories.
3. Fit UME-II models to historical corpora using embeddings and citation networks.
4. Design AI discovery systems that optimize ecological diversity rather than raw theorem throughput.
5. Create formal proof-environment metrics for viability, complexity cost, and structural adaptation.
6. Study paraconsistent and nonclassical foundations as specialized ecological niches.
7. Analyze educational systems as reproductive environments for mathematical populations.

The program establishes UME-II as a formal discipline at the intersection of mathematical logic, dynamical systems, epistemology, history of mathematics, and AI-assisted discovery.

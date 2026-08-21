# Recursive Mathematical Ecology: A Formal Theory of Populations of Interacting Mathematical Structures

**Preprint**

---

## Abstract

We develop **Recursive Mathematical Ecology** (RME), a formal framework in which mathematical structures are treated as ecological populations. In RME, objects such as formulas, programs, proofs, graphs, tensors, architectures, heuristics, and transformation rules are represented as organisms inhabting a measurable structure space. These organisms compete for evaluative resources, cooperate through compositional or inferential interactions, reproduce by variation and recombination, and disappear through extinction induced by low fitness, inconsistency, irrelevance, or resource exhaustion. The central novelty of RME is **recursive closure**: mathematical organisms may encode operators that modify the fitness function, mutation kernel, resource dynamics, or ecological transition law itself. The population therefore generates the very law governing its future evolution. We formulate RME in both finite-dimensional tensorial form and measure-valued continuous form, derive replicator–mutator and Lotka–Volterra-type dynamics, prove existence of self-consistent recursive equilibria, give extinction and invasion criteria, establish stability results for symmetric competition systems, and provide a variational interpretation connecting RME to stochastic optimization. We then apply the theory to evolutionary algorithms, optimization, artificial intelligence, and complex systems. RME provides a unified mathematical language for open-ended evolution, self-modifying search, co-evolutionary learning, and ecosystems of mathematical knowledge.

**Keywords:** recursive dynamical systems, mathematical ecology, evolutionary computation, measure-valued population dynamics, tensor interactions, self-modifying systems, coevolution, open-ended learning.

---

## 1. Introduction

Classical ecology studies populations of biological organisms interacting through competition, predation, mutualism, parasitism, reproduction, and death. Evolutionary computation abstracts this process into populations of candidate solutions subjected to selection, mutation, recombination, and replacement. In both cases, the entities being evolved are usually passive objects acted upon by a fixed external evolutionary law: a fixed fitness function, a fixed mutation operator, a fixed crossover operator, and a fixed selection mechanism.

Recursive Mathematical Ecology begins from a stronger premise:

> **Mathematical structures are not merely objects acted upon by an evolutionary process; they can be treated as ecological agents that generate, modify, and inherit the operators by which they are transformed and evaluated.**

In this view, a population may contain not only candidate solutions but also search operators, proof tactics, evaluation heuristics, representations, compression schemes, and meta-learning rules. These objects interact with one another. Some compete for computational resources or explanatory power. Others cooperate by composing into larger structures. Some reproduce by generating variants. Some vanish because they are inconsistent, inefficient, or dominated by superior structures. Crucially, some organisms encode rules that modify the ecology itself.

This produces a recursive system:

\[
\text{population} \longrightarrow \text{operator} \longrightarrow \text{population transition law} \longrightarrow \text{population}.
\]

RME formalizes this recursion as a dynamical system on populations, environments, and operators. It is intended as a foundational framework for:

1. **Evolutionary algorithms** in which variation operators, representations, and fitness evaluators coevolve with solutions.
2. **Optimization** in which the search law adapts to the structure of the objective landscape.
3. **Artificial intelligence** in which hypotheses, programs, proofs, architectures, and learning rules form interacting ecosystems.
4. **Complex systems** in which macro-level organization emerges from micro-level mathematical interactions.

The present paper develops RME as a formal theory. We introduce object spaces, population measures, resource fields, fitness functionals, interaction tensors, mutation kernels, and recursive operator maps. We derive dynamical equations, prove several foundational results, and demonstrate how the framework specializes to known computational paradigms while also suggesting new classes of recursive algorithms.

---

## 2. Primitive Notions

### 2.1 Mathematical object space

Let

\[
\mathcal{M}
\]

be a measurable space of mathematical objects. Elements

\[
m \in \mathcal{M}
\]

are called **mathematical organisms**. Depending on the application, \(\mathcal{M}\) may encode:

- symbolic expressions,
- logical formulas,
- proofs,
- programs,
- neural architectures,
- tensor networks,
- graphs,
- categories,
- optimization heuristics,
- mutation operators,
- fitness evaluators,
- compression schemes,
- policies,
- theorem-proving tactics,
- data representations.

We assume \(\mathcal{M}\) is equipped with a \(\sigma\)-algebra \(\mathcal{B}(\mathcal{M})\), allowing populations to be represented as measures.

A **population** at time \(t\) is a finite nonnegative measure

\[
\mu_t \in \mathcal{M}_+(\mathcal{M}).
\]

For any measurable set \(A \subseteq \mathcal{M}\),

\[
\mu_t(A)
\]

is the abundance of organisms whose structure lies in \(A\). The total population size is

\[
N(t) = \int_{\mathcal{M}} d\mu_t(m).
\]

When \(N(t)>0\), the normalized population distribution is

\[
p_t = \frac{\mu_t}{N(t)}.
\]

### 2.2 Phenotype and evaluation

A mathematical organism may possess an internal syntactic form and an external functional behavior. We distinguish:

- **Genotype**: the encoded structure \(m\).
- **Phenotype**: the evaluated behavior of \(m\).

Let

\[
\Phi : \mathcal{M} \to \mathcal{P}
\]

be a phenotype map into a phenotype space \(\mathcal{P}\). For example, if \(m\) is a program, \(\Phi(m)\) may be its input-output function. If \(m\) is a proof, \(\Phi(m)\) may be its verified theorem. If \(m\) is a neural architecture, \(\Phi(m)\) may be its trained predictor.

An **environment** is represented by a state

\[
e_t \in \mathcal{E}.
\]

In many cases the environment contains a resource vector

\[
r_t \in \mathbb{R}_+^q,
\]

where resources may denote computational budget, memory, data access, proof search time, representational capacity, or epistemic utility.

A **fitness functional**

\[
\varphi : \mathcal{M} \times \mathcal{M}_+(\mathcal{M}) \times \mathcal{E} \to \mathbb{R}
\]

assigns to organism \(m\) a net growth rate

\[
\varphi(m;\mu_t,e_t).
\]

Fitness is generally frequency-dependent and environment-dependent.

### 2.3 Resources and niches

Resources evolve according to an environmental map

\[
\dot r_t = S(r_t) - D(r_t) - C(\mu_t,r_t),
\]

where:

- \(S\) is a supply term,
- \(D\) is decay or depreciation,
- \(C\) is consumption by the population.

A **niche** is a region of object-environment space where invasion fitness is positive. Formally, given a resident population \(\mu\), a rare mutant \(m\) has invasion fitness

\[
\lambda(m;\mu,e) = \varphi(m;\mu,e).
\]

If

\[
\lambda(m;\mu,e) > 0,
\]

then \(m\) can invade the resident ecology, at least locally.

---

## 3. Tensorial Discrete Population Dynamics

We first develop a finite-type model. Let there be \(n\) organism types indexed by

\[
i = 1,\dots,n.
\]

Let

\[
x^i(t) \ge 0
\]

denote the abundance of type \(i\). We use Einstein summation convention where appropriate, and we raise or lower indices using the Euclidean metric unless otherwise stated.

Let

\[
r^\alpha(t) \ge 0, \qquad \alpha = 1,\dots,q,
\]

denote environmental resources.

### 3.1 Resource dynamics

The resource field evolves as

\[
\dot r^\alpha
=
S^\alpha(r)
-
\lambda^\alpha r^\alpha
-
c^\alpha{}_i x^i,
\tag{3.1}
\]

where:

- \(S^\alpha(r)\) is the supply rate of resource \(\alpha\),
- \(\lambda^\alpha > 0\) is its decay rate,
- \(c^\alpha{}_i \ge 0\) is the consumption tensor describing use of resource \(\alpha\) by organism type \(i\).

Equation (3.1) couples ecological abundance to environmental capacity.

### 3.2 Fitness tensor decomposition

The per-capita net growth rate of type \(i\) is written as

\[
f^i(x,r)
=
\beta^i{}_\alpha r^\alpha
-
d^i
-
a^i{}_j x^j
+
\frac{1}{2}
b^i{}_{jk} x^j x^k.
\tag{3.2}
\]

Here:

- \(\beta^i{}_\alpha\) is the resource-utilization tensor,
- \(d^i \ge 0\) is baseline death or rejection rate,
- \(a^i{}_j \ge 0\) is the competition tensor,
- \(b^i{}_{jk}\) is the cooperation or autocatalytic production tensor.

The term

\[
\beta^i{}_\alpha r^\alpha
\]

represents fitness gained from resources.

The term

\[
-a^i{}_j x^j
\]

represents competitive suppression by other types.

The term

\[
\frac{1}{2} b^i{}_{jk} x^j x^k
\]

represents nonlinear cooperative enhancement. For example, two mathematical structures may combine to generate a third, more valuable structure.

We usually assume

\[
b^i{}_{jk} = b^i{}_{kj},
\]

so that pairwise cooperation is symmetric in its contributors, although asymmetric generalizations are possible.

### 3.3 Mutation and variation

Let

\[
U^i{}_j
\]

be a variation or mutation tensor. If \(U^i{}_j\) describes flow from type \(j\) to type \(i\), conservation of total mass requires

\[
\sum_i U^i{}_j = 0
\quad
\text{for each } j.
\tag{3.3}
\]

Equivalently, in tensor notation,

\[
\mathbf{1}_i U^i{}_j = 0.
\]

The off-diagonal components satisfy

\[
U^i{}_j \ge 0
\quad
\text{for } i \neq j,
\]

while diagonal components are negative and given by total outgoing flow.

### 3.4 Absolute abundance dynamics

The ecological dynamics are

\[
\dot x^i
=
x^i f^i(x,r)
+
U^i{}_j x^j.
\tag{3.4}
\]

Expanding,

\[
\dot x^i
=
x^i
\left(
\beta^i{}_\alpha r^\alpha
-
d^i
-
a^i{}_j x^j
+
\frac{1}{2}
b^i{}_{jk}x^jx^k
\right)
+
U^i{}_j x^j.
\tag{3.5}
\]

This is a recursive generalization of Lotka–Volterra and replicator–mutator dynamics.

### 3.5 Normalized replicator–mutator form

Let

\[
N = \sum_i x^i,
\qquad
p^i = \frac{x^i}{N}.
\]

Using (3.3), the total population satisfies

\[
\dot N
=
N \bar f,
\]

where

\[
\bar f = p_i f^i.
\]

Differentiating \(p^i = x^i/N\) gives

\[
\dot p^i
=
p^i(f^i - \bar f)
+
U^i{}_j p^j.
\tag{3.6}
\]

Equation (3.6) is the **replicator–mutator equation with ecological feedback**.

Substituting (3.2), we obtain

\[
\begin{aligned}
\bar f
&=
p_i \beta^i{}_\alpha r^\alpha
-
p_i d^i
-
N p_i a^i{}_j p^j
+
\frac{N^2}{2}
p_i b^i{}_{jk} p^j p^k.
\end{aligned}
\tag{3.7}
\]

Thus selection is generally frequency-dependent and population-size-dependent.

### 3.6 Interpretation of tensor terms

The tensors have the following ecological meanings:

| Tensor | Role |
|---|---|
| \(\beta^i{}_\alpha\) | Resource exploitation |
| \(d^i\) | Baseline mortality or rejection |
| \(a^i{}_j\) | Competitive suppression |
| \(b^i{}_{jk}\) | Cooperative production or autocatalysis |
| \(U^i{}_j\) | Mutation, variation, or structural transformation |
| \(c^\alpha{}_i\) | Resource consumption |

In RME, these tensors are not necessarily fixed. Recursive organisms may modify them.

---

## 4. Measure-Valued Formulation

For infinite or continuous object spaces, the finite-type vector \(x^i\) is replaced by a measure \(\mu_t\).

Let

\[
\beta(m;\mu_t,r_t)
\]

be the birth rate of organism \(m\), and let

\[
\delta(m;\mu_t,r_t)
\]

be its death rate.

Let

\[
K(dm' \mid m)
\]

be a Markov kernel giving the distribution of offspring or mutants produced by parent \(m\).

Then the non-cooperative part of the population dynamics is

\[
\begin{aligned}
\frac{d}{dt}\mu_t(A)
&=
\int_{\mathcal{M}}
K(A \mid m)
\beta(m;\mu_t,r_t)
\,\mu_t(dm)
\\
&\quad
-
\int_A
\delta(m;\mu_t,r_t)
\,\mu_t(dm).
\end{aligned}
\tag{4.1}
\]

To include cooperation, let

\[
C(dz \mid m,m')
\]

be a kernel describing the production of new object \(z\) from interaction of \(m\) and \(m'\), with rate

\[
\gamma(m,m';\mu_t,r_t).
\]

Then

\[
\begin{aligned}
\frac{d}{dt}\mu_t(A)
&=
\int_{\mathcal{M}}
K(A \mid m)
\beta(m;\mu_t,r_t)
\,\mu_t(dm)
\\
&\quad
-
\int_A
\delta(m;\mu_t,r_t)
\,\mu_t(dm)
\\
&\quad
+
\frac{1}{2}
\int_{\mathcal{M}}
\int_{\mathcal{M}}
C(A \mid m,m')
\gamma(m,m';\mu_t,r_t)
\,\mu_t(dm)\mu_t(dm').
\end{aligned}
\tag{4.2}
\]

The factor \(1/2\) avoids double counting unordered cooperative pairs when \(\gamma\) is symmetric.

For a test function \(\psi : \mathcal{M} \to \mathbb{R}\), the weak form is

\[
\begin{aligned}
\frac{d}{dt}
\int \psi(m)\,\mu_t(dm)
&=
\int
\left[
\int \psi(m')K(dm'\mid m)-\psi(m)
\right]
\beta(m;\mu_t,r_t)
\,\mu_t(dm)
\\
&\quad
-
\int
\psi(m)\delta(m;\mu_t,r_t)
\,\mu_t(dm)
\\
&\quad
+
\frac{1}{2}
\int
\int
\left[
\int \psi(z)C(dz\mid m,m')-\psi(m)
\right]
\gamma(m,m';\mu_t,r_t)
\,\mu_t(dm)\mu_t(dm').
\end{aligned}
\tag{4.3}
\]

Equations (4.1)–(4.3) define a generalized ecological generator. We write this compactly as

\[
\partial_t \mu_t = \mathcal{L}_{\mu_t,r_t}^* \mu_t,
\tag{4.4}
\]

where \(\mathcal{L}_{\mu_t,r_t}\) is the generator acting on observables and \(\mathcal{L}_{\mu_t,r_t}^*\) is its adjoint acting on measures.

---

## 5. Recursive Closure

The defining feature of RME is that the generator of ecological dynamics may itself be produced by the population.

### 5.1 Operator-valued organisms

Let

\[
\mathfrak{L}
\]

be a space of admissible ecological operators. Elements of \(\mathfrak{L}\) may modify:

- mutation kernels,
- fitness functions,
- resource dynamics,
- cooperation rules,
- selection temperature,
- proof-search tactics,
- optimization heuristics,
- representation encodings.

Each organism \(m\) may encode an operator

\[
\Theta(m) \in \mathfrak{L}.
\]

The map

\[
\Theta : \mathcal{M} \to \mathfrak{L}
\]

is called the **operator encoding map**.

Not all organisms have equal influence. Let

\[
w(m;\mu_t,r_t) \ge 0
\]

be an influence weight. For example, \(w\) may depend on fitness, recency, proof validity, computational efficiency, or epistemic credibility.

Define the normalized aggregate operator

\[
\bar\Theta(\mu_t,r_t)
=
\frac{
\int_{\mathcal{M}}
\Theta(m) w(m;\mu_t,r_t)
\,\mu_t(dm)
}{
\int_{\mathcal{M}}
w(m;\mu_t,r_t)
\,\mu_t(dm)
+
\varepsilon
},
\tag{5.1}
\]

where \(\varepsilon>0\) prevents division by zero.

### 5.2 Recursive continuous-time dynamics

Let \(L_t \in \mathfrak{L}\) be the effective ecological operator at time \(t\). We propose the continuous recursive system

\[
\partial_t \mu_t
=
\mathcal{L}_{L_t}^* \mu_t,
\tag{5.2}
\]

\[
\tau \dot L_t
=
\bar\Theta(\mu_t,r_t)-L_t,
\tag{5.3}
\]

\[
\dot r_t
=
S(r_t)-D(r_t)-C(\mu_t,r_t,L_t).
\tag{5.4}
\]

Here \(\tau>0\) is a recursion relaxation time.

Equation (5.2) states that the population evolves according to the current operator.

Equation (5.3) states that the operator evolves toward the population-encoded aggregate operator.

Equation (5.4) states that the environment is affected by both population and operator.

The system is recursively closed: the population produces the operator, and the operator produces the future population.

### 5.3 Discrete-time recursive ecology

For algorithmic implementation, a discrete-time form is often preferable. Let

\[
T_L : \mathcal{M}_+(\mathcal{M}) \times \mathcal{E} \to \mathcal{M}_+(\mathcal{M})
\]

be the population transition map induced by operator \(L\).

Let

\[
R_L : \mathcal{E} \times \mathcal{M}_+(\mathcal{M}) \to \mathcal{E}
\]

be the environment update map.

Then a discrete RME is

\[
\mu_{t+1}
=
T_{L_t}(\mu_t,r_t),
\tag{5.5}
\]

\[
r_{t+1}
=
R_{L_t}(r_t,\mu_t),
\tag{5.6}
\]

\[
L_{t+1}
=
(1-\rho)L_t
+
\rho \bar\Theta(\mu_t,r_t),
\tag{5.7}
\]

where

\[
0 \le \rho \le 1
\]

is the recursive adaptation rate.

The case \(\rho=0\) recovers a fixed-law evolutionary system. The case \(\rho>0\) produces genuine recursive mathematical ecology.

### 5.4 Self-consistent ecological laws

A recursively closed equilibrium satisfies

\[
\mu^*
=
T_{L^*}(\mu^*,r^*),
\tag{5.8}
\]

\[
r^*
=
R_{L^*}(r^*,\mu^*),
\tag{5.9}
\]

\[
L^*
=
\bar\Theta(\mu^*,r^*).
\tag{5.10}
\]

Equivalently,

\[
(\mu^*,r^*,L^*)
\]

is a fixed point of the meta-map

\[
H(\mu,r,L)
=
\left(
T_L(\mu,r),
R_L(r,\mu),
\bar\Theta(\mu,r)
\right).
\tag{5.11}
\]

This is the central self-consistency condition of RME.

---

## 6. Analytical Results

We now establish several foundational results.

---

### Theorem 1: Existence of self-consistent recursive equilibria

Let \(\Delta_n\) be the finite-type population simplex,

\[
\Delta_n
=
\left\{
p \in \mathbb{R}_+^n : \sum_i p^i = 1
\right\}.
\]

Let \(K \subset \mathbb{R}_+^q\) be a compact convex resource set, and let \(\mathfrak{L}\) be a compact convex set of operators.

Assume the maps

\[
T : \Delta_n \times K \times \mathfrak{L} \to \Delta_n,
\]

\[
R : K \times \Delta_n \times \mathfrak{L} \to K,
\]

\[
\Lambda : \Delta_n \times K \to \mathfrak{L}
\]

are continuous.

Define

\[
H(p,r,L)
=
\left(
T(p,r,L),
R(r,p,L),
\Lambda(p,r)
\right).
\]

Then \(H\) has at least one fixed point

\[
(p^*,r^*,L^*) = H(p^*,r^*,L^*).
\]

Moreover, if \(H\) is a contraction with respect to a metric on \(\Delta_n \times K \times \mathfrak{L}\), the fixed point is unique.

#### Proof

The set

\[
C = \Delta_n \times K \times \mathfrak{L}
\]

is nonempty, compact, and convex. By assumption, \(H:C \to C\) is continuous. Therefore, by Brouwer’s fixed-point theorem, there exists

\[
z^* \in C
\]

such that

\[
H(z^*) = z^*.
\]

Writing \(z^*=(p^*,r^*,L^*)\) gives the desired equilibrium.

If \(H\) is a contraction, then Banach’s fixed-point theorem yields uniqueness and convergence of the iteration

\[
z_{t+1} = H(z_t).
\]

∎

---

### Theorem 2: Extinction and invasion criterion

Consider the finite-type system near the extinction state \(x=0\). Suppose the resource dynamics without organisms possess an equilibrium \(r^0\) satisfying

\[
S(r^0)-\lambda r^0 = 0.
\]

Linearizing (3.5) about \(x=0\), \(r=r^0\) yields

\[
\dot x^i
=
A^i{}_j x^j,
\tag{6.1}
\]

where

\[
A^i{}_j
=
\left(
\beta^i{}_\alpha r^{0\alpha}
-
d^i
\right)\delta^i{}_j
+
U^i{}_j.
\tag{6.2}
\]

Let

\[
s(A) = \max\{\operatorname{Re}\lambda : \lambda \in \sigma(A)\}
\]

be the spectral bound of \(A\).

Then:

1. If \(s(A)<0\), the extinction state is locally exponentially stable.
2. If \(s(A)>0\), there exists at least one invading mode that grows locally.
3. If \(A\) is irreducible Metzler, the dominant eigenvalue determines invasion fitness.

#### Proof

The linearized system is

\[
\dot x = Ax.
\]

Its solution is

\[
x(t) = e^{At}x(0).
\]

If \(s(A)<0\), then there exist constants \(M,\alpha>0\) such that

\[
\|e^{At}\| \le M e^{-\alpha t}.
\]

Thus \(x(t)\to 0\) exponentially.

If \(s(A)>0\), there exists an eigenvalue \(\lambda\) with positive real part. For initial conditions with nonzero projection onto the associated eigenspace, the solution grows like \(e^{\lambda t}\).

When \(A\) is Metzler, meaning its off-diagonal entries are nonnegative, the Perron–Frobenius theorem for Metzler matrices implies that the dominant eigenvalue is real and has a nonnegative eigenvector. This eigenvector corresponds to a viable invading population structure.

∎

---

### Theorem 3: Stability of symmetric competitive ecologies

Consider the special case with constant resources, no mutation, and no cooperation:

\[
\dot x_i
=
x_i
\left(
r_i - \sum_j a_{ij}x_j
\right).
\tag{6.3}
\]

Assume the competition matrix

\[
A = (a_{ij})
\]

is symmetric and positive definite. Suppose there exists a positive equilibrium

\[
x^* \in \mathbb{R}_{++}^n
\]

satisfying

\[
A x^* = r.
\tag{6.4}
\]

Define

\[
V(x)
=
\sum_i
\left(
x_i - x_i^* - x_i^* \ln \frac{x_i}{x_i^*}
\right).
\tag{6.5}
\]

Then \(V(x)\ge 0\), with equality only at \(x=x^*\), and

\[
\dot V(x)
=
-
\sum_{i,j}
(x_i-x_i^*)a_{ij}(x_j-x_j^*)
\le 0.
\tag{6.6}
\]

If \(A\) is positive definite, \(x^*\) is globally asymptotically stable in \(\mathbb{R}_{++}^n\).

#### Proof

Since

\[
z - 1 - \ln z \ge 0
\]

for \(z>0\), each term in \(V\) is nonnegative, and \(V(x)=0\) iff \(x=x^*\).

Differentiate:

\[
\dot V
=
\sum_i
\left(
1 - \frac{x_i^*}{x_i}
\right)
\dot x_i.
\]

Using (6.3),

\[
\dot V
=
\sum_i
(x_i-x_i^*)
\left(
r_i - \sum_j a_{ij}x_j
\right).
\]

By equilibrium condition (6.4),

\[
r_i = \sum_j a_{ij}x_j^*.
\]

Therefore,

\[
\dot V
=
\sum_i
(x_i-x_i^*)
\left(
\sum_j a_{ij}x_j^*
-
\sum_j a_{ij}x_j
\right).
\]

Thus

\[
\dot V
=
-
\sum_{i,j}
(x_i-x_i^*)a_{ij}(x_j-x_j^*).
\]

If \(A\) is symmetric positive definite, this quadratic form is positive definite, so

\[
\dot V < 0
\]

for all \(x\neq x^*\) in \(\mathbb{R}_{++}^n\). Hence \(x^*\) is globally asymptotically stable.

∎

---

### Proposition 4: Boltzmann stationary distribution for fixed-fitness RME optimization

Let fitness \(f_i\) be frequency-independent. Let proposal kernel \(Q_{ij}\) be symmetric and irreducible. Define a Metropolis transition

\[
P_{ij}
=
Q_{ij}
\min\left\{
1,
\exp\left(
\frac{f_j-f_i}{T}
\right)
\right\},
\qquad i\neq j,
\tag{6.7}
\]

with diagonal entries chosen so that rows sum to one.

Then the stationary distribution is

\[
\pi_i
=
\frac{
\exp(f_i/T)
}{
\sum_k \exp(f_k/T)
}.
\tag{6.8}
\]

#### Proof

For \(i\neq j\), detailed balance requires

\[
\pi_i P_{ij} = \pi_j P_{ji}.
\]

Using symmetry \(Q_{ij}=Q_{ji}\),

\[
\pi_i P_{ij}
=
\frac{e^{f_i/T}}{Z}
Q_{ij}
\min\left\{
1,
e^{(f_j-f_i)/T}
\right\}.
\]

If \(f_j\ge f_i\), this equals

\[
\frac{1}{Z}
Q_{ij}
e^{f_j/T}.
\]

The reverse term is

\[
\pi_j P_{ji}
=
\frac{e^{f_j/T}}{Z}
Q_{ji}
\min\left\{
1,
e^{(f_i-f_j)/T}
\right\}
=
\frac{1}{Z}
Q_{ij}
e^{f_j/T}.
\]

The case \(f_i>f_j\) is analogous. Therefore detailed balance holds, and \(\pi\) is stationary. Irreducibility implies uniqueness.

∎

---

## 7. Variational Interpretation

For fixed fitness \(f_i\) and temperature \(T>0\), the stationary distribution (6.8) maximizes the free-energy functional

\[
\mathcal{J}[p]
=
\sum_i p_i f_i
+
T H(p),
\tag{7.1}
\]

where

\[
H(p)
=
-
\sum_i p_i \ln p_i
\]

is the Shannon entropy.

Indeed, maximizing \(\mathcal{J}\) under the constraint \(\sum_i p_i=1\) gives the Lagrangian

\[
\mathcal{L}[p,\lambda]
=
\sum_i p_i f_i
+
T H(p)
-
\lambda
\left(
\sum_i p_i - 1
\right).
\]

Differentiating,

\[
\frac{\partial \mathcal{L}}{\partial p_i}
=
f_i
-
T(\ln p_i + 1)
-
\lambda
=
0.
\]

Thus

\[
\ln p_i
=
\frac{f_i}{T}
-
1
-
\frac{\lambda}{T},
\]

so

\[
p_i
\propto
e^{f_i/T}.
\]

In RME, however, fitness may depend on the population and on the recursive operator:

\[
f_i = f_i(p,L,r).
\]

The variational problem becomes self-consistent:

\[
p_i
=
\frac{
\exp(f_i(p,L,r)/T)
}{
\sum_k \exp(f_k(p,L,r)/T)
},
\tag{7.2}
\]

\[
L
=
\Lambda(p,r).
\tag{7.3}
\]

Thus RME generalizes maximum-entropy evolutionary optimization to recursive, self-modifying systems.

---

## 8. Algorithmic Realization

We now describe an abstract RME algorithm.

---

### Algorithm 1: Recursive Mathematical Ecology

**Input:**

- initial population \(\mu_0\),
- initial environment \(r_0\),
- initial operator \(L_0\),
- evaluation functional \(\varphi\),
- operator encoding map \(\Theta\),
- influence weight \(w\),
- recursion rate \(\rho\),
- number of generations \(T\).

**Output:**

- final population \(\mu_T\),
- final recursive operator \(L_T\),
- elite organism(s) \(m_{\text{best}}\).

For \(t=0,1,\dots,T-1\):

1. **Evaluate organisms**

   For each \(m \in \operatorname{supp}(\mu_t)\), compute

   \[
   \varphi_t(m)
   =
   \varphi(m;\mu_t,r_t,L_t).
   \]

2. **Select parents**

   Sample parents according to a selection rule, for example Boltzmann selection

   \[
   \Pr(m \text{ selected})
   \propto
   \exp(\varphi_t(m)/T_t).
   \]

3. **Apply current operator**

   Use \(L_t\) to generate offspring. The operator \(L_t\) may include mutation, crossover, theorem proving, program synthesis, architecture modification, or hyperparameter adaptation.

4. **Update population**

   Form \(\mu_{t+1}\) by replacing low-fitness organisms and adding offspring.

5. **Update environment**

   Compute

   \[
   r_{t+1}
   =
   R_{L_t}(r_t,\mu_t).
   \]

6. **Extract recursive operators**

   Compute

   \[
   \bar\Theta_t
   =
   \frac{
   \int \Theta(m)w(m;\mu_t,r_t)\,\mu_t(dm)
   }{
   \int w(m;\mu_t,r_t)\,\mu_t(dm)
   +
   \varepsilon
   }.
   \]

7. **Update ecological law**

   Set

   \[
   L_{t+1}
   =
   (1-\rho)L_t
   +
   \rho \bar\Theta_t.
   \]

8. **Archive elites**

   Store high-fitness organisms in an elite archive.

Return the final population and operator.

---

### Remarks on implementation

The operator \(L_t\) may be represented as:

- a probabilistic program,
- a neural network,
- a probabilistic model,
- a grammar,
- a proof tactic,
- a set of rewrite rules,
- a tensor of transition probabilities,
- a learned policy.

The influence weight \(w\) may be chosen as

\[
w(m;\mu,r)
=
\exp(\varphi(m;\mu,r)/T),
\]

or as a robust credibility measure incorporating verification, compression length, or generalization performance.

---

## 9. Applications

---

## 9.1 Evolutionary algorithms

Standard evolutionary algorithms evolve a population of candidate solutions using fixed variation operators. Let \(X\) be a search space and \(F:X\to\mathbb{R}\) an objective. A conventional genetic algorithm has the form

\[
x_{t+1}
=
\operatorname{Select}
\left(
\operatorname{Mutate}
\left(
\operatorname{Crossover}(x_t)
\right),
F
\right).
\]

In RME, mutation and crossover operators are themselves organisms. Let

\[
\mu_t
\]

be a population of solutions, and let

\[
\nu_t
\]

be a population of variation operators. A variation operator is a map

\[
V : \mathcal{M}^k \to \mathcal{M}.
\]

The coupled system becomes

\[
\mu_{t+1}
=
T_{\nu_t}(\mu_t),
\tag{9.1}
\]

\[
\nu_{t+1}
=
\widehat T_{\mu_t}(\nu_t).
\tag{9.2}
\]

The fitness of an operator \(V\) may be defined by the improvement it produces:

\[
\varphi_V(V;\mu_t)
=
\mathbb{E}_{m \sim \mu_t}
\left[
F(V(m)) - F(m)
\right].
\tag{9.3}
\]

Thus successful operators reproduce. Operators that fail to generate improvement disappear. This yields a recursive evolutionary algorithm in which the search law evolves with the searched population.

RME generalizes:

- genetic programming,
- evolutionary programming,
- meta-evolutionary algorithms,
- self-adaptive evolution strategies,
- hyper-heuristics,
- coevolutionary learning.

---

## 9.2 Optimization

In optimization, RME treats candidate solutions, search distributions, and heuristics as interacting organisms.

Let \(p_t\) be a probability distribution over candidate solutions. The objective is to maximize

\[
\mathbb{E}_{x\sim p_t}[F(x)].
\]

A nonrecursive estimation-of-distribution algorithm updates

\[
p_{t+1}
=
\operatorname{Project}
\left(
p_t
+
\eta \nabla_p \mathbb{E}_{x\sim p_t}[F(x)]
\right).
\]

In RME, the update rule itself may be an organism. Let \(U\) be an update operator. Then the ecology contains both distributions and update operators.

The recursive equilibrium satisfies

\[
p^*
=
T_{U^*}(p^*),
\tag{9.4}
\]

\[
U^*
=
\Lambda(p^*).
\tag{9.5}
\]

This provides a formal account of adaptive optimization. It also suggests new algorithms in which the optimizer evolves a library of local search operators, global explorers, surrogate models, and proof-based feasibility checkers.

For fixed fitness and symmetric proposal kernels, Proposition 4 shows that Boltzmann selection converges to a maximum-entropy distribution over high-fitness solutions. In recursive RME, the same principle becomes self-referential because the fitness and proposal kernel depend on the evolved operator.

---

## 9.3 Artificial intelligence

RME is particularly relevant to artificial intelligence because modern AI systems increasingly contain interacting learned components.

Examples include populations of:

- neural architectures,
- prompts,
- policies,
- symbolic rules,
- theorem provers,
- program modules,
- world models,
- curricula,
- reward functions,
- data selectors,
- meta-learning rules.

In an RME formulation, an AI system is not a single monolithic model but an ecology of mathematical structures.

For example, let \(\mathcal{M}\) contain both hypotheses \(h\) and experiment-design policies \(\pi\). Hypotheses compete for explanatory power, while policies compete for information gain. The environment includes available data and computational budget.

A hypothesis may have fitness

\[
\varphi(h)
=
\log p(D \mid h)
-
\lambda \operatorname{Complexity}(h).
\]

An experiment policy may have fitness

\[
\varphi(\pi)
=
\mathbb{E}_{h \sim \mu_t}
[
\operatorname{InfoGain}(\pi,h)
].
\]

The recursive operator may modify the hypothesis language itself, allowing the AI system to evolve new representations.

RME therefore provides a formal setting for:

- open-ended learning,
- self-improving agents,
- automated mathematics,
- program synthesis,
- neural architecture search,
- curriculum learning,
- meta-learning,
- population-based training,
- multi-agent coevolution.

---

## 9.4 Complex systems

Complex systems often exhibit emergent organization through interacting heterogeneous components. RME models such systems as populations of mathematical structures whose interactions generate macroscopic regularity.

Let

\[
H(t)
=
-
\sum_i p^i(t)\ln p^i(t)
\]

be the Shannon diversity of the ecology.

For the mutation-free replicator equation,

\[
\dot p^i = p^i(f^i-\bar f),
\]

we have

\[
\dot H
=
-
\sum_i \dot p^i \ln p^i
=
-
\sum_i p^i(f^i-\bar f)\ln p^i.
\tag{9.6}
\]

Thus diversity changes according to the covariance between fitness and surprisal:

\[
\dot H
=
-
\operatorname{Cov}
\left(
f,
\ln p
\right).
\tag{9.7}
\]

Selection can reduce diversity by concentrating probability on high-fitness types, while cooperation, mutation, and niche construction can increase diversity.

RME thus gives a language for studying:

- phase transitions in populations of structures,
- emergence of autocatalytic sets,
- collapse of representational diversity,
- cooperative innovation,
- ecological resilience,
- open-endedness,
- self-organized criticality in symbolic systems.

---

## 10. Illustrative Examples

---

### Example 1: Symbolic expression ecology

Let \(\mathcal{M}\) be the set of symbolic expressions generated from variables, constants, and operators.

An organism \(m\) may be an expression such as

\[
m(x) = \sin(x^2) + \log(1+x).
\]

Fitness for symbolic regression is

\[
\varphi(m)
=
-
\frac{1}{N}
\sum_{k=1}^N
\left(
m(x_k)-y_k
\right)^2
-
\lambda \operatorname{Complexity}(m).
\]

Cooperation occurs when two expressions combine:

\[
C(m_1,m_2)
=
\alpha m_1 + \beta m_2,
\]

or

\[
C(m_1,m_2)
=
m_1 \circ m_2.
\]

Recursive RME allows expressions that encode simplification rules or feature transformations to influence future expression generation.

---

### Example 2: Theorem-proving lemma ecology

Let \(\mathcal{M}\) be a set of lemmas, tactics, and proof sketches.

A lemma organism may be a statement

\[
\ell : P \Rightarrow Q.
\]

A tactic organism may be a function mapping proof states to candidate proof steps.

Fitness of a lemma may combine:

- proof success rate,
- reuse frequency,
- generality,
- proof length reduction.

For a lemma \(\ell\),

\[
\varphi(\ell)
=
w_1 \operatorname{Reuse}(\ell)
+
w_2 \operatorname{Success}(\ell)
-
w_3 \operatorname{ProofCost}(\ell).
\]

A tactic \(T\) has fitness

\[
\varphi(T)
=
\mathbb{E}_{s \sim \text{proof states}}
[
\operatorname{Progress}(T,s)
].
\]

The recursive operator may modify the tactic library, rewrite rule set, or search priority function. Thus a theorem prover can be viewed as a mathematical ecology in which useful lemmas and tactics reproduce, while unproductive ones vanish.

---

### Example 3: Recursive neural architecture search

Let \(\mathcal{M}\) contain neural architectures, training rules, and architecture mutation operators.

An architecture organism \(a\) has fitness equal to validation performance after training:

\[
\varphi(a)
=
\operatorname{ValAcc}(\operatorname{Train}(a))
-
\lambda \operatorname{Cost}(a).
\]

A mutation operator organism \(V\) modifies architectures:

\[
V(a) = a'.
\]

The fitness of \(V\) is

\[
\varphi(V)
=
\mathbb{E}_{a \sim \mu_t}
[
\varphi(V(a))-\varphi(a)
].
\]

The recursive law updates the architecture search operator according to successful operators. This yields a self-modifying architecture search process.

---

## 11. Recursive Niches and Autopoietic Mathematical Systems

A central conceptual contribution of RME is the formalization of **recursive niche construction**.

In classical ecology, niche construction occurs when organisms modify their environment, thereby altering selection pressures. In RME, mathematical organisms may modify not only the environment but also the transition law of the ecology.

We define a recursively constructed niche as a pair

\[
(\mu,L)
\]

such that

\[
L = \bar\Theta(\mu)
\]

and the population \(\mu\) is viable under \(L\).

This leads to an autopoietic interpretation:

\[
\text{organisms} \to \text{operators} \to \text{law} \to \text{organisms}.
\]

A recursively closed mathematical ecology is a system that partially produces its own evolutionary dynamics.

This is not merely metaphorical. In algorithmic terms, it means that the population can encode and select:

- its own mutation kernels,
- its own fitness estimators,
- its own search heuristics,
- its own simplification rules,
- its own proof tactics,
- its own representation spaces.

RME gives this phenomenon a precise dynamical formulation.

---

## 12. Open Problems

The theory of Recursive Mathematical Ecology suggests several open problems.

### 12.1 General existence theory

The fixed-point theorem in Theorem 1 applies to finite-type or compact continuous settings under strong continuity assumptions. A deeper theory is needed for infinite-dimensional object spaces, unbounded fitness, and singular mutation kernels.

### 12.2 Stability of recursive operator dynamics

Equation (5.3) couples population measures to operator dynamics. General Lyapunov theory for such coupled measure-operator systems remains to be developed.

### 12.3 Recursive optimization guarantees

For frequency-independent fitness, Proposition 4 gives a stationary distribution. For recursive frequency-dependent systems, new fixed-point and convergence theorems are required.

### 12.4 Open-endedness criteria

A major question is whether an RME can sustain unbounded growth in complexity, diversity, or capability. Formal open-endedness may be characterized by the absence of absorbing finite attractors and the persistent creation of positive-invasion niches.

### 12.5 Safety and controllability

Recursive self-modification raises control-theoretic questions. One may ask whether the recursive operator map \(\Lambda\) can be constrained to remain within a certified class of operators.

### 12.6 Categorical formulations

RME may be expressible categorically using coalgebras, operads, or recursive domain equations. A categorical theory could clarify compositionality of mathematical organisms.

---

## 13. Conclusion

Recursive Mathematical Ecology provides a formal framework in which mathematical structures behave as ecological populations. By representing populations as measures over object spaces, interactions as tensors and kernels, and evolutionary laws as recursively generated operators, RME unifies evolutionary computation, optimization, AI, and complex systems under a single mathematical theory.

The central insight is that a population of mathematical structures need not evolve under a fixed external law. If some structures encode operators that modify evaluation, variation, or resource dynamics, then the population becomes recursively coupled to its own evolutionary law. The resulting system is a self-consistent ecological universe of mathematical objects.

The framework yields concrete dynamical equations, fixed-point theorems, extinction criteria, stability results, and algorithmic schemas. It also suggests new forms of adaptive computation in which solutions, search operators, representations, and evaluators coevolve.

RME therefore offers both a theoretical language and an algorithmic foundation for studying open-ended mathematical evolution.

---

## References

1. Darwin, C. *On the Origin of Species*. John Murray, 1859.  
2. Lotka, A. J. *Elements of Physical Biology*. Williams & Wilkins, 1925.  
3. Volterra, V. “Variations and Fluctuations of the Number of Individuals in Animal Species Living Together.” *ICES Journal of Marine Science*, 1926.  
4. May, R. M. *Stability and Complexity in Model Ecosystems*. Princeton University Press, 1973.  
5. Holland, J. H. *Adaptation in Natural and Artificial Systems*. University of Michigan Press, 1975.  
6. Kauffman, S. A. *The Origins of Order: Self-Organization and Selection in Evolution*. Oxford University Press, 1993.  
7. Koza, J. R. *Genetic Programming: On the Programming of Computers by Means of Natural Selection*. MIT Press, 1992.  
8. Hofbauer, J., and Sigmund, K. *Evolutionary Games and Population Dynamics*. Cambridge University Press, 1998.  
9. Nowak, M. A. *Evolutionary Dynamics: Exploring the Equations of Life*. Harvard University Press, 2006.  
10. Pelikan, M., Goldberg, D. E., and Lobo, F. G. “A Survey of Optimization by Building and Using Probabilistic Models.” *Computational Optimization and Applications*, 2002.

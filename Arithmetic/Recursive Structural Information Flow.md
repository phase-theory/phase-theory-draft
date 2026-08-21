# Recursive Structural Information Flow

**A Theory of Propagating Informational Structure**

*Preprint*

---

## Abstract

We develop a formal theory of **Recursive Structural Information Flow** (RSIF), in which information flow is treated as a first-class mathematical object propagating through mathematical structures according to recursive flow equations. Rather than regarding information transfer as a derived statistical correlation or a secondary quantity computed after a dynamics has been specified, RSIF promotes flow to a primitive field defined on the structural substrate itself. The theory is formulated on directed graphs, hypergraphs, and categorical path spaces, with local stochastic maps supplying the structural mechanisms by which information is transformed, routed, aggregated, and dissipated. We introduce edge-wise and path-wise flow objects, tensorial transport laws, discrete continuity equations, and fixed-point equations for stationary structural flow. We prove existence and uniqueness of RSIF fields under monotonicity and contraction hypotheses, derive a linear resolvent representation, establish an entropy-balance identity, and give a variational formulation for symmetrizable flows. We also develop a partial-information-decomposition-compatible tensorial refinement capable of separating unique, redundant, and synergistic contributions. Applications are developed to information theory, network science, artificial intelligence, and distributed systems. In each domain, RSIF provides a unified structural account of how information originates, propagates, combines, and constrains global behavior.

**Keywords:** information flow, recursive equations, structural information, transfer entropy, partial information decomposition, graphical models, tensor networks, distributed systems, attention, network centrality.

---

## 1. Introduction

Information is usually treated as a derived quantity. In classical information theory one begins with random variables, probability measures, and channels, and then defines entropy, mutual information, directed information, or transfer entropy as functionals of those objects. In network theory one begins with a graph and a stochastic process on the graph, and then asks whether statistical dependencies imply some notion of influence or communication. In machine learning one begins with an architecture and a training distribution, and then attempts post hoc to infer which parts of the network transmitted relevant information. In distributed systems one begins with messages, replicas, and protocols, and only indirectly reasons about the propagation of knowledge.

This paper develops a different starting point.

We propose that **information flow itself should be treated as a primary structural field**, governed by recursive equations determined by the architecture through which it moves. The central object of the theory is not merely the entropy of a random variable, nor the mutual information between two variables, but a flow field

\[
F = \{F_e\}_{e\in E}
\]

defined over the edges, hyperedges, or morphisms of a structural substrate. The value \(F_e\) is the amount, type, or tensorial content of information carried by the structural element \(e\). The field is not simply computed from correlations after the fact; it is defined recursively by local structural transport laws.

The core principle of **Recursive Structural Information Flow** is:

\[
\boxed{
\text{Information propagates through structure according to recursive flow equations.}
}
\]

This principle has several consequences.

1. **Flow is first-class.** Information flow is represented by its own mathematical object: a scalar, vector, tensor, measure on paths, or section of an information bundle.

2. **Structure determines transport.** The graph, hypergraph, category, or computational architecture supplies the admissible routes and transformations of flow.

3. **Recursion captures indirect propagation.** Information carried by one structural element can be transformed and forwarded into subsequent elements. The total flow is therefore a fixed point of a recursive transport operator.

4. **Entropy and information theory are recovered as constraints.** Shannon entropy, conditional mutual information, transfer entropy, and data-processing inequalities appear as balance laws, constitutive constraints, or local sources of the flow field.

5. **The theory is multi-domain.** The same formalism applies to communication channels, biological and social networks, neural networks, transformers, consensus protocols, replication schemes, and distributed state machines.

The purpose of this paper is to give a rigorous foundation for RSIF, to derive its main analytical properties, and to show how it unifies several seemingly distinct notions of information propagation.

---

## 2. Structural Substrates and Information Primitives

### 2.1 Directed structural substrates

Let

\[
G=(V,E)
\]

be a finite directed graph. The vertex set \(V\) represents structural sites: processors, neurons, agents, variables, services, replicas, or subsystems. The edge set \(E\) represents directed structural relations: channels, dependencies, transformations, messages, attention links, or causal influences.

For an edge \(e\in E\), write

\[
\partial^- e \in V
\]

for its tail and

\[
\partial^+ e \in V
\]

for its head. Thus \(e:\partial^- e\to \partial^+ e\). We define the predecessor set of an edge \(f\) by

\[
\operatorname{Pred}(f)
=
\{e\in E:\partial^+ e=\partial^- f\}.
\]

Equivalently, \(e\in\operatorname{Pred}(f)\) means that \(e\) enters the node from which \(f\) exits. We write \(e\prec f\) when \(e\in\operatorname{Pred}(f)\).

For a vertex \(v\in V\), define

\[
\operatorname{In}(v)=\{e\in E:\partial^+e=v\},
\]

\[
\operatorname{Out}(v)=\{e\in E:\partial^-e=v\}.
\]

The theory extends naturally to directed hypergraphs, where an edge may have multiple inputs and multiple outputs. In that case one replaces \(\partial^-e\) by an input set \(\partial^-e\subseteq V\) and \(\partial^+e\) by an output set \(\partial^+e\subseteq V\). For clarity we primarily develop the ordinary directed-edge case and indicate hypergraph extensions when needed.

---

### 2.2 State spaces and stochastic structural maps

For each vertex \(v\in V\), let \(X_v\) be a measurable state space. In the finite discrete case, \(X_v\) is a finite alphabet. For stochastic processes we write \(X_v^t\) for the state of vertex \(v\) at discrete time \(t\).

Let \(\operatorname{Pa}(v)\subseteq V\) denote the structural parents of \(v\):

\[
\operatorname{Pa}(v)=\{u\in V:(u,v)\in E\}.
\]

A structural stochastic model assigns to each vertex \(v\) a transition kernel

\[
K_v:
\prod_{u\in\operatorname{Pa}(v)} X_u
\longrightarrow
\Delta(X_v),
\]

where \(\Delta(X_v)\) denotes probability measures on \(X_v\). Equivalently, the conditional law of \(X_v^{t+1}\) given the past is determined by the parents:

\[
\mathbb{P}\left(
X_v^{t+1}\mid X_V^t
\right)
=
K_v\left(\cdot\mid X_{\operatorname{Pa}(v)}^t\right).
\]

When self-loops are present, one includes \(X_v^t\) among the conditioning variables. More generally, we may write

\[
X_v^{t+1}
=
\phi_v\left(
X_{\operatorname{Pa}(v)}^t,
N_v^t
\right),
\]

where \(N_v^t\) is an innovation or noise variable. This representation will be useful for separating inherited information from locally generated information.

---

### 2.3 Entropy and local information transfer

Let \(H(\cdot)\) denote Shannon entropy, measured in bits unless otherwise stated. For random variables \(Y,Z\), write

\[
I(Y;Z)
\]

for mutual information and

\[
I(Y;Z\mid W)
\]

for conditional mutual information.

For a vertex \(v\), define the one-step entropy rate

\[
h_v
=
H\left(X_v^{t+1}\mid X_v^t\right).
\]

Define the local noise entropy

\[
\eta_v
=
H\left(
X_v^{t+1}
\mid
X_v^t,
X_{\operatorname{Pa}(v)}^t
\right),
\]

and the incoming structural information

\[
J_v
=
I\left(
X_v^{t+1};
X_{\operatorname{Pa}(v)}^t
\mid
X_v^t
\right).
\]

By the chain rule for conditional mutual information,

\[
\begin{aligned}
h_v
&=
H\left(X_v^{t+1}\mid X_v^t\right) \\
&=
H\left(
X_v^{t+1}
\mid
X_v^t,
X_{\operatorname{Pa}(v)}^t
\right)
+
I\left(
X_v^{t+1};
X_{\operatorname{Pa}(v)}^t
\mid
X_v^t
\right) \\
&=
\eta_v+J_v.
\end{aligned}
\]

Thus the local predictive uncertainty of \(X_v^{t+1}\) splits into irreducible local noise and information supplied by the structural parents.

For an individual edge \(e=(u,v)\), a natural local transfer quantity is the edge-conditioned transfer information

\[
J_e
=
I\left(
X_v^{t+1};
X_u^t
\mid
X_v^t,
X_{\operatorname{Pa}(v)\setminus\{u\}}^t
\right).
\]

This is a conditional mutual information term measuring the information that the parent \(u\) provides about the next state of \(v\), beyond the other parents and the current state of \(v\). It is closely related to transfer entropy, but localized to the structural edge.

However, \(J_e\) is only a local transfer term. It does not yet describe the total information carried by \(e\) through the entire downstream structure. RSIF is concerned with precisely this stronger object.

---

## 3. Recursive Structural Information Flow Fields

### 3.1 Edge flows as first-class objects

Let \(\mathcal{E}\) denote the space of edge flows. In the scalar case,

\[
\mathcal{E}=\mathbb{R}_{\ge 0}^{E}.
\]

A scalar RSIF field is a vector

\[
F=(F_e)_{e\in E},
\]

where \(F_e\) is the total structural information carried by edge \(e\), including information generated upstream and recursively transmitted through \(e\).

The distinction between local transfer and total flow is essential.

- \(J_e\) is the information locally transferred across \(e\).
- \(F_e\) is the total information routed through \(e\) by the recursive structure.

For example, in a chain

\[
A\to B\to C,
\]

the edge \(B\to C\) may carry not only information generated at \(B\), but also information originally generated at \(A\) and forwarded through \(B\). RSIF treats the latter as part of the flow on \(B\to C\).

---

### 3.2 Source terms

Let \(N_v^t\) denote the intrinsic innovation at vertex \(v\). Information that originates at \(v\) and is transmitted along an outgoing edge \(f=(v,w)\) is represented by a source term

\[
S_f
=
I\left(
X_w^{t+1};
N_v^t
\mid
X_{\operatorname{Pa}(w)\setminus\{v\}}^t,
X_v^t
\right).
\]

Thus \(S_f\) is the portion of flow on \(f\) that is locally generated at the tail of \(f\), rather than inherited from incoming edges.

In deterministic systems without local innovation, source terms may vanish except at external inputs. In stochastic systems, noise may act either as entropy production or as a source of new informational content, depending on the modeling convention.

---

### 3.3 Transport operators

For each pair \(e\prec f\), let

\[
\mathcal{T}_{fe}:\mathbb{R}_{\ge 0}\to\mathbb{R}_{\ge 0}
\]

be a transport operator mapping flow on \(e\) into the contribution carried forward onto \(f\). In the simplest scalar linear case,

\[
\mathcal{T}_{fe}(x)=a_{fe}x,
\]

with \(a_{fe}\ge 0\). The coefficient \(a_{fe}\) is the structural transmissivity from \(e\) to \(f\).

A fundamental constraint is data processing. If flow on \(e\) is transformed into flow on \(f\) through a structural channel, then the transmitted information cannot exceed the input flow. Thus we impose

\[
0\le \mathcal{T}_{fe}(x)\le x.
\]

More generally, if \(f\) has finite information capacity \(C_f\), we require

\[
0\le \mathcal{T}_{fe}(x)\le \min\{x,C_f\}.
\]

These inequalities are the RSIF analogues of the data-processing inequality.

---

### 3.4 The recursive flow equation

The scalar RSIF equation is

\[
\boxed{
F_f
=
S_f
+
\sum_{e\prec f}
\mathcal{T}_{fe}(F_e).
}
\tag{3.1}
\]

Equation (3.1) says that the total flow on an edge \(f\) is the sum of:

1. information newly generated at the tail of \(f\);
2. information inherited from all predecessor edges and transformed by the local structural transport maps.

In time-indexed form,

\[
F_f^{(n+1)}
=
S_f^{(n)}
+
\sum_{e\prec f}
\mathcal{T}_{fe}^{(n)}\left(F_e^{(n)}\right).
\tag{3.2}
\]

The stationary RSIF field is a fixed point of the recursive operator

\[
\Phi(F)_f
=
S_f
+
\sum_{e\prec f}
\mathcal{T}_{fe}(F_e).
\]

Thus

\[
F=\Phi(F).
\tag{3.3}
\]

This fixed point is the central object of the theory.

---

### 3.5 Linear RSIF

In the linear case,

\[
\mathcal{T}_{fe}(F_e)=a_{fe}F_e,
\]

with \(a_{fe}\in[0,1]\). Define the nonnegative matrix \(A\in\mathbb{R}_{\ge 0}^{E\times E}\) by

\[
A_{fe}
=
\begin{cases}
a_{fe}, & e\prec f,\\
0, & \text{otherwise}.
\end{cases}
\]

Then

\[
F=S+AF.
\tag{3.4}
\]

If the spectral radius satisfies

\[
\rho(A)<1,
\]

then

\[
F=(I-A)^{-1}S.
\tag{3.5}
\]

Expanding the resolvent,

\[
F
=
\sum_{k=0}^{\infty}A^k S.
\tag{3.6}
\]

The term \(A^kS\) is the information that has traversed exactly \(k\) structural transitions. Thus the RSIF field decomposes naturally into path contributions.

---

### 3.6 Path-space formulation

Let \(\mathcal{P}\) be the set of finite directed paths in \(G\). A path is a sequence

\[
\pi=(e_1,e_2,\dots,e_k)
\]

such that

\[
\partial^+ e_i=\partial^- e_{i+1}
\]

for all \(i=1,\dots,k-1\).

In the linear case, define the path flow

\[
\rho(\pi)
=
S_{e_1}
\prod_{i=2}^{k}
a_{e_i e_{i-1}}.
\tag{3.7}
\]

Then the edge flow is the marginalization over paths ending at that edge:

\[
F_f
=
\sum_{\pi\in\mathcal{P}:\,\operatorname{last}(\pi)=f}
\rho(\pi).
\tag{3.8}
\]

More generally, one may define a path measure \(\rho\) recursively by

\[
\rho(\pi f)
=
\rho(\pi)\tau_f(\pi),
\tag{3.9}
\]

where \(\tau_f(\pi)\in[0,1]\) is the transmissivity of appending edge \(f\) to path \(\pi\). This gives a measure-theoretic formulation of RSIF on the path category of the graph.

The path-space view makes precise the statement that information flow is a structural propagation phenomenon rather than a pairwise correlation.

---

## 4. Tensorial RSIF

Scalar flows are often insufficient. In realistic structures, information has type: feature dimension, semantic channel, logical variable, tensor component, modality, or protocol field. RSIF therefore admits a tensorial formulation.

### 4.1 Information bundles

Assign to each edge \(e\) a finite-dimensional vector space \(W_e\). The collection

\[
\mathcal{W}=\{W_e\}_{e\in E}
\]

is an information bundle over the structural substrate. A tensorial flow field is a section

\[
\mathbf{F}
=
(\mathbf{F}_e)_{e\in E},
\qquad
\mathbf{F}_e\in W_e.
\]

A scalar information value is obtained by contracting with a positive covector

\[
\omega_e\in W_e^*,
\]

so that

\[
|\mathbf{F}_e|
=
\omega_e(\mathbf{F}_e).
\]

The covector \(\omega_e\) defines the measurement functional that converts typed informational content into a scalar amount.

---

### 4.2 Linear tensor transport

For each \(e\prec f\), let

\[
\mathsf{K}_{fe}:W_e\to W_f
\]

be a linear transport tensor. In components,

\[
(\mathsf{K}_{fe})^{\alpha}{}_{\beta}
\]

maps a component \(\beta\) of the incoming flow to a component \(\alpha\) of the outgoing flow.

The linear tensorial RSIF equation is

\[
\boxed{
\mathbf{F}_f
=
\mathbf{S}_f
+
\sum_{e\prec f}
\mathsf{K}_{fe}\mathbf{F}_e.
}
\tag{4.1}
\]

In index notation,

\[
F_f^{\alpha}
=
S_f^{\alpha}
+
\sum_{e\prec f}
(\mathsf{K}_{fe})^{\alpha}{}_{\beta}
F_e^{\beta}.
\tag{4.2}
\]

Einstein summation over repeated indices is understood when convenient.

Data processing is expressed by the contraction inequality

\[
\omega_f\mathsf{K}_{fe}
\le
\omega_e,
\tag{4.3}
\]

meaning that the scalar information after transport cannot exceed the scalar information before transport.

---

### 4.3 Nonlinear and synergistic transport

Information can combine synergistically. Two incoming flows may jointly produce more outgoing information than either carries separately. To model this, introduce higher-order transport tensors

\[
\mathsf{K}_{fe_1e_2}:W_{e_1}\otimes W_{e_2}\to W_f,
\]

and more generally

\[
\mathsf{K}_{fe_1\dots e_m}:
W_{e_1}\otimes\dots\otimes W_{e_m}
\to
W_f.
\]

The nonlinear RSIF equation is

\[
\boxed{
\begin{aligned}
\mathbf{F}_f
&=
\mathbf{S}_f
+
\sum_{e\prec f}
\mathsf{K}_{fe}\mathbf{F}_e \\
&\quad
+
\sum_{e_1,e_2\prec f}
\mathsf{K}_{fe_1e_2}
(\mathbf{F}_{e_1},\mathbf{F}_{e_2}) \\
&\quad
+
\sum_{m\ge 3}
\sum_{e_1,\dots,e_m\prec f}
\mathsf{K}_{fe_1\dots e_m}
(\mathbf{F}_{e_1},\dots,\mathbf{F}_{e_m}).
\end{aligned}
}
\tag{4.4}
\]

In components,

\[
\begin{aligned}
F_f^{\alpha}
&=
S_f^{\alpha}
+
K_{fe}^{\alpha}{}_{\beta}F_e^{\beta} \\
&\quad
+
K_{fe_1e_2}^{\alpha}{}_{\beta\gamma}
F_{e_1}^{\beta}F_{e_2}^{\gamma} \\
&\quad
+
K_{fe_1\dots e_m}^{\alpha}{}_{\beta_1\dots\beta_m}
F_{e_1}^{\beta_1}\cdots F_{e_m}^{\beta_m}.
\end{aligned}
\tag{4.5}
\]

The quadratic and higher-order terms encode synergistic information generation. They are essential for modeling systems in which information is not merely routed but computed.

---

## 5. Discrete Continuity and Information Conservation

Let \(|\mathbf{F}_e|=\omega_e(\mathbf{F}_e)\) be the scalar information carried by edge \(e\). Define the structural divergence at a vertex \(v\) by

\[
\delta F(v)
=
\sum_{e\in\operatorname{Out}(v)}
|\mathbf{F}_e|
-
\sum_{e\in\operatorname{In}(v)}
|\mathbf{F}_e|.
\tag{5.1}
\]

Let \(g_v\) denote information generated at \(v\), and let \(d_v\) denote information dissipated, erased, or lost to inaccessible noise at \(v\). Then RSIF satisfies the discrete continuity equation

\[
\boxed{
\delta F(v)=g_v-d_v.
}
\tag{5.2}
\]

Equivalently,

\[
\sum_{e\in\operatorname{Out}(v)}
|\mathbf{F}_e|
=
\sum_{e\in\operatorname{In}(v)}
|\mathbf{F}_e|
+
g_v
-
d_v.
\tag{5.3}
\]

This is the information-theoretic analogue of a conservation law. In lossless routing, \(d_v=0\). In purely dissipative nodes, \(g_v=0\). In computational nodes, both generation and dissipation may be present.

Using the incidence matrix \(B\in\mathbb{R}^{V\times E}\), defined by

\[
B_{ve}
=
\begin{cases}
-1, & \partial^-e=v,\\
1, & \partial^+e=v,\\
0, & \text{otherwise},
\end{cases}
\]

the net inflow is

\[
(B|F|)_v
=
\sum_{e\in\operatorname{In}(v)}|F_e|
-
\sum_{e\in\operatorname{Out}(v)}|F_e|.
\]

Thus

\[
-B|F|=g-d.
\tag{5.4}
\]

Equation (5.4) is the global balance law of RSIF.

---

## 6. Entropy Balance and Local Information Accounting

Let us connect RSIF to Shannon information more explicitly.

For each vertex \(v\), recall

\[
h_v
=
H(X_v^{t+1}\mid X_v^t),
\]

\[
\eta_v
=
H(X_v^{t+1}\mid X_v^t,X_{\operatorname{Pa}(v)}^t),
\]

\[
J_v
=
I(X_v^{t+1};X_{\operatorname{Pa}(v)}^t\mid X_v^t).
\]

Then

\[
h_v=\eta_v+J_v.
\tag{6.1}
\]

Suppose the incoming information \(J_v\) is decomposed into edge-wise contributions

\[
J_v
=
\sum_{e\in\operatorname{In}(v)}
F_e^{\mathrm{dir}}
+
R_v^{\mathrm{red}}
+
S_v^{\mathrm{syn}},
\tag{6.2}
\]

where:

- \(F_e^{\mathrm{dir}}\) is the unique contribution from edge \(e\);
- \(R_v^{\mathrm{red}}\) is redundant information supplied by multiple parents;
- \(S_v^{\mathrm{syn}}\) is synergistic information supplied only by combinations of parents.

A choice of partial information decomposition makes (6.2) precise. Under such a decomposition, the direct edge terms become local sources for outgoing recursive flows.

Summing (6.1) over all vertices gives

\[
\sum_{v\in V}h_v
=
\sum_{v\in V}\eta_v
+
\sum_{v\in V}J_v.
\tag{6.3}
\]

If the decomposition of \(J_v\) is edge-resolved, then

\[
\sum_{v\in V}J_v
=
\sum_{e\in E}F_e^{\mathrm{dir}}
+
\sum_{v\in V}R_v^{\mathrm{red}}
+
\sum_{v\in V}S_v^{\mathrm{syn}}.
\tag{6.4}
\]

Equations (6.3) and (6.4) show that RSIF does not replace Shannon theory; it refines it by assigning information to structural routes.

---

## 7. Existence, Uniqueness, and Stability

We now establish basic analytical properties of RSIF fields.

Let

\[
\Phi:\mathbb{R}_{\ge 0}^{E}\to\mathbb{R}_{\ge 0}^{E}
\]

be the RSIF operator

\[
\Phi(F)_f
=
S_f+
\sum_{e\prec f}\mathcal{T}_{fe}(F_e).
\]

Assume \(S\ge 0\).

### Theorem 1: Contraction fixed point

Suppose each \(\mathcal{T}_{fe}\) is Lipschitz with constant \(\ell_{fe}\), and suppose there exists a positive weight vector \(w=(w_e)_{e\in E}\) and a constant \(\lambda<1\) such that for every \(f\),

\[
\sum_{e\prec f}\ell_{fe}w_e
\le
\lambda w_f.
\]

Then \(\Phi\) is a contraction in the weighted sup-norm

\[
\|F\|_w
=
\max_{e\in E}\frac{|F_e|}{w_e}.
\]

Therefore \(\Phi\) has a unique fixed point \(F^*\), and the iteration

\[
F^{(n+1)}=\Phi(F^{(n)})
\]

converges to \(F^*\) geometrically.

**Proof.** For \(F,G\ge 0\),

\[
\begin{aligned}
|\Phi(F)_f-\Phi(G)_f|
&\le
\sum_{e\prec f}
|\mathcal{T}_{fe}(F_e)-\mathcal{T}_{fe}(G_e)| \\
&\le
\sum_{e\prec f}
\ell_{fe}|F_e-G_e| \\
&\le
\left(
\sum_{e\prec f}
\ell_{fe}w_e
\right)
\|F-G\|_w \\
&\le
\lambda w_f\|F-G\|_w.
\end{aligned}
\]

Dividing by \(w_f\) and taking the maximum over \(f\) gives

\[
\|\Phi(F)-\Phi(G)\|_w
\le
\lambda\|F-G\|_w.
\]

Since \(\lambda<1\), Banach’s fixed-point theorem applies. \(\square\)

---

### Theorem 2: Linear resolvent

Let \(\mathcal{T}_{fe}(x)=a_{fe}x\) with \(A=(a_{fe})\ge 0\). If

\[
\rho(A)<1,
\]

then the linear RSIF equation

\[
F=S+AF
\]

has the unique nonnegative solution

\[
F^*=(I-A)^{-1}S
=
\sum_{k=0}^{\infty}A^kS.
\]

**Proof.** Since \(\rho(A)<1\), the Neumann series converges:

\[
(I-A)^{-1}=\sum_{k=0}^{\infty}A^k.
\]

Then

\[
(I-A)\sum_{k=0}^{\infty}A^kS
=
S.
\]

Uniqueness follows because if \(F_1,F_2\) solve the equation, then \(F_1-F_2=A(F_1-F_2)\). Since \(1\) is not an eigenvalue of \(A\), \(F_1=F_2\). Nonnegativity follows from \(A,S\ge 0\). \(\square\)

---

### Theorem 3: Monotone iteration and least fixed point

Suppose \(\Phi\) is monotone:

\[
F\le G
\implies
\Phi(F)\le \Phi(G),
\]

and suppose there exists an upper bound \(M\in\mathbb{R}_{\ge 0}^{E}\) such that

\[
\Phi([0,M])\subseteq[0,M].
\]

Then \(\Phi\) has at least one fixed point in \([0,M]\). Moreover, if \(\Phi\) is continuous and the sequence

\[
F^{(0)}=0,
\qquad
F^{(n+1)}=\Phi(F^{(n)})
\]

converges, its limit is the least fixed point of \(\Phi\).

**Proof.** Monotonicity gives

\[
0\le F^{(1)}\le F^{(2)}\le\cdots\le M.
\]

A bounded monotone sequence in \(\mathbb{R}^E\) converges pointwise. If \(\Phi\) is continuous, the limit satisfies \(F=\Phi(F)\). Minimality follows because any fixed point \(G\) satisfies \(0\le G\), hence by induction \(F^{(n)}\le G\) for all \(n\). \(\square\)

This theorem is important when information transport includes saturation, thresholds, or nonlinear synergy, because contraction may fail while monotone boundedness still holds.

---

### Theorem 4: Sufficient condition for finite linear flow

Let \(A\ge 0\). Suppose there exists a positive vector \(w>0\) and \(\lambda<1\) such that

\[
Aw\le \lambda w.
\]

Then

\[
\rho(A)\le \lambda<1.
\]

Hence the linear RSIF field is finite and unique.

**Proof.** This is an immediate consequence of the Collatz–Wielandt characterization of the spectral radius for nonnegative matrices. \(\square\)

A useful interpretation is that the existence of a positive potential \(w\) that strictly decreases along expected flow paths implies global stability.

---

## 8. Variational Formulation

For linear RSIF, one can often obtain a variational principle.

Let

\[
F=S+AF,
\]

with \(A\ge 0\) and \(\rho(A)<1\). Suppose there exists a positive diagonal matrix \(D\) such that

\[
B=D(I-A)
\]

is symmetric positive definite. Define the energy functional

\[
\mathcal{E}(F)
=
\frac12 F^{\top}D(I-A)F
-
F^{\top}DS.
\tag{8.1}
\]

Then

\[
\nabla \mathcal{E}(F)
=
D(I-A)F-DS.
\]

Thus the stationary point satisfies

\[
D(I-A)F=DS,
\]

equivalently,

\[
F=S+AF.
\]

Therefore:

### Theorem 5: RSIF variational principle

If \(D(I-A)\) is symmetric positive definite, the unique RSIF fixed point \(F^*\) is the unique minimizer of \(\mathcal{E}\).

This provides a bridge between RSIF and energy-based formulations, statistical physics, and convex optimization. In nonlinear RSIF, analogous functionals can often be constructed using Legendre transforms of the transport operators, though the resulting principles may be nonconvex when synergistic terms are present.

---

## 9. Partial Information Decomposition and Synergistic Flow

A central difficulty in any theory of information flow is that mutual information does not uniquely decompose among multiple sources. RSIF addresses this using partial information decomposition (PID).

Let \(Y\) be an output variable and let \(X_1,\dots,X_m\) be source variables. A PID assigns nonnegative atoms

\[
I_\alpha(Y;X_1,\dots,X_m)
\]

to information atoms \(\alpha\) in a redundancy lattice, such that

\[
\sum_{\alpha}I_\alpha
=
I(Y;X_1,\dots,X_m).
\]

The atoms separate:

1. **unique information** from a single source;
2. **redundant information** shared by multiple sources;
3. **synergistic information** available only from joint observation of multiple sources.

In RSIF, for a node \(v\) with incoming edges

\[
\operatorname{In}(v)=\{e_1,\dots,e_m\},
\]

and output variable \(Y=X_v^{t+1}\), one applies PID to

\[
I\left(
X_v^{t+1};
X_{\partial^-e_1}^t,\dots,X_{\partial^-e_m}^t
\mid
X_v^t
\right).
\]

The resulting atoms determine how much flow should be assigned to each incoming edge, to redundant combinations, and to synergistic combinations.

For an outgoing edge \(f=(v,w)\), the flow generated by the incoming information atoms is

\[
F_f
=
S_f
+
\sum_{\alpha}
\lambda_{\alpha\to f} I_\alpha,
\tag{9.1}
\]

where \(\lambda_{\alpha\to f}\) is the routing coefficient of atom \(\alpha\) into edge \(f\).

Unique atoms produce linear transport terms. Redundant atoms produce allocation ambiguities that must be resolved by a chosen PID rule. Synergistic atoms produce higher-order tensor transport terms of the form

\[
K_{fe_i e_j}^{\alpha}{}_{\beta\gamma}
F_{e_i}^{\beta}F_{e_j}^{\gamma}.
\]

Thus the nonlinear tensorial RSIF equation is the natural flow-theoretic expression of partial information decomposition.

---

## 10. A Solvable Model: Linear-Gaussian Structural Flow

To illustrate the formalism, consider a linear-Gaussian structural system.

Let \(x_t\in\mathbb{R}^n\) satisfy

\[
x_{t+1}=Ax_t+\xi_t,
\]

where

\[
\xi_t\sim\mathcal{N}(0,Q),
\]

and \(Q\) is positive definite. If \(\rho(A)<1\), the stationary covariance \(\Sigma\) solves the discrete Lyapunov equation

\[
\Sigma=A\Sigma A^{\top}+Q.
\tag{10.1}
\]

For Gaussian variables, conditional mutual informations are expressible through log-determinants. For an edge \(u\to v\), the Gaussian transfer information conditioned on the remaining parents is

\[
J_{u\to v}
=
\frac12
\log
\frac{
\det \Sigma_{v\mid \operatorname{Pa}(v)\setminus\{u\}}
}{
\det \Sigma_{v\mid \operatorname{Pa}(v)}
}.
\tag{10.2}
\]

Here \(\Sigma_{v\mid S}\) denotes the conditional covariance of the next state of \(v\) given the parent subset \(S\).

In the scalar acyclic case,

\[
x_i
=
\sum_{j\in\operatorname{Pa}(i)}a_{ij}x_j
+
\varepsilon_i,
\]

with independent innovations \(\varepsilon_i\) of variance \(q_i\), define the variance flow

\[
f_{j\to i}
=
a_{ij}^2\operatorname{Var}(x_j).
\tag{10.3}
\]

Then

\[
\operatorname{Var}(x_i)
=
q_i+
\sum_{j\in\operatorname{Pa}(i)}
f_{j\to i}.
\tag{10.4}
\]

Since

\[
\operatorname{Var}(x_j)
=
q_j+
\sum_{k\in\operatorname{Pa}(j)}
f_{k\to j},
\]

we obtain

\[
\boxed{
f_{j\to i}
=
a_{ij}^2q_j
+
\sum_{k\in\operatorname{Pa}(j)}
a_{ij}^2f_{k\to j}.
}
\tag{10.5}
\]

This is exactly a linear RSIF equation with source

\[
s_{j\to i}=a_{ij}^2q_j
\]

and transmissivity

\[
a_{(j\to i),(k\to j)}=a_{ij}^2.
\]

In the multivariate case, let \(x_i\in\mathbb{R}^{d_i}\), and let the structural equation be

\[
x_i
=
\sum_{j\in\operatorname{Pa}(i)}A_{ij}x_j
+
\varepsilon_i,
\]

with

\[
\operatorname{Cov}(\varepsilon_i)=Q_i.
\]

Define the covariance flow tensor from \(j\) to \(i\) by

\[
\mathcal{F}_{j\to i}^{ab}
=
A_{ij}^{a c}
\Sigma_j^{c d}
A_{ij}^{b d},
\tag{10.6}
\]

where repeated indices are summed. Then

\[
\Sigma_i^{ab}
=
Q_i^{ab}
+
\sum_{j\in\operatorname{Pa}(i)}
\mathcal{F}_{j\to i}^{ab}.
\tag{10.7}
\]

Equation (10.7) is a tensorial RSIF balance law. The scalar Gaussian information associated with a flow tensor can be obtained by log-determinant contractions of the form (10.2).

---

## 11. Feedback and Recursive Amplification

RSIF is especially useful in cyclic structures, where ordinary path decompositions fail without additional assumptions.

Consider two vertices \(1,2\) with edges

\[
e:1\to 2,
\qquad
f:2\to 1.
\]

Let the linear RSIF equations be

\[
F_e=s_e+a_{ef}F_f,
\]

\[
F_f=s_f+a_{fe}F_e.
\]

In matrix form,

\[
\begin{pmatrix}
F_e\\
F_f
\end{pmatrix}
=
\begin{pmatrix}
s_e\\
s_f
\end{pmatrix}
+
\begin{pmatrix}
0 & a_{ef}\\
a_{fe} & 0
\end{pmatrix}
\begin{pmatrix}
F_e\\
F_f
\end{pmatrix}.
\]

If

\[
a_{ef}a_{fe}<1,
\]

then

\[
F_e
=
\frac{s_e+a_{ef}s_f}{1-a_{ef}a_{fe}},
\]

\[
F_f
=
\frac{s_f+a_{fe}s_e}{1-a_{ef}a_{fe}}.
\]

The denominator exhibits recursive amplification. Feedback increases total structural flow when the cycle gain is positive but less than one. If the cycle gain approaches one, the system becomes informationally critical. If it exceeds one, the unconstrained linear model diverges, indicating the need for saturation, dissipation, or capacity constraints.

This behavior is structurally analogous to:

- reverberating neural circuits;
- retry loops in distributed protocols;
- feedback in control systems;
- recursive attention in transformers;
- rumor amplification in social networks.

RSIF gives a precise algebraic account of such amplification.

---

## 12. Computational Methods

### 12.1 Fixed-point iteration

The simplest algorithm for nonlinear RSIF is Picard iteration.

```
Input: source field S, transport operators T_fe, tolerance ε.
Initialize F_e^(0) = 0 or S_e.
Repeat:
    For each edge f:
        F_f^(n+1) = S_f + Σ_{e≺f} T_fe(F_e^(n))
    Stop if ||F^(n+1) - F^(n)|| < ε.
Output: F^(n+1).
```

If \(\Phi\) is a contraction, convergence is geometric.

---

### 12.2 Linear solution

For linear RSIF,

\[
F=S+AF,
\]

one may compute

\[
F=(I-A)^{-1}S
\]

directly if \(|E|\) is small, or iteratively using:

- Jacobi iteration;
- Gauss–Seidel iteration;
- conjugate gradients on the symmetrized system;
- GMRES for nonsymmetric systems;
- Neumann series truncation when \(\rho(A)\ll 1\).

---

### 12.3 Tensor contraction

For tensorial RSIF,

\[
F_f^{\alpha}
=
S_f^{\alpha}
+
K_{fe}^{\alpha}{}_{\beta}F_e^{\beta}
+
K_{fe_1e_2}^{\alpha}{}_{\beta\gamma}
F_{e_1}^{\beta}F_{e_2}^{\gamma}
+\cdots,
\]

the computational cost depends on tensor rank. In practice one uses:

- low-rank tensor decomposition;
- matrix product states;
- Tucker or tensor-train approximations;
- Monte Carlo path sampling;
- automatic differentiation for learned transport tensors.

---

### 12.4 Differentiable RSIF

If the transport tensors are parameterized by learnable parameters \(\theta\),

\[
K=K_\theta,
\]

then the fixed point \(F_\theta\) can be differentiated using implicit differentiation.

From

\[
F_\theta=S+K_\theta(F_\theta),
\]

we obtain

\[
(I-\partial_F K_\theta)\frac{\partial F_\theta}{\partial\theta}
=
\frac{\partial K_\theta}{\partial\theta}.
\]

Thus RSIF can be embedded as a differentiable layer inside machine-learning architectures.

---

## 13. Applications to Information Theory

RSIF refines several classical information quantities.

### 13.1 Directed information

Directed information from \(X^n\) to \(Y^n\) is

\[
I(X^n\to Y^n)
=
\sum_{t=1}^n
I(X^t;Y_t\mid Y^{t-1}).
\]

RSIF decomposes directed information into structural routes. Rather than assigning a single scalar to a pair of processes, RSIF asks which structural edges carried which portions of the directed information.

---

### 13.2 Transfer entropy

Transfer entropy from \(u\) to \(v\) is

\[
T_{u\to v}
=
I\left(
X_v^{t+1};
X_u^t
\mid
X_v^{t-},
X_{\operatorname{Pa}(v)\setminus u}^t
\right).
\]

This is a local edge quantity. RSIF extends it by defining the total downstream influence of \(u\) through \(v\), recursively propagated over all structural continuations.

Thus RSIF distinguishes:

- direct transfer;
- indirect transfer;
- redundant transfer;
- synergistic transfer;
- recirculated transfer.

---

### 13.3 Data processing

For any structural path

\[
\pi=e_1\dots e_k,
\]

the path transmissivity satisfies

\[
\tau_\pi
=
\prod_{i=2}^k
\tau_{e_i}(\pi_{<i})
\le 1.
\]

Therefore information cannot increase along a passive chain. This is the path-space version of the data-processing inequality.

---

### 13.4 Information capacity

If each edge \(e\) has capacity \(C_e\), RSIF can be constrained by

\[
0\le F_e\le C_e.
\]

The maximal feasible flow becomes a network coding problem with recursive structural constraints. RSIF therefore connects information theory with structural routing.

---

## 14. Applications to Network Science

### 14.1 Flow centrality

Define the RSIF centrality of a vertex \(v\) by

\[
C_{\mathrm{RSIF}}(v)
=
\sum_{e\in\operatorname{In}(v)}F_e
+
\sum_{e\in\operatorname{Out}(v)}F_e.
\]

Alternatively, one may use the path-through flow

\[
B(v)
=
\sum_{\pi\ni v}\rho(\pi),
\]

which generalizes betweenness centrality by weighting paths according to information flow rather than mere shortest-path counts.

---

### 14.2 Edge importance

The importance of an edge \(e\) is its total flow \(F_e\). In the linear case, removing edge \(e\) corresponds to setting to zero all transport coefficients entering or leaving \(e\). Let \(A'\) be the modified matrix. The flow perturbation is

\[
\Delta F
=
(I-A')^{-1}S
-
(I-A)^{-1}S.
\]

For small perturbations,

\[
\Delta F
\approx
-(I-A)^{-1}(\Delta A)F^*.
\]

This gives a principled sensitivity analysis.

---

### 14.3 Bottlenecks and cuts

For a cut \(U\subset V\), define the cut flow

\[
F(U)
=
\sum_{e:\partial^-e\in U,\ \partial^+e\notin U}F_e.
\]

RSIF cut capacities generalize max-flow min-cut ideas to recursive, information-theoretic settings. Unlike classical flow, RSIF flow may be nonlinear, synergistic, and lossy, so cut inequalities become constraints on transport operators rather than simple additive capacities.

---

### 14.4 Robustness

A network is informationally robust if the RSIF field remains close to its original value under edge deletions or transmissivity perturbations. A natural robustness modulus is

\[
\mathcal{R}
=
\inf_{\Delta A}
\left\{
\|\Delta A\|:
\rho(A+\Delta A)\ge 1
\right\}.
\]

This measures the smallest structural perturbation that drives the information dynamics into divergence or criticality.

---

## 15. Applications to Artificial Intelligence

RSIF is particularly natural for modern machine-learning systems, where architecture defines a directed computational graph and information must be routed through layers, attention heads, residual streams, and modules.

### 15.1 Deep networks

Let \(h_i^{(\ell)}\) denote the activation of unit or token \(i\) at layer \(\ell\). A feedforward layer defines edges

\[
(i,\ell)\to(j,\ell+1).
\]

An RSIF flow field assigns to each such edge the information transmitted from unit \(i\) at layer \(\ell\) to unit \(j\) at layer \(\ell+1\).

For a linearized layer with weight matrix \(W^{(\ell)}\),

\[
F_{j\leftarrow i}^{(\ell+1)}
=
S_{j\leftarrow i}^{(\ell+1)}
+
\sum_{k}
K_{j i,k}^{(\ell+1)}
F_{k\leftarrow i}^{(\ell)}.
\]

In tensor form,

\[
\mathbf{F}_{j}^{(\ell+1)}
=
\mathbf{S}_{j}^{(\ell+1)}
+
\sum_i
\mathsf{K}_{ji}^{(\ell+1)}
\mathbf{F}_{i}^{(\ell)}.
\]

This permits layer-wise accounting of which input features survive, merge, or disappear.

---

### 15.2 Transformers

In a transformer layer, the representation of token \(j\) is updated by attention over tokens \(i\). Let

\[
\alpha_{ji}^{(\ell)}
\]

be the attention weight from query \(j\) to key \(i\) at layer \(\ell\). Let \(W_V^{(\ell)}\) be the value projection. A natural attention transport tensor is

\[
\mathsf{K}_{ji}^{(\ell)}
=
\alpha_{ji}^{(\ell)}W_V^{(\ell)}.
\]

Then the RSIF recursion for the residual stream can be written schematically as

\[
\mathbf{F}_{j}^{(\ell+1)}
=
\mathbf{F}_{j}^{(\ell)}
+
\sum_i
\alpha_{ji}^{(\ell)}
W_V^{(\ell)}
\mathbf{F}_{i}^{(\ell)}
+
\mathbf{M}_{j}^{(\ell+1)},
\]

where \(\mathbf{M}_{j}^{(\ell+1)}\) is the contribution from the MLP block.

In components,

\[
F_{j}^{(\ell+1),a}
=
F_{j}^{(\ell),a}
+
\alpha_{ji}^{(\ell)}
(W_V^{(\ell)})^{a}{}_{b}
F_{i}^{(\ell),b}
+
M_{j}^{(\ell+1),a}.
\]

This gives a recursive account of how information from one token propagates into another across layers.

RSIF can therefore be used to define:

- attention path importance;
- circuit discovery scores;
- token-level information attribution;
- layer-wise redundancy and synergy;
- representational bottlenecks.

---

### 15.3 Credit assignment

Standard backpropagation assigns gradients through differentiable maps. RSIF assigns information flow through structural maps. The two are related but distinct.

For a loss \(\mathcal{L}\), define the informational relevance of edge \(e\) by

\[
R_e
=
F_e\cdot
\left|
\frac{\partial \mathcal{L}}{\partial F_e}
\right|.
\]

This combines structural transmission with task relevance. It yields an information-theoretic credit-assignment mechanism that can operate even when exact gradients are unavailable or when the system contains discrete components.

---

## 16. Applications to Distributed Systems

Distributed systems are inherently structural information processors. Nodes maintain partial views of global state, and messages propagate knowledge across unreliable channels.

### 16.1 Messages as information edges

Let each process \(p\) maintain local state \(S_p^t\). A message from \(p\) to \(q\) defines an edge \(e=(p,q)\). The edge flow is

\[
F_{pq}
=
I\left(
S_q^{t+\Delta};
S_p^t
\mid
\mathcal{H}_q^t
\right),
\]

where \(\mathcal{H}_q^t\) is the history available at \(q\).

RSIF quantifies how much knowledge of one process’s state is transmitted to another through the protocol graph.

---

### 16.2 Consensus and quorums

Consensus protocols often require aggregation from multiple replicas. This is naturally represented by hyperedges.

Let \(Q\subseteq V\) be a quorum. Define a hyperedge

\[
h_Q:Q\to c,
\]

where \(c\) is the committed state. The flow into commitment is

\[
F_{h_Q}
=
I\left(
C;
S_Q
\mid
\mathcal{H}
\right),
\]

where \(C\) is the committed value and \(S_Q\) is the joint state of the quorum.

For majority quorums, the aggregation is nonlinear and threshold-like. In tensorial RSIF, the quorum hyperedge has a higher-order transport tensor that extracts the jointly redundant information required for commitment.

---

### 16.3 Replication

Replication can be modeled as flow duplication. If a primary \(p\) sends state to replicas \(r_1,\dots,r_k\), then

\[
F_{p\to r_i}
=
\tau_i F_p,
\]

with

\[
\sum_i \tau_i\le k
\]

and data-processing constraints. Perfect replication would preserve the same informational content across multiple edges, but physical channels and consistency requirements introduce loss, delay, and redundancy.

---

### 16.4 Partitions and failures

A network partition removes edges. Let \(E'\subseteq E\) be the surviving edge set. The post-partition RSIF field is

\[
F'=
\Phi_{E'}(F').
\]

The informational cost of the partition is

\[
\Delta_{\mathrm{partition}}
=
\|F-F'\|.
\]

This provides a quantitative measure of how much global knowledge is destroyed by a failure.

In the CAP tradeoff, consistency can be interpreted as the maintenance of a high-value commitment flow, availability as the preservation of edge capacities, and partition tolerance as the stability of RSIF under edge removal. RSIF does not eliminate the tradeoff, but it gives it a precise flow-theoretic formulation.

---

### 16.5 Byzantine and noisy channels

Byzantine behavior can be modeled as adversarial corruption of transport operators. A Byzantine edge \(e\) replaces \(\mathcal{T}_{fe}\) by an unreliable operator \(\widetilde{\mathcal{T}}_{fe}\). The resulting flow satisfies

\[
F_f
=
S_f
+
\sum_{e\prec f}
\widetilde{\mathcal{T}}_{fe}(F_e).
\]

Robustness then becomes a question of whether the fixed point remains close to the honest fixed point under operator perturbations.

---

## 17. Categorical Formulation

RSIF can be expressed categorically.

Let \(\mathcal{C}\) be the path category of the directed graph \(G\). Objects are vertices, and morphisms are directed paths. A structural channel assignment is a functor

\[
K:\mathcal{C}\to\mathbf{Stoch},
\]

where \(\mathbf{Stoch}\) is a category of measurable spaces and stochastic maps.

An information valuation is a monotone map

\[
I:\operatorname{Obj}(\mathcal{C})\to\mathbb{R}_{\ge 0}
\]

or, more generally, a functor into an information semiring.

A recursive flow is then a fixed point of a propagation operator on the category of paths. In this language:

- paths are morphisms;
- transport operators are functorial channel compositions;
- recursion is a fixed point over the path category;
- PID atoms are decompositions of information valuations over source lattices.

This categorical view suggests extensions to:

- probabilistic programming semantics;
- Markov categories;
- open systems;
- compositional information theory.

---

## 18. Relation to Existing Concepts

RSIF is related to, but distinct from, several existing frameworks.

### 18.1 Transfer entropy

Transfer entropy measures directed pairwise information transfer. RSIF generalizes transfer entropy by making flow recursive, path-resolved, and structurally typed.

### 18.2 Network flow

Classical network flow concerns conserved scalar commodities. RSIF allows loss, amplification, synergy, and tensorial content, and its flow laws are recursive rather than purely local.

### 18.3 Message passing

Belief propagation passes probability messages on graphs. RSIF passes information-flow objects. The two can be related: message updates induce transport operators, while RSIF tracks the information carried by those messages.

### 18.4 Causal influence

Causal influence measures intervention effects. RSIF is compatible with causal modeling but focuses on informational routing through structure. When structural equations are causal, RSIF flow can be interpreted as path-specific causal information.

---

## 19. Limitations and Open Problems

Several theoretical directions remain open.

1. **Canonical PID extension.** A universally accepted PID for continuous variables remains unsettled. RSIF can accommodate any chosen PID, but canonical choices are desirable.

2. **Infinite graphs.** The present theory assumes finite substrates. Extension to countable or continuous structures requires measure-theoretic fixed-point theory.

3. **Quantum information.** RSIF should be generalized to quantum channels, where entropy is von Neumann entropy and flow tensors may become completely positive maps.

4. **Learning transport operators.** In applied settings, transport tensors must be inferred from data. Statistical consistency and identifiability require further study.

5. **Nonlinear stability.** Synergistic terms can create noncontractive dynamics. A full classification of informational phase transitions is open.

6. **Causal identifiability.** Distinguishing true causal flow from statistical routing requires intervention or structural assumptions.

---

## 20. Conclusion

We have introduced **Recursive Structural Information Flow**, a formal theory in which information flow is a primary structural object governed by recursive equations. The theory assigns flow fields to graphs, hypergraphs, or categorical path spaces, relates them to Shannon entropy and conditional mutual information, and provides fixed-point, tensorial, variational, and path-space formulations.

The central achievement of RSIF is to unify several previously separate ideas:

- transfer entropy becomes local edge transfer;
- directed information becomes structural path accumulation;
- network centrality becomes flow exposure;
- deep-network interpretability becomes recursive tensor attribution;
- distributed consistency becomes quorum-aggregated information routing.

The recursive viewpoint reveals that information is not merely present in variables; it propagates, combines, amplifies, and dissipates through structure. By making this propagation mathematically explicit, RSIF provides a foundation for analyzing and engineering complex informational systems.

---

## Appendix A: Notation

| Symbol | Meaning |
|---|---|
| \(G=(V,E)\) | directed structural graph |
| \(\partial^-e,\partial^+e\) | tail and head of edge \(e\) |
| \(\operatorname{Pred}(f)\) | edges entering the tail of \(f\) |
| \(X_v^t\) | state of vertex \(v\) at time \(t\) |
| \(H(\cdot)\) | Shannon entropy |
| \(I(\cdot;\cdot)\) | mutual information |
| \(J_e\) | local edge transfer information |
| \(S_f\) | local source term on edge \(f\) |
| \(F_f\) | total recursive flow on edge \(f\) |
| \(\mathcal{T}_{fe}\) | transport operator from \(e\) to \(f\) |
| \(A\) | linear transport matrix |
| \(\rho(A)\) | spectral radius of \(A\) |
| \(\mathbf{F}_e\) | tensorial flow on edge \(e\) |
| \(\mathsf{K}_{fe}\) | tensor transport map |
| \(\delta F(v)\) | structural divergence at \(v\) |
| \(g_v,d_v\) | information generation and dissipation at \(v\) |

---

## Appendix B: Proof of the Path Expansion Formula

Assume linear RSIF:

\[
F_f=S_f+\sum_{e\prec f}a_{fe}F_e.
\]

Define path flow for a path \(\pi=(e_1,\dots,e_k)\) by

\[
\rho(\pi)
=
S_{e_1}
\prod_{i=2}^k
a_{e_i e_{i-1}}.
\]

We prove by induction on path length that

\[
F_f
=
\sum_{\pi:\operatorname{last}(\pi)=f}
\rho(\pi).
\]

For length one, the only paths ending at \(f\) are \((f)\), and

\[
\rho((f))=S_f.
\]

Thus the formula gives \(F_f=S_f\) if there are no predecessors, matching the base case.

Assume the formula holds for all paths of length at most \(k\). For edge \(f\),

\[
\begin{aligned}
F_f
&=
S_f+
\sum_{e\prec f}a_{fe}F_e \\
&=
S_f+
\sum_{e\prec f}
a_{fe}
\sum_{\pi:\operatorname{last}(\pi)=e}
\rho(\pi) \\
&=
\sum_{\pi:\operatorname{last}(\pi)=f}
\rho(\pi).
\end{aligned}
\]

The last equality follows because every path ending at \(f\) is either the length-one path \((f)\), contributing \(S_f\), or is obtained by appending \(f\) to a path ending at some predecessor \(e\prec f\), contributing \(a_{fe}\rho(\pi)\). \(\square\)

---

## Appendix C: Proof of the Variational Principle

Let

\[
\mathcal{E}(F)
=
\frac12 F^{\top}D(I-A)F
-
F^{\top}DS,
\]

with \(D\) positive diagonal and \(B=D(I-A)\) symmetric positive definite.

The gradient is

\[
\nabla\mathcal{E}(F)
=
\frac12(B+B^{\top})F-DS.
\]

Since \(B\) is symmetric,

\[
\nabla\mathcal{E}(F)
=
BF-DS.
\]

Setting the gradient to zero gives

\[
BF=DS.
\]

Substituting \(B=D(I-A)\),

\[
D(I-A)F=DS.
\]

Since \(D\) is invertible,

\[
(I-A)F=S,
\]

so

\[
F=S+AF.
\]

Because \(B\) is positive definite, \(\mathcal{E}\) is strictly convex, and the stationary point is the unique global minimizer. \(\square\)

# **Correlation–Causation Compatibility Bound (CCCB)**

## **Quantitative Trade-Off Theorems for Nonlocal Correlation, Causal Response, and Operational Constraints**

**Dust LLC — Research Preprint**

## **Abstract**

The coexistence of strong correlations between spatially separated outcomes and restrictions on causal influence is a central structural feature of modern physical theory. Bell inequalities, Tsirelson bounds, no-signaling constraints, causal models, and network-source independence each characterize different aspects of this relationship. Yet these constraints are usually formulated separately: one bounds the strength of correlations, another restricts signaling, and another constrains the causal architecture that may generate the observed statistics.

We develop the **Correlation–Causation Compatibility Bound (CCCB)** as a general mathematical framework for deriving quantitative trade-offs between a specified correlation strength and a specified measure of causal-response violation. The objective is to determine when a theory can support strong distant correlations while satisfying operational constraints that restrict causal influence.

Let \\(P(\mathbf a|\mathbf x)\\) denote a conditional probability distribution for a multipartite experiment. Let \\(\mathcal N(P)\\) be a correlation-strength functional defined by an explicitly selected Bell or network witness, and let \\(\mathcal V(P)\\) quantify departure from a specified causal-response constraint. Let \\(\mathcal Q\\) encode the assumptions defining the admissible theory class. We seek bounds of the form

\\[ \boxed{ \mathcal N(P) \leq F\bigl(\mathcal V(P),\mathcal Q\bigr). } \\]

The framework distinguishes correlation magnitude, operational signaling, causal-model compatibility, measurement independence, and source independence. These are mathematically different restrictions and cannot be compressed into a single unqualified notion of causality.

A complete analytical treatment is developed for the bipartite binary-input, binary-output scenario. We define a CHSH correlation functional, an operational signaling measure, and derive an exact compatibility bound for nonsignaling correlations. We then derive a second bound under a quantitative relaxation of the no-signaling constraint, and establish the quantum Tsirelson ceiling as an independent restriction. The resulting inequalities demonstrate both the utility and the limitations of the CCCB programme.

The central conclusion is that a meaningful correlation–causation bound is necessarily assumption-relative. A bound that follows from no-signaling alone is not a Bell-locality bound; a quantum bound is not a causal-model bound; and a network-source independence constraint is not equivalent to measurement independence. The research opportunity lies in deriving new sharp trade-off surfaces for operationally distinct causal structures, especially in multipartite networks and sequential experiments.

## **1. Introduction**

### **1.1 The correlation–causation distinction**

Two distant systems may exhibit statistical correlations even when no controllable signal propagates between them.

For two observers, Alice and Bob, let the measurement settings be \\(x,y\\) and outcomes be \\(a,b\\). Their observable statistics are represented by

\\[ P(a,b|x,y). \\]

A causal-response restriction can require that Alice's marginal outcome distribution be independent of Bob's setting:

\\[ P(a|x,y)=P(a|x), \\]

and that Bob's marginal be independent of Alice's setting:

\\[ P(b|x,y)=P(b|y). \\]

These are the bipartite no-signaling conditions.

They do not require the joint distribution to factorize:

\\[ P(a,b|x,y) \neq P(a|x)P(b|y) \\]

in general.

Thus correlation and controllable influence are distinct statistical properties.

Bell's theorem sharpens this distinction. Quantum correlations can violate Bell inequalities while satisfying no-signaling. Consequently, the absence of operational signaling does not imply the existence of a local hidden-variable model.

### **1.2 From qualitative distinction to quantitative compatibility**

The usual formulation separates three questions:

1. How strong are the observed correlations?
2. How much operational signaling or causal-response violation is present?
3. Which theoretical assumptions restrict the admissible distributions?

CCCB unifies these questions into a constrained optimization problem.

For a chosen correlation witness \\(W\\), define

\\[ \mathcal N(P)=W(P). \\]

For a chosen causal-response constraint, define a violation measure

\\[ \mathcal V(P)\geq0, \\]

with \\(\mathcal V(P)=0\\) representing exact compatibility.

The research target is the upper envelope

\\[ F(v,\mathcal Q) = \sup\_{P\in\mathfrak P(\mathcal Q):\\, \mathcal V(P)\leq v} \mathcal N(P), \\]

where \\(\mathfrak P(\mathcal Q)\\) is the set of distributions satisfying the stated theoretical assumptions.

This formulation makes the central objective precise: determine the maximum correlation strength compatible with a prescribed degree of causal-response violation and a fixed assumption set.

### **1.3 Central research question**

The principal question is:

> Given a specified operational causal constraint and a specified physical theory class, what is the maximum correlation strength that remains compatible with those constraints?

This question is more precise than asking whether correlations are “nonlocal” or “causal.” It demands an explicit optimization problem and a sharp extremal theorem.

### **1.4 Scope and epistemic status**

This paper distinguishes:

- **Established results:** Bell inequalities, Tsirelson's bound, no-signaling constraints, causal factorization, and network-source independence.
- **Derived results:** a general CCCB optimization formulation, an exact CHSH–signaling bound for the nonsignaling relaxation, and a quantitative bound for approximate no-signaling.
- **Proposed extensions:** causal-response distances, network CCCB surfaces, and intervention-sensitive correlation witnesses.
- **Open conjectures:** sharp trade-off surfaces under combinations of quantum realizability, measurement dependence, and source dependence.

The inequalities derived below are not presented as new universal laws. They provide a rigorous baseline against which genuinely new CCCB theorems must be measured.

## **2. Mathematical framework**

### **2.1 Bell experiment**

Consider a bipartite Bell experiment with finite setting sets

\\[ x\in\mathcal X,\qquad y\in\mathcal Y \\]

and outcome sets

\\[ a\in\mathcal A,\qquad b\in\mathcal B. \\]

The observed conditional distribution is

\\[ P(a,b|x,y)\geq0, \\]

with normalization

\\[ \sum\_{a,b}P(a,b|x,y)=1 \\]

for every setting pair.

The operational experiment is characterized by the family

\\[ P=\\{P(a,b|x,y)\\}\_{a,b,x,y}. \\]

No assumption of quantum realizability, locality, or measurement independence is implied by this definition.

### **2.2 Correlation strength**

A correlation strength must be defined relative to a chosen witness. There is no unique scalar measure that captures every form of nonlocality.

For binary outcomes \\(a,b\in\\{-1,+1\\}\\), define the correlators

\\[ E\_{xy} = \sum\_{a,b}ab\\,P(a,b|x,y). \\]

The CHSH expression is

\\[ S(P) = E\_{00}+E\_{01}+E\_{10}-E\_{11}. \\]

Because the sign of the expression depends on outcome relabelings and setting choices, define the optimized CHSH strength

\\[ \boxed{ \mathcal N\_{\mathrm{CHSH}}(P) = \max\_{\text{local relabelings}} |S(P)|. } \\]

The standard bounds are

\\[ \mathcal N\_{\mathrm{CHSH}}\leq2 \\]

for Bell-local correlations and

\\[ \mathcal N\_{\mathrm{CHSH}}\leq2\sqrt2 \\]

for quantum correlations.

For general no-signaling correlations,

\\[ \mathcal N\_{\mathrm{CHSH}}\leq4. \\]

The value of \\(\mathcal N\\) therefore depends on the theory class as well as the observed statistics.

### **2.3 General witness formulation**

For a finite Bell scenario, a linear correlation witness has the form

\\[ W(P) = \sum\_{a,b,x,y} c\_{abxy}P(a,b|x,y). \\]

A corresponding CCCB can be written

\\[ \boxed{ W(P) \leq F_W\bigl(\mathcal V(P),\mathcal Q\bigr). } \\]

Different choices of coefficients \\(c\_{abxy}\\) detect different correlation structures.

A complete CCCB programme must therefore either specify one witness or characterize a family of witnesses.

## **3. Causal-response constraints**

### **3.1 Operational no-signaling**

For the bipartite Bell scenario, define Alice's marginal:

\\[ P_A(a|x,y) = \sum_bP(a,b|x,y). \\]

No-signaling from Bob to Alice requires

\\[ P_A(a|x,y)=P_A(a|x,y') \\]

for every \\(a,x,y,y'\\).

Similarly, no-signaling from Alice to Bob requires

\\[ P_B(b|x,y)=P_B(b|x',y) \\]

for every \\(b,y,x,x'\\).

These conditions restrict the dependence of marginal outcome distributions on remote settings.

They do not constrain the joint distribution to be Bell-local.

### **3.2 A quantitative signaling measure**

Define the total-variation distance between two probability distributions \\(p,q\\) by

\\[ D\_{\mathrm{TV}}(p,q) = \frac12\sum_i|p_i-q_i|. \\]

The signaling strength from Bob to Alice is

\\[ \mathcal V\_{B\rightarrow A}(P) = \max\_{x,y,y'} \frac12 \sum_a \left| P_A(a|x,y)-P_A(a|x,y') \right|. \\]

Similarly,

\\[ \mathcal V\_{A\rightarrow B}(P) = \max\_{y,x,x'} \frac12 \sum_b \left| P_B(b|x,y)-P_B(b|x',y) \right|. \\]

The overall operational signaling measure is

\\[ \boxed{ \mathcal V\_{\mathrm{NS}}(P) = \max\\{ \mathcal V\_{B\rightarrow A}, \mathcal V\_{A\rightarrow B} \\}. } \\]

It satisfies

\\[ 0\leq\mathcal V\_{\mathrm{NS}}(P)\leq1. \\]

Exact no-signaling is equivalent to

\\[ \mathcal V\_{\mathrm{NS}}(P)=0. \\]

This is an operational measure. It quantifies remote-setting dependence in observed marginals, not every possible notion of causal influence.

### **3.3 Why a causal-response violation measure must be explicit**

Several inequivalent restrictions may be called causal:

- operational no-signaling;
- Bell-local factorization;
- absence of direct inter-party influence in a causal graph;
- measurement independence;
- independent sources in a network;
- relativistic causal ordering;
- intervention invariance;
- bounds on communication or signaling capacity.

A theory can satisfy one while violating another.

Accordingly, a CCCB must identify which constraint its \\(\mathcal V\\) measures. A signaling distance cannot serve as a universal measure of causal violation.

## **4. Assumption classes**

Let

\\[ \mathcal Q \\]

denote a collection of explicit theoretical assumptions.

The admissible distribution set is

\\[ \mathfrak P(\mathcal Q) = \\{P:\ P\text{ satisfies the constraints in }\mathcal Q\\}. \\]

Examples include:

### **4.1 Quantum realizability**

There exist Hilbert spaces, a state \\(\rho\_{AB}\\), and local POVMs such that

\\[ P(a,b|x,y) = \operatorname{Tr} \left[ \rho\_{AB} (M\_{a|x}\otimes N\_{b|y}) \right]. \\]

For spacelike separated measurements, the local measurement operators act on separate tensor factors.

### **4.2 Measurement independence**

In a hidden-variable model with variable \\(\lambda\\), measurement independence is

\\[ P(\lambda|x,y)=P(\lambda). \\]

Relaxations may quantify the deviation from this condition, for example through total-variation distance or mutual information.

### **4.3 Bell-local causal factorization**

A local hidden-variable model has the form

\\[ P(a,b|x,y) = \int d\lambda\\, q(\lambda) P(a|x,\lambda) P(b|y,\lambda), \\]

with measurement-independent \\(q(\lambda)\\).

This assumption is stronger than no-signaling.

### **4.4 Network-source independence**

For a network with independent sources \\(\lambda_1,\ldots,\lambda_m\\),

\\[ q(\lambda_1,\ldots,\lambda_m) = \prod\_{j=1}^{m}q_j(\lambda_j). \\]

Network independence is not implied by ordinary bipartite no-signaling.

### **4.5 Assumption-relative bounds**

For fixed \\(\mathcal Q\\), define the CCCB envelope

\\[ \boxed{ F\_{\mathcal Q}(v) = \sup\_{\substack{P\in\mathfrak P(\mathcal Q)\\\ \mathcal V(P)\leq v}} \mathcal N(P). } \\]

This is the tightest possible upper bound for the selected witness and constraint.

It is monotone nondecreasing in \\(v\\), because increasing the allowed violation enlarges the feasible set.

This envelope is the central mathematical object of CCCB.

## **5. General CCCB optimization theorem**

### **Definition 5.1 — Correlation–causation compatibility envelope**

Given:

- a compact set of conditional probability distributions \\(\mathfrak P(\mathcal Q)\\);
- a continuous correlation functional \\(\mathcal N(P)\\);
- a continuous violation functional \\(\mathcal V(P)\\);

define

\\[ F\_{\mathcal Q}(v) = \max\_{\substack{P\in\mathfrak P(\mathcal Q)\\\ \mathcal V(P)\leq v}} \mathcal N(P). \\]

### **Theorem 5.1 — Existence of the compatibility bound**

If \\(\mathfrak P(\mathcal Q)\\) is compact and the feasible set

\\[ \\{P\in\mathfrak P(\mathcal Q): \mathcal V(P)\leq v\\} \\]

is nonempty, then \\(F\_{\mathcal Q}(v)\\) is attained.

**Proof.**

The feasible set is a closed subset of a compact set because \\(\mathcal V\\) is continuous. It is therefore compact. Since \\(\mathcal N\\) is continuous, the extreme-value theorem guarantees that \\(\mathcal N\\) attains a maximum on the feasible set. \\(\square\\)

### **5.1 Linear and convex cases**

If the admissible set is a polytope and both the witness and violation constraints are linear or can be represented by linear inequalities, the CCCB envelope can be computed by linear programming.

If quantum realizability is imposed exactly, the optimization is generally more difficult. Depending on the scenario and representation, one may use:

- semidefinite relaxations;
- the Navascués–Pironio–Acín hierarchy;
- dimension-constrained optimization;
- see-saw numerical optimization;
- analytical operator inequalities.

A numerical upper bound from a relaxation must be distinguished from an attained quantum optimum.

## **6. The decisive distinction: no-signaling is not Bell locality**

Before deriving a trade-off theorem, one structural obstruction must be addressed.

No-signaling correlations can violate Bell inequalities maximally. Therefore, no universal inequality of the form

\\[ \mathcal N(P)\leq F(\mathcal V\_{\mathrm{NS}}(P)) \\]

can force the Bell correlation strength down to the local bound when \\(\mathcal V\_{\mathrm{NS}}=0\\).

For CHSH, the Popescu–Rohrlich (PR) distribution satisfies

\\[ P(a,b|x,y)= \begin{cases} \frac12,&a\oplus b=xy,\\\ 0,&\text{otherwise}, \end{cases} \\]

where outcomes are represented by bits \\(a,b\in\\{0,1\\}\\).

Its marginals are uniform:

\\[ P(a|x,y)=P(b|x,y)=\frac12. \\]

It is exactly nonsignaling, but its correlators give

\\[ S\_{\mathrm{PR}}=4. \\]

Consequently,

\\[ \boxed{ F\_{\mathrm{NS}}(0)=4 } \\]

for the CHSH witness over the full nonsignaling set.

This is not a failure of the CCCB framework. It demonstrates why the assumptions \\(\mathcal Q\\) must be explicit.

Three distinct compatibility problems must be separated:

1. **Nonsignaling compatibility:** How strong can correlations be without operational signaling?
2. **Quantum compatibility:** How strong can correlations be if they arise from quantum states and local measurements?
3. **Bell-local compatibility:** How strong can correlations be if they admit a measurement-independent local causal model?

The corresponding ceilings are different:

| Theory class         | Maximum CHSH value |
| -------------------- | ------------------ |
| Bell-local           | \\(2\\)            |
| Quantum              | \\(2\sqrt2\\)      |
| General nonsignaling | \\(4\\)            |

A meaningful CCCB must state which of these boundaries is being relaxed.

## **7. Exact baseline theorem: nonsignaling correlation strength**

### **7.1 Binary correlator representation**

For binary outcomes \\(a,b\in\\{-1,+1\\}\\), every conditional distribution can be written

\\[ P(a,b|x,y) = \frac14 \left[ 1+aA\_{xy}+bB\_{xy}+abE\_{xy} \right], \\]

where

\\[ A\_{xy}=\langle a\rangle\_{xy},\qquad B\_{xy}=\langle b\rangle\_{xy},\qquad E\_{xy}=\langle ab\rangle\_{xy}. \\]

No-signaling requires

\\[ A\_{xy}=A_x,\qquad B\_{xy}=B_y. \\]

The correlators \\(E\_{xy}\\) remain free subject to positivity.

### **Theorem 7.1 — Nonsignaling CHSH ceiling**

For every bipartite binary-input, binary-output nonsignaling distribution,

\\[ \boxed{ |S(P)|\leq4. } \\]

The bound is tight.

**Proof.**

Each correlator is an expectation of the product of two \\(\pm1\\)-valued random variables. Therefore,

\\[ -1\leq E\_{xy}\leq1. \\]

Hence

\\[ \begin{aligned} |S| &= |E\_{00}+E\_{01}+E\_{10}-E\_{11}|\\\ &\leq |E\_{00}|+|E\_{01}|+|E\_{10}|+|E\_{11}|\\\ &\leq4. \end{aligned} \\]

The PR distribution has

\\[ (E\_{00},E\_{01},E\_{10},E\_{11})=(1,1,1,-1), \\]

and thus attains \\(S=4\\), while satisfying no-signaling. \\(\square\\)

### **7.2 Consequence for CCCB**

The exact nonsignaling compatibility envelope is constant:

\\[ \boxed{ F\_{\mathrm{NS}}(v)=4 \qquad 0\leq v\leq1, } \\]

because the admissible set with \\(\mathcal V\_{\mathrm{NS}}\leq v\\) always contains the PR distribution.

Thus operational signaling strength alone cannot bound Bell correlation strength more tightly than the algebraic ceiling.

This is an important negative result: the absence of operational signaling, without additional physical assumptions, places no restriction below the algebraic CHSH maximum.

## **8. Quantum compatibility: Tsirelson's bound**

### **8.1 Quantum model**

Assume a bipartite quantum state

\\[ \rho\in\mathcal D(\mathcal H_A\otimes\mathcal H_B) \\]

and local Hermitian observables

\\[ A_0,A_1,\quad B_0,B_1 \\]

satisfying

\\[ A_x^2=B_y^2=I. \\]

The correlators are

\\[ E\_{xy} = \operatorname{Tr} \left[ \rho(A_x\otimes B_y) \right]. \\]

The CHSH operator is

\\[ \widehat S = A_0\otimes(B_0+B_1) + A_1\otimes(B_0-B_1). \\]

### **Theorem 8.1 — Tsirelson bound**

For every quantum state and every pair of local binary observables,

\\[ \boxed{ |S|\leq2\sqrt2. } \\]

**Proof.**

For observables squaring to identity,

\\[ \widehat S^2 = 4I-[A_0,A_1]\otimes[B_0,B_1]. \\]

Since

\\[ \\|[A_0,A_1]\\|\_\infty\leq2, \qquad \\|[B_0,B_1]\\|\_\infty\leq2, \\]

we have

\\[ \\|\widehat S^2\\|\_\infty \leq4+4=8. \\]

Therefore,

\\[ \\|\widehat S\\|\_\infty\leq2\sqrt2. \\]

For any normalized state,

\\[ |S| = |\operatorname{Tr}(\rho\widehat S)| \leq \\|\widehat S\\|\_\infty \leq2\sqrt2. \\]

The bound is attainable using a maximally entangled two-qubit state and appropriately oriented Pauli observables. \\(\square\\)

### **8.2 Quantum signaling constraint**

For local quantum measurements on a shared bipartite state,

\\[ P(a|x,y) = \operatorname{Tr} \left[ \rho(M\_{a|x}\otimes I) \right], \\]

which is independent of \\(y\\). Similarly,

\\[ P(b|x,y) = \operatorname{Tr} \left[ \rho(I\otimes N\_{b|y}) \right] \\]

is independent of \\(x\\).

Thus

\\[ \mathcal V\_{\mathrm{NS}}(P)=0. \\]

The quantum CHSH envelope is consequently

\\[ \boxed{ F\_{\mathrm Q}(v)=2\sqrt2 } \\]

for every \\(v\geq0\\), if the admissible class is restricted to ordinary bipartite quantum correlations with local measurements.

The signaling parameter does not improve this bound because all distributions in that model already have zero operational signaling.

### **8.3 Interpretation**

This result establishes an important baseline:

- no-signaling permits CHSH value \\(4\\);
- quantum theory restricts the value to \\(2\sqrt2\\);
- Bell-local models restrict it to \\(2\\).

The gap between these values is not explained by operational signaling strength. It is a restriction imposed by the mathematical structure of quantum correlations and, more generally, by the assumed physical model.

A nontrivial quantum CCCB must therefore vary an additional assumption or resource, rather than merely allowing small deviations from no-signaling.

## **9. A quantitative bound relative to Bell-local correlations**

A more informative trade-off can be obtained by defining the causal constraint as proximity to a local causal model.

This does not replace no-signaling. It answers a different question: how much Bell violation is possible when the observed distribution is allowed to deviate by a bounded amount from the set of Bell-local distributions?

### **9.1 Local correlation set**

Let

\\[ \mathcal L \\]

denote the set of distributions admitting a measurement-independent Bell-local model:

\\[ L(a,b|x,y) = \int d\lambda\\, q(\lambda) L_A(a|x,\lambda) L_B(b|y,\lambda). \\]

For the finite CHSH scenario, \\(\mathcal L\\) is a convex polytope.

### **9.2 Operational distance to locality**

Define the worst-setting total-variation distance from \\(P\\) to the local set:

\\[ \boxed{ \mathcal V\_{\mathrm{loc}}(P) = \inf\_{L\in\mathcal L} \max\_{x,y} D\_{\mathrm{TV}} \left( P(\cdot,\cdot|x,y), L(\cdot,\cdot|x,y) \right). } \\]

This is zero precisely when \\(P\\) is Bell-local.

It is a causal-model compatibility measure relative to the specified Bell scenario and the assumed measurement-independent factorization.

It should not be interpreted as a universal measure of all causal influence.

### **9.3 Theorem 9.1 — CHSH bound from distance to locality**

For any binary-input, binary-output distribution,

\\[ \boxed{ \mathcal N\_{\mathrm{CHSH}}(P) \leq 2+8\mathcal V\_{\mathrm{loc}}(P). } \\]

**Proof.**

For any local distribution \\(L\\), the CHSH inequality gives

\\[ |S(L)|\leq2. \\]

For each setting pair,

\\[ E\_{xy}(P) = \sum\_{a,b}ab\\,P(a,b|x,y). \\]

Because \\(ab\in\\{-1,+1\\}\\), the difference in correlators obeys

\\[ |E\_{xy}(P)-E\_{xy}(L)| \leq 2D\_{\mathrm{TV}} \left(P(\cdot,\cdot|x,y),L(\cdot,\cdot|x,y)\right). \\]

Summing over the four CHSH setting pairs,

\\[ |S(P)-S(L)| \leq 8\max\_{x,y}D\_{\mathrm{TV}}(P\_{xy},L\_{xy}). \\]

The triangle inequality yields

\\[ |S(P)| \leq |S(L)|+|S(P)-S(L)| \leq 2+8\max\_{x,y}D\_{\mathrm{TV}}(P\_{xy},L\_{xy}). \\]

Taking the infimum over all \\(L\in\mathcal L\\) gives the result. \\(\square\\)

### **9.4 A bounded version**

Since the algebraic CHSH ceiling is \\(4\\), the inequality can be written

\\[ \boxed{ \mathcal N\_{\mathrm{CHSH}}(P) \leq \min\left\\{ 4,\\, 2+8\mathcal V\_{\mathrm{loc}}(P) \right\\}. } \\]

This is a valid CCCB.

It is not yet established to be the sharp envelope for every value of \\(\mathcal V\_{\mathrm{loc}}\\). The coefficient \\(8\\) follows from a general Lipschitz estimate and may be improvable when the full geometry of the local polytope is used.

### **9.5 Geometric meaning**

The inequality states that Bell violation cannot increase arbitrarily rapidly as a distribution moves away from the local set in the selected operational metric.

At zero distance,

\\[ \mathcal V\_{\mathrm{loc}}=0 \Rightarrow \mathcal N\_{\mathrm{CHSH}}\leq2. \\]

At larger distances, the admissible upper bound increases linearly until the algebraic ceiling is reached.

This is a direct quantitative relation between correlation strength and causal-model incompatibility.

## **10. Toward a sharp local-distance trade-off**

The preceding theorem gives a universal Lipschitz bound. The stronger CCCB objective is to compute the exact maximum CHSH value at a specified distance from the local set.

### **10.1 Exact optimization problem**

Define

\\[ \boxed{ F\_{\mathrm{loc}}(v) = \max\_{\substack{P\in\mathcal{NS}\\\ \mathcal V\_{\mathrm{loc}}(P)\leq v}} \mathcal N\_{\mathrm{CHSH}}(P), } \\]

where \\(\mathcal{NS}\\) is the nonsignaling polytope.

This is a finite-dimensional optimization problem. The feasible set is compact, and the maximum exists.

For the quantum-restricted version, define

\\[ F\_{\mathrm{loc}}^{\mathrm Q}(v) = \sup\_{\substack{P\in\mathcal Q\_{\mathrm{CHSH}}\\\ \mathcal V\_{\mathrm{loc}}(P)\leq v}} \mathcal N\_{\mathrm{CHSH}}(P), \\]

where \\(\mathcal Q\_{\mathrm{CHSH}}\\) denotes the quantum-achievable set in the CHSH scenario.

The second envelope is bounded above by \\(2\sqrt2\\), while the first is bounded above by \\(4\\).

### **10.2 Polytope representation**

In the binary CHSH scenario, every local deterministic strategy is specified by four bits

\\[ (a_0,a_1,b_0,b_1)\in\\{-1,+1\\}^4. \\]

There are \\(2^4=16\\) such deterministic strategies.

Every local distribution is a convex combination:

\\[ L=\sum\_{\lambda=1}^{16}q\_\lambda L\_\lambda, \\]

with

\\[ q\_\lambda\geq0,\qquad \sum\_\lambda q\_\lambda=1. \\]

The distance optimization can therefore be formulated by introducing local mixture variables \\(q\_\lambda\\), response variables \\(P(a,b|x,y)\\), and auxiliary absolute-value variables for the total-variation constraints.

For a fixed CHSH orientation, the optimization becomes a linear program:

\\[ \begin{aligned} \text{maximize}\quad& E\_{00}+E\_{01}+E\_{10}-E\_{11}\\\ \text{subject to}\quad& P(a,b|x,y)\geq0,\\\ &\sum\_{a,b}P(a,b|x,y)=1,\\\ &P\in\mathcal{NS},\\\ &\exists q\_\lambda\geq0,\quad\sum\_\lambda q\_\lambda=1,\\\ &\frac12\sum\_{a,b} |P(a,b|x,y)-L(a,b|x,y)| \leq v \quad\forall x,y. \end{aligned} \\]

The absolute-value constraints can be linearized in the standard way.

Optimizing over the eight CHSH orientations accounts for outcome and setting relabelings.

### **10.3 Why the exact envelope matters**

The general bound

\\[ F\_{\mathrm{loc}}(v) \leq \min\\{4,2+8v\\} \\]

is not the final research target.

A sharp theorem would provide:

1. the exact function \\(F\_{\mathrm{loc}}(v)\\);
2. the extremal distributions attaining it;
3. the geometry of the corresponding optimal faces;
4. the range in which quantum correlations attain the same envelope;
5. the point at which post-quantum nonsignaling correlations become necessary.

The resulting curve would be a precise quantitative description of the trade-off between Bell strength and distance from local causal models.

### **10.4 A useful extremal benchmark**

The PR distribution has

\\[ \mathcal N\_{\mathrm{CHSH}}(P\_{\mathrm{PR}})=4. \\]

Its distance from the local set under the chosen worst-setting total-variation metric is at most \\(1/2\\), since it can be mixed with an appropriate local distribution to reach a local boundary. Determining the exact distance, and whether this is the unique extremal geometry up to relabeling, is a finite optimization problem that should be solved rather than assumed.

A numerical linear-programming solution should be followed by a dual certificate if the result is to be presented as an exact theorem.

## **11. Measurement dependence as a separate causal resource**

The local-distance measure above treats deviation from Bell-local correlations as a single operational quantity. A different approach is to relax one of the assumptions used in deriving Bell inequalities.

One such assumption is measurement independence.

### **11.1 Measurement-independent local models**

A conventional local hidden-variable model is

\\[ P(a,b|x,y) = \int d\lambda\\, q(\lambda) P(a|x,\lambda)P(b|y,\lambda), \\]

where

\\[ q(\lambda) \\]

does not depend on \\(x,y\\).

Measurement independence is

\\[ P(\lambda|x,y)=q(\lambda). \\]

### **11.2 Quantifying measurement dependence**

One possible measure is

\\[ \boxed{ \mathcal M = \sup\_{x,y,x',y'} D\_{\mathrm{TV}} \left( q(\lambda|x,y), q(\lambda|x',y') \right). } \\]

This measures the maximum variation in the hidden-variable distribution across setting pairs.

It satisfies

\\[ 0\leq\mathcal M\leq1. \\]

Exact measurement independence corresponds to

\\[ \mathcal M=0. \\]

This definition is not the only possible measure. Other choices include mutual information,

\\[ I(\Lambda:XY), \\]

or average total-variation deviations relative to a specified distribution over settings.

The choice affects the resulting bound and must be treated as part of the assumptions.

### **11.3 A simple CHSH upper bound**

Let the hidden variable be distributed according to \\(q(\lambda|x,y)\\). Assume deterministic local response functions for the moment:

\\[ a=A_x(\lambda),\qquad b=B_y(\lambda). \\]

For each setting pair, compare \\(q(\lambda|x,y)\\) to a fixed reference distribution \\(q_0(\lambda)\\). If

\\[ D\_{\mathrm{TV}}(q(\lambda|x,y),q_0(\lambda)) \leq\delta \\]

for all \\(x,y\\), then the correlator difference satisfies

\\[ |E\_{xy}-E^{(0)}\_{xy}|\leq2\delta. \\]

The reference model is measurement independent and local, so

\\[ |S^{(0)}|\leq2. \\]

It follows that

\\[ \boxed{ |S| \leq 2+8\delta. } \\]

The result extends to stochastic local response functions by absorbing local randomness into \\(\lambda\\).

This inequality is a useful baseline, but it is not automatically a sharp bound in terms of \\(\mathcal M\\). The pairwise supremum defining \\(\mathcal M\\) does not guarantee the existence of one reference distribution \\(q_0\\) within distance \\(\mathcal M\\) of every conditional distribution. A common-reference assumption or a separately defined radius is required.

### **11.4 Common-reference radius**

Define

\\[ \mathcal R\_{\mathrm{MI}} = \inf\_{q_0} \sup\_{x,y} D\_{\mathrm{TV}} \left( q(\lambda|x,y),q_0(\lambda) \right). \\]

Then

\\[ \boxed{ |S|\leq2+8\mathcal R\_{\mathrm{MI}}. } \\]

This is a rigorous measurement-dependence relaxation bound under the stated local-response model.

The distinction between \\(\mathcal M\\) and \\(\mathcal R\_{\mathrm{MI}}\\) matters. Pairwise variation and distance to a common reference are different geometric quantities.

### **11.5 Research opportunity**

A sharper result would optimize the CHSH value directly over all measurement-dependent local models satisfying a specified information or variation budget:

\\[ F\_{\mathrm{MI}}(m) = \sup\_{\substack{P\in\mathcal L\_{\mathrm{MD}}\\\ \mathcal C\_{\mathrm{MI}}\leq m}} |S(P)|. \\]

Here \\(\mathcal L\_{\mathrm{MD}}\\) is the class of local-response models with setting-dependent hidden-variable distributions, and \\(\mathcal C\_{\mathrm{MI}}\\) is an explicitly selected dependence measure.

The optimization should specify the setting distribution, because mutual information and average dependence costs depend on it.

## **12. Network CCCB: independent sources and multipartite correlation**

The bipartite Bell scenario does not capture the full structure of causal constraints in networks. A network may contain several independent sources that distribute systems to overlapping groups of parties.

### **12.1 Bilocal network**

Consider a three-party line network:

\\[ A\longleftarrow S_1\longrightarrow B \longleftarrow S_2\longrightarrow C. \\]

The central party \\(B\\) receives systems from two sources. The end parties \\(A,C\\) each receive one.

The hidden variables are \\(\lambda_1,\lambda_2\\), with source independence

\\[ q(\lambda_1,\lambda_2) = q_1(\lambda_1)q_2(\lambda_2). \\]

A bilocal model has the form

\\[ \begin{aligned} P(a,b,c|x,z) = \int d\lambda_1d\lambda_2\\, &q_1(\lambda_1)q_2(\lambda_2)\\\ &\times P_A(a|x,\lambda_1) P_B(b|\lambda_1,\lambda_2) P_C(c|z,\lambda_2). \end{aligned} \\]

This is not simply ordinary Bell locality for three parties. It contains a stronger structural assumption: the two sources are independent.

### **12.2 Network correlation witness**

For suitable binary observables, define correlators

\\[ I = \frac14\sum\_{x,z} \langle A_x B^0 C_z\rangle, \\]

\\[ J = \frac14\sum\_{x,z} (-1)^{x+z} \langle A_x B^1 C_z\rangle. \\]

Here \\(B^0,B^1\\) are two central observables and \\(A_x,C_z\\) are endpoint observables.

A standard bilocal inequality takes the form

\\[ \boxed{ \sqrt{|I|}+\sqrt{|J|}\leq1. } \\]

Its derivation uses the independent-source factorization. It is not an ordinary linear Bell inequality.

### **12.3 Source-independence violation**

A quantitative source-dependence measure can be defined by

\\[ \mathcal V\_{\mathrm{SI}} = D\_{\mathrm{TV}} \left( q(\lambda_1,\lambda_2), q_1(\lambda_1)q_2(\lambda_2) \right). \\]

Exact source independence corresponds to

\\[ \mathcal V\_{\mathrm{SI}}=0. \\]

However, the hidden variables are generally unobserved. This measure is therefore directly meaningful only within a specified hidden-variable model or when an independent experimental certification procedure supplies a bound on source dependence.

An operational CCCB should avoid treating an unobservable hidden-variable distance as though it were directly measured.

### **12.4 Network CCCB target**

A network correlation strength may be defined by

\\[ \mathcal N\_{\mathrm{net}}(P) = \sqrt{|I(P)|}+\sqrt{|J(P)|}. \\]

A network CCCB would seek

\\[ \boxed{ \mathcal N\_{\mathrm{net}}(P) \leq F\_{\mathrm{net}} \bigl( \mathcal V\_{\mathrm{SI}}(P), \mathcal Q\_{\mathrm{net}} \bigr). } \\]

Here \\(\mathcal Q\_{\mathrm{net}}\\) must specify:

- the network topology;
- which sources are independent;
- the allowed measurements at each node;
- whether quantum or classical sources are permitted;
- whether measurement independence is imposed;
- whether communication between nodes is excluded;
- whether memory across trials is permitted.

### **12.5 Important distinction**

A network-source independence condition is not a no-signaling condition.

A distribution can be nonsignaling while failing to admit a bilocal model. Conversely, a causal network model can satisfy its source-independence structure while exhibiting strong correlations that are not captured by a simple bipartite Bell witness.

The network version of CCCB must therefore treat source independence as an independent causal resource.

## **13. Sequential and intervention-based CCCB**

The static Bell scenario uses measurement settings and outcomes. A more general causal-response framework allows interventions at multiple times.

### **13.1 Sequential experiment**

Let a system undergo a sequence of interventions

\\[ \mathcal E_1,\mathcal E_2,\ldots,\mathcal E_m \\]

with outcomes

\\[ a_1,a_2,\ldots,a_m. \\]

The full process is described by a multi-time probability distribution

\\[ P(a_1,\ldots,a_m| x_1,\ldots,x_m). \\]

A causal-response constraint may restrict whether a later intervention can influence an earlier recorded outcome, or whether one laboratory's choice can influence another laboratory's marginal statistics outside the allowed causal order.

### **13.2 Temporal signaling measure**

For a two-stage experiment, define

\\[ \mathcal V\_{2\rightarrow1} = \max\_{x_1,x_2,x_2'} D\_{\mathrm{TV}} \left( P(a_1|x_1,x_2), P(a_1|x_1,x_2') \right). \\]

In a causally ordered process where stage 2 occurs strictly after stage 1, this quantity should vanish when \\(x_2\\) is chosen after \\(a_1\\) has been irreversibly recorded.

The exact condition depends on the operational protocol and whether postselection or conditioning is permitted.

### **13.3 Temporal correlation strength**

One may define a temporal witness

\\[ \mathcal N\_{\mathrm{temp}} = \sum\_{i,j}c\_{ij} \langle A_i(t_1)B_j(t_2)\rangle \\]

or a Leggett–Garg-type expression.

The corresponding CCCB takes the form

\\[ \mathcal N\_{\mathrm{temp}} \leq F\_{\mathrm{temp}} ( \mathcal V\_{\mathrm{temp}}, \mathcal Q\_{\mathrm{temp}} ). \\]

The assumptions must distinguish:

- temporal quantum correlations;
- classical macrorealist models;
- invasive measurement effects;
- memory between trials;
- causal ordering;
- postselection.

A temporal correlation inequality cannot be imported into a spatial Bell scenario without re-deriving the operational assumptions.

### **13.4 Process-level formulation**

For general multi-time quantum processes, a process matrix or quantum comb provides a suitable mathematical representation.

Let \\(W\\) denote a process and \\(\mathfrak I\\) a collection of local instruments. Then

\\[ P_W(\mathbf a|\mathbf x) = \operatorname{Tr} \left[ W\\, \bigotimes_i M^{(i)}\_{a_i|x_i} \right] \\]

in an appropriate Choi representation.

The process-level CCCB problem is to optimize a chosen temporal or spatial correlation witness over process matrices satisfying specified causal-order or normalization constraints.

This is a natural extension of the present framework, but it is not equivalent to the static-state problem.

## **14. General geometry of the CCCB envelope**

The preceding examples suggest a general geometric interpretation.

Let \\(\mathfrak P(\mathcal Q)\\) be the admissible set of conditional distributions. Each distribution is a point in a finite-dimensional probability space.

The correlation functional \\(\mathcal N\\) assigns a scalar to each point. The causal-response functional \\(\mathcal V\\) assigns a measure of departure from a selected constraint.

The CCCB envelope is the upper boundary of the attainable region

\\[ \boxed{ \Omega\_{\mathcal Q} = \left\\{ (\mathcal V(P),\mathcal N(P)): P\in\mathfrak P(\mathcal Q) \right\\}. } \\]

The desired function is

\\[ F\_{\mathcal Q}(v) = \sup\left\\{ n:(v',n)\in\Omega\_{\mathcal Q}, \ v'\leq v \right\\}. \\]

[Bohrium | AI for Science with Global Scientists](https://images.openai.com/static-rsc-4/DyVRg6uwAzuQC-R2CsH9sHiPyiwl6eTRkK_jsJvNsiqBk8bsHWeWC1lvNiCR5Jgukf_A22kPLpXxLza41CjamNG0xtHn6Czr52x--03BH9gRIHQ_sIQ_qEBBV_vYkLdj8hYdb30Jp5EiSnoV8uXTekJUWJMIih48Pw_FFkgqk84?purpose=inline)

### **14.1 Monotonicity**

If \\(v_1\leq v_2\\), then

\\[ \\{P:\mathcal V(P)\leq v_1\\} \subseteq \\{P:\mathcal V(P)\leq v_2\\}. \\]

Therefore,

\\[ \boxed{ F\_{\mathcal Q}(v_1) \leq F\_{\mathcal Q}(v_2). } \\]

This monotonicity is guaranteed by the optimization definition.

### **14.2 Concavity under convexity assumptions**

Suppose:

1. \\(\mathfrak P(\mathcal Q)\\) is convex;
2. \\(\mathcal N(P)\\) is affine;
3. \\(\mathcal V(P)\\) is convex.

Then the upper envelope \\(F\_{\mathcal Q}(v)\\), defined with the constraint \\(\mathcal V(P)\leq v\\), is concave wherever the optimization is feasible.

**Proof.**

Let \\(P_1,P_2\\) be feasible at budgets \\(v_1,v_2\\), respectively, and let \\(0\leq t\leq1\\). By convexity,

\\[ P_t=tP_1+(1-t)P_2 \\]

is admissible. Convexity of \\(\mathcal V\\) gives

\\[ \mathcal V(P_t) \leq t\mathcal V(P_1)+(1-t)\mathcal V(P_2) \leq tv_1+(1-t)v_2. \\]

Affineness of \\(\mathcal N\\) gives

\\[ \mathcal N(P_t) = t\mathcal N(P_1)+(1-t)\mathcal N(P_2). \\]

Taking maximizing sequences, or maximizers when they exist, yields

\\[ \boxed{ F\_{\mathcal Q}(tv_1+(1-t)v_2) \geq tF\_{\mathcal Q}(v_1) + (1-t)F\_{\mathcal Q}(v_2). } \\]

Thus the envelope is concave. \\(\square\\)

This theorem does not automatically apply when \\(\mathcal N\\) is nonlinear, when the quantum-realizable set is represented by a nonconvex restriction such as fixed local dimension, or when the violation measure is not convex.

### **14.3 Supporting-line formulation**

For a concave envelope, one can seek a family of inequalities

\\[ \boxed{ \mathcal N(P) \leq \alpha+\beta\mathcal V(P) } \\]

for constants \\(\alpha,\beta\geq0\\).

Each valid inequality defines a supporting line above the attainable region. A complete family of optimal supporting lines can reconstruct the upper envelope.

This is useful analytically because a trade-off theorem may be proved by establishing an operator or probability inequality of this form, rather than solving the entire optimization problem at once.

### **14.4 Lagrange-dual formulation**

For a fixed violation budget \\(v\\), consider

\\[ F\_{\mathcal Q}(v) = \sup\_{\substack{P\in\mathfrak P(\mathcal Q)\\\ \mathcal V(P)\leq v}} \mathcal N(P). \\]

Its Lagrangian relaxation is

\\[ F\_{\mathcal Q}(v) \leq \inf\_{\lambda\geq0} \left[ \lambda v+ \sup\_{P\in\mathfrak P(\mathcal Q)} \left( \mathcal N(P)-\lambda\mathcal V(P) \right) \right]. \\]

Under suitable convexity, closedness, and regularity conditions, strong duality can hold.

The inner supremum defines a penalized correlation-response optimization. This gives a practical route to deriving families of CCCB inequalities.

## **15. Experimental and computational programme**

The CCCB programme should progress from exactly solvable probability models to quantum experiments and then to network and sequential architectures.

### **15.1 Phase I — Exact finite-scenario optimization**

Begin with the CHSH scenario.

Compute:

\\[ F\_{\mathrm{loc}}(v),\qquad F\_{\mathrm{NS}}(v),\qquad F\_{\mathrm Q}(v). \\]

The first should use a local-polytope distance, the second a nonsignaling feasible set, and the third a quantum-realizable set.

For the local-distance case, use linear programming. For quantum correlations, use semidefinite relaxations and analytical operator bounds.

Every numerical optimum should be accompanied by:

- the primal candidate distribution;
- a dual certificate or rigorous upper bound;
- the assumed normalization of the violation measure;
- a statement of whether the quantum dimension is unrestricted or bounded;
- a comparison with known Bell and Tsirelson limits.

### **15.2 Phase II — Quantum optimization**

For the quantum scenario, the standard NPA hierarchy provides a sequence of semidefinite outer approximations to the quantum set.

A generic optimization can be written

\\[ \begin{aligned} \text{maximize}\quad &\mathcal N(P)\\\ \text{subject to}\quad& P\in\mathcal Q_k,\\\ &\mathcal V(P)\leq v, \end{aligned} \\]

where \\(\mathcal Q_k\\) is the level-\\(k\\) NPA relaxation.

As \\(k\\) increases, the outer approximations become tighter under the hierarchy's convergence conditions.

A relaxation optimum is an upper bound on the true quantum optimum, not necessarily an achievable quantum value.

### **15.3 Phase III — Experimental realization**

[File:Alice and Bob Setup in a Polarization Quantum Entanglement Experiment.jpg - Wikimedia Commons](https://images.openai.com/static-rsc-4/pVqo_40aSsE2XGUzTGUr5ANFHYBPZrDogbl3WD-viTJXRznjVOmBr7oA9cNOgUQqH1auzCu4Stk30BduF0ofTqMyBUnK9OuMc4U5bCbJ-NPP1mz7b5l1xAA0efbTS5EcdILovKCpET_Pn288BOR7nuU1A4ywjL_Ocwl4O_d_fcw?purpose=inline)

**Photonic Bell tests**

Measure CHSH correlations and characterize marginal signaling under controlled detection and timing conditions.

[São necessárias 7.000 GPUs para simular um minúsculo processador quântico; embora possa não parecer, esta é uma excelente notícia](https://images.openai.com/static-rsc-4/9LFn8lc7FuuNjqqYGehMtU8Elg9dFk0TuzwNPprqE40qnR80TZ-gk4zJwxkSXertat7hleu4Lw8bZdNPsDvMrmggdaZbTaoyOkzVagQdBgM-WPv4I3AJV5dJlw3UMZuXOHwevQ1LPNrKPhEQ83BPLbPn1I8D4hh47N2jDmEltQc?purpose=inline)

**Superconducting processors**

Explore controlled deviations from ideal measurement assumptions and reconstruct response statistics.

[New Frontiers in Quantum Information With Atoms and Ions - Physics Today](https://images.openai.com/static-rsc-4/umN6pwi6yasXb_QaZG6WDTDpQqld0OTkyOjD9DlLx4LuawawOI6OTK4DQOJd_bJnyDrQ_37btzFOKZPLFWf8IW5NZ39dYsIqex344XbZY6pI3VekMVtnNrZxcs7OA0W8M7dLSa4bNTK3Nnxv8246vkFUPQ1HDd3YUGRWynTAyOQ?purpose=inline)

**Trapped-ion systems**

Test high-precision Bell witnesses and sequential intervention protocols.

[Photonic Quantum Technologies | National Institute of Information and Communications Technology](https://images.openai.com/static-rsc-4/TuQFhNIieKkbqHS6IryvnkIAJwkkrJ0PcOFsktKWR_1ddJXIa3PX-K6dc2GWHJVsDTT79ZeYDwqaSZsaBOrdKLlfBVZxPWomr2o7-RvOcwlIGJROFNc5kX75bBuX5kJJGqftcwko-eqsDINUyQlsuFbFfNMLczFUZcZJ5G_hw_U?purpose=inline)

**Quantum networks**

Test network inequalities under independently characterized source and measurement configurations.

### **15.4 Experimental control variables**

A practical study should independently vary:

- source visibility and entanglement;
- measurement-setting distribution;
- detector efficiency;
- measurement timing;
- local measurement orientation;
- communication isolation;
- source independence;
- state-preparation fidelity;
- trial-to-trial memory;
- postselection rules.

The experiment must avoid changing several assumptions simultaneously. Otherwise, the measured movement in the \\((\mathcal V,\mathcal N)\\) plane cannot be attributed to a specific causal constraint.

### **15.5 Primary measured quantities**

| Quantity                   | Mathematical object                 | Experimental role                  |
| -------------------------- | ----------------------------------- | ---------------------------------- |
| Correlation strength       | \\(\mathcal N(P)\\)                 | Bell or network witness            |
| Operational signaling      | \\(\mathcal V\_{\mathrm{NS}}(P)\\)  | Remote-setting dependence          |
| Distance from locality     | \\(\mathcal V\_{\mathrm{loc}}(P)\\) | Local-model incompatibility        |
| Quantum compatibility      | Quantum realization constraints     | Physical-theory restriction        |
| Source dependence          | \\(\mathcal V\_{\mathrm{SI}}\\)     | Network causal assumption          |
| Measurement dependence     | \\(\mathcal C\_{\mathrm{MI}}\\)     | Setting–hidden-variable dependence |
| Reconstruction uncertainty | Confidence region for \\(P\\)       | Finite-statistics control          |

### **15.6 Statistical inference**

For each setting pair, estimate the conditional distribution

\\[ \widehat P(a,b|x,y) \\]

from repeated trials.

Construct a joint confidence region

\\[ \mathcal C\_{1-\alpha} \\]

for the full probability table.

Then compute bounds on the CCCB coordinates:

\\[ \mathcal N\_{\min} = \inf\_{P\in\mathcal C\_{1-\alpha}}\mathcal N(P), \qquad \mathcal N\_{\max} = \sup\_{P\in\mathcal C\_{1-\alpha}}\mathcal N(P), \\]

and similarly for \\(\mathcal V\\).

The claim that an experiment violates a proposed CCCB should be based on confidence regions and a statistically justified comparison with the theoretical envelope, not merely on inserting point estimates into the inequality.

### **15.7 Memory and loopholes**

A rigorous experimental test must address:

- detection and fair-sampling assumptions;
- setting independence;
- communication between measurement stations;
- source characterization;
- memory across trials;
- postselection;
- timing and causal ordering.

A claimed causal-response violation can arise from an unmodeled experimental dependency. It should not be interpreted as a new physical effect until those alternatives are excluded.

## **16. Falsifiability and failure conditions**

A CCCB theorem is only meaningful if its assumptions, witness, and violation measure can be independently checked.

### **16.1 Witness ambiguity**

A claimed bound is not established if the correlation functional changes between the derivation and experiment.

For example, an inequality derived for the CHSH expression cannot automatically be applied to a different Bell functional or to a network witness.

### **16.2 Incorrect causal-response measure**

A signaling measure that examines only marginal distributions cannot detect every failure of causal factorization.

Likewise, distance to the local polytope does not measure all possible forms of causal influence.

A CCCB claim fails if its interpretation is broader than the actual mathematical constraint.

### **16.3 Incomplete assumption set**

A bound derived under measurement independence cannot be applied unchanged to a model with measurement-dependent hidden variables.

A bilocal inequality cannot be used without its independent-source assumption.

A quantum bound cannot be used to constrain arbitrary nonsignaling theories.

### **16.4 Failure of sharpness**

A proposed sharp bound is disproved if an admissible distribution exceeds it.

A numerical optimization is insufficient to establish sharpness without a reliable upper bound and an attainable lower-bound construction.

### **16.5 Failure of experimental reproducibility**

A proposed trade-off must survive independent implementations and reasonable changes in calibration. If the result depends on a particular estimator, detector model, or postselection rule, that dependence must be included in the theorem's operational assumptions.

## **17. Novelty assessment**

### **17.1 Established foundations**

The following are already established mathematical and physical results:

- Bell inequalities and local hidden-variable bounds;
- Tsirelson's quantum CHSH bound;
- the algebraic CHSH ceiling;
- nonsignaling polytopes;
- causal factorization and Bell-local models;
- measurement-dependent Bell models;
- bilocal and network inequalities;
- semidefinite relaxations of quantum correlations;
- statistical distances between probability distributions.

A general statement that stronger correlations require relaxing some causal or operational assumption is not new by itself.

### **17.2 What this paper establishes**

The paper develops a unified optimization language for the problem:

\\[ F\_{\mathcal Q}(v) = \sup\_{\substack{P\in\mathfrak P(\mathcal Q)\\\ \mathcal V(P)\leq v}} \mathcal N(P). \\]

It establishes:

1. existence of the compatibility envelope under compactness and continuity;
2. monotonicity of the envelope;
3. concavity under specified convexity assumptions;
4. the exact nonsignaling CHSH ceiling;
5. the quantum Tsirelson ceiling;
6. a general Lipschitz bound relating CHSH strength to distance from Bell-local correlations;
7. a measurement-dependence relaxation bound under a common-reference condition.

These are useful baseline results, but several are direct consequences of established mathematics.

### **17.3 What would constitute a genuine discovery**

A substantive new CCCB result should provide at least one of the following:

**A. A new sharp trade-off surface**

Derive an exact function

\\[ F\_{\mathcal Q}(v) \\]

for a causal constraint or network structure not already covered by known inequalities.

**B. A stronger metric-sensitive Bell bound**

Show that a selected operational distance yields a sharp bound tighter than the generic Lipschitz estimate, with an exact family of extremal distributions.

**C. A joint constraint theorem**

Derive a sharp bound when several assumptions are relaxed simultaneously, for example:

\\[ \mathcal N(P) \leq F\left( \mathcal V\_{\mathrm{NS}}, \mathcal C\_{\mathrm{MI}}, \mathcal V\_{\mathrm{SI}}, \mathcal Q \right). \\]

The difficulty is to avoid double-counting correlated relaxations or treating hidden-variable parameters as directly observable.

**D. A network-specific theorem**

Characterize the maximum network correlation under quantitatively bounded source dependence, with a physically meaningful operational certification of the independence defect.

**E. A sequential causal-response theorem**

Derive a trade-off between temporal correlation strength and violations of specified causal ordering constraints, including memory and intervention effects.

### **17.4 Novelty verdict**



Coherent mathematical framework

New sharp trade-off not yet established



CCCB is a sound research programme and a useful unifying formulation. The strongest result at present is not a new universal physical law but the explicit construction of a family of assumption-relative optimization problems.

The most important negative result is that no-signaling alone permits maximal CHSH correlation. This rules out a broad class of overly simple correlation-versus-signaling trade-off claims.

The most promising route to novelty is a sharp network or sequential CCCB with a genuinely operational causal-violation measure and a dual-certified extremal theorem.

## **18. Principal conjectures and open problems**

### **Conjecture 18.1 — Metric-sensitive extremal frontier**

For selected finite Bell scenarios, the exact correlation–locality frontier may admit a piecewise analytic representation

\\[ F\_{\mathrm{loc}}(v) = \begin{cases} f_1(v),&0\leq v\leq v_1,\\\ f_2(v),&v_1\<v\leq v_2,\\\ \vdots \end{cases} \\]

whose segments correspond to changes in the extremal faces of the local and nonsignaling polytopes.

This conjecture is testable by exact polytope optimization. The existence of a piecewise-linear frontier follows in appropriate polyhedral formulations; the nontrivial issue is its exact form for the selected metric and witness.

### **Conjecture 18.2 — Quantum frontier under bounded operational deviation**

For suitably generalized quantum process models that permit a controlled operational deviation from ideal local measurement assumptions, there may be a nontrivial trade-off between correlation strength and a precisely defined response violation.

Ordinary tensor-product quantum correlations do not supply such a trade-off for marginal signaling because their operational signaling measure is identically zero.

A new result must therefore specify what physical feature is being relaxed, rather than simply allowing quantum probabilities to signal.

### **Conjecture 18.3 — Joint resource accounting**

For a network with several independent causal assumptions, a joint resource function may characterize the admissible correlation region:

\\[ \mathcal N(P) \leq F( v\_{\mathrm{response}}, v\_{\mathrm{source}}, v\_{\mathrm{measurement}}, \mathcal Q ). \\]

The key open question is whether the separate violation measures can be combined without losing sharpness or introducing redundant parameters.

### **Conjecture 18.4 — Operationally certified source independence**

A useful network CCCB should replace inaccessible hidden-variable dependence measures with quantities that can be independently bounded from observed source preparation, calibration, and intervention data.

The conjectured result is an experimentally meaningful source-dependence budget that implies a rigorous network-correlation ceiling.

### **Open Problem 18.5 — Dimension-constrained CCCB**

Determine the exact frontier

\\[ F\_{\mathcal Q,d}(v) \\]

for quantum realizations with local Hilbert-space dimension bounded by \\(d\\).

This may differ from the unrestricted quantum frontier and may expose dimension-dependent extremal correlation structures.

### **Open Problem 18.6 — Robust CCCB under finite data**

Develop a theorem that directly bounds the probability of falsely rejecting a causal model when both the correlation witness and violation measure are estimated from finite samples.

This would connect the mathematical trade-off to experimentally defensible statistical certification.

## **19. Conclusion**

The Correlation–Causation Compatibility Bound framework treats the relationship between distant correlations and causal-response restrictions as a quantitative optimization problem.

Its central object is

\\[ \boxed{ F\_{\mathcal Q}(v) = \sup\_{\substack{P\in\mathfrak P(\mathcal Q)\\\ \mathcal V(P)\leq v}} \mathcal N(P). } \\]

The function is not universal. It depends on the correlation witness, the operational violation measure, and the theoretical assumptions defining the admissible distribution set.

The analysis establishes several essential distinctions.

First, no-signaling does not imply Bell locality. The PR distribution achieves the algebraic CHSH maximum while exhibiting exactly zero operational signaling.

Second, quantum realizability imposes the Tsirelson ceiling independently of the signaling measure. In ordinary quantum theory with local measurements, the marginal signaling measure is identically zero.

Third, a quantitative distance to the Bell-local set does yield a direct correlation bound:

\\[ \boxed{ \mathcal N\_{\mathrm{CHSH}}(P) \leq \min\left\\{ 4,\\, 2+8\mathcal V\_{\mathrm{loc}}(P) \right\\}. } \\]

This is a valid general estimate, although its sharpness remains a separate optimization problem.

Fourth, measurement independence and network-source independence are distinct causal assumptions. They require separate violation measures and separate compatibility theorems.

The research programme therefore has a clear mathematical direction: select a causal architecture, define its violation measure operationally, select a correlation witness, and derive the exact upper envelope of the admissible region.

A successful CCCB discovery would not merely restate Bell or Tsirelson bounds. It would establish a new sharp theorem showing how a quantitatively specified relaxation of a causal or operational constraint changes the maximum possible correlation strength.

The most promising next step is the exact CHSH local-distance optimization, followed by a network-source-independence extension. These provide finite, testable problems with clear extremal conditions, established comparison bounds, and a realistic route to a rigorous novelty claim.

## **References**

1\. J. S. Bell, “On the Einstein Podolsky Rosen paradox,” *Physics Physique Fizika* **1**, 195–200 (1964).

2\. J. F. Clauser, M. A. Horne, A. Shimony, and R. A. Holt, “Proposed experiment to test local hidden-variable theories,” *Physical Review Letters* **23**, 880–884 (1969).

3\. B. S. Cirel'son, “Quantum generalizations of Bell's inequality,” *Letters in Mathematical Physics* **4**, 93–100 (1980).

4\. S. Popescu and D. Rohrlich, “Quantum nonlocality as an axiom,” *Foundations of Physics* **24**, 379–385 (1994).

5\. J. Barrett, N. Linden, S. Massar, S. Pironio, S. Popescu, and D. Roberts, “Nonlocal correlations as an information-theoretic resource,” *Physical Review A* **71**, 022101 (2005).

6\. J. Barrett, L. Hardy, and A. Kent, “No signaling and quantum key distribution,” *Physical Review Letters* **95**, 010503 (2005).

7\. A. Fine, “Hidden variables, joint probability, and the Bell inequalities,” *Physical Review Letters* **48**, 291–295 (1982).

8\. J. Henson, R. Lal, and M. F. Pusey, “Theory-independent limits on correlations from generalised Bayesian networks,” *New Journal of Physics* **16**, 113043 (2014).

9\. M. J. W. Hall, “Local deterministic model of singlet state correlations based on relaxing measurement independence,” *Physical Review Letters* **105**, 250404 (2010).

10\. J. Barrett, R. Augusiak, M. Navascués, T. Vértesi, and A. Acín, “Maximally nonlocal behavior and the limits of quantum theory,” *Physical Review Letters* **110**, 010403 (2013).

11\. M. Navascués, S. Pironio, and A. Acín, “A convergent hierarchy of semidefinite programs characterizing the set of quantum correlations,” *New Journal of Physics* **10**, 073013 (2008).

12\. C. Branciard, N. Gisin, and S. Pironio, “Characterizing the nonlocal correlations created via entanglement swapping,” *Physical Review Letters* **104**, 170401 (2010).

13\. C. Branciard, D. Rosset, N. Gisin, and S. Pironio, “Bilocal versus nonbilocal correlations in entanglement swapping experiments,” *Physical Review A* **85**, 032119 (2012).

14\. T. Fritz, “Beyond Bell's theorem: Correlation scenarios,” *New Journal of Physics* **14**, 103001 (2012).

15\. R. Chaves, “Polynomial Bell inequalities,” *Physical Review A* **87**, 022102 (2013).

16\. M. F. Pusey, “Anomalous weak values are proofs of contextuality,” *Physical Review Letters* **113**, 200401 (2014).

17\. N. Brunner, D. Cavalcanti, S. Pironio, V. Scarani, and S. Wehner, “Bell nonlocality,” *Reviews of Modern Physics* **86**, 419–478 (2014).

18\. R. Augusiak, M. Demianowicz, and A. Acín, “Local hidden-variable models for entangled quantum states,” *Journal of Physics A: Mathematical and Theoretical* **47**, 424002 (2014).

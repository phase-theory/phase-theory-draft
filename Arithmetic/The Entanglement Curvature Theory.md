# The Entanglement Curvature Theory

## A Reconstruction Framework Connecting Quantum Correlations, Geometric Invariants, and Emergent Spacetime

Research preprint · October 19, 2026 · Quantum information, differential geometry, holography, mathematical physics

## Abstract

The Entanglement Curvature Theory (ECT) investigates whether geometric curvature can be reconstructed from the organization of quantum correlations, rather than introduced as a primitive property of an underlying spacetime. Its starting point is the reduced density operator of a quantum subsystem AAA, with entanglement entropy

S(A)=−Tr⁡(ρAln⁡ρA).S(A)=-\operatorname{Tr}(\rho_A\ln\rho_A).S(A)=−Tr(ρAlnρA).

In selected holographic theories, entanglement entropy is related to the area of a minimal or extremal surface in a gravitational dual. The Ryu–Takayanagi prescription establishes this relation in static semiclassical holographic settings, while its covariant generalization and quantum corrections extend the connection under additional assumptions. These are established results within their respective domains, not evidence that arbitrary entanglement patterns uniquely determine spacetime.

![](https://www.google.com/s2/favicons?domain=https://arxiv.org\&sz=32)

arXiv

+2

ECT asks a more general inverse question: given a precisely defined family of quantum correlation data, under what conditions can one reconstruct a geometric invariant, and when can that invariant be identified with curvature?

This paper develops a candidate Entanglement Curvature Reconstruction (ECR) framework based on region-indexed entropies, mutual information, multipartite correlation data, and the response of entanglement to controlled changes in subsystem configuration. It distinguishes the entanglement data themselves from a reconstructed distance, the distance from a metric, and the metric from its curvature. A conditional reconstruction theorem is formulated for a specified class of quantum states whose correlation data admit a controlled geometric limit. A second theorem identifies the additional assumptions required to recover curvature from reconstructed distances.

The principal result is a rigorous architecture for a reconstruction program, not a universal theorem that entropy alone determines geometry. The theory's central conjecture is that, for an appropriately restricted class of states with locality, regularity, and identifiability properties, an enriched entanglement signature can determine a metric-measure structure and thereby its curvature invariants. The decisive obstacle is nonuniqueness: different quantum states, tensor-network realizations, and geometries can share the same entanglement entropies. ECT must therefore establish exactly which information is sufficient, which ambiguities remain, and why its chosen correlation data do not encode the target geometry circularly.

Central claim. Quantum correlations may provide reconstructive evidence for geometry, but curvature becomes a theorem only after the correlation-to-distance map, its continuum limit, and the required regularity assumptions have been proved.

## 1. The foundational problem

In conventional differential geometry, curvature is defined from a metric and its derivatives. For a Riemannian manifold (M,g)(M,g)(M,g), the metric determines the Levi-Civita connection, which determines the Riemann curvature tensor,

Rρσμν=∂μΓνσρ−∂νΓμσρ+ΓμαρΓνσα−ΓναρΓμσα.R^\rho{}_{\sigma\mu\nu} = \partial_\mu\Gamma^\rho_{\nu\sigma} -\partial_\nu\Gamma^\rho_{\mu\sigma} +\Gamma^\rho_{\mu\alpha}\Gamma^\alpha_{\nu\sigma} -\Gamma^\rho_{\nu\alpha}\Gamma^\alpha_{\mu\sigma}.Rρσμν=∂μΓνσρ−∂νΓμσρ+ΓμαρΓνσα−ΓναρΓμσα.

Quantum entanglement, by contrast, is defined from the state of a composite quantum system and a choice of subsystem decomposition. Given a bipartite state ρAB\rho_{AB}ρAB, the reduced state of AAA is

ρA=Tr⁡BρAB,\rho_A=\operatorname{Tr}_B\rho_{AB},ρA=TrBρAB,

and its von Neumann entropy measures the mixedness of that reduced state. For a pure global state, this entropy quantifies entanglement between AAA and its complement; for a mixed global state, it also reflects correlations with an environment and need not measure entanglement alone.

ECT reverses the usual explanatory order. Rather than assume a metric and then compute entanglement, it asks whether a suitable pattern of quantum correlations can define a distance, whether that distance can determine a metric, and whether the metric's curvature can then be reconstructed.

The proposed sequence is

Quantum state→Correlation structure→Distance→Metric→Curvature\boxed{ \text{Quantum state} \rightarrow \text{Correlation structure} \rightarrow \text{Distance} \rightarrow \text{Metric} \rightarrow \text{Curvature} }Quantum state→Correlation structure→Distance→Metric→Curvature

Each arrow has a distinct mathematical burden. Entropy is defined by quantum information theory. Distance requires a reconstruction rule. A metric requires local regularity or a suitable metric-space limit. Curvature requires additional smoothness or a generalized notion of curvature. None of these later structures follows merely from the existence of entanglement.

The research question is therefore not whether entanglement and geometry are related in some known settings. They are. The question is whether the relationship can be generalized into a controlled inverse theorem for a clearly specified class of quantum systems.

## 2. Quantum state space and the primitive correlation data

### 2.1 Bipartite systems

Let HA\mathcal H_AHA and HB\mathcal H_BHB be Hilbert spaces associated with subsystems AAA and BBB. A joint quantum state is a positive trace-class operator

ρAB≥0,Tr⁡ρAB=1.\rho_{AB}\geq0,\qquad \operatorname{Tr}\rho_{AB}=1.ρAB≥0,TrρAB=1.

The reduced density operators are

ρA=Tr⁡BρAB,ρB=Tr⁡AρAB.\rho_A=\operatorname{Tr}_B\rho_{AB}, \qquad \rho_B=\operatorname{Tr}_A\rho_{AB}.ρA=TrBρAB,ρB=TrAρAB.

The entanglement entropy is

S(A)=−Tr⁡(ρAln⁡ρA).S(A)=-\operatorname{Tr}(\rho_A\ln\rho_A).S(A)=−Tr(ρAlnρA).

For a pure state ρAB=∣Ψ⟩⟨Ψ∣\rho_{AB}=|\Psi\rangle\langle\Psi|ρAB=∣Ψ⟩⟨Ψ∣, one has S(A)=S(B)S(A)=S(B)S(A)=S(B), and this entropy is an entanglement measure across the bipartition. For mixed states, S(A)S(A)S(A) alone does not distinguish quantum entanglement from classical or environmental correlations.

This distinction is foundational. An ECT model must specify whether it uses pure global states, mixed states with a controlled purification, or entanglement measures designed for mixed bipartitions.

### 2.2 Region-indexed quantum systems

To discuss geometry, one needs more than a single bipartition. Let R\mathcal RR denote a family of subsystems or regions in a quantum system. For each A∈RA\in\mathcal RA∈R, suppose a reduced density operator ρA\rho_AρA is defined.

The elementary entropy data are

E1={S(A):A∈R}.\mathcal E_1=\{S(A):A\in\mathcal R\}.E1={S(A):A∈R}.

This collection is not necessarily geometric. If the subsystem labels are abstract, their organization does not yet define spatial adjacency, distance, dimension, or curvature.

We therefore distinguish the labels from the geometry to be reconstructed. The subsystem family R\mathcal RR may initially be a set of factors, a collection of selected tensor factors, a family of subalgebras, or another mathematically precise subsystem structure. If its labels already specify spatial regions in a manifold, the geometry has partly been supplied in advance.

### 2.3 The enriched entanglement signature

The candidate ECT input is not the entropy of one region but a collection of correlation observables:

E(Ψ)=(E1,E2,E3,…).\mathfrak E(\Psi)= \left( \mathcal E_1,\mathcal E_2,\mathcal E_3,\ldots \right).E(Ψ)=(E1,E2,E3,…).

Its components may include:

* single-region entropies;

* mutual information between disjoint subsystems;

* multipartite entropy combinations;

* Rényi entropies and their parameter dependence;

* responses under controlled changes of the state or subsystem algebra;

* correlation functions of specified observables;

* conditional mutual information and other measures of correlation structure.

The inclusion of these quantities is a research proposal, not a claim that they universally determine geometry. Each component must be justified by a precise reconstruction theorem and a clearly defined class of states.

## 3. Mutual information as a candidate relational observable

For two subsystems AAA and BBB, define the mutual information

I(A:B)=S(A)+S(B)−S(AB).I(A:B)=S(A)+S(B)-S(AB).I(A:B)=S(A)+S(B)−S(AB).

Mutual information measures total correlations between AAA and BBB. It is nonnegative for ordinary quantum states and vanishes precisely when the joint state factorizes as ρAB=ρA⊗ρB\rho_{AB}=\rho_A\otimes\rho_BρAB=ρA⊗ρB.

Unlike an individual entropy, mutual information is naturally relational. It compares two subsystems rather than characterizing one subsystem's mixedness in isolation.

ECT considers the possibility that mutual information can induce a notion of separation. In many local quantum field theories, correlations depend on spatial separation, and mutual information between separated regions can decay as their separation increases. However, the relationship depends on the state, observables, subsystem sizes, energy scale, and theory. It is not a universal monotone of geometric distance.

### 3.1 A candidate information distance

Suppose Q\mathcal QQ is a collection of elementary subsystems and that I(A:B)I(A:B)I(A:B) is defined for distinct A,B∈QA,B\in\mathcal QA,B∈Q. A possible candidate separation score is

Dη(A,B)=−ηln⁡(I(A:B)+δI∗),D_\eta(A,B)= -\eta\ln\left( \frac{I(A:B)+\delta} {I_*} \right),Dη(A,B)=−ηln(I∗I(A:B)+δ),

where η&gt;0\eta>0η&gt;0 sets a scale, I∗&gt;0I_*>0I∗&gt;0 is a reference value, and δ≥0\delta\geq0δ≥0 is a regulator for vanishing mutual information.

This expression is only a candidate dissimilarity, not a proven metric. It may be negative for large mutual information, depend strongly on normalization, fail the triangle inequality, or diverge when correlations vanish. The regulator also changes the meaning of the result.

A valid ECT distance must therefore satisfy, at minimum,

d(A,B)≥0,d(A,B)=d(B,A),d(A,B)\geq0,\qquad d(A,B)=d(B,A),d(A,B)≥0,d(A,B)=d(B,A),

d(A,B)=0  ⟺  A=B,d(A,B)=0\iff A=B,d(A,B)=0⟺A=B,

d(A,C)≤d(A,B)+d(B,C).d(A,C)\leq d(A,B)+d(B,C).d(A,C)≤d(A,B)+d(B,C).

If distinct subsystems can have zero reconstructed separation, the construction yields at most a pseudometric until the corresponding equivalence classes are identified.

### 3.2 An operational route to distance

Instead of choosing a logarithmic transform arbitrarily, one can define a distance through the decay of a specified correlation function or a family of distinguishability measures. For example, if a model yields

I(A:B)∼C(A,B)e−d(A,B)/ξI(A:B)\sim C(A,B)e^{-d(A,B)/\xi}I(A:B)∼C(A,B)e−d(A,B)/ξ

in a declared regime, then

d(A,B)∼−ξln⁡(I(A:B)C(A,B)).d(A,B)\sim -\xi\ln\left(\frac{I(A:B)}{C(A,B)}\right).d(A,B)∼−ξln(C(A,B)I(A:B)).

This inference is valid only if the exponential law, amplitude C(A,B)C(A,B)C(A,B), and correlation length ξ\xiξ are independently specified or derived. It is not a universal identity for quantum mutual information.

The strongest version of ECT would derive a distance from a correlation law rather than define the law to reproduce an already-known distance. This is the first test of noncircularity.

## 4. Entanglement entropy and geometric area in holography

The strongest established bridge between entanglement and geometry occurs in holographic duality. In a static semiclassical bulk with an appropriate gravitational dual, the Ryu–Takayanagi prescription relates the entropy of a boundary region to the area of a minimal bulk surface homologous to that region:

S(A)=Area⁡(γA)4GNS(A)=\frac{\operatorname{Area}(\gamma_A)}{4G_N}S(A)=4GNArea(γA)

in units with ℏ=1\hbar=1ℏ=1, where GNG_NGN is the bulk Newton constant in the corresponding dimension and γA\gamma_AγA is the appropriate codimension-two minimal surface. The covariant HRT prescription uses extremal surfaces for time-dependent settings. Quantum corrections lead to generalized entropy and quantum extremal surfaces under further assumptions.

![](https://www.google.com/s2/favicons?domain=https://arxiv.org\&sz=32)

arXiv

+2

This relation is highly significant because a quantum-information quantity on one side of a duality is computed by a geometric area on the other. But it is important to state exactly what it establishes.

It does not say that the entropy of any arbitrary subsystem equals an area in an arbitrary geometry. The formula depends on the holographic dictionary, the bulk gravitational theory, the state, the boundary region, and the regime in which the semiclassical description is valid.

### 4.1 From area data to curvature: the inverse problem

Suppose one knows the entropy S(A)S(A)S(A) for many boundary regions. In a holographic setting, these entropies may constrain areas of a family of extremal surfaces. Under sufficiently rich coverage and additional assumptions, such area data can constrain the bulk geometry.

But area data are not the same as a complete metric. Different metrics can share some surface areas, and the set of surfaces accessible to a given boundary theory may be restricted. The inverse problem requires proving that the available surfaces are sufficiently rich to identify the target geometric class.

ECT generalizes this question:

> Can a state-defined family of entanglement observables determine a curvature invariant without assuming a holographic bulk geometry at the outset?

That is a substantially stronger claim than the Ryu–Takayanagi relation. It needs its own theorem.

### 4.2 A hierarchy of possible results

Established bridge

In suitable holographic settings, entanglement entropy is related to extremal-surface area.

Inverse area reconstruction

A sufficiently rich and identifiable family of area data may constrain geometry within a specified class.

General entanglement reconstruction

A non-holographic or more general quantum system yields a well-defined metric and curvature from a specified enriched entanglement signature. This is the proposed ECT research target.

The third result cannot be inferred simply by extending the holographic formula to all quantum states. It requires an independent construction and proof.

## 5. Entanglement curvature: what exactly is the target?

The phrase entanglement curvature can refer to several mathematically different objects. ECT must choose among them rather than use the phrase as though they were equivalent.

We distinguish four candidates.

### 5.1 Curvature reconstructed from an information metric

If the entanglement data determine a smooth distance dEd_{\mathfrak E}dE on a reconstructed space XXX, and that distance arises from a Riemannian metric gEg_{\mathfrak E}gE, then the ordinary Riemann curvature tensor is well-defined:

Rρσμν\(gE\).R^\rho{}_{\sigma\mu\nu}\(g\_{\\mathfrak E}\).Rρσμν\(gE​\).

The scalar curvature

RE=gEμνRμν\(gE\)R_{\mathfrak E} = g_{\mathfrak E}^{\mu\nu} R_{\mu\nu}\(g\_{\\mathfrak E}\)RE=gEμνRμν\(gE​\)

is then an ordinary geometric invariant. The novelty would lie in deriving gEg_{\mathfrak E}gE from the quantum data, not in redefining the Riemann tensor.

This is the most direct target for a theory claiming that geometric curvature emerges from quantum correlations.

### 5.2 Curvature of a statistical or quantum-state manifold

A parameterized family of states ρ(θ)\rho(\theta)ρ(θ) can itself carry a geometric structure. For example, a quantum Fisher-information metric may be defined on a suitable family of states, and its curvature characterizes aspects of the geometry of state space.

That curvature is not automatically spatial curvature. The parameters θa\theta^aθa might represent couplings, temperatures, control fields, or variational parameters rather than positions in spacetime.

ECT must prove a mapping between state-space geometry and the target physical geometry before identifying these curvatures.

### 5.3 Curvature from entanglement response

Suppose a family of states ρ(θ)\rho(\theta)ρ(θ) is generated by controlled deformations. Entanglement observables can be differentiated with respect to θ\thetaθ, producing a response matrix or higher-order response tensors.

These objects may reveal local structure in the space of states. However, their indices initially refer to deformation parameters. They should not be interpreted as spacetime tensor indices unless a reconstruction map identifies the parameter directions with physical directions.

### 5.4 Curvature as a correlation defect

One might define a discrete curvature-like quantity from departures of correlation distances from flat-space relations. For a set of nodes with reconstructed pairwise distances, one could compare local distance configurations against Euclidean or constant-curvature reference configurations.

Such a defect may be useful computationally. But unless it is proved to converge to a known curvature tensor or scalar, it is a discrete diagnostic rather than a fundamental geometric invariant.

For the core theory, the preferred target is ordinary scalar curvature R\(gE\)R\(g\_{\\mathfrak E}\)R\(gE​\) of a reconstructed metric, with state-space and discrete curvatures treated as possible tools rather than substitutes.

## 6. The entanglement response structure

The single entropy S(A)S(A)S(A) is too compressed to serve as a universal geometric signature. ECT therefore considers a family of observables that describe how entanglement changes across a structured set of subsystem choices.

### 6.1 Rényi entropy

For n&gt;0n>0n&gt;0, n≠1n\neq1n=1, define

Sn(A)=11−nln⁡Tr⁡(ρAn).S_n(A)=\frac{1}{1-n}\ln\operatorname{Tr}(\rho_A^n).Sn(A)=1−n1lnTr(ρAn).

When the limit is well-defined,

lim⁡n→1Sn(A)=S(A).\lim_{n\to1}S_n(A)=S(A).n→1limSn(A)=S(A).

The Rényi family probes more of the eigenvalue distribution of ρA\rho_AρA than the von Neumann entropy alone. In particular, S2(A)=−ln⁡Tr⁡(ρA2)S_2(A)=-\ln\operatorname{Tr}(\rho_A^2)S2(A)=−lnTr(ρA2) depends on the purity of the reduced state.

Even the full Rényi spectrum of one subsystem does not generally determine the global quantum state or a unique geometry. Its potential value is in combination with subsystem dependence and relational correlation data.

### 6.2 Entropy variation

Let ρA(ϵ)\rho_A(\epsilon)ρA(ϵ) be a differentiable family of reduced states. When the relevant derivatives and support conditions are controlled,

dS(A)dϵ=−Tr⁡(dρAdϵln⁡ρA),\frac{dS(A)}{d\epsilon} = -\operatorname{Tr}\left( \frac{d\rho_A}{d\epsilon}\ln\rho_A \right),dϵdS(A)=−Tr(dϵdρAlnρA),

using Tr⁡(dρA/dϵ)=0\operatorname{Tr}(d\rho_A/d\epsilon)=0Tr(dρA/dϵ)=0. If the state has changing support or zero eigenvalues, the derivative may require more careful treatment.

This response describes the sensitivity of entanglement to a chosen deformation. It does not directly measure curvature. The deformation must be physically specified, and the relationship between its response and geometric invariants must be derived.

### 6.3 A regional entanglement Hessian

Let θ=(θ1,…,θm)\theta=(\theta^1,\ldots,\theta^m)θ=(θ1,…,θm) parameterize a family of subsystem configurations or states. Define the regional entropy Hessian

Hab(θ)=∂2S(θ)∂θa∂θb.H_{ab}(\theta) = \frac{\partial^2 S(\theta)} {\partial\theta^a\partial\theta^b}.Hab(θ)=∂θa∂θb∂2S(θ).

This matrix need not be positive, and it is not automatically a metric. It can be coordinate-dependent and can change under reparameterization.

A metric-like tensor requires a justified construction. For example, a positive information metric can arise from the second-order expansion of an appropriate distinguishability measure between states. But even if such a metric exists, its curvature belongs to the parameter manifold until its relationship to physical space is proven.

### 6.4 The ECT correlation signature

For a declared family of subsystems R\mathcal RR, define

EΨ={Sn(A), I(A:B), I(A:B∣C), C(A1,…,Ak)},\mathfrak E_\Psi= \left\{ S_n(A),\, I(A:B),\, I(A:B|C),\, \mathcal C(A_1,\ldots,A_k) \right\},EΨ={Sn(A),I(A:B),I(A:B∣C),C(A1,…,Ak)},

where C\mathcal CC denotes any additional specified correlation observables, and

I(A:B∣C)=S(AC)+S(BC)−S(C)−S(ABC)I(A:B|C)=S(AC)+S(BC)-S(C)-S(ABC)I(A:B∣C)=S(AC)+S(BC)−S(C)−S(ABC)

is the conditional mutual information for the indicated subsystem decomposition.

The conditional mutual information is nonnegative in finite-dimensional quantum systems and can reveal approximate conditional independence. Such structure may help distinguish local from nonlocal correlation patterns, but it does not by itself define a spatial metric.

The theory's task is to show that the selected signature is both sufficient for a declared reconstruction and stable under the physical transformations considered irrelevant.

## 7. Candidate ECT distance from correlation distinguishability

An important design choice is whether to use correlation strength directly or compare how distinguishable quantum states are when the subsystem configuration changes.

A general construction can begin with a family of reduced states ρA(x)\rho_A(x)ρA(x) indexed by abstract labels x∈Xx\in Xx∈X. These labels are not assumed to be coordinates on a manifold.

Let D(ρ,σ)\mathcal D(\rho,\sigma)D(ρ,σ) be a nonnegative distinguishability functional. A candidate distance is

dD(x,y)=F ⁣\(D(ρA(x),ρA(y))\),d_{\mathcal D}(x,y) = \mathcal F\!\left\( \\mathcal D\\bigl(\\rho\_A(x),\\rho\_A(y)\\bigr) \\right\),dD(x,y)=F\(D(ρA​(x),ρA​(y))\),

where F\mathcal FF is a fixed nonnegative transformation chosen to yield the correct limiting behavior.

Possible choices of D\mathcal DD include quantum relative entropy, fidelity-based distances, or metrics induced by quantum information geometry. Each has distinct properties. Quantum relative entropy, for example, is generally asymmetric and does not satisfy the triangle inequality, so it cannot be treated as a metric without a separate symmetrization and proof. Fidelity-based constructions may yield a metric after a suitable transformation, but their operational interpretation and relation to spatial distance must still be established.

The central requirement is not to select whichever formula best resembles a known metric. It is to demonstrate that the candidate distance satisfies the metric axioms and converges to a physically meaningful separation under a specified class of states.

### 7.1 Nondegeneracy

If two distinct labels yield identical reduced states for every allowed observable, then the proposed signature cannot distinguish them. One must either identify the labels as equivalent or enrich the observable family.

### 7.2 Triangle inequality

Pairwise correlation strengths need not obey the triangle inequality. The triangle inequality must follow from the chosen distinguishability construction or be established as a theorem under explicit assumptions.

### 7.3 Locality

If the target is a local geometry, the reconstructed distance should be compatible with local behavior. A distance that is determined primarily by long-range entanglement may encode connectivity or global topology without defining a local Riemannian metric.

### 7.4 Scale

The reconstructed distance must have a physical scale. Quantum information measures are dimensionless, while spatial distances carry dimensions of length. A length scale must emerge from correlation decay, a coupling, a state-dependent correlation length, a calibration observable, or another declared physical quantity.

Without such a scale-setting mechanism, ECT may at best reconstruct a dimensionless geometry or a metric up to overall rescaling.

## 8. From entanglement distance to local geometry

Assume that the ECT reconstruction has produced a metric space (X,dE)(X,d_{\mathfrak E})(X,dE). The next question is whether its local structure can be represented by a Riemannian metric.

### 8.1 The infinitesimal metric

If XXX is a smooth manifold and dEd_{\mathfrak E}dE is the distance induced by a smooth Riemannian metric ggg, then in normal coordinates around ppp,

dE(p,exp⁡pv)2=gp(v,v)d_{\mathfrak E}(p,\exp_p v)^2 = g_p(v,v)dE(p,exppv)2=gp(v,v)

for sufficiently small vvv within a normal neighborhood.

In arbitrary nearby coordinates, the leading expansion is

dE(x,x+Δx)2=gμν(x)ΔxμΔxν+O(∣Δx∣3).d_{\mathfrak E}(x,x+\Delta x)^2 = g_{\mu\nu}(x)\Delta x^\mu\Delta x^\nu +O(|\Delta x|^3).dE(x,x+Δx)2=gμν(x)ΔxμΔxν+O(∣Δx∣3).

This gives an operational criterion for metric emergence: the reconstructed distance must admit a local quadratic expansion whose coefficients define a positive-definite tensor and transform appropriately under coordinate changes.

### 8.2 Curvature from distance expansion

In Riemannian normal coordinates centered at ppp, the volume density satisfies

det⁡g(x)=1−16Rij(p)xixj+O(∣x∣3),\sqrt{\det g(x)} = 1-\frac16R_{ij}(p)x^ix^j +O(|x|^3),detg(x)=1−61Rij(p)xixj+O(∣x∣3),

where the convention for the Riemann tensor is fixed as in Section 1.

Integrating over a small geodesic ball Br(p)B_r(p)Br(p) gives

Vol⁡(Br(p))=ωdrd\(1−R(p)6(d+2)r2+O(r4)\),\operatorname{Vol}(B_r(p)) = \omega_d r^d \left\( 1-\\frac{R(p)}{6(d+2)}r^2 +O(r^4) \\right\),Vol(Br(p))=ωdrd\(1−6(d+2)R(p)​r2+O(r4)\),

for a smooth ddd-dimensional Riemannian manifold, with the stated curvature convention and sufficient regularity. Here ωd\omega_dωd is the volume of the Euclidean unit ball in dimension ddd.

This equation is a useful bridge from local geometry to a scalar invariant. If ECT can reconstruct the distance and a compatible measure, it can estimate small-ball volumes and extract scalar curvature from their leading deviation from Euclidean volume growth.

The inverse procedure is conditional: one must first establish the correct dimension, the regularity of the limiting space, and the compatibility of the measure with Riemannian volume. In a singular or fractal space, the same expansion need not hold.

### 8.3 Curvature from correlation-ball growth

Let

VE(p,r)=μE({q:dE(p,q)<r})V_{\mathfrak E}(p,r) = \mu_{\mathfrak E} \bigl(\{q:d_{\mathfrak E}(p,q)<r\}\bigr)VE(p,r)=μE({q:dE(p,q)<r})

be the volume of a reconstructed ball, if a compatible measure exists.

If the continuum limit is a smooth Riemannian ddd-manifold, then the preceding expansion motivates

RE(p)=lim⁡r→06(d+2)r2\(1−VE(p,r)ωdrd\),R_{\mathfrak E}(p) = \lim_{r\to0} \frac{6(d+2)}{r^2} \left\( 1-\\frac{V\_{\\mathfrak E}(p,r)} {\\omega\_d r^d} \\right\),RE(p)=r→0limr26(d+2)\(1−ωd​rdVE​(p,r)​\),

provided the measure is the Riemannian volume measure and the limit is taken within a sufficiently regular regime.

This is not a new formula for curvature; it is the standard small-ball curvature relation recast as a target for entanglement-based reconstruction. ECT's contribution would be to prove that the correlation data generate dEd_{\mathfrak E}dE and μE\mu_{\mathfrak E}μE with the required properties.

## 9. The proposed Entanglement Curvature Reconstruction theorem

The central theorem should make clear what data are used, what geometry is reconstructed, and what equivalence class is determined.

### Definition 9.1 — Entanglement signature

Let Q\mathfrak QQ be a specified class of quantum systems with states ρ\rhoρ, subsystem family R\mathcal RR, and a fixed admissible family of correlation observables. Define the entanglement signature

IE(ρ)=({Sn(A)},{I(A:B)},{I(A:B∣C)},{Cα}),\mathfrak I_{\mathrm E}(\rho) = \left( \{S_n(A)\}, \{I(A:B)\}, \{I(A:B|C)\}, \{\mathcal C_\alpha\} \right),IE(ρ)=({Sn(A)},{I(A:B)},{I(A:B∣C)},{Cα}),

where every subsystem and observable is defined within the microscopic model.

The signature is assumed invariant under the declared equivalences of quantum description. It must not contain an explicit list of target metric components unless those components are independently part of the microscopic input.

### Theorem 9.2 — Conditional entanglement-to-curvature reconstruction

Let {ρε}\{\rho_\varepsilon\}{ρε} be a family of quantum states in a specified class Q\mathfrak QQ, with a correlation signature IE,ε\mathfrak I_{\mathrm E,\varepsilon}IE,ε. Suppose the following conditions hold.

(E1) Metric identifiability. The signature determines a nondegenerate distance dεd_\varepsilondε, uniquely up to a declared equivalence, on the reconstructed set XεX_\varepsilonXε.

(E2) Measure reconstruction. The signature or an independently justified state-dependent construction determines a measure με\mu_\varepsilonμε compatible with the distance.

(E3) Compactness and convergence. The metric-measure spaces (Xε,dε,με)(X_\varepsilon,d_\varepsilon,\mu_\varepsilon)(Xε,dε,με) converge in a specified measured geometric topology to (X,d,μ)(X,d,\mu)(X,d,μ).

(E4) Smooth regularity. The limit is a smooth ddd-dimensional Riemannian manifold, or belongs to a precisely defined class for which the intended curvature invariant exists.

(E5) Local metric compatibility. The limiting distance is induced by a Riemannian metric gEg_{\mathfrak E}gE, and the limiting measure agrees with its volume measure, or with a specified smooth density relative to it.

(E6) Correlation-to-geometry consistency. The reconstructed signature converges to the corresponding signature of the limiting geometric model within a stated error bound.

Then the limiting metric gEg_{\mathfrak E}gE and its scalar curvature R\(gE\)R\(g\_{\\mathfrak E}\)R\(gE​\) are determined uniquely up to the declared geometric equivalence. Moreover, the small-ball volume expansion recovers R\(gE\)R\(g\_{\\mathfrak E}\)R\(gE​\) by the limit in Section 8.3.

#### Proof

By (E1), the correlation signature determines the limiting distance up to the declared equivalence. By (E2), it determines the compatible measure. By (E3), these structures have a controlled continuum limit. Assumptions (E4) and (E5) ensure that the limiting distance is induced by a smooth Riemannian metric and that the measure is the corresponding volume measure. The metric is therefore uniquely determined up to the stated equivalence, and its Riemann curvature tensor and scalar curvature follow from the standard differential-geometric construction. Finally, the local small-ball volume expansion for a smooth Riemannian manifold yields the curvature formula. Assumption (E6) connects the limiting geometric invariant to the original entanglement data rather than merely to an unrelated metric. □\square□

### 9.3 What this theorem does—and does not—prove

The theorem proves a conditional implication once its hypotheses hold. It does not yet establish that any particular entanglement signature satisfies (E1)–(E6) for a nontrivial class of quantum systems.

The main open mathematical task is to construct a natural signature and prove metric identifiability without presupposing the target geometry. A complete ECT result must instantiate this theorem for a concrete model class, derive the distance and measure, and demonstrate that the reconstructed curvature agrees with an independently defined geometric or dynamical quantity.

The distinction between a conditional theorem and a proved model-specific reconstruction is essential. Otherwise, the assumptions would merely restate the desired conclusion.

## 10. A worked reconstruction model: correlation geometry on a finite quantum network

A useful first test of ECT is a finite-dimensional system where all quantities can be computed exactly. The model below is illustrative: it tests how correlation structure can define relational geometry, but it does not by itself demonstrate emergent curvature.

### 10.1 Quantum graph

Let G=(V,E)G=(V,E)G=(V,E) be a finite graph with vertices V={1,…,N}V=\{1,\ldots,N\}V={1,…,N}. Associate a finite-dimensional Hilbert space Hi\mathcal H_iHi with each vertex and define

H=⨂i=1NHi.\mathcal H=\bigotimes_{i=1}^N\mathcal H_i.H=i=1⨂NHi.

Let ρ\rhoρ be a joint quantum state. For each vertex, define the reduced state ρi\rho_iρi; for each pair, define ρij\rho_{ij}ρij. The pairwise mutual information is

Iij=S(ρi)+S(ρj)−S(ρij).I_{ij}=S(\rho_i)+S(\rho_j)-S(\rho_{ij}).Iij=S(ρi)+S(ρj)−S(ρij).

The matrix I=(Iij)I=(I_{ij})I=(Iij) is a symmetric matrix of correlation strengths, not necessarily a metric or a graph adjacency matrix.

### 10.2 From correlations to edge costs

Choose a fixed, declared monotone transformation φ\varphiφ and define edge costs

wij=φ(Iij)w_{ij}=\varphi(I_{ij})wij=φ(Iij)

for the allowed edges. For example, a positive cost may be defined from a regularized decreasing function of mutual information. The exact transformation must be selected before examining the reconstructed geometry.

If wij≥0w_{ij}\geq0wij≥0, define the shortest-path distance

dG(i,j)=inf⁡γ:i⇝j∑(u,v)∈γwuv.d_G(i,j) = \inf_{\gamma:i\leadsto j} \sum_{(u,v)\in\gamma}w_{uv}.dG(i,j)=γ:i⇝jinf(u,v)∈γ∑wuv.

For a connected graph with strictly positive edge costs, dGd_GdG is a metric on the vertices. If the graph is disconnected, the distance between components is infinite unless a further convention is supplied.

The important limitation is that the shortest-path construction assumes a graph of allowed edges. It reconstructs a metric from the graph and its correlation-derived costs; it does not prove that the graph itself emerges from entanglement.

### 10.3 Testing the curvature limit

For each vertex iii, define a graph ball

Br(i)={j:dG(i,j)<r}.B_r(i)=\{j:d_G(i,j)<r\}.Br(i)={j:dG(i,j)<r}.

A discrete ball-volume estimator can be built from vertex weights or a measure μ(i)\mu(i)μ(i):

VG(i,r)=∑j∈Br(i)μ(j).V_G(i,r)=\sum_{j\in B_r(i)}\mu(j).VG(i,r)=j∈Br(i)∑μ(j).

One can then compare the measured volume-growth law against the Euclidean and constant-curvature reference laws. On a sequence of increasingly refined graphs, the question is whether a properly normalized estimator converges to a known curvature invariant.

This requires care. The discrete neighborhood of a vertex changes in jumps as rrr crosses edge distances; the measure must scale correctly with refinement; and graph curvature definitions are not interchangeable with Riemannian scalar curvature.

A successful finite-network experiment should therefore report three distinct results:

1. whether the correlation transformation produces a valid metric;

2. whether the metric exhibits a stable continuum scaling regime;

3. whether the limiting curvature estimator agrees with an independently known geometric target.

Only the third result, together with the necessary convergence proof, would support a claim of curvature reconstruction.

## 11. An exactly solvable example: a pure bipartite state

Consider a bipartite pure state in Schmidt form,

∣Ψ⟩=∑k=1rpk ∣k⟩A∣k⟩B,pk≥0,∑kpk=1.|\Psi\rangle = \sum_{k=1}^{r}\sqrt{p_k}\, |k\rangle_A|k\rangle_B, \qquad p_k\geq0,\qquad \sum_k p_k=1.∣Ψ⟩=k=1∑rpk∣k⟩A∣k⟩B,pk≥0,k∑pk=1.

The reduced density operators are

ρA=∑kpk∣k⟩⟨k∣,ρB=∑kpk∣k⟩⟨k∣.\rho_A=\sum_kp_k|k\rangle\langle k|, \qquad \rho_B=\sum_kp_k|k\rangle\langle k|.ρA=k∑pk∣k⟩⟨k∣,ρB=k∑pk∣k⟩⟨k∣.

Consequently,

S(A)=S(B)=−∑kpkln⁡pk.S(A)=S(B)=-\sum_kp_k\ln p_k.S(A)=S(B)=−k∑pklnpk.

Because the joint state is pure, S(AB)=0S(AB)=0S(AB)=0, and therefore

I(A:B)=2S(A).I(A:B)=2S(A).I(A:B)=2S(A).

This exact result shows that the entropy measures the amount of bipartite entanglement in the pure state. It does not tell us the spatial distance between AAA and BBB.

For example, the same Schmidt coefficients can occur in systems whose subsystems are interpreted as neighboring sites, distant sites, or abstract internal degrees of freedom. The reduced-state spectra alone do not distinguish those interpretations.

The example isolates the central issue: entanglement magnitude is a property of a quantum state and a partition; distance and curvature require additional relational organization.

## 12. Entanglement inequalities as geometric consistency conditions

A proposed entanglement geometry must preserve the fundamental constraints of quantum information. These constraints can act as consistency tests for candidate geometric reconstructions.

### 12.1 Subadditivity

For subsystems AAA and BBB,

S(AB)≤S(A)+S(B).S(AB)\leq S(A)+S(B).S(AB)≤S(A)+S(B).

Equivalently, I(A:B)≥0I(A:B)\geq0I(A:B)≥0. A reconstruction using mutual information must respect this nonnegativity.

### 12.2 Strong subadditivity

For three subsystems,

S(AB)+S(BC)≥S(B)+S(ABC).S(AB)+S(BC)\geq S(B)+S(ABC).S(AB)+S(BC)≥S(B)+S(ABC).

Equivalently,

I(A:C∣B)≥0.I(A:C|B)\geq0.I(A:C∣B)≥0.

This inequality is universal for ordinary finite-dimensional quantum states. In holographic theories, additional entropy inequalities and relations can arise from the geometric prescription.

![](https://www.google.com/s2/favicons?domain=https://arxiv.org\&sz=32)

arXiv

+1

### 12.3 Why entropy inequalities are not sufficient for geometry

Quantum entropy inequalities constrain allowed correlation data, but they do not by themselves establish that a metric exists. A collection of numbers can satisfy subadditivity and strong subadditivity without defining pairwise distances that obey the triangle inequality, let alone a smooth metric with a well-defined curvature tensor.

ECT should therefore treat quantum entropy inequalities as necessary consistency conditions on its inputs, not as a substitute for the metric reconstruction theorem.

### 12.4 Conditional independence and geometric separation

If I(A:C∣B)=0I(A:C|B)=0I(A:C∣B)=0, the state has a quantum Markov property for the relevant tripartition, under the standard finite-dimensional formulation. This can indicate that BBB screens certain correlations between AAA and CCC.

Such screening may be useful in identifying candidate separators or locality structures. But conditional independence does not universally mean that BBB lies spatially between AAA and CCC. The interpretation requires a model-specific theorem.

## 13. From curvature reconstruction to gravitational dynamics

Even if ECT successfully reconstructs a metric and scalar curvature, it has not yet derived gravity.

A geometric invariant describes the structure of a metric. A gravitational field equation describes how that metric responds to sources and admissible variations. The second statement requires a dynamical principle.

In holographic settings, there are important results linking the first law of entanglement and relative entropy to gravitational equations under specific assumptions. In particular, the derivation of linearized gravitational equations relies on the holographic entropy-area relation and a specified bulk gravitational framework.

![](https://www.google.com/s2/favicons?domain=https://arxiv.org\&sz=32)

arXiv

+1

ECT may seek a broader result, but it cannot claim that arbitrary entanglement entropy generates Einstein's equations.

### 13.1 First law of entanglement

For a reference state σA\sigma_AσA, define its modular Hamiltonian

KA=−ln⁡σA.K_A=-\ln\sigma_A.KA=−lnσA.

For a sufficiently small perturbation of the state, the first-order variation of the entropy obeys

δSA=δ⟨KA⟩.\delta S_A=\delta\langle K_A\rangle.δSA=δ⟨KA⟩.

This is the entanglement first law. It follows from the first-order variation of von Neumann entropy around a fixed reference state.

To obtain a gravitational equation, one must identify the modular-energy variation with the corresponding bulk quantities, use a valid entropy-area relation, and establish the relevant geometric identities. Those steps are not supplied by the first law alone.

### 13.2 Relative entropy

For states ρA\rho_AρA and σA\sigma_AσA, define

D(ρA∥σA)=Tr⁡\(ρA(ln⁡ρA−ln⁡σA)\).D(\rho_A\Vert\sigma_A) = \operatorname{Tr} \left\( \\rho\_A(\\ln\\rho\_A-\\ln\\sigma\_A) \\right\).D(ρA∥σA)=Tr\(ρA​(lnρA​−lnσA​)\).

Relative entropy is nonnegative when defined and finite. It combines changes in modular energy with changes in entropy and can encode more information than entropy differences alone.

In suitable holographic code-subspace settings, relative-entropy relations help connect boundary distinguishability with bulk reconstruction and gravitational perturbations. These results depend on the holographic dictionary and its assumptions; they do not imply that any abstract relative-entropy matrix determines a unique metric.

![](https://www.google.com/s2/favicons?domain=https://link.springer.com\&sz=32)

Springer Nature Link

+1

### 13.3 ECT's separate dynamical target

A genuine entanglement-derived gravity model would need to specify:

* the microscopic quantum degrees of freedom and their dynamics;

* the state space and allowed variations;

* the reconstruction map to the emergent metric;

* an effective action or equivalent dynamical law;

* the matter sector and its coupling to the emergent geometry;

* the convergence regime in which the resulting equations hold.

Only then can one ask whether the limiting equations reproduce Einstein gravity, a modified gravitational theory, or no local gravitational dynamics at all.

## 14. The nonuniqueness problem

The central obstacle in ECT is that entanglement data do not uniquely determine a spacetime without additional conditions.

### 14.1 State nonuniqueness

Different global states can have the same reduced entropies for a selected collection of subsystems. Even a large set of entropy values need not determine all phases, observables, or correlation functions of the state.

### 14.2 Partition nonuniqueness

The meaning of a subsystem depends on the factorization or algebraic decomposition used to define it. Different decompositions can assign different entropies to what might otherwise be described as the same physical system.

### 14.3 Geometric nonuniqueness

Different geometries may reproduce the same subset of entanglement observables. In holographic reconstruction, the ability to infer bulk geometry depends on which boundary regions are available, which extremal surfaces they probe, and what assumptions restrict the bulk theory.

### 14.4 Scale and normalization ambiguity

If the entanglement data determine only ratios or dimensionless quantities, an overall length scale may remain undetermined. Curvature has dimensions of inverse length squared, so absolute curvature cannot be recovered without fixing that scale.

### 14.5 The circularity test

A reconstruction is not explanatory if it inserts the desired geometry into the definition of the entanglement signature. For example, defining subsystem distances by the geodesic distances of a target metric and then recovering that metric from those distances is tautological.

The theory must instead demonstrate that the signature is defined from independent microscopic data and that the target geometry follows as a theorem.

## 15. Stability and finite-data reconstruction

An exact theorem for idealized infinite data may still be physically uninformative if the reconstruction is unstable.

Let IE\mathfrak I_{\mathrm E}IE be the entanglement signature and let dEd_{\mathrm E}dE quantify discrepancies between signatures. A stable reconstruction would satisfy

dgeom(G(ρ1),G(ρ2))≤Ω ⁣(dE(IE(ρ1),IE(ρ2))),d_{\mathrm{geom}} \bigl(\mathfrak G(\rho_1),\mathfrak G(\rho_2)\bigr) \leq \Omega\!\left( d_{\mathrm E} \bigl(\mathfrak I_{\mathrm E}(\rho_1), \mathfrak I_{\mathrm E}(\rho_2)\bigr) \right),dgeom(G(ρ1),G(ρ2))≤Ω(dE(IE(ρ1),IE(ρ2))),

where Ω(ϵ)→0\Omega(\epsilon)\to0Ω(ϵ)→0 as ϵ→0\epsilon\to0ϵ→0.

The geometric discrepancy may be a distance between metric-measure spaces or a suitable norm on metrics modulo diffeomorphisms. The choice must be stated, not left implicit.

### 15.1 Sources of instability

* Near-degenerate correlation patterns;

* entropies measured with finite precision;

* small subsystems that do not resolve the intended scale;

* changes in subsystem factorization;

* phase transitions in the dominant geometric reconstruction;

* correlation decay that is too weak to fix a stable distance;

* incomplete access to the required subsystem family.

### 15.2 A practical reconstruction protocol

A computational ECT model should fix its reconstruction map before fitting to a target geometry. It should then test the map on synthetic quantum states whose geometric targets are independently known, perturb the state or correlation data, and quantify the resulting geometric error.

The critical output is not simply a visually plausible curved embedding. It is an error-controlled statement relating uncertainty in the quantum data to uncertainty in the reconstructed metric and curvature.

## 16. A falsifiable research program

ECT should advance through a sequence of tests in which each stage can fail independently.

Stage I — Quantum-state specification

Choose a concrete model, define its subsystem algebra, and calculate the entropies and correlation observables exactly or with controlled approximation.

Stage II — Relational reconstruction

Construct a candidate distance from a predeclared correlation rule. Prove positivity, symmetry, nondegeneracy, and the triangle inequality, or characterize the resulting pseudometric.

Stage III — Metric-measure limit

Show that a sequence of systems converges to a metric-measure space, with explicit scaling and error estimates.

Stage IV — Curvature identification

Recover curvature from local distance or volume data and compare it with an independent geometric benchmark. Demonstrate stability under controlled perturbations.

Stage V — Gravitational dynamics

If gravity is claimed, derive an effective dynamical law and establish its continuum limit. Metric reconstruction alone does not satisfy this stage.

### 16.1 Minimum decisive experiment

A first serious ECT result should use a quantum system with a known target geometry, such as a controlled family of quantum states on a lattice approximating a smooth space.

The protocol should:

1. Specify the state, Hamiltonian or preparation procedure, and subsystem family.

2. Define the correlation signature and distance rule without using the target metric.

3. Reconstruct the distance and estimate curvature.

4. Repeat the reconstruction at multiple lattice resolutions.

5. Compare the result with the known continuum curvature.

6. Perturb the quantum state and measure the stability of the reconstructed geometry.

7. Test a competing state or geometry that shares the basic entropy data.

A successful result would establish more than a correlation between entropy and curvature. It would show that a fixed, independently specified quantum-information procedure reconstructs the correct geometric invariant with controlled error.

## 17. Principal conjectures

The framework suggests several conjectures, each requiring separate proof.

Conjecture 17.1 — Entanglement metric completeness. For a nontrivial class of quantum states with a suitable locality structure, an enriched entanglement signature determines a metric-measure space up to the declared equivalence.

Conjecture 17.2 — Curvature recoverability. If the reconstructed metric-measure spaces converge to a sufficiently regular Riemannian manifold and the reconstructed measure agrees with Riemannian volume, the scalar curvature is recoverable from local correlation-ball volume data.

The geometric portion of this statement follows from established small-ball asymptotics. The unresolved part is whether the required metric and measure emerge from the specified entanglement signature.

Conjecture 17.3 — Holographic compatibility. In a class of semiclassical holographic states, an ECT reconstruction based on a sufficiently rich boundary entanglement signature agrees, within controlled corrections, with the geometry inferred through the appropriate extremal-surface prescription.

Conjecture 17.4 — Dynamical universality. A restricted class of microscopic quantum models may produce a common low-energy gravitational regime despite differences in microscopic entanglement structure.

This last conjecture is the most ambitious. It requires a dynamical universality theorem and cannot be inferred from geometric reconstruction alone.

## 18. Epistemic audit

| Claim                                                                                           | Status                                                |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| Von Neumann entropy measures reduced-state mixedness                                            | Established                                           |
| Mutual information measures total correlations                                                  | Established                                           |
| Entanglement entropy is related to extremal-surface area in suitable holographic settings       | Established within the relevant holographic framework |
| Entanglement data can constrain geometric structure in particular models                        | Established in selected settings                      |
| Entropy alone determines a unique spacetime                                                     | Not established; false as a universal claim           |
| The proposed enriched ECT signature reconstructs a unique metric for a nontrivial general class | Open                                                  |
| The reconstructed metric's curvature follows from its local distance structure                  | Established once the required smooth metric exists    |
| Curvature is universally determined by entanglement without additional structure                | Not established                                       |
| Einstein's equations follow from arbitrary entanglement patterns                                | Not established                                       |
| A specific ECT microscopic model converges to a known gravitational regime                      | Requires a model-specific derivation                  |

The framework has a sound mathematical starting point, but its novelty depends on a concrete inverse theorem. The use of entanglement entropy, mutual information, and information geometry is not itself new. The distinctive ECT contribution would be a noncircular, identifiable, and stable reconstruction procedure that proves when these quantities determine a geometric curvature invariant.

## 19. Conclusion

The Entanglement Curvature Theory proposes that curvature may be reconstructed from the structure of quantum correlations. Its strongest mathematical route is to avoid identifying entropy directly with curvature and instead establish a chain of rigorously defined maps:

Quantum state and subsystem algebra⇓Enriched entanglement signature⇓Reconstructed distance and measure⇓Metric-measure continuum⇓Riemannian metric⇓Curvature invariants⇓Possible gravitational dynamics.\boxed{ \begin{aligned} &\text{Quantum state and subsystem algebra}\\ &\quad\Downarrow\\ &\text{Enriched entanglement signature}\\ &\quad\Downarrow\\ &\text{Reconstructed distance and measure}\\ &\quad\Downarrow\\ &\text{Metric-measure continuum}\\ &\quad\Downarrow\\ &\text{Riemannian metric}\\ &\quad\Downarrow\\ &\text{Curvature invariants}\\ &\quad\Downarrow\\ &\text{Possible gravitational dynamics}. \end{aligned} }Quantum state and subsystem algebra⇓Enriched entanglement signature⇓Reconstructed distance and measure⇓Metric-measure continuum⇓Riemannian metric⇓Curvature invariants⇓Possible gravitational dynamics.

The first stages are quantum-information constructions; the middle stages are inverse geometry; the final stage is a separate problem in mathematical physics. Each transition must be justified by its own assumptions and proof.

The central reconstruction theorem formulated here states that if an enriched entanglement signature uniquely determines a metric-measure structure, if that structure converges to a sufficiently regular manifold, and if its measure is compatible with the reconstructed metric, then the scalar curvature is uniquely recoverable from the limiting geometry. The theorem identifies a precise target, but a complete ECT result still requires an explicit quantum model in which the assumptions are proved rather than postulated.

The central obstacle remains nonuniqueness. Entanglement is relational, but not every relational pattern is spatial; entropy constrains geometry, but does not automatically determine it. A convincing theory must establish which additional correlation observables resolve the ambiguity, how they generate a local metric, and whether the reconstruction survives finite precision and continuum refinement.

The strongest defensible thesis is therefore:

Quantum entanglement may be a source of geometric information, and in a suitably restricted class of quantum systems it may suffice to reconstruct curvature. But entanglement becomes a theory of geometry only when the map from correlations to distance is proved, and it becomes a theory of gravity only when the reconstructed geometry is supplied with an independently derived dynamical law.

# The Universal Spectral Structure Theory

## An Inverse-Spectral Framework for Reconstructing Geometry, Dynamics, and Hidden Structure from Operator Data

Research preprint · October 16, 2026 · Spectral geometry, operator theory, inverse problems, and mathematical physics

## Abstract

The Universal Spectral Structure Theory (USST) investigates the extent to which the spectrum of an operator encodes the geometric, topological, and dynamical structure from which that operator arises. Its starting point is the heat trace

K(t)=Tr⁡(e−tL)=∑ne−tλn,t&gt;0,K(t)=\operatorname{Tr}(e^{-tL}) =\sum_n e^{-t\lambda_n}, \qquad t>0,K(t)=Tr(e−tL)=n∑e−tλn,t&gt;0,

where LLL is an operator with discrete spectrum {λn}\{\lambda_n\}{λn}, counted with multiplicity, and ttt is a spectral scale parameter. In established settings, the short-time asymptotics of K(t)K(t)K(t) encode dimension, volume, curvature integrals, and boundary data. Yet spectral information is not universally complete: non-isometric spaces can be isospectral, and operators with identical eigenvalues can possess different eigenfunctions, local geometric structures, or dynamics.

USST treats this nonuniqueness as the central mathematical problem rather than an exception to be ignored. The objective is to construct an enriched spectral invariant that distinguishes a specified class of structures left unresolved by the eigenvalue spectrum alone.

The proposed invariant is the Spectral Response Signature (SRS), built from the joint response of eigenvalues and spectral projectors to a controlled family of perturbations. For a self-adjoint operator LLL and admissible perturbations VaV_aVa, the basic response data include the first and higher derivatives of the heat trace,

Ra(t)=−∂∂εTr⁡e−t(L+εVa)∣ε=0,\mathcal R_a(t) = -\left.\frac{\partial}{\partial\varepsilon} \operatorname{Tr} e^{-t(L+\varepsilon V_a)} \right|_{\varepsilon=0},Ra(t)=−∂ε∂Tre−t(L+εVa)ε=0,

together with mixed responses, spectral-projector information, and the symmetry class of the perturbation family. These data preserve the advantages of heat-trace analysis while probing how the spectrum is embedded in the operator's surrounding structure.

A conditional separation theorem is established for a specified operator class: if two operators have identical unperturbed spectra but differ in their joint spectral-projector responses to a complete, geometrically meaningful perturbation family, then their enriched spectral signatures distinguish them. This is a separation result relative to the chosen perturbations, not a universal claim that every isospectral pair can be distinguished. The paper identifies the additional conditions required for the invariant to be geometrically meaningful, stable, and independent of arbitrary basis choices.

The framework also develops a hierarchy of spectral reconstruction, from scalar heat traces to weighted traces, perturbative response functions, eigenfunction-sensitive data, and dynamical propagators. It separates proven spectral facts from proposed extensions and establishes a research program for testing USST against explicit isospectral examples.

Keywords: inverse spectral geometry; heat kernel; isospectral manifolds; spectral projectors; perturbation theory; heat invariants; operator algebras; eigenfunction correlations; inverse problems; spectral response.

## 1. Introduction: What Does a Spectrum Remember?

A spectrum is one of the most compressed representations of a mathematical structure. Given an operator LLL, its eigenvalues may summarize geometric constraints, dynamical modes, boundary conditions, and global structural information. In many settings, spectral data reveal features that are not immediately apparent from the original equations.

For a positive self-adjoint elliptic operator on a compact space, the heat trace

K(t)=Tr⁡(e−tL)(1.1)K(t)=\operatorname{Tr}(e^{-tL}) \tag{1.1}K(t)=Tr(e−tL)(1.1)

provides a bridge between spectral and geometric descriptions. At large ttt, it emphasizes low-energy modes. At small ttt, it probes the high-frequency spectrum and exposes local geometric invariants through its asymptotic expansion.

This connection motivates a natural inverse problem:

> Given the spectrum of an operator, how much of the structure that generated it can be reconstructed?

The question is not answered by the spectrum alone in every case. Isospectral non-isometric manifolds demonstrate that even complete eigenvalue data, including multiplicities, need not determine a unique geometry. More generally, different operators may share spectral data while differing in their eigenvectors, symmetry representations, local response, or dynamical interpretation.

The Universal Spectral Structure Theory proposes that the appropriate object for reconstruction is not always the bare spectrum. It may instead be a structured family of spectral responses that records how the operator behaves under a controlled set of probes.

The goal is to determine whether this enrichment can resolve a clearly specified class of inverse-spectral ambiguities.

### 1.1 The central hypothesis

Let C\mathcal CC be a class of admissible structures and let

S:C⟶D(1.2)\mathfrak S:\mathcal C\longrightarrow\mathfrak D \tag{1.2}S:C⟶D(1.2)

map each structure to its spectral data.

If S\mathfrak SS is not injective, there exist distinct structures X,Y∈CX,Y\in\mathcal CX,Y∈C such that

S(X)=S(Y),X≇Y,(1.3)\mathfrak S(X)=\mathfrak S(Y), \qquad X\not\cong Y, \tag{1.3}S(X)=S(Y),X≅Y,(1.3)

where ≅\cong≅ denotes the declared notion of structural equivalence.

USST seeks an enriched map

Senr:C⟶Denr(1.4)\mathfrak S_{\mathrm{enr}}: \mathcal C\longrightarrow\mathfrak D_{\mathrm{enr}} \tag{1.4}Senr:C⟶Denr(1.4)

such that

Senr(X)=Senr(Y)⟹X≅Y(1.5)\mathfrak S_{\mathrm{enr}}(X) = \mathfrak S_{\mathrm{enr}}(Y) \quad\Longrightarrow\quad X\cong Y \tag{1.5}Senr(X)=Senr(Y)⟹X≅Y(1.5)

for a specified class of structures.

Equation (1.5) is the target, not a universal theorem assumed at the outset. Its validity depends on the chosen structure class, the additional spectral data, and the equivalence relation.

### 1.2 The central methodological constraint

An inverse-spectral invariant cannot be declared successful merely because it contains more information than the eigenvalue list. It must satisfy four requirements:

1. Well-definedness: the invariant is mathematically defined for the stated class.

2. Invariance: it is unchanged under the equivalences it is intended to ignore.

3. Discrimination: it distinguishes at least one explicitly identified class of structures that the original spectrum cannot distinguish.

4. Reconstruction scope: the precise class on which it is sufficient is stated and justified.

The theory will therefore proceed from established heat-trace results to a proposed response invariant, a conditional separation theorem, and a sequence of reconstruction problems.

## 2. Mathematical Setup: Operators, Spectra, and Equivalence

### 2.1 The operator class

Let H\mathcal HH be a separable Hilbert space, and let

L:D(L)⊆H→H(2.1)L:\mathcal D(L)\subseteq\mathcal H\to\mathcal H \tag{2.1}L:D(L)⊆H→H(2.1)

be a self-adjoint operator bounded below. For the initial theory, assume that LLL has compact resolvent, so its spectrum consists of isolated real eigenvalues of finite multiplicity,

λ0≤λ1≤λ2≤⋯ ,λn→+∞,(2.2)\lambda_0\leq\lambda_1\leq\lambda_2\leq\cdots, \qquad \lambda_n\to+\infty, \tag{2.2}λ0≤λ1≤λ2≤⋯,λn→+∞,(2.2)

where eigenvalues are repeated according to multiplicity.

When LLL is positive and e−tLe^{-tL}e−tL is trace-class for every t&gt;0t>0t&gt;0, the heat trace is well-defined:

KL(t)=Tr⁡(e−tL)=∑n=0∞e−tλn.(2.3)K_L(t)=\operatorname{Tr}(e^{-tL}) =\sum_{n=0}^{\infty}e^{-t\lambda_n}. \tag{2.3}KL(t)=Tr(e−tL)=n=0∑∞e−tλn.(2.3)

More generally, if LLL is only bounded below, a constant shift can make it nonnegative without changing its eigenspaces. The shift changes the heat trace by a known exponential factor and must be recorded when comparing operators.

The compact-resolvent assumption covers many elliptic operators on compact manifolds and finite-dimensional discretizations. It does not cover every operator relevant to physics. Continuous spectra require spectral measures and regularized traces; those extensions are discussed later.

### 2.2 The spectrum as a measure

The eigenvalue list can be represented by the spectral counting measure

dNL(λ)=∑nδ(λ−λn) dλ.(2.4)dN_L(\lambda) = \sum_n\delta(\lambda-\lambda_n)\,d\lambda. \tag{2.4}dNL(λ)=n∑δ(λ−λn)dλ.(2.4)

Then

KL(t)=∫Re−tλ dNL(λ).(2.5)K_L(t)= \int_{\mathbb R}e^{-t\lambda}\,dN_L(\lambda). \tag{2.5}KL(t)=∫Re−tλdNL(λ).(2.5)

The heat trace is therefore a Laplace transform of the spectral measure. Under suitable growth and domain conditions, knowing KL(t)K_L(t)KL(t) for all t&gt;0t>0t&gt;0 determines the eigenvalue measure, including multiplicities.

This fact clarifies an important limitation: the heat trace does not contain less eigenvalue information than the complete spectrum when known exactly for every positive ttt. Any new invariant intended to distinguish isospectral structures must add information not already determined by NLN_LNL.

### 2.3 Isospectrality and geometric equivalence

Two operators LXL_XLX and LYL_YLY are isospectral if their spectra agree with multiplicities:

Spec⁡(LX)=Spec⁡(LY).(2.6)\operatorname{Spec}(L_X) = \operatorname{Spec}(L_Y). \tag{2.6}Spec(LX)=Spec(LY).(2.6)

For Laplace operators on compact Riemannian manifolds XXX and YYY, this means the manifolds have identical Laplace eigenvalue lists.

An isometry F:X→YF:X\to YF:X→Y induces a unitary map between the corresponding L2L^2L2 spaces that intertwines the Laplace operators. Hence isometric manifolds are isospectral under the standard assumptions.

The converse is false: isospectral non-isometric manifolds exist.

The inverse problem is thus naturally phrased in terms of equivalence classes. If C\mathcal CC is a class of geometric structures, the desired reconstruction is not necessarily a unique coordinate representation, but a unique equivalence class

\(X\)={Y∈C:Y≅X}.(2.7)\(X\)=\{Y\in\mathcal C:Y\cong X\}. \tag{2.7}\(X\)={Y∈C:Y≅X}.(2.7)

The relation ≅\cong≅ must be specified in advance. Depending on the application, it may mean isometry, unitary equivalence, equivalence of a marked geometry, or equivalence preserving additional fields and boundary data.

### 2.4 What counts as additional spectral information?

An enriched spectral invariant may incorporate data such as:

* eigenvalues and multiplicities;

* spectral projectors;

* traces weighted by specified operators;

* joint responses to perturbations;

* symmetry representations on eigenspaces;

* localized or marked heat kernels;

* eigenfunction correlations;

* resolvent matrix elements;

* time-dependent propagators.

These are not interchangeable. Each reveals a different aspect of the operator.

The central design problem is to choose additional information that is sufficient for a target reconstruction class without simply encoding the entire original geometry by hand.

## 3. The Heat Trace and Its Geometric Content

### 3.1 The short-time expansion

Let (M,g)(M,g)(M,g) be a compact ddd-dimensional Riemannian manifold without boundary, and let

L=−Δg(3.1)L=-\Delta_g \tag{3.1}L=−Δg(3.1)

be the nonnegative Laplace–Beltrami operator, with sign convention chosen so that its spectrum is nonnegative.

As t↓0t\downarrow0t↓0, the heat trace has an asymptotic expansion of the form

KL(t)∼1(4πt)d/2∑j=0∞aj(L)tj.(3.2)K_L(t) \sim \frac{1}{(4\pi t)^{d/2}} \sum_{j=0}^{\infty}a_j(L)t^j. \tag{3.2}KL(t)∼(4πt)d/21j=0∑∞aj(L)tj.(3.2)

For the scalar Laplacian on a closed manifold, the first coefficients include

a0(L)=Vol⁡(M,g),(3.3)a_0(L)=\operatorname{Vol}(M,g), \tag{3.3}a0(L)=Vol(M,g),(3.3)

and

a1(L)=16∫MRg dvol⁡g,(3.4)a_1(L)=\frac16\int_M R_g\,d\operatorname{vol}_g, \tag{3.4}a1(L)=61∫MRgdvolg,(3.4)

where RgR_gRg is scalar curvature.

Higher coefficients involve integrals of curvature polynomials and their covariant derivatives. For manifolds with boundary, the expansion generally includes additional boundary terms and may contain half-integer powers of ttt.

The exact coefficient formulas depend on the operator, the bundle, the potential, the boundary conditions, and the chosen sign conventions.

### 3.2 What the heat coefficients determine

The heat coefficients can reveal:

* the dimension of the manifold;

* its volume;

* integrated curvature information;

* certain combinations of higher curvature invariants;

* boundary contributions;

* properties of lower-order terms in Laplace-type operators.

But integrated invariants do not generally determine the full pointwise geometry. Different structures may share the same values of many or all heat coefficients.

Moreover, the heat expansion is asymptotic. Equality of every coefficient does not, in general, imply equality of the full heat trace, and equality of the heat trace does not imply isometry.

### 3.3 The heat kernel contains more information than the heat trace

The heat operator e−tLe^{-tL}e−tL has an integral kernel HL(t;x,y)H_L(t;x,y)HL(t;x,y), under the usual elliptic assumptions:

(e−tLf)(x)=∫MHL(t;x,y)f(y) dvol⁡g(y).(3.5)(e^{-tL}f)(x) = \int_M H_L(t;x,y)f(y)\,d\operatorname{vol}_g(y). \tag{3.5}(e−tLf)(x)=∫MHL(t;x,y)f(y)dvolg(y).(3.5)

The heat trace is its diagonal integral:

KL(t)=∫MHL(t;x,x) dvol⁡g(x).(3.6)K_L(t)= \int_M H_L(t;x,x)\,d\operatorname{vol}_g(x). \tag{3.6}KL(t)=∫MHL(t;x,x)dvolg(x).(3.6)

This operation discards the spatial location of the diagonal values and all off-diagonal information. A marked heat kernel retains information that a scalar trace averages away.

This suggests a hierarchy:

eigenvalues⟶heat trace⟶weighted traces⟶marked kernels and joint responses.(3.7)\text{eigenvalues} \longrightarrow \text{heat trace} \longrightarrow \text{weighted traces} \longrightarrow \text{marked kernels and joint responses}. \tag{3.7}eigenvalues⟶heat trace⟶weighted traces⟶marked kernels and joint responses.(3.7)

The arrows indicate possible enrichments of data, not a claim that every item in the hierarchy is reconstructible from the previous one. In particular, the heat trace and eigenvalue list contain equivalent information when the trace is known exactly for all t&gt;0t>0t&gt;0.

### 3.4 Large-time behavior

If the lowest eigenvalue is λ0\lambda_0λ0 with multiplicity m0m_0m0, then

KL(t)=m0e−tλ0\(1+O ⁣(e−t(λm0−λ0))\)(3.8)K_L(t) = m_0e^{-t\lambda_0} \left\( 1+O\\!\\left(e^{-t(\\lambda\_{m\_0}-\\lambda\_0)}\\right) \\right\) \tag{3.8}KL(t)=m0e−tλ0\(1+O(e−t(λm0​​−λ0​))\)(3.8)

when there is a positive gap to the next distinct eigenvalue.

Thus, large ttt emphasizes the low-energy spectrum, while small ttt samples the high-energy spectrum. Together, these regimes provide complementary information, but neither automatically resolves isospectral ambiguity.

## 4. Why the Spectrum Alone Cannot Reconstruct Every Structure

### 4.1 Isospectral non-isometric manifolds

The existence of isospectral non-isometric manifolds establishes a basic obstruction to universal reconstruction from Laplace eigenvalues alone.

If

Spec⁡(ΔgX)=Spec⁡(ΔgY),X≇Y,(4.1)\operatorname{Spec}(\Delta_{g_X}) = \operatorname{Spec}(\Delta_{g_Y}), \qquad X\not\cong Y, \tag{4.1}Spec(ΔgX)=Spec(ΔgY),X≅Y,(4.1)

then every scalar spectral function determined only by the eigenvalue list agrees for the two manifolds. In particular,

KX(t)=KY(t)for every t&gt;0.(4.2)K_X(t)=K_Y(t) \quad\text{for every }t>0. \tag{4.2}KX(t)=KY(t)for every t&gt;0.(4.2)

Consequently, any proposed invariant of the form

I(X)=F(Spec⁡(ΔgX))(4.3)I(X)=F\big(\operatorname{Spec}(\Delta_{g_X})\big) \tag{4.3}I(X)=F(Spec(ΔgX))(4.3)

must also agree on this pair. No manipulation of the same eigenvalue list can distinguish the structures.

This is a mathematical impossibility result, not merely a limitation of current computational methods.

### 4.2 Eigenvalues do not specify eigenfunctions

An operator contains both eigenvalues and eigenspaces. Its spectral decomposition is

L=∑λ∈Spec⁡(L)λPλ,(4.4)L=\sum_{\lambda\in\operatorname{Spec}(L)} \lambda P_\lambda, \tag{4.4}L=λ∈Spec(L)∑λPλ,(4.4)

where PλP_\lambdaPλ is the orthogonal projector onto the eigenspace corresponding to λ\lambdaλ.

The eigenvalue list records the scalar labels λ\lambdaλ and the ranks of PλP_\lambdaPλ, but not the embedding of those subspaces in H\mathcal HH.

Two operators can have the same eigenvalues and multiplicities while their spectral projectors differ relative to a common family of physically meaningful observables or probes.

The qualification “relative to” matters. If arbitrary unitary transformations are treated as equivalences, then a change of basis alone is not a meaningful distinction. An enriched invariant must be constructed from data that transform correctly under the equivalences the theory intends to preserve.

### 4.3 The inverse problem is underdetermined

The map from geometry to spectrum is many-to-one on sufficiently broad classes. A successful reconstruction theory must therefore either:

1. restrict the admissible class until the spectrum becomes determining; or

2. add data that separate the structures within the intended class.

USST pursues the second strategy while allowing the first when necessary.

The aim is not to invent a universal scalar that defeats every possible isospectral construction. The aim is to establish a controlled reconstruction theorem for a declared class.

## 5. The Proposed Invariant: Spectral Response Signature

The central proposal is to enrich the spectrum with its response to a family of admissible operator perturbations.

### 5.1 Perturbed operators

Let LLL be self-adjoint and bounded below with compact resolvent. Let

V={Va:a∈A}(5.1)\mathcal V=\{V_a:a\in A\} \tag{5.1}V={Va:a∈A}(5.1)

be a specified family of self-adjoint perturbations. For bounded VaV_aVa, define

L(ε)=L+∑a∈A0εaVa,(5.2)L(\boldsymbol\varepsilon) = L+\sum_{a\in A_0}\varepsilon_aV_a, \tag{5.2}L(ε)=L+a∈A0∑εaVa,(5.2)

where A0⊂AA_0\subset AA0⊂A is finite and the parameters εa\varepsilon_aεa lie in a neighborhood of zero where the relevant operator family is well-defined.

For unbounded perturbations, additional domain and relative-boundedness assumptions are required.

The perturbed heat trace is

K(t;ε)=Tr⁡exp⁡\(−t(L+∑aεaVa)\).(5.3)K(t;\boldsymbol\varepsilon) = \operatorname{Tr} \exp\left\( -t\\left(L+\\sum\_a\\varepsilon\_aV\_a\\right) \\right\). \tag{5.3}K(t;ε)=Trexp\(−t(L+a∑​εa​Va​)\).(5.3)

The Spectral Response Signature is the family of derivatives of this function at zero perturbation, supplemented when necessary by projector and symmetry data.

### 5.2 First-order response

For a bounded perturbation VVV, Duhamel's formula gives

ddεe−t(L+εV)∣ε=0=−∫0te−(t−s)LVe−sL ds.(5.4)\left.\frac{d}{d\varepsilon} e^{-t(L+\varepsilon V)} \right|_{\varepsilon=0} = -\int_0^t e^{-(t-s)L}Ve^{-sL}\,ds. \tag{5.4}dεde−t(L+εV)ε=0=−∫0te−(t−s)LVe−sLds.(5.4)

Taking the trace and using cyclicity yields

ddεK(t;ε)∣ε=0=−t Tr⁡(Ve−tL),(5.5)\left.\frac{d}{d\varepsilon} K(t;\varepsilon) \right|_{\varepsilon=0} = -t\,\operatorname{Tr}(Ve^{-tL}), \tag{5.5}dεdK(t;ε)ε=0=−tTr(Ve−tL),(5.5)

whenever the trace operations and differentiations are justified.

Define the first response by

RV(t)=−ddεK(t;ε)∣ε=0=t Tr⁡(Ve−tL).(5.6)\boxed{ \mathcal R_V(t) = -\left.\frac{d}{d\varepsilon} K(t;\varepsilon)\right|_{\varepsilon=0} = t\,\operatorname{Tr}(Ve^{-tL}). } \tag{5.6}RV(t)=−dεdK(t;ε)ε=0=tTr(Ve−tL).(5.6)

If PλP_\lambdaPλ denotes the spectral projector of LLL, then

RV(t)=t∑λe−tλTr⁡(VPλ).(5.7)\mathcal R_V(t) = t\sum_\lambda e^{-t\lambda}\operatorname{Tr}(VP_\lambda). \tag{5.7}RV(t)=tλ∑e−tλTr(VPλ).(5.7)

The coefficients

wV(λ)=Tr⁡(VPλ)(5.8)w_V(\lambda)=\operatorname{Tr}(VP_\lambda) \tag{5.8}wV(λ)=Tr(VPλ)(5.8)

are weighted spectral data. They record how the perturbation VVV overlaps with each eigenspace.

Unlike the unweighted heat trace, the first response depends on the relation between the operator and the chosen perturbation.

### 5.3 What the first response can distinguish

Suppose two isospectral operators LXL_XLX and LYL_YLY are represented on Hilbert spaces equipped with corresponding probes VXV_XVX and VYV_YVY. If

Tr⁡(VXPλX)≠Tr⁡(VYPλY)(5.9)\operatorname{Tr}(V_XP_\lambda^X) \neq \operatorname{Tr}(V_YP_\lambda^Y) \tag{5.9}Tr(VXPλX)=Tr(VYPλY)(5.9)

for at least one eigenvalue, then their first response functions differ.

Indeed, if their first response functions agreed for every t&gt;0t>0t&gt;0, then

∑λe−tλ\(Tr⁡(VXPλX)−Tr⁡(VYPλY)\)=0(5.10)\sum_\lambda e^{-t\lambda} \left\( \\operatorname{Tr}(V\_XP\_\\lambda^X) - \\operatorname{Tr}(V\_YP\_\\lambda^Y) \\right\) =0 \tag{5.10}λ∑e−tλ\(Tr(VX​PλX​)−Tr(VY​PλY​)\)=0(5.10)

for all t&gt;0t>0t&gt;0. Under the discrete-spectrum and convergence assumptions, uniqueness of the Laplace transform implies equality of the corresponding weighted spectral measures. Therefore a difference in any weighted eigenspace coefficient forces a difference in the response function.

This provides the first concrete mechanism for resolving an isospectral ambiguity.

### 5.4 The probe problem

The perturbation family V\mathcal VV must not be chosen arbitrarily after inspecting the desired answer. Otherwise, the invariant could merely encode the structure by hand.

A defensible probe family should be generated by a stated principle, for example:

* multiplication by a physically marked scalar field;

* covariant differential operators of bounded order;

* geometric tensor fields already included in the model;

* boundary-localized perturbations;

* symmetry generators;

* a controlled family of external potentials or sources.

The probe class determines what the invariant can distinguish. A family too small may miss relevant differences; a family too rich may encode the entire original structure and offer little explanatory compression.

USST therefore treats the choice of probe family as part of the theorem statement.

## 6. Higher-Order Responses and Joint Spectral Information

First-order weighted traces can fail to distinguish structures. Higher-order responses can probe interactions among spectral subspaces.

### 6.1 Second-order response

For two perturbations VVV and WWW, the mixed second derivative is

RV,W(2)(t)=∂2∂ε ∂ηK(t;ε,η)∣ε=η=0,(6.1)\mathcal R_{V,W}^{(2)}(t) = \left. \frac{\partial^2}{\partial\varepsilon\,\partial\eta} K(t;\varepsilon,\eta) \right|_{\varepsilon=\eta=0}, \tag{6.1}RV,W(2)(t)=∂ε∂η∂2K(t;ε,η)ε=η=0,(6.1)

where

K(t;ε,η)=Tr⁡e−t(L+εV+ηW).(6.2)K(t;\varepsilon,\eta) = \operatorname{Tr} e^{-t(L+\varepsilon V+\eta W)}. \tag{6.2}K(t;ε,η)=Tre−t(L+εV+ηW).(6.2)

Repeated application of Duhamel's formula gives

RV,W(2)(t)=∫s1,s2≥0s1+s2≤tTr⁡\(e−(t−s1−s2)LVe−s1LWe−s2L\) ds1 ds2+∫s1,s2≥0s1+s2≤tTr⁡\(e−(t−s1−s2)LWe−s1LVe−s2L\) ds1 ds2.(6.3)\begin{aligned} \mathcal R_{V,W}^{(2)}(t) ={}& \int_{\substack{s_1,s_2\geq0\\s_1+s_2\leq t}} \operatorname{Tr}\Big\( e^{-(t-s\_1-s\_2)L} V e^{-s\_1L} W e^{-s\_2L} \\Big\)\,ds_1\,ds_2\\ &+ \int_{\substack{s_1,s_2\geq0\\s_1+s_2\leq t}} \operatorname{Tr}\Big\( e^{-(t-s\_1-s\_2)L} W e^{-s\_1L} V e^{-s\_2L} \\Big\)\,ds_1\,ds_2. \end{aligned} \tag{6.3}RV,W(2)(t)=∫s1,s2≥0s1+s2≤tTr\(e−(t−s1​−s2​)LVe−s1​LWe−s2​L\)ds1ds2+∫s1,s2≥0s1+s2≤tTr\(e−(t−s1​−s2​)LWe−s1​LVe−s2​L\)ds1ds2.(6.3)

The two terms represent the two possible perturbation orderings. Equivalent parameterizations of the simplex yield the same derivative.

In an eigenbasis, the response depends on matrix elements such as

⟨ψm,Vψn⟩,⟨ψn,Wψm⟩,(6.4)\langle \psi_m,V\psi_n\rangle, \qquad \langle \psi_n,W\psi_m\rangle, \tag{6.4}⟨ψm,Vψn⟩,⟨ψn,Wψm⟩,(6.4)

together with the corresponding spectral weights.

Thus, higher-order responses can reveal relationships among eigenspaces that are absent from the eigenvalue list and may not be visible in first-order weighted traces.

### 6.2 Ordered response words

For a finite sequence of probes Va1,…,VakV_{a_1},\ldots,V_{a_k}Va1,…,Vak, define the kkk-th response tensor

Ra1⋯ak(t)=∂kK(t;ε)∂εa1⋯∂εak∣ε=0.(6.5)\mathcal R_{a_1\cdots a_k}(t) = \left. \frac{\partial^k K(t;\boldsymbol\varepsilon)} {\partial\varepsilon_{a_1}\cdots \partial\varepsilon_{a_k}} \right|_{\boldsymbol\varepsilon=0}. \tag{6.5}Ra1⋯ak(t)=∂εa1⋯∂εak∂kK(t;ε)ε=0.(6.5)

These derivatives are sums of time-ordered trace integrals involving products of heat operators and probes. They encode increasingly detailed correlations between the perturbation family and the spectral decomposition.

The collection

SV(L)={KL(t),Ra1(t),Ra1a2(t),…}(6.6)\mathfrak S_{\mathcal V}(L) = \left\{ K_L(t), \mathcal R_{a_1}(t), \mathcal R_{a_1a_2}(t), \ldots \right\} \tag{6.6}SV(L)={KL(t),Ra1(t),Ra1a2(t),…}(6.6)

is the Spectral Response Signature relative to V\mathcal VV.

The signature is not a single scalar. It is a structured family of functions, and its complexity can be controlled by restricting the probe class, derivative order, or range of ttt.

### 6.3 Basis independence

The traces in (6.5) are invariant under simultaneous unitary conjugation,

L↦ULU−1,Va↦UVaU−1.(6.7)L\mapsto ULU^{-1}, \qquad V_a\mapsto UV_aU^{-1}. \tag{6.7}L↦ULU−1,Va↦UVaU−1.(6.7)

This is desirable: changing the Hilbert-space basis should not alter the invariant.

However, conjugating LLL while leaving the physical probes fixed is not the same operation. The response signature is designed to detect changes in the relative placement of LLL and the probe family, not arbitrary changes of basis.

This distinction is central to its usefulness.

## 7. The Main Separation Theorem

The proposed invariant should have a mathematically precise guarantee. The first theorem is deliberately limited to what the response data can establish.

### 7.1 Theorem: separation by weighted spectral responses

Theorem 7.1 — First-order spectral-response separation.

Let LXL_XLX and LYL_YLY be self-adjoint operators with discrete spectra bounded below and heat operators of trace class for all t&gt;0t>0t&gt;0. Suppose they are isospectral, including multiplicities. Let PλXP_\lambda^XPλX and PλYP_\lambda^YPλY denote their spectral projectors.

Let VXV_XVX and VYV_YVY be corresponding admissible probes. Define

RX(t)=t Tr⁡(VXe−tLX),RY(t)=t Tr⁡(VYe−tLY).(7.1)\mathcal R_X(t) = t\,\operatorname{Tr}(V_Xe^{-tL_X}), \qquad \mathcal R_Y(t) = t\,\operatorname{Tr}(V_Ye^{-tL_Y}). \tag{7.1}RX(t)=tTr(VXe−tLX),RY(t)=tTr(VYe−tLY).(7.1)

Assume the weighted spectral measures are well-defined and their Laplace transforms are unique in the relevant function class.

If there exists an eigenvalue λ∗\lambda_*λ∗ such that

Tr⁡(VXPλ∗X)≠Tr⁡(VYPλ∗Y),(7.2)\operatorname{Tr}(V_XP_{\lambda_*}^X) \neq \operatorname{Tr}(V_YP_{\lambda_*}^Y), \tag{7.2}Tr(VXPλ∗X)=Tr(VYPλ∗Y),(7.2)

then

RX(t)≠RY(t)\mathcal R_X(t)\neq\mathcal R_Y(t)RX(t)=RY(t)

for at least one t&gt;0t>0t&gt;0.

Therefore, the first-order spectral-response invariant distinguishes the two operators relative to the chosen probe correspondence, even though their unperturbed spectra agree.

Proof. Expand each response in its spectral decomposition:

RX(t)t=∑λe−tλTr⁡(VXPλX),(7.3)\frac{\mathcal R_X(t)}{t} = \sum_\lambda e^{-t\lambda} \operatorname{Tr}(V_XP_\lambda^X), \tag{7.3}tRX(t)=λ∑e−tλTr(VXPλX),(7.3)

RY(t)t=∑λe−tλTr⁡(VYPλY).(7.4)\frac{\mathcal R_Y(t)}{t} = \sum_\lambda e^{-t\lambda} \operatorname{Tr}(V_YP_\lambda^Y). \tag{7.4}tRY(t)=λ∑e−tλTr(VYPλY).(7.4)

If the responses agreed for every t&gt;0t>0t&gt;0, the difference of these Laplace transforms would vanish identically. By uniqueness of the Laplace transform under the stated assumptions, the weighted spectral measures would coincide. This contradicts (7.2). Hence the response functions differ for some positive ttt. □\square□

### 7.2 Interpretation

The theorem establishes a genuine separation mechanism, but it does not claim that the proposed invariant distinguishes every isospectral pair.

Its conclusion is conditional on a difference in the weighted spectral-projector data. If all chosen probes yield identical weighted measures, first-order response cannot separate the pair. Higher-order responses or a richer probe family may still distinguish them.

The result also depends on how the probes on XXX and YYY are matched. If no meaningful correspondence between probes exists, the comparison is not yet an invariant geometric test.

### 7.3 Theorem: separation by the full response signature

Let VX\mathcal V_XVX and VY\mathcal V_YVY be matched probe families. Suppose LXL_XLX and LYL_YLY have identical unperturbed spectra but differ in at least one mixed response function:

Ra1⋯akX(t)≠Ra1⋯akY(t)(7.5)\mathcal R^X_{a_1\cdots a_k}(t) \neq \mathcal R^Y_{a_1\cdots a_k}(t) \tag{7.5}Ra1⋯akX(t)=Ra1⋯akY(t)(7.5)

for some finite kkk, some probe word (a1,…,ak)(a_1,\ldots,a_k)(a1,…,ak), and some t&gt;0t>0t&gt;0.

Then

SVX(LX)≠SVY(LY).(7.6)\mathfrak S_{\mathcal V_X}(L_X) \neq \mathfrak S_{\mathcal V_Y}(L_Y). \tag{7.6}SVX(LX)=SVY(LY).(7.6)

This follows directly from the definition of the signature. Its significance is methodological: the enriched invariant distinguishes the pair precisely when the selected response data expose a difference.

The theorem does not establish that such a response difference must exist for every non-isometric isospectral pair. That stronger assertion would require a completeness theorem for the probe family.

### 7.4 The reconstruction theorem sought by USST

The more ambitious target is the following conditional result.

Conjecture 7.1 — Probe-complete inverse-spectral reconstruction.

Let C\mathcal CC be a specified class of compact geometric structures equipped with a natural family of Laplace-type operators and a geometrically defined probe family V\mathcal VV. Suppose the complete response signature is invariant under the declared equivalence relation on C\mathcal CC, and suppose it separates all inequivalent members of C\mathcal CC. Then the signature determines the equivalence class of each structure in C\mathcal CC.

The conclusion is formally immediate once the separation assumption is proved. The substantive open problem is to identify natural classes and probe families for which separation can be established without encoding the geometry trivially into the probes.

A satisfactory USST result must therefore prove the completeness property for a nontrivial model class or produce an explicit counterexample.

## 8. A Stronger Candidate: The Joint Spectral Response Kernel

The response signature can be expressed in a form that makes its dependence on eigenspaces explicit.

### 8.1 Spectral projectors and probe matrix elements

Let PλP_\lambdaPλ denote the spectral projectors of LLL. For two probes Va,VbV_a,V_bVa,Vb, define the joint projector data

Jab(λ,μ)=Tr⁡(PλVaPμVb),(8.1)J_{ab}(\lambda,\mu) = \operatorname{Tr} \left(P_\lambda V_aP_\mu V_b\right), \tag{8.1}Jab(λ,μ)=Tr(PλVaPμVb),(8.1)

whenever the product is trace-class or is otherwise well-defined under the adopted regularization.

Expanding in eigenbases gives

Jab(λ,μ)=∑m:λm=λn:λn=μ⟨ψm,Vaψn⟩⟨ψn,Vbψm⟩.(8.2)J_{ab}(\lambda,\mu) = \sum_{\substack{m:\lambda_m=\lambda\\ n:\lambda_n=\mu}} \langle\psi_m,V_a\psi_n\rangle \langle\psi_n,V_b\psi_m\rangle. \tag{8.2}Jab(λ,μ)=m:λm=λn:λn=μ∑⟨ψm,Vaψn⟩⟨ψn,Vbψm⟩.(8.2)

This quantity records transitions between spectral subspaces under the probes. It is insensitive to arbitrary rotations of basis vectors within degenerate eigenspaces because it is written in terms of projectors and traces.

### 8.2 The joint spectral response kernel

Define

Jab(t,s)=Tr⁡(e−tLVae−sLVb).(8.3)\boxed{ \mathcal J_{ab}(t,s) = \operatorname{Tr} \left(e^{-tL}V_a e^{-sL}V_b\right). } \tag{8.3}Jab(t,s)=Tr(e−tLVae−sLVb).(8.3)

When the trace is well-defined, its spectral expansion is

Jab(t,s)=∑λ,μe−tλ−sμJab(λ,μ).(8.4)\mathcal J_{ab}(t,s) = \sum_{\lambda,\mu} e^{-t\lambda-s\mu} J_{ab}(\lambda,\mu). \tag{8.4}Jab(t,s)=λ,μ∑e−tλ−sμJab(λ,μ).(8.4)

This is a two-parameter Laplace transform of the joint projector data.

If Jab(t,s)\mathcal J_{ab}(t,s)Jab(t,s) is known for all t,s&gt;0t,s>0t,s&gt;0, and the corresponding two-variable Laplace transform is unique in the relevant class, then it determines Jab(λ,μ)J_{ab}(\lambda,\mu)Jab(λ,μ).

The proposed Joint Spectral Response Kernel (JSRK) is the family

JV(L)={Jab(t,s):Va,Vb∈V, t,s&gt;0}.(8.5)\mathfrak J_{\mathcal V}(L) = \left\{ \mathcal J_{ab}(t,s): V_a,V_b\in\mathcal V,\ t,s>0 \right\}. \tag{8.5}JV(L)={Jab(t,s):Va,Vb∈V, t,s&gt;0}.(8.5)

Unlike the unweighted heat trace, this object probes the relationships between eigenspaces under a selected family of operators.

### 8.3 Why the joint kernel may outperform first-order responses

The first-order trace

Tr⁡(Vae−tL)=∑λe−tλTr⁡(VaPλ)(8.6)\operatorname{Tr}(V_ae^{-tL}) = \sum_\lambda e^{-t\lambda} \operatorname{Tr}(V_aP_\lambda) \tag{8.6}Tr(Vae−tL)=λ∑e−tλTr(VaPλ)(8.6)

records only the diagonal weighted projector traces.

The joint kernel records

Tr⁡(PλVaPμVb)(8.7)\operatorname{Tr}(P_\lambda V_aP_\mu V_b) \tag{8.7}Tr(PλVaPμVb)(8.7)

for pairs of spectral subspaces. It can therefore distinguish cases in which all diagonal weights agree but the transition structure between distinct eigenspaces differs.

This does not make the JSRK universally complete. Its discriminatory power depends on the probes and on the operator class. If the probes fail to connect or distinguish relevant subspaces, different structures can still produce identical joint kernels.

### 8.4 Higher-order joint kernels

For a finite word of probes Va1,…,VakV_{a_1},\ldots,V_{a_k}Va1,…,Vak, define

Ja1⋯ak(t1,…,tk)=Tr⁡(e−t1LVa1e−t2LVa2⋯e−tkLVak).(8.8)\mathcal J_{a_1\cdots a_k} (t_1,\ldots,t_k) = \operatorname{Tr} \left( e^{-t_1L}V_{a_1} e^{-t_2L}V_{a_2} \cdots e^{-t_kL}V_{a_k} \right). \tag{8.8}Ja1⋯ak(t1,…,tk)=Tr(e−t1LVa1e−t2LVa2⋯e−tkLVak).(8.8)

These kernels capture cyclic sequences of transitions through spectral subspaces. Their multi-variable Laplace transforms are built from products of spectral projectors and probes.

The complete family of such kernels can be viewed as a spectral analogue of a collection of correlation functions. Whether it reconstructs a given geometry is an inverse problem that must be solved separately for each admissible class.

## 9. Invariance, Gauge Freedom, and the Meaning of a Spectral Signature

An invariant is useful only if its behavior under changes of representation is explicit.

### 9.1 Unitary covariance

Let U:HX→HYU:\mathcal H_X\to\mathcal H_YU:HX→HY be unitary. If

LY=ULXU−1,Va,Y=UVa,XU−1,(9.1)L_Y=UL_XU^{-1}, \qquad V_{a,Y}=UV_{a,X}U^{-1}, \tag{9.1}LY=ULXU−1,Va,Y=UVa,XU−1,(9.1)

then

JabY(t,s)=JabX(t,s)(9.2)\mathcal J^Y_{ab}(t,s) = \mathcal J^X_{ab}(t,s) \tag{9.2}JabY(t,s)=JabX(t,s)(9.2)

for all admissible t,st,st,s. This follows from the functional calculus for LLL, the identity

e−tLY=Ue−tLXU−1,(9.3)e^{-tL_Y}=Ue^{-tL_X}U^{-1}, \tag{9.3}e−tLY=Ue−tLXU−1,(9.3)

and cyclicity of the trace.

Thus the JSRK is invariant under simultaneous unitary equivalence of the operator and the probe family.

### 9.2 The role of geometric markings

If VaV_aVa is a multiplication operator associated with a scalar field faf_afa on a manifold, then a geometric equivalence should transport faf_afa along with the manifold. If the probe is held fixed in a common external coordinate system, it can act as a marking that distinguishes structures otherwise identified by unmarked isometry.

This leads to two different reconstruction questions:

* Unmarked reconstruction: can the invariant determine the geometry up to isometry?

* Marked reconstruction: can it determine the geometry together with specified fields, sources, boundary components, or other markings?

The second problem may be easier because the markings add information. It is also a different problem and should not be presented as a solution to the first unless the markings are part of the intended physical structure.

### 9.3 The trivial-encoding problem

If one allows an arbitrary probe VVV constructed from the entire target geometry, the response signature could distinguish structures for a trivial reason: the geometry would already be encoded in the probe.

To avoid this circularity, USST imposes a probe admissibility principle:

> The probe family must be defined independently of the unknown structural features that the invariant is intended to reconstruct, using only declared background data, physical couplings, or a natural functorial construction.

The principle does not by itself prove that a particular probe family is admissible. Each application must justify its choice.

### 9.4 Minimality and compression

A successful invariant should ideally reveal the missing structure without reproducing the entire original object in disguised form.

This motivates a minimality question: what is the smallest probe family, derivative order, and set of response variables sufficient to distinguish the target class?

The answer may depend strongly on the class. A finite family may suffice for a restricted family of manifolds, while broader classes may require infinitely many probes or response orders.

A complete theory should report both reconstruction power and information cost.

## 10. An Explicit Finite-Dimensional Example

The separation mechanism can be illustrated without assuming a geometric interpretation.

Consider the two self-adjoint matrices

LX=(0001),LY=(1000).(10.1)L_X= \begin{pmatrix} 0&0\\ 0&1 \end{pmatrix}, \qquad L_Y= \begin{pmatrix} 1&0\\ 0&0 \end{pmatrix}. \tag{10.1}LX=(0001),LY=(1000).(10.1)

They are isospectral, with eigenvalues 000 and 111. Their heat traces are identical:

KX(t)=KY(t)=1+e−t.(10.2)K_X(t)=K_Y(t)=1+e^{-t}. \tag{10.2}KX(t)=KY(t)=1+e−t.(10.2)

Let the probe in the common coordinate basis be

V=(1000).(10.3)V= \begin{pmatrix} 1&0\\ 0&0 \end{pmatrix}. \tag{10.3}V=(1000).(10.3)

Then

RX(t)=t Tr⁡(Ve−tLX)=t,(10.4)\mathcal R_X(t) = t\,\operatorname{Tr}(Ve^{-tL_X}) =t, \tag{10.4}RX(t)=tTr(Ve−tLX)=t,(10.4)

whereas

RY(t)=t Tr⁡(Ve−tLY)=te−t.(10.5)\mathcal R_Y(t) = t\,\operatorname{Tr}(Ve^{-tL_Y}) =te^{-t}. \tag{10.5}RY(t)=tTr(Ve−tLY)=te−t.(10.5)

The unperturbed heat trace cannot distinguish the matrices, but the marked probe response can.

There is an important caveat. The two matrices are unitarily equivalent if arbitrary unitary transformations are allowed and the probe is transformed together with the operator. Their difference here is relative to the fixed probe VVV. The example demonstrates marked spectral separation, not an invariant distinction between unmarked unitary-equivalence classes.

This is precisely why USST must declare the admissible equivalences and probe transformation laws.

### 10.1 A higher-order diagnostic

In larger systems, two operators may have identical eigenvalues and identical diagonal weights Tr⁡(VPλ)\operatorname{Tr}(VP_\lambda)Tr(VPλ), yet differ in the matrix elements linking distinct eigenspaces. Then the first-order response is insufficient, but a joint kernel such as

JVW(t,s)=Tr⁡(e−tLVe−sLW)(10.6)\mathcal J_{VW}(t,s) = \operatorname{Tr}(e^{-tL}Ve^{-sL}W) \tag{10.6}JVW(t,s)=Tr(e−tLVe−sLW)(10.6)

may distinguish them.

The example above establishes the principle that eigenvalue data can be enriched by probe-relative spectral information. It does not establish that this specific invariant resolves a known family of isospectral non-isometric manifolds. That remains a geometric research target.

## 11. From Operator Responses to Geometric Reconstruction

The central geometric question is whether the spectral response signature can distinguish spaces, not merely operators on a fixed Hilbert space.

### 11.1 Geometric operators with marked fields

Let (M,g)(M,g)(M,g) be a compact Riemannian manifold and let LgL_gLg be a Laplace-type operator acting on scalar functions or sections of a vector bundle. A natural probe family may be generated by smooth scalar fields faf_afa, acting by multiplication:

(Vfaψ)(x)=fa(x)ψ(x).(11.1)(V_{f_a}\psi)(x)=f_a(x)\psi(x). \tag{11.1}(Vfaψ)(x)=fa(x)ψ(x).(11.1)

The first-order response becomes

Rfa(t)=t∫Mfa(x)Hg(t;x,x) dvol⁡g(x),(11.2)\mathcal R_{f_a}(t) = t\int_M f_a(x)H_g(t;x,x)\, d\operatorname{vol}_g(x), \tag{11.2}Rfa(t)=t∫Mfa(x)Hg(t;x,x)dvolg(x),(11.2)

where Hg(t;x,y)H_g(t;x,y)Hg(t;x,y) is the heat kernel of LgL_gLg.

This formula exposes the information retained by the probe. The unweighted heat trace integrates the diagonal heat kernel without a marker. The weighted trace tests the same diagonal against a specified field.

If the family of admissible fields is sufficiently rich, these weighted integrals can reveal information that the unweighted integral loses. But the fields must be meaningfully matched across the candidate manifolds, and the completeness of the family must be established.

### 11.2 Localized probes

Consider a sequence of smooth functions fϵf_\epsilonfϵ concentrating near a point p∈Mp\in Mp∈M, normalized so that they approach a delta distribution in a suitable weak sense. Under suitable regularity and limiting conditions,

lim⁡ϵ→0Tr⁡(Vfϵe−tLg)=Hg(t;p,p).(11.3)\lim_{\epsilon\to0} \operatorname{Tr} \left(V_{f_\epsilon}e^{-tL_g}\right) = H_g(t;p,p). \tag{11.3}ϵ→0limTr(Vfϵe−tLg)=Hg(t;p,p).(11.3)

Thus, sufficiently localized probes recover the diagonal heat kernel at a marked point.

By combining local probes with additional geometric information, one can investigate local heat invariants and spatial variation of the heat kernel. Yet this does not automatically reconstruct the entire metric: the diagonal kernel alone is not known to determine every metric in every dimension and class.

The limiting construction also uses spatial localization. If the location of the probe is supplied externally, the resulting invariant is a marked-geometric invariant.

### 11.3 Off-diagonal information

The full heat kernel Hg(t;x,y)H_g(t;x,y)Hg(t;x,y) describes heat propagation between two points. Its short-time behavior reflects geodesic distance in appropriate local regions, and its longer-time behavior encodes global propagation.

A marked or two-point spectral invariant can retain information that a scalar trace discards. For example, if the points p,qp,qp,q are marked, one can study

Hg(t;p,q).(11.4)H_g(t;p,q). \tag{11.4}Hg(t;p,q).(11.4)

However, an inverse theorem must specify how the points are identified across the structures being compared. Without a canonical marking, the statement “the kernels agree at p,qp,qp,q” may not be well-defined between different manifolds.

### 11.4 A geometric reconstruction target

For a specified class C\mathcal CC of compact Riemannian manifolds, define

GV(M,g)=(Kg,SV(Δg),JV(Δg)).(11.5)\mathfrak G_{\mathcal V}(M,g) = \left( K_g, \mathfrak S_{\mathcal V}(\Delta_g), \mathfrak J_{\mathcal V}(\Delta_g) \right). \tag{11.5}GV(M,g)=(Kg,SV(Δg),JV(Δg)).(11.5)

The geometric reconstruction problem is to determine whether

GV(M,g)=GV(N,h)⟹(M,g)≅(N,h)(11.6)\mathfrak G_{\mathcal V}(M,g) = \mathfrak G_{\mathcal V}(N,h) \quad\Longrightarrow\quad (M,g)\cong(N,h) \tag{11.6}GV(M,g)=GV(N,h)⟹(M,g)≅(N,h)(11.6)

for the chosen class and probe family.

Equation (11.6) is a target theorem. It is not established by the operator-level separation result alone. Proving it requires both a geometrically natural definition of the probes and a completeness argument for the enriched data.

## 12. Spectral Response and Dynamical Reconstruction

USST also applies to systems in which the operator spectrum describes dynamics rather than spatial geometry.

### 12.1 Resolvents and spectral response

For a self-adjoint operator LLL, the resolvent is

G(z)=(L−zI)−1,(12.1)G(z)=(L-zI)^{-1}, \tag{12.1}G(z)=(L−zI)−1,(12.1)

defined away from the spectrum. Its matrix elements,

Gab(z)=⟨a,(L−zI)−1b⟩,(12.2)G_{ab}(z)= \langle a,(L-zI)^{-1}b\rangle, \tag{12.2}Gab(z)=⟨a,(L−zI)−1b⟩,(12.2)

depend on both eigenvalues and the overlaps of the states a,ba,ba,b with the eigenvectors.

In a discrete eigenbasis,

Gab(z)=∑n⟨a,ψn⟩⟨ψn,b⟩λn−z,(12.3)G_{ab}(z) = \sum_n \frac{\langle a,\psi_n\rangle \langle\psi_n,b\rangle} {\lambda_n-z}, \tag{12.3}Gab(z)=n∑λn−z⟨a,ψn⟩⟨ψn,b⟩,(12.3)

when the expansion is valid in the appropriate operator or weak sense.

The poles reveal spectral locations, while the residues reveal probe-dependent spectral weights. Thus, a family of resolvent matrix elements can distinguish operators with the same eigenvalues but different responses to selected states or sources.

### 12.2 Time-domain propagation

The heat semigroup e−tLe^{-tL}e−tL is one type of evolution operator. For a self-adjoint Hamiltonian HHH, unitary time evolution is instead

U(τ)=e−iτH/ℏ.(12.4)U(\tau)=e^{-i\tau H/\hbar}. \tag{12.4}U(τ)=e−iτH/ℏ.(12.4)

A corresponding two-point amplitude is

Aab(τ)=⟨a,e−iτH/ℏb⟩.(12.5)A_{ab}(\tau) = \langle a,e^{-i\tau H/\hbar}b\rangle. \tag{12.5}Aab(τ)=⟨a,e−iτH/ℏb⟩.(12.5)

This amplitude depends on the spectrum and on the overlaps with the states a,ba,ba,b. Knowing only the eigenvalues is insufficient to determine all such amplitudes when the states and their relation to the eigenvectors are not also specified.

A dynamical version of USST can therefore enrich the spectrum with transition amplitudes, correlation functions, and response coefficients.

### 12.3 Causal and operational constraints

The fact that a resolvent or propagator distinguishes two operators does not establish that the distinction is physically observable. A valid physical reconstruction must identify the probes as realizable sources, states, or measurements, and it must show that the relevant response can be measured or derived within the theory.

In a quantum system, unitary equivalence can preserve all predictions if states and observables are transformed consistently. In a controlled experiment, however, fixed external couplings may provide a meaningful marking that makes two otherwise isospectral descriptions operationally distinguishable.

The general lesson is the same as in geometry: spectral enrichment works relative to a declared family of physical interactions.

## 13. Spectral Structure in Quantum Field Theory

The operator framework extends naturally to regulated quantum field theories, where fluctuation operators, kinetic operators, and Hamiltonians carry information about the background structure.

### 13.1 Fluctuation operators

Suppose a field theory has an action S\(ϕ\)S\(\\phi\)S\(ϕ\), and let ϕˉ\bar\phiϕˉ be a background configuration. The quadratic fluctuation operator is formally

Lϕˉ=δ2Sδϕ δϕ∣ϕ=ϕˉ.(13.1)L_{\bar\phi} = \left. \frac{\delta^2 S} {\delta\phi\,\delta\phi} \right|_{\phi=\bar\phi}. \tag{13.1}Lϕˉ=δϕδϕδ2Sϕ=ϕˉ.(13.1)

Its spectrum controls the Gaussian approximation around the background. In a regulated setting, a determinant of LϕˉL_{\bar\phi}Lϕˉ contributes to the one-loop effective action:

Γ(1)\(ϕˉ\)=12log⁡det⁡Lϕˉ,(13.2)\Gamma^{(1)}\(\\bar\\phi\) = \frac12\log\det L_{\bar\phi}, \tag{13.2}Γ(1)\(ϕˉ​\)=21logdetLϕˉ,(13.2)

up to conventional factors, normalization, and regularization terms.

For infinitely many modes, the determinant generally requires regularization. A heat-kernel representation is often used schematically:

log⁡det⁡L=−∫0∞dtt Tr⁡(e−tL)+regularization terms.(13.3)\log\det L = -\int_0^\infty\frac{dt}{t}\, \operatorname{Tr}(e^{-tL}) +\text{regularization terms}. \tag{13.3}logdetL=−∫0∞tdtTr(e−tL)+regularization terms.(13.3)

The exact formula depends on the operator, zero modes, mass scales, and renormalization prescription.

### 13.2 Background discrimination

Two backgrounds can potentially produce fluctuation operators with identical spectra but different eigenfunctions or couplings to background-dependent probes. The response signature can then distinguish their fluctuation structures.

However, one-loop spectral information does not necessarily determine the full interacting quantum field theory. Different interactions may share the same quadratic operator around a particular background. Gauge symmetries, constraints, zero modes, and renormalization further complicate the inverse problem.

The proposed theory should therefore be applied first to a well-defined operator sector before claims are extended to the complete quantum theory.

### 13.3 Gauge and symmetry constraints

For gauge theories, raw operator spectra can include gauge-dependent or unphysical modes. A meaningful invariant must specify the gauge fixing, treatment of constraints, and physical state space—or demonstrate that the final signature is gauge-invariant.

If the operator family changes under a gauge transformation, the probe family must transform consistently. Otherwise, an apparent spectral distinction may be a gauge artifact rather than a physical difference.

### 13.4 A controlled field-theoretic target

A concrete research target is to select a class of backgrounds for which:

1. the fluctuation operator is self-adjoint after a specified Euclidean continuation or other suitable construction;

2. the heat trace and response traces are regularized consistently;

3. the probe family is gauge-compatible;

4. known isospectral or spectrally degenerate backgrounds can be identified;

5. the enriched response data are tested for separation.

A positive result would establish a model-specific inverse theorem. It would not, without further work, establish universal reconstruction of spacetime or all field-theoretic dynamics.

## 14. The Limits of the Proposed Invariant

The Spectral Response Signature and Joint Spectral Response Kernel are promising candidates, but several obstructions remain.

### 14.1 Incomplete probe families

If every probe in V\mathcal VV acts identically on the relevant spectral subspaces, then the response signature may fail to distinguish the structures.

This is a direct consequence of the definitions. The invariant can detect only the information that the chosen probes couple to.

### 14.2 Symmetry-protected degeneracy

High symmetry can cause multiple structures or subspaces to produce identical responses for a restricted probe family. Resolving such cases may require symmetry-breaking probes, representation-valued spectral data, or higher-order responses.

Adding symmetry-breaking information changes the reconstruction problem and must be justified by the intended physical setup.

### 14.3 Isospectrality under enriched data

Even a rich family of weighted traces need not be complete on every geometric class. Different structures may share all the responses accessible to a given probe family.

The correct conclusion in that case is not that the structures are identical, but that the selected invariant is insufficient for the chosen class.

### 14.4 Stability and ill-conditioning

A response signature may distinguish two structures mathematically while doing so only through an extremely small difference. Finite measurement precision or numerical error may erase the distinction.

A practical reconstruction theorem should therefore address not only injectivity but also stability. If the inverse map is discontinuous or badly conditioned, exact uniqueness may offer little operational value.

### 14.5 Infinite data and finite resources

The full signature may require knowledge of response functions for a continuum of time parameters and arbitrarily high derivative order. This is mathematically legitimate but may be computationally or experimentally impractical.

A useful theory should seek finite or efficiently approximable subsets of the signature that suffice for a target class.

## 15. A Stability Framework for Inverse-Spectral Reconstruction

### 15.1 Perturbation of spectral data

Let LLL be a self-adjoint operator with isolated eigenvalues. Under suitable bounded perturbations, isolated spectral clusters and their Riesz projectors vary continuously, and often analytically, with the perturbation parameter.

For an isolated spectral cluster enclosed by a contour Γ\GammaΓ,

P(ε)=12πi∮Γ(zI−L−εV)−1 dz.(15.1)P(\varepsilon) = \frac{1}{2\pi i} \oint_\Gamma (zI-L-\varepsilon V)^{-1}\,dz. \tag{15.1}P(ε)=2πi1∮Γ(zI−L−εV)−1dz.(15.1)

As long as Γ\GammaΓ remains in the resolvent set of the perturbed operator, this formula defines a stable projector for the cluster.

Individual eigenvectors inside a degenerate cluster may not vary uniquely, but the cluster projector can remain well-defined. This is another reason to formulate USST using projectors and traces rather than arbitrarily selected eigenvectors.

### 15.2 Response stability

For a bounded probe VVV, the first response is

RV(t)=tTr⁡(Ve−tL).(15.2)\mathcal R_V(t)=t\operatorname{Tr}(Ve^{-tL}). \tag{15.2}RV(t)=tTr(Ve−tL).(15.2)

If LLL varies to L+δLL+\delta LL+δL, the first-order variation is

δRV(t)=−t∫0tTr⁡\(Ve−(t−s)L(δL)e−sL\)ds,(15.3)\delta\mathcal R_V(t) = -t\int_0^t \operatorname{Tr} \left\( V e^{-(t-s)L} (\\delta L) e^{-sL} \\right\)ds, \tag{15.3}δRV(t)=−t∫0tTr\(Ve−(t−s)L(δL)e−sL\)ds,(15.3)

subject to trace-class and differentiability conditions.

This formula expresses the local sensitivity of the response to an operator perturbation. Bounds on the semigroup and on the trace norms can be used to derive explicit error estimates for particular operator classes.

### 15.3 Reconstruction stability

Suppose SV\mathfrak S_{\mathcal V}SV maps a structure to its response signature. A useful inverse theorem would establish an estimate of the form

dC(X,Y)≤Ω ⁣(dD(SV(X),SV(Y))),(15.4)d_{\mathcal C}(X,Y) \leq \Omega\!\left( d_{\mathfrak D} \big( \mathfrak S_{\mathcal V}(X), \mathfrak S_{\mathcal V}(Y) \big) \right), \tag{15.4}dC(X,Y)≤Ω(dD(SV(X),SV(Y))),(15.4)

where:

* dCd_{\mathcal C}dC measures structural distance modulo the declared equivalence;

* dDd_{\mathfrak D}dD measures distance between spectral signatures;

* Ω\OmegaΩ is a continuity modulus satisfying Ω(r)→0\Omega(r)\to0Ω(r)→0 as r→0r\to0r→0.

The existence of such an estimate is not guaranteed by injectivity. Some inverse problems are uniquely solvable but unstable.

For USST, uniqueness and stability should be treated as separate milestones.

## 16. The Universal Spectral Structure Principle

The preceding analysis suggests a general principle, with a precise distinction between its established mathematical content and its proposed extension.

### 16.1 Principle of spectral enrichment

Principle. The reconstructive content of an operator is determined not only by its eigenvalues, but by the collection of spectral data that remains invariant under the declared equivalences and that captures the operator's relations to an admissible family of probes.

The bare spectrum records the eigenvalue measure. The response signature adds weighted spectral measures. The joint response kernel adds transition information between spectral subspaces. Higher-order kernels add ordered correlations among multiple probes.

The resulting hierarchy is

S0(L)={λn},S1(L;V)={Tr⁡(VaPλ)},S2(L;V)={Tr⁡(PλVaPμVb)},Sk(L;V)={higher joint projector correlations}.(16.1)\begin{aligned} \mathfrak S_0(L) &=\{\lambda_n\},\\ \mathfrak S_1(L;\mathcal V) &=\{\operatorname{Tr}(V_aP_\lambda)\},\\ \mathfrak S_2(L;\mathcal V) &=\{\operatorname{Tr}(P_\lambda V_aP_\mu V_b)\},\\ \mathfrak S_k(L;\mathcal V) &=\{\text{higher joint projector correlations}\}. \end{aligned} \tag{16.1}S0(L)S1(L;V)S2(L;V)Sk(L;V)={λn},={Tr(VaPλ)},={Tr(PλVaPμVb)},={higher joint projector correlations}.(16.1)

Each level can contain information not present in the preceding level. The hierarchy is not automatically strictly increasing for every operator or probe family; in some cases, lower-order data already suffice.

### 16.2 Reconstruction as separation

Let C\mathcal CC be the target class and ≅\cong≅ the declared equivalence relation. An invariant I\mathfrak II is complete on C\mathcal CC if

I(X)=I(Y)⟺X≅Y(X,Y∈C).(16.2)\mathfrak I(X)=\mathfrak I(Y) \quad\Longleftrightarrow\quad X\cong Y \qquad (X,Y\in\mathcal C). \tag{16.2}I(X)=I(Y)⟺X≅Y(X,Y∈C).(16.2)

The forward implication is the difficult direction: it says that equal invariant data force structural equivalence. The reverse implication is the invariance requirement.

For USST, completeness is a class-dependent property. A response signature may be complete on one restricted class and incomplete on a larger one.

### 16.3 The spectral response conjecture

Conjecture 16.1 — Response completeness for a natural geometric class.

There exist nontrivial classes of compact geometric structures for which a naturally defined, geometrically covariant probe family produces a spectral response signature that distinguishes all inequivalent members of the class.

The conjecture does not assert that one fixed probe family distinguishes every isospectral non-isometric manifold. It proposes that useful classes and natural probe families exist for which a completeness theorem can be proved.

A convincing proof would need to:

1. define the geometric class without using the desired answer;

2. define the probes independently of the unknown geometry, except for explicitly allowed geometric couplings;

3. establish invariance under isometry or the chosen equivalence;

4. prove that equality of the complete response signatures implies equivalence;

5. provide at least one explicit isospectral ambiguity that the enriched invariant resolves;

6. assess stability and the minimal amount of response data required.

Until these steps are completed, response completeness remains a conjectural research direction.

## 17. Computational and Experimental Program

The framework can be tested using numerical operators, exactly solvable models, and geometric examples.

### 17.1 Discrete operator experiments

Begin with finite-dimensional self-adjoint matrices LiL_iLi. Compute their eigenvalues and identify pairs that are exactly or approximately isospectral.

For each pair, select a probe family V\mathcal VV and calculate

Ki(t)=Tr⁡(e−tLi),(17.1)K_i(t)=\operatorname{Tr}(e^{-tL_i}), \tag{17.1}Ki(t)=Tr(e−tLi),(17.1)

Ra,i(t)=tTr⁡(Va,ie−tLi),(17.2)\mathcal R_{a,i}(t) =t\operatorname{Tr}(V_{a,i}e^{-tL_i}), \tag{17.2}Ra,i(t)=tTr(Va,ie−tLi),(17.2)

and

Jab,i(t,s)=Tr⁡(e−tLiVa,ie−sLiVb,i).(17.3)\mathcal J_{ab,i}(t,s) =\operatorname{Tr}(e^{-tL_i}V_{a,i}e^{-sL_i}V_{b,i}). \tag{17.3}Jab,i(t,s)=Tr(e−tLiVa,ie−sLiVb,i).(17.3)

The test is whether the enriched data distinguish the pair while respecting the intended equivalence.

For finite matrices, these calculations are computationally tractable and allow exact checks against the underlying spectral decompositions.

### 17.2 Geometric benchmark problems

The next step is to use established isospectral constructions of non-isometric manifolds or domains.

For each benchmark, the investigation should specify:

* the geometric class and its equivalence relation;

* the Laplace-type operator and boundary conditions;

* the unperturbed spectral data;

* the probe family and its geometric meaning;

* the response quantities computed;

* the evidence that the probes are not encoding the unknown geometry directly;

* the result of the separation test.

A numerical difference is evidence for discrimination in the tested example, not a proof of general completeness. A theorem must explain why the difference persists for the entire claimed class.

### 17.3 Numerical conditioning

Numerical studies should distinguish exact separation from approximate separation. If two response functions differ by an amount smaller than the numerical error, the computed result cannot reliably establish discrimination.

Useful diagnostics include:

* convergence under discretization refinement;

* sensitivity to perturbation strength;

* conditioning of eigenprojector calculations;

* stability of response differences under noise;

* dependence on the range and sampling of ttt and sss.

The objective is not merely to produce a distinguishing numerical signature, but to understand how robustly it distinguishes the target structures.

### 17.4 A staged benchmark

Benchmark A — Finite matrices

Verify response identities, projector formulas, unitary covariance, and known failure cases exactly.

Benchmark B — Isospectral geometries

Test whether natural weighted heat traces or joint response kernels separate known non-isometric examples.

Benchmark C — Stability and noise

Determine whether the distinguishing information survives finite precision, model perturbations, and discretization.

Benchmark D — Reconstruction theorem

Prove that equality of the selected invariant forces equivalence throughout a precisely defined structural class.

## 18. Open Problems

The proposed theory leaves several substantial questions unresolved.

### Problem 1 — Minimal probe completeness

Find the smallest natural probe family V\mathcal VV for which the response signature separates a nontrivial class of isospectral structures.

The strongest result would provide both a completeness theorem and a demonstration that a strictly smaller family fails.

### Problem 2 — Unmarked reconstruction

Determine whether a response invariant can distinguish unmarked isospectral non-isometric manifolds without relying on external coordinate systems or geometry-specific probes.

This is a more demanding problem than marked reconstruction because the invariant must remain meaningful without preassigned point correspondences.

### Problem 3 — Finite-order sufficiency

Determine whether a bounded response order kkk suffices for a useful structural class, or whether arbitrarily high-order correlations are required.

A finite-order theorem would substantially improve computational feasibility.

### Problem 4 — Stability of inverse reconstruction

Prove quantitative estimates that relate changes in the response signature to changes in geometry modulo isometry. Uniqueness without stability may be inadequate for physical applications.

### Problem 5 — Continuous spectra

Extend the framework to operators with continuous spectrum, scattering states, resonances, or non-trace-class heat operators. Suitable replacements may involve relative heat traces, spectral-shift functions, scattering matrices, or renormalized response kernels.

### Problem 6 — Gauge-invariant reconstruction

Construct a response signature for gauge theories that is invariant under the appropriate gauge transformations and separates physically inequivalent backgrounds without relying on gauge artifacts.

### Problem 7 — Dynamical equivalence

Determine when spectral response data for Hamiltonians or evolution generators establish equivalence of dynamics, rather than only equivalence of selected correlation functions.

### Problem 8 — Universal versus class-specific invariants

Determine whether there is a meaningful universal response architecture whose specialization to different operator classes yields complete invariants, or whether completeness must always be proved separately for each class.

The present framework supports the latter as a safe baseline. Any stronger universality claim requires proof.

## 19. Conclusions

The Universal Spectral Structure Theory addresses a fundamental limitation of inverse-spectral reconstruction: eigenvalues can encode extensive geometric and dynamical information without uniquely determining the structure that generated them.

The heat trace

K(t)=Tr⁡(e−tL)K(t)=\operatorname{Tr}(e^{-tL})K(t)=Tr(e−tL)

is a powerful spectral summary. Its short-time asymptotics reveal established geometric invariants, while its full dependence on ttt encodes the complete eigenvalue measure under the stated discrete-spectrum assumptions. Yet isospectral non-isometric structures show that no invariant derived solely from the same unweighted eigenvalue list can distinguish every such pair.

The proposed response-based approach introduces additional information through the operator's interaction with a controlled probe family. The Spectral Response Signature records weighted spectral-projector traces and their higher derivatives. The Joint Spectral Response Kernel records transitions between spectral subspaces. Both are invariant under simultaneous unitary transformations of the operator and probes, and both can distinguish some pairs whose unperturbed spectra coincide.

The central mathematical result is a conditional separation theorem: a difference in a weighted spectral measure forces a difference in the corresponding response function. Higher-order response data provide further possible separation mechanisms. These results establish that spectral enrichment can resolve specified ambiguities, but they do not establish universal geometric reconstruction.

The unresolved task is to identify natural probe families for which the enriched invariant is complete on a nontrivial class of geometric structures. Such a theorem must prove invariance, separation, and preferably stability, while preventing the probes from encoding the desired geometry by construction.

The guiding principle is therefore:

A spectrum records the eigenvalues of an operator. A response signature records how its spectral subspaces participate in a larger structure of interactions. Reconstruction becomes possible when that additional structure is both invariant and sufficiently discriminating.

USST is best understood at this stage as a proposed inverse-spectral research program with established operator identities, a conditional separation theorem, and open geometric completeness conjectures. Its success will be determined not by the breadth of its terminology, but by whether a natural, independently specified spectral response invariant can distinguish a known class of isospectral structures and support a rigorous reconstruction theorem.

## Appendix A. Core Definitions

### A.1 Heat trace

For a self-adjoint operator LLL with a trace-class heat semigroup,

KL(t)=Tr⁡(e−tL).(A.1)K_L(t)=\operatorname{Tr}(e^{-tL}). \tag{A.1}KL(t)=Tr(e−tL).(A.1)

### A.2 Spectral Response Signature

For an admissible probe family V={Va}\mathcal V=\{V_a\}V={Va},

SV(L)={∂εa1⋯∂εakTr⁡e−t(L+∑aεaVa)∣ε=0:k≥1}.(A.2)\mathfrak S_{\mathcal V}(L) = \left\{ \left. \partial_{\varepsilon_{a_1}}\cdots \partial_{\varepsilon_{a_k}} \operatorname{Tr} e^{-t(L+\sum_a\varepsilon_aV_a)} \right|_{\boldsymbol\varepsilon=0} : k\geq1 \right\}. \tag{A.2}SV(L)={∂εa1⋯∂εakTre−t(L+∑aεaVa)ε=0:k≥1}.(A.2)

The full signature includes the unperturbed heat trace and all specified response orders. In applications, one may restrict it to a finite probe family or finite maximum order.

### A.3 Joint Spectral Response Kernel

For admissible probes Va,VbV_a,V_bVa,Vb,

Jab(t,s)=Tr⁡(e−tLVae−sLVb).(A.3)\mathcal J_{ab}(t,s) = \operatorname{Tr} (e^{-tL}V_ae^{-sL}V_b). \tag{A.3}Jab(t,s)=Tr(e−tLVae−sLVb).(A.3)

Its spectral coefficients are

Jab(λ,μ)=Tr⁡(PλVaPμVb).(A.4)J_{ab}(\lambda,\mu) = \operatorname{Tr}(P_\lambda V_aP_\mu V_b). \tag{A.4}Jab(λ,μ)=Tr(PλVaPμVb).(A.4)

### A.4 Completeness criterion

For a structure class C\mathcal CC and declared equivalence relation ≅\cong≅, an invariant I\mathfrak II is complete if

I(X)=I(Y)  ⟺  X≅Y.(A.5)\mathfrak I(X)=\mathfrak I(Y) \iff X\cong Y. \tag{A.5}I(X)=I(Y)⟺X≅Y.(A.5)

Completeness is a property to prove for a specific class, not a consequence of adding response terms by definition.

### A.5 Stability criterion

A reconstruction is stable if closeness of invariant data controls structural distance, for example through an estimate

dC(X,Y)≤Ω ⁣(dD(I(X),I(Y))),Ω(r)→0(r→0).(A.6)d_{\mathcal C}(X,Y) \leq \Omega\!\left( d_{\mathfrak D}(\mathfrak I(X),\mathfrak I(Y)) \right), \qquad \Omega(r)\to0 \quad(r\to0). \tag{A.6}dC(X,Y)≤Ω(dD(I(X),I(Y))),Ω(r)→0(r→0).(A.6)

The existence and form of such a modulus depend on the operator class and the inverse problem.

## Appendix B. Research Audit for a Proposed USST Application

Before claiming that the theory reconstructs a geometry or dynamics, an application should answer the following questions.

* Is the operator class precisely defined, including domains, boundary conditions, and spectral assumptions?

* Is the unperturbed spectrum or heat trace known to be insufficient for the target reconstruction?

* Is the probe family defined independently of the unknown structure?

* Does the invariant respect the intended equivalences?

* Is a specific isospectral ambiguity actually distinguished?

* Are the weighted response identities and convergence conditions proved?

* Is the probe family complete for the claimed structural class, or is completeness explicitly left open?

* Are numerical errors and stability addressed?

* Is the distinction between marked and unmarked reconstruction explicit?

* Are physical interpretations supported by observable or dynamical correspondence, rather than inferred from spectral differences alone?

The decisive next result would be a worked theorem for a known family of isospectral non-isometric spaces: specify a natural probe family, calculate its response invariant, prove that it separates the family, and establish the precise equivalence class it reconstructs. That would turn the central proposal of USST into a concrete contribution to inverse spectral geometry.

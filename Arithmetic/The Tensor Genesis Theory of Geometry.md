The Tensor Genesis Theory of Geometry

Reconstructing Metric Geometry from Relational Tensor Structures, Contractions, and Symmetry

Research preprint

Date: October 13, 2026

Abstract

The Tensor Genesis Theory of Geometry (TGTG) investigates whether metric geometry can be reconstructed from relational tensor data before a metric is specified as a primitive structure. Its central question is whether a collection of tensors, together with admissible contraction rules, algebraic identities, symmetry conditions, and regularity assumptions, contains sufficient information to determine an effective metric uniquely up to a declared equivalence.

Let be a smooth manifold, and consider a relational tensor field

T\in\Gamma\!\left(
(T^\ast M)^{\otimes p}\otimes (TM)^{\otimes q}
\right),

with local components

T_{a_1\cdots a_p}{}^{b_1\cdots b_q}.

A tensor of this type is defined without choosing a metric, although contractions between covariant and contravariant indices still use the canonical tensor pairing. The theory asks when such relational data determine a nondegenerate symmetric bilinear form , or a more general geometric structure from which follows.

The principal result developed here is a conditional metric-reconstruction theorem. If the relational data determine, at every point, a unique symmetric bilinear form up to a prescribed positive scale, and if the reconstructed forms vary smoothly and satisfy the required nondegeneracy and signature conditions, then they define a conformal metric structure. If the relational data additionally determine a compatible scale, the conformal class selects a unique metric. A second reconstruction route uses a nondegenerate symmetric covariant tensor obtained from an algebraic contraction of the relational data. A third route treats a tensor as a symmetry-breaking structure whose stabilizer group determines a metric up to scale.

These results distinguish three problems that are often conflated: constructing a candidate bilinear form, proving its invariance under the allowed symmetries, and establishing uniqueness among all admissible metrics. They also show why generic tensor data do not determine a metric automatically. A vector, a differential form, or a high-rank tensor may admit many compatible metrics, while degenerate contractions and excessive stabilizer symmetry can obstruct uniqueness.

The proposed theory is therefore not a claim that geometry universally emerges from any tensor. It is a framework for identifying the exact algebraic, differential, and symmetry conditions under which metric geometry is recoverable from premetric relational structure. Its main research objective is to characterize the minimal relational data sufficient for metric reconstruction, and to determine when that reconstruction is canonical, stable under perturbations, and compatible with tensor-network representations.

Keywords: differential geometry; metric reconstruction; relational tensors; tensor contractions; invariant theory; stabilizer groups; conformal geometry; tensor networks; premetric geometry; geometric emergence.

1. Introduction

Differential geometry ordinarily begins with a smooth manifold and then introduces additional structure: a metric, a connection, a symplectic form, a volume form, or some combination of these. Each structure provides different geometric information.

A metric determines lengths, angles, orthogonality, geodesics, and—when nondegenerate—a canonical correspondence between tangent and cotangent vectors. A connection determines parallel transport and covariant differentiation. A volume form determines oriented volume. A symplectic form determines a nondegenerate antisymmetric pairing. These structures are related, but none is interchangeable with all the others.

The Tensor Genesis Theory of Geometry reverses one particular direction of construction. Instead of starting with a metric and using it to interpret tensors, it asks whether a suitable relational tensor system already constrains the possible metric structures.

The question is not whether tensors can be written down on a manifold without a metric. They can. The question is whether their algebraic relationships, transformation properties, and contraction identities select a metric uniquely.

Let be a smooth -dimensional manifold. A relational tensor field may be written locally as

T_{a_1\cdots a_p}{}^{b_1\cdots b_q}.
\tag{1.1}

The lower indices transform covariantly, and the upper indices transform contravariantly. The tensor field is independent of any metric choice.

The central reconstruction problem is to determine whether there exists a smooth field

g\in\Gamma(S^2T^\ast M)
\tag{1.2}

such that is nondegenerate, has a prescribed signature, and is uniquely determined by together with the stated admissibility rules.

The problem separates naturally into three questions:

* Existence: Does a metric compatible with the relational tensor data exist?
* Uniqueness: Is that metric uniquely determined, either exactly or up to a specified equivalence?
* Naturality: Does the reconstruction commute with coordinate changes, symmetry transformations, and admissible maps between manifolds?

A construction that answers only the first question is not a metric reconstruction theorem. Many metrics may satisfy the same weak compatibility conditions.

1.1 Central hypothesis

The central hypothesis of TGTG is that certain relational tensor systems possess enough algebraic rigidity to determine a metric, or at least a conformal class, without assuming that metric as independent input.

The hypothesis is conditional. It does not assert that every tensor contains metric information, or that contractions can manufacture a unique metric from arbitrary data.

A valid theory must establish that:

* the candidate metric is constructed without using an unacknowledged metric;
* its symmetry and nondegeneracy follow from stated hypotheses;
* its transformation law is tensorial;
* all residual ambiguities are identified;
* the reconstruction is unique in the declared class;
* the conditions are not merely restatements of the existence of the desired metric.

1.2 Scope and mathematical strategy

This paper develops four complementary reconstruction mechanisms:

* Direct algebraic reconstruction: a contraction of relational tensors produces a symmetric, nondegenerate covariant two-tensor.
* Stabilizer reconstruction: the symmetry group preserving the relational data determines a metric up to scale or exact normalization.
* Conformal reconstruction: relational data determine a conformal class, with an additional scalar structure fixing the metric scale.
* Tensor-network reconstruction: a contraction architecture defines relational quantities whose consistency conditions may select an effective bilinear form.

The first three admit precise mathematical formulations using established differential geometry and invariant theory. The fourth is a research program requiring additional assumptions about the network, its contractions, and the interpretation of its outputs.

The intended contribution is a unified reconstruction framework with explicit existence, uniqueness, and obstruction criteria.

2. Mathematical Foundations: Geometry Before the Metric

2.1 The smooth manifold

Let be a smooth manifold of dimension . Its tangent space at is , and its cotangent space is .

A tensor of type , using the convention of contravariant and covariant indices, belongs to

T_x^{\otimes q}M\otimes (T_x^\ast M)^{\otimes p}.
\tag{2.1}

The corresponding tensor field is a smooth section of the associated tensor bundle.

No metric is required to define these spaces, the tensor product, the dual pairing, or contraction between a vector and a covector.

2.2 Canonical contraction without a metric

For a vector and a covector , the natural pairing is

\langle\alpha,v\rangle=\alpha(v).
\tag{2.2}

In components,

\alpha_av^a.
\tag{2.3}

This contraction is canonical. It does not require a metric.

By contrast, contracting two covariant indices or two contravariant indices requires an additional pairing, such as a metric or its inverse, unless the tensor structure already supplies an appropriate map.

This distinction is foundational. A premetric reconstruction theory must not use or implicitly in the very contractions from which is supposed to emerge.

2.3 The relational tensor

Let

T\in\Gamma\!\left(
(T^\ast M)^{\otimes p}\otimes (TM)^{\otimes q}
\right).
\tag{2.4}

The tensor may encode one or more of the following:

* a multilinear relation among tangent and cotangent directions;
* an algebraic operation on tangent vectors;
* a field of endomorphisms;
* a collection of invariant subspaces;
* a preferred distribution or family of distributions;
* a volume or orientation structure;
* a tensor-network contraction pattern;
* a family of constraints on admissible local frames.

The word relational refers to the role of in constraining possible geometric structures. It does not introduce a new mathematical object beyond a tensor field and its specified relations.

2.4 Metric structure

A metric is a smooth section

g\in\Gamma(S^2T^\ast M)
\tag{2.5}

such that, at every , the bilinear form is nondegenerate.

In local coordinates,

g=g_{ab}\,dx^a\otimes dx^b,
\qquad g_{ab}=g_{ba},
\tag{2.6}

with

\det(g_{ab})\neq0.
\tag{2.7}

For a positive-definite Riemannian metric,

g(v,v)>0
\quad\text{for all }v\neq0.
\tag{2.8}

For a pseudo-Riemannian metric, the signature is fixed but need not be positive definite.

The metric induces the musical isomorphisms

\flat_g:TM\to T^\ast M,
\qquad
v^a\mapsto g_{ab}v^b,
\tag{2.9}

and

\sharp_g:T^\ast M\to TM,
\qquad
\alpha_a\mapsto g^{ab}\alpha_b.
\tag{2.10}

These maps should be consequences of the reconstruction, not assumed in advance.

3. The Reconstruction Problem

Let denote a specified class of relational tensor configurations on . A configuration may consist of one tensor or a finite collection:

\mathbf T=(T^{(1)},\ldots,T^{(N)}).
\tag{3.1}

The reconstruction problem seeks a map

\mathfrak G:\mathcal D\to\operatorname{Met}_{\sigma}(M),
\tag{3.2}

where denotes the set of smooth nondegenerate metrics with a prescribed signature .

The key requirement is that be defined using only the declared relational data and admissible operations.

3.1 Exact reconstruction

Exact reconstruction means

g=\mathfrak G(\mathbf T)
\tag{3.3}

is uniquely determined by the input data.

3.2 Reconstruction up to scale

Two metrics are conformally equivalent if

\widetilde g=\Omega^2g,
\qquad \Omega:M\to(0,\infty)
\tag{3.4}

is smooth.

If the relational data determine only the conformal class

g=\{\Omega^2g:\Omega>0\},
\tag{3.5}

then they determine angles and null directions in the appropriate signature, but not absolute lengths or volume scales.

The conformal class is a valid geometric output, but it is not a unique metric.

3.3 Reconstruction up to a group action

Let act on the class of candidate metrics. If two metrics are considered equivalent under , reconstruction may yield a unique orbit

gH\in\operatorname{Met}{\sigma}(M)/H.
\tag{3.6}

The group must be specified. Possible equivalences include positive rescaling, diffeomorphisms, or a restricted gauge action.

One must distinguish a coordinate transformation from a change of geometric metric: diffeomorphically related metrics are not necessarily identical tensor fields on a fixed manifold, even though they may represent equivalent geometric structures.

3.4 The admissible metric set

For a relational configuration , define

\mathcal M(\mathbf T)

\{g\in\operatorname{Met}_{\sigma}(M):
g\text{ satisfies the specified compatibility conditions with }\mathbf T\}.
\tag{3.7}

The reconstruction question becomes:

* Is nonempty?
* Is it a singleton?
* Is it a single orbit under the declared equivalence group?
* Does it vary smoothly with ?
* Is the resulting structure stable under small perturbations of ?

This formulation prevents the phrase “the tensor determines the metric” from concealing the actual mathematical claim.

4. Algebraic Reconstruction from Tensor Contractions

The most direct reconstruction mechanism is to construct a covariant rank-two tensor from the relational data using operations that do not presuppose a metric.

Suppose the relational configuration includes tensors whose indices can be contracted using the canonical pairing. Let denote a specified contraction polynomial or multilinear contraction rule. It defines

B_{ab}=\mathcal P(\mathbf T)_{ab}.
\tag{4.1}

The intended output is a covariant two-tensor. If

B_{ab}=B_{ba}
\tag{4.2}

and

\det(B_{ab})\neq0,
\tag{4.3}

then is itself a metric of some signature.

This route is mathematically straightforward, but the difficult question is whether the relational data admit a canonical construction of , and whether that construction is unique under the allowed operations.

4.1 A general contraction scheme

Suppose the relational configuration contains a tensor

A^a{}_{bc}\in\Gamma(TM\otimes T^\ast M\otimes T^\ast M)
\tag{4.4}

that is symmetric in its two lower indices:

A^a{}{bc}=A^a{}{cb}.
\tag{4.5}

It defines a bilinear operation on vector fields,

A(X,Y)^a=A^a{}_{bc}X^bY^c.
\tag{4.6}

The trace

\tau_c=A^a{}_{ac}
\tag{4.7}

is a covector field. The trace operation uses only the canonical contraction between the upper index and one lower index.

However, alone does not determine a metric. It is a covector, not a symmetric bilinear form. The tensor may also have no natural contraction yielding a nondegenerate two-tensor. The type of the input constrains which outputs can be constructed without extra structure.

This illustrates an important principle: tensor rank and index variance impose algebraic limits on metric reconstruction.

4.2 Contraction-generated bilinear forms

Suppose a relational configuration supports a natural contraction rule

B_{ab}

\mathcal P_{ab}
\left(T^{(1)},\ldots,T^{(N)}\right).
\tag{4.8}

The word natural here means that the rule is defined using tensor products, permutations of tensor factors, canonical vector-covector pairings, and fixed scalar coefficients, without inserting a metric or another undeclared geometric structure.

If is symmetric and nondegenerate, then

g_{ab}=B_{ab}
\tag{4.9}

is a metric.

If is positive definite, it defines a Riemannian metric. If it has a constant nondegenerate signature, it defines a pseudo-Riemannian metric.

The signature is locally constant on a connected domain as long as the form remains nondegenerate.

4.3 The uniqueness problem

Even if a contraction yields one metric , it does not follow that is the only metric compatible with .

For example, a compatibility condition might require a metric to preserve a given subspace, be invariant under a group, or satisfy a selected tensor identity. Many different metrics can satisfy such conditions.

A rigorous reconstruction theorem must prove either that the contraction rule is canonical and uniquely prescribed, or that every other compatible metric belongs to the same declared equivalence class.

4.4 Proposition: direct contraction reconstruction

Proposition 4.1 — Metric from a canonical bilinear contraction.

Let be a smooth manifold, and let be a smooth relational tensor configuration. Suppose a specified metric-independent contraction rule produces a smooth tensor field

B=\mathcal P(\mathbf T)\in\Gamma(S^2T^\ast M).

If is nondegenerate at every point of , then defines a smooth pseudo-Riemannian metric. If is positive definite everywhere, it defines a Riemannian metric.

Proof.

By construction, is a smooth covariant rank-two tensor and is symmetric. Nondegeneracy gives an invertible linear map at every . Thus satisfies the definition of a pseudo-Riemannian metric. Positive definiteness gives the Riemannian case.

This proposition is a construction theorem, not a uniqueness theorem. Its key assumption is that the contraction rule is already specified. TGTG must explain why that rule is canonically selected by the relational structure rather than arbitrarily chosen from many possibilities.

5. Metric Reconstruction from Endomorphism Data

A different route begins with a tensor that defines linear transformations of tangent spaces. The question becomes whether those transformations constrain the inner product.

Let be a smooth field of endomorphisms, represented locally by .

A metric is compatible with in the self-adjoint sense if

g(AX,Y)=g(X,AY)
\tag{5.1}

for all tangent vectors . In coordinates,

g_{ac}A^c{}_b

g_{bc}A^c{}_a.
\tag{5.2}

This is a linear system for the components of . It can constrain the metric, but usually does not determine it uniquely.

5.1 The linear solution space

At a point , define

\mathcal G_A

\left\{
g\in S^2T_x^\ast M:
g(Au,v)=g(u,Av)
\ \forall u,v
\right\}.
\tag{5.3}

The compatibility condition is linear in . Therefore is a vector subspace of .

Metric candidates lie in the nondegenerate portion of this subspace, restricted to the desired signature.

If , the compatibility condition alone cannot uniquely determine a metric, even when nondegenerate candidates exist.

5.2 A simple nonuniqueness example

Take , where is the identity endomorphism. Then

g(Au,v)=\lambda g(u,v)
=\lambda g(u,v)=g(u,Av)
\tag{5.4}

for every symmetric bilinear form .

Thus every metric of the prescribed signature is compatible with . An endomorphism proportional to the identity provides no information about the metric beyond what was already assumed.

5.3 Multiple endomorphisms

Let be a collection of endomorphisms. Define

\mathcal G_{\mathbf A}

\bigcap_{i=1}^m\mathcal G_{A_i}.
\tag{5.5}

The common compatibility space can be much smaller than the individual spaces. A reconstruction theorem may become possible if the common solution space is one-dimensional and contains a nondegenerate form of the required signature.

5.4 Proposition: uniqueness up to scale

Proposition 5.1 — One-dimensional compatibility space.

At a point , let be a collection of endomorphisms. Suppose

\dim\mathcal G_{\mathbf A}=1
\tag{5.6}

and the nonzero elements of are nondegenerate and have the required signature up to an allowed sign convention. Then the endomorphism compatibility conditions determine a metric at uniquely up to multiplication by a nonzero scalar. If the admissible equivalence is positive rescaling and the signature convention fixes the sign, the metric is determined up to positive scale.

Proof.

Since the solution space is one-dimensional, any two nonzero compatible symmetric bilinear forms satisfy for some nonzero scalar . The signature convention and allowed equivalence restrict the permitted values of .

For a smooth metric field, the pointwise solutions must additionally vary smoothly, and the dimension of the compatibility space must remain constant on the domain under consideration.

The proposition identifies a concrete algebraic route to conformal metric reconstruction. The difficult part is finding tensor configurations for which the one-dimensionality condition follows from meaningful structural hypotheses.

6. Stabilizer Groups and the Metric as an Invariant Form

The symmetry group of a tensor can reveal which bilinear forms are compatible with it. This gives a second major reconstruction mechanism.

At a point , let , and let be a tensor on . Its stabilizer in is

G_T

\{A\in\mathrm{GL}(V):A\cdot T=T\}.
\tag{6.1}

The action is the natural tensor representation induced by the linear transformation .

A bilinear form is -invariant if

g(Av,Aw)=g(v,w)
\tag{6.2}

for every and .

Define the space of invariant symmetric bilinear forms:

\operatorname{Inv}_2(G_T)

\left(S^2V^\ast\right)^{G_T}.
\tag{6.3}

This is the vector space of symmetric bilinear forms fixed by the stabilizer action.

6.1 The stabilizer criterion

If

\dim\operatorname{Inv}_2(G_T)=1
\tag{6.4}

and the unique invariant line contains a nondegenerate form of the desired signature, then the stabilizer determines that metric up to scale.

The logic is straightforward: all invariant symmetric bilinear forms lie on the same one-dimensional line, so any two nonzero invariant forms are proportional.

This is a strong algebraic condition. It does not follow from the tensor rank alone, and it does not guarantee that the invariant line contains a metric of the desired signature.

6.2 Why the stabilizer matters

A tensor with a large stabilizer may be too symmetric to determine a metric uniquely. A tensor with a smaller, more restrictive stabilizer may determine more structure.

For example, a generic tensor may have a very small stabilizer, but a trivial stabilizer does not itself imply that a unique invariant metric exists. If contains only the identity, every bilinear form is invariant under that group.

Thus the relevant question is not simply the size of the stabilizer. It is the dimension and signature content of its invariant symmetric bilinear forms.

6.3 A useful distinction

There are two different reconstruction statements:

* The tensor itself algebraically generates a bilinear form .
* The symmetry group preserves a unique metric line.

The first is a construction problem. The second is an invariant-theory problem. A tensor may satisfy one condition without satisfying the other.

6.4 Smooth reconstruction over a manifold

Suppose is a smooth tensor field on , and the stabilizer-invariant line

\mathcal L_x

\left(S^2T_x^\ast M\right)^{G_{T_x}}
\tag{6.5}

has constant dimension one.

If the family forms a smooth line subbundle of , and each fiber contains a nondegenerate bilinear form of the required signature, then it defines a conformal metric structure, provided the line can be oriented or normalized consistently to select the desired metric ray.

This last condition is not automatic. A real line bundle need not possess a globally defined nowhere-zero section, and the invariant line may fail to distinguish from . Global topology and signature conventions therefore enter the reconstruction problem.

7. The Main Metric-Reconstruction Theorem

The preceding sections yield a general theorem separating pointwise algebraic uniqueness from global differential-geometric existence.

Definition 7.1 — Relational metric selector

A relational metric selector on a domain is an assignment

\mathfrak g_x:\mathbf T_x\longmapstog_x
\tag{7.1}

that assigns to the relational data at each point a unique equivalence class of nondegenerate symmetric bilinear forms, where the equivalence relation is explicitly specified.

The assignment must be natural under admissible changes of frame: if the relational data are transformed by a change of basis, the selected metric class must transform as a covariant bilinear form.

Theorem 7.1 — Conditional reconstruction of a conformal metric

Let be a smooth manifold and let be a smooth configuration of tensor fields on . Suppose that on an open set :

* Pointwise existence: For every , the relational data determine at least one nondegenerate symmetric bilinear form of a prescribed signature.
* Pointwise uniqueness up to scale: Every two compatible forms at differ by a positive scalar: \\\widetilde g_x=\\lambda(x)g_x,\\qquad \\lambda(x)>0. \\tag{7.2} \\
* Naturality: The selected equivalence class transforms tensorially under changes of local frame.
* Smoothness: The pointwise classes form a smooth conformal structure on .
* Signature consistency: The signature is constant on .

Then the relational tensor configuration determines a conformal metric structure on , unique among conformal structures satisfying the same compatibility conditions.

If, in addition, the relational data determine a smooth positive scale normalization that selects one representative from each conformal class, then they determine a unique metric in that normalized class.

Proof.

By assumptions 1 and 2, each point has a unique conformal class of compatible bilinear forms. Assumptions 3 and 4 ensure that these classes are not coordinate artifacts and assemble into a smooth conformal structure. Assumption 5 guarantees a consistent metric signature throughout the domain. Hence the classes define .

If a smooth positive scale normalization is supplied, each class contains exactly one representative satisfying that normalization. This representative defines the unique normalized metric.

7.1 Interpretation

The theorem gives the desired conditional result, but its hypotheses identify the real work of TGTG.

The first two assumptions are algebraic: the relational data must admit compatible metrics and reduce their ambiguity to a positive scale. The next two are differential-geometric: pointwise choices must transform correctly and fit together smoothly. The final assumption controls the signature.

The theorem does not assert that a generic tensor configuration satisfies these conditions. It states what follows if those conditions are proved for a particular class of relational tensor systems.

7.2 Exact metric reconstruction

A stronger version replaces assumption 2 with

\widetilde g_x=g_x
\tag{7.3}

for every pair of compatible forms. In that case, the relational data determine the metric pointwise without a scale ambiguity.

An equivalent construction is to prove that the data determine a unique nondegenerate symmetric two-tensor , normalized by a canonical scalar relation or another intrinsic condition.

7.3 The theorem’s limits

The theorem does not identify a universal tensor whose existence is guaranteed on every manifold. It also does not establish that a finite set of contractions will always produce the required metric.

Its contribution is to formalize the conditions under which a metric-reconstruction claim is valid and to expose the assumptions that any proposed concrete model must prove.

8. Scale Selection: From Conformal Geometry to a Unique Metric

Determining a conformal class is weaker than determining a metric. If

\widetilde g=\Omega^2g,
\tag{8.1}

then angles and conformal light cones are preserved, but lengths and volumes change.

A second relational quantity is needed if the objective is to recover an exact metric rather than its conformal class.

8.1 Scalar normalization

Suppose the relational data determine a conformal metric and a scalar functional satisfying

S(\Omega^2g)=\mathcal T(\Omega,g)
\tag{8.2}

for a known transformation rule .

If the normalization equation

S(g)=s_0
\tag{8.3}

has exactly one admissible representative within each conformal class, the scale is fixed.

The uniqueness of this representative must be proved. Some normalization equations admit multiple solutions or no global solution.

8.2 Volume normalization

For an -dimensional Riemannian metric,

dV_{\Omega^2g}=\Omega^n\,dV_g.
\tag{8.4}

If is compact and the conformal factor is restricted to a positive constant , then

\operatorname{Vol}(M,c^2g)
=c^n\operatorname{Vol}(M,g).
\tag{8.5}

Given a target volume , there is a unique positive constant

c=
\left(
\frac{V_0}{\operatorname{Vol}(M,g)}
\right)^{1/n}
\tag{8.6}

that produces the target volume.

This fixes a constant scale ambiguity. It does not generally fix an arbitrary spatially varying conformal factor . A total-volume constraint alone is insufficient to determine a metric uniquely from a conformal class.

8.3 Scale from a relational density

Suppose the relational data also determine a positive volume density . A metric with the same orientation convention has volume density

dV_g=\sqrt{|\det(g_{ab})|}\,|dx^1\cdots dx^n|.
\tag{8.7}

If the metric must satisfy

dV_g=\nu,
\tag{8.8}

then the determinant magnitude is constrained. However, a determinant condition alone does not generally determine all metric components. Additional compatibility conditions are still needed.

8.4 Scale from curvature or an operator

Another possible normalization is to impose a scalar condition involving curvature or a differential operator. For example,

Rg=R_0
\tag{8.9}

is a geometric constraint on the scalar curvature.

Such a condition can select a representative in certain conformal classes under suitable hypotheses, but existence and uniqueness are delicate and depend on the dimension, topology, regularity, and sign conditions. It must not be treated as a universal normalization theorem.

Conclusion of this section: exact metric reconstruction generally requires two kinds of information—relational information fixing the conformal or metric direction, and scale information fixing the remaining normalization. A scale condition should be justified by a uniqueness result rather than chosen for convenience.

9. An Algebraic Rigidity Theorem for Relational Endomorphisms

The stabilizer criterion can be turned into a pointwise reconstruction theorem that is directly testable for a given tensor system.

Let be a real vector space of dimension . Let be a family of endomorphisms derived from the relational tensors by metric-independent operations.

Define the common symmetric bilinear-form space

\mathcal B(\mathcal A)

\left\{
b\in S^2V^\ast:
b(Au,v)=b(u,Av)
\ \text{for all }A\in\mathcal A
\right\}.
\tag{9.1}

This is a linear subspace of .

Theorem 9.1 — Algebraic metric-line rigidity

Suppose:

* ;
* every nonzero element of is nondegenerate;
* the desired signature is realized by a representative of this line;
* the sign or positive-ray convention is specified.

Then determines a unique metric line of the prescribed signature, and hence a unique conformal metric at the point.

Proof.

Because is one-dimensional, any two nonzero elements satisfy for some nonzero scalar . By assumption 2, the line contains no degenerate nonzero forms. Assumptions 3 and 4 select the admissible signature and ray. Thus the relational endomorphism family determines a unique metric line.

9.1 Computational formulation

Choose a basis of , and represent a symmetric bilinear form by a symmetric matrix . Each compatibility condition becomes a linear equation in the independent entries of :

A^\mathsf{T}G=GA.
\tag{9.2}

Stacking the linear equations from all gives a homogeneous linear system

\mathscr L_{\mathcal A}(G)=0.
\tag{9.3}

The dimension of its kernel is

\dim\mathcal B(\mathcal A)

\frac{n(n+1)}2-\operatorname{rank}\mathscr L_{\mathcal A}.
\tag{9.4}

Therefore, one-dimensionality can be tested using finite-dimensional linear algebra whenever the relational system produces a finite family of endomorphisms.

This provides a concrete diagnostic:

* kernel dimension zero: no nonzero symmetric form satisfies the conditions;
* kernel dimension one: a unique metric line is possible, subject to nondegeneracy and signature;
* kernel dimension greater than one: the compatibility equations alone do not select a unique metric line.

A one-dimensional kernel is necessary for this particular reconstruction route, but the kernel must still be checked for degeneracy.

9.2 Globalization

For a smooth family , the kernel of the corresponding bundle map must have constant rank to define a smooth subbundle under the standard regularity assumptions.

If the kernel is a smooth line subbundle of , it defines a conformal metric candidate provided its nonzero sections are nondegenerate with the required signature.

A global representative may require a trivialization or an appropriate positive-ray structure. Thus pointwise algebraic uniqueness does not automatically imply a globally defined metric tensor.

10. Obstructions to Metric Reconstruction

The proposed theory is only as strong as its treatment of cases where reconstruction fails.

10.1 Insufficient tensor rank or type

A scalar field contains no directional information about a metric. A single covector field selects a hyperplane distribution where it is nonzero, but generally leaves many bilinear forms compatible with that distribution.

The tensor type determines the available operations. Metric-independent contractions cannot arbitrarily lower or raise indices.

10.2 Degenerate contraction

A canonical contraction may yield a symmetric tensor with

\det B=0.
\tag{10.1}

Such a tensor is not a metric. It may encode a degenerate geometric structure, such as a distinguished null direction or a lower-rank pairing, but a nondegenerate metric cannot be claimed without an additional reconstruction step.

10.3 Excessive symmetry

If the relational tensor is invariant under a group that preserves many distinct bilinear forms, symmetry does not select a unique metric.

For instance, if the stabilizer is the identity group, every bilinear form is invariant under it. A small stabilizer is not enough; the invariant-form space itself must be analyzed.

10.4 Multiple compatible signatures

A linear compatibility system may admit nondegenerate forms with different signatures. Unless the relational data determine the signature, the result is not a unique metric structure.

In particular, a one-dimensional solution space can still contain both and . These have opposite overall sign conventions, and the admissible equivalence must be stated.

10.5 Global topological obstruction

A pointwise family of metric lines may fail to admit a global smooth representative if the associated line bundle is nontrivial. Local reconstruction does not settle global existence.

Likewise, the existence of a nondegenerate metric of a specified signature on a given manifold can impose topological conditions.

10.6 Insufficient differential information

An algebraically reconstructed metric does not automatically determine a connection, curvature, or geodesic structure beyond what follows from that metric and the chosen additional data.

If the intended theory claims that the relational tensor determines the full differential geometry, it must also explain how derivatives of the relational data determine the required connection or other geometric fields.

10.7 Non-identifiability

Two non-equivalent relational configurations may induce the same metric. This is not a failure of metric reconstruction if the target is only the metric, but it prevents the metric from serving as a complete invariant of the original relational structure.

Metric reconstruction and reconstruction of the entire relational tensor are different inverse problems.

11. Tensor Networks as Relational Geometric Data

Tensor networks provide a natural setting for expressing geometry through local tensors and their contraction architecture. But a network does not, by itself, guarantee a metric on the manifold being modeled.

A tensor network consists of a graph or hypergraph together with tensors assigned to vertices or edges and a specified pattern of index contractions. The network evaluates a multilinear or scalar quantity when its internal indices are contracted according to the prescribed rules.

11.1 Network architecture

Let be a graph. Assign a tensor to each vertex , with index spaces associated to incident edges. An edge carries a specified pairing between its endpoint index spaces.

A complete contraction may be written abstractly as

Z_\Gamma

\operatorname{Contr}{\Gamma}
\left(\bigotimes{v\in V_\Gamma}T_v\right).
\tag{11.1}

The contraction map depends on the edge pairings. If those pairings are given by dual vector spaces, contraction can be metric-independent. If an edge pairing is introduced through an inner product, then the metric information has already entered the network and cannot be claimed as an output of the same reconstruction without further explanation.

11.2 Local relations and emergent bilinear forms

Suppose the network produces a two-index object

B_{ab}(\Gamma,\mathbf T)
\tag{11.2}

with both indices in the cotangent space associated with a target point or effective tangent space.

If the construction is covariant, symmetric, smooth in the relevant continuum limit, and nondegenerate, it can define a candidate metric.

The difficult questions are:

* What are the index spaces associated with ?
* How is the network related to a smooth manifold?
* Which edge pairings are primitive?
* Does the construction use a hidden metric?
* Why is the output symmetric?
* What guarantees nondegeneracy?
* Is the output invariant under changes in the network representation?

These conditions must be established before interpreting geometrically.

11.3 Gauge freedom in tensor-network representations

Tensor-network descriptions often admit internal basis changes that leave the fully contracted object unchanged. If a network representation is transformed by invertible changes of basis on internal index spaces, its local tensors may change while the represented global quantity remains the same.

A reconstructed metric should be invariant under these representation redundancies, or transform according to a declared equivalence. Otherwise it describes a chosen network gauge rather than an intrinsic geometric output.

11.4 Coarse-graining and effective geometry

Let denote a coarse-graining operation on network data. A scale-dependent relational configuration is

\mathbf T^{(k+1)}=\mathcal R(\mathbf T^{(k)}).
\tag{11.3}

One may ask whether the corresponding effective bilinear forms satisfy

g^{(k+1)}\approx g^{(k)}
\tag{11.4}

under a suitable identification of the effective spaces, or whether they converge to a fixed geometric structure.

This requires a precise definition of how tangent or cotangent spaces at different coarse-graining scales are compared. Without such an identification, equation (11.4) is only suggestive notation.

A successful result would prove that the effective metric is stable under a specified renormalization or coarse-graining procedure and quantify its dependence on the microscopic relational data.

11.5 Tensor-network reconstruction as a research program

The network route is promising because it separates local relational data from global contraction structure. However, it is not yet a general theorem of emergent geometry.

A rigorous result would need to provide:

* a defined family of local tensor spaces;
* metric-independent edge pairings;
* a continuum or effective-manifold limit;
* a covariant two-tensor construction;
* symmetry and nondegeneracy proofs;
* a uniqueness theorem;
* control of representation and coarse-graining ambiguities.

Only then could the network be said to reconstruct geometry rather than merely encode data on a preselected geometric substrate.

12. From Metric Reconstruction to Connection and Curvature

A metric is not the entirety of differential geometry. If TGTG aims to derive a full geometric structure, it must address how relational data determine derivatives, parallel transport, and curvature.

12.1 The metric-induced connection

Once a smooth nondegenerate metric has been reconstructed, there exists a unique torsion-free connection satisfying

\nabla g=0.
\tag{12.1}

This is the Levi-Civita connection. In local coordinates,

\Gamma^a{}_{bc}

\frac12g^{ad}
\left(
\partial_b g_{cd}
+\partial_c g_{bd}
-\partial_d g_{bc}
\right).
\tag{12.2}

Equation (12.2) uses both the reconstructed metric and its inverse. Thus, after metric reconstruction, the Levi-Civita connection follows uniquely from established differential geometry.

But the result does not show that the original relational tensor determines every possible connection. Connections with torsion or nonmetricity require additional data or different compatibility conditions.

12.2 Independent connection data

Suppose the relational configuration includes an affine connection or an equivalent connection-like tensor. Metric compatibility can then be expressed as

\nabla_a g_{bc}=0.
\tag{12.3}

If torsion is also constrained to vanish, the connection is Levi-Civita for . If torsion or nonmetricity is allowed, the relation between and changes.

An independently supplied connection may constrain the metric, but metric compatibility alone need not select a unique metric. The space of parallel metrics can have dimension greater than one, depending on the holonomy representation.

12.3 Holonomy and invariant bilinear forms

Parallel transport around loops generates a holonomy group acting on tangent spaces. A metric preserved by the connection corresponds to a holonomy-invariant nondegenerate symmetric bilinear form.

Thus the invariant-form method from Section 6 has a differential-geometric counterpart:

\operatorname{Inv}_2(\operatorname{Hol}(\nabla))

\left(S^2T_x^\ast M\right)^{\operatorname{Hol}_x(\nabla)}.
\tag{12.4}

If this space is one-dimensional and contains a nondegenerate form of the desired signature, the connection determines a metric up to scale.

This is a genuine geometric reconstruction criterion. It depends on the holonomy representation and its invariant bilinear forms, not simply on the existence of an affine connection.

12.4 Curvature

Once a connection is specified, its curvature is

R(X,Y)Z

\nabla_X\nabla_YZ
-\nabla_Y\nabla_XZ
-\nabla_{X,Y}Z.
\tag{12.5}

In components,

R^a{}_{bcd}

\partial_c\Gamma^a{}{db}
-\partial_d\Gamma^a{}{cb}
+\Gamma^a{}{ce}\Gamma^e{}{db}
-\Gamma^a{}{de}\Gamma^e{}{cb},
\tag{12.6}

using the stated index convention.

If the connection is the Levi-Civita connection of the reconstructed metric, curvature follows from and its derivatives. If the relational data include curvature-like tensors independently, their compatibility with the reconstructed metric imposes additional constraints.

12.5 Hierarchy of geometric reconstruction

The mathematically justified hierarchy is therefore conditional:

\boxed{
\text{Relational tensors}
\to
\text{metric or conformal class}
\to
\text{compatible connection}
\to
\text{curvature}
}
\tag{12.7}

Each arrow requires a separate existence and uniqueness argument. The first is the central problem of TGTG; the later arrows are standard once the relevant assumptions are met.

13. An Illustrative Model: Recovering a Metric from a Family of Linear Operators

A useful test model is a smooth family of endomorphisms

A_1,\ldots,A_m:TM\to TM
\tag{13.1}

whose common self-adjointness conditions are intended to select the metric.

13.1 The algebraic system

In a local frame, let be the symmetric matrix of a candidate metric. For each operator , impose

A_i^\mathsf{T}G=GA_i.
\tag{13.2}

This is a homogeneous linear system in the independent entries of .

If its kernel is one-dimensional and its nonzero generator is nondegenerate with the required signature, the metric line is uniquely determined.

13.2 A concrete two-dimensional example

Consider the fixed operator

A=
\begin{pmatrix}
1&0\\
0&2
\end{pmatrix}
\tag{13.3}

on . Let

G=
\begin{pmatrix}
a&c\\
c&b
\end{pmatrix}.
\tag{13.4}

The self-adjointness condition yields

\begin{pmatrix}
a&c\\
2c&2b
\end{pmatrix}

\begin{pmatrix}
a&2c\\
c&2b
\end{pmatrix}.
\tag{13.5}

Thus , so the compatible symmetric forms are

G=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix}.
\tag{13.6}

The compatibility space is two-dimensional. If , these forms are positive definite, and infinitely many Riemannian metrics are compatible with .

The operator selects the coordinate eigendirections as orthogonal, but it does not determine the relative scale of those directions.

13.3 Adding relational constraints

Suppose a second operator or an additional tensor relation imposes

b=\kappa a,
\qquad \kappa>0
\tag{13.7}

with determined intrinsically by the relational data.

Then

G=a
\begin{pmatrix}
1&0\\
0&\kappa
\end{pmatrix}.
\tag{13.8}

The remaining ambiguity is one positive scalar. The conformal metric is fixed.

If an independent normalization determines , the metric is uniquely recovered.

This model demonstrates the two-stage structure of reconstruction:

* algebraic constraints eliminate incompatible metric components;
* a normalization condition removes the residual scale.

It also illustrates why the uniqueness claim must be derived from the rank of the compatibility system rather than inferred from the mere presence of several tensors.

14. Stability of the Reconstructed Metric

Even when a relational configuration determines a unique metric, small changes in the input may produce large changes in the output. A useful reconstruction theory should therefore study conditioning and perturbation stability.

Let be a relational configuration and suppose the metric is reconstructed by

g=\mathfrak G(\mathbf T).
\tag{14.1}

Perturb the input:

\mathbf T\mapsto\mathbf T+\delta\mathbf T.
\tag{14.2}

If is differentiable in an appropriate sense, then

\delta g

D\mathfrak G_{\mathbf T}\\delta\\mathbf T
+o(\|\delta\mathbf T\|).
\tag{14.3}

A local condition number can be defined relative to chosen norms:

\kappa_{\mathfrak G}(\mathbf T)

\sup_{\delta\mathbf T\neq0}
\frac{\|D\mathfrak G_{\mathbf T}\\delta\\mathbf T\|}
{\|\delta\mathbf T\|}.
\tag{14.4}

This quantity measures first-order sensitivity. It depends on the chosen norms and representation, so those choices must be documented.

14.1 Degeneracy and ill-conditioning

If a reconstructed metric approaches degeneracy, then

\det(g_{ab})\to0.
\tag{14.5}

The inverse metric becomes ill-conditioned or ceases to exist at the degeneracy boundary. Consequently, small perturbations in the relational data may cause large changes in the reconstructed inverse metric, signature, or derived connection.

A complete theory should identify the degeneracy locus in relational-data space and determine whether it is avoidable, generic, or associated with a meaningful change of geometric type.

14.2 Rank changes

For the linear compatibility system of Section 9, reconstruction depends on the kernel of . If the rank of this operator changes under perturbation, the dimension of the metric-compatible space may jump.

At such points, a unique metric line may cease to exist or may become non-unique. Thus a rank-one reconstruction theorem is naturally accompanied by a regularity condition: the kernel dimension should remain constant on the region where the metric is claimed to be smoothly determined.

14.3 Stability criterion

A useful reconstruction theorem should therefore establish not only uniqueness but also one of the following:

* continuity of ;
* differentiability of ;
* a quantitative perturbation bound;
* a characterization of the singular set where reconstruction fails.

Without such a result, the metric may be mathematically determined but practically unstable.

15. A Reconstruction Audit: Necessary Questions for Any Proposed Model

Every concrete proposal within TGTG should pass the following audit before its metric is described as emergent.

15.1 Input audit

* Are the tensor fields defined without a metric?
* Are the vector and covector spaces, index types, and transformation laws explicit?
* Does any contraction use an undeclared metric, inverse metric, Hodge star, or metric-dependent volume form?
* Are the primitive algebraic operations listed completely?

15.2 Existence audit

* Is a candidate symmetric bilinear form actually constructed?
* Is its smoothness established?
* Is nondegeneracy proved?
* Is the signature determined or merely assumed?
* Are the global topological conditions satisfied?

15.3 Uniqueness audit

* What is the full space of compatible metrics?
* What is its dimension?
* Is the metric unique, unique up to scale, or unique only up to a group action?
* Could two non-equivalent metrics satisfy every stated constraint?
* If a normalization is used, does it select exactly one representative?

15.4 Naturalness audit

* Does the reconstruction commute with coordinate transformations?
* Is it invariant under internal tensor-network basis changes?
* Does it respect the declared equivalence relation?
* Is the result independent of arbitrary choices of local frame?

15.5 Differential audit

* Do the pointwise metric candidates fit together into a smooth global field?
* Is the signature constant?
* Does the reconstructed metric admit the intended connection?
* Are curvature claims derived from that connection rather than inserted as hidden assumptions?

15.6 Novelty audit

* Does the result improve on known invariant-theory or holonomy criteria?
* Does it identify a new class of relational tensors for which the invariant-form space is provably one-dimensional?
* Does it provide a new reconstruction algorithm with a theorem of correctness?
* Does it establish a stability or robustness bound absent from the existing model?

A proposal that fails an audit item may still be useful, but its claim must be narrowed to match what is actually established.

16. Principal Research Conjecture: Relational Metric Rigidity

The central research program can now be stated in a form that distinguishes an ambitious hypothesis from established results.

Conjecture 16.1 — Relational metric rigidity

There exist nontrivial classes of smooth relational tensor configurations for which the following conditions can be derived from the tensor relations themselves:

* the space of compatible symmetric bilinear forms is nonempty;
* that space is one-dimensional at each point;
* its nonzero elements are nondegenerate and have a prescribed signature;
* the resulting metric line varies smoothly;
* a specified scalar normalization, when required, uniquely selects a metric representative.

For such classes, the relational tensor configuration determines a unique conformal metric, or a unique normalized metric, without assuming a metric as primitive input.

Status: Research conjecture in its broad form. The conditional theorems above establish what follows when the required hypotheses hold, but they do not establish that an important new class of tensor systems satisfies those hypotheses.

16.1 Stronger target: classification of admissible relational tensors

Let be a class of relational tensor configurations. Define an equivalence relation that identifies configurations related by the allowed frame changes, tensor-network gauge transformations, or other specified redundancies.

The stronger objective is a classification theorem of the form

\mathbf T_1\sim\mathbf T_2
\quad\Longleftrightarrow\quad
\mathfrak I(\mathbf T_1)=\mathfrak I(\mathbf T_2),
\tag{16.1}

where includes the reconstructed metric class and the residual relational data not captured by that metric.

This is stronger than reconstructing . Different relational tensors can determine the same metric while retaining different higher-order structures. A metric is therefore generally not a complete invariant of the tensor configuration that generated it.

16.2 A possible rigidity mechanism

One possible route is to classify the invariant bilinear forms of the stabilizer group:

\operatorname{Inv}2(G{\mathbf T})

\left(S^2V^\ast\right)^{G_{\mathbf T}}.
\tag{16.2}

If the dimension of this space is one and its nonzero elements are nondegenerate, the tensor stabilizer fixes a metric line.

The substantive discovery would be to derive these conditions from a meaningful set of tensor identities or a tensor-network architecture, and then prove that the resulting reconstruction is stable and globalizable.

17. Research Program and Milestones

A rigorous development of TGTG should proceed from algebraic reconstruction toward differential and network-based geometry.

Stage I — Finite-dimensional invariant theory

Classify tensor representations whose stabilizer groups admit exactly one invariant symmetric bilinear form up to scale.

Deliverables:

* explicit classes of tensors;
* a description of their stabilizers;
* dimension calculations for invariant-form spaces;
* proofs of nondegeneracy and signature;
* examples showing failure outside the classified class.

Stage II — Smooth bundle reconstruction

Extend the pointwise results to smooth tensor fields on manifolds.

Deliverables:

* constant-rank conditions;
* smoothness of the metric line;
* global existence criteria;
* treatment of line-bundle and signature obstructions;
* a scale-selection theorem where possible.

Stage III — Differential reconstruction

Determine when relational tensors select not only a metric but a connection, and whether the connection is necessarily Levi-Civita.

Deliverables:

* holonomy-based uniqueness criteria;
* conditions for metric compatibility;
* explicit treatment of torsion and nonmetricity;
* curvature identities derived from the reconstructed fields.

Stage IV — Tensor-network realization

Specify a class of tensor networks whose contraction rules produce candidate bilinear forms without using a metric-dependent pairing.

Deliverables:

* a defined network model;
* gauge-invariance results;
* a continuum-limit theorem or finite-dimensional effective-geometry theorem;
* symmetry and nondegeneracy proofs;
* a reconstruction uniqueness result.

Stage V — Stability and universality

Establish whether the reconstruction remains valid under perturbations of the relational data and whether the same mathematical criteria transfer across multiple model classes.

Deliverables:

* condition-number bounds;
* degeneracy and rank-change criteria;
* compositionality results;
* explicit limits on the domains where the framework applies.

Stage VI — Comparison with existing geometry

Identify which results are direct applications of established invariant theory, holonomy theory, or differential geometry, and isolate any genuinely new theorem.

The aim is not to rename existing results. It is to find a class of relational tensor systems for which metric reconstruction becomes demonstrably canonical, unique, and robust.

18. Discussion: What “Geometry Before Metric” Can Mean Precisely

The phrase geometry before metric can refer to several mathematically different situations.

Premetric algebraic structure. Tensor fields and algebraic relations exist on a manifold before any metric is selected. This is mathematically standard and does not itself imply metric emergence.

Conformal structure. Relational data determine null directions or angles, but leave a positive scale undetermined. This gives a conformal geometry rather than a unique metric.

Metric reconstruction. Algebraic or differential constraints reduce the admissible metrics to one equivalence class, after which the metric can be constructed explicitly.

Full geometric reconstruction. The data determine a metric together with the relevant connection and other geometric structures, with each step justified by separate theorems.

Effective geometry from networks. A network model defines relational data whose large-scale or continuum behavior is shown to converge to a metric structure. This requires a model-specific limit theorem.

These meanings should not be collapsed into one claim. A conformal reconstruction theorem is already significant, but it does not establish a unique length scale. A pointwise algebraic theorem does not establish a smooth global metric. A metric reconstruction theorem does not establish a dynamical theory of gravity or derive physical spacetime.

The strongest version of TGTG would establish a canonical reconstruction mechanism from a clearly specified class of relational tensors and prove that its output is independent of arbitrary choices.

19. Conclusions

The Tensor Genesis Theory of Geometry investigates whether metric geometry can be reconstructed from relational tensor data without taking a metric as a primitive input.

The mathematical analysis yields several firm conclusions.

First, tensors can be defined and manipulated on smooth manifolds without a metric. Canonical vector-covector contractions are available, but lowering or raising indices and applying metric-dependent operations require additional structure.

Second, a metric can be reconstructed directly when the relational data canonically generate a symmetric, nondegenerate covariant two-tensor. Such a construction proves existence, but uniqueness still requires justification.

Third, a collection of endomorphisms or a tensor stabilizer group can constrain the compatible symmetric bilinear forms. When the relevant invariant-form space is one-dimensional and contains a nondegenerate form of the desired signature, a metric line is uniquely determined.

Fourth, pointwise uniqueness is insufficient for a global geometric result. Smoothness, signature consistency, global bundle structure, and scale normalization must also be addressed.

Fifth, tensor networks provide a promising language for relational construction, but they do not automatically produce a metric. Their edge pairings, gauge freedoms, effective spaces, and continuum limits must be defined and analyzed explicitly.

The central theorem of the framework is conditional: if relational tensor data determine a unique smooth nondegenerate metric class and, when needed, a unique scale, then they determine the corresponding metric geometry. The research challenge is to identify important classes of relational structures for which these hypotheses follow from the tensor relations themselves.

The governing principle is therefore:

\boxed{
\text{Relational structure determines geometry only when}
}\boxed{
\text{its admissible metric space is provably rigid.}
}

The central open problem is to discover which tensor relations generate that rigidity, which obstructions prevent it, and whether a common reconstruction theory can connect algebraic invariant theory, differential geometry, and tensor-network constructions without importing the metric through an undeclared assumption.

20. Selected Mathematical Foundations

The framework is connected to established work in differential geometry, invariant theory, and tensor networks. These references provide the mathematical background against which any novelty claim should be assessed.

* Kobayashi, S., and Nomizu, K. (1963–1969). Foundations of Differential Geometry, Volumes I–II. Wiley.
* Lee, J. M. (2018). Introduction to Riemannian Manifolds. 2nd ed., Springer.
* O’Neill, B. (1983). Semi-Riemannian Geometry with Applications to Relativity. Academic Press.
* Weyl, H. (1939). The Classical Groups: Their Invariants and Representations. Princeton University Press.
* Sternberg, S. (1964). Lectures on Differential Geometry. Prentice-Hall.
* Besse, A. L. (1987). Einstein Manifolds. Springer.
* Penrose, R. (1971). “Applications of Negative Dimensional Tensors.” In Combinatorial Mathematics and Its Applications, Academic Press.
* Bridgeman, M., Chubb, C. T., and Flammia, S. T. (2016). “Tensor Networks and Entanglement.” Annals of Physics, 370, 1–32.
* Orús, R. (2014). “A Practical Introduction to Tensor Networks: Matrix Product States and Projected Entangled Pair States.” Annals of Physics, 349, 117–158.
* Baez, J. C., and Muniain, J. P. (1994). Gauge Fields, Knots and Gravity. World Scientific.

These foundations already contain substantial results on metrics, invariant tensors, holonomy, conformal structure, and tensor-network representations. TGTG becomes a distinct mathematical contribution only where it proves new reconstruction, uniqueness, stability, or cross-domain classification theorems beyond those existing results.

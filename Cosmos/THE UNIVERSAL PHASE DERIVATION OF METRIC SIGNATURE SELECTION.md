UNIVERSAL PHASE THEORY

THE UNIVERSAL PHASE DERIVATION OF METRIC SIGNATURE SELECTION

Phase Stability, Causal Propagation, and the Dynamical Selection of Lorentzian Geometry

⸻

Abstract

Universal Phase Theory (UPT) proposes that phase organization is more fundamental than spacetime geometry. The preceding Phase-Web and Phase Causality programs suggest the hierarchy

[
\Phi
\rightarrow
\mathcal N_\Phi
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
g^\Phi_{\mu\nu}.
]

A critical unresolved question lies between causal structure and metric reconstruction:

[
\boxed{
\text{Why should the emergent metric have Lorentzian signature?}
}
]

A generic bilinear construction such as

[
g^\Phi_{ab}

T_{ai}\chi_\Phi^{ij}T_{bj}
]

does not answer this question. If the susceptibility (\chi_\Phi) is positive definite, the resulting metric is naturally Euclidean. If it is indefinite, the signature depends on the number of positive and negative eigenvalues. Nothing in the algebra alone forces

[
(-,+,+,+).
]

This paper therefore treats metric signature as an independent UPT emergence gate.

The central hypothesis investigated is that Lorentzian signature may arise from a dynamical spectral asymmetry of the phase system:

[
\boxed{
\text{phase stability}
\rightarrow
\text{spectral index}
\rightarrow
\text{causal propagation}
\rightarrow
(-,+,+,+).
}
]

The proposed mechanism is not that one simply postulates “one unstable direction and three stable directions.” Rather, the theory must demonstrate that a stable propagating phase vacuum possesses exactly one distinguished negative/kinetic direction and three positive spatial directions, while eliminating alternative signatures such as

[
(+,+,+,+),
\qquad
(-,-,+,+),
\qquad
(-,+,+,+,+),
]

and more general multi-cone or indefinite structures.

The analysis establishes several important structural facts.

First, Sylvester’s law of inertia implies that a nonsingular congruence transformation cannot change the signature of the underlying bilinear form. Therefore the map (T) cannot manufacture Lorentzian signature from a positive-definite susceptibility.

Second, stability and Lorentzian signature are not equivalent. A Lorentzian Hessian does not automatically mean physical instability; conversely, a positive-definite Euclidean Hessian does not produce relativistic causal propagation.

Third, the appropriate object for signature selection is likely not the static susceptibility alone but the principal kinetic/propagation structure of the phase equations. The principal symbol determines characteristics, and characteristics determine causal cones. A Lorentzian metric can then arise as the quadratic form whose null cone coincides with the phase propagation cone.

The paper develops a candidate Phase Signature Selection Principle, several spectral and dynamical mechanisms, a no-go theorem for naive susceptibility-based derivation, a conditional theorem for Lorentzian emergence, numerical diagnostics, falsification criteria, and a complete claim ledger.

The current conclusion is deliberately conservative:

[
\boxed{
\text{UPT does not yet derive }(-,+,+,+).
}
]

However, the analysis identifies a precise route by which it could:

[
\boxed{
\Phi
\rightarrow
\mathcal L_\Phi
\rightarrow
\text{phase spectral structure}
\rightarrow
\text{single hyperbolic cone}
\rightarrow
[g^\Phi]
\rightarrow
(-,+,+,+).
}
]

If this route can be established without importing time, Lorentzian geometry, or a preferred signature, metric signature selection would become a genuine structural prediction of UPT rather than a geometric assumption.

⸻

I. INTRODUCTION

A theory that claims spacetime is emergent must explain more than the existence of a metric.

It must explain why the metric has the signature that it does.

The observed local spacetime interval has Lorentzian form

[
ds^2

-c^2dt^2
+
dx^2+dy^2+dz^2
]

or, in units (c=1),

[
ds^2

-dt^2+dx^2+dy^2+dz^2.
]

Its signature is

[
(-,+,+,+).
]

This sign structure is not cosmetic.

It determines:

* timelike directions,
* spacelike directions,
* null propagation,
* causal ordering,
* finite signal speed,
* proper time,
* relativistic kinematics,
* hyperbolic evolution.

If UPT derives spacetime from phase organization, it must therefore explain:

[
\boxed{
\text{Why one direction is temporally distinguished from three spatial directions.}
}
]

This paper addresses that problem directly.

⸻

II. THE SIGNATURE GATE

The UPT metric construction has previously been represented schematically as

[
g^\Phi_{ab}

T_{ai}\chi_\Phi^{ij}T_{bj}.
]

Here (T) maps phase-space variations into emergent geometric directions and

[
\chi_\Phi

\mathcal L_\Phi^{-1}
]

is a phase susceptibility where defined.

The signature question is:

[
\boxed{
\operatorname{sign}(g^\Phi)

?
}
]

Possible outcomes include

[
(4,0),
]

[
(3,1),
]

[
(2,2),
]

[
(1,3),
]

or more complicated degenerate structures.

The physical Lorentzian case is

[
\boxed{
\operatorname{Inertia}(g^\Phi)=(1,3)
}
]

up to overall sign convention.

Nothing in the expression

[
T\chi T^T
]

by itself selects this.

That is the first major result.

⸻

III. SYLVESTER’S LAW OF INERTIA

Suppose (T) is square and invertible.

Then

[
g=T\chi T^T
]

is a congruence transformation of (\chi).

By Sylvester’s law of inertia, the numbers of positive and negative eigenvalues are invariant under such a transformation.

Therefore

[
\boxed{
\operatorname{sign}(g)

\operatorname{sign}(\chi).
}
]

Consequently:

If

[
\chi>0,
]

then

[
g>0.
]

No choice of (T) can turn it into Lorentzian signature.

This gives a rigorous no-go statement.

⸻

IV. NAIVE SUSCEPTIBILITY NO-GO THEOREM

Theorem

Let

[
g^\Phi=T\chi_\Phi T^T
]

with (T) nonsingular and (\chi_\Phi) real, symmetric, and positive definite.

Then

[
g^\Phi
]

is positive definite and therefore cannot possess Lorentzian signature.

Proof

For any nonzero vector (v),

[
v^Tg^\Phi v

v^TT\chi_\Phi T^Tv.
]

Define

[
u=T^Tv.
]

Since (T) is nonsingular,

[
u\neq0.
]

Because (\chi_\Phi) is positive definite,

[
u^T\chi_\Phi u>0.
]

Therefore

[
v^Tg^\Phi v>0.
]

Hence (g^\Phi) is positive definite.

[
\boxed{\square}
]

This is a foundational constraint on UPT.

A positive susceptibility cannot be converted into Lorentzian spacetime merely by changing coordinates or embeddings.

⸻

V. SIGNATURE MUST COME FROM PHASE STRUCTURE

The previous result forces a conceptual revision.

The question cannot be:

How does (T) turn susceptibility into a Lorentzian metric?

Instead:

What intrinsic property of phase dynamics makes the relevant geometric bilinear form indefinite with exactly one distinguished negative direction?

The desired hierarchy becomes

[
\boxed{
\text{phase dynamics}
\rightarrow
\text{signature}
\rightarrow
\text{causal cone}
\rightarrow
\text{metric}.
}
]

This is substantially more restrictive.

⸻

VI. STABILITY IS NOT SIGNATURE

The intuitive proposal

[
\text{one unstable direction}
+
\text{three stable directions}
]

requires careful interpretation.

A static Hessian

[
H_\Phi

\frac{\delta^2S_\Phi}{\delta\Phi^2}
]

with one negative eigenvalue generally indicates an instability of the configuration.

That is not automatically physical time.

A system sitting at a saddle point with one negative Hessian eigenvalue is unstable.

Therefore:

[
\boxed{
\text{one negative Hessian eigenvalue}
\neq
\text{one time dimension}.
}
]

This distinction is essential.

A viable mechanism must distinguish:

1. negative potential curvature,
2. negative kinetic signature,
3. hyperbolic propagation,
4. causal orientation.

Only the latter three are relevant to spacetime signature.

⸻

VII. KINETIC SIGNATURE

Consider a generic effective phase action:

[
S_\Phi

\int d^nx
\left[
\frac12K_{ab}^{\mu\nu}
\partial_\mu\Phi^a
\partial_\nu\Phi^b

V(\Phi)
\right].
]

The tensor

[
K_{ab}^{\mu\nu}
]

controls propagation.

A Lorentzian effective structure requires an appropriate indefinite contraction among the emergent directions.

The crucial object is therefore not simply

[
H_{ab}

\frac{\partial^2V}{\partial\Phi^a\partial\Phi^b},
]

but the principal derivative structure

[
K_{ab}^{\mu\nu}.
]

This motivates a stronger UPT principle:

[
\boxed{
\text{metric signature is selected by the phase propagation operator, not by static potential stability alone}.
}
]

⸻

VIII. THE PRINCIPAL SYMBOL

For the linearized equation

[
\mathcal L_\Phi\delta\Phi=0,
]

write the highest-derivative part schematically as

[
A^{\mu\nu}{ab}
\partial\mu\partial_\nu\delta\Phi^b.
]

Its principal symbol is

[
\mathcal P_\Phi(x,k)_{ab}

A^{\mu\nu}{ab}k\mu k_\nu.
]

The characteristic equation is

[
\boxed{
\det\mathcal P_\Phi(x,k)=0.
}
]

This equation determines propagation.

It is therefore the natural starting point for deriving the causal cone.

⸻

IX. THE PHASE PROPAGATION CONE

Define

[
\mathcal C_\Phi(x)
]

as the set of directions along which the principal symbol admits propagating solutions.

The corresponding covector cone satisfies

[
\mathcal P_\Phi(x,k)=0.
]

The tangent-space cone is its dual.

If the cone is a single nondegenerate quadratic cone, there exists a bilinear form

[
g^\Phi_{\mu\nu}
]

such that

[
\boxed{
g_\Phi^{\mu\nu}k_\mu k_\nu=0.
}
]

If its signature is Lorentzian, then:

[
\boxed{
\mathcal C_\Phi

\text{Lorentzian null cone}.
}
]

Thus the causal route is:

[
\boxed{
\mathcal L_\Phi
\rightarrow
\mathcal P_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
[g^\Phi].
}
]

⸻

X. WHY THE CONE IS MORE FUNDAMENTAL THAN THE METRIC

A Lorentzian metric contains more information than causal structure.

The causal cone determines only the conformal class:

[
g_{\mu\nu}
\sim
\Omega^2g_{\mu\nu}.
]

Therefore signature selection should be performed before metric normalization.

UPT naturally separates:

[
\boxed{
\text{cone}
\rightarrow
\text{signature/conformal structure}
}
]

from

[
\boxed{
\text{response/volume}
\rightarrow
\text{metric scale}.
}
]

This is conceptually superior to trying to obtain all metric properties from (\chi_\Phi).

⸻

XI. THE ONE-TIME-DIRECTION HYPOTHESIS

The desired UPT result is:

[
\boxed{
\operatorname{Inertia}(g^\Phi)=(1,3).
}
]

This means there exists one direction with opposite sign to the other three.

In a local orthonormal basis,

[
g^\Phi
\sim
\operatorname{diag}(-1,+1,+1,+1).
]

The corresponding null condition is

[
-(k_0)^2
+
|\mathbf k|^2

]

Hence:

[
|k_0|=|\mathbf k|.
]

This produces a universal light cone.

The signature problem is therefore equivalent to the question:

Can UPT dynamically select a single-cone hyperbolic structure with one temporal and three spatial directions?

⸻

XII. PHASE SPECTRAL INDEX

Introduce the spectral index of the relevant phase propagation form:

[
\operatorname{ind}(\mathcal P_\Phi)

(n_-,n_+),
]

where (n_-) and (n_+) count negative and positive propagation directions after appropriate reduction.

The desired infrared condition is

[
\boxed{
\operatorname{ind}(\mathcal P_\Phi)

(1,3).
}
]

This quantity is more appropriate than the Morse index of a static potential.

The Phase Signature Problem becomes:

[
\boxed{
\text{Does UPT force }
\operatorname{ind}(\mathcal P_\Phi)=(1,3)?
}
]

⸻

XIII. CANDIDATE MECHANISM I — STABILITY-PROPAGATION SPLIT

One possible mechanism separates phase amplitude stability from phase propagation.

Suppose the linearized phase equation takes the form

[
K_\Phi^{AB}\nabla_A\nabla_B\delta\Phi
+
H_\Phi\delta\Phi

]

The potential Hessian

[
H_\Phi
]

may be positive definite, ensuring stability.

Meanwhile,

[
K_\Phi
]

may have Lorentzian signature.

Then:

[
\boxed{
H_\Phi>0
\quad\text{and}\quad
\operatorname{sign}(K_\Phi)=(1,3).
}
]

This is physically preferable to requiring an unstable phase vacuum.

It permits:

* stable amplitudes,
* hyperbolic propagation,
* Lorentzian causal structure.

The phrase “one unstable direction” should therefore be replaced by the more precise concept:

one dynamically distinguished hyperbolic direction.

⸻

XIV. CANDIDATE MECHANISM II — PHASE-SPACE SYMPLECTIC ORIENTATION

A symplectic structure

[
\Omega_\Phi
]

distinguishes canonical phase-space directions.

If a preferred polarization or complex structure

[
J_\Phi
]

exists satisfying

[
J_\Phi^2=-I,
]

one may construct a bilinear form

[
G_\Phi(u,v)

\Omega_\Phi(u,J_\Phi v).
]

In ordinary geometric settings this can produce a positive-definite metric.

But alternative compatibility structures may generate indefinite bilinear forms.

A future UPT construction could therefore investigate whether a special phase-space structure naturally yields

[
(1,3)
]

rather than Euclidean signature.

No such mechanism is currently derived.

⸻

XV. CANDIDATE MECHANISM III — CAUSAL ORIENTATION

Suppose the phase network possesses an intrinsic orientation

[
x\prec_\Phi y.
]

The order defines a distinction between future and past.

If the continuum limit possesses a nondegenerate cone, the orientation may select one branch of the cone as future-directed.

Then:

[
\boxed{
\text{phase order}
\rightarrow
\text{cone orientation}.
}
]

However, orientation alone does not determine signature.

An acyclic Euclidean graph still has an order.

Therefore:

[
\text{causal orientation}
\neq
\text{Lorentzian signature}.
]

Both must be derived.

⸻

XVI. CANDIDATE MECHANISM IV — COMPETITION BETWEEN PHASE MODES

Suppose the phase field contains modes

[
\Phi

\sum_a\phi_a e_a.
]

Their effective propagation forms may be

[
K_a^{\mu\nu}.
]

A collective phase transition could suppress all but a universal mode combination

[
K_{\rm eff}^{\mu\nu}

\sum_a w_aK_a^{\mu\nu}.
]

The signature could then be selected dynamically.

One would seek an attractor:

[
K_{\rm eff}
\rightarrow
K_\star
]

with

[
\operatorname{sign}(K_\star)=(1,3).
]

This would make Lorentzian signature an infrared universality class.

⸻

XVII. CANDIDATE MECHANISM V — SIGNATURE AS AN ORDER PARAMETER

Define

[
\Sigma_\Phi

(n_-,n_+).
]

Then signature itself becomes a phase order parameter.

Possible phases include:

[
(4,0),
]

[
(3,1),
]

[
(2,2),
]

[
(1,3).
]

A phase transition could select:

[
(4,0)
\rightarrow
(1,3).
]

This would be a genuine metric signature phase transition.

The universe would begin in a pre-geometric phase and enter a Lorentzian phase.

⸻

XVIII. SIGNATURE GEOMETROGENESIS

The combined hypothesis becomes:

[
\boxed{
\text{phase ordering}
\rightarrow
\text{causal structure}
\rightarrow
\text{signature selection}
\rightarrow
\text{geometry}.
}
]

This is stronger than ordinary geometrogenesis.

Geometry is not merely condensing.

Its causal character is being selected.

⸻

XIX. WHY EUCLIDEAN SIGNATURE IS A SERIOUS COMPETITOR

A Euclidean phase geometry

[
(+,+,+,+)
]

is mathematically natural.

Many positive-definite response functions produce it automatically.

Therefore UPT cannot treat Euclidean signature as an irrelevant alternative.

It must explain why it is not the physical infrared phase.

A successful mechanism must produce:

[
\boxed{
\text{Lorentzian attractor}
}
]

rather than merely permit it.

⸻

XX. THE ((2,2)) COMPETITOR

Split signature

[
(-,-,+,+)
]

is also mathematically viable.

It possesses null directions and hyperbolic-like structures but does not reproduce ordinary (3+1)-dimensional causality.

Therefore:

[
\operatorname{ind}=(2,2)
]

must be dynamically excluded.

A generic indefinite form does not solve the problem.

UPT needs exactly one negative direction.

⸻

XXI. HIGHER-SIGNATURE COMPETITORS

Likewise:

[
(1,n)
]

for (n\neq3)

must be considered.

If the number of emergent directions is not already fixed, signature selection and dimensional selection become coupled.

The complete requirement becomes:

[
\boxed{
(n_-,n_+)

(1,3).
}
]

Thus the signature problem cannot be completely separated from the four-dimensionality problem.

⸻

XXII. THE SINGLE-CONE REQUIREMENT

Even

[
\operatorname{sign}(K)=(1,3)
]

may not be sufficient.

Multiple phase sectors may generate:

[
\mathcal C_1,
\mathcal C_2,
\ldots.
]

The physical infrared theory should ideally have

[
\boxed{
\mathcal C_1

\mathcal C_2

\cdots

\mathcal C_\star.
}
]

Otherwise different particles experience different notions of causality.

Therefore the stronger condition is:

[
\boxed{
\text{unique Lorentzian cone}.
}
]

⸻

XXIII. CONE STABILITY

Suppose the effective propagation tensor is

[
K_\Phi(\lambda).
]

As the phase configuration changes,

[
K_\Phi
\rightarrow
K_\Phi+\delta K.
]

The signature must remain invariant within the physical phase basin.

Thus there should exist an open neighborhood

[
\mathcal U_\Phi
]

such that

[
\operatorname{sign}(K_\Phi+\delta K)

(1,3)
]

for all

[
\delta K\in\mathcal U_\Phi.
]

This is signature stability.

A signature that changes under arbitrarily small perturbations is not a robust physical phase.

⸻

XXIV. SIGNATURE PROTECTION

A strong UPT theory should ideally identify a mechanism protecting the signature.

Candidates include:

* topological protection,
* spectral-gap protection,
* RG fixed-point attraction,
* phase stability,
* symmetry,
* causal-order constraints.

If the signature is topologically protected, then changing it would require crossing a degeneracy:

[
\det K_\Phi=0.
]

This suggests an interesting possibility:

[
\boxed{
\text{Lorentzian signature may be a topological phase of the propagation operator}.
}
]

This is an important avenue for investigation.

⸻

XXV. SIGNATURE TRANSITIONS REQUIRE DEGENERACY

For a continuous family of nondegenerate symmetric matrices

[
K(\lambda),
]

the signature cannot change continuously without an eigenvalue crossing zero.

Thus:

[
\boxed{
\Delta\operatorname{sign}K\neq0
\Rightarrow
\det K(\lambda_c)=0
}
]

at some transition point.

This gives a direct numerical and analytical diagnostic.

A signature-changing phase transition must pass through a degenerate propagation structure.

That is a rigorous structural constraint.

⸻

XXVI. THE PHASE SIGNATURE ORDER PARAMETER

Define

[
\Sigma_\Phi

\left(
n_-(K_\Phi),
n_+(K_\Phi),
n_0(K_\Phi)
\right).
]

For physical UPT spacetime:

[
\boxed{
\Sigma_\Phi=(1,3,0).
}
]

The degenerate transition phase satisfies

[
n_0>0.
]

This creates a precise classification of phase geometries.

⸻

XXVII. SIGNATURE AS AN RG ATTRACTOR

Let the effective propagation tensor flow according to

[
\frac{dK}{d\ln b}

\beta_K(K,\lambda).
]

A Lorentzian fixed point satisfies

[
\beta_K(K_\star)=0
]

with

[
\operatorname{sign}(K_\star)=(1,3).
]

More strongly, the fixed point must be attractive:

[
\delta K(b)
\rightarrow0.
]

Then Lorentzian spacetime would be an infrared universality class.

This would be one of the strongest possible derivations.

⸻

XXVIII. WHAT MUST NOT BE DONE

UPT must not set

[
K_\Phi

\eta_{\mu\nu}
]

by hand.

That simply assumes the answer.

Likewise, one must not write an action such as

[
S_\Phi

\int d^4x
\left[
-\frac12(\partial_t\Phi)^2
+
\frac12|\nabla\Phi|^2
-\cdots
\right]
]

and then claim Lorentzian signature was derived.

The signs have already been inserted.

The valid program is:

[
\boxed{
\text{phase dynamics}
\rightarrow
K_\Phi
\rightarrow
\operatorname{sign}K_\Phi.
}
]

⸻

XXIX. THE TIME-INSERTION TEST

There is a particularly dangerous circularity.

Suppose one writes

[
\partial_t^2\Phi.
]

The symbol (t) already assumes a temporal coordinate.

If time is supposed to emerge, this is potentially circular.

Therefore the signature experiment should preferably begin with the primitive UPT structure:

[
\Phi,
\qquad
\mathcal N_\Phi,
\qquad
\mathcal L_\Phi,
]

and derive the hyperbolic direction from relational phase dynamics.

A continuum (t) may only appear after the causal structure has been reconstructed.

⸻

XXX. DISCRETE VERSION

On the discrete phase web, one may define an update operator

[
\mathcal U_\Phi.
]

The challenge is to determine whether its spectrum contains a continuum limit with hyperbolic propagation.

A possible discrete dispersion relation is

[
\mathcal D_\Phi(\omega,\mathbf k)=0.
]

But (\omega) itself should be interpreted as an emergent spectral variable rather than assumed physical time.

The key question is whether, in the long-wavelength limit,

[
\mathcal D_\Phi
\rightarrow
\omega^2-c^2|\mathbf k|^2.
]

If so, a Lorentzian cone emerges:

[
\boxed{
\omega^2-c^2|\mathbf k|^2=0.
}
]

This is a highly concrete numerical target.

⸻

XXXI. DISPERSION AS A SIGNATURE TEST

Suppose the low-energy dispersion relation has the form

[
\omega^2

c^2|\mathbf k|^2
+
m^2.
]

The massless characteristic surface is

[
\omega^2-c^2|\mathbf k|^2=0.
]

This corresponds to one distinguished spectral direction and three spatial directions.

By contrast:

Euclidean behavior

[
\omega^2+c^2|\mathbf k|^2=0
]

does not yield real propagating waves in the same way.

Multi-time behavior

A dispersion such as

[
\omega_1^2+\omega_2^2

k_x^2-k_y^2=0
]

contains two temporal-type directions and leads to very different causal behavior.

Thus dispersion provides an operational signature diagnostic.

⸻

XXXII. PHASE STABILITY VERSUS GHOSTS

An indefinite kinetic form can introduce negative-energy modes.

This is dangerous.

A Lorentzian spacetime metric itself is indefinite, but not every indefinite field kinetic matrix is physically acceptable.

UPT must therefore distinguish:

[
\boxed{
\text{geometric Lorentzian signature}
}
]

from

[
\boxed{
\text{ghost instability}.
}
]

A viable phase construction must ensure that the negative direction corresponds to causal temporal structure rather than an independently propagating negative-energy ghost.

⸻

XXXIII. THE NO-GHOST CONDITION

Suppose the quadratic phase action is

[
S^{(2)}

\frac12
\int
\delta\Phi^A
\mathcal L_{AB}
\delta\Phi^B.
]

After constraint reduction, the physical Hamiltonian must be bounded appropriately.

The theory should satisfy:

[
\boxed{
\text{one Lorentzian spacetime direction}
\not\Rightarrow
\text{negative-energy physical mode}.
}
]

This requires a proper constraint analysis.

The signature of spacetime and the signature of the physical phase kinetic matrix are related but not identical.

⸻

XXXIV. GAUGE REDUNDANCY

Gauge modes may artificially change the apparent signature of the unreduced operator.

Therefore the signature must be evaluated on the physical quotient space:

[
\mathcal H_{\rm phys}

\frac{\mathcal H_\Phi}{\mathcal G_\Phi}.
]

The relevant propagation form is

[
K_\Phi^{\rm phys}.
]

The requirement becomes

[
\boxed{
\operatorname{sign}
K_\Phi^{\rm phys}

(1,3).
}
]

This prevents gauge artifacts from being mistaken for physical dimensions.

⸻

XXXV. CONSTRAINTS AND DEGENERACY

The phase operator may be degenerate because of constraints.

Then

[
\det K_\Phi=0
]

does not necessarily signal failure.

One must separate:

* gauge zero modes,
* constraint zero modes,
* genuine strong-coupling degeneracy,
* signature-transition degeneracy.

Only after reduction can the physical signature be assessed.

⸻

XXXVI. PHASE SIGNATURE THEOREM

We can now formulate a conditional theorem.

Theorem

Suppose the UPT linearized dynamics admit a physical reduced principal symbol

[
\mathcal P_\Phi^{\rm phys}(x,k)
]

whose characteristic set is:

1. nondegenerate,
2. quadratic in (k),
3. single-sheeted up to future/past orientation,
4. invariant under a local symmetry group acting transitively on the cone,
5. stable under small perturbations,
6. shared by all low-energy physical sectors.

If its tangent-space dual cone has exactly one connected temporal direction and three spatial directions, then there exists a conformal Lorentzian metric

[
[g^\Phi_{\mu\nu}]
]

with signature

[
(-,+,+,+)
]

whose null cone coincides with the phase propagation cone.

Significance

This theorem does not derive the hypotheses.

It establishes the precise mathematical bridge:

[
\boxed{
\text{single stable hyperbolic phase cone}
\Rightarrow
\text{Lorentzian conformal geometry}.
}
]

The remaining UPT problem is therefore to derive those hypotheses.

⸻

XXXVII. THE STRONGER UPT SIGNATURE THEOREM

A genuine UPT result would require proving:

[
\boxed{
\Phi\text{ stable}
\Rightarrow
\operatorname{ind}
(\mathcal P_\Phi^{\rm phys})

(1,3).
}
]

This is the actual target.

If successful, metric signature becomes a structural prediction.

⸻

XXXVIII. SIGNATURE SELECTION FROM PHASE STABILITY

The user’s proposed mechanism can now be sharpened.

Instead of

[
\text{one unstable}
+
\text{three stable},
]

the mathematically safer statement is:

[
\boxed{
\text{stable phase vacuum}
\rightarrow
\text{one hyperbolic causal direction}
+
\text{three elliptic spatial directions}.
}
]

In local coordinates this corresponds to a principal operator of schematic form

[
\mathcal L_\Phi
\sim
-\partial_\tau^2
+
\nabla^2
+
\mathcal M_\Phi.
]

The signs are not assumed; they must emerge from the microscopic phase dynamics.

⸻

XXXIX. PHASE STABILITY AS A SPECTRAL SELECTION RULE

Suppose several stationary phase branches exist:

[
\Phi_1,\Phi_2,\ldots,\Phi_n.
]

Each produces

[
K_i.
]

Define a stability functional

[
\mathcal S_i.
]

If only the branch satisfying

[
\operatorname{sign}(K_i)=(1,3)
]

is dynamically stable, then signature is selected.

The key condition is:

[
\boxed{
\mathcal S_i
\text{ must independently determine stability}.
}
]

One may not define stability to favor Lorentzian signature.

⸻

XL. SIGNATURE SELECTION WITHOUT FINE-TUNING

A true derivation requires an open basin:

[
\mathcal B_\Phi
]

such that generic initial conditions within the basin flow toward the Lorentzian phase.

The desired structure is:

[
\Phi_{\rm initial}
\in\mathcal B_\Phi
\Rightarrow
K_\Phi
\rightarrow
K_\star,
]

with

[
\operatorname{sign}(K_\star)=(1,3).
]

If Lorentzian signature occurs only for a measure-zero parameter set, it is not a robust prediction.

⸻

XLI. THE ROLE OF (c)

Once

[
g^{\mu\nu}\Phi k\mu k_\nu=0
]

takes the form

[
-\omega^2+c_\Phi^2|\mathbf k|^2=0,
]

the causal speed is

[
c_\Phi.
]

If all sectors share the same cone, then

[
c_\Phi=c.
]

Thus signature selection and invariant light speed become linked:

[
\boxed{
\text{Lorentzian cone}
\rightarrow
\text{universal causal speed}.
}
]

The numerical value of (c) may still require units/normalization.

⸻

XLII. DIMENSIONAL SELECTION

Signature alone does not determine dimension.

A theory could produce

[
(1,n)
]

for many values of (n).

Therefore the strongest target is:

[
\boxed{
(1,3)
}
]

not merely

[
(1,n).
]

This connects directly with the unresolved UPT dimension-selection problem.

A successful mechanism may therefore solve two problems simultaneously:

[
\boxed{
\text{signature selection}
+
\text{dimension selection}.
}
]

⸻

XLIII. POSSIBLE FOUR-DIMENSIONAL SELECTION MECHANISMS

Candidate mechanisms include:

Spectral stability

Only (1+3) has a stable propagating phase sector.

Topological stability

Only three spatial dimensions support the required phase-defect topology.

RG universality

Only (1+3) is an attractive infrared fixed point.

Network criticality

Only a particular connectivity exponent produces

[
d_{\rm eff}=4.
]

Mode-counting constraint

The phase representation may permit exactly three mutually compatible spatial modes.

None is currently established.

⸻

XLIV. PHASE SIGNATURE AND TOPOLOGY

A particularly interesting possibility is that phase topology constrains the number of spatial dimensions.

Stable localized structures depend strongly on dimensionality.

If the existence of the relevant phase defects requires

[
d=3
]

spatial dimensions, and causal propagation supplies one temporal direction, then

[
(1,3)
]

could emerge jointly.

This is highly speculative but mathematically testable.

⸻

XLV. PHASE SIGNATURE AND PARTICLES

Particle stability could provide an indirect selector.

Suppose stable localized phase defects exist only in a particular signature.

Then:

[
\boxed{
\text{particle stability}
\rightarrow
\text{signature selection}.
}
]

This would create a striking feedback:

[
\text{phase topology}
\rightarrow
\text{particles}
\rightarrow
\text{geometry}.
]

However, the logic must be derived rather than tuned to reproduce the Standard Model.

⸻

XLVI. PHASE SIGNATURE AND QUANTIZATION

Quantization also depends on causal structure.

If the phase operator becomes hyperbolic only in the Lorentzian phase, then the existence of a well-defined propagator may select that phase.

One could investigate:

[
\text{quantizable phase sector}
\iff
\text{Lorentzian causal phase}.
]

If a Euclidean phase lacks the required physical state space while the Lorentzian phase supports it, this could provide a dynamical selection principle.

This remains open.

⸻

XLVII. PHASE SIGNATURE AND THERMODYNAMICS

Suppose only the Lorentzian phase permits a consistent entropy-producing causal evolution:

[
\frac{dS_\Phi}{d\tau_\Phi}\ge0.
]

Then thermodynamic consistency could select the signature.

But again:

[
\text{thermodynamic arrow}
\neq
\text{Lorentzian signature}
]

unless the relationship is explicitly derived.

⸻

XLVIII. SIGNATURE AS A UNIVERSALITY CLASS

The most attractive long-term picture is:

[
\boxed{
\text{many microscopic phase networks}
\rightarrow
\text{same Lorentzian infrared phase}.
}
]

Then the observed signature would not depend on microscopic details.

It would be universal.

This would explain why radically different microscopic realizations could nevertheless produce the same macroscopic spacetime.

⸻

XLIX. NUMERICAL EXPERIMENT

The first computational test should use the smallest nontrivial UPT phase network.

For each stable configuration (\Phi_\star):

1. construct the linearized operator;
2. remove gauge/constraint zero modes;
3. compute the reduced principal symbol;
4. determine its characteristic surface;
5. reconstruct the effective propagation cone;
6. measure its signature;
7. perturb the configuration;
8. coarse-grain;
9. repeat.

The critical output is:

[
\boxed{
\Sigma_\Phi

(n_-,n_+,n_0).
}
]

⸻

L. NUMERICAL SIGNATURE TEST

For each scale (\ell), measure

[
\Sigma_\Phi(\ell).
]

A successful result might show:

[
(4,0,0)
\rightarrow
(2,2,0)
\rightarrow
(1,3,0).
]

That would indicate a sequence of geometric phase transitions.

Alternatively:

[
(1,3,0)
\rightarrow
(1,3,0)
]

across all scales would indicate signature stability.

A failure could show:

[
(1,3,0)
\rightarrow
(2,2,0),
]

indicating that Lorentzian signature is not an infrared attractor.

⸻

LI. DISPERSION-RELATION EXPERIMENT

For long-wavelength modes calculate

[
\omega(\mathbf k).
]

Fit the leading relation:

[
\omega^2

A|\mathbf k|^2
+
B|\mathbf k|^4
+\cdots.
]

A Lorentzian infrared limit requires

[
A>0
]

and

[
\omega\rightarrow c|\mathbf k|
]

for massless modes.

The coefficient

[
c^2=A
]

then becomes the emergent propagation speed.

The higher-order terms quantify microscopic departures from Lorentz invariance.

⸻

LII. CONE-COLLAPSE TEST

A genuine Lorentzian cone should remain nondegenerate.

Monitor

[
\det K_\Phi.
]

The desired infrared condition is

[
\det K_\Phi\neq0.
]

A transition between signatures requires

[
\det K_\Phi=0.
]

This provides a direct numerical indicator of signature-changing phase transitions.

⸻

LIII. OBSERVER-INDEPENDENCE TEST

Construct the cone in multiple coordinate representations.

If

[
K_\Phi
\rightarrow
J^TK_\Phi J,
]

its inertia must remain unchanged.

This provides a direct implementation of observer-independent signature.

The numerical test is:

[
\operatorname{sign}(K_\Phi’)

\operatorname{sign}(K_\Phi).
]

Failure indicates that the apparent signature is coordinate-dependent and therefore not physical.

⸻

LIV. COARSE-GRAINING TEST

Let

[
\mathcal R_b
]

be the network coarse-graining map.

Require

[
\Sigma_\Phi^{(b)}
\rightarrow
(1,3,0)
]

at large scales.

The strongest result would be:

[
\boxed{
\Sigma_\Phi^{(b)}

(1,3,0)
\quad
\forall b>b_c.
}
]

This would demonstrate an infrared Lorentzian phase.

⸻

LV. MULTI-SECTOR TEST

For each physical phase sector (a), determine

[
K_a.
]

Measure:

[
\Sigma_a
]

and

[
\mathcal C_a.
]

The desired result is:

[
\boxed{
\Sigma_a=(1,3,0),
\qquad
\mathcal C_a=\mathcal C_\star.
}
]

If different sectors have different cones, the theory does not recover universal relativity.

⸻

LVI. FALSIFICATION CRITERIA

The signature program should be regarded as unsuccessful if:

1. the susceptibility construction remains positive definite;
2. Lorentzian signature must be inserted manually;
3. the physical phase operator has no hyperbolic sector;
4. multiple time directions are generic;
5. Euclidean signature is equally stable;
6. Lorentzian signature requires fine tuning;
7. signature varies uncontrollably under coarse-graining;
8. different physical sectors possess incompatible cones;
9. Lorentzian behavior exists only because primitive time was inserted;
10. the negative direction corresponds to a physical ghost;
11. (1+3) dimensions are not dynamically preferred.

Any one of these would identify a specific failure mode.

⸻

LVII. CLAIM LEDGER

Statement	Status
(T\chi T^T) preserves inertia under nonsingular congruence	Established mathematics
Positive-definite (\chi) cannot produce Lorentzian (g)	Derived theorem
Static instability is not equivalent to time direction	Established conceptual constraint
Principal symbols determine characteristics	Established mathematics
A nondegenerate quadratic Lorentzian cone defines conformal Lorentzian geometry	Established conditional mathematics
UPT currently selects Lorentzian signature	Not established
UPT currently selects one temporal direction	Open
UPT currently selects three spatial directions	Open
Phase stability can select signature	Conditional hypothesis
Signature can behave as a phase order parameter	Conditional hypothesis
Lorentzian signature could be an RG attractor	Conditional hypothesis
Signature transition requires degeneracy	Established mathematical result
Universal (c) follows if a universal Lorentzian cone emerges	Conditional
Einstein gravity follows from signature selection	Open

⸻

LVIII. THE CENTRAL UPT SIGNATURE POSTULATE

A possible future postulate is:

Phase Signature Selection Principle: The stable infrared phase of the universal phase dynamics possesses a unique nondegenerate hyperbolic propagation cone with exactly one temporal direction and three spatial directions.

Symbolically:

[
\boxed{
\Phi_{\rm IR}^{\rm stable}
\Rightarrow
\operatorname{ind}(\mathcal P_\Phi^{\rm phys})=(1,3).
}
]

But under the Phase-II discipline, this should not yet be promoted to a foundational postulate.

It is currently a target for derivation.

⸻

LIX. WHAT WOULD MAKE IT A PREDICTION?

The strongest possible UPT result would show:

[
{\text{existing UPT postulates}}
\Rightarrow
(1,3)
]

without:

* assuming a time coordinate,
* inserting a Minkowski metric,
* fixing the signs by hand,
* selecting parameters for the desired outcome,
* imposing four dimensions externally.

Then:

[
\boxed{
(-,+,+,+)
}
]

would become an actual UPT prediction.

That would be enormously more significant than merely demonstrating that UPT can accommodate Lorentzian spacetime.

⸻

LX. THE HIERARCHY OF SUCCESS

There are several levels of success.

Level 0 — Compatibility

UPT permits Lorentzian geometry.

Level 1 — Construction

A particular UPT model generates Lorentzian signature.

Level 2 — Stability

Lorentzian signature is dynamically stable.

Level 3 — Universality

Different microscopic realizations flow toward the same Lorentzian signature.

Level 4 — Structural derivation

Existing UPT postulates force

[
(1,3).
]

Level 5 — Quantitative prediction

The same derivation also fixes:

[
c,\quad d=4,
]

and the low-energy dispersion corrections.

Only Levels 4–5 constitute strong foundational predictions.

⸻

LXI. THE DEEPER SYNTHESIS

The preceding Phase Causality program proposed:

[
\Phi
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi.
]

The present work adds:

[
\mathcal C_\Phi
\rightarrow
\operatorname{sign}(g^\Phi).
]

Therefore:

[
\boxed{
\Phi
\rightarrow
\text{phase influence}
\rightarrow
\text{causal order}
\rightarrow
\text{causal cone}
\rightarrow
\text{signature}.
}
]

The next step is:

[
\text{signature}
+
\text{response}
+
\text{volume}
\rightarrow
g^\Phi.
]

Thus the full UPT spacetime emergence program becomes:

[
\boxed{
\Phi
\rightarrow
\mathcal N_\Phi
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
[g^\Phi]
\rightarrow
g^\Phi
\rightarrow
\text{spacetime}.
}
]

⸻

LXII. THE MOST IMPORTANT CONCEPTUAL REFINEMENT

The original intuition

[
\boxed{
\text{phase stability}
\rightarrow
\text{one unstable}
+
\text{three stable}
}
]

is therefore modified.

The mathematically safer formulation is:

[
\boxed{
\text{phase stability}
\rightarrow
\text{stable hyperbolic propagation structure}
\rightarrow
(1,3).
}
]

This avoids confusing an unstable potential direction with the temporal direction of spacetime.

The temporal direction is not necessarily an instability.

It is a direction in the causal propagation structure.

⸻

LXIII. A POSSIBLE MASTER PRINCIPLE

The deepest candidate formulation is:

The physical metric signature is the stable inertia class of the universal phase propagation operator in the infrared.

Formally,

[
\boxed{
\operatorname{Signature}(g^\Phi)

\operatorname{Inertia}
\left(
\mathcal P_\Phi^{\rm phys}
\right)_{\rm IR}.
}
]

Then:

[
\boxed{
\operatorname{Inertia}
\left(
\mathcal P_\Phi^{\rm phys}
\right)_{\rm IR}

(1,3)
}
]

would constitute the desired derivation.

This is a concrete mathematical target.

⸻

LXIV. FINAL CONCLUSION

Metric signature is not a secondary detail of emergent geometry.

It is one of the deepest pieces of information that must be explained if spacetime is not fundamental.

The naive UPT construction

[
g^\Phi=T\chi_\Phi T^T
]

cannot by itself select Lorentzian signature.

If (\chi_\Phi) is positive definite, the resulting metric is necessarily positive definite.

Therefore the origin of Lorentzian signature must lie deeper in the phase dynamics.

The natural candidate is the phase propagation operator:

[
\mathcal L_\Phi
\rightarrow
\mathcal P_\Phi
\rightarrow
\mathcal C_\Phi.
]

If the infrared phase dynamics possess a unique stable nondegenerate hyperbolic cone with exactly one temporal and three spatial directions, then:

[
\boxed{
\mathcal C_\Phi
\rightarrow
[g^\Phi_{\mu\nu}]
}
]

and

[
\boxed{
\operatorname{sign}(g^\Phi)

(-,+,+,+).
}
]

The decisive UPT question is therefore:

[
\boxed{
\textbf{Does phase organization dynamically force a }(1,3)\textbf{ propagation signature?}
}
]

Not:

[
\text{Can we construct a Lorentzian metric?}
]

But:

[
\boxed{
\text{Why is every stable macroscopic phase configuration driven toward }(1,3)\text{?}
}
]

A successful answer would simultaneously illuminate:

[
\text{causality},
]

[
\text{time},
]

[
\text{invariant }c,
]

[
\text{Lorentz symmetry},
]

[
\text{four-dimensionality},
]

and

[
\text{emergent spacetime}.
]

The desired foundational chain would then be:

[
\boxed{
\Phi
\rightarrow
\text{phase influence}
\rightarrow
\text{causal order}
\rightarrow
\text{hyperbolic propagation}
\rightarrow
(1,3)\text{ signature}
\rightarrow
\text{Lorentzian geometry}
\rightarrow
\text{spacetime}.
}
]

At present, UPT has not established this chain.

What has been established is something more precise and useful: the signature problem can now be stated as a sharply defined spectral-dynamical gate, and the naive susceptibility route has a rigorous no-go result.

That is exactly where Phase II should begin.

The next decisive investigation is therefore:

[
\boxed{
\textbf{“Universal Phase Origin of the Light Cone:
Derivation of Hyperbolicity, Invariant }c\textbf{, and Lorentz Symmetry.”}
}
]

If the signature program succeeds, that paper becomes the bridge from Phase Causality to actual Lorentzian spacetime.

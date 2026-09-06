UNIVERSAL PHASE THEORY

UNIVERSAL PHASE DERIVATION OF PHASE CAUSALITY

From Phase Influence to Causal Order, Temporal Structure, and Emergent Spacetime

A Foundational Phase-II Investigation

⸻

Abstract

Universal Phase Theory (UPT) takes phase organization as more fundamental than spacetime, matter, or conventional field ontology. The theory therefore faces a foundational question that precedes the derivation of an emergent metric:

Can causality itself be derived from phase structure?

The present work develops a formal program in which causal order is not initially imposed as an independent physical principle, but is defined through the capacity of one phase configuration to influence another. Given a phase configuration (\Phi) on an underlying relational substrate, we define a phase-causal relation

[
x\prec_\Phi y
]

whenever an admissible perturbation localized near (x) can produce a physically distinguishable response near (y) through the intrinsic phase dynamics.

The central proposed hierarchy is

[
\boxed{
\text{phase influence}
\longrightarrow
\text{causal order}
\longrightarrow
\text{causal cone}
\longrightarrow
\text{metric structure}
\longrightarrow
\text{spacetime}.
}
]

This construction transforms the update directed acyclic graph (\mathcal X) from a potentially arbitrary computational substrate into a candidate physical manifestation of phase influence.

Five mathematical requirements are investigated:

1. transitivity,
2. local finiteness,
3. antisymmetry,
4. observer independence,
5. compatibility with coarse graining.

The analysis distinguishes sharply between properties inherited from a stipulated DAG and properties genuinely derived from phase dynamics. Transitivity and local finiteness are not sufficient merely because they hold for an update DAG. They become physically meaningful only if the same properties emerge from the phase-response relation itself.

A central result is a conditional Phase Causality Theorem: if the linearized UPT dynamics possess a well-defined finite-domain influence kernel, if influence composes under propagation, if no closed influence cycles exist, and if coarse-graining preserves the support structure of the response kernel, then the induced relation is a locally finite partial order and can serve as a candidate causal order.

The paper then develops a route from causal order to Lorentzian geometry using characteristic propagation rather than assuming a metric from the beginning. The principal symbol of the phase stability operator defines candidate phase characteristics,

[
\mathcal P_\Phi(x,k)=0,
]

whose dual structure may generate a phase causal cone

[
\mathcal C_\Phi(x).
]

A Lorentzian metric is recovered only under an additional nontrivial condition: the characteristic cone must be sufficiently quadratic and nondegenerate that it defines a conformal Lorentzian structure. Thus

[
\prec_\Phi\not\Rightarrow g_{\mu\nu}
]

in general. The stronger result requires

[
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
[g^\Phi_{\mu\nu}],
]

with the metric scale determined separately.

The paper also introduces phase clocks, phase horizons, causal phase transitions, dimension flow, and geometrogenesis as consequences that become mathematically meaningful if the causal program succeeds.

No unconditional claim is made that UPT currently derives physical spacetime. The investigation instead identifies precise gates separating conceptual compatibility from structural derivation.

The resulting foundational target is:

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
g^\Phi_{\mu\nu}
\rightarrow
\text{spacetime physics}.
}
]

The ultimate question is therefore not whether UPT can be placed on a causal graph, but whether causality itself is an emergent property of organized phase influence.

⸻

I. FOUNDATIONAL MOTIVATION

Conventional physical reasoning usually begins with spacetime.

One specifies a manifold

[
M
]

equipped with a metric

[
g_{\mu\nu},
]

and from the metric derives:

* temporal separation,
* spatial separation,
* light cones,
* causal relations,
* geodesics,
* curvature,
* gravitational dynamics.

Schematically,

[
\boxed{
\text{geometry}
\rightarrow
\text{causality}
\rightarrow
\text{dynamics}.
}
]

Universal Phase Theory reverses the proposed ontology.

The fundamental object is the phase configuration

[
\Phi.
]

The substrate on which phase organization occurs is represented abstractly by

[
\mathcal X.
]

At microscopic scales, (\mathcal X) need not be a manifold and need not possess a primitive metric.

The corresponding UPT hierarchy is therefore intended to be

[
\boxed{
\Phi
\rightarrow
\mathcal N_\Phi
\rightarrow
\text{causal organization}
\rightarrow
\text{geometry}.
}
]

The crucial conceptual step is to recognize that the update DAG need not itself be fundamental.

It may be merely an encoding of something deeper:

[
\boxed{
\mathcal X
\approx
\text{representation of phase influence}.
}
]

The purpose of this paper is to determine whether that statement can be made mathematically meaningful.

⸻

II. THE CENTRAL QUESTION

The fundamental question is:

[
\boxed{
\text{Can phase dynamics generate causal order without primitive spacetime?}
}
]

More explicitly:

Given two elementary phase configurations or events (x,y\in\mathcal X), can one determine whether

[
x\prec_\Phi y
]

solely from the phase dynamics?

We define the intended meaning as follows:

[
x\prec_\Phi y
]

if and only if a physically admissible perturbation introduced at (x) can produce a physically distinguishable phase response at (y).

This definition is intentionally operational.

It does not initially refer to:

* clocks,
* coordinate time,
* spacetime distance,
* a Lorentzian metric,
* gravitational fields.

Causality is instead identified with directed influence.

⸻

III. UPT ONTOLOGY

The foundational UPT hierarchy begins with a universal phase field

[
\Phi:\mathcal X\rightarrow\mathcal M_\Phi,
]

where (\mathcal M_\Phi) is the phase configuration space.

The universal phase dynamics are represented schematically by

[
\mathscr F[\Phi;\lambda]=0.
]

If a variational formulation exists,

[
\mathscr F[\Phi;\lambda]

\frac{\delta S_\Phi}{\delta\Phi}.
]

Perturbations around a solution

[
\Phi_0
]

are written

[
\Phi=\Phi_0+\delta\Phi.
]

To first order,

[
\mathcal L_\Phi\delta\Phi=0,
]

where

[
\boxed{
\mathcal L_\Phi

\left.
\frac{\delta\mathscr F}{\delta\Phi}
\right|_{\Phi_0}
}
]

is the phase stability operator.

Whenever its inverse exists in an appropriate sense,

[
\chi_\Phi=\mathcal L_\Phi^{-1}
]

defines the linear phase susceptibility.

The present paper introduces a second object:

[
\boxed{
\mathfrak I_\Phi(x,y)
}
]

representing the existence and strength of causal influence from (x) to (y).

The fundamental proposal is that

[
\mathfrak I_\Phi(x,y)
]

should be derived from (\mathcal L_\Phi), not independently stipulated.

⸻

IV. PHASE INFLUENCE

Consider a localized perturbation

[
\delta\Phi_x
]

supported near (x).

The resulting response is formally

[
\delta\Phi(y)

\chi_\Phi(y,x),\delta\Phi_x.
]

This suggests the preliminary definition

[
\mathfrak I_\Phi(x,y)\neq0
]

whenever

[
\chi_\Phi(y,x)
]

contains a physically admissible response channel.

However, an important distinction must be made.

A nonzero susceptibility does not automatically imply causal influence.

A static Green function can be nonzero outside a causal propagation cone.

Therefore the relevant object is not simply

[
\chi_\Phi(x,y),
]

but the retarded influence kernel.

Denote it by

[
G_\Phi^{\rm R}(x,y).
]

Then define

[
x\prec_\Phi y
]

only when

[
\boxed{
G_\Phi^{\rm R}(y,x)\neq0
}
]

for at least one admissible perturbation channel.

This distinction is fundamental.

⸻

V. THE PHASE-CAUSAL RELATION

Let

[
\mathcal A_x
]

be the space of admissible perturbations localized at (x).

Let

[
\mathcal O_y
]

be the space of physically distinguishable observables near (y).

Define the response map

[
\mathscr R_{yx}:
\mathcal A_x
\rightarrow
\mathcal O_y.
]

Then:

[
\boxed{
x\prec_\Phi y
\iff
\mathscr R_{yx}\neq0.
}
]

This definition is more fundamental than a coordinate statement.

No time coordinate is required.

No metric is required.

No distance is required.

The relation is determined entirely by whether phase influence can propagate.

⸻

VI. DIRECT AND TRANSITIVE CAUSALITY

A microscopic phase network may contain direct influence relations

[
x\rightarrow y.
]

But physical causality should generally include indirect influence.

If

[
x\rightarrow y
]

and

[
y\rightarrow z,
]

then a perturbation at (x) can influence (z) through (y).

Therefore the physically meaningful relation is the transitive closure:

[
x\prec_\Phi z.
]

Define the direct influence graph

[
E_\Phi
]

and its transitive closure

[
E_\Phi^+.
]

Then

[
\boxed{
\prec_\Phi = E_\Phi^+.
}
]

This provides the first connection between phase dynamics and the update DAG.

The DAG is no longer fundamental merely because it was chosen to be acyclic.

Rather, it should arise as the graph representation of the phase influence relation.

⸻

VII. THE TRANSITIVITY GATE

A causal relation must satisfy

[
x\prec_\Phi y,\quad
y\prec_\Phi z
]

implies

[
x\prec_\Phi z.
]

This is the transitivity condition.

In a well-composed deterministic dynamical system, influence composition suggests

[
\mathscr R_{zx}
\sim
\mathscr R_{zy}\circ
\mathscr R_{yx}.
]

If both maps contain nontrivial admissible channels, then a composite channel exists.

Thus transitivity can emerge from composability of phase propagation.

Conditional Phase Transitivity Theorem

Suppose:

1. phase perturbations propagate through composable local response maps;
2. admissible perturbation spaces are closed under composition;
3. propagation does not erase every composite channel;
4. the physical influence relation is defined by existence of a nonzero composite response.

Then

[
x\prec_\Phi y
\land
y\prec_\Phi z
\Rightarrow
x\prec_\Phi z.
]

This is a genuine structural route to transitivity.

It is not yet a proof that the full UPT theory satisfies the hypotheses.

⸻

VIII. ANTISYMMETRY

A causal order must not contain a closed causal cycle.

Suppose

[
x\prec_\Phi y
]

and simultaneously

[
y\prec_\Phi x.
]

Then phase influence forms a closed loop.

For distinct (x\neq y), this violates antisymmetry.

Therefore we require

[
\boxed{
x\prec_\Phi y
\land
y\prec_\Phi x
\Rightarrow
x=y.
}
]

The physical question is:

What prevents phase influence from forming closed causal loops?

There are several possibilities.

Possibility A: Primitive DAG structure

The update substrate is stipulated to be acyclic.

This guarantees antisymmetry, but does not derive it.

Possibility B: Phase stability

A closed influence loop could generate a self-reinforcing instability.

If stable phase configurations prohibit such loops, antisymmetry becomes a dynamical consequence.

Possibility C: Dissipative orientation

An irreversible phase-order parameter might orient influence globally.

Possibility D: No-go result

UPT may permit closed phase-influence cycles.

If so, causal order cannot be globally defined without an additional postulate.

This is a major Phase-II gate.

⸻

IX. LOCAL FINITENESS

For a causal-set-like structure, one requires that the causal interval

[
I(x,y)

{z:x\prec_\Phi z\prec_\Phi y}
]

contain finitely many elementary events for finite causal separation.

Thus:

[
\boxed{
|I(x,y)|<\infty.
}
]

Local finiteness cannot simply be inherited from the implementation DAG.

The stronger requirement is:

[
\boxed{
\text{phase influence itself is locally finite}.
}
]

This may arise if:

* phase excitations have finite propagation bandwidth,
* the microscopic phase substrate is discrete,
* the response operator has finite-range support,
* or the phase dynamics admit a finite propagation speed.

⸻

X. FINITE PROPAGATION SPEED

A local differential operator can possess a finite domain of dependence.

For a hyperbolic equation,

[
\mathcal L_\Phi\delta\Phi=0,
]

the solution at (y) depends only on initial data inside a characteristic domain.

This is precisely the mathematical structure required for causal propagation.

The deepest possibility is therefore:

[
\boxed{
\text{hyperbolicity of phase dynamics}
\rightarrow
\text{finite influence speed}.
}
]

If the maximal phase propagation velocity is

[
c_\Phi,
]

then the emergent invariant speed of relativistic physics could potentially be identified with

[
\boxed{
c=c_\Phi.
}
]

But this is conditional.

A finite propagation velocity is not enough to prove that (c_\Phi) is universal, observer-independent, or Lorentz invariant.

⸻

XI. THE PHASE CHARACTERISTIC STRUCTURE

Consider the principal symbol of the phase operator.

For a continuum operator,

[
\mathcal L_\Phi

A^{\mu\nu}{ab}
\partial\mu\partial_\nu
+
B^\mu_{ab}\partial_\mu
+
C_{ab}
+\cdots.
]

The principal symbol is

[
\mathcal P_{\Phi,ab}(x,k)

A^{\mu\nu}{ab}(x)k\mu k_\nu.
]

Characteristic propagation occurs when

[
\boxed{
\det\mathcal P_\Phi(x,k)=0.
}
]

This equation defines the phase characteristic set.

Its dual in tangent space defines candidate propagation directions.

Thus:

[
\boxed{
\mathcal L_\Phi
\rightarrow
\mathcal P_\Phi
\rightarrow
\mathcal C_\Phi.
}
]

This is a potentially decisive bridge between phase dynamics and spacetime causality.

⸻

XII. THE PHASE CAUSAL CONE

At each coarse-grained point (x), define

[
\mathcal C_\Phi(x)
]

as the set of tangent directions along which phase disturbances can propagate.

The causal relation should then be expressible geometrically as:

[
x\prec_\Phi y
]

if there exists a future-directed phase-propagating curve

[
\gamma:[0,1]\rightarrow\mathcal X
]

such that

[
\dot\gamma(s)\in\mathcal C_\Phi(\gamma(s)).
]

Then

[
\boxed{
\prec_\Phi
\leftrightarrow
\mathcal C_\Phi.
}
]

This is conceptually important.

The metric no longer defines causality.

The causal cone does.

The metric may subsequently be reconstructed from the cone.

⸻

XIII. CAUSALITY BEFORE METRIC

In ordinary general relativity,

[
g_{\mu\nu}
]

determines the light cone.

UPT proposes the reverse possibility:

[
\boxed{
\mathcal C_\Phi
\rightarrow
[g^\Phi_{\mu\nu}].
}
]

The square brackets emphasize that a causal cone determines a metric only up to conformal transformation.

If

[
g_{\mu\nu}
]

is compatible with the cone, then so is

[
\tilde g_{\mu\nu}

\Omega^2(x)g_{\mu\nu}.
]

Therefore phase causality can at most determine the conformal metric initially.

The scale factor

[
\Omega(x)
]

requires an additional physical structure.

This gives a natural two-stage emergence:

[
\boxed{
\text{phase causality}
\rightarrow
\text{conformal geometry}
}
]

followed by

[
\boxed{
\text{phase response}
\rightarrow
\text{metric scale}.
}
]

⸻

XIV. LORENTZIAN SIGNATURE

A major UPT gate is the emergence of Lorentzian signature.

A causal cone alone does not guarantee

[
(-,+,+,+).
]

The phase dynamics must produce a cone with the appropriate topology.

For four dimensions, one seeks a quadratic characteristic form

[
g^{\mu\nu}\Phi k\mu k_\nu=0
]

with signature

[
(-,+,+,+).
]

If this occurs, the phase system naturally defines a Lorentzian conformal structure.

But there is no justification for assuming this outcome.

Possible alternatives include:

[
(+,+,+,+),
]

multi-cone structures,

higher-order dispersion surfaces,

or anisotropic/Finsler-like causal geometries.

Therefore:

[
\boxed{
\text{Lorentzian signature is a derived gate, not a premise.}
}
]

⸻

XV. THE SINGLE-CONE CONDITION

Suppose the phase system contains multiple sectors:

[
\delta\Phi

\sum_a\delta\Phi_a.
]

Each sector may possess its own characteristic polynomial

[
\mathcal P_a(x,k)=0.
]

Then one might obtain

[
\mathcal C_1,\mathcal C_2,\ldots,\mathcal C_n.
]

If different sectors propagate with different cones, there may be no unique spacetime causal structure.

Thus UPT should test:

[
\boxed{
\mathcal C_1

\mathcal C_2

\cdots

\mathcal C_n
}
]

in the low-energy limit.

A universal cone would provide a natural origin for the universality of relativistic causal structure.

Failure would instead predict sector-dependent propagation and potential violations of the equivalence principle.

⸻

XVI. OBSERVER INDEPENDENCE

A causal relation cannot depend on an arbitrary observer’s coordinate description.

Suppose two observers use phase coordinates

[
X^\mu
]

and

[
X’^\mu.
]

The relation should satisfy

[
x\prec_\Phi y
\iff
x’\prec_\Phi y’.
]

This is stronger than coordinate covariance.

It requires that causal influence itself be an invariant property of the phase configuration.

The desired principle is therefore:

[
\boxed{
\text{causal influence is observer-independent}.
}
]

If this follows from intrinsic properties of (\Phi), then coordinate time becomes secondary.

⸻

XVII. PHASE TIME

Once causal order exists, temporal ordering can potentially be defined without primitive time.

Suppose

[
x\prec_\Phi y.
]

Then (y) lies in the future phase domain of (x).

A phase clock can be represented by a monotonic scalar

[
\tau_\Phi:\mathcal X\rightarrow\mathbb R
]

satisfying

[
x\prec_\Phi y
\Rightarrow
\tau_\Phi(x)<\tau_\Phi(y).
]

Such a function is a time function.

The central question becomes:

Does UPT possess a naturally generated time function?

If yes,

[
\boxed{
\text{phase order}
\rightarrow
\text{phase time}.
}
]

This would resolve an important conceptual problem created by the rejection of primitive time.

⸻

XVIII. PROPER TIME AS PHASE ACCUMULATION

A stronger possibility is that proper time measures accumulated phase evolution.

Introduce a phase clock functional

[
d\tau_\Phi

\mathcal Q_\Phi(d\Phi,d\Phi),
]

where (\mathcal Q_\Phi) is determined by the intrinsic phase structure.

Then the proper time of a phase trajectory becomes

[
\tau_\Phi[\gamma]

\int_\gamma d\tau_\Phi.
]

The standard relativistic interval would emerge if

[
d\tau_\Phi^2

-\frac{1}{c^2}
g^\Phi_{\mu\nu}
dx^\mu dx^\nu.
]

This is a possible endpoint, not an established UPT result.

⸻

XIX. PHASE CAUSALITY AND THE UPDATE DAG

The update DAG should now be reinterpreted.

Previously:

[
\mathcal X

\text{allowed update structure}.
]

Under the Phase Causality hypothesis:

[
\boxed{
\mathcal X_\Phi

\text{transitive reduction or representation of phase influence}.
}
]

This changes the ontology substantially.

The DAG is no longer arbitrary computational scaffolding.

Instead:

[
\Phi
\rightarrow
\mathfrak I_\Phi
\rightarrow
\mathcal X_\Phi.
]

The fundamental object becomes the influence relation.

The DAG is its discrete representation.

⸻

XX. PHASE-WEB FORMULATION

Define the phase web as

[
\boxed{
\mathcal N_\Phi

(V,E_\Phi,W_\Phi,\mathcal H_\Phi,\Phi)
}
]

where:

* (V) is the set of phase events,
* (E_\Phi) is the directed influence relation,
* (W_\Phi) contains influence weights,
* (\mathcal H_\Phi) contains phase holonomies or internal relational data,
* (\Phi) assigns phase states.

The central hierarchy becomes

[
\boxed{
\Phi
\rightarrow
E_\Phi
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
g^\Phi.
}
]

This is the proposed Phase-Web causal architecture.

⸻

XXI. INFLUENCE WEIGHTS

The binary relation

[
x\prec_\Phi y
]

contains only existence information.

A richer theory assigns a magnitude

[
W_\Phi(x,y).
]

Possible definitions include

[
W_\Phi(x,y)

|\mathscr R_{yx}|,
]

or a spectral quantity derived from the phase propagator.

Then

[
W_\Phi(x,y)>0
]

indicates influence strength.

The causal relation remains binary:

[
x\prec_\Phi y
\iff
W_\Phi(x,y)\neq0,
]

while the magnitude controls effective response.

This separates:

[
\boxed{
\text{causal structure}
}
]

from

[
\boxed{
\text{metric/response structure}.
}
]

⸻

XXII. FROM CAUSAL ORDER TO DISTANCE

Causal order alone does not generally determine metric distance.

However, causal order plus an appropriate volume measure can reconstruct spacetime geometry under suitable assumptions.

UPT therefore requires a volume-like phase measure

[
\mu_\Phi.
]

The emergent geometric data would then be

[
\boxed{
(\prec_\Phi,\mu_\Phi)
\rightarrow
g^\Phi_{\mu\nu}.
}
]

The phase network supplies both:

1. order,
2. effective volume.

The metric then emerges from their combination.

⸻

XXIII. PHASE VOLUME

A microscopic phase volume may be defined by counting elementary phase states:

[
V_\Phi(R)

#{x\in R}.
]

At large scales, one seeks

[
V_\Phi(R)
\sim
\int_R d^dx\sqrt{|g^\Phi|}.
]

This produces a correspondence:

[
\boxed{
\text{phase-event density}
\rightarrow
\sqrt{|g^\Phi|}.
}
]

Again, the proportionality constant and continuum scaling must be derived.

⸻

XXIV. CAUSAL DISTANCE

A discrete causal structure provides several candidate notions of distance.

For example, define the longest-chain distance

[
D_{\rm chain}(x,y)

\max_{\gamma:x\prec_\Phi y}
|\gamma|.
]

Alternatively, use graph diffusion:

[
K_\Phi(s)

e^{-s\Delta_\Phi^{\rm graph}}.
]

A diffusion distance can be defined by

[
D_{\rm diff}^2(x,y;s)

\sum_z
|K_\Phi(s;x,z)-K_\Phi(s;y,z)|^2.
]

The crucial requirement is that, in an appropriate continuum limit,

[
D_{\rm chain},D_{\rm diff}
]

must converge to quantities compatible with the same (g^\Phi_{\mu\nu}).

⸻

XXV. PHASE DIMENSION

The effective dimension of the causal web can be measured through spectral properties.

For a graph Laplacian,

[
\Delta_{\mathcal N},
]

define the return probability

[
P(s)

\frac{1}{|V|}
\operatorname{Tr}
e^{-s\Delta_{\mathcal N}}.
]

The spectral dimension is

[
\boxed{
d_s(s)

-2
\frac{d\ln P(s)}
{d\ln s}.
}
]

If

[
d_s(s)\rightarrow4
]

at macroscopic scales, the phase web possesses four-dimensional effective diffusion geometry.

But:

[
d_s=4
]

alone does not establish a four-dimensional Lorentzian spacetime.

It is a diagnostic, not a derivation.

⸻

XXVI. COARSE-GRAINING COMPATIBILITY

A physical causal structure must survive coarse-graining.

Let

[
\mathcal R_b
]

be a coarse-graining transformation.

Then

[
\mathcal N_\Phi
\rightarrow
\mathcal N_\Phi^{(b)}.
]

The corresponding causal relation becomes

[
\prec_\Phi^{(b)}.
]

The central requirement is:

[
\boxed{
x\prec_\Phi y
\Rightarrow
\mathcal R_b(x)
\prec_\Phi^{(b)}
\mathcal R_b(y)
}
]

whenever the separation remains resolved at scale (b).

This is causal coarse-graining covariance.

⸻

XXVII. NO SPURIOUS MACROSCOPIC CAUSALITY

Coarse-graining can create effective connections that were absent microscopically.

Therefore the reverse implication must be treated carefully.

One seeks an approximate relation:

[
\mathcal R_b(x)\prec_\Phi^{(b)}\mathcal R_b(y)
]

only if there exists an actual microscopic influence channel connecting the corresponding regions, or if the new connection is a controlled effective approximation.

Otherwise coarse-graining generates artificial causal structure.

This provides a powerful numerical falsification test.

⸻

XXVIII. SCALE-DEPENDENT CAUSALITY

UPT may naturally produce scale-dependent causal structure.

Define

[
\mathcal C_\Phi(x;\ell)
]

at coarse-graining scale (\ell).

Then investigate

[
\mathcal C_\Phi(x;\ell)
\rightarrow
\mathcal C_\Phi^{\rm IR}(x)
]

as

[
\ell\rightarrow\infty.
]

Three possibilities exist.

Fixed causal structure

[
\mathcal C_\Phi(\ell)\rightarrow\mathcal C.
]

This is compatible with conventional spacetime.

Running causal structure

[
\mathcal C_\Phi(\ell_1)\neq
\mathcal C_\Phi(\ell_2).
]

This predicts scale-dependent causal propagation.

Causal phase transition

At some scale,

[
\mathcal C_\Phi
]

changes topology or signature.

This would constitute a causal phase transition.

⸻

XXIX. PHASE CAUSAL PHASE TRANSITIONS

Suppose a control parameter (\lambda) causes the phase response structure to undergo a bifurcation.

Then:

[
\lambda<\lambda_c
\quad\Rightarrow\quad
\mathcal C_\Phi^{(1)}
]

while

[
\lambda>\lambda_c
\quad\Rightarrow\quad
\mathcal C_\Phi^{(2)}.
]

The universe could therefore transition between different causal regimes.

A particularly radical possibility is

[
\boxed{
\text{pre-geometric phase}
\rightarrow
\text{Lorentzian causal phase}.
}
]

This is causal geometrogenesis.

⸻

XXX. GEOMETROGENESIS

The proposed full emergence chain becomes

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

The stages have distinct meanings.

Stage 1 — Phase

[
\Phi
]

is primitive.

Stage 2 — Organization

Phase relations produce

[
\mathcal N_\Phi.
]

Stage 3 — Influence

Phase perturbations establish

[
\prec_\Phi.
]

Stage 4 — Causality

The influence relation defines

[
\mathcal C_\Phi.
]

Stage 5 — Conformal geometry

The cone determines

[
[g^\Phi].
]

Stage 6 — Metric scale

Phase susceptibility or volume determines

[
g^\Phi.
]

Stage 7 — Spacetime

The resulting structure becomes the effective spacetime experienced by low-energy excitations.

⸻

XXXI. PHASE CAUSALITY THEOREM

We may now formulate a central conditional result.

Theorem — Phase Causality

Let (\Phi) be a stable UPT phase configuration with linearized operator (\mathcal L_\Phi). Suppose:

1. a retarded response kernel (G_\Phi^{\rm R}) exists;
2. its support defines finite-domain propagation;
3. admissible influence channels compose;
4. no nontrivial closed influence cycles exist;
5. the response relation is invariant under admissible observer transformations;
6. coarse-graining preserves macroscopic influence support;
7. the continuum limit exists.

Then the relation

[
x\prec_\Phi y
\iff
G_\Phi^{\rm R}(y,x)\neq0
]

defines a causal partial order on the resolved phase events.

If, in addition, the continuum characteristic structure is a nondegenerate single Lorentzian cone, then (\prec_\Phi) determines an emergent conformal Lorentzian geometry.

Proof structure

Conditions 3 and finite propagation provide transitive composition.

Condition 4 provides antisymmetry.

Condition 2 provides local finiteness at the microscopic level.

Condition 5 provides observer independence.

Condition 6 preserves the relation under scale transformation.

Condition 7 permits continuum reconstruction.

The single-cone Lorentzian condition then establishes the conformal metric structure.

The theorem is conditional because UPT has not yet derived all seven hypotheses from its existing postulates.

⸻

XXXII. WHAT THIS THEOREM DOES NOT CLAIM

The theorem does not establish that UPT already produces spacetime.

It establishes something more useful:

If the phase dynamics satisfy a precise set of structural conditions, then causal order and Lorentzian conformal geometry follow.

This converts a philosophical proposition into a finite mathematical research program.

The remaining task is to determine whether those conditions follow from UPT itself.

⸻

XXXIII. PHASE CAUSALITY VERSUS STIPULATED DAG CAUSALITY

This distinction is essential.

A DAG automatically possesses:

[
\text{acyclicity}
]

and therefore a partial order.

But if UPT begins with a DAG and simply calls it causal, then nothing has been derived.

That would amount to:

[
\mathcal X
\equiv
\text{causal order by definition}.
]

The stronger program is:

[
\boxed{
\Phi
\rightarrow
\text{influence}
\rightarrow
\mathcal X_\Phi.
}
]

Only then does the DAG acquire physical significance.

⸻

XXXIV. THE CIRCULARITY TEST

UPT must avoid the following circular construction:

[
\text{assume time}
\rightarrow
\text{define dynamics}
\rightarrow
\text{derive causality}.
]

Likewise, it must avoid:

[
\text{assume metric}
\rightarrow
\text{define light cone}
\rightarrow
\text{call it phase causality}.
]

The clean route is:

[
\boxed{
\Phi
\rightarrow
\mathcal L_\Phi
\rightarrow
G_\Phi^{\rm R}
\rightarrow
\prec_\Phi.
}
]

Only after this should geometry enter.

⸻

XXXV. PHASE CAUSALITY AND SUSCEPTIBILITY

UPT already contains

[
\chi_\Phi=\mathcal L_\Phi^{-1}.
]

This creates an important connection.

The same operator can potentially provide:

[
\boxed{
\mathcal L_\Phi
\rightarrow
\begin{cases}
\chi_\Phi & \text{response}\
\mathcal P_\Phi & \text{causal propagation}
\end{cases}
}
]

Thus the susceptibility and causal structure may have a common origin.

At the appropriate level:

[
\boxed{
\text{phase stability operator}
\rightarrow
{\text{response},\text{causality}}.
}
]

This is potentially one of the deepest unifying structures in UPT.

⸻

XXXVI. FROM SUSCEPTIBILITY TO METRIC

The existing UPT metric ansatz is

[
g_{ij}^{\Phi}

T_{ia}\chi_\Phi^{ab}T_{jb}.
]

The causal analysis suggests a refinement.

The metric should not be identified with susceptibility alone.

Instead:

[
\boxed{
g^\Phi

\mathcal G
\left(
\mathcal C_\Phi,
\chi_\Phi,
\mu_\Phi
\right),
}
]

where:

* (\mathcal C_\Phi) determines causal structure,
* (\chi_\Phi) determines response/scale,
* (\mu_\Phi) determines volume normalization.

This avoids forcing an intrinsically Euclidean susceptibility tensor to become Lorentzian.

⸻

XXXVII. THE SIGNATURE PROBLEM REVISITED

A positive susceptibility often resembles a positive-definite quadratic form.

A Lorentzian metric is indefinite.

Therefore the naive relation

[
g=T\chi T^T
]

cannot automatically provide Lorentzian signature.

A more promising construction is to separate causal and response bilinear forms:

[
g^\Phi

\Omega^2_\Phi,\hat g^\Phi,
]

where

[
\hat g^\Phi
]

is reconstructed from the phase causal cone and

[
\Omega_\Phi
]

is determined by response/volume information.

This suggests:

[
\boxed{
\text{causality determines signature and conformal class;}
}
]

[
\boxed{
\text{phase response determines metric scale.}
}
]

This is structurally cleaner.

⸻

XXXVIII. PHASE GEODESICS

Once (g^\Phi) exists, free phase excitations may follow

[
\frac{D^2x^\mu}{d\tau^2}=0.
]

But the deeper formulation is causal:

A freely propagating excitation follows an extremal phase-influence trajectory.

If the emergent metric exists, this becomes a geodesic:

[
\frac{d^2x^\mu}{d\tau^2}
+
\Gamma^\mu_{\alpha\beta}
\frac{dx^\alpha}{d\tau}
\frac{dx^\beta}{d\tau}
=0.
]

Thus gravity need not be introduced as a force.

It may arise because the phase causal structure is curved.

⸻

XXXIX. PHASE GRAVITY

The conceptual hierarchy becomes

[
\boxed{
\text{phase organization}
\rightarrow
\text{causal geometry}
\rightarrow
\text{geodesic motion}.
}
]

If localized phase structures deform

[
\mathcal C_\Phi,
]

then they deform

[
g^\Phi.
]

A second localized structure follows the resulting geometry.

The apparent interaction is therefore geometric.

This provides a rigorous route for investigating the intuition:

[
\boxed{
\text{there is no fundamental gravitational force;
there is emergent geometry.}
}
]

That statement remains a hypothesis until the phase-to-geometry derivation is completed.

⸻

XL. PHASE HORIZONS

A phase horizon can be defined without invoking a pre-existing black-hole metric.

Let

[
\mathcal C_\Phi(x)
]

be the local future influence cone.

A phase horizon is a hypersurface

[
\mathcal H_\Phi
]

across which future-directed phase influence cannot propagate outward.

Symbolically,

[
\boxed{
\mathcal H_\Phi:
\quad
\text{outgoing phase influence}\rightarrow0.
}
]

If the continuum metric exists, this should reduce to the usual null-horizon condition.

Thus horizons could be fundamentally causal rather than gravitational.

⸻

XLI. PHASE CAUSAL ENTROPY

A causal network may possess an enormous number of internal phase configurations consistent with a macroscopic causal boundary.

Define schematically

[
S_\Phi(\mathcal H)

k_B\ln\Omega_\Phi(\mathcal H),
]

where (\Omega_\Phi) counts admissible microscopic phase configurations.

A future objective is to test whether

[
S_\Phi(\mathcal H)
\propto
\mathcal A_{\mathcal H}.
]

If successful, horizon entropy would emerge from phase-web microstructure.

This would connect:

[
\text{causality}
\rightarrow
\text{geometry}
\rightarrow
\text{horizon}
\rightarrow
\text{thermodynamics}.
]

⸻

XLII. PHASE COSMOLOGY

At large scales, suppose the phase web becomes homogeneous and isotropic.

Then the effective metric may approach

[
ds^2

-dt^2
+
a^2(t)\gamma_{ij}dx^idx^j.
]

The scale factor would then represent coarse-grained phase-web expansion rather than expansion of a pre-existing container.

The cosmological hierarchy becomes:

[
\boxed{
\text{phase-network evolution}
\rightarrow
\text{causal structure evolution}
\rightarrow
a(t).
}
]

This offers a new interpretation of cosmic expansion.

⸻

XLIII. CAUSAL GEOMETRIC DARK SECTORS

Suppose phase excitations exist that are weakly coupled to the emergent electromagnetic sector but strongly modify

[
\mathcal C_\Phi
]

or

[
g^\Phi.
]

Then they would be electromagnetically dark but geometrically active.

Such states would constitute a candidate phase-geometric dark sector.

The defining condition would be

[
\mathcal O_{\rm EM}[\delta\Phi]\approx0,
]

while

[
\delta g^\Phi\neq0.
]

This is a candidate phenomenology, not a current prediction.

⸻

XLIV. CAUSAL REFRACTION

If the phase characteristic cone depends on scale,

[
\mathcal C_\Phi(k),
]

then different wavelengths may experience slightly different effective propagation.

This could produce a phase-geometric analogue of refraction.

The corresponding dispersion relation would be

[
\mathcal P_\Phi(k)=0.
]

A viable UPT model must, however, satisfy extremely strong low-energy constraints on Lorentz violation.

Therefore this is an experimentally constrained avenue rather than an assumption.

⸻

XLV. CAUSAL ANISOTROPY

A phase network may possess directional organization.

Then

[
\mathcal C_\Phi(x,\hat n)
]

may depend on orientation.

The effective metric may become anisotropic or even Finsler-like.

Such anisotropy would produce:

* directional propagation,
* polarization-dependent speeds,
* modified lensing,
* preferred-frame signatures.

The absence of such observations becomes a constraint on UPT network structure.

⸻

XLVI. PHASE CAUSAL WAVES

A perturbation of the phase network,

[
\delta\mathcal N_\Phi,
]

may perturb the causal cone:

[
\delta\mathcal C_\Phi.
]

If the emergent metric exists,

[
\delta\mathcal C_\Phi
\rightarrow
\delta g^\Phi_{\mu\nu}.
]

This defines a candidate phase gravitational wave:

[
\boxed{
\delta\mathcal N_\Phi
\rightarrow
\delta g^\Phi.
}
]

The decisive question is whether such modes possess the observed tensorial polarization structure.

That must be derived.

⸻

XLVII. CAUSAL NETWORK DEFECTS

Topological defects in the phase web may alter connectivity.

Examples include:

[
\text{phase strings},
\qquad
\text{phase knots},
\qquad
\text{phase walls},
\qquad
\text{causal dislocations}.
]

Their geometric manifestation could be encoded by

[
\Delta\prec_\Phi\neq0.
]

This provides a new classification:

[
\boxed{
\text{matter-like defect}
\quad\text{vs.}\quad
\text{causal defect}.
}
]

A causal defect is fundamentally a defect in the influence structure.

⸻

XLVIII. WORMHOLE-LIKE PHASE CONNECTIVITY

A phase web might contain nonlocal connectivity that becomes geometrically represented as a shortcut.

Suppose two regions

[
A,\ B
]

are macroscopically distant according to emergent geometry but possess a direct phase-network connection.

Then:

[
A\leftrightarrow B
]

could appear as a wormhole-like geometric structure.

However, this is not automatically a traversable wormhole.

One must establish:

1. continuum geometric reconstruction,
2. global topology,
3. causal consistency,
4. finite propagation,
5. stability,
6. absence of unacceptable closed causal curves.

Therefore:

[
\boxed{
\text{network shortcut}\neq\text{wormhole prediction}.
}
]

⸻

XLIX. CAUSAL SINGULARITY AVOIDANCE

Suppose phase susceptibility saturates:

[
\chi_\Phi
\rightarrow
\chi_{\rm max}.
]

Then geometric quantities derived from it may remain finite.

A possible mechanism is

[
\boxed{
\text{phase saturation}
\rightarrow
\text{bounded geometric response}
\rightarrow
\text{singularity avoidance}.
}
]

But singularity avoidance must be demonstrated using an actual solution of the phase dynamics.

Bounded susceptibility alone is insufficient.

⸻

L. THE EMERGENCE OF THE SPEED OF LIGHT

The phase causal program offers a new route toward (c).

If the low-energy phase cone is

[
g^{\mu\nu}\Phi k\mu k_\nu=0,
]

then in an appropriate local frame:

[
\omega^2=c_\Phi^2|\mathbf k|^2.
]

If all physical sectors share the same cone,

[
c_\Phi=c,
]

then the invariant speed is a property of the phase web.

Thus:

[
\boxed{
c

\text{maximum universal phase-influence velocity}.
}
]

This would be conceptually stronger than merely inserting (c) into the metric.

⸻

LI. EMERGENCE OF LORENTZ SYMMETRY

The next requirement is symmetry.

The low-energy characteristic equation must become invariant under a group isomorphic to

[
SO(1,3)
]

or its appropriate covering group.

Thus:

[
\boxed{
\text{phase causal cone}
\rightarrow
\text{Lorentz symmetry}.
}
]

Lorentz symmetry would then be an infrared symmetry of the phase network.

Microscopic violations could exist provided they are irrelevant under coarse-graining.

This naturally connects Phase Causality with the Phase RG program.

⸻

LII. CAUSAL RG FLOW

Let

[
\mathcal R_b
]

coarse-grain the phase network.

The causal structure flows:

[
\mathcal C_\Phi
\rightarrow
\mathcal C_\Phi^{(b)}.
]

A Lorentzian fixed point would satisfy

[
\mathcal R_b(\mathcal C_\Phi)
\rightarrow
\mathcal C_\star
]

with

[
\mathcal C_\star
]

Lorentz invariant.

The profound possibility is:

[
\boxed{
\text{Lorentz symmetry is an infrared fixed point of phase causality}.
}
]

This would turn Lorentz invariance from a primitive symmetry into an emergent universality class.

⸻

LIII. CAUSAL UNIVERSALITY CLASSES

Different microscopic phase networks may flow to the same macroscopic causal structure.

Define a causal universality class

[
[\mathcal N_\Phi]_{\rm causal}
]

by equivalence under coarse-graining:

[
\mathcal N_1
\sim_{\rm causal}
\mathcal N_2
]

if both flow to the same infrared cone and causal geometry.

Then conventional spacetime could be universal despite radically different microscopic phase substrates.

This would provide a powerful explanation for why low-energy physics appears smooth.

⸻

LIV. THE PHASE CAUSALITY HIERARCHY

The complete hierarchy is:

[
\boxed{
\Phi
}
]

[
\downarrow
]

[
\boxed{
\mathcal L_\Phi
}
]

[
\downarrow
]

[
\boxed{
G_\Phi^{\rm R}
}
]

[
\downarrow
]

[
\boxed{
\prec_\Phi
}
]

[
\downarrow
]

[
\boxed{
\mathcal C_\Phi
}
]

[
\downarrow
]

[
\boxed{
[g^\Phi]
}
]

[
\downarrow
]

[
\boxed{
g^\Phi
}
]

[
\downarrow
]

[
\boxed{
\text{spacetime}.
}
]

This is the proposed foundational architecture of Phase Causality.

⸻

LV. REQUIRED MATHEMATICAL GATES

The theory should now be tested through explicit gates.

Gate A — Retarded response

Does

[
G_\Phi^{\rm R}
]

exist without primitive time?

Status: OPEN.

⸻

Gate B — Finite propagation

Does the phase operator possess finite-domain influence?

Status: OPEN.

⸻

Gate C — Transitivity

Does phase influence compose?

[
x\prec_\Phi y,\ y\prec_\Phi z
\Rightarrow
x\prec_\Phi z.
]

Status: CONDITIONAL.

⸻

Gate D — Antisymmetry

Are closed phase-influence cycles forbidden dynamically?

Status: OPEN.

⸻

Gate E — Local finiteness

Does microscopic phase influence remain locally finite?

Status: CONDITIONAL on substrate/dynamics.

⸻

Gate F — Observer independence

Is phase influence invariant under admissible observer transformations?

Status: OPEN.

⸻

Gate G — Coarse-graining covariance

Does causal structure survive renormalization?

Status: OPEN.

⸻

Gate H — Unique causal cone

Do physical sectors share one low-energy cone?

Status: OPEN.

⸻

Gate I — Lorentzian signature

Does the cone define a Lorentzian conformal structure?

Status: OPEN.

⸻

Gate J — Four-dimensionality

Does the infrared causal structure select

[
d=4?
]

Status: OPEN.

⸻

Gate K — Metric scale

Can phase response determine the conformal factor?

Status: OPEN.

⸻

Gate L — Einstein limit

Does the resulting geometry reproduce general relativity?

Status: OPEN.

⸻

LVI. WHAT IS ACTUALLY DERIVED?

At the current stage, the strict epistemic classification is:

Established mathematics

The following are mathematically well-defined concepts:

[
\mathcal L_\Phi,
\qquad
G_\Phi^{\rm R},
\qquad
\mathcal P_\Phi,
\qquad
\prec_\Phi,
\qquad
\mathcal C_\Phi.
]

Conditional structural result

If phase influence satisfies finite propagation, composability, and acyclicity, then a causal partial order follows.

Conceptual compatibility

UPT is compatible with:

[
\text{phase influence}
\rightarrow
\text{causal order}.
]

Not yet derived

UPT has not yet established:

[
\prec_\Phi
\rightarrow
\text{Lorentzian spacetime}.
]

Nor has it established:

[
c,\quad d=4,\quad
G,\quad
\text{Einstein equations}.
]

These remain research gates.

⸻

LVII. THE MOST IMPORTANT NEGATIVE RESULT TO AVOID

There is a tempting but invalid argument:

[
\mathcal X\text{ is a DAG}
]

therefore

[
\mathcal X\text{ is causal}.
]

This is insufficient.

A DAG has mathematical order, but physical causality requires an influence interpretation.

The correct logical structure is:

[
\boxed{
\text{phase influence}
\Rightarrow
\text{DAG}
}
]

not

[
\boxed{
\text{DAG}
\Rightarrow
\text{phase influence}.
}
]

This distinction must remain explicit throughout UPT.

⸻

LVIII. EXPERIMENTAL PROGRAM

The theory can be tested at several levels.

Tier I — Numerical phase propagation

Construct a microscopic UPT phase model.

Inject a localized perturbation.

Measure

[
G_\Phi^{\rm R}(x,y).
]

Determine its support.

⸻

Tier II — Causal-order reconstruction

Construct

[
x\prec_\Phi y
]

from measured influence.

Test:

[
\text{transitivity},
]

[
\text{antisymmetry},
]

[
\text{local finiteness}.
]

⸻

Tier III — Continuum reconstruction

Increase system size while decreasing lattice/network scale.

Measure:

[
d_s,
]

cone structure,

correlation lengths,

and effective volume.

⸻

Tier IV — Lorentzian test

Fit the low-energy characteristic surface to

[
g^{\mu\nu}k_\mu k_\nu=0.
]

Test:

* single cone,
* isotropy,
* Lorentz invariance,
* universal propagation speed.

⸻

Tier V — Metric reconstruction

Determine whether

[
(\prec_\Phi,\mu_\Phi,\chi_\Phi)
]

reconstruct a unique effective metric.

⸻

LIX. FALSIFICATION CRITERIA

The Phase Causality program should be considered unsuccessful if any of the following persist generically:

1. phase response permits unavoidable closed causal loops;
2. influence is intrinsically nonlocal;
3. no observer-independent influence relation exists;
4. coarse-graining destroys causal order;
5. different sectors possess irreconcilable causal cones;
6. the continuum limit fails;
7. the characteristic geometry is not Lorentzian;
8. no universal propagation speed emerges;
9. four-dimensionality requires arbitrary tuning;
10. metric reconstruction requires inserting spacetime by hand.

A clean failure would be scientifically valuable.

⸻

LX. THE STRONGEST POSSIBLE SUCCESS

The strongest outcome would establish the sequence

[
\boxed{
\Phi
\Rightarrow
G_\Phi^{\rm R}
\Rightarrow
\prec_\Phi
\Rightarrow
\mathcal C_\Phi
\Rightarrow
[g^\Phi]
\Rightarrow
g^\Phi
}
]

with no independently stipulated spacetime structure.

Then:

[
\boxed{
\text{causality would be emergent}.
}
]

And spacetime would not merely be emergent from phase organization.

It would be emergent in a more precise sense:

[
\boxed{
\text{spacetime is the macroscopic geometry of phase influence}.
}
]

⸻

LXI. A DEEPER REINTERPRETATION OF THE DAG

If the program succeeds, the update DAG acquires a fundamentally different interpretation.

It would not represent:

“the order in which a computer updates variables.”

It would represent:

the partial order of physically possible phase influence.

Then an elementary event is not fundamentally a spacetime point.

It is an elementary phase event.

A causal edge is not fundamentally a temporal tick.

It is an elementary influence channel.

A path is not fundamentally a worldline.

It is a chain of compatible phase influence.

A continuum worldline would emerge only after coarse-graining.

This is a profound ontological reversal.

⸻

LXII. PHASE EVENTS

The primitive discrete object becomes

[
e_i=(\Phi_i,\mathcal R_i),
]

where (\Phi_i) is the local phase state and (\mathcal R_i) represents admissible response channels.

An event is therefore defined by a phase transition capable of participating in influence.

The causal order is

[
e_i\prec_\Phi e_j.
]

Spacetime points are emergent equivalence classes of sufficiently coherent phase events.

⸻

LXIII. WORLDLINES AS PHASE CHAINS

A particle trajectory could then be represented microscopically as

[
e_1\prec_\Phi e_2\prec_\Phi e_3\prec_\Phi\cdots.
]

The continuum trajectory

[
x^\mu(\tau)
]

is the coarse-grained image of that chain.

Thus:

[
\boxed{
\text{worldline}

\text{coarse-grained phase-causal chain}.
}
]

Particle motion becomes a statement about phase continuity.

⸻

LXIV. LIGHT AS THE NULL PHASE SECTOR

A particularly elegant possibility follows.

If photons are phase excitations propagating exactly on the phase causal boundary, then:

[
\boxed{
\text{photon propagation}

\text{null phase propagation}.
}
]

The observed universal speed of light would then arise because photons follow the boundary of the phase influence cone.

The conventional statement

[
ds^2=0
]

would become emergent rather than fundamental.

⸻

LXV. MASSIVE MOTION

Massive phase structures would occupy the interior of the causal cone.

Their coarse-grained trajectories satisfy

[
ds^2<0
]

for the chosen mostly-plus convention.

The distinction between massive and massless propagation would therefore correspond to:

[
\boxed{
\text{interior phase propagation}
\quad\text{vs.}\quad
\text{boundary phase propagation}.
}
]

This offers a geometric reinterpretation of particle kinematics.

⸻

LXVI. CAUSALITY AND QUANTUM THEORY

The phase-causal program may also clarify an important quantum question.

Quantum amplitudes may involve many possible phase histories, but physical influence should still obey the underlying causal support.

The relevant object could be a phase propagator

[
G_\Phi(x,y)
]

whose support determines possible influence while its complex phase determines interference.

Then:

[
\boxed{
\text{causal support}
+
\text{phase amplitude}

\text{quantum propagation}.
}
]

This potentially separates causality from probability.

The Born rule remains an independent unresolved problem.

⸻

LXVII. MEASUREMENT AND PHASE CAUSALITY

A measurement event (M) should not be defined by primitive temporal collapse.

Instead, it is a phase coupling:

[
\Phi_{\rm system}
\leftrightarrow
\Phi_{\rm detector}.
]

Measurement is possible when a phase-influence channel exists:

[
x\prec_\Phi M.
]

This makes measurement causal without requiring primitive time.

Again, this does not derive quantum probabilities.

⸻

LXVIII. INFORMATION FLOW

The phase causal relation can also be interpreted informationally.

If a perturbation at (x) changes the distinguishable state space at (y), then information has propagated.

Define an influence information measure

[
\mathcal I_\Phi(x\rightarrow y).
]

Then:

[
x\prec_\Phi y
]

if

[
\mathcal I_\Phi(x\rightarrow y)>0.
]

The causal structure is therefore potentially equivalent to the directed support of physically available phase information.

This suggests:

[
\boxed{
\text{phase influence}

\text{physical information flow}.
}
]

This must be formalized without assuming information theory as a primitive ontology.

⸻

LXIX. THE PHASE CAUSAL PRINCIPLE

The proposed foundational principle can now be stated:

[
\boxed{
\textbf{Phase Causal Principle:}
\quad
\text{A causal relation exists exactly where an admissible phase perturbation can propagate.}
}
]

Formally,

[
x\prec_\Phi y
\iff
\exists,\delta\Phi_x
\text{ such that }
\delta\Phi_y\neq0
]

through an admissible retarded phase channel.

This is the central hypothesis of the present paper.

⸻

LXX. STRONG FORM OF THE PRINCIPLE

A stronger version states:

[
\boxed{
\text{All physical causal relations are projections of phase influence.}
}
]

If true, there would be no independent causal sector.

Causality would be an emergent organizational property of the universal phase field.

This would make causality itself part of UPT’s ontology rather than a background assumption.

⸻

LXXI. PHASE CAUSALITY AS A UNIVERSAL CONSTRAINT

If all physical interactions emerge from (\Phi), then all must obey the same underlying phase causal structure.

Thus:

[
\boxed{
\mathcal C_{\rm EM}

\mathcal C_{\rm matter}

\mathcal C_{\rm gravity}

\mathcal C_\Phi
}
]

in the universal low-energy limit.

This could provide a deep explanation for the universality of relativistic causal structure.

It also creates an extremely strong experimental constraint.

Any persistent sector-dependent causal cone would challenge the strongest version of UPT.

⸻

LXXII. PHASE CAUSALITY AND EQUIVALENCE

If every sector experiences the same phase causal cone, then local free-fall universality follows naturally at the causal level.

One obtains the hierarchy:

[
\boxed{
\text{universal phase cone}
\rightarrow
\text{universal null structure}
\rightarrow
\text{equivalence-principle candidate}.
}
]

The metric response must still be derived before the full equivalence principle can be claimed.

⸻

LXXIII. THE CAUSAL-METRIC SPLIT

The analysis suggests that UPT should distinguish three structures:

[
\boxed{
\mathfrak C_\Phi

\text{causal structure}
}
]

[
\boxed{
\mathfrak G_\Phi

\text{metric structure}
}
]

[
\boxed{
\mathfrak R_\Phi

\text{response structure}.
}
]

They need not be identical.

The proposed hierarchy is

[
\mathfrak C_\Phi
\rightarrow
\mathfrak G_\Phi
]

and

[
\mathfrak R_\Phi
\rightarrow
\text{metric scale}.
]

This decomposition may resolve the earlier difficulty of deriving a Lorentzian metric directly from a susceptibility tensor.

⸻

LXXIV. PHASE CAUSAL CURVATURE

Once a causal cone varies from point to point,

[
\partial_\rho\mathcal C_\Phi\neq0,
]

the emergent conformal geometry becomes nontrivial.

After metric reconstruction,

[
R^\rho{}_{\sigma\mu\nu}[g^\Phi]
\neq0.
]

Curvature can therefore be interpreted as:

[
\boxed{
\text{spatial variation of phase influence structure}.
}
]

This offers a direct physical meaning for curvature.

⸻

LXXV. GRAVITY AS CAUSAL INHOMOGENEITY

Under this interpretation, gravitational fields are not fundamentally forces.

They are spatial and temporal variations in the local phase causal structure.

Symbolically:

[
\boxed{
\nabla\mathcal C_\Phi
\neq0
\Rightarrow
\text{effective gravitational geometry}.
}
]

A mass-like phase defect changes the network.

The network changes the causal cone.

The causal cone changes the metric.

The metric changes free trajectories.

This produces apparent gravitational attraction without a fundamental gravitational interaction.

⸻

LXXVI. PHASE-WEB GEOMETRIC RESPONSE

The full response chain can therefore be written:

[
\delta\Phi
\rightarrow
\delta\mathcal N_\Phi
\rightarrow
\delta\prec_\Phi
\rightarrow
\delta\mathcal C_\Phi
\rightarrow
\delta g^\Phi.
]

This provides a more fundamental version of the previously proposed relation

[
\delta g

\delta T,\chi T^T

T\chi(\delta\mathcal L_\Phi)\chi T^T
+\cdots.
]

The causal formulation inserts the missing intermediate structure.

⸻

LXXVII. THE PHASE-WEB RESPONSE EQUATION

A general future formulation might be written schematically as

[
\boxed{
\delta g^\Phi

\mathcal K_C[\delta\prec_\Phi]
+
\mathcal K_R[\delta\chi_\Phi]
+
\mathcal K_V[\delta\mu_\Phi].
}
]

Here:

* (\mathcal K_C) reconstructs conformal geometry from causal changes;
* (\mathcal K_R) determines response scale;
* (\mathcal K_V) determines volume normalization.

This is not yet a derived UPT equation.

It is the proposed mathematical target.

⸻

LXXVIII. THE FOUR FOUNDATIONAL QUESTIONS

The entire Phase Causality program reduces to four questions:

1. Can phase influence be defined?

[
\Phi\rightarrow\mathfrak I_\Phi?
]

2. Does phase influence become causal order?

[
\mathfrak I_\Phi\rightarrow\prec_\Phi?
]

3. Does causal order become Lorentzian geometry?

[
\prec_\Phi\rightarrow\mathcal C_\Phi\rightarrow[g^\Phi]?
]

4. Does the resulting geometry become physical spacetime?

[
[g^\Phi]\rightarrow g^\Phi\rightarrow\text{observables}?
]

These should be treated as separate gates.

⸻

LXXIX. PHASE-II RESEARCH PROTOCOL

The next computational/theoretical study should not begin by fitting a cosmology.

Instead:

Experiment 1

Construct the smallest nontrivial UPT phase model with an explicitly defined retarded response.

Measure:

[
G_\Phi^{\rm R}(x,y).
]

Experiment 2

Construct the influence relation.

Test:

[
\text{transitivity},
]

[
\text{antisymmetry}.
]

Experiment 3

Measure influence range as system size grows.

Test local finiteness and finite propagation.

Experiment 4

Coarse-grain the network.

Test:

[
\prec_\Phi
\rightarrow
\prec_\Phi^{(b)}.
]

Experiment 5

Extract the characteristic polynomial.

Test whether:

[
\det\mathcal P_\Phi(k)=0
]

approaches a single quadratic Lorentzian cone.

Experiment 6

Measure the effective dimension.

Test whether:

[
d_{\rm eff}\rightarrow4.
]

Experiment 7

Attempt metric reconstruction.

Only after these tests should gravitational phenomenology be attempted.

⸻

LXXX. THE MINIMAL PHASE-CAUSAL MODEL

A minimal test model should contain:

[
\Phi_i\in U(1)
]

on a finite relational network.

Let

[
\theta_i
]

be the local phase.

Define an interaction

[
S_\Phi

\sum_{(ij)\in E}
\kappa_{ij}
\left[
1-\cos(\theta_i-\theta_j-A_{ij})
\right].
]

Linearization around a stable configuration gives

[
S_\Phi^{(2)}
\sim
\frac12
\sum_{ij}
\delta\theta_i
L_{ij}
\delta\theta_j.
]

The response operator is

[
L.
]

The crucial next step is to determine whether a genuinely directed propagation operator can be derived without introducing primitive time.

This exposes the central difficulty rather than hiding it.

⸻

LXXXI. THE TIME PROBLEM

A conventional dynamical equation such as

[
\ddot\theta_i
+
\sum_jL_{ij}\theta_j
=0
]

already assumes time.

That would violate the strongest UPT ontology.

Therefore a valid Phase Causality construction must derive temporal orientation from something deeper, such as:

* directed phase updates,
* noncommuting phase transformations,
* causal influence ordering,
* a covariant phase-space structure,
* or another primitive-free construction.

This is one of the hardest remaining problems.

⸻

LXXXII. COVARIANT PHASE SPACE

One possible route is to formulate phase dynamics without a primitive time coordinate.

Let

[
\Sigma
]

be a codimension-one solution surface.

The covariant phase-space construction defines a symplectic current

[
\omega_\Phi
]

and symplectic form

[
\Omega_\Phi

\int_\Sigma\omega_\Phi.
]

If the integral is independent of the choice of (\Sigma), then dynamics can be characterized relationally.

This may provide the mathematical infrastructure needed for a retarded/advanced distinction without choosing a preferred external time.

However, as established in earlier UPT audits, covariant symplecticity is generic mathematics and does not by itself derive a UPT-specific causal orientation.

⸻

LXXXIII. THE ARROW OF TIME

Causal order also requires orientation.

Why is

[
x\prec_\Phi y
]

different from

[
y\prec_\Phi x?
]

One possibility is that phase organization contains a monotonic quantity

[
\mathcal A_\Phi
]

satisfying

[
x\prec_\Phi y
\Rightarrow
\mathcal A_\Phi(x)<\mathcal A_\Phi(y).
]

This would generate a phase arrow of time.

But UPT should not simply identify

[
\mathcal A_\Phi=S_\Phi
]

without derivation.

The origin of temporal orientation remains an independent question.

⸻

LXXXIV. REVERSIBILITY VERSUS CAUSALITY

Microscopic equations may be reversible while causal order remains directed.

This is not necessarily contradictory.

A reversible equation may have retarded and advanced solutions.

The physical causal structure requires a rule selecting the admissible direction.

Thus:

[
\text{dynamical reversibility}
\neq
\text{causal symmetry}.
]

UPT must determine whether the direction of phase influence emerges from boundary conditions, phase stability, coarse-graining, or an intrinsic asymmetry.

⸻

LXXXV. CAUSALITY AND ENTROPY

A possible relationship is

[
\frac{dS_\Phi}{d\tau_\Phi}\ge0.
]

If phase entropy is monotonic along causal chains, then entropy could provide an emergent arrow of time.

But this should not be assumed.

The correct program is to investigate whether

[
\boxed{
x\prec_\Phi y
\Rightarrow
S_\Phi(y)\ge S_\Phi(x)
}
]

follows statistically or structurally.

If not, causality and thermodynamic time remain distinct emergent structures.

⸻

LXXXVI. THE DEEP POSSIBILITY

The strongest UPT interpretation would therefore be:

[
\boxed{
\text{phase order}

\text{causal order}

\text{physical temporal order}.
}
]

Then time would not be an independent dimension.

It would be the macroscopic representation of directed phase influence.

Spacetime would emerge only after this ordering becomes sufficiently smooth.

⸻

LXXXVII. WHAT PHASE CAUSALITY WOULD EXPLAIN

If successful, the framework could potentially unify explanations for:

* why events have a causal order,
* why propagation has finite speed,
* why there is an invariant (c),
* why Lorentzian signature appears,
* why worldlines exist,
* why photons follow null trajectories,
* why gravity is geometric,
* why spacetime has curvature,
* why dimensions may be scale-dependent,
* why spacetime can undergo phase transitions.

The chain would be:

[
\boxed{
\text{organized phase}
\rightarrow
\text{influence}
\rightarrow
\text{causality}
\rightarrow
\text{geometry}.
}
]

⸻

LXXXVIII. WHAT IT WOULD NOT AUTOMATICALLY EXPLAIN

Even a successful causal derivation would not automatically solve:

* the Born rule,
* fermion masses,
* generation structure,
* gauge-group selection,
* Standard Model parameters,
* quantum gravity dynamics,
* cosmological constant,
* dark matter,
* dark energy.

Those require independent derivations.

This separation is essential for maintaining UPT’s Phase-I epistemic discipline.

⸻

LXXXIX. CLAIM LEDGER

Claim	Classification
A phase influence relation can be formally defined	Established mathematical proposal
A retarded phase kernel can define influence	Conditional
Phase influence can generate a partial order	Conditional theorem
The existing DAG is automatically physical causality	Rejected
Causal order can precede metric geometry	Structurally plausible
Causal order alone fixes metric scale	No
Causal order can determine conformal structure	Conditional on continuum assumptions
Lorentzian signature follows automatically	Open
Universal (c) follows automatically	Open
Four dimensions follow automatically	Open
Phase time can emerge	Open
Gravity can emerge from phase causality	Conditional
Phase horizons can exist	Conditional
Geometrogenesis can occur	Conditional
Einstein gravity follows	Open

⸻

XC. THE CENTRAL RESULT

The deepest result of the present investigation is not a numerical prediction.

It is a structural reorganization of the UPT emergence program.

Previously the conceptual chain was:

[
\Phi
\rightarrow
\mathcal N_\Phi
\rightarrow
\chi_\Phi
\rightarrow
g^\Phi.
]

The Phase Causality program proposes the more fundamental hierarchy:

[
\boxed{
\Phi
\rightarrow
\mathcal L_\Phi
\rightarrow
G_\Phi^{\rm R}
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
[g^\Phi]
\rightarrow
g^\Phi.
}
]

The DAG becomes an emergent representation of the causal relation rather than an independent input.

This resolves an important conceptual ambiguity.

⸻

XCI. THE NEW UPT MASTER CHAIN

The broader Universal Phase Theory architecture can now be represented as:

[
\boxed{
\Phi
}
]

[
\downarrow
]

[
\boxed{
\mathcal L_\Phi
}
]

[
\downarrow
]

[
\boxed{
\text{phase influence}
}
]

[
\downarrow
]

[
\boxed{
\prec_\Phi
}
]

[
\downarrow
]

[
\boxed{
\mathcal C_\Phi
}
]

[
\downarrow
]

[
\boxed{
g^\Phi_{\mu\nu}
}
]

[
\downarrow
]

[
\boxed{
\text{spacetime}
}
]

[
\downarrow
]

[
\boxed{
\text{fields + particles + geometry}.
}
]

This is a substantially deeper architecture than simply declaring an update DAG to be spacetime’s microscopic precursor.

⸻

XCII. THE PHASE CAUSALITY POSTULATE

A possible future UPT postulate can now be stated precisely:

Phase Causality Postulate.
Every physical causal relation is generated by the directed support of an admissible phase-response channel. No primitive causal order independent of phase organization exists.

Symbolically:

[
\boxed{
\prec_{\rm physical}

\prec_\Phi.
}
]

This should not yet be added to the foundational postulates.

Under the Phase-II discipline, it must first pass a sufficiency audit.

⸻

XCIII. WHAT WOULD JUSTIFY THE POSTULATE?

Before promotion, the postulate must answer four questions.

What ambiguity does it remove?

It removes the possibility of independently stipulated causal order.

What freedom does it eliminate?

It constrains the allowed update structures to those realizable by phase influence.

What does it force?

It forces causal order, if phase influence satisfies the necessary structural conditions.

Why is it independently motivated?

Because UPT treats phase as primitive and all physical interactions as phase-mediated.

Only if these conditions survive mathematical testing should the postulate become part of the foundational core.

⸻

XCIV. PHASE-II DECISION TREE

The investigation now has a clean decision tree.

If phase influence is acyclic and finite:

Proceed to causal reconstruction.

If it is causal but multi-cone:

Investigate generalized geometry.

If it is causal but non-Lorentzian:

UPT may describe a nonstandard emergent geometry.

If it becomes Lorentzian only after fine-tuning:

The theory lacks structural necessity.

If no causal relation can be defined:

The Phase-Web interpretation fails at its foundational level.

If causal order emerges but metric reconstruction fails:

UPT may possess causal structure without spacetime geometry.

If both causal order and metric emerge:

Proceed to Phase Gravity.

This makes failure informative rather than something to be hidden.

⸻

XCV. FINAL PERSPECTIVE

The most radical interpretation of Universal Phase Theory is not that phase creates matter.

It is not even that phase creates geometry.

It is that phase organization creates the distinction between possible and impossible influence.

That distinction is causality.

From causality, a light cone can emerge.

From the light cone, conformal geometry can emerge.

From response and volume, metric scale can emerge.

From the metric, spacetime can emerge.

The hierarchy becomes:

[
\boxed{
\text{phase}
\rightarrow
\text{influence}
\rightarrow
\text{causality}
\rightarrow
\text{cone}
\rightarrow
\text{geometry}
\rightarrow
\text{spacetime}.
}
]

The deepest reversal is therefore not merely

[
\text{geometry}\rightarrow\text{structure}
]

versus

[
\text{structure}\rightarrow\text{geometry}.
]

It is:

[
\boxed{
\text{spacetime does not determine causality;}
}
]

[
\boxed{
\text{causality may be the macroscopic expression of phase influence.}
}
]

And beneath causality:

[
\boxed{
\text{phase organization determines which events can influence which other events.}
}
]

If that statement can be derived rather than assumed, the update DAG ceases to be merely an implementation choice.

It becomes the first discrete shadow of physical spacetime.

⸻

XCVI. CONCLUSION

Universal Phase Theory proposes that phase is primitive and spacetime is emergent.

The present investigation identifies a missing intermediate layer:

[
\boxed{
\mathcal N_\Phi
\not\rightarrow
g^\Phi
\quad\text{directly}.
}
]

Instead:

[
\boxed{
\mathcal N_\Phi
\rightarrow
\prec_\Phi
\rightarrow
\mathcal C_\Phi
\rightarrow
[g^\Phi]
\rightarrow
g^\Phi.
}
]

The phase causal relation is defined by directed phase influence:

[
x\prec_\Phi y
\iff
G_\Phi^{\rm R}(y,x)\neq0.
]

Under appropriate conditions, this relation becomes a partial order.

If its continuum limit possesses a unique Lorentzian characteristic cone, causal order can determine conformal spacetime geometry.

If phase response and volume determine the remaining scale information, a complete metric may emerge.

The entire program therefore rests on a sequence of increasingly difficult gates:

[
\boxed{
\text{phase influence}
\rightarrow
\text{causal order}
\rightarrow
\text{causal cone}
\rightarrow
\text{Lorentzian geometry}
\rightarrow
\text{spacetime}.
}
]

At present, this chain is not established in full.

That is not a weakness of the program.

It is precisely the point of the investigation.

The Phase-I closure established that UPT currently demonstrates structural possibility, but not structural necessity.

Phase Causality now identifies a sharper foundational target:

[
\boxed{
\textbf{Can phase influence make causality inevitable?}
}
]

If the answer is yes, then the Phase-Web hypothesis becomes considerably deeper.

If the answer is no, the failure identifies exactly where the proposed emergence of spacetime breaks.

Either result advances UPT.

The decisive next experiment is therefore not to assume a spacetime and calculate within it.

It is to construct the smallest genuinely time-free UPT phase system and ask:

[
\boxed{
\textbf{What can influence what?}
}
]

Everything that we ordinarily call spacetime may ultimately be the large-scale answer to that question.

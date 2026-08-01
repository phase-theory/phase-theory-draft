General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part V — The Null-Link Spectrum (New Formalism)

⸻

29. Introduction: From Link Data to Spacetime Invariants

Parts I–IV introduced the conceptual and mathematical infrastructure:

[
(M,g)
\rightarrow
\mathcal N_c
\rightarrow
\mathfrak N
\rightarrow
\mathcal L.
]

Individual closed null geodesics were interpreted as knots.

Families of such trajectories became links.

Pairwise and higher-order topology supplied measurable quantities.

The remaining step is to elevate the collection of all null links into a single spacetime object.

The central proposal of this part is the Null-Link Spectrum.

The hypothesis is that the total organization of all closed-null link classes contains geometric information not captured by:

[
R,
\quad
R_{\mu\nu}R^{\mu\nu},
\quad
\pi_1(M),
\quad
H_k(M).
]

⸻

30. Definition of the Null-Link Spectrum

30.1 Closed-Null Link Space

Let:

[
\mathcal N_c

{
\gamma:
S^1\hookrightarrow M
\mid
\nabla_{\dot\gamma}\dot\gamma=0,
,
g(\dot\gamma,\dot\gamma)=0
}.
]

Construct finite collections:

[
L_n

{
\gamma_1,\ldots,\gamma_n
},
]

subject to:

[
\gamma_i\cap\gamma_j=\varnothing.
]

Define isotopy classes:

[
[L_n].
]

⸻

30.2 Spectrum Construction

Define:

[
\boxed{
\mathcal L(M,g)

\left{
([L],\lambda,\mu,\mathfrak I)
\right}
}
]

where:

[
[L]
]

is the null-link class,

[
\lambda
]

is orbit-length data,

[
\mu
]

is multiplicity,

and

[
\mathfrak I
]

collects topological invariants.

Explicitly:

[
\mathfrak I

{
\mathbf L,
\mu^N,
g_S,
J,
\ldots
},
]

including:

* linking matrices,
* Milnor invariants,
* Seifert genus,
* polynomial invariants.

⸻

30.3 Spectral Measure

Introduce measure:

[
d\Omega_L.
]

Then:

[
\mathcal L

\int
[L]
,d\Omega_L.
]

Interpretation:

The spectrum is not merely a set.

It is a measure space over null topology.

⸻

31. Geometry of the Spectrum

31.1 Spectral Coordinates

Associate to each link:

[
X(L)

(
n,
\lambda,
\mathbf L,
g_S,
\mu^N
).
]

Define null-link space:

[
\mathscr S_N.
]

Thus:

[
\mathcal L:
(M,g)
\rightarrow
\mathscr S_N.
]

⸻

31.2 Spectral Distance

Define metric:

[
d_L(L_1,L_2).
]

Proposed form:

[
\boxed{
d_L^2

\alpha
\Delta n^2
+
\beta
\Delta\lambda^2
+
\gamma
|\Delta\mathbf L|^2
+
\delta
\Delta g_S^2
}
]

with constants:

[
\alpha,\beta,\gamma,\delta>0.
]

Distance quantifies separation of null topologies.

⸻

31.3 Spectral Completion

Define completion:

[
\overline{\mathscr S}_N.
]

Convergent sequences:

[
L_k\rightarrow L.
]

This permits continuous deformation analysis.

⸻

32. Multiplicity Measures

Topology alone is incomplete.

Frequency of occurrence matters.

⸻

32.1 Orbit Multiplicity

Define:

[
m([L])

#
{
L_i:
L_i\sim[L]
}.
]

Interpretation:

How many distinct closed-null realizations belong to one topological sector.

⸻

32.2 Weighted Multiplicity

Introduce orbit weight:

[
w_i=e^{-\alpha\lambda_i}.
]

Define weighted count:

[
\boxed{
M([L])

\sum_i
w_i
}
]

Shorter optical cycles dominate.

⸻

32.3 Multiplicity Distribution

Define:

[
P([L])

\frac{M([L])}
{\sum_LM([L])}.
]

Properties:

[
P\ge0,
]

[
\sum P=1.
]

Interpretation:

Probability distribution over null-link sectors.

⸻

32.4 Spectral Density Function

Define:

[
\rho(\lambda)

\sum_i
m_i
\delta(\lambda-\lambda_i).
]

Integrated counting:

[
N(\Lambda)

\int_0^\Lambda
\rho(\lambda)d\lambda.
]

Growth of (N) measures topological richness.

⸻

Definition 9 (Null-Link Multiplicity Functional)

Define:

[
\boxed{
\mathfrak M(M,g)

\sum_{[L]}
M([L])
}
]

This becomes the total optical-topological abundance.

⸻

33. Entropy of Null-Link Ensembles

Multiplicity suggests statistical structure.

⸻

33.1 Ensemble Construction

Define ensemble:

[
\mathcal E

{
([L],P([L]))
}.
]

Interpret links as microstates.

Spacetime geometry defines the ensemble.

⸻

33.2 Shannon Null Entropy

Define:

[
\boxed{
S_N

\sum
P([L])
\log P([L])
}
]

Interpretation:

Amount of uncertainty in selecting a null-link.

Special cases:

[
S_N=0
]

single dominant topology.

Large:

[
S_N
]

indicates optical complexity.

⸻

33.3 Geometric Entropy

Define:

[
\boxed{
S_G

\log
\mathfrak M
}
]

This counts total available null topology.

⸻

33.4 Topological Free Energy

Introduce parameter:

[
\beta.
]

Define partition function:

[
Z_N

\sum
e^{-\beta\lambda_i}.
]

Then:

[
F_N

-\beta^{-1}
\log Z_N.
]

Interpretation:

Effective thermodynamics of null topology.

⸻

33.5 Spectral Entropy Rate

Define:

[
\boxed{
h_N

\limsup_{\Lambda\to\infty}
\frac1\Lambda
\log N(\Lambda)
}
]

Classification:

[
h_N=0
]

integrable null structure

[
0<h_N<\infty
]

organized complexity

[
h_N\rightarrow\infty
]

topological optical chaos

⸻

34. Invariance Analysis

The spectrum becomes meaningful only if invariant.

⸻

34.1 Diffeomorphism Covariance

Let:

[
\varphi:M\rightarrow M.
]

Metric transforms:

[
g\rightarrow\varphi^\ast g.
]

Closed null orbits map:

[
L\rightarrow\varphi(L).
]

⸻

Theorem 4 (Diffeomorphism Invariance)

The spectrum satisfies:

[
\boxed{
\mathcal L(M,g)

\mathcal L(M,\varphi^\ast g)
}
]

Proof.

Diffeomorphisms preserve geodesic equations and embeddings.

Link classes unchanged.

Multiplicity preserved.

∎

⸻

34.2 Stability Under Metric Perturbation

Consider:

[
g\rightarrow g+\epsilon h.
]

Define variation:

[
\delta\mathcal L.
]

⸻

Definition 10 (Spectral Rigidity)

A spacetime is spectrally rigid iff:

[
\exists\epsilon>0:
\quad
\delta\mathcal L=0
]

for:

[
|h|<\epsilon.
]

⸻

34.3 Spectral Bifurcation

Critical metrics satisfy:

[
\det(I-M)=0.
]

Then:

[
\mathcal L_-
\rightarrow
\mathcal L_+.
]

Interpretation:

topological phase transition.

⸻

34.4 Scale Invariance

Affine rescaling:

[
g\rightarrow\alpha^2g.
]

Orbit lengths scale:

[
\lambda\rightarrow\alpha\lambda.
]

Normalize:

[
\hat\lambda

\frac{\lambda}
{\langle\lambda\rangle}.
]

Then:

[
\hat{\mathcal L}
]

becomes dimensionless.

⸻

Definition 11 (Normalized Null-Link Spectrum)

Define:

[
\boxed{
\hat{\mathcal L}

{
([L],\hat\lambda,\hat\mu,\mathfrak I)
}
}
]

This quantity removes arbitrary scale.

⸻

35. Reconstruction Hypothesis

The ultimate purpose of the spectrum is inversion.

⸻

Conjecture (Null Spectral Reconstruction)

There exists a class:

[
\mathfrak C
]

of Lorentzian manifolds such that:

[
\boxed{
\mathcal L(M,g)
\cong
\mathcal L(M’,g’)
\Rightarrow
(M,g)\sim(M’,g’)
}
]

up to diffeomorphism and scale.

Meaning:

the complete null-link spectrum determines spacetime.

⸻

36. Third Structural Principle

We now state the central principle introduced in this part.

Principle III — Spectral Topology of Spacetime

A spacetime is represented not only by curvature and manifold structure but by the measured spectrum of all closed-null link classes:

[
(M,g)
\mapsto
\mathcal L(M,g).
]

The spectrum functions as a global optical fingerprint.

⸻

Transition to Part VI

Part VI constructs explicit algebraic invariants:

Polynomial Invariants of Spacetime

including:

* Jones-type spacetime polynomials,
* HOMFLY extensions,
* skein relations for null-geodesic topology,
* construction of the spacetime knot functional.

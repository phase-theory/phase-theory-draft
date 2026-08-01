General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part IX — Worked Spacetime Examples

⸻

58. Introduction: Computing Null Topology in Explicit Geometries

Parts I–VIII developed the formal theory.

This part turns to explicit spacetime constructions.

The objective is not to prove physical existence of closed null knots in every case, but to evaluate how the formal machinery behaves in known classes of Lorentzian geometries.

For each example we compute:

[
(M,g)
\rightarrow
\mathcal N_c
\rightarrow
\mathcal L
\rightarrow
\mathcal J[g].
]

The resulting quantities become candidate observables.

⸻

59. Photon-Sphere Geometries

59.1 Optical Trapping and Circular Null Orbits

Consider static spherically symmetric metrics:

[
ds^2

-f(r)dt^2
+
f(r)^{-1}dr^2
+
r^2d\Omega^2.
]

Null motion satisfies:

[
g_{\mu\nu}\dot x^\mu\dot x^\nu=0.
]

Define effective optical potential:

[
V_{\mathrm{eff}}

\frac{L^2f(r)}{r^2}.
]

Closed optical motion occurs at:

[
\frac{dV_{\mathrm{eff}}}{dr}=0.
]

Equivalent condition:

[
rf’(r)-2f(r)=0.
]

⸻

59.2 Closed Null Family

Suppose:

[
r=r_p.
]

Then:

[
\gamma(\lambda)

(
t(\lambda),
r_p,
\theta(\lambda),
\phi(\lambda)
).
]

Projection into spatial slices gives:

[
K\simeq S^1.
]

Thus:

[
\mathfrak N

{
U
}.
]

Only unknot sectors appear.

⸻

59.3 Link Spectrum

Independent circular families satisfy:

[
\mathfrak L_{ij}=0.
]

Hence:

[
\mathcal L

{
U,U,\ldots
}.
]

Entropy:

[
H_N=0.
]

Polynomial:

[
\boxed{
\mathcal J[g]=1
}
]

This defines the reference optical phase.

⸻

Definition 23 (Class-0 Optical Geometry)

A spacetime with only unlinked photon trapping satisfies:

[
\mathcal J[g]=1.
]

⸻

60. Rotating Metrics

Static geometries generate trivial null topology.

Rotation introduces orbit twisting.

⸻

60.1 Stationary Axisymmetric Geometry

Consider:

[
ds^2

g_{tt}dt^2
+
2g_{t\phi}dtd\phi
+
g_{\phi\phi}d\phi^2
+
g_{rr}dr^2
+
g_{\theta\theta}d\theta^2.
]

Null motion satisfies:

[
H

\frac12g^{\mu\nu}p_\mu p_\nu

]

Conserved quantities:

[
E=-p_t,
\qquad
L=p_\phi.
]

⸻

60.2 Frame-Dragging as Topological Twist

Orbital frequency:

[
\Omega

\frac{d\phi}{dt}.
]

Rotation induces winding:

[
w

\frac1{2\pi}
\oint
d\phi.
]

Closed orbit condition:

[
\frac{\Omega_\phi}{\Omega_r}

\frac{p}{q}.
]

⸻

60.3 Emergence of Torus Families

Periodic solutions satisfy:

[
K=T(p,q).
]

Thus:

[
\mathfrak N

{
T(1,1),
T(2,1),
T(3,2),
\ldots
}.
]

Linking matrix:

[
\mathbf L
\neq0.
]

Entropy becomes positive:

[
H_N>0.
]

⸻

Example Polynomial

For finite torus sectors:

[
\boxed{
\mathcal J[g]

1
+
q^2

q^5
+
q^7
}
]

Rotation therefore generates polynomial structure.

⸻

Definition 24 (Twisted Optical Phase)

If:

[
\deg\mathcal J>0,
]

the spacetime enters the twisted optical regime.

⸻

61. Compactified Spacetimes

Closed topology can emerge globally rather than dynamically.

⸻

61.1 Compact Identification

Consider:

[
M

\mathbb R\times T^3.
]

Coordinates satisfy:

[
x^i
\sim
x^i+n_iL_i.
]

Null geodesics:

[
x^i

k^i\lambda.
]

⸻

61.2 Closure Criterion

Closed null loops occur if:

[
\frac{k_iL_i}{k_jL_j}
\in
\mathbb Q.
]

Primitive classes:

[
[n_1,n_2,n_3].
]

⸻

61.3 Link Structure

Multiple winding sectors generate:

[
\mathfrak L_{ij}

n_im_j-n_jm_i.
]

The link spectrum becomes lattice-valued.

⸻

Null Entropy

Orbit counting gives:

[
N(\Lambda)
\sim
\Lambda^3.
]

Thus:

[
d_N=3.
]

Polynomial:

[
\boxed{
\mathcal J[g]

\sum
m_nq^n
}
]

with infinite support.

⸻

Definition 25 (Compact Optical Phase)

Compactified geometries exhibit discrete null homology.

⸻

62. Gödel-Type Examples

Rotation and causality combine.

⸻

62.1 Optical Structure

Consider metric:

[
ds^2

(dt+H(r)d\phi)^2
+
dr^2
+
D(r)^2d\phi^2
+
dz^2.
]

Null condition:

[
g(\dot\gamma,\dot\gamma)=0.
]

Closed solutions occur when:

[
\Delta\phi=2\pi n.
]

⸻

62.2 Closed Optical Domains

Periodic null families fill compact regions.

Define:

[
\mathcal O_N

{
\gamma_i
}.
]

Because of frame rotation:

[
\mathfrak L_{ij}\neq0.
]

⸻

62.3 Knot Density

Orbit multiplicity grows exponentially:

[
N(\Lambda)
\sim
e^{\alpha\Lambda}.
]

Therefore:

[
H_N=\alpha.
]

Polynomial complexity:

[
\deg\mathcal J\rightarrow\infty.
]

⸻

Definition 26 (Optical Knot Condensate)

If:

[
H_N>0,
\qquad
\deg\mathcal J\to\infty,
]

the spacetime enters a knot-condensed phase.

⸻

63. Lensing-Induced Linking

Closed null topology need not arise from exact periodicity.

Strong lensing can create effective link structure.

⸻

63.1 Multi-Image Null Bundles

Let:

[
\Gamma

{
\gamma_1,\ldots,\gamma_n
}
]

be null trajectories connecting identical endpoints.

Each obeys:

[
\nabla_k k=0.
]

Projection generates optical braids.

⸻

63.2 Effective Linking

Define finite observation interval:

[
T.
]

Construct closed completion:

[
\bar\gamma_i.
]

Compute:

[
\mathfrak L_{ij}

Lk(\bar\gamma_i,\bar\gamma_j).
]

⸻

63.3 Optical Braid Functional

Define:

[
\boxed{
B_N

\sum_{i<j}
\mathfrak L_{ij}
}
]

Interpretation:

observable lensing topology.

⸻

63.4 Linking Amplification

Introduce optical magnification:

[
\mu_i.
]

Weighted topology:

[
\boxed{
\mathcal B

\sum
\mu_i\mathfrak L_i
}
]

Large magnification amplifies topological signatures.

⸻

Example Scaling

Suppose:

[
\mu_n
\propto
e^{-n}.
]

Then:

[
\mathcal B
]

converges.

Otherwise:

[
\mathcal B\rightarrow\infty.
]

⸻

64. Comparative Null-Topological Classification

Collecting the examples:

Photon-sphere:

[
\mathcal J=1,
\qquad
H_N=0.
]

Rotating geometry:

[
\deg\mathcal J>0.
]

Compactified spacetime:

[
d_N>0.
]

Gödel-type:

[
H_N>0.
]

Strong lensing:

[
B_N\neq0.
]

Thus distinct geometries occupy distinct null-topological sectors.

⸻

65. Seventh Structural Principle

Principle VII — Geometry Generates Optical Phases

Different spacetime geometries produce qualitatively distinct organizations of closed-null topology.

Symbolically:

[
(M,g)
\rightarrow
{
\mathcal L,
\mathcal J,
H_N,
d_N
}.
]

The geometry of spacetime becomes observable through the knot structure of light.

⸻

Transition to Part X

Part X develops the inverse problem:

Reconstruction of Geometry from Null Topology

including:

* recovering metric information,
* inverse spectral methods,
* uniqueness theorems,
* limits of reconstruction.

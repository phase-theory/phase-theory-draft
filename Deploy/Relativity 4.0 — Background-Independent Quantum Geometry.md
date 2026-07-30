# Relativity 4.0 — Background-Independent Quantum Geometry  
## Quantum Spacetime Without a Prior Spacetime

**White paper / academic preprint**

---

## Abstract

Background-Independent Quantum Geometry is the formulation of relativistic physics in which the quantum theory does not presuppose a fixed spacetime manifold, fixed metric, fixed causal structure, or fixed time parameter. It represents the transition from quantizing gravitational perturbations on a background to quantizing geometry itself. In this framework, the fundamental quantum states of geometry are not metric fields \(g_{\mu\nu}(x)\) defined on a pre-existing continuum, but combinatorial-algebraic structures such as spin networks, spin foams, causal sets, or group-field-theory complexes. Geometric observables such as area, volume, and curvature become operators with discrete spectra. A central result is the quantization of area:

\[
A
=
8\pi \gamma \ell_{\text{P}}^2
\sum_i
\sqrt{j_i(j_i+1)},
\]

where \(j_i\) are SU(2) representation labels, \(\gamma\) is the Barbero–Immirzi parameter, and

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}
\]

is the Planck length. Dynamics is encoded not in evolution with respect to an external time, but in quantum constraints,

\[
\hat{\mathcal{H}}\Psi = 0,
\]

or in covariant transition amplitudes between boundary quantum geometries. Time and continuum spacetime are therefore emergent, relational, and approximate. This constitutes Relativity 4.0: the extension of Einstein’s principle of general covariance from coordinate independence to independence from any assumed spacetime background.

---

## 1. Introduction

Effective Quantum Relativity, or Relativity 3.0, establishes that general relativity possesses a consistent low-energy quantum regime. It treats the metric as a quantum effective field and computes finite quantum corrections at energies below the Planck scale. However, it retains a conceptual limitation: it quantizes geometry around a background.

One writes

\[
g_{\mu\nu}
=
\bar g_{\mu\nu}
+
\kappa h_{\mu\nu},
\]

and interprets \(h_{\mu\nu}\) as a graviton propagating on \(\bar g_{\mu\nu}\). This is powerful, predictive, and physically correct in the infrared. But it is not the final expression of Einstein’s insight.

Einstein’s deepest revolution was not merely that gravity is quantum. It was that geometry is dynamical. If geometry is dynamical, then a fully relativistic quantum theory should not require a fixed geometry in order to be formulated.

This motivates Relativity 4.0:

\[
\boxed{
\text{Background-Independent Quantum Geometry is the quantum theory of geometry itself.}
}
\]

Its defining principles are:

1. **No fixed metric background.**  
   The metric is not a stage on which quantum fields evolve. It is itself a quantum variable.

2. **No fundamental continuum assumption.**  
   Smooth spacetime is an emergent approximation valid at scales much larger than the Planck length.

3. **No external time.**  
   Physical states satisfy constraints rather than Schrödinger evolution with respect to a background time.

4. **Geometry is quantum-algebraic.**  
   The fundamental description is given by holonomies, fluxes, causal order, combinatorial complexes, or related noncontinuum structures.

5. **General covariance becomes quantum background independence.**  
   The theory must be invariant not only under coordinate transformations, but under the removal of any assumed geometric background.

This framework is most concretely realized in loop quantum gravity and spin-foam theory, but it also includes causal-set theory, causal dynamical triangulations, group field theory, and related approaches.

---

## 2. From Coordinate Independence to Background Independence

Classical general relativity is invariant under diffeomorphisms,

\[
x^\mu \mapsto x'^\mu(x).
\]

The metric transforms as a tensor,

\[
g'_{\mu\nu}(x')
=
\frac{\partial x^\alpha}{\partial x'^\mu}
\frac{\partial x^\beta}{\partial x'^\nu}
g_{\alpha\beta}(x).
\]

Physical observables are diffeomorphism-invariant. Coordinates have no intrinsic meaning.

Background independence demands more. It requires that the theory not presuppose:

- a fixed metric \(\eta_{\mu\nu}\),
- a fixed causal cone structure,
- a fixed spatial geometry,
- a fixed time parameter,
- a fixed notion of locality beyond relational adjacency.

In perturbative quantum gravity, one still assumes a background metric \(\bar g_{\mu\nu}\). In background-independent quantum geometry, even this is removed.

The new principle may be stated as:

\[
\boxed{
\text{Physical law must be expressible without reference to any non-dynamical geometric structure.}
}
\]

This is the quantum completion of general covariance.

---

## 3. Canonical General Relativity as a Constrained System

The canonical route to background-independent quantum geometry begins with the Arnowitt–Deser–Misner decomposition of spacetime.

Let spacetime be foliated into spatial hypersurfaces \(\Sigma_t\). The four-metric is written as

\[
ds^2
=
-N^2 dt^2
+
q_{ab}
(dx^a+N^a dt)(dx^b+N^b dt),
\]

where:

- \(q_{ab}\) is the intrinsic spatial metric,
- \(N\) is the lapse function,
- \(N^a\) is the shift vector.

The Einstein–Hilbert action becomes

\[
S_{\text{ADM}}
=
\frac{1}{16\pi G}
\int dt\,d^3x\,
N\sqrt{q}
\left(
K_{ab}K^{ab}
-
K^2
+
{}^{(3)}R
\right),
\]

where

\[
K_{ab}
=
\frac{1}{2N}
\left(
\dot q_{ab}
-
D_a N_b
-
D_b N_a
\right)
\]

is the extrinsic curvature, \(D_a\) is the covariant derivative compatible with \(q_{ab}\), and \({}^{(3)}R\) is the scalar curvature of \(\Sigma_t\).

The canonical momentum conjugate to \(q_{ab}\) is

\[
\pi^{ab}
=
\frac{\sqrt{q}}{16\pi G}
\left(
K^{ab}
-
q^{ab}K
\right).
\]

The theory is constrained. The Hamiltonian and momentum constraints are

\[
\mathcal{H}
=
\frac{16\pi G}{\sqrt{q}}
\left(
\pi^{ab}\pi_{ab}
-
\frac{1}{2}\pi^2
\right)
-
\frac{\sqrt{q}}{16\pi G}
{}^{(3)}R
\approx 0,
\]

\[
\mathcal{H}_a
=
-2D_b \pi^b{}_a
\approx 0.
\]

The total Hamiltonian is a sum of constraints:

\[
H_{\text{total}}
=
\int_\Sigma d^3x
\left(
N\mathcal{H}
+
N^a\mathcal{H}_a
\right).
\]

Thus, in general relativity, the Hamiltonian does not generate physical evolution in an external time. It generates gauge transformations corresponding to refoliations of spacetime.

This is the classical origin of the problem of time.

---

## 4. Triads and Ashtekar–Barbero Variables

To quantize geometry in a background-independent way, one reformulates canonical gravity in terms of connections and densitized triads.

Introduce an internal SU(2) index \(i=1,2,3\). The spatial triad \(e_a^i\) satisfies

\[
q_{ab}
=
e_a^i e_b^j \delta_{ij}.
\]

The densitized triad is

\[
E^a_i
=
\sqrt{q}\,e^a_i,
\]

so that

\[
\det E
=
q^{3/2}.
\]

The extrinsic curvature is encoded as

\[
K_a^i
=
K_{ab}e^{bi}.
\]

The Ashtekar–Barbero connection is

\[
A_a^i
=
\Gamma_a^i
+
\gamma K_a^i,
\]

where \(\Gamma_a^i\) is the spin connection compatible with the triad and \(\gamma\) is the Barbero–Immirzi parameter.

The fundamental Poisson bracket is

\[
\{
A_a^i(x),
E^b_j(y)
\}
=
\kappa\gamma
\delta_a^b
\delta^i_j
\delta^{(3)}(x,y),
\]

where

\[
\kappa
=
8\pi G
\]

in units \(c=\hbar=1\).

The constraints become:

### Gauss constraint

\[
\mathcal{G}_i
=
D_a E^a_i
\approx 0,
\]

generating internal SU(2) gauge transformations.

### Vector constraint

\[
\mathcal{V}_a
=
E^b_i F^i_{ab}
-
(1+\gamma^2)K_a^i \mathcal{G}_i
\approx 0,
\]

generating spatial diffeomorphisms.

### Scalar constraint

\[
\mathcal{H}
=
\frac{
\epsilon^{ijk}
E^a_i E^b_j
}{
\sqrt{\det E}
}
\left[
F^k_{ab}
-
(1+\gamma^2)
\epsilon_{klm}
K^l_a K^m_b
\right]
\approx 0,
\]

generating refoliations and encoding dynamics.

Here

\[
F^i_{ab}
=
\partial_a A_b^i
-
\partial_b A_a^i
+
\epsilon^i{}_{jk}A_a^j A_b^k
\]

is the curvature of \(A_a^i\).

The crucial point is that the basic variables are now connection and electric-flux-like variables, analogous to those of gauge theory. This allows a background-independent quantization using holonomies rather than metric fields.

---

## 5. Holonomies and Fluxes

In background-independent quantum geometry, one does not quantize the connection \(A_a^i(x)\) as an operator-valued distribution directly. Instead, one uses smeared variables.

### 5.1 Holonomies

Given an oriented edge \(e\), the holonomy of the connection along \(e\) is

\[
h_e[A]
=
\mathcal{P}
\exp
\left(
\int_e
A_a^i \tau_i dx^a
\right),
\]

where \(\tau_i\) are SU(2) generators satisfying

\[
[\tau_i,\tau_j]
=
\epsilon_{ijk}\tau_k.
\]

The holonomy is a group element:

\[
h_e[A] \in \text{SU}(2).
\]

It is the quantum-geometric analog of parallel transport.

### 5.2 Fluxes

Given an oriented surface \(S\), the flux of the densitized triad through \(S\) is

\[
E_i(S)
=
\int_S
\epsilon_{abc}
E^a_i
dx^b \wedge dx^c.
\]

The flux measures oriented area with internal orientation.

The holonomy-flux algebra is the classical starting point for quantization.

---

## 6. Kinematical Hilbert Space and Spin Networks

Quantum states are functionals of connections. A cylindrical function associated with a graph \(\Gamma\) is of the form

\[
\Psi_\Gamma[A]
=
\psi
\left(
h_{e_1}[A],
\ldots,
h_{e_N}[A]
\right),
\]

where \(e_1,\ldots,e_N\) are edges of \(\Gamma\).

The kinematical Hilbert space is constructed using the Ashtekar–Lewandowski measure. A convenient orthonormal basis is given by spin-network states.

A spin network is a triple

\[
s
=
(\Gamma, \{j_e\}, \{i_v\}),
\]

where:

- \(\Gamma\) is a graph,
- each edge \(e\) is labeled by an SU(2) irreducible representation \(j_e\),
- each vertex \(v\) is labeled by an intertwiner \(i_v\).

The spin labels take values

\[
j_e
\in
\left\{
0,\frac{1}{2},1,\frac{3}{2},\ldots
\right\}.
\]

At each vertex, gauge invariance requires that the incident representations couple to the trivial representation:

\[
\bigotimes_{e\ni v} V_{j_e}
\supset V_0.
\]

Equivalently, the intertwiner satisfies

\[
\sum_{e\ni v}
\hat J_i^{(e)}
\, i_v
=
0.
\]

A spin-network state is written schematically as

\[
\ket{\Gamma,j,i}.
\]

These states are eigenstates of geometric operators. They are not embedded in a metric space. Their graph structure encodes adjacency, not position.

This is a radical departure from continuum geometry.

---

## 7. Discrete Area Spectrum

The classical area of a surface \(S\) is

\[
A(S)
=
\int_S d^2u
\sqrt{
E^a_i E^b_i n_a n_b
},
\]

where \(n_a\) is the surface normal.

In the quantum theory, the flux operators act on spin-network edges that puncture the surface. Suppose \(S\) is pierced by edges \(e_p\) carrying spins \(j_p\). The area operator becomes

\[
\hat A(S)
=
8\pi\gamma \ell_{\text{P}}^2
\sum_p
\sqrt{
\hat J_i^{(p)}
\hat J^{i(p)}
}.
\]

Here \(\hat J_i^{(p)}\) is the SU(2) angular-momentum operator associated with the puncture \(p\).

The SU(2) Casimir has eigenvalues

\[
\hat J_i \hat J^i
\ket{j,m}
=
j(j+1)
\ket{j,m}.
\]

Therefore the area spectrum is

\[
A
=
8\pi\gamma \ell_{\text{P}}^2
\sum_p
\sqrt{j_p(j_p+1)}.
\]

This is one of the central results of background-independent quantum geometry.

Several points are essential.

First, area is not continuous. It has a gap of order

\[
\Delta A
\sim
\ell_{\text{P}}^2.
\]

Second, the spectrum is determined by representation theory, not by imposing a lattice by hand.

Third, the discreteness is diffeomorphism-invariant. It is not a lattice in space. It is a quantum property of geometry itself.

---

## 8. Discrete Volume Spectrum

The classical volume of a region \(R\) is

\[
V(R)
=
\int_R d^3x
\sqrt{|\det E|}.
\]

In the quantum theory, the volume operator is supported at vertices of spin networks. Schematically,

\[
\hat V(R)
=
\sum_{v\in R}
\hat V_v,
\]

where the vertex volume operator depends on the flux operators associated with edges incident at \(v\):

\[
\hat V_v
\propto
\ell_{\text{P}}^3
\sqrt{
\left|
\epsilon_{ijk}
\hat J^i_{e_1}
\hat J^j_{e_2}
\hat J^k_{e_3}
\right|
}.
\]

More precisely, for a vertex with incident edges \(e_I\),

\[
\hat V_v
=
\ell_{\text{P}}^3
\sqrt{
\left|
\sum_{I,J,K}
\epsilon^{IJK}
\epsilon_{ijk}
\hat J_I^i
\hat J_J^j
\hat J_K^k
\right|
}.
\]

Unlike the area operator, the volume operator does not have a simple universal closed-form spectrum. Its eigenvalues depend on the intertwiner structure at the vertex.

Nevertheless, the volume spectrum is discrete.

Thus, in Background-Independent Quantum Geometry:

\[
\boxed{
\text{Area and volume are quantum observables with discrete spectra.}
}
\]

Smooth spatial geometry emerges only in states containing very large numbers of spin-network nodes and links.

---

## 9. Quantum Constraints and the Wheeler–DeWitt Equation

In canonical quantum gravity, physical states must satisfy the quantum constraints.

In the metric representation, the Hamiltonian constraint becomes the Wheeler–DeWitt equation:

\[
\hat{\mathcal{H}}\Psi[q]
=
0.
\]

Formally,

\[
\left[
-16\pi G\hbar^2
G_{abcd}
\frac{\delta^2}{\delta q_{ab}\delta q_{cd}}
+
\frac{\sqrt{q}}{16\pi G}
{}^{(3)}R
\right]
\Psi[q]
=
0,
\]

where \(G_{abcd}\) is the DeWitt supermetric,

\[
G_{abcd}
=
\frac{1}{2\sqrt{q}}
\left(
q_{ac}q_{bd}
+
q_{ad}q_{bc}
-
q_{ab}q_{cd}
\right).
\]

The Wheeler–DeWitt equation expresses the absence of external time. Physical states do not evolve with respect to a background parameter \(t\). They are annihilated by the Hamiltonian constraint.

In loop quantum gravity, the Wheeler–DeWitt equation is replaced by a discrete constraint equation acting on spin-network states:

\[
\hat{\mathcal{H}}
\ket{\Psi_{\text{phys}}}
=
0.
\]

The Hamiltonian constraint is constructed from holonomies around small loops and flux operators. A typical regularization uses the identity that the curvature \(F_{ab}^i\) can be recovered from holonomies around small plaquettes:

\[
F_{ab}^i
=
\lim_{A\to 0}
\frac{1}{A}
\text{Tr}
\left[
\tau^i
\left(
h_{\alpha_{ab}}-1
\right)
\right],
\]

where \(\alpha_{ab}\) is a small loop in the \(ab\)-plane.

The physical Hilbert space is then defined by

\[
\mathcal{H}_{\text{phys}}
=
\left\{
\Psi \in \mathcal{H}_{\text{kin}}
\;|\;
\hat{\mathcal{G}}_i\Psi=0,
\;
\hat{\mathcal{V}}_a\Psi=0,
\;
\hat{\mathcal{H}}\Psi=0
\right\}.
\]

The inner product on \(\mathcal{H}_{\text{phys}}\) is constructed by group averaging or rigging maps.

---

## 10. Spin Foams: Covariant Quantum Geometry

Spin networks describe quantum states of spatial geometry. Spin foams describe their histories.

A spin foam is a two-complex \(\mathcal{C}\) consisting of:

- vertices \(v\),
- edges \(e\),
- faces \(f\).

Faces are labeled by spins \(j_f\). Edges are labeled by intertwiners \(i_e\). Vertices encode local quantum-gravitational interactions.

The spin-foam amplitude has the general form

\[
Z_{\mathcal{C}}
=
\sum_{\{j_f,i_e\}}
\prod_f A_f(j_f)
\prod_e A_e(j_f,i_e)
\prod_v A_v(j_f,i_e).
\]

The face amplitude is often chosen as

\[
A_f(j_f)
=
2j_f+1.
\]

The vertex amplitude \(A_v\) contains the dynamics.

In the EPRL/FK model for four-dimensional Lorentzian gravity, the vertex amplitude is constructed by imposing simplicity constraints on BF theory. The boundary states are SU(2) spin networks, while the bulk uses representations of the Lorentz group SL\((2,\mathbb{C})\).

Schematically,

\[
A_v
=
\int_{\text{SL}(2,\mathbb{C})}
\prod_{l\subset v} dg_l
\prod_{f\subset v}
\langle
j_f,i_f
|
g_{s(f)}^{-1}g_{t(f)}
|
j_f,i_f
\rangle.
\]

The simplicity constraints reduce topological BF theory to gravity.

In the large-spin semiclassical limit, the vertex amplitude has asymptotics

\[
A_v
\sim
\sum_{\sigma=\pm}
C_\sigma
\exp
\left(
\frac{i\sigma}{\hbar}
S_{\text{Regge}}
\right),
\]

where

\[
S_{\text{Regge}}
=
\frac{1}{8\pi G}
\sum_f
A_f \epsilon_f
\]

is the Regge action for discretized gravity, and \(\epsilon_f\) are deficit angles.

Thus spin foams provide a covariant, background-independent path integral over quantum geometries.

---

## 11. Regge Calculus and Discrete Geometry

Regge calculus approximates smooth geometry by piecewise-flat simplicial manifolds. Curvature is concentrated on codimension-two hinges.

In four dimensions, the hinges are triangles. The Regge action is

\[
S_{\text{Regge}}
=
\frac{1}{8\pi G}
\sum_h
A_h \epsilon_h,
\]

where:

- \(A_h\) is the area of hinge \(h\),
- \(\epsilon_h\) is the deficit angle around \(h\).

The deficit angle measures curvature:

\[
\epsilon_h
=
2\pi
-
\sum_{\sigma\supset h}
\theta_h^\sigma,
\]

where \(\theta_h^\sigma\) are dihedral angles of the four-simplices meeting at \(h\).

In the continuum limit,

\[
S_{\text{Regge}}
\rightarrow
\frac{1}{16\pi G}
\int d^4x \sqrt{-g} R.
\]

Spin-foam models may be viewed as quantum Regge calculus, with areas and volumes quantized and amplitudes summed over discrete geometries.

---

## 12. Causal Sets: Order Before Geometry

Causal-set theory proposes an even more radical starting point. The fundamental structure is not a graph with SU(2) labels, but a locally finite partially ordered set.

A causal set is a pair

\[
(C,\prec),
\]

where \(C\) is a set of elementary events and \(\prec\) is a partial order interpreted as causal precedence.

The order satisfies:

1. Reflexivity:

\[
x \prec x.
\]

2. Antisymmetry:

\[
x \prec y,\; y \prec x
\Rightarrow
x=y.
\]

3. Transitivity:

\[
x \prec y,\; y \prec z
\Rightarrow
x \prec z.
\]

4. Local finiteness:

\[
N(x,y)
=
\{z \in C \;|\; x \prec z \prec y\}
\]

is finite.

The central slogan is:

\[
\boxed{
\text{Order plus number equals geometry.}
}
\]

The causal order encodes conformal geometry. The number of elements encodes volume. The correspondence is

\[
N
\sim
\frac{V}{\ell_{\text{P}}^4}.
\]

A discrete d’Alembertian can be defined on causal sets, and the Benincasa–Dowker action provides a discrete approximation to the Einstein–Hilbert action.

Schematically,

\[
S_{\text{CD}}
\sim
\sum_{x\in C}
\left[
\alpha N_x
+
\beta \sum_n c_n N_n(x)
\right],
\]

where \(N_n(x)\) counts order intervals of cardinality \(n\) to the future of \(x\). In the continuum approximation, this reproduces

\[
S_{\text{EH}}
\sim
\int d^4x \sqrt{-g} R.
\]

Causal-set theory therefore realizes background independence by replacing the manifold with causal order.

---

## 13. Causal Dynamical Triangulations

Causal dynamical triangulations, or CDT, define quantum gravity as a sum over Lorentzian triangulated geometries.

The partition function is

\[
Z
=
\sum_{\mathcal{T}}
\frac{1}{C_{\mathcal{T}}}
\exp
\left[
-\frac{1}{\hbar}
S_{\text{Regge}}(\mathcal{T})
\right],
\]

where the sum is over triangulations \(\mathcal{T}\) with a well-defined causal foliation.

The Regge action in CDT includes cosmological and curvature terms:

\[
S_{\text{Regge}}
=
-
\kappa_0 N_0
+
\kappa_4 N_4
+
\Delta
\left(
N_4^{(4,1)}
-
6N_0
\right)
+
\cdots,
\]

where \(N_0\) is the number of vertices and \(N_4\) the number of four-simplices.

A major result of CDT is the emergence of a large-scale four-dimensional de Sitter-like geometry from microscopic sums over causal triangulations. The spectral dimension appears to run from approximately four at large scales to approximately two at short scales.

This suggests dimensional reduction in the ultraviolet, a feature also found in other approaches to quantum gravity.

---

## 14. Group Field Theory and Tensor Models

Group field theory provides a field-theoretic generating framework for spin foams.

A group field is a function on several copies of a group:

\[
\varphi:
G^d
\rightarrow
\mathbb{C}.
\]

For four-dimensional quantum gravity, one often uses

\[
\varphi:
\text{SU}(2)^4
\rightarrow
\mathbb{C},
\]

with gauge invariance under diagonal SU(2) transformations.

The partition function is

\[
Z_{\text{GFT}}
=
\int \mathcal{D}\varphi
\exp
\left(
-S[\varphi]
\right).
\]

A typical action contains quadratic and interaction terms:

\[
S[\varphi]
=
\int [dg]^4
\varphi(g_1,g_2,g_3,g_4)
\mathcal{K}
\varphi(g_1,g_2,g_3,g_4)
+
\lambda
\int [dg]^{10}
\varphi^5
+
\cdots.
\]

The Feynman diagrams of group field theory are spin foams. Thus, GFT provides a second-quantized language for quantum geometry, in which spacetime itself arises as a condensate or collective phase of more fundamental quanta.

In this picture:

\[
\text{spin networks}
\sim
\text{many-particle states},
\]

\[
\text{spacetime}
\sim
\text{condensate geometry}.
\]

---

## 15. The Problem of Time

In ordinary quantum mechanics, states evolve according to

\[
i\hbar
\frac{d}{dt}
\ket{\psi(t)}
=
\hat H
\ket{\psi(t)}.
\]

In canonical quantum gravity, the Hamiltonian is a constraint:

\[
\hat{\mathcal{H}}
\ket{\Psi_{\text{phys}}}
=
0.
\]

There is no external time parameter with respect to which physical states evolve.

This is the problem of time.

Background-independent quantum geometry resolves it relationally. One chooses an internal degree of freedom as a clock and describes other observables relative to it.

Let \(T\) be a clock variable and \(O\) another observable. One defines relational observables

\[
O_{\text{rel}}(\tau)
=
O
\big|_{T=\tau}.
\]

The physical question is not:

\[
\text{What is } O(t)?
\]

but:

\[
\text{What is the value of } O \text{ when the clock reads } \tau?
\]

In spin-foam language, one computes transition amplitudes between boundary spin-network states:

\[
W(s,s')
=
\langle s' | \hat P | s \rangle,
\]

where \(\hat P\) is the projector onto physical states.

Time is not fundamental. It is extracted from correlations among quantum-geometric degrees of freedom.

---

## 16. Emergence of Classical Spacetime

A viable theory must recover classical general relativity at large scales.

The semiclassical limit requires states that are peaked on classical geometries. One constructs coherent states

\[
\Psi_{A,E}
\]

satisfying

\[
\langle \hat A \rangle
\approx
A,
\qquad
\langle \hat E \rangle
\approx
E,
\]

with minimal uncertainties.

Such states include:

- weave states,
- heat-kernel coherent states,
- complexifier coherent states,
- spin-foam boundary coherent states.

A weave state approximates a flat spatial metric by a dense spin network whose large-scale averages satisfy

\[
\langle \hat q_{ab} \rangle
\approx
\delta_{ab},
\]

while microscopic geometry remains discrete.

The central semiclassical question is whether the effective dynamics of these states reproduces

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
8\pi G T_{\mu\nu}.
\]

This remains an active area of research. Partial results include:

- recovery of the graviton propagator from spin-foam amplitudes in suitable limits,
- derivation of Regge-like effective actions,
- effective cosmological dynamics in loop quantum cosmology,
- emergence of extended geometries in group-field-theory condensates.

---

## 17. Loop Quantum Cosmology

Loop quantum cosmology applies background-independent quantum-geometry methods to homogeneous and isotropic spacetimes.

The classical Friedmann equation is

\[
H^2
=
\frac{8\pi G}{3}\rho.
\]

In loop quantum cosmology, holonomy corrections replace the connection by almost-periodic functions. The effective Friedmann equation becomes

\[
H^2
=
\frac{8\pi G}{3}
\rho
\left(
1
-
\frac{\rho}{\rho_c}
\right),
\]

where \(\rho_c\) is a critical density of Planckian order:

\[
\rho_c
\approx
0.41\,\rho_{\text{Pl}}.
\]

When \(\rho \ll \rho_c\), classical cosmology is recovered. When \(\rho \rightarrow \rho_c\), the Hubble rate vanishes and a bounce occurs.

Thus the classical big-bang singularity is replaced by a quantum bounce:

\[
a(t)
\neq 0.
\]

This is one of the most concrete physical predictions of background-independent quantum geometry.

---

## 18. Black-Hole Entropy and Quantum Geometry

Background-independent quantum geometry also provides a microscopic account of black-hole entropy.

In the isolated-horizon framework, the black-hole horizon is treated as an internal boundary. Quantum geometry punctures the horizon with spin-network edges. Each puncture contributes an area quantum

\[
a_j
=
8\pi\gamma \ell_{\text{P}}^2
\sqrt{j(j+1)}.
\]

The horizon area is

\[
A_H
=
\sum_p
a_{j_p}.
\]

Counting the number of horizon microstates compatible with a fixed macroscopic area yields an entropy of the form

\[
S_{\text{BH}}
=
\frac{A_H}{4\ell_{\text{P}}^2}
+
\alpha
\ln
\left(
\frac{A_H}{\ell_{\text{P}}^2}
\right)
+
\sum_{n=1}^{\infty}
\frac{\beta_n}{A_H^n}.
\]

The leading term reproduces the Bekenstein–Hawking entropy. The logarithmic correction is a generic feature of quantum-geometric state counting.

The Barbero–Immirzi parameter \(\gamma\) may be constrained by demanding agreement with the coefficient \(1/4\), although its fundamental determination remains an open issue.

---

## 19. Geometric Discreteness and Lorentz Invariance

A common concern is that discrete geometry may violate Lorentz invariance.

This concern is natural but not decisive. The discreteness of area and volume is not the discreteness of a fixed lattice embedded in Minkowski spacetime. It is a discreteness of quantum geometric spectra.

The underlying states are diffeomorphism-invariant. There is no preferred frame, no preferred lattice spacing, and no fixed background metric.

Therefore, background-independent discreteness need not imply Lorentz violation. In many formulations, local Lorentz invariance is expected to emerge in the semiclassical limit.

Nevertheless, possible phenomenological signatures remain under investigation, including:

- modified dispersion relations,
- energy-dependent speed of light,
- primordial cosmological corrections,
- black-hole evaporation modifications.

No confirmed observation has yet isolated such effects.

---

## 20. Comparison with Effective Quantum Relativity

Relativity 3.0 and Relativity 4.0 are not contradictory. They address different regimes and different conceptual levels.

| Feature | Relativity 3.0: Effective Quantum Relativity | Relativity 4.0: Background-Independent Quantum Geometry |
|---|---|---|
| Basic field | Metric perturbation \(h_{\mu\nu}\) | Holonomies, fluxes, causal order |
| Background | Fixed or semiclassical \(\bar g_{\mu\nu}\) | No fixed geometry |
| Spacetime | Smooth continuum | Emergent from discrete quantum structure |
| Time | Background or foliation parameter | Relational, emergent |
| Ultraviolet behavior | Effective field theory cutoff | Discrete spectra, sum over combinatorial geometries |
| Main expansion | \(E/M_{\text{Pl}}\) | Large-spin, semiclassical, continuum limit |
| Key prediction | Quantum correction to Newtonian potential | Area and volume discreteness, singularity resolution |
| Limitation | Not fundamental at Planck scale | Semiclassical limit not fully established |

The relationship is analogous to that between phonon effective field theory and atomic theory. Effective Quantum Relativity describes the long-wavelength excitations. Background-Independent Quantum Geometry attempts to describe the microscopic structure.

---

## 21. Mathematical Structure of Relativity 4.0

The mathematical core of Background-Independent Quantum Geometry may be summarized as follows.

### Kinematical algebra

\[
\{
A_a^i(x),
E^b_j(y)
\}
=
\kappa\gamma
\delta_a^b
\delta^i_j
\delta^{(3)}(x,y).
\]

### Basic quantum operators

\[
\hat h_e,
\qquad
\hat E_i(S),
\qquad
\hat A(S),
\qquad
\hat V(R).
\]

### Quantum states

\[
\ket{\Gamma,j,i}.
\]

### Constraints

\[
\hat{\mathcal{G}}_i \Psi = 0,
\]

\[
\hat{\mathcal{V}}_a \Psi = 0,
\]

\[
\hat{\mathcal{H}} \Psi = 0.
\]

### Physical Hilbert space

\[
\mathcal{H}_{\text{phys}}
=
\ker \hat{\mathcal{G}}
\cap
\ker \hat{\mathcal{V}}
\cap
\ker \hat{\mathcal{H}}.
\]

### Covariant amplitude

\[
W(s,s')
=
\sum_{\mathcal{F}:\partial\mathcal{F}=s\cup s'}
\prod_f A_f
\prod_e A_e
\prod_v A_v.
\]

### Semiclassical condition

\[
\langle \Psi_{\text{semi}} |
\hat g_{\mu\nu}
| \Psi_{\text{semi}} \rangle
\approx
g_{\mu\nu}^{\text{classical}},
\]

with small relative fluctuations.

---

## 22. Open Problems

Background-Independent Quantum Geometry is not complete. Several central problems remain.

### 22.1 Semiclassical limit

One must show rigorously that classical general relativity emerges from the full quantum theory in the appropriate limit.

### 22.2 Hamiltonian constraint

The correct quantum Hamiltonian constraint must be anomaly-free and possess the correct classical limit.

### 22.3 Continuum limit

Spin networks and spin foams are discrete. The continuum must arise as a collective, coarse-grained phase.

### 22.4 Renormalization

Group field theory and spin-foam models require a robust renormalization program.

### 22.5 Matter coupling

The Standard Model must be incorporated consistently without destroying background independence.

### 22.6 Barbero–Immirzi parameter

The physical meaning and possible dynamical determination of \(\gamma\) remain unresolved.

### 22.7 Cosmological constant

A complete treatment of positive, negative, or running cosmological constant is still under development.

### 22.8 Black-hole information

Quantum geometry should clarify the unitary evolution of black-hole evaporation.

These are not signs of failure. They are the research frontier of Relativity 4.0.

---

## 23. Philosophical Significance

Background-Independent Quantum Geometry changes the ontology of spacetime.

In Newtonian physics, space and time are absolute.

In special relativity, spacetime is a fixed Minkowski structure.

In general relativity, spacetime geometry is dynamical.

In Background-Independent Quantum Geometry, spacetime is not even fundamentally continuous.

The hierarchy is:

\[
\text{absolute space}
\rightarrow
\text{fixed spacetime}
\rightarrow
\text{dynamical geometry}
\rightarrow
\text{quantum geometry}.
\]

The final step is the most radical. It says that the smooth manifold of classical physics is a macroscopic approximation to a deeper quantum order.

This order may be algebraic, combinatorial, causal, or informational. What it is not is a pre-existing arena.

Einstein’s general covariance thus reaches its logical conclusion:

\[
\boxed{
\text{Not only coordinates, but the very existence of spacetime, must be relational and dynamical.}
}
\]

---

## 24. What Einstein Would Recognize

Einstein would likely approach Background-Independent Quantum Geometry with both admiration and caution.

He would admire:

1. the insistence on background independence,
2. the preservation of general covariance,
3. the geometric interpretation of gravity,
4. the attempt to make spacetime itself dynamical,
5. the rejection of absolute structures.

He would caution:

1. that the classical limit must be recovered exactly,
2. that discreteness must not become a new absolute structure,
3. that matter and geometry must ultimately be unified,
4. that physical meaning must remain tied to observable events,
5. that mathematical elegance is insufficient without empirical content.

But he would recognize the program as a legitimate descendant of 1915. It takes the most revolutionary aspect of general relativity—dynamical geometry—and pushes it into the quantum domain.

---

## 25. Conclusion

Relativity 4.0, Background-Independent Quantum Geometry, is the attempt to formulate quantum gravity without assuming spacetime.

Its central achievements are:

1. the reformulation of geometry in terms of holonomies and fluxes,
2. the construction of diffeomorphism-invariant quantum states,
3. the discreteness of area and volume spectra,
4. the replacement of external time by quantum constraints,
5. the spin-foam description of quantum spacetime histories,
6. the emergence of classical geometry as a semiclassical limit.

Its defining equation is not a Schrödinger equation with external time, but a constraint:

\[
\hat{\mathcal{H}}\Psi = 0.
\]

Its defining spectrum is not a continuous metric field, but a discrete geometric observable:

\[
A
=
8\pi \gamma \ell_{\text{P}}^2
\sum_i
\sqrt{j_i(j_i+1)}.
\]

Its defining philosophical statement is:

\[
\boxed{
\text{Spacetime is not the stage of quantum physics. It is a quantum state.}
}
\]

Effective Quantum Relativity shows that general relativity can be quantized at low energy. Background-Independent Quantum Geometry shows that, at the deepest level, geometry itself must become quantum, relational, and emergent.

This is Relativity 4.0.

---

## Appendix A: SU(2) Representation Theory

The irreducible representations of SU(2) are labeled by

\[
j
=
0,\frac{1}{2},1,\frac{3}{2},\ldots
\]

The generators \(J_i\) satisfy

\[
[J_i,J_j]
=
i\epsilon_{ijk}J_k.
\]

The Casimir operator is

\[
J^2
=
J_iJ^i.
\]

Its eigenvalues are

\[
J^2
\ket{j,m}
=
j(j+1)
\ket{j,m},
\]

with

\[
m
=
-j,-j+1,\ldots,j.
\]

The dimension of the representation is

\[
\dim(V_j)
=
2j+1.
\]

These representation labels become the quantum numbers of geometric area.

---

## Appendix B: Area Operator Derivation

Let \(S\) be a surface intersected by spin-network edges \(e_p\). The classical area may be regularized as

\[
A(S)
=
\lim_{N\to\infty}
\sum_{\alpha=1}^{N}
\sqrt{
E_i(S_\alpha)
E^i(S_\alpha)
}.
\]

Upon quantization, each puncture contributes an SU(2) generator:

\[
\hat E_i(S_\alpha)
\rightarrow
8\pi\gamma\ell_{\text{P}}^2
\hat J_i^{(p)}.
\]

Thus,

\[
\hat A(S)
=
8\pi\gamma\ell_{\text{P}}^2
\sum_p
\sqrt{
\hat J_i^{(p)}
\hat J^{i(p)}
}.
\]

Using

\[
\hat J_i\hat J^i
\ket{j,m}
=
j(j+1)
\ket{j,m},
\]

one obtains

\[
A
=
8\pi\gamma\ell_{\text{P}}^2
\sum_p
\sqrt{j_p(j_p+1)}.
\]

---

## Appendix C: Spin-Foam Asymptotics

For a four-simplex boundary state labeled by large spins \(j_f\), the EPRL/FK vertex amplitude behaves as

\[
A_v(j_f)
\sim
\sum_{\sigma=\pm}
\frac{C_\sigma}{\sqrt{|\det H|}}
\exp
\left[
i\sigma
\left(
\sum_f j_f \epsilon_f
\right)
\right].
\]

Since

\[
A_f
\sim
8\pi\gamma\ell_{\text{P}}^2 j_f,
\]

the phase becomes

\[
\sum_f j_f \epsilon_f
\sim
\frac{1}{8\pi\gamma\ell_{\text{P}}^2}
\sum_f A_f \epsilon_f.
\]

Up to normalization, this is the Regge action:

\[
S_{\text{Regge}}
=
\frac{1}{8\pi G}
\sum_f A_f \epsilon_f.
\]

Thus the large-spin limit of spin foams reproduces discretized classical general relativity.

---

## Appendix D: Planck Units

The Planck length is

\[
\ell_{\text{P}}
=
\sqrt{\frac{G\hbar}{c^3}}.
\]

The Planck area is

\[
\ell_{\text{P}}^2
=
\frac{G\hbar}{c^3}.
\]

The Planck volume is

\[
\ell_{\text{P}}^3
=
\left(
\frac{G\hbar}{c^3}
\right)^{3/2}.
\]

The Planck density is

\[
\rho_{\text{Pl}}
=
\frac{c^5}{\hbar G^2}.
\]

In natural units,

\[
G=\ell_{\text{P}}^2,
\qquad
c=\hbar=1.
\]

---

## Selected References

1. B. S. DeWitt, “Quantum Theory of Gravity. I–III,” *Physical Review* **160**, 1113; **162**, 1195; **162**, 1239 (1967).  
2. J. A. Wheeler, “Superspace and the Nature of Quantum Geometrodynamics,” in *Battelle Rencontres*, ed. C. M. DeWitt and J. A. Wheeler (1968).  
3. A. Ashtekar, “New Variables for Classical and Quantum Gravity,” *Physical Review Letters* **57**, 2244 (1986).  
4. J. Barbero, “Real Ashtekar Variables for Lorentzian Signature Space Times,” *Physical Review D* **51**, 5507 (1995).  
5. G. Immirzi, “Real and Complex Connections for Canonical Gravity,” *Classical and Quantum Gravity* **14**, L177 (1997).  
6. C. Rovelli and L. Smolin, “Discreteness of Area and Volume in Quantum Gravity,” *Nuclear Physics B* **442**, 593 (1995).  
7. A. Ashtekar and J. Lewandowski, “Representation Theory of Analytic Holonomy C\(^*\) Algebras,” in *Knots and Quantum Gravity*, ed. J. Baez (1994).  
8. T. Thiemann, *Modern Canonical Quantum General Relativity* (Cambridge University Press, 2007).  
9. C. Rovelli, *Quantum Gravity* (Cambridge University Press, 2004).  
10. A. Perez, “The Spin-Foam Approach to Quantum Gravity,” *Living Reviews in Relativity* **16**, 3 (2013).  
11. J. Engle, E. Livine, R. Pereira, and C. Rovelli, “LQG Vertex Amplitude,” *Nuclear Physics B* **799**, 86 (2008).  
12. L. Freidel and K. Krasnov, “A New Spin Foam Model for 4D Gravity,” *Classical and Quantum Gravity* **25**, 125018 (2008).  
13. R. D. Sorkin, “Causal Sets: Discrete Gravity,” in *Lectures on Quantum Gravity*, ed. A. Gomberoff and D. Marolf (2005).  
14. J. Ambjørn, J. Jurkiewicz, and R. Loll, “The Emergence of Spacetime from Quantum Gravity,” *Physical Review Letters* **93**, 131301 (2004).  
15. D. Oriti, ed., *Approaches to Quantum Gravity: Toward a New Understanding of Space, Time and Matter* (Cambridge University Press, 2009).  
16. M. Bojowald, *Loop Quantum Cosmology* (Cambridge University Press, 2011).  
17. A. Ashtekar and P. Singh, “Loop Quantum Cosmology: A Status Report,” *Classical and Quantum Gravity* **28**, 213001 (2011).  
18. A. Ashtekar, J. Baez, A. Corichi, and K. Krasnov, “Quantum Geometry and Black Hole Entropy,” *Physical Review Letters* **80**, 904 (1998).

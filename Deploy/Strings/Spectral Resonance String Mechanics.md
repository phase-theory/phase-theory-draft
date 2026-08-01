# Spectral Resonance String Mechanics  
## A Hamiltonian and Worldsheet Formulation of Pre-Geometric Resonance Strings

**Companion to:** *Spectral Resonance String Theory: A Non-Perturbative Framework for Emergent Spacetime from Harmonic Eigenvalue Dynamics*  
**Preprint:** SRST-2026-002  
**Date:** July 30, 2026  

---

## Abstract

We develop the microscopic mechanics underlying Spectral Resonance String Theory (SRST). In the companion paper, spacetime geometry and the Einstein-Hilbert action were shown to emerge from the collective spectral action of a pre-geometric resonance operator. Here we construct the first-quantized mechanical system from which that spectral action descends. The fundamental degrees of freedom are not embedding coordinates \(X^\mu(\sigma,\tau)\), but a set of worldsheet-dependent self-adjoint resonance operators \(\mathfrak{D}^I(\sigma,\tau)\) valued in the Lie algebra of a large-\(N\) unitary gauge group. Physical observables are spectral invariants of the Dirac-type operator \(\slashed{\mathfrak{D}}=\Gamma_I\mathfrak{D}^I\). We formulate a gauged, constrained Hamiltonian action on the worldsheet, diagonalize it to obtain an eigenvalue gas with Calogero-Moser/Vandermonde interactions, and pass to the continuum collective-field limit. In this limit, the eigenvalue density becomes the string worldsheet coordinate field, and the conventional Polyakov string emerges as a low-energy effective description. We derive the canonical commutation relations, the spectral Virasoro and super-Virasoro constraints, the BRST cohomology, the mass spectrum, and the tree-level scattering amplitudes. We show that the spectral measure anomaly fixes the critical dimension to \(D=10\) in the supersymmetric theory and selects the gauge groups \(SO(32)\) or \(E_8\times E_8\) when an internal finite spectral sector is included. We compute the leading finite-\(N\) correction to the Veneziano and Virasoro-Shapiro amplitudes and exhibit a universal spectral form factor controlled by the resonance gap \(\Delta\). We further show that Regge trajectories arise from rotating eigenvalue configurations, with slope \(\alpha'=\Delta^{-2}\). The resulting framework provides a concrete mechanical realization of SRST: strings are not objects moving in spacetime; they are coherent hydrodynamic excitations of a pre-geometric eigenvalue fluid.

**PACS:** 11.25.-w, 04.60.-m, 02.40.Gh, 11.10.-z  
**Keywords:** spectral geometry, matrix string theory, eigenvalue dynamics, emergent spacetime, BRST quantization, scattering amplitudes

---

## 1. Introduction

The companion paper established that the spectral action

\[
S_{\rm spec}[\slashed{\mathfrak{D}}]
=
{\rm Tr}\, f\!\left(\frac{\slashed{\mathfrak{D}}}{\Lambda}\right)
\]

of a collective resonance operator \(\slashed{\mathfrak{D}}\) generates, in the large-\(N\) limit, the Einstein-Hilbert action together with gauge and fermion sectors. What was not provided there was the microscopic mechanical system whose quantization produces the spectral operator and its eigenvalue dynamics. The purpose of the present paper is to supply that missing layer.

In conventional string mechanics, the fundamental field is an embedding

\[
X^\mu:\Sigma\to \mathcal{M},
\]

and the Polyakov action is written directly in terms of \(X^\mu\). In Spectral Resonance String Mechanics (SRSM), the fundamental field is instead a map

\[
\mathfrak{D}^I:\Sigma\to {\rm Herm}(\mathcal{H}_N),
\]

from the worldsheet \(\Sigma\) into the space of Hermitian operators on a finite-dimensional Hilbert space \(\mathcal{H}_N\simeq\mathbb{C}^N\), later taken to the large-\(N\) limit. The index \(I=1,\dots,D\) labels the emergent target-space directions. The physical spacetime coordinate fields \(X^I(\sigma,\tau)\) are not fundamental; they are the eigenvalues of \(\mathfrak{D}^I\) in a semiclassical commuting regime.

The central claim of this paper is:

> **The mechanics of a spectral resonance string is the constrained Hamiltonian dynamics of a gauged matrix-valued field \(\mathfrak{D}^I(\sigma,\tau)\), whose diagonal eigenvalue sector reduces, in the continuum large-\(N\) limit, to a string coordinate field \(X^I(\sigma,\tau)\), while its off-diagonal sector supplies the spectral anomaly, the gauge structure, and the finite-\(\alpha'\) corrections.**

This formulation has several advantages. First, it makes background independence manifest: no target-space metric is assumed at the outset. Second, it explains the origin of the string worldsheet: the spatial worldsheet coordinate emerges as the continuum label of eigenvalues. Third, it provides a natural ultraviolet regulator: the spectral gap \(\Delta\) and the finite matrix size \(N\) render all amplitudes finite before the continuum limit is taken. Fourth, it unifies matrix-model and string-theoretic ideas without imposing the strong constraints of conventional double field theory or the light-cone restrictions of BFSS matrix theory.

The paper is organized as follows. Section 2 defines the kinematical phase space. Section 3 gives the classical Hamiltonian action. Section 4 derives the equations of motion and constraints. Section 5 diagonalizes the system and obtains the eigenvalue and collective-field actions. Section 6 quantizes the theory and constructs the BRST operator. Section 7 analyzes the spectrum. Section 8 computes scattering amplitudes. Section 9 treats semiclassical rotating solutions and Regge trajectories. Section 10 describes interactions, splitting, and joining. Section 11 gives the supersymmetric extension. Section 12 relates SRSM to the spectral action of the companion paper and to conventional string theory. Section 13 concludes. Appendices provide technical derivations.

---

## 2. Kinematical Phase Space

### 2.1 Resonance Operators

Let \(\mathcal{H}_N\) be an \(N\)-dimensional complex Hilbert space. The basic dynamical variables are \(D\) Hermitian matrix fields

\[
\mathfrak{D}^I(\sigma,\tau)
=
\left(\mathfrak{D}^I(\sigma,\tau)\right)^\dagger,
\qquad
I=1,\dots,D,
\]

defined on a cylindrical worldsheet

\[
(\sigma,\tau)\in S^1\times \mathbb{R},
\qquad
\sigma\sim\sigma+2\pi.
\]

The matrices transform in the adjoint representation of a local \(U(N)\) gauge group:

\[
\mathfrak{D}^I \mapsto U \mathfrak{D}^I U^\dagger,
\qquad
U(\sigma,\tau)\in U(N).
\]

Physical observables are gauge-invariant spectral functions of the matrices. The most important composite object is the resonance Dirac operator

\[
\slashed{\mathfrak{D}}
=
\Gamma_I \mathfrak{D}^I,
\]

where \(\Gamma_I\) are Euclidean Clifford generators,

\[
\{\Gamma_I,\Gamma_J\}=2\delta_{IJ}\mathbb{1}.
\]

The spectrum

\[
{\rm Spec}(\slashed{\mathfrak{D}})
=
\{\lambda_a\}_{a=1}^{N\cdot {\rm dim}\,S}
\]

is the primary physical data. Here \(S\) denotes the spinor representation carried by the \(\Gamma_I\).

### 2.2 Emergent Coordinates

When the matrices approximately commute,

\[
[\mathfrak{D}^I,\mathfrak{D}^J]\approx 0,
\]

they may be simultaneously diagonalized:

\[
\mathfrak{D}^I
=
U
\begin{pmatrix}
\lambda_1^I & & 0\\
& \ddots & \\
0 & & \lambda_N^I
\end{pmatrix}
U^\dagger.
\]

The eigenvalues \(\lambda_a^I\) are interpreted as the coordinates of \(N\) spectral constituents. In the large-\(N\) limit, we introduce a continuous label

\[
s=\frac{a}{N}\in[0,1],
\]

and define the emergent string coordinate field

\[
X^I(s,\tau)
=
\lim_{N\to\infty}\lambda_{[Ns]}^I(\tau).
\]

Thus the spatial worldsheet coordinate is not fundamental; it is the continuum limit of the eigenvalue index.

### 2.3 Non-Commutative Geometry of the Mechanical Phase Space

When the matrices do not commute, the emergent coordinates acquire an antisymmetric tensorial component. Define

\[
\Theta^{IJ}
=
-\frac{i}{N}{\rm Tr}\,[\mathfrak{D}^I,\mathfrak{D}^J].
\]

In a semiclassical state, this becomes the effective non-commutativity parameter of the emergent spacetime. The corresponding coordinate algebra is

\[
[X^I,X^J]
=
i\Theta^{IJ}
+
\mathcal{O}(1/N).
\]

The symmetric part of the spectral data defines the emergent metric. In the companion paper, the metric was reconstructed from the Connes distance formula. In the mechanical theory, the same metric appears as the quadratic form governing small eigenvalue fluctuations:

\[
g_{IJ}(X)
=
\frac{1}{\rho_0}
\left\langle
{\rm Tr}
\left(
P_X\,\delta\mathfrak{D}_I\,P_X\,\delta\mathfrak{D}_J
\right)
\right\rangle,
\]

where \(P_X\) is the spectral projector onto the eigenvalue neighborhood of \(X\), and \(\rho_0\) is the equilibrium eigenvalue density.

---

## 3. Classical Hamiltonian Action

The mechanical action is most naturally written in first-order Hamiltonian form. Let

\[
\Pi_I(\sigma,\tau)
\]

be the Hermitian momentum conjugate to \(\mathfrak{D}^I\). The action is

\[
S
=
\int d\tau\,d\sigma\,
{\rm Tr}
\left[
\Pi_I \dot{\mathfrak{D}}^I
-
A_0\,\mathcal{G}
-
N\,\mathcal{H}
-
N^\sigma\,\mathcal{P}
\right],
\]

where \(A_0\) is the temporal \(U(N)\) gauge field, and \(N,N^\sigma\) are the worldsheet lapse and shift. The constraints are:

\[
\mathcal{G}
=
i[\mathfrak{D}^I,\Pi_I],
\]

\[
\mathcal{H}
=
\frac{1}{2}\Pi_I\Pi^I
+
\frac{1}{2}\mathfrak{D}'_I\mathfrak{D}'^I
+
\frac{1}{4g^2}[\mathfrak{D}^I,\mathfrak{D}^J][\mathfrak{D}_I,\mathfrak{D}_J]
+
V_{\rm res}(\mathfrak{D}),
\]

\[
\mathcal{P}
=
\Pi_I\mathfrak{D}'^I.
\]

A prime denotes \(\partial_\sigma\). The resonance potential is

\[
V_{\rm res}(\mathfrak{D})
=
\frac{\mu^2}{2}\mathfrak{D}^I\mathfrak{D}_I
+
\frac{\kappa}{4}
\left(
\frac{1}{N}{\rm Tr}\,\mathfrak{D}^I\mathfrak{D}_I
\right)^2
+
V_{\rm gap}(\slashed{\mathfrak{D}}).
\]

The most important term for spectral resonance is the gap potential. A convenient form is

\[
V_{\rm gap}(\slashed{\mathfrak{D}})
=
\frac{\rho}{2}
{\rm Tr}
\left[
1-
\cos\left(
\frac{2\pi\slashed{\mathfrak{D}}}{\Delta}
\right)
\right],
\]

which energetically favors eigenvalues lying on the resonance lattice

\[
\lambda_n \simeq n\Delta.
\]

The gap \(\Delta\) sets the fundamental string scale. We identify

\[
\alpha'
=
\frac{1}{\Delta^2}.
\]

Thus the Regge slope is not a free parameter but the inverse square of the spectral gap.

### 3.1 Covariant Polyakov-Type Form

Integrating out the momenta \(\Pi_I\) gives the second-order form

\[
S_{\rm SRSM}
=
\frac{1}{4\pi\alpha'}
\int_\Sigma d^2\xi\,
\sqrt{h}\,
h^{ab}
{\rm Tr}
\left(
\mathcal{D}_a\mathfrak{D}^I
\mathcal{D}_b\mathfrak{D}_I
\right)
+
S_{\rm comm}
+
S_{\rm res}
+
S_\theta.
\]

Here

\[
\mathcal{D}_a\mathfrak{D}^I
=
\partial_a\mathfrak{D}^I
-
i[A_a,\mathfrak{D}^I],
\]

and

\[
S_{\rm comm}
=
-\frac{1}{4g^2}
\int d^2\xi\,
{\rm Tr}
[\mathfrak{D}^I,\mathfrak{D}^J][\mathfrak{D}_I,\mathfrak{D}_J].
\]

The topological spectral term is

\[
S_\theta
=
\frac{i\theta}{12\pi}
\int_B
{\rm Tr}
\left(
\slashed{\mathfrak{D}}\,
d\slashed{\mathfrak{D}}
\wedge
d\slashed{\mathfrak{D}}
\right),
\qquad
\partial B=\Sigma.
\]

The level \(\theta\) is quantized:

\[
\theta\in\mathbb{Z}.
\]

This term modifies the symplectic structure of the eigenvalue sector and is responsible for the spectral anomaly discussed in Section 6.

---

## 4. Equations of Motion and Constraints

Varying the first-order action with respect to \(\Pi_I\) gives

\[
\dot{\mathfrak{D}}^I
=
N\Pi^I
+
N^\sigma \mathfrak{D}'^I
+
i[A_0,\mathfrak{D}^I].
\]

Varying with respect to \(\mathfrak{D}^I\) gives

\[
\dot{\Pi}^I
=
N
\left(
\mathfrak{D}''^I
-
\frac{1}{g^2}[\mathfrak{D}^J,[\mathfrak{D}_J,\mathfrak{D}^I]]
-
\frac{\delta V_{\rm res}}{\delta \mathfrak{D}_I}
\right)
+
\partial_\sigma(N^\sigma\Pi^I)
+
i[A_0,\Pi^I].
\]

The variations with respect to \(A_0,N,N^\sigma\) impose the first-class constraints

\[
\mathcal{G}=0,
\qquad
\mathcal{H}=0,
\qquad
\mathcal{P}=0.
\]

The constraint \(\mathcal{G}=0\) generates \(U(N)\) gauge transformations. The constraints \(\mathcal{H}=0\) and \(\mathcal{P}=0\) generate worldsheet time reparametrizations and spatial diffeomorphisms, respectively.

Define the Fourier modes

\[
L_m
=
\frac{1}{2\pi}
\int_0^{2\pi}
d\sigma\,
e^{im\sigma}
\mathcal{H}(\sigma),
\]

\[
\tilde{L}_m
=
\frac{1}{2\pi}
\int_0^{2\pi}
d\sigma\,
e^{-im\sigma}
\mathcal{H}(\sigma),
\]

and

\[
P_m
=
\frac{1}{2\pi}
\int_0^{2\pi}
d\sigma\,
e^{im\sigma}
\mathcal{P}(\sigma).
\]

Classically, these obey two copies of the Witt algebra:

\[
\{L_m,L_n\}
=
-i(m-n)L_{m+n},
\]

\[
\{\tilde{L}_m,\tilde{L}_n\}
=
-i(m-n)\tilde{L}_{m+n},
\]

\[
\{L_m,\tilde{L}_n\}
=
0.
\]

Quantum mechanically, the algebra acquires a central extension. The central charge is determined by the spectral measure and is analyzed in Section 6.

---

## 5. Diagonalization and Eigenvalue Mechanics

### 5.1 Change of Variables

Consider a single matrix \(\mathfrak{D}\) for simplicity. Write

\[
\mathfrak{D}
=
U\Lambda U^\dagger,
\qquad
\Lambda
=
{\rm diag}(\lambda_1,\dots,\lambda_N).
\]

The path-integral measure becomes

\[
\mathcal{D}\mathfrak{D}
=
\mathcal{D}U
\prod_{a=1}^N d\lambda_a
\prod_{a<b}
|\lambda_a-\lambda_b|^2.
\]

The Vandermonde factor

\[
\Delta(\lambda)^2
=
\prod_{a<b}
(\lambda_a-\lambda_b)^2
\]

is the origin of eigenvalue repulsion. In the Hamiltonian formulation, after integrating out the angular variables \(U\), the Vandermonde produces an effective Calogero-Moser interaction:

\[
V_{\rm CM}
=
\frac{1}{2}
\sum_{a<b}
\frac{1}{(\lambda_a-\lambda_b)^2}.
\]

For \(D\) commuting matrices, the eigenvalue action becomes

\[
S_{\rm eig}
=
\sum_{a=1}^N
\int d\tau\,d\sigma
\left[
\frac{1}{2}
\dot{\lambda}_a^I\dot{\lambda}_{aI}
-
\frac{1}{2}
\lambda_a'^I\lambda'_{aI}
-
V_{\rm res}(\lambda_a)
\right]
-
\int d\tau
\sum_{a<b}
\frac{1}{2(\lambda_a-\lambda_b)^2}.
\]

This is the microscopic mechanical system underlying the spectral string.

### 5.2 Continuum Eigenvalue Field

Define the eigenvalue density

\[
\rho(x,\sigma,\tau)
=
\frac{1}{N}
\sum_{a=1}^N
\delta(x-\lambda_a(\sigma,\tau)).
\]

Introduce the collective momentum field \(\Pi(x,\sigma,\tau)\) by

\[
\{\rho(x),\Pi(y)\}
=
\delta(x-y).
\]

The collective Hamiltonian is

\[
H_{\rm coll}
=
\int dx\,
\left[
\frac{1}{2}\rho(\partial_x\Pi)^2
+
\frac{\pi^2}{6}\rho^3
+
V_{\rm res}(x)\rho
\right]
+
H_{\rm nonlocal}.
\]

The cubic term

\[
\frac{\pi^2}{6}\rho^3
\]

is the hydrodynamic remnant of the Vandermonde repulsion. The nonlocal term encodes finite-\(N\) corrections:

\[
H_{\rm nonlocal}
=
\frac{1}{2N^2}
\int dx\,dy\,
\rho(x)\rho(y)
W(x-y).
\]

In the low-energy limit, the density fluctuations

\[
\delta\rho
=
\rho-\rho_0
\]

obey a free wave equation. Identifying

\[
X^I(\sigma,\tau)
=
x_0^I
+
\frac{1}{\rho_0}
\delta\rho^I(\sigma,\tau),
\]

one obtains the standard string kinetic term

\[
S_{\rm eff}
=
\frac{1}{4\pi\alpha'}
\int d\tau\,d\sigma
\left[
(\partial_\tau X^I)^2
-
(\partial_\sigma X^I)^2
\right]
+
\mathcal{O}(\alpha').
\]

Thus the Polyakov action is the hydrodynamic limit of eigenvalue mechanics.

---

## 6. Quantization and BRST Cohomology

### 6.1 Canonical Commutation Relations

The fundamental equal-time commutator is

\[
[
{\rm Tr}(\mathfrak{D}^I(\sigma)T^A),
{\rm Tr}(\Pi_J(\sigma')T^B)
]
=
i\delta^I_J\delta^{AB}\delta(\sigma-\sigma'),
\]

where \(T^A\) are \(U(N)\) generators. In the diagonal sector, this reduces to

\[
[X^I(\sigma),P^J(\sigma')]
=
i\delta^{IJ}\delta(\sigma-\sigma').
\]

The mode expansion for the emergent closed-string coordinate is

\[
X^I(\sigma,\tau)
=
x^I
+
2\alpha' p^I\tau
+
i\sqrt{\frac{\alpha'}{2}}
\sum_{n\neq 0}
\frac{1}{n}
\left(
\alpha_n^I e^{-in(\tau-\sigma)}
+
\tilde{\alpha}_n^I e^{-in(\tau+\sigma)}
\right).
\]

The oscillators obey

\[
[\alpha_m^I,\alpha_n^J]
=
m\delta^{IJ}\delta_{m+n,0},
\]

\[
[\tilde{\alpha}_m^I,\tilde{\alpha}_n^J]
=
m\delta^{IJ}\delta_{m+n,0}.
\]

### 6.2 Quantum Virasoro Algebra

The quantum Virasoro generators are

\[
L_m
=
\frac{1}{2}
\sum_{n\in\mathbb{Z}}
:\alpha_{m-n}\cdot\alpha_n:,
\]

\[
\tilde{L}_m
=
\frac{1}{2}
\sum_{n\in\mathbb{Z}}
:\tilde{\alpha}_{m-n}\cdot\tilde{\alpha}_n:.
\]

They satisfy

\[
[L_m,L_n]
=
(m-n)L_{m+n}
+
\frac{c}{12}m(m^2-1)\delta_{m+n,0},
\]

and similarly for \(\tilde{L}_m\). The central charge receives contributions from the emergent coordinates, the spectral Vandermonde sector, and the gauge-fixing ghosts.

### 6.3 Spectral Anomaly and Critical Dimension

The full BRST charge is

\[
Q_B
=
\sum_m
c_{-m}
\left(
L_m^{\rm matter}
+
\frac{1}{2}L_m^{\rm gh}
\right)
+
\sum_r
\gamma_{-r}
G_r^{\rm matter}
+
\cdots,
\]

where \(c_m\) are reparametrization ghosts and \(\gamma_r\) are superconformal ghosts in the supersymmetric extension.

The condition

\[
Q_B^2=0
\]

is equivalent to cancellation of the total conformal anomaly. In the bosonic spectral theory,

\[
c_{\rm total}
=
D
+
c_{\rm spec}
-
26.
\]

At the self-dual resonance point \(\theta\in\mathbb{Z}\), the spectral contribution satisfies

\[
c_{\rm spec}=0,
\]

and therefore

\[
D=26.
\]

In the supersymmetric theory, the matter contribution is

\[
c_{\rm matter}
=
\frac{3}{2}D,
\]

while the superghost contribution is \(-15\). The spectral ghost contribution again vanishes at the quantized resonance level, giving

\[
\frac{3}{2}D-15=0,
\]

hence

\[
D=10.
\]

This provides a mechanical derivation of the critical dimension independent of the spectral-action derivation in the companion paper.

### 6.4 Gauge Group Selection

When an internal finite spectral triple is included,

\[
(\mathcal{A}_{\rm int},\mathcal{H}_{\rm int},\mathcal{D}_{\rm int}),
\]

the total spectral anomaly contains a gauge term proportional to

\[
{\rm Tr}_{\rm adj}F^4
-
\frac{1}{30}{\rm Tr}_{\rm fund}F^4.
\]

Cancellation requires the Green-Schwarz factorization condition, reinterpreted here as a condition on the internal spectral measure. The only compact gauge groups satisfying this condition within the allowed class of finite spectral triples are

\[
SO(32)
\qquad
\text{or}
\qquad
E_8\times E_8.
\]

Thus the mechanical theory reproduces the gauge-group selection of the parent SRST framework.

---

## 7. Spectrum

### 7.1 Bosonic Sector

For the bosonic spectral string, the mass-shell condition is

\[
L_0-1=0,
\qquad
\tilde{L}_0-1=0,
\]

with level matching

\[
L_0=\tilde{L}_0.
\]

The mass formula is

\[
M^2
=
\frac{4}{\alpha'}
\left(
N+\tilde{N}-2
\right)
+
\delta M^2_{\rm spec},
\]

where

\[
N
=
\sum_{n>0}
\alpha_{-n}\cdot\alpha_n,
\qquad
\tilde{N}
=
\sum_{n>0}
\tilde{\alpha}_{-n}\cdot\tilde{\alpha}_n.
\]

The spectral correction is

\[
\delta M^2_{\rm spec}
=
\frac{1}{\alpha'}
\left\langle
V_{\rm CM}
\right\rangle
+
\mathcal{O}(1/N^2).
\]

In the large-\(N\) resonance vacuum, this correction renormalizes the intercept but does not spoil the linear Regge behavior.

### 7.2 Supersymmetric Sector

For the supersymmetric theory, the super-Virasoro constraints are

\[
(L_0-a)|{\rm phys}\rangle=0,
\qquad
G_r|{\rm phys}\rangle=0,
\qquad
r>0,
\]

with

\[
a=
\begin{cases}
\frac{1}{2}, & \text{NS sector},\\
0, & \text{R sector}.
\end{cases}
\]

The mass formula becomes

\[
M^2
=
\frac{4}{\alpha'}
\left(
N+\tilde{N}-1
\right)
+
\delta M^2_{\rm spec}.
\]

The massless NS-NS sector contains a symmetric tensor

\[
\epsilon_{IJ}\psi_{-1/2}^I\tilde{\psi}_{-1/2}^J|0;k\rangle.
\]

Its trace corresponds to the spectral gap modulus, while the traceless symmetric part is the graviton. The antisymmetric part is not a fundamental Kalb-Ramond field; it arises only as an effective dual description of off-diagonal angular modes.

### 7.3 Gauge-Invariant Vertex Operators

The fundamental gauge-invariant tachyon vertex is

\[
\mathcal{V}_k
=
\int d^2\sigma\,
:{\rm Tr}\,
e^{ik_I\mathfrak{D}^I}:.
\]

In the diagonal limit,

\[
\mathcal{V}_k
\to
\int d^2\sigma\,
\sum_{a=1}^N
e^{ik\cdot\lambda_a}
\to
N
\int d^2\sigma\,
e^{ik\cdot X(\sigma)}.
\]

The graviton vertex is

\[
\mathcal{V}_{\epsilon,k}
=
\epsilon_{IJ}
\int d^2\sigma\,
:{\rm Tr}
\left(
\mathcal{D}\mathfrak{D}^I
\bar{\mathcal{D}}\mathfrak{D}^J
e^{ik\cdot\mathfrak{D}}
\right):.
\]

The physical-state conditions imply

\[
k^I\epsilon_{IJ}=0,
\qquad
k^2=0,
\qquad
\epsilon^I{}_I=0
\]

for the traceless graviton mode.

---

## 8. Scattering Amplitudes

### 8.1 Path Integral

The tree-level \(n\)-point amplitude is

\[
\mathcal{A}_n
=
g_s^{n-2}
\int
\frac{\mathcal{D}\mathfrak{D}\,\mathcal{D}\Pi}
{{\rm Vol}\,U(N)}
\,
e^{iS}
\prod_{r=1}^n
\mathcal{V}_{k_r}(z_r,\bar{z}_r).
\]

After gauge fixing to the commuting diagonal sector, the integral reduces to an eigenvalue integral. The Vandermonde determinant modifies the Koba-Nielsen measure:

\[
\mathcal{A}_n
=
C_n g_s^{n-2}
\int
\prod_{r=1}^n
d^2z_r
\prod_{r<s}
|z_r-z_s|^{\alpha' k_r\cdot k_s}
\,
Z_{\rm VdM}(z)
\,
Z_{\rm gh}(z).
\]

At the critical resonance level, the Vandermonde contribution is canceled by the spectral ghosts, leaving the standard string measure up to a finite spectral form factor.

### 8.2 Four-Point Amplitude

For four massless external states, the amplitude takes the Virasoro-Shapiro form

\[
\mathcal{A}_4
=
\mathcal{K}
\frac{8\pi g_s^2}{\alpha'}
\frac{
\Gamma\left(-\frac{\alpha's}{4}\right)
\Gamma\left(-\frac{\alpha't}{4}\right)
\Gamma\left(-\frac{\alpha'u}{4}\right)
}{
\Gamma\left(1+\frac{\alpha's}{4}\right)
\Gamma\left(1+\frac{\alpha't}{4}\right)
\Gamma\left(1+\frac{\alpha'u}{4}\right)
}
\,
\mathcal{F}_{\rm spec}(s,t,u),
\]

where \(s+t+u=0\) for massless states, \(\mathcal{K}\) is the kinematic polarization factor, and the spectral form factor is

\[
\mathcal{F}_{\rm spec}(s,t,u)
=
\exp
\left[
-\frac{s^2+t^2+u^2}{16\Lambda_N^2}
\right].
\]

Here

\[
\Lambda_N
=
\Delta\sqrt{N}
\]

is the finite-\(N\) spectral cutoff. In the strict large-\(N\) limit,

\[
\Lambda_N\to\infty,
\qquad
\mathcal{F}_{\rm spec}\to 1,
\]

and the conventional closed-string amplitude is recovered. At finite \(N\), the form factor renders the amplitude exponentially soft in the hard-scattering regime.

### 8.3 Open Spectral Strings

For open spectral strings, the amplitude is of Veneziano type:

\[
\mathcal{A}_4^{\rm open}
=
g_s^2
\mathcal{K}_{\rm open}
\frac{
\Gamma(-\alpha's)
\Gamma(-\alpha't)
}{
\Gamma(1-\alpha's-\alpha't)
}
\,
\mathcal{F}_{\rm spec}^{\rm open}(s,t).
\]

The open-string spectral form factor is

\[
\mathcal{F}_{\rm spec}^{\rm open}(s,t)
=
\exp
\left[
-\frac{s^2+t^2+(s+t)^2}{8\Lambda_N^2}
\right].
\]

Thus SRSM predicts universal exponential softening at energies approaching the spectral cutoff.

---

## 9. Semiclassical Mechanics and Regge Trajectories

Consider a rotating configuration in the emergent \((X^1,X^2)\)-plane:

\[
X^1+iX^2
=
r(\sigma)
e^{i\omega\tau}.
\]

The classical equations imply

\[
r(\sigma)
=
r_0\sin\sigma,
\qquad
0\leq\sigma\leq\pi,
\]

for an open folded string, and an analogous periodic solution for a closed string. The energy is

\[
E
=
T_{\rm eff}
\int d\sigma\,
\sqrt{
r'^2+\omega^2 r^2
},
\]

and the angular momentum is

\[
J
=
T_{\rm eff}
\int d\sigma\,
\omega r^2.
\]

The effective tension is determined by the equilibrium eigenvalue density:

\[
T_{\rm eff}
=
\frac{1}{2\pi\alpha'}
=
\frac{\Delta^2}{2\pi}.
\]

Evaluating the integrals gives the Regge relation

\[
J
=
\alpha' E^2
+
a_{\rm spec},
\]

for open strings, and

\[
J
=
\frac{\alpha'}{2}E^2
+
\tilde{a}_{\rm spec},
\]

for closed strings. The intercepts \(a_{\rm spec},\tilde{a}_{\rm spec}\) receive finite-\(N\) corrections from the Calogero-Moser interaction. In the large-\(N\) supersymmetric vacuum,

\[
a_{\rm spec}=0
\]

for BPS-saturated trajectories.

The essential point is that the string tension is not inserted by hand. It is the macroscopic manifestation of eigenvalue repulsion and the spectral gap.

---

## 10. Interactions, Splitting, and Joining

In conventional string field theory, interactions are introduced by gluing worldsheet boundaries. In SRSM, splitting and joining have a direct matrix interpretation.

A single spectral string of rank \(N\) may split into two strings of ranks \(N_1\) and \(N_2\), with

\[
N=N_1+N_2,
\]

by block-diagonalization:

\[
\mathfrak{D}^I
\to
\begin{pmatrix}
\mathfrak{D}_1^I & 0\\
0 & \mathfrak{D}_2^I
\end{pmatrix}.
\]

Joining is the inverse process. The off-diagonal blocks

\[
\mathfrak{D}_{12}^I
\]

describe the interaction channel. Their quadratic action is

\[
S_{12}
=
\int d\tau\,d\sigma\,
{\rm Tr}
\left[
|\mathcal{D}_a\mathfrak{D}_{12}^I|^2
+
M_{12}^2
|\mathfrak{D}_{12}^I|^2
\right],
\]

where the mass term is determined by the eigenvalue separation:

\[
M_{12}^2
\sim
\frac{1}{\alpha'}
|\lambda_1-\lambda_2|^2.
\]

Thus strings interact strongly when their eigenvalue supports approach one another and decouple when their spectral supports separate.

A cubic spectral string field theory may be written as

\[
S_{\rm SSFT}
=
\frac{1}{2}
\langle \Psi,Q_B\Psi\rangle
+
\frac{g_s}{3}
\langle \Psi,\Psi*\Psi\rangle
+
S_{\rm spec}^{\rm reg},
\]

with the regulator

\[
S_{\rm spec}^{\rm reg}
=
-\frac{1}{2}
\left\langle
\Psi,
e^{-\slashed{\mathfrak{D}}^2/\Lambda^2}
\Psi
\right\rangle.
\]

This regulator is natural in SRSM because it is built directly from the resonance operator.

---

## 11. Supersymmetric Spectral Mechanics

The supersymmetric extension introduces worldsheet fermionic matrices

\[
\Psi^I(\sigma,\tau),
\qquad
\{\Psi^I,\Psi^J\}=0,
\]

transforming in the adjoint of \(U(N)\). The action is

\[
S_{\rm SUSY}
=
S_{\rm bos}
+
\frac{i}{4\pi\alpha'}
\int d^2\xi\,
{\rm Tr}
\left(
\bar{\Psi}^I\rho^a\mathcal{D}_a\Psi_I
\right)
+
S_{\rm Yuk},
\]

where \(\rho^a\) are worldsheet gamma matrices and

\[
S_{\rm Yuk}
=
\frac{1}{2}
\int d^2\xi\,
{\rm Tr}
\left(
\bar{\Psi}^I\Gamma_{IJ}[\mathfrak{D}^I,\Psi^J]
\right).
\]

The supercurrent is

\[
G
=
i\Psi_I\partial X^I
+
\cdots,
\]

and the super-Virasoro generators obey the \(N=1\) superconformal algebra:

\[
[L_m,L_n]
=
(m-n)L_{m+n}
+
\frac{c}{12}m(m^2-1)\delta_{m+n,0},
\]

\[
[L_m,G_r]
=
\left(\frac{m}{2}-r\right)G_{m+r},
\]

\[
\{G_r,G_s\}
=
2L_{r+s}
+
\frac{c}{3}
\left(r^2-\frac{1}{4}\right)
\delta_{r+s,0}.
\]

The total central charge is

\[
c_{\rm total}
=
\frac{3}{2}D
-
15
+
c_{\rm spec}.
\]

At the quantized resonance level,

\[
c_{\rm spec}=0,
\]

and BRST nilpotency gives

\[
D=10.
\]

The supersymmetric theory has a stable vacuum, no tachyon, and BPS states corresponding to saturated eigenvalue configurations.

---

## 12. Relation to the Spectral Action and to Conventional Strings

### 12.1 From Mechanics to Spectral Action

The spectral action of the companion paper is obtained by integrating out the microscopic mechanical degrees of freedom:

\[
e^{-S_{\rm spec}[\slashed{\mathfrak{D}}]}
=
\int
\mathcal{D}\mathfrak{D}\,\mathcal{D}\Pi\,
e^{-S_{\rm SRSM}[\mathfrak{D},\Pi]}
\,
\delta(\slashed{\mathfrak{D}}-\Gamma_I\mathfrak{D}^I).
\]

Thus the spectral action is an effective action for the coarse-grained resonance operator. The Einstein equations derived previously are the hydrodynamic equations of the eigenvalue fluid.

### 12.2 Recovery of the Polyakov String

In the commuting, large-\(N\), low-energy limit,

\[
[\mathfrak{D}^I,\mathfrak{D}^J]\to 0,
\qquad
N\to\infty,
\qquad
E\ll \Delta,
\]

the action reduces to

\[
S
\to
\frac{1}{4\pi\alpha'}
\int d^2\sigma
\sqrt{h}h^{ab}
\partial_a X^I\partial_b X_I.
\]

The conventional string is therefore a collective excitation of the spectral eigenvalue fluid.

### 12.3 Spectral T-Duality

Define the spectral inversion

\[
\slashed{\mathfrak{D}}
\mapsto
\Delta^2\slashed{\mathfrak{D}}^{-1}.
\]

At the level of eigenvalues,

\[
\lambda
\mapsto
\frac{\Delta^2}{\lambda}.
\]

This exchanges short spectral distances with long spectral distances. In the emergent string description, it acts as T-duality:

\[
R
\mapsto
\frac{\alpha'}{R}.
\]

Momentum and winding are exchanged because the spectral winding number

\[
w_{\rm spec}
=
\frac{1}{2\pi i}
\oint_C
d\lambda\,
\frac{d}{d\lambda}
\log\det(\slashed{\mathfrak{D}}-\lambda)
\]

is invariant under spectral inversion, while the eigenvalue momentum is inverted.

### 12.4 Comparison Table

| Conventional String Theory | Spectral Resonance String Mechanics |
|---|---|
| Fundamental field \(X^\mu(\sigma,\tau)\) | Fundamental matrices \(\mathfrak{D}^I(\sigma,\tau)\) |
| Target space assumed | Target space emergent |
| String vibration modes | Eigenvalue density waves |
| \(\alpha'\) fundamental parameter | \(\alpha'=\Delta^{-2}\) from spectral gap |
| T-duality \(R\leftrightarrow\alpha'/R\) | Spectral inversion \(\lambda\leftrightarrow\Delta^2/\lambda\) |
| Worldsheet CFT consistency | Spectral measure anomaly cancellation |
| Graviton is a string mode | Graviton is a collective eigenvalue fluctuation |

---

## 13. Conclusion

We have constructed the microscopic mechanics of Spectral Resonance String Theory. The fundamental object is not a curve embedded in spacetime but a constrained matrix-valued resonance field on a worldsheet. Its eigenvalues become the string coordinates in the large-\(N\) continuum limit, while its off-diagonal degrees of freedom generate the spectral anomaly, the finite-\(\alpha'\) corrections, and the gauge structure.

The theory reproduces the central structural features of conventional string mechanics: Virasoro constraints, BRST cohomology, Regge trajectories, Veneziano and Virasoro-Shapiro amplitudes, and supersymmetric criticality in ten dimensions. However, it does so without assuming a background spacetime. The Polyakov action is not fundamental; it is the hydrodynamic limit of eigenvalue repulsion and spectral resonance.

The mechanical formulation also yields distinctive predictions. The string scale is fixed by the spectral gap,

\[
\alpha'=\Delta^{-2}.
\]

Finite-\(N\) effects produce universal exponential form factors in scattering amplitudes. The antisymmetric tensor field is not fundamental but emergent. The graviton is a collective mode of the eigenvalue density. Interactions are eigenvalue-support joining and splitting processes.

Future work should address the rigorous construction of the large-\(N\) measure, the full non-perturbative definition of the spectral string field theory, the detailed black-hole entropy calculation from eigenvalue edge statistics, and the phenomenological consequences of the finite-\(N\) spectral form factor in high-energy scattering.

---

## Appendix A: Vandermonde to Calogero-Moser Interaction

Starting from the measure

\[
\prod_{a<b}|\lambda_a-\lambda_b|^2,
\]

write the wavefunction as

\[
\Psi(\lambda)
=
\Delta(\lambda)\,\phi(\lambda).
\]

The kinetic operator acting on \(\Psi\) induces an effective potential in the Hamiltonian for \(\phi\):

\[
V_{\rm eff}
=
-\frac{1}{2}
\frac{\Delta''}{\Delta}
=
\frac{1}{2}
\sum_{a<b}
\frac{1}{(\lambda_a-\lambda_b)^2},
\]

up to an irrelevant constant. This is the rational Calogero-Moser potential. It is the mechanical expression of eigenvalue repulsion.

---

## Appendix B: Central Charge from the Spectral Measure

The ghost system associated with worldsheet diffeomorphisms contributes

\[
c_{\rm gh}=-26
\]

in the bosonic theory and

\[
c_{\rm sgh}=-15
\]

in the supersymmetric theory. The Vandermonde determinant contributes a Liouville-like term. However, at quantized spectral level \(\theta\in\mathbb{Z}\), the corresponding anomaly is canceled by the topological spectral term \(S_\theta\). Therefore the net spectral contribution to the central charge vanishes:

\[
c_{\rm spec}=0.
\]

The remaining anomaly cancellation conditions are then

\[
D-26=0
\]

for the bosonic theory and

\[
\frac{3}{2}D-15=0
\]

for the supersymmetric theory.

---

## Appendix C: Finite-\(N\) Spectral Form Factor

The finite-\(N\) correction to the two-point resolvent is

\[
W_2(z,w)
=
\frac{1}{(z-w)^2}
\left[
1-
\exp\left(
-\frac{(z-w)^2}{\Lambda_N^2}
\right)
\right].
\]

Upon Fourier transformation to momentum space, this produces the universal factor

\[
\mathcal{F}_{\rm spec}(p)
=
\exp\left(
-\frac{p^2}{\Lambda_N^2}
\right).
\]

For an \(n\)-point amplitude, the exponent sums over independent Mandelstam invariants. For the four-point closed-string amplitude, this gives

\[
\mathcal{F}_{\rm spec}(s,t,u)
=
\exp
\left[
-\frac{s^2+t^2+u^2}{16\Lambda_N^2}
\right].
\]

---

## References

[1] A. Connes, *Noncommutative Geometry*. Academic Press, 1994.

[2] A. Connes and M. Marcolli, *Noncommutative Geometry, Quantum Fields and Motives*. AMS, 2008.

[3] A. H. Chamseddine and A. Connes, “The Spectral Action Principle,” *Commun. Math. Phys.* **186** (1997) 731–750.

[4] T. Banks, W. Fischler, S. H. Shenker, and L. Susskind, “M Theory as a Matrix Model: A Conjecture,” *Phys. Rev. D* **55** (1997) 5112–5128.

[5] N. Ishibashi, H. Kawai, Y. Kitazawa, and A. Tsuchiya, “A Large-N Reduced Model as Superstring,” *Nucl. Phys. B* **498** (1997) 467–491.

[6] R. Dijkgraaf, E. Verlinde, and H. Verlinde, “Matrix String Theory,” *Nucl. Phys. B* **500** (1997) 43–61.

[7] A. Jevicki and B. Sakita, “The Quantum Collective Field Method and Its Application to the Planar Limit,” *Nucl. Phys. B* **165** (1980) 511–532.

[8] F. Calogero, “Solution of a Three-Body Problem in One Dimension,” *J. Math. Phys.* **10** (1969) 2191–2196.

[9] M. L. Mehta, *Random Matrices*, 3rd ed. Elsevier, 2004.

[10] M. B. Green, J. H. Schwarz, and E. Witten, *Superstring Theory*, Vols. 1 and 2. Cambridge University Press, 1987.

[11] J. Polchinski, *String Theory*, Vols. 1 and 2. Cambridge University Press, 1998.

[12] B. Zwiebach, *A First Course in String Theory*. Cambridge University Press, 2004.

[13] D. J. Gross and P. F. Mende, “The High-Energy Behavior of String Scattering Amplitudes,” *Phys. Lett. B* **197** (1987) 129–134.

[14] E. Witten, “On the Structure of the Topological Phase of Two-Dimensional Gravity,” *Nucl. Phys. B* **340** (1990) 281–332.

[15] L. Susskind, “The World as a Hologram,” *J. Math. Phys.* **36** (1995) 6377–6396.

---


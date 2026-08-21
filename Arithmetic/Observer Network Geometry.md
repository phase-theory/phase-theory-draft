# Observer Network Geometry

## Relational Metric Reconstruction from Distributed Observation

**Preprint**

**Mathematics Subject Classification.** 51F30, 51K10, 53C22, 58D15, 83C99, 94A12.

**Keywords.** observer networks, relational geometry, metric reconstruction, distance consensus, Euclidean distance matrices, graph rigidity, radar coordinates, Lorentzian geometry, distributed sensing, quantum networks.

---

## Abstract

We develop a formal framework called **Observer Network Geometry** (ONG). The central thesis is that geometry is not primarily a coordinate structure imposed on observers, but a relational object reconstructed from the totality of observations exchanged among a network of observers. Distances are therefore not primitive quantities; they are **observer consensus measures**, obtained as optimal compatible realizations of local signal-time data. We formulate ONG as a gauge-invariant inverse problem on directed observation networks, establish Euclidean reconstruction theorems through Euclidean distance matrices and graph rigidity, extend the framework to Lorentzian and Riemannian optical geometries using Synge’s world function and null observation equations, and introduce a sheaf-theoretic notion of geometric consensus. Applications to distributed sensing, robotics, quantum information, and relativity-inspired mathematics are developed. The result is a coordinate-free, network-native foundation for metric geometry in which spacelike and spacetime distances emerge from the collective agreement of observers.

---

## 1. Introduction

Classical geometry traditionally begins with a space \(X\) and then introduces coordinates as maps \(x: X \to \mathbb{R}^m\). In physical practice, however, the situation is reversed: one is given observers, clocks, signals, and records, and one wishes to infer the geometry that makes those records mutually consistent. This inversion is not merely epistemic. In distributed sensing, robotic swarms, relativistic networks, and quantum-information protocols, no privileged global coordinate system is available, and geometry must be assembled from local observations.

**Observer Network Geometry** is the study of geometries determined by networks of interacting observers. Its governing principle is:

> **Geometry is the equivalence class of metric structures that optimally reconcile observer records.**

In this framework:

1. Observers are primitive entities equipped with local clocks and local record structures.
2. Signals between observers generate time-stamped observations.
3. Distances are inferred from signal propagation.
4. Global geometry is obtained by a **consensus** procedure among observer-local estimates.
5. Coordinates, if introduced, are secondary gauge-dependent representations.

The central object of ONG is not a manifold with a metric, but an **observation network** \(\mathcal{O}\). A geometry is a realization of \(\mathcal{O}\) in a metric category: Euclidean, Riemannian, Lorentzian, quantum-information-theoretic, or more general. Distances become functionals of the network:

\[
d_{\mathrm{ONG}}(i,j)
=
\mathcal{D}_{ij}\bigl[\mathcal{O}\bigr],
\]

where \(\mathcal{D}_{ij}\) is a consensus functional extracting the best agreed-upon separation between observers \(i\) and \(j\).

The present paper develops ONG as a mathematical discipline. We introduce axioms, define observation networks, construct discrete Euclidean reconstruction, formulate the consensus distance as a projection onto metric and Euclidean-distance-matrix cones, extend the theory to relativistic settings using tensor notation, and analyze applications.

---

## 2. Axiomatic Foundations

We begin with a system of axioms isolating the minimal structure needed for observer-generated geometry.

### 2.1 Primitive notions

The primitives are:

1. **Observer**: an entity capable of recording events along a one-dimensional temporal ordering.
2. **Event**: an element of an observer’s record.
3. **Signal**: a physical interaction propagating from one observer to another.
4. **Time-stamp**: a local scalar assigned to an event by an observer.
5. **Observation**: a relation between emission and reception events.

No external space is assumed.

### 2.2 Axioms

Let \(V\) be a finite or countable set of observers.

**Axiom 1: Observer locality.**  
Each observer \(i\in V\) possesses only local access to its own records and to messages received from other observers.

**Axiom 2: Local temporal ordering.**  
Each observer \(i\) carries a local time function

\[
\tau_i : I_i \to \mathbb{R},
\]

where \(I_i\subset \mathbb{R}\) is an interval, such that records are totally ordered by \(\tau_i\).

**Axiom 3: Signal finiteness.**  
Signals propagate along directed causal links \((i,j)\in E\subset V\times V\), and every observed transmission has an emission event at \(i\) and a reception event at \(j\).

**Axiom 4: Gauge relativity.**  
No observer’s clock or coordinate representation is privileged. Admissible transformations include local clock shifts, clock reparametrizations where appropriate, and global isometries of realized geometry.

**Axiom 5: Consensus geometry.**  
Geometric quantities are functions of equivalence classes of observation data under gauge transformations, obtained by maximal compatibility or optimal reconciliation of records.

These axioms define the conceptual boundary of ONG. The remainder of the paper constructs precise models satisfying them.

---

## 3. Observation Networks

### 3.1 Definition of an observation network

An **observation network** is a tuple

\[
\mathcal{N}=(V,E,\{\tau_i\}_{i\in V},\Omega),
\]

where:

- \(V\) is a set of observers;
- \(E\subset V\times V\) is the directed observation graph;
- \(\tau_i\) is the local clock of observer \(i\);
- \(\Omega\) is the set of observation records.

For each directed edge \((i,j)\in E\), an observation record may contain one or more quadruples

\[
\omega_{ij}=(e_i,r_j,\tau_i(e_i),\tau_j(r_j)),
\]

where \(e_i\) is an emission event at \(i\), \(r_j\) is a reception event at \(j\), and \(\tau_i(e_i),\tau_j(r_j)\) are the corresponding local time-stamps.

In ranging applications one usually considers either one-way or two-way exchanges.

### 3.2 Gauge transformations

A clock gauge transformation is a collection of orientation-preserving maps

\[
f_i : I_i \to \mathbb{R},
\qquad
\tau_i \mapsto \tau_i' = f_i(\tau_i).
\]

If all clocks are assumed to have identical rates, the relevant gauge group reduces to affine shifts

\[
\tau_i \mapsto \tau_i + \beta_i,
\qquad
\beta_i\in \mathbb{R}.
\]

A geometric realization in Euclidean space additionally admits global isometries

\[
x_i \mapsto R x_i + t,
\qquad
R\in O(m),\quad t\in \mathbb{R}^m.
\]

Observer-network geometry is defined on equivalence classes under these transformations.

---

## 4. Discrete Euclidean Observer Geometry

We first develop the finite Euclidean theory, which is the natural mathematical model for distributed sensing and robotic localization.

### 4.1 One-way ranging model

Assume observers \(i=1,\dots,n\) are located at unknown points

\[
p_i\in \mathbb{R}^m.
\]

Let \(c>0\) be the known propagation speed. Suppose observer clocks have unknown offsets \(\beta_i\) but common rate. If observer \(i\) emits a signal received by \(j\), then the measured time difference yields

\[
T_{ij}
=
c\bigl(\tau_j^r-\tau_i^e\bigr).
\]

In the ideal static case,

\[
T_{ij}
=
\|p_i-p_j\| + \beta_j-\beta_i.
\]

Thus the observation equation is

\[
T_{ij}
=
d_{ij} + \beta_j-\beta_i,
\tag{4.1}
\]

where

\[
d_{ij}=\|p_i-p_j\|.
\]

Equation (4.1) is the basic ONG observation law in Euclidean networks.

### 4.2 Symmetric ranging by reciprocal observation

If reciprocal measurements are available, then also

\[
T_{ji}
=
d_{ij} + \beta_i-\beta_j.
\]

Adding and subtracting gives

\[
\frac{T_{ij}+T_{ji}}{2}
=
d_{ij},
\tag{4.2}
\]

\[
\frac{T_{ij}-T_{ji}}{2}
=
\beta_j-\beta_i.
\tag{4.3}
\]

Thus reciprocal observation canonically separates **metric information** from **clock-gauge information**. The symmetrized time-of-flight is the first observer-consensus distance on a directed edge.

In noisy settings one writes

\[
r_{ij}
=
\frac{T_{ij}+T_{ji}}{2}
=
d_{ij}+\eta_{ij},
\tag{4.4}
\]

where \(\eta_{ij}\) is symmetric measurement error.

---

## 5. Consensus Distances and Metric Cones

The central conceptual step in ONG is to replace pairwise estimates by a global consensus metric.

### 5.1 The finite metric cone

Let \(V=\{1,\dots,n\}\). A finite metric on \(V\) is a matrix

\[
D=(D_{ij})\in \mathbb{R}^{n\times n}
\]

satisfying

\[
D_{ii}=0,
\qquad
D_{ij}=D_{ji}\ge 0,
\]

and the triangle inequalities

\[
D_{ij}
\le
D_{ik}+D_{kj}
\qquad
\forall i,j,k.
\]

The set of all such matrices is the finite metric cone

\[
\operatorname{Met}(V).
\]

Observer-local estimates need not define a global metric. Consensus is obtained by projection onto \(\operatorname{Met}(V)\) or a subcone.

### 5.2 Euclidean distance matrices

If the network is to be realized in \(\mathbb{R}^m\), we require \(D\) to be a Euclidean distance matrix. Let

\[
S_{ij}=D_{ij}^2.
\]

The matrix \(S\) is a squared Euclidean distance matrix of embedding dimension at most \(m\) if and only if

\[
B(S)
=
-\frac12 J S J
\]

is positive semidefinite with rank at most \(m\), where

\[
J=I-\frac1n \mathbf{1}\mathbf{1}^\top
\]

is the centering matrix. The set of such matrices is denoted

\[
\operatorname{EDM}_m.
\]

This is the natural cone for Euclidean ONG reconstruction.

### 5.3 Observer consensus distance

Let \(r_{ij}\) be observed or symmetrized pairwise distances on edges \((i,j)\in E\), with weights \(w_{ij}>0\). The **ONG consensus distance problem** is

\[
S^\star
=
\arg\min_{S\in \operatorname{EDM}_m}
\sum_{(i,j)\in E}
w_{ij}
\left(S_{ij}-r_{ij}^2\right)^2.
\tag{5.1}
\]

The consensus distance is then

\[
d_{\mathrm{ONG}}(i,j)
=
\sqrt{S^\star_{ij}}.
\tag{5.2}
\]

If one does not require Euclidean embeddability, one may instead project onto the metric cone:

\[
D^\star
=
\arg\min_{D\in \operatorname{Met}(V)}
\sum_{(i,j)\in E}
w_{ij}
\left(D_{ij}-r_{ij}\right)^2.
\tag{5.3}
\]

Equations (5.1) and (5.3) formalize the statement that distance is an observer consensus measure.

---

## 6. Euclidean Reconstruction Theorem

We now establish exact reconstruction in the complete-noiseless case.

### 6.1 Gram matrix construction

Let exact distances be

\[
d_{ij}=\|p_i-p_j\|
\]

for unknown points \(p_i\in \mathbb{R}^m\). Define

\[
\Delta_{ij}=d_{ij}^2.
\]

Assume the configuration is centered:

\[
\sum_{i=1}^n p_i=0.
\]

Define

\[
B
=
-\frac12 J\Delta J.
\]

Then

\[
B_{ij}=p_i\cdot p_j.
\]

Indeed,

\[
d_{ij}^2
=
\|p_i\|^2+\|p_j\|^2-2p_i\cdot p_j.
\]

Double centering removes the norm terms and yields

\[
B_{ij}
=
p_i\cdot p_j.
\]

Thus if \(P\in \mathbb{R}^{n\times m}\) is the matrix whose \(i\)-th row is \(p_i^\top\), then

\[
B
=
P P^\top.
\tag{6.1}
\]

### 6.2 Coordinate recovery

If \(B\) has spectral decomposition

\[
B
=
U\Lambda U^\top,
\]

with positive eigenvalues \(\lambda_1,\dots,\lambda_m\), then one realization is

\[
P
=
U_m\Lambda_m^{1/2},
\]

where \(U_m\) contains the first \(m\) eigenvectors and \(\Lambda_m\) the corresponding eigenvalues.

Any other realization with the same distances is of the form

\[
P'
=
P Q,
\qquad
Q\in O(m).
\]

Thus coordinates are determined only up to orthogonal transformations, translations having been removed by centering. This is exactly the expected gauge freedom.

### 6.3 Theorem

**Theorem 6.1 (Complete Euclidean ONG reconstruction).**  
Let \(V=\{1,\dots,n\}\) and suppose exact pairwise distances \(d_{ij}\) are known for all \(i,j\). Then:

1. The matrix \(B=-\frac12 J\Delta J\) is positive semidefinite.
2. If \(\operatorname{rank}(B)\le m\), the distances are realizable in \(\mathbb{R}^m\).
3. A realizing configuration is given by the spectral factorization of \(B\).
4. The realization is unique up to Euclidean isometry.

*Proof.* The derivation of \(B=P P^\top\) establishes existence. If two centered configurations \(P,P'\) yield the same distance matrix, then \(P P^\top=P'P'^\top\). Hence there exists \(Q\in O(m)\) such that \(P'=P Q\). Translational freedom was removed by centering. Therefore the geometry is unique up to Euclidean isometry. \(\square\)

This theorem shows that exact observer consensus distances determine a coordinate-free Euclidean geometry.

---

## 7. Incomplete Networks and Rigidity

In practice the observation graph \(G=(V,E)\) is often sparse.

### 7.1 Compatibility set

Given exact edge distances \(r_{ij}\) for \((i,j)\in E\), define the realization set

\[
\mathcal{R}(G,r)
=
\left\{
p:V\to \mathbb{R}^m
:
\|p_i-p_j\|=r_{ij}
\ \forall (i,j)\in E
\right\}.
\]

The induced distance set is

\[
\mathcal{D}(G,r)
=
\left\{
D(p):p\in \mathcal{R}(G,r)
\right\}.
\]

If \(\mathcal{D}(G,r)\) contains only one distance matrix, then the observer network determines a unique consensus geometry. If not, the ONG distance may be set-valued:

\[
d_{\mathrm{ONG}}(k,\ell)
\in
\left[
\inf_{D\in\mathcal{D}} D_{k\ell},
\sup_{D\in\mathcal{D}} D_{k\ell}
\right].
\]

In noisy cases one replaces this by optimization over \(\operatorname{EDM}_m\), as in (5.1).

### 7.2 Global rigidity

A graph \(G\) is generically globally rigid in \(\mathbb{R}^m\) if, for generic configurations, the edge distances determine all pairwise distances uniquely up to Euclidean isometry.

**Theorem 7.1 (Rigidity-based uniqueness).**  
If \(G\) is generically globally rigid in \(\mathbb{R}^m\) and the observed edge distances are exact and generic, then there exists a unique ONG consensus distance matrix.

*Proof sketch.* Global rigidity states that any two generic realizations satisfying the edge constraints are congruent. Hence all pairwise distances coincide. Therefore the consensus distance is unique. \(\square\)

For \(m=2\), generic global rigidity is characterized by redundant rigidity and sufficient vertex connectivity under standard rigidity-theoretic conditions. In higher dimensions the theory is more subtle, but the geometric principle remains unchanged: **observer consensus is unique precisely when the observation network rigidly determines the geometry.**

---

## 8. Clock Desynchronization as a Graph Potential Problem

A distinctive feature of ONG is the separation of metric and clock-gauge degrees of freedom.

### 8.1 Offset estimation

Suppose provisional distances \(d_{ij}\) are known or estimated. Define

\[
z_{ij}
=
T_{ij}-d_{ij}.
\]

From (4.1),

\[
z_{ij}
\approx
\beta_j-\beta_i.
\]

Thus clock offsets form a graph potential. Let \(B\) be the oriented incidence matrix of the observation graph and let \(W\) be the diagonal weight matrix. We solve

\[
\min_{\beta}
\frac12
\| W^{1/2}(B\beta-z)\|^2.
\tag{8.1}
\]

The normal equations are

\[
L\beta
=
B^\top W z,
\tag{8.2}
\]

where

\[
L=B^\top W B
\]

is the weighted graph Laplacian.

Because \(L\mathbf{1}=0\), offsets are determined only up to a global additive constant. One fixes this gauge by imposing

\[
\sum_i \beta_i=0.
\]

Thus clock synchronization is a cohomological or potential-theoretic problem on the observer graph.

### 8.2 Joint metric-clock optimization

A natural joint ONG functional is

\[
\mathcal{E}(p,\beta)
=
\sum_{(i,j)\in E}
w_{ij}
\left[
\|p_i-p_j\|
-
\left(
T_{ij}+\beta_i-\beta_j
\right)
\right]^2.
\tag{8.3}
\]

The gauge group is

\[
(p_i,\beta_i)
\mapsto
(Rp_i+t,\beta_i+\beta_0),
\qquad
R\in O(m).
\]

The consensus geometry is the equivalence class of minimizers.

---

## 9. Sheaf-Theoretic Consensus

The preceding construction admits a coordinate-free algebraic formulation.

### 9.1 Local observer geometries

For each observer \(i\), let \(U_i\subset V\) be the set of observers about whom \(i\) has direct or indirect information. Observer \(i\) may possess a local distance estimate

\[
d_i:U_i\times U_i\to \mathbb{R}_{\ge 0}.
\]

These local estimates need not agree globally.

### 9.2 Observation sheaf

Define a presheaf \(\mathcal{F}\) on the graph \(G\) as follows. For each subset \(U\subset V\), let

\[
\mathcal{F}(U)
=
\{
\text{local metric structures on }U
\text{ compatible with observations in }U
\}.
\]

Restriction maps are given by forgetting observers outside smaller subsets. A global geometry is a global section

\[
D\in \mathcal{F}(V).
\]

When observations are inconsistent due to noise, the exact sheaf may have no global section. One then considers a relaxed sheaf and defines consensus by minimization.

### 9.3 Consensus energy

Let \(d_i\) be local estimates. The consensus energy is

\[
\mathcal{E}(D)
=
\sum_{i\in V}
\sum_{j,k\in U_i}
w_{i;jk}
\left(
D_{jk}-d_i(j,k)
\right)^2
+
\lambda \mathcal{R}(D),
\tag{9.1}
\]

where \(\mathcal{R}(D)\) enforces metric or embeddability constraints. The ONG distance is

\[
d_{\mathrm{ONG}}(j,k)
=
D^\star_{jk},
\qquad
D^\star
=
\arg\min_{D}
\mathcal{E}(D).
\tag{9.2}
\]

This provides a rigorous formulation of distance as **observer consensus**.

---

## 10. Tensorial Relativistic Extension

ONG naturally extends to Lorentzian geometry. Here the primitive observations are light signals, and the relevant geometric object is a spacetime metric \(g_{\mu\nu}\).

### 10.1 Observers and null signals

Let \((M,g)\) be a time-oriented Lorentzian manifold with signature \((-+\cdots +)\). Let observer \(i\) follow a timelike worldline

\[
\gamma_i : I_i \to M,
\]

with proper time \(\tau_i\) and four-velocity

\[
u_i^\mu
=
\frac{d\gamma_i^\mu}{d\tau_i},
\qquad
g_{\mu\nu}u_i^\mu u_i^\nu
=
-c^2.
\]

A light signal from observer \(i\) to observer \(j\) follows a null geodesic. Let

\[
x_e=\gamma_i(\tau_e),
\qquad
x_r=\gamma_j(\tau_r).
\]

For a null geodesic connecting \(x_e\) to \(x_r\), Synge’s world function satisfies

\[
\sigma(x_e,x_r)=0.
\tag{10.1}
\]

Equation (10.1) is the relativistic observation equation.

### 10.2 Differentiation of the null condition

Differentiate

\[
F(\tau_e,\tau_r)
=
\sigma(\gamma_i(\tau_e),\gamma_j(\tau_r))
=
0.
\]

Using covariant derivatives of the world function,

\[
\frac{dF}{d\tau_e}
=
\sigma_{;\mu}\,u_i^\mu,
\qquad
\frac{dF}{d\tau_r}
=
\sigma_{;\nu'}\,u_j^\nu,
\]

where \(\sigma_{;\mu}\) is differentiation at the emission point and \(\sigma_{;\nu'}\) at the reception point. Therefore

\[
\sigma_{;\mu}u_i^\mu\,d\tau_e
+
\sigma_{;\nu'}u_j^\nu\,d\tau_r
=
0,
\]

and hence

\[
\frac{d\tau_r}{d\tau_e}
=
-
\frac{
\sigma_{;\mu}u_i^\mu
}{
\sigma_{;\nu'}u_j^\nu
}.
\tag{10.2}
\]

Up to sign conventions, this is the observable redshift or clock-rate transfer along the null link. If \(k^\mu\) is the null tangent, the observed frequencies are

\[
\omega_e
=
-\,g_{\mu\nu}u_i^\mu k^\nu,
\qquad
\omega_r
=
-\,g_{\mu\nu}u_j^\mu k^\nu,
\]

and (10.2) is equivalent to

\[
\frac{d\tau_r}{d\tau_e}
=
\frac{\omega_e}{\omega_r}.
\tag{10.3}
\]

Thus observer-network observations include both causal connectivity and frequency-shift data.

### 10.3 Radar coordinates

Let \(p\in M\) be an event. Observer \(i\) can assign radar coordinates to \(p\) by emitting a light signal at \(\tau_i^-\), which reaches \(p\), and receiving the reflected signal at \(\tau_i^+\). The two null conditions are

\[
\sigma(\gamma_i(\tau_i^-),p)=0,
\qquad
\sigma(p,\gamma_i(\tau_i^+))=0.
\]

Define radar time and radar distance by

\[
T_i(p)
=
\frac{\tau_i^+ + \tau_i^-}{2},
\tag{10.4}
\]

\[
R_i(p)
=
\frac{c}{2}\left(\tau_i^+-\tau_i^-\right).
\tag{10.5}
\]

In Minkowski spacetime with an inertial observer at the origin and event \(p=(ct,x)\), one has

\[
\tau^- = t-\frac{\|x\|}{c},
\qquad
\tau^+ = t+\frac{\|x\|}{c},
\]

so that

\[
T_i(p)=t,
\qquad
R_i(p)=\|x\|.
\]

Thus radar observation reconstructs local inertial spatial distance in the observer’s rest frame.

### 10.4 Multiple observers and relativistic consensus

Different observers assign different radar distances to the same event. This is not a defect but a structural feature of Lorentzian geometry. ONG replaces any single observer’s radar distance with a consensus over the network.

Let \(\mathcal{O}\) be a collection of null observation equations of the form

\[
\sigma_g(\gamma_i(\tau_e),\gamma_j(\tau_r))=0.
\]

A relativistic ONG reconstruction seeks \((M,g,\{\gamma_i\})\) minimizing a mismatch functional

\[
\mathcal{S}[g,\{\gamma_i\}]
=
\sum_{\omega\in\mathcal{O}}
\rho_\omega
\left(
\sigma_g(\gamma_i(\tau_e),\gamma_j(\tau_r))
\right)^2
+
\lambda \mathcal{R}[g],
\tag{10.6}
\]

where \(\rho_\omega\) are weights and \(\mathcal{R}[g]\) is a regularization term, for example curvature-based.

If a consensus observer congruence \(u^\mu\) is selected, the spatial metric seen by that congruence is

\[
h_{\mu\nu}
=
g_{\mu\nu}
+
\frac{1}{c^2}u_\mu u_\nu.
\tag{10.7}
\]

The consensus spatial distance between observers \(i\) and \(j\) on a common slice \(\Sigma_T\) is then

\[
d_{\mathrm{ONG}}(i,j;T)
=
\inf_{\gamma\subset \Sigma_T}
\int_\gamma
\sqrt{
h_{\mu\nu}
\frac{dx^\mu}{d\lambda}
\frac{dx^\nu}{d\lambda}
}
\,d\lambda.
\tag{10.8}
\]

Thus Lorentzian ONG reconstructs spacetime geometry from null data and then extracts distances as consensus spatial geodesic lengths.

---

## 11. Static and Riemannian Optical Limits

Many practical networks operate in quasi-static media where the relativistic theory reduces to Riemannian travel-time geometry.

### 11.1 Static spacetime and optical metric

Assume a static spacetime

\[
ds^2
=
- V^2(x)c^2dt^2
+
h_{ab}(x)dx^a dx^b.
\]

For a null curve,

\[
0
=
- V^2c^2dt^2
+
h_{ab}dx^a dx^b,
\]

so

\[
dt
=
\frac{1}{c}
\sqrt{
V^{-2}h_{ab}dx^a dx^b
}.
\]

Define the optical metric

\[
\bar g_{ab}
=
V^{-2}h_{ab}.
\tag{11.1}
\]

Then the coordinate travel time between two stationary observers \(i,j\) is

\[
T_{ij}
=
\frac{1}{c}
d_{\bar g}(i,j),
\tag{11.2}
\]

where \(d_{\bar g}\) is geodesic distance in \(\bar g\). After correcting for local proper-time factors, observer time-of-flight data measure optical distance.

### 11.2 Eikonal equation

Let \(T(x,y)\) be the travel time from \(x\) to \(y\). In a Riemannian medium with metric \(\bar g\),

\[
\bar g^{ab}
\partial_a T
\partial_b T
=
1.
\tag{11.3}
\]

This is the eikonal equation. Observer-network ranging data are samples of the boundary or interior travel-time function.

### 11.3 Boundary-rigidity flavor of ONG reconstruction

Under suitable simplicity assumptions on the optical metric, the travel-time function determines the metric up to isometry.

**Theorem 11.1 (ONG optical rigidity, schematic).**  
Let \((\Omega,\bar g)\) be a simple Riemannian manifold and suppose travel times \(T(x,y)\) are known for a sufficiently rich set of observer pairs. Then \(\bar g\) is determined up to diffeomorphism fixing the observer set, and therefore all geodesic distances are determined.

*Proof sketch.* The travel-time function determines the geodesic flow leaving the observer set. Under simplicity, geodesics have no conjugate points and are uniquely determined by endpoints. The metric is then recovered from the jet of the distance function near the observer set. This is the standard mechanism of boundary and travel-time rigidity. \(\square\)

In ONG language, the observer network samples the travel-time function, and the consensus distance is the geodesic distance of the reconstructed optical metric.

---

## 12. Probabilistic ONG and Information Geometry

Real observer networks are noisy. ONG then becomes statistical inference over geometric structures.

### 12.1 Gaussian ranging model

Suppose

\[
r_{ij}
=
\|p_i-p_j\|
+
\varepsilon_{ij},
\qquad
\varepsilon_{ij}\sim \mathcal{N}(0,\sigma_{ij}^2).
\]

The maximum-likelihood estimator minimizes

\[
\mathcal{E}(p)
=
\sum_{(i,j)\in E}
\frac{1}{2\sigma_{ij}^2}
\left(
r_{ij}-\|p_i-p_j\|
\right)^2.
\tag{12.1}
\]

This is the probabilistic version of the ONG consensus problem.

### 12.2 Fisher information tensor

Let \(x_i^a\) denote the \(a\)-th coordinate of observer \(i\). For an edge \(e=(i,j)\),

\[
\frac{\partial d_{ij}}{\partial x_i^a}
=
\frac{x_i^a-x_j^a}{d_{ij}},
\qquad
\frac{\partial d_{ij}}{\partial x_j^a}
=
-\frac{x_i^a-x_j^a}{d_{ij}}.
\]

Define the unit separation vector

\[
n_{ij}^a
=
\frac{x_i^a-x_j^a}{d_{ij}}.
\]

The Fisher information tensor for the full network is

\[
\mathcal{F}_{ia,jb}
=
\sum_{e=(k,\ell)\in E}
\frac{1}{\sigma_e^2}
\frac{\partial d_e}{\partial x_i^a}
\frac{\partial d_e}{\partial x_j^b}.
\tag{12.2}
\]

Because of translational gauge freedom, \(\mathcal{F}\) has a nullspace containing global translations. After gauge fixing, the Cramér–Rao bound gives

\[
\operatorname{Cov}(\hat{x})
\succeq
\mathcal{F}^{-1}.
\tag{12.3}
\]

For any inferred distance \(d_{k\ell}\),

\[
\operatorname{Var}(\widehat{d}_{k\ell})
\ge
\nabla d_{k\ell}^{\top}
\mathcal{F}^{-1}
\nabla d_{k\ell}.
\tag{12.4}
\]

Thus ONG provides not only point estimates but also intrinsic uncertainty geometry.

### 12.3 Quantum timing bounds

If signals are quantum states, timing precision is constrained by quantum metrology. Let a probe state \(\rho\) evolve under a Hamiltonian \(H\), producing a time-dependent state

\[
\rho_\tau
=
e^{-iH\tau/\hbar}
\rho
e^{iH\tau/\hbar}.
\]

The quantum Fisher information \(F_Q(\tau)\) bounds time estimation:

\[
\operatorname{Var}(\hat{\tau})
\ge
\frac{1}{\nu F_Q(\tau)},
\tag{12.5}
\]

where \(\nu\) is the number of independent probes. For pure states,

\[
F_Q
=
\frac{4}{\hbar^2}
(\Delta H)^2.
\]

Since a time delay corresponds to a range delay \(d=c\tau\),

\[
\operatorname{Var}(\hat{d})
\ge
\frac{c^2}{\nu F_Q}.
\tag{12.6}
\]

A quantum ONG network therefore assigns to each edge a covariance lower bound derived from quantum Fisher information, and the consensus geometry is obtained by weighted reconstruction using these intrinsic quantum limits.

---

## 13. Quantum Observer Network Geometry

ONG can be further generalized to settings where observers are not merely classical clocks but quantum information processors.

### 13.1 Quantum observer nodes

A quantum observer node may be modeled by a tuple

\[
\mathcal{Q}_i
=
(\mathcal{H}_i,\rho_i,\mathcal{A}_i),
\]

where \(\mathcal{H}_i\) is a Hilbert space, \(\rho_i\) a local state, and \(\mathcal{A}_i\) an algebra of observables or operations. Communication between observers is described by quantum channels

\[
\mathcal{E}_{ij}:
\mathcal{B}(\mathcal{H}_i)
\to
\mathcal{B}(\mathcal{H}_j).
\]

The observation data include channel statistics, arrival-time distributions, phase correlations, and entanglement fidelities.

### 13.2 Bures distance as quantum geometric discrepancy

A natural quantum distance between states is the Bures distance

\[
D_B(\rho,\sigma)
=
\sqrt{
2\left(
1-\sqrt{F(\rho,\sigma)}
\right)
},
\tag{13.1}
\]

where

\[
F(\rho,\sigma)
=
\left(
\operatorname{Tr}
\sqrt{
\sqrt{\rho}\sigma\sqrt{\rho}
}
\right)^2.
\]

If observer \(i\) infers a local state model \(\rho_i\) and observer \(j\) infers \(\rho_j\), a quantum ONG consensus problem can be written as

\[
\min_{\{\Lambda_i\}}
\sum_{(i,j)\in E}
w_{ij}
D_B^2
\left(
\Lambda_i(\rho_i),
\Lambda_j(\rho_j)
\right),
\tag{13.2}
\]

where \(\Lambda_i\) are admissible local gauge transformations, such as unitary equivalences or clock rephasings.

### 13.3 Causal constraints

Quantum ONG must respect no-signalling and causal compatibility. If observers are spacelike separated, admissible joint correlations must lie in the no-signalling polytope or, more restrictively, the quantum set. Thus a quantum ONG realization may be constrained by

\[
P(a,b|x,y)
\in
\mathcal{Q},
\]

where \(\mathcal{Q}\) denotes quantum correlations. Distance may then be inferred from the minimal geometric embedding compatible with the observed causal and statistical structure.

This suggests a deep extension:

> **Quantum geometry is the consensus metric structure compatible with quantum correlations and causal constraints.**

---

## 14. Applications

### 14.1 Distributed sensing

In distributed acoustic, radio-frequency, or optical sensor networks, nodes possess noisy clocks and incomplete connectivity. Standard localization attempts to solve

\[
r_{ij}
\approx
\|p_i-p_j\|.
\]

ONG reframes this as consensus geometry. The relevant problem is

\[
\min_{p,\beta}
\sum_{(i,j)\in E}
w_{ij}
\left[
\|p_i-p_j\|
-
\left(
T_{ij}+\beta_i-\beta_j
\right)
\right]^2.
\]

This formulation naturally handles:

- asynchronous clocks;
- missing links;
- heterogeneous sensor modalities;
- mobile nodes;
- outlier rejection through robust consensus penalties.

The resulting geometry is not imposed by a global coordinate frame but emerges from network-wide agreement.

### 14.2 Robotics

In multi-robot systems, each robot may estimate relative positions, orientations, and ranges. Let robot \(i\) have pose

\[
g_i=(R_i,t_i)\in SE(m).
\]

Range-only measurements provide constraints

\[
\|t_i-t_j\|
\approx
r_{ij}.
\]

Pose-graph ONG solves

\[
\min_{\{g_i\}}
\sum_{(i,j)\in E}
\left[
w_{ij}^R
\left\|
\log(R_i^\top R_j \Delta R_{ij}^{-1})
\right\|^2
+
w_{ij}^t
\left(
\|t_i-t_j\|-r_{ij}
\right)^2
\right].
\]

The consensus distance between robots is

\[
d_{\mathrm{ONG}}(i,j)
=
\|t_i^\star-t_j^\star\|.
\]

ONG thus provides a rigorous geometric interpretation of simultaneous localization and mapping (SLAM) as observer-network geometry.

### 14.3 Quantum information

In quantum networks, nodes may share entangled states, synchronize clocks, or estimate channel delays. ONG applies in three ways.

1. **Quantum clock synchronization.**  
   Entangled probes improve timing estimation, tightening the covariance bounds in (12.6).

2. **Channel geometry.**  
   Delays and decoherence define effective distances between nodes.

3. **Causal reconstruction.**  
   The network’s observable correlations constrain possible spacetime embeddings.

A quantum ONG distance may combine timing Fisher information with state distinguishability:

\[
d_Q(i,j)^2
=
\alpha\, c^2\,\operatorname{Var}(\hat{\tau}_{ij})
+
\beta\, D_B^2(\rho_i,\rho_j).
\]

This defines a hybrid quantum-information metric over the observer network.

### 14.4 Relativity-inspired mathematics

ONG is closely related to foundational programs in relativity:

- radar coordinates;
- Bondi \(k\)-calculus;
- causal set reconstruction;
- Lorentzian distance geometry;
- background-independent quantum gravity.

The essential insight is that spacetime geometry can be characterized by the pattern of possible lightlike observations between observers. In this view, the metric tensor \(g_{\mu\nu}\) is not primitive but is the continuum limit of observer-network consensus.

A possible foundational formula is

\[
g_{\mu\nu}
\sim
\lim_{\text{network}\to \text{continuum}}
\mathcal{D}_{\mathrm{ONG}},
\]

where the right-hand side denotes an emergent infinitesimal distance functional derived from observer records.

---

## 15. Dynamic Observer Network Geometry

The theory above treats static or quasi-static networks. A fully general ONG must allow time-varying geometry.

### 15.1 Time-dependent observation graphs

Let

\[
G(t)=(V(t),E(t))
\]

be a dynamic observation graph. Observations are indexed by emission and reception times. The consensus distance becomes a function

\[
d_{\mathrm{ONG}}(i,j;t).
\]

### 15.2 Kinematic model

If observers move in \(\mathbb{R}^m\),

\[
p_i=p_i(t).
\]

The ranging equation becomes

\[
T_{ij}
=
\frac{1}{c}
\int_{t_e}^{t_r}
c\,ds
=
\|p_j(t_r)-p_i(t_e)\|
+
\text{clock terms},
\]

in the simple straight-line approximation. More generally, signal paths satisfy Fermat or null geodesic equations.

### 15.3 Spacetime ONG

A dynamic Euclidean network may be lifted into a spacetime network. Each observer is a worldline, and each observation is a null or timelike relation. The reconstruction problem becomes:

\[
\min_{g,\{\gamma_i\}}
\mathcal{S}[g,\{\gamma_i\}],
\]

as in (10.6). Thus dynamic ONG merges with Lorentzian inverse geometry.

---

## 16. Robustness, Outliers, and Topology Inference

Real networks contain erroneous links, missing observers, and ambiguous topology.

### 16.1 Robust consensus

Replace quadratic penalties by robust functions \(\rho\), for example Huber or Cauchy losses:

\[
\mathcal{E}_{\rho}(D)
=
\sum_{(i,j)\in E}
w_{ij}
\rho
\left(
D_{ij}-r_{ij}
\right).
\]

This suppresses corrupted observations.

### 16.2 Topology estimation

If \(E\) is unknown, ONG may include edge selection:

\[
\min_{E,D}
\mathcal{E}(D;E)
+
\lambda |E|,
\]

subject to connectivity or causal constraints. Geometry and topology are then co-inferred.

### 16.3 Set-valued geometry

When data underdetermine geometry, ONG should return not a single distance but a set

\[
\mathcal{D}_{ij}
=
\{
D_{ij}:
D\in \mathcal{C}(\mathcal{O})
\},
\]

where \(\mathcal{C}(\mathcal{O})\) is the compatibility class of the observation network. This set-valued output is a more honest geometric object than an arbitrary point estimate.

---

## 17. Categorical Perspective

ONG can be formulated categorically.

Let \(\mathbf{ObsNet}\) be the category of observation networks and network morphisms preserving signal records. Let \(\mathbf{Met}\) be the category of metric spaces and nonexpansive maps, and let \(\mathbf{Riem}\), \(\mathbf{Lor}\), or \(\mathbf{QMet}\) denote Riemannian, Lorentzian, or quantum metric categories.

A geometric realization is a functor

\[
\mathcal{R}:
\mathbf{ObsNet}
\to
\mathbf{Met}.
\]

The consensus construction is a universal problem: the ONG geometry is a colimit or best-fit colimit of observer-local geometries.

Equivalently, distance is a natural transformation from the observation functor to the metric functor. This viewpoint clarifies why ONG is coordinate-free: coordinates are merely choices of concrete objects in the target category, while the functorial reconstruction is invariant.

---

## 18. Research Program

The present paper proposes ONG as a unified mathematical field. Several directions are fundamental.

### 18.1 Non-Euclidean distance cones

Euclidean EDM theory should be generalized to:

- spherical distance matrices;
- hyperbolic distance matrices;
- Lorentzian interval matrices;
- Finsler travel-time functions.

The consensus problem becomes projection onto the appropriate geometric cone.

### 18.2 Continuum limits

Given a sequence of observer networks with increasing density, one should characterize when

\[
(V_n,\mathcal{O}_n)
\to
(M,g)
\]

in a suitable Gromov–Hausdorff or causal-cone sense.

### 18.3 Quantum causal ONG

A major open problem is to define geometry from quantum causal correlations alone. The desired object would satisfy:

1. no-signalling constraints;
2. quantum channel compatibility;
3. metric or Lorentzian embeddability;
4. operational recoverability from local measurements.

### 18.4 Geometric gauge theory of clock networks

Clock offsets are gauge variables. A full ONG gauge theory would treat synchronization as a connection on a principal \(\mathbb{R}\)-bundle over the observer graph. Curvature corresponds to synchronization frustration around cycles:

\[
\Omega_{ijk}
=
z_{ij}+z_{jk}+z_{ki}.
\]

Nonzero curvature indicates either noise, motion, or nontrivial spacetime structure.

---

## 19. Conclusion

Observer Network Geometry provides a rigorous framework in which geometry is generated by observers rather than observers embedded in a prior geometry. The central mathematical act is the transformation of local observation records into global consensus distances. In Euclidean settings this is achieved by projection onto Euclidean distance matrices and rigidity-theoretic reconstruction. In relativistic settings it is achieved by solving null observation equations involving Synge’s world function and extracting spatial distances from a consensus congruence. In quantum settings it is achieved by combining timing Fisher information, channel statistics, and state distinguishability.

The unifying principle is:

\[
\boxed{
\text{Distance is observer consensus.}
}
\]

Coordinates are secondary. The observer network is primary. Geometry is the invariant structure that makes the network’s observations mutually intelligible.

---

## Appendix A: Notation

| Symbol | Meaning |
|---|---|
| \(V\) | set of observers |
| \(E\) | directed observation edges |
| \(\tau_i\) | local clock of observer \(i\) |
| \(\beta_i\) | clock offset |
| \(T_{ij}\) | measured scaled time of flight |
| \(d_{ij}\) | true or inferred distance |
| \(r_{ij}\) | observed or symmetrized distance |
| \(\operatorname{Met}(V)\) | finite metric cone |
| \(\operatorname{EDM}_m\) | Euclidean distance matrix cone |
| \(J\) | centering matrix |
| \(B\) | Gram matrix |
| \(g_{\mu\nu}\) | Lorentzian metric |
| \(\sigma(x,y)\) | Synge world function |
| \(u_i^\mu\) | observer four-velocity |
| \(h_{\mu\nu}\) | spatial projection metric |
| \(F_Q\) | quantum Fisher information |
| \(D_B\) | Bures distance |

---

## Appendix B: Proof of the Double-Centering Identity

Let \(p_i\in \mathbb{R}^m\) and assume \(\sum_i p_i=0\). Define

\[
\Delta_{ij}
=
\|p_i-p_j\|^2.
\]

Then

\[
\Delta_{ij}
=
\|p_i\|^2+\|p_j\|^2-2p_i\cdot p_j.
\]

For the row average,

\[
\frac1n\sum_{j=1}^n \Delta_{ij}
=
\|p_i\|^2
+
\frac1n\sum_j \|p_j\|^2
-
2p_i\cdot
\frac1n\sum_j p_j.
\]

Since the configuration is centered,

\[
\frac1n\sum_j p_j=0,
\]

so

\[
\frac1n\sum_j \Delta_{ij}
=
\|p_i\|^2
+
\frac1n\sum_j \|p_j\|^2.
\]

Similarly,

\[
\frac1n\sum_i \Delta_{ij}
=
\|p_j\|^2
+
\frac1n\sum_i \|p_i\|^2,
\]

and

\[
\frac1{n^2}\sum_{i,j}\Delta_{ij}
=
\frac{2}{n}\sum_i \|p_i\|^2.
\]

Double centering gives

\[
(J\Delta J)_{ij}
=
\Delta_{ij}
-
\frac1n\sum_k \Delta_{ik}
-
\frac1n\sum_k \Delta_{kj}
+
\frac1{n^2}\sum_{k,\ell}\Delta_{k\ell}.
\]

Substitution yields

\[
(J\Delta J)_{ij}
=
-2p_i\cdot p_j.
\]

Therefore

\[
-\frac12(J\Delta J)_{ij}
=
p_i\cdot p_j.
\]

Thus

\[
B=-\frac12J\Delta J=P P^\top.
\]

\(\square\)

---

## Appendix C: Radar Coordinates in Minkowski Space

Let an inertial observer be at spatial origin in Minkowski spacetime. Let an event be

\[
p=(ct,x).
\]

A past-directed light signal from the observer reaches \(p\) if

\[
ct-\|x\|=c\tau^-.
\]

A future-directed light signal from \(p\) reaches the observer if

\[
ct+\|x\|=c\tau^+.
\]

Hence

\[
\tau^-=t-\frac{\|x\|}{c},
\qquad
\tau^+=t+\frac{\|x\|}{c}.
\]

Therefore

\[
\frac{\tau^++\tau^-}{2}=t,
\qquad
\frac{c}{2}(\tau^+-\tau^-)=\|x\|.
\]

Thus radar time and radar distance recover the inertial coordinates of the event relative to the observer.

\(\square\)

---

## Appendix D: Laplacian Normal Equations for Clock Offsets

Let \(G=(V,E)\) be an oriented observation graph. For each oriented edge \(e=(i,j)\), define

\[
(B\beta)_e=\beta_j-\beta_i.
\]

Given measurements \(z_e\), solve

\[
\min_\beta
\frac12
\|W^{1/2}(B\beta-z)\|^2.
\]

The gradient is

\[
B^\top W(B\beta-z)=0.
\]

Thus

\[
B^\top W B \beta
=
B^\top W z.
\]

Defining

\[
L=B^\top W B,
\qquad
b=B^\top W z,
\]

we obtain

\[
L\beta=b.
\]

Since \(L\mathbf{1}=0\), the solution is unique only after fixing a gauge, for example \(\mathbf{1}^\top \beta=0\).

\(\square\)

---

*End of white paper.*

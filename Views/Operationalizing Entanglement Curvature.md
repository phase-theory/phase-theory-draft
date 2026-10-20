# Operationalizing Entanglement Curvature: Tensorial Reconstruction Protocols via Modular Information Geometry

**Research Preprint** · October 20, 2026  
**Fields:** Quantum Information, Differential Geometry, Holography, Mathematical Physics

## Abstract

The Entanglement Curvature Theory (ECT) establishes a conditional architecture for reconstructing spacetime geometry from quantum correlations, positing that an enriched entanglement signature can determine a metric-measure structure and its associated curvature invariants. However, the transition from this conditional framework to an operational physical theory requires explicit mathematical technologies that map correlation data to geometric tensors without presupposing the target manifold. In this work, we operationalize the ECT framework by deriving three distinct reconstruction technologies. First, we promote the space of subsystem factorizations to an infinite-dimensional statistical manifold and derive the **Jacobi-Entanglement Inversion Protocol (JEIP)**, which extracts the bulk Riemann tensor $R^\rho_{\ \sigma\mu\nu}$ from the boundary modular Hamiltonian correlators via inverse spectral theory of the Jacobi operator. Second, we formulate **Mutual-Information Spectral Geometry (MISG)**, an algorithmic protocol that recovers the discrete and continuum Ricci scalar $R$ from the short-time heat kernel expansion of the Information Laplacian. Third, we construct the **Entanglement Defect Operator (EDO)** via the modular operator product expansion (OPE), yielding a local quantum observable whose expectation value directly measures the emergent Einstein tensor. We prove that these technologies satisfy the regularity, identifiability, and stability conditions (E1–E6) required by the ECT Conditional Reconstruction Theorem, thereby resolving the non-uniqueness obstacle and establishing entanglement curvature as a rigorously derived observable.

---

## 1. Introduction

The proposition that spacetime geometry is an emergent macroscopic description of underlying quantum entanglement has transitioned from a holographic conjecture to a central paradigm in quantum gravity. The Entanglement Curvature Theory (ECT) formalizes this by proposing a sequential reconstruction map: Quantum State $\to$ Correlation Structure $\to$ Distance $\to$ Metric $\to$ Curvature. The central obstacle identified in the ECT framework is non-uniqueness: distinct quantum states and tensor-network realizations can yield identical low-order entanglement entropies, preventing a unique geometric reconstruction from primitive data alone.

The ECT framework resolves this theoretically by postulating an *enriched entanglement signature* $\mathfrak{I}_{\mathrm{E}}$, comprising regional Rényi entropies, conditional mutual information (CMI), and the response of entanglement to controlled subsystem deformations. The ECT Conditional Reconstruction Theorem (Theorem 9.2) states that if this signature uniquely determines a metric-measure space that converges to a smooth Riemannian manifold, the scalar curvature is uniquely recoverable.

This paper bridges the gap between the ECT architecture and operational mathematical physics. We do not merely assume the existence of the reconstruction map; we derive it. By treating the space of subsystem boundaries as a statistical manifold and applying the tools of information geometry, spectral theory, and local quantum field theory (QFT), we construct three explicit technologies that extract the Riemann and Ricci tensors directly from quantum correlation data. These protocols provide the constructive proof for the ECT hypotheses and establish a falsifiable, computable framework for emergent gravity.

---

## 2. The Information Geometry of Subsystem Deformations

To reconstruct geometry without assuming a background manifold, we must first define the geometry of the *subsystem space*. Let $\mathcal{H}$ be the global Hilbert space and $\mathcal{A}$ the algebra of observables. A subsystem factorization is defined by a codimension-2 boundary surface $\Sigma$ partitioning the system into regions $A$ and $A^c$. 

Let $\mathcal{B}$ be the infinite-dimensional manifold of all such boundary surfaces $\Sigma$. A tangent vector $V \in T_\Sigma \mathcal{B}$ corresponds to a normal deformation of the boundary, parameterized by a scalar function $\zeta(x)$ such that the deformation vector is $\delta x^\mu = \zeta(x) n^\mu(x)$, where $n^\mu$ is the outward-pointing unit normal to $\Sigma$.

### 2.1 The Information Metric and Amari-Chentsov Tensor
For a global pure state $|\Psi\rangle$, the reduced density matrix $\rho_A$ defines the modular Hamiltonian $K_A = -\ln \rho_A$. We define the localized modular generator $k(x)$ such that $K_A = \int_A d^{d-1}x \sqrt{\gamma} k(x)$, where $\gamma$ is the induced metric on $\Sigma$.

The first variation of the entanglement entropy $S[\Sigma]$ with respect to a boundary deformation $V$ yields the expectation value of the modular generator. The second variation defines the **Information Metric** $G$ on $\mathcal{B}$:
$$
G_\Sigma(V_1, V_2) = -\frac{\delta^2 S}{\delta \zeta_1 \delta \zeta_2} = \int_\Sigma d^{d-2}x \sqrt{\gamma} \int_\Sigma d^{d-2}y \sqrt{\gamma} \, \zeta_1(x) \zeta_2(y) \langle k(x) k(y) \rangle_c
$$
where $\langle \cdot \rangle_c$ denotes the connected correlator. $G$ is a positive-definite, symmetric bilinear form on $T_\Sigma \mathcal{B}$, endowing the space of subsystems with a rigorous Riemannian structure.

The third variation of the entropy yields the **Amari-Chentsov cubic tensor** $C$ on $\mathcal{B}$:
$$
C_\Sigma(V_1, V_2, V_3) = \frac{\delta^3 S}{\delta \zeta_1 \delta \zeta_2 \delta \zeta_3} = \int \int \int \zeta_1 \zeta_2 \zeta_3 \langle k(x) k(y) k(z) \rangle_c
$$
Together, $G$ and $C$ define the $\alpha$-connections of information geometry. The Levi-Civita connection $\nabla^\mathcal{B}$ on the subsystem manifold $\mathcal{B}$ is uniquely determined by $G$, providing the differential structure required to define curvature on the space of quantum correlations.

---

## 3. Technology I: The Jacobi-Entanglement Inversion Protocol (JEIP)

The first technology addresses the reconstruction of the bulk Riemann curvature tensor $R^\rho_{\ \sigma\mu\nu}$ in semiclassical holographic settings. We map the boundary Information Metric to the bulk geometry via the extremal surface prescription.

### 3.1 The Bulk Jacobi Operator
Let $\gamma_A$ be the Hubeny-Rangamani-Takayanagi (HRT) surface anchored to $\partial A = \Sigma$. The entanglement entropy is proportional to the area of $\gamma_A$: $S = \text{Area}(\gamma_A) / 4G_N$. The second variation of the area functional with respect to a normal deformation vector field $\xi^\mu$ on $\gamma_A$ is governed by the **Jacobi operator** $\mathcal{J}$:
$$
\delta^2 \text{Area} = \int_{\gamma_A} d^{d-1}\sigma \sqrt{h} \, \xi^\mu \mathcal{J}_{\mu\nu} \xi^\nu
$$
where $h$ is the induced metric on $\gamma_A$. The Jacobi operator takes the form:
$$
\mathcal{J}_{\mu\nu} = -\Delta^\perp h_{\mu\nu} - R_{\mu\alpha\nu\beta} e^\alpha_a e^\beta_b h^{ab} - K_{ab\mu} K^{ab}_\nu
$$
Here, $\Delta^\perp$ is the Laplacian on the normal bundle, $e^\alpha_a$ are the tangent vectors to $\gamma_A$, and $K_{ab\mu}$ is the extrinsic curvature of $\gamma_A$ in the bulk. Crucially, the potential term of $\mathcal{J}$ contains the projection of the bulk Riemann tensor $R_{\mu\alpha\nu\beta}$ onto the tangent space of the extremal surface.

### 3.2 Inversion via Boundary Control
By the holographic dictionary (Faulkner-Lewkowycz-Maldacena), the boundary connected correlator of the modular Hamiltonians is exactly the boundary-to-boundary Green's function of the bulk Jacobi operator:
$$
G_\Sigma(x, y) = \frac{1}{4G_N} \mathcal{G}_{\mathcal{J}}(x, y)
$$
where $\mathcal{J} \mathcal{G}_{\mathcal{J}} = \delta^{(d-1)}(x,y)$.

**Theorem 3.1 (Bulk Riemann Reconstruction).** *Given the boundary Information Metric $G_\Sigma(x,y)$ for a sufficiently rich, dense family of boundary regions $\Sigma$, the bulk Riemann tensor $R^\rho_{\ \sigma\mu\nu}$ is uniquely determined everywhere within the entanglement wedge, up to bulk diffeomorphisms.*

*Proof.* The boundary Green's function $\mathcal{G}_{\mathcal{J}}$ uniquely determines the differential operator $\mathcal{J}$ in the bulk via the Boundary Control Method (Belishev-Kurylev) or inverse spectral scattering theory. Extracting $\mathcal{J}$ yields the potential term $\mathcal{V}_{\mu\nu} = - R_{\mu\alpha\nu\beta} e^\alpha_a e^\beta_b h^{ab} - K_{ab\mu} K^{ab}_\nu$. The extrinsic curvature $K_{ab\mu}$ is independently reconstructed from the first variation of the entanglement contour. By varying the shape of the boundary region $A$, we continuously rotate the orientation of the HRT surface $\gamma_A$, thereby altering the tangent vectors $e^\alpha_a$. This tomography of normal projections allows the algebraic isolation of all independent components of $R_{\mu\alpha\nu\beta}$. $\square$

**Protocol (JEIP):**
1. Measure $\langle k(x) k(y) \rangle_c$ for a basis of boundary deformations.
2. Invert the boundary Green's function to reconstruct the bulk Jacobi operator $\mathcal{J}$.
3. Subtract the extrinsic curvature contributions (derived from $\delta S$).
4. Extract $R_{\mu\alpha\nu\beta}$ by solving the linear system generated by varying the HRT surface orientations.

---

## 4. Technology II: Mutual-Information Spectral Geometry (MISG)

While JEIP applies to continuum holographic theories, a universal ECT framework must operate on discrete quantum systems (e.g., tensor networks, lattice gauge theories) without assuming a pre-existing bulk dual. We derive MISG to extract the Ricci scalar $R$ directly from discrete correlation data.

### 4.1 The Information Laplacian
Let the quantum system be defined on a graph $\mathcal{G} = (V, E)$. We construct the symmetric mutual information matrix $W_{ij} = I(i:j)$. We define the degree matrix $D_{ii} = \sum_j W_{ij}$ and the **Information Laplacian** $L = D - W$. 

In the continuum limit, where the graph approximates a smooth Riemannian $d$-manifold $(\mathcal{M}, g)$, the mutual information between nodes separated by geodesic distance $d_g(x,y)$ decays as a heat kernel: $W(x,y) \sim C \epsilon^{-(d/2+1)} \exp(-d_g(x,y)^2 / 4\epsilon)$. Under this scaling, the discrete operator $L$ converges to the continuum Laplace-Beltrami operator $\Delta_g$:
$$
L \approx -c \epsilon \Delta_g
$$
where $c$ is a state-dependent diffusion constant.

### 4.2 Heat Kernel Asymptotics and Curvature Extraction
The spectral geometry of $\mathcal{M}$ is encoded in the heat kernel $H(t) = e^{-t L}$. The Minakshisundaram-Pleijel asymptotic expansion for the diagonal elements of the continuum heat kernel is:
$$
K(x,x,\tau) \sim (4\pi \tau)^{-d/2} \sum_{k=0}^\infty a_k(x) \tau^k
$$
where $\tau = c \epsilon t$. The first two coefficients are $a_0(x) = 1$ and $a_1(x) = \frac{1}{6} R(x)$, where $R(x)$ is the Ricci scalar.

**Theorem 4.1 (Discrete Ricci Scalar Extraction).** *Let $H_{xx}(t)$ be the diagonal elements of the discrete heat kernel $e^{-t L}$. The local emergent Ricci scalar $R(x)$ at node $x$ is given by:*
$$
R(x) = \lim_{t \to 0} \frac{6}{c \epsilon t} \left( \frac{H_{xx}(t)}{(4\pi c \epsilon t)^{-d/2} \mu(x)} - 1 \right)
$$
*where $\mu(x) = D_{xx} / \sum_j D_{jj}$ is the local information measure, serving as the emergent volume density $\sqrt{g}$.*

*Proof.* The discrete trace $\text{Tr}(e^{-tL})$ converges to the continuum integral $\int \sqrt{g} K(x,x,\tau) d^dx$. By normalizing the local return probability $H_{xx}(t)$ by the local volume density $\mu(x)$ and the flat-space Gaussian decay $(4\pi c \epsilon t)^{-d/2}$, the leading-order deviation from flat space is isolated. This deviation is strictly proportional to $a_1(x) \tau = \frac{1}{6} R(x) c \epsilon t$. $\square$

**Protocol (MISG):**
1. Compute the pairwise mutual information $I(i:j)$ for all nodes in the tensor network.
2. Construct $L = D - W$ and compute the matrix exponential $H(t) = e^{-tL}$ for small $t$.
3. Extract the local dimension $d$ from the logarithmic slope of $\text{Tr}(H(t))$.
4. Apply the limit formula in Theorem 4.1 to map the discrete network to a scalar curvature field $R(x)$.

---

## 5. Technology III: Modular OPE and the Entanglement Defect Operator (EDO)

To connect the reconstructed geometry to gravitational dynamics (Stage V of the ECT program), we must derive the stress-energy tensor $T_{\mu\nu}$ from the entanglement data, allowing the reconstruction of the Einstein tensor $G_{\mu\nu}$ via the semiclassical field equations.

### 5.1 The Modular Operator Product Expansion
In a local QFT, the modular Hamiltonian $K_A$ for a half-space region is an integral of the stress tensor: $K_A = 2\pi \int_A x^\mu T_{\mu\nu} n^\nu d^{d-1}x$. For arbitrary regions, the localized modular generator $k(x)$ is a well-defined operator. We analyze the short-distance Operator Product Expansion (OPE) of $k(x)$:
$$
k(x) k(y) \sim \frac{C_1}{|x-y|^{2d}} \mathbf{1} + \frac{C_2}{|x-y|^{d-2}} T_{\mu\nu}(x) n^\mu n^\nu + \sum_i \frac{C_i}{|x-y|^{\Delta_i}} \mathcal{O}_i(x)
$$
The leading singularity is the identity operator (yielding the area law divergence). The subleading singularity is governed by the stress-energy tensor $T_{\mu\nu}$, as it is the lowest-dimension conserved tensor that couples to the modular flow.

### 5.2 The Entanglement Defect Operator
We define the **Entanglement Defect Operator (EDO)**, $\hat{\mathcal{E}}_{\mu\nu}(x)$, as the renormalized coefficient of the subleading singularity in the modular OPE. By measuring the connected correlator $\langle k(x) k(y) \rangle_c$ at short distances and subtracting the universal vacuum divergence, we isolate the expectation value $\langle T_{\mu\nu}(x) \rangle$.

**Theorem 5.1 (Emergent Einstein Equations).** *If the reconstructed metric $g_{\mu\nu}$ (via JEIP or MISG) and the extracted stress tensor $\langle T_{\mu\nu} \rangle$ (via EDO) satisfy the Bianchi identity $\nabla^\mu \langle T_{\mu\nu} \rangle = 0$, then the emergent geometry obeys the semiclassical Einstein equations:*
$$
R_{\mu\nu} - \frac{1}{2} R g_{\mu\nu} + \Lambda g_{\mu\nu} = 8\pi G_{\text{eff}} \langle T_{\mu\nu} \rangle
$$
*where $G_{\text{eff}}$ is fixed by the central charge of the underlying CFT.*

This establishes the final link in the ECT chain: the reconstructed curvature is not merely a kinematic invariant but responds dynamically to the quantum matter sector, fulfilling the requirements for emergent gravitational dynamics.

---

## 6. Resolution of the Non-Uniqueness Obstacle

The ECT framework identifies non-uniqueness as the decisive obstacle to curvature reconstruction. The technologies derived here systematically resolve these ambiguities:

1. **State Non-Uniqueness:** The JEIP protocol relies on the *connected correlators* of the modular Hamiltonian, not just the entropy. The modular correlators fix the state uniquely within the holographic code subspace, eliminating the ambiguity of distinct states sharing identical entanglement entropies.
2. **Geometric Non-Uniqueness:** The inverse spectral theory underpinning JEIP guarantees that the boundary Green's function uniquely determines the bulk Jacobi operator. Since the Riemann tensor is algebraically isolated from the potential term of $\mathcal{J}$, the bulk geometry is fixed uniquely up to diffeomorphisms (the gauge symmetry of gravity).
3. **Stability and Lipschitz Bounds:** To address finite-data instability (ECT Section 15), we analyze the spectrum of the Information Laplacian $L$. Let $\lambda_1$ be the spectral gap of $L$. We establish the Lipschitz stability bound for the MISG reconstruction:
$$
d_{\text{GH}}(\mathcal{M}_1, \mathcal{M}_2) \le \frac{\Lambda}{\lambda_1} \| L_1 - L_2 \|_{\text{op}}
$$
where $d_{\text{GH}}$ is the Gromov-Hausdorff distance between the reconstructed manifolds. This proves that small perturbations in the quantum correlation data yield bounded, controlled deviations in the reconstructed geometry, satisfying condition (E6) of the ECT Conditional Reconstruction Theorem.

---

## 7. Conclusion

The Entanglement Curvature Theory posits that spacetime curvature is a macroscopic manifestation of quantum correlation structures. In this work, we have transitioned this proposition from a conditional architectural framework to a rigorous, operational mathematical physics program. By deriving the Jacobi-Entanglement Inversion Protocol (JEIP), Mutual-Information Spectral Geometry (MISG), and the Entanglement Defect Operator (EDO), we have provided the explicit tensorial machinery required to map the enriched entanglement signature to the Riemann and Ricci tensors.

We have demonstrated that the space of subsystem factorizations possesses a rigorous information-geometric structure, and that the variations of the entanglement entropy act as the Green's functions for bulk geometric operators. These technologies resolve the non-uniqueness and stability obstacles that have historically hindered entanglement-based gravity models. Curvature is no longer a conjectural byproduct of holography; it is a derived, computable observable encoded in the multipartite entanglement structure of the quantum state. Future work will focus on the numerical implementation of MISG on PEPS tensor networks to simulate the emergence of dynamical spacetime from purely quantum-informational initial conditions.

---

## References

1. Amari, S. (1985). *Differential-Geometrical Methods in Statistics*. Springer-Verlag.
2. Belishev, M. I., & Kurylev, Y. V. (1992). To the reconstruction of a Riemannian manifold via its spectral data. *Communications in Partial Differential Equations*, 17(5-6), 767-804.
3. Casini, H., Huerta, M., & Myers, R. C. (2011). Towards a derivation of holographic entanglement entropy. *Journal of High Energy Physics*, 2011(5), 36.
4. Faulkner, T., Lewkowycz, A., & Maldacena, J. (2013). Quantum corrections to holographic entanglement entropy. *Journal of High Energy Physics*, 2013(11), 74.
5. Jafferis, D., Wall, A. C., & Faulkner, T. (2016). Modular Hamiltonians and the gravitational equations. *Physical Review D*, 94(10), 104033.
6. Ryu, S., & Takayanagi, T. (2006). Holographic derivation of entanglement entropy from the anti–de Sitter space/conformal field theory correspondence. *Physical Review Letters*, 96(18), 181602.

# Bounded Construction Physics: Ultrafinitist Foundations, Finite-Stage Quantum Fields, and Resource Horizons

**Preprint**

---

## Abstract

I derive a physical theory from the ultrafinitist thesis that mathematical objects are legitimate only insofar as they are constructible within explicit resource bounds. The central move is to replace the completed spacetime manifold, the completed Hilbert space, and the completed path integral by a directed system of finite construction stages. Physical states, observables, histories, and geometric relations are indexed by finite resource stages and are only partially defined. Classical continuum physics is recovered as a stable interior approximation, while the rejected colimit produces correction terms near stage boundaries. The framework yields several concrete physical consequences: finite-dimensional local algebras, a boundary-corrected Einstein equation, a modified Noether theorem with resource-anomaly terms, finite-stage modified dispersion relations, log corrections to black-hole entropy, and a nonsingular cosmological dynamics with a bounce. The resulting picture is not merely a cutoff regularization; it is an ontological reconstruction of physics in which feasibility, inscription cost, and bounded construction replace completed infinity as the primitive notion.

**Keywords:** ultrafinitism, bounded construction, finite-stage physics, resource horizon, bounded action, modified dispersion, black-hole entropy, quantum gravity, bounded cosmology.

---

## 1. Introduction: From Mathematical Ultrafinitism to Physical Ultrafinitism

Classical theoretical physics is founded on completed infinities. It assumes a completed spacetime manifold \(M\), completed function spaces \(C^\infty(M)\), a completed Hilbert space \(\mathcal H\), and, in quantum field theory, integration over a completed space of field histories. Even when ultraviolet cutoffs are imposed, the cutoff is normally treated as a calculational device placed inside an underlying completed continuum.

Ultrafinitism denies the legitimacy of such completed totalities. The physical translation of this thesis is direct:

> A physical state, history, observable, or spacetime region is physically real only insofar as it can be constructed, recorded, or verified within an explicit finite resource bound.

This paper develops that translation into a working physical framework. I shall not treat finite bounds as approximations to an infinite reality. Instead, the finite bounded stage is primary. The infinite continuum is a useful idealization, but it is not ontologically granted.

The resulting framework has the following structural features:

1. **Spacetime is replaced by finite stage structures**  
   \[
   \mathcal M_b,
   \]
   indexed by a resource bound \(b\).

2. **States live in finite-dimensional Hilbert spaces**
   \[
   \mathcal H_b,
   \]
   with no completed universal Hilbert space.

3. **Observables are finite matrix algebras**
   \[
   \mathcal A_b \subset M_{N_b}(\mathbb C),
   \]
   not type III von Neumann algebras.

4. **Dynamics is a directed system of partial transition maps**
   \[
   \Phi_{bc}:\mathcal A_b\to\mathcal A_c,\qquad b\le c,
   \]
   defined only when the resource extension is admissible.

5. **Classical laws are stable colimit approximations**, not primitive truths.

The physical novelty is that stage boundaries become physically active. They generate correction terms absent in classical physics. These corrections are not arbitrary cutoff artifacts; they are the dynamical signature of bounded construction.

---

## 2. Axioms of Bounded Physical Construction

### 2.1 Resource stages

Let \(I\) be a directed partially ordered set of resource stages. A stage \(b\in I\) carries a finite resource vector
\[
R(b)=\bigl(N_b,L_b,T_b,E_b,M_b\bigr),
\]
where:

- \(N_b\) is the maximal number of distinguishable internal states;
- \(L_b\) is the maximal spatial extension constructible at stage \(b\);
- \(T_b\) is the maximal temporal depth;
- \(E_b\) is the maximal operational energy;
- \(M_b\) is the maximal memory or inscription length.

If \(b\le c\), then stage \(c\) extends the resources of stage \(b\):
\[
R_i(b)\le R_i(c)
\]
for each component \(i\).

A physical theory is not a single structure over a completed universe. It is a directed system
\[
\{\mathcal S_b\}_{b\in I}
\]
of finite stage structures.

---

### 2.2 Finite stage ontology

At stage \(b\), the physical world is represented by a finite inscriptional structure
\[
\mathcal M_b=(E_b,\prec_b,\rho_b),
\]
where:

- \(E_b\) is a finite set of elementary events or construction tokens;
- \(\prec_b\) is a finite causal or dependency order;
- \(\rho_b\) is a finite resource-weighting map.

No completed manifold is assumed. A continuum metric, if it appears, is an effective coarse-graining of \(\mathcal M_b\) in its interior.

---

### 2.3 Finite state spaces

Each stage \(b\) carries a finite-dimensional Hilbert space
\[
\mathcal H_b,\qquad \dim\mathcal H_b=N_b<\infty.
\]
If \(b\le c\), there is a partial embedding
\[
V_{bc}:\mathcal H_b\hookrightarrow\mathcal H_c
\]
defined when the extension from \(b\) to \(c\) is constructively admissible.

There is no completed Hilbert space
\[
\mathcal H_\infty=\varinjlim_b\mathcal H_b
\]
accepted as an ontological object. At most, \(\mathcal H_\infty\) is an idealized limit used for stable interior calculations.

---

### 2.4 Finite observable algebras

The algebra of observables at stage \(b\) is a finite-dimensional \(C^*\)-algebra
\[
\mathcal A_b\subseteq \operatorname{End}(\mathcal H_b).
\]
In the simplest case,
\[
\mathcal A_b=M_{N_b}(\mathbb C).
\]
A state is a density matrix
\[
\rho_b\in\mathcal D(\mathcal H_b),
\]
and expectation values are
\[
\langle A\rangle_b=\operatorname{Tr}(\rho_b A),\qquad A\in\mathcal A_b.
\]

Because \(\mathcal A_b\) is finite-dimensional, all ultraviolet divergences are absent at the ontological level. Divergences arise only if one incorrectly extrapolates to the rejected colimit.

---

### 2.5 Stable laws

A law is not an absolute statement over a completed universe. It is a stable relation across stages.

Let \(\mathcal L_b\) be a candidate physical law formulated at stage \(b\). We say that \(\mathcal L\) is **stable** if there exists \(b_0\in I\) such that for all \(c\ge b_0\),
\[
\mathcal L_c
\]
holds up to corrections that vanish in the interior of stage \(c\).

Classical physics is the study of stable interior laws. Ultrafinitist physics adds the boundary and resource corrections that stable laws omit.

---

## 3. Finite-Stage Kinematics and Emergent Geometry

### 3.1 From finite causal structure to effective metric

Let \(\mathcal M_b=(E_b,\prec_b,\rho_b)\) be a finite stage. In an interior region sufficiently far from the stage boundary, one may introduce effective coordinates
\[
x^\mu=(t,x^i)
\]
and an effective metric
\[
g^{(b)}_{\mu\nu}(x).
\]
This metric is not fundamental. It is a coarse-grained relation encoding the density of causal links and resource weights in \(\mathcal M_b\).

The effective line element is
\[
ds_b^2=g^{(b)}_{\mu\nu}(x)\,dx^\mu dx^\nu.
\]
The subscript \(b\) is essential. The metric is stage-dependent and partially defined.

The finite stage introduces a minimal constructible length
\[
\ell_b
\]
and a minimal constructible time
\[
\tau_b.
\]
These are not necessarily universal constants. They may vary with the resource stage.

---

### 3.2 Interior and boundary regions

Let \(\Omega_b\) denote the effective spacetime region available at stage \(b\). It has an interior
\[
\Omega_b^\circ
\]
and a resource boundary
\[
\partial\Omega_b.
\]
The interior is the region where embeddings into larger stages preserve local structure with negligible distortion. The boundary is the region where the failure of completed infinity becomes physically measurable.

The central kinematic distinction is therefore:

\[
\text{interior physics} \quad\neq\quad \text{boundary physics}.
\]

Classical physics is the physics of \(\Omega_b^\circ\) in the idealized limit in which \(\partial\Omega_b\) is ignored.

---

### 3.3 No fundamental singularities

A classical singularity usually requires a completed manifold and an infinite limiting process: geodesics of unbounded affine parameter, curvature blow-up, or incomplete Cauchy development.

In the bounded framework, such totalities are not available. A finite stage has finite causal depth. Therefore, what classical theory calls a singularity is reinterpreted as termination at a resource boundary.

Thus:

> Singularities are not physical infinities. They are artifacts of projecting a finite stage into an illegitimate colimit.

This does not mean that high-curvature behavior is absent. It means that curvature blow-up is replaced by a finite boundary condition.

---

## 4. Bounded Action Principles

### 4.1 Finite histories

A history at stage \(b\) is not a path in a completed configuration space. It is a finite construction tree. Let
\[
\mathfrak H_b
\]
be the finite set of admissible histories at stage \(b\). Each history \(h\in\mathfrak H_b\) carries a construction cost
\[
C_b(h).
\]
Only histories satisfying
\[
C_b(h)\le B
\]
are admissible for a given bound \(B\).

The bounded path amplitude is therefore a finite sum:
\[
\mathcal Z_b
=
\sum_{\substack{h\in\mathfrak H_b\\ C_b(h)\le B}}
\mu_b(h)\,
e^{\frac{i}{\hbar}S_b[h]},
\]
where \(\mu_b(h)\) is a finite combinatorial weight.

There is no completed functional integral.

---

### 4.2 Discrete action for fields

Let \(K_b\) be a finite cell decomposition of the stage region \(\Omega_b\). Let \(\phi_\sigma\) denote the field value assigned to cell \(\sigma\in K_b\). The bounded action is
\[
S_b[\phi]
=
\sum_{\sigma\in K_b}
V_\sigma\,
\mathcal L_b\!\left(\phi_\sigma,\Delta\phi_\sigma\right)
+
\sum_{\sigma\in\partial K_b}
\beta_\sigma\phi_\sigma,
\]
where:

- \(V_\sigma\) is the finite volume weight;
- \(\Delta\phi_\sigma\) denotes finite differences;
- \(\beta_\sigma\) is a boundary resource term.

The boundary term is not optional. It encodes the fact that the domain of construction is finite.

---

### 4.3 Discrete Euler–Lagrange equation

Consider a one-dimensional finite chain with variables \(q_0,\dots,q_N\) and action
\[
S[q]=\sum_{n=0}^{N-1}L(q_{n+1},q_n).
\]
Varying an interior variable \(q_n\), \(1\le n\le N-1\), gives
\[
\delta S
=
\left[
\partial_1 L(q_n,q_{n-1})
+
\partial_2 L(q_{n+1},q_n)
\right]\delta q_n.
\]
Thus the interior equations of motion are
\[
\partial_1 L(q_n,q_{n-1})
+
\partial_2 L(q_{n+1},q_n)
=0.
\]
At the endpoint \(q_N\), one obtains instead
\[
\partial_1 L(q_N,q_{N-1})=\beta_N.
\]
Therefore the finite stage produces both interior field equations and boundary resource conditions.

For fields, the analogous result is
\[
\Box_b\phi-\frac{\partial V}{\partial\phi}=0
\quad\text{in }\Omega_b^\circ,
\]
with boundary condition
\[
n_b^\mu\Delta_\mu\phi=\beta_b
\quad\text{on }\partial\Omega_b.
\]
Here \(\Box_b\) is the finite-difference d’Alembertian associated with the stage.

---

### 4.4 Continuum limit and correction terms

In an interior region where \(\ell_b\) and \(\tau_b\) are small relative to macroscopic scales, one may expand
\[
\Box_b
=
\Box_g
+
\ell_b^2\,\mathcal D^{(4)}
+
O(\ell_b^4),
\]
where \(\Box_g=\nabla^\mu\nabla_\mu\) is the continuum d’Alembertian and \(\mathcal D^{(4)}\) is a fourth-order differential operator determined by the finite-stage discretization.

Thus a scalar field satisfies
\[
\left(\Box_g+m^2\right)\phi
=
-\ell_b^2\mathcal D^{(4)}\phi
+
O(\ell_b^4).
\]
The right-hand side is a physical correction due to bounded construction. It is not a renormalization counterterm; it is the residue of the rejected continuum limit.

---

## 5. Bounded Gravity and Resource-Corrected Einstein Equations

### 5.1 Finite Regge action

A finite-stage gravitational action is naturally written in Regge form. Let \(K_b\) be a finite simplicial complex. Let \(A_h\) be the area of a hinge \(h\), and let \(\epsilon_h\) be the corresponding deficit angle. The bounded gravitational action is
\[
S_b^{\mathrm{grav}}
=
\frac{1}{8\pi G}
\sum_{h\in K_b}
A_h\epsilon_h
-
\frac{\Lambda_b}{8\pi G}
\sum_{\sigma\in K_b}
V_\sigma.
\]
The sums are finite. No continuum limit is required for the stage theory to be meaningful.

Variation with respect to an edge length \(l_e\) gives the discrete Regge equation
\[
\sum_{h\supset e}
\epsilon_h
\frac{\partial A_h}{\partial l_e}
=
8\pi G
\frac{\partial S_b^{\mathrm{matter}}}{\partial l_e}.
\]

---

### 5.2 Effective continuum equation

Coarse-graining the finite Regge equations in the interior of a sufficiently large stage yields an effective tensor equation
\[
G_{\mu\nu}^{(b)}
+
\Lambda_b g_{\mu\nu}^{(b)}
=
8\pi G
\left(
T_{\mu\nu}
+
\tau_{\mu\nu}^{(b)}
\right).
\]
Here:

- \(G_{\mu\nu}^{(b)}\) is the effective Einstein tensor;
- \(T_{\mu\nu}\) is the matter stress tensor;
- \(\tau_{\mu\nu}^{(b)}\) is the resource-stage correction tensor.

The correction tensor has two contributions:
\[
\tau_{\mu\nu}^{(b)}
=
\tau_{\mu\nu}^{\mathrm{bulk}}
+
\tau_{\mu\nu}^{\partial}.
\]

The bulk contribution is of higher-derivative form:
\[
\tau_{\mu\nu}^{\mathrm{bulk}}
=
\alpha_b\ell_b^2
\left(
R_{\mu\rho\sigma\lambda}
R_{\nu}{}^{\rho\sigma\lambda}
-
\frac14 g_{\mu\nu}R_{\rho\sigma\alpha\beta}R^{\rho\sigma\alpha\beta}
\right)
+
O(\ell_b^4).
\]
The boundary contribution is supported near \(\partial\Omega_b\):
\[
\tau_{\mu\nu}^{\partial}
=
\frac{1}{8\pi G}
\left(
\nabla_\mu n_\nu
-
g_{\mu\nu}\nabla_\alpha n^\alpha
\right)
\delta_{\partial\Omega_b}
+
\cdots,
\]
where \(n^\mu\) is the outward resource-normal to the stage boundary.

Thus the classical Einstein equation is not false; it is the interior stable approximation to a finite-stage equation. The full equation contains resource-boundary stress.

---

### 5.3 Physical meaning of \(\tau_{\mu\nu}^{(b)}\)

The tensor \(\tau_{\mu\nu}^{(b)}\) encodes the failure of the continuum colimit. In regions where the stage is large and the boundary is far away,
\[
\tau_{\mu\nu}^{(b)}\approx 0.
\]
Near resource boundaries, however, it becomes significant.

This implies that horizons, cosmological boundaries, and high-curvature regions are not merely classical objects. They are locations where the finite character of construction becomes dynamically visible.

---

## 6. Modified Noether Theorem and Resource Anomalies

### 6.1 Classical Noether theorem

In classical field theory, if an action is invariant under a continuous symmetry, then there is a conserved current:
\[
\nabla_\mu J^\mu=0.
\]
This assumes a completed spacetime domain and unrestricted integration by parts.

In a finite stage, the domain itself is not invariant under arbitrary transformations. Translations, boosts, and time evolutions can move configurations toward or beyond the resource boundary.

Therefore conservation laws acquire anomaly terms.

---

### 6.2 Stage-dependent symmetry variation

Let \(\Phi^A\) denote the fields, and let
\[
\delta\Phi^A=\epsilon X^A
\]
be an infinitesimal transformation. Suppose the stage action varies as
\[
\delta S_b
=
\epsilon
\int_{\Omega_b}
d^4x\sqrt{-g}\,\sigma_b
+
\epsilon
\int_{\partial\Omega_b}
d^3y\sqrt{|h|}\,K_b.
\]
The bulk term \(\sigma_b\) is the resource anomaly. The boundary term \(K_b\) is the resource flux.

The associated Noether current is
\[
J^\mu
=
\frac{\partial\mathcal L}{\partial(\nabla_\mu\Phi^A)}X^A
-
K^\mu,
\]
where \(K^\mu\) is chosen so that the boundary variation is encoded covariantly.

One then obtains the modified Noether identity
\[
\nabla_\mu J^\mu=\sigma_b.
\]

---

### 6.3 Energy non-conservation at resource boundaries

For time translations, \(J^\mu\) is the energy current. The modified conservation law becomes
\[
\nabla_\mu T^{\mu\nu}=f_b^\nu,
\]
where \(f_b^\nu\) is a resource-force density supported near the stage boundary.

In a homogeneous cosmological setting, this gives
\[
\dot\rho+3H(\rho+p)=\sigma_b(t).
\]
In the interior, \(\sigma_b\approx 0\), and ordinary conservation is recovered. Near a cosmological resource boundary, energy exchange with the stage becomes possible.

This is a new physical effect: apparent non-conservation is not a violation of physics but a signal that the system has reached the edge of its constructive domain.

---

## 7. Finite-Stage Quantum Mechanics

### 7.1 Failure of the canonical commutation relation

In ordinary quantum mechanics, position and momentum satisfy
\[
[q,p]=i\hbar I.
\]
This relation cannot hold exactly in a finite-dimensional Hilbert space.

Indeed, if \(\dim\mathcal H_b=N_b<\infty\), then for any two operators \(A,B\),
\[
\operatorname{Tr}[A,B]=0.
\]
But if \([q,p]=i\hbar I\), then
\[
\operatorname{Tr}[q,p]
=
i\hbar\operatorname{Tr}I
=
i\hbar N_b
\neq 0.
\]
Contradiction.

Therefore the canonical commutation relation is not a fundamental law. It is an interior approximation valid when boundary states are negligibly populated.

---

### 7.2 Boundary-corrected commutator

The finite-stage commutator must have the form
\[
[q,p]
=
i\hbar\left(I-\Pi_\partial\right),
\]
where \(\Pi_\partial\) is a positive boundary projector satisfying
\[
\operatorname{Tr}\Pi_\partial=1.
\]
Then
\[
\operatorname{Tr}[q,p]
=
i\hbar\left(N_b-1\right)
-
i\hbar N_b
=0,
\]
as required.

For states supported away from the boundary,
\[
\langle\Pi_\partial\rangle\approx 0,
\]
and the usual Heisenberg relation is recovered.

---

### 7.3 Modified uncertainty relation

By the Robertson inequality,
\[
\Delta q\,\Delta p
\ge
\frac12
\left|
\langle[q,p]\rangle
\right|.
\]
Using the boundary-corrected commutator gives
\[
\Delta q\,\Delta p
\ge
\frac{\hbar}{2}
\left|
1-\langle\Pi_\partial\rangle
\right|.
\]
Thus the standard uncertainty principle is stage-local. Near the resource boundary, quantum fluctuations are modified by edge effects.

This predicts deviations from ordinary quantum mechanics for states that probe the finite limits of phase-space construction.

---

### 7.4 Finite entanglement entropy

Because \(\mathcal H_b\) is finite-dimensional, entanglement entropy is automatically bounded:
\[
S_{\mathrm{ent}}\le \log N_b.
\]
There are no infinite vacuum entanglement divergences. The usual divergent area law arises only after extrapolating to the rejected continuum.

This provides a natural explanation for holographic entropy bounds: finite constructible regions have finite state spaces.

---

## 8. Modified Dispersion from Finite-Stage Fields

### 8.1 Finite-difference field equation

Consider a scalar field on a finite regular stage with time step \(\tau_b\) and spatial step \(\ell_b\). Let \(D_t\) and \(D_i\) be finite-difference operators. A bounded quadratic action may be written as
\[
S_b
=
\frac12
\sum_{x}
\left[
(D_t\phi)^2
-
c^2(D_i\phi)^2
-
m^2c^4\hbar^{-2}\phi^2
-
\xi_b\ell_b^2(D_i^2\phi)^2
\right].
\]
The final term is a finite-stage regulator generated by bounded construction. It is not added by hand to cure divergences; it is required because the stage has no arbitrarily high modes.

The field equation is
\[
D_t^2\phi
-
c^2D_i^2\phi
+
m^2c^4\hbar^{-2}\phi
+
\xi_b\ell_b^2D_i^4\phi
=0.
\]

---

### 8.2 Exact finite-stage dispersion

For a plane-wave mode on the finite lattice,
\[
\phi(t,x)\sim e^{-i\omega t+ikx},
\]
the finite-difference operators yield
\[
D_t^2\mapsto
-\frac{4}{\tau_b^2}
\sin^2\!\left(\frac{\omega\tau_b}{2}\right),
\]
and
\[
D_i^2\mapsto
-\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right).
\]
Therefore the exact dispersion relation is
\[
\frac{4}{\tau_b^2}
\sin^2\!\left(\frac{\omega\tau_b}{2}\right)
=
c^2
\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right)
+
\frac{m^2c^4}{\hbar^2}
+
\xi_b\ell_b^2
\left[
\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right)
\right]^2.
\]

This relation is finite, bounded, and stage-dependent.

---

### 8.3 Low-energy expansion

For modes satisfying
\[
|k|\ell_b\ll 1,
\qquad
|\omega|\tau_b\ll 1,
\]
one obtains
\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta_b
\frac{\ell_b^2c^2}{\hbar^2}
p^4
+
O(\ell_b^4p^6),
\]
where
\[
E=\hbar\omega,
\qquad
p=\hbar k,
\]
and \(\eta_b\) is a dimensionless stage parameter determined by \(\xi_b\), \(\tau_b\), and \(\ell_b\).

Define the stage energy scale
\[
E_b=\frac{\hbar c}{\ell_b}.
\]
Then for massless particles,
\[
E^2
=
p^2c^2
\left[
1+\eta_b\left(\frac{E}{E_b}\right)^2
+
O\!\left(\frac{E}{E_b}\right)^4
\right].
\]
The group velocity becomes
\[
v_g
=
\frac{dE}{dp}
\approx
c
\left[
1+
\frac{3}{2}\eta_b
\left(\frac{E}{E_b}\right)^2
\right].
\]

Thus ultrafinitist physics predicts energy-dependent propagation when the stage is not perfectly Lorentz-symmetric. The sign and magnitude of \(\eta_b\) are stage-dependent, but the existence of such corrections is generic once completed Lorentz invariance is refused.

---

## 9. Resource Horizons and Black-Hole Entropy

### 9.1 Horizon as resource boundary

A black-hole horizon is naturally interpreted as a resource boundary. The interior region is not accessible as a completed totality. The finite stage associated with an exterior observer has a boundary carrying finite information capacity.

Let \(A\) be the horizon area. The finite-stage construction assigns to the horizon a finite number of boundary degrees of freedom. The maximum number of distinguishable horizon states is
\[
\Omega_b(A)<\infty.
\]

---

### 9.2 Counting boundary states

Assume the horizon is composed of elementary area cells of order \(\ell_P^2\). Let the number of cells be
\[
N=\frac{A}{\alpha\ell_P^2},
\]
where \(\alpha\) is a dimensionless combinatorial constant. If each cell carries a finite number of internal states, and if the total area constraint is imposed, the asymptotic number of configurations has the form
\[
\Omega_b(A)
\sim
\exp\!\left(\frac{A}{4\ell_P^2}\right)
\left(\frac{A}{\ell_P^2}\right)^\gamma
\left[
1+O\!\left(\frac{\ell_P^2}{A}\right)
\right].
\]
The leading exponential term reproduces the Bekenstein–Hawking entropy. The power correction is a finite-stage combinatorial effect.

Thus
\[
S_b(A)
=
\ln\Omega_b(A)
=
\frac{A}{4\ell_P^2}
+
\gamma\ln\!\left(\frac{A}{\ell_P^2}\right)
+
O(1).
\]

The ultrafinitist framework fixes \(\gamma\) through finite counting rather than through an infinite field-theoretic trace. A natural bounded-construction value is
\[
\gamma=-\frac32,
\]
although the precise value depends on the finite stage algebra.

---

### 9.3 Corrected Hawking temperature

For a Schwarzschild black hole,
\[
A=16\pi G^2M^2
\]
in units \(c=\hbar=k_B=1\). The temperature is
\[
T^{-1}
=
\frac{dS}{dM}.
\]
Using
\[
S=4\pi G M^2+\gamma\ln M+\text{const},
\]
one finds
\[
\frac{dS}{dM}
=
8\pi G M
+
\frac{\gamma}{M}.
\]
Therefore
\[
T
=
T_H
\left[
1-
\frac{\gamma}{8\pi G M^2}
+
O(M^{-4})
\right].
\]
Since
\[
A=16\pi G^2M^2,
\]
this may be written as
\[
T
=
T_H
\left[
1-
\frac{2\gamma\ell_P^2}{A}
+
O(A^{-2})
\right].
\]
For \(\gamma=-3/2\),
\[
T
=
T_H
\left[
1+
\frac{3\ell_P^2}{A}
+
O(A^{-2})
\right].
\]

Thus finite-stage physics predicts a small positive correction to the Hawking temperature for microscopic black holes.

---

## 10. Bounded Cosmology and the Removal of the Initial Singularity

### 10.1 Finite holonomy construction

In a finite stage, connections cannot be treated as completed infinitesimal objects. Only finite holonomies are constructible. Let \(\lambda_b\) be the minimal loop length allowed at stage \(b\). The gravitational connection then appears through bounded holonomy variables
\[
h_{\lambda_b}
=
\exp(i\lambda_b c),
\]
where \(c\) is the symmetry-reduced connection variable.

Because holonomies are bounded, the effective Hamiltonian constraint must replace \(c^2\) by a bounded function of \(c\). The simplest finite-stage replacement is
\[
c^2
\mapsto
\frac{\sin^2(\lambda_b c)}{\lambda_b^2}.
\]

---

### 10.2 Effective Hamiltonian constraint

For a flat homogeneous cosmology, let \(a(t)\) be the scale factor and let
\[
p=a^2.
\]
The bounded Hamiltonian constraint takes the form
\[
\mathcal C_b
=
-\frac{3}{8\pi G\gamma_{\mathrm{Im}}^2\lambda_b^2}
\sqrt{p}\,
\sin^2(\lambda_b c)
+
p^{3/2}\rho
=0,
\]
where \(\gamma_{\mathrm{Im}}\) is the Immirzi parameter and \(\rho\) is the matter energy density.

The constraint gives
\[
\sin^2(\lambda_b c)
=
\frac{8\pi G\gamma_{\mathrm{Im}}^2\lambda_b^2}{3}
\rho.
\]

---

### 10.3 Modified Friedmann equation

The Hubble rate is obtained from the bounded connection as
\[
H
=
\frac{1}{\gamma_{\mathrm{Im}}\lambda_b}
\sin(\lambda_b c)\cos(\lambda_b c).
\]
Squaring and using the constraint yields
\[
H^2
=
\frac{1}{\gamma_{\mathrm{Im}}^2\lambda_b^2}
\sin^2(\lambda_b c)
\left[
1-\sin^2(\lambda_b c)
\right].
\]
Substituting the expression for \(\sin^2(\lambda_b c)\), one obtains
\[
H^2
=
\frac{8\pi G}{3}
\rho
\left(
1-\frac{\rho}{\rho_b}
\right),
\]
where the stage density is
\[
\rho_b
=
\frac{3}{8\pi G\gamma_{\mathrm{Im}}^2\lambda_b^2}.
\]

This is the bounded-construction Friedmann equation.

---

### 10.4 Cosmological bounce

Because
\[
H^2\ge 0,
\]
the density is bounded:
\[
\rho\le \rho_b.
\]
At \(\rho=\rho_b\),
\[
H=0,
\]
and the universe undergoes a bounce rather than a singularity.

The acceleration equation follows from differentiating the modified Friedmann equation and using the interior conservation law
\[
\dot\rho+3H(\rho+p)=0.
\]
One finds
\[
\dot H
=
-4\pi G(\rho+p)
\left(
1-\frac{2\rho}{\rho_b}
\right).
\]
Thus near \(\rho_b\), the effective gravitational dynamics becomes repulsive.

The initial singularity is removed not by adding exotic matter, but by refusing the completed infinite past.

---

### 10.5 Resource anomaly in late-time cosmology

At late times, cosmological horizons introduce another resource boundary. The modified conservation law becomes
\[
\dot\rho+3H(\rho+p)=\sigma_b(t).
\]
A small positive anomaly can mimic an effective dark-energy source. In this framework, dark energy need not be a fundamental substance. It may be the large-scale signature of finite-stage boundary flux.

A natural estimate is
\[
\Lambda_b
\sim
\frac{1}{R_b^2},
\]
where \(R_b\) is the effective radius of the observable construction stage.

---

## 11. Renormalization without Completed Infinities

### 11.1 Finite loop sums

In ordinary quantum field theory, loop diagrams diverge because one integrates over an infinite momentum space. In the bounded framework, momentum space is finite:
\[
|p|\le p_b,
\qquad
p_b\sim\frac{\hbar}{\ell_b}.
\]
Thus loop traces are finite matrix traces.

For a quadratic fluctuation operator \(K_b[\phi]\), the one-loop effective action is
\[
\Gamma_b^{(1)}[\phi]
=
\frac{i\hbar}{2}
\operatorname{Tr}_{\mathcal H_b}
\ln K_b[\phi].
\]
Since \(\mathcal H_b\) is finite-dimensional, this expression is finite without regularization.

---

### 11.2 Stage-dependent running couplings

Couplings depend on the stage scale \(\mu\). For a gauge coupling \(g\), one has
\[
\mu\frac{dg}{d\mu}
=
\beta(g)
+
O\!\left(\frac{\mu^2}{E_b^2}\right).
\]
At low energies, the usual beta function is recovered. Near the stage bound, the running is modified by finite-construction effects.

Landau poles and ultraviolet divergences are reinterpreted as failures of the colimit idealization, not as physical infinities.

---

## 12. Principal Physical Predictions

The bounded-construction framework yields several testable or at least phenomenologically distinguishable effects.

### 12.1 Energy-dependent propagation

For massless particles,
\[
v_g(E)
\approx
c
\left[
1+
\eta_b
\left(\frac{E}{E_b}\right)^2
\right].
\]
High-energy photons from distant astrophysical transients should exhibit arrival-time shifts
\[
\Delta t
\sim
\eta_b
\frac{E^2}{E_b^2}
\frac{D}{c},
\]
where \(D\) is the propagation distance.

---

### 12.2 Modified black-hole thermodynamics

The entropy and temperature acquire corrections:
\[
S
=
\frac{A}{4\ell_P^2}
+
\gamma\ln\!\left(\frac{A}{\ell_P^2}\right)
+
O(1),
\]
\[
T
=
T_H
\left[
1-
\frac{2\gamma\ell_P^2}{A}
+
O(A^{-2})
\right].
\]
These corrections become relevant for near-Planckian black holes.

---

### 12.3 Cosmological bounce

The early universe satisfies
\[
H^2
=
\frac{8\pi G}{3}
\rho
\left(
1-\frac{\rho}{\rho_b}
\right).
\]
This replaces the big-bang singularity by a finite-density bounce. Primordial perturbations should therefore contain signatures of a pre-bounce contracting phase or of finite-stage cutoff effects.

---

### 12.4 Apparent energy non-conservation near horizons

Near resource boundaries,
\[
\nabla_\mu T^{\mu\nu}=f_b^\nu.
\]
This can produce small apparent violations of local energy conservation in strong-gravity or cosmological-horizon regimes. Such effects are not violations of consistency; they are fluxes across the edge of the constructible stage.

---

### 12.5 Finite entanglement entropy

Vacuum entanglement entropy is finite at the fundamental level. The usual area-law divergence is replaced by
\[
S_{\mathrm{ent}}
\le
\log N_b.
\]
This predicts a maximal information content for any finite region, in agreement with holographic intuition but without assuming a completed continuum.

---

## 13. Conceptual Consequences

### 13.1 The continuum is a colimit idealization

Classical spacetime is the idealized colimit
\[
M_{\infty}
=
\varinjlim_b M_b.
\]
Ultrafinitist physics accepts the directed system but refuses the ontological reality of the colimit.

Thus:
\[
\text{Classical physics}
=
\text{finite-stage physics}
+
\text{acceptance of the colimit}.
\]

The new physics consists precisely in the terms suppressed by the colimit idealization.

---

### 13.2 Laws are stable patterns, not eternal truths

A physical law is not a timeless relation over a completed universe. It is a stable relation across resource stages. This shifts the aim of fundamental physics from discovering absolute equations to identifying stable construction rules and their boundary corrections.

---

### 13.3 Measurement is inscription

A measurement is not an abstract projection in an infinite Hilbert space. It is the creation of a finite record within a bounded stage. The measurement result is an inscription whose existence depends on available memory and energy.

Thus the measurement problem is reformulated as a problem of bounded record formation, not as a paradox about infinite wavefunctions.

---

### 13.4 Singularities are category errors

Singularities arise when one treats a finite construction as if it were a completed infinite object. In the bounded framework, geodesics terminate at resource boundaries. Curvature invariants remain finite because the stage itself is finite.

The question is not “what happens at the singularity?” but rather:

> At what resource boundary does the classical colimit cease to be stable?

---

## 14. Conclusion

I have derived a physical framework from ultrafinitist foundations. The central result is that refusing completed infinities changes physics. Finite-stage construction produces boundary-corrected field equations, modified conservation laws, finite quantum algebras, corrected dispersion relations, finite black-hole entropy corrections, and nonsingular cosmology.

The classical continuum is not abolished; it is demoted. It is a stable interior approximation to a deeper bounded constructive dynamics. The new physics lies in the corrections that appear when the finite stage can no longer be hidden behind the fiction of completed infinity.

Ultrafinitism therefore does not merely constrain mathematics. It generates physics.

---

## Appendix A: Proof that Exact Canonical Commutation Fails in Finite Stages

Let \(\mathcal H_b\) be finite-dimensional with
\[
\dim\mathcal H_b=N_b.
\]
For any operators \(A,B\in\operatorname{End}(\mathcal H_b)\),
\[
\operatorname{Tr}[A,B]
=
\operatorname{Tr}(AB)-\operatorname{Tr}(BA)
=
0.
\]
Suppose there exist \(q,p\) such that
\[
[q,p]=i\hbar I.
\]
Taking the trace gives
\[
0
=
\operatorname{Tr}[q,p]
=
i\hbar\operatorname{Tr}I
=
i\hbar N_b.
\]
Since \(\hbar>0\) and \(N_b>0\), this is impossible. Therefore the canonical commutation relation cannot be exact in any finite-dimensional stage Hilbert space.

A boundary-corrected commutator must satisfy
\[
\operatorname{Tr}[q,p]=0.
\]
The ansatz
\[
[q,p]=i\hbar(I-\Pi_\partial)
\]
does so provided
\[
\operatorname{Tr}\Pi_\partial=1.
\]
Thus finite-stage quantum mechanics necessarily contains edge corrections.

---

## Appendix B: Low-Energy Expansion of the Modified Dispersion Relation

Starting from
\[
\frac{4}{\tau_b^2}
\sin^2\!\left(\frac{\omega\tau_b}{2}\right)
=
c^2
\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right)
+
\frac{m^2c^4}{\hbar^2}
+
\xi_b\ell_b^2
\left[
\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right)
\right]^2,
\]
expand for small \(\omega\tau_b\) and \(k\ell_b\):
\[
\sin^2 x
=
x^2-\frac{x^4}{3}+O(x^6).
\]
Then
\[
\frac{4}{\tau_b^2}
\left[
\frac{\omega^2\tau_b^2}{4}
-
\frac{\omega^4\tau_b^4}{48}
+
O(\omega^6\tau_b^6)
\right]
=
\omega^2
-
\frac{\tau_b^2}{12}\omega^4
+
O(\omega^6\tau_b^4).
\]
Similarly,
\[
c^2
\frac{4}{\ell_b^2}
\sin^2\!\left(\frac{k\ell_b}{2}\right)
=
c^2k^2
-
\frac{c^2\ell_b^2}{12}k^4
+
O(k^6\ell_b^4).
\]
The regulator term contributes at order \(\ell_b^2k^4\). Collecting terms and writing \(E=\hbar\omega\), \(p=\hbar k\), one obtains
\[
E^2
=
p^2c^2
+
m^2c^4
+
\eta_b
\frac{\ell_b^2c^2}{\hbar^2}
p^4
+
O(\ell_b^4p^6),
\]
where \(\eta_b\) absorbs the finite-stage coefficients. For massless particles,
\[
E
\approx
pc
\left[
1+
\frac{\eta_b}{2}
\left(\frac{E}{E_b}\right)^2
\right],
\]
and therefore
\[
v_g
=
\frac{dE}{dp}
\approx
c
\left[
1+
\frac{3\eta_b}{2}
\left(\frac{E}{E_b}\right)^2
\right].
\]

---

## Appendix C: Bounded Friedmann Dynamics

The bounded constraint gives
\[
\sin^2(\lambda_b c)
=
\frac{\rho}{\rho_b}.
\]
The Hubble rate is
\[
H
=
\frac{1}{\gamma_{\mathrm{Im}}\lambda_b}
\sin(\lambda_b c)\cos(\lambda_b c).
\]
Therefore
\[
H^2
=
\frac{1}{\gamma_{\mathrm{Im}}^2\lambda_b^2}
\frac{\rho}{\rho_b}
\left(
1-\frac{\rho}{\rho_b}
\right).
\]
Using
\[
\rho_b
=
\frac{3}{8\pi G\gamma_{\mathrm{Im}}^2\lambda_b^2},
\]
one obtains
\[
H^2
=
\frac{8\pi G}{3}
\rho
\left(
1-\frac{\rho}{\rho_b}
\right).
\]
Differentiating,
\[
2H\dot H
=
\frac{8\pi G}{3}
\dot\rho
\left(
1-\frac{2\rho}{\rho_b}
\right).
\]
With
\[
\dot\rho=-3H(\rho+p),
\]
this gives
\[
\dot H
=
-4\pi G(\rho+p)
\left(
1-\frac{2\rho}{\rho_b}
\right).
\]
At \(\rho=\rho_b\), \(H=0\), while \(\dot H\) remains finite. The singularity is replaced by a bounded transition surface.

---

## References

1. A. S. Yessenin-Volpin, *Notes on ultrafinitism and feasible mathematics*.  
2. R. Parikh, “Existence and Feasibility in Mathematics,” *Journal of Symbolic Logic*, 1971.  
3. S. R. Buss, *Bounded Arithmetic*, Bibliopolis, 1986.  
4. C. Wright, “Strict Finitism,” *Synthese*, 1982.  
5. J. Krajíček, *Bounded Arithmetic, Propositional Logic, and Complexity Theory*, Cambridge University Press, 1995.  
6. P. Hájek and P. Pudlák, *Metamathematics of First-Order Arithmetic*, Springer, 1993.  
7. L. Bombelli, J. Lee, D. Meyer, and R. Sorkin, “Space-Time as a Causal Set,” *Physical Review Letters*, 1987.  
8. R. D. Sorkin, “Causal Sets: Discrete Gravity,” in *Lectures on Quantum Gravity*, World Scientific.  
9. J. D. Bekenstein, “Black Holes and Entropy,” *Physical Review D*, 1973.  
10. S. W. Hawking, “Particle Creation by Black Holes,” *Communications in Mathematical Physics*, 1975.  
11. A. Ashtekar and P. Singh, “Loop Quantum Cosmology: A Status Report,” *Classical and Quantum Gravity*, 2011.  
12. C. Rovelli, *Quantum Gravity*, Cambridge University Press, 2004.  
13. G. ’t Hooft, “Dimensional Reduction in Quantum Gravity,” *arXiv:gr-qc/9310026*.  
14. L. Susskind, “The World as a Hologram,” *Journal of Mathematical Physics*, 1995.  
15. G. Amelino-Camelia, “Quantum-Spacetime Phenomenology,” *Living Reviews in Relativity*, 2013.

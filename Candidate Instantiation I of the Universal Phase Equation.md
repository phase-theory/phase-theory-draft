# Candidate Instantiation I of the Universal Phase Equation  
## A Combinatorial Phase Complex, an \(SU(2)\) Phase Target, and a Stabilized Topological Phase Action

**Dust LLC — Universal Phase Theory Preprint**  
**Foundational Series: Concrete Instantiations of \(\mathscr F\)**  
**August 2026**

---

## Abstract

We propose the first concrete candidate instantiation of the universal phase equation  
\[
\mathscr F[\Phi;\lambda]=0
\]
within Universal Phase Theory (UPT). This construction is a proposal, not the completed universal phase equation. Its purpose is to convert the UPT operator hierarchy
\[
\mathscr F[\Phi;\lambda]=0,
\qquad
\mathscr L_\Phi:=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi:=\operatorname{Det}_\Phi(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi:=\mathscr L_\Phi^{-1}
\]
into an explicitly computable phase system.

The candidate chooses:

1. **Base structure**  
   \[
   \mathcal X
   \]
   as a finite oriented combinatorial phase complex: a cell complex or incidence category with vertices, edges, higher cells, orientations, and adjacency, but no assumed metric, no assumed spacetime manifold, and no assumed Lorentzian signature.

2. **Phase target**  
   \[
   \mathcal M_\Phi = SU(2)
   \]
   regarded not as the Standard Model weak group, but as the minimal compact non-Abelian Lie group supporting nontrivial three-dimensional topological sectors,
   \[
   \pi_3(SU(2))\cong \mathbb Z.
   \]

3. **Phase action**  
   A discrete phase functional
   \[
   S_\Phi[\Phi;\lambda]
   =
   S_{\mathrm{grad}}[\Phi]
   +
   S_{\mathrm{curv}}[\Phi]
   +
   i\theta\,Q[\Phi],
   \]
   where \(S_{\mathrm{grad}}\) is a kinetic phase-difference term, \(S_{\mathrm{curv}}\) is a quartic phase-curvature stabilization term, and \(Q[\Phi]\) is an integer-valued topological winding functional. No bulk Standard Model field content, no pre-existing metric, no particle list, and no Born rule are inserted.

We derive the corresponding phase equation, stability operator, bifurcation operator, and susceptibility tensor. We show that the candidate possesses a stable vacuum sector, finite-excess topological sectors, a discrete sector label \(Q\in\mathbb Z\), and a candidate particle object of the form
\[
\mathfrak P_Q
=
[\Phi_Q]_{\mathscr G_\Phi}.
\]
We then audit the candidate against UPT Falsifiability Criteria A–F. The result is decisive: Candidate I provides a concrete computational realization of the UPT particle-sector mechanism, but it does not yet derive the observed gauge group, Lorentzian spacetime signature, Einstein gravity, or quantum measurement probabilities. It is therefore not the answer. It is the first falsifiable instantiation of \(\mathscr F\) from which the answer must be distinguished.

---

## Part I — Scope and Non-Insertion Principle

The purpose of this preprint is not to present a completed derivation of known physics from phase. It is to specify a concrete universal phase datum
\[
\mathfrak U
=
(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\lambda)
\]
sufficient to begin computation.

The construction is governed by the non-insertion principle.

The following structures must not be placed into \(\mathscr F\) as assumptions if they are to count as UPT derivations:

| Structure | Status in UPT | Forbidden insertion |
|---|---:|---|
| Spacetime metric \(g_{\mu\nu}\) | Emergent | Fixed Lorentzian metric |
| Gauge group \(SU(3)\times SU(2)\times U(1)\) | Emergent | Declared phase-frame group |
| Particle spectrum | Emergent | Predefined particle labels |
| Masses | Emergent | Fitted coefficients |
| Hilbert space | Emergent | Primitive quantum state space |
| Born rule | Emergent | Probability postulate |
| Dimension \(d_{\mathrm{eff}}=4\) | Emergent | Assumed four-dimensional manifold |

Candidate I is deliberately minimal. It is chosen to test whether the UPT hierarchy can generate:

\[
\Phi
\rightarrow
\text{topology}
\rightarrow
\text{geometry}
\rightarrow
\text{connections}
\rightarrow
\text{fields}
\rightarrow
\text{particles}
\rightarrow
\text{observables}.
\]

If even this minimal candidate fails to produce stable localized sectors, finite excess, or a coherent response geometry, the UPT program must be revised. If it succeeds mechanically but fails to generate the observed gauge structure, the candidate is falsified as a final theory but validated as a structural prototype.

---

## Part II — The Concrete UPT Datum

### 2.1 The base \(\mathcal X\): a combinatorial phase complex

We take \(\mathcal X\) to be a finite oriented combinatorial phase complex \(K\). Concretely, \(K\) is specified by:

1. A set of vertices \(K^{(0)}\).
2. A set of oriented edges \(K^{(1)}\).
3. Optional higher cells \(K^{(p)}\), \(p=2,3,4\), with incidence relations.
4. Orientations on edges and higher cells.
5. Positive combinatorial weights \(w_e,w_p\) on cells.

No metric is supplied. No coordinate distance is supplied. No Lorentzian signature is supplied. The only primitive relational data are incidence, orientation, and adjacency.

Let
\[
C^p(K)
\]
denote the real vector space of \(p\)-cochains on \(K\). The coboundary operator is
\[
d_p:C^p(K)\to C^{p+1}(K),
\qquad
d_{p+1}d_p=0.
\]
The weighted inner product on \(p\)-cochains is
\[
\langle \alpha,\beta\rangle_w
=
\sum_{\sigma\in K^{(p)}}
w_\sigma\,\alpha_\sigma\beta_\sigma.
\]
The adjoint coboundary is
\[
\delta_p
=
d_{p-1}^{*,w}.
\]
The combinatorial Laplacian on \(0\)-cochains is
\[
\Delta_0
=
\delta_1 d_0.
\]

This structure is not spacetime. It is a phase-support complex. Spacetime dimension, causal structure, and distance must arise later from phase response.

---

### 2.2 The phase target \(\mathcal M_\Phi = SU(2)\)

We choose
\[
\mathcal M_\Phi = SU(2).
\]

This choice is made for structural reasons, not Standard Model reasons.

The relevant properties are:

1. \(SU(2)\) is compact.
2. \(SU(2)\) is non-Abelian.
3. \(SU(2)\cong S^3\) as a manifold.
4. It admits a bi-invariant Killing metric.
5. It supports nontrivial topological sectors
   \[
   \pi_3(SU(2))\cong \mathbb Z.
   \]
6. It is the minimal non-Abelian compact Lie group capable of supporting localized finite-excess topological textures.

Let \(\{T_a\}_{a=1}^3\) be an anti-Hermitian basis of \(\mathfrak{su}(2)\), normalized by
\[
[T_a,T_b]
=
\epsilon_{abc}T_c,
\qquad
\langle T_a,T_b\rangle
=
-\frac12\operatorname{Tr}(T_aT_b)
=
\delta_{ab}.
\]

The phase field is initially defined on vertices:
\[
\Phi_i \in SU(2),
\qquad
i\in K^{(0)}.
\]
Equivalently,
\[
\Phi:K^{(0)}\to SU(2).
\]

The configuration space before quotienting is
\[
\widetilde{\mathcal C}_\Phi
=
\{\Phi:K^{(0)}\to SU(2)\}.
\]

---

### 2.3 Phase equivalence and admissible transformations

At the minimal level, Candidate I possesses a global right phase-frame action:
\[
\Phi_i
\mapsto
\Phi_i g,
\qquad
g\in SU(2).
\]
The edge phase differences defined below are invariant under global left multiplication and transform by conjugation under global right multiplication. Their norms are therefore invariant.

In the connection completion discussed later, this is enlarged to a local phase-frame action,
\[
\Phi_i
\mapsto
\Phi_i g_i,
\qquad
g_i\in SU(2),
\]
together with a corresponding transformation of phase transporters. Candidate I proper, however, does not assume local gauge invariance as a primitive. Local gauge structure must emerge from phase transport.

---

## Part III — The Candidate Phase Action

### 3.1 Edge phase difference

For each oriented edge \(e=(ij)\), define the edge phase transporter
\[
U_{ij}
=
\Phi_i^{-1}\Phi_j
\in SU(2).
\]
Define the edge phase logarithm
\[
\Omega_{ij}
=
\log U_{ij}
\in \mathfrak{su}(2),
\]
where the logarithm is taken in the principal branch except at singular phase jumps. Write
\[
\Omega_{ij}
=
\Omega_{ij}^a T_a.
\]
The norm is
\[
|\Omega_{ij}|^2
=
\delta_{ab}\Omega_{ij}^a\Omega_{ij}^b
=
-\frac12\operatorname{Tr}(\Omega_{ij}^2).
\]

This object measures the infinitesimal or finite phase mismatch between neighboring phase cells.

---

### 3.2 Gradient phase energy

The kinetic or gradient term is
\[
S_{\mathrm{grad}}[\Phi]
=
\frac{J}{2}
\sum_{(ij)\in K^{(1)}}
w_{ij}
|\Omega_{ij}|^2,
\]
where \(J>0\) is the phase stiffness and \(w_{ij}>0\) are combinatorial edge weights.

This term penalizes phase mismatch. It is the discrete analogue of
\[
\frac{J}{2}\int \langle \Phi^{-1}d\Phi,\Phi^{-1}d\Phi\rangle,
\]
but no metric on \(\mathcal X\) is assumed. The weights \(w_{ij}\) are control data, not spacetime metric components.

---

### 3.3 Phase-curvature stabilization term

The gradient term alone is insufficient to stabilize localized finite-excess textures against collapse or spreading. We therefore introduce a quartic phase-curvature term,
\[
S_{\mathrm{curv}}[\Phi]
=
\frac{\kappa}{4}
\sum_{i\in K^{(0)}}
\sum_{j,k\in \partial i}
w_{ijk}
\left|
[\Omega_{ij},\Omega_{ik}]
\right|^2,
\]
where \(\kappa>0\), \(w_{ijk}>0\), and the sum runs over pairs of edges incident at \(i\).

In a continuum approximation, this corresponds to a term of the form
\[
\frac{\kappa}{4}
\int
\left\langle
[L,L],[L,L]
\right\rangle,
\qquad
L=\Phi^{-1}d\Phi.
\]

This term is not inserted as a known physical interaction. It is the minimal nonlinear phase-curvature term capable of stabilizing localized topological phase textures.

---

### 3.4 Topological winding term

Let \(\Phi\) approach a vacuum value \(\Phi_\star\) on the effective phase boundary at infinity:
\[
\Phi
\to
\Phi_\star
\quad
\text{on}
\quad
\partial_\infty K.
\]
By global phase-frame choice, take
\[
\Phi_\star=I.
\]

A localized configuration then defines an asymptotic map
\[
\partial_\infty\Phi:
S^3_{\mathrm{phase}}
\to
SU(2),
\]
where \(S^3_{\mathrm{phase}}\) is the phase boundary surrounding the localized excess. The topological sector is
\[
Q[\Phi]
=
[\partial_\infty\Phi]
\in
\pi_3(SU(2))
\cong
\mathbb Z.
\]

In a continuum representation, the winding number is
\[
Q[\Phi]
=
\frac{1}{24\pi^2}
\int_{\Sigma}
\operatorname{Tr}
\left(
\Omega\wedge\Omega\wedge\Omega
\right),
\qquad
\Omega=\Phi^{-1}d\Phi,
\]
where \(\Sigma\) is an emergent three-dimensional phase boundary. On the combinatorial complex, \(Q[\Phi]\) is computed by a discrete degree formula using oriented geodesic simplices in \(SU(2)\).

The topological term in the action is
\[
S_{\mathrm{top}}[\Phi]
=
i\theta\,Q[\Phi],
\]
where \(\theta\) is a phase angle. This is Chern–Simons-like in the sense that it is a topological phase functional depending on phase transport rather than on a metric. It does not alter the classical equations of motion inside a fixed smooth topological sector, but it weights sectors in the phase measure and becomes physically significant when phase interference is derived.

---

### 3.5 Total candidate action

The Candidate I phase action is therefore
\[
\boxed{
S_\Phi[\Phi;\lambda]
=
\frac{J}{2}
\sum_{(ij)}
w_{ij}
|\Omega_{ij}|^2
+
\frac{\kappa}{4}
\sum_i
\sum_{j,k\in\partial i}
w_{ijk}
\left|
[\Omega_{ij},\Omega_{ik}]
\right|^2
+
i\theta\,Q[\Phi].
}
\]

The control data are
\[
\lambda
=
(J,\kappa,\theta,\{w_{ij}\},\{w_{ijk}\}).
\]

No bulk potential term is included in the primary candidate. The vacuum is selected by the finite-excess boundary condition, not by a preferred bulk potential. This avoids inserting a physical phase frame by hand.

A optional pinning regulator may be introduced for finite-volume numerical work:
\[
S_{\mathrm{pin}}[\Phi]
=
\frac{\alpha}{2}
\sum_i
|\log \Phi_i|^2,
\qquad
\alpha>0,
\]
but this is a gauge-fixing regulator, not a physical term. Physical predictions must be extracted in the limit \(\alpha\to0\) after gauge-invariant observables are computed.

---

## Part IV — The Universal Phase Equation for Candidate I

The universal phase equation is the stationarity condition
\[
\boxed{
\mathscr F_i[\Phi;\lambda]
:=
\frac{\delta S_\Phi}{\delta \Phi_i}
=
0.
}
\]

Because \(\Phi_i\in SU(2)\), variations are taken in the Lie algebra:
\[
\delta\Phi_i
=
\epsilon_i^a T_a \Phi_i,
\qquad
\epsilon_i^a\in\mathbb R.
\]

The discrete phase equation may be written formally as
\[
\mathscr F_i^a[\Phi;\lambda]
=
J\,\mathscr G_i^a[\Phi]
+
\kappa\,\mathscr C_i^a[\Phi]
=
0,
\]
where \(\mathscr G_i^a\) is the phase-gradient force and \(\mathscr C_i^a\) is the phase-curvature force. The topological term contributes only through sector weighting and boundary variations.

In a continuum approximation, with
\[
L_\mu
=
\Phi^{-1}\partial_\mu\Phi
=
L_\mu^a T_a,
\]
the phase equation takes the schematic form
\[
\boxed{
\mathscr F^a[\Phi]
=
J\,D_\mu L^{\mu a}
+
\kappa\,D_\mu
\left[
L_\nu,[L^\mu,L^\nu]
\right]^a
=
0.
}
\]
Here \(D_\mu\) is the phase-covariant derivative associated with the Maurer–Cartan structure. This is not introduced as a known field equation. It is the continuum shadow of the discrete phase stationarity condition.

---

## Part V — Vacuum Sector and Stability

### 5.1 Vacuum configuration

The vacuum sector is the constant phase configuration
\[
\Phi_i
=
I
\quad
\forall i,
\]
or more generally any globally constant configuration
\[
\Phi_i=\Phi_0.
\]
With boundary condition \(\Phi|_{\partial_\infty K}=I\), the representative vacuum is
\[
\Phi_\star=I.
\]

For this configuration,
\[
U_{ij}=I,
\qquad
\Omega_{ij}=0,
\qquad
[\Omega_{ij},\Omega_{ik}]=0,
\qquad
Q=0.
\]
Thus
\[
S_\Phi[\Phi_\star]=0.
\]

---

### 5.2 Quadratic stability operator

Expand near the vacuum:
\[
\Phi_i
=
\exp(\phi_i^a T_a)
\approx
I+\phi_i^aT_a.
\]
Then
\[
\Omega_{ij}^a
\approx
\phi_j^a-\phi_i^a.
\]
The quadratic action is
\[
S_\Phi^{(2)}
=
\frac{J}{2}
\sum_{(ij)}
w_{ij}
(\phi_j^a-\phi_i^a)^2
+
O(\phi^4).
\]
The quartic curvature term contributes only at higher order near the vacuum.

The stability operator is therefore
\[
\boxed{
(\mathscr L_{\Phi_\star})_{ij}^{ab}
=
J\,\delta^{ab}\,(\Delta_0)_{ij},
}
\]
with Dirichlet boundary conditions if the finite-excess sector is imposed.

The spectrum is
\[
\sigma(\mathscr L_{\Phi_\star})
=
J\,\sigma(\Delta_0),
\]
with multiplicity three. For a connected complex with Dirichlet boundary, the lowest eigenvalue is strictly positive:
\[
\lambda_0>0.
\]
Therefore the vacuum is a strict local minimum of the phase action in the finite-excess sector.

---

### 5.3 Susceptibility

Away from zero modes, the phase susceptibility is
\[
\boxed{
\boldsymbol\chi_{\Phi_\star}
=
\mathscr L_{\Phi_\star}^{-1}
=
\frac{1}{J}\Delta_0^{-1}\otimes \mathbf 1_3.
}
\]

This Green operator measures the phase response to localized perturbations. It will be used below to construct the emergent response geometry.

---

## Part VI — Bifurcation and Critical Phase Directions

Although Candidate I contains no bulk potential, criticality can arise in several ways:

1. Vanishing stiffness:
   \[
   J\to0.
   \]
2. Loss of connectivity in the phase complex.
3. Appearance of collective zero modes around nontrivial defect solutions.
4. Introduction of a pinning regulator \(\alpha\) and taking \(\alpha\to0\).

If a pinning regulator is used,
\[
S_{\mathrm{pin}}
=
\frac{\alpha}{2}
\sum_i|\phi_i|^2,
\]
then the vacuum stability operator becomes
\[
\mathscr L_{\Phi_\star}
=
J\Delta_0+\alpha I.
\]
The bifurcation operator is
\[
\boxed{
\Delta_\Phi(\alpha)
=
\operatorname{Det}'
\left(
J\Delta_0+\alpha I
\right)^3.
}
\]
The prime indicates omission of boundary-fixed or gauge-frame zero directions.

The critical manifold is
\[
\Sigma_\Phi
=
\{\alpha=0\}
\]
in the regulator-augmented model. At \(\alpha=0\), constant global phase rotations become zero modes. The kernel is
\[
\ker\mathscr L_{\Phi_\star}
\cong
\mathfrak{su}(2),
\]
with dimension three.

Lyapunov–Schmidt reduction then gives order parameters
\[
\eta^a
\]
corresponding to global phase orientation. The reduced potential is generated by nonlinearities and boundary effects. In the unpinned candidate, these directions are pure phase-frame directions and are quotiented out.

---

## Part VII — Topological Sector Separation

Let \(\Phi_Q\) be a finite-excess configuration satisfying
\[
\Phi_Q
\to
I
\quad
\text{on}
\quad
\partial_\infty K.
\]
Its sector label is
\[
Q[\Phi_Q]
\in
\pi_3(SU(2))
\cong
\mathbb Z.
\]

### Proposition 1 — Topological separation

Let \(\mathcal C_{\mathrm{fin}}\) be the space of finite-excess configurations obeying the vacuum boundary condition. If
\[
Q[\Phi_Q]\neq0,
\]
then there is no continuous path
\[
\Phi_s\in\mathcal C_{\mathrm{fin}},
\qquad
s\in[0,1],
\]
such that
\[
\Phi_0=\Phi_Q,
\qquad
\Phi_1=\Phi_\star.
\]

**Proof.** A continuous path in \(\mathcal C_{\mathrm{fin}}\) induces a homotopy of the asymptotic boundary maps
\[
\partial_\infty\Phi_s:S^3_{\mathrm{phase}}\to SU(2).
\]
Homotopic maps define the same element of \(\pi_3(SU(2))\). Since \(Q[\Phi_Q]\neq0\) while \(Q[\Phi_\star]=0\), no such homotopy exists. \(\square\)

Thus Candidate I automatically contains discrete superselection sectors labeled by \(Q\).

---

## Part VIII — Finite Excess and Normal Stability

Define the real phase excess functional
\[
\mathcal E_\Phi[\Phi]
=
S_{\mathrm{grad}}[\Phi]
+
S_{\mathrm{curv}}[\Phi].
\]
Relative to the vacuum,
\[
\mathcal E_\Phi[\Phi_Q\mid\Phi_\star]
=
\mathcal E_\Phi[\Phi_Q]
-
\mathcal E_\Phi[\Phi_\star].
\]

A candidate particle sector must satisfy
\[
\boxed{
0<
\mathcal E_\Phi[\Phi_Q\mid\Phi_\star]
<
\infty.
}
\]

The gradient term penalizes phase variation; the curvature term prevents collapse of localized textures. In the continuum analogue, the topological degree supplies a lower bound of the form
\[
\mathcal E_\Phi[\Phi_Q]
\ge
C\,\sqrt{J\kappa}\,|Q|,
\]
up to model-dependent constants and boundary corrections. The discrete candidate is expected to admit an analogous bound provided the combinatorial weights are uniformly bounded and the complex is refined consistently.

Let \(\mathcal Z_Q\) denote the tangent space generated by collective phase-frame and positional moduli. Let \(N_Q\) be the normal complement. The projected stability operator is
\[
\boxed{
\mathscr L_Q^\perp
=
\Pi_{N_Q}
\mathscr L_{\Phi_Q}
\Pi_{N_Q}.
}
\]

Normal stability requires
\[
\ker\mathscr L_Q^\perp=\{0\},
\]
and
\[
\langle \zeta,\mathscr L_Q^\perp\zeta\rangle_\Phi
\ge
\kappa_Q
\|\zeta\|_\Phi^2,
\qquad
\kappa_Q>0,
\]
for all normal perturbations \(\zeta\in N_Q\).

Candidate I does not yet prove this condition analytically. It defines it as a computable requirement.

---

## Part IX — Emergence of Particle Sectors

We now apply the UPT particle emergence theorem.

### Theorem 1 — Candidate particle sectors in Candidate I

Suppose there exists a configuration \(\Phi_Q\) such that:

1. **Admissibility**
   \[
   \mathscr F[\Phi_Q;\lambda]=0.
   \]
2. **Finite excess**
   \[
   0<
   \mathcal E_\Phi[\Phi_Q\mid\Phi_\star]
   <
   \infty.
   \]
3. **Nontrivial sector**
   \[
   Q[\Phi_Q]\neq0.
   \]
4. **Normal stability**
   \[
   \mathscr L_Q^\perp>0.
   \]
5. **Localization**
   The invariant excess density concentrates within finite response distance.
6. **Transportability**
   The solution family possesses collective moduli allowing controlled displacement.

Then
\[
\boxed{
\mathfrak P_Q
=
[\Phi_Q]_{\mathscr G_\Phi}
}
\]
is a UPT particle sector: a stable, localizable, transportable, observationally distinguishable phase-sector object.

**Proof.** Conditions 1–3 establish an admissible nonvacuum phase branch separated from the vacuum by an integer topological invariant. Condition 4 gives persistence under normal perturbations. Condition 5 defines localization in the response geometry constructed below. Condition 6 permits collective propagation. Quotienting by phase-frame redundancy removes unobservable representatives. The resulting orbit has the structural content of a particle. \(\square\)

Candidate I therefore reduces the particle problem to a concrete computational task: find stable finite-action minimizers in fixed topological sectors \(Q\).

---

## Part X — Emergent Response Geometry

### 10.1 Control couplings

Let \(\lambda^i\) denote local control variables. In Candidate I, natural controls include:

1. Edge weights \(w_{ij}\).
2. Curvature weights \(w_{ijk}\).
3. Local stiffness variations \(J_i\).
4. Boundary or source couplings.

Let \(\eta^a\) denote collective coordinates of a phase sector. These may include:

1. Position moduli.
2. Global phase orientation moduli.
3. Internal shape moduli.
4. Sector size moduli, if present.

Define the control-coupling tensor
\[
T_{ia}
=
\frac{\partial^2 S_\Phi}
{\partial\lambda^i\partial\eta^a}.
\]

The stability tensor is
\[
S_{ab}
=
\frac{\partial^2 S_{\mathrm{eff}}}
{\partial\eta^a\partial\eta^b},
\]
and the susceptibility is
\[
\chi^{ab}
=
(S^{-1})^{ab}
\]
on the normal slice.

The UPT response metric is then
\[
\boxed{
g^\Phi_{ij}
=
T_{ia}\chi^{ab}T_{jb}.
}
\]

For the vacuum sector, where the collective coordinates are removed or fixed, one may instead define a field-susceptibility metric directly from the Green operator:
\[
G_{ij}^{\Phi}
\sim
\frac{\delta\langle O_i\rangle}{\delta\lambda^j},
\]
where \(O_i\) are local phase observables.

---

### 10.2 Phase distance

Given the response metric, define phase distance between two control configurations by
\[
D_\Phi(\lambda_1,\lambda_2)
=
\inf_\gamma
\int_\gamma
\sqrt{
g^\Phi_{ij}
\,d\lambda^i d\lambda^j
}.
\]

A phase defect is localized if its invariant excess density \(\varepsilon_Q\) satisfies
\[
\int_{D_\Phi(x,X_Q)>R}
|\varepsilon_Q(x)|
\,d\mu_{g^\Phi}
\to
0
\quad
\text{as}
\quad
R\to\infty.
\]

This is the UPT localization criterion. Location is not a primitive coordinate of \(\mathcal X\). It is an emergent collective property of the phase configuration.

---

### 10.3 Signature problem

In the present candidate, the combinatorial weights and the quadratic phase action produce a positive-definite response metric at the vacuum:
\[
g^\Phi_{ij}
\succ
0.
\]
Therefore Candidate I naturally yields a Euclidean-type response geometry.

A Lorentzian signature
\[
(-,+,+,+)
\]
is not derived. This is a direct consequence of the candidate’s structure. To recover spacetime, Candidate I must be augmented by a phase-propagation operator
\[
\mathscr P_\Phi
\]
whose principal symbol develops an indefinite effective signature. Candidate I does not yet provide this.

Thus Candidate I passes the geometry-construction requirement but fails the Lorentzian-spacetime requirement.

---

## Part XI — Phase Transport and Gauge Structure

### 11.1 Edge transport as phase connection

The edge object
\[
U_{ij}
=
\Phi_i^{-1}\Phi_j
\]
is the primitive phase comparator. Under a local phase-frame change, if introduced, it transforms as
\[
U_{ij}
\mapsto
g_i^{-1}U_{ij}g_j.
\]
This is precisely the transformation law of a discrete connection.

Define the phase connection one-cochain
\[
A_{ij}
=
\Omega_{ij}
=
\log U_{ij}.
\]
For configurations arising from a single-valued phase field on a contractible region, this connection is flat:
\[
F_{ijk}
=
U_{ij}U_{jk}U_{ki}
=
I.
\]
Nontrivial curvature arises when:

1. The phase field has singular defect cores.
2. The phase bundle is topologically nontrivial.
3. The connection completion promotes \(U_{ij}\) to an independent phase transporter.

The curvature around a plaquette \(p\) is
\[
F_p
=
\prod_{e\in\partial p}U_e.
\]
Its infinitesimal form is
\[
F_{\mu\nu}
=
\partial_\mu A_\nu
-
\partial_\nu A_\mu
+
[A_\mu,A_\nu].
\]

Thus Candidate I realizes the UPT principle:
\[
\boxed{
\text{gauge curvature}
=
\text{nontrivial phase transport}.
}
\]

---

### 11.2 Connection completion

Candidate I may be extended to a connection completion by taking phase transporters \(U_{ij}\) as independent variables modulo local phase-frame transformations:
\[
U_{ij}
\mapsto
g_i^{-1}U_{ij}g_j.
\]

The connection action can include a curvature term,
\[
S_{\mathrm{conn}}
=
\frac{1}{2g_\Phi^2}
\sum_{p}
w_p
|\log F_p|^2,
\]
and a Chern–Simons-like topological term on three-dimensional phase subcomplexes,
\[
S_{\mathrm{CS}}
=
\frac{k}{4\pi}
\sum_{t}
\operatorname{CS}_t(A),
\]
where locally
\[
\operatorname{CS}(A)
=
\operatorname{Tr}
\left(
A\wedge dA
+
\frac23 A\wedge A\wedge A
\right).
\]

This completion is not yet required for the particle-sector mechanism, but it is the natural route to dynamical gauge curvature.

---

### 11.3 Gauge-group consequence

The phase-frame group of Candidate I is
\[
\mathscr G_\Phi = SU(2).
\]

This is not the Standard Model gauge group. Candidate I does not produce
\[
SU(3)\times SU(2)\times U(1)
\]
from phase topology or vacuum stabilizer structure. To declare the \(SU(2)\) of Candidate I to be the weak \(SU(2)\) would be an insertion and is forbidden.

Therefore Candidate I demonstrates the mechanism of gauge emergence but fails the observed-gauge-group criterion.

---

## Part XII — Discreteness, Spectrum, and Mass

### 12.1 Discrete topological sectors

Candidate I possesses discrete sectors
\[
Q\in\mathbb Z.
\]
These sectors are not inserted as particle labels. They arise from the topology of the phase target:
\[
\pi_3(SU(2))\cong\mathbb Z.
\]

Thus discreteness appears before quantization. It is structural, not Hilbert-space-imposed.

---

### 12.2 Normal-mode spectrum

Around a stable defect \(\Phi_Q\), normal perturbations satisfy
\[
\mathscr L_Q^\perp u_n
=
\omega_n^2
\mathscr W_Q u_n,
\]
where \(\mathscr W_Q\) is the emergent dynamical weight determined by the quadratic phase action.

If the normal spectrum contains isolated eigenvalues below a continuum threshold,
\[
0<\omega_1^2\le\omega_2^2\le\cdots<\omega_{\mathrm{cont}}^2,
\]
then the sector \(\mathfrak P_Q\) possesses discrete internal excitations.

Candidate I predicts that such internal modes, if present, are determined by:

1. The topological sector \(Q\).
2. The stiffness ratio \(\kappa/J\).
3. The topological angle \(\theta\).
4. The combinatorial universality class of \(K\).

---

### 12.3 Mass after emergent relativistic phase

Candidate I does not yet derive a relativistic causal speed \(c_\Phi\). If a Lorentzian phase regime is later obtained, the rest mass of sector \(Q\) is defined by
\[
\boxed{
m_Q
=
\frac{
\mathcal E_\Phi[\Phi_Q]
-
\mathcal E_\Phi[\Phi_\star]
}{
c_\Phi^2
}.
}
\]

Until \(c_\Phi\) is derived, the quantity computed by Candidate I is a phase excess, not a physical mass.

---

## Part XIII — Audit Against UPT Falsifiability Criteria A–F

We now evaluate Candidate I against the falsifiability criteria stated in the UPT particle-sector preprint.

---

### Criterion A — Existence

**Requirement.** There must exist at least one explicitly specified \(\mathscr F\) and a solution \(\Phi_q\) for which the full particle-sector conditions can be verified.

**Candidate I status.** Candidate I supplies an explicit action and phase equation. The vacuum solution is explicit. Nontrivial topological sectors are well defined. Existence of stable finite-excess minimizers in \(Q\neq0\) sectors is expected from the continuum Skyrme-type structure but is not analytically proven here.

**Verdict.** Actionable. Requires numerical verification.

---

### Criterion B — Spectrum

**Requirement.** The stable quotient solution space must produce discrete sectors with calculated, not fitted, invariant data.

**Candidate I status.** The topological sector label
\[
Q\in\mathbb Z
\]
is derived from phase topology. Internal normal modes are defined by the projected stability operator. Their numerical values remain to be computed.

**Verdict.** Mechanism present. Explicit spectrum not yet computed.

---

### Criterion C — Geometry

**Requirement.** The response metric must yield the observed low-energy causal signature and free propagation law as a phase-geometric limit.

**Candidate I status.** The response metric
\[
g^\Phi_{ij}=T_{ia}\chi^{ab}T_{jb}
\]
is constructed from phase susceptibility. However, the candidate naturally yields a positive-definite response geometry. Lorentzian signature is not derived. The effective dimension is also not yet derived independently of the combinatorial complex.

**Verdict.** Fails as a final spacetime derivation. Passes as a concrete response-geometry construction.

---

### Criterion D — Gauge structure

**Requirement.** The observed internal gauge group and its matter representations must arise from phase-frame topology, stabilizers, or holonomy rather than be placed into the phase bundle by declaration.

**Candidate I status.** The phase-frame group is \(SU(2)\). This is a minimal non-Abelian test choice, not the Standard Model gauge group. Candidate I does not derive
\[
SU(3)\times SU(2)\times U(1).
\]
Any identification of the Candidate I \(SU(2)\) with weak isospin would be an insertion.

**Verdict.** Fails as a final gauge derivation. Passes as a mechanism demonstration.

---

### Criterion E — Quantum structure

**Requirement.** A phase-derived measure and quantization map must reproduce interference and observed transition statistics without imposing the Born rule.

**Candidate I status.** Candidate I contains a topological angle \(\theta\) and sector weighting \(e^{i\theta Q}\), but it does not derive a Hilbert space, a phase symplectic form, an intrinsic action period \(\hbar_\Phi\), or the Born measure.

**Verdict.** Not satisfied.

---

### Criterion F — Novel prediction

**Requirement.** The same \(\mathscr F\) must generate a new quantitative spectral, scattering, topological-defect, or scale-dependence prediction that can be wrong.

**Candidate I status.** Candidate I generates several internal predictions:

1. Stable \(Q\in\mathbb Z\) sectors exist only above a critical stabilization ratio \(\kappa/J\).
2. The sector excess scales as
   \[
   \mathcal E_Q
   =
   \sqrt{J\kappa}\,
   F_Q\!\left(\theta,\frac{\kappa}{J},K\right)
   \]
   in the continuum limit.
3. The \(Q=1\) sector, if stable, possesses collective zero modes corresponding to phase translation and phase rotation.
4. The topological angle is periodic:
   \[
   \theta\sim\theta+2\pi.
   \]
5. Sector interference depends on \(\Delta Q\) through \(e^{i\theta\Delta Q}\).

These are falsifiable within the model.

**Verdict.** Satisfied at the internal-model level.

---

## Part XIV — Consequences of the Candidate Choices

### 14.1 Consequence of choosing a combinatorial base

Choosing \(\mathcal X\) as a finite cell complex allows computation without assuming spacetime. However, if the complex is constructed with four-dimensional cells and the resulting effective dimension is then declared to be four, the derivation is contaminated.

Therefore the correct test is:

\[
d_{\mathrm{eff}}
\stackrel{?}{=}
d_{\mathrm{spectral}}[g^\Phi]
\]
not the topological dimension of \(K\).

Candidate I must be tested under complexes with no preferred four-dimensional structure. If \(d_{\mathrm{eff}}=4\) emerges only when a four-complex is inserted, Candidate I fails the dimension-derivation requirement.

---

### 14.2 Consequence of choosing \(SU(2)\)

The choice \(SU(2)\) gives:

1. Non-Abelian phase transport.
2. Integer topological sectors.
3. A minimal setting for stable textures.
4. A simple Lie-algebraic computational structure.

But it cannot yield color, hypercharge, or three generations. It is therefore structurally insufficient as a final candidate.

This is not a defect of the UPT method. It is a necessary no-go result for the minimal candidate.

---

### 14.3 Consequence of omitting a bulk potential

Omitting a bulk potential avoids inserting a preferred absolute phase. The vacuum is selected by boundary class. This preserves phase-relational ontology.

The cost is that strict isolation of the vacuum inside the bulk is weaker. Numerical work may require a pinning regulator. If a physical vacuum-selection mechanism is required, it must later arise from phase dynamics, not from an inserted potential tuned to known physics.

---

### 14.4 Consequence of the quartic curvature term

The quartic phase-curvature term is essential for stabilization. Without it, localized textures are susceptible to scaling instabilities. With it, finite-size stable sectors become possible.

This term is therefore not optional if Candidate I is to produce particle-like localized sectors.

---

### 14.5 Consequence of the topological term

The topological term does not change smooth local equations inside a fixed sector, but it creates a phase-memory structure across sectors. It is the first seed of phase interference. It does not yet produce quantum probability, but it supplies the sector-dependent phase needed for later interference.

---

## Part XV — Computational Protocol

Candidate I is designed for direct computation.

### Step 1 — Construct the phase complex

Choose a sequence of finite oriented complexes \(K_L\) with increasing size \(L\). Do not embed them in a metric spacetime. Use only incidence and weights.

### Step 2 — Initialize sector \(Q\)

Construct an initial configuration \(\Phi^{(0)}_Q\) with prescribed degree \(Q\). For \(Q=1\), a phase hedgehog may be used as an initial guess.

### Step 3 — Gradient flow

Evolve
\[
\Phi_i^{-1}\dot\Phi_i
=
-\mathscr F_i[\Phi;\lambda]
\]
while preserving the topological sector.

### Step 4 — Minimize

Find a stationary configuration
\[
\mathscr F_i[\Phi_Q]=0.
\]

### Step 5 — Compute the Hessian

Construct
\[
\mathscr L_{\Phi_Q}
=
D_\Phi\mathscr F[\Phi_Q].
\]
Project out collective zero modes and compute the normal spectrum.

### Step 6 — Verify normal stability

Check
\[
\mathscr L_Q^\perp>0.
\]

### Step 7 — Compute response geometry

Vary control parameters \(\lambda^i\) and compute
\[
T_{ia},
\qquad
\chi^{ab},
\qquad
g^\Phi_{ij}.
\]

### Step 8 — Extract scaling

Refine \(K_L\) and test whether
\[
\mathcal E_Q/\sqrt{J\kappa}
\]
approves a finite universal function.

---

## Part XVI — Candidate Predictions

Candidate I yields the following concrete predictions.

### Prediction 1 — Critical stabilization

There exists a critical ratio
\[
\left(\frac{\kappa}{J}\right)_c
\]
such that stable localized \(Q=1\) solutions exist only when
\[
\frac{\kappa}{J}
>
\left(\frac{\kappa}{J}\right)_c.
\]

### Prediction 2 — Integer sector tower

If \(Q=1\) is stable, then sectors with all integer \(Q\) are structurally permitted, though not necessarily all energetically stable.

### Prediction 3 — Universal scaling

In the continuum limit,
\[
\mathcal E_Q
=
\sqrt{J\kappa}\,
F_Q\!\left(\theta,\frac{\kappa}{J}\right)
+
o(1),
\]
independent of microscopic combinatorial details.

### Prediction 4 — Zero-mode count

The \(Q=1\) sector, when stable in an emergent translational regime, possesses collective zero modes associated with phase position and phase orientation.

### Prediction 5 — Topological-angle periodicity

Physical sector interference is invariant under
\[
\theta\to\theta+2\pi.
\]

---

## Part XVII — What Candidate I Does Not Derive

Candidate I does not derive:

1. The observed spacetime dimension.
2. Lorentzian signature.
3. Einstein gravity.
4. The Standard Model gauge group.
5. Three fermion generations.
6. Electric charge quantization.
7. The mass spectrum.
8. The Born rule.
9. A physical value of \(\hbar\).
10. A physical value of \(c\).

These omissions are not incidental. They define the next derivational burdens.

---

## Part XVIII — Relation to the Full UPT Program

Candidate I is a concrete realization of the following fragment of UPT:

\[
\Phi
\rightarrow
\text{phase topology}
\rightarrow
\text{finite excess}
\rightarrow
\text{stable sector}
\rightarrow
\text{particle candidate}.
\]

It does not yet realize the full hierarchy:

\[
\Phi
\rightarrow
\text{topology}
\rightarrow
\text{geometry}
\rightarrow
\text{connections}
\rightarrow
\text{fields}
\rightarrow
\text{particles}
\rightarrow
\text{observables}.
\]

The missing links are:

1. Derivation of Lorentzian geometry from phase propagation.
2. Derivation of the observed gauge group from vacuum stabilizer and holonomy.
3. Derivation of quantum measure from phase structure.
4. Derivation of gravitational dynamics from phase response.

Candidate I is therefore the first computable entry point into the full program.

---

## Part XIX — Necessary Next Candidate

The failure modes of Candidate I determine the requirements for Candidate II.

Candidate II must possess:

1. A phase target rich enough to produce multiple residual symmetry factors.
2. A vacuum stabilizer whose centralizer is computed, not chosen to match the Standard Model.
3. Topological sectors capable of supporting localized finite-excess particles.
4. A phase-propagation operator capable of yielding indefinite causal signature.
5. A connection completion in which curvature is dynamical.
6. A scale-dependence mechanism capable of producing infrared universality.

A tempting but forbidden construction would be to choose a target because its automorphism group already contains
\[
SU(3)\times SU(2)\times U(1).
\]
That would reverse-engineer the answer.

The correct next step is to choose Candidate II from a classification principle internal to phase structure, such as:

1. Minimal rank required for stable sector separation.
2. Minimal homotopy required for discrete charge.
3. Minimal holonomy required for spinorial transport.
4. Minimal critical-kernel dimension required for emergent four-dimensional response.

Until such a principle is specified and tested, Candidate I remains the first honest instantiation.

---

## Part XX — Conclusion

We have proposed the first concrete candidate instantiation of the universal phase equation. The candidate is defined by the UPT datum
\[
\mathfrak U
=
(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\lambda),
\]
with
\[
\mathcal X
=
\text{finite oriented combinatorial phase complex},
\]
\[
\mathcal M_\Phi
=
SU(2),
\]
and
\[
S_\Phi[\Phi;\lambda]
=
S_{\mathrm{grad}}[\Phi]
+
S_{\mathrm{curv}}[\Phi]
+
i\theta Q[\Phi].
\]

The resulting universal phase equation is
\[
\mathscr F[\Phi;\lambda]
=
\frac{\delta S_\Phi}{\delta\Phi}
=
0.
\]

The stability operator is
\[
\mathscr L_\Phi
=
D_\Phi\mathscr F.
\]

The bifurcation operator is
\[
\Delta_\Phi
=
\operatorname{Det}_\Phi(\mathscr L_\Phi).
\]

The susceptibility is
\[
\boldsymbol\chi_\Phi
=
\mathscr L_\Phi^{-1}
\]
on the normal slice.

The candidate yields:

1. A stable vacuum sector.
2. Integer topological sectors \(Q\in\mathbb Z\).
3. Finite-excess localized phase configurations.
4. A particle-sector object
   \[
   \mathfrak P_Q=[\Phi_Q]_{\mathscr G_\Phi}.
   \]
5. A response geometry constructed from phase susceptibility.
6. A phase-transport connection.
7. Falsifiable scaling and stability predictions.

It does not yield the observed gauge group, Lorentzian spacetime, quantum probability, or Einstein gravity. It is therefore not the final universal phase equation. It is the first concrete candidate against which the UPT program can be computationally tested.

The decisive next step is numerical and analytical execution of Candidate I:

\[
\boxed{
\text{Specify }K,
\quad
\text{minimize }S_\Phi,
\quad
\text{verify stable }Q\neq0,
\quad
\text{compute }g^\Phi,
\quad
\text{test scaling}.
}
\]

If Candidate I fails, UPT must be revised. If Candidate I succeeds mechanically but fails physically, the no-go result directs the construction of Candidate II. In either case, Universal Phase Theory has now crossed from formal architecture to concrete falsifiable instantiation.

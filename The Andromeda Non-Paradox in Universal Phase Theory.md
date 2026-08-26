# The Andromeda Non-Paradox in Universal Phase Theory

## Phase-Covariant Emergence, Relational Observability, and the Non-Bifurcation of Distant Events

**White Paper / Foundational Preprint**  
**Dust LLC — Universal Phase Theory Series**  
**August 2026**

---

## Abstract

The Andromeda construction, associated with the Rietdijk–Putnam–Penrose family of arguments, begins from the relativistic fact that two observers meeting locally but possessing distinct velocities assign distinct spacelike simultaneity sections to a distant system. Applied to the Andromeda galaxy, the separation of those sections is macroscopically large despite the observers’ minute relative motion. The construction is then commonly taken to produce a contradiction: one observer’s present contains an Andromedean decision to launch a fleet, while the other observer’s present contains a period before that decision. The proposed contradiction depends on treating the observer-indexed membership of a spacelike synchronization section as an invariant physical property of a remote phase configuration.

This paper derives the **Andromeda Non-Paradox** within Universal Phase Theory (UPT). The derivation begins with the universal phase equation \(\mathscr F[\Phi;\lambda]=0\), its stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\), bifurcation operator \(\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi)\), and susceptibility \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\) on the physical phase quotient. Geometry emerges from the phase-response tensor \(g^\Phi_{\mu\nu}=T_{\mu a}\overline\chi^{ab}_\Phi T_{\nu b}\); phase comparison is governed by a derived connection \(D_\mu=\partial_\mu+A_\mu[\Phi]\); and causal accessibility is determined by the characteristic set of the phase propagation operator \(\mathscr P_\Phi\). In a stable Lorentzian phase sector, a change of inertial observer is shown to be a change of local phase frame and observer-indexed synchrony section, not a transition between distinct physical phase histories.

Three formal results are established. First, observer re-slicing preserves the physical phase orbit and every gauge-invariant relational observable. Second, the physical stability spectrum, bifurcation locus, Lyapunov–Schmidt reduced branch structure, topological charge, and holonomy conjugacy class are invariant under such a re-slicing. Third, the domain of dependence of \(\mathscr P_\Phi\) excludes any spacelike observer operation from altering a remote local phase observable. The remote events selected by two simultaneity sections are different events; the apparent inconsistency is the illicit removal of the observer index followed by their identification. Accordingly, the Andromeda construction does not demonstrate observer-created futures, remote phase selection, or determinism. It demonstrates only the frame dependence of a non-observable synchrony predicate.

The paper also identifies the non-negotiable UPT derivation obligations: a concrete \(\mathscr F\) must yield a stable Lorentzian response metric, an infrared Lorentz covariance class, and a hyperbolic propagation operator. A preferred global phase clock, if present, must arise as a gauge-invariant dynamical order parameter and is not permitted as an inserted repair. These requirements define direct falsifiability criteria for any UPT realization.

**Keywords:** Universal Phase Theory; Andromeda paradox; relativity of simultaneity; emergent spacetime; phase transport; bifurcation theory; Lyapunov–Schmidt reduction; phase holonomy; causal propagation; relational observables.

---

## 1. Statement of the Problem

The Andromeda construction is a sharpened instance of relativity of simultaneity. Two observers meet at an Earth event \(p\) and are assigned slightly different instantaneous velocities along the Earth–Andromeda axis. Each observer extends an inertial simultaneity section from \(p\) toward a distant Andromedean world-tube. Because the sections are distinct, they intersect that world-tube at distinct events. One section may intersect before a hypothetical command decision, while the other intersects after it. Penrose’s formulation expresses this in terms of an Andromedean fleet whose launch is assigned to one observer’s past and the other’s future.[3]

The special-relativistic calculation itself is elementary. What requires analysis is the ontological inference. Standard relativity establishes that distant simultaneity is frame-relative; it does not identify an observer’s simultaneity assignment with a local intervention into the distant system.[2] The classical Rietdijk–Putnam inference instead promotes the fact that some distant observer can count an event as past into an inference about fixed global existence or determinism.[4] That extrapolation has been extensively contested at the level of physical interpretation and metaphysics.[5] [6]

UPT reformulates the issue at the correct structural level. Its primitive object is not a pre-given spacetime event manifold, an absolute clock, or a local observer’s psychological present. It is a phase configuration \(\Phi\) satisfying a universal admissibility equation. Spacetime geometry, transport, field content, localized excitations, and observables are successive derived strata:

\[
\boxed{
\Phi
\longrightarrow
\text{topology}
\longrightarrow
\text{geometry}
\longrightarrow
\text{connections}
\longrightarrow
\text{fields}
\longrightarrow
\text{particles}
\longrightarrow
\text{observables}.
}
\]

The Andromeda Non-Paradox is the theorem that follows when this hierarchy is respected. The observer’s synchrony section belongs to the representational layer generated by a local temporal phase frame. It does not belong to the invariant observable layer and therefore cannot create, erase, bifurcate, or select a remote physical phase branch.

![Figure 1. UPT architecture of the Andromeda Non-Paradox: distinct observer-indexed simultaneity sections select distinct remote events while phase-orbit invariance, stability invariance, relational transport, and causal propagation exclude a contradiction.](https://private-us-east-1.manuscdn.com/sessionFile/Tiy5vGVHZsndCnNgwKv3Pk/sandbox/h7uPtDZvI0z1L03ebFBqjh-images_1787732456142_na1fn_L2hvbWUvdWJ1bnR1L2FuZHJvbWVkYV9ub25fcGFyYWRveF9zY2hlbWF0aWM.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvVGl5NXZHVkhac25kQ25OZ3dLdjNQay9zYW5kYm94L2g3dVB0RFp2STB6MUwwM2ViRkJxamgtaW1hZ2VzXzE3ODc3MzI0NTYxNDJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyRnVaSEp2YldWa1lWOXViMjVmY0dGeVlXUnZlRjl6WTJobGJXRjBhV00ucG5nIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzg5NDMwNDAwfX19XX0_&Key-Pair-Id=K2QY5QTL8JSY6C&Signature=MEUCIQDe7H5QKosFpiH6r1R7KWuDvJb4uJYtLXuDc-2tVMN5SAIgMiAvTTFbChMjJTdZtV~HTxz3sK9yv2USQ83euq7ruEQ_)

*Figure 1. The resolution is architectural: a local phase-frame change generates a different synchrony section, not a different physical phase history.*

> **Andromeda Non-Paradox.** In a UPT phase sector with emergent Lorentzian geometry, covariant phase transport, and hyperbolic phase propagation, two observers’ distinct simultaneity sections select distinct remote events without inducing distinct remote phase histories. The difference is an observer-indexed relational assignment, not a contradiction in the physical phase orbit.

The remainder of this paper proves that statement and specifies the conditions under which it is a genuine UPT consequence rather than an assumption placed into the theory.

| Layer | UPT object | Role in the present derivation |
|---|---|---|
| Fundamental configuration | \(\Phi\in\Gamma(E_\Phi)\) | Universal phase field |
| Admissibility | \(\mathscr F[\Phi;\lambda]=0\) | Selects physical phase histories |
| Stability | \(\mathscr L_\Phi=D_\Phi\mathscr F\) | Detects physical critical directions |
| Transition | \(\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi)\) | Locates true phase bifurcations |
| Response | \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\) | Generates metric response away from criticality |
| Geometry | \(g^\Phi_{\mu\nu}\) | Defines emergent local causal classification |
| Transport | \(D_\mu=\partial_\mu+A_\mu[\Phi]\) | Compares phases at separated locations |
| Observability | \(\mathfrak{Obs}_\Phi\) | Excludes bare synchrony labels from physical observables |

---

## 2. The Kinematical Andromeda Construction

Let \(p\) be the Earth encounter event and let the local effective geometry be approximately Minkowskian in a neighborhood containing the tangent data of the two observers. Observer \(A\) adopts coordinates \((t_A,x_A)\) in which \(p=(0,0)\), while observer \(B\) moves with infinitesimal velocity \(v\) in the positive \(x\)-direction. The effective Lorentz transformation is

\[
t_B=\gamma\left(t_A-\frac{v x_A}{c^2}\right),
\qquad
x_B=\gamma(x_A-vt_A),
\qquad
\gamma=(1-v^2/c^2)^{-1/2}.
\]

Choose an Andromedean world-tube with coordinate distance \(L\) in the relevant local direction. The event \(q_A\) selected by \(A\)’s simultaneity section satisfies

\[
q_A=(t_A=0,x_A=L).
\]

The event \(q_B\) selected by \(B\)’s section satisfies \(t_B(q_B)=0\). Hence

\[
0=\gamma\left(t_A(q_B)-\frac{vL}{c^2}\right),
\qquad
\boxed{t_A(q_B)=\frac{vL}{c^2}}.
\]

The separation between the two selected events is therefore

\[
\boxed{\delta t_{BA}=\frac{vL}{c^2}}.
\]

For a representative Earth–Andromeda distance of \(2.5\times10^6\) light-years, a relative velocity of \(1\,\mathrm{m\,s^{-1}}\) yields \(|\delta t|\approx2.63162\times10^5\,\mathrm{s}\approx3.046\) days.[7] The large numerical value is a kinematic amplification by distance; it is not a transmission time, a causal influence, or an alteration of any Andromedean state.

The conceptual failure occurs when the following two propositions are replaced by a single unindexed proposition:

\[
\mathsf N_A(p,q_A)=1,
\qquad
\mathsf N_B(p,q_B)=1,
\qquad
q_A\neq q_B.
\]

Here \(\mathsf N_A(p,q)=1\) means only that \(q\) lies on observer \(A\)’s synchrony section through \(p\). The construction becomes paradoxical only after erasing the subscripts and treating \(q_A\) and \(q_B\) as incompatible descriptions of the same remote event. UPT makes the index structure fundamental rather than tacit.

---

## 3. Universal Phase Space and the Physical Quotient

Let

\[
\pi_\Phi:E_\Phi\rightarrow\mathcal X
\]

be a phase bundle over a generalized substrate \(\mathcal X\), which is not assumed to be spacetime. A phase configuration is a section

\[
\Phi\in\mathcal C_\Phi:=\Gamma(E_\Phi).
\]

The phase configuration is admissible when it satisfies the universal phase equation

\[
\boxed{\mathscr F[\Phi;\lambda]=0,}
\]

where \(\lambda\) denotes control data, boundary data, scale data, conserved quantities, or environmental couplings. The equation is the primitive structural law. Neither a Lorentzian metric, an observer foliation, a global time function, nor a particle ontology enters at this stage.

Let \(\mathscr G_\Phi\) be the groupoid of admissible phase transformations. The physical phase space is the quotient

\[
\boxed{\mathcal P_\Phi:=\mathcal C_\Phi/\mathscr G_\Phi.}
\]

A physical statement must descend to \(\mathcal P_\Phi\). Thus the invariant observable algebra is

\[
\mathfrak{Obs}_\Phi
=
\left\{
\mathcal O:\mathcal C_\Phi\to\mathcal V
\;\middle|\;
\mathcal O[g\cdot\Phi]=\mathcal O[\Phi],\;g\in\mathscr G_\Phi
\right\}.
\]

This quotient condition is decisive. An observer-specific label may be useful within a chosen phase frame but becomes physically meaningful only after its frame dependence has been removed through an invariant relational construction.

The hierarchy of response and transition is

\[
\boxed{
\mathscr L_\Phi:=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi:=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi:=\mathscr L_\Phi^{-1}.
}
\]

Gauge directions can produce kinematical zero modes in the raw operator. The physical operators must therefore be understood on the transverse quotient tangent space:

\[
\overline{\mathscr L}_\Phi:
T_{[\Phi]}\mathcal P_\Phi\to T_{[\Phi]}\mathcal P_\Phi,
\qquad
\overline\Delta_\Phi:=\operatorname{Det}'\mathscr L_\Phi,
\qquad
\overline\chi_\Phi:=\overline{\mathscr L}_\Phi^{-1}.
\]

The prime indicates removal of pure redundancy directions. A genuine phase transition requires noninvertibility on the physical quotient, not merely a coordinate or gauge degeneracy. This distinction is the operator-theoretic form of the Andromeda result: a re-description of simultaneity must not be misread as a phase bifurcation.

---

## 4. Emergent Lorentzian Phase Sectors

### 4.1 Phase-response metric

Let \(\eta^a\) denote local phase order parameters and let \(\lambda^\mu\) be control coordinates that become effective spacetime coordinates in a stable emergent regime. Introduce the response map

\[
T_{\mu a}:=\frac{\partial\eta_a}{\partial\lambda^\mu}.
\]

The phase susceptibility defines the response metric

\[
\boxed{
 g^\Phi_{\mu\nu}
 =T_{\mu a}\,\overline\chi^{ab}_\Phi\,T_{\nu b}.
}
\]

This metric is not inserted as a primitive geometric background. It is the tensor that measures the distinguishability of neighboring phase configurations:

\[
ds_\Phi^2=g^\Phi_{\mu\nu}\,d\lambda^\mu d\lambda^\nu.
\]

An emergent Lorentzian vacuum is a connected stable region \(\mathcal V_L\subset\mathcal P_\Phi\) for which

\[
M_{\mathrm{eff}}=\mathcal E[\Phi],
\qquad
\operatorname{sig}(g^\Phi)=(-,+,+,+),
\qquad
\mathrm{Stab}(\mathcal V_L)\supset SO^+(1,3).
\]

The first condition establishes a physical manifold as a phase-derived structure. The second establishes the local distinction between timelike, null, and spacelike response directions. The third establishes the infrared covariance class of local phase frames. These conditions are the UPT antecedents of the Andromeda Non-Paradox.

### 4.2 Phase propagation and causal cones

Let \(\mathscr P_\Phi\) be the phase propagation operator obtained from the dynamical extension of \(\mathscr F\). Its principal symbol determines the characteristic set:

\[
\operatorname{Char}(\mathscr P_\Phi)
=
\left\{(x,k)\in T^*M_{\mathrm{eff}}:
\det\sigma(\mathscr P_\Phi,k)=0
\right\}.
\]

The emergent Lorentzian limit requires

\[
\det\sigma(\mathscr P_\Phi,k)=0
\quad\Longrightarrow\quad
 g_\Phi^{\mu\nu}k_\mu k_\nu=0
\quad\text{at infrared order}.
\]

Thus the causal cone is not an independent axiom. It is the characteristic geometry of phase propagation. The Andromeda distance enters a synchrony assignment across spacelike separation, whereas causal influence is determined by \(\operatorname{Char}(\mathscr P_\Phi)\). These are mathematically distinct constructions.

| Object | Definition | UPT status | Consequence for Andromeda |
|---|---|---|---|
| Synchrony section | \(\Sigma_A(p)\) | Observer-indexed local construction | May vary with \(A\) |
| Causal cone | \(g^{\mu\nu}_\Phi k_\mu k_\nu=0\) | Derived from \(\mathscr P_\Phi\) | Bounds phase influence |
| Phase history | \([\Phi]\in\mathcal P_\Phi\) | Physical quotient object | Does not change under re-slicing |
| Critical surface | \(\overline\Delta_\Phi=0\) | Physical transition locus | Cannot be crossed by relabeling |
| Observable | \(\mathcal O\in\mathfrak{Obs}_\Phi\) | Gauge/frame invariant | Cannot equal a bare \(\mathsf N_A\) |

---

## 5. Observers, Phase Frames, and the Derived Meaning of “Now”

A UPT observer is not a primitive Cartesian origin. It is a stable localized phase excitation embedded in the emergent Lorentzian sector. Represent an observer by

\[
\mathcal O_A=(\Phi_A,\gamma_A,e_A),
\]

where \(\Phi_A\) is the stable excitation, \(\gamma_A\) is its timelike trajectory in \((M_{\mathrm{eff}},g^\Phi)\), and \(e_A\) is its local phase frame. At \(p\in\gamma_A\), choose a normalized future-directed covector \(n^A_\mu\) satisfying

\[
g^{\mu\nu}_\Phi n^A_\mu n^A_\nu=-1.
\]

The local spatial rest distribution is

\[
\mathscr H_A(p):=\ker n^A\subset T_pM_{\mathrm{eff}}.
\]

Within a normal neighborhood, its exponential image gives a local synchrony section

\[
\boxed{
\Sigma_A(p):=\exp_p\big(\mathscr H_A(p)\big).
}
\]

The corresponding synchrony predicate is

\[
\mathsf N_A(p,q)=1
\quad\Longleftrightarrow\quad
q\in\Sigma_A(p).
\]

This predicate has three indices of dependence: the local observer \(A\), the local temporal phase frame \(e_A\), and the resulting rest distribution \(\mathscr H_A\). It is consequently not a function solely of the physical phase orbit \([\Phi]\). It does not descend to the observable algebra \(\mathfrak{Obs}_\Phi\).

UPT therefore defines the operational present at \(p\) as the local phase-stability and local relational data available to the observer excitation at \(p\). It does **not** define it as an ontological global section that exhausts the physical phase history. The universal phase history is specified by the solution orbit \([\Phi]\); the observer’s local phase frame selects a useful coordinate decomposition of that history.

This is not a semantic substitution. It is a bundle-theoretic distinction. A section \(\Sigma_A\) is a choice of local geometric splitting after the emergent metric has appeared. A phase orbit \([\Phi]\) is the physical object from which that emergent structure is derived. The two cannot be identified without reversing the UPT ontological hierarchy.

---

## 6. Phase Transport, Holonomy, and Remote Relational Data

The physical comparison of phase configurations at separated locations requires transport. Let

\[
D_\mu:=\partial_\mu+A_\mu[\Phi]
\]

be the derived phase connection. Parallel phase transport obeys

\[
D_\mu\Phi=0.
\]

Along a path \(\gamma:p\to q\), the transport operator is

\[
\boxed{
U_\gamma[\Phi]
=
\mathcal P\exp\left(-\int_\gamma A[\Phi]\right).
}
\]

Under a local phase-frame transformation \(h\in\mathscr G_\Phi\),

\[
A\mapsto A^h=hAh^{-1}-(dh)h^{-1},
\qquad
U_\gamma\mapsto h(q)U_\gamma h(p)^{-1}.
\]

The physical remote comparison is therefore not \(\mathsf N_A(p,q)\). It is an invariant contraction, such as

\[
\mathcal I_\gamma(p,q;\Phi)
=
\left\langle
\Phi(p),U_\gamma^{-1}[\Phi]\Phi(q)
\right\rangle_{\mathrm{inv}},
\]

or a closed-loop holonomy invariant

\[
\mathcal W_\Gamma[\Phi]
=
\operatorname{Tr}\,\mathcal P\exp\left(-\oint_\Gamma A[\Phi]\right).
\]

For a closed loop \(\Gamma\), nontrivial holonomy

\[
U_\Gamma\neq I
\]

expresses path dependence of phase transport. Its conjugacy class, rather than a particular frame matrix, is physical. A change of simultaneity section changes neither the connection curvature

\[
F_{\mu\nu}=[D_\mu,D_\nu]
\]

nor the conjugacy class of \(U_\Gamma\). Thus the Andromeda re-slicing does not add, subtract, or alter any topological or transport datum.

The distinction is especially important because the Andromeda construction concerns remote events beyond causal reach. A local observer at \(p\) cannot compare its phase frame directly to a remote frame at \(q\) without specifying a transport history or a received phase signal. A bare simultaneity section provides neither. It identifies an observer-dependent geometric locus; it does not supply a physical comparison protocol.

---

## 7. The Phase-History Covariance Theorem

We may now state the first central result.

### Proposition 1. Emergent phase-frame covariance

Let \([\Phi]\in\mathcal V_L\) be an admissible stable phase history. Let two observers \(A\) and \(B\) meet at \(p\), and let their local phase frames be related by \(h_{BA}\) in the emergent Lorentz/phase-frame action. Then the induced re-slicing map is

\[
\mathcal R_{BA}:
(\Phi_A,\lambda_A,\Sigma_A)
\mapsto
(\Phi_B,\lambda_B,\Sigma_B),
\qquad
\Phi_B=h_{BA}\cdot\Phi_A.
\]

If \(\mathscr F\) is covariant in the emergent Lorentzian sector, then

\[
\mathscr F[\Phi_B;\lambda_B]
=h_{BA}\cdot\mathscr F[\Phi_A;\lambda_A].
\]

Consequently,

\[
\mathscr F[\Phi_A;\lambda_A]=0
\quad\Longrightarrow\quad
\mathscr F[\Phi_B;\lambda_B]=0,
\]

and

\[
\boxed{[\Phi_B]=[\Phi_A]\in\mathcal P_\Phi.}
\]

#### Proof

The effective Lorentz action is a stabilizer action of the emergent vacuum sector. Covariance of the effective phase equation implies that application of \(h_{BA}\) maps a solution representative to another representative of the same solution orbit. Quotienting by \(\mathscr G_\Phi\) identifies the representatives. The synchrony sections are associated with different local rest distributions but do not label distinct physical phase orbits. \(\square\)

### Corollary 1. Invariance of relational observables

For every \(\mathcal O\in\mathfrak{Obs}_\Phi\),

\[
\boxed{\mathcal O[\Phi_B]=\mathcal O[\Phi_A].}
\]

The event membership relations \(\mathsf N_A(p,q_A)=1\) and \(\mathsf N_B(p,q_B)=1\) are not counterexamples because neither relation is an invariant functional of \([\Phi]\). They are frame-indexed predicates over distinct events.

### Corollary 2. The nonidentity of the remote selections

When \(vL\neq0\), the sections \(\Sigma_A(p)\) and \(\Sigma_B(p)\) intersect the remote Andromedean world-tube at different events:

\[
q_A\neq q_B.
\]

Thus there exists no logical form of the type

\[
\mathsf N(p,q)\wedge\neg\mathsf N(p,q)
\]

to be inferred. The alleged contradiction arises only by substituting \(q_A=q_B\) after suppressing the very observer data that define the relations.

---

## 8. Stability, Bifurcation, and the Impossibility of Remote Branch Selection by Re-Slicing

The physical content of an Andromedean decision, launch, or branch selection must be stated as a local property of the remote phase configuration. Suppose the relevant remote event occurs at a critical configuration \([\Phi_c]\). A true phase transition is signaled by

\[
\ker\overline{\mathscr L}_{\Phi_c}\neq0,
\qquad
\overline\Delta_{\Phi_c}=0.
\]

A mere transformation of the observer frame cannot produce this condition.

### Proposition 2. Stability-spectrum invariance

Under the phase-frame transformation of Proposition 1, the physical stability operators satisfy

\[
\boxed{
\overline{\mathscr L}_{\Phi_B}
=
h_{BA}\overline{\mathscr L}_{\Phi_A}h_{BA}^{-1}.
}
\]

Therefore,

\[
\operatorname{spec}(\overline{\mathscr L}_{\Phi_B})
=
\operatorname{spec}(\overline{\mathscr L}_{\Phi_A}),
\]

\[
\ker\overline{\mathscr L}_{\Phi_B}
=h_{BA}\big(\ker\overline{\mathscr L}_{\Phi_A}\big),
\]

and

\[
\boxed{
\overline\Delta_{\Phi_A}=0
\Longleftrightarrow
\overline\Delta_{\Phi_B}=0.
}
\]

#### Proof

Differentiate the covariant phase equation at a solution and restrict to the physical quotient. The transformed and untransformed linearizations are similar operators. Similarity preserves spectrum, kernel dimension, Fredholm index, and determinant zero-set. \(\square\)

Where the inverse exists, the susceptibility transforms covariantly:

\[
\overline\chi_{\Phi_B}
=
h_{BA}\overline\chi_{\Phi_A}h_{BA}^{-1}.
\]

Because the response tensors \(T_{\mu a}\) transform compatibly, the metric is carried by the corresponding pullback:

\[
g^\Phi_B=(h_{BA})^*g^\Phi_A.
\]

No pedestrian’s change of velocity can therefore shift a remote system from a stable pre-decision phase to a post-decision phase. It can only choose a different event on an already specified phase history as the event satisfying the observer’s local synchrony convention.

### 8.1 Lyapunov–Schmidt reduction of a genuine Andromedean branch point

Suppose a remote phase process truly undergoes a finite-codimension transition. At \([\Phi_c]\), decompose the physical tangent space as

\[
T_{[\Phi_c]}\mathcal P_\Phi=K\oplus R,
\qquad
K:=\ker\overline{\mathscr L}_{\Phi_c}.
\]

Writing

\[
\Phi=\Phi_c+u^ae_a+v,
\qquad
u=(u^1,\ldots,u^k)\in K,
\qquad
v\in R,
\]

the range equation may be solved locally as \(v=v(u,\lambda)\). Projection onto the cokernel gives the finite-dimensional reduced equation

\[
\boxed{
\varphi^a(u,\lambda)
=P\mathscr F\big[\Phi_c+u^be_b+v(u,\lambda);\lambda\big]=0.
}
\]

Its normal form has the expansion

\[
\varphi^a(u,\lambda)
=M^a{}_{i}\,\delta\lambda^i
+\frac12C^a{}_{bc}u^bu^c
+\frac16D^a{}_{bcd}u^bu^cu^d
+O(\|u\|^4,\|u\|^2\|\delta\lambda\|).
\]

The \(u^a\) are the physical phase order parameters of the remote transition. A frame transformation acts by invertible representation matrices

\[
u\mapsto R_Ku,
\qquad
\varphi\mapsto R_{K^*}\varphi.
\]

It preserves the zero locus and the normal-form equivalence class. Hence the existence, codimension, and branch connectivity of the remote transition are frame invariant. The coordinate components of \(u\) may change, but the bifurcation cannot be created by re-slicing.

> **Structural conclusion.** The phrase “the decision is already made for one observer” can have a physical meaning only if it refers to a branch of the reduced equation at a definite remote event. Re-slicing changes which remote event is named simultaneous with \(p\); it does not change the reduced branch structure at any event.

---

## 9. The Causal Non-Action Theorem

The phase equation provides the local ontology; the propagation operator provides causal accessibility. Let the effective phase dynamics be normally hyperbolic in \(\mathcal V_L\), with retarded Green operator \(G^\mathrm{ret}_\Phi\). For a compactly supported local perturbation \(J\) near \(p\), the linearized response is

\[
\delta\Phi=G^\mathrm{ret}_\Phi J.
\]

Hyperbolicity implies the support condition

\[
\operatorname{supp}(G^\mathrm{ret}_\Phi J)
\subseteq J^+_\Phi(\operatorname{supp}J),
\]

where \(J^+_\Phi\) is defined by the characteristic cone of \(\mathscr P_\Phi\). For a spacelike remote event \(q\),

\[
q\notin J^+_\Phi(p)
\quad\Longrightarrow\quad
\delta\mathcal O(q)=0
\]

for every local gauge-invariant observable \(\mathcal O(q)\), until a characteristic signal reaches \(q\).

### Proposition 3. Causal non-action of an observer re-slicing

Let \(p\) and \(q\) be spacelike separated in the emergent metric. An observer re-slicing at \(p\) changes neither the physical source \(J\), nor \([\Phi]\), nor the support of any phase perturbation. Therefore it cannot change a local phase observable at \(q\):

\[
\boxed{
\mathcal R_{BA}\!:\;\mathsf N_A\mapsto\mathsf N_B
\quad\text{while}\quad
\delta_{\mathcal R_{BA}}\mathcal O(q)=0.
}
\]

#### Proof

A re-slicing is a local phase-frame transformation in the representation of the same quotient history. It supplies no source term in \(\mathscr P_\Phi\), induces no change of \([\Phi]\), and leaves the domain-of-dependence relation invariant. Since \(q\) is spacelike to \(p\), no retarded phase response from an operation near \(p\) reaches \(q\). A re-description, being weaker than an operation, has no effect a fortiori. \(\square\)

The Andromeda construction therefore cannot encode a causal retroaction, observer-generated future, or remotely triggered phase selection. The numerical shift \(vL/c^2\) measures a difference of section intersection, not a propagation of phase information.

---

## 10. Topological Sector Invariance and Holonomy Protection

UPT recognizes particle-like and persistent structures as topologically protected phase configurations. Let the phase map define a class

\[
[\Phi]\in\pi_n(\mathcal M_\Phi),
\]

or, for a compact Abelian phase, a winding number

\[
Q[\Phi]=\frac{1}{2\pi}\oint d\theta\in\mathbb Z.
\]

For a local conserved current,

\[
Q_\Sigma[\Phi]=\int_\Sigma j^\mu[\Phi]d\Sigma_\mu,
\qquad
\nabla_\mu j^\mu=0.
\]

A change of observer frame acts as an automorphism of the representation of the same phase bundle. It cannot change a homotopy class, winding number, conserved charge, or holonomy conjugacy class:

\[
[\Phi_B]_{\pi_n}=[\Phi_A]_{\pi_n},
\qquad
Q[\Phi_B]=Q[\Phi_A],
\qquad
[U_\Gamma(\Phi_B)]=[U_\Gamma(\Phi_A)].
\]

This result excludes a subtler version of the paradox in which different simultaneity sections are claimed to slice a different topological content from the remote system. A local slice may display a different coordinate decomposition of a defect or process, but its invariant topological sector is a property of the phase orbit. It is not determined by membership in an observer’s \(\Sigma_A(p)\).

Global issues do not restore the paradox. On a curved or topologically nontrivial emergent spacetime, a single observer’s rest distribution need not integrate to a global foliation. Such failure strengthens rather than weakens the theorem: it prevents the extension of a local synchrony construction into a global physical ontology without additional phase-dynamical input. The physical invariant remains the phase orbit and its relational observables.

---

## 11. The Andromeda Non-Paradox Theorem

We can now consolidate the preceding propositions.

### Theorem. Andromeda Non-Paradox in UPT

Let \(\mathcal V_L\subset\mathcal P_\Phi\) be a stable UPT phase sector satisfying the following conditions:

1. **Phase quotient covariance:** admissible phase-frame transformations act equivariantly on \(\mathscr F[\Phi;\lambda]=0\) and preserve physical phase orbits.
2. **Emergent Lorentzian geometry:** the susceptibility response tensor defines \(g^\Phi_{\mu\nu}\) with Lorentzian signature and an infrared local Lorentz symmetry class.
3. **Covariant phase transport:** remote phase comparisons are represented by \(D_\mu=\partial_\mu+A_\mu[\Phi]\) and its invariant contractions or holonomies.
4. **Hyperbolic phase propagation:** the characteristic set of \(\mathscr P_\Phi\) defines the causal cone and the corresponding domain of dependence.

Then, for two stable observers \(A\) and \(B\) meeting at \(p\), distinct observer-indexed simultaneity sections \(\Sigma_A(p)\) and \(\Sigma_B(p)\) may select distinct spacelike events \(q_A\) and \(q_B\) on a remote world-tube, but cannot induce any of the following solely by the change of section:

\[
\begin{aligned}
&[\Phi]\mapsto[\Phi']\neq[\Phi],\\
&\overline\Delta_\Phi\mapsto0,\\
&\text{a change of Lyapunov–Schmidt branch},\\
&Q[\Phi]\mapsto Q'[\Phi]\neq Q[\Phi],\\
&[U_\Gamma]\mapsto[U_\Gamma']\neq[U_\Gamma],\\
&\mathcal O(q)\mapsto\mathcal O'(q)\neq\mathcal O(q)
\quad\text{for spacelike }q.
\end{aligned}
\]

#### Proof

By phase quotient covariance, \(A\) and \(B\) represent the same phase orbit. By stability-spectrum invariance, their re-slicing cannot alter \(\ker\overline{\mathscr L}_\Phi\), \(\overline\Delta_\Phi\), \(\overline\chi_\Phi\), or the Lyapunov–Schmidt reduced branch set. By transport covariance, frame-dependent remote comparisons acquire physical meaning only through invariant transport composites, which are unchanged by the re-slicing. By topological invariance, charge and holonomy data are constant on the orbit. By hyperbolic propagation, no spacelike local operation, and therefore no re-description, alters a remote local observable. Finally, the selected remote events satisfy \(q_A\neq q_B\); the two synchrony predicates describe different relational pairings rather than contradictory properties of a single event. \(\square\)

The theorem is named a **non-paradox** because the standard kinematic effect remains intact. UPT does not deny the relation

\[
\delta t=\frac{vL}{c^2}.
\]

It identifies its categorical status: it is a relation between two observer-defined sections and a remote world-tube. It is not a change in the remote solution of \(\mathscr F=0\).

---

## 12. What the Derivation Establishes, What It Requires, and What It Forbids

A foundational theory remains rigorous only when it separates derivation from insertion. The Andromeda Non-Paradox has a precise logical status.

| Category | Statement |
|---|---|
| **Derived in a Lorentzian UPT sector** | Observer re-slicing preserves phase orbits, physical stability spectra, bifurcation loci, branch structure, topological classes, holonomy invariants, and local gauge-invariant observables. |
| **Required UPT dynamical result** | A specific universal phase equation \(\mathscr F\) must generate a stable physical quotient, a Lorentzian \(g^\Phi_{\mu\nu}\), emergent local Lorentz covariance, and hyperbolic \(\mathscr P_\Phi\). |
| **Forbidden assumption** | A pre-given Minkowski metric, primitive global time, preferred simultaneity foliation, or remote branch value may not be postulated as the explanation. |
| **Permissible additional UPT discovery** | A gauge-invariant temporal phase order parameter may emerge, but only as a solution-dependent field with derived dynamics and testable couplings. |

### 12.1 Why preferred simultaneity is not an available shortcut

Suppose one attempts to repair the construction by declaring a fundamental phase clock \(\Theta[\Phi]\). For it to define a physical foliation, the covector

\[
T_\mu[\Phi]:=\nabla_\mu\Theta[\Phi]
\]

must satisfy

\[
g_\Phi^{\mu\nu}T_\mu T_\nu<0,
\qquad
\nabla_{[\mu}T_{\nu]}=0,
\qquad
T_\mu[h\cdot\Phi]=T_\mu[\Phi].
\]

The first condition makes the phase clock timelike; the second makes its rest distribution integrable; the third ensures physical rather than gauge-dependent status. Such a field is a dynamical order parameter. Its existence would amount to a genuine additional UPT prediction, potentially accompanied by preferred-frame observables. It cannot be inserted solely because the Andromeda construction appears uncomfortable.

The present theorem does not require \(\Theta\). It establishes non-contradiction without a global phase clock. This is structurally preferable because it preserves the UPT demand that geometry and temporal structure be derived from \(\Phi\), not stipulated above it.

### 12.2 Scale dependence

UPT postulate X permits scale-dependent effective descriptions,

\[
\Phi\longmapsto\Phi_\ell,
\qquad
\mathcal R_b:\Phi_\ell\longmapsto\Phi_{b\ell}.
\]

The emergent Lorentzian phase need only be an infrared universality class. Write the effective action schematically as

\[
S_{\mathrm{eff},\ell}
=
\int d^{d_{\mathrm{eff}}}x\,\sqrt{-g^\Phi}
\left[
\mathcal L_{\mathrm{Lor}}(\Phi_\ell,g^\Phi)
+
\sum_{r}\frac{c_r(\ell)}{\Lambda_\Phi^{\Delta_r-d_{\mathrm{eff}}}}\mathcal O_r
\right].
\]

The Andromeda theorem holds exactly in the Lorentz-covariant fixed sector and perturbatively to the accuracy with which the effective propagation and response structures obey the stated covariance. If irrelevant operators generate measurable phase-frame dependence, that dependence is not a reinterpretation of the thought experiment; it is a physical prediction to be bounded experimentally.

---

## 13. Research Questions and Falsifiability Criteria

The paper yields a research program rather than a verbal resolution. A candidate UPT realization must provide a concrete phase equation, a vacuum sector, and explicit observable consequences.

### 13.1 Research questions

| Question | Formal target |
|---|---|
| What microscopic phase bundle supports the relevant vacuum? | Construct \(E_\Phi\to\mathcal X\) and \(\mathscr G_\Phi\). |
| What equation selects the vacuum? | Specify \(\mathscr F[\Phi;\lambda]=0\) or an action \(S_\Phi\) with \(\delta S_\Phi/\delta\Phi=0\). |
| Why is the physical quotient stable? | Show spectral control of \(\overline{\mathscr L}_\Phi\) and classify \(\overline\Delta_\Phi=0\). |
| How does Lorentzian geometry arise? | Derive \(g^\Phi_{\mu\nu}=T_{\mu a}\overline\chi^{ab}_\Phi T_{\nu b}\) with signature \((-,+,+,+)\). |
| How is the causal cone fixed? | Compute \(\det\sigma(\mathscr P_\Phi,k)\) and establish hyperbolicity. |
| How is local Lorentz covariance recovered? | Identify the infrared stabilizer/renormalization fixed point. |
| Does a physical phase clock exist? | Derive or exclude a gauge-invariant integrable timelike \(T_\mu[\Phi]\). |
| How are remote phase comparisons measured? | Construct invariant transport observables \(\mathcal I_\gamma\) and holonomy classes. |

### 13.2 Falsifiability conditions

A concrete UPT realization fails the Andromeda Non-Paradox test if one finds any of the following:

1. **Orbit non-covariance:** two local phase-frame descriptions of identical local data solve inequivalent quotient phase histories.
2. **Observer-induced bifurcation:** an infinitesimal frame change alters \(\operatorname{spec}(\overline{\mathscr L}_\Phi)\), creates a new zero mode, or changes the reduced branch set without a physical control-parameter perturbation.
3. **Invariant alteration under re-slicing:** a topological charge, holonomy conjugacy class, or gauge-invariant local observable changes under a pure synchrony re-description.
4. **Spacelike propagation:** the retarded response of \(\mathscr P_\Phi\) has support outside the emergent characteristic cone in a manner coupled to observable phase degrees of freedom.
5. **Metric failure:** the susceptibility construction fails to generate a stable Lorentzian response tensor in the purported physical vacuum.
6. **Uncontrolled preferred frame:** a required global phase clock produces observable preferred-frame effects inconsistent with empirical bounds, without a compensating phase-dynamical mechanism.

These are decisive criteria. The theorem is not protected by terminology: it stands or falls with the quotient covariance, spectral stability, and causal structure of a specified \(\mathscr F\).

---

## 14. Discussion: Determinism, Openness, and the Phase-History Distinction

The Andromeda construction is frequently turned into an argument for a fixed four-dimensional reality. UPT does not license that transition from kinematics to a conclusion about the microscopic determinism of \(\mathscr F\). A solution orbit may be specified globally in a mathematical treatment without implying that the universal phase equation is deterministic, unique, or globally well-posed under the data physically available to a localized phase excitation.

The determinism question is controlled by the solution map of the phase dynamics. Given admissible data \(\mathcal D_\Sigma\) on a suitable characteristic or Cauchy structure, one must study whether

\[
\mathcal D_\Sigma
\longmapsto
[\Phi]
\]

is unique, multi-valued, measure-valued, or branch-structured. At a critical configuration, Lyapunov–Schmidt reduction may yield multiple admissible branches. At the quantum-effective level, a phase measure over branches may be required. None of those dynamical questions is answered by the fact that two observers choose different \(\Sigma_A(p)\).

The phase-historical ontology of UPT is therefore exact: a remote decision corresponds to phase evolution and possibly branch selection in the Andromedean subsystem. Its operational accessibility at Earth is determined by phase propagation and transport. Its membership in a particular Earth observer’s synchrony section is an indexical geometric relation. The first is physical evolution; the second is an observer-conditioned representation. Confusing them converts a covariance statement into a false causal or ontological contradiction.

---

## 15. Conclusion

Universal Phase Theory resolves the Andromeda construction by placing each of its elements at the correct level of the phase hierarchy. The universal phase field \(\Phi\) supplies the primitive configuration. Its topological class protects persistent sectors. Its susceptibility generates geometry. Its connection defines meaningful remote phase transport. Its stable defects define observer excitations. Its invariant functionals define observables. A simultaneity section appears only after the emergent Lorentzian phase has been locally decomposed relative to an observer’s temporal phase frame.

The central result is therefore not that relativity of simultaneity disappears. It remains, with its large distance-amplified shift

\[
\delta t=\frac{vL}{c^2}.
\]

What disappears is the category error. The shift is not a motion through physical phase space, not a zero of \(\overline\Delta_\Phi\), not a change in \(\overline\chi_\Phi\), not a deformation of topological charge, not an alteration of holonomy, and not a causal influence at Andromeda. It is a change in an observer-indexed synchrony relation.

The Andromeda Non-Paradox theorem establishes the following chain:

\[
\boxed{
\text{phase-frame change}
\Longrightarrow
\text{new synchrony section}
\Longrightarrow
\text{different remote event selection}
\not\Longrightarrow
\text{new phase history or remote branch selection}.
}
\]

This is the precise UPT answer. A viable UPT model must still derive its Lorentzian phase, phase propagation operator, and covariance class from a concrete universal equation. Once that work is done, the Andromeda construction no longer threatens causal structure, local openness, or relational observability. It becomes a direct manifestation of the distinction between an observer’s geometric slicing and the invariant phase structure from which geometry itself emerges.

---

## Appendix A. Coordinate Derivation of the Simultaneity Displacement

Let \(A\) and \(B\) coincide at \(p\). In \(A\)’s local inertial chart, place the remote world-tube at \(x_A=L\). The observer \(B\) has relative velocity \(v\) along the positive axis. The Lorentz transformation is

\[
t_B=\gamma\left(t_A-\frac{vx_A}{c^2}\right).
\]

The intersection of \(A\)’s simultaneous section with the world-tube is \(q_A=(0,L)\). The intersection of \(B\)’s simultaneous section satisfies \(t_B(q_B)=0\), and hence

\[
t_A(q_B)=\frac{vL}{c^2}.
\]

Consequently,

\[
q_A\neq q_B
\quad\text{if}\quad vL\neq0.
\]

The invariant interval between the Earth encounter \(p\) and either remote selected event is spacelike when \(L\gg c|t|\). Therefore no causal signal has connected the events. This fact is independent of the order assigned to the remote events by any observer frame.

---

## Appendix B. Formal Status Ledger

| Claim | Mathematical basis | Status |
|---|---|---|
| Remote simultaneity assignments vary with velocity | Emergent Lorentz transformation | Kinematical result |
| The assignments select distinct remote events | \(q_A\neq q_B\) for \(vL\neq0\) | Direct consequence |
| Re-slicing preserves phase orbit | Equivariance and \(\mathcal P_\Phi=\mathcal C_\Phi/\mathscr G_\Phi\) | Theorem antecedent |
| Re-slicing preserves critical structure | Similarity of \(\overline{\mathscr L}_\Phi\) | Derived theorem |
| Re-slicing cannot cause remote change | Hyperbolic domain of dependence | Derived theorem antecedent |
| A global present is fundamental | Requires \(\Theta[\Phi]\) | Not assumed |
| A preferred phase clock exists | Requires gauge-invariant timelike integrable order parameter | Open dynamical question |
| Lorentzian geometry exists | Requires stable response-metric sector | UPT derivation obligation |
| Determinism follows from simultaneity | No implication | Rejected inference |

---

## References

[1] Dust LLC, *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, supplied manuscript, August 2026.

[2] J. D. Norton, “[Special Relativity Simultaneity](https://sites.pitt.edu/~jdnorton/teaching/HPS_0410/chapters/Special_relativity_rel_sim/index.html),” *Einstein for Everyone*, University of Pittsburgh, accessed August 2026.

[3] R. Penrose, *[The Emperor’s New Mind: Concerning Computers, Minds, and the Laws of Physics](https://archive.org/details/emperorsnewmindc00penr)*, Oxford University Press, 1989, pp. 303–304.

[4] C. W. Rietdijk, “[A Rigorous Proof of Determinism Derived from the Special Theory of Relativity](https://doi.org/10.1086/288106),” *Philosophy of Science* **33**, 341–344 (1966).

[5] H. Stein, “[On Relativity Theory and Openness of the Future](https://doi.org/10.1086/289609),” *Philosophy of Science* **58**, 147–167 (1991).

[6] S. Savitt, N. Deng, and O. Pooley, “[Being and Becoming in Modern Physics](https://plato.stanford.edu/entries/spacetime-bebecome/),” *Stanford Encyclopedia of Philosophy*, substantive revision 2021.

[7] NASA, “[Messier 31 (The Andromeda Galaxy)](https://science.nasa.gov/mission/hubble/science/explore-the-night-sky/hubble-messier-catalog/messier-31/),” Hubble Messier Catalog, accessed August 2026.

# Uncertainty Mechanics: Physical Law Before Probability

**Preprint — September 2026**

---

## Abstract

We develop a physical theory whose primitive object is not a probability distribution, not a wavefunction, and not a stochastic process, but an *uncertainty structure*. Starting from the mathematics of uncertainty without probability, we promote possibility spaces, information constraints, compatibility relations, and refinement operations to dynamical physical objects. The central claim is that physical law is more fundamentally a law governing the evolution of unresolved possibilities, while probability is a derived additive coordinate chart that becomes available only under additional structural assumptions.

We introduce:

\[
\mathfrak U=(\mathcal X,\mathcal A,\preceq,\mathcal R,\mathcal E),
\]

where \(\mathcal X\) is a possibility space, \(\mathcal A\) a proposition algebra, \(\preceq\) an information-refinement order, \(\mathcal R\) a compatibility relation, and \(\mathcal E\) an evidence/update family. From this structure we construct a physical kinematics of possibility regions, a Hamiltonian dynamics of unresolved phase-space sets, a relativistic uncertainty field theory, and a noncommutative sector from which quantum mechanics emerges as a special probabilistic representation.

The resulting theory yields several physical consequences:

1. **Possibility conservation**: Hamiltonian evolution conserves symplectic uncertainty volume independently of probability.
2. **Information contraction**: Measurement and evidence act as geometric refinements that reduce admissible possibility regions.
3. **Uncertainty pressure**: Boundaries of possibility regions obey a generalized Hamilton–Jacobi equation with a curvature-dependent term.
4. **Uncertainty gauge fields**: Local incompatibility of information charts produces a connection \(\mathcal A_\mu\) and curvature \(\mathcal F_{\mu\nu}\).
5. **Residual uncertainty as dark energy**: A homogeneous irreducible uncertainty scalar generates an effective cosmological constant.
6. **Geometric quantum bound**: The quantum of action \(\hbar\) appears as a minimal symplectic capacity of admissible possibility regions.
7. **Non-Born corrections**: Nontrivial uncertainty holonomies produce deviations from ordinary Born-rule interference.

The central result is that probability is not the foundation of physical uncertainty. Rather, probability is one possible additive realization of a deeper geometry of unresolved possibility.

---

## 1. Introduction

Modern physics has treated uncertainty mainly through probability. Classical statistical mechanics assigns a measure \(\rho(q,p)\) on phase space. Quantum mechanics assigns a state \(\rho\) or wavefunction \(\psi\), from which Born probabilities are extracted. Stochastic field theory, thermodynamics, and measurement theory likewise assume that uncertainty is ultimately represented by normalized additive weights.

This assumption is powerful but not primitive. A physical system may be uncertain because:

\[
x\in U\subseteq \mathcal X,
\]

without any commitment to a probability distribution on \(U\). An interval,

\[
x\in[a,b],
\]

does not imply

\[
x\sim \mathrm{Uniform}(a,b).
\]

A set of compatible models,

\[
M\in\mathcal M_E,
\]

does not imply a probability distribution over \(\mathcal M_E\). A quantum incompatibility between observables does not automatically reduce to classical ignorance over pre-existing values. Probability is one representation of unresolved alternatives; it is not the only one, and it is not necessarily the first.

The present paper derives physics from a more primitive principle:

\[
\boxed{
\text{Physical states are structures of unresolved possibility.}
}
\]

The central object is an uncertainty structure

\[
\mathfrak U=(\mathcal X,\mathcal A,\preceq,\mathcal R,\mathcal E),
\]

where:

* \(\mathcal X\) is the space of physically possible configurations;
* \(\mathcal A\subseteq 2^{\mathcal X}\) is an algebra of physical propositions;
* \(\preceq\) orders information states by refinement;
* \(\mathcal R\) encodes compatibility between alternatives;
* \(\mathcal E\) is the family of admissible evidence or update operations.

Probability appears only when \(\mathfrak U\) admits an additive normalized scalar chart.

The physical program is therefore:

\[
\boxed{
\text{possibility}
\rightarrow
\text{constraint}
\rightarrow
\text{uncertainty geometry}
\rightarrow
\text{dynamics}
\rightarrow
\text{probability}.
}
\]

This is not an interpretation of quantum mechanics. It is a reconstruction of physical kinematics and dynamics before probabilistic quantification.

---

## 2. Axioms of Pre-Probabilistic Physical Uncertainty

We introduce five physical postulates.

### Postulate 1: Primacy of Possibility

A physical system is associated with a nonempty possibility space

\[
\mathcal X\neq\varnothing.
\]

A point \(x\in\mathcal X\) is a physically admissible configuration. No measure on \(\mathcal X\) is assumed.

### Postulate 2: Uncertainty as Non-Identification

The physical state of knowledge is represented by an admissible subset

\[
U\subseteq \mathcal X.
\]

The system is uncertain relative to a question \(Q:\mathcal X\to\mathcal Y\) whenever

\[
|Q(U)|>1.
\]

Certainty with respect to \(Q\) occurs if and only if

\[
|Q(U)|=1.
\]

### Postulate 3: Information as Refinement

Information \(I\) acts by restriction:

\[
\mathcal X_I=\{x\in\mathcal X:x\models I\}.
\]

If \(I_2\) contains more information than \(I_1\), then

\[
I_1\preceq I_2
\quad\Longleftrightarrow\quad
\mathcal X_{I_2}\subseteq \mathcal X_{I_1}.
\]

Thus:

\[
\boxed{
\text{more information}
\Longleftrightarrow
\text{smaller possibility region}.
}
\]

### Postulate 4: Evidence as Morphism

Evidence is not a probability likelihood. It is an operator

\[
\mathcal E_e:\mathfrak U\to\mathfrak U
\]

such that, for pure constraint evidence,

\[
\mathcal E_e(U)=U\cap E.
\]

More generally, evidence may transform compatibility relations, accessibility structures, or algebraic states.

### Postulate 5: Probability as Derived Chart

A probability measure is an additive chart

\[
P:\mathcal A\to[0,1]
\]

satisfying

\[
P(\mathcal X)=1,
\qquad
P\left(\bigcup_i A_i\right)=\sum_i P(A_i)
\]

for disjoint measurable \(A_i\). Such a chart exists only after additional structure has been imposed.

---

## 3. Kinematics of Possibility Regions

Let \(\mathcal Q\) be a smooth configuration manifold. A physical possibility region is a compact subset

\[
U\subseteq \mathcal Q.
\]

For an observable

\[
f:\mathcal Q\to\mathbb R,
\]

the unresolved range of \(f\) over \(U\) is

\[
\Delta_U f
=
\sup_{x\in U}f(x)-\inf_{x\in U}f(x).
\]

This is a probability-free measure of observable uncertainty.

### 3.1 Certainty and Observable Projection

Given an observable map

\[
Q:\mathcal Q\to\mathcal Y,
\]

the observable uncertainty induced by \(U\) is

\[
U_Q=Q(U).
\]

A quantity \(Q\) is certain if

\[
U_Q=\{q^\ast\}.
\]

Thus one may have

\[
|U|>1
\]

while still

\[
|Q(U)|=1.
\]

This gives a precise distinction between state uncertainty and observable uncertainty.

### 3.2 Geometric Uncertainty Tensors

Suppose \(U\subset\mathbb R^n\) is convex. Define its support function

\[
h_U(n)
=
\sup_{x\in U}n_i x^i,
\qquad
n\in S^{n-1}.
\]

The support function encodes the geometry of the possibility region. The inverse Weingarten tensor on the unit sphere is

\[
W_U^{ij}(n)
=
\bar\nabla^i\bar\nabla^j h_U(n)
+
h_U(n)\bar g^{ij}(n),
\]

where \(\bar\nabla\) and \(\bar g\) are the covariant derivative and metric on \(S^{n-1}\). The eigenvalues of \(W_U^{ij}\) are the principal radii of curvature of \(\partial U\).

The mean geometric uncertainty radius is

\[
R_U(n)
=
\frac{1}{n}W_U{}^i_i(n).
\]

This provides a tensorial, probability-free descriptor of uncertainty shape.

When a reference volume form \(\mu\) exists, define the uncertainty volume

\[
V_U=\int_U \mu.
\]

The associated scalar uncertainty functional is

\[
\mathscr H(U)=\log\frac{V_U}{V_0},
\]

where \(V_0\) is a fixed reference volume. This is not Shannon entropy. It is a geometric uncertainty measure.

---

## 4. Hamiltonian Possibility Dynamics

Let phase space be

\[
\Gamma=T^\ast\mathcal Q
\]

with canonical coordinates \((q^i,p_i)\), symplectic form

\[
\omega=dq^i\wedge dp_i,
\]

and Liouville volume form

\[
\Omega=\frac{1}{n!}\omega^n.
\]

A pre-probabilistic physical state is a compact possibility region

\[
\Omega_U\subseteq \Gamma.
\]

We do not assign a density \(\rho\) on \(\Omega_U\). The physically relevant object is the region itself.

Let \(H:\Gamma\to\mathbb R\) be a Hamiltonian. The Hamiltonian vector field \(X_H\) is defined by

\[
\iota_{X_H}\omega=-dH.
\]

Closed physical evolution is the flow

\[
\Phi_t:\Gamma\to\Gamma,
\]

and the possibility region evolves as

\[
\Omega_U(t)=\Phi_t(\Omega_U(0)).
\]

### Theorem 1: Conservation of Possibility Volume

For Hamiltonian evolution,

\[
\frac{d}{dt}\operatorname{Vol}(\Omega_U(t))=0,
\]

where

\[
\operatorname{Vol}(\Omega_U)=\int_{\Omega_U}\Omega.
\]

**Proof.** By Cartan’s formula,

\[
\mathcal L_{X_H}\omega
=
d(\iota_{X_H}\omega)+\iota_{X_H}d\omega
=
d(-dH)+0
=
0.
\]

Therefore,

\[
\mathcal L_{X_H}\Omega
=
\mathcal L_{X_H}\left(\frac{1}{n!}\omega^n\right)
=
0.
\]

Using transport by the flow,

\[
\frac{d}{dt}\int_{\Omega_U(t)}\Omega
=
\int_{\Omega_U(t)}\mathcal L_{X_H}\Omega
=
0.
\]

Thus Hamiltonian evolution conserves phase-space possibility volume.

\[
\boxed{\square}
\]

This is a probability-free analogue of Liouville’s theorem. It does not require a probability density. It states that closed Hamiltonian dynamics preserves the volume of unresolved phase-space possibilities.

### 4.1 Boundary Evolution

Let the boundary of \(\Omega_U(t)\) be represented by a level-set function

\[
\phi(q,p,t)=0.
\]

The evolution of the boundary under Hamiltonian flow is

\[
\partial_t\phi+\{\phi,H\}=0,
\]

where

\[
\{f,g\}
=
\frac{\partial f}{\partial q^i}\frac{\partial g}{\partial p_i}
-
\frac{\partial f}{\partial p_i}\frac{\partial g}{\partial q^i}.
\]

This is the Hamilton–Jacobi transport of possibility boundaries.

---

## 5. Information Contraction and the First Law of Uncertainty Dynamics

Evidence modifies the possibility region by refinement. Let evidence arrive continuously. The update is

\[
\Omega_U(t+dt)
=
\Phi_{dt}(\Omega_U(t))\cap C_t,
\]

where \(C_t\) is the constraint imposed by new information.

Define the information absorption scalar \(\sigma_I\ge 0\). The volume evolution becomes

\[
\frac{d}{dt}V_U(t)
=
-\int_{\Omega_U(t)}\sigma_I\,\Omega.
\]

Therefore,

\[
\boxed{
\frac{dV_U}{dt}=-\Sigma_I,
}
\]

where

\[
\Sigma_I=\int_{\Omega_U}\sigma_I\,\Omega.
\]

Using

\[
\mathscr H_U=\log\frac{V_U}{V_0},
\]

we obtain

\[
\frac{d\mathscr H_U}{dt}
=
-\frac{\Sigma_I}{V_U}.
\]

This is the first law of uncertainty dynamics:

\[
\boxed{
\text{information reduces uncertainty volume.}
}
\]

The law is not probabilistic. It is a geometric conservation law with a source term representing evidence.

---

## 6. Least-Commitment Dynamics and Uncertainty Pressure

We now derive a dynamical principle for possibility boundaries. The physical evolution should introduce no more structure than required by the available information. We formulate this as a variational principle.

Let \(\Sigma_t=\partial\Omega_U(t)\). Consider the action

\[
\mathcal S[\Omega_U]
=
\int_{t_0}^{t_1}
\left[
\int_{\Omega_U(t)}
\left(p_i\dot q^i-H\right)\Omega
+
\beta\,\operatorname{Area}(\Sigma_t)
\right]dt,
\]

where \(\beta\) is a constant with dimensions of action per area.

The first term is the usual phase-space action integrated over the possibility region. The second term penalizes the boundary area of the unresolved region. It expresses a geometric resistance to fragmentation or excessive boundary complexity.

Varying the boundary gives

\[
\delta\operatorname{Area}(\Sigma)
=
\int_{\Sigma}K\,\delta r\,dA,
\]

where \(K\) is the mean curvature of \(\Sigma\) in phase space and \(\delta r\) is the normal displacement.

The resulting boundary equation is

\[
\boxed{
\partial_t S+H(q,\partial_q S)=\beta K.
}
\]

This is a generalized Hamilton–Jacobi equation. The usual Hamilton–Jacobi equation is recovered when

\[
\beta=0.
\]

The term \(\beta K\) is an uncertainty pressure. It implies that possibility boundaries do not merely follow classical characteristics; they also respond to their own geometry.

This is a genuinely new physical effect:

\[
\boxed{
\text{unresolved possibility regions possess geometric surface dynamics.}
}
\]

---

## 7. Relativistic Uncertainty Field Theory

We now lift the formalism to spacetime. Let \(M\) be a four-dimensional Lorentzian manifold with metric \(g_{\mu\nu}\). At each spacetime point \(x\in M\), suppose there is a local possibility fiber \(\mathcal F_x\). The collection forms an uncertainty bundle

\[
\pi:\mathcal F\to M.
\]

A physical uncertainty field is a section

\[
U:x\mapsto U_x\subset \mathcal F_x.
\]

### 7.1 Uncertainty Scalar

Let \(V_U(x)\) be the local possibility volume. Define

\[
h(x)=\log\frac{V_U(x)}{V_0}.
\]

The scalar \(h\) measures local residual uncertainty. It is not a probability density.

### 7.2 Information Connection

Local descriptions of uncertainty may fail to glue globally. Let \(\{U_\alpha\}\) be an open cover of \(M\). On overlaps \(U_\alpha\cap U_\beta\), local information charts are related by transition maps

\[
g_{\alpha\beta}:U_\alpha\cap U_\beta\to G,
\]

where \(G\) is the relevant structure group of admissible uncertainty transformations.

If the transition functions are nontrivial, they define a connection

\[
\mathcal A_\mu=\mathcal A_\mu^a T_a,
\]

with curvature

\[
\mathcal F_{\mu\nu}
=
\partial_\mu\mathcal A_\nu-\partial_\nu\mathcal A_\mu
+
[\mathcal A_\mu,\mathcal A_\nu].
\]

In components,

\[
\mathcal F_{\mu\nu}^a
=
\partial_\mu\mathcal A_\nu^a
-
\partial_\nu\mathcal A_\mu^a
+
f^a{}_{bc}\mathcal A_\mu^b\mathcal A_\nu^c.
\]

This curvature measures the failure of local uncertainty charts to combine into a single global chart.

Physically:

\[
\boxed{
\mathcal F_{\mu\nu}
=
\text{curvature of incompatible information.}
}
\]

### 7.3 Uncertainty Action

We propose the action

\[
S[g,\mathcal A,h]
=
\int_M
\sqrt{-g}
\left[
\frac{1}{2\kappa}R
-
\frac{1}{4\gamma^2}
\mathcal F_{\mu\nu}^a\mathcal F_a^{\mu\nu}
-
\frac{1}{2}
\nabla_\mu h\nabla^\mu h
-
V(h)
\right]
d^4x
+
S_\mathrm{matter}.
\]

Here:

* \(R\) is the Ricci scalar;
* \(\kappa=8\pi G/c^4\);
* \(\gamma\) is an uncertainty gauge coupling;
* \(V(h)\) is the potential of residual uncertainty.

### 7.4 Field Equations

Varying with respect to \(\mathcal A_\mu^a\) gives

\[
\boxed{
D_\mu\mathcal F_a^{\mu\nu}= \gamma^2 J_{a}^{\nu},
}
\]

where \(D_\mu\) is the gauge-covariant derivative and \(J_a^\nu\) is the information current sourced by matter.

Varying with respect to \(h\) gives

\[
\boxed{
\square h - V'(h)=\eta\,J_h,
}
\]

where \(J_h\) is a scalar information source and \(\eta\) is a coupling constant.

Varying with respect to \(g^{\mu\nu}\) gives

\[
\boxed{
G_{\mu\nu}
=
\kappa
\left(
T_{\mu\nu}^{\mathrm{matter}}
+
T_{\mu\nu}^{U}
\right).
}
\]

The uncertainty stress-energy tensor is

\[
T_{\mu\nu}^{U}
=
\frac{1}{\gamma^2}
\left(
\mathcal F_{\mu\alpha}^a
\mathcal F_{\nu}^{a\ \alpha}
-
\frac{1}{4}
g_{\mu\nu}
\mathcal F_{\alpha\beta}^a
\mathcal F_a^{\alpha\beta}
\right)
+
\nabla_\mu h\nabla_\nu h
-
g_{\mu\nu}
\left(
\frac{1}{2}\nabla_\alpha h\nabla^\alpha h
+
V(h)
\right).
\]

Thus uncertainty contributes gravitationally.

---

## 8. Residual Uncertainty as Dark Energy

Assume a homogeneous and slowly varying uncertainty scalar,

\[
h=h(t),
\qquad
|\dot h|^2\ll V(h).
\]

In a spatially flat FLRW background, the uncertainty energy density and pressure are

\[
\rho_U
=
\frac{1}{2}\dot h^2+V(h),
\]

\[
p_U
=
\frac{1}{2}\dot h^2-V(h).
\]

If \(\dot h\approx 0\), then

\[
p_U\approx -\rho_U.
\]

Thus the equation of state is

\[
w_U=\frac{p_U}{\rho_U}\approx -1.
\]

The residual uncertainty behaves as a cosmological constant,

\[
\Lambda_\mathrm{eff}
=
\kappa V(h_\infty),
\]

where

\[
h_\infty=\lim_{t\to\infty}h(t)
\]

is the irreducible uncertainty remaining after all admissible information has been applied.

Therefore,

\[
\boxed{
\text{dark energy can be interpreted as gravitating residual uncertainty.}
}
\]

This is not a stochastic vacuum energy. It is a geometric consequence of irreducible non-identification.

---

## 9. Quantum Mechanics as an Additive Chart

Quantum theory emerges when the uncertainty algebra becomes noncommutative but admits additive expectation states.

Let \(\mathcal A\) be a \(C^\ast\)-algebra of observables. A pre-probabilistic state is a positive normalized linear functional

\[
\omega:\mathcal A\to\mathbb C,
\]

with

\[
\omega(A^\ast A)\ge 0,
\qquad
\omega(\mathbf 1)=1.
\]

No probability measure is primitive. The Gelfand–Naimark–Segal construction yields a Hilbert space \(\mathcal H_\omega\), a representation \(\pi_\omega\), and a cyclic vector \(\Omega_\omega\) such that

\[
\omega(A)=\langle \Omega_\omega,\pi_\omega(A)\Omega_\omega\rangle.
\]

For a projection \(\Pi_E\), the additive chart gives

\[
P(E)=\omega(\Pi_E).
\]

Thus the Born rule appears only after the additive Hilbert-space chart has been chosen.

The deeper object is the algebraic uncertainty state \(\omega\), not the probability \(P\).

---

## 10. Minimal Symplectic Capacity and the Origin of \(\hbar\)

In standard quantum mechanics, \(\hbar\) appears as a constant in commutation relations. In the present framework, \(\hbar\) arises as a minimal admissible symplectic capacity of possibility regions.

Let \(\Omega_U\subset\Gamma\) be a physically admissible possibility region. Define its symplectic capacity \(c(\Omega_U)\). We postulate:

\[
\boxed{
c(\Omega_U)\ge 2\pi\hbar.
}
\]

This is not a statement about measurement disturbance. It is a geometric restriction on admissible possibility regions.

For a canonical pair \((q,p)\), let

\[
\Delta_U q=\sup_{\Omega_U}q-\inf_{\Omega_U}q,
\]

\[
\Delta_U p=\sup_{\Omega_U}p-\inf_{\Omega_U}p.
\]

For centrally symmetric convex regions, symplectic non-squeezing implies

\[
\boxed{
\Delta_U q\,\Delta_U p\ge \frac{\hbar}{2}.
}
\]

More generally,

\[
\Delta_U q\,\Delta_U p\ge \eta_U\hbar,
\]

where \(\eta_U\ge 1/2\) is a shape-dependent geometric factor.

This uncertainty relation is not derived from variance. It is derived from the impossibility of compressing a possibility region below a minimal symplectic capacity.

Thus:

\[
\boxed{
\hbar=\text{quantum of admissible possibility volume.}
}
\]

---

## 11. Measurement as Refinement, Not Collapse

In the present theory, measurement is not fundamentally stochastic collapse. It is an evidence operation

\[
\mathcal E_E:U\mapsto U_E.
\]

For a sharp constraint,

\[
U_E=U\cap E.
\]

The probability-free update law is

\[
\boxed{
U\longrightarrow U\cap E.
}
\]

If an additive probability chart exists, then this becomes

\[
P'(A)=\frac{P(A\cap E)}{P(E)}.
\]

But the primitive operation is set-theoretic or algebraic refinement.

Apparent randomness arises when an additive chart is forced after refinement. The unresolved alternatives prior to refinement are not weighted; they are merely compatible.

---

## 12. Noncommuting Evidence and Contextuality

Let two evidence operations be \(\mathcal E_a\) and \(\mathcal E_b\). In general,

\[
\mathcal E_a\mathcal E_b U
\neq
\mathcal E_b\mathcal E_a U.
\]

Define the evidence commutator

\[
[\mathcal E_a,\mathcal E_b]U
=
\mathcal E_a\mathcal E_bU
-
\mathcal E_b\mathcal E_aU.
\]

Nonzero commutators imply that the order of information acquisition changes the resulting uncertainty structure.

This gives a structural origin of contextuality. It is not a failure of hidden variables; it is a failure of global commutative information refinement.

In the quantum sector, this becomes

\[
[\hat A,\hat B]\neq 0.
\]

But the deeper statement is:

\[
\boxed{
\text{information operations need not commute.}
}
\]

---

## 13. Uncertainty Holonomy and Interference

Suppose a physical process admits two alternative possibility channels, labeled \(1\) and \(2\). Locally, an additive chart may exist. However, if the uncertainty connection has nontrivial curvature, the charts on the two channels differ by a holonomy.

Let

\[
\theta_{12}
=
\oint_{\Gamma_{12}}\mathcal A
=
\int_{\Sigma_{12}}\mathcal F
\]

be the uncertainty holonomy between the two channels.

In an additive chart, the observed probability takes the form

\[
P
=
|\psi_1+\psi_2|^2
+
\delta P_{12},
\]

where the correction is

\[
\delta P_{12}
=
2|\psi_1||\psi_2|
\left[
\cos(\Delta\phi+\theta_{12})
-
\cos(\Delta\phi)
\right].
\]

If \(\theta_{12}=0\), ordinary quantum interference is recovered. If \(\theta_{12}\neq 0\), the interference pattern is shifted by uncertainty curvature.

Thus the theory predicts deviations from standard Born interference in regimes where information curvature is nonzero.

---

## 14. Noncommutative Coordinates from Uncertainty Curvature

If the uncertainty curvature is nonzero at the level of configuration space, effective noncommutative coordinates emerge. Let

\[
\theta^{ij}
=
\ell_U^2\mathcal F^{ij},
\]

where \(\ell_U\) is a characteristic uncertainty length. Then the effective coordinate algebra satisfies

\[
\boxed{
[x^i,x^j]=i\theta^{ij}.
}
\]

This noncommutativity is not imposed ad hoc. It arises because local possibility charts cannot be globally identified.

Thus:

\[
\boxed{
\text{noncommutative geometry is a macroscopic shadow of uncertainty curvature.}
}
\]

---

## 15. Generalized Uncertainty Relation in Tensor Form

Let \(f^A=(q^i,p_i)\) be phase-space coordinates and let \(\omega_{AB}\) be the symplectic matrix. Define the geometric uncertainty tensor

\[
\Sigma_U^{AB}
=
\frac{1}{V_U}
\int_{\Omega_U}
(f^A-\bar f^A)(f^B-\bar f^B)\,\Omega,
\]

where \(\bar f^A\) is the centroid with respect to the reference volume form. This tensor is a shape descriptor, not a probabilistic covariance.

The symplectic invariant

\[
\mathcal I_U
=
\frac{1}{2}
\omega_{AC}\omega_{BD}
\Sigma_U^{AB}\Sigma_U^{CD}
\]

measures the symplectic spread of the possibility region.

The minimal-capacity condition implies

\[
\boxed{
\mathcal I_U\ge \frac{\hbar^2}{4}.
}
\]

In canonical coordinates this reduces to

\[
\Sigma_U^{qq}\Sigma_U^{pp}
-
(\Sigma_U^{qp})^2
\ge
\frac{\hbar^2}{4}.
\]

This is a tensorial, geometric uncertainty principle.

---

## 16. Classical, Quantum, and Statistical Limits

The theory contains several limiting regimes.

### 16.1 Classical Singleton Limit

If

\[
U=\{x\},
\]

then uncertainty vanishes. The dynamics reduces to ordinary Hamiltonian mechanics.

### 16.2 Classical Ensemble Limit

If \(U\) is large and boundary curvature is negligible,

\[
\beta K\approx 0,
\]

then the generalized Hamilton–Jacobi equation reduces to the classical Hamilton–Jacobi equation.

### 16.3 Quantum Limit

If possibility regions are constrained by minimal symplectic capacity and evidence operations are noncommutative, the additive chart yields Hilbert-space quantum mechanics.

### 16.4 Statistical Limit

If a unique additive normalized measure exists and information is purely Bayesian, the theory reduces to classical probability theory.

Thus:

\[
\boxed{
\text{probability is a sector, not the foundation.}
}
\]

---

## 17. Experimental Signatures

The theory predicts several possible deviations from standard physics.

### 17.1 Interferometric Holonomy Shifts

In an interferometer, the phase shift receives an additional contribution

\[
\delta\phi=\theta_{12}
=
\int_{\Sigma_{12}}\mathcal F.
\]

This effect is not due to electromagnetic or gravitational potentials alone. It is due to curvature of the uncertainty connection.

### 17.2 Born-Rule Deviations

For coherent alternatives,

\[
P=|\psi_1+\psi_2|^2+\delta P_{12}.
\]

The correction is controlled by uncertainty curvature and should vanish when local additive charts glue globally.

### 17.3 Modified Wavepacket Boundary Dynamics

Wavepacket boundaries obey

\[
\partial_t S+H=\beta K.
\]

This predicts small curvature-dependent corrections to spreading and focusing, especially in constrained or high-precision systems.

### 17.4 Cosmological Residual Uncertainty

If the universe retains an irreducible uncertainty scalar \(h_\infty\), then

\[
\Lambda_\mathrm{eff}=\kappa V(h_\infty).
\]

The dark-energy equation of state may deviate slightly from \(w=-1\) if \(h(t)\) evolves slowly.

### 17.5 Effective Noncommutativity

At scales where \(\mathcal F^{ij}\) is significant,

\[
[x^i,x^j]=i\ell_U^2\mathcal F^{ij}.
\]

This may produce direction-dependent noncommutative signatures in high-energy or precision systems.

---

## 18. Conceptual Consequences

The theory changes the interpretation of several foundational notions.

### 18.1 Unknown Is Not Random

If

\[
x\in U,
\qquad
|U|>1,
\]

this does not imply a probability distribution over \(U\). Unknown does not mean random.

### 18.2 Possible Is Not Probable

A possibility degree is not a probability unless additivity is imposed.

### 18.3 Measurement Is Not Essentially Stochastic

Measurement is refinement:

\[
U\mapsto U\cap E.
\]

Stochastic collapse is a derived representation.

### 18.4 Quantum Noncommutativity Is Information-Structural

Noncommuting observables arise because evidence operations and context charts fail to commute.

### 18.5 Probability Is a Coordinate Chart

Probability is to uncertainty what coordinates are to a manifold. A chart may be useful, but it is not the manifold.

---

## 19. Central Theorem

We conclude with the foundational theorem of the theory.

### Theorem 2: Physical Precedence of Uncertainty Structure

Let \(\mathfrak U\) be a coherent physical uncertainty structure. Any probabilistic representation

\[
\Phi:\mathfrak U\to \mathcal P(\mathcal X)
\]

is valid only if it preserves the relevant refinement, compatibility, and update operations of \(\mathfrak U\). Therefore probability is a derived representation of physical uncertainty, not its definition.

**Proof.** The physical content of \(\mathfrak U\) is encoded in the relations

\[
\preceq,\quad \mathcal R,\quad \mathcal E.
\]

A map \(\Phi\) represents \(\mathfrak U\) probabilistically only if for all admissible \(U_1,U_2\),

\[
U_1\preceq U_2
\Rightarrow
\Phi(U_1)\preceq_P\Phi(U_2),
\]

and for all evidence operations,

\[
\Phi(\mathcal E_e(U))
=
\mathcal E^P_e(\Phi(U)),
\]

where \(\mathcal E^P_e\) is the probabilistic update, such as conditioning. If no such structure-preserving map exists, the probability chart misrepresents the uncertainty structure. Hence probability is secondary to the structure it represents.

\[
\boxed{\square}
\]

---

## 20. Conclusion

We have derived a physical theory from the mathematics of uncertainty without probability. The resulting framework replaces the primacy of probability with the primacy of unresolved possibility.

The central objects are not distributions but possibility regions, information refinements, compatibility relations, evidence morphisms, and uncertainty geometries.

The main results are:

\[
\boxed{
\text{Hamiltonian dynamics conserves possibility volume.}
}
\]

\[
\boxed{
\text{Evidence contracts uncertainty regions.}
}
\]

\[
\boxed{
\text{Possibility boundaries obey curvature-corrected Hamilton--Jacobi dynamics.}
}
\]

\[
\boxed{
\text{Information incompatibility produces gauge curvature.}
}
\]

\[
\boxed{
\text{Residual uncertainty can gravitate as dark energy.}
}
\]

\[
\boxed{
\text{Quantum mechanics emerges as an additive chart on noncommutative uncertainty.}
}
\]

\[
\boxed{
\text{Probability is a representation, not the foundation.}
}
\]

The foundational question of physics therefore changes from

\[
\boxed{
\text{What probability distribution describes the system?}
}
\]

to

\[
\boxed{
\text{What uncertainty structure does the system possess?}
}
\]

This is the starting point of uncertainty mechanics.

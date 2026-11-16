# Structural Evasion of the Ostrogradsky Instability in Universal Phase Theory

### Lyapunov–Schmidt Rank Deficiency, Hessian Geometry, and the Gauss–Horndeski Mechanism

**UPT Foundational Series · Working Paper UPT-F/2026-04**
**16 November 2026**

**MSC 2020.** Primary 70H50; Secondary 53B12, 58K05, 70H45, 37G10, 83D05.
**Keywords.** Ostrogradsky theorem; higher-derivative Lagrangians; degenerate kinetic matrices; Lyapunov–Schmidt reduction; Hessian metrics; information geometry; Horndeski theory; emergent gravity; bifurcation; phase substrate.

---

## Abstract

Universal Phase Theory (UPT) posits a fundamental action $S_\Phi=\int\mathcal L(\Phi,D\Phi,D^2\Phi,\mathcal R_\Phi,\mathcal I_\Phi)\,d\mu_\Phi$ whose Lagrangian depends on second covariant derivatives of the primitive field. Ostrogradsky's theorem is routinely invoked to conclude that any such theory is fatally unstable. We show that this inference is false for the UPT class, and false *structurally* rather than by tuning. Three independent mechanisms are proved. **(I)** Lyapunov–Schmidt mediation forces the acceleration Hessian to factor through the critical kernel $K_\Phi=\ker\mathscr L_\Phi$, giving $\operatorname{rank}\mathcal H\le k=\dim K_\Phi$ and $N-k$ primary constraints. **(II)** The stiff sector is slaved by an invertible operator; the reduced dynamics is symplectically equivalent to a first-order parent and carries no additional modes. **(III)** The phase metric $g^\Phi_{ij}=T_{ia}\chi^{ab}T_{jb}$ is the pullback of a *dual Hessian metric*; its Christoffel symbols are totally symmetric, fourth derivatives cancel identically in the Riemann tensor, and the Gauss equation of the order-parameter immersion renders $\sqrt{-g^\Phi}R^\Phi$ **affine in accelerations**, with acceleration Hessian identically zero. Mechanism III reproduces precisely the Horndeski $\mathcal L_4$ combination $(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)^2$, thereby *deriving* rather than postulating the ghost-free structure. We prove corollaries: an emergent-dimension bound $d_{\rm eff}\le k$; Lorentzian signature $\Leftrightarrow$ Morse index one; $R^\Phi=\tfrac14(\|\Theta\|^2-|v|^2)$ with $\Theta$ the cubic phase coupling; and a flatness rigidity theorem via Jörgens–Calabi–Pogorelov. A worked model violating the mediation axiom is exhibited with a genuine Pais–Uhlenbeck ghost, establishing sharpness. This is a counterexample to the *applicability* of Ostrogradsky's theorem, not to the theorem.

---

## 1. Introduction

### 1.1 The obstruction

Universal Phase Theory takes as primitive a phase field $\Phi\in\Gamma(E_\Phi)$ over a base $\mathcal X$ that is *not* assumed to be spacetime, and derives geometry, connections, spectra and observables as functionals of $\Phi$ [1]. Its foundational action is

$$
S_\Phi=\int_{\mathcal X}\mathcal L\!\left(\Phi,\,D\Phi,\,D^2\Phi,\,\mathcal R_\Phi,\,\mathcal I_\Phi\right)d\mu_\Phi .
\tag{1.1}
$$

Two features of (1.1) are, from the standpoint of higher-derivative dynamics, alarming. First, $D^2\Phi$ appears explicitly. Second, the emergent metric is itself a functional of the phase field,

$$
g^\Phi_{ij}=T_{ia}\,\chi^{ab}\,T_{jb},
\qquad
\chi^{ab}=(S^{-1})^{ab},
\qquad
S_{ab}=\frac{\partial^2 \mathcal W}{\partial\eta^a\partial\eta^b},
\tag{1.2}
$$

so that any curvature scalar built from $g^\Phi$ automatically contains second derivatives of $\Phi$. A theory of the form (1.1) is therefore *intrinsically* higher-derivative. It cannot be made second-order by fiat, and it cannot be treated as an effective field theory with the higher-derivative operators discarded, because those operators are the very mechanism by which geometry is supposed to emerge.

The standard objection is then immediate. Ostrogradsky's theorem [2,3] states that a nondegenerate Lagrangian depending on $q^{(n)}$ with $n\ge2$ yields a Hamiltonian linear in $n-1$ canonical momenta, hence unbounded above and below. Applied to (1.1), the objection reads: *UPT is dead on arrival.*

### 1.2 What we prove

The objection is invalid, and its invalidity is not accidental. We prove that the UPT construction **cannot** satisfy Ostrogradsky's nondegeneracy hypothesis, and that this failure is forced by the same structural axioms that define the theory.

The logical situation must be stated with precision, because the literature is careless about it. Ostrogradsky's theorem is *true*. What is false is the informal corollary that is almost universally drawn from it:

> **(OF) The Ostrogradsky Fallacy.** *Any fundamental action containing second derivatives of its primitive field is fatally unstable.*

(OF) is not a theorem; it is an inference that silently assumes nondegeneracy. We construct a counterexample to (OF) whose nondegeneracy failure is a *theorem of the framework*, not a tuning of coupling functions.

Our results are as follows.

**Theorem A (Kernel rank deficiency).** Under the mediation axiom (H5), the acceleration Hessian factors as $\mathcal H^{AB}=\partial_Au_a\,\partial_Bu_b\,\hat{\mathcal H}^{ab}$ with $a,b\le k$. Hence $\operatorname{rank}\mathcal H\le k$ and there are $N-k$ primary constraints. (§4)

**Theorem B (Slaving equivalence).** Lyapunov–Schmidt elimination of the stiff sector is the elimination of a field with invertible linearization. The exact reduced theory is in solution-bijection with a first-order parent and carries no extra modes. (§5)

**Theorem C (Hessian curvature).** $g^\Phi$ is the pullback of the Hessian metric of the Legendre-dual potential $\mathcal W^*$. Its Christoffel symbols are totally symmetric; fourth derivatives cancel identically; and
$$
R^\Phi=\tfrac14\left(\|\Theta\|^2-|v|^2\right),\qquad \Theta_{abc}=\partial_a\partial_b\partial_c\mathcal W^*,\quad v_a=\partial_a\log\det h .
$$
(§7)

**Theorem D (Gauss–Horndeski).** The Gauss equation of the order-parameter immersion gives $R^\Lambda=R^{\rm amb}+\|\operatorname{tr}\mathrm{II}\|^2-\|\mathrm{II}\|^2$. The acceleration-squared terms cancel identically. Consequently $\hat{\mathcal H}^{ab}\equiv0$: the emergent gravitational Lagrangian is *affine*, not merely degenerate, in accelerations. The surviving combination is exactly Horndeski's $\mathcal L_4$ structure. (§8)

**Theorem D′ (ADM order reduction).** Modulo a total divergence, $\sqrt{-g^\Phi}R^\Phi$ is first order in time derivatives of $\Phi$. Ostrogradsky's construction cannot be initiated. (§8.4)

**Theorem E (Signature transmutation).** $\operatorname{sig}(g^\Phi)=\operatorname{sig}(S)$ on the image of $T$. Lorentzian signature requires Morse index one. The single negative direction of the phase Hessian becomes the *timelike direction of emergent spacetime*, not a negative-energy mode. (§9)

Combining these with Lemmas 6.1–6.3 (which show that the connection and topological sectors contain no second derivatives at all), we obtain the Main Theorem (§10).

### 1.3 Relation to prior evasions

The known routes around Ostrogradsky are: (i) degeneracy of the highest-derivative Hessian, exploited in $f(R)$, Galileon, Horndeski, beyond-Horndeski and DHOST theories [8–13]; (ii) gauge constraints; (iii) nonlocality [16]; (iv) effective-field-theory postponement above a cutoff [17]; (v) Lee–Wick/fakeon contour prescriptions; (vi) $\mathcal{PT}$-symmetric quantization with a modified inner product [14,15].

UPT belongs to family (i), but with a decisive difference of *epistemic status*. In Horndeski and DHOST, degeneracy is **imposed**: one writes down a general higher-derivative ansatz with free functions and then solves algebraic conditions on those functions to kill the ghost. The ghost-free locus is a measure-zero subset of theory space, selected by hand. In UPT, degeneracy is **derived**: it is a consequence of the definition of the phase field, the Lyapunov–Schmidt structure of admissibility, and the response-theoretic construction of the metric. There is no free function to tune. The ghost-free locus is the *entire* admissible configuration space.

This is the sense in which UPT is a counterexample worth recording. It is not a new evasion mechanism; it is a demonstration that an existing mechanism can be *forced by a foundational principle* rather than imposed as a constraint on couplings.

### 1.4 A remark on the meaning of "counterexample"

We do not claim, and nothing below implies, that Ostrogradsky's theorem admits exceptions. We claim:

$$
\mathcal C_\Phi^{\rm UPT}\ \subset\ \Sigma_{\rm deg}:=\{\Phi:\det\mathcal H(\Phi)=0\},
\tag{1.3}
$$

i.e. the UPT admissible set lies entirely inside the locus where hypothesis (O1) fails. Section 11.4 exhibits a UPT-*admissible-in-the-loose-sense* model that violates the mediation axiom and does possess a genuine ghost. The hypotheses are therefore sharp and the result non-vacuous.

We also emphasize a distinction that will matter throughout: **UPT is always Ostrogradsky-degenerate, and only sometimes UPT-critical.** The Ostrogradsky degeneracy locus $\Sigma_{\rm deg}$ and the UPT critical manifold $\Sigma_\Phi=\{\Delta_\Phi=0\}$ are different loci. Conflating them is the most common error in informal discussion of this material.

---

## 2. Ostrogradsky's Theorem: Statement, Proof, and Logical Anatomy

### 2.1 Setting

Let $Q\subset\mathbb R^N$ be open with coordinates $q^A$, and let
$$
L:T^{(n)}Q\to\mathbb R,\qquad
L=L\!\left(q^A,\dot q^A,\ldots,q^{(n)A}\right),\qquad n\ge2 .
$$

**Hypothesis (O1) — Nondegeneracy.**
$$
\det\!\left(\frac{\partial^2L}{\partial q^{(n)A}\,\partial q^{(n)B}}\right)\neq0 .
\tag{2.1}
$$

**Hypothesis (O2) — Locality and finite order.** $L$ depends on finitely many derivatives at a single time.

**Hypothesis (O3) — Unconstrained Legendre map.** The map $(q,\ldots,q^{(2n-1)})\mapsto(Q_i,P_i)$ defined below is a local diffeomorphism onto an open set of $\mathbb R^{2nN}$.

**Hypothesis (O4) — Standard symplectic quantization.** Dynamics is generated by $H$ via the canonical form $\omega=dP_i\wedge dQ_i$, with real phase space and the standard positivity structure.

### 2.2 The construction

Define Ostrogradsky coordinates
$$
Q_i^A:=q^{(i-1)A},\qquad
P_i^A:=\sum_{j=i}^{n}\left(-\frac{d}{dt}\right)^{j-i}\frac{\partial L}{\partial q^{(j)A}},
\qquad i=1,\ldots,n .
\tag{2.2}
$$
In particular $P_n^A=\partial L/\partial q^{(n)A}$. By (O1) and the implicit function theorem this may be inverted:
$$
q^{(n)A}=\mathcal A^A(Q_1,\ldots,Q_n,P_n).
\tag{2.3}
$$
The Hamiltonian is
$$
H=\sum_{i=1}^{n-1}P_i^A\,Q_{i+1}^A+P_n^A\mathcal A^A-L\!\left(Q_1,\ldots,Q_n,\mathcal A\right).
\tag{2.4}
$$

**Theorem 2.1 (Ostrogradsky).** *Under (O1)–(O3), $H$ is affine in $P_1,\ldots,P_{n-1}$ with coefficients $Q_2,\ldots,Q_n$ that are independent coordinates ranging over open sets. Hence $H$ is unbounded above and below on every nonempty open subset of phase space.*

*Proof.* Immediate from (2.4): the only appearance of $P_1,\ldots,P_{n-1}$ is in the first sum, which is linear. By (O3) these momenta are free coordinates. Fixing $Q_2\neq0$ and letting $P_1\to\pm\infty$ along a fixed direction gives $H\to\pm\infty$. $\square$

### 2.3 From unboundedness to instability

Unboundedness alone is not instability. The free Pais–Uhlenbeck oscillator has unbounded $H$ and perfectly regular, quasi-periodic solutions: the positive- and negative-energy sectors decouple. The catastrophe requires interaction.

**Proposition 2.2 (Resonance mechanism).** *Let $H=H_+(z_+)-H_-(z_-)+\epsilon\,V(z_+,z_-)$ with $H_\pm$ positive definite and proper on their factors, and suppose $\partial^2V/\partial z_+\partial z_-\neq0$ on an open set. Then for generic initial data there exist solutions with $\|z_\pm(t)\|\to\infty$; the runaway time scales as $\epsilon^{-1}$ times a characteristic period.*

*Proof sketch.* The interaction transports energy from the negative sector to the positive sector while conserving $H$; both energies grow without bound at fixed total. Properness of $H_\pm$ converts energy growth into phase-space escape. Non-vanishing mixed Hessian guarantees the transport channel is open. $\square$

Thus (OF) requires three ingredients: unboundedness, interaction, and non-compactness of the joint energy surface. UPT will remove the *first*, which is the strongest form of evasion.

### 2.4 The four logical exits

A theory escapes Theorem 2.1 by violating exactly one of:

| Exit | Hypothesis violated | Representative |
|---|---|---|
| E1 | (O1) nondegeneracy | Horndeski, DHOST, $f(R)$ |
| E2 | (O2) locality/finite order | infinite-derivative gravity |
| E3 | (O3) unconstrained Legendre | gauge theories, slaved fields |
| E4 | (O4) standard quantization | $\mathcal{PT}$-symmetric PU |

UPT uses **E1 and E3 jointly**, and requires neither E2 nor E4. This is important: the evasion is entirely classical and does not depend on a nonstandard inner product. We will not need $\mathcal{PT}$ symmetry (§13).

### 2.5 A warning on partial degeneracy

For $N>1$, $\det\mathcal H=0$ is *not* sufficient. If $\operatorname{rank}\mathcal H=r$ with $1\le r<N$ and the nonzero $r\times r$ block is invertible, one obtains $r$ Ostrogradsky modes and $N-r$ constrained directions; the $r$ modes are generically ghosts. The correct sufficient condition, established in the degenerate-higher-order literature [11–13], is that the *full* kinetic matrix — including mixing between the higher-derivative field and any auxiliary sector — be degenerate, with the resulting primary constraint generating a secondary constraint that removes the would-be ghost.

We flag this explicitly because Theorem A alone gives only $\operatorname{rank}\mathcal H\le k$, which is **insufficient**. The elimination is completed by Theorems B, D and D′. Any presentation claiming that Lyapunov–Schmidt reduction *by itself* defeats Ostrogradsky is wrong.

---

## 3. UPT: Axioms and Standing Hypotheses

We now fix the sector of UPT under analysis and state the hypotheses precisely. Everything in this section is either taken from [1] or is an explicit specification made necessary by the imprecision of the source formulation.

### 3.1 Geometric data

- $\pi:E_\Phi\to\mathcal X$, a fibre bundle with $\dim\mathcal X=d$, fibre $\mathcal M_\Phi$ of real dimension $N$.
- $\Phi\in\Gamma(E_\Phi)$, components $\Phi^A$, $A=1,\ldots,N$.
- $\Lambda$: control manifold, coordinates $\lambda^i$, $i=1,\ldots,d$.
- $\mathscr F:\Gamma(E_\Phi)\times\Lambda\to\Gamma(F_\Phi)$, the admissibility operator, $\mathscr F[\Phi;\lambda]=0$.
- $\mathscr L_\Phi:=D_\Phi\mathscr F$, the stability operator.

### 3.2 Standing hypotheses

**(H1) Fredholm regularity.** On the Sobolev completion $H^s$, $s$ sufficiently large, $\mathscr L_\Phi$ is Fredholm of index zero. Write $K_\Phi=\ker\mathscr L_\Phi$, $k:=\dim K_\Phi<\infty$.

**(H2) Regular stratum.** There is an open stratum $\mathcal C^{\rm reg}\subset\mathcal C_\Phi$ on which $k$ is locally constant and on which the pointwise soft projector has constant rank. We work on $\mathcal C^{\rm reg}$; §12 treats the boundary.

**(H3) Stiff invertibility.** With $\mathcal C=K\oplus R$ the $L^2$-orthogonal splitting and $P$ the projection onto $\operatorname{coker}\mathscr L\cong K$, the operator $(I-P)\mathscr L|_R$ is boundedly invertible.

**(H4) Spectral gap.** $\operatorname{spec}(\mathscr L|_R)$ is bounded away from zero by $\Lambda_{\rm stiff}>0$.

**(H5) Mediation.** *All* dependence of $\mathcal L$ on second derivatives of $\Phi$ enters through
 (a) the geometric response $\mathcal R_\Phi=\mathcal R[g^\Phi]$, and
 (b) the stiff-sector slaving.
There is no independent higher-derivative operator in the soft sector.

**(H6) Variational realization.** $\mathscr F=\delta S_\Phi/\delta\Phi$.

Hypothesis (H5) is the substantive one. It is not an arbitrary restriction: §6 shows that within the UPT construction the connection and topological sectors *automatically* contain no second derivatives, so (H5) reduces to the statement that the phase-kinetic term is the standard sigma-model one, $\tfrac12 G_{ab}\partial\Phi^a\partial\Phi^b$, as written in Part XVII of [1]. Section 11.4 shows what happens when (H5) is dropped.

### 3.3 Lyapunov–Schmidt reduction

Write $\Phi=\eta^ae_a+\xi$, $\xi\in R$, with $\{e_a\}_{a=1}^k$ a basis of $K_\Phi$. The equation $\mathscr F=0$ splits:
$$
(I-P)\mathscr F(\eta+\xi,\lambda)=0,
\qquad
P\mathscr F(\eta+\xi,\lambda)=0 .
\tag{3.1}
$$
By (H3) and the implicit function theorem the first equation has a unique local solution
$$
\xi=\xi_*(\eta,\lambda),\qquad \xi_*(0,\lambda_*)=0,\qquad D_\eta\xi_*(0,\lambda_*)=0 .
\tag{3.2}
$$
Substituting gives the **reduced bifurcation equation**
$$
\mathfrak b(\eta,\lambda):=P\mathscr F\!\left(\eta+\xi_*(\eta,\lambda),\lambda\right)=0,
\qquad \mathfrak b:\mathbb R^k\times\Lambda\to\mathbb R^k .
\tag{3.3}
$$

**Lemma 3.1 (Reduced action principle).** *Under (H6), define $S_{\rm red}(\eta,\lambda):=S_\Phi[\eta+\xi_*(\eta,\lambda),\lambda]$. Then*
$$
\frac{\partial S_{\rm red}}{\partial\eta^a}=\left\langle \frac{\delta S_\Phi}{\delta\Phi},\,e_a+\partial_a\xi_*\right\rangle=\big\langle\mathfrak b,\,e_a\big\rangle .
$$

*Proof.* Chain rule, then note $(I-P)\,\delta S_\Phi/\delta\Phi=0$ on the slaving surface by (3.1), so the $\partial_a\xi_*$ term is annihilated. $\square$

Thus reduction commutes with variation: the reduced action generates the reduced equation. Write $\mathcal W(\eta)$ for the reduced potential, $S_{\rm red}=\int(\text{kinetic})-\mathcal W$. In the notation of [1], $\mathcal W\equiv\Phi_{\rm eff}$.

### 3.4 The two levels

UPT operates at two levels and we keep them distinct throughout.

**Level I (moduli).** $\eta\in\mathbb R^k$ are collective coordinates; $\xi_*$ is an algebraic function of $\eta$; the reduced system is mechanics on $\mathbb R^k$. Theorem B applies exactly.

**Level II (fields).** $\eta^a=\eta^a(x)$ are promoted to local fields (adiabatic promotion of moduli); $\xi_*$ is the inverse of a differential operator; the derivative expansion of $S_{\rm red}$ generates higher-derivative terms. Theorems C, D, D′ control this level.

Failure to distinguish these levels is the source of most confusion about higher derivatives in reduced descriptions.

---

## 4. Mechanism I: Kernel Rank Deficiency

### 4.1 The dual order-parameter map

The construction (1.2) requires specification of $T_{ia}$. In [1] it is written $T_{ia}=\partial\eta_a/\partial\lambda^i$ with an ambiguous index position. We make the natural choice explicit.

**Definition 4.1 (Conjugate response).** Let $\mathcal W:\mathbb R^k\to\mathbb R$ be the reduced potential with invertible Hessian $S_{ab}=\partial_a\partial_b\mathcal W$. Define the **conjugate order parameters**
$$
u_a:=\frac{\partial\mathcal W}{\partial\eta^a},
\qquad
\chi^{ab}:=(S^{-1})^{ab}=\frac{\partial\eta^a}{\partial u_b},
\tag{4.1}
$$
and the response tensor
$$
T_{ia}:=\frac{\partial u_a}{\partial\lambda^i}
=\frac{\partial u_a}{\partial\Phi^A}\,\partial_i\Phi^A .
\tag{4.2}
$$

The second equality in (4.2) is the crucial structural fact: **$u_a$ is an algebraic function of $\Phi$**, so $T$ is *first order* in $\Phi$. Consequently
$$
g^\Phi_{ij}=g^\Phi_{ij}(\Phi,\partial\Phi),
\tag{4.3}
$$
with no second derivatives. Everything in §7–§8 rests on (4.3).

### 4.2 The rank theorem

Let $\ddot\Phi^A$ denote the acceleration in a fixed foliation (more covariantly, $n^\mu n^\nu\nabla_\mu\nabla_\nu\Phi^A$ with $n$ the unit normal), and set
$$
\mathcal H^{AB}:=\frac{\partial^2\mathcal L}{\partial\ddot\Phi^A\,\partial\ddot\Phi^B}.
$$

**Theorem A.** *Assume (H1)–(H5). Then*
$$
\mathcal H^{AB}=\frac{\partial u_a}{\partial\Phi^A}\,\frac{\partial u_b}{\partial\Phi^B}\;\hat{\mathcal H}^{ab},
\qquad
\hat{\mathcal H}^{ab}:=\frac{\partial^2\mathcal L}{\partial\ddot u_a\,\partial\ddot u_b},
\tag{4.4}
$$
*and therefore*
$$
\operatorname{rank}\mathcal H\ \le\ \min\!\left(k,\ \operatorname{rank}\hat{\mathcal H}\right)\ \le\ k .
$$
*In particular $\det\mathcal H=0$ whenever $k<N$, and the Ostrogradsky momenta obey $N-k$ primary constraints*
$$
\phi_{(p)}:=\Pi_A\,\mathfrak n^A_{(p)}\approx0,\qquad p=1,\ldots,N-k,
\tag{4.5}
$$
*where $\{\mathfrak n_{(p)}\}$ spans $\operatorname{coker}(du)$ and $\Pi_A=\partial\mathcal L/\partial\ddot\Phi^A$.*

*Proof.* By (H5) the only $\ddot\Phi$-dependence is via $\mathcal R[g^\Phi]$ and slaving. By (4.3), $g^\Phi$ contains no accelerations, so $\mathcal R[g^\Phi]$ depends on $\ddot\Phi$ only through $\ddot u_a=\partial_Au_a\,\ddot\Phi^A+\partial_A\partial_Bu_a\,\dot\Phi^A\dot\Phi^B$. The slaved sector contributes $\ddot\Phi$ only through the same channel, since $\xi_*$ is determined by $\eta$ and hence by $u$. Chain rule twice gives (4.4). The rank bound is the rank of a product. For (4.5), $\Pi_A=\partial_Au_a\,\hat\Pi^a$ lies in $\operatorname{im}(du)^{\mathsf T}$, whose annihilator has dimension $N-k$. $\square$

### 4.3 What Theorem A does and does not establish

Theorem A is *robust*: it survives weakening of the geometric assumptions, requiring only mediation through a finite-rank response. But by §2.5 it is **not sufficient**. If $\hat{\mathcal H}$ is invertible on the $k$-dimensional soft block, UPT propagates $k$ Ostrogradsky ghosts rather than $N$. The reduction from $N$ to $k$ is a quantitative improvement, not an evasion.

The elimination of $\hat{\mathcal H}$ is the content of Theorem D. We record the honest logical dependency:
$$
\text{A (rank}\le k)\ \wedge\ \text{D}\ (\hat{\mathcal H}=0)\ \Longrightarrow\ \mathcal H\equiv0 .
$$

### 4.4 A corollary on emergent dimension

The same factorization that produces rank deficiency constrains the emergent geometry.

**Corollary A.1 (Dimension bound).** *$g^\Phi=T\chi T^{\mathsf T}$ is nondegenerate on $\Lambda$ only if $\operatorname{rank}T=d$, hence only if*
$$
\boxed{\ d_{\rm eff}\ \le\ k=\dim\ker\mathscr L_\Phi\ .}
\tag{4.6}
$$

*Proof.* $\operatorname{rank}(T\chi T^{\mathsf T})\le\operatorname{rank}T\le\min(d,k)$. Nondegeneracy of a $d\times d$ matrix requires rank $d$. $\square$

This is a genuine, derived, quantitative statement addressing Q3 of [1]: **the emergent spacetime dimension is bounded above by the dimension of the critical kernel.** A four-dimensional emergent spacetime requires at least a four-dimensional soft sector. The bound is necessary, not sufficient; we do not claim to derive $d=4$. But it converts "why four dimensions?" from an unstructured question into the sharper question "why does the admissibility operator have a four-dimensional kernel at the physical vacuum?" — a question about $\mathscr F$, which is where such a question belongs.

---

## 5. Mechanism II: Slaving and Auxiliary Origin

### 5.1 The exact statement

**Theorem B.** *Assume (H3), (H4), (H6). Let $S_\Phi[\eta,\xi]$ be first order in time derivatives, with $\delta S_\Phi/\delta\xi=0$ uniquely solvable as $\xi=\xi_*[\eta]$ on the domain guaranteed by (H3). Then:*

1. *The solution sets of $S_\Phi$ and $S_{\rm red}$ are in bijection under $\eta\mapsto(\eta,\xi_*[\eta])$.*
2. *$\delta S_{\rm red}/\delta\eta=(\delta S_\Phi/\delta\eta)|_{\xi=\xi_*}$ (Lemma 3.1).*
3. *The physical phase space of the exact reduced theory is symplectomorphic to that of the parent, with the same dimension. No additional degrees of freedom appear.*
4. *At Level I the slaving is algebraic and $S_{\rm red}$ is first order; Ostrogradsky's construction is inapplicable.*

*Proof.* (1) and (2) are Lemma 3.1 and uniqueness in (H3). For (3): the parent's Legendre map has image a constraint surface $\mathcal S$; slaving is precisely the statement that the $\xi$-block of the Legendre map is a diffeomorphism, so $\xi$ and its momentum are eliminated by a second-class pair. Dirac reduction on a second-class pair is a symplectomorphism onto the reduced surface, preserving dimension count. (4) is immediate: with $\xi_*$ algebraic in $\eta$, no derivatives of $\eta$ beyond first order are generated. $\square$

### 5.2 The truncation caveat — stated honestly

At Level II the slaving operator contains derivatives. Schematically, with $\mathscr L_{\xi\xi}=M^2-\Box$ and $M\ge\Lambda_{\rm stiff}$,
$$
\xi_*=\left(M^2-\Box\right)^{-1}J[\eta]
=\frac{J}{M^2}+\frac{\Box J}{M^4}+\frac{\Box^2J}{M^6}+\cdots .
\tag{5.1}
$$
The exact reduced action is **nonlocal**. Its derivative expansion at any finite order *does* generate higher-derivative operators, and truncating at order $\Box^2$ *does* introduce a spurious pole at $p^2\sim M^2$.

We must therefore be precise:

> Theorem B guarantees absence of extra modes in the **exact** reduced theory. It does **not** guarantee that a finite-order truncation is ghost-free. Truncation ghosts sit at or above $\Lambda_{\rm stiff}$ and are excluded from the admissible spectrum by (H4), but they are artifacts of truncation, not of the theory.

This is the standard effective-field-theory situation [17], and it would be a weak evasion if it were all UPT had. It is not. The *geometric* sector — the one that matters for emergent gravity — is degenerate **to all derivative orders**, by Theorem D. That is the strong result, and it is what distinguishes UPT from generic EFT postponement.

---

## 6. Where Second Derivatives Can Live

Before analyzing $\mathcal R_\Phi$, we eliminate the other sectors of (1.1). Three lemmas, each elementary but collectively decisive.

### 6.1 The connection sector

**Lemma 6.1 (Maurer–Cartan flatness).** *If $\Phi(x)\in G$ and $A_\mu=\mathcal A_\mu[\Phi]=\Phi^{-1}\partial_\mu\Phi$, then*
$$
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu+[A_\mu,A_\nu]\equiv0 .
$$
*The phase-connection sector contributes no second derivatives, and $\operatorname{Tr}(\Omega_\mu\Omega^\mu)$ is first order.*

*Proof.* Direct computation: $\partial_\mu(\Phi^{-1}\partial_\nu\Phi)=-\Phi^{-1}\partial_\mu\Phi\,\Phi^{-1}\partial_\nu\Phi+\Phi^{-1}\partial_\mu\partial_\nu\Phi$. Antisymmetrizing cancels the second-derivative term and yields $-[A_\mu,A_\nu]$, cancelling the commutator. $\square$

A pure-gauge connection is flat and dynamically empty. Nontrivial curvature requires the composite (CCWZ) construction [18].

**Lemma 6.2 (CCWZ curvature).** *Let $G/H$ be reductive, $\mathfrak g=\mathfrak h\oplus\mathfrak m$, $\operatorname{Ad}(H)\mathfrak m\subset\mathfrak m$. Decompose $\Omega=\Phi^{-1}d\Phi=A+e$ with $A\in\mathfrak h$, $e\in\mathfrak m$. Then the Maurer–Cartan identity $d\Omega+\Omega\wedge\Omega=0$ gives*
$$
F_A=dA+A\wedge A=-\tfrac12[e,e]_{\mathfrak h}.
\tag{6.1}
$$
*Hence $F_A$ is quadratic in **first** derivatives of $\Phi$, and $\operatorname{Tr}F_A^2$ is quartic in first derivatives. The connection sector contains no second derivatives of $\Phi$.*

*Proof.* Project $d\Omega+\Omega\wedge\Omega=0$ onto $\mathfrak h$: $dA+A\wedge A+\tfrac12[e,e]_{\mathfrak h}=0$, using $[\mathfrak h,\mathfrak m]\subset\mathfrak m$ so that the cross terms have no $\mathfrak h$ component. Since $e=e_\mu dx^\mu$ with $e_\mu$ linear in $\partial_\mu\Phi$, the result follows. $\square$

Lemmas 6.1–6.2 are stronger than they look. They say that the **entire gauge sector of UPT is Ostrogradsky-trivial**, at any order in the coupling, for any $G$ and $H$. Whatever difficulties UPT faces in reproducing $SU(3)\times SU(2)\times U(1)$, higher-derivative instability is not among them.

### 6.2 The topological sector

**Lemma 6.3.** *Let $\omega$ be a closed $d$-form on $\mathcal M_\Phi$ and $S_{\rm top}=2\pi k\int_{\mathcal X}\Phi^*\omega$. Then $\Phi^*\omega$ is a polynomial in first derivatives of $\Phi$, and $S_{\rm top}$ is metric-independent and locally a total divergence. It contributes nothing to $\mathcal H$.*

*Proof.* $(\Phi^*\omega)_{i_1\cdots i_d}=\omega_{a_1\cdots a_d}(\Phi)\,\partial_{i_1}\Phi^{a_1}\cdots\partial_{i_d}\Phi^{a_d}$. Only first derivatives appear. Closedness plus $d=\dim\mathcal X$ makes the variation a boundary term. $\square$

### 6.3 The remaining sectors

The sigma-model kinetic term $\tfrac12G_{ab}(\Phi)\partial_\mu\Phi^a\partial^\mu\Phi^b$ is first order; the potential $V(\Phi)$ is zeroth order. We conclude:

**Proposition 6.4.** *Under (H5), the unique source of second derivatives in $S_\Phi$ is the geometric response $\mathcal R_\Phi=\mathcal R[g^\Phi]$.*

The Ostrogradsky question for UPT is therefore *entirely* a question about the curvature of the phase metric. Sections 7 and 8 answer it.

---

## 7. Hessian Geometry of the Phase Metric

### 7.1 The metric is a dual Hessian metric

**Lemma 7.1 (Legendre duality).** *Let $\mathcal W$ have invertible Hessian $S_{ab}$ and let $\mathcal W^*(u)=u_a\eta^a-\mathcal W(\eta)$ be its local Legendre transform, with $u_a=\partial_a\mathcal W$. Then*
$$
\frac{\partial\mathcal W^*}{\partial u_a}=\eta^a,
\qquad
h_{ab}:=\frac{\partial^2\mathcal W^*}{\partial u_a\partial u_b}=(S^{-1})^{ab}=\chi^{ab}.
\tag{7.1}
$$

*Proof.* Differentiate $\mathcal W^*$ at fixed $u$: $\partial\mathcal W^*/\partial u_a=\eta^a+u_b\,\partial\eta^b/\partial u_a-\partial_b\mathcal W\,\partial\eta^b/\partial u_a=\eta^a$. Differentiate again and use $\partial u_b/\partial\eta^a=S_{ba}$. $\square$

Combining with Definition 4.1:

$$
\boxed{\ g^\Phi=u^*h,\qquad h=\operatorname{Hess}\mathcal W^*\ .}
\tag{7.2}
$$

**The emergent metric is the pullback, along the conjugate order-parameter map $u:\Lambda\to\mathbb R^k$, of a Hessian metric.** This is not an analogy. It is the literal content of UPT's equation $g^\Phi=T\chi T$, once the index ambiguity is resolved.

Hessian geometry is a well-developed subject [19,20]; the metric $h=\operatorname{Hess}\mathcal W^*$ is the Ruppeiner–Weinhold structure of thermodynamic fluctuation theory [21,22] and the Fisher–Rao structure of information geometry. UPT's phase metric is thus a *thermodynamic* metric on the space of controls. That identification carries consequences, which we now derive.

### 7.2 Totally symmetric connection

**Lemma 7.2.** *For $h_{ab}=\partial_a\partial_b\mathcal W^*$, the lowered Christoffel symbols are*
$$
\Gamma_{abc}=\tfrac12\,\Theta_{abc},
\qquad
\Theta_{abc}:=\partial_a\partial_b\partial_c\mathcal W^* ,
\tag{7.3}
$$
*totally symmetric in all three indices.*

*Proof.* $\Gamma_{abc}=\tfrac12(\partial_bh_{ac}+\partial_ch_{ab}-\partial_ah_{bc})=\tfrac12(\Theta_{abc}+\Theta_{acb}-\Theta_{bca})=\tfrac12\Theta_{abc}$. $\square$

$\Theta$ is the Amari–Chentsov cubic tensor. In UPT language it is the **cubic phase self-coupling**: the third derivative of the dual reduced potential.

### 7.3 Fourth derivatives cancel

**Theorem C.** *Let $h=\operatorname{Hess}\mathcal W^*$ with $v_a:=h^{bc}\Theta_{abc}=\partial_a\log\det h$. Then, with the convention $R^\rho{}_{\sigma\mu\nu}=\partial_\mu\Gamma^\rho_{\nu\sigma}-\partial_\nu\Gamma^\rho_{\mu\sigma}+\Gamma^\rho_{\mu\lambda}\Gamma^\lambda_{\nu\sigma}-\Gamma^\rho_{\nu\lambda}\Gamma^\lambda_{\mu\sigma}$ and $R_{\sigma\nu}=R^\mu{}_{\sigma\mu\nu}$:*
$$
R_{ab}=\tfrac14\left(\Theta_a{}^{cd}\,\Theta_{bcd}-v^c\,\Theta_{cab}\right),
\tag{7.4}
$$
$$
\boxed{\ R=\tfrac14\left(\|\Theta\|^2-|v|^2\right),\qquad
\|\Theta\|^2=\Theta^{abc}\Theta_{abc},\quad |v|^2=h^{ab}v_av_b .}
\tag{7.5}
$$
*In particular the Riemann tensor contains **no fourth derivatives** of $\mathcal W^*$: it is quadratic in third derivatives.*

*Proof.* Write $\Gamma^c_{ab}=\tfrac12h^{cd}\Theta_{dab}$. Then
$$
\partial_c\Gamma^c_{ab}=\tfrac12(\partial_ch^{cd})\Theta_{dab}+\tfrac12h^{cd}\partial_c\Theta_{dab},
\qquad
\partial_a\Gamma^c_{cb}=\tfrac12(\partial_ah^{cd})\Theta_{dcb}+\tfrac12h^{cd}\partial_a\Theta_{dcb}.
$$
The fourth-derivative terms are $\tfrac12h^{cd}(\partial_c\Theta_{dab}-\partial_a\Theta_{dcb})=0$ by total symmetry of $\partial\Theta$. Using $\partial_ch^{cd}=-h^{ce}h^{df}\Theta_{efc}$ and $h^{ce}\Theta_{efc}=v_f$:
$$
\partial_c\Gamma^c_{ab}=-\tfrac12 v^d\Theta_{dab},
\qquad
\partial_a\Gamma^c_{cb}=-\tfrac12\Theta_a{}^{cd}\Theta_{bcd}.
$$
The quadratic terms are
$$
\Gamma^c_{cd}\Gamma^d_{ab}=\tfrac14 v^d\Theta_{dab},
\qquad
\Gamma^c_{ad}\Gamma^d_{cb}=\tfrac14\Theta_a{}^{cd}\Theta_{bcd}.
$$
Summing with the signs of the convention gives (7.4); tracing gives (7.5). $\square$

**Verification.** Take $k=2$, $\mathcal W^*=\tfrac12(u_1^2+u_2^2)+\tfrac{\epsilon}{2}u_1^2u_2$. Then $h_{11}=1+\epsilon u_2$, $h_{12}=\epsilon u_1$, $h_{22}=1$; the only nonzero cubic component is $\Theta_{112}=\epsilon$ and permutations. At the origin $h=\delta$, $v=(0,\epsilon)$, so $|v|^2=\epsilon^2$, $\|\Theta\|^2=3\epsilon^2$, and (7.5) gives $R=\epsilon^2/2$. Direct evaluation of $\partial\Gamma-\partial\Gamma+\Gamma\Gamma-\Gamma\Gamma$ at the origin gives $R_{11}=R_{22}=\epsilon^2/4$, hence $R=\epsilon^2/2$. ✓ (Appendix B.)

### 7.4 Physical reading

Equation (7.5) is a derived, quantitative statement:

> **Emergent curvature is the square of the phase self-interaction.**

If $\mathcal W^*$ is quadratic — a free phase potential — then $\Theta=0$ and $g^\Phi$ is flat. Curvature is not an independent primitive; it is the *nonlinearity* of the order-parameter sector, measured by the Amari–Chentsov tensor, minus a volume-gradient term. This is a sharper statement than the qualitative "$\Phi\to g_{\mu\nu}$" of [1].

The second term also has a clean meaning. Since $v_a=\partial_a\log\det h$ and $\det h$ is the density of distinguishable phase states, $|v|^2$ measures the *gradient of phase-state volume*. Curvature is the excess of interaction strength over volume inhomogeneity.

### 7.5 A rigidity theorem

**Theorem 7.3 (Flatness rigidity).** *Suppose $\mathcal M_\Phi\cong\mathbb R^k$, $\mathcal W^*$ is entire and strictly convex, and $\det\operatorname{Hess}\mathcal W^*=\text{const}$ (the real Monge–Ampère condition, equivalently $v=0$). Then $\mathcal W^*$ is a quadratic polynomial and $g^\Phi$ is flat.*

*Proof.* By the Jörgens–Calabi–Pogorelov theorem [23–25], every entire convex solution of $\det\operatorname{Hess}W=c>0$ on $\mathbb R^k$ is quadratic. Then $\Theta=0$ and $R=0$ by (7.5); vanishing of the full Riemann tensor follows from Lemma 7.2 since $\Gamma\equiv0$ in affine coordinates. $\square$

**Corollary 7.4.** *Nontrivial emergent curvature in UPT requires at least one of: (i) non-convexity of $\mathcal W^*$; (ii) topologically nontrivial order-parameter domain; (iii) failure of the Monge–Ampère condition.*

Since Lorentzian signature *requires* non-convexity (Theorem E below), option (i) is automatically realized in the physical sector. The rigidity theorem is therefore not an obstruction but a sharp structural statement: **Lorentzian emergent geometry lives on the non-convex stratum of the phase potential.** This is a satisfying coherence between two independent requirements.

---

## 8. Mechanism III: The Gauss–Horndeski Theorem

### 8.1 The immersion

By (7.2), $u:\Lambda\to(\mathbb R^k,h)$ is an immersion with induced metric $g^\Phi=u^*h$. Assume the normal bundle $\mathcal N$ is nondegenerate (the null-stratum caveat is treated in §12.3). Let
$$
\mathrm{II}_{ij}:=\nabla^h_i\partial_ju-\nabla^{g}_i\partial_ju
=\partial_i\partial_ju^a+\Gamma^{h\,a}_{bc}\partial_iu^b\partial_ju^c-\Gamma^{g\,l}_{ij}\partial_lu^a
\tag{8.1}
$$
be the second fundamental form, $\mathcal N$-valued. Note:

$$
\mathrm{II}_{ij}\ \text{is affine in}\ \partial^2u,\ \text{with coefficients depending on}\ (u,\partial u).
\tag{8.2}
$$

### 8.2 The Gauss equation

$$
R^\Lambda_{ijkl}
=R^h_{abcd}\,\partial_iu^a\partial_ju^b\partial_ku^c\partial_lu^d
+\big\langle\mathrm{II}_{ik},\mathrm{II}_{jl}\big\rangle
-\big\langle\mathrm{II}_{il},\mathrm{II}_{jk}\big\rangle ,
\tag{8.3}
$$
whence, tracing,
$$
R^\Lambda=\mathcal R_{\rm amb}+\|\operatorname{tr}_g\mathrm{II}\|^2-\|\mathrm{II}\|_g^2 ,
\tag{8.4}
$$
with $\mathcal R_{\rm amb}$ the ambient curvature contracted on the tangent frame. By Theorem C, $\mathcal R_{\rm amb}$ is **algebraic in $\partial u$** — it depends on $\partial^2u$ not at all, being $\tfrac14(\|\Theta\|^2-|v|^2)$ evaluated at $u(\lambda)$.

### 8.3 The cancellation

**Theorem D.** *Under (H1)–(H6), the emergent Einstein–Hilbert density is affine in accelerations:*
$$
\boxed{\ \frac{\partial^2}{\partial\ddot u_a\,\partial\ddot u_b}\left(\sqrt{-g^\Phi}\,R^\Phi\right)\equiv0\ .}
\tag{8.5}
$$
*Consequently $\hat{\mathcal H}^{ab}=0$ and, by Theorem A, $\mathcal H^{AB}\equiv0$.*

*Proof.* Since $g^\Phi=g^\Phi(u,\partial u)$ by (4.3), $\sqrt{-g^\Phi}$ contains no second derivatives. All second-derivative dependence of $R^\Phi$ resides in $\|\operatorname{tr}\mathrm{II}\|^2-\|\mathrm{II}\|^2$, which by (8.2) is quadratic in $\partial^2u$. Work at a point in Gaussian normal coordinates for $g^\Phi$ with $g_{ij}=\operatorname{diag}(-1,1,\ldots,1)$, $\lambda^0$ timelike, and write $A_{ij}=\mathrm{II}_{ij}$. Then
$$
\|\operatorname{tr}A\|^2=\big\langle A_{00},A_{00}\big\rangle-2\sum_m\big\langle A_{00},A_{mm}\big\rangle+\sum_{m,n}\big\langle A_{mm},A_{nn}\big\rangle,
$$
$$
\|A\|^2=g^{ik}g^{jl}\langle A_{ij},A_{kl}\rangle
=\big\langle A_{00},A_{00}\big\rangle+(\text{terms with at most one }A_{00}).
$$
The coefficient of $\langle A_{00},A_{00}\rangle$ is $(g^{00})^2=+1$ in both expressions. **They cancel identically.** Since $A_{00}=\ddot u_\perp+(\text{lower order})$, no $\ddot u^2$ survives. The remaining terms are at most linear in $\ddot u$. $\square$

Note the mechanism: the cancellation is *not* a property of a particular potential or a tuned coupling. It is the algebraic identity $(\operatorname{tr}A)^2-|A|^2$, i.e. the second elementary symmetric polynomial of the shape operator. It holds for every immersion, every signature, every $\mathcal W^*$. This is precisely the sense in which UPT's degeneracy is structural.

### 8.4 Order reduction, constructively

Theorem D establishes degeneracy. To exclude ghosts definitively we exhibit a first-order form.

**Theorem D′.** *Let $g^\Phi$ be Lorentzian with spacelike leaves in a foliation $\lambda^0=t$. Then, modulo a total divergence,*
$$
\sqrt{-g^\Phi}\,R^\Phi
=N\sqrt{\mathfrak h}\left(K_{ij}K^{ij}-K^2+{}^{(3)}R[\mathfrak h]\right)+\partial_\mu(\cdots),
\tag{8.6}
$$
*and the right-hand side is **first order in time derivatives of $\Phi$**. Hence $n=1$ and Ostrogradsky's construction cannot be initiated.*

*Proof.* Equation (8.6) is the ADM identity [26]. By (4.3) with spatial indices, $\mathfrak h_{ij}=\partial_iu_a\chi^{ab}\partial_ju_b$ depends on $\Phi$ and *spatial* derivatives $\partial_k\Phi$ only — never on $\dot\Phi$. Therefore $K_{ij}=\tfrac{1}{2N}(\dot{\mathfrak h}_{ij}-D_iN_j-D_jN_i)$ is first order in time. The intrinsic curvature ${}^{(3)}R[\mathfrak h]$ contains spatial derivatives up to third order in $\Phi$ but zero time derivatives. Lapse and shift, built from $g_{0\mu}$, contain $\dot\Phi$ but no higher time derivatives. $\square$

Theorem D′ is the decisive statement. Ostrogradsky's theorem requires $n\ge2$; UPT's emergent gravitational sector has $n=1$ after a field-theoretic Legendre rearrangement. The theorem is not evaded; its domain is empty.

**Caveat, stated plainly.** Because lapse and shift are *composite* — functions of $(\Phi,\partial\Phi)$ rather than independent multipliers — the Hamiltonian constraint is not automatically first class. This can leave an additional scalar mode of *healthy derivative order*, whose gradient stability and strong-coupling scale must be checked separately. That is a genuine open problem (§15, O3), but it is **not** an Ostrogradsky problem, and conflating the two would be an error.

### 8.5 Identification with Horndeski

Consider the single-scalar reduction in which the immersion is locally a graph, $\mathrm{II}_{\mu\nu}\propto\nabla_\mu\nabla_\nu\phi$. Then (8.4) yields the combination
$$
(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)(\nabla^\mu\nabla^\nu\phi).
\tag{8.7}
$$
This is *exactly* the nonminimal structure of Horndeski's fourth Lagrangian [8,9,13]:
$$
\mathcal L_4=G_4(\phi,X)\,R+G_{4,X}\left[(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)^2\right].
\tag{8.8}
$$

**Explicit flat-space check.** With signature $(-,+,+,+)$,
$$
(\Box\phi)^2=\ddot\phi^2-2\ddot\phi\nabla^2\phi+(\nabla^2\phi)^2,
$$
$$
(\nabla_\mu\nabla_\nu\phi)^2=\ddot\phi^2-2\sum_i(\partial_t\partial_i\phi)^2+\sum_{i,j}(\partial_i\partial_j\phi)^2 .
$$
The $\ddot\phi^2$ terms cancel, leaving a Lagrangian *linear* in $\ddot\phi$ with coefficient $-2\nabla^2\phi$ independent of $\dot\phi$. Integrating by parts twice,
$$
(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)^2\ \simeq\ (\nabla^2\phi)^2-\sum_{i,j}(\partial_i\partial_j\phi)^2 ,
\tag{8.9}
$$
manifestly first order in time. ✓ (Appendix C.)

We record the conceptual consequence:

> **Horndeski's "miraculous" ghost-free combination is the Gauss equation of the order-parameter immersion.**

In the Horndeski programme, (8.7) is discovered by demanding second-order field equations — a reverse-engineered condition. In UPT it is *forced*: it is the extrinsic-curvature term of Gauss's *Theorema Egregium* for the embedding of the control manifold into phase space. What is a constraint on couplings in one framework is a geometric identity in the other. This is, in our view, the strongest evidence that the phase-response construction is the right organizing principle for degenerate higher-order dynamics.

---

## 9. Signature Transmutation: The Negative Direction Becomes Time

### 9.1 Inertia

**Theorem E.** *Let $T$ have full rank $d$ and $V:=\operatorname{im}(T^{\mathsf T})\subset\mathbb R^k$. Then*
$$
\operatorname{sig}(g^\Phi)=\operatorname{sig}\!\left(\chi|_V\right),
\qquad
\operatorname{sig}(\chi)=\operatorname{sig}(S).
\tag{9.1}
$$
*In particular for $d=k$:*
$$
\boxed{\ \operatorname{sig}(g^\Phi)=\operatorname{sig}\!\left(\operatorname{Hess}\mathcal W\right).}
\tag{9.2}
$$
*Lorentzian signature $(-,+,+,+)$ therefore holds iff the reduced phase potential has Morse index one (up to overall sign) at the vacuum.*

*Proof.* $g^\Phi=T\chi T^{\mathsf T}$ is the restriction of $\chi$ to $V$ in the frame $T$; congruence preserves inertia (Sylvester). $\chi=S^{-1}$ and a symmetric matrix and its inverse have identical inertia. $\square$

**Corollary E.1 (Dimension–Morse bound).** *A $(1,3)$ emergent spacetime requires*
$$
k\ge4,\qquad \operatorname{ind}_-(S)\ge1,\qquad \operatorname{ind}_+(S)\ge3 .
$$
*If $k=4$ exactly, then $\operatorname{sig}(S)=(1,3)$ or $(3,1)$.*

*Proof.* Cauchy interlacing for restriction of a symmetric form to a subspace, combined with (4.6) and (9.1). $\square$

This addresses Q3 and Q4 of [1] jointly and quantitatively: **four-dimensional Lorentzian spacetime requires a four-dimensional critical kernel with Morse index one.** We do not claim to derive either number. We claim that the framework converts two vague questions into one sharp spectral question about $\mathscr L_\Phi$ and $\operatorname{Hess}\mathcal W$.

### 9.2 Why this is not a ghost

Here is the conceptual heart of the paper, and it must be stated carefully because it is easy to get wrong.

A ghost is a negative eigenvalue of the **kinetic matrix on field space**. A timelike direction is a negative eigenvalue of the **metric on spacetime**. These are different bilinear forms on different spaces.

In UPT they are:
- Field-space kinetic metric: $G_{ab}(\Phi)$ in $\tfrac12G_{ab}\partial_\mu\Phi^a\partial^\mu\Phi^b$. Ghost-freedom requires $G\succ0$.
- Emergent spacetime metric: $g^\Phi_{ij}=T\chi T^{\mathsf T}$ with $\chi=(\operatorname{Hess}\mathcal W)^{-1}$. Lorentzian signature requires $\operatorname{ind}_-(\operatorname{Hess}\mathcal W)=1$.

**Proposition 9.1 (Compatibility).** *The conditions $G\succ0$ and $\operatorname{ind}_-(\operatorname{Hess}\mathcal W)=1$ are independent and simultaneously satisfiable.*

*Proof.* $G$ is the coefficient of the kinetic term; $\operatorname{Hess}\mathcal W$ is the Hessian of the reduced potential. They are independent data of the Lagrangian. Explicitly, $G_{ab}=\delta_{ab}$ and $\mathcal W=-\tfrac12(\eta^0)^2+\tfrac12\sum_{i}(\eta^i)^2+\cdots$ realizes both. $\square$

The negative direction of the phase potential — the direction an incautious reading would label "the unstable mode" — is not a negative-energy excitation. It is the direction along which the emergent metric acquires its timelike signature.

$$
\boxed{\ \text{The instability direction is not eliminated. It is geometrized: it becomes time.}\ }
$$

Contrast this with Ostrogradsky, where the negative direction is a *momentum* direction $P_1$ in phase space and the Hamiltonian is linear in it. There is no such momentum in UPT: Theorem D′ removed it. What remains of the "negative direction" is a signature label on the emergent metric.

We flag the epistemic status: this is a structural theorem *within the UPT construction*. It is not a claim that nature works this way. It is a claim that the construction is internally consistent on precisely the point where it was supposed to fail.

---

## 10. The Main Theorem and the Degree-of-Freedom Ledger

### 10.1 Main theorem

**Main Theorem.** *Let $\Phi$ satisfy (H1)–(H6) on the regular stratum $\mathcal C^{\rm reg}$, with nondegenerate normal bundle. Then:*

1. *The connection and topological sectors contain no second derivatives of $\Phi$ (Lemmas 6.1–6.3).*
2. *The unique second-derivative source is $\mathcal R[g^\Phi]$ (Prop. 6.4), with $g^\Phi=u^*\operatorname{Hess}\mathcal W^*$ (Lemma 7.1).*
3. *$\mathcal H^{AB}$ factors through $du$ and $\operatorname{rank}\mathcal H\le k$ (Theorem A).*
4. *$\hat{\mathcal H}^{ab}\equiv0$ by the Gauss cancellation, hence $\mathcal H^{AB}\equiv0$ (Theorem D).*
5. *Modulo a total divergence, the Lagrangian is first order in time derivatives (Theorem D′).*

*Therefore hypothesis (O1) fails identically, hypothesis (O3) fails by virtue of $N-k$ primary constraints, and Ostrogradsky's theorem has empty domain on $\mathcal C^{\rm reg}$. The UPT admissible sector propagates no Ostrogradsky ghost.*

### 10.2 Ledger

| Sector | Derivative order in $\Phi$ | $\mathcal H$ contribution | Mechanism |
|---|---|---|---|
| Potential $V(\Phi)$ | 0 | 0 | trivial |
| Sigma kinetic $G_{ab}\partial\Phi\partial\Phi$ | 1 | 0 | trivial |
| Maurer–Cartan $\operatorname{Tr}\Omega^2$ | 1 | 0 | Lemma 6.1 |
| CCWZ $\operatorname{Tr}F_A^2$ | 1 (quartic) | 0 | Lemma 6.2 |
| Topological $\Phi^*\omega$ | 1 (boundary) | 0 | Lemma 6.3 |
| Stiff slaving $\xi_*[\eta]$ | $\ge2$ (Level II) | 0 | Theorem B |
| Geometric $\sqrt{-g^\Phi}R^\Phi$ | 2 | **0** | Theorems C, D, D′ |

Every entry vanishes. The last is the nontrivial one.

### 10.3 The two loci

We restate (1.3) with the sharpened result:
$$
\mathcal C_\Phi^{\rm UPT}\subset\{\mathcal H\equiv0\}\subsetneq\Sigma_{\rm deg}=\{\det\mathcal H=0\}.
$$
UPT lies not merely in the degenerate locus but in the *maximally* degenerate locus where the Lagrangian is affine in accelerations. Its own criticality condition $\Delta_\Phi=0$ is an independent and further degeneration, analysed in §12.

---

## 11. Worked Models

### 11.1 M1 — Quadratic potential: flat emergence

$k=4$, $\mathcal W=\tfrac12\Sigma_{ab}\eta^a\eta^b$ with $\Sigma=\operatorname{diag}(-1,1,1,1)$. Then $S=\Sigma$, $\chi=\Sigma^{-1}=\Sigma$, $h$ is the Minkowski metric in conjugate coordinates, $\Theta=0$. For $u$ a local diffeomorphism, $g^\Phi=u^*\eta$ is flat: $R^\Phi_{ijkl}\equiv0$.

**Reading.** A free phase potential generates no curvature. Emergent gravity is entirely an interaction effect. Note also $\operatorname{sig}(g^\Phi)=(-,+,+,+)$ ✓, illustrating Theorem E with $\operatorname{ind}_-(\mathcal W)=1$.

### 11.2 M2 — Cubic potential: curvature from self-coupling

$k=4$, $\mathcal W^*(u)=\tfrac12\eta^{ab}u_au_b+\tfrac16\Theta^{abc}u_au_bu_c$ with constant totally symmetric $\Theta$. At $u=0$, $h=\eta$, $v_a=\eta^{bc}\Theta_{abc}$, and (7.5) gives
$$
R^\Phi\big|_{u=0}=\tfrac14\left(\Theta^{abc}\Theta_{abc}-\eta^{ab}v_av_b\right).
\tag{11.1}
$$
If $\Theta$ is trace-free ($v=0$), $R^\Phi=\tfrac14\|\Theta\|^2$. With $\Theta_{001}=\epsilon$ (and permutations) and all else zero: $\|\Theta\|^2=3\epsilon^2$, $v_1=-\epsilon$, $|v|^2=\epsilon^2$, giving $R^\Phi=\epsilon^2/2$ — a de Sitter-like curvature generated purely by cubic phase self-interaction.

**Dimensional caveat.** For $d=2$ the Einstein–Hilbert density is topological (Gauss–Bonnet), so (11.1) is a curvature statement, not a dynamics statement. Dynamical content requires $d\ge3$; the physically relevant case is $d=k=4$.

**Quantitative content.** Writing the emergent gravitational coupling as $M_{\rm Pl}^2\,\sqrt{-g}R$, equation (11.1) ties the vacuum curvature scale to the cubic phase coupling: $\Lambda_{\rm eff}\sim\epsilon^2/M_{\rm Pl}^2$ in appropriate units. This is a *relation*, not a prediction of a number, but it is the kind of relation the framework was supposed to produce.

### 11.3 M3 — Explicit degeneracy with constraints

Take the mechanical shadow of the Gauss structure, $k=1$:
$$
L=\tfrac12\dot q^2+\tfrac{c}{2}\left(\ddot\phi+\dot q\right)^2-U(\phi,q).
\tag{11.2}
$$
The acceleration Hessian in $(\phi,q)$ is $\operatorname{diag}(c,0)$: rank 1, degenerate. Naive counting suggests one Ostrogradsky mode. But define $\psi:=\dot\phi$. Then (11.2) is equivalent to the first-order system
$$
\tilde L=\tfrac12\psi^2+\tfrac{c}{2}(\dot\psi+\dot q)^2-U(\phi,q),
\qquad \text{constraint }\ \dot\phi-\psi=0 ,
$$
with Lagrange multiplier $\lambda$. The multiplier's momentum is a primary constraint; its consistency condition fixes $\lambda$; the pair is second class and removes exactly the would-be ghost. Physical phase space: $(\phi,\psi,q)$ and conjugates, dimension 6, minus 2 second-class constraints $=4$, i.e. two healthy degrees of freedom.

This is Mechanism II in fully explicit form: **the higher-derivative appearance is an artifact of eliminating a field that was auxiliary all along.** It is the mechanical shadow of $\xi=\xi_*[\eta]$.

### 11.4 M4 — Sharpness: a genuine ghost

We now violate (H5) and exhibit the failure. Add an *independent* soft-sector higher-derivative operator:
$$
S=\int d^dx\left[\tfrac12G_{ab}\partial\Phi^a\partial\Phi^b-V(\Phi)+\sqrt{-g^\Phi}R^\Phi+\tfrac{\alpha}{2}\left(\Box\eta^1\right)^2\right].
\tag{11.3}
$$
Now
$$
\hat{\mathcal H}^{11}=\alpha\neq0 ,
$$
and Theorem D no longer applies: the second-derivative dependence is *not* mediated by $\mathcal R[g^\Phi]$. The theory propagates an additional scalar of mass$^2\sim1/\alpha$ with wrong-sign kinetic term. Its mechanical restriction is the Pais–Uhlenbeck oscillator
$$
L_{\rm PU}=\tfrac12\ddot q^2-\tfrac12(\omega_1^2+\omega_2^2)\dot q^2+\tfrac12\omega_1^2\omega_2^2q^2 ,
$$
with $Q_1=q$, $Q_2=\dot q$, $P_2=\ddot q$, $P_1=-(\omega_1^2+\omega_2^2)\dot q-\dddot q$, and
$$
H=P_1Q_2+\tfrac12P_2^2+\tfrac12(\omega_1^2+\omega_2^2)Q_2^2-\tfrac12\omega_1^2\omega_2^2Q_1^2 ,
\tag{11.4}
$$
manifestly linear in $P_1$, unbounded, and diagonalizable into two oscillators of opposite-sign energy. Interactions trigger the runaway of Prop. 2.2.

**Conclusion.** The mediation axiom (H5) is *necessary*, not decorative. UPT's evasion is a property of a specific structural class, and stepping outside that class restores the instability immediately. The counterexample is sharp.

---

## 12. Critical Strata and the Stability of the Evasion

### 12.1 The apparent tension

UPT's most interesting physics lives on $\Sigma_\Phi=\{\Delta_\Phi=0\}$, where $\ker\mathscr L_\Phi\neq0$. But there $S_{ab}$ acquires a kernel, $\chi=S^{-1}$ diverges, and the construction (7.2) appears to break down. Is the Ostrogradsky evasion an artifact of the *uninteresting* regular stratum?

### 12.2 Resolution by rank absorption

**Proposition 12.1.** *Let $\Phi$ approach $\Sigma_\Phi$ so that $\dim\ker S$ increases by $r$. Replace $\chi$ by its Moore–Penrose pseudo-inverse $\chi^+$ on $\operatorname{ran}S$, and enlarge the order-parameter set by the $r$ new soft directions, $k\to k'=k+r$. Then the Lyapunov–Schmidt construction applies verbatim with $k'$, Theorem A holds with rank bound $k'$, and Theorems C, D, D′ are unchanged since they never used invertibility of $S$ on the full space — only the immersion structure of $u$.*

*Proof.* Theorem D's proof used only (i) $g^\Phi=g^\Phi(u,\partial u)$ and (ii) the Gauss identity. Neither references $\det S$. The pseudo-inverse is smooth on the constant-rank stratum, so (i) persists. $\square$

**Corollary 12.2.** *The Ostrogradsky evasion is stable across critical strata, at the cost of a jump $k\to k'$ in the soft-sector dimension — and hence, by Corollary A.1, a possible jump in the maximum emergent dimension.*

This is a nontrivial coherence with Part XII of [1], which explicitly contemplates $d_{\rm eff}$ changing at cosmological phase transitions. The dimension bound (4.6) supplies a *mechanism* for that contemplated behaviour: dimensional change is kernel growth.

### 12.3 Where the argument genuinely fails

We list the boundaries honestly.

**(B1) Non-Fredholm operators.** If $\mathscr L_\Phi$ has essential spectrum reaching zero — as on non-compact $\mathcal X$ without decay conditions — then $k=\infty$, (H1) fails, and Theorem A gives no bound. The evasion is unproved, not disproved.

**(B2) Rank-changing strata.** Where $k$ is not locally constant, (H2) fails; the projector $\Pi$ is discontinuous and the mediated form of $\mathcal L$ is not smooth. A stratified analysis is required.

**(B3) Null immersions.** If $g^\Phi|_{\text{some leaf}}$ degenerates, the normal bundle is degenerate and the Gauss equation (8.3) is invalid. This is precisely the signature-change locus. Since Theorem E ties signature to Morse index, signature change is a Morse-index jump — a real phase transition, and the argument must be redone on each side.

**(B4) Composite lapse.** As noted in §8.4, first-class structure is not automatic. Extra healthy-order modes may appear.

None of these is an Ostrogradsky ghost. All are genuine open problems.

---

## 13. The Quantum Sector

### 13.1 What the classical result buys

Because the classical Hamiltonian is not linear in any momentum after reduction (Theorem D′), quantization proceeds on the reduced phase space with a **positive-definite inner product**. No negative-norm states are forced, no indefinite metric is required, and no $\mathcal{PT}$-symmetric reinterpretation is needed.

This is worth contrasting sharply with the Bender–Mannheim treatment of the Pais–Uhlenbeck oscillator [14,15], in which the Hamiltonian is non-Hermitian but $\mathcal{PT}$-symmetric, the spectrum is real, and unitarity is restored by a dynamically determined $\mathcal{CPT}$ inner product. That programme evades via exit **E4**. UPT evades via **E1 + E3**, at the classical level, which is logically prior and structurally cheaper: one does not have to reinterpret the Hilbert space because one never generated the ghost.

### 13.2 What it does not buy

Three caveats, stated without softening.

1. **Constraint anomalies.** The $N-k$ primary constraints (4.5) and their secondaries must close as an algebra after quantization. An anomaly would reintroduce modes. We have not verified closure in general; this is open problem O2.

2. **Absence of Ostrogradsky ghosts $\neq$ positive energy.** GR itself has a Hamiltonian constraint rather than a positive Hamiltonian, and the conformal-factor problem in the Euclidean sector. UPT inherits these. They are not Ostrogradsky pathologies.

3. **Born rule untouched.** Nothing here derives $P=|\psi|^2$. Required Result I of [1] remains open. The phase-measure programme of Part VII is unaffected by the present analysis.

---

## 14. Status Ledger and Falsifiable Consequences

### 14.1 What is proved, what is conditional, what is open

**Proved outright (given the stated hypotheses):**
- Lemmas 6.1–6.3: connection and topological sectors are second-derivative-free.
- Lemma 7.1: $g^\Phi$ is a pullback dual Hessian metric.
- Theorem C: no fourth derivatives; $R=\tfrac14(\|\Theta\|^2-|v|^2)$, verified against direct computation.
- Theorem D: Gauss cancellation; $\hat{\mathcal H}\equiv0$.
- Theorem D′: first-order ADM form.
- Theorem E: Sylvester inertia; signature–Morse correspondence.
- Theorem 7.3: flatness rigidity via Jörgens–Calabi–Pogorelov.
- §11.4: sharpness of (H5).

**Conditional on UPT's construction being the correct substrate:**
- Corollary A.1 ($d_{\rm eff}\le k$) and Corollary E.1 as statements about *nature*.
- The interpretation of the Morse-index-one direction as physical time.
- Equation (11.1) as a relation between observed curvature and phase couplings.

**Open:**
- Everything in §12.3 and §13.2.
- Required Results D–J of [1] without exception.

We wish to be unambiguous: **this paper establishes that UPT is not killed by Ostrogradsky. It does not establish that UPT is correct.** Removing a lethal objection is a necessary condition for a research programme to continue, not evidence in its favour.

### 14.2 Falsifiable consequences

**(P1) No massive spin-2 ghost pole.** Unlike quadratic gravity $\int(R^2+ R_{\mu\nu}R^{\mu\nu})$ [5], which propagates a massive spin-2 ghost, UPT's geometric sector is affine in accelerations and propagates no such mode. Hence UPT predicts **no Stelle-type Yukawa correction** $\propto e^{-m_2r}/r$ to the Newtonian potential from a ghost pole. Torsion-balance and short-range gravity experiments constrain this directly. A confirmed spin-2 ghost pole would falsify the mediation structure.

**(P2) Horndeski-restricted deviations.** By §8.5, deviations from GR are confined to a subfamily of Horndeski determined by the immersion geometry, not the full Horndeski function space. The GW170817 tensor-speed bound $|c_T/c-1|\lesssim10^{-15}$ [27–29] then carves the allowed region sharply. The specific relations among $G_4,G_{4,X},G_5$ implied by (8.4) are computable and constitute a genuine test.

**(P3) Curvature–coupling relation.** Equation (11.1) predicts that emergent vacuum curvature is quadratic in the cubic phase coupling with a fixed tensorial contraction pattern. Any measured deviation from that pattern — in particular a curvature contribution linear in a cubic coupling — would contradict (7.5).

**(P4) Dimension–kernel correlation.** If a phase transition changes $k$, the maximum emergent dimension changes with it (Cor. 12.2). Any observation of dimensional flow at high energy (spectral dimension running) is constrained by the requirement that it track kernel growth, not vary independently.

**(P5) Flatness rigidity.** By Theorem 7.3, an entire convex Monge–Ampère phase potential is necessarily flat. Observation of curvature therefore *requires* non-convexity — which, by Theorem E, is independently required for Lorentzian signature. A construction achieving Lorentzian signature with a globally convex potential is impossible; this is an internal consistency test that any explicit UPT model must pass.

---

## 15. Open Problems

**O1 (Converse / representability).** Is every degenerate higher-order scalar-tensor theory of phase-response origin? Precisely: given a DHOST Lagrangian satisfying the degeneracy conditions of [12,13], does there exist $(\mathcal W^*,u,k)$ realizing it as $\sqrt{-g^\Phi}R^\Phi$ with $g^\Phi=u^*\operatorname{Hess}\mathcal W^*$? An affirmative answer would make UPT a *classification* of ghost-free higher-order dynamics rather than one example of it. We conjecture the answer is affirmative for the subclass with $G_5=0$ and negative for the general case.

**O2 (Constraint closure).** Complete the Dirac–Bergmann analysis of the $N-k$ primaries (4.5) with composite lapse and shift. Determine the secondary structure, classify first/second class, and check quantum closure.

**O3 (Healthy-sector stability).** The extra scalar potentially left by the composite lapse is of healthy derivative order. Compute its sound speed squared and strong-coupling scale. Gradient instability, not Ostrogradsky instability, is the live danger here.

**O4 (Kernel dimension).** Why would $\dim\ker\mathscr L_\Phi=4$ at the physical vacuum? Corollary A.1 makes this the sharp form of the dimensionality problem. It is a question about the index theory of $\mathscr F$, and it is now posed where it can be attacked.

**O5 (Null stratum).** Extend Theorem D across signature-change loci where the normal bundle degenerates. This requires a Gauss equation for degenerate immersions, which exists in the lightlike-submanifold literature but has not been applied here.

**O6 (Non-Fredholm extension).** Replace $\ker\mathscr L$ by a spectral subspace and Theorem A by a statement about the *rank of the spectral projection below a threshold*. This would extend the evasion to non-compact $\mathcal X$, which is the physically relevant case.

---

## 16. Conclusion

Ostrogradsky's theorem is correct. The inference commonly drawn from it — that a fundamental action containing $D^2\Phi$ is fatally unstable — is not, and Universal Phase Theory supplies a counterexample in which the failure of the theorem's hypothesis is *derived from the framework's own axioms* rather than imposed by tuning couplings.

The chain is:
$$
\underbrace{\mathscr L_\Phi\ \text{Fredholm}}_{\text{H1}}
\ \Rightarrow\
\underbrace{k=\dim\ker\mathscr L_\Phi<\infty}_{\text{Lyapunov–Schmidt}}
\ \Rightarrow\
\underbrace{g^\Phi=u^*\operatorname{Hess}\mathcal W^*}_{\text{response construction}}
\ \Rightarrow\
\underbrace{\Gamma_{abc}=\tfrac12\Theta_{abc}}_{\text{Hessian}}
\ \Rightarrow\
\underbrace{R^\Lambda=\mathcal R_{\rm amb}+\|\operatorname{tr}\mathrm{II}\|^2-\|\mathrm{II}\|^2}_{\text{Gauss}}
\ \Rightarrow\
\underbrace{\mathcal H\equiv0}_{\text{cancellation}} .
$$

Three results deserve emphasis beyond the evasion itself. First, the emergent-dimension bound $d_{\rm eff}\le\dim\ker\mathscr L_\Phi$ converts the dimensionality problem into a spectral problem. Second, the signature–Morse correspondence identifies the single negative direction of the phase Hessian with the timelike direction of emergent spacetime: the instability is not removed but *geometrized*. Third, the Gauss equation reproduces exactly Horndeski's $\mathcal L_4$ combination, so that a structure discovered by reverse-engineering second-order field equations is here revealed as the extrinsic curvature of the order-parameter immersion.

None of this makes UPT a physical theory. Required Results D through J of the foundational document remain entirely open, and §12.3 lists four places where the present argument does not reach. What has been established is narrower and worth stating exactly: **the objection that higher-derivative phase dynamics is necessarily unstable does not apply, and its inapplicability is a theorem rather than a hope.** The programme survives this particular obstruction. It must now be judged on the obstructions that remain.

---

## Appendix A. Ostrogradsky Construction, Details

From the variational principle with $L(q,\ldots,q^{(n)})$, integration by parts gives
$$
\delta S=\int\sum_{j=0}^{n}\left(-\frac{d}{dt}\right)^{j}\frac{\partial L}{\partial q^{(j)}}\,\delta q\,dt+\Big[\sum_{i=1}^{n}P_i\,\delta Q_i\Big],
$$
which identifies the boundary term and hence the canonical one-form $\theta=P_i\,dQ_i$. The symplectic form $\omega=d\theta=dP_i\wedge dQ_i$ is nondegenerate exactly when (O3) holds. The Hamiltonian follows from $H=\iota_{\partial_t}\theta-L$ evaluated on the Legendre image, giving (2.4). Under (O1) the map $q^{(n)}\mapsto P_n$ is invertible; under (O3) the remaining momenta are free. Linearity in $P_1,\ldots,P_{n-1}$ is then manifest and unboundedness follows.

For the Pais–Uhlenbeck case (11.4), the canonical transformation
$$
Q_\pm=\frac{\ddot q+\omega_\mp^2 q}{\sqrt{\omega_2^2-\omega_1^2}},\qquad
P_\pm=\mp\frac{\dot q\,\omega_\mp^2+\dddot q}{\sqrt{\omega_2^2-\omega_1^2}}\cdot(\cdots)
$$
diagonalizes $H$ into $\omega_2$- and $\omega_1$-oscillators with opposite energy signs; the explicit coefficients are standard [4,14] and are not needed for the argument, which uses only the linearity in $P_1$.

## Appendix B. Verification of the Hessian Curvature Formula

Take $k=2$, $\mathcal W^*=\tfrac12(x^2+y^2)+\tfrac{\epsilon}{2}x^2y$. Then
$$
h=\begin{pmatrix}1+\epsilon y&\epsilon x\\ \epsilon x&1\end{pmatrix},\qquad
\Theta_{112}=\Theta_{121}=\Theta_{211}=\epsilon,\ \text{else }0 .
$$
At the origin $h=\delta$, $v_a=h^{bc}\Theta_{abc}$ gives $v=(0,\epsilon)$.

Formula (7.4): $R_{11}=\tfrac14(\Theta_1{}^{cd}\Theta_{1cd}-v^c\Theta_{c11})=\tfrac14(2\epsilon^2-\epsilon^2)=\tfrac{\epsilon^2}{4}$; $R_{22}=\tfrac14(\epsilon^2-0)=\tfrac{\epsilon^2}{4}$. Hence $R=\epsilon^2/2$.

Direct: at the origin $\Gamma^1_{12}=\Gamma^1_{21}=\Gamma^2_{11}=\epsilon/2$, others zero; $\partial_\mu h^{\mu1}=0$, $\partial_\mu h^{\mu2}=-\epsilon$; $\partial_1v_1=-2\epsilon^2$, $\partial_2v_2=-\epsilon^2$. Then
$$
R_{11}=\underbrace{-\tfrac{\epsilon^2}{2}}_{\partial_\mu\Gamma^\mu_{11}}-\underbrace{(-\epsilon^2)}_{\partial_1\Gamma^\mu_{\mu1}}+\underbrace{\tfrac{\epsilon^2}{4}}_{\Gamma\Gamma}-\underbrace{\tfrac{\epsilon^2}{2}}_{\Gamma\Gamma}=+\tfrac{\epsilon^2}{4}\ \checkmark
$$
$$
R_{22}=0-\left(-\tfrac{\epsilon^2}{2}\right)+0-\tfrac{\epsilon^2}{4}=+\tfrac{\epsilon^2}{4}\ \checkmark
$$
Formula (7.5): $\tfrac14(3\epsilon^2-\epsilon^2)=\epsilon^2/2$ ✓.

The same test with Lorentzian $\mathcal W^*=-\tfrac12u_0^2+\tfrac12u_1^2+\tfrac\epsilon2u_0^2u_1$ gives $\|\Theta\|^2=3\epsilon^2$, $|v|^2=\epsilon^2$, $R=\epsilon^2/2$, signature $(-,+)$ ✓.

## Appendix C. The Gauss Combination in Flat Space

With $\Box=-\partial_t^2+\nabla^2$,
$$
(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)^2
=-2\ddot\phi\,\nabla^2\phi+(\nabla^2\phi)^2+2\sum_i(\partial_t\partial_i\phi)^2-\sum_{i,j}(\partial_i\partial_j\phi)^2 .
$$
The coefficient of $\ddot\phi$ is $-2\nabla^2\phi$, independent of $\dot\phi$. Hence
$$
\int-2\ddot\phi\,\nabla^2\phi\,dt=\int 2\dot\phi\,\nabla^2\dot\phi\,dt=-\int2|\nabla\dot\phi|^2\,dt=-\int2\sum_i(\partial_t\partial_i\phi)^2\,dt ,
$$
using spatial integration by parts twice. Substituting yields (8.9):
$$
(\Box\phi)^2-(\nabla_\mu\nabla_\nu\phi)^2\ \simeq\ (\nabla^2\phi)^2-\sum_{i,j}(\partial_i\partial_j\phi)^2 ,
$$
containing only spatial second derivatives and no time derivatives beyond first order. ∎

## Appendix D. Constraint Structure of the Affine Case

Write $\mathcal L=A_a(\Phi,\dot\Phi)\,\ddot u^a+B(\Phi,\dot\Phi)$. Ostrogradsky variables $(Q^A,R^A;\Pi_A,P_A)$ with $\{Q^A,P_B\}=\{R^A,\Pi_B\}=\delta$. Primary constraints:
$$
\varphi_A:=\Pi_A-A_a(Q,R)\,\partial_Au^a\approx0 ,
$$
splitting into $N-k$ conditions $\Pi_A\mathfrak n^A_{(p)}\approx0$ and $k$ conditions fixing the soft components. The Hamiltonian
$$
H=P_AR^A-A_a\,\partial_A\partial_Bu^a\,R^AR^B-B
$$
is independent of $\Pi$ on the constraint surface. Consistency $\dot\varphi_A\approx0$ generates secondaries whenever the bracket matrix
$$
\{\varphi_A,\varphi_B\}=\partial_Au^a\,\frac{\partial A_a}{\partial R^B}-\partial_Bu^a\,\frac{\partial A_a}{\partial R^A}+\cdots
$$
has corank; the general theorem of [11–13] guarantees that under regularity the resulting second-class pair removes the would-be Ostrogradsky mode. The constructive route via Theorem D′ bypasses this analysis entirely by exhibiting a first-order form, and is the argument we rely on. The residual first-class structure with composite lapse is open problem O2.

## Appendix E. Notation

| Symbol | Meaning |
|---|---|
| $\Phi^A$, $A=1..N$ | phase field components |
| $\eta^a$, $a=1..k$ | order parameters (soft) |
| $\xi$ | stiff sector |
| $u_a=\partial_a\mathcal W$ | conjugate order parameters |
| $\lambda^i$, $i=1..d$ | control / emergent-spacetime coordinates |
| $\mathcal W(\eta)$ | reduced phase potential ($\equiv\Phi_{\rm eff}$ of [1]) |
| $\mathcal W^*(u)$ | Legendre dual |
| $S_{ab}=\partial_a\partial_b\mathcal W$ | stability tensor |
| $\chi^{ab}=(S^{-1})^{ab}=h_{ab}$ | susceptibility = dual Hessian metric |
| $\Theta_{abc}=\partial_a\partial_b\partial_c\mathcal W^*$ | cubic (Amari–Chentsov) phase coupling |
| $v_a=\partial_a\log\det h$ | log-volume gradient ($=2\times$ Koszul form) |
| $\mathrm{II}_{ij}$ | second fundamental form of $u:\Lambda\hookrightarrow\mathbb R^k$ |
| $\mathcal H^{AB}$, $\hat{\mathcal H}^{ab}$ | acceleration Hessians |
| $\mathfrak b(\eta,\lambda)$ | reduced bifurcation equation |
| $\Sigma_{\rm deg}$, $\Sigma_\Phi$ | Ostrogradsky degeneracy locus; UPT critical manifold |

Signature $(-,+,+,+)$. Riemann convention as in Theorem C. Symmetrization weight one.

---

## References

[1] *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality.* Foundational Preprint, August 2026.

[2] M. Ostrogradsky, *Mémoires sur les équations différentielles relatives au problème des isopérimètres*, Mém. Ac. Imp. Sci. St. Pétersbourg **6** (1850) 385.

[3] R. P. Woodard, *The Theorem of Ostrogradsky*, Scholarpedia **10**(8) (2015) 32243; arXiv:1506.02210.

[4] A. Pais and G. E. Uhlenbeck, *On Field Theories with Non-Localized Action*, Phys. Rev. **79** (1950) 145.

[5] K. S. Stelle, *Renormalization of Higher-Derivative Quantum Gravity*, Phys. Rev. D **16** (1977) 953.

[6] D. Lovelock, *The Einstein Tensor and Its Generalizations*, J. Math. Phys. **12** (1971) 498.

[7] S. W. Hawking and T. Hertog, *Living with Ghosts*, Phys. Rev. D **65** (2002) 103515.

[8] G. W. Horndeski, *Second-Order Scalar-Tensor Field Equations in a Four-Dimensional Space*, Int. J. Theor. Phys. **10** (1974) 363.

[9] A. Nicolis, R. Rattazzi and E. Trincherini, *The Galileon as a Local Modification of Gravity*, Phys. Rev. D **79** (2009) 064036.

[10] C. Deffayet, G. Esposito-Farèse and A. Vikman, *Covariant Galileon*, Phys. Rev. D **79** (2009) 084003.

[11] H. Motohashi and T. Suyama, *Third Order Equations of Motion that can be Solved into Second Order Ones*, Phys. Rev. D **91** (2015) 085009.

[12] D. Langlois and K. Noui, *Degenerate Higher Order Scalar-Tensor Theories beyond Horndeski and Hamiltonian Analysis*, JCAP **02** (2016) 034.

[13] T. Kobayashi, *Horndeski Theory and Beyond: A Review*, PTEP **2019** (2019) 071E01; arXiv:1901.07183.

[14] C. M. Bender and P. D. Mannheim, *No-Ghost Theorem for the Fourth-Order Derivative Pais–Uhlenbeck Oscillator Model*, Phys. Rev. Lett. **100** (2008) 110402.

[15] A. Smilga, *Benign vs. Malicious Ghosts in Higher-Derivative Field Theory*, Nucl. Phys. B **704** (2005) 367.

[16] J. Z. Simon, *Higher-Derivative Lagrangians, Nonlocality, Problems, and Solutions*, Phys. Rev. D **41** (1990) 3720.

[17] C. P. Burgess, *Introduction to Effective Field Theory*, Ann. Rev. Nucl. Part. Sci. **57** (2007) 329.

[18] S. Coleman, J. Wess and B. Zumino, *Structure of Phenomenological Lagrangians I*, Phys. Rev. **177** (1969) 2239; C. G. Callan, S. Coleman, J. Wess and B. Zumino, *ibid. II*, Phys. Rev. **177** (1969) 2247.

[19] H. Shima, *The Geometry of Hessian Structures*, World Scientific, 2007.

[20] S.-i. Amari, *Information Geometry and Its Applications*, Springer, 2016.

[21] F. Weinhold, *Metric Geometry of Equilibrium Thermodynamics*, J. Chem. Phys. **63** (1975) 2479.

[22] G. Ruppeiner, *Riemannian Geometry in Thermodynamic Fluctuation Theory*, Rev. Mod. Phys. **67** (1995) 605.

[23] K. Jörgens, *Über die Lösungen der Differentialgleichung $rt-s^2=1$*, Math. Ann. **127** (1954) 130.

[24] E. Calabi, *Improper Affine Hyperspheres of Convex Type and a Generalization of a Theorem by K. Jörgens*, Michigan Math. J. **5** (1958) 105.

[25] A. V. Pogorelov, *On the Improper Convex Affine Hyperspheres*, Geom. Dedicata **1** (1972) 33.

[26] R. Arnowitt, S. Deser and C. W. Misner, *The Dynamics of General Relativity*, in *Gravitation: An Introduction to Current Research*, Wiley, 1962; reprinted Gen. Rel. Grav. **40** (2008) 1997.

[27] B. P. Abbott *et al.* (LIGO/Virgo), *Gravitational Waves and Gamma-Rays from a Binary Neutron Star Merger*, ApJL **848** (2017) L13.

[28] T. Baker *et al.*, *Strong Constraints on Cosmological Gravity from GW170817 and GRB 170817A*, Phys. Rev. Lett. **119** (2017) 251301.

[29] J. M. Ezquiaga and M. Zumalacárregui, *Dark Energy After GW170817: Dead Ends and the Road Ahead*, Phys. Rev. Lett. **119** (2017) 251304.

[30] M. Golubitsky and D. G. Schaeffer, *Singularities and Groups in Bifurcation Theory*, Vol. I, Springer, 1985.

[31] R. M. Wald, *General Relativity*, University of Chicago Press, 1984.

---

*End of preprint UPT-F/2026-04.*

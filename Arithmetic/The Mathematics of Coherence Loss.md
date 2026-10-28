# The Mathematics of Coherence Loss

## A Spectral–Correlational Theory of Quantum Channels, Conserved Structure, and Predictive Coherence Lifetimes

Research preprint · 27 October 2026

## Abstract

Quantum decoherence is conventionally characterized through phenomenological rates, master equations, environmental spectral densities, and channel-specific measures of state distinguishability. These methods are powerful, but they do not by themselves provide a universal classification of coherence loss across different quantum channels. A dephasing channel, an amplitude-damping channel, a correlated noise process, and a channel that conserves selected observables can exhibit the same decay rate for one chosen coherence while producing radically different transformations of the system's spectrum, correlations, and recoverable quantum information.

This paper develops a mathematical framework in which coherence loss is characterized by the structural action of a quantum channel, rather than by a single scalar rate. The framework separates four quantities: contraction of off-diagonal coherence, change in the spectrum of the density operator, degradation of correlations, and violation or preservation of specified conservation laws. Their joint behavior defines a channel-dependent coherence signature.

The principal candidate invariant is a spectral–correlational contraction index, constructed from the action of a quantum channel on a specified operator subspace and supplemented by a correlation-contraction bound. For repeated applications of a fixed channel, the contraction index is determined by the spectral radius of the channel restricted to the relevant coherence sector. Under explicit invariance and diagonalizability assumptions, this produces an exponential lifetime bound. In the more general non-normal case, singular-value and resolvent estimates are required because the spectral radius alone does not control finite-time decay.

A rigorous distinction is maintained between mathematical results established by the framework and the open physical hypothesis: that combining coherence contraction, spectral redistribution, and correlation loss yields predictive information beyond existing channel diagnostics. The theory does not claim a new universal law of decoherence. Instead, it identifies a precise route by which a new invariant could earn that status through provable bounds, parameter-free predictions, and experimental comparison against standard channel models.

Keywords: quantum channels; decoherence; completely positive maps; spectral contraction; quantum coherence; quantum correlations; conserved observables; channel powers; coherence lifetime; open quantum systems.

## 1. Introduction: From Decay Rates to Structural Classification

A quantum state on a finite-dimensional Hilbert space \\(\mathcal H\\) is represented by a density operator

\\[ \rho\geq 0,\qquad \operatorname{Tr}\rho=1. \\]

An open-system evolution over a fixed time interval can be represented by a completely positive, trace-preserving (CPTP) map

\\[ \mathcal E:\mathcal B(\mathcal H)\rightarrow\mathcal B(\mathcal H), \qquad \rho\mapsto\mathcal E(\rho). \\]

Complete positivity ensures that the map remains positive when tensored with the identity map on an arbitrary auxiliary system. Trace preservation ensures conservation of total probability. Neither condition implies conservation of purity, quantum coherence, entropy, entanglement, or individual observables.

For repeated applications of a stationary channel,

\\[ \rho_n=\mathcal E^n(\rho_0). \\]

The conventional question is often: At what rate does a selected observable of coherence decay?

The structural question proposed here is broader:

Which properties of the channel determine how coherence, spectral information, correlations, and conserved quantities change together under iteration?

These questions are not equivalent. Consider two channels that satisfy

\\[ C(\mathcal E_1^n(\rho_0)) \approx C(\mathcal E_2^n(\rho_0)) \\]

for a chosen coherence measure \\(C\\). The equality of those scalar trajectories does not imply that the two output states have the same eigenvalue distribution, entanglement with an ancilla, distinguishability from neighboring states, or response to subsequent operations.

A more complete classification must therefore specify both the channel and the structural feature being measured.

### 1.1 The central hypothesis

The working hypothesis is that the loss of quantum coherence in a well-defined class of systems can be bounded more sharply by a joint description of:

1. contraction of a coherence-carrying operator subspace;
2. spectral redistribution of the density operator;
3. loss or redistribution of correlations with auxiliary degrees of freedom;
4. preservation of selected observables or symmetry sectors;
5. non-normal transient dynamics and the structure of channel eigenoperators.

The hypothesis is deliberately narrower than the claim that all decoherence has one underlying invariant. Different channels can have different invariant subspaces, different fixed-point algebras, and different asymptotic states. A useful theory must preserve these distinctions rather than conceal them inside a universal decay constant.

### 1.2 What would count as a genuine advance?

A new classification is scientifically useful only if it does more than rename known quantities. The target is a theorem of the following general form:

> Given a specified channel class, an independently measurable structural index, and explicit assumptions on the initial state and conserved sectors, the index supplies a bound on the time required for a defined coherence observable to fall below a prescribed threshold.

The index must be calculable without fitting the same lifetime it is intended to predict. Otherwise, it is a descriptive statistic, not a predictive law.

## 2. Mathematical Preliminaries

### 2.1 Quantum channels and Kraus representations

Every finite-dimensional CPTP map admits a Kraus representation

\\[ \mathcal E(\rho)=\sum\_{\alpha=1}^{r} K\_\alpha\rho K\_\alpha^\dagger, \\]

with

\\[ \sum\_{\alpha=1}^{r}K\_\alpha^\dagger K\_\alpha=I. \\]

The Kraus operators are not unique. Different Kraus representations can describe the same physical channel, so a candidate coherence invariant should be defined directly from \\(\mathcal E\\), not from an arbitrary choice of its Kraus operators.

The adjoint channel is defined by

\\[ \operatorname{Tr}[A\\,\mathcal E(\rho)] = \operatorname{Tr}[\mathcal E^\dagger(A)\rho], \\]

where

\\[ \mathcal E^\dagger(A) = \sum\_\alpha K\_\alpha^\dagger A K\_\alpha. \\]

Trace preservation of \\(\mathcal E\\) is equivalent to unitality of its adjoint:

\\[ \mathcal E^\dagger(I)=I. \\]

Conversely, the Schrödinger-picture channel is unital if \\(\mathcal E(I)=I\\). This distinction matters because a unital channel and a non-unital channel can have different spectral and entropy behavior even when both are CPTP.

### 2.2 Fixed points and asymptotic states

A fixed point satisfies

\\[ \mathcal E(\rho\_\*)=\rho\_\*. \\]

The fixed-point set need not consist of a unique state. For example, a dephasing channel may preserve every density operator diagonal in a preferred basis, while an amplitude-damping channel may drive every initial state toward a single ground state.

Thus, the limiting state is channel-dependent:

\\[ \lim\_{n\to\infty}\mathcal E^n(\rho_0)=\rho\_\* \\]

only when the required convergence conditions hold. In general, peripheral eigenvalues, invariant sectors, or periodic behavior may prevent convergence to a single state.

The theory will consequently distinguish coherence contraction toward a fixed-point algebra from contraction toward a unique equilibrium state.

### 2.3 A specified coherence measure

Let \\(\\{|i\rangle\\}\_{i=1}^d\\) be a fixed reference basis. Define the dephasing projection

\\[ \Delta(\rho)=\sum_i |i\rangle\langle i| \rho|i\rangle\langle i|. \\]

The off-diagonal component of a state is

\\[ \rho\_{\mathrm{off}}=(I-\Delta)(\rho). \\]

A useful norm-based coherence functional is

\\[ C_2(\rho)=\\|(I-\Delta)(\rho)\\|\_2, \\]

where

\\[ \\|A\\|\_2=\sqrt{\operatorname{Tr}(A^\dagger A)} \\]

is the Hilbert–Schmidt norm.

For a qubit,

\\[ \rho= \begin{pmatrix} p & c\\\ c^\* & 1-p \end{pmatrix}, \qquad C_2(\rho)=\sqrt{2}|c|. \\]

This functional is not asserted to be a universal measure of quantum coherence. It is chosen because its behavior under linear maps can be analyzed directly. The \\(l_1\\)-norm coherence, relative-entropy coherence, and resource-theoretic coherence measures remain relevant alternatives, each with different contraction properties.

Measurement convention. Coherence is always relative to a specified basis or observable algebra. A basis change can convert off-diagonal matrix elements into diagonal ones, so basis-independent claims must use a different operational definition.

### 2.4 Coherence as an operator sector

Let \\(\mathcal P\\) be a linear projection on the operator space satisfying

\\[ \mathcal P^2=\mathcal P. \\]

The operator

\\[ X\_{\mathrm c}=\mathcal P(X) \\]

is the component assigned to the coherence sector. In the basis-specific example, \\(\mathcal P=I-\Delta\\).

The complementary projection \\(I-\mathcal P\\) describes the remaining operator sector. This need not be merely a population sector: for a more general symmetry decomposition, it may include several distinct invariant components.

A key structural condition is whether the channel preserves the decomposition:

\\[ \mathcal E\mathcal P=\mathcal P\mathcal E. \\]

When this relation holds, coherence and non-coherence sectors evolve independently. When it fails, the channel can transfer information between them. In that case, the coherence trajectory depends not only on contraction within the coherence sector but also on transfer into and out of it.

This observation motivates the first requirement of the proposed theory: a coherence index must be accompanied by a leakage term whenever the chosen operator sector is not invariant.

## 3. The Structural Data of Coherence Loss

We now define the four structural layers to be tracked.

### 3.1 Layer I: Coherence contraction

For a channel that preserves the coherence sector, define its restricted action

\\[ \mathcal E\_{\mathrm c} = \mathcal P\mathcal E\mathcal P \big|\_{\operatorname{Ran}\mathcal P}. \\]

If the sector is invariant, this is simply the restriction of \\(\mathcal E\\) to that sector. Its behavior under iteration is governed by the operator powers

\\[ \mathcal E\_{\mathrm c}^n. \\]

The asymptotic contraction scale is related to the spectral radius

\\[ r\_{\mathrm c}=r(\mathcal E\_{\mathrm c}) =\max\_{\lambda\in\sigma(\mathcal E\_{\mathrm c})}|\lambda|. \\]

For \\(r\_{\mathrm c}<1\\), every eigenoperator in the coherence sector decays asymptotically, provided the restriction has no additional non-decaying component. But \\(r\_{\mathrm c}\\) alone does not determine the finite-time norm of \\(\mathcal E\_{\mathrm c}^n\\), particularly for non-normal maps.

### 3.2 Layer II: Spectral redistribution

Let the eigenvalues of \\(\rho\\) be ordered as

\\[ p_1(\rho)\geq p_2(\rho)\geq\cdots\geq p_d(\rho)\geq0. \\]

The channel transforms the spectrum according to

\\[ \\{p_i(\rho)\\}\_{i=1}^d \longrightarrow \\{p_i(\mathcal E(\rho))\\}\_{i=1}^d. \\]

Useful diagnostics include the purity

\\[ \gamma(\rho)=\operatorname{Tr}(\rho^2), \\]

the von Neumann entropy

\\[ S(\rho)=-\operatorname{Tr}(\rho\log\rho), \\]

and spectral distance from a chosen reference state \\(\sigma\\),

\\[ D\_{\mathrm{spec}}(\rho,\sigma) = \left(\sum_i [p_i(\rho)-p_i(\sigma)]^2\right)^{1/2}. \\]

The last expression compares ordered eigenvalue lists. It is not a complete measure of state distinguishability because it discards eigenvectors.

No universal monotonicity of purity or entropy holds for every CPTP channel and every initial state. Unital channels have stronger spectral-ordering properties than general non-unital channels, but even then the interpretation depends on the chosen quantity and comparison state.

### 3.3 Layer III: Correlational change

A system \\(S\\) may be correlated with an ancilla \\(A\\). The joint state is \\(\rho\_{SA}\\), and local channel action produces

\\[ \rho\_{SA}'=(\mathcal E_S\otimes I_A)(\rho\_{SA}). \\]

Possible diagnostics include mutual information,

\\[ I(S{:}A)\_\rho = S(\rho_S)+S(\rho_A)-S(\rho\_{SA}), \\]

and, when appropriate, entanglement measures such as negativity or entanglement fidelity.

For a local CPTP map, quantum mutual information cannot increase under the data-processing inequality:

\\[ I(S{:}A)\_{\rho'} \leq I(S{:}A)\_\rho. \\]

This does not imply that every form of correlation must decrease monotonically. Classical correlations, quantum discord, and entanglement can respond differently, and some entanglement measures can exhibit non-monotonic behavior under more general multipartite operations or changing partitions.

The proposed framework therefore tracks a specified correlation measure rather than treating “correlation loss” as one universal scalar.

### 3.4 Layer IV: Conserved observables and invariant sectors

An observable \\(Q=Q^\dagger\\) is conserved in expectation for every initial state if

\\[ \mathcal E^\dagger(Q)=Q. \\]

Indeed,

\\[ \operatorname{Tr}[Q\mathcal E(\rho)] = \operatorname{Tr}[\mathcal E^\dagger(Q)\rho] = \operatorname{Tr}[Q\rho]. \\]

A stronger condition is preservation of the full probability distribution of \\(Q\\), which generally requires preservation of its spectral projectors or an appropriate compatibility condition with the channel.

For a continuous symmetry generated by \\(Q\\), covariance takes the form

\\[ \mathcal E(U\_\theta\rho U\_\theta^\dagger) = U\_\theta\mathcal E(\rho)U\_\theta^\dagger, \qquad U\_\theta=e^{-i\theta Q}. \\]

Covariance is not the same as conservation. A channel may respect a symmetry while transferring population between different charge sectors in a manner compatible with that symmetry.

The distinction is important: the conservation structure constrains the channel, but it does not uniquely determine its coherence lifetime.

## 4. Channel Geometry and the Proposed Structural Index

### 4.1 Why a single rate is insufficient

Suppose a coherence amplitude obeys

\\[ c\_{n+1}=\eta c_n. \\]

Then

\\[ c_n=\eta^n c_0. \\]

The scalar \\(\eta\\) determines this trajectory. It does not, however, determine how populations evolve, whether the channel is unital, how an ancilla becomes correlated with the system, or whether the channel transfers coherence between distinct sectors.

A rate extracted from one matrix element is therefore a property of a channel–state–observable triple, not necessarily a complete property of the channel.

### 4.2 Definition: restricted coherence contraction

Fix a coherence projection \\(\mathcal P\\) and a norm \\(\\|\cdot\\|\\) on its range. Define

\\[ \kappa\_{\mathrm c}(\mathcal E;\mathcal P) = \sup\_{\substack{X\in\operatorname{Ran}\mathcal P\\\X\ne0}} \frac{\\|\mathcal P\mathcal E(X)\\|} {\\|X\\|}. \\]

Equivalently,

\\[ \kappa\_{\mathrm c} = \\|\mathcal P\mathcal E\mathcal P \\|\_{\operatorname{Ran}\mathcal P\to\operatorname{Ran}\mathcal P} \\]

when the restriction is well-defined.

This is a one-step induced-norm contraction coefficient. It satisfies

\\[ \\|\mathcal E\_{\mathrm c}(X)\\| \leq\kappa\_{\mathrm c}\\|X\\|. \\]

If \\(\kappa\_{\mathrm c}<1\\), then

\\[ \\|\mathcal E\_{\mathrm c}^{\\,n}(X)\\| \leq\kappa\_{\mathrm c}^{\\,n}\\|X\\|. \\]

The coefficient depends on the norm, the coherence projection, and the channel. That dependence is not a defect; it makes explicit which operational notion of coherence is being bounded.

For an orthogonal projection in the Hilbert–Schmidt inner product, the Hilbert–Schmidt norm gives a particularly direct implementation. Other norms may yield tighter bounds for specific experiments.

### 4.3 The candidate invariant: spectral–correlational coherence signature

The proposed structural signature is the tuple

\\[ \boxed{ \mathfrak C\_{\mathcal P}(\mathcal E) = \big( r\_{\mathrm c}, \kappa\_{\mathrm c}, \ell\_{\mathrm c}, \mathfrak S, \mathfrak K \big) } \\]

with the following components:

- \\(r\_{\mathrm c}\\): spectral radius of the restricted coherence action;
- \\(\kappa\_{\mathrm c}\\): one-step contraction coefficient in the chosen norm;
- \\(\ell\_{\mathrm c}\\): a coherence-sector leakage coefficient;
- \\(\mathfrak S\\): a specified spectral-redistribution profile;
- \\(\mathfrak K\\): a specified correlational response profile.

The first two entries are channel-dependent numbers for a fixed sector and norm. The remaining entries may be functions of input states or state classes, rather than universal scalars.

Define leakage by

\\[ \ell\_{\mathrm c} = \\|(I-\mathcal P)\mathcal E\mathcal P\\|. \\]

This quantifies transfer from the selected coherence sector into its complement. A complementary transfer coefficient,

\\[ \ell\_{\mathrm{in}} = \\|\mathcal P\mathcal E(I-\mathcal P)\\|, \\]

quantifies the generation of the chosen coherence sector from the complementary sector.

If \\(\ell\_{\mathrm{in}}>0\\), an initially incoherent component can continually feed the coherence sector. A decay law based solely on \\(\kappa\_{\mathrm c}\\) then need not describe the full trajectory.

The signature \\(\mathfrak C\_{\mathcal P}\\) is a candidate classification invariant, not yet a demonstrated new invariant in the strongest mathematical sense. It is invariant under a change of Kraus representation because it is defined from the channel itself. It is not automatically invariant under arbitrary changes of basis, norm, or coherence projection. Those choices must be fixed as part of the operational definition.

### 4.4 A stricter notion of invariant

In mathematics, “invariant” often means unchanged under a specified equivalence relation. Here the natural equivalence is channel conjugation by a unitary \\(U\\), accompanied by the corresponding transformation of the coherence projection:

\\[ \mathcal E'(\rho) = U\mathcal E(U^\dagger\rho U)U^\dagger, \\]

\\[ \mathcal P'(X)=U\mathcal P(U^\dagger XU)U^\dagger. \\]

For unitarily invariant norms, the restricted spectrum and induced contraction coefficient are preserved under this joint transformation.

The signature is thus covariant with the physical reference structure and invariant under its consistent unitary relabeling. A stronger claim—that it classifies all channels up to physically relevant equivalence—would require proving that no two inequivalent channels share the same signature. That claim is not established here and is unlikely to hold for a finite tuple of scalar diagnostics.

## 5. Main Theorem: A Structural Bound on Coherence Lifetime

We now establish a lifetime bound for a class of channels with invariant coherence sectors.

### 5.1 Assumptions

Let \\(\mathcal H\\) be finite-dimensional, let \\(\mathcal E\\) be a fixed CPTP channel, and let \\(\mathcal P\\) be a linear projection satisfying

\\[ \mathcal E\mathcal P=\mathcal P\mathcal E. \\]

Assume the chosen coherence measure is

\\[ C\_{\mathcal P}(\rho) = \\|\mathcal P(\rho)\\|, \\]

or a norm-equivalent functional on the coherence sector. Suppose the restricted action has a uniform contraction coefficient

\\[ \kappa\_{\mathrm c} = \\|\mathcal E\_{\mathrm c}\\|<1. \\]

For a lifetime statement, define a threshold \\(0<\varepsilon<1\\) relative to the initial coherence:

\\[ C\_{\mathcal P}(\rho_n) \leq\varepsilon C\_{\mathcal P}(\rho_0). \\]

The discrete coherence lifetime is the first iteration index

\\[ N\_\varepsilon = \inf\left\\{ n\in\mathbb N: C\_{\mathcal P}(\rho_n) \leq\varepsilon C\_{\mathcal P}(\rho_0) \right\\}. \\]

### Theorem 5.1 — Coherence-lifetime upper bound

Under the assumptions above, if \\(C\_{\mathcal P}(\rho_0)>0\\), then

\\[ C\_{\mathcal P}(\rho_n) \leq \kappa\_{\mathrm c}^{\\,n} C\_{\mathcal P}(\rho_0). \\]

Consequently, for \\(0<\kappa\_{\mathrm c}<1\\),

\\[ \boxed{ N\_\varepsilon \leq \left\lceil \frac{\ln\varepsilon} {\ln\kappa\_{\mathrm c}} \right\rceil } \\]

is a valid upper bound on the number of channel applications required to reach the specified threshold.

If each channel application corresponds to a fixed physical interval \\(\Delta t\\), then

\\[ \boxed{ \tau\_\varepsilon \leq \Delta t \left\lceil \frac{\ln\varepsilon} {\ln\kappa\_{\mathrm c}} \right\rceil. } \\]

The bound is interpreted with the usual limiting cases: if \\(\kappa\_{\mathrm c}=0\\), coherence vanishes in one application; if \\(\kappa\_{\mathrm c}=1\\), this argument provides no finite lifetime bound.

#### Proof

Because \\(\mathcal P\\) commutes with \\(\mathcal E\\),

\\[ \mathcal P(\rho_n) = \mathcal E\_{\mathrm c}^{\\,n} \mathcal P(\rho_0). \\]

By the definition of the induced norm,

\\[ \\|\mathcal E\_{\mathrm c}(X)\\| \leq \kappa\_{\mathrm c}\\|X\\|. \\]

Applying this inequality successively gives

\\[ \begin{aligned} \\|\mathcal P(\rho_n)\\| &=\\|\mathcal E\_{\mathrm c}^{\\,n} \mathcal P(\rho_0)\\|\\\ &\leq\kappa\_{\mathrm c}^{\\,n} \\|\mathcal P(\rho_0)\\|. \end{aligned} \\]

Thus the threshold is guaranteed once

\\[ \kappa\_{\mathrm c}^{\\,n}\leq\varepsilon. \\]

Taking logarithms and noting that \\(\ln\kappa\_{\mathrm c}<0\\),

\\[ n\geq\frac{\ln\varepsilon}{\ln\kappa\_{\mathrm c}}. \\]

Taking the ceiling yields the claimed bound. Multiplication by the fixed interval \\(\Delta t\\) gives the time bound. \\(\square\\)

### 5.2 What the theorem establishes—and what it does not

The theorem is a genuine mathematical result, but its scope must be stated precisely.

It establishes a sufficient upper bound, not necessarily the exact lifetime. The bound can be loose because the induced norm maximizes over every operator in the coherence sector, whereas a particular initial state may occupy only rapidly contracting directions—or may not reach the maximizing direction at all.

It also does not prove that the structural signature is more predictive than standard channel methods. If \\(\kappa\_{\mathrm c}\\) is measured from the same decay trajectory being predicted, the result is a reformulation of known contraction reasoning. New predictive power requires independently determining \\(\kappa\_{\mathrm c}\\), or a tighter structural bound, from a channel model, calibration protocol, symmetry constraint, or microscopic interaction model.

That is the central experimental challenge of the theory.

## 6. Spectral Radius Versus Finite-Time Contraction

The spectral radius \\(r\_{\mathrm c}\\) and the induced norm \\(\kappa\_{\mathrm c}\\) answer different questions.

The spectral radius describes the asymptotic exponential scale of powers of a finite-dimensional linear operator:

\\[ \lim\_{n\to\infty} \\|\mathcal E\_{\mathrm c}^{\\,n}\\|^{1/n} = r\_{\mathrm c}. \\]

This is the finite-dimensional spectral-radius formula. But it does not imply

\\[ \\|\mathcal E\_{\mathrm c}^{\\,n}\\| \leq r\_{\mathrm c}^{\\,n} \\]

for finite \\(n\\).

For a normal operator in a compatible Hilbert-space norm, the induced norm equals the largest eigenvalue magnitude. For a non-normal operator, transient amplification can occur even when every eigenvalue lies strictly inside the unit disk.

### 6.1 Jordan-block correction

Consider a restricted linear map with a Jordan block

\\[ J=\begin{pmatrix} \lambda&1\\\ 0&\lambda \end{pmatrix}, \qquad |\lambda|<1. \\]

Its powers are

\\[ J^n= \begin{pmatrix} \lambda^n&n\lambda^{n-1}\\\ 0&\lambda^n \end{pmatrix}. \\]

The factor \\(n|\lambda|^{n-1}\\) can dominate the pure exponential term over an initial range of \\(n\\). Hence an eigenvalue-only prediction may underestimate the time required to reach a threshold.

For a diagonalizable restricted channel,

\\[ \mathcal E\_{\mathrm c} = V\Lambda V^{-1}, \\]

one has

\\[ \\|\mathcal E\_{\mathrm c}^{\\,n}\\| \leq \\|V\\|\\|V^{-1}\\|\\,r\_{\mathrm c}^{\\,n} \\]

for a compatible operator norm. Writing

\\[ K_V=\\|V\\|\\|V^{-1}\\|\geq1, \\]

the bound becomes

\\[ C\_{\mathcal P}(\rho_n) \leq K_V r\_{\mathrm c}^{\\,n} C\_{\mathcal P}(\rho_0). \\]

When \\(0\<r\_{\mathrm c}<1\\) and \\(K_V>\varepsilon\\), a sufficient threshold index is

\\[ N\_\varepsilon \leq \left\lceil \frac{\ln(\varepsilon/K_V)} {\ln r\_{\mathrm c}} \right\rceil, \\]

provided the right-hand side is nonnegative. This estimate may be much weaker than the induced-norm bound, but it makes the eigenvalue geometry explicit.

### 6.2 Proposed refinement

The most useful refinement is not to replace every contraction coefficient with a spectral radius. It is to report both:

\\[ \boxed{ \text{asymptotic scale }r\_{\mathrm c} \quad+\quad \text{finite-time envelope }B(n) } \\]

where \\(B(n)\\) is an independently established bound satisfying

\\[ \\|\mathcal E\_{\mathrm c}^{\\,n}\\|\leq B(n). \\]

For a normal restricted map, \\(B(n)=r\_{\mathrm c}^n\\). For a non-normal map, \\(B(n)\\) may require singular values, a condition-number bound, a Jordan-form estimate, or a directly certified power bound.

This two-part description separates long-time decay from transient behavior and avoids the false inference that eigenvalues alone determine a measured lifetime.

## 7. Continuous-Time Dynamics and Decoherence Rates

A time-homogeneous Markovian open-system evolution is often represented by a quantum dynamical semigroup

\\[ \mathcal E_t=e^{t\mathcal L}, \\]

where the generator \\(\mathcal L\\) has Lindblad form,

\\[ \mathcal L(\rho) = -i[H,\rho] + \sum_j\gamma_j \left( L_j\rho L_j^\dagger -\frac12\\{L_j^\dagger L_j,\rho\\} \right), \\]

with \\(\gamma_j\geq0\\) under the usual finite-dimensional, time-homogeneous assumptions.

If the coherence sector is invariant under \\(\mathcal L\\), define

\\[ \mathcal L\_{\mathrm c} = \mathcal P\mathcal L\mathcal P \big|\_{\operatorname{Ran}\mathcal P}. \\]

Then

\\[ \mathcal E\_{\mathrm c}(t)=e^{t\mathcal L\_{\mathrm c}}. \\]

Let \\(\mu\_{\max}\\) denote the largest real part among eigenvalues of \\(\mathcal L\_{\mathrm c}\\). If \\(\mu\_{\max}<0\\), the asymptotic envelope decays exponentially, up to possible polynomial factors arising from nontrivial Jordan blocks.

In the normal case, a direct bound takes the form

\\[ \\|\mathcal E\_{\mathrm c}(t)\\| \leq e^{\mu\_{\max}t}. \\]

For a threshold \\(C(t)\leq\varepsilon C(0)\\), this yields

\\[ \tau\_\varepsilon \leq \frac{\ln(1/\varepsilon)} {-\mu\_{\max}}. \\]

This is the continuous-time counterpart of Theorem 5.1 under the stated normality and invariance conditions.

In a general non-normal semigroup, the spectral abscissa alone does not provide that finite-time bound. A valid analysis must establish a bound on \\(\\|e^{t\mathcal L\_{\mathrm c}}\\|\\), not merely inspect the real parts of its eigenvalues.

### 7.1 Non-Markovian dynamics

If the reduced evolution is not a semigroup, the family \\(\\{\mathcal E_t\\}\\) need not satisfy

\\[ \mathcal E\_{t+s}=\mathcal E_t\mathcal E_s. \\]

A fixed generator may not exist, and coherence may temporarily revive. The channel signature must then be time-dependent:

\\[ \mathfrak C\_{\mathcal P}(t) = \mathfrak C\_{\mathcal P}(\mathcal E_t). \\]

A lifetime bound can still be constructed if one independently establishes a contraction envelope \\(B(t)\\) satisfying

\\[ C\_{\mathcal P}(\rho_t) \leq B(t)C\_{\mathcal P}(\rho_0), \\]

with \\(B(t)\\) falling below the desired threshold. But the semigroup theorem cannot be transferred automatically to arbitrary non-Markovian processes.

## 8. Exactly Solvable Example I: Qubit Dephasing

Consider a qubit in the basis \\(\\{|0\rangle,|1\rangle\\}\\), with initial state

\\[ \rho_0= \begin{pmatrix} p&c_0\\\ c_0^\*&1-p \end{pmatrix}. \\]

A phase-damping channel can be written

\\[ \mathcal E(\rho)= \begin{pmatrix} \rho\_{00}&\eta\rho\_{01}\\\ \eta^\*\rho\_{10}&\rho\_{11} \end{pmatrix}, \qquad |\eta|\leq1. \\]

After \\(n\\) applications,

\\[ \rho_n= \begin{pmatrix} p&\eta^n c_0\\\ (\eta^\*)^n c_0^\*&1-p \end{pmatrix}. \\]

The off-diagonal coherence satisfies

\\[ C_2(\rho_n)=|\eta|^n C_2(\rho_0). \\]

The coherence sector is invariant, and its restricted action is multiplication by \\(\eta\\). Therefore,

\\[ r\_{\mathrm c}=\kappa\_{\mathrm c}=|\eta| \\]

for the natural Hilbert–Schmidt norm on the one-dimensional complex coherence direction, with the phase of \\(\eta\\) contributing a rotation but not a change in magnitude.

The threshold lifetime is exactly

\\[ N\_\varepsilon= \left\lceil \frac{\ln\varepsilon}{\ln|\eta|} \right\rceil \\]

for \\(0<|\eta|<1\\), except that the ceiling convention depends on whether the initial state already meets the threshold at iteration zero. For the usual case \\(0<\varepsilon<1\\), the expression gives the first nonnegative integer meeting the threshold.

### 8.1 Spectral redistribution is not identical to coherence decay

For the qubit above,

\\[ \operatorname{Tr}(\rho_n^2) = p^2+(1-p)^2+2|c_0|^2|\eta|^{2n}. \\]

Thus the purity approaches

\\[ p^2+(1-p)^2, \\]

which is the purity of the diagonal state with the same populations.

This is a useful demonstration of the distinction between coherence loss and total mixing. If \\(p=0\\) or \\(p=1\\), positivity forces \\(c_0=0\\), and the state is already pure and incoherent. If \\(p=1/2\\), the diagonal limiting state is maximally mixed, and purity falls to \\(1/2\\).

For intermediate \\(p\\), coherence loss can occur while the final state retains nonzero population imbalance. The spectral endpoint therefore carries information not contained in the coherence lifetime alone.

### 8.2 A physical prediction

If the same channel is applied at time intervals \\(\Delta t\\), and independent calibration establishes \\(|\eta|\\), then the time required to reduce coherence to a fraction \\(\varepsilon\\) is predicted by

\\[ \tau\_\varepsilon = \Delta t\\, \left\lceil \frac{\ln\varepsilon}{\ln|\eta|} \right\rceil. \\]

In a continuous-time Markovian dephasing model with

\\[ \eta(t)=e^{-\Gamma t}, \\]

the threshold time is

\\[ \tau\_\varepsilon = \frac{\ln(1/\varepsilon)}{\Gamma}. \\]

This recovers the standard exponential-decay result. It is not a new physical law. The potential advance would arise if a structural calculation predicted \\(\Gamma\\), or bounded it more tightly, without fitting the coherence decay itself.

## 9. Exactly Solvable Example II: Amplitude Damping

Consider an amplitude-damping channel with probability \\(\gamma\in[0,1]\\), with Kraus operators

\\[ K_0= \begin{pmatrix} 1&0\\\ 0&\sqrt{1-\gamma} \end{pmatrix}, \qquad K_1= \begin{pmatrix} 0&\sqrt{\gamma}\\\ 0&0 \end{pmatrix}. \\]

Its action on a general qubit state is

\\[ \mathcal E(\rho)= \begin{pmatrix} \rho\_{00}+\gamma\rho\_{11} & \sqrt{1-\gamma}\rho\_{01}\\\ \sqrt{1-\gamma}\rho\_{10} & (1-\gamma)\rho\_{11} \end{pmatrix}. \\]

The coherence amplitude contracts by

\\[ \eta\_{\mathrm c}=\sqrt{1-\gamma}, \\]

while the excited-state population contracts by

\\[ \eta\_{\mathrm p}=1-\gamma. \\]

After \\(n\\) applications,

\\[ \rho\_{11}^{(n)}=(1-\gamma)^n\rho\_{11}^{(0)}, \\]

and

\\[ \rho\_{01}^{(n)}=(1-\gamma)^{n/2}\rho\_{01}^{(0)}. \\]

Consequently, coherence and population deviation decay on different scales. In particular,

\\[ |\rho\_{01}^{(n)}| = (1-\gamma)^{n/2}|\rho\_{01}^{(0)}|. \\]

The channel is non-unital for \\(\gamma>0\\), since

\\[ \mathcal E(I)\neq I. \\]

It drives the system toward the ground state rather than toward the maximally mixed state.

### 9.1 Structural distinction from pure dephasing

A pure-dephasing channel can have the same off-diagonal contraction factor as an amplitude-damping channel. Yet the two channels have different population dynamics, different fixed points, and different effects on the spectrum.

For a dephasing channel, populations in the reference basis are unchanged. For amplitude damping, the excited-state population flows toward the ground state. Thus the tuple

\\[ (r\_{\mathrm c},\kappa\_{\mathrm c}, \text{population dynamics},\text{fixed-point structure}) \\]

distinguishes these channels even when one selected coherence trajectory is identical.

This is the simplest illustration of the motivation for structural classification.

### 9.2 A caveat about spectral information

The eigenvalues of the output density matrix depend on both the diagonal entries and the off-diagonal coherence. They cannot be inferred from the off-diagonal contraction factor alone.

For a qubit,

\\[ \lambda\_\pm(\rho) = \frac12 \left( 1\pm \sqrt{(2p-1)^2+4|c|^2} \right). \\]

The spectrum therefore changes through the joint evolution of populations and coherence. A complete predictive model must specify both.

## 10. Correlations with an Ancilla: Coherence Is Not Entanglement

Let the system qubit \\(S\\) and ancilla \\(A\\) begin in the Bell state

\\[ |\Phi^+\rangle = \frac{|00\rangle+|11\rangle}{\sqrt2}. \\]

Apply a dephasing channel to \\(S\\), with real coherence factor \\(0\leq\eta\leq1\\). The resulting joint state is

\\[ \rho\_{SA}(\eta) = \frac12 \left( |00\rangle\langle00| + |11\rangle\langle11| + \eta|00\rangle\langle11| + \eta|11\rangle\langle00| \right). \\]

The system marginal is

\\[ \rho_S=\frac{I}{2}, \\]

for every \\(\eta\\). Thus the local system remains maximally mixed, even as the joint state loses entanglement.

The eigenvalues of the joint state are

\\[ \lambda\_\pm=\frac{1\pm\eta}{2}, \\]

with two additional zero eigenvalues. Its entropy is

\\[ S(\rho\_{SA}) = h_2\left(\frac{1+\eta}{2}\right), \\]

where

\\[ h_2(x)=-x\log x-(1-x)\log(1-x) \\]

is the binary entropy in the selected logarithm base.

Because both marginals are maximally mixed,

\\[ I(S{:}A) = 2\log2 - h_2\left(\frac{1+\eta}{2}\right). \\]

For this particular state and channel, mutual information decreases as \\(\eta\\) falls from one to zero. At \\(\eta=1\\), the joint state is pure and maximally entangled. At \\(\eta=0\\), the state is a classical mixture of \\(|00\rangle\\) and \\(|11\rangle\\), with nonzero classical correlations but no entanglement.

### 10.1 What this example teaches

The local reduced state \\(\rho_S=I/2\\) contains no information about the changing entanglement. A description based only on the system's local density matrix would miss the distinction between a maximally entangled pure state and a classically correlated mixed state.

The correlation layer must therefore be specified at the level of the system–ancilla state or an equivalent operational probe. It cannot be reconstructed from the system's local coherence alone.

For the Bell-state example, the concurrence equals \\(\eta\\) for \\(0\leq\eta\leq1\\), while the mutual information follows a nonlinear entropy function. Different correlation diagnostics therefore yield different apparent lifetimes.

A structural theory should not combine these quantities into a single scalar without specifying the intended task. A coherence lifetime, entanglement lifetime, and mutual-information threshold time are distinct operational observables.

## 11. Conserved Quantities as Constraints on Coherence Dynamics

Conservation laws can sharply restrict which coherence components are allowed to evolve into which other components.

Suppose \\(Q\\) has spectral decomposition

\\[ Q=\sum_q q\\,\Pi_q. \\]

An operator \\(X\\) decomposes into charge sectors,

\\[ X=\sum\_{q,q'}\Pi_qX\Pi\_{q'}. \\]

The component \\(\Pi_qX\Pi\_{q'}\\) carries a charge difference \\(q-q'\\) under the symmetry generated by \\(Q\\).

If the channel is covariant under \\(U\_\theta=e^{-i\theta Q}\\), then it preserves the symmetry mode structure. In particular, operators transforming with distinct characters of the symmetry cannot mix arbitrarily under the channel.

For a \\(U(1)\\) symmetry, an operator mode \\(X_m\\) satisfies

\\[ U\_\theta X_m U\_\theta^\dagger = e^{-im\theta}X_m. \\]

Covariance implies

\\[ \mathcal E(X_m) \\]

lies in the same mode, subject to degeneracies and the relevant representation structure. This can create invariant coherence sectors and make Theorem 5.1 applicable mode by mode.

### 11.1 Mode-dependent contraction

Let \\(\mathcal P_m\\) project onto a symmetry mode. Define

\\[ \kappa_m= \\|\mathcal P_m\mathcal E\mathcal P_m\\|. \\]

Each mode can have its own contraction bound:

\\[ \\|\mathcal P_m(\rho_n)\\| \leq \kappa_m^n\\|\mathcal P_m(\rho_0)\\|. \\]

The result is a coherence spectrum rather than one universal rate. Some modes may be rapidly suppressed; others may be protected by a symmetry, conservation law, or decoherence-free subspace.

If \\(\kappa_m=1\\), the norm bound does not imply decay. A unit-modulus eigenvalue may correspond to a phase rotation, a conserved mode, or periodic dynamics rather than irreversible coherence loss.

### 11.2 Conservation is not immunity to decoherence

A conserved expectation value does not guarantee that every coherence involving its eigenspaces is preserved. Conversely, a channel can destroy certain coherences while conserving the population distribution of the associated observable.

The relevant mathematical object is therefore the joint structure of:

- the channel's invariant operator sectors;
- the observable algebra preserved by the adjoint channel;
- the contraction properties within each sector.

The conserved algebra constrains the available dynamics, while the restricted channel determines how quickly particular components disappear.

## 12. A General Leakage Bound for Non-Invariant Coherence Sectors

The commutation condition

\\[ \mathcal E\mathcal P=\mathcal P\mathcal E \\]

is restrictive. Physical channels may mix the chosen coherence sector with other operator components. We therefore require a bound that remains useful when exact sector invariance fails.

Write

\\[ \rho\_{n+1,\mathrm c} = \mathcal P\mathcal E(\rho_n). \\]

Decompose the state into

\\[ \rho_n=\mathcal P(\rho_n)+(I-\mathcal P)(\rho_n). \\]

Then

\\[ \begin{aligned} \rho\_{n+1,\mathrm c} ={}& \mathcal P\mathcal E\mathcal P(\rho_n)\\\ &+ \mathcal P\mathcal E(I-\mathcal P)(\rho_n). \end{aligned} \\]

Taking norms yields

\\[ \\|\rho\_{n+1,\mathrm c}\\| \leq \kappa\_{\mathrm c}\\|\rho\_{n,\mathrm c}\\| + \ell\_{\mathrm{in}} \\|\rho\_{n,\perp}\\|, \\]

where

\\[ \kappa\_{\mathrm c} = \\|\mathcal P\mathcal E\mathcal P\\|, \qquad \ell\_{\mathrm{in}} = \\|\mathcal P\mathcal E(I-\mathcal P)\\|. \\]

Iterating this inequality gives

\\[ \boxed{ \\|\rho\_{n,\mathrm c}\\| \leq \kappa\_{\mathrm c}^{\\,n}\\|\rho\_{0,\mathrm c}\\| + \ell\_{\mathrm{in}} \sum\_{j=0}^{n-1} \kappa\_{\mathrm c}^{\\,n-1-j} \\|\rho\_{j,\perp}\\|. } \\]

This follows by induction: each step contracts the previous coherence component and adds the incoming contribution from the complementary sector.

If a uniform bound

\\[ \\|\rho\_{j,\perp}\\|\leq M \\]

is known, then for \\(0\leq\kappa\_{\mathrm c}<1\\),

\\[ \\|\rho\_{n,\mathrm c}\\| \leq \kappa\_{\mathrm c}^{\\,n}\\|\rho\_{0,\mathrm c}\\| + \ell\_{\mathrm{in}}M \frac{1-\kappa\_{\mathrm c}^{\\,n}} {1-\kappa\_{\mathrm c}}. \\]

The second term is a coherence floor arising from continuous feeding of the chosen sector. If

\\[ \frac{\ell\_{\mathrm{in}}M}{1-\kappa\_{\mathrm c}} \\]

exceeds the target threshold, the bound does not guarantee that coherence ever falls below that threshold.

This is an important improvement in interpretation, not yet a new universal invariant: it distinguishes intrinsic contraction from externally or internally generated coherence.

### 12.1 Operational meaning

In an experiment, apparent coherence revival may have at least three origins:

1. a genuinely non-Markovian return of environmental information;
2. transfer into the selected coherence sector from other system degrees of freedom;
3. a change in the measurement basis or effective observable.

A single fitted decay rate cannot distinguish these mechanisms. The leakage terms make them explicit in the mathematical model.

## 13. Entropy Production, Purity, and the Limits of Spectral Monotonicity

A channel's action on coherence is related to, but not determined by, its action on entropy and purity.

For any density matrix,

\\[ \operatorname{Tr}(\rho^2) = \sum_i p_i(\rho)^2. \\]

Purity is a function of the spectrum alone. Coherence, however, depends on the relationship between the state and a specified reference structure. Two states with the same eigenvalues can have different coherence in the same basis.

For example, a pure qubit state can be written

\\[ |\psi\rangle = \cos\frac{\theta}{2}|0\rangle + e^{i\phi}\sin\frac{\theta}{2}|1\rangle. \\]

All such pure states have the same spectrum \\(\\{1,0\\}\\), yet their off-diagonal magnitude is

\\[ |\rho\_{01}|=\frac{|\sin\theta|}{2}. \\]

It vanishes at the basis states and is maximal for equal superpositions. Thus no function of the density-operator eigenvalues alone can determine basis-specific coherence.

### 13.1 Unital channels

A unital channel satisfies

\\[ \mathcal E(I)=I. \\]

In finite dimensions, a unital CPTP map is doubly stochastic in the quantum sense. Its output spectrum is majorized by the input spectrum:

\\[ \lambda(\mathcal E(\rho)) \prec\lambda(\rho), \\]

where eigenvalues are arranged in nonincreasing order.

This entails that the output cannot be more spectrally concentrated than the input in the majorization order. In particular, von Neumann entropy cannot decrease under a unital channel:

\\[ S(\mathcal E(\rho))\geq S(\rho). \\]

Purity also cannot increase under such a channel. These properties do not hold for arbitrary non-unital channels, which may purify a system by relaxing it toward a pure fixed point.

### 13.2 Entropy production is not a universal coherence measure

A pure-dephasing channel can reduce coherence while leaving populations unchanged. An amplitude-damping channel can reduce coherence while driving the system toward a pure ground state. The latter can decrease entropy despite losing coherence.

Consequently, the sign of

\\[ \Delta S=S(\mathcal E(\rho))-S(\rho) \\]

does not classify coherence loss without additional assumptions.

The spectral layer of the proposed signature should therefore report the behavior relevant to the channel class: purity change, entropy change, majorization relations, or a full spectral profile. It should not presume that every channel generates entropy monotonically.

### 13.3 A spectral response profile

For a specified state family \\(\rho(\theta)\\), define the spectral response

\\[ \mathfrak S\_{\mathcal E}[\rho(\theta)] = \left\\{ \lambda_i\big(\mathcal E(\rho(\theta))\big) \right\\}\_{i=1}^d. \\]

This profile can be compared with the coherence response

\\[ \mathfrak C\_{\mathcal E}[\rho(\theta)] = C\_{\mathcal P}(\mathcal E(\rho(\theta))). \\]

A useful empirical test is to determine whether the spectral profile predicts coherence loss beyond the restricted channel contraction coefficient. If not, the additional spectral layer may be redundant for that system class. If it does, the improvement must be quantified through an out-of-sample prediction or a tighter proven bound.

## 14. An Operational Classification of Coherence-Loss Mechanisms

The framework suggests classifying channels by their structural action rather than by the labels “dephasing” or “damping” alone.

| Structural class      | Mathematical signature                                        | Typical behavior                                               | Lifetime implication                                    |
| --------------------- | ------------------------------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------- |
| Pure contraction      | Invariant coherence sector, \\(\kappa\_{\mathrm c}<1\\)       | Monotonic norm bound                                           | Exponential upper bound                                 |
| Symmetry-protected    | Nontrivial fixed or peripheral sector                         | Some modes persist                                             | Infinite or undefined lifetime for protected components |
| Population-coupled    | Coherence couples to populations                              | Coherence may be generated or suppressed by other sectors      | Requires leakage-aware bound                            |
| Non-unital relaxation | Fixed point differs from maximally mixed state                | Coherence and entropy may decrease together or separately      | Depends on the target state and mode                    |
| Non-normal transient  | Spectral radius below one but powers exhibit transient growth | Early-time decay can deviate from asymptotic exponential       | Requires a finite-time envelope                         |
| Non-Markovian         | No fixed semigroup generator in general                       | Revivals and time-dependent contraction                        | Requires time-resolved bounds                           |
| Correlation-selective | Local coherence and ancilla correlations evolve differently   | Entanglement can disappear while classical correlations remain | Separate coherence and correlation lifetimes            |

These categories are not mutually exclusive. A non-unital channel can also be non-normal; a symmetry-protected channel can contain rapidly contracting modes; and a time-dependent process can preserve some observables while erasing others.

The table is a taxonomy of mechanisms, not a proof that every physical channel belongs to exactly one class.

## 15. Does the Proposed Signature Add Predictive Power?

This is the decisive question. A framework that combines existing channel diagnostics can be mathematically useful without being a new theory of decoherence.

### 15.1 The redundancy problem

In finite dimensions, a CPTP channel is already a complete mathematical description of the reduced system's evolution at the modeled time step. If the full channel is known exactly, every output state and every well-defined observable trajectory can, in principle, be calculated from it.

Therefore, a signature computed entirely from the channel cannot contain information absent from that fully specified channel in an information-theoretic sense.

Its possible value lies elsewhere:

- Compression: a small number of channel features may predict lifetimes across a family of states.
- Robustness: bounds may remain valid under model uncertainty.
- Identifiability: the signature may distinguish mechanisms that produce similar single-observable decay curves.
- Experimental efficiency: a restricted set of measurements may estimate the relevant bound more easily than full process tomography.
- Generalization: the signature may predict a lifetime for an unmeasured initial state or system size within a specified class.

These are meaningful forms of predictive advantage, but each must be demonstrated.

### 15.2 The non-tautological prediction criterion

Let \\(\Theta\\) denote the parameters of a channel model. A structural predictor has the form

\\[ \widehat{\tau}\_\varepsilon = F\big(\mathfrak C\_{\mathcal P}(\mathcal E\_\Theta), \varepsilon\big). \\]

It adds predictive value only if the inputs to \\(F\\) can be independently determined, without fitting the target lifetime \\(\tau\_\varepsilon\\).

A stronger test compares it with a baseline predictor \\(F_0\\) using the same experimental resources. If the new signature uses full process tomography while the baseline uses a single coherence measurement, an apparent improvement may merely reflect more data.

A fair comparison should control the information available to each method.

### 15.3 Candidate advance: a certified lifetime interval

A particularly defensible target is not an exact lifetime but an interval

\\[ \tau\_\varepsilon \in [\tau\_\varepsilon^{-},\tau\_\varepsilon^{+}] \\]

derived from independently estimated channel parameters and their uncertainties.

For example, suppose the restricted contraction coefficient is known to lie within

\\[ \kappa\_{\mathrm c}\in[\kappa\_-,\kappa\_+], \qquad 0\leq\kappa\_-\leq\kappa\_+<1. \\]

Since a larger contraction coefficient gives a weaker guarantee, the robust upper bound is

\\[ N\_\varepsilon \leq \left\lceil \frac{\ln\varepsilon}{\ln\kappa\_+} \right\rceil, \\]

for \\(0<\kappa\_+<1\\). The inequality remains valid for every channel in the estimated interval, assuming the invariant-sector and norm conditions hold.

This yields a model-robust guarantee rather than a point estimate. The gain is practical only if the interval is narrower or more reliable than existing methods at comparable measurement cost.

### 15.4 Candidate advance: mode-resolved lifetime prediction

A single channel may have multiple coherence modes \\(m\\), each with a contraction coefficient \\(\kappa_m\\). If the initial coherence decomposes as

\\[ \rho\_{\mathrm c}(0)=\sum_m X_m, \\]

then the triangle inequality gives

\\[ C\_{\mathcal P}(\rho_n) \leq \sum_m \kappa_m^n\\|X_m\\|. \\]

This is potentially more informative than a single-rate model. A rapidly decaying mode can dominate early behavior, while a slowly decaying mode controls the long-time tail.

The mode-resolved envelope is predictive only when the decomposition and contraction factors are independently obtained. Otherwise, it is simply a more elaborate fit.

## 16. A Sharper Bound for Multimode Coherence

The mode-resolved expression can be made more precise when the coherence sector admits a direct-sum decomposition into invariant subspaces:

\\[ \operatorname{Ran}\mathcal P = \bigoplus\_{m=1}^{M}\mathcal V_m, \\]

with

\\[ \mathcal E\_{\mathrm c}(\mathcal V_m) \subseteq\mathcal V_m. \\]

Let \\(P_m\\) be the projection onto \\(\mathcal V_m\\). Assume the chosen norm is compatible with this decomposition, and define

\\[ \kappa_m = \\|\mathcal E\_{\mathrm c}|\_{\mathcal V_m}\\|<1. \\]

Write

\\[ X_0=\mathcal P(\rho_0)=\sum_m X_m, \qquad X_m=P_mX_0. \\]

Then

\\[ X_n=\sum_m\mathcal E\_{\mathrm c}^{\\,n}(X_m), \\]

and hence

\\[ \boxed{ \\|X_n\\| \leq \sum_m\kappa_m^n\\|X_m\\|. } \\]

This bound can be substantially tighter than

\\[ \\|X_n\\|\leq \left(\max_m\kappa_m\right)^n\\|X_0\\| \\]

when the initial state has little weight in the slowest mode.

### 16.1 A lifetime bound from the spectral distribution of coherence

Define the initial mode weights

\\[ w_m=\frac{\\|X_m\\|}{\\|X_0\\|}, \\]

provided \\(X_0\neq0\\). For a direct-sum decomposition in which the norm is additive across modes, \\(\sum_mw_m=1\\); for a general decomposition, the weights need not sum to one.

Then

\\[ \frac{\\|X_n\\|}{\\|X_0\\|} \leq \sum_m w_m\kappa_m^n. \\]

The threshold condition is guaranteed whenever

\\[ \sum_mw_m\kappa_m^n\leq\varepsilon. \\]

This defines a mode-resolved upper envelope for the coherence lifetime. It need not have a closed-form solution, but the right-hand side is a finite sum of known exponential terms and can be solved numerically.

The result is a candidate for the most useful structural prediction in the framework: not a universal scalar invariant, but a bound combining the channel's mode contraction spectrum with the initial state's distribution across those modes.

### 16.2 What would make this result novel?

The inequality follows from standard operator-norm reasoning. Its mathematical validity is not in doubt under the stated assumptions, but the bound itself is not claimed as a new general theorem of quantum information.

Novelty would require an additional result, for example:

- a new theorem connecting experimentally accessible spectral data to the mode weights \\(w_m\\);
- a tighter upper envelope derived from symmetry and conservation constraints without full process tomography;
- a proof that a restricted signature predicts a system-size scaling law unavailable from existing baselines;
- a channel family in which the proposed structural bound is provably sharper than the best bound available under the same data constraints.

Until such a result is obtained, the mode-resolved lifetime is a useful research direction rather than an established advance over the mature channel framework.

## 17. Experimental Program: Predicting Coherence Lifetimes Before Measuring Them

The theory should be tested in a system for which the channel structure can be independently characterized and repeated evolution is experimentally accessible. A single-qubit platform is sufficient for the first test; multiqubit systems are needed to evaluate the correlational layer.

### 17.1 Stage I: Establish the channel class

Choose a well-defined system, such as a qubit undergoing controlled dephasing or amplitude damping. Specify:

- the Hilbert space and reference basis;
- the operational coherence measure;
- the channel or generator;
- the physical time interval per channel application;
- the observable or correlation threshold defining the lifetime;
- the conservation laws and symmetries expected to hold.

For a first experiment, a stationary qubit channel with an invariant coherence sector is preferable because the lifetime theorem can be tested without additional assumptions about leakage or memory effects.

### 17.2 Stage II: Estimate structural parameters independently

Estimate the channel parameters through a calibration protocol that does not fit the target lifetime curve. Depending on the system, this may involve process tomography, randomized benchmarking supplemented by appropriate coherence measurements, symmetry-resolved measurements, or direct characterization of the relevant channel eigenmodes.

Full process tomography is useful for a benchmark but may be too costly to constitute an experimental advantage. The longer-term objective is to infer the relevant contraction bound from a restricted set of measurements.

The channel model should be independently checked for complete positivity, trace preservation, and compatibility with the assumed invariant sectors.

### 17.3 Stage III: Predict the threshold crossing

Using the independently estimated contraction coefficient or mode-resolved envelope, calculate the predicted threshold iteration:

\\[ N\_\varepsilon^{\mathrm{pred}} = \min\left\\{ n\geq0: B(n)\leq\varepsilon \right\\}, \\]

where \\(B(n)\\) is the certified normalized coherence envelope.

For the single-mode contraction theorem,

\\[ B(n)=\kappa\_{\mathrm c}^{\\,n}. \\]

For a mode-resolved model,

\\[ B(n)=\sum_mw_m\kappa_m^n. \\]

The prediction must be registered before collecting the target lifetime data. Otherwise, the experiment cannot cleanly distinguish prediction from post hoc curve fitting.

### 17.4 Stage IV: Measure the coherence lifetime

Prepare the initial state, apply the channel repeatedly, and measure the specified coherence observable at a sequence of iteration counts. Estimate the first threshold crossing with confidence intervals.

Because finite-sample noise can create apparent threshold crossings, the protocol should specify in advance whether lifetime means:

- the first measured point below threshold;
- the fitted crossing of a validated decay model;
- the first time the upper confidence bound lies below threshold;
- or a persistence condition requiring the threshold to remain satisfied.

These operational definitions are not interchangeable.

### 17.5 Stage V: Test the additional structural predictions

For selected experiments, measure spectral and correlational observables in addition to local coherence. Examples include purity, output-state eigenvalues, ancilla mutual information, and entanglement fidelity.

Compare the structural model against established alternatives using the same calibration data and measurement budget. Report prediction error, confidence-interval coverage, calibration cost, and performance on initial states excluded from model fitting.

### 17.6 Stage VI: Test beyond the original calibration

A meaningful theory should generalize. Repeat the experiment for different initial states, channel strengths, system sizes, or symmetry sectors within the stated domain.

The key question is whether the independently determined structural signature predicts lifetimes across this family better than a baseline model using the same information.

A theory that succeeds only for the state from which its parameters were fitted has demonstrated characterization, not additional predictive power.

## 18. Falsifiability and Failure Conditions

The proposal must be capable of failing. The following outcomes would materially weaken or refute specific claims.

### 18.1 Failure of the contraction bound

If a measured evolution satisfying the stated assumptions violates

\\[ C\_{\mathcal P}(\rho_n) \leq \kappa\_{\mathrm c}^{\\,n} C\_{\mathcal P}(\rho_0), \\]

then at least one of the assumed conditions, the channel estimate, the norm bound, or the coherence measurement is incorrect. Reproducible violation after these possibilities are controlled would invalidate the claimed application of the theorem.

### 18.2 Failure of the invariant-sector assumption

If the channel transfers significant amplitude between the coherence and complementary sectors, the invariant-sector theorem is not directly applicable. A successful description would require the leakage-aware bound or a more complete block-operator model.

This is not a falsification of the general framework, but it is a falsification of an unqualified use of the simpler lifetime formula.

### 18.3 No gain over standard methods

Suppose the structural signature predicts lifetimes no more accurately than a fitted exponential, a standard Lindblad model, or an existing channel-contraction bound, when all methods are given comparable calibration data.

Then the claim of additional predictive power fails for that system class. The framework may still be useful as a taxonomy or diagnostic, but it would not have established the proposed advance.

### 18.4 Failure of the spectral layer

If spectral redistribution does not improve prediction, tighten bounds, or distinguish relevant channel classes beyond the coherence-sector contraction data, then the spectral component should be removed from the minimal predictor for that domain.

The theory should not retain a variable merely because it is conceptually attractive.

### 18.5 Failure of the correlation layer

If correlations with an ancilla are fully predicted by the existing channel model and provide no additional practical information under the experimental constraints, then the correlational component is redundant for that task.

Conversely, if local coherence fails to predict the correlation lifetime, this demonstrates that the two observables must remain separate—not that they can automatically be unified by a new scalar.

### 18.6 Failure of universality

If different systems require incompatible definitions of coherence, sector projections, or lifetime thresholds, the theory cannot claim a single universal coherence-loss invariant. It may still yield a family of invariants indexed by the operational structure.

The appropriate scientific response to such a result is a narrower theorem, not an unsupported universalization.

## 19. Relation to Established Quantum Information Theory

The mathematical framework is adjacent to several mature research areas. Its contribution must be assessed against them rather than in isolation.

| Established framework                | What it already provides                                              | Remaining question for this proposal                                                              |
| ------------------------------------ | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| CPTP channel theory                  | Complete description of finite-dimensional quantum operations         | Can a reduced structural signature predict selected outputs more efficiently?                     |
| Lindblad dynamics                    | Markovian continuous-time generators and decay modes                  | Can independent structural data improve lifetime bounds beyond generator analysis?                |
| Quantum resource theory of coherence | Basis-relative coherence measures and free operations                 | Can symmetry-resolved contraction provide useful bounds for a restricted resource class?          |
| Quantum dynamical semigroups         | Spectral analysis of long-time behavior                               | Can finite-time non-normality be bounded more tightly from accessible data?                       |
| Quantum information theory           | Entanglement, mutual information, distinguishability, data processing | Which joint diagnostics improve prediction without redundant measurements?                        |
| Process tomography                   | Reconstruction of channel action                                      | Can the relevant lifetime be predicted with fewer measurements than full reconstruction requires? |
| Non-Markovian open-system theory     | Memory effects, divisibility criteria, coherence revivals             | Can a time-dependent structural envelope give robust lifetime guarantees?                         |

Several parts of the proposed framework are therefore established mathematics in a new organizational arrangement. The new contribution is not the existence of CPTP maps, the spectral radius, or exponential contraction. It is the research program of identifying a minimal, independently estimable structural signature that predicts coherence thresholds across a specified family of channels.

That program remains open.

## 20. The Identifiability Problem

A structural index can only support a classification theorem if its limitations are explicit.

### 20.1 Distinct channels can share a coherence contraction factor

Pure dephasing and amplitude damping can have the same off-diagonal contraction factor. Their actions on populations, fixed points, and spectra differ. Therefore, the scalar \\(\kappa\_{\mathrm c}\\) cannot classify arbitrary quantum channels.

### 20.2 Distinct channels can share several coarse diagnostics

Even if two channels have the same restricted coherence spectrum, the same purity trajectory for a selected state, and the same value of one correlation measure, they need not agree on other inputs or observables.

A finite collection of state-dependent diagnostics generally does not reconstruct the entire channel.

### 20.3 Full channel equivalence is stronger than signature equality

Two channels are operationally equivalent only relative to a specified domain of inputs, outputs, and allowed experiments. Equality of a structural signature does not imply equality of their Choi operators, equality of their action on an ancilla, or equality of their multi-step behavior.

The signature should thus be interpreted as a predictive descriptor for a declared task, unless a stronger equivalence theorem is proved.

### 20.4 A minimality theorem remains desirable

A substantial mathematical advance would be a theorem identifying the minimal channel data sufficient to predict the coherence lifetime for a particular class.

For example, one might seek conditions under which the threshold lifetime is determined by:

\\[ \big\\{\kappa_m,w_m\big\\}\_{m=1}^M \\]

and no additional information about the channel is required.

Such a result would establish sufficiency, not universal completeness. Its domain would be the stated channel family and operational coherence measure.

A further result could show that any predictor using less information must incur a nonzero worst-case error. That would turn the search for a structural invariant into a rigorous problem of predictive identifiability.

## 21. A Proposed Research Theorem: Minimal Structural Sufficiency

The most promising direction is to replace the ambition of a universal coherence invariant with a precise sufficiency result.

Let \\(\mathfrak E\\) be a family of channels on a finite-dimensional system. Let \\(\mathfrak P\\) be a fixed coherence projection and let \\(\mathcal X\\) be a specified set of admissible initial states.

Suppose each channel \\(\mathcal E\in\mathfrak E\\) admits an invariant decomposition

\\[ \operatorname{Ran}\mathfrak P = \bigoplus\_{m=1}^{M}\mathcal V_m \\]

with known restricted contraction bounds

\\[ \\|\mathcal E|\_{\mathcal V_m}\\|\leq\kappa_m. \\]

Suppose also that every initial state in \\(\mathcal X\\) has known mode-weight bounds

\\[ \\|P_m\mathfrak P(\rho)\\|\leq w_m(\rho). \\]

Then

\\[ C\_{\mathfrak P}(\mathcal E^n(\rho)) \leq \sum\_{m=1}^{M} w_m(\rho)\kappa_m^n. \\]

This is a direct consequence of the invariant decomposition and triangle inequality. It gives a sufficient lifetime bound for every \\(\rho\in\mathcal X\\).

### 21.1 The open minimality question

The genuinely new theorem would establish that, for a specified channel family, the mode bounds and initial weights are not merely sufficient but optimal among all predictors using the same information.

That would require an adversarial or minimax comparison. One would define a predictor class \\(\mathfrak F\\), an error metric for lifetime predictions, and the allowed calibration information. Then one would seek to prove a lower bound on the worst-case error of every predictor that discards specified structural data.

For example, if two channels are indistinguishable under a restricted calibration protocol but have different threshold lifetimes, no predictor using only that protocol can correctly predict both lifetimes with arbitrarily small error.

Formally, if channels \\(\mathcal E_1,\mathcal E_2\\) are observationally indistinguishable under the allowed measurements but

\\[ |\tau\_\varepsilon(\mathcal E_1,\rho) -\tau\_\varepsilon(\mathcal E_2,\rho)| \geq\delta, \\]

then any common point prediction must incur absolute error at least \\(\delta/2\\) on one of the two cases.

This simple minimax observation identifies a concrete route to a meaningful result: determine which structural measurements eliminate such ambiguities for the chosen class.

### 21.2 Why this is preferable to a universal scalar

A universal scalar would have to compress many inequivalent channel actions into one number. That compression generally loses information.

A task-specific sufficient signature is more defensible. It specifies:

1. the channel family;
2. the coherence observable;
3. the initial-state class;
4. the allowed calibration measurements;
5. the lifetime threshold;
6. the proven prediction guarantee.

This structure makes it possible to prove sufficiency, demonstrate minimality, and identify failure conditions.

## 22. Limitations of the Present Theory

The results established here are conditional and should not be overstated.

First, the channel is assumed to be known or bounded. The framework does not derive a CPTP map from microscopic system–environment dynamics. Such a derivation would require additional assumptions about the environment, system–environment interaction, initial correlations, and the validity of the reduced dynamical description.

Second, coherence is operationally defined. The projection \\(\mathcal P\\) is not uniquely specified by the density matrix alone. It depends on a preferred basis, symmetry, observable algebra, or resource-theoretic convention. Different choices can yield different contraction factors and lifetimes.

Third, spectral and correlational data are not universally monotone. Unitality, locality, state preparation, and the selected correlation measure matter. A single scalar cannot be presumed to order every channel's decoherence behavior.

Fourth, non-normality matters. The spectral radius controls asymptotic exponential scaling, not necessarily finite-time decay. Reliable lifetime estimates require an appropriate finite-time bound.

Fifth, the proposed signature has not yet been shown to outperform established methods. The mathematical bounds follow from standard operator theory. A claim of novelty requires either a new optimality theorem, a more efficient estimator, a tighter bound under explicit data constraints, or a successful out-of-sample prediction.

Sixth, the theory is not universal across all open quantum systems. Non-Markovian evolution, infinite-dimensional systems, unbounded generators, and continuously varying coherence sectors require additional technical work. The finite-dimensional results cannot simply be transferred to those settings without proving the necessary domain and convergence conditions.

These limitations define the boundaries of the present result rather than invalidating the research program.

## 23. Research Program and Milestones

The program can be organized into six successive gates.

## 1

Operational closure

Fix the channel class, coherence projection, norm, initial-state domain, and lifetime threshold. Prove that every proposed quantity is well-defined and experimentally meaningful.

## 2

Channel-structure theorem

Establish invariant sectors, contraction coefficients, and leakage bounds. Treat non-normal dynamics explicitly.

## 3

Sufficiency and identifiability

Determine when a restricted signature is sufficient for lifetime prediction and when distinct channels remain indistinguishable.

## 4

Independent estimation

Develop calibration protocols that estimate the required signature without fitting the target lifetime.

## 5

Experimental prediction

Predict threshold crossings before measurement and compare against standard baselines using equal data budgets.

## 6

Minimality and generalization

Prove optimality where possible, extend to multiqubit and non-Markovian settings, and retain only structural terms that demonstrate independent value.

The program succeeds only if it passes all six gates. Deriving a compact descriptor is not enough; the descriptor must predict something that was not used to construct it.

## 24. Conclusion

The mathematics of coherence loss is richer than a single phenomenological decay rate. Quantum channels act on operator sectors, transform density-operator spectra, modify correlations with auxiliary systems, and preserve or break specific conservation structures. Two channels can agree on one coherence trajectory while differing sharply in their fixed points, population dynamics, entanglement behavior, or transient response.

This paper has developed a structural framework that separates these mechanisms. Its central candidate is the spectral–correlational coherence signature

\\[ \mathfrak C\_{\mathcal P}(\mathcal E) = (r\_{\mathrm c},\kappa\_{\mathrm c}, \ell\_{\mathrm c},\mathfrak S,\mathfrak K), \\]

defined relative to a specified coherence sector and operational measurement scheme. The framework yields a rigorous contraction theorem, a leakage-aware extension, a mode-resolved lifetime envelope, and a clear distinction between asymptotic spectral decay and finite-time behavior.

The most important result is conditional:

\\[ \boxed{ C\_{\mathcal P}(\rho_n) \leq \kappa\_{\mathrm c}^{\\,n} C\_{\mathcal P}(\rho_0) } \\]

for a channel that preserves the chosen coherence sector and has a restricted induced norm below unity. This gives an explicit upper bound on the number of channel applications required to reach a specified coherence threshold.

But the result is not, by itself, a new universal law of decoherence. The contraction inequality belongs to established operator theory. The proposed signature is a candidate for predictive compression, not a proven complete classification. The spectral and correlational layers must justify their inclusion by adding measurable predictive power.

The decisive research target is therefore not to find a number that merely redescribes coherence decay. It is to prove that a minimal, independently estimable set of channel-structural quantities predicts coherence lifetimes across a well-defined class of systems, with better robustness, tighter bounds, or lower measurement cost than existing methods.

If such a sufficiency and minimality theorem can be established and experimentally validated, the mathematics of coherence loss will have advanced from descriptive channel classification toward a predictive theory of coherence lifetime. Until then, the framework presented here is a rigorous research program with established conditional bounds and a clearly identified open problem.

## References

The following works provide the established mathematical and physical foundations relevant to this framework. Their inclusion does not imply that the proposed spectral–correlational signature has already been validated as a new invariant.

1\. Gorini, V., Kossakowski, A., & Sudarshan, E. C. G. (1976). Completely positive dynamical semigroups of \\(N\\)-level systems. Journal of Mathematical Physics, 17, 821–825.

2\. Lindblad, G. (1976). On the generators of quantum dynamical semigroups. Communications in Mathematical Physics, 48, 119–130.

3\. Kraus, K. (1983). States, Effects, and Operations: Fundamental Notions of Quantum Theory. Springer.

4\. Nielsen, M. A., & Chuang, I. L. (2000). Quantum Computation and Quantum Information. Cambridge University Press.

5\. Watrous, J. (2018). The Theory of Quantum Information. Cambridge University Press.

6\. Breuer, H.-P., Laine, E.-M., Piilo, J., & Vacchini, B. (2016). Colloquium: Non-Markovian dynamics in open quantum systems. Reviews of Modern Physics, 88, 021002.

7\. Baumgratz, T., Cramer, M., & Plenio, M. B. (2014). Quantifying coherence. Physical Review Letters, 113, 140401.

8\. Streltsov, A., Adesso, G., & Plenio, M. B. (2017). Colloquium: Quantum coherence as a resource. Reviews of Modern Physics, 89, 041003.

9\. Horodecki, M., & Oppenheim, J. (2013). (Quantumness in the context of) resource theories. International Journal of Modern Physics B, 27, 1345019.

10\. Uhlmann, A. (1971). Sätze über Dichtematrizen. Wissenschaftliche Zeitschrift der Karl-Marx-Universität Leipzig, 20, 633–637.

11\. Bhatia, R. (1997). Matrix Analysis. Springer.

12\. Wolf, M. M. (2012). Quantum Channels & Operations: A Guided Tour. Lecture notes.

13\. Fagnola, F., & Rebolledo, R. (2001). Subharmonic projections for a quantum Markov semigroup. Journal of Mathematical Physics, 42, 1296–1308.

14\. Choi, M.-D. (1975). Completely positive linear maps on complex matrices. Linear Algebra and its Applications, 10, 285–290.

15\. Rivas, Á., Huelga, S. F., & Plenio, M. B. (2014). Quantum non-Markovianity: Characterization, quantification and detection. Reports on Progress in Physics, 77, 094001.

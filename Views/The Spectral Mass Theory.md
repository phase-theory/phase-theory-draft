# The Spectral Mass Theory

## Deriving Particle Masses from Fundamental Spectral Gaps: Operator Construction, Relativistic Consistency, and Standard-Model Tests

Research preprint · October 25, 2026

### Abstract

The Spectral Mass Theory (SMT) investigates whether the masses of elementary particles can be derived as spectral gaps of a more fundamental dynamical operator, rather than introduced as independent parameters of an effective field theory. Its central hypothesis is that particle mass may encode the excitation spectrum of an underlying operator whose structure is fixed by deeper dynamics, symmetry, and consistency conditions.

A candidate relation is

\\[ m_n^2=\frac{\lambda_n-\lambda_0}{\ell^2}, \\]

where \\(\lambda_n\\) are dimensionless eigenvalues of a specified operator, \\(\lambda_0\\) is a reference eigenvalue, and \\(\ell\\) is a physical length scale. Although dimensionally consistent, this relation has physical content only if the operator, its domain, its symmetries, the reference state, and the scale \\(\ell\\) are independently derived. Otherwise, it is a parametrization capable of reproducing arbitrary masses without explaining them.

This paper develops a rigorous framework for the hypothesis. It distinguishes eigenvalue gaps from singular-value gaps, spectral parameters from physical masses, and a genuine dynamical derivation from a post hoc fit. It establishes the conditions under which spectral data can determine relativistic mass poles, formulates a conditional spectral-mass theorem, and derives necessary tests for Lorentz invariance, stability, degeneracy, radiative corrections, and empirical identifiability. It also examines the decisive obstacle: the Standard Model already contains a rich and experimentally constrained mass-generation structure, including Yukawa couplings, electroweak symmetry breaking, and quantum corrections. A new spectral theory must reproduce these results or derive a demonstrably superior explanation without simply relocating their free parameters into an unspecified operator.

The paper proposes a staged program: define the fundamental operator; derive its spectrum from independently fixed dynamics; establish the map from spectral gaps to relativistic poles; recover a known particle sector without fitting every mass separately; and test the resulting predictions against independent observables. The central theorem is conditional, and no universal particle-mass operator is asserted to have been established. The intended result is a mathematically auditable route from fundamental dynamics to measurable mass spectra.

Keywords: particle masses; spectral theory; eigenvalue gaps; relativistic quantum field theory; mass operators; Standard Model; spectral geometry; effective field theory; inverse spectral problems; radiative stability.

## 1. Introduction: Are particle masses spectral observables?

Particle masses occupy a distinctive position in fundamental physics. They are among the most directly measurable properties of elementary excitations, yet the numerical values of the fermion masses and many parameters controlling the spectrum are not predicted by the Standard Model from first principles.

The Higgs mechanism explains how elementary fermion masses arise within the electroweak theory once Yukawa couplings are specified. Schematically,

\\[ m_f=\frac{y_f v}{\sqrt{2}}, \\]

where \\(y_f\\) is the fermion's Yukawa coupling and \\(v\\) is the Higgs vacuum expectation value, with convention-dependent renormalization-scale qualifications. This relation explains the mechanism of mass generation, but it does not derive the full observed hierarchy of Yukawa couplings.

Spectral Mass Theory asks whether a deeper dynamical structure could determine these values.

Its hypothesis is that particle masses are not arbitrary labels attached to fields, but encode differences between allowed spectral levels of an underlying operator. The operator could, in principle, arise from geometry, an internal dynamical space, a field-theoretic stability operator, a compactification, a bound-state equation, or another independently defined structure.

The broad mathematical idea is not new in isolation. Kaluza–Klein theories generate mass towers from eigenvalues of internal differential operators; hadron masses emerge from spectral problems in quantum chromodynamics; and quantum field theories describe physical particles through poles of two-point functions. The research challenge is therefore not to notice that spectra can contain masses. It is to derive an operator that explains a specified particle spectrum with fewer independent assumptions than the theory it seeks to improve.

### 1.1 The central hypothesis

Let \\(\mathcal H\\) be a Hilbert space associated with a fundamental dynamical system, and let

\\[ \mathcal L:\mathcal D(\mathcal L)\subset\mathcal H \longrightarrow\mathcal H \\]

be a specified operator with a suitable spectral realization.

Suppose, for an appropriate sector, that its eigenvalues satisfy

\\[ \lambda_0\le\lambda_1\le\lambda_2\le\cdots. \\]

A candidate mass law is

\\[ \boxed{ m_n^2=\frac{\lambda_n-\lambda_0}{\ell^2} } \\]

with \\(\ell\\) a reference length.

This equation is a hypothesis, not a derivation. To make it physically meaningful, the theory must establish at least five claims:

1. \\(\mathcal L\\) is derived from an independently motivated dynamical principle.
2. Its spectral values are defined with a fixed normalization and domain.
3. The reference level \\(\lambda_0\\) has a physical interpretation.
4. The relation between the eigenvalue gaps and relativistic mass poles follows from the dynamics.
5. The predicted spectrum matches observations without assigning one adjustable parameter to each measured mass.

The fifth requirement is the discriminating one. Almost any finite collection of positive masses can be reproduced by constructing an operator with a chosen spectrum. Such a construction is an inverse-fitting exercise, not an explanation of mass.

### 1.2 The target result

The principal target is a theorem of the form

\\[ \operatorname{Spec}(\mathcal L) \quad\Longrightarrow\quad \\{m_1,m_2,\ldots,m_N\\}, \\]

where the operator is derived before the particle masses are inserted and where the resulting spectrum predicts measured pole masses or mass ratios.

A stronger result would predict at least one mass, degeneracy, mass ratio, or additional state not used in constructing the operator. The prediction must survive independent checks of normalization, renormalization, and uncertainty.

### 1.3 Scope and epistemic status

This paper develops a candidate mathematical architecture. It distinguishes established results from conditional theorems and research conjectures. It does not claim that all elementary-particle masses are already known to arise from one universal spectral operator.

The theory is successful only if its operator construction produces nontrivial, independently testable consequences.

## 2. Dimensional foundations and the meaning of a spectral gap

The candidate law

\\[ m_n^2=\frac{\lambda_n-\lambda_0}{\ell^2} \\]

is dimensionally consistent only under a particular convention: \\(\lambda_n\\) must be dimensionless and \\(\ell\\) must have units of inverse mass in natural units, or units of length when \\(\hbar\\) and \\(c\\) are restored.

In natural units, \\(\hbar=c=1\\),

\\[ [m_n]=L^{-1},\qquad [m_n^2]=L^{-2},\qquad [\ell]=L. \\]

Thus,

\\[ \left[\frac{\lambda_n-\lambda_0}{\ell^2}\right] =L^{-2} \\]

when \\(\lambda_n\\) is dimensionless.

Restoring units, if \\(m_n\\) denotes mass rather than energy, the corresponding relation is

\\[ m_n^2c^4 = \frac{\hbar^2c^2}{\ell^2} (\lambda_n-\lambda_0). \\]

Equivalently,

\\[ m_n = \frac{\hbar}{c\ell} \sqrt{\lambda_n-\lambda_0}. \\]

This equation fixes units but does not identify the operator.

### 2.1 Three distinct spectral conventions

A spectral-mass construction can take at least three forms.

Convention A: Dimensionless internal operator

\\[ \mathcal L u_n=\lambda_n u_n, \qquad [\lambda_n]=1. \\]

Masses are generated by dividing dimensionless gaps by a reference length squared.

Convention B: Dimensionful operator

\\[ \mathcal A u_n=\mu_n^2u_n, \qquad [\mu_n^2]=L^{-2}. \\]

In this case, the mass relation may simply be

\\[ m_n^2=\mu_n^2-\mu_0^2. \\]

The reference length is already absorbed into \\(\mathcal A\\), so inserting another \\(\ell^{-2}\\) would double-count the scale.

Convention C: Generalized eigenvalue problem

\\[ \mathcal A u_n=\lambda_n\mathcal B u_n, \\]

where \\(\mathcal A\\) and \\(\mathcal B\\) may carry different units and \\(\mathcal B\\) defines the relevant inner product or kinetic normalization. The physical interpretation then depends on the quadratic form and normalization, not on the eigenvalue equation alone.

The theory must select one convention at the outset. Changing conventions after seeing the data can disguise additional free parameters.

### 2.2 Why the reference eigenvalue is not innocuous

Subtracting \\(\lambda_0\\) guarantees that the lowest state in the selected sector has zero mass under the proposed relation. That is not automatically physically appropriate.

For a sector containing a massless mode, this may be natural. For a sector whose lightest particle is massive, the reference level must either be associated with a separate vacuum or background contribution, or the relation must be modified.

A more general affine spectral law is

\\[ m_n^2=a\lambda_n+b, \\]

with \\(a\\) carrying the required units and \\(b\\) an additive mass-squared offset. The gap formula is the special case \\(a=\ell^{-2}\\) and \\(b=-\lambda_0\ell^{-2}\\).

Allowing both \\(a\\) and \\(b\\) can improve a fit, but it also weakens predictive power. The reference state and offset should therefore follow from the dynamics, not be chosen independently for each particle family.

## 3. The correct physical object: a relativistic mass pole

A spectral eigenvalue is not a particle mass merely because it has units of mass squared. The physical meaning of mass in relativistic quantum field theory is tied to the representation of the Poincaré group and, operationally, to the invariant-mass spectrum and pole structure of correlation functions.

For a stable particle of mass \\(m\\), the one-particle states satisfy

\\[ p^\mu p\_\mu=-m^2 \\]

under the mostly-plus metric convention, or \\(p^2=m^2\\) under the mostly-minus convention. The physical statement is convention-independent: the mass is the positive square root of the particle's invariant mass squared.

For an interacting scalar field, the exact two-point function admits a Källén–Lehmann spectral representation under the usual assumptions of relativistic quantum field theory. Its spectral measure can contain isolated one-particle contributions and a multiparticle continuum.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://qft.org\&sz=32)

QFT .org

+1



Schematically, in a mostly-minus convention,

\\[ \widetilde G_F(p) = i\int_0^\infty \frac{\rho(s)}{p^2-s+i0}\\,ds, \\]

with the understanding that the integral may require distributional interpretation or subtractions in particular theories. An isolated stable particle produces a delta-function contribution to \\(\rho(s)\\) at \\(s=m^2\\); the continuum records additional states accessible to the chosen field operator.

This gives SMT a more rigorous target than a numerical mass table: derive the locations of physical poles or isolated spectral atoms from the eigenvalues of a fundamental operator.

### 3.1 The mass operator

In a positive-metric physical Hilbert space carrying a unitary representation of the Poincaré group, the Casimir operator \\(P\_\mu P^\mu\\) determines invariant mass, with the sign depending on metric convention. In a mostly-minus convention,

\\[ \widehat M^2=\widehat P\_\mu\widehat P^\mu. \\]

This is already a mass-squared operator in a precise representation-theoretic sense. However, it does not by itself explain why a given theory has the observed masses: it classifies the irreducible components of the physical state space.

SMT therefore needs a deeper operator \\(\mathcal L\\) whose spectral data derive the eigenvalues of the physical mass operator or the poles of the propagator. It cannot simply rename \\(\widehat M^2\\) as the fundamental spectral operator.

### 3.2 Three levels of mass prediction

The theory should distinguish:

1. Kinematic identification: a spectral value equals an already-known mass eigenvalue.
2. Dynamical derivation: a fundamental operator's spectrum determines the mass eigenvalue.
3. Predictive explanation: the operator, its scale, and its parameters are independently fixed and predict masses or relations not used in its construction.

Only the second and third levels address the central research question, and the third is the decisive test.

## 4. Candidate operator classes

No single operator class is mandated by the spectral-mass hypothesis. Different constructions imply different physical commitments. A viable theory must choose one and derive it.

### 4.1 Internal elliptic operators

Let \\(K\\) be a compact Riemannian internal space, and let \\(\mathcal L_K\\) be a positive self-adjoint elliptic operator on an appropriate bundle over \\(K\\):

\\[ \mathcal L_K u_n=\lambda_nu_n. \\]

Compactness and ellipticity provide a discrete spectrum under standard conditions. If the higher-dimensional field is expanded in eigenmodes \\(u_n\\), the lower-dimensional effective theory can acquire a tower of masses proportional to the internal eigenvalues.

For example, a scalar field on a product spacetime \\(M^{d}\times K\\) may be expanded as

\\[ \Phi(x,y)=\sum_n\phi_n(x)u_n(y). \\]

Under suitable product-metric and operator assumptions, separation of variables gives effective lower-dimensional equations of the form

\\[ \left(\Box\_{M}-\mu_n^2\right)\phi_n=0, \\]

with

\\[ \mu_n^2=\mu\_{\mathrm{bulk}}^2+\lambda_n, \\]

up to the chosen sign and normalization conventions.

This is a genuine mechanism: an internal spectral problem can generate lower-dimensional mass parameters. It is not yet a derivation of the observed Standard-Model spectrum. That requires deriving the internal geometry, the relevant bundles and representations, the operator's coefficients, and the map from eigenmodes to observed particles.

### 4.2 Stability or Hessian operators

Suppose a fundamental field configuration \\(\Phi_0\\) extremizes an action \\(S[\Phi]\\). Its second variation defines a fluctuation operator schematically given by

\\[ \mathcal H\_{\Phi_0} = \left. \frac{\delta^2 S}{\delta\Phi\\,\delta\Phi} \right|\_{\Phi=\Phi_0}. \\]

The eigenvalues of this operator characterize linearized fluctuation modes. Depending on the kinetic terms and conventions, they may encode squared frequencies, instability rates, or effective mass-squared parameters.

This route is attractive if the fundamental configuration is independently derived and the Hessian is positive on the physical fluctuation sector. It is dangerous if negative modes are ignored or if gauge zero modes are mistaken for physical particles.

A stability operator yields a mass spectrum only after its kinetic normalization, gauge constraints, and relativistic dispersion relation are established.

### 4.3 Dirac-type operators

For fermions, a natural starting point is a self-adjoint or appropriately defined Dirac-type operator \\(\mathcal D\\). If

\\[ \mathcal D u_n=\nu_nu_n, \\]

then \\(\mathcal D^2\\) has eigenvalues \\(\nu_n^2\\) under suitable domain and self-adjointness assumptions.

A candidate mass relation might be

\\[ m_n^2=\frac{\nu_n^2-\nu_0^2}{\ell^2}. \\]

But a Dirac eigenvalue is not automatically a fermion mass. Chirality, gauge representation, degeneracy, and the form of the lower-dimensional kinetic term must all be included. The spectrum must also be compatible with the observed pattern of chiral fermions and their interactions.

### 4.4 Integral and nonlocal operators

The underlying dynamics need not be local at the fundamental level. A self-adjoint integral operator with kernel \\(K(x,y)\\), for example, may have a discrete spectrum if it is compact on the relevant Hilbert space.

However, an arbitrary kernel can be constructed to reproduce almost any desired finite spectrum. The physical challenge is to derive \\(K(x,y)\\) from an independent action, symmetry, or consistency principle and to establish the correct relativistic limit.

The operator's mathematical flexibility is not evidence for its physical validity.

### 4.5 Comparative assessment

| Operator class             | Potential strength                      | Principal burden                                                                   |
| -------------------------- | --------------------------------------- | ---------------------------------------------------------------------------------- |
| Internal elliptic operator | Naturally discrete mass towers          | Derive internal space and field content                                            |
| Stability/Hessian operator | Connects masses to fundamental dynamics | Separate physical modes from gauge and instability modes                           |
| Dirac-type operator        | Natural for fermionic sectors           | Recover chirality, representations, and mass couplings                             |
| Integral/nonlocal operator | Broad dynamical flexibility             | Prevent arbitrary kernel fitting; establish causality and relativistic consistency |

SMT should not combine these possibilities into one undefined operator. A concrete realization must choose a class, define its domain and symmetries, and derive the mass map.

## 5. Spectral Mass Theory as a variational and inverse problem

A fundamental operator should emerge from a mathematical structure that precedes the particle-mass data. One disciplined route is to define a dynamical functional and derive the operator from its second variation or from a constrained eigenvalue problem.

Let \\(\Phi\\) denote the fundamental fields, \\(X\\) the underlying configuration space, and \\(\theta\\) the finite set of independently motivated model parameters. Consider an action

\\[ S[\Phi;X,\theta]. \\]

A background solution \\(\Phi_0\\) satisfies

\\[ \left.\frac{\delta S}{\delta\Phi}\right|\_{\Phi_0}=0. \\]

Writing \\(\Phi=\Phi_0+\epsilon\eta\\), the quadratic action is

\\[ S[\Phi_0+\epsilon\eta] = S[\Phi_0] +\frac{\epsilon^2}{2} \langle\eta,\mathcal H\_{\Phi_0}\eta\rangle +O(\epsilon^3), \\]

where \\(\mathcal H\_{\Phi_0}\\) is the Hessian or fluctuation operator after the relevant boundary terms and constraints have been treated consistently.

If the quadratic kinetic term is governed by a positive operator \\(\mathcal K\\) on the physical fluctuation sector, the linearized equations may take the generalized eigenvalue form

\\[ \mathcal H\_{\Phi_0}u_n = m_n^2\\,\mathcal K u_n. \\]

This is potentially a physical mass eigenvalue problem because it is derived from the quadratic dynamics. Yet it still does not guarantee that \\(m_n\\) equals an observed particle mass. That identification requires showing that the modes transform in the correct relativistic and gauge representations and that their propagators have poles at the corresponding masses.

### 5.1 The operator must precede the fit

The derivation must fix, before mass-spectrum comparison:

- the underlying configuration space and measure;
- the action or dynamical functional;
- the physical domain and boundary conditions;
- gauge constraints and removal of redundant modes;
- the kinetic inner product;
- the reference vacuum or background;
- the dimensional scale;
- the renormalization prescription, where relevant.

If these ingredients are chosen to reproduce each mass individually, the result is a reparameterization of the data. The inverse problem becomes explanatory only when the admissible operators are constrained independently and the measured masses select among a limited number of genuine predictions.

### 5.2 Why the inverse problem is underdetermined

Suppose the observed squared masses in a finite sector are \\(m_1^2,\ldots,m_N^2\\). One can define an \\(N\\)-dimensional Hilbert space and the diagonal matrix

\\[ \mathcal L = \ell^2\operatorname{diag} (m_1^2,\ldots,m_N^2)+\lambda_0 I. \\]

Its eigenvalues reproduce the desired masses by construction. But this operator contains the data it purports to explain.

The example demonstrates a general inverse-spectral obstruction: matching eigenvalues does not uniquely determine an operator, and a constructed operator need not have an independent physical interpretation.

A successful SMT model must therefore restrict the operator class through symmetries, locality or a justified nonlocality, a dynamical action, and independently specified parameters.

## 6. Relativistic consistency and the mass-pole theorem

The next question is how an internal or fundamental eigenvalue becomes a relativistic mass.

Consider a set of physical modes \\(\phi_n(x)\\) in a \\(d\\)-dimensional Lorentzian spacetime. Suppose a reduction or linearization yields the quadratic action

\\[ S^{(2)} = -\frac12\sum_n \int d^dx \left[ Z_n\\,\partial\_\mu\phi_n\partial^\mu\phi_n + Z_n\\,m_n^2\phi_n^2 \right], \\]

with sign conventions adjusted to the chosen metric signature, \\(Z_n>0\\), and with no kinetic mixing after diagonalization. Canonical normalization is obtained by rescaling \\(\phi_n\\).

The corresponding free propagator has a pole at the invariant mass \\(m_n\\). Thus, the spectral-to-mass map is justified if the operator eigenvalue appears in the quadratic action as the coefficient of the mode's mass term, relative to its kinetic normalization.

### Theorem 6.1 — Conditional spectral-to-pole correspondence

Let \\(\mathcal H\_{\mathrm{phys}}\\) be a physical fluctuation Hilbert space. Suppose:

1. A self-adjoint operator \\(\mathcal L\\) is derived from the quadratic dynamics on a specified physical domain.
2. Its relevant spectrum is discrete, with orthonormal eigenmodes \\(u_n\\) and eigenvalues \\(\lambda_n\\).
3. The quadratic action separates into modes \\(u_n\\), with positive kinetic coefficients \\(Z_n\\).
4. The coefficient of the \\(n\\)-th mode's mass term is \\(Z_n(\lambda_n-\lambda_0)/\ell^2\\), where \\(\ell\\) and \\(\lambda_0\\) are independently fixed.
5. The linearized theory is Lorentz invariant in the observed spacetime dimensions, and no additional mass mixing remains.

Then the canonically normalized mode \\(\phi_n\\) has a free propagator with a pole at

\\[ \boxed{ p^2=m_n^2 = \frac{\lambda_n-\lambda_0}{\ell^2} } \\]

in a mostly-minus convention.

#### Proof

Expand the physical fluctuation field in the eigenbasis of \\(\mathcal L\\). By assumptions 3 and 4, the quadratic action separates into independent modes whose kinetic and mass terms share the positive factor \\(Z_n\\). Rescaling each mode by \\(\phi_n\mapsto Z_n^{-1/2}\phi_n\\) produces a canonically normalized quadratic action. Its inverse kinetic operator has denominator \\(p^2-(\lambda_n-\lambda_0)/\ell^2+i0\\), so the pole occurs at the stated invariant mass squared. \\(\square\\)

### 6.1 What the theorem does not prove

The theorem establishes a conditional correspondence between eigenvalues and propagator poles. It does not derive the operator, the eigenvalues, or the scale. Those are precisely the unresolved parts of SMT.

Assumption 4 is especially important. If the desired mass law is simply inserted into the quadratic action, the theorem only confirms the definition. A substantive derivation must obtain the mass coefficient from the fundamental action or a controlled reduction.

The theorem also applies directly to stable free modes or the quadratic approximation. In an interacting theory, a physical mass should be identified with an appropriate pole or spectral threshold of the full renormalized correlation function. Unstable particles may correspond to complex poles or resonant structures rather than isolated real-axis poles.

## 7. The Standard Model as a non-negotiable benchmark

A proposed mass theory must reproduce the experimentally established particle spectrum and its associated interactions, not merely a list of numbers.

The Standard Model's electroweak sector generates fermion masses through Yukawa matrices and the Higgs vacuum expectation value. For each fermion species,

\\[ M_f=\frac{v}{\sqrt2}Y_f, \\]

where \\(Y_f\\) is the Yukawa matrix and \\(v\\) is the electroweak vacuum expectation value. Diagonalization produces the fermion mass eigenvalues, while the mismatch between the left-handed rotations of the up- and down-type quarks gives the CKM mixing matrix.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://qft.org\&sz=32)

QFT .org

+2



This framework makes specific predictions about Higgs couplings, gauge interactions, and flavor structure. A spectral explanation that reproduces the masses but fails to reproduce these associated relationships is incomplete.

### 7.1 What must be derived?

For a fermion sector, SMT should ideally derive the Yukawa matrix or its physical singular values from the fundamental operator. It must also explain how the resulting eigenmodes transform under

\\[ SU(3)\_C\times SU(2)\_L\times U(1)\_Y \\]

and why the observed chirality structure arises.

For gauge bosons, the theory must recover the relation between electroweak symmetry breaking and the \\(W\\) and \\(Z\\) masses, including the corresponding gauge couplings and mixing parameters.

For the Higgs boson, it must recover the scalar excitation spectrum and its couplings. For neutrinos, it must accommodate the observed flavor mixing and the possibility of mass-generation mechanisms beyond the minimal Dirac-Yukawa construction.

The measured particle data and their uncertainties must be taken from a declared data release and scheme. The Particle Data Group's particle listings provide a standard starting point for the established spectrum.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pdgweb.lbl.gov\&sz=32)

Particle Data Group



### 7.2 A mass-only fit is not enough

Suppose an operator reproduces the six quark masses but does not derive the CKM angles or CP-violating phase. It has explained only a subset of the flavor structure.

Similarly, reproducing charged-lepton masses without predicting their Higgs couplings adds little if the model has simply encoded the corresponding Yukawa values in its coefficients.

The strongest SMT target is therefore a joint spectral structure: a single independently specified operator or a tightly constrained operator family should yield mass eigenvalues, degeneracies, selection rules, and relevant mixing information.

## 8. Flavor as a matrix spectral problem

The scalar formula \\(m_n^2=(\lambda_n-\lambda_0)/\ell^2\\) is most natural for a sequence of modes. The Standard Model's flavor sectors require a matrix generalization.

Let \\(\mathcal Y_f\\) be an effective mass-generating operator for a fermion species \\(f\\), mapping right-handed flavor space into left-handed flavor space. The physical masses are its singular values:

\\[ \mathcal Y_f^\dagger\mathcal Y_f\\,v_i = m\_{f_i}^2v_i. \\]

If SMT is to explain the spectrum, it must derive \\(\mathcal Y_f\\) or an equivalent operator from the underlying dynamics. Merely specifying a Hermitian matrix with eigenvalues equal to the observed squared masses repeats the inverse-fitting problem.

A stronger construction would yield a relation such as

\\[ \mathcal Y_f = \frac{1}{\ell}\\, \mathcal F_f(\mathcal L,\mathcal G,\theta), \\]

where \\(\mathcal G\\) denotes independently derived gauge or geometric structure, and \\(\theta\\) is a small set of independently constrained parameters. The singular values of \\(\mathcal Y_f\\) would then determine the masses.

### 8.1 Mixing angles are additional spectral data

Mass eigenvalues alone do not determine the mixing matrix. If two flavor sectors are described by different mass operators, the relative eigenvectors determine mixing.

For quarks, if \\(U\_{uL}\\) and \\(U\_{dL}\\) diagonalize the corresponding left-handed mass structures, then

\\[ V\_{\mathrm{CKM}}=U\_{uL}^\dagger U\_{dL}. \\]

A spectral mass theory that predicts only eigenvalues but leaves the eigenvectors unconstrained cannot claim to have derived the full flavor sector.

### 8.2 Degeneracy and selection rules

An underlying symmetry may force eigenvalue degeneracies. Breaking that symmetry may split them. This suggests a possible explanatory mechanism for mass patterns, but the symmetry and breaking operator must be derived independently.

A successful model should predict which degeneracies are exact, which are approximate, and which are lifted by specified interactions. These predictions can be tested independently of the overall mass scale.

## 9. Spectral gaps, absolute masses, and mass ratios

The reference-gap relation naturally predicts squared-mass differences:

\\[ m_n^2-m_k^2 = \frac{\lambda_n-\lambda_k}{\ell^2}. \\]

If \\(\ell\\) is fixed independently, this determines the scale of the mass-squared differences. If \\(\ell\\) is not fixed, the spectrum predicts only ratios of gaps.

For a reference level \\(\lambda_0\\),

\\[ \frac{m_n^2}{m_k^2} = \frac{\lambda_n-\lambda_0} {\lambda_k-\lambda_0}, \\]

provided the denominator is nonzero and the same scale and offset apply to both modes.

This is an important distinction. A model might predict a hierarchy or a set of mass ratios without predicting the absolute mass scale. That can still be useful, but it should be stated as the actual prediction.

### 9.1 A scale-free test

Define

\\[ R\_{nk} = \frac{m_n^2-m_0^2}{m_k^2-m_0^2} = \frac{\lambda_n-\lambda_0}{\lambda_k-\lambda_0}. \\]

If the operator predicts the right-hand side independently, then the measured ratios provide a direct test that does not require prior knowledge of \\(\ell\\).

However, if \\(\lambda_n\\) are themselves fitted to the observed masses, the relation is tautological. A valid prediction requires the operator spectrum to be computed or derived before the comparison.

### 9.2 A danger of choosing the reference state

Different particle families may have different ground states, symmetries, or effective operators. Subtracting one universal \\(\lambda_0\\) across sectors may be unjustified.

If each sector receives its own reference eigenvalue, the theory acquires additional structure and possibly additional parameters. That may be physically legitimate, but the number of independent offsets must be counted as part of the model's complexity.

## 10. Radiative corrections and renormalization

The masses reported in particle tables do not all have the same operational meaning. Stable-particle masses, resonance pole masses, and scheme-dependent running masses are distinct quantities.

Quark masses, in particular, are conventionally reported in renormalization schemes such as \\(\overline{\mathrm{MS}}\\), with a scale dependence governed by renormalization-group equations. The pole-mass concept for quarks also has subtleties associated with confinement and infrared sensitivity. A spectral operator that claims to reproduce quark masses must specify which mass definition it predicts.

Let \\(\mathcal L(\mu)\\) be an effective operator defined at renormalization scale \\(\mu\\). A candidate law may take the form

\\[ m_n^2(\mu) = \frac{\lambda_n(\mu)-\lambda_0(\mu)} {\ell^2(\mu)}. \\]

The scale dependence of the right-hand side must match the known running of the physical parameters. It is not enough to fit the masses at one arbitrary scale.

### 10.1 Spectral flow

If the operator depends smoothly on a coupling \\(g(\mu)\\), its eigenvalues can vary with the coupling. For a simple isolated eigenvalue of a differentiable self-adjoint operator, the Hellmann–Feynman relation gives, schematically,

\\[ \frac{d\lambda_n}{dg} = \left\langle u_n, \frac{d\mathcal L}{dg}u_n \right\rangle, \\]

under the usual domain and differentiability conditions.

This formula could provide a bridge between operator dynamics and mass running, but only if the operator's coupling dependence is independently derived. The beta functions of the underlying theory must be consistent with the observed renormalization-group flow.

### 10.2 Radiative stability

A proposed mass hierarchy is physically compelling only if it survives quantum corrections or explains how those corrections are controlled.

If a small mass is generated by the difference of two large spectral quantities,

\\[ m_n^2 = \ell^{-2}(\lambda_n-\lambda_0), \\]

then radiative corrections may destabilize the difference unless a symmetry or structural mechanism protects it. SMT should identify whether the hierarchy is symmetry-protected, dynamically selected, or simply tuned.

This requirement is particularly important for any model that attempts to explain large ratios between particle masses using small spectral gaps.

## 11. Positivity, stability, and tachyonic modes

The gap formula imposes a nontrivial constraint:

\\[ \lambda_n-\lambda_0\ge0 \\]

if \\(\lambda_0\\) is the lowest eigenvalue of a self-adjoint operator bounded below. Under the proposed mass relation, this guarantees \\(m_n^2\ge0\\).

But the interpretation of a negative eigenvalue depends on the operator. In a fluctuation Hessian, a negative physical mass-squared mode may signal instability of the assumed background. In a gauge theory, an apparent negative mode may be an artifact of an incorrect treatment of constraints. In a symmetry-breaking theory, a negative quadratic coefficient can indicate that the chosen configuration is not the true vacuum.

SMT must not automatically discard every negative eigenvalue or declare every nonnegative spectrum physically stable.

### 11.1 Physical-sector positivity

Let \\(\mathcal H\_{\mathrm{phys}}\\) be the physical fluctuation space after gauge constraints and redundant directions have been removed. A stable background should have a nonnegative quadratic form on this space, apart from genuine zero modes:

\\[ \langle u,\mathcal H\_{\Phi_0}u\rangle\ge0 \qquad \forall u\in\mathcal D\_{\mathrm{phys}}. \\]

The zero modes require classification. They may represent gauge redundancy, a symmetry-generated collective coordinate, a true massless particle, or a flat direction lifted by quantum corrections.

A credible mass derivation must distinguish these possibilities.

### 11.2 The reference mode as a physical question

If \\(\lambda_0\\) is subtracted to make the lightest mode massless, the model predicts a massless excitation unless the physical interpretation of the reference state is different from an observable particle mode.

A universal gap formula cannot simultaneously make every sector's ground state massless and reproduce sectors whose lightest states are massive without additional offsets, constraints, or a different reference prescription.

That is a structural issue, not a matter of choosing convenient units.

## 12. A conditional operator-construction theorem

The mass-pole theorem established how a specified quadratic action converts spectral coefficients into masses. We now state a second result that identifies what is required for the operator to count as a dynamical derivation.

### Definition 12.1 — Independently specified spectral model

A spectral mass model is a tuple

\\[ \mathfrak M= (\mathcal H,\mathcal D,\mathcal L, \mathcal K,\mathcal G,\ell,\mathcal P), \\]

where:

- \\(\mathcal H\\) is the physical fluctuation space;
- \\(\mathcal D\\) is the operator domain;
- \\(\mathcal L\\) is the derived spectral operator;
- \\(\mathcal K\\) is the kinetic normalization operator;
- \\(\mathcal G\\) represents the required gauge and symmetry data;
- \\(\ell\\) is an independently fixed physical scale;
- \\(\mathcal P\\) is the prescription mapping eigenmodes to observable particle channels.

The tuple is independently specified if its definition does not use the target masses as input, except through explicitly declared calibration data that are excluded from the model's claimed predictions.

### Theorem 12.1 — Conditional spectral prediction

Suppose a spectral mass model \\(\mathfrak M\\) satisfies:

1. \\(\mathcal L\\) is self-adjoint and bounded below on the physical domain.
2. Its relevant eigenvalues and eigenmodes are uniquely determined by the independently specified dynamics and boundary conditions, up to the declared degeneracies.
3. The quadratic action has a positive kinetic form and reduces to a diagonal mode expansion.
4. The coefficient of each mode's canonically normalized mass term is \\((\lambda_n-\lambda_0)/\ell^2\\).
5. The mode-to-particle map \\(\mathcal P\\) identifies the correct relativistic and internal-symmetry representations.
6. The resulting propagators have stable poles, or appropriately defined resonance poles, at the predicted masses.

Then the model predicts the corresponding mass spectrum

\\[ m_n^2=\frac{\lambda_n-\lambda_0}{\ell^2} \\]

without independently assigning each \\(m_n\\).

#### Proof

By assumptions 1 and 2, the spectral data are well-defined and fixed by the model. Assumptions 3 and 4 place the spectral gaps in the canonically normalized quadratic mass terms. Assumption 5 identifies the resulting modes with the intended physical channels, while assumption 6 establishes that their pole locations are the relevant observables. The mass relation follows for each identified mode. \\(\square\\)

### 12.1 Significance and limitations

The theorem makes the explanatory burden explicit. It is conditional, not a proof that a suitable operator exists for the Standard Model. In particular, assumptions 2, 4, and 5 contain most of the hard physics.

A model that meets these assumptions and predicts the observed masses from independently fixed data would establish a substantive spectral explanation. A model that merely defines \\(\mathcal L\\) from the desired mass values would not satisfy the independence condition.

## 13. The parameter-counting criterion

A central danger in spectral theories is moving free parameters from an explicit mass table into the coefficients of an operator.

Suppose a model uses \\(N\\) measured masses and introduces \\(N\\) independent parameters \\(\theta_i\\) that determine the eigenvalues. Even if it writes the result as

\\[ m_i^2=\frac{\lambda_i(\theta_1,\ldots,\theta_N)-\lambda_0}{\ell^2}, \\]

it has not reduced the predictive freedom.

The relevant comparison is not the number of symbols in the final formula. It is the number of independent physical inputs required to produce the predictions.

### 13.1 Predictive compression

Let \\(D\\) denote the calibration data and \\(P\\) the predictions withheld from calibration. A meaningful spectral model should satisfy three conditions:

1. Its operator family is restricted by independent theoretical principles.
2. Its parameters are fixed by a calibration subset \\(D\_{\mathrm{cal}}\\), not by the full target spectrum.
3. Its predictions for \\(P\\) agree with independent measurements within stated uncertainties.

A useful scorecard includes:

- the number of free parameters;
- the number of independently predicted observables;
- uncertainty propagation from operator parameters to eigenvalues;
- sensitivity to the assumed geometry and boundary conditions;
- and robustness under reasonable changes in the model's regularization or approximation scheme.

A parameter-count reduction is evidence of explanatory compression, but it is not sufficient. A compact model can still be wrong.

### 13.2 An out-of-sample requirement

The strongest simple test is to derive the operator using a limited subset of the spectrum, then predict withheld masses or mass ratios. If every particle mass is used to adjust the operator before the test, the result is a fit, regardless of how elegant the final eigenvalue formula looks.

## 14. A proposed spectral mechanism for a particle hierarchy

The following is a candidate research architecture, not an established model.

Suppose the fundamental dynamics yield a positive self-adjoint operator

\\[ \mathcal L(\theta) = \mathcal L_0+\mathcal V(\theta), \\]

where \\(\mathcal L_0\\) is fixed by a base geometry or symmetry and \\(\mathcal V\\) is a restricted perturbation derived from a small number of independent couplings.

If the unperturbed spectrum contains a degeneracy, a symmetry-breaking perturbation can split it. For a nondegenerate normalized eigenmode \\(u_n\\), first-order perturbation theory gives

\\[ \delta\lambda_n = \langle u_n,\mathcal V u_n\rangle. \\]

For a degenerate eigenspace, the perturbation must first be diagonalized within that subspace.

The mass shifts would then satisfy

\\[ \delta m_n^2 = \frac{\delta\lambda_n-\delta\lambda_0}{\ell^2}, \\]

if \\(\ell\\) is fixed and the reference prescription remains unchanged.

### 14.1 What this could explain

A derived operator with symmetry-protected degeneracies and constrained symmetry-breaking terms could, in principle, explain:

- approximate mass degeneracies;
- a hierarchy of splittings;
- correlations between masses in different sectors;
- selection rules that forbid certain couplings;
- and additional states predicted by the same spectrum.

The mechanism becomes explanatory only if the perturbation \\(\mathcal V\\) is determined independently. If its matrix elements are adjusted one by one to match the mass splittings, the model simply relocates the original parameters.

### 14.2 The role of a universal scale

If a single \\(\ell\\) controls several sectors, the theory predicts common scale relations. This is powerful but restrictive.

A model that needs separate \\(\ell_f\\) for every fermion family, separate reference levels, and independent corrections for each eigenmode may remain mathematically valid, but its claimed universality weakens. Each additional scale or correction must be justified by an independently derived physical distinction.

## 15. Connection to spectral geometry and inverse problems

Spectral geometry demonstrates that differential operators can encode geometric information. For example, the eigenvalues of a Laplace-type operator on a compact Riemannian manifold are constrained by the manifold's volume, curvature, topology, and other geometric features.

However, the inverse spectral problem is not generally unique: spectral data of one operator need not determine the geometry completely. Distinct spaces can share the same spectrum under suitable constructions, and different operator choices encode different geometric information.

For SMT, this creates two distinct questions:

1. Can a fundamental geometry or dynamical structure derive the operator?
2. Does that operator's spectrum determine the observed particle masses uniquely enough to be predictive?

The first is a forward problem. The second is an inverse problem. Neither follows automatically from the other.

### 15.1 A spectral identifiability condition

Let \\(\Theta\\) denote the admissible parameter space and define

\\[ \mathcal S:\Theta\to\mathbb R^N, \qquad \mathcal S(\theta) = \big(m_1^2(\theta),\ldots,m_N^2(\theta)\big). \\]

Local identifiability requires that distinct nearby parameter variations produce distinguishable predictions. A common necessary test is the rank of the sensitivity matrix,

\\[ J\_{ij} = \frac{\partial m_i^2}{\partial\theta_j}. \\]

If \\(J\\) has deficient rank, some parameter combinations cannot be distinguished using the chosen masses alone. Additional observables may be needed.

This test does not establish the model's physical correctness, but it reveals whether the model can be meaningfully calibrated and whether its parameters can be inferred from the proposed data.

### 15.2 Eigenvalue crossings and particle labels

As parameters vary, eigenvalues may cross or undergo avoided crossings. An ordering by eigenvalue does not always preserve a physical particle identity. Modes must therefore be tracked using symmetry quantum numbers, overlaps, or continuity criteria rather than simply labeling the smallest eigenvalue as particle 1 and the next as particle 2.

This issue becomes critical when a theory claims that a specific spectral level corresponds to a particular quark, lepton, or boson.

## 16. Experimental and numerical validation

A serious SMT program should begin with a model class small enough to compute rigorously or numerically and with data precise enough to falsify it.

### Stage I — Operator audit

- Derive the operator from an action, symmetry principle, or independently specified dynamical law.
- State the domain, inner product, boundary conditions, and gauge constraints.
- Prove self-adjointness or identify the appropriate alternative spectral framework.
- Determine whether the relevant spectrum is discrete, continuous, or mixed.

### Stage II — Spectral computation

- Compute the spectrum analytically where possible.
- Otherwise use a convergent numerical method with controlled discretization error.
- Track eigenvalue multiplicities and eigenvectors.
- Propagate uncertainties in the operator parameters into uncertainties in the predicted masses.

### Stage III — Mass-pole verification

- Derive the effective quadratic action for the modes.
- Verify the relativistic dispersion relation.
- Establish the propagator pole or resonance interpretation.
- Compare the resulting mass definitions with the chosen experimental data scheme.

### Stage IV — Blind prediction

- Fix all permitted parameters using an explicitly declared calibration subset.
- Withhold selected masses, mass ratios, degeneracies, or mixing observables.
- Generate predictions before examining the withheld values.
- Report discrepancies, uncertainty intervals, and failed predictions without retuning the model after each failure.

### Stage V — Independent consistency

- Check gauge and Lorentz invariance.
- Check radiative stability and renormalization-group behavior.
- Verify compatibility with Higgs and gauge couplings.
- Search for additional states implied by the same operator.

A successful numerical fit is only the beginning. The central result must be robust to refinement, parameter uncertainty, and independent physical tests.

## 17. Falsifiable predictions and failure criteria

SMT must expose itself to failure. The following outcomes would count against a proposed realization.

Failure A — Spectrum requires one parameter per mass. If the operator's independent coefficients must be tuned separately to reproduce each measured mass, the model has not achieved predictive compression.

Failure B — Wrong pole structure. If the computed eigenvalues do not correspond to poles or appropriate resonances of the physical propagators, the spectral interpretation fails.

Failure C — Incorrect particle representations. If the modes have the wrong gauge charges, chirality, spin, or flavor quantum numbers, a numerical mass match does not identify the observed particles.

Failure D — Unstable hierarchy. If quantum corrections destroy the predicted mass relations without an independently derived protection mechanism, the model lacks the claimed robustness.

Failure E — Incorrect withheld predictions. If masses or mass ratios predicted from a calibration subset disagree with independent measurements beyond the combined uncertainties, the model is falsified in that sector.

Failure F — Uncontrolled operator ambiguity. If equally admissible operator choices yield incompatible predictions and no independent principle selects among them, the proposed operator has insufficient explanatory content.

Failure G — Incorrect interaction structure. If the model reproduces masses but fails established relationships involving Higgs couplings, gauge interactions, or flavor mixing, it does not reproduce the relevant Standard-Model sector.

### 17.1 A minimum acceptance standard

A proposed realization should not be described as a derived particle-mass theory until it has:

1. an independently defined dynamical operator;
2. a justified spectral-to-pole correspondence;
3. a specified scale and reference prescription;
4. a parameter count that demonstrates predictive compression;
5. at least one successful prediction not used in calibration;
6. and compatibility with the associated interactions and quantum corrections.

This standard distinguishes a physically derived spectrum from a mathematical representation of known masses.

## 18. The principal research conjectures

The following are open research directions rather than established results.

### Conjecture 18.1 — Dynamical spectral origin of a fermion hierarchy

There exists a constrained family of self-adjoint or generalized mass operators, derived from an independent symmetry and dynamical structure, whose eigenvalues or singular values reproduce a nontrivial subset of the observed fermion mass hierarchy without independent fitting of every mass.

The strongest version would also derive relevant mixing data and identify the physical origin of the operator's scale.

### Conjecture 18.2 — Spectral protection of mass ratios

A symmetry or structural constraint may enforce relations among spectral gaps that remain stable under a specified class of quantum corrections. Such a result would provide an explanation for selected mass ratios rather than merely a fit at one renormalization scale.

The conjecture requires an explicit symmetry, a renormalized operator, and a quantitative stability theorem.

### Conjecture 18.3 — Joint spectral prediction of masses and interactions

A single fundamental operator family may determine both particle masses and selected interaction parameters, such as mode couplings or mixing constraints. This would be more explanatory than reproducing masses alone because the same eigenmodes would govern multiple independently measurable phenomena.

The conjecture should be tested against Higgs couplings, flavor observables, and any additional states implied by the model.

### Candidate theorem 18.4 — Predictive spectral compression

Let \\(\mathfrak M(\theta)\\) be an independently specified dynamical model with \\(p\\) free parameters, and let \\(\mathbf m(\theta)\\) be its predicted spectrum. If the model uniquely determines \\(N\\) mass observables from \\(p\<N\\) independent inputs, has an identifiable parameter map, and correctly predicts a withheld subset with controlled uncertainty, then it provides a testable reduction in the number of independent mass inputs relative to an unconstrained \\(N\\)-mass parametrization.

This statement is a criterion for explanatory compression, not a theorem that any particular spectral model meets it. Its physical value depends on independent derivation, identifiability, and empirical success.

## 19. A compact research architecture

A. Fundamental dynamics

Action, symmetries, background, physical degrees of freedom

B. Derived operator

Domain, kinetic inner product, gauge constraints, self-adjointness

C. Spectral solution

Eigenvalues, degeneracies, eigenvectors, spectral gaps

D. Relativistic mass map

Quadratic action, canonical normalization, propagator poles

E. Empirical test

Masses, ratios, mixing, interactions, radiative stability, blind predictions

Every arrow represents a distinct proof obligation. In particular, a spectrum does not identify physical particles by itself, and a mass-pole relation does not derive the operator.

## 20. Conclusions

The Spectral Mass Theory proposes that particle masses may encode gaps in a more fundamental dynamical spectrum. This is a mathematically plausible hypothesis with established analogues in Kaluza–Klein reductions, fluctuation theory, and relativistic quantum-field spectral representations. Its significance depends on whether a new realization can derive a known particle spectrum without encoding each mass as an independent input.

The candidate formula

\\[ \boxed{ m_n^2=\frac{\lambda_n-\lambda_0}{\ell^2} } \\]

is dimensionally consistent when the eigenvalues are dimensionless and the reference length is properly defined. But dimensional consistency is the least difficult requirement.

A physically successful theory must derive the operator, its domain, the reference state, the physical scale, and the mapping from eigenmodes to particle representations. It must then establish that the spectral gaps determine the pole locations of the relevant propagators. Finally, it must reproduce not only mass values but the associated interactions and quantum corrections.

The conditional theorems in this paper establish the mathematical form of the required spectral-to-pole connection and the conditions for a genuine prediction. They do not establish that a universal operator producing the Standard-Model mass spectrum has been found.

The most promising first target is a restricted sector with a well-defined operator, a calculable spectrum, and at least one withheld observable. A successful result there would provide a concrete foundation for extending the program to the full flavor structure.

The decisive distinction is between an operator that contains the observed masses and an operator whose independently derived dynamics predict them. SMT becomes a physical theory only when that distinction is demonstrated mathematically and experimentally.

## Selected references

1\. Particle Data Group. (2024). “Review of Particle Physics.” Physical Review D, 110, 030001. Particle properties and review articles.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pdgweb.lbl.gov\&sz=32)

Particle Data Group



2\. Cerutti, F., and Salerno, R. (2026). “Higgs Boson Couplings: Present and Future.” Annual Review of Nuclear and Particle Science, 76, in press.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.annualreviews.org\&sz=32)

Annual Reviews

+1



3\. Källén, G. (1952). “On the Definition of the Renormalized Quantities in Quantum Electrodynamics.” Helvetica Physica Acta, 25, 417–434.

4\. Lehmann, H. (1954). “On the Properties of Propagation Functions and Renormalization Constants of Quantized Fields.” Il Nuovo Cimento, 11, 342–357. See also modern expositions of the Källén–Lehmann representation.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://qft.org\&sz=32)

QFT .org

+1



5\. Antusch, S., Hinze, K., and Saad, S. (2026). “Updated Running Quark and Lepton Parameters at Various Scales.” Physical Review D, 113, 095011.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. D



6\. The Standard Model. The Black Book of Quantum Chromodynamics: A Primer for the LHC Era. Oxford University Press. Discussion of Yukawa matrices, fermion mass diagonalization, and flavor mixing.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://academic.oup.com\&sz=32)

Oxford Academic



7\. Lawson, H. B., and Michelsohn, M.-L. (1989). Spin Geometry. Princeton University Press.

8\. Reed, M., and Simon, B. (1978–1980). Methods of Modern Mathematical Physics, Vols. I–IV. Academic Press.

9\. Gilkey, P. B. (1995). Invariance Theory, the Heat Equation, and the Atiyah–Singer Index Theorem, 2nd ed. CRC Press.

10\. Kaluza–Klein spectral reductions and higher-dimensional field theories provide established examples in which internal differential-operator spectra generate lower-dimensional mass towers. Their existence establishes the mechanism in particular models, not a universal derivation of the observed elementary-particle spectrum.

Final epistemic status: The spectral-to-mass correspondence is mathematically well-defined under the stated assumptions. The existence of a uniquely justified operator that derives the observed Standard-Model masses with genuine predictive compression remains an open research problem.

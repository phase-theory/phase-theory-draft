# The Information Curvature Theory

## A Variational Framework for Relating Statistical Distinguishability, Geometric Curvature, and Measurable Physical Response

Research objective: To establish whether the intrinsic curvature of a statistical or quantum state manifold constrains a measurable response function in a specified physical system, and to identify the conditions under which such a relation constitutes a new physical result rather than a reformulation of established information geometry.

The central problem is not to equip a family of states with a metric. Fisher information, quantum Fisher information, and their associated geometric structures already provide well-developed tools for doing so. The problem is to derive a nontrivial, falsifiable relation between an invariant of information geometry and an independently measurable physical quantity.

The theory developed here takes a concrete route: a two-parameter family of thermal quantum states, with inverse temperature and a dimensionless external-field parameter as coordinates, provides a setting in which information curvature can be related to thermodynamic response. The derivation distinguishes universal geometric identities from model-dependent physical predictions and identifies what additional result would be required to elevate the framework into a genuinely new theory.

A critical qualification governs the entire construction: a curvature–response relation cannot be called a new law merely because both sides can be calculated from the same partition function. Novelty requires an invariant relation with explanatory or predictive content beyond the known statistical identities, together with a specified regime of validity and an experimental protocol capable of falsifying it.

# Abstract

We formulate Information Curvature Theory (ICT) as a research framework in which the intrinsic geometry of a manifold of physically accessible states is used to characterize, constrain, and potentially predict the response of a system to external perturbations.

For a regular statistical family \\(p(x\mid\theta)\\), the Fisher information metric is

\\[ g\_{ij}(\theta) = \mathbb E\_\theta \left[ \partial_i\ln p(x\mid\theta)\\, \partial_j\ln p(x\mid\theta) \right]. \\]

When this metric is positive definite, it defines a Riemannian geometry with scalar curvature \\(\mathcal R\_{\mathrm I}\\). In a quantum system, an analogous construction begins with a family of density operators and a specified quantum information metric, such as the Bures metric or the Kubo–Mori metric. These choices are not interchangeable in general.

The central hypothesis of ICT is that information curvature can contain physically useful information about how a system responds to perturbations that is not captured by any single component of the information metric. The proposed framework separates three levels of result:

1. Established identities: information metrics encode local statistical distinguishability, and, under appropriate assumptions, their components coincide with measurable fluctuation or susceptibility quantities.
2. Derived curvature–response relation: in a two-dimensional statistical manifold, the scalar curvature can be written exactly in terms of the response matrix and its parameter derivatives.
3. Research conjecture: for selected interacting systems, a suitably normalized curvature invariant may provide a robust predictor of a measurable response enhancement or instability, beyond the information supplied by local susceptibilities alone.

The second result can be proved directly. The third requires model-specific analysis and experimental validation. Neither should be confused with a universal new law of physics.

This distinction is essential because information-geometric thermodynamics, beginning with foundational work on thermodynamic state-space geometry, already relates curvature to fluctuations, interactions, and correlation scales in appropriate settings.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A

+1

&#x20;The contribution sought here is a sharper, operationally testable invariant relation—not the mere assignment of curvature to a parameter space.



## 1. Foundations and scope

### 1.1 The physical question

Suppose a physical system is described by a family of states

\\[ \mathscr S=\\{\rho(\theta):\theta\in\Theta\\}, \\]

where \\(\Theta\\) is a parameter manifold and \\(\rho(\theta)\\) is either a probability distribution or a quantum density operator.

The coordinates \\(\theta^i\\) may represent temperature, external field, chemical potential, coupling strength, control voltage, or another experimentally tunable quantity. A small displacement \\(d\theta^i\\) changes the state by an amount that can be quantified through statistical distinguishability:

\\[ ds\_{\mathrm I}^{\\,2} =g\_{ij}(\theta)d\theta^i d\theta^j. \\]

This metric measures local sensitivity. Curvature, however, is not simply another sensitivity coefficient. It measures how the local geometry varies across the state manifold and whether that geometry can be flattened by a change of coordinates.

ICT asks whether that additional geometric information constrains measurable physical response.

Let \\(Y^a\\) denote observables and \\(\lambda^i\\) externally controlled parameters. A response matrix can be defined as

\\[ \chi^a{}\_i = \frac{\partial\langle Y^a\rangle}{\partial\lambda^i}. \\]

The research question is whether a coordinate-invariant scalar built from the information metric and its derivatives can predict a feature of \\(\chi^a{}\_i\\), or of higher-order response, that is not already evident from the metric itself.

### 1.2 What ICT does not assume

The theory does not assume that:

- information geometry replaces spacetime geometry;
- every physical interaction corresponds to nonzero information curvature;
- a curvature singularity necessarily represents a physical phase transition;
- every quantum information metric has the same curvature;
- information curvature is an independent force or a new fundamental field.

Such claims would require additional dynamical principles.

Instead, ICT begins with a family of experimentally specified states, constructs an information geometry, derives invariant relations, and tests whether those relations yield independent physical predictions.

### 1.3 Research hypotheses

We state three hypotheses with different evidential status.

H1 — Geometric response identity. For a regular two-parameter exponential family, the information curvature is determined by the response matrix and its first derivatives.

H2 — Response enhancement hypothesis. In selected interacting systems, a normalized curvature invariant may exhibit systematic scaling with a measurable response enhancement, after ordinary finite-size, coordinate, and background effects have been removed.

H3 — Predictive sufficiency hypothesis. In a specified class of systems, the curvature invariant may constrain a response observable more robustly than any one local susceptibility component.

H1 is a mathematical statement that can be proved under explicit regularity assumptions. H2 and H3 are empirical research hypotheses. Their validity is not assumed in the derivations below.

## 2. Statistical distinguishability and the Fisher metric

Let \\(p(x\mid\theta)\\) be a normalized probability density with respect to a fixed reference measure. Define the score functions

\\[ s_i(x;\theta)=\partial_i\ln p(x\mid\theta). \\]

Under regularity conditions allowing differentiation under the integral,

\\[ \mathbb E\_\theta[s_i] = \int dx\\,\partial_i p(x\mid\theta) =0. \\]

The Fisher information metric is

\\[ g\_{ij} = \mathbb E\_\theta[s_i s_j]. \\]

For any vector \\(v^i\\),

\\[ v^i g\_{ij}v^j = \mathbb E\_\theta[(v^is_i)^2] \geq0. \\]

Thus \\(g\_{ij}\\) is positive semidefinite. It is a Riemannian metric only where it is positive definite and nonsingular.

For a sufficiently small parameter displacement, the Kullback–Leibler divergence satisfies

\\[ D\_{\mathrm{KL}} \bigl(p\_\theta\Vert p\_{\theta+d\theta}\bigr) = \frac12g\_{ij}d\theta^i d\theta^j +O(\\|d\theta\\|^3). \\]

Consequently, the Fisher metric provides a local, coordinate-covariant measure of distinguishability.

The metric is not an arbitrary choice once the statistical model and measurement procedure are fixed. It follows from the local distinguishability structure of that model. However, changing the accessible measurement scheme or the statistical model may change the relevant metric.

### 2.1 Curvature as a second-order geometric invariant

The Levi-Civita connection associated with \\(g\_{ij}\\) is

\\[ \Gamma^k{}\_{ij} = \frac12g^{k\ell} \left( \partial_i g\_{j\ell} +\partial_j g\_{i\ell} -\partial\_\ell g\_{ij} \right). \\]

The Riemann tensor is

\\[ R^i{}\_{jkl} = \partial_k\Gamma^i{}\_{lj} -\partial_l\Gamma^i{}\_{kj} +\Gamma^i{}\_{km}\Gamma^m{}\_{lj} -\Gamma^i{}\_{lm}\Gamma^m{}\_{kj}, \\]

with the sign convention fixed by this expression. Contracting indices yields the Ricci tensor and scalar curvature:

\\[ R\_{jl}=R^i{}\_{jil}, \qquad \mathcal R\_{\mathrm I}=g^{jl}R\_{jl}. \\]

The scalar \\(\mathcal R\_{\mathrm I}\\) is invariant under smooth reparameterizations of the state manifold. Its numerical value still depends on the chosen metric, and its physical units depend on the units assigned to the metric and coordinates.

Curvature therefore carries a different kind of information from a single diagonal Fisher component. A large \\(g\_{11}\\) indicates strong local distinguishability in one coordinate direction. A large \\(|\mathcal R\_{\mathrm I}|\\) indicates strong intrinsic curvature of the metric geometry. One does not, in general, imply the other.

## 3. The exponential-family connection to measurable response

The most direct bridge between information geometry and physical response occurs for exponential families.

Consider

\\[ p(x\mid\theta) = h(x)\exp\\!\left[ \theta^i T_i(x)-\psi(\theta) \right], \\]

where \\(\psi(\theta)\\) is the log-partition function and the distribution is normalized. We assume the sufficient statistics \\(T_i\\) do not themselves depend on \\(\theta\\).

Normalization gives

\\[ \partial_i\psi=\langle T_i\rangle. \\]

The score is

\\[ s_i=T_i-\langle T_i\rangle, \\]

so the Fisher metric becomes

\\[ \boxed{ g\_{ij} = \partial_i\partial_j\psi = \operatorname{Cov}(T_i,T_j). } \\]

This is an exact result under the stated assumptions.

If the coordinates are thermodynamic fields conjugate to physical observables, the Fisher metric is therefore a covariance matrix. Derivatives of the mean observables with respect to the conjugate fields give the same response matrix, up to the appropriate sign and temperature factors.

For example, in a canonical ensemble with Hamiltonian \\(H\\) independent of inverse temperature \\(\beta\\),

\\[ p_n(\beta)=\frac{e^{-\beta E_n}}{Z(\beta)}, \qquad Z(\beta)=\sum_n e^{-\beta E_n}, \\]

we have

\\[ g\_{\beta\beta} = \operatorname{Var}\_\beta(H). \\]

The heat capacity at constant volume is

\\[ C_V = \frac{\partial\langle H\rangle}{\partial T} = \frac{\operatorname{Var}(H)}{k\_{\mathrm B}T^2}. \\]

Since \\(\beta=(k\_{\mathrm B}T)^{-1}\\),

\\[ \boxed{ g\_{\beta\beta} = \frac{C_V}{k\_{\mathrm B}\beta^2}. } \\]

Thus a diagonal Fisher component is directly proportional to a measurable equilibrium response. This identity is established statistical mechanics, not a novel prediction of ICT.

The potential new result must concern what the curvature of the full multidimensional response geometry reveals beyond the individual response coefficients.

## 4. The central theorem: information curvature as a response invariant

We now derive the principal mathematical result of the framework.

Let \\(\Theta\subset\mathbb R^2\\) be a two-dimensional parameter domain and let

\\[ p(x\mid\theta) = h(x)\exp\\!\left[ \theta^1T_1(x)+\theta^2T_2(x)-\psi(\theta) \right] \\]

be a regular exponential family. Assume \\(\psi\in C^5(\Theta)\\), the Fisher metric is positive definite, and all derivatives and expectations used below exist.

Define the response matrix

\\[ \chi\_{ij} = \frac{\partial\langle T_i\rangle}{\partial\theta^j}. \\]

For natural parameters,

\\[ \chi\_{ij} = \partial_i\partial_j\psi = g\_{ij}. \\]

Introduce the third-order response tensor

\\[ C\_{ijk} = \partial_k\chi\_{ij} = \partial_i\partial_j\partial_k\psi. \\]

For an exponential family, \\(C\_{ijk}\\) is the third joint cumulant of the sufficient statistics:

\\[ C\_{ijk} = \operatorname{Cum}(T_i,T_j,T_k). \\]

This equality follows by differentiating the log-partition function. The derivatives of the partition potential are therefore measurable cumulants or response derivatives, not abstract geometric quantities detached from the system.

### Theorem 4.1 — Two-dimensional information-curvature/response identity

Under the assumptions above, define

\\[ \Delta=\det\chi =\chi\_{11}\chi\_{22}-\chi\_{12}^{\\,2}>0. \\]

Then, using the curvature convention specified in Section 2, the scalar curvature of the Fisher metric is

\\[ \boxed{ \mathcal R\_{\mathrm I} = -\frac{1}{2\Delta^2} \det \begin{pmatrix} \chi\_{11}&\chi\_{12}&\chi\_{22}\\\ \partial_1\chi\_{11}&\partial_1\chi\_{12}&\partial_1\chi\_{22}\\\ \partial_2\chi\_{11}&\partial_2\chi\_{12}&\partial_2\chi\_{22} \end{pmatrix}. } \tag{4.1} \\]

Here the determinant uses the symmetry of mixed derivatives; in particular, \\(\partial_1\chi\_{12}=\partial_2\chi\_{11}\\) and \\(\partial_2\chi\_{12}=\partial_1\chi\_{22}\\).

The overall sign reverses if the opposite Riemann-tensor convention is adopted.

#### Proof

Since \\(g\_{ij}=\partial_i\partial_j\psi\\), the Fisher metric is a Hessian metric. Its first derivatives are

\\[ \partial_k g\_{ij} = \partial_i\partial_j\partial_k\psi = C\_{ijk}. \\]

The Christoffel symbols with the final index lowered are

\\[ \Gamma\_{ijk} = \frac12 \left( \partial_i g\_{jk} +\partial_j g\_{ik} -\partial_k g\_{ij} \right). \\]

Commutation of the third derivatives of \\(\psi\\) gives

\\[ \Gamma\_{ijk}=\frac12 C\_{ijk}. \\]

The derivatives of the inverse metric satisfy

\\[ \partial\_\ell g^{ij} = -g^{ia}(\partial\_\ell g\_{ab})g^{bj} = -g^{ia}C\_{ab\ell}g^{bj}. \\]

Substituting these identities into the Riemann tensor eliminates all independent derivatives of the metric in favor of the third derivatives of the potential. In the Hessian geometry, the resulting curvature tensor is algebraic in the cubic tensor \\(C\_{ijk}\\) and the inverse metric. Contracting to the scalar curvature and using the two-dimensional determinant identity yields

\\[ \mathcal R\_{\mathrm I} = -\frac{1}{2(\det g)^2} \det \begin{pmatrix} \psi\_{11}&\psi\_{12}&\psi\_{22}\\\ \psi\_{111}&\psi\_{112}&\psi\_{122}\\\ \psi\_{112}&\psi\_{122}&\psi\_{222} \end{pmatrix}. \\]

Finally, substituting \\(g\_{ij}=\chi\_{ij}\\) and \\(C\_{ijk}=\partial_k\chi\_{ij}\\) proves (4.1). \\(\square\\)

### Interpretation

Equation (4.1) expresses intrinsic information curvature entirely in terms of a measurable response matrix and its derivatives.

Its numerator vanishes when the three rows in the determinant are linearly dependent. Subject to \\(\Delta>0\\), the scalar curvature then vanishes even if individual response coefficients are nonzero.

Conversely, curvature can become large when the determinant of the response matrix becomes small or when response derivatives become large. These are distinct mechanisms and must not be conflated.

The identity is exact, but it is not, by itself, a new empirical law. It is a geometric rewriting of derivatives of the log-partition function. The potential research contribution lies in identifying systems where the resulting scalar provides a robust, nonredundant predictor of physical response.

The relationship between Hessian geometry, cumulants, and information-geometric curvature is part of the established mathematical framework of information geometry.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://pmc.ncbi.nlm.nih.gov\&sz=32)

PMC

+1



## 5. A measurable curvature invariant

Equation (4.1) suggests a natural experimental strategy: reconstruct the response matrix from measurements, estimate its derivatives, and compare the curvature calculated from those data with an independent geometric reconstruction.

To make the proposal precise, define the response-determinant curvature numerator

\\[ \mathfrak D\_{\chi} = \det \begin{pmatrix} \chi\_{11}&\chi\_{12}&\chi\_{22}\\\ \partial_1\chi\_{11}&\partial_1\chi\_{12}&\partial_1\chi\_{22}\\\ \partial_2\chi\_{11}&\partial_2\chi\_{12}&\partial_2\chi\_{22} \end{pmatrix}. \\]

Then

\\[ \boxed{ \mathfrak D\_{\chi} =-2\mathcal R\_{\mathrm I}(\det\chi)^2. } \tag{5.1} \\]

This equation gives a direct consistency test between independently estimated response data and the information metric.

However, \\(\mathfrak D\_\chi\\) is a coordinate-dependent component expression, not itself a scalar invariant under arbitrary reparameterization. The scalar curvature is invariant. The determinant formula is valid in the natural coordinates of the exponential family and transforms with the appropriate coordinate factors.

A useful physical test must therefore distinguish:

- the coordinate-invariant scalar \\(\mathcal R\_{\mathrm I}\\);
- the response matrix \\(\chi\_{ij}\\), whose components depend on the chosen parameter coordinates;
- experimentally defined controls, which fix the physical coordinate system and units;
- any proposed normalized invariant, whose transformation properties must be demonstrated rather than assumed.

### 5.1 Proposed normalized response-curvature observable

For a two-parameter system, let \\(\chi\\) be the positive-definite response matrix in a fixed natural-coordinate chart. A candidate dimensionless quantity can be formed by multiplying the scalar curvature by a physically defined area scale \\(A\_{\mathrm{ref}}\\):

\\[ \mathcal K\_{\mathrm I} = A\_{\mathrm{ref}}\mathcal R\_{\mathrm I}. \\]

The area scale must be defined operationally—for example, from a calibrated parameter-space resolution cell or from specified characteristic parameter scales. It cannot be selected after seeing the data merely to improve agreement.

If \\(\theta^i\\) are dimensionless natural parameters, the Fisher line element and \\(\mathcal R\_{\mathrm I}\\) are dimensionless in the conventional statistical normalization, and \\(A\_{\mathrm{ref}}\\) can be dimensionless as well. If the coordinates carry physical units, the dimensions must instead be tracked explicitly.

The hypothesis that \\(\mathcal K\_{\mathrm I}\\) predicts a response anomaly is a proposal for experimental investigation, not a consequence of (5.1) alone.

## 6. Specified physical system: the finite Ising chain

We now select a concrete system in which the response-curvature identity can be tested.

Consider a periodic one-dimensional Ising chain with \\(N\\) spins \\(\sigma_i\in\\{-1,+1\\}\\), exchange coupling \\(J\\), external field \\(h\\), and temperature \\(T\\). Its energy is

\\[ H(\boldsymbol\sigma) = -J\sum\_{i=1}^{N}\sigma_i\sigma\_{i+1} -h\sum\_{i=1}^{N}\sigma_i, \qquad \sigma\_{N+1}=\sigma_1. \\]

Define dimensionless natural parameters

\\[ K=\beta J,\qquad B=\beta h, \qquad \beta=(k\_{\mathrm B}T)^{-1}. \\]

The Gibbs distribution is

\\[ p(\boldsymbol\sigma\mid K,B) = \frac{1}{Z_N(K,B)} \exp\\!\left[ K\sum_i\sigma_i\sigma\_{i+1} +B\sum_i\sigma_i \right]. \\]

The sufficient statistics are

\\[ T_1=\sum_i\sigma_i\sigma\_{i+1}, \qquad T_2=\sum_i\sigma_i. \\]

The log-partition potential is \\(\psi(K,B)=\ln Z_N(K,B)\\), and the Fisher metric is

\\[ g\_{ij} = \partial_i\partial_j\ln Z_N. \\]

Its components are

\\[ g\_{KK}=\operatorname{Var}(T_1), \qquad g\_{BB}=\operatorname{Var}(T_2), \qquad g\_{KB}=\operatorname{Cov}(T_1,T_2). \\]

These quantities can be obtained experimentally from repeated spin configurations, from fluctuation measurements, or from calibrated estimates of the corresponding susceptibilities.

### 6.1 Transfer-matrix partition function

The transfer matrix is

\\[ \mathbf T= \begin{pmatrix} e^{K+B}&e^{-K}\\\ e^{-K}&e^{K-B} \end{pmatrix}. \\]

Its eigenvalues are

\\[ \lambda\_\pm = e^K\cosh B \pm \sqrt{e^{2K}\sinh^2B+e^{-2K}}. \\]

Therefore the finite periodic chain has partition function

\\[ \boxed{ Z_N(K,B)=\lambda\_+^N+\lambda\_-^N. } \tag{6.1} \\]

Equations (6.1) and the response-curvature identity define a complete analytical prediction for the Fisher curvature of this model. Differentiating \\(\ln Z_N\\) gives the response matrix; differentiating the response matrix and inserting it into (4.1) gives the scalar curvature.

No additional geometric postulate is needed.

### 6.2 Connection to measurable magnetic response

The mean magnetization per spin is

\\[ m(K,B) = \frac1N\langle T_2\rangle = \frac1N\partial_B\ln Z_N. \\]

Its susceptibility at fixed \\(K\\) is

\\[ \chi_m = \left.\frac{\partial m}{\partial B}\right|\_K = \frac1N g\_{BB}. \\]

In physical units, the derivative with respect to the applied field \\(h\\) includes the factor \\(\beta\\) arising from \\(B=\beta h\\).

The energy-like response is associated with derivatives with respect to \\(K\\). The mixed component \\(g\_{KB}\\) measures the covariance between bond energy and total magnetization.

Consequently, the scalar curvature \\(\mathcal R\_{\mathrm I}(K,B)\\) can be reconstructed from the field-dependent magnetic susceptibility, the energy-fluctuation response, the mixed covariance, and derivatives of those responses.

This is a measurable relationship in a specified physical system. It is not yet evidence that curvature predicts an independent phenomenon: all of the terms are generated by the same equilibrium distribution.

### 6.3 A null test

At \\(B=0\\), spin-flip symmetry gives

\\[ \langle T_2\rangle=0, \qquad \operatorname{Cov}(T_1,T_2)=0. \\]

Thus \\(g\_{KB}=0\\) on the symmetry line. This simplifies the response matrix but does not by itself imply that the scalar curvature vanishes, because the curvature also depends on derivatives of the response components away from the symmetry line.

This is a useful safeguard against a common error: a diagonal response matrix at one point does not establish a flat statistical manifold.

### 6.4 What the Ising test can establish

The finite chain provides four concrete tests.

1. Identity test: Does the curvature calculated from the analytic partition function agree with the curvature reconstructed from measured response functions?
2. Coordinate test: Does a change of parameter coordinates leave the computed scalar curvature invariant?
3. Finite-size test: How does the reconstructed curvature vary with \\(N\\), particularly near regimes of rapidly changing susceptibility?
4. Predictive test: Does curvature add statistically significant out-of-sample predictive information about a chosen response observable after the local response matrix and finite-size effects have already been included?

The fourth test is the critical one for the proposed physical significance of ICT.

## 7. Quantum extension: choosing the correct information metric

For a quantum system, the state is represented by a density operator

\\[ \rho(\theta)\geq0,\qquad \operatorname{Tr}\rho(\theta)=1. \\]

A quantum information metric quantifies distinguishability between nearby density operators. Unlike the classical regular setting, there is no single universally interchangeable quantum metric for every operational question.

The choice must reflect the measurement or response being studied. The Bures metric is tied to quantum-state fidelity and quantum estimation, whereas the Kubo–Mori metric is naturally associated with equilibrium statistical response. Their geometric properties and operational meanings differ.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A

+1



### 7.1 Quantum Fisher information

For a parameter \\(\theta^i\\), the symmetric logarithmic derivative \\(L_i\\) is defined by

\\[ \partial_i\rho = \frac12(\rho L_i+L_i\rho). \\]

The symmetric-logarithmic-derivative quantum Fisher information matrix is

\\[ F\_{ij}^{\mathrm{SLD}} = \frac12\operatorname{Tr} \left[ \rho(L_iL_j+L_jL_i) \right]. \\]

Under a common convention, the Bures metric is related to this matrix by

\\[ g\_{ij}^{\mathrm B}=\frac14F\_{ij}^{\mathrm{SLD}}. \\]

The factor of four is conventional and must be retained consistently when computing curvature. Constant rescaling of a metric changes its scalar curvature inversely: if \\(\tilde g=cg\\) for constant \\(c>0\\), then

\\[ \widetilde{\mathcal R}\_{\mathrm I} = \frac{1}{c}\mathcal R\_{\mathrm I}. \\]

Therefore, curvature values computed from different metric normalizations cannot be compared without specifying the convention.

For a pure state \\(|\psi(\theta)\rangle\\), the quantum geometric tensor is

\\[ Q\_{ij} = \langle\partial_i\psi|\partial_j\psi\rangle - \langle\partial_i\psi|\psi\rangle \langle\psi|\partial_j\psi\rangle. \\]

Its real part supplies the pure-state metric, while its imaginary part encodes geometric phase information. The relationship between quantum geometric tensors, Bures distinguishability, and parameter sensitivity is established in quantum information geometry.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

PRX Quantum

+1



### 7.2 Quantum response and equilibrium geometry

For a Gibbs state,

\\[ \rho\_\theta = \frac{e^{-K(\theta)}}{Z(\theta)}, \\]

the connection between the information metric and physical response depends on the generator \\(K\\), its parameter dependence, and whether the relevant generators commute.

For a single parameter \\(\theta\\) that enters through a parameter-independent Hamiltonian \\(H\\) as \\(\rho\_\beta=e^{-\beta H}/Z\\), the eigenvalues follow a classical exponential family. The corresponding thermal statistical metric satisfies

\\[ g\_{\beta\beta}^{\mathrm{cl}} = \operatorname{Var}(H). \\]

For noncommuting parameter-dependent Hamiltonians, the quantum response includes changes in eigenvectors as well as changes in eigenvalues. The symmetric logarithmic derivative metric, the Kubo–Mori metric, and the ordinary covariance matrix need not agree.

An ICT calculation must therefore specify:

- the state family \\(\rho(\theta)\\);
- the chosen quantum metric;
- the physical response observable;
- the response protocol, including what is held fixed;
- the normalization and treatment of rank-changing states.

The last point is not merely technical. The quantum Fisher information can behave discontinuously when the rank of the density operator changes, while the Bures metric admits a continuous formulation in cases where the two quantities no longer coincide in the naive way.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A



### 7.3 Quantum curvature-response hypothesis

For a two-parameter quantum family, define \\(\mathcal R\_{\mathrm B}\\) from the Bures metric. A proposed test is to compare its variation with an independently measured response, such as magnetic susceptibility, fidelity susceptibility, or a calibrated dynamical response coefficient.

The hypothesis is not that every quantum susceptibility is proportional to Bures curvature. Rather, it is that in a selected model and a specified regime, a properly normalized curvature invariant may track a particular response enhancement with a scaling law that survives changes of coordinates and finite-size extrapolation.

Such a relation must be derived for the chosen Hamiltonian and metric. The classical identity in Theorem 4.1 cannot simply be transferred to a general quantum Bures metric, because the latter need not be a Hessian metric in the same natural coordinates.

## 8. Distinguishing geometric identity from new physical law

The central challenge for ICT is to avoid relabeling established information geometry as a new physical theory.

The following distinctions are decisive.

| Claim                                                                                                   | Status                            | What would establish it?                                                          |
| ------------------------------------------------------------------------------------------------------- | --------------------------------- | --------------------------------------------------------------------------------- |
| Fisher information measures local statistical distinguishability                                        | Established                       | Regular statistical model and standard assumptions                                |
| Fisher information in an exponential family equals a covariance matrix                                  | Established                       | Differentiation of the log-partition function                                     |
| Two-dimensional Hessian-metric curvature is determined by second and third derivatives of the potential | Established mathematical identity | Differential-geometric derivation                                                 |
| Curvature of a particular physical state manifold tracks a measurable response anomaly                  | Model-dependent                   | Analytical prediction and experimental comparison                                 |
| Curvature predicts response beyond the full local response matrix                                       | Unproven research hypothesis      | Out-of-sample predictive advantage under controlled comparison                    |
| Information curvature imposes a universal new constraint on physical dynamics                           | Not established                   | A general theorem with explicit assumptions and independently tested consequences |

The first three statements supply the mathematical foundation. The fourth may yield a useful physical result. The fifth is a stronger novelty criterion. The sixth would require a substantially broader theory.

### 8.1 Why correlation is insufficient

Suppose both \\(\mathcal R\_{\mathrm I}\\) and a susceptibility \\(\chi\\) are calculated from the same partition function. A correlation between them may arise because both depend on the same underlying derivatives of \\(\ln Z\\).

Such a correlation is not, by itself, evidence that curvature causes, controls, or independently predicts the susceptibility.

A defensible predictive claim requires at least one of the following:

- a derived relation that eliminates microscopic parameters;
- a universal scaling law that holds across a defined class of models;
- a bound on response that follows from geometric assumptions;
- an out-of-sample prediction that outperforms a baseline using the complete local response matrix;
- an experimentally measured relation not used to construct or fit the proposed curvature law.

The strongest route would be a parameter-free or independently calibrated relation, but even then the assumptions and range of validity must be stated.

## 9. A proposed new research invariant: curvature-weighted response susceptibility

We now introduce a candidate observable for systematic investigation. It is a research definition, not a theorem that the quantity obeys a universal law.

Let \\(\chi\\) be a positive-definite response matrix on a two-dimensional natural-parameter manifold, and let \\(Y\\) be a specified observable with susceptibility \\(\chi_Y\\). Define

\\[ \boxed{ \mathcal J_Y = \ell\_{\mathrm{ref}}^2 \\,\mathcal R\_{\mathrm I}\\, \chi_Y, } \tag{9.1} \\]

where \\(\ell\_{\mathrm{ref}}^2\\) denotes a fixed, physically calibrated normalization with units chosen so that \\(\mathcal J_Y\\) is dimensionless.

The normalization cannot be chosen arbitrarily: it must be specified before fitting the relation and must transform consistently under reparameterization. For dimensionless natural coordinates, the Fisher curvature is dimensionless in the conventional statistical normalization; if the susceptibility carries units, the scale factor must remove them.

The motivation is to test whether curvature modifies the interpretation of a response enhancement. The central question is whether \\(\mathcal J_Y\\) exhibits a stable scaling relation across system sizes, interaction strengths, or independent realizations of the same model.

### 9.1 The conjectured scaling form

Near a critical or crossover regime, consider the hypothesis

\\[ \mathcal J_Y \sim A\\,|\epsilon|^{-\kappa}, \qquad \epsilon=\frac{T-T_c}{T_c}, \tag{9.2} \\]

where \\(A\\) is an amplitude and \\(\kappa\\) is a scaling exponent.

Equation (9.2) is a candidate scaling ansatz. Neither the existence of a divergence nor the value of \\(\kappa\\) follows from information geometry alone. The exponent must be derived from the chosen model or estimated from data, with finite-size and regular-background effects accounted for.

For the finite one-dimensional Ising chain at nonzero temperature, there is no finite-temperature thermodynamic phase transition in the infinite-chain limit. Thus one should not use that system to assert a genuine finite-temperature critical divergence. It is instead a useful controlled test of the exact identity and finite-size behavior. A system with a genuine critical point would be required to test (9.2) as a critical scaling law.

### 9.2 Conditions for an invariant formulation

A quantity deserves to be called an invariant only if its transformation properties have been established.

Under a coordinate change \\(\theta^i\mapsto\tilde\theta^a\\), the metric transforms as a rank-two tensor, and \\(\mathcal R\_{\mathrm I}\\) remains a scalar. A response component such as \\(\chi_Y=\partial\langle Y\rangle/\partial\theta^1\\), however, is not generally a scalar.

Accordingly, \\(\mathcal J_Y\\) in (9.1) is not automatically coordinate invariant. A fully invariant version must replace \\(\chi_Y\\) with a scalar constructed using a specified tangent direction, vector field, or contraction of response tensors.

For example, let \\(v^i\\) be a physically specified unit tangent vector satisfying

\\[ g\_{ij}v^iv^j=1. \\]

Then a directional response may be defined as

\\[ \chi_Y(v)=v^i\partial_i\langle Y\rangle. \\]

If \\(v^i\\) is transformed as a vector under reparameterization, \\(\chi_Y(v)\\) is a scalar. A curvature-weighted directional response can therefore be defined by

\\[ \mathcal J_Y(v) = \mathcal R\_{\mathrm I}\\, \chi_Y(v)\\, s_Y, \\]

where \\(s_Y\\) is an independently specified normalization with the units needed to make the result dimensionless.

This construction is geometrically consistent once \\(v^i\\), \\(Y\\), and \\(s_Y\\) are operationally defined. It still does not establish that \\(\mathcal J_Y(v)\\) obeys a universal scaling law.

### 9.3 A stringent novelty criterion

A convincing new ICT result would demonstrate that \\(\mathcal J_Y(v)\\) obeys a relation of the form

\\[ \mathcal F\\!\left( \mathcal J_Y, \text{independently measured controls} \right)=0 \\]

for a defined class of systems, with \\(\mathcal F\\) derived from the physical model rather than fitted without constraints.

The relation should survive coordinate changes, finite-size analysis, and independent measurement of the response. It should also fail, or change in a specifically predicted way, when the system is taken outside the assumed class.

Until such a result is obtained, (9.1)–(9.2) define a research program rather than an established law.

## 10. Experimental program

The experimental program must separate validation of the mathematical construction from validation of the stronger physical hypothesis.

### 10.1 Stage I: reconstruct the information geometry

For each experimental control point \\(\theta\\), collect sufficient measurements to estimate the relevant state distribution or quantum state.

For a classical exponential family, estimate

\\[ \widehat g\_{ij} = \widehat{\operatorname{Cov}}(T_i,T_j). \\]

Estimate response derivatives either by controlled finite differences or by direct higher-order fluctuation measurements. The preferred method depends on the noise, sample size, and differentiability of the underlying response.

For a quantum system, perform state tomography or use a validated measurement protocol sufficient to estimate the selected quantum metric. The measurement design must be fixed before comparing different metric definitions.

### 10.2 Stage II: compute curvature independently

There are two complementary routes:

1. Model-based calculation: calculate curvature from the analytically known partition function or quantum-state model.
2. Data-based reconstruction: estimate the metric and its derivatives from measured responses, then compute curvature.

Agreement between these routes is a consistency test. Disagreement can reveal sampling bias, finite-difference instability, an incorrect state model, or failure of the assumed equilibrium description.

Since curvature involves derivatives of the metric, it is particularly sensitive to statistical noise. Confidence intervals should be obtained by bootstrap resampling, Bayesian posterior sampling, or another justified uncertainty-propagation procedure. Derivatives should not be smoothed in a way that artificially creates or suppresses curvature singularities.

### 10.3 Stage III: test predictive content

The primary outcome must be selected in advance. Suitable outcomes include a susceptibility at an independently sampled control point, a response peak location, a finite-size scaling exponent, or a response coefficient under a new perturbation.

Compare at least two predictive models:

- Baseline model: uses the measured local response matrix and prespecified control variables.
- Curvature-augmented model: adds the proposed invariant or curvature-derived constraint.

Evaluation must use held-out conditions or independent samples. A curvature-augmented model that only reproduces the data used to estimate the curvature has not demonstrated predictive novelty.

### 10.4 Stage IV: cross-system validation

The finite Ising chain is a controlled analytical test. It should be followed by a system with a genuinely interacting critical regime if critical scaling is the intended target.

A suitable candidate is a two-dimensional magnetic system whose order parameter, susceptibility, and finite-size behavior can be measured independently. A quantum spin system may also be suitable if its state family and measurement-accessible metric are well characterized.

The test should compare:

- the predicted curvature and its uncertainty;
- the response peak and its location;
- finite-size scaling;
- the response of an appropriate noncritical reference system;
- the stability of conclusions under legitimate reparameterizations.

A successful result would be a relation that persists across independent realizations within a clearly stated model class, not merely a curve that fits one dataset.

## 11. Falsifiability and failure conditions

ICT must be capable of failing. The following outcomes would directly weaken or exclude particular versions of the theory.

### 11.1 Failure of the statistical geometry

If the chosen state family is not differentiable, the Fisher metric is singular, or the required moments diverge, the regular Riemannian construction may not apply. A singularity should not automatically be interpreted as physical curvature; it may indicate that the statistical model has left the domain in which the metric is well defined.

### 11.2 Failure of the curvature–response identity

For a regular two-dimensional exponential family, Theorem 4.1 is an exact mathematical identity. A reproducible disagreement between the two sides after uncertainty and coordinate conventions are handled correctly would indicate a computational error, an incorrect model, or a violation of the assumptions—not a new physical effect.

For a general quantum metric, the classical Hessian identity is not guaranteed. A quantum extension must be proved separately.

### 11.3 Failure of the proposed predictive law

Suppose a candidate normalized curvature invariant is hypothesized to predict a response enhancement. The hypothesis is weakened if:

- the predicted scaling fails under increasing system size;
- the relation disappears after accounting for known susceptibility scaling;
- the curvature adds no predictive information on held-out data;
- its fitted exponent varies without explanation across nominally equivalent systems;
- the relation depends on arbitrary parameterization or normalization choices;
- the same behavior occurs in control systems where the proposed mechanism is absent.

A hypothesis that can be preserved by changing its normalization or interpretation after every failed test is not a useful physical law.

### 11.4 Failure of a universal interpretation

Nonzero information curvature is not universally equivalent to strong interactions, criticality, or large correlations. Thermodynamic curvature has been investigated in relation to interactions and correlation volumes, but its physical interpretation depends on the model and regime.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A

+1



ICT must therefore specify the class of systems to which each proposed relation applies. If different systems exhibit different curvature–response relations, the correct conclusion may be a family of model-dependent results rather than a universal theory.

## 12. Relationship to established approaches

Information Curvature Theory intersects several mature research areas. Its novelty must be judged relative to them.

### 12.1 Fisher–Rao information geometry

Fisher–Rao geometry constructs a metric from statistical distinguishability and studies the resulting geometric structure. ICT adopts this foundation rather than replacing it.

The proposed extension is to organize curvature–response relations around operationally measurable invariants and require evidence that those invariants add predictive content.

### 12.2 Ruppeiner thermodynamic geometry

Ruppeiner geometry relates thermodynamic fluctuations to a Riemannian structure on the space of equilibrium states. Its literature already investigates thermodynamic curvature, interaction effects, and correlations near criticality.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A

+1



Consequently, the assertion that “thermodynamic curvature relates to response” cannot itself be the novel claim of ICT.

The research task is to derive a more precise relation for a specified system, identify the circumstances under which it remains invariant and predictive, and determine whether it yields a result not already implied by existing thermodynamic geometry.

### 12.3 Quantum information geometry

Quantum Fisher information and the Bures metric connect state distinguishability with quantum parameter estimation. They also appear in studies of fidelity susceptibility and quantum critical behavior.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

PRX Quantum

+2



ICT's quantum extension must go beyond restating those connections. It needs a specified metric, a physical response, and a derived relation that survives an independent test.

### 12.4 Thermodynamic response theory

Ordinary statistical mechanics already supplies fluctuation–response identities. Information geometry can reorganize these identities into tensorial and coordinate-invariant statements, but a new notation is not a new physical mechanism.

The distinction is between a geometric representation of known response theory and a geometric constraint that yields additional predictive power.

## 13. Limitations and unresolved questions

The present framework has five principal limitations.

First, curvature is model dependent. The metric depends on the chosen statistical family and, in the quantum case, on the selected quantum information metric. There is no unique curvature independent of these choices.

Second, curvature does not automatically determine dynamics. The state manifold describes how states vary with parameters. A dynamical law additionally specifies time evolution, constraints, and how external perturbations are applied. A geometric identity alone does not determine those ingredients.

Third, curvature can amplify estimation errors. Because it depends on derivatives of the metric, a curvature estimate may be substantially noisier than the underlying response measurements. Any proposed enhancement must be distinguished from a numerical differentiation artifact.

Fourth, singular geometry needs interpretation. A vanishing metric determinant can make the scalar curvature representation singular, but that fact alone does not establish a physical instability. One must determine whether the singularity reflects a genuine thermodynamic limit, a loss of parameter identifiability, a boundary of state space, or a defect of the chosen representation.

Fifth, no universal new response law has yet been established here. The response-curvature identity is derived, but the stronger claim—that curvature predicts an independent measurable feature of physical response—remains a model-specific research objective.

These limitations define the work required to turn the framework into a predictive physical theory.

## 14. Research propositions and theorem status

The mathematical and physical claims can be summarized in a hierarchy.

### Established mathematical results

1. The Fisher metric is the local distinguishability metric of a regular statistical family.
2. For a regular exponential family, \\(g\_{ij}=\partial_i\partial_j\psi=\operatorname{Cov}(T_i,T_j)\\).
3. For a two-dimensional Hessian metric, scalar curvature is determined by the Hessian potential's second and third derivatives.
4. Combining the preceding results gives the response-curvature identity in Theorem 4.1.

### Results derived for the selected model

5. The finite Ising-chain partition function gives an explicit route to its Fisher metric and curvature.
6. The magnetic susceptibility and energy-like response components are entries of the information metric in the chosen natural coordinates.
7. The scalar curvature can be reconstructed from the response matrix and its derivatives, subject to regularity and measurement precision.

### Unproven research hypotheses

8. A normalized curvature invariant may exhibit a robust scaling law in selected interacting systems.
9. Curvature may provide out-of-sample predictive information beyond the complete local response matrix.
10. A broader class of physical systems may obey a common curvature–response constraint derived from additional dynamical assumptions.

The distinction is substantive. The first group follows from established mathematics. The second provides a concrete model in which the identities can be evaluated. The third contains the claims that must survive independent testing before ICT can be regarded as a new predictive physical theory.

## 15. Conclusions

Information Curvature Theory begins from a defensible premise: the geometry of distinguishability between physically accessible states is mathematically connected to fluctuations and response. Its challenge is to convert that connection into a nontrivial physical constraint.

The central theorem establishes that, for a regular two-parameter exponential family, the scalar Fisher curvature is expressible through the response matrix and its derivatives. The finite Ising chain supplies a concrete system with a known partition function, measurable magnetic response, and a controlled route to testing the identity.

This is a useful foundation, but it is not yet the sought-after new physical law. The identity is a geometric consequence of the exponential-family structure, and information-geometric thermodynamics already provides closely related curvature–fluctuation connections.

The decisive next step is to derive a model-specific invariant relation that makes a prediction not already contained in the measured local response matrix. The relation must specify its normalization, regime of validity, finite-size behavior, and failure conditions before it is tested against independent data.

If such a relation can be established across a defined class of interacting systems, Information Curvature Theory would offer more than a geometric reinterpretation of statistical mechanics: it would supply a compact invariant constraint linking state-space geometry to measurable physical response.

If no independent predictive relation survives these tests, the appropriate conclusion is narrower but still useful: information curvature provides a geometric representation of response structure, without constituting a new fundamental dynamical law.

## References

1\. R. A. Fisher, “On the Mathematical Foundations of Theoretical Statistics,” Philosophical Transactions of the Royal Society A 222, 309–368 (1922).

2\. C. R. Rao, “Information and the Accuracy Attainable in the Estimation of Statistical Parameters,” Bulletin of the Calcutta Mathematical Society 37, 81–91 (1945).

3\. S. Amari and H. Nagaoka, Methods of Information Geometry, American Mathematical Society and Oxford University Press (2000).

4\. N. N. Čencov, Statistical Decision Rules and Optimal Inference, American Mathematical Society (1982).

5\. G. Ruppeiner, “Thermodynamics: A Riemannian Geometric Model,” Physical Review A 20, 1608–1613 (1979).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A



6\. G. Ruppeiner, “Riemannian Geometry in Thermodynamic Fluctuation Theory,” Reviews of Modern Physics 67, 605–659 (1995).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Rev. Mod. Phys.



7\. S. Amari, Information Geometry and Its Applications, Springer (2016).

8\. D. Petz, “Monotone Metrics on Matrix Spaces,” Linear Algebra and its Applications 244, 81–96 (1996).

9\. D. Šafránek, “Discontinuities of the Quantum Fisher Information and the Bures Metric,” Physical Review A 95, 052320 (2017).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://doi.org\&sz=32)

Phys. Rev. A



10\. A. Monras and F. Illuminati, “Information Geometry of Gaussian Channels,” Physical Review A 81, 062326 (2010).&#x20;

[image](https://www.google.com/s2/favicons?domain=https://journals.aps.org\&sz=32)

Phys. Rev. A



11\. C. W. Helstrom, Quantum Detection and Estimation Theory, Academic Press (1976).

12\. A. Lesniewski and M. B. Ruskai, “Monotone Riemannian Metrics and Relative Entropy on Non-Commutative Probability Spaces,” Journal of Mathematical Physics 40, 5702–5724 (1999).

13\. R. Kubo, “Statistical-Mechanical Theory of Irreversible Processes. I. General Theory and Simple Applications to Magnetic and Conduction Problems,” Journal of the Physical Society of Japan 12, 570–586 (1957).

14\. L. Onsager, “Reciprocal Relations in Irreversible Processes. I,” Physical Review 37, 405–426 (1931).

15\. R. J. Baxter, Exactly Solved Models in Statistical Mechanics, Academic Press (1982).

16\. E. T. Jaynes, “Information Theory and Statistical Mechanics,” Physical Review 106, 620–630 (1957).

17\. M. A. Nielsen and I. L. Chuang, Quantum Computation and Quantum Information, Cambridge University Press (2000).

18\. P. Zanardi, P. Giorda, and M. Cozzini, “Information-Theoretic Differential Geometry of Quantum Phase Transitions,” Physical Review Letters 99, 100603 (2007).

19\. L. Campos Venuti and P. Zanardi, “Quantum Critical Scaling of the Geometric Tensors,” Physical Review Letters 99, 095701 (2007).

20\. S. L. Braunstein and C. M. Caves, “Statistical Distance and the Geometry of Quantum States,” Physical Review Letters 72, 3439–3443 (1994).

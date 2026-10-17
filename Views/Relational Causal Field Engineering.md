# Relational Causal Field Engineering: A Technology Derived from RR-NPM

**Research preprint — October 2026**

## Abstract

We derive a concrete technology program from the theoretical framework called Relational Relativity without Fundamental Photon Motion, RR-NPM. The central technological consequence is this: if electromagnetic propagation is not fundamentally explained by photon trajectories but by field structure and null relations among events, then the primary engineering object is not a ray, beam, or photon path, but the retarded two-point causal response kernel connecting emission events to detection events.

Starting from Maxwell theory, Lorentzian geometry, and quantum detection theory, we construct a device class called **Relational Causal Field Engineering**, or RC-FE. Its basic function is to synthesize, shape, and interrogate the retarded electromagnetic Green tensor between controlled event sets. The resulting technologies include:

1. **Null-relation optical routers**, which direct electromagnetic information by programming effective spacetime metrics and boundary phase structures rather than by assigning geometric ray paths.
2. **Relational causal processors**, which compute by programming the source–detector response matrix and using interference, thresholding, and causal gating.
3. **Event-correlation imagers**, which reconstruct objects from changes in two-point field response rather than from ray trajectories.
4. **Relational positioning and synchronization networks**, which reconstruct geometry from null-relation data and radar intervals.
5. **Quantum causal-link devices**, whose operational variables are field correlation functions rather than individual photon worldlines.

The central formal result is that a broad class of electromagnetic technologies can be reformulated as the problem of engineering the retarded bitensor  
\[
G^\mu{}_{\nu'}(q,p)
\]
between emission event \(p\) and detection event \(q\), subject to retarded support, gauge constraints, energy conservation, and Lorentz covariance. The RR-NPM framework therefore supplies not merely an interpretive reformulation of relativity but a principled engineering ontology: **build devices that control causal relations, not photon trajectories.**

**Keywords:** RR-NPM; relational relativity; null geometry; Green tensor; causal field engineering; photonic computing; transformation optics; metasurfaces; quantum detection; event-based sensing.

---

## 1. Technological Consequence of RR-NPM

The RR-NPM framework replaces the primitive explanatory role of photon trajectories with the structure  
\[
\mathfrak R=(\mathcal E,\mathcal N,\mathcal F),
\]
where \(\mathcal E\) is a set of physical events, \(\mathcal N\) specifies null relations, and \(\mathcal F\) denotes electromagnetic field structure. The physical content of light propagation is then encoded by relations among events and by the field dynamics that connect them.

From an engineering standpoint, this produces a precise shift:

\[
\text{Conventional photon technology:}
\qquad
\text{source} \to \text{ray/beam path} \to \text{detector},
\]

\[
\text{RR-NPM-derived technology:}
\qquad
(p,q)\text{ event pair} \to
G^\mu{}_{\nu'}(q,p)
\to
P(q\mid p).
\]

The central object becomes the conditional detection probability
\[
P(q\mid p,\mathcal F,g,\mathcal I),
\]
where \(p\) is a preparation or emission event, \(q\) is a detection event, \(g\) is the spacetime or effective metric, \(\mathcal F\) is the field configuration, and \(\mathcal I\) denotes the interaction and measurement conditions.

The technology derived here does not require denial of ordinary electromagnetic propagation. It does not assert that signals are instantaneous. It does not assign a photon a rest frame. It instead uses the following engineering principle.

### Engineering Principle I: Causal-kernel primacy

The primary controllable quantity in electromagnetic technology is the retarded causal response kernel between events, not the trajectory of an individual photon.

This principle converts RR-NPM into a design theory.

---

## 2. The Fundamental Engineering Object: The Retarded Causal Kernel

### 2.1 Maxwell theory as an event-response theory

In a four-dimensional Lorentzian spacetime \((M,g_{\mu\nu})\) with signature \((-+++)\), the electromagnetic field tensor is
\[
F_{\mu\nu}=2\nabla_{[\mu}A_{\nu]}.
\]

In the presence of a source current \(J^\mu\), Maxwell’s equations are
\[
\nabla_\mu F^{\mu\nu}=\mu_0 J^\nu,
\tag{2.1}
\]
\[
\nabla_{[\alpha}F_{\beta\gamma]}=0.
\tag{2.2}
\]

In Lorenz gauge,
\[
\nabla_\mu A^\mu=0,
\]
the potential satisfies, in curved spacetime,
\[
\square_g A^\nu-R^\nu{}_\mu A^\mu=-\mu_0 J^\nu,
\tag{2.3}
\]
where \(\square_g=\nabla_\mu\nabla^\mu\) and \(R^\nu{}_\mu\) is the Ricci tensor.

Define the retarded vector Green bitensor \(G^\nu{}_{\rho'}(x,x')\) by
\[
\left(\square_g \delta^\nu{}_\sigma-R^\nu{}_\sigma\right)
G^\sigma{}_{\rho'}(x,x')
=
-\delta^\nu{}_{\rho'}\delta_g(x,x'),
\tag{2.4}
\]
with retarded support,
\[
G^\nu{}_{\rho'}(x,x')=0
\quad
\text{if }x\notin J^+(x').
\tag{2.5}
\]

Here \(\delta_g(x,x')\) is the invariant Dirac distribution,
\[
\int dV_{x'}\,\delta_g(x,x')f(x')=f(x).
\]

The retarded solution is
\[
A^\nu(x)
=
\mu_0\int_{J^-(x)}
dV_{x'}\,
G^\nu{}_{\rho'}(x,x')J^{\rho'}(x').
\tag{2.6}
\]

Equation (2.6) is the mathematical foundation of relational causal field engineering. It expresses the field at an event \(x\) as a causal functional of source data in its past.

### 2.2 Point-event emission and detection

Let the source be localized near an emission event \(p\) with effective dipole or current moment \(s^\rho\). Ideally,
\[
J^\rho(x')=s^\rho\delta_g(x',p).
\]

Then the potential at detection event \(q\) is
\[
A^\nu(q)
=
\mu_0 G^\nu{}_{\rho'}(q,p)s^\rho.
\tag{2.7}
\]

A physical detector couples not to the gauge-dependent potential alone but to the field strength. Define the field-strength Green tensor
\[
\mathcal G_{\mu\nu\rho'}(q,p)
=
2\nabla_{[\mu}G_{\nu]\rho'}(q,p).
\tag{2.8}
\]

Then
\[
F_{\mu\nu}(q)
=
\mu_0\mathcal G_{\mu\nu\rho'}(q,p)s^\rho.
\tag{2.9}
\]

Let the detector be characterized by a response tensor \(d^{\mu\nu}(q)\). The elementary event-response amplitude is
\[
\mathcal M(q\mid p)
=
\kappa\,
d^{\mu\nu}(q)
\mathcal G_{\mu\nu\rho'}(q,p)
s^{\rho'}(p),
\tag{2.10}
\]
where \(\kappa\) contains coupling constants and normalization.

The corresponding detection probability is, to lowest order,
\[
P(q\mid p)
\propto
\left|\mathcal M(q\mid p)\right|^2.
\tag{2.11}
\]

Equation (2.10) is the elementary device equation of RC-FE. It replaces the statement “a photon travels from \(p\) to \(q\)” with the statement “the source, field kernel, and detector jointly define an event-response amplitude.”

### 2.3 Null-cone dominance

For a massless field in four-dimensional globally hyperbolic spacetime, the retarded Green function has the Hadamard form
\[
G_{\mathrm{ret}}(q,p)
=
\Theta_+(q,p)
\left[
U(q,p)\delta(\sigma(q,p))
+
V(q,p)\theta(-\sigma(q,p))
\right],
\tag{2.12}
\]
where \(\sigma(q,p)\) is Synge’s world function, equal to one half the squared geodesic interval, and \(\Theta_+(q,p)\) enforces future-directed causal support.

The leading singular term is supported on
\[
\sigma(q,p)=0,
\tag{2.13}
\]
which is precisely the null relation.

Thus, in the high-frequency or geometrical-optics regime, the dominant causal connection between emission and detection is governed by the null geometry:
\[
g^{\mu\nu}\nabla_\mu\sigma\nabla_\nu\sigma=0
\quad
\text{on }\sigma=0.
\tag{2.14}
\]

This gives the first technological theorem.

### Theorem 1: Null-relation engineering is sufficient for leading-order light routing

If a device controls the effective null relation \(\sigma_g(q,p)=0\) between chosen event sets, then it controls the leading-order propagation channel between those events.

**Proof sketch.** The leading singular support of the retarded Green tensor lies on the null cone \(\sigma=0\). The wavefront set of the field generated by a localized source is propagated along the bicharacteristics determined by the principal symbol of the wave operator. Those bicharacteristics are the null covectors satisfying
\[
g^{\mu\nu}k_\mu k_\nu=0.
\]
Therefore, shaping the effective null structure shapes the dominant event-response kernel. \(\square\)

This theorem converts the RR-NPM null relation into an engineering target.

---

## 3. Relational Causal Field Engineering: Core Technology Principle

We now define the technology.

### Definition 1: Relational Causal Field Engineering

Relational Causal Field Engineering, abbreviated RC-FE, is the design and control of electromagnetic systems by direct synthesis of the retarded event-response kernel
\[
K(q,p)
=
d^{\mu\nu}(q)
\mathcal G_{\mu\nu\rho'}(q,p)
s^{\rho'}(p),
\tag{3.1}
\]
subject to the constraints of retarded causal support, gauge invariance, energy conservation, and covariance.

The objective is not to optimize a photon path. It is to synthesize a desired conditional event map
\[
p\longmapsto q
\]
through the kernel \(K(q,p)\).

### 3.1 Target event relation

Let \(\mathcal R\subseteq\mathcal E_{\mathrm{src}}\times\mathcal E_{\mathrm{det}}\) be a desired relational map between source events and detector events. A device realizes \(\mathcal R\) with contrast \(\eta\) if
\[
|K(q,p)|^2
\ge K_0
\quad
\text{for }(p,q)\in\mathcal R,
\tag{3.2}
\]
and
\[
|K(q,p)|^2
\le \eta K_0
\quad
\text{for }(p,q)\notin\mathcal R,
\tag{3.3}
\]
with \(0\le\eta\ll1\).

The engineering loss functional may be written as
\[
\mathcal L[K]
=
\sum_{(p,q)\in\mathcal R}
\left|K(q,p)-K_\star(q,p)\right|^2
+
\lambda
\sum_{(p,q)\notin\mathcal R}
|K(q,p)|^2
+
\mathcal C[K],
\tag{3.4}
\]
where \(\mathcal C[K]\) enforces physical constraints such as passivity, reciprocity, bandwidth, and power limitations.

### 3.2 Realizability conditions

A target kernel \(K_{\mathrm{target}}(q,p)\) is physically admissible only if it satisfies:

1. **Retarded causal support:**
   \[
   K(q,p)=0
   \quad
   \text{if }q\notin J^+(p).
   \tag{3.5}
   \]

2. **Null-cone compatibility in the high-frequency limit:**
   \[
   \sigma_{\mathrm{eff}}(q,p)=0
   \quad
   \text{for dominant channels}.
   \tag{3.6}
   \]

3. **Gauge consistency:**
   Physical detector couplings must depend on \(F_{\mu\nu}\), not on gauge-dependent quantities.

4. **Energy-momentum conservation:**
   The field stress-energy tensor
   \[
   T_{\mu\nu}
   =
   \frac{1}{\mu_0}
   \left(
   F_{\mu\alpha}F_\nu{}^\alpha
   -
   \frac14 g_{\mu\nu}F_{\alpha\beta}F^{\alpha\beta}
   \right)
   \tag{3.7}
   \]
   must satisfy the appropriate local balance law.

5. **Passivity and bounded gain:**
   The device cannot produce net energy except through supplied sources.

These constraints define the feasible set of RC-FE designs.

---

## 4. Technology I: Null-Relation Optical Router

The first concrete technology is a router that establishes selected event-to-event links by programming effective null relations.

### 4.1 Effective metric control

In a material or metamaterial medium, Maxwell’s equations may be written in terms of an excitation tensor \(H^{\mu\nu}\):
\[
\partial_\nu H^{\mu\nu}=J^\mu,
\tag{4.1}
\]
with constitutive relation
\[
H^{\mu\nu}
=
\frac12
\chi^{\mu\nu\alpha\beta}
F_{\alpha\beta}.
\tag{4.2}
\]

For a metric-type medium, the constitutive tensor may be written, up to constants, as
\[
\chi^{\mu\nu\alpha\beta}
=
\sqrt{-g_{\mathrm{eff}}}
\left(
g_{\mathrm{eff}}^{\mu\alpha}g_{\mathrm{eff}}^{\nu\beta}
-
g_{\mathrm{eff}}^{\mu\beta}g_{\mathrm{eff}}^{\nu\alpha}
\right).
\tag{4.3}
\]

In the geometric-optics limit, the wave covector \(k_\mu=\partial_\mu S\) satisfies
\[
g_{\mathrm{eff}}^{\mu\nu}k_\mu k_\nu=0.
\tag{4.4}
\]

Therefore, by engineering \(\chi^{\mu\nu\alpha\beta}\), one engineers the effective null cone.

### 4.2 Router condition

Given a source event \(p\) and a desired detection event \(q\), the router must impose an effective metric \(g_{\mathrm{eff}}\) such that
\[
\sigma_{g_{\mathrm{eff}}}(q,p)=0,
\tag{4.5}
\]
and such that competing events \(q'\notin\mathcal R(p)\) satisfy
\[
|K(q',p)|^2\ll |K(q,p)|^2.
\tag{4.6}
\]

In homogeneous vacuum, the condition reduces to
\[
-c^2(t_q-t_p)^2+|\mathbf x_q-\mathbf x_p|^2=0.
\tag{4.7}
\]

In a programmable medium,
\[
g_{\mathrm{eff}}^{\mu\nu}(x)\partial_\mu T(x)\partial_\nu T(x)=0,
\tag{4.8}
\]
where \(T(x)\) is the arrival-time phase field. The router solves an inverse problem: choose \(g_{\mathrm{eff}}\) or \(\chi\) so that the solution \(T\) has prescribed level sets at the target detectors.

### 4.3 Metasurface implementation

Let \(\Sigma\) be a programmable metasurface between source and detector. The field at \(q\) due to source \(p\) after transmission through \(\Sigma\) is approximately
\[
E(q)
\sim
\int_\Sigma d^2y\,
G_0(q,y)\,
t(y)\,
G_0(y,p),
\tag{4.9}
\]
where \(t(y)=a(y)e^{i\phi(y)}\) is the programmable complex transmission coefficient.

For a homogeneous background,
\[
G_0(x,y)\sim
\frac{e^{ik|x-y|}}{|x-y|}.
\]

Stationary phase requires
\[
\nabla_\Sigma
\left[
k|q-y|
+
\phi(y)
+
k|y-p|
\right]
=0.
\tag{4.10}
\]

Thus the required phase profile is
\[
\nabla_\Sigma\phi(y)
=
-k\nabla_\Sigma
\left[
|q-y|+|y-p|
\right].
\tag{4.11}
\]

Equation (4.11) is the relational routing equation. It designs a null relation between \(p\) and \(q\) without referring to a photon trajectory. The metasurface does not guide a particle along a path; it enforces a constructive event-response relation between two spacetime events.

### 4.4 Device architecture

A practical null-relation router consists of:

1. A source array defining emission events \(p_i\).
2. A programmable metasurface or transformation-optical medium controlling \(\chi^{\mu\nu\alpha\beta}\).
3. A detector array defining candidate detection events \(q_a\).
4. A feedback controller estimating the measured kernel \(K(q_a,p_i)\).
5. An optimizer minimizing \(\mathcal L[K]\).

The router may operate in microwave, terahertz, infrared, or optical regimes.

### 4.5 Performance metrics

Define the causal contrast ratio
\[
\Gamma
=
\frac{|K(q_{\mathrm{target}},p)|^2}
{\sum_{q\ne q_{\mathrm{target}}}|K(q,p)|^2}.
\tag{4.12}
\]

Define the causal fidelity
\[
\mathcal F_C
=
\frac{
\left|
\sum_{p,q}
K_{\mathrm{meas}}(q,p)
K_{\mathrm{target}}^\ast(q,p)
\right|^2
}{
\left(
\sum_{p,q}|K_{\mathrm{meas}}(q,p)|^2
\right)
\left(
\sum_{p,q}|K_{\mathrm{target}}(q,p)|^2
\right)
}.
\tag{4.13}
\]

The minimum latency satisfies the causal bound
\[
t_q-t_p
\ge
\frac{1}{c}
\int_{\gamma_{\mathrm{opt}}}
n_{\mathrm{eff}}\,d\ell,
\tag{4.14}
\]
where \(\gamma_{\mathrm{opt}}\) is the extremal optical path determined by \(g_{\mathrm{eff}}\).

This technology is not superluminal. It is causal-relation engineering.

---

## 5. Technology II: Relational Causal Processor

The second technology is a computational architecture based on programming the full source–detector kernel.

### 5.1 Multiport causal response matrix

Let there be \(N\) source ports and \(M\) detector ports. Let source amplitudes be \(x_i\), \(i=1,\dots,N\). Let detector outputs be \(y_a\), \(a=1,\dots,M\). Then
\[
y_a
=
\sum_{i=1}^N
K_{ai}x_i
+
n_a,
\tag{5.1}
\]
where
\[
K_{ai}
=
d_a^{\mu\nu}
\mathcal G_{\mu\nu\rho'}
(q_a,p_i)
s_i^{\rho'}
\tag{5.2}
\]
and \(n_a\) is noise.

The device computes by implementing a desired matrix \(K\) and then applying nonlinear thresholding or digital decision.

### 5.2 Matrix programming through boundary control

The Green tensor inside a bounded domain \(\Omega\) is determined by the interior operator and the boundary conditions. Let \(B\) denote a programmable boundary operator, for example a metasurface impedance map. Then schematically
\[
G_B(q,p)=G_0(q,p)+\delta G_B(q,p).
\tag{5.3}
\]

By controlling \(B\), one controls \(K_{ai}\). The programming problem is
\[
B^\star
=
\arg\min_B
\left\|
K(B)-K_{\mathrm{target}}
\right\|^2.
\tag{5.4}
\]

This is a physical implementation of an analog matrix processor, but the RR-NPM interpretation gives it a different operational meaning: the processor does not route photons along wires or rays; it realizes a relation between input events and output events.

### 5.3 Logic from relational interference

Let logical variables be encoded by complex source amplitudes. A logic output may be defined by
\[
z_a
=
\Theta
\left(
|y_a|^2-\theta_a
\right),
\tag{5.5}
\]
where \(\Theta\) is a threshold function.

For a Boolean function \(f:\{0,1\}^N\to\{0,1\}\), the relational logic condition is
\[
\left|
\beta_a+
\sum_{i=1}^N K_{ai}x_i
\right|^2
\begin{cases}
>\theta_a, & f(x)=1,\\
<\theta_a, & f(x)=0.
\end{cases}
\tag{5.6}
\]

With enough complex degrees of freedom, the points corresponding to different input strings can be separated in the output complex plane. Thus universal logic is obtainable through linear causal-kernel synthesis plus nonlinear detection.

### 5.4 Computational capacity

The number of independent spatial channels in a diffraction-limited system of area \(A\) and angular bandwidth \(\Omega\) is approximately
\[
N_{\mathrm{modes}}
\sim
\frac{A\Omega}{\lambda^2}.
\tag{5.7}
\]

With electrical bandwidth \(B\), the number of complex degrees of freedom per second is approximately
\[
N_{\mathrm{dof}}
\sim
2BN_{\mathrm{modes}}.
\tag{5.8}
\]

If the singular-value decomposition of the kernel is
\[
K=U\Sigma V^\dagger,
\]
then the communication or computational capacity under additive Gaussian noise is bounded by
\[
C
\le
\sum_{j}
B_j
\log_2
\left(
1+
\frac{P_j\sigma_j^2}{N_j}
\right),
\tag{5.9}
\]
where \(\sigma_j\) are the singular values of \(K\), \(P_j\) is allocated power, and \(N_j\) is noise power in channel \(j\).

Thus RC-FE computation is constrained by the singular structure of the causal kernel. The technology problem is to shape that singular structure.

### 5.5 Energy-per-bit bound

For direct detection of an on-off keyed coherent optical signal with quantum efficiency \(\eta\), the mean detected photon number per bit is \(\eta\bar n\). In the shot-noise limit, the bit-error probability is approximately
\[
P_e
\approx
\frac12
\operatorname{erfc}
\left(
\sqrt{\frac{\eta\bar n}{2}}
\right).
\tag{5.10}
\]

Solving for \(\bar n\),
\[
\bar n
\ge
\frac{2}{\eta}
\left[
\operatorname{erfc}^{-1}(2P_e)
\right]^2.
\tag{5.11}
\]

The energy per bit is therefore bounded by
\[
E_{\mathrm{bit}}
\ge
\hbar\omega
\frac{2}{\eta}
\left[
\operatorname{erfc}^{-1}(2P_e)
\right]^2.
\tag{5.12}
\]

This bound is independent of trajectory ontology. It is a constraint on the field-response technology.

---

## 6. Technology III: Event-Correlation Imager

The third technology is an imaging system based on changes in the two-point causal kernel.

### 6.1 Scattering as relational kernel perturbation

Let the background wave operator be \(L_0\), with Green tensor \(G_0\). Let an object introduce a perturbation \(\delta V(z)\), so that
\[
L=L_0+\delta V.
\]

To first Born order,
\[
\delta G(q,p)
=
-
\int dV_z\,
G_0(q,z)
\delta V(z)
G_0(z,p).
\tag{6.13}
\]

The measured object signature is not a ray deflection. It is a change in the event-response kernel:
\[
\delta K(q,p)
=
d^{\mu\nu}(q)
\delta\mathcal G_{\mu\nu\rho'}(q,p)
s^{\rho'}(p).
\tag{6.14}
\]

### 6.2 Relational backpropagation functional

Define the imaging functional
\[
I(z)
=
-
\sum_{p,q}
\delta K(q,p)
G_0^\ast(q,z)
G_0^\ast(p,z).
\tag{6.15}
\]

Under ideal sampling,
\[
I(z)
\approx
\delta V(z)
\]
up to the point-spread function of the aperture.

The resolution limit is approximately
\[
\Delta x
\sim
\frac{\lambda}{2\,\mathrm{NA}},
\tag{6.16}
\]
where \(\mathrm{NA}\) is the numerical aperture.

### 6.3 Operational advantage

Conventional ray-based imaging assumes that the relevant information is carried by trajectories through space. RC-FE imaging instead treats the measured data as samples of the two-point causal response. This is especially useful when:

1. Multipath scattering invalidates simple ray pictures.
2. Diffraction and interference dominate.
3. The medium is strongly inhomogeneous.
4. Quantum correlations are measured rather than intensities.
5. The geometry itself is unknown and must be reconstructed jointly with the object.

The imager reconstructs the perturbation \(\delta V\) from event correlations, not from assigned photon paths.

---

## 7. Technology IV: Relational Positioning and Synchronization Network

The fourth technology is a positioning and clock-synchronization system derived from null relations.

### 7.1 Radar coordinates

An observer emits a signal at proper time \(\tau_-\) and receives its reflection at proper time \(\tau_+\). The reflected event is assigned radar time
\[
\tau
=
\frac{\tau_++\tau_-}{2},
\tag{7.1}
\]
and radar distance
\[
\rho
=
\frac{c(\tau_+-\tau_-)}{2}.
\tag{7.2}
\]

These coordinates are operational and event-based. They do not require a photon trajectory as a primitive; they require only emission, reflection, and reception events.

### 7.2 Network reconstruction

For a network of nodes \(i,j\), null-related time-of-flight measurements satisfy, in a local inertial approximation,
\[
c^2(t_i-t_j)^2
-
|\mathbf x_i-\mathbf x_j|^2
=0.
\tag{7.3}
\]

Define residuals
\[
r_{ij}
=
c^2(t_i-t_j)^2
-
|\mathbf x_i-\mathbf x_j|^2.
\tag{7.4}
\]

The positions and clock offsets are estimated by minimizing
\[
\mathcal S
=
\sum_{i<j}
w_{ij}r_{ij}^2.
\tag{7.5}
\]

In curved or inhomogeneous environments, replace (7.3) by the null condition
\[
g_{\mu\nu}dx^\mu dx^\nu=0
\tag{7.6}
\]
or by the eikonal equation
\[
g^{\mu\nu}\partial_\mu T\partial_\nu T=0.
\tag{7.7}
\]

### 7.3 Metric reconstruction from causal data

RR-NPM states that causal relations determine the conformal metric, while scale information is supplied by clocks or volume standards. Technologically, this implies a two-stage reconstruction:

1. **Conformal stage:** reconstruct null cones from event relations.
2. **Scale stage:** reconstruct the conformal factor \(\Omega(x)\) from proper-time and distance standards.

Write
\[
g_{\mu\nu}
=
\Omega^2(x)\widehat g_{\mu\nu}.
\tag{7.8}
\]

The null structure fixes \(\widehat g_{\mu\nu}\). Clocks and rods fix \(\Omega\).

This yields a technology for **self-calibrating spacetime mapping**: a distributed network can reconstruct its local effective geometry from event-relational measurements.

---

## 8. Technology V: Quantum Causal-Link Devices

The quantum version of RC-FE uses field correlation functions rather than classical amplitudes.

### 8.1 One-photon event response

Let a one-photon state be
\[
|1_f\rangle
=
\int d\mu(k)\,
f(k)a^\dagger(k)|0\rangle.
\tag{8.1}
\]

The detection amplitude at event \(q\) is governed by the positive-frequency field operator:
\[
\mathcal A(q)
=
\langle 0|
E^{(+)}(q)
|1_f\rangle.
\tag{8.2}
\]

In a Green-function representation,
\[
\mathcal A(q)
\propto
\int dV_x\,
G_{\mathrm{ret}}(q,x)f(x).
\tag{8.3}
\]

The detection probability density is
\[
P(q)
\propto
\left|\mathcal A(q)\right|^2.
\tag{8.4}
\]

Again, no primitive photon trajectory is required. The operational object is the field-mediated correlation between preparation and detection.

### 8.2 Glauber correlation technology

The first-order field correlation is
\[
G^{(1)}(x,y)
=
\langle
E^{(-)}(x)E^{(+)}(y)
\rangle.
\tag{8.5}
\]

The local detection rate is
\[
R(x)
=
G^{(1)}(x,x).
\tag{8.6}
\]

A quantum RC-FE device engineers \(G^{(1)}(x,y)\) across selected event pairs.

### 8.3 Quantum causal key distribution

A communication protocol may be defined as follows.

1. Alice and Bob share a programmable causal channel with kernel \(K(q,p)\).
2. They encode key bits by selecting among two or more causal configurations, for example different metasurface phase maps.
3. The legitimate receiver verifies the expected correlation signature.
4. An eavesdropper who attempts to sample or alter the channel changes the effective kernel.

Define the kernel disturbance
\[
D
=
1-
\frac{
\left|
\sum_{p,q}
K_{\mathrm{expected}}^\ast(q,p)
K_{\mathrm{observed}}(q,p)
\right|^2
}{
\left(
\sum |K_{\mathrm{expected}}|^2
\right)
\left(
\sum |K_{\mathrm{observed}}|^2
\right)
}.
\tag{8.7}
\]

The induced quantum bit-error rate is approximately
\[
Q
\sim
\frac{D}{2},
\tag{8.8}
\]
for symmetric disturbance models.

The security basis is not the secrecy of a photon path. It is the integrity of the causal-correlation structure.

---

## 9. General RC-FE Device Equation

All of the above technologies are special cases of one master equation.

Let \(s_i\) denote source controls, \(d_a\) detector controls, \(B\) boundary controls, and \(g_{\mathrm{eff}}\) effective metric controls. The device output is
\[
y_a
=
\mathcal D_a
\left[
G_{\mathrm{ret}}
\left[
g_{\mathrm{eff}},B
\right]
(s_i)
\right]
+
n_a,
\tag{9.1}
\]
where \(\mathcal D_a\) is the detector functional.

The engineering problem is
\[
\{s_i^\star,d_a^\star,B^\star,g_{\mathrm{eff}}^\star\}
=
\arg\min
\mathcal L
\left[
y_a-y_a^{\mathrm{target}}
\right],
\tag{9.2}
\]
subject to retarded causal support, passivity, bandwidth, and energy constraints.

This is the master control problem of Relational Causal Field Engineering.

---

## 10. Experimental Implementation Program

### 10.1 Phase I: Microwave causal-kernel synthesis

Use phased antenna arrays and programmable impedance boundaries to measure and shape \(K(q,p)\) in the microwave regime.

Objective:

\[
\mathcal F_C>0.95
\]
for a target event-relation map in a bounded cavity.

Measurements:

1. Time-domain Green function.
2. S-parameter matrix.
3. Causal contrast \(\Gamma\).
4. Latency bound saturation.

### 10.2 Phase II: Metasurface null-relation router

Implement a programmable optical or infrared metasurface with phase and amplitude control.

Objective:

Route selected source–detector event pairs with extinction ratio
\[
\Gamma>10^3
\]
over a reconfigurable set of target events.

Key equation:
\[
\nabla_\Sigma\phi(y)
=
-k\nabla_\Sigma
\left[
|q-y|+|y-p|
\right].
\]

### 10.3 Phase III: Relational photonic processor

Integrate source arrays, programmable scattering media, and threshold detectors.

Objective:

Implement a programmable matrix \(K\) with rank
\[
r(K)\ge 16
\]
and demonstrate reconfigurable logic or reservoir computing.

Figure of merit:
\[
\mathrm{TOPS/W}
=
\frac{N_{\mathrm{ops}}/s}{P_{\mathrm{total}}}.
\]

### 10.4 Phase IV: Event-correlation imager

Use broadband illumination and detector arrays to reconstruct \(\delta V(z)\) from \(\delta K(q,p)\).

Objective:

Achieve diffraction-limited reconstruction using only two-point response data, without ray-based reconstruction.

Objective metric:
\[
\mathrm{SSIM}
>
0.9
\]
for calibrated test targets.

### 10.5 Phase V: Quantum causal-link demonstration

Use single-photon or weak-coherent states and time-resolved detectors to measure \(G^{(1)}(q,p)\) under programmed boundary conditions.

Objective:

Demonstrate that intentional boundary disturbance produces measurable increase in \(D\) and corresponding error rate \(Q\).

---

## 11. Novelty Relative to Conventional Photonics

The novelty is not merely incremental. Conventional photonic engineering usually treats beams, rays, modes, or photons as primary objects. RC-FE instead treats the retarded event-response kernel as primary.

The conceptual hierarchy becomes:

\[
\text{RR-NPM ontology}
\quad
\Rightarrow
\quad
\text{event relations}
\]

\[
\text{event relations}
\quad
\Rightarrow
\quad
\text{Green-kernel engineering}
\]

\[
\text{Green-kernel engineering}
\quad
\Rightarrow
\quad
\text{router, processor, imager, synchronization network}
\]

The new technological primitive is

\[
\boxed{
K(q,p)
=
d^{\mu\nu}(q)
\mathcal G_{\mu\nu\rho'}(q,p)
s^{\rho'}(p)
}
\]

rather than a photon trajectory.

---

## 12. The Central Technological Claim

The central claim derived from RR-NPM is therefore:

\[
\boxed{
\text{Electromagnetic technology can be formulated as the controlled synthesis of retarded null-relational field responses between physical events.}
}
\]

This claim does not require superluminal signaling, photon rest frames, or denial of observed propagation. It preserves the invariant causal structure and the vacuum speed \(c\). It changes the engineering target from path control to causal-relation control.

The resulting technology program is experimentally accessible through existing electromagnetic platforms: phased arrays, transformation optics, programmable metasurfaces, cavity electrodynamics, integrated photonics, and quantum correlation measurements.

---

## 13. Conclusion

The RR-NPM framework, when taken seriously as an engineering ontology, generates a new technology class. The removal of fundamental photon motion does not weaken electromagnetic theory; it redirects attention to the actual calculable objects of the theory: retarded Green tensors, field correlations, null relations, and detector response functionals.

From this redirection follows a concrete technological program:

\[
\boxed{
\text{Relational Causal Field Engineering}
}
\]

Its governing equation is the event-response amplitude

\[
\mathcal M(q\mid p)
=
\kappa\,
d^{\mu\nu}(q)
\mathcal G_{\mu\nu\rho'}(q,p)
s^{\rho'}(p),
\]

its design target is the null relation

\[
\sigma_g(q,p)=0,
\]

and its operational objective is to synthesize desired causal maps

\[
p\longmapsto q
\]

without assigning ontological or engineering primacy to photon trajectories.

The decisive next step is not philosophical but experimental: build a programmable electromagnetic domain in which the measured kernel \(K(q,p)\) can be shaped to realize prescribed event relations, and verify that the resulting device performance is governed by the causal-kernel design equations derived above.

THE IONIC TEMPORAL INTEGRATOR (ITI)

A Material-State Circuit Element for Analog Temporal Integration Through Ionic Penetration and Electrochemical Doping

A Comprehensive Research Preprint

⸻

Abstract

This paper proposes the Ionic Temporal Integrator (ITI), an organic electronic circuit element that performs analog temporal integration through the controlled penetration, redistribution, and relaxation of mobile ions within an organic mixed ionic–electronic conductor (OMIEC).

The central hypothesis is that the ionic and electrochemical state of an organic material can encode a weighted history of an electrical input and provide a directly measurable output without requiring a conventional discrete capacitor-based integrator as the primary computational element.

The proposed first-order phenomenological law is

[
\boxed{
\tau\frac{dx}{dt}+x=kV_{\mathrm{in}}(t)
}
]

where (x(t)) represents a normalized electrochemical state, (\tau) is an effective ionic relaxation time, (k) is an input-coupling coefficient, and (V_{\mathrm{in}}) is the applied input voltage.

The equation defines a leaky integrator with an exponential memory kernel. Its physical interpretation is that an electrical input drives ionic redistribution and electrochemical doping, while diffusion, extraction, and relaxation progressively reduce the stored state. The output therefore represents a weighted temporal history rather than an instantaneous voltage measurement.

A distributed drift–diffusion model is developed to connect ionic transport to the lumped ITI equation. The model includes ionic conservation, electronic charge compensation, electrochemical potential, chemical capacitance, nonlinear doping response, and terminal transduction. The reduction from spatially distributed transport to a first-order state equation is derived under explicit assumptions and accompanied by conditions under which it fails.

The paper develops a device architecture, material-selection criteria, fabrication strategy, readout configurations, pulse-response theory, frequency-domain characteristics, energy considerations, stability conditions, noise analysis, and experimental validation protocol. It also proposes a distinction between three operating regimes: leaky integration, quasi-ideal integration, and persistent electrochemical memory.

The principal scientific claim is not that ionic integration or organic electrochemical memory is individually unknown. Organic electrochemical transistors already demonstrate ion-mediated conductance modulation, transient responses, and history-dependent operation. The proposed contribution is to define and validate a dedicated circuit primitive whose intended operation is calibrated temporal integration through internal electrochemical state evolution.

The most important experimental requirement is to demonstrate that the measured output is governed by a reproducible ionic state and not adequately explained by ordinary parasitic capacitance, external RC filtering, contact artifacts, or irreversible material degradation.

Keywords: ionic temporal integration; organic electrochemical transistor; organic mixed ionic–electronic conductor; electrochemical doping; chemical capacitance; ion diffusion; material-state computation; leaky integrator; analog computing; neuromorphic electronics; electrochemical memory; organic circuit theory.

⸻

1. Introduction

1.1 The temporal problem in electronic computation

A signal is not completely characterized by its instantaneous amplitude.

In many physical systems, the significance of a signal depends on how long it persists, how frequently it occurs, how rapidly it changes, and how it relates temporally to previous events.

Examples include:

* Accumulation of weak biological signals.
* Detection of repeated chemical events.
* Temporal coincidence in sensory systems.
* Integration of mechanical disturbances.
* Monitoring of slowly varying environmental conditions.
* Recognition of pulse sequences.
* Detection of sustained deviations from a baseline.

Conventional electronics performs these operations through combinations of capacitors, resistors, operational amplifiers, digital counters, filters, and programmed processors.

An ideal electrical integrator is represented by

[
V_{\mathrm{out}}(t)

-\frac{1}{RC}
\int_0^t V_{\mathrm{in}}(s),ds,
]

for an ideal inverting operational-amplifier integrator.

A conventional leaky integrator may instead use an appropriate feedback network to produce an exponentially weighted history of the input.

These circuits are effective, but they generally represent temporal memory through a deliberately constructed electrical network.

Organic mixed ionic–electronic conductors introduce another possibility: the temporal state may be stored directly within the active material through ion penetration and electrochemical doping.

1.2 The proposed alternative

An organic electrochemical material can respond to an applied potential by admitting or expelling mobile ions.

Those ions may penetrate the active polymer volume and compensate electronic charges. The resulting electrochemical state modifies the material’s conductivity.

The sequence is

[
V_{\mathrm{in}}
\rightarrow
\text{ionic transport}
\rightarrow
\text{electrochemical doping}
\rightarrow
\text{conductivity change}
\rightarrow
\text{measurable output}.
]

The ionic state evolves more slowly than the applied voltage under suitable operating conditions.

Consequently, the material does not respond only to the voltage present at a given instant. It retains information about prior excitation.

This behavior provides the physical foundation for the Ionic Temporal Integrator.

1.3 Definition of the ITI

An Ionic Temporal Integrator is defined as an organic mixed-conduction element satisfying the following functional requirements:

1. An electrical input drives a mobile-ion redistribution process.
2. Ionic redistribution changes an electrochemical or doping state within the active material.
3. The internal state evolves over a measurable time interval.
4. The state depends on the history of the input.
5. The state can be read through an electrical or other measurable output.
6. The state exhibits a reproducible relaxation, retention, or reset process.
7. Its integration function is not supplied entirely by an external conventional RC circuit.

The ITI is therefore a material-state circuit element.

Its computational state is physical: it is represented by an ionic distribution and its associated electronic compensation.

1.4 Principal hypothesis

The central hypothesis is:

[
\boxed{
\text{Ionic redistribution in an organic mixed conductor can implement a controllable temporal integration kernel.}
}
]

The most useful initial implementation is expected to approximate a first-order leaky integrator.

A more advanced implementation may exhibit multiple characteristic relaxation times, nonlinear integration, adaptive memory, or programmable temporal kernels.

⸻

2. Scientific Foundations

2.1 Organic mixed ionic–electronic conductors

Organic mixed ionic–electronic conductors combine electronic transport through a conjugated molecular backbone with ionic transport through accessible pathways in the material.

The electronic subsystem supports charge transport through holes or electrons.

The ionic subsystem supports the redistribution of counterions, including cations and anions.

The two subsystems interact through electrostatic and electrochemical coupling.

A general electronic conductivity relation is

[
\sigma_e=q\mu_e n,
]

where:

* (q) is the elementary charge;
* (\mu_e) is electronic mobility;
* (n) is the mobile electronic carrier density.

In an organic material, the effective conductivity may also depend on morphology, molecular ordering, trap occupancy, doping fraction, hydration, and temperature:

[
\sigma_e

\sigma_e(n,z,m,c,T).
]

Here:

* (z) is electrochemical doping state;
* (m) is a molecular or morphological state;
* (c) is an ionic concentration.

This dependence creates the possibility of converting ionic state into electronic output.

2.2 Electrochemical doping

Consider a p-type conjugated polymer initially in a relatively neutral state.

An anion may enter the polymer to compensate a positively charged electronic state.

A schematic reaction is

[
P^0+Q^-
\rightleftharpoons
P^+Q^-+e^-.
]

The expression indicates that oxidation of the polymer produces a positive electronic charge compensated by an anion.

The exact reaction mechanism depends on the polymer, electrolyte, electrode potentials, and operating regime.

For an n-type material, the corresponding compensation process may involve cation penetration.

The resulting doping state changes the electronic carrier population and therefore the conductivity.

A simplified constitutive law is

[
\sigma_e=\sigma_0+\alpha_z z,
]

where (z) is a normalized doping fraction and (\alpha_z) is a material-dependent coefficient.

More generally,

[
\sigma_e=\sigma_e(z,T,m).
]

The ITI exploits the fact that (z) evolves over time.

2.3 Ion penetration

Let (c_i(\mathbf r,t)) represent the concentration of mobile ionic species (i).

For diffusion-dominated transport,

[
\mathbf J_i=-D_i\nabla c_i,
]

where (D_i) is the ionic diffusion coefficient.

If an electric field contributes significantly, the flux becomes

[
\mathbf J_i

-D_i\nabla c_i

\mu_i z_iq c_i\nabla\phi,
]

where:

* (\mu_i) is ionic mobility;
* (z_i) is ionic valence;
* (\phi) is electrostatic potential.

For a dilute ideal solution, the Nernst–Einstein relation connects mobility and diffusivity:

[
\mu_i=\frac{D_i}{k_{\mathrm B}T}.
]

The ionic continuity equation is

[
\boxed{
\frac{\partial c_i}{\partial t}

-\nabla\cdot\mathbf J_i+R_i
}
]

where (R_i) accounts for chemical reactions, ion exchange, or other local sources and sinks.

For a closed, nonreactive ionic subsystem,

[
R_i=0.
]

The ionic concentration is then governed by transport and boundary conditions.

2.4 Coupled electronic response

Ionic motion cannot generally be treated as an isolated diffusion problem because ionic charge must be compensated by electronic charge, electrostatic polarization, or chemical reactions.

A simplified charge-balance condition is

[
\rho_{\mathrm{ion}}+\rho_{\mathrm{electron}}+\rho_{\mathrm{fixed}}\approx0
]

in regions where local electroneutrality is a reasonable approximation.

Near interfaces, the full electrostatic problem may require Poisson’s equation:

[
-\nabla\cdot
\left(
\varepsilon\nabla\phi
\right)

\rho_{\mathrm{free}}.
]

The coupled ionic and electronic distributions determine the electrochemical state of the active polymer.

2.5 Chemical capacitance

A mixed conductor may store charge through changes in its internal electrochemical occupancy.

The differential chemical capacitance is

[
C_\mu

\frac{\partial Q}{\partial V_\mu},
]

where (V_\mu) is an appropriate electrochemical potential expressed in voltage units.

For a spatially distributed material,

[
C_\mu

\int_\Omega
c_\mu(\mathbf r),dV.
]

This chemical capacitance is an intrinsic material property associated with changes in carrier and redox occupancy.

It is not identical to an ordinary geometric capacitor, although it can contribute to an equivalent-circuit description.

The ITI therefore does not claim to eliminate capacitance from electrochemical physics. It proposes to use internal ionic and chemical state dynamics instead of relying on a conventional discrete capacitor-based integrator architecture.

⸻

3. Mathematical Definition of the Ionic Temporal Integrator

3.1 Minimal state equation

Let (x(t)) be a normalized internal state representing the effective ionic/electrochemical condition of the active material.

The proposed first-order model is

[
\boxed{
\tau\dot{x}+x=kV_{\mathrm{in}}.
}
\tag{1}
]

The parameters are:

[
\begin{aligned}
x(t)&:\text{ normalized material state},\
\tau&:\text{ effective ionic relaxation time},\
k&:\text{ voltage-to-state coupling coefficient},\
V_{\mathrm{in}}(t)&:\text{ applied electrical input}.
\end{aligned}
]

For a dimensionless (x), (k) has units of inverse voltage.

The equation can be written as

[
\dot{x}

-\frac{x}{\tau}
+
\frac{k}{\tau}V_{\mathrm{in}}.
]

The first term represents relaxation.

The second term represents input-driven state accumulation.

3.2 Solution for arbitrary input

Using the integrating-factor method,

[
\dot{x}+\frac{x}{\tau}

\frac{k}{\tau}V_{\mathrm{in}}(t).
]

Multiplication by (e^{t/\tau}) gives

[
\frac{d}{dt}
\left(
x e^{t/\tau}
\right)

\frac{k}{\tau}
e^{t/\tau}V_{\mathrm{in}}(t).
]

Integrating from (0) to (t),

[
x(t)e^{t/\tau}-x(0)

\frac{k}{\tau}
\int_0^t
e^{s/\tau}V_{\mathrm{in}}(s),ds.
]

Therefore,

[
\boxed{
x(t)

x(0)e^{-t/\tau}
+
\frac{k}{\tau}
\int_0^t
e^{-(t-s)/\tau}
V_{\mathrm{in}}(s),ds.
}
\tag{2}
]

This equation is the defining temporal response of the first-order ITI.

3.3 Temporal interpretation

The internal state is a weighted integral over the input history.

The weighting function is

[
K(t-s)

\frac{k}{\tau}e^{-(t-s)/\tau}.
]

Recent inputs receive greater weight than older inputs.

The characteristic memory horizon is controlled by (\tau).

For an input applied at time (s), its contribution to the state at time (t) decreases as

[
e^{-(t-s)/\tau}.
]

At one time constant,

[
e^{-1}\approx0.368.
]

At three time constants,

[
e^{-3}\approx0.050.
]

At five time constants,

[
e^{-5}\approx0.0067.
]

Thus, the material state progressively forgets earlier input.

3.4 Constant-voltage response

For

[
V_{\mathrm{in}}(t)=V_0,
]

with (x(0)=0),

[
\boxed{
x(t)=kV_0(1-e^{-t/\tau}).
}
\tag{3}
]

The state approaches

[
x_\infty=kV_0.
]

The response is initially approximately linear:

[
x(t)\approx\frac{kV_0}{\tau}t
]

when

[
t\ll\tau.
]

This early-time regime resembles ideal integration.

At longer times, relaxation becomes significant and the state approaches a finite equilibrium.

3.5 Pulse response

For a rectangular pulse

[
V_{\mathrm{in}}(t)

\begin{cases}
V_0,&0\leq t\leq T_p,\
0,&t>T_p,
\end{cases}
]

the state during the pulse is

[
x(t)

kV_0(1-e^{-t/\tau}).
]

At the end of the pulse,

[
x(T_p)

kV_0(1-e^{-T_p/\tau}).
]

After the pulse,

[
\boxed{
x(t)

kV_0
(1-e^{-T_p/\tau})
e^{-(t-T_p)/\tau}.
}
\tag{4}
]

This is a direct prediction of the ITI: the output rises during excitation and relaxes after the input is removed.

3.6 Pulse-pair accumulation

Consider two identical pulses separated by an interval (\Delta t).

Let the state immediately after the first pulse be (x_1).

After the interval,

[
x_{\mathrm{pre},2}

x_1e^{-\Delta t/\tau}.
]

The second pulse adds a new contribution.

For pulse duration (T_p),

[
x_2

x_1e^{-\Delta t/\tau}e^{-T_p/\tau}
+
kV_0(1-e^{-T_p/\tau}).
]

The state depends on the interval between pulses.

Closely spaced pulses accumulate more strongly than widely spaced pulses.

This provides a physically meaningful temporal coincidence function.

⸻

4. From Ionic Diffusion to the ITI Equation

The minimal equation must be derived from a physical transport model rather than introduced solely as a convenient mathematical approximation.

4.1 One-dimensional diffusion model

Consider an organic active layer occupying

[
0\leq z\leq d,
]

where (d) is the film thickness.

Let (c(z,t)) be the concentration of a mobile ionic species.

For diffusion-dominated transport,

[
\boxed{
\frac{\partial c}{\partial t}

D_{\mathrm{ion}}
\frac{\partial^2c}{\partial z^2}.
}
\tag{5}
]

The diffusion coefficient (D_{\mathrm{ion}}) is assumed constant in the simplest model.

The boundary at (z=0) is exposed to the electrolyte and can exchange ions with it.

The boundary at (z=d) is initially treated as blocking:

[
\left.
\frac{\partial c}{\partial z}
\right|_{z=d}=0.
]

The electrolyte boundary condition is determined by the applied electrochemical potential.

4.2 Equilibrium concentration

For small perturbations around a stable operating point, define

[
\delta c(z,t)=c(z,t)-c_0.
]

The equilibrium concentration at the electrolyte interface can be linearized as

[
\delta c(0,t)

\chi_V V_{\mathrm{in}}(t),
]

where (\chi_V) is an effective voltage-to-concentration coefficient.

This approximation assumes:

* Small input excursions.
* A fixed electrolyte composition.
* A stable operating temperature.
* Negligible irreversible side reactions.
* A locally linear electrochemical response.

For larger voltages, the equilibrium boundary relation must be replaced with a nonlinear electrochemical constitutive law.

4.3 Spatial eigenmodes

The diffusion equation can be separated into spatial and temporal components.

Let

[
\delta c(z,t)

\sum_{n=0}^{\infty}a_n(t)\psi_n(z).
]

The spatial functions satisfy an eigenvalue problem determined by the boundary conditions.

For a diffusion mode with eigenvalue (\lambda_n),

[
\dot a_n

-D_{\mathrm{ion}}\lambda_n^2a_n
+
b_nV_{\mathrm{in}}(t).
]

Thus,

[
\dot a_n+\frac{a_n}{\tau_n}

b_nV_{\mathrm{in}}(t),
]

where

[
\boxed{
\tau_n=
\frac{1}{D_{\mathrm{ion}}\lambda_n^2}.
}
\tag{6}
]

The ionic system therefore contains multiple relaxation modes.

The first-order ITI model is justified when one mode dominates the measured output over the operating bandwidth.

4.4 Dominant-mode approximation

If the first mode contributes much more strongly to the measured state than the remaining modes,

[
x(t)\approx a_1(t),
]

then

[
\dot x+\frac{x}{\tau_1}

b_1V_{\mathrm{in}}.
]

Multiplying by (\tau_1),

[
\boxed{
\tau_1\dot x+x=kV_{\mathrm{in}},
}
]

where

[
k=b_1\tau_1.
]

This derives the proposed ITI equation as a dominant-mode approximation to distributed ionic diffusion.

The approximation is not universally valid. It must be tested against measured transients and, where necessary, replaced by a multimode model.

4.5 Diffusion time scaling

A characteristic diffusion time is

[
\boxed{
\tau_D\sim\frac{d^2}{D_{\mathrm{ion}}}.
}
\tag{7}
]

The exact prefactor depends on boundary conditions and the definition of the measured mode.

For example, a particular slab eigenmode may have

[
\tau_1=\frac{4d^2}{\pi^2D_{\mathrm{ion}}},
]

but this expression must not be used indiscriminately for every geometry.

The important design result is the quadratic thickness dependence:

[
\tau_D\propto d^2.
]

Reducing active-layer thickness can substantially shorten the ionic response time.

4.6 Field-driven transport

If the applied field is sufficiently strong, drift must be retained.

The Nernst–Planck flux is

[
J

-D_{\mathrm{ion}}\frac{\partial c}{\partial z}

\mu_{\mathrm{ion}}z_iqc
\frac{\partial\phi}{\partial z}.
]

The governing equation becomes

[
\frac{\partial c}{\partial t}

-\frac{\partial J}{\partial z}.
]

The effective relaxation time can then depend on voltage, concentration, and device geometry.

Consequently,

[
\tau=\tau(V,c,d,T)
]

may be more accurate than treating (\tau) as a universal constant.

⸻

5. Electrochemical State and Conductivity Transduction

5.1 Definition of the electrochemical state

The ITI state should be connected to a measurable physical quantity.

One useful definition is a normalized average doping fraction:

[
x(t)

\frac{1}{c_{\max}d}
\int_0^d c_{\mathrm{dop}}(z,t),dz,
]

where (c_{\mathrm{dop}}) is the concentration of ions participating in charge compensation and (c_{\max}) is a normalization concentration.

This definition is appropriate only when the chosen ion concentration tracks the relevant electrochemical doping process.

If some ions are electrostatically accumulated without producing the assumed redox state, the state definition must be refined.

5.2 Conductivity relationship

For a simplified p-type material,

[
\sigma_p=q\mu_p p,
]

where (p) is the hole density.

If hole density depends on doping state,

[
p=p_0+\alpha_p x,
]

then

[
\sigma_p

q\mu_p(p_0+\alpha_p x).
]

Assuming constant mobility,

[
\boxed{
\sigma_p=\sigma_0+\alpha_\sigma x.
}
\tag{8}
]

This linear relationship is a first-order approximation.

In real organic mixed conductors, mobility can itself depend on doping, hydration, and morphology:

[
\mu_p=\mu_p(x,m,c,T).
]

A more complete relation is therefore

[
\sigma_p=\sigma_p(x,m,c,T).
]

5.3 Conductance readout

For a uniform channel of length (L), width (W), and thickness (d),

[
G(x)=\frac{W d}{L}\sigma_p(x).
]

Under the linear approximation,

[
G(x)=G_0+g_xx,
]

where

[
g_x=\frac{Wd}{L}\alpha_\sigma.
]

At a constant drain bias (V_{DS}),

[
I_D(t)

V_{DS}G(x(t)).
]

The output current is

[
\boxed{
I_D(t)

V_{DS}
\left[
G_0+g_xx(t)
\right].
}
\tag{9}
]

Subtracting the baseline current,

[
\Delta I_D(t)

V_{DS}g_xx(t).
]

Therefore,

[
\boxed{
x(t)

\frac{\Delta I_D(t)}
{V_{DS}g_x}.
}
\tag{10}
]

This provides an electrical readout of the internal integration state.

5.4 Alternative output variables

The ITI does not require conductance to be the only output.

Possible output observables include:

* Drain current.
* Channel conductance.
* Transconductance.
* Electrochromic optical absorption.
* Photoluminescence modulation.
* Electrochemical impedance.
* Open-circuit potential after controlled excitation.

The first implementation should favor a direct electrical output because it simplifies calibration and comparison.

⸻

6. Device Architecture

6.1 Proposed architecture

The recommended first-generation ITI is a three-terminal organic electrochemical transistor configured as an ionic integration element.

Its principal components are:

1. Source electrode.
2. Drain electrode.
3. Organic mixed-conductor channel.
4. Electrolyte layer.
5. Gate electrode.
6. Substrate.
7. Encapsulation and ion-access structure.

The gate voltage drives ionic penetration into the channel.

The source–drain path measures the resulting conductance change.

6.2 Functional separation

The device has two distinct electrical functions.

Input function: The gate controls the ionic state.

Output function: The source–drain channel converts that state into a measurable current.

This separation is important because it allows the ionic integration state to be read without requiring the same current path to supply the integration input.

6.3 Proposed geometry

A planar architecture is recommended for initial experiments.

The source and drain electrodes are patterned beneath or adjacent to the active polymer channel.

The electrolyte contacts the channel and gate electrode.

The active layer is exposed to ions through a controlled interface.

The principal geometric variables are:

[
L,\quad W,\quad d,
]

representing channel length, width, and active-layer thickness.

The initial design should permit independent variation of (d) while keeping the other dimensions approximately fixed.

This allows direct testing of the diffusion scaling law.

6.4 Candidate material families

Candidate active materials should be selected according to the desired polarity, ion compatibility, and electrochemical stability.

Possible material families include:

* PEDOT-based mixed conductors.
* Glycolated polythiophene derivatives.
* Polar-sidechain conjugated polymers.
* BBL-based organic electrochemical materials.
* Other p-type or n-type OMIECs with characterized ion uptake.

No single material is declared optimal.

The first material should be chosen for reproducibility and characterized ionic response rather than maximum transconductance alone.

6.5 Electrolyte selection

The electrolyte determines:

* Mobile-ion identity.
* Ionic conductivity.
* Ion activity.
* Electrochemical potential window.
* Hydration.
* Interfacial resistance.
* Swelling and stability.

The electrolyte should be selected to avoid irreversible redox reactions and uncontrolled degradation within the intended voltage range.

Ion size and polymer side-chain chemistry influence uptake, transport, swelling, and functional response.

The relationship between side-chain design and ion uptake is an important materials-engineering variable, not a secondary detail.

6.6 Architecture diagram

[
\begin{array}{c}
\text{Gate voltage }V_{\mathrm{in}}(t)\
\downarrow\
\text{Electrolyte / ionic reservoir}\
\downarrow\
\text{Ion penetration into OMIEC}\
\downarrow\
\text{Electrochemical doping state }x(t)\
\downarrow\
\text{Conductivity modulation}\
\downarrow\
\text{Source–drain readout}\
\downarrow\
\text{ITI output }y(t)
\end{array}
]

The material state is the computational memory.

The output stage measures that state.

⸻

7. ITI Transfer Function and Signal Processing

7.1 Laplace-domain response

Taking the Laplace transform of

[
\tau\dot x+x=kV_{\mathrm{in}},
]

with zero initial state gives

[
\tau sX(s)+X(s)=kV_{\mathrm{in}}(s).
]

Therefore,

[
\boxed{
H(s)

\frac{X(s)}{V_{\mathrm{in}}(s)}

\frac{k}{1+s\tau}.
}
\tag{11}
]

This is a first-order low-pass response.

It is also the transfer function of a leaky integrator.

7.2 Frequency response

For

[
s=j\omega,
]

[
H(j\omega)

\frac{k}{1+j\omega\tau}.
]

The magnitude is

[
|H(j\omega)|

\frac{|k|}
{\sqrt{1+\omega^2\tau^2}}.
]

The phase is

[
\angle H(j\omega)

-\tan^{-1}(\omega\tau)
]

for positive (k).

The characteristic corner frequency is

[
\boxed{
\omega_c=\frac{1}{\tau},
\qquad
f_c=\frac{1}{2\pi\tau}.
}
\tag{12}
]

The material therefore implements a temporal filter whose bandwidth is determined by ionic relaxation.

7.3 Low-frequency behavior

When

[
\omega\tau\ll1,
]

[
H(j\omega)\approx k.
]

The material follows slow inputs approximately quasi-statically.

7.4 High-frequency behavior

When

[
\omega\tau\gg1,
]

[
H(j\omega)\approx\frac{k}{j\omega\tau}.
]

The output magnitude decreases inversely with frequency.

The phase approaches (-90^\circ).

In this regime, the device behaves approximately as an integrator:

[
X(j\omega)\approx
\frac{k}{\tau}
\frac{V_{\mathrm{in}}(j\omega)}{j\omega}.
]

This approximation is valid only over a frequency interval in which the first-order model remains applicable.

7.5 Ideal integration limit

If the relaxation term is negligible over the measurement interval,

[
\frac{x}{\tau}\approx0,
]

then

[
\dot x\approx\frac{k}{\tau}V_{\mathrm{in}}.
]

Thus,

[
x(t)\approx x(0)+\frac{k}{\tau}
\int_0^tV_{\mathrm{in}}(s),ds.
]

The effective integration coefficient is

[
K_{\mathrm{ITI}}=\frac{k}{\tau}.
]

This is a finite-time approximation.

It does not imply that the physical device has become an ideal integrator at arbitrarily long times.

7.6 Why the ITI is not merely a low-pass filter

Mathematically, a first-order ITI and a conventional first-order low-pass filter may have identical transfer functions.

Their distinction is physical and architectural.

In a conventional filter, the state may be stored predominantly in a discrete capacitor.

In the ITI, the state is intended to be represented by ionic penetration and electrochemical doping within the active organic material.

This difference may matter for:

* Direct chemical sensing.
* Material-state memory.
* Integration with bioelectronic interfaces.
* Distributed temporal processing.
* Flexible and conformable devices.
* Physical integration with other organic circuit primitives.

The distinction must be demonstrated experimentally, not inferred from the transfer function alone.

⸻

8. Multiple Ionic Relaxation Times

8.1 Why one time constant may be insufficient

A real organic film is spatially distributed.

Ions can experience different transport distances, local environments, energetic barriers, and polymer morphologies.

The measured response may therefore contain several relaxation modes.

A generalized model is

[
x(t)=\sum_{n=1}^{N}x_n(t),
]

with

[
\tau_n\dot x_n+x_n=k_nV_{\mathrm{in}}.
]

The transfer function becomes

[
\boxed{
H(s)=
\sum_{n=1}^{N}
\frac{k_n}{1+s\tau_n}.
}
\tag{13}
]

This produces a multi-timescale temporal integrator.

8.2 Continuous relaxation spectrum

A more general representation is

[
x(t)

\int_0^\infty x_\tau(t),d\mu(\tau),
]

where (d\mu(\tau)) represents the distribution of relaxation strengths.

The transfer function is

[
H(s)

\int_0^\infty
\frac{d\mu(\tau)}{1+s\tau}.
]

This formulation can represent broad relaxation spectra.

8.3 Physical interpretation

A fast ionic population may contribute short-term memory.

A slower population may contribute longer-term memory.

A distribution of ionic pathways may therefore provide a naturally multi-timescale integration kernel.

This is potentially useful for temporal signal classification, but it introduces a more difficult calibration problem.

8.4 Proposed ITI classes

The following classes are proposed for research classification:

Class	Internal dynamics	Intended function
ITI-1	Single dominant relaxation	First-order leaky integration
ITI-2	Two or more discrete modes	Multi-timescale integration
ITI-3	Broad relaxation spectrum	Distributed temporal memory
ITI-4	Nonlinear ionic kinetics	Amplitude-dependent integration
ITI-5	Programmable ionic relaxation	Adjustable temporal window
ITI-6	Persistent electrochemical state	Long-duration accumulation

These are proposed device classes, not established industry categories.

⸻

9. Nonlinear Ionic Temporal Integration

9.1 Limitations of the linear model

The first-order equation assumes that the state responds linearly to voltage.

Real organic electrochemical systems may exhibit:

* Voltage-dependent ion uptake.
* Concentration-dependent diffusion.
* Nonlinear electrochemical potentials.
* Mobility variation.
* Saturation of available doping sites.
* Asymmetric insertion and extraction.
* Morphological changes.
* Hysteresis.

A more general ITI model is

[
\dot x

F(x,V_{\mathrm{in}},T).
]

9.2 Saturating integration model

A simple saturating model is

[
\dot x

aV_{\mathrm{in}}(1-x)

bx.
]

Here (0\leq x\leq1).

The first term describes voltage-dependent state accumulation into available sites.

The second term represents relaxation.

For constant (V_{\mathrm{in}}=V_0), the equilibrium is

[
x_\infty

\frac{aV_0}{aV_0+b}.
]

The effective time constant is

[
\tau_{\mathrm{eff}}

\frac{1}{aV_0+b}.
]

Unlike the linear model, the response time depends on input amplitude.

9.3 Asymmetric insertion and extraction

The ionic insertion process may differ from extraction.

A piecewise model is

[
\dot x=
\begin{cases}
a_+(V)(1-x)-b_+x,&V>0,\
a_-(V)(1-x)-b_-x,&V<0.
\end{cases}
]

This can produce different charging and recovery time constants.

The asymmetry may be useful for directional event processing but may also complicate reset and calibration.

9.4 Nonlinear temporal kernel

For nonlinear systems, a single convolution kernel is generally insufficient.

The response depends on the trajectory of the internal state.

The ITI should then be described through its state-transition operator:

[
x(t)

\mathcal T
\left[
x(0),V_{\mathrm{in}}(0:t)
\right].
]

The linear convolution model remains the reference model for initial device development.

⸻

10. Operating Modes

The ITI should be designed around an explicit operating regime.

10.1 Mode A: Leaky integration

The normal first-order mode is

[
\tau\dot x+x=kV_{\mathrm{in}}.
]

It provides finite memory and controlled relaxation.

Applications include:

* Event accumulation.
* Pulse-pair detection.
* Temporal filtering.
* Sensory preprocessing.

10.2 Mode B: Quasi-ideal integration

For a time interval much shorter than the relaxation time,

[
t_{\mathrm{op}}\ll\tau,
]

the state approximately satisfies

[
x(t)-x(0)
\approx
\frac{k}{\tau}
\int_0^tV_{\mathrm{in}}(s),ds.
]

This is the closest ITI operating regime to ideal analog integration.

The usable duration is bounded by state saturation and drift.

10.3 Mode C: Persistent electrochemical memory

If ions remain trapped or energetically stabilized after the input is removed, the relaxation time may become very long.

The device may then behave as a memory element.

However, persistent retention can undermine rapid temporal integration if the state cannot be reset reproducibly.

A useful ITI should distinguish intended finite memory from unwanted irreversible trapping.

10.4 Mode D: Adaptive integration

If the relaxation time or coupling coefficient depends on a secondary control variable,

[
\tau=\tau(u_c),
\qquad
k=k(u_c),
]

the temporal integration window becomes programmable.

Possible control variables include:

* Gate bias.
* Electrolyte composition.
* Temperature.
* A secondary ionic input.
* A controlled chemical environment.

This mode is a proposed extension beyond the minimum ITI.

⸻

11. Circuit-Level Applications

11.1 Pulse accumulation

The ITI can accumulate a series of electrical pulses.

Each pulse increases the internal state, while the interval between pulses determines how much state is lost before the next event.

This permits a threshold decision based on cumulative stimulation.

11.2 Duration discrimination

A short pulse and a long pulse with the same amplitude produce different maximum states.

The ITI can therefore distinguish duration without a separate digital timer.

11.3 Temporal coincidence

Two input channels may each contribute to a shared ionic state.

A threshold output occurs only when the inputs arrive within a suitable time interval.

For two inputs,

[
\tau\dot x+x=k_1V_1+k_2V_2.
]

The output can be defined by

[
Y=H(x-x_{\mathrm{th}}).
]

The resulting device implements a weighted temporal coincidence operation.

11.4 Event-rate detection

For a train of pulses, the average state depends on pulse amplitude, duration, repetition rate, and relaxation time.

A sufficiently high event rate maintains a larger average state than a low event rate.

This creates an analog event-rate detector.

11.5 Biological signal integration

An ITI may be useful in interfaces that receive slow or transient biological signals.

The device can integrate ionic or electrical events directly within an organic mixed conductor.

The potential advantage is close coupling between sensing and temporal processing.

11.6 Chemical event accumulation

If a chemical event changes the ionic or electrochemical state, the ITI can potentially integrate repeated chemical exposure.

This requires a chemically selective input mechanism and should be treated as an extension of the electrical-input ITI.

⸻

12. Materials Engineering

12.1 Material requirements

The ideal ITI material should provide:

1. Reversible ion penetration.
2. Stable electronic transport.
3. A reproducible doping–conductivity relationship.
4. A tunable ionic diffusion coefficient.
5. Low irreversible chemical degradation.
6. Controlled swelling.
7. Low device-to-device variability.
8. A useful operating voltage window.
9. A measurable relaxation time.
10. Compatibility with a stable electrolyte.

12.2 Side-chain engineering

Polymer side chains influence ion uptake and transport.

Hydrophilic and glycolated side chains may facilitate ionic access.

However, increased ion uptake can also alter morphology, swelling, and electronic mobility.

The design objective is not maximum ionic uptake.

It is controlled ionic access with reproducible state evolution.

12.3 Morphological control

The polymer morphology determines the distribution of ionic and electronic pathways.

Crystalline and amorphous regions may provide different transport barriers.

The ionic response may depend on:

* Domain size.
* Crystallinity.
* Chain orientation.
* Side-chain packing.
* Film porosity.
* Hydration.
* Processing history.

The ITI requires morphology to be treated as a design variable.

12.4 Electrolyte and ion selection

The ion species determines transport speed and interaction with the polymer.

Relevant parameters include:

[
D_{\mathrm{ion}},
\quad
z_i,
\quad
r_i,
\quad
\gamma_i,
\quad
\Delta G_{\mathrm{insertion}},
]

where (r_i) is an effective ionic size, (\gamma_i) represents activity effects, and (\Delta G_{\mathrm{insertion}}) is the insertion free-energy change.

The choice of ion should balance response speed, retention, reversibility, and stability.

12.5 Temperature dependence

The ionic diffusion coefficient may follow an Arrhenius-like relation:

[
D_{\mathrm{ion}}(T)

D_0
\exp\left(
-\frac{E_a}{k_{\mathrm B}T}
\right).
]

Consequently,

[
\tau_D(T)
\sim
\frac{d^2}{D_0}
\exp\left(
\frac{E_a}{k_{\mathrm B}T}
\right).
]

The ITI time constant may therefore vary significantly with temperature.

Temperature compensation or calibration may be required for precision applications.

⸻

13. Device Fabrication Strategy

13.1 Initial prototype

The first prototype should use a planar organic electrochemical transistor geometry.

A suitable fabrication sequence is:

1. Prepare a clean glass or flexible polymer substrate.
2. Pattern source and drain electrodes.
3. Deposit or pattern the organic mixed-conductor channel.
4. Apply a controlled electrolyte layer.
5. Integrate a gate electrode.
6. Define the active ion-access area.
7. Encapsulate regions not intended for ionic exposure.
8. Connect electrical terminals for independent input and output measurement.

13.2 Geometric design variables

The primary variables are:

Parameter	Function
(L)	Electronic channel length
(W)	Channel width
(d)	Active organic thickness
(A_g)	Gate area
(A_{\mathrm{ion}})	Effective ionic access area
(t_{\mathrm{electrolyte}})	Electrolyte thickness
(r_{\mathrm{contact}})	Effective contact resistance

The initial experimental series should vary active-layer thickness while maintaining approximately constant channel length and width.

This is necessary to test the predicted diffusion-time dependence.

13.3 Patterning methods

Potential fabrication methods include:

* Spin coating.
* Blade coating.
* Inkjet printing.
* Screen printing.
* Photolithography.
* Shadow-mask deposition.
* Aerosol-jet printing.

The selected process must preserve the active material’s ionic and electronic properties.

13.4 Encapsulation

Encapsulation should protect the device from uncontrolled oxygen, water, and contamination.

However, the electrolyte and ion-access regions must remain functional.

A practical ITI may therefore require selective encapsulation rather than complete isolation.

13.5 Fabrication controls

At least three control structures should be fabricated:

Control A: An otherwise comparable device with a blocking layer that suppresses ion penetration.

Control B: A conventional electronic channel without the intended electrochemical coupling.

Control C: A geometrically matched passive structure used to characterize parasitic capacitance and leakage.

These controls are essential for determining whether the integration behavior originates from the intended ionic process.

⸻

14. Readout Architecture

14.1 Continuous electrical readout

A constant source–drain voltage is applied:

[
V_{DS}=V_{\mathrm{read}}.
]

The output current is

[
I_{\mathrm{out}}(t)

G[x(t)]V_{\mathrm{read}}.
]

This configuration provides continuous monitoring.

The read voltage should be sufficiently small that it does not significantly disturb the ionic state.

14.2 Pulsed readout

An alternative is to apply short read pulses after the input integration interval.

This reduces continuous electrical loading.

The tradeoff is reduced temporal resolution.

14.3 Differential readout

A reference organic channel may be operated without the integration input.

The output difference is

[
\Delta I(t)

I_{\mathrm{ITI}}(t)-I_{\mathrm{ref}}(t).
]

This can help suppress common-mode temperature drift and baseline variation.

14.4 State calibration

The measured current should be mapped to an estimated internal state.

For a locally linear conductance relation,

[
\hat x(t)

\frac{I_{\mathrm{out}}(t)-I_0}
{V_{\mathrm{read}}g_x}.
]

The calibration must be repeated if mobility, morphology, or electrochemical state changes alter (g_x).

⸻

15. Energy and Thermodynamic Analysis

15.1 Input energy

The electrical energy supplied at the gate is

[
E_{\mathrm{in}}

\int_{t_0}^{t_1}
V_g(t)I_g(t),dt.
]

The readout energy is

[
E_{\mathrm{read}}

\int_{t_0}^{t_1}
V_{DS}(t)I_D(t),dt.
]

The total operating energy must include both input and readout processes.

If an external amplifier or instrumentation circuit performs part of the integration, its energy must also be included in system-level comparisons.

15.2 Electrochemical free energy

The internal ionic state may store electrochemical free energy.

A schematic free-energy functional is

[
\mathcal F[c]

\int_\Omega
\left[
f_{\mathrm{chem}}(c)
+
\frac{\varepsilon}{2}|\nabla\phi|^2
\right]dV.
]

The first term describes chemical free energy.

The second represents electrostatic energy.

A complete model may also require polymer deformation, mixing, and redox contributions.

15.3 Dissipation

Ion transport dissipates energy through irreversible flux.

In a simplified diffusion model, the entropy-production contribution is proportional to

[
T\dot S_{\mathrm{prod}}
\sim
\int_\Omega
\frac{D_{\mathrm{ion}}c}{k_{\mathrm B}T}
|\nabla\mu_{\mathrm{ion}}|^2,dV,
]

under the corresponding idealized constitutive assumptions.

The exact expression depends on the thermodynamic model.

15.4 No free computation

The ITI does not create energy or information without physical cost.

Its advantage, if established, would arise from integrating temporal storage and signal processing into the active material rather than requiring a separate conventional integration network.

The energy comparison must be performed against a conventional circuit implementing the same transfer function and output load.

⸻

16. Noise and Uncertainty

16.1 Ionic concentration fluctuations

The ionic state is subject to stochastic fluctuations.

A simplified stochastic model is

[
\tau\dot x+x

kV_{\mathrm{in}}+\xi(t),
]

where (\xi(t)) represents effective state noise.

16.2 Output noise

If the output is

[
I_{\mathrm{out}}=G(x)V_{\mathrm{read}},
]

then small fluctuations produce

[
\delta I
\approx
V_{\mathrm{read}}
\frac{dG}{dx}\delta x.
]

The output noise depends on both the material-state noise and the sensitivity of conductance to the state.

16.3 State covariance

For a linear stochastic model,

[
\dot{\delta x}

-\frac{1}{\tau}\delta x+\eta(t),
]

the stationary variance depends on the noise intensity and relaxation time.

For white noise with

[
\langle\eta(t)\eta(t’)\rangle

Q\delta(t-t’),
]

the stationary variance is

[
\operatorname{Var}(x)

\frac{Q\tau}{2}
]

under this particular noise normalization.

A longer time constant can therefore increase accumulated low-frequency state fluctuations.

16.4 Signal-to-noise requirement

A practical ITI should provide a state separation substantially larger than the state uncertainty.

For two distinguishable levels (x_0) and (x_1), a useful measure is

[
\mathrm{SNR}_x

\frac{|x_1-x_0|}
{\sqrt{\sigma_{x_0}^2+\sigma_{x_1}^2}}.
]

The acceptable value depends on the intended application and decision error rate.

⸻

17. Stability and Reliability

17.1 Small-signal stability

For the linear ITI,

[
\dot x

-\frac{x}{\tau}
+
\frac{k}{\tau}V_{\mathrm{in}},
]

the homogeneous solution is

[
x_h(t)=x(0)e^{-t/\tau}.
]

The system is asymptotically stable when

[
\tau>0.
]

17.2 Nonlinear stability

For a nonlinear model,

[
\dot x=F(x,V),
]

an equilibrium (x_0) satisfies

[
F(x_0,V_0)=0.
]

Local stability requires

[
\left.
\frac{\partial F}{\partial x}
\right|_{x_0,V_0}<0.
]

17.3 Degradation mechanisms

Potential failure mechanisms include:

* Irreversible oxidation or reduction.
* Polymer chain degradation.
* Electrolyte decomposition.
* Ion trapping.
* Delamination.
* Swelling-induced mechanical damage.
* Contact corrosion.
* Morphological drift.
* Uncontrolled hydration.

17.4 Reliability metrics

The ITI should be characterized by:

* Repeated pulse-response stability.
* Time-constant drift.
* State retention.
* Reset reproducibility.
* Device-to-device variation.
* Endurance.
* Environmental stability.
* Baseline conductance drift.

⸻

18. Distinguishing the ITI from Conventional RC Integration

This is the central experimental and conceptual challenge.

18.1 Mathematical equivalence

The first-order ITI equation has the same mathematical form as an ordinary RC low-pass circuit.

Therefore, observing an exponential transient is not sufficient evidence of a new circuit primitive.

18.2 Physical distinction

The proposed ITI differs through its state variable.

In a conventional RC circuit, the primary state is capacitor charge or voltage.

In the ITI, the primary state is intended to be a distributed ionic/electrochemical configuration.

The distinction must be supported by independent evidence.

18.3 Required evidence

A credible demonstration should establish:

1. The active material admits or redistributes ions under the applied input.
2. The internal ionic state changes with time.
3. The electrochemical state correlates with the output.
4. The response time changes with ion-transport parameters.
5. Blocking ion penetration substantially changes or suppresses the intended integration response.
6. The response is not explained by parasitic capacitance alone.
7. The behavior remains reproducible after repeated cycles.

18.4 Thickness scaling experiment

Because diffusion time scales approximately as

[
\tau_D\propto d^2,
]

fabricate devices with several active-layer thicknesses.

Measure their relaxation times.

Fit

[
\tau(d)=\tau_0+\alpha d^2.
]

A positive, reproducible (d^2) dependence supports a diffusion-limited interpretation.

The intercept (\tau_0) may represent interfacial, electrolyte, or measurement-system contributions.

Failure to observe the expected scaling does not necessarily disprove ionic involvement, but it weakens the simplest bulk-diffusion model.

18.5 Ion-blocking experiment

Introduce a control structure that suppresses ion penetration while preserving as much of the electronic geometry as possible.

If the integration behavior remains unchanged, the claim that ion penetration is the primary mechanism requires revision.

18.6 Operando characterization

The most convincing validation combines electrical measurements with a direct or indirect measurement of internal ionic state.

Candidate methods include:

* Electrochemical impedance spectroscopy.
* Operando optical spectroscopy.
* Spectroelectrochemical measurements.
* X-ray-based ion or chemical-state characterization.
* Neutron or isotope-sensitive methods where appropriate.
* In situ structural characterization.
* Spatially resolved potential or concentration mapping.

The technique must be chosen according to the material and electrolyte.

⸻

19. Experimental Research Program

19.1 Experiment 1: Baseline electrochemical characterization

Measure:

* Current–voltage response.
* Gate leakage.
* Conductance modulation.
* Electrochemical stability window.
* Baseline drift.
* Electrochemical impedance.

Determine the safe operating range before temporal integration testing.

19.2 Experiment 2: Step response

Apply a voltage step and measure the output over time.

Fit the measured state to

[
x(t)=x_\infty+(x_0-x_\infty)e^{-t/\tau}.
]

Extract:

* (x_\infty).
* (\tau).
* Input sensitivity.
* Rise time.
* Recovery time.

Repeat across multiple input amplitudes.

19.3 Experiment 3: Pulse-width dependence

Apply rectangular pulses with varying duration.

Measure the peak state:

[
x_{\max}(T_p)

kV_0(1-e^{-T_p/\tau})
]

under the linear model.

Plot the measured peak state against pulse duration.

A reproducible saturating curve supports the first-order leaky-integrator model.

19.4 Experiment 4: Pulse-spacing dependence

Apply two identical pulses separated by variable (\Delta t).

Measure the residual state before the second pulse.

The model predicts

[
x_{\mathrm{residual}}(\Delta t)

x_1e^{-\Delta t/\tau}.
]

The extracted relaxation time should agree with the step-response measurement within the limits of the model and experimental uncertainty.

19.5 Experiment 5: Frequency response

Apply a sinusoidal input:

[
V_{\mathrm{in}}(t)=V_0\sin(\omega t).
]

Measure amplitude and phase.

Compare the results with

[
|H(j\omega)|

\frac{|k|}
{\sqrt{1+\omega^2\tau^2}}
]

and

[
\phi(\omega)

-\tan^{-1}(\omega\tau).
]

Deviations may reveal multiple relaxation modes or nonlinear transport.

19.6 Experiment 6: Thickness dependence

Fabricate multiple active-layer thicknesses.

Determine whether the dominant response time follows

[
\tau\propto d^2.
]

This experiment is central to connecting the ITI state equation to ionic diffusion.

19.7 Experiment 7: Ion-species dependence

Change the electrolyte ion species while controlling other parameters as closely as possible.

Measure changes in:

* Uptake.
* Diffusion response.
* Relaxation.
* Conductance sensitivity.
* Hysteresis.
* Stability.

19.8 Experiment 8: Temperature dependence

Measure the time constant at multiple temperatures.

Fit an Arrhenius-like relation where justified:

[
\ln\tau

\ln\tau_0+\frac{E_a}{k_{\mathrm B}T}.
]

Extract an effective activation energy.

19.9 Experiment 9: Read disturbance

Compare continuous readout with pulsed readout.

Determine whether the source–drain bias changes the stored ionic state.

19.10 Experiment 10: Repeated-cycle endurance

Apply repeated write–relax–read sequences.

Measure changes in:

* Baseline conductance.
* Integration gain.
* Time constant.
* Maximum state.
* Reset efficiency.
* Output variability.

⸻

20. Prototype Design: ITI-1

20.1 Objective

ITI-1 is the first proposed physical implementation.

Its purpose is to demonstrate first-order leaky integration through ionic penetration and electrochemical doping.

It is not intended initially to optimize speed, density, or energy efficiency.

The primary objective is mechanism validation.

20.2 Functional architecture

ITI-1 contains:

* One organic mixed-conductor channel.
* One electrolyte region.
* One gate electrode.
* One source electrode.
* One drain electrode.
* A controlled ionic access boundary.
* A low-disturbance readout path.

20.3 Operating sequence

Initialization

Apply a controlled reset condition to establish the baseline state.

Integration

Apply the input voltage waveform to the gate.

State evolution

Allow ions to penetrate and alter the electrochemical doping state.

Readout

Measure source–drain conductance at a low read bias.

Relaxation

Remove the input and measure the recovery trajectory.

Reset

Apply a defined reverse or recovery protocol if passive relaxation is insufficient.

20.4 Minimum demonstrator output

The first demonstrator should show:

1. A reproducible voltage-step response.
2. A measurable relaxation time.
3. Pulse-width-dependent state accumulation.
4. Pulse-spacing-dependent memory.
5. A conductance output correlated with the internal electrochemical state.
6. A response that changes when ion penetration is inhibited.

20.5 Proposed engineering targets

The following are initial design targets for experimental planning, not established performance results or guaranteed material capabilities.

Parameter	Initial target
Operating input	Low-voltage electrochemical window
Active state	Reversible ionic/doping fraction
Dominant dynamics	Approximately single-exponential
Integration mode	Leaky
Readout	Source–drain conductance
Reset	Reproducible passive or active recovery
Endurance objective	At least (10^3) initial cycles
Device population	Multiple devices across multiple fabrication batches
Mechanism validation	Ionic-state correlation and ion-blocking controls

The numerical endurance target is a proposed first screening criterion, not a prediction of achieved performance.

⸻

21. System Integration

21.1 ITI as an Organic Circuit Primitive

Once validated, the ITI can be represented as a reusable element within Organic Circuit Theory.

Its functional symbol is

[
\boxed{
\mathrm{ITI}:
V_{\mathrm{in}}(t)
\longrightarrow
x(t)
\longrightarrow
y(t).
}
]

The internal state is electrochemical.

The output is electrical or otherwise measurable.

21.2 ITI threshold element

Coupling the ITI to a threshold device gives

[
Y=
H(x-x_{\mathrm{th}}).
]

This produces a duration-sensitive event detector.

21.3 ITI memory element

If the relaxation time is sufficiently long,

[
\tau\gg t_{\mathrm{operation}},
]

the ITI can function as a short-term material-state memory.

21.4 ITI adaptive circuit

A second input may control the time constant:

[
\tau=\tau(u_c).
]

The temporal window can then be adjusted dynamically.

21.5 ITI network

For multiple interconnected integrators,

[
\tau_i\dot x_i+x_i

\sum_jk_{ij}u_j.
]

This provides a network of coupled temporal states.

The coefficients (k_{ij}) may be determined by electrical coupling, ionic coupling, or other controlled physical interactions.

A large network could implement temporal filtering, event accumulation, and distributed signal processing.

⸻

22. Performance Metrics

A complete ITI characterization should report the following.

22.1 Temporal metrics

* Integration time constant.
* Relaxation time.
* Pulse-width sensitivity.
* Pulse-spacing sensitivity.
* Effective memory horizon.
* Frequency response.
* Temporal resolution.

22.2 Electrochemical metrics

* Ionic diffusion coefficient.
* Chemical capacitance.
* Electrochemical doping range.
* Ion uptake.
* Electrochemical reversibility.
* Hysteresis.
* Leakage.
* Swelling.

22.3 Electrical metrics

* Baseline conductance.
* Conductance modulation.
* Transconductance.
* Read current.
* Noise.
* Read disturbance.
* Operating voltage.

22.4 Reliability metrics

* Endurance.
* State drift.
* Reset efficiency.
* Environmental sensitivity.
* Device-to-device variation.
* Batch reproducibility.

22.5 Energy metrics

* Input energy per pulse.
* Energy per integration event.
* Readout energy.
* Reset energy.
* Total energy per useful operation.

A fair benchmark must include the energy of all supporting circuitry.

⸻

23. Novelty Assessment

23.1 Established scientific foundations

The following phenomena are established research areas:

* Organic mixed ionic–electronic conduction.
* Electrochemical doping of conjugated polymers.
* Ion penetration into organic electrochemical transistor channels.
* Ionic diffusion-limited transients.
* Chemical capacitance.
* History-dependent conductance.
* Organic electrochemical memory.
* Neuromorphic integration and synaptic response.
* Multi-timescale ionic relaxation.

Organic electrochemical transistors already use ion penetration and electrochemical doping to modulate channel conductivity.

Studies of transient OECT behavior have shown that the measured response can depend on ionic diffusion, chemical capacitance, external ionic resistance, electronic transport, and device geometry.

Organic electrochemical devices have also demonstrated memory, synaptic behavior, and neuron-like temporal processing.

Therefore, it would be inaccurate to claim that ionic temporal integration as a physical phenomenon is entirely undiscovered.

23.2 Proposed contribution

The proposed contribution of the ITI is the explicit definition of a dedicated circuit element whose intended function is:

[
\text{electrical input history}
\rightarrow
\text{ionic/electrochemical state}
\rightarrow
\text{analog integrated output}.
]

The framework establishes:

1. A specific material-state definition.
2. A first-order integration equation.
3. A physical diffusion-based derivation.
4. A distinction between leaky and ideal integration.
5. A device architecture optimized for integration rather than general transistor operation.
6. A validation protocol designed to distinguish ionic integration from ordinary RC behavior.
7. A proposed interface for composing the ITI with other organic circuit primitives.

23.3 Novelty classification

Claim	Assessment
Ion penetration into OMIEC materials	Established
Electrochemical doping changes conductivity	Established
OECT transient response depends on ionic dynamics	Established
Ionic history-dependent conductance	Established
Organic electrochemical memory	Established
First-order leaky-integrator behavior in an ionic material	Physically supported and closely related to established transient dynamics
ITI as a dedicated, calibrated circuit primitive	Proposed formalization
ITI device architecture optimized specifically for analog temporal integration	Proposed
Demonstration of intrinsic integration independent of external RC processing	Unresolved experimental objective
Multi-timescale programmable ITI	Proposed extension

23.4 The unresolved novelty question

The critical question is not whether an organic electrochemical transistor has a transient response.

It is whether a deliberately engineered device can provide a stable, reproducible, and useful integration operation in which the dominant memory state is the controlled ionic/electrochemical configuration of the active material.

That is the research claim requiring direct experimental validation.

⸻

24. Falsifiability

The ITI hypothesis must be exposed to experiments capable of rejecting it.

24.1 Falsification condition A: No ionic dependence

If blocking ion penetration does not materially alter the integration response, the proposed ionic mechanism is not established.

24.2 Falsification condition B: Conventional RC explanation

If a matched passive RC model explains the entire measured response and no independent ionic state is demonstrated, the device has not established a distinct material-state integrator.

24.3 Falsification condition C: No state–output correspondence

If ionic-state measurements do not correlate with the measured output, the proposed state variable is incomplete or incorrect.

24.4 Falsification condition D: Irreversible degradation

If the apparent accumulation is caused primarily by irreversible chemical damage, the device is not a reproducible temporal integrator.

24.5 Falsification condition E: Uncontrolled variability

If the integration time constant and input sensitivity cannot be calibrated reproducibly across devices, the proposed primitive is not yet suitable for circuit composition.

24.6 Falsification condition F: No functional advantage

If the device offers no useful advantage over a conventional integrator for its intended application, the architecture may remain scientifically interesting but lack a practical rationale.

⸻

25. Principal Technical Obstacles

25.1 Distributed rather than lumped dynamics

Ionic transport is spatially distributed.

The first-order equation may not capture all modes.

A multimode model may be necessary.

25.2 Drift and baseline instability

Changes in hydration, oxygen exposure, and morphology may shift the baseline conductance.

25.3 State saturation

Finite doping capacity limits the accumulated state.

25.4 Asymmetric relaxation

Insertion and extraction may have different kinetics.

25.5 Electrochemical side reactions

Irreversible reactions may contaminate the intended state evolution.

25.6 Readout disturbance

The measurement current may alter the state being measured.

25.7 Device variability

Polymer morphology and ionic pathways can vary between nominally identical devices.

25.8 Temperature dependence

Ionic mobility and electrochemical kinetics may change significantly with temperature.

25.9 Integration and reset tradeoff

Long retention increases the memory horizon but may make rapid reset difficult.

The design must balance accumulation, relaxation, and reversibility.

⸻

26. Research Roadmap

Phase I — Physical characterization

Establish the material’s ionic transport, electrochemical doping, and conductivity response.

Deliverable: A validated coupled ionic–electronic transport model.

Phase II — First-order ITI demonstration

Demonstrate a reproducible voltage-step response and fit the first-order state equation.

Deliverable: A measured (\tau), (k), and state–conductance relationship.

Phase III — Temporal operation

Demonstrate pulse-width discrimination, pulse accumulation, and pulse-spacing dependence.

Deliverable: A calibrated temporal integration element.

Phase IV — Mechanism discrimination

Perform ion-blocking, thickness-scaling, impedance, and operando characterization.

Deliverable: Evidence that ionic/electrochemical state evolution is the dominant physical mechanism.

Phase V — Programmable integration

Develop control over the integration time constant and state sensitivity.

Deliverable: An adjustable temporal window.

Phase VI — Circuit composition

Connect the ITI to an organic threshold element or molecular memory device.

Deliverable: An integrated organic temporal computation circuit.

Phase VII — Benchmarking

Compare the device against conventional analog integrators and digital temporal-processing systems.

Deliverable: A quantified performance assessment.

⸻

27. Proposed Research Predictions

The following predictions are derived from the proposed model and should be tested experimentally.

Prediction 1: Pulse-width dependence

For fixed pulse amplitude,

[
x_{\max}(T_p)

kV_0(1-e^{-T_p/\tau}).
]

The peak state should increase monotonically with pulse duration and approach a saturation value.

Prediction 2: Pulse-spacing dependence

For a residual state,

[
x_{\mathrm{residual}}(\Delta t)

x_0e^{-\Delta t/\tau}.
]

The residual contribution should decay exponentially in the first-order regime.

Prediction 3: Thickness dependence

For diffusion-limited response,

[
\tau\propto d^2.
]

The dominant time constant should increase with the square of active-layer thickness, subject to interfacial and transport corrections.

Prediction 4: Frequency response

The first-order regime should exhibit a corner frequency near

[
f_c=\frac{1}{2\pi\tau}.
]

Prediction 5: Ion-dependent relaxation

Changing the ionic species or electrolyte should alter the relaxation response when ionic transport is rate limiting.

Prediction 6: Temperature dependence

The time constant should exhibit a systematic temperature dependence consistent with the measured transport mechanism.

Prediction 7: State–conductance correlation

The conductance response should correlate reproducibly with the electrochemical state.

Prediction 8: Ion-blocking sensitivity

Suppressing ion penetration should substantially reduce or alter the intended integration behavior.

⸻

28. Discussion: What Would Constitute a Genuine ITI Discovery?

A transient response is not automatically a circuit primitive.

A hysteretic current curve is not automatically temporal integration.

A device that retains a previous voltage state is not necessarily an integrator.

To establish the ITI as a distinct and useful organic circuit element, the experiment must demonstrate a sequence of increasingly demanding results.

First, the device must show that an input produces a measurable internal ionic state.

Second, that state must follow a predictable temporal law.

Third, the state must be readable through an output variable.

Fourth, its dependence on pulse amplitude, duration, spacing, and frequency must agree with a physical model.

Fifth, the integration must be attributable to the material rather than to an external passive network.

Finally, the element must perform a useful operation when connected to another circuit component.

The distinction between a material response and a computational primitive is crucial.

A material may have a complex transient response without being a useful integrator.

An ITI must provide a controllable and repeatable temporal transformation.

The first-order equation is therefore not the final theory. It is the minimum model against which the physical device should be tested.

If the measured behavior requires multiple modes, nonlinear kinetics, or spatially distributed state variables, the theory should be expanded rather than forcing the data into an inadequate exponential model.

⸻

29. Conclusions

The Ionic Temporal Integrator is proposed as an organic material-state circuit element that performs temporal integration through ionic penetration and electrochemical doping.

Its central equation is

[
\boxed{
\tau\dot{x}+x=kV_{\mathrm{in}}.
}
]

This equation describes a leaky integrator whose output represents an exponentially weighted history of the input.

The physical foundation is the coupling of ionic transport and electronic conductivity in organic mixed ionic–electronic conductors.

An applied voltage drives ion penetration, modifies electrochemical doping, and changes the conductivity of the active material. The resulting internal state persists after the input changes and relaxes according to the material’s ionic and electrochemical dynamics.

The paper has established a hierarchy of models:

1. A lumped first-order state equation.
2. A spatial ionic diffusion model.
3. A coupled ionic–electronic transport description.
4. A conductivity transduction relation.
5. A nonlinear extension for saturation and asymmetric kinetics.
6. A multimode model for distributed relaxation.

The ITI should not be described as an ideal integrator under all conditions. Its natural first implementation is a leaky integrator with a finite memory horizon. An ideal-integration approximation is available over a restricted time interval when relaxation is negligible.

The proposed device architecture uses a three-terminal organic electrochemical structure in which gate voltage controls the ionic state and source–drain current measures the resulting conductance.

The decisive experiments are pulse-width dependence, pulse-spacing dependence, frequency response, active-layer thickness scaling, ion-species dependence, operando state measurement, and ion-blocking controls.

The central novelty claim is deliberately constrained. Ion-mediated transients, electrochemical memory, and organic neuromorphic functions are established research areas. What remains to be demonstrated is a deliberately engineered and independently validated circuit element whose primary function is calibrated analog temporal integration through an intrinsic ionic/electrochemical state.

If successful, the ITI would establish a useful primitive for Organic Circuit Theory.

Its significance would lie in allowing a material to perform a temporal operation directly through its internal physical evolution:

[
\boxed{
\text{Input history}
\rightarrow
\text{Ionic state}
\rightarrow
\text{Electrochemical memory}
\rightarrow
\text{Analog output}.
}
]

The first research priority should be a single-mode ITI-1 device with independently measured ionic dynamics and conductance readout. Only after this operation is validated should the architecture advance toward programmable time constants, distributed memory kernels, adaptive temporal processing, and large-scale organic computational networks.

⸻

Appendix A. Core Mathematical Reference

A.1 First-order ITI

[
\tau\dot x+x=kV_{\mathrm{in}}.
]

A.2 Impulse response

[
h(t)=\frac{k}{\tau}e^{-t/\tau}H(t).
]

A.3 General solution

[
x(t)=x(0)e^{-t/\tau}
+
\frac{k}{\tau}
\int_0^t e^{-(t-s)/\tau}V_{\mathrm{in}}(s),ds.
]

A.4 Step response

[
x(t)=kV_0(1-e^{-t/\tau}).
]

A.5 Pulse response

[
x(t)=
\begin{cases}
kV_0(1-e^{-t/\tau}),&0\leq t\leq T_p,\
kV_0(1-e^{-T_p/\tau})e^{-(t-T_p)/\tau},&t>T_p.
\end{cases}
]

A.6 Transfer function

[
H(s)=\frac{k}{1+s\tau}.
]

A.7 Corner frequency

[
f_c=\frac{1}{2\pi\tau}.
]

A.8 Diffusion timescale

[
\tau_D\sim\frac{d^2}{D_{\mathrm{ion}}}.
]

A.9 Ionic flux

[
\mathbf J_i

-D_i\nabla c_i

\mu_i z_iq c_i\nabla\phi.
]

A.10 Ionic conservation

[
\frac{\partial c_i}{\partial t}

-\nabla\cdot\mathbf J_i+R_i.
]

A.11 Conductivity transduction

[
\sigma_e=\sigma_0+\alpha_\sigma x.
]

A.12 Output current

[
I_{\mathrm{out}}

V_{\mathrm{read}}G(x).
]

A.13 Multimode response

[
H(s)=
\sum_{n=1}^{N}
\frac{k_n}{1+s\tau_n}.
]

⸻

Appendix B. Proposed ITI Terminology

Term	Definition
Ionic state	Internal ionic distribution or occupancy governing the device response
Electrochemical state	Coupled ionic and electronic doping configuration
Integration gain	State response per unit input voltage
Ionic relaxation time	Characteristic timescale of internal state recovery
Integration horizon	Effective interval over which input history contributes materially
State saturation	Limitation of additional accumulation as available doping sites are occupied
Read disturbance	Change in ionic state caused by output measurement
Reset operation	Controlled return to a defined baseline state
Multimode ITI	ITI with multiple significant ionic relaxation modes
Programmable ITI	ITI with controllable temporal response parameters

⸻

Appendix C. Minimum Experimental Reporting Standard

Every ITI demonstration should report:

1. Active material identity and composition.
2. Film thickness and channel geometry.
3. Electrolyte composition and ionic species.
4. Gate and drain voltage ranges.
5. Baseline and doped conductance.
6. Input pulse amplitude and duration.
7. Step-response time constant.
8. Pulse-pair relaxation measurement.
9. Frequency-response measurement.
10. Thickness-dependence analysis.
11. Ionic-state characterization.
12. Read-disturbance measurement.
13. Reset and endurance results.
14. Device-to-device variability.
15. Energy per integration event.
16. Competing RC and electrochemical models.
17. Evidence distinguishing ionic integration from parasitic electrical effects.

⸻

Final Research Position

The ITI should be developed first as a rigorously characterized ionic material-state integrator, not as a speculative universal computing device.

Its strongest initial scientific proposition is simple:

A controllable ionic state within an organic mixed conductor can serve as the physical memory variable of an analog temporal integrator.

The first experiment must establish the relationship between applied voltage, ionic redistribution, electrochemical doping, and measured conductance. The second must establish the predicted dependence on pulse duration and pulse spacing. The third must show that the measured temporal response follows ionic transport scaling rather than ordinary parasitic RC behavior.

These results would provide the foundation for a genuinely composable Ionic Temporal Integrator within Organic Circuit Theory.

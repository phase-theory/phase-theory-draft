ORGANIC CIRCUIT THEORY

A Mathematical and Physical Framework for Molecular, Ionic, Excitonic, Chemical, and Multiphysical Circuit Primitives

Research objective: To establish a rigorous circuit-theoretic framework for organic electronic systems in which computation, signal transformation, memory, and control arise not only from electronic charge transport but also from the coupled evolution of ionic distributions, molecular configurations, redox states, exciton populations, chemical concentrations, and mechanical deformation.

Central thesis: Organic materials permit circuit elements whose operative state variables extend beyond conventional terminal voltage and current. Consequently, the primitive vocabulary of circuit theory can be enlarged to include temporal integration, chemical-state retention, multiphysical coincidence detection, adaptive conductance routing, excitonic coupling, and reaction–diffusion dynamics.

The existence of these physical mechanisms is established in varying degrees. Their organization into a unified circuit theory, the proposed taxonomy of primitives, and the architectures developed below constitute a research framework. They are not presented as experimentally established discoveries merely because their mathematical descriptions are plausible.

The theory developed here treats an organic circuit as a dynamical physical network whose internal material states participate directly in computation. Its defining departure from conventional circuit abstraction is not that voltage and current cease to matter, but that they become only part of a larger state space.

The framework therefore has three levels:

* Constitutive physics: how organic materials convert electrical, ionic, optical, chemical, and mechanical inputs into changes of state.
* Circuit primitives: how those state changes implement recognizable operations such as integration, thresholding, memory, comparison, routing, and oscillation.
* Circuit architectures: how primitives can be interconnected to create functional computational systems.

A central requirement throughout is that a proposed primitive must be distinguishable from an ordinary transistor or passive component surrounded by external control electronics. Its defining operation must arise substantially from the organic material’s own internal dynamics.

ORGANIC CIRCUIT THEORY

A Mathematical and Physical Framework for Molecular, Ionic, Excitonic, Chemical, and Multiphysical Circuit Primitives

Abstract

Conventional circuit theory represents electronic systems through terminal variables—principally voltage, current, charge, and magnetic flux—and describes their operation through networks of resistive, capacitive, inductive, and active elements. Organic electronic materials introduce a substantially larger physical state space. Their electrical behavior may depend on ionic redistribution, molecular conformation, electrochemical doping, redox occupancy, exciton populations, chemical concentration, mechanical deformation, and the history of prior excitation.

This paper proposes Organic Circuit Theory (OCT) as a generalized circuit framework for these systems. Its principal object is a network of coupled electronic and material-state dynamics in which computation may occur through the controlled evolution of internal physical and chemical variables.

A generalized organic circuit is represented by

\dot{\mathbf{x}}
=
\mathbf{F}(\mathbf{x},\mathbf{u},T;\boldsymbol{\theta}),
\qquad
\mathbf{y}
=
\mathbf{G}(\mathbf{x},\mathbf{u},T;\boldsymbol{\theta}),

where \mathbf{x} contains electrical, ionic, molecular, optical, chemical, and mechanical state variables; \mathbf{u} denotes applied inputs; \mathbf{y} denotes measurable outputs; and \boldsymbol{\theta} contains constitutive and geometric parameters.

The theory develops generalized constitutive relations, conservation laws, network interconnection rules, stability conditions, thermodynamic constraints, and a taxonomy of candidate organic circuit primitives. Ten classes are examined: molecular resistance, ionic temporal integration, molecular memory, excitonic coupling, chemical comparison, mechanoconductive transduction, adaptive routing, reaction–diffusion oscillation, multiphysical coincidence detection, and organic state amplification.

Five architectures are developed in detail: the Organic Temporal Logic Element, Organic Multiphysical Gate, Molecular State Router, Organic Excitonic Coincidence Circuit, and Organic Reaction–Diffusion Oscillator. A proposed experimental demonstrator, OCEAN-1, is specified to test whether these operations can be implemented with a small network of organic devices.

The paper distinguishes established physical mechanisms from derived circuit behavior and conjectural architectures. It does not assert that all proposed primitives are unprecedented. Organic electrochemical transistors, organic memristive systems, neuromorphic devices, excitonic processes, and chemical sensors already establish important portions of the underlying physical foundation. The novelty sought here is a systematic mathematical classification and a circuit-design methodology that treats these internal material dynamics as first-class computational elements.

Keywords: organic electronics; organic circuit theory; organic electrochemical transistors; mixed ionic–electronic conductors; molecular electronics; excitonic logic; chemical computation; reaction–diffusion systems; neuromorphic circuits; multiphysical computation; material-state dynamics.

⸻

1. Introduction

1.1 The limitation of conventional circuit primitives

The familiar circuit architecture is constructed from a relatively compact vocabulary:

\mathcal{C}_{\mathrm{classical}}
=
\{R,C,L,D,T,S\},

where R, C, and L represent resistive, capacitive, and inductive elements; D denotes diodes; T denotes transistors; and S denotes switching elements.

This vocabulary is extraordinarily general. It supports amplification, filtering, oscillation, switching, storage, computation, and communication.

Yet the abstraction underlying conventional circuit theory usually treats the material itself as a constitutive medium whose internal microscopic dynamics are compressed into parameters such as resistance, capacitance, mobility, threshold voltage, and dielectric constant.

In many organic electronic systems, this compression discards information essential to device operation.

An organic electrochemical transistor, for example, may exhibit conductance controlled by the redistribution of ions throughout an organic mixed ionic–electronic conductor. The electrical response depends on the internal ionic distribution and the history of electrochemical excitation.

Similarly:

* A molecular electronic element may change conductance through a conformational transition.
* An organic photoconductor may retain a photoinduced electronic state.
* An electrochemical organic device may exhibit redox-dependent conductance.
* An organic semiconductor may transport and convert excitons.
* A mechanically deformable organic conductor may change its electrical response under strain.
* A chemically responsive organic material may alter its electrical state through local reactions.

These processes are not merely incidental disturbances. They can determine the function of the device.

The fundamental question is therefore:

Can the internal material dynamics of organic electronics be organized into a systematic theory of circuit elements and computational architectures?

Organic Circuit Theory answers this question affirmatively as a research proposition.

1.2 From terminal-state electronics to material-state electronics

A conventional two-terminal element is often modeled as

i(t)=f(v(t)).

For a linear resistor,

i(t)=Gv(t),

where G is conductance.

For a capacitor,

i(t)=C\frac{dv}{dt}.

For an ideal inductor,

v(t)=L\frac{di}{dt}.

An organic material-state element generally requires an additional internal variable:

i(t)=G(x,t)v(t),

with

\dot{x}=F(x,v,u,T).

Here x may represent an ionic concentration profile, redox fraction, molecular configuration, exciton density, or another internal state.

The conductance is therefore not necessarily a fixed property of the material. It can be a dynamical function of its physical history.

This introduces a distinction between:

1. Terminal state: the externally measurable electrical condition.
2. Material state: the internal configuration governing the terminal response.
3. Computational state: the information encoded in the material configuration and used to determine subsequent outputs.

The three states may be coupled, but they are not identical.

1.3 The central proposition

Organic Circuit Theory proposes that a material can function as a circuit element when its internal state obeys a reproducible, controllable, and measurable dynamical law that performs a useful transformation of inputs into outputs.

This definition is deliberately stricter than simply observing an interesting material response.

A proposed circuit primitive must possess:

* A defined input domain.
* A measurable output.
* A reproducible state-transition law.
* A characteristic operating regime.
* A method of initialization or reset.
* A mechanism for interconnection with other elements.
* A demonstrated function that cannot be reduced trivially to an ordinary passive response without losing the relevant material-state operation.

⸻

2. Physical Foundations of Organic Circuit Behavior

2.1 Organic semiconductors

Organic semiconductors consist of molecular or polymeric structures whose electronic states arise from conjugated molecular orbitals and intermolecular electronic coupling.

Charge transport can occur through several limiting mechanisms.

Localized hopping transport

For localized molecular states, charge transport can be approximated as a sequence of transitions between sites.

A transition rate between molecular sites i and j may be represented schematically by

k_{ij}
=
k_0
\exp\left(-\frac{2r_{ij}}{\xi}\right)
\exp\left[
-\frac{\Delta E_{ij}-q\mathbf{E}\cdot\mathbf{r}_{ij}}
{k_{\mathrm B}T}
\right],

where:

* r_{ij} is the separation between sites;
* \xi is a localization length;
* \Delta E_{ij} is an effective activation energy;
* \mathbf{E} is the electric field;
* q is the carrier charge.

This expression is illustrative. Actual hopping rates depend on energetic disorder, molecular vibrations, reorganization energy, and the detailed transport model.

Effective mobility

At a continuum scale, electronic transport may be represented by a drift–diffusion equation:

\mathbf{J}_e
=
q n\mu_e\mathbf{E}
+
qD_e\nabla n,

where n is carrier density, \mu_e is mobility, and D_e is the electronic diffusion coefficient.

The corresponding charge-continuity equation is

\frac{\partial \rho_e}{\partial t}
+
\nabla\cdot\mathbf{J}_e
=
S_e-R_e,

where S_e and R_e represent carrier generation and recombination.

These equations provide the electronic transport layer of OCT.

2.2 Mixed ionic–electronic conduction

Organic mixed conductors permit simultaneous transport of electronic carriers and mobile ions.

Let

c_i(\mathbf r,t)

denote the concentration of ionic species i.

A simplified ionic flux is

\mathbf J_i
=
-D_i\nabla c_i
-
\mu_i z_iq c_i\nabla\phi,

where:

* D_i is ionic diffusivity;
* \mu_i is ionic mobility;
* z_i is the ionic valence;
* \phi is electrostatic potential.

Ionic conservation gives

\frac{\partial c_i}{\partial t}
=
-\nabla\cdot\mathbf J_i
+
R_i.

The reaction term R_i accounts for local ionic creation, consumption, or exchange with chemical reservoirs.

In an organic electrochemical transistor, ionic penetration and electrochemical doping can alter the electronic carrier density throughout a substantial fraction of the active material volume.

This differs from a purely electrostatic field-effect response.

The device conductance may therefore be written as

G(t)=
G\left[
n(\mathbf r,t),
c_i(\mathbf r,t),
\mu_e(\mathbf r,t),
T
\right].

The history dependence arises because the ionic and electronic distributions do not necessarily relax instantaneously when the external voltage changes.

2.3 Electrochemical state

Let z(\mathbf r,t) represent a local redox or doping fraction.

A general kinetic model is

\frac{\partial z}{\partial t}
=
k_{\mathrm{ox}}(1-z)
-
k_{\mathrm{red}}z,

where the effective rate constants depend on electrochemical potential, temperature, and local chemical environment.

For a simple potential-dependent model,

k_{\mathrm{ox}}
=
k_{\mathrm{ox}}^0
\exp\left(
\frac{\alpha q\eta}{k_{\mathrm B}T}
\right),

k_{\mathrm{red}}
=
k_{\mathrm{red}}^0
\exp\left(
-\frac{(1-\alpha)q\eta}{k_{\mathrm B}T}
\right),

with overpotential \eta and transfer coefficient \alpha.

The conductance becomes

G=G(z).

A material with two or more sufficiently stable electrochemical states can therefore provide a physical memory element.

2.4 Excitonic dynamics

Organic semiconductors can support excitons: bound electron–hole excitations.

Let n_X(\mathbf r,t) denote exciton density.

A minimal reaction–diffusion model is

\frac{\partial n_X}{\partial t}
=
D_X\nabla^2n_X
+
G_X
-
k_Xn_X
-
k_{XX}n_X^2,

where:

* D_X is exciton diffusivity;
* G_X is exciton generation;
* k_X is the first-order decay rate;
* k_{XX} describes bimolecular exciton loss.

The quadratic term is important because exciton–exciton interactions may suppress emission or reduce the available exciton population rather than produce a logic output.

Consequently, excitonic logic cannot be assumed to behave like transistor logic. Its operation must be derived from the actual excitation-transfer, annihilation, quenching, or energy-transfer mechanism.

2.5 Molecular configuration

Let m denote a molecular configuration coordinate.

Its dynamics may be approximated by

\gamma_m\dot m
=
-\frac{\partial U(m;V,T)}{\partial m}
+
\eta_m(t),

where:

* \gamma_m is an effective damping coefficient;
* U is a voltage- and temperature-dependent potential;
* \eta_m represents thermal fluctuations.

If the molecular potential has multiple minima, the material may exhibit configurational memory.

Conductance can depend on the molecular state:

G=G(m).

This creates a possible route to mechanically or electrically controlled molecular switching.

2.6 Mechanical coupling

For a deformable organic conductor, strain can influence electronic overlap, molecular packing, and mobility.

A first-order approximation is

G(\epsilon)
=
G_0(1+\pi\epsilon),

where \epsilon is strain and \pi is an effective electromechanical coefficient.

For larger deformations, nonlinear constitutive laws are required.

The essential point is that the mechanical state may become an input variable of an electrical circuit primitive.

⸻

3. General Mathematical Structure of Organic Circuit Theory

3.1 Generalized state vector

The proposed OCT state vector is

\boxed{
\mathbf x
=
\begin{bmatrix}
q\\
\phi_m\\
c_1\\
\vdots\\
c_N\\
z_{\mathrm{redox}}\\
n_X\\
m\\
\epsilon\\
\mathbf s
\end{bmatrix}
}

where:

* q is terminal or internal electrical charge;
* \phi_m denotes relevant molecular or electrochemical potentials;
* c_i are ionic concentrations;
* z_{\mathrm{redox}} is redox occupancy;
* n_X is exciton density;
* m represents molecular configuration;
* \epsilon is mechanical strain;
* \mathbf s represents additional internal states, such as trap occupancy or chemical reaction intermediates.

Not every organic device requires every component.

A specific implementation selects a reduced state vector appropriate to its physical mechanisms.

3.2 Generalized input vector

Define

\mathbf u
=
\begin{bmatrix}
V\\
I\\
\Phi_{\mathrm{opt}}\\
C_1\\
\vdots\\
C_M\\
\epsilon_{\mathrm{ext}}\\
T
\end{bmatrix},

where the inputs may include:

* Electrical voltage or current.
* Optical flux.
* Chemical concentrations.
* External mechanical strain.
* Temperature.

The input vector must be dimensionally consistent in an actual model. Its components represent different physical quantities and cannot be freely added without appropriate normalization or coupling coefficients.

3.3 State-space equations

The central dynamical equation is

\boxed{
\dot{\mathbf x}
=
\mathbf F(\mathbf x,\mathbf u;\boldsymbol{\theta})
}

with observable output

\boxed{
\mathbf y
=
\mathbf G(\mathbf x,\mathbf u;\boldsymbol{\theta}).
}

The parameter vector

\boldsymbol{\theta}
=
\{\mu_e,D_i,k_r,\tau_i,C_{\mathrm{chem}},\ldots\}

contains transport, reaction, geometric, and constitutive parameters.

This representation includes conventional circuit elements as special cases.

For example, an ideal capacitor has

x=q,\qquad V=\frac{q}{C},
\qquad I=\dot q.

A resistive element has

I=G V.

An ionic temporal element has an additional state variable:

\tau\dot x+x=kV.

Thus, conventional circuit theory is embedded within OCT rather than discarded.

3.4 Spatially distributed formulation

Some organic devices cannot be represented accurately by a small number of lumped states.

Their governing equations must retain spatial dependence:

\frac{\partial\mathbf x(\mathbf r,t)}{\partial t}
=
\mathbf F
\left(
\mathbf x,
\nabla\mathbf x,
\nabla^2\mathbf x,
\mathbf u
\right).

A general coupled formulation is

\begin{aligned}
\frac{\partial n}{\partial t}
&=
-\nabla\cdot\mathbf J_e
+
S_e-R_e,\\[4pt]
\frac{\partial c_i}{\partial t}
&=
-\nabla\cdot\mathbf J_i+R_i,\\[4pt]
\frac{\partial z}{\partial t}
&=
f_z(z,\eta,c_i,T),\\[4pt]
\frac{\partial n_X}{\partial t}
&=
D_X\nabla^2n_X+G_X-k_Xn_X-k_{XX}n_X^2.
\end{aligned}

These equations are coupled through electrostatic potential, electrochemical potential, carrier density, and reaction kinetics.

The terminal current is obtained by integrating the appropriate current density over the electrode boundary:

I(t)
=
\int_{\partial\Omega_e}
\mathbf J\cdot\mathbf n\,dA.

The distinction between local material dynamics and terminal circuit response is essential. A spatially complex device may produce a simple terminal response, while apparently simple terminal hysteresis may conceal multiple internal mechanisms.

3.5 Constitutive closure

A state-space model is not complete merely because its variables have been identified.

It requires constitutive equations connecting:

* Carrier density to conductivity.
* Ionic concentration to electrochemical potential.
* Redox occupancy to electronic structure.
* Molecular configuration to transport parameters.
* Exciton density to optical and electronic observables.
* Mechanical deformation to molecular and electronic response.

For example,

\sigma
=
q\mu_en+\sigma_{\mathrm{hop}}(m,z,T),

and

\mathbf J_e
=
\sigma\mathbf E
+
qD_e\nabla n.

These expressions are illustrative constitutive forms, not universal laws for all organic semiconductors.

The specific functional dependence must be determined experimentally or derived from a validated microscopic model.

⸻

4. Generalized Circuit Laws

4.1 Conservation of electrical charge

For an electrical node k,

\sum_j I_{kj}
=
\frac{dQ_k}{dt}.

This remains valid in organic circuits.

However, charge transferred into an electrochemical material may be accompanied by ionic redistribution and chemical transformation.

The terminal current therefore need not equal the instantaneous rate of change of electronic charge alone.

4.2 Ionic conservation

For an ionic species i,

\frac{\partial c_i}{\partial t}
+
\nabla\cdot\mathbf J_i
=
R_i.

For a closed system without chemical production or consumption,

\frac{d}{dt}
\int_\Omega c_i\,dV
=
-\int_{\partial\Omega}\mathbf J_i\cdot\mathbf n\,dA.

This provides an important conservation constraint for any proposed ionic circuit primitive.

4.3 Charge neutrality and electrostatics

The electrostatic potential may be determined by Poisson’s equation:

-\nabla\cdot
\left(
\varepsilon\nabla\phi
\right)
=
\rho_{\mathrm{free}}.

For sufficiently screened regions, approximate local electroneutrality may be appropriate:

\sum_i z_i c_i
+
\frac{\rho_e}{q}
\approx 0.

The approximation must not be imposed indiscriminately, especially near interfaces or under rapid transients.

4.4 Energy conservation

A generalized organic circuit exchanges energy through several channels:

P_{\mathrm{in}}
=
P_{\mathrm{elec}}
+
P_{\mathrm{opt}}
+
P_{\mathrm{chem}}
+
P_{\mathrm{mech}}.

The system’s internal energy changes according to

\frac{dU}{dt}
=
P_{\mathrm{in}}
-
P_{\mathrm{out}}
-
P_{\mathrm{diss}}.

For a passive device, total dissipation must be nonnegative under the adopted sign convention:

P_{\mathrm{diss}}\geq0.

An active organic circuit may draw chemical or optical energy from an external reservoir. Its apparent electrical gain must therefore be evaluated against all supplied energy channels.

4.5 Thermodynamic admissibility

A useful general requirement is that internal dynamics respect an appropriate free-energy balance.

For an isothermal system with free energy \mathcal F,

\frac{d\mathcal F}{dt}
=
P_{\mathrm{ext}}
-
T\dot S_{\mathrm{prod}},

where

\dot S_{\mathrm{prod}}\geq0.

The precise balance depends on whether the system is open, chemically driven, illuminated, or mechanically actuated.

A proposed primitive that produces sustained oscillation or amplification must identify its energy source.

It cannot generate net work from equilibrium fluctuations alone.

4.6 Interconnection law

Organic circuit primitives must be connected without violating conservation.

At an electrical junction,

\sum_j I_j=0

for an ideal zero-storage node.

At an ionic interface, flux continuity and interfacial reaction conditions must be specified.

At an optical interface, the incident and outgoing optical power must account for reflection, transmission, absorption, and conversion.

At a mechanical interface, force and displacement compatibility must be respected.

OCT therefore requires a multi-domain interconnection formalism rather than treating every device as an electrical black box.

⸻

5. The Organic Circuit Primitive Taxonomy

The proposed taxonomy classifies circuit elements by their dominant internal material operation.

Symbol	Primitive	Primary state	Principal function
MR	Molecular Resistor	Molecular configuration	State-dependent conduction
II	Ionic Integrator	Ionic distribution	Temporal integration
MM	Molecular Memory	Redox/configurational state	Nonvolatile or persistent state
EC	Excitonic Coupler	Exciton population	Optical excitation transfer
CC	Chemical Comparator	Chemical state	Chemical threshold detection
ST	Strain Transducer	Mechanical deformation	Electromechanical conversion
AR	Adaptive Router	Conductance distribution	History-dependent signal routing
RO	Reaction Oscillator	Chemical concentrations	Autonomous oscillation
MG	Multiphysical Gate	Coupled material states	Coincidence detection
OSA	Organic State Amplifier	Internal state and carrier population	State-dependent gain

This taxonomy is proposed. It is not a claim that each class is a previously unknown physical device.

⸻

6. Primitive I: Molecular Resistor

6.1 Definition

A molecular resistor is an element whose electrical conductance depends materially on a molecular configuration variable.

Let m represent the configuration state.

Then

I=G(m,V,T)V.

For a simple two-state model,

m\in\{m_0,m_1\},

with

G(m_0)=G_0,\qquad G(m_1)=G_1.

The state transition may be induced by voltage, temperature, optical excitation, or chemical environment.

6.2 Continuous configuration model

A more general model is

\dot m
=
-\Gamma_m\frac{\partial U(m,V)}{\partial m}.

If the energy landscape possesses two minima, the molecular system may retain one of two configurations.

The current then depends on both the terminal voltage and the stored molecular state.

6.3 Circuit significance

The molecular resistor can serve as:

* A state-dependent load.
* A molecular switch.
* A conductance memory element.
* A reconfigurable routing component.

6.4 Principal obstacle

The molecular configuration must remain sufficiently stable to distinguish states while permitting controlled switching.

A molecular transition that occurs randomly or irreversibly is not a reliable circuit primitive.

⸻

7. Primitive II: Ionic Temporal Integrator

7.1 Definition

The Ionic Temporal Integrator (ITI) is a proposed primitive in which ionic redistribution accumulates the effect of an input over time.

Let x(t) be a normalized internal ionic state.

A first-order model is

\boxed{
\tau\dot x+x=kV_{\mathrm{in}}(t).
}

Its solution is

x(t)
=
x(0)e^{-t/\tau}
+
\frac{k}{\tau}
\int_0^t
e^{-(t-s)/\tau}
V_{\mathrm{in}}(s)\,ds.

The state is therefore an exponentially weighted history of the input.

7.2 Pulse accumulation

For a constant input V_0 applied over duration T_p,

x(T_p)
=
x(0)e^{-T_p/\tau}
+
kV_0
\left(
1-e^{-T_p/\tau}
\right).

If the device begins from x(0)=0,

x(T_p)
=
kV_0
\left(
1-e^{-T_p/\tau}
\right).

A threshold output occurs when

x(T_p)\geq x_{\mathrm{th}}.

The required pulse duration is

T_p
\geq
-\tau
\ln
\left(
1-\frac{x_{\mathrm{th}}}{kV_0}
\right),

provided kV_0>x_{\mathrm{th}}.

This produces duration-sensitive logic.

7.3 Physical implementation

A candidate implementation uses an organic mixed ionic–electronic conductor whose ionic penetration changes its conductance.

The output may be measured through a second electrical terminal or a coupled sensing transistor.

The external measurement apparatus must not supply the integration function if the device is being claimed as an intrinsic ITI.

7.4 Distinction from a conventional capacitor

A capacitor stores electrical charge according to

Q=CV.

An ionic integrator stores a distributed material state whose relaxation and response depend on diffusion, electrochemical coupling, and ionic boundary conditions.

In a linear regime, the terminal response may resemble a conventional RC network.

The proposed novelty is therefore not the mathematical existence of an integrator. It is the use of a controllable ionic material state as the physical substrate of temporal computation.

7.5 Falsifiable prediction

At fixed pulse amplitude, the output threshold should depend systematically on pulse duration and pulse spacing.

If all observed behavior can be explained by parasitic capacitance and external RC components, the claim of a distinct ionic computational primitive is not supported.

⸻

8. Primitive III: Molecular Memory

8.1 Definition

A Molecular Memory (MM) element stores information in a persistent internal material state.

Let z denote redox occupancy or another molecular state.

The electrical output is

I=G(z)V.

The state evolves according to

\dot z=f(z,V,C,T).

A write operation changes z, while a read operation measures G(z) with sufficiently small disturbance.

8.2 State retention

For a simple relaxation model,

\dot z
=
-\frac{z-z_{\mathrm{eq}}}{\tau_r}.

The solution is

z(t)-z_{\mathrm{eq}}
=
[z(0)-z_{\mathrm{eq}}]e^{-t/\tau_r}.

The retention time is determined by the material’s relaxation dynamics.

A useful memory requires

\tau_r\gg t_{\mathrm{operation}},

with a sufficiently large separation between distinguishable conductance states.

8.3 Multilevel storage

If z is continuous and experimentally controllable, multiple states may be encoded:

z_0,z_1,\ldots,z_{N-1}.

The number of practically distinguishable states depends on noise, drift, device variability, read disturbance, and retention.

The theoretical existence of a continuum of states does not establish reliable analog memory.

8.4 Required tests

A molecular memory claim requires:

1. Repeatable write operations.
2. Non-destructive or characterized read operations.
3. Retention measurements.
4. Endurance testing.
5. Device-to-device variability analysis.
6. Environmental stability measurements.

Organic memristive and electrochemical memory devices provide relevant prior art. The proposed OCT contribution is their inclusion in a common primitive and network formalism.

⸻

9. Primitive IV: Excitonic Coupler

9.1 Definition

An Excitonic Coupler (EC) is an optical or electronic circuit element in which exciton generation, transfer, quenching, or interaction mediates a controlled signal transformation.

Let n_A and n_B denote exciton populations in coupled regions.

A general coupled model is

\begin{aligned}
\dot n_A
&=
G_A-k_A n_A
-\kappa_{AB}n_A
+\kappa_{BA}n_B,\\
\dot n_B
&=
G_B-k_B n_B
+\kappa_{AB}n_A
-\kappa_{BA}n_B.
\end{aligned}

The transfer coefficients depend on geometry, energetic alignment, molecular orientation, and coupling strength.

9.2 Conditional coupling

A candidate logic operation requires a measurable output that depends nonlinearly on two or more excitonic inputs.

For example,

Y=H(n_A n_B-\theta),

where H is a threshold function and \theta is a detection threshold.

This is a proposed abstract operation, not a universal excitonic law.

The actual output must be derived from the microscopic process.

9.3 Exciton–exciton annihilation

A common interaction is represented by

\dot n_X
=
G_X-k_Xn_X-k_{XX}n_X^2.

The nonlinear term often reduces the exciton population.

It may therefore generate an inverse response rather than a positive coincidence output.

An excitonic logic design must explicitly account for this behavior.

9.4 Potential applications

* Optical coincidence detection.
* Molecular energy-transfer networks.
* Excitonic signal routing.
* Hybrid photonic–organic computation.
* Optical preprocessing in flexible systems.

9.5 Principal obstacle

Exciton lifetimes, diffusion lengths, energy disorder, optical losses, and the absence of robust gain can limit circuit depth.

A useful excitonic circuit requires a mechanism for signal restoration or cascading.

⸻

10. Primitive V: Chemical Comparator

10.1 Definition

A Chemical Comparator (CC) converts a chemical concentration or reaction state into a thresholded electrical response.

Let C be the concentration of a target species.

A simple response law is

G(C)
=
G_{\min}
+
\frac{G_{\max}-G_{\min}}
{1+\exp[-\beta(C-C_0)]}.

Here C_0 is the midpoint of the response and \beta controls sensitivity.

A comparator output may be defined by

Y=H(C-C_{\mathrm{th}}).

10.2 Reaction-mediated response

If the chemical species reacts with the organic material, the relevant state may be a reaction occupancy r:

\dot r
=
k_f C(1-r)-k_r r.

The conductance becomes

G=G(r).

This provides a direct route from chemical exposure to electrical state.

10.3 Circuit applications

* Chemical threshold alarms.
* Environmental sensing.
* Biochemical event detection.
* Chemical preprocessing.
* Sensor-integrated logic.

10.4 Important distinction

A chemical sensor is not automatically a chemical comparator.

A comparator must produce a reproducible decision boundary or threshold response, with characterized selectivity, hysteresis, recovery, and false-positive behavior.

⸻

11. Primitive VI: Mechanoconductive Transducer

11.1 Definition

The Mechanoconductive Comparator (MCC) converts mechanical deformation into an electrical response.

Let \epsilon be strain.

The simplest model is

G(\epsilon)=G_0(1+\pi\epsilon).

For nonlinear behavior,

G(\epsilon)
=
G_0
\exp(a\epsilon+b\epsilon^2).

A threshold response may be defined by

Y=H(G(\epsilon)-G_{\mathrm{th}}).

11.2 Physical mechanisms

Potential mechanisms include:

* Changes in intermolecular overlap.
* Variation in chain orientation.
* Microstructural rearrangement.
* Strain-dependent hopping distances.
* Changes in contact resistance.
* Mechanical modulation of ionic transport.

11.3 Applications

* Flexible tactile logic.
* Strain-triggered switching.
* Structural monitoring.
* Wearable computational sensors.
* Mechanically adaptive routing.

11.4 Principal obstacle

Mechanical deformation may produce irreversible morphology changes, fatigue, and contact artifacts.

A true mechanoconductive primitive must distinguish reversible material-state operation from uncontrolled mechanical damage.

⸻

12. Primitive VII: Adaptive Conductance Router

12.1 Definition

The Adaptive Conductance Router (AR) is a network element in which internal material states determine the distribution of current among multiple output paths.

For branch j,

I_j=G_j(z_j)V.

The conductance states evolve according to

\dot z_j
=
f_j(z_j,V,I_j,\mathbf z,\mathbf u).

The total current is

I_{\mathrm{in}}
=
\sum_{j=1}^{N}I_j.

The current division is

\frac{I_j}{I_{\mathrm{in}}}
=
\frac{G_j(z_j)}
{\sum_k G_k(z_k)}

for ideal parallel branches under a common voltage.

12.2 History-dependent routing

The router can adapt its branch conductances based on prior inputs.

A simple competitive update rule is

\dot z_j
=
\eta I_j
-
\lambda z_j
-
\gamma z_j\sum_{k\neq j}z_k.

This equation is illustrative and requires a physical implementation that produces the specified dynamics.

The first term reinforces active paths, the second introduces relaxation, and the third represents competition.

12.3 Applications

* Adaptive sensor networks.
* Self-adjusting signal paths.
* Neuromorphic connectivity.
* Material-based routing.
* Fault-tolerant organic circuits.

12.4 Novelty limitation

Adaptive routing is not a new computational concept. Its potential contribution is an implementation in which routing weights are stored and updated intrinsically by organic material states.

⸻

13. Primitive VIII: Organic Reaction–Diffusion Oscillator

13.1 Definition

The Organic Reaction–Diffusion Oscillator (ORDO) is a spatially distributed chemical system whose coupled reaction kinetics produce periodic or quasi-periodic electrical or optical outputs.

Let a and b represent two chemical state variables.

A generic reaction–diffusion model is

\frac{\partial a}{\partial t}
=
D_a\nabla^2a+f(a,b),

\frac{\partial b}{\partial t}
=
D_b\nabla^2b+g(a,b).

13.2 Local oscillatory dynamics

A simplified local model is

\dot a=f(a,b),
\qquad
\dot b=g(a,b).

An equilibrium (a_0,b_0) is locally stable when the eigenvalues of the Jacobian

J=
\begin{bmatrix}
\partial_a f & \partial_b f\\
\partial_a g & \partial_b g
\end{bmatrix}_{(a_0,b_0)}

have negative real parts.

An oscillatory instability may occur when the trace and determinant satisfy the appropriate Hopf bifurcation conditions:

\operatorname{tr}(J)=0,
\qquad
\det(J)>0,

with a nonzero crossing speed and the relevant nondegeneracy conditions.

13.3 Electrical transduction

The chemical state may control conductance:

I(t)=G(a,b)V.

Alternatively, the oscillator may produce an optical signal:

L(t)=L(a,b).

13.4 Applications

* Organic timing circuits.
* Autonomous chemical clocks.
* Oscillatory sensor networks.
* Event generators.
* Distributed wave-based computation.

13.5 Energy requirement

A sustained oscillator requires an energy source and a mechanism that maintains the system away from equilibrium.

The chemical fuel, applied bias, or optical drive must be explicitly accounted for.

⸻

14. Primitive IX: Multiphysical Coincidence Gate

14.1 Definition

The Multiphysical Gate (MG) produces an output only when multiple physically distinct inputs jointly satisfy a condition.

For example, an electrical input V, chemical concentration C, and mechanical strain \epsilon may determine an output:

Y=F(V,C,\epsilon).

A threshold model is

Y=
H(V-V_0)
H(C-C_0)
H(\epsilon-\epsilon_0).

This represents a three-input coincidence condition.

14.2 Physical realization

The inputs may act through distinct internal states:

\begin{aligned}
\dot x_e&=f_e(x_e,V),\\
\dot x_c&=f_c(x_c,C),\\
\dot x_m&=f_m(x_m,\epsilon).
\end{aligned}

The output state is then

y=H(\Psi(x_e,x_c,x_m)-\theta).

A physical implementation could use electrochemical gating, chemical doping, and strain-dependent transport in the same active material.

14.3 Why this matters

Conventional electronic logic generally converts external inputs into electrical signals before combining them.

An organic multiphysical gate may combine the inputs through direct interactions with the material itself.

This may reduce the need for separate sensor, amplifier, and logic stages in some applications.

14.4 Principal obstacle

Cross-sensitivity can be mistaken for useful coincidence behavior.

The device must demonstrate that each input contributes independently and that the output is not simply dominated by one variable.

⸻

15. Primitive X: Organic State Amplifier

15.1 Definition

An Organic State Amplifier (OSA) is an active device in which a small input-induced change in an internal material state produces a larger measurable output response.

Let the output current be

I_{\mathrm{out}}=G(x)V_{\mathrm{bias}}.

For a small perturbation \delta x,

\delta I_{\mathrm{out}}
=
V_{\mathrm{bias}}
\frac{\partial G}{\partial x}
\delta x.

The small-signal state sensitivity is therefore

A_x
=
V_{\mathrm{bias}}
\frac{\partial G}{\partial x}.

A large A_x does not by itself prove power gain.

The device must be evaluated using complete input and output power measurements.

15.2 Dynamic response

If

\tau\dot x+x=k u,

then the state transfer function is

H_x(s)=\frac{k}{1+s\tau}.

The output transfer function depends on the sensitivity of the conductance to x.

This produces a frequency-dependent amplifier whose response may depend on material relaxation.

15.3 Applications

* Chemical signal amplification.
* Ionic-state sensing.
* Optical signal transduction.
* Low-frequency neuromorphic processing.
* Material-state readout.

⸻

16. Organic Temporal Logic

16.1 Motivation

Digital logic traditionally operates on voltage levels and transitions.

An ionic material can respond to the duration, spacing, and sequence of input pulses.

This creates a route to temporal logic in which the internal state represents a weighted history of previous events.

16.2 Mathematical definition

Define the state variable

x(t)
=
\int_{-\infty}^{t}
K(t-s)u(s)\,ds,

where K is a causal memory kernel.

For exponential memory,

K(t)=\frac{k}{\tau}e^{-t/\tau}H(t).

The corresponding state equation is

\tau\dot x+x=ku.

An output event occurs when

x(t)\geq x_{\mathrm{th}}.

16.3 Pulse-pair discrimination

For two identical pulses separated by time \Delta t, the residual state from the first pulse is proportional to

e^{-\Delta t/\tau}.

The second pulse therefore produces a larger peak state when the interval is short.

The device can discriminate between:

* Closely spaced events.
* Widely spaced events.
* Repeated low-amplitude events.
* A single high-amplitude event.

16.4 Temporal logic functions

A family of operations becomes possible:

Operation	Material-state interpretation
Duration threshold	State crosses a threshold after sustained input
Pulse accumulation	Repeated pulses increase internal state
Temporal coincidence	Two inputs arrive within a relaxation window
Delayed response	Internal state reaches threshold after a delay
Adaptation	Response decreases or changes after repeated stimulation
Reset	Reverse bias or chemical recovery restores baseline

16.5 Limitation

Temporal integration is not unique to organic materials. Capacitors, RC circuits, and digital counters can implement related functions.

The OCT proposition is that ionic and molecular state dynamics can implement temporal operations within the active material, potentially with different energy, area, and sensing characteristics.

⸻

17. Multiphysical Computation

17.1 General formulation

A multiphysical computational element accepts inputs from more than one physical domain:

\mathbf u=
(V,\Phi_{\mathrm{opt}},C,\epsilon,T).

Its output is

y=G(\mathbf x,\mathbf u).

The material state evolves through coupled dynamics:

\dot{\mathbf x}
=
\begin{bmatrix}
F_e\\
F_i\\
F_c\\
F_X\\
F_m
\end{bmatrix}.

The resulting operation can be viewed as a physical transformation from a heterogeneous input space into an electrical, optical, or chemical output space.

17.2 Cross-domain coupling

A simplified coupling structure is

\begin{aligned}
\dot x_e&=f_e(x_e,x_i,V),\\
\dot x_i&=f_i(x_i,x_c,V),\\
\dot x_c&=f_c(x_c,C,x_e),\\
\dot x_X&=f_X(x_X,\Phi_{\mathrm{opt}},x_e),\\
\dot x_m&=f_m(x_m,\epsilon,x_i).
\end{aligned}

The cross terms represent coupling between electronic, ionic, chemical, excitonic, and mechanical states.

They must be measured or derived. Their presence cannot simply be assumed.

17.3 Computational advantage hypothesis

A material that directly responds to chemical, optical, and mechanical signals may eliminate some transduction stages.

The potential advantages include:

* Reduced sensor-to-processor interfaces.
* Local signal preprocessing.
* Distributed memory.
* Adaptive sensing.
* Low-frequency temporal computation.
* Conformable computational structures.

These are hypotheses about system-level benefits, not established universal advantages.

⸻

18. Network Theory and Composition

18.1 Organic circuit graph

Represent an OCT network as a directed graph

\mathcal G=(\mathcal V,\mathcal E),

where each vertex v_i represents a material-state element and each edge represents a permitted physical coupling.

The graph may contain:

* Electrical connections.
* Ionic transport paths.
* Chemical diffusion paths.
* Optical couplings.
* Mechanical connections.

A single graph may therefore contain multiple edge types.

18.2 Hybrid network equations

For N interconnected elements,

\dot{\mathbf X}
=
\mathbf F_{\mathcal G}(\mathbf X,\mathbf U),

where

\mathbf X=
[\mathbf x_1^T,\mathbf x_2^T,\ldots,\mathbf x_N^T]^T.

Electrical interconnections are constrained by Kirchhoff’s laws, while other domains require their own conservation and boundary conditions.

18.3 Composition

Two primitives can be composed when their outputs are compatible with the inputs of the next element.

If

y_A=G_A(x_A,u_A)

and

\dot x_B=F_B(x_B,y_A),

then the composite system is

\begin{aligned}
\dot x_A&=F_A(x_A,u_A),\\
\dot x_B&=F_B(x_B,G_A(x_A,u_A)).
\end{aligned}

The composition is mathematically straightforward, but physical implementation requires compatible signal levels, timescales, interfaces, and energy budgets.

18.4 Cascadability

A primitive is useful in a large network only if its output can reliably drive another primitive.

Cascadability requires:

1. Sufficient output amplitude.
2. Adequate noise margin.
3. Controlled loading.
4. Stable operating points.
5. Compatible response times.
6. A reset or initialization strategy.
7. Bounded accumulated drift.

An organic circuit architecture that performs a single isolated operation but cannot be cascaded is not yet a general-purpose computational technology.

⸻

19. Candidate Architecture I: Organic Temporal Logic Element

19.1 Architecture

The Organic Temporal Logic Element (OTLE) consists of:

* An organic mixed ionic–electronic conductor.
* An ionic accumulation region.
* A conductance readout channel.
* A threshold output stage.
* A reset mechanism.

The central state equation is

\tau\dot x+x=kV_{\mathrm{in}}.

The output is

V_{\mathrm{out}}
=
V_H H(x-x_{\mathrm{th}}).

A practical device may use an organic electrochemical transistor as the active state element.

19.2 Functional operations

The OTLE is intended to provide:

* Pulse-duration discrimination.
* Temporal integration.
* Event accumulation.
* Delayed switching.
* Adjustable temporal thresholds.

19.3 Required measurements

The experiment must measure:

* State response versus pulse amplitude.
* State response versus pulse duration.
* Relaxation time.
* Pulse-pair interaction.
* Reset efficiency.
* Read disturbance.
* Device-to-device variation.

19.4 Success criterion

The device must reproduce a predictable temporal response over repeated cycles without relying on an external integrator to create the claimed function.

⸻

20. Candidate Architecture II: Organic Multiphysical Gate

20.1 Architecture

The Organic Multiphysical Gate (OMG) combines at least two independently controllable input channels.

A representative design uses:

* An electrical gate.
* A chemical exposure channel.
* A strain-sensitive active layer.
* An electrical output channel.

The output condition is

Y=
H(V-V_0)
H(C-C_0)
H(\epsilon-\epsilon_0).

20.2 Experimental logic table

Electrical input	Chemical input	Mechanical input	Expected output
0	0	0	0
1	0	0	0
0	1	0	0
0	0	1	0
1	1	0	0
1	0	1	0
0	1	1	0
1	1	1	1

The table represents an ideal three-input AND-like operation.

Actual devices will have finite transition widths and cross-sensitivities.

20.3 Critical experiment

Each input must be varied independently while the others are held below threshold.

The experiment must also test combinations that should not produce an output.

This distinguishes genuine coincidence detection from a device that simply responds to the strongest input.

⸻

21. Candidate Architecture III: Molecular State Router

21.1 Architecture

The Molecular State Router (MSR) contains several organic conductive branches whose internal states determine the relative branch conductances.

For branch j,

I_j=G_j(z_j)V.

The state vector is

\mathbf z=(z_1,z_2,\ldots,z_N).

A history-dependent update rule changes the conductance distribution.

21.2 Intended operation

The MSR can direct subsequent signals preferentially toward paths that were previously active.

This resembles adaptive routing and synaptic weighting, but the proposed implementation places the adaptive state inside the organic material.

21.3 Demonstration

A two-branch device is sufficient for an initial experiment.

Apply a sequence of inputs that favors branch A, then measure the redistribution of current.

Repeat with branch B.

A successful device should exhibit:

* Reproducible state-dependent routing.
* A controllable adaptation rate.
* A measurable retention time.
* A reset or rebalancing process.
* Stable operation over repeated switching cycles.

⸻

22. Candidate Architecture IV: Organic Excitonic Coincidence Circuit

22.1 Architecture

The Organic Excitonic Coincidence Circuit (OECC) uses two optically addressable regions coupled through an organic excitonic medium.

The inputs are

u_A(t),\qquad u_B(t).

Exciton populations evolve according to coupled transport and reaction equations.

A measurable output may be photoluminescence, photocurrent, or another exciton-sensitive observable.

22.2 Coincidence requirement

The device should distinguish simultaneous or closely spaced optical inputs from isolated inputs.

A general response is

Y=F[n_A(t),n_B(t)].

The coincidence window is determined by exciton lifetime, transfer time, diffusion, and the nonlinear interaction mechanism.

22.3 Main difficulty

Excitonic interactions may reduce the available signal through annihilation or quenching.

The circuit must identify a physical process that creates a reliable, measurable conditional output.

Without that mechanism, the architecture remains a proposed experimental direction rather than a validated logic primitive.

⸻

23. Candidate Architecture V: Organic Reaction–Diffusion Oscillator

23.1 Architecture

The ORDO contains an organic active medium coupled to a chemical reaction network.

The chemical state evolves spatially:

\frac{\partial\mathbf c}{\partial t}
=
\mathbf D\nabla^2\mathbf c
+
\mathbf R(\mathbf c,\mathbf u).

The output is obtained through an electrical or optical transducer:

y(t)=G(\mathbf c(t)).

23.2 Intended operations

* Autonomous timing.
* Oscillatory event generation.
* Spatial wave propagation.
* Chemical synchronization.
* Distributed temporal processing.

23.3 Required evidence

The system must demonstrate a reproducible oscillation whose frequency, amplitude, or phase can be controlled by a defined input.

The experiment must distinguish an intrinsic chemical oscillator from periodicity introduced by the external measurement circuit.

⸻

24. Proposed Demonstrator: OCEAN-1

24.1 Objective

The Organic Computational Element Architecture Network, designated OCEAN-1, is proposed as a compact experimental platform for determining whether several OCT primitives can be integrated into a single functional network.

The initial objective is not to construct a competitive processor.

It is to establish whether internal organic material states can perform distinct computational operations and be interconnected reproducibly.

24.2 Functional composition

Subsystem	Quantity	Intended operation
Organic electrochemical transistor	4	Electrical control and readout
Ionic temporal integrator	2	Pulse accumulation
Molecular memory element	2	State storage
Multiphysical input gate	2	Chemical/electrical coincidence
Organic oscillator	1	Autonomous timing
Output transistor	1	Signal restoration and readout

The quantities describe a proposed functional inventory, not a finalized fabrication layout.

24.3 Block architecture

\boxed{
\text{Input}
\rightarrow
\text{Ionic Integration}
\rightarrow
\text{Molecular State}
\rightarrow
\text{Multiphysical Decision}
\rightarrow
\text{Output}
}

An oscillator supplies an additional temporal reference.

The architecture should allow each subsystem to be tested independently before integration.

24.4 Demonstration sequence

Experiment A — Temporal accumulation

Apply pulses of varying duration and spacing. Measure the ionic state and output threshold.

Experiment B — Molecular memory

Write two or more distinguishable states. Measure retention and read disturbance.

Experiment C — Chemical modulation

Vary chemical concentration while holding electrical conditions constant. Determine the response threshold and selectivity.

Experiment D — Multiplexed coincidence

Apply electrical and chemical inputs independently and jointly. Verify the expected truth table.

Experiment E — Oscillation

Measure autonomous output oscillations and determine their dependence on temperature, chemical supply, and applied bias.

Experiment F — Integrated operation

Connect the elements and demonstrate a complete sequence in which one material-state operation influences a downstream element.

24.5 Minimum success criteria

OCEAN-1 should not be considered successful merely because each device produces an interesting electrical response.

It must demonstrate:

* Independently identifiable internal states.
* Predictable input–state–output relationships.
* Reproducible operation.
* Characterized noise and drift.
* Measurable energy consumption.
* Functional interconnection.
* A complete operation that cannot be attributed entirely to external instrumentation.

⸻

25. Fabrication and Materials Strategy

25.1 Material selection

The first implementation should favor well-characterized organic mixed conductors and electrochemically active polymers rather than an unproven molecular system.

Selection criteria include:

* Electronic conductivity.
* Ionic accessibility.
* Electrochemical stability.
* Reversible doping.
* Environmental stability.
* Compatibility with substrates and electrodes.
* Processability.
* Device-to-device reproducibility.

25.2 Device geometry

The simplest demonstrator should use planar structures with separately addressable electrodes.

A possible layer sequence is:

1. Flexible or rigid substrate.
2. Patterned source and drain electrodes.
3. Organic active channel.
4. Ionic or electrolyte interface.
5. Gate electrode.
6. Encapsulation and environmental barrier.
7. Optional optical or chemical access region.

The actual stack depends on the selected OECT or mixed-conductor architecture.

25.3 Patterning

Candidate fabrication methods include:

* Photolithography.
* Shadow-mask deposition.
* Inkjet printing.
* Screen printing.
* Aerosol-jet printing.
* Solution coating.
* Laser patterning.

The chosen process must preserve the electrochemical and mechanical properties of the active material.

25.4 Encapsulation

Organic circuits may be sensitive to oxygen, water, light, and chemical contamination.

Encapsulation must protect the device without blocking the intended ionic, optical, or chemical input pathways.

This creates an architectural tradeoff between environmental stability and material accessibility.

25.5 Integration challenge

Electrical integration is not sufficient.

A practical OCT platform must also manage:

* Ionic cross-talk.
* Chemical diffusion between adjacent elements.
* Optical leakage.
* Mechanical coupling.
* Thermal gradients.
* Electrochemical contamination.
* Variability in active-layer morphology.

These effects may be useful in some architectures but must be controlled in others.

⸻

26. Modeling and Simulation Methodology

26.1 Hierarchical modeling

OCT should employ a hierarchy of models.

Level 1 — Lumped circuit models

Represent each device using a small number of internal state variables.

Level 2 — Distributed transport models

Resolve spatial ionic, electronic, and excitonic transport.

Level 3 — Molecular models

Describe molecular configurations, electronic structure, and reaction pathways.

Level 4 — Network models

Combine device-level state equations into a circuit architecture.

The levels should be connected through physically consistent parameters.

26.2 Parameter identification

For a state-space model

\dot{\mathbf x}
=
\mathbf F(\mathbf x,\mathbf u;\boldsymbol\theta),

the parameters \boldsymbol\theta must be estimated from controlled experiments.

Parameter fitting should not be treated as proof that the model is physically correct.

Alternative models should be compared.

26.3 Identifiability

A central problem is determining whether the internal states can be distinguished from terminal measurements.

Two models may produce nearly identical current–voltage curves while assigning different physical mechanisms to the response.

A useful OCT model should therefore identify which parameters and states are experimentally observable.

The local observability of a nonlinear system can be investigated through the output function and its Lie derivatives with respect to the state dynamics.

For a linearized system,

\dot{\delta x}=A\delta x+B\delta u,
\qquad
\delta y=C\delta x,

the observability matrix is

\mathcal O=
\begin{bmatrix}
C\\
CA\\
CA^2\\
\vdots\\
CA^{n-1}
\end{bmatrix}.

Full rank is required for complete linear observability.

26.4 Model discrimination

A proposed ionic memory model should be compared against:

* A conventional RC model.
* A trap-mediated model.
* A contact-resistance model.
* A thermal model.
* A purely electronic hysteresis model.

A proposed chemical comparator should be compared against nonspecific adsorption and environmental drift.

A proposed excitonic gate should be compared against ordinary photoconductive nonlinearities.

The objective is to establish the actual mechanism rather than merely reproduce a measured curve.

⸻

27. Performance Metrics

A useful organic circuit theory requires standardized metrics.

27.1 Electrical performance

* On/off ratio.
* Transconductance.
* Output current.
* Switching voltage.
* Output impedance.
* Noise spectral density.
* Power consumption.

27.2 Temporal performance

* State integration time.
* Relaxation time.
* Response latency.
* Pulse-pair resolution.
* Recovery time.
* Oscillation frequency.
* Timing variability.

27.3 Memory performance

* Retention time.
* Write energy.
* Read energy.
* Endurance.
* State separability.
* Drift.
* Multilevel distinguishability.

27.4 Chemical performance

* Detection limit.
* Selectivity.
* Dynamic range.
* Response time.
* Recovery time.
* Cross-sensitivity.
* Chemical stability.

27.5 System-level performance

* Primitive density.
* Functional yield.
* Cascadability.
* Energy per operation.
* Reset cost.
* State reproducibility.
* Network-level error rate.

An OCT architecture should be compared with conventional implementations performing the same function under equivalent conditions.

⸻

28. Stability, Noise, and Reliability

28.1 Sources of noise

Organic circuit behavior may be affected by:

* Thermal fluctuations.
* Ionic concentration fluctuations.
* Molecular conformational fluctuations.
* Charge trapping.
* Contact variability.
* Electrochemical side reactions.
* Morphological rearrangement.
* Environmental contamination.

28.2 State stability

For a state equation

\dot{\mathbf x}=\mathbf F(\mathbf x,\mathbf u),

an operating point \mathbf x_0 satisfies

\mathbf F(\mathbf x_0,\mathbf u_0)=0.

The local stability is determined by the Jacobian

J=
\left.
\frac{\partial\mathbf F}{\partial\mathbf x}
\right|_{\mathbf x_0,\mathbf u_0}.

If every eigenvalue of J has negative real part, the operating point is locally asymptotically stable for the linearized dynamics.

A memory device may intentionally require multiple stable operating points.

An oscillator may require a stable limit cycle rather than a stable equilibrium.

The relevant stability criterion therefore depends on the primitive.

28.3 Noise propagation

For a linearized stochastic model,

\dot{\delta x}=A\delta x+B\eta(t),

the covariance matrix P may satisfy a Lyapunov equation in a stable stationary regime:

AP+PA^T+Q=0,

where Q is the noise covariance input.

This provides a starting point for calculating state uncertainty and output variability.

28.4 Reliability requirement

A computational material state must be sufficiently separated from its neighboring states relative to noise and drift.

If two states produce overlapping output distributions, they cannot reliably encode distinct symbols without additional error correction.

⸻

29. Theoretical Novelty and Prior-Art Assessment

29.1 What is already established

The physical foundations of OCT are not wholly new.

Established areas include:

1. Organic field-effect transistors.
2. Organic electrochemical transistors.
3. Mixed ionic–electronic conductors.
4. Electrochemical and memristive organic devices.
5. Organic neuromorphic and synaptic systems.
6. Organic photodetectors and excitonic processes.
7. Flexible and strain-responsive organic electronics.
8. Chemically responsive organic electronic sensors.
9. Reaction–diffusion systems.
10. Hybrid electronic–chemical sensing architectures.

Organic electrochemical devices have already demonstrated history-dependent conductance, temporal response, and neuromorphic functions. Organic logic gates and complementary circuit demonstrations also exist.

Excitonic logic and multiexcitonic computation have been discussed as research directions, although their practical circuit realization presents substantial challenges.

Accordingly, this paper does not claim to discover organic memory, ionic integration, chemical sensing, excitonic transport, or neuromorphic computation.

29.2 Proposed theoretical contribution

The proposed contribution is the organization of these mechanisms into a generalized circuit framework with:

* A common state-space representation.
* Explicit multi-domain conservation laws.
* Constitutive closure requirements.
* A taxonomy of material-state primitives.
* Formal interconnection rules.
* Thermodynamic admissibility constraints.
* Standardized criteria for primitive validation.
* A progression from individual elements to integrated architectures.

The framework is intended to make organic material-state devices comparable and composable.

29.3 Novelty classification

Proposition	Assessment
Organic mixed ionic–electronic conduction	Established
Organic electrochemical memory	Established research area
Ionic temporal integration	Established mechanism; OCT primitive formalization proposed
Organic neuromorphic adaptation	Established research area
Chemical-to-electrical transduction	Established
Strain-dependent organic conductance	Established research area
Excitonic transport and annihilation	Established physical processes
Practical organic excitonic logic	Developing and technically challenging
Organic reaction–diffusion computation	Plausible research direction requiring specific implementation
Unified OCT state-space theory	Proposed framework
OCT primitive taxonomy	Proposed classification
OCEAN-1 integrated architecture	Proposed experimental system

29.4 The central novelty question

The critical scientific question is not whether organic materials can exhibit memory, hysteresis, or nonlinear response.

Those behaviors are already known.

The more important question is:

Can the internal dynamics of organic materials be formalized as a composable library of circuit primitives whose operations are physically distinct, measurable, scalable, and advantageous over equivalent conventional circuits?

That is the central hypothesis of Organic Circuit Theory.

⸻

30. Falsifiability and Experimental Rejection Criteria

A theory becomes scientifically useful when it specifies how its claims may fail.

OCT contains several levels of claim, and each must be tested separately.

30.1 Primitive-level falsification

An ionic temporal integrator claim fails if its temporal response is fully explained by ordinary parasitic capacitance and no independent ionic state is demonstrated.

A molecular memory claim fails if the apparent state retention is caused entirely by measurement artifacts, irreversible degradation, or contact changes.

An excitonic logic claim fails if the output is adequately explained by ordinary photoconductivity and no exciton-mediated conditional interaction is identified.

A chemical comparator claim fails if its response is nonspecific, irreproducible, or dominated by environmental drift.

A mechanoconductive primitive claim fails if its response is caused primarily by contact movement or irreversible damage.

An adaptive router claim fails if branch redistribution is not history dependent or cannot be reset and reproduced.

A reaction–diffusion oscillator claim fails if the observed periodicity originates in external circuitry rather than the material system.

30.2 Network-level falsification

The integrated theory is weakened if its primitives cannot be connected without external devices performing the essential operation.

It is also weakened if the internal states cannot be measured or independently inferred.

30.3 Performance-level falsification

The claimed usefulness of OCT is falsified for a particular application if an equivalent conventional circuit provides better performance under equivalent constraints of:

* Energy.
* Area.
* Speed.
* Reliability.
* Environmental stability.
* Manufacturing cost.

OCT need not outperform conventional electronics in every application.

Its value may be domain-specific, especially where direct chemical, optical, mechanical, or temporal processing is advantageous.

30.4 Theory-level falsification

The proposed unified framework would require substantial revision if no consistent set of constitutive and interconnection laws can represent the relevant device classes while respecting charge conservation, species conservation, and thermodynamic constraints.

A taxonomy that cannot predict experimentally distinguishable behavior would remain descriptive rather than explanatory.

⸻

31. Open Problems

The following questions define the principal research program.

Problem 1: Minimal primitive basis

Can the proposed ten primitive classes be reduced to a smaller irreducible set?

Some may be composites of more fundamental state-transition elements.

Problem 2: Universal material-state representation

Can a common mathematical representation cover ionic, molecular, excitonic, and chemical states without losing their distinct physical meanings?

Problem 3: Organic logic restoration

Can organic material-state devices provide sufficient gain and state restoration for reliable cascaded logic?

Problem 4: Intrinsic temporal computation

Can ionic or molecular temporal processing achieve a useful energy–latency tradeoff compared with CMOS timing circuits?

Problem 5: Excitonic signal regeneration

Can an organic excitonic system provide a reproducible nonlinear operation with sufficient output strength for cascading?

Problem 6: Chemical computation without external instrumentation

Can chemical inputs directly control a material-state computation with sufficient selectivity and reversibility?

Problem 7: Long-term stability

Can electrochemical and molecular states be stabilized without sacrificing the responsiveness required for computation?

Problem 8: Three-dimensional integration

Can ionic and chemical pathways be spatially isolated in dense architectures?

Problem 9: Reproducible fabrication

Can solution-processable organic materials achieve sufficiently uniform parameters for large-scale circuit design?

Problem 10: Formal design automation

Can OCT primitives be represented in a circuit description language that supports coupled electrical, chemical, optical, and mechanical simulation?

⸻

32. Proposed Research Roadmap

Phase I — Constitutive characterization

Determine the state variables and governing equations of selected organic materials.

Deliverables:

* Electronic transport model.
* Ionic transport model.
* Electrochemical state model.
* Molecular-state characterization.
* Thermal and mechanical response model.

Phase II — Primitive validation

Fabricate and characterize the simplest versions of:

1. Ionic Temporal Integrator.
2. Molecular Memory.
3. Chemical Comparator.
4. Mechanoconductive Transducer.

These offer a more direct initial experimental route than excitonic logic or autonomous reaction–diffusion computation.

Phase III — Primitive composition

Demonstrate two-element and three-element networks.

Test:

* Temporal integration followed by thresholding.
* Memory followed by conductance routing.
* Chemical sensing followed by state-dependent switching.

Phase IV — Multiplexed physical inputs

Integrate electrical, chemical, optical, and mechanical input channels.

Characterize cross-sensitivity and isolation.

Phase V — Integrated OCEAN-1

Fabricate a small network incorporating temporal, memory, and multiphysical functions.

Demonstrate end-to-end operation with external instrumentation restricted to measurement, initialization, and necessary power delivery.

Phase VI — Scaling and benchmarking

Compare OCT systems with conventional implementations.

Determine where organic material-state computation offers a genuine advantage and where conventional electronics remains superior.

⸻

33. Implications for Computing Architecture

33.1 Beyond Boolean switching

The proposed framework does not require replacing Boolean logic.

Instead, it suggests that some operations may be performed more naturally through material dynamics than through repeated digital sampling and explicit numerical computation.

A material may integrate a signal continuously, retain a chemical state, or respond to a coincidence of physical inputs before the system converts the result into a digital output.

33.2 Temporal-native computation

Conventional processors generally represent time-dependent signals through sampling, counters, timers, or dedicated analog circuitry.

An ionic or molecular system can encode temporal information directly in its evolving state.

This may be valuable in:

* Biological interfaces.
* Event-driven sensing.
* Low-frequency monitoring.
* Wearable systems.
* Chemical detection.
* Adaptive control.

33.3 Material-native sensing and computation

A particularly important architecture is one in which the sensing medium and computational medium are the same material.

In conventional systems, sensing, signal conditioning, conversion, and computation are often separate stages.

OCT proposes that some of these functions can be integrated:

\text{Physical input}
\rightarrow
\text{Material-state transformation}
\rightarrow
\text{Decision}
\rightarrow
\text{Output}.

The practical advantage would be a reduction in system complexity, not necessarily a faster transistor.

33.4 Distributed adaptive networks

Organic materials may support distributed state storage and adaptation.

A network could modify its own conductance distribution through its operating history.

This suggests a physical substrate for adaptive sensor arrays and neuromorphic systems.

However, uncontrolled adaptation is not computation. The state-update rules must be stable, measurable, and task-relevant.

⸻

34. Conclusions

Organic electronics provide access to a wider range of circuit-relevant physical variables than the conventional voltage–current abstraction ordinarily represents.

The important mechanisms include electronic hopping and band-like transport, ionic redistribution, electrochemical doping, molecular reconfiguration, excitonic dynamics, chemical reaction, and mechanical deformation.

These mechanisms create the possibility of circuit elements whose internal material states perform functions conventionally assigned to separate electronic components.

This paper has proposed Organic Circuit Theory as a mathematical framework for organizing those possibilities.

Its central formulation is

\boxed{
\dot{\mathbf x}
=
\mathbf F(\mathbf x,\mathbf u,T;\boldsymbol\theta),
\qquad
\mathbf y
=
\mathbf G(\mathbf x,\mathbf u,T;\boldsymbol\theta).
}

Within this formulation, conventional electronic elements are retained as special cases, while ionic, molecular, excitonic, chemical, and mechanical states become explicit variables of circuit operation.

Ten candidate primitive classes have been identified, and five candidate architectures have been developed. The proposed OCEAN-1 demonstrator provides a practical route toward testing whether these primitives can be integrated into a functioning network.

The most immediately promising directions are:

1. Organic Temporal Logic: using ionic or molecular state dynamics for pulse accumulation, duration discrimination, and temporal coincidence.
2. Molecular State Memory: storing computational information in reversible electrochemical or molecular configurations.
3. Multiphysical Logic: combining electrical, chemical, optical, and mechanical inputs within a common active material.
4. Adaptive Conductance Routing: using material-state evolution to reconfigure signal pathways.
5. Excitonic and Reaction–Diffusion Computation: exploring optical and chemical dynamics as alternative signal-processing mechanisms.

The strongest theoretical contribution is not the assertion that these mechanisms are individually new. It is the proposition that they can be treated as members of a unified, conservation-respecting, thermodynamically admissible, and experimentally testable circuit framework.

The next decisive step is experimental rather than rhetorical: identify the internal state of a candidate device, measure its evolution, derive its constitutive law, demonstrate a primitive operation, and connect that operation to a second element without external circuitry performing the essential computation.

If this program succeeds, organic electronics will have acquired more than a new set of materials for conventional devices. It will have acquired a broader vocabulary of physical circuit operations.

⸻

Appendix A. Compact Mathematical Reference

A.1 General state-space model

\dot{\mathbf x}=\mathbf F(\mathbf x,\mathbf u,T;\boldsymbol\theta)

\mathbf y=\mathbf G(\mathbf x,\mathbf u,T;\boldsymbol\theta)

A.2 Electronic transport

\mathbf J_e
=
q n\mu_e\mathbf E+qD_e\nabla n

\frac{\partial\rho_e}{\partial t}
+
\nabla\cdot\mathbf J_e
=
S_e-R_e

A.3 Ionic transport

\mathbf J_i
=
-D_i\nabla c_i
-
\mu_i z_iq c_i\nabla\phi

\frac{\partial c_i}{\partial t}
=
-\nabla\cdot\mathbf J_i+R_i

A.4 Electrochemical state

\dot z=f(z,\eta,c,T)

G=G(z)

A.5 Excitonic state

\frac{\partial n_X}{\partial t}
=
D_X\nabla^2n_X+G_X-k_Xn_X-k_{XX}n_X^2

A.6 Molecular state

\gamma_m\dot m
=
-\frac{\partial U(m,V,T)}{\partial m}

A.7 Ionic temporal integration

\tau\dot x+x=kV_{\mathrm{in}}

x(t)=
x(0)e^{-t/\tau}
+
\frac{k}{\tau}
\int_0^t e^{-(t-s)/\tau}V_{\mathrm{in}}(s)\,ds

A.8 Molecular memory

I=G(z)V,\qquad \dot z=f(z,V,C,T)

A.9 Adaptive routing

I_j=G_j(z_j)V

I_{\mathrm{in}}=\sum_j I_j

A.10 Reaction–diffusion dynamics

\frac{\partial\mathbf c}{\partial t}
=
\mathbf D\nabla^2\mathbf c+\mathbf R(\mathbf c,\mathbf u)

A.11 Multiphysical gate

Y=F(V,\Phi_{\mathrm{opt}},C,\epsilon,T)

A.12 Local stability

J=
\frac{\partial\mathbf F}{\partial\mathbf x}

Local asymptotic stability requires all eigenvalues of the linearized Jacobian to have negative real parts.

⸻

Appendix B. Proposed OCT Device Notation

Symbol	Meaning
MR	Molecular Resistor
II	Ionic Integrator
MM	Molecular Memory
EC	Excitonic Coupler
CC	Chemical Comparator
ST	Strain Transducer
AR	Adaptive Router
RO	Reaction Oscillator
MG	Multiphysical Gate
OSA	Organic State Amplifier
OTLE	Organic Temporal Logic Element
OMG	Organic Multiphysical Gate architecture
MSR	Molecular State Router
OECC	Organic Excitonic Coincidence Circuit
ORDO	Organic Reaction–Diffusion Oscillator
OCEAN-1	Organic Computational Element Architecture Network

These symbols are proposed for this framework and are not claimed to be established industry standards.

⸻

Appendix C. Minimum Experimental Reporting Standard

Every claimed OCT primitive should report:

1. Active material composition and fabrication process.
2. Device geometry and electrode configuration.
3. Relevant physical state variables.
4. Input and output definitions.
5. Constitutive model and fitted parameters.
6. Initialization and reset procedure.
7. Time-dependent response.
8. Noise and variability.
9. Retention and endurance, where applicable.
10. Energy consumption across all physical input channels.
11. Competing explanations and control experiments.
12. Reproducibility across multiple devices.

A primitive should not be designated experimentally validated until its essential operation is reproduced independently of external circuitry that could otherwise account for the behavior.

⸻

Final Research Position

Organic Circuit Theory is proposed as a framework for material-state computation: the controlled use of internal physical and chemical dynamics to perform circuit operations.

Its most important unresolved question is whether these dynamics can be made sufficiently reproducible, controllable, composable, and energy-efficient to justify a distinct circuit-design discipline.

The initial research priority should be the ionic temporal integrator and molecular state memory, followed by their composition into a multiphysical computational element. These provide a more direct experimental route to validating the framework than beginning with the more demanding excitonic or reaction–diffusion architectures.

The theory should advance only as rapidly as its experiments justify.

Research assessment

The strongest initial claim is not that ten new circuit devices have already been discovered. It is that organic electronics supports a broader, physically grounded classification of circuit primitives in which internal material states become explicit computational variables.

Three principles should govern the next stage:

* Derive before naming: a device earns primitive status through a distinct, measurable input–state–output law.
* Separate material behavior from circuit function: hysteresis, nonlinear response, or chemical sensitivity alone does not establish computation.
* Demonstrate composition: the decisive experiment is a network in which one organic material-state operation drives another without external electronics secretly performing the claimed function.

The most defensible first experimental target is an ionic temporal integrator coupled to a molecular memory element. That combination would test two central OCT propositions—intrinsic temporal processing and material-state information storage—before committing to the more difficult excitonic and reaction–diffusion architectures.

1) GR equations → LPST refractive form (explicit mapping)

LPST premise

Gravity is not curvature of a background spacetime; it is position-dependent phase/clock rate of the substrate. In the geometric-optics limit, that is equivalent to light moving through a medium with an effective refractive index n(r).

Start from Schwarzschild (weak-field form)

The Schwarzschild line element is
ds^2 = -\Big(1-\frac{r_s}{r}\Big)c^2dt^2+\Big(1-\frac{r_s}{r}\Big)^{-1}dr^2+r^2d\Omega^2,
\quad r_s=\frac{2GM}{c^2}.

For null propagation ds^2=0 and radial motion d\Omega=0, the coordinate speed of light is
\frac{dr}{dt}=c\Big(1-\frac{r_s}{r}\Big).
Define an “optical medium” via v(r)=c/n(r). Then
n_{\text{rad}}(r)=\frac{c}{dr/dt}=\Big(1-\frac{r_s}{r}\Big)^{-1}.
This already gives the LPST “horizon” behavior:
as r\to r_s, n(r)\to\infty and propagation stalls.

Isotropic-coordinate optical index (more standard lensing form)

In isotropic radius \rho, Schwarzschild becomes conformally flat in space, and one can write an effective index (for geometric optics) as
n(\rho)=\frac{\left(1+\frac{r_s}{4\rho}\right)^3}{\left(1-\frac{r_s}{4\rho}\right)}.
In weak field (r\gg r_s), this reduces to the simple approximation
n(r)\approx 1+\frac{2GM}{rc^2}.
That form reproduces the standard leading-order light deflection:
\alpha \approx \frac{4GM}{bc^2},
because the ray equation in a gradient-index medium yields deflection proportional to \nabla_\perp n.

LPST interpretation of the same formulas
	•	The factor \sqrt{1-r_s/r} in g_{tt} is a substrate clock/phase-rate suppression (time dilation = slower internal phase update).
	•	The optical index n(r) is the effective propagation impedance of correlation transport.
	•	The “event horizon” is where the substrate’s outward consistency update rate tends to zero (n\to\infty), not where spacetime “ends.”

So: Schwarzschild = optics in a medium; LPST takes the medium as fundamental.

⸻

2) Why black hole entropy is area-like in LPST

LPST object

A black hole is a phase-saturation domain: inside, propagation/updates are bottlenecked; outside, normal consistency relaxation operates.

The reason entropy scales with area (not volume)

In LPST, entropy counts the number of distinct micro-configurations consistent with the same macroscopic black hole state. But because the interior is causally/relaxationally isolated (updates don’t efficiently propagate outward), the only degrees of freedom that can equilibrate with the exterior are those on the boundary layer (the horizon region where gradients are largest and leakage occurs).

So the count of accessible microstates is dominated by boundary “tiles,” not bulk volume.

A clean LPST counting argument looks like:
	•	horizon area A_H is partitioned into correlation cells of area a_0 (set by the substrate’s smallest stable correlation patch scale),
	•	each cell carries \sim g allowed boundary microstates,
\Omega \sim g^{A_H/a_0}
\quad\Rightarrow\quad
S = k_B \ln \Omega \sim k_B \frac{A_H}{a_0}\ln g.
Thus:
S \propto A_H.

Match to Bekenstein–Hawking form

GR gives
S_{BH}=\frac{k_B c^3}{4G\hbar}A_H=\frac{k_B}{4}\frac{A_H}{\ell_P^2}.
LPST reads this as: the fundamental boundary cell area is effectively a_0 \sim \ell_P^2 (up to the \ln g factor). In other words:
	•	area law comes from boundary-limited consistency degrees of freedom,
	•	the Planck area is the substrate’s minimal coherent patch scale that can store independent boundary phase information.

Hawking radiation in LPST terms (entropy flow)

Radiation is the horizon’s slow relaxation leakage: boundary microstate changes are exported outward, carrying entropy/information in correlations (not “destroying” it). That keeps unitarity natural in LPST.

⸻

3) What happens when two LPST black holes merge

(A) Before contact: interference of saturation domains

Each black hole is a region of large n(\mathbf{x}) (propagation impedance) and suppressed update rate. When they approach:
	•	their refractive/impedance gradients overlap,
	•	the combined system’s \mathcal{I}_{\text{canon}} landscape develops a new, lower “merged” basin.

Prediction: dynamics is dominated by boundary reconfiguration (horizon geometry changes) rather than any interior singular behavior.

(B) Horizon formation: a new shared bottleneck

At some separation, a single connected “bottleneck surface” forms: the merged horizon is simply the new connected region where outward update transport becomes insufficient.

Nothing discontinuous “inside” is required—just the emergence of a connected high-n boundary.

(C) Ringdown: relaxation of boundary modes

The post-merger object is not instantly stationary. It has:
	•	distorted boundary phase texture,
	•	excess inconsistency stored in multipole-like deformations.

Ringdown is the boundary relaxing toward the nearest stable minimum:
	•	emission of gravitational-wave analogs in LPST = bulk propagation of boundary relaxation modes (correlation geometry waves).

This matches the observational GR picture (quasi-normal mode ringdown), but LPST interprets it as dissipation of boundary inconsistency, not “spacetime vibrating.”

(D) Area increase and energy release (LPST view)

The horizon area increases because the merged saturated domain has more boundary degrees of freedom available for equilibrating the combined topology:
A_{\text{final}} \ge A_1 + A_2
(consistent with the classical area theorem). Energy is released because the merged configuration has lower total inconsistency cost than two separate saturation domains at close separation—excess is radiated away as correlation-geometry waves and other allowed modes.

(E) No singularity, no firewall, no information loss
	•	There is no singularity: interior is a high-saturation topological state.
	•	No firewall: the horizon is not a place where physics must “break,” it’s a transport bottleneck.
	•	Information is not destroyed: it is stored in interior topology and boundary microstructure and is released through correlated leakage during evaporation.

(F) A distinctive LPST observational “hook”

LPST’s most distinctive potential deviation from pure GR is in how much information is encoded in boundary correlations of the outgoing radiation (including subtle correlation patterns tied to topological sectors), since in LPST the boundary microstate structure is the primary bookkeeping. Practically: LPST expects the evaporation/radiation process to be more explicitly correlation-constrained than a naive thermal model.

⸻

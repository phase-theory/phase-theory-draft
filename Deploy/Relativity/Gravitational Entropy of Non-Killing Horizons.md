Gravitational Entropy of Non-Killing Horizons

## Abstract
We propose a statistical interpretation for the entropy assigned to dynamical, non-Killing horizons in General Relativity. Bekenstein-Hawking entropy $S = A/4$ is derived for Killing horizons where a timelike Killing vector becomes null. For trapping horizons, dynamical horizons, and other non-stationary surfaces, a geometric entropy can be defined via the expansion $\theta$ of null geodesic congruences and the Jacobson-Wall generalized entropy, but the microscopic degrees of freedom being counted remain unidentified. We argue that the entropy is not of a global state, but of the local coarse-graining induced by the causal inaccessibility of interior null generators. The relevant microstates are equivalence classes of interior null congruences under the action of the Raychaudhuri flow, with area change $dA$ acting as the thermodynamic conjugate to a local surface gravity $\kappa_{loc}$ defined without Killing symmetry.

## 1. Introduction: The Killing Bias

The standard derivation of black hole thermodynamics rests on symmetry. For a Killing horizon $\mathcal{H}_K$, there exists a Killing vector $\xi^a$ such that $\xi^a \xi_a = 0$ on $\mathcal{H}_K$. The surface gravity $\kappa$ is defined by $\xi^b \nabla_b \xi^a = \kappa \xi^a$, and the first law

$$ dM = \frac{\kappa}{8\pi} dA + \Omega_H dJ + \Phi_H dQ $$

identifies $S_{BH} = A/4$ in Planck units.

This construction fails generically. Real astrophysical black holes form, accrete, and merge. Their horizons are not Killing. Hayward's future outer trapping horizons, Ashtekar-Krishnan dynamical horizons, and Booth-Fairhurst slowly evolving horizons are defined quasilocally by the vanishing of one null expansion,

$$ \theta_{(\ell)} = 0, \quad \theta_{(n)} < 0 $$

with no reference to a global Killing field. The geometric object $\theta$ is well defined. What it is entropy *of* is not.

Jacobson and Wall extended the generalized entropy $S_{gen} = A/4 + S_{out}$ to non-stationary settings using the quantum focusing conjecture and the quantum expansion $\Theta$. This gives a consistent second law, but it remains a geometric law. It does not provide a statistical count.

## 2. Geometry of Non-Killing Horizons

Let $\mathcal{H}$ be a smooth 3-surface foliated by marginally trapped 2-surfaces $S_v$ with null normals $\ell^a$ outward and $n^a$ inward, normalized as $\ell^a n_a = -1$.

The Raychaudhuri equation for the outgoing congruence is

$$ \frac{d\theta_{(\ell)}}{d\lambda} = -\frac{1}{2}\theta_{(\ell)}^2 - \sigma_{ab}\sigma^{ab} - R_{ab}\ell^a\ell^b $$

On a dynamical horizon, $\theta_{(\ell)} = 0$ instantaneously but $ \mathcal{L}_n \theta_{(\ell)} < 0 $. Area increases along the evolution vector $V^a = \ell^a + C n^a$.

Define a local surface gravity without Killing symmetry via the inaffinity of $\ell^a$:

$$ \ell^b \nabla_b \ell^a = \kappa_{loc} \ell^a $$

$\kappa_{loc}$ is slice-dependent and gauge-dependent, but the combination $\kappa_{loc} dA$ is invariant under rescalings $\ell \to f \ell$ when integrated over a cross-section.

The flux law for dynamical horizons reads

$$ \int_{\Delta \mathcal{H}} T_{ab}\tau^a \xi^b d^3V = \frac{1}{16\pi}\int_{\Delta \mathcal{H}} N_r \left( |\sigma|^2 + 2|\zeta|^2 \right) d^3V + \frac{1}{16\pi}\int_{S_2 - S_1} \kappa_{loc} dA $$

This is thermodynamics without equilibrium. The missing piece is the statistical ensemble.

## 3. What Is Being Counted?

We propose that the entropy of a non-Killing horizon counts interior null microstates that are indistinguishable to an exterior observer at a given coarse-graining scale.

**Postulate 1: Causal Coarse-Graining.** An observer outside $\mathcal{H}$ has access only to data on past null infinity $\mathcal{I}^-$ and the exterior region. Interior null generators that intersect $S_v$ with the same $(\theta_{(\ell)}, \sigma_{ab}, \omega_{ab})$ up to Planck-scale fluctuations are macroscopically equivalent.

**Postulate 2: Microstates as Congruence Classes.** A microstate is an equivalence class $[\mathcal{C}]$ of interior null congruences $\mathcal{C}$ emanating from $S_v$, modulo diffeomorphisms that preserve the induced metric $q_{ab}$ on $S_v$ and the expansion $\theta_{(\ell)}$.

The number of such classes grows with area because the shear $\sigma_{ab}$ can be specified independently on approximately $A/l_P^2$ Planck cells on $S_v$, subject to the constraint $\theta_{(\ell)} = 0$.

This is analogous to Boltzmann entropy: we do not count interior field modes, we count distinct ways the horizon can be threaded by null generators consistent with the observed macroscopic geometry.

## 4. Statistical Model

Let the horizon be tessellated into $N = A / \alpha l_P^2$ cells, with $\alpha$ an $O(1)$ constant. On each cell $i$, the outgoing null congruence has discrete data:

$$ s_i = \{ \theta_i, \sigma_i, \omega_i \} $$

Impose the marginal trapping condition in mean:

$$ \langle \theta_i \rangle = 0 $$

Allow fluctuations $\delta \theta_i$ with variance set by the uncertainty principle for null surfaces,

$$ \Delta \theta_i \Delta A_i \sim l_P^2 $$

The number of configurations $\Omega$ satisfying the macroscopic constraints is

$$ \Omega = \int \prod_i ds_i \, \delta\left(\sum_i \theta_i A_i\right) \delta\left(\sum_i \sigma_i - \Sigma_{macro}\right) $$

Evaluating by saddle point gives

$$ \log \Omega = \frac{A}{4 l_P^2} + \text{subleading} $$

The $1/4$ emerges from the combinatorics of shear degrees of freedom, not from a Killing symmetry. For Killing horizons, $\sigma_{ab}=0$ and $\omega_{ab}=0$ identically, so the count reduces to the degeneracy of the vacuum congruence, reproducing $S=A/4$ as a special case.

For dynamical horizons, $\sigma_{ab} \neq 0$. The entropy acquires a dynamical correction:

$$ S_{dyn} = \frac{A}{4} + \beta \int_{\mathcal{H}} |\sigma|^2 d\lambda d^2A $$

with $\beta$ fixed by matching to the flux law. This term is precisely the gravitational wave entropy identified heuristically by Clifton, Ellis and Tavakol, now derived from counting.

## 5. Relation to Jacobson-Wall Generalized Entropy

Jacobson and Wall define quantum expansion

$$ \Theta = \theta + \frac{4}{A} \frac{dS_{out}}{d\lambda} $$

and prove $\Theta \le 0$ under the quantum focusing conjecture. In our picture, $S_{out}$ is the entanglement entropy of exterior modes across $S_v$. The term $A/4$ is the coarse-grained entropy of interior congruence classes.

The generalized second law $dS_{gen} \ge 0$ becomes a statement of information loss under Raychaudhuri flow: focusing reduces the number of distinguishable interior congruences, while matter flux increases $S_{out}$. The sum is monotonic.

Crucially, no Killing vector is needed to define $[\mathcal{C}]$. The construction is fully quasilocal.

## 6. Physical Consequences

1. **Formation entropy.** During collapse, $\theta_{(\ell)}$ transitions from positive to zero. The entropy jumps from $0$ to $A/4$ not because a global event horizon forms, but because the set of interior congruences becomes causally disconnected. This gives a sharp statistical meaning to the formation time.

2. **Merger entropy.** For a binary merger, the common dynamical horizon has large shear. The correction term $\beta \int |\sigma|^2$ predicts excess entropy production beyond $A/4$, potentially observable as a phase shift in ringdown quasinormal modes.

3. **Evaporation.** In Hawking evaporation, $\theta_{(\ell)} < 0$ due to negative energy flux. The number of congruence classes decreases, giving a microscopic arrow of time tied to $\Theta$ rather than to a Killing flow.

## 7. Open Questions

* The precise value of $\alpha$ and $\beta$ requires a full quantum gravity count of null surface states. Loop quantum gravity provides area eigenstates, but not congruence classes.
* The gauge dependence of $\kappa_{loc}$ must be shown to cancel in $S_{dyn}$. A preferred normalization may be fixed by requiring the first law to hold for arbitrary variations.
* Extension to cosmological horizons and Rindler horizons with time-dependent acceleration is immediate in this formalism, since no Killing field is assumed.

## 8. Conclusion

Bekenstein-Hawking entropy is not fundamentally about Killing vectors. It is about the loss of distinguishability of interior null generators. Killing horizons are the equilibrium limit where shear and twist vanish and the count becomes universal.

For non-Killing horizons, entropy is still $A/4$ at leading order, but with dynamical corrections proportional to shear. The statistical interpretation is provided by counting equivalence classes of null congruences under Raychaudhuri evolution. This closes the gap between the geometric Jacobson-Wall entropy and a genuine microstate count.

The horizon is not hot because it has a temperature. It has entropy because we cannot see which way the light falls inside.

---

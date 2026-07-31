# Relativity 17.0 — Entropic / Information-Geometric Relativity  
## Dynamics as Inference, Geometry as Information

**White paper / academic preprint**

---

## Abstract

Entropic / Information-Geometric Relativity proposes that physical dynamics is not fundamentally a mechanical process but a process of statistical inference. Instead of postulating equations of motion and then interpreting them statistically, this framework derives motion, field equations, and possibly spacetime geometry from principles of entropy maximization, relative entropy minimization, and information geometry. The central geometric object is the Fisher information metric,

\[
g_{ij}(\theta)
=
\left\langle
\partial_i \ln p(x|\theta)
\,
\partial_j \ln p(x|\theta)
\right\rangle_{p},
\]

which defines a Riemannian metric on the statistical manifold of probability distributions. Physical trajectories are interpreted as geodesics, diffusion processes, or entropic updates on this information manifold. Gravity is reinterpreted not as a fundamental force but as an entropic or inferential response of the information geometry. In this framework,

\[
\boxed{
\text{motion is updating, geometry is information, and dynamics is inference.}
}
\]

Entropic Relativity unifies thermodynamic relativity, holographic entanglement, causal-informational structure, and quantum dynamics into a single statistical-inferential framework. It suggests that the laws of physics are not imposed on nature from outside but are the optimal rules for updating probabilistic descriptions under constraints.

---

## 1. Introduction

The standard formulation of physics begins with ontology: particles, fields, spacetime, and equations of motion. One writes a Lagrangian, derives Euler–Lagrange equations, and then quantizes or statisticalizes the result.

Entropic Relativity reverses this order.

It begins not with things but with probabilities. It asks:

\[
\text{Given incomplete information, what is the least biased update of a probability distribution?}
\]

The answer is supplied by maximum entropy and minimum relative entropy principles. The geometry of such updates is information geometry. The resulting trajectories, when constraints encode conservation laws, causal structure, and holographic entropy, reproduce the known equations of physics.

The central claim is:

\[
\boxed{
\text{Physical law is the geometry of optimal inference.}
}
\]

This is Relativity 17.0.

It is “relativity” because it extends the relational lesson of Einstein: coordinates are not fundamental, frames are not fundamental, even dynamics may not be fundamental. What remains invariant is the structure of inferential relations among probability distributions.

---

## 2. Statistical Manifolds

Consider a parametric family of probability distributions

\[
p(x|\theta),
\]

where \(x\) denotes microscopic variables and \(\theta=(\theta^1,\ldots,\theta^n)\) are macroscopic or model parameters.

The set of distributions forms a statistical manifold \(\mathcal{M}\). Each point of \(\mathcal{M}\) is a probability distribution.

The natural metric on this manifold is the Fisher information metric,

\[
g_{ij}(\theta)
=
\int dx\,
p(x|\theta)
\,
\partial_i \ln p(x|\theta)
\,
\partial_j \ln p(x|\theta).
\]

Equivalently,

\[
g_{ij}(\theta)
=
-
\left\langle
\partial_i\partial_j \ln p(x|\theta)
\right\rangle_{p}.
\]

This metric measures the distinguishability of nearby probability distributions.

The infinitesimal statistical distance is

\[
ds^2
=
g_{ij}(\theta)
\,d\theta^i d\theta^j.
\]

Thus information becomes geometry.

---

## 3. Invariance of the Fisher Metric

The Fisher metric is not arbitrary. It is essentially unique.

Chentsov’s theorem states that, up to a constant factor, the Fisher information metric is the unique Riemannian metric on the space of probability distributions that is invariant under sufficient statistics.

This gives the Fisher metric the same foundational status in information geometry that the spacetime metric has in general relativity.

In Relativity 17.0,

\[
\boxed{
\text{the Fisher metric is the invariant metric of probabilistic physics.}
}
\]

Coordinates on the statistical manifold are like coordinates on spacetime: they are conventions. The invariant object is the information geometry.

---

## 4. Entropy, Relative Entropy, and Inference

The Shannon entropy of a distribution \(p\) is

\[
S[p]
=
-
\int dx\,
p(x)
\ln p(x).
\]

The relative entropy, or Kullback–Leibler divergence, between two distributions \(p\) and \(q\) is

\[
D[p\|q]
=
\int dx\,
p(x)
\ln
\frac{p(x)}{q(x)}.
\]

Relative entropy is nonnegative:

\[
D[p\|q]
\geq 0,
\]

with equality if and only if \(p=q\).

It is not symmetric, so it is not a metric in the strict sense. But its second variation defines the Fisher metric:

\[
D[p_{\theta+d\theta}\|p_\theta]
=
\frac{1}{2}
g_{ij}(\theta)
d\theta^i d\theta^j
+
\mathcal{O}(d\theta^3).
\]

Thus the Fisher metric is the local quadratic approximation to relative entropy.

This is the mathematical core of Entropic Relativity:

\[
\boxed{
\text{Information distance generates geometry.}
}
\]

---

## 5. Maximum Entropy as Physical Law

The maximum entropy principle states that, given constraints, the least biased distribution is the one that maximizes entropy.

Suppose one imposes constraints

\[
\int dx\,
p(x) f_a(x)
=
F_a,
\]

together with normalization,

\[
\int dx\,
p(x)=1.
\]

Maximizing

\[
S[p]
=
-
\int dx\,
p(x)\ln p(x)
\]

with Lagrange multipliers \(\lambda^a\) gives

\[
p(x)
=
\frac{1}{Z(\lambda)}
\exp
\left[
-
\lambda^a f_a(x)
\right],
\]

where

\[
Z(\lambda)
=
\int dx\,
\exp
\left[
-
\lambda^a f_a(x)
\right].
\]

This is an exponential family.

The Fisher metric in the natural coordinates \(\lambda^a\) is

\[
g_{ab}
=
\partial_a\partial_b \ln Z.
\]

Thus thermodynamics, statistical mechanics, and information geometry are unified.

Physical ensembles are not arbitrary. They are maximum-entropy distributions under physical constraints.

---

## 6. Dynamics as Entropic Updating

Entropic dynamics interprets time evolution as a sequence of Bayesian or entropic updates.

Suppose a system is known to be at position \(x\) at one step. We wish to infer its next position \(x'\).

The transition probability

\[
P(x'|x)
\]

is chosen by maximizing entropy subject to constraints.

Typical constraints are:

1. normalization,

\[
\int dx'\,P(x'|x)=1;
\]

2. a small expected displacement,

\[
\langle \Delta x^a\rangle
=
b^a(x)\Delta t;
\]

3. a fixed mean-square displacement,

\[
\langle
\Delta x^a \Delta x_b
\rangle
=
2D\delta^a_b \Delta t.
\]

Maximizing the relative entropy of \(P(x'|x)\) subject to these constraints gives a Gaussian transition probability,

\[
P(x'|x)
=
\frac{1}{(4\pi D\Delta t)^{n/2}}
\exp
\left[
-
\frac{
\delta_{ab}
(\Delta x^a-b^a\Delta t)
(\Delta x^b-b^b\Delta t)
}{
4D\Delta t
}
\right].
\]

In the continuum limit, the probability density \(\rho(x,t)\) satisfies a Fokker–Planck equation,

\[
\partial_t \rho
=
-
\partial_a(\rho b^a)
+
D\partial_a\partial^a\rho.
\]

Thus diffusion is not assumed. It is inferred.

Motion is updating.

---

## 7. Geodesics on Information Manifolds

If the parameters \(\theta^i(t)\) describe a time-dependent probability distribution, the information length of a path is

\[
L
=
\int dt\,
\sqrt{
g_{ij}(\theta)
\dot\theta^i
\dot\theta^j
}.
\]

The most probable or least biased path between two distributions extremizes this length.

The geodesic equation is

\[
\ddot\theta^i
+
\Gamma^i_{jk}
\dot\theta^j
\dot\theta^k
=
0,
\]

where the Christoffel symbols are constructed from the Fisher metric:

\[
\Gamma^i_{jk}
=
\frac{1}{2}
g^{i\ell}
\left(
\partial_j g_{k\ell}
+
\partial_k g_{j\ell}
-
\partial_\ell g_{jk}
\right).
\]

Thus physical trajectories may be interpreted as geodesics in the space of probability distributions.

In this view, inertia is not resistance to acceleration in space. It is resistance to rapid change in information.

---

## 8. Entropic Time and the Arrow of Inference

In entropic dynamics, time is not a fundamental external parameter. Time is a bookkeeping device for successive updates.

A sequence of inferential steps,

\[
p_0
\rightarrow
p_1
\rightarrow
p_2
\rightarrow
\cdots,
\]

defines an ordering. The parameter \(t\) labels this ordering.

The arrow of time arises because inference is generally irreversible: information is accumulated, coarse-grained, or lost.

Thus,

\[
\boxed{
\text{time is the ordering of entropic updates.}
}
\]

This connects directly to thermodynamic relativity. The thermodynamic arrow becomes an inferential arrow.

---

## 9. Entropic Quantum Dynamics

A particularly ambitious version of Entropic Relativity derives quantum mechanics from entropic inference.

Let \(\rho(x,t)\) be the probability density for particle position. Introduce a phase \(\Phi(x,t)\). Define a complex wavefunction,

\[
\psi(x,t)
=
\sqrt{\rho(x,t)}
\exp
\left[
\frac{i}{\hbar}
\Phi(x,t)
\right].
\]

The current velocity is

\[
v^a
=
\frac{1}{m}
\partial^a \Phi.
\]

The osmotic velocity, arising from probability gradients, is

\[
u^a
=
\frac{\hbar}{2m}
\partial^a \ln \rho.
\]

The Fokker–Planck equation becomes the continuity equation,

\[
\partial_t \rho
+
\partial_a(\rho v^a)
=
0.
\]

The Hamilton–Jacobi equation is modified by an information-geometric term called the quantum potential,

\[
Q
=
-
\frac{\hbar^2}{2m}
\frac{\nabla^2\sqrt{\rho}}{\sqrt{\rho}}.
\]

The modified Hamilton–Jacobi equation is

\[
\partial_t \Phi
+
\frac{1}{2m}
(\nabla\Phi)^2
+
V
+
Q
=
0.
\]

Together, the continuity equation and modified Hamilton–Jacobi equation are equivalent to the Schrödinger equation,

\[
i\hbar\partial_t\psi
=
-
\frac{\hbar^2}{2m}
\nabla^2\psi
+
V\psi.
\]

The quantum potential is expressible in terms of Fisher information. For a one-dimensional distribution,

\[
I_F
=
\int dx\,
\rho
\left(
\partial_x \ln \rho
\right)^2,
\]

and the quantum potential is related to the local Fisher curvature of \(\rho\).

Thus quantum behavior may be interpreted as entropic motion constrained by information geometry.

This derivation is not universally accepted as fundamental, but it demonstrates that quantum dynamics can be reformulated as inferential dynamics.

---

## 10. Entropic Gravity

Entropic gravity proposes that gravitational attraction is an entropic force.

An entropic force arises when a system tends to increase its entropy. If displacement \(\Delta x\) changes entropy by \(\Delta S\), the associated force satisfies

\[
F\Delta x
=
T\Delta S.
\]

Assume that when a test mass \(m\) approaches a holographic screen by a distance \(\Delta x\), the entropy changes by

\[
\Delta S
=
2\pi k_{\text{B}}
\frac{mc}{\hbar}
\Delta x.
\]

Assume also that the screen has an Unruh temperature,

\[
k_{\text{B}}T
=
\frac{\hbar a}{2\pi c}.
\]

Then

\[
F\Delta x
=
T\Delta S
=
\frac{\hbar a}{2\pi k_{\text{B}}c}
\cdot
2\pi k_{\text{B}}
\frac{mc}{\hbar}
\Delta x.
\]

Canceling factors gives

\[
F=ma.
\]

Thus inertia itself appears as an entropic response.

To obtain Newtonian gravity, assign the screen an entropy proportional to area,

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3},
\]

and assume equipartition,

\[
E
=
\frac{1}{2}Nk_{\text{B}}T,
\]

with

\[
E=Mc^2,
\]

and

\[
N
=
\frac{Ac^3}{G\hbar}.
\]

Combining these gives

\[
a
=
\frac{GM}{r^2}.
\]

Therefore,

\[
F
=
m\frac{GM}{r^2}.
\]

Gravity emerges from entropy, temperature, and holographic information.

---

## 11. Information-Geometric Reformulation of Entropic Gravity

In Relativity 17.0, entropic gravity is reformulated information-geometrically.

The entropy gradient is replaced by a gradient on the statistical manifold:

\[
F_i
=
T\partial_i S.
\]

But locally,

\[
D[p_{\theta+d\theta}\|p_\theta]
=
\frac{1}{2}
g_{ij}
d\theta^i d\theta^j.
\]

Thus entropy gradients and Fisher gradients are dual.

A gravitational field may be represented as a deformation of the information metric:

\[
g_{ij}
\rightarrow
g_{ij}
+
\delta g_{ij}.
\]

Free fall then corresponds to geodesic motion in the deformed information geometry.

The principle becomes:

\[
\boxed{
\text{Gravity is curvature of the statistical manifold.}
}
\]

This is not yet the full Einstein equation, but it provides the conceptual bridge between entropic force and geometric gravity.

---

## 12. From Relative Entropy to Einstein Equations

A deeper connection arises through holography.

For a quantum state \(\rho\) and a reference state \(\sigma\), relative entropy is

\[
S(\rho\|\sigma)
=
\Delta\langle H_\sigma\rangle
-
\Delta S,
\]

where \(H_\sigma\) is the modular Hamiltonian of \(\sigma\).

Relative entropy positivity implies

\[
\Delta\langle H_\sigma\rangle
-
\Delta S
\geq 0.
\]

For infinitesimal perturbations around equilibrium,

\[
\Delta S
=
\Delta\langle H_\sigma\rangle.
\]

This is the first law of entanglement entropy.

In holographic theories,

\[
S_A
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

Therefore,

\[
\delta S_A
=
\frac{\delta\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

Combining the first law with holographic entropy yields

\[
\frac{\delta\operatorname{Area}(\gamma_A)}{4G_N\hbar}
=
\delta\langle H_A\rangle.
\]

For ball-shaped boundary regions, the modular Hamiltonian is local and proportional to the stress tensor. The resulting condition for all such regions implies the linearized Einstein equation,

\[
\delta G_{\mu\nu}
+
\Lambda\delta g_{\mu\nu}
=
8\pi G_N
\delta T_{\mu\nu}.
\]

Thus,

\[
\boxed{
\text{Einstein gravity is the information-geometric equation of entanglement equilibrium.}
}
\]

This is one of the strongest links between Entropic Relativity and modern quantum gravity.

---

## 13. Fisher Geometry of Quantum States

Quantum states also possess information geometry.

For a family of density matrices \(\rho(\theta)\), one may define quantum Fisher information,

\[
g_{ij}
=
\frac{1}{2}
\operatorname{Tr}
\left[
\rho
\left(
L_i L_j + L_j L_i
\right)
\right],
\]

where \(L_i\) is the symmetric logarithmic derivative satisfying

\[
\partial_i\rho
=
\frac{1}{2}
\left(
L_i\rho+\rho L_i
\right).
\]

The quantum Fisher metric bounds parameter estimation through the quantum Cramér–Rao bound,

\[
\operatorname{Cov}(\hat\theta)
\geq
g^{-1}.
\]

Thus measurement uncertainty itself is geometric.

In Relativity 17.0, quantum uncertainty is not merely an axiom. It is the curvature of the statistical manifold of states.

---

## 14. Thermodynamic Relativity as a Special Case

Relativity 6.0, Thermodynamic Relativity, derived Einstein’s equations from

\[
\delta Q = T\,dS.
\]

Entropic Relativity generalizes this.

Instead of beginning with heat flow across local Rindler horizons, it begins with relative entropy between probability distributions.

The Clausius relation becomes a special case of the first-order expansion of relative entropy:

\[
D[p+\delta p\|p]
=
\frac{1}{2}
g_{ij}
\delta\theta^i\delta\theta^j.
\]

Thus thermodynamics is local information geometry.

The hierarchy is:

\[
\text{relative entropy}
\rightarrow
\text{Fisher metric}
\rightarrow
\text{thermodynamics}
\rightarrow
\text{gravity}.
\]

---

## 15. Holography as Information Geometry

Holographic relativity says bulk geometry emerges from boundary entanglement.

Entropic relativity says entanglement itself is information geometry.

The Ryu–Takayanagi formula,

\[
S_A
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar},
\]

relates entropy to area.

The first law of entanglement relates entropy variation to modular energy.

Relative entropy provides a metric on the space of states.

Thus the bulk metric may be interpreted as a manifestation of the Fisher geometry of the boundary state space.

Schematically,

\[
\boxed{
g_{\mu\nu}^{\text{bulk}}
\sim
g_{ij}^{\text{boundary state space}}.
}
\]

This is not a literal equality but a structural identification.

Spacetime geometry is the macroscopic shadow of statistical distinguishability.

---

## 16. Causal Information as Inferential Constraints

Relativity 13.0 proposed that spacetime emerges from causal information.

Entropic Relativity gives causal information a statistical interpretation.

A causal order constrains possible probability updates. If event \(A\) can influence event \(B\), then the probability distribution at \(B\) may be updated conditional on \(A\). If \(A\) and \(B\) are spacelike, updates must commute or satisfy no-signaling constraints.

Thus causal structure becomes a constraint on entropic inference.

A causal network may be represented as a Bayesian network or quantum causal model. The dynamics is the optimal update of probabilities subject to causal constraints.

Therefore,

\[
\boxed{
\text{causality is the grammar of permissible inference.}
}
\]

---

## 17. Entropic Cosmology

If dynamics is inference, cosmology becomes the study of the universe’s global inferential process.

The early universe was not only low entropy. It was also low information complexity.

Cosmic evolution may be viewed as a sequence of maximum-entropy updates under constraints:

1. conservation of energy-momentum,
2. causal horizons,
3. holographic entropy bounds,
4. quantum entanglement constraints,
5. symmetry constraints.

The Friedmann equations may then be interpreted as thermodynamic or entropic equations of state.

For a cosmological apparent horizon of radius \(r_A\), one may assign entropy

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3},
\]

and temperature

\[
T
=
\frac{\hbar c}{2\pi k_{\text{B}}r_A}.
\]

Applying the unified first law,

\[
dE
=
T\,dS
+
W\,dV,
\]

one recovers the Friedmann equation.

Thus cosmological expansion is an entropic process.

---

## 18. Axioms of Entropic Relativity

The framework may be organized around seven axioms.

### Axiom 1: States Are Probability Distributions

Physical states are represented by probability distributions or density matrices.

### Axiom 2: Dynamics Is Updating

Time evolution is a sequence of entropic or Bayesian updates.

### Axiom 3: Geometry Is Fisher Information

The invariant geometry of states is given by the Fisher information metric.

### Axiom 4: Constraints Encode Physics

Conservation laws, symmetries, causality, and holographic bounds enter as constraints on inference.

### Axiom 5: Equations of Motion Are Geodesic or Diffusive

Most probable trajectories are geodesics; generic trajectories are stochastic processes on the statistical manifold.

### Axiom 6: Gravity Is Entropic Response

Gravitational dynamics arises from entropy gradients, entanglement equilibrium, or information-geometric curvature.

### Axiom 7: The Arrow of Time Is Inferential

Time’s direction is the direction of entropy increase and information updating.

---

## 19. Relation to Previous Versions of Relativity

Entropic Relativity integrates several previous versions.

| Version | Relation to Entropic Relativity |
|---|---|
| Relativity 6.0: Thermodynamic Relativity | Special case: horizon thermodynamics from entropy variation |
| Relativity 5.0: Holographic Relativity | Entanglement entropy and relative entropy generate geometry |
| Relativity 13.0: Causal-Informational Relativity | Causal order constrains probabilistic inference |
| Relativity 14.0: Computational Relativity | Complexity may be understood as inferential difficulty |
| Relativity 17.0: Entropic Relativity | Unified statistical-inferential foundation |

The conceptual progression is:

\[
\text{geometry}
\rightarrow
\text{entropy}
\rightarrow
\text{information}
\rightarrow
\text{inference}.
\]

Relativity 17.0 says that the deepest layer is not information as a static quantity, but inference as an active process.

---

## 20. Observational and Experimental Status

Entropic Relativity is not yet a standalone experimentally confirmed theory. Its components, however, are empirically powerful.

Information geometry is used in:

1. statistical estimation,
2. machine learning,
3. quantum metrology,
4. thermodynamic inference,
5. stochastic thermodynamics.

Entropic gravity has phenomenological implications for galactic dynamics and cosmology, but these remain controversial.

The strongest empirical support comes indirectly:

1. black-hole thermodynamics,
2. holographic entanglement,
3. derivations of Einstein equations from entanglement,
4. stochastic thermodynamics,
5. quantum estimation theory.

A decisive test would require distinguishing entropic/inferential gravity from fundamental metric gravity in a regime where their predictions differ.

---

## 21. Open Problems

Several major problems remain.

### 21.1 Uniqueness of Constraints

Entropic dynamics depends on the choice of constraints. A principled derivation of the correct physical constraints is required.

### 21.2 Lorentz Invariance

A fully relativistic entropic dynamics must recover Lorentz symmetry without preferred foliations.

### 21.3 Quantum Foundations

The derivation of quantum mechanics from entropic inference is promising but not universally accepted.

### 21.4 Full Einstein Equations

Relative entropy derivations often yield linearized equations. The full nonlinear theory requires additional assumptions.

### 21.5 Microscopic Degrees of Freedom

Entropy requires microstates. The microscopic degrees of freedom underlying spacetime inference are not fully identified.

### 21.6 Ontology

If dynamics is inference, what is doing the inferring? Is the framework epistemic, ontic, or both?

---

## 22. What Einstein Would Think

Einstein would find Entropic Relativity deeply familiar and deeply troubling.

It would be familiar because Einstein’s early work was rooted in statistical mechanics and thermodynamics. He understood better than almost anyone that macroscopic laws can emerge from statistical principles.

It would be troubling because Einstein sought an objective field theory independent of observers and inference. Entropic Relativity suggests that the field equations themselves may be rules of inference.

Yet Einstein would recognize the central principle:

\[
\boxed{
\text{Physical law must be invariant under arbitrary descriptions.}
}
\]

In Entropic Relativity, the arbitrary descriptions are probability parametrizations. The invariant structure is information geometry.

This is a statistical generalization of general covariance.

Einstein might not accept it as final. But he would respect its ambition.

---

## 23. Summary of Core Equations

### Fisher information metric

\[
g_{ij}(\theta)
=
\int dx\,
p(x|\theta)
\partial_i\ln p
\partial_j\ln p.
\]

### Statistical distance

\[
ds^2
=
g_{ij}d\theta^i d\theta^j.
\]

### Relative entropy

\[
D[p\|q]
=
\int dx\,
p\ln\frac{p}{q}.
\]

### Local relative entropy expansion

\[
D[p_{\theta+d\theta}\|p_\theta]
=
\frac{1}{2}
g_{ij}d\theta^i d\theta^j
+
\mathcal{O}(d\theta^3).
\]

### Maximum entropy distribution

\[
p(x)
=
\frac{1}{Z}
e^{-\lambda^a f_a(x)}.
\]

### Fokker–Planck equation from entropic updating

\[
\partial_t\rho
=
-
\partial_a(\rho b^a)
+
D\partial_a\partial^a\rho.
\]

### Quantum potential

\[
Q
=
-
\frac{\hbar^2}{2m}
\frac{\nabla^2\sqrt{\rho}}{\sqrt{\rho}}.
\]

### Schrödinger equation from entropic dynamics

\[
i\hbar\partial_t\psi
=
-
\frac{\hbar^2}{2m}\nabla^2\psi
+
V\psi.
\]

### Entropic force

\[
F\Delta x
=
T\Delta S.
\]

### Holographic entropy

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3}.
\]

### First law of entanglement

\[
\delta S
=
\delta\langle H_{\text{mod}}\rangle.
\]

### Linearized Einstein equation from entanglement

\[
\delta G_{\mu\nu}
+
\Lambda\delta g_{\mu\nu}
=
8\pi G_N
\delta T_{\mu\nu}.
\]

---

## 24. Conclusion

Relativity 17.0, Entropic / Information-Geometric Relativity, proposes that the laws of physics are not primitive dynamical commands but optimal rules of inference.

The metric of physics is not first a spacetime metric. It is a Fisher information metric. Motion is not first a trajectory through space. It is an update of probability. Gravity is not first a force. It is an entropic response of information geometry.

The central equation is not Newton’s law, nor even Einstein’s equation, but the Fisher metric,

\[
g_{ij}
=
\left\langle
\partial_i\ln p\,
\partial_j\ln p
\right\rangle.
\]

The central principle is:

\[
\boxed{
\text{Motion is updating; geometry is information; dynamics is inference.}
}
\]

Thermodynamic relativity showed that gravity is an equation of state. Holographic relativity showed that geometry is entanglement. Causal-informational relativity showed that spacetime is causal order. Entropic relativity unifies these by showing that all three may be expressions of statistical inference.

This is Relativity 17.0.

---

## Appendix A: Fisher Metric from Relative Entropy

Let

\[
p_\theta(x)
=
p(x|\theta).
\]

The relative entropy between nearby distributions is

\[
D[p_{\theta+d\theta}\|p_\theta]
=
\int dx\,
p_{\theta+d\theta}
\ln
\frac{p_{\theta+d\theta}}{p_\theta}.
\]

Expand:

\[
\ln p_{\theta+d\theta}
=
\ln p_\theta
+
\partial_i\ln p_\theta\,d\theta^i
+
\frac{1}{2}
\partial_i\partial_j\ln p_\theta\,
d\theta^i d\theta^j
+
\cdots.
\]

The first-order term vanishes by normalization. The second-order term gives

\[
D[p_{\theta+d\theta}\|p_\theta]
=
\frac{1}{2}
g_{ij}
d\theta^i d\theta^j,
\]

where

\[
g_{ij}
=
\int dx\,
p_\theta
\partial_i\ln p_\theta
\partial_j\ln p_\theta.
\]

Thus the Fisher metric is the local quadratic form of relative entropy.

---

## Appendix B: Maximum Entropy Derivation

Maximize

\[
S[p]
=
-
\int dx\,
p\ln p
\]

subject to

\[
\int dx\,p=1,
\]

\[
\int dx\,p f_a = F_a.
\]

Introduce multipliers \(\alpha,\lambda^a\) and vary

\[
\delta
\left[
S
-
\alpha
\left(
\int p-1
\right)
-
\lambda^a
\left(
\int p f_a-F_a
\right)
\right]
=
0.
\]

This gives

\[
-
\ln p
-
1
-
\alpha
-
\lambda^a f_a
=
0.
\]

Therefore,

\[
p(x)
=
\exp[-1-\alpha]
\exp[-\lambda^a f_a(x)].
\]

Normalization gives

\[
p(x)
=
\frac{1}{Z(\lambda)}
e^{-\lambda^a f_a(x)}.
\]

---

## Appendix C: Entropic Transition Probability

Maximize the entropy of \(P(x'|x)\),

\[
S[P]
=
-
\int dx'\,
P(x'|x)
\ln
\frac{P(x'|x)}{Q(x'|x)},
\]

subject to

\[
\int dx'P(x'|x)=1,
\]

\[
\langle \Delta x^a\rangle
=
b^a\Delta t,
\]

\[
\langle
\Delta x^a\Delta x_b
\rangle
=
2D\delta^a_b\Delta t.
\]

The result is Gaussian:

\[
P(x'|x)
=
\frac{1}{(4\pi D\Delta t)^{n/2}}
\exp
\left[
-
\frac{
\delta_{ab}
(\Delta x^a-b^a\Delta t)
(\Delta x^b-b^b\Delta t)
}{
4D\Delta t
}
\right].
\]

The continuum limit yields the Fokker–Planck equation.

---

## Appendix D: Entropic Force Derivation

Assume

\[
\Delta S
=
2\pi k_{\text{B}}
\frac{mc}{\hbar}
\Delta x,
\]

and

\[
k_{\text{B}}T
=
\frac{\hbar a}{2\pi c}.
\]

The entropic force relation is

\[
F\Delta x
=
T\Delta S.
\]

Substituting,

\[
F\Delta x
=
\frac{\hbar a}{2\pi k_{\text{B}}c}
\cdot
2\pi k_{\text{B}}
\frac{mc}{\hbar}
\Delta x.
\]

Canceling,

\[
F=ma.
\]

With holographic entropy and equipartition, one obtains

\[
a=\frac{GM}{r^2}.
\]

---

## Appendix E: Relative Entropy and Linearized Einstein Equations

For states \(\rho\) and \(\sigma\),

\[
S(\rho\|\sigma)
=
\Delta\langle H_\sigma\rangle
-
\Delta S.
\]

For infinitesimal perturbations,

\[
\Delta S
=
\Delta\langle H_\sigma\rangle.
\]

In holography,

\[
\Delta S_A
=
\frac{\Delta\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

For ball-shaped regions,

\[
H_A
=
2\pi
\int_A
\frac{R^2-|\mathbf{x}-\mathbf{x}_0|^2}{2R}
T_{00}.
\]

Requiring the first law for all balls gives

\[
\delta G_{\mu\nu}
+
\Lambda\delta g_{\mu\nu}
=
8\pi G_N
\delta T_{\mu\nu}.
\]

---

## Selected References

1. E. T. Jaynes, “Information Theory and Statistical Mechanics,” *Physical Review* **106**, 620 (1957).  
2. E. T. Jaynes, *Probability Theory: The Logic of Science* (Cambridge University Press, 2003).  
3. S.-I. Amari, *Information Geometry and Its Applications* (Springer, 2016).  
4. S.-I. Amari and H. Nagaoka, *Methods of Information Geometry* (American Mathematical Society, 2000).  
5. N. N. Chentsov, *Statistical Decision Rules and Optimal Inference* (American Mathematical Society, 1982).  
6. A. Caticha, “Entropic Dynamics,” *Entropy* **17**, 6110 (2015).  
7. A. Caticha, “Entropic Dynamics: Quantum Mechanics from Entropy and Information Geometry,” arXiv:1711.02538.  
8. A. Caticha, “Quantum Entropic Dynamics,” *AIP Conference Proceedings* **1635**, 3 (2014).  
9. E. Nelson, *Quantum Fluctuations* (Princeton University Press, 1985).  
10. B. R. Frieden, *Physics from Fisher Information* (Cambridge University Press, 1998).  
11. T. Jacobson, “Thermodynamics of Spacetime: The Einstein Equation of State,” *Physical Review Letters* **75**, 1260 (1995).  
12. E. Verlinde, “On the Origin of Gravity and the Laws of Newton,” *Journal of High Energy Physics* **1104**, 029 (2011).  
13. T. Padmanabhan, “Thermodynamical Aspects of Gravity: New Insights,” *Reports on Progress in Physics* **73**, 046901 (2010).  
14. M. Van Raamsdonk, “Building Up Spacetime with Quantum Entanglement,” *General Relativity and Gravitation* **42**, 2323 (2010).  
15. T. Faulkner, A. Lewkowycz, and J. Maldacena, “Quantum Corrections to Holographic Entanglement Entropy,” *Journal of High Energy Physics* **1311**, 074 (2013).  
16. N. Lashkari, M. B. McDermott, and M. Van Raamsdonk, “Gravitational Dynamics from Entanglement Thermodynamics,” *Journal of High Energy Physics* **1404**, 195 (2014).  
17. D. L. Jafferis, A. Lewkowycz, J. Maldacena, and S. J. Suh, “Relative Entropy Equals Bulk Relative Entropy,” *Journal of High Energy Physics* **1606**, 004 (2016).  
18. S. Ryu and T. Takayanagi, “Holographic Derivation of Entanglement Entropy from AdS/CFT,” *Physical Review Letters* **96**, 181602 (2006).  
19. C. E. Shannon, “A Mathematical Theory of Communication,” *Bell System Technical Journal* **27**, 379 (1948).  
20. T. M. Cover and J. A. Thomas, *Elements of Information Theory* (Wiley, 2006).  
21. M. R. Dowson and A. J. Landau, “The Fréchet Distance between Multivariate Normal Distributions,” *Journal of Multivariate Analysis* **12**, 450 (1982).  
22. S. L. Braunstein and C. M. Caves, “Statistical Distance and the Geometry of Quantum States,” *Physical Review Letters* **72**, 3439 (1994).  
23. M. G. A. Paris, “Quantum Estimation for Quantum Technology,” *International Journal of Quantum Information* **7**, 125 (2009).  
24. R. Balian, *From Microphysics to Macrophysics* (Springer, 2007).  
25. A. Caticha, “Entropic Inference and the Foundations of Physics,” lecture notes, University at Albany (2012).

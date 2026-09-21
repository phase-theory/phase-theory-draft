# Transformational Physics: A Relational Theory of Admissible Transformations and the Emergence of Dynamical Law

**Preprint**

---

## Abstract

This paper develops a physical theory whose primitive notion is not number, point, set, or field value, but an admissible transformation

\[
A \xrightarrow{f} B .
\]

Starting from a relational–transformational foundation, we construct a physical ontology in which states are stable transformational loci, histories are composable transformation paths, geometry is induced by transformational cost, quantum amplitudes are unitary representations of transformational composition, gauge fields are connections required by local transformation equivalence, gravity is curvature of relational parallel transport, and thermodynamic entropy measures loss of distinguishability under non-invertible transformations.

The central results are:

1. **Classical dynamics** follows from stationarity of an additive transformational action.
2. **Metric geometry** follows from reversible, locally quadratic transformational cost.
3. **Quantum theory** follows when indistinguishable transformation paths carry coherent phase weights.
4. **Gauge structure** follows from demanding covariance under local transformations.
5. **General relativity** follows when transformations between local frames are made dynamical.
6. **Irreversibility and entropy** arise from quotienting transformation histories by observational equivalence.

The framework also yields new physical conjectures: transformational inertia, minimal transformation length, holonomy noise, entropy–complexity bounds, and anomaly-like conservation defects arising from higher transformational obstructions.

---

## 1. Introduction

The conventional foundations of physics usually begin with entities:

\[
\text{particles},\quad
\text{fields},\quad
\text{spacetime points},\quad
\text{states},\quad
\text{observables}.
\]

Relations and transformations are then defined between these entities. In the present framework, the conceptual order is reversed. The primitive mathematical event is

\[
A \xrightarrow{f} B .
\]

Here \(A\) and \(B\) are not assumed to be pre-given objects with numerical coordinates. They are transformational loci whose physical identity is reconstructed from the transformations in which they participate.

The physical thesis is:

\[
\boxed{
\text{Physical law is a constraint on admissible transformation.}
}
\]

Thus, rather than asking first “What exists?”, we ask:

\[
\text{What transformations are admissible, composable, invariant, and observable?}
\]

From this question we derive dynamics, geometry, quantum propagation, gauge structure, gravitation, and thermodynamic irreversibility.

---

## 2. Transformational Ontology

### 2.1 Primitive transformational structure

Let a transformational structure be

\[
\mathfrak T
=
(\mathsf L,\mathsf M,s,t,\circ,\mathbf 1,\sim),
\]

where:

- \(\mathsf L\) is a collection of transformational loci;
- \(\mathsf M\) is a collection of transformations;
- \(s:\mathsf M\to\mathsf L\) assigns a source;
- \(t:\mathsf M\to\mathsf L\) assigns a target;
- \(\circ\) is partially defined composition;
- \(\mathbf 1\) assigns identity transformations;
- \(\sim\) denotes observational or structural equivalence.

For each transformation,

\[
f:A\to B,
\]

we write

\[
s(f)=A,
\qquad
t(f)=B.
\]

If

\[
A\xrightarrow{f}B,
\qquad
B\xrightarrow{g}C,
\]

then there exists a composite

\[
A\xrightarrow{g\circ f}C.
\]

Composition is associative:

\[
h\circ(g\circ f)=(h\circ g)\circ f,
\]

and identities satisfy

\[
f\circ \mathbf 1_A=f,
\qquad
\mathbf 1_B\circ f=f.
\]

A physical theory is obtained when additional structure is imposed on \(\mathfrak T\), especially an action functional, equivalence relation, and observational functor.

---

### 2.2 Transformation paths

A finite transformation path is a composable sequence

\[
\gamma=
A_0
\xrightarrow{f_1}
A_1
\xrightarrow{f_2}
A_2
\to\cdots\to
A_{n-1}
\xrightarrow{f_n}
A_n .
\]

Its composite is

\[
\operatorname{Comp}(\gamma)
=
f_n\circ\cdots\circ f_1 .
\]

Physical histories are not merely endpoints but equivalence classes of paths:

\[
[\gamma].
\]

Two paths may be physically equivalent if they induce indistinguishable transformations under all admissible observations.

---

### 2.3 Transformational action

Introduce an additive cost or action functional

\[
\mathcal S:\operatorname{Path}(\mathfrak T)\to\mathbb R
\]

such that

\[
\mathcal S(\gamma_2\circ\gamma_1)
=
\mathcal S(\gamma_2)+\mathcal S(\gamma_1)
\]

whenever the paths are composable.

For elementary transformations one may write

\[
\mathcal S(\gamma)
=
\sum_{i=1}^n \kappa(f_i),
\]

where \(\kappa(f_i)\) is the transformational cost of the step \(f_i\).

In the continuum limit, paths become curves \(x^\mu(\lambda)\), and the additive action becomes an integral:

\[
\mathcal S[x]
=
\int_{\lambda_i}^{\lambda_f}
L\bigl(x,\dot x,\lambda\bigr)\,d\lambda .
\]

Thus the familiar action principle is recovered as a continuum representation of transformational composition.

---

## 3. Physical Postulates

We impose the following physical postulates.

### Postulate P1: Relational states

A physical state is not a primitive object but an equivalence class of transformational loci:

\[
[A]=\{B:B\sim A\}.
\]

Equivalence is determined by observational indistinguishability under admissible transformations.

---

### Postulate P2: Histories are transformation paths

A physical history from state \([A]\) to state \([B]\) is an equivalence class of transformation paths

\[
[A]\xrightarrow{\gamma}[B].
\]

---

### Postulate P3: Classical extremization

Classical histories are stationary transformation paths:

\[
\delta\mathcal S[\gamma]=0.
\]

---

### Postulate P4: Quantum coherence

If multiple transformation paths are observationally indistinguishable, their contributions are summed coherently:

\[
\mathcal K(B,A)
=
\int_{\gamma:A\to B}
\mathcal D\gamma\,
e^{\frac{i}{\hbar}\mathcal S[\gamma]}.
\]

If paths are distinguishable, probabilities are summed instead.

---

### Postulate P5: Gauge equivalence

Transformations related by local representation changes describe the same physical history.

If

\[
\gamma_1\sim_{\text{gauge}}\gamma_2,
\]

then

\[
\mathcal K[\gamma_1]=\mathcal K[\gamma_2].
\]

---

### Postulate P6: Information loss under non-invertible transformations

If a transformation is non-invertible, it may identify previously distinguishable states. Entropy measures the resulting loss of distinguishability.

---

## 4. Emergence of Classical Dynamics

Assume that the transformational locus admits a differentiable coordinate representation

\[
x^\mu(\lambda),
\qquad
\mu=0,\dots,d-1.
\]

An infinitesimal transformation is then

\[
x^\mu\mapsto x^\mu+dx^\mu.
\]

If the transformational action is local and additive, it takes the form

\[
\mathcal S[x]
=
\int_{\lambda_i}^{\lambda_f}
L(x,\dot x,\lambda)\,d\lambda .
\]

Consider a variation

\[
x^\mu(\lambda)\mapsto x^\mu(\lambda)+\delta x^\mu(\lambda),
\]

with fixed endpoints:

\[
\delta x^\mu(\lambda_i)=\delta x^\mu(\lambda_f)=0.
\]

Then

\[
\delta\mathcal S
=
\int_{\lambda_i}^{\lambda_f}
\left(
\frac{\partial L}{\partial x^\mu}\delta x^\mu
+
\frac{\partial L}{\partial \dot x^\mu}\delta\dot x^\mu
\right)d\lambda .
\]

Integrating the second term by parts gives

\[
\delta\mathcal S
=
\left[
\frac{\partial L}{\partial \dot x^\mu}\delta x^\mu
\right]_{\lambda_i}^{\lambda_f}
+
\int_{\lambda_i}^{\lambda_f}
\left(
\frac{\partial L}{\partial x^\mu}
-
\frac{d}{d\lambda}
\frac{\partial L}{\partial \dot x^\mu}
\right)
\delta x^\mu
\,d\lambda .
\]

The boundary term vanishes. Since the variation is arbitrary, stationarity implies the Euler–Lagrange equations:

\[
\boxed{
\frac{\partial L}{\partial x^\mu}
-
\frac{d}{d\lambda}
\frac{\partial L}{\partial \dot x^\mu}
=0.
}
\]

Thus classical dynamics is the stationarity condition for transformational paths.

---

## 5. Metric Geometry from Transformational Cost

Suppose the transformation system is reversible and locally admits a quadratic cost:

\[
d\sigma^2
=
g_{\mu\nu}(x)\,dx^\mu dx^\nu .
\]

Then the length of a transformation path is

\[
\ell[x]
=
\int
\sqrt{
g_{\mu\nu}(x)\dot x^\mu\dot x^\nu
}
\,d\lambda .
\]

Equivalently, one may use the energy action

\[
\mathcal S_E[x]
=
\frac12
\int
g_{\mu\nu}(x)\dot x^\mu\dot x^\nu
\,d\lambda .
\]

The Euler–Lagrange equations for \(\mathcal S_E\) give

\[
\frac{d}{d\lambda}
\left(
g_{\rho\nu}\dot x^\nu
\right)
-
\frac12
\partial_\rho g_{\mu\nu}\dot x^\mu\dot x^\nu
=0.
\]

Expanding,

\[
g_{\rho\nu}\ddot x^\nu
+
\partial_\mu g_{\rho\nu}\dot x^\mu\dot x^\nu
-
\frac12
\partial_\rho g_{\mu\nu}\dot x^\mu\dot x^\nu
=0.
\]

Multiplying by \(g^{\sigma\rho}\) and symmetrizing gives

\[
\boxed{
\ddot x^\sigma
+
\Gamma^\sigma_{\mu\nu}
\dot x^\mu\dot x^\nu
=0,
}
\]

where

\[
\Gamma^\sigma_{\mu\nu}
=
\frac12
g^{\sigma\rho}
\left(
\partial_\mu g_{\nu\rho}
+
\partial_\nu g_{\mu\rho}
-
\partial_\rho g_{\mu\nu}
\right).
\]

Therefore:

\[
\boxed{
\text{Metric geometry emerges from reversible transformational cost.}
}
\]

The geodesic equation is the classical law of minimal transformational resistance.

---

## 6. Noether Theorem as Transformational Invariance

Let the action be invariant under an infinitesimal transformation

\[
\delta x^\mu
=
\epsilon X^\mu(x),
\]

possibly up to a boundary term:

\[
\delta L
=
\epsilon\frac{dF}{d\lambda}.
\]

Define canonical momenta

\[
p_\mu
=
\frac{\partial L}{\partial\dot x^\mu}.
\]

Then

\[
\delta L
=
\frac{\partial L}{\partial x^\mu}\epsilon X^\mu
+
p_\mu \epsilon\dot X^\mu .
\]

Using the equations of motion,

\[
\frac{\partial L}{\partial x^\mu}
=
\dot p_\mu,
\]

we obtain

\[
\epsilon\frac{dF}{d\lambda}
=
\epsilon
\left(
\dot p_\mu X^\mu
+
p_\mu\dot X^\mu
\right)
=
\epsilon
\frac{d}{d\lambda}
\left(
p_\mu X^\mu
\right).
\]

Hence

\[
\frac{d}{d\lambda}
\left(
p_\mu X^\mu-F
\right)
=0.
\]

Therefore the conserved charge is

\[
\boxed{
Q
=
p_\mu X^\mu-F.
}
\]

This is the transformational form of Noether’s theorem:

\[
\boxed{
\text{Continuous transformation symmetry}
\quad\Longrightarrow\quad
\text{conserved quantity.}
}
\]

Energy, momentum, and angular momentum are invariants of admissible transformational symmetries.

---

## 7. Quantum Theory as Coherent Transformational Composition

Let \(\Pi(A,B)\) denote the space of transformation paths from \(A\) to \(B\). Assign to each path a phase weight

\[
W[\gamma]
=
\exp\left(
\frac{i}{\hbar}\mathcal S[\gamma]
\right).
\]

The transition amplitude is

\[
\boxed{
\mathcal K(B,A)
=
\int_{\Pi(A,B)/\sim}
\mathcal D\gamma\,
\exp\left(
\frac{i}{\hbar}\mathcal S[\gamma]
\right).
}
\]

The quotient by \(\sim\) removes gauge-equivalent or observationally indistinguishable paths.

### 7.1 Composition law

Let \(A,B,C\) be transformational loci. Because every path \(A\to C\) may be decomposed as

\[
A\to B\to C,
\]

and because the action is additive,

\[
\mathcal S[\gamma_{AC}]
=
\mathcal S[\gamma_{AB}]
+
\mathcal S[\gamma_{BC}],
\]

the amplitude satisfies

\[
\boxed{
\mathcal K(C,A)
=
\int_{\mathsf L_B}
d\mu(B)\,
\mathcal K(C,B)\mathcal K(B,A).
}
\]

This is the relational origin of quantum propagation.

---

### 7.2 Classical limit

For large action relative to \(\hbar\), the phase oscillates rapidly. By stationary phase, dominant contributions come from paths satisfying

\[
\delta\mathcal S=0.
\]

Thus classical trajectories are the leading asymptotics of quantum transformational composition:

\[
\boxed{
\hbar\to 0
\quad\Longrightarrow\quad
\text{classical transformational extremals.}
}
\]

---

### 7.3 Observables as transformation generators

Let \(U(\epsilon)\) be a one-parameter family of reversible transformations. Write

\[
U(\epsilon)
=
\exp\left(
-\frac{i}{\hbar}\epsilon G
\right),
\]

where \(G\) is the generator.

If transformations form a Lie group with structure constants \(f_{ab}{}^c\), then

\[
U_a(\epsilon)U_b(\eta)U_a(-\epsilon)U_b(-\eta)
=
U_c(f_{ab}{}^c\epsilon\eta+\cdots),
\]

which implies

\[
\boxed{
[G_a,G_b]
=
i\hbar f_{ab}{}^c G_c.
}
\]

Observables are therefore generators of admissible transformations.

For canonical position and translation transformations, one obtains

\[
\boxed{
[Q^i,P_j]=i\hbar\delta^i{}_j.
}
\]

The Robertson uncertainty relation follows:

\[
\boxed{
\Delta A\,\Delta B
\ge
\frac12
\left|
\langle [A,B]\rangle
\right|.
}
\]

Thus quantum noncommutativity is noncommutativity of transformations.

---

### 7.4 Schrödinger evolution

If time is an ordered transformation parameter, the elementary time transformation is generated by an operator \(H\):

\[
U(t)
=
\exp\left(
-\frac{i}{\hbar}Ht
\right).
\]

For a state vector \(\psi(t)\),

\[
\psi(t)
=
U(t)\psi(0).
\]

Differentiating,

\[
\frac{d\psi}{dt}
=
-\frac{i}{\hbar}H\psi,
\]

so

\[
\boxed{
i\hbar\frac{\partial\psi}{\partial t}
=
H\psi.
}
\]

The Schrödinger equation is therefore the infinitesimal law of temporal transformation.

---

## 8. Gauge Fields from Local Transformation Equivalence

Let \(\psi(x)\) be a field valued in a vector space \(V\). Suppose there is a local transformation group \(G\) acting by

\[
\psi(x)\mapsto \psi'(x)=g(x)\psi(x),
\qquad
g(x)\in G.
\]

The ordinary derivative transforms as

\[
\partial_\mu\psi'
=
(\partial_\mu g)\psi
+
g\partial_\mu\psi.
\]

The extra term \((\partial_\mu g)\psi\) prevents covariance. To compare transformations at neighboring loci, introduce a connection \(A_\mu\) and define

\[
D_\mu
=
\partial_\mu+A_\mu.
\]

Demand

\[
D'_\mu\psi'
=
gD_\mu\psi.
\]

Then

\[
(\partial_\mu+A'_\mu)(g\psi)
=
g(\partial_\mu+A_\mu)\psi.
\]

Expanding,

\[
(\partial_\mu g)\psi
+
g\partial_\mu\psi
+
A'_\mu g\psi
=
g\partial_\mu\psi
+
gA_\mu\psi.
\]

Therefore

\[
A'_\mu g
=
gA_\mu-\partial_\mu g,
\]

and hence

\[
\boxed{
A'_\mu
=
gA_\mu g^{-1}
-
(\partial_\mu g)g^{-1}.
}
\]

The connection \(A_\mu\) is the relational structure required to compare local transformations.

Define curvature by

\[
F_{\mu\nu}
=
[D_\mu,D_\nu].
\]

A direct calculation gives

\[
\boxed{
F_{\mu\nu}
=
\partial_\mu A_\nu
-
\partial_\nu A_\mu
+
[A_\mu,A_\nu].
}
\]

Under local transformations,

\[
F_{\mu\nu}
\mapsto
F'_{\mu\nu}
=
gF_{\mu\nu}g^{-1}.
\]

Thus curvature is the invariant failure of local transformations to commute.

The simplest local, gauge-invariant action is

\[
\boxed{
\mathcal S_{\text{YM}}
=
-\frac14
\int
F^a_{\mu\nu}F^{a\mu\nu}
\sqrt{-g}\,d^4x.
}
\]

Varying \(A_\mu\), using

\[
\delta F_{\mu\nu}
=
D_\mu\delta A_\nu
-
D_\nu\delta A_\mu,
\]

and integrating by parts gives

\[
\delta\mathcal S_{\text{YM}}
=
\int
(D_\mu F^{\mu\nu})^a
\delta A_\nu^a
\sqrt{-g}\,d^4x.
\]

Hence the Yang–Mills equations follow:

\[
\boxed{
D_\mu F^{\mu\nu}
=
J^\nu.
}
\]

In vacuum,

\[
D_\mu F^{\mu\nu}=0.
\]

Thus gauge bosons are dynamical relational connections.

---

## 9. Gravity as Curvature of Relational Transport

Spacetime geometry arises when transformations between neighboring loci include changes of local frame. Let \(x^\mu\mapsto x'^\mu(x)\) be a coordinate transformation. A vector transforms as

\[
V'^\mu
=
\frac{\partial x'^\mu}{\partial x^\nu}V^\nu.
\]

To compare vectors at neighboring loci, introduce a covariant derivative

\[
\nabla_\mu V^\rho
=
\partial_\mu V^\rho
+
\Gamma^\rho_{\mu\sigma}V^\sigma.
\]

The curvature tensor is defined by the commutator

\[
[\nabla_\mu,\nabla_\nu]V^\rho
=
R^\rho{}_{\sigma\mu\nu}V^\sigma,
\]

assuming vanishing torsion. Explicitly,

\[
\boxed{
R^\rho{}_{\sigma\mu\nu}
=
\partial_\mu\Gamma^\rho_{\nu\sigma}
-
\partial_\nu\Gamma^\rho_{\mu\sigma}
+
\Gamma^\rho_{\mu\lambda}\Gamma^\lambda_{\nu\sigma}
-
\Gamma^\rho_{\nu\lambda}\Gamma^\lambda_{\mu\sigma}.
}
\]

This is the mathematical expression of transformational noncommutativity.

Parallel transport around an infinitesimal loop with area element \(\delta\Sigma^{\mu\nu}\) produces

\[
\delta V^\rho
=
\frac12
R^\rho{}_{\sigma\mu\nu}
V^\sigma
\delta\Sigma^{\mu\nu}.
\]

Thus curvature is holonomy: the memory of transformational transport.

---

### 9.1 Einstein–Hilbert action

The simplest scalar invariant built from curvature is the Ricci scalar

\[
R
=
g^{\mu\nu}R_{\mu\nu}.
\]

The gravitational action is

\[
\boxed{
\mathcal S_G
=
\frac{1}{16\pi G}
\int
(R-2\Lambda)
\sqrt{-g}\,d^4x.
}
\]

Adding matter action \(\mathcal S_m\), define the stress-energy tensor by

\[
T_{\mu\nu}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta\mathcal S_m}{\delta g^{\mu\nu}}.
\]

The metric variation satisfies

\[
\delta
\left(
\sqrt{-g}R
\right)
=
\sqrt{-g}
\left(
G_{\mu\nu}\delta g^{\mu\nu}
+
\nabla_\alpha v^\alpha
\right),
\]

where

\[
G_{\mu\nu}
=
R_{\mu\nu}
-
\frac12 Rg_{\mu\nu}.
\]

Stationarity of

\[
\mathcal S
=
\mathcal S_G+\mathcal S_m
\]

therefore gives

\[
\boxed{
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
8\pi G T_{\mu\nu}.
}
\]

Thus Einstein’s equation is the balance law of relational curvature and transformational energy.

---

### 9.2 Newtonian limit

Let the metric be weakly perturbed around flat spacetime:

\[
g_{00}
=
-(1+2\Phi),
\qquad
|\Phi|\ll1,
\]

and assume slow motion. Then

\[
G_{00}
\approx
2\nabla^2\Phi.
\]

For nonrelativistic matter,

\[
T_{00}\approx\rho.
\]

Einstein’s equation gives

\[
2\nabla^2\Phi
=
8\pi G\rho,
\]

or

\[
\boxed{
\nabla^2\Phi
=
4\pi G\rho.
}
\]

This recovers Newtonian gravity as a coarse transformational limit.

---

## 10. Matter Fields as Representations of Transformation Groups

Matter fields are representations of admissible transformation groups.

### 10.1 Scalar fields

A scalar field \(\phi\) satisfies

\[
\phi'(x')=\phi(x).
\]

The simplest invariant action is

\[
\boxed{
\mathcal S_\phi
=
\int
\sqrt{-g}
\left(
-\frac12 g^{\mu\nu}\nabla_\mu\phi\nabla_\nu\phi
-
V(\phi)
\right)
d^4x.
}
\]

Variation gives

\[
\boxed{
\square_g\phi
-
V'(\phi)
=0,
}
\]

where

\[
\square_g\phi
=
\frac{1}{\sqrt{-g}}
\partial_\mu
\left(
\sqrt{-g}g^{\mu\nu}\partial_\nu\phi
\right).
\]

---

### 10.2 Spinors and local Lorentz transformations

If local transformations include the Lorentz group \(SO(1,3)\), its double cover \(\mathrm{Spin}(1,3)\) acts on spinor fields. Introduce a tetrad \(e^a{}_\mu\) satisfying

\[
g_{\mu\nu}
=
e^a{}_\mu e^b{}_\nu\eta_{ab}.
\]

The spin connection \(\omega_\mu{}^{ab}\) defines

\[
D_\mu\psi
=
\left(
\partial_\mu
+
\frac14
\omega_\mu{}^{ab}\gamma_{ab}
\right)\psi,
\]

where

\[
\gamma_{ab}
=
\frac12[\gamma_a,\gamma_b].
\]

The curved-space Dirac action is

\[
\boxed{
\mathcal S_\psi
=
\int
e\,
\bar\psi
\left(
i\gamma^\mu D_\mu
-
m
\right)
\psi
\,d^4x,
}
\]

with

\[
e=\det(e^a{}_\mu),
\qquad
\gamma^\mu=e_a{}^\mu\gamma^a.
\]

Variation yields

\[
\boxed{
\left(
i\gamma^\mu D_\mu
-
m
\right)\psi
=0.
}
\]

Thus fermions arise as projective representations of local transformation structure.

---

## 11. Causality from Directed Transformation

If transformations are not all reversible, the system possesses directed structure:

\[
A\prec B
\]

meaning there exists an admissible transformation from \(A\) to \(B\), but not necessarily from \(B\) to \(A\).

In a continuum, directed transformations define cones in tangent space. Let \(C_x\) be the cone of allowed infinitesimal transformations at locus \(x\). If there is a finite maximal rate of transformation, the cone is nontrivial and may be represented by a Lorentzian metric:

\[
ds^2
=
g_{\mu\nu}dx^\mu dx^\nu.
\]

Causal transformations satisfy

\[
ds^2\le0
\]

for signature \((-+++)\\).

The free relativistic particle action is then

\[
\boxed{
\mathcal S
=
-m\int
\sqrt{
-g_{\mu\nu}\dot x^\mu\dot x^\nu
}
\,d\lambda.
}
\]

Stationarity again yields geodesic motion. Thus relativistic causal structure is the geometry of directed admissible transformations.

---

## 12. Information, Entropy, and Irreversibility

Let \(X\) be a space of microscopic states. A stochastic transformation is a kernel

\[
K(x'|x)
\]

satisfying

\[
\sum_{x'}K(x'|x)=1.
\]

It maps probability distributions by

\[
(Kp)(x')
=
\sum_x K(x'|x)p(x).
\]

Distinguishability between distributions \(p\) and \(q\) is measured by relative entropy:

\[
D_{\mathrm{KL}}(p\|q)
=
\sum_x p(x)\log\frac{p(x)}{q(x)}.
\]

A fundamental theorem is the data-processing inequality:

\[
\boxed{
D_{\mathrm{KL}}(Kp\|Kq)
\le
D_{\mathrm{KL}}(p\|q).
}
\]

Thus non-invertible transformations cannot increase distinguishability.

Define relational entropy by

\[
S[p]
=
-k_B\sum_x p(x)\log p(x).
\]

If an observational map

\[
\pi:X\to X/{\sim}
\]

coarse-grains microscopic states, then the observed distribution is

\[
\bar p=\pi_*p.
\]

The hidden correlations produce an entropy increase:

\[
S[\bar p]\ge S[p]
\]

under natural mixing conditions.

In quantum theory, if the total state evolves unitarily,

\[
\rho_{\text{tot}}(t)
=
U(t)\rho_{\text{tot}}(0)U^\dagger(t),
\]

then the total von Neumann entropy is conserved:

\[
S(\rho_{\text{tot}})
=
-\operatorname{Tr}\rho_{\text{tot}}\log\rho_{\text{tot}}.
\]

But for an observed subsystem \(A\),

\[
\rho_A
=
\operatorname{Tr}_{\bar A}\rho_{\text{tot}},
\]

and generally

\[
S(\rho_A)
\]

can increase. This is not a fundamental loss of microscopic reversibility but a loss of access to transformational correlations.

Thus:

\[
\boxed{
\text{Entropy is relational information loss under non-invertible observation.}
}
\]

---

## 13. Higher Transformations and Anomalies

A transformation between transformations is a 2-transformation:

\[
f\xRightarrow{\alpha}g.
\]

In physics, such higher transformations appear as homotopies between histories, gauge transformations between gauge transformations, and anomalies as obstructions to lifting classical symmetries to quantum amplitudes.

Suppose a classical symmetry transformation preserves the action:

\[
\delta\mathcal S=0.
\]

At the quantum level, the path-integral measure may fail to be invariant:

\[
\mathcal D\phi
\mapsto
J[\alpha]\mathcal D\phi,
\]

where

\[
J[\alpha]
\neq
1.
\]

Then the Ward identity is modified:

\[
\boxed{
\nabla_\mu J^\mu
=
\mathcal A,
}
\]

where \(\mathcal A\) is the anomaly.

In transformational language, an anomaly is a higher obstruction: the classical symmetry exists at the level of paths, but cannot be coherently extended to the level of quantum amplitudes.

For chiral gauge theories, one obtains the familiar form

\[
\partial_\mu J^\mu_5
=
\frac{g^2}{16\pi^2}
F^a_{\mu\nu}\widetilde F^{a\mu\nu}.
\]

Thus anomalies are transformational defects in the coherence of quantum histories.

---

## 14. New Physical Principles

The preceding reconstruction suggests several new physical principles.

---

### 14.1 Transformational inertia

In ordinary mechanics, mass is an intrinsic parameter. In the transformational framework, mass is a measure of resistance to change of transformational state.

Let the cost of a small velocity transformation \(v^i\) be expanded as

\[
\kappa(v)
=
\kappa_0
+
\frac12 m_{ij}v^iv^j
+
O(v^4).
\]

Then

\[
\boxed{
m_{ij}
=
\left.
\frac{\partial^2\kappa}{\partial v^i\partial v^j}
\right|_{v=0}.
}
\]

Mass is the Hessian of transformational cost.

If the relational background changes, the effective inertia may change. In a sufficiently homogeneous relational environment, \(m_{ij}\) becomes universal, yielding the equivalence principle.

---

### 14.2 Minimal transformation length

Suppose there exists an elementary transformation of nonzero minimal cost \(\ell_*\). Then path length is not infinitely divisible. The continuum metric becomes an approximation:

\[
d(A,B)
=
\inf_{\gamma:A\to B}
\sum_{f\in\gamma}\kappa(f),
\qquad
\kappa(f)\ge \ell_*.
\]

At low energies, this may induce modified dispersion relations:

\[
\boxed{
E^2
=
p^2c^2
+
m^2c^4
+
\alpha \ell_* p^3c^3
+
\beta\ell_*^2p^4c^4
+
\cdots.
}
\]

The coefficients \(\alpha,\beta\) depend on the underlying transformational structure.

This gives a possible phenomenological window into pre-geometric transformation discreteness.

---

### 14.3 Holonomy noise

If the gravitational connection is not a smooth classical field but an ensemble of transformational relations, then holonomies fluctuate:

\[
\operatorname{Hol}(\gamma)
=
\mathcal P
\exp
\left(
\oint_\gamma \Gamma
\right).
\]

A simple stochastic model gives

\[
\left\langle
\operatorname{Hol}(\gamma)
\right\rangle
=
\exp\left(
-\lambda A(\gamma)
\right),
\]

where \(A(\gamma)\) is the area enclosed by the loop and \(\lambda\) is a Planck-scale suppression factor.

Thus interferometric phase noise may scale with enclosed area rather than path length.

---

### 14.4 Entropy–complexity bound

Let \(\Omega\) be a region and let \(\partial\Omega\) be its boundary. Suppose the number of independent admissible transformations through the boundary is \(N(\partial\Omega)\). Then the internal relational entropy is bounded by

\[
\boxed{
S(\Omega)
\le
k_B\log N(\partial\Omega).
}
\]

If the minimal transformational cost per boundary degree of freedom is gravitational, one obtains

\[
\boxed{
S(\Omega)
\le
\frac{k_B A(\partial\Omega)}{4\ell_P^2}.
}
\]

This gives a transformational derivation of holographic entropy scaling.

---

### 14.5 Relational conservation defects

If a symmetry holds only up to a higher transformation, the corresponding conserved current acquires a source:

\[
\boxed{
\nabla_\mu J^\mu
=
\mathcal D,
}
\]

where \(\mathcal D\) is a transformational defect.

Known anomalies are special cases. More general defects could produce tiny violations of global conservation laws in regimes where the transformational structure is not effectively smooth.

---

## 15. Unified Transformational Field Equation

The known dynamical equations can be written as stationarity conditions of a total transformational action:

\[
\boxed{
\mathcal S_{\text{total}}
=
\mathcal S_{\text{geom}}
+
\mathcal S_{\text{gauge}}
+
\mathcal S_{\text{matter}}
+
\mathcal S_{\text{info}}.
}
\]

Here

\[
\mathcal S_{\text{geom}}
=
\frac{1}{16\pi G}
\int
(R-2\Lambda)\sqrt{-g}\,d^4x,
\]

\[
\mathcal S_{\text{gauge}}
=
-\frac14
\int
F^a_{\mu\nu}F^{a\mu\nu}
\sqrt{-g}\,d^4x,
\]

\[
\mathcal S_{\text{matter}}
=
\int
\sqrt{-g}
\mathcal L_{\text{matter}}
\,d^4x,
\]

and \(\mathcal S_{\text{info}}\) encodes coarse-graining, entropy currents, and higher transformational obstructions.

Variation with respect to the metric gives

\[
\boxed{
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
8\pi G
\left(
T^{\text{matter}}_{\mu\nu}
+
T^{\text{gauge}}_{\mu\nu}
+
T^{\text{info}}_{\mu\nu}
\right).
}
\]

The novel term \(T^{\text{info}}_{\mu\nu}\) represents stress contributed by relational information structure. In ordinary regimes it is negligible, but near singularities, horizons, or Planckian curvature it may become significant.

---

## 16. Conceptual Consequences

The theory reinterprets the central concepts of physics as follows.

| Concept | Transformational interpretation |
|---|---|
| State | Stable equivalence class of transformational loci |
| History | Composable transformation path |
| Action | Additive transformational cost |
| Classical law | Stationary transformation path |
| Quantum amplitude | Coherent sum over indistinguishable paths |
| Observable | Generator of reversible transformations |
| Gauge field | Connection comparing local transformations |
| Curvature | Noncommutativity of transformational transport |
| Gravity | Dynamics of relational frame transport |
| Entropy | Loss of distinguishability under quotienting |
| Causality | Directed admissibility of transformations |
| Number | Invariant extracted from transformational structure |

Thus physics is not built upon numerical quantities. Numbers appear as compressed invariants of a deeper transformational order.

---

## 17. Conclusion

We have derived a physical theory from the primitive transformation

\[
A\xrightarrow{f}B.
\]

The resulting architecture is:

\[
\boxed{
\text{transformations}
\to
\text{paths}
\to
\text{composition}
\to
\text{action}
\to
\text{invariants}
\to
\text{geometry}
\to
\text{dynamics}
\to
\text{numbers}.
}
\]

Classical mechanics arises as extremal transformational composition. Geometry arises as the metric induced by transformational cost. Quantum theory arises from coherent summation over indistinguishable transformation paths. Gauge fields arise as connections required by local transformation equivalence. Gravity arises as curvature of relational transport. Thermodynamic entropy arises from loss of distinguishability under non-invertible transformations.

The deepest physical claim is therefore:

\[
\boxed{
\text{Physical reality is not primarily a collection of things,}
\quad
\text{but a structured field of admissible transformations.}
}
\]

Numerical physics remains valid, but as a representation layer:

\[
\boxed{
\text{Number is the compressed invariant of transformation.}
}
\]

The resulting program suggests new research directions: transformational derivations of quantum gravity, coarse-grained holography, minimal transformation scales, anomaly-like conservation defects, and experimental searches for holonomy noise or modified dispersion relations.

The primitive event of physics is not a quantity to be measured.

It is a transformation to be composed.

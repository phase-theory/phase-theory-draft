# Frame Theory: Local Reference Frames and the Emergence of General Relativity from Relativity Mechanics

## Abstract

Frame Theory is a theorem-level specialization of Relativity Mechanics obtained by choosing the description space to consist of local reference frames and the admissibility group to be the local spin group. Its primitive question is:

\[
\boxed{
\text{What if the admissible descriptions are local reference frames?}
}
\]

The answer is to take

\[
\Omega=\{\text{frames}\},
\qquad
G=\mathrm{Spin}(1,3),
\]

or, more precisely, the local gauge group of maps into \(\mathrm{Spin}(1,3)\). A frame description is a local Lorentz coframe \(e^I=e^I_\mu dx^\mu\). The admissibility action is local Lorentz rotation of the frame:

\[
e^I\mapsto \Lambda^I{}_J(x)e^J,
\qquad
\Lambda(x)\in \mathrm{Spin}(1,3).
\]

The central invariant of this action is the Lorentzian metric

\[
\boxed{
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
}
\]

Thus the metric is not primitive. It is the invariant content of an orbit of local frames. Frame Theory therefore reverses the usual presentation of general relativity: geometry is not first given as a metric; geometry is the invariant of local frame descriptions.

This paper develops Frame Theory from the relativity schema

\[
\mathcal R_{\rm FT}
=
(\Omega_{\rm FT},G_{\rm FT},\triangleright,I_{\rm FT}).
\]

We define the frame description space, the local spin admissibility group, the invariant projection to metric geometry, the spin connection, torsion, curvature, and the invariant Palatini action. We show that imposing vanishing torsion recovers the Levi-Civita connection and the Einstein–Hilbert action, thereby yielding general relativity. Allowing torsion sourced by spin yields Einstein–Cartan theory. Spinor fields require precisely the double-cover group \(\mathrm{Spin}(1,3)\), not merely \(\mathrm{SO}(1,3)\).

Frame Theory therefore demonstrates that general relativity arises from Relativity Mechanics by taking the metric as the invariant of local frame admissibility.

---

## 1. Introduction

Relativity Mechanics teaches that physical content is not carried by individual descriptions but by equivalence classes of descriptions under admissibility transformations. Orbit Theory identifies the physical object with an orbit. Invariant Theory identifies measurable content with functions constant on that orbit.

Frame Theory applies this logic to the description of spacetime itself.

The primitive question is:

\[
\boxed{
\text{What if the admissible descriptions are local reference frames?}
}
\]

A local reference frame is not a physical object in itself. It is a presentation of local spacetime directions, local inertial axes, local laboratory orientations, and local spinor bases. Different local frames may describe the same physical geometry. The admissibility transformations relating such descriptions are local Lorentz transformations, or more fundamentally local spin transformations.

Thus we choose:

\[
\Omega_{\rm FT}=\{\text{local frames}\},
\]

\[
G_{\rm FT}=\mathrm{Spin}(1,3).
\]

More precisely, because the transformations may vary from point to point, the admissibility group is the gauge group

\[
\mathcal G_{\rm Spin}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

The invariant projection is

\[
I_{\rm FT}:\Omega_{\rm FT}\to \Omega_{\rm FT}/\mathcal G_{\rm Spin},
\]

and its principal geometric invariant is the metric

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

Thus Frame Theory is the theory of local frame orbits and their invariants.

General relativity is obtained when one:

1. takes the metric invariant seriously as the physical gravitational field,
2. imposes diffeomorphism admissibility,
3. introduces a torsion-free or dynamically torsion-free connection,
4. uses the invariant Einstein–Hilbert or Palatini action.

In this sense, Frame Theory is not an alternative to general relativity. It is the frame-relational foundation from which general relativity emerges.

---

## 2. The Relativity Schema of Frame Theory

Frame Theory is specified by the relativity schema

\[
\boxed{
\mathcal R_{\rm FT}
=
(\Omega_{\rm FT},G_{\rm FT},\triangleright,I_{\rm FT}).
}
\]

The ingredients are:

1. **Description space:**

   \[
   \Omega_{\rm FT}
   =
   \{\text{local Lorentz frames or coframes}\}.
   \]

2. **Admissibility group:**

   \[
   G_{\rm FT}
   =
   \mathrm{Spin}(1,3),
   \]

   or locally,

   \[
   \mathcal G_{\rm Spin}
   =
   C^\infty(M,\mathrm{Spin}(1,3)).
   \]

3. **Action:**

   \[
   e^I\mapsto \Lambda^I{}_J(x)e^J,
   \qquad
   \Lambda(x)\in \mathrm{Spin}(1,3).
   \]

4. **Invariant projection:**

   \[
   I_{\rm FT}(e)
   =
   g,
   \qquad
   g_{\mu\nu}
   =
   \eta_{IJ}e^I_\mu e^J_\nu.
   \]

The physical content of a frame description \(e\) is not the frame itself but its orbit

\[
[e]
=
\mathcal G_{\rm Spin}\cdot e.
\]

The metric \(g\) is the primary invariant of that orbit.

---

## 3. The Frame Description Space

Let \(M\) be a smooth four-dimensional manifold. A local frame may be described either by a basis of vector fields

\[
e_I=e_I^\mu\partial_\mu,
\qquad I=0,1,2,3,
\]

or by the dual coframe

\[
e^I=e^I_\mu dx^\mu.
\]

They satisfy

\[
e^I(e_J)=\delta^I_J.
\]

The coframe components obey

\[
e^I_\mu e_J^\mu=\delta^I_J,
\qquad
e^I_\mu e_I^\nu=\delta_\mu^\nu.
\]

We take the frame description space to be the space of Lorentz coframes:

\[
\Omega_{\rm FT}
=
\{e^I_\mu(x)\mid \det(e^I_\mu)\neq 0\}.
\]

Every coframe defines a Lorentzian metric by

\[
\boxed{
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu,
}
\]

where

\[
\eta_{IJ}=\operatorname{diag}(-1,1,1,1).
\]

The inverse metric is

\[
g^{\mu\nu}
=
\eta^{IJ}e_I^\mu e_J^\nu.
\]

The determinant of the metric satisfies

\[
\sqrt{-g}
=
|\det(e^I_\mu)|.
\]

For oriented and time-oriented frames,

\[
\sqrt{-g}
=
\det(e^I_\mu).
\]

Thus a coframe contains more information than the metric: it contains a choice of local Lorentz basis. The excess information is precisely the descriptive redundancy that Frame Theory quotients out.

---

## 4. The Spin Admissibility Group

The group \(\mathrm{Spin}(1,3)\) is the double cover of the proper orthochronous Lorentz group:

\[
\mathrm{Spin}(1,3)
\to
\mathrm{SO}^+(1,3).
\]

Its Lie algebra is

\[
\mathfrak{spin}(1,3)
\cong
\mathfrak{so}(1,3).
\]

We use \(\mathrm{Spin}(1,3)\) rather than \(\mathrm{SO}(1,3)\) because spinor fields, if present, require the double cover.

A local spin transformation is a smooth map

\[
S:M\to \mathrm{Spin}(1,3).
\]

In the vector representation,

\[
S(x)\mapsto \Lambda^I{}_J(x)\in \mathrm{SO}^+(1,3).
\]

The coframe transforms as

\[
\boxed{
e^I_\mu(x)
\mapsto
e'^I_\mu(x)
=
\Lambda^I{}_J(x)e^J_\mu(x).
}
\]

The inverse frame transforms contragrediently:

\[
e_I^\mu
\mapsto
e'_I{}^\mu
=
(\Lambda^{-1})^J{}_I e_J^\mu.
\]

The admissibility group is therefore

\[
\mathcal G_{\rm Spin}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

This is the local gauge group of frame admissibility.

---

## 5. The Metric Invariant

The central theorem of Frame Theory is that the metric is invariant under local spin transformations.

### Theorem 5.1: Metric invariance under local spin transformations

Let

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

Under

\[
e^I_\mu\mapsto \Lambda^I{}_K e^K_\mu,
\]

with

\[
\Lambda^I{}_K\Lambda^J{}_L\eta_{IJ}
=
\eta_{KL},
\]

the metric is invariant:

\[
g'_{\mu\nu}=g_{\mu\nu}.
\]

### Proof

We compute:

\[
g'_{\mu\nu}
=
\eta_{IJ}e'^I_\mu e'^J_\nu
=
\eta_{IJ}
\Lambda^I{}_K e^K_\mu
\Lambda^J{}_L e^L_\nu.
\]

Using Lorentz invariance of \(\eta\),

\[
\eta_{IJ}
\Lambda^I{}_K
\Lambda^J{}_L
=
\eta_{KL}.
\]

Therefore

\[
g'_{\mu\nu}
=
\eta_{KL}e^K_\mu e^L_\nu
=
g_{\mu\nu}.
\]

\(\square\)

Thus the metric is an invariant of the frame orbit.

Conversely, if two oriented, time-oriented coframes \(e\) and \(e'\) define the same metric, then they are related pointwise by a proper orthochronous Lorentz transformation. If the manifold admits a spin structure, this transformation lifts locally, and globally when spin data are included, to \(\mathrm{Spin}(1,3)\).

Therefore, up to orientation and time-orientation, the quotient of the coframe space by local spin transformations is the space of Lorentzian metrics:

\[
\boxed{
\Omega_{\rm FT}/\mathcal G_{\rm Spin}
\cong
\mathrm{Met}_{1,3}^{\rm orient.,\,time}(M).
}
\]

This is the precise sense in which Frame Theory produces metric geometry as an invariant of frame descriptions.

---

## 6. Orbit Ontology of Frames

According to Orbit Theory, the physical object is the orbit

\[
[e]
=
\mathcal G_{\rm Spin}\cdot e.
\]

The individual coframe \(e^I_\mu\) is a description. The orbit \([e]\) is the physical local geometric structure.

The invariant projection is

\[
I_{\rm FT}:\Omega_{\rm FT}\to \Omega_{\rm FT}/\mathcal G_{\rm Spin},
\]

\[
I_{\rm FT}(e)=[e].
\]

In metric terms,

\[
I_{\rm FT}(e)=g_{\mu\nu}.
\]

Thus:

\[
\boxed{
\text{The frame is a description; the metric is the invariant content.}
}
\]

This is the core ontological move of Frame Theory.

---

## 7. Spin Connections and Local Frame Covariance

To describe dynamics and parallel transport, Frame Theory introduces a spin connection

\[
\omega^{IJ}
=
\omega_\mu{}^{IJ}dx^\mu,
\]

with

\[
\omega^{IJ}=-\omega^{JI}.
\]

The spin connection is a connection on the local spin bundle. It defines covariant differentiation of Lorentz-tensor and spinor fields.

Under a local spin transformation, the connection transforms as

\[
\omega
\mapsto
\omega'
=
\Lambda\omega\Lambda^{-1}
-
(d\Lambda)\Lambda^{-1}.
\]

In components,

\[
\omega_\mu
\mapsto
\omega'_\mu
=
\Lambda\omega_\mu\Lambda^{-1}
-
(\partial_\mu\Lambda)\Lambda^{-1}.
\]

Infinitesimally, for

\[
\Lambda^I{}_J
=
\delta^I{}_J+\lambda^I{}_J,
\qquad
\lambda_{IJ}=-\lambda_{JI},
\]

the coframe transforms as

\[
\delta_\lambda e^I_\mu
=
\lambda^I{}_J e^J_\mu,
\]

and the spin connection transforms as

\[
\delta_\lambda \omega_\mu{}^{IJ}
=
-D_\mu\lambda^{IJ},
\]

where

\[
D_\mu\lambda^{IJ}
=
\partial_\mu\lambda^{IJ}
+
\omega_\mu{}^I{}_K\lambda^{KJ}
+
\omega_\mu{}^J{}_K\lambda^{IK}.
\]

Thus the spin connection is not itself invariant. It is a gauge potential for local frame admissibility.

---

## 8. Torsion and Curvature

Frame Theory defines two fundamental field strengths.

### 8.1 Torsion

The torsion two-form is

\[
\boxed{
T^I
=
de^I+\omega^I{}_J\wedge e^J.
}
\]

In components,

\[
T^I
=
\frac12 T^I{}_{\mu\nu}dx^\mu\wedge dx^\nu.
\]

Under local spin transformations,

\[
T^I\mapsto \Lambda^I{}_J T^J.
\]

Thus torsion is Lorentz-covariant.

### 8.2 Curvature

The curvature two-form is

\[
\boxed{
R^{IJ}
=
d\omega^{IJ}
+
\omega^I{}_K\wedge\omega^{KJ}.
}
\]

In components,

\[
R^{IJ}
=
\frac12 R^{IJ}{}_{\mu\nu}
dx^\mu\wedge dx^\nu.
\]

Under local spin transformations,

\[
R^{IJ}
\mapsto
\Lambda^I{}_K\Lambda^J{}_L R^{KL}.
\]

Thus curvature is also Lorentz-covariant.

### 8.3 Bianchi identities

The geometric Bianchi identities are

\[
DT^I
=
R^I{}_J\wedge e^J,
\]

\[
DR^{IJ}
=
0.
\]

Here \(D\) is the Lorentz-covariant exterior derivative.

These identities are structural consequences of Frame Theory and do not depend on a particular action.

---

## 9. Invariant Frame Observables

Invariant Theory says that measurable quantities must be invariant under local spin transformations.

Examples of local frame invariants include:

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu,
\]

\[
R
=
e_I^\mu e_J^\nu R^{IJ}{}_{\mu\nu},
\]

\[
R_{\mu\nu\rho\sigma}
R^{\mu\nu\rho\sigma},
\]

\[
\epsilon_{IJKL}e^I\wedge e^J\wedge R^{KL},
\]

and spinor bilinears constructed with appropriate frame covariance.

The volume form is also invariant:

\[
\epsilon
=
e^0\wedge e^1\wedge e^2\wedge e^3
=
\sqrt{-g}\,d^4x.
\]

Local frame components such as

\[
e^I_\mu(x)
\]

are not themselves invariant observables. They are descriptive variables. Physical quantities arise only after contraction, tracing, integration, or relational completion.

Thus Frame Theory obeys the central principle of Invariant Theory:

\[
\boxed{
\text{Frame components describe; frame invariants measure.}
}
\]

---

## 10. The Palatini Frame Action

The dynamics of Frame Theory is obtained by constructing an invariant action on the frame description space.

The first-order Palatini action is

\[
\boxed{
S[e,\omega]
=
\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
e^I\wedge e^J\wedge R^{KL}
+
S_{\rm matter}[e,\omega,\psi].
}
\]

Here

\[
\kappa=8\pi G,
\]

and

\[
\epsilon_{IJKL}
\]

is the internal Minkowski Levi-Civita symbol.

This action is invariant under local \(\mathrm{Spin}(1,3)\) transformations because:

1. \(\epsilon_{IJKL}\) is invariant,
2. \(e^I\) transforms covariantly,
3. \(R^{KL}\) transforms covariantly,
4. the wedge product and integration are coordinate-independent.

It is also diffeomorphism invariant when the fields are treated as differential forms on \(M\).

---

## 11. Variation with Respect to the Spin Connection

Vary the action with respect to \(\omega^{IJ}\). Since

\[
\delta R^{KL}
=
D\delta\omega^{KL},
\]

we have

\[
\delta_\omega S
=
\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
e^I\wedge e^J\wedge D\delta\omega^{KL}.
\]

Integrating by parts gives

\[
\delta_\omega S
=
-\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
D(e^I\wedge e^J)
\wedge
\delta\omega^{KL}
+
\text{boundary term}.
\]

The bulk equation is

\[
\boxed{
\epsilon_{IJKL}
D(e^I\wedge e^J)
=
0.
}
\]

Using

\[
De^I=T^I,
\]

this becomes

\[
\epsilon_{IJKL}
e^J\wedge T^K
=
0.
\]

For nondegenerate coframes in four dimensions, this implies

\[
\boxed{
T^I=0.
}
\]

Thus, in the absence of spin sources, the Palatini equation of motion for the connection enforces vanishing torsion.

The torsion-free condition is

\[
de^I+\omega^I{}_J\wedge e^J=0.
\]

This equation determines the spin connection uniquely in terms of the coframe. It is the frame version of the Levi-Civita connection.

---

## 12. Variation with Respect to the Coframe

Vary the action with respect to \(e^I\). One obtains

\[
\delta_e S
=
\frac{1}{\kappa}
\int
\epsilon_{IJKL}
\delta e^I\wedge e^J\wedge R^{KL}.
\]

If matter is present, define the matter stress-energy three-form \(\tau_I\) by

\[
\delta S_{\rm matter}
=
\int
\delta e^I\wedge \tau_I.
\]

The cofield equation is then

\[
\boxed{
\epsilon_{IJKL}
e^J\wedge R^{KL}
=
\kappa\tau_I.
}
\]

This is the tetrad form of the Einstein field equations.

In tensor notation, it is equivalent to

\[
\boxed{
G_{\mu\nu}
=
\kappa T_{\mu\nu}.
}
\]

Thus the dynamics of the frame invariant yields general relativistic gravitation.

---

## 13. Recovery of the Einstein–Hilbert Action

If the torsion-free condition is imposed,

\[
T^I=0,
\]

the spin connection becomes the Levi-Civita spin connection \(\omega(e)\). Substituting \(\omega(e)\) into the Palatini action gives the second-order Einstein–Hilbert action in frame variables.

Up to conventional normalization,

\[
S[e]
=
\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
e^I\wedge e^J\wedge R^{KL}(e).
\]

Equivalently,

\[
\boxed{
S[g]
=
\frac{1}{2\kappa}
\int
d^4x\,\sqrt{-g}\,R[g].
}
\]

Since

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu,
\]

the action depends on the frame only through its invariant metric, plus possible orientation data.

Thus general relativity is obtained by taking the metric invariant of Frame Theory and using the invariant curvature dynamics on the quotient.

---

## 14. General Relativity as a Frame Quotient Theory

General relativity emerges from Frame Theory through the following sequence.

### Step 1: Choose local frames as descriptions

\[
\Omega_{\rm FT}
=
\{e^I_\mu\}.
\]

### Step 2: Choose local spin transformations as admissibility transformations

\[
G_{\rm FT}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

### Step 3: Take the metric invariant

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

### Step 4: Identify frames related by local spin transformations

\[
e\sim \Lambda e.
\]

### Step 5: Include diffeomorphism admissibility

Coordinates are also descriptive. Therefore one further identifies

\[
g\sim \phi^*g,
\qquad
\phi\in \operatorname{Diff}(M).
\]

### Step 6: Use invariant dynamics

The Einstein–Hilbert or Palatini action yields

\[
G_{\mu\nu}
=
\kappa T_{\mu\nu}.
\]

Therefore:

\[
\boxed{
\text{General relativity is Frame Theory plus metric invariance, diffeomorphism admissibility, and torsion-free curvature dynamics.}
}
\]

The metric is not introduced as an absolute primitive. It is the invariant of local frame descriptions.

---

## 15. Diffeomorphisms and the Full Admissibility Group

The primitive Frame Theory specified by the user takes

\[
G=\mathrm{Spin}(1,3).
\]

This identifies local Lorentz frame redundancy. To obtain full general relativity, one must also treat coordinate descriptions as admissible.

The full frame-gravity admissibility group is therefore

\[
\boxed{
G_{\rm GR}^{\rm frame}
=
\operatorname{Diff}(M)
\ltimes
C^\infty(M,\mathrm{Spin}(1,3)).
}
\]

A diffeomorphism \(\phi\) acts on the coframe by pullback:

\[
e^I\mapsto \phi^*e^I.
\]

A local spin transformation acts by internal rotation:

\[
e^I\mapsto \Lambda^I{}_J e^J.
\]

The metric is invariant under both:

\[
g\mapsto \phi^*g,
\]

with physical geometry given by the diffeomorphism orbit

\[
[g].
\]

Thus Frame Theory naturally extends to the full relativity schema of general relativity:

\[
\mathcal R_{\rm GR}^{\rm frame}
=
(\Omega_{\rm FT},
\operatorname{Diff}(M)\ltimes\mathcal G_{\rm Spin},
\triangleright,
I).
\]

---

## 16. Einstein–Cartan Theory from Frame Theory

If the spin connection is treated as independent and matter carries intrinsic spin, the connection equation need not imply vanishing torsion.

Let the matter spin current be

\[
\Sigma^{IJ}.
\]

The variation of the matter action with respect to \(\omega_{IJ}\) gives

\[
\delta S_{\rm matter}
=
\frac12
\int
\delta\omega_{IJ}\wedge \Sigma^{IJ}.
\]

The connection equation becomes

\[
\boxed{
\epsilon_{IJKL}
D(e^I\wedge e^J)
=
\kappa\Sigma_{KL}.
}
\]

Equivalently, torsion is sourced by spin:

\[
T^I
\sim
\kappa\,\text{spin density}.
\]

The resulting theory is Einstein–Cartan theory.

In Einstein–Cartan theory:

1. the metric is still the primary invariant of the coframe orbit,
2. the spin connection is independent,
3. torsion is nonzero in the presence of spin,
4. for ordinary macroscopic matter, torsion is typically negligible,
5. in vacuum, torsion usually vanishes and general relativity is recovered.

Thus Einstein–Cartan theory is another natural specialization of Frame Theory.

---

## 17. Why \(\mathrm{Spin}(1,3)\) Rather Than \(\mathrm{SO}(1,3)\)?

For purely bosonic tensor geometry, \(\mathrm{SO}^+(1,3)\) is often sufficient. However, the fundamental admissibility group in Frame Theory is taken to be

\[
\mathrm{Spin}(1,3)
\]

because physical matter includes spinor fields.

Let \(\psi\) be a Dirac spinor. It transforms under the spin representation:

\[
\psi\mapsto S(x)\psi,
\qquad
S(x)\in \mathrm{Spin}(1,3).
\]

The gamma matrices satisfy the Clifford algebra

\[
\{\gamma^I,\gamma^J\}
=
2\eta^{IJ}.
\]

The spinor covariant derivative is

\[
D_\mu\psi
=
\partial_\mu\psi
+
\frac14\omega_\mu{}^{IJ}\gamma_{IJ}\psi,
\]

where

\[
\gamma_{IJ}
=
\frac12[\gamma_I,\gamma_J].
\]

The curved-spacetime Dirac action is

\[
S_{\rm Dirac}
=
\int d^4x\,e
\left[
\frac{i}{2}
\left(
\bar\psi\gamma^I e_I^\mu D_\mu\psi
-
D_\mu\bar\psi\,\gamma^I e_I^\mu\psi
\right)
-
m\bar\psi\psi
\right].
\]

This action is invariant under local spin transformations provided the coframe, spin connection, and spinor transform consistently.

Thus the use of \(\mathrm{Spin}(1,3)\) is not optional if the frame theory is to accommodate fermions. It is required by the admissibility of spinorial descriptions.

---

## 18. Frame Theory and Local Measurement

Frames are not merely mathematical conveniences. They model local laboratories.

An observer carrying an orthonormal frame measures components of tensors in that frame. For example, the electromagnetic field measured by a local frame is

\[
F_{IJ}
=
e_I^\mu e_J^\nu F_{\mu\nu}.
\]

The electric field measured by the observer whose four-velocity is aligned with \(e_0\) is

\[
E_I
=
F_{I0},
\]

and the magnetic field is

\[
B^I
=
\frac12\epsilon^I{}_{JK}F^{JK}.
\]

Under a local frame rotation, the components \(F_{IJ}\) transform, but scalar invariants such as

\[
F_{\mu\nu}F^{\mu\nu},
\]

\[
F_{\mu\nu}{}^\ast F^{\mu\nu},
\]

remain unchanged.

Thus Frame Theory clarifies the operational meaning of local measurement:

\[
\boxed{
\text{Local frames present measurements; invariants constitute measured facts.}
}
\]

The frame is the observer’s descriptive interface. The invariant is the physical content.

---

## 19. Frame Theory and Gauge Structure

Frame Theory has the structure of a gauge theory.

The spin bundle

\[
P_{\rm Spin}(M)\to M
\]

is a principal \(\mathrm{Spin}(1,3)\)-bundle. The spin connection \(\omega\) is a gauge connection. Its curvature \(R\) is the gauge field strength. The coframe \(e^I\) is an additional Lorentz-vector-valued one-form.

The local admissibility group is

\[
\mathcal G_{\rm Spin}
=
\operatorname{Aut}(P_{\rm Spin}).
\]

The quotient

\[
\Omega_{\rm FT}/\mathcal G_{\rm Spin}
\]

produces metric geometry.

Thus Frame Theory is simultaneously:

1. a gauge theory of local Lorentz frames,
2. a geometric theory of spacetime,
3. a relational theory of local reference systems,
4. a specialization of Relativity Mechanics.

This places general relativity and gauge theory within the same foundational pattern.

---

## 20. Frame Theory and Constraints

In canonical form, Frame Theory possesses constraints corresponding to admissibility transformations.

Local Lorentz invariance gives Lorentz constraints:

\[
\mathcal J^{IJ}\approx0.
\]

Spatial diffeomorphism invariance gives momentum constraints:

\[
\mathcal H_i\approx0.
\]

Time reparametrization or hypersurface-deformation invariance gives Hamiltonian constraints:

\[
\mathcal H_\perp\approx0.
\]

Physical observables must commute with these constraints:

\[
\{O,\mathcal J^{IJ}\}=0,
\]

\[
\{O,\mathcal H_i\}=0,
\]

\[
\{O,\mathcal H_\perp\}=0.
\]

Thus the constraint structure of general relativity is inherited directly from the frame admissibility structure.

---

## 21. Frame Theory and the Geometry of the Quotient

The quotient structure of Frame Theory may be summarized as follows.

Starting with the coframe space,

\[
\Omega_{\rm FT},
\]

quotient by local spin transformations:

\[
\Omega_{\rm FT}/\mathcal G_{\rm Spin}
\cong
\mathrm{Met}_{1,3}^{\rm orient.,\,time}(M).
\]

Then quotient by diffeomorphisms:

\[
\mathrm{Met}_{1,3}(M)/\operatorname{Diff}(M).
\]

This final quotient is the superspace of general relativity.

Thus the hierarchy is:

\[
\boxed{
\text{frames}
\longrightarrow
\text{metrics}
\longrightarrow
\text{geometries}.
}
\]

Or, in orbit language:

\[
\boxed{
e^I_\mu
\longrightarrow
[e^I_\mu]_{\mathrm{Spin}}
\longrightarrow
[g_{\mu\nu}]_{\operatorname{Diff}}.
}
\]

The physical gravitational field is the final orbit.

---

## 22. Frame Theory and Invariant Geometry

Frame Theory does not deny the reality of geometry. It explains the origin of geometric invariants.

The metric is invariant under local frame rotations.

The curvature scalar is invariant under local frame rotations and diffeomorphisms:

\[
R
=
e_I^\mu e_J^\nu R^{IJ}{}_{\mu\nu}.
\]

The Einstein tensor is invariant:

\[
G_{\mu\nu}
=
R_{\mu\nu}
-
\frac12 Rg_{\mu\nu}.
\]

The field equations are tensorial and therefore admissibility-covariant:

\[
G_{\mu\nu}
=
\kappa T_{\mu\nu}.
\]

But the measurable physical content is not the coordinate components of \(G_{\mu\nu}\). It is the invariant relations among geometric and material fields.

Thus Frame Theory unites the gauge-theoretic and geometric presentations of gravity.

---

## 23. Frame Theory Within Relativity Mechanics

Frame Theory is not the foundation of Relativity Mechanics. It is a high-level specialization.

It presupposes:

1. **Orbit Theory:** physical objects are orbits.
2. **Invariant Theory:** measurable quantities are invariants.
3. **Observer Theory:** frames are observational structures.
4. **Constraint Mechanics:** local frame symmetries generate constraints.
5. **Relativistic Dynamics:** frame dynamics descends to the quotient.
6. **Relativity Geometry:** geometry is induced on quotient spaces.
7. **Gauge Theory of Admissibility:** local frame transformations are gauge transformations.

Frame Theory then chooses the specific admissibility group

\[
\mathrm{Spin}(1,3).
\]

It therefore answers the primitive question:

\[
\boxed{
\text{What if the admissible descriptions are local reference frames?}
}
\]

with the construction:

\[
\Omega=\{\text{frames}\},
\qquad
G=\mathrm{Spin}(1,3).
\]

The result is Frame Theory.

Taking the metric invariant yields general relativity.

---

## 24. Variants of Frame-Based Gravitation

Frame Theory also provides a common language for related gravitational theories.

### 24.1 General relativity

Impose torsion-free connection:

\[
T^I=0.
\]

Recover Levi-Civita geometry and Einstein equations.

### 24.2 Einstein–Cartan theory

Allow independent spin connection and spin sources:

\[
T^I\neq0.
\]

Torsion couples to spin current.

### 24.3 Teleparallel gravity

Use curvature-free connection and torsion-based dynamics. The coframe remains fundamental, but the invariant metric is still

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

### 24.4 Poincaré gauge theory

Enlarge the admissibility group to include local translations as well as local Lorentz transformations.

All of these remain within the frame-relational logic of Relativity Mechanics. They differ by the choice of connection, constraints, and dynamical invariants.

---

## 25. Summary of the Frame-Theoretic Derivation

The central derivation may be summarized as follows.

Choose

\[
\Omega_{\rm FT}
=
\{e^I_\mu\},
\]

\[
G_{\rm FT}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

The action is

\[
e^I_\mu
\mapsto
\Lambda^I{}_J(x)e^J_\mu.
\]

The invariant projection is

\[
I_{\rm FT}(e)
=
g,
\]

with

\[
\boxed{
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
}
\]

The spin connection transforms as

\[
\omega
\mapsto
\Lambda\omega\Lambda^{-1}
-
(d\Lambda)\Lambda^{-1}.
\]

The torsion and curvature are

\[
T^I
=
de^I+\omega^I{}_J\wedge e^J,
\]

\[
R^{IJ}
=
d\omega^{IJ}
+
\omega^I{}_K\wedge\omega^{KJ}.
\]

The invariant Palatini action is

\[
S[e,\omega]
=
\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
e^I\wedge e^J\wedge R^{KL}.
\]

Variation gives

\[
T^I=0
\]

in vacuum, and

\[
\epsilon_{IJKL}
e^J\wedge R^{KL}
=
\kappa\tau_I.
\]

In tensor form:

\[
\boxed{
G_{\mu\nu}
=
\kappa T_{\mu\nu}.
}
\]

Thus general relativity is recovered.

---

## 26. Conclusion

Frame Theory answers the primitive question:

\[
\boxed{
\text{What if the admissible descriptions are local reference frames?}
}
\]

The answer is to take

\[
\boxed{
\Omega=\{\text{frames}\},
\qquad
G=\mathrm{Spin}(1,3).
}
\]

The resulting relativity schema is

\[
\mathcal R_{\rm FT}
=
(\Omega_{\rm FT},G_{\rm FT},\triangleright,I_{\rm FT}).
\]

The physical object is the orbit of local frames. The central invariant is the metric:

\[
\boxed{
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
}
\]

The metric is therefore not primitive. It is the invariant content of a local frame orbit.

Introducing a spin connection, curvature, and torsion yields a gauge-theoretic frame dynamics. The invariant Palatini action produces the Einstein equations when torsion is absent or dynamically suppressed. Allowing torsion sourced by spin yields Einstein–Cartan theory. Including spinors requires the full \(\mathrm{Spin}(1,3)\) admissibility group.

Thus Frame Theory demonstrates that general relativity is not an independent starting point. It is a theorem-level specialization of Relativity Mechanics obtained by choosing local frames as descriptions, local spin transformations as admissibility transformations, and the metric as the invariant.

\[
\boxed{
\text{General relativity emerges from Frame Theory by taking the metric invariant of local frame orbits.}
}
\]

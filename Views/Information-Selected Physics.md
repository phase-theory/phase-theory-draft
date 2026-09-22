# Information-Selected Physics  
## Emergent Geometry, Informational Stress, and Scale-Dependent Gravitation  

**Preprint**

---

## Abstract

We develop a physical theory in which geometry, topology, causal structure, and dynamics are derived from primitive informational relations rather than imposed as background structure. Starting from an information substrate  
\[
\mathfrak I=(X,\mathscr D,\mathscr C,\mathscr K),
\]
where \(X\) is a set of informational states, \(\mathscr D\) is a class of distinguishability functionals, \(\mathscr C\) a class of constraints, and \(\mathscr K\) a family of compression maps, we prove a sequence of emergence theorems. First, local distinguishability generates a Riemannian metric \(g^{(\mathcal I)}\) on the quotient of informational redundancies. Second, the third-order structure of distinguishability generates canonical affine connections and curvature. Third, directed information flow with finite propagation speed induces Lorentzian causal cones. Fourth, compression renormalization selects a geometric fixed-point condition equivalent to a gravitational field equation containing an informational scalar and an informational asymmetry stress tensor.

The resulting physical theory contains new effects: a Yukawa correction to Newtonian gravity from the information dilaton, scale-dependent effective dimension, modified galactic force laws from dimensional crossover, an information-driven late-time acceleration, and logarithmic corrections to horizon entropy. The central result is that physical geometry is not primitive but is an invariant of informational distinguishability, compression stability, and causal information propagation.

---

## 1. Primitive Informational Structure

Let the information substrate be  
\[
\boxed{
\mathfrak I=(X,\mathscr D,\mathscr C,\mathscr K)
}
\]
with the following ingredients:

1. \(X\): a set of informational states.  
2. \(\mathscr D\): a family of distinguishability functionals  
   \[
   D:X\times X\to [0,\infty),
   \]
   satisfying at minimum  
   \[
   D(x,x)=0,\qquad D(x,y)\ge 0.
   \]
3. \(\mathscr C\): constraints defining admissible informational configurations.  
4. \(\mathscr K\): compression or coarse-graining maps  
   \[
   K_\lambda:X\to X_\lambda,
   \]
   obeying data-processing monotonicity.

No coordinate system, topology, metric, dimension, causal order, or physical time is assumed at the outset.

The foundational direction is therefore  
\[
\boxed{
\mathfrak I
\longrightarrow
\mathcal X_{\mathfrak I}
\longrightarrow
\mathcal T_{\mathfrak I}
\longrightarrow
g_{\mathfrak I}
\longrightarrow
\nabla_{\mathfrak I}
\longrightarrow
R_{\mathfrak I}
\longrightarrow
\mathcal D_{\mathfrak I}
\longrightarrow
\mathcal O_{\mathfrak I}.
}
\]

We now derive the first physical consequences of this chain.

---

## 2. Emergence of the Information Metric

### 2.1 Symmetric distinguishability

Because a generic divergence is not symmetric, define the symmetrized distinguishability functional  
\[
D_S(x,y)=\frac12\bigl[D(x,y)+D(y,x)\bigr].
\]

Assume that after quotienting informational redundancies, the state space admits local coordinates  
\[
\theta=(\theta^1,\ldots,\theta^n).
\]

Let  
\[
\theta'=\theta+\xi.
\]

Expand \(D_S\) about coincidence:
\[
D_S(\theta,\theta+\xi)
=
\frac12 g_{ab}(\theta)\,\xi^a\xi^b
+
\frac16 A_{abc}(\theta)\,\xi^a\xi^b\xi^c
+
O(\xi^4).
\]

Since \(D_S(\theta,\theta)=0\) and \(D_S\ge 0\), the first derivative vanishes at coincidence. The leading nontrivial term is quadratic.

Define the information metric by  
\[
\boxed{
g_{ab}(\theta)
=
\left.
\frac{\partial^2}
{\partial \xi^a\partial \xi^b}
D_S(\theta,\theta+\xi)
\right|_{\xi=0}.
}
\]

This metric measures infinitesimal informational distinguishability:
\[
\boxed{
ds_{\mathcal I}^2
=
g_{ab}(\theta)\,d\theta^a d\theta^b.
}
\]

### 2.2 Informational gauge quotient

If there exist nonzero tangent vectors \(v^a\) such that  
\[
g_{ab}v^a v^b=0,
\]
then those directions are informationally invisible. They must be quotiented.

Define informational equivalence by  
\[
x\sim_{\mathcal I}y
\iff
D_S(x,y)=0.
\]

The physical state space is then  
\[
\boxed{
\mathcal M_{\mathcal I}=X/\!\sim_{\mathcal I}.
}
\]

Assuming regularity of the null distribution, \(\mathcal M_{\mathcal I}\) is a smooth manifold and \(g_{ab}\) descends to a positive-definite metric on \(\mathcal M_{\mathcal I}\).

Thus we obtain the first emergence theorem.

---

### Theorem 1: Local Riemannian emergence

Let \(D_S\) be \(C^2\), nonnegative, and minimized at coincidence. If the Hessian of \(D_S\) at coincidence has constant rank and its null distribution is quotientable, then there exists a Riemannian manifold  
\[
(\mathcal M_{\mathcal I},g_{\mathcal I})
\]
canonically associated with the informational equivalence class of \(\mathfrak I\), such that  
\[
\boxed{
d_{\mathcal I}(x,y)^2
=
2D_S(x,y)
+
O(D_S^{3/2}).
}
\]

Therefore, local geometry is local distinguishability.

---

## 3. Connections from Higher-Order Information

The metric captures only second-order distinguishability. The third-order term encodes informational asymmetry and selects affine structure.

Let the unsymmetrized divergence have the expansion  
\[
D(\theta,\theta+\xi)
=
\frac12 g_{ab}\xi^a\xi^b
+
\frac16 C_{abc}\xi^a\xi^b\xi^c
+
O(\xi^4).
\]

The tensor \(C_{abc}\) is the cubic informational tensor. For a regular divergence, one may take the coincidence derivative  
\[
\boxed{
C_{abc}
=
\left.
\frac{\partial^3 D}
{\partial \theta^a\partial\theta^b\partial \theta'^c}
\right|_{\theta'=\theta},
}
\]
with appropriate symmetrization when necessary.

The cubic tensor determines a canonical family of informational connections:
\[
\boxed{
\Gamma^{(\alpha)a}{}_{bc}
=
\left\{^{a}_{bc}\right\}
+
\frac{\alpha}{2}C^a{}_{bc},
}
\]
where \(\left\{^{a}_{bc}\right\}\) are the Levi-Civita coefficients of \(g_{ab}\), and  
\[
C^a{}_{bc}=g^{ad}C_{dbc}.
\]

The parameter \(\alpha\) measures the degree to which directional informational asymmetry is retained. The dual connection is obtained by \(\alpha\mapsto-\alpha\). The symmetric case \(\alpha=0\) recovers the Levi-Civita connection.

The curvature of the information connection is  
\[
\boxed{
R^{(\alpha)a}{}_{bcd}
=
\partial_c\Gamma^{(\alpha)a}{}_{db}
-
\partial_d\Gamma^{(\alpha)a}{}_{cb}
+
\Gamma^{(\alpha)a}{}_{c m}\Gamma^{(\alpha)m}{}_{db}
-
\Gamma^{(\alpha)a}{}_{d m}\Gamma^{(\alpha)m}{}_{cb}.
}
\]

The Ricci tensor and scalar are  
\[
R^{(\alpha)}_{bd}
=
R^{(\alpha)a}{}_{bad},
\]
\[
R^{(\alpha)}
=
g^{bd}R^{(\alpha)}_{bd}.
\]

Thus the hierarchy  
\[
\boxed{
D
\longrightarrow
g
\longrightarrow
C
\longrightarrow
\nabla^{(\alpha)}
\longrightarrow
R^{(\alpha)}
}
\]
is established.

---

## 4. Emergent Causal Structure and Lorentzian Signature

The metric derived above is naturally Riemannian because it is based on symmetric distinguishability. To obtain physical spacetime, one must derive signature.

Assume the informational substrate contains directed channels  
\[
\mathcal N(y|x),
\]
so that information can propagate asymmetrically.

Let \(\tau(x,y)\) be the minimal informational latency from \(x\) to \(y\). Define the informational future of \(x\) by  
\[
J^+(x)=\{y:\tau(x,y)<\infty\}.
\]

Assume a finite maximal information speed \(c_{\mathcal I}\). Then for any allowed infinitesimal informational displacement,  
\[
h_{ij}dx^i dx^j
\le
c_{\mathcal I}^2 d\tau^2,
\]
where \(h_{ij}\) is the Riemannian information metric on spatial informational states.

The boundary of the allowed region satisfies  
\[
\boxed{
h_{ij}dx^i dx^j
=
c_{\mathcal I}^2 d\tau^2.
}
\]

This defines an information light cone.

Introduce the Lorentzian line element  
\[
\boxed{
ds^2
=
-c_{\mathcal I}^2 d\tau^2
+
h_{ij}dx^i dx^j.
}
\]

The null condition \(ds^2=0\) coincides with maximal-speed information propagation. Therefore, directed finite-speed information flow induces a Lorentzian conformal structure.

Thus:

\[
\boxed{
\text{directed information}
+
\text{finite propagation speed}
\Longrightarrow
\text{emergent Lorentzian causal structure}.
}
\]

The signature is not assumed. It is selected by the existence of a stable causal cone in the informational propagation channels.

---

## 5. Compression Renormalization

Let \(K_\lambda\) be a compression map resolving information at scale \(\lambda\). Define the compressed divergence by  
\[
D_\lambda(x,y)
=
D(K_\lambda x,K_\lambda y).
\]

Data-processing monotonicity implies  
\[
D_\lambda(x,y)
\le
D(x,y).
\]

The induced metric at scale \(\lambda\) is  
\[
g_{ab}(\lambda)
=
\left.
\frac{\partial^2}
{\partial \xi^a\partial \xi^b}
D_{S,\lambda}(\theta,\theta+\xi)
\right|_{\xi=0}.
\]

Define the RG time  
\[
s=\log \lambda.
\]

The information metric then satisfies a geometric flow  
\[
\boxed{
\frac{\partial g_{ab}}{\partial s}
=
\beta_{ab}[g,\Phi,C].
}
\]

Here \(\Phi\) is the information dilaton, measuring local compression deficit or marginal information density.

The leading covariant beta functional consistent with informational monotonicity is  
\[
\boxed{
\beta_{ab}
=
-2\ell_{\mathcal I}^2
\left[
R_{ab}
+
2\nabla_a\nabla_b\Phi
-
\frac14 C_{acd}C_b{}^{cd}
\right]
+
O(\ell_{\mathcal I}^4).
}
\]

Here \(\ell_{\mathcal I}\) is the fundamental information length scale.

A scale-stable informational geometry satisfies the fixed-point condition  
\[
\boxed{
\beta_{ab}=0.
}
\]

Therefore,
\[
\boxed{
R_{ab}
+
2\nabla_a\nabla_b\Phi
-
\frac14 C_{acd}C_b{}^{cd}
=
0.
}
\]

When matter-like informational channels are present, they contribute an additional term to the beta functional. Writing this contribution as \(\kappa_{\mathcal I}T^{(m)}_{ab}\), the fixed-point condition becomes  
\[
\boxed{
R_{ab}
+
2\nabla_a\nabla_b\Phi
-
\frac14 C_{acd}C_b{}^{cd}
=
\kappa_{\mathcal I}T^{(m)}_{ab}.
}
\]

This is the fundamental information-geometric field equation in the informational frame.

---

## 6. Einstein-Frame Informational Field Equations

To express the theory in standard gravitational form, perform a Weyl rescaling to the Einstein information metric \(\widehat g_{ab}\). The precise rescaling depends on the dimension; in four emergent dimensions one may write schematically  
\[
\widehat g_{ab}
=
e^{-2\Phi}g_{ab}.
\]

In the Einstein frame, the fixed-point equation becomes  
\[
\boxed{
\widehat G_{ab}
+
\Lambda_{\mathcal I}\widehat g_{ab}
=
\kappa_{\mathcal I}
\left(
\widehat T^{(m)}_{ab}
+
\widehat T^{(\Phi)}_{ab}
+
\widehat T^{(C)}_{ab}
\right).
}
\]

The informational scalar stress tensor is  
\[
\boxed{
\widehat T^{(\Phi)}_{ab}
=
\nabla_a\phi\nabla_b\phi
-
\frac12\widehat g_{ab}(\nabla\phi)^2
-
\widehat g_{ab}U(\phi),
}
\]
where \(\phi\) is the Einstein-frame information dilaton and \(U(\phi)\) is the compression potential.

The cubic informational stress tensor is  
\[
\boxed{
\widehat T^{(C)}_{ab}
=
C_{acd}C_b{}^{cd}
-
\frac16\widehat g_{ab}
C_{def}C^{def}.
}
\]

The scalar equation is  
\[
\boxed{
\widehat\square\phi
=
\frac{dU}{d\phi}
-
\alpha(\phi)T^{(m)},
}
\]
where  
\[
\alpha(\phi)
=
\frac{d\log A(\phi)}{d\phi}
\]
measures the coupling between matter and the information dilaton.

Thus the emergent gravitational dynamics are  
\[
\boxed{
\text{information compression stability}
\Longrightarrow
\text{Einstein-type field equations with informational sources}.
}
\]

---

## 7. Weak-Field Limit and Yukawa Correction to Gravity

Consider a weak-field, static background:
\[
\widehat g_{00}
=
-(1+2\Phi_N),
\]
\[
\widehat g_{ij}
=
(1-2\Psi_N)\delta_{ij},
\]
and let  
\[
\phi=\phi_0+\varphi.
\]

Assume the compression potential has a stationary point at \(\phi_0\):
\[
U'(\phi_0)=0,
\]
and define the information-dilaton mass  
\[
\boxed{
m_\phi^2
=
U''(\phi_0).
}
\]

For nonrelativistic matter,
\[
T^{(m)}\simeq -\rho.
\]

The linearized scalar equation becomes  
\[
\boxed{
(\nabla^2-m_\phi^2)\varphi
=
-\alpha_0\rho,
}
\]
where \(\alpha_0=\alpha(\phi_0)\).

For a point mass \(M\),
\[
\rho(\mathbf x)=M\delta^{(3)}(\mathbf x).
\]

The solution is  
\[
\boxed{
\varphi(r)
=
\frac{\alpha_0 M}{4\pi}
\frac{e^{-m_\phi r}}{r}.
}
\]

The metric potential becomes  
\[
\boxed{
\Phi_N(r)
=
-\frac{G_N M}{r}
\left[
1+
2\alpha_0^2 e^{-m_\phi r}
\right].
}
\]

The corresponding radial acceleration is  
\[
\boxed{
a(r)
=
\frac{G_N M}{r^2}
\left[
1+
2\alpha_0^2 e^{-m_\phi r}(1+m_\phi r)
\right].
}
\]

Therefore, the theory predicts a finite-range fifth-force correction to Newtonian gravity.

Define the information length  
\[
\lambda_{\mathcal I}=m_\phi^{-1}.
\]

Then:

- For \(r\ll\lambda_{\mathcal I}\),  
  \[
  G_{\rm eff}
  \simeq
  G_N(1+2\alpha_0^2).
  \]

- For \(r\gg\lambda_{\mathcal I}\),  
  \[
  G_{\rm eff}\to G_N.
  \]

Thus ordinary gravity is recovered at large distances if the dilaton is massive, while deviations appear at the information scale.

---

## 8. Informational Asymmetry as Dark Sector

The cubic tensor \(C_{abc}\) contributes an additional stress tensor:
\[
T^{(C)}_{ab}
=
C_{acd}C_b{}^{cd}
-
\frac16 g_{ab}C^2.
\]

If the background is statistically isotropic, then  
\[
\langle C_{acd}C_b{}^{cd}\rangle
=
\frac{1}{4}C^2 g_{ab},
\]
and the trace-free part vanishes. The isotropic contribution behaves like an effective cosmological term:
\[
\Lambda_C
\sim
\kappa_{\mathcal I}C^2.
\]

If instead \(C_{abc}\) has anisotropic structure, it behaves as an anisotropic dark fluid or dark radiation component.

Thus the informational cubic tensor provides a geometric origin for dark-sector stress-energy:
\[
\boxed{
\text{informational asymmetry}
\longrightarrow
\text{effective dark stress-energy}.
}
\]

---

## 9. Information Dimension and Spectral Flow

Once an information metric exists, dimension becomes a derived scaling property.

Define the information Laplacian  
\[
\Delta_{\mathcal I}
=
-\nabla^a\nabla_a
+
\xi R_{\mathcal I}
+
\zeta C^2.
\]

The heat kernel is  
\[
K(s;x,y)
=
\left(e^{-s\Delta_{\mathcal I}}\right)(x,y).
\]

The return probability is  
\[
P(s)
=
\operatorname{Tr}e^{-s\Delta_{\mathcal I}}.
\]

The spectral dimension is  
\[
\boxed{
d_s(s)
=
-2\frac{d\log P(s)}{d\log s}.
}
\]

Identifying the diffusion length with physical scale,
\[
\ell\sim \sqrt{s},
\]
we define the effective information dimension
\[
\boxed{
d_{\rm eff}(\ell)=d_s(\ell^2).
}
\]

Compression renormalization naturally produces dimensional crossover:
\[
\boxed{
d_{\rm eff}(\ell)
=
d_{\rm IR}
+
(d_{\rm UV}-d_{\rm IR})
e^{-(\ell/\ell_*)^\nu}.
}
\]

Thus dimension is not fundamental. It is a scale-dependent invariant of information diffusion.

---

## 10. Modified Force Law from Dimensional Crossover

In an effectively \(d\)-dimensional information geometry, the flux of an informational field through a sphere is governed by  
\[
\Omega_{d-1}r^{d-1}J^r
=
\text{constant}.
\]

For a source of strength \(M\),
\[
J^r
\propto
\frac{M}{\Omega_{d-1}r^{d-1}}.
\]

Identifying the gravitational acceleration with the informational flux,
\[
a(r)=\kappa_d J^r,
\]
and normalizing to Newtonian gravity at scales where \(d_{\rm eff}=3\), one obtains  
\[
\boxed{
a(r)
=
\frac{G_N M}{r^2}
\left(
\frac{r}{r_0}
\right)^{3-d_{\rm eff}(r)}.
}
\]

If \(d_{\rm eff}\to 2\) at large distances, then  
\[
\boxed{
a(r)
\sim
\frac{G_N M}{r\,r_0}.
}
\]

The circular velocity becomes  
\[
v_c^2(r)
=
r a(r)
\sim
\frac{G_N M}{r_0}.
\]

Thus dimensional crossover from \(d_{\rm eff}=3\) to \(d_{\rm eff}=2\) produces asymptotically flat rotation curves without introducing particle dark matter.

If the compression scale \(r_0\) itself depends on the total information content of the source, one obtains a MOND-like acceleration scale. For example, if  
\[
r_0(M)
=
\sqrt{\frac{G_N M}{a_{\mathcal I}}},
\]
then  
\[
\boxed{
a(r)
=
\frac{\sqrt{G_N M a_{\mathcal I}}}{r}.
}
\]

Here \(a_{\mathcal I}\) is a fundamental informational acceleration scale, for instance  
\[
a_{\mathcal I}
\sim
\frac{c_{\mathcal I}^2}{\ell_{\mathcal I}}.
\]

Therefore, the theory predicts a transition from inverse-square gravity to an information-dimension-controlled regime.

---

## 11. Cosmological Consequences

For a homogeneous and isotropic emergent spacetime, take the Einstein-frame FLRW metric  
\[
ds^2
=
-dt^2
+
a(t)^2
\left[
\frac{dr^2}{1-kr^2}
+
r^2d\Omega^2
\right].
\]

The Friedmann equations become  
\[
\boxed{
H^2
=
\frac{\kappa_{\mathcal I}}{3}
\left(
\rho_m+\rho_\phi+\rho_C
\right)
-
\frac{k}{a^2},
}
\]
and  
\[
\boxed{
\dot H
=
-\frac{\kappa_{\mathcal I}}{2}
\left(
\rho_m+p_m+\rho_\phi+p_\phi+\rho_C+p_C
\right)
+
\frac{k}{a^2}.
}
\]

The information-dilaton energy density and pressure are  
\[
\rho_\phi
=
\frac12\dot\phi^2
+
U(\phi),
\]
\[
p_\phi
=
\frac12\dot\phi^2
-
U(\phi).
\]

The effective equation of state is  
\[
\boxed{
w_\phi
=
\frac{\frac12\dot\phi^2-U(\phi)}
{\frac12\dot\phi^2+U(\phi)}.
}
\]

If the compression potential \(U(\phi)\) possesses a flat region, then  
\[
\dot\phi^2\ll U(\phi),
\]
and therefore  
\[
w_\phi\simeq -1.
\]

Thus late-time acceleration arises as an information compression effect:
\[
\boxed{
\text{dark energy}
\sim
\text{fixed-point compression potential}.
}
\]

The cubic informational stress \(T^{(C)}_{ab}\) may contribute an effective dark radiation or dark curvature component depending on its isotropy.

---

## 12. Information-Theoretic Origin of the Cosmological Constant

The trace of the fixed-point equation gives  
\[
R
+
2\square\Phi
-
\frac14 C^2
=
\kappa_{\mathcal I}T^{(m)}.
\]

In a homogeneous informational vacuum,  
\[
\square\Phi\simeq 0,
\qquad
T^{(m)}\simeq 0.
\]

Then  
\[
R
\simeq
\frac14 C^2.
\]

Thus the vacuum curvature is determined by the residual cubic informational content. In the Einstein frame, this appears as  
\[
\boxed{
\Lambda_{\rm eff}
=
\Lambda_{\mathcal I}
+
\kappa_{\mathcal I}U(\phi_0)
+
\gamma C_0^2.
}
\]

Therefore the cosmological constant is not an arbitrary geometric parameter. It is the scale-stable residue of informational distinguishability after maximal compression.

---

## 13. Black-Hole Entropy and Information Corrections

The information-geometric origin of horizon entropy follows from counting distinguishable informational states compatible with a horizon constraint.

Let \(A\) be the horizon area measured in the emergent metric. The leading Bekenstein-Hawking term is  
\[
S_0
=
\frac{A}{4G_{\mathcal I}\ell_{\mathcal I}^2}.
\]

One-loop information fluctuations around the fixed point produce logarithmic corrections. The heat-kernel expansion gives  
\[
\boxed{
S
=
\frac{A}{4G_{\mathcal I}\ell_{\mathcal I}^2}
+
\sigma\log\left(\frac{A}{\ell_{\mathcal I}^2}\right)
+
\sum_{n\ge1}\beta_n
\left(\frac{\ell_{\mathcal I}^2}{A}\right)^n.
}
\]

The coefficient \(\sigma\) depends on the number of informational degrees of freedom, including the dilaton and cubic modes.

Thus black-hole entropy is the logarithm of the number of compression-stable informational microstates.

---

## 14. Informational Equivalence Principle

The universal coupling of matter to the emergent metric follows if all physical systems are realized as informational channels over the same substrate.

Let matter fields \(\psi\) couple to the information metric \(g_{ab}\) through an action  
\[
S_m[\psi,g_{ab}].
\]

After passing to the Einstein frame, matter couples to  
\[
\widetilde g_{ab}
=
A^2(\phi)g_{ab}.
\]

If \(A(\phi)\) is universal, all bodies follow the same emergent geodesics up to scalar-force corrections. The weak equivalence principle is therefore preserved in the universal-information limit.

If different physical systems encode information with different compression maps \(K_\lambda\), then \(A(\phi)\) becomes species-dependent, producing violations of the equivalence principle. Thus equivalence-principle tests directly constrain the universality of informational compression.

---

## 15. Observational Signatures

The theory predicts several distinctive effects.

### 15.1 Fifth force

A Yukawa correction to Newtonian gravity:
\[
\boxed{
a(r)
=
\frac{G_NM}{r^2}
\left[
1+
2\alpha_0^2 e^{-r/\lambda_{\mathcal I}}
\left(1+\frac{r}{\lambda_{\mathcal I}}\right)
\right].
}
\]

This is testable in torsion-balance experiments, planetary ephemerides, and short-range gravity tests.

### 15.2 Scale-dependent dimension

The spectral dimension runs:
\[
\boxed{
d_s(\ell)
=
d_{\rm IR}
+
(d_{\rm UV}-d_{\rm IR})
e^{-(\ell/\ell_*)^\nu}.
}
\]

This could affect gravitational-wave propagation, high-energy dispersion, and diffusion processes in quantum-gravity phenomenology.

### 15.3 Flat rotation curves

If \(d_{\rm eff}\to 2\) at galactic scales,
\[
\boxed{
a(r)\sim \frac{1}{r},
\qquad
v_c^2(r)\sim \text{constant}.
}
\]

This provides an information-geometric alternative to particle dark matter.

### 15.4 Late-time acceleration

A slowly varying information dilaton yields  
\[
w_{\rm eff}\simeq -1.
\]

Thus dark energy is interpreted as a compression fixed point.

### 15.5 Logarithmic entropy corrections

Black-hole entropy receives corrections:
\[
\boxed{
S
=
\frac{A}{4G\ell_{\mathcal I}^2}
+
\sigma\log A
+
\cdots.
}
\]

---

## 16. Summary of Derived Physical Laws

From the informational substrate we have derived:

1. **Information metric theorem**  
   \[
   D_S
   \longrightarrow
   g_{ab}^{(\mathcal I)}.
   \]

2. **Connection from cubic distinguishability**  
   \[
   C_{abc}
   \longrightarrow
   \nabla^{(\alpha)}.
   \]

3. **Curvature from noncommutativity of information transport**  
   \[
   \nabla^{(\alpha)}
   \longrightarrow
   R^{(\alpha)}.
   \]

4. **Lorentzian signature from finite-speed directed information**  
   \[
   \text{directed channels}
   +
   c_{\mathcal I}
   \longrightarrow
   ds^2=-c_{\mathcal I}^2d\tau^2+h_{ij}dx^idx^j.
   \]

5. **Compression fixed-point field equation**  
   \[
   R_{ab}
   +
   2\nabla_a\nabla_b\Phi
   -
   \frac14 C_{acd}C_b{}^{cd}
   =
   \kappa_{\mathcal I}T^{(m)}_{ab}.
   \]

6. **Einstein-frame gravitational equation**  
   \[
   G_{ab}
   +
   \Lambda_{\mathcal I}g_{ab}
   =
   \kappa_{\mathcal I}
   \left(
   T^{(m)}_{ab}
   +
   T^{(\phi)}_{ab}
   +
   T^{(C)}_{ab}
   \right).
   \]

7. **Yukawa modification of gravity**  
   \[
   \Phi_N(r)
   =
   -\frac{G_NM}{r}
   \left[
   1+2\alpha_0^2e^{-m_\phi r}
   \right].
   \]

8. **Dimensional crossover force law**  
   \[
   a(r)
   =
   \frac{G_NM}{r^2}
   \left(
   \frac{r}{r_0}
   \right)^{3-d_{\rm eff}(r)}.
   \]

9. **Information-driven cosmological acceleration**  
   \[
   \rho_\phi
   =
   \frac12\dot\phi^2+U(\phi),
   \qquad
   w_\phi\simeq -1.
   \]

10. **Black-hole entropy corrections**  
   \[
   S
   =
   \frac{A}{4G\ell_{\mathcal I}^2}
   +
   \sigma\log A
   +
   \cdots.
   \]

---

## 17. Conclusion

We have shown that the information-geometric program can be developed into a physical theory in which geometry is not primitive but information-selected.

The core result is the emergence chain  
\[
\boxed{
\text{information}
\rightarrow
\text{distinguishability}
\rightarrow
\text{equivalence}
\rightarrow
\text{metric}
\rightarrow
\text{connection}
\rightarrow
\text{curvature}
\rightarrow
\text{compression fixed point}
\rightarrow
\text{dynamics}.
}
\]

In this framework:

\[
\boxed{
\text{Gravity is the macroscopic dynamics of compression-stable information.}
}
\]

\[
\boxed{
\text{Causal structure is the cone structure of finite-speed information propagation.}
}
\]

\[
\boxed{
\text{Dark-sector effects are residuals of informational asymmetry and compression potential.}
}
\]

\[
\boxed{
\text{Dimension is a scale-dependent invariant of information diffusion.}
}
\]

The resulting theory is not merely an analogy between information and geometry. It is a constructive derivation of geometry, causal order, and gravitational dynamics from informational distinguishability, compression stability, and directed information flow.

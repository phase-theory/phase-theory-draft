# Fractional Fermi Sea as a Rational Stable Phase Sector of Universal Phase Theory

**Dust LLC — Universal Phase Theory Preprint**  
**October 2026**

---

## Abstract

A fractional Fermi sea (FFS) is derived here as a stable, finite-density, rational phase sector of Universal Phase Theory (UPT). The primitive datum is again a generalized phase section \(\Phi\in\Gamma(E_\Phi)\) over a non-spatiotemporal base \(\mathcal X\), subject to the universal phase equation

\[
\mathscr F[\Phi;\lambda]=0,
\qquad
\mathscr L_\Phi:=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi:=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi:=\mathscr L_\Phi^{-1}.
\]

No fractional particle, pre-assigned occupation number, Fermi surface, or many-body Hilbert space is inserted at the outset. Starting only from the UPT operator hierarchy, we show that a fractional Fermi sea arises when a finite-density phase branch satisfies four additional structural conditions: (i) the phase stability operator possesses a critical phase band with a finite orbital degeneracy; (ii) the admissible phase-frame group contains a discrete root quotient, producing a rational phase bundle \(L_{p/q}\); (iii) the reduced phase symplectic cell is correspondingly rescaled, yielding a generalized exclusion bound \(0\le n_\alpha\le p/q\); and (iv) phase transport generates a gapless Fermi locus in the emergent response geometry. The resulting state is the gauge-equivalence class

\[
\boxed{
\mathfrak F_{p/q}
=
[\Phi_{p/q}]_{\mathscr G_\Phi},
}
\]

where \(p/q\) is the invariant filling fraction. In the minimal bosonic realization, \(p/q=1/2\), and the translationally invariant one-body density matrix has fractional diagonal occupation

\[
\boxed{
n_\alpha=\frac12
}
\]

for every orbital \(\alpha\) in the active phase band. The object is therefore not a Fermi liquid of elementary fermions, but a compressible, highly excited, stable phase sector in which bosonic phase constituents organize into an orderly finite-density sea with rational occupancy. The derivation establishes the conceptual and mathematical origin of fractional Fermi seas within UPT and provides explicit stability, transport, and falsifiability criteria.

---

## 1. Ontological statement and central result

Universal Phase Theory does not begin with particles, fields, Hilbert spaces, or occupation numbers. It begins with a phase configuration \(\Phi\) and the universal admissibility condition

\[
\mathscr F[\Phi;\lambda]=0.
\]

A particle was previously derived as a stable, localizable, transportable phase-sector orbit

\[
\mathfrak P_q=[\Phi_q]_{\mathscr G_\Phi}.
\]

A fractional Fermi sea is a higher-order phase-sector object. It is not a single localized defect, but a finite-density, compressible, stable sector of the quotient solution space

\[
\mathscr S_\Phi/\mathscr G_\Phi.
\]

The central claim of this paper is:

\[
\boxed{
\text{A fractional Fermi sea is a stable rational phase-sector orbit with fractional phase-cell occupancy.}
}
\]

More precisely, we derive a phase branch \(\Phi_{p/q}\) for which the invariant one-body occupation function in the active phase band is

\[
\boxed{
n_\alpha
=
\frac{p}{q}\,\Theta(\mu-\varepsilon_\alpha),
\qquad
0<\frac{p}{q}\le 1,
}
\tag{1.1}
\]

where \(\varepsilon_\alpha\) are the reduced single-particle phase energies, \(\mu\) is the phase chemical potential, and \(\Theta\) is the occupation step function determined by the reduced phase dynamics. For the minimal half-filled bosonic case,

\[
\boxed{
p=1,\quad q=2,\quad n_\alpha=\frac12.
}
\tag{1.2}
\]

The corresponding Fermi surface is not imposed. It is the emergent locus in phase momentum space where the reduced phase energy equals the chemical potential:

\[
\boxed{
\Sigma_F:
\qquad
g_\Phi^{ij}k_i k_j
=
k_F^2,
}
\tag{1.3}
\]

with \(g_\Phi^{ij}\) the inverse of the UPT response metric. Thus the fractional Fermi sea is a phase-geometric object:

\[
\boxed{
\mathfrak F_{p/q}
=
[\Phi_{p/q}]_{\mathscr G_\Phi}
\in
\mathscr S_\Phi/\mathscr G_\Phi.
}
\tag{1.4}
\]

The derivation proceeds in seven stages:

1. Finite-density criticality of the universal phase equation.  
2. Lyapunov–Schmidt reduction to an active phase band.  
3. Construction of a rational phase-frame bundle.  
4. Derivation of fractional phase-cell volume.  
5. Derivation of a generalized exclusion bound.  
6. Emergence of a Fermi locus from phase transport.  
7. Stability and topological separation of the fractional sea.  

The result is a UPT derivation of the fractional Fermi sea concept, not an analogy with known fermionic systems.

---

## 2. UPT data for finite-density phase sectors

Let

\[
\pi_\Phi:E_\Phi\to\mathcal X
\]

be the universal phase bundle over a generalized base \(\mathcal X\), not assumed to be spacetime. Let \(\mathscr G_\Phi\) be the admissible phase-frame group or groupoid, and let

\[
\mathcal C_\Phi\subseteq\Gamma(E_\Phi)
\]

be the admissible configuration space. A UPT datum is

\[
\mathfrak U
=
(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\lambda),
\tag{2.1}
\]

where

\[
\mathscr F:\mathcal C_\Phi\times\Lambda\to\mathcal Y_\Phi
\]

is the universal admissibility map.

For a finite-density sector, the control data include a phase chemical potential and, where relevant, a background phase curvature:

\[
\lambda
=
(\mu,\mathcal B_\Phi,\ldots).
\tag{2.2}
\]

The universal phase equation is

\[
\boxed{
\mathscr F[\Phi;\lambda]=0.
}
\tag{2.3}
\]

If a variational realization exists,

\[
S_\Phi[\Phi;\lambda]
=
\int_{\mathcal X}
\mathcal L_\Phi
\bigl(\Phi,D\Phi,D^2\Phi,\ldots;\lambda\bigr)
\,d\mu_\Phi,
\tag{2.4}
\]

then

\[
\mathscr F[\Phi;\lambda]
=
\frac{\delta S_\Phi}{\delta\Phi}.
\tag{2.5}
\]

No spatial metric, Fermi surface, or many-body occupation number is assumed in (2.4).

Let \(\Phi_0\) be a stable vacuum phase. A finite-density branch \(\Phi_\rho\) satisfies

\[
\Phi_\rho
\longrightarrow
\Phi_0
\quad
\text{on the phase boundary at infinity},
\tag{2.6}
\]

but carries nonzero conserved phase density

\[
\rho
=
\langle J^0[\Phi_\rho]\rangle.
\tag{2.7}
\]

Before spacetime has emerged, \(J^\mu\) is interpreted as the Noether current of a residual phase-translation symmetry. After the response geometry has produced an effective spacetime \(M_{\rm eff}\), \(J^\mu\) becomes the physical density current.

The UPT response metric is again

\[
\boxed{
g^\Phi_{ij}
=
T_{ia}\chi^{ab}T_{jb},
}
\tag{2.8}
\]

where

\[
\chi^{ab}
=
(S^{-1})^{ab},
\qquad
S_{ab}
=
\frac{\partial^2\mathcal V_{\rm red}}{\partial\eta^a\partial\eta^b},
\qquad
T_{ia}
=
\frac{\partial^2\mathcal V_{\rm red}}{\partial\lambda^i\partial\eta^a}.
\tag{2.9}
\]

The finite-density state is localized or homogeneous with respect to this emergent geometry. The fractional Fermi sea will be constructed on a homogeneous finite-density stratum for which \(g^\Phi_{ij}\) is nondegenerate.

---

## 3. Critical phase band and Lyapunov–Schmidt reduction

A fractional Fermi sea requires a dense family of near-critical phase directions. Let \(\Phi_c\) be a critical vacuum or background phase at control value \(\lambda_c\), with stability operator

\[
\mathscr L_{\Phi_c}
=
D_\Phi\mathscr F[\Phi_c;\lambda_c].
\tag{3.1}
\]

Assume that the critical kernel is not merely finite-dimensional but forms an active phase band:

\[
K_c
=
\ker\mathscr L_{\Phi_c}.
\tag{3.2}
\]

In a finite effective spatial volume, let the band contain \(N_\phi\) nearly degenerate modes. We write

\[
K_c
=
\operatorname{span}\{u_\alpha\}_{\alpha=1}^{N_\phi}.
\tag{3.3}
\]

The complement is \(R_c\), so that

\[
\mathcal T_{\Phi_c}\mathcal C_\Phi
=
K_c\oplus R_c.
\tag{3.4}
\]

A phase configuration near \(\Phi_c\) decomposes as

\[
\Phi
=
\Phi_c
+
\sum_{\alpha=1}^{N_\phi}
z^\alpha u_\alpha
+
\xi,
\qquad
\xi\in R_c.
\tag{3.5}
\]

The range equation

\[
P_R\mathscr F[\Phi_c+z^\alpha u_\alpha+\xi;\lambda]=0
\tag{3.6}
\]

has a local solution

\[
\xi=\xi(z,\lambda),
\tag{3.7}
\]

provided the restricted linearization on \(R_c\) is invertible. The residual equation is the reduced universal phase equation

\[
\boxed{
\varphi^\alpha(z,\lambda)
=
\left\langle
u^{*\alpha},
\mathscr F
\left[
\Phi_c
+
z^\beta u_\beta
+
\xi(z,\lambda);
\lambda
\right]
\right\rangle
=
0.
}
\tag{3.8}
\]

For a finite-density sector, the relevant order parameter is not a single condensate amplitude. The active band is macroscopically occupied, and the reduced variables are the collective occupation data of the band. The appropriate reduced object is therefore a phase occupation operator

\[
\widehat n
:
K_c\to K_c,
\tag{3.9}
\]

rather than a single complex vector \(z^\alpha\). In a basis \(\{u_\alpha\}\),

\[
\widehat n_{\alpha\beta}
=
\left\langle
u_\alpha,
\widehat n\,u_\beta
\right\rangle.
\tag{3.10}
\]

The reduced phase potential becomes a functional

\[
\mathcal V_{\rm red}
=
\mathcal V_{\rm red}[\widehat n;\lambda].
\tag{3.11}
\]

This is the UPT analog of a many-body reduction: it is not imposed by second quantization, but forced by the structure of the critical kernel of \(\mathscr L_\Phi\).

---

## 4. Rational phase-frame bundles and fractional filling

The decisive step is the derivation of rational occupation from phase-frame topology.

Let the active critical band define a derived phase line bundle

\[
L\to \Sigma,
\tag{4.1}
\]

where \(\Sigma\) is the emergent spatial slice produced by the response geometry. Let \(A=\mathcal A[\Phi]\) be the UPT-derived phase connection, with curvature

\[
F=dA.
\tag{4.2}
\]

The number of active phase orbitals is the Chern number

\[
\boxed{
N_\phi
=
c_1(L)
=
\frac{1}{2\pi}
\int_\Sigma F.
}
\tag{4.3}
\]

In ordinary U(1) phase theory, each orbital contributes one available phase cell. Fractionality arises when the admissible phase-frame group is not simply \(U(1)\), but contains a discrete quotient.

Assume that the phase-frame group contains a central discrete identification

\[
\mathbb Z_q
\subset
U(1),
\tag{4.4}
\]

so that admissible phase frames are identified under

\[
\theta
\sim
\theta+\frac{2\pi}{q}.
\tag{4.5}
\]

The physical phase-frame group is therefore effectively

\[
\mathscr G_{\rm phase}
=
U(1)/\mathbb Z_q.
\tag{4.6}
\]

This quotient permits rational phase bundles. Define a \((p,q)\) phase-root bundle \(L_{p/q}\) by the relation

\[
\boxed{
L_{p/q}^{\otimes q}
\cong
L^{\otimes p}.
}
\tag{4.7}
\]

Formally,

\[
L_{p/q}
=
L^{p/q}.
\tag{4.8}
\]

Its curvature is

\[
\boxed{
F_{p/q}
=
\frac{p}{q}F.
}
\tag{4.9}
\]

The associated phase charge is

\[
\boxed{
Q_{p/q}
=
\frac{1}{2\pi}
\int_\Sigma F_{p/q}
=
\frac{p}{q}
\frac{1}{2\pi}
\int_\Sigma F.
}
\tag{4.10}
\]

Therefore

\[
\boxed{
Q_{p/q}
=
\frac{p}{q}N_\phi.
}
\tag{4.11}
\]

The invariant filling fraction is

\[
\boxed{
\nu
=
\frac{Q_{p/q}}{N_\phi}
=
\frac{p}{q}.
}
\tag{4.12}
\]

This is the first central derivation: fractional filling is not an externally chosen occupation number. It is the rational characteristic class of a phase-root bundle permitted by the discrete phase-frame quotient.

### Proposition 1: Rational filling from phase-frame quotient

Let \(L\) be the active phase bundle with \(c_1(L)=N_\phi\), and let the admissible phase-frame group admit a \(\mathbb Z_q\) root structure. Then an admissible \((p,q)\) phase sector has filling fraction

\[
\nu=\frac{p}{q}.
\]

**Proof.** By definition of the root bundle \(L_{p/q}\),

\[
q\,c_1(L_{p/q})
=
p\,c_1(L)
=
pN_\phi.
\]

Thus

\[
c_1(L_{p/q})
=
\frac{p}{q}N_\phi.
\]

The UPT phase charge is the integral of the root curvature, hence

\[
Q_{p/q}
=
c_1(L_{p/q})
=
\frac{p}{q}N_\phi.
\]

Dividing by the orbital degeneracy \(N_\phi\) gives \(\nu=p/q\). \(\square\)

For finite systems, global admissibility may require \(q\mid pN_\phi\) or the inclusion of appropriate boundary defects. In the thermodynamic limit, the rational filling \(\nu=p/q\) is well-defined as an intensive phase-sector invariant.

---

## 5. Fractional phase cells and generalized exclusion

The rational bundle modifies the phase-space cell volume. Let \(\Omega_0\) be the ordinary one-particle phase symplectic form associated with \(L\). The root bundle \(L_{p/q}\) carries the rescaled symplectic form

\[
\boxed{
\Omega_{p/q}
=
\frac{p}{q}\Omega_0.
}
\tag{5.1}
\]

The number of available phase cells is therefore

\[
\boxed{
N_{p/q}
=
\frac{1}{2\pi\hbar_\Phi}
\int_{\Sigma_{\rm phase}}
\Omega_{p/q}
=
\frac{p}{q}N_0.
}
\tag{5.2}
\]

Equivalently, the effective phase quantum is rescaled:

\[
\boxed{
\hbar_{\Phi;p/q}
=
\frac{q}{p}\hbar_\Phi.
}
\tag{5.3}
\]

Thus the root sector has fewer independent phase cells than the original bosonic phase band by the factor \(p/q\). This is the geometric origin of fractional exclusion.

Let \(G\) be the number of one-particle orbitals in the original active band. The UPT root structure implies that the effective number of available states after admitting \(N\) phase excitations is

\[
\boxed{
d_N
=
G
-
g(N-1),
\qquad
g=\frac{q}{p}.
}
\tag{5.4}
\]

Equation (5.4) is the UPT derivation of a generalized Pauli principle. For \(p=q\), one has \(g=1\), recovering ordinary fermionic exclusion. For \(p/q=1/2\), one has \(g=2\): each added excitation removes two original orbital degrees of freedom from the available phase space. The maximal admissible density satisfies

\[
d_N\ge 0
\quad
\Longrightarrow
\quad
\frac{N}{G}
\le
\frac{p}{q}.
\tag{5.5}
\]

Therefore the maximum occupation per original orbital is

\[
\boxed{
n_{\max}
=
\frac{p}{q}.
}
\tag{5.6}
\]

This is not a statistical average imposed by hand. It is a consequence of the reduced phase-cell volume of the root bundle.

The translationally invariant one-body density operator of a saturated fractional sea is therefore

\[
\boxed{
\widehat n_{\rm FFS}
=
\frac{p}{q}\,\Pi_0,
}
\tag{5.7}
\]

where \(\Pi_0\) is the projector onto the active phase band. For any normalized orbital \(u_\alpha\) in that band,

\[
\boxed{
n_\alpha
=
\langle u_\alpha|\widehat n_{\rm FFS}|u_\alpha\rangle
=
\frac{p}{q}.
}
\tag{5.8}
\]

In the minimal case,

\[
\boxed{
n_\alpha=\frac12.
}
\tag{5.9}
\]

This is the precise UPT meaning of a quantum state being fractionally filled.

---

## 6. Emergence of the fractional Fermi sea

A fractional occupation bound alone does not produce a Fermi sea. One must also derive a gapless Fermi locus. This follows from phase transport on the reduced branch.

The quadratic part of the reduced phase action defines an effective single-particle phase Hamiltonian on the active band:

\[
\boxed{
h_{\alpha\beta}
=
\left\langle
u_\alpha,
\mathscr L_{\Phi_c}
u_\beta
\right\rangle_\Phi.
}
\tag{6.1}
\]

In an emergent affine chart with response metric \(g^\Phi_{ij}\), the low-energy symbol of \(h\) is

\[
\boxed{
\varepsilon(k)
=
\frac{1}{2m_\Phi}
g_\Phi^{ij}
\left(k_i-A_i^{\rm eff}\right)
\left(k_j-A_j^{\rm eff}\right)
-
\mu
+
\cdots,
}
\tag{6.2}
\]

where \(A_i^{\rm eff}\) is the effective phase connection seen by the reduced collective modes.

The occupation function of the saturated fractional sea is

\[
\boxed{
n(k)
=
\frac{p}{q}
\Theta\bigl(\mu-\varepsilon(k)\bigr).
}
\tag{6.3}
\]

The Fermi surface is the boundary of the occupied region:

\[
\boxed{
\Sigma_F:
\qquad
\varepsilon(k)=\mu.
}
\tag{6.4}
\]

For a locally isotropic phase geometry,

\[
\boxed{
g_\Phi^{ij}k_i k_j
=
k_F^2.
}
\tag{6.5}
\]

Thus the fractional Fermi sea is a filled phase-space region with fractional height \(p/q\). In \(d\) spatial dimensions, the density satisfies

\[
\boxed{
\rho
=
\frac{p}{q}
\int_{\varepsilon(k)<\mu}
\frac{d^d k}{(2\pi)^d}.
}
\tag{6.6}
\]

For \(d=2\),

\[
\boxed{
\rho
=
\frac{p}{q}
\frac{k_F^2}{4\pi}.
}
\tag{6.7}
\]

Equivalently,

\[
\boxed{
k_F^2
=
\frac{4\pi q}{p}\rho.
}
\tag{6.8}
\]

For the half-filled case \(p/q=1/2\),

\[
\boxed{
\rho
=
\frac12
\frac{k_F^2}{4\pi},
\qquad
k_F^2
=
8\pi\rho.
}
\tag{6.9}
\]

This is the UPT modification of the usual Fermi-surface counting law: the Fermi volume is multiplied by the rational phase-sector invariant \(\nu=p/q\).

---

## 7. Phase vortices, statistical transmutation, and bosonic realization

The derivation above does not require the underlying phase field to be fermionic. The primitive field \(\Phi\) may be bosonic, meaning that its elementary exchange holonomy is initially trivial. Fractional exclusion arises from the phase-frame quotient and the root bundle, not from an elementary fermionic anticommutation relation inserted at the start.

In \(2+1\) effective dimensions, the same rational structure may be represented through phase vortices and an emergent statistical connection. Let \(a_\mu\) be the statistical phase connection derived from phase transport. The finite-density branch satisfies the UPT topological constraint

\[
\boxed{
\rho
=
\frac{p}{2\pi q}
\epsilon^{ij}F_{ij}[A],
}
\tag{7.1}
\]

where \(A\) is the external or background phase curvature coupling to the conserved phase charge. Equivalently, the effective curvature seen by the reduced collective modes is

\[
\boxed{
F_{\rm eff}
=
F
-
\frac{2\pi q}{p}\rho.
}
\tag{7.2}
\]

The fractional sea condition is

\[
\boxed{
F_{\rm eff}=0.
}
\tag{7.3}
\]

Using (7.1),

\[
F_{\rm eff}
=
F
-
\frac{2\pi q}{p}
\left(
\frac{p}{2\pi q}F
\right)
=
0.
\tag{7.4}
\]

Thus the rational filling condition is simultaneously the condition for vanishing effective phase curvature. In the half-filled bosonic case,

\[
\rho
=
\frac{1}{4\pi}F,
\qquad
F_{\rm eff}=0.
\tag{7.5}
\]

The collective modes then propagate as if they are in zero effective curvature, producing a compressible sea rather than a gapped topological liquid.

The exchange holonomy of the collective modes is derived from phase transport. For a closed exchange loop \(\gamma_{\rm ex}\) in the two-particle moduli space,

\[
\boxed{
\mathscr U_{\rm ex}
=
\mathcal P
\exp
\left(
-\oint_{\gamma_{\rm ex}}
\mathscr A[\Phi]
\right).
}
\tag{7.6}
\]

If the residual stabilizer representation satisfies

\[
\boxed{
\mathscr U_{\rm ex}=-1,
}
\tag{7.7}
\]

the collective branch obeys fermionic exclusion. In the rational root sector, this fermionic holonomy may coexist with fractional filling because the one-particle phase-cell volume has already been reduced by \(p/q\). Thus bosonic phase constituents can generate an effective Fermi sea without elementary fermions being inserted into \(\mathscr F\).

The minimal bosonic fractional Fermi sea therefore has the following structure:

\[
\boxed{
\text{bosonic phase constituents}
\;
+
\;
\mathbb Z_2\text{ phase-frame quotient}
\;
\longrightarrow
\;
n_\alpha=\frac12
\;
+
\;
\text{Fermi locus}.
}
\tag{7.8}
\]

---

## 8. Reduced variational equation for the fractional sea

The reduced phase potential may be written as a functional of the occupation operator \(\widehat n\):

\[
\boxed{
\mathcal V_{\rm red}[\widehat n;\mu]
=
\operatorname{Tr}
\bigl[
(\widehat h-\mu\widehat I)\widehat n
\bigr]
+
\frac12
\operatorname{Tr}
\bigl[
\widehat V
(\widehat n\otimes\widehat n)
\bigr]
+
\cdots,
}
\tag{8.1}
\]

subject to the UPT exclusion constraint

\[
\boxed{
0
\le
\widehat n
\le
\frac{p}{q}\widehat I.
}
\tag{8.2}
\]

The stationarity condition is

\[
\boxed{
\frac{\delta\mathcal V_{\rm red}}{\delta\widehat n}
=
0
\quad
\text{on admissible variations}.
}
\tag{8.3}
\]

For a translationally invariant branch with a flat or nearly flat active band, the interaction tensor \(\widehat V\) is minimized by a homogeneous occupation operator. Hence

\[
\widehat n_{\rm FFS}
=
\frac{p}{q}\Pi_0.
\tag{8.4}
\]

If the single-particle symbol \(\varepsilon(k)\) is dispersive, the solution becomes

\[
\boxed{
\widehat n_{\rm FFS}
=
\frac{p}{q}
\Theta(\mu-\widehat h).
}
\tag{8.5}
\]

Equation (8.5) is the reduced UPT equation for the fractional Fermi sea. It is the finite-density analog of the particle emergence condition: the sea is a solution of the reduced universal phase equation on the critical band.

---

## 9. Fractional Fermi Sea Emergence Theorem

We can now state the central theorem.

### Theorem 1: Fractional Fermi Sea emergence

Let \(\mathfrak U=(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\lambda)\) be a UPT datum. Suppose there exists a finite-density phase branch \(\Phi_{p/q}\) such that:

1. **Admissibility**  
   \[
   \mathscr F[\Phi_{p/q};\lambda]=0.
   \]

2. **Critical active band**  
   The stability operator \(\mathscr L_{\Phi_c}\) possesses an active phase band \(K_c\) with orbital degeneracy \(N_\phi\).

3. **Rational phase-frame quotient**  
   The phase-frame group admits a discrete root structure \(L_{p/q}\) satisfying  
   \[
   L_{p/q}^{\otimes q}\cong L^{\otimes p}.
   \]

4. **Fractional phase-cell exclusion**  
   The reduced symplectic cell implies  
   \[
   0\le n_\alpha\le \frac{p}{q}.
   \]

5. **Finite density**  
   The branch carries nonzero conserved phase density  
   \[
   \rho>0.
   \]

6. **Gapless Fermi locus**  
   The reduced Hamiltonian has a nonempty solution set  
   \[
   \varepsilon(k)=\mu,
   \]
   defining a codimension-one Fermi surface in the emergent momentum geometry.

7. **Normal stability**  
   The projected stability operator satisfies  
   \[
   \langle\zeta,\mathscr L_{p/q}^{\perp}\zeta\rangle_\Phi
   \ge
   \kappa
   \|\zeta\|_\Phi^2,
   \qquad
   \kappa>0,
   \]
   for all perturbations orthogonal to gauge directions, collective translations, and neutral Fermi-surface particle-hole zero modes.

Then the orbit

\[
\boxed{
\mathfrak F_{p/q}
=
[\Phi_{p/q}]_{\mathscr G_\Phi}
}
\tag{9.1}
\]

is a fractional Fermi sea: a stable, compressible, finite-density phase-sector object with invariant occupation

\[
\boxed{
n_\alpha
=
\frac{p}{q}
\Theta(\mu-\varepsilon_\alpha).
}
\tag{9.2}
\]

### Proof

Condition 1 makes \(\Phi_{p/q}\) an admissible UPT configuration. Condition 2 provides the active band in which a finite-density sea can form. Condition 3 implies, by Proposition 1, that the phase charge and orbital degeneracy satisfy

\[
Q_{p/q}
=
\frac{p}{q}N_\phi.
\]

Condition 4 follows from the rescaled phase-cell volume and gives the maximal occupation \(p/q\). Condition 5 ensures that the branch is nonvacuum and finite-density. Condition 6 supplies a gapless boundary between occupied and unoccupied reduced phase modes, which is the Fermi surface. Condition 7 ensures that the branch is stable against local perturbations except for the required neutral Fermi-surface deformations. Modding out by \(\mathscr G_\Phi\) removes phase-frame redundancy. The resulting orbit is therefore a stable finite-density phase sector with rational occupation and a Fermi locus. \(\square\)

---

## 10. Stability, excess action, and topological protection

A fractional Fermi sea is highly excited relative to the zero-density vacuum. Its excess phase energy density is

\[
\boxed{
\epsilon_{\rm FFS}
=
\frac{
\mathcal E[\Phi_{p/q}]
-
\mathcal E[\Phi_0]
}{
\operatorname{Vol}(\Sigma)
}.
}
\tag{10.1}
\]

For a stable finite-density sector,

\[
\boxed{
0
<
\epsilon_{\rm FFS}
<
\infty.
}
\tag{10.2}
\]

The state is not protected by a single localized topological charge, as a soliton would be. It is protected by a combination of:

1. **Charge conservation**  
   \[
   Q_{p/q}
   =
   \frac{p}{q}N_\phi
   \]
   cannot change without altering the phase density or boundary flux.

2. **Rational phase-frame class**  
   The root bundle \(L_{p/q}\) defines a distinct equivariant phase sector.

3. **Fermi-surface kinematics**  
   Low-energy particle-hole excitations are confined to the Fermi locus.

4. **Normal coercivity**  
   Perturbations away from the Fermi locus are restored by the positive projected stability operator.

The topological separation statement is:

### Proposition 2: Sector separation

Let \(\Phi_0\) be the vacuum phase and \(\Phi_{p/q}\) a finite-density fractional sea with \(p/q\neq 0\). If the path of configurations is required to preserve the phase-frame quotient, conserved phase density, and boundary flux class, then there is no continuous admissible path from \(\Phi_{p/q}\) to \(\Phi_0\).

**Proof.** A continuous admissible path would preserve the rational phase class \(L_{p/q}\) and the conserved density. Since \(\Phi_0\) has \(Q=0\) and trivial root class, while \(\Phi_{p/q}\) has \(Q_{p/q}=(p/q)N_\phi\), the path would have to cross a non-admissible configuration or change the phase-frame quotient. Therefore the sectors are separated. \(\square\)

Thus the fractional Fermi sea is a distinct phase sector, not a perturbative excitation of the vacuum.

---

## 11. Effective action and collective dynamics

Once the emergent spacetime geometry has been established, the low-energy effective action of the fractional Fermi sea can be written in UPT-derived variables. Let \(f\) denote the collective phase mode that fills the root band. Its effective action is

\[
\boxed{
S_{\rm FFS}
=
\int dt\,d^d x\,
\sqrt{g_\Phi}
\left[
f^\dagger
\left(
iD_t
+
\mu
+
\frac{1}{2m_\Phi}
g_\Phi^{ij}D_iD_j
\right)
f
\right]
+
S_{\rm top}
+
S_{\rm int}.
}
\tag{11.1}
\]

Here

\[
D_\mu
=
\partial_\mu
+
i a_\mu,
\tag{11.2}
\]

where \(a_\mu\) is the UPT-derived statistical phase connection. The topological constraint is

\[
\boxed{
\rho
-
\frac{p}{2\pi q}
\epsilon^{ij}F_{ij}[A]
=
0.
}
\tag{11.3}
\]

In a Lagrange-multiplier representation,

\[
S_{\rm top}
=
\int dt\,d^2x\,
a_0
\left(
\rho
-
\frac{p}{2\pi q}B
\right)
+
\cdots,
\tag{11.4}
\]

where

\[
B=\epsilon^{ij}\partial_i A_j.
\tag{11.5}
\]

The interaction action \(S_{\rm int}\) contains projected phase interactions on the Fermi surface. Stability requires that the projected quartic tensor have no negative pairing eigenvalue. If a pairing channel becomes attractive, the fractional Fermi sea becomes unstable toward a paired rational phase sector. This is the UPT analog of a BCS instability, but derived from the reduced phase potential rather than assumed.

The collective moduli of the Fermi surface are smooth deformations

\[
k_F
\to
k_F+\delta k_F(\theta),
\tag{11.6}
\]

with an induced phase kinetic tensor on the space of deformations. The resulting dynamics is a phase-geometric analog of Fermi-surface hydrodynamics.

---

## 12. Response functions and observable consequences

The fractional Fermi sea produces several distinctive consequences.

### 12.1 Fractional occupation plateau

The most direct signature is the occupation function

\[
\boxed{
n(k)
=
\frac{p}{q}
\Theta(k_F-|k|_\Phi).
}
\tag{12.1}
\]

For the minimal bosonic state,

\[
\boxed{
n(k)=\frac12
}
\tag{12.2}
\]

inside the Fermi sea. This is not a thermal mixture and not a disorder average. It is a sector-level invariant of the rational phase bundle.

### 12.2 Modified Luttinger count

The density is related to the Fermi volume by

\[
\boxed{
\rho
=
\frac{p}{q}
\frac{S_{d-1}}{d(2\pi)^d}
k_F^d.
}
\tag{12.3}
\]

In two dimensions,

\[
\boxed{
\rho
=
\frac{p}{q}
\frac{k_F^2}{4\pi}.
}
\tag{12.4}
\]

Thus the Fermi volume is reduced or enlarged by the rational invariant \(p/q\). For \(p/q=1/2\), the Fermi area at fixed density is twice that of an ordinary spinless Fermi sea with the same density.

### 12.3 Compressibility

For a parabolic phase dispersion in two dimensions,

\[
\varepsilon(k)
=
\frac{g_\Phi^{ij}k_i k_j}{2m_\Phi},
\tag{12.5}
\]

the compressibility is

\[
\boxed{
\kappa
=
\frac{\partial\rho}{\partial\mu}
=
\frac{p}{q}
\frac{m_\Phi}{2\pi}.
}
\tag{12.6}
\]

For the half-filled state,

\[
\boxed{
\kappa
=
\frac12
\frac{m_\Phi}{2\pi}.
}
\tag{12.7}
\]

The factor \(p/q\) is a direct observable of the fractional phase-cell volume.

### 12.4 Phase Berry holonomy

A quasiparticle transported around a closed loop in the Fermi-surface moduli space acquires a UPT Berry phase

\[
\boxed{
\gamma_{\rm FFS}
=
2\pi\frac{p}{q}
\mod 2\pi,
}
\tag{12.8}
\]

up to metric and interaction corrections. For \(p/q=1/2\), the fundamental sector holonomy is \(\pi\).

### 12.5 Instability to paired rational phases

If the projected interaction tensor develops a negative pairing eigenvalue, the Fermi surface is unstable. The descendant phase is a gapped rational phase sector. In that case, the effective topological response may become

\[
\boxed{
\sigma_{xy}^{\Phi}
=
\frac{p}{q}
\frac{e_\Phi^2}{h_\Phi},
}
\tag{12.9}
\]

where \(e_\Phi\) and \(h_\Phi\) are emergent phase charge and action units. Thus a gapped descendant of the FFS can exhibit fractional topological transport.

---

## 13. Relation to ordinary Fermi seas and fractional quantum liquids

The fractional Fermi sea is distinct from three familiar classes of states.

### 13.1 Ordinary Fermi sea

An ordinary spinless Fermi sea has

\[
\frac{p}{q}=1,
\qquad
n(k)=\Theta(k_F-|k|).
\]

The UPT fractional Fermi sea replaces the unit occupation by a rational phase-sector invariant:

\[
n(k)=\frac{p}{q}\Theta(k_F-|k|).
\]

Thus the Fermi surface remains, but the phase-cell count is fractional.

### 13.2 Fractional quantum Hall liquids

Fractional quantum Hall states are typically gapped, incompressible, and topologically ordered. The FFS derived here is compressible and possesses a Fermi locus. If interactions gap the Fermi surface, the FFS may flow to a fractional topological phase, but the primary FFS itself is gapless.

### 13.3 Fermionized bosons

The FFS may involve bosonic underlying phase constituents. The effective exclusion is not inserted as elementary fermionic anticommutation. It is derived from the rational phase-frame quotient and the rescaled phase-cell volume. The theory therefore permits bosonic microscopic degrees of freedom to form a Fermi-sea-like phase sector.

---

## 14. Necessary non-insertions

The derivation is meaningful only if the fractional Fermi sea is not smuggled into the universal phase equation. The following audit is required.

| Structure | May not be inserted | Required UPT derivation |
|---|---|---|
| Fractional occupation | Fixed \(n_\alpha=1/2\) | Root phase bundle and phase-cell reduction |
| Fermi surface | Primitive momentum-space cutoff | Critical phase band and response geometry |
| Fermionic statistics | Elementary anticommutators | Phase holonomy and generalized exclusion |
| Density | Arbitrary filling parameter | Conserved phase charge and rational curvature relation |
| Effective metric | Background spatial metric | Susceptibility metric \(g^\Phi_{ij}\) |
| Statistical gauge field | External Chern–Simons field | Phase transport \(A_\mu=\mathcal A_\mu[\Phi]\) |
| Fractional response | Assumed Hall conductivity | Phase curvature and root bundle characteristic class |

A construction that places a fractional occupation number, Fermi momentum, or fermionic Fock space directly into \(\mathscr F\) does not derive a fractional Fermi sea from UPT. It merely rewrites the target phenomenon.

---

## 15. Falsifiability criteria

A concrete UPT realization of the fractional Fermi sea must satisfy the following tests.

### Criterion A — Explicit phase equation

There must exist an explicit \(\mathscr F[\Phi;\lambda]\) whose finite-density solutions include a branch \(\Phi_{p/q}\).

### Criterion B — Root bundle derivation

The rational bundle \(L_{p/q}\) must arise from the phase-frame group, not be imposed as an external mathematical decoration.

### Criterion C — Fractional cell count

The reduced symplectic volume must yield

\[
N_{p/q}
=
\frac{p}{q}N_0.
\]

### Criterion D — Occupation function

The reduced phase equation must produce

\[
n(k)
=
\frac{p}{q}
\Theta(\mu-\varepsilon(k)).
\]

### Criterion E — Fermi-surface stability

The projected stability operator must have no negative modes except possible pairing instabilities, and the Fermi-surface zero modes must be neutral.

### Criterion F — Observable relation

The theory must predict at least one quantitative relation not present in ordinary Fermi-liquid theory, such as

\[
\boxed{
\kappa
=
\frac{p}{q}
\frac{m_\Phi}{2\pi}
}
\]

in the two-dimensional parabolic regime, or the holonomy-occupation relation

\[
\boxed{
n
=
\frac{1}{2\pi}
\arg\mathscr U_{\rm cell}.
}
\]

Failure to derive these structures from a specified \(\mathscr F\) falsifies that particular UPT realization as a theory of fractional Fermi seas.

---

## 16. Minimal half-filled bosonic realization

The simplest nontrivial realization is

\[
p=1,
\qquad
q=2.
\]

The phase-frame group contains a \(\mathbb Z_2\) identification,

\[
\theta\sim\theta+\pi.
\]

The root bundle satisfies

\[
L_{1/2}^{\otimes 2}
\cong
L.
\]

The phase charge is

\[
Q_{1/2}
=
\frac12 N_\phi.
\]

The exclusion bound is

\[
0\le n_\alpha\le\frac12.
\]

The occupation function is

\[
\boxed{
n(k)
=
\frac12
\Theta(k_F-|k|_\Phi).
}
\tag{16.1}
\]

The density satisfies

\[
\boxed{
\rho
=
\frac12
\frac{k_F^2}{4\pi}.
}
\tag{16.2}
\]

The compressibility is

\[
\boxed{
\kappa
=
\frac12
\frac{m_\Phi}{2\pi}.
}
\tag{16.3}
\]

The sector holonomy is

\[
\boxed{
\gamma_{\rm FFS}
=
\pi
\mod 2\pi.
}
\tag{16.4}
\]

Thus the minimal bosonic fractional Fermi sea is the UPT phase sector

\[
\boxed{
\mathfrak F_{1/2}
=
[\Phi_{1/2}]_{\mathscr G_\Phi}.
}
\tag{16.5}
\]

This is the rigorous UPT formulation of the statement that each quantum state in the active band is half-filled.

---

## 17. Conclusion

The fractional Fermi sea has been derived as a rational stable phase sector of Universal Phase Theory. The primitive statement remains

\[
\boxed{
\mathscr F[\Phi;\lambda]=0.
}
\]

A fractional Fermi sea appears only when the universal phase equation admits a finite-density branch whose critical kernel forms an active phase band, whose phase-frame group admits a rational root bundle, whose reduced phase-cell volume produces a generalized exclusion bound, and whose phase transport produces a gapless Fermi locus.

The resulting object is

\[
\boxed{
\mathfrak F_{p/q}
=
[\Phi_{p/q}]_{\mathscr G_\Phi}
\in
\mathscr S_\Phi/\mathscr G_\Phi,
}
\]

with invariant occupation

\[
\boxed{
n_\alpha
=
\frac{p}{q}
\Theta(\mu-\varepsilon_\alpha).
}
\]

For the minimal bosonic case,

\[
\boxed{
n_\alpha=\frac12.
}
\]

Thus the fractional Fermi sea is not a sea of primitive fractional particles. It is the stable, compressible, finite-density organization of a universal phase substrate into a rational phase-sector orbit. Fractional occupation is topology. The Fermi surface is phase geometry. Stability is phase coercivity. The many-body state is a quotient solution of the universal phase equation.

The next required step is explicit model construction: specify \(\mathscr F\), solve for \(\Phi_{p/q}\), compute the root bundle \(L_{p/q}\), verify the projected stability spectrum, and derive the observable response functions without inserting the fractional Fermi sea by hand. That is the point at which the UPT derivation becomes either a predictive theory of fractional quantum matter or is excluded.

---

## References

[1] *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, supplied manuscript, August 2026.

[2] *The Particle as a Stable Phase Sector: A Derivation from the Universal Phase Equation, Topological Separation, and Phase Transport*, supplied manuscript, August 2026.

[3] S. Guo and J. Wu, “Lyapunov–Schmidt Reduction,” in *Bifurcation Theory of Functional Differential Equations*, Applied Mathematical Sciences 184, 119–151 (2013).

[4] F. D. M. Haldane, “Fractional statistics in arbitrary dimensions: A generalization of the Pauli principle and the statistical mechanics of ideal gases,” *Physical Review Letters* **66**, 1529 (1991).

[5] F. Wilczek, “Quantum Mechanics of Fractional-Spin Particles,” *Physical Review Letters* **49**, 957 (1982).

[6] R. B. Laughlin, “Anomalous Quantum Hall Effect: An Incompressible Quantum Fluid with Fractionally Charged Excitations,” *Physical Review Letters* **50**, 1395 (1983).

[7] J. K. Jain, “Composite-fermion approach for the fractional quantum Hall effect,” *Physical Review Letters* **63**, 199 (1989).

[8] B. I. Halperin, P. A. Lee, and N. Read, “Theory of the half-filled Landau level,” *Physical Review B* **47**, 7312 (1993).

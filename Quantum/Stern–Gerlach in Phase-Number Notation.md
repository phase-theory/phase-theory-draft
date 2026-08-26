# Stern–Gerlach in Phase-Number Notation

**A reformulation of the spin-\(\tfrac12\) Stern–Gerlach derivation without a free-standing imaginary-unit symbol**  
**Based on the phase-number calculus supplied by Marlon Hanks**  
**26 August 2026**

## Abstract

This note rewrites the standard spin-\(\tfrac12\) Stern–Gerlach analysis using **phase numbers**—globally defined elements of \(U(1)\)—rather than writing scalar phases with a free-standing imaginary-unit symbol. The replacement is not a new dynamical theory and does not alter any prediction. Its benefit is conceptual: every scalar factor of modulus one is explicitly treated as a phase number, and the observable content of a relative phase is displayed as a gauge-invariant quotient of two phase numbers.

The inhomogeneous magnetic field couples the spin magnetic moment to a spatial degree of freedom. The two eigenprojectors of spin along the analyser axis correlate with two separated wave packets, producing the two outgoing beams. The probabilities follow from projector norms and are independent of the phase number for a one-channel spin measurement. The phase number becomes observable when coherent alternatives are recombined: the output depends on the relative phase number, not on either arm’s phase coordinate.

> **Central result.** For an input state prepared as spin-up along \(\mathbf m\), an ideal Stern–Gerlach analyser along \(\mathbf n\) gives
> \[
> \Pr(+\mathbf n\mid+\mathbf m)=\frac{1+\mathbf m\!\cdot\!\mathbf n}{2},
> \qquad
> \Pr(-\mathbf n\mid+\mathbf m)=\frac{1-\mathbf m\!\cdot\!\mathbf n}{2}.
> \]
> No scalar imaginary-unit notation is needed in this expression or in the spinor/projector derivation below.

## 1. What “using phase numbers instead” can mean precisely

Let

\[
\mathbb T=U(1),\qquad
\operatorname{Exp}(\alpha)\in\mathbb T,
\qquad
\operatorname{Exp}(\alpha+\beta)=\operatorname{Exp}(\alpha)\operatorname{Exp}(\beta).
\]

Here \(\operatorname{Exp}(\alpha)\) is the **phase number** associated with the angular class \(\alpha\pmod {2\pi}\). Its inverse and conjugate coincide:

\[
\overline{\operatorname{Exp}(\alpha)}
=\operatorname{Exp}(-\alpha)
=\operatorname{Exp}(\alpha)^{-1}.
\tag{1}
\]

A nonzero quantum amplitude is written intrinsically in polar form,

\[
A=r\,u,\qquad r\ge 0,\quad u\in\mathbb T,
\tag{2}
\]

rather than as a magnitude multiplied by an exponential containing an imaginary-unit symbol. Conjugation gives \(\overline A=r\,u^{-1}\), so that

\[
|A|^2=A\overline A=r^2.
\tag{3}
\]

This notation should be interpreted carefully. A theory with interference needs an ambient two-real-dimensional scalar algebra because amplitudes must be **added**, not merely multiplied. The phase-number framework does not claim that \(U(1)\) alone is closed under addition; in general \(u+v\notin U(1)\). Instead, it identifies the unit-modulus factor of every nonzero amplitude as the primary global phase object. One may coordinatize the ambient scalar plane by choosing the quarter-turn phase number \(\operatorname{Exp}(\pi/2)\), but no such coordinate is needed in the main derivation.

| Conventional role | Phase-number formulation | Invariant content |
| --- | --- | --- |
| Unit-modulus exponential factor | \(\operatorname{Exp}(\alpha)\in U(1)\) | A globally defined phase number |
| Conjugate phase | \(\operatorname{Exp}(-\alpha)\) | Group inverse |
| Amplitude phase | \(A=|A|\operatorname{ph}(A)\) | \(\operatorname{ph}(A)=A/|A|\) |
| Common phase on a ket | \(w\lvert\psi\rangle\), \(w\in U(1)\) | No change of the physical ray |
| Relative phase of two amplitudes | \(u_1\overline{u_2}\) | Gauge-invariant phase number |

The Stern–Gerlach effect requires two distinct structures. The first is the scalar phase group \(U(1)\), which controls amplitude phases. The second is the two-dimensional spin state space and its noncommuting spin observables. The latter cannot be reduced to a single scalar phase number: rotations of spin directions belong to the matrix group \(SU(2)\). What phase numbers do is make the scalar factors in those matrices intrinsic and branch-free.

## 2. Spin states in a phase-number gauge

Fix an analyser axis \(\mathbf z\), and denote its two normalized output eigenstates by \(\lvert+\mathbf z\rangle\) and \(\lvert-\mathbf z\rangle\). They satisfy

\[
\langle+\mathbf z\mid+\mathbf z\rangle
=\langle-\mathbf z\mid-\mathbf z\rangle=1,
\qquad
\langle+\mathbf z\mid-\mathbf z\rangle=0.
\tag{4}
\]

For a direction

\[
\mathbf n=(\sin\vartheta\cos\varphi,\;\sin\vartheta\sin\varphi,\;\cos\vartheta),
\tag{5}
\]

a convenient north-chart choice of eigenkets is

\[
\begin{aligned}
\lvert+\mathbf n\rangle
 &=\cos\!\left(\frac\vartheta2\right)\lvert+\mathbf z\rangle
 +\operatorname{Exp}(\varphi)\sin\!\left(\frac\vartheta2\right)\lvert-\mathbf z\rangle,\\
\lvert-\mathbf n\rangle
 &=-\operatorname{Exp}(-\varphi)\sin\!\left(\frac\vartheta2\right)\lvert+\mathbf z\rangle
 +\cos\!\left(\frac\vartheta2\right)\lvert-\mathbf z\rangle .
\end{aligned}
\tag{6}
\]

The only directional phase in this gauge is the phase number \(\operatorname{Exp}(\varphi)\). Directly from (1), the two vectors are normalized and orthogonal. For example,

\[
\langle+\mathbf n\mid-\mathbf n\rangle
=-\cos\!\left(\frac\vartheta2\right)\operatorname{Exp}(-\varphi)\sin\!\left(\frac\vartheta2\right)
+\operatorname{Exp}(-\varphi)\sin\!\left(\frac\vartheta2\right)\cos\!\left(\frac\vartheta2\right)=0.
\tag{7}
\]

The phase number in (6) depends on the chosen local section of the spinor bundle. A rephasing \(\lvert\pm\mathbf n\rangle\mapsto w_\pm(\mathbf n)\lvert\pm\mathbf n\rangle\), with \(w_\pm\in U(1)\), changes a ket representative but not its rank-one projector:

\[
P_{\mathbf n,\pm}=\lvert\pm\mathbf n\rangle\langle\pm\mathbf n\rvert.
\tag{8}
\]

Thus the projectors, rather than a selected spinor phase coordinate, are the natural objects for the measurement derivation.

In the \(\{\lvert+\mathbf z\rangle,\lvert-\mathbf z\rangle\}\) basis, write \(c=\cos(\vartheta/2)\) and \(s=\sin(\vartheta/2)\). Equation (8) gives

\[
P_{\mathbf n,+}=
\begin{pmatrix}
 c^2 & cs\,\operatorname{Exp}(-\varphi)\\
 cs\,\operatorname{Exp}(\varphi) & s^2
\end{pmatrix},
\quad
P_{\mathbf n,-}=I-P_{\mathbf n,+}.
\tag{9}
\]

This is a phase-number presentation of the usual spin projector. It makes the roles transparent: real trigonometric factors set the populations, while mutually conjugate phase numbers ensure Hermiticity and encode azimuthal orientation.

## 3. The magnetic-gradient interaction and two output packets

The physical Stern–Gerlach apparatus sends neutral atoms through an **inhomogeneous** magnetic field. The magnetic potential energy and force are

\[
\widehat H_{\rm int}=-\widehat{\boldsymbol\mu}\!\cdot\!\mathbf B,
\qquad
\widehat{\mathbf F}=\nabla(\widehat{\boldsymbol\mu}\!\cdot\!\mathbf B).
\tag{10}
\]

For a spin-\(\tfrac12\) magnetic moment \(\widehat{\boldsymbol\mu}=\gamma\widehat{\mathbf S}\), choose the local analyser direction \(\mathbf n\) along the field gradient and approximate \(\mathbf B\simeq B_{\mathbf n}(q)\mathbf n\). Then

\[
\widehat H_{\rm int}\simeq-\gamma B_{\mathbf n}(q)\widehat S_{\mathbf n},
\qquad
\widehat F_{\mathbf n}\simeq\gamma\,\frac{\partial B_{\mathbf n}}{\partial q}\widehat S_{\mathbf n}.
\tag{11}
\]

These equations use no phase convention. They also show why a field **gradient**, rather than a uniform field alone, is needed to spatially resolve the spin states. The magnetic-gradient force and the two observed spin components are standard features of the Stern–Gerlach analysis.[1] [2]

The two spin eigenvalues are

\[
\widehat S_{\mathbf n}\lvert s\mathbf n\rangle
=s\frac\hbar2\lvert s\mathbf n\rangle,
\qquad s\in\{+1,-1\}.
\tag{12}
\]

Therefore the two force eigenvalues are

\[
F_{\mathbf n,s}=s\frac{\gamma\hbar}{2}\frac{\partial B_{\mathbf n}}{\partial q}.
\tag{13}
\]

The sign convention for \(\gamma\) determines which branch is labelled “up”; the essential result is the existence of **two opposite, discrete forces**. The apparatus consequently correlates the two spin projectors with two displaced spatial packets. If \(\lvert\phi_0\rangle\) is the incident packet, the ideal measurement interaction has the form

\[
U_{\rm SG}\bigl(\lvert\psi\rangle\otimes\lvert\phi_0\rangle\bigr)
=
P_{\mathbf n,+}\lvert\psi\rangle\otimes\lvert\phi_+\rangle
+
P_{\mathbf n,-}\lvert\psi\rangle\otimes\lvert\phi_-\rangle,
\tag{14}
\]

where the packet centers differ by the momentum kick implied by (13). Once the packets are resolved at the detector, \(\langle\phi_+\mid\phi_-\rangle\simeq0\), and a position measurement records one of the two beams.

## 4. Probabilities from phase-number spinors

Consider an incident spin-up state along \(\mathbf m\). Let \(\Gamma\in[0,\pi]\) be the angle between \(\mathbf m\) and the analyser direction \(\mathbf n\), so \(\mathbf m\!\cdot\!\mathbf n=\cos\Gamma\). Choose \(\mathbf n\) as the local polar axis. Equation (6) becomes

\[
\lvert+\mathbf m\rangle
=\cos\!\left(\frac\Gamma2\right)\lvert+\mathbf n\rangle
+\operatorname{Exp}(\Phi)\sin\!\left(\frac\Gamma2\right)\lvert-\mathbf n\rangle,
\tag{15}
\]

for some azimuthal phase class \(\Phi\). Applying (14) gives

\[
\begin{aligned}
U_{\rm SG}\bigl(\lvert+\mathbf m\rangle\otimes\lvert\phi_0\rangle\bigr)
={}&\cos\!\left(\frac\Gamma2\right)\lvert+\mathbf n\rangle\otimes\lvert\phi_+\rangle\\
&+\operatorname{Exp}(\Phi)\sin\!\left(\frac\Gamma2\right)\lvert-\mathbf n\rangle\otimes\lvert\phi_-\rangle.
\end{aligned}
\tag{16}
\]

The probability of each spatially separated beam is the squared norm of its branch amplitude. Since every phase number has modulus one,

\[
\begin{aligned}
\Pr(+\mathbf n\mid+\mathbf m)
&=\left|\cos\!\left(\frac\Gamma2\right)\right|^2
=\cos^2\!\left(\frac\Gamma2\right)
=\frac{1+\cos\Gamma}{2},\\
\Pr(-\mathbf n\mid+\mathbf m)
&=\left|\operatorname{Exp}(\Phi)\sin\!\left(\frac\Gamma2\right)\right|^2
=\sin^2\!\left(\frac\Gamma2\right)
=\frac{1-\cos\Gamma}{2}.
\end{aligned}
\tag{17}
\]

Substituting \(\cos\Gamma=\mathbf m\!\cdot\!\mathbf n\) yields the central result. The phase number in (16) is not discarded; rather, it cancels from a **single resolved-branch probability** because the Born norm pairs it with its inverse. This is exactly the phase-number statement of gauge invariance.

| Preparation and analysis | Relative angle \(\Gamma\) | \(\Pr(+\mathbf n)\) | \(\Pr(-\mathbf n)\) |
| --- | ---: | ---: | ---: |
| \(+\mathbf z\) into SG\(_z\) | \(0\) | \(1\) | \(0\) |
| \(+\mathbf z\) into SG\(_x\) | \(\pi/2\) | \(1/2\) | \(1/2\) |
| \(+\mathbf z\) into SG\(_{-z}\) | \(\pi\) | \(0\) | \(1\) |
| \(+\mathbf m\) into SG\(_n\) | \(\Gamma\) | \(\cos^2(\Gamma/2)\) | \(\sin^2(\Gamma/2)\) |

The special \(+\mathbf z\rightarrow\mathrm{SG}_x\) result is the familiar equal splitting in an orthogonal analyser. Sequential Stern–Gerlach experiments exhibit this incompatibility of spin components experimentally and pedagogically.[1] [2]

## 5. Sequential analysers and the physical role of a relative phase number

An SG\(_z\) apparatus followed by a selected \(+z\) output prepares \(\lvert+\mathbf z\rangle\). A second SG\(_z\) then gives \(+z\) with certainty because

\[
P_{\mathbf z,+}\lvert+\mathbf z\rangle=\lvert+\mathbf z\rangle.
\tag{18}
\]

By contrast, because \(\mathbf x\) is orthogonal to \(\mathbf z\),

\[
\lvert+\mathbf z\rangle
=\frac{\lvert+\mathbf x\rangle+\lvert-\mathbf x\rangle}{\sqrt2}.
\tag{19}
\]

A selective SG\(_x\) measurement produces either \(\lvert+\mathbf x\rangle\) or \(\lvert-\mathbf x\rangle\). Each subsequently gives \(+z\) or \(-z\) with probability \(1/2\). This is not a deficiency of phase coordinates; it is the physical consequence of applying noncommuting spin projectors.

The phase-number benefit becomes clearest in a **coherent recombination** experiment, in which the two \(x\)-separated paths remain unmeasured and are recombined. Let phase shifters apply the two phase numbers \(u_+,u_-\in U(1)\) to the two paths. Beginning with (19), the recombined spin state is

\[
\lvert\psi_{\rm rec}\rangle
=\frac{u_+\lvert+\mathbf x\rangle+u_-\lvert-\mathbf x\rangle}{\sqrt2}.
\tag{20}
\]

Its \(+z\) amplitude and probability are

\[
\begin{aligned}
A_{+z}
&=\langle+\mathbf z\mid\psi_{\rm rec}\rangle
=\frac{u_++u_-}{2},\\
\Pr(+z)
&=\frac14\left|u_++u_-\right|^2
=\frac{1+\operatorname{Re}(u_+\overline{u_-})}{2}.
\end{aligned}
\tag{21}
\]

Similarly,

\[
\Pr(-z)=\frac{1-\operatorname{Re}(u_+\overline{u_-})}{2}.
\tag{22}
\]

Only

\[
\rho=u_+\overline{u_-}\in U(1)
\tag{23}
\]

appears. This \(\rho\) is the **relative phase number**. Multiplying both arm factors by the same phase number \(w\) sends \((u_+,u_-)\mapsto(wu_+,wu_-)\), while

\[
(wu_+)\overline{(wu_-)}=u_+\overline{u_-}=\rho.
\tag{24}
\]

Hence common phase is gauge, while the relative phase number is operationally accessible through interference. When \(u_+=u_-\), equation (21) gives certainty of \(+z\), recovering the original state. When \(u_+=\operatorname{Exp}(\pi)u_-\), equation (22) gives certainty of \(-z\). This is an especially direct application of the supplied framework’s principle that a phase number—not a chosen real-valued phase lift—is the physical global object.

## 6. Spin rotations in phase-number form

The distinction between scalar phase and spin rotation is compactly expressed with the spectral projectors. A rotation of the spin state by an angle \(\alpha\) about \(\mathbf n\) is

\[
R_{\mathbf n}(\alpha)
=
\operatorname{Exp}(-\alpha/2)P_{\mathbf n,+}
+
\operatorname{Exp}(+\alpha/2)P_{\mathbf n,-}.
\tag{25}
\]

Equation (25) is the full spin-\(\tfrac12\) rotation operator written as a sum of projectors weighted by phase numbers. It reveals two important points.

First, the two eigenspaces acquire **opposite phase numbers**, so a rotation generally changes a relative phase and therefore the physical spin direction. Second,

\[
R_{\mathbf n}(2\pi)
=\operatorname{Exp}(-\pi)P_{\mathbf n,+}
+\operatorname{Exp}(\pi)P_{\mathbf n,-}
=-I.
\tag{26}
\]

A \(2\pi\) rotation multiplies a spinor by the phase number \(\operatorname{Exp}(\pi)=-1\). It leaves an isolated state ray unchanged, yet can become observable as a relative phase if one arm of an interferometer undergoes that rotation. The half-angle in (25), and hence this sign, belongs to the \(SU(2)\) geometry of spinors; it is not a scalar \(U(1)\) phenomenon by itself.

## 7. Scope and conclusion

The phase-number reformulation leaves the Stern–Gerlach physics unchanged:

\[
\boxed{
\Pr(\pm\mathbf n\mid+\mathbf m)
=\frac{1\pm\mathbf m\!\cdot\!\mathbf n}{2}}
\tag{27}
\]

The magnetic gradient converts the two eigenvalues of \(\widehat S_{\mathbf n}\) into opposite momentum kicks, producing two spatially distinct beams. Phase numbers describe the azimuthal factor in spinors, the branch factors under rotations, and the phases accumulated in coherent paths. In a resolved single-analyser measurement, their inverse pairing removes them from probabilities. In recombination, the gauge-invariant product \(u_+\overline{u_-}\) controls interference.

The framework therefore supports a clean conceptual separation:

| Layer of the calculation | Intrinsic object | Physical role |
| --- | --- | --- |
| Scalar phase | \(u\in U(1)\) | A unit-modulus factor of an amplitude |
| Relative scalar phase | \(u_1\overline{u_2}\in U(1)\) | Interference observable |
| Spin outcome | \(P_{\mathbf n,\pm}\) | Two Stern–Gerlach branches |
| Spatial record | \(\lvert\phi_\pm\rangle\) | Separated detector packets |
| Spin rotation | \(R_{\mathbf n}(\alpha)\in SU(2)\) | Noncommuting change of analyser basis |

The only necessary caution is that **phase numbers do not replace the spinor state space or its noncommutative rotation structure**. They replace the ambiguous treatment of scalar phases by globally defined elements of \(U(1)\). In that precise sense, the Stern–Gerlach derivation can be written entirely with phase numbers while preserving all standard predictions.

## References

[1] [A. J. McCulloch, “The Stern–Gerlach Experiment,” *Quantum Mechanics*, University of Tasmania.](https://qm.utasphys.cloud.edu.au/01-stern-gerlach/1-1-exp/)

[2] [V. F. M. de Oliveira, “Chapter 1: Stern–Gerlach Experiments,” *Introduction to Quantum Mechanics: Self Guided Course*, Pennsylvania State University.](https://sites.esm.psu.edu/~vfm5153/IQM/chapter1.html)

[3] [IBM Quantum, “The Stern–Gerlach Experiment Using Quantum Computers.”](https://quantum.cloud.ibm.com/learning/en/modules/quantum-mechanics/stern-gerlach-measurements-with-qiskit)

[4] Marlon Hanks, *Phase Numbers: An Intrinsic Calculus of Unit-Complex Scalars, Circular Coordinates, and Holonomy*, user-supplied manuscript, 22 August 2026.

---

### Notational note

The function \(\operatorname{Exp}\) in this document is exactly the phase-number map from the supplied manuscript. It stands for the globally defined member of \(U(1)\) associated with an angular class. Angles such as \(\varphi\), \(\Phi\), and \(\alpha\) are therefore local representatives only; every observable phase statement above is expressed through a phase number or a relative phase number.

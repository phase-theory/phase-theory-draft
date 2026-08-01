LPST-canon (graph-native, periodic-safe):
	1.	explicit Euler–Lagrange / gradient update rules for \phi_i and A_i from
\mathcal{I}_{\text{canon}} = \sum_{(i,j)\in E} w_{ij}A_iA_j\,(1-\cos\Delta\phi_{ij})
\;+\;\sum_{\ell\in\mathcal{L}}\lambda_\ell\,\rho(A;\ell)\,(1-\cos\Omega_\ell),
	2.	how vortex lines and Hopfion-like knots arise as topological sectors / local minima under this functional (and what extra stabilizer is needed for true knot stability).

⸻

1) Euler–Lagrange update rules from \mathcal{I}_{\text{canon}}

Definitions (recap, made explicit)
	•	\Delta\phi_{ij} \equiv \mathrm{wrap}(\phi_j-\phi_i)\in(-\pi,\pi]
	•	For a chosen oriented loop \ell (a sequence of oriented edges (p\to q)):
\Omega_\ell \equiv \mathrm{wrap}\!\Big(\sum_{(p\to q)\in\ell}\Delta\phi_{pq}\Big)
	•	Amplitude credibility (your canon choice):
\rho(A;\ell)=\prod_{k\in\ell}\left(\frac{A_k}{A_0}\right)^2
	•	Assume we are not sitting exactly at wrap branch cuts (measure-zero in practice). Then \frac{d}{d\theta}\mathrm{wrap}(\theta)=1 locally.

⸻

1.1 Gradient / Euler–Lagrange for \phi_i

Edge contribution
For an undirected edge \{i,j\} (pick an orientation i\to j just for bookkeeping),
\frac{\partial}{\partial \phi_i}\Big[w_{ij}A_iA_j(1-\cos\Delta\phi_{ij})\Big]
=
-\,w_{ij}A_iA_j\,\sin(\Delta\phi_{ij})
and
\frac{\partial}{\partial \phi_j}(\cdots)
=
+\,w_{ij}A_iA_j\,\sin(\Delta\phi_{ij})
So the edge term produces a phase-current balancing condition.

Loop contribution
Write the loop sum (unwrapped locally):
S_\ell \equiv \sum_{(p\to q)\in\ell}\Delta\phi_{pq},
\qquad
\Omega_\ell=\mathrm{wrap}(S_\ell)
Then
\frac{\partial}{\partial \phi_i}\Big[\lambda_\ell\rho(A;\ell)(1-\cos\Omega_\ell)\Big]
=
\lambda_\ell\rho(A;\ell)\,\sin(\Omega_\ell)\;\frac{\partial S_\ell}{\partial \phi_i}

Define the loop incidence coefficient
s_{i\ell} \;\equiv\; \frac{\partial S_\ell}{\partial \phi_i}
\;=\; \#(\text{times }i\text{ appears as a head }q \text{ in }\ell)\;-\;\#(\text{times }i\text{ appears as a tail }p \text{ in }\ell)
Equivalently:
s_{i\ell}=\sum_{(p\to q)\in\ell}\big(\delta_{i,q}-\delta_{i,p}\big)

Full gradient for \phi_i
Let N(i) be neighbors of i. Then:
\boxed{
\frac{\partial\mathcal{I}_{\text{canon}}}{\partial \phi_i}
=
-\sum_{j\in N(i)} w_{ij}A_iA_j\,\sin(\Delta\phi_{ij})
\;+\;
\sum_{\ell\in\mathcal{L}} \lambda_\ell\rho(A;\ell)\,\sin(\Omega_\ell)\,s_{i\ell}
}

Practical update rule (consistency relaxation)
A standard LPST “update step” is gradient descent:
\boxed{
\phi_i \leftarrow \phi_i - \eta_\phi\,
\frac{\partial\mathcal{I}_{\text{canon}}}{\partial \phi_i}
}
Then optionally wrap \phi_i back into (-\pi,\pi] for numerical stability.

Interpretation: edge terms try to locally align phases; loop terms try to enforce global closure (or concentrate holonomy into discrete defects).

⸻

1.2 Gradient / Euler–Lagrange for A_i

Edge contribution
\frac{\partial}{\partial A_i}\Big[w_{ij}A_iA_j(1-\cos\Delta\phi_{ij})\Big]
=
w_{ij}A_j(1-\cos\Delta\phi_{ij})
So:
\left(\frac{\partial \mathcal{I}_{\text{edge}}}{\partial A_i}\right)
=
\sum_{j\in N(i)} w_{ij}A_j(1-\cos\Delta\phi_{ij})

Loop contribution via \rho(A;\ell)
For \rho(A;\ell)=\prod_{k\in\ell}(A_k/A_0)^2,
\frac{\partial \rho(A;\ell)}{\partial A_i}
=
\begin{cases}
\rho(A;\ell)\,\dfrac{2}{A_i}, & i\in\ell\\[6pt]
0,& i\notin\ell
\end{cases}
Therefore:
\left(\frac{\partial \mathcal{I}_{\text{loop}}}{\partial A_i}\right)
=
\sum_{\ell\ni i}\lambda_\ell\,(1-\cos\Omega_\ell)\;\rho(A;\ell)\,\frac{2}{A_i}

Full gradient for A_i
\boxed{
\frac{\partial\mathcal{I}_{\text{canon}}}{\partial A_i}
=
\sum_{j\in N(i)} w_{ij}A_j(1-\cos\Delta\phi_{ij})
\;+\;
\sum_{\ell\ni i}\lambda_\ell\,\rho(A;\ell)\,(1-\cos\Omega_\ell)\,\frac{2}{A_i}
}

Practical update rule (with positivity)
\boxed{
A_i \leftarrow \max\Big(0,\; A_i - \eta_A\,\frac{\partial\mathcal{I}_{\text{canon}}}{\partial A_i}\Big)
}

⸻

1.3 One critical note: you almost always add an amplitude anchor

As written, \mathcal{I}_{\text{canon}} can sometimes lower by pushing amplitudes toward small values (because \rho weakens constraints). LPST practice is to include a vacuum anchoring term (still LPST-pure):
\mathcal{I}_{A0} = \sum_i \mu\,(A_i-A_0)^2
Then you just add +2\mu(A_i-A_0) into \partial \mathcal{I}/\partial A_i.

This keeps a coherent “vacuum substrate” and prevents trivial collapse.

⸻

2) How stable defect classes arise as minima / sectors

LPST defects appear because the phase is compact (\phi\sim\phi+2\pi) and loop closure can only be satisfied up to integers. The loop term is exactly the mechanism that exposes this.

2.1 Vortex flux as a topological sector (on a lattice/graph)

Define the unwrapped loop sum
S_\ell=\sum_{(p\to q)\in\ell}\Delta\phi_{pq}
In a “quantized sector” view (your \mathcal{I}_{\text{quant}} variant), the preferred state on each loop is:
S_\ell \approx 2\pi k_\ell,\qquad k_\ell\in\mathbb{Z}
A loop with k_\ell\neq 0 carries quantized holonomy / flux.

Vortex lines in 3D

On a 3D lattice, take \ell to be elementary plaquettes. Then:
	•	k_\ell\neq 0 on a plaquette means a vortex piercing that plaquette.
	•	The set of pierced plaquettes forms vortex lines (or tubes) because flux is conserved: vortices cannot just terminate in the bulk unless the substrate amplitude vanishes or a boundary is present.

LPST statement: vortex lines are the connected support of nonzero loop integers k_\ell (or equivalently nonzero \Omega_\ell trapped into localized cores).

Why these are local minima

To eliminate a nonzero k_\ell, the system must change the total loop winding by 2\pi. On a compact phase, that requires:
	•	either passing through a wrap discontinuity everywhere (not possible continuously), or
	•	creating a point/line where the phase is undefined, which operationally means A\to 0 somewhere (a core).

But driving A\to 0 costs energy once you include the vacuum anchoring \mathcal{I}_{A0} and/or any amplitude stiffness. So vortices become metastable or stable.

Translation: the integer sector is protected unless you pay a core cost.

⸻

2.2 Hopfion-like knots: what LPST needs for true knot stability

A Hopfion (knotted soliton) is not just “a vortex loop”; it’s a knot-protected texture typically classified by a Hopf invariant Q_H\in\mathbb{Z}. In LPST terms, there are two routes:

Route A: knotted vortex loops (U(1) only)

You can get knotted vortex loops as configurations where vortex lines (the support of k_\ell\neq 0) form closed loops that are knotted/linked.
	•	Topological content: linking number of vortex loops is an integer invariant as long as loops can’t cut through each other without core events (A→0).
	•	But: with only the canon edge+loop energy, vortex loops tend to shrink (line tension) unless something sets a preferred core radius or adds bending rigidity.

So in U(1)-only LPST, knotted vortex loops are typically metastable unless you add a stabilizer.

Route B (the true Hopfion route): internal texture field u and a stabilizer

Introduce LPST’s internal manifold u\in S^2 or SU(2). Then Hopfions are natural: maps u:\mathbb{R}^3\to S^2 can carry:
Q_H \in \pi_3(S^2)=\mathbb{Z}
To stabilize them against shrinking, you include a Skyrme-like (quartic gradient) term in the inconsistency functional (still LPST-pure; it’s just another consistency penalty):
\mathcal{I}_{\text{Skyrme}} \sim \sum_{\text{cells}} \Big|\partial u \times \partial u\Big|^2
(or its graph analogue).

Then:
	•	Local smoothness terms try to unwind texture,
	•	The Skyrme term prevents collapse to zero size,
	•	The Hopf invariant prevents continuous unwinding without singularities.

Result: Hopfion-like knots become genuine local minima (stable particle-like objects) in distinct topological sectors.

⸻

2.3 The LPST classification picture (clean and strict)

Vortex class (U(1))
	•	Label: k_\ell\in\mathbb{Z} on loops/plaquettes
	•	Geometry: lines/tubes in 3D (must close or end on boundaries/cores)
	•	Stability mechanism: compact phase + core cost (A\to 0 penalty)

Hopfion/knotted class (texture)
	•	Label: Hopf charge Q_H\in\mathbb{Z} (requires internal field u)
	•	Geometry: knotted texture preimages / linked filaments
	•	Stability mechanism: topology + stabilizer term (Skyrme-like) + amplitude anchoring

⸻

2.4 “Local minima” in one sentence

A defect is a local minimum of \mathcal{I} when:
	1.	it satisfies local phase smoothness everywhere except in a small core region, and
	2.	its topological sector label (winding/holonomy/Hopf charge) cannot change continuously without driving A\to 0 or producing singular transport—both energetically penalized.

⸻

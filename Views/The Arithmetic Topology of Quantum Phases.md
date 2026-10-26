# The Arithmetic Topology of Quantum Phases

Integer-Valued Invariants, Number-Theoretic Constraints, and Classification of Topological Band Transitions

Research preprint · October 25, 2026

## Abstract

Topological phases of quantum matter are classified, in important settings, by integer-valued invariants that remain stable under continuous deformations preserving specified spectral and symmetry conditions. In two-dimensional periodic band systems, the first Chern number of an isolated band bundle is

\\[ C=\frac{1}{2\pi}\int\_{\mathrm{BZ}}\Omega(\mathbf k)\\,d^2k\in\mathbb Z, \\]

where \\(\Omega(\mathbf k)\\) is the Berry curvature and the Brillouin zone is treated as a compact two-dimensional manifold. The integrality of \\(C\\) is a theorem of bundle topology. Whether further arithmetic restrictions govern the values of \\(C\\), the allowed sequences of topological transitions, or the structure of families of Hamiltonians is a separate and substantially more difficult question.

This paper develops an explicit framework for investigating that question. It distinguishes topological quantization from additional arithmetic constraints; constructs a classification problem for smooth and analytic families of finite-range Bloch Hamiltonians; derives transition-charge conservation from the topology of the occupied-state bundle; and formulates conditions under which arithmetic restrictions on transition sequences could become rigorous theorems rather than numerical observations. A concrete two-band lattice Hamiltonian is analyzed in detail. Its phase diagram demonstrates both the power and the limitations of integer classification: the Chern number is quantized and changes at gap closings, but its allowed values depend on the Hamiltonian family and its parameterization, not on a universal divisibility rule imposed by the Chern number alone.

The central result is a conditional classification theorem for gapped regions and isolated topological transitions in a one-parameter Hamiltonian family. A second theorem identifies the conservation law for the total topological charge of isolated degeneracies in an extended parameter space. These results establish the mathematical infrastructure required for an arithmetic theory of quantum phases while isolating the genuinely open step: deriving additional number-theoretic restrictions from explicit microscopic, symmetry, locality, or representation-theoretic hypotheses. The paper concludes with falsifiable criteria and a research program for identifying such restrictions in concrete materials and Hamiltonian families.

Keywords: topological phases; Chern number; Berry curvature; Bloch Hamiltonians; arithmetic topology; topological transitions; Dirac points; symmetry constraints; spectral gaps; lattice models.

## 1. Introduction: From Topological Integers to Arithmetic Structure

Topological band theory begins with a robust observation: certain global properties of quantum states cannot change continuously while the relevant energy gap and protecting assumptions remain intact. In two dimensions, the first Chern number provides a canonical example. It classifies complex vector bundles over the Brillouin torus when the occupied subspace has fixed rank and no additional symmetry changes the classification problem.

The integer is not merely an approximately quantized observable. Its integrality follows from the global geometry of the eigenstates, even though the Berry curvature itself can vary continuously across momentum space. The integer thus compresses information about a continuous quantum system into a discrete invariant.

Arithmetic topology asks a further question:

> Do microscopic structure, symmetry, locality, or the arithmetic organization of Hamiltonian parameters impose additional exact restrictions on the topological integers and on how those integers can change?

The question has several distinct meanings that must not be conflated.

1. Topological integrality: why a Chern number belongs to \\(\mathbb Z\\).
2. Family-specific restrictions: why a particular Hamiltonian family realizes only certain Chern numbers.
3. Transition arithmetic: why a specified family permits only certain changes \\(\Delta C\\).
4. Relations among invariants: whether Chern numbers, symmetry indicators, winding numbers, or other integers obey additional identities.
5. Arithmetic organization of parameter space: whether divisibility, congruence, prime factorization, or integer-valued functions describe physically meaningful partitions of model families.
6. Material prediction: whether a derived arithmetic rule predicts a phase or transition not used to formulate the rule.

The first problem is established mathematics. The remaining problems require explicit hypotheses and model-dependent analysis. In particular, the fact that numerical Chern numbers form an integer sequence does not imply that the sequence obeys a deeper number-theoretic law.

The purpose of this paper is to construct a rigorous bridge between these questions without assuming that the bridge already exists.

### 1.1 Central thesis

The thesis investigated here is conditional:

Arithmetic restrictions on topological quantum phases can arise when the topology of the occupied-state bundle is combined with additional structure that restricts the admissible Hamiltonians or their degeneracies.

Such structure might include crystalline symmetry, constrained hopping ranges, chiral or particle-hole symmetry, representation content at high-symmetry momenta, a fixed algebraic parameterization, or an independently specified family of allowed perturbations. The arithmetic restriction must be derived from that structure; it cannot be inferred from a small list of computed invariants.

### 1.2 Scope and conventions

We consider noninteracting periodic systems initially, with extensions to interacting systems discussed separately. The Brillouin zone is a torus \\(\mathbb T^2\\). We set \\(\hbar=1\\) unless units are explicitly needed.

For an \\(N\\)-band Bloch Hamiltonian,

\\[ H(\mathbf k;\lambda)\in \operatorname{Herm}(N), \qquad \mathbf k\in\mathbb T^2, \\]

the parameter \\(\lambda\\) may represent a tunable coupling, mass, strain, magnetic field, or another externally controlled variable. We assume smoothness in momentum and parameter unless otherwise stated.

For a chosen Fermi energy \\(E_F\\), a gap is open if

\\[ \operatorname{dist} \big(E_F,\sigma(H(\mathbf k;\lambda))\big)>0 \quad\text{for all }\mathbf k\in\mathbb T^2. \\]

The occupied projector is then smooth and defines a vector bundle over the Brillouin zone. Its topological classification is the starting point of the analysis.

## 2. Mathematical Foundations

### 2.1 The occupied-state bundle

Let \\(H(\mathbf k)\\) be a smooth Bloch Hamiltonian with \\(r\\) occupied bands separated by a spectral gap from all unoccupied bands. The spectral projector onto the occupied subspace is

\\[ P(\mathbf k)=\frac{1}{2\pi i} \oint\_{\Gamma}(z-H(\mathbf k))^{-1}\\,dz, \\]

where the contour \\(\Gamma\\) encloses the occupied spectrum and no unoccupied eigenvalues. As long as the gap remains open, \\(P(\mathbf k)\\) varies smoothly with \\(\mathbf k\\).

The occupied eigenspaces

\\[ E\_{\mathbf k}=\operatorname{Ran}P(\mathbf k) \\]

form a rank-\\(r\\) complex vector bundle \\(E\to\mathbb T^2\\). Its first Chern number is the integral of the first Chern class over the Brillouin torus:

\\[ C_1(E)=\langle c_1(E),[\mathbb T^2]\rangle\in\mathbb Z. \\]

This is the bundle-theoretic origin of the Chern number. The integer is not obtained by rounding a numerical integral. Rather, an exactly defined smooth bundle possesses an integral characteristic class, and the curvature integral represents that class.

For a single isolated occupied band, choose a normalized local eigenvector \\(|u(\mathbf k)\rangle\\). With Berry connection

\\[ A=i\langle u|d u\rangle \\]

and curvature \\(F=dA\\), the first Chern number is

\\[ C=\frac{1}{2\pi}\int\_{\mathbb T^2}F. \\]

Writing \\(F=\Omega(\mathbf k)\\,dk_x\wedge dk_y\\) recovers

\\[ C=\frac{1}{2\pi}\int\_{\mathrm{BZ}} \Omega(\mathbf k)\\,d^2k. \\]

For multiple occupied bands, the gauge-invariant expression is

\\[ C=\frac{i}{2\pi} \int\_{\mathbb T^2} \operatorname{Tr}\\!\left( P[\partial\_{k_x}P,\partial\_{k_y}P] \right)d^2k, \\]

with the overall sign fixed by the Berry-connection convention. The projector expression avoids choosing a global basis for the occupied subspace, which may not exist.

### 2.2 Stability under gapped deformation

Let \\(H_s(\mathbf k)\\), \\(s\in[0,1]\\), be a smooth family with a common spectral gap at \\(E_F\\). The occupied projectors form a vector bundle over \\(\mathbb T^2\times[0,1]\\). Restricting this bundle to the two boundary tori gives isomorphic topological classes. Consequently,

\\[ C[H_0]=C[H_1]. \\]

This is the basic homotopy-invariance theorem.

Corollary 2.1 — Necessity of a gap closing.\
If two Hamiltonians in a continuous family have different occupied-band Chern numbers, every continuous interpolation between them must close the relevant spectral gap at some intermediate parameter.

This conclusion does not determine the value of the change in \\(C\\), the number of gap closings, or the momentum at which they occur. Those depend on the detailed family.

### 2.3 What the integer does—and does not—classify

For a two-dimensional charge-conserving band insulator in symmetry class A, the first Chern number classifies stable topological phases in the relevant two-dimensional setting. For a fixed finite-dimensional Hamiltonian family, however, the set of realizable values may be smaller than \\(\mathbb Z\\).

The distinction is fundamental:

- \\(\mathbb Z\\) describes the general topological classification available in the class-A setting.
- A specified Hamiltonian family traces out only a subset of that classification space.
- Extra restrictions on the family can exclude otherwise topologically allowed phases.
- Those exclusions may be arithmetic, but the arithmetic must follow from the restrictions.

A family realizing only \\(C\in\\{-1,0,1\\}\\) does not establish that Chern numbers are universally bounded by one. It establishes that the particular family has that property, subject to its stated assumptions.

### 2.4 Arithmetic functions as candidate classifiers

Let \\(\mathcal H\\) denote a space of admissible Hamiltonians, and let

\\[ C:\mathcal H\_{\mathrm{gap}}\to\mathbb Z \\]

be the Chern-number map on the gapped subset. An arithmetic constraint is a further statement about this map or its variation. Examples include

\\[ C(H)\equiv a\pmod q, \\]

\\[ \Delta C\in q\mathbb Z, \\]

or a relation involving a family of integer invariants,

\\[ \mathcal R(C_1,\ldots,C_s)=0. \\]

Here \\(q\\) must be specified by the underlying model or symmetry; it cannot be chosen after observing a finite dataset merely to make the data fit.

A general arithmetic function \\(f:\mathbb Z\to\mathbb Z\\), such as a divisor-counting or Möbius function, has no automatic physical significance when evaluated on a Chern number. It becomes relevant only if a derivation connects it to a gauge-invariant property of the Hamiltonian, its symmetry representations, its allowed defects, or its experimentally measurable response.

We therefore distinguish three layers:

\\[ \boxed{ \text{topological invariant} \\;\longrightarrow\\; \text{model-imposed restriction} \\;\longrightarrow\\; \text{arithmetic law} } \\]

The first arrow is not automatic, and the second is not guaranteed. This hierarchy will govern the classification theorems below.

## 3. The Arithmetic Classification Problem

### 3.1 Hamiltonian families and their phase spaces

Let \\(\Lambda\\) be a parameter manifold and consider

\\[ H:\mathbb T^2\times\Lambda\to\operatorname{Herm}(N). \\]

Define the gapped parameter set

\\[ \Lambda\_{\mathrm{gap}} = \left\\{ \lambda\in\Lambda: \min\_{\mathbf k\in\mathbb T^2} \operatorname{dist}(E_F,\sigma(H(\mathbf k;\lambda)))>0 \right\\}. \\]

On each connected component \\(U\subseteq\Lambda\_{\mathrm{gap}}\\), the Chern number is constant. Hence the phase diagram induces a locally constant function

\\[ C:\Lambda\_{\mathrm{gap}}\to\mathbb Z. \\]

The classification problem has two complementary forms.

Phase classification: determine the connected components of \\(\Lambda\_{\mathrm{gap}}\\) and the integer label assigned to each component.

Transition classification: determine the gap-closing locus and calculate the integer charge carried by each isolated degeneracy, including how symmetry or family constraints restrict the possible charges.

Arithmetic topology seeks additional structure in these maps: congruence classes, divisibility restrictions, allowed jump sets, or relations between invariants across distinct components.

### 3.2 The distinction between an image and a law

For a fixed family \\(\mathcal F\subseteq\mathcal H\\), define its realized Chern set

\\[ \mathcal C(\mathcal F) = \\{C(H):H\in\mathcal F,\ H\text{ gapped}\\}. \\]

A computed set \\(\mathcal C(\mathcal F)=\\{-1,0,1\\}\\) is a descriptive result. A theorem of arithmetic restriction requires a proof that

\\[ C(H)\in S \quad\text{for every admissible }H\in\mathcal F \\]

for a specified subset \\(S\subseteq\mathbb Z\\).

If the family is described by a finite-range hopping ansatz, the proof must account for every allowed coefficient and every parameter value covered by the claim. If the family is constrained by symmetry, the proof must use the actual symmetry representation and not merely the symmetry label. If parameters are restricted to rational or integer values, the domain restriction must be physically justified and stated explicitly.

### 3.3 Candidate sources of arithmetic restrictions

Several mechanisms could, in principle, generate exact arithmetic constraints.

1. Symmetry representations. Rotation or other crystalline symmetries can relate topological invariants to symmetry eigenvalues at invariant momenta, subject to the symmetry class and the precise invariant being considered.
2. Constrained band crossings. Symmetry can force degeneracies to occur in related sets. The total topological charge of such a set may then be restricted.
3. Restricted hopping range. A finite Fourier expansion limits the functional form of the Bloch Hamiltonian. The realized invariant set may depend on the allowed harmonics and coefficients.
4. Chiral or particle-hole structure. Additional symmetries change the classification problem and can introduce winding numbers, parity constraints, or relations among invariants.
5. Parameter-space topology. A family may define a map between parameter spaces whose degree constrains an induced invariant.
6. Algebraic constraints. If a Hamiltonian family is defined by exact polynomial relations, its degeneracy locus and transition multiplicities may inherit algebraic restrictions.
7. Interacting response constraints. In suitable settings, quantized response coefficients and anomaly-matching conditions can constrain allowed phases beyond a single-particle band description.

None of these mechanisms implies a universal prime-factorization law for Chern numbers. The appropriate arithmetic structure depends on the assumptions.

## 4. Transition Charges and Conservation

The strongest starting point for a rigorous arithmetic theory is the local topology of isolated gap closings.

### 4.1 An isolated degeneracy as a source of Chern-number change

Consider a one-parameter family \\(H(\mathbf k;\lambda)\\). Suppose the gap closes at an isolated point \\((\mathbf k\_\ast,\lambda\_\ast)\\) and remains open on a small enclosing surface in the three-dimensional space \\((k_x,k_y,\lambda)\\).

For a two-band crossing, write the effective Hamiltonian near the degeneracy as

\\[ H\_{\mathrm{eff}}(\mathbf q) = d_0(\mathbf q)I+ \mathbf d(\mathbf q)\cdot\boldsymbol\sigma, \\]

where

\\[ \mathbf q=(k_x-k\_{x\ast},\\,k_y-k\_{y\ast},\\,\lambda-\lambda\_\ast). \\]

The identity term \\(d_0I\\) does not affect the eigenvectors. If the crossing is linear and isolated,

\\[ d_i(\mathbf q)=\sum\_{j=1}^{3}V\_{ij}q_j+O(|\mathbf q|^2), \qquad \det V\ne0. \\]

On a small sphere \\(S^2\_\epsilon\\) surrounding the degeneracy, the normalized vector

\\[ \widehat{\mathbf d}=\frac{\mathbf d}{|\mathbf d|} \\]

defines a map \\(S^2\_\epsilon\to S^2\\). Its degree is

\\[ Q=\deg(\widehat{\mathbf d})\in\mathbb Z. \\]

For a simple linear crossing, \\(Q=\operatorname{sgn}(\det V)\\), with the sign of the associated Chern jump depending on the orientation and Berry-curvature convention.

The degeneracy is therefore a monopole of Berry curvature in the extended momentum-parameter space. The change in the two-dimensional Chern number across the crossing is the charge enclosed by the corresponding surface, up to the same orientation convention.

### 4.2 Transition-charge theorem

Theorem 4.1 — Chern jump as a degeneracy charge.\
Let \\(H(\mathbf k;\lambda)\\) be a smooth two-band Bloch Hamiltonian on \\(\mathbb T^2\times[\lambda\_-,\lambda\_+]\\). Suppose the occupied band is nondegenerate and separated from the unoccupied band except at a finite set of isolated degeneracies \\(p_j=(\mathbf k_j,\lambda_j)\\) in the interior. Assume the gap is open at \\(\lambda\_-\\) and \\(\lambda\_+\\). Let \\(Q_j\\) be the oriented Berry-monopole charge of the \\(j\\)-th degeneracy. Then

\\[ C(\lambda\_+)-C(\lambda\_-) = \sum_j Q_j, \\]

provided the orientations defining \\(Q_j\\) and the Chern number are chosen consistently.

Proof. Remove disjoint small three-balls around the degeneracies from \\(\mathbb T^2\times[\lambda\_-,\lambda\_+]\\). On the remaining manifold the occupied-state line bundle is smooth, and its Berry curvature is closed. Stokes' theorem applied to the curvature flux gives equality between the flux through the two boundary tori and the sum of fluxes through the small spheres surrounding the removed points, with the induced orientations. Dividing by \\(2\pi\\) identifies the torus fluxes with the endpoint Chern numbers and the sphere fluxes with the integer charges \\(Q_j\\). Rearranging gives the result. \\(\square\\)

The theorem is topological, not conjectural. It establishes that the change in \\(C\\) is an integer sum of local charges. It does not say that each charge is \\(+1\\) or \\(-1\\), that the number of crossings is fixed, or that the sum is divisible by a particular integer.

### 4.3 What symmetry can add

Suppose a symmetry maps a degeneracy at \\(\mathbf k\_\ast\\) to a distinct degeneracy at \\(g\mathbf k\_\ast\\). If the symmetry preserves the Hamiltonian family, it can constrain the relation between the two local charges. Depending on how the symmetry acts on momentum, the parameter, and the occupied states, the related charges may agree or differ in sign.

If every allowed isolated crossing occurs in a symmetry orbit whose total charge is a multiple of \\(q\\), then Theorem 4.1 immediately gives

\\[ \Delta C\in q\mathbb Z. \\]

But this conclusion requires the orbit-charge statement as a proven hypothesis. Symmetry-related degeneracies do not automatically have equal charges, and fixed points of a symmetry need separate treatment. A claimed divisibility law must account for all allowed degeneracy orbits, including symmetry-invariant points and any non-generic higher-order crossings.

This gives a useful general principle:

Arithmetic restrictions on topological transitions can be derived by proving restrictions on the allowed sums of local topological charges.

The principle is rigorous. Whether a given material or Hamiltonian family satisfies the required hypotheses is a separate problem.

## 5. A Concrete Hamiltonian: The Two-Band Chern Insulator

We now examine a lattice model for which the entire topological phase diagram can be calculated analytically. The model is commonly associated with the Qi–Wu–Zhang construction of a two-dimensional Chern insulator.

### 5.1 Hamiltonian and spectrum

Consider the square-lattice Bloch Hamiltonian

\\[ H(\mathbf k;m)= \sin k_x\\,\sigma_x+ \sin k_y\\,\sigma_y+ (m+\cos k_x+\cos k_y)\\,\sigma_z, \\]

where \\(\mathbf k=(k_x,k_y)\in[-\pi,\pi)^2\\) and \\(m\in\mathbb R\\) is a tunable mass parameter. The lattice spacing and overall hopping scale have been set to one.

The Hamiltonian has two bands with energies

\\[ E\_\pm(\mathbf k;m)=\pm|\mathbf d(\mathbf k;m)|, \\]

where

\\[ \mathbf d= \big( \sin k_x,\\, \sin k_y,\\, m+\cos k_x+\cos k_y \big). \\]

At half filling, the lower band is occupied. A gap closing requires \\(\mathbf d=0\\). The first two components vanish simultaneously only when

\\[ k_x,k_y\in\\{0,\pi\\}. \\]

The third component then yields four candidate critical points:

| Momentum        | Gap-closing condition |
| --------------- | --------------------- |
| \\((0,0)\\)     | \\(m=-2\\)            |
| \\((\pi,0)\\)   | \\(m=0\\)             |
| \\((0,\pi)\\)   | \\(m=0\\)             |
| \\((\pi,\pi)\\) | \\(m=2\\)             |

Therefore the model is gapped for

\\[ m\notin\\{-2,0,2\\}. \\]

This gap analysis is exact and already constrains the possible phase transitions. It does not yet assign a Chern number to each region.

### 5.2 Computing the Chern number

For a two-band Hamiltonian \\(H=\mathbf d\cdot\boldsymbol\sigma\\), the lower-band Chern number can be expressed, under a fixed Berry-curvature convention, as the degree of the map \\(\widehat{\mathbf d}:\mathbb T^2\to S^2\\), with a possible overall sign depending on convention:

\\[ C=\frac{1}{4\pi}\int\_{\mathbb T^2} \widehat{\mathbf d}\cdot \left( \partial\_{k_x}\widehat{\mathbf d} \times \partial\_{k_y}\widehat{\mathbf d} \right)d^2k. \\]

An equivalent and efficient calculation uses the massive Dirac cones at the four momenta where \\(\sin k_x=\sin k_y=0\\). Near each point, the Hamiltonian has the form

\\[ H_j(\mathbf q)\simeq v\_{x,j}q_x\sigma_x+ v\_{y,j}q_y\sigma_y+ M_j(m)\sigma_z. \\]

Each cone contributes a half-integer term proportional to the sign of its Dirac mass and velocity orientation. Although individual continuum-cone contributions are half-integer, their properly regularized lattice sum is an integer. In the convention adopted here, the phase diagram is

\\[ C(m)= \begin{cases} 0, & m<-2,\\\\[2pt] +1, & -2\<m<0,\\\\[2pt] -1, & 0\<m<2,\\\\[2pt] 0, & m>2. \end{cases} \\]

Reversing the orientation convention for Berry curvature reverses every sign but leaves the phase boundaries and the absolute jumps unchanged.

### Phase diagram of the lattice model

The critical values are gapless; the open intervals are gapped phases.

## \\(m<-2\\)

# \\(C=0\\)

Topologically trivial band insulator

## \\(-2\<m<0\\)

# \\(C=+1\\)

Chern-insulating phase

## \\(0\<m<2\\)

# \\(C=-1\\)

Chern-insulating phase of opposite sign

## \\(m>2\\)

# \\(C=0\\)

Topologically trivial band insulator

At \\(m=-2,0,2\\), the bulk gap closes and the gapped-phase Chern number is not defined for the touching bands as an isolated-band invariant.

### 5.3 Local transition charges

The sequence of Chern numbers across the critical values is

\\[ 0\longrightarrow +1\longrightarrow -1\longrightarrow 0. \\]

Thus the oriented jumps are

\\[ \Delta C\in\\{+1,-2,+1\\}, \\]

when the parameter is increased through \\(-2,0,2\\), respectively, with the stated convention.

The middle transition occurs at two distinct momenta, \\((\pi,0)\\) and \\((0,\pi)\\). Each contributes a unit local charge of the same oriented sign, yielding the total jump of magnitude two. This is a concrete example of a larger Chern-number change arising from multiple gap closings at the same parameter value, rather than from a single crossing that must carry charge two.

The transition sequence therefore has a simple arithmetic signature: the central jump has magnitude \\(2\\), whereas the outer jumps have magnitude \\(1\\). But the sequence does not, by itself, imply a universal arithmetic law. The value \\(2\\) follows from the two simultaneous degeneracies in this Hamiltonian. A perturbation that breaks the symmetry relating those degeneracies can, if it preserves the relevant setting and separates their critical parameters, split the middle transition into two unit transitions.

### 5.4 Theorem 5.1 — Exact classification of the one-parameter model

Theorem. For the Hamiltonian

\\[ H(\mathbf k;m)= \sin k_x\\,\sigma_x+ \sin k_y\\,\sigma_y+ (m+\cos k_x+\cos k_y)\sigma_z, \\]

at half filling and with the orientation convention specified above:

1. the spectrum is gapped precisely for \\(m\notin\\{-2,0,2\\}\\);
2. the Chern number is constant on each connected component of the gapped parameter set;
3. the Chern number takes the values \\(0,+1,-1,0\\) on the four successive intervals;
4. the changes at the three critical values are \\(+1,-2,+1\\).

Proof. The gap-closing conditions follow from \\(E\_\pm=\pm|\mathbf d|\\) and the simultaneous equations \\(d_x=d_y=d_z=0\\). The Chern number is constant on each gapped interval by homotopy invariance. Evaluating the degree of the map \\(\widehat{\mathbf d}\\), or summing the oriented contributions of the four lattice Dirac points, yields the stated values. The transition jumps are the differences of the adjacent values and agree with the sum of the local degeneracy charges. \\(\square\\)

The theorem is a genuine classification result for a specified Hamiltonian family. Its arithmetic content is exact but family-specific.

### 5.5 What this model proves about arithmetic topology

The model supports four conclusions.

First, topological transitions are discrete events in parameter space even though the Hamiltonian varies continuously.

Second, transition jumps are sums of local integer charges.

Third, the multiplicity and symmetry relations of degeneracies can determine whether a transition changes \\(C\\) by one unit or several units.

Fourth, a numerical pattern among transition jumps becomes a theorem only when the degeneracy structure and its charge relations are derived from the Hamiltonian.

The model does not establish that Chern numbers must be prime, square-free, bounded, or restricted to special congruence classes. Nor does it establish that the divisor function, Möbius function, or another classical arithmetic function predicts topological phases. Such claims require an additional theorem connecting the arithmetic function to a defined physical structure.

## 6. A General Classification Theorem for Hamiltonian Families

The preceding example motivates a broader theorem that separates what follows from topology from what must be proved about the model.

Let \\(\mathcal F\\) be a specified family of smooth Bloch Hamiltonians on \\(\mathbb T^2\\), with a fixed number of occupied bands and a fixed symmetry and locality class. Let \\(\mathcal F\_{\mathrm{gap}}\\) denote its gapped members.

### 6.1 Theorem 6.1 — Classification by connected gapped components

Suppose:

1. the occupied subspace is separated by a nonzero gap throughout each path considered;
2. the occupied projectors vary smoothly along those paths;
3. the symmetry and band-filling conditions defining the family remain fixed;
4. the first Chern number is defined using the occupied projector.

Then the Chern-number map

\\[ C:\mathcal F\_{\mathrm{gap}}\to\mathbb Z \\]

is constant on every path-connected component of \\(\mathcal F\_{\mathrm{gap}}\\). Consequently, distinct values of \\(C\\) label distinct path-connected gapped sectors, although equal values need not imply that two Hamiltonians are connected within the chosen family.

Proof. Let \\(H_0,H_1\\) lie in the same path-connected component. By definition there exists a continuous path \\(H_s\\) within the gapped family joining them. Smoothness of the occupied projector gives a homotopy of the occupied bundle over the Brillouin torus. The first Chern class is invariant under bundle isomorphism induced by homotopy. Therefore \\(C(H_0)=C(H_1)\\). \\(\square\\)

This theorem is general, but it does not by itself produce an arithmetic restriction beyond integer-valuedness. The image

\\[ \mathcal C(\mathcal F) = C(\mathcal F\_{\mathrm{gap}}) \subseteq\mathbb Z \\]

may be all of \\(\mathbb Z\\), a finite subset, or a more restricted set. Determining which requires analysis of \\(\mathcal F\\).

### 6.2 Theorem 6.2 — Conditional divisibility of topological transitions

Let \\(H(\mathbf k;\lambda)\\) be a smooth one-parameter family with gapped endpoints and finitely many isolated gap closings in between. Suppose the degeneracies are partitioned into complete groups \\(G\_\alpha\\), and each group has total oriented charge

\\[ Q(G\_\alpha)=\sum\_{j\in G\_\alpha}Q_j\in q\mathbb Z \\]

for some fixed positive integer \\(q\\). Then

\\[ C(\lambda\_+)-C(\lambda\_-)\in q\mathbb Z. \\]

Proof. By Theorem 4.1,

\\[ C(\lambda\_+)-C(\lambda\_-) =\sum\_\alpha Q(G\_\alpha). \\]

Each term belongs to \\(q\mathbb Z\\) by hypothesis, and \\(\mathbb Z\\) is closed under addition. Hence the sum belongs to \\(q\mathbb Z\\). \\(\square\\)

The theorem gives an explicit route from local structure to arithmetic. But the substantive burden is in the hypothesis: one must derive why all allowed degeneracy groups have total charge divisible by \\(q\\). The theorem does not create that restriction on its own.

### 6.3 A precise definition of an arithmetic topological law

For this paper, an arithmetic topological law is a statement of the form

\\[ \mathcal A\big(C_1,\ldots,C_s;\theta\big)=0 \\]

or

\\[ \Delta C\in S\_\theta\subsetneq\mathbb Z, \\]

where:

- \\(C_i\\) are well-defined topological invariants;
- \\(\theta\\) denotes explicitly stated physical or mathematical data, such as symmetry representations or hopping constraints;
- the admissible set \\(S\_\theta\\) is fixed independently of the observed output;
- the relation follows from the stated assumptions;
- the law remains valid throughout the claimed model class.

A restriction such as \\(\Delta C\in 2\mathbb Z\\) is meaningful only if \\(2\mathbb Z\\) is derived as a consequence of the allowed crossing structure. A relation that merely describes a finite set of numerically sampled models is an empirical regularity, not yet a theorem.

## 7. Beyond the Chern Number: Arithmetic Relations Among Invariants

The Chern number is only one possible integer-valued descriptor of a quantum phase. A richer arithmetic topology would investigate relations among several invariants, while preserving the distinction between independent classification data and quantities that are mathematically dependent.

### 7.1 Multiple occupied bands and additivity

For two isolated occupied bundles \\(E\\) and \\(F\\), the first Chern class obeys

\\[ c_1(E\oplus F)=c_1(E)+c_1(F). \\]

Thus, when the occupied space decomposes into smooth invariant subbundles,

\\[ C\_{\mathrm{tot}}=\sum_a C_a. \\]

This is an exact additive law. It is not an additional arithmetic restriction on the possible integers: without further assumptions, the summands can vary across the available classification space.

A genuine new constraint would require a reason that the \\(C_a\\) cannot vary independently. Such a reason might be a symmetry relating the subbundles, a conserved quantum number, a representation constraint, or a structural condition on the Hamiltonian.

### 7.2 Symmetry indicators and congruence relations

Crystalline symmetries can constrain the relationship between a Chern number and symmetry eigenvalues at high-symmetry momenta. In appropriate rotation-symmetric systems, for example, a Chern number modulo a symmetry-dependent integer can be related to products of rotation eigenvalues at invariant momenta.

Schematically, one may encounter a relation of the form

\\[ e^{2\pi i C/n}=\mathcal R, \\]

where \\(n\\) is determined by the relevant rotational symmetry and \\(\mathcal R\\) is constructed from the appropriate symmetry representations. This schematic expression is not a universal formula: the actual relation depends on the symmetry group, its action on the Bloch states, occupied-band representations, and the convention for the symmetry indicator.

The arithmetic information is a congruence class, not necessarily the complete integer. Knowing \\(C\bmod n\\) does not determine \\(C\\) uniquely because

\\[ C\quad\text{and}\quad C+kn \\]

have the same residue for any \\(k\in\mathbb Z\\).

This is an important model for a rigorous arithmetic-topological result. A symmetry constraint can yield a modular relation, but it must be derived for a specified symmetry setting and cannot be generalized merely by observing similar residues in unrelated systems.

### 7.3 Winding numbers, parity, and classification changes

Other symmetry classes can admit invariants different from the Chern number. Depending on dimension and symmetry, these may be winding numbers, \\(\mathbb Z_2\\) indices, or combinations of integer and torsion-valued invariants.

A \\(\mathbb Z_2\\) invariant is arithmetic in the elementary sense that it distinguishes parity classes, but it does not imply that the Chern number of a class-A model is restricted to even or odd values. A parity relation requires a theorem linking the two classifications under a specified symmetry and construction.

Similarly, the presence of a chiral symmetry can permit a winding-number description in settings where the Chern number alone is not the appropriate invariant. A valid arithmetic classification must therefore begin by identifying the symmetry class and the correct classifying space, rather than treating every topological integer as interchangeable.

### 7.4 Prime factorization and divisor functions: a test for relevance

Suppose a proposed theory assigns to each phase a Chern number \\(C\\) and then introduces an arithmetic function such as

\\[ \tau(|C|),\qquad \mu(|C|),\qquad \varphi(|C|), \\]

where \\(\tau\\) is the divisor-counting function, \\(\mu\\) is the Möbius function, and \\(\varphi\\) is Euler's totient function. These expressions are mathematically well-defined for suitable integer arguments, but their existence alone does not create a physical law.

Several issues must be addressed.

- At \\(C=0\\), the ordinary finite divisor-counting interpretation of \\(\tau(|C|)\\) is not applicable in the same way as for positive integers. A proposed invariant must define its zero case.
- The sign of \\(C\\) can encode orientation or Hall-response sign. Replacing \\(C\\) by \\(|C|\\) discards that information.
- The value of an arithmetic function may depend strongly on the integer's factorization without corresponding to any independent property of the quantum state.
- If the same data are used both to invent the arithmetic function and to claim its predictive success, the resulting fit is circular.

A nontrivial proposal would derive a physical quantity \\(O\\) satisfying, for example,

\\[ O(H)=f(C(H)) \\]

from a microscopic theory, symmetry principle, response formula, or independently testable theorem. Alternatively, it could predict that only a specific subset of Chern numbers is realizable under stated hypotheses. Without such a bridge, the arithmetic function is a relabeling, not a classifier.

## 8. The Finite-Range Problem: Can Locality Restrict the Integer Spectrum?

A particularly promising direction is to ask whether a fixed hopping range and a fixed number of orbitals impose restrictions on the attainable Chern numbers.

### 8.1 Bloch Hamiltonians as finite Fourier series

For a lattice model with finite-range hopping, the Bloch Hamiltonian is a finite Fourier sum,

\\[ H(\mathbf k)=\sum\_{\mathbf R\in\mathcal S} T\_{\mathbf R}e^{i\mathbf k\cdot\mathbf R}, \\]

where \\(\mathcal S\subset\mathbb Z^2\\) is a finite set of allowed displacement vectors and Hermiticity requires

\\[ T\_{-\mathbf R}=T\_{\mathbf R}^{\dagger}. \\]

For a two-band traceless Hamiltonian,

\\[ H(\mathbf k)=\mathbf d(\mathbf k)\cdot\boldsymbol\sigma, \\]

the components of \\(\mathbf d\\) are trigonometric polynomials determined by the hopping support \\(\mathcal S\\). The Chern number is the degree of the normalized map

\\[ \widehat{\mathbf d}:\mathbb T^2\to S^2, \\]

provided \\(\mathbf d(\mathbf k)\ne0\\) everywhere.

This formulation turns the problem into one about the possible degrees of maps induced by constrained trigonometric polynomials.

### 8.2 A precise research question

Fix:

- the number of bands \\(N\\);
- the hopping support \\(\mathcal S\\);
- the symmetry constraints on the matrices \\(T\_{\mathbf R}\\);
- the occupied-band rank;
- and any normalization or coefficient restrictions.

Let \\(\mathcal F(N,\mathcal S,\mathcal G)\\) be the resulting family, where \\(\mathcal G\\) denotes the specified symmetry data. Determine

\\[ \mathcal C(N,\mathcal S,\mathcal G) = \\{C(H):H\in\mathcal F(N,\mathcal S,\mathcal G), \ H\text{ gapped}\\}. \\]

There are several possible outcomes:

1. every integer is attainable;
2. only a subset of integers is attainable;
3. the set is bounded for the fixed hopping support;
4. a congruence restriction holds;
5. the answer depends on symmetry or the number of orbitals;
6. the set changes when coefficients are restricted to a special arithmetic domain.

Each outcome would be mathematically informative. In particular, a bound or congruence that holds for an entire family would be a genuine family-level classification theorem.

### 8.3 Why a finite hopping range is not itself an arithmetic law

The finite Fourier representation constrains the functional form of the Hamiltonian. But one cannot infer a specific Chern-number bound merely by counting Fourier coefficients. The degree of the map depends on the joint zeros and orientations of the components, and the gap condition excludes parameter values at which \\(\mathbf d=0\\).

Any claimed upper bound must be proved from the chosen support, coefficient space, and nonvanishing condition. A numerical scan may identify candidate extremal values, but it cannot certify a global bound over a continuous parameter space.

An exact approach could proceed by algebraically characterizing the gap-closing set, partitioning the coefficient space into gapped components, and evaluating the degree on one representative of each component. For polynomial or rational parameterizations, tools from real algebraic geometry may assist with the parameter-space decomposition. The final topological conclusion must still be established by a valid degree or bundle argument.

### 8.4 Coefficient arithmetic versus physical arithmetic

If hopping amplitudes are restricted to integers or rational numbers, arithmetic properties of the coefficients may influence the degeneracy locus. But this is not automatically a physical restriction. Real materials generally have effective hopping parameters that vary continuously under strain, gating, chemical substitution, and other perturbations.

A coefficient restriction is physically meaningful only if it follows from a microscopic construction, a quantization condition, a symmetry, or a controlled approximation. Otherwise, the integer or rational parameter domain is a mathematical choice that may be useful for a theorem but does not by itself describe the material's full accessible parameter space.

## 9. From Classification to a Concrete Material

A classification theorem becomes more compelling when it produces a testable consequence for an identifiable Hamiltonian or material family.

### 9.1 Minimal experimental setting

Consider a two-dimensional Chern-insulating system whose effective low-energy Hamiltonian is described by a finite number of bands and a tunable parameter \\(m\\). The parameter could be controlled by an applied field, gate voltage, strain, or composition, depending on the material.

The relevant observables are not limited to a computed Chern number. They may include:

- the bulk spectral gap;
- the location and multiplicity of gap-closing points;
- the quantized Hall conductance in a regime where the insulating and transport assumptions hold;
- edge-state spectral flow;
- and the response of the phase boundaries to symmetry-breaking perturbations.

For a noninteracting, charge-conserving two-dimensional insulator at zero temperature, with the Fermi energy in a bulk gap and the appropriate transport conditions, the Hall conductance is related to the occupied-band Chern number by

\\[ \sigma\_{xy}=C\frac{e^2}{h}, \\]

up to sign convention. This relation provides a bridge between a topological invariant and an experimentally accessible response. Disorder, interactions, finite temperature, and imperfect insulating behavior require a more careful treatment of the measured plateau and the conditions under which quantization is expected.

### 9.2 A proposed test for the two-band lattice family

For the Hamiltonian in Section 5, the model predicts three critical parameter values and the Chern sequence

\\[ 0\to +1\to -1\to 0. \\]

A concrete test would require identifying a material platform whose effective Hamiltonian is independently shown to approximate this family over the relevant parameter range. One would then test whether:

1. the bulk gap closes at the predicted critical values after parameters are calibrated independently;
2. the intervening insulating regimes exhibit the expected topological response;
3. the two simultaneous crossings at \\(m=0\\) are present within the model's symmetry assumptions;
4. a symmetry-breaking perturbation separates the crossings when the effective Hamiltonian predicts that it should;
5. the transition charges, inferred from Berry curvature or band-structure measurements, account for the observed change in the topological response.

The last two tests are particularly relevant to arithmetic topology. They examine whether the magnitude-two transition is a structural consequence of a paired degeneracy or an accidental coincidence that disappears under generic allowed perturbations.

This is a test program, not a claim that a specific material has already satisfied these conditions.

### 9.3 Distinguishing model predictions from material facts

A material's effective Hamiltonian may include additional bands, spin-orbit terms, disorder, interactions, and momentum-dependent couplings absent from the minimal two-band model. A material may therefore depart from the idealized phase diagram without contradicting the theorem for the idealized Hamiltonian.

To claim a material-level arithmetic law, the following chain must be established:

\\[ \text{microscopic model} \to \text{controlled effective Hamiltonian} \to \text{topological classification} \to \text{arithmetic restriction} \to \text{measurable consequence}. \\]

Each arrow has its own assumptions. If the effective Hamiltonian is only fitted to the observed phase boundaries, it cannot independently validate the same phase boundaries as predictions.

## 10. Numerical Verification and the Preprint Audit

Arithmetic topology is especially vulnerable to overinterpreting finite numerical datasets. A robust research program must separate numerical discovery from mathematical proof.

### 10.1 Numerical Chern-number computation

For a discretized Brillouin zone, a gauge-invariant lattice method can estimate the Chern number using link variables between neighboring occupied states. For a single occupied band, define normalized overlap links

\\[ U\_\mu(\mathbf k)= \frac{\langle u(\mathbf k)|u(\mathbf k+\Delta k\_\mu)\rangle} {|\langle u(\mathbf k)|u(\mathbf k+\Delta k\_\mu)\rangle|}, \\]

where the overlaps are nonzero. The oriented plaquette phase is

\\[ F\_{12}^{\mathrm{lat}}(\mathbf k) = \arg\\!\left[ U_1(\mathbf k) U_2(\mathbf k+\Delta k_1) U_1(\mathbf k+\Delta k_2)^{-1} U_2(\mathbf k)^{-1} \right]. \\]

The lattice estimate is

\\[ C\_{\mathrm{lat}}= \frac{1}{2\pi}\sum\_{\mathbf k} F\_{12}^{\mathrm{lat}}(\mathbf k), \\]

with consistent orientation and branch conventions. For multiple occupied bands, determinant links or an equivalent non-Abelian formulation should be used.

When the discretization resolves the Berry curvature and the system remains gapped, this method provides a practical numerical check. It is not a substitute for an exact proof of a proposed arithmetic relation across the entire model family.

### 10.2 A three-level verification protocol

Level I — Numerical evidence. Compute phase diagrams over the parameter domain, refine momentum meshes, track minimum gaps, and repeat with independent algorithms. Record numerical uncertainty and possible degeneracies near phase boundaries.

Level II — Analytic reconstruction. Solve the gap-closing equations, identify the degeneracies, derive their local effective Hamiltonians, and calculate their charges. Establish the exact phase boundaries and the Chern number in each region.

Level III — Family-wide theorem. Prove that every Hamiltonian satisfying the stated constraints obeys the claimed arithmetic restriction. The proof must cover all admissible coefficients and all possible degeneracies, including non-generic cases not encountered in a finite numerical scan.

A result should not be promoted from Level I to Level III simply because the numerical pattern persists over a larger sample.

### 10.3 Independent parameter counting

Suppose an arithmetic rule is inferred from a model containing several adjustable parameters. If each observed Chern jump is controlled by a separately chosen parameter, then the model may reproduce the dataset without explaining it.

The audit must ask:

- How many independent parameters define the admissible family?
- Which parameters are fixed by independent microscopic measurements?
- Which arithmetic predictions follow before the topological data are computed?
- Were any phase boundaries or transition charges used to choose the rule?
- Does the proposed restriction survive perturbations allowed by the theory?
- Can the rule predict a withheld transition or a new Hamiltonian in the same class?

Predictive compression is evidence of explanatory value only when the restrictions are derived independently of the outputs they purport to explain.

### 10.4 What constitutes a failed arithmetic hypothesis?

An arithmetic hypothesis is falsified within its stated domain if a valid counterexample satisfies all its assumptions but violates its predicted relation. Examples include:

- a permitted Hamiltonian with \\(\Delta C\notin q\mathbb Z\\), contradicting a claimed divisibility law;
- a symmetry-compatible isolated degeneracy that invalidates the proposed orbit-charge argument;
- a gapped model whose Chern number lies outside a claimed family-wide set;
- or a material realization that robustly violates a claimed universal relation after the effective-model assumptions have been checked.

Conversely, failure of an approximate material model does not necessarily falsify a theorem restricted to an idealized Hamiltonian. The domain of validity must be fixed before testing.

## 11. Interacting Systems and the Limits of Band Arithmetic

The preceding classification is formulated primarily for noninteracting Bloch Hamiltonians. Interacting systems require additional care because the many-body ground state may not be represented by a set of occupied single-particle bands.

### 11.1 Many-body topological response

For suitable interacting systems with conserved charge, a quantized Hall response can be characterized through many-body methods, including twisted boundary conditions on a torus. Let \\((\theta_x,\theta_y)\\) denote boundary-condition phases. If the many-body ground state remains unique and gapped over the twist-angle torus, its Berry curvature can define a many-body Chern number,

\\[ C\_{\mathrm{MB}}= \frac{1}{2\pi}\int_0^{2\pi}\\!\\!\int_0^{2\pi} F\_{\theta_x\theta_y}\\, d\theta_x\\,d\theta_y. \\]

Under the required smoothness, gap, and uniqueness assumptions, this is an integer. The construction generalizes the bundle-theoretic logic of band Chern numbers, but the underlying bundle is now built from many-body ground states.

The integer response alone does not determine the full interacting phase. Distinct phases can share the same Hall conductance, and intrinsic topological order can introduce fractionalized excitations and ground-state degeneracy that require more information than a single integer.

### 11.2 Fractional response is not a contradiction

In fractional quantum Hall phases, a measured Hall conductance can be a rational multiple of \\(e^2/h\\). This does not contradict the integrality of the first Chern number in the simple nondegenerate line-bundle setting. The many-body structure, degeneracy, and response formula differ from the assumptions used in that elementary construction.

A proposed arithmetic classification of interacting phases must specify whether its invariants belong to:

- a single-particle occupied bundle;
- a nondegenerate many-body ground-state bundle;
- a ground-state subspace of dimension greater than one;
- a response theory with topological order;
- or another well-defined mathematical object.

Without this specification, comparing an integer band invariant with a fractional response coefficient can produce false contradictions.

### 11.3 Green-function invariants and their caveats

For interacting systems, topological indices may sometimes be expressed through the single-particle Green function. Such formulations require hypotheses concerning analyticity, singularities, and the relevant symmetry class. Green-function zeros, poles, and interaction-driven changes can complicate a naive identification between a band-theoretic invariant and an observable.

Therefore, arithmetic relations that hold for noninteracting Bloch Hamiltonians should not be transferred to interacting systems without an explicit extension theorem.

## 12. Open Problems and Conjectures

The following questions define a research agenda. They are not asserted as established laws.

### 12.1 Conjecture A — Restricted-hopping Chern spectrum

For fixed band number, hopping support, and symmetry data, the attainable Chern numbers may form a restricted subset of \\(\mathbb Z\\), with the restriction determined by the allowed degeneracy structure and the degree of the associated map.

Required proof: characterize the full gapped parameter space and show that no admissible Hamiltonian realizes a value outside the proposed set.

### 12.2 Conjecture B — Symmetry-orbit divisibility

In selected symmetry-constrained families, every generic topological transition may occur through complete degeneracy orbits whose total charge is divisible by a fixed integer \\(q\\). If proved, this would enforce

\\[ \Delta C\in q\mathbb Z \\]

for transitions that satisfy the specified orbit assumptions.

Required proof: derive the local charge transformation under each symmetry, analyze symmetry-fixed degeneracies separately, and establish that all allowed gap closings have been covered.

### 12.3 Conjecture C — Arithmetic structure in multi-invariant phase spaces

For certain multiband families, symmetry indicators and integer topological invariants may obey relations that reduce the admissible invariant tuples to a proper subset of the naive product classification space.

Required proof: define the relevant invariants and classification group, derive the relation from the symmetry representation or classifying-space map, and determine whether the relation is complete or merely necessary.

### 12.4 Conjecture D — Predictive arithmetic signatures of material families

A restricted family of experimentally realizable Hamiltonians may exhibit stable arithmetic patterns in phase-transition sequences that are predictable from independently determined microscopic constraints.

Required test: identify a material family, derive the effective Hamiltonian and restriction before examining the full transition sequence, and test the resulting prediction on withheld control parameters or related samples.

### 12.5 Conjecture E — Arithmetic functions as response classifiers

There may exist settings in which an arithmetic function of topological invariants predicts a separately measurable response or a structural property of the phase.

Required proof: derive a relation such as \\(O(H)=f(C(H),\ldots)\\) from the microscopic or effective theory, establish gauge invariance and robustness under the claimed deformations, and show that the observable is not merely a restatement of the invariant.

The burden of proof is especially high for this conjecture. Prime-factorization patterns or divisor functions should be introduced only when a physical derivation motivates them.

## 13. A Program for Proving New Arithmetic Restrictions

A productive research program should proceed in a fixed order.

### Step 1 — Fix the classification problem

Specify the symmetry class, number of bands, occupied rank, locality assumptions, parameter domain, and equivalence relation. State exactly which topological invariants are under investigation.

### Step 2 — Define the admissible family independently

Write the Hamiltonian in a form that exposes its allowed terms, for example,

\\[ H(\mathbf k;\boldsymbol\theta) = \sum\_{\mathbf R\in\mathcal S} T\_{\mathbf R}(\boldsymbol\theta) e^{i\mathbf k\cdot\mathbf R}. \\]

Identify which coefficients are free, which are constrained, and which are fixed by independent physical input.

### Step 3 — Derive the gap-closing locus

Solve

\\[ \det\big(H(\mathbf k;\boldsymbol\theta)-E_F I\big)=0 \\]

together with the conditions needed for a closing of the relevant occupied–unoccupied gap. Determine whether the degeneracies are isolated, symmetry-related, higher-order, or extended.

### Step 4 — Compute local charges

Near each isolated degeneracy, derive the effective Hamiltonian and calculate its charge. Where the crossing is not linear, use the degree of the normalized map or another appropriate local invariant rather than assuming a unit Dirac charge.

### Step 5 — Establish the arithmetic statement

Use the degeneracy classification to prove a bound, congruence, divisibility condition, or relation among invariants. The arithmetic statement should be explicit enough that a counterexample can be constructed if it is false.

### Step 6 — Establish completeness

Show that all allowed degeneracies and all connected gapped components have been included. Treat boundary points, symmetry-fixed points, non-generic parameter values, and possible changes in the model's symmetry class.

### Step 7 — Derive an observable consequence

Connect the invariant to a measurable response or a distinctive spectral feature. State the conditions under which the correspondence holds and the experimental precision needed to distinguish the predicted alternatives.

### Step 8 — Test out of sample

Apply the theorem to Hamiltonians, parameter regions, or material samples not used to discover the arithmetic relation. If the law is claimed to be universal within a class, seek counterexamples across that class rather than merely confirming additional examples.

This sequence makes the epistemic distinction operational: numerical patterns can guide the discovery of hypotheses, but only explicit assumptions and a complete proof can elevate them to classification laws.

## 14. Conclusions

The arithmetic topology of quantum phases is a viable research direction, but its mathematical content must be distinguished from the mere observation that topological invariants are integers.

The Chern number

\\[ C=\frac{1}{2\pi}\int\_{\mathrm{BZ}}\Omega(\mathbf k)\\,d^2k \\]

is an integer because it represents the first Chern class of the occupied-state bundle. Its stability under gapped deformation is a theorem. Its change at isolated band degeneracies is controlled by the integer charges of those degeneracies. These are established structural results, not conjectures.

The additional arithmetic problem is to determine whether microscopic constraints, symmetry representations, hopping restrictions, or the topology of a Hamiltonian family force the invariant to lie in a smaller subset of the integers or force transition charges to obey divisibility or congruence relations.

The two-band lattice model studied here provides a concrete example. Its Chern numbers are \\(0,+1,-1,0\\) across the four gapped parameter regions, with transition jumps \\(+1,-2,+1\\). The central jump of magnitude two arises from two simultaneous degeneracies. It is not a universal rule for Chern insulators; it is a consequence of the model's specific gap-closing structure.

The general theorems established in this paper provide the framework for stronger results:

- the Chern number is constant on each path-connected gapped component of a specified Hamiltonian family;
- the change in Chern number equals the sum of the oriented charges of intervening isolated degeneracies;
- if the admissible degeneracy groups have total charges divisible by \\(q\\), the corresponding transition satisfies \\(\Delta C\in q\mathbb Z\\).

The third statement is the essential bridge between topology and arithmetic. Its value lies not in the elementary divisibility conclusion but in the task of deriving the charge restriction from an explicit physical or mathematical mechanism.

The proposed research program is therefore precise: characterize a restricted Hamiltonian family, derive its complete gap-closing structure, calculate the allowed local charges, prove a family-wide arithmetic restriction, and identify an independent experimental consequence. A successful result would explain why certain topological integers or transition sequences are allowed and others are forbidden—not merely recognize a pattern after the calculation.

Final epistemic status: The topological classification and transition-charge framework are established under the stated hypotheses. The two-band model supplies an exact example of family-specific transition arithmetic. Whether new, predictive arithmetic laws classify broader families of topological materials remains an open research problem. No universal prime-factorization law, divisor-function classifier, or additional restriction on Chern numbers has been established here.

## References

1. M. Nakahara, Geometry, Topology and Physics, 2nd ed., Taylor & Francis, 2003.
2. M. V. Berry, “Quantal Phase Factors Accompanying Adiabatic Changes,” Proceedings of the Royal Society A 392, 45–57 (1984).
3. D. J. Thouless, M. Kohmoto, M. P. Nightingale, and M. den Nijs, “Quantized Hall Conductance in a Two-Dimensional Periodic Potential,” Physical Review Letters 49, 405–408 (1982).
4. M. Kohmoto, “Topological Invariant and the Quantization of the Hall Conductance,” Annals of Physics 160, 343–354 (1985).
5. X.-L. Qi, Y.-S. Wu, and S.-C. Zhang, “Topological Quantization of the Spin Hall Effect in Two-Dimensional Paramagnetic Semiconductors,” Physical Review B 74, 085308 (2006).
6. M. Z. Hasan and C. L. Kane, “Colloquium: Topological Insulators,” Reviews of Modern Physics 82, 3045–3067 (2010).
7. X.-L. Qi and S.-C. Zhang, “Topological Insulators and Superconductors,” Reviews of Modern Physics 83, 1057–1110 (2011).
8. C.-K. Chiu, J. C. Y. Teo, A. P. Schnyder, and S. Ryu, “Classification of Topological Quantum Matter with Symmetries,” Reviews of Modern Physics 88, 035005 (2016).
9. B. Bradlyn et al., “Topological Quantum Chemistry,” Nature 547, 298–305 (2017).
10. H. C. Po, A. Vishwanath, and H. Watanabe, “Symmetry-Based Indicators of Band Topology in the 230 Space Groups,” Nature Communications 8, 50 (2017).
11. T. Fukui, Y. Hatsugai, and H. Suzuki, “Chern Numbers in Discretized Brillouin Zone: Efficient Method of Computing Spin Hall Conductances,” Journal of the Physical Society of Japan 74, 1674–1677 (2005).
12. N. R. Cooper, J. Dalibard, and I. B. Spielman, “Topological Bands for Ultracold Atoms,” Reviews of Modern Physics 91, 015005 (2019).

These references establish the topological, band-theoretic, symmetry-classification, and numerical foundations used here. The proposed broader arithmetic classification remains a research program rather than an established consequence of those works.

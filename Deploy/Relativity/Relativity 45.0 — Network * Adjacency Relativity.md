# Relativity 45.0 — Network / Adjacency Relativity  
## Relations Before Nodes and the Emergence of Objects from Invariant Network Structure

**White paper / academic preprint**

---

## Abstract

Network / Adjacency Relativity is the hypothesis that adjacency, connectivity, and even nodes are not fundamental ingredients of reality. They are emergent, frame-relative presentations of deeper relational invariants. A network is often represented by a graph \(G=(V,E)\) and an adjacency matrix \(A\), but the physical content does not reside in the labels of nodes or in a particular adjacency presentation. It resides in invariant relational structure: spectra, homology, causal order, entanglement pattern, automorphism structure, and dynamical coherence. Different graphs may be dual descriptions of the same relational structure,

\[
G
\sim
G',
\]

and physical objectivity lies in the equivalence class of such descriptions. The central principle is:

\[
\boxed{
\text{Relations precede nodes; objects emerge from invariant network structure.}
}
\]

Spacetime points, particles, fields, and observers are not primitive nodes in a fundamental graph. They are stable patterns, motifs, excitations, or substructures within a deeper relational network. Network / Adjacency Relativity unifies graph theory, spectral geometry, algebraic topology, causal-set theory, spin networks, tensor networks, holographic entanglement, and relational ontology into a single framework. It implies that the question “What are the fundamental things?” should be replaced by the question “What invariant relational structure gives rise to thing-like patterns?”

---

## 1. Introduction

Physics has often been imagined as a theory of things.

Atoms. Particles. Fields. Strings. Qubits. Nodes.

But each time physics has looked deeper, the “things” have dissolved into relations.

Particles became excitations of fields. Fields became gauge-equivalence classes. Spacetime points became relational coincidences. Quantum information became entanglement structure. Holography suggested that bulk geometry emerges from boundary correlations.

Network / Adjacency Relativity takes the next step.

It says that even networks should not be understood as collections of fundamental nodes connected by fundamental edges.

A network is a presentation of relational structure.

The nodes are not primary. The adjacency matrix is not primary. The graph drawing is not primary.

What is primary is the invariant relational pattern.

Nodes emerge as stable positions in that pattern.

Thus:

\[
\boxed{
\text{Relations precede nodes.}
}
\]

This is Network / Adjacency Relativity.

---

## 2. The Classical Picture: Nodes and Edges

A graph is usually defined as a pair,

\[
G=(V,E),
\]

where:

- \(V\) is a set of nodes,
- \(E\subseteq V\times V\) is a set of edges.

For a finite graph with \(N\) nodes, the adjacency matrix is

\[
A_{ij}
=
\begin{cases}
1, & i\sim j,\\
0, & i\not\sim j.
\end{cases}
\]

For weighted graphs,

\[
A_{ij}
=
w_{ij}.
\]

The degree of node \(i\) is

\[
d_i
=
\sum_j A_{ij}.
\]

This representation is useful.

But it is not ontologically fundamental.

The labels \(i,j\) are arbitrary. The node set is a basis. The adjacency matrix is a coordinate representation of relational structure.

Network / Adjacency Relativity says:

\[
\boxed{
\text{The adjacency matrix is a coordinate system for relations.}
}
\]

---

## 3. Graph Isomorphism and Relational Invariance

Two graphs \(G\) and \(G'\) are isomorphic if there exists a bijection,

\[
\phi:V(G)\to V(G'),
\]

such that

\[
i\sim j
\quad
\Longleftrightarrow
\quad
\phi(i)\sim\phi(j).
\]

In matrix form, there exists a permutation matrix \(P\) such that

\[
A'
=
PAP^T.
\]

Isomorphic graphs are not two different relational structures.

They are the same structure with different node labels.

Thus:

\[
G\cong G'
\quad
\Rightarrow
\quad
\text{same physical network}.
\]

This is the first lesson of Network Relativity.

Node labels are gauge.

---

## 4. Invariant Network Structure

Physical content lies in invariants under graph isomorphism and, more generally, under admissible dualities.

Important invariants include:

1. degree sequence,
2. adjacency spectrum,
3. Laplacian spectrum,
4. automorphism group,
5. connectivity and cut structure,
6. homology,
7. persistent homology,
8. causal order,
9. entanglement pattern,
10. community structure,
11. motif distribution,
12. graph entropy,
13. diffusion behavior,
14. spectral dimension.

No single invariant is always sufficient.

For example, two non-isomorphic graphs can be cospectral: they share the same adjacency spectrum.

Thus the full invariant structure is richer than any single number or spectrum.

The physical network is the equivalence class,

\[
[G],
\]

under all admissible relational equivalences.

---

## 5. The Laplacian and Spectral Geometry

The graph Laplacian is

\[
L
=
D-A,
\]

where \(D\) is the degree matrix,

\[
D_{ij}
=
d_i\delta_{ij}.
\]

The normalized Laplacian is

\[
\mathcal{L}
=
I-D^{-1/2}AD^{-1/2}.
\]

The eigenvalues of \(L\) satisfy

\[
0=\lambda_0
\leq
\lambda_1
\leq
\cdots
\leq
\lambda_{N-1}.
\]

The first nonzero eigenvalue \(\lambda_1\) is the spectral gap.

It controls connectivity, mixing, and diffusion.

The heat kernel on the graph is

\[
K(t)
=
e^{-tL}.
\]

The return probability is

\[
P(t)
=
\frac{1}{N}
\operatorname{Tr}
e^{-tL}.
\]

The spectral dimension is

\[
d_s(t)
=
-2
\frac{d\ln P(t)}{d\ln t}.
\]

Thus geometry can be extracted from relational diffusion.

This is a precise example of the principle:

\[
\boxed{
\text{Geometry emerges from relational spectra.}
}
\]

---

## 6. Homology and Topological Invariants

A graph can be thickened into a simplicial complex.

For example, the clique complex associates:

- nodes to vertices,
- edges to pairs,
- triangles to cliques of three,
- tetrahedra to cliques of four,
- and so on.

The boundary operator satisfies

\[
\partial_{k-1}\partial_k=0.
\]

The \(k\)-th homology group is

\[
H_k
=
\frac{\ker\partial_k}{\operatorname{im}\partial_{k+1}}.
\]

The Betti numbers are

\[
\beta_k
=
\dim H_k.
\]

They count:

- \(\beta_0\): connected components,
- \(\beta_1\): loops,
- \(\beta_2\): voids,
- and higher-dimensional holes.

Persistent homology studies how these features persist across scales.

Thus topology itself can be understood as invariant relational structure.

---

## 7. Causal Structure as Primitive Adjacency

In causal-set theory, the fundamental structure is not a graph of symmetric adjacency but a partial order.

A causal set is a pair,

\[
(C,\prec),
\]

where \(\prec\) is a partial order satisfying local finiteness.

The relation

\[
x\prec y
\]

means that \(x\) can causally influence \(y\).

Adjacency is replaced by causal precedence.

A link is an irreducible causal relation:

\[
x\prec y
\]

with no \(z\) such that

\[
x\prec z\prec y.
\]

The causal set program proposes:

\[
\boxed{
\text{Order plus number equals geometry.}
}
\]

Spacetime volume is counted by the number of causal-set elements.

Causal structure and counting together approximate Lorentzian geometry.

Thus adjacency is not fundamental. Causal relation is deeper.

---

## 8. Entanglement Graphs and Holographic Connectivity

In quantum information, adjacency can be defined by entanglement.

Let a system be divided into subsystems \(A_i\).

Define a weighted entanglement graph with edge weights,

\[
w_{ij}
=
I(A_i:A_j),
\]

where the mutual information is

\[
I(A_i:A_j)
=
S(A_i)+S(A_j)-S(A_i\cup A_j).
\]

Strong entanglement defines effective connectivity.

In holography, bulk geometry is related to boundary entanglement.

The Ryu–Takayanagi formula states,

\[
S(A)
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

Thus geometric area is entanglement entropy.

Bulk adjacency is not fundamental. It emerges from entanglement structure.

This is one of the strongest examples of Network / Adjacency Relativity.

---

## 9. Tensor Networks as Relational Geometry

Tensor networks represent quantum states as graphs of contracted tensors.

A tensor-network state has the form,

\[
\psi_{s_1\cdots s_N}
=
\sum_{\text{internal}}
\prod_v
T_v.
\]

The graph of tensors defines a relational geometry.

The bond dimension \(\chi\) controls entanglement.

Across a cut,

\[
S
\leq
\log\chi.
\]

MERA tensor networks produce hyperbolic geometries.

The radial direction of the network corresponds to scale.

Thus tensor networks show that geometry can be reconstructed from entanglement adjacency.

But again, the nodes of the tensor network are not necessarily fundamental substances.

They are part of a presentation.

The invariant is the entanglement and correlation structure.

---

## 10. Spin Networks and Quantum Geometry

In loop quantum gravity, quantum geometry is represented by spin networks.

A spin network is a graph \(\Gamma\) with:

- edges labeled by spins \(j_e\),
- nodes labeled by intertwiners \(i_v\).

The area operator has eigenvalues,

\[
A
=
8\pi\gamma\ell_{\text{P}}^2
\sum_e
\sqrt{j_e(j_e+1)}.
\]

The volume operator depends on intertwiners at nodes.

Thus geometry is quantized into relational network data.

The nodes are not spacetime points.

They are quanta of relational geometry.

Thus:

\[
\boxed{
\text{Spin-network nodes are not points. They are relational atoms of geometry.}
}
\]

---

## 11. Graph Dualities and Equivalence

Different graphs can represent the same relational physics.

Examples include:

1. graph isomorphism,
2. planar dual graphs,
3. line graphs,
4. graph Fourier duals,
5. tensor-network gauge redundancies,
6. spin-network recoupling moves,
7. Pachner moves in triangulations,
8. causal-set thickening,
9. entanglement-graph threshold duals,
10. holographic bulk-boundary duals.

Define graph equivalence as

\[
G\sim G'
\]

if there exists a duality preserving invariant relational structure:

\[
\mathcal{I}(G)
=
\mathcal{I}(G').
\]

Then physical reality is the equivalence class,

\[
[G].
\]

Thus:

\[
\boxed{
\text{Graphs are presentations; relational structure is physical.}
}
\]

---

## 12. Nodes as Emergent Objects

If nodes are not fundamental, what are they?

Nodes are emergent stable positions in relational structure.

They may arise as:

1. eigenvector localizations,
2. community centers,
3. topological defects,
4. persistent homology features,
5. automorphism orbits,
6. stable motifs,
7. attractors of network dynamics,
8. coarse-grained cells,
9. intertwiner nodes in spin networks,
10. tensor nodes in network contractions.

Thus a node is not a primitive thing.

It is a stable relational role.

This is the network version of Identity Relativity.

An object is not a node-substance.

It is an invariant pattern of relations.

---

## 13. Particles as Network Patterns

Particles may be understood as stable excitations of relational networks.

In lattice field theory, particles are modes of fields on a graph.

The graph Laplacian defines discrete wave equations.

Eigenmodes of the Laplacian behave like particle-like excitations.

In spin networks, particles may be defects or excitations of the network.

In tensor networks, particles may be localized perturbations of entanglement structure.

In causal sets, particles may be patterns in causal order.

Thus:

\[
\boxed{
\text{Particles are not nodes. They are stable relational excitations.}
}
\]

---

## 14. Spacetime as Emergent Network Geometry

Spacetime may be an emergent geometry of a deeper relational network.

At large scales, the network may approximate a manifold.

At small scales, it may be discrete, fractal, causal, or entanglement-based.

The effective metric may be reconstructed from:

1. causal order,
2. diffusion behavior,
3. entanglement entropy,
4. spectral dimension,
5. graph distance,
6. curvature estimators,
7. persistent topology.

Thus the metric is not fundamental.

It is a large-scale invariant of relational structure.

This connects Network / Adjacency Relativity to Scale Relativity and Dimensional Relativity.

---

## 15. Observers as Subnetworks

An observer is not an external node looking at the network.

An observer is a subnetwork with:

1. internal states,
2. records,
3. memory,
4. predictive models,
5. self-models,
6. causal access constraints.

An observer’s adjacency structure is inferred from correlations.

There may be a difference between:

1. structural adjacency,
2. causal adjacency,
3. functional adjacency,
4. inferred adjacency,
5. effective adjacency.

Thus adjacency is observer-relative.

What counts as connected may depend on resolution, interaction, and measurement context.

Thus:

\[
\boxed{
\text{Adjacency is not absolute. It is relational and observer-relative.}
}
\]

---

## 16. Network Dynamics

A relational universe may be described by dynamics of network structure.

Possible formulations include:

1. graph rewriting systems,
2. Hamiltonian dynamics on graph states,
3. quantum graphity models,
4. spin-foam histories,
5. group field theory,
6. tensor-model Feynman graphs,
7. causal-set growth processes,
8. dynamical triangulations,
9. tensor-network renormalization,
10. categorical process theories.

A path integral over networks may be written schematically as

\[
Z
=
\sum_G
\mu(G)
e^{iS[G]/\hbar}.
\]

In Euclidean form,

\[
Z
=
\sum_G
\mu(G)
e^{-S_E[G]}.
\]

The sum is over relational structures, not over fixed node sets.

Thus:

\[
\boxed{
\text{The fundamental path integral may be a sum over relational networks.}
}
\]

---

## 17. Categorical Formulation

Category theory gives a nodeless formulation.

A graph can be viewed as a category:

- objects are nodes,
- morphisms are paths.

But category theory emphasizes morphisms over objects.

The Yoneda lemma says that an object \(X\) is determined by its relations to all other objects:

\[
X
\cong
\mathrm{Hom}(-,X).
\]

Thus an object is not a primitive substance.

It is a relational profile.

Network / Adjacency Relativity generalizes this:

\[
\boxed{
\text{Nodes are determined by relational roles.}
}
\]

---

## 18. Network Relativity and Gauge

Graph labeling is gauge.

But gauge appears at deeper levels too.

In tensor networks, different contractions can represent the same state.

In spin networks, recoupling moves preserve quantum geometry.

In triangulations, Pachner moves preserve topology.

In gauge theory, different connections can represent the same physical field.

Thus network relativity is a generalized gauge principle.

The gauge is not merely local field redundancy.

It is relational redundancy.

Thus:

\[
\boxed{
\text{Network redundancy is gauge.}
}
\]

---

## 19. Network Relativity and Substance Relativity

Substance Relativity says that particles, fields, strings, and qubits are not fundamental substances.

Network / Adjacency Relativity gives this a precise relational form.

Substances are stable substructures in a network.

They are not nodes.

They are invariant patterns.

Thus:

\[
\text{substance}
\rightarrow
\text{stable relational motif}.
\]

---

## 20. Network Relativity and Algorithmic Substrate Relativity

Algorithmic / Substrate Relativity says that computational substrates are gauge.

Network / Adjacency Relativity says that network presentations are gauge.

These are complementary.

A computational substrate may be represented as a circuit graph, tensor network, cellular automaton, or categorical diagram.

If different network presentations efficiently preserve invariant structure, their differences are gauge.

Thus:

\[
\boxed{
\text{Substrate gauge and adjacency gauge are aspects of one relational principle.}
}
\]

---

## 21. Formal Framework

Let a relational structure be

\[
\mathcal{R}
=
\left(
X,
\{R_i\},
w,
\mathcal{D}
\right),
\]

where:

- \(X\) is a set of relational positions,
- \(R_i\) are relations,
- \(w\) are weights,
- \(\mathcal{D}\) is dynamics.

A graph \(G\) is a presentation of \(\mathcal{R}\).

Two presentations are equivalent if they preserve invariant structure:

\[
G\sim G'
\quad
\Longleftrightarrow
\quad
\mathcal{I}(G)=\mathcal{I}(G').
\]

Physical reality is the equivalence class,

\[
[\mathcal{R}].
\]

Nodes are basis choices within a presentation.

Thus:

\[
\boxed{
\text{Reality is relational equivalence class; nodes are presentation artifacts.}
}
\]

---

## 22. Axioms of Network / Adjacency Relativity

The framework may be organized around twelve axioms.

### Axiom 1: Relations Precede Nodes

Nodes are not primitive. They emerge from relations.

### Axiom 2: Adjacency Is Frame-Relative

Adjacency depends on scale, resolution, observer, and presentation.

### Axiom 3: Graph Labels Are Gauge

Node labels and graph drawings are not physical.

### Axiom 4: Invariants Are Physical

Spectra, topology, causality, entanglement, and dynamics are physical invariants.

### Axiom 5: Graph Equivalence Is Physical Equivalence

Dual graphs represent the same relational structure.

### Axiom 6: Objects Are Stable Patterns

Particles, observers, and spacetime points are stable relational patterns.

### Axiom 7: Geometry Emerges from Networks

Metric geometry is a large-scale invariant of relational structure.

### Axiom 8: Entanglement Defines Connectivity

Quantum connectivity is entanglement structure.

### Axiom 9: Causal Order Is Deeper Than Symmetric Adjacency

Causality may be more fundamental than graph adjacency.

### Axiom 10: Dynamics Is Relational Transformation

Physical evolution is transformation of relational structure.

### Axiom 11: Observers Are Subnetworks

Observers are internal relational patterns with self-models.

### Axiom 12: Reflexivity Is Required

Network relativity applies to its own network presentations.

---

## 23. Relation to Previous Relativities

Network / Adjacency Relativity integrates earlier relativities.

| Relativity | Contribution |
|---|---|
| General Relativity | Geometry is relational |
| Quantum Reference Frames | Observers are physical systems |
| Identity Relativity | Identity is structural role |
| Substance Relativity | Substances are effective patterns |
| Algorithmic Relativity | Substrates are gauge |
| Scale Relativity | Structure changes with resolution |
| Topological Relativity | Topology may be emergent |
| Network / Adjacency Relativity | Nodes and adjacency are emergent |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative frames}
\rightarrow
\text{relative substances}
\rightarrow
\text{relative substrates}
\rightarrow
\text{relative adjacency}.
\]

---

## 24. Scientific Status

Network / Adjacency Relativity is not a single empirical theory.

It is a meta-framework.

It is supported by:

1. spectral graph theory,
2. topological data analysis,
3. causal-set theory,
4. loop quantum gravity,
5. spin foams,
6. tensor networks,
7. holographic entanglement,
8. lattice field theory,
9. quantum graphity models,
10. network science,
11. categorical quantum mechanics.

It becomes scientifically powerful when applied to specific models with explicit invariants and dynamics.

It becomes vacuous if every graph is declared equivalent without demonstrating invariant preservation.

Thus the framework must be disciplined by mathematics and empirical constraints.

---

## 25. Open Problems

Several major problems remain.

### 25.1 Reconstruction

Can spacetime geometry be uniquely reconstructed from relational invariants?

### 25.2 Cospectral Ambiguity

Different graphs can share spectra. What additional invariants are required?

### 25.3 Quantum Graphs

How should superpositions of graphs be formulated?

### 25.4 Continuum Limit

How does smooth spacetime emerge from discrete relational networks?

### 25.5 Lorentz Invariance

Can discrete networks reproduce exact or effective Lorentz symmetry?

### 25.6 Locality

How does local adjacency emerge from nonlocal entanglement?

### 25.7 Dynamics

What is the correct action or Hamiltonian for relational networks?

### 25.8 Observers

How do observer-subnetworks infer adjacency without circularity?

### 25.9 Empirical Tests

Can network-relational quantum gravity yield testable predictions?

### 25.10 Reflexivity

Can the framework describe its own relational presentation without paradox?

---

## 26. What Einstein Would Think

Einstein would be sympathetic to Network / Adjacency Relativity.

His hole argument already showed that spacetime points lack individuality independent of fields.

General covariance says that coordinates are not physical.

Network relativity generalizes this:

\[
\text{Nodes are coordinates of relational structure.}
\]

Einstein might resist the idea that spacetime is fundamentally discrete or network-like.

But he would recognize the central principle:

\[
\boxed{
\text{Physical reality must be identified with invariant relational structure, not with arbitrary labels.}
}
\]

Network / Adjacency Relativity carries that principle to its logical conclusion.

---

## 27. Summary of Core Equations

### Graph

\[
G=(V,E).
\]

### Adjacency matrix

\[
A_{ij}
=
\begin{cases}
1, & i\sim j,\\
0, & i\not\sim j.
\end{cases}
\]

### Graph isomorphism

\[
A'
=
PAP^T.
\]

### Laplacian

\[
L=D-A.
\]

### Heat kernel

\[
K(t)=e^{-tL}.
\]

### Spectral dimension

\[
d_s(t)
=
-2
\frac{d\ln P(t)}{d\ln t}.
\]

### Homology

\[
H_k
=
\frac{\ker\partial_k}{\operatorname{im}\partial_{k+1}}.
\]

### Betti numbers

\[
\beta_k=\dim H_k.
\]

### Entanglement graph weight

\[
w_{ij}=I(A_i:A_j).
\]

### Ryu–Takayanagi formula

\[
S(A)
=
\frac{\operatorname{Area}(\gamma_A)}{4G_N\hbar}.
\]

### Spin-network area

\[
A
=
8\pi\gamma\ell_{\text{P}}^2
\sum_e
\sqrt{j_e(j_e+1)}.
\]

### Graph equivalence

\[
G\sim G'
\quad
\Longleftrightarrow
\quad
\mathcal{I}(G)=\mathcal{I}(G').
\]

### Central principle

\[
\boxed{
\text{Relations precede nodes; objects emerge from invariant network structure.}
}
\]

---

## 28. Conclusion

Relativity 45.0, Network / Adjacency Relativity, asserts that nodes and adjacency are not fundamental.

They are emergent presentations of deeper relational invariants.

A graph is not reality. It is a coordinate system for relations.

The physical content lies in spectra, topology, causal order, entanglement, dynamics, and equivalence classes of relational structure.

The central principle is:

\[
\boxed{
\text{Relations precede nodes; objects emerge from invariant network structure.}
}
\]

Spacetime points are not primitive nodes.

Particles are not primitive nodes.

Observers are not primitive nodes.

They are stable patterns in a deeper relational network.

This is Network / Adjacency Relativity.

---

## Appendix A: Graph Invariants

A graph invariant is a function \(I(G)\) satisfying

\[
G\cong G'
\quad
\Rightarrow
\quad
I(G)=I(G').
\]

Examples include:

\[
\text{spec}(A),
\quad
\text{spec}(L),
\quad
\beta_k,
\quad
\text{Aut}(G),
\quad
\text{diam}(G),
\quad
\chi(G).
\]

No single invariant is always complete.

Physical relational structure may require the full equivalence class.

---

## Appendix B: Spectral Dimension

The return probability is

\[
P(t)
=
\frac{1}{N}
\operatorname{Tr}
e^{-tL}.
\]

If

\[
P(t)\sim t^{-d_s/2},
\]

then \(d_s\) is the spectral dimension.

Thus diffusion on a network defines an effective geometry.

---

## Appendix C: Persistent Homology

Given a filtered family of complexes,

\[
K_0\subseteq K_1\subseteq\cdots\subseteq K_n,
\]

homology classes appear and disappear across scale.

The resulting barcodes or persistence diagrams encode scale-dependent topology.

Thus topology becomes scale-relative.

---

## Appendix D: Causal-Set Order

A causal set is a locally finite partial order,

\[
(C,\prec).
\]

The number of elements in a region corresponds to spacetime volume.

The order corresponds to causal structure.

Thus:

\[
\text{order}+\text{number}
\rightarrow
\text{geometry}.
\]

---

## Appendix E: Spin-Network Geometry

A spin network is a labeled graph,

\[
\Gamma=(V,E,j_e,i_v).
\]

Edges carry spins \(j_e\).

Nodes carry intertwiners \(i_v\).

Area eigenvalues are

\[
A
=
8\pi\gamma\ell_{\text{P}}^2
\sum_e
\sqrt{j_e(j_e+1)}.
\]

Thus geometry is encoded in relational network labels.

---

## Selected References

1. L. Euler, “Solutio Problematis ad Geometriam Situs Pertinentis,” *Commentarii Academiae Scientiarum Petropolitanae* **8**, 128 (1741).  
2. F. Harary, *Graph Theory* (Addison-Wesley, 1969).  
3. B. Bollobás, *Modern Graph Theory* (Springer, 1998).  
4. F. R. K. Chung, *Spectral Graph Theory* (American Mathematical Society, 1997).  
5. M. E. J. Newman, *Networks: An Introduction* (Oxford University Press, 2010).  
6. D. J. Watts and S. H. Strogatz, “Collective Dynamics of ‘Small-World’ Networks,” *Nature* **393**, 440 (1998).  
7. A.-L. Barabási and R. Albert, “Emergence of Scaling in Random Networks,” *Science* **286**, 509 (1999).  
8. L. Lovász, *Large Networks and Graph Limits* (American Mathematical Society, 2012).  
9. G. Carlsson, “Topology and Data,” *Bulletin of the American Mathematical Society* **46**, 255 (2009).  
10. H. Edelsbrunner and J. L. Harer, *Computational Topology: An Introduction* (American Mathematical Society, 2010).  
11. L. Bombelli, J. Lee, D. Meyer, and R. D. Sorkin, “Space-Time as a Causal Set,” *Physical Review Letters* **59**, 521 (1987).  
12. R. D. Sorkin, “Causal Sets: Discrete Gravity,” in *Lectures on Quantum Gravity* (World Scientific, 2005).  
13. R. Penrose, “Angular Momentum: An Approach to Combinatorial Space-Time,” in *Quantum Theory and Beyond* (Cambridge University Press, 1971).  
14. C. Rovelli and L. Smolin, “Spin Networks and Quantum Gravity,” *Physical Review D* **52**, 5743 (1995).  
15. J. C. Baez, “Spin Network States in Gauge Theory,” *Advances in Mathematics* **117**, 253 (1996).  
16. T. Thiemann, *Modern Canonical Quantum General Relativity* (Cambridge University Press, 2007).  
17. A. Perez, “The Spin-Foam Approach to Quantum Gravity,” *Living Reviews in Relativity* **16**, 3 (2013).  
18. D. Oriti, ed., *Approaches to Quantum Gravity* (Cambridge University Press, 2009).  
19. G. Vidal, “Entanglement Renormalization,” *Physical Review Letters* **99**, 220405 (2007).  
20. B. Swingle, “Entanglement Renormalization and Holography,” *Physical Review D* **86**, 065007 (2012).  
21. M. Van Raamsdonk, “Building Up Spacetime with Quantum Entanglement,” *General Relativity and Gravitation* **42**, 2323 (2010).  
22. F. Pastawski, B. Yoshida, D. Harlow, and J. Preskill, “Holographic Quantum Error-Correcting Codes,” *Journal of High Energy Physics* **1506**, 149 (2015).  
23. S. Ryu and T. Takayanagi, “Holographic Derivation of Entanglement Entropy from AdS/CFT,” *Physical Review Letters* **96**, 181602 (2006).  
24. J. Ambjørn, J. Jurkiewicz, and R. Loll, “Spectral Dimension of the Universe,” *Physical Review Letters* **95**, 171301 (2005).  
25. T. Konopka, F. Markopoulou, and S. Severini, “Quantum Graphity: A Model of Emergent Locality,” *Physical Review D* **77**, 104029 (2008).

# Relativity 30.0 — Complexity-Horizon Relativity  
## Computational Inaccessibility as a Physical Horizon

**White paper / academic preprint**

---

## Abstract

Complexity-Horizon Relativity proposes that horizons are not only causal, thermodynamic, or geometric. Some horizons are computational. A physical system may encode information in principle while rendering it inaccessible in practice because reconstructing that information requires computational resources that grow exponentially with entropy. For black holes, this suggests that the interior is not hidden merely by a causal event horizon but also by a complexity horizon: decoding interior information from exterior radiation may require time

\[
t_{\text{decode}}
\sim
e^{S},
\]

where \(S\) is the black-hole entropy. At the same time, holographic conjectures identify the growth of black-hole interiors with the growth of quantum computational complexity,

\[
\mathcal{C}(t)
\sim
t,
\]

over exponentially long times. Complexity becomes a physical coordinate, and the interior becomes an operationally protected region of encoded reality. The central principle is:

\[
\boxed{
\text{Some regions of reality are hidden not by distance, but by computational complexity.}
}
\]

Complexity-Horizon Relativity unifies black-hole interiors, holographic quantum error correction, scrambling, fast scrambling, the Hayden–Preskill mirror, the Harlow–Hayden decoding obstruction, complexity equals volume, complexity equals action, and the Lloyd bound into a single framework. It implies that the boundary between the physically real and the operationally accessible is not fixed by spacetime alone. It is fixed by computational feasibility.

---

## 1. Introduction

General relativity taught us that horizons are causal boundaries.

An event horizon separates events that can send signals to an observer from events that cannot. A black-hole horizon hides an interior from distant observers. A cosmological horizon limits what can ever be observed by an observer in an accelerating universe.

Thermodynamic relativity taught us that horizons are also entropy boundaries.

A horizon carries entropy,

\[
S
=
\frac{k_{\text{B}}A}{4G\hbar/c^3},
\]

and temperature,

\[
T
=
\frac{\hbar\kappa}{2\pi k_{\text{B}}c}.
\]

The horizon is not merely a geometric surface. It is a thermodynamic membrane.

Complexity-Horizon Relativity adds a third lesson:

\[
\boxed{
\text{Horizons can be computational.}
}
\]

Even when information is not destroyed, and even when it is encoded in accessible radiation, it may be impossible to reconstruct within any feasible amount of time or computational resources.

This changes the meaning of hiddenness.

A region may be hidden because:

1. it is outside the causal past,
2. it is beyond a thermodynamic horizon,
3. it is encoded in a code subspace whose decoding complexity is exponential,
4. its reconstruction requires operations saturating fundamental computational bounds.

The black-hole interior is the paradigmatic example.

---

## 2. Quantum Computational Complexity

Quantum computational complexity measures the difficulty of preparing a state or implementing a unitary operation.

Let \(U\) be a unitary operator acting on \(n\) qubits. Given a universal gate set \(\mathcal{G}\), the circuit complexity of \(U\) is the minimum number of gates required to approximate \(U\):

\[
\mathcal{C}(U)
=
\min
\left\{
N
\mid
U
\approx
G_N G_{N-1}\cdots G_1,
\;
G_i\in\mathcal{G}
\right\}.
\]

For a state \(\ket{\psi}\), one defines state complexity relative to a reference state \(\ket{0}\):

\[
\mathcal{C}(\ket{\psi})
=
\min
\left\{
\mathcal{C}(U)
\mid
U\ket{0}
\approx
\ket{\psi}
\right\}.
\]

Complexity is not entropy.

Entropy measures how many states are compatible with macroscopic data. Complexity measures how hard it is to construct a particular state or operation.

A thermal state may have maximal entropy but relatively low preparation complexity. A generic pure state may have both high entropy of subsystems and enormous complexity.

This distinction is central.

Black holes thermalize quickly, but their microscopic states continue to complexify for exponentially long times.

---

## 3. Nielsen Geometry and Continuous Complexity

Nielsen’s geometric formulation turns complexity into a geodesic problem.

Let \(U(s)\) be a continuous path in the unitary group with

\[
U(0)=I,
\qquad
U(1)=U.
\]

Define a time-dependent Hamiltonian \(H(s)\) by

\[
\frac{dU(s)}{ds}
=
-iH(s)U(s).
\]

One assigns a cost metric to Hamiltonians, penalizing nonlocal or difficult directions. The complexity of \(U\) is the length of the shortest path:

\[
\mathcal{C}(U)
=
\min_{U(s)}
\int_0^1 ds\,
F(H(s)),
\]

where \(F\) is a positive homogeneous cost function.

A simple quadratic choice is

\[
F(H)
=
\sqrt{
\sum_I q_I |h_I|^2
},
\]

where

\[
H
=
\sum_I h_I \sigma_I,
\]

and \(q_I\) are penalty factors.

The geometry of the unitary group then determines the growth of complexity.

In chaotic quantum systems, geodesics tend to diverge, and complexity grows linearly for long times.

---

## 4. Operator Complexity and Krylov Complexity

Complexity can also be assigned to operators.

In the Heisenberg picture, an initially simple operator evolves as

\[
O(t)
=
e^{iHt}
O
e^{-iHt}.
\]

Under time evolution, a simple local operator spreads over increasingly many degrees of freedom.

One measure is operator size:

\[
s(O(t))
=
\sum_s
s\,P_s(O(t)),
\]

where \(P_s\) is the weight of the operator on terms acting nontrivially on \(s\) qubits.

A more refined measure is Krylov complexity.

Given an initial operator \(O\), one constructs a Krylov basis using the Liouvillian superoperator

\[
\mathcal{L}(\cdot)
=
[H,\cdot].
\]

The evolved operator is expanded as

\[
O(t)
=
\sum_n
\phi_n(t) O_n.
\]

Krylov complexity is

\[
K(t)
=
\sum_n
n\,|\phi_n(t)|^2.
\]

In maximally chaotic systems, Krylov complexity can grow exponentially at early times:

\[
K(t)
\sim
e^{2\lambda t},
\]

and then saturate or grow linearly depending on the system.

Thus complexity captures the growth of nonlocality in operator space.

---

## 5. Scrambling and Fast Scramblers

A quantum system scrambles when initially localized information becomes delocalized over many degrees of freedom.

The scrambling time is the time required for information to become inaccessible to simple local measurements.

For a system with entropy \(S\), the fast-scrambling conjecture states that the minimum scrambling time is

\[
t_{\text{scr}}
\sim
\frac{\beta}{2\pi}
\log S,
\]

where

\[
\beta
=
\frac{1}{k_{\text{B}}T}
\]

is the inverse temperature.

Black holes are conjectured to be the fastest scramblers in nature.

Thus a black hole thermalizes and scrambles information in time

\[
t_{\text{scr}}
\sim
\frac{\hbar}{2\pi k_{\text{B}}T}
\log S.
\]

This is much shorter than the evaporation time but much longer than microscopic dynamical times.

Scrambling creates the first layer of hiddenness: information is not destroyed, but it is no longer locally accessible.

Complexity creates the second layer: even after information is encoded in radiation, decoding it may require exponential resources.

---

## 6. Entropy, Complexity, and the Arrow of Time

Entropy and complexity behave differently in time.

A closed quantum system evolving from a simple initial state typically shows:

1. rapid entropy growth of subsystems,
2. thermalization,
3. scrambling,
4. long-term complexity growth,
5. eventual complexity saturation,
6. Poincaré recurrence on exponentially long times.

Entropy may saturate at

\[
S_{\max},
\]

but complexity continues to grow until times of order

\[
t_{\text{sat}}
\sim
e^{S}.
\]

Thus complexity provides a finer arrow of time than entropy.

The thermodynamic arrow says:

\[
S(t)
\text{ increases}.
\]

The complexity arrow says:

\[
\mathcal{C}(t)
\text{ increases long after } S(t) \text{ has saturated}.
\]

Black-hole interiors appear to follow the complexity arrow.

---

## 7. Black-Hole Entropy and the Size of the Code

A black hole of horizon area \(A\) has entropy

\[
S_{\text{BH}}
=
\frac{k_{\text{B}}A}{4G\hbar/c^3}.
\]

In natural units,

\[
S_{\text{BH}}
=
\frac{A}{4G}.
\]

The number of internal microstates is approximately

\[
\dim\mathcal{H}_{\text{BH}}
\sim
e^{S_{\text{BH}}}.
\]

This exponential dimensionality is the source of computational protection.

If information is encoded into a typical subspace of dimension \(e^S\), then generic decoding requires operations whose complexity scales exponentially in \(S\).

Thus the black-hole interior is not merely large. It is computationally deep.

---

## 8. Hayden–Preskill Recovery and the Black-Hole Mirror

Hayden and Preskill proposed that an old black hole acts as an information mirror.

After the Page time, when the black hole has emitted more than half of its entropy,

\[
S_{\text{rad}}
>
S_{\text{BH}},
\]

new information thrown into the black hole can emerge relatively quickly in the Hawking radiation.

The information does not remain hidden until complete evaporation. It emerges after a scrambling time:

\[
t_{\text{emergence}}
\sim
t_{\text{scr}}.
\]

However, emergence is not the same as accessibility.

The information may be present in the radiation but encoded in highly nonlocal correlations. To recover it, one may need to perform a highly complex quantum computation on the radiation.

Thus Hayden–Preskill shows that black holes do not destroy information, but it also reveals that information can be both present and inaccessible.

---

## 9. Harlow–Hayden and the Complexity Obstruction

Harlow and Hayden sharpened this point.

They considered the computational task required to verify the AMPS firewall argument.

The firewall argument requires an observer to decode early Hawking radiation, extract a partner mode, and verify entanglement with a late outgoing mode.

Harlow and Hayden showed that, under plausible complexity assumptions, the decoding task requires time exponential in the black-hole entropy:

\[
t_{\text{decode}}
\sim
e^{S_{\text{BH}}}.
\]

This is vastly longer than the black-hole evaporation time.

Thus an exterior observer cannot operationally verify the conditions that would lead to a firewall paradox.

The interior may be encoded in the radiation, but the decoding complexity forms a horizon.

This is a complexity horizon.

---

## 10. Complexity Horizons: Definition

Let a physical system encode information \(I\) in some degrees of freedom.

Let \(\mathcal{C}_{\text{decode}}(I)\) be the minimum computational complexity required to reconstruct \(I\) from accessible data.

Let an observer have computational budget \(B\).

The observer-accessible information set is

\[
\mathcal{A}_B
=
\left\{
I
\mid
\mathcal{C}_{\text{decode}}(I)
\leq
B
\right\}.
\]

The complexity horizon is the boundary of this set:

\[
\mathcal{H}_B
=
\partial \mathcal{A}_B.
\]

Information beyond the complexity horizon satisfies

\[
\mathcal{C}_{\text{decode}}(I)
>
B.
\]

It is encoded but not operationally accessible.

Thus:

\[
\boxed{
\text{A complexity horizon separates encoded reality from feasible accessibility.}
}
\]

Unlike a causal horizon, a complexity horizon depends on the observer’s computational resources.

Unlike a thermodynamic horizon, it need not involve temperature or entropy flow.

It is a horizon of operational feasibility.

---

## 11. Complexity Equals Volume

The first major holographic complexity conjecture is complexity equals volume.

It states that the computational complexity of the boundary state dual to a black hole is proportional to the volume of a maximal spatial slice behind the horizon:

\[
\mathcal{C}_V
=
\frac{V(\Sigma)}{G_N L},
\]

where:

- \(V(\Sigma)\) is the volume of a maximal bulk slice,
- \(G_N\) is Newton’s constant,
- \(L\) is a characteristic length scale, often the AdS radius.

For an eternal AdS black hole, the interior volume grows linearly with boundary time:

\[
V(t)
\sim
V_0 + \alpha t.
\]

Therefore,

\[
\mathcal{C}_V(t)
\sim
\mathcal{C}_0 + \alpha' t.
\]

The black-hole interior grows because the boundary state becomes more complex.

Thus:

\[
\boxed{
\text{Interior volume is geometric complexity.}
}
\]

---

## 12. Complexity Equals Action

The second major conjecture is complexity equals action.

It identifies the complexity of the boundary state with the gravitational action evaluated on the Wheeler–DeWitt patch:

\[
\mathcal{C}_A
=
\frac{I_{\text{WDW}}}{\pi\hbar}.
\]

The Wheeler–DeWitt patch is the domain of dependence of a bulk Cauchy surface anchored at a boundary time slice.

For a neutral AdS black hole of mass \(M\), the late-time growth rate is

\[
\frac{d\mathcal{C}_A}{dt}
=
\frac{2Mc^2}{\pi\hbar}.
\]

This saturates the Lloyd bound on computational rate.

Thus black holes are not only fast scramblers. They are maximal computers.

---

## 13. The Lloyd Bound

The Lloyd bound states that the rate of computation for a physical system of energy \(E\) is bounded by

\[
\frac{d\mathcal{C}}{dt}
\leq
\frac{2E}{\pi\hbar}.
\]

For a black hole,

\[
E
=
Mc^2.
\]

Therefore,

\[
\frac{d\mathcal{C}}{dt}
\leq
\frac{2Mc^2}{\pi\hbar}.
\]

The complexity equals action conjecture gives equality for neutral AdS black holes.

Thus:

\[
\boxed{
\text{Black holes grow interior complexity at the maximum rate allowed by quantum mechanics.}
}
\]

This is one of the deepest connections between gravity, information, and computation.

---

## 14. The Interior as a Complexity Coordinate

If interior volume grows with complexity, then complexity can function as a coordinate.

Let \(\chi\) be a dimensionless complexity coordinate:

\[
\chi
=
\frac{\mathcal{C}(t)}{S}.
\]

The black-hole interior may be foliated by surfaces of constant complexity.

Near the horizon, complexity is relatively low. Deeper inside, complexity is larger.

The radial or temporal depth behind the horizon corresponds to computational depth.

Thus:

\[
\boxed{
\text{The black-hole interior is a region of increasing computational depth.}
}
\]

This does not mean the interior is unreal. It means that its accessibility is graded by complexity.

---

## 15. Interior Reconstruction and Precursors

In holography, bulk operators inside the black hole are represented by highly complex boundary operators.

A simple interior operator \(b\) may correspond to a boundary precursor:

\[
b_{\text{bdy}}
=
U^\dagger
b_{\text{bulk}}
U,
\]

where \(U\) is the time-evolution operator of the boundary theory.

As time evolves, the precursor becomes increasingly nonlocal and complex:

\[
\mathcal{C}(b_{\text{bdy}}(t))
\sim
t.
\]

For an old black hole, reconstructing an interior mode from the radiation may require an exponentially complex precursor.

Thus the interior is encoded, but only accessible through operations of enormous complexity.

---

## 16. Quantum Error Correction and Protected Interiors

Holographic quantum error correction explains how bulk information can be redundantly encoded in boundary degrees of freedom.

A bulk operator may be reconstructible from multiple boundary regions:

\[
O_{\text{bulk}}
\cong
O_A
\cong
O_B
\cong
O_C.
\]

These reconstructions agree only within a code subspace:

\[
P_{\mathcal{C}}O_A P_{\mathcal{C}}
=
P_{\mathcal{C}}O_B P_{\mathcal{C}}.
\]

The code subspace protects bulk locality against erasures of boundary subregions.

But reconstruction may be computationally hard.

Thus there are two layers of protection:

1. error-correcting redundancy,
2. computational complexity.

The interior is both redundantly encoded and computationally shielded.

---

## 17. Complexity Horizons and Firewalls

The AMPS firewall argument assumes that an observer can in principle decode Hawking radiation and verify entanglement relations.

Complexity-Horizon Relativity modifies this assumption.

The required decoding operation may have complexity

\[
\mathcal{C}_{\text{decode}}
\sim
e^{S}.
\]

No physical observer can perform such a computation within the lifetime of the black hole.

Thus the operational conditions for a firewall cannot be realized.

The infalling observer sees a smooth horizon.

The exterior observer sees encoded radiation.

Both descriptions are consistent because they are separated by a complexity horizon.

Thus:

\[
\boxed{
\text{Complexity horizons protect the consistency of black-hole complementarity.}
}
\]

---

## 18. Traversable Wormholes and Complexity Reduction

Ordinary Einstein–Rosen bridges are nontraversable.

Gao, Jafferis, and Wall showed that a suitable double-trace coupling between two boundary CFTs can render a wormhole traversable.

The coupling effectively introduces negative energy, allowing signals to pass through the wormhole.

From the complexity perspective, traversability can be understood as reducing the computational barrier between the two sides.

The interior information that was previously accessible only through exponential decoding becomes accessible through a simpler protocol.

Thus:

\[
\boxed{
\text{Traversability is the lowering of a complexity horizon.}
}
\]

This connects wormhole physics to quantum teleportation and computational complexity.

---

## 19. de Sitter Complexity Horizons

Complexity horizons are not limited to black holes.

De Sitter space has a cosmological horizon with entropy

\[
S_{\text{dS}}
=
\frac{3\pi}{G\Lambda}.
\]

A static-patch observer has access to a finite-dimensional Hilbert space:

\[
\dim\mathcal{H}_{\text{dS}}
\sim
e^{S_{\text{dS}}}.
\]

The observer’s accessible information is bounded by the horizon entropy.

Moreover, decoding global information from static-patch data may require complexity exponential in \(S_{\text{dS}}\).

Thus de Sitter space may possess a complexity horizon in addition to its causal and thermodynamic horizons.

This has implications for late-time cosmology, Poincaré recurrence, and the measure problem.

---

## 20. Cosmological Computational Bounds

The observable universe also has finite computational capacity.

A system of energy \(E\) operating for time \(t\) can perform at most approximately

\[
N_{\text{ops}}
\sim
\frac{Et}{\hbar}
\]

elementary operations.

For the observable universe, this gives a finite but enormous number of operations.

Memory is bounded by entropy and area laws.

Thus even cosmological observation is subject to computational limits.

What can be known by any civilization is bounded not only by causal horizons but also by computational horizons.

---

## 21. Complexity and the Emergence of Classical Spacetime

Classical spacetime may be the sector of reality accessible within feasible complexity.

The full quantum gravitational state contains enormously complex correlations.

Only a low-complexity sector can be described by smooth geometry, local fields, and semiclassical causality.

Thus:

\[
\boxed{
\text{Classical spacetime is a low-complexity effective description.}
}
\]

Beyond that sector, geometry may still be encoded, but not in a form accessible to simple geometric variables.

---

## 22. Tensor Networks and Geometric Complexity

Tensor-network models provide an intuitive picture.

A holographic tensor network encodes bulk geometry in entanglement patterns.

The depth of the network corresponds to radial direction.

The number of tensors required to prepare a state corresponds to complexity.

As complexity increases, the network grows deeper, and the emergent geometry expands.

Thus tensor networks realize the principle:

\[
\boxed{
\text{Geometric depth is computational depth.}
}
\]

This is a discrete analogue of complexity equals volume.

---

## 23. Complexity Relativity

Complexity is not absolute. It depends on:

1. gate set,
2. reference state,
3. allowed operations,
4. penalty factors,
5. precision,
6. observer resources.

However, robust features are invariant under reasonable changes of description.

Exponential versus polynomial complexity is stable under efficient changes of gate set.

Thus physical conclusions should be formulated in terms of complexity classes rather than exact gate counts.

The invariant distinction is not:

\[
\mathcal{C}=N,
\]

but:

\[
\mathcal{C}
\sim
\text{poly}(S)
\quad
\text{versus}
\quad
\mathcal{C}
\sim
e^{S}.
\]

Thus:

\[
\boxed{
\text{Complexity horizons are defined by scaling, not by microscopic gate conventions.}
}
\]

---

## 24. Formal Framework of Complexity-Horizon Relativity

Let \(\mathcal{H}\) be the Hilbert space of a system.

Let \(\mathcal{E}\) be the set of encoded physical information.

Let \(\mathcal{C}_{\text{decode}}(I)\) be the decoding complexity of information \(I\).

Let an observer \(O\) have time-dependent computational budget

\[
B_O(t).
\]

The accessible reality of \(O\) at time \(t\) is

\[
\mathcal{R}_O(t)
=
\left\{
I\in\mathcal{E}
\mid
\mathcal{C}_{\text{decode}}(I)
\leq
B_O(t)
\right\}.
\]

The complexity horizon is

\[
\mathcal{H}_O(t)
=
\partial \mathcal{R}_O(t).
\]

Different observers with different computational resources have different accessible realities:

\[
\mathcal{R}_O(t)
\neq
\mathcal{R}_{O'}(t).
\]

The invariant is the full encoded structure \(\mathcal{E}\), together with the complexity function

\[
\mathcal{C}_{\text{decode}}:
\mathcal{E}
\rightarrow
\mathbb{N}.
\]

Thus reality is stratified by computational accessibility.

---

## 25. Axioms of Complexity-Horizon Relativity

The framework may be organized around ten axioms.

### Axiom 1: Complexity Is Physical

Computational complexity is not merely epistemic. It constrains physical accessibility.

### Axiom 2: Horizons Can Be Computational

A horizon may separate not only causally disconnected regions but computationally inaccessible regions.

### Axiom 3: Encoding Does Not Imply Accessibility

Information may be physically present but operationally hidden.

### Axiom 4: Black Holes Are Maximal Complexity Engines

Black holes saturate fundamental bounds on complexity growth.

### Axiom 5: Interior Growth Is Complexity Growth

The growth of black-hole interiors corresponds to the growth of boundary-state complexity.

### Axiom 6: Scrambling Creates Short-Time Hiddenness

Scrambling hides information from local measurements on logarithmic timescales.

### Axiom 7: Complexity Creates Long-Time Hiddenness

Complexity hides information from decoding on exponential timescales.

### Axiom 8: Observers Have Computational Budgets

Physical observers are bounded by energy, time, memory, and complexity.

### Axiom 9: Classical Spacetime Is Low-Complexity

Semiclassical geometry is an effective description valid within feasible complexity sectors.

### Axiom 10: Invariant Reality Is Encoded Structure

The invariant content is the full encoded structure plus its complexity profile.

---

## 26. Relation to Previous Versions of Relativity

Complexity-Horizon Relativity connects deeply to earlier versions.

| Version | Relation |
|---|---|
| General Relativity | Causal horizons |
| Thermodynamic Relativity | Entropy and temperature horizons |
| Holographic Relativity | Bulk encoded on boundary |
| Computational Relativity | Complexity as physical time |
| Code-Subspace Relativity | Bulk locality as protected encoding |
| Vacuum Relativity | Observer-dependent vacua |
| Complexity-Horizon Relativity | Computational inaccessibility as horizon |

The progression is:

\[
\text{causal horizon}
\rightarrow
\text{thermodynamic horizon}
\rightarrow
\text{holographic encoding}
\rightarrow
\text{computational horizon}.
\]

---

## 27. Experimental and Observational Relevance

Direct observation of black-hole interiors is impossible by definition.

But complexity-horizon physics may be indirectly explored.

### 27.1 Quantum Simulators

SYK-like systems, superconducting qubits, trapped ions, and cold atoms can simulate scrambling and complexity growth.

### 27.2 Out-of-Time-Order Correlators

OTOCs diagnose scrambling:

\[
C(t)
=
-
\langle
[W(t),V]^2
\rangle.
\]

Their growth reflects operator complexity.

### 27.3 Quantum Processors

Quantum computers can measure circuit complexity growth, Krylov complexity, and information spreading.

### 27.4 Analog Black Holes

Analog gravity systems may simulate horizon thermality and information flow.

### 27.5 Holographic Models

Tensor networks and solvable holographic models provide laboratories for complexity equals volume and complexity equals action.

Thus Complexity-Horizon Relativity is not directly testable in astrophysical black holes, but it is testable in quantum-information analogues.

---

## 28. Open Problems

Several major problems remain.

### 28.1 Defining Complexity in Quantum Field Theory

Circuit complexity in continuum QFT and gravity requires regularization and gauge-invariant definitions.

### 28.2 Penalty Factors

Nielsen complexity depends on penalty choices. A physical principle for selecting penalties is needed.

### 28.3 Complexity Saturation

What happens when complexity saturates? How does the interior behave near recurrence times?

### 28.4 Interior Reconstruction

A complete map between interior operators and boundary precursors remains incomplete.

### 28.5 Firewalls and State Dependence

The precise status of interior operators and state dependence remains debated.

### 28.6 de Sitter Complexity

Complexity horizons in cosmological spacetimes require further development.

### 28.7 Observational Signatures

Direct empirical signatures of complexity horizons are unknown.

### 28.8 Complexity and Arrow of Time

The relation between complexity growth, thermodynamic irreversibility, and cosmological initial conditions remains deep and open.

---

## 29. What Einstein Would Think

Einstein would find Complexity-Horizon Relativity both strange and compelling.

He would appreciate the operational emphasis. A horizon that prevents observation is physically meaningful. A region that is encoded but computationally inaccessible is also operationally hidden.

But Einstein would be cautious about making computational complexity ontological. He sought geometric clarity, not computational obstruction.

Still, he would recognize the central lesson:

\[
\boxed{
\text{Physical reality must be understood in terms of what can be observed, reconstructed, and verified by physical observers.}
}
\]

Complexity-Horizon Relativity adds a modern qualification:

\[
\text{What can be observed is bounded not only by light cones, but by computation.}
\]

---

## 30. Summary of Core Equations

### Circuit complexity

\[
\mathcal{C}(U)
=
\min
\left\{
N
\mid
U
\approx
G_N\cdots G_1
\right\}.
\]

### Nielsen complexity

\[
\mathcal{C}(U)
=
\min_{U(s)}
\int_0^1 ds\,
F(H(s)).
\]

### Krylov complexity

\[
K(t)
=
\sum_n
n|\phi_n(t)|^2.
\]

### Scrambling time

\[
t_{\text{scr}}
\sim
\frac{\beta}{2\pi}
\log S.
\]

### Black-hole entropy

\[
S_{\text{BH}}
=
\frac{A}{4G}.
\]

### Decoding time

\[
t_{\text{decode}}
\sim
e^{S}.
\]

### Complexity equals volume

\[
\mathcal{C}_V
=
\frac{V(\Sigma)}{G_N L}.
\]

### Complexity equals action

\[
\mathcal{C}_A
=
\frac{I_{\text{WDW}}}{\pi\hbar}.
\]

### Late-time complexity growth

\[
\frac{d\mathcal{C}_A}{dt}
=
\frac{2Mc^2}{\pi\hbar}.
\]

### Lloyd bound

\[
\frac{d\mathcal{C}}{dt}
\leq
\frac{2E}{\pi\hbar}.
\]

### Accessible reality

\[
\mathcal{R}_O(t)
=
\left\{
I
\mid
\mathcal{C}_{\text{decode}}(I)
\leq
B_O(t)
\right\}.
\]

### Complexity horizon

\[
\mathcal{H}_O(t)
=
\partial \mathcal{R}_O(t).
\]

### Central principle

\[
\boxed{
\text{Some regions of reality are hidden not by distance, but by computational complexity.}
}
\]

---

## 31. Conclusion

Relativity 30.0, Complexity-Horizon Relativity, reveals a new kind of horizon.

Causal horizons hide regions because signals cannot escape.

Thermodynamic horizons hide regions because entropy and temperature govern information flow.

Complexity horizons hide regions because reconstruction requires computational resources that grow exponentially with entropy.

The black-hole interior is the central example. It may be encoded in exterior radiation, but decoding it may require time

\[
t_{\text{decode}}
\sim
e^{S}.
\]

At the same time, the interior grows as complexity grows:

\[
\mathcal{C}(t)
\sim
t,
\]

for exponentially long times.

The central principle is:

\[
\boxed{
\text{Some regions of reality are hidden not by distance, but by computational complexity.}
}
\]

A complexity horizon separates what is physically encoded from what is operationally accessible.

This is Complexity-Horizon Relativity.

It tells us that the universe is not only curved, thermal, holographic, and quantum. It is also computationally stratified.

Reality may be fully encoded, but not fully available.

What is real may exceed what can be reconstructed.

This is the computational horizon of relativity.

---

## Appendix A: Nielsen Complexity Geometry

Let

\[
\frac{dU(s)}{ds}
=
-iH(s)U(s).
\]

Expand

\[
H(s)
=
\sum_I h_I(s)\sigma_I.
\]

A quadratic cost function is

\[
F(H)
=
\sqrt{
\sum_I q_I |h_I|^2
}.
\]

The complexity is

\[
\mathcal{C}(U)
=
\min_{U(s)}
\int_0^1 ds\,F(H(s)).
\]

Penalty factors \(q_I\) suppress nonlocal directions, making complexity sensitive to physical implementability.

---

## Appendix B: Lloyd Bound Sketch

A quantum system with average energy \(E\) above its ground state can undergo at most approximately

\[
\nu_{\max}
=
\frac{2E}{\pi\hbar}
\]

distinct elementary state transitions per unit time.

If each transition increases complexity by at most one unit, then

\[
\frac{d\mathcal{C}}{dt}
\leq
\frac{2E}{\pi\hbar}.
\]

For a black hole,

\[
E=Mc^2,
\]

so

\[
\frac{d\mathcal{C}}{dt}
\leq
\frac{2Mc^2}{\pi\hbar}.
\]

Complexity equals action saturates this bound.

---

## Appendix C: Hayden–Preskill Mirror

After the Page time,

\[
S_{\text{rad}}>S_{\text{BH}},
\]

a black hole becomes an information mirror.

Information thrown into the black hole emerges in the radiation after a scrambling time:

\[
t_{\text{emergence}}
\sim
t_{\text{scr}}
\sim
\frac{\beta}{2\pi}\log S.
\]

The information is present in the radiation, but encoded nonlocally.

Recovery requires a decoding operation whose complexity may be enormous.

---

## Appendix D: Complexity Horizon Construction

Let \(I\) be encoded information.

Let

\[
\mathcal{C}_{\text{decode}}(I)
\]

be the minimal circuit complexity required to reconstruct \(I\).

For observer budget \(B\), define

\[
\mathcal{R}_B
=
\{I:\mathcal{C}_{\text{decode}}(I)\leq B\}.
\]

The complexity horizon is

\[
\mathcal{H}_B
=
\partial\mathcal{R}_B.
\]

Information with

\[
\mathcal{C}_{\text{decode}}(I)>B
\]

is beyond the horizon.

---

## Appendix E: Complexity Equals Volume Growth

For an eternal AdS black hole, the maximal interior volume grows approximately linearly:

\[
V(t)
\sim
V_0+\alpha t.
\]

Using

\[
\mathcal{C}_V
=
\frac{V}{G_N L},
\]

one obtains

\[
\mathcal{C}_V(t)
\sim
\mathcal{C}_0+\alpha' t.
\]

Thus interior growth corresponds to complexity growth.

---

## Selected References

1. L. Susskind, “Computational Complexity and Black Hole Horizons,” *Fortschritte der Physik* **64**, 24 (2016).  
2. L. Susskind, “ER = EPR,” in *Strings, Branes and Cosmology* (2016).  
3. A. R. Brown, D. A. Roberts, L. Susskind, B. Swingle, and Y. Zhao, “Holographic Complexity Equals Bulk Action?” *Physical Review Letters* **116**, 191301 (2016).  
4. A. R. Brown, D. A. Roberts, L. Susskind, B. Swingle, and Y. Zhao, “Complexity, Action, and Black Holes,” *Physical Review D* **93**, 086006 (2016).  
5. D. A. Roberts, L. Susskind, and B. Swingle, “Volume Law for Complex States and Bounds for Black Holes,” *Physical Review D* **93**, 026009 (2016).  
6. L. Susskind and Y. Zhao, “Complexity and Momentum,” *Journal of High Energy Physics* **2003**, 239 (2020).  
7. P. Hayden and J. Preskill, “Black Holes as Mirrors: Quantum Information in Random Subsystems,” *Journal of High Energy Physics* **0709**, 120 (2007).  
8. D. Harlow and P. Hayden, “Quantum Computation vs. Firewalls,” *Journal of High Energy Physics* **1306**, 085 (2013).  
9. Y. Sekino and L. Susskind, “Fast Scramblers,” *Journal of High Energy Physics* **0810**, 065 (2008).  
10. J. Maldacena, S. H. Shenker, and D. Stanford, “A Bound on Chaos,” *Journal of High Energy Physics* **1608**, 106 (2016).  
11. M. A. Nielsen, “A Geometric Approach to Quantum Circuit Lower Bounds,” *Quantum Information and Computation* **6**, 213 (2006).  
12. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information* (Cambridge University Press, 2000).  
13. S. Lloyd, “Ultimate Physical Limits to Computation,” *Nature* **406**, 1047 (2000).  
14. D. E. Parker, X. Cao, A. Avdoshkin, T. Scaffidi, and E. Altman, “A Universal Operator Growth Hypothesis,” *Physical Review X* **9**, 031017 (2019).  
15. V. Balasubramanian, P. Caputa, J. M. Magan, and Q. Wu, “From Quantum Chaos and Eigenstate Thermalization to Statistical Mechanics and Thermodynamics,” *Journal of Statistical Mechanics* (2022).  
16. A. Almheiri, X. Dong, and D. Harlow, “Bulk Locality and Quantum Error Correction in AdS/CFT,” *Journal of High Energy Physics* **1504**, 163 (2015).  
17. D. Harlow, “The Ryu-Takayanagi Formula from Quantum Error Correction,” *Communications in Mathematical Physics* **354**, 865 (2017).  
18. P. Gao, D. L. Jafferis, and A. C. Wall, “Traversable Wormholes via a Double Trace Deformation,” *Journal of High Energy Physics* **1712**, 151 (2017).  
19. K. Papadodimas and S. Raju, “An Infalling Observer in AdS/CFT,” *Journal of High Energy Physics* **1310**, 212 (2013).  
20. A. Almheiri, D. Marolf, J. Polchinski, and J. Sully, “Black Holes: Complementarity or Firewalls?” *Journal of High Energy Physics* **1302**, 062 (2013).  
21. B. Swingle, “Entanglement Renormalization and Holography,” *Physical Review D* **86**, 065007 (2012).  
22. S. Ryu and T. Takayanagi, “Holographic Derivation of Entanglement Entropy from AdS/CFT,” *Physical Review Letters* **96**, 181602 (2006).  
23. G. ’t Hooft, “Dimensional Reduction in Quantum Gravity,” in *Salamfest* (World Scientific, 1993).  
24. L. Susskind, “The World as a Hologram,” *Journal of Mathematical Physics* **36**, 6377 (1995).  
25. R. Bousso, “The Holographic Principle,” *Reviews of Modern Physics* **74**, 825 (2002).

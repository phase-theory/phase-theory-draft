# Higher-Spin Holography as a String Limit

## A proof-of-principle derivation of Vasiliev gravity from the tensionless string and the vector-model holographic limit

**White paper draft**  
**Date:** 2026-06-11  

---

## Abstract

Vasiliev's higher-spin gravity in anti-de Sitter space is widely regarded as the most explicit non-supersymmetric and non-matrix example of holography. In its best understood form, the type-A bosonic higher-spin theory on `AdS_4` is dual to the singlet sector of the three-dimensional `O(N)` vector model. The relation to string theory is often summarized by the slogan that Vasiliev theory is the tensionless limit of a string theory, but this statement is usually schematic: there is no standard finite-tension critical string background whose controlled `alpha' -> infinity` limit has been shown rigorously to become four-dimensional Vasiliev theory.

This white paper formulates a precise proof-of-principle derivation. The central claim is not that a known ten-dimensional finite-tension string compactification has already been rigorously reduced to Vasiliev theory. Rather, we show that if one defines the relevant string limit in the operational way appropriate to holography—namely as the zero-tension, singleton-string field theory whose physical closed-string Hilbert space is the singlet bilinear of boundary singletons—then the limit necessarily produces the spectrum, gauge algebra, unfolded master fields, interaction vertices, and holographic correlators of Vasiliev's type-A higher-spin gravity. The derivation proceeds through five equivalent descriptions:

1. the `alpha' -> infinity` collapse of the string Regge tower into massless AdS gauge fields;
2. the Flato-Fronsdal decomposition of two AdS singletons into the complete tower of bulk massless integer-spin representations;
3. the bilocal collective field of the `O(N)` vector model;
4. the Weyl/Wigner transform from bilocals to oscillator master fields with Moyal star product;
5. the Maurer-Cartan/unfolded form of tensionless string field theory, which is Vasiliev's system after adding the standard auxiliary `Z`-oscillators implementing the homological resolution of nonlinear constraints.

The result is a conditional derivation theorem: any AdS string theory whose zero-tension physical closed-string sector is the singlet square of the scalar singleton and whose cubic vertex reduces to the canonical oscillator overlap has Vasiliev type-A theory as its universal tensionless bulk limit. This gives a concrete sense in which the Klebanov-Polyakov higher-spin/vector duality is the simplest string holography: it is the `lambda = R^2/alpha' -> 0`, `N -> infinity` limit where the string becomes a higher-spin gauge theory, the worldsheet becomes topological or bit-like, and holography does not require supersymmetry or a large-`N` matrix gauge sector.

---

## Executive summary

The tensionless limit of a string in AdS is governed by the dimensionless parameter

```text
lambda_s = R_AdS^2 / alpha' .
```

Large `lambda_s` corresponds to a semiclassical Einstein-like string regime with only a few light fields and a large string tension. The tensionless regime is

```text
lambda_s -> 0,
T = 1/(2 pi alpha') -> 0,
```

so every Regge excitation becomes parametrically light on the AdS scale. In flat space this produces an infinite degeneracy and an enhanced gauge symmetry that is difficult to organize locally. In AdS, the same degeneracy is naturally organized by the higher-spin algebra `hs(4)`, the algebra of bilinears of the scalar singleton representation of `SO(3,2)`.

The key representation-theoretic identity is the Flato-Fronsdal theorem:

```text
Rac \otimes Rac = \bigoplus_{s=0}^{\infty} D(s+1,s),
```

with a parity projection giving the minimal bosonic tower

```text
Rac \otimes Rac |_{O(N) even} = D(1,0) \oplus \bigoplus_{s=2,4,6,...} D(s+1,s).
```

Here `Rac` is the scalar singleton of `SO(3,2)`, and `D(E_0,s)` is the lowest-weight AdS representation with energy `E_0` and spin `s`. The massless AdS spin-`s` representation has `E_0=s+1`, exactly the dimension of a conserved spin-`s` current in a free three-dimensional vector model. Thus the closed tensionless string Hilbert space built from two singleton endpoints is precisely the Vasiliev spectrum.

The dynamical derivation follows by rewriting the vector-model singlet sector in bilocal variables

```text
Psi(x,y) = (1/N) phi^i(x) phi^i(y),
```

and then applying a Wigner transform from the two boundary points `(x,y)` to a bulk point `X`, a radial variable `z`, and internal oscillator variables `Y`. The algebra of bilocals becomes a Moyal star algebra of oscillators. The bilocal Schwinger-Dyson equation becomes the unfolded flatness/covariant-constancy system for a one-form master connection `W(X;Y,Z)` and zero-form master field `B(X;Y,Z)`. The auxiliary `Z` variables appear as the homological resolution needed to write the nonlinear string field equation off shell. The resulting equations are Vasiliev's equations:

```text
d_x W + W * W = 0,
d_x B + W * B - B * pi(W) = 0,
d_x S + W * S - S * W = 0,
S * B = B * pi(S),
S * S = -i dz^alpha dz_alpha [1 + B * kappa]
        -i d\bar z^{\dot alpha} d\bar z_{\dot alpha} [1 + B * \bar kappa]
```

with the appropriate reality, parity, and projection conditions. The parity-even scalar boundary condition gives the type-A/free-`O(N)` dual; changing the scalar boundary condition gives the critical `O(N)` model. At finite `N`, higher-spin currents acquire nonconservation at order `1/N`, giving quantum corrections to the bulk higher-spin theory.

The proof of principle is therefore: Vasiliev theory is not an arbitrary cousin of string theory. It is the universal zero-tension closed-string field theory of two singleton endpoints in AdS. The `O(N)` vector model is the boundary gauge-fixing of this tensionless string, and Vasiliev's unfolded equations are the spacetime string field equations after the infinite tower of massless Regge modes has been organized by higher-spin symmetry.

---

## 1. The problem and the target statement

### 1.1 The usual slogan

One often says:

> Vasiliev higher-spin gravity in AdS is the tensionless limit of string theory.

The slogan is motivated by a structural analogy. In ordinary string theory, massive higher-spin excitations lie on Regge trajectories with masses of order

```text
m_n^2 ~ n / alpha'.
```

As the tension tends to zero, `alpha' -> infinity`, these states become massless. An interacting theory with infinitely many massless higher-spin fields is exactly what Vasiliev theory provides.

However, the slogan is not a derivation. A derivation must explain:

1. **Spectrum:** why the tensionless string contains precisely one massless field of each relevant spin, not too many or too few;
2. **Gauge algebra:** why the enhanced string gauge symmetry becomes the higher-spin algebra `hs(4)`;
3. **Interactions:** why the cubic and higher interactions are those of Vasiliev theory rather than some other higher-spin theory;
4. **Holography:** why the boundary theory is the `O(N)` vector model singlet sector;
5. **String interpretation:** what plays the role of worldsheet, Regge tower, string field, and string coupling in the vector-model setting.

This paper supplies a derivation in a precise proof-of-principle sense.

### 1.2 Main theorem: conditional derivation of Vasiliev theory

Let `S_alpha'` be a family of AdS string field theories with AdS radius `R`, string scale `alpha'`, and coupling `g_s`, satisfying the following assumptions:

**A1. Singleton endpoint condition.** In the limit

```text
lambda_s = R^2/alpha' -> 0,
```

the physical boundary degrees of freedom of the string reduce to scalar singletons `Rac` of `SO(3,2)`.

**A2. Closed-string singlet condition.** The physical closed-string Hilbert space is the singlet bilinear sector

```text
H_closed^(0) = Sym^2(Rac)
```

for the minimal `O(N)` theory, or `Rac \otimes \overline{Rac}` for the non-minimal/unitary version.

**A3. Oscillator overlap vertex.** The zero-tension cubic string field vertex reduces to the canonical phase-space overlap vertex. Equivalently, in the Weyl representation its product is the Moyal product of AdS singleton oscillators.

**A4. Large-N classical limit.** The closed-string coupling scales as

```text
g_s ~ G_N/R^2 ~ 1/N,
```

so that `N -> infinity` is the classical bulk limit.

**A5. AdS covariance and parity projection.** The resulting string field theory preserves `SO(3,2)`, the required bosonic reality conditions, and the even-spin projection for the minimal type-A model.

Then the `lambda_s -> 0` limit of `S_alpha'` is the type-A Vasiliev higher-spin theory on `AdS_4`, with boundary conditions dual to the free or critical `O(N)` vector model depending on the scalar quantization. In particular:

```text
lim_{lambda_s -> 0} S_alpha' = S_Vasiliev,type-A + O(1/N quantum corrections).
```

The theorem is conditional because assumptions A1-A3 specify the relevant universality class of the tensionless string. This is analogous to deriving a low-energy effective field theory from symmetry, spectrum, and locality data when a microscopic lattice regulator is not explicitly solved. The content of the derivation is that once the string limit is singleton-like, Vasiliev theory is forced.

---

## 2. AdS tensionless strings and the higher-spin limit

### 2.1 The dimensionless tension

For strings in AdS, the physical control parameter is not simply `alpha'`, but

```text
lambda_s = R_AdS^2 / alpha'.
```

In familiar `AdS_5/CFT_4`, this parameter is related to the 't Hooft coupling by

```text
R_AdS^2/alpha' ~ sqrt(lambda_tHooft).
```

Weakly coupled gauge theory corresponds to small `lambda_tHooft`, hence small string tension in AdS units. In the vector-model duality there is no matrix 't Hooft coupling. The natural statement is therefore that the theory sits directly at the tensionless point:

```text
lambda_s = 0,
N large.
```

The large parameter `N` controls the bulk loop expansion, not the string tension.

### 2.2 Regge collapse

At finite tension, a string has a tower of states with schematic mass formula

```text
m_n^2 R^2 ~ lambda_s (n - a) + curvature corrections.
```

When `lambda_s -> 0`, states at all oscillator levels become light relative to the AdS scale. But a generic collection of infinitely many light fields is inconsistent. The limit can exist only if it is accompanied by an enhanced gauge symmetry eliminating negative-norm and redundant polarizations. In AdS, the consistent enhancement is the higher-spin gauge symmetry generated by `hs(4)`.

For a totally symmetric spin-`s` field in `AdS_4`, masslessness corresponds to the lowest energy

```text
E_0 = s + 1,
```

or, in CFT language, to a conserved spin-`s` current of dimension

```text
Delta_s = s + 1.
```

This is exactly the spectrum of bilinear currents in a free three-dimensional vector model:

```text
J_{mu1...mus} = phi^i partial_{(mu1} ... partial_{mus)} phi^i + traces/improvements,
partial^{mu1} J_{mu1...mus} = 0.
```

For the real `O(N)` model only even spins occur. For the complex `U(N)` model all integer spins occur.

### 2.3 Why AdS is essential

Flat-space interacting massless higher-spin theories face severe no-go constraints. AdS avoids the assumptions of those theorems because interactions can contain inverse powers of the cosmological constant:

```text
g_{s_1 s_2 s_3} ~ R^{-k}.
```

Thus a smooth higher-spin theory exists at finite AdS radius but typically has no conventional local flat-space limit. The tensionless string limit should therefore be taken in AdS units, not by first flattening space.

---

## 3. Singletons as string endpoints

### 3.1 The scalar singleton

The scalar singleton `Rac` is a special representation of `SO(3,2)`, the isometry group of `AdS_4`. It does not describe a propagating particle in the four-dimensional bulk. Instead, it naturally lives on the three-dimensional conformal boundary. It is the representation carried by a free scalar field `phi(x)` in three dimensions with scaling dimension

```text
Delta_phi = 1/2.
```

The singleton is therefore the correct representation-theoretic object for the elementary vector-model field.

### 3.2 Two singletons make a bulk particle

The Flato-Fronsdal theorem states that the tensor product of two scalar singletons decomposes into all massless integer-spin representations in `AdS_4`:

```text
Rac \otimes Rac = \bigoplus_{s=0}^{\infty} D(s+1,s).
```

For the minimal real `O(N)` theory, Bose symmetry keeps only even spins:

```text
Sym^2(Rac) = D(1,0) \oplus \bigoplus_{s=2,4,6,...} D(s+1,s).
```

This is the first decisive step. If a tensionless closed string is the singlet bilinear of two singleton endpoints, its spectrum is exactly the minimal type-A Vasiliev spectrum:

```text
spin 0, 2, 4, 6, ... .
```

The scalar `D(1,0)` admits alternate quantization in `AdS_4`, corresponding to boundary scalar operator dimensions `Delta=1` and `Delta=2`. These are dual to the free and critical `O(N)` vector models respectively.

### 3.3 Interpretation as a tensionless string

A tensile string is an extended object whose oscillators describe relative motion along the string. In the zero-tension limit, the cost of stretching vanishes. The string becomes a collection of null or singleton-like bits. For the closed string sector relevant here, the gauge-invariant object is not a single singleton, but a bilinear singlet:

```text
phi^i(x) phi^i(y).
```

This bilocal object has two endpoints on the boundary and an infinite expansion in relative separation. That expansion is the boundary manifestation of the infinite higher-spin tower.

Thus the fundamental tensionless string field is naturally the bilocal collective field

```text
Psi(x,y) = (1/N) phi^i(x) phi^i(y).
```

The center-of-mass and relative coordinates of the bilocal become, after an appropriate canonical transformation, the bulk AdS coordinates and internal spin variables.

---

## 4. The `O(N)` vector model as the boundary string field theory

### 4.1 Boundary action and singlet sector

Consider the Euclidean free `O(N)` vector model in three dimensions:

```text
S_free = (1/2) \int d^3x partial_mu phi^i partial^mu phi^i,
qquad i=1,...,N.
```

The singlet sector consists of operators invariant under global `O(N)`. Its single-trace analogues are bilinear currents:

```text
J_s(x,epsilon)
= phi^i(x) (epsilon · partial)^s phi^i(x) + ...,
```

where `epsilon^2=0` packages the symmetric traceless indices and the omitted terms ensure conservation and tracelessness. At `N=infinity`, these currents are exactly conserved:

```text
partial · J_s = 0.
```

By the AdS/CFT dictionary, each conserved current corresponds to a massless gauge field in the bulk.

### 4.2 Collective field formulation

Define the bilocal collective field

```text
Psi(x,y) = (1/N) phi^i(x) phi^i(y).
```

Changing variables from `phi^i` to `Psi` gives a collective action of the schematic form

```text
S_coll[Psi]
= N/2 Tr[-partial_x^2 Psi(x,y)|_{x=y}]
  - N/2 Tr log Psi.
```

Expanding around the large-`N` saddle,

```text
Psi = Psi_0 + N^{-1/2} eta,
```

gives

```text
S_coll = S_0 + (1/2) eta K eta
         + (1/sqrt(N)) V_3 eta^3
         + (1/N) V_4 eta^4 + ... .
```

This is already a closed-string field theory:

```text
g_s ~ 1/N,
```

and the fields `eta(x,y)` create and annihilate bilinear singlet excitations. The loop expansion of the bilocal theory is the bulk genus expansion.

### 4.3 Bilocal field as a string field

The bilocal field `Psi(x,y)` has precisely the interpretation expected of a tensionless closed string field:

- the two boundary points are the endpoints of two singleton bits;
- the center-of-mass coordinate maps to the bulk spacetime coordinate;
- the relative coordinate maps to spin and radial data;
- the `1/N` expansion is the closed-string coupling expansion;
- the infinite Taylor expansion in `x-y` produces the infinite tower of higher-spin currents.

In this sense, the `O(N)` vector model is not merely dual to a string theory. It is a gauge-fixed presentation of the tensionless string field theory.

---

## 5. From bilocals to AdS fields

### 5.1 Bilocal expansion into currents

Set

```text
X = (x+y)/2,
r = x-y.
```

A bilocal fluctuation can be expanded as

```text
eta(X,r) = \sum_{s=0}^{\infty} eta_{mu1...mus}(X) r^{mu1}...r^{mus}.
```

After imposing the equations of motion and quotienting by improvements, the coefficients correspond to conserved currents and therefore to bulk massless fields.

A more precise version uses a null polarization vector `epsilon` and writes

```text
J_s(X,epsilon)
= [f_s(epsilon · partial_x, epsilon · partial_y)
   phi^i(x) phi^i(y)]_{x=y},
```

where `f_s` is chosen so that `J_s` is a conformal primary. Conservation follows from the free scalar equation.

### 5.2 Emergent radial coordinate

The map from bilocals to AdS fields is nonlocal but canonical. In momentum space, introduce momenta `p_1,p_2` conjugate to `x,y`. The invariant mass of the two-singleton system supplies the radial momentum, while the relative momentum and separation supply spin. Schematically,

```text
P = p_1 + p_2,
q = (p_1 - p_2)/2.
```

The bilocal phase space `(X,r;P,q)` can be transformed into AdS phase space `(x_bulk,z;p_bulk,p_z)` plus an internal angle conjugate to spin. The radial coordinate is controlled by the inverse relative momentum scale:

```text
z ~ |r|   or, in momentum representation,   z ~ 1/|q|,
```

with the precise map depending on the chosen gauge. This explains why a theory of bilocal boundary variables contains one extra emergent holographic dimension.

### 5.3 Fronsdal equations from current conservation

A conserved boundary current of dimension `Delta=s+1` sources a bulk spin-`s` Fronsdal field `h_{mu1...mus}` obeying, at the linearized level,

```text
F_{mu1...mus}(h) = 0,
```

with gauge symmetry

```text
delta h_{mu1...mus} = nabla_{(mu1} xi_{mu2...mus)}.
```

The AdS/CFT mass-dimension relation for a symmetric spin-`s` field in `AdS_4` implies that `Delta=s+1` is exactly the massless point. Therefore the linearized bilocal singlet sector is identical to the linearized Vasiliev spectrum.

---

## 6. Oscillator realization and the higher-spin algebra

### 6.1 Oscillators for `SO(3,2)`

The higher-spin algebra in four dimensions is conveniently written using spinor oscillators

```text
Y_A = (y_alpha, \bar y_{\dot alpha}),
alpha, dot alpha = 1,2,
```

with Moyal star product

```text
(f * g)(Y)
= f(Y) exp[i \overleftarrow{partial_A} C^{AB} \overrightarrow{partial_B}] g(Y),
```

so that

```text
[Y_A,Y_B]_* = 2i C_{AB}.
```

The `AdS_4` isometry algebra `sp(4) ~ so(3,2)` is generated by bilinears

```text
T_{AB} = (1/2) {Y_A,Y_B}_*.
```

The higher-spin algebra is the even part of the Weyl algebra generated by these oscillators, modulo the appropriate ideal fixing the singleton representation:

```text
hs(4) = U(so(3,2)) / Ann(Rac).
```

This equation is central. It says that higher-spin symmetry is the algebra of all endomorphisms of the singleton compatible with the `SO(3,2)` structure.

### 6.2 Bilocals become Moyal products

The bilocal collective field has a natural operator product induced by contraction of the vector index:

```text
(phi^i(x) phi^i(y)) (phi^j(u) phi^j(v))
```

contains a singlet channel contraction. In phase space, the product of bilocal kernels is ordinary operator composition:

```text
(K_1 \circ K_2)(x,z) = \int d^3y K_1(x,y) K_2(y,z).
```

Under the Wigner transform, operator composition becomes the Moyal star product:

```text
W[K_1 \circ K_2] = W[K_1] * W[K_2].
```

Therefore the algebra of tensionless string fields is precisely the oscillator star algebra used by Vasiliev.

### 6.3 Gauge symmetry from singlet constraints

The singlet constraint in the vector model removes nonsinglet degrees of freedom. In the bilocal language, it becomes a redundancy under changes of basis of the singleton Hilbert space:

```text
Psi -> U^{-1} Psi U.
```

Infinitesimally,

```text
delta Psi = [epsilon, Psi].
```

Under the Wigner transform this becomes

```text
delta Phi = epsilon * Phi - Phi * epsilon.
```

This is the adjoint action of the higher-spin algebra. Thus higher-spin gauge symmetry is the bulk expression of the redundancy in the singleton bilocal description.

---

## 7. Linearized Vasiliev theory from the tensionless string

### 7.1 Master fields

The linearized type-A Vasiliev system uses two master fields:

1. a one-form connection

```text
W(x;Y) = dx^mu W_mu(x;Y),
```

containing the spin connections and frame-like gauge fields for all even spins;

2. a zero-form

```text
B(x;Y),
```

containing the scalar and generalized Weyl tensors.

The AdS vacuum is a flat `sp(4)` connection:

```text
W_0 = (1/4i) (omega_0^{AB} + h_0^{AB}) Y_A Y_B,
qquad
d W_0 + W_0 * W_0 = 0.
```

Linearized fluctuations obey

```text
d w + W_0 * w + w * W_0 = 0,
```

up to source terms from the Weyl zero-form, and

```text
D_0 B = dB + W_0 * B - B * pi(W_0) = 0,
```

where `pi` flips the sign of one chirality of oscillators, e.g.

```text
pi(y,\bar y)=(-y,\bar y).
```

### 7.2 Matching to the string spectrum

Expand the master connection in oscillator degree:

```text
W(x;Y) = \sum_{m,n} W_{alpha(m) dot alpha(n)}(x)
          y^{alpha1}...y^{alpham}
          \bar y^{dot alpha1}...\bar y^{dot alphan}.
```

The spin-`s` gauge field sits at total oscillator degree

```text
m+n = 2(s-1).
```

The minimal bosonic projection keeps even spins. The zero-form similarly packages all on-shell curvatures:

```text
C_{alpha(2s)}(x),
\bar C_{dot alpha(2s)}(x).
```

This is exactly the oscillator expansion of the tensionless closed string field after the Regge tower has collapsed. The string oscillator number is replaced by oscillator polynomial degree in `Y`.

### 7.3 BRST interpretation

The covariant string field equation has the universal form

```text
Q_B Phi + Phi * Phi = 0,
```

where `Q_B` is the BRST operator and `*` is the string field product. In the tensionless AdS singleton limit,

```text
Q_B -> D_0,
```

and the product becomes the Moyal product. Therefore the linearized and cubic equations become

```text
D_0 Phi + Phi * Phi = 0.
```

Resolving this equation into frame-like components and including the twisted-adjoint zero-form gives the Vasiliev unfolded system. This is the dynamical bridge between string field theory and higher-spin gravity.

---

## 8. Nonlinear completion: why the Vasiliev equations are forced

### 8.1 The need for auxiliary `Z` variables

The nonlinear higher-spin equations cannot be written solely with the physical oscillator variables `Y` while maintaining manifest gauge covariance and integrability. Vasiliev's construction introduces auxiliary oscillators

```text
Z_A = (z_alpha, \bar z_{dot alpha})
```

with star-commutation relations opposite to those of `Y`:

```text
[Z_A,Z_B]_* = -2i C_{AB},
[Y_A,Z_B]_* = 0.
```

The extended star product acts on functions of `(Y,Z)`. The `Z` variables are not extra physical spacetime dimensions or particles. They provide a homological resolution of the nonlinear constraints, analogous to auxiliary fields in string field theory.

### 8.2 Master fields in extended space

The full system uses:

```text
W = dx^mu W_mu(x;Y,Z),
S = dZ^A S_A(x;Y,Z),
B = B(x;Y,Z).
```

Here `W` is the spacetime connection, `S` is the auxiliary connection in `Z` space, and `B` is the twisted-adjoint zero-form.

### 8.3 Vasiliev equations

In a standard convention, the bosonic equations take the schematic form

```text
d_x W + W * W = 0,

d_x S + W * S + S * W = 0,

d_x B + W * B - B * pi(W) = 0,

S * B = B * pi(S),

S * S = -i dz^alpha dz_alpha [1 + B * kappa]
        -i d\bar z^{dot alpha} d\bar z_{dot alpha} [1 + B * \bar kappa].
```

The inner Kleinians are

```text
kappa = exp(i y_alpha z^alpha),
\bar kappa = exp(-i \bar y_{dot alpha} \bar z^{dot alpha}).
```

Reality and projection conditions select the desired model. The type-A theory is parity even; the type-B theory is parity odd. A continuous parity-violating phase is possible in more general versions and is related holographically to Chern-Simons vector models.

### 8.4 Derivation from zero-tension string field theory

The nonlinear string field equation in the tensionless limit is a Maurer-Cartan equation in the algebra of singleton kernels:

```text
Q Phi + Phi * Phi = 0.
```

The proof that this becomes Vasiliev theory consists of the following steps.

**Step 1: identify the algebra.**  
The zero-tension string product is kernel composition in singleton Hilbert space. Its Wigner transform is the Moyal product of `(Y,Z)` oscillators.

**Step 2: identify the differential.**  
The BRST differential reduces to the sum of the AdS covariant derivative and the auxiliary resolution differential:

```text
Q -> d_x + d_Z + [W_0 + S_0, ·]_* .
```

**Step 3: split the string field.**  
The total string field decomposes into a connection-like part and a twisted-adjoint part:

```text
Phi -> W + S + B.
```

This split is forced by the two possible actions of the higher-spin algebra on singleton bilinears: adjoint for gauge connections and twisted-adjoint for physical curvatures.

**Step 4: impose integrability.**  
The nilpotency of the string BRST charge and associativity of the star product imply

```text
Q^2 = 0,
qquad
Q(A*B)=Q(A)*B+(-1)^A A*Q(B).
```

Hence the Maurer-Cartan equation is integrable:

```text
Q(QPhi+Phi*Phi)+[Phi,QPhi+Phi*Phi]_* = 0.
```

The most general integrable deformation preserving the minimal bosonic projection and the singleton ideal is the Vasiliev deformation proportional to `B*kappa` and `B*\bar kappa`.

**Step 5: recover physical fields.**  
Gauge-fixing the `Z` dependence and solving the auxiliary equations expresses all `Z` components in terms of the physical spacetime fields in `W(x;Y,0)` and `B(x;Y,0)`. These fields obey the Fronsdal equations at linear order and the Vasiliev interactions at higher order.

Thus Vasiliev's equations are not added by hand. They are the homological completion of the tensionless singleton string field equation.

---

## 9. Cubic couplings and correlator matching

### 9.1 CFT fixes the cubic vertices

In a conformal field theory, the three-point functions of conserved currents are strongly constrained. For the free scalar vector model, the correlators

```text
< J_{s1} J_{s2} J_{s3} >
```

are fixed up to normalization by conformal symmetry, conservation, and parity. In AdS, these correlators determine the cubic couplings among the dual higher-spin fields.

Therefore the cubic Vasiliev vertices must reproduce the free-vector-model current correlators. This gives an unambiguous test of the string-limit derivation.

### 9.2 Oscillator overlap gives the correct structure constants

The cubic vertex of the bilocal collective theory comes from expanding

```text
- (N/2) Tr log Psi
```

around the saddle. The cubic term is essentially

```text
V_3 ~ Tr(Psi_0^{-1} eta Psi_0^{-1} eta Psi_0^{-1} eta).
```

In Wigner variables, the trace of kernel products becomes

```text
Tr(K_1 K_2 K_3)
= \int dX dY Phi_1(X,Y) * Phi_2(X,Y) * Phi_3(X,Y).
```

This is precisely the oscillator-overlap form of the cubic string field vertex. Its structure constants are those of the higher-spin algebra. Consequently the cubic couplings agree with type-A Vasiliev theory.

### 9.3 Normalization and Newton's constant

The two-point functions of vector-model currents scale as

```text
< J_s J_s > ~ N.
```

Canonical normalization of bulk fields therefore gives

```text
G_N / R^2 ~ 1/N.
```

Equivalently,

```text
g_s ~ 1/N.
```

The higher-spin interaction strength is controlled by `1/sqrt(N)` for canonically normalized cubic vertices, as expected for closed-string interactions.

### 9.4 Boundary conditions and the critical model

The bulk scalar in type-A Vasiliev theory has

```text
m^2 R^2 = -2,
```

which allows two quantizations in `AdS_4`:

```text
Delta = 1,
qquad Delta = 2.
```

The `Delta=1` boundary condition is dual to the free `O(N)` vector model. The `Delta=2` boundary condition is dual to the critical `O(N)` model. Higher-spin symmetry remains exact at leading order in `1/N`, while at subleading order the critical model has weakly broken higher-spin symmetry.

---

## 10. Finite tension as higher-spin symmetry breaking

### 10.1 What finite tension would do

A finite string tension would lift the degeneracy of the higher-spin tower. In CFT terms, finite tension corresponds to anomalous dimensions for the higher-spin currents:

```text
Delta_s = s + 1 + gamma_s.
```

Nonzero `gamma_s` means the current is no longer conserved:

```text
partial · J_s != 0.
```

In the bulk, the spin-`s` field becomes massive by eating a lower-spin Goldstone mode. Thus string tension is holographically equivalent to higher-spin symmetry breaking.

### 10.2 Vector models versus matrix models

In matrix large-`N` gauge theories, a tunable 't Hooft coupling controls the string tension. At weak coupling, many higher-spin currents are approximately conserved; at strong coupling, they acquire large anomalous dimensions and only the low-spin supergravity modes remain light.

In the pure `O(N)` vector model, there is no analogous large 't Hooft coupling. The theory remains at the higher-spin symmetric point in the strict `N=infinity` limit. Therefore it directly describes the tensionless string rather than a finite-tension deformation.

### 10.3 Chern-Simons vector models as partially broken phases

Coupling the vector model to Chern-Simons gauge fields produces a family of theories with slightly broken higher-spin symmetry at large `N` and fixed 't Hooft coupling

```text
lambda_CS = N/k.
```

The bulk dual is a parity-violating Vasiliev theory with a phase depending on `lambda_CS`. This is not a conventional finite-tension string in the matrix-model sense, but it demonstrates how deformations of the singleton string appear as controlled deformations of Vasiliev theory.

---

## 11. Proof of the main theorem

We now assemble the derivation in theorem-proof form.

### Theorem

Given assumptions A1-A5 of Section 1.2, the zero-tension limit of the AdS string field theory is the minimal type-A Vasiliev theory on `AdS_4`, with classical coupling `G_N/R^2 ~ 1/N`, and holographic dual the singlet sector of the free or critical `O(N)` vector model depending on the scalar boundary condition.

### Proof

**1. Spectrum.**  
By A1, the elementary zero-tension boundary degrees of freedom transform as scalar singletons `Rac` of `SO(3,2)`. By A2, the physical closed-string Hilbert space is the singlet square `Sym^2(Rac)`. The Flato-Fronsdal theorem gives

```text
Sym^2(Rac) = D(1,0) \oplus \bigoplus_{s=2,4,6,...} D(s+1,s).
```

This is exactly the spectrum of the minimal bosonic type-A Vasiliev theory: one scalar plus one massless gauge field for every even spin `s >= 2`. Therefore the zero-tension string spectrum equals the Vasiliev spectrum.

**2. Gauge algebra.**  
The algebra of endomorphisms of the singleton representation, modulo the annihilator ideal, is

```text
hs(4) = U(so(3,2))/Ann(Rac).
```

In oscillator variables this is the even Weyl algebra with Moyal product. By A3, the tensionless string field product is precisely this oscillator product. Hence the enhanced gauge algebra of the tensionless string is `hs(4)`, the Vasiliev higher-spin algebra.

**3. Linearized dynamics.**  
The string BRST operator becomes the AdS covariant derivative acting on singleton-bilinear fields. Its cohomology consists of massless AdS representations `D(s+1,s)`. Written in oscillator variables, the cohomology is represented by the master one-form `W(x;Y)` and zero-form `B(x;Y)` satisfying the linearized unfolded equations. These equations are equivalent to the Fronsdal equations for all even spins plus the scalar equation with `m^2 R^2=-2`.

**4. Cubic interactions.**  
By A3, the cubic string vertex is the canonical overlap vertex. Under the Wigner transform this is the trace of three Moyal-multiplied master fields. The structure constants are therefore those of `hs(4)`. Gauge invariance under `hs(4)` fixes the cubic vertices, and these are the type-A Vasiliev cubic vertices. Equivalently, the resulting Witten diagrams reproduce the unique free-scalar vector-model three-point functions of conserved currents.

**5. Nonlinear completion.**  
Associativity of the star product and nilpotency of the BRST differential imply the Maurer-Cartan integrability condition. The unique formal integrable nonlinear completion preserving `SO(3,2)`, the bosonic projection, the twisted-adjoint scalar sector, and the singleton ideal is Vasiliev's unfolded system with auxiliary `Z` variables. The `Z` variables are the homological resolution of the nonlinear constraints; solving them perturbatively gives interactions among the physical fields in `W(x;Y,0)` and `B(x;Y,0)`.

**6. Holographic dictionary.**  
The scalar singleton is the elementary field `phi^i` of the boundary vector model. The closed-string singlet bilinear is the collective field `Psi(x,y)=phi^i(x)phi^i(y)/N`. Its expansion gives conserved currents `J_s`, which source the bulk spin-`s` gauge fields. The normalization of current correlators gives `G_N/R^2 ~ 1/N`. The scalar boundary condition selects the free or critical vector model.

Therefore all defining data of the zero-tension string limit—spectrum, gauge algebra, linear equations, interactions, coupling, and boundary dictionary—coincide with those of minimal type-A Vasiliev theory. This proves the theorem. `□`

---

## 12. Why this is a string limit rather than merely a higher-spin field theory

A skeptic may object that the derivation starts from singletons and bilocals rather than from a conventional Polyakov worldsheet. The response is that the relevant notion of string theory in the tensionless regime is string field theoretic and holographic.

A conventional finite-tension string has:

| Tensile string concept | Tensionless/vector-model realization |
|---|---|
| Worldsheet oscillators | singleton bilocal modes |
| closed-string field | collective bilocal field `Psi(x,y)` |
| string product | kernel composition / Moyal star product |
| Regge tower | conserved higher-spin currents |
| string coupling | `g_s ~ 1/N` |
| tension | higher-spin symmetry breaking scale |
| BRST equation | unfolded higher-spin Maurer-Cartan equation |
| spacetime equations | Vasiliev equations |

The zero-tension limit is singular from the worldsheet point of view. The worldsheet metric degenerates, and the usual separation between low-energy fields and massive string states disappears. The bilocal/string-field formulation is the correct non-singular variable set at the tensionless point.

Thus Vasiliev theory is a string limit in the same operational sense that supergravity is a low-energy string limit: it is the universal spacetime field theory selected by the limiting spectrum, symmetries, and string field product.

---

## 13. Holography without supersymmetry or matrix large N

The derivation clarifies why the Klebanov-Polyakov duality is a proof of principle for holography in its most economical form.

### 13.1 No supersymmetry required

The boundary `O(N)` vector model can be purely bosonic. The bulk type-A Vasiliev theory is also purely bosonic. The duality relies on conformal symmetry, singlet projection, large `N`, and higher-spin symmetry, not supersymmetry.

### 13.2 No matrix gauge theory required

The vector model has `O(N)` fundamental fields, not `N x N` matrix fields. Its singlet bilinears scale like closed-string single-particle states, but the number of degrees of freedom is `O(N)`, not `O(N^2)`. Consequently

```text
G_N^{-1} ~ N
```

rather than `N^2`. This shows that holography does not require a matrix gauge theory; matrix theories are one route to string worldsheets, but vector models realize the tensionless limit directly.

### 13.3 Emergent dimension from bilocality

The extra AdS radial dimension arises from the relative separation or relative momentum of the bilocal field. This gives a concrete mechanism for emergent bulk geometry in a non-matrix theory.

### 13.4 Gravity as one gauge field in an infinite multiplet

The spin-2 graviton is present, but it is not isolated. It belongs to an infinite higher-spin gauge multiplet. Einstein gravity emerges only after higher-spin symmetry is broken or after a regime is reached in which higher-spin fields become heavy. The vector model instead describes the opposite endpoint: the fully symmetric tensionless string.

---

## 14. Limitations and open problems

This white paper gives a proof-of-principle derivation, not a completed construction of a conventional finite-tension parent string. Important limitations remain.

### 14.1 Finite-tension completion

No explicit critical finite-tension string background is known whose smooth `alpha' -> infinity` limit has been rigorously shown to be minimal type-A Vasiliev theory on `AdS_4`. The theorem identifies the universality class such a parent must have.

### 14.2 Locality

Higher-spin interactions in AdS involve infinitely many derivatives. Vasiliev theory is local in the unfolded/twistor sense but not local in the same Wilsonian sense as low-spin effective field theory. Understanding the precise notion of admissible field redefinitions remains an active issue.

### 14.3 Bulk action

Vasiliev theory is most naturally formulated as equations of motion rather than from a simple covariant spacetime action. The bilocal collective action supplies an action principle in holographic variables, but translating it into a compact local bulk action is nontrivial.

### 14.4 Quantum completion

The `1/N` expansion of the vector model gives the quantum expansion of the bulk theory. A fully intrinsic bulk quantization of Vasiliev theory matching all finite-`N` effects remains difficult.

### 14.5 Beyond type A

Other singleton choices yield other higher-spin theories: fermionic singletons give type-B models; supersingletons give supersymmetric higher-spin theories; Chern-Simons matter theories give parity-violating phases. A broader classification of tensionless string limits should be organized by singleton categories and their tensor products.

---

## 15. Research program implied by the derivation

The derivation suggests a concrete program for making the string origin of Vasiliev theory increasingly explicit.

1. **Construct the singleton worldsheet.**  
   Develop a first-quantized worldsheet or ambitwistor-like model whose BRST cohomology is the scalar singleton and whose closed sector is the singleton square.

2. **Derive the Moyal vertex from a degenerate worldsheet.**  
   Show directly that the zero-tension pair-of-pants amplitude reduces to the oscillator overlap vertex.

3. **Systematize the bilocal-to-bulk canonical map.**  
   Produce explicit formulas relating bilocal phase-space variables to AdS Fronsdal fields for all spins.

4. **Quantize the collective string field.**  
   Match one-loop bulk determinants and finite-`N` constraints with vector-model singlet partition functions.

5. **Identify finite-tension deformations.**  
   Determine which deformations of the vector model correspond to genuine string tension rather than merely parity phases or boundary-condition changes.

6. **Clarify locality and observables.**  
   Define a higher-spin-invariant notion of bulk locality appropriate to the tensionless phase.

---

## 16. Conclusion

The tensionless string limit in AdS is not a limit in which string theory disappears into an ordinary low-energy gravitational theory. It is the opposite: all string modes become equally important, and the organizing principle becomes an infinite-dimensional higher-spin gauge symmetry.

For `AdS_4`, the scalar singleton provides the fundamental bit of this tensionless string. The closed string is the singlet bilinear of two singletons. By the Flato-Fronsdal theorem, this bilinear contains exactly the massless spectrum of type-A Vasiliev gravity. By the Wigner transform, the algebra of bilocals becomes the oscillator Moyal algebra of Vasiliev theory. By the large-`N` collective action, the bilocal theory has the interaction and genus structure of a closed string field theory. By homological completion of the tensionless string Maurer-Cartan equation, one obtains the full nonlinear Vasiliev equations.

Thus the Klebanov-Polyakov duality is not merely an analogy between a vector model and a higher-spin field theory. It is the cleanest known realization of holographic string theory at zero tension:

```text
O(N) singlet vector model
      = boundary gauge-fixed tensionless singleton string
      = type-A Vasiliev higher-spin gravity on AdS_4.
```

This provides a proof of principle for holography independent of supersymmetry and independent of matrix large-`N` gauge theory. Supersymmetric matrix models describe one powerful corner of holography; higher-spin/vector duality describes another, more primitive corner, where the string is tensionless, the worldsheet is replaced by singleton bilocals, and spacetime gauge symmetry is enlarged from diffeomorphisms to the full higher-spin algebra.

---

## Appendix A. Key equations

### A.1 Tensionless parameter

```text
lambda_s = R_AdS^2 / alpha',
qquad
lambda_s -> 0.
```

### A.2 Flato-Fronsdal decomposition

```text
Rac \otimes Rac = \bigoplus_{s=0}^{\infty} D(s+1,s).
```

Minimal bosonic projection:

```text
Sym^2(Rac)=D(1,0) \oplus \bigoplus_{s=2,4,6,...}D(s+1,s).
```

### A.3 Higher-spin algebra

```text
hs(4)=U(so(3,2))/Ann(Rac).
```

Oscillator form:

```text
[Y_A,Y_B]_* = 2i C_{AB}.
```

### A.4 Bilocal collective field

```text
Psi(x,y)=\frac{1}{N} phi^i(x) phi^i(y).
```

Collective action:

```text
S_coll[Psi]
= N/2 Tr[-partial_x^2 Psi(x,y)|_{x=y}]
  - N/2 Tr log Psi.
```

### A.5 Vasiliev master equations, schematic

```text
d_x W + W * W = 0,

d_x B + W * B - B * pi(W) = 0,

d_x S + W * S + S * W = 0,

S * B = B * pi(S),

S * S = -i dz^alpha dz_alpha [1 + B * kappa]
        -i d\bar z^{dot alpha} d\bar z_{dot alpha} [1 + B * \bar kappa].
```

### A.6 Bulk coupling

```text
G_N/R^2 ~ 1/N,
qquad
g_s ~ 1/N.
```

---

## Appendix B. Dictionary

| Boundary/vector model | Bulk/tensionless string | Vasiliev variable |
|---|---|---|
| scalar `phi^i` | singleton bit | `Rac` |
| singlet bilinear `phi^i(x)phi^i(y)` | closed tensionless string field | bilocal `Psi(x,y)` |
| conserved current `J_s` | massless spin-`s` state | component of `W`, `B` |
| current conservation | gauge invariance | `delta h_s = nabla xi_{s-1}` |
| operator product of bilocals | string joining/splitting | Moyal star product |
| large `N` | classical bulk | `G_N ~ 1/N` |
| `1/N` corrections | string loops | quantum Vasiliev corrections |
| scalar boundary condition `Delta=1` | free vector model | type-A alternate quantization |
| scalar boundary condition `Delta=2` | critical vector model | type-A standard quantization |

---

## Appendix C. Suggested references for a final scholarly version

A final publishable manuscript should cite, at minimum, the foundational literature on:

1. Vasiliev's nonlinear higher-spin equations in four dimensions;
2. the Flato-Fronsdal theorem and singleton representations;
3. the Klebanov-Polyakov conjecture relating type-A higher-spin gravity on `AdS_4` to the `O(N)` vector model;
4. collective-field and bilocal formulations of vector-model holography;
5. Giombi-Yin and related tests of higher-spin/vector-model correlators;
6. tensionless strings, high-energy string symmetry, and AdS higher-spin limits;
7. Chern-Simons vector models and parity-violating Vasiliev theories;
8. unfolded dynamics and oscillator/star-product formulations of higher-spin gravity.

This paper deliberately presents the derivation in a self-contained white-paper form. A reference-complete academic version should add detailed citations and convention-specific equation normalizations.

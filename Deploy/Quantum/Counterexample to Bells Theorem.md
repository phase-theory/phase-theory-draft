# Counterexample to Bell’s Theorem: A Local, Measurement-Dependent Hidden-Variable Construction for the Singlet Correlations

**Preprint format**

---

## Abstract

Bell’s theorem is frequently stated in the unqualified form: *no local hidden-variable theory can reproduce the quantum-mechanical correlations of the singlet state*. In this paper I construct an explicit local hidden-variable model that reproduces the full two-spin singlet correlation  
\[
E_{\psi^-}(\mathbf a,\mathbf b)=-\mathbf a\cdot \mathbf b
\]
and violates the CHSH inequality up to the Tsirelson value \(2\sqrt 2\). The construction is deterministic at the level of local response functions and satisfies parameter independence and operational no-signalling. The model evades Bell’s inequality by replacing Bell’s statistical-independence assumption, often called measurement independence or free-choice independence, with a contextual probability kernel
\[
\rho(\lambda\mid \mathbf a,\mathbf b)\neq \rho(\lambda).
\]
Equivalently, the model is local but not describable by a single setting-independent probability space over counterfactual outcomes. The result is therefore a counterexample to the common physical reading of Bell’s theorem as a no-go theorem for all local hidden-variable theories. It is not a counterexample to the purely conditional mathematical statement that locality plus measurement independence implies Bell inequalities; rather, it exhibits precisely the premise whose removal makes local reproduction of the singlet correlations possible.

---

## 1. Introduction

Bell’s theorem is one of the most important results in the foundations of physics. In its standard 1964 form, it shows that certain correlations predicted by quantum mechanics for spatially separated measurements cannot be reproduced by a local hidden-variable theory satisfying a small number of apparently natural assumptions. The theorem has since been refined into the Clauser-Horne-Shimony-Holt (CHSH) inequality and has become the conceptual basis for a large number of experimental tests.

However, the theorem is often quoted in a stronger form than is strictly warranted. One commonly encounters the statement:

> *No local realistic theory can reproduce the quantum correlations.*

Taken literally, this statement is false unless one specifies precisely what is meant by “local realistic.” Bell’s actual derivation requires, in addition to locality and realism, an independence assumption connecting the hidden variables with the later measurement settings. This assumption is usually written as
\[
\rho(\lambda\mid \mathbf a,\mathbf b)=\rho(\lambda),
\]
where \(\lambda\) denotes the hidden state prepared at the source and \(\mathbf a,\mathbf b\) denote the measurement settings chosen at the two wings of the experiment.

The purpose of this paper is to construct an explicit counterexample to the unrestricted version of Bell’s theorem. The counterexample is not a loophole involving detector inefficiency, coincidence selection, or memory effects, although those are also known ways of evading particular experimental forms of Bell inequalities. Instead, the counterexample attacks the most important conceptual premise: the assumption that the distribution of hidden variables is independent of the measurement settings.

The main results are as follows.

1. I give a deterministic local hidden-variable model for the singlet state.
2. The model reproduces exactly the quantum joint probabilities
   \[
   P_{\psi^-}(\alpha,\beta\mid \mathbf a,\mathbf b)
   =
   \frac14\left(1-\alpha\beta\,\mathbf a\cdot\mathbf b\right),
   \qquad \alpha,\beta\in\{+1,-1\}.
   \]
3. The model violates the CHSH inequality up to
   \[
   |S|=2\sqrt 2.
   \]
4. The model satisfies parameter independence and operational no-signalling.
5. The model violates measurement independence, thereby exposing the precise assumption required for Bell’s inequality.

The construction shows that Bell inequalities are not consequences of locality alone. They are constraints on theories that admit a single, setting-independent probability measure over hidden variables and counterfactual outcomes. Once this requirement is relaxed, local models can reproduce the quantum singlet correlations exactly.

---

## 2. Bell’s Theorem in Standard Form

Consider a bipartite experiment. Two spacelike-separated observers, traditionally called Alice and Bob, choose measurement settings
\[
\mathbf a,\mathbf a'\in S^2,
\qquad
\mathbf b,\mathbf b'\in S^2,
\]
and obtain binary outcomes
\[
A,B\in\{+1,-1\}.
\]

A deterministic local hidden-variable model assumes the existence of a measurable space \((\Lambda,\Sigma,\mu)\), where \(\lambda\in\Lambda\) is the hidden variable. The outcomes are functions
\[
A_{\mathbf a}(\lambda)\in\{+1,-1\},
\qquad
B_{\mathbf b}(\lambda)\in\{+1,-1\}.
\]

The correlation predicted by the model is
\[
E(\mathbf a,\mathbf b)
=
\int_\Lambda d\mu(\lambda)\,
A_{\mathbf a}(\lambda)B_{\mathbf b}(\lambda).
\]

Bell’s derivation uses three assumptions.

### 2.1 Realism or hidden-variable completeness

There exists a hidden variable \(\lambda\) that determines, or at least statistically governs, the outcomes of all possible measurements.

### 2.2 Locality or factorization

In the deterministic case, locality means that Alice’s outcome depends only on \(\mathbf a\) and \(\lambda\), while Bob’s outcome depends only on \(\mathbf b\) and \(\lambda\):
\[
A=A(\mathbf a,\lambda),
\qquad
B=B(\mathbf b,\lambda).
\]

In a stochastic theory, the corresponding condition is
\[
P(A,B\mid \mathbf a,\mathbf b,\lambda)
=
P(A\mid \mathbf a,\lambda)
P(B\mid \mathbf b,\lambda).
\]

### 2.3 Measurement independence

The hidden variable distribution is independent of the later measurement settings:
\[
\rho(\lambda\mid \mathbf a,\mathbf b)=\rho(\lambda).
\]

Equivalently, the source variables and the setting choices are statistically independent.

From these assumptions one derives the CHSH inequality. Define
\[
S
=
E(\mathbf a,\mathbf b)
+
E(\mathbf a,\mathbf b')
+
E(\mathbf a',\mathbf b)
-
E(\mathbf a',\mathbf b').
\]

Then
\[
\begin{aligned}
S
&=
\int_\Lambda d\mu(\lambda)
\Big[
A_{\mathbf a}B_{\mathbf b}
+
A_{\mathbf a}B_{\mathbf b'}
+
A_{\mathbf a'}B_{\mathbf b}
-
A_{\mathbf a'}B_{\mathbf b'}
\Big]
\\
&=
\int_\Lambda d\mu(\lambda)
\Big[
A_{\mathbf a}
\big(
B_{\mathbf b}+B_{\mathbf b'}
\big)
+
A_{\mathbf a'}
\big(
B_{\mathbf b}-B_{\mathbf b'}
\big)
\Big].
\end{aligned}
\]

Since \(B_{\mathbf b},B_{\mathbf b'}\in\{+1,-1\}\), one of the two brackets equals \(\pm 2\) and the other equals \(0\), or vice versa. Therefore the integrand has magnitude at most \(2\), and hence
\[
|S|\le 2.
\]

This is the CHSH inequality.

---

## 3. Quantum Singlet Correlations

The spin-singlet state of two spin-\(\frac12\) particles is
\[
|\psi^-\rangle
=
\frac{1}{\sqrt 2}
\left(
|\uparrow\rangle\otimes|\downarrow\rangle
-
|\downarrow\rangle\otimes|\uparrow\rangle
\right).
\]

Its density operator may be written using Pauli matrices as
\[
\rho_{\psi^-}
=
|\psi^-\rangle\langle\psi^-|
=
\frac14
\left(
I\otimes I
-
\sigma_i\otimes\sigma_i
\right),
\]
where Einstein summation over \(i=1,2,3\) is understood and
\[
\sigma_i
\]
are the Pauli matrices.

For spin measurements along unit vectors \(\mathbf a,\mathbf b\in S^2\), the observables are
\[
\hat A_{\mathbf a}
=
\boldsymbol\sigma\cdot\mathbf a
=
\sigma_i a^i,
\qquad
\hat B_{\mathbf b}
=
\boldsymbol\sigma\cdot\mathbf b
=
\sigma_j b^j.
\]

The quantum correlation is
\[
\begin{aligned}
E_{\psi^-}(\mathbf a,\mathbf b)
&=
\operatorname{Tr}
\left[
\rho_{\psi^-}
\left(
\boldsymbol\sigma\cdot\mathbf a
\otimes
\boldsymbol\sigma\cdot\mathbf b
\right)
\right]
\\
&=
-\delta_{ij}a^i b^j
\\
&=
-\mathbf a\cdot\mathbf b.
\end{aligned}
\]

The corresponding joint probabilities are
\[
P_{\psi^-}(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\left(
1-\alpha\beta\,\mathbf a\cdot\mathbf b
\right),
\qquad
\alpha,\beta\in\{+1,-1\}.
\]

Choosing coplanar settings
\[
\mathbf a=0^\circ,
\quad
\mathbf a'=90^\circ,
\quad
\mathbf b=45^\circ,
\quad
\mathbf b'=-45^\circ,
\]
one obtains
\[
|S|=2\sqrt 2,
\]
which violates the CHSH bound \(2\).

---

## 4. The Structural Source of Bell’s No-Go Result

Bell’s inequality is often interpreted as a consequence of locality. But the mathematical structure of the theorem is stronger than that. The inequality requires the existence of a single probability space supporting all four counterfactual random variables
\[
A_{\mathbf a},
\quad
A_{\mathbf a'},
\quad
B_{\mathbf b},
\quad
B_{\mathbf b'}.
\]

Equivalently, Bell’s theorem requires a joint probability distribution
\[
P(A_{\mathbf a},A_{\mathbf a'},B_{\mathbf b},B_{\mathbf b'})
\]
whose marginals reproduce the observed pairwise distributions. This is the content of Fine’s theorem: for binary outcomes, satisfaction of all CHSH inequalities is equivalent to the existence of such a joint distribution.

The counterexample developed below rejects exactly this global Kolmogorovian structure. It assigns a probability measure to each experimental context \((\mathbf a,\mathbf b)\):
\[
\mu_{\mathbf a,\mathbf b}.
\]
There is no requirement that these measures be marginals of one single global measure. Thus the model is local at the level of each actual experiment but does not admit a global counterfactual completion.

In compact form, Bell’s standard model is
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\int d\lambda\,
\rho(\lambda)
P_A(\alpha\mid \mathbf a,\lambda)
P_B(\beta\mid \mathbf b,\lambda).
\]

The counterexample replaces this with
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\int d\lambda\,
\rho(\lambda\mid \mathbf a,\mathbf b)
P_A(\alpha\mid \mathbf a,\lambda)
P_B(\beta\mid \mathbf b,\lambda).
\]

The second equation preserves local response but abandons measurement independence.

---

## 5. General Measurement-Dependent Local Representation

Before constructing the explicit geometric model, it is useful to state a general proposition.

### Proposition 1

Let
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
\]
be any nonsignalling bipartite probability distribution with binary outcomes. Then there exists a local deterministic hidden-variable representation with measurement-dependent measure.

### Proof

Take the hidden-variable space to be
\[
\Lambda=\{+1,-1\}\times\{+1,-1\}.
\]

For each setting pair \((\mathbf a,\mathbf b)\), define
\[
\rho_{\mathbf a,\mathbf b}(\alpha,\beta)
=
P(\alpha,\beta\mid \mathbf a,\mathbf b).
\]

Let
\[
A(\mathbf a,\alpha,\beta)=\alpha,
\qquad
B(\mathbf b,\alpha,\beta)=\beta.
\]

Then
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\sum_{\lambda\in\Lambda}
\rho_{\mathbf a,\mathbf b}(\lambda)
\delta_{A(\mathbf a,\lambda),\alpha}
\delta_{B(\mathbf b,\lambda),\beta}.
\]

The response functions are local:
\[
A(\mathbf a,\alpha,\beta)
\]
does not depend on \(\mathbf b\), and
\[
B(\mathbf b,\alpha,\beta)
\]
does not depend on \(\mathbf a\).

Operational no-signalling follows from the assumed no-signalling property of \(P\):
\[
\sum_\beta P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
P_A(\alpha\mid \mathbf a),
\]
which is independent of \(\mathbf b\).

Thus any nonsignalling behavior can be represented locally if one allows the hidden-variable measure to depend on the measurement context. \(\square\)

This proposition already demonstrates that locality alone is insufficient to imply Bell inequalities. However, the construction is abstract. To make the counterexample physically transparent, I now give an explicit geometric model for the singlet state.

---

## 6. A Geometric Local Counterexample for the Singlet State

### 6.1 Settings and hidden space

Let
\[
\mathbf a,\mathbf b\in S^2
\]
be unit vectors. Define the angle \(\theta\) between them by
\[
\cos\theta=\mathbf a\cdot\mathbf b,
\qquad
0\le \theta\le \pi.
\]

For non-collinear \(\mathbf a,\mathbf b\), let
\[
\Pi(\mathbf a,\mathbf b)=\operatorname{span}\{\mathbf a,\mathbf b\}
\]
be the plane spanned by the two settings. The hidden variable is a unit vector
\[
\lambda\in S^1_{\mathbf a,\mathbf b}
\subset
\Pi(\mathbf a,\mathbf b),
\]
where \(S^1_{\mathbf a,\mathbf b}\) is the unit circle in that plane.

Choose an oriented orthonormal basis
\[
\mathbf e_1=\mathbf a,
\qquad
\mathbf e_2=
\frac{\mathbf b-(\mathbf a\cdot\mathbf b)\mathbf a}{\sin\theta}.
\]

Then
\[
\mathbf b=\cos\theta\,\mathbf e_1+\sin\theta\,\mathbf e_2.
\]

Parameterize the hidden vector by an angle \(\phi\in[0,2\pi)\):
\[
\lambda(\phi)
=
\cos\phi\,\mathbf e_1
+
\sin\phi\,\mathbf e_2.
\]

Then
\[
\mathbf a\cdot\lambda=\cos\phi,
\]
and
\[
\mathbf b\cdot\lambda
=
\cos\theta\cos\phi+\sin\theta\sin\phi
=
\cos(\phi-\theta).
\]

### 6.2 Local deterministic response functions

Define the local outcomes by
\[
A(\mathbf a,\lambda)
=
\operatorname{sgn}(\mathbf a\cdot\lambda),
\]
and
\[
B(\mathbf b,\lambda)
=
-\operatorname{sgn}(\mathbf b\cdot\lambda).
\]

In the parameterization above,
\[
A(\phi)=\operatorname{sgn}(\cos\phi),
\]
and
\[
B(\phi)=-\operatorname{sgn}(\cos(\phi-\theta)).
\]

The cases in which \(\cos\phi=0\) or \(\cos(\phi-\theta)=0\) form a set of measure zero and may be assigned arbitrarily.

The important point is that Alice’s response depends only on \(\mathbf a\) and \(\lambda\), while Bob’s response depends only on \(\mathbf b\) and \(\lambda\). There is no direct dependence of \(A\) on \(\mathbf b\), nor of \(B\) on \(\mathbf a\).

---

## 7. The Contextual Probability Measure

The essential ingredient of the counterexample is the probability measure on the hidden circle. For each setting pair \((\mathbf a,\mathbf b)\), define a measure \(\mu_{\mathbf a,\mathbf b}\) on \(S^1_{\mathbf a,\mathbf b}\) by the density
\[
\rho_{\mathbf a,\mathbf b}(\phi)
=
\begin{cases}
c_+(\theta),
&
\operatorname{sgn}(\cos\phi)
=
\operatorname{sgn}(\cos(\phi-\theta)),
\\[1ex]
c_-(\theta),
&
\operatorname{sgn}(\cos\phi)
\neq
\operatorname{sgn}(\cos(\phi-\theta)),
\end{cases}
\]
where
\[
c_+(\theta)
=
\frac{\cos^2(\theta/2)}{2(\pi-\theta)},
\]
and
\[
c_-(\theta)
=
\frac{\sin^2(\theta/2)}{2\theta}.
\]

Equivalently, in invariant notation,
\[
d\mu_{\mathbf a,\mathbf b}(\lambda)
=
\left[
c_+(\theta)\,
\mathbf 1_{\{(\mathbf a\cdot\lambda)(\mathbf b\cdot\lambda)>0\}}
+
c_-(\theta)\,
\mathbf 1_{\{(\mathbf a\cdot\lambda)(\mathbf b\cdot\lambda)<0\}}
\right]
d\ell(\lambda),
\]
where \(d\ell\) is arc length on the circle \(S^1_{\mathbf a,\mathbf b}\).

The limiting cases are understood by continuity:

- If \(\theta=0\), then \(\mathbf a=\mathbf b\), and
  \[
  d\mu_{\mathbf a,\mathbf a}(\lambda)=\frac{d\ell(\lambda)}{2\pi}.
  \]

- If \(\theta=\pi\), then \(\mathbf a=-\mathbf b\), and again the limiting measure is uniform.

---

## 8. Normalization of the Measure

The circle is divided into arcs on which the two signs agree and arcs on which they disagree.

For \(0<\theta<\pi\), the total arc length on which
\[
\operatorname{sgn}(\cos\phi)
=
\operatorname{sgn}(\cos(\phi-\theta))
\]
is
\[
L_+=2(\pi-\theta).
\]

The total arc length on which the signs disagree is
\[
L_-=2\theta.
\]

Therefore
\[
\int_0^{2\pi}
\rho_{\mathbf a,\mathbf b}(\phi)\,d\phi
=
L_+c_+(\theta)+L_-c_-(\theta).
\]

Substituting the definitions,
\[
\begin{aligned}
\int_0^{2\pi}
\rho_{\mathbf a,\mathbf b}(\phi)\,d\phi
&=
2(\pi-\theta)
\frac{\cos^2(\theta/2)}{2(\pi-\theta)}
+
2\theta
\frac{\sin^2(\theta/2)}{2\theta}
\\
&=
\cos^2(\theta/2)+\sin^2(\theta/2)
\\
&=
1.
\end{aligned}
\]

Thus \(\mu_{\mathbf a,\mathbf b}\) is a normalized probability measure.

---

## 9. Reproduction of the Singlet Marginals

The marginal probability that Alice obtains \(+1\) is
\[
P(A=+1\mid \mathbf a,\mathbf b)
=
\int_{\cos\phi>0}
\rho_{\mathbf a,\mathbf b}(\phi)\,d\phi.
\]

The region \(\cos\phi>0\) consists of an arc of length \(\pi-\theta\) on which the signs agree and an arc of length \(\theta\) on which they disagree. Hence
\[
\begin{aligned}
P(A=+1\mid \mathbf a,\mathbf b)
&=
(\pi-\theta)c_+(\theta)
+
\theta c_-(\theta)
\\
&=
(\pi-\theta)
\frac{\cos^2(\theta/2)}{2(\pi-\theta)}
+
\theta
\frac{\sin^2(\theta/2)}{2\theta}
\\
&=
\frac12\cos^2(\theta/2)
+
\frac12\sin^2(\theta/2)
\\
&=
\frac12.
\end{aligned}
\]

Similarly,
\[
P(B=+1\mid \mathbf a,\mathbf b)=\frac12.
\]

Thus both local marginals are uniformly random and independent of the distant setting.

---

## 10. Reproduction of the Singlet Correlation

Define the auxiliary sign functions
\[
s_{\mathbf a}(\lambda)=\operatorname{sgn}(\mathbf a\cdot\lambda),
\qquad
s_{\mathbf b}(\lambda)=\operatorname{sgn}(\mathbf b\cdot\lambda).
\]

Then
\[
A=s_{\mathbf a},
\qquad
B=-s_{\mathbf b}.
\]

Therefore
\[
AB=-s_{\mathbf a}s_{\mathbf b}.
\]

The correlation of the auxiliary signs is
\[
C(\mathbf a,\mathbf b)
=
\int_{S^1_{\mathbf a,\mathbf b}}
s_{\mathbf a}(\lambda)s_{\mathbf b}(\lambda)
\,d\mu_{\mathbf a,\mathbf b}(\lambda).
\]

On arcs where the signs agree, \(s_{\mathbf a}s_{\mathbf b}=+1\). On arcs where they disagree, \(s_{\mathbf a}s_{\mathbf b}=-1\). Therefore
\[
\begin{aligned}
C(\mathbf a,\mathbf b)
&=
L_+c_+(\theta)-L_-c_-(\theta)
\\
&=
2(\pi-\theta)
\frac{\cos^2(\theta/2)}{2(\pi-\theta)}
-
2\theta
\frac{\sin^2(\theta/2)}{2\theta}
\\
&=
\cos^2(\theta/2)-\sin^2(\theta/2)
\\
&=
\cos\theta.
\end{aligned}
\]

Since
\[
\cos\theta=\mathbf a\cdot\mathbf b,
\]
we have
\[
C(\mathbf a,\mathbf b)=\mathbf a\cdot\mathbf b.
\]

Thus the model predicts
\[
\begin{aligned}
E(\mathbf a,\mathbf b)
&=
\int AB\,d\mu_{\mathbf a,\mathbf b}
\\
&=
-\int s_{\mathbf a}s_{\mathbf b}\,d\mu_{\mathbf a,\mathbf b}
\\
&=
-\mathbf a\cdot\mathbf b.
\end{aligned}
\]

This is exactly the quantum singlet correlation.

---

## 11. Exact Reproduction of the Quantum Joint Probabilities

Because the local marginals vanish,
\[
\langle A\rangle=0,
\qquad
\langle B\rangle=0,
\]
and the correlation is
\[
\langle AB\rangle=-\mathbf a\cdot\mathbf b,
\]
the joint probabilities are completely determined. For binary outcomes,
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\left[
1
+
\alpha\langle A\rangle
+
\beta\langle B\rangle
+
\alpha\beta\langle AB\rangle
\right].
\]

Therefore
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\left(
1-\alpha\beta\,\mathbf a\cdot\mathbf b
\right).
\]

This is identical to the quantum-mechanical prediction for the singlet state:
\[
P_{\psi^-}(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\left(
1-\alpha\beta\,\mathbf a\cdot\mathbf b
\right).
\]

Thus the counterexample reproduces not merely the correlation function but the full observable bipartite statistics of the singlet state.

---

## 12. Violation of the CHSH Inequality

The model predicts
\[
E(\mathbf a,\mathbf b)=-\mathbf a\cdot\mathbf b.
\]

Choose coplanar settings with angular coordinates
\[
\mathbf a=0,
\qquad
\mathbf a'=\frac{\pi}{2},
\qquad
\mathbf b=\frac{\pi}{4},
\qquad
\mathbf b'=-\frac{\pi}{4}.
\]

Then
\[
E(\mathbf a,\mathbf b)
=
-\cos\frac{\pi}{4}
=
-\frac{1}{\sqrt2},
\]
\[
E(\mathbf a,\mathbf b')
=
-\cos\left(-\frac{\pi}{4}\right)
=
-\frac{1}{\sqrt2},
\]
\[
E(\mathbf a',\mathbf b)
=
-\cos\left(\frac{\pi}{2}-\frac{\pi}{4}\right)
=
-\frac{1}{\sqrt2},
\]
and
\[
E(\mathbf a',\mathbf b')
=
-\cos\left(\frac{\pi}{2}+\frac{\pi}{4}\right)
=
+\frac{1}{\sqrt2}.
\]

Hence
\[
\begin{aligned}
S
&=
E(\mathbf a,\mathbf b)
+
E(\mathbf a,\mathbf b')
+
E(\mathbf a',\mathbf b)
-
E(\mathbf a',\mathbf b')
\\
&=
-\frac{1}{\sqrt2}
-\frac{1}{\sqrt2}
-\frac{1}{\sqrt2}
-\frac{1}{\sqrt2}
\\
&=
-2\sqrt2.
\end{aligned}
\]

Therefore
\[
|S|=2\sqrt2.
\]

The model violates the CHSH inequality exactly as quantum mechanics does.

---

## 13. Why Bell’s Derivation Fails for the Counterexample

Bell’s CHSH derivation requires that the four correlations be written as integrals over a common measure \(\mu\):
\[
S
=
\int d\mu(\lambda)
\Big[
A_{\mathbf a}B_{\mathbf b}
+
A_{\mathbf a}B_{\mathbf b'}
+
A_{\mathbf a'}B_{\mathbf b}
-
A_{\mathbf a'}B_{\mathbf b'}
\Big].
\]

In the present model, however, the four terms are evaluated with four different contextual measures:
\[
\begin{aligned}
S
&=
\int d\mu_{\mathbf a,\mathbf b}(\lambda)\,
A_{\mathbf a}B_{\mathbf b}
\\
&\quad+
\int d\mu_{\mathbf a,\mathbf b'}(\lambda)\,
A_{\mathbf a}B_{\mathbf b'}
\\
&\quad+
\int d\mu_{\mathbf a',\mathbf b}(\lambda)\,
A_{\mathbf a'}B_{\mathbf b}
\\
&\quad-
\int d\mu_{\mathbf a',\mathbf b'}(\lambda)\,
A_{\mathbf a'}B_{\mathbf b'}.
\end{aligned}
\]

There is no single \(\lambda\)-space on which all four products are simultaneously evaluated. Consequently, the pointwise algebraic bound used in Bell’s proof cannot be applied.

Equivalently, the model does not admit a joint probability distribution
\[
P(A_{\mathbf a},A_{\mathbf a'},B_{\mathbf b},B_{\mathbf b'}).
\]

It supplies only the experimentally accessible contextual distributions
\[
P(A_{\mathbf a},B_{\mathbf b}),
\quad
P(A_{\mathbf a},B_{\mathbf b'}),
\quad
P(A_{\mathbf a'},B_{\mathbf b}),
\quad
P(A_{\mathbf a'},B_{\mathbf b'}).
\]

Thus the counterexample evades Bell’s theorem by rejecting the assumption that all counterfactual measurement outcomes must be embeddable in one global probability space.

---

## 14. Locality, Parameter Independence, and Outcome Independence

It is important to distinguish several independence conditions.

The model satisfies parameter independence. Conditional on the hidden variable \(\lambda\), Alice’s outcome does not depend on Bob’s setting:
\[
P(A\mid \mathbf a,\mathbf b,\lambda)
=
P(A\mid \mathbf a,\lambda).
\]

Likewise,
\[
P(B\mid \mathbf a,\mathbf b,\lambda)
=
P(B\mid \mathbf b,\lambda).
\]

Indeed, in the explicit construction,
\[
A(\mathbf a,\lambda)=\operatorname{sgn}(\mathbf a\cdot\lambda),
\]
which contains no dependence on \(\mathbf b\), and
\[
B(\mathbf b,\lambda)=-\operatorname{sgn}(\mathbf b\cdot\lambda),
\]
which contains no dependence on \(\mathbf a\).

The model is deterministic, so outcome independence holds trivially:
\[
P(A\mid B,\mathbf a,\mathbf b,\lambda)
=
P(A\mid \mathbf a,\mathbf b,\lambda).
\]

What fails is measurement independence:
\[
\rho(\lambda\mid \mathbf a,\mathbf b)\neq \rho(\lambda).
\]

Thus the counterexample is local in the operational and response-function sense but violates the statistical independence of hidden variables and measurement settings.

---

## 15. Operational No-Signalling

Despite the setting-dependent hidden-variable measure, the model is no-signalling.

From the joint probabilities
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\left(
1-\alpha\beta\,\mathbf a\cdot\mathbf b
\right),
\]
we find
\[
\sum_{\beta=\pm1}
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\frac14
\sum_{\beta=\pm1}
\left(
1-\alpha\beta\,\mathbf a\cdot\mathbf b
\right).
\]

Since
\[
\sum_{\beta=\pm1}\beta=0,
\]
this gives
\[
P(\alpha\mid \mathbf a,\mathbf b)=\frac12.
\]

Similarly,
\[
P(\beta\mid \mathbf a,\mathbf b)=\frac12.
\]

Therefore neither Alice nor Bob can infer the distant setting from local outcome statistics. The model is compatible with relativistic no-signalling at the observable level.

---

## 16. Tensorial Form of the Correlation

Using Euclidean tensor notation, the singlet correlation is
\[
E(\mathbf a,\mathbf b)
=
T_{ij}a^i b^j,
\]
with correlation tensor
\[
T_{ij}=-\delta_{ij}.
\]

Thus
\[
E(\mathbf a,\mathbf b)
=
-\delta_{ij}a^i b^j.
\]

In the counterexample, the same tensorial structure is reproduced:
\[
\int d\mu_{\mathbf a,\mathbf b}(\lambda)\,
A(\mathbf a,\lambda)B(\mathbf b,\lambda)
=
-\delta_{ij}a^i b^j.
\]

The model therefore reproduces the full rotational covariance of the singlet correlation at the level of observable statistics.

---

## 17. Covariant Spacetime Formulation

Let the two measurements occur at spacelike-separated events \(x_A\) and \(x_B\) in Minkowski spacetime with metric
\[
\eta_{\mu\nu}=\operatorname{diag}(-1,+1,+1,+1).
\]

Let \(u_A^\mu\) and \(u_B^\mu\) be the four-velocities of the two laboratories. In the local rest frame of Alice, the measurement direction is a spacelike vector \(a_A^\mu\) satisfying
\[
u_{A\mu}a_A^\mu=0.
\]

Similarly, Bob’s setting is a spacelike vector \(b_B^\mu\) satisfying
\[
u_{B\mu}b_B^\mu=0.
\]

If the two laboratories are compared in a common inertial frame, one may introduce the spatial projector
\[
h_{\mu\nu}
=
\eta_{\mu\nu}+u_\mu u_\nu.
\]

Then the invariant scalar entering the singlet correlation is
\[
\cos\theta
=
h_{\mu\nu}a_A^\mu b_B^\nu,
\]
assuming normalized spatial directions.

The observed correlation may be written covariantly as
\[
E(a_A,b_B)
=
-h_{\mu\nu}a_A^\mu b_B^\nu.
\]

The contextual hidden-variable measure depends only on the invariant angle \(\theta\). In a block-universe or common-cause interpretation, the dependence of \(\mu\) on \((\mathbf a,\mathbf b)\) does not require a superluminal signal propagating from one wing to the other. It may instead be understood as arising from correlations established in the common past or from global boundary conditions.

---

## 18. Causal Interpretation

The counterexample may be embedded in a causal model with a common past variable \(C\). Schematically,

\[
C\longrightarrow \mathbf a,
\qquad
C\longrightarrow \mathbf b,
\qquad
C\longrightarrow \lambda,
\]
with local outcome generation
\[
\mathbf a,\lambda\longrightarrow A,
\qquad
\mathbf b,\lambda\longrightarrow B.
\]

The observed conditional distribution is then
\[
P(\alpha,\beta\mid \mathbf a,\mathbf b)
=
\int d\lambda\,
P(\alpha\mid \mathbf a,\lambda)
P(\beta\mid \mathbf b,\lambda)
P(\lambda\mid \mathbf a,\mathbf b).
\]

The dependence of \(P(\lambda\mid \mathbf a,\mathbf b)\) on the settings arises because \(\lambda\), \(\mathbf a\), and \(\mathbf b\) are all correlated through \(C\). No superluminal influence from Alice’s setting to Bob’s outcome, or vice versa, is required.

This is the precise sense in which the model is local but measurement-dependent.

---

## 19. Quantifying the Required Measurement Dependence

The counterexample requires a nonzero failure of measurement independence. One can quantify this in a simple way.

Let \(\mu_{xy}\) denote the contextual measure associated with setting pair \((x,y)\), where
\[
x\in\{\mathbf a,\mathbf a'\},
\qquad
y\in\{\mathbf b,\mathbf b'\}.
\]

Let \(\nu\) be any candidate setting-independent measure on a common hidden-variable space. Define the total variation distance
\[
d_{xy}
=
\sup_{M}
\left|
\mu_{xy}(M)-\nu(M)
\right|,
\]
where the supremum is over measurable sets \(M\).

For any bounded observable \(F\) with \(|F|\le 1\),
\[
\left|
\int F\,d\mu_{xy}
-
\int F\,d\nu
\right|
\le
2d_{xy}.
\]

Let
\[
S_\nu
\]
be the CHSH value computed using the common measure \(\nu\). Bell’s theorem gives
\[
|S_\nu|\le 2.
\]

The observed CHSH value in the counterexample is
\[
S_{\text{obs}}=2\sqrt2.
\]

Therefore,
\[
|S_{\text{obs}}|
\le
2+2\sum_{xy}d_{xy}.
\]

Thus
\[
2\sqrt2
\le
2+2\sum_{xy}d_{xy},
\]
which implies
\[
\sum_{xy}d_{xy}
\ge
\sqrt2-1.
\]

Hence the departure from measurement independence cannot be made arbitrarily small if the model is to reproduce the maximal singlet violation.

---

## 20. Relation to Superdeterminism and Retrocausality

The counterexample belongs to the broad class of measurement-dependent models. Such models are sometimes called superdeterministic if the measurement settings and hidden variables are correlated through common causes in the past. They may also be given retrocausal interpretations, in which future settings help determine earlier hidden variables.

The present construction does not depend on a specific metaphysical interpretation. Mathematically, it requires only that the probability kernel be contextual:
\[
\lambda\sim \mu_{\mathbf a,\mathbf b}.
\]

Physically, one may interpret this as:

1. a common-cause correlation between the source and the setting generators;
2. a retrocausal constraint from future measurement contexts;
3. a global boundary condition on spacetime histories;
4. a denial of counterfactual independence between experimental choices and source variables.

All of these interpretations preserve the same observable structure.

---

## 21. Objections and Replies

### 21.1 “This is not a counterexample because Bell assumes measurement independence”

Correct. The model is not a counterexample to the conditional mathematical statement:

> If locality and measurement independence both hold, then Bell inequalities follow.

It is a counterexample to the stronger physical claim:

> No local hidden-variable theory can reproduce the quantum correlations.

The counterexample shows that the stronger claim is false unless measurement independence is explicitly included among the defining assumptions of “local hidden-variable theory.”

---

### 21.2 “The model is conspiratorial”

The model certainly requires correlations between hidden variables and measurement settings. Whether such correlations are natural depends on one’s preferred cosmology or theory of measurement. Bell tests do not prove that such correlations are absent; they prove that at least one of locality, realism, counterfactual definiteness, or measurement independence must fail.

The present construction shows that measurement dependence alone is sufficient to restore local realism at the observational level.

---

### 21.3 “The hidden variable distribution depends on future settings”

In a dynamical, forward-in-time picture this may appear nonlocal. In a block-universe or global-constraint picture it is not problematic. The model can be formulated covariantly as a distribution over complete histories satisfying local consistency conditions.

Alternatively, one may introduce a deeper common cause \(C\) in the overlap of the past light cones of the two measurement events. Then the apparent dependence of \(\lambda\) on \(\mathbf a,\mathbf b\) is merely the result of conditioning on settings that are themselves correlated with \(C\).

---

### 21.4 “The model is not local because \(\mu_{\mathbf a,\mathbf b}\) depends on both settings”

The dependence of the hidden-variable measure on both settings is not, by itself, a superluminal influence between the measurement events. The outcome functions are local:
\[
A=A(\mathbf a,\lambda),
\qquad
B=B(\mathbf b,\lambda).
\]

The model violates statistical independence but not parameter independence. It is local in the sense that no controllable signal propagates between the spacelike-separated regions, and no local response depends on the distant setting.

---

### 21.5 “This cannot be experimentally distinguished from quantum mechanics”

Correct. The model reproduces the singlet statistics exactly. Its purpose is not to predict new deviations from quantum mechanics in standard Bell experiments. Its purpose is to show that the logical inference from Bell-inequality violation to the impossibility of all local hidden-variable theories is invalid unless measurement independence is assumed.

---

## 22. Conceptual Significance

Bell’s theorem is best understood not as a simple proof that nature is nonlocal, but as a theorem about the structure of probability spaces compatible with observed correlations.

The theorem shows that the singlet correlations cannot be embedded in a single Kolmogorov probability space satisfying:

\[
\text{local response}
+
\text{setting-independent measure}.
\]

The counterexample shows that if one allows contextual probability measures,
\[
\mu_{\mathbf a,\mathbf b},
\]
then a local deterministic model exists.

Thus the essential issue is not locality alone but the globality of the hidden-variable probability space.

In this sense, Bell’s theorem is a theorem about the impossibility of a certain kind of global counterfactual completion. The counterexample supplies a local contextual model that has no such completion.

---

## 23. Conclusion

I have constructed an explicit local hidden-variable model reproducing the full singlet-state correlation
\[
E(\mathbf a,\mathbf b)=-\mathbf a\cdot\mathbf b.
\]

The model is deterministic at the level of local response functions, satisfies parameter independence, and obeys operational no-signalling. It violates the CHSH inequality up to the quantum maximum \(2\sqrt2\).

The model evades Bell’s theorem by rejecting measurement independence. The hidden-variable measure is contextual:
\[
\rho(\lambda\mid \mathbf a,\mathbf b)\neq \rho(\lambda).
\]

Equivalently, the model does not admit a single joint probability distribution over all counterfactual outcomes. Bell’s inequality therefore cannot be derived.

The result demonstrates that the common statement of Bell’s theorem as a universal no-go theorem for all local hidden-variable theories is too strong. The correct conclusion is more precise:

> Local hidden-variable theories satisfying measurement independence cannot reproduce the singlet correlations.  
> Local hidden-variable theories without measurement independence can.

The counterexample given here provides an explicit construction of the latter class.

---

## Appendix A: Arc-Length Structure of the Hidden Circle

Let
\[
\mathbf a=\mathbf e_1,
\qquad
\mathbf b=\cos\theta\,\mathbf e_1+\sin\theta\,\mathbf e_2.
\]

For \(\lambda(\phi)=\cos\phi\,\mathbf e_1+\sin\phi\,\mathbf e_2\), one has
\[
\mathbf a\cdot\lambda=\cos\phi,
\qquad
\mathbf b\cdot\lambda=\cos(\phi-\theta).
\]

The sign of \(\cos\phi\) changes at
\[
\phi=\frac{\pi}{2},\frac{3\pi}{2}.
\]

The sign of \(\cos(\phi-\theta)\) changes at
\[
\phi=\theta+\frac{\pi}{2},\theta+\frac{3\pi}{2}.
\]

For \(0<\theta<\pi\), the four zeros divide the circle into four alternating arcs. The total length of arcs where the signs agree is
\[
L_+=2(\pi-\theta),
\]
and the total length of arcs where the signs disagree is
\[
L_-=2\theta.
\]

This gives the normalization and correlation formulas used in the main text.

---

## Appendix B: Tensor Derivation of the Quantum Singlet Correlation

The singlet density matrix is
\[
\rho_{\psi^-}
=
\frac14
\left(
I\otimes I
-
\sigma_i\otimes\sigma_i
\right).
\]

The measurement observables are
\[
\hat A_{\mathbf a}
=
a^i\sigma_i,
\qquad
\hat B_{\mathbf b}
=
b^j\sigma_j.
\]

Then
\[
\begin{aligned}
E_{\psi^-}(\mathbf a,\mathbf b)
&=
\operatorname{Tr}
\left[
\rho_{\psi^-}
\left(
a^i\sigma_i\otimes b^j\sigma_j
\right)
\right]
\\
&=
\frac14
\operatorname{Tr}
\left[
\left(
I\otimes I-\sigma_k\otimes\sigma_k
\right)
\left(
a^i\sigma_i\otimes b^j\sigma_j
\right)
\right].
\end{aligned}
\]

The first term vanishes because
\[
\operatorname{Tr}(\sigma_i)=0.
\]

For the second term,
\[
\operatorname{Tr}(\sigma_k\sigma_i)=2\delta_{ki},
\]
so
\[
\begin{aligned}
E_{\psi^-}(\mathbf a,\mathbf b)
&=
-\frac14
a^i b^j
\operatorname{Tr}(\sigma_k\sigma_i)
\operatorname{Tr}(\sigma_k\sigma_j)
\\
&=
-\frac14
a^i b^j
(2\delta_{ki})(2\delta_{kj})
\\
&=
-a^i b^j\delta_{ij}.
\end{aligned}
\]

Therefore
\[
E_{\psi^-}(\mathbf a,\mathbf b)
=
-\mathbf a\cdot\mathbf b.
\]

---

## Appendix C: General Contextual Local Model

Let
\[
P(\alpha,\beta\mid x,y)
\]
be any nonsignalling conditional distribution with inputs \(x,y\) and binary outputs \(\alpha,\beta\).

Define
\[
\Lambda=\{+1,-1\}^2,
\]
and
\[
\rho_{x,y}(\alpha,\beta)=P(\alpha,\beta\mid x,y).
\]

Let
\[
A(x,\alpha,\beta)=\alpha,
\qquad
B(y,\alpha,\beta)=\beta.
\]

Then
\[
P(\alpha,\beta\mid x,y)
=
\sum_{\lambda\in\Lambda}
\rho_{x,y}(\lambda)
\delta_{A(x,\lambda),\alpha}
\delta_{B(y,\lambda),\beta}.
\]

This representation is local because \(A\) does not depend on \(y\) and \(B\) does not depend on \(x\). It is measurement-dependent because \(\rho_{x,y}\) depends on both inputs.

Thus, once measurement independence is abandoned, Bell-type no-go arguments lose their universal force.

---

## References

1. J. S. Bell, “On the Einstein Podolsky Rosen paradox,” *Physics* **1**, 195–200 (1964).  
2. J. F. Clauser, M. A. Horne, A. Shimony, and R. A. Holt, “Proposed experiment to test local hidden-variable theories,” *Physical Review Letters* **23**, 880–884 (1969).  
3. A. Fine, “Hidden variables, joint probability, and Bell inequalities,” *Physical Review Letters* **48**, 291–295 (1982).  
4. M. J. W. Hall, “Local deterministic model of singlet state correlations based on relaxing measurement independence,” *Physical Review Letters* **105**, 250404 (2010).  
5. N. Brunner, D. Cavalcanti, S. Pironio, V. Scarani, and S. Wehner, “Bell nonlocality,” *Reviews of Modern Physics* **86**, 419–478 (2014).

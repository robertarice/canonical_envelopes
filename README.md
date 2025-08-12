# Canonical Envelopes

## Idea

**Canonical envelopes** provide a mathematical framework for understanding completion phenomena in category theory and related mathematical disciplines through systematic factorization of pairings via virtual weighted (co)limiting structures.

The framework unifies and extends several foundational insights:

1. **Riehl's weighted limit characterization** through natural transformations $\theta : Q \Rightarrow C(D, E)$
2. **Garner's cylinder factorization systems** for categorical completion
3. **Gabriel-Ulmer virtual morphism methodology** extended to arbitrary weights

Canonical envelope theory demonstrates that numerous completion constructions—including canonical extensions, topological compactifications, categorical completions, and constructions in algebraic geometry—can be understood as instances of universal factorization through bilateral envelope structure.

The theory organizes around two key insights:
1. **Gem theory**: A systematic classification revealing how mathematical structures arise from bilateral completion properties determined by representability
2. **Pseudomonad organization**: Deep categorical foundations showing completion phenomena share universal organizational principles

## Foundational Motivation

### From Weighted Limits to Pairings

The foundation emerges from **Riehl's characterization of weighted limits** building on Kelly's enriched category theory. For a profunctor $Q : I^{op} \times J \to V$ and diagrams $D : I \to C$, $E : J \to C$, weighted limits satisfy:

$[I, C](\mathrm{colim}^Q D, E) \cong [I^{op} \times J, V](Q, C(D, E)) \cong [J, C](D, \mathrm{lim}^Q E)$

The **key insight** is that the central term $[I^{op} \times J, V](Q, C(D, E))$ represents a **pairing between the profunctor $Q$ and the hom-structure $C(D, E)$**. This pairing exists even when the classical weighted (co)limits on the exterior fail to exist.

More precisely, this gives rise to an **adjunction**:
$\mathrm{colim}^Q : [I, C] \rightleftarrows [J, C] : \mathrm{lim}^Q$
with natural isomorphism:
$[J, C](D, \mathrm{lim}^Q E) \cong [I, C](\mathrm{colim}^Q D, E)$

When this adjunction exists, the natural transformations $\theta : Q \Rightarrow C(D, E)$ arise from the **unit** and **counit** of the adjunction via transposition. When the adjunction fails to exist, these natural transformations $\theta$ still make sense and serve as **proxies for limiting behavior**.

This observation suggests that **pairings** $\theta : Q \Rightarrow C(D, E)$ can serve as fundamental objects of study, enabling completion methodology in contexts where classical limits are unavailable.

### Garner's Cylinder Factorization Systems

Parallel developments in **Garner's cylinder factorization systems** provide complementary organizational principles for categorical completion through systematic factorization methodology.

#### Cylinders and Factorization

A **Garner cylinder** from $D : I \to C$ to $E : J \to C$ is a natural transformation $\theta : 1 \Rightarrow C(D, E)$, i.e., a family of arrows $\theta_{i,j} : D(i) \to E(j)$.

Garner's framework systematically factorizes cylinders through **left and right cylinder classes**:
- **Left cylinder class** $\mathcal{L}$: Morphisms with left lifting properties
- **Right cylinder class** $\mathcal{R}$: Morphisms with right lifting properties  
- **Orthogonality**: $f \perp g$ when every commutative square has a unique diagonal filler

Every cylinder $\theta$ admits a canonical factorization:
$\theta = \rho \circ \gamma \circ \lambda$
where $\lambda \in \mathcal{L}$, $\rho \in \mathcal{R}$, and $\gamma$ is the **canonical interpolant**.

#### Key Examples

1. **Isbell envelopes**: Universal adjoint completion through cylinder factorization
2. **Dense-codense factorizations**: Systematic organization of representable-based completions  
3. **Presheaf completions**: Universal factorization methodology for Yoneda embedding

#### Limitation and Extension

Garner's approach applies to cylinders with **trivial weights** $Q = 1$. This raises the fundamental question: 

> *Can systematic factorization extend to arbitrary weighted contexts, potentially unifying weighted limit theory with factorization methodology?*

### The Canonical Envelope Solution

Canonical envelope theory demonstrates that both Riehl's and Garner's insights unify through **systematic factorization of arbitrary pairings** $\theta : Q \Rightarrow C(D, E)$ through bilateral structure.

The framework provides:
- **Generalization of Riehl**: When classical limits exist, canonical envelopes recover them
- **Generalization of Garner**: When $Q = 1$, canonical envelopes reduce to cylinder factorizations  
- **Virtual completion**: When classical constructions fail, canonical envelopes provide systematic approximation

This systematic approach reveals that:
1. **Weighted limits** are special cases of canonical envelope completion
2. **Cylinder factorizations** are unweighted specializations  
3. **Virtual methods** provide coherent extension when classical methods fail
4. **Bilateral structure** captures the fundamental balance underlying mathematical completion

## Definition

### Pairings

A **pairing** is a 6-tuple $(I, J, D, E, Q, \theta)$ where:

* $I, J$ are small $V$-categories (indexing categories)
* $D : I \to C$, $E : J \to C$ are $V$-functors (source and target functors)  
* $Q : I^{op} \times J \to V$ is a $V$-profunctor (bilateral weight)
* $\theta : Q \Rightarrow C(D, E)$ is a $V$-natural transformation (the pairing morphism)

### Canonical Envelopes

A **canonical envelope** of a pairing $\theta : Q \Rightarrow C(D, E)$ is a factorization $(\lambda, \gamma, \rho)$ where:

* $Y : J \to C$ and $X : I \to C$ are $V$-functors (completion functors)
* $\lambda : Q \Rightarrow C(D, Y)$ (left envelope)
* $\gamma : Q \Rightarrow C(Y, X)$ (canonical interpolant)  
* $\rho : Q \Rightarrow C(X, E)$ (right envelope)
* $\theta = \rho \star \gamma \star \lambda$ (factorization property)
* $\star$ is pointwise composition
* The factorization is initial among all such factorizations

More precisely, a canonical envelope is an initial object in the category $\mathsf{Fact}(\theta)$ of factorizations of $\theta$.

## Bilateral Conditions

The existence and uniqueness of canonical envelopes is governed by bilateral conditions:

### Bilateral Denseness

A pairing $\theta : Q \Rightarrow C(D, E)$ is **bilaterally dense** if there exists a factorization $\theta = \rho \star \gamma \star \lambda$ where the left envelope $\lambda$, canonical interpolant $\gamma$, and right envelope $\rho$ exist.

### Bilateral Compactness

A bilaterally dense pairing is **bilaterally compact** if the factorization is essentially unique: any two factorizations are related by a unique isomorphism of factorizations.

## Fundamental Theorem

**Theorem**: A pairing $\theta : Q \Rightarrow C(D, E)$ admits a canonical envelope if and only if it is bilaterally dense and bilaterally compact. When a canonical envelope exists, it is unique up to unique isomorphism.

## Summary of Key Framework Components

### The Pseudomonad Structure

The canonical envelope construction organizes through a **pseudomonad** $\mathbb{E}^{\rtimes \ltimes}$ that captures the universal principles of mathematical completion:

- **Domain**: Acts on the 2-category $\mathsf{Pair}$ of pairings $(Q, D, E, \theta)$
- **Action**: Transforms pairings into their bilateral envelope completions
- **Universal Property**: EM-algebras are precisely the bilaterally dense and compact pairings
- **Idempotency**: KZ pseudomonad structure ensures systematic virtual extension when classical completions fail
- **Unification**: Generalizes Garner's Isbell monad (specialization to trivial weights $Q = 1$)

This pseudomonad reveals that diverse completion phenomena—from Stone-Čech compactification to Boolean algebra extensions—share fundamental categorical organization principles.

### Gem Theory Classification

**Gem theory** provides systematic classification of mathematical structures through bilateral completion properties:

- **Gems**: Left-biased completion (Yoneda embedding on source)
- **CoGems**: Right-biased completion (Yoneda embedding on target)  
- **DiGems**: Bilateral completion (Yoneda embeddings on both sides)

The **classification principle**: For enrichment base $V$ and index category $X$:
- $V$ determines the mathematical context (Set, Cat, Ab, etc.)
- $X$ determines foundational granularity (atomic, Boolean, finite, general)
- Gem type determines bilateral bias (left/right/balanced)

This yields a **systematic map** from $(X,V)$ pairs to mathematical structures, revealing patterns like:
- $(2, \mathrm{Set}) \mapsto$ Complete lattices (DiGem), Semilattices (Gem/CoGem)
- $(\mathrm{FinCat}, \mathrm{Cat}) \mapsto$ Grothendieck topoi (Gem), Bitopoi (DiGem)
- $(1, \mathrm{Ab}) \mapsto$ Rings (Gem), Commutative rings (DiGem)

## Virtual Weighted Limits

Canonical envelopes systematically extend classical weighted limit theory:

**Virtual weighted limits** are canonical envelopes of pairings that encode classical weighted (co)limit data. When classical weighted limits exist, virtual weighted limits coincide with them. When classical limits fail, virtual weighted limits provide systematic approximation through bilateral completion.

This extends the Gabriel-Ulmer methodology from filtered/cofiltered diagrams to arbitrary weights.

## Examples

### Stone-Čech Compactification

The Stone-Čech compactification $\beta X$ of a completely regular space $X$ arises as the canonical envelope with:
* $I = J = X$
* $D(x) = E(x) =$ principal (ultra)filter on $x$  
* $Q(F,U) = \{*\}$ if $F \subseteq U$, $\emptyset$ otherwise
* $\theta =$ convergence relation in $\beta X$

### Boolean Algebra Canonical Extensions

The canonical extension $L^\delta$ of a distributive lattice $L$ arises as the canonical envelope with:
* $I = \mathsf{Filt}(L)$, $J = \mathsf{Idl}(L)$
* $D$, $E$ are embeddings into the canonical extension
* $Q(F,I) = \{*\}$ if $F \cap I = \emptyset$, $\emptyset$ otherwise
* $\theta = \mathrm{id}_Q$ (internal completion)

### Isbell Envelopes

For a small category $C$, the Isbell envelope $E(C)$ is the canonical envelope with:
* $I = J = C$
* $D = E = \mathrm{id}_C$
* $Q = C(-,-)$ (hom-profunctor)
* $\theta = \mathrm{id}_{C(-,-)}$

## Gem Theory

**Gems** are special canonical envelopes whose bilateral structure is determined by representability and the Yoneda embedding, providing a systematic classification of mathematical structures according to their bilateral completion properties.

### Definition of Gems

Let $V$ be a complete and cocomplete symmetric monoidal closed category, and let $X$ be a small $V$-category. Write $C = [X^{op}, V]$ for the $V$-category of $V$-enriched presheaves.

A **gem** is a canonical envelope $(Q, D, E, \theta)$ where:
1. $D : X \to C$ is the Yoneda embedding $Y$, so $D(x) = Y(x) := C(-, x)$
2. $E : I \to C$ is constant at a presheaf $P \in C$ (with $I$ the unit category)  
3. $Q : X^{op} \to V$ is a representable weight with $Q(x) \cong P(x)$ naturally in $x$
4. $\theta : Q \Rightarrow C(D, E)$ is the identity under the isomorphisms $Q(x) \cong P(x) \cong C(Y(x), P)$

**CoGems** and **DiGems** are defined dually:
- **CoGem**: $D$ constant, $E$ the Yoneda embedding  
- **DiGem**: Both $D$ and $E$ are Yoneda embeddings (fully bilateral)

### Six Equivalent Facets of Gems

**Theorem**: For $P \in [X^{op}, V]$, the following are equivalent:

1. **Canonical extension facet**: $\eta_P : \int^{x \in X} P(x) \otimes Y(x) \cong P$ is an isomorphism
2. **Profunctor facet**: $\phi_x : C(Y(x), P) \cong P(x)$ is an isomorphism naturally in $x$  
3. **Codensity monad facet**: $P$ is a fixed point of the codensity monad of $Y$
4. **Kan extension facet**: The unit $P \to \mathrm{Ran}_Y(P \circ Y)$ is an isomorphism
5. **Canonical envelope facet**: $P$ arises as the interpolant in a canonical envelope with specified data
6. **Distributivity facet**: For finite diagrams $K : J \to [X^{op}, V]$ of representables, the canonical morphism $\mathrm{Hom}(\mathrm{colim}_j K(j), P) \to \lim_j \mathrm{Hom}(K(j), P)$ is an isomorphism

### Systematic Classification

The gem classification reveals stable patterns across mathematical domains:

| Base $V$ | Index $X$ | Gem$(X,V)$ | CoGem$(X,V)$ | DiGem$(X,V)$ |
|----------|-----------|------------|--------------|--------------|
| Set | 1 | Monoids | Comonoids | Commutative Monoids |
| Set | 2 | Complete Semilattices | Complete Cosemilattices | Complete Lattices |
| Set | DiscSet | Topological Spaces | Cotopological Spaces | Stably Compact Spaces |
| Set | FinSet | Bounded Ionads | Bounded Coionads | Finite Approximations |
| Set | FinPoset | Continuous Posets | Cocontinuous Posets | Bicontinuous Lattices |
| Set | Span(Set) | Small Categories | Small Cocategories | Dagger Categories |
| Cat | 1 | Monoidal Categories | Comonoidal Categories | Symmetric Monoidal Categories |
| Cat | FinCat | Grothendieck Topoi | Grothendieck Cotopoi | Bitopoi |
| Ab | 1 | Rings | Corings | Commutative Rings |

### Classification Principle

For each row in the classification table:
1. **$V$ fixes the enrichment scale**: discrete (Set), categorical (Cat), linear (Ab), quantum (FdHilb), relational (Rel)
2. **$X$ fixes foundational granularity**: atomic (1), Boolean (2), finite/combinatorial (FinSet, FinCat), general (Set)  
3. **Gem type fixes bilateral pattern**: left-biased (Gem), right-biased (CoGem), balanced (DiGem)

The resulting structures are precisely those obtained by instantiating Yoneda-based completion in the $([X^{op}, V], Y)$ context, with each entry verified through the six-facet equivalence.

### Examples

**Complete Lattices as DiGems**: There is an equivalence $\mathrm{DiGem}(2, \mathrm{Set}) \simeq \mathrm{ComplLat}$, where 2-element Boolean algebra structure determines bilateral completion through join/meet-irreducible representation.

**Grothendieck Topoi as Gems**: There is an equivalence $\mathrm{GrTop} \simeq \mathrm{Gem}(\mathrm{Cat}, \mathrm{FinCat})$, where the Yoneda embedding provides dense generation of topoi through finite-limit-preserving functors.

## Categorical Foundations

### The Canonical Envelope Pseudomonad

The canonical envelope construction admits systematic organization through a pseudomonad, revealing deep categorical foundations for completion theory.

#### The Pairing 2-Category

Let $\mathsf{Pair}$ be the 2-category with:
- **Objects**: Quadruples $(Q, D, E, \theta)$ where $D : I \to C$, $E : J \to C$ are $V$-functors, $Q : I \times J \to V$ is a weight, and $\theta : Q \Rightarrow C(D, E)$ is the pairing
- **1-cells**: Triples $(u, v, \alpha)$ where $u : I' \to I$, $v : J' \to J$ are functors and $\alpha : Q' \to Q \circ (u \times v)$ makes $\theta$ compatible under whiskering
- **2-cells**: Natural transformations between the functors making $\alpha$ compatible

#### Pseudomonad Structure

**Theorem**: The assignment $(Q, D, E, \theta) \mapsto \mathbb{E}^{\rtimes \ltimes}(Q, D, E, \theta)$ extends to a pseudomonad $\mathbb{E}^{\rtimes \ltimes}$ on $\mathsf{Pair}$ with:

1. **Unit**: For each pairing, the identity factorization provides $\eta : (Q, D, E, \theta) \to \mathbb{E}^{\rtimes \ltimes}(Q, D, E, \theta)$
2. **Multiplication**: Applying $\mathbb{E}^{\rtimes \ltimes}$ twice gives an envelope of an envelope; by initiality this collapses to the same envelope up to equivalence, giving $\mu : \mathbb{E}^{\rtimes \ltimes 2} \Rightarrow \mathbb{E}^{\rtimes \ltimes}$  
3. **Coherence**: Associativity and unit laws hold up to invertible modifications, making $\mathbb{E}^{\rtimes \ltimes}$ a KZ pseudomonad (idempotent up to equivalence)

The **envelope construction** creates, for a pairing $(Q, D, E, \theta)$ with canonical envelope $(X, Y; \lambda, \gamma, \rho)$:
- $p(i) = [J, V](Q(i, -), C(D(i), Y(-)))$
- $q(j) = [I^{op}, V](Q(-, j), C(X(-), E(j)))$  
- $\chi : p^{op} \otimes q \to Q$ satisfying closure conditions ensuring bilateral denseness

#### Eilenberg-Moore Category

**Theorem**: The Eilenberg-Moore category $\mathsf{EnvAlg}$ for the canonical envelope pseudomonad $\mathbb{E}^{\rtimes \ltimes}$ is equivalent to:
$\{\text{$V$-pairings that are bilaterally dense and compact, closed under whiskering}\}$

An **EM-algebra** consists of:
1. A pairing $(Q, D, E, \theta)$ in $\mathsf{Pair}$
2. A choice of $(p, q, \chi)$ computed from completion functors $(X, Y)$ in $C$
3. Stability under whiskering (closure under reindexing)

#### Relationship to Garner's Isbell Monad

**Theorem**: Garner's Isbell monad $\mathcal{I}$ on $\mathrm{Cat}$ is the natural specialization of $\mathbb{E}^{\rtimes \ltimes}$ to:
- Trivial weight $Q = 1$ (unweighted case)
- Identity shapes $I = J = C$ (categories as their own indexing)  
- Object apexes rather than general diagrams

Under these restrictions: $\mathbb{E}^{\rtimes \ltimes}|_{Q=1,I=J=C} \cong \mathcal{I}$

This demonstrates that canonical envelopes provide systematic weighted generalization of Garner's cylinder factorization systems, unifying weighted limit theory with factorization methodology.

### Relationship to Existing Theory

Canonical envelope theory unifies several classical frameworks:

* **Garner's cylinder factorization systems**: Special case with trivial weight $Q = 1$
* **Schoots's categorical extensions**: Correspondence via filtered/cofiltered diagram structure  
* **Pratt's communes**: Equivalence for identity pairings $\theta = \mathrm{id}_P$
* **Riehl's weighted limits**: Direct generalization to virtual contexts

## Properties

### Pullback Characterization

**Theorem**: The canonical interpolant $\gamma$ in a canonical envelope factorization arises as a pullback in the category of natural transformations, demonstrating that canonical interpolants are categorically determined rather than arbitrary constructions.

### Classical Recovery

When classical completion constructions exist, canonical envelopes coincide with classical results. When classical constructions fail, canonical envelopes provide systematic virtual approximation with optimal properties.

## Applications

Canonical envelope theory has applications across mathematics:

* **Topology**: Systematic understanding of compactification procedures
* **Algebra**: Unified theory of canonical extensions and completions  
* **Category Theory**: Virtual extensions of weighted limit theory
* **Logic**: Systematic treatment of logical completion phenomena

## References

* Robert A. Rice, *Canonical Envelopes: A Mathematical Framework for Virtual Weighted Limits and Completion Theory*, 2025

* Emily Riehl, *Weighted limits and colimits*, 2008

* Richard Garner, *The Isbell monad*, Advances in Mathematics 333:1-31, 2018

* Vaughan Pratt, *Communes*, Category Theory 2010 Abstracts, 2010

## Related Concepts

* [[weighted limit]]
* [[virtual double category]]  
* [[Isbell envelope]]
* [[canonical extension]]
* [[Stone-Čech compactification]]
* [[profunctor]]
* [[enriched category theory]]
* [[Gabriel-Ulmer duality]]

[[!redirects canonical envelope]]
[[!redirects canonical envelopes]]
[[!redirects bilateral envelope]]
[[!redirects virtual weighted limit]]
[[!redirects virtual weighted limits]]
[[!redirects gem theory]]

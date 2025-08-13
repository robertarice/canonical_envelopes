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

### Cylinder Factorization Characterization

One of the most elegant structural results reveals that canonical interpolants arise through **cylinder factorization systems**, providing deep insight into the categorical organization of completion theory.

#### The Factorization Structure

**Theorem**: Let $\theta : Q \Rightarrow C(D, E)$ be a bilaterally dense and compact pairing with canonical envelope $(\lambda, \gamma, \rho)$. Then the canonical interpolant $\gamma$ is characterized through cylinder factorization structure: for each $q \in Q(i, j)$, the morphism $\theta(i, j, q) : D(i) \to E(j)$ factors as:

$$D(i) \xrightarrow{\lambda(i,j,q)} Y(j) \xrightarrow{\gamma(i,j,q)} X(i) \xrightarrow{\rho(i,j,q)} E(j)$$

where $\theta(i,j,q) = \rho(i,j,q) \circ \gamma(i,j,q) \circ \lambda(i,j,q)$.

#### Universal Property
**Theorem**: For any other factorization of $\theta(i,j,q)$ through intermediate objects, there exists a unique way to factor this through the canonical envelope. Specifically, there exist morphisms $\alpha : Y' \to Y(j)$ and $\beta : X' \to X(i)$ such that the alternative factorization equals $\beta \circ \gamma(i,j,q) \circ \alpha$.

#### Connection to Garner's Framework
This cylinder factorization structure corresponds precisely to Garner's cylinder factorization systems:

- **Left cylinder class**: morphisms of the form $\lambda(i,j,q)$ (source completion morphisms)
- **Right cylinder class**: morphisms of the form $\rho(i,j,q)$ (target completion morphisms)  
- **Interpolant class**: morphisms of the form $\gamma(i,j,q)$ (canonical mediating morphisms)

The **orthogonality conditions** in Garner's framework correspond exactly to the **bilateral denseness conditions** in canonical envelope theory. This reveals that canonical envelopes provide systematic weighted generalization of Garner's unweighted cylinder systems while preserving the essential geometric insight of factorization through orthogonal classes.

### The Pseudomonad Structure

The canonical envelope construction organizes through a **pseudomonad** $\mathbb{ENV}$ that captures the universal principles of mathematical completion:

#### The Pairing 2-Category

Let $\mathsf{Pair}$ be the 2-category with:
- **Objects**: Quadruples $(Q, D, E, \theta)$ where $D : I \to C$, $E : J \to C$ are $V$-functors, $Q : I \times J \to V$ is a weight, and $\theta : Q \Rightarrow C(D, E)$ is the pairing
- **1-cells**: Triples $(u, v, \alpha)$ where $u : I' \to I$, $v : J' \to J$ are functors and $\alpha : Q' \to Q \circ (u \times v)$ makes $\theta$ compatible under whiskering
- **2-cells**: Natural transformations between the functors making $\alpha$ compatible

#### Pseudomonad Structure

**Theorem**: The assignment $(Q, D, E, \theta) \mapsto \mathbb{ENV}(Q, D, E, \theta)$ extends to a pseudomonad $\mathbb{ENV}$ on $\mathsf{Pair}$ with:

1. **Unit**: For each pairing, the identity factorization provides $\eta : (Q, D, E, \theta) \to \mathbb{ENV}(Q, D, E, \theta)$
2. **Multiplication**: Applying $\mathbb{ENV}$ twice gives an envelope of an envelope; by initiality this collapses to the same envelope up to equivalence, giving $\mu : \mathbb{ENV}^2 \Rightarrow \mathbb{ENV}$  
3. **Coherence**: Associativity and unit laws hold up to invertible modifications, making $\mathbb{ENV}$ a KZ pseudomonad (idempotent up to equivalence)

#### Eilenberg-Moore Category

**Theorem**: The Eilenberg-Moore category $\mathsf{EnvAlg}$ for the canonical envelope pseudomonad $\mathbb{ENV}$ is equivalent to:
$$\{\text{$V$-pairings that are bilaterally dense and compact, closed under whiskering}\}$$

#### Relationship to Garner's Isbell Monad

**Theorem**: Garner's Isbell monad $\mathcal{I}$ on $\mathrm{Cat}$ is the natural specialization of $\mathbb{ENV}$ to:
- Trivial weight $Q = 1$ (unweighted case)
- Identity shapes $I = J = C$ (categories as their own indexing)  
- Object apexes rather than general diagrams

Under these restrictions: $\mathbb{ENV}|_{Q=1,I=J=C} \cong \mathcal{I}$

This demonstrates that canonical envelopes provide systematic weighted generalization of Garner's cylinder factorization systems, unifying weighted limit theory with factorization methodology.

### Gem Theory Classification

**Gem theory** provides systematic classification of mathematical structures through bilateral completion properties:

- **Gems**: Left-biased completion (Yoneda embedding on source)
- **CoGems**: Right-biased completion (Yoneda embedding on target)  
- **DiGems**: Bilateral completion (Yoneda embeddings on both sides)

#### Six Equivalent Facets of Gems

**Theorem**: For $P \in [X^{op}, V]$, the following are equivalent:

1. **Canonical extension facet**: $\eta_P : \int^{x \in X} P(x) \otimes Y(x) \cong P$ is an isomorphism
2. **Profunctor facet**: $\phi_x : C(Y(x), P) \cong P(x)$ is an isomorphism naturally in $x$  
3. **Codensity monad facet**: $P$ is a fixed point of the codensity monad of $Y$
4. **Kan extension facet**: The unit $P \to \mathrm{Ran}_Y(P \circ Y)$ is an isomorphism
5. **Canonical envelope facet**: $P$ arises as the interpolant in a canonical envelope with specified data
6. **Distributivity facet**: For finite diagrams $K : J \to [X^{op}, V]$ of representables, the canonical morphism $\mathrm{Hom}(\mathrm{colim}_j K(j), P) \to \lim_j \mathrm{Hom}(K(j), P)$ is an isomorphism

These equivalences reveal that gems capture multiple fundamental categorical completion phenomena simultaneously, providing deep insight into how mathematical structures arise from bilateral completion properties.

#### Systematic Correspondence Tables

Different pairs $(X, V)$ yield different kinds of structures via gem/cogem/digem completion:

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

#### Classification Principle

For each row in the classification table:
1. **$V$ fixes the enrichment scale**: discrete (Set), categorical (Cat), linear (Ab), quantum (FdHilb), relational (Rel)
2. **$X$ fixes foundational granularity**: atomic (1), Boolean (2), finite/combinatorial (FinSet, FinCat), general (Set)  
3. **Gem type fixes bilateral pattern**: left-biased (Gem), right-biased (CoGem), balanced (DiGem)

The resulting structures are precisely those obtained by instantiating Yoneda-based completion in the $([X^{op}, V], Y)$ context, with each entry verified through the six-facet equivalence.

## Virtual Weighted Limits

Canonical envelopes systematically extend classical weighted limit theory through **virtual methodology**:

### Definition
**Virtual weighted limits** are canonical envelopes of pairings that encode classical weighted (co)limit data. When classical weighted limits exist, virtual weighted limits coincide with them. When classical limits fail, virtual weighted limits provide systematic approximation through bilateral completion.

### The Correspondence Principle
**Theorem**: When the relevant classical weighted (co)limits exist in $C$, virtual weighted limits coincide with classical weighted limits. When classical limits fail to exist, virtual weighted limits provide systematic approximation through canonical envelope completion.

### Virtual Extension Methodology

When classical constructions fail, the virtual extension process works as follows:

1. **Bilateral Analysis**: Examine why classical bilateral denseness fails - typically due to insufficient representable structure or failed compactness conditions

2. **Optimal Approximation**: The canonical envelope construction provides the "best possible" completion respecting existing structure through the universal factorization property

3. **Systematic Composition**: Virtual weighted limits compose coherently through the pseudomonad structure, ensuring that virtual extensions preserve essential mathematical relationships

4. **Gabriel-Ulmer Extension**: The framework extends Gabriel-Ulmer virtual morphism methodology from filtered/cofiltered contexts to arbitrary weights

### Key Features
- **Coherent virtual morphism composition** extending Gabriel-Ulmer methodology  
- **Optimal approximation properties** when classical completions fail
- **Systematic preservation** of essential categorical structure
- **Universal factorization** through bilateral envelope organization

This extends the Gabriel-Ulmer methodology from filtered/cofiltered diagrams to arbitrary weights, providing principled completion methodology even in incomplete categorical frameworks.

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

## Applications

Canonical envelope theory has applications across mathematics:

### Topology
* **Compactification theory**: Systematic understanding of Stone-Čech, Alexandroff, and Wallman compactifications
* **Sobrification**: Topological completion via irreducible closed set structure  
* **Stably compact spaces**: DiGem completion of discrete topological contexts

### Algebra  
* **Canonical extensions**: Unified theory for Boolean algebras and distributive lattices
* **MacNeille completions**: DiGem structure for arbitrary posets via polarity
* **Ring completions**: Profinite and other categorical completions via bilateral structure

### Category Theory
* **Virtual limit theory**: Systematic extension when classical weighted (co)limits fail
* **Accessibility theory**: Preservation of presentability through bilateral completion
* **Higher category theory**: Extensions to (∞,1)-categorical and homotopical settings

### Logic and Computer Science  
* **Type theory**: Completion of type contexts via dependent bilateral structure
* **Domain theory**: Continuous and algebraic domain completion via canonical envelopes
* **Programming semantics**: Denotational semantics through virtual weighted limit methodology

## Properties

### Classical Recovery

When classical completion constructions exist, canonical envelopes coincide with classical results. When classical constructions fail, canonical envelopes provide systematic virtual approximation with optimal properties.

## Related Concepts

### Core Category Theory
* [[weighted limit]] - Classical weighted (co)limits that canonical envelopes generalize
* [[profunctor]] - Bilateral weights Q : I^op × J → V in the framework
* [[enriched category theory]] - Foundational setting following Kelly's development
* [[Kan extension]] - Recovered as special cases via gem theory facet equivalences

### Completion Theory  
* [[Isbell envelope]] - Canonical envelope with hom-profunctor and identity diagrams
* [[canonical extension]] - Boolean/lattice completions via filter-ideal pairings  
* [[Stone-Čech compactification]] - Topological completion via filter-ultrafilter structure
* [[Gabriel-Ulmer duality]] - Extended to arbitrary weights via virtual methodology

### Advanced Structures
* [[virtual double category]] - Higher categorical extensions of the framework
* [[pseudomonad]] - Organizational structure for canonical envelope completion
* [[factorization system]] - Cylinder characterization of canonical interpolants
* [[accessible category]] - Preservation properties under canonical envelope completion

## References

* Robert A. Rice, *Canonical Envelopes: A Mathematical Framework for Virtual Weighted Limits and Completion Theory*, 2025

* Emily Riehl, *Weighted limits and colimits*, 2008

* Richard Garner, *The Isbell monad*, Advances in Mathematics 333:1-31, 2018

* Vaughan Pratt, *Communes*, Category Theory 2010 Abstracts, 2010

[[!redirects canonical envelope]]
[[!redirects canonical envelopes]]
[[!redirects bilateral envelope]]
[[!redirects virtual weighted limit]]
[[!redirects virtual weighted limits]]
[[!redirects gem theory]]

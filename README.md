# Bilateral Weighted Completion Theory

## Overview

**Bilateral weighted completion theory** provides a categorical framework for studying completion phenomena through systematic factorization of bilateral pairings. The theory unifies several important completion constructions including Stone-Čech compactification, canonical extensions of distributive lattices, profinite completions, and Kan extensions within a common bilateral structure.

The framework builds on foundational work by:
- **Emily Riehl's weighted limit theory** - extending classical weighted limits to bilateral contexts
- **Richard Garner's cylinder factorization systems** - generalizing from trivial to arbitrary bilateral weights  
- **Gabriel-Ulmer virtual morphism methodology** - extending from filtered/cofiltered to general bilateral weights

## Core Construction

### Bilateral Pairings

A **bilateral pairing** consists of a 6-tuple $(I, J, D, E, Q, \theta)$ where:
- $I, J$ are small $V$-categories (bilateral indexing categories)
- $D : I \to C$, $E : J \to C$ are $V$-functors (source and target diagrams)  
- $Q : I^{\mathrm{op}} \otimes J \to V$ is a $V$-profunctor (bilateral weight)
- $\theta : Q \Rightarrow C(D, E)$ is a $V$-natural transformation (bilateral pairing morphism)

### Weighted Completion

A **weighted completion** of a bilateral pairing $\theta : Q \Rightarrow C(D, E)$ is a pair $(\hat{C}, \varepsilon_C)$ consisting of:
- A $V$-category $\hat{C}$ 
- A fully faithful $V$-functor $\varepsilon_C : C \hookrightarrow \hat{C}$ (completion embedding)

such that the lifted pairing $\varepsilon_C^* \theta : Q \Rightarrow \hat{C}(\varepsilon_C D, \varepsilon_C E)$ admits a **bilateral factorization**:
$$\varepsilon_C^* \theta = \rho \star \gamma \star \lambda$$
where:
- $\lambda : Q \Rightarrow \hat{C}(\varepsilon_C D, Y)$ (left envelope)
- $\gamma : Q \Rightarrow \hat{C}(Y, Z)$ (bilateral interpolant)  
- $\rho : Q \Rightarrow \hat{C}(Z, \varepsilon_C E)$ (right envelope)

for some $V$-functors $Y : J \to \hat{C}$ and $Z : I \to \hat{C}$.

## Fundamental Results

### Universal Existence Theorem
**Theorem**: Every bilateral pairing admits a weighted completion. The completion can be constructed systematically through $V$-presheaf extension.

### Completeness Properties
**Theorem**: 
1. Weighted completions always yield complete objects
2. Completing complete objects is trivial (idempotency)
3. A bilateral pairing is complete if and only if its completion embedding is an equivalence

### Bilateral Conditions
The structure of weighted completion is governed by:
- **Bilateral denseness**: Existence of the bilateral factorization within the original category
- **Bilateral compactness**: Essential uniqueness of bilateral factorizations

## Examples

### Stone-Čech Compactification
For a completely regular space $X$, the Stone-Čech compactification $\beta X$ arises as the weighted completion of:
- $I = \mathrm{Filt}(X)$ (proper filters), $J = \mathrm{UF}(X)$ (ultrafilters)
- $D(F) = X$, $E(U) = \{*\}$ 
- $Q(F,U) = \{*\}$ if $F \subseteq U$, $\emptyset$ otherwise
- $\theta$ represents the convergence relation

### Canonical Extensions  
For a distributive lattice $L$, the canonical extension $L^{\delta}$ arises as the weighted completion of:
- $I = \mathrm{Filt}(L)$ (filters), $J = \mathrm{Idl}(L)$ (ideals)
- $Q(F,I) = \{*\}$ if $F \cap I \neq \emptyset$, $\emptyset$ otherwise
- The bilateral structure captures filter-ideal interactions

### Profinite Completions
For a residually finite group $G$, the profinite completion $\hat{G}$ arises as the weighted completion of:
- $I = J = \mathrm{FinQuot}(G)$ (finite quotients)
- $Q(G/N, G/M) = \mathrm{Grp}(G/N, G/M)$
- The bilateral structure captures finite quotient relationships

## Categorical Organization

### Weighted Completion Monad
**Theorem**: Weighted completion extends to a monad $W$ on the category of bilateral pairings, with:
- **Unit**: The completion embedding morphism
- **Multiplication**: Canonical equivalence between iterated and single completion
- **Eilenberg-Moore algebras**: Complete bilateral pairings

### Relationship to Existing Frameworks
The weighted completion monad specializes to recover:
- **Garner's Isbell monad** (trivial weights, hom-profunctor structure)
- **Gabriel-Ulmer Ind/Pro completions** (filtered/cofiltered weight restrictions)

## Gem Theory

**Gem theory** studies representable bilateral completions, providing six equivalent characterizations of how presheaves arise through bilateral completion:

### Six Equivalent Facets
For $P \in [X^{\mathrm{op}}, V]$, the following are equivalent:
1. **Weighted completion facet**: $P$ arises as bilateral interpolant with Yoneda embedding structure
2. **Canonical extension facet**: $\eta_P : \int^x P(x) \otimes Y(x) \xrightarrow{\sim} P$ 
3. **Profunctor facet**: $\phi_x : C(Y(x), P) \xrightarrow{\sim} P(x)$ naturally
4. **Codensity monad facet**: $P$ is fixed by the codensity monad of $Y$
5. **Kan extension facet**: $P \to \mathrm{Ran}_Y(P \circ Y)$ is an isomorphism
6. **Distributivity facet**: $P$ distributes over finite colimits of representables

## Virtual Extension

When classical completion constructions fail due to insufficient structure, weighted completion provides **systematic virtual approximation**:

### Virtual Methodology
1. **Classical correspondence**: When classical completions exist, weighted completion recovers them exactly
2. **Virtual extension**: When classical completions fail, weighted completion provides optimal bilateral approximation
3. **Gabriel-Ulmer generalization**: Extends virtual morphism methodology from filtered/cofiltered to arbitrary bilateral weights

## Framework Correspondences

The theory establishes precise correspondences with existing frameworks:

| Framework | Correspondence | Key Insight |
|-----------|----------------|-------------|
| Schoots's categorical extensions | Filtered/cofiltered bilateral structure | P-density ⟷ Bilateral denseness |
| Pratt's communes | Identity bilateral pairings | Didensity ⟷ Bilateral conditions |
| Garner's cylinder systems | Trivial weights $Q = 1$ | Orthogonality ⟷ Bilateral denseness |
| Riehl's weighted limits | Unilateral specialization | Classical limits ⟷ Unilateral completion |
| Gabriel-Ulmer Ind-Pro | Filtered/cofiltered restriction | Virtual morphisms ⟷ Weighted completion morphisms |

## Applications

The framework has applications across several mathematical areas:

### Topology
- Systematic approach to compactification theory
- Unification of Stone-Čech, Alexandroff, and Wallman compactifications
- Virtual compactification when classical methods fail

### Algebra  
- Unified treatment of canonical extensions and MacNeille completions
- Systematic profinite completion methodology
- Virtual completion for non-residually finite groups

### Category Theory
- Extension of weighted limit theory to incomplete contexts
- Systematic virtual Kan extension methodology
- Organization of Isbell envelope theory

## Properties

### Preservation Properties
Weighted completion systematically preserves:
- Finite limits and colimits
- Monomorphisms and epimorphisms  
- Adjunctions (under appropriate conditions)
- $V$-enriched structure

### Functoriality
**Theorem**: Weighted completion is functorial with respect to morphisms of bilateral pairings, preserving factorization structure.

## Future Directions

Potential extensions include:
- Higher categorical generalizations to $(\infty,1)$-categories
- Enrichment over different base categories $V$
- Applications to type theory and programming language semantics
- Geometric realization through topological constructions

## Related Concepts

### Foundational
- [[weighted limit]] - Classical weighted limits that the theory extends
- [[profunctor]] - Bilateral weights in the framework
- [[enriched category theory]] - Base setting following Kelly's development
- [[Kan extension]] - Recovered through gem theory equivalences

### Completion Theory
- [[Isbell envelope]] - Special case with hom-profunctor structure
- [[canonical extension]] - Boolean/lattice completions via filter-ideal bilateral structure
- [[Stone-Čech compactification]] - Topological completion via filter-ultrafilter bilateral structure
- [[Gabriel-Ulmer duality]] - Extended to arbitrary weights

### Advanced
- [[cylinder factorization system]] - Geometric interpretation of bilateral factorization
- [[accessible category]] - Preservation under weighted completion
- [[virtual double category]] - Potential higher categorical extensions

## References

* Robert A. Rice, *Bilateral Weighted Completions: A Universal Framework for Mathematical Completion*, 2025

* Emily Riehl, *Weighted limits and colimits*, 2008

* Richard Garner, *The Isbell monad*, Advances in Mathematics 333:1-31, 2018  

* Peter Gabriel and Friedrich Ulmer, *Lokal präsentierbare Kategorien*, Springer LNM 221, 1971

* Vaughan Pratt, *Communes via Yoneda*, Fundamenta Informaticae 103:203-218, 2010

[[!redirects bilateral weighted completion]]
[[!redirects weighted completion]]
[[!redirects bilateral pairing]]
[[!redirects gem theory]]
[[!redirects virtual weighted limit]]

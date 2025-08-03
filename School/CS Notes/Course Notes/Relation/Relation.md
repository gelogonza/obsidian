---
Course: C241 Discrete Math
---
# Binary Relations

A binary relation R from set A to set B is a subset of the Cartesian product A × B. It defines how elements from set A are related to elements in set B.

## Key Concepts

- **Definition:** If (a,b) ∈ R, we say "a is related to b" and write aRb
- **Domain:** The set of all first elements in the ordered pairs of R
- **Range:** The set of all second elements in the ordered pairs of R

## Properties of Relations

### 1. Reflexive

A relation R on set A is reflexive if (a,a) ∈ R for all a ∈ A

```undefined
∀a ∈ A, (a,a) ∈ R
```

### 2. Symmetric

A relation R on set A is symmetric if whenever (a,b) ∈ R, then (b,a) ∈ R

```undefined
∀a,b ∈ A, if (a,b) ∈ R then (b,a) ∈ R
```

### 3. Antisymmetric

A relation R on set A is antisymmetric if whenever (a,b) ∈ R and (b,a) ∈ R, then a = b

```undefined
∀a,b ∈ A, if (a,b) ∈ R and (b,a) ∈ R then a = b
```

### 4. Transitive

A relation R on set A is transitive if whenever (a,b) ∈ R and (b,c) ∈ R, then (a,c) ∈ R

```undefined
∀a,b,c ∈ A, if (a,b) ∈ R and (b,c) ∈ R then (a,c) ∈ R
```

## Types of Relations

### 1. Equivalence Relations

A relation that is reflexive, symmetric, and transitive

- Examples: "is equal to", "is similar to", "is congruent to"

### 2. Partial Order Relations

A relation that is reflexive, antisymmetric, and transitive

- Examples: "less than or equal to", "subset of", "divides"

## Representation Methods

- **Set Notation:** R = {(a,b) | a is related to b}
- **Matrix Representation:** Using 0s and 1s to show relationships
- **Directed Graph (Digraph):** Vertices represent elements, arrows show relationships

## Applications

Binary relations are fundamental in:

- Database Management Systems
- Graph Theory
- Set Theory
- Computer Science Algorithms
- Mathematical Logic

![[image.jpg]]
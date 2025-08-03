---
Course: C241 Discrete Math
---
## **⚙️ Set Operations**

In this section, we will cover operations performed on sets, including **union**, **intersection**, **complement**, and **difference**.

### **Union of Sets ⋃**

The **union** of sets A and B includes all elements present in either set A or set B. The notation for the union of sets is: A∪BA∪B.

Think of the union as combining all elements from both sets into one, similar to pouring everything from set A and set B into a cup. Duplicate values are listed only once.

For example, given set A = {1, 4, 7} and set B = {4, 5, 6}, the union A∪BA∪B would be {1, 4, 5, 6, 7}.

Visually, the union includes everything within either circle in a Venn diagram, including the overlapping section.

The inclusion-exclusion formula relates the sizes of the sets and their union:

∣A∪B∣=∣A∣+∣B∣−∣A∩B∣∣A∪B∣=∣A∣+∣B∣−∣A∩B∣

Using the example sets A and B, we would calculate the union by adding all elements of A (1, 4, 7) to all elements of B (4, 5, 6) and then subtracting the intersection (4) to avoid duplication, resulting in the set {1, 4, 7, 5, 6}.

### **Intersection of Sets ⋂**

The **intersection** of sets A and B consists of elements common to both sets. The notation is A∩BA∩B.

If the union is thought of as an "or" condition, the intersection is like an "and". An element must be in both set A and set B to be included in their intersection.

Mathematically, A∩BA∩B is the set of all x such that x is in A and x is in B.

In the example where A = {1, 4, 7} and B = {4, 5, 6}, A∩BA∩B would be {4} because 4 is the only element present in both A and B.

If the intersection of two sets is an empty set, i.e., they have no common elements, the sets are said to be **disjoint**. In a Venn diagram, disjoint sets would appear as two separate circles with no overlap.

### **Complement of a Set 補**

The **complement** of a set A includes all elements in the **universal set** (or domain) that are not in A. The complement of A is denoted as "not A".

Mathematically, "not A" is defined as all x in the universal set such that x is not in A.

If the universal set is the digits from 0 to 9, and set A = {1, 4, 7}, then the complement of A (not A) would be {0, 2, 3, 5, 6, 8, 9}. This includes all digits from 0 to 9 except those in set A. If set B = {4, 5, 6}, then the complement of B (not B) would be {0, 1, 2, 3, 7, 8, 9}.

We can also find the complement of the union or intersection of sets. For example, the complement of A∪BA∪B would be all elements not in either A or B. The complement of A∩BA∩B would be all elements not in the intersection of A and B.

### **Difference of Sets ➖**

The **difference** between set A and set B, denoted as A - B, is the set of all elements in A that are not in B.

Mathematically, A - B is the set of all x such that x is in A but x is not in B.

Using the example sets A = {1, 4, 7} and B = {4, 5, 6}, A - B would be {1, 7}. This includes elements in A (1, 4, 7) but excludes any that are also in B (4).

### **Practice Question ❓**

Consider set A = {a, e, i, o, u} and set B, which consists of the letters in the word "discrete math". Determine:

- A∪BA∪B
- A∩BA∩B
- A−BA−B

First, rewrite set B in roster notation: B = {d, i, s, c, r, e, t, m, a, h}

- A∪BA∪B = {a, e, i, o, u, d, s, c, r, t, m, h}
- A∩BA∩B = {a, e, i}
- A - B = {o, u} because when removing a, e, and i from set A, only o and u are left.

## **Set Operations 🧮**

### **Set Difference ➖**

- The set difference between two sets A and B, denoted as A - B, consists of elements that are in A but not in B.
    - Given A = {A, E, I, O, U} and B = {A, E, I, D, S, C, R, T, H}, A - B = {O, U}.
    - Given B = {A, E, I, D, S, C, R, T, H} and A = {A, E, I, O, U}, B - A = {D, S, C, R, T, H}.
        - This is derived by removing the underlined letters (A, E, I) from set B, leaving the remaining elements.

### **Complement of Intersection 🤝**

- The complement of the intersection of sets A and B, denoted as (A∩B)′(A∩B)′, includes all elements in the universal set (U) that are not in the intersection of A and B.
    - If U is the set of all letters in the alphabet, and A∩B = {A, E, I}, then (A∩B)′ includes all letters of the alphabet except A, E, and I.
        
        A∩B
        
        (A∩B)′
        
    - (A∩B)′(A∩B)′ = {B, C, D, F, G, H, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z}

### **Subsets ⊂**

- A is a **subset** of B if all elements of A are also elements of B.
    - Denoted as A ⊆ B.
    - If A = {A, E, I, O, U} and B = {A, E, I, D, S, C, R, T, H}, A is **not** a subset of B because O and U are in A but not in B.
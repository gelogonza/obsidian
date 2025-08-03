---
Course: C241 Discrete Math
---
## **🤝 Set Relationships**

### **Set Equality**

Sets are considered **equal** if and only if they contain the same elements.

- Notation: For all X, X is an element of A if and only if X is an element of B.A=B
    
    A=B
    
- Example:
    
    If A=0,1,1,3,4,4A=0,1,1,3,4,4 and B=0,1,3,4B=0,1,3,4, then A=BA=B. Duplicates do not matter.
    
- If BB included 55, then A≠BA=B because BB has an element 55 that is not in AA.

### **Subsets**

A set AA is a **subset** of BB if every element of AA is also an element of BB.

- Venn Diagram Representation:
    
    [![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/Venn_subset.svg/300px-Venn_subset.svg.png)](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/Venn_subset.svg/300px-Venn_subset.svg.png)
    
- Example:
    
    If A=1,2,3A=1,2,3 and B=1,2,3,4,5B=1,2,3,4,5, then AA is a subset of BB.
    
- Notation: For all XX, if XX is an element in AA, then XX is an element in BB.A⊆B
    
    A⊆B
    

### **Showing That a Set is a Subset**

To show that AA is a subset of BB, demonstrate that every element of AA belongs to BB.

if X∈A, then X∈B

if X∈A, then X∈B

### **Showing That a Set is NOT a Subset**

To show that AA is **not** a subset of BB, find at least one element that belongs to AA but does not belong to BB.

There exists some element X that belongs to A, but does not belong to B

There exists some element X that belongs to A, but does not belong to B

### **Showing Two Sets Are Equal Using Subsets**

To prove that A=BA=B, show that AA is a subset of BB and BB is a subset of AA.

(A⊆B)∧(B⊆A)  ⟹  A=B

(A⊆B)∧(B⊆A)⟹A=B

### **Proper Subsets**

A set AA is a **proper subset** of BB if AA is a subset of BB, but AA is not equal to BB. This means that BB contains at least one element that is not in AA.

- Notation change: The notation changes slightly to indicate a proper subset.
- Example:
    
    If A=1,2,3A=1,2,3 and B=1,2,3,4B=1,2,3,4, then AA is a proper subset of BB.
    
- Using predicate logic: For all XX, if XX belongs to AA, then XX belongs to BB, AND there exists some element that belongs to BB that does not belong to AA.

### **🔢 Cardinality**

**Cardinality** is the number of **distinct** elements in a set.

- Notation: Represented using absolute value brackets around the set.
- Example 1:
    
    If A=1,2,3,3,3,4A=1,2,3,3,3,4, then the cardinality of AA, denoted as ∣A∣∣A∣, is 4 because there are four distinct elements.
    
- Example 2:
    
    The cardinality of the set of the alphabet is 26.
    
- Cardinality of the Empty Set:
    
    The cardinality of the empty set is 0.
    

### **🧰 Power Set**

The **power set** is the set of all subsets of a set.

- Example:
    
    If A=0,1,2A=0,1,2, then the power set of AA is ∅,0,1,2,0,1,0,2,1,2,0,1,2∅,0,1,2,0,1,0,2,1,2,0,1,2.
    
- Cardinality of a Power Set:
    
    The cardinality of the power set of a set with nn elements is 2n2n.
    
    - In the example above, the cardinality of the power set of A is 8, since 23=8.
        
        A
        
        23=8
        

### **↔️ Tuples**

A **tuple** is an **ordered** collection of elements.

- Tuples are ordered collections of elements a1,a2,...a1​,a2​,...
- Example:
    
    Ordered pairs (a1,a2)(a1​,a2​) are tuples with two elements. The order matters, unlike in sets.
    

## **Ordered Pairs and Cartesian Products 🧮**

- **Ordered pairs**: The order of elements matters, meaning (5, 2) is different from (2, 5).
- **Cartesian Product**: Denoted as A ×× B, it's the set of all ordered pairs (a, b) where 'a' belongs to set A and 'b' belongs to set B.
    - If set A = {0, 1} and set B = {2, 3, 4}, then A × B = {(0, 2), (0, 3), (0, 4), (1, 2), (1, 3), (1, 4)}.
        
        ×
        
- **Relation**: A subset of the Cartesian product.
    - If a subset R = {(0, 2), (1, 2)}, then R is a relation because it is a subset of A × B.
        
        ×
        

## **Truth Sets 💯**

- **Definition**: A truth set of P is the set of elements x in the domain such that P(x) is true.
- **Notation**: {x ∈∈ D | P(x) is true}, where D is the domain and P(x) is a propositional function.
- **Example**:
    - If the domain is the set of integers, and P(x) is |x| = 3, then the truth set is {-3, 3} because these are the values of x that make the statement true.
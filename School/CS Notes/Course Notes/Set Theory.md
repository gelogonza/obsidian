---
Course: C241 Discrete Math
---
**Sets: Collections of Objects 🧮**

A **set** is a collection of objects, referred to as **elements**. These elements can be physical objects, thoughts, ideas, concepts, or mathematical objects. Sets package objects that share similar properties. For example, the set of triangles: you can unambiguously state whether something is or isn't in this set.

The lack of ambiguity in determining what is or isn't in a set is foundational to set theory. Claims about the set can be assessed without ambiguity to determine whether they're true or false.

### **Representing Sets**

A set containing the numbers 1, 2, and 3 is written with curly brackets: {1,2,3}{1,2,3}.

We can name a set for easier reference. If A={1,2,3}A={1,2,3}, we can refer to the set as A. To express that an element belongs to a set, we use the symbol "∈∈".

If A={1,2,3}A={1,2,3}, then:

- 1∈A1∈A
- 2∈A2∈A
- 4∉A4∈/A (4 is not in A, denoted by "∈/")
    
    ∉
    

### **Set Builder Notation**

In most cases, we write a shorthand description using **set builder notation**. For example, the set of prime numbers can be written as:

P={p∣p is prime}P={p∣p is prime}

Here, pp is a variable that must satisfy a criterion (the **predicate**). The vertical line "∣∣" is shorthand for "such that".

When dealing with sets of numbers, declare explicitly which sets you're starting with before the "such that" symbol. For example:

P∈N∣p<5P∈N∣p<5

This is a different set than:

R∈R∣r<5R∈R∣r<5

### **Set Equality**

Two sets are **equal** if they contain the same elements. If for all a∈Aa∈A, a∈Ba∈B, and for all b∈Bb∈B, b∈Ab∈A, then the sets AA and BB are equal.

This definition means the order of the elements doesn't matter. For example, if A={1,2,3}A={1,2,3} and B={2,3,1}B={2,3,1}, then A=BA=B. Repetition of elements also doesn't matter for set equality.

### **Cardinality of a Set**

The **size** or **cardinality** of a set is the number of elements it contains. If A={1,2,3}A={1,2,3}, then the cardinality of AA is 3, denoted as ∣A∣=3∣A∣=3.

A set can have an infinite number of elements. For example, the set of prime numbers has infinite cardinality, denoted as ∣A∣=∞∣A∣=∞.

## **Subsets and the Empty Set 🔍**

### **Subsets**

A set is a **subset** of another if all of its elements are also elements of the other set. For example, if A={2,4,6}A={2,4,6} and B={1,2,3,4,5,6}B={1,2,3,4,5,6}, then AA is a subset of BB, denoted as A⊆BA⊆B.

**Example:**

If B={b∈N∣b is even}B={b∈N∣b is even}, which of these are subsets of B?

- A = {4}
- B = {10, 100, 1000}
- C = {a ∣ a = 2k, where k ∈N}
    
    ∣
    
    ∈N
    

AA is an element of B but not a subset. B={10,100,1000}B={10,100,1000} is a subset of BB because these are all even numbers. The set C={a∣a=2k, where k∈N}C={a∣a=2k, where k∈N} is another way of writing the even numbers, so it is equal to B and technically a subset of B.

All sets are subsets of themselves.

If AA is a subset of BB and BB is a subset of AA, then A=BA=B.

If AA is a subset of BB, but AA is not equal to BB, then AA is a **proper subset** of BB. This implies that there are elements in BB that are not in AA. A proper subset can be denoted as A⊂BA⊂B.

If AA is a subset of BB and BB is a subset of CC, then AA is a subset of CC.

### **Empty Set**

The **empty set** is a set with no elements, denoted by the symbol "∅∅".

Properties of the empty set:

- The empty set is a subset of any set. Let A be a set. Since the empty set has no elements, all elements in the empty set are also in A. Therefore, ∅⊆A.
    
    ∅⊆A
    
- The empty set is unique. If ∅1​ and ∅2​ are two empty sets, then ∅1​⊆∅2​ and ∅2​⊆∅1​. This implies that ∅1​=∅2​, meaning we only have a single unique empty set.
    
    ∅1
    
    ∅2
    
    ∅1⊆∅2
    
    ∅2⊆∅1
    
    ∅1=∅2
    

## **Combining Sets 🤝**

Two sets may share some elements. We indicate the elements in common to both sets using the overlap of two circles in a **Venn diagram**. The **union** and the **intersection** are two ways of combining the elements in two sets into a new set.

### **Union**

The **union** of two sets AA and BB is a set containing all elements in AA as well as all elements in BB.

Formally, A∪B={x∣x∈A or x∈B}A∪B={x∣x∈A or x∈B}.

The word "or" is important here. The union includes elements in both A and B.

### **Intersection**

The **intersection** of two sets AA and BB is a set containing elements that are in both AA and BB.

The intersection of AA and BB is denoted as A∩BA∩B and is formally defined as:

## **🤝 Intersection of Sets**

The **intersection** of sets A and B (denoted as A∩BA∩B) is the set containing all elements that are in both A **and** B. The word "**and**" is crucial. In a Venn diagram, this is the overlapping area.

- **Example 1:**
    - Let A={0,1} and B={1,2,3}
        
        A={0,1}
        
        B={1,2,3}
        
    - The union of A and B (A∪B) contains all elements in A and B: A∪B={0,1,2,3}.
        
        A∪B
        
        A∪B={0,1,2,3}
        
    - The intersection of A and B (A∩B) contains only elements in both A and B: A∩B={1}
        
        A∩B
        
        A∩B={1}
        
- **Example 2:**
    - Let A be the set of odd natural numbers.
    - Let B be the set of even natural numbers.
    - A∪BA∪B is the set of all natural numbers.
    - A∩B={}A∩B={} (the empty set), since there are no numbers that are both odd and even.

## **➕ Properties of Unions**

- The union of any set A with the empty set is A: A∪{}=A
    
    A∪{}=A
    
- The union of any set A with itself is A: A∪A=A
    
    A∪A=A
    
- If A is a subset of B, then A∪B=B, because all elements in A are already in B.
    
    A∪B=B
    
- The union of A and B is the same as the union of B and A: A∪B=B∪A
    
    A∪B=B∪A
    
- For three sets A, B, and C, the order of taking unions doesn't matter: (A∪B)∪C=A∪(B∪C). This generalizes to any number of sets.
    
    (A∪B)∪C=A∪(B∪C)
    

## **✖️ Properties of Intersections**

- For any set A, the intersection of A with the empty set is the empty set: A∩{}={}. The empty set has no elements in common with any other set.
    
    A∩{}={}
    
- The intersection of any set A with itself is A: A∩A=A
    
    A∩A=A
    
- If A is a subset of B, then A∩B=A, because the elements in A are also in B.
    
    A∩B=A
    
- A∩B=B∩AA∩B=B∩A: The order of the sets doesn't affect the intersection.
- (A∩B)∩C=A∩(B∩C)(A∩B)∩C=A∩(B∩C): The order of intersections doesn't matter with three or more sets. In both cases, we end up with the set containing elements found in A, B, and C.

## **🔢 Cardinality of Unions and Intersections**

Given two sets A and B:

∣A∪B∣=∣A∣+∣B∣−∣A∩B∣∣A∪B∣=∣A∣+∣B∣−∣A∩B∣

This identity is always true.

- ∣A∪B∣≤∣A∣+∣B∣∣A∪B∣≤∣A∣+∣B∣
- **Example:**
    - Let A={1,2,3} and B={3,4}
        
        A={1,2,3}
        
        B={3,4}
        
        - ∣A∣=3∣A∣=3
        - ∣B∣=2∣B∣=2
        - A∪B={1,2,3,4}A∪B={1,2,3,4} so ∣A∪B∣=4
            
            ∣A∪B∣=4
            
        - A∩B={3}A∩B={3} so ∣A∩B∣=1
            
            ∣A∩B∣=1
            
    - ∣A∪B∣=∣A∣+∣B∣−∣A∩B∣∣A∪B∣=∣A∣+∣B∣−∣A∩B∣
    - 4=3+2−14=3+2−1

## **🧮 Distributive Property**

For three sets A, B, and C:

- A∪(B∩C)=(A∪B)∩(A∪C)A∪(B∩C)=(A∪B)∩(A∪C)
- A∩(B∪C)=(A∩B)∪(A∩C)A∩(B∪C)=(A∩B)∪(A∩C)

These identities are similar to multiplying out the brackets. This kind of property in general is known as **distributivity**.

## **💡 Application of Set Theory**

Set theory can be used to manipulate logical statements.

- **Example 1:**
    - I only cycle in the summer or in the winter when it's warmer than 20 degrees Celsius.
    - Let S = summer days, W = winter days, and T = days warmer than 20°C.
    - The days I can cycle = S∪(W∩T).
        
        S∪(W∩T)
        
    - Using the distributive property: (S∪W)∩(S∪T).
        
        (S∪W)∩(S∪T)
        
        - S∪WS∪W = any day.
        - S∪TS∪T = the days when I cycle.
        - Therefore, I cycle any day of the year but only when it's summer or more than 20 degrees.
- **Example 2:**
    - I only wear white or blue shirts.
    - Let S = shirts, B = blue clothes, and W = white clothes.
    - Blue and white shirts: (B∪W)∩S.
        
        (B∪W)∩S
        
    - Using the distributive rule: (B∩S)∪(W∩S).
        
        (B∩S)∪(W∩S)
        
        - This can be interpreted as I only wear blue shirts or white shirts.

## **📝 Proving Set Equality**

To prove that two sets are equal (e.g., A=BA=B), we can show:

1. AA is a subset of B (A⊆B)
    
    B
    
    A⊆B
    
2. BB is a subset of A (B⊆A)
    
    A
    
    B⊆A
    

If both conditions are true, then A=BA=B.

- We can use this method to prove equations involving unions and intersections. First, show that A∪(B∩C) is a subset of (A∪B)∩(A∪C), and then show that (A∪B)∩(A∪C) is a subset of A∪(B∩C).
    
    A∪(B∩C)
    
    (A∪B)∩(A∪C)
    
    (A∪B)∩(A∪C)
    
    A∪(B∩C)
    

## **Set Theory Proofs**

If we have an element xx in A∪(B∩C)A∪(B∩C), then xx is in AA or in B∩CB∩C. This implies that xx is in both BB and CC. In either case, xx is in both A∪BA∪B and A∪CA∪C. Therefore, A∪(B∩C)A∪(B∩C) is a subset of (A∪B)∩(A∪C)(A∪B)∩(A∪C).

Now suppose xx is in (A∪B)∩(A∪C)(A∪B)∩(A∪C). This means that xx is in both A∪BA∪B and A∪CA∪C. If xx is not in AA, then it must be in both BB and CC, so it must be in B∩CB∩C. Otherwise, xx is in AA, so xx is in the union of AA and B∩CB∩C. This implies that (A∪B)∩(A∪C)(A∪B)∩(A∪C) is a subset of A∪(B∩C)A∪(B∩C).

Since we've shown that A∪(B∩C)A∪(B∩C) is a subset of (A∪B)∩(A∪C)(A∪B)∩(A∪C) and (A∪B)∩(A∪C)(A∪B)∩(A∪C) is a subset of A∪(B∩C)A∪(B∩C), we've proven that they are equal:

A∪(B∩C)=(A∪B)∩(A∪C)A∪(B∩C)=(A∪B)∩(A∪C)

## **Set Theoretic Difference ➖**

The **set theoretic difference** of two sets AA and BB is the set of all elements in AA that are not in BB. It is denoted by A∖BA∖B, which can be thought of as subtracting BB from AA. For simplicity, it can be referred to as A−BA−B.

**Example:**

Given:

- A={1,2,3,4,5}A={1,2,3,4,5}
- B={2,4,6,8}B={2,4,6,8}

Then:

- A−B={1,3,5}A−B={1,3,5}
- B−A={6,8}B−A={6,8}

## **Complement of a Set 💯**

If BB is a subset of AA, the set theoretic difference of AA and BB is the **complement** of BB with respect to AA. It's denoted as BcBc or C(B)C(B). The complement is like a background to B, the elements outside of B.

## **Universal Set 🌌**

The **universal set** UU is the set of all elements that are relevant for a given topic of interest. If a set AA isn't a subset of something specific, we usually assume the complement to AA is the universal set. The universal set depends on context.

**Quote:**

> in the discussion about dogs, when thinking about all non-sheep dogs, it's pointless to worry about camels

**Example:** Imagine we are throwing two dice. Let AA be the set of outcomes of rolling a pair of dice in which both dice show the same number. A sensible universal set in this case would be the set of all possible outcomes of rolling two dice, and the complement of AA would be the outcomes where each die shows a different number.

**More examples:**

- The complement of the set of odd numbers is the even numbers.
- The complement of the rational numbers is the set of irrational numbers.

With the complement, we often get something that feels like the opposite of the original set. That's because the complement negates the predicate.

With set builder notation, if we have a set AA which contains all xx from sunset BB such that it fulfills some predicate PP, well, the complement of AA, the things not in AA, must by definition not satisfy PP. So, the complement of AA is the elements xx in BB such that PP isn't true, denoted by putting the symbol before PP.

**Example:**

If AA is the set of animals that are dogs, then the complement of AA is animals that aren't dogs.

Let AA and BB be subsets of the universal set UU.

- Because nothing is in the empty set, its complement is U.
    
    U
    
- Similarly, the complement of U, which contains everything, is the empty set.
    
    U
    
- The complement of the complement of a set returns the original set: (Ac)c=A
    
    (Ac)c=A
    
- If A is a subset of B, then the complement of B is a subset of the complement of A.
    
    A
    
    B
    
    B
    
    A
    

## **De Morgan's Laws ⚖️**

1. The complement of A∪B is Ac∩Bc.
    
    A∪B
    
    Ac∩Bc
    
2. The complement of A∩B is Ac∪Bc.
    
    A∩B
    
    Ac∪Bc
    

**Examples to illustrate the laws:**

1. **First Law:**
    
    Let UU be the set of all animals, AA be the set of dogs, and BB be the set of cats. De Morgan's Law says that the complement of (dogs union cats) is equal to (dog's complement intersect cat's complements). Animals that are neither dogs nor cats are not dogs and are not cats. (A∪B)c=Ac∩Bc(A∪B)c=Ac∩Bc
    
2. **Second Law:**
    
    If UU is the set of natural numbers, AA is the set of prime numbers, and BB is the set of xx in the natural numbers such that x<100x<100. Using De Morgan's Law, we get that the complement of (prime and less than 100) is equal to (the complement of prime numbers) or (the complement of less than 100). Remember, the complement is like changing "true" to "not true". So, the set of numbers that are not prime and less than 100 is the set of numbers that are either not prime or greater than 100. (A∩B)c=Ac∪Bc(A∩B)c=Ac∪Bc Notice that we're allowing numbers greater than 100, but only those that are not prime.
    

## **De Morgan Duality Principle ♾️**

Given any set theoretic identity involving the union and the intersection, if the union and intersection are interchanged throughout, then the result will be another valid identity. For all of these identities you've seen so far that they come in pairs, you'll be happy to know that you can just remember one of them and exchange the union and the intersections to get a second one.

## **Sets as Elements 🧱**

The elements of a set may be sets themselves. If we have a set AA, then the set containing 0 is an element of AA, but not 0 on its own, since the elements of AA are all sets. Here, it becomes tricky to keep track of what's an element and what's a subset. The set containing zero isn't a subset of AA, it's an element.

**Example:**

If A={{0},{0,1},{0,1,2}}A={{0},{0,1},{0,1,2}}, then {0}∈A{0}∈A but {0}⊈A{0}⊈A. However, ${{0}} \subseteq A$$.

## **Power Set 💪**

The **power set** of AA, denoted as P(A)P(A), contains all subsets of AA.

**Definition:** P(A)={x∣x⊆A}P(A)={x∣x⊆A}

**Example:**

If A={0,1}A={0,1}, then P(A)={∅,A,{0},{1}}P(A)={∅,A,{0},{1}}.

## **Indexed Families of Sets 👨‍👩‍👧‍👦**

Each element, which is a set itself, is indexed by a number and usually written as a subscript. So A={Ai∣i∈{1,2,3}}A={Ai​∣i∈{1,2,3}} is saying that AA contains three sets: A1A1​, A2A2​, and A3A3​.

**Example:**

If A={{0},{0,1},{0,1,2}}A={{0},{0,1},{0,1,2}}, we can write this as A1A1​, A2A2​, and A3A3​, where:

- A1={0}A1​={0}
- A2={0,1}A2​={0,1}
- A3={0,1,2}A3​={0,1,2}

Imagine a set containing everything... everything in the universe!

## **Set Theory 🧮**

### **Omega Set 🤯**

- **Omega** is the set containing everything imaginable and all combined knowledge.
- It has the property of containing itself.
- This leads to an infinite regress of omegas within omegas.

### **Russell's Paradox 😕**

- A modification of the **definition of omega**: Omega is the set containing all sets that do not contain themselves.
- **Russell's Paradox**:
    - Assume omega isn't a member of itself. By definition, it must contain itself.
    - If it does contain itself, it can't contain itself.
- This paradox is less about the set construction and more about the **definition of a set**.

### **Naive Set Theory 😵‍💫**

- It doesn't provide guidance on what constitutes a set.
- Generally, this isn't a concern, but it can lead to problems like Russell's Paradox.

### **Axiomatic Set Theory 😎**

- Aims to navigate the paradoxes of naive set theory.
- Provides a rigorous definition of what a set is through a list of axioms.
- These **axioms** are statements that something must satisfy to be a set.
---
Course: C241 Discrete Math
---
## **Direct Proof 📝**

In a **direct proof**, we assume the **antecedent** is true and use rules of inference, axioms, and definitions to show that the **consequent** is true.

- Assume P is true.
- Prove Q is true.

### **Example: If n is an odd integer, then n2n2 is odd**

1. Assume **P is true**: n is an odd integer.
2. By the definition of an odd integer, n=2k+1, where k is an integer.
    
    n=2k+1
    
3. Goal: show that n2 is odd.
    
    n2
    
    - Square both sides of the equation: n2=(2k+1)2.
        
        n2=(2k+1)2
        
    - Expand the right side: n2=4k2+4k+1.
        
        n2=4k2+4k+1
        
    - Factor out a 2 from the first two terms: n2=2(2k2+2k)+1.
        
        n2=2(2k2+2k)+1
        
    - Let R=2k2+2k, where R is an integer.
        
        R=2k2+2k
        
    - Then, n2=2R+1.
        
        n2=2R+1
        
4. Since n2 can be written in the form 2R+1, where R is an integer, n2 is odd.
    
    n2
    
    2R+1
    
    n2
    
5. Therefore, n2 is odd.
    
    n2
    

### **Definitions for Even and Odd Integers**

|   |   |
|---|---|
|**Concept**|**Definition**|
|Even integer|n=2×Kn=2×K, where K is some other integer|
|Odd integer|n=2K+1n=2K+1, where K is some other integer|

## **Sum of Two Even Integers ➕**

Prove: The sum of two even integers is even.

1. Assume **A** and **B** are even integers.
2. By the definition of an even integer:
    - A=2KA=2K, for some integer K.
    - B=2MB=2M, for some integer M.
3. Goal: show that A+B is even.
    
    A+B
    
    - A+B=2K+2MA+B=2K+2M.
    - Factor out a 2: A+B=2(K+M).
        
        A+B=2(K+M)
        
    - Let R=K+M, where R is an integer.
        
        R=K+M
        
    - Then, A+B=2R.
        
        A+B=2R
        
4. Since A+B can be written in the form 2R, where R is an integer, A+B is even.
    
    A+B
    
    2R
    
    A+B
    
5. Therefore, the sum of two even integers is even.

### **Notation for Completion of Proof**

- Three dots in a triangle formation: therefore
- ◻: end of proof
- △: end of proof
- Q.E.D.: quod erat demonstrandum, "what was to be demonstrated"

## **Proof by Contraposition 🔄**

The lecture transitions to the next method of proof, proof by contraposition.
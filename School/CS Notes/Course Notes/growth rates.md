---
Course: C241 Discrete Math
---
logarithms and exponentials via trees

- recall a perfect binary tree
    - perfect means all leaves are the same level
    - every non leaf has 2 children
- how many leaves are at the lth level? 2^l
- at what height do we obtain n vertices for n a power of 2?
- at what height do we obtain n vertices for a given n, and what values of n are potentially the number of vertices in a perfect binary tree?
- induction proofs
- binary search tree
    - tree if which each left child is ordered before its parent, and each right child is ordered after its parent
    - each node has at most 2 children
- exponential
- polynomial
- logarithmic
- linear
- constant
- quadratic
- universal, existential claims
    - a is a subset of b for every a in A, a in B
    - f is onto ~ universal-existential
    - for every y in codmain there exists x in domain
- can precompute small inputs
    - rsa cryptography - basically says to crack the key need, to run hard factoring algorithm
    - inverting hashed passwords is also a hard computation
    - rainbow table is a pre-computation of small hashes

### Moore’s Law

- number of transistors in a computer chip doubles about every 2 years
    - basically computing power growing exponentially in time

### Big O notation

- f(n) = O(g(n))
---
Course: C241 Discrete Math
Date: 2025-04-02
---
- For functions f, g! N → N, f is eventually smaller than g if Em is an element of N such that for very n > m, f(n) < g(n)
- Fix some a element of all real numbers, a > 0. is a^n eventually smaller/bigger than n! ? does this depend on which “a” we chose?
- Try on some examples
    - try a = 3
    - n = 5
        - get 3^5 = 345 > 5! = 120
    - n = 10
    - 3^10 = 59,049 < 10! = 3,628,800
    - n = 9
        - 3^9 = 19683, 9! = 362880
    - n = 7
        - 3^7 = 2187 < 7! = 5040
- After all these examples we see that a^n is smaller than n!

a = ?

We cant be sure if it holds for every a, n

- Claim: n! is eventually larger than a^n for every b element of N
    - f(n) = n!, g(n) = a^n. f is evenually larger than g for very choice of a
- Proof: D = fine m = 2a^2
    - Case 0 : Assume n is an element of N, n > m, and n is even
        - n! = n(n-1)… 1>/n(n-1)… n/2 = n Pi i, ≥ (n/2)^n/2
        - Since we chose n> 2a^2, n/2 > a^2
        - Hence n/2^(n/2) > a^2(^n/2) = a^n
        - So for every even n> m =2a^2, a^n ≤ n!
    - Case 1: Assume n is an element of N, n>m, and n is odd
        - Assume that (n-1)! > a^(n-1). Subgoal: n! > a^n
        - n! = n(n-1)! > na^n-1 If n>2a^2 > , then na^n-1 > a^n
        - We know by case 0 that (n-1)!2a^(n-1) so this completes the proof
- Features of “eventually smaller/larger”, Big-O
    - need to choose a smallest “m^n, then prove for every n>m.
    - **Strategy that could be beneficia**l could be to prove m larger
- Derivatives of Induction
    - not always induction proofs

  

### Let g: N imply N be a function

O(g) = {h| h: N → N, E c, m elemtn of N such that V n >/m, h(h)< cg(n)}

- “f(n) = O(g(n)) = f element of O(g)
- Simple example
    - Claim: 2^n+1 element of O(2^n)
    - Choose c = 3. Choose m = 0
    - 2^n+1 = 2*2^n <3 *2^n for every n element of N
    - so 2^n+1 ≤ c2^n Vn , so 2^n+1 element of O(2^n)

  

### Question: 2^n+a element O(2^n+b) Va, b element of R?

  

  

Question define f(n) = a^n, g(n) = n! for some a > 0 is f an element of O(g)

- Hint: is “f is an element of O(g)” easier to show than “f is eventually smaller than g”?
- “f element O(g) = ….
- “ f is eventually smaller than g” …..
- Does P imply Q and/or Q imply P?
- P is implied by R….
    - R is equivalent to Q
    - Q implies P
---
Course: C241 Discrete Math
Date: 2025-03-24
---
# Probability/Randomness

- randomized algos are often easier to develop than deterministic
- takes as input: problem to solve, some random bits
- study possibility of correct input
- relevant in ML/AI
- too much to ask that a model or AI is always correct
- probably approximately correct computation
- security: how likely is it that someone could guess the decryption key?
- quantum computing, bovel paradigms
- Terms
    - **sample space** of an **experiment**
    - repeatable procedure with a well defined **set** of possible outcomes
    - an event is a subset of the sample space
        - in a coin flip the sample space could be something like H,T(heads, tails)
            - outcomes are h,t
            - events: {} 0% probability
                - (H} 50% PROB
                - {T} 50% PROB
                - {h,T} 100% probability, sum to 100% sum to 1
            - Probability; a real number between 0 and 1
                - 50% 50/100= 1/2
                - probabilities of single outcome events sum to 1
        - Rolling a 6 sided die (experiment)
            - outcomes: 1,2,3,4,5,6
                - in many cases we would assume that P({1})= P({2}). and so on until Probability of 6 = 1/6 (unweighted)
                - when the outcomes are equally likely , for any event E, is a subset of the sample space A, the probability p(E) = |E|/|A| (cardinality of e divide by cardinality of a)
        - Rolling two dice / rolling a dice twice
            - outcome become pairs
                - (1,1), (1,2)
        - 2 rules for combining probabilities
            - if A and B are **mutually exclusive** events, then P(E) + P(B) = Probability of either event E or event B happening.
                - Example: what is the prob that rolling one die yields either 1 or 6?
                - P(E union B) = P(E) + P(B) = 1/6 to 1/3
            - If A and B are **independent events**, meaning that observing A doesnt change the probability of B, then the probability of **both** happening is P(A) * P(B)
                - prob of getting 3 tails in a row? (from 3 coin flips) = 1/2 * 1/2 * 1/2 = 1/8
                - a diffferent setup:
                    - 3 coinn flips sample space {(h,h,h), (h,h,t)
                    - E= {(T,T,T)}
                    - P(E) = |E| / |S| = 1/8
                    - (fair coins)
            - 1 fair coin, 1 die roll
                
                - S={(H,1), (T,1), (H,2), (T,2)
                - |S| = 2*6 = 12 rule of product
                
                  
                
        - Sample space S, Event E subset of S
            - What is the probability that E doesnt occur?
                - Let C subset of E be another event. what is the probability that E occurs but not C?
                    - P(S-E) or P(E’) universe as S
                    - p(E intersect C’) or P(E-C)
            - When outcomes are equally likely, probability~combinatorics
                - What is the probability that a permutation of the numbers 1-10 puts 1 before 2?
                - recall what to do when you get more outcomes than you want when using a formula
                    - **Rule of division**
                        - how many permutations are there of {1…10}?
                            - 10! in total
                            - How many put 1 before 2?
                            - 8! permutation od 3-19 (x3,x4,x5,x6,x7,x8)
                            - 9 place to insert 1 or 2
                            - Observe in any permutation of 1-10 I can exchange whether it is in E(permutations putting 2 before 2) by exchanging positions of 1 and 2
                                - Means that for each key in E there is exactly 1 p prime in E’
                                    - |S| = 2|E| So p(E) = |E|/|S| = 1/2
                                        - use rule of division and have 10! = number of perms 1-10/ 2! = number of perms 1.2 = |E|
                                        - |S| = 10! which equals 1/2
                    - in many cases involving probabilities of sets there are usually brute forces solutions and in many cases there are simpler ways to get there

# Induction

- extremely important proof technique
    - used to prove results about complexity of algorithms, computer program correctness, theorems about graphs and trees

### Example: Climbing an infinite ladder

- Suppose that we have an infinite ladder and we want to know whether we can reach every step on this ladder.
    - We know we can reach the first rung of the ladder
    - If we can reach a particular rung of the ladder, then we can reach the next rung
        - Can we conclude that we can reach every rung?
            - Yes because we can reach the first rung which implies that we can reach the next rung. Since we can reach the next rung then that means we can reach the rung after that; we can clim the ladder infinitely.
                
                ![[Untitled.png]]
                

### Proof by Mathematical induction

- has two parts
    - **Basis step** - where we show that P(1) is true
    - **Inductive step** - where we show that for all positive integers k, if P(k) is true, then P(k+1) is true
- To complete the inductive step of a proof using mathematical induction
    - assume that P(k) is true for an arbitrary positive integer k, then show that under this assumption, P(k+1) must also be true
        - this would be called the **inductive hypothesis**
        - once we complete both steps in the inductive step, we have shown that P(n) is true for all positive integers n, we have also shown that ∀_nP_(_n_) is true where the quantification is over the set of positive integers. In the inductive step, we show that ∀_k_(_P_(_k_) → _P_(_k_ +1)) is true, where again, the domain is the set of positive integers.
        - the proof technique can be stated as
            - (_P_(1) ∧∀_k_(_P_(_k_) → _P_(_k_ +1))) → ∀_nP_(_n_)_, when the domain is the set of positive integers_
        - it is worthwhile to explain in detail, the steps of a proof using **induction**
        - After completing both the basis and inductive steps of a proof that P(n) is true for all positive integers n, we know that P(1) is true. We can conclude that P(2) is true because we know that P(1) is true, and from the inductive step we know that P(1) implies P(2), and by this logic through induction we could also say that P(3) is true because P(2) is true and P(2) implies P(3), and so on using a finite number of implications we can show that P(n) is true for any particular positive integer n

### Domino Example for Induction

  

  

![[Domino_Induction_Example.png]]

- Consider an infinite row of dominoes, labeled 1, 2, 3,…, n, where each domino is standing. Let P(n) be the proposition that domino n is knocked over. if the first domino is knocked over then P(1) is true and if the _kth_ domino is knocked over then it also knocks the (k+1)st domino over, that is if P(k) implies P(k+1) is true for all positive integers k then all the dominos are knocked over.

  

  

*alternative to calculus

Which is bigger? 2^n or 3n?

|   |   |   |
|---|---|---|
|n|2^n|3n|
|0|1|0|
|1|2|3|
|2|4|6|
|3|8|9|
|4|16|12|
|5|32|15|
|6|64|18|

for all n greater than or equal to 4

**Claim: 2^n > 3n V n >4**

*Could prove using calculus

**Proof by Induction**

- every universal claim could be analyzed as a possibly infinite proof by cases
- case 0; n=4 (2^4 = 16>12 = 3:4
- case 1: n = k+1, where k greater than or equal to 4
    - Induction hypothesis: 2^k is greater than or equal to 3k, suppose this is true
    - Subgoal: prove that 2^k+1 greater than or equal to 3(k+1)
    - 2^k+1 = 2(2^k)=2^k + 2^k greater than or equal to 3k+3k = 6k greater than 3k+1=3(k+1)
    - So the subgoal holds, by induction the original claim holds
    - Base case: n=4 2^4 is greater than 3*4, same goes for n=5, and n=6
        - base cases shows for smallest n considered
        - Induction step: show that if it holds for k then it hold for k+1
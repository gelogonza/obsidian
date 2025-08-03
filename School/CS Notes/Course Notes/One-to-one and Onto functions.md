---
Course: C241 Discrete Math
---
# 🚀 One-to-One (Injective) Functions

## 📝 Definition

A function f:A→Bf: A \to Bf:A→B is called **one-to-one** (also known as **injective**) if **no two distinct elements** in AAA map to the **same** element in BBB. Formally:

If f(a1)=f(a2), then a1=a2.\text{If } f(a_1) = f(a_2), \text{ then } a_1 = a_2.

If f(a1​)=f(a2​), then a1​=a2​.

Equivalently:

If a1≠a2, then f(a1)≠f(a2).\text{If } a_1 \neq a_2, \text{ then } f(a_1) \neq f(a_2).

If a1​=a2​, then f(a1​)=f(a2​).

## 🌐 Intuitive Understanding

- **Real-world analogy**: Think of **one-to-one** like assigning **unique student IDs** to students: no two different students share the **same** ID number.
- Another perspective: **different inputs** lead to **different outputs**.

### Examples

1. **Numerical**: f(x)=x+1f(x) = x + 1f(x)=x+1 over the integers Z\mathbb{Z}Z.
    - If f(a1​)=f(a2​), then a1​+1=a2​+1⟹a1​=a2​. No collisions ⇒ injective.
        
        f(a1)=f(a2)f(a_1) = f(a_2)
        
        a1+1=a2+1  ⟹  a1=a2a_1 + 1 = a_2 + 1 \implies a_1 = a_2
        
2. **Non-injective**: g(x)=x2g(x) = x^2g(x)=x2 over the integers Z\mathbb{Z}Z.
    - g(2)=g(−2)=4g(2) = g(-2) = 4g(2)=g(−2)=4. Different inputs (2 and −2) yield the **same** output (4), so it fails to be one-to-one on Z.
        
        22
        
        −2-2
        
        44
        
        Z\mathbb{Z}
        

### Checking One-to-One

1. **Algebraic approach** (if you have a formula): Assume f(a1​)=f(a2​) and see if that forces a1​=a2​.
    
    f(a1)=f(a2)f(a_1) = f(a_2)
    
    a1=a2a_1 = a_2
    
2. **Counterexamples**: If you can find **at least one pair** (a1​,a2​) with a1​=a2​ but f(a1​)=f(a2​), then the function is **not** injective.
    
    (a1,a2)(a_1, a_2)
    
    a1≠a2a_1 \neq a_2
    
    f(a1)=f(a2)f(a_1) = f(a_2)
    

---

# 🚀 Onto (Surjective) Functions

## 📝 Definition

A function f:A→Bf: A \to Bf:A→B is **onto** (also called **surjective**) if **every** element of BBB is an output of **at least one** element in AAA. Formally:

∀b∈B, ∃a∈A:f(a)=b.\forall b \in B,\, \exists a \in A : f(a) = b.

∀b∈B,∃a∈A:f(a)=b.

## 🌐 Intuitive Understanding

- **Real-world analogy**: If you think of B as **“slots to be filled,”** surjective means **each slot in BBB is filled** by at least one element from A.
    
    BB
    
    AA
    
- Another perspective: For **each** potential output in B, there is some input in A that hits it.
    
    BB
    
    AA
    

### Examples

1. **Surjective**: f(x)=x+1f(x) = x + 1f(x)=x+1 from Z\mathbb{Z}Z to Z\mathbb{Z}Z.
    - For **any** integer m∈Z, we can find n=m−1 in Z such that f(n)=n+1=(m−1)+1=m. So every integer in the codomain is “reached” by some input.
        
        m∈Zm\in \mathbb{Z}
        
        n=m−1n = m - 1
        
        Z\mathbb{Z}
        
        f(n)=n+1=(m−1)+1=mf(n)=n+1=(m-1)+1=m
        
2. **Not Surjective**: g(x)=x2g(x) = x^2g(x)=x2 from Z\mathbb{Z}Z to Z\mathbb{Z}Z.
    - There’s **no integer** n such that n2=−1. So −1∈Z is never an output, failing surjectivity.
        
        nn
        
        n2=−1n^2 = -1
        
        −1∈Z-1\in \mathbb{Z}
        

### Checking Onto

1. **Method**: Pick an **arbitrary** element b∈B. Show there **exists** some a∈A such that f(a)=b.
    
    b∈Bb\in B
    
    a∈Aa\in A
    
    f(a)=bf(a)=b
    
2. **Counterexample**: If you can find just **one** element in B that is **never** produced by any a∈A, it’s **not** onto.
    
    BB
    
    a∈Aa\in A
    

---

# 🔀 Combining One-to-One & Onto

When a function is both **one-to-one** and **onto**, it’s called a **bijection** (or **bijective**). Bijections have special properties, like **inverses**.

- **Bijection**: f is **injective** + **surjective**.
    
    ff
    
- **Inverse function**: If f is bijective, we can define f−1 that “undoes” f.
    
    ff
    
    f−1f^{-1}
    
    ff
    

Example: f(x)=x+1f(x)=x+1f(x)=x+1 on Z\mathbb{Z}Z is both injective **and** surjective, hence bijective. Its inverse is f−1(y)=y−1f^{-1}(y)=y-1f−1(y)=y−1.

---

# 📚 Key Takeaways and Quick Reference

1. **One-to-One (Injective)**:
    - Distinct inputs → Distinct outputs.
    - Check by setting f(a1​)=f(a2​) and seeing if that forces a1​=a2​.
        
        f(a1)=f(a2)f(a_1)=f(a_2)
        
        a1=a2a_1=a_2
        
2. **Onto (Surjective)**:
    - Every element in the codomain is mapped to by some element of the domain.
    - Check by taking an arbitrary b∈B and solving f(a)=b.
        
        b∈Bb\in B
        
        f(a)=bf(a)=b
        
3. **Why it Matters**:
    - **Injective** means no “collisions” among outputs.
    - **Surjective** means the function “covers” the entire codomain.
    - **Bijective** means both—perfect “pairing” between A and B.
        
        AA
        
        BB
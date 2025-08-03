---
Course: C241 Discrete Math
---
## **Truth Tables for Compound Propositions 📝**

Truth tables are used to show **equivalencies** between different **compound propositions**.

### **Number of Rows**

To determine the number of rows needed:

- Each proposition can be either **true** or **false**.
- Use the formula: 2n, where n is the number of propositions.
    
    2n
    

### **Number of Columns**

To determine the number of columns needed:

- One column for each **propositional variable**.
- One column for every **expression** in the compound proposition.
- One column for the **final result**.

### **Order of Operations**

It's important to know the **order of operations** for logical operators.

### **Example**

Let's construct a truth table for the compound proposition: P or Q implies not R, written as (P∨Q)  ⟹  ¬R(P∨Q)⟹¬R

**Step 1**: Construct columns for each proposition P, Q, and R.

With 3 propositions, we have 23=823=8 rows.

|   |   |   |
|---|---|---|
|**P**|**Q**|**R**|
|True|||
|True|||
|True|||
|True|||
|False|||
|False|||
|False|||
|False|||

**Step 2**: Create a column for each compound proposition (P∨QP∨Q) and (¬R¬R), and a column for the final result (P∨Q)  ⟹  ¬R(P∨Q)⟹¬R.

**Truth Table Structure**:

|   |   |   |
|---|---|---|
|**Propositions**|**Compound Propositions**|**Result**|
|P, Q, R|P∨QP∨Q, ¬R¬R|(P∨Q)  ⟹  ¬R(P∨Q)⟹¬R|

**Completed Left-Hand Side of the Truth Table**:

|   |   |   |
|---|---|---|
|**P**|**Q**|**R**|
|True|True|True|
|True|True|False|
|True|False|True|
|True|False|False|
|False|True|True|
|False|True|False|
|False|False|True|
|False|False|False|

### **Filling in the Middle Section**

- P∨QP∨Q: True if either P or Q is true.
- ¬R¬R: The negation of R (reverses the truth value of R).

|   |   |   |   |   |
|---|---|---|---|---|
|**P**|**Q**|**R**|**P∨QP∨Q**|**¬R¬R**|
|True|True|True|True|False|
|True|True|False|True|True|
|True|False|True|True|False|
|True|False|False|True|True|
|False|True|True|True|False|
|False|True|False|True|True|
|False|False|True|False|False|
|False|False|False|False|True|

### **Final Solution**

(P∨Q)  ⟹  ¬R(P∨Q)⟹¬R

An implication is true if:

- Both parts are true.
- The first part (hypothesis) is false.

|   |   |   |   |   |   |
|---|---|---|---|---|---|
|**P**|**Q**|**R**|**P∨QP∨Q**|**¬R¬R**|**(P∨Q)  ⟹  ¬R(P∨Q)⟹¬R**|
|True|True|True|True|False|False|
|True|True|False|True|True|True|
|True|False|True|True|False|False|
|True|False|False|True|True|True|
|False|True|True|True|False|False|
|False|True|False|True|True|True|
|False|False|True|False|False|True|
|False|False|False|False|True|True|

### **Practice 🚀**

Create a truth table for the implication: (P∨¬Q)  ⟹  (P∧Q)(P∨¬Q)⟹(P∧Q)

**Given**:

- Propositions: P, Q
- Rows: 4
- Columns: 6

### **Solution**

**Step 1**: Set up the columns for the propositions P and Q.

|   |   |
|---|---|
|**P**|**Q**|
|True|True|
|True|False|
|False|True|
|False|False|

**Step 2**: Add columns for the intermediate expressions: ¬Q¬Q, P∨¬QP∨¬Q, and P∧QP∧Q.

- ¬Q¬Q is the negation of Q.
- P∨¬QP∨¬Q is true if either P or ¬Q is true.
    
    ¬Q
    
- P∧QP∧Q is true if both P and Q are true.

|   |   |   |   |   |
|---|---|---|---|---|
|**P**|**Q**|**¬Q¬Q**|**P∨¬QP∨¬Q**|**P∧QP∧Q**|
|True|True|False|True|True|
|True|False|True|True|False|
|False|True|False|False|False|
|False|False|True|True|False|

**Step 3**: Create the column for the final result: (P∨¬Q)  ⟹  (P∧Q)(P∨¬Q)⟹(P∧Q).

|   |   |   |   |   |   |
|---|---|---|---|---|---|
|**P**|**Q**|**¬Q¬Q**|**P∨¬QP∨¬Q**|**P∧QP∧Q**|**(P∨¬Q)  ⟹  (P∧Q)(P∨¬Q)⟹(P∧Q)**|
|True|True|False|True|True|True|
|True|False|True|True|False|False|
|False|True|False|False|False|True|
|False|False|True|True|False|False|
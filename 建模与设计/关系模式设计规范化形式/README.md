# Normal Form of Relation Schema Design

<img src="README.assets/image-20221219184910451.png" alt="image-20221219184910451" style="zoom:50%;" />

<img src="README.assets/image-20221219184924968.png" alt="image-20221219184924968" style="zoom:50%;" />

## First Normal Form

<img src="README.assets/image-20221219185144105.png" alt="image-20221219185144105" style="zoom:67%;" />

-   No **composite attribute**
-   No **multi-valued attribute**

>   Example:
>
>   <img src="README.assets/image-20221219185249999.png" alt="image-20221219185249999" style="zoom:50%;" />

---

Handle situation where 1NF is violated:

<img src="README.assets/image-20221219191521936.png" alt="image-20221219191521936" style="zoom:50%;" />

## Second Normal Form

<img src="README.assets/image-20221219204728954.png" alt="image-20221219204728954" style="zoom:67%;" />

-   ***Partial Function Dependency***, but notice that it is alternative attribute and candidate key
-   Uncontrolled redundancy: attributes related with **partial dependency** causes the **other attributes** being redundant
-   Schema decomposition

>   Examples:
>
>   <img src="README.assets/image-20221219205158260.png" alt="image-20221219205158260" style="zoom:50%;" />

## Third Normal Form

### 1 Definition

<img src="README.assets/image-20221219210108395.png" alt="image-20221219210108395" style="zoom:50%;" />

-   ***Transitive function dependency*** is nonexistent, but notice X is candidate key, A is alternative attribute

    >   Refer to the definition of transitive function dependency

-   Uncontrolled redundancy: the **transitivity** itself is **redundant**. Since the deduction is certain,  there is no need to add the **deduced attributes** in the schema

>   Examples:
>
>   <img src="README.assets/image-20221219210120243.png" alt="image-20221219210120243" style="zoom:50%;" />
>
>   -   **Argumentation rule** is required in the demonstration
>
>   <img src="README.assets/image-20221219212029322.png" alt="image-20221219212029322" style="zoom:50%;" />

### 2 Relation Schema Decomposition

<img src="README.assets/image-20221219220116592.png" alt="image-20221219220116592" style="zoom:50%;" />

1.   **Decompose** into schemas composed by single function dependency
2.   **Combine** some schemas, ensuring 3NF

## Boyce-Codd Normal Form

### 1 Definition

<img src="README.assets/image-20221219220458082.png" alt="image-20221219220458082" style="zoom:67%;" />

-   All function dependencies’ left parts contain a candidate key

>   Examples:
>
>   <img src="README.assets/image-20221219220832840.png" alt="image-20221219220832840" style="zoom:50%;" />
>
>   -   Notice the **definition** of transitive function dependency, this situation doesn’t satisfy **all the conditions**
>
>   <img src="README.assets/image-20221219221605147.png" alt="image-20221219221605147" style="zoom:50%;" />

<img src="README.assets/image-20221219221719802.png" alt="image-20221219221719802" style="zoom:50%;" />

### 2 Relation Schema Decomposition

<img src="README.assets/image-20221219221950003.png" alt="image-20221219221950003" style="zoom:67%;" />

## Multi-valued Dependency

### 1 Definition

<img src="README.assets/image-20221219222257551.png" alt="image-20221219222257551" style="zoom:67%;" />

<img src="README.assets/image-20221219222813661.png" alt="image-20221219222813661" style="zoom:50%;" />

-   For those tuples which have the same X, their Y can be randomly exchanged, the result tuples also belong to the same relationship

### 2 Properties

<img src="README.assets/image-20221219222832261.png" alt="image-20221219222832261" style="zoom:67%;" />

>   Example:
>
>   <img src="README.assets/image-20221219222847483.png" alt="image-20221219222847483" style="zoom:67%;" />

### 3 Axioms and Theorems

<img src="README.assets/image-20221220105723353.png" alt="image-20221220105723353" style="zoom:67%;" />

-   Transitivity in multi-valued dependency is more strict

<img src="README.assets/image-20221220110004373.png" alt="image-20221220110004373" style="zoom:50%;" />

-   A7 and A8 indicate the relation between function dependency and multi-valued dependency

>   Examples of demonstration
>
>   <img src="README.assets/image-20221220110508450.png" alt="image-20221220110508450" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221220111839603.png" alt="image-20221220111839603" style="zoom:50%;" />
>
>   -   Notice that $X\cap Z\subseteq Z,X\cap Z\subseteq X$
>   -   Notice that w[Y]=s[Y] and w[U-Z-Y]=s[U-Z-Y], so w[U-Z]=s[U-Z]
>
>   <img src="README.assets/image-20221220112231852.png" alt="image-20221220112231852" style="zoom:50%;" />

<img src="README.assets/image-20221220112412217.png" alt="image-20221220112412217" style="zoom:50%;" />

## Forth Normal Form

<img src="README.assets/image-20221219223746957.png" alt="image-20221219223746957" style="zoom:50%;" />

-   The conditions aim to eliminate **non-trivial function dependency**
-   By contrast with **BCNF**, here it is **multi-valued dependency**

<img src="README.assets/image-20221219224052577.png" alt="image-20221219224052577" style="zoom:50%;" />

---

<img src="README.assets/image-20221219224138947.png" alt="image-20221219224138947" style="zoom:50%;" />

## Brief Summary

<img src="README.assets/image-20221220112541761.png" alt="image-20221220112541761" style="zoom:50%;" />
# Functional Dependency with Its Axiom and Theorem

<img src="README.assets/image-20221219133206901.png" alt="image-20221219133206901" style="zoom:50%;" />

<img src="README.assets/image-20221219133241249.png" alt="image-20221219133241249" style="zoom:67%;" />

## Functional Dependency

### 1 Definition

<img src="README.assets/image-20221219133844334.png" alt="image-20221219133844334" style="zoom:50%;" />

<img src="README.assets/image-20221219134022843.png" alt="image-20221219134022843" style="zoom:50%;" />

It’s important to find **data dependency sets**

>   Examples:
>
>   <img src="README.assets/image-20221219134624678.png" alt="image-20221219134624678" style="zoom:50%;" />
>
>   We need some careful analysis to get all the functional dependencies

### 2 Character of functional Dependency

<img src="README.assets/image-20221219135225991.png" alt="image-20221219135225991" style="zoom:67%;" />

>   Examples:
>
>   <img src="README.assets/image-20221219135317393.png" alt="image-20221219135317393" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221219135327047.png" alt="image-20221219135327047" style="zoom:50%;" />

There may be some constraints concerning functional dependency

### 3 Full functional Dependency and Partial functional Dependency

#### 3.1 Definition

<img src="README.assets/image-20221219151532029.png" alt="image-20221219151532029" style="zoom:50%;" />

<img src="README.assets/image-20221219151701683.png" alt="image-20221219151701683" style="zoom:67%;" />

In partial functional dependency, there are uncontrolled redundancies

>   Examples:
>
>   <img src="README.assets/image-20221219152032478.png" alt="image-20221219152032478" style="zoom:50%;" />

### 4 Transitive functional Dependency

<img src="README.assets/image-20221219152746517.png" alt="image-20221219152746517" style="zoom:50%;" />

<img src="README.assets/image-20221219152757390.png" alt="image-20221219152757390" style="zoom:67%;" />

-   There must be “real three parts” in the transitive functional dependency
-   The conditions aim to eliminate **non-trivial** functional dependencies
-   There will be uncontrolled redundancies in transitive functional dependency

>   Examples:
>
>   <img src="README.assets/image-20221219153221239.png" alt="image-20221219153221239" style="zoom:50%;" />

## Concepts Concerning functional Dependency

### 1 Candidate Key and Primary Key

<img src="README.assets/image-20221219153426620.png" alt="image-20221219153426620" style="zoom:50%;" />

<img src="README.assets/image-20221219153652461.png" alt="image-20221219153652461" style="zoom:50%;" />

-   Candidate Key
-   Primary Key
-   Prime Attribute
-   Alternative Attribute

>   Examples:
>
>   <img src="README.assets/image-20221219153829284.png" alt="image-20221219153829284" style="zoom:50%;" />

### 2 Foreign Key

<img src="README.assets/image-20221219153953898.png" alt="image-20221219153953898" style="zoom:50%;" />

### 3 Logical Implications

<img src="README.assets/image-20221219154408420.png" alt="image-20221219154408420" style="zoom:50%;" />

-   The two red girds below indicate the same thing

### 4 Closure

<img src="README.assets/image-20221219155046850.png" alt="image-20221219155046850" style="zoom:50%;" />

## Axioms and Theorems

### 1 Armstrong Axiom

>   Deduce new functional dependencies by given functional dependencies

<img src="README.assets/image-20221219155935066.png" alt="image-20221219155935066" style="zoom:50%;" />

-   So when we express a relation schema later, we need to give not only **attribute set** but also **functional dependency set**
-   Notice that the argumentation rule should be XU$\rarr$YZ
-   Notice the **usage** of Armstrong Axiom

<img src="README.assets/image-20221219160507273.png" alt="image-20221219160507273" style="zoom:50%;" />

### 2 Armstrong Axiom Deduction

<img src="README.assets/image-20221219160749197.png" alt="image-20221219160749197" style="zoom:50%;" />

-   Lemma 3 indicates the relation between **single attribute functional dependency** and union attributes functional dependency
-   We can easily demonstrate lemma 3 with union rule and decomposition rule

### 3 Attribute Closure

<img src="README.assets/image-20221219162959245.png" alt="image-20221219162959245" style="zoom:50%;" />

<img src="README.assets/image-20221219163547491.png" alt="image-20221219163547491" style="zoom:67%;" />

## Cover and Minimal Cover

### 1 Definition of Cover

<img src="README.assets/image-20221219164542503.png" alt="image-20221219164542503" style="zoom:50%;" />

### 2 Calculate Attribute Closure

<img src="README.assets/image-20221219171228954.png" alt="image-20221219171228954" style="zoom:67%;" />

>   <img src="README.assets/image-20221219171237111.png" alt="image-20221219171237111" style="zoom:50%;" />
>
>   Notice that the **left part** of a functional dependency is also **an attribute set**

>   <img src="README.assets/image-20221219171442708.png" alt="image-20221219171442708" style="zoom:50%;" />

### 3 Property of functional Dependency Set

<img src="README.assets/image-20221219171845708.png" alt="image-20221219171845708" style="zoom:50%;" />

-   Divide the **right part** into **single attribute**

### 4 Minimal Cover

<img src="README.assets/image-20221219183331290.png" alt="image-20221219183331290" style="zoom:50%;" />

-   The third entry means that no attribute in $X$ is redundant

## Summary

<img src="README.assets/image-20221219183921197.png" alt="image-20221219183921197" style="zoom:50%;" />








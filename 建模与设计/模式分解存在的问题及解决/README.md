# Problems of Schema Decomposition

<img src="README.assets/image-20221220114035319.png" alt="image-20221220114035319" style="zoom:50%;" />

<img src="README.assets/image-20221220114216994.png" alt="image-20221220114216994" style="zoom:50%;" />

## Overview of Schema Decomposition

### 1 Definition

<img src="README.assets/image-20221220114652523.png" alt="image-20221220114652523" style="zoom:67%;" />

Aspects to take care of:

<img src="README.assets/image-20221220114806193.png" alt="image-20221220114806193" style="zoom:67%;" />

-   The “join” here is “natural join”

### 2 Equivalence of Data Content

<img src="README.assets/image-20221220115804534.png" alt="image-20221220115804534" style="zoom:50%;" />

-   **Rule 1** indicates that there will be **more information** after joining, which may contain some ***wrong information***
    -   If it does contain wrong information, we call this **lossy join**
-   **Rule 2** means the result of joining after projecting causes the same results when projected again
-   **Rules 3** means that **no more information** will be produced after projecting and joining over and over again

### 3 Equivalence of Data Constraint

<img src="README.assets/image-20221220120944048.png" alt="image-20221220120944048" style="zoom:67%;" />

>   It does lose some constraint

### 4 Schema Decomposition

<img src="README.assets/image-20221220121423390.png" alt="image-20221220121423390" style="zoom:50%;" />

## Lossless Join Decomposition and Its Testing Algorithm

### 1 Definition

<img src="README.assets/image-20221220123943273.png" alt="image-20221220123943273" style="zoom:50%;" />

### 2 Testing Algorithm

1.   Construct an $R_\rho$ Table
2.   Modify $R_\rho$ Table according to **function dependencies**
     -   Lines having same value about X each other
     -   Let the decided Y of the same line also same, with $a_j$ or $b_{ij}$
3.   Try finding a line with all $a_j$s

<img src="README.assets/image-20221220124646034.png" alt="image-20221220124646034" style="zoom:67%;" />

<img src="README.assets/image-20221220130005209.png" alt="image-20221220130005209" style="zoom:60%;" />

>   Example:
>
>   <img src="README.assets/image-20221220130124942.png" alt="image-20221220130124942" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221220130136516.png" alt="image-20221220130136516" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221220130434210.png" alt="image-20221220130434210" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221220130441919.png" alt="image-20221220130441919" style="zoom:50%;" />

<img src="README.assets/image-20221220130615848.png" alt="image-20221220130615848" style="zoom:67%;" />

---

:star:A simple version in **binary decomposition**:

<img src="README.assets/image-20221220130721590.png" alt="image-20221220130721590" style="zoom:50%;" />

-   So if the two decomposed relation is **unrelated**, it must not be lossless decomposition

### 3 Properties of Lossless Decomposition

<img src="README.assets/image-20221220130935422.png" alt="image-20221220130935422" style="zoom:67%;" />

-   Decompose further into more subsets
-   Decompose directly more subsets

## Remaining Function Dependency Decomposition and Its Testing Algorithm

### 1 Definition

<img src="README.assets/image-20221221105624747.png" alt="image-20221221105624747" style="zoom:67%;" />

-   Mind the definition of $\pi_{R_i}(F)$

>   <img src="README.assets/image-20221221105821223.png" alt="image-20221221105821223" style="zoom:67%;" />

### 2 Testing Algorithm

<img src="README.assets/image-20221221110843344.png" alt="image-20221221110843344" style="zoom:67%;" />

>   Example:
>
>   <img src="README.assets/image-20221221111045123.png" alt="image-20221221111045123" style="zoom:67%;" />
>
>   -   So we can easily get the conclusion with human’s eyes

## Decompose Schema into 3NF or BCNF

>   <img src="README.assets/image-20221222104005418.png" alt="image-20221222104005418" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221222105047311.png" alt="image-20221222105047311" style="zoom:50%;" />

### 1 Decompose Schema into BCNF with Lossless Join

<img src="README.assets/image-20221222104351787.png" alt="image-20221222104351787" style="zoom:50%;" />

-   <img src="README.assets/image-20221222104400321.png" alt="image-20221222104400321" style="zoom:67%;" /> 
-   <img src="README.assets/image-20221222104408321.png" alt="image-20221222104408321" style="zoom:67%;" /> 

### 2 Decompose Schema into 3NF Remaining Function Dependency

<img src="README.assets/image-20221222105505139.png" alt="image-20221222105505139" style="zoom:50%;" />

-   <img src="README.assets/image-20221222105527801.png" alt="image-20221222105527801" style="zoom:50%;" /> 

### 3 Decompose Schema with Lossless Join and Remaining Function Dependency

<img src="README.assets/image-20221222110306083.png" alt="image-20221222110306083" style="zoom:50%;" />

-   So long as one schema contains the whole original candidate key 

### 4 Decompose Schema into 4NF with Lossless Join

<img src="README.assets/image-20221222110726579.png" alt="image-20221222110726579" style="zoom:50%;" />

-   the same thought as BCNF

## Join Dependency and Fifth Normal Form

### 1 Join Dependency

<img src="README.assets/image-20221222111405656.png" alt="image-20221222111405656" style="zoom:50%;" />

Relationship between multi-valued dependency and join dependency:

<img src="README.assets/image-20221222111456421.png" alt="image-20221222111456421" style="zoom:50%;" />

Others:

<img src="README.assets/image-20221222111508197.png" alt="image-20221222111508197" style="zoom:50%;" />

### 2 5NF

<img src="README.assets/image-20221222111637894.png" alt="image-20221222111637894" style="zoom:67%;" />

-   Remembering its conception is just OK

## Summary about Database Design

<img src="README.assets/image-20221222112651153.png" alt="image-20221222112651153" style="zoom:50%;" />

<img src="README.assets/image-20221222112923301.png" alt="image-20221222112923301" style="zoom:50%;" />

### 1 Theories about Database Design

<img src="README.assets/image-20221222112821091.png" alt="image-20221222112821091" style="zoom:50%;" />

### 2 Primary Problem about Database Design

<img src="README.assets/image-20221222112855305.png" alt="image-20221222112855305" style="zoom:50%;" />

<img src="README.assets/image-20221222112910873.png" alt="image-20221222112910873" style="zoom:50%;" />

## Brief Summary

<img src="README.assets/image-20221222113010116.png" alt="image-20221222113010116" style="zoom:50%;" />

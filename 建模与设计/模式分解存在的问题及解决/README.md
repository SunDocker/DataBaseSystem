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

## Lossless Decomposition and Its Testing Algorithm

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

A simple version in **binary decomposition**:

<img src="README.assets/image-20221220130721590.png" alt="image-20221220130721590" style="zoom:50%;" />

### 3 Properties of Lossless Decomposition

<img src="README.assets/image-20221220130935422.png" alt="image-20221220130935422" style="zoom:67%;" />

-   Decompose further into more subsets
-   Decompose directly more subsets








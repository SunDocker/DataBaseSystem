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








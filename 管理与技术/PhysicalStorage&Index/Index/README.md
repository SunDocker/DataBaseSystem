# Index

<img src="README.assets/image-20230109120932234.png" alt="image-20230109120932234" style="zoom:67%;" />

## What and Why Index

### 1 Concept of Index

In life:

<img src="README.assets/image-20230109121309246.png" alt="image-20230109121309246" style="zoom:50%;" />

Ordered little scale data

---

In DB:

<img src="README.assets/image-20230109121741278.png" alt="image-20230109121741278" style="zoom:50%;" />

-   Secondary storage structure
-   Based on: Table
-   Function: Quickly search record
-   Constituted: **Index Entries** in *Index File*
    -   Index-field: **different** value in table field
    -   Pointer

### 2 Ordinary Features of Index File

<img src="README.assets/image-20230109132552895.png" alt="image-20230109132552895" style="zoom:50%;" />

<img src="README.assets/image-20230109132954652.png" alt="image-20230109132954652" style="zoom:50%;" />

-   Existence
-   Organization
-   Multiple
-   Little
-   Synchronize

### 3 Evaluation of Index

<img src="README.assets/image-20230109151546761.png" alt="image-20230109151546761" style="zoom:50%;" />

### 4 Distinguish Concepts About Index

<img src="README.assets/image-20230109153431915.png" alt="image-20230109153431915" style="zoom:50%;" />

-   Notice that the three keys below may not **unique**

## Index Creation and Maintaining

### 1 Basic Knowledge

<img src="README.assets/image-20230109185752925.png" alt="image-20230109185752925" style="zoom:50%;" />

-   Primary index
-   DBMS maintain and delete all the indexes automatically

### 2 SQL Creating & Maintaining Index

<img src="README.assets/image-20230109190347329.png" alt="image-20230109190347329" style="zoom:50%;" />

-   It follows X/OPEN standard
-   `unique` is optional. If set, filed value should be no repeating
-   Combination is permitted

### 3 Regard Performance of Index

<img src="README.assets/image-20230109190816468.png" alt="image-20230109190816468" style="zoom:50%;" />

-   Balance **performance optimization** and **cost**
-   **Type** of index

## Dense Index & Sparse Index

### 1 Conceptual Framework

<img src="README.assets/image-20230109202405274.png" alt="image-20230109202405274" style="zoom:50%;" />

-   Every index value
-   All
-   Partial

### 2 Allocating Record by Sparse Index

<img src="README.assets/image-20230109202917982.png" alt="image-20230109202917982" style="zoom:50%;" />

-   Biggest less than
-   Ordered
-   Lighter but slower
-   Primary index: one index entry per block

>   Value excluded in index file may be included in main file

### 3 Allocating Record by Dense Index

>   Value excluded  in index file must be excluded in main file

#### 3.1 On candidate key

<img src="README.assets/image-20230109210605802.png" alt="image-20230109210605802" style="zoom:50%;" />

-   One-to-one correspondence
-   May be not ordered

#### 3.2 On non-candidate key

*Unique index field in index file:*

<img src="README.assets/image-20230109210834948.png" alt="image-20230109210834948" style="zoom:50%;" />

-   One-to-many
-   Ordered

---

*Non-Unique index field in index file:*

<img src="README.assets/image-20230109211034202.png" alt="image-20230109211034202" style="zoom:67%;" />

-   “one-to-one”
-   Not ordered

---

*Unique index field in index file:*

<img src="README.assets/image-20230109211250812.png" alt="image-20230109211250812" style="zoom:50%;" />

-   “one-to-many”
-   Middle layer
-   Ordered

---

*Features summary:*

<img src="README.assets/image-20230109211703313.png" alt="image-20230109211703313" style="zoom:50%;" />

-   Index field in index file is **unique or not**
-   Index field in main file is **ordered or not**

## Primary Index & Secondary Index

### 1 Primary Index

<img src="README.assets/image-20230109212541307.png" alt="image-20230109212541307" style="zoom:50%;" />

-   Anchor record
-   Primary key

### 2 Secondary Index

<img src="README.assets/image-20230109212806209.png" alt="image-20230109212806209" style="zoom:50%;" />

-   Every different value
-   Bucket / Middle Layer
-   Effective

### 3 Primary vs. Secondary

<img src="README.assets/image-20230109212948836.png" alt="image-20230109212948836" style="zoom:50%;" />

-   Block address
-   Record address

Primary Index almost define the organization of primary file, thus can be used to reorganize primary file. But secondary index not.

## Other Types of Index

 


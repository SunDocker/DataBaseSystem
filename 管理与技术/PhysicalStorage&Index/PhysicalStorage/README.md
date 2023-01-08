# Physical Storage

<img src="README.assets/image-20230102141121819.png" alt="image-20230102141121819" style="zoom:67%;" />

## Storage Architecture of Computer System

### 1 Storage and Search About Database

<img src="README.assets/image-20230108100355803.png" alt="image-20230108100355803" style="zoom:50%;" />

-   Index
-   Query Algorithm

### 2 Storage Architecture

<img src="README.assets/image-20230108102544755.png" alt="image-20230108102544755" style="zoom:50%;" />

-   Goals: **high speed, huge volume**
-   How to implement? **Storage architecture**
-   Three types of database in a broad sense
    -   But we always regard main memory as **database buffer**

### 3 Access Time Difference between Storage Levels

<img src="README.assets/image-20230108112543405.png" alt="image-20230108112543405" style="zoom:50%;" />

### 4 OS Managing Disk and Data

<img src="README.assets/image-20230108113028435.png" alt="image-20230108113028435" style="zoom:50%;" />

-   OS manage data by **FILE**
-   R/W disk by **BLOCK**

### 5 OS Managing Memory and Buffer

<img src="README.assets/image-20230108114915027.png" alt="image-20230108114915027" style="zoom:50%;" />

-   R/W memory by **PAGE** 

## Structure and Features of Disk

### 1 Disk and its Volume

<img src="README.assets/image-20230108120011558.png" alt="image-20230108120011558" style="zoom:50%;" />

>   Refer to Operation System

### 2 R/W Disk

<img src="README.assets/image-20230108120237116.png" alt="image-20230108120237116" style="zoom:50%;" />

>   Refer to *Operation System*

-   Key to optimize: I/O count
-   How to decrease disk r/w time?

### 3 Raise Speed and Reliability of Disk

<img src="README.assets/image-20230108121726548.png" alt="image-20230108121726548" style="zoom:50%;" />

-   **Parallel**
    -   Divide:
        -   **Bit**
        -   **Block**
-   **Reliable**
    -   Verify
        -   Between **blocks**
        -   Between **disks**

According to tech above, we have **RAIDs** below:

-   RAID0
-   RAID1
-   RAID2
-   RAID3
-   RAID4
-   RAID5

>   Refer to *Composition Principle of Computer*

## Basic Thoughts of DBMS Storage and Query

### 1 Map of Data Storage

<img src="README.assets/image-20230108142438506.png" alt="image-20230108142438506" style="zoom:50%;" />

Three maps:

-   Map from record to block
-   Map from page to block
-   Map from record to page

>   Index file will store this information

Three managements:

-   Disk: manage itself

-   Memory: manage itself and call disk interface

-   File & Index (Logic): manage itself call memory and disk interface

    >   **Main file** and **index file** both need to be stored

And then we can implement query algorithm

### 2 Components of DBMS / Framework

>   Functions of DBMS

<img src="README.assets/image-20230108143805639.png" alt="image-20230108143805639" style="zoom:50%;" />

Four levels:

-   Storage: disk block

-   Buffer: memory page

-   Record & Index: table & schema & data control information

    -   table: DML
    -   schema: DDL
    -   data control information: DCL

    >   **Main file** and **index file** both need to be stored

-   Application: DML & DDL & DCL

    -   Engine and Compiler
    -   Algorithm

## Map between record and block

>   **Index file** will store map information

### 1 Map between Concepts

<img src="README.assets/image-20230108170647279.png" alt="image-20230108170647279" style="zoom:50%;" />

Operation: File to Block

DBMS: Table to Block

### 2 Distinguish records and attributes

<img src="README.assets/image-20230108171538284.png" alt="image-20230108171538284" style="zoom:50%;" />

-   Fixed-length record

-   Variable-length record: sign or pointer

    >   Situation where **free space is insufficient** may occur

### 3 Record vs Disk

<img src="README.assets/image-20230108172053509.png" alt="image-20230108172053509" style="zoom:50%;" />

-   Cross block storage: pointer, waste access time, save space
-   Not cross block storage: waste space, increase speed by parallel access

### 4 Table vs Disk

<img src="README.assets/image-20230108172108897.png" alt="image-20230108172108897" style="zoom:50%;" />

-   Four allocating method

Index is like FAT in OS, but there can be various indexes

## File Organization of DB

### 1 Data Organization and Access Method

<img src="README.assets/image-20230108175746686.png" alt="image-20230108175746686" style="zoom:50%;" />

-   Like data structure and algorithm

### 2 Heap File Organization

Two storage strategy:

<img src="README.assets/image-20230108180540220.png" alt="image-20230108180540220" style="zoom:50%;" />

---

Reorganization:

<img src="README.assets/image-20230108181007248.png" alt="image-20230108181007248" style="zoom:50%;" />

Implemented by DBA when realizing database’s performance is decreasing

### 3 Sequential File Organization

Ordering filed:

<img src="README.assets/image-20230108181240275.png" alt="image-20230108181240275" style="zoom:50%;" />

---

Insert:

<img src="README.assets/image-20230108181344469.png" alt="image-20230108181344469" style="zoom:50%;" />

Move data in a large scale

---

Overflow:

<img src="README.assets/image-20230108181706527.png" alt="image-20230108181706527" style="zoom:50%;" />

Reorganization is implemented by DBA when realizing database’s performance is decreasing

### 4 Hash File Organization

<img src="README.assets/image-20230108195555635.png" alt="image-20230108195555635" style="zoom:50%;" />

Hash field

---

<img src="README.assets/image-20230108195638096.png" alt="image-20230108195638096" style="zoom:50%;" />

Sequential search

---

<img src="README.assets/image-20230108195755677.png" alt="image-20230108195755677" style="zoom:50%;" />

Overflow bucket

---

### 5 Cluster File Organization

<img src="README.assets/image-20230108200245791.png" alt="image-20230108200245791" style="zoom:50%;" />

### 6 Brief Summary

<img src="README.assets/image-20230108200936028.png" alt="image-20230108200936028" style="zoom:50%;" />

-   Require high update: heap or hash
-   Require high query: sequential or clustering
-   If performance decreasing, reorganize
-   Different file organization, different access algorithm

## Overview

<img src="README.assets/image-20230108212008161.png" alt="image-20230108212008161" style="zoom:50%;" />

-   **Index file** will store map information
-   Different **file organization**, different access algorithm
-   Reorganize


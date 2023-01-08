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

Three managements:

-   Disk: manage itself
-   Memory: manage itself and call disk interface
-   File / Index (Logic): manage itself call memory and disk interface

And then we can implement query algorithm

### 2 Components of DBMS / Framework

>   Functions of DBMS

<img src="README.assets/image-20230108143805639.png" alt="image-20230108143805639" style="zoom:50%;" />

Four levels:

-   Storage: disk block
-   Buffer: memory page
-   Record / Index: table & schema & data control information
    -   table: DML
    -   schema: DDL
    -   data control information: DCL
-   Application: DML & DDL & DCL
    -   Engine and Compiler
    -   Algorithm


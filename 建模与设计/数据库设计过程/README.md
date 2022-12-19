# Process of Database Design

<img src="README.assets/image-20221218220346804.png" alt="image-20221218220346804" style="zoom:50%;" />

## Overview

1.   Demand analysis
2.   Conceptual database design 
3.   Logical database design 
4.   Physical database design

<img src="README.assets/image-20221218220647386.png" alt="image-20221218220647386" style="zoom:67%;" />

<img src="README.assets/image-20221218220659384.png" alt="image-20221218220659384" style="zoom:67%;" />

<img src="README.assets/image-20221218220715136.png" alt="image-20221218220715136" style="zoom:50%;" />

<img src="README.assets/image-20221218221049549.png" alt="image-20221218221049549" style="zoom:50%;" />

<img src="README.assets/image-20221218221100904.png" alt="image-20221218221100904" style="zoom:50%;" />

<img src="README.assets/image-20221218221118916.png" alt="image-20221218221118916" style="zoom:50%;" />

## Demand Analysis

### 1 Overview

<img src="README.assets/image-20221218221450953.png" alt="image-20221218221450953" style="zoom:50%;" />

### 2 Source List and Attribute List

<img src="README.assets/image-20221218221649994.png" alt="image-20221218221649994" style="zoom:50%;" />

<img src="README.assets/image-20221218221926332.png" alt="image-20221218221926332" style="zoom:50%;" />

<img src="README.assets/image-20221218221938349.png" alt="image-20221218221938349" style="zoom:50%;" />

### 3 Brief Summary

<img src="README.assets/image-20221218222226479.png" alt="image-20221218222226479" style="zoom:50%;" />

## Conceptual Database Design

### 1 Overview

<img src="README.assets/image-20221218222517419.png" alt="image-20221218222517419" style="zoom:67%;" />

<img src="README.assets/image-20221218222730745.png" alt="image-20221218222730745" style="zoom:50%;" />

-   Discover the **nature relationship**
-   Helpful for **comprehending demand**

### 2 Two Design Thoughts of Conceptual Database

<img src="README.assets/image-20221218222952169.png" alt="image-20221218222952169" style="zoom:50%;" />

<img src="README.assets/image-20221218223059137.png" alt="image-20221218223059137" style="zoom:50%;" />

<img src="README.assets/image-20221218223107806.png" alt="image-20221218223107806" style="zoom:50%;" />

<img src="README.assets/image-20221218223357598.png" alt="image-20221218223357598" style="zoom:50%;" />

### 3 Possible Conflicts in Database Design

<img src="README.assets/image-20221218223317407.png" alt="image-20221218223317407" style="zoom:67%;" />

### 4 Outcomes

E-R Diagram / IDEF1x Diagram: 

<img src="README.assets/image-20221218223557611.png" alt="image-20221218223557611" style="zoom:50%;" />

-   Key-level Diagrams are most commonly-used

---

Entity List:

<img src="README.assets/image-20221218223936299.png" alt="image-20221218223936299" style="zoom:50%;" />

---

Entity Definition Table:

<img src="README.assets/image-20221218224003355.png" alt="image-20221218224003355" style="zoom:50%;" />

---

Entity-Relationship Matrix:

<img src="README.assets/image-20221218224050821.png" alt="image-20221218224050821" style="zoom:50%;" />

---

Entity-Attribute Matrix:

<img src="README.assets/image-20221218224154569.png" alt="image-20221218224154569" style="zoom:50%;" />

### 5 Brief Summary

<img src="README.assets/image-20221218224826424.png" alt="image-20221218224826424" style="zoom:50%;" />

## Logical Database Design

### 1 Overview

<img src="README.assets/image-20221219095917645.png" alt="image-20221219095917645" style="zoom:50%;" />

### 2 Transforming from E-R Diagram to Relation Schema

#### 2.1 Tow Ports:

<img src="README.assets/image-20221219100355041.png" alt="image-20221219100355041" style="zoom:50%;" />

---

#### 2.2 Basic Transformation:

<img src="README.assets/image-20221219100542503.png" alt="image-20221219100542503" style="zoom:50%;" />

---

#### 2.3 Composite and Multi-valued Attribute:

<img src="README.assets/image-20221219100641333.png" alt="image-20221219100641333" style="zoom:50%;" />

<img src="README.assets/image-20221219101148087.png" alt="image-20221219101148087" style="zoom:50%;" />

---

#### 2.4 Relationship:

1:1 partial or full participation

<img src="README.assets/image-20221219102402919.png" alt="image-20221219102402919" style="zoom:50%;" />

1:m

<img src="README.assets/image-20221219102531314.png" alt="image-20221219102531314" style="zoom:50%;" />

m:n

<img src="README.assets/image-20221219103127809.png" alt="image-20221219103127809" style="zoom:50%;" />

---

#### 2.5 Identifier-dependent entities:

<img src="README.assets/image-20221219103430861.png" alt="image-20221219103430861" style="zoom:50%;" />

---

#### 2.6 Specialize and Generalize:

<img src="README.assets/image-20221219104052182.png" alt="image-20221219104052182" style="zoom:50%;" />

-   Just **inherit primary key** in schema, rather than all attributes (if incomplete)

Complete or Incomplete:

<img src="README.assets/image-20221219104255307.png" alt="image-20221219104255307" style="zoom:50%;" />

<img src="README.assets/image-20221219104447999.png" alt="image-20221219104447999" style="zoom:50%;" />

---

#### 2.7 Multi-Relationship:

<img src="README.assets/image-20221219104947043.png" alt="image-20221219104947043" style="zoom:50%;" />

-   Type 1 transformation doesn’t allow partial participation
-   Type 2 transformation allows partial participation

>   <img src="README.assets/image-20221219105329587.png" alt="image-20221219105329587" style="zoom:50%;" />

#### 2.8 IDEF1x

<img src="README.assets/image-20221219105500791.png" alt="image-20221219105500791" style="zoom:50%;" />

### 3 Problems

#### 3.1 Controlled Redundancy and Uncontrolled Redundancy:

<img src="README.assets/image-20221219105838012.png" alt="image-20221219105838012" style="zoom:50%;" />

<img src="README.assets/image-20221219105910562.png" alt="image-20221219105910562" style="zoom:50%;" />

#### 3.2 Insert and Delete Exceptions

<img src="README.assets/image-20221219110014337.png" alt="image-20221219110014337" style="zoom:50%;" />

>   <img src="README.assets/image-20221219110050666.png" alt="image-20221219110050666" style="zoom:50%;" />

#### 3.3 How to Avoid

<img src="README.assets/image-20221219110241705.png" alt="image-20221219110241705" style="zoom:50%;" />

#### 3.4 :star:Normative Database Design

<img src="README.assets/image-20221219110448353.png" alt="image-20221219110448353" style="zoom:50%;" />

According to **Data Dependence**, judge the **Relationship Normal Form**, then apply the **Schema Decomposition**

### 4 Brief Summary

<img src="README.assets/image-20221219111301683.png" alt="image-20221219111301683" style="zoom:50%;" />

## Physical database design

### 1 Overview

<img src="README.assets/image-20221219120006375.png" alt="image-20221219120006375" style="zoom:50%;" />

<img src="README.assets/image-20221219120015406.png" alt="image-20221219120015406" style="zoom:50%;" />

Physical database design is related to **the concrete database system**

### 2 Brief Summary

<img src="README.assets/image-20221219120357389.png" alt="image-20221219120357389" style="zoom:50%;" />

## Summary

<img src="README.assets/image-20221219132636144.png" alt="image-20221219132636144" style="zoom:50%;" />




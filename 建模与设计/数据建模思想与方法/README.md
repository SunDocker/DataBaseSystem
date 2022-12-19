# Data Modeling: Thoughts and Ways

>   <img src="README.assets/image-20221218094553642.png" alt="image-20221218094553642" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221218094604058.png" alt="image-20221218094604058" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221218094814092.png" alt="image-20221218094814092" style="zoom:67%;" />

## Overview

### 1 Why Data Modeling and Database Designing are necessary

<img src="README.assets/image-20221218094946459.png" alt="image-20221218094946459" style="zoom:50%;" />

-   Understand clients’ demand
-   The ***Comprehension and Expression*** of demand matters !

---

Comprehension of Demand

-   Comprehension of **Data** Demand
-   Comprehension of **Processing Rules** Demand

<img src="README.assets/image-20221218095257530.png" alt="image-20221218095257530" style="zoom:50%;" />

-   Which is better with the accumulation clients’ demand

    >   **Data demand** is even more essential

### 2 Data Model and Conceptual Model

<img src="README.assets/image-20221218100131579.png" alt="image-20221218100131579" style="zoom:67%;" />

<img src="README.assets/image-20221218100142518.png" alt="image-20221218100142518" style="zoom:67%;" />

-   Pay attention to the **Conceptual/Information World**
    -   where we have *conceptual model*
    -   notice the <u>levels of **abstraction**</u>
-   ABSTRACTION: It’s worth noticing that the computer world also contains tow levels of **abstraction**, *logic level to physical level*
    -   **<u>Data modeling</u>**: abstraction of **conceptual level**
    -   **<u>Database design</u>**: abstraction of **implemented level**

>   Example1:
>
>   <img src="README.assets/image-20221218100941880.png" alt="image-20221218100941880" style="zoom:67%;" />
>
>   -   It’s **difficult** to **directly abstract** the real world into computer world
>   -   We can make it with the help of ***conceptual model***
>
>   Example2:
>
>   <img src="README.assets/image-20221218101256649.png" alt="image-20221218101256649" style="zoom:50%;" />

### 3 How to make abstraction of conceptual level

What’s abstraction:

-   ***Comprehend***
-   ***Distinguish***
-   ***Name***
-   ***Express***

<img src="README.assets/image-20221218103545286.png" alt="image-20221218103545286" style="zoom:50%;" />

## Entity-Relationship Model

### 1 The Thought of Data Modeling

<img src="README.assets/image-20221218103758447.png" alt="image-20221218103758447" style="zoom:50%;" />

-   E-R Model’s basic viewpoint
-   tow aspects:
    -   thought of modeling
    -   method of expression

### 2 Conceptual Framework

<img src="README.assets/image-20221218104117894.png" alt="image-20221218104117894" style="zoom:67%;" />

-   Entity
-   Attribute
-   Relationship
-   Keyword

>   <img src="README.assets/image-20221218104128372.png" alt="image-20221218104128372" style="zoom:67%;" />

### 3 Entity and Attribute

>   The Meaning and Description of Entity 

<img src="README.assets/image-20221218104756271.png" alt="image-20221218104756271" style="zoom:50%;" />

-   Entity: the pattern of entity
-   Instance: the value of entity

---

<img src="README.assets/image-20221218104942066.png" alt="image-20221218104942066" style="zoom:50%;" />

-   Entity
-   Attribute: description of entity
-   **At least keyword** to describe entity

---

Classification of Attribute

<img src="README.assets/image-20221218105140891.png" alt="image-20221218105140891" style="zoom:50%;" />

-   Single attribute
-   Composite attribute
-   Value
    -   Single-valued attribute
    -   Multi-valued attribute
-   Nullability
    -   Nullable attribute
    -   Non-null attribute
-   Exporting
    -   Exported attribute
    -   Non-exported attribute

---

Keyword:

<img src="README.assets/image-20221218105855386.png" alt="image-20221218105855386" style="zoom:50%;" />

### 4 Relationship, Degree and Cardinality

<img src="README.assets/image-20221218110125649.png" alt="image-20221218110125649" style="zoom:67%;" />

-   Actually, it’s the relation between **instances** of entities
-   Relationship also needs ***names*** to be distinguished, and may also need ***attributes***

---

Classification of relationship

-   Degree of Relationship
    -   Unary Relationship
    -   Binary Relationship
    -   Ternary Relationship
    -   Quaternary Relationship
-   Notice: the number of **entities**, not instances

<img src="README.assets/image-20221218110816779.png" alt="image-20221218110816779" style="zoom:50%;" /><img src="README.assets/image-20221218110845887.png" alt="image-20221218110845887" style="zoom:50%;" /><img src="README.assets/image-20221218110921859.png" alt="image-20221218110921859" style="zoom:50%;" />

---

***Role***, used for distinguishing the function of instances in a **relationship**

<img src="README.assets/image-20221218111426510.png" alt="image-20221218111426510" style="zoom:67%;" />

<img src="README.assets/image-20221218111501398.png" alt="image-20221218111501398" style="zoom:67%;" />

-   We may need mark some words beside the line
-   Commonly used in **unary relationship**

---

Cardinalities of binary relationship:

<img src="README.assets/image-20221218112335806.png" alt="image-20221218112335806" style="zoom:50%;" />

<img src="README.assets/image-20221218112440610.png" alt="image-20221218112440610" style="zoom:50%;" />

-   Why to distinguish this? It’s related to save the **design** of relationship

    >   Data Design

<img src="README.assets/image-20221218112554501.png" alt="image-20221218112554501" style="zoom:50%;" />

-   For m:m, we need an **intermediate table**
-   For 1:m, we can only add a foreign key

---

Minimum cardinality and maximum cardinality

<img src="README.assets/image-20221218113433655.png" alt="image-20221218113433655" style="zoom:67%;" />

-   Why to distinguish this? It’s related to the nullability, also a part of saving the **design** of relationship

<img src="README.assets/image-20221218113648829.png" alt="image-20221218113648829" style="zoom:50%;" />

<img src="README.assets/image-20221218113659816.png" alt="image-20221218113659816" style="zoom:67%;" />

-   how to interpret the null value

## Graphic Expressions of E-R Model

### 1 Chen Method

#### 1.1 Conceptual Framework

<img src="README.assets/image-20221218114457417.png" alt="image-20221218114457417" style="zoom:50%;" />

-   Entity

-   Attribute

    -   Keyword

        >   Composite keywords are labeled by a same number. Notice that the number is just a label, not means the amount

    -   Composite Attribute: straight line

-   Relationship

-   Connectivity: straight line

    >   Which means the **keyword** of entity will be **counted as an attribute of relationship**. So do not draw a straight line casually

---

Expression of Cardinality

<img src="README.assets/image-20221218114648532.png" alt="image-20221218114648532" style="zoom:50%;" />

<img src="README.assets/image-20221218115033327.png" alt="image-20221218115033327" style="zoom:50%;" />

-   With arrow: single end
-   Without arrow: multiple end
-   Partial participation Relationship
-   All participation Relationship
-   number

#### 1.2 Attributes, Role and Cardinalities in E-R Model

<img src="README.assets/image-20221218115614539.png" alt="image-20221218115614539" style="zoom:50%;" />

<img src="README.assets/image-20221218120305313.png" alt="image-20221218120305313" style="zoom:50%;" />

---

Multiple, Multi-valued, exported attribute:

<img src="README.assets/image-20221218120736214.png" alt="image-20221218120736214" style="zoom:50%;" />

<img src="README.assets/image-20221218120827598.png" alt="image-20221218120827598" style="zoom:50%;" />

---

Role in relationship

<img src="README.assets/image-20221218121406205.png" alt="image-20221218121406205" style="zoom:50%;" />

-   Some words added next to the line

---

Cardinalities:

<img src="README.assets/image-20221218121609101.png" alt="image-20221218121609101" style="zoom:67%;" />

-   It’s necessary to estimate which one fits demand better

#### 1.3 Cases of Chen Method

demands:

<img src="README.assets/image-20221218170212858.png" alt="image-20221218170212858" style="zoom:67%;" />

1.   Comprehend demands, discover **entities**

     >   which can be led by **“a” or some quantifier**

2.   Describe every entity with **attributes**

     <img src="README.assets/image-20221218180929661.png" alt="image-20221218180929661" style="zoom:50%;" />

     >   Some “attributes” can be reflected by **relationships**

3.   Confirm **keywords**

     <img src="README.assets/image-20221218181001591.png" alt="image-20221218181001591" style="zoom:50%;" />

4.   Analyze the **relationships** (and their **attributes**) between entities

     <img src="README.assets/image-20221218181536695.png" alt="image-20221218181536695" style="zoom:50%;" />

     >   It’s better not to have **isolated entities**

     -   Don’t forget the **cardinalities**

5.   Check whether **all the demands are covered**

     <img src="README.assets/image-20221218181711352.png" alt="image-20221218181711352" style="zoom:50%;" />

     How to estimate the correctness of an E-R graph with Chen Method ?

     -   Content: **semantic** requirement
     -   Form: obeying the **rules**

### 2 Crow’s Foot Method

#### 2.1 Entity and Attribute

<img src="README.assets/image-20221218182248674.png" alt="image-20221218182248674" style="zoom:50%;" />

>   The circles in Chen Method occupy too much space

#### 2.2 Relationship and Cardinality

<img src="README.assets/image-20221218182537437.png" alt="image-20221218182537437" style="zoom:67%;" />

>   <img src="README.assets/image-20221218182604843.png" alt="image-20221218182604843" style="zoom:50%;" />

<img src="README.assets/image-20221218182557477.png" alt="image-20221218182557477" style="zoom:50%;" />

>   <img src="README.assets/image-20221218182642286.png" alt="image-20221218182642286" style="zoom:50%;" />

>   BUT I don’t know how to add attributes to relationship in Crow’s Foot Method

#### 2.3 Examples

<img src="README.assets/image-20221218182819660.png" alt="image-20221218182819660" style="zoom:50%;" /><img src="README.assets/image-20221218182845858.png" alt="image-20221218182845858" style="zoom:50%;" />

Notice: <u>Express the ***business rules***</u>

---

<img src="README.assets/image-20221218183110259.png" alt="image-20221218183110259" style="zoom:67%;" />

Partial participation and Full participation

---

Unary relationship and words marked

<img src="README.assets/image-20221218183246006.png" alt="image-20221218183246006" style="zoom:60%;" />

#### 2.4 Cases of Crow’s Foot Method

<img src="README.assets/image-20221218183538188.png" alt="image-20221218183538188" style="zoom:50%;" />

Still the tow aspects:

-   Covering all the demands
-   Obey the rules of Crow’s foot Method

## Abstraction in Database Design

### 1 Information

<img src="README.assets/image-20221218184641483.png" alt="image-20221218184641483" style="zoom:67%;" />

<img src="README.assets/image-20221218184657940.png" alt="image-20221218184657940" style="zoom:50%;" />

-   Information and Relationship
-   What information is necessary for us to describe

### 2 Three Words

<img src="README.assets/image-20221218184808275.png" alt="image-20221218184808275" style="zoom:67%;" />

### 3 Type and Value

<img src="README.assets/image-20221218184927603.png" alt="image-20221218184927603" style="zoom:67%;" />

<img src="README.assets/image-20221218185004924.png" alt="image-20221218185004924" style="zoom:60%;" />

>   <img src="README.assets/image-20221218185212983.png" alt="image-20221218185212983" style="zoom:67%;" />

### 4 Levels of Abstraction

<img src="README.assets/image-20221218185316796.png" alt="image-20221218185316796" style="zoom:67%;" />

### 5 Data Model and Conceptual Data Model

<img src="README.assets/image-20221218185701285.png" alt="image-20221218185701285" style="zoom:50%;" />

-   Unitive conception and expression
-   Union for communication and sharing

<img src="README.assets/image-20221218185841813.png" alt="image-20221218185841813" style="zoom:67%;" />

### 6 How to Abstraction

<img src="README.assets/image-20221218190226362.png" alt="image-20221218190226362" style="zoom:50%;" />

<img src="README.assets/image-20221218190515988.png" alt="image-20221218190515988" style="zoom:67%;" />

### 7 Methodology

<img src="README.assets/image-20221218190504819.png" alt="image-20221218190504819" style="zoom:50%;" />

### 8 Levels of Modeling

<img src="README.assets/image-20221218191026316.png" alt="image-20221218191026316" style="zoom:60%;" />

<img src="README.assets/image-20221218191342250.png" alt="image-20221218191342250" style="zoom:50%;" />

-   Abstraction: comprehend, distinguish, name, express
-   Levels:
    -   Methodology and methodology mpplication
    -   Model and meta model
-   Three worlds

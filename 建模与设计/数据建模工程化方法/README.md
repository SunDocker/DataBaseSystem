# Data Modeling: Engineering Methods and Cases

## IDEF1x: Conceptual Framework

### 1 Origin

<img src="README.assets/image-20221218200457443.png" alt="image-20221218200457443" style="zoom:50%;" />

### 2 Entity, Relationship, Attribute/Key

<img src="README.assets/image-20221218200710754.png" alt="image-20221218200710754" style="zoom:50%;" />

### 3 Example

<img src="README.assets/image-20221218200800742.png" alt="image-20221218200800742" style="zoom:50%;" />

## IDEF1x: Tow Kinds of Entities

<img src="README.assets/image-20221218202357104.png" alt="image-20221218202357104" style="zoom:67%;" />

### 1 Identifier-Independent Entity

<img src="README.assets/image-20221218202630461.png" alt="image-20221218202630461" style="zoom:50%;" />

-   **Primary key** is pivotal, it must be the entity’s own attribute
-   Graphic expression: rectangle

### 2 Identifier-Dependent Entity

<img src="README.assets/image-20221218203150050.png" alt="image-20221218203150050" style="zoom:50%;" />

<img src="README.assets/image-20221218203920916.png" alt="image-20221218203920916" style="zoom:50%;" />

-   **Extending key** from another entity as **a part of primary key**
-   So there is a **inclusion relation**: the **primary key of identifier-dependent entity** includes a **foreign key**, the **primary key of an identifier-independent entity**
-   Graphic expression: rounded rectangle

### 3 Rules about Entity

<img src="README.assets/image-20221218204543320.png" alt="image-20221218204543320" style="zoom:50%;" />

-   Rectangle
-   name
-   FK
-   Dependent

<img src="README.assets/image-20221218205654046.png" alt="image-20221218205654046" style="zoom:50%;" />

### 4 Attributes and Primary & Alternate & Foreign Key

<img src="README.assets/image-20221218205959437.png" alt="image-20221218205959437" style="zoom:50%;" />

-   Just write in the grid below, and add **brackets** to indicate the AK or FK, or no brackets

<img src="README.assets/image-20221218210144834.png" alt="image-20221218210144834" style="zoom:50%;" />

### 5 Rules about Key

<img src="README.assets/image-20221218210011745.png" alt="image-20221218210011745" style="zoom:50%;" />

<img src="README.assets/image-20221218210131361.png" alt="image-20221218210131361" style="zoom:50%;" />

<img src="README.assets/image-20221218210154366.png" alt="image-20221218210154366" style="zoom:50%;" />

-   Notice the red ones 
-   Read these rules and summarize them in the post

## IDEF1x: Connection Relationship - Identifying and Non-Identifying

<img src="README.assets/image-20221218211457842.png" alt="image-20221218211457842" style="zoom:50%;" />

-   Connection Relationship is 1:1 or 1:m

### 1 Identifying Connection Relationship

<img src="README.assets/image-20221218211659771.png" alt="image-20221218211659771" style="zoom:50%;" />

-   1:1 or 1:m
-   Between identifier-independent entity and identifier-dependent entity
-   Extend primary key **into primary key**

### 2 Non-Identifying Connection Relationship

<img src="README.assets/image-20221218211840060.png" alt="image-20221218211840060" style="zoom:50%;" />

-   1:1 or 1:m
-   Between two identifier-independent entities
-   Extend primary key **into simple attributes**

### 3 Rules

<img src="README.assets/image-20221218212037182.png" alt="image-20221218212037182" style="zoom:50%;" />

<img src="README.assets/image-20221218212305671.png" alt="image-20221218212305671" style="zoom:50%;" />

## IDEF1x: Categorization Relationship

<img src="README.assets/image-20221218213452739.png" alt="image-20221218213452739" style="zoom:50%;" />

### 1 Definition

<img src="README.assets/image-20221218213536776.png" alt="image-20221218213536776" style="zoom:50%;" />

<img src="README.assets/image-20221218213736437.png" alt="image-20221218213736437" style="zoom:50%;" />

>   Just like class and abstract class

-   There will be a **discriminator attribute** in the categorize relationship, used for categorizing the entities, which will be marked next to the lines
-   **Categorize relationship** is not just categorization, there must be **attribute(s) to distinguish** sub entities, also called **special attributes**
-   Categorization entities have the same primary key as super entity

### 2 Specialization and Generalization

<img src="README.assets/image-20221218214255559.png" alt="image-20221218214255559" style="zoom:50%;" />

>   <img src="README.assets/image-20221218214306895.png" alt="image-20221218214306895" style="zoom:67%;" />

---

<img src="README.assets/image-20221218214601000.png" alt="image-20221218214601000" style="zoom:50%;" />

---

Expression of Specialization and Generalization

<img src="README.assets/image-20221218214712251.png" alt="image-20221218214712251" style="zoom:50%;" />

<img src="README.assets/image-20221218214841682.png" alt="image-20221218214841682" style="zoom:50%;" />

---

Inheritance of Attribute:

<img src="README.assets/image-20221218214929572.png" alt="image-20221218214929572" style="zoom:67%;" />

### 3 Perfect Categorization Relationship and Imperfect Categorization Relationship

<img src="README.assets/image-20221218215125612.png" alt="image-20221218215125612" style="zoom:50%;" />

### 4 Rules

<img src="README.assets/image-20221218215438987.png" alt="image-20221218215438987" style="zoom:50%;" />

<img src="README.assets/image-20221218215543156.png" alt="image-20221218215543156" style="zoom:50%;" />

## IDEF1x: Non-Specific Relationship

<img src="README.assets/image-20221218212437508.png" alt="image-20221218212437508" style="zoom:50%;" />

-   Non-Specific Relationship is m:n

### 1 Definition

<img src="README.assets/image-20221218212647109.png" alt="image-20221218212647109" style="zoom:67%;" />

>   <img src="README.assets/image-20221218212655402.png" alt="image-20221218212655402" style="zoom:50%;" />
>
>   These are all wrong !

### 2 Intersection/Associative Entity

We need transform m:n to 1:m

<img src="README.assets/image-20221218212852631.png" alt="image-20221218212852631" style="zoom:50%;" />

So the relationship itself **doesn’t need any attributes**, we may **only focus on the entities**, which may **contain relationships**

>   Examples:
>
>   <img src="README.assets/image-20221218213031886.png" alt="image-20221218213031886" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221218213211580.png" alt="image-20221218213211580" style="zoom:50%;" />

### 4 Rules

<img src="README.assets/image-20221218213402954.png" alt="image-20221218213402954" style="zoom:50%;" />
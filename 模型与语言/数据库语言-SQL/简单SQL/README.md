# 简单SQL

## SQL概述

>   总览：
>
>   <img src="README.assets/image-20221110140953456.png" alt="image-20221110140953456" style="zoom:67%;" />
>
>   难点：
>
>   <img src="README.assets/image-20221110141021395.png" alt="image-20221110141021395" style="zoom:67%;" />

### 1 SQL的提出与发展

<img src="README.assets/image-20221110141501395.png" alt="image-20221110141501395" style="zoom:67%;" />

<img src="README.assets/image-20221110141524741.png" alt="image-20221110141524741" style="zoom:67%;" />

<img src="README.assets/image-20221110141613289.png" alt="image-20221110141613289" style="zoom:67%;" />

### 2 SQL功能概述

<img src="README.assets/image-20221110141752371.png" alt="image-20221110141752371" style="zoom:67%;" />

-   重点：需求、表达

## SQL建立数据库

<img src="README.assets/image-20221110142458693.png" alt="image-20221110142458693" style="zoom:67%;" />

<img src="README.assets/image-20221110143616620.png" alt="image-20221110143616620" style="zoom:67%;" />

DDL+DML

>   课程使用的表：
>
>   <img src="README.assets/image-20221110142256505.png" alt="image-20221110142256505" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221110142322254.png" alt="image-20221110142322254" style="zoom:67%;" />

### 1 SQL-DDL

<img src="README.assets/image-20221110142543170.png" alt="image-20221110142543170" style="zoom:67%;" />

>   其他可行的定义操作：
>
>   <img src="README.assets/image-20221110142550755.png" alt="image-20221110142550755" style="zoom:67%;" />
>
>   DDL的使用者：
>
>   <img src="README.assets/image-20221110142620370.png" alt="image-20221110142620370" style="zoom:67%;" />

#### 1.1 Create Database

<img src="README.assets/image-20221110142732615.png" alt="image-20221110142732615" style="zoom:67%;" />

>   举例：
>
>   <img src="README.assets/image-20221110142744413.png" alt="image-20221110142744413" style="zoom:50%;" />

#### 1.2 Create Table

 <img src="README.assets/image-20221110143019405.png" alt="image-20221110143019405" style="zoom:67%;" />

-    <img src="README.assets/image-20221110143029673.png" alt="image-20221110143029673" style="zoom:67%;" />

 <img src="README.assets/image-20221110143132135.png" alt="image-20221110143132135" style="zoom:67%;" />

-    <img src="README.assets/image-20221110143147593.png" alt="image-20221110143147593" style="zoom:50%;" />

>   举例：
>
>   -    <img src="README.assets/image-20221110143408341.png" alt="image-20221110143408341" style="zoom:67%;" />
>
>        <img src="README.assets/image-20221110143426758.png" alt="image-20221110143426758" style="zoom:67%;" />
>
>   -    <img src="README.assets/image-20221110143444196.png" alt="image-20221110143444196" style="zoom:67%;" />
>
>        <img src="README.assets/image-20221110143502644.png" alt="image-20221110143502644" style="zoom:67%;" />
>
>   >    <img src="README.assets/image-20221110143516591.png" alt="image-20221110143516591" style="zoom:67%;" /><img src="README.assets/image-20221110143528543.png" alt="image-20221110143528543" style="zoom:67%;" />

### 2 SQL-DML

<img src="README.assets/image-20221110143737668.png" alt="image-20221110143737668" style="zoom:67%;" />

-   这里主要讲简单的Insert

    >   Insert可以结合Select进行复杂插入

-   DML的使用者：

     <img src="README.assets/image-20221110143818752.png" alt="image-20221110143818752" style="zoom:80%;" />

#### 2.1 INSERT INTO

 <img src="README.assets/image-20221110143858435.png" alt="image-20221110143858435" style="zoom:67%;" />

 <img src="README.assets/image-20221110143930792.png" alt="image-20221110143930792" style="zoom:67%;" />

>   举例：
>
>    <img src="README.assets/image-20221110144020039.png" alt="image-20221110144020039" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144033622.png" alt="image-20221110144033622" style="zoom:80%;" />
>
>    <img src="README.assets/image-20221110144056716.png" alt="image-20221110144056716" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144109554.png" alt="image-20221110144109554" style="zoom:67%;" />

## SQL查询数据库

### 1 单表查询

#### 1.1 单表简单查询

 <img src="README.assets/image-20221110144314122.png" alt="image-20221110144314122" style="zoom:67%;" />

-   语义：<img src="README.assets/image-20221110144343907.png" alt="image-20221110144343907" style="zoom:67%;" />
-   数学描述：<img src="README.assets/image-20221110144358386.png" alt="image-20221110144358386" style="zoom:67%;" />
-   子句：<img src="README.assets/image-20221110144416217.png" alt="image-20221110144416217" style="zoom:70%;" />
    -   `select`子句
    -   `from`子句
    -   `where`子句

>   举例：
>
>   <img src="README.assets/image-20221110144543385.png" alt="image-20221110144543385" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144439036.png" alt="image-20221110144439036" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144512715.png" alt="image-20221110144512715" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144524175.png" alt="image-20221110144524175" style="zoom:67%;" />

检索条件/`where`子句的书写：

 <img src="README.assets/image-20221110144733464.png" alt="image-20221110144733464" style="zoom:67%;" />

>    举例：
>
>   <img src="README.assets/image-20221110144807906.png" alt="image-20221110144807906" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144748147.png" alt="image-20221110144748147" style="zoom:50%;" />
>
>   ---
>
>   <img src="README.assets/image-20221110144914809.png" alt="image-20221110144914809" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144901835.png" alt="image-20221110144901835" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110144927908.png" alt="image-20221110144927908" style="zoom:67%;" />
>
>   >   需要用**表的自连接**解决

#### 1.2 单表去重查询

SELECT DISTINCT FROM-WHERE

 <img src="README.assets/image-20221110145053349.png" alt="image-20221110145053349" style="zoom:67%;" />

>   举例：
>
>    <img src="README.assets/image-20221110145131318.png" alt="image-20221110145131318" style="zoom:67%;" />

#### 1.3 单表排序查询

SELECT-FROM-WHERE-ORDER BY

 <img src="README.assets/image-20221110145239082.png" alt="image-20221110145239082" style="zoom:67%;" />

>   举例：
>
>    <img src="README.assets/image-20221110145352519.png" alt="image-20221110145352519" style="zoom:50%;" />

#### 1.4 单表模糊查询

SELECT-FROM-WHERE \* LIKE \*

 <img src="README.assets/image-20221110145653922.png" alt="image-20221110145653922" style="zoom:67%;" />

>   举例：
>
>   <img src="README.assets/image-20221110145900812.png" alt="image-20221110145900812" style="zoom:67%;" />
>
>   -   注：有时候可能用**两个下划线**表示**一个汉字字符**

### 2 多表联合查询

<img src="README.assets/image-20221110150153385.png" alt="image-20221110150153385" style="zoom:80%;" />

#### 2.1 多表连接

>   <img src="README.assets/image-20221110150210436.png" alt="image-20221110150210436" style="zoom:67%;" />

 <img src="README.assets/image-20221110150301939.png" alt="image-20221110150301939" style="zoom:67%;" />

-    <img src="README.assets/image-20221110150533664.png" alt="image-20221110150533664" style="zoom:67%;" />
-   注意这样先笛卡尔积再过滤其实效率很低，不如`join`关键字

>   等值连接举例：
>
>    <img src="README.assets/image-20221110150627204.png" alt="image-20221110150627204" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110150636947.png" alt="image-20221110150636947" style="zoom:67%;" />

#### 2.2 表更名/别名

 <img src="README.assets/image-20221110150756698.png" alt="image-20221110150756698" style="zoom:67%;" />

 <img src="README.assets/image-20221110151320371.png" alt="image-20221110151320371" style="zoom:67%;" />

>   举例：不等值连接
>
>    <img src="README.assets/image-20221110151119495.png" alt="image-20221110151119495" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110151548045.png" alt="image-20221110151548045" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221110151600924.png" alt="image-20221110151600924" style="zoom:67%;" />

>   举例：错误的
>
>    <img src="README.assets/image-20221110152030922.png" alt="image-20221110152030922" style="zoom:50%;" />
>
>   -   重点：==**与客观实体相关的记录不唯一**==，有时就需要**逆向思维**
>
>       >   在这个情景下就是，和同学（客观实体）相关的记录不唯一

## SQL对表增删改

<img src="README.assets/image-20221110152544447.png" alt="image-20221110152544447" style="zoom:67%;" />

### 1 SQL-INSERT

<img src="README.assets/image-20221110152637506.png" alt="image-20221110152637506" style="zoom:67%;" />

-   这里所谓的“批数据”，其实是基于已有的表创建新表
-   约束问题： <img src="README.assets/image-20221110152926165.png" alt="image-20221110152926165" style="zoom:67%;" />

>   举例：单一元组新增
>
>    <img src="README.assets/image-20221110152734852.png" alt="image-20221110152734852" style="zoom:50%;" />
>
>   举例：批元组新增
>
>    <img src="README.assets/image-20221110152915841.png" alt="image-20221110152915841" style="zoom:50%;" />
>
>    <img src="README.assets/image-20221110153014678.png" alt="image-20221110153014678" style="zoom:50%;" />
>
>   举例：复杂一点的批数据，涉及到聚集操作
>
>    <img src="README.assets/image-20221110153259067.png" alt="image-20221110153259067" style="zoom:50%;" />

### 2 SQL-DELETE

<img src="README.assets/image-20221110153423418.png" alt="image-20221110153423418" style="zoom:67%;" />

-   约束问题：<img src="README.assets/image-20221110153832630.png" alt="image-20221110153832630" style="zoom:67%;" />

>   举例：
>
>    <img src="README.assets/image-20221110153525213.png" alt="image-20221110153525213" style="zoom:50%;" />
>
>   举例：**在`where`子句中嵌套子查询与`in`关键字**
>
>    <img src="README.assets/image-20221110153557601.png" alt="image-20221110153557601" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110153724829.png" alt="image-20221110153724829" style="zoom:50%;" />

### 3 SQL-UPDATE

 <img src="README.assets/image-20221110153937069.png" alt="image-20221110153937069" style="zoom:60%;" />

>   举例：
>
>    <img src="README.assets/image-20221110154018552.png" alt="image-20221110154018552" style="zoom:67%;" />
>
>    <img src="README.assets/image-20221110154302312.png" alt="image-20221110154302312" style="zoom:50%;" />
>
>    <img src="README.assets/image-20221110154345018.png" alt="image-20221110154345018" style="zoom:50%;" />

## SQL修正与撤销数据库

### 1 SQL修改与删除表

<img src="README.assets/image-20221115160326475.png" alt="image-20221115160326475" style="zoom:60%;" />

-   之前已经讲了数据库的建立，但数据库建立后还可能修正，修正数据库主要就是在修正数据表
-   更具体的会在后面介绍

>   举例：
>
>   <img src="README.assets/image-20221115160446654.png" alt="image-20221115160446654" style="zoom:50%;" /> 

---

<img src="README.assets/image-20221115160630548.png" alt="image-20221115160630548" style="zoom:80%;" />

-   <img src="README.assets/image-20221115160639854.png" alt="image-20221115160639854" style="zoom:50%;" /> 

>   举例：
>
>   <img src="README.assets/image-20221115160653965.png" alt="image-20221115160653965" style="zoom:50%;" /> 

### 2 SQL删除数据库

<img src="README.assets/image-20221115160723955.png" alt="image-20221115160723955" style="zoom:67%;" />

>   举例：
>
>   <img src="README.assets/image-20221115160733907.png" alt="image-20221115160733907" style="zoom:67%;" />

### 3 SQL指定与关闭数据库

<img src="README.assets/image-20221115160945103.png" alt="image-20221115160945103" style="zoom:67%;" />

## 总结

<img src="README.assets/image-20221115161029598.png" alt="image-20221115161029598" style="zoom:60%;" />

-   `Create Table`可以定义关系模式、完整性约束，还可以定义物理存储，但这里没讲定义物理存储




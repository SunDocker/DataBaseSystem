# SQL语言与数据库完整性和安全性

<img src="README.assets/image-20221201110734457.png" alt="image-20221201110734457" style="zoom:50%;" />

## 数据库完整性的概念及分类

### 1 什么是数据库完整性

 <img src="README.assets/image-20221201111212142.png" alt="image-20221201111212142" style="zoom:67%;" />

-    <img src="README.assets/image-20221201111233671.png" alt="image-20221201111233671" style="zoom:50%;" />

    >   数据库设计中还会讲解该部分内容，从现实生活中发现约束、表达约束，在DBMS中起作用

### 2 为什么会产生完整性问题

<img src="README.assets/image-20221201111630508.png" alt="image-20221201111630508" style="zoom:67%;" /> 

-    重点：DBMS自动防止，让DBMS承担风险

>   <img src="README.assets/image-20221201111642166.png" alt="image-20221201111642166" style="zoom:67%;" />

### 3 怎样保证数据库完整性

<img src="README.assets/image-20221201111851468.png" alt="image-20221201111851468" style="zoom:50%;" /> 

-   方面二：**完整性控制程序**
-   方面一：**完整性规则**通常由DBA定义（DDL）

---

完整性约束规则：

<img src="README.assets/image-20221201112108783.png" alt="image-20221201112108783" style="zoom:67%;" /> 

-   四元组
-   对O在A条件下触发后，检查P，若不满足则R

### 4 数据库完整性的分类

#### 4.1 按约束对象分类

<img src="README.assets/image-20221201121646734.png" alt="image-20221201121646734" style="zoom:60%;" /> 

-   一列
-   多列/表

>   <img src="README.assets/image-20221201121709175.png" alt="image-20221201121709175" style="zoom:80%;" /> 

#### 4.2 按约束来源分类

<img src="README.assets/image-20221201121805462.png" alt="image-20221201121805462" style="zoom:67%;" /> 

>   <img src="README.assets/image-20221201121823539.png" alt="image-20221201121823539" style="zoom:67%;" /> 

#### 4.3 按约束状态分类

<img src="README.assets/image-20221201121841582.png" alt="image-20221201121841582" style="zoom:67%;" /> 

>   <img src="README.assets/image-20221201121916899.png" alt="image-20221201121916899" style="zoom:67%;" />

## SQL语言之列约束与表约束—静态约束

### 1 SQL支持的约束/静态约束模型

<img src="README.assets/image-20221201122003698.png" alt="image-20221201122003698" style="zoom:67%;" /> 

<img src="README.assets/image-20221201122052580.png" alt="image-20221201122052580" style="zoom:67%;" /> 

-   所以静态约束可以只在定义时表达O和P

### 2 SQL实现约束-Create Table

<img src="README.assets/image-20221201122215120.png" alt="image-20221201122215120" style="zoom:67%;" /> 

-   列约束空格隔开，表约束用逗号隔开

---

#### 2.1 列约束

<img src="README.assets/image-20221201122837574.png" alt="image-20221201122837574" style="zoom:67%;" /> 

-   一般来说`not null`算是一种比较独立的约束
-   `search_cond`比较特别，就是P，在更新时会检查是否满足
-   `references`是外键，那个`colname`，如果和正在定义约束的这个字段名字相同，就可以省略
    -   `on delete`是级联删除，是指在删除外键来源表时，对引用外键的表的操作
        -   `cascade`是删除
        -   `set null`是置空
    -   外键当然也有`on update`，这里没讲

>   举例：
>
>   <img src="README.assets/image-20221201123628081.png" alt="image-20221201123628081" style="zoom:67%;" /> 

#### 2.2 表约束

<img src="README.assets/image-20221201124224885.png" alt="image-20221201124224885" style="zoom:67%;" /> 

-   还是那些约束类型（除了`not null`），只是作用在多列上

    -   这里在`refrences`前要写`foreign key`表明是哪些列联合外键了

-   表约束与列约束、表约束之间是用`,`隔开的

    >   一个列的列约束用空格，列本身之间也用`,`

>   举例：
>
>   <img src="README.assets/image-20221201124526860.png" alt="image-20221201124526860" style="zoom:50%;" /> 
>
>   <img src="README.assets/image-20221201124717215.png" alt="image-20221201124717215" style="zoom:67%;" /> 
>
>   复杂的`check`
>
>    <img src="README.assets/image-20221201124811645.png" alt="image-20221201124811645" style="zoom:67%;" />

#### 2.3 Alter Table

<img src="README.assets/image-20221201125009382.png" alt="image-20221201125009382" style="zoom:67%;" /> 

>   举例：
>
>   <img src="README.assets/image-20221201125128885.png" alt="image-20221201125128885" style="zoom:67%;" /> 
>
>   <img src="README.assets/image-20221201125219051.png" alt="image-20221201125219051" style="zoom:67%;" />

### 3 SQL实现约束-Assertion

断言的概念与定义：

<img src="README.assets/image-20221201142109312.png" alt="image-20221201142109312" style="zoom:67%;" /> 

-   断言定义多了会影响数据库运行效率，增加DBMS的负担

<img src="README.assets/image-20221201142119152.png" alt="image-20221201142119152" style="zoom:67%;" /> 

>   举例：
>
>   <img src="README.assets/image-20221201142403058.png" alt="image-20221201142403058" style="zoom:67%;" /> 
>
>   <img src="README.assets/image-20221201142512531.png" alt="image-20221201142512531" style="zoom:67%;" />

## SQL语言之触发器—动态约束

### 1 模型

<img src="README.assets/image-20221201142627971.png" alt="image-20221201142627971" style="zoom:67%;" />

-   都需要定义，某些情况下可以省略

### 2 Trigger

<img src="README.assets/image-20221201142846929.png" alt="image-20221201142846929" style="zoom:67%;" />

-   过程完整性

---

定义：

<img src="README.assets/image-20221201143421031.png" alt="image-20221201143421031" style="zoom:67%;" />

-   `reference`用于定义后面会使用的变量
    -   其实就是在起别名，不超别名后面也能用，就直接用`new`、`old`也行
-   `for each row`是检索结果的每一行都要应用
-   `for each statement`是对每条SQL语句应用
-   `begin atomic ... end`是定义多条原子语句，就是这些语句要么全部执行，要么都别执行

---

事件：

<img src="README.assets/image-20221201143547490.png" alt="image-20221201143547490" style="zoom:67%;" />

---

别名：

<img src="README.assets/image-20221201143739169.png" alt="image-20221201143739169" style="zoom:67%;" />

---

举例1：

<img src="README.assets/image-20221201144026488.png" alt="image-20221201144026488" style="zoom:67%;" /> 

-   O：`salary on teacher`
-   P：`x.salary < y.salary`
-   A：`before update`
-   R：`raise_application_error`

举例2：

<img src="README.assets/image-20221201144443592.png" alt="image-20221201144443592" style="zoom:67%;" /> 

举例3：

<img src="README.assets/image-20221201144610874.png" alt="image-20221201144610874" style="zoom:60%;" /> 

-   外键相关修改，其实外键约束本身也可以自带

举例4：

<img src="README.assets/image-20221201145031563.png" alt="image-20221201145031563" style="zoom:60%;" /> 

举例5：

<img src="README.assets/image-20221201145427773.png" alt="image-20221201145427773" style="zoom:67%;" /> 

举例6：

<img src="README.assets/image-20221201145606821.png" alt="image-20221201145606821" style="zoom:67%;" /> 

>   小结1：
>
>   <img src="README.assets/image-20221201150100916.png" alt="image-20221201150100916" style="zoom:67%;" />

## 数据库安全性的概念及分类

### 1 数据库安全性的概念

<img src="README.assets/image-20221201152352163.png" alt="image-20221201152352163" style="zoom:67%;" /> 

-   本课程只介绍DBMS方面的安全性

### 2 数据库安全性的分类

<img src="README.assets/image-20221201152556426.png" alt="image-20221201152556426" style="zoom:67%;" /> 

<img src="README.assets/image-20221201152610288.png" alt="image-20221201152610288" style="zoom:67%;" /> 

### 3 数据库管理员的责任和义务

<img src="README.assets/image-20221201152912670.png" alt="image-20221201152912670" style="zoom:67%;" />

## 数据库自主安全性机制

### 1 数据库自主安全性

<img src="README.assets/image-20221201153024145.png" alt="image-20221201153024145" style="zoom:67%;" /> 

### 2 DBMS怎样实现数据库自主安全性

<img src="README.assets/image-20221201153216587.png" alt="image-20221201153216587" style="zoom:67%;" />

### 3 数据库自主安全性访问规则

<img src="README.assets/image-20221201153512516.png" alt="image-20221201153512516" style="zoom:67%;" />

-   用户S对对象O，在满足P条件时，拥有权利t 

---

举例：

<img src="README.assets/image-20221201153920600.png" alt="image-20221201153920600" style="zoom:67%;" />

<img src="README.assets/image-20221201154300231.png" alt="image-20221201154300231" style="zoom:67%;" />

### 4 自主安全性的实现方式

#### 4.1 存储矩阵

<img src="README.assets/image-20221201154741251.png" alt="image-20221201154741251" style="zoom:67%;" />

-   只有SOt，P可能太复杂，就省略了

>   <img src="README.assets/image-20221201154807421.png" alt="image-20221201154807421" style="zoom:67%;" />

#### 4.2 视图

<img src="README.assets/image-20221201155732031.png" alt="image-20221201155732031" style="zoom:67%;" />

-   视图可以通过`where`反映谓词
-   结合存储矩阵使用

## SQL语言之安全性实现

### 1 SQL语言的用户与权利

<img src="README.assets/image-20221201160310984.png" alt="image-20221201160310984" style="zoom:80%;" />

<img src="README.assets/image-20221201160422356.png" alt="image-20221201160422356" style="zoom:80%;" />

<img src="README.assets/image-20221201160432893.png" alt="image-20221201160432893" style="zoom:70%;" />

### 2 SQL-DCL的命令及其应用

语法：

<img src="README.assets/image-20221201160710738.png" alt="image-20221201160710738" style="zoom:67%;" />

-    <img src="README.assets/image-20221201161028620.png" alt="image-20221201161028620" style="zoom:67%;" />
-   授权+视图可以完全较为完整的自主安全性

<img src="README.assets/image-20221201161047575.png" alt="image-20221201161047575" style="zoom:67%;" />  

>   举例：
>
>   <img src="README.assets/image-20221201161013063.png" alt="image-20221201161013063" style="zoom:67%;" /> 
>
>   <img src="README.assets/image-20221201161059641.png" alt="image-20221201161059641" style="zoom:67%;" /> 

## 安全性控制的其他方面

### 1 自主安全性的授权过程及其问题

<img src="README.assets/image-20221201161522313.png" alt="image-20221201161522313" style="zoom:67%;" /> 

<img src="README.assets/image-20221201161659680.png" alt="image-20221201161659680" style="zoom:67%;" /> 

-   广度与深度范围限制

<img src="README.assets/image-20221201161744496.png" alt="image-20221201161744496" style="zoom:67%;" /> 

-   收回问题

>   这些问题本课程不讲

### 2 强制安全性

>   还记得最开始的安全性分类吗，有自主安全性和强制安全性

<img src="README.assets/image-20221201162028315.png" alt="image-20221201162028315" style="zoom:67%;" />

-   高级别用户不能写低级别数据，因为一旦写了，低级别数据中就会出现高级别用户相关的信息，这样是不合法的，可能低级别的用户就不再能访问了

---

<img src="README.assets/image-20221201162336583.png" alt="image-20221201162336583" style="zoom:67%;" /> 

-   对列安全性的规定
-   对行安全性的规定

---

新的问题：

<img src="README.assets/image-20221201162402869.png" alt="image-20221201162402869" style="zoom:67%;" /> 

-   多级关系，有更多的管理技巧

    >   本课程不讲

>   小结2：
>
>   <img src="README.assets/image-20221201162806762.png" alt="image-20221201162806762" style="zoom:67%;" />
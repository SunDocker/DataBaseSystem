# 关系模型

## 基本概念

<img src="README.assets/image-20221103140952556.png" alt="image-20221103140952556" style="zoom:67%;" />

-   一组概念
-   三个完整性 

### 1 关系模型概述

#### 1.1 关系模型的提出

<img src="README.assets/image-20221103141134682.png" alt="image-20221103141134682" style="zoom:50%;" />

#### 1.2 关系模型的研究内容

<img src="README.assets/image-20221103141245065.png" alt="image-20221103141245065" style="zoom:50%;" />

-   描述table
-   table的操作
-   table操作的含义、结果、约束

#### 1.3 关系模型的三要素

<img src="README.assets/image-20221103141447448.png" alt="image-20221103141447448" style="zoom:50%;" />

#### 1.4 关系模型与关系数据库语言的关系

<img src="README.assets/image-20221103141842208.png" alt="image-20221103141842208" style="zoom:50%;" />

<img src="README.assets/image-20221103142029178.png" alt="image-20221103142029178" style="zoom:50%;" />

<img src="README.assets/image-20221103142234159.png" alt="image-20221103142234159" style="zoom:67%;" />

关系运算：

-   基于关系代数的运算：基于集合的运算

-   基于关系演算的运算

    -   元组演算：基于逻辑的运算

    -   域演算：基于示例的运算

        >   虽然形式上与元组演算类似，但是以域为单位的，操作的对象是域（元组演算则是元组）

数学语言转换为计算机语言：

<img src="README.assets/image-20221103141853800.png" alt="image-20221103141853800" style="zoom:50%;" />

<img src="README.assets/image-20221103142113090.png" alt="image-20221103142113090" style="zoom:50%;" />

<img src="README.assets/image-20221103142252350.png" alt="image-20221103142252350" style="zoom:50%;" />

#### 1.5 开发软件系统的一种思维

基于数学的设计与开发

<img src="README.assets/image-20221103142439041.png" alt="image-20221103142439041" style="zoom:50%;" />

#### 1.6 主要学习内容

<img src="README.assets/image-20221103142535538.png" alt="image-20221103142535538" style="zoom:50%;" />

### 2 什么是关系

#### 2.1 表的构成要素

>   <img src="README.assets/image-20221103142647135.png" alt="image-20221103142647135" style="zoom:50%;" />

<img src="README.assets/image-20221103142819250.png" alt="image-20221103142819250" style="zoom:50%;" />

#### 2.2 表的严格定义

列的取值范围：域

<img src="README.assets/image-20221103142952109.png" alt="image-20221103142952109" style="zoom:50%;" />

元组及所有可能的组合：笛卡尔积

<img src="README.assets/image-20221103143154588.png" alt="image-20221103143154588" style="zoom:50%;" />

<img src="README.assets/image-20221103143307451.png" alt="image-20221103143307451" style="zoom:50%;" />

关系：笛卡尔积的子集

<img src="README.assets/image-20221103143559981.png" alt="image-20221103143559981" style="zoom:50%;" />

>   域名是对域的命名，属性名是对关系中列的命名

关系模式：Schema / Head，对关系的描述

<img src="README.assets/image-20221103143752640.png" alt="image-20221103143752640" style="zoom:50%;" />

>   注意这里的R(A1:D1,...)就应该叫做**关系模式**，不应当认为其是关系

>   <img src="README.assets/image-20221103143803075.png" alt="image-20221103143803075" style="zoom:50%;" />

-   DBMS中的关系模式：`关系模式(属性名 域名, ...)`

    <img src="README.assets/image-20221103144234248.png" alt="image-20221103144234248" style="zoom:67%;" />

-   域名就是`属性类型(长度)`

关系模式与关系：

<img src="README.assets/image-20221103144611255.png" alt="image-20221103144611255" style="zoom:50%;" />

思维回顾：

<img src="README.assets/image-20221103145017099.png" alt="image-20221103145017099" style="zoom:50%;" />

#### 2.2 关系的特性

列**同质**：

<img src="README.assets/image-20221103145225346.png" alt="image-20221103145225346" style="zoom:50%;" />

>   <img src="README.assets/image-20221103145246729.png" alt="image-20221103145246729" style="zoom:67%;" />



不同列不同属性名：

<img src="README.assets/image-20221103145330533.png" alt="image-20221103145330533" style="zoom:50%;" />

>   <img src="README.assets/image-20221103145345425.png" alt="image-20221103145345425" style="zoom:50%;" />



行列互换性：

-   列区分：属性名
-   行区分：某几列的值/关键字

<img src="README.assets/image-20221103145529434.png" alt="image-20221103145529434" style="zoom:50%;" />

>   <img src="README.assets/image-20221103145547602.png" alt="image-20221103145547602" style="zoom:50%;" />



不重复：

<img src="README.assets/image-20221103145634167.png" alt="image-20221103145634167" style="zoom:67%;" />

-   这里就体现出了表和关系的区别

>   <img src="README.assets/image-20221103145645358.png" alt="image-20221103145645358" style="zoom:50%;" />



第一范式：

<img src="README.assets/image-20221103145820050.png" alt="image-20221103145820050" style="zoom:67%;" />

>   <img src="README.assets/image-20221103145829751.png" alt="image-20221103145829751" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221103145910477.png" alt="image-20221103145910477" style="zoom:50%;" />
>
>   让不符合的转换为符号的，加记录、加列

#### 2.3 重要概念

候选码(Candidate Key)/候选键：

<img src="README.assets/image-20221103150317224.png" alt="image-20221103150317224" style="zoom:67%;" />

-   注意其**极小性**

>   <img src="README.assets/image-20221103150325758.png" alt="image-20221103150325758" style="zoom:67%;" />
>
>   **多个候选码**：
>
>   <img src="README.assets/image-20221103150443201.png" alt="image-20221103150443201" style="zoom:50%;" />

主码(Primary Key)/主键：

<img src="README.assets/image-20221103150529461.png" alt="image-20221103150529461" style="zoom:50%;" />

>   <img src="README.assets/image-20221103150542100.png" alt="image-20221103150542100" style="zoom:67%;" />

主属性与非主属性：

<img src="README.assets/image-20221103150617905.png" alt="image-20221103150617905" style="zoom:67%;" />

>   <img src="README.assets/image-20221103150628399.png" alt="image-20221103150628399" style="zoom:67%;" />

<img src="README.assets/image-20221103150638048.png" alt="image-20221103150638048" style="zoom:67%;" />

>   <img src="README.assets/image-20221103150645487.png" alt="image-20221103150645487" style="zoom:67%;" />

外码(Foreign Key)/外键：

<img src="README.assets/image-20221103150721245.png" alt="image-20221103150721245" style="zoom:50%;" />

-   两个关系通常是靠外码连接起来的

>   <img src="README.assets/image-20221103150744901.png" alt="image-20221103150744901" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221103150858964.png" alt="image-20221103150858964" style="zoom:50%;" />

#### 2.5 小结

<img src="README.assets/image-20221103151305309.png" alt="image-20221103151305309" style="zoom:67%;" />

### 3 关系模型中的完整性约束

>   回顾三要素：
>
>   -   数据结构：关系
>   -   基本操作：并、差、积、选择、投影
>   -   完整性约束

#### 3.1 实体完整性

<img src="README.assets/image-20221103151605577.png" alt="image-20221103151605577" style="zoom:67%;" />

>   <img src="README.assets/image-20221103151615724.png" alt="image-20221103151615724" style="zoom:67%;" />

空值的概念：

<img src="README.assets/image-20221103151706410.png" alt="image-20221103151706410" style="zoom:67%;" />

-   ？：<img src="README.assets/image-20221103151715553.png" alt="image-20221103151715553" style="zoom:67%;" />

-   ？的影响：<img src="README.assets/image-20221103151730510.png" alt="image-20221103151730510" style="zoom:67%;" />

    >   <img src="README.assets/image-20221103151755241.png" alt="image-20221103151755241" style="zoom:67%;" />

-    <img src="README.assets/image-20221103151803069.png" alt="image-20221103151803069" style="zoom:67%;" />

    -   常用的策略：**默认值**

#### 3.2 参照完整性

<img src="README.assets/image-20221103152022199.png" alt="image-20221103152022199" style="zoom:70%;" />

>   <img src="README.assets/image-20221103152041174.png" alt="image-20221103152041174" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221103152049687.png" alt="image-20221103152049687" style="zoom:67%;" /><img src="README.assets/image-20221103152056246.png" alt="image-20221103152056246" style="zoom:67%;" />

#### 3.3 用户自定义完整性

<img src="README.assets/image-20221103152225871.png" alt="image-20221103152225871" style="zoom:67%;" />

-   在**列数据类型**基础上的约束
-   对属性或属性组合的约束

>   <img src="README.assets/image-20221103152235861.png" alt="image-20221103152235861" style="zoom:50%;" />

#### 3.4 DBMS对关系完整性的支持

<img src="README.assets/image-20221103152455979.png" alt="image-20221103152455979" style="zoom:67%;" />

### 4 总结

<img src="README.assets/image-20221103152617210.png" alt="image-20221103152617210" style="zoom:67%;" />

## 关系代数

<img src="README.assets/image-20221103152802931.png" alt="image-20221103152802931" style="zoom:67%;" />

-   一个集合，操作，一个集合，关系代数，结果

### 1 关系代数概述

#### 1.1 关系代数运算的特点

<img src="README.assets/image-20221103153111685.png" alt="image-20221103153111685" style="zoom:67%;" />

#### 1.2 关系代数运算的基本操作

<img src="README.assets/image-20221103153242413.png" alt="image-20221103153242413" style="zoom:50%;" />

#### 1.3 为什么要提出关系代数

<img src="README.assets/image-20221103153313104.png" alt="image-20221103153313104" style="zoom:67%;" />

借鉴思想，先实现基本操作，再组合成复杂操作

<img src="README.assets/image-20221103153535154.png" alt="image-20221103153535154" style="zoom:67%;" />

### 2 关系代数的基本操作

#### 2.0 关系代数运算的约束

>   <img src="README.assets/image-20221103153722536.png" alt="image-20221103153722536" style="zoom:67%;" />

<img src="README.assets/image-20221103153757777.png" alt="image-20221103153757777" style="zoom:67%;" />

>   满足并相容性的例子：
>
>   <img src="README.assets/image-20221103153916787.png" alt="image-20221103153916787" style="zoom:60%;" />

#### 2.1 “并”操作

<img src="README.assets/image-20221103154023712.png" alt="image-20221103154023712" style="zoom:67%;" />

<img src="README.assets/image-20221103154040109.png" alt="image-20221103154040109" style="zoom:67%;" />

-   注意：需要去重
-   当然前提是并相容
-   位置无关性

>   抽象举例：
>
>   <img src="README.assets/image-20221103154120406.png" alt="image-20221103154120406" style="zoom:67%;" />
>
>   语义举例：
>
>   <img src="README.assets/image-20221103154146169.png" alt="image-20221103154146169" style="zoom:67%;" />
>
>   <img src="README.assets/image-20221103154245254.png" alt="image-20221103154245254" style="zoom:67%;" />
>
>   注意如何正确表述汉语的查询要求

#### 2.2 “差”操作

<img src="README.assets/image-20221103154341025.png" alt="image-20221103154341025" style="zoom:67%;" />

-   注意，不满足交换律

    <img src="README.assets/image-20221103154417805.png" alt="image-20221103154417805" style="zoom:67%;" />

>   抽象举例：
>
>   <img src="README.assets/image-20221103154431919.png" alt="image-20221103154431919" style="zoom:50%;" />
>
>   语义举例：
>
>   <img src="README.assets/image-20221103154446707.png" alt="image-20221103154446707" style="zoom:50%;" />
>
>   <img src="README.assets/image-20221103154502565.png" alt="image-20221103154502565" style="zoom:67%;" />
>
>   注意如何正确表述汉语的查询要求










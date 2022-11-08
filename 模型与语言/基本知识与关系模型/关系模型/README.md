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
>   注意如何正确表述汉语的查询要求（汉语的这部分也写进总结博客里吧）

#### 2.3 广义笛卡尔积

<img src="README.assets/image-20221103160918457.png" alt="image-20221103160918457" style="zoom:67%;" />

- 交换律

  <img src="README.assets/image-20221103161423968.png" alt="image-20221103161423968" style="zoom:67%;" />

- 度数：相加

  <img src="README.assets/image-20221103161436366.png" alt="image-20221103161436366" style="zoom:60%;" />

- 基数：相乘

  <img src="README.assets/image-20221103161452591.png" alt="image-20221103161452591" style="zoom:67%;" />

- 一个检索涉及到多个表时，需要将这些表串接或拼接起来，然后才能检索，这时，就要使用广义笛卡尔积运算

- 

> 抽象举例：
>
> <img src="README.assets/image-20221103161055172.png" alt="image-20221103161055172" style="zoom:50%;" />
>
> <img src="README.assets/image-20221103161250731.png" alt="image-20221103161250731" style="zoom:50%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221103161331298.png" alt="image-20221103161331298" style="zoom:50%;" />

#### 2.4 “选择”操作

<img src="README.assets/image-20221103161636373.png" alt="image-20221103161636373" style="zoom:67%;" />

<img src="README.assets/image-20221103161800835.png" alt="image-20221103161800835" style="zoom:67%;" />

- 选择操作从给定的关系中选出满足条件的行
- 组成条件的三要素：分量、逻辑运算符、比较表达式
- 条件的书写很重要，尤其是当不同运算符在一起时，要注意运算符的优先次序，优先次序自高至低为${ 括弧；\theta ；\neg ；\and ；\or }$

> 抽象举例：
>
> <img src="README.assets/image-20221103162006401.png" alt="image-20221103162006401" style="zoom:67%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221103162247819.png" alt="image-20221103162247819" style="zoom:60%;" />
>
> - 这里加**引号**表示**字符串**
>
> > 战神教我们的书写顺序：先写`(R)`，代表要操作`R`这个关系，再写$\sigma$，代表要进行选择操作，然后再写`con(t)`，代表选择的条件
>
> <img src="README.assets/image-20221103162459172.png" alt="image-20221103162459172" style="zoom:50%;" />
>
> <img src="README.assets/image-20221103162513401.png" alt="image-20221103162513401" style="zoom:60%;" />

#### 2.5 “投影”操作

<img src="README.assets/image-20221103162757211.png" alt="image-20221103162757211" style="zoom:67%;" />

- 用户可以根据需要通过投影、选择操作查询他所关心的数据信息。

<img src="README.assets/image-20221103163026580.png" alt="image-20221103163026580" style="zoom:67%;" />

- 对于**关系**来说，如果投影后有**重复元组**，应该去掉

<img src="README.assets/image-20221103163043375.png" alt="image-20221103163043375" style="zoom:67%;" />

> 抽象举例：
>
> <img src="README.assets/image-20221103163132301.png" alt="image-20221103163132301" style="zoom:50%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221103163305527.png" alt="image-20221103163305527" style="zoom:50%;" />
>
> 投影与选择操作一起使用的语义举例：
>
> <img src="README.assets/image-20221103163449508.png" alt="image-20221103163449508" style="zoom:67%;" />

#### 2.6 小结/书写思路

<img src="README.assets/image-20221103170155976.png" alt="image-20221103170155976" style="zoom:67%;" />

操作含义

用户语义

### 3 关系代数的扩展操作

> 用基本操作组合实现的操作

#### 3.1 “交”操作

<img src="README.assets/image-20221108155529746.png" alt="image-20221108155529746" style="zoom:67%;" />

性质：

- <img src="README.assets/image-20221108155556989.png" alt="image-20221108155556989" style="zoom:80%;" />

> <img src="README.assets/image-20221108155708906.png" alt="image-20221108155708906" style="zoom:80%;" />

> 抽象举例：
>
> <img src="README.assets/image-20221108160250994.png" alt="image-20221108160250994" style="zoom:67%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221108160358069.png" alt="image-20221108160358069" style="zoom:67%;" />
>
> <img src="README.assets/image-20221108160426021.png" alt="image-20221108160426021" style="zoom:67%;" />
>
> <img src="README.assets/image-20221108160431781.png" alt="image-20221108160431781" style="zoom:67%;" />

#### 3.2 “$\theta-$连接操作”

<img src="README.assets/image-20221108160547077.png" alt="image-20221108160547077" style="zoom:67%;" />

- 现实中有很多**对多个关系的操作**
- 也有许多需要**关系与自身连接**的操作

> <img src="README.assets/image-20221108160610697.png" alt="image-20221108160610697" style="zoom:67%;" />

数学定义：

<img src="README.assets/image-20221108161644119.png" alt="image-20221108161644119" style="zoom:67%;" />

> <img src="README.assets/image-20221108161652019.png" alt="image-20221108161652019" style="zoom:80%;" />

:star:DBMS的实现：

<img src="README.assets/image-20221108163141764.png" alt="image-20221108163141764" style="zoom:67%;" />

- 也就是说，从实现的角度来讲，**$\theta-$连接**操作快于**笛卡尔积再选择**

  > 所以，能连接就连接，会比较快，能**优化**

> 抽象举例：
>
> <img src="README.assets/image-20221108161828478.png" alt="image-20221108161828478" style="zoom:67%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221108162049395.png" alt="image-20221108162049395" style="zoom:67%;" />
>
> <img src="README.assets/image-20221108162224307.png" alt="image-20221108162224307" style="zoom:67%;" />
>
> > 注意，这只理论操作的过程，实际实现时不需要这样笛卡尔积，能直接得到结果
>
> :star:关系自连接与**更名**：:star:
>
> > 这个例子很重要，体会**<u>连接、选择、投影</u>**的结合作用
>
> <img src="README.assets/image-20221108162601517.png" alt="image-20221108162601517" style="zoom:67%;" />
>
> <img src="README.assets/image-20221108162609414.png" alt="image-20221108162609414" style="zoom:67%;" />
>
> > 有的教学中会将**更名**也作为**基本操作**

#### 3.3 “等值-连接”操作

> 一种特殊的$\theta-$连接

<img src="README.assets/image-20221108163317102.png" alt="image-20221108163317102" style="zoom:67%;" />

> <img src="README.assets/image-20221108163326584.png" alt="image-20221108163326584" style="zoom:60%;" />
>
> 注意这里说的第二点，就是**效率问题**

> 抽象举例：
>
> <img src="README.assets/image-20221108163516527.png" alt="image-20221108163516527" style="zoom:60%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221108163628501.png" alt="image-20221108163628501" style="zoom:67%;" />
>
> <img src="README.assets/image-20221108163644829.png" alt="image-20221108163644829" style="zoom:67%;" />
>
> 注意，这只理论操作的过程，实际实现时不需要这样笛卡尔积，能直接得到结果

#### 3.4 “自然连接”操作

> 普遍使用的一种$\theta-$连接

<img src="README.assets/image-20221108163841853.png" alt="image-20221108163841853" style="zoom:67%;" />

> 就是要有**属性名相同的属性**，可以有多个。然后结果中还会自动去掉同样的属性

<img src="README.assets/image-20221108164045564.png" alt="image-20221108164045564" style="zoom:67%;" />

> 抽象举例：
>
> <img src="README.assets/image-20221108164151941.png" alt="image-20221108164151941" style="zoom:67%;" />
>
> 语义举例：
>
> <img src="README.assets/image-20221108164516851.png" alt="image-20221108164516851" style="zoom:60%;" />
>
> > 理论步骤：
> >
> > <img src="README.assets/image-20221108164538421.png" alt="image-20221108164538421" style="zoom:60%;" />
> >
> > <img src="README.assets/image-20221108164558030.png" alt="image-20221108164558030" style="zoom:60%;" />
>
> <img src="README.assets/image-20221108164627374.png" alt="image-20221108164627374" style="zoom:67%;" />

#### 3.5 小结/书写思路

<img src="README.assets/image-20221108164732028.png" alt="image-20221108164732028" style="zoom:67%;" />

- **连接操作**是数据库的重要特点，效率高

### 4 组合与应用训练

#### 4.1 集合操作思维训练

1. 涉及几个表

   > 涉及几个表本质是看需要**哪些列**，同时还要看语义情景下**表之间的关系**，无关的不必要的表不算在内

2. 要求啥条件

3. 关注哪些列

---

举例1：

<img src="README.assets/image-20221108165032243.png" alt="image-20221108165032243" style="zoom:60%;" />

> 由里向外书写

---

举例2：连接条件

<img src="README.assets/image-20221108165524877.png" alt="image-20221108165524877" style="zoom:60%;" />

#### 4.2 语法和语义问题

举例：正确的

<img src="README.assets/image-20221108165653550.png" alt="image-20221108165653550" style="zoom:80%;" />

---

举例：语义“且”错误的

<img src="README.assets/image-20221108165734692.png" alt="image-20221108165734692" style="zoom:67%;" />

> 这个用交运算实现也可以
>
> <img src="README.assets/image-20221108170136163.png" alt="image-20221108170136163" style="zoom:67%;" />

---

举例：“语义且”改正的

<img src="README.assets/image-20221108165854642.png" alt="image-20221108165854642" style="zoom:67%;" />

---

举例：错误使用“自然连接”

<img src="README.assets/image-20221108165917278.png" alt="image-20221108165917278" style="zoom:67%;" />

> 自然连接会**将值相等的属性连接完后直接合并成一个**，自己自然连接自己得到的还是自己

---

举例：语义“不相等”，错误的

<img src="README.assets/image-20221108170329316.png" alt="image-20221108170329316" style="zoom:67%;" />

---

举例：语义“不相等”，不满足**并相容性**，错误的

<img src="README.assets/image-20221108170412187.png" alt="image-20221108170412187" style="zoom:67%;" />

---

举例：语义“不相等”，正确的

<img src="README.assets/image-20221108170601522.png" alt="image-20221108170601522" style="zoom:80%;" />

> 解决方法：先投影好再差

#### 4.3 基本思路

<img src="README.assets/image-20221108170738368.png" alt="image-20221108170738368" style="zoom:80%;" />

### 5 复杂扩展操作

#### 5.1 “除”操作

概述：

<img src="README.assets/image-20221108190441310.png" alt="image-20221108190441310" style="zoom:67%;" />

---

前提运算：

<img src="README.assets/image-20221108190524513.png" alt="image-20221108190524513" style="zoom:67%;" />

---

定义：

- 属性的构成

  <img src="README.assets/image-20221108190615192.png" alt="image-20221108190615192" style="zoom:67%;" />

- 元组的构成

  <img src="README.assets/image-20221108190742890.png" alt="image-20221108190742890" style="zoom:67%;" />

---

数学描述：

<img src="README.assets/image-20221108190908393.png" alt="image-20221108190908393" style="zoom:67%;" />

> 第一条数学描述就是按照上面的**构成**说的；
>
> 第二条数学描述要通过例子理解

---

抽象举例：

<img src="README.assets/image-20221108191321664.png" alt="image-20221108191321664" style="zoom:67%;" />

抽象举例：用基本操作表示除法

<img src="README.assets/image-20221108192130403.png" alt="image-20221108192130403" style="zoom:67%;" />

- 先找出组合完之后不在R中的，再做差，剩下的就是在R中的

> 1. 把R对应的属性扔掉，剩下的去重（投影）
> 2. 因为要找的就是剩下的当中，和S组合后是R中记录的东西，所以先把剩下的这个东西直接和S乘积一下，得出一大堆
> 3. 一大堆中有些在R中有些不在R中，差R，就得到了不在R中的，也就是说这些组合是不行的，组完了不在R中
> 4. 把上一步差完的东西再删除对应的属性，就是这些东西不能和S组合，所以最后把它们差去就可以

语义举例：主要应用在带有“全部”、“所有”字样的语义中

<img src="README.assets/image-20221108192347019.png" alt="image-20221108192347019" style="zoom:80%;" />

- **“全部”主要是全在了S上**，因为得到“商”，和S所有的记录组合“全部”都是R中的

语义举例3：体会“中间表”的作用

<img src="README.assets/image-20221108192730139.png" alt="image-20221108192730139" style="zoom:67%;" />

> <img src="README.assets/image-20221108192819103.png" alt="image-20221108192819103" style="zoom:67%;" />
>
> 在这里是一样的，因为S#和C#是主键，如果不是主键呢？？？

#### 5.2 “外连接”操作

概述：外连接的提出

<img src="README.assets/image-20221108195725168.png" alt="image-20221108195725168" style="zoom:67%;" />

- 有的老师没讲课我也想知道，也要体现在结果里

---

定义：

<img src="README.assets/image-20221108195851363.png" alt="image-20221108195851363" style="zoom:67%;" />

- 连接时的依据还是**同名属性的值相等**

举例：

<img src="README.assets/image-20221108195937956.png" alt="image-20221108195937956" style="zoom:67%;" />

---

外连接的分类：

<img src="README.assets/image-20221108200036170.png" alt="image-20221108200036170" style="zoom:67%;" />

举例：

<img src="README.assets/image-20221108200324066.png" alt="image-20221108200324066" style="zoom:67%;" />

<img src="README.assets/image-20221108200332478.png" alt="image-20221108200332478" style="zoom:67%;" />

<img src="README.assets/image-20221108200410546.png" alt="image-20221108200410546" style="zoom:67%;" />

<img src="README.assets/image-20221108200437759.png" alt="image-20221108200437759" style="zoom:67%;" />

<img src="README.assets/image-20221108200538517.png" alt="image-20221108200538517" style="zoom:67%;" />

### 6 总结

<img src="README.assets/image-20221108200632664.png" alt="image-20221108200632664" style="zoom:67%;" />

<img src="README.assets/image-20221108200742012.png" alt="image-20221108200742012" style="zoom:67%;" />

回顾计算机系统的设计思想之一：基本运算的组合

<img src="README.assets/image-20221108200854790.png" alt="image-20221108200854790" style="zoom:67%;" />

- 有关系代数操作，数据库管理系统的实现就会变容易了




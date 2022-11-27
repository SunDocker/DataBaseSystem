# 复杂SQL与视图

>   主要内容概览：
>
>   <img src="README.assets/image-20221115161522154.png" alt="image-20221115161522154" style="zoom:67%;" /> 
>
>   重点与难点：
>
>   <img src="README.assets/image-20221115161612888.png" alt="image-20221115161612888" style="zoom:60%;" /> 
>
>   -   三组谓词的运用
>   -   聚集函数、分组
>   -   视图

## 子查询

### 子查询概述

### 1 为什么需要子查询/子查询的作用

<img src="README.assets/image-20221115161755185.png" alt="image-20221115161755185" style="zoom:67%;" /> 

### 2 子查询的概念与分类

<img src="README.assets/image-20221115161902779.png" alt="image-20221115161902779" style="zoom:67%;" /> 

-   子查询返回的是**结果的集合**

## (NOT)IN谓词子查询

### 1 基本语法

<img src="README.assets/image-20221115161941031.png" alt="image-20221115161941031" style="zoom:67%;" /> 

-   表达式是某个**计算的结果**
-   注意表达式与子查询的匹配性
-   本质上等于多个`or`

>   举例：
>
>   -   枚举给出集合
>
>       <img src="README.assets/image-20221115162202977.png" alt="image-20221115162202977" style="zoom:67%;" /> 
>
>   -   子查询代替**表连接**
>
>       <img src="README.assets/image-20221115162455754.png" alt="image-20221115162455754" style="zoom:67%;" /> 
>
>       <img src="README.assets/image-20221115162517050.png" alt="image-20221115162517050" style="zoom:67%;" /> 
>
>   -   not in/子查询结合表连接
>
>       <img src="README.assets/image-20221115162847516.png" alt="image-20221115162847516" style="zoom:67%;" /> 
>
>       >   回顾之前讲过的不正确的子查询：
>       >
>       >   <img src="README.assets/image-20221115162913870.png" alt="image-20221115162913870" style="zoom:67%;" /> 

### 2 子查询的相关性

<img src="README.assets/image-20221115163020692.png" alt="image-20221115163020692" style="zoom:67%;" />

-   还会有变量作用域的约束，外层无法看到内层，内层可以看到外层

>   举例：
>
>   <img src="README.assets/image-20221115163035578.png" alt="image-20221115163035578" style="zoom:67%;" /> 

---

<img src="README.assets/image-20221115163135845.png" alt="image-20221115163135845" style="zoom:67%;" />

---

<img src="README.assets/image-20221115163215238.png" alt="image-20221115163215238" style="zoom:67%;" />

>   举例：
>
>   <img src="README.assets/image-20221115163523655.png" alt="image-20221115163523655" style="zoom:67%;" />
>
>   -   Select语句本质是一个循环，循环遍历所有表记录
>
>   -   这里的子查询要用到外层查询的变量，所以从SQL实现与执行的角度讲，就不能先执行子查询得到结果集合了，而是要在每次执行外层查询时，确定外层给到内层的参数，然后再执行子查询，再判断
>
>       >   在这里，每次传递给子查询的参数就是S#，当然子查询返回的集合中往往就一个学号或者是空，但毕竟是个集合，所以还是要用`in`
>
>       >   所以说，能非相关最好还是非相关，因为子查询不用执行那么多次

## $\theta$ Some与$\theta$ All谓词子查询

### 1 基本语法

<img src="README.assets/image-20221115164341969.png" alt="image-20221115164341969" style="zoom:67%;" /> 

-   某一个/存在量词
-   所有/全称量词

>   举例：
>
>   -   “最”
>
>       <img src="README.assets/image-20221115164704071.png" alt="image-20221115164704071" style="zoom:67%;" /> 
>
>       <img src="README.assets/image-20221115165245784.png" alt="image-20221115165245784" style="zoom:67%;" /> 
>
>       <img src="README.assets/image-20221115165307339.png" alt="image-20221115165307339" style="zoom:67%;" /> 
>
>   -   “不是最”
>
>       <img src="README.assets/image-20221115164752073.png" alt="image-20221115164752073" style="zoom:67%;" /> 
>
>   -   **相关子查询**，要循环运行子查询，因为要传递参数
>
>       <img src="README.assets/image-20221115165037689.png" alt="image-20221115165037689" style="zoom:67%;" /> 
>
>       >   通过这个例子也可以知道，要不要相关子查询，主要看子查询是否需要从外层查询中获取某些信息
>
>       <img src="README.assets/image-20221115165639790.png" alt="image-20221115165639790" style="zoom:60%;" /> 
>
>       >   注意这里把”张三“的约束都写到外层了，而且先于子查询，这样当”张三“约束不满足时也就没必要去执行子查询了，减少子查询执行次数

>   补充：为什么不用$\theta$ Any？
>
>   <img src="README.assets/image-20221115183554677.png" alt="image-20221115183554677" style="zoom:67%;" />
>
>   >   <img src="README.assets/image-20221115183612552.png" alt="image-20221115183612552" style="zoom:50%;" /> 

### 2 等价变换

<img src="README.assets/image-20221115183937170.png" alt="image-20221115183937170" style="zoom:80%;" /> 

-   `in`和`some`是等价的

>   举例：
>
>   <img src="README.assets/image-20221115183955706.png" alt="image-20221115183955706" style="zoom:67%;" /> 

---

<img src="README.assets/image-20221115184025303.png" alt="image-20221115184025303" style="zoom:67%;" /> 

-   `not in`和`<> all`是等价的

>   举例：
>
>   <img src="README.assets/image-20221115184147812.png" alt="image-20221115184147812" style="zoom:67%;" />

## (NOT)EXISTS子查询

### 1 基本语法

 <img src="README.assets/image-20221115193636516.png" alt="image-20221115193636516" style="zoom:67%;" />

-   <img src="README.assets/image-20221115194034116.png" alt="image-20221115194034116" style="zoom:67%;" /> 
-   <img src="README.assets/image-20221115194118398.png" alt="image-20221115194118398" style="zoom:67%;" /> 
    -   所有、全部$\Lrarr$不存在没有

>   举例：相关子查询
>
>   <img src="README.assets/image-20221115193849759.png" alt="image-20221115193849759" style="zoom:67%;" /> 
>
>   -   在内循环中，代表这个同学是否学过这个课，然后这个子查询的结果直接影响了`where`，从而能决定是否过滤
>
>   -   其实在没有`not`的情况下，`exist`完全没必要
>
>       <img src="README.assets/image-20221115194101117.png" alt="image-20221115194101117" style="zoom:67%;" />

>   举例：”所有“=”不存在没“
>
>   <img src="README.assets/image-20221115194641604.png" alt="image-20221115194641604" style="zoom:67%;" />
>
>   :star:子查询的思路
>
>   1.   确定最主要的投影、关系、选择条件
>
>        -   投影（`select`）：学生姓名
>        -   关系（`from`）：Student
>        -   选择条件（`where`）：学过001号教师的所有课程
>   2.   选择条件中有“所有”，则逆向思维，使用`not exists`，变成“不存在没学过的课”，则在`not exists`内部，只需要查找这个学生没学过的001号教师的课
>        -   投影：保留整条**课程记录**即可，投影不是重点，但要注意查找的主体是**课程**
>        -   关系：Course
>        -   选择条件：首先要是001号老师教的课（`C.T#=001`），并且外层的学生没学过001号教师的这个课
>   3.   选择条件中的“没学过这个课”，也就是对应的记录不存在，就是查出来是空，所以再用一次`not exists`，只需要查询这个学生学过的001号教师的课
>        -   投影：保留整条**课程记录**即可，投影不是重点，但要注意查找的主体是**课程**
>        -   关系：SC
>        -   选择条件：是外层学生的且是001号老师教的（`Student.S#=SC.S# and Course.C#=SC.C#`）
>
>   举例：”没有任何“
>
>   <img src="README.assets/image-20221115195124485.png" alt="image-20221115195124485" style="zoom:67%;" />
>
>   -   没学过，意思就是，把这个同学当参数传入子查询，然后查一查老师讲的并且这个同学学了的记录
>   -   所以要自然连接，然后把学生条件（`S#=Student.S#`）和老师条件（`Tname=‘李明’`）加入
>
>   举例：”所有“
>
>   <img src="README.assets/image-20221115200032610.png" alt="image-20221115200032610" style="zoom:67%;" />
>
>   -   和上上个例子相同的思路
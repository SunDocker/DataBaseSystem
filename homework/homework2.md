# 《数据库系统》课程第二次作业-函数依赖和模式分解

>   姓名：孙铎
>
>   学号：200110503

*一．设有关系模式 $R(A, B, C, D, E)$ ，其上的函数依赖集为：*
$$
F = \{A → C, B → AC, D → CE, AD → C\}
$$

1. *求 $R$ 的候选码。（1 分）*
2. *计算$(AD)^+$。（2 分）*
3. *求 $F$ 的最小函数依赖集。（2 分）*
4. *关系模式 $R$ 属于哪个范式？给出理由。（2 分）*
5. *将 $R$ 分解使其满足 $BCNF$ 且具有无损连接性。（2 分）*

解：

1.   记 $U=ABCDE$

     $\because B\rarr AC,D\rarr CE, B\rarr B, D\rarr D$

     $\therefore BD\rarr ABCDE$

     $\therefore $ 结合题意可知：$BD\overset f\rarr U$

     故 R 的候选码是 BD

2.   $\because A\rarr C,D \rarr CE$

     $\therefore AD\rarr CD,AD\rarr ACE$

     又 $\because$ $AD\rarr C, AD\rarr AD$

     $\therefore$ $(AD)^+=\{A,C,D,E\}$

3.   首先保证右部均为单个属性：

     $G=\{A\rarr C,B\rarr A,B\rarr C,D\rarr C,D\rarr E,AD\rarr C\}$

     然后进行第一轮检查：

     去除 $AD\rarr C$ 后，得到的依赖集与 $G$ 等价，因为由 $A\rarr C$（或 $B\rarr C$ ）可以推出 $AD\rarr C$。

     去除 $B\rarr C$ 后，得到的依赖集与 $G$ 等价，因为由 $B\rarr A$ 和 $A\rarr C$ 可以推出 $B\rarr C$。

     其他依赖直接去除后，均无法与原依赖集等价。

     所以令 $G'=\{A\rarr C,B\rarr A,D\rarr C,D\rarr E\}$

     $G'$ 中所有依赖的左端已经为单个属性，所以：

      $F$ 的最小函数依赖集为：$\{A\rarr C,B\rarr A,D\rarr C,D\rarr E\}$。

4.   R 中没有复合属性或多值属性，符合 1NF。

     R 的候选码为 BD，而 $BD\overset p\rarr CE$，所以不符合 2NF，因而也不符合 3NF 和 BCNF。

     所以关系模式 R 属于第一范式。

5.   令 $\rho=\{R\}$，算法求解过程为：

     $\rho=\{R\}$

     $=\{R_1(A,C),R_2(A,B,D,E)\}$

     $=\{R_1(A,C),R_2(A,B),R_3(B,D,E)\}$

     $=\{R_1(A,C),R_2(A,B),R_3(B,D,E)\}$

     $=\{R_1(A,C),R_2(A,B),R_3(D,E),R_4(B,D)\}$
     
     所以可将 $R$ 无损连接分解为 $\{R_1(A,C),R_2(A,B),R_3(D,E),R_4(B,D)\}$

---

*二．设有关系模式 R(A, B, C, D, E) ，其上的函数依赖为：*
*$F = \{A → D, E → D, D → B, BC → D, DC → A\}$*

1. *求 R 的候选码。（1 分）*
2. *判断 ρ = {AD, AB, BC, CDE, AE} 是否为无损连接分解？（5 分）*

解：

1.   设 U = ABCDE

     $\because E\rarr D$

     $\therefore CE\rarr D$

     $\because E\rarr D,D\rarr B$

     $\therefore E\rarr B$

     $\therefore CE\rarr B$

     $\because E\rarr D,DC\rarr A$

     $\therefore CE\rarr A$

     $\therefore CE\rarr CE$

     $\therefore CE\overset f\rarr U$

     故 R 的候选码是 CE

2.   令 $\rho=\{R_1(AD),R_2(AB),R_3(BC),R_4(CDE),R_5(AE)\}$

     构造 $R_\rho$ 表：

     |      |   A   |   B   |   C   |   D   |   E   |
     | :--: | :---: | :---: | :---: | :---: | :---: |
     | R~1~ | a~1~  | b~12~ | b~13~ | a~4~  | b~15~ |
     | R~2~ | a~1~  | a~2~  | b~23~ | b~24~ | b~25~ |
     | R~3~ | b~31~ | a~2~  | a~3~  | b~34~ | b~35~ |
     | R~4~ | b~41~ | b~42~ | a~3~  | a~4~  | a~5~  |
     | R~5~ | a~1~  | b~52~ | b~53~ | b~54~ | a~5~  |

     依次用 F 中的各依赖按规则修改表格：

     |      |   A   |  B   |   C   |  D   |   E   |
     | :--: | :---: | :--: | :---: | :--: | :---: |
     | R~1~ | a~1~  | a~2~ | b~13~ | a~4~ | b~15~ |
     | R~2~ | a~1~  | a~2~ | b~23~ | a~4~ | b~25~ |
     | R~3~ | b~31~ | a~2~ | a~3~  | a~4~ | b~35~ |
     | R~4~ | b~31~ | a~2~ | a~3~  | a~4~ | a~5~  |
     | R~5~ | a~1~  | a~2~ | b~53~ | a~4~ | a~5~  |

     没有一行全 a，所以 $\rho$ 不是无损连接分解












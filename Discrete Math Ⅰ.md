# 命题公式 
#####  1. 命题逻辑
   
|  p  |  q  |      与      |
|:---:|:---:|:------------:|
|  p  |  q  | $p \wedge q$ |
|  0  |  0  |      0       |
|  0  |  1  |      0       |
|  1  |  0  |      0       |
|  1  |  1  |      1       |
    
|  p  |  q  |     或     |
|:---:|:---:|:----------:|
|  p  |  q  | $p \vee q$ |
|  0  |  0  |     0      |
|  0  |  1  |     1      |
|  1  |  0  |     1      |
|  1  |  1  |     1      |

|  p  |  q  |      蕴含式      |
|:---:|:---:|:----------------:|
|  p  |  q  | $p\rightarrow q$ |
|  0  |  0  |        1         |
|  0  |  1  |        1         |
|  1  |  0  |        0         |
|  1  |  1  |        1         |

|  p  |  q  |        等价式        |
|:---:|:---:|:--------------------:|
|  p  |  q  | $p\leftrightarrow q$ |
|  0  |  0  |          1           |
|  0  |  1  |          0           |
|  1  |  0  |          0           |
|  1  |  1  |          1           |

##### 2. 等值式
1. 永假式 0,  $p \wedge \neg q$
2. 永真式 1,  $p \wedge (p\vee q) \leftrightarrow p$ 
  
 |  p  |  q  |     等价公式     |                 |                                                          |
 |:---:|:---:|:----------------:|:---------------:|:--------------------------------------------------------:|
 |  p  |  q  | $p\rightarrow q$ | $\neg p \vee q$ | $( p \rightarrow q) \Longleftrightarrow (\neg p \vee q)$ |
 |  0  |  0  |        1         |        1        |                            1                             |
 |  0  |  1  |        1         |        1        |                            1                             |
 |  1  |  0  |        0         |        0        |                            1                             |
 |  1  |  1  |        1         |        1        |                            1                             |
$\therefore$  $p \rightarrow q \Longleftrightarrow \neg p \vee q$

##### 3. 基本等值式
1. $\forall x (A (x) \vee B) \Longleftrightarrow \forall x A (x) \vee B$ 
2. $\forall x (A (x) \wedge B) \Longleftrightarrow \forall x A (x) \wedge B$
   
##### 4. 量词否定等式
1. $\neg \forall xA (x) \Longleftrightarrow \exists x \neg A (x)$
2. $\neg \exists xA (x) \Longleftrightarrow \forall x \neg A (x)$
   
# 集合
##### 1. 笛卡尔积分配率证明
$A*(B \cup C ) = (A*B) \cup (A*C)$
x, y 为有序对, 那么就意味着第一个元素属于第一个集合，第二个元素属于第二个集合
证明: $\forall<x, y>, <x, y> \in A*(B \cup C)$
$\Longleftrightarrow x \in A \wedge y \in (B \cup C)$
$\Longleftrightarrow x \in A \wedge (y \in B \vee y \in C)$
$\Longleftrightarrow (x \in A \wedge y \in B) \vee (x \in A \wedge y \in C)$
$\Longleftrightarrow (<x, y> \in A*B) \vee (<x, y> \in A * C)$
$\Longleftrightarrow <x, y> \in (A*B) \cup (A*C)$
$\therefore A*(B \cup C) = (A*B) \cup (B*C)$

##### 2. 合成运算结合律
1. Rule A: 
设 R1, R2, R3 为集合, 则 $(R_1 \circ R_2)\circ R_3 = R_1 \circ (R_2\circ R_3)$
证明: 
$\forall <x, y>, <x, y> \in (R_1 \circ R_2)\circ R_3$
$\Longleftrightarrow \exists z (xR_3z \wedge z (R_1 \circ R_2) y)$
$\Longleftrightarrow \exists z (x R_3z \wedge \exists t (zR_2t \wedge R_1ty))$
$\Longleftrightarrow \exists z \exists t (xR_3z \wedge (zR_2t \wedge R_1ty))$
$\Longleftrightarrow \exists z \exists t (xR_3z \wedge zR_2t \wedge R_1ty)$
$\Longleftrightarrow \exists t \exists z (xR_3z \wedge zR_2t \wedge R_1ty)$ -----> 开始反推
$\Longleftrightarrow \exists t (\exists z (xR_3z \wedge zR_2t) \wedge R_1ty)$
$\Longleftrightarrow \exists t (x(R_2 \circ R_3) t \wedge tR_1y)$
$\Longleftrightarrow xR_1 \circ (R_2 \circ R_3) y$
$\Longleftrightarrow <x, y> \in R_1 (R_2 \circ R_3)$
$\therefore (R_1 \circ R_2)\circ R_3 = R_1 \circ (R_2 \circ R_3)$

2. Rule B: 
设 F, G 为二集合，则
$(F \circ G)^{-1} = G^{-1} \circ F^{-1}$
证明:
$\forall <x, y>, <x, y> \in (F \circ G)^{-1}$
$\Longleftrightarrow <y, x> \in (F \circ G)$
$\Longleftrightarrow \exists z (yGz \wedge zFx)$
$\Longleftrightarrow \exists z (zG^{-1}y \wedge xF^{-1} z)$
$\Longleftrightarrow \exists z (xF^{-1}z \wedge zG^{-1}y)$
$\Longleftrightarrow <x, y> \in G^{-1} \circ F^{-1}$ 

##### 3. 二元关系
3. 二元关系符号
$<x, y> \in F \Longleftrightarrow x 与 y 具有 f 关系 \Longleftrightarrow xFy$, 
例如 2<15 $\Longleftrightarrow <(2, 15) \Longleftrightarrow <2, 15> \in <$

4. 自反性/反自反性
自反:  $\forall x (x \in A \longrightarrow xRx) \Longleftrightarrow (\forall x \in A) xRx$ 
反自反: $\exists x (x \in A \wedge \neg xRx)$ 
设 A＝｛1，2，3，4｝，下列几个是 A 上的二元关系。
R1={<1，1>，<1，2>，<2，1>，<2，2>，<3，4>，<4，1>，<4，4>}；
R2={<1，1>，<1，2>，<2，1>}；
R3={<1，1>，<1，2>，<1，4>，<2，1>，<2，2>，<3，3>，<4，1>，<4，4>}；
R4={<2，1>，<3，1>，<3，2>，<4，1>，<4，2>，<4，3>}；
R5=(<1，1>，<1，2>，<1，3>，<1，4>，<2，2>，<2，3>，<2，4>，<3，3>，<3，4>，<4，4>}；
R6={<3，4>}。
其中 R1, R2 包含 x, y 有序对，所以都不属于自反也不属于反自反, 
其中 R3, R5 包含 x, y 有序对，并且能够连续，所以属于自反
其中 R4, R6 不包含 x, y 有序对，所以属于反自反

5. 对称性/非对称性
R 是对称的 
$\Longleftrightarrow \forall x \forall y (x \in A \wedge y \in A \wedge xRy \longrightarrow yRx)$
$\Longleftrightarrow (\forall x \in A)(\forall y \in A)[xRy \longrightarrow yRx]$
R 是非对称的
$\exists x \exists y (x \in A \wedge y \in A \wedge xRy \wedge \neg yRx)$

6. 传递性
如果 a, b 是等价；b, c 又等价，那么我们可以肯定 a, c 等价，这也是等价应该满足的。和集合论语言描述就是 $(a, b) \in R \wedge (b, c) \in R \Longrightarrow (a, c) \in R$ 

7. 示例
反对称, 传递
$R_1={<a, a>, <a, b>, <b, c>,<a, c>}$
G ($R_1$): 
``` mermaid
graph LR;
	a-->a
	a-->b
	b-->c
	a--传递表现-->c
```
$R_2 ={<a, a>, <a, b>, <b, c>,<c, a>}$
反对称, 不传递
G ($R_2$):
``` mermaid
graph LR
	a-->a
	a--不传递表现, b到不了a-->b
	b-->c
	c-->a
```
$R_3={<a, a>, <b, b>, <a, b>,<b, a>,<c, c>}$
自反, 对称, 传递
G ($R_3$ ):
``` mermaid
graph
	a-->a
	b-->b
	a-->b
	b-->a
	c-->c
```
$R_4={<a, a>, <a, b>, <b, a>,<c, c>}$
对称
G ($R_4$):
``` mermaid
graph
	a-->a
	a-->b
	b-->a
	b.-这里不自反所以不传递.->b
	c-->c
```
$R_5={<a, a>, <a, b>, <b, b>,<c, c>}$
自反, 反对称, 传递
G ($R_5$):
``` mermaid
graph
	a-->a
	a-->b
	b-->b
	c-->c
```
$R_6={<a, a>, <b, a>, <b, c>,<a, a>}$
无任何性质
G ($R_6$):
``` mermaid
graph
	a-->a
	b-->a
	b-->c
	a-->a
```

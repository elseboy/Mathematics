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

##### 4. 关系幂运算
关系的 0 次幂就等于恒等关系
关系的 1 次幂就等于它自己
$$
\begin{cases}
R^0 = I_A \\
R^{n+1} = R^n \circ R (n \geq 0)  \\
\end{cases}
$$
例：
设 A=(a, b, c), $R \subseteq A*A$
R={<a, b>,<b, a>,<a, c>}, 求 R 的各次幂
$\because R^0 = I_A$, 其实说白了就只有环
G ($R^0$):
``` mermaid
graph
	a-->a
	b-->b
	c-->c
```
$\because R^1 = R$, 也就是只有它自己
G ($R^1$):
``` mermaid
graph
	a-->b
	b-->a
	a-->c
```
$R^2 = R \circ R = {<a, a>,<b, b>,<b, c>}$
从 a 出发到 b 又能回到 a, 合成的话就有 a, a, 所以 a 这里有环
从 b 出发到 a 又能回到 b, 合成的话就有 b, b, 所以 b 这里有环
从 b 出发到 c 就只有单边
G ($R^2$):
``` mermaid
graph
	a-->a
	b-->b
	b-->c
	a-.合成a,a.->a
	b-.合成b,b.->b
	b-.单边b,c.->c
```
$R^3 = R^2 \circ R = {<a, b>, <b , a>, <a, c>} = R^1$
相当于在关系 R 里面找长度为 3 的边 
a->b->a->c，b->a->b->a，a->b->a->b
G ($R^3$):
``` mermaid
graph
	a-->b
	b-->a
	a-->c
```
$\therefore$
$R^0 = I_A$
$R^{2k+1 （奇数次幂）} = R, k = 0, 1 , 2...$
$R^{2k （偶数次幂）} = R^2, k = 1 , 2...$

定理：
设 $R\subseteq A*A, m, n \in N$, 则：
	$R^m \circ R^n = R^{m+n}$
	$(R^m)^n = R^{m*n}$
证明：给定 m, 对 n 归纳
n=0 时，$R^m \circ R^0 = R^m \circ I_A = R^m = R^{m+0}$
假设 $R^m \circ R^n = R^{m+n}$, 则 
$R^m \circ R^{n+1} = R^m \circ (R^n \circ R^1) = (R^m \circ R^n) \circ R^1 = R^{m+n} \circ R = R^{(m+n)+1} = R^{m+(n+1)}$

##### 5. 关系闭包
必须要有三个性质: 
1. 包含给定的元素
2. 具有给定的性质
3. 是最小的二元关系 
	1. 求交就是最小
	2. 任意选取的集合都比给定的集合还大
自反闭包 r (R)
对称闭包 s (R)
传递闭包 t (R)
例:
R = { < a , b > , < b , a > , < b , c > , < c , d > }
最小也就是说自反

- 自反闭包：
G (r (R)):
``` mermaid
graph LR
	a-->b
	b-->a
	b-->c
	c-->d
	a.->a
	b.->b
	c.->c
	d.->d
```
也就是说对角线填 1 即可
M (r (R)): 

$$
\left[
\begin{matrix}
\textcolor{red}{1} & 1 & 0 & 0 \\
1 & \textcolor{red}{1} & 1 & 0 \\
0 & 0 & \textcolor{red}{1} & 1 \\
0 & 0 & 0 & \textcolor{red}{1} \\
\end{matrix}
\right]
$$

- 对称闭包：
G (s (R)):
``` mermaid
graph LR
	a-->b
	b-->a
	b-->c
	c-->d
	c.->b
	d.->c
```
也就是说主对角线对齐，对角线两边的值对称
M (s (R)):
$$
\left[
\begin{matrix}
0 & 1 & 0 & 0 \\
1 & 0 & 1 & 0 \\
0 & \textcolor{red}{1} & 0 & 1 \\
0 & 0 & \textcolor{red}{1} & 0 \\
\end{matrix}
\right]
$$
- 传递闭包
G (s (R)):
``` mermaid
graph LR
	a-->b
	b-->a
	b-->c
	c-->d
	a-.1.->a
	a-.2.->c
	a-.3.->d
	b-.4.->b
	b-.5.->d
```
也就是说只加长度为 2 的边
t (R) = $\textcolor{red}{R}  + \textcolor{red}{R^2}\ (R \circ R) + \textcolor{red}{R^3}\ (R^2 \circ R) + \textcolor{red}{R^4}\ (R^3 \circ R)$ 
$M (R)$ = 
$$
\left[
\begin{matrix}
0 & 1 & 0 & 0 \\
1 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 \\
\end{matrix}
\right]
$$

$m*n$ 得到
$M (R^2) = R \circ R$  = 
$$
\left[
\begin{matrix}
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
\end{matrix}
\right]
$$
$M (R^3) = R^2 \circ R$ = 
$$
\left[
\begin{matrix}
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
\end{matrix}
\right]
$$
$M (R^4) = R^3 \circ R = M (R^2)$ = 
$$
\left[
\begin{matrix}
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
\end{matrix}
\right]
$$
出现循环为止，然后将前面的相加或 $\vee$ 起来即可
即 $M (t (R)) = M (R) \vee M (R^2) \vee M (R^3)$ = 
$$
\left[
\begin{matrix}
\textcolor{red}{1} & \textcolor{red}{1} & \textcolor{red}{1} & \textcolor{red}{1} \\
\textcolor{red}{1} & \textcolor{red}{1} & \textcolor{red}{1} & \textcolor{red}{1} \\
0 & 0 & 0 & \textcolor{red}{1} \\
0 & 0 & 0 & 0 \\
\end{matrix}
\right]
$$
##### 6. 等价关系
A 上的自反，对称，传递的二元关系称为等价关系
设 R 为 A 上的等价关系，对于每个 $a \in A$, a 的等价类记作 $[a]_R$, 简记 $[a]$
例:
设 A={1, 2, 3, 4, 5, 8}, A 上的模 3 同余关系 $R_3=\{<x, y> | x, y \in A \wedge x \equiv (mod 3)\}$ 的等价类，则:
4 mod 3 = 1
$[1]=[4]=\{\textcolor{red}{1}, \textcolor{red}{4}\}$
``` mermaid
graph LR
	1-->4
	4-->1
	1-->1
	4-->4
```
$[2]=[5]=[8]=\{\textcolor{red}{2}, \textcolor{red}{5}, \textcolor{red}{8}\}$
``` mermaid
graph LR
	2-->2
	2-->5
	2-->8
	5-->2
	5-->5
	5-->8
	8-->2
	8-->5
	8-->8
```
$[3]=\{\textcolor{red}{3}\}$
``` mermaid
graph
	3-->3
```
以上对应的 A 的商集记作 $\textcolor{red}{A/R_3}=\{\{1, 4\},\{2, 5, 8\},\{3\}\}$
最小就是恒等关系 $\textcolor{red}{I_A}$，最大就是全域关系 $\textcolor{red}{E_A}$

##### 7. Stirling Approximation
1. Stirling 数计算公式 :
① S ( n , 0 ) = 0
② S ( n , 1 ) = 1
③ S ( n , 2 ) = $2^{n − 1}$ − 1
④ S ( n , n − 1 ) = C ( n , 2 )
⑤ S ( n , n ) = 1
2. Stirling 数递推公式 : 
S ( n , r ) = r S ( n − 1 , r ) + S ( n − 1 , r − 1 )
$$\left\{ 
	\begin{matrix} 
	n \\ 
	0 \\ 
	\end{matrix}
	\right\} = 0$$
一次性放进去一个盒子相当于全域关系
$$\left\{ 
	\begin{matrix} 
	n \\ 
	1 \\ 
	\end{matrix}
	\right\} = 1$$
分成两类，也就是/2，但是要除去全集合跟空集合
$$\left\{ 
	\begin{matrix} 
	n \\ 
	2 \\ 
	\end{matrix}
	\right\} = 2^{n-1} - 1$$
相当于说把两个元素放一块，比如 3 个苹果放 2 个篮子，篮子非空，怎么放都会变成 1, 23 或 12, 3
$$\left\{ 
	\begin{matrix} 
	n \\ 
	n-1 \\ 
	\end{matrix}
	\right\} = C^n_2
$$
相当于全域关系 $I_A$
$$\left\{ 
	\begin{matrix} 
	n \\ 
	n \\ 
	\end{matrix}
	\right\} = 0$$
先把一个元素挑出来放到一边，那么就剩 n-1 个元素，然后再去分成 k 类
由此可见:
$$\left\{ 
	\begin{matrix} 
	n \\ 
	k \\ 
	\end{matrix}
	\right\} = k*
	\left\{ \begin{matrix} 
	n-1 \\ 
	k \\ 
	\end{matrix}
	\right\} + 
	\left\{
	\begin{matrix} 
	n-1 \\ 
	k-1 \\ 
	\end{matrix}
	\right\}$$

- 球有编号 , 盒子没有编号 ( 不同的球放在相同盒子里 ) : 
	这是求<font color=green> 集合划分问题 </font>, Stirling 数 ; 这属于放球子模型 ;
- 球没有编号 , 盒子有编号 ( 相同的球放在不同盒子里 ) : 
	<font color=red>不定方程解问题 , 多重集组合问题 , 正整数剖分问题</font>;
- 球有编号 , 盒子有编号 ( 不同的球放在不同的盒子里 ) : 
	<font color=orange> 多重集排列 , 指数函数问题</font> ;


# 函数
#####  1. 单值的二元关系
单值: 
$\forall x \in dom F$,  $\forall\ y, z \in ran F$,  $xFy \wedge xFz \longrightarrow y = z$
$F (x) = y \Longleftrightarrow <x, y>\in F \Longleftrightarrow xFy$

1. 从 A 到 B 的<font color=red>偏函数</font>: 
   $dom F \subseteq A \wedge ran F\subseteq B$，也记作: $\color{red}{F:A \rightharpoonup B}$
   A 称为 F 的前域，B 称为 F 的后域
2. 从 A 到 B 的<font color=red>全体偏函数</font>:
   $A \longrightarrow B = \color{red}{\{F | F: A \nrightarrow B\}}$, 显然 $A \longrightarrow B \subseteq P (A*B)$
3. 从 A 到 B 的<font color = red>全函数</font>:
	$A \longrightarrow B = \{F | F: A \longrightarrow B\}$ = $\color{red} {B^A}$
4. 从 A 到 B 的真偏函数
	$dom F \subset A$, 也记作: $\color{red}{F: A \twoheadrightarrow B}$ = $A \twoheadrightarrow B = \{F | F: A \twoheadrightarrow B\}$

结论：
- $A \rightharpoonup B = A \longrightarrow B \ \cup A \twoheadrightarrow B$
- $F: A \rightharpoonup B \Longrightarrow F: domF \longrightarrow B$

##### 2.全函数性;质
单射：F 是单根的
满射：ranF = B
双射：一一对应，（1-1 mapping）
<font color = green>F 既是单射又是满射</font>

##### 3. 自然数的定义
封闭:
F 是 A 上的一元运算就是封闭
$f: N \longrightarrow N, f (x)=x+1$
A={0, 2, 4, 6, ...}在 f 下不封闭
B={1, 2, 3, 4, ...}在 f 下封闭

Peano 系统:
三元组<M, F, e>, $\{F \longrightarrow M\}$
- $e \in M$
- M 在 F 下封闭
- $e \notin ran F$
- F 是单射
- $A \subseteq M \wedge e \in A \wedge A$ 在 F 下封闭 $\Longrightarrow A=M$（极小性公理）
其中 3 跟 4 就会保证此曲线不会出现回环，也就是一直能持续下去
``` mermaid
graph LR
	e-->Fe
	Fe-->F2e
	F2e-->F3e
	F3e-->...
```

归纳集:
A 是归纳集 
$\Longleftrightarrow \varnothing \in A$
$\Longleftrightarrow \forall x (x \in A \longrightarrow x^+ \in A)$
A 是归纳集 $\Longleftrightarrow$ A 含有 $\varnothing$ 且对<font color=red>后继封闭</font>
- $0=\varnothing$
- $1=\varnothing^+ = \{\varnothing\} = \{0\}$
- $2=\varnothing^{++} = \{\varnothing, \{\varnothing\}\} = \{0,1\}$
- $3 = \varnothing^{+++} = \{\varnothing, \{\varnothing\}, \{\varnothing,\{\varnothing\}\}\} = \{1, 2, 3\}$
- $n = (n-1)^+ =\{0, 1, 2,..., n-1\}$

自然数集
自然数集是包含于每个归纳集的集合，每个归纳集有空集合
例：
N 是归纳集，证明 N= $\cap D = \cup\{ v | v 是空纳集\}$ = $\{x | \forall v (v 是归纳集 \longrightarrow x \in v)\}$
1). $\forall v, v 是归纳集\Longrightarrow \varnothing \in v$. $\ \ \therefore \varnothing \in N$
2). $\forall a, a \in N$
	$\Longrightarrow \forall v (v 是空纳集 \longrightarrow a \in v)$ (<font color=red>N 定义</font>)，
	$\Longrightarrow \forall v (v 是空纳集 \longrightarrow a^2 \in v)$ (<font color=red>归纳集定义</font>),
	$\Longrightarrow a^+ \in N$
	$\therefore \ N 对后继封闭$

##### 4. 自然数的性质


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

##### 2. Jiijhjs

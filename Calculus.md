##### 1. 集合基础
1. 对偶律
$\overline {A \cup B} = \mathop{\overline {A} \cap \overline {B}}$
![[Pasted image 20221211105259.png]]
$\overline {A \cap B} = \mathop{\overline {A} \cup \overline {B}}$
![[Pasted image 20221211105419.png]]

##### 2. 数列极限
数列极限求解：
- 直接代入法 (代入后有意义)：

有意义：
例： $\large {\lim\limits_{x \to 1}\ (2x^2 + x - 1)}$
$= 2 + 1 - 1$
$= 2$

无意义：
例： $\large {\lim\limits_{x \to 1}\ (\frac {2x} {x-1})}$
$=\large {\frac 2 0}$
$= \infty$
那么此时结果是无意义的，也就是说当分母为 0，分子不为 0 的时候，那么它的极限就是无穷
例： $\large {\lim\limits_{x \to \infty}\ (\frac {2} {x-1})}$
$=\large {\frac 2 \infty}$
$= 0$
上面这种也是无意义的，所以它的极限一般直接记作 0

- "$\frac 0 0$ 型"极限
1. 因式分解去零因子
例： $\large {\lim\limits_{x \to 1}\ (\frac {x^2 - 1} {X-1})}$
$=\large {\lim\limits_{x \to 1}\ (\frac {(x-1)(x+1)} {x-1})}$ 平方差公式
$= \large {\lim\limits_{x \to 1} (x +1)}$
$= 1 + 1$
$= 2$

2. 上下同乘一项构成平方差
例：$\large {\lim\limits_{x \to 0}\ (\frac {\sqrt{1+x}-\sqrt{1-x}} {2x})}$
$= \large {\lim\limits_{x \to 0}\ (\frac {(\sqrt{1+x}-\sqrt{1-x})(\sqrt{1+x}+\sqrt{1-x})} {2x(\sqrt{1+x}+\sqrt{1-x})})}$
$=\large {\lim\limits_{x \to 0}\ (\frac {{1+x}-{(1-x)}} {2x(\sqrt{1+x}+\sqrt{1-x})})}$
$=\large {\lim\limits_{x \to 0}\ (\frac {{2x}} {2x(\sqrt{1+x} + \sqrt{1-x})})}$ 
$=\large {\frac 1 2}$



##### 3. 函数极限
1. 如果左右极限有一个不存在的话那么此函数极限就不存在
2. 如果左右极限不相等那么此函数极限也不存在
无穷小：
无穷小乘以一个有界的数是无穷小

运算:
$\large {\frac {\infty} {\infty}}$
- 分子分母同次，最高次的系数之比
- 分母次数高，0
- 分子次数高，$\infty$
平方差公式
分子分母有理化
求和公式

<font color=red>重要公式总结</font>：
$\large {\frac {\infty} {\infty}}$ 型：
系数相等的时候直接分子比分母即可
小于的时候即是 0
大于的时候即是 $\infty$
$$
\left\{ 
	\begin{matrix} 
	\large {m = n, \frac{a_0}{b_0}}\\
	\large{m < n}, 0\\
	\large{m > n}, \infty 
	\end{matrix}
	\right\} = 0
$$



##### 4. 导数
1. 洛必达法则只有在 $\large{\frac {\infty} {\infty} \ \frac{0}{0}}$ 才可以使用
2. 等价替换优先，只有在乘法跟除法的时候才可以使用
3. 分离非零项，分离成两个极限公式相乘

反三角函数导数：
$\large{(arcsinx)' = \frac{1}{\sqrt{1-x^2}}}$
$\large{(arccosx)' = \frac{1}{\sqrt{1-x^2}}}$
$\large{(arctanx)' = \frac{1}{\sqrt{1+x^2}}}$
$\large{(arccotx)' = \frac{1}{\sqrt{1+x^2}}}$

常见导数公式：
$C' = 0$ C 为常数
$\large{(x^a)' = ax^{a-1}}$
$\large{(a^x)' = a^x lna}$
$\color{yellow}{\large{(e^x)' = e^x}}$
$\color{yellow}{\large{(sin\ x)' = cos\ x}}$ 极限为 1
$\color{yellow}{\large{(cos\ x)' = -sin\ x}}$
$\large{(tan\ x)' = sec^2 x}$
$\large{(cot\ x)'= -csc^2x}$
$\large{(sec\ x)' = sec\ x\ tan\ x}$
$\large{(\ln x)' = \frac{1}{x}}$
$\large{(csc\ x)' = - csc\ x\ cot\ x}$
$\large{ln (1+x)'趋于 0，导数为 \large{1+\frac{1}{1+x}}}$
$\color{green}{\large{(\sqrt{x})' = \frac{1}{2}}}$
$\color{green}{\large{((\sqrt{x})^2)' = x =1}}$ 
$\large {(tan x)' = sec^2 x}$
$\large {(cotx)' = csc^2x}$
$\large {(secx)' = secx * tanx}$
$\large{(cscx)' = cscx*cotx}$


- 如果结果为 $1^\infty$ 时，$\large{\lim\limits_{x \to ?}底数^{指数}= \lim\limits_{e^{x \to ?}}指数\times (底数-1)}$
- 如果结果为 $0\times \infty$ 时，直接把它转化成 $\frac{?}{?}$ 的形式即可
- 证明极限是否存在步骤是先求左极限然后求右极限，如果相等并不等于 $\infty$ 就存在极限
- $\large {\lim\limits_{\Delta \to 0}\ (\frac {f(X_0+\alpha\Delta)-f(X_0)} {\Delta}) = f'(X_0)\times \lim\limits_{\Delta \to 0} \alpha}$
- $\large {\lim\limits_{\Delta \to 0}\ (\frac {f(X_0+\alpha\Delta)-f(X_0+\beta\Delta)} {\Delta}) = f'(X_0)\times (\lim\limits_{\Delta \to 0} \alpha - \lim\limits_{\Delta \to 0} \beta)}$


X->0 时等价无穷小替换公式：
等价 X 本身的：
1. $\color{red}{\large {\sin x}}$
2. $\color{red}{\large {\tan x}}$
3. $\color{red}{\large {\arctan x}}$
4. $\color{red}{\large {\arctan x}}$
5. $\color{red}{\large {\ln(1+x)}}$
6. $\color{red}{\large {\ln (x+\sqrt{1+x^2} \sim x}}$
特殊型：
1. $\color{pink}{\large {1-cosx \sim \frac {1}{2} x^2}}$
2. $\color{pink}{\large {(1+x)^{\alpha} - 1 \sim \alpha \times x}}$
3. $\color{pink}{\large {a^x - 1 \sim x \times lna}}$
4. $\color{pink}{\large {e^x - 1 \sim x}}$



##### 5. 三角函数公式速记
- 积化和差公式：
$\large\boldsymbol{{\sin\alpha\times\cos\beta=\frac{\sin(\alpha+\beta)+\sin(\alpha-\beta)}{2}}}$
$\large\boldsymbol{{\cos\alpha\times\sin\beta=\frac{\sin(\alpha+\beta)-\sin(\alpha-\beta)}{2}}}$
$\large\boldsymbol{{\cos\alpha\times\cos\beta=\frac{\cos(\alpha+\beta)+\cos(\alpha-\beta)}{2}}}$
$\large\boldsymbol{{\sin\alpha\times\sin\beta=\frac{\cos(\alpha+\beta)-\cos(\alpha-\beta)}{2}}}$
正余余正、正加正减、余余正正、余加负余减
- 和差化积公式：
$\large\boldsymbol{{\sin\alpha+\sin\beta=2\sin\frac{\alpha+\beta}{2}\times\cos\frac{\alpha-\beta}{2}}}$
$\large\boldsymbol{{\sin\alpha-\sin\beta=2\cos\frac{\alpha+\beta}{2}\times\sin\frac{\alpha-\beta}{2}}}$
$\large\boldsymbol{{\cos\alpha+\cos\beta=2\cos\frac{\alpha+\beta}{2}\times\cos\frac{\alpha-\beta}{2}}}$
$\large\boldsymbol{{\cos\alpha-\cos\beta=-2\sin\frac{\alpha+\beta}{2}\times\sin\frac{\alpha-\beta}{2}}}$
正加正、正在前
正减正、余在前
余加余、余并肩
余减余、负正弦



##### 6. 不定积分

知道原函数，它的但函数是唯一的，比如$x^2 = 2x$
知道导函数，他的原函数是无穷的，比如$2x = x^2$，也可以是$x^2 + 5$或者任意一个常数C
所以：
$\int f(x) dx = F(x) + C$
其中dx为导数，$F(x)$为原函数，C为函数
不定积分性质：
$[\int f(x)dx]' = f(x)$
倍积函数：
$\int kf(x)dx = k \int f(x)dx = \int 3x^2dx =3\int x^2dx$





基本积分公式：
$\color{pink}{\large {\int \sin x dx = -cos x + C}}$ !
$\color{pink}{\large {\int \cos x dx = \sin x + C}}$ !
$\color{pink}{\large {\frac{1}{x}dx = \ln|x|+c}}$ !
$\color{pink}{\large {\int 0 dx = C}}$ !
$\color{pink}{\large {\int k dx = kx +C}}$
$\color{pink}{\large {\int x^a dx = x^{a+1} + C \ (a\neq -1)}}$ !
$\color{pink}{\large {\int a^xdx = \frac{1}{\ln a}a^x +C}}$
$\color{pink}{\large {\int e^x = e^x +  C}}$ !
$\color{pink}{\large {\int \sec x^2 dx = \tan x + C}}$
$\color{pink}{\large {\int \csc x^2 dx = -\cot x + C}}$
$\color{pink}{\large {\int \frac{1}{\sqrt {1 - x^2}}dx = \arcsin x+C}}$ !
$\color{pink}{\large {\int \frac{1}{1+x^2}dx = \arctan x + C}}$ !
$\color{pink}{\large {\int \sec x \tan x dx = \sec x+ C}}$
$\color{pink}{\large {\int \csc x \cot x dx = -\csc x+C}}$ 

固定技巧：
$(1 - x)^2 = x^2 - 2x +1$
$\large{x \sqrt {x} = x^{\frac{3}{2}}}$

			
积分法：
$\color{pink}{\large {\cos()d() = \sin() + C \sim \cos(x^2)d(x^2) = \sin(x^2) + C}}$
第一换元积分法:
1）吧 d 外面的某项拿到 d 里面去（变成原函数）
第二换元积分法：
1）把 d 里面的函数往外拿到 d 外面去（求导数）
分步积分法：
$\large{\int udv = uv - \int vdu}$


##### 7. 微积分基本原理
基本定理：
$\color{pink}{\large {p (x)= \int_{a}^{x} f(t)dt, \ x \in [a,b]; \ p(x)=f(x)}}$
1）如果上限是 x，那么直接将 x 可以代入被积函数
例：
- $\color{orange}{\Large {(\int_{-1}^{x} \sin t^3\ dt)' = \sin x^3}}$
2）如果下线是 x，那么交换上下限需要在 $\int$ 前面加-
例：
- $\color{orange}{\Large {(\int_{x}^{5} \cos t\ dt)' = (-\int_{5}^{x} \cos t dt )' = -\cos x}}$
3）如果上限是 $x^2$, 那么使用复合函数求导并代入即可
例：
- $\color{orange}{\Large{(\int_{1}^{x^2}\sin t\ dt)' = \int_{u(2x)}^{1} \sin u \times 2x}}$
4）如果下限是 $x^2$, 那么使用复合函数求导并代入再加-
例：
- $\color{orange}{\Large{(\int_{x^2}^{x}\sin t\ dt)' = -(\int_{u(2x)}^{1} \sin u \times 2x)}}$
5）如果上限是 $g(x)$, 下限是 $h(x)$,
例：
- $\color{orange}{\Large{[\int_{h(x)}^{g(x)}f(t)\ dt]' = f(g(x))\times g(x)' - f(h(x)) \times h(x)'}}$

###### 牛顿莱布尼茨公式 :
$\color{orange}{\Large{\int_{a}^{b}f (x)\ dx = F (x)|_{a}^{b} = F (b) - F(a)}}$


##### 8. 定积分
$\color{orange}{\Large{\int_{0}^{a}\sqrt{a^2 - x^2}\ dx = \frac{1}{4}\pi a^2}}$


##### 9. 广义积分


##### 10. 多远函数微积分
开集：不包含边界点
闭集：包含边界点以及内点

##### 11. 偏导数
对 x 求导时，把 y 看做常数不变
$\color{orange}{\Huge {\lim\limits_{\Delta x \to 0}\frac{\varDelta_x Z}{\varDelta x} = \lim\limits_{\Delta x \to 0}\frac{f(x_0+\varDelta x \times y_0)-f(x_0 \times y_0)}{\varDelta x}}}$
对 y 求导时，把 x 看做常数不变
$\color{orange}{\Huge {\lim\limits_{\Delta y \to 0}\frac{\varDelta_y Z}{\varDelta y} = \lim\limits_{\Delta y \to 0}\frac{f(x_0 \times y_0 + \varDelta y)-f(x_0 \times y_0)}{\varDelta y}}}$

##### 12. 全微分
偏导数是 x 或者 y 发生变化而引起 Z 的变化
全增量是想 x, y 同时发生变化而引起 z 的变化
全增量公式：
$\color{orange}{\Huge {\Delta Z = f(x+\varDelta x, y+\varDelta y)- f(x,y)}}$

##### 13.  二重积分
计算公式：
X 型： 
$\color{orange}{\Huge {\iint \limits_{D}f(x,y)\ dx\ dy = \int_{a}^{b}dx\int_{1(x)}^{2(x)}f(xy)dy}}$

##### 14. 无穷积数







  




























































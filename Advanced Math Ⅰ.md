# 实数与运算G
---

## Summary
1. 用科学计数法表示一些数位较多的数字 x 时, 一般写成 $\underline{a * 10^n}$ 的形式, 其中$1\leq|a|<10$, |n| 为小数点移动的位数, 当$|x| \geq 1$ 时, n 是$\underline{正整数}$, 当|X|<1 时, n 是$\underline{负整数}$
    - 比如：120000=$\underline{1.2*10^5}$ , 0.0012= $\underline{1.2*10^{-3}}$ , 0.0000146=$\underline{1.46*10^{-5}}$
2. $\sqrt{a^2}$=$\pm{a}$, 也就是|a|, 因为正数的绝对值是它本身, 而负数的绝对值是它的相反数
3. 平方差公式 $a^2$-$b^2$=(a+b)(a-b), 完全平方公式 $a^2$+2ab+$b^2$=$(a+b)^2$
4. 映射 map
    1. 按<font color=red>法则</font> f 使 X 中的每个元素与 Y 中映射记作：$f: X \rightarrow Y$
    2. 集合 X 称为映射 f 的<font color=red>定义域</font>记作：$D_{f}$即$D_{f}=X$
    3. X 中所有元素所组成的集合称为映射 f 的<font color=red>值域</font>记作：$R_{f}$或 f(x)或 $R_{f}$=f(x)={f(x) | $x\in X$}
    4. 构成映射的三要素：
        1. 集合 X, 即定义域$D_{f}=X$;
        2. 集合 Y, 即值域的范围, $R_f$ $\subset Y$;
        3. 对应法则 f, 使得每个$x\in X$, 有唯一确定的 y=f(x)与之对应；
    5. 只有单射才有<font color=red>逆映射</font>并记作：$f^{-1}$, 一般记作：$g: R_f \rightarrow X$
    6. 复合映射：
        1. 设有两个集合：$g: X\rightarrow Y1$, $f: Y2\rightarrow Z$, 其中$Y1\subset Y2$, 则由映射 g 和 f 可以定义出一个从 X 到 Z 的映射, 这个便称为映射 g 和映射 f 的<font color=red>复合映射</font>并记作：$f\circ g$, 既$f\circ g: X\rightarrow Z$, $(f\circ g)(x)=f[g(x)]$, $x\in X$
        2. 映射 f 和 g 构成的复合映射的前提：
            1. 映射 g 的值域$R_g$必须包含在映射 f 的定义域$D_f$之内, 既$R_g \subset D_f$
            2. 映射 g 和 f 的复合是有顺序的, $f\circ g$有意义并不代表$g\circ f$有意义
5. 函数
    1. 函数就是由一个变量 x 与常数构成的任意表达式, 成为 x 的函数, 列如 f(x)=x, f(x)=$x^2$, f(x)=$2^x$, f(x)=$e^x$, f(x)=$sin^x$, 等号的右侧就是由一个变量 x 与常数构成的表达式；其实还有一种隐函数 f(x, y)=0, 比如$x^3+2y+x^2-x^4=0$就是一个隐函数
    2. 函数界限：
        1. $\exists$$k_1$, 如果给定是上界$k_1$, 也就是说$f(a)\leq k_1$, 所有所有比它大的数都属于上界也就是无穷的
        2. $\exists k_2$, 如果给定是下界$k_2$, 也就是说$f(a) \geq k_2$, 所以所有比它小的数都属于下界也就是无穷的
        3. 有界: 如果有正数 $\exists M$, 并且$|f(x) \leq M$, 那么它就是有界函数
        4. 无界: 如果有 $\forall 正数 M$, 并且 $\exists x_1 \in X$, |$f(x_1)$|<M, 那么它就是无界函数
        5. 奇偶函数例题
            ![[Drawing 2022-10-27 23.33.49.excalidraw|600|center]]
6. 数列：
	1. 收敛数列也叫存在极限，发散数列也叫不存在极限
# 图论
##### 1. 无序积
A&$B = \{\{a, b\}\} | x \in A \wedge y \in B$
- 记{a, b}=(a, b)
- 允许 a = b
- (a, b) = (b , a)

##### 2. 有向图跟无向图
有向图 D=<V, E>
- V 不能为 $\emptyset$, 顶点集为 V (D)
- E $\subseteq V*V$, 边集（多重集）E (D)
例: D=<V, E>
V={a, b, c, , d, e}, E={<a, a>,<a, b>,<a, b>,<b, a>,<b, c>,<c, d>,<d, b>}
``` mermaid
graph LR
	a-->a
	a-->b
	a-->b
	b-->a
	b-->c
	c-->d
	d-->b
```
无向图的连通度
- 破坏连通性
p (G-V') > p (G)
G-V' 表示从图 G 中删除结点集合 V' 中的所有结点以及这些结点关联的所有边，既：
删除极小<font color=red>点割集并保证极小性的条件</font>即可
p (G-E') > p (G) 删除一组边
G-E' 表示从图 G 中删除边的集合 E'中的所有边
删除全部的边割集里的边使得被删除后的<font color=red>图的联通分支数变大</font>

# 欧拉图
sss

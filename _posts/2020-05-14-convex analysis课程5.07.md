---
layout:     post
title:      Convex analysis 5.07
subtitle:   硕士课程
date:       2020-05-14
author:     WC
header-img: img/con set.png
catalog: true
tags:                               #标签
    - convex analysis


---

# Convex analysis 5.07

- ## 分离定理

非空闭凸集$$S \subseteqq R^n$$中与点$$x \in R^n$$距离最近的点称为$$x$$在$$S$$上的投影，记为$$Ps(x)$$，即$$Ps(x)$$为$$S$$中满足如下条件的点：


$$
\Vert x-Ps(x)\Vert = min\{\Vert x-z \Vert |z \in S\}
$$


显然，若$$x \in S$$，则有$$x = Ps(x)$$。

- ## 非扩张性质

下面的定理揭示了任意两点间的距离不因到闭凸集上的投影而扩大.这意味着，当把投影$$Ps$$看作从$$R^n$$到$$R^n$$的映射时，它具有所谓的**非扩张**性质.

设$$S \subseteqq R^n$$为非空闭凸集，则有下式成立：


$$
\Vert Ps(x)-Ps(y) \Vert \leqq \Vert x-y \Vert   \qquad(x,y \in R^n)
$$




- ## 分离超平面

给定非空凸集$$S \subseteqq R^n$$与点$$x \notin cl S$$，则必存在$$S$$与$$x$$的分离超平面$$H=\{ y= R^n|\langle a，y \rangle =a \}$$使得


$$
\langle a,z \rangle \geqq \alpha > \langle a,x \rangle     \qquad(z \in S)
$$


上式意味着$$S \subseteqq H^+$$, 而$$x \in H^-$$，此时也称超平面H严格分离$$S$$与$$x$$ 。

<img src="https://i.loli.net/2020/05/15/X3aR64FtSLfowx1.png" alt="Hyperplane.png" style="zoom:150%;" />

若凸集$$S \subseteqq R^n$$包含于由超平面$$H$$定义的半空间$$H^+$$或$$H^-$$，而点$$x \in clS$$在$$H$$上，则称$$H$$为$$S$$在$$x$$处的支撑超平面（如图2.7）依照定义，$$S$$在$$x$$处的支撑超平面是$$S$$与$$x$$的分离超平面的特殊情形。

- ## 凸多面体到凸多面集

由给定点$$x^0,x^1,…,x^m \in R^n$$的所有凸组合构成的集合


$$
S=\left\{\boldsymbol{x} \in \boldsymbol{R}^{n} | \boldsymbol{x}=\sum_{i=0}^{m} \alpha_{i} \boldsymbol{x}^{j}, \sum_{i=0}^{m} \alpha_{i}=1, \alpha_{i} \geqq 0(i=0,1, \ldots, m)\right\}
$$


称为**凸多面体**.若凸多面体$$S$$中的$$m$$个向量$$x^0, x^1,....., x^m - x^0$$线性无关，则称$$S$$为**$$m$$维单纯形**，对应的：$$x^0，x^1,...,x^m$$则称为$$S$$的**顶点**.

由$$x^0,x^1,…,x^m \in R^n$$的凸组合与$$y^1,…,y^l \in R^n$$的非负线性组合的和的全体构成的集合


$$
\begin{array}{c}
S=\left\{\boldsymbol{x} \in R^{n} | \boldsymbol{x}=\sum_{i=0}^{m} \alpha_{i} \boldsymbol{x}^{j}+\sum_{j=1}^{l} \beta_{j} \boldsymbol{y}^{j}, \sum_{i=0}^{m} \alpha_{i}=1\right. \\
\left.\alpha_{i} \geqq 0(i=0,1, \ldots, m), \beta_{j} \geqq 0(j=1, \ldots, l)\right\}
\end{array}
$$



称为**凸多面集**.凸多面集也可以定义为有限个半空间的交集，它是凸多面体的推广。



## 锥与极锥

满足下述条件的集合$$C \in R^n$$称为**锥**：


$$
x \in C, \quad \alpha \in [0,\infty ) \quad\Longrightarrow \quad \alpha x \in C
$$


亦即锥$$C$$是包含所有以原点$$x=0$$为始点并通过$$C$$中一点的射线的集合.依照定义，非空锥通常包含原点.当锥是凸集时称为**凸锥**，是闭集时则称为**闭锥**，既是闭集又是凸集的锥称为**闭凸锥**.

<img src="https://i.loli.net/2020/05/15/P7Rvq2QwxZrUA3L.png" alt="极锥.png" style="zoom: 150%;" />

对任意锥$$C \subseteqq R^n$$，考虑由下式定义的集合$$C^* \subseteqq R^n$$：


$$
C^*=\{ y \in R^n | \langle y,x \rangle \leqq 0(x \in C) \}
$$


这是由与$$C$$中每个向量都保持$$90°$$以上夹角的向量全体构成的集合，因此显然是锥（如图2.9）.称$$C^*$$为$$C$$的**极锥**.特别，若$$C$$是线性子空间，则$$C^*$$恰为与$$C$$正交的线性子空间，亦即$$C^*$$与$$C$$的正交补空间$$C^ \bot$$一致.

- ## Farkas定理

Farkas定理在推导非线性规划问题的最优性条件时起着重要作用。

考虑由向量$$a^1,…, a^m \in R^n$$生成的闭凸多面锥


$$
C=\left\{\boldsymbol{x} \in \boldsymbol{R}^{n} | \boldsymbol{x}=\sum_{i=1}^{m} \alpha_{i} \boldsymbol{a}^{i}, \alpha_{i} \geqq 0(i=1, \ldots, m)\right\}
$$




以及与每个$$a^i$$都保持$$90°$$以上夹角的向量全体形成的闭凸多面锥


$$
K=\left\{\boldsymbol{y} \in \boldsymbol{R}^{n} |\left\langle\boldsymbol{a}^{i}, \boldsymbol{y}\right\rangle \leqq 0(i=1, \ldots, m)\right\}
$$


则$$K=C^*$$并且$$C=K^*$$.



**Some Tips:** 

1. 凸集的并不一定是凸集，凸集的交一定是凸集
2. 闭凸锥的并集不一定是闭凸锥
3. 任意并集的闭集一定是闭集
4. 任意非空锥的极锥一定是闭凸锥
5. 欲证两集合相等，可证互为包含关系。



- ## 作业

复习本科高数（数分）知识。


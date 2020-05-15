---
layout:     post
title:      Convex analysis 4.30
subtitle:   硕士课程
date:       2020-05-07
author:     WC
header-img: img/con set.png
catalog: true
tags:                               #标签
    - convex analysis

---

# Convex analysis 4.30

- ## 线性子空间

设$$W$$为空间$$R$$的子集，记为$$W$$$$\subseteq$$ $$R^n$$.若对任意向量$$x,y\in W$$以及任意$$\alpha \in R$$总有$$x+y \in W$$及$$\alpha x \in W$$成立，则称$$W$$为线性子空间（subspace）.若$$W$$可表示为



$$
W = \{x \in R^n|x=\alpha_1x^1+···\alpha_kx^k,\alpha_1 \in R,···,\alpha_k \in R\}
$$



即$$W$$为向量$$x^{1} ,···, x^k \in R^n$$的全体线性组合构成的集合，则称张成$$x^{1} ,···, x^k$$线性子空间$W$.线性子空间$$W$$中含有的线性无关向量的最大个数称为$$W$$的维数(dimension)
线性子空间的具体例子包括二维空间（平面）中过原点的直线，以及三维空间中过原点的平面或者直线等.再有，空间$$R^n$$本身与只含有零向量的集合$$\{0\}$$也可看成是特殊的线性子空间.此外，二维空间中的任意直线以及三维空间中的任意平面。

- ## 仿射集

集合$$C \subset R^n$$称为仿射集(affine set)，若对任意的$$x1,x2 \in C$$及$$\theta \in R$$，有


$$
\theta x_1 + (1-\theta)x_2 \in C.
$$


A set $$C \in R^n$$is affine if the line through any two distinct points in $$C$$ lies in $$C,i.e$$., if for any $$x_1, x_2, \in C$$, and $$\theta \in R$$, we have $$\theta x_1 + (1-\theta)x_2 \in C.$$ 

从几何上看，过仿射集上任意两个相异的点的直线都包含在该集合内。（过两点直线表示形式可由直角坐标小推导）

- ## 仿射集例子

仿射集的例子：

1.空集、单点集、直线、平面、$$R^n$$；

2.线性子空间（零点一定在内）;

3.线性方程组的解集:


$$
\{x| Ax=b\}（Solution set of linear equations\{x|Ax=b\};
$$


4.超平面:


$$
\{x|a^T x = \beta\}
$$


- ## 仿射组合

设$$x_1, x_2, ···, x_k \in R^n$$。当$$\theta_1 + \theta_2 + ··· + \theta_k = 1$$时，线性组合


$$
\theta_{1} x_{1}+\theta_{2} x_{2}+\cdots+\theta_{k} x_{k}
$$


称为$$x_{1}, x_{2}, \cdots, x_{k}$$的仿射组合（affine combination）。

- ## 仿射无关

点集$$\{x_0, x_1···, x_m\} \subset R^n$$称为仿射无关的，如果其仿射包的维数为$$m$$。
点集$$\{x_0, x_1···, x_m\} \subset R^n$$仿射无关当且仅当$$x_1 - x_0, ···, x_m - x_0$$线性无关。

- ## 凸集定义

集合$$C \subset R^n$$称为凸集（convex set）, 若对任意的$$x_{1}, x_{2} \in C$$及$$\theta \in [0,1]$$,有


$$
\theta x_{1}+(1-\theta) x_{2} \in C
$$


从几何上看，以四集上任意两个相异的点为端点的线段都包含在该集合内。

- ## 凸集例子

![未命名1588848511.png](https://i.loli.net/2020/05/07/DoNeMJlvj5EfbXQ.png)

1.线段；

2.仿射集；

3.半空间


$$
\{x|a^T x \le \beta\}、\{x|a^T x < \beta\}；
$$


4.任意范数下的球:


$$
\begin{array}{l}
B\left(x_{0}, r\right):=\left\{x |\left\|x-x_{0}\right\| \leq r\right\} \\
U\left(x_{0}, r\right):=\left\{x |\left\|x-x_{0}\right\|<r\right\}
\end{array}
$$



- ## 凸组合定义

设$$x^1, x^2, ···, x^k \in R^n$$。当$$\theta_1 + \theta_2 + ··· + \theta_k = 1$$时，线性组合


$$
\theta_{1} x^{1}+\theta_{2} x^{2}+\cdots+\theta_{k} x^{k}
$$


称为$$x^{1}, x^{2}, \cdots, x^{k}$$的凸组合（convex combination）。

凸集内任意有限个点的凸组合都在凸集内。

- ## 凸包定义

设集合$$C \in R$$，称包含$$C$$的最小凸集为$$C$$的凸包（convex hull），记为$$coC$$。

- ## 卡西拉莫多引理

设点$$x \in R^n$$为$$m$$个点$$x^1, ···，x^m \in R^n$$的凸组合，若$$m \ge n+2$$，则可以从$$x^1, ···，x^m$$中选出至多$$n+1$$个点，使得$$x$$可以表示为这些点的凸组合.

- ## 卡西拉莫多定理

设点$$x \in R^n$$为$$m$$个点$$x^1, ···，x^m \in R^n$$的凸组合，若$$m \ge n+2$$，则可以从$$x^1, ···，x^m$$中选出至多$$n+1$$个点，使得$$x$$可以表示为这些点的凸组合.

下列两种表述等价：
（1）任意集合$$S \subset R^n$$的凸包$$coS$$等同于由$$S$$中至多$$n+1$$个点的凸组合的全体构成的集合。
（2）设集合$$S \subset R^n$$，则对任意点$$x \in coS$$，存在$$S$$中的至多$$n+1$$个点$$x^0,x^l,···,x^m(m≤n)$$使得$$x \in co\{x^0，x^1, ···, x^m\}$$。



- ## 作业

定理：$$R^n$$中有界闭集的凸包依旧是有界闭集。

试证明：当$$S$$有界时，$$cl co S = co cl S$$

其中$$cl$$为闭包简写，$$co$$为凸包简写。


---
title: 2. 代价函数
date: 2022/04/05 20:12:21
tags:
 - linear regression
 - one variable
categories:
 - machine learning
---

::: tip 参考视频: 

2 - 2 - Cost Function (8 min).mkv

:::

## 2.1 代价函数的引入

Training Set

| Size   in feet2 (x) | Price   ($) in 1000's (y) |
| ------------------- | ------------------------- |
| 2104                | 460                       |
| 1416                | 232                       |
| 1534                | 315                       |
| 852                 | 178                       |
| …                   | …                         |

Hypothesis:    $h_\theta \left( x \right)=\theta_{0}+\theta_{1}x$

Parameters：$\theta_{0}$ ， $\theta_{1}$

通过上一节，我们知道了，我们**要完成**朋友的需求（**根据他房子的大小预测房价**），就**需要知道**假设函数    $h$，我们也对    $h$     做出这样一种假设：$h_\theta \left( x \right)=\theta_{0}+\theta_{1}x$。通过观察这个函数，我们可以把这个问题转化为求$\theta_{0}$ 和 $\theta_{1}$，从而当你朋友把房子大小告诉你，你将其代入公式即可得到预测的房价。那么，我们如何选择呢$\theta_{0}$ 和 $\theta_{1}$？

首先，我们先直观理解$h_\theta \left( x \right)$ ---下图是$\theta_{0}$ 和 $\theta_{1}$取不同值时，$h$的整体图像。

![1_2_1_figure_of_h](/assets/img/1_2_1_figure_of_h.png)
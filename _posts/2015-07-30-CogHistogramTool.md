---
layout: post
title: "CogHistogramTool"
date: 2015-07-30 22:03:51
postid: post0730
categories: [notes]
tags: [Vision Pro]
published: True
comments: True

---

**工具介绍**

柱状图是建立图像指定区域内所找到的灰度值的统计数字及平面线图。柱状图是在整个图像中以每种可能的像素浓度(X轴)对图像像素(Y轴)计数的平面图。沿X轴每个像素浓度位置上图形的高度表明工具中具有该浓度的区域中像素的数量。X轴位置可以表示浓度组,而不是单个浓度。

<!--more-->

![histogramtool](http://i3.tietuku.com/7b4070b9511c7042.png)

**用途**

- 探测图像中是否存在某物
- 监视光源的输出
- 软件测光仪
- 测量图像内灰度值是否一致
- 决定图像中的灰度值分布，以便设置其他视觉对象

**关注区域**

默认状态下,柱状图在整个图像上运行，为了分析图像的单个区域,选择一个区域形状并且在`Current.InputImage`上操纵。

![histogramtool](http://i3.tietuku.com/4723e6073556085f.png)

![histogramtool](http://i3.tietuku.com/27efde479297c198.png)

**图形**

可选项,更改在运行时显示的图形

![histogramtool](http://i3.tietuku.com/64e51f4d3a22906c.png)

**结果**

结果显示在控件和浮动结果表格中，也可在VB或者C语言代码中访问

![histogramtool](http://i3.tietuku.com/aefd9d296c213fe9.png)

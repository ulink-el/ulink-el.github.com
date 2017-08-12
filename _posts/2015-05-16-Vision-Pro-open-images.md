---
layout: post
title:  "Vision Pro 打开本地图片"
postid: post0516
date:   2015-05-16 02:00:11
tags: [Vision Pro, VB.NET]
categories: [Code]
comments: ture
---
在 Vision Pro 的vpp作业中添加 cogImageFileTool 工具，并添加引用到 form 中。

<!--more-->

{% highlight vb.net linenos %}

imports cognex.visionpro.cogImageFileTool

{% endhighlight %}

使用 cogImageFileTool 可以将本地图片作为图片源.

> cogImageFileTool.[Operator].Open(图片地址,CogImageFileModeContents.Read)

示例代码：
{% highlight vb.net linenos %}

'用 ImageTool 打开图片的函数
mImageFileTool.[Operator].Open(mImagePath, CogImageFileModeConstants.Read)

'将图像显示在 mToolDispaly 的方法
mToolDisplay1.Tool = mBarcodeTool
mToolDisplay1.SelectedRecordKey = "LastRun.InputImage"

{% endhighlight %}

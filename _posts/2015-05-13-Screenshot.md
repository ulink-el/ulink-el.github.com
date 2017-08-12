---
layout: post
title:  "VB.NET Screenshot"
postid: post0513
date:   2015-05-13 22:23:43
tags: [VB.NET]
categories: [Code]
comments: ture
---
调用外部工程函数。对当前显示屏幕进行截屏并保存。

<!--more-->

{% highlight vb.net linenos %}

Imports Cognex.VisionPro.ImageProcessing
Imports System.Runtime.Serialization.Formatters.Binar

Public Declare Function ClipCursor Lib "user32" Alias "ClipCursor" (ByRef rec As System.Drawing.Rectangle) As Long

Dim Begin_Record As Boolean
Dim Digital_Click As String

Private Sub SaveImage()
  Dim Bit1 As Bitmap = New Bitmap(Me.CogDisplay1.Width, Me.CogDisplay1.Height)
  Me.CogDisplay1.DrawToBitmap(Bit1, New Rectangle(0, 0, Me.CogDisplay1.Width, Me.CogDisplay1.Height))

  'Dim Border As Integer = (Me.gbx_Image_Display.Width - Me.gbx_Image_Display.ClientSize.Width) / 2 '边框宽
  'Dim caption As Integer = (Me.CogDisplay1.Height - Me.CogDisplay1.ClientSize.Height) - Border '标题栏高度

  Bit1.Save("C:\\错误图片.jpg", System.Drawing.Imaging.ImageFormat.Jpeg) '不包括标题栏和边框
  Bit1.Dispose()

End Sub

{% endhighlight %}

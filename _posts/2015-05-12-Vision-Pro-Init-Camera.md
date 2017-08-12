---
layout: post
title:  "Vision Pro 初始化相机"
postid: post0512
date:   2015-05-12 00:56:13
tags: [Vision Pro, VB.NET]
categories: [Code]
comments: ture
---

**先用GetFifoState获取AcqFifoTool的状态.**

<!--more-->

{% highlight vb.net linenos %}
void GetFifoState(
    out Int32& numPending,
    out Int32& numReady,
    out Boolean& busy
)
{% endhighlight %}

*numPending/挂起状态数*

>  The number of acquisitions in the pending state.
>  This is the number of acquisitions requested by StartAcquire for which acquisition has not started.
>  To achieve frame rate acquisition in manual trigger mode,
>  the FIFO must always have one or more pending acquisitions.
>
>  获取的挂起状态的数量.
>  这是获取由StartAcquire为其获取尚未开始请求的数目.
>  以实现帧速率采集在手动触发模式中,FIFO始终有一个或多个待决获取.

*numReady/准备完成数*

>  The number of acquisition requests ready to be completed.
>
>  获取请求准备完成的数量.

*busy/状态*

>  True if the oldest outstanding acquisition is waiting for a trigger signal or is acquiring an image.
>  For master/slave acquisitions,
>  it becomes true only after the master and all slaves are ready for acquisition.
>
>  如果最早的突出获取正在等待一个触发信号或获取图像则busy为True.
>  对于主/从获取,只有主和所有从都准备好后被获取时它才变为True.

##### 判断各状态参数的值,获取图片到CogDisplay1

[谷歌翻译]
完成由给定的票券中指定的获取和返回所获取的图像.如果票证被省略,或设置为-1,未完成的获取被至少最近开始将完成.

> CompleteAcquire(
>               out Int32 requestedTicket,
>               out Int32& ticket,
>               out Int32& triggerNumber
> )
>
> 返回值为图像

*requestedTicket*

> The ticket of an outstanding acquisition.
> This is usually a value returned by StartAcquire.
> If this value is omitted or set to -1, the oldest outstanding acquisition is completed.
> requestedTicket must be -1 for automatically triggered acquisitions.
>
> 一个优秀的收购票.这通常是通过StartAcquire返回的值.
> 如果这个值被省略或设置为-1,最古老的杰出收购完成.
> requestedTicket必须为-1自动触发并购.

*ticket*

> The actual ticket of the completed acquisition.
> When requestedTicket is not -1, this value is the same as requestedTicket.
>
> 在完成收购的实际门票.
> 当requestedTicket不是-1,则该值是相同的requestedTicket.

*triggerNumber*

> The trigger sequence number of the completed acquisition.
> You can compare this value with Trigger value returned by Acquire to see if there were missed triggers.
>
> 在完成收购的触发顺序号.
> 你可以比较这个值与采集返回触发值,看是否有遗漏的触发器.

完成相机初始化,相机的运行由触发模式决定(自动/硬件触发).

示例代码:
{% highlight vb.net linenos %}

'mAcqFifo 为定义的 cogAcqFifoTool 工具
Dim numReadyVal, numPendingVal, myTicket, currentTrigNum As Integer
Dim busyVal As Boolean
Try
    mAcqFifo.GetFifoState(numPendingVal,numReadyVal,busyVal)
    If(numReadyVal > 0)Then
        Me.CogDisplay1.Image = mAcqFifo.CompleteAcquire(-1,myTicket,currentTrigNum)
        Me.CogDisplay1.Fit()
    EndIf
    numacqs + = 1
    If ckb_Run.Checked Then
        run()
    EndIf
    If numacqs < 4 Then
        GC.Collect()
        numacqs =0
    EndIf
Catch As CogException
Catch As Exception

EndTry

{% endhighlight %}

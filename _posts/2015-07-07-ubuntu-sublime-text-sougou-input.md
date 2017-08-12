---
layout: post
title: Ubuntu中Sublime Text 3中文输入解决方法
date: 2015-07-07 21:27:22
postid: post070701
categories: [Method]
tags: [Sublime Text, Ubuntu]
comments: true
published: True

---

本文整理自百度经验，作者[LunnLew](http://jingyan.baidu.com/user/npublic?un=LunnLew)，[原文链接](http://jingyan.baidu.com/article/f3ad7d0ff8731609c3345b3b.html)。解决Ubuntu系统中使用Sublime Text 3时无法切换到搜狗输入法输入中文的问题。

<!--more-->

环境与工具:

+ 系统：Ubuntu14.04
+ 输入法：搜狗输入法 for Linux
+ 编辑器：Sublime text 3


<br>
<br>
<br>


##### 步骤一

保存下面的代码到文件`sublime_imfix.c` (位于~目录)

{% highlight c linenos %}

    #include <gtk/gtkimcontext.h>
    void gtk_im_context_set_client_window (GtkIMContext *context,GdkWindow *window)
    {
    GtkIMContextClass *klass;
    g_return_if_fail (GTK_IS_IM_CONTEXT (context));
    klass = GTK_IM_CONTEXT_GET_CLASS (context);
    if (klass->set_client_window)
        klass->set_client_window (context, window);
        g_object_set_data(G_OBJECT(context),"window",window);
    if(!GDK_IS_WINDOW (window))
        return;
    int width = gdk_window_get_width(window);
    int height = gdk_window_get_height(window);
    if(width != 0 && height != 0)
        gtk_im_context_focus_in(context);
    }

{% endhighlight %}


<br>
<br>
<br>


##### 步骤二

将上一步的代码编译成共享库`libsublime-imfix.so`，命令

{% highlight bash linenos %}

cd ~
gcc -shared -o libsublime-imfix.so sublime_imfix.c  `pkg-config --libs --cflags gtk+-2.0` -fPIC

{% endhighlight %}

注意：运行此命令前,可能需要先安装`gtk+-2.0`。


<br>
<br>
<br>


##### 步骤三

将`libsublime-imfix.so`拷贝到sublime_text所在文件夹

{% highlight bash linenos %}

    sudo mv libsublime-imfix.so /opt/sublime_text/

{% endhighlight %}

修改文件`/usr/bin/subl`的内容

{% highlight bash linenos %}

    sudo gedit /usr/bin/subl

{% endhighlight %}

将

> *exec /opt/sublime_text/sublime_text "$@"*

修改为

> *LD_PRELOAD=/opt/sublime_text/libsublime-imfix.so exec /opt/sublime_text/sublime_text "$@"*

此时，在命令中执行 `subl` 将可以使用搜狗for linux的中文输入。


<br>
<br>
<br>


##### 步骤四

为了使用鼠标右键打开文件及点击图标打开sublime时能够使用中文输入，还需要修改文件`sublime_text.desktop`的内容。

命令

{% highlight bash linenos %}

    sudo gedit /usr/share/applications/sublime_text.desktop

{% endhighlight %}

将`[Desktop Entry]`中的字符串

> *Exec=/opt/sublime_text/sublime_text %F*

修改为

> *Exec=bash -c "LD_PRELOAD=/opt/sublime_text/libsublime-imfix.so exec /opt/sublime_text/sublime_text %F"*

将`[Desktop Action Window]`中的字符串

> *Exec=/opt/sublime_text/sublime_text -n*

修改为

> *Exec=bash -c "LD_PRELOAD=/opt/sublime_text/libsublime-imfix.so exec /opt/sublime_text/sublime_text -n"*

将`[Desktop Action Document]`中的字符串

> *Exec=/opt/sublime_text/sublime_text --command new_file*

修改为

> *Exec=bash -c "LD_PRELOAD=/opt/sublime_text/libsublime-imfix.so exec /opt/sublime_text/sublime_text --command new_file"*

**注意：**

修改时请注意双引号`""`,否则会导致不能打开带有空格文件名的文件。

此处仅修改了`/usr/share/applications/sublime-text.desktop`，但可以正常使用了。

`opt/sublime_text/`目录下的`sublime-text.desktop`可以修改，也可不修改。

经过以上步骤我们能在Sublime中输入中文了。

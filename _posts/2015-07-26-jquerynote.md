---
layout: post
title: jQuery参考手册及学习笔记
date: 2015-07-26 08:19:35
postid: post0726
categories: [Notes]
tags: [Web, jQuery]
published: True
comments: True
---

不学习JavaScript直接学习jQuery，目的是使用jQuery完成一些提升浏览体验的细节动画和交互。

<!--more-->

<a style="padding-top:64px;" name="selector"></a>


<br>
<br>
<br>


##### 选择器

<table class="hoverable">
<thead><tr>
<th>选择器</th>
<th>实例</th>
<th>选取</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_all.asp" title="jQuery * 选择器">*</a></td>
<td>$("*")</td>
<td>所有元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_id.asp" title="jQuery # 选择器">#<i>id</i></a></td>
<td>$("#lastname")</td>
<td>id="lastname" 的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_class.asp" title="jQuery . 选择器">.<i>class</i></a></td>
<td>$(".intro")</td>
<td>所有 class="intro" 的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_element.asp" title="jQuery element 选择器"><i>element</i></a></td>
<td>$("p")</td>
<td>所有 &lt;p&gt; 元素</td>
</tr>

<tr>
<td>.<i>class</i>.<i>class</i></td>
<td>$(".intro.demo")</td>
<td>所有 class="intro" 且 class="demo" 的元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_first.asp" title="jQuery :first 选择器">:first</a></td>
<td>$("p:first")</td>
<td>第一个 &lt;p&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_last.asp" title="jQuery :last 选择器">:last</a></td>
<td>$("p:last")</td>
<td>最后一个 &lt;p&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_even.asp" title="jQuery :even 选择器">:even</a></td>
<td>$("tr:even")</td>
<td>所有偶数 &lt;tr&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_odd.asp" title="jQuery :odd 选择器">:odd</a></td>
<td>$("tr:odd")</td>
<td>所有奇数 &lt;tr&gt; 元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_eq.asp" title="jQuery :eq() 选择器">:eq(<i>index</i>)</a></td>
<td>$("ul li:eq(3)")</td>
<td>列表中的第四个元素（index 从 0 开始）</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_gt.asp" title="jQuery :gt 选择器">:gt(<i>no</i>)</a></td>
<td>$("ul li:gt(3)")</td>
<td>列出 index 大于 3 的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_lt.asp" title="jQuery :lt 选择器">:lt(<i>no</i>)</a></td>
<td>$("ul li:lt(3)")</td>
<td>列出 index 小于 3 的元素</td>
</tr>

<tr>
<td>:not(<i>selector</i>)</td>
<td>$("input:not(:empty)")</td>
<td>所有不为空的 input 元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_header.asp" title="jQuery :header 选择器">:header</a></td>
<td>$(":header")</td>
<td>所有标题元素 &lt;h1&gt; - &lt;h6&gt;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_animated.asp" title="jQuery :animated 选择器">:animated</a></td>
<td>&nbsp;</td>
<td>所有动画元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_contains.asp" title="jQuery :contains 选择器">:contains(<i>text</i>)</a></td>
<td>$(":contains('W3School')")</td>
<td>包含指定字符串的所有元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_empty.asp" title="jQuery :empty 选择器">:empty</a></td>
<td>$(":empty")</td>
<td>无子（元素）节点的所有元素</td>
</tr>

<tr>
<td>:hidden</td>
<td>$("p:hidden")</td>
<td>所有隐藏的 &lt;p&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_visible.asp" title="jQuery :visible 选择器">:visible</a></td>
<td>$("table:visible")</td>
<td>所有可见的表格</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td>s1,s2,s3</td>
<td>$("th,td,.intro")</td>
<td>所有带有匹配选择的元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_attribute.asp" title="jQuery [attribute] 选择器">[<i>attribute</i>]</a></td>
<td>$("[href]")</td>
<td>所有带有 href 属性的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_attribute_equal_value.asp" title="jQuery [attribute=value] 选择器">[<i>attribute</i>=<i>value</i>]</a></td>
<td>$("[href='#']")</td>
<td>所有 href 属性的值等于 "#" 的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_attribute_notequal_value.asp" title="jQuery [attribute!=value] 选择器">[<i>attribute</i>!=<i>value</i>]</a></td>
<td>$("[href!='#']")</td>
<td>所有 href 属性的值不等于 "#" 的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_attribute_end_value.asp" title="jQuery [attribute$=value] 选择器">[<i>attribute</i>$=<i>value</i>]</a></td>
<td>$("[href$='.jpg']")</td>
<td>所有 href 属性的值包含以 ".jpg" 结尾的元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input.asp" title="jQuery :input 选择器">:input</a></td>
<td>$(":input")</td>
<td>所有 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_text.asp" title="jQuery :text 选择器">:text</a></td>
<td>$(":text")</td>
<td>所有 type="text" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_password.asp" title="jQuery :password 选择器">:password</a></td>
<td>$(":password")</td>
<td>所有 type="password" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_radio.asp" title="jQuery :radio 选择器">:radio</a></td>
<td>$(":radio")</td>
<td>所有 type="radio" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_checkbox.asp" title="jQuery :checkbox 选择器">:checkbox</a></td>
<td>$(":checkbox")</td>
<td>所有 type="checkbox" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_submit.asp" title="jQuery :submit 选择器">:submit</a></td>
<td>$(":submit")</td>
<td>所有 type="submit" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_reset.asp" title="jQuery :reset 选择器">:reset</a></td>
<td>$(":reset")</td>
<td>所有 type="reset" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_button.asp" title="jQuery :button 选择器">:button</a></td>
<td>$(":button")</td>
<td>所有 type="button" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_image.asp" title="jQuery :image 选择器">:image</a></td>
<td>$(":image")</td>
<td>所有 type="image" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_file.asp" title="jQuery :file 选择器">:file</a></td>
<td>$(":file")</td>
<td>所有 type="file" 的 &lt;input&gt; 元素</td>
</tr>

<tr>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
<td style="background-color:#fff;">&nbsp;</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_enabled.asp" title="jQuery :enabled 选择器">:enabled</a></td>
<td>$(":enabled")</td>
<td>所有激活的 input 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_disabled.asp" title="jQuery :disabled 选择器">:disabled</a></td>
<td>$(":disabled")</td>
<td>所有禁用的 input 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_selected.asp" title="jQuery :selected 选择器">:selected</a></td>
<td>$(":selected")</td>
<td>所有被选取的 input 元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/selector_input_checked.asp" title="jQuery :checked 选择器">:checked</a></td>
<td>$(":checked")</td>
<td>所有被选中的 input 元素</td>
</tr>
</tbody></table>

<a style="padding-top:64px;" name="events"></a>


<br>
<br>
<br>


##### 事件方法

<table class="hoverable">
<thead><tr>
<th style="width:35%;">方法</th>
<th>描述</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_bind.asp" title="jQuery 事件 - bind() 方法">bind()</a></td>
<td>向匹配元素附加一个或更多事件处理器</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_blur.asp" title="jQuery 事件 - blur() 方法">blur()</a></td>
<td>触发、或将函数绑定到指定元素的 blur 事件</td>
</tr>


<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_change.asp" title="jQuery 事件 - change() 方法">change()</a></td>
<td>触发、或将函数绑定到指定元素的 change 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_click.asp" title="jQuery 事件 - click() 方法">click()</a></td>
<td>触发、或将函数绑定到指定元素的 click 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_dblclick.asp" title="jQuery 事件 - dblclick() 方法">dblclick()</a></td>
<td>触发、或将函数绑定到指定元素的 double click 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_delegate.asp" title="jQuery 事件 - delegate() 方法">delegate()</a></td>
<td>向匹配元素的当前或未来的子元素附加一个或多个事件处理器</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_die.asp" title="jQuery 事件 - die() 方法">die()</a></td>
<td>移除所有通过 live() 函数添加的事件处理程序。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_error.asp" title="jQuery 事件 - error() 方法">error()</a></td>
<td>触发、或将函数绑定到指定元素的 error 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_isdefaultprevented.asp" title="jQuery 事件 - isDefaultPrevented() 方法">event.isDefaultPrevented()</a></td>
<td>返回 event 对象上是否调用了 event.preventDefault()。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_pagex.asp" title="jQuery 事件 - pageX 属性">event.pageX</a></td>
<td>相对于文档左边缘的鼠标位置。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_pagey.asp" title="jQuery 事件 - pageY 属性">event.pageY</a></td>
<td>相对于文档上边缘的鼠标位置。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_preventdefault.asp" title="jQuery 事件 - preventDefault() 方法">event.preventDefault()</a></td>
<td>阻止事件的默认动作。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_result.asp" title="jQuery 事件 - result 属性">event.result</a></td>
<td>包含由被指定事件触发的事件处理器返回的最后一个值。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_target.asp" title="jQuery 事件 - target 属性">event.target</a></td>
<td>触发该事件的 DOM 元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_timeStamp.asp" title="jQuery 事件 - timeStamp 属性">event.timeStamp</a></td>
<td>该属性返回从 1970 年 1 月 1 日到事件发生时的毫秒数。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_type.asp" title="jQuery 事件 - type 属性">event.type</a></td>
<td>描述事件的类型。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_which.asp" title="jQuery 事件 - which 属性">event.which</a></td>
<td>指示按了哪个键或按钮。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_focus.asp" title="jQuery 事件 - focus() 方法">focus()</a></td>
<td>触发、或将函数绑定到指定元素的 focus 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_keydown.asp" title="jQuery 事件 - keydown() 方法">keydown()</a></td>
<td>触发、或将函数绑定到指定元素的 key down 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_keypress.asp" title="jQuery 事件 - keypress() 方法">keypress()</a></td>
<td>触发、或将函数绑定到指定元素的 key press 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_keyup.asp" title="jQuery 事件 - keyup() 方法">keyup()</a></td>
<td>触发、或将函数绑定到指定元素的 key up 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_live.asp" title="jQuery 事件 - live() 方法">live()</a></td>
<td>为当前或未来的匹配元素添加一个或多个事件处理器</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_load.asp" title="jQuery 事件 - load() 方法">load()</a></td>
<td>触发、或将函数绑定到指定元素的 load 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mousedown.asp" title="jQuery 事件 - mousedown() 方法">mousedown()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse down 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mouseenter.asp" title="jQuery 事件 - mouseenter() 方法">mouseenter()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse enter 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mouseleave.asp" title="jQuery 事件 - mouseleave() 方法">mouseleave()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse leave 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mousemove.asp" title="jQuery 事件 - mousemove() 方法">mousemove()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse move 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mouseout.asp" title="jQuery 事件 - mouseout() 方法">mouseout()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse out 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mouseover.asp" title="jQuery 事件 - mouseover() 方法">mouseover()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse over 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_mouseup.asp" title="jQuery 事件 - mouseup() 方法">mouseup()</a></td>
<td>触发、或将函数绑定到指定元素的 mouse up 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_one.asp" title="jQuery 事件 - one() 方法">one()</a></td>
<td>向匹配元素添加事件处理器。每个元素只能触发一次该处理器。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_ready.asp" title="jQuery 事件 - ready() 方法">ready()</a></td>
<td>文档就绪事件（当 HTML 文档就绪可用时）</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_resize.asp" title="jQuery 事件 - resize() 方法">resize()</a></td>
<td>触发、或将函数绑定到指定元素的 resize 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_scroll.asp" title="jQuery 事件 - scroll() 方法">scroll()</a></td>
<td>触发、或将函数绑定到指定元素的 scroll 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_select.asp" title="jQuery 事件 - select() 方法">select()</a></td>
<td>触发、或将函数绑定到指定元素的 select 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_submit.asp" title="jQuery 事件 - submit() 方法">submit()</a></td>
<td>触发、或将函数绑定到指定元素的 submit 事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_toggle.asp" title="jQuery 事件 - toggle() 方法">toggle()</a></td>
<td>绑定两个或多个事件处理器函数，当发生轮流的 click 事件时执行。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_trigger.asp" title="jQuery 事件 - trigger() 方法">trigger()</a></td>
<td>所有匹配元素的指定事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_triggerhandler.asp" title="jQuery 事件 - triggerHandler() 方法">triggerHandler()</a></td>
<td>第一个被匹配元素的指定事件</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_unbind.asp" title="jQuery 事件 - unbind() 方法">unbind()</a></td>
<td>从匹配元素移除一个被添加的事件处理器</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_undelegate.asp" title="jQuery 事件 - undelegate() 方法">undelegate()</a></td>
<td>从匹配元素移除一个被添加的事件处理器，现在或将来</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/event_unload.asp" title="jQuery 事件 - unload() 方法">unload()</a></td>
<td>触发、或将函数绑定到指定元素的 unload 事件</td>
</tr>
</tbody></table>

<a style="padding-top:64px;" name="effect"></a>


<br>
<br>
<br>


##### 效果函数

<table class="hoverable">
<thead><tr>
<th>方法</th>
<th>描述</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_animate.asp" title="jQuery 效果 - animate() 方法">animate()</a></td>
<td>对被选元素应用“自定义”的动画</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_clearqueue.asp" title="jQuery 效果 - clearQueue() 方法">clearQueue()</a></td>
<td>对被选元素移除所有排队的函数（仍未运行的）</td>
</tr>

<tr>
<td>delay()</td>
<td>对被选元素的所有排队函数（仍未运行）设置延迟</td>
</tr>

<tr>
<td>dequeue()</td>
<td>运行被选元素的下一个排队函数</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_fadein.asp" title="jQuery 效果 - fadeIn() 方法">fadeIn()</a></td>
<td>逐渐改变被选元素的不透明度，从隐藏到可见</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_fadeout.asp" title="jQuery 效果 - fadeOut() 方法">fadeOut()</a></td>
<td>逐渐改变被选元素的不透明度，从可见到隐藏</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_fadeto.asp" title="jQuery 效果 - fadeTo() 方法">fadeTo()</a></td>
<td>把被选元素逐渐改变至给定的不透明度</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_hide.asp" title="jQuery 效果 - hide() 方法">hide()</a></td>
<td>隐藏被选的元素</td>
</tr>

<tr>
<td>queue()</td>
<td>显示被选元素的排队函数</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_show.asp" title="jQuery 效果 - show() 方法">show()</a></td>
<td>显示被选的元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_slidedown.asp" title="jQuery 效果 - slideDown() 方法">slideDown()</a></td>
<td>通过调整高度来滑动显示被选元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_slidetoggle.asp" title="jQuery 效果 - slideToggle() 方法">slideToggle()</a></td>
<td>对被选元素进行滑动隐藏和滑动显示的切换</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_slideup.asp" title="jQuery 效果 - slideUp() 方法">slideUp()</a></td>
<td>通过调整高度来滑动隐藏被选元素</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_stop.asp" title="jQuery 效果 - stop() 方法">stop()</a></td>
<td>停止在被选元素上运行动画</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/effect_toggle.asp" title="jQuery 效果 - toggle() 方法">toggle()</a></td>
<td>对被选元素进行隐藏和显示的切换</td>
</tr>
</tbody></table>

<a style="padding-top:64px;" name="doc"></a>


<br>
<br>
<br>


##### 文档操作方法

<table class="hoverable">
<thead><tr>
<th style="width:30%;">方法</th>
<th>描述</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_addclass.asp" title="jQuery HTML - addClass() 方法">addClass()</a></td>
<td>向匹配的元素添加指定的类名。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_after.asp" title="jQuery HTML - after() 方法">after()</a></td>
<td>在匹配的元素之后插入内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_append.asp" title="jQuery HTML - append() 方法">append()</a></td>
<td>向匹配元素集合中的每个元素结尾插入由参数指定的内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_appendto.asp" title="jQuery HTML - appendTo() 方法">appendTo()</a></td>
<td>向目标结尾插入匹配元素集合中的每个元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_attr.asp" title="jQuery HTML - attr() 方法">attr()</a></td>
<td>设置或返回匹配元素的属性和值。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_before.asp" title="jQuery HTML - before() 方法">before()</a></td>
<td>在每个匹配的元素之前插入内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_clone.asp" title="jQuery HTML - clone() 方法">clone()</a></td>
<td>创建匹配元素集合的副本。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_detach.asp" title="jQuery HTML - detach() 方法">detach()</a></td>
<td>从 DOM 中移除匹配元素集合。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_empty.asp" title="jQuery HTML - empty() 方法">empty()</a></td>
<td>删除匹配的元素集合中所有的子节点。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_hasclass.asp" title="jQuery HTML - hasClass() 方法">hasClass()</a></td>
<td>检查匹配的元素是否拥有指定的类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_html.asp" title="jQuery HTML - html() 方法">html()</a></td>
<td>设置或返回匹配的元素集合中的 HTML 内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_insertafter.asp" title="jQuery HTML - insertAfter() 方法">insertAfter()</a></td>
<td>把匹配的元素插入到另一个指定的元素集合的后面。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_insertbefore.asp" title="jQuery HTML - insertBefore() 方法">insertBefore()</a></td>
<td>把匹配的元素插入到另一个指定的元素集合的前面。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_prepend.asp" title="jQuery HTML - prepend() 方法">prepend()</a></td>
<td>向匹配元素集合中的每个元素开头插入由参数指定的内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_perpendto.asp" title="jQuery HTML - prependTo() 方法">prependTo()</a></td>
<td>向目标开头插入匹配元素集合中的每个元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_remove.asp" title="jQuery HTML - remove() 方法">remove()</a></td>
<td>移除所有匹配的元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_removeattr.asp" title="jQuery HTML - removeAttr() 方法">removeAttr()</a></td>
<td>从所有匹配的元素中移除指定的属性。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_removeclass.asp" title="jQuery HTML - removeClass() 方法">removeClass()</a></td>
<td>从所有匹配的元素中删除全部或者指定的类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_replaceall.asp" title="jQuery HTML - replaceAll() 方法">replaceAll()</a></td>
<td>用匹配的元素替换所有匹配到的元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_replacewith.asp" title="jQuery HTML - replaceWith() 方法">replaceWith()</a></td>
<td>用新内容替换匹配的元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_text.asp" title="jQuery HTML - text() 方法">text()</a></td>
<td>设置或返回匹配元素的内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_toggleclass.asp" title="jQuery HTML - toggleClass() 方法">toggleClass()</a></td>
<td>从匹配的元素中添加或删除一个类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_unwrap.asp" title="jQuery HTML - unwrap() 方法">unwrap()</a></td>
<td>移除并替换指定元素的父元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_val.asp" title="jQuery HTML - val() 方法">val()</a></td>
<td>设置或返回匹配元素的值。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_wrap.asp" title="jQuery HTML - wrap() 方法">wrap()</a></td>
<td>把匹配的元素用指定的内容或元素包裹起来。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_wrapall.asp" title="jQuery HTML - wrapAll() 方法">wrapAll()</a></td>
<td>把所有匹配的元素用指定的内容或元素包裹起来。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_wrapinner.asp" title="jQuery HTML - wrapinner() 方法">wrapinner()</a></td>
<td>将每一个匹配的元素的子内容用指定的内容或元素包裹起来。</td>
</tr>
</tbody></table>

<a style="padding-top:64px;" name="propertyoperate"></a>


<br>
<br>
<br>


##### 属性操作方法

<table class="hoverable">
<thead><tr>
<th>方法</th>
<th>描述</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_addclass.asp" title="jQuery HTML - addClass() 方法">addClass()</a></td>
<td>向匹配的元素添加指定的类名。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_attr.asp" title="jQuery HTML - attr() 方法">attr()</a></td>
<td>设置或返回匹配元素的属性和值。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_hasclass.asp" title="jQuery HTML - hasClass() 方法">hasClass()</a></td>
<td>检查匹配的元素是否拥有指定的类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/manipulation_html.asp" title="jQuery HTML - html() 方法">html()</a></td>
<td>设置或返回匹配的元素集合中的 HTML 内容。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_removeattr.asp" title="jQuery HTML - removeAttr() 方法">removeAttr()</a></td>
<td>从所有匹配的元素中移除指定的属性。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_removeclass.asp" title="jQuery HTML - removeClass() 方法">removeClass()</a></td>
<td>从所有匹配的元素中删除全部或者指定的类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_toggleclass.asp" title="jQuery HTML - toggleClass() 方法">toggleClass()</a></td>
<td>从匹配的元素中添加或删除一个类。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/attributes_val.asp" title="jQuery HTML - val() 方法">val()</a></td>
<td>设置或返回匹配元素的值。</td>
</tr>

</tbody></table>

<a style="padding-top:64px;" name="CSS"></a>


<br>
<br>
<br>


#####  CSS 操作函数

<table class="hoverable">
<thead><tr>
<th>CSS 属性</th>
<th>描述</th>
</tr>
</thead>

<tbody>
<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_css.asp" title="jQuery CSS 操作 - css() 方法">css()</a></td>
<td>设置或返回匹配元素的样式属性。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_height.asp" title="jQuery CSS 操作 - height() 方法">height()</a></td>
<td>设置或返回匹配元素的高度。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_offset.asp" title="jQuery CSS 操作 - offset() 方法">offset()</a></td>
<td>返回第一个匹配元素相对于文档的位置。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_offsetparent.asp" title="jQuery CSS 操作 - offsetParent() 方法">offsetParent()</a></td>
<td>返回最近的定位祖先元素。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_position.asp" title="jQuery CSS 操作 - position() 方法">position()</a></td>
<td>返回第一个匹配元素相对于父元素的位置。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_scrollleft.asp" title="jQuery CSS 操作 - scrollLeft() 方法">scrollLeft()</a></td>
<td>设置或返回匹配元素相对滚动条左侧的偏移。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_scrolltop.asp" title="jQuery CSS 操作 - scrollTop() 方法">scrollTop()</a></td>
<td>设置或返回匹配元素相对滚动条顶部的偏移。</td>
</tr>

<tr>
<td><a href="http://www.w3school.com.cn/jquery/css_width.asp" title="jQuery CSS 操作 - width() 方法">width()</a></td>
<td>设置或返回匹配元素的宽度。</td>
</tr>
</tbody></table>

<a style="padding-top:64px;" name="Ajax"></a>


<br>
<br>
<br>


##### [Ajax 操作函数](http://www.w3school.com.cn/jquery/jquery_ref_ajax.asp)

<a style="padding-top:64px;" name="Traversal"></a>


<br>
<br>
<br>


##### [遍历函数](http://www.w3school.com.cn/jquery/jquery_ref_traversing.asp)

<a style="padding-top:64px;" name="data"></a>


<br>
<br>
<br>


##### [数据操作函数](http://www.w3school.com.cn/jquery/jquery_ref_data.asp)

<a style="padding-top:64px;" name="DOM"></a>


<br>
<br>
<br>


##### [DOM 元素方法](http://www.w3school.com.cn/jquery/jquery_ref_dom_element_methods.asp)

<a style="padding-top:64px;" name="Core"></a>


<br>
<br>
<br>


##### 核心

<a style="padding-top:64px;" name="property"></a>


<br>
<br>
<br>


##### 属性

<!-- [在线编辑器测试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_selector_id) -->


<div id="side-fixed-nav">
    <ul id="dropdown1" class="collection dropdown-content">
        <li><a href="#selector">选择器</a></li>
        <li><a href="#events">事件方法</a></li>
        <li><a href="#effect">效果函数</a></li>
        <li><a href="#doc">文档操作方法</a></li>
        <li><a href="#propertyoperate">属性操作方法</a></li>
        <li><a href="#CSS">CSS操作函数</a></li>
        <li><a href="#Ajax"><i>进阶</i></a></li>
        <!-- <li><a href="#Ajax">Ajax</a></li>
        <li><a href="#Traversal">遍历</a></li>
        <li><a href="#data">数据</a></li>
        <li><a href="#DOM">DOM元素</a></li>
        <li><a href="#Core">核心</a></li>
        <li><a href="#property">属性</a></li> -->
    </ul>
    <a class="btn-large waves-effect waves-light dropdown-button" href="#!" data-activates="dropdown1">段落目录<i class="mdi-action-list left"></i></a>
</div>
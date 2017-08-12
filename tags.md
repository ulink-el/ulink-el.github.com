---
layout: page
title: Tags
permalink: /tags/
---
<div class="catalist">
   {% for tags in site.tags %}
   <h3 id="{{ tags | first }}-ref" style="padding-top:64px;">{{ tags | first }}<span class="cata-num" style="margin-left:1rem;">{{ tags | last | size }}</span></h3>
    <ul class="catabrick">
    {% for post in tags.last %}
        <li>
            <a class="catatitle" href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
            <span class="catainfo grey-text light right">{{post.date | date: "%b %-d , %Y"}}</span>
        </li>
        <div class="divider"></div>
    {% endfor %}
    </ul>
    {% endfor %}
</div>
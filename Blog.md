---
layout: collection
title: Blog
permalink: Blog/
---

{% assign char-count = 500 %}

{% for post in site.posts %}
<article class="post-entry">
    <h2 class="post-title">
        <a href="{{ post.url | prepend: site.baseurl }}">
            {{ post.title }}
        </a>
    </h2>

{% include post-info.html tags = post.tags date=post.date %}

    <div class="post-excerpt">
        {{post.content | markdownify | strip_html | truncate: char-count}}

        <a class="post-see-more" href="{{ post.url | prepend: site.baseurl }}">
            <i>See&nbsp;More</i>
        </a>
    </div>
</article>
<br>
{% endfor %}

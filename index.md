---
layout: home2
title: About
description: "About Patrick Stuedi"
tags: [Jekyll, theme, responsive, blog, template]
image:
  feature: trees.jpg
---
<div style="text-align: justify"> 
<p>
I'm a member of the research staff at IBM research Zurich. My research interests are in distributed systems, networking and operating systems. I graduated with a PhD from ETH Zurich in 2008 and spent two years (2008-2010) as a Postdoc at Microsoft Research Silicon Valley. 
</p>
<p>
The general theme of my work is to explore how modern networking and storage hardware can be exploited in distributed systems. Over the last years, I've been working on Crail, a fast distributed data store designed from ground up for fast storage (DRAM, NVMe, PCM) and networking hardware (100Gb/s RDMA, NVMf). Crail is built upon principles of user-level I/O and primarily targets fast sharing of ephemeral data in distributed data processing workloads (Spark, Tensforflow, serverless workloads, etc.).
</p>
<br>
<p>
Currently, I'm working on a new storage platform for efficient ML training on disaggregated storage.
</p>
<br>
<p>
Earlier, I developed DiSNI, a zero-copy RDMA-based network stack for the JVM, DaRPC, a ultra-low latency RPC library also for the JVM, and jVerbs, an RDMA-based network stack and precurser of DiSNI, which is part of the IBM JDK since May 2014.
</p>
</div>

### News
<ul class="news list-unstyled">
{% for post in site.categories.news limit: site.front_page_news %}
    {% if post.shortnews %}
        <li class="shortnews">
            <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
            {{ post.content }}
        </li>
    {% else %}
        <li class="bloglink">
            <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
            <a href="{{ post.url }}">&raquo; {{ post.title }}</a>
        </li>
    {% endif %}
{% endfor %}
</ul>
{% assign numposts = site.categories.news | size %}
{% if numposts >= site.front_page_news %}
<p><a href="{{ site.base }}/news/">more posts&hellip;</a></p>
{% endif %}


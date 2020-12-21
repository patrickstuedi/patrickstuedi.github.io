---
layout: home2
title: About
description: "About Patrick Stuedi"
tags: [Jekyll, theme, responsive, blog, template]
image:
  feature: trees.jpg
---
I'm a researcher and system's builder in the area of distributed systems, networking and operating systems. From 2010 to 2019 I was a member of the research staff at IBM Research Zurich. I'm holding a PhD in Compuer Science from ETH Zurich. From 2008 to 2019 I spent two years as a Postdoc at Microsoft Research Silicon Valley. Since Nov 2019 I'm part of the distributed graph database team at Linkedin.<br/><br/>The general theme of my work is to explore how modern networking and storage hardware can be exploited in distributed systems. Over the last years, I've been working on [Crail](http://crail.apache.org), a fast distributed data store designed from ground up for fast storage (DRAM, NVMe, PCM) and networking hardware (100Gb/s RDMA, NVMf). Crail is built upon principles of user-level I/O and primarily targets fast sharing of ephemeral data over disaggregated storage in distributed data processing workloads (Spark, Tensforflow, serverless workloads, etc.).<br/><br/>Earlier, I developed [DiSNI](https://github.com/zrlio/disni), a zero-copy RDMA-based network stack for the JVM, [DaRPC](https://github.com/zrlio/darpc), a ultra-low latency RPC library also for the JVM, and [jVerbs](https://www.ibm.com/support/knowledgecenter/en/SSYKE2_8.0.0/com.ibm.java.80.doc/docs/rdma_jverbs.html), an RDMA-based network stack and precurser of DiSNI, which is part of the IBM JDK since May 2014.
{: style="text-align: justify"}  

### News
<ul class="news list-unstyled">
{% for post in site.categories.news limit: site.front_page_news %}
    {% if post.shortnews %}
        <li class="shortnews">
            <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
            &raquo; {{ post.title }}
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

### Recent Talks

  * [**Unification of Temporary Storage in the NodeKernel Architecture**](https://www.usenix.org/conference/atc19/presentation/stuedi), *USENIX ATC 19*, Renton, WA, USA, July 2019.
  * [**Data Processing at the Speed of 100Gpbs using Apache Crail**](https://conferences.oreilly.com/strata/strata-ca-2019/public/schedule/detail/71902), *Oreilly Strata*, San Francisco, CA, USA, Februrary 2019.
  * [**COMPASS Talk about Apache Crail**](https://www.systems.ethz.ch/node/1321), *ETH Zurich*, Zurich, Switzerland, September 2018.
  * [**Serverless Machine Learning on Modern Hardware Using Apache Spark**](https://databricks.com/session/serverless-machine-learning-on-modern-hardware-using-apache-spark), *Spark Summit*, San Francisco, CA, June 2018.
  * [**Running Apache Spark on a High-Performance Cluster Using RDMA and NVMe Flash**](https://databricks.com/session/running-apache-spark-on-a-high-performance-cluster-using-rdma-and-nvme-flash), *Spark Summit*, San Francisco, CA, June 2017.
  
### Program Committes

USENIX ATC'21, SoCC'20, USENIX ATC'20, ASPLOS'20 (ERC), USENIX ATC'19, ASPLOS'19 (ERC), USENIX ATC'18, SoCC'18, SoCC'17, Systor'17, ICDCS'14, ICDCS'11, ICDCS'10

### Teaching

I have been co-teaching the following courses:

  * **Advanced Computer Networks**, Spring Semester 2018, ETH Zurich
  * **Advanced Computer Networks**, Spring Semester 2017, ETH Zurich
  * [**Advanced Computer Networks**, Spring Semster 2016, ETH Zurich](https://www.systems.ethz.ch/courses/spring2016/acn)
  * **Advanced Computer Networks**, Spring Semster 2015, ETH Zurich
  * [**Advanced Computer Networks**, Spring Semester 2014, ETH Zurich](https://www.systems.ethz.ch/courses/spring2014/acn)
  * [**Advanced Computer Networks**, Spring Semster 2013, ETH Zurich](https://www.systems.ethz.ch/courses/spring2013/acn)
  * [**Advanced Computer Networks**, Spring Semester 2012, ETH Zurich](http://archive.systems.ethz.ch/www.systems.ethz.ch/education/spring-2012/adv-comp-netw.html)
  * [**Advanced Computer Networks**, Spring Semster 2011, ETH Zurich](http://archive.systems.ethz.ch/www.systems.ethz.ch/education/fs11/advanced-computer-networks.html)


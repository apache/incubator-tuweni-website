---
layout: tutorial
title: Getting Started with Bytes
description: Getting Started with Bytes
group: nav-right
categories: ["bytes"]
previous: index.md
next: creating-bytes.md
---
Apache Tuweni provides support for manipulating bytes.

To get started, install the `bytes` library.

With Maven:

{% highlight xml %}
<dependency>
  <groupId>org.apache.tuweni</groupId>
  <artifactId>bytes</artifactId>
  <version>{{site.data.project.latest_release}}</version>
</dependency>
{% endhighlight %}

Or using Gradle:

{% highlight groovy %}
implementation("org.apache.tuweni:bytes:{{site.data.project.latest_release}}")
{% endhighlight %}

The [bytes library](/docs/org.apache.tuweni.bytes/index.html) revolves mainly around the [`Bytes`](/docs/org.apache.tuweni.bytes/-bytes/index.html) interface.

This tutorial goes over the main uses of `Bytes`, from creating them to manipulating them.


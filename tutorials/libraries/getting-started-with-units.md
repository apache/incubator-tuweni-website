---
layout: tutorial
title: Getting Started with Unsigned Integers
description: Getting Started with Unsigned Integers
group: nav-right
categories: ["units", "bigints"]
previous: index.md
next: creating-uints.md
---

Apache Tuweni provides support for manipulating unsigned integers and base Ethereum currencies.

To get started, install the `units` library.

With Maven:

{% highlight xml %}
<dependency>
  <groupId>org.apache.tuweni</groupId>
  <artifactId>units</artifactId>
  <version>{{site.data.project.latest_release}}</version>
</dependency>
{% endhighlight %}

Or using Gradle:

{% highlight groovy %}
implementation("org.apache.tuweni:units:{{site.data.project.latest_release}}")
{% endhighlight %}

The [units library](/docs/org.apache.tuweni.units.bigints/index.html) revolves mainly around the [`Uint256`](/docs/org.apache.tuweni.units.bigints/-u-int256/index.html), [`Uint384`](/docs/org.apache.tuweni.units.bigints/-u-int384/index.html)  and [`Uint64`](/docs/org.apache.tuweni.units.bigints/-u-int64/index.html)  interfaces.

This tutorial goes over the main uses of `Uint256` - you can apply the same behaviors over to `Uint384`, `Uint64` or `Uint32`.

It will also touch on `Wei` and `Gas`.
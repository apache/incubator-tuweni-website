---
layout: tutorial
title: Creating your own unsigned integer class
description: Creating your own unsigned integer class
group: nav-right
categories: ["units", "bigints"]
previous: uint-operations.md
---

You can create your own domain class based off the `Uints`. A good example is the [`Wei class`](/docs/org.apache.tuweni.units.ethereum/-wei/index.html).

You will need to provide the super constructor the constructor of your class.

{%highlight java%}
public final class Wei extends BaseUInt256Value<Wei> {
...
  private Wei(UInt256 bytes) {
    super(bytes, Wei::new);
  }
...
}
{%endhighlight%}


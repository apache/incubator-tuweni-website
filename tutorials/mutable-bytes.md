---
layout: tutorial
title: Mutable Bytes
description: Mutable Bytes
group: nav-right
categories: ["bytes"]
previous: manipulating-bytes.md
---


By default, bytes objects are not mutable. You can use [`MutableBytes` objects](/docs/org.apache.tuweni.bytes/-mutable-bytes/index.html) instead.

# Creating MutableBytes objects

The methods described in the [tutorial "Creating Bytes"](/tutorials/creating-bytes) all work in the same way for `MutableBytes`.

You can call the [method `mutableCopy()`](/docs/org.apache.tuweni.bytes/-mutable-bytes/mutable-copy.html) on any Bytes object to get a copy of the Bytes object as mutable.

Finally, you can create fresh objects with the [`create()` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/create.html).

# Fill, Clear

Fill a MutableBytes with the same byte the [fill method](/docs/org.apache.tuweni.bytes/-mutable-bytes/fill.html):

{%highlight java%}
MutableBytes bytes = MutableBytes.create(2);
bytes.fill((byte) 34);
assertEquals(Bytes.fromHexString("0x2222"), bytes);
{%endhighlight%}

You can clear the contents with the [`clear` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/clear.html):

{%highlight java%}
MutableBytes bytes = MutableBytes.fromHexString("0xdeadbeef");
bytes.clear();
{%endhighlight%}

# Setting values

You can set values with different arguments:

* The [`set(int i, byte b)` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/set.html) sets the value of a byte at index `i`.
* The [`setInt(int i, int value)` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/set-int.html) sets the value of the next four bytes at index `i`.
* The [`setLong(int i, long value)` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/set-long.html) sets the value of the next eight bytes at index `i`.
* The [`set(int offset, Bytes bytes)` method](/docs/org.apache.tuweni.bytes/-mutable-bytes/set.html) sets the value of the next bytes at index `i`.



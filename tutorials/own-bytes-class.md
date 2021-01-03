---
layout: tutorial
title: Creating your very own Bytes classs
description: Creating your very own Bytes classs
group: nav-right
categories: ["bytes"]
previous: mutable-bytes.md
---

You can create your very own implementation of `Bytes` by extending the [`AbstractBytes` class](/docs/org.apache.tuweni.bytes/-abstract-bytes/index.html).

You will need to implement the following functions:
* [`get(i)`](/docs/org.apache.tuweni.bytes/-bytes/get.html)
* [`size()`](/docs/org.apache.tuweni.bytes/-bytes/size.html)
* [`slice(offset, size)`](/docs/org.apache.tuweni.bytes/-bytes/slice.html)
* [`copy(offset, size)`](/docs/org.apache.tuweni.bytes/-bytes/copy.html)
* [`mutableCopy(offset, size)`](/docs/org.apache.tuweni.bytes/-bytes/mutable-copy.html)

You can choose to simplify greatly by extending the [`DelegatingBytes` class](/docs/org.apache.tuweni.bytes/-delegating-bytes/index.html) instead.

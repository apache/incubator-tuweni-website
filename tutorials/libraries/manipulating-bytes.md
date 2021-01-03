---
layout: tutorial
title: Manipulating Bytes
description: Manipulating Bytes
group: nav-right
categories: ["bytes"]
previous: creating-bytes.md
next: extracting-values.md
---

# Concatenating and wrapping

You can [concatenate](/docs/org.apache.tuweni.bytes/-bytes/concatenate.html) or [wrap](/docs/org.apache.tuweni.bytes/-bytes/wrap.html) bytes objects.

When concatenating, the underlying objects are copied into a new bytes object.

When wrapping, you are creating a *view* made of the underlying bytes objects. If their values change, the wrapped view changes as well.

Of course, wrapping is preferrable to avoid copying bytes in memory.

# Copying and slicing

In the same spirit as above, you can [copy](/docs/org.apache.tuweni.bytes/-bytes/copy.html) or [slice](/docs/org.apache.tuweni.bytes/-bytes/slice.html) bytes objects. When you slice a bytes object, you create a view of the original bytes object, and the slice will change if the underlying bytes object changes. If you copy instead, you create a new copy of the bytes.

{%highlight java%}
// slice from the second byte:
bytes.slice(2);
// slice from the second byte to the fifth byte:
bytes.slice(2, 5);
{%endhighlight%}

# Shifting bytes

You can shift [right](/docs/org.apache.tuweni.bytes/-bytes/shift-right.html) and [left](/docs/org.apache.tuweni.bytes/-bytes/shift-left.html) the bits of a bytes object by a given distance.

This is equivalent to the `<<<` or `>>>` operators in Java.

# xor, or, and

You can apply boolean operations to Bytes objects.

* [xor](/docs/org.apache.tuweni.bytes/-bytes/xor.html)
* [or](/docs/org.apache.tuweni.bytes/-bytes/or.html)
* [and](/docs/org.apache.tuweni.bytes/-bytes/and.html)

Those methods take as argument the value to compare this value with, and return a new Bytes object that is the result of the boolean operation.

If the argument and the value are different lengths, then the shorter will be zero-padded to the left.

{%highlight java%}
Bytes value = Bytes.fromHexString("0x01000001").xor(Bytes.fromHexString("0x01000000"));
assertEquals(Bytes.fromHexString("0x00000001"), value);
{%endhighlight%}

# not

The [`not` method](https://tuweni.apache.org/docs/org.apache.tuweni.bytes/-bytes/not.html) returns a bit-wise NOT of the bytes.

{%highlight java%}
Bytes value = Bytes.fromHexString("0x01000001").not();
assertEquals(Bytes.fromHexString("0xfefffffe"), value);
{%endhighlight%}

# commonPrefix

The [`commonPrefix` method](https://tuweni.apache.org/docs/org.apache.tuweni.bytes/-bytes/common-prefix.html) returns the common bytes both the value and the argument start with.


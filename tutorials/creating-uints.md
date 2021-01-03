---
layout: tutorial
title: Creating Uints
description: Creating Uints
group: nav-right
categories: ["units", "bigints"]
previous: getting-started-with-units.md
next: uints-operations.md
---

NOTE: We are going to use the [`UInt256` class](/docs/org.apache.tuweni.units.bigints/-u-int256/index.html) for all examples, but the same behaviors are possible with the [`UInt384`](/docs/org.apache.tuweni.units.bigints/-u-int384/index.html), [`UInt64`](/docs/org.apache.tuweni.units.bigints/-u-int64/index.html), [`UInt32`](/docs/org.apache.tuweni.units.bigints/-u-int32/index.html) classes.

We refer to those classes as `UInt`.

# Creating Uints

## `valueOf`

You can initialize a `UInt` with the [static method `valueOf`](/docs/org.apache.tuweni.units.bigints/-u-int256/value-of.html), with an integer, a long, or a BigInteger object. This only accepts positive values.

{%highlight java%}
// from an int
UInt256 value = UInt256.valueOf(42);
// from a long
UInt256 value = UInt256.valueOf(42L);
// from a BigInteger
UInt256 value = UInt256.valueOf(BigInteger.ONE);
{%endhighlight%}

## `fromBytes`

You can initialize a `UInt` from a `Bytes` object, using the [`fromBytes` method](/docs/org.apache.tuweni.units.bigints/-u-int256/from-bytes.html).

{%highlight java%}
UInt256 value = UInt256.fromBytes(Bytes.wrap(new byte[] {0x01, 0x02, 0x03}));
{%endhighlight%}

## `fromHexString`

You can initialize a `UInt` from a string representing a hexadecimal encoding of bytes, with an optional prefix of `0x`.

{%highlight java%}
UInt256 value = UInt256.fromHexString("0xdeadbeef");
{%endhighlight%}

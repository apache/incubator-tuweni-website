---
layout: tutorial
title: Extracting values
description: Extracting values
group: nav-right
categories: ["bytes"]
previous: manipulating-bytes.md
next: mutable-bytes.md
---

You can extract values from a bytes object into native Java objects such as ints and longs, bytes, byte arrays and so on.

Note all the methods here take an optional `ByteOrder` argument, defaulting to big endian by default.

# toInt() and toLong()

The [method `toInt()`](docs/org.apache.tuweni.bytes/-bytes/to-int.html) and the [method `toLong()`](/docs/org.apache.tuweni.bytes/-bytes/to-long.html) respectively translate the bytes values into an int or a long, requiring respectively the value to be at most 4 or 8 bytes long.

# get(i)

The [`get(i)` method](/docs/org.apache.tuweni.bytes/-bytes/get.html) provides the byte at index `i`.

# getInt(i) and getLong(i)

The [method `getInt()`](docs/org.apache.tuweni.bytes/-bytes/get-int.html) and the [method `getLong()`](/docs/org.apache.tuweni.bytes/-bytes/get-long.html) respectively return the next 4 or 8 bytes into an int or a long.

# toArray() and toArrayUnsafe()

The [method `toArray`](/docs/org.apache.tuweni.bytes/-bytes/to-array.html) copies the bytes of the object into a new bytes array.

The [method `toArrayUnsafe`](/docs/org.apache.tuweni.bytes/-bytes/to-array-unsafe.html) makes available the underlying byte array of the object - modifying it changes the Bytes object. Note this is more performant as it doesn't allocate new memory.

# To BigIntegers

The [method `toUnsignedBigInteger`](/docs/org.apache.tuweni.bytes/-bytes/to-unsigned-big-integer.html) creates a new unsigned BigInteger object with the contents of the Bytes object.
You can also use the method [`toBigInteger`](/docs/org.apache.tuweni.bytes/-bytes/to-big-integer.html) to represent Bytes as a signed integer, using the two's-complement representation.

# Transforming Bytes into strings

There is a sleuth of options to turn bytes into strings, and they all have different use cases.

* The [method `toHexString`](/docs/org.apache.tuweni.bytes/-bytes/to-hex-string.html) provides the value represented as hexadecimal, starting with "0x".
* The [method `toUnprefixedHexString`](/docs/org.apache.tuweni.bytes/-bytes/to-unprefixed-hex-string.html) provides the value represented as hexadecimal, no "0x" prefix though.
* The [method `toShortHexString`](/docs/org.apache.tuweni.bytes/-bytes/to-short-hex-string.html) provides the value represented as a minimal hexadecimal string (without any leading zero).
* The [method `toQuantityHexString`](/docs/org.apache.tuweni.bytes/-bytes/to-quantity-hex-string.html) provides the value represented as a minimal hexadecimal string (without any leading zero, except if it's valued zero or empty, in which case it returns 0x0).
* The [method `toEllipsisHexString`](/docs/org.apache.tuweni.bytes/-bytes/to-ellipsis-hex-string.html) provides the first 3 bytes and last 3 bytes represented as hexadecimal strings, joined with an ellipsis (`...`).

By default, `toString()` calls `toHexString()`.
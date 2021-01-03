---
layout: tutorial
title: Unsigned Integers operations
description: Unsigned Integers operations
group: nav-right
categories: ["units", "bigints"]
previous: creating-uints.md
---

`Uints` are immutable, so all operations create a new object as the result of the operation.

# Arithmetic operations

## Adding and subtracting

* [`add(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/add.html)
* [`substract(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/subtract.html)

Since these are bound integers, they will overflow and underflow if the operation returns a value outside the boundaries - for a `Uint256`, 0 to 2^256.

For this reason, the API also contains `exact` methods that throw exceptions if the operations overflows or underflows.

* [`addExact(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/add-exact.html)
* [`subtractExact(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/subtract-exact.html)

## Multiplying and dividing

* [`multiply(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/multiply.html)
* [`divide(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/divide.html)

Additionally, the [method `divideCeil(other)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/divide-ceil.html) divides integers but returns the ceiling of the rounding.

{%highlight java%}
UInt256 result = UInt256.valueOf(12L).divide(UInt256.valueOf(5L)); // returns 2
UInt256 resultCeiling = UInt256.valueOf(12L).divideCeil(UInt256.valueOf(5L)); // returns 3
{%endhighlight%}

## Modulus

You can use the [method `mod(divisor)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/mod.html) to get the modulus of the value by the divisor.

The [method `mod0`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/mod0.html) is more forgiving - if you divide by zero, it will return zero instead of throwing an exception.

## Power

The [method `pow(exponent)`](/docs/org.apache.tuweni.units.bigints/-u-int256-value/pow.html) returns a value that is `value^exponent mod 2^256.

# Boolean operations

You can use the following methods to perform boolean operations:

* [`not()`: bit-wise NOT of this value.](/docs/org.apache.tuweni.units.bigints/-u-int256/not.html)
* [`and(other)`: bit-wise AND of this value and the supplied value.](/docs/org.apache.tuweni.units.bigints/-u-int256/and.html)
* [`or(other)`: bit-wise OR of this value and the supplied value.](/docs/org.apache.tuweni.units.bigints/-u-int256/or.html)
* [`xor(other)`: bit-wise XOR of this value and the supplied value.](/docs/org.apache.tuweni.units.bigints/-u-int256/xor.html)

# Shifting bytes

You can shift [right](/docs/org.apache.tuweni.units.bigints/-u-int256/shift-right.html) and [left](/docs/org.apache.tuweni.units.bigints/-u-int256/shift-left.html) the bits of the underlying bytes object by a given distance.

This is equivalent to the `<<<` or `>>>` operators in Java.
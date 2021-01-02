---
layout: tutorial
title: Creating Bytes
description: Creating Bytes
group: nav-right
categories: ["bytes"]
previous: getting-started-with-bytes.md
next: manipulating-bytes.md
---

# From a bytes array:

You can create `Bytes` objects by wrapping a native byte array:

{% highlight java %}
Bytes bytes = Bytes.wrap(new byte[] {1, 2, 3, 4});
{% endhighlight %}

Note the underlying array is not copied - any change to the byte array will change the Bytes object's behavior.

You can also wrap with an offset and a size to select a portion of the array:

{% highlight java %}
// wrapping with an offset of 2 and a size of one byte
Bytes bytes = Bytes.wrap(new byte[] {1, 2, 3, 4}, 2, 1);
{% endhighlight %}

# From a hex string:

You can create `Bytes` objects from a hexadecimal-encoded string with the [`fromHexString`](/docs/org.apache.tuweni.bytes/-bytes/from-hex-string.html) method:

{% highlight java %}
Bytes bytes = Bytes.fromHexString("0xdeadbeef");
{% endhighlight %}

The `"0x"` prefix is optional.

However, this requires an even-sized string. For example, this succeeds:

{% highlight java %}
Bytes bytes = Bytes.fromHexString("01FF2A");
{% endhighlight %}

This fails:

{% highlight java %}
Bytes bytes = Bytes.fromHexString("1FF2A");
{% endhighlight %}

You can circumvent this with the [`fromHexStringLenient` method](/docs/org.apache.tuweni.bytes/-bytes/from-hex-string-lenient.html):

{% highlight java %}
Bytes bytes = Bytes.fromHexStringLenient("1FF2A");
{% endhighlight %}

# From a base64-encoded string:

You can create `Bytes` objects from a base64-encoded string with the [`fromBase64String`](/docs/org.apache.tuweni.bytes/-bytes/from-base64-string.html) method:

{% highlight java %}
Bytes value = Bytes.fromBase64String("deadbeefISDAbest");
{% endhighlight %}

# From primitive types

We also have convenience methods to create `Bytes` objects from primitive types.

* [Bytes.of()](/docs/org.apache.tuweni.bytes/-bytes/of.html)

[Bytes.of()](/docs/org.apache.tuweni.bytes/-bytes/of.html) takes a variadic argument of bytes:

{% highlight java %}
Bytes value = Bytes.of(0x00, 0x01, 0xff, 0x2a);
{% endhighlight %}

* [Bytes.ofUnsignedInt()](/docs/org.apache.tuweni.bytes/-bytes/of-unsigned-int.html)
* [Bytes.ofUnsignedLong()](/docs/org.apache.tuweni.bytes/-bytes/of-unsigned-long.html)
* [Bytes.ofUnsignedShort()](/docs/org.apache.tuweni.bytes/-bytes/of-unsigned-short.html)

{% highlight java %}
Bytes value = Bytes.ofUnsignedInt(42);
{% endhighlight %}

# More wrapping
### Use [`Bytes.wrapByteBuf(buffer)`](/docs/org.apache.tuweni.bytes/-bytes/wrap-byte-buf.html) to wrap a Netty `ByteBuf` object as a `Bytes` object.

{% highlight java %}
ByteBuf buffer = Unpooled.buffer(42);
Bytes.wrapByteBuf(buffer);
{% endhighlight %}

You can apply an offset and size parameter:

{% highlight java %}
Bytes value = Bytes.wrapByteBuf(buffer, 1, 1);
{% endhighlight %}

### Use [`Bytes.wrapByteBuffer(buffer)`](/docs/org.apache.tuweni.bytes/-bytes/wrap-byte-buffer.html) to wrap a `ByteBuffer` object as a `Bytes` object.

{% highlight java %}
Bytes.wrapByteBuffer(buffer);
{% endhighlight %}

You can apply an offset and size parameter:

{% highlight java %}
Bytes value = Bytes.wrapByteBuffer(buffer, 1, 1);
{% endhighlight %}


### Use [`Bytes.wrapBuffer(buffer)`](/docs/org.apache.tuweni.bytes/-bytes/wrap-byte-buffer.html) to wrap a Vert.x `Buffer` object as a `Bytes` object.

{% highlight java %}
Bytes.wrapBuffer(buffer);
{% endhighlight %}

You can apply an offset and size parameter:

{% highlight java %}
Bytes value = Bytes.wrapBuffer(buffer, 1, 1);
{% endhighlight %}

# Random

You can create random bytes objects of a given length with the [Bytes.random() method](/docs/org.apache.tuweni.bytes/-bytes/random.html):

{% highlight java %}
// create a Bytes object of 20 bytes:
Bytes.random(20);
{% endhighlight %}

Create a Bytes object with our own Random implementation:

{% highlight java %}
Random random = new SecureRandom();
...
Bytes.random(20, random);
{% endhighlight %}

---
description: Built-in Types in Golang
---

# 🈁 Types

## Basics

* `string` - "Hello, Gophers!" `%s`
* `bool` - true | false `%t`

## Numbers

### Integers

* `int` - -2147483648 to 2147483647 `%d`
* `int8` - -128 to 127 `%d`
* `int16` - -32768 to 32767 `%d`
* `int32` - -2147483648 to 2147483647 `%d`
* `int64` - -9223372036854775808 to 9223372036854775807 `%d`

### Unsigned Integers

{% hint style="info" %}
Unsigned integers are integers that are only positives.
{% endhint %}

* `uint` - 0 to 4294967295 `%d`
* `uint8` - 0 to 255 `%d`
* `uint16` - 0 to 65535 `%d`
* `uint32` - 0 to 4294967295 `%d`
* `uint64` - 0 to 18446744073709551615 `%d`

### Float (Decimals)

* `float32` - IEEE-754 32-bit floating-point numbers `%f`
* `float64` - IEEE-754 64-bit floating-point numbers `%f`
* `complex64` - complex numbers with float32 real and imaginary parts `%f`
* `complex128` - complex numbers with float64 real and imaginary parts `%f`

## Alias

* `byte` - alias for `uint8`
* `rune` - alias for `int32`

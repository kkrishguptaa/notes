---
description: How to work with Arrays in Golang?
---

# 🔄 Arrays

{% hint style="info" %}
Arrays start at index 0
{% endhint %}

## Declaration

```go
var names [3]string

names = ["Krish", "Kultiversan K", "K"]
```

## Accessing

```go
names[0] // "Krish"
```

## Assigning

```go
names[0] = "Karuto"
```

## Appending

```go
names = append(names, "Hellooo")
```

## Deleting

```go
names = append(names[:2], names[3:]...)
```

## Tips

> Tip: While defining variable, You can use `...` to let the compiler count the size for you

> Note: While defining variable, if is not specified, it is unbounded

> Note: When you use `arr[0:3]` you get the elements including index 0 to index 3, excluding index 3 (so 0, 1, 2)

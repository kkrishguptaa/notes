---
description: How to Import Files in Golang?
---

# 📥 Importing Other Files

{% hint style="warning" %}
You can only import variables, functions, and types that start with a capital letter that are public and in the scope of the package
{% endhint %}

```go
import "go-todo-api/types" // import package from module (module is the name in in go.mod)

types.Name // You can access this

types.name // You cannot access this as it does not start with capital letter
```

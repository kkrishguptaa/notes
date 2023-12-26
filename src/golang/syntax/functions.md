---
description: Declaring functions in Golang
---

# 🦙 Functions

### One Return Variable

<pre class="language-go"><code class="lang-go"><strong>// User &#x26; Format are argument types
</strong><strong>func getName(user User, format Format) string {
</strong>  return user.getDetails(format).name
}
</code></pre>

### Multiple Return Variable

```go
// User & Format are argument types
func getNameAndAge(user User, format Format) (string, int) {
  return user.getDetails(format).name, user.getDetails(format).age
}
```

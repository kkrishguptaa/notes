---
description: How to declare variables?
---

# ♒ Variables

## Types

### Based on mutability:

* Immutable (constants) - Cannot be changed
* Mutable (vars) - Can be changed

## Examples

### Vars

#### Without Assignment

```go
// declaration
var name string

// later in the code
name = "Krish Gupta"
```

#### With Assignment

```go
var name string = "Krish Gupta"
```

#### Inferred

```go
// one
name := "Krish Gupta"

// more than one
name, age := "Krish Gupta", 18
```

### Constants

#### Explicit Type

```go
const name string = "Krish Gupta"
```

#### Inferred Type

```go
const name = "Krish Gupta"
```

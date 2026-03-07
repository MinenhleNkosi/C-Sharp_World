# The var Keyword

The `var` keyword lets the compiler figure out the type of a variable from the value you assign to it. The variable is still strongly typed, but you don't have to write the type name yourself.

## Basic Usage

```cs
// Instead of writing:
int number = 42;
int doubled = number * 2;

// You can write:
var number = 42;      // Compiler knows this is an int
var doubled = number * 2;   // Compiler knows this is also an int
```

## var vs Explicit Types

| Explicit Type    | With var         | What the Compiler Sees |
| ---------------- | ---------------- | ---------------------- |
| `int x = 5;`     | `var x = 5;`     | `int`                  |
| `int y = x + 3;` | `var y = x + 3;` | `int`                  |
| `int z = x * 2;` | `var z = x * 2;` | `int`                  |

## Important Rules

```cs
// var MUST have a value - the compiler needs it to know the type
var x = 10;    // Valid
// var y;       // ERROR: Cannot use var without a value

// The type cannot change after it's set
var count = 5;
count = 10;    // Valid - still an int
// count = 3.14;  // ERROR: count is an int, not a double
```

## Visualization

```mermaid
flowchart TD
    A([The var Keyword]) --> B[Basic Usage]
    A --> C[var vs Explicit Types]
    A --> D[Important Rules]

    B --> B1[Compiler infers the type from the assigned value]
    B1 --> B2[Variable is still strongly typed]
    B2 --> B3[You just don't write the type name yourself]
    B3 --> B4[Example: var number = 42 - compiler knows this is int]
    B4 --> B5[Example: var doubled = number * 2 - compiler knows this is int]

    C --> C1[Explicit: int x = 5]
    C --> C2[Explicit: int y = x + 3]
    C --> C3[Explicit: int z = x * 2]
    C1 --> C1a[With var: var x = 5 - compiler sees int]
    C2 --> C2a[With var: var y = x + 3 - compiler sees int]
    C3 --> C3a[With var: var z = x * 2 - compiler sees int]

    D --> D1[var MUST be assigned a value at declaration]
    D --> D2[Type cannot change after it is set]
    D1 --> D1a{Value provided?}
    D1a --> |Yes - var x = 10| D1b[Valid - compiler infers type]
    D1a --> |No - var y| D1c[ERROR: compiler cannot infer type]
    D2 --> D2a{Assigning a different type later?}
    D2a --> |Same type - count = 10| D2b[Valid - still an int]
    D2a --> |Different type - count = 3.14| D2c[ERROR: count is int not double]
```

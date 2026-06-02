# Named Arguments

Named arguments let you specify which parameter receives which value by using the parameter name, allowing you to pass arguments in any order.

## Basic Syntax

```cs
// Method definition
void Greet(string name, int times, bool loud)
{
    // implementation
}

// Normal positional call - order matters
Greet("Sam", 3, true);

// Named arguments - order doesn't matter!
Greet(times: 3, loud: true, name: "Sam");
Greet(name: "Sam", loud: true, times: 3);
```

## Mixing Positional and Named

```cs
// Positional arguments must come BEFORE named ones
Greet("Sam", times: 3, loud: true);  // Valid - "Sam" is positional
Greet("Sam", 3, loud: true);          // Valid - only last is named

// This is INVALID - positional after named
// Greet(name: "Sam", 3, true);  // Won't compile!
```

## Why Use Named Arguments?

| Benefit          | Example                                        |
| ---------------- | ---------------------------------------------- |
| Clarity          | `Draw(x: 10, y: 20)` vs `Draw(10, 20)`         |
| Flexibility      | Skip thinking about parameter order            |
| Readability      | `SetAlarm(hour: 7, minute: 30, enabled: true)` |
| Selective naming | Name only confusing params                     |

# Visualization

```mermaid
flowchart TD
    A([Named Arguments in C#]) --> B[What are Named Arguments?]
    A --> C[Basic Syntax]
    A --> D[Mixing Positional and Named]
    A --> E[Why Use Named Arguments?]

    B --> B1[Specify which parameter receives which value using the parameter name]
    B1 --> B2[Arguments can be passed in any order when names are used]
    B2 --> B3[The compiler matches each value to its parameter by name not by position]
    B3 --> B4[Works with any method - no changes needed to the method definition]

    C --> C1[Normal positional call - Greet Sam 3 true - order is fixed]
    C --> C2[Named call - times 3 loud true name Sam - order is free]
    C --> C3[Named call - name Sam loud true times 3 - different order same result]
    C1 --> C4[Positional arguments rely entirely on declaration order to map correctly]
    C2 --> C5[Each argument carries its own label so position no longer matters]
    C3 --> C5
    C4 --> C6[Same method accepts both styles - caller chooses which to use]
    C5 --> C6

    D --> D1[Positional arguments must come before named arguments in the call]
    D --> D2[Invalid ordering - named argument followed by positional]
    D1 --> D1a[Greet Sam times 3 loud true - Sam is positional rest are named - valid]
    D1a --> D1b[Greet Sam 3 loud true - first two positional last one named - valid]
    D2 --> D2a[Greet name Sam 3 true - positional 3 appears after named name Sam]
    D2a --> D2b[Compiler cannot determine where the unlabelled value belongs - does not compile]
    D1b --> D3[Rule: positional arguments must always come before named ones in a call]
    D2b --> D3

    E --> E1[Clarity - makes the meaning of each argument obvious at the call site]
    E --> E2[Flexibility - removes the need to remember parameter order]
    E --> E3[Readability - self-documents calls with many or similar-typed parameters]
    E --> E4[Selective naming - name only the confusing parameters and leave the rest positional]
    E1 --> E1a[Draw x 10 y 20 makes intent clear vs Draw 10 20 which could be confused]
    E2 --> E2a[Skip thinking about order entirely when names are provided]
    E3 --> E3a[SetAlarm hour 7 minute 30 enabled true reads like a sentence]
    E4 --> E4a[Mix positional for obvious args and named for ambiguous ones in the same call]
    E1a --> E5[Named arguments cost nothing at runtime - the benefit is entirely for the reader]
    E2a --> E5
    E3a --> E5
    E4a --> E5
```

The flowchart branches into four sections. **What are Named Arguments?** establishes the core mechanic — the compiler matches by name rather than position — and confirms that no changes to the method definition are needed. **Basic Syntax** maps all three calling styles side by side, converging on the point that the same method accepts both positional and named calls and the caller freely chooses which to use. **Mixing Positional and Named** traces two valid mixed calls against one invalid one, converging on the rule that positional arguments must always precede named ones because the compiler has no way to place an unlabelled value once a named argument has appeared. **Why Use Named Arguments?** maps the four practical benefits — clarity, flexibility, readability, and selective naming — converging on the principle that named arguments are a zero-cost readability tool whose entire value is for the person reading the call site.

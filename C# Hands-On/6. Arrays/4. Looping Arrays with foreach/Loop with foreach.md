# The foreach Loop

The `foreach` loop provides a simpler way to iterate over collections when you don't need the index. It automatically handles iteration and gives you direct access to each element.

## Basic Syntax

```cs
foreach (Type variableName in collection)
{
    // Use variableName directly
}
```

## foreach vs for

```cs
// Using for - you manage the index
for (int i = 0; i < names.Length; i++)
{
    Console.WriteLine(names[i]);
}

// Using foreach - cleaner when you just need the values
foreach (string name in names)
{
    Console.WriteLine(name);
}
```

## When to Use foreach

- When you need to read each element in order
- When you don't need to know the index
- When you don't need to modify the array during iteration

## When to Use for Instead

- When you need the index for calculations
- When you need to modify array elements
- When you need to iterate in reverse or skip elements

# Visualization

```mermaid
flowchart TD
    A([The foreach Loop in C#]) --> B[What is foreach?]
    A --> C[Basic Syntax]
    A --> D[foreach vs for]
    A --> E[When to Use foreach]
    A --> F[When to Use for Instead]

    B --> B1[Simpler way to iterate over a collection without managing an index]
    B1 --> B2[Automatically advances through every element in order]
    B2 --> B3[Gives direct access to each element by value not by position]
    B3 --> B4[Preferred when you only need to read each element once from start to finish]

    C --> C1[Structure: foreach Type variableName in collection]
    C1 --> C2[Type matches the element type of the collection]
    C2 --> C3[variableName holds the current element on each iteration]
    C3 --> C4[in keyword separates the variable declaration from the collection]
    C4 --> C5[No initializer, condition, or iterator to write - loop handles all of it]

    D --> D1[for loop - you declare i, check i less than Length, increment i, access via index]
    D --> D2[foreach loop - declare element variable, loop manages everything else]
    D1 --> D1a[for int i = 0 - i less than names.Length - i++ then Console.WriteLine names at i]
    D2 --> D2a[foreach string name in names then Console.WriteLine name]
    D1a --> D3[for exposes the index at every step - more control but more ceremony]
    D2a --> D4[foreach hides the index entirely - less control but cleaner and safer]
    D3 --> D5[Both loops produce identical output when reading every element in order]
    D4 --> D5

    E --> E1[Reading each element in order from first to last]
    E --> E2[Index position is not needed anywhere in the loop body]
    E --> E3[Array elements should not be modified during iteration]
    E1 --> E4[foreach signals to the reader that every element will be visited exactly once]
    E2 --> E4
    E3 --> E4
    E4 --> E5[Use foreach as the default choice for simple read-only traversal]

    F --> F1[Index is needed for calculations inside the loop body]
    F --> F2[Array elements need to be modified during iteration]
    F --> F3[Iteration order is non-standard - reverse, skip, or step by more than one]
    F1 --> F1a[foreach provides no way to know the current position]
    F2 --> F2a[foreach variable is read-only - assigning to it does not change the array]
    F3 --> F3a[foreach always moves forward one element at a time with no variation]
    F1a --> F4[Reach for for whenever index access, mutation, or custom traversal order is needed]
    F2a --> F4
    F3a --> F4
```

The flowchart branches into five sections. **What is foreach?** establishes the core promise — automatic advancement through every element with no index to manage — and positions it as the default for read-only traversal. **Basic Syntax** breaks down each part of the foreach header, converging on the point that the loop handles all iteration mechanics so there is nothing to initialise, check, or increment manually. **foreach vs for** places both loops side by side against the same array, converging on the trade-off that for exposes more control while foreach offers less ceremony for identical output. **When to Use foreach** maps the three conditions that favour it, converging on the guideline that foreach signals to the reader that every element will be visited exactly once. **When to Use for Instead** maps the three conditions where foreach falls short, converging on the rule that for is the right reach whenever index access, element mutation, or a custom traversal order is needed.

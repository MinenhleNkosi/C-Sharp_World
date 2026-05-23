# What is an Array?

An **array** is a collection that holds multiple values of the same type in a single variable. Instead of creating separate variables for each item (like `fruit1`, `fruit2`, `fruit3`), you store them all together in one container.

## Creating Arrays

```cs
// Declare and initialize an array with values
string[] fruits = { "Apple", "Banana", "Cherry" };

// Declare an array with a specific size (all elements start as default values)
int[] numbers = new int[5]; // Creates array with 5 slots, all set to 0

// Declare and initialize with the new keyword
string[] colors = new string[] { "Red", "Green", "Blue" };
```

## Accessing Array Elements

Arrays use **zero-based indexing** - the first element is at index 0:

```cs
string[] fruits = { "Apple", "Banana", "Cherry" };
Console.WriteLine(fruits[0]); // Output: Apple
Console.WriteLine(fruits[1]); // Output: Banana
Console.WriteLine(fruits[2]); // Output: Cherry
```

## Array Length

Use the `Length` property to get the number of elements:

```cs
string[] fruits = { "Apple", "Banana", "Cherry" };
Console.WriteLine(fruits.Length); // Output: 3
```

## The Foreach Loop

The `foreach` loop is designed specifically for iterating over collections like arrays. It automatically handles the iteration, so you don't need to manage an index variable.

```cs
foreach (type variableName in collection)
{
    // Use variableName to access each element
}
Foreach vs For Loop
string[] names = { "Alice", "Bob", "Charlie" };

// For loop - you manage the index
for (int i = 0; i < names.Length; i++)
{
    Console.WriteLine(names[i]);
}

// Foreach loop - cleaner and safer
foreach (string name in names)
{
    Console.WriteLine(name);
}
```

## When to Use Foreach

- When you need to process every element in order
- When you don't need the index position
- When you want cleaner, more readable code

# Visualization

```mermaid
flowchart TD
    A([What is an Array? in C#]) --> B[What is an Array?]
    A --> C[Creating Arrays]
    A --> D[Accessing Elements]
    A --> E[Array Length]
    A --> F[The Foreach Loop]

    B --> B1[Holds multiple values of the same type in a single variable]
    B1 --> B2[Replaces separate variables like fruit1 fruit2 fruit3]
    B2 --> B3[All items stored together in one named container]
    B3 --> B4[Every element must be the same data type]

    C --> C1[Inline initializer - string[] fruits = Apple Banana Cherry]
    C --> C2[Fixed size declaration - int[] numbers = new int[5]]
    C --> C3[New keyword with values - new string[] Red Green Blue]
    C1 --> C4[Values provided at declaration time]
    C2 --> C4a[5 slots created, all default to 0]
    C3 --> C4
    C4 --> C5[Array size is fixed once created]
    C4a --> C5

    D --> D1[Arrays use zero-based indexing]
    D1 --> D2[First element is always at index 0]
    D2 --> D3[fruits[0] returns Apple]
    D2 --> D4[fruits[1] returns Banana]
    D2 --> D5[fruits[2] returns Cherry]
    D3 --> D6[Index is always one less than the position number]
    D4 --> D6
    D5 --> D6

    E --> E1[Use the Length property to count elements]
    E1 --> E2[fruits.Length returns 3 for a three-element array]
    E2 --> E3[Commonly used in for loop conditions - i < array.Length]
    E3 --> E4[Prevents accessing an index that does not exist]

    F --> F1[Syntax: foreach type variableName in collection]
    F --> F2[Foreach vs For Loop]
    F --> F3[When to use foreach]
    F1 --> F1a[Automatically advances through every element in order]
    F1a --> F1b[No index variable needed - loop handles iteration internally]
    F2 --> F2a[For loop - you declare i, check i < Length, increment i manually]
    F2 --> F2b[Foreach loop - cleaner syntax, no index management required]
    F2a --> F2c[Use for when you need the index position]
    F2b --> F2c
    F3 --> F3a[Processing every element in order]
    F3 --> F3b[Index position is not needed]
    F3 --> F3c[Readability and safety are the priority]
    F3a --> F4[Foreach is the default choice for simple array traversal]
    F3b --> F4
    F3c --> F4
```

The flowchart branches into five sections. **What is an Array?** establishes the core concept — a single container replacing many individual variables — with the constraint that all elements share one type. **Creating Arrays** maps the three declaration styles, converging on the rule that array size is fixed once created. **Accessing Elements** traces zero-based indexing showing how each index maps to a specific value and converging on the off-by-one principle that an index is always one less than its position. **Array Length** shows how the `Length` property is used and why it matters for safe iteration. **The Foreach Loop** contrasts foreach against for, maps three conditions that favour foreach, and converges on the guideline that foreach is the default choice for simple array traversal whenever the index is not needed.

# While Loops

A while loop repeatedly executes a block of code as long as a condition remains true. Use it when you don't know exactly how many times you need to iterate.

## Basic Syntax

```cs
while (condition)
{
    // code to execute
}
```

The loop checks the condition before each iteration. If the condition is false initially, the loop body never executes.

## Loop Components

```cs
int counter = 1;        // 1. Initialize a counter variable
while (counter <= 3)    // 2. Condition checked before each iteration
{
    Console.WriteLine(counter);  // 3. Loop body
    counter++;                   // 4. Update counter (crucial!)
}
// Output: 1, 2, 3 (each on new line)
```

## Common Patterns

```cs
// Counting up
int i = 0;
while (i < 5)
{
    Console.WriteLine(i);  // Prints 0, 1, 2, 3, 4
    i++;
}

// Counting down
int j = 5;
while (j > 0)
{
    Console.WriteLine(j);  // Prints 5, 4, 3, 2, 1
    j--;
}
```

## Infinite Loop Warning

```cs
// DANGER: This runs forever!
int x = 1;
while (x <= 5)
{
    Console.WriteLine(x);
    // Missing x++ means x is always 1!
}
```

Always ensure your loop condition will eventually become false.

# Visualization

Here's the while loop diagram in the same style — plain Mermaid markdown with a summary paragraph, ready to copy:

```mermaid
flowchart TD
    A([While Loops in C#]) --> B[What is a While Loop?]
    A --> C[Syntax and Structure]
    A --> D[Loop Components]
    A --> E[Common Patterns]
    A --> F[Infinite Loop Warning]

    B --> B1[Repeats a block of code while condition is true]
    B1 --> B2[Use when iteration count is not known in advance]
    B2 --> B3[Condition is checked before each iteration]
    B3 --> B4[If condition is false initially, body never executes]

    C --> C1[Structure: while condition - code to execute]
    C1 --> C2{Is condition true?}
    C2 --> |Yes| C3[Execute the loop body]
    C2 --> |No| C4[Skip loop entirely]
    C3 --> C5[Re-check condition on next iteration]
    C4 --> C6[Continue with code after loop]

    D --> D1[Step 1 - Initialize]
    D --> D2[Step 2 - Condition]
    D --> D3[Step 3 - Loop body]
    D --> D4[Step 4 - Update]
    D1 --> D1a[Declare counter variable before loop - int counter = 1]
    D2 --> D2a[Checked before every iteration - counter <= 3]
    D3 --> D3a[Code that runs each pass - Console.WriteLine counter]
    D4 --> D4a[Modify counter to progress the loop - counter++]
    D4a --> D4b[Output: 1 then 2 then 3 each on new line]

    E --> E1[Counting up]
    E --> E2[Counting down]
    E1 --> E1a[i = 0 while i < 5 with i++]
    E1a --> E1b[Prints 0 1 2 3 4]
    E2 --> E2a[j = 5 while j > 0 with j--]
    E2a --> E2b[Prints 5 4 3 2 1]

    F --> F1[Missing update means condition never becomes false]
    F --> F2[Loop runs forever and freezes the program]
    F1 --> F1a[Example: x = 1 while x <= 5 with no x++]
    F1a --> F1b[x stays 1 so condition is always true]
    F2 --> F2a[Always ensure the update moves toward a false condition]
    F1b --> F3[Rule: every while loop must have a path to false]
    F2a --> F3
```

The flowchart branches into five sections. **What is a While Loop?** establishes the concept and its pre-check behaviour. **Syntax and Structure** traces the decision flow showing how the condition gates entry into the loop body. **Loop Components** walks through the four required steps — initialize, check, execute, and update — grounding them in a concrete counter example. **Common Patterns** contrasts counting up and counting down as the two most typical use cases. **Infinite Loop Warning** maps the danger of a missing update step, with both branches converging on the rule that every while loop must have a clear path to a false condition.

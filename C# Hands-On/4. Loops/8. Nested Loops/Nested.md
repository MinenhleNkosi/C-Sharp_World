# Nested Loops

A nested loop is a loop placed inside another loop. The inner loop completes all its iterations for each single iteration of the outer loop.

## Basic Structure

```cs
for (int outer = 1; outer <= 3; outer++)
{
    for (int inner = 1; inner <= 3; inner++)
    {
        Console.Write($"({outer},{inner}) ");
    }
    Console.WriteLine(); // New line after inner loop completes
}

// Output:
// (1,1) (1,2) (1,3)
// (2,1) (2,2) (2,3)
// (3,1) (3,2) (3,3)
```

## How Nested Loops Execute

1. Outer loop starts: outer = 1
2. Inner loop runs completely: inner = 1, 2, 3
3. Outer loop increments: outer = 2
4. Inner loop runs completely again: inner = 1, 2, 3
5. This continues until outer loop finishes

## Common Uses

| Pattern          | Description                           |
| ---------------- | ------------------------------------- |
| Grid/Table       | Process rows and columns              |
| Matrix           | Access 2D data structures             |
| Pattern printing | Create shapes with characters         |
| Comparisons      | Compare each element with every other |

# Visualization

```mermaid
flowchart TD
    A([Nested Loops in C#]) --> B[What is a Nested Loop?]
    A --> C[Basic Structure]
    A --> D[How Nested Loops Execute]
    A --> E[Common Uses]

    B --> B1[A loop placed inside another loop]
    B1 --> B2[The inner loop completes all its iterations for each single outer iteration]
    B2 --> B3[Outer loop controls rows - inner loop controls columns]
    B3 --> B4[Total iterations equals outer count multiplied by inner count]

    C --> C1[Outer loop: for int outer = 1 - outer <= 3 - outer++]
    C --> C2[Inner loop: for int inner = 1 - inner <= 3 - inner++]
    C1 --> C3[Each outer iteration triggers a full run of the inner loop]
    C2 --> C3
    C3 --> C4[Console.Write prints outer and inner pair on same line]
    C4 --> C5[Console.WriteLine after inner loop moves to next line]
    C5 --> C6[Output: 1,1 1,2 1,3 then 2,1 2,2 2,3 then 3,1 3,2 3,3]

    D --> D1[Step 1 - outer = 1 - inner loop runs: inner = 1 2 3]
    D1 --> D2[Step 2 - outer increments to 2 - inner loop resets and runs: inner = 1 2 3]
    D2 --> D3[Step 3 - outer increments to 3 - inner loop resets and runs: inner = 1 2 3]
    D3 --> D4[Step 4 - outer increments to 4 - outer condition false - loop exits]
    D4 --> D5[Inner loop always resets to its initializer at the start of each outer iteration]
    D5 --> D6[3 outer iterations times 3 inner iterations equals 9 total executions]

    E --> E1[Grid and Table]
    E --> E2[Matrix]
    E --> E3[Pattern printing]
    E --> E4[Comparisons]
    E1 --> E1a[Outer loop iterates rows - inner loop iterates columns]
    E1a --> E1b[Each cell addressed by its row and column index pair]
    E2 --> E2a[Outer index selects a row in a 2D structure]
    E2a --> E2b[Inner index selects an element within that row]
    E3 --> E3a[Outer loop controls number of rows in the shape]
    E3a --> E3b[Inner loop controls number of characters per row]
    E4 --> E4a[Outer loop picks each element as the reference]
    E4a --> E4b[Inner loop compares that element against every other element]
    E1b --> E5[All four patterns share the same principle: outer sets context, inner does the work]
    E2b --> E5
    E3b --> E5
    E4b --> E5
```

The flowchart branches into four sections. **What is a Nested Loop?** establishes the core mechanic — the inner loop runs to completion on every single outer iteration — and introduces the multiplication rule for calculating total executions. **Basic Structure** maps the two loop headers and traces the output line by line, showing how `Console.Write` and `Console.WriteLine` work together to produce the grid layout. **How Nested Loops Execute** walks through all three outer iterations step by step, highlighting that the inner loop always resets to its initializer and converging on the total of nine executions. **Common Uses** maps the four canonical patterns — grids, matrices, pattern printing, and comparisons — converging on the unifying principle that the outer loop always sets the context while the inner loop performs the repeated work within it.

# Do-While Loops

A do-while loop executes its body at least once before checking the condition. This is perfect for scenarios where you need to do something first, then decide whether to continue.

## Syntax

```cs
do
{
    // Code executes at least once
} while (condition);
```

## While vs Do-While

```cs
// While loop - might never execute
int x = 10;
while (x < 5)
{
    Console.WriteLine("This never prints");
}

// Do-while loop - always executes at least once
int y = 10;
do
{
    Console.WriteLine("This prints once!");
} while (y < 5);
```

## Counter-Controlled Do-While

Do-while loops work well with counters when you need at least one iteration:

```cs
int count = 1;
do
{
    Console.WriteLine($"Count: {count}");
    count++;
} while (count <= 3);
// Prints: Count: 1, Count: 2, Count: 3
```

## Common Use Cases

| Use Case     | Why Do-While?                        |
| ------------ | ------------------------------------ |
| Menu systems | Must show menu at least once         |
| Retry logic  | Must attempt operation at least once |
| Game loops   | Must run at least one frame          |
| Processing   | Must process at least one item       |

# Visualization

```mermaid
flowchart TD
    A([Do-While Loops in C#]) --> B[What is a Do-While Loop?]
    A --> C[Syntax and Structure]
    A --> D[While vs Do-While]
    A --> E[Counter-Controlled Do-While]
    A --> F[Common Use Cases]

    B --> B1[Executes the body at least once before checking the condition]
    B1 --> B2[Unlike while loops the condition is checked at the end]
    B2 --> B3[Use when something must happen before deciding to continue]
    B3 --> B4[Guarantees one execution regardless of condition]

    C --> C1[Structure: do - code block - while condition with semicolon]
    C1 --> C2[Execute body first]
    C2 --> C3{Is condition true?}
    C3 --> |Yes| C2
    C3 --> |No| C4[Exit loop]
    C4 --> C5[Semicolon after while condition is required]

    D --> D1[While loop - condition checked before body]
    D --> D2[Do-while loop - condition checked after body]
    D1 --> D1a[x = 10 while x < 5]
    D1a --> D1b[Condition is false immediately - body never runs]
    D2 --> D2a[y = 10 do block while y < 5]
    D2a --> D2b[Body runs once then condition checked - prints one time]
    D1b --> D3[Key difference: do-while always runs the body at least once]
    D2b --> D3

    E --> E1[count = 1 - do block - while count <= 3]
    E1 --> E2[Iteration 1 - prints Count: 1 then count becomes 2]
    E2 --> E3[Iteration 2 - prints Count: 2 then count becomes 3]
    E3 --> E4[Iteration 3 - prints Count: 3 then count becomes 4]
    E4 --> E5[count is 4 so count <= 3 is false - loop exits]
    E5 --> E6[Output: Count: 1 then Count: 2 then Count: 3]

    F --> F1[Menu systems]
    F --> F2[Retry logic]
    F --> F3[Game loops]
    F --> F4[Processing]
    F1 --> F1a[Must display menu before user can make a choice]
    F2 --> F2a[Must attempt the operation before knowing if retry is needed]
    F3 --> F3a[Must render at least one frame before checking quit condition]
    F4 --> F4a[Must process at least one item before checking for more]
    F1a --> F5[Common thread: action must come before the decision to repeat]
    F2a --> F5
    F3a --> F5
    F4a --> F5
```

The flowchart branches into five sections. **What is a Do-While Loop?** establishes the core guarantee — the body always runs at least once because the condition lives at the end. **Syntax and Structure** traces the execution order showing the body fires before the condition is ever evaluated. **While vs Do-While** contrasts both loop types with the same starting value, converging on the key difference that do-while cannot be skipped entirely. **Counter-Controlled Do-While** walks through each iteration of a concrete counter example showing exactly how the output is produced. **Common Use Cases** maps the four canonical scenarios — menus, retries, game loops, and processing — and converges on the shared principle that the action must precede the decision to repeat.

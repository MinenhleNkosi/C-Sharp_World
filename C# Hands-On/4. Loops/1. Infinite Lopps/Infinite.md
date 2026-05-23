# Avoiding Infinite Loops

An infinite loop occurs when the loop condition never becomes false, causing the program to run forever (or until it crashes).

## hy Loops Become Infinite

```cs
// BROKEN - counter never changes, so counter <= 5 is always true
int counter = 1;
while (counter <= 5)
{
    Console.WriteLine(counter);
    // Missing: counter++;
}

// FIXED - counter increases, eventually making counter <= 5 false
int counter = 1;
while (counter <= 5)
{
    Console.WriteLine(counter);
    counter++;  // This ensures termination!
}
```

## The Termination Rule

Every while loop needs something inside its body that moves it closer to the exit condition:

| Loop Type     | What Must Change           | Example                      |
| ------------- | -------------------------- | ---------------------------- |
| Counting up   | Increment the counter      | `counter++`                  |
| Counting down | Decrement the counter      | `counter--`                  |
| Searching     | Update the search position | `index++`                    |
| Input-based   | Read new input             | `input = Console.ReadLine()` |

## Common Mistakes

```cs
// Mistake 1: Forgetting to update the variable
int i = 0;
while (i < 10)
{
    Console.WriteLine(i);
    // Oops! i never changes
}

// Mistake 2: Updating in the wrong direction
int i = 0;
while (i < 10)
{
    Console.WriteLine(i);
    i--;  // Going the wrong way!
}

// Mistake 3: Condition can never be false
int x = 5;
while (x > 0)
{
    Console.WriteLine(x);
    x++;  // x gets bigger, never reaches 0
}
```

# visualization

```mermaid
flowchart TD
    A([Avoiding Infinite Loops in C#]) --> B[What is an Infinite Loop?]
    A --> C[The Termination Rule]
    A --> D[Common Mistakes]
    A --> E[Broken vs Fixed]

    B --> B1[Loop condition never becomes false]
    B1 --> B2[Program runs forever or until it crashes]
    B2 --> B3[Caused by a missing or incorrect update step]
    B3 --> B4[Every while loop must have a path to false]

    C --> C1[Something inside the body must move toward the exit condition]
    C1 --> C2[Counting up - increment the counter - counter++]
    C1 --> C3[Counting down - decrement the counter - counter--]
    C1 --> C4[Searching - advance the position - index++]
    C1 --> C5[Input-based - read new input - input = Console.ReadLine]
    C2 --> C6[Rule: each iteration must bring condition closer to false]
    C3 --> C6
    C4 --> C6
    C5 --> C6

    D --> D1[Mistake 1 - Forgetting to update]
    D --> D2[Mistake 2 - Updating in the wrong direction]
    D --> D3[Mistake 3 - Condition can never be false]
    D1 --> D1a[i = 0 while i < 10 with no i++]
    D1a --> D1b[i stays 0 forever - condition always true]
    D2 --> D2a[i = 0 while i < 10 with i--]
    D2a --> D2b[i goes negative - never reaches 10]
    D3 --> D3a[x = 5 while x > 0 with x++]
    D3a --> D3b[x grows away from 0 - exits only by crashing]
    D1b --> D4[All three mistakes share the same root cause]
    D2b --> D4
    D3b --> D4
    D4[Update does not move condition toward false]

    E --> E1[Broken - counter never changes]
    E --> E2[Fixed - counter increases each iteration]
    E1 --> E1a[counter = 1 while counter <= 5 - no counter++]
    E1a --> E1b[counter stays 1 so loop never exits]
    E2 --> E2a[counter = 1 while counter <= 5 with counter++]
    E2a --> E2b[counter reaches 6 making condition false]
    E1b --> E3[Ask: does every iteration change the variable the condition depends on?]
    E2b --> E3
```

The flowchart branches into four sections. **What is an Infinite Loop?** defines the problem and traces it back to a missing or incorrect update step. **The Termination Rule** maps the four loop types — counting, searching, and input-based — converging on the principle that every iteration must bring the condition closer to false. **Common Mistakes** walks through the three classic errors (no update, wrong direction, condition that grows away from false) and shows they all share the same root cause. **Broken vs Fixed** contrasts the two counter examples side by side, ending with a diagnostic question to apply when writing any while loop.

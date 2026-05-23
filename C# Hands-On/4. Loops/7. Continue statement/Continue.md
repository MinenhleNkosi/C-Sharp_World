# The continue Statement

The `continue` statement skips the rest of the current loop iteration and jumps to the next one. Unlike `break` which exits the loop entirely, `continue` just moves on to the next cycle.

## Basic Usage

```cs
for (int i = 1; i <= 5; i++)
{
    if (i == 3)
    {
        continue; // Skip when i is 3
    }
    Console.WriteLine(i);
}
// Output: 1, 2, 4, 5 (3 is skipped)
```

## break vs continue

| Statement  | Behavior                  | Use When                       |
| ---------- | ------------------------- | ------------------------------ |
| `break`    | Exits the loop completely | You found what you need        |
| `continue` | Skips to next iteration   | Current item should be ignored |

```cs
// break example - stops at 3
for (int i = 1; i <= 5; i++)
{
    if (i == 3) break;
    Console.WriteLine(i);
}
// Output: 1, 2

// continue example - skips 3
for (int i = 1; i <= 5; i++)
{
    if (i == 3) continue;
    Console.WriteLine(i);
}
// Output: 1, 2, 4, 5
```

## Checking Multiples

Use the modulo operator `%` to check if a number is a multiple of another:

```cs
if (number % 3 == 0)  // True if number is a multiple of 3
```

# Visualization

```mermaid
flowchart TD
    A([The continue Statement in C#]) --> B[What is continue?]
    A --> C[Basic Usage]
    A --> D[break vs continue]
    A --> E[Checking Multiples]

    B --> B1[Skips the rest of the current iteration and jumps to the next one]
    B1 --> B2[Unlike break it does not exit the loop entirely]
    B2 --> B3[Remaining code in the current cycle is ignored]
    B3 --> B4[Use when the current item should be skipped but the loop should continue]

    C --> C1[for int i = 1 - i <= 5 - i++ with if i == 3 continue]
    C1 --> C2[i = 1 - condition false - prints 1]
    C2 --> C3[i = 2 - condition false - prints 2]
    C3 --> C4[i = 3 - condition true - continue fires]
    C4 --> C5[Console.WriteLine skipped - jumps to i++]
    C5 --> C6[i = 4 - condition false - prints 4]
    C6 --> C7[i = 5 - condition false - prints 5]
    C7 --> C8[Output: 1 2 4 5 - 3 is absent from output]

    D --> D1[break - exits the loop completely]
    D --> D2[continue - skips to the next iteration]
    D1 --> D1a[for i = 1 to 5 - if i == 3 break]
    D1a --> D1b[Loop stops at 3 - 3 4 5 never reached]
    D1b --> D1c[Output: 1 2]
    D2 --> D2a[for i = 1 to 5 - if i == 3 continue]
    D2a --> D2b[i = 3 skipped but loop resumes at i = 4]
    D2b --> D2c[Output: 1 2 4 5]
    D1c --> D3[break ends the loop - continue only skips one cycle]
    D2c --> D3
    D3 --> D4[Use break when done searching - use continue when filtering unwanted items]

    E --> E1[Modulo operator % returns the remainder after division]
    E1 --> E2[If number % 3 == 0 then number is a multiple of 3]
    E2 --> E3[9 % 3 == 0 is true - 9 is a multiple of 3]
    E2 --> E4[10 % 3 == 1 is false - 10 is not a multiple of 3]
    E3 --> E5[Pair with continue to skip multiples and process only non-matching values]
    E4 --> E5
```

The flowchart branches into four sections. **What is continue?** establishes the distinction up front — continue skips one cycle while the loop itself keeps running, making it the right tool for filtering rather than stopping. **Basic Usage** traces every iteration of the counting example step by step, showing exactly where continue fires, which line gets skipped, and why 3 is absent from the output. **break vs continue** runs both statements against identical loops converging on the core rule: break ends the search entirely while continue filters out a single unwanted item and moves on. **Checking Multiples** introduces the modulo operator, maps a true and false case, and converges on its natural pairing with continue for skipping over values that match an unwanted pattern.

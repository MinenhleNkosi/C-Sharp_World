# Your Task

Use a do-while loop to display a menu exactly 3 times. Each iteration should:

1. Display the menu header `=== MENU ===`
2. Display three menu options
3. Display the current iteration number

The loop should continue while the counter is less than or equal to 3.

## Menu Format (each iteration)

```
=== MENU ===
1. Exit
2. Say Hello
3. Say Goodbye
Iteration: [number]
```

## Method Signature

```cs
public static void DisplayMenu()
```

## Expected Output

```
=== MENU ===
1. Exit
2. Say Hello
3. Say Goodbye
Iteration: 1
=== MENU ===
1. Exit
2. Say Hello
3. Say Goodbye
Iteration: 2
=== MENU ===
1. Exit
2. Say Hello
3. Say Goodbye
Iteration: 3
```

## Hints

- Use do `{ ... } while (condition);` - don't forget the semicolon after the condition!.
- Initialize a counter variable (e.g., `int counter = 1;`) before the do-while loop.
- Increment the counter inside the loop with `counter++` after printing.
- The while condition should check `counter <= 3` to loop exactly 3 times.

## Code Format Example

```cs
using System;

public class Solution
{
    public static void DisplayMenu()
    {
        // Create a do-while loop that:
        // 1. Displays the menu header
        // 2. Displays menu options
        // 3. Displays a counter value
        // 4. Continues while counter is less than 3

        // Menu format:
        // === MENU ===
        // 1. Exit
        // 2. Say Hello
        // 3. Say Goodbye
        // Iteration: [number]

        // Your code here

    }
}
```

# Your Task

The starter code has a broken while loop that would run forever. Fix it by adding the missing line that ensures the loop eventually terminates.

The loop should print numbers 1 through 5, one per line.

## Method Signature

```cs
public static void FixInfiniteLoop()
```

## Expected Output

```
1
2
3
4
5
```

## Hints

- Look at the loop condition: `counter <= 5`. What needs to happen for this to eventually become false?
- The variable `counter` starts at 1. For the loop to stop, `counter` needs to become greater than 5.
- Add `counter++` inside the loop to increment the counter after each iteration.

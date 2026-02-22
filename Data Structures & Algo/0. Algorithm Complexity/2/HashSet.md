# HashSet for O(1) Lookups

A `HashSet<T>` stores unique values and provides **O(1)** average-time operations for **Add**, **Remove**, and **Contains**. This makes it perfect for tracking "have I seen this before?" scenarios.

## O(n²) vs O(n) Comparison

```cs
// O(n²) - Nested loops approach
for (int i = 0; i < numbers.Length; i++)
{
    for (int j = i + 1; j < numbers.Length; j++)
    {
        if (numbers[i] == numbers[j]) return true;
    }
}

// O(n) - HashSet approach
var seen = new HashSet<int>();
foreach (int num in numbers)
{
    if (!seen.Add(num)) return true;  // Add returns false if already exists
}
```

## Why HashSet.Add Returns a Boolean

The `Add` method returns `true` if the element was successfully, or `false` if it already exists. This single operation both checks and adds in **O(1)** time:

```cs
var set = new HashSet<int>();
set.Add(5);  // returns true (5 added)
set.Add(3);  // returns true (3 added)
set.Add(5);  // returns false (5 already exists!)
```

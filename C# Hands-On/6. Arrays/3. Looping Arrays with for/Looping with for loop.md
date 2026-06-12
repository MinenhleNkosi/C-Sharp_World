# Looping Arrays with for

The `for` loop is the classic way to iterate through arrays when you need access to the index. It gives you precise control over which elements to access and in what order.

## The Length Property

Every array has a `Length` property that tells you how many elements it contains:

```cs
int[] scores = { 85, 92, 78 };
Console.WriteLine(scores.Length); // Output: 3
```

## Basic For Loop Pattern

The standard pattern for iterating through an entire array:

```cs
int[] values = { 10, 20, 30, 40 };

for (int i = 0; i < values.Length; i++)
{
    Console.WriteLine(values[i]);
}
// Output:
// 10
// 20
// 30
// 40
```

## Understanding the Loop

| Part                | Meaning                                 |
| ------------------- | --------------------------------------- |
| `int i = 0`         | Start at index 0 (first element)        |
| `i < values.Length` | Continue while index is valid           |
| `i++`               | Move to next index after each iteration |
| `values[i]`         | Access element at current index         |

## Why Use i < Length (Not <=)?

Arrays are zero-indexed, so valid indices are `0` to `Length - 1`:

```cs
int[] arr = { 5, 10, 15 };
// Length is 3
// Valid indices: 0, 1, 2
// Using i <= arr.Length would try to access index 3 (error!)
```

# Visualization

```mermaid
flowchart TD
    A([Looping Arrays with for in C#]) --> B[The Length Property]
    A --> C[Basic For Loop Pattern]
    A --> D[Understanding the Loop Parts]
    A --> E[Why Less Than and Not Less Than or Equal]

    B --> B1[Every array exposes a Length property]
    B1 --> B2[Length returns the total number of elements the array holds]
    B2 --> B3[int array scores = 85 92 78 - scores.Length returns 3]
    B3 --> B4[Length is used in the loop condition to know when to stop]

    C --> C1[int array values = 10 20 30 40]
    C1 --> C2[for int i = 0 - i less than values.Length - i++]
    C2 --> C3[Iteration 1 - i = 0 - values at 0 prints 10]
    C3 --> C4[Iteration 2 - i = 1 - values at 1 prints 20]
    C4 --> C5[Iteration 3 - i = 2 - values at 2 prints 30]
    C5 --> C6[Iteration 4 - i = 3 - values at 3 prints 40]
    C6 --> C7[i increments to 4 - 4 is not less than 4 - loop exits]
    C7 --> C8[Output: 10 then 20 then 30 then 40]

    D --> D1[int i = 0 - start at index 0 which is the first element]
    D --> D2[i less than values.Length - continue only while the index is valid]
    D --> D3[i++ - advance to the next index after each iteration]
    D --> D4[values at i - access whichever element the current index points to]
    D1 --> D5[Initializer anchors the loop at the first valid index]
    D2 --> D5
    D3 --> D5
    D4 --> D5
    D5 --> D6[All four parts work together to walk every element exactly once]

    E --> E1[int array arr = 5 10 15 - Length is 3]
    E1 --> E2[Valid indices are 0 1 and 2 - there is no index 3]
    E2 --> E3[Using i less than arr.Length stops at i = 2 - all elements covered safely]
    E2 --> E4[Using i less than or equal to arr.Length allows i = 3 - index 3 does not exist]
    E3 --> E5[Loop ends correctly after the last valid element]
    E4 --> E6[Accessing index 3 throws an IndexOutOfRangeException at runtime]
    E5 --> E7[Rule: always use i less than Length not less than or equal - last valid index is always Length minus 1]
    E6 --> E7
```

The flowchart branches into four sections. **The Length Property** establishes that every array carries a Length value and that it is what the loop condition relies on to know when to stop. **Basic For Loop Pattern** traces all four iterations of the values array step by step, showing exactly which index is active, which value is printed, and how the loop exits cleanly when i reaches 4. **Understanding the Loop Parts** maps each of the four loop components to its purpose and converges on the principle that all four work together to walk every element exactly once. **Why Less Than and Not Less Than or Equal** contrasts the safe and unsafe conditions against the same array, converging on the exception that fires at runtime when the boundary is crossed and closing with the rule that the last valid index is always Length minus 1.

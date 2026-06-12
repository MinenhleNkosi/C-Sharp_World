# Modifying Array Elements

Arrays are mutable, meaning you can change their elements after creation. You access and modify elements using their index position.

## Accessing Elements by Index

```cs
int[] scores = { 85, 90, 78 };

// Reading an element
int firstScore = scores[0];  // 85

// Modifying an element
scores[0] = 95;  // First element is now 95
scores[2] = 82;  // Third element is now 82
```

## Remember: Zero-Based Indexing

```cs
string[] fruits = { "apple", "banana", "cherry" };
//                    [0]       [1]        [2]

// The "second" element is at index 1
fruits[1] = "blueberry";  // Changes "banana" to "blueberry"
```

## Common Mistake

```cs
int[] nums = { 10, 20, 30 };

// WRONG: Trying to access the "second" position with index 2
// nums[2] is actually the THIRD element (value 30)

// CORRECT: The second element is at index 1
nums[1] = 99;  // Changes 20 to 99
```

# Visualization

```mermaid
flowchart TD
    A([Modifying Array Elements in C#]) --> B[Arrays are Mutable]
    A --> C[Accessing and Modifying by Index]
    A --> D[Zero-Based Indexing Reminder]
    A --> E[Common Mistake]

    B --> B1[Array elements can be changed after the array is created]
    B1 --> B2[The array size stays fixed but the values inside can be overwritten]
    B2 --> B3[Use the same square bracket notation for both reading and writing]
    B3 --> B4[Assigning to an index replaces whatever value was previously stored there]

    C --> C1[int array scores = 85 90 78]
    C1 --> C2[Reading - int firstScore = scores at index 0 - firstScore holds 85]
    C1 --> C3[Modifying - scores at index 0 = 95 - first element is now 95]
    C1 --> C4[Modifying - scores at index 2 = 82 - third element is now 82]
    C2 --> C5[Reading retrieves the current value without changing the array]
    C3 --> C6[Writing overwrites the slot - the old value is gone]
    C4 --> C6
    C5 --> C7[Same index syntax used for both - left of equals writes, right of equals reads]
    C6 --> C7

    D --> D1[string array fruits = apple banana cherry]
    D1 --> D2[apple sits at index 0 - banana at index 1 - cherry at index 2]
    D2 --> D3[The second element is at index 1 not index 2]
    D3 --> D4[fruits at index 1 = blueberry - changes banana to blueberry]
    D4 --> D5[Position in plain language is always one more than the index number]

    E --> E1[int array nums = 10 20 30]
    E1 --> E2[Wrong assumption - treating index 2 as the second position]
    E1 --> E3[Correct understanding - index 2 is the third element holding value 30]
    E2 --> E4[nums at index 2 = 99 modifies 30 not 20 - silent wrong result]
    E3 --> E5[nums at index 1 = 99 correctly changes 20 to 99]
    E4 --> E6[No error is thrown - the wrong element is silently overwritten]
    E5 --> E6
    E6 --> E7[Rule: always subtract 1 from the human position to get the correct index]
```

The flowchart branches into four sections. **Arrays are Mutable** establishes that while the size is fixed the values are not, and that the same square bracket notation covers both reading and writing. **Accessing and Modifying by Index** traces the scores array through one read and two writes, converging on the rule that the position of an expression relative to the equals sign determines whether it reads or overwrites. **Zero-Based Indexing Reminder** maps each fruit to its index and traces the blueberry assignment, converging on the off-by-one principle that a plain-language position is always one greater than its index. **Common Mistake** runs the wrong and correct assumptions side by side against the same array, converging on the warning that accessing the wrong index produces no error and silently overwrites the unintended element, closing with the rule to always subtract 1 from the human position to land on the correct index.

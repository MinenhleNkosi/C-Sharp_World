# O(log n) Complexity - Binary Search

Binary search is the classic example of **O(log n)** complexity. Instead of checking every element like linear search O(n), binary search **halves the search space** with each comparison.

## How Binary Search Works

```cs
// On a sorted array [1, 3, 5, 7, 9, 11, 13]
// Searching for 11:

// Step 1: Check middle (7) - 11 > 7, search right half
// Step 2: Check middle of [9, 11, 13] which is 11 - Found!
// Total: 2 steps instead of 6 with linear search
```

## Why O(log n) is Powerful

| Array Size | Linear Search O(n) | Binary Search O(log n) |
| ---------- | ------------------ | ---------------------- |
| 100        | up to 100 steps    | up to 7 steps          |
| 1,000      | up to 1,000 steps  | up to 10 steps         |
| 1,000,000  | up to 1M steps     | up to 20 steps         |

Each step halves the remaining elements: `n → n/2 → n/4 → n/8 → ... → 1`
The number of times you can halve `n` until reaching 1 is **log₂(n)**.

## Binary Search Algorithm

```cs
// 1. Start with left = 0, right = length - 1
// 2. Calculate middle index: mid = left + (right - left) / 2
// 3. Compare middle element to target:
//    - If equal: found it!
//    - If target is larger: search right half (left = mid + 1)
//    - If target is smaller: search left half (right = mid - 1)
// 4. Repeat until left > right (not found)
```

## Visualization

```mermaid
flowchart TD
    A([O-log n Complexity - Binary Search]) --> B[How Binary Search Works]
    A --> C[Why O-log n is Powerful]
    A --> D[Binary Search Algorithm]

    B --> B1[Start with sorted array]
    B1 --> B2[Check the middle element]
    B2 --> B3{Is it the target?}
    B3 --> |Yes| B4[Found it!]
    B3 --> |Target is larger| B5[Search right half]
    B3 --> |Target is smaller| B6[Search left half]
    B5 --> B2
    B6 --> B2

    B --> B7[Example: Find 11 in 1, 3, 5, 7, 9, 11, 13]
    B7 --> B8[Step 1: Check middle 7 - 11 is larger, search right]
    B8 --> B9[Step 2: Check middle of 9, 11, 13 which is 11 - Found!]
    B9 --> B10[Total: 2 steps vs 6 with linear search]

    C --> C1[Each step halves remaining elements]
    C1 --> C2[n to n/2 to n/4 to n/8 to 1]
    C2 --> C3[Steps = log2 of n]
    C --> C4[Linear vs Binary comparison]
    C4 --> C4a[100 items: 100 steps vs 7 steps]
    C4 --> C4b[1000 items: 1000 steps vs 10 steps]
    C4 --> C4c[1000000 items: 1M steps vs 20 steps]

    D --> D1[Set left = 0, right = length - 1]
    D1 --> D2[Calculate mid = left + right - left / 2]
    D2 --> D3{Compare mid element to target}
    D3 --> |Equal| D4[Return found]
    D3 --> |Target is larger| D5[Set left = mid + 1]
    D3 --> |Target is smaller| D6[Set right = mid - 1]
    D5 --> D7{Is left greater than right?}
    D6 --> D7
    D7 --> |No| D2
    D7 --> |Yes| D8[Return not found]
```

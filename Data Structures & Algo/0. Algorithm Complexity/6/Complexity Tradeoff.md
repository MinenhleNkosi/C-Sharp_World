# Complexity Tradeoff Analyzer Capstone

This capstone exercise brings together the key complexity concepts you've learned: **O(n²)** nested loops, **O(n)** HashSet lookups, and **O(log n)** binary search.

## The Three Algorithms

1. **Naive Duplicate Check - O(n²)**

```cs
// Compare every pair of elements
for (int i = 0; i < arr.Length; i++)
    for (int j = i + 1; j < arr.Length; j++)
        if (arr[i] == arr[j]) return true;
```

2. **HashSet Duplicate Check - O(n)**

```cs
// Track seen values with O(1) lookups
HashSet<int> seen = new HashSet<int>();
foreach (int num in arr)
    if (!seen.Add(num)) return true;
```

3. **Binary Search - O(log n)**

```cs
// Each comparison halves the search space
while (left <= right)
{
    steps++;
    int mid = left + (right - left) / 2;
    if (arr[mid] == target) return steps;
    // Narrow to left or right half
}
```

## Complexity Comparison

| Algorithm     | Time Complexity | 1000 elements        |
| ------------- | --------------- | -------------------- |
| Nested loops  | O(n²)           | ~500,000 comparisons |
| HashSet       | O(n)            | ~1,000 operations    |
| Binary search | O(log n)        | ~10 comparisons      |

## Visualization

```mermaid
flowchart TD
    A([Complexity Tradeoff Analyzer Capstone]) --> B[Naive Duplicate Check - O-n2]
    A --> C[HashSet Duplicate Check - O-n]
    A --> D[Binary Search - O-log n]
    A --> E[Complexity Comparison]

    B --> B1[Outer loop iterates over every element]
    B1 --> B2[Inner loop starts at i+1 to compare remaining]
    B2 --> B3{Are any two elements equal?}
    B3 --> |Yes| B4[Duplicate found - return true]
    B3 --> |No| B5[Continue comparing]
    B5 --> B2
    B4 --> B6[1000 elements: ~500,000 comparisons]

    C --> C1[Create empty HashSet]
    C1 --> C2[Iterate through each element]
    C2 --> C3{Does HashSet already contain element?}
    C3 --> |Yes - Add returns false| C4[Duplicate found - return true]
    C3 --> |No - Add returns true| C5[Store element and continue]
    C5 --> C2
    C4 --> C6[1000 elements: ~1,000 operations]

    D --> D1[Set left = 0, right = length - 1]
    D1 --> D2[Calculate mid = left + right - left / 2]
    D2 --> D3[Increment step counter]
    D3 --> D4{Is arr-mid equal to target?}
    D4 --> |Yes| D5[Return steps taken]
    D4 --> |Target is larger| D6[Search right half - left = mid + 1]
    D4 --> |Target is smaller| D7[Search left half - right = mid - 1]
    D6 --> D2
    D7 --> D2
    D5 --> D8[1000 elements: ~10 comparisons]

    B6 --> E
    C6 --> E
    D8 --> E

    E --> E1[O-n2 Nested loops - slowest]
    E --> E2[O-n HashSet - efficient]
    E --> E3[O-log n Binary search - fastest]
    E1 --> E4[500x more operations than HashSet at n=1000]
    E2 --> E5[100x more operations than Binary Search at n=1000]
```

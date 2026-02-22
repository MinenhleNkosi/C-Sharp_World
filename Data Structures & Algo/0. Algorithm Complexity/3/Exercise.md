# Your Task

Classify algorithms by their Big O notation. Given an algorithm name, return its time complexity.

**O(1) - Constant**:
`"array_access"`, `"hash_lookup"`, `"stack_push"`, `"stack_pop"`

**O(log n) - Logarithmic**:
`"binary_search"`, `"balanced_tree_search"`

**O(n) - Linear**:
`"linear_search"`, `"find_max"`, `"array_sum"`

**O(n log n) - Linearithmic**:
`"merge_sort"`, `"heap_sort"`, `"quicksort_average"`

**O(n²) - Quadratic**:
`"bubble_sort"`, `"selection_sort"`, `"insertion_sort"`

Return `"Unknown"` for any other algorithm. Input matching should be case-insensitive.

## Method Signature

```cs
public static string ClassifyComplexity(string algorithm)
{
    // Analyze the algorithm name and return its Big O complexity
    // Return "Unknown" for unrecognized algorithms
}
```

## Expected Results

```cs
ClassifyComplexity("array_access") -> "O(1)"
ClassifyComplexity("binary_search") -> "O(log n)"
ClassifyComplexity("merge_sort") -> "O(n log n)"
ClassifyComplexity("BUBBLE_SORT") -> "O(n^2)"
ClassifyComplexity("dijkstra") -> "Unknown"
```

## Hints

💡 1. Use ToLower() on the input to handle case-insensitive matching before your switch

💡 2. The or pattern in C# switch expressions lets you match multiple values: "a" or "b" => result

💡 3. Think about what makes each algorithm fall into its category: O(1) has no loops over input, O(n) has one loop, O(n²) has nested loops

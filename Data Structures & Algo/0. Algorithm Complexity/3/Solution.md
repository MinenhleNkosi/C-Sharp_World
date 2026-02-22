```cs
using System;

public class Solution
{
    public static string ClassifyComplexity(string algorithm)
    {
        // Analyze the algorithm name and return its Big O complexity
        // Return "Unknown" for unrecognized algorithms
        string loweredAlgorithm = algorithm.ToLower();

        var complexity = loweredAlgorithm switch
        {
          "array_access" => "O(1)",
          "hash_lookup" => "O(1)",
          "stack_push" => "O(1)",
          "stack_pop" => "O(1)",
          "binary_search" => "O(log n)",
          "balanced_tree_search" => "O(log n)",
          "linear_search" => "O(n)",
          "find_max" => "O(n)",
          "array_sum" => "O(n)",
          "merge_sort" => "O(n log n)",
          "heap_sort" => "O(n log n)",
          "quicksort_average" => "O(n log n)",
          "bubble_sort" => "O(n^2)",
          "selection_sort" => "O(n^2)",
          "insertion_sort" => "O(n^2)",
          _ => "Unknown"
        };
        return complexity;
    }
}
```

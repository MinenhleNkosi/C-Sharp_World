# Comparing O(n) vs O(n²) Growth

The best way to understand algorithm complexity is to see it in action. By counting actual operations, you can observe how dramatically O(n²) algorithms slow down compared to O(n) as input grows.

## O(n) - Linear Growth

```cs
int count = 0;
for (int i = 0; i < n; i++)
{
    count++;  // Executes exactly n times
}
// count == n
```

A single loop iterating `n` times performs exactly `n` operations.

## O(n²) - Quadratic Growth

```cs
int count = 0;
for (int i = 0; i < n; i++)
{
    for (int j = 0; j < n; j++)
    {
        count++;  // Executes n × n times
    }
}
// count == n * n
```

Nested loops where both iterate `n` times perform `n × n = n²` operations.

## Growth Comparison

| n    | O(n) ops | O(n²) ops | Ratio |
| ---- | -------- | --------- | ----- |
| 5    | 5        | 25        | 5×    |
| 10   | 10       | 100       | 10×   |
| 100  | 100      | 10,000    | 100×  |
| 1000 | 1,000    | 1,000,000 | 1000× |

Notice how the ratio equals `n` itself - O(n²) becomes `n` times slower than O(n)!.

## Visualization

```mermaid
flowchart TD
    A([Comparing O-n vs O-n2 Growth]) --> B[O-n Linear Growth]
    A --> C[O-n2 Quadratic Growth]
    A --> D[Growth Comparison]

    B --> B1[Single loop iterating n times]
    B1 --> B2[Executes exactly n operations]
    B2 --> B3[count equals n]
    B3 --> B4[Double input = Double operations]

    C --> C1[Outer loop runs n times]
    C1 --> C2[Inner loop runs n times per outer]
    C2 --> C3[Executes n x n operations]
    C3 --> C4[count equals n x n]
    C4 --> C5[Double input = Quadruple operations]

    D --> D1[n=5: 5 ops vs 25 ops - Ratio 5x]
    D --> D2[n=10: 10 ops vs 100 ops - Ratio 10x]
    D --> D3[n=100: 100 ops vs 10000 ops - Ratio 100x]
    D --> D4[n=1000: 1000 ops vs 1000000 ops - Ratio 1000x]

    D1 --> D5[Ratio equals n itself]
    D2 --> D5
    D3 --> D5
    D4 --> D5

    D5 --> D6[O-n2 becomes n times slower than O-n]

    B3 --> D6
    C4 --> D6
```

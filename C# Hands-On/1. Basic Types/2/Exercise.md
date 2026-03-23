# Your Task

Add two prices together and return the total. Use the `decimal.Add()` method to combine the two decimal values.

## Method Signature

```cs
public static decimal AddPrices(decimal price1, decimal price2)
```

## Expected Results

```cs
AddPrices(10.00m, 5.99m) -> 15.99
AddPrices(19.99m, 0.01m) -> 20.00
AddPrices(0.00m, 7.50m) -> 7.50
```

## Hints

💡1. Use `decimal.Add(a, b)` to add two decimal values together.

💡2. The method returns a decimal value, so you can return the result of `decimal.Add()` directly.

💡3. Remember that decimal literals need the `m` suffix (e.g., `10.00m`).

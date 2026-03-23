# Decimals

The `decimal` type is a 128-bit precise decimal number, perfect for financial calculations where accuracy matters. Unlike `double`, decimals avoid floating-point rounding errors.

## When to Use Decimal vs Double

```cs
// Double: scientific calculations, graphics, where tiny errors are OK
double distance = 3.14159265358979;

// Decimal: money, financial data, where precision is critical
decimal price = 19.99m; // Note the 'm' suffix!
decimal taxAmount = 1.60m;
```

## The 'm' Suffix

Decimals require the `m` or `M` suffix to distinguish them from doubles:

```cs
decimal cost = 29.99m; // Correct
decimal rate = 0.075M; // Also correct
// decimal wrong = 29.99; // Error! Compiler sees this as double
```

## Decimal Methods for Arithmetic

The `decimal` type provides static methods for performing arithmetic without using operators:

| Method                   | Description           | Example                                  |
| ------------------------ | --------------------- | ---------------------------------------- |
| `decimal.Add(a, b)`      | Add two decimals      | `decimal.Add(10.50m, 3.25m)` = 13.75     |
| `decimal.Subtract(a, b)` | Subtract b from a     | `decimal.Subtract(10.50m, 3.25m)` = 7.25 |
| `decimal.Multiply(a, b)` | Multiply two decimals | `decimal.Multiply(10.00m, 2m)` = 20.00   |
| `decimal.Divide(a, b)`   | Divide a by b         | `decimal.Divide(10.00m, 4m)` = 2.50      |

## Using Decimal Methods

```cs
decimal itemPrice = 15.99m;
decimal shippingCost = 4.50m;

// Add two prices together
decimal total = decimal.Add(itemPrice, shippingCost); // 20.49

// Combine multiple items
decimal item1 = 9.99m;
decimal item2 = 14.50m;
decimal item3 = 3.25m;
decimal subtotal = decimal.Add(decimal.Add(item1, item2), item3); // 27.74
```

# Visualization

```mermaid
flowchart TD
    A([The decimal Type]) --> B[What is decimal?]
    A --> C[When to Use decimal vs double]
    A --> D[The m Suffix]
    A --> E[Decimal Methods for Arithmetic]
    A --> F[Using Decimal Methods]

    B --> B1[128-bit precise decimal number]
    B1 --> B2[Perfect for financial calculations]
    B2 --> B3[Avoids floating-point rounding errors unlike double]

    C --> C1[Use double for...]
    C --> C2[Use decimal for...]
    C1 --> C1a[Scientific calculations]
    C1 --> C1b[Graphics]
    C1 --> C1c[Where tiny errors are acceptable]
    C2 --> C2a[Money and financial data]
    C2 --> C2b[Where precision is critical]
    C2 --> C2c[Example: decimal price = 19.99m]

    D --> D1[Decimals require m or M suffix]
    D1 --> D2{Suffix provided?}
    D2 --> |Yes - 29.99m or 0.075M| D3[Valid - compiler treats as decimal]
    D2 --> |No - 29.99| D4[ERROR - compiler treats as double]

    E --> E1[decimal.Add - a, b]
    E --> E2[decimal.Subtract - a, b]
    E --> E3[decimal.Multiply - a, b]
    E --> E4[decimal.Divide - a, b]
    E1 --> E1a[Add two decimals - 10.50m + 3.25m = 13.75]
    E2 --> E2a[Subtract b from a - 10.50m - 3.25m = 7.25]
    E3 --> E3a[Multiply two decimals - 10.00m * 2m = 20.00]
    E4 --> E4a[Divide a by b - 10.00m / 4m = 2.50]

    F --> F1[Add two prices - decimal.Add-itemPrice, shippingCost-]
    F --> F2[Combine multiple items by nesting calls]
    F1 --> F1a[15.99m + 4.50m = 20.49]
    F2 --> F2a[decimal.Add-decimal.Add-item1, item2-, item3-]
    F2a --> F2b[9.99m + 14.50m + 3.25m = 27.74]
```

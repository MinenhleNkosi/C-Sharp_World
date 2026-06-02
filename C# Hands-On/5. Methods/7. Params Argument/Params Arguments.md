# The params Keyword

The `params` keyword allows a method to accept a variable number of arguments of the same type. Instead of creating an array manually, callers can pass any number of arguments directly.

## Basic Syntax

```cs
// Without params - caller must create an array
public static void PrintNumbers(int[] numbers) { }
PrintNumbers(new int[] { 1, 2, 3 }); // awkward

// With params - caller passes values directly
public static void PrintNumbers(params int[] numbers) { }
PrintNumbers(1, 2, 3);        // clean!
PrintNumbers(1, 2, 3, 4, 5);  // any number of args
PrintNumbers();               // zero args also works
```

## How It Works

```cs
public static double Average(params double[] values)
{
    if (values.Length == 0) return 0;

    double sum = 0;
    foreach (double value in values)
    {
        sum += value;
    }
    return sum / values.Length;
}

// All these calls are valid:
Average(5.0);                    // 1 argument
Average(10.0, 20.0);             // 2 arguments
Average(1.5, 2.5, 3.5, 4.5);     // 4 arguments
```

## Rules for params

| Rule     | Description                                        |
| -------- | -------------------------------------------------- |
| Position | Must be the last parameter in the method signature |
| Count    | Only one `params` parameter allowed per method     |
| Type     | Must be a single-dimensional array                 |
| Optional | Callers can pass zero or more arguments            |

## Combining with Other Parameters

```cs
public static string FormatMessage(string prefix, params string[] words)
{
    return prefix + ": " + string.Join(", ", words);
}

FormatMessage("Items", "apple", "banana", "cherry");
// Returns: "Items: apple, banana, cherry"
```

# Visualization

```mermaid
flowchart TD
    A([The params Keyword in C#]) --> B[What is params?]
    A --> C[Basic Syntax]
    A --> D[How It Works]
    A --> E[Rules for params]
    A --> F[Combining with Other Parameters]

    B --> B1[Allows a method to accept a variable number of arguments of the same type]
    B1 --> B2[Caller passes values directly instead of constructing an array manually]
    B2 --> B3[Inside the method the arguments are treated as a regular array]
    B3 --> B4[Zero arguments is valid - the array simply has a Length of 0]

    C --> C1[Without params - caller must pass new int array with values explicitly]
    C --> C2[With params - caller passes comma-separated values directly]
    C1 --> C3[PrintNumbers new int array 1 2 3 - verbose and awkward at the call site]
    C2 --> C4[PrintNumbers 1 2 3 - clean and readable]
    C2 --> C5[PrintNumbers 1 2 3 4 5 - any number of arguments accepted]
    C2 --> C6[PrintNumbers with no arguments - zero args also valid]
    C3 --> C7[params removes the ceremony of array construction from the caller]
    C4 --> C7
    C5 --> C7
    C6 --> C7

    D --> D1[public static double Average params double array values]
    D1 --> D2[Check values.Length == 0 and return 0 to handle the empty case]
    D2 --> D3[foreach loop accumulates sum across all values]
    D3 --> D4[Return sum divided by values.Length]
    D4 --> D5[Average of 5.0 - one argument - returns 5.0]
    D4 --> D6[Average of 10.0 and 20.0 - two arguments - returns 15.0]
    D4 --> D7[Average of 1.5 and 2.5 and 3.5 and 4.5 - four arguments - returns 3.0]
    D5 --> D8[Same method body handles any argument count without any changes]
    D6 --> D8
    D7 --> D8

    E --> E1[Position - params parameter must be last in the signature]
    E --> E2[Count - only one params parameter allowed per method]
    E --> E3[Type - must be a single-dimensional array]
    E --> E4[Optional - caller may pass zero or more arguments]
    E1 --> E1a[Placing params first would prevent the compiler mapping earlier positional args]
    E2 --> E2a[Two params parameters would make argument grouping ambiguous]
    E3 --> E3a[Multi-dimensional arrays are not supported with params]
    E4 --> E4a[Zero arguments means the array exists but is empty - not null]
    E1a --> E5[All four rules exist to ensure the compiler can always resolve calls unambiguously]
    E2a --> E5
    E3a --> E5
    E4a --> E5

    F --> F1[public static string FormatMessage string prefix params string array words]
    F1 --> F2[prefix is a required positional parameter - words captures all remaining args]
    F2 --> F3[FormatMessage called with Items then apple banana cherry]
    F3 --> F4[prefix receives Items - words array holds apple banana cherry]
    F4 --> F5[string.Join combines the words array with comma separators]
    F5 --> F6[Returns: Items colon apple comma banana comma cherry]
    F6 --> F7[Rule: params must still be last even when combined with other parameters]
```

The flowchart branches into five sections. **What is params?** establishes the core promise — any number of same-type arguments, treated as an array inside the method, with zero being a valid count. **Basic Syntax** contrasts the without-params and with-params calling styles, converging on the principle that params removes all array construction ceremony from the caller. **How It Works** walks through the Average method step by step across three different argument counts, converging on the point that the same method body handles every case without modification. **Rules for params** maps the four constraints — position, count, type, and optionality — converging on the explanation that all four rules exist so the compiler can always resolve calls without ambiguity. **Combining with Other Parameters** traces FormatMessage from definition through to output, converging on the reminder that params must remain last in the signature even when paired with required positional parameters.

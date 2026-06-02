# Using Return Values

When a method returns a value, you can store it in a variable or use it directly in expressions. This lets you build complex logic from simple, reusable methods.

## Storing Return Values

```cs
// Store the return value in a variable
int result = SomeMethod(5);
Console.WriteLine(result);

// Use the variable in further calculations
int doubled = result * 2;
```

## Using Return Values Directly

```cs
// Use the return value directly in an expression
int total = SomeMethod(5) * 10;

// Pass the return value to another method
int final = AnotherMethod(SomeMethod(5));
```

## Chaining Method Calls

```cs
// Methods can use other methods' return values
public static int Square(int n)
{
    return n * n;
}

public static int SumOfSquares(int a, int b)
{
    return Square(a) + Square(b);
}
```

# Visualization

```mermaid
flowchart TD
    A([Using Return Values in C#]) --> B[Storing Return Values]
    A --> C[Using Return Values Directly]
    A --> D[Chaining Method Calls]

    B --> B1[Assign the method call to a variable matching the return type]
    B1 --> B2[int result = SomeMethod of 5 - result holds the returned value]
    B2 --> B3[Print or inspect the value using the variable name]
    B3 --> B4[Use the variable in further calculations - int doubled = result times 2]
    B4 --> B5[Storing first is useful when the value is needed more than once]

    C --> C1[Return value used directly in an expression without storing]
    C --> C2[Return value passed immediately as an argument to another method]
    C1 --> C3[int total = SomeMethod of 5 times 10 - return value multiplied inline]
    C3 --> C4[Method call is evaluated first then the result slots into the expression]
    C2 --> C5[int final = AnotherMethod of SomeMethod of 5]
    C5 --> C6[Inner call resolves first - its return value becomes the outer argument]
    C4 --> C7[Use directly when the value is only needed once and storing would add no clarity]
    C6 --> C7

    D --> D1[public static int Square int n - returns n times n]
    D --> D2[public static int SumOfSquares int a int b - returns Square of a plus Square of b]
    D1 --> D3[Square encapsulates one operation and returns a single result]
    D2 --> D4[SumOfSquares calls Square twice and combines both return values]
    D3 --> D5[Each call to Square is replaced by its return value before the addition runs]
    D4 --> D5
    D5 --> D6[Chaining keeps each method small and lets complex logic build from simple parts]
    D6 --> D7[Rule: any expression that expects a type can be replaced by a method call that returns that type]
```

The flowchart branches into three sections. **Storing Return Values** traces the pattern of capturing a return value in a variable, showing how it can be printed and reused in further calculations, converging on the guideline that storing is the right choice when the value is needed more than once. **Using Return Values Directly** maps two inline patterns — using the return value in an expression and passing it straight into another method — converging on the principle that the method call is always evaluated first and its result slots in as if it were a literal value. **Chaining Method Calls** walks through the Square and SumOfSquares pair to show how one method can consume another's return value, converging on the rule that any expression expecting a given type can be replaced by a method call that returns that same type.

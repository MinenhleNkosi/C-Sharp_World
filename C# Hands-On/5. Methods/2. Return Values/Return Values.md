# Return Values

Methods can send data back to the code that called them using the `return` statement. The return type in the method signature tells C# what type of value will be returned.

## Return Types vs void

```cs
// void method - performs an action, returns nothing
public static void SayHello()
{
    Console.WriteLine("Hello!");
}

// Method with return type - sends a value back
public static int GetAge()
{
    return 25;
}

public static string GetGreeting()
{
    return "Welcome!";
}
```

## The return Statement

The `return` statement does two things:

1. Specifies the value to send back
2. Immediately exits the method

```cs
public static int Double(int x)
{
    return x * 2;  // Returns the result and exits
}

public static bool IsPositive(int number)
{
    return number > 0;  // Returns true or false
}
```

## Using Return Values

```cs
// Store the returned value in a variable
int result = Double(5);  // result = 10

// Use directly in expressions
int total = Double(3) + Double(4);  // total = 14

// Use in conditions
if (IsPositive(-5))
{
    Console.WriteLine("Positive!");
}
```

# Visualization

```mermaid
flowchart TD
    A([Return Values in C#]) --> B[Return Types vs void]
    A --> C[The return Statement]
    A --> D[Using Return Values]

    B --> B1[void methods perform an action and send nothing back]
    B --> B2[Non-void methods send a value back to the caller]
    B1 --> B3[public static void SayHello - prints but returns nothing]
    B2 --> B4[public static int GetAge - returns the integer 25]
    B2 --> B5[public static string GetGreeting - returns the string Welcome]
    B3 --> B6[Return type in the signature tells C# what type of value to expect]
    B4 --> B6
    B5 --> B6
    B6 --> B7[Rule: return type must exactly match the value the method sends back]

    C --> C1[return does two things in one statement]
    C1 --> C2[Specifies the value to send back to the caller]
    C1 --> C3[Immediately exits the method - no further lines run]
    C2 --> C4[public static int Double int x - returns x times 2]
    C3 --> C4
    C4 --> C5[public static bool IsPositive int number - returns number greater than 0]
    C5 --> C6[Expression after return is evaluated first then the result is sent back]
    C6 --> C7[Any code placed after a return statement in the same block is unreachable]

    D --> D1[Store the returned value in a variable]
    D --> D2[Use the returned value directly in an expression]
    D --> D3[Use the returned value in a condition]
    D1 --> D1a[int result = Double of 5 - result holds 10]
    D1a --> D1b[Variable type must match the method return type]
    D2 --> D2a[int total = Double of 3 plus Double of 4 - total holds 14]
    D2a --> D2b[Each method call is replaced by its return value before the expression resolves]
    D3 --> D3a[if IsPositive of negative 5 - condition receives false - block does not run]
    D3a --> D3b[Bool-returning methods slot directly into if conditions without comparison operators]
    D1b --> D4[Return values can be stored, combined, or evaluated - treat them like any value of that type]
    D2b --> D4
    D3b --> D4
```

The flowchart branches into three sections. **Return Types vs void** contrasts void methods against non-void methods across three concrete examples, converging on the rule that the declared return type must exactly match what the method sends back. **The return Statement** establishes the two simultaneous effects — sending a value and exiting immediately — and converges on the consequence that any code placed after a return in the same block is unreachable. **Using Return Values** maps the three ways a caller can consume a returned value — storing it, combining it in an expression, and using it in a condition — converging on the principle that a return value behaves exactly like any other value of that type wherever it appears.

# Method Parameters

Methods can accept multiple parameters, allowing you to pass data into them for processing. Parameters are defined in the parentheses after the method name, separated by commas.

## Defining Multiple Parameters

```cs
// A method with two parameters
public static void Greet(string firstName, string lastName)
{
    Console.WriteLine("Hello, " + firstName + " " + lastName);
}

// A method with three parameters
public static void PrintRectangleArea(int width, int height, string unit)
{
    Console.WriteLine(width * height + " " + unit);
}
```

## Calling Methods with Parameters

When calling a method, you must provide arguments in the same order as the parameters are defined:

```cs
// The arguments match the parameter order
Greet("John", "Doe");        // firstName = "John", lastName = "Doe"
PrintRectangleArea(5, 10, "cm²");  // width = 5, height = 10, unit = "cm²"
```

## Calling from Main

The `Main` method is the entry point of your program. You can call other methods from within `Main`:

```cs
public static void Main()
{
    SayHello();      // Call a method with no parameters
    Add(10, 20);     // Call a method with two parameters
}
```

# Visualization

```mermaid
flowchart TD
    A([Method Parameters in C#]) --> B[What are Method Parameters?]
    A --> C[Defining Multiple Parameters]
    A --> D[Calling Methods with Parameters]
    A --> E[Calling from Main]

    B --> B1[Parameters allow you to pass data into a method for processing]
    B1 --> B2[Defined in parentheses after the method name]
    B2 --> B3[Multiple parameters are separated by commas]
    B3 --> B4[Each parameter needs a type and a name - type comes first]

    C --> C1[Two parameters - public static void Greet string firstName string lastName]
    C --> C2[Three parameters - public static void PrintRectangleArea int width int height string unit]
    C1 --> C3[firstName and lastName are both strings - passed in separately]
    C2 --> C4[width and height are ints - unit is a string - mixed types are allowed]
    C3 --> C5[Parameter list defines what the caller must supply when invoking the method]
    C4 --> C5

    D --> D1[Arguments must be provided in the same order as the parameters are defined]
    D1 --> D2[Greet called with John and Doe]
    D1 --> D3[PrintRectangleArea called with 5 and 10 and cm squared]
    D2 --> D4[firstName receives John - lastName receives Doe]
    D3 --> D5[width receives 5 - height receives 10 - unit receives cm squared]
    D4 --> D6[Order mismatch silently assigns wrong values - no error is thrown]
    D5 --> D6
    D6 --> D7[Rule: argument order at the call site must mirror parameter order in the definition]

    E --> E1[Main is the entry point - every program starts here]
    E1 --> E2[Other methods are called from within Main by name]
    E2 --> E3[SayHello called with no arguments - empty parentheses]
    E2 --> E4[Add called with two arguments - 10 and 20]
    E3 --> E5[No arguments means the method signature has no parameters]
    E4 --> E6[Arguments map positionally to the parameters declared in Add]
    E5 --> E7[Main orchestrates the program flow by calling methods in sequence]
    E6 --> E7
```

The flowchart branches into four sections. **What are Method Parameters?** establishes that parameters are typed placeholders defined in the signature that tell the caller exactly what data to supply. **Defining Multiple Parameters** maps the two and three parameter forms, converging on the rule that every parameter needs a type and a name and that mixed types across parameters are perfectly valid. **Calling Methods with Parameters** traces how each argument at the call site maps positionally to its corresponding parameter, converging on the warning that order mismatches assign wrong values silently with no compiler error. **Calling from Main** establishes Main as the program entry point, contrasts a no-argument call against a two-argument call, and converges on the principle that Main orchestrates program flow by invoking methods in sequence.

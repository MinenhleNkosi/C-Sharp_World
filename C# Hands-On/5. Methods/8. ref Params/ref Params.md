# The ref Keyword

The `ref` keyword allows you to pass arguments **by reference**, meaning the method can modify the original variable, not just a copy of its value.

## Pass by Value vs Pass by Reference

```cs
// Without ref - value is copied, original unchanged
void Double(int x) { x = x * 2; }  // Original NOT modified

// With ref - reference to original variable
void Double(ref int x) { x = x * 2; }  // Original IS modified
```

## Using ref Parameters

```cs
// Declaration: use ref in the parameter
public static void Increment(ref int value)
{
    value++;  // Modifies the original variable
}

// Call: must also use ref keyword
int number = 5;
Increment(ref number);  // number is now 6
```

## The Classic Swap Pattern

```cs
public static void Swap(ref int a, ref int b)
{
    int temp = a;  // Store first value
    a = b;         // Overwrite first with second
    b = temp;      // Set second to stored value
}

int x = 10, y = 20;
Swap(ref x, ref y);  // x=20, y=10
```

## Helper Files Available

- `ResultFormatter.Format(a, b)` - Returns a formatted string like `"a=5, b=10"`
- `SwapHelper.DemoSwap(ref x, ref y)` - A reference implementation of swap

# Visualization

```mermaid
flowchart TD
    A([The ref Keyword in C#]) --> B[What is ref?]
    A --> C[Pass by Value vs Pass by Reference]
    A --> D[Using ref Parameters]
    A --> E[The Classic Swap Pattern]

    B --> B1[Passes a reference to the original variable instead of a copy of its value]
    B1 --> B2[The method can read and modify the caller's original variable directly]
    B2 --> B3[Both the method signature and the call site must use the ref keyword]
    B3 --> B4[Use when a method needs to change a variable that lives outside of it]

    C --> C1[Pass by value - method receives a copy - original is never touched]
    C --> C2[Pass by reference - method receives the original - changes persist after return]
    C1 --> C1a[void Double int x - x = x times 2 - only the local copy changes]
    C1a --> C1b[Caller's variable holds the same value it had before the call]
    C2 --> C2a[void Double ref int x - x = x times 2 - the original variable changes]
    C2a --> C2b[Caller's variable reflects the new value after the call returns]
    C1b --> C3[Rule: without ref every argument is an independent copy inside the method]
    C2b --> C3

    D --> D1[Declaration - add ref before the parameter type in the method signature]
    D --> D2[Call site - add ref before the argument variable when calling the method]
    D1 --> D1a[public static void Increment ref int value - value++ modifies the original]
    D2 --> D2a[int number = 5 - Increment ref number - number is now 6 after the call]
    D1a --> D3[ref in the signature tells the compiler this parameter is a reference not a copy]
    D2a --> D3
    D3 --> D4[Omitting ref at either the declaration or the call site causes a compile error]
    D4 --> D5[Rule: ref must appear in both places - signature and call - or it does not compile]

    E --> E1[public static void Swap ref int a ref int b]
    E1 --> E2[Step 1 - int temp = a - store first value in a temporary variable]
    E2 --> E3[Step 2 - a = b - overwrite first variable with second variable's value]
    E3 --> E4[Step 3 - b = temp - assign stored value to second variable]
    E4 --> E5[int x = 10 int y = 20 - Swap ref x ref y]
    E5 --> E6[x holds 20 - y holds 10 after the call]
    E6 --> E7[temp is essential - without it the original value of a is lost at step 2]
    E7 --> E8[Swap is the canonical example of ref because it is impossible without modifying both originals]
```

The flowchart branches into four sections. **What is ref?** establishes the core mechanic — a reference to the original variable rather than a copy — and surfaces the rule that both declaration and call site must carry the keyword. **Pass by Value vs Pass by Reference** runs the same Double method in both modes side by side, converging on the principle that without ref every argument inside a method is an independent copy that cannot affect the caller. **Using ref Parameters** traces the Increment example through declaration and call, converging on the compile-time rule that ref must appear in both places or the code will not build. **The Classic Swap Pattern** walks through all three steps of the swap algorithm in order, converging on the explanation that temp is non-negotiable and that swap is the definitive ref example because the operation is structurally impossible without direct access to both original variables.

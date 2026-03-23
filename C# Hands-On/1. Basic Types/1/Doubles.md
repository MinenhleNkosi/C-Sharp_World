# The double Type

A `double` is a 64-bit floating-point number used for storing decimal values. Use it when you need to represent fractional numbers like temperatures, measurements, or scientific constants.

## Declaring double Variables

```cs
// Declare and assign a double variable
double temperature = 36.5;
double pi = 3.14159;
double negativeValue = -273.15;
```

## double vs int

Integers (`int`) can only hold whole numbers without decimal parts. When you need precision with fractional values, use `double`.

```cs
int wholeNumber = 36;        // No decimal allowed
double preciseValue = 36.5;  // Decimal values preserved
```

## Using Decimal Points

When assigning values to doubles, include a decimal point to make your intent clear:

```cs
double exactValue = 100.0;   // Clear: this is a double
double fraction = 0.5;       // Decimal values work perfectly
double negative = -40.0;     // Negative decimals too
```

# Visualization

```mermaid
flowchart TD
    A([The double Type]) --> B[What is double?]
    A --> C[Declaring double Variables]
    A --> D[double vs int]
    A --> E[Using Decimal Points]

    B --> B1[64-bit floating-point number]
    B1 --> B2[Stores decimal values]
    B2 --> B3[Use for fractional numbers]
    B3 --> B3a[Temperatures]
    B3 --> B3b[Measurements]
    B3 --> B3c[Scientific constants]

    C --> C1[Example: double temperature = 36.5]
    C --> C2[Example: double pi = 3.14159]
    C --> C3[Example: double negativeValue = -273.15]

    D --> D1[int]
    D --> D2[double]
    D1 --> D1a[Only holds whole numbers]
    D1 --> D1b[No decimal part allowed]
    D1 --> D1c[Example: int wholeNumber = 36]
    D2 --> D2a[Holds fractional values]
    D2 --> D2b[Decimal precision preserved]
    D2 --> D2c[Example: double preciseValue = 36.5]

    E --> E1[Include a decimal point to make intent clear]
    E1 --> E2[Example: double exactValue = 100.0]
    E1 --> E3[Example: double fraction = 0.5]
    E1 --> E4[Example: double negative = -40.0]
    E2 --> E5[Decimal point signals this is a double not an int]
    E3 --> E5
    E4 --> E5
```

# Your Task

Create methods that return important temperature and scientific constants as `double` values. Each method should declare a `double` variable, assign the specified value, and return it.

## Method Signatures

```cs
public static double GetBoilingPointFahrenheit()   // Return 212.0
public static double GetFreezingPointFahrenheit()  // Return 32.0
public static double GetAbsoluteZeroCelsius()      // Return -273.15
public static double GetPi()                       // Return 3.14159
public static double GetBodyTemperatureCelsius()   // Return 37.0
```

## Expected Results

```cs
GetBoilingPointFahrenheit() -> 212.0
GetFreezingPointFahrenheit() -> 32.0
GetAbsoluteZeroCelsius() -> -273.15
GetPi() -> 3.14159
GetBodyTemperatureCelsius() -> 37.0
```

## Hints

💡 1. Declare a `double` variable using: `double variableName = value;`

💡 2. Include decimal points in your values, like `212.0` instead of just `212`

💡 3. For negative values like absolute zero, simply put a minus sign before the number: `-273.15`

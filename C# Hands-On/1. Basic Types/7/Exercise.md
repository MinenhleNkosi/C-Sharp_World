# Your Task

Create a method that prints a formatted user profile using string interpolation. The profile should display the user's name, age, height, and account balance on separate lines.

## Method Signature

```cs
public static void PrintUserProfile(string name, int age, double height, decimal balance)
```

## Expected Output Format

```
Name: [name]
Age: [age] years old
Height: [height]m
Balance: $[balance]
```

## Expected Results

```cs
PrintUserProfile("Alice", 25, 1.65, 1000.50m)
-> Name: Alice
   Age: 25 years old
   Height: 1.65m
   Balance: $1000.50
```

## Hints

💡 1. Start your string with `$` to enable interpolation: `$"text {variable} more text"`

💡 2. Use `Console.WriteLine()` four times, once for each line of the profile

💡 3. Put variables directly inside curly braces like `{name}` - no need for string concatenation

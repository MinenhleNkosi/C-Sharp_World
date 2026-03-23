# Your Task

Write a method that takes a first name, last name, and age, then prints three lines:

- The full name (first name + space + last name)
- A greeting: `Hello, [fullName]!`
- An age message: `[fullName] is [age] years old.`

## Method Signature

```cs
public static void PrintConcatenation(string firstName, string lastName, int age)
```

## Expected Output

For `PrintConcatenation("John", "Doe", 30)`:

```cs
John Doe
Hello, John Doe!
John Doe is 30 years old.
```

## Hints

💡 1. Use the `+` operator to join strings together: `firstName + " " + lastName`

💡 2. You can concatenate integers directly with strings: `"Age: " + age` will work because C# converts the int to a string

💡 3. Build the full name first, then reuse it in the other two lines to avoid repetition

# Your Task

Create a method that prints:

- A Windows file path: `C:\Users\Admin\Documents\report.txt`
- A multi-line SQL query (on separate lines):
  - `SELECT *`
  - `FROM Users`
  - `WHERE Active = 1`

Use verbatim strings (`@"..."`) for both outputs.

## Method Signature

```cs
public static void PrintFilePaths()
```

## Expected Output

```cs
C:\Users\Admin\Documents\report.txt
SELECT *
FROM Users
WHERE Active = 1
```

## Hints

💡 1. Start the string with `@` before the opening quote: `@"..."`

💡 2. In verbatim strings, backslashes `\` are treated literally - no need to escape them

💡 3. For multi-line verbatim strings, just press Enter in the string - the newlines are preserved

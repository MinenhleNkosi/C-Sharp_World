# Arrays in C#

An array is a fixed-size collection that holds multiple values of the same type. Use arrays when you know exactly how many elements you need upfront.

## Declaring Arrays with `new`

```cs
// Create an array with a specific size (all elements initialized to default values)
int[] numbers = new int[5];        // 5 integers, all initialized to 0
string[] names = new string[3];    // 3 strings, all initialized to null
bool[] flags = new bool[10];       // 10 booleans, all initialized to false
```

## The Length Property

Every array has a `Length` property that tells you how many elements it can hold:

```cs
int[] scores = new int[7];
Console.WriteLine(scores.Length);  // Prints: 7

string[] cities = new string[100];
int size = cities.Length;          // size is 100
```

## Default Values

When you create an array with `new`, all elements are set to their default values:

| Type               | Default Value |
| ------------------ | ------------- |
| int, double, float | 0             |
| bool               | false         |
| string, objects    | null          |

# Visualization

```mermaid
flowchart TD
    A([Arrays in C#]) --> B[What is an Array?]
    A --> C[Declaring Arrays with new]
    A --> D[The Length Property]
    A --> E[Default Values]

    B --> B1[Fixed-size collection that holds multiple values of the same type]
    B1 --> B2[Size is set at creation and cannot change afterwards]
    B2 --> B3[Use when the number of elements is known upfront]
    B3 --> B4[All elements must share the same declared type]

    C --> C1[int array numbers = new int of size 5 - five integers all set to 0]
    C --> C2[string array names = new string of size 3 - three strings all set to null]
    C --> C3[bool array flags = new bool of size 10 - ten booleans all set to false]
    C1 --> C4[new keyword allocates the array and fills every slot with the type default]
    C2 --> C4
    C3 --> C4
    C4 --> C5[The number inside the brackets sets the fixed capacity at declaration time]

    D --> D1[Every array exposes a Length property]
    D1 --> D2[Length returns the total number of slots the array was created with]
    D2 --> D3[int array scores = new int of size 7 - scores.Length returns 7]
    D2 --> D4[string array cities = new string of size 100 - cities.Length returns 100]
    D3 --> D5[Length is commonly used in for loop conditions - i less than array.Length]
    D4 --> D5
    D5 --> D6[Length reflects capacity not the number of non-default values stored]

    E --> E1[Numeric types - int double float - default to 0]
    E --> E2[bool defaults to false]
    E --> E3[string and all object types default to null]
    E1 --> E4[Default is the natural zero-like value for each type]
    E2 --> E4
    E3 --> E4
    E4 --> E5[Defaults are assigned automatically by new - no manual initialisation needed]
    E5 --> E6[Rule: always assign meaningful values before reading array elements to avoid working with defaults unintentionally]
```

The flowchart branches into four sections. **What is an Array?** establishes the two defining constraints — fixed size and single type — and anchors the guidance that arrays suit scenarios where the element count is known upfront. **Declaring Arrays with new** maps the three common type examples, converging on the principle that the `new` keyword both allocates the array and fills every slot with the type's default value. **The Length Property** traces two concrete examples and converges on the important distinction that `Length` reflects the declared capacity, not the count of meaningful values stored. **Default Values** maps the three default categories by type, converges on the rule that defaults are assigned automatically, and closes with the practical warning to assign real values before reading slots to avoid silently operating on defaults.

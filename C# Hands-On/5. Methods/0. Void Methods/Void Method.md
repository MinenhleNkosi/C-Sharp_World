# Void Methods

A **void method** is a method that performs an action but does not return a value. Use `void` as the return type when your method should execute code without sending data back to the caller.

## Defining a Void Method

```cs
// Basic void method syntax
public static void SayHello()
{
    Console.WriteLine("Hello!");
}

// Void method with parameters
public static void PrintNumber(int number)
{
    Console.WriteLine(number);
}
```

## Access Modifiers

Methods can have different access levels:

| Modifier  | Description                           |
| --------- | ------------------------------------- |
| `public`  | Accessible from anywhere              |
| `private` | Only accessible within the same class |
| `static`  | Belongs to the class, not an instance |

```cs
// Private method - can only be called from within Solution class
private static void SecretMethod()
{
    Console.WriteLine("This is private!");
}

// Public method - can be called from outside
public static void PublicMethod()
{
    SecretMethod(); // Calling private method from within the class
}
```

## Calling Static vs Instance Methods

How you call a method depends on whether it's **static** or an **instance method**:

```cs
public class Example
{
    // Static method - belongs to the class itself
    public static void StaticMethod()
    {
        Console.WriteLine("I'm static!");
    }

    // Instance method - belongs to an object
    public void InstanceMethod()
    {
        Console.WriteLine("I'm an instance method!");
    }
}

// Calling static methods - use the class name or call directly within the same class
Example.StaticMethod();  // From outside the class
StaticMethod();          // From within the same class

// Calling instance methods - requires creating an object first
Example obj = new Example();
obj.InstanceMethod();  // Must call on an instance
```

**Key difference**: Static methods can be called directly using the class name (or just the method name within the same class). Instance methods require you to create an object first using `new`.

Here, we're using `static` methods, so you can call them directly by name within the same class.

# Visualization

```mermaid
flowchart TD
    A([Void Methods in C#]) --> B[What is a Void Method?]
    A --> C[Defining a Void Method]
    A --> D[Access Modifiers]
    A --> E[Static vs Instance Methods]

    B --> B1[Performs an action but does not return a value]
    B1 --> B2[Use void as the return type in the method signature]
    B2 --> B3[Executes code without sending any data back to the caller]
    B3 --> B4[Use when the goal is to do something not to produce a result]

    C --> C1[Basic void method - public static void SayHello]
    C --> C2[Void method with parameters - public static void PrintNumber int number]
    C1 --> C3[No return statement needed - method just runs its body]
    C2 --> C4[Parameters let you pass data in even though nothing comes back out]
    C3 --> C5[Signature pattern: access modifier - static - void - method name - parameters]
    C4 --> C5

    D --> D1[public - accessible from anywhere]
    D --> D2[private - only accessible within the same class]
    D --> D3[static - belongs to the class not to an instance]
    D1 --> D4[PublicMethod can be called from outside the class]
    D2 --> D5[SecretMethod can only be called from within the same class]
    D3 --> D6[No object needs to be created to call a static method]
    D4 --> D7[A public method can call a private method from within the same class]
    D5 --> D7
    D6 --> D7
    D7 --> D8[Access modifiers control visibility - static controls how the method is called]

    E --> E1[Static method - belongs to the class itself]
    E --> E2[Instance method - belongs to an object created from the class]
    E1 --> E1a[Declared with the static keyword]
    E1a --> E1b[Call from outside using ClassName.MethodName]
    E1b --> E1c[Call from within the same class using just the method name]
    E2 --> E2a[Declared without the static keyword]
    E2a --> E2b[Must create an object first using new ClassName]
    E2b --> E2c[Call using objectName.MethodName]
    E1c --> E3[Key rule: static needs a class name or nothing - instance needs an object]
    E2c --> E3
    E3 --> E4[In these examples all methods are static so they are called directly by name]
```

The flowchart branches into four sections. **What is a Void Method?** establishes the core concept — void signals that a method does something rather than producing a result, so no return value is ever sent back to the caller. **Defining a Void Method** maps the basic and parameterised forms, converging on the full signature pattern and the rule that no return statement is required. **Access Modifiers** traces the three modifiers independently, converging on the distinction that access modifiers control visibility while static controls how the method is invoked. **Static vs Instance Methods** contrasts the two calling patterns step by step, converging on the key rule that static methods need only a class name or nothing at all while instance methods always require an object to be created first.

# 🧠 Prompt: Order and Format C# Class Members

## 📝 Description
This prompt formats and reorders members of a C# class to follow a clean and consistent structure. It ensures proper indentation and organizes members in a logical order for readability and maintainability.

## 🎯 Goals
- Format code with 4-space indentation.
- Place opening braces on new lines.
- Reorder class members in the following order:
  1. `private readonly` fields (e.g. `_props`)
  2. Public properties
  3. Constructors
  4. Methods (ordered by visibility: `public`, `protected`, `private`)
- Normalize naming conventions (PascalCase for types and members, camelCase for fields).
- Remove unnecessary whitespace and align code blocks.

## 📥 Input
A C# class file with unordered or poorly formatted members.

## 📤 Output
A clean, well-formatted C# class with members ordered and styled according to standard conventions.

## 💬 Example
### Input:
```csharp
public class Example {
public void DoSomething() {}
private readonly string _name;
public string Name { get; set; }
public Example(string name) { _name = name; }
}
```
### Output:
```csharp
public class Example
{
    private readonly string _name;

    public string Name { get; set; }

    public Example(string name)
    {
        _name = name;
    }

    public void DoSomething()
    {
    }
}
```

## 🛠️ Notes
- Do not modify logic or add/remove comments unless necessary for formatting.
- Preserve attributes, region tags, and preprocessor directives.

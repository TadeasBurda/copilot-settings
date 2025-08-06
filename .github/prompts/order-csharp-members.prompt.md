# 🧠 Prompt: Order and Format C# Class Members

## 📝 Description
This prompt formats and reorders members of a C# class to follow a clean and consistent structure. It ensures proper indentation and organizes members in a logical order for readability and maintainability.

## 🎯 Goals
- Format code with 4-space indentation.
- Place opening braces on new lines.
- Reorder class members in the following order:
  1. private readonly fields (e.g. _props)
  2. private fields with default value (e.g. int = 0)
  3. private nullable fields (e.g. int?)
  4. protected fields
  5. internal properties
  6. public properties
  7. Constructors
  8. Methods (in order: public, protected, private)
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
private int _age = 20;
private readonly string _name;
public string Name { get; set; }
private bool? _isActive;
internal int Total { get; set; }
public Example(string name) { _name = name; }
}
protected readonly Services _services;
protected string _fullName = "ExampleName";
protected bool? _isInit;
protected void GetSomething()
{

}
private void SaveSomething()
{

}
```
### Output:
```csharp
public class Example
{
    private readonly string _name;

    private int _age = 20;

    private bool? _isActive;

    protected readonly Services _services;

    protected string _fullName = "ExampleName";

    protected bool? _isInit;

    internal int Total { get; set; }

    public string Name { get; set; }

    public Example(string name, Services services)
    {
        _name = name;
        _services = services;
    }

    public void DoSomething()
    {
    }

    protected void GetSomething()
    {

    }

    private void SaveSomething()
    {

    }
}
```

## 🛠️ Notes
- Do not modify logic or add/remove comments unless necessary for formatting.
- Preserve attributes, region tags, and preprocessor directives.

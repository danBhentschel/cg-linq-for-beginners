[//]: # (GENERATED FILE -- DO NOT EDIT)
# Exercise: Extension Methods

In the previous lesson, we learned how to write extension methods to enhance existing types.

In this exercise, you must add an extension method, `SayHello()` to the built-in `string` type. The `SayHello()` method should return the string: "Hello, &lt;subject&gt;!"

For reference, here is the example extension method from the previous page:

```csharp
namespace IntExtensions
{
    public static class CoolExtensionsForInt
    {
        public static string Growl(this int num)
        {
            return $"G{new string('r', num)}";
        }
    }
}
```

@[Extension Methods Exercise]({"stubs": ["ExtensionMethods1/ExtensionMethodsExercise1.cs"], "command": "ExtensionMethods1.UnitTest.Exercise1", "project": "exercises"})

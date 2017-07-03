[//]: # (GENERATED FILE -- DO NOT EDIT)
# Background: Extension method parameters

An extension method can take extra parameters, in addition to an instance of the type that it is extending. Here is an example of how this works:

```csharp
namespace IntExtensions
{
    public static class CoolExtensionsForInt
    {
        public static string Growl(this int num, char a, char b)
        {
            return $"{a}{new string(b, num)}";
        }
    }
}
```

What does this do? Let's call it a few times and find out:

```csharp
using IntExtensions;

  ...

    // Prints "Grrrrrrr" to the console
    Console.WriteLine(7.Growl('G', 'r'));

    // Prints "Brrr" to the console
    Console.WriteLine(3.Growl('B', 'r'));

    // Prints "Shhhh" to the console
    Console.WriteLine(4.Growl('S', 'h'));
```

# Exercise
Try adding another extension method to the `string` type. This time, call it `MakePlural()`. The `MakePlural()` method should take an `int` parameter and return a string that is either the original string if the parameter is 1, or the string with an 's' appended to it if the parameter is not equal to 1.

@[Extension Method Parameters Exercise]({"stubs": ["ExtensionMethods2/ExtensionMethodsExercise2.cs"], "command": "ExtensionMethods2.UnitTest.Exercise2", "project": "exercises"})

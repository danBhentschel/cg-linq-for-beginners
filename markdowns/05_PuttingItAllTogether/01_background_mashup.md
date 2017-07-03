[//]: # (GENERATED FILE -- DO NOT EDIT)
# Exercise

Congratulations! We have made it through all the background material. We now know enough to not only use LINQ, but to even reimplement some elements of it ourselves! Doesn't that sound exciting?

Let's try it out!

> **WARNING:** This exercise is quite challenging. Don't be discouraged if you are not able to solve it. You can continue with the rest of the course, and you will probably still be able to understand most of the material.

## LINQ Select() method

One of the more commonly used methods in LINQ is the `Select()` method. `Select()` is an extension method to the `IEnumerable<T>` interface. It is analogous to the `map()` method found in many other programming languages.

`Select()` takes each element, one-at-a-time, from a source `IEnumerable<T>`, applies a delegate function to the elements, and then returns an `IEnumerable<U>` result.

> **NOTE:** The type inside the collection can change, hence the change from `IEnumerable<T>` to `IEnumerable<U>`.

## Implement a Transform() method

In order to avoid the complications of dealing with generics in this exercise, let's limit the extension method to only work with `IEnumerable<int>`. Here is what you need to do:

 - Implement an extension to `IEnumerable<int>` called `Transform()`
 - The `Transform()` method should accept, as a parameter, a delegate that takes an `int` input and returns an `int` output
 - The `Transform()` method should be a generator that iterates through the input `IEnumerable<int>`, applies the delegate to each value, and `yield return`s the result
 - The `Transform()` should generate an `IEnumerable<int>`

## Here are some examples to help you out

### Example delegate declaration
```csharp
private delegate int FuncTwoInts(int one, int two);
```

### Example extension method
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

### Example generator
```csharp
public IEnumerable<int> GetDoubles(int n)
{
    for (int i = 0; i < n; i++)
    {
        yield return i * 2;
    }
}
```

@[Putting It Together Exercise]({"stubs": ["Background1/BackgroundReviewExercise1.cs"], "command": "Background1.UnitTest.Exercise1", "project": "exercises"})

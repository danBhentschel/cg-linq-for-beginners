# IEnumerable&lt;T&gt;

## Why learn about generators and IEnumerable&lt;T&gt;?
LINQ methods are extension methods to the `IEnumerable<T>` interface. It is important to understand how `IEnumerable<T>` works to fully understand the more subtle details of how LINQ works.

## Collections as IEnumerable&lt;T&gt;
A method returning an object that implements the `IEnumerable<T>` interface can be enumerated via a `foreach` block. For example:

```csharp
//// EMBED: LinqCourseEmbeddedCode/IEnumerable1.cs, Declare method returning IEnumerable
```

Since `List<T>` implements `IEnumerable<T>`, you can iterate the return value from `GetInts()` like so:

```csharp
//// EMBED: LinqCourseEmbeddedCode/IEnumerable1.cs, Call method returning IEnumerable
```

> **NOTE:** `IEnumerable<T>` is an implementation of the [Iterator Pattern](https://en.wikipedia.org/wiki/Iterator_pattern) in C#.

Not all that surprising or impressive, is it? Well, let's take a look at generators next. That's where the true value of `IEnumerable<T>` lies.

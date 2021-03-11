# Classes

Classes in Vivian are a reference type that the user can define for any purpose, classes can contain `procedures` and `fields`

Here's an example of how a class looks in Vivian:
```javascript
class Foo
{
    var Bar = "Foo";
    // fields may also be declared without an initialiser if a type is specified
    var Name: string; 

    var X: float32; 
    var Y: float32;
}

procedure Foo.Sum(x: float32, y: float32) => float32
{
    // 'this' keyword can be used to access the fields within the class
    if (this.X == 0 && this.Y == 0)
    {
        this.X = x;
        this.Y = y;
    }
    return this.X + this.Y;
}
```

If you'd like to instantiate your class elsewhere in your code to be used, this is how you can do so:
```javascript
procedure Main() => void
{
    var console = Console();
    // this will allocate foo with an empty ctor
    // be aware that if you instantiate a class with an empty ctor
    // none of your fields will be initialised!
    // this is highly discouraged.
    var foo = Foo();

    // correct method
    // the constructor is called in the order of field declarations
    var foo2 = Foo("Foo", "John", 4, 2);

    var sum = foo2.Sum(foo2.X, foo2.Y);
    console.WriteLine(sum); // outputs 6!
}
```

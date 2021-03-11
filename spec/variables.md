# Variables

Variables in Vivian follow really closely to TypeScript and C# syntax for declaration: 
```javascript
procedure Main() => void
{
    var console = Console();
    var hello = "hello";
    var world = "world";

    var helloworld = hello + " " + world;
    console.WriteLine(helloworld); // prints "hello world"
    // Variables may also be declared with explicit type visibility
    var xCoord: float32 = 0.7;
    var yCoord: float32 = 0.2;
    // a conversion method would be required for return a `float64` from summing two `float32`s
    var sumCoords: float64 = float64(xCoord + yCoord);
    // string conversions are not required for calls with WriteLine, but are encouraged 
    // to avoid boxing.
    console.WriteLine(string(sumCoords));
}
```
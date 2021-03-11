# Conversions

Since Vivian is a strongly typed language, conversions can be both implicit, and explicit. If you're unfamiliar with the Vivian type system, please see [types file](types). 

Basic conversions in Vivian follow as such: 
```javascript 
int8(x);
int16(x);
int32(x);
int64(x);
uint8(x);
uint16(x);
uint32(x);
uint64(x);
char(x);
string(x);
object(x);
bool(x);
float32(x);
float64(x);
```
A conversion call would look along the lines of this:
```javascript
procedure Main() => void
{
    // a basic conversion to a float
    // note: this WILL crash if the compiler fails
    // to convert the string properly
    var console = Console();
    var x = float32("12.2");
    console.WriteLine(x);

    // You also have access to string conversions
    // since types won't automatically be promoted to a string
    // an explicit conversion is required
    Printer(string(12)); // prints "12"
    Printer(string(true)); // prints "True" 
}

procedure Printer(text: string) => void
{
    // This is a method that ONLY takes a string,
    // the compiler will not promote any integeral/boolean/char value
    // to a string
    var console = Console();
    console.WriteLine(text);
}
```
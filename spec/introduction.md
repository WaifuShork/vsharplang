# Introduction
Vivian is a simple, modern, object-oriented and type-safe programming language. It was created as a high level abstraction while also offering lower level access, and running on the CLR.

Vivian has a unified type system, all primitive types such as `int32` and `float64`, inherit from a single root `object` type. Vivian also supports user-defined reference types.

## Hello world
The "Hello world" program is typically used to introduce a programming language, here's how it's done in Vivian:
```javascript
procedure Main() => void
{
    var console = Console();
    console.WriteLine("Hello, world");
}
```

Vivian source files typically have a file extension of `.viv`. Assuming that the "Hello world" program is stored in a file named `hello.viv`, the program can be compiled with the Vivian compiler using the command line

```console
vc hello.viv
```
which produces an executable assembled named `hello.exe`. The output produced by this application when run is
```console
Hello, world
```

The "Hello world" program starts with a `procedure`, procedures are just an instruction set to be run. This one is `Main`, which happens to be the entry point of all Vivian applications. Next we create a `Console` instance, which contains various methods for I/O operations. 

`Note: print(string) and input() can be used but is highly discouraged to uphold conventions`
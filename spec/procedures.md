# Procedures

Procedures are just a fancy name for `methods` or `functions`. They may seem to have funny syntax at first, but the way I designed this was very purposeful. 

If you're unfamiliar with how a Vivian procedure looks, it's as follows:
```javascript
procedure Sum(a: int32, b: int32) => int32
{
    return a + b;
}
```

It may look awkward at first but this is because the syntax is borrowed from C# and TypeScript. the `=>` is used to basically *point* your eyes in the direction of what the procedure will be returning. Basically saying "this procedure of Sum will equal an int32 value". Simple, right? 

You can pass any number of parameters into a procedure as you like. Paramters also have a second syntax, this also follows for procedure returns. Look close: 

```javascript
procedure Sum(a => int32, b => int32): int32
{
    return a + b;
}
```
Cool right?. Vivian was designed to be both flexible and strict, allowing the developer to have expressive freedom, while limiting them to a safely-typed environment.
# Types

Vivian has 2 main categories of types, `reference` and `value` types. All of Vivians types are explicity named with their allocation sizes, the decision for this was made for ease of use. Remembering is hard, and you should be able to look at the type to know exactly the size it will be. 

## Simple Types && Default Constructors 
- For `int8`, `int16`, `int32`, `int64`, `uint8`, `uint16`, `uint32`, and `uint64` all default to `0`.
- For `char`, the default value is `'\x0000'`.
- For `float32`, the default value is `0.0`.
- For `float64`, the default value is `0.0`.
- For `bool`, the default value is `false`.
- For `string`, the default value is `String.Empty`.

| __Reserved word__ | __Aliased type__ |
|-------------------|------------------|
| `int8`            | `System.SByte`   | 
| `int16`           | `System.Int16`   | 
| `int32`           | `System.Int32`   | 
| `int64`           | `System.Int64`   | 
| `uint8`           | `System.Byte`    | 
| `uint16`          | `System.UInt16`  | 
| `uint32`          | `System.UInt32`  | 
| `uint64`          | `System.UInt64`  | 
| `char`            | `System.Char`    | 
| `float32`         | `System.Single`  | 
| `float64`         | `System.Double`  | 
| `bool`            | `System.Boolean` | 
| `string`          | `System.String`  |
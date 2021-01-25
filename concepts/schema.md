---
description: This page is a reference the format used to write schema files.
---

# Schema

```text
package sandbox.example

component Example {
  uint current_health // a property
  uint max_health // another property
}
```

### Types

#### Primitive Types

| Syntax | Type | Notes |
| :--- | :--- | :--- |
| `bool` | Boolean | True or False. |
| `uint`, `ulong` | Unsigned Integer | Variable-length encoding; smaller values use fewer bits. |
| `int`, `long` | Signed Integer | Variable-length encoding; smaller values use fewer bits. Negative values are represented in the usual two's-complement manner, and so use the maximum number of bits. |
| `sint`, `slong` | Zig-Zag Signed Integer | Variable-length zig-zag encoding; smaller absolute values use fewer bits. More space-efficient than `int`or `long` when values are likely to be negative. |
| `float`, `double` | Floating Point Integer |  |
| `string` | String of Characters | Strings should always be either ASCII or UTF-8. |
| `bytes` | Array of Bytes |  |
| `TagCompound` | Compound NBT Tag |  |
| `Entity` | A Component Set | A data structure that represents an arbitrary collection of components. |

#### Enumerations

You can define enumerations and use them like built-in types. Like types, enums can be defined within the scope of an outer type.

```text
package sandbox.example

enum Colour {
    BLACK
    RED
    GREEN
    BROWN
    BLUE
    PURPLE
    CYAN
    LIGHT_GRAY
    GRAY
    PINK
    LIME
    YELLOW
    LIGHT_BLUE
    MAGENTA
    ORANGE
    WHITE
}

type Example {
  Colour colour
}
```

#### Collections

The collection types available are:

* Optional: `T?` represents either no value or a single `T` value
* Array/List: `T[]` represents either zero or more `T` values
* Map: `[K,V]` represents a map from keys of type `K` to values of type `V`

```text
package sandbox.example

type Example {
  uint? an_integer
  uint[] integer_list
  [uint,bool] integer_boolean_map
}
```

You can create nested collections \(like lists of lists, maps of lists, and so on\), however, you cannot create a list or map of optional values.

```text
package sandbox.example

type Works {
  uint[][] list_of_list
  [uint, uint[]] map_of_list
}

type Errors {
  uint?[] list_of_optional
  [uint, uint?] map_of_optional
}
```


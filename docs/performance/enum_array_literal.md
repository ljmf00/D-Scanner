# Enum Array Literal Check

Checks for array literals declared `enum` in `class` and `struct` declarations. These lead to large amounts of run-time memory allocation.

## Noncompliant Code Example

The runtime will allocate a copy of this array literal every time it is used.

```d
struct SomeStruct {
    enum VALUES = [1, 2, 3, 4, 5];
}
```

## Compliant Solution

Use static immutable instead.

```d
struct SomeStruct {
    static immutable VALUES = [1, 2, 3, 4, 5];
}
```

See also: [Arrays](https://dlang.org/spec/arrays.html).

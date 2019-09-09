# Auto function without return statement

Checks for auto functions without return statement. Auto function without return statement can be an omission and are not detected by the compiler. However sometimes they can be used as a trick to infer attributes.

## Noncompliant Code Example

```d
auto doStuff()
{
    writeln("foobar");
}
```

## Compliant Solution

```d
void doStuff()
{
    writeln("foobar");
}
```

See [Auto Functions](https://dlang.org/spec/function.html#auto-functions).

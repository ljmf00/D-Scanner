# Auto Ref Template Functions

An auto ref function template parameter becomes a ref parameter if its corresponding argument is an lvalue, otherwise it becomes a value parameter.

This rule checks for assignment to auto-ref function parameters.

## Noncompliant Code Example

Using `auto ref` with assignment.

```d
int doStuff(T)(auto ref int a)
{
    a = 10;
}
```

## Compliant Solution

Use `ref` instead.

```d
int doStuff(T)(ref int a)
{
    a = 10;
}
```

See [Function Templates with Auto Ref Parameters](https://dlang.org/spec/template.html#auto-ref-parameters).

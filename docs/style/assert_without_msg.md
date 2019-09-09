# Assert without a message

Check that all asserts have an explanatory message.

## Noncompliant Code Example

```d
assert(0);
```

## Compliant Solution

```d
assert(0, "foo bar");
```

See [Assert Expressions](https://dlang.org/spec/expression.html#AssertExpression).

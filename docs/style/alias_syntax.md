# Deprecated Alias Syntax

Checks for use of the deprecated `alias` declaration syntax.

## Noncompliant Code Example

```d
alias int abcde;
```

## Compliant Solution

```d
alias abcde = int;
```

See [Alias Declarations](https://dlang.org/spec/declaration.html#alias).

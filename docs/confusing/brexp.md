# Confusing BrExp

Catches use of the assembly br expression that can be confused with an array index expression.

## Noncompliant Code Example

```d
asm
{
    mov a, someArray[1];
    add near ptr [EAX], 3;
}
```

## Compliant Solution

```d
asm
{
    mov a, [someArray + 1];
    add near ptr [EAX], 3;
}
```

See [Issue 9738](https://issues.dlang.org/show_bug.cgi?id=9738).

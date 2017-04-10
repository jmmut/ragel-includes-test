# Ragel includes test

This is a small example of reusing machines or actions in ragel.

Compile the ragel sources into C code:
```
ragel main.ragel
```

Compile the C code into binary:
```
gcc main.c
```

The machines recognize the next grammar:

```
main = fooFSM barFSM;
fooFSM = "foo" | "bar";
barFSM = "bar" | "baz";
```

and they use common actions included from another file.


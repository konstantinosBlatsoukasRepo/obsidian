
```java

enum Values { ONE, TWO, THREE }

int val  = switch (num) {
  ONE -> 1;
  TWO -> 2;
  THREE -> 3;
};

```

the expression must be a primitive type (all boxed forms included) or enum
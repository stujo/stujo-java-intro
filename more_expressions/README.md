# More Expressions

* char vs String literals

* Short Circuit && || vs & | (p49)
  * Zero test && divide by zero

* Type Conversion
  * Casting and information loss (p55)

```
int i1 = Short.MAX_VALUE;
short s1 = (short) i1;
System.out.printf("%d == %d -> %b%n", i1, s1, i1 == s1);
```

* Handy Operator Precedence Table (p56)
  * [http://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html)

* Expression Type Conversion / Promotion (p58)

```
short x = 5;
short y = 2;
short shortSum = (short) (y * x);
int intSum = (y * x);
```


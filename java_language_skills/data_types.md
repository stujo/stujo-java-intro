# Data Types

* Understand and use [Java Data Types](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

* Default Values (only for fields) and sizes
 * ``byte``	-> ``0`` -> 8-bit
 * ``short`` -> ``0`` -> 16-bit
 * ``int`` -> ``0`` -> 32-bit
 * ``long`` -> ``0L``  -> 64-bit
 * ``float`` -> ``0.0f`` -> 32-bit
 * ``double`` -> ``0.0d`` -> 64-bit
 * ``char`` -> ``'\u0000'`` - 16-bit Unicode
 * ``String`` (or any object) -> ``null``
 * ``boolean`` -> ``false`` - unknown size

* Literals:
  * null
  * true false
  * '\uffff' is Unicode in hex
  * 0xff is hex
  * 'c' != "c"

* Formatting using PrintStream.format
  * [Formatter Syntax](http://docs.oracle.com/javase/6/docs/api/java/util/Formatter.html#syntax)


* __Note:__ Java 7 has binary literals too
  * byte fourTimesThree = 0b1100;

* __Note:__ To see the binary:
```
int x = 100;
System.out.println(Integer.toBinaryString(x));
```

* __Note:__ When we use printf we are actually converting the raw datatypes to objects using autoboxing, but you probably didn't notice and you don't know about this yet :)



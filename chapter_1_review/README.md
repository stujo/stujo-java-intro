# Chapter 1 Review

* __Important Update:__
 * [Formatter Syntax for Boolean Values, Dates and Argument Indexes](http://docs.oracle.com/javase/6/docs/api/java/util/Formatter.html#syntax)

```
// Booleans
System.out.format("%b, %B%n", true, true);
System.out.format("%b, %B%n", false, false);

// Exponents
System.out.format("%e%n", Math.PI);

// Times and Dates
// American Style Date
Date today = new Date();

System.out.format("Today is %tD%n", today);
System.out.format("The year is %tY%n", today);
System.out.format("Today is %tA%n", today);
```

* Self Test in text book (p30)



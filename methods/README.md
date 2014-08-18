# Methods

At the moment we are only _writing_ ``static`` or Class Methods, we'll start writing instance methods later


```
class String {
...
    public static String format(String format,
            Object... args)
    {
        ...
    }
...
}


String.format("%2.4f", Math.PI);

```

* [String Formatting Examples](http://examples.javacodegeeks.com/core-java/lang/string/java-string-format-example/)

But we are _calling_ instance methods on the objects that we are working with.

```
class String {
...
    public String toUpperCase()
    {
        ...
    }
...
}


"convertMe".toUpperCase();

```

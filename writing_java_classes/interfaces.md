# Interfaces

* Understand Interfaces and how to use them
 * [http://docs.oracle.com/javase/tutorial/java/IandI/index.html](http://docs.oracle.com/javase/tutorial/java/IandI/index.html)

* Interfaces are entirely abstract but can contain constants

###Exercise
* __EXERCISE:__ ``NamedSurface`` as ``interface`` have ``Shape`` implement ``NamedSurface``

```
interface NamedSurface
{
   String getName();
   double getArea();
}
```

* See the errors you get and adjust your classes to fix them

* __BONUS EXERCISE:__ Write a class method on your App which takes and array of NamedSurfaces and returns the longest name

```
static String getLongestName(NamedSurface[] namedObjects)
{
   ...
}

```




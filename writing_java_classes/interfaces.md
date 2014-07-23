# Interfaces

* Understand Interfaces and how to use them
 * [http://docs.oracle.com/javase/tutorial/java/IandI/index.html](http://docs.oracle.com/javase/tutorial/java/IandI/index.html)

* Interfaces are entirely abstract but can contain constants

###Exercise
* __EXERCISE:__ ``LineArt`` as ``interface`` have ``Shape`` implement ``LineArt``

```
interface LineArt
{
   double getPerimeter();
}
```

* See the errors you get and adjust your classes to fix them

* __BONUS EXERCISE:__ Write a class method on your App which takes and array of ``LineArt``s and returns the total sum of all perimeters as an indication of how much ink a plotter would use to draw them.

```
static double getInkUsage(LineArt[] drawables)
{
   double totalLineLength = 0.0;

   // ... sum up the values

   return totalLineLength;
}

```




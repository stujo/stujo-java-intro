# for - loop

* [for loop](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)

```
for(int i=0; i < limit; i++)
{
}

for(;;)
{
  // Runs forever :) and this is a comment
}
```

###Exercise
* __EXERCISE:__ Write an application called ``RandomArrayer``. The application should generate a random number between ``10`` and ``20`` (inclusive). Then allocate a new array of ``int``s. The use a for loop to assign each ``int`` in the array to a random number. Use [java.util.Arrays.sort()](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html#sort%28int[]%29) to sort the array of ``int``s in ascending order and then another for loop to print out the numbers to the console

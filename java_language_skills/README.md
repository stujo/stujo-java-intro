# Java Language Skills

##Class Methods (Java Language)
* Understand and use [Class Methods (static) esp. main]
 * No instance needed - We'll get to Instance Methods later
 * ``String[] args``
 * ``System.out.println()``
 * ``public static void`` - Access Modifiers

##Packages (Java Language)
* Understand [Java Packages](http://docs.oracle.com/javase/tutorial/java/package/packages.html) ~ Namespace and Folder Name
* __EXERCISE:__ Move your HelloWorld class to a package using eclipse

##Data Types (Java Language)
* Understand and use [Java Data Types](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

##Local Variables (Java Language)
* Understand and use [Local Variables](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html)
* Variable initialization rules

##Printing Out Values (Java Platform)
* [System.out.printf](http://www.java2s.com/Code/JavaAPI/java.lang/System.out.printf.htm)
* [Formatter](http://docs.oracle.com/javase/6/docs/api/java/util/Formatter.html#syntax)
* [Cheat Sheet](http://alvinalexander.com/programming/printf-format-cheat-sheet)

###Exercise
* __EXERCISE:__ Create a new folder called ``datatypes`` and a main application class called ``DataTypeApp``. Put the ``DataTypeApp`` in an appropriate ``package``. In DataTypeApp.main method, add a local variable of each of the built in data types and print out the values on separate lines, hint: ``%n`` translates to a new line

* __CHECKPOINT:__ Primitive Data Types

##Expressions, Statements and Blocks (Java Language)
* Understand and use [Expressions, Statements and Block](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html)
* Expression - evaluates to a value
* Statement - (expression, declaration or control flow)
* Blocks - a group of zero or more statements, hint at scope

##Operators (Java Language)
Eclipse will show warnings and errors as you type, pay attention to them to learn how to use these operators

* The Arithmetic Operators
* __EXERCISE:__ Create a new folder called ``operators`` with a class called ``OperatorsApp`` in an appropriate package. For each of the Arithmetic operators ``+``,``-``,``/``,``%``,``++``,``--`` write an example usage and print out the results. Ensure that your app describes the difference between prefix and postfix ``--/++``.

* The Equality and Relational Operators
* __EXERCISE:__ Create a new app any way you wish. In the main method, write an example expression for each of these operators which prints something out:
 * ==      equal to
 * !=      not equal to
 * &gt;       greater than
 * &gt;=      greater than or equal to
 * <       less than
 * <=      less than or equal to
What data type do these expressions return?

## Comments (Java Language)
* Understand and use Comments rest-of-line, in-line (and javadoc later)

##Random Number Generator Code Sample
This code is used in the next examples, we'll learn what all the pieces do later, for now just use this code in your exercises

```
Random random = new java.util.Random();
int randomIntBetween0and99 = random.nextInt(100);
/*
nextInt(int n)
Returns a pseudorandom, uniformly distributed int value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence.
*/
```

##if (Control Flow)
Simplest Control flow if-then

* [if](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html)
* ``else``
* ``else if``
* Recommendation: Always use blocks

###Exercise
* __EXERCISE:__ Write an application which prints HEADS 50% of the time and TAILS 50% of the time to the console and exits

##switch (Control Flow)
* [switch](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html)
* ``break``
* ``default``

###Exercise
* __EXERCISE:__ Write an application called ``LuckyDay`` which randomly selects a number between 0 and 6 (inclusive) and uses a ``switch`` statement to print out a day of the week in the format "This week, 'Wednesday' is your lucky day!". Where the day of the week printed is determined by the random number (Sunday is 0..Saturday is 6)

* __CHECKPOINT:__ Branching Structures

##Basic Arrays (Java Language)
* Understand [Java Array Usage](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)
* Allocate an array with the literal syntax
* Assign and access individual elements in the array
```
int[] anArray = {
    100, 200, 300,
    400, 500, 600,
    700, 800, 900, 1000
};
```
* ``array.length``
* ``System.arraycopy()``

###Exercise
* __EXERCISE:__ Re-write the ``LuckyDay`` application to use an array

##Arrays and Array
Array Utilities
* [Arrays](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html)


##Command Line Arguments (Java Language)
Enough hard coding! Let's read in some arguments

* ``public static void main(String[] args)``
* How can we access args?

###Exercise
* __EXERCISE:__ Write a simple application in ``sorter`` which takes multiple command line arguments, puts them into an array, sorts the array and prints out the sorted array

* __CHECKPOINT:__ Arrays

###Converting Values
* __DEMO:__ Parsing Strings into primitive Types
* __EXERCISE:__ Write a simple application in ``cladder`` which takes two command line arguments, checks that they are present, converts them into double values, multiplies them together and prints out the answer to two decimal places.

##while (Control Flow)
* [while / do-while](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html)

###Exercise
* __EXERCISE:__ Write an application called ``HighRoller`` which utilizes one of these loop types to count the number of dice rolls required to reach ``25``. Each dice roll is a random number between ``1`` and ``6`` inclusive. At the end, print out, the total score and how many rolls it took. If the player rolls exactly ``25`` then print out the special message ``YOU ARE A HIGH ROLLER!!!``

##for (Control Flow)
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

##for each (Control Flow)
* [for each](http://docs.oracle.com/javase/6/docs/technotes/guides/language/foreach.html)

###Exercise
* __EXERCISE:__ Rewrite one of the loops in ``RandomArrayer`` to use the for each loop syntax

##break in loops (Control Flow)
* Shortcut exit loop

##continue in loops (Control Flow)
* Shortcut next iteration

* __CHECKPOINT:__ Loop Structures


##Strings (Java Platform)
* [String](http://docs.oracle.com/javase/tutorial/java/data/strings.html) is a special case object in that you can use a literal notation ``"my string contents"`` and get an object reference
* [StringBuilder](http://docs.oracle.com/javase/tutorial/java/data/buffers.html)

##Returning Values (Methods)
* ``return``
* void
* types
* Recommendation: Single Return Statement is preferred

* __CHECKPOINT:__ Returning Values

##Method Names (Methods)
* camelCase beginning with lowercase

##Passing Parameters (Methods)
* Understand argument passing and method invokation
 * Everything is passed by value, the value passed is either a primitive data type or an __object reference__
 * Objects themselves are always stored in the heap, and we only ever have a reference to that space

* __CHECKPOINT:__ Passing Arguments

##Class Methods (Methods)
* You don't need to create an instance to call ``Class`` (static) methods
* The instance of the ``Class`` is created when the bytecode is loaded by the ``ClassLoader``
* ``Math.min(a,b);``
* Our app is started when ``main`` is called
* Explore [``Math``](http://docs.oracle.com/javase/6/docs/api/java/lang/Math.html)
* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template. In your ``App`` class use a loop and the Math library to print out a table with the radius, the area and the circumference of 10 circles with each radius between  ``1`` and ``10`` units. Instead of printing the values out directly, write a ``class`` method called ``getCircleInfo()`` on your application class which takes an ``array`` of radii (type ``double[n]``) and returns a 2 dimensional array ``double[n][3]``, where in each row of the array the 0th element contains the radius, 1st the area, 2nd the circumference.
* __EXERCISE:__ Replace the AppTest generated by the template with this AppTest Class to your Application. Try it out, by running the tests as a JUnit 4 Unit Test Case in eclipse. (The archetype template uses JUnit 3 syntax, so we are upgrading!)

```
package com.skillbox.boxes.circles;
// You'll need to change this package declaration, eclipse will help!

import static org.junit.Assert.*;
import org.junit.Test;

public class AppTest {
	@Test
	public void testCirclrInfoResultLength() {
		double[] radii = { 1, 2, 3, 4 };
		assertEquals(radii.length, CircleApp.getCircleInfo(radii).length);
	}
}
```


##Instance Methods (Methods)
* If you have an Object Reference to an ``instanceof`` a ``Class`` you can call it's instance methods
* ``String myString = "Contents of String";``
* ``myString.contains(" of ");``
* Explore [``String``](http://docs.oracle.com/javase/6/docs/api/java/lang/String.html)
* How can you change a value of a ``String``?
* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template. In your ``App`` class write a class method called ``reverseUpperCase`` which takes a ``String`` parameter and uses some instance methods of the String class to return its contents in reversed UPPERCASE as a new ``String``. Call your ``reverseUpperCase`` method 5 times from your main method with some different arguments including "" and print out the results
* __EXERCISE:__ Add a Test!


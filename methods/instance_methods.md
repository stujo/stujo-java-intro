# Instance Variables and Methods

* If you have an Object Reference to an ``instanceof`` a ``Class`` you can call it's instance methods

* Fields
* Instance Methods such as _getters_ and _setters_:



```
class Shape
{
  String mType; //circle, square, etc.
  double mArea;
  String mColor;

  // add getters and setters

  // toString
}
```

* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template with the artifact id of 'shapes'. In your application write a ``Shape`` class, with the fields above.
* Add 'getters and setters'
* Create an array of 3 ``Shape``s
* Create three instances, a circle, a square and an equilateral triangle
* Set the instance variables to the correct values using the setters
* Assign the new ``Shape``s to the elements in the array
* Implement the toString method to display information about the __this__ ``Shape`` object

* Use a for loop to print out the contents of the array


* __EXERCISE:__ Add a Test for the toString method of ``Shape``


* __BONUS:__ Where can we put the math for the area calculations?
```
class Shapes
{
    static public double getAreaOfEquilateralTriangle(double sideLength) {
        // Area of equilateral triangle
    	return Math.sqrt(3) / 4 * sideLength * sideLength;
    }
}
```

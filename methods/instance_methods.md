# Instance Methods

* If you have an Object Reference to an ``instanceof`` a ``Class`` you can call it's instance methods

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

* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template with the artifact id of 'shapes'. In your application write a ``Shape`` class, with the fields above. Add 'getters and setters' and create three instances, a circle, a square and an equilateral triangle.
* Call the area, type and toString methods and print out the results

* __EXERCISE:__ Add a Test!

# Object Oriented Coding

##OO Principals in Java
* Understand the following Object Oriented Concepts:
 * Classes
 * Objects
 * Inheritance
 * Abstraction and Encapsulation
 * Constructors, ``new`` and ``super``
 * Static versus Instance
 * Polymorphism
##OO Overview
* [Overview](http://docs.oracle.com/javase/tutorial/java/concepts/index.html)
[What Is an Object?](http://docs.oracle.com/javase/tutorial/java/concepts/object.html)
[What Is a Class?](http://docs.oracle.com/javase/tutorial/java/concepts/class.html)
[What Is Inheritance?](http://docs.oracle.com/javase/tutorial/java/concepts/inheritance.html)
[What Is an Interface?](http://docs.oracle.com/javase/tutorial/java/concepts/interface.html)
[What Is a Package?](http://docs.oracle.com/javase/tutorial/java/concepts/package.html)
[What Is Composition?](http://javarevisited.blogspot.com/2013/06/why-favor-composition-over-inheritance-java-oops-design.html)

##Classes and Objects
If ``Object`` instances are Cookies then ``Class``es are the cookie cutters

* [Overview](http://docs.oracle.com/javase/tutorial/java/javaOO/)
* Class definitions define:
 * How instances must be created and initialized (Constructors, or other creation pattern)
 * What instances can do - behaviour - (their interfaces, instance methods)
 * How they do it - implementation
 * What data they store internally - instance data
 * Who can access what
 * Any Class specific data, constants or behaviours (``static``)

##Inheritance and Classes
###Exercise
* __EXERCISE:__ Group discussion, select and brainstorm on domain
* __LIVE CODE:__ examples of``extends``, ``class``
* __EXERCISE:__ Now on your own in groups of two. Pick a domain and make some notes:
 * Describe Domain (package name)
 * Find Classes (``class``)
 * Find Inheritance (``extends``)
 * Draft up classes on paper
* __DISCUSSION:__ Review of examples


##Writing Your Own Java Classes
##Class Definitions (Java Language)
* One public class per .java file
* Must Match path with package
* Must Match Class name with Filename
* Constructors
 * ``new``
 * ``super``
 * ``this``
* Fields
* Getters and Setters
* Review Class Methods and Class Variables
 * ``static``
* Instance Methods and Instance Variables
 * non-``static``

* __EXERCISE:__  Implement the basics of your classes from the previous exercise.

* __CHECKPOINT:__ Constructors


##Object Equality (Java Language)
* [``equals``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#equals%28java.lang.Object%29) and [``hashCode``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#hashCode%28%29)
* __EXERCISE:__ Write a Java class called ``Employee`` with fields for ``firstName``, ``lastName`` and  . Override ``toString`` in a meaningful way. Now try and implement equals and hashCode according to the documentation provided

* __EXERCISE:__ Write some ``@Test``s for your ``equals`` code

* __DEMO:__ Eclipse Generators

##Dates and Calendars (Java Platform)
* For this exercise [``GregorianCalendar.html#GregorianCalendar(int, int, int)``](http://docs.oracle.com/javase/6/docs/api/java/util/GregorianCalendar.html#GregorianCalendar%28int, int, int%29) might be handy
* __EXERCISE:__ Add ``dateOfBirth`` as ``java.util.Date`` to your Employee Class
* __DISCUSSION:__ GregorianCalendar - Allows you to create dates and Calendar - Date Math
* __EXERCISE:__ Run your tests again from the previous exercise

* __CHECKPOINT:__ Classes and Objects

##Access Modifiers (Java Language)
* [Access Modifiers](http://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)
* ``public``
* ``private``
* 'package' - The default
* ``protected``

* __EXERCISE:__  Discuss with your partner the appropriate access modifiers for parts of your class system

##More Inheritance in Java (Java Language)
* Understand Class inheritance and how to implement it
 * Overriding
 * Abstract classes and methods
 * Final (classes, methods, variables, parameters)
* Recommendation: use ``final`` where you don't intend a value to change and avoid coding errors

##Interfaces in Java
* Understand Interfaces and how to use them
 * [http://docs.oracle.com/javase/tutorial/java/IandI/index.html](http://docs.oracle.com/javase/tutorial/java/IandI/index.html)
* Understand Abstract Classes and how to define them
* Interfaces are entirely abstract but can contain constants

##Abstraction, Encapsulation and Interfaces
When you turn the steering wheel, the front wheels turn, you don't care how it works
* Use [StringBuilder](http://docs.oracle.com/javase/6/docs/api/java/lang/StringBuilder.html) as an example
* Abstraction (Interface / Observable Behaviour / Exposed)
* Encapsulation (Implementation / Hidden)
* 'The way you use it' is well defined
 * ``interface`` or ``class`` definition
* Clearly defined interfaces allow _Polymorphism..._

* __CHECKPOINT:__ Abstraction
* __CHECKPOINT:__ Encapsulation


##Polymorphism
When you rent a car, it doesn't matter what model it is, you can still drive it
* [Polymorphism](http://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html)
* Share some common nature but differ in implementation or additional behaviours
 * Interfaces with multiple implementations
 * ``@Override``s of instance methods
 * Implementations of ``abstract`` methods
* [WikiPedia](http://en.wikipedia.org/wiki/Polymorphism_(computer_science))

##The Java Collections Framework and Generics
* [Collections Overview](http://docs.oracle.com/javase/tutorial/collections/)
* Interfaces
 * [Overview](http://docs.oracle.com/javase/tutorial/collections/interfaces/collection.html)
 * [List](http://docs.oracle.com/javase/6/docs/api/java/util/List.html)
 * [Map](http://docs.oracle.com/javase/6/docs/api/java/util/Map.html)
 * [Set](http://docs.oracle.com/javase/6/docs/api/java/util/Set.html)
* Concrete Implementations (Many we'll only cover the basics)
 * [ArrayList](http://docs.oracle.com/javase/6/docs/api/java/util/ArrayList.html)
 * [HashMap](http://docs.oracle.com/javase/6/docs/api/java/util/HashMap.html)
 * [HashSet](http://docs.oracle.com/javase/6/docs/api/java/util/HashSet.html)
 * __NOTE:__ If you want to use your own classes as keys or in unique collections ``hashCode`` and ``equals`` will need to be implemented (later)
* [Generics](http://docs.oracle.com/javase/tutorial/java/generics/) - you may have noticed something new: ``<E>``
* [generics_collections.html](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/generics_collections.html)

* Additional Note: [unmodifiableCollection](http://docs.oracle.com/javase/6/docs/api/java/util/Collections.html#unmodifiableCollection%28java.util.Collection%29)
 * ``UnsupportedOperationException``

* __CHECKPOINT:__ Polymorphism

###Exercise
* __EXERCISE:__ Group discussion on collections
* __EXERCISE:__ Write a java method which generates an ArrayList<Integer> of the Fibonacci series numbers starting with 0 and 1, up to and including the first value which exceeds ``limit`` where ``limit`` is a parameter. Recommendation use __TDD__ and if the problem is unclear, ask your instructor to clarify

* __CHECKPOINT:__ Collections

##Object Basics (Java Objects)
* Every class extends ``Object``
* ``toString`` -> type plus hashCode
* ``getClass()`` -> ``Class``
* ``instanceof``casting - A lot less of it now we have Generic Collections
* ``clone`` - ``Cloneable`` Marker interface
* [``hashCode`` and ``equals`` contract](http://www.ibm.com/developerworks/library/j-jtp05273/)

* __LIVE DEMO:__ Using ``String`` as an example

##Class Class Basics (Java Objects)
* ``Class`` extends ``Object``
* ``getName()`` -> Useful for resources, jdbc drivers and loggers to avoid hard coding
* ``getClassLoader()``
* ``Class.forName()`` -> ``Class``

* __LIVE DEMO:__ Using ``String.getClass`` as an example

##More Class Implementation (Java Objects)
* Constructors Calling Constructors
* __CHECKPOINT:__ Constructors
* Inheritance Review
* Method Overloading
* __CHECKPOINT:__ Inheritance
* Static vs Instance Review
* __CHECKPOINT:__ Static versus Instance

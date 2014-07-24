# Exceptions

##Understand Java Exceptions
[Discussion](http://www.oracle.com/technetwork/articles/entarch/effective-exceptions-092345.html)

Exception throwing / handling philosophy is a subject of debate even in the docs: [exceptions/runtime.html](http://docs.oracle.com/javase/tutorial/essential/exceptions/runtime.html)


##The Throwable Class Hierarchy

* Throwable
  * Error - unchecked
    * OutOfMemoryError
  * Exeception  - checked
    * RuntimeException - unchecked
      * IllegalArgumentException
      * NullPointerException
    * FileNotFoundException - checked

* Using methods that declare checked exceptions
  * Decide if you can handle it
  * Decide if your caller needs to handle it

* Handling unchecked exceptions
  * ``RuntimeException``s mostly represent bugs
  * ``Error``s mostly represent things you cannot handle

* Throwing self generated exceptions
  * Throw runtime exceptions for bugs
    * Use existing Exception type if applicable
    * NullPointerException or IllegalArgumentException
  * Throw checked exception for anticipated but  exceptional conditions
    * FileNotFoundException
    * Create own subclass of exception if necessary
  * Document your decisions in your javadoc comments

* [Java Tutorial](http://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)


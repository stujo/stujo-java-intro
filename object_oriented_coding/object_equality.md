# Object Equality

* ``==`` vs ``equals``

* [``equals``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#equals%28java.lang.Object%29) and [``hashCode``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#hashCode%28%29)

###Exercise
* __EXERCISE:__ Write a Java class called ``Employee`` with fields for ``firstName``, ``lastName`` and  . Override ``toString`` in a meaningful way. Now try and implement equals and hashCode according to the documentation provided

* __EXERCISE:__ Write some ``@Test``s for your ``equals`` code

###Demo
* __DEMO:__ Eclipse Generators


###Dates and Calendars (Java Platform)
* For this exercise [``GregorianCalendar.html#GregorianCalendar(int, int, int)``](http://docs.oracle.com/javase/6/docs/api/java/util/GregorianCalendar.html#GregorianCalendar%28int, int, int%29) might be handy


###Exercise
* __EXERCISE:__ Add ``dateOfBirth`` as ``java.util.Date`` to your Employee Class
* __DISCUSSION:__ GregorianCalendar - Allows you to create dates and Calendar - Date Math
* __EXERCISE:__ Run your tests again from the previous exercise

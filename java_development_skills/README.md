# Java Development Skills

* Java is an programming language based on the object oriented principles of:
  * P Polymorphism
  * I Inheritance
  * E Encapsulation

* Would you like some PIE?

* Unlike most compiled languages, the compiler (``javac``) produces __bytecode__ instead of __binary files__. This allows the same code to run on multiple platforms, with platform specific ``JVM``s __Java Virtual Machines__


* Explain the Java Development Workflow
 * ``.java`` File
 * ``javac``
 * Compile-Time ``CLASSPATH``
 * ``.class`` file
 * ``java``
 * Run-Time ``CLASSPATH``
 * Hello World!

* [](http://www.oracle.com/technetwork/topics/newtojava/downloads/index.html)
* Write Hello World java application with no tools (Requires: text editor)

__EXERCISE:__ Create projects folder

```
mkdir projects
cd projects
```

__EXERCISE:__ Create a HelloWorld Java Application

```
cd projects
mkdir scratch
cd scratch/
mkdir src
vi src/HelloWorld.java
```

* ``public static void`` - Access Modifiers
* ``main``
* ``String[] args``
* ``System.out.println()``
* Compile your application (Requires: javac from the JDK) (javac -verbose HelloWorld.java)

```
javac src/HelloWorld.java
```
* Run your Application (Requires: java from JRE)

```
java -cp ./src HelloWorld
```
* ``-verbose`` option:

```
javac -verbose src/HelloWorld.java
java -verbose -cp ./src HelloWorld
```

* ``-d`` option

* [Intro CLASS_PATH](http://docs.oracle.com/javase/tutorial/essential/environment/paths.html)

* __CHECKPOINT:__ Know how to create an application from scratch

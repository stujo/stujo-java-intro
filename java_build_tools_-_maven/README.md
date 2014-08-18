# Java Build Tools - Maven
* Generate a template application with Maven (App + AppTest)
 * ``mvn archetype:generate``
* Use Maven to Build and Package a Java Application
* Use Maven to run JUnit Unit Tests for your code
* Build, Test and Package:
```
$ mvn package
```

* Run the app with the correct classpath:
```
$ mvn exec:java -Dexec.mainClass=com.example.java5day.App
```
* Import a maven project into Eclipse (Requires: Maven Integration for Eclipse)

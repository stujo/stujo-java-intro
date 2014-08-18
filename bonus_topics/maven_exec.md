# Maven Exec

Useful for quickly firing up your app

* [Maven Exec Plugin](http://mojo.codehaus.org/exec-maven-plugin/usage.html)

* ``mvn help:describe -Dplugin=exec -Dfull``

* Sets up the ``classpath``:

* `` mvn exec:java -Dexec.mainClass=com.example.Main -Dexec.args="94103"``

* ``mvn dependency:resolve``
* ``mvn dependency:tree``


* [3 Ways to Run Java Main](http://www.vineetmanohar.com/2009/11/3-ways-to-run-java-main-from-maven/)


Building Self Contained Artifacts

* Simple
  * [Assembly Plugin](http://maven.apache.org/plugins/maven-assembly-plugin/)

* Uber Jar
  * [Shade Plugin](http://maven.apache.org/plugins/maven-shade-plugin/)

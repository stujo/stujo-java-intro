# Self Executing Jar

To Run a Java application the JVM needs the following resources on the CLASSPATH

* Your compiled code (bytecode) classes
  * This is usually packaged in a ``.jar`` file
* Any libraries your code imported that are not a part of the platform
  * e.g. ``sqlite``, ``opencsv``

You can use wildcards, but only to select .jar files in a given directory

```
java -cp ./lib/*:myapp.jar com.example.MyApp
```

This works find but sometimes we want to be able to run an app without having to send out multiple files, the [maven shade plugin](http://maven.apache.org/plugins/maven-shade-plugin/) can help. It creates a single jar with all our dependencies. We also want to be able to execute the application without specifying the complete main class name on the command line.

Add the ``maven-shade-plugin`` to your build plugins in your ``pom.xml`` as below, replacing the example with your main class:

```
<project>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-shade-plugin</artifactId>
        <version>2.3</version>
        <executions>
          <execution>
            <phase>package</phase>
            <goals>
              <goal>shade</goal>
            </goals>
            <configuration>
              <transformers>
                <transformer implementation="org.apache.maven.plugins.shade.resource.ManifestResourceTransformer">
                  <mainClass>com.example.MainClassName</mainClass>
                </transformer>
              </transformers>
            </configuration>
          </execution>
        </executions>
      </plugin>
    </plugins>
  </build>
  ...
</project>

```

* Next run ``mvn package``

This does the build and then re-packages the jar to include the dependent classes and specify the main class in the jar's meta data.

* Next you can try ``java -jar target/the-jar-file-name.jar``

Replacing the-jar-file-name with your artifactId

* Hopefully your app runs!






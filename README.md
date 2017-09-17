# java-useful-tips

## Java language
##### JRE remote debug
add -agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=8074 to JRE options, suspend=y for suspend, 8074 is debug port.



## Eclipse
##### auto refresh resources
from Eclipse 3.7, check windows > preferences > general > workspace > Refresh using native hooks or polling

##### better hot swap
try jrebel (install using eclipse marketplace)

##### can not open java source in windowsbuilder
right click file > open with, select proper editor.

##### compile error for old API like BASE64Decoder 
windows > preferences > Java > Compiler > Deprecated and restricted API, set Forbidden reference to  Warning.

##### paste multi line text to java string
Preferences > Java > Editor > Typing, check "Escape text when pasting into a string literal"

## Maven

##### set project local repository
in pom file, add:
```xml
<repositories>
 	<repository>
        <id>project.local</id>
        <name>project</name>
        <url>file:${project.basedir}/repo</url>
    </repository>
</repositories>
```
##### Dependency convergence check
in pom file, add: 
```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-enforcer-plugin</artifactId>
    <version>1.4.1</version>
    <executions>
      <execution>
        <id>enforce</id>
        <configuration>
          <rules>
            <DependencyConvergence />
          </rules>
        </configuration>
        <goals>
          <goal>enforce</goal>
        </goals>
      </execution>
    </executions>
</plugin>
```

## Swing

##### how to add undo and redo to JTextArea?
http://www.java-tips.org/java-se-tips-100019/44-javax-swing-undo/1964-how-to-add-undo-and-redo-to-a-text-component.html


## linux
##### JVM Delays Caused by Random Number Generation
add -Djava.security.egd=file:/dev/./urandom to JRE options

## Don't Reinvent The Wheel
* [joor](https://github.com/jOOQ/jOOR) better reflection
* [liquibase](http://www.liquibase.org/) source control for database




























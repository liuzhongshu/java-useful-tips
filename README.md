# java-useful-tips

## Java language

## Eclipse
##### hot swap not working
check project/Build Automatically, uncheck windows > preferences > Java > Compiler > Building > Abort build when build path errors occur.

##### can not open java source in windowsbuilder
right click file > open with, select proper editor.

##### compile error for old API like BASE64Decoder 
windows > preferences > Java > Compiler > Deprecated and restricted API, set Forbidden reference to  Warning.

## Maven

##### how to set project local repository
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































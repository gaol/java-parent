# java-parent
Maven parent project with handy configuration and plugins

## Enable debug when executing the test case

> mvn clean install -Djpda

or 

> mvn clean install -Pjpda

This will start the `maven-surefire-plugin` with the following arguments:

> -agentlib:jdwp=transport=dt_socket,address=8787,server=y,suspend=y

The test will suspend and wait remote debugging on part: `8787`

## Run tests on JDK 9 +

Modules are introduced in JDK9+, to be able to run the tests on JDK9+, the following arguments are added:

```
 --add-exports=java.base/sun.nio.ch=ALL-UNNAMED
 --add-exports=jdk.unsupported/sun.reflect=ALL-UNNAMED
 --add-exports=jdk.unsupported/sun.misc=ALL-UNNAMED
 --add-modules=java.se
```

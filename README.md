# Problem with JavaParser and module-info.java files

Compile the demo:

```shell
./gradlew clean assemble
```

Run the example: `java -jar build/libs/javaparser-module-bug-all.jar src/`

You should see one line of output:

```
Found src/main/java/demo/Main.java
```

Copy the `example-module-info.java` file:

`cp -i example-module-info.java src/main/java/`

Run the example again: `java -jar build/libs/javaparser-module-bug-all.jar src/`

I would expect one or two lines of output, but get none.

Note that the file name is `example-module-info.java` and not the real name `module-info.java`.

It's not even the file name that matters, it is the `module demo {}` content.

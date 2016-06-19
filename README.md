# Hello Jigsaw

This is a demo for JDK 9 Module System / Project Jigsaw
It just prints Hello Jigsaw in console.
But the project structure / Compiling and running is a little different also take note of the module-info.java class. 


This workspace contain 3 packages(Each is a module as in JDK 9) in the src folder:

*com.foo.app
- Contains the Main Class
*com.foo.bar
-Contains a class that return Hello String from a static method
com.foo.baz
-Contains a class that return Jigsaw String from a static method

##To Compile
Each Module to be compiled separately:

```javac -d mods/com.foo.baz src/com/foo/baz/module-info.java src/com/foo/baz/Jigsaw.java ```

```javac -d mods/com.foo.bar src/com/foo/bar/module-info.java src/com/foo/bar/Hello.java ```

```javac9 -mp mods/ -d mods/com.foo.app src/com/foo/app/module-info.java src/com/foo/app/Main.java```

##To Execute the program
```java -mp mods/ -m com.foo.app/com.foo.app.Main```



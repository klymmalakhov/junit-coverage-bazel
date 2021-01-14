Bazel Maven Java Jacoco application
----------------------

In this project I would like to count a JUnit coverage using a Jacoco library based on the existed Maven project [`coverage_with_jacoco`](https://github.com/klymmalakhov/coverage_with_jacoco)   where we are creation a coverage report by Jacoco library. 

Build the application by running:

```
$ bazel build :java-maven
```

Test the application by running:

```
$ bazel test :tests
```



### Coverage

Generate a file with coverage data in the **LCOV format**
 
 ```
 $  bazel coverage tests --combined_report=lcov
 ```

Generate a ***console output** based on the coverage report:
 
 ```
 $  lcov --list  <FILE_PATH>/tests/coverage.dat

 ```

Generate a **HTML report** based on the coverage report:

```
$ genhtml  <FILE_PATH>/tests/coverage.dat
```

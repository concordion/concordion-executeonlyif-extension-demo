[![Build Status](https://travis-ci.org/concordion/concordion-executeonlyif-extension-demo.svg?branch=master)](https://travis-ci.org/concordion/concordion-executeonlyif-extension-demo)
[![Apache License 2.0](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

# Introduction
------------

This project demonstrates the usage of the [Concordion](https://concordion.org) [ExecuteOnlyif Extension](http://github.com/concordion/concordion-executeonlyif-extension).

Example output is shown [here](http://concordion.github.io/concordion-executeonlyif-extension-demo/spec/org/concordion/ext/demo/ExecuteOnlyIfDemo.html).

    
# Running the tests
---------------------------

The download includes support to run the tests with the [Gradle](http://www.gradle.org/) build tool. The code base includes the Gradle Wrapper, which will automatically download the correct version of Gradle. 

Gradle can be run from the command line or from your IDE:

Command line
============
From the command line, `cd` to the folder containing a copy of this project, and run 

  `./gradlew clean test` on Unix-based systems, or 
  `.\gradlew clean test` on Windows.

This will download the required dependencies, clean the existing project, recompile all source code and run all the tests. 

View the Concordion output in `build/reports/spec/org/concordion/ext/demo/ExecuteOnlyIfDemo.html`.


IDE
===
For Eclipse and NetBeans, you will need to install a Gradle plugin to your IDE before importing the project. See [Gradle tooling](https://www.gradle.org/tooling) for details.

On importing the project to your IDE, the required dependencies will be downloaded.

Under the `src/test/java` folder, find the `ExecuteOnlyIfDemo` class in the `org.concordion.ext.demo` package and run as a JUnit test. The location of the Concordion output is shown on the standard output console.

What you should see
--------------------------------
    
### JUnit output
The test should pass successfully, though the console output will show 2 tests as ignored:

```Successes: 2, Failures: 0, Ignored: 2```

### Concordion output
The output folder should contain the following specification. (You can see an example of it [here](http://concordion.github.io/concordion-executeonlyif-extension-demo/spec/org/concordion/ext/demo/ExecuteOnlyIfDemo.html)).
    
#### ExecuteOnlyIfDemo.html

Example 2 is ignored since the conditional test returns false. It also shows the use of the Embed extension to show a reason of why the example is ignored.

Example 3 shows that a link to a specification is highlighted in grey, when that specification contains a test that is ignored using this extension.

Additional Gradle Files
-----------------------
`dev.gradle` is only needed if you want to run against snapshot or local builds of the concordion-executeonlyif-extension.

`publish.gradle` is only needed if you want to publish the output to Github pages.

If copying the project for your own use, you probably won't want either of these files.

Mailing List
-----------------
Feel free to discuss this demo project on the Concordion [mailing list](https://groups.google.com/d/forum/concordion).

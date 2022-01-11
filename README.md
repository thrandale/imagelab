# ImageLab

ImageLab is a framework that allows students to develop
image modification processors (filters) and to experience
the results visually and aurally.

## Contents
- The __imagelab__ and __sound__ packages may be provided in an `imagelab.jar` file.
- The `imagelab.jar` file also includes the class __Run__ with a `public static void main` method in the unnamed package, used to facilitate running the ImageLab application.
- The repository contents may also be used directly as a [BlueJ](http://bluej.org) project.
- The __filter__ package is generally provided as a folder with source (`.java`) and compiled (`.class`) files, with the source versions serving as examples for students to create their own filters.
- A sample set of images are provided in an __"images"__ directory.

## Creating an executable jar file
The project is set up to use gradle wrapper to create the jar file.
1. Change the working directory to be the project's root directory.
2. Execute the command `./gradlew build`
   A. This will build/rebuild the jar file and required dependencies.
3. The new jar file will be named "imagelab.jar" and located in the project's root directory.

More information on gradle can be found [here](https://docs.gradle.org/current/userguide/userguide.html) and more information on the gradle wrapper can be found [here](https://docs.gradle.org/current/userguide/gradle_wrapper.html).

If there is no automated build environment set up, the jar file can be created using the `jar` command.
1. CHange the working directory to be the project's root directory.
2. Execute the command `javac Run.java` to compile the Run.java file.
3. Execute the command `javac */*.java` to compile/recompile the files in packages imagelab, sound, and filters.
4. In the root directory execute the command `echo Main-Class: Run > MANIFEST.MF` to create the manifest file for the jar.
5. Create the jar using the command `jar cfm imagelab.jar MANIFEST.MF *.class sound/*.class imagelab/*.class`
6. The new jar file will be named "imagelab.jar" and located in the project's root directory.

More information on creating the jar can be found [here](https://docs.oracle.com/javase/tutorial/deployment/jar/build.html) and more information about java commands can be found [here.](https://docs.oracle.com/en/java/javase/15/docs/specs/man/index.html)

An executable jar file can also be created within most IDEs.

## To use from command line:  
* Change the working directory to be the one that contains the __imagelab.jar__ file.
* Make sure the __filters__ directory is _in the same directory_ as the __imagelab.jar__ file and that it contains at least one filter.
* If the filter source code is not yet compiled, issue the command
`javac -cp .:imagelab.jar filters/*.java`
* Run the ImageLab application using the command  
`java -cp ".:imagelab.jar" Run`  
(Note that on Windows platforms, the ":" character in the classpath must be changed to the ";" character.)

## Build Instructions 

### Build System Requirements
- Install Gradle
  * Gradle is the tool used in this repository for automation of the build. Please visit https://gradle.org/ for specific installation instructions.

### Using Gradle
To build the project from a copy of the repository use the command:  
   `./gradlew build`

#### Useful Commands
  * Display the full list of tasks that can be excecuted  
    * `./gradlew tasks --all`  
  * Run the program  
    * `./gradlew run`  
  * Compile the main java source  
    * `./gradlew compileJava`  
  * Delete the build directory  
    * `./gradlew clean` 
  * Assemble the main classes  
    * `./gradlew classes`    
  * Assemble and test the project
    * `./gradlew build`   
  * Assemble the test classes  
    * `./gradlew testClasses`  
  * Generate checkstyle reports 
    * `./gradlew checkstyle`  
  * Run unit tests
    * `./gradlew test`  
  * Compile unit tests  
    * `./gradlew compileTestJava`   
  * Run all checks 
    * `./gradlew check`   


### Resources and References

https://gradle.org/guides/


## License

ImageLab is a framework for student exploration of image processing.  
Copyright (C) 2016,2019 by Aaron Gordon & Jody Paul  
The software comes with ABSOLUTELY NO WARRANTY.
 
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see https://www.gnu.org/licenses/

___

Project Website: https://metrocs.github.io/imagelab/

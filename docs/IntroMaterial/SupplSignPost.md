# Supplementary Signposting Document to Accompany The Introductory Exercises

## Pre-face
This document is aimed at students with little or no C-programming experience, but maybe used as a signposted reference for anyone. For students with little or no C-programming experience, this document can be used in parallel to the  <debugHL>[Introductory Exercises document](./IntroExercises.md)</debugHL>. This document provides structured signposted links to the <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL> tutorial website, <debugHL>[C-Programming.com](https://www.cprogramming.com/){target="_blank"}</debugHL>, the <debugHL>[Arduino programming reference](https://docs.arduino.cc/language-reference/){target="_blank"}</debugHL>, and also links in some of the early exercises from the <debugHL>[Introductory Exercises document](./IntroExercises.md)</debugHL>.

Students with some C-programming skills may wish to skip this document, and go on to the only use the <debugHL>[Introductory Exercises document](./IntroExercises.md)</debugHL> or skip these and go straight to the first of the assessed exercises: <debugHL>[Basic: LED Pattern](../BasicExercises/ledPattern.md)</debugHL>

## Introduction

In previous years it has become evident that some groups of students, taking the Mechatronics modules, do not have any background experience on programming in C/C++ or experience with using Arduino or other microcontroller based development systems. As a result, these students have struggled with some of the basics of the Mechatronics laboratory activities, due to not having learned any C-programming skills before starting this module.

To provide you with comprehensive instruction into C-programming is both outside the scope of this module and would take far more time than is available for the teaching/contact time allocated to this module. There are countless very good on-line resources for self-paced learning of programming languages. Therefore, instead of writing yet another tutorial, this document will provide you with some signposts to resources for basic C programming topics that we think are necessary to facilitate the laboratory activities within this module. 

!!!NOTE
    This document is not aimed at providing you with a comprehensive list of topics required for this module, and it may be necessary for you to discover further resources to improve your programming knowledge and skills.

In this iteration of this document we will signpost some of the tutorial resources from <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL>, sections from <debugHL>[C-Programming.com](https://www.cprogramming.com/){target="_blank"}</debugHL>, and the programming references and examples/tutorials from the <debugHL>[Arduino website](https://docs.arduino.cc/){target="_blank"}</debugHL>.

It will be up to you to self-guide your own learning to improve your skills and understanding, required for the labs and your project activities, and if necessary discover further resources. (If you do find topics/resources that you think would be of benefit, please make us aware of these, and if appropriate, we may provide further sign posting to these materials.)

The remaining subsections of the introduction highlight some resources you may find useful whilst going through the remainder of this document, and while you are completing the mechatronics module laboratory exercises and project.

### External tutorial websites linked from this document

The tutorials provided on <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL> are aimed at programming for computer systems, (PC, Linux, etc), and not specifically for embedded C-programming, the likes of which we will be doing on the Arduino platform. As a result, there are some slight differences in the structure of the Arduino programs, or ‘Sketches’ as they are known. However, these <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL> tutorials provide a good introduction to the basics of C programming, and we have supplemented them with signposted information from the <debugHL>[Arduino website](https://docs.arduino.cc/){target="_blank"}</debugHL>.

Each <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL> tutorial provides a short introduction to each topic and has an on-line compiler that allows you to practice parts of each tutorial exercise, and topics discussed. These should provide sufficient background for you to complete the Mechatronics laboratory exercises.

Another useful resource is <debugHL>[C-Programming.com](https://www.cprogramming.com/){target="_blank"}</debugHL>, (again aimed at programming for computer systems), which provides a more in depth overview/tutorial for learning C, and you may only wish to consider the lessons from the <debugHL>[”Introduction and Basic C Features” section of the C-Tutorial](https://www.cprogramming.com/tutorial/c-tutorial.html?inl=nv){target="_blank"}</debugHL>

!!! Note
    In the next section of this document we have selected relevant sections from the <debugHL>[C-Programming.com](https://www.cprogramming.com/){target="_blank"}</debugHL> and <debugHL>[C-Programming.com](https://www.cprogramming.com/){target="_blank"}</debugHL> websites, and linked them with relevant material from the Arduino language guide. It is suggested that you access these tutorials as instructed in the following sections. 

### Arduino Language Reference

The <debugHL>[Arduino programming reference](https://docs.arduino.cc/language-reference/){target="_blank"}</debugHL> is a web page, within the Arduino website, which provides a complete reference for Arduino functions, variables and programming structures for the core Arduino language. The language reference may seem a little daunting to a novice programmer, but is a very useful resource when you have some experience with Arduino programming. 
!!! Note
    Relevant sections of the <debugHL>[Arduino programming reference](https://docs.arduino.cc/language-reference/){target="_blank"}</debugHL> are linked throughout the remainder of this document, therefore, it is not necessary to read it before proceeding.

### Arduino Build-in Examples within the Arduino IDE

There is a <debugHL>[tutorials section](https://www.arduino.cc/en/Tutorial/HomePage){target="_blank"}</debugHL> within the Arduino web site, which provides you with a large range of tutorials, from simple getting started guides for the software and hardware, through to the descriptions of the Arduino Software’s <debugHL>[build-in examples](https://www.arduino.cc/en/Tutorial/BuiltInExamples){target="_blank"}</debugHL>. There are also links into tutorials on the <debugHL>[Arduino Project Hub](https://projecthub.arduino.cc/){target="_blank"}</debugHL>, and links to other more advanced topics to help expand your capabilities.

Some of the links sections within the <debugHL>[tutorials section](https://www.arduino.cc/en/Tutorial/HomePage){target="_blank"}</debugHL> section may be useful when you come to do your project.

## Introduction to Programming an Arduino in C.

The remainder of this document is aimed at providing you with a structured set of signposted links to help build your understanding of the basics of C-programming. This document will signpost you to a number of tutorials on the <debugHL>[Learn-C](https://www.learn-c.org/){target="_blank"}</debugHL> website, and interweave these with signposted links to relevant sections of the <debugHL>[Arduino programming reference](https://docs.arduino.cc/language-reference/){target="_blank"}</debugHL>, and some of the early exercises from the <debugHL>[Introductory Exercises document](./IntroExercises.md)</debugHL>. 

The Arduino programming libraries are a series of C/C++ functions that can be called from the code you write. The native programming languages for Arduino are either C or C++. Throughout the remainder of this module, we will only be considering programming Arduino in C. 

(For those interested, there is a brief overview and history of the C-programming language on the <debugHL>[Wikipedia site](https://en.wikipedia.org/wiki/C_(programming_language)){target="_blank"}</debugHL>.)

### Hello World Example
A typical place to start with any programming language is the “Hello World” example - (See the <debugHL>[“Hello World”](https://www.learn-c.org/en/Hello%2C_World%21){target="_blank"}</debugHL> example from the Learn-C Tutorial), this illustrates the basic structure of a programming language, using a program that writes the words “Hello World” to the “standard output”. 

!!! info "The Standard Output in Arduino"
    In Arduino, there is no standard output, because it is an embedded operating system operating without a console terminal. Generally, we direct the standard output to the <debugHL>[serial monitor](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/){target="_blank"}</debugHL> in the Arduino IDE. This will be discussed in a later section.

The following programming syntax, (linked from the Arduino language reference), are necessary for correct implementation of your code:

* <debugHL>[Semicolon](https://www.arduino.cc/reference/en/language/structure/further-syntax/semicolon/){target="_blank"}</debugHL>
* <debugHL>[Curly braces](https://www.arduino.cc/reference/cs/language/structure/further-syntax/curlybraces/){target="_blank"}</debugHL>

Code comments are a readable explanation or annotation of the code that you have written. You should provide comments throughout your code to help explain what you have written and why you have written it in that way. Code comments are an invaluable tool to help you debug code that is not working in the manner intended, and should be updated when code is changed. Links to how to implement code commenting in Arduino:

* <debugHL>[Single Line Comment](https://docs.arduino.cc/language-reference/en/structure/further-syntax/singleLineComment/){target="_blank"}</debugHL>
* <debugHL>[Block Comment](https://docs.arduino.cc/language-reference/en/structure/further-syntax/singleLineComment){target="_blank"}</debugHL>

Simple Macros are a very useful tool when writing clear and effective embedded code, not only helping with the readability of your code, but also help when trying to debug your work. The <debugHL>[#define](https://docs.arduino.cc/language-reference/en/structure/further-syntax/define/){target="_blank"}</debugHL> directive replace a constant numeric value throughout your code, with a simple name defined in the global namespace. This can simplify the readability of your code and allow you to quickly update these distributed constants from a single location. The <debugHL>[#define](https://docs.arduino.cc/language-reference/en/structure/further-syntax/define/){target="_blank"}</debugHL> can also be used to create macros for small blocks of instructions, but care must be used, because it may be more appropriate to use a function instead.

Whilst programming, you may wish to link an external library into your Arduino code. The <debugHL>[#include](https://docs.arduino.cc/language-reference/en/structure/further-syntax/include/){target="_blank"}</debugHL> directive can be used to link external libraries into your work, such as an external library of code to interface a servo device.

### Variables and Numbers
One of the key considerations when programming computer systems and embedded systems, is the handling and storage of different types of numbers. The <debugHL>[Variables and numbers](https://www.learn-c.org/en/Variables_and_Types){target="_blank"}</debugHL> - tutorial from Learn-C provides a brief introduction to this, but does not consider the conversion between data types. See the <debugHL>[variables section of Arduino Language Reference](https://docs.arduino.cc/language-reference/#variables){target="_blank"}</debugHL> for a more detailed list of variable types and commands used to convert between them.

(Also see the Using Variables section of the <debugHL>[Introduction to C lesson](https://www.cprogramming.com/tutorial/c/lesson1.html){target="_blank"}</debugHL> from C-Programming.com)

Arrays are a data structure that is essentially a list/collection of values of the same data type, arranged in an indexed manner - See <debugHL>[Arrays - Learn-C Tutorial](https://www.learn-c.org/en/Multidimensional_Arrays){target="_blank"}</debugHL>, and the <debugHL>[Array section of the Arduino Language Reference](https://docs.arduino.cc/language-reference/en/variables/data-types/array/){target="_blank"}</debugHL>. Multidimensional arrays can also store <debugHL>[multidimensional data](https://www.learn-c.org/en/Multidimensional_Arrays){target="_blank"}</debugHL>, by employing more than one set of indexes, e.g. a 2-dimensional array would be arranged similar to a spreadsheet of data and would have 2 sets of indices. 

(Another, and more comprehensive, reference for Arrays in C, is provided in <debugHL>[lesson-8 of C Tutorial in C-Programming.com](https://www.cprogramming.com/tutorial/c/lesson8.html){target="_blank"}</debugHL>.)

### Functions

Functions are blocks of code that perform a predefined set of commands, and are either used to ‘tidy-up’ your code to make it more readable, or to perform repeated activities. As you write your Arduino code, you will be using some of the built-in and 3rd party library functions, and you may also wish to define your own.
Functions are discussed in the <debugHL>[Learn-C, Functions tutorial](https://www.learn-c.org/en/Functions){target="_blank"}</debugHL> and the <debugHL>[Functions in C lesson from C-Programming](https://www.cprogramming.com/tutorial/c/lesson4.html){target="_blank"}</debugHL>.

### <debugHL>[Blink Example](./IntroExercises.md/#intro-exercise-1-blink-example)</debugHL> - Introductory Exercise

The <debugHL>[blink example](./IntroExercises.md/#intro-exercise-1-blink-example)</debugHL> is used in the Introductory Exercises, and can be accessed from the Arduino IDE files menu : 

*Files > Examples > 01.Basics > Blink*

The <debugHL>[in-build example tutorial for the Blink](https://docs.arduino.cc/built-in-examples/basics/Blink/){target="_blank"}</debugHL> program is provided in the Arduino Tutorial section of the website. (Note: Arduino suggest using a 220𝛺 resistor, but in Exercise 1 will instruct you to use a 470𝛺 resistor.)

The Blink example code is a simple test program, often used to ensure the Arduino compiler is working correctly, and the hardware can communicate with the IDE correctly. Look at the Arduino code example, there are three sections to the code:

* Global namespace - area at the top of the code used for declaration of global variables and location for compiler directives, such as #define and #include instructions
* <debugHL>[setup()](https://docs.arduino.cc/language-reference/en/structure/sketch/setup/){target="_blank"}</debugHL> function - This function runs once at the start of the program and is generally used to initialise variables, hardware and libraries, and to define I/O pin modes.
* <debugHL>[loop()](https://docs.arduino.cc/language-reference/en/structure/sketch/loop/){target="_blank"}</debugHL> function - This function is the generally main body of your Arduino program, and loop continuously, allowing your system hardware to be read and controlled each loop iteration.

You will notice the use of the <debugHL>[delay()](https://docs.arduino.cc/language-reference/en/functions/time/delay/){target="_blank"}</debugHL> function. This is a simple time delay function used to control the execution of your code.

At this point is worth signposting:

* The while loop is a programming structure that will continuously loop until a logical termination is satisfied
* The for loop is a programming structure that will loop for a pre-specified number of iterations.

Learn-C provides tutorials for the <debugHL>[for loop](https://www.learn-c.org/en/For_loops){target="_blank"}</debugHL> and the <debugHL>[while loop](https://www.learn-c.org/en/While_loops){target="_blank"}</debugHL> structures. Both of these structures are discussed on <debugHL>[Loops in C lesson from C-Programming.com](https://www.cprogramming.com/tutorial/c/lesson3.html){target="_blank"}</debugHL>. The Arduino Language reference also has sections for the <debugHL>[for loop](https://docs.arduino.cc/language-reference/en/structure/control-structure/for/){target="_blank"}</debugHL> and the <debugHL>[while loop](https://docs.arduino.cc/language-reference/en/structure/control-structure/while/){target="_blank"}</debugHL> structures

### Decision making

One of the basic tasks we use computer systems for is decision making, based on logical conditions and inputs. The Learn-C <debugHL>[Conditions tutorial](https://www.learn-c.org/en/Conditions){target="_blank"}</debugHL> provides an introduction to using the if statement on C. The Arduino language reference for the <debugHL>[if statement](https://docs.arduino.cc/language-reference/en/structure/control-structure/if/){target="_blank"}</debugHL> is linked here, but you should also look at the different logical and comparison operation from the <debugHL>[Arduino language reference](https://docs.arduino.cc/language-reference/#structure){target="_blank"}</debugHL>, located in the structures section. The if statement, logical and relational operators are also discussed in the <debugHL>[If Statements in C](https://www.cprogramming.com/tutorial/c/lesson2.html){target="_blank"}</debugHL> lesson of C-Programming.com.

At this point it is worth mentioning the switch case structure in C. This is a more advanced topic but you may find it a useful programming structure for your projects: <debugHL>[Arduino language reference](https://www.arduino.cc/reference/cs/language/structure/control-structure/switchcase/){target="_blank"}</debugHL> and <debugHL>[C-Programming.com lesson](https://www.cprogramming.com/tutorial/c/lesson5.html){target="_blank"}</debugHL>.

The switch case structure can be used in the place of a long if structure that uses a definite value of a control variable to select one or more blocks of code to be executed. Switch case structures and widely used when programming state machine type behaviour. 

<debugHL>[Finite state machines](https://en.wikipedia.org/wiki/Finite-state_machine){target="_blank"}</debugHL> are a useful conceptual design tool when implementing sequenced and decision-based behaviour. You may find them useful when implementing the software for your project, but they will not be further discussed in this material.

### Serial Monitor

As previously mentioned, there is no standard output for Arduino hardware. When using Arduino hardware, a serial terminal is often used to read user generated messages from the Arduino hardware, or to stream variable values to a readable interface. The Serial Monitor, in the Arduino IDE, provides a convenient serial terminal to view text based messages generated from your Arduino code.

The <debugHL>[Instructables.com “HOW-TO Use the ARDUINO SERIAL MONITOR”](https://www.instructables.com/HOW-TO-use-the-ARDUINO-SERIAL-MONITOR/){target="_blank"}</debugHL> how-to web page provides an insight into the use of the serial monitor. You will notice that the code provided in this tutorial uses a number of the <debugHL>[serial communications functions](https://docs.arduino.cc/language-reference/en/functions/communication/serial/){target="_blank"}</debugHL>, which are described in the Arduino language reference. Data sent across the serial interface to the serial monitor.

### The string data type
Before using the serial monitor it is worth going through the Learn-C Tutorial on <debugHL>[Strings](https://www.learn-c.org/en/Strings){target="_blank"}</debugHL>, and being aware of the <debugHL>[String as an array of characters](https://docs.arduino.cc/language-reference/en/variables/data-types/string/){target="_blank"}</debugHL> section and the <debugHL>[String DataType object](https://docs.arduino.cc/language-reference/en/variables/data-types/stringObject/){target="_blank"}</debugHL> section of the Arduino language reference.

### <debugHL>[Push button and LED Example](./IntroExercises.md#intro-exercise-2-push-button-and-led)</debugHL> - Introductory Exercise

The <debugHL>[Push button and LED example](./IntroExercises.md#intro-exercise-2-push-button-and-led)</debugHL> is based on the Button example from the in-built Arduino examples - <debugHL>[the tutorial for the Button example](https://docs.arduino.cc/built-in-examples/digital/Button/){target="_blank"}</debugHL> is linked, here. The code provided in the laboratory worksheet demonstrates how the serial monitor can be incorporated into an Arduino program, to monitor an internal variable within the code.

## Final Comment

The signposting of background C programming resources provided in the previous sections of this document should be sufficient for you to implement the remaining laboratory work in this Mechatronics module. You may wish to find further resources, either on-line or in print, to help you practice your C programming skills, but you will need to discover these yourself.

If you do find further topics/resources that you think would be beneficial in enriching this document, please make us aware of these topics/resources. If appropriate, we may use some of these resources to improve future iterations of this document

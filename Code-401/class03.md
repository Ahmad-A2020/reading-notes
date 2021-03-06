### Resources:
- [Primitives vs. Objects](https://www.baeldung.com/java-primitives-vs-objects)
-[Exceptions](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)
- [Using Scanner to read in a file in Java](https://docs.oracle.com/javase/tutorial/essential/io/scanning.html)

#### [lab](https://github.com/Ahmad-A2020/java-fundamentals):
![lab3](/Code-401/ScreenShot/lab3-1.PNG)
![lab3](/Code-401/ScreenShot/lab3-2.PNG)
![lab3](/Code-401/ScreenShot/lab3-3.PNG)

### Primitives vs. Objects:
- Java has a two-fold type system consisting of primitives such as int, boolean and reference types such as Integer, Boolean.
- Default values of the primitive types are 0 for numeric types, false for the boolean type, For the wrapper classes, the default value is null.

### Exceptions in Java (read the first three sections on the left: What is an Exception, The Catch or Specify Requirement, Catching and Handling Exceptions).
-  exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions.
- there are three types of the exceptions:  first type is the checked exception; it is exceptional conditions that a well-written application should anticipate and recover from. the second one is error which is  external to the application, and that the application usually cannot anticipate or recover from. finally is the  runtime exception which is exceptional conditions that are internal to the application, and that the application usually cannot anticipate or recover from.
- to write an exception handler. we start with  a try block by providing and followed by one or more catch blocks directly after the try block. 
- The runtime system invokes the exception handler when the handler is the first one in the call stack whose ExceptionType matches the type of the exception thrown.
- after the catch finally block added: the finally block always executes when the try block exits. This ensures that the finally block is executed even if an unexpected exception occurs


### Using Scanner to read in a file in Java
- Java tokens are smallest elements of a program which are identified by the compiler. Tokens in java include identifiers, keywords, literals, operators and, separators.
- Class Scanner. A simple text scanner which can parse primitive types and strings using regular expressions. 
- A Scanner breaks its input into tokens using a delimiter pattern, which by default matches whitespace. The resulting tokens may then be converted into values of different types using the various next methods

Resources:
- [Java Basics](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)
- [compiler](https://www.reddit.com/r/explainlikeimfive/comments/233dq5/eli5_what_does_it_mean_to_compile_code/)
- [Java Documentation](https://www.dummies.com/programming/java/making-sense-of-javas-api-documentation/)



### Java Basics
##### **Variables:** 
The Java programming language defines the following kinds of variables:
- Instance Variables (Non-Static Fields):  it is a variable which is declared in a class but outside of constructors, methods, or blocks.
- Class Variables (Static Fields) :  any field declared with the static modifier
- Local Variables:  specific type of variable that are only available within the context of a particular expression and can only be accessed within the function that defines them.
- Parameters: it is a value that you can pass to a method. 
##### Primitive Data Types: 
Java programming language is statically-typed, which means that all variables must first be declared before they can be used. Java programming language ssupports the following primitive data types: 
- byte: The byte data type is an 8-bit signed two's complement integer. It has a minimum value of -128 and a maximum value of 127 (inclusive). 
- short: The short data type is a 16-bit signed two's complement integer. It has a minimum value of -32,768 and a maximum value of 32,767 (inclusive).
- int: By default, the int data type is a 32-bit signed two's complement integer, which has a minimum value of -231 and a maximum value of 231-1. 
- long: The long data type is a 64-bit two's complement integer. The signed long has a minimum value of -263 and a maximum value of 263-1.
- float: The float data type is a single-precision 32-bit IEEE 754 floating point.
- double: The double data type is a double-precision 64-bit IEEE 754 floating point
- boolean: The boolean data type has only two possible values: true and false.
- char: The char data type is a single 16-bit Unicode character. It has a minimum value of '\u0000' (or 0) and a maximum value of '\uffff' (or 65,535 inclusive).
#####  Arrays: 
An array is a container object that holds a fixed number of values of a single type.Each item in an array is called an element, which is accessed by its numerical index.
- **Declaring a Variable to Refer to an Array** Like declarations for variables of other types, an array declaration has two components: the array's type and the array's name. An array's type is written as type[], where type is the data type of the contained elements; the brackets are special symbols indicating that this variable holds an array.
- **Copying Arrays:** The System class has an arraycopy method that you can use to efficiently copy data from one array into another.
-  **Array Manipulations:** Java SE provides several methods for performing array manipulations (common tasks, such as copying, sorting and searching arrays) in the java.util.Arrays class. 
##### Operators: 
Operators are special symbols that perform specific operations on one, two, or three operands, and then return a result. there are various types of operators including: 
- The Simple Assignment Operator "="
- The Arithmetic Operators
The Java programming language provides operators that perform addition, subtraction, multiplication, and division. 
- The Unary Operators: The unary operators require only one operand; they perform various operations such as incrementing/decrementing a value by one. 
- Equality, Relational, and Conditional Operators: The equality and relational operators determine if one operand is greater than, less than, equal to, or not equal to another operand.
- Bitwise and Bit Shift Operators: The bitwise & operator performs a bitwise AND operation, the bitwise ^ operator performs a bitwise exclusive OR operation, and the bitwise | operator performs a bitwise inclusive OR operation.



### The first response in this Reddit thread on compiling
### XKCD: Compiling
### Reading Java Documentation
#### Summarized from the Duckett JS book:

##### JavaScript book, Ch. 10, “Error Handling & Debugging”
The aim of this chapter is to help javascript user in finding the code error and ammanded it. 
**EXECUTION CONTEXT** 
Every statement in a script lives in one of three execution contexts:
- GLOBAL CONTEXT: Code that is in the script, but not in a function. There is only one global context in any page.
- FUNCTION CONTEXT: Code that is being run within a function. Each function has its own function context.
- EVAL CONTEXT (NOT SHOWN): Text is executed like code in an internal function
called eval (). 
**VARIABLE SCOPE**
There are two type of variable scope:
- GLOBAL SCOPE:  variables that  declared outside a function, it can be used anywhere because it has global scope. 
- FUNCTION-LEVEL SCOPE: When a variable is declared within a function,
it can only be used within that function. This is because it has function-level scope.
##### EXECUTION CONTEXT & HOISTING: 
Each time a script enters a new execution context, there are two phases
of activity:
-  PREPARE; this includes the following:
   - The new scope is created
   - ariables, functions, and arguments are created
   - The value of the this keyword is determined
-  EXECUTE ; this includes the following:
  - Now it can assign values to variables
  - Reference functions and run their code
  -  Execute statements

##### ERROR: 
- If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code. 
- When an Er ror object is created, it will contain the following properties: 
  - *name*: Type of execution message.
  - *message*: Description. 
  - *file Number*: Name of the JavaScript file.
  - *line Number*: Line number of error

- **ERROR OBJECTS CONTINUED**: 
   - Syntax Error (SYNTAX IS NOT CORRECT): This is caused by incorrect use of the rules of the language. It is often the result of a simple typo.
    - Ref erenceError (VARIABLE DOES NOT EXIST): This is caused by a variable that is not declared or is out of scope.
    - URI Error (INCORRECT USE OF URI FUNCTIONS): If these characters are not escaped in URls, they will cause an error: / ? & I : ;
    - Type Error (VALUE IS UNEXPECTED DATA TYPE): This is often caused by trying to use an object or method that does not exist.
    - RangeError (NUMBER OUTSIDE OF RANGE): If you call a function using numbers outside of its accepted range.
- **Deals with Error**: 
  -  DEBUG THE SCRIPT TO FIX ERRORS: This doing by track down the source of the error, and fix it.
  - HANDLE ERRORS GRACEFULLY: You can handle errors gracefully using try, catch, throw, and fina1ly statements.

- **Debugging** is about deduction: eliminating potential causes of an error.
- The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.Browsers that have a console have a console object, which has several methods that your script can use to display data in the console including: 
   - console . log () method: This method logging data to the console. 
   - console.info(): can be used for general information
   - console.warn(): can be used for warnings.
   - console.error (): can be used to hold errors.
- If you know your code might fail, use try, catch, and finally. Each one is given its own code block. TRY:First, you specify the code that you t hink might throw an exception within the try block. CATCH: If the try code block throws an
exception, catch steps in with an alternative set of code. FINALLY :The contents of the fina11y code block will run either way whether the try block succeeded or failed. 
Resources:
- [Java Imports](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)
- [Different types of loops in Java](https://www.baeldung.com/java-loops)

### Java Imports (ignore the parts about NetBeans):
- Packages: it is the directory contains the .java files (clases).
- to declare Package, we use import statements.
- for the Default package, it's possible to omit the package declaration.
- there are three options for importing classes. first by importing all packages classes such as `import javax.swing.*`, on where the wildcard character (*) indicate to import all classes. second is specified explicitly on import the class name sush as `import javax.swing.JOptionPane`, and the last one is by fully qualified class name without an import such as  `javax.swing.JOptionPane....`.

### Different types of loops in Java:

looping: it is  is a feature which facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false. following are  the loop types in Java: 
-  for loop: use to iteration , which allows code to be executed repeatedly.there are different for loop in java including :
     - simple for loop as illustrate below:  
     `for (initialization; Boolean-expression; step)` 
     `statement;` 
     -  labeled for loops: used in nested for loop so we can break the father one from the parent.
     - enhanced for loops as illustrate below: it is used to iterate over array elements.  
     `for(Type item : items)`
     `statement;` 
     - for-each loops: 
- while loop:  It repeats a statement or a block of statements while its condition is true. 
-  do-while loop: same the while loop, but the first iteration is applied before check the condition. 
# Features of Java

### Platform Independence (Write Once, Run Anywhere)

Java achieves platform independence through its **"Write Once, Run Anywhere"** philosophy. Java programs are compiled into an intermediate bytecode that can be executed on any platform with a compatible Java Virtual Machine (JVM). This enables Java applications to run on diverse operating systems without modification.

### Object-Oriented
Java is a fully object-oriented programming (OOP) language, which means it follows OOP principles such as **encapsulation, inheritance, and polymorphism**. Everything in Java is an object, which simplifies code organization and promotes code reuse.

### Strongly Typed
Java enforces strong data typing, which means variables must be declared with their data types, and type compatibility is strictly checked at compile-time. This helps catch type-related errors early in the development process.

### Portability
Java's platform independence and the availability of JVM implementations for various platforms make it highly portable. Code written in Java can be easily migrated between different environments.

# Real-world applications of Java

### Web Applications

Java is widely used for building web applications, thanks to technologies like Servlets and JavaServer Pages (JSP). Frameworks like Spring and JavaServer Faces (JSF) simplify web application development. Popular websites like LinkedIn, eBay, and Amazon use Java for their backend systems.

### Mobile Applications
Java is used for developing Android applications. Android Studio, the official Android development environment, primarily relies on Java for coding Android apps.

### Gaming
Java is used in game development, with libraries like LibGDX and engines like Minecraft built on Java. It's also used for creating mobile games on the Android platform.

### Cloud Services
Many cloud-based services and platforms, such as Amazon Web Services (AWS) and Microsoft Azure, offer Java SDKs and support for Java applications.

# Java Development Kit (JDK) and the Java Runtime Environment (JRE)

### Java Development Kit (JDK)
The JDK is a software package that provides the necessary tools, libraries, and executables for developing, compiling, and debugging Java applications. It includes the following key components:

- #### Java Compiler (javac)
    The JDK includes the Java compiler, which translates Java source code (.java files) into bytecode (.class files) that can be executed by the Java Virtual Machine (JVM).

- #### Java Virtual Machine (JVM)
    The JDK includes a JVM, which allows developers to run Java applications on their development machines for testing and debugging. It is used to execute compiled bytecode.

### Java Runtime Environment (JRE)
The Java Runtime Environment is a subset of the JDK and is designed solely for running compiled Java applications. It includes the following components:

- #### Java Virtual Machine (JVM)
    The JRE includes the JVM, which is responsible for executing Java bytecode. Unlike the JDK, which contains development tools, the JRE focuses solely on runtime execution.

- #### Java Standard Library
    The JRE includes the Java Standard Library, which consists of the core classes and APIs required to run Java applications. It does not include development or compilation tools, as its purpose is to provide the runtime environment.    

# Components of object-oriented programming

- ### Classes
    Classes are blueprint or templates for creating objects. They define the properties (attributes) and behaviors (methods) that objects of that class will have. Classes encapsulate data and functionality into a single unit.

- ### Objects
    Objects are instances of classes. They represent real-world entities or concepts and encapsulate both data (attributes or properties) and behaviors (methods or functions). Each object has its own state, and changes to an object's state do not affect other objects of the same class.

- ### Abstraction
    Abstraction is the process of simplifying complex systems by modeling classes based on their essential characteristics. It allows you to focus on the relevant details while hiding unnecessary complexity. In OOP, classes are the primary means of abstraction.

- ### Encapsulation
    Encapsulation is the concept of bundling data (attributes) and methods (functions) that operate on that data into a single unit, i.e., a class. It enforces access control, ensuring that data is only accessed and modified through well-defined interfaces (methods). Access modifiers like public, private, and protected help control the visibility of class members.

- ### Inheritance
    Inheritance allows one class (the subclass or derived class) to inherit properties and methods from another class (the superclass or base class). This promotes code reuse and establishes an "is-a" relationship between classes. Subclasses can extend the functionality of their superclass or override inherited methods to provide specialized behavior.

- ### Polymorphism
    Polymorphism means "many forms" and refers to the ability of different objects or classes to respond to the same method or function call in different ways. It allows for flexibility and extensibility in code. Two common forms of polymorphism are compile-time (method overloading) and runtime (method overriding) polymorphism.

- ### Method Overloading
    Method overloading allows a class to have multiple methods with the same name but different parameters. The appropriate method to execute is determined at compile time based on the method's signature.

- ### Method Overriding
    Method overriding occurs when a subclass provides a specific implementation for a method that is already defined in its superclass. The subclass's implementation is used when calling the overridden method on objects of the subclass.

- ### Interfaces
    Interfaces define a contract that a class must adhere to. They specify a set of methods that implementing classes must provide. Multiple inheritance of interfaces is allowed in some programming languages like Java.

# Components of a basic Java program

1. Comments
2. Package Declaration
3. Import Statements
4. Class Definition
5. Main Method
6. Statements and Expressions
7. Access Modifiers (public, private)

# Compile and execute a Java program

1. **Write a Java Program:** Create a text file with a .java extension and write your Java program in it.
2. **Save the File:** Save the file with the same name as the class name and a .java extension  
3. **Open a Command Prompt or Terminal:** Open a command prompt on Windows or a terminal on macOS/Linux. 
4. **Navigate to the Directory:** Use the cd command to navigate to the directory where you saved your .java file.
5. **Compile the Java Program:** Compile the Java program using the javac command followed by the name of your .java file:

    ```bash
    javac HelloWorld.java
    ```

6. **Execute the Java Program:** Run the Java program using the java command followed by the name of your class (without the .class extension): 

    ```bash
    java HelloWorld
    ```

# Describe the java.lang package

The java.lang package is a fundamental package in the Java programming language and is automatically imported into every Java program. It contains classes and interfaces that provide core functionality and fundamental types for Java programs. The classes and interfaces within the java.lang package are so crucial that you don't need to explicitly import them; they are readily available to all Java programs. 

# Final variable
A `final` variable is a constant, and once it's assigned a value, it cannot be changed. Attempting to reassign a final variable will result in a compilation error.

Note that it's a common convention in Java to name constants in uppercase letters with underscores to improve readability, as shown in the example above.

```java
final int MAX_VALUE = 100; // Declaration and Initialization
```
# Cast a value from one data type to another

### Automatic (Implicit) Type Casting (Promotion):

Automatic type casting happens when you convert a value from a smaller data type to a larger one without explicitly specifying the cast. Java performs this type of casting automatically to prevent data loss.

```java
int intValue = 42;
double doubleValue = intValue; // Automatic promotion from int to double
System.out.println(doubleValue); // Output: 42.0
```
### Manual (Explicit) Type Casting:

Manual type casting is used when you want to convert a value from a larger data type to a smaller one, or when you want to force a conversion from one data type to another. Manual casting requires explicit casting syntax.

```java
double doubleValue = 42.56;
int intValue = (int) doubleValue; // Manual casting from double to int
System.out.println(intValue); // Output: 42
```
# Ternary Operator (? :)

The ternary operator ? : is a shorthand way to write a simple conditional expression. It takes three operands: a condition, a value to return if the condition is true, and a value to return if the condition is `false`.

```java
int score = 75;
String result = (score >= 70) ? "Pass" : "Fail";
System.out.println("Result: " + result);
```
# Formatting Strings using escape sequences including `%d`, `%n`, and `%s`

### %d for Formatting Integers:

**`%d`** is used for formatting integers (decimal numbers). You can include it in a string and provide the integer value to be formatted. 

```java
int age = 25;
System.out.printf("My age is %d years old.%n", age);
```

### %s for Formatting Strings

**`%s`** is used for formatting strings. You can use it to insert strings into a formatted text.

```java
String name = "Alice";
System.out.printf("Hello, %s! How are you today?%n", name);
```

### %n for Newline Characters

**`%n`** is an escape sequence that represents a platform-independent newline character. It's used to add line breaks in the formatted output, which ensures that your output is correctly formatted on different operating systems.

```java
System.out.printf("Line 1%nLine 2%nLine 3%n");
```
# Math class in Java

### Exponentiation and Square Root

```java
double base = 2.0;
double exponent = 3.0;

// Exponentiation (2^3)
double result = Math.pow(base, exponent);

// Square root
double squareRoot = Math.sqrt(25.0);

System.out.println("2^3 = " + result);
System.out.println("Square root of 25: " + squareRoot);
```
### Trigonometric Functions

```java
double angleInDegrees = 45.0;

// Sine
double sineValue = Math.sin(Math.toRadians(angleInDegrees));

// Cosine
double cosineValue = Math.cos(Math.toRadians(angleInDegrees));

// Tangent
double tangentValue = Math.tan(Math.toRadians(angleInDegrees));

System.out.println("Sine: " + sineValue);
System.out.println("Cosine: " + cosineValue);
System.out.println("Tangent: " + tangentValue);
```

### Rounding Numbers

```java
double valueToRound = 3.75;

// Round up
double roundedUp = Math.ceil(valueToRound);

// Round down
double roundedDown = Math.floor(valueToRound);

// Round to the nearest integer
double roundedNearest = Math.round(valueToRound);

System.out.println("Rounded up: " + roundedUp);
System.out.println("Rounded down: " + roundedDown);
System.out.println("Rounded to the nearest integer: " + roundedNearest);
```
### Constants

```java
/* The Math class provides several mathematical constants, such as Math.PI (π) and Math.E (the base of the natural logarithm). */

double piValue = Math.PI;
double eValue = Math.E;

System.out.println("π (pi): " + piValue);
System.out.println("e: " + eValue);
```
# Iterators

To traverse an `ArrayList` using an iterator, you need to create an `iterator object` using the `iterator()` method of the ArrayList. Then, you can use the `hasNext()` and `next()` methods of the iterator to iterate through the elements.

```java
import java.util.ArrayList;
import java.util.Iterator;

public class ArrayListTraversal {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.add("Date");

        // Using an iterator
        Iterator<String> iterator = fruits.iterator();
        while (iterator.hasNext()) {
            String fruit = iterator.next();
            System.out.println(fruit);
        }
    }
}
```
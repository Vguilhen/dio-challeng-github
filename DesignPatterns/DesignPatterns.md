# Design Patterns

## About:

Design patterns are reusable Object-Oriented solutions to commonly occurring software design problems.

The main reference book for design patterns is "Design Patterns: Elements of Reusable Object-Oriented Software" by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, also known as the "Gang of Four" (GoF). This book, published in 1994, is considered the seminal work on design patterns and has had a significant impact on software development practices.

In addition to the Gang of Four book, there are other notable books on design patterns, such as "Head First Design Patterns" by Eric Freeman and Elisabeth Robson, "Patterns of Enterprise Application Architecture" by Martin Fowler, and "Domain-Driven Design: Tackling Complexity in the Heart of Software" by Eric Evans.

## Design Patterns Categories:

Design patterns are typically classified into three main categories:

Creational patterns: These patterns are concerned with object creation mechanisms, trying to create objects in a manner that is suitable for a given situation. Creational patterns help to decouple the client code from the objects it needs to instantiate, thereby making it easier to change the object creation process without affecting the rest of the code. Examples of creational patterns include **Singleton**, Factory Method, Abstract Factory, Builder, and Prototype.

Structural patterns: These patterns deal with object composition and help to define how objects can be composed to form larger structures or systems. Structural patterns provide ways to simplify the design of complex systems by identifying simple relationships between objects. Examples of structural patterns include Adapter, Bridge, Composite, Decorator, **Facade**, Flyweight, and Proxy.

Behavioral patterns: These patterns are concerned with communication between objects and how they collaborate to achieve a common goal. Behavioral patterns help to define how objects interact with one another and how they respond to changes in the system. Examples of behavioral patterns include Chain of Responsibility, Command, Interpreter, Iterator, Mediator, Memento, Observer, State, **Strategy**, Template Method, and Visitor.

## Singleton

The Singleton pattern is a creational pattern that ensures that only one instance of a class is created and provides a global point of access to that instance. This pattern is useful in situations where you need to ensure that there is only one instance of a class in your application, such as managing a connection to a database or controlling access to a shared resource.

example:

    public class MyClassName {
        // class implementation
    }

    public class Person {
        // class implementation
    }

    public class PremiumCustomer {
        // class implementation
    }

2 - Variable and method names should start with a lowercase letter and use CamelCase.

example:

    public class MyClass {
        private int myVariable;
    
    public void doSomething() {
        // method implementation
        }
    
    public int getMyVariable() {
        return myVariable;
        }
    }

3 - Constant names should be written in uppercase letters separated by underscore:

example:

    public class Constants {
        public static final double PI_VALUE = 3.14159;
        public static final int MAX_SIZE = 100;
    }

4 - Package names should be in lowercase letters and follow the class naming convention.

example:

    package com.myapp.util;

    import com.myapp.util.MyClass;
    import com.myapp.util.MyOtherClass;

    public class MyUtilClass {
        // class implementation
    }

5 - Methods that return a boolean value should start with "is" or "has".

example:

    public class Person {
        private boolean isActive;
    
    public boolean isActive() {
        return isActive;
        }
    
    public boolean hasPermission() {
        // implementation
        }
    }

6 - Enumeration (enum) names should be written in uppercase letters separated by underscore.

example:

    public enum DayOfWeek {
        MONDAY,
        TUESDAY,
        WEDNESDAY,
        THURSDAY,
        FRIDAY,
        SATURDAY,
        SUNDAY
    }

7 - Method parameter names should follow the variable naming convention.

example:

    public class MyClass {
        public double calculateAverage(double[] grades) {
            // implementation
        }
    }

## Patterns for variables

1 - a final variable can never be changed and must be written in uppercase:

example:

    final String BR = "Brasil";

2 - A valid variable declaration must start with a letter, underscore, or dollar sign, and can be followed by any combination of letters, numbers, underscores, or dollar signs.

example: 
Valid variable declarations:

    int myVariable;
    double myDouble;
    String myString;
    boolean isActive;
    char firstLetter;
    float $myFloat;

Invalid variable declarations:

    int 123myVariable; // starts with a number
    double my-Double; // contains a dash
    String my string; // contains a space
    boolean is active; // contains a space
    char first letter; // contains a space
    float my$Float$; // contains consecutive dollar signs
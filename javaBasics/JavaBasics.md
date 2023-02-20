# Java Basics

## Class name:

The class name should start with a capital letter and use camelCase.

Example:

public class MyClass {
	}

## Main:
The main class is the entry point of the program. The main class contains the main method

public static void main(String[] args)

The main method takes a parameter args (which is an array of strings) that can be used to pass command-line arguments to the program.

## Naming Convention in JAVA
The naming conventions are a set of rule used to name clases, methods, variable and other elements in Java.

1 - Class names shoud start with an uppercase and use CamelCase.

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

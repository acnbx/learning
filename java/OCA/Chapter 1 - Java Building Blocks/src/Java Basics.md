# Understanding the Java Class Structure

In Java a *class* is the basic building block.
When defining a class you must describe all the *methods* (operations it can perform) and *fields* (pieces of information it can hold) it has.
To use a class we typically must create an *instance* of it in memory.
All the various objects of the classes represent the *state* of the program.


## Fields and Methods

Java classes have two primary elements:
    
- methods; An operation that an be called; Also called functions or procedures.
- fields; Information that is held in memory; Also called a variable.

In combination these *methods* and *fields* are known as the *members* of the class.

Here is an example of a very simple class with a couple of methods;

    public class Animal {
        String name;

        // This is a public method meaning it can be called by other classes not just internally.
        // It has a return type of String meaning when called it must return a String Object to the caller.
        public String getName() {
            return name;
        }

        // This method has a return type of void meaning it does not return anything to its caller.
        // It has a String parameter meaning the caller must provide a String argument. 
        public void setName(String newName) {
            name = newName;
        }
    }

The full declaration of a method is called a *method signature*, the declaration contains all the information on how to call the method and what to expect in return. 

## Classes vs. Files

Each Java class is typically defined in its own *.java file and is usually declared as public meaning it can be accessed by any other Java code.

Strictly speaking classes do not have to be declared as public and multiple classes can be declared in the same *.java file like so;

    public class Animal {
        String name;
    }

    class otherAnimal {
    }

#### Basic rules for classes:
1. Each file can contain only one *public* class.
2. The file m=name must match the class name, including case, and have the .java file extension. 

## The *main()* method

Every Java program needs an entrypoint - The gateway through which the Java Virtual Machine 

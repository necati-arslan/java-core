1

- ## compile code;
  javac com/neco/Main.java
- ## run bit code;
  src java com.neco.Main

## Primitive types

int myNum = 5; // Integer (whole number)
float myFloatNum = 5.99f; // Floating point number
char myLetter = 'D'; // Character
boolean myBool = true; // Boolean
String myText = "Hello"; // String

- A primitive type has always a value, while non-primitive types can be null.


## Shorthand Reassignment
- +=	x += 3	x = x + 3	
- -=	x -= 3	x = x - 3	
- *=	x *= 3	x = x * 3	
- /=	x /= 3	x = x / 3

## Concatenate Strings in Java
String result = str1 + str2;

## how to work string in java
```
char[] helloArray = { 'h', 'e', 'l', 'l', 'o', '.' };
String helloString = new String(helloArray);
System.out.println(helloString);
```
## How to work primitive and reference
<img src="/assets/stack.png" alt="memory stack">

## Array
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
int[] myNum = {10, 20, 30, 40};

```
- Primitives the default value for arrays is zero 
- for String array default value is 'nnull'

## Widening Casting
 ```
     int myInt = 9;

     double myDouble = myInt; // Automatic casting: int to double

```

## Ternary Operator

 ```
int time = 20;
String result = (time < 18) ? "Good day." : "Good evening.";
 ```

## Java For Each Loop
````
for (type variableName : arrayName) {
  // code block to be executed
}
````
## Java Break
```
for (int i = 0; i < 10; i++) {
      if (i == 4) {
        break;
      }
      System.out.println(i);
    }  
```
output= 0,1,2,3


## Multidimensional Arrays
```
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
System.out.println(myNumbers[1][2]); // Outputs 7
```

# Java Methods
## Create a Method

```
public class Main {
  static void myMethod() {
    // code to be executed
  }
    
 static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }
}

  static int myMethod(int x, int y) {
    return x + y;
  }
```
- **static** means that the method belongs to the Main class and not an object of the Main class.
- **void means** that this method does not have a return value. You will learn more about return values later in this chapter

## Java Block Scope
- A block of code refers to all of the code between curly braces {}.
```
public class Main {
  public static void main(String[] args) {

    // Code here CANNOT use x

    { // This is a block

      // Code here CANNOT use x

      int x = 100;

      // Code here CAN use x
      System.out.println(x);

    } // The block ends here

  // Code here CANNOT use x

  }
}

--------
    public static void main(String[] args) {
	// write your code here


        if (true){
            int x =10;
        }

        System.out.println(x); // cant use x heir

    }
```
## Java Recursion
- Recursion is the technique of making a function call itself. This technique provides a way to break complicated problems down into simple problems 

```
public class Main {
  public static void main(String[] args) {
    int result = sum(10);
    System.out.println(result);
  }
  public static int sum(int k) {
    if (k > 0) {
      return k + sum(k - 1);
    } else {
      return 0;
    }
  }
}
```

## What OOP?
- Object-Oriented Programming (OOP) is a programming approach that uses objects to structure and organize code. 
- Objects are instances of classes, which contain data and the methods that operate on that data
- OOP is based on the principles of encapsulation, inheritance, and polymorphism,

## Creating Object

```
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```

## Diffirece Static vs. Public
-  we created a static method, which means that it can be accessed without creating an object of the class, unlike public, which can only be accessed by objects:

```
public class Main {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }

  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // Call the static method
    // myPublicMethod(); This would compile an error

    Main myObj = new Main(); // Create an object of Main
    myObj.myPublicMethod(); // Call the public method on the object
  }
}
```

## Java Constructors
- A constructor in Java is a special method that is used to initialize objects.
-  It can be used to set initial values for object attributes:
  ```
// Create a Main class
public class Main {
  int x;

  // Create a class constructor for the Main class
  public Main() {
    x = 5;
  }

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}

```
- Note that the constructor name must match the class name, and it cannot have a return type (like void).
  
````
//filename: Main.java
public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}

---------

  public Main(int year, String name) {
    modelYear = year;
   String modelName = name;
  } // we get error 
````
# Java Modifiers
meaning that it is used to set the access level for classes, attributes, methods and constructors.

##Access Modifiers

- Public; The class is accessible by any other class	

- Private: The code is only accessible within the declared class	

## Non-Access Modifiers
- For classes, you can use either final or abstract:
- abstract;The class cannot be used to create objects

## Java Encapsulation
- meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users.

```
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```

# Java Packages

- To use a class or a package from the library, you need to use the import keyword:
  
```
import package.name.Class;   // Import a single class
import package.name.*;   // Import the whole package
---
import java.util.Scanner;
//In the example above, java.util is a package, while Scanner is a class of the java.util package.
  

```

# Java Inheritance

- subclass (child) - the class that inherits from another class
- superclass (parent) - the class being inherited from

```
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```
- Polymorfism

```
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```

## Enums

- An enum is a special "class" that represents a group of constants (unchangeable variables, like final variables).
  
```
public class Main {
  enum Level {
    LOW,
    MEDIUM,
    HIGH
  }

  public static void main(String[] args) {
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar);
  }
}
```

## Java Date and Time
- Java does not have a built-in Date class, but we can import the java.time package to work with the date and time API.
```
√import java.time.LocalDate; // import the LocalDate class
 
 public class Main {
   public static void main(String[] args) {
     LocalDate myObj = LocalDate.now(); // Create a date object
     System.out.println(myObj); // Display the current date
   }
 }
```

## Diffirence Array & ArrayList

- The difference between a built-in array and an ArrayList in Java, is that the size of an array cannot be modified 
```
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
  }
}
```

## Java Exceptions - Try...Catch
```
Example
public class Main {
  public static void main(String[ ] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    }
  }
}

```

## Java File Handlig

```aidl
import java.io.File;  // Import the File class

File myObj = new File("filename.txt"); // Specify the filename
```
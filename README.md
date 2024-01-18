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
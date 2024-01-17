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



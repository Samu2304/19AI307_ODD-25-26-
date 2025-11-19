# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To demonstrate accessing an inner class from an outer class in Java.

## ALGORITHM :
1.Create an outer class with a private variable.

2.Define an inner class inside it with a method to access the outer variable.

3.In main(), create an object of the outer class.

4.Use it to create an object of the inner class.

5.Call the inner class method.


## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();

        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```

## OUTPUT:

<img width="1223" height="347" alt="image" src="https://github.com/user-attachments/assets/15414c4a-4b5c-4828-96c2-b6dcdf6fbd9b" />

## RESULT:
The program successfully accesses and prints data from the inner class using the outer class.



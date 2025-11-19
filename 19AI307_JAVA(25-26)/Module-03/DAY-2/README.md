# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:

area(int side) for square

area(int length, int breadth) for rectangle

area(double radius) for circle


## AIM:
To calculate the area of different shapes (square, rectangle, circle) using method overloading in Java.
To demonstrate how multiple methods with the same name can perform different computations based on parameters.

## ALGORITHM :
1.Create a class AreaCalculator.

2.Define an area(int side) method to calculate and return the area of a square (side * side).

3.Define an area(int length, int breadth) method to calculate and return the area of a rectangle (length * breadth).

4.Define an area(double radius) method to calculate and return the area of a circle (Math.PI * radius * radius).

5.In the main method:

6.Create an instance of AreaCalculator.

7.Call area() for square, rectangle, and circle with appropriate arguments.

8.Print the calculated areas.	

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Samyuktha S 
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.*;
class AreaOf
{
    int area(int side)
    {
        return side*side;
    }
    int area(int length,int breadth)
    {
        return length*breadth;
    }
    double area(double radius)
    {
        return Math.PI*radius*radius;
    }
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        AreaOf a=new AreaOf();
        int side=sc.nextInt();
        System.out.printf("Area of square: %d\n",a.area(side));
        int len=sc.nextInt();
        int b=sc.nextInt();
        System.out.printf("Area of rectangle: %d\n",a.area(len,b));
        double radius=sc.nextDouble();
        System.out.println("Area of circle: "+a.area(radius));
    }
}
```

## OUTPUT:

<img width="840" height="382" alt="image" src="https://github.com/user-attachments/assets/c5d70c26-754c-4bcb-a3e7-9761a5eba9b9" />

## RESULT:
Thus, the Java program to calculate the area of square, rectangle, and circle using method overloading was successfully executed, and the output was verified to produce correct area values for each shape.

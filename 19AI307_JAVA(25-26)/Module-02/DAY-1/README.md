# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a Car class with attributes brand, model, and year, instantiate objects, and display their details.

## ALGORITHM :
1.Define a class Car with attributes brand, model, and year.

2.Create a constructor to initialize the attributes of the class.

3.Create a method displayDetails() to print the car details.

4.In the main method, create two Car objects with different attribute values.

5.Call displayDetails() for each object to print its information.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```

class Car
{
    String brand;
    String model;
    int year;
}








public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}

```

## OUTPUT:
<img width="632" height="167" alt="image" src="https://github.com/user-attachments/assets/14df8c2c-5063-496d-aecc-bec084d7fcb9" />

## RESULT:
Thus, the Java program to create a Car class, instantiate two objects, and display their details was successfully executed, and the output was verified to show correct car information.

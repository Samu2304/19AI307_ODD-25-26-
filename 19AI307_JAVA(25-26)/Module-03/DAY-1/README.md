# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Vehicle with fields brand (String) and speed (int). Create a subclass Car that inherits from Vehicle and adds a field fuelType (String).

Implement a method in Car called displayInfo() that prints the vehicle's brand, speed, and fuel type.

Write a program that:

Takes input for brand, speed, and fuel type using Scanner.

Creates a Car object.

Calls displayInfo() to print the details.

## AIM:
To demonstrate single inheritance in Java by creating a Vehicle superclass and a Car subclass, and to display vehicle details using a method in the subclass.
To understand how subclass inherits fields from a superclass and can extend functionality.

## ALGORITHM :
1.Create a superclass Vehicle with fields brand (String) and speed (int).

2.Create a subclass Car that extends Vehicle and adds a field fuelType (String).

3.In Car, define a method displayInfo() to print the brand, speed, and fuel type.

4.In the main method:

5.Use Scanner to read input values for brand, speed, and fuel type.

6.Create a Car object using the input values.

7.Call displayInfo() to print the car details.


## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;


class Vehicle {
    String brand;
    int speed;


    Vehicle(String brand, int speed) {
        this.brand = brand;
        this.speed = speed;
    }
}


class Car extends Vehicle {
    String fuelType;

   
    Car(String brand, int speed, String fuelType) {
        super(brand, speed);
        this.fuelType = fuelType;
    }

   
    void displayInfo() {
        System.out.println("Brand: " + brand);
        System.out.println("Speed: " + speed + " km/h");
        System.out.println("Fuel Type: " + fuelType);
    }
}


public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

    
       
        String brand = sc.nextLine();

        int speed = sc.nextInt();
        sc.nextLine(); 

        String fuelType = sc.nextLine();

     
        Car car = new Car(brand, speed, fuelType);

     
        car.displayInfo();

    }
}

```

## OUTPUT:

<img width="642" height="361" alt="image" src="https://github.com/user-attachments/assets/fa58f2af-1486-4696-8dc7-59bcfbe7d696" />

## RESULT:
Thus, the Java program to demonstrate inheritance by creating a Vehicle superclass and Car subclass was successfully executed, and the output verified the correct display of brand, speed, and fuel type.

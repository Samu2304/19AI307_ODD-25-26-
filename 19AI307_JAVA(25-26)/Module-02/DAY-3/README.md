# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To create a Smartphone class with private attributes brand, model, and storageCapacity, and to modify and display these values using getter, setter, and a custom method increaseStorage().
To demonstrate encapsulation and controlled access to class properties in Java.

## ALGORITHM :
1.Create a class Smartphone with private instance variables: brand, model, and storageCapacity.

2.Provide public getter and setter methods for each variable to access and modify their values.

3.Implement a method increaseStorage(int value) to increment storageCapacity by the given value.

4.Implement a display() method to print the smartphone details.

5.In the main method, read brand, model, storageCapacity, and extra storage to add from the user.

6.Set the values using setters and call increaseStorage() to update the storage.

7.Display the updated smartphone details using the display() method.	

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Smartphone phone = new Smartphone();

  
        phone.setBrand(sc.nextLine());
        phone.setModel(sc.nextLine());
        phone.setStorageCapacity(sc.nextInt());
        int extra = sc.nextInt();

  
        phone.increaseStorage(extra);
        phone.display();

        phone.setStorageCapacity(phone.getStorageCapacity() - extra); 
        

        sc.close();
    }
}

```

## OUTPUT:
<img width="920" height="453" alt="image" src="https://github.com/user-attachments/assets/24e4b651-1288-45de-9937-f3924139f7be" />

## RESULT:
Thus, the Java program to create a Smartphone class, modify its attributes, increase storage, and display the updated details was successfully executed, and the output was verified to reflect the correct updated storage capacity.

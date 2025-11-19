# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To calculate and display the average of all elements in an array using Java.
To demonstrate array handling and basic arithmetic operations in Java.

## ALGORITHM :
1.Read the size of the array n from the user.

2.Create an array of size n.

3.Read n elements from the user and store them in the array.

4.Initialize a variable sum to 0.

5.Use a loop to traverse the array and add each element to sum.

6.Calculate the average as sum / n.

7.Print the average.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ArrayAverage {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        int sum = 0;

        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }

        double average = (double) sum / n;
        System.out.println("Average of array elements: " + average);

        sc.close();
    }
}
```

## OUTPUT:
<img width="771" height="466" alt="image" src="https://github.com/user-attachments/assets/bb0ae6fa-a67e-4fe3-9c7a-2c6f75dac1a9" />

## RESULT:
Thus, the Java program to calculate the average of array elements was successfully executed, and the output was verified to produce the correct average value.





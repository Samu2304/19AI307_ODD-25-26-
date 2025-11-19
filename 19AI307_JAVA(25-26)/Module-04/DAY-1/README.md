# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program that divides two integers input by the user and handles division by zero using exception handling.
To demonstrate the use of try-catch blocks for runtime error prevention.

## ALGORITHM :
1.Import the Scanner class for user input.

2.Read two integers, num1 and num2, from the user.

3.Use a try block to perform the division num1 / num2.

4.Catch the ArithmeticException to handle the case where num2 is zero.

5.If no exception occurs, print the result of the division.

6.If an exception occurs, print a user-friendly message like "Cannot divide by zero".

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Samyuktha S 
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        try {
            int result = a / b;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }

        sc.close();
    }
}

```


## OUTPUT:
<img width="668" height="302" alt="image" src="https://github.com/user-attachments/assets/889a0d52-6e13-4049-be57-aa3e7aa28580" />

## RESULT:
Thus, the Java program to divide two integers with proper handling of division by zero using exception handling was successfully executed, and the output was verified to correctly handle both valid and invalid inputs.

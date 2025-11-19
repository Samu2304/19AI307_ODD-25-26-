# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To calculate and display the factorial of a given positive integer using a for loop in Java.
To demonstrate iterative computation and use of loops in solving mathematical problems.

## ALGORITHM :
1.Read an integer n from the user.

2.Initialize a variable factorial to 1.

3.Use a for loop from 1 to n (inclusive).

4.Multiply factorial by the loop counter in each iteration.

5.After the loop ends, print the value of factorial.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int fact=1;
        for(int i=1;i<=n;i++)
        {
            fact*=i;
        }
        System.out.printf("Factorial of %d is: %d",n,fact);
    }
}
```

## OUTPUT:
<img width="676" height="242" alt="image" src="https://github.com/user-attachments/assets/4e854ae5-5a17-491f-a944-d1a8e449a934" />

## RESULT:
Thus, the Java program to calculate the factorial of a number using a for loop was successfully executed, and the factorial output was verified for correctness.

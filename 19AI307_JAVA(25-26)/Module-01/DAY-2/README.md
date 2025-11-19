# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it skips that floor.

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number.

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:
To simulate an elevator that announces different messages based on the floor number using conditional logic in Java.
To demonstrate the use of if-else statements for multiple conditions.

## ALGORITHM :
1.Read the floor number as input from the user.

2.Check if the floor number is divisible by both 3 and 5.

3.If yes, print “Skipping floor!”

4.Else, check if the floor number is divisible by 3 only.

5.If yes, print “Beware!”

6.Else, check if the floor number is divisible by 5 only.

7.If yes, print “Blessings!”

8.Otherwise, print the floor number itself.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        if(a%3==0 && a%5==0)
        {
            System.out.println("Skipped");
        }
        else if(a%3==0)
        {
            System.out.println("Beware!");
        }
        else if(a%5==0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.printf("Floor %d",a);
        }
    }
}
```

## OUTPUT:
<img width="473" height="292" alt="image" src="https://github.com/user-attachments/assets/1a7c1bd8-4d28-4a3d-aafd-1ff2e2e7e442" />

## RESULT:
Thus, the Java program to simulate a magical elevator that announces messages based on floor numbers was successfully executed, and all conditional outputs were verified correctly.

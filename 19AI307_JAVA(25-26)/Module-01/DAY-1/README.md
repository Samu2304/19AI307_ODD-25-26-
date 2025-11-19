# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has just started learning Java and is very excited about how to display messages on the screen. Her first mission is to understand how different types of print statements work:

System.out.print() → prints on the same line

System.out.println() → prints and moves to the next line

System.out.printf() → prints formatted output

Your task is to help Lovely write a program that:

Takes her name, age, and her favorite decimal number.

Prints a greeting message using print().

Prints her age using println().

Prints her favorite number using printf() with 2 decimal places.

Input Format
First line: String → Lovely's name (no spaces)

Second line: int → Lovely's age

Third line: float → Lovely's favorite decimal number

Output Format
All outputs should demonstrate different printing styles:

Use System.out.print() for greeting

Use System.out.println() for age

Use System.out.printf() for decimal number with 2 digits after the decimal point

## AIM:
To demonstrate the use of different Java print statements (print, println, printf) by displaying a greeting, age, and a formatted decimal number.
To help beginners understand how output formatting works in Java.

## ALGORITHM :
1.Read the user’s name as a String.

2.Read the user’s age as an int.

3.Read the user’s favorite decimal number as a float.

4.Use System.out.print() to display a greeting message with the name on the same line.

5.Use System.out.println() to display the age, moving to the next line.

6.Use System.out.printf() to display the favorite number formatted to 2 decimal places.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## Sourcecode.java:
```
import java.util.*;
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String s=sc.nextLine();
        int a=sc.nextInt();
        float b=sc.nextFloat();
        System.out.println("Hello, "+s);
        System.out.println("You are " +a+ " years old");
        System.out.printf("Your favorite number is %.2f",b);
    }
}
```

## OUTPUT:
<img width="735" height="372" alt="image" src="https://github.com/user-attachments/assets/ca4dd429-8007-48e5-a4a8-ceeeae7e250d" />

## RESULT:
Thus, the Java program demonstrating print(), println(), and printf() with user inputs executed successfully and produced the expected output.



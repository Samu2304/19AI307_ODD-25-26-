# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To calculate the cube of a given integer using a helper method square() in Java.
To demonstrate method calling and code reusability in Java.

## ALGORITHM :
1.Define a method square(int x) that returns x * x.

2.Define a method cube(int x) that calls square(x) and multiplies the result by x.

3.In the main method, read an integer input from the user.

4.Call the cube() method with the input value.

5.Display the cube of the number.


## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.*;
class mathops
{
    int square(int a)
    {
        return a*a;
    }
    int cube(int a)
    {
        return square(a)*a;
    }
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        mathops m=new mathops();
        int res=m.cube(a);
        System.out.println(res);
    }
}
```
## OUTPUT:
<img width="347" height="162" alt="image" src="https://github.com/user-attachments/assets/02a02856-4a73-4a94-a782-699be9e4d44f" />

## RESULT:
Thus, the Java program to calculate the cube of a number by internally calling a square method was successfully executed, and the output was verified to produce the correct cube value.

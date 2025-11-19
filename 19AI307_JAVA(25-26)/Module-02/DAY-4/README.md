# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

## AIM:
To demonstrate accessing a static variable in Java using both the class name and an object.
To understand how static variables are shared among all instances of a class.

## ALGORITHM :
1.Create a class name with a static variable n1.

2.In the main method, read an integer input from the user.

3.Assign the input value to n1 using the class name: name.n1 = value.

4.Print the value of n1 using the class name.

5.Create an object of the class name.

6.Print the value of n1 using the object reference.

7.Observe that the value is the same, demonstrating that static variables are shared across instances.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089  
*/
```

## SOURCE CODE:
```
import java.util.*;
class name
{
    static int n1;
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        name.n1=sc.nextInt();
        System.out.println("Accessing using class name: "+name.n1);
        name n=new name();
        System.out.println("Accessing using object: "+n.n1);
    }
}
```

## OUTPUT:
<img width="740" height="302" alt="image" src="https://github.com/user-attachments/assets/76ac00f3-548c-4131-a966-816e03f27c47" />

## RESULT:
Thus, the Java program to access a static variable using both the class name and an object was successfully executed, and the output verified that the static variable is shared across instances.

# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To reverse a given string in Java and display the reversed output.
To demonstrate string manipulation and basic loop usage in Java.

## ALGORITHM :
1.Read a string input from the user.

2.Initialize an empty string reversed.

3.Loop through the original string from the last character to the first.

4.In each iteration, append the current character to reversed.

5.After the loop ends, print the reversed string.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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
        String s=sc.nextLine();
        char[] arr=s.toCharArray();
        int left=0;
        int right=arr.length-1;
        while(left<right)
        {
            char temp=arr[left];
            arr[left]=arr[right];
            arr[right]=temp;
            left++;
            right--;
        }
        String rev=new String(arr);
        System.out.println("Reversed string: "+rev);
        
    }
}
```

## OUTPUT:
<img width="697" height="242" alt="image" src="https://github.com/user-attachments/assets/9b0626a0-4da0-488d-846a-ed25ee79e85d" />

## RESULT:
Thus, the Java program to reverse a given string was successfully executed, and the output was verified to correctly display the reversed string.

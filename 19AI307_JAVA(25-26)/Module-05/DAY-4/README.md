# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:
To write a Java program that reads a thread name from the user, sets it for the current thread, and displays the thread’s name and priority.

## ALGORITHM :
1.Import java.util.Scanner to read input from the user.

2.Read the thread name from the user.

3.Get a reference to the current thread using Thread.currentThread().

4.Set the thread’s name using setName(threadName).

5.Get the thread’s priority using getPriority().

6.Print the thread name, priority, and thread details using System.out.println().

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String newName = sc.nextLine();

        Thread t = Thread.currentThread();

        t.setName(newName);

      
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t.toString());
    }
}

```

## OUTPUT:

<img width="688" height="208" alt="image" src="https://github.com/user-attachments/assets/1c5cc26d-5f6f-4ce0-a949-14ae4fb5753a" />

## RESULT:
Thus, the Java program successfully determined and displayed the name and priority of the current thread as per the user input.

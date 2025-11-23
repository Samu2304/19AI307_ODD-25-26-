# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.

 Input:

Two lines: <threadName>, <priority>

 Output:

Thread <threadName> priority set to <priority>

## AIM:
To write a Java program that reads a thread name and priority from the user, creates a new thread, sets its name and priority, and displays the values.

## ALGORITHM :
1.Import java.util.Scanner to read input.

2.Read the thread name from the user.

3.Read the thread priority (integer from 1 to 10) from the user.

4.Create a new Thread object.

5.Set the thread’s name using setName(threadName).

6.Set the thread’s priority using setPriority(priority).

7.Print the thread name and priority in the required format.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
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

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread(threadName) {
            public void run() {
              
            }
        };

        t.setPriority(priority);

        System.out.println("Thread " + threadName + " priority is " + priority);
    }
}
```
## OUTPUT:

<img width="745" height="307" alt="image" src="https://github.com/user-attachments/assets/58e5fbad-1e14-463e-8e06-a76b1d8208a2" />

## RESULT:
Thus, the Java program successfully created a new thread, set its name and priority based on user input, and displayed the thread details.

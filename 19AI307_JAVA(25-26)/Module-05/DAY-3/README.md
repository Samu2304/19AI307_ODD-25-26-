# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to overwrite the content of a file.

## AIM:
To write a Java program that overwrites the content of a file with new data, demonstrating the use of FileWriter in overwrite mode.

## ALGORITHM :
1.Import the required java.io.* classes.

2.Create a FileWriter object for the target file. By default, FileWriter overwrites the existing file content.

3.Read new content from the user.

4.Write the new content to the file using write().

5.Close the FileWriter to save changes.

6.Print a message confirming that the file content has been successfully overwritten.

7.Handle exceptions using a try-catch block.	

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089  
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String content = sc.nextLine();

        String fileName = "output.txt";

        try {
            FileWriter writer = new FileWriter(fileName, false); 
            writer.write(content);
            writer.close();

            System.out.println("File content overwritten successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}

```

## OUTPUT:

<img width="1102" height="201" alt="image" src="https://github.com/user-attachments/assets/42a5e0f8-b9ac-451f-a6aa-4c440f638e24" />

## RESULT:
Thus, the Java program to overwrite the content of a file was successfully executed, and the new data replaced the previous content in the file.

# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program that uses FileWriter to write characters into a text file and confirm successful file writing.

## ALGORITHM :
1.Import the required java.io.* package.

2.Create a FileWriter object and pass the filename as a parameter.

3.Read a string input from the user.

4.Use the write() method of FileWriter to write the input into the file.

5.Close the FileWriter to save and release resources.

6.Print a message confirming successful writing.

7.Handle exceptions using try–catch.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by:Samyuktha S 
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:

```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteCharactersToFile {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String fileName = sc.nextLine();
        String content = sc.nextLine();

        try (FileWriter writer = new FileWriter(fileName)) {
            
            writer.write(content);
            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="711" height="302" alt="image" src="https://github.com/user-attachments/assets/6ca8a699-bff6-4b51-b3be-adb4b1452cd4" />

## RESULT:
Thus, the Java program to write characters to a file using FileWriter was successfully executed, and the output was verified.

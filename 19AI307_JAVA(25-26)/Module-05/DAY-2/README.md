# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.

## AIM:
To develop a Java program that reads multiple UTF strings from the user, writes them into a ByteArrayOutputStream using DataOutputStream, and displays the resulting byte array content.

## ALGORITHM :
1.Import the required java.io.* classes.

2.Create a ByteArrayOutputStream object to hold the data in memory.

3.Wrap it inside a DataOutputStream to write UTF strings.

4.Read the number of strings from the user.

5.Loop through the input and write each string using writeUTF().

6.Convert the ByteArrayOutputStream content into a byte array.

7.Print the byte array elements.

8.Close the streams.

9.Handle exceptions using try–catch.	

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089  
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            // Create ByteArrayOutputStream to store data in memory
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);

            // Get number of strings from user
            int n = scanner.nextInt();
            scanner.nextLine(); // Consume newline

            // Read strings from user and write them in UTF format
            for (int i = 0; i < n; i++) {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }

            // Convert to byte array
            byte[] byteData = baos.toByteArray();

            // Display byte array contents
            System.out.println("Byte array contents:");
            for (byte b : byteData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);

            // Read strings back from memory
            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);

            System.out.println("\nStrings read from memory:");
            for (int i = 0; i < n; i++) {
                String str = dis.readUTF();
                System.out.println(str);
            }

            // Close streams
            dos.close();
            dis.close();
            scanner.close();

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

## OUTPUT:

<img width="1172" height="700" alt="image" src="https://github.com/user-attachments/assets/88a03971-682f-452e-b792-b49280e7a82f" />

## RESULT:
Thus, the Java program to read multiple UTF strings, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents was successfully executed and verified.

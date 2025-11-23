# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A Department contains Professor objects, but professors can exist independently.
If no inputs gets passed, print "No professors assigned."

For example:

Input	Result
2
Dr. Hariharan
Dr. Saveetha
Department: Computer Science
- Dr. Hariharan
- Dr. Saveetha

## AIM:
To create a Java program demonstrating aggregation, where a Department contains multiple Professor objects that can exist independently, and display the list of assigned professors or show a message when none are provided.

## ALGORITHM :
1.Create a Professor class with a field for name.

2.Create a Department class that contains:

3.A department name

4.An array/list of Professor objects

5.A method to display all assigned professors

6.In the main method:

Read the number of professors.

If the number is zero, print "No professors assigned."

Otherwise, read professor names and store them in an array.

Create a Department object with professors.

7.Display department name and list of professors.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class DepartmentAssociation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();  
        sc.nextLine();

        Department dept = new Department("Computer Science");

        for (int i = 0; i < n; i++) {
            String profName = sc.nextLine();
            Professor prof = new Professor(profName);
            dept.addProfessor(prof);
        }

        dept.showProfessors();
        sc.close();
    }
}

class Professor {
    private String name;

    public Professor(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

class Department {
    private String name;
    private List<Professor> professors;

    public Department(String name) {
        this.name = name;
        this.professors = new ArrayList<>();
    }

    public void addProfessor(Professor prof) {
        professors.add(prof);
    }

    public void showProfessors() {
        System.out.println("Department: " + name);
        if (professors.isEmpty()) {
            System.out.println("No professors assigned.");
        } else {
            for (Professor p : professors) {
                System.out.println("- " + p.getName());
            }
        }
    }
}
```
## OUTPUT:
<img width="838" height="215" alt="image" src="https://github.com/user-attachments/assets/f32fd5c0-a0d4-4ae5-a957-b5bc14883ef3" />

## RESULT:
Thus, the Java program demonstrating aggregation between Department and Professor was successfully executed, and the output was verified.

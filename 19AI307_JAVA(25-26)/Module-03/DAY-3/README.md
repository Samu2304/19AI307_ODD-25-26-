# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class Employee with method calculatePay(). Extend it to HourlyEmployee and SalariedEmployee.

Input Format:

- The first line contains an integer:
    1 → for HourlyEmployee  
    2 → for SalariedEmployee

- If input is 1 (HourlyEmployee):
    The second line contains two values:
    - hours worked (integer)
    - rate per hour (double)

- If input is 2 (SalariedEmployee):
    The second line contains one value:
    - monthly salary (double)

Output Format:

- A single line containing the calculated pay formatted to two decimal places.

## AIM:
To create an abstract class Employee with a method calculatePay() and extend it to HourlyEmployee and SalariedEmployee to calculate and display pay.
To demonstrate abstraction and method overriding in Java.

## ALGORITHM :
1.Create an abstract class Employee with an abstract method calculatePay().

2.Create a subclass HourlyEmployee that stores hoursWorked and ratePerHour.

3.Override calculatePay() to return hoursWorked * ratePerHour.

4.Create a subclass SalariedEmployee that stores monthlySalary.

5.Override calculatePay() to return monthlySalary.

6.In the main method:

7.Read the employee type (1 for HourlyEmployee, 2 for SalariedEmployee).

8.Read the corresponding input values.

9.Create an object of the appropriate subclass.

10.Call calculatePay() and print the pay formatted to two decimal places.


## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Samyuktha S
RegisterNumber: 21222220089  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

abstract class Employee {
    abstract double calculatePay();
}

class HourlyEmployee extends Employee {
    private int hoursWorked;
    private double ratePerHour;

    HourlyEmployee(int hoursWorked, double ratePerHour) {
        this.hoursWorked = hoursWorked;
        this.ratePerHour = ratePerHour;
    }

    @Override
    double calculatePay() {
        return hoursWorked * ratePerHour;
    }
}

class SalariedEmployee extends Employee {
    private double monthlySalary;

    SalariedEmployee(double monthlySalary) {
        this.monthlySalary = monthlySalary;
    }

    @Override
    double calculatePay() {
        return monthlySalary;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();

        Employee emp;

        if (choice == 1) { 
            int hours = sc.nextInt();
            double rate = sc.nextDouble();
            emp = new HourlyEmployee(hours, rate);
        } else if (choice == 2) { 
            double salary = sc.nextDouble();
            emp = new SalariedEmployee(salary);
        } else {
            System.out.println("Invalid input");
            sc.close();
            return;
        }

        double pay = emp.calculatePay();

        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println(df.format(pay));

        sc.close();
    }
}

```

## OUTPUT:

<img width="361" height="258" alt="image" src="https://github.com/user-attachments/assets/29a64df6-aaa4-4196-8edb-3444abb4cce6" />

## RESULT:
Thus, the Java program to calculate pay using an abstract Employee class and its subclasses HourlyEmployee and SalariedEmployee was successfully executed, and the output was verified to correctly display the calculated pay.

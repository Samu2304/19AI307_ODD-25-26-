# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class SpeedLimit with a final method displayLimit() that prints "Max Speed: 80 km/h". Try to override it in a subclass. Show that overriding a final method is not allowed.

## AIM:
To create a SpeedLimit class with a final method displayLimit() and demonstrate that overriding a final method in a subclass is not allowed.
To understand the use of final keyword to prevent method overriding in Java.

## ALGORITHM :

1.Create a class SpeedLimit with a final method displayLimit() that prints the maximum speed.

2.Create a subclass Car that attempts to override the displayLimit() method.

3.Observe that the Java compiler throws an error because final methods cannot be overridden.

4.Optionally, create an object of SpeedLimit and call displayLimit() to show it works normally.


## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Samyuktha S 
RegisterNumber: 212222240089  
*/
```

## SOURCE CODE:
```
class SpeedLimit
{
    final void displayLimit()
    {
        System.out.println("Max Speed: 80 km/h");
    }
}
class HighwaySpeed extends SpeedLimit
{
}
public class main
{
    public static void main(String[] args)
    {
        HighwaySpeed s=new HighwaySpeed();
        s.displayLimit();
    }
}
```
## OUTPUT:
<img width="453" height="165" alt="image" src="https://github.com/user-attachments/assets/70bbc068-e371-4a1f-99c0-c4fdd33b2db9" />

## RESULT:
Thus, the Java program successfully demonstrated that a final method cannot be overridden, and the output verified the correct behavior of the final method.

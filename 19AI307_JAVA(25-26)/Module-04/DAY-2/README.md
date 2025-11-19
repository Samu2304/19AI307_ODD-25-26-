# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

Input Format:

n
[Player1]
[Player2]
...
First line: Integer n – number of players turning on consoles

Next n lines: Each line contains the player's name.

 

Output Format:
For each player, print:

[PlayerName] accessed Master Power Switch. Total accesses so far: [count]

 

## AIM:
To implement a singleton class MasterPowerSwitch that ensures only one instance exists, logs each access, and maintains a global access count for all players in a gaming lounge.

## ALGORITHM :
1.Create a class MasterPowerSwitch with:

2.A private static instance variable to store the single instance.

3.A private constructor to prevent external instantiation.

4.An accessCount variable to track total accesses.

5.A public static method getInstance() to provide the single instance.

6.A method logAccess() that increments and returns the access count.

7.In the main method:

Read the number of players n.

For each player, read their name.

Get the singleton instance of MasterPowerSwitch.

8.Call logAccess() and print the player name along with the current access count.


## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Samyuktha S 
RegisterNumber: 212222240089  
*/
```

## SOURCE CODE:
```
import java.util.*;

class MasterPowerSwitch {
    // Single instance
    private static MasterPowerSwitch instance;

    // Access count
    private int accessCount;

    // Private constructor to prevent instantiation
    private MasterPowerSwitch() {
        accessCount = 0;
    }

    // Method to get the single instance
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    // Log access and return current count
    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }

        sc.close();
    }
}

```

## OUTPUT:
<img width="1072" height="240" alt="image" src="https://github.com/user-attachments/assets/3608cdb4-db01-413b-8017-d8630276d574" />

## RESULT:
Thus, the Java program successfully implemented a singleton MasterPowerSwitch, ensuring a single instance while logging and displaying the cumulative access count for each player.

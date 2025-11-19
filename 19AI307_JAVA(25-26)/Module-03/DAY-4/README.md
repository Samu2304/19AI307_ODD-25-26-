# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

## AIM:
To implement a common interface for weather bots and generate temperature predictions using different bot types (SunBot and RainBot).
To demonstrate interface implementation and polymorphism in Java.

## ALGORITHM :
1.Define an interface WeatherBot with a method predict(int temperature) that returns a String.

2.Implement SunBot class:

3.If temperature > 30, return "HOT".

4.Else, return "MODERATE".

5.Implement RainBot class:

6.If temperature < 20, return "COLD".

7.Else, return "WARM".

8.In the main method:

9.Read the temperature and bot type (1 for SunBot, 2 for RainBot) from the user.

10.Create an instance of the selected bot type.

11.Call predict() and print the prediction.	

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Samyuktha S 
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        return (temperature > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        return (temperature < 20) ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;
        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
    }
}

```

## OUTPUT:

<img width="358" height="161" alt="image" src="https://github.com/user-attachments/assets/3b40fce9-f000-4a4e-91f9-720a5fed9348" />

## RESULT:
Thus, the Java program to implement weather prediction bots using an interface was successfully executed, and the output verified the correct prediction based on temperature and bot type.

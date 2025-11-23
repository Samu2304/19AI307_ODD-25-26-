# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement the Abstract Factory design pattern in Java that generates UI components (Button and Checkbox) for different themes (Dark and Light) based on user input, and display the created component types.

## ALGORITHM :
1.Create interfaces:

-Button with a method createButton()

-Checkbox with a method createCheckbox()

-UIFactory with methods to create both components.

2.Implement DarkButton, LightButton, DarkCheckbox, LightCheckbox.

3.Create DarkFactory and LightFactory implementing UIFactory.

4.In the main method:

-Read user input ("dark" or "light").

-Based on input, choose the correct factory.

-Create Button and Checkbox using the selected factory.

-Display the created component types.

5.If input is invalid, print an error message.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button {
    void create();
}

interface Checkbox {
    void create();
}

class DarkButton implements Button {
    public void create() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void create() {
        System.out.println("Dark Checkbox created");
    }
}

class LightButton implements Button {
    public void create() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void create() {
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkUIFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightUIFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

class UIFactoryProvider {
    public static UIFactory getFactory(String theme) {
        if (theme.equalsIgnoreCase("dark")) return new DarkUIFactory();
        if (theme.equalsIgnoreCase("light")) return new LightUIFactory();
        return null;
    }
}

public class UIClient {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine();

        UIFactory factory = UIFactoryProvider.getFactory(theme);

        if (factory != null) {
            Button btn = factory.createButton();
            Checkbox chk = factory.createCheckbox();
            btn.create();
            chk.create();
        } else {
            System.out.println("Invalid theme");
        }

        sc.close();
    }
}

```

## OUTPUT:
<img width="628" height="297" alt="image" src="https://github.com/user-attachments/assets/0b47440d-e3ae-4f9b-b144-61f603d6471d" />

## RESULT:
Thus, the Java program using the Abstract Factory pattern to generate theme-specific UI components (Button & Checkbox) based on user choice was successfully executed, and the output was verified.


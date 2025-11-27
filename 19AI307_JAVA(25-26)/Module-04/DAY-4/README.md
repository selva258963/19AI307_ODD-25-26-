
# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types
<img width="357" height="123" alt="image" src="https://github.com/user-attachments/assets/ee651ca7-9034-4186-8aa2-296b64d2a5d6" />



## AIM:
To implement the Abstract Factory Design Pattern in Java by creating themed UI components using different factories based on user input.

## ALGORITHM :
1.Start the program and read the theme input from the user.

2.Based on the theme, create the corresponding factory object (DarkThemeFactory or LightThemeFactory).

3.Use the selected factory to create a Button and a Checkbox object.

4.Call the render() method on both objects to display their theme-specific outputs.

5.End the program.



## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151
*/
```

## SOURCE CODE:
```java
import java.util.*;

interface Button {
    void render();
}

interface Checkbox {
    void render();
}

// Concrete Products for Dark Theme
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

// Concrete Products for Light Theme
class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

// Abstract Factory
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Concrete Factories
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

// Main class
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim().toLowerCase();

        UIFactory factory = null;

        if (theme.equals("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equals("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            sc.close();
            return;
        }

        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();

        button.render();
        checkbox.render();

        sc.close();
    }
}
```



## OUTPUT:
<img width="1305" height="426" alt="image" src="https://github.com/user-attachments/assets/6d667a53-9338-49e0-8c27-fc049974b791" />



## RESULT:
The program successfully implemented the Abstract Factory design pattern in Java, creating UI components based on selected theme using appropriate factory classes.


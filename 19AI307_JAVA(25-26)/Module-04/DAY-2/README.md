# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state

<img width="657" height="227" alt="image" src="https://github.com/user-attachments/assets/e68dc29f-d6ea-4ee1-952a-dec4f0b52d6b" />



## AIM:
To implement SOLID principles in Java using the Singleton Design Pattern by ensuring only one instance of the master power switch exists and maintains a shared access count.


## ALGORITHM :
1.Start the program.

2.Import the necessary package java.util.

3.Create a class MasterPowerSwitch with:

- A private static instance.

- A private constructor (restricts object creation).

- A static method getInstance() to return the single instance.

4.Maintain a counter accessCount to log switch usage.

5.In the main class, read number of players.

6.For each player, call getInstance() to get the same object and update count.

7.Display output for each player.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151  
*/
```

## SOURCE CODE:
```java
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance = null; // single instance
    private int accessCount = 0; // shared counter

    // private constructor → prevents outside object creation
    private MasterPowerSwitch() {}

    // static method to return the single instance
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    // method to increment and return access count
    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}
```




## OUTPUT:
<img width="1322" height="406" alt="image" src="https://github.com/user-attachments/assets/c4532c8c-8366-4367-ba12-eb2426b25ee0" />


## RESULT:
The program successfully demonstrated SOLID principles by implementing the Singleton design pattern, ensuring only one instance of the master power switch exists, while maintaining a common access count across all users.

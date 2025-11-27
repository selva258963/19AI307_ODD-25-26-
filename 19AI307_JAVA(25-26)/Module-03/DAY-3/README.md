# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.
-  Input Format:
-  First line: 1 for SavingsAccount, 2 for FixedDepositAccount
- If 1: next line → balance (double)
- If 2: next line → amount (double) and years (int)
- Output Format:
- A single line showing interest earned rounded to 2 decimal places.
- For example:
<img width="161" height="207" alt="image" src="https://github.com/user-attachments/assets/c79ccbd0-6bbe-487c-807b-c1b6df8cbf1b" />


## AIM:
To write a Java program that demonstrates runtime polymorphism using an abstract class BankAccount and its subclasses to calculate interest for Savings and Fixed Deposit accounts.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the account type from the user.
4. If the user selects Savings, read balance and create a SavingsAccount object; otherwise, read amount and years to create a FixedDepositAccount object.
5. Store the object in the base class reference BankAccount.
6. Call the calculateInterest() method using runtime polymorphism.
7. Display the calculated interest.

## PROGRAM:
 ```
Program to implement a Abstraction using Java
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151
```

## SOURCE CODE:
```java
import java.util.*;
abstract class BankAccount {
    abstract double calculateInterest();
}

class SavingsAccount extends BankAccount {
    double balance;
    SavingsAccount(double balance) {
        this.balance = balance;
    }
    double calculateInterest() {
        return balance * 0.04;
    }
}

class FixedDepositAccount extends BankAccount {
    double amount;
    int years;
    FixedDepositAccount(double amount, int years) {
        this.amount = amount;
        this.years = years;
    }
    double calculateInterest() {
        return amount * 0.07 * years;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        BankAccount account;
        if (type == 1) {
            double balance = sc.nextDouble();
            account = new SavingsAccount(balance);
        } else {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            account = new FixedDepositAccount(amount, years);
        }
        System.out.printf("%.2f", account.calculateInterest());
    }
}
```


## OUTPUT:

<img width="410" height="373" alt="image" src="https://github.com/user-attachments/assets/967d446a-59be-4821-9d42-13a04bc22c25" />

## RESULT:
The program successfully demonstrates runtime polymorphism using an abstract class. Depending on the account type entered by the user, the appropriate calculateInterest() method from the corresponding subclass is executed, and the interest amount is correctly displayed.

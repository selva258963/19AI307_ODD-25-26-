# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.
<img width="331" height="116" alt="image" src="https://github.com/user-attachments/assets/ec78b3d1-8320-4e6a-96d5-3f0672a873fb" />

## AIM:
To write a Java program that checks whether a given number is an Armstrong number by summing each digit raised to the power of the total number of digits.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer input from the user.
4. Count the number of digits in the given number.
5. Extract each digit using modulus, raise it to the power of the digit count, and accumulate the sum.
6. Repeat the process until all digits are processed.
7. Compare the final sum with the original number and display whether it is an Armstrong number.


## PROGRAM:
 ```
Program to implement a Wrapper Class using Java
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151
```

## SOURCE CODE:
```
import java.util.*;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = Integer.parseInt(sc.nextLine());
        int digits = Integer.toString(num).length();
        int sum = 0, temp = num;

        while (temp > 0) {
            int d = temp % 10;
            sum += (int) Math.pow(d, digits);
            temp /= 10;
        }

        if (sum == num)
            System.out.println(num + " is an Armstrong number.");
        else
            System.out.println(num + " is not an Armstrong number.");
    }
}
```
## OUTPUT:
<img width="1249" height="262" alt="image" src="https://github.com/user-attachments/assets/9af1dcf2-99be-4cf1-a952-abe5ab50901c" />

## RESULT:
The program correctly reads a number, computes the sum of its digits raised to the required power, and successfully determines whether the given number is an Armstrong number or not.



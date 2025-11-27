# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.
<img width="518" height="133" alt="image" src="https://github.com/user-attachments/assets/c2652869-39ad-4d6e-9f7a-66caa98752da" />


## AIM:
To write a Java program that demonstrates variable scope by accessing a static variable using both class name and object reference.



## ALGORITHM :
1.Start the program.

2.Import the necessary package java.util.

3.Declare a static variable inside the class.

4.In the main method, get input from the user and store it in the static variable.

5.Access and print the static variable using the class name.

6.Create an object of the class.

7.Access and print the static variable using the object.

8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class prog
{ 
    static int val;
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        prog.val=input.nextInt();
        System.out.println("Accessing using class name: "+prog.val);
        prog obj=new prog();
        System.out.println("Accessing using object: "+obj.val);
    }
}
```




## OUTPUT:
<img width="1291" height="446" alt="image" src="https://github.com/user-attachments/assets/bd2d1ee0-6b4f-40c8-8118-a87ef5529822" />



## RESULT:
The program to demonstrate variable scope and access a static variable using both class name and object was successfully executed.

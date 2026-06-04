# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to swap two strings without using a third variable.

Input	Result
hello
world	
After swapping:
First string (A): world
Second string (B): hello


## AIM:
To swap two strings without using a third variable.

## ALGORITHM :
1. Start the program execution.
2. Read two strings A and B from the user.
3. Concatenate string B to string A and store the result in A.
4. Extract the original value of A from the concatenated string and assign it to B.
5. Extract the original value of B from the concatenated string and assign it to A.
6. Display the swapped values of strings A and B.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class swap{
    public static void main(String[] s){
        Scanner in = new Scanner(System.in);
        System.out.println("After swapping:");
        String s1 = in.nextLine();
        String s2 = in.nextLine();
        s1=s1+s2;
        s2 = s1.substring(0,(s1.length()-s2.length()));
        s1=s1.substring(s2.length());
        System.out.printf("First string (A): %s\n",s1);
        System.out.printf("Second string (B): %s",s2);
    }
}
```






## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-01/DAY-5/Screenshot%202026-06-04%20152341.png)


## RESULT:
The program successfully swaps the two strings without using a third variable and displays the swapped values.


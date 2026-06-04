# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
In mathematics, the factorial of a non-negative integer n, denoted as n!, is the product of all positive integers less than or equal to n. For example:

5! = 5 × 4 × 3 × 2 × 1 = 120

3! = 3 × 2 × 1 = 6

0! is defined as 1.

Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.

Use a for loop to perform the calculation.

Make sure to handle the case when the user enters 0.

Display the result in a clear and user-friendly way.

For example:

Input	Result
0
Factorial of 0 is: 1


## AIM:
To calculate and display the factorial of a given non-negative integer using a for loop.

## ALGORITHM :
1. Start the program execution.
2. Read the non-negative integer n from the user.
3. Initialize the variable fact with the value 1.
4. Execute a for loop from 1 to n and multiply fact by each loop value.
5. Keep fact as 1 when the entered value of n is 0.
6. Display the factorial of the given number to the user.
7. Stop the program execution.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class fact{
    public static void main(String args[]){
        Scanner in = new Scanner(System.in);
        int n =in.nextInt();
        int f=1;
        for(int i = n;i>=0;i--){
            if(i==0||i==1){
                f*=1;
            }
            else{
                f*=i;
            }
        }
        System.out.printf("Factorial of %d is: %d",n,f);
    }
}
```
## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-01/DAY-3/Screenshot%202026-06-04%20151018.png)

## RESULT:
The program successfully calculates and displays the factorial of the given non-negative integer using a for loop.

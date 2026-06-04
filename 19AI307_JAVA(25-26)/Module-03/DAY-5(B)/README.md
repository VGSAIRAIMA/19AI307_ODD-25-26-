# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

Input	Result
32
32
Sum = 64


## AIM:
To convert string inputs into integers and calculate their sum using wrapper class methods in Java.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary package for user input.
3. Read two numeric values as strings from the user.
4. Convert the string values into integers using the Integer.parseInt() method.
5. Add the converted integer values and store the result.
6. Display the calculated sum on the screen.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String a = sc.nextLine();
        String b = sc.nextLine();
        int ad = Integer.parseInt(a)+Integer.parseInt(b);
        System.out.println("Sum = "+ad);
    }
}
```


## OUTPUT:
![IMAGE](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-5(B)/Screenshot%202026-06-04%20171923.png)
## RESULT:
The program successfully converts the entered string values into integers and displays their sum.

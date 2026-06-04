# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is a treasure hunter and has reached the final chamber of the dungeon. To unlock the treasure chest, she must enter a secret 4-digit code.

A riddle appears on the wall:

"The code is hidden in the numbers you enter. Solve these puzzles to form it!"

The puzzle has 4 steps:

First digit = sum of the first two numbers

Second digit = difference between the third and fourth numbers

Third digit = product of the second and fourth numbers

Fourth digit = remainder when third number is divided by first number

Input Format:
Enter four numbers as input (integers):

<number1>
<number2>
<number3>
<number4>
Output Format:

The treasure code
The treasure code is: <digit1><digit2><digit3><digit4>

## AIM:
To read four integers and generate a treasure code using arithmetic operations such as addition, subtraction, multiplication, and modulus.

## ALGORITHM :

1. Start.
2. Read four integers `a`, `b`, `c`, and `d`.
3. Calculate `x = a + b`.
4. Calculate `y = c - d`.
5. Calculate `z = b * d`.
6. Calculate `w = c % a` and display `x`, `y`, `z`, and `w` as the treasure code.
7. Stop.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## Sourcecode.java:

```
import java.util.Scanner;
public class treasure{
    public static void main(String[] srgs){
        Scanner in = new Scanner(System.in);
        int a = in.nextInt();
        int b= in.nextInt();
        int c= in.nextInt();
        int d = in.nextInt();
        System.out.printf("The treasure code is: %d%d%d%d",a+b,c-d,b*d,c%a);
        
        
    }
}
```





## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-01/DAY-1/Screenshot%202026-06-04%20145823.png)


## RESULT:
The program successfully accepts four integer inputs, computes the treasure code (a+b, c-d, b*d, c%a), and displays it in the specified format.

# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
It was Christmas Eve, and the Cathedral Chapel was alive with celebrations commemorating the birth of Jesus. After the mass and feast, the Event Management Team organized a series of fun games, with enthusiastic participation from both kids and adults. One such game, called the "Chocolate Game," was specially arranged for the children.

In this game, a standard chocolate bar is divided into an n x m grid, forming a rectangular plate with n rows and m columns.

Two kids take turns playing the game. The first kid begins by making a single cut—either horizontal or vertical—dividing the chocolate into two parts. Next, the second kid chooses any one of the resulting pieces and makes a similar cut. The first kid then selects any one of the currently available chocolate pieces and repeats the process. This alternation continues. A player who cannot make a move on their turn loses the game.

Write a program that determines whether the first player will win the game if both kids play optimally.
Output "yes" if the first player can guarantee a win, otherwise output "no".

Input Format:
A single line containing two space-separated integers n and m — representing the size of the chocolate.

Output Format:
Print one word: "Yes" if the first player can force a win, or "No" otherwise.

## AIM:
To determine whether the first player can guarantee a win in the Chocolate Game by checking if the product of the chocolate dimensions (n × m) is even or odd.

## ALGORITHM :
```
Start.
Read two integers n and m.
Calculate p = n × m.
Check whether p is divisible by 2.
If p is even, print "yes".
Otherwise, print "no".
Stop.
```

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class eve{
    public static void main(String args[]){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int m = in.nextInt();
        if((n*m)%2==0){
            System.out.print("yes");
        }
        else{
            System.out.print("no");
        }
        
    }
}

```

## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-01/DAY-2/Screenshot%202026-06-04%20150313.png)

## RESULT: 
The program successfully reads the dimensions of the chocolate bar and determines whether the first player can force a win. It prints "yes" when n × m is even and "no" when n × m is odd.

# Ex.No:3(E) ENUM

## QUESTION:

WriTe a Java program to define an enum called Direction that contains four constants: NORTH, SOUTH, EAST, and WEST.
## AIM:

To demonstrate the use of enumeration (enum) in Java for validating and displaying direction values.
## ALGORITHM :
1. Start the program execution.
2. Create an enum named Direction containing the constants NORTH, SOUTH, EAST, and WEST.
3. Read a direction value from the user.
4. Convert the input to uppercase and attempt to match it with an enum constant.
5. Store the matched value in a Direction variable if the input is valid.
6. Display the entered direction or an error message for invalid input.
7. Stop the program execution.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
enum Direction{
    NORTH,
    SOUTH,
    EAST,
    WEST;
}
public class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String inp = sc.nextLine();
        try{
            Direction d = Direction.valueOf(inp.toUpperCase());
            System.out.println("You entered direction: "+d);
        }
        catch(IllegalArgumentException e){
            System.out.println("Invalid direction entered.");
        }
    }
}
```






## OUTPUT:
![IMAGE](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-5(A)/Screenshot%202026-06-04%20171757.png)


## RESULT:
The program successfully validates the user-entered direction using an enum and displays the corresponding direction or an error message for invalid input.

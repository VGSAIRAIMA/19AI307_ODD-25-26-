# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?
## AIM:
To demonstrate exception handling by catching and handling a NullPointerException in Java.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary package for user input.
3. Read a string value from the user.
4. Assign null to the string variable if the input is "null".
5. Attempt to convert the string to uppercase using the toUpperCase() method.
6. Catch the NullPointerException and display an appropriate error message.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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
        String str = sc.nextLine();
        try{
            if(str.equals("null")){
                str = null;
            }
            System.out.println(str.toUpperCase());
        }
        catch(NullPointerException e){
            System.out.println("Null element");
        }
    }
}
```

## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-04/DAY-1/Screenshot%202026-06-04%20172214.png)


## RESULT:
The program successfully demonstrates exception handling by catching a NullPointerException and displaying a suitable message when a null value is encountered.

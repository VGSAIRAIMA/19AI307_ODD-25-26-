# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

Input	Result
Ram
25
--- User Details ---
Name: Ram
Age: 25
## AIM:
To read and display user details using chained input streams in Java.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary packages 'java.io.BufferedReader', 'java.io.IOException', and 'java.io.InputStreamReader'.
3. Create a BufferedReader object by chaining it with an InputStreamReader object.
4. Read the user's name and age from the keyboard.
5. Store the entered values in string variables.
6. Display the user's name and age on the screen.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: V G SAIRAIMA
Register Number: 212225040359
*/
```

## SOURCE CODE:


```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) throws IOException {
        System.out.println("--- User Details ---");
        BufferedReader obj = new BufferedReader(new InputStreamReader(System.in));
        String name = obj.readLine();
        String age = obj.readLine();
        System.out.println("Name: "+name);
        System.out.println("Age: "+age);
        //while((data=obj.readLine())!=null){
         //   System.out.println("Name: "+data);
        //}
        
    }
}
```




## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-05/DAY-1/Screenshot%202026-06-04%20161018.png)
## RESULT:
The program successfully reads the user's name and age using chained streams and displays the entered details.

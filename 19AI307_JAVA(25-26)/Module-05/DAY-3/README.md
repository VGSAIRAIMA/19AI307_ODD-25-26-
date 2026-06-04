# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

For example:

Input	Result
Saveetha
25
saveetha.ac.in
User Information
================
Name  : Saveetha
Age   : 25
Email : saveetha.ac.in

## AIM:
To write user information into a text file and read the stored information from the file using file handling in Java.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary packages for file handling and user input.
3. Read the user's name, age, and email address from the keyboard.
4. Create a PrintWriter object and write the user details into the text file.
5. Close the file after writing the data successfully.
6. Open the file using BufferedReader, read each line, and display the stored information.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.*;
import java.io.*;

public class prog{
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        String fileName="userdata.txt";
        String name = in.nextLine();
        int age = in.nextInt();
        String email = in.next();
        try{
        PrintWriter pw = new PrintWriter(new FileWriter(fileName,true));
        pw.println("Name  : "+name);
        pw.println("Age   : "+age);
        pw.println("Email : "+email);
        pw.close();
        
        BufferedReader br = new BufferedReader(new FileReader(fileName));
        String data;
        System.out.println("User Information");
        System.out.println("================");
        while((data = br.readLine())!=null){
            System.out.println(data);
        }
        br.close();
    }
    catch(IOException e){
        e.printStackTrace();
    }
    }
}

```
## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-05/DAY-3/Screenshot%202026-06-04%20161842.png)


## RESULT:
The program successfully stores the user's details in a text file and retrieves the stored information for display using file handling operations.

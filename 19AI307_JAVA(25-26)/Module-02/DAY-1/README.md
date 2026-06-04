# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

For example:

Input	Result
TN10AB1234 Car Ravi
TN22CD5678 Bike Meena
TN10AB1234 | Car | Ravi
TN22CD5678 | Bike | Meena


## AIM:

To create a Vehicle class with attributes number, type, and owner, and display the vehicle details.
## ALGORITHM :
1. Start the program execution.
2. Create a Vehicle class with attributes number, type, and owner.
3. Read the vehicle number, type, and owner details from the user.
4. Create Vehicle objects and assign the entered values to the attributes.
5. Access the stored vehicle details from the objects.
6. Display the vehicle details in the required format.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Vehicle{
    String number;
    String type;
    String owner;
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}

```






## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-02/DAY-1/Screenshot%202026-06-04%20163259.png)


## RESULT:
The program successfully creates Vehicle objects, stores the vehicle number, type, and owner details, and displays them in the specified format.

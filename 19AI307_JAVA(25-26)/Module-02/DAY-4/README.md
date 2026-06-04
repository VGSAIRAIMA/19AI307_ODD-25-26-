# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java class with a constructor that accepts two numbers as input parameters. The constructor should calculate and display the sum, difference, product, and quotient of the two numbers.

Input	Result
3
4
Sum: 7.0
Difference: -1.0
Product: 12.0
Quotient: 0.75


## AIM:
To perform basic arithmetic operations using a parameterized constructor in Java.

## ALGORITHM :
1. Start the program execution.
2. Create a class with a parameterized constructor to accept two numbers.
3. Read two decimal numbers from the user.
4. Pass the input values to the constructor while creating the object.
5. Calculate the sum, difference, product, and quotient of the two numbers inside the constructor.
6. Display the results of all arithmetic operations.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Op{
    double a ;
    double b ;
    Op (double a,double b){
        this.a=a;
        this.b=b;
        System.out.printf("Sum: %.1f\n",(this.a+this.b));
        System.out.printf("Difference: %.1f\n",(this.a-this.b));
        System.out.printf("Product: %.1f\n",(this.a*this.b));
        System.out.print("Quotient: "+(this.a/this.b));
        
    }
}
class prog{
    public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    double a = sc.nextDouble();
    double b = sc.nextDouble();
    Op o = new Op(a,b);
    }
}
```






## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-02/DAY-4/Screenshot%202026-06-04%20164346.png)


## RESULT:
The program successfully performs addition, subtraction, multiplication, and division on two numbers using a parameterized constructor and displays the results.

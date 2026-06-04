# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:
To demonstrate the use of the this keyword by returning the current object from a method and invoking another method using method chaining.

## ALGORITHM :
1. Start the program execution.
2. Create a class Employee with methods display() and printName().
3. Define the display() method to return the current object using the this keyword.
4. Define the printName() method to display the employee name or details.
5. Create another method that calls display().printName() using method chaining.
6. Create an Employee object and invoke the chaining method.
7. Stop the program execution.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Employee{
    String name;
    void setName(String name){
        this.name=name;
    }
    Employee display(){
        return this;
    }
    void printName(){
        System.out.println("Employee Name: "+this.name);
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String name= sc.nextLine();
        Employee e = new Employee();
        e.setName(name);
        e.display().printName();
    }
}
```





## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-02/DAY-5/Screenshot%202026-06-04%20164656.png)

## RESULT:
The program successfully demonstrates the use of the this keyword by returning the current object and invoking another method through method chaining

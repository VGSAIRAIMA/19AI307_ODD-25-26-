# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To implement encapsulation in Java by creating a BankAccount class with private instance variables and public getter and setter methods.

## ALGORITHM :
1. Start the program execution.
2. Create a BankAccount class with private variables accountNumber and balance.
3. Define public getter and setter methods for accessing and modifying the private variables.
4. Create an object of the BankAccount class in the main method.
5. Read the account number and balance from the user.
6. Use the setter methods to assign values and the getter methods to display them.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class BankAccount{
    private String accountNumber;
    private double bal;
    public String getAccountNumber(){
        return accountNumber;
    }
    public double getBalance(){
        return bal;}
    public void setAccountNumber(String accountNumber){
        this.accountNumber = accountNumber;
    }
    public void setBalance(double bal){
        this.bal = bal;}
    void display(){
        System.out.println("Account Number: "+this.accountNumber);
        System.out.println("Balance: "+this.bal);
    }
    
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String ac = sc.nextLine();
        double bal = sc.nextDouble();
        BankAccount b = new BankAccount();
        b.setAccountNumber(ac);
        b.setBalance(bal);
        b.display();
    }
}
```





## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-02/DAY-3/Screenshot%202026-06-04%20151921.png)


## RESULT:
The program successfully demonstrates encapsulation by using private instance variables and public getter and setter methods to access and modify bank account details.

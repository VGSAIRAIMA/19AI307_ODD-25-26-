# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

Input:

3 100 200 300
Output:

Final Balance: 600
For example:

Input	Result
3
100
200
300

Final Balance: 600


## AIM:
To perform synchronized deposit operations on a bank account using multiple threads and display the final account balance.

## ALGORITHM :
1. Start the program execution.
2. Create a BankAccount object with an initial balance of zero.
3. Read the number of deposit transactions and the deposit amounts from the user.
4. Create a separate thread for each deposit operation and pass the bank account object and amount.
5. Execute the deposit method using synchronization to ensure thread safety.
6. Wait for all deposit operations to complete and display the final account balance.
7. Stop the program execution.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class BankAccount {
    int balance = 0;

    public synchronized void deposit(int amount) {
        balance = balance + amount;
    }

    public int getBalance() {
        return balance;
    }
}
class DepositThread extends Thread{
    BankAccount ba;
    int amt;
    DepositThread(BankAccount ba,int amt){
        this.ba=ba;
        this.amt=amt;
    }
    public void run(){
        ba.deposit(amt);
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        BankAccount ba = new BankAccount();
        for(int i=0;i<n;i++){
            int amt = sc.nextInt();
            DepositThread dt = new DepositThread(ba,amt);
            dt.start();
        }
        try { Thread.sleep(1000); } catch(Exception e) {}

        System.out.println("Final Balance: " + ba.getBalance());
    }
}
```


## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-05/DAY-5/Screenshot%202026-06-04%20162504.png)



## RESULT:

The program successfully performs multiple deposit transactions using synchronized threads and displays the correct final balance in the bank account.


# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

For example:

Input	Result
NewThread
Priority of Thread: 5
Name of Thread: NewThread
Thread[NewThread,5,main]


## AIM:
To create a thread with a user-defined name and display its priority, name, and thread information using Java multithreading.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary package for user input.
3. Read the thread name from the user.
4. Create a new thread using the Runnable interface and assign the given name to it.
5. Retrieve and display the thread's priority, name, and complete thread information.
6. Start the execution of the created thread.
7. Stop the program execution.


## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.*;
public class prog{
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        String name=in.nextLine();
        Thread t = new Thread(new Runnable(){
            @Override
            public void run(){
            System.out.println("Priority of Thread: "+Thread.currentThread().getPriority());
            System.out.println("Name of Thread: "+Thread.currentThread().getName());
            System.out.println(Thread.currentThread());
            }
        },name);
        t.start();
    }
}
```





## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-05/DAY-4/Screenshot%202026-06-04%20162152.png)

## RESULT:
The program successfully creates a thread with the specified name and displays its priority, name, and thread details.

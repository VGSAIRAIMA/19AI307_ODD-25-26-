# Ex.No:3(D)    INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.


AggressiveController: Allows only if "GREEN".

DefensiveController: Allows for "GREEN" or "YELLOW".

 Input Format:

signalColor
controllerType
signalColor: A string indicating the signal color (GREEN, YELLOW, RED)

controllerType: An integer (1 for AggressiveController, 2 for DefensiveController)

 Output Format:

Print "GO"       → if vehicle is allowed to move  
Print "STOP"     → if vehicle must stop

For example:

Input	Result
GREEN 1
GO
## AIM:
To demonstrate the use of interfaces and runtime polymorphism in controlling vehicle movement based on traffic signal conditions.


## ALGORITHM :
1. Start the program execution.
2. Create an interface Signal containing the method canPass().
3. Implement the interface in AggressiveController and DefensiveController classes with different passing rules.
4. Read the traffic signal color and controller type from the user.
5. Create an object of the appropriate controller class using an interface reference.
6. Invoke the canPass() method and display "GO" or "STOP" based on the result.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
interface Signal{
    public boolean canPass(String s);
}
class AggressiveController implements Signal{
     public boolean canPass(String s){
         if(s.equalsIgnoreCase("GREEN")){
             return true;
         }
         else{
             return false;
         }
     }
}
class DefensiveController implements Signal{
       public  boolean canPass(String s){
         if(s.equalsIgnoreCase("GREEN")||s.equalsIgnoreCase("YELLOW")){
             return true;
         }
         else{
             return false;
         }
}}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        String s = sc.next();
        int t = sc.nextInt();
        Signal sn;
        if(t==1){
            sn = new AggressiveController();
            if(sn.canPass(s)){
                System.out.println("GO");
            }
            else{
                System.out.println("STOP");
            }
        }
        else{
            sn = new DefensiveController();
            if(sn.canPass(s)){
                System.out.println("GO");
            }
            else{
                System.out.println("STOP");
            }
        }
    }
}
```





## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-4/Screenshot%202026-06-04%20171356.png)

## RESULT:
The program successfully demonstrates interfaces and runtime polymorphism by applying different traffic control strategies and displaying whether a vehicle can proceed or must stop.

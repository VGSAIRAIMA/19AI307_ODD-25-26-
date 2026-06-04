# Ex.No:2(B) METHODS

## QUESTION:
Write a method void modifyValue(int num) that tries to modify the passed value(add passed value with 10) and print "Inside method: "+num . 

Show in main() that the original value does not change.

After calling modifyValue(int num) method in main , print the "Outside method: "+num

For example:

Input	Result
10
Inside method: 20
Outside method: 10


## AIM:

To demonstrate pass-by-value in Java by modifying a parameter inside a method and showing that the original value remains unchanged.
## ALGORITHM :
1. Start the program execution.
2. Read an integer value from the user in the main method.
3. Pass the integer value as an argument to the modifyValue() method.
4. Add 10 to the received parameter inside the modifyValue() method.
5. Display the modified value inside the method.
6. Display the original value in the main method after the method call.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class res{
    int num;
    void modifyValue(int num){
        System.out.println("Inside method: "+(num+10));
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        res r = new res();
        r.modifyValue(num);
        System.out.println("Outside method: "+num);
    }
}
```





## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-02/DAY-2/Screenshot%202026-06-04%20163531.png)

## RESULT:
The program successfully demonstrates that Java uses pass-by-value, as the value modified inside the method does not affect the original variable in the main method.

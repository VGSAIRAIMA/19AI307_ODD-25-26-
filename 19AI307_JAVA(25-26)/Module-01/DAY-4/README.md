# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to find the maximum odd number in an array

 
For example:

Input	Result
5
2
3
7
8
6
7
4
2
4
6
8
No odd number found

## AIM:
To find and display the maximum odd number present in an array of integers.

## ALGORITHM :
1. Start the program execution.
2. Read the size of the array and store the elements in the array.
3. Initialize max with the minimum integer value and a flag variable to indicate the presence of odd numbers.
4. Traverse the array and check whether each element is odd.
5. If an odd element is found, update max whenever the element is greater than the current maximum odd value.
6. Display the maximum odd number if any odd number exists; otherwise display "No odd number found".
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
rt java.util.Scanner;
public class max{
    public static void main(String [] args){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int i;
        int arr[]= new int[n];
        for (i=0;i<n;i++){
            arr[i]=in.nextInt();
        }
        int max=Integer.MIN_VALUE;
        int odd=0;
        for (i=0;i<n;i++){
            if(arr[i]%2!=0){
                odd=1;
                if(max<arr[i])
                {
                    max=arr[i];
                }
            }
            
        }
        if(odd==0){
            System.out.print("No odd number found");
        }
        else{
            System.out.print(max);
        }
            
        
    }
}
```

## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-01/DAY-4/Screenshot%202026-06-04%20151605.png)
## RESULT:
The program successfully finds and displays the maximum odd number in the array, or prints "No odd number found" when the array contains no odd numbers.

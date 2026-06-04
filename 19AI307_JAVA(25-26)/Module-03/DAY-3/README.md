# Ex.No:3(C) ABSTRACTION

## QUESTION:
A group of researchers receives mysterious numerical sequences believed to be sent by intelligent alien life. To decode them, scientists have built intelligent SignalAgents that follow abstract processing rules. Each agent listens to the numbers differently.

Your task is to create a system where a base abstract class SignalAgent declares:abstract int decodeSignal(int[] signal);
Two intelligent agents extend this class:

PrimeAgent

MirrorAgent

🧩 Agent Behaviors (Described Indirectly):
🔍 PrimeAgent
This agent believes the signal's meaning lies in rarity. It scans the signal, only considers prime numbers, and returns the sum of them.


MirrorAgent
This one trusts symmetry. It compares elements from both ends inward. If all such pairs are perfectly symmetric (same from left and right), it considers the message balanced, otherwise broken.

 Input Format:

n
x1 x2 x3 ... xn
type
n = number of elements in the signal

x1 ... xn = space-separated integers

type = 1 for PrimeAgent, 2 for MirrorAgent

Output Format:
If PrimeAgent is selected → output the sum.

If MirrorAgent is selected → output "BALANCED" or "BROKEN" depending on the symmetry.

 

For example:

Input	Result
5
2 3 4 5 6
1
10
5
1 2 3 2 1
2
BALANCED


## AIM:
To demonstrate abstraction and runtime polymorphism by decoding signals using different agent classes.

## ALGORITHM :
1. Start the program execution.
2. Create an abstract class SignalAgent with an abstract method decodeSignal().
3. Implement PrimeAgent and MirrorAgent classes by overriding the decodeSignal() method.
4. Read the signal array elements and the agent type from the user.
5. Create an object of the appropriate agent class using a SignalAgent reference.
6. Decode the signal and display the result based on the selected agent.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:


```
import java.util.Scanner;
abstract class SignalAgent{
    abstract int decodeSignal(int[] signal);
}
class PrimeAgent extends SignalAgent{
    boolean isPrime(int n){
        int c=0;
        for(int i=2;i<=n/2;i++){
            if(n%i==0){
                c++;
                break;
            }
        }
        if (c==0&&n!=1){
            return true;
        }
        else{
            return false;
        }
    }
    int decodeSignal(int[] signal){
        int sum=0;
      for(int i=0;i<signal.length;i++){
          if(isPrime(signal[i])==true){
              sum+=signal[i];
          }
          
      }
      return sum;
    }
}
class MirrorAgent extends SignalAgent{
    int decodeSignal (int[] signal){
        boolean f = true;
        for(int i=0;i<=signal.length/2;i++){
            if(signal[i]!=signal[signal.length-i-1]){
                f=false;
            }
        }
        if(f==true){
            return 1;
        }
        else{
            return 0;
        }
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int t = sc.nextInt();
        SignalAgent sa;
        if(t==1){
            sa = new PrimeAgent();
            System.out.println(sa.decodeSignal(arr));

        }
        else{
            sa=new MirrorAgent();
            if(sa.decodeSignal(arr)==1){
                System.out.println("BALANCED");
            }
            else{
                 System.out.println("BROKEN");
            }
        }
    }
}
```




## OUTPUT:

![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-3/Screenshot%202026-06-04%20170906.png)

## RESULT:
The program successfully demonstrates abstraction and runtime polymorphism by using different agent classes to decode signals and produce the required output.

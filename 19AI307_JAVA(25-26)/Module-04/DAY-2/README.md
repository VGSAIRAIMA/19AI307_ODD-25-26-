# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

Each user has their own preference:

Some are looking for "Gamers"

Some prefer "Pet Lovers"

Others vibe with "Bookworms"

Or maybe they're into "Gym Freaks", etc.

When a new user signs up, the app should only notify users whose preferences match that new person’s type.

Users subscribe to MatchIt’s notification service based on their “match interest”. The system notifies them only when someone with their preferred type signs up.

What Students Must Do:
Implement the Observer Pattern

MatchItServer = Subject

User = Observer

When a new person joins, notify only users who match the preference

Each user prints a custom message when their preferred type joins.

Input Format:
First line: Number of users n

Next n lines: UserName Preference
(e.g., Alice Gamer)

Next line: Number of sign-ups m

Next m lines: NewUserName Type
(e.g., Jack Gamer)

Output Format:
For each signup:

New User Joined: [NewUserName] - Type: [Type]
[UserName]: Omg! A new [Type]? MatchIt, you know me too well! 
...
Only matching users get notified.

For example:

Input	Result
3
Alice Gamer
Bob Bookworm
Cleo PetLover
2
Jack Gamer
Lily Bookworm
New User Joined: Jack - Type: Gamer  
Alice: Omg! A new Gamer? MatchIt, you know me too well! (It’s Jack!)  
New User Joined: Lily - Type: Bookworm  
Bob: Omg! A new Bookworm? MatchIt, you know me too well! (It’s Lily!)
2
Daisy GymFreak
Ethan PetLover
1
Zara Bookworm
New User Joined: Zara - Type: Bookworm

## AIM:
To implement the Observer Design Pattern following SOLID principles for notifying registered users when a new user with a matching preference joins the system.
## ALGORITHM :
1. Start the program execution.
2. Define an Observer interface to follow the Interface Segregation Principle by declaring notification-related methods.
3. Create a User class that implements the Observer interface, adhering to the Single Responsibility Principle.
4. Create a MatchItServer class responsible only for managing observers and sending notifications.
5. Register existing users as observers in the MatchItServer object.
6. Notify only the observers whose preferences match the newly joined user's type, following the Open/Closed and Dependency Inversion Principles.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.*;

interface Observer {
    void notify(String name, String type);
    String getPreference();
}

class User implements Observer {
    String name;
    String type;
    User(String name,String type){
        this.name=name;
        this.type=type;
    }
    public void notify(String name,String type){
        System.out.println(this.name+": Omg! A new "+this.type+"? MatchIt, you know me too well! (It’s "+name+"!)");
    }
    public String getPreference(){
        return type;
    }
}

class MatchItServer {
    List<Observer> users = new ArrayList<>();
    void register(Observer o){
        users.add(o);
    }
    void newSignup(String name,String type){
        System.out.println("New User Joined: "+name+" - Type: "+type);
        for(Observer o:users){
            if(o.getPreference().equals(type)){
                o.notify(name,type);
            }
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       MatchItServer server = new MatchItServer();

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] userInfo = sc.nextLine().split(" ");
            server.register(new User(userInfo[0], userInfo[1]));
        }

        int m = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < m; i++) {
            String[] newUser = sc.nextLine().split(" ");
            server.newSignup(newUser[0], newUser[1]);
        }
    }
}

```





## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-04/DAY-2/Screenshot%202026-06-04%20172615.png)


## RESULT:
The program successfully implements the Observer Design Pattern while adhering to SOLID principles, ensuring modularity, maintainability, extensibility, and proper separation of responsibilities.

# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to simulate a hotel booking system using method overloading.

Create a program for a hotel booking system using method overloading. There are two types of bookings:

Single-day booking → Uses only room type

Multi-day booking → Uses both room type and number of nights

The program should:

Ask the user for the room type

Ask whether the user wants to book for multiple nights

Use overloaded methods to:

Print per-night charge if only room type is entered

Calculate total amount for multiple nights if the duration is entered

For example:

Input	Result
Single Room  
no
Single Room   booked. ₹1000 per night.


## AIM:
To demonstrate compile-time polymorphism using method overloading in a hotel room booking system.

## ALGORITHM :
1. Start the program execution.
2. Create a HotelBooking class with overloaded bookRoom() methods.
3. Read the room type and booking choice from the user.
4. Check whether the user wants to specify the number of nights.
5. Call the bookRoom(roomType, nights) method if the user enters "yes".
6. Otherwise, call the bookRoom(roomType) method to perform a default booking.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class HotelBooking {
    static int price =1000;

    void bookRoom(String roomType) {
        System.out.println(roomType + " booked. ₹" + price + " per night.");}
    
    void bookRoom(String roomType, int nights) {
        int total = price * nights;
        System.out.println(roomType + " booked for " + nights + " nights. Total: ₹" + total);
    }

}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        HotelBooking hb = new HotelBooking();

        String roomType = sc.nextLine();

        String choice = sc.nextLine();

        if (choice.trim().equalsIgnoreCase("yes")) {
            int nights = sc.nextInt();
            hb.bookRoom(roomType, nights); 
        } else {
            hb.bookRoom(roomType);
        }

        sc.close();
    }
}

```






## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-2/Screenshot%202026-06-04%20170611.png)



## RESULT:
The program successfully demonstrates compile-time polymorphism through method overloading by booking a hotel room with or without specifying the number of nights.

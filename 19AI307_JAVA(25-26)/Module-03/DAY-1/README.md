# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

## AIM:
To demonstrate inheritance and method overriding by calculating the final gold purchase price and discounts for different types of customers.

## ALGORITHM :
1. Start the program execution.
2. Create a base class Customer and derived classes RegularCustomer and PremiumCustomer.
3. Read the customer type, customer ID, name, purchase weight, and gold rate from the user.
4. Create an object of the appropriate customer class based on the entered customer type.
5. Calculate the discount and final purchase price using the overridden methods.
6. Display the customer details, discount percentage, final price, and cashback for premium customers.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:


```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
     
    }
}

class RegularCustomer extends Customer{
    RegularCustomer(String customerId,String name,double purchaseWeight,double goldRatePerGram){
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    int getDiscountRate() {
        return 2;
    }
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
     
    }
    
}
class PremiumCustomer extends Customer{
        PremiumCustomer(String customerId,String name,double purchaseWeight,double goldRatePerGram){
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    int getDiscountRate() {
        return 5;
    }
    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
     
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String t = sc.nextLine();
        String id = sc.nextLine();
        String name= sc.nextLine();
        double w = sc.nextDouble();
        double r = sc.nextDouble();
        Customer c;
        if(t.trim().equalsIgnoreCase("regular")) {
    c = new RegularCustomer(id, name, w, r);
}
    else if(t.trim().equalsIgnoreCase("premium")) {
    c = new PremiumCustomer(id, name, w, r);
}
else{
    System.out.println("Invalid");
    return ;
}
c.display();
    }
}
```




## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-03/DAY-1/Screenshot%202026-06-04%20165715.png)


## RESULT:
The program successfully demonstrates inheritance and method overriding by calculating and displaying customer-specific discounts, final gold purchase prices, and cashback benefits based on the customer type.

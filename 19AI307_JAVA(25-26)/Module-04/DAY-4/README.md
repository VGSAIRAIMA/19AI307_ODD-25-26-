# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

For example:

Input	Result
africa
Lion eats Wildebeest


## AIM:
To implement the Abstract Factory Design Pattern following SOLID principles for creating related carnivore and herbivore objects based on a selected region.

## ALGORITHM :
1. Start the program execution.
2. Define interfaces for AnimalFactory, Carnivore, and Herbivore to follow the Dependency Inversion and Interface Segregation Principles.
3. Create concrete factory classes and animal classes for different regions while adhering to the Open/Closed Principle.
4. Read the region name from the user and select the appropriate factory object.
5. Use the factory object to create the corresponding carnivore and herbivore objects.
6. Invoke the carnivore's eat() method using the created herbivore object and display the result.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
interface AnimalFactory{
    public abstract Carnivore createCarnivore();
    public abstract Herbivore createHerbivore();
}
class AfricaFactory implements AnimalFactory{
    @Override
    public Carnivore createCarnivore(){
        return new AfricaCarnivore();
    }
    @Override
    public Herbivore createHerbivore(){
        return new AfricaHerbivore();
    }
    
}
class AsiaFactory implements AnimalFactory{
    @Override
    public Carnivore createCarnivore(){
        return new AsiaCarnivore();
    }
    @Override
    public Herbivore createHerbivore(){
        return new AsiaHerbivore();
    }
    
}
interface Carnivore{
    public abstract void eat(Herbivore animal);
}
class AfricaCarnivore implements Carnivore{
    @Override
    public void eat(Herbivore animal){
        System.out.print("Lion eats "+animal.returnName());
    }
} 
class AsiaCarnivore implements Carnivore{
    @Override
    public void eat(Herbivore animal){
        System.out.print("Tiger eats "+animal.returnName());
    }
} 
interface Herbivore{
    public abstract String returnName();
}
class AfricaHerbivore implements Herbivore{
    @Override
    public String returnName()
    {
        return "Wildebeest";
    }
}
class AsiaHerbivore implements Herbivore{
    @Override
    public String returnName()
    {
        return "Buffalo";
    }
}


// write your code here
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equalsIgnoreCase("africa")){
         factory = new AfricaFactory();
        }
        else if (region.equalsIgnoreCase("asia")) {
            factory = new AsiaFactory();
            
        }
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}

```





## OUTPUT:

![IMAGE](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-04/DAY-4/Screenshot%202026-06-04%20173055.png)

## RESULT:
The program successfully implements the Abstract Factory Design Pattern while following SOLID principles, creating region-specific animal objects and demonstrating their interaction.

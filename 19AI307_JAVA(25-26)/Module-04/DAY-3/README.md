# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

For example:

Input	Result
2
Java
James Gosling
Python
Guido Van Rossum
Books in Library:
- Java by James Gosling
- Python by Guido Van Rossum
1
Machine Learning
Andrew Ng
Books in Library:
- Machine Learning by Andrew Ng


## AIM:
To demonstrate composition by creating a Library class that contains and manages multiple Book objects.

## ALGORITHM :
1. Start the program execution.
2. Create a Book class with attributes for title and author.
3. Create a Library class that contains a collection of Book objects.
4. Read the number of books and their details from the user.
5. Create Book objects and add them to the Library object.
6. Display the details of all books stored in the library.
7. Stop the program execution.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return "- "+title + " by " + author;
    }
}

class Library {
    Book obj ;
    List<Book> books = new ArrayList<>();
    public void addBook(String title, String author) {
        
        obj = new Book(title,author);
        books.add(obj);
    }

    public void showBooks() {
        // Type Your Code Here
        System.out.println("Books in Library:");
        for (Book i : books){
        System.out.println(i.getDetails());
        }
        
    }
}



```






## OUTPUT:

![IAMGE](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-04/DAY-3/Screenshot%202026-06-04%20173626.png)

## RESULT:
The program successfully demonstrates composition by allowing a Library object to manage multiple Book objects and display their details.

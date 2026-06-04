# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

Input	Result
2
101
Alice
89.5
102
Bob
92.0
Students serialized successfully into: students.dat
Students deserialized successfully from: students.dat

Deserialized Students:
Student{id=101, name='Alice', marks=89.5}
Student{id=102, name='Bob', marks=92.0}

## AIM:
To serialize and deserialize a collection of Student objects using an ArrayList and file handling in Java.

## ALGORITHM :
1. Start the program execution.
2. Import the necessary packages for collections, serialization, and file handling.
3. Create a Student class that implements the Serializable interface.
4. Read the student details from the user and store them in an ArrayList.
5. Serialize the ArrayList of Student objects and write it into a file.
6. Deserialize the objects from the file and display the student details.
7. Stop the program execution.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {// it is a marker interface with zero fns
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = in.nextInt();
        in.nextLine(); // consume newline
        for(int i =0;i<n;i++){
            int id = in.nextInt();
            String name = in.next();
            double marks = in.nextDouble();
            Student s = new Student(id,name,marks);
            students.add(s);
        }
        StudentSerializationUserInput serialize = new StudentSerializationUserInput();
        serialize.serializeStudents(students,"students.dat");
        
        List<Student> deserialized=serialize.deserializeStudents("students.dat");
        
        
        if (deserialized != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserialized) {
                System.out.println(s);
            }
        }

        in.close();
    }
}

```





## OUTPUT:
![image](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-05/DAY-2/Screenshot%202026-06-04%20161506.png)
## RESULT:
The program successfully serializes the collection of Student objects into a file and deserializes them back, displaying the stored student details correctly.

# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:

To write a Java program that serializes a collection of Student objects (stored inside an ArrayList) into a file using ObjectOutputStream.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student class that implements Serializable.
4. Create an ArrayList<Student> and add multiple Student objects into it.
5. Create a FileOutputStream to the destination file (example: students.ser).
6. Wrap it with ObjectOutputStream.
7. Write the ArrayList to the file using writeObject().
8. Close the streams.
9. Display a message confirming successful serialization.
10. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.io.*;
import java.util.*;
class Student implements Serializable
{
    private static final long serialVersionUID = 1L;
    private int id;
    private String name;
    private double marks;
    public Student(int id, String name, double marks)
    {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }
    public String toString()
    {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput
{
    public static void serializeStudents(List<Student> students, String fileName)
    {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName)))
        {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        }
        catch (IOException e)
        {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName)
    {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName)))
        {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        }
        catch (Exception e)
        {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();
        int n = scanner.nextInt();
        scanner.nextLine();
        for (int i = 0; i < n; i++)
        {
            int id = scanner.nextInt();
            scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id, name, marks));
        }
        String fileName = "students.dat";
        serializeStudents(students, fileName);
        List<Student> deserializedStudents = deserializeStudents(fileName);
        if (deserializedStudents != null)
        {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents)
            {
                System.out.println(s);
            }
        }
        scanner.close();
    }
}
```

## OUTPUT:

<img width="1176" height="762" alt="image" src="https://github.com/user-attachments/assets/a93b000b-ed48-480d-9235-2190665b2a10" />

## RESULT:

The program successfully serializes a collection of Student objects into the file students.ser, storing the entire ArrayList in serialized form.

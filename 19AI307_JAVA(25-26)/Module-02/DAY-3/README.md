# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:

To write a Java program that defines a class Person with private instance variables name, age, and country, and to provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class named Person.
4. Declare private instance variables:</br>
     - name (String)</br>
     - age (int)</br>
     - country (String)</br>
5. Define public setter methods to assign values to each variable.
6. Define public getter methods to retrieve the values of each variable.
7. In the main method:</br>
     - Create an object of the Person class.</br>
     - Use setter methods to set name, age, and country.</br>
     - Use getter methods to display the values.</br>
8. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
class Person
{
    private String name;
    private int age;
    private String country;  
    public String getName()
    {
        return name;
    }
    public void setName(String name)
    {
        this.name = name;
    }
    public int getAge()
    {
        return age;
    }
    public void setAge(int age)
    {
        this.age = age;
    }
    public String getCountry()
    {
        return country;
    }
    public void setCountry(String country)
    {
        this.country = country;
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Person obj = new Person();
        obj.setName(sc.nextLine());
        obj.setAge(sc.nextInt());
        obj.setCountry(sc.nextLine());
        System.out.println("Person 1");
        System.out.println("Name: " + obj.getName());
        System.out.println("Age: " + obj.getAge());
        System.out.println("Country: " + obj.getCountry());
    }
}
```

## OUTPUT:

<img width="648" height="365" alt="image" src="https://github.com/user-attachments/assets/ef3379a6-f10a-4c24-963d-9dfb149f2458" />


## RESULT:

The program successfully creates a Person class with private variables and accesses them using getter and setter methods, demonstrating encapsulation in Java.

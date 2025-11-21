# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to create an inner class and access it from the outer class.

## AIM:

To write a Java program that creates an inner class and accesses it from the outer class. The inner class should display a greeting message using a name entered by the user.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class named Outer.
4. Inside the outer class, define an inner class named Inner.
5. In the Inner class, create a method greet() that accepts a name and prints a greeting message.
6. In the Main class, create a Scanner object to read input from the user.
7. Read the user's name as a string.
8. Create an object of the Outer class.
9. Using the outer class object, create an object of the inner class.
10. Call the greet() method of the inner class and pass the user input.
11. Display the result.
12. End the program

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.Scanner;
class Outer 
{
    class Inner 
    {
        void greet(String name) 
        {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main 
{
    public static void main(String[] args) 
    {

        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        Outer outer = new Outer();
        Outer.Inner inner = outer.new Inner();
        inner.greet(name);
    }
}
```

## OUTPUT:

<img width="1129" height="194" alt="image" src="https://github.com/user-attachments/assets/e7167a2e-a015-48c3-8c7d-56afed7502f6" />

## RESULT:

The program successfully demonstrates the concept of an inner class in Java.
By taking a name as input, the inner class prints the output.

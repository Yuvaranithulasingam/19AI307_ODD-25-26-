# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Lovely is learning java basics, can you teach her the different types of datatypes in java? Write a program that uses all datatypes and print them all.
Input Format:
byte - 24, short - 11000, int - 1,34,500, long - 24,23,10,34, float - 24.20, double - 1,30,000.80, boolean - true/false, char - 'u', String -"Heyyy, Lovely, Let's learn java!".

## AIM:

To understand and demonstrate the basic data types in Java by declaring variables of each data type (byte, short, int, long, float, double, boolean, char, and String) and displaying their values using a Java program.

## ALGORITHM :

1. Start the program.
2. Declare variables for all primitive datatypes:</br>
     -> byte</br>
     -> short</br>
     -> int</br>
     -> long</br>
     -> float</br>
     -> double</br>
     -> boolean</br>
     -> char</br>
3. Declare a variable for the non-primitive datatype:</br>
     -> String</br>
4. Assign appropriate values to each of the declared variables.
5. Print all the variable values using System.out.println() statements.
6. End the program.

## PROGRAM:
#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## Sourcecode.java:
```
import java.util.Scanner;
public class AllDataTypes 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        byte byteVal = sc.nextByte();
        short shortVal = sc.nextShort();
        int intVal = sc.nextInt();
        long longVal = sc.nextLong();
        float floatVal = sc.nextFloat();
        double doubleVal = sc.nextDouble();
        boolean boolVal = sc.nextBoolean();
        char charVal = sc.next().charAt(0); 
        sc.nextLine(); 
        String stringVal = sc.nextLine();
        System.out.println("Hey Lovely, let's print all types of data received from user using different data types");
        System.out.println("This is byte datatype " + byteVal);
        System.out.println("This is short datatype " + shortVal);
        System.out.println("This is int datatype " + intVal);
        System.out.println("This is long datatype " + longVal);
        System.out.println("This is float datatype " + floatVal);
        System.out.println("This is double datatype " + doubleVal);
        System.out.println("This is boolean datatype " + boolVal);
        System.out.println("This is char datatype " + charVal);
        System.out.println("This is string datatype " + stringVal);
    }
}
```

## OUTPUT:

<img width="1228" height="399" alt="image" src="https://github.com/user-attachments/assets/25a7df9f-31ea-47b7-8d5e-d814abeaa4c5" />

## RESULT:

Thus, the Java program was successfully written and executed to demonstrate the use of all primitive and non-primitive data types. The values of each data type were displayed correctly, and the objective of understanding Java data types, variables, and basic operations was achieved.


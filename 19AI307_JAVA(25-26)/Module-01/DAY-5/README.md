# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to calculate the power of a given number.

## AIM:

To write a Java program that calculates the power of a given number using a loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the base number and exponent from the user.
4. Initialize a variable result = 1.
5. Use a loop from 1 to exponent:
     - Multiply result by the base each time.</BR>
6. After the loop ends, result will hold the final power value.
7. Display the value of result.
8. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        double base = sc.nextDouble();
        double exponent = sc.nextDouble();
        double result = Math.pow(base, exponent);
        System.out.println(base + " raised to the power of " + exponent + " is: " + result);
    }
}
```

## OUTPUT:

<img width="910" height="194" alt="image" src="https://github.com/user-attachments/assets/cd9c0438-6f3e-47c3-bc46-19ccb2a252ec" />


## RESULT:

The program successfully computes the power of a given number by repeatedly multiplying the base according to the exponent and displays the final result.

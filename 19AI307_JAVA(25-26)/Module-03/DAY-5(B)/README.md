# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:

To write a Java program that checks whether a given number is an Armstrong number using Math.pow() and the Integer wrapper class.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Take an integer input from the user.
4. Convert the number to a string using Integer.toString() to count the digits.
5. Extract each digit using modulus (%) and division (/).
6. For each digit, calculate the power using Math.pow(digit, numberOfDigits).
7. Add all powered digits to get the sum.
8. Compare the sum with the original number.
9. If both are equal, it is an Armstrong number; otherwise, it is not.
10. Display the result.
11. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.Scanner;
public class Main
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();  
        int original = num;
        int digits = Integer.toString(num).length(); 
        int sum = 0;
        while (num > 0) 
        {
            int digit = num % 10;
            sum += (int)Math.pow(digit, digits);
            num /= 10;
        }

        if (sum == original) 
        {
            System.out.println(original + " is an Armstrong number.");
        } 
        else 
        {
            System.out.println(original + " is not an Armstrong number.");
        }
    }
}
```

## OUTPUT:

<img width="757" height="195" alt="image" src="https://github.com/user-attachments/assets/f580a4e8-a86d-444e-a035-b609b76d23b6" />

## RESULT:

The program successfully checks whether a given number is an Armstrong number using Math.pow() and Integer wrapper class.

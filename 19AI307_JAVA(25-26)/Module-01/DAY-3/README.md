# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321

## AIM:

To write a Java program that reverses a given number using a while loop by extracting digits one by one and constructing the reversed number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input number from the user.</br>
4. Initialize a variable reverse = 0.
5. Repeat while the number is greater than 0:.</br>
     - Extract the last digit using digit = number % 10.</br>
     - Add the digit to the reversed number using</br>
          -- reverse = reverse * 10 + digit..</br>
     - Remove the last digit from the original number using.</br>
          -- number = number / 10..</br>
6. Display the reversed number.
7. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber: 212222110057

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int reversed = 0;
        while(num != 0)
        {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }
        System.out.println("Reversed number: " + reversed);
    }
}
```

## OUTPUT:

<img width="578" height="197" alt="image" src="https://github.com/user-attachments/assets/3740026f-0533-4451-bc6f-622d871d210f" />

## RESULT:

Thus, the Java program to reverse a number using a while loop was successfully implemented and executed.

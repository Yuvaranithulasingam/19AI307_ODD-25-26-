# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
You're entering a magical maze with a 3-digit access code. Based on its digits, the maze behaves differently:</br>
   -> If the middle digit is 0 → Maze freezes.</br>
   -> If the sum of digits is exactly 15 → Maze reflects you back.</br>
   -> If the first digit is odd and the last digit is even →  Maze opens.</br>
   -> Otherwise →  Maze collapses.</br>

## AIM:

To write a Java program that reads a 3-digit access code and determines the behavior of a magical maze based on the conditions involving the digits—whether the maze freezes, reflects, opens, or collapses.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the 3-digit access code from the user.
4. Extract the digits:
     - first digit = code / 100 </br>
     - middle digit = (code / 10) % 10 </br>
     - last digit = code % 10 </br>
5. Check the conditions in order:
     - If the middle digit is 0, display “Maze freezes.”</br>
     - Else if the sum of all digits is 15, display “Maze reflects you back.”</br>
     - Else if the first digit is odd AND the last digit is even, display “Maze opens.”</br>
     - Otherwise, display “Maze collapses.”</br>
6.End the program.

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
        int num = sc.nextInt();
        int first = num / 100;
        int mid = (num / 10) % 10;
        int last = num % 10;
        int sum = first + mid + last;
        if(mid == 0)
        {
            System.out.print("Freezes");
        }
        else if(sum==15)
        {
            System.out.print("Reflects");
        }
        else if(first % 2 == 1 && last % 2 == 0)
        {
            System.out.print("Opens");
        }
        else
        {
            System.out.print("Collapses");
        }
    }
}
```

## OUTPUT:

<img width="364" height="232" alt="image" src="https://github.com/user-attachments/assets/deb5528c-7796-4f87-9fda-388c39175600" />

## RESULT:

Thus, the program was successfully written and executed. The behavior of the magical maze was correctly determined based on the digits of the 3-digit access code according to the given conditions.

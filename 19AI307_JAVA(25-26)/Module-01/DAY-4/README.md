# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to count the number of positive, negative, and zero elements in an array.

## AIM:

To write a Java program that counts how many elements in an array are positive, negative, and zero using a loop.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare an array with integer elements.
4. Create three counters:</br>
    - positive = 0</br>
    - negative = 0</br>
    - zero = 0</br>
5. Traverse the array using a loop.
    - For each element:</br>
        -- If the element > 0 → increment positive.</br>
        -- Else if the element < 0 → increment negative.</br>
        -- Else → increment zero.</br>
6. After the loop ends, display the values of positive, negative, and zero.
7. End the program.

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
        int numbers = sc.nextInt();
        int[] arr = new int[numbers];
        for(int ind=0; ind<numbers; ind++)
        {
            arr[ind]=sc.nextInt();
        }
        int pc = 0;
        int nc = 0;
        int zc = 0;      
        for(int ind = 0;ind < numbers; ind++)
        {
           if(arr[ind] > 0)
           {
               pc++;
           }
           else if(arr[ind] < 0)
           {
               nc++;
           }
           else
           {
               zc++;
           }
        }       
        System.out.println("Positive count: " + pc);
        System.out.println("Negative count: " + nc);
        System.out.println("Zero count: " +zc);
    }
}
```

## OUTPUT:

<img width="508" height="524" alt="image" src="https://github.com/user-attachments/assets/407b61d7-88f0-4d1f-bd09-139f3c9ecc5a" />

## RESULT:

The program successfully counts the number of positive, negative, and zero elements in the given array and displays the result.

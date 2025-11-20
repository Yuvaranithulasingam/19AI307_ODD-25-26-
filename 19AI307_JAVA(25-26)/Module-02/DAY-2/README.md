# Ex.No:2(B) METHODS

## QUESTION:

Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:

To write a Java program that defines a method cube(int x) which internally calls another method square(int x) to compute the cube of a number using the formula:
cube = x * square(x).

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a method square(int x) that returns the value of x * x.
4. Create another method cube(int x) that:</BR>
     - Calls square(x)</BR>
     - Multiplies the result by x</BR>
     - Returns the final cube value.</BR>
5. In the main method:</BR>
     - Read or assign a value for x</BR>
     - Call the cube(x) method</BR>
6. Display the cube.
7. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    static int square(int x)
    {
        return x*x;
    }
    static int cube(int x)
    {
        return x*square(x);
    }
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println(cube(n));
    }
}
```

## OUTPUT:

<img width="282" height="90" alt="image" src="https://github.com/user-attachments/assets/95f3e522-3a04-4365-90f4-029903bdd3d7" />

## RESULT:

The program successfully calculates the cube of a given number by calling the square() method from within the cube() method, demonstrating method calling and reuse in Java.

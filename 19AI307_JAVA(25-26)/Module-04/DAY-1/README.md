# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:

To understand what happens when the toString() method is called on a null Integer object in Java, and to learn how to safely prevent a NullPointerException by using proper null checks.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare an Integer object.
4. Assign null to the Integer object (directly or through input conditions).
5. Try to call the .toString() method on the Integer object.
6. Java will throw a NullPointerException because calling methods on a null reference is not allowed.
7. To prevent this exception:
    - Check if the Integer object is not null before calling .toString().
    - If it is null, handle it using: An if condition, or A try–catch block.
8. Display a safe output message when the object is null.
9. End the program.

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
        Integer num = null;
        try
        {
            if (sc.hasNextInt())
            {       
                num = sc.nextInt();     
            }
            if (num == null)
            {
                System.out.println("Null Integer");
            } 
            else
            {
                System.out.println(num.toString());
            }

        }
        catch(Exception e)
        {
            System.out.println("Error occurred");
        }
    }
}
```

## OUTPUT:

<img width="464" height="233" alt="image" src="https://github.com/user-attachments/assets/a7a44074-d309-4c95-88ba-f1dbae543b6c" />

## RESULT:

Calling the .toString() method on a null Integer object results in a NullPointerException.
By performing a null check before calling methods on the object, or by handling it using a try–catch block, the exception can be prevented, ensuring the program runs safely.

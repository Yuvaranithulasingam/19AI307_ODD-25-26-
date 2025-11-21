# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2.
Note : Read the threadname from the User. set the priority as 4 for t1 and set the priority as 2 for t2

## AIM:

To write a Java program that sets the name and priority of two threads (t1 and t2).
Thread names are taken from the user.
Set priority 4 for t1 and 2 for t2.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two thread names from the user:
    - First name → for thread t1
    - Second name → for thread t2
4. Create two Thread objects using the names.
5. Set priorities:
    - t1 → priority 4
    - t2 → priority 2
6. Print the thread names and their priorities.
7. Start both threads to demonstrate execution.
8. End the program.

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
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        System.out.println(t1);
        System.out.println(t2);
        sc.close();
    }
}
```

## OUTPUT:

<img width="775" height="193" alt="image" src="https://github.com/user-attachments/assets/c4fa0179-3559-4197-a92f-616b22d788e9" />

## RESULT:

The program successfully reads the thread names from the user, assigns the names to threads t1 and t2, sets the priority of t1 to 4 and t2 to 2, and displays the updated thread details.

# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:

To demonstrate the concept of stream chaining in Java by creating a BufferedReader object wrapped over an InputStreamReader, which is further wrapped over System.in, and reading input efficiently from the user.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BufferedReader object by wrapping it around an InputStreamReader that reads from System.in.
4. Display a message asking the user to enter some text.
5. Use the readLine() method to read the input string.
6. Print the user-entered text back to the console.
7. Close the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
public class ChainingStreamsDemo
{
    public static void main(String[] args)
    {
        try
        {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            String name = br.readLine();
            String age = br.readLine();
            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);
        }
        catch (IOException e)
        {
            e.printStackTrace();
        }
    }
}
```

## OUTPUT:

<img width="557" height="242" alt="image" src="https://github.com/user-attachments/assets/b4d174a2-8d75-49f7-b903-c829ca7e3405" />

## RESULT:

The program successfully demonstrates chaining of streams and reads input using
BufferedReader → InputStreamReader → System.in, then prints the entered text.

# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:

Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:

To write a Java program that collects a user’s name, age, and email address, and writes the information into a file named userdata.txt in a structured and readable format.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read user inputs.
4. Ask the user to enter:
    - Name
    - Age
    - Email
5. Open a FileWriter or BufferedWriter to write data into userdata.txt.
6. Close the writer.
7. Display a success message.
8. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.io.*;
import java.util.*;
public class UserDataWriter
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int age = Integer.parseInt(sc.nextLine());
        String email = sc.nextLine();
        try (PrintWriter pw = new PrintWriter("userdata.txt"))
        {
            pw.println("User Information");
            pw.println("================");
            pw.println("Name  : " + name);
            pw.println("Age   : " + age);
            pw.println("Email : " + email);
        }
        catch (IOException e)
        {
            e.printStackTrace();
        }
        System.out.println("User Information");
        System.out.println("================");
        System.out.println("Name  : " + name);
        System.out.println("Age   : " + age);
        System.out.println("Email : " + email);
    }
}
```

## OUTPUT:

<img width="666" height="197" alt="image" src="https://github.com/user-attachments/assets/2889a189-03a3-43a9-b95b-8c3e7cd920b8" />

## RESULT:

User data was successfully collected (name, age, email) and written into the file userdata.txt in a structured format. The program also displayed the same formatted information on the screen.

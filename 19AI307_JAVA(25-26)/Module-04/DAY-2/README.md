# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

## AIM:

To write a Java program that simulates a centralized Print Spooler Manager using the Singleton design pattern such that only one instance controls all print job submissions. For every print job submitted by any department, the total queue count should be incremented and displayed.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Singleton class PrintSpooler:
     - Declare a private static instance of the class.
     - Create a private constructor.
     - Provide a public getInstance() method to return the same instance every time.
     - Maintain a private counter for total print jobs.
     - Create a method submitJob(String dept) to:
          - increment the counter
          - print the department name and updated job count.
4. In the Main class:
     - Read the number of print jobs n.
     - For each job:
         - Read the department name.
         - Get the Singleton instance.
         - Call submitJob(department).
5. Display output for each job submission.
6. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
class PrintSpoolerManager
{
    private static PrintSpoolerManager instance; 
    private int jobCount; 
    private PrintSpoolerManager()
    {
        jobCount = 0;
    }
    public static PrintSpoolerManager getInstance()
    {
        if (instance == null)
        {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }
    public int submitJob(String department)
    {
        jobCount++;
        return jobCount;
    }
}

public class Main
{
    public static void main(String[] args)
{
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++)
        {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance(); 
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```

## OUTPUT:

<img width="1111" height="328" alt="image" src="https://github.com/user-attachments/assets/60f69e39-e33a-4793-8a5a-f906f05a8c11" />

## RESULT:

The program successfully demonstrates the Singleton design pattern.
Only one instance of the PrintSpooler manages all print job submissions, preserving the job count across all departments.

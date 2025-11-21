# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

## AIM:

To write a Java program that synchronizes the deposit() method in a BankAccount class and simulates concurrent deposits using multiple threads, ensuring the final balance is updated correctly without race conditions.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class BankAccount with:
     - A private variable balance.
     - A synchronized deposit(int amount) method that adds the amount to the balance.
     - A method getBalance() to return the final balance.
4. In the main() method:
     - Read the number of deposits (n).
     - Read n deposit amounts from the user.
     - For each amount, create a thread that calls deposit().
     - Start all threads.
     - Join all threads to ensure all deposits complete before printing result.
5. Display the final balance.
6. Stop the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.Scanner;
class BankAccount
{
    private int balance = 0;
    public synchronized void deposit(int amount)
    {
        balance += amount;
    }
    public int getBalance()
    {
        return balance;
    }
}

public class BankDepositSimulation
{
    public static void main(String[] args) throws InterruptedException
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  
        int[] deposits = new int[n];
        for (int i = 0; i < n; i++)
        {
            deposits[i] = sc.nextInt();
        }
        BankAccount account = new BankAccount();
        Thread[] threads = new Thread[n];
        for (int i = 0; i < n; i++)
        {
            int amount = deposits[i];
            threads[i] = new Thread(() -> {
                account.deposit(amount);
            });
            threads[i].start();
        }
        for (int i = 0; i < n; i++)
        {
            threads[i].join();
        }
        System.out.println("Final Balance: " + account.getBalance());
    }
}
```

## OUTPUT:

<img width="539" height="397" alt="image" src="https://github.com/user-attachments/assets/97d9adc6-1b00-4185-b422-c774cd161ded" />

## RESULT:

The program executed successfully. Multiple threads deposited amounts into the
shared BankAccount object, and synchronization ensured correct updates.


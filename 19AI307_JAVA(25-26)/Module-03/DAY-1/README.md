# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
finalPrice = purchaseWeight * (goldRatePerGram - discount)
For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:

To write a Java program using inheritance where a base class Customer stores details like customerId, name, and purchaseWeight. Two derived classes — RegularCustomer and PremiumCustomer — calculate the final payable amount based on discounts:
      RegularCustomer → 2% discount on gold rate per gram</br>
      PremiumCustomer → 5% discount + 1% cashback on final price</br>
The program should accept gold rate per gram at runtime and display the final amount for each customer.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create the base class Customer with:</br>
        - customerId</br>
  	     - name</br>
        - purchaseWeight</br>
  	     - Constructor to initialize these values</br>
  	     - A method calculatePrice() (to be overridden in child classes)</br>
4. Create subclass RegularCustomer:</br>
        - Override calculatePrice()</br>
        - Apply 2% discount on gold rate per gram</br>
        - Calculate finalPrice = purchaseWeight × (goldRatePerGram − discount)</br>
5. Create subclass PremiumCustomer:</br>
        - Override calculatePrice()</br>
        - Apply 5% discount</br>
        - After calculating finalPrice, compute cashback = 1% of finalPrice</br>
6. In the main method:</br>
        - Get goldRatePerGram from user input</br>
        - Create objects for RegularCustomer and PremiumCustomer</br>
        - Call calculatePrice() for each object</br>
        - Display the final price and cashback (only for premium)</br>
7. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber: 212222110057 

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;
class Customer
{
    String customerId, name;
    double purchaseWeight, goldRatePerGram;
    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram)
    {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }
    double getDiscountRate()
    {
        return 0;
    }
    double calculateFinalPrice()
    {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }
    void display()
    {
        // Base class won't display anything directly
    }
}

class RegularCustomer extends Customer
{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram)
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    double getDiscountRate()
    {
        return 2;
    }
    void display()
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer
{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram)
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    double getDiscountRate()
    {
        return 5;
    }
    double getCashback()
    {
        return calculateFinalPrice() * 0.01;
    }
    void display()
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();  
        String customerId = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double purchaseWeight = sc.nextDouble();
        double goldRatePerGram = sc.nextDouble();
        Customer customer = null;
        if (type.equalsIgnoreCase("Regular"))
        {
            customer = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        }
        else if (type.equalsIgnoreCase("Premium"))
        {
            customer = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        }
        else
        {
            System.out.println("Invalid customer type.");
            System.exit(0);
        }
        customer.display();
    }
}
```

## OUTPUT:

<img width="729" height="586" alt="image" src="https://github.com/user-attachments/assets/94047e65-2287-4ad9-a975-ae9d42c2591f" />

## RESULT:

Thus, the program successfully demonstrates inheritance, method overriding, and different discount rules for Regular and Premium customers. It calculates and displays:
Final amount payable by RegularCustomer
Final amount payable by PremiumCustomer
Cashback amount for PremiumCustomer

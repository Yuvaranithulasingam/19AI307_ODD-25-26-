# Ex.No:3(b) POLYMORPHISM

## QUESTION:

Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

## AIM:

To write a Java program that demonstrates method overriding using inheritance.
Create a base class Animal with a method sound(), and subclasses Dog, Cat, and Cow, each overriding the sound() method to display their specific sounds.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Animal with a method sound() that prints a general message.
4. Create subclasses Dog, Cat, Cow that override the sound() method.
5. In each subclass, implement the sound() method to print the specific sound:
      - Dog → “Dog barks”
      - Cat → “Cat meows”
      - Cow → “Cow moos”
6. In the main() method:
      - Create objects of Dog, Cat, and Cow.
      - Call the overridden sound() method using each object.
      - Display the output.
7. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.Scanner;
class Animal
{
    public void sound()
    {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal
{
    public void sound()
    {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal
{
    public void sound()
    {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal
{
    public void sound()
    {
        System.out.println("Cow moos");
    }
}

public class AnimalSound
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        Animal a;
        String input = scanner.nextLine().trim().toLowerCase();
        switch (input)
        {
            case "dog":
                a = new Dog();
                break;
            case "cat":
                a = new Cat();
                break;
            case "cow":
                a = new Cow();
                break;
            default:
                System.out.println("Unknown animal");
                scanner.close();
                return;
        }
        a.sound();
        scanner.close();
    }
}
```

## OUTPUT:

<img width="416" height="219" alt="image" src="https://github.com/user-attachments/assets/a8ce77d6-bb65-4d10-8ae4-83bfa015120e" />

## RESULT:

Thus, the Java program successfully demonstrates method overriding, where the subclasses Dog, Cat, and Cow provide their own implementations of the sound() method, replacing the version defined in the base class Animal.

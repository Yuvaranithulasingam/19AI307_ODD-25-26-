# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

You need to clone documents. Implement the Prototype Pattern to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone.

## AIM:

To implement the Prototype Design Pattern in Java by creating a Document class that supports cloning. The program should take user input for the document’s title and content, create a clone of the document, and print both the original and the cloned object to demonstrate that the prototype pattern works.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Document class that implements the Cloneable interface.
4. Define two attributes: title and content.
5. Override the clone() method to return a copy of the current object.
6. In the main() method:
     - Accept user input for title and content.
     - Create a Document object with these values.
     - Clone the document using the clone() method.
9. Print the original document details.
10. Print the cloned document details.
11. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.Scanner;
class Document implements Cloneable
{
    String title, content;
    Document(String title, String content)
    {
        this.title = title;
        this.content = content;
    }
    public Document clone()
    {
        try
        {
            return (Document) super.clone();
        }
        catch (CloneNotSupportedException e)
        {
            return null;
        }
    }
    void display(String label)
    {
        System.out.println(label + ": " + title + " - " + content);
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        String title = scanner.nextLine();
        String content = scanner.nextLine();
        Document original = new Document(title, content);
        Document clone = original.clone();
        original.display("Original");
        clone.display("Cloned");
    }
}
```

## OUTPUT:

<img width="1202" height="234" alt="image" src="https://github.com/user-attachments/assets/cdc26773-ca8a-499d-b902-bbbf021cf543" />

## RESULT:

The program successfully demonstrates the Prototype Pattern by creating a duplicate of a document object.

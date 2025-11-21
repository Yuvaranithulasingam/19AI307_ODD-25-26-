# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:

To implement the concept of Composition in Java by creating a system where a Library contains multiple Book objects.
In composition, the contained objects (Books) cannot exist without the container object (Library), meaning their lifecycle is tied to the Library.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Book with attributes like title and author.
4. Create a class Library that:
     - Contains an ArrayList of Book objects.
     - Creates Book objects inside the Library (not from outside).
     - Provides a method to add books and another to display them.
5. In the main() method:
     - Create a Library object.
     - Add multiple books to it using the Library's method.
     - Call the display method to show book details.
6. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
public class CompositionExample
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++)
        {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }
        library.showBooks();
        sc.close();
    }
}

class Book
{
    private String title;
    private String author;
    Book(String title, String author)
    {
        this.title = title;
        this.author = author;
    }
    String getDetails()
    {
        return "- " + title + " by " + author;
    }
}

class Library
{
    private List<Book> books;
    Library()
    {
        books = new ArrayList<>();
    }
    void addBook(String title, String author)
    {
        books.add(new Book(title, author));
    }
    void showBooks()
    {
        System.out.println("Books in Library:");
        for (Book b : books)
            System.out.println(b.getDetails());
    }
}
```

## OUTPUT:

<img width="1065" height="589" alt="image" src="https://github.com/user-attachments/assets/64296bfd-24d0-43e2-aa31-2b0264c824ce" />

## RESULT:
The program successfully demonstrates Composition in Java by showing that a Library owns its Book objects.
Books are created and managed only inside the Library, proving that they cannot exist independently.
The Library displays all the books it contains, validating the composition relationship.

# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).
<img width="463" height="277" alt="image" src="https://github.com/user-attachments/assets/f07362a4-b64b-4afb-b05a-f7e293a7c5e0" />

## AIM:
To implement the concept of Composition in Java by creating a Library class that owns and manages multiple Book objects, ensuring that books cannot exist outside the library.


## ALGORITHM :
1.Start the program.

2.Import the necessary package java.util.

3.Create a class Book to hold title and author.

4.Create a class Library that contains a list of Book objects.

5.Inside Library, create books within the addBook() method (composition).

6.In the main method, read input from user.

7.Add books to the library.

8.Display all stored books.

9.End the program.	





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Selvamuthu Kumaran V
RegisterNumber: 212222040151 
*/
```

## SOURCE CODE:
```java
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>(); // Library owns the books (composition)

    public void addBook(String title, String author) {
        Book b = new Book(title, author); // Book created inside Library
        books.add(b);
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}
```




## OUTPUT:
<img width="1287" height="577" alt="image" src="https://github.com/user-attachments/assets/34f2cbdd-e122-4979-845a-01871b40d5cd" />




## RESULT:
The program successfully demonstrated composition in Java, where the Library class creates and owns Book objects, ensuring they do not exist independently.

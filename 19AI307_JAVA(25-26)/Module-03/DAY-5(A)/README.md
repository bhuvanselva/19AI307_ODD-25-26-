# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

## AIM:
To write a Java program to check whether a given number is a Palindrome or not using Inner Class.

## ALGORITHM :
Create an outer class with a private variable.

Define an inner class inside it with a method to access the outer variable.

In main(), create an object of the outer class.

Use it to create an object of the inner class.

Call the inner class method.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();

        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```
## OUTPUT:

<img width="1223" height="347" alt="image" src="https://github.com/user-attachments/assets/7e5a676c-243c-4472-9dc1-bb7377717c31" />

## RESULT:
The program successfully accesses and prints data from the inner class using the outer class.



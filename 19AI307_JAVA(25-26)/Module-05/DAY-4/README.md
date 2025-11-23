# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:
To read a thread name from the user and display the current thread’s name and priority.

## ALGORITHM :
Read the thread name from the user.

Get the reference of the current thread using Thread.currentThread().

Set the name of the current thread using setName().

Retrieve the thread’s name and priority using getName() and getPriority().

Display both values.


## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadInfoExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String threadName = scanner.nextLine();

        Thread t = new Thread(() -> {}, threadName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());

        System.out.println(t);

        scanner.close();
    }
}
```

## OUTPUT:

<img width="1313" height="265" alt="image" src="https://github.com/user-attachments/assets/3ffa1956-fdb3-443f-8686-abfdffb48d6c" />


## RESULT:
The program successfully reads the thread name from the user and displays the current thread’s name and priority.

# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program that reads two integers, performs division, and handles the ArithmeticException when division by zero occurs.

## ALGORITHM :
Start the program.

Read two integers from the user: dividend and divisor.

Use a try block to perform the division.

If the divisor is zero, an ArithmeticException will occur.

Catch the exception and display an appropriate message.

If no exception occurs, print the division result.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String args[]){
        Scanner input=new Scanner(System.in);
        try{
            int a=input.nextInt();
            int b=input.nextInt();
            System.out.print("Result: "+(a/b));
        }
        catch(ArithmeticException e){
            System.out.print("Error: Division by zero");
        }
    }
}
```
## OUTPUT:
<img width="1262" height="276" alt="image" src="https://github.com/user-attachments/assets/617da354-a3d9-4270-a9cb-61d3b3423a74" />

## RESULT:
The program successfully performs division of two integers and handles division-by-zero errors using exception handling.

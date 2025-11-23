# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write character data into a file using the FileWriter class in Java.

## ALGORITHM :
Import java.io.FileWriter and java.io.IOException.

Take user input using Scanner.

Create a FileWriter object with the desired file name.

Use write() method to write text into the file.

Close the FileWriter and handle exceptions using try-catch.


## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008 
*/
```

## SOURCE CODE:
```
import java.io.*;

public class FileWriteExample {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            String filename = br.readLine();
            String content = br.readLine();

            FileWriter fw = new FileWriter(filename);
            fw.write(content);
            fw.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```


## OUTPUT:

<img width="1239" height="395" alt="image" src="https://github.com/user-attachments/assets/9cada0f7-f0a2-4bce-ad9f-2c371f5acd89" />


## RESULT:
The program successfully writes the entered text into output.txt using FileWriter.

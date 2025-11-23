# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

## AIM:
To count and display the total number of characters in a file using FileReader.

## ALGORITHM :

Ask the user for the file name.

Open the file using FileReader.

Read each character one by one until the end of the file.

Increment a counter for each character read.

Display the total character count.


## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.io.*;

public class FileCharacterCount {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

            String text = br.readLine();

            String fileName = "output.txt";

            try (FileWriter fw = new FileWriter(fileName)) {
                if (text != null) {
                    fw.write(text);
                }
            }

            int charCount = 0;
            try (FileReader fr = new FileReader(fileName)) {
                while (fr.read() != -1) {
                    charCount++;
                }
            }

            System.out.println("Number of characters written to the file: " + charCount);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}

```





## OUTPUT:

<img width="1271" height="303" alt="image" src="https://github.com/user-attachments/assets/9106ffe8-d84b-4425-9ee2-9d8599d5fe54" />


## RESULT:
The program successfully reads the file and prints the total number of characters present in it.

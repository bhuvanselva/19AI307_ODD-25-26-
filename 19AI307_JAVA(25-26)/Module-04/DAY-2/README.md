# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

Input Format: n [Player1] [Player2] ... First line: Integer n – number of players turning on consoles Next n lines: Each line contains the player's name. Output Format: For each player, print: [PlayerName] accessed Master Power Switch. Total accesses so far: [count]



## AIM:
To implement a Singleton design pattern in Java so that only one instance of the master power switch exists. Each player accessing the switch should increment a shared global access count.

## ALGORITHM :
Start the program.

Create a Singleton class MasterSwitch with: a private static instance variable a private constructor a public static getInstance() method a counter 
variable to track accesses

Read the number of players n.

For each player, read their name.

Using getInstance(), access the Singleton object.

Increment the access count and print the player's access message.

End the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance;
    private  int accesscount = 0;
    private MasterPowerSwitch(){}
    public static MasterPowerSwitch getInstance(){
        if(instance == null){
            instance = new MasterPowerSwitch();
        }
        return instance;
    }
    
    public int logAccess(){
        return (++accesscount);
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}
```
## OUTPUT:
<img width="1262" height="266" alt="image" src="https://github.com/user-attachments/assets/6b70a2c0-cbec-4a46-bba1-70a483728a9f" />

## RESULT:
The program was executed successfully. A Singleton master power switch object was created, ensuring only one shared instance. Each player accessed the same master switch, and the global access count increased correctly for every access.



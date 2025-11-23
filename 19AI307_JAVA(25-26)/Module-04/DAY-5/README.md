# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Implement the Observer pattern for a dating app MatchIt. MatchItServer is the Subject; User is the Observer. Each User subscribes with a preference (e.g., Gamer, PetLover, Bookworm). When a new person signs up with a type, notify only users whose preference matches that type. Each notified user prints a custom message.

## AIM:
To implement the Observer design pattern where MatchItServer notifies only those User observers whose preference matches the type of each newly joined user.



## ALGORITHM :
Create a User class that implements an Observer interface; store name and preference and implement an update(newUserName, type) method that prints the custom message.
Create MatchItServer as the Subject with methods to register(User), remove(User) and notify(type, newUserName). Maintain a list of registered users.
Read n and register n users (store each user’s preference).
Read m. For each signup (newUserName, type): print the "New User Joined..." line.
Call notify(type, newUserName) — iterate over registered users and for each user whose preference.equals(type) call update(...).
End program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Observer {
    void notify(String name, String type);
    String getPreference();
}

class User implements Observer {
    private String name;
    private String preference;
    
    public User(String name,String type){
        this.name=name;
        this.preference=type;
    }
    public String getName(){
        return name;
    }
    public String getPreference(){
        return preference;
    }
    public void notify(String Name,String type){
        if(type.equalsIgnoreCase(preference)){
            System.out.println(name+": Omg! A new "+type+"? MatchIt, you know me too well! (It’s "+Name+"!)");
        }
    }
    
}

class MatchItServer {
    private List<Observer> subscribers=new ArrayList<>();
    
    public void register(User o){
        subscribers.add(o);
    }
    
    public void newSignup(String name,String type){
        System.out.println("New User Joined: "+name+" - Type: "+type);
        for(Observer o : subscribers){
            o.notify(name,type);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] userInfo = sc.nextLine().split(" ");
            server.register(new User(userInfo[0], userInfo[1]));
        }

        int m = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < m; i++) {
            String[] newUser = sc.nextLine().split(" ");
            server.newSignup(newUser[0], newUser[1]);
        }
    }
}

```



## OUTPUT:

<img width="1216" height="408" alt="image" src="https://github.com/user-attachments/assets/111d7746-9f81-4b57-8100-7e5d221be0ab" />


## RESULT:
The program executes successfully. For every new signup, the server announces the new user and then notifies only those users whose saved preference matches the signup’s type. Each notified user prints the expected personalized message. Non-matching users do not receive notifications.

# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Write a Java program to demonstrate Composition, where one class contains another class as a part of it. Create an Engine class and a Car class. The Car class should contain an Engine object and use it to start the car.

## AIM:
To write a Java program that demonstrates composition by creating a Car class that has an Engine object. When the car starts, the engine is also started, showing strong ownership between the two objects.

## ALGORITHM :
Start the program.

Create an Engine class with a method start() that prints a message.

Create a Car class that contains a private Engine object.

Initialize the Engine object inside the Car constructor.

Define a startCar() method in Car to call the engine.start() method.

In main(), create an object of the Car class.

Call the startCar() method to demonstrate composition.

End the program.	


## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Bhuvaneshwari S
RegisterNumber: 212222220008
*/
```

## SOURCE CODE:
```
// Engine class (part of Car)
class Engine {
    void start() {
        System.out.println("Engine started.");
    }
}

// Car class uses Composition
class Car {
    private Engine engine;  // Car HAS-A Engine

    Car() {
        engine = new Engine();  // Engine created inside Car
    }

    void startCar() {
        engine.start();
        System.out.println("Car is running.");
    }
}

public class CompositionDemo {
    public static void main(String[] args) {
        Car car = new Car();
        car.startCar();
    }
}
```
## OUTPUT:
<img width="440" height="81" alt="image" src="https://github.com/user-attachments/assets/43e1d721-9a0e-419e-9241-8c070d88b47a" />


## RESULT:
The program was executed successfully. It demonstrated the concept of composition, where a Car object contains an Engine object. When the car was started, the engine started first, showing strong dependency between the two objects

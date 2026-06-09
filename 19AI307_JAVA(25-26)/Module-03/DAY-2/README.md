# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

## AIM:
To write a Java program that demonstrates method overriding using inheritance and polymorphism.

## ALGORITHM :
1.	Create a base class Animal with a method sound().
2.	Create subclasses Dog, Cat, and Cow that extend Animal.
3.	Override the sound() method in each subclass to print specific sounds.
4.	In main(), use an Animal reference to point to each subclass object.
5.	Call the sound() method to demonstrate runtime polymorphism.


## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: GOKUL PRAKASH M
RegisterNumber: 212223240041
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    void sound() {
        System.out.println("Unknown animal");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    @Override
    void sound() {
        System.out.println("Cow moos");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();
            if (input.isEmpty()) continue;

            Animal a;
            switch(input.toLowerCase()) {
                case "dog": a = new Dog(); break;
                case "cat": a = new Cat(); break;
                case "cow": a = new Cow(); break;
                default: a = new Animal();
            }
            a.sound();
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="1215" height="500" alt="image" src="https://github.com/user-attachments/assets/d08ba277-f28b-4af5-9ac8-8a8c71761ca5" />

## RESULT:
The program successfully demonstrates method overriding, showing different behaviors of the sound() method for different animal subclasses.




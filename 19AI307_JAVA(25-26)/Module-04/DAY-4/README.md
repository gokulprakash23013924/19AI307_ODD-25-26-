# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To implement the Factory Design Pattern for creating different types of notifications and invoke the appropriate notifyUser() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an interface Notification.
4.  Declare the method notifyUser() in the interface.
4.  Create a class EmailNotification that implements the Notification interface.
4.  Implement the notifyUser() method to display an email notification message.
4.  Create a class SMSNotification that implements the Notification interface.
4.  Implement the notifyUser() method to display an SMS notification message.
4.  Create a class PushNotification that implements the Notification interface.
4.  Implement the notifyUser() method to display a push notification message.
4.  Create a class NotificationFactory.
4.  Define a method createNotification(String type).
4.  Check the notification type provided by the user.
4.  If the type is "email", create and return an EmailNotification object.
4.  If the type is "sms", create and return an SMSNotification object.
4.  If the type is "push", create and return a PushNotification object.
4.  If the type is invalid, return null.
4.  Define the main() method.
4.  Create a Scanner object to read input from the user.
4.  Create an object of NotificationFactory.
4.  Repeatedly read notification types from the user.
4.  If the input is "exit", terminate the loop.
4.  Call createNotification() to obtain the appropriate notification object.
4.  If a valid object is returned, invoke its notifyUser() method.
4.  Otherwise, display an invalid notification type message.
4.  End





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: GOKUL PRAKASH M
RegisterNumber: 212223240041
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface Notification {
    void notifyUser();
}
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}
class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}
class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}
class NotificationFactory {
    public Notification createNotification(String type) {
        if (type.equalsIgnoreCase("email")) {
            return new EmailNotification();
        } else if (type.equalsIgnoreCase("sms")) {
            return new SMSNotification();
        } else if (type.equalsIgnoreCase("push")) {
            return new PushNotification();
        }
        return null;
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        NotificationFactory factory = new NotificationFactory();

        while (true) {

            String input = sc.nextLine();

            if (input.equalsIgnoreCase("exit"))
                break;

            Notification n = factory.createNotification(input);

            if (n != null)
                n.notifyUser();
            else
                System.out.println("Invalid notification type: " + input);
        }
    }
}
```




## OUTPUT:

<img width="489" height="189" alt="image" src="https://github.com/user-attachments/assets/68ca5268-83ec-45f0-9c73-9b6992aff557" />



## RESULT:
Thus, the program to implement the Factory Design Pattern for creating different types of notifications and invoking the corresponding notifyUser() method was implemented and executed successfully.

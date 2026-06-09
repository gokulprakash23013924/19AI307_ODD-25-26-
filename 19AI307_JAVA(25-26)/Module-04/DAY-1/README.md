# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To demonstrate the behavior of calling .toString() on a null Integer object and handle the resulting exception using exception handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare an Integer object intVal and initialize it to null.
3. Create a Scanner object to read input from the user.
3. Read an integer value from the user and assign it to intVal.
3. Check whether the entered value is 0.
3. If the value is 0, assign null to intVal.
3. Use a try block to call the toString() method on intVal.
3. If intVal is not null, display its string representation.
3. If intVal is null, a NullPointerException is generated.
3. Catch the exception using a catch block.
3. Display the message "Null Integer".
3. Terminate the program.
3. End





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: GOKUL PRAKASH M
RegisterNumber: 212223240041
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
import java.lang.NullPointerException;
public class Main{
    public static void main(String[] args){
        Integer intVal = null;
        Scanner sc = new Scanner(System.in);
        intVal = sc.nextInt();
        intVal = intVal==0?null:intVal;
        try{
            System.out.println(intVal.toString());
        }catch(NullPointerException e){
            System.out.println("Null Integer");
        }
    }
}
```


## OUTPUT:

<img width="389" height="180" alt="image" src="https://github.com/user-attachments/assets/4a532c4d-7e83-4d5b-a74f-ef3390eadb44" />



## RESULT:
Thus, the program to demonstrate the behavior of calling .toString() on a null Integer object and prevent program termination using exception handling was implemented and executed successfully. It was observed that invoking .toString() on a null object throws a NullPointerException, which can be handled using a try-catch block.

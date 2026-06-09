# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to replace each space with a hyphen.



## AIM:
To write a Java program that replaces all spaces in a given string with hyphens (-).

## ALGORITHM :
1.	Start the program and create a Scanner object.
2.	Read a string input from the user.
3.	Use the replace() method to replace all spaces with -.
4.	Display the modified string.
5.	End the program.




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

public class ReplaceSpace {
    public static String replaceSpaces(String str) {
        return str.replace(' ', '-');
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        String result = replaceSpaces(input);
        System.out.println("Modified string: " + result);
    }
}

```





## OUTPUT:
<img width="1145" height="420" alt="image" src="https://github.com/user-attachments/assets/c831a76c-b77a-4c75-82de-8b9c087033d2" />



## RESULT:
The program successfully replaces all spaces in the input string with hyphens.




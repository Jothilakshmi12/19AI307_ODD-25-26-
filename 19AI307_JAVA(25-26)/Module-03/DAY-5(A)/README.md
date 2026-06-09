# Ex.No:3(E) INNER CLASS


## AIM:
To write a Java program that defines an enum Department with constants CS, IT, and ECE, each storing its full form using a constructor, and displays the corresponding full form based on user input.

## ALGORITHM :

1.Start the program.

2.Define an enum Department with constants CS, IT, and ECE, each having a full form string.

3.Read the department code from the user.

4.Compare the input with the enum constants and display the corresponding full form if valid.

5.If the input is invalid, display an error message and stop the program.



## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by:  Jothilakshmi Palani
RegisterNumber:  212223110017
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

enum Department {
    CS("Computer Science"),
    IT("Information Technology"),
    ECE("Electronics and Communication Engineering");

    private String fullForm;

    Department(String fullForm) {
        this.fullForm = fullForm;
    }

    public String getFullForm() {
        return fullForm;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.nextLine();

        try {
            Department dept = Department.valueOf(input.toUpperCase());
            System.out.println("Full Form: " + dept.getFullForm());
        } 
        catch (IllegalArgumentException e) {
            System.out.println("Invalid department code entered.");
        }
    }
}
```






## OUTPUT:


<img width="1027" height="252" alt="image" src="https://github.com/user-attachments/assets/845bc9b6-7f7d-4327-930d-45e420894e23" />

## RESULT:

Thus, the program successfully uses an enum with a constructor to store department full forms and displays the appropriate full form or an error message based on the user's input.

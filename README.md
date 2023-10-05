# OOP ASSIGNMENT ONE
import java.util.Scanner;

public class LoginProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String correctUsername = "JOSEPH MBURU";
        String correctPassword = "JOE452";
        int attempts = 3;

        System.out.println("Welcome to the Login Program!");

        while (attempts > 0) {
            System.out.print("Enter your username: ");
            String username = scanner.nextLine();

            System.out.print("Enter your password: ");
            String password = scanner.nextLine();

            if (username.equals(correctUsername) && password.equals(correctPassword)) {
                System.out.println("Login successful!");
                break;
            } else {
                System.out.println("Login failed. You have " + (attempts - 1) + " attempts remaining.");
                attempts--;
            }
        }

        if (attempts == 0) {
            System.out.println("You've exceeded  maximum number of login attempts.Your  Account is locked!!!.");
        }

        scanner.close();
    }
}

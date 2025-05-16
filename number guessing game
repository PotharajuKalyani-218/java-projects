// Number guessing game using java
//code:
import java.util.Scanner;
import java.util.Random;

public class NumberGuessingGame {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        String playAgain;

        do {
            int numberToGuess = random.nextInt(100) + 1;
            int guess;
            int numberOfTries = 0;
            int maxTries = 5;
            boolean hasGuessedCorrectly = false;

            System.out.println("\nWelcome to the Number Guessing Game!");
            System.out.println("I'm thinking of a number between 1 and 100.");
            System.out.println("You have " + maxTries + " tries to guess it.");

            while (numberOfTries < maxTries) {
                System.out.print("Enter your guess: ");

                while (!scanner.hasNextInt()) {
                    System.out.println("That's not a valid number. Try again.");
                    scanner.next(); 
                    System.out.print("Enter your guess: ");
                }

                guess = scanner.nextInt();
                numberOfTries++;

                if (guess < 1 || guess > 100) {
                    System.out.println("Out of bounds! Please guess a number between 1 and 100.");
                } else if (guess < numberToGuess) {
                    System.out.println("Too low!");
                } else if (guess > numberToGuess) {
                    System.out.println("Too high!");
                } else {
                    hasGuessedCorrectly = true;
                    System.out.println("Congratulations! You guessed the number in " + numberOfTries + " tries.");
                    break;
                }

                if (numberOfTries < maxTries) {
                    System.out.println("You have " + (maxTries - numberOfTries) + " tries left.");
                }
            }

            if (!hasGuessedCorrectly) {
                System.out.println("You've used all your tries. The correct number was: " + numberToGuess);
            }

            System.out.print("Do you want to play again? (yes/no): ");
            scanner.nextLine(); 
            playAgain = scanner.nextLine().trim().toLowerCase();

        } while (playAgain.equals("yes"));

        System.out.println("Thanks for playing! Goodbye ");
        scanner.close();
    }
}

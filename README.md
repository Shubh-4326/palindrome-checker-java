# palindrome-checker-java
import java.util.Scanner;

public class PalindromeChecker {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a word or phrase: ");
        String input = scanner.nextLine();

        if (isPalindrome(input)) {
            System.out.println("✅ It is a palindrome.");
        } else {
            System.out.println("❌ It is not a palindrome.");
        }

        scanner.close();
    }

    public static boolean isPalindrome(String input) {
        // Remove all non-letter characters and convert to lowercase
        String cleaned = input.replaceAll("[^a-zA-Z]", "").toLowerCase();

        // Reverse the cleaned string
        String reversed = new StringBuilder(cleaned).reverse().toString();

        // Compare cleaned and reversed
        return cleaned.equals(reversed);
    }
}

OUTPUT : PS D:\Programming\Internship_prac> cd "d:\Programming\Internship_prac\" ; if ($?) { javac PalindromeChecker.java } ; if ($?) { java PalindromeChecker }
Enter a word or phrase: Hello World
? It is not a palindrome.
PS D:\Programming\Internship_prac> cd "d:\Programming\Internship_prac\" ; if ($?) { javac PalindromeChecker.java } ; if ($?) { java PalindromeChecker }
Enter a word or phrase: A man, a plan, a canal, Panama
? It is a palindrome.

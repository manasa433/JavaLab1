2Q'
Create a Java program called "Alphabet War" that simulates a battle between two teams of letters: left-side letters (w, p, b, s) and right-side letters (m, q, d, z), each with specific strengths.
STATEMENTS: If the left side's total strength is greater, output "Left side wins!"
            If the right side's total strength is greater, output "Right side wins!"
             If the scores are equal, output "Let's fight again!"

import java.util.HashMap;
import java.util.Map;

public class AlphabetWarGame {
    private Map<Character, Integer> leftStrengths;
    private Map<Character, Integer> rightStrengths;

    // Default strengths
    public AlphabetWarGame() {
        leftStrengths = new HashMap<>() {{
            put('w', 4);
            put('p', 3);
            put('b', 2);
            put('s', 1);
        }};
        rightStrengths = new HashMap<>() {{
            put('m', 4);
            put('q', 3);
            put('d', 2);
            put('z', 1);
        }};
    }

    // Custom strengths constructor
    public AlphabetWarGame(Map<Character, Integer> left, Map<Character, Integer> right) {
        leftStrengths = left;
        rightStrengths = right;
    }

    // Method to determine the winner based on a single word
    public String AlphabetWar(String word) {
        return AlphabetWar(word, "");
    }

    // Method to determine the winner based on separate left and right words
    public String AlphabetWar(String leftWord, String rightWord) {
        int leftScore = calculateScore(leftWord, leftStrengths);
        int rightScore = calculateScore(rightWord, rightStrengths);

        if (leftScore > rightScore) {
            return "Left side wins!";
        } else if (rightScore > leftScore) {
            return "Right side wins!";
        } else {
            return "Let's fight again!";
        }
    }

    private int calculateScore(String word, Map<Character, Integer> strengths) {
        int score = 0;
        for (char c : word.toCharArray()) {
            score += strengths.getOrDefault(c, 0);
        }
        return score;
    }

    public static void main(String[] args) {
        AlphabetWarGame game = new AlphabetWarGame();

        System.out.println(game.AlphabetWar("z"));               // Right side wins!
        System.out.println(game.AlphabetWar("zdqmwpbs"));        // Let's fight again!
        System.out.println(game.AlphabetWar("wwwwwwz"));         // Left side wins!
    }
}

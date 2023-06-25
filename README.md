# Repeating_Character

public class Main {
    public static int findFirstNonRepeatingChar(String s) {
        int[] charCount = new int[26]; 

        
        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            charCount[c - 'a']++;
        }

        
        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            if (charCount[c - 'a'] == 1) {
                return i;
            }
        }

        return -1; 
    }

    public static void main(String[] args) {
        String input = "abccdef";
        int index = findFirstNonRepeatingChar(input);
        System.out.println("Index of the first non-repeating character: " + index);
    }
}

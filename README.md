# CodeSpace
This repo is for 30 day javascript coding practice

1.3 Widget

USING KOTLIN--> https://github.com/mvmike/min-cal-widget.git

2.1 Create an Android app that uses Intent with button to create a page and passes values from one activity to another

KOTLIN--> https://github.com/souvikm3/ToDo

2.2 Button-->

For KOTLIN--> https://github.com/avisper/EasyCompoundButtonGroup.git

For JAVA--> https://github.com/krunalpatel3/Common-Components-Android.git

2.3 Create an Android-based application and use intent to send SMS.( CO4, CO5)

SMS--> https://github.com/souvikm3/ToDo

3.1 Create an Android application using Fragments.

KOTLIN---> https://github.com/souvikm3/YumHub

3.2 Implement building blocks for Android Application using different layouts such as linear, relative and absolute---> You can use my 3.1 link same thing use in layout

3.3 Design the Android application using menus and action bar

KOTLIN----> https://github.com/jacobras/ComposeActionMenu.git


/////////////////////////////
import java.util.Scanner;

public class LongestPalindromeCreator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String inputString = scanner.nextLine();

        String longestPalindrome = findLongestPalindrome(inputString);
        
        if (!longestPalindrome.isEmpty()) {
            System.out.println("Longest palindrome: " + longestPalindrome);
        } else {
            System.out.println("No palindrome found in the input string.");
        }
        
        scanner.close();
    }
    
    public static boolean isPalindrome(String s) {
        int left = 0;
        int right = s.length() - 1;
        while (left < right) {
            if (s.charAt(left) != s.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static String findLongestPalindrome(String inputString) {
        String longestPalindrome = "";
        
        for (int i = 0; i < inputString.length(); i++) {
            for (int j = i + 1; j <= inputString.length(); j++) {
                String substring = inputString.substring(i, j);
                if (isPalindrome(substring) && substring.length() > longestPalindrome.length()) {
                    longestPalindrome = substring;
                }
            }
        }
        
        return longestPalindrome;
    }
}




/////

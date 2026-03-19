package quiz;

import java.util.Scanner;

public class quizmaster {

    static Scanner sc = new Scanner(System.in);
    static int score = 0;

    public static void main(String[] args) {

        System.out.println("===== QUIZ APPLICATION =====");
        System.out.println("Select Category:");
        System.out.println("1. Sports");
        System.out.println("2. Technology");
        System.out.println("3. General Knowledge");

        int choice = sc.nextInt();

        switch (choice) {
            case 1:
                sports();
                break;
            case 2:
                technology();
                break;
            case 3:
                gk();
                break;
            default:
                System.out.println("Invalid choice");
        }

        System.out.println("\nFinal Score: " + score + " out of 10");
        feedback();
    }

    public static void askQuestion(String question, String[] options, String correct) {

        System.out.println("\n" + question);

        for (String option : options) {
            System.out.println(option);
        }

        String answer = sc.next().toUpperCase();

        if (answer.equals(correct)) {
            System.out.println("Correct");
            score++;
        } else {
            System.out.println("Wrong. Correct answer: " + correct);
        }
    }

    // SPORTS (10)
    public static void sports() {

        score = 0;

        System.out.println("\n--- Sports Quiz ---");

        askQuestion("Who is known as King of Football?",
                new String[]{"A. Ronaldo", "B. Messi", "C. Neymar", "D. Pele"}, "D");

        askQuestion("Cricket bat is made of?",
                new String[]{"A. Wood", "B. Willow Wood", "C. Plastic", "D. Glass"}, "B");

        askQuestion("National sport of India?",
                new String[]{"A. Cricket", "B. Football", "C. Tennis", "D. Hockey"}, "D");

        askQuestion("Players in a cricket team?",
                new String[]{"A. 11", "B. 10", "C. 12", "D. 9"}, "A");

        askQuestion("Olympics held every how many years?",
                new String[]{"A. 2", "B. 4", "C. 6", "D. 8"}, "B");

        askQuestion("Serena Williams plays which sport?",
                new String[]{"A. Basketball", "B. Tennis", "C. Cricket", "D. Hockey"}, "B");

        askQuestion("Little Master is?",
                new String[]{"A. Gavaskar", "B. Kohli", "C. Dhoni", "D. Rohit"}, "A");

        askQuestion("Messi belongs to?",
                new String[]{"A. Spain", "B. Brazil", "C. Argentina", "D. Portugal"}, "C");

        askQuestion("Wimbledon is related to?",
                new String[]{"A. Football", "B. Tennis", "C. Golf", "D. Cricket"}, "B");

        askQuestion("How many rings in Olympic symbol?",
                new String[]{"A. 4", "B. 5", "C. 6", "D. 7"}, "B");
    }

    // TECHNOLOGY (10)
    public static void technology() {

        score = 0;

        System.out.println("\n--- Technology Quiz ---");

        askQuestion("Father of Java?",
                new String[]{"A. Dennis Ritchie", "B. James Gosling", "C. Bill Gates", "D. Elon Musk"}, "B");

        askQuestion("Android development uses?",
                new String[]{"A. Python", "B. Java", "C. Swift", "D. C"}, "B");

        askQuestion("CPU stands for?",
                new String[]{"A. Central Process Unit", "B. Central Processing Unit", "C. Computer Unit", "D. None"}, "B");

        askQuestion("Java developed by?",
                new String[]{"A. Google", "B. Apple", "C. Sun Microsystems", "D. IBM"}, "C");

        askQuestion("HTML is used for?",
                new String[]{"A. Styling", "B. Structure", "C. Database", "D. AI"}, "B");

        askQuestion("Which is not a programming language?",
                new String[]{"A. Java", "B. Python", "C. HTML", "D. C++"}, "C");

        askQuestion("Binary system uses?",
                new String[]{"A. 0 and 1", "B. 1 and 2", "C. 2 and 3", "D. 0 and 2"}, "A");

        askQuestion("Which is an operating system?",
                new String[]{"A. Windows", "B. Java", "C. Python", "D. HTML"}, "A");

        askQuestion("RAM is?",
                new String[]{"A. Storage", "B. Memory", "C. Input", "D. Output"}, "B");

        askQuestion("Which is a database?",
                new String[]{"A. MySQL", "B. Java", "C. HTML", "D. CSS"}, "A");
    }

    // GK (10)
    public static void gk() {

        score = 0;

        System.out.println("\n--- General Knowledge Quiz ---");

        askQuestion("Capital of India?",
                new String[]{"A. Mumbai", "B. Delhi", "C. Chennai", "D. Kolkata"}, "B");

        askQuestion("Largest planet?",
                new String[]{"A. Earth", "B. Mars", "C. Jupiter", "D. Saturn"}, "C");

        askQuestion("National Anthem written by?",
                new String[]{"A. Gandhi", "B. Nehru", "C. Tagore", "D. Bose"}, "C");

        askQuestion("Longest river?",
                new String[]{"A. Ganga", "B. Nile", "C. Amazon", "D. Yamuna"}, "B");

        askQuestion("Currency of USA?",
                new String[]{"A. Euro", "B. Dollar", "C. Pound", "D. Yen"}, "B");

        askQuestion("Red Planet?",
                new String[]{"A. Venus", "B. Mars", "C. Jupiter", "D. Saturn"}, "B");

        askQuestion("Prime Minister of India?",
                new String[]{"A. Modi", "B. Gandhi", "C. Kejriwal", "D. Rahul"}, "A");

        askQuestion("National animal of India?",
                new String[]{"A. Lion", "B. Tiger", "C. Elephant", "D. Leopard"}, "B");

        askQuestion("Water formula?",
                new String[]{"A. CO2", "B. H2O", "C. O2", "D. H2"}, "B");

        askQuestion("Sun is a?",
                new String[]{"A. Planet", "B. Star", "C. Satellite", "D. Asteroid"}, "B");
    }

    public static void feedback() {

        System.out.println("\n--- Performance ---");

        if (score >= 8) {
            System.out.println("Excellent");
        } else if (score >= 5) {
            System.out.println("Good");
        } else {
            System.out.println("Needs Improvement");
        }
    }
}

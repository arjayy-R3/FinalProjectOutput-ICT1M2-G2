import java.util.InputMismatchException;
import java.util.Scanner;


public class FinalProjectOutput {


 public static final String RESET = "\033[0m";
 public static final String RED = "\033[0;31m";
 public static final String GREEN = "\033[0;32m";
 public static final String YELLOW = "\033[0;33m";
 public static final String BLUE = "\033[0;34m";
 public static final String CYAN = "\033[0;36m";
 public static final String WHITE = "\033[0;37m";
 public static final String BLACK_BACKGROUND = "\033[40m";
 public static final String GREY_BACKGROUND = "\033[47m";


 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 int mainChoice;


 showLoadingScreen();
 while (true) {
 clearConsole();
 System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " 🌟🌟🌟 MAIN MENU 🌟🌟🌟 " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 printCentered(RED + "1: Start" + RESET);
 printCentered(GREEN + "2: About Us" + RESET);
 printCentered(RED + "3: Exit" + RESET);
 System.out.println();
 printCentered(YELLOW + "Choice (1-3): " + RESET);
 System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 System.out.println("👇");
 try {
 mainChoice = scanner.nextInt();
 scanner.nextLine();
 if (mainChoice == 1) {
 handleStartMenu(scanner);
 } else if (mainChoice == 2) {
 clearConsole();
 System.out.println(CYAN + "👩💻 ABOUT US 👨💻" + RESET);
 System.out.println();
 System.out.println("➡️ Developed by:");
 System.out.println("➡️ GEMARINO, RAINE M.");
 System.out.println("➡️PONCE, CHRISTIAN");
 System.out.println("➡️REYES, ARJAY");
 System.out.println("➡️MEDALLA, CHRISTIAN");
 System.out.println("➡️DELA CRUZ, YOJ MITCHELL A.");
 System.out.println("➡️PABLO, REGINE");
 System.out.println(
 "In this program includes many contents like Start Menu, About Us, and Exit. And in the Start menu includes Calculator, Area and Circumference, Odd or Even, and the Conversion of millimeter. And in About Us includes our names and ofcourse whats inside our program. And lastly the exit, which ends the program.");


 System.out.println();
 printCentered(YELLOW + "Press Enter to return..." + RESET);
 scanner.nextLine();
 } else if (mainChoice == 3) {
 printAsciiArt(); // Call the ASCII art method here
 printCentered(RED + "Exiting program... Goodbye!" + RESET);
 scanner.close();
 return;
 } else {
 clearConsole();
 printCentered(RED + "X           X" + RESET);
 printCentered(RED + "  X       X  " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "       X      " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "  X        X " + RESET);
 printCentered(RED + "X            X" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 System.out.println(YELLOW + " Invalid Choice! Press [ENTER] and Choose (1-3)" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.nextLine();
 }
 } catch (InputMismatchException e) {
 clearConsole();
 printCentered(RED + "X           X" + RESET);
 printCentered(RED + "  X       X  " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "       X      " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "  X        X " + RESET);
 printCentered(RED + "X            X" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 System.out.println(YELLOW + " Invalid input! Numbers only. Press [ENTER]" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.next();
 scanner.nextLine();
 }
 }
 }


 private static void handleStartMenu(Scanner scanner) {
 while (true) {
 clearConsole();
 printCentered(BLUE + "╔════════════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " ⚙ START MENU ⚙ " + RESET);
 printCentered(BLUE + "╚════════════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 printCentered(GREEN + "1: Calculator" + RESET);
 printCentered(GREEN + "2: Area/Circumference" + RESET);
 printCentered(GREEN + "3: Odd/Even" + RESET);
 printCentered(GREEN + "4: Conversion" + RESET);
 printCentered(YELLOW + "5: Back" + RESET);
 printCentered(RED + "6: Exit" + RESET);
 System.out.println();
 printCentered(YELLOW + "Choice (1-6): " + RESET);
  System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 System.out.print("➡ ");
 try {
 int subChoice = scanner.nextInt();
 scanner.nextLine();
 if (subChoice == 1)
 handleCalculatorOperations(scanner);
 else if (subChoice == 2)
 handleAreaCircumference(scanner);
 else if (subChoice == 3)
 handleOddEven(scanner);
 else if (subChoice == 4)
 handleConversion(scanner);
 else if (subChoice == 5)
 return;
 else if (subChoice == 6) {
 printAsciiArt(); // Call the ASCII art method here
 printCentered(RED + "Exiting program..." + RESET);
 System.exit(0);
 } else {
 clearConsole();
 printCentered(RED + "X           X" + RESET);
 printCentered(RED + "  X       X  " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "       X      " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "  X        X " + RESET);
 printCentered(RED + "X            X" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 System.out.println(YELLOW + " Invalid Choice! Press [ENTER] and Choose (1-6)" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.nextLine();
 }
 } catch (InputMismatchException e) {
 clearConsole();
 printCentered(RED + "X           X" + RESET);
 printCentered(RED + "  X       X  " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "       X      " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "  X        X " + RESET);
 printCentered(RED + "X            X" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 System.out.println(YELLOW + " Invalid input! Numbers only. Press [ENTER]" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.next();
 scanner.nextLine();
 }
 }
 }


 private static void handleCalculatorOperations(Scanner scanner) {
 while (true) {
 clearConsole();
 printCentered(BLUE + "╔════════════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " 🧮 CALCULATOR 🧮 " + RESET);
 printCentered(BLUE + "╚════════════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 printCentered(GREEN + "1: Add (+)" + RESET);
 printCentered(GREEN + "2: Subtract (-)" + RESET);
 printCentered(GREEN + "3: Multiply (*)" + RESET);
 printCentered(GREEN + "4: Divide (/)" + RESET);
 printCentered(YELLOW + "5: Back" + RESET);
 System.out.println();
 printCentered(YELLOW + "Choice (1-5): " + RESET);
  System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 System.out.print("➡ ");
 try {
 int operation = scanner.nextInt();
 scanner.nextLine();
 if (operation == 5)
 return;
 if (operation < 1 || operation > 5) {
 clearConsole();
 printCentered(RED + "X           X" + RESET);
 printCentered(RED + "  X       X  " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "       X      " + RESET);
 printCentered(RED + "    X   X    " + RESET);
 printCentered(RED + "  X        X " + RESET);
 printCentered(RED + "X            X" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 System.out.println(YELLOW + " Invalid Choice! Press [ENTER] and Choose (1-5)" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.nextLine();
 continue;
 }
 System.out.print("Enter first number: ");
 double num1 = scanner.nextDouble();
 System.out.print("Enter second number: ");
 double num2 = scanner.nextDouble();
 scanner.nextLine();
 clearConsole();
 printCentered(BLUE + "--- RESULT ---" + RESET);
 if (operation == 1)
 printCentered(CYAN + String.format("%.2f + %.2f = %.2f", num1, num2, num1 + num2) + RESET);
 else if (operation == 2)
 printCentered(CYAN + String.format("%.2f - %.2f = %.2f", num1, num2, num1 - num2) + RESET);
 else if (operation == 3)
 printCentered(CYAN + String.format("%.2f * %.2f = %.2f", num1, num2, num1 * num2) + RESET);
 else if (operation == 4)
 if (num2 == 0)
 printCentered(RED + "Error: Divide by zero!" + RESET);
 else
 printCentered(CYAN + String.format("%.2f / %.2f = %.2f", num1, num2, num1 / num2) + RESET);
 System.out.println();
 printCentered(YELLOW + "Press Enter..." + RESET);

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
 scanner.nextLine();
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


 private static void handleAreaCircumference(Scanner scanner) {
 while (true) {
 clearConsole();
 printCentered(BLUE + "╔════════════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " 🔵 AREA/CIRCUMFERENCE 🔵 " + RESET);
 printCentered(BLUE + "╚════════════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 printCentered(GREEN + "1: Circle" + RESET);
 printCentered(YELLOW + "2: Back" + RESET);
 System.out.println();
 printCentered(YELLOW + "Choice (1-2): " + RESET);
  System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 System.out.print("➡ ");
 try {
 int shapeChoice = scanner.nextInt();
 scanner.nextLine();
 if (shapeChoice == 2)
 return;
 if (shapeChoice == 1) {
 System.out.print("Enter radius: ");
 double radius = scanner.nextDouble();
 scanner.nextLine();
 double area = Math.PI * radius * radius;
 double circumference = 2 * Math.PI * radius;
 printCentered(CYAN + String.format("Area: %.2f", area) + RESET);
 printCentered(CYAN + String.format("Circumference: %.2f", circumference) + RESET);
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
 System.out.println(YELLOW + " Invalid Choice! Press [ENTER] and Choose (1-2)" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 }
 System.out.println();
 printCentered(YELLOW + "Press Enter..." + RESET);
 scanner.nextLine();
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


 private static void handleOddEven(Scanner scanner) {
 clearConsole();
 printCentered(BLUE + "╔════════════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " 🔢 ODD / EVEN CHECKER 🔢 " + RESET);
 printCentered(BLUE + "╚════════════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 System.out.print("Enter an integer: ");
 try {
 int num = scanner.nextInt();
 scanner.nextLine();
 if (num % 2 == 0)
 printCentered(CYAN + num + " is EVEN." + RESET);
 else
 printCentered(CYAN + num + " is ODD." + RESET);
 System.out.println();
 printCentered(YELLOW + "Press Enter..." + RESET);
  System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 
 scanner.nextLine();
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
 System.out.println(YELLOW + " Invalid input! Enter an integer. Press [ENTER]" + RESET);
 System.out.println(BLUE + " ||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||=||" + RESET);
 scanner.next();
 scanner.nextLine();
 }
 }


 private static void handleConversion(Scanner scanner) {
 while (true) {
 clearConsole();
 printCentered(BLUE + "╔════════════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " 🔄 UNIT CONVERSION 🔄 " + RESET);
 printCentered(BLUE + "╚════════════════════════════════════════════════════════╝" + RESET);
 System.out.println();
 printCentered(GREEN + "1: Centimeters to Meters" + RESET);
 printCentered(GREEN + "2: Centimeters to Millimeters" + RESET);
 printCentered(YELLOW + "3: Back" + RESET);
 System.out.println();
 printCentered(YELLOW + "Enter your choice (1-3): " + RESET);
  System.out.println();
 printCentered(BLUE + "╔══════════════════════════════════════════════════╗" + RESET);
 printCentered(YELLOW + " " + RESET);
 printCentered(BLUE + "╚══════════════════════════════════════════════════╝" + RESET);
 
 System.out.print("➡ ");
 try {
 int choice = scanner.nextInt();
 scanner.nextLine();
 if (choice == 3)
 return;
 if (choice == 1 || choice == 2) {
 System.out.print("Enter value in centimeters: ");
 double cm = scanner.nextDouble();
 scanner.nextLine();
 if (choice == 1)
 printCentered(CYAN + String.format("%.2f cm = %.2f m", cm, cm / 100) + RESET);
 else if (choice == 2)
 printCentered(CYAN + String.format("%.2f cm = %.2f mm", cm, cm * 10) + RESET);
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
 }
 System.out.println();
 printCentered(YELLOW + "Press Enter..." + RESET);
 scanner.nextLine();
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


 private static void showLoadingScreen() {
 clearConsole();
 System.out.println();
 printCentered(YELLOW + "LOADING..." + RESET);
 System.out.println();
 int totalWidth = 40;
 int animationDuration = 1500; // milliseconds
 int frameRate = 50; // milliseconds per frame
 int numFrames = animationDuration / frameRate;
 for (int i = 0; i <= numFrames; i++) {
 clearConsole();
 System.out.println();
 printCentered(YELLOW + "LOADING..." + RESET);
 System.out.println();
 double progress = (double) i / numFrames;
 int filledWidth = (int) (totalWidth * progress);
 StringBuilder progressBar = new StringBuilder();
 progressBar.append(GREY_BACKGROUND + " " + RESET); // Start of the bar outline
 // Cyan filled portion with blue chevrons
 for (int j = 0; j < filledWidth; j++) {
 if (j % 2 == 0) {
 progressBar.append(CYAN + BLACK_BACKGROUND + ">" + RESET);
 } else {
 progressBar.append(CYAN + BLACK_BACKGROUND + ">" + RESET);
 }
 }
 // White empty portion
 for (int j = filledWidth; j < totalWidth; j++) {
 progressBar.append(WHITE + BLACK_BACKGROUND + " " + RESET);
 }
 progressBar.append(GREY_BACKGROUND + " " + RESET); // End of the bar outline
 printCentered(progressBar.toString());
 try {
 Thread.sleep(frameRate);
 } catch (InterruptedException e) {
 e.printStackTrace();
 }
 }
 System.out.println();
 printCentered(GREEN + "Loading complete!" + RESET);
 try {
 Thread.sleep(500);
 } catch (InterruptedException ignored) {
 } // Short delay after completion
 }


 // Utility methods
 private static void clearConsole() {
 System.out.print("\033[H\033[2J");
 System.out.flush();
 }


 private static void showRocketLoadingAnimation() {
 System.out.println(YELLOW + "🚀 Loading..." + RESET);
 try {
 Thread.sleep(800);
 } catch (InterruptedException ignored) {
 }
 }


 private static void printCentered(String text) {
 int width = 60;
 int pad = (width - text.replaceAll("\033\\[[;\\d]*m", "").length()) / 2;
 System.out.println(" ".repeat(Math.max(0, pad)) + text);
 }


 // Method to print the ASCII art
 public static void printAsciiArt() {
 	clearConsole();
printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠒⢦⡀⠀⠀⠀⠀⠀⠀");
 printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠆⠀⣿⡇⠀⠀⠀⠀⠀⠀");
 printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠞⢉⣽⡿⠀⠀⠀⠀⠀⠀⠀");
 printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡠⠋⢐⣾⣷⠁⠀⠀⠀⠀⠀⠀⠀");
 printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣰⠡⠤⣮⣿⣵⠆⠠⠤⣀⣀⡀⠀⠀");
 printCentered("⠀⠀⠀⠀⠀⠀⠀⠀⠀⡰⠏⠀⠐⢾⣽⣛⠟⠚⠛⠓⠒⠈⠱⡄");
 printCentered("⠀⣀⣀⣤⣀⣤⣄⠠⡜⠃⠀⢀⣀⣼⣿⣿⠿⢦⣶⣶⣦⣿⣿⡟");
 printCentered("⣾⣿⣿⠻⢿⣿⡇⠀⢫⣣⡱⣾⡿⣿⣿⣿⣆⣄⢀⢉⡉⣩⣿⠀");
 printCentered("⢻⢻⡿⡎⠀⠀⢇⣀⣬⣷⠉⠙⠉⠙⣻⣿⠙⠓⠛⠿⣿⣿⠟⠀");
 printCentered("⢸⣄⠈⢧⠀⠀⠸⡀⢀⣿⣤⣀⠀⠀⣺⡟⠿⣶⢦⣦⣤⡿⠀⠀");
 printCentered("⠀⢻⣷⣼⡄⠀⠀⢱⣿⡿⠿⠾⠷⣶⣿⣷⣦⣌⢉⣻⠏⠁⠀⠀");
 printCentered("⠀⠀⢧⣿⣷⡤⠒⠓⠁⠀⠀⠀⠀⠀⠀⠀⠉⠉⠋⠁⠀⠀⠀⠀");
 printCentered("⠀⠀⠈⣚⡻⠇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
 printCentered("PLEASE GIVE US A THUMBS UP!! ^ _ ^");
 }
}

# javadeveloperinternship
import java.util.Scanner;
public class Calculator {

  public static double add(double a, double b) {
        return a + b;
    }

   public static double subtract(double a, double b) {
        return a - b;
    }

   public static double multiply(double a, double b) {
        return a * b;
    }

   public static double divide(double a, double b) {
        if (b == 0) {
            System.out.println("Error: Cannot divide by zero.");
            return 0;
        }
        return a / b;
    }

  public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

   while (true) {
            System.out.println("\n--- Simple Calculator ---");
            System.out.println("Choose operation: +  -  *  /");
            System.out.println("Enter 'exit' to quit.");

  String operation = scanner.next();

   if (operation.equalsIgnoreCase("exit")) {
                System.out.println("Exiting calculator. Goodbye!");
                break;
            }

  System.out.print("Enter first number: ");
            double num1 = scanner.nextDouble();

   System.out.print("Enter second number: ");
            double num2 = scanner.nextDouble();

  double result;

  switch (operation) {
                case "+":
                    result = add(num1, num2);
                    System.out.println("Result: " + result);
                    break;
                case "-":
                    result = subtract(num1, num2);
                    System.out.println("Result: " + result);
                    break;
                case "*":
                    result = multiply(num1, num2);
                    System.out.println("Result: " + result);
                    break;
                case "/":
                    result = divide(num1, num2);
                    System.out.println("Result: " + result);
                    break;
                default:
                    System.out.println("Invalid operation!");
            }
        }

   scanner.close();
   }
}

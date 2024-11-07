package shadowfox.beginner;

import java.util.Scanner;

public class Calculator {
	

	

	    public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        boolean running = true;

	        System.out.println("Welcome to the Console Calculator!");

	        while (running) {
	            System.out.println("\nSelect an option:");
	            System.out.println("1. Basic Arithmetic");
	            System.out.println("2. Scientific Calculations");
	            System.out.println("3. Unit Conversions");
	            System.out.println("4. Exit");
	            int choice = scanner.nextInt();

	            switch (choice) {
	                case 1:
	                    basicArithmetic(scanner);
	                    break;
	                case 2:
	                    scientificCalculations(scanner);
	                    break;
	                case 3:
	                    unitConversions(scanner);
	                    break;
	                case 4:
	                    running = false;
	                    System.out.println("Exiting...");
	                    break;
	                default:
	                    System.out.println("Invalid choice. Please try again.");
	            }
	        }
	        scanner.close();
	    }

	    public static void basicArithmetic(Scanner scanner) {
	        System.out.println("\nBasic Arithmetic Operations:");
	        System.out.println("1. Addition (+)");
	        System.out.println("2. Subtraction (-)");
	        System.out.println("3. Multiplication (*)");
	        System.out.println("4. Division (/)");

	        int operation = scanner.nextInt();
	        System.out.print("Enter first number: ");
	        double num1 = scanner.nextDouble();
	        System.out.print("Enter second number: ");
	        double num2 = scanner.nextDouble();
	        double result;

	        switch (operation) {
	            case 1:
	                result = num1 + num2;
	                System.out.println("Result: " + result);
	                break;
	            case 2:
	                result = num1 - num2;
	                System.out.println("Result: " + result);
	                break;
	            case 3:
	                result = num1 * num2;
	                System.out.println("Result: " + result);
	                break;
	            case 4:
	                if (num2 != 0) {
	                    result = num1 / num2;
	                    System.out.println("Result: " + result);
	                } else {
	                    System.out.println("Error: Cannot divide by zero.");
	                }
	                break;
	            default:
	                System.out.println("Invalid operation.");
	        }
	    }

	    public static void scientificCalculations(Scanner scanner) {
	        System.out.println("\nScientific Calculations:");
	        System.out.println("1. Square Root");
	        System.out.println("2. Exponentiation");

	        int operation = scanner.nextInt();
	        double result;

	        switch (operation) {
	            case 1:
	                System.out.print("Enter a number: ");
	                double num = scanner.nextDouble();
	                if (num >= 0) {
	                    result = Math.sqrt(num);
	                    System.out.println("Square Root: " + result);
	                } else {
	                    System.out.println("Error: Cannot take the square root of a negative number.");
	                }
	                break;
	            case 2:
	                System.out.print("Enter the base: ");
	                double base = scanner.nextDouble();
	                System.out.print("Enter the exponent: ");
	                double exponent = scanner.nextDouble();
	                result = Math.pow(base, exponent);
	                System.out.println("Exponentiation Result: " + result);
	                break;
	            default:
	                System.out.println("Invalid operation.");
	        }
	    }

	    public static void unitConversions(Scanner scanner) {
	        System.out.println("\nUnit Conversions:");
	        System.out.println("1. Temperature (Celsius to Fahrenheit)");
	        System.out.println("2. Temperature (Fahrenheit to Celsius)");

	        int choice = scanner.nextInt();
	        double result;

	        switch (choice) {
	            case 1:
	                System.out.print("Enter temperature in Celsius: ");
	                double celsius = scanner.nextDouble();
	                result = (celsius * 9/5) + 32;
	                System.out.println("Temperature in Fahrenheit: " + result);
	                break;
	            case 2:
	                System.out.print("Enter temperature in Fahrenheit: ");
	                double fahrenheit = scanner.nextDouble();
	                result = (fahrenheit - 32) * 5/9;
	                System.out.println("Temperature in Celsius: " + result);
	                break;
	            default:
	                System.out.println("Invalid conversion option.");
	        }
	    }
	}




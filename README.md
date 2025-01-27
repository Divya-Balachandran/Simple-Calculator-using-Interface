# Simple-Calculator-using-Interface
package calculatorprogram;
import java.util.Scanner;
interface Calculator {
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculator implements Calculator {

    @Override
    public double add(double a, double b) {
        return a+b;
    }

    @Override
    public double subtract(double a, double b) {
        return a-b;
    }

    @Override
    public double multiply(double a, double b) {
        return a*b; 
    }

    @Override
    public double divide(double a, double b) {
        if(b==0){
            System.out.println("Errot:Division by zero is not allowed!");
            return Double.NaN;
        }
          return a/b;
            
        }
    }
    
    

/**
 *
 * @author 1BSCCSA44
 */
public class CalculatorProgram {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner scanner=new Scanner(System.in);
        Calculator calculator=new SimpleCalculator();
        System.out.println("Welcome to the Simple Calculator!");
        System.out.print("Enter the first number:");
        double num1=scanner.nextDouble();
        System.out.println("Enter the second number:");
        double num2=scanner.nextDouble();
         System.out.println("\nResults:");
        System.out.println("Addition: " + calculator.add(num1, num2));
        System.out.println("Subtraction: " + calculator.subtract(num1, num2));
        System.out.println("Multiplication: " + calculator.multiply(num1, num2));
        System.out.println("Division: " + calculator.divide(num1, num2));
        scanner.close();

    }
    
}

OUTPUT:
Welcome to the Simple Calculator!
Enter the first number:4
Enter the second number:
2

Results:
Addition: 6.0
Subtraction: 2.0
Multiplication: 8.0
Division: 2.0


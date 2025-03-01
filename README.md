# Write a program to read a four digit number through the keyboard and calculate the sum of its digits.
# java_programming
 
 
 
 

import java.util.Scanner;

public class sumOfDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a four-digit number:");
        int num = sc.nextInt();

       
        if (num < 1000 || num > 9999) {
            System.out.println("Invalid! Please enter a correct four-digit number.");
        } else {
            int sum = 0;
            int temp = num; // Store original number

            
            while (temp > 0) {
                sum += temp % 10; // Get last digit and add to sum
                temp /= 10; // Remove last digit
            }

            System.out.println("The sum of the digits of " + num + " is: " + sum);
        }

        sc.close(); 
    }
}

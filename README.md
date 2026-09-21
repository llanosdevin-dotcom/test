/*
Description: This program calculates the GCD of two non-negative integers
using the recursive Euclidean algorithm.

Programmed by: Devin Llanos - BSIT - [48160] [Subject]

Last Modified: September 21, 2026

Version: 1.0

Acknowledgements: Class notes, learning resources, and ChatGPT
*/

import java.util.Scanner;

public class RecursiveGCD {

    static int gcd(int a, int b) {

        System.out.println("gcd(" + a + ", " + b + ")");

        if (b == 0) {
            return a;
        }

        int remainder = a % b;
        System.out.println(a + " % " + b + " = " + remainder);

        return gcd(b, remainder);
    }

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = input.nextInt();

        System.out.print("Enter second number: ");
        int b = input.nextInt();

        if (a == 0 && b == 0) {
            System.out.println("Both numbers cannot be zero.");
        } else {
            int result = gcd(a, b);
            System.out.println("GCD: " + result);
        }

        input.close();
    }
}

// “The gcd() method uses recursion. The base case is when b == 0, and the recursive case is gcd(b, a % b). The % operator gets the remainder, which moves the values toward the base case.”

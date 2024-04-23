#include <stdio.h>

int main() {
    int sumEven = 0; // For accumulating even numbers, start from 0
    int sumOdd = 0;  // For accumulating odd numbers
    int upperBound = 0; // Sum from 1 upper bound
    int absDiff = 0; // The absolute difference between the sums

    printf("Enter the upper bound of the subject: "); // Prompt user for input
    scanf("%d", &upperBound); // Use %d to read an int

    int number = 1; // Use a while-loop to repeatedly add 1, 2, 3, ... to the sum
    while (number <= upperBound) {
        if (number % 2 == 0) {
            sumEven += number;
        } else {
            sumOdd += number;
        }
        number++;
    }

    absDiff = sumOdd - sumEven; // Calculate the absolute difference between sumOdd and sumEven
    if (absDiff < 0) {
        absDiff = -absDiff;
    }

    printf("Sum of even numbers of the subject: %d\n", sumEven);
    printf("Sum of odd numbers of the subject: %d\n", sumOdd);
    printf("Absolute difference between subjects: %d\n", absDiff);

    return 0;
}

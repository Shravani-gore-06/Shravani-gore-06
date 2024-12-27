#include <stdio.h>
#include<conio.h>

void add();
void subtract();
void multiply();
void divide();

int main() {
    int choice;
    
    printf("\tSimple Calculator\n");
    printf("\t=================\n");
    
    while (1) {
        
        printf("\nMenu:\n");
        printf("1. Add\n");
        printf("2. Subtract\n");
        printf("3. Multiply\n");
        printf("4. Divide\n");
        printf("5. Exit\n");
        
        
        printf("Enter your choice (1-5): ");
        if (scanf("%d", &choice) != 1) { 
            
            printf("Invalid input!\n");
            while (getchar() != '\n'); 
            continue;
        }

        
        switch (choice) {
            case 1:
                add();
                break;
            case 2:
                subtract();
                break;
            case 3:
                multiply();
                break;
            case 4:
                divide();
                break;
            case 5:
                printf("Exiting...\n");
                return 0;
            default:
                printf("Invalid choice!.\n");
        }
    }
    
    return 0;
}


void add() {
    float num1, num2;
    printf("Enter two numbers to add: ");
    if (scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input!\n");
        while (getchar() != '\n'); 
        return;
    }
    printf("Result: %.2f\n", num1 + num2);
}


void subtract() {
    float num1, num2;
    printf("Enter two numbers to subtract: ");
    if (scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input!\n");
        while (getchar() != '\n'); 
        return;
    }
    printf("Result: %.2f\n", num1 - num2);
}


void multiply() {
    float num1, num2;
    printf("Enter two numbers to multiply: ");
    if (scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input!\n");
        while (getchar() != '\n'); 
        return;
    }
    printf("Result: %.2f\n", num1 * num2);
}


void divide() {
    float num1, num2;
    printf("Enter two numbers to divide: ");
    if (scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input!\n");
        while (getchar() != '\n'); 
        return;
    }
    if (num2 == 0) {
        printf("Error!\n");
    } else {
        printf("Result: %.2f\n", num1 / num2);
    }
}

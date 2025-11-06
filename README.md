# ATM-PROJECT

Project Report
Title:
ATM Simulation System in C

Aim:
To design and implement a simple ATM simulation program using the C programming language that allows users to check balance, deposit money, and withdraw money interactively.

Objectives:


To develop a console-based ATM program using C language.


To simulate basic banking operations such as balance inquiry, deposit, and withdrawal.


To provide a user-friendly interface using menu-driven options.


To apply concepts of decision-making, loops, and conditional statements in C programming.


To enhance understanding of real-time banking logic implementation in a simple form.



Introduction of the Project:
The ATM Simulation System is a simple console-based application designed to mimic the basic functionalities of an Automated Teller Machine (ATM).
Users can interact with the system by choosing from a set of menu options such as checking their balance, depositing money, withdrawing money, or exiting the application.
The system is initialized with a fixed balance (₹1000.00) and updates the balance dynamically based on user input. The project demonstrates fundamental programming concepts including conditional statements, loops, input/output operations, and basic arithmetic operations.

Methodology:


Problem Analysis:
Identify the need for simulating ATM operations like balance check, deposit, and withdrawal.


Design:


Use a menu-driven structure for interaction.


Implement a loop for continuous operations until the user chooses to exit.


Use switch-case statements for menu options.




Implementation:


Code developed using C language.


Logical operations for deposit, withdrawal, and validation of user input.




Testing:


Test for invalid inputs (e.g., negative amounts).


Test for insufficient balance.


Validate that balance updates correctly after each transaction.





Technology Used in Project:


Programming Language: C


Compiler: GCC (GNU Compiler Collection) / Turbo C / Code::Blocks / Dev C++


Platform: Windows / Linux


Paradigm: Procedural Programming



Hardware and Software Requirements:
Hardware:


Processor: Intel i3 or higher


RAM: Minimum 2 GB


Storage: 100 MB free disk space


Software:


Operating System: Windows / Linux


C Compiler: GCC / Turbo C


IDE (Optional): Code::Blocks / Dev C++ / Visual Studio Code



Source Code:
#include <stdio.h>
int main() {
    int choice;
    float balance = 1000.00; // Initial balance
    float amount;

    while (1) {
        printf("\n===== ATM Menu =====\n");
        printf("1. Check Balance\n");
        printf("2. Deposit Money\n");
        printf("3. Withdraw Money\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Your current balance is ₹%.2f\n", balance);
                break;
            case 2:
                printf("Enter amount to deposit: ₹");
                scanf("%f", &amount);
                if (amount > 0) {
                    balance += amount;
                    printf("₹%.2f deposited successfully.\n", amount);
                } else {
                    printf("Invalid deposit amount.\n");
                }
                break;
            case 3:
                printf("Enter amount to withdraw: ₹");
                scanf("%f", &amount);
                if (amount > 0 && amount <= balance) {
                    balance -= amount;
                    printf("₹%.2f withdrawn successfully.\n", amount);
                } else {
                    printf("Insufficient balance or invalid amount.\n");
                }
                break;
            case 4:
                printf("Thank you for using the ATM. Goodbye!\n");
                return 0;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

    return 0;
}


Code Screenshot:
📸 (Insert screenshot of your code editor showing the above program here)

Output Screenshot:
📸 (Insert console output screenshot showing menu, deposit, withdrawal, and exit options here)
Example Output:
===== ATM Menu =====
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 1
Your current balance is ₹1000.00


Conclusion:
The ATM Simulation Project successfully demonstrates basic banking operations using C programming. It provides a simple yet effective model to understand how an ATM functions. Through this project, key programming concepts like loops, decision-making, user input validation, and modular code design are reinforced. The program can be extended to include additional features such as PIN authentication, transaction history, and multi-user functionality.

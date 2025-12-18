# -Define-a-class-to-represent-a-bank-account-which-includes-the-following-members-
#include <iostream.h>
#include <conio.h>

class Bank {
    char name[30];
    int acc_no;
    float balance;

public:
    // Function to assign initial values
    void initialValues() {
        cout << "Enter Depositor Name: ";
        cin >> name;
        cout << "Enter Account Number: ";
        cin >> acc_no;
        cout << "Enter Initial Balance: ";
        cin >> balance;
    }

    // Function to deposit amount
    void deposit() {
        float amt;
        cout << "Enter amount to deposit: ";
        cin >> amt;
        balance += amt;
        cout << "Amount Deposited Successfully.\n";
    }

    // Function to withdraw amount
    void withdraw() {
        float amt;
        cout << "Enter amount to withdraw: ";
        cin >> amt;

        if (amt > balance) {
            cout << "Insufficient Balance!\n";
        } else {
            balance -= amt;
            cout << "Withdrawal Successful.\n";
        }
    }

    // Function to display name and balance
    void display() {
        cout << "\n--- Account Details ---\n";
        cout << "Name of Depositor : " << name << endl;
        cout << "Account Number    : " << acc_no << endl;
        cout << "Balance Amount    : " << balance << endl;
    }
};

void main() {
    clrscr();
    Bank b;
    
    b.initialValues();
    b.deposit();
    b.withdraw();
    b.display();

    getch();
}

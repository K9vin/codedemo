# codedemo
C++ Demo MPESA Transaction Code
// MPESA Transaction Code
#include <iostream>

using namespace std;

int main() {
    int number, phone_number, pin, agent_number, paybill, till_number;
    float choice;
    double amount;
    double balance = 5000;

    // Display available options
    cout << "1.Send Money" << endl;
    cout << "2.Withdraw Money" << endl;
    cout << "3.Buy Airtime" << endl;
    cout << "4.Loans and Savings" << endl;
    cout << "5.Lipa na Mpesa" << endl;
    cout << "6.My Account" << endl;
    cout << "Enter number: " << endl;

    // Get user selection
    cin >> number;

    // Option 1: Send Money
    if (number == 1) {
        cout << "Send Money" << endl;
        cout << "Enter the phone number:" << endl;
        cin >> phone_number;
        cout << "Enter Amount" << endl;
        cin >> amount;
        cout << "Enter PIN" << endl;
        cin >> pin;

        if (amount <= balance) {
            cout << "Successful transaction to number 0" << phone_number << endl;
        } else {
            cout << "Insufficient funds. Top up to complete transaction" << endl;
        }
    }
    // Option 2: Withdraw Money
    else if (number == 2) {
        cout << "Withdraw Money" << endl;
        cout << "Enter the agent number:" << endl;
        cin >> agent_number;
        cout << "Enter Amount" << endl;
        cin >> amount;
        cout << "Enter PIN" << endl;
        cin >> pin;

        if (amount <= balance) {
            cout << "Successfully withdrew " << amount << endl;
        } else {
            cout << "Insufficient funds. Cannot withdraw." << endl;
        }
    }
    // Option 3: Buy Airtime
    else if (number == 3) {
        cout << "Buy Airtime" << endl;
        cout << "Enter the phone number:" << endl;
        cin >> phone_number;
        cout << "Enter Amount" << endl;
        cin >> amount;
        cout << "Enter PIN" << endl;
        cin >> pin;

        if (amount <= balance) {
            cout << "Confirmed purchase of airtime for 0" << phone_number << endl;
        } else {
            cout << "Insufficient funds. Top up" << endl;
        }
    }
    // Option 4: Loans and Savings
    else if (number == 4) {
        cout << "Loans and Savings" << endl;
        cout << "Enter the phone number:" << endl;
        cin >> phone_number;
        cout << "Enter Amount" << endl;
        cin >> amount;
        cout << "Enter PIN" << endl;
        cin >> pin;

        if (amount <= balance) {
            cout << "Successful loaned through number 0" << phone_number << endl;
        } else {
            cout << "Insufficient funds to set as savings" << endl;
        }
    }
    // Option 5: Lipa na Mpesa
    else if (number == 5) {
        int paybill, till_number;

        cout << "Lipa na Mpesa" << endl;
        cout << "1.1 Pay Bill" << endl;
        cout << "1.2 Buy Goods and Services" << endl;
        cin >> choice;

        if (choice == 1.1f) {  // Use float literal for matching
            cout << "Enter Pay Bill: " << endl;
            cin >> paybill;
            cout << "Enter the phone number:" << endl;
            cin >> phone_number;
            cout << "Enter Amount:" << endl;
            cin >> amount;
            cout << "Enter PIN:" << endl;
            cin >> pin;

            if (amount <= balance) {
                cout << "Successful transaction to 0" << phone_number << " via Pay Bill " << paybill << endl;
            } else {
                cout << "Insufficient funds. Top up to complete transaction" << endl;
            }
        }
        else if (choice == 1.2f) {
            cout << "Enter Till Number: " << endl;
            cin >> till_number;
            cout << "Enter the phone number:" << endl;
            cin >> phone_number;
            cout << "Enter Amount:" << endl;
            cin >> amount;
            cout << "Enter PIN:" << endl;
            cin >> pin;

            if (amount <= balance) {
                cout << "Successful transaction to 0" << phone_number << " via Till Number " << till_number << endl;
            } else {
                cout << "Insufficient funds. Top up to complete transaction" << endl;
            }
        } else {
            cout << "Invalid Lipa na Mpesa option selected!" << endl;
        }
    }
    // Option 6: My Account
    else if (number == 6) {
        cout << "My Account" << endl;
        cout << "Enter the phone number:" << endl;
        cin >> phone_number;
        cout << "Enter PIN" << endl;
        cin >> pin;
        cout << "Your current balance is " << balance << endl;
    }
    else {
        cout << "Invalid option selected!" << endl;
    }

    return 0;
}

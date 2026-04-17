# BANK-MANAGEMENT-SYSTEM-UNIT2
This project implements core banking operations like account creation, deposit, withdrawal, balance enquiry, and transaction handling. It demonstrates OOP concepts, data management, and user interaction using Java for efficient banking simulation.
# 🏦 Bank Account Management System (Java)

## 📌 Overview

This is a simple **Bank Account Management System** implemented in Java using Object-Oriented Programming (OOP) concepts.
The program allows users to:

* Store account details
* Perform deposit and withdrawal transactions
* Display account summary

---

## 🚀 Features

* Create and store bank account details
* Display account information
* Perform deposit and withdrawal operations
* Show transaction summary
* Console-based application

---

## 🛠️ Technologies Used

* Java
* OOP Concepts (Encapsulation, Classes, Methods)
* Scanner (for user input)

---

## 📂 Project Structure

```
BankAccountProject/
│
├── Solution.java   (Main class)
```

---

## 💻 Source Code

```java
import java.util.*;

class BankAccount {
    private String accountNumber;
    private String accountHolder;
    private String accountType;
    private double balance;

    void setDetails(String accNo, String holder, String type, double bal) {
        accountNumber = accNo;
        accountHolder = holder;
        accountType = type;
        balance = bal;
    }

    void displayAccountDetails() {
        System.out.println();
        System.out.println(" BANK ACCOUNT DETAILS");
        System.out.println("Account Number : " + accountNumber);
        System.out.println("Account Holder : " + accountHolder);
        System.out.println("Account Type : " + accountType);
        System.out.println("Bank Status : Active\n");
    }

    void transactionDetails(double deposit, double withdraw) {
        System.out.println();
        System.out.println("TRANSACTION DETAILS");
        System.out.printf("Opening Balance : ₹%.2f\n", balance);

        balance += deposit;
        System.out.printf("Deposit Amount : ₹%.2f\n", deposit);
        System.out.printf("Balance After Deposit : ₹%.2f\n\n", balance);

        balance -= withdraw;
        System.out.printf("Withdrawal Amount: ₹%.2f\n", withdraw);
        System.out.printf("Balance After Withdrawal : ₹%.2f\n\n", balance);
    }

    void summary(double deposit, double withdraw) {
        System.out.println(" SUMMARY");
        System.out.printf("Total Deposits : ₹%.2f\n", deposit);
        System.out.printf("Total Withdrawals: ₹%.2f\n", withdraw);
        System.out.printf("Current Balance : ₹%.2f\n\n", balance);
        System.out.println("Transaction Status : Successful");
        System.out.println("Last Updated : Today");
    }
}

public class Solution {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        String accNo = s.nextLine();
        String name = s.nextLine();
        double balance = s.nextDouble();
        s.nextLine();
        String type = s.nextLine();
        double deposit = s.nextDouble();
        double withdraw = s.nextDouble();

        BankAccount b = new BankAccount();
        b.setDetails(accNo, name, type, balance);

        b.displayAccountDetails();
        b.transactionDetails(deposit, withdraw);
        b.summary(deposit, withdraw);
    }
}
```
<img width="1600" height="731" alt="1" src="https://github.com/user-attachments/assets/53dc0919-3dd5-4311-a2eb-0cab1fb8872b" />
<img width="1600" height="738" alt="2" src="https://github.com/user-attachments/assets/d4056fc2-35d8-446b-b772-622c4b192acb" />

---

## ▶️ How to Run

1. Save the file as `Solution.java`
2. Open terminal / command prompt
3. Compile the program:

```
javac Solution.java
```

4. Run the program:

```
java Solution
```

---

## 📥 Sample Input

```
123456789
John Doe
5000
Savings
2000
1500
```

---

## 📤 Sample Output

```
BANK ACCOUNT DETAILS
Account Number : 123456789
Account Holder : John Doe
Account Type : Savings
Bank Status : Active

TRANSACTION DETAILS
Opening Balance : ₹5000.00
Deposit Amount : ₹2000.00
Balance After Deposit : ₹7000.00

Withdrawal Amount: ₹1500.00
Balance After Withdrawal : ₹5500.00

SUMMARY
Total Deposits : ₹2000.00
Total Withdrawals: ₹1500.00
Current Balance : ₹5500.00

Transaction Status : Successful
Last Updated : Today
```

---

## 📌 Future Improvements

* Add validation for insufficient balance
* Implement multiple accounts
* Add GUI using Swing or JavaFX
* Store data using files or database

---

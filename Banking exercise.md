# Beginner Java Project (OOP-Focused)

## Project Title
**Simple Banking System (Console Application)**

---

## Project Overview

Build a console-based **Banking System** that allows users to create accounts and perform basic banking operations.

The main goal of this project is to practice **proper Object-Oriented Programming (OOP)** using core Java concepts. Students must also complete several tasks using **Streams and Lambda expressions**.

JDBC integration is optional for students who want an additional challenge.

---

# 🎯 Main Learning Focus: OOP Fundamentals

This project must clearly demonstrate:

- Classes and Objects
- Encapsulation (private fields + getters/setters)
- Constructors
- Method overloading
- Inheritance
- Polymorphism
- Use of at least one Interface
- Proper class responsibilities (clean design)

---

## Functional Requirements

### 1. Account Management

The system must allow a user to:

- Create a new bank account
- View account details
- Deposit money
- Withdraw money
- Transfer money between accounts
- View all accounts

Each Account must contain:
- Account Number
- Account Holder Name
- Balance
- Account Type (Savings / Current)

---

### 2. Transaction Tracking

The system must:

- Record every deposit, withdrawal, and transfer
- Store transactions per account
- Display transaction history

Each Transaction must contain:
- Transaction ID
- Type (Deposit / Withdrawal / Transfer)
- Amount
- Date

---

## Required OOP Structure (Suggested)

```
src/
 ├── model/
 │     ├── Account.java (abstract class)
 │     ├── SavingsAccount.java
 │     ├── CurrentAccount.java
 │     ├── Transaction.java
 │     └── Transferable.java (interface)
 │
 ├── service/
 │     ├── BankService.java
 │
 └── Main.java
```

---

## OOP Design Requirements

### 1. Inheritance
- `Account` must be an abstract class.
- `SavingsAccount` and `CurrentAccount` must extend `Account`.

### 2. Interface
- Create a `Transferable` interface.
- Accounts should implement `Transferable`.

### 3. Polymorphism
- Store different account types using an `Account` reference.
- Override at least one method (e.g., calculateFees()).

---

## Business Rules

- Withdrawal should not be allowed if balance is insufficient.
- SavingsAccount may have a minimum balance rule.
- CurrentAccount may allow overdraft (optional).

---

## Collections Requirement

- Use `ArrayList` to store accounts.
- Use `ArrayList` to store transactions.

---

## Streams & Lambda Tasks (Optional Bonus)

Students may implement the following using **Streams and Lambda expressions** for additional practice:

1. Display all accounts sorted by balance.
2. Find accounts with balance greater than a given amount.
3. Calculate total money stored in the bank.
4. Count how many transactions are withdrawals.
5. Display the top 3 highest-value transactions.

### If NOT Using Streams

Students can complete the same tasks using:

- Traditional `for` or `foreach` loops
- `Collections.sort()` with a Comparator class
- Manual filtering using conditional statements
- Accumulator variables for totals and counts
- Nested loops where necessary

The goal is to understand the logic first. Streams and Lambdas are encouraged for cleaner and more modern solutions, but they are not mandatory.

---

## Exception Handling

You must:

- Handle invalid menu input
- Prevent withdrawing more than available balance
- Create at least one custom exception (e.g., `InsufficientFundsException`)

---

## Optional: JDBC Integration (Bonus)

For students who want an extra challenge:

- Store accounts and transactions in a relational database.
- Use JDBC for CRUD operations.
- Use PreparedStatement.
- Handle SQLExceptions properly.

---

## Optional: Advanced Extensions (Harder Tasks)

Students who finish early may implement the following advanced features:

### 1. Interest Calculation (Savings Account)
- Add an interest rate field to SavingsAccount.
- Implement a method to calculate monthly interest.
- Add a "Process Monthly Update" option in the menu that applies interest to all savings accounts.

### 2. Monthly Account Processing
- Deduct maintenance fees from CurrentAccount.
- Record these deductions as transactions.
- Demonstrate polymorphism by overriding a method like `processMonthEnd()` in each account type.

### 3. Overdraft Feature (Current Account)
- Allow overdraft up to a fixed limit.
- Prevent withdrawals beyond overdraft limit.
- Track overdraft usage separately.

### 4. Transaction Limits
- Limit number of withdrawals per month for SavingsAccount.
- Throw a custom exception if the limit is exceeded.

### 5. Advanced Stream Reports
- Group transactions by type (Deposit, Withdrawal, Transfer).
- Calculate average transaction amount.
- Find the account with the highest number of transactions.

These tasks should reinforce deeper understanding of inheritance, polymorphism, and real-world modeling.

---




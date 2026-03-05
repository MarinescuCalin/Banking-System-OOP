# Banking System OOP

Java banking simulator that processes JSON scenarios and executes account, card, transfer, savings, split-payment, and business-account operations.

## Tech Stack
- Java 21
- Maven
- Jackson + Gson

## Implemented Operations
Supported commands in the engine include:
- `printUsers`, `printTransactions`
- `addAccount`, `deleteAccount`, `addFunds`
- `createCard`, `createOneTimeCard`, `deleteCard`, `checkCardStatus`, `setMinimumBalance`
- `payOnline`, `sendMoney`, `cashWithdrawal`
- `setAlias`
- `addInterest`, `changeInterestRate`, `withdrawSavings`
- `splitPayment`, `acceptSplitPayment`, `rejectSplitPayment`
- `upgradePlan`
- `report`, `spendingsReport`, `businessReport`
- `addNewBusinessAssociate`, `changeSpendingLimit`, `changeDepositLimit`

## Run
Build the project:

```bash
mvn clean package
```

Run all scenarios from `input/` and write outputs in `result/`:

```bash
java -cp target/j-poo-morgan-phase-two-1.0-SNAPSHOT-jar-with-dependencies.jar org.poo.main.Main
```

Run a single scenario and write output to `out.txt`:

```bash
printf "test01_user_updates.json\n" | java -cp target/j-poo-morgan-phase-two-1.0-SNAPSHOT-jar-with-dependencies.jar org.poo.main.Test
```

## Project Structure
- `src/main/java/org/poo/bank` - core domain logic (users, accounts, cards, plans, transactions, business flows)
- `src/main/java/org/poo/main` - command dispatch and execution entrypoints
- `src/main/java/org/poo/fileio` - input/output mapping classes
- `input/` - JSON scenarios
- `ref/` - expected outputs for scenario comparison

## What This Project Demonstrates
- OOP design with clear domain entities and responsibilities
- command-based processing engine
- stateful banking flows with validation and transaction history
- reporting and business-account management use cases

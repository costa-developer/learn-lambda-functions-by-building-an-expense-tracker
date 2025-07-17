# Learn Lambda Functions by Building an Expense Tracker

This is a simple Python project designed to teach you how to use **lambda functions** while building a basic expense tracker.

## Features So Far

* Add expenses with amounts and categories
* Print a list of all expenses
* Calculate the total expense amount using a lambda function and the `map()` function

## Code Overview

```python
def add_expense(expenses, amount, category):
    """
    Adds a new expense dictionary to the expenses list.
    
    Parameters:
    - expenses (list): The list storing expense dictionaries.
    - amount (float): The cost of the expense.
    - category (str): The category of the expense.
    """
    expenses.append({'amount': amount, 'category': category})
    
def print_expenses(expenses):
    """
    Prints all expenses in a readable format.
    
    Parameters:
    - expenses (list): The list storing expense dictionaries.
    """
    for expense in expenses:
        print(f'Amount: {expense["amount"]}, Category: {expense["category"]}')
    
def total_expenses(expenses):
    """
    Returns the sum of all expense amounts.
    
    Parameters:
    - expenses (list): The list storing expense dictionaries.
    
    Uses a lambda function with map() to extract the amounts.
    """
    return sum(map(lambda expense: expense['amount'], expenses))

# Initialize empty expenses list
expenses = []
```

## Example Usage

```python
add_expense(expenses, 100.0, "Groceries")
add_expense(expenses, 50.0, "Transport")
print_expenses(expenses)
print(f"Total Expenses: {total_expenses(expenses)}")
```

**Output:**

```
Amount: 100.0, Category: Groceries
Amount: 50.0, Category: Transport
Total Expenses: 150.0
```

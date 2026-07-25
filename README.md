[README.md](https://github.com/user-attachments/files/30369763/README.md)
# NGO Donation Management System

A console-based Python application for managing company registrations and donations to an NGO. The system stores company information, records eligible donations, identifies registered companies that have not donated, and calculates the total amount collected.

## Project Overview

This project was developed as a **CSC101L Final Project**. It demonstrates fundamental Python programming concepts through a practical donation management application.

The program uses a menu-driven interface that allows users to:

* View companies that have donated
* Calculate the total donated amount
* View registered companies that have not donated
* Record a donation for an existing company
* Register a new company
* Prevent duplicate company registrations
* Validate the minimum donation amount

## Features

### 1. Donation Summary

Displays companies that have donated at least **100,000 Tk** and calculates the total donation amount.

### 2. Non-Donating Company Report

Lists all registered companies whose donation amount is currently zero.

### 3. Donation Collection

Records a donation for an existing company when:

* The company number exists
* The company has not donated previously
* The donation is at least **100,000 Tk**

### 4. New Company Registration

Registers a new company using:

* Company number
* Company ID
* Company name
* Donation amount

A company may register without donating by entering `0` as the donation amount.

### 5. Duplicate Company Detection

Company names are compared without considering uppercase or lowercase letters. This prevents entries such as `Walton` and `walton` from being registered as separate companies.

### 6. Input Validation

The program rejects:

* Donations below **100,000 Tk**
* Donations from companies that have already donated
* Invalid company numbers
* Invalid menu options

## Technologies Used

* Python 3
* Jupyter Notebook or Google Colab
* Python lists
* Functions
* Loops
* Conditional statements
* Formatted output
* User input handling

## Data Structure

Company information is stored in a nested Python list.

```python
Companies = [
    ["01", "5681983", "Grameenphone", 0],
    ["02", "5682008", "Walton", 500000]
]
```

Each company record follows this structure:

```text
[Company Number, Company ID, Company Name, Donation Amount]
```

## Main Functions

| Function | Purpose |
|---|---|
| `amount_donated()` | Displays donating companies and calculates the total donation amount |
| `non_donating_companies()` | Displays companies that have not donated |
| `collect_donation(company_no)` | Records a donation for an eligible registered company |
| `add_new_company()` | Registers a new company or handles an existing company |
| `print_menu()` | Displays the available menu options |

## Program Menu

```text
Menu:
1 >> View Companies and Total Donations
2 >> View Registered Companies That Haven't Donated
3 >> Make a Donation
4 >> Add New Company to the Registry
5 >> Print Menu Again
0 >> Exit the Program
```

## How to Run

### Using Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Select **File > Upload notebook**.
3. Upload `CSC101L_Final_Project_(NGO DONATION MANAGEMENT).ipynb`.
4. Run the code cell.
5. Enter a menu option when prompted.

### Using Jupyter Notebook

1. Install Jupyter Notebook if it is not already installed.

```bash
pip install notebook
```

2. Start Jupyter Notebook.

```bash
jupyter notebook
```

3. Open the project notebook.
4. Run the code cell.
5. Use the console prompts to operate the system.

## Example Output

```text
Company No      Company Id      Company Name        Amount
02              5682008         Walton              500000
04              5681940         Akij                700000
06              5681978         Aarong              200000
07              5681974         Jamuna Group        175000

Total Donated Amount = 1575000 Tk
```

## Donation Rules

* The minimum accepted donation is **100,000 Tk**.
* A company may be registered with a donation amount of `0`.
* A company that has already donated cannot donate again through the donation menu.
* A company name cannot be registered more than once.
* Company name matching is case-insensitive.

## Initial Dataset

The notebook contains ten initially registered companies, including:

* Grameenphone
* Walton
* Nestlé Bangladesh Ltd.
* Akij
* ACI Ltd.
* Aarong
* Jamuna Group
* Sheltech
* ACME Laboratories Ltd.
* Transcom Group

The initial total donation amount is **1,575,000 Tk**.

## Current Limitations

* Data is stored only in memory and is lost when the program stops.
* Company IDs are not checked for duplicates.
* Non-numeric input may cause an error where an integer is expected.
* Donation history and transaction dates are not stored.
* A company that has already donated cannot submit an additional donation.
* The project does not currently use a graphical user interface or database.

## Possible Future Improvements

* Store company and donation records in a file or database
* Add exception handling for invalid user input
* Support multiple donations from the same company
* Maintain complete donation history
* Add search, update, and delete options
* Generate downloadable donation reports
* Add administrator authentication
* Create a graphical or web-based interface

## Project File

```text
CSC101L_Final_Project_(NGO DONATION MANAGEMENT).ipynb
```

## Course

**Course:** CSC101L  
**Project:** Final Project  
**Project Type:** NGO Donation Management System

## License

This project is intended for academic and educational use.

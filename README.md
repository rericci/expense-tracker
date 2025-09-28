# expense-tracker
A Python-based tool to automatically consolidate and categorize personal expenses from multiple banks (only Amex in this version).
It merges new transactions into a master Excel file, applies category mapping, and updates the mapping file dynamically.

🚀 **Features**

📂 Reads bank exports from the Input/ folder:

Amex_test (.xlsx)


🧹 Cleans and normalizes data across banks (date format, amounts, descriptions).

🏷️ Applies categories automatically:

From mapping_categories_test.xlsx

From historical transactions (if a description was already categorized)

🔄 Updates mapping_categories_test.xlsx with new description–category pairs.

📊 Saves a unified master file (expenses_tracker_test.xlsx) with all transactions.

├── Input/ # Drop your bank statements here
│ └── amex_test.xlsx # Example Amex test file
├── mapping_categories_test.xlsx # Mapping file: keyword → category
├── expenses_tracker_test.xlsx # Master file with all transactions
├── Automate_expenses_tracking_test.py
└── README.md


📑 **Output Format**


The master Excel (expenses_tracker_test.xlsx) contains:

Date	Description	Amount	Origin	Category	TypeTransaction	TypeExpense
2025-09-21	Coop	100.00	Amex	Groceries	Expense	Fixed
2025-09-20	McDonalds	30.00	N26	Eating Out	Expense	Variable
⚙️ Requirements

Python 3.10+

Dependencies:

pip install pandas openpyxl

▶️ **Usage**

Place your bank export files into the Input/ folder.

Run the script:

python Automate_expenses_tracking.py


The script will:

Import new transactions

Deduplicate

Apply categories

Save results in expenses_tracker.xlsx

Update mapping_categories.xlsx


# Singlish Translator Test Automation

This project is created to automate testing process of Singlish Translator website using Python and Playwright.

The automation script reads test cases from Excel file, enter inputs automatically to the website, capture translated outputs, compare expected outputs and save results back to Excel file.

---

# Technologies Used

- Python
- Playwright
- Openpyxl
- Excel
- VS Code

---

# Project Structure

```text
test_automation/
│
├── test_automation.py
├── Assignment 1 - Test cases.xlsx
├── README.md
```

---

# Prerequisites

Before running this project install following software.

- Python 3.11 or above
- Google Chrome
- VS Code (recommended)

---

# Step 1 - Install Python

Download and install Python:

https://www.python.org/downloads/

Important:

During installation tick:

```text
Add Python to PATH
```

After installation check Python version using terminal.

```bash
python --version
```

Example output:

```bash
Python 3.13.7
```

---

# Step 2 - Install VS Code

Download and install VS Code:

https://code.visualstudio.com/

---

# Step 3 - Extract Project Folder

Move ZIP file to D drive and extract it.

Example:

```text
D:\test_automation
```

Inside extracted folder there should be:

```text
test_automation.py
Assignment 1 - Test cases.xlsx
```

---

# Step 4 - Open Project in VS Code

Open VS Code.

Click:

```text
File -> Open Folder
```

Select project folder.

Example:

```text
D:\test_automation\test_automation
```

---

# Step 5 - Open Terminal

Open VS Code terminal using:

```text
Terminal -> New Terminal
```

or press:

```text
CTRL + `
```

---

# Step 6 - Navigate to Project Folder

Run below command in terminal.

```powershell
cd D:\test_automation\test_automation
```

---

# Step 7 - Install Required Packages

Run below commands one by one.

## Update pip

```bash
python -m pip install -U pip
```

## Install dependencies

```bash
pip install playwright openpyxl
```

## Install Playwright browsers

```bash
playwright install
```

---

# Step 8 - Add Test Cases to Excel File

Open Excel file:

```text
Assignment 1 - Test cases.xlsx
```

Fill only below columns:

- TC ID
- Input length type
- Input
- Expected output

Do not fill:

- Actual output
- Status

These columns automatically updated by automation script.

Save and close Excel file before running automation.

---

# Step 9 - Run Automation Script

Run below command in terminal.

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

---

# What Automation Does

Automation script will:

- Open browser automatically
- Open Singlish Translator website
- Read test cases from Excel
- Type inputs automatically
- Capture translated outputs
- Compare expected and actual outputs
- Save results to Excel file automatically

---

# Output

After execution Excel file automatically updates:

- Actual output
- PASS / FAIL status

---

# Notes

- Excel file must be closed before running automation.
- Internet connection is required.
- Browser may remain open because `--keep-open` option is used.

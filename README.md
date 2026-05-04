# Playwright Negative Test Automation

This project runs 50 negative Singlish-to-Sinhala test cases using Playwright and records outputs in the Excel sheet.

## 1) Install prerequisites (one-time)

- Install Python 3.11 or 3.12.
- Install Google Chrome (recommended), or let Playwright install Chromium.

## 2) Set up the project environment

1. Save the provided ZIP file to your D: drive.
2. Extract it so your project path is D:\test_automation.
3. Open Command Prompt.
4. Navigate to the extracted folder:

```cmd
cd /d D:\test_automation
```

## 3) Install required dependencies (one-time)

From D:\test_automation, run:

```cmd
pip install -U pip
pip install playwright openpyxl
playwright install
```

## 4) Run the automation

From D:\test_automation, run:

```cmd
python test_automation.py --excel "test_automation/ Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

## 5) Check results

1. Go to the test_automation folder.
2. Reopen the Excel file.
3. Verify that values under Actual output and Status are correctly recorded.

## 6) Add additional columns to Excel

After review, add these two columns next to Status:

- Singlish input types covered
- Evidence or rationale for the input type covered

Manually fill both columns based on your assessment, using Appendix 2 template style.

## Current repository state

- Contains 50 negative test cases.
- Status is set to FAIL for all 50 negative cases.
- Includes the two additional columns with populated values.

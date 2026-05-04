# Playwright Negative Test Automation

This repository runs 50 negative Playwright test cases from the provided Excel workbook and writes the live execution results back to the workbook.

## Files

- `test_automation.py` - Playwright runner that reads the test cases from Excel, executes the UI flow, and writes `Actual output` and `Status` values.
- `Assignment 1 - Test cases.xlsx` - Source workbook with the 50 negative test cases, categorized by Singlish input type.
- `requirements.txt` - Python dependencies.

## Prerequisites

- Python 3.9 or newer
- Microsoft Edge / Chromium browser support for Playwright

## Install

```powershell
py -3.9 -m pip install -r requirements.txt
py -3.9 -m playwright install chromium
```

## Run the tests

```powershell
py -3.9 .\test_automation.py --headless
```

By default, the script reads the workbook in this folder, runs all rows in the sheet named ` Test cases`, and records the actual output plus a `PASS`, `FAIL`, or `UI Error` status.

## Test Coverage

The 50 negative test cases cover the following Singlish input types:

- Question forms
- Requests
- Inputs with punctuation marks
- Romanization and spelling variants
- Isolated English word insertions
- Multi-word English phrases
- English digital terms
- Platform/app names
- Time formats
- Slang and casual phrasing
- Extended messages with multiple sentences
- Special characters and emojis
- Mixed language code-switching

## Notes

- All 50 test cases are marked as FAIL, indicating the system did not correctly convert these Singlish inputs to Sinhala (as expected for negative test cases).
- The workbook includes detailed categorization of input types in the "Singlish input types covered" column.
- Evidence and rationale for each categorization is provided in the "Evidence or rationale for the input type covered" column.

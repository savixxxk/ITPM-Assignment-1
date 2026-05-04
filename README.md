# Playwright Negative Test Automation

This repository runs 50 negative Playwright test cases from the provided Excel workbook and writes the live execution results back to a results workbook.

## Files

- `test_automation.py` - Playwright runner that reads the test cases from Excel, executes the UI flow, and writes `Actual output` and `Status` values.
- `Assignment 1 - Test cases.xlsx` - Source workbook with the 50 negative test cases.
- `Assignment 1 - Test cases.results.xlsx` - Saved execution results from the latest run.
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
py -3.9 .\test_automation.py --headless --output ".\Assignment 1 - Test cases.results.xlsx"
```

By default, the script reads the workbook in this folder, runs all rows in the sheet named ` Test cases`, and records the actual output plus a `PASS`, `FAIL`, or `UI Error` status.

## Notes

- The current workbook contains 50 negative cases.
- The execution results in `Assignment 1 - Test cases.results.xlsx` are based on the actual Playwright run captured in this workspace.
- If the source workbook is open in Excel, the script can still write to the separate results workbook.

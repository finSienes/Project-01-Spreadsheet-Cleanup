# Project 01 — Spreadsheet Cleanup Automation

## Overview

A local workflow automation project built with n8n and JavaScript. It reads a CSV file containing customer records, checks for common data-quality problems, and produces separate CSV reports for clean records and records that need review.

## Problem

Spreadsheet data can contain duplicate customer IDs, missing information, and invalid email addresses. Checking these problems manually can take time and lead to mistakes.

## Solution

This workflow automates basic data validation and separates records into two output files.

## Tools Used

- **n8n** — workflow automation and file processing
- **JavaScript** — validation rules and record classification
- **CSV** — input and output data format
- **openSUSE Linux** — local development environment

## Workflow

1. Read the input CSV file.
2. Extract the CSV rows into individual records.
3. Check customer IDs, names, email addresses, and cities.
4. Identify duplicate IDs, missing values, and invalid email addresses.
5. Separate clean records from records that need review.
6. Generate two CSV output files.

## Test Results

Tested with 10 sample customer records:

- 5 clean records
- 5 records flagged for review
- 1 clean-record CSV generated
- 1 issues-report CSV generated

## Output Files

- `cleaned_customers.csv` — records that passed the configured checks
- `customer_issues.csv` — records flagged with an explanation of the issue

## Data and Limitations

The input data is synthetic and does not represent real customers.

The workflow flags problematic records; it does not automatically invent missing information or repair invalid data. Duplicate IDs are flagged for review rather than silently removed from the original source.

This is a small proof-of-concept project. It has been tested locally with the sample dataset and is not yet a production system.

## My Contribution

I configured the n8n workflow, implemented JavaScript validation rules, tested the workflow with sample CSV data, and verified that both output files were generated successfully.

## Possible Improvements

- Generate an automated summary report.
- Handle different CSV formats and larger datasets.
- Add more validation rules and test cases.
- Improve error handling and documentation.
- Prepare a repeatable demo using synthetic data.

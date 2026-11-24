# Week 5 – Token Economics: LLM Budget Planner

## Overview

This practical focuses on estimating token consumption, API costs, and provider rate-limit capacity before implementing an LLM-powered feature.

A reusable Python budgeting tool is developed to calculate estimated usage and cost, check RPM and TPM limits, evaluate budget constraints, and generate a final GO or REVISE recommendation.

## Project Structure

```text
week5/
└── TokenEconomics/
    ├── .env
    ├── .gitignore
    ├── budget.py
    ├── requirements.txt
    └── test_budget.py
```

## Features

- Estimates daily input and output token consumption.
- Calculates daily and monthly API costs.
- Checks Requests Per Minute (RPM) limits.
- Checks Tokens Per Minute (TPM) limits.
- Applies a configurable safety margin.
- Checks daily and monthly budget constraints.
- Generates a final GO or REVISE recommendation.
- Includes automated unit tests.

## Technologies Used

- Python
- python-dotenv
- Python unittest
- PowerShell
- Visual Studio Code

## Prerequisites

- Python 3.x
- pip (Python package manager)
- Visual Studio Code

## Configuration

The `.env` file contains the assumptions used by the budget planner.

Example configuration:

```env
INPUT_PRICE_PER_MILLION=0.30
OUTPUT_PRICE_PER_MILLION=1.20

REQUESTS_PER_DAY=2000
AVG_INPUT_TOKENS=1200
AVG_OUTPUT_TOKENS=300
PEAK_REQUESTS_PER_MINUTE=30

RPM_LIMIT=60
TPM_LIMIT=100000

MONTHLY_BUDGET_USD=50
DAILY_BUDGET_USD=2
SAFETY_MARGIN_PERCENT=20
```

*Note: These are illustrative planning values, not guaranteed current API prices or provider limits.*

## Setup and Execution

### 1. Navigate to the project folder

```powershell
cd week5\TokenEconomics
```

### 2. Create a virtual environment

```powershell
py -m venv .venv
```

### 3. Activate the virtual environment

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```powershell
python -m pip install -r requirements.txt
```

### 5. Run the budget planner

```powershell
python budget.py
```

## Sample Results

| Metric | Result |
|---|---:|
| Input tokens/day | 2,400,000 |
| Output tokens/day | 600,000 |
| Total tokens/day | 3,000,000 |
| Estimated daily cost | $1.44 |
| Estimated monthly cost | $43.20 |
| Peak RPM with margin | 36 |
| Peak TPM with margin | 54,000 |

### Limit Checks

| Check | Result |
|---|---|
| RPM limit | PASS |
| TPM limit | PASS |
| Daily budget | PASS |
| Monthly budget | REVIEW |

**Recommendation: REVISE**

The monthly budget check fails because the estimated monthly cost with a 20% safety margin is $51.84, which exceeds the configured $50 budget.

## Automated Testing

Run the test suite using:

```powershell
python -m unittest -v
```

### Test Cases

1. `test_cost_estimate` – Verifies daily and monthly cost calculations.
2. `test_capacity_passes` – Verifies RPM and TPM capacity checks.
3. `test_rpm_limit_fails` – Verifies RPM limit failure handling.
4. `test_monthly_budget_fails` – Verifies monthly budget failure handling.

**Test Result:** 4 tests passed successfully.

## Files Description

| File | Description |
|---|---|
| `budget.py` | Main budgeting and cost calculation implementation |
| `test_budget.py` | Automated unit tests |
| `requirements.txt` | Required Python dependency |
| `.env` | Configuration and planning assumptions |
| `.gitignore` | Excludes virtual environments and local configuration files |

## Conclusion

This experiment demonstrates how token usage, API pricing, rate limits, and budget constraints can be evaluated before deploying an LLM-powered feature.

It provides a reusable budgeting approach to help determine whether a planned feature is financially and technically feasible.

## Author

**Deepak**

**Repository:** [GenAI Practicals](https://github.com/jaswanthbhaskar-elite/GenAI-2520030553-Jaswanthbhaskar)

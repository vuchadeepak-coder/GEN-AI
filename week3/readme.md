# Week 3 – LLM Client and Usage Logging

## Overview

This folder contains the Week 3 Generative AI practical implementation, extending the LLM client project with a separate usage logging component.

The project follows a modular structure, separating the LLM client, main execution program, usage logger, and automated tests.

## Project Structure

```text
week3/
├── llm_client.py
├── main.py
├── requirements.txt
├── test_client.py
└── usage_logger.py
```

## Technologies Used

- Python
- Large Language Models (LLMs)
- Python unittest

## Prerequisites

- Python 3.x
- pip (Python package manager)
- Visual Studio Code

## Setup and Execution

### 1. Navigate to the Week 3 folder

```powershell
cd week3
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

### 5. Run the program

```powershell
python main.py
```

## Files Description

| File | Description |
|---|---|
| `llm_client.py` | Contains the LLM client implementation |
| `main.py` | Main program for executing the practical |
| `usage_logger.py` | Handles usage logging functionality |
| `test_client.py` | Contains automated tests for the LLM client |
| `requirements.txt` | Lists required Python dependencies |

## Running Tests

Run the automated tests using:

```powershell
python -m unittest -v
```

## Author

**Deepak**

**Repository:** [GenAI Practicals](https://github.com/jaswanthbhaskar-elite/GenAI-2520030553-Jaswanthbhaskar)

# Week 2 – LLM Client

## Overview

This folder contains the Week 2 Generative AI practical implementation, introducing a modular Large Language Model (LLM) client using Python.

The project separates the LLM client implementation, main execution program, and automated tests into individual files.

## Project Structure

```text
week2/
├── llm_client.py
├── main.py
├── requirements.txt
└── test_client.py
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

### 1. Navigate to the Week 2 folder

```powershell
cd week2
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
| `test_client.py` | Contains automated tests for the client |
| `requirements.txt` | Lists required Python dependencies |

## Running Tests

Execute the following command to run the automated tests:

```powershell
python -m unittest -v
```

## Author

**Jaswanth Bhaskar**

**Repository:** [GenAI Practicals](https://github.com/jaswanthbhaskar-elite/GenAI-2520030553-Jaswanthbhaskar)

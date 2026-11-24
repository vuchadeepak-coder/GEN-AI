# Week 4 – Tokenizer Comparison: BPE, WordPiece and SentencePiece

## Overview

This practical explores and compares three popular tokenization techniques used in Natural Language Processing (NLP) and Large Language Models.

The implementation uses Hugging Face Transformers to compare how different tokenizers process English, Telugu, and Hindi text.

## Project Structure

```text
week4/
├── .gitignore
├── .venv/
├── .vscode/
├── requirements.txt
└── tokenizer_comparison.py
```

## Tokenization Techniques

| Technique | Model Used |
|---|---|
| BPE (Byte Pair Encoding) | GPT-2 |
| WordPiece | Multilingual BERT |
| SentencePiece | XLM-R |

## Languages Tested

- English
- Telugu
- Hindi

## Technologies Used

- Python
- Hugging Face Transformers
- SentencePiece
- GPT-2
- Multilingual BERT
- XLM-R

## Prerequisites

- Python 3.x
- pip (Python package manager)
- Visual Studio Code
- Internet connection for downloading pretrained tokenizer files

## Setup and Execution

### 1. Navigate to the Week 4 folder

```powershell
cd week4
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
python tokenizer_comparison.py
```

## Experimental Results

Token counts obtained from the tested English, Telugu, and Hindi examples:

| Language | GPT-2 (BPE) | mBERT (WordPiece) | XLM-R (SentencePiece) |
|---|---:|---:|---:|
| English | 8 | 10 | 10 |
| Telugu | 112 | 18 | 14 |
| Hindi | 68 | 17 | 14 |

*Note: Counts include special tokens.*

## Observations

1. GPT-2 produced significantly more tokens for Telugu and Hindi compared to the multilingual models.
2. Multilingual BERT and XLM-R handled the tested non-English examples more efficiently.
3. XLM-R produced the fewest tokens for the Telugu and Hindi examples.
4. Tokenization efficiency varies depending on the language and tokenizer vocabulary.

## Conclusion

This experiment demonstrates how different tokenization techniques affect text representation across multiple languages. It highlights the importance of multilingual tokenizers when working with languages beyond English.

## Author

**Deepak**

**Repository:** [GenAI Practicals](https://github.com/jaswanthbhaskar-elite/GenAI-2520030553-Jaswanthbhaskar)

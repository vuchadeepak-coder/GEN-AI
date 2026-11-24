# Week 1 – First LLM API Call using OpenAI

## 📌 Overview
This project demonstrates how to connect a Python application to a Large Language Model (LLM) using the OpenAI API. It sends a prompt to an AI model and displays the generated response in the terminal.

## 🎯 Objectives
- Understand how APIs connect Python applications with AI models.
- Make a first LLM API call using Python.
- Learn how to use the OpenAI Python SDK.
- Store API keys securely using environment variables and a `.env` file.
- Generate AI responses from user prompts.
- Understand basic API error handling and troubleshooting.

## 🛠️ Technologies Used
- Python
- OpenAI API
- OpenAI Python SDK
- python-dotenv
- Visual Studio Code

## 📂 Project Structure
```text
Week1/
├── main.py
├── requirements.txt
├── .env
└── .gitignore
```

## ⚙️ How It Works
1. Loads the API key from the `.env` file.
2. Initializes the OpenAI client.
3. Sends a prompt to the AI model using the API.
4. Receives the AI-generated response.
5. Displays the response in the terminal.

## ▶️ How to Run
1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Create a `.env` file and add your API key:
   ```env
   OPENAI_API_KEY=your_api_key_here
   ```
3. Run the Python program:
   ```bash
   python main.py
   ```

## 📚 What I Learned
- How to connect Python with an AI model through an API.
- How API keys are used for authentication.
- How to securely store API keys using environment variables.
- How to send prompts and receive responses from an LLM.
- How to use the OpenAI Python SDK.

## ✅ Expected Output
The program displays an AI-generated answer to the prompt:

**"What is Artificial Intelligence? Explain in simple words."**

The response is generated dynamically by the AI model.

## 🔐 Security
API keys and environment files are excluded from Git using `.gitignore` to prevent sensitive information from being exposed.

---
*Week 1 Generative AI Lab Assignment*


# 🧠 AI Quiz Generator (LangChain + OpenAI)

## 📌 Overview

Creating educational content manually can be time-consuming and repetitive. This project automates quiz generation using AI by producing beginner-level questions and detailed answers in seconds.

The application is built using **LangChain’s chain composition**, where complex tasks are broken into smaller, focused steps and executed sequentially.

---

## ⚙️ How It Works

The quiz generator uses two main chains:

1. **Question Generation Chain**

   * Takes a topic as input
   * Generates a beginner-level quiz question

2. **Answer Generation Chain**

   * Takes the generated question
   * Produces a detailed answer with explanation

These are connected using a **SequentialChain**, which automatically passes data between steps.

---

## 🧱 Tech Stack

* Python
* LangChain (`LLMChain`, `SequentialChain`)
* OpenAI API
* Jupyter Notebook

---

## 🧩 Key Concepts

* **PromptTemplate** – defines structured prompts with dynamic variables
* **LLMChain** – connects prompts to the language model
* **SequentialChain** – manages multi-step workflows and data flow

---

## 🚀 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/infoagambisa-source/langchain-mini-quiz-generator.git
cd langchain-mini-quiz-generator
```

---

### 2. Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 API Key Setup

This project uses the OpenAI API.

### Create a `.env` file in the project root:

```bash
OPENAI_API_KEY=your_api_key_here
```

### Load it in the notebook:

```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("OPENAI_API_KEY")
```

⚠️ **Important:**

* Never commit your `.env` file
* Ensure `.env` is included in `.gitignore`

---

## ▶️ Running the Project

Run the notebook and execute:

```python
topic = input("Enter a topic for your quiz: ")
response = quiz_chain.invoke({"topic": topic})
```

### Example Output

```
Topic: Photosynthesis

Question:
What is the role of chlorophyll in photosynthesis?

Answer:
Chlorophyll absorbs sunlight and converts it into energy used to produce glucose from carbon dioxide and water. This process enables plants to create their own food.
```

---

## ⚠️ Note on API Usage

This project requires an active OpenAI API key with billing enabled.

If you encounter this error:

```
RateLimitError: insufficient_quota
```

It means:

* Billing is not set up, or
* API credits have been exhausted

---

## 📁 Project Structure

```
langchain-mini-quiz-generator/
│
├── LC_MiniQuizGen.ipynb
├── requirements.txt
├── .gitignore
├── .env.example
└── README.md
```

---

## 🧠 What I Learned

* How to build multi-step AI workflows using LangChain
* How SequentialChain manages data flow between components
* Handling environment variables securely
* Managing dependency compatibility in real-world projects

---

## 🚧 Future Improvements

* Add multiple-choice question support
* Introduce difficulty levels
* Build a Streamlit or Flask UI
* Store quiz history in a database

---

## 📄 License

This project is for educational purposes.

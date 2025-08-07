# 💡 Gemini-Powered SQL Query Generator (Streamlit + LangChain)

This is a lightweight Streamlit-based application that lets users **ask questions in plain English**, which are then **converted to SQL queries using Google's Gemini-1.5-Flash LLM**. The query is executed on a connected **MySQL database**, and the results are displayed on the screen.

---

## 🚀 Features

- 🌐 Converts natural language questions into SQL using **LangChain** + **GoogleGenerativeAI**
- 🛢️ Executes the generated query on a **MySQL database** via **SQLAlchemy**
- ⚡ Displays both the generated SQL and the query results on the UI
- 📦 Uses `dotenv` to load Gemini API Key from `.env`
- 🧠 Powered by **Gemini-1.5-Flash**
- 🖥️ Simple and clean **Streamlit UI**

---

## 🛠️ Tech Stack

- Python 🐍
- Streamlit
- LangChain
- Google Generative AI (Gemini-1.5-Flash)
- SQLAlchemy
- MySQL (via PyMySQL)
- dotenv

---

## 📁 File Structure

```
project/
├── main.py               # Your main Streamlit app file
├── .env                  # Holds your Gemini API Key
└── README.md             # This file
```

---

## 🔑 .env Format

Create a `.env` file in the root directory and add:

```
GEMINI_API_KEY=your_google_gemini_api_key
```

---

## 🧑‍💻 Setup Instructions

1. **Clone the repository** (or copy the code into a Python file):

    ```bash
    git clone https://github.com/your-username/your-repo.git
    cd your-repo
    ```

2. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

    Or install individually:

    ```bash
    pip install streamlit langchain sqlalchemy pymysql python-dotenv langchain-google-genai langchain-community
    ```

3. **Set up your MySQL Database**:

    Ensure you have a MySQL database running with the following credentials:

    ```
    user:     root
    password: Sathwik
    host:     localhost
    database: retail_sales_db
    ```

4. **Run the App**:

    ```bash
    streamlit run main.py
    ```

---

## 📷 App Preview

> 👤 **User enters a natural language question** like:
>  
> _"What are the total sales for each product in the last month?"_

🔁 The app:

- Sends the question to Gemini via LangChain
- Gemini responds with a SQL query
- Query is run on your MySQL DB
- Results are shown neatly in the UI

---
##Screenshot
Once you run this you will see this
<img width="778" height="139" alt="image" src="https://github.com/user-attachments/assets/b5dca2d4-3543-4af6-9dbb-70f6a3372c39" />
your front end is this
<img width="1174" height="561" alt="image" src="https://github.com/user-attachments/assets/2064ed9d-3b8d-4083-866a-206f2c2047a9" />
once you ask the question it gonna retreive information from our SQL database through SQL query you will get the answer
<img width="1270" height="711" alt="image" src="https://github.com/user-attachments/assets/02a7c907-089a-464c-84b3-0b3296a3c9ed" />



## ⚠️ Error Handling

If the SQL execution fails (e.g., due to a bad query or wrong DB schema), the app catches the `ProgrammingError` and shows a user-friendly message in Streamlit.

---


Crafted for demonstration and interview readiness by someone who codes with ❤️ and curiosity.

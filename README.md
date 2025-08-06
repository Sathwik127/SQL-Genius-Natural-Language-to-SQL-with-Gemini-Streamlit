# SQL-Genius-Natural-Language-to-SQL-with-Gemini-Streamlit
SQL-Genius is a Streamlit-powered application that transforms natural language questions into accurate SQL queries using Google Gemini (via LangChain). It executes the queries on a MySQL-based retail sales database and displays the results instantly. Ideal for non-technical users who want insights from structured data without writing any SQL.
# 🧠 SQL-Genius: Natural Language to SQL with Gemini + Streamlit

**SQL-Genius** is a natural language interface to structured data. It takes your question in plain English, converts it into SQL using **Google Gemini (via LangChain)**, runs it on a **MySQL database**, and displays the results—all through a simple **Streamlit** web UI.

---

## 🚀 Features

- 💬 Ask questions like:  
  `"What were the top 5 products sold last month?"`  
  `"Show total sales by region for Q1 2024."`

- 🤖 Powered by **Google Gemini 1.5 Flash** for generating SQL.

- 🧠 Uses **LangChain** for LLM chaining and SQL generation.

- 🗄️ Connects to a **MySQL retail_sales_db** with SQLAlchemy.

- 📊 Displays query + result interactively via **Streamlit**.

---

## 📦 Tech Stack

| Component    | Description                      |
|--------------|----------------------------------|
| LangChain    | LLM-based SQL generation         |
| Google Gemini| LLM provider                     |
| Streamlit    | Front-end web app UI             |
| SQLAlchemy   | Database connection              |
| MySQL        | Relational database (retail)     |
| Python dotenv| For secure API key management    |

---

## 🔧 Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/sql-genius.git
cd sql-genius
2. Create Virtual Environment (optional but recommended)
bash
Copy code
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy code
pip install -r requirements.txt
4. Set Up .env
Create a .env file in the root folder:

env
Copy code
GEMINI_API_KEY=your_google_api_key
Make sure you have access to Google Generative AI and have enabled the Gemini API.

5. Configure MySQL Connection
Edit app.py with your MySQL credentials:

python
Copy code
db_user = "root"
db_password = "yourpassword"
db_host = "localhost"
db_name = "retail_sales_db"
▶️ Run the App
bash
Copy code
streamlit run app.py
Then open your browser to http://localhost:8501

🧪 Example Usage
Question: "What are the top 3 selling products by revenue?"

Generated SQL: SELECT product_name, SUM(revenue) FROM sales GROUP BY product_name ORDER BY SUM(revenue) DESC LIMIT 3;

Result: (Displayed in Streamlit UI)

📄 requirements.txt
nginx
Copy code
streamlit
langchain
langchain-community
langchain-core
langchain-google-genai
sqlalchemy
pymysql
python-dotenv
Save this as requirements.txt and install using:

bash
Copy code
pip install -r requirements.txt
📌 Notes
Supports only MySQL out-of-the-box (can be extended to Postgres or SQLite).

Make sure your DB is running and populated with data before using the app.

sample_rows_in_table_info=3 is used to assist Gemini with schema comprehension.

📄 License
This project is for academic and educational purposes.
All external packages and APIs follow their respective licenses.

👤 Author
[Your Name]
Capstone Project – [Your Institution or Course]
GitHub: @your-username


# 🛒 AI Customer Support Agent with Memory

This is a Streamlit-based AI customer support chatbot that uses OpenAI’s GPT and `mem0` to remember past interactions, provide contextual responses, and even preload customer history from Amazon reviews or generate synthetic customer profiles.

---

## 💡 Features

- 💬 **Chat UI** with Streamlit for natural interaction
- 🧠 **Memory system** powered by `mem0` to:
  - Store and retrieve past conversations
  - Recall customer-specific history
- 📦 **Preloaded memories** from Amazon product reviews
- 🧪 **Synthetic customer data generation** for demos and simulations
- 📚 **Memory browser**: view stored interactions by customer ID

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ai-customer-support-agent.git
cd ai-customer-support-agent
2. Create environment and install dependencies
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
📌 Note: Please ensure mem0, openai, streamlit, pandas, and qdrant-client are included in requirements.txt.

🔧 Setup
Ensure Qdrant is running locally on port 6333.

Install Qdrant

Prepare your Amazon.csv file with review data:

Must contain columns: Customer ID, Text, Summary

File path expected: C:/Users/swathiga/Downloads/Amazon.csv (or modify it in the code)

Add your OpenAI API Key in the app when prompted.

▶️ Running the App
bash
Copy
Edit
streamlit run customer_support_agent.py
Then open your browser at http://localhost:8501.

🧭 How to Use
Enter your OpenAI API key

Provide a Customer ID in the sidebar

Chat with the support agent

Use sidebar buttons to:

🔁 Generate synthetic data

👤 View stored customer profile

🧠 View memory of past interactions

🧠 Memory Functionality
Memories are stored per customer (user_id)

New queries and responses are added to memory

Search queries retrieve relevant past conversations

🧪 Synthetic Data Generation
Uses GPT to create:

Customer profile

Past orders

Previous support queries

Stored directly in memory for simulation

📁 Project Structure
bash
Copy
Edit
├── customer_support_agent.py   # Main application file
├── Amazon.csv                  # Optional review data (user-provided)
├── requirements.txt            # Required dependencies
└── README.md                   # Project documentation
🧠 Tech Stack
Streamlit

OpenAI GPT-3.5

mem0

Qdrant (vector memory store)

Pandas

📄 License
MIT License — Free to use and modify.

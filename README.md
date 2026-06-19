# 🚀 LCEL Translation API using LangChain, LangServe & Groq

A production-ready translation API built using **LangChain Expression Language (LCEL)**, **LangServe**, **FastAPI**, and **Groq's Llama 3.1 8B Instant** model.

This project demonstrates how to create and deploy a LangChain pipeline as a REST API using LangServe while leveraging Groq's ultra-fast inference capabilities.

---

## 📌 Features

- ⚡ Fast LLM inference with Groq
- 🔗 Built using LangChain Expression Language (LCEL)
- 🌐 REST API deployment via LangServe
- 🚀 FastAPI backend
- 📝 Dynamic prompt templating
- 🔄 Structured output parsing
- 🌍 Multi-language translation support
- 🏗️ Minimal and modular architecture

---

## 🛠 Tech Stack

- Python
- FastAPI
- LangChain
- LangServe
- Groq API
- Llama 3.1 8B Instant
- Uvicorn
- python-dotenv

---

## 📂 Project Structure

```text
.
├── serv.py
├── .env
├── LICENSE
├── README.md
└── .gitattributes
```

---

## 🧠 How It Works

The application creates an LCEL chain:

```python
chain = prompt | model | output_parser
```

### Workflow

```text
User Input
    │
    ▼
Prompt Template
    │
    ▼
Llama 3.1 8B Instant (Groq)
    │
    ▼
Output Parser
    │
    ▼
Translated Text
```

---

## ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/lcel-translation-api.git
cd lcel-translation-api
```

### Create Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux / macOS

```bash
python -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install fastapi
pip install uvicorn
pip install langchain
pip install langchain-groq
pip install langserve
pip install python-dotenv
```

## 🔑 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key
```

Get your API key from:

https://console.groq.com

---

## 🚀 Running the Application

Start the server:

```bash
python serv.py
```

The API will be available at:

```text
http://localhost:8000
```

---

## 📡 API Endpoints

### LangServe Playground

```text
http://localhost:8000/chain/playground/
```

### Invoke Endpoint

```text
POST /chain/invoke
```

### Sample Request

```json
{
  "input": {
    "language": "French",
    "text": "Hello, how are you?"
  }
}
```

### Sample Response

```json
{
  "output": "Bonjour, comment allez-vous ?"
}
```

---

## 🔍 Model Configuration

The application uses:

```python
ChatGroq(
    model="llama-3.1-8b-instant"
)
```

### Why Groq?

- Low latency inference
- High translation quality
- Cost-efficient deployment
- Production-grade performance
- Groq LPU™ AI Inference Technology

---

## 🏗 Core Components

### Prompt Template

```python
generic_template = "Translate the following into {language}:"
```

### Model

```python
ChatGroq(model="llama-3.1-8b-instant")
```

### Output Parser

```python
StrOutputParser()
```

### Chain

```python
chain = prompt | model | output_parser
```

---

## 📚 Learning Outcomes

This project demonstrates:

- LangChain fundamentals
- LangChain Expression Language (LCEL)
- Prompt Engineering
- FastAPI integration
- LangServe deployment
- Groq API integration
- REST API development
- LLM application deployment

---

## 🔮 Future Improvements

- Language auto-detection
- Translation history
- User authentication
- Docker deployment
- LangSmith observability
- Frontend integration with Streamlit or React
- Conversation memory support
- Multiple model selection

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Osmium**

Electronics & Instrumentation Engineering  
National Institute of Technology Silchar

### Interests

- Artificial Intelligence
- Large Language Models
- Backend Development
- Agentic AI Systems
- Production AI Applications

---

⭐ If you found this project useful, consider giving it a star on GitHub!

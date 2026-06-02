# AI Machine Learning Tutor Chatbot

An AI-powered Machine Learning Tutor built using **FastAPI**, **LangChain**, and **Google Gemini**. The chatbot is designed to help beginners learn Artificial Intelligence and Machine Learning concepts through simple explanations, real-world examples, and interactive learning.

## Features

* Beginner-friendly AI & Machine Learning tutor
* Powered by Google Gemini LLM
* Built with FastAPI for high performance
* LangChain Expression Language (LCEL) implementation
* Topic-restricted responses (AI/ML only)
* Simple explanations with examples
* Follow-up questions for unclear queries
* Environment variable support for API keys
* Async request handling

## Tech Stack

* Python 3.11+
* FastAPI
* LangChain
* Google Gemini API
* Uvicorn
* Pydantic
* Python Dotenv

## Project Structure

```text
ai-ml-tutor-chatbot/
│
├── chatbot.py
├── requirements.txt
├── .env
├── .gitignore
├── README.md

```

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/ai-ml-tutor-chatbot.git

cd ai-ml-tutor-chatbot
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Virtual Environment

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=YOUR_GEMINI_API_KEY
```

## Run the Application

```bash
uvicorn chatbot:app --reload
```

Server will start at:

```text
http://127.0.0.1:8000
```

## API Endpoints

### Health Check

```http
GET /
```

Response:

```json
{
  "message": "AI ML Tutor Running"
}
```

### Chat Endpoint

```http
POST /chat
```

Request:

```json
{
  "question": "What is Machine Learning?"
}
```

Response:

```json
{
  "question": "What is Machine Learning?",
  "answer": "Machine Learning is..."
}
```

## LangChain LCEL Flow

```text
User Question
      │
      ▼
ChatPromptTemplate
      │
      ▼
Gemini LLM
      │
      ▼
StrOutputParser
      │
      ▼
Final Response
```

## System Prompt Behavior

The chatbot only answers questions related to:

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Neural Networks
* Data Science
* Generative AI
* Large Language Models (LLMs)
* NLP
* Computer Vision
* Reinforcement Learning
* MLOps

For non-AI/ML topics, the chatbot politely asks the user to ask AI or Machine Learning-related questions.

## Example Conversation

### User

```text
What is Supervised Learning?
```

### Bot

```text
Simple Explanation:
Supervised Learning is a machine learning technique where a model learns from labeled data.

Example:
Teaching a child to identify cats and dogs using labeled pictures.

Key Takeaway:
The model learns from examples with correct answers.
```

## Future Improvements

* Chat history and memory support
* MongoDB integration
* User authentication
* RAG (Retrieval-Augmented Generation)
* Vector Database integration
* Streaming responses
* Docker deployment
* Kubernetes deployment
* CI/CD pipeline

## Author

Vikash Kushwaha

Software Engineer | AI Engineer | IoT Engineer

## License

This project is licensed under the MIT License.

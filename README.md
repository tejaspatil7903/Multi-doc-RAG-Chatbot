# 📚 PDF Chat Assistant

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Python](https://img.shields.io/badge/python-3.10%2B-brightgreen)
![License](https://img.shields.io/badge/license-MIT-orange)

</div>

A powerful Streamlit-based chatbot that enables intelligent conversations with your PDF documents. Leveraging **HuggingFace embeddings** for semantic search and **Groq/Gemini LLM** for natural language understanding, this application provides accurate and context-aware responses to your questions.

## ✨ Features

<div align="center">
<table>
<tr>
<td>🔄 Multi-PDF Support</td>
<td>📊 Vector Embeddings</td>
<td>🔍 FAISS Search</td>
</tr>
<tr>
<td>💬 Chat Interface</td>
<td>🧠 Context Awareness</td>
<td>🗑️ Auto-Cleanup</td>
</tr>
</table>
</div>

- 📤 **Bulk Upload**: Process multiple PDF documents simultaneously
- 🔢 **Smart Vectorization**: Convert text to HuggingFace embeddings
- ⚡ **Fast Search**: Utilize FAISS for efficient similarity matching
- 💡 **Interactive Chat**: Engage in natural conversations through Streamlit
- 🔄 **Multi-turn Support**: Context-aware question reformulation
- 🧹 **Space Optimization**: Automatic cleanup of processed PDFs

## 🚀 Installation

1. **Clone the Repository**
```bash
git clone https://github.com/tejaspatil7903/Multi-doc-RAG-Chatbot.git
cd pdf-chat
2. **Set Up Environment**
```bash
# Create and activate virtual environment
python -m venv .venv

# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

3. **Install Dependencies**
```bash
# Core dependencies
pip install -r requirements.txt

# Choose your FAISS version
pip install faiss-cpu   # For CPU-only systems
# OR
pip install faiss-gpu   # For GPU acceleration (CUDA required)

# HuggingFace integration
pip install sentence-transformers langchain-huggingface
```

4. **Configure Environment Variables**
```bash
# Create .env file with your settings
LANGCHAIN_TRACING_V2=true
LANGCHAIN_API_KEY=your_api_key_here
```
## 💻 Usage

1. **Launch the Application**
```bash
streamlit run main.py
```

2. **Access the Interface**
- Open your browser to `http://localhost:8501`
- The modern Streamlit interface will welcome you

3. **Start Chatting**
- 📂 Upload PDFs through the sidebar
- ▶️ Click "Process" to analyze documents
- 💭 Type your questions in the chat
- 🤖 Receive AI-powered responses

## 🏗️ Architecture

<div align="center">
<table>
<tr>
<th>Component</th>
<th>Description</th>
</tr>
<tr>
<td><code>main.py</code></td>
<td>Streamlit application entry point</td>
</tr>
<tr>
<td><code>get_conversational_answer()</code></td>
<td>Async Q&A engine with LLM integration</td>
</tr>
<tr>
<td>FAISS</td>
<td>High-performance similarity search engine</td>
</tr>
<tr>
<td>HuggingFaceEmbeddings</td>
<td>Text-to-vector transformation engine</td>
</tr>
</table>
</div>

## ⚠️ Important Notes

- 🕒 Large PDFs may require extended processing time
- ⚙️ Verify FAISS and sentence-transformers installation
- 🗑️ PDFs are automatically removed post-processing

## 📦 Dependencies

- Python 3.10+
- Streamlit
- LangChain (langchain, langchain_huggingface)
- FAISS (CPU or GPU version)
- Sentence-Transformers



# 🧠 AI Study Assistant

An AI-powered study companion that helps students understand lecture material through intelligent question answering, slide summarization, PDF summaries, and flashcard generation. Built with LangChain, Hugging Face Transformers, and Gradio — and fully powered by open-source LLMs running on your local GPU.

---

## 🚀 Features

### 📄 Upload Lecture PDFs
Drag and drop any academic or lecture PDF — slides or notes.

### ❓ Ask Questions from Slides
Use natural language to ask:
- “Summarize Slide 4”
- “What is Linear Regression?”
- “What is covered under Artificial Neural Networks?”

Supports fuzzy slide matching and page number detection.

### 🧠 Full PDF Summarizer
Click one button to get a concise overview of the entire document.

### 📝 Flashcard Generator
Automatically generates Q&A-style flashcards from your material — perfect for revision and quizzes.

### 🧩 Slide Number Matching (Fuzzy Logic)
Queries like "Summarize Slide 5" are matched against actual page content using fuzzy logic for accurate results.

---
![image](https://github.com/user-attachments/assets/b0be2987-3971-45a3-91b6-a419c6ebccf2)
![Screenshot 2025-06-19 181347](https://github.com/user-attachments/assets/fb136bc8-5339-4eee-9fa0-cb07dac1a4fb)
![Screenshot 2025-06-19 181559](https://github.com/user-attachments/assets/45727f26-f502-44ac-8bc8-0cdfecd30a32)


---

## 🛠 Tech Stack

| Layer           | Tools Used |
|----------------|------------|
| **Frontend**    | Gradio (Python UI) |
| **LLM**         | Hugging Face Transformers (Phi-2 / Mistral 7B / Falcon) |
| **Framework**   | LangChain |
| **Vector DB**   | FAISS |
| **PDF Parsing** | PyMuPDF (via LangChain loaders) |
| **Embeddings**  | SentenceTransformers (MiniLM-L6-v2) |
| **Fuzzy Matching** | RapidFuzz |

---

## 📁 Project Structure

```
ai_tutor/
├── app.py
├── ui/
│   └── interface.py
├── modules/
│   ├── document_loader.py
│   ├── vector_store.py
│   ├── rag_pipeline.py
│   ├── llm_interface.py
│   ├── slide_mapper.py
│   ├── summarizer.py
│   └── flashcards.py
├── data/
│   └── (your PDFs here)
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/ai-study-assistant.git
cd ai-study-assistant
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the app
```bash
python -m ui.interface
```

---

## 💡 Example Questions

- “Summarize Slide 3”
- “What is supervised learning?”
- “What is covered on page 10?”
- “Generate flashcards for the regression topic”
- “Give a summary of this entire PDF”

---

## 📦 Models Tested

- `microsoft/phi-2` ✅ (recommended for speed and accuracy)
- `mistralai/Mistral-7B-Instruct-v0.1` ✅
- `tiiuae/falcon-rw-1b` ✅ (lightweight)

> You can switch models in `llm_interface.py`

---

## 🔐 Local & Private
This project runs entirely **offline** on your own PC — no API keys or cloud calls required. Perfect for privacy and local LLM experimentation.

---

## 🧠 Skills Used

- **LangChain chains** and document loaders
- **RAG (Retrieval-Augmented Generation)** pipeline
- **LLM fine-tuned prompting**
- **Embedding & similarity search** with FAISS
- **PDF text extraction** using PyMuPDF
- **RapidFuzz** for slide number matching
- **Gradio UI design**

---

## 👨‍🎓 Author

**Deshan Senanayake**  
BSc (Hons) Artificial Intelligence & Data Science  
Robert Gordon University (via IIT, Sri Lanka)  

---

## Issues

Feel free to add any issues you find.


---

## 🏁 Future Work

- [ ] Export flashcards as `.csv` or `.txt`
- [ ] Add MCQ quiz generator
- [ ] Add feedback loop to improve flashcards
- [ ] Deploy to HuggingFace Spaces or Streamlit Cloud
- [ ] Voice input (Whisper integration)

---

## 📜 License

MIT License – free to use, modify, and share with credit.

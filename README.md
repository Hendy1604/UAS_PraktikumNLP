# UAS_PraktikumNLP
# Gym Assistant — RAG Chatbot dengan LangChain, LangGraph & LangSmith

## Deskripsi Proyek

Gym Assistant adalah chatbot berbasis Artificial Intelligence (AI) yang berfungsi sebagai asisten latihan gym virtual. Sistem ini dibangun menggunakan pendekatan **Retrieval-Augmented Generation (RAG)** sehingga jawaban yang diberikan tidak hanya berasal dari pengetahuan model bahasa, tetapi juga berdasarkan dataset latihan gym yang telah disediakan.

Project ini dikembangkan sebagai tugas **UAS Natural Language Processing (NLP)** dengan mengimplementasikan tiga framework utama:

* **LangChain** → Mengelola proses RAG, embedding, retrieval, dan prompt.
* **LangGraph** → Mengatur workflow chatbot menggunakan graph-based workflow.
* **LangSmith** → Monitoring, tracing, dan debugging proses chatbot.

---

# Tujuan Proyek

Tujuan utama dari project ini adalah membangun chatbot personal trainer yang mampu:

* Memberikan rekomendasi latihan gym.
* Menjawab pertanyaan terkait olahraga dan kebugaran.
* Memberikan saran latihan berdasarkan target otot.
* Memberikan rekomendasi berdasarkan tingkat kemampuan pengguna.
* Menampilkan proses AI yang transparan melalui LangSmith.

---

# Fitur Utama

## 1. Gym Exercise Recommendation

Pengguna dapat menanyakan latihan untuk bagian tubuh tertentu.

**Contoh:**

> Latihan dada untuk pemula

---

## 2. Retrieval-Augmented Generation (RAG)

Sistem menggunakan metode RAG sehingga jawaban dihasilkan berdasarkan dokumen latihan gym yang relevan.

Alur:

User Question → Retriever → Dokumen Relevan → LLM → Jawaban

---

## 3. Semantic Search

Menggunakan embedding untuk memahami makna pertanyaan pengguna.

Contoh:

* Chest Workout
* Latihan Dada

akan menghasilkan rekomendasi yang relevan meskipun menggunakan bahasa yang berbeda.

---

## 4. Hybrid Retrieval

Menggabungkan:

* Semantic Search (Embedding)
* Keyword Search

untuk meningkatkan akurasi pencarian latihan.

---

## 5. Body Part Recommendation

Mencari latihan berdasarkan target otot:

* Chest
* Back
* Shoulder
* Legs
* Biceps
* Triceps
* Abs

---

## 6. Equipment-Based Recommendation

Mencari latihan berdasarkan alat gym yang tersedia:

* Dumbbell
* Barbell
* Cable
* Machine

---

## 7. Beginner-Friendly Recommendation

Mampu memberikan rekomendasi berdasarkan level:

* Beginner
* Intermediate
* Expert

---

## 8. Workflow AI dengan LangGraph

Workflow chatbot dibangun menggunakan LangGraph:

START → Retrieve → Generate → END

---

## 9. Monitoring dengan LangSmith

Seluruh proses chatbot dapat dipantau menggunakan LangSmith:

* Input pengguna
* Retrieval
* Prompt
* Output model
* Runtime

---

## 10. Interactive Web Interface

Menggunakan Gradio untuk menyediakan antarmuka berbasis web yang mudah digunakan.

---

# Arsitektur Sistem

```text
User
 ↓
Gradio UI
 ↓
LangGraph
 ↓
Retrieve
 ↓
FAISS Vector Store
 ↓
Generate
 ↓
Groq LLM
 ↓
Response
 ↓
LangSmith
```

---

# Teknologi yang Digunakan

## Framework AI

* LangChain
* LangGraph
* LangSmith

## Model Bahasa

* Groq
* Llama 3.3 70B Versatile

## Vector Database

* FAISS

## Embedding Model

* sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2

## Frontend

* Gradio

## Bahasa Pemrograman

* Python

---

# Screenshot

## Tampilan Gym Assistant
<img width="1918" height="1078" alt="Screenshot 2026-06-22 173119" src="https://github.com/user-attachments/assets/00859440-ba33-4b67-b862-1ff90b1041cf" />
```



```

---

## Monitoring LangSmith
<img width="1918" height="1078" alt="Screenshot 2026-06-22 171455" src="https://github.com/user-attachments/assets/9ca29f4c-3323-461f-a8a4-06377f7f5887" />

---



# Cara Menjalankan Program

## 1. jalankan seluruh cell


## 2. Masukkan dataset MegaGymDataset.csv nya

## 3. Masukkan API Key
masukkan API KEY nya yang berada di cell TEXT code nya

## 4. Jalankan Gradio
Setelah notebook selesai dijalankan, Gradio akan menghasilkan URL seperti:

```text
Running on public URL:
https://xxxx.gradio.live
```

Buka URL tersebut untuk menggunakan Gym Assistant.

---

# 📊 Implementasi Framework

## LangChain

Digunakan untuk:

* Prompt Template
* Embedding
* FAISS Vector Store
* Retriever
* Integrasi LLM

---

## LangGraph

Digunakan untuk:

* State Management
* Workflow AI
* Node Retrieve
* Node Generate

---

## LangSmith

Digunakan untuk:

* Monitoring
* Tracing
* Debugging
* Evaluasi Workflow

---



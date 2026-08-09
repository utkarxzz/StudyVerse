# 📚 StudyVerse

### Learn smarter. Understand faster. Grow better.

**StudyVerse** is an AI-powered learning platform built to make studying more interactive, personalized, and accessible.

Instead of using AI only as a question-answering chatbot, StudyVerse aims to create a learning companion that helps students **understand concepts, ask questions, practice, and improve their learning experience.**

---

## 🌟 Why StudyVerse?

Learning resources are everywhere—but personalized learning isn't always easy to access.

Students often spend time searching for explanations, switching between different resources, and trying to figure out what they should focus on next.

**StudyVerse brings AI-powered learning assistance into one simple platform.**

Our vision is simple:

> **AI shouldn't just give students answers. It should help them learn.**

---

# ✨ Features

### 🤖 AI Study Assistant

Ask questions and interact with an AI-powered learning assistant whenever you need help understanding a topic.

### 📖 Concept Explanation

Use AI to break down difficult concepts into easier-to-understand explanations.

### 🧠 Interactive Learning

StudyVerse focuses on making learning more interactive instead of simply providing static educational content.

### ⚡ Fast AI Responses

AI requests are processed through the **Groq API** and powered by **Llama 3.1**.

### 🔐 Secure API Architecture

The Groq API key is kept on the backend rather than being exposed in the public frontend.

### 🌐 Separate Frontend & Backend

The frontend and backend are maintained as separate repositories and deployed independently.

---

# 🏗️ Architecture

```text
                         👨‍🎓 Student
                              │
                              ▼
                 ┌────────────────────────┐
                 │      StudyVerse        │
                 │       Frontend         │
                 │     GitHub Pages       │
                 └────────────┬───────────┘
                              │
                         HTTPS Request
                              │
                              ▼
                 ┌────────────────────────┐
                 │   StudyVerse Backend   │
                 │        Vercel          │
                 └────────────┬───────────┘
                              │
                         Secure API Call
                              │
                              ▼
                 ┌────────────────────────┐
                 │       Groq API         │
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │      Llama 3.1         │
                 │       AI Model         │
                 └────────────┬───────────┘
                              │
                         AI Response
                              │
                              ▼
                 ┌────────────────────────┐
                 │     StudyVerse UI      │
                 └────────────────────────┘
```

---

# 🔐 Security

StudyVerse uses a separate backend to prevent the AI API credential from being exposed directly in the public frontend.

```text
Student
   ↓
Frontend
   ↓
Vercel Backend
   ↓
Environment Variable
   ↓
Groq API
   ↓
Llama 3.1
```

The backend uses the `GROQ_API_KEY` environment variable, keeping the actual API credential outside the frontend source code.

**Never commit your real API key to GitHub.**

---

# 🛠️ Tech Stack

### Frontend

* HTML
* CSS
* JavaScript
* GitHub Pages

### Backend

* Node.js
* JavaScript
* REST API
* Vercel

### AI

* Groq API
* Llama 3.1

### Development & Deployment

* GitHub
* GitHub Pages
* Vercel
* Environment Variables

The current backend repository describes itself as a serverless proxy between the GitHub Pages frontend and Groq, with the API key configured through Vercel environment variables.

---

# 📂 Project Structure

StudyVerse is organized into two separate repositories:

```text
StudyVerse
│
├── 🎨 Frontend
│   └── GitHub Pages
│
└── ⚙️ Backend
    ├── API
    ├── Environment Variables
    └── Vercel
          │
          ▼
       Groq API
          │
          ▼
       Llama 3.1
```

---

# 🚀 Deployment

### Frontend

The StudyVerse frontend is hosted through GitHub Pages.

### Backend

The backend is deployed independently through Vercel and acts as the API layer between the frontend and Groq.

The backend repository also includes the `/api/chat` endpoint architecture used for AI requests.

---

# 🔗 Project Links

### 🌐 Live StudyVerse

https://utkarxzz.github.io/StudyVerse/

### 💻 Frontend Repository

https://github.com/utkarxzz/StudyVerse

### ⚙️ Backend Repository

https://github.com/utkarxzz/StudyVerse-Backend

### 🚀 Backend Deployment

https://study-verse-backend-five.vercel.app/

---

# 🎯 Our Vision

We believe technology should make learning **more personal, not more complicated.**

StudyVerse is built around a simple learning cycle:

```text
Understand
    ↓
Practice
    ↓
Identify Weaknesses
    ↓
Improve
    ↓
Learn Better
```

Our goal is to explore how generative AI can become more than an answer generator—and instead become a meaningful part of a student's learning journey.

---

# 💡 The Idea

Traditional digital learning gives students content.

AI can give students answers.

**StudyVerse connects the two.**

It provides students with an interactive AI-powered environment where they can ask, understand, explore, and learn.

> **StudyVerse — Where learning meets AI.**

---

# 👨‍💻 Built With

**Groq + Llama 3.1 + JavaScript + Node.js + Vercel + GitHub Pages**

---

# 📜 License

This project was created for educational and hackathon purposes.

© 2026 StudyVerse

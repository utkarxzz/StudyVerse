# 📚 StudyVerse Backend

### AI-powered backend for a smarter learning experience.

**StudyVerse** is an AI-powered learning platform designed to help students understand concepts, practice their knowledge, and make learning more interactive.

This repository contains the **StudyVerse backend**, which provides the API layer between the StudyVerse frontend and the AI model.

The frontend is hosted on **GitHub Pages**, while the backend is deployed independently on **Vercel**.

---

## 🚀 What is StudyVerse?

Studying can become difficult when students have to switch between multiple resources, search for explanations, and figure out what they should focus on next.

**StudyVerse brings AI-powered learning assistance into one place.**

Students can interact with the AI to ask questions, understand difficult concepts, and get personalized learning assistance through a simple and accessible interface.

Our goal is to make the journey from:

**"I don't understand this." → "Now I understand it."**

faster, easier, and more engaging.

---

# 🧠 AI Architecture

StudyVerse uses **Groq's API** to communicate with the **Llama 3.1** model.

Instead of placing the API key directly inside the public frontend, requests are routed through the backend.

```text
                    ┌──────────────────────┐
                    │    👨‍🎓 Student       │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   StudyVerse         │
                    │     Frontend        │
                    │    GitHub Pages      │
                    └──────────┬───────────┘
                               │
                         HTTPS Request
                               │
                               ▼
                    ┌──────────────────────┐
                    │  StudyVerse Backend  │
                    │       Vercel         │
                    └──────────┬───────────┘
                               │
                         Secure API Call
                               │
                               ▼
                    ┌──────────────────────┐
                    │      Groq API        │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │     Llama 3.1        │
                    │   AI Model           │
                    └──────────┬───────────┘
                               │
                         AI Response
                               │
                               ▼
                    ┌──────────────────────┐
                    │   StudyVerse UI      │
                    └──────────────────────┘
```

---

# 🔐 Secure API Architecture

A major reason for separating the backend from the frontend is **API key protection**.

The Groq API key is **not placed directly in the public GitHub Pages frontend**.

Instead:

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

This keeps the API credential on the server side rather than exposing it in client-side JavaScript.

---

# ✨ Features

### 🤖 AI Study Assistant

Students can interact with an AI-powered assistant to ask questions and get help with their studies.

### 📖 Concept Explanation

Difficult topics can be explained through AI-powered responses designed to make learning easier to understand.

### 🧠 Interactive Learning

StudyVerse focuses on making students actively interact with learning content instead of simply consuming information.

### ⚡ Fast AI Responses

Requests are processed through the Groq API and powered by Llama 3.1.

### 🔒 Backend API Protection

The AI API credentials are handled through the backend environment rather than being exposed in the frontend.

### 🌐 Independent Deployment

The frontend and backend are deployed independently, making the system easier to maintain and update.

---

# 🛠️ Tech Stack

## Frontend

* HTML
* CSS
* JavaScript
* GitHub Pages

## Backend

* Node.js
* JavaScript
* REST API
* Vercel

## AI

* Groq API
* Llama 3.1

## Development

* GitHub
* Vercel
* REST APIs
* Environment Variables

---

# 📁 Project Architecture

```text
StudyVerse
│
├── Frontend
│   └── GitHub Pages
│
│       ↓ HTTPS API Request
│
└── Backend
    ├── API Routes
    ├── Environment Variables
    └── Vercel Deployment
            │
            ↓
        Groq API
            │
            ↓
        Llama 3.1
```

The frontend and backend are maintained as separate repositories.

---

# ⚙️ Environment Variables

The backend requires the Groq API key to communicate with the AI model.

Example:

```env
GROQ_API_KEY=your_api_key_here
```

The actual API key should **never be committed to GitHub**.

For production deployment, the key should be configured through Vercel's environment variables.

---

# 🚀 Deployment

StudyVerse follows a simple deployment architecture:

```text
Developer
    ↓
GitHub
    ↓
Frontend → GitHub Pages
    │
    └──── API Request ────→ Backend → Vercel
                                  │
                                  ↓
                              Groq API
                                  │
                                  ↓
                              Llama 3.1
```

The backend can be updated independently without modifying the frontend hosting environment.

---

# 🌐 Project

### StudyVerse Frontend

https://utkarxzz.github.io/StudyVerse/

### Backend

The StudyVerse backend is deployed separately through Vercel.

---

# 🎯 Our Vision

StudyVerse is built around a simple idea:

> **AI shouldn't just give students answers. It should help them learn.**

We want to make learning more accessible, interactive, and personalized by bringing AI-powered assistance into a dedicated educational environment.

Our long-term vision is to help students move through the complete learning cycle:

**Understand → Practice → Identify Weaknesses → Improve → Learn Better**

---

# 💡 Why StudyVerse?

Traditional digital learning often gives students content.

AI can give students answers.

**StudyVerse aims to connect the two.**

Instead of treating AI as just a chatbot, StudyVerse uses it as a learning companion that can help students understand concepts and interact with their studies in a more meaningful way.

---

# 👨‍💻 Built With

**StudyVerse** was created as an AI-powered educational project focused on exploring how generative AI can improve the student learning experience.

### Core Technologies

**Groq + Llama 3.1 + JavaScript + Node.js + Vercel + GitHub Pages**

---

# 📜 License

This project is created for educational and hackathon purposes.

© 2026 StudyVerse

# 📚 StudyVerse

### Learn smarter. Understand faster. Grow better.

**StudyVerse** is an AI-powered learning platform designed to make studying more interactive, accessible, and engaging.

Instead of treating AI as only a question-answering chatbot, StudyVerse aims to give students an interactive learning companion for understanding concepts, asking questions, practicing, and improving their learning experience.

> **AI shouldn't just give students answers. It should help them learn.**

---

## 🌟 Why StudyVerse?

Educational resources are everywhere, but finding the right explanation and getting help at the right moment can still be difficult.

StudyVerse brings AI-powered learning assistance into one simple platform so students can spend less time searching and more time learning.

The core learning idea is:

**Understand → Practice → Identify Weaknesses → Improve → Learn Better**

---

## ✨ Features

- 🤖 **AI Study Assistant** — Ask questions and get AI-powered learning assistance.
- 📖 **Concept Explanation** — Use AI to make difficult concepts easier to understand.
- 🧠 **Interactive Learning** — Turn questions into an active learning experience.
- ⚡ **Fast AI Responses** — AI requests are handled through Groq and Llama 3.1.
- 🔐 **Separated Backend** — AI credentials are handled server-side instead of being exposed in the public frontend.
- 🌐 **Independent Deployment** — Frontend and backend are maintained and deployed separately.

> Add or remove feature bullets above so that this section matches the exact features currently implemented in the live project.

---

## 🏗️ Architecture

StudyVerse uses a separated frontend/backend architecture:

```text
Student
   |
   v
StudyVerse Frontend
GitHub Pages
   |
   | HTTPS API Request
   v
StudyVerse Backend
Vercel
   |
   | Server-side API Request
   v
Groq API
   |
   v
Llama 3.1
   |
   v
AI Response
   |
   v
StudyVerse Frontend
```

See the detailed architecture documentation:

**`docs/architecture.md`**

---

## 🔐 Security

The Groq API key is kept on the backend through an environment variable rather than being placed directly in the public frontend.

Example:

```env
GROQ_API_KEY=your_api_key_here
```

**Never commit a real API key to GitHub.**

For production, configure the secret through the Vercel project environment variables.

---

## 🛠️ Tech Stack

### Frontend
- HTML
- CSS
- JavaScript
- GitHub Pages

### Backend
- Node.js / JavaScript
- REST API
- Vercel

### AI
- Groq API
- Llama 3.1

### Development & Deployment
- GitHub
- GitHub Pages
- Vercel
- Environment Variables

---

## 📂 Repository Structure

The project is maintained across two repositories:

```text
StudyVerse
├── Frontend
│   └── GitHub Pages
│
└── Backend
    ├── API
    ├── Environment Variables
    └── Vercel
        └── Groq → Llama 3.1
```

---

## 🚀 Getting Started

### Frontend

The frontend is a static web application.

1. Clone the repository.
2. Open the project folder.
3. Open `index.html` in a browser or serve the folder with a local static server.
4. Make sure the frontend API configuration points to the deployed backend endpoint.

### Backend

The backend is maintained in a separate repository.

1. Clone the backend repository.
2. Install the project's dependencies according to its `package.json`.
3. Configure the required environment variable:
   ```env
   GROQ_API_KEY=your_api_key_here
   ```
4. Run/deploy the backend according to its Vercel configuration.

> Keep the setup instructions synchronized with the actual backend repository as the implementation evolves.

---

## 🔗 Project Links

### 🌐 Live Demo
https://utkarxzz.github.io/StudyVerse/

### 💻 Frontend Repository
https://github.com/utkarxzz/StudyVerse

### ⚙️ Backend Repository
https://github.com/utkarxzz/StudyVerse-Backend

### 🚀 Backend Deployment
https://study-verse-backend-five.vercel.app/

---



## 🧩 Project Goals

StudyVerse is built around three goals:

1. Make AI-assisted learning easier to access.
2. Make learning more interactive than simple content consumption.
3. Explore how generative AI can support a student's learning journey.

---

## 🎯 Vision

We believe technology should make learning **more personal, not more complicated**.

StudyVerse explores a future where AI can become a useful learning companion—not simply an answer generator.

> **StudyVerse — Where learning meets AI.**

---

## 🏆 Hackathon

**StudyVerse** was developed as an AI-powered educational project for hackathon participation.

The project focuses on:

- Innovation in AI-powered education
- Practical student impact
- Clear user experience
- A functional and reproducible implementation

---

## 👨‍💻 Built With

**Groq · Llama 3.1 · JavaScript · Node.js · Vercel · GitHub Pages**

---

## 📜 License

This project is licensed under the **MIT License**.

Copyright © 2026 Utkarsh Tiwari.

See [`LICENSE`](LICENSE) for details.

---

## ⚠️ Disclaimer

StudyVerse is an educational project. AI-generated responses can contain mistakes, so important academic information should be verified with trusted educational sources.

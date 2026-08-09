# StudyVerse Architecture

## Overview

StudyVerse uses a separated frontend/backend architecture.

- **Frontend:** HTML, CSS and JavaScript hosted on GitHub Pages.
- **Backend:** Separate API repository deployed on Vercel.
- **AI:** Groq API with the Llama 3.1 model.
- **Secrets:** The Groq API key is kept on the backend through environment variables and is not placed in the public frontend.

## System Flow

```text
                    +----------------------+
                    |      Student         |
                    +----------+-----------+
                               |
                               | HTTPS
                               v
                    +----------------------+
                    |  StudyVerse Frontend |
                    |    GitHub Pages      |
                    +----------+-----------+
                               |
                               | API Request
                               v
                    +----------------------+
                    |  StudyVerse Backend  |
                    |       Vercel         |
                    +----------+-----------+
                               |
                               | Server-side
                               | API request
                               v
                    +----------------------+
                    |       Groq API       |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |      Llama 3.1       |
                    +----------+-----------+
                               |
                               | AI response
                               v
                    +----------------------+
                    |  StudyVerse Backend  |
                    +----------+-----------+
                               |
                               | JSON response
                               v
                    +----------------------+
                    |  StudyVerse Frontend |
                    +----------------------+
```

## Why Separate the Backend?

The frontend is public because it is hosted as a static site. Keeping the AI API credential in the backend prevents the secret from being directly embedded in the public frontend source.

The frontend sends a request to the backend. The backend then communicates with Groq using the server-side environment variable.

```text
Frontend
   |
   v
Vercel Backend
   |
   +--> GROQ_API_KEY (server-side environment variable)
   |
   v
Groq API
   |
   v
Llama 3.1
```

## Repositories

### Frontend
https://github.com/utkarxzz/StudyVerse

### Backend
https://github.com/utkarxzz/StudyVerse-Backend

## Deployments

### Live Frontend
https://utkarxzz.github.io/StudyVerse/

### Backend Deployment
https://study-verse-backend-five.vercel.app/

## Security Notes

- Never commit a real API key to GitHub.
- Store secrets in Vercel environment variables for production.
- Do not place `.env` files in the repository.
- The backend should validate incoming requests before forwarding them to the AI provider.

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Frontend Hosting | GitHub Pages |
| Backend | Node.js / JavaScript API |
| Backend Hosting | Vercel |
| AI Provider | Groq |
| AI Model | Llama 3.1 |
| Source Control | GitHub |

## Request Lifecycle

1. A student interacts with StudyVerse.
2. The frontend creates an API request.
3. The request is sent over HTTPS to the StudyVerse backend.
4. The backend accesses the Groq API using its server-side credential.
5. Groq processes the request with Llama 3.1.
6. The backend returns the AI response to the frontend.
7. StudyVerse displays the response to the student.

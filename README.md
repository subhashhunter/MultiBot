# 🤖 MultiBot

A full-stack AI-powered content generation platform that lets users generate articles, blog titles, images, remove image backgrounds/objects, and review resumes — all from a single interface. Built with **React.js** on the frontend and **Node.js + Express.js** on the backend, deployed live on Vercel.

🔗 **Live Demo:** [multi-bot-server.vercel.app](https://multi-bot-server.vercel.app)

---

## 📁 Project Structure

```
MultiBot/
├── frontend/              # React.js user interface
└── backend/               # Node.js + Express.js API server
    ├── controllers/
    │   ├── aiController.js
    │   └── userController.js
    ├── middlewares/
    │   └── auth.js
    ├── configs/
    │   └── multer.js
    └── routes/
        ├── aiRouter.js
        └── userRouter.js
```

---

## ✨ Features

- 📝 AI-powered article generation
- 💡 Blog title generator
- 🎨 AI image generation
- 🖼️ Remove image backgrounds automatically
- ✂️ Remove objects from images
- 📄 Resume review with AI feedback
- ❤️ Like & save AI-generated creations
- 🔐 JWT-based authentication & protected routes
- 📁 File uploads handled via Multer
- 📱 Responsive UI — works on desktop and mobile

---

## 🛠️ Tech Stack

| Layer      | Technology                              |
|------------|-----------------------------------------|
| Frontend   | React.js, React Router, Axios           |
| Backend    | Node.js, Express.js                     |
| Auth       | JWT (JSON Web Tokens)                   |
| File Upload| Multer                                  |
| AI APIs    |  OpenAI 
| Deployment | Vercel (Frontend + Backend)             |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/)
- API keys for the AI providers you're using

---

### 1. Clone the Repository

```bash
git clone https://github.com/subhashhunter/MultiBot.git
cd MultiBot
```

---

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory:

```env
PORT=5000
GEMINI_API_KEY=your_gemini_api_key
OPENAI_API_KEY=your_openai_api_key
# Add any other API keys here
```

Start the backend server:

```bash
npm run dev
```

The API will be running at `http://localhost:3000`.

---

### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

Create a `.env` file in the `frontend/` directory:

```env
VITE_API_URL=http://localhost:3000
```

Start the frontend:

```bash
npm run dev
```

The app will be running at `http://localhost:5173`.

---

## 📦 API Endpoints

All protected routes require a valid JWT token in the request header.

### 🤖 AI Routes — `/api/ai`

| Method | Endpoint                        | Auth | File Upload       | Description                        |
|--------|---------------------------------|------|-------------------|------------------------------------|
| POST   | `/api/ai/generate-article`      | ✅   | ❌                | Generate an AI-written article     |
| POST   | `/api/ai/generate-blog-title`   | ✅   | ❌                | Generate blog title suggestions    |
| POST   | `/api/ai/generate-image`        | ✅   | ❌                | Generate an AI image               |
| POST   | `/api/ai/remove-image-background` | ✅ | ✅ `image` field  | Remove background from an image    |
| POST   | `/api/ai/remove-image-object`   | ✅   | ✅ `image` field  | Remove an object from an image     |
| POST   | `/api/ai/resume-review`         | ✅   | ✅ `resume` field | Review a resume and give AI feedback |

### 👤 User Routes — `/api/user`

| Method | Endpoint                            | Auth | Description                          |
|--------|-------------------------------------|------|--------------------------------------|
| GET    | `/api/user/get-user-creations`      | ✅   | Get all creations by the logged-in user |
| GET    | `/api/user/get-published-creations` | ✅   | Get all publicly published creations |
| POST   | `/api/user/toggle-like-creations`   | ✅   | Like or unlike a creation            |

---

## 🌐 Deployment

Both frontend and backend are deployed on **Vercel**:


## 👤 Author

**Subhash**
- GitHub: [@subhashhunter](https://github.com/subhashhunter)

---

> ⭐ If you found this project helpful, please give it a star!

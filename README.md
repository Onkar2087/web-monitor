# 🔍 Web Monitor

AI-powered website monitoring system that detects webpage changes, generates diffs, extracts evidence, and summarizes updates using LLMs.

---

## 🚀 Features

- Monitor website content changes
- AI-generated summaries
- Evidence extraction
- Diff visualization
- Snapshot history tracking
- System health monitoring
- Responsive frontend UI
- SQLite persistence

---

## 🛠 Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- Axios
- React Router

### Backend
- Node.js
- Express.js
- SQLite
- Cheerio
- Axios
- Diff
- Google Gemini API

---

## 📂 Project Structure

```bash
web-monitor/
│
├── backend/
├── frontend/
├── ABOUT_ME.md
├── AI_NOTES.md
├── PROMPTS_USED.md
└── README.md
```

---

# ⚙️ Full Project Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/Onkar2087/web-monitor.git
```

Move into project:

```bash
cd web-monitor
```

---

# ⚙️ Backend Setup

## 2️⃣ Move to Backend Folder

```bash
cd backend
```

---

## 3️⃣ Install Backend Dependencies

```bash
npm install
```

---

## 4️⃣ Create Backend `.env`

Create a `.env` file inside `backend/`

```env
PORT=5000
FRONTEND_URL=http://localhost:5173
GEMINI_API_KEY=your_gemini_api_key
NODE_ENV = "production"
```

---

## 5️⃣ Start Backend Server

Development mode:

```bash
npm run dev
```

Production mode:

```bash
npm start
```

Backend runs on:

```bash
http://localhost:5000
```

---

# ⚙️ Frontend Setup

Open a NEW terminal.

---

## 6️⃣ Move to Frontend Folder

```bash
cd frontend
```

---

## 7️⃣ Install Frontend Dependencies

```bash
npm install
```

---

## 8️⃣ Create Frontend `.env`

Create a `.env` file inside `frontend/`

```env
VITE_API_URL=http://localhost:5000
```

---

## 9️⃣ Start Frontend

```bash
npm run dev
```

Frontend runs on:

```bash
http://localhost:5173
```

---

# 🌐 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/add` | Add new URL |
| POST | `/api/check/:id` | Check for changes |
| GET | `/api/status/:id` | Get latest status |
| GET | `/api/links` | Get all links |
| DELETE | `/api/delete/:id` | Delete link |
| GET | `/api/health` | System health |

---

# 🧠 How It Works

1. Fetch webpage HTML
2. Extract readable text using Cheerio
3. Compare against previous snapshot
4. Generate diff
5. Extract evidence lines
6. Generate AI summary
7. Store snapshots in SQLite

---

# 📊 UI Features

### 🔹 Diff View
Displays added and removed content changes.

### 🔹 Summary
LLM-generated explanation of detected changes.

### 🔹 Evidence
Important lines responsible for the detected changes.

### 🔹 History
Stores and displays previous monitoring timestamps.

### 🔹 System Health
Checks:
- Backend availability
- Database connection
- LLM availability

---

# 🚀 Deployment

### Frontend
- Vercel

### Backend
- Render

---

# ⚠️ Notes

- Some websites may block scraping requests from cloud servers
- SQLite is used for lightweight deployment
- Designed for small-scale monitoring workloads
- Large pages are truncated for performance

---

# 📌 Future Improvements

- PostgreSQL migration
- Authentication
- Email/Slack notifications
- Side-by-side diff viewer
- Scheduled monitoring jobs
- User dashboards

---

# 👨‍💻 Author

### Onkar Dhingra

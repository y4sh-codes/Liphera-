# Liphera-
Liphera is an offline-first language interaction platform with a web UI, backend, and Raspberry Pi model server, enabling fast, private, and reliable multilingual communication anywhere.
  
This repository contains the **frontend, backend, and Raspberry Pi model server** for Liphera.  

The system allows users to:
- Browse and download language packs  
- Interact with text/audio models  
- Run inference **locally on Raspberry Pi** without cloud dependency  

---

## 🚀 Architecture


- **Frontend** → User interface for interactions & language pack options  
- **Backend** → Bridge between frontend and model; manages APIs & user requests  
- **Raspberry Pi** → Hosts the AI model, exposes inference API  

---

## 📂 Repository Structure

liphera/
│── frontend/                  # Frontend code (React/Next.js/Vue)
│   ├── public/                # Static assets
│   ├── src/                   
│   │   ├── components/        # Reusable UI components
│   │   ├── pages/             # Routes/pages (if Next.js)
│   │   ├── services/          # API calls to backend
│   │   └── styles/            # CSS/Tailwind
│   └── package.json           
│
│── backend/                   # Backend code (FastAPI/Node/Django)
│   ├── app/
│   │   ├── api/               # API endpoints
│   │   ├── models/            # Database models (if needed)
│   │   ├── services/          # Logic for interacting with Pi
│   │   └── main.py            # Entry point
│   ├── requirements.txt       # Python deps (if FastAPI)
│   └── Dockerfile             # For deployment (optional)
│
│── raspberry_pi/              # Model server code for Pi
│   ├── model/                 # Your trained model files
│   ├── app.py                 # FastAPI/Flask server exposing inference API
│   └── requirements.txt
│
│── docs/                      # Documentation
│   ├── architecture.md
│   └── setup.md
│
│── scripts/                   # Helper scripts (build, deploy, etc.)
│
│── .gitignore
│── README.md


---

## 🛠️ Setup Instructions

### 1. Frontend (React/Next.js)
```bash
cd frontend
npm install
npm run dev
```
### 2. Backend (FastAPI Example)
```bash
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload
```
### 3. Raspberry Pi Model Server
```bash
cd raspberry_pi
pip install -r requirements.txt
python app.py
```




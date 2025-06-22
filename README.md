# 🚀 Python Webhook API with FastAPI (Railway Ready)

A simple webhook receiver built using FastAPI, designed for free deployment on [Railway](https://railway.app).

---

## 📦 Project Structure

```
python-webhook/
├── main.py
├── requirements.txt
├── railway.json
└── README.md
```

---

## 🧑‍💻 Run Locally

1. Clone the repo or unzip the project
2. Create a virtual environment (optional)
```bash
python -m venv venv
venv\Scripts\activate
```
3. Install dependencies
```bash
pip install -r requirements.txt
```
4. Run the server
```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
5. Send test webhook
```bash
curl -X POST http://localhost:8000/webhook -H "Content-Type: application/json" -d '{"test":"ok"}'
```

---

## 🌍 Deploy to Railway

1. Push this project to a GitHub repository
2. Go to [https://railway.app](https://railway.app)
3. Create a new project → "Deploy from GitHub"
4. Choose your repository
5. Railway auto-detects `FastAPI` from `requirements.txt`
6. Done! Your public webhook endpoint:
```
https://your-app.up.railway.app/webhook
```

---

## 🔁 Sample Payload

```json
{
  "event": "new_user",
  "status": "active"
}
```

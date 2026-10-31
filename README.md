# AI Interview Assistant 🎯

An AI-powered interview practice application that helps users prepare for technical and general interviews through interactive conversations. It uses Generative AI, speech-to-text, and text-to-speech technologies to create a realistic interview experience.

## 🚀 Features

* Select interview subjects such as Python, HTML, CSS, Generative AI, English, and Self Introduction.
* Generate interview questions dynamically using Google Gemini.
* Convert AI-generated questions into speech using Murf AI.
* Record answers using the browser microphone.
* Convert spoken answers into text using AssemblyAI.
* Generate follow-up questions based on previous answers.
* Generate interview feedback with scores, strengths, and areas for improvement.
* Conduct interviews with five questions.

## 🛠️ Tech Stack

### Frontend

* HTML
* CSS
* JavaScript

### Backend

* Python
* Flask
* Flask-CORS
* LangChain
* LangGraph
* Google Gemini
* Murf AI
* AssemblyAI

## 📂 Project Structure

```text
AI_Interview_Project/
│
├── frontend/
│   ├── index.html
│   └── index.js
│
├── backend/
│   ├── app.py
│   └── requirements.txt
│
├── .gitignore
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
cd AI_Interview_Project
```

### 2. Navigate to Backend

```bash
cd backend
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

**Windows:**

```bash
venv\Scripts\activate
```

**Mac/Linux:**

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables

Create a `.env` file inside the backend folder.

Add your API keys:

```env
GEMINI_API_KEY=your_gemini_api_key
MURF_API_KEY=your_murf_api_key
ASSEMBLYAI_API_KEY=your_assemblyai_api_key
```

**Important:** Never upload your `.env` file or expose your API keys on GitHub.

### 6. Run the Backend

```bash
python app.py
```

The Flask backend runs at:

```text
http://127.0.0.1:5000
```

### 7. Run the Frontend

Open `frontend/index.html` in your browser or use the VS Code Live Server extension.

## 🔗 API Endpoints

| Method | Endpoint           | Description                                                           |
| ------ | ------------------ | --------------------------------------------------------------------- |
| POST   | `/start-interview` | Starts a new interview.                                               |
| POST   | `/submit-answer`   | Processes the user's recorded answer and generates the next question. |
| POST   | `/get-feedback`    | Generates final interview feedback.                                   |

## ☁️ Deployment

The application can be deployed using Render with a single GitHub repository.

**Backend:**

* Platform: Render Web Service
* Root Directory: `backend`
* Build Command: `pip install -r requirements.txt`
* Start Command: `gunicorn app:app`

**Frontend:**

* Platform: Render Static Site
* Root Directory: `frontend`
* Publish Directory: `.`

After deploying the backend, update the frontend API URLs to use the deployed backend URL.

Configure your API keys through Render Environment Variables.

## 🔮 Future Improvements

* User authentication.
* Interview history and progress tracking.
* Database integration.
* Multiple interview difficulty levels.
* Improved interview analytics.

## 👨‍💻 Author

Developed as an AI-powered interview practice project using Python, LangChain, LangGraph, and Generative AI.

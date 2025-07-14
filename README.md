# 📄 CV Assessor

**AI-powered Resume Reviewer built using Google Gemini + Flask**

CV Assessor is a web app that allows users to upload a PDF resume and receive a detailed review powered by Google Gemini. The review includes strengths, weaknesses, improvement suggestions, and an overall rating — all neatly formatted and career-level aware.

---

## 🚀 Features

- 🧠 Uses Google's Gemini (via `google-generativeai`) to generate intelligent feedback  
- 📂 Accepts PDF resumes and detects if the uploaded file is not a resume  
- 💬 Gives specific suggestions for structure, content, and visual improvements  
- ⭐ Industry fit and rating out of 5  
- 🛠️ Flask backend and HTML front-end  
- 📃 Clean HTML-formatted output  

---

## 🧑‍💻 Tech Stack

- Python  
- Flask  
- LangChain  
- Google Generative AI (Gemini)  
- PyPDF2  
- dotenv  

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/Charchit-Sharma/CV_Assessor.git
cd CV_Assessor
```

### 2. Create and activate a virtual environment (optional but recommended)

```bash
python -m venv venv
source venv/bin/activate     # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up your environment variables

Create a `.env` file in the project root directory and add:

```env
GOOGLE_API_KEY=your_api_key_here
```

> 🔑 You can get your Gemini API key from [Google AI Studio]
---

## ▶️ Running the App

```bash
python app.py
```

---

## 📂 Project Structure

```
├── app.py               # Flask server  
├── functions.py         # Core Gemini logic and formatting  
├── requirements.txt     # Python dependencies  
├── templates/
│   └── index.html       # Frontend HTML Template
└── .env                 # (You create this) API key config  
```

---

## ✨ Output Format

If a valid resume is uploaded, the model returns:

- ✅ A quick 2-line summary  
- 🌟 Top 3 strengths  
- ❌ Top 3 improvement areas  
- 📊 Industry alignment and a rating (X.X/5)  
- 💡 3 quick tips to improve  
- 🙌 Encouraging final conclusion  

If the file isn't a resume, you'll see a polite rejection message.

---

## 📌 Notes

- Only PDF files are supported.  
- Make sure the resume is not image-scanned (text must be extractable).  
- Uses Gemini model: `gemini-2.0-flash-exp`  

---

## 📜 License

MIT License

---

## 🙌 Credits

Built with ❤️ by [Your Name] using:

- Google Gemini API  
- LangChain  
- Flask
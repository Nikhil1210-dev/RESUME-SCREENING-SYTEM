# Smart Resume Screening System

A web-based resume screening application built using Python and FastAPI. It analyzes resumes against job descriptions, calculates candidate match scores, identifies matched and missing skills, and ranks candidates based on their relevance.

## 🚀 Features

- **Job Description Analysis:** Analyze job requirements and skills.
- **Multiple Resume Screening:** Compare multiple candidates against one job description.
- **TF-IDF:** Calculate the importance of words in documents.
- **Cosine Similarity:** Measure similarity between job descriptions and resumes.
- **Skill Matching:** Identify matched and missing technical skills.
- **Match Score:** Calculate candidate compatibility scores.
- **Candidate Ranking:** Automatically rank candidates from highest to lowest score.
- **Interactive Dashboard:** View screening results through a web interface.
- **REST API:** Process screening requests using FastAPI.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend development |
| FastAPI | REST API framework |
| Pydantic | Data validation |
| HTML | Webpage structure |
| CSS | User interface styling |
| JavaScript | Frontend functionality |
| TF-IDF | Text analysis |
| Cosine Similarity | Resume comparison |
| Regular Expressions | Skill and experience extraction |

## ⚙️ Screening Algorithm

The system combines two matching techniques:

1. **TF-IDF + Cosine Similarity (40%)** – Measures textual similarity between the job description and resume.
2. **Skill Matching (60%)** – Identifies relevant skills and calculates skill overlap.

**Final Score Formula:**

`Final Score = (Similarity × 40) + (Skill Overlap × 60)`

Candidates are sorted according to their final match scores.

## 📂 Project Structure

```text
smart-resume-screening-main/
│
├── app/
│   ├── main.py
│   ├── schemas.py
│   ├── parser.py
│   └── matcher.py
│
├── static/
│   ├── index.html
│   ├── styles.css
│   └── app.js
│
├── samples/
│   └── request.json
│
├── requirements.txt
└── README.md
```

## 💻 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Open the Project Folder

```bash
cd smart-resume-screening-main
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate Virtual Environment (Windows)

```powershell
.venv\Scripts\Activate.ps1
```

### 5. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 6. Run the Application

```bash
python -m uvicorn app.main:app --host 127.0.0.1 --port 8000 --reload
```

## 🌐 Access the Application

- **Web Application:** http://127.0.0.1:8000/
- **Swagger API Documentation:** http://127.0.0.1:8000/docs
- **ReDoc Documentation:** http://127.0.0.1:8000/redoc

## 🔗 API Endpoint

| Method | Endpoint | Description |
|---|---|---|
| POST | `/screen-resumes` | Screen and rank candidates |

## 🎯 Project Objective

The main objective is to reduce manual recruitment effort by automating the initial resume-screening process. The system helps recruiters identify relevant candidates through skill matching, text similarity, transparent scoring, and candidate ranking.

## 🔮 Future Enhancements

- Advanced NLP-based resume analysis
- Improved skill extraction and synonym detection
- PDF and DOCX resume processing
- Database integration
- Candidate screening history
- Enhanced analytics and reporting

## ⚠️ Disclaimer

This system is designed as a recruitment decision-support tool. Its match scores are indicative and should not replace human evaluation or final hiring decisions.

## 👨‍💻 Developed By

**Smart Resume Screening System Project**

Built using Python, FastAPI, and web technologies.

#  AI Internship & Career Advisor

### Powered by Hindsight Memory + LLMs

---

##  Overview

AI Internship & Career Advisor is an intelligent system that analyzes a user's resume, tracks their progress over time, and provides personalized career advice using **memory-based learning**.

Unlike traditional AI tools, this system **remembers past interactions** and improves its guidance across sessions using **Hindsight memory**.

---

##  Key Features

* **Persistent Memory (Hindsight)**
  Stores user skills, projects, and goals across sessions

* **Progress Tracking**
  Compares past vs current data to detect improvement

* **Skill Extraction**
  Extracts skills from resume text using keyword + normalization

* **Skill Gap Analysis**
  Identifies missing skills required for internships

* **Personalized AI Advice**
  Uses LLM (Groq) to generate adaptive recommendations

* **Project Detection**
  Detects if user has built real projects

* **Multi-session Learning**
  AI becomes stricter or smarter based on history

---

## How It Works

### Data Flow

User Input (Resume)
→ FastAPI Backend
→ Skill & Project Extraction
→ Hindsight Memory (store/retrieve)
→ Compare Past vs Present
→ LLM (Groq)
→ Personalized Advice

---

##  Tech Stack

* **Backend:** FastAPI
* **Frontend:** Streamlit
* **LLM:** Groq API (LLaMA3)
* **Memory:** Hindsight
* **Language:** Python

---

##  Project Structure

```
ai-career-advisor/
│
├── backend/
│   ├── main.py          # FastAPI app
│   ├── utils.py         # Skill + project logic
│   ├── memory.py        # Hindsight integration
│   ├── llm.py           # Groq API calls
│
├── frontend/
│   ├── app.py           # Streamlit UI
│
├── .env
├── requirements.txt
└── README.md
```

---

## Setup Instructions

### Clone Repository

```
git clone <your-repo-link>
cd ai-career-advisor
```

---

### Create Virtual Environment

```
python -m venv venv
venv\Scripts\activate   # Windows
```

---

### Install Dependencies

```
pip install -r requirements.txt
```

---

### Setup Environment Variables

Create a `.env` file:

```
GROQ_API_KEY=your_groq_key
HINDSIGHT_API_KEY=your_hindsight_key
```

---

### Run Backend

```
cd backend
uvicorn main:app --reload
```

---

### Run Frontend

```
cd frontend
streamlit run app.py
```

---

## Example Usage

### First Session

Input:

```
I know Python and SQL
```

Output:

* Missing Skills: ML
* Advice: Build projects

---

### Second Session

Input:

```
I built a machine learning project
```

Output:

* Improvement detected
* Feedback: "Great! You added projects 🎉"
* Advice becomes more advanced

---

##  Memory Example

### Stored Data

```json
{
  "skills": ["python", "ml"],
  "projects": ["machine learning project"],
  "goal": "internship"
}
```

---

## Demo Flow

1. Enter user_id (e.g., `101`)
2. Paste basic resume → Analyze
3. Run again with improved resume
4. Show:

   * Memory comparison
   * Behavior change
   * Personalized feedback

---

## Hackathon Highlights

✔ Uses Hindsight memory effectively
✔ Demonstrates real **learning over time**
✔ Shows adaptive AI behavior
✔ Works without GPU
✔ End-to-end system

---

## Future Improvements

* Career Score (0–100)
* Progress graphs
* LLM-based skill extraction
* Internship recommendation engine

---

## Acknowledgements

* Hindsight for memory system
* Groq for fast LLM inference

---




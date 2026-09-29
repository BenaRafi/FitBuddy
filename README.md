

# 🏋️ FitBuddy – AI Fitness Plan Generator using Gemini Models

FitBuddy is a web-based application that uses AI to generate personalized 7-day workout plans and nutrition/recovery tips based on a user's goal (weight loss, muscle gain, general wellness). Users can also submit feedback to refine their plan, and an admin view shows all users with their original and updated plans.

**Tech Stack:** FastAPI · Google Gemini (1.5 Pro & Flash) · SQLite + SQLAlchemy · HTML/CSS + Jinja2 · Python · Uvicorn

**Project Type:** Group Project
**Class:** II BSc Computer Science (2025–26)
**College:** Tiruppur Kumaran College for Women
**Demo Video:https://drive.google.com/file/d/1zfRmzG_mks1Ze7XzI4_GR0lQJa-rwztq/view

## 👥 Team Members
| S.No | Name | Role / Contribution |
|------|------|---------------------|
| 1 | Benazir R (**Team Lead**) | Team lead · Development environment setup, core functionalities, UI design |
| 2 | Vinothini | AI model research & selection, application architecture, Jinja2 dynamic templates |
| 3 | Jamuna M | FastAPI backend, routes (main application logic), local deployment preparation |
| 4 | Nithya Pushpam | Pre-requisites, project workflow, testing & verifying local deployment |
| 5 | Pandiselvi | Conclusion and project documentation |

**Team Lead:** Benazir R
**Trainer / Guide: Premalatha 

## 📂 Project Phases
1. [Brainstorming & Ideation Phase](1-Brainstorming-Ideation-Phase.md)
2. [Requirement Analysis Phase](2-Requirement-Analysis-Phase.md)
3. [Project Design Phase](3-Project-Design-Phase.md)
4. [Project Planning Phase](4-Project-Planning-Phase.md)
5. [Project Development Phase](5-Project-Development-Phase.md)
6. [Project Testing Phase](6-Project-Testing-Phase.md)
7. [Project Documentation Phase](7-Project-Documentation-Phase.md)
8. [Project Demonstration Phase](8-Project-Demonstration-Phase.md)

## ▶️ Quick Start
```bash
git clone https://github.com/<your-username>/FitBuddy.git
cd FitBuddy
python -m venv venv
venv\Scripts\activate          # Windows  (Linux/Mac: source venv/bin/activate)
pip install -r requirements.txt
# create .env file:  GOOGLE_API_KEY=your_gemini_api_key_here
uvicorn app.main:app --reload
```
Open http://127.0.0.1:8000 (API docs at `/docs`).

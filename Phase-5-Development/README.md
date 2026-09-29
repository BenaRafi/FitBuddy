# 5. Project Development Phase

## Folder Structure
```
FitBuddy/
├── app/
│   ├── main.py
│   ├── routes.py
│   ├── database.py
│   ├── gemini_generator.py
│   ├── gemini_flash_generator.py
│   ├── updated_plan.py
│   └── schemas.py
├── templates/
│   ├── index.html
│   ├── result.html
│   └── all_users.html
├── static/images/
├── requirements.txt
├── .env
└── README.md
```

## Environment Setup
```bash
python -m venv venv
venv\Scripts\activate            # Windows
pip install fastapi uvicorn jinja2 sqlalchemy python-multipart google-generativeai python-dotenv
```
Create `.env`:
```
GOOGLE_API_KEY=your_gemini_api_key_here
```

## Core Features Developed
| Feature | Function / File | Description |
|---------|-----------------|-------------|
| Workout generation | `generate_workout_gemini()` in `gemini_generator.py` | Sends goal and intensity to Gemini 1.5 Pro; returns 7-day plan with warm-up, main workout and cooldown |
| Nutrition tip | `generate_nutrition_tip_with_flash()` in `gemini_flash_generator.py` | Gemini Flash returns a short goal-based tip |
| Feedback update | `update_workout_plan()` in `updated_plan.py` | Sends original plan + feedback to Gemini 1.5 Pro for a revised plan |
| Data storage | `database.py` | Saves users, original plan and updated plan via SQLAlchemy |
| Admin view | `/view-all-users` | Shows all users and plans using Jinja2 loop |

## Backend (FastAPI)
- Routes defined in `routes.py`
- Form inputs captured with `Form(...)`
- Pydantic schemas `UserInput` and `FeedbackRequest` validate data
- `/generate-workout` → calls workout + tip functions → saves user and plan → renders `result.html`
- `/submit-feedback` → fetches original plan → updates via Gemini → saves updated plan → renders `result.html`

## Frontend
- Jinja2 rendering: `Jinja2Templates(directory=TEMPLATE_DIR)` with `TemplateResponse`
- Variables used: `{{ username }}`, `{{ goal }}`, `{{ workout_plan }}`, `{{ nutrition_tip }}`
- Flexbox layout, media queries, dark theme, Roboto font
- AI text displayed inside `<pre>` blocks to keep formatting

## Run the Application
```bash
uvicorn app.main:app --reload
```
- App: http://127.0.0.1:8000
- API docs: http://127.0.0.1:8000/docs

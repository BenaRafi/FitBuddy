
# 3. Project Design Phase

## System Architecture
FitBuddy follows a modular FastAPI-based architecture.

```
   User (Browser)
        │
        ▼
 Frontend: HTML + Jinja2 templates
        │  (Form POST)
        ▼
 Backend: FastAPI (routes.py)
   │              │
   ▼              ▼
 AI Layer       Database
 Gemini Pro     SQLite + SQLAlchemy
 Gemini Flash
```

| Layer | Technology | Responsibility |
|-------|------------|----------------|
| Frontend | HTML, CSS, Jinja2 | Input form, result display, admin view |
| Backend | FastAPI | Routing, validation, business logic |
| AI | Gemini 1.5 Pro / Flash | Workout plans, updates, nutrition tips |
| Database | SQLite + SQLAlchemy | Store users and plans |

## Module Design
| Module | File | Function |
|--------|------|----------|
| Workout generation | `gemini_generator.py` | `generate_workout_gemini()` |
| Nutrition tip | `gemini_flash_generator.py` | `generate_nutrition_tip_with_flash()` |
| Plan update | `updated_plan.py` | `update_workout_plan()` |
| Database | `database.py` | `save_user()`, `save_plan()`, `update_plan()`, `get_original_plan()`, `get_user()` |
| Routing | `routes.py` | All endpoints |
| Entry point | `main.py` | Starts the FastAPI app |

## Route Design
| Route | Method | Purpose |
|-------|--------|---------|
| `/` | GET | Home page (input form) |
| `/generate-workout` | POST | Generate workout plan + nutrition tip and save data |
| `/submit-feedback` | POST | Update plan using feedback |
| `/view-all-users` | GET | Admin dashboard |

## Data Design
**User / Plan data:** user ID, name, age, weight, goal, intensity, original plan, updated plan (stored separately to keep both versions).

## UI Design
| Page | Template | Content |
|------|----------|---------|
| Home | `index.html` | Form: name, user ID, age, weight, goal, intensity + "Generate Plan" button |
| Result | `result.html` | User info, 7-day plan, nutrition tip, feedback form |
| Admin | `all_users.html` | Table of all users with original and updated plans |

Design choices: gym-themed background image, Roboto font, Flexbox layout, media queries for mobile, hover effects on buttons, dark theme.


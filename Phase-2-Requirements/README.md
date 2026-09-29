# 2. Requirement Analysis Phase

## Functional Requirements
| ID | Requirement |
|----|-------------|
| FR1 | User can enter name, user ID, age, weight, fitness goal and workout intensity (low / medium / high) |
| FR2 | System generates a personalized 7-day workout plan using Gemini 1.5 Pro |
| FR3 | System generates a nutrition/recovery tip using Gemini Flash |
| FR4 | User can submit feedback (e.g., "more cardio", "add rest days") to update the plan |
| FR5 | System stores user details, original plan and updated plan in the database |
| FR6 | Admin can view all users with original and updated plans |
| FR7 | Admin can delete users |

## Non-Functional Requirements
- **Usability:** clean, simple interface with gym-themed design
- **Performance:** fast response using Gemini Flash for lightweight tasks
- **Responsiveness:** works on desktop and mobile (CSS media queries)
- **Security:** API key stored in `.env`, not in source code
- **Maintainability:** modular code (separate files for AI, DB, routes)

## User Scenarios
1. **Plan generation** – User enters details and gets a 7-day goal-specific plan.
2. **Feedback update** – User submits feedback and receives a refined plan.
3. **Nutrition tip** – User receives a short tip matching the goal (e.g., protein after workout for muscle gain).
4. **Admin view** – Admin/coach views all users and compares original vs updated plans.

## Software Requirements
| Item | Details |
|------|---------|
| Language | Python 3 |
| Backend framework | FastAPI |
| Server | Uvicorn (ASGI) |
| AI | Google Gemini API (`google-generativeai`) |
| Database | SQLite with SQLAlchemy ORM |
| Frontend | HTML, CSS, Jinja2 templates |
| Other libraries | python-multipart, python-dotenv, Pydantic |
| Tools | VS Code, Git, GitHub, virtualenv |

## Hardware Requirements
- Processor: Intel i3 or above
- RAM: 4 GB minimum
- Internet connection (for Gemini API calls)
- Any modern web browser

## Prerequisites (Knowledge)
FastAPI, Gemini API, HTML/CSS/Jinja2, Python, Git, SQLAlchemy & SQLite, virtual environments, Uvicorn.

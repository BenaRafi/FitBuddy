# 7. Project Documentation Phase

## Project Overview
FitBuddy is a FastAPI web application that integrates Google Gemini models to generate personalized 7-day workout plans and nutrition/recovery tips, update plans through user feedback, and provide an admin dashboard.

## Application Pages

### Home Page (`index.html`)
Form with **Name, User ID, Age, Weight (kg), Fitness Goal, Workout Intensity (Low/Medium/High)** and a **Generate Plan** button. Gym-themed background and clean UI.

### Personalized Workout Page (`result.html`)
- **User information:** name, ID, age, weight, goal, intensity
- **Workout plan:** day-wise plan (full body, upper/lower body, cardio, core, flexibility) with exercises, sets, reps/duration, rest intervals, plus warm-up and cooldown
- **Nutrition tip:** short practical advice (e.g., include protein in every meal)

### Feedback Section
User enters User ID and feedback. The system updates the plan through Gemini 1.5 Pro and shows a confirmation message.

### View All Users Page (`all_users.html`)
Shows all users with details, original plan and updated plan. Admin can delete users.

## API Endpoints
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Home page |
| `/generate-workout` | POST | Generate plan and tip |
| `/submit-feedback` | POST | Update plan with feedback |
| `/view-all-users` | GET | Admin dashboard |
| `/docs` | GET | Swagger API documentation |

## How to Use
1. Open the app in the browser.
2. Fill in your details and click **Generate Plan**.
3. Read your 7-day plan and nutrition tip.
4. Enter your User ID and feedback to update the plan.
5. Admin opens `/view-all-users` to monitor users.

## Installation Guide
See the [README](README.md) Quick Start section.

## Future Enhancements
- Cloud deployment (Render, Railway, etc.)
- User login and authentication
- Progress tracking and charts
- Meal and calorie planning
- Mobile app version

## Conclusion
FitBuddy demonstrates how generative AI can be combined with a web framework to deliver personalized, adaptive fitness guidance. Using Gemini 1.5 Pro and Flash with FastAPI, SQLAlchemy/SQLite and Jinja2, it produces tailored plans, refines them through feedback, and gives coaches a clear view of user activity.



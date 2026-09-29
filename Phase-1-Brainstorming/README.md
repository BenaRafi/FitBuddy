# 1. Brainstorming & Ideation Phase

## Project Title
**FitBuddy – AI Fitness Plan Generator using Gemini Models**

## Problem Statement
Many people want to stay fit but do not know how to build a structured workout routine that suits their goal, age, weight and fitness level. Hiring a personal trainer is costly, and generic plans found online are not personalized or adaptable.

## Purpose of the Project
To build a web application that uses Generative AI to create personalized 7-day workout plans and nutrition/recovery tips, and to update the plan based on user feedback.

## Ideas Considered
| Idea | Description | Decision |
|------|-------------|----------|
| AI workout plan generator | Generate a 7-day plan from user details | ✅ Selected |
| Feedback-based plan update | Regenerate plan using user feedback | ✅ Selected |
| Nutrition / recovery tips | Short tip based on user goal | ✅ Selected |
| Admin dashboard | View all users and their plans | ✅ Selected |
| Calorie / meal tracker | Log daily meals | ❌ Future scope |
| Mobile app | Android/iOS version | ❌ Future scope |

## AI Model Brainstorming
Hugging Face models (T5, BART, DistilBERT, Bloom) were tried first. They needed local GPU/hosting, fine-tuning and complex prompting to produce structured plans.

**Final choice: Google Gemini**
- **Gemini 1.5 Pro** – 7-day workout generation and plan updating
- **Gemini Flash** – fast nutrition/recovery tips

Reasons: API-based and easy to integrate with FastAPI, understands structured formats (days, sections), high accuracy with little prompt tuning, fast and scalable.

## Target Users
- Beginners and students starting their fitness journey
- Gym-goers who want structured routines
- Coaches/trainers managing multiple clients (admin view)

## Expected Outcome
A working web app where a user enters details, receives an AI-generated plan and tip, submits feedback for an updated plan, and an admin can monitor all users.

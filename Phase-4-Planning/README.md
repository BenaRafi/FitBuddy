# 4. Project Planning Phase

## Project Workflow (Milestones)
| Milestone | Activities |
|-----------|-----------|
| **1. Model Selection & Architecture** | Research and select Gemini models · Define architecture · Set up development environment |
| **2. Core Functionalities Development** | Develop workout, tip, feedback and storage functions · Implement FastAPI backend |
| **3. routes.py Development** | Write main application logic and routes |
| **4. Frontend Development** | Design UI (HTML/CSS) · Create dynamic Jinja2 templates |
| **5. Deployment** | Prepare local deployment · Test and verify |

## Timeline
| Week | Task | Milestone |
|------|------|-----------|
| 1 | Requirement study, AI model research, environment setup | 1 |
| 2 | AI functions (workout, tip, feedback update) and database | 2 |
| 3 | FastAPI routes and Pydantic schemas | 2–3 |
| 4 | Frontend templates and styling | 4 |
| 5 | Local deployment, testing, bug fixing | 5 |



## Team Roles and Responsibilities
| Member | Milestone / Activity | Responsibilities |
|--------|---------------------|------------------|
| Nithya Pushpam | Pre-requisites, Workflow, Milestone 5 (Activity 5.2) | Topic links, project workflow, testing and verifying local deployment |
| Vinothini | Milestone 1 (Activities 1.1, 1.2), Milestone 4 (Activity 4.2) | Research and select the generative AI model, define architecture, Jinja2 dynamic templates |
| Benazir R (Team Lead) | Milestone 1 (Activity 1.3), Milestone 2 (Activity 2.1), Milestone 4 (Activity 4.1) | Lead the team, set up development environment, develop core functionalities, design and develop the UI |
| Jamuna M | Milestone 2 (Activity 2.2), Milestone 3, Milestone 5 (Activity 5.1) | FastAPI backend (routing and user input), main application logic in routes, prepare local deployment |
| Pandiselvi | Conclusion | Project conclusion and documentation |

**Trainer / Guide:Premalatha

## Risks and Mitigation
| Risk | Mitigation |
|------|-----------|
| Gemini API key exposed | Store in `.env`, add `.env` to `.gitignore` |
| API errors / slow response | Use try-except and show error message |
| Inconsistent AI output format | Use structured prompts and `<pre>` display |
| Invalid user input | Pydantic validation |

# Project Journal

## Week 1
### What I worked on
- Defined the project scope, target audience, and problem statement for the HealthInfo Simplifier.
- Established strict product boundaries by differentiating educational simplification from medical diagnosis.
- Created the initial repository structure and drafted core documentation including the README, safety contract, and research questions.
- Designed the conceptual architecture flow from user to React frontend, Python FastAPI backend, and the AI model.

### What I learned
- Why healthcare AI projects require rigid safety boundaries and data constraints.
- The security risks of exposing API keys in frontend code versus keeping them secure on a backend server.
- The value of version control using Git commits as historical checkpoints for tracking project evolution.

### What confused me
- Balancing how much simplification an AI can do without unintentionally altering or omitting critical clinical context.

### Decisions I made
- Decided to completely restrict the application from storing any user health data or handling personal medical histories to prioritize privacy and safety.

### Problems I encountered
- Ensuring the safety contract clearly outlines what the app will not do without being overly restrictive to its core educational purpose.

### Questions I still have
- How can we systematically evaluate whether the AI's simplified output remains factually faithful to the original source text?

### What I will do next
- Move to Phase 2, focusing on researching trusted health sources and building a 20 to 30 passage evaluation dataset.
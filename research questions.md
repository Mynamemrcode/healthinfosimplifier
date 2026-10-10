# Research Questions and Architectural Decisions

## Question 1: Why not just use standard ChatGPT?
While general-purpose AI assistants can summarize text, building a dedicated application provides critical advantages for healthcare education:
- Controlled Scope: Constraining the system prompt and UI boundaries to prevent medical advice or diagnosis.
- Structured Output: Enforcing consistent formatting (plain-language summary, key terms, source attribution, and doctor discussion questions).
- Source Attribution: Guaranteeing that the original reference source remains visible and linked.
- Explicit Safety Rules: Hardcoding guardrails and fallback responses for health-related queries.
- Consistent Evaluation: Testing performance against a curated dataset of health passages to measure readability improvements and factual preservation.
- Dedicated User Experience: Designing a workflow tailored specifically for health literacy rather than general chat.

## Question 2: Why shouldn't the browser directly contain the AI API key?
- Security Risk: Exposing API keys in frontend browser code allows anyone using browser developer tools to steal your credentials, leading to unauthorized usage, financial loss, or account bans.
- Best Practice: Secrets and API keys must always reside securely on the backend server (Python FastAPI) where clients cannot access them.
Our HealthInfo Simplifier is a LLM Based web app that translates medical jargon into clear language that the common people can understand.
The target audience is the general public, or just anyone in need. 
The key focus is essential functionability in a single statement.

Imagine you found a medical article online that is full of confusing jargon when all you want to do is just understand a diagnosis or condition. With healthinfo Simplifier, you paste the text, and it breaks it down into plain old english. It showcases terms, what they mean, and provides references back to the trustworthy original sources. 

This app, HealthInfo Simplifier would use React and TypeScript to build the frontend with a python fastapi backend. The Api validates and sanitiizes given documents before passing prompts to an LLM. It parses the output into JSON that has the plain language text, definitions of key vocab, and source provenance links to ensure traceability.
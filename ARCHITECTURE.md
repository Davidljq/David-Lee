## 2. `ARCHITECTURE.md`

```markdown
# Architecture Overview

Below, sketch (ASCII, hand-drawn JPEG/PNG pasted in, or ASCII art) the high-level components of your agent.


<img width="1996" height="1155" alt="Architecture file" src="https://github.com/user-attachments/assets/b8b8d6ae-e62d-4d42-8765-4a0dd8283ae7" />


## Components

1. **User Interface**  
   - E.g., Streamlit, CLI, Slack bot  

2. **Agent Core**  
   - **Planner**: how you break down tasks  
   - **Executor**: LLM prompt + tool-calling logic  
   - **Memory**: vector store, cache, or on-disk logs  

3. **Tools / APIs**  
   - E.g., Google Gemini API, Tools, etc

4. **Observability**  
   - Logging of each reasoning step  
   - Error handling / retries  


## 2. `ARCHITECTURE.md`

```markdown
# Architecture Overview

Below, sketch (ASCII, hand-drawn JPEG/PNG pasted in, or ASCII art) the high-level components of your agent.

<img width="1996" height="1155" alt="Architecture file" src="https://github.com/user-attachments/assets/f2530d08-a652-480b-9ef1-67cb02d733ae" />




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


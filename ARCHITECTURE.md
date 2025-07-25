## 2. `ARCHITECTURE.md`

```markdown
# Architecture Overview

Below, sketch (ASCII, hand-drawn JPEG/PNG pasted in, or ASCII art) the high-level components of your agent.

<img width="1996" height="1155" alt="Architecture file" src="Architecture file.png" />





## Components

1. **User Interface**  
   - python, IPython Notebook 

2. **Agent Core**  
   - **Planner**: The agent’s logic first checks the user’s input type (file or website), loads content safely, scans for suspicious code patterns line by line, extracts URLs, validates them, queries VirusTotal if needed, then generates a single combined security report. 
   - **Executor**: The agent uses Python to validate and send API requests to VirusTotal, and then calls the Gemini LLM with a structured prompt to summarize all suspicious code and malicious URLs. The final output is user-friendly advice like a trusted friend.  
   - **Memory**: N/A 

3. **Tools / APIs**  
   - Google Gemini API, VirusTotal

4. **Observability**  
   - Logging of each reasoning step  
   - Error handling / retries  


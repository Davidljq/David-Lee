# Technical Explanation

## 1. Agent Workflow

Describe step-by-step how your agent processes an input:
1. Receive user input of API keys and 1 for file or 2 for websites  
2. Checks file or website against VirusTotal
3. If not suspicious, informs user that file or website is not suspicious
4. If suspicious, give 1 line description from VirusTotal (how many engines detected suspicious activity)
5. Calls Gemini AI to provide

## 2. Key Modules

- **Planner** (`planner.py`): No planner required  
- **Executor** (`executor.py`): No executor required  
- **Memory Store** (`memory.py`): No memory store required
- **User Interface**: Colab
- **LLM used**: Gemini AI
- **External Sites used**: https://www.virustotal.com/, https://aistudio.google.com/

## 3. Tool Integration

List each external tool or API and how you call it:

- VirusTotal API:	Checks if a URL is malicious or suspicious by sending the URL for scanning and retrieving the scan report.	Function: scan_url_virustotal(url, api_key)
  
- Gemini AI REST API:	Generates a user-friendly natural language explanation for why a file or URL is flagged as suspicious or malicious.	Function: call_gemini_rest_simple(target_label, api_key)

## 4. Observability & Testing

Explain your logging and how judges can trace decisions:
- Logs: Logging is done via print statements to console for simplicity. There are no separate logs/ directory — the script output shows step-by-step decisions in real time. For reproducibility, the results can be re-run by providing the same file or URL input.  
- Testing: Code fully tested in Colab.

## 5. Known Limitations

Be honest about edge cases or performance bottlenecks:
- Limited free API calls: May result in 429 Too Many Requests errors
- Only checked against VirusTotal and a local script. Local script only matches simple regex patterns like eval( or os.system.
- Local script won’t catch obfuscated code, encoded payloads, or sophisticated exploits.
- Local script has no static analysis, sandboxing, or real malware scanning — it’s just basic pattern-matching
- No multi-threading: Only scans a single URL or file to prevent 429 Too Many Requests Errors
- No persistent memory: Writes output to console, if the script crashes, past results are gone
- Does not sandbox suspicious codes, does not catch runtime behaviors, dropped files, or hidden malware
- Basic URL checks, relies solely on VirusTotal
- Minimal Error Handling: If VirusTotal or Gemini returns an unexpected JSON structure, the code might throw a KeyError or print fallback output
- Runs in notebook mode: No GUI, no API server, no chatbot front-end.

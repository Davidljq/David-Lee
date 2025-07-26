# MalwareMate, the malware checker

A **minimal agentic AI** that scans files or websites for malicious content using **VirusTotal** and **Gemini AI**.  
It combines **static code checks**, a **trusted threat intelligence API**, and a **friendly LLM explanation**, so anyone can understand if a file or URL is suspicious.

---

##  How It Works

**1. User Input:**  
- Pick a local file or website URL to scan.

**2. Static Checks:**  
- The agent scans code for suspicious patterns (like `eval(`, `os.system`, `<script>`, etc.).

**3. VirusTotal API:**  
- The agent calls VirusTotal’s API to check URLs against 90+ antivirus engines.

**4. Conditional Gemini AI:**  
- If a threat is found, the agent calls **Gemini AI** with a clear prompt:  
  _"Explain to me like a friend why this file or URL is malicious."_

**5. Final Report:**  
- The combined results help non-technical users understand exactly why the content is risky.

---

## Agentic Behavior

This tool demonstrates **agentic AI** principles:
- **Multiple tools:** VirusTotal + Gemini AI.
- **Conditional logic:** Only calls Gemini when suspicious.
- **Automatic actions:** Plans, decides, and explains.
- **User-friendly:** Generates plain-English advice.

---

## Folder Structure
```plaintext
project/
 src/
  ├── MalwareMate.ipynb      # Interactive notebook version
 ├── ARCHITECHTURE.MD        # Flow of script
 ├── Architecture file.png   # Diagram of the flow of the script
 ├── DEMO.md                 # Demo showing how it works and its limitations
 ├── EXPLANATION.md          # Details of the script
 ├── LICENSE                 # Apache2 License Agreement as part of the ODSC Hackathon
 ├── README.md               # This file!
 ├── TEST.sh                 # Test script
 ├── requirements.txt        # Dependencies


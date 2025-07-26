# 🛡️ Agentic AI Security Checker

A **minimal agentic AI** that scans files or websites for malicious content using **VirusTotal** and **Gemini AI**.  
It combines **static code checks**, a **trusted threat intelligence API**, and a **friendly LLM explanation**, so anyone can understand if their file or URL is risky.

---

## 🚀 How It Works

**1️⃣ User Input:**  
- Pick a local file or website URL to scan.

**2️⃣ Static Checks:**  
- The agent scans code for suspicious patterns (like `eval(`, `os.system`, `<script>`, etc.).

**3️⃣ VirusTotal API:**  
- The agent calls VirusTotal’s API to check URLs against 90+ antivirus engines.

**4️⃣ Conditional Gemini AI:**  
- If a threat is found, the agent calls **Gemini AI** with a clear prompt:  
  _"Explain to me like a friend why this file or URL is malicious."_

**5️⃣ Final Report:**  
- The combined results help non-technical users understand exactly why the content is risky.

---

## ✅ Agentic Behavior

This tool demonstrates **agentic AI** principles:
- **Multiple tools:** VirusTotal + Gemini AI.
- **Conditional logic:** Only calls Gemini when suspicious.
- **Automatic actions:** Plans, decides, and explains.
- **User-friendly:** Generates plain-English advice.

---

## 📂 Folder Structure

```plaintext
project/
 ├── main.ipynb          # Interactive notebook version
 ├── main.py             # (Optional) .py version if you convert
 ├── TEST.sh             # Test script to run headlessly
 ├── requirements.txt    # Dependencies
 ├── README.md           # This file!

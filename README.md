# PhishGuard 🛡️
## AI-Powered Gmail Phishing Detection System
Capstone Project 2025 | ITAI 2277

# Overview

PhishGuard is a hybrid security tool that integrates directly with Gmail to detect sophisticated phishing attacks. Unlike traditional filters that rely on simple blacklists, PhishGuard uses Generative AI (GPT-4) to analyze the intent and tone of emails, combined with VirusTotal to verify the reputation of embedded links.

It features an Adaptive Learning System, allowing users to correct the model's mistakes, which instantly retrains the system context without code changes.

# Features

📧 Real-Time Gmail Integration: Fetches and scans emails directly from your inbox using IMAP.

🧠 Hybrid Analysis: Combines LLM psychological analysis with VirusTotal technical reputation checks.

🎓 Reinforcement Learning: "Mark as Safe" / "Mark as Phishing" buttons save feedback to a local database to improve future accuracy.

🚦 Consensus Scoring: Reduces false positives by requiring multiple security vendors to flag a URL before marking it as dangerous.

📊 Interactive Dashboard: Built with Gradio for a user-friendly experience.

# Tech Stack

Python 3.10+
Gradio (Frontend UI)
OpenAI API (GPT-4o-mini)
VirusTotal API v3 (URL Scanning)
IMAPlib (Email Retrieval)

# Installation

Clone the Repository
git clone https://github.com/yourusername/phishguard.git
cd phishguard

## Install Dependencies
pip install -r requirements.txt

## Get API Keys
OpenAI: https://platform.openai.com/
VirusTotal: https://www.virustotal.com/

## Gmail App Password: Go to Google Account > Security > 2-Step Verification > App Passwords.

# Usage

Run the App
python app.py
Open Browser
Navigate to the local URL provided (usually http://127.0.0.1:7860).

# Setup Keys
Go to the Setup tab and enter your OpenAI and VirusTotal API keys.

Scan Emails
Go to Scan Inbox.
Enter your Gmail address and App Password.
Click Fetch Emails.
Select an email index (e.g., 0 for the newest) and click Scan.

Project Structure

phishguard/
├── app.py                 # Main application logic
├── requirements.txt       # Python dependencies
├── README.md             # Documentation
├── user_corrections.json  # (Generated) Local memory for RL
└── feedback_data/        # Directory for logs


License

This project is for educational purposes as part of the ITAI 2277 Capstone.

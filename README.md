# 🧠 Smart Job Applier Bot

A modular, AI-enhanced automation tool for applying to job roles across platforms like Naukri, LinkedIn, and Indeed. Built for scalability, observability, and resilience, this bot streamlines your job hunt with secure login, dynamic scraping, intelligent question answering, and real-time feedback.

---

## 🚀 Features

- 🔍 **Dynamic Job Scraping**: Resilient selectors with fallback logic for platform-specific job listings.
- 📝 **Automated Form Filling**: Secure credential handling and adaptive field mapping.
- 🤖 **AI Integration**: Smart responses to application questions and auto-generated cover letters.
- 🖥️ **GUI + CLI Support**: Tkinter interface and CLI flags for flexible control.
- 🛎️ **System Tray Notifications**: Real-time feedback on job status and errors.
- 📊 **Observability Dashboard**: Logs, analytics, and visual reports for tracking submissions.
- ⏱️ **Scheduler**: Immediate and periodic execution with graceful shutdown and resume.

---

## 🧩 Folder Structure
job_applier_bot/
├── main.py                  # Entry point and orchestrator
│
├── gui/                     # Tkinter GUI components
│   ├── interface.py         # Main GUI window and layout
│   └── widgets.py           # Custom input fields, buttons, etc.
│
├── cli/                     # CLI argument parser
│   └── parser.py            # argparse-based flag handling
│
├── scraper/                 # Site-specific scraping logic
│   ├── naukri.py            # Naukri-specific scraper
│   ├── linkedin.py          # LinkedIn-specific scraper
│   ├── indeed.py            # (Optional) Indeed scraper
│   └── utils.py             # Shared scraping utilities
│
├── applier/                 # Form filling and submission logic
│   ├── login.py             # Secure login and session management
│   ├── submit.py            # Form submission engine
│   └── selectors.py         # Dynamic XPath/CSS selectors
│
├── ai/                      # AI-driven Q&A and cover letter generation
│   ├── responder.py         # Generates answers to job questions
│   └── templates/           # Cover letter and resume templates
│       └── default.md
│
├── utils/                   # Logging, notifications, error handling
│   ├── logger.py            # Log setup and rotation
│   ├── notifier.py          # System tray and desktop notifications
│   └── diagnostics.py       # Screenshot capture and error tracebacks
│
├── config/                  # Credentials, settings, selectors
│   ├── credentials.env      # Encrypted login credentials
│   ├── settings.yaml        # User preferences and flags
│   └── selectors.json       # Site-specific field mappings
│
├── scheduler/               # Job timing and execution
│   ├── runner.py            # Immediate and periodic execution
│   └── cron.py              # Cron-style scheduling logic
│
├── dashboard/               # Analytics and job tracking
│   ├── tracker.py           # Submission history and metrics
│   └── report.html          # Visual dashboard output
│
├── assets/                  # Icons, screenshots, logs
│   ├── tray_icon.ico        # System tray icon
│   ├── error_screenshots/   # Screenshots on failure
│   └── logs/                # Timestamped logs
│
└── requirements.txt         # Python dependencies

---

## ⚙️ Installation

```bash
git clone https://github.com/8ASHURA24/job_applier_bot.git
cd job_applier_bot
pip install -r requirements.txt

# n8n_job_match_automation

[![n8n](https://img.shields.io/badge/Automation-n8n-2088FF?logo=n8n)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/AI-OpenAI-412991?logo=openai)](https://openai.com/)
[![Telegram](https://img.shields.io/badge/Chat-Telegram-2CA5E0?logo=telegram)](https://core.telegram.org/bots)
[![Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python)](https://www.python.org/)
[![BeautifulSoup](https://img.shields.io/badge/Scraper-BeautifulSoup-4E9A06)](https://www.crummy.com/software/BeautifulSoup/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Automated AI job matcher — Scrapes recent job postings, scores them against your resume with OpenAI, and sends top matches to Telegram.

---

## Features
- Automated job search – Finds fresh postings from your chosen search URL.
- AI-powered scoring – Uses OpenAI to evaluate job descriptions against your resume.
- Customizable threshold – Filters out low-score matches.
- Instant notifications – Sends shortlisted roles straight to your Telegram chat.
- Environment-based config – Keep your resume and credentials out of source control.

---

## Tech Stack
- [n8n](https://n8n.io/) – Workflow automation
- [OpenAI API](https://openai.com/) – Job matching logic
- [Telegram Bot API](https://core.telegram.org/bots) – Notifications
- [Python](https://www.python.org/) – Parsing and scraping
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) – HTML extraction

---

## Setup

### 1. Prerequisites
- n8n ≥ 1.0
- OpenAI API key
- Telegram bot token + chat ID
- Python code execution enabled in n8n

### 2. Environment Variables
Create a `.env` file (or configure in n8n's environment settings):

```env
RESUME_TEXT="Paste your resume text here"
SEARCH_URL="https://www.linkedin.com/jobs/search/?keywords=Java%20OR%20Spring%20Boot&location=United%20Kingdom&f_TPR=r10800"
MIN_SCORE=50
PAUSE_SECONDS=10
TELEGRAM_CHAT_ID=123456789
OPENAI_MODEL=gpt-4o-mini

# 📧 n8n Email Automation Engine

![Built With n8n](https://img.shields.io/badge/Built%20With-n8n-orange)
![Automation](https://img.shields.io/badge/Type-Workflow%20Automation-blue)
![Project](https://img.shields.io/badge/Project-Marketing%20Automation-green)
![Status](https://img.shields.io/badge/Status-Portfolio-blue)

A **MailerLite-style email automation system** built using **n8n workflows and Google Sheets**.

This project demonstrates how to design a **multi-step email drip campaign system** that automatically sends onboarding or marketing emails to leads while tracking progress and logging automation activity.

The system replicates core functionality of marketing automation platforms like:

- MailerLite
- ConvertKit
- ActiveCampaign

---

# 🚀 Features

- Multi-step email automation
- Email template management
- Lead state tracking
- Automation logging
- Delay scheduling between emails
- Google Sheets integration
- Workflow automation using n8n

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|--------|
| n8n | Workflow automation engine |
| Google Sheets | Database for leads, templates, and logs |
| SMTP / Email Node | Sending automated emails |
| HTML Templates | Email content formatting |

---

# 🎯 Project Overview

This project demonstrates how marketing automation platforms manage automated email campaigns.

The workflow automates:

- onboarding email sequences
- marketing drip campaigns
- lead tracking
- automation monitoring

---

# 🏗 System Architecture

The automation system consists of three core components.

## Email Templates

Stores reusable email templates.

| Name | Subject | HTML |
|------|--------|------|
| welcome | Welcome to Agile IT Tech | HTML template |
| day1 | What We Do | HTML template |
| day2 | Social Proof | HTML template |
| day3 | Value | HTML template |
| day4 | Last Chance | HTML template |

These templates are dynamically loaded by the workflow.

---

## Lead State Tracking

Tracks subscriber progress in the automation sequence.

| Email | Role | Current Step | Status | Last Updated |
|------|------|-------------|--------|-------------|
| user@email.com | BA | day2 | active | timestamp |

The workflow reads the **current_step** column to determine the next email.

---

## Automation Logs

Logs all automation activity.

| Time | Email | Step | Status | Error |
|------|------|------|--------|------|
| timestamp | user@email.com | welcome | sent | |

Logs help monitor:

- email delivery
- workflow execution
- automation failures

---

# 🧠 Automation Architecture

The system follows a workflow automation architecture.
Lead Enters System
│
▼
Load Email Template
│
▼
Send Email
│
▼
Log Automation Event
│
▼
Update Lead State
│
▼
Wait (Delay)
│
▼
Next Email Step

---

# 🔄 Workflow Logic

The automation runs as a drip email campaign.
Trigger
↓
Send Welcome Email
↓
Wait
↓
Send Day1 Email
↓
Wait
↓
Send Day2 Email
↓
Wait
↓
Send Day3 Email
↓
Wait
↓
Send Day4 Email

Each step updates the **lead state sheet**.

---

# 📷 Screenshots

## n8n Automation Workflow

![Workflow](Workflow/images/workflow-image.png)

---

## Email Templates (Google Sheets)

![Templates](Workflow/images/email-template.png)

---

## Lead State Tracking

![Lead State](Workflow/images/lead-state.png)

---

## Automation Logs

![Logs](Workflow/images/automation-log.png)

---

# 📂 Project Structure
n8n-email-automation-engine
│
├── README.md
│
├── Workflow
│ ├── email_automation_workflow.json
│ └── images
│ ├── workflow-image.png
│ ├── email-template.png
│ ├── lead-state.png
│ └── automation-log.png

---

# ⚙ Setup Instructions

## Install n8n

Using npm:
npm install n8n -g


Using Docker:


docker run -it --rm -p 5678:5678 n8nio/n8n


---

## Import Workflow

1. Open the **n8n dashboard**
2. Click **Import Workflow**
3. Upload the workflow JSON file

---

## Configure Credentials

Set up credentials for:

- Google Sheets
- SMTP Email provider

---

## Activate Workflow

Activate the workflow to start sending automated email sequences.

---

# 📊 Example Email Sequence

| Step | Email |
|------|------|
| Step 1 | Welcome Email |
| Step 2 | What We Do |
| Step 3 | Social Proof |
| Step 4 | Value |
| Step 5 | Last Chance |

---

# 💡 Future Improvements

- Email open tracking
- Click tracking
- Unsubscribe system
- Lead segmentation
- Analytics dashboard

---

# 📚 Learning Outcomes

This project demonstrates:

- workflow automation design
- marketing automation architecture
- state management
- automation logging
- third-party integrations

---

# 👨‍💻 Author

**Pa1KalyanY**

GitHub  
https://github.com/Pa1KalyanY

---

⭐ If you found this project useful, consider **starring the repository**.

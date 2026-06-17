# Customer Support Automation using n8n

## Overview

This repository contains two versions of an automated customer support system built using **n8n**, **Google Sheets**, **Gmail**, **JavaScript**, and **Google Gemini AI**.

The project automatically detects new customer requests submitted through Google Sheets, categorizes them, sends automated email responses, and logs processed requests into another Google Sheet.

The repository demonstrates the evolution from a traditional rule-based workflow to an AI-powered workflow with intelligent classification and failure handling.

---

## Project Versions

### V1: Rule-Based Workflow

A deterministic workflow that uses JavaScript and Switch nodes to classify customer queries into predefined categories.

**Features:**

* Google Sheets Trigger
* JavaScript preprocessing
* Rule-based categorization
* Gmail automated responses
* Logging to Google Sheets

Supported categories:

* Billing
* Technical
* Feedback

---

### V2: AI-Powered Workflow

An enhanced workflow that leverages **Google Gemini AI** for intelligent query classification.

**Additional Features:**

* AI-based customer query classification
* Google Gemini integration
* AI failure detection and fallback handling
* AI status logging
* Automated AI failure email alerts

---

## Workflow Architecture

### V1 Architecture

```text
Google Sheets Trigger
        ↓
JavaScript Processing
        ↓
Switch Node
   ┌──────────┬────────────┬───────────┐
 Billing   Technical   Feedback
    ↓          ↓           ↓
 Gmail      Gmail       Gmail
    └──────────┴───────────┘
              ↓
      Append Row in Sheet
```

### V2 Architecture

```text
Google Sheets Trigger
        ↓
Preprocess Query
        ↓
Google Gemini AI
        ↓
Merge Results
        ↓
Switch Node
 ┌────────┬──────────┬──────────┬───────────┐
Billing Technical Feedback AI Failed
    ↓         ↓         ↓          ↓
 Gmail     Gmail     Gmail   Alert Email
    └─────────┴─────────┴──────────┘
                  ↓
         Log Support Request
```

---

## Repository Structure

```text
ai-customer-support-agent-n8n/
│
├── v1-rule-based/
│   ├── workflow.json
│   ├── README.md
│   └── screenshots/
│
├── v2-ai-based/
│   ├── workflow.json
│   ├── README.md
│   └── screenshots/
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Technologies Used

* n8n
* JavaScript
* Google Sheets API
* Gmail API
* Google Gemini AI
* AI Prompt Engineering

---

## Key Features

* Automated customer support workflow
* Real-time Google Sheets trigger
* Email automation using Gmail
* Query classification
* AI-powered routing
* Failure handling and alerts
* Audit logging
* Scalable workflow design

---

## Future Improvements

* Dynamic AI-generated email responses
* Sentiment analysis
* Ticket ID generation
* Slack/Discord notifications
* Database integration
* Dashboard for analytics
* Multi-language support

---

## Author

Pratham Singh

---

## License

This project is licensed under the MIT License.

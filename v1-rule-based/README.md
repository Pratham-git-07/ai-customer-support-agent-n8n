# Customer Support Automation (V1)

## Overview

This project implements a rule-based customer support automation workflow using n8n.

The workflow automatically processes customer requests submitted through Google Sheets, routes them based on category, sends email responses using Gmail, and logs processed requests into another Google Sheet.

## Features

* Google Sheets Trigger
* JavaScript Data Processing
* Switch-based Routing
* Gmail Integration
* Request Logging
* Audit Trail Generation

## Categories Supported

* Billing
* Technical
* Feedback

## Workflow

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

## Screenshots

### Workflow Overview

<img width="1847" height="851" alt="workflow-overview" src="https://github.com/user-attachments/assets/6ec0b972-a109-4fc3-bc52-0f1fcfe315ae" />


### Input Sheet

<img width="1441" height="635" alt="google-sheet-input" src="https://github.com/user-attachments/assets/085c7b55-f92e-40fe-bde0-ae8d22c6a756" />


### Log Sheet

<img width="1637" height="573" alt="log-sheet" src="https://github.com/user-attachments/assets/f15d6587-e382-448f-94db-32ceeaab8406" />


## Technologies Used

* n8n
* JavaScript
* Google Sheets API
* Gmail API

## Future Improvements

* AI-based query classification
* AI-generated email responses
* Ticket ID generation
* Sentiment analysis

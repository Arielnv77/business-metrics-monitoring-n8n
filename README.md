
# Event-Driven Business Metrics Monitoring (n8n)

This project implements an event-driven automation system to monitor business metrics, detect anomalies, and store only relevant alerts for further analysis.

The goal is to reduce noise and focus exclusively on signals that require action.

---

## 🚀 Overview

Companies often track multiple metrics at once (sales, leads, churn, etc.), but reacting to every data point creates unnecessary noise.

This system:
- Receives multiple business metrics via webhook
- Normalizes and evaluates each metric automatically
- Detects anomalies based on predefined thresholds
- Stores only alert-level events in Google Sheets

---

## 🧠 How It Works

1. **Webhook ingestion**  
   Metrics are sent as a JSON payload to an n8n webhook.

2. **Normalization & rule evaluation**  
   Incoming metrics are normalized into a standard structure and evaluated against business thresholds.

3. **Event-based processing**  
   Each metric is processed as an independent event.

4. **Alert filtering**  
   Only metrics in an `ALERT` state continue through the workflow.

5. **Human-readable alert generation**  
   Alert messages are generated in a concise, business-friendly format.

6. **Persistence**  
   Alerts are appended to Google Sheets for tracking and analysis.

---

# Event-Driven Business Metrics Monitoring (n8n)

This project implements an event-driven automation system to monitor business metrics, detect anomalies, and store only relevant alerts for further analysis.

The goal is to reduce noise and focus exclusively on signals that require action.

---

## 🚀 Overview

Companies often track multiple metrics at once (sales, leads, churn, etc.), but reacting to every data point creates unnecessary noise.

This system:
- Receives multiple business metrics via webhook
- Normalizes and evaluates each metric automatically
- Detects anomalies based on predefined thresholds
- Stores only alert-level events in Google Sheets

---

## 🧠 How It Works

1. **Webhook ingestion**  
   Metrics are sent as a JSON payload to an n8n webhook.

2. **Normalization & rule evaluation**  
   Incoming metrics are normalized into a standard structure and evaluated against business thresholds.

3. **Event-based processing**  
   Each metric is processed as an independent event.

4. **Alert filtering**  
   Only metrics in an `ALERT` state continue through the workflow.

5. **Human-readable alert generation**  
   Alert messages are generated in a concise, business-friendly format.

6. **Persistence**  
   Alerts are appended to Google Sheets for tracking and analysis.

---

# Tech Stack
	•	n8n (self-hosted, Docker)
	•	JavaScript (workflow logic)
	•	Google Sheets API (OAuth 2.0)
	•	Webhooks (HTTP-based ingestion)

## 🧩 Example Input

```json
{
  "company": "DemoCorp",
  "period": "2026-03",
  "metrics": {
    "monthly_sales": 5000,
    "new_leads": 30,
    "churn_rate": 0.06
  }
}

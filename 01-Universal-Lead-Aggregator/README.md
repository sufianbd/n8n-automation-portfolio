# 01. Universal Lead Aggregator

## 📋 Project Overview
**Primary Goal:** Centralize and normalize lead data from disparate sources (Webforms, Ads, Partners) into a single, clean database structure.

**Description:**
A robust data pipeline that accepts raw JSON payloads via Webhook, standardizes formatting (e.g., capitalization, date stamping), validates email integrity to block spam, and routes valid leads to a master Google Sheet.

## 🛠 Technical Implementation
* **Trigger:** Webhook (POST) receiving JSON payloads.
* **Logic:** Javascript (Code Node) to normalize string capitalization and generate ISO timestamps.
* **Validation:** Conditional Logic (If Node) to filter out generic spam domains.
* **Storage:** Google Sheets API (Service Account Auth).

## 📸 Workflow Diagram
[Webhook] --> [Edit Fields (Normalize)] --> [If (Validate Email)]
                                                   |
                                            (True) v
                                             [Google Sheets]


## 🧪 How to Test
1. Import the `workflow.json` into n8n.
2. Activate the workflow.
3. Send a POST request to the Webhook URL with this JSON body:

```json
{
  "name": "john doe",
  "email": "john.doe@tech-example.com",
  "budget": 5000,
  "source": "Facebook Ads"
}

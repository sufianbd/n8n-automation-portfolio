# 03. Enriched RevOps Pipeline

## 📋 Project Overview
**Primary Goal:** Automate lead research and CRM data entry to reduce manual sales labor.

**Description:**
A revenue operations pipeline that detects new leads, parses their email domain, enriches the profile with company data (Employee Count, Revenue), and syncs it to HubSpot. It includes a "VIP Alert" system for high-value prospects.

## 🛠 Technical Implementation
* **API Simulation:** Integrated mock REST API responses to simulate data enrichment services (like Clearbit).
* **Data Normalization:** Mapped raw numerical data to specific CRM dropdown values (e.g., converting `120000` to `"1000+"`).
* **Rich Notifications:** Designed Block Kit JSON payloads for Slack to display company logos and formatted text for sales alerts.

## 📸 Workflow Diagram
[Webhook] --> [Code (Parse Domain)] --> [HTTP Request (Enrichment API)]
                                                        |
                                                        v
                                          [If (VIP Check: Employees > 50)]
                                            |
                                            v
                                   [HubSpot (Upsert Contact)] --> [Slack Alert]

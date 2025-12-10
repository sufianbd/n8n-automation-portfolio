# 02. Dynamic PDF Invoice Engine

## 📋 Project Overview
**Primary Goal:** Automate the generation and delivery of financial documents based on raw transactional data.

**Description:**
A backend engine that accepts billing data via Webhook, performs complex tax/total calculations via JavaScript, generates an HTML template, converts it to a binary PDF file, and emails it to the client automatically.

## 🛠 Technical Implementation
* **Binary Data:** Advanced manipulation of binary streams to convert HTML strings into PDF files.
* **Code Node:** Custom JavaScript to calculate sub-totals, apply tax rates (10%), and generate unique Invoice IDs.
* **Email Delivery:** Automated attachment handling via Gmail API.

## 📸 Workflow Diagram
[Webhook] --> [Code Node (Calc Logic)] --> [Convert to File (HTML to PDF)]
                                                        |
                                                        v
                                            [Gmail (Send Attachment)]

# 06. Secure Freelance Onboarding System

## 📋 Project Overview
**Primary Goal:** Streamline client acquisition while maintaining security and configurability.

**Description:**
A template-based system for handling new client inquiries via Webhook (or Email). It features a "Global Config" node for easy setting updates and separates logic from credentials, ensuring a secure handover to clients.

## 🛠 Technical Implementation
* **Parameterization:** Created a "Soft Variable" control panel (Global_Config) allowing non-technical users to update email addresses and thresholds without editing node logic.
* **Credential Security:** Architected the solution for secure JSON export, ensuring API keys are stripped before client handover.
* **Dynamic Mapping:** Used expressions to reference global variables across multiple nodes (Trello, Gmail).

## 📸 Workflow Diagram
[Webhook] --> [Global_Config (Variables)] --> [If (Budget > Min)]
                                                      |
                                               (True) v
                                          [Trello (Create Card)]
                                                      |
                                                      v
                                            [Gmail (Send Contract)]

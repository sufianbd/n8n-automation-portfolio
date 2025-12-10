# 04. Autonomous AI Support Agent

## 📋 Project Overview
**Primary Goal:** Deploy an intelligent agent capable of context-aware conversation and tool usage.

**Description:**
An AI Agent utilizing OpenAI's LLM that goes beyond simple chat. It acts as a Tier 1 Support Rep that can "remember" conversation history and autonomously decide to use external tools (Calculator, Database) based on user intent.

## 🛠 Technical Implementation
* **LangChain Integration:** Built using the n8n AI Agent node (LangChain framework).
* **Tool Calling:** Configured custom tools allowing the LLM to write to a Google Sheet database only when specific intent (e.g., "Report Bug") is detected.
* **System Prompting:** Engineered robust system instructions to define the agent's persona and guardrails.
* **Memory Management:** Implemented Window Buffer Memory to maintain conversational context.

## 📸 Workflow Diagram
[Chat Trigger] --> [AI Agent Controller] <--> [OpenAI Model (Brain)]
                            |
                            +--> [Tool: Calculator]
                            |
                            +--> [Tool: Google Sheets (Ticket DB)]
                            |
                            +--> [Memory: Window Buffer]

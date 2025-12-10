# 07. Capstone Project: Daily Market Intelligence Bot

## 🏆 Project Overview
**Primary Goal:** Create an autonomous research agent that monitors news trends and delivers executive summaries.

**Description:**
The "Final Exam" of the n8n Mastery Course. This workflow combines API integration, Code logic, and Generative AI into a single pipeline. It fetches global news, filters for "Artificial Intelligence" stories, uses Javascript to slice the data, and employs GPT-4o to write a daily executive briefing delivered via email.

## 🛠 Technical Implementation
* **NewsAPI Integration:** HTTP Request node fetching real-time data with query parameters.
* **Javascript Optimization:** Custom code to slice large JSON arrays (reducing 100 items to 3) before sending to AI, optimizing token usage and cost.
* **LangChain AI:** Integrated the OpenAI Chat Model to synthesize disparate news articles into a cohesive paragraph.
* **Reliability:** Connected to a Global Error Handler to alert via Slack if the News API fails.

## 📸 Workflow Diagram
[Schedule] --> [HTTP Request (NewsAPI)] --> [Code (Slice Top 3)]
                                                    |
                                                    v
                                          [OpenAI (Summarize)]
                                                    |
                                                    v
                                            [Gmail (Send Brief)]





  For Another Chat Model Such as Google Gemini Chat Model

  # 08. Gemini-Powered AI Assistant

## 📋 Project Overview
**Primary Goal:** Leverage Google's advanced Gemini Pro model to build a high-speed, cost-effective conversational agent.

**Description:**
This workflow replaces traditional LLMs with **Google Gemini Pro** via n8n's native integration. It demonstrates how to authenticate with Google Cloud Vertex AI (or Google AI Studio), manage conversational memory, and generate complex text responses for customer support or content creation tasks.

## 🛠 Technical Implementation
* **Model Integration:** Utilized the **Google Gemini Chat Model** node for high-speed inference and large context window capabilities.
* **Authentication:** Configured Google credentials securely (using API Key or Service Account).
* **Memory Architecture:** Implemented a **Window Buffer Memory** to allow the Gemini model to retain context of the last 5 interactions.
* **Chain Logic:** Connected via the **Basic LLM Chain** to streamline the prompt-response cycle.

## 📸 Workflow Diagram
[Chat Trigger] --> [Basic LLM Chain] <--> [Google Gemini Chat Model]
                            |
                            +--> [Window Buffer Memory]




                            # 07. Capstone Project: Daily Market Intelligence Bot

## 🏆 Project Overview
**Primary Goal:** Create an autonomous research agent that monitors news trends and delivers executive summaries.

**Description:**
The "Final Exam" of the n8n Mastery Course. This workflow combines API integration, Code logic, and Generative AI into a single pipeline. It fetches global news, filters for "Artificial Intelligence" stories, uses Javascript to slice the data, and employs GPT-4o to write a daily executive briefing delivered via email.

## 🛠 Technical Implementation
* **NewsAPI Integration:** HTTP Request node fetching real-time data with query parameters.
* **Javascript Optimization:** Custom code to slice large JSON arrays (reducing 100 items to 3) before sending to AI, optimizing token usage and cost.
* **LangChain AI:** Integrated the OpenAI Chat Model to synthesize disparate news articles into a cohesive paragraph.
* **Reliability:** Connected to a Global Error Handler to alert via Slack if the News API fails.

## 📸 Workflow Diagram
[Schedule] --> [HTTP Request (NewsAPI)] --> [Code (Slice Top 3)]
                                                    |
                                                    v
                                          [OpenAI (Summarize)]
                                                    |
                                                    v
                                            [Gmail (Send Brief)]

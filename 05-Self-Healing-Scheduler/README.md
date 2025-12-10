# 05. Self-Healing Data Scheduler

## 📋 Project Overview
**Primary Goal:** Ensure workflow reliability and data integrity during bulk processing operations.

**Description:**
A resilient batch-processing system designed to handle external API failures gracefully. Instead of crashing when a single item fails (e.g., a broken URL), the system isolates the error, logs it to a separate "Error Database," and continues processing the remaining queue without interruption.

## 🛠 Technical Implementation
* **Loop Isolation:** utilized the "Split in Batches" node to process items individually, creating a firewall between data points.
* **Error Routing:** Configured "Continue On Fail" settings to capture error JSON instead of stopping execution.
* **Feedback Loops:** Designed closed-loop architecture to ensure the process returns to the start of the batch after handling exceptions.

## 📸 Workflow Diagram
[Schedule] --> [Split in Batches (Loop)]
                        |
                        v
          [HTTP Request (Continue On Fail)]
                        |
                        v
                 [If (Error Exists?)]
                  |              |
           (True) v              v (False)
        [Log to Error DB]    [Log to Success DB]
                  |              |
                  +----<---------+
             (Loop back to Splitter)

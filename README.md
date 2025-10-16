# sprint-feedback-automation-ifttt-make
Automated sprint feedback workflow using IFTTT + Make + Google Sheets + Gmail to collect responses and email summaries post-sprint.
# 🧩 Sprint Feedback Automation (IFTTT + Make)

## 📌 Overview
This automation streamlines the sprint retrospective process by automatically:
- Triggering at sprint end (via Google Calendar)
- Sending a feedback form to all team members
- Waiting 24 hours for responses
- Aggregating data from Google Sheets
- Emailing the sprint summary to the Project Manager

---

## ⚙️ Tools & Platforms Used
| Tool | Purpose |
|------|----------|
| **IFTTT** | Detects sprint-end event from Google Calendar and sends data to Make |
| **Make (Integromat)** | Handles delay, Google Sheets lookup, and automated summary email |
| **Google Sheets** | Stores form responses and calculates averages |
| **Google Forms** | Collects team feedback |
| **Gmail** | Sends automated summary email to PM |

---



## 🔄 Workflow Steps
1. **IFTTT Trigger:** Calendar event “Sprint End — Sprint X” starts  
2. **IFTTT Action:** Webhook → Sends data (Sprint name, date) to Make  
3. **Make Scenario:**
   - Sleep for 24 hours  
   - Search Sprint in Google Sheets (Summary tab)  
   - Send summary via Gmail  
4. **Google Sheets:** Formulas calculate average ratings and text summaries.

---


---

## 🧱 Architecture

Google Calendar (Sprint End)
        ↓
     IFTTT (Webhook)
        ↓
     Make (24h Delay)
        ↓
   Google Sheets (Lookup)
        ↓
      Gmail (Summary Email)

https://drive.google.com/file/d/16QS6NJA3mOY0NVcFBMW6MD4oEQ6gGTNz/view?usp=sharing
https://drive.google.com/file/d/1Do398T39P5knEDFmIHY6DJ1sk3EoBktc/view?usp=sharing

# AI Job Search Automation using n8n

An AI-powered job search automation workflow built with **n8n** that analyzes a resume, finds relevant internships/jobs, scores them using LLMs, and delivers organized results via Google Sheets and email.

---

## Features

* Downloads a resume PDF from Google Drive
* Extracts text from the resume
* Uses **Groq LLM** to identify:

  * target roles
  * technical skills
  * job search keywords
  * internship keywords
* Searches jobs from multiple platforms:

  * **RemoteOK**
  * **Arbeitnow**
  * **Internshala**
  * **Google Jobs (via SerpAPI)**
* Cleans and merges results from all sources
* Removes duplicate job listings
* Scores job relevance using AI
* Saves results to Google Sheets
* Sends a formatted email summary of matched jobs

---

## Workflow Overview

1. **Manual Trigger**
2. **Download Resume PDF** from Google Drive
3. **Extract Resume Text**
4. **Build Resume Prompt**
5. **Groq Keyword Extraction**
6. **Parse Resume Keywords**
7. **Fetch jobs** from multiple sources
8. **Parse and clean** the job data
9. **Merge + deduplicate** jobs
10. **Score jobs using AI**
11. **Append results to Google Sheets**
12. **Send email summary via Gmail**

---

## Tech Stack

* **n8n**
* **Groq API**
* **SerpAPI**
* **Google Drive**
* **Google Sheets**
* **Gmail**
* **RemoteOK API**
* **Arbeitnow API**

---

## Setup

1. Import `workflow.json` into n8n.
2. Configure the required credentials inside n8n:

   * Google Drive OAuth2
   * Google Sheets OAuth2
   * Gmail OAuth2
   * Groq API / HTTP Request authentication
3. Replace placeholder values in the workflow where required:

   * `YOUR_GROQ_API_KEY_HERE`
   * `YOUR_SERPAPI_KEY_HERE`
   * `YOUR_GOOGLE_SHEET_ID_HERE`
   * `YOUR_EMAIL_HERE`
4. Update the Google Drive Resume file ID and target Google Sheet ID.
5. Run the workflow manually or schedule it for periodic execution.

---

## Use Case

This workflow is useful for:

* students searching for internships
* freshers applying for entry-level roles
* automating repetitive job search tasks
* ranking job opportunities based on resume relevance

---

## Important Note

Do **not** upload real API keys, tokens, or personal credentials to GitHub.
Use **n8n credentials** or **environment variables** to keep secrets secure.

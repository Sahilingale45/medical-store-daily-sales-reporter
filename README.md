# medical-store-daily-sales-reporter
A scheduled automation workflow that fetches daily pharmaceutical sales sheets, processes metrics using JavaScript logic, evaluates data via a conditional IF node, and sends aggregated report emails via Gmail.
# Medical Store Daily Sales Report Automation

This repository houses a scheduled integration workflow designed to compile pharmacy ledger transactions automatically, run analytical data calculations via an internal JavaScript node, and email finalized reporting summaries using Gmail.

## 🚀 How It Works
1. **Trigger (Schedule Trigger):** Fires automatically on a recurring routine schedule (e.g., every day at 9:00 PM) to initialize the pharmacy processing sequence.
2. **Data Polling (Google Sheets - Get row(s) in sheet):** Pulls down transactional logs or ledger lines representing the current day's itemized drug and equipment sales.
3. **Data Calculation (Code in JavaScript):** Processes the rows using custom JavaScript to parse individual totals, summarize net revenue, track quantity numbers, or filter for anomalies.
4. **Validation (If):** Evaluates if the output contains actionable summary items (`true`). If empty (`false`), it can safely stop or fall back to evaluate alternate lines.
5. **Report Layout (Edit Fields1):** Formats raw math variables and strings into structured textual paragraphs ready for a human reader.
6. **Notification Delivery (Gmail - Send a message):** Connects to your email delivery node to send the daily closing report summary straight to management or store owners.
7. **Flag Logging (Google Sheets - Update row in sheet):** Updates tracking markers back on the core sheet to verify that these specific logs have been safely accounted for and compiled.

## 📦 What's Included
* `/blueprints/medical-store-daily-sales-reporter.json`: The complete structural configuration export file for the automation pipeline.

## 🔧 Setup Instructions
1. Open your workflow automation dashboard workspace.
2. Create a new automation project pipeline, access the tool options panel, and choose **Import Blueprint**.
3. Upload the `.json` blueprint configuration file saved from this repository.
4. Configure your active integrations and environmental handles:
   * **Schedule Trigger:** Select your specific time-zone constraints and adjust your target daily cron runtime window.
   * **Google Sheets Modules:** Authenticate your Google Sheet workspace path, connect your database ledger sheet, and match your lookup row column variables.
   * **JavaScript Module:** Review or customize the JavaScript script snippet inside the execution node to correspond exactly with your spreadsheet's column names.
   * **Gmail Module:** Authorize your business email handle or app-specific workspace connection and input your target subscriber distribution email list.
5. Save the scenario modifications and toggle the master automation engine switch to **ON**.

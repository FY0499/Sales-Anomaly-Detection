# Sales Anomaly Detection

I built this n8n workflow to monitor daily sales data, detect unusual changes compared with historical performance, and use AI to explain possible reasons behind the anomaly.

## How it works

1. A scheduled trigger retrieves sales records from Google Sheets.
2. JavaScript calculates the latest sales value, historical average, standard deviation, and deviation score.
3. The workflow flags an anomaly when the absolute deviation is greater than two standard deviations.
4. Google Gemini analyzes the detected change and suggests possible causes and actions to investigate.
5. The result is sent through Telegram with the sales direction, explanation, possible causes, and suggested actions.

## Main features

- Scheduled sales monitoring.
- Historical average and standard deviation calculations.
- Detection of unusual sales increases or decreases.
- AI-generated explanation and possible causes.
- Suggested investigation actions.
- Telegram anomaly alerts.

## Technologies

n8n, Google Sheets, Google Gemini, JavaScript, AI Agent, Telegram, and Schedule Trigger.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Google Sheets, Gemini, and Telegram credentials, then connect your sales sheet and make sure the daily sales values are available in the expected column.

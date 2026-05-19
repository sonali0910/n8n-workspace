# Equity Portfolio Rebalancer – n8n AI Workflow

An AI-powered portfolio rebalancing workflow built with n8n, OpenAI, Google Sheets, Marketstack API, Gmail API, and Pushover.

This workflow automatically:

* Accepts portfolio rebalance requests through an n8n form
* Reads a portfolio from Google Sheets
* Fetches live market prices
* Calculates new portfolio allocations
* Iteratively rebalances the portfolio to match a target allocation
* Updates the spreadsheet with new quantities
* Sends notifications through Gmail and Pushover

---

# 🚀 Features

* AI-driven portfolio rebalancing using OpenAI GPT models
* Automated market price retrieval using Marketstack API
* Google Sheets integration for portfolio tracking
* Email trade summaries via Gmail
* Mobile/Desktop notifications via Pushover
* Iterative validation loop to ensure target allocation is achieved
* End-to-end automation using n8n workflows

---

# 🏗️ Architecture Overview

## Workflow Components

1. **n8n Form Trigger**

   * Accepts user rebalance instructions

2. **OpenAI AI Agent**

   * Interprets the rebalance goal
   * Decides required trades
   * Iterates until allocation target is achieved

3. **Google Sheets Tools**

   * Reads current holdings
   * Updates prices
   * Updates rebalanced quantities

4. **Marketstack API**

   * Fetches latest End-of-Day market prices

5. **Notifications**

   * Gmail sends detailed trade summary
   * Pushover sends concise push notification

---

# 📸 Screenshots

## Workflow Diagram

<img width="1119" height="530" alt="Equity Portfolio Rebalancer Workflow" src="https://github.com/user-attachments/assets/a7270b5a-7515-4ee0-b1c8-24a35debc698" />

---

## Portfolio Rebalance Form

<img width="531" height="359" alt="Portfolio Rebalancer Submit Form" src="https://github.com/user-attachments/assets/1eefb408-34ed-4c53-a450-776d9a9a5983" />

---

## Form Submission Success

<img width="531" height="240" alt="Portfolio Rebalancer Form Submitted" src="https://github.com/user-attachments/assets/c4cf8dbf-f969-4edf-b236-cdedc39939c7" />

---

## Workflow Execution

<img width="1115" height="506" alt="Rebalancer app executions" src="https://github.com/user-attachments/assets/10ed1962-f704-48b2-b7af-bb2853013b22" />

---

## Google Sheets Portfolio

<img width="1118" height="281" alt="Portfolio Spreadsheet" src="https://github.com/user-attachments/assets/8a435bad-0f22-42d6-8220-c91f5653b51f" />

---

## Gmail Notification

<img width="896" height="296" alt="Gmail Notification" src="https://github.com/user-attachments/assets/7c07ee2d-4b06-4a76-af96-0f4a63b48690" />

---

## Pushover Notification

<img width="1117" height="203" alt="Pushover Notification" src="https://github.com/user-attachments/assets/b560060d-69fc-4fad-96af-a78704da22cb" />

---

# ⚙️ Technologies Used

| Technology        | Purpose                |
| ----------------- | ---------------------- |
| n8n               | Workflow orchestration |
| OpenAI GPT-5 Mini | AI decision making     |
| Google Sheets API | Portfolio data storage |
| Marketstack API   | Market price retrieval |
| Gmail API         | Email notifications    |
| Pushover API      | Push notifications     |

---

# 📂 Workflow File

The exported n8n workflow JSON is included in this repository:

```bash
Equity Portfolio Rebalancer.json
```

Import this file directly into your n8n instance.

Workflow source: 

---

# 🛠️ Setup Instructions

## 1. Clone Repository

```bash
git clone https://github.com/your-username/equity-portfolio-rebalancer.git
cd equity-portfolio-rebalancer
```

---

## 2. Import Workflow into n8n

1. Open your n8n instance
2. Click **Import from File**
3. Select:

```bash
Equity Portfolio Rebalancer(1).json
```

---

## 3. Configure Credentials

Create the following credentials inside n8n:

* OpenAI API
* Google Sheets OAuth2
* Gmail OAuth2
* Marketstack API
* Pushover API

Example credentials page:

<img width="1118" height="530" alt="Rebalancer credentials" src="https://github.com/user-attachments/assets/a51f51bf-f699-4752-a1cc-8413e5e00b4f" />

---

## 4. Configure Google Sheet

Create a spreadsheet with columns similar to:

| Ticker | Quantity | Equity ratio | Fixed income ratio | Price | Total Value | New Quantity After Rebalancing | New Total Value |
| ------ | -------- | ------------ | ------------------ | ----- | ----------- | ------------------------------ | --------------- |

---

## 5. Activate Workflow

* Enable workflow
* Open the generated form URL
* Submit rebalance instructions

Example:

```text
Ensure the portfolio is 60% equity and 40% fixed income
```

---

# 🔄 Workflow Logic

The AI Agent performs the following steps:

1. Read portfolio holdings from Google Sheets
2. Fetch latest market prices
3. Update spreadsheet prices
4. Calculate current allocation
5. Determine required trades
6. Update new quantities
7. Re-read spreadsheet to verify allocation
8. Repeat until target allocation is reached
9. Send email and push notification

---

# 📧 Example Output

## Email Summary

```text
Rebalanced portfolio to target 60/40 allocation.

Trades:
- Sell SPY
- Buy BND

Portfolio updated successfully.
```

## Push Notification

```text
Rebalanced to 60/40 — Sell SPY, Buy BND.
```

---

# 🔐 Security Notes

* Never commit API keys or OAuth credentials
* Use environment variables or n8n credential manager
* Restrict Google Sheet access appropriately

---

# 📈 Future Enhancements

* Broker API integration for automated trade execution
* Support for fractional/whole share strategies
* Risk tolerance profiles
* Historical performance analytics
* Multi-account portfolio support
* Real-time market pricing
* Advanced tax-loss harvesting

---

# 🤝 Contributing

Contributions are welcome.

Feel free to fork the repository and submit pull requests.

---

# 📜 License

MIT License

---

# 👨‍💻 Author

Built by Sonali Singla using n8n + OpenAI automation.


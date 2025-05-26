# Joker Bot — Telegram Bot using n8n and Google AI Studio

## Overview

This project is a Telegram Joker Bot that automatically generates and rates funny jokes using n8n workflows integrated with Google AI Studio (Gemini model). It listens to Telegram messages, creates jokes based on the input, and evaluates their humor score.

---

## Features

- Uses **Telegram Trigger** node in n8n to listen to messages.
- Generates jokes with Google Gemini language models.
- Evaluates joke punchlines with AI scoring.
- Fully managed within n8n with no separate code needed.
- Easy to import and set up in your own n8n instance.

---

## Setup Instructions

### 1. Import Workflow

- Download the workflow JSON file (`joker-bot-workflow.json`).
- Open your n8n instance.
- Go to **Workflows > Import from file**.
- Select the downloaded JSON file and import it.

### 2. Configure Credentials

Create the following credentials inside n8n:

- **Telegram API Credential**  
  Obtain your Telegram Bot token from [BotFather](https://telegram.me/BotFather).  
  Add it in n8n under **Settings > Credentials** as a Telegram API credential.

- **Google AI Studio API Credential**  
  Set up your Google AI API access.  
  Add the credentials in n8n under **Settings > Credentials** as Google API credentials.

### 3. Connect Credentials

- In the imported workflow, assign the Telegram API credential to the **Telegram Trigger** node.  
- Assign the Google API credential to the Google Gemini Chat Model nodes.

### 4. Activate the Workflow

- Turn the workflow active in n8n.  
- Your Joker bot should now respond to Telegram messages.

---

## Security Notes

- **Do not commit your API keys or tokens** to GitHub.  
- Store all secret credentials securely using n8n’s credential management or environment variables.

---

## Running n8n

- You can run n8n locally, on your own server, or use a cloud provider.  
- See [n8n documentation](https://docs.n8n.io/getting-started/installation/) for installation and setup guides.

---

## License

This project is licensed under the MIT License — see the LICENSE file for details.

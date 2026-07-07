# Finance App User Guide

Welcome to Finance! This guide will help you understand how to use our application for financial data analysis. You don't need any coding experience to get started.

## Introduction
Finance is a Bloomberg-grade terminal powered by AI, presented as a simple chat interface. It allows you to access institutional-grade financial data, run complex analyses, and create stunning visualizations—all just by asking questions in plain English.

## Adding API Keys (Important Setup)
Before the app can search the internet or run calculations, it needs permission to access certain databases. We do this using "API Keys" (think of them like special passwords).

Here is exactly how to add your API keys:

**Step 1: Get your API Keys**
You will need to create free accounts on two websites to get these keys:
- **Valyu API Key:** Go to [platform.valyu.ai](https://platform.valyu.ai) to get a key for financial data.
- **Daytona API Key:** Go to [app.daytona.io](https://app.daytona.io) to get a key that allows the AI to draw charts and run calculations securely.

**Step 2: Create a Settings File**
1. Open the folder where you downloaded the Finance app on your computer.
2. Find the file named `.env.example`.
3. Copy that file and paste it into the exact same folder.
4. Rename the newly copied file to exactly: `.env.local`

**Step 3: Add Your Keys (Pay Close Attention!)**
1. Open your new `.env.local` file using a simple text editor (like Notepad on Windows, or TextEdit on Mac).
2. Look for the line that says `VALYU_API_KEY=valyu_your_api_key_here`.
   - **IMPORTANT:** You must delete the text `valyu_your_api_key_here` entirely and paste your *real* secret code from Valyu. Do not leave the placeholder text!
3. Look for the line that says `DAYTONA_API_KEY=your_daytona_api_key_here`.
   - **IMPORTANT:** Delete `your_daytona_api_key_here` entirely and paste your *real* secret code from Daytona.
4. Save the file and close it. You are now ready to start the app!

---
**What about OpenAI? (Optional)**
You might notice a line for `OPENAI_API_KEY`. **You do not need to use OpenAI!** If you are getting errors like "Incorrect API key provided" (because you used placeholder text like `sk-your_openai_api_key_here`), or if you don't want to pay for OpenAI, you can completely ignore this line.

Instead of OpenAI, this app fully supports **100% free, private local AI** using a tool called Ollama or LM Studio. If you install Ollama (from [ollama.com](https://ollama.com)), the app will automatically use your computer's free local AI instead of OpenAI, saving you money and avoiding key errors.

---

## Getting Started

You have two ways to start using the Finance App:

### Option 1: Use the Live Demo (Easiest)
If you don't want to run the app on your computer, you can simply open your web browser and navigate to the live demo at:
**[https://finance.valyu.ai](https://finance.valyu.ai)**
*(Note: The live version may require Valyu credits to use).*

### Option 2: Run it Locally on Your Computer (Free/Self-Hosted)
If you want to run the application entirely on your own computer without needing credits, you can start it locally. Ensure you have completed the **Adding API Keys** steps above first. Although this requires using a terminal, it is a very simple process!

**Step 1: Open Your Terminal**
- **On Mac:** Press `Command + Space`, type "Terminal", and hit Enter.
- **On Windows:** Press the `Windows key`, type "cmd" or "Command Prompt", and hit Enter.

**Step 2: Navigate to the App Folder**
You need to tell the terminal to go to the folder where you downloaded the Finance app.
- Type `cd ` (with a space at the end).
- Drag the folder containing the Finance app from your file explorer directly into the terminal window. It will automatically paste the folder path for you.
- Hit Enter.

**Step 3: Start the App**
- Type the following command and hit Enter:
  `npm run dev`
- The terminal will display some loading text. Leave this window open in the background!

**Step 4: Open Your Browser**
Once the app has started in the terminal, open your web browser (like Chrome or Safari) and go to this exact address:
**http://localhost:3000**

You will automatically be logged in and can start chatting! When you are done, you can close the terminal window to stop the application.

## Input Formats
**You do not need to upload Excel files, PDFs, or any other documents.**

The application expects **natural language text** as input. You simply type your questions or requests into the chat box, just as you would when talking to a colleague or a financial analyst.

The application automatically searches and retrieves the necessary data from various sources using the Valyu Search API. These sources include:
- **Live Global Market Data:** Prices, volumes, and technical indicators across global exchanges.
- **SEC Filings Index:** 10-Ks, 10-Qs, 8-Ks, proxy statements, and insider trading reports.
- **Patent Database:** Patents across various jurisdictions.
- **Academic Research:** arXiv papers, Wiley finance journals, and academic publications.
- **Web Search:** Real-time news, social sentiment, and market analysis.

## Core Features
- **SEC Filings Analysis:** Deep dive into company filings like 10-Ks, 10-Qs, and 8-Ks without reading hundreds of pages manually.
- **Market Data:** Access real-time and historical stock prices, trading volumes, and technical indicators.
- **Financial Statements:** Review income statements, balance sheets, and cash flows with automatic calculations.
- **Insider Trading:** Track institutional and insider transactions to see what company insiders are doing.
- **Academic Research:** Access scholarly articles and financial research papers.
- **News & Sentiment:** Get real-time news analysis and understand how it might impact the market.

## Output Formats
Based on your questions, the AI will generate various types of outputs directly in the chat interface:
- **Text Summaries:** Plain-English explanations and direct answers to your financial questions.
- **Interactive Visualizations:** Beautiful, interactive charts, graphs, and dashboards comparing stocks, showing trends, or breaking down financial statements.
- **Advanced Analytics / Code Execution Results:** The AI can write and run Python code behind the scenes to perform complex analyses (like Monte Carlo simulations, backtesting, or calculating specific ratios) and present the final results to you.
- **Data Tables & CSVs:** Structured data that you can easily read, preview, export, or share.

## Example Queries
Here are some examples of what you can ask the AI:
- *"Build a Monte Carlo simulation to predict Tesla's stock price in 6 months"*
- *"Analyze GameStop's latest 10-K filing and extract key financial metrics"*
- *"Research how recent news affects Elon Musk's companies"*
- *"Create an interactive dashboard comparing the 'Magnificent 7' stocks"*
- *"Do an in-depth report on COVID-19's effect on Pfizer with insider trading data"*
- *"Analyze PepsiCo's recent SEC filings and calculate key financial ratios"*

---
Enjoy your simple, yet incredibly powerful financial research experience!

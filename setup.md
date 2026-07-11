# Gen AI Chatbot - Setup Guide

This guide will walk you through setting up the Gen AI Chatbot locally on your machine.

## Prerequisites
- **Node.js 18+**: Download and install from [nodejs.org](https://nodejs.org)
- **Groq API Key**: Get your free API key from [console.groq.com](https://console.groq.com/keys)

## Step 1: Clone the Repository
```bash
git clone https://github.com/johnsikder312-spec/Genai_chatbot.git
cd Genai_chatbot
```

## Step 2: Install Dependencies
Navigate to the backend directory and install dependencies:
```bash
cd groq-chatbot/backend
npm install
```

## Step 3: Configure Environment Variables
1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```
2. Open `.env` and paste your Groq API key:
   ```
   GROQ_API_KEY=gsk_your_api_key_here
   ```

## Step 4: Start the Server
```bash
npm start
```
Or for development with auto-reload:
```bash
npm run dev
```

## Step 5: Use the Chatbot
Open your browser and go to [http://localhost:3000](http://localhost:3000)

## Troubleshooting
- If you get "Missing GROQ_API_KEY", make sure your `.env` file is correctly configured
- If you get a CORS error, make sure you're accessing the app via `http://localhost:3000` and not directly opening `index.html`

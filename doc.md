# Gen AI Chatbot - Documentation

## Project Overview
The Gen AI Chatbot is a production-ready, beginner-friendly AI chatbot powered by Groq's ultra-fast inference API. It features streaming responses, conversation history, and a clean, modern UI.

## Architecture
The project is split into two main parts:
1. **Frontend**: Static HTML/CSS/JS files in the `groq-chatbot/frontend` directory
2. **Backend**: Express.js server in the `groq-chatbot/backend` directory that handles API calls to Groq

## Frontend Files
- `index.html`: Basic structure of the chat UI
- `style.css`: Modern, responsive dark theme using CSS variables
- `script.js`: Chat logic, state management, and streaming response handling

## Backend Files
- `server.js`: Express server with API endpoints for chat and health checks
- `package.json`: Dependencies and scripts for the backend
- `.env.example`: Example environment variables file

## API Endpoints
### POST /api/chat
Accepts a conversation history and returns a streaming AI response.

**Request Body**:
```json
{
  "messages": [
    {"role": "user", "content": "Hello!"},
    {"role": "assistant", "content": "Hi there!"}
  ]
}
```

**Response**: Plain text stream of the AI's reply

### GET /api/health
Returns the server status and current model being used.

## Customization
- **Bot Personality**: Edit the `systemMessage.content` in `server.js`
- **Model**: Set the `GROQ_MODEL` environment variable in `.env`
- **Colors/Theme**: Modify the CSS variables at the top of `style.css`
- **History Limit**: Change `messages.slice(-20)` in `server.js` to adjust how much history is sent to the model
- **Rate Limit**: Modify `RATE_LIMIT` and `RATE_WINDOW_MS` in `server.js`

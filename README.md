# Gemini Chat Application

This is a chat application that integrates Google's Gemini LLM with a web UI. The backend is built with Flask and uses the Gemini Pro model for generating responses.

## Setup

1. Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the root directory and add your Gemini API key:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

## Running the Application

1. Start the Flask server:
   ```bash
   python main.py
   ```

2. The server will start at `http://localhost:8000`

## API Endpoints

- GET `/`: Health check endpoint
- POST `/chat`: Send a message to Gemini
  - Request body: `{"message": "Your message here"}`
  - Response: `{"response": "Gemini's response"}`

## Features

- Real-time chat with Gemini Pro model
- Flask backend with CORS support
- Simple JSON-based API
- Error handling
- Environment variable configuration

## Testing the API

You can test the API using curl:

```bash
# Test the health check endpoint
curl http://localhost:8000/

# Send a message to Gemini
curl -X POST http://localhost:8000/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "What is the meaning of life?"}'
```

## Note

This is the backend part of the application. The frontend needs to be implemented separately to create a complete chat interface. 
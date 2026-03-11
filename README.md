# AI Companion: Iris

This is a personal chatbot project that allows you to create and interact with a customized AI companion named Iris. The project runs entirely on your local machine using an open-source large language model (Ollama), ensuring privacy and full control over your data.

## Features

- **Local Processing:** Runs locally on your computer using Ollama. No internet connection or API fees are required.
- **Custom Persona:** The AI's personality, communication style, and attitude are fully customizable within the application code.
- **Contextual Memory:** Maintains a short-term memory of the conversation context for a more natural and fluid interaction.
- **Concise Responses:** Tuned to provide short, complete, and engaging replies.
- **Web Interface:** A straightforward HTML and JavaScript interface allows for easy conversation through any modern web browser.

## Prerequisites

Before starting, ensure you have the following installed:

- **Python:** Version 3.8 or higher.
- **Ollama:** The application that runs the local language model.
- **Mistral Model:** Required language model, downloadable via Ollama.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Adarsh-Aravind/AI-GF-using-Ollama.git
   cd AI-GF-using-Ollama
   ```

2. Install the necessary Python libraries:
   ```bash
   pip install flask Flask-Cors requests
   ```

3. Download the language model using Ollama:
   ```bash
   ollama pull mistral
   ```

## Usage

1. **Start the server:**
   Open your terminal in the project directory and run the Python application:
   ```bash
   python local_app.py
   ```

2. **Open the interface:**
   With the server running, open the `index.html` file in your preferred web browser to start chatting with Iris.

## Customization

You can personalize the AI's behavior and traits by modifying the `local_app.py` file.

- **Personality:** Modify the `SYSTEM_PROMPT` variable to alter Iris's traits, rules, and fundamental behavior.
- **Response Length:** Adjust the `num_predict` value in the `data` dictionary to control the maximum length of the generated replies.
- **Response Style:** Adjust the `temperature` value (e.g., lower values like 0.1 for concise and deterministic replies, higher values like 0.8 for more creative and varied responses).

## Architecture

The project is structured into two main components:
- **Backend (`local_app.py`):** A Flask-based server that handles API requests from the frontend, maintains conversation history, and communicates with the local Ollama instance.
- **Frontend (`index.html`):** A simple browser interface for chatting, sending messages to the Flask backend via asynchronous JavaScript requests.

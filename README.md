# Voice_assistant
Loki Voice Assistant
This repository contains the code for an AI-powered voice assistant designed with the persona of Loki, the God of Mischief, from the Marvel Universe. The assistant interacts with users through speech, maintaining Loki's characteristic charm, wit, and subtle arrogance.

Features
Loki Persona: The AI is meticulously prompted to embody Loki's personality, including his unique speaking style, philosophical insights, and iconic phrases.

Voice Interaction: Fully voice-enabled, allowing users to speak naturally and receive spoken responses.

Real-time Processing: Utilizes advanced speech-to-text (STT), large language model (LLM) processing, and text-to-speech (TTS) for a fluid conversational experience.

Asynchronous Operations: Built with asyncio for efficient handling of concurrent voice and AI processes.

Technologies Used
Python: The core programming language for the entire application.

LiveKit Agents: A framework for building real-time communication applications, providing:

AutoSubscribe

JobContext

WorkerOptions

cli (for running the application)

llm (for LLM context management)

VoiceAssistant (the main assistant class)

LiveKit Plugins:

openai: Used for Speech-to-Text (STT), Large Language Model (LLM) inference, and Text-to-Speech (TTS).

silero: Used for Voice Activity Detection (VAD) to efficiently detect when speech begins and ends.

python-dotenv: For securely loading environment variables (like API keys) from a .env file.

asyncio: Python's built-in library for writing concurrent code using the async/await syntax.

 Setup and Installation
Follow these steps to get the Loki Voice Assistant running locally.

1. Clone the Repository
First, clone this GitHub repository to your local machine:

git clone https://github.com/YOUR_USERNAME/voice_assistant.git
cd voice_assistant

(Replace YOUR_USERNAME with your actual GitHub username)

2. Create a Virtual Environment
It's highly recommended to use a virtual environment to manage dependencies:

python -m venv venv
# On Windows:
# .\venv\Scripts\activate
# On macOS/Linux:
# source venv/bin/activate

3. Install Dependencies
Install the required Python packages:

pip install -r requirements.txt

(You'll need to create this file first, see step 5)

4. Configure Environment Variables
This project requires API keys for OpenAI and LiveKit. To keep your sensitive information secure, create a .env file in the root directory of your project (the same directory as main.py):

# .env
# Replace with your actual API keys
OPENAI_API_KEY="your_openai_api_key_here"
LIVEKIT_API_API_KEY="your_livekit_api_key_here"
LIVEKIT_API_SECRET="your_livekit_api_secret_here"
LIVEKIT_URL="wss://your-livekit-server-url.livekit.cloud" # Or your self-hosted URL

Important: The .env file is included in .gitignore to prevent it from being accidentally committed to version control.

5. Generate requirements.txt
If you haven't already, generate a requirements.txt file from your current environment. This is crucial for others to install the correct dependencies:

pip freeze > requirements.txt

Make sure to add and commit requirements.txt to your repository:

git add requirements.txt
git commit -m "Add requirements.txt"
git push origin main

How to Run
Once you have set up your environment variables and installed dependencies, you can run the bot:

livekit-cli run main.py

The bot will connect to your LiveKit room, and Loki will greet you!

Future Enhancements
More Dynamic Persona Management: Allow for switching personas or loading them from a configuration.

Memory/Context Persistence: Implement a more robust memory system for longer conversations.

Integration with Tools: Enable Loki to perform actions (e.g., fetch information from the web, set reminders).

Customizable Voice/Speech Models: Allow users to choose different VAD, STT, and TTS models.

Contributing
Contributions are welcome! Please feel free to fork the repository, make changes, and submit pull requests.


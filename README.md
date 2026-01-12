# Jarvis-Voice-Assistant🤖
Jarvis is a end-to-end AI Voice Assistant built in Python. It integrates speech recognition, large language models (LLMs), and speech synthesis to create a real-time conversational agent capable of automating web tasks and providing intelligent responses.

🚀 Core Functionalities
Wake-Word Activation: Optimized to listen for "Jarvis" before triggering active command processing, preserving API resources.

Intelligent Logic Routing:

Deterministic Logic: Instant response for predefined tasks like opening Google, Facebook, LinkedIn, or YouTube.

Generative Brain: Powered by OpenAI's GPT-3.5-Turbo for handling complex, open-ended queries.

Dynamic Music Library: A modular musicLibrary.py mapping voice commands to specific media streams.

High-Fidelity TTS: Utilizes Google Text-to-Speech (gTTS) with pygame for smooth, low-latency audio playback.

🛠️ Technical Architecture
The system follows a standard NLP Pipeline:

Speech Recognition: Uses Google’s Web Speech API via the SpeechRecognition library.

Command Processing: Implements a logical gate that checks for local commands before forwarding requests to the OpenAI API.

Synthesis & Cleanup: Generates a temporary MP3 payload, plays it via the pygame mixer, and ensures system cleanliness by deleting the file immediately after playback.

💻 Tech Stack
Language: Python 3.10+

APIs: OpenAI (GPT-3.5)

Libraries: gTTS, pygame, SpeechRecognition, pyttsx3, webbrowser

Security: python-dotenv (for Environment Variable management)

📦 Installation & Setup
Clone the repository:

Bash

git clone https://github.com/ishikajaiswal657/Jarvis-Voice-Assistant.git
cd Jarvis-Voice-Assistant
Install dependencies:

Bash

pip install -r requirements.txt
Configure API Credentials: Create a .env file in the root directory and add your OpenAI secret key:

Code snippet

OPENAI_API_KEY=your_actual_key_here
Run the Application:

Bash

python main.py
🛡️ Security
This project implements Secret Masking. All sensitive API keys are stored in a .env file, which is excluded from version control via .gitignore. This follows industry-standard security practices to prevent credential leakage.



SanctuaryHealth AI: AI-Enabled Virtual Health Assistant for Refugees
SanctuaryHealth AI is a web-based virtual health assistant designed to provide reliable medical guidance to refugees and displaced communities. By breaking down language and accessibility barriers, this project aims to offer a first line of health support, connecting users to humanitarian aid and promoting well-being in vulnerable populations.

This project is aligned with the UN Sustainable Development Goals, specifically SDG 3 (Good Health and Well-being), SDG 10 (Reduced Inequalities), and SDG 16 (Peace, Justice, and Strong Institutions).

Core Features
🌐 Multilingual Symptom Input: Users can describe their health concerns in their native language via text.

🤖 AI-Powered Triage: A machine learning model analyzes the symptoms and classifies them into three urgency levels: Emergency (Red), Urgent (Yellow), or Self-Care (Green).

💡 Clear Guidance: Provides immediate, actionable advice and first-aid information based on the triage result.

🗺️ Humanitarian Service Locator: Displays a map with nearby clinics and health services run by NGOs and other humanitarian organizations.

🔍 Explainable AI: Builds trust by explaining why a certain recommendation was made based on the user's input.

Project Workflow
(To make this image appear, upload your worlflow.jpg file to your GitHub repository and change the path below to match its location.)
![Workflow Diagram](worlflow.jpg)

Technology Stack
Backend:

Framework: FastAPI

Language: Python

Translation: googletrans library

AI / Machine Learning:

Model: SentenceTransformers for natural language understanding.

Persistence: joblib for saving and loading the trained model.

Frontend:

Framework: Vanilla HTML, CSS, JavaScript

Mapping: Leaflet.js with OpenStreetMap

Setup and Installation
Follow these steps to run the project locally.

1. Prerequisites
Git

Python 3.8+

A code editor like Visual Studio Code

2. Clone the Repository
Bash

git clone https://github.com/Lohith-07-coder/Ai-Health-Assistant-for-Refugees.git
cd Ai-Health-Assistant-for-Refugees
3. Set Up the Backend
Bash

# Create and activate a Python virtual environment
python -m venv venv
# On Windows
.\venv\Scripts\Activate.ps1
# On macOS/Linux
# source venv/bin/activate

# Install the required libraries
pip install -r requirements.txt
4. Train the AI Model
Run the training script once to create the triage_model.pkl file.

Bash

python backend/train_classifier.py
5. Run the Backend Server
Start the FastAPI server from the project's root folder.

Bash

uvicorn backend.app:app --reload
The backend will be running at http://127.0.0.1:8000. You can test it by visiting http://127.0.0.1:8000/docs.

6. Run the Frontend
The easiest way to run the frontend is with the Live Server extension in Visual Studio Code.

Install the "Live Server" extension.

Right-click on the frontend/index.html file.

Select "Open with Live Server".

Your browser will open, and you can now use the application.

How to Use
Select your preferred language from the dropdown menu.

Describe your symptoms in the text box.

Click "Get Help".

The application will provide a color-coded triage level, guidance, and a map of nearby clinics.

Future Work
Integrate a voice-to-text feature for even greater accessibility.

Develop an offline-first mode for use in areas with poor internet connectivity.

Partner with NGOs to integrate live data on clinic availability and services.

Move from the googletrans library to an official, more reliable translation API.

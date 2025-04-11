

```markdown
<h1 align="center">🛡 CyberGuard AI - National Cyber Crime Reporting Portal</h1>
<h3 align="center">AI-Powered Cybercrime Reporting Solution with Gemini Integration</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Security-Level_5_Critical-red" />
  <img src="https://img.shields.io/badge/Compliance-GDPR%2FCCPA-blue" />
  <img src="https://img.shields.io/badge/Powered_By-Google_Gemini_AI-important" />
</p>

---

## 🌟 Overview

*CyberGuard AI* is a state-of-the-art platform designed to transform how cybercrime complaints are reported, tracked, and managed in India. Leveraging the advanced capabilities of Google’s *Gemini AI*, this solution provides an intuitive, secure, and multilingual interface for users to submit cybercrime complaints effortlessly. Whether through text, voice, or file uploads, CyberGuard AI ensures complaints are processed efficiently, categorized accurately, and tracked in real-time—all while prioritizing user privacy and data security.

Built with *Streamlit* for a seamless and visually appealing frontend, and *Supabase* for robust, secure backend data management, CyberGuard AI integrates cutting-edge AI to automate complaint categorization and evidence analysis. This platform is tailored to support India's diverse linguistic landscape, offering complaint submission in *22 Indian languages* plus English, making it accessible to citizens nationwide. Beyond a reporting tool, CyberGuard AI empowers individuals and authorities alike to combat digital crime effectively.

---

## 🚀 Key Benefits

- **🔍 AI-Driven Categorization**: Automatically classifies complaints into categories like Cyber Harassment, Financial Fraud, System Security, Illegal Activities, or Other, ensuring rapid and precise handling by authorities.
- **🧑‍💻 User-Friendly Interface**: Simplifies the reporting process with an easy-to-navigate design, supporting multiple input methods—text, voice (speech-to-text), and file uploads (e.g., PDFs, images).
- **🔐 Secure and Private**: Safeguards sensitive user data with Supabase’s encrypted storage and complies with privacy standards such as GDPR and CCPA.
- **📈 Real-Time Tracking**: Offers transparency with live updates on complaint status, accessible via a unique ticket ID.

CyberGuard AI bridges the gap between citizens and law enforcement, providing a comprehensive, AI-powered solution to address the growing threat of cybercrime in the digital age.

---

## 💥 Key Features

- **✅ Multilingual Support**: Submit complaints in *22 Indian languages* (e.g., Hindi, Tamil, Telugu, etc.) plus English via text, voice (STT), or file uploads (PDFs/Images).
- **✅ AI Categorization**: Uses *Google Gemini AI* to intelligently categorize complaints based on user input and uploaded evidence.
- **✅ Real-Time Ticket System**: Generates unique ticket IDs for each complaint and allows users to track progress instantly.
- **✅ Confirmation Emails**: Sends multilingual confirmation emails with ticket numbers and tailored cybersecurity tips.
- **✅ Speech-to-Text & OCR**: Built-in speech recognition for voice input and Gemini-powered OCR for analyzing uploaded images or documents.
- **✅ Language Translation**: Automatically translates user responses into English for processing while preserving native language input.
- **✅ Admin Dashboard**: Provides authorities with tools to view tickets, update statuses, and filter complaints (simulated in the user-facing dashboard for demo purposes).
- **✅ Streamlit UI**: Features a tabbed interface with themed displays and structured workflows for an enhanced user experience.
- **✅ Supabase Backend**: Ensures secure storage of user data, authentication, and complaint logs.
- **✅ Optional Enhancements**: Supports OTP login and additional email notifications (configurable but not implemented in the base version).

### ➡ Complaint Flow:
👤 *User* → 🔐 *Secure Login* → 🤖 *AI Chatbot or Manual Form* → 🧠 *Automated Categorization* → 📊 *Real-Time Tracking*

---

## 🔑 Core Features

| **Category**         | **Features**                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| *AI Capabilities*    | Complaint Processing • Auto-Categorization • Detail Extraction from Text/Images |
| *User Experience*    | Voice/Text Input • Multi-Language UI • Real-Time Dashboard • Evidence Upload |

---

## 🛠 Tech Stack

```mermaid
graph LR
A[Streamlit UI] --> B[Python Backend]
B --> C[Google Gemini AI]
C --> D[Supabase DB]
D --> E[Encrypted Storage]
```

### Detailed Tech Stack Breakdown:
- **Streamlit**: A Python framework for building an interactive, web-based frontend with minimal code, powering the user interface.
- **Python**: The core programming language handling business logic, integrations, and data processing.
- **Google Gemini AI**: Provides AI-driven features like complaint categorization, text extraction, audio transcription, and image analysis.
- **Supabase**: An open-source Firebase alternative offering a PostgreSQL database for secure data storage, user authentication, and complaint logging.
- **SpeechRecognition**: Python library for converting voice input to text using Google’s STT API.
- **ReportLab**: Generates downloadable PDF reports for submitted complaints.
- **PyDub**: Analyzes audio files to ensure they contain discernible sound before processing.
- **PyAudio**: Facilitates microphone input for speech-to-text functionality.

---

## 🏗 Architecture

```
+---------------------+
|  Presentation Layer |
|    (Streamlit UI)   |
| - Complaint Forms   |
| - Dashboard         |
| - Real-Time Updates |
+---------------------+
          ↓
+---------------------+
|   Business Logic    |
|      (Python)       |
| - User Auth         |
| - Form Processing   |
| - Ticket Management |
+---------------------+
          ↓
+---------------------+
|   AI Processing     |
|    (Gemini AI)      |
| - Categorization    |
| - Text Extraction   |
| - Image Analysis    |
+---------------------+
          ↓
+---------------------+
|  Data Persistence   |
|    (Supabase PG)    |
| - User Data         |
| - Complaint Records |
| - Secure Storage    |
+---------------------+
```

### Architecture Explanation:
1. **Presentation Layer**: The Streamlit UI provides an interactive interface with forms for complaint submission, a dashboard for tracking, and real-time status updates.
2. **Business Logic**: Python scripts manage user authentication, form submissions, ticket generation, and integration with AI and database layers.
3. **AI Processing**: Google Gemini AI handles complaint categorization, extracts details from text/audio/images, and transcribes speech when STT fails.
4. **Data Persistence**: Supabase stores user credentials and complaint data securely, with encrypted fields to protect sensitive information.

---

## 🚀 Quick Start

Follow these steps to set up and run CyberGuard AI locally.

### 1. Install Dependencies
Install the required Python packages and system libraries:

```bash
pip install -r requirements.txt
sudo apt-get install portaudio19-dev  # Required for PyAudio (Linux)
```

On Windows/Mac, ensure `portaudio` is installed via Homebrew (`brew install portaudio`) or a similar package manager.

### 2. Configure Environment
Create a `.env` file in the project root with the following keys:

```env
# .env file
SUPABASE_URL=https://kyuubcusqtbczcexsire.supabase.co
SUPABASE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Imt5dXViY3VzcXRiY3pjZXhzaXJlIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDI5MTk0NjIsImV4cCI6MjA1ODQ5NTQ2Mn0.rntfn9r-1VzKmL0OFG2Y-_JrjFycsuQX525UtTKGPUU
GEMINI_API_KEY=AIzaSyAWQiJDabf7L2Jh28vjg_qBz2LNeoeXSQ4
SMTP_EMAIL=madhurisabale09@gmail.com
SMTP_PASSWORD=argigfabzyogwnyj  # Use an App Password for Gmail
```

Replace the values with your own credentials:
- **Supabase**: Get URL and anon key from your Supabase project settings.
- **Gemini API**: Obtain from Google’s AI platform.
- **SMTP**: Configure with your email provider (e.g., Gmail).

### 3. Launch Application
Run the app using Streamlit:

```bash
streamlit run app.py --server.port 8501
```

Open your browser to `http://localhost:8501` to access the portal.

---

## 🗂 Project Structure

```
CyberGuardAI/
├── app.py              # Main application logic (authentication, UI, AI integration)
├── requirements.txt    # Python dependencies list
├── .env.example        # Template for environment variables
└── README.md           # Comprehensive project documentation
```

### Supabase Schema:
- **users**: Stores user credentials for authentication.
  ```
  id (UUID, primary key)
  username (VARCHAR, unique)
  email (VARCHAR, unique)
  password_hash (VARCHAR)  # Plaintext in demo; hash in production
  ```
- **complaints**: Logs all submitted complaints.
  ```
  ticket_id (VARCHAR, primary key, e.g., CYBER-XXXXXXXX)
  category (VARCHAR, e.g., Financial Fraud)
  status (VARCHAR, e.g., Under Investigation)
  evidence (JSON, stores file metadata)
  data (JSON, raw user input)
  translated_data (JSON, English translations)
  date_filed (TIMESTAMP)
  last_updated (TIMESTAMP)
  ```

---

## 🤖 AI Workflow

Here’s how CyberGuard AI processes a complaint:

> *Example*: User reports "Received a phishing email from a fake bank asking for my account details."
> 1. **Input**: User submits via text, voice, or uploads an email screenshot.
> 2. **Gemini Analysis**: AI analyzes the text/image:
>    - Identifies keywords: "phishing," "fake bank," "account details."
>    - Classifies as "Financial Fraud."
>    - Extracts details: Sender email, content summary.
> 3. **Categorization**: Assigns category "Financial Fraud" with a detailed explanation.
> 4. **Ticket Generation**: Creates a unique ticket ID (e.g., CYBER-ABC12345).
> 5. **Output**: Sends a confirmation email with tips like "Avoid clicking links in unsolicited emails."

This workflow ensures complaints are actionable and well-documented for authorities.

---

## 🌐 Deployment Options

### Streamlit Cloud
Deploy CyberGuard AI effortlessly on Streamlit Cloud:

[![Deploy](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://streamlit.io/cloud)

#### Steps:
1. **Push to GitHub**: Upload the project to a public/private GitHub repository.
2. **Connect to Streamlit Cloud**: Log in to Streamlit Cloud, link your repo via the dashboard.
3. **Configure Secrets**: Add `.env` variables (e.g., `SUPABASE_URL`, `GEMINI_API_KEY`) in Streamlit Cloud’s "Secrets" section.
4. **Deploy**: Click "Deploy" to launch the app; access it via a custom URL.

#### Requirements:
- GitHub account
- Streamlit Cloud account (free tier available)

### Alternative: Docker or VPS
For custom hosting:
1. **Dockerize**: Create a `Dockerfile`:
   ```dockerfile
   FROM python:3.9-slim
   WORKDIR /app
   COPY . /app
   RUN pip install -r requirements.txt
   CMD ["streamlit", "run", "app.py", "--server.port", "8501"]
   ```
2. **Build & Run**: `docker build -t cyberguard-ai . && docker run -p 8501:8501 cyberguard-ai`
3. **VPS**: Deploy on a server (e.g., AWS EC2, DigitalOcean) with public access.

---

## 🔗 Links

- **🎬 Demo Video**: [View on Google Drive](https://drive.google.com/drive/folders/1DyI5qzy40ks3LV69vTq5YpW-f8gLjbCL)
- **Source Code**: [GitHub Repository](#) (Update with your repo link)
- **Official Portal**: [cybercrime.gov.in](https://cybercrime.gov.in) (Reference for real-world use)

---

## 🔌 API Integrations

CyberGuard AI leverages the following APIs and libraries for its smart features:

- **Google Gemini AI**: Powers complaint categorization, text extraction from audio/images, and transcription fallback for speech-to-text.
- **Supabase**: Provides a PostgreSQL database, user authentication, and secure storage for complaint data.
- **SpeechRecognition**: Converts voice input to text using Google’s STT API (requires internet and microphone).
- **ReportLab**: Generates PDF reports summarizing complaints with ticket details.
- **PyDub**: Validates audio files to ensure they contain sound before processing.
- **SMTPLib**: Sends confirmation emails via Gmail’s SMTP server.

These integrations enable automation, multilingual support, and a seamless user experience.

---

<p align="center">
  Built for 🇮🇳 India | Empowering citizens against digital crime 💻🔒
</p>

---

## 🙏 Acknowledgments

- **Google Gemini Team**: For providing the powerful AI capabilities that drive categorization and analysis.
- **Streamlit Developers**: For creating an intuitive framework that simplifies web app development.
- **Supabase Community**: For offering a reliable, open-source backend solution.
- **Python Software Foundation**: For maintaining Python, the backbone of this project.

Special thanks to the open-source community and contributors who inspire innovation in cybersecurity solutions.

---

<p align="center">
  © 2023 CyberGuard AI | All Rights Reserved | A demo project for educational purposes
</p>
```

---

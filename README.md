# Scam Message Investigator
<img width="1333" height="464" alt="image" src="https://github.com/user-attachments/assets/f289e002-2d7a-4bda-9d81-f49d50cc9636" />

## Project Overview

Scam Message Investigator is a Python-based AI application that analyzes suspicious SMS messages, emails, job offers, and online messages using a locally running Gemma 3 1B language model through Ollama.

The application identifies possible scam indicators, explains warning signs, assesses the concern level, and recommends safe actions.

## Features

- Analyze suspicious SMS messages, emails, and online messages.
- Uses Gemma 3 1B through Ollama for local AI inference.
- Identifies possible scam indicators and warning signs.
- Classifies messages into Low Concern, Medium Concern, or High Concern.
- Generates structured investigation reports in JSON format.
- Provides recommended safety actions.
- Includes error handling for API connection and response issues.
- Provides a simple and interactive Streamlit interface.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Streamlit | User interface |
| Ollama | Local AI model execution |
| Gemma 3 1B | Message analysis |
| Requests | HTTP API communication |
| JSON | Structured AI responses |

## Project Structure

```text
Scam_Message_Investigator/
│
├── app.py
├── requirements.txt
└── README.md
```

## System Requirements

- Windows, macOS, or Linux.
- Python 3.10 or newer.
- Ollama installed on the system.
- Gemma 3 1B model downloaded.
- Sufficient RAM and disk space.

## Installation and Setup

### 1. Install Python

Download and install Python from:

https://www.python.org/downloads/

### 2. Install Ollama

Download Ollama from:

https://ollama.com/download

### 3. Download the Gemma Model

Open Command Prompt and execute:

```bash
ollama pull gemma3:1b
```

### 4. Verify the Model

```bash
ollama run gemma3:1b
```

To exit the model, enter:

```text
/bye
```

### 5. Clone the Repository

```bash
git clone <your-repository-url>
```

Navigate to the project folder:

```bash
cd Scam_Message_Investigator
```

### 6. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 7. Run the Application

```bash
python -m streamlit run app.py
```

The application will open in your default web browser.

## Model Configuration

The application uses the following configuration:

```python
MODEL = "gemma3:1b"

OLLAMA_URL = "http://localhost:11434/api/chat"
```

Ensure Ollama is running before starting the application.

## How It Works

1. The user enters a suspicious message into the Streamlit interface.
2. The application sends the message and analysis instructions to the local Ollama API.
3. Gemma 3 1B analyzes the message.
4. The model generates a structured JSON investigation report.
5. Python processes the response.
6. Streamlit displays the concern level, warning signs, summary, and recommended actions.

## Sample Test Cases

| Test Message | Expected Concern |
|---|---|
| Bank account blocked unless OTP is provided | High Concern |
| Work-from-home job requiring registration fees | Medium/High Concern |
| Unexpected lottery prize requiring payment | High Concern |
| College examination schedule notification | Low Concern |
| Parcel delivery message requesting payment through an unfamiliar link | Medium/High Concern |
<img width="1260" height="519" alt="image" src="https://github.com/user-attachments/assets/6380d6b7-82f3-4b45-93b5-6168b099f3d2" />
<img width="1292" height="492" alt="image" src="https://github.com/user-attachments/assets/8fdda681-42b1-4552-a618-3d921237a4aa" />
![Uploading image.png…]()


## Safety and Limitations

- The application provides an AI-generated assessment, not a guaranteed scam verdict.
- It analyzes message text only.
- It does not independently verify URLs or sender identities.
- A Low Concern result does not guarantee that a message is safe.
- Users should verify suspicious communications through official channels.
- Never enter real passwords, PINs, or OTPs during testing.

## Future Enhancements

- URL analysis and suspicious link detection.
- Email scam detection.
- Multilingual message analysis.
- Message history and investigation reports.
- Improved scam classification accuracy.
- Additional security analysis features.

## Author

**Nandhini Sri L V**

B.Sc Computer Science with Artificial Intelligence

## Project Category

Artificial Intelligence | Natural Language Processing | Cybersecurity | Python

https://scam-message-investigator-ekcwyljku33yfgjpf6j39z.streamlit.app/

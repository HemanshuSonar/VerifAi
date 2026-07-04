<div align="center">

# 🔍 VERIFAI
### AI-Powered Misinformation Detection Platform

**Detect fake news, AI-generated images, and manipulated content — with transparent, explainable results.**

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Backend-000000?style=flat&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Ollama](https://img.shields.io/badge/Ollama-Llama%203.2-orange?style=flat)](https://ollama.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[Demo](#-demo) · [Features](#-key-features) · [Tech Stack](#-tech-stack) · [Getting Started](#-getting-started) · [Architecture](#-architecture) · [Contributing](#-contributing)

</div>

---

## 📌 Problem Statement

The rapid growth of digital media and generative AI has made misinformation more convincing and harder to detect. Fake news, AI-generated images, and manipulated content spread quickly across platforms — impacting public trust, elections, financial decisions, and public safety.

Most existing solutions:
- Are **fragmented** across tools
- Focus on only **one content type** (text *or* image, rarely both)
- Return a verdict **without explaining why** — leaving users unable to judge credibility for themselves

**VERIFAI** was built to close that gap.

---

## 💡 Solution Overview

**VERIFAI** is an all-in-one, **explainable AI** platform that verifies both **text and images** to detect misinformation and AI-generated or manipulated content.

Instead of a simple true/false label, VERIFAI provides:

| Capability | Description |
|---|---|
| 📊 **Authenticity Score** | A quantified confidence score instead of a binary verdict |
| 🧠 **Explainable Reasoning** | Human-readable explanation of *why* content was flagged |
| 🌍 **Multilingual Support** | Analyze and translate content across languages |
| 🔗 **Source Cross-Checking** | Verifies claims against trusted, real-world sources |

---

## 🚀 Key Features

- ✅ **Text & Image Verification** — single platform for both content types
- 🤖 **AI-Generated Content Detection** — flags text/images likely produced by generative AI
- 🧬 **Manipulation & Deepfake Detection** — identifies tampered or synthetic media
- 🌐 **Cross-Reference Engine** — validates claims against trusted external sources
- 📈 **Explainable Authenticity Score** — transparent scoring with reasoning, not a black box
- 🌍 **Multilingual Analysis & Translation** — supports non-English content out of the box
- 🔐 **Secure & Scalable Architecture** — built with production-readiness in mind

---

## 🎥 Demo

> Screenshots.

<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/9655e506-1867-490c-a8aa-5d23ff1f3f9b" />
<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/bddb13d1-acd5-4206-a36f-85c633d5b5a3" />
<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/d231b9f2-1100-4579-9638-2969eb40334d" />
<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/02add9e5-bfaf-477d-97ba-0d3ff942cd22" />


🔗 Live Demo: https://verifai-lh2n.onrender.com/
---

## 🏗 Architecture

<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/2879c683-9276-454d-97ac-bb74de69cdb1" />

---

## 🛠 Tech Stack

**Frontend**
- HTML, CSS, JavaScript

**Backend**
- Flask (Python)

**AI / ML**
- Ollama running Llama 3.2 for reasoning and explanation generation

**APIs & Integrations**
- Google Custom Search API — trusted source cross-checking
- Translation API — multilingual support
- Flask-Mail — email notifications

**Content Extraction**
- BeautifulSoup, Trafilatura — web scraping & article extraction

---

## 📂 Project Structure

```
verifai/
├── app.py                  # Flask application entry point
├── config.py                # App configuration
├── requirements.txt          # Python dependencies
├── static/                   # CSS, JS, images
├── templates/                 # HTML templates
├── modules/
│   ├── text_verifier.py       # Text/misinformation analysis
│   ├── image_verifier.py      # Image/deepfake detection
│   ├── cross_reference.py     # Source verification logic
│   └── translator.py          # Multilingual handling
├── utils/
│   └── extractor.py           # Content extraction helpers
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites
- Python 3.10+
- [Ollama](https://ollama.com/) installed locally with the `llama3.2` model pulled
- Google Custom Search API key
- Translation API key

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/HemanshuSonar/VerifAi.git
cd VerifAi

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Pull the required LLM model
ollama pull llama3.2

# 5. Configure environment variables
cp .env.example .env
# Add your API keys and secrets to .env

# 6. Run the application
python app.py
```

The app will be available at `http://localhost:5000`.

### Environment Variables

```
GOOGLE_SEARCH_API_KEY=your_key_here
TRANSLATION_API_KEY=your_key_here
MAIL_USERNAME=your_email
MAIL_PASSWORD=your_password
SECRET_KEY=your_flask_secret_key
```

---

## 🧪 Usage

1. Open the web app and choose **Text** or **Image** verification.
2. Paste text or upload an image.
3. VERIFAI analyzes the content using the LLM pipeline, cross-references trusted sources, and returns:
   - An **authenticity score**
   - A plain-language **explanation**
   - Relevant **source links**

---

## 🎯 Impact

VERIFAI helps to:
- 🧑‍🤝‍🧑 Help users identify and avoid fake news
- 🗳 Protect democratic processes from disinformation
- 💼 Prevent financial fraud driven by fake content
- 🚨 Improve public safety and trust in digital media

---

## 🗺 Roadmap

- [ ] Browser extension for real-time verification
- [ ] Video/deepfake detection support
- [ ] Public REST API for developers
- [ ] Mobile app (iOS/Android)

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Hemanshu Sonar**
📧 hemanshusonar77@gmail.com · 🔗 [LinkedIn](https://www.linkedin.com/in/hemanshusonar/)

</div>

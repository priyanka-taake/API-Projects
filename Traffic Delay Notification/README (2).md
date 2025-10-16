
# 🧠 AI-Powered Smart Delay Notification System

This project automates delay notifications using real-time traffic data and AI-generated, human-like messages.  
It integrates multiple APIs — Google Routes, OpenAI, and SendGrid/Twilio — to provide clear, empathetic, and personalized communication to end-users.

## 🚀 Features

✅ Google Routes API – Fetches live route & traffic data  
✅ Logic Layer – Detects delays based on defined thresholds  
✅ OpenAI Integration – Generates customized, natural messages  
✅ AI Evaluator – Scores message quality for clarity, empathy, professionalism  
✅ Notification API – Sends final messages via email or SMS  
✅ Postman-ready workflow – Easily test and document API flows

## 🧩 Architecture

1️⃣ Google Routes API → Fetch route and traffic data  
2️⃣ Logic Layer → Checks if delay exceeds threshold  
3️⃣ OpenAI → Generates delay message (context-aware)  
4️⃣ AI Evaluator → Scores message quality  
5️⃣ Notification API (SendGrid/Twilio) → Sends to customer

**Tools used:**
- Google Routes API (`directions/v2:computeRoutes`)
- OpenAI GPT-4o-mini
- Postman (testing and workflow management)
- SendGrid / Twilio (notifications)

## ⚙️ Setup Instructions

### 1. Clone this repository
```bash
git clone https://github.com/<your-username>/ai-delay-notifier.git
cd ai-delay-notifier
```

### 2. Create .env file
```bash
GOOGLE_API_KEY=your_google_routes_api_key
OPENAI_API_KEY=your_openai_api_key
SENDGRID_API_KEY=your_sendgrid_key
```

### 3. Install dependencies
For Node.js:
```bash
npm install
```
For Python:
```bash
pip install -r requirements.txt
```

### 4. Run the workflow
```bash
node app.js
# or
python main.py
```

## 🧰 Environment Variables

| Variable | Description |
|-----------|--------------|
| GOOGLE_API_KEY | API key for Google Routes API |
| OPENAI_API_KEY | API key from OpenAI platform |
| SENDGRID_API_KEY | API key for SendGrid |
| TWILIO_SID / TWILIO_AUTH_TOKEN | (Optional) For SMS notifications |

## 🔍 Example Output

```json
{
  "delay_minutes": 18,
  "message": "Hi Alex, your driver might reach 15–20 mins late due to heavy traffic near MG Road. Thank you for your patience!",
  "clarity_score": 9,
  "empathy_score": 8,
  "professionalism_score": 9,
  "notification_status": "sent"
}
```

## 🧾 Documentation & Reflection Notes

- **Prompt Design:** Optimized for short, empathetic responses using GPT-4o-mini  
- **Evaluation Criteria:** clarity, empathy, professionalism  
- **Assumptions:** Delays beyond 10 mins trigger a message  
- **Limitations:** Subjective evaluation; dependent on external APIs

## 🧱 Folder Structure

```
.
├── src/
│   ├── routes_api.py / .js
│   ├── ai_message_generator.py
│   ├── ai_evaluator.py
│   ├── notifier.py
│   └── main.py
├── postman/
│   ├── collection.json
│   └── environment.json
├── .env.example
├── README.md
└── requirements.txt / package.json
```

## 💡 Future Improvements
- Add contextual user history for more personalized messages  
- Dashboard for analytics  
- Scheduled re-checks for ETA  
- Multi-language message generation  

## 🪪 License
MIT License

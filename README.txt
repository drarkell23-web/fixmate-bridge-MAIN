# FixMate Telegram Bridge 🛠️

A minimal, secure Flask backend for the FixMate Maintenance Chatbot.

This bridge safely receives lead data from the FixMate HTML front-end and forwards it to a private Telegram chat using your bot token — without exposing secrets on the client side.

---

## 🧩 Features
- Accepts JSON POST requests at `/send_lead`
- Formats and sends the message to your Telegram bot
- Hides your Telegram token securely on the server
- Works with any front-end (HTML, React, etc.)
- Deployed easily on [Render.com](https://render.com) Free Plan

---

## 🚀 Quick Deploy on Render

1. Push this folder to a new **GitHub repository** (e.g. `fixmate-bridge`).

2. Go to **Render Dashboard → New + → Web Service**.

3. Connect your GitHub repo.

4. Set these options:

| Setting | Value |
|----------|-------|
| **Build Command** | `pip install -r requirements.txt` |
| **Start Command** | `python telegram_bridge.py` |
| **Environment** | `Python 3` |
| **Instance Type** | Free |
| **Region** | Closest to your users |

5. Add **Environment Variables** on Render (optional but safer):
   - `BOT_TOKEN` = your Telegram bot token  
   - `CHAT_IDS` = your Telegram chat IDs (comma-separated)

6. Click **Deploy** and wait 1–2 minutes.

7. Visit your live URL, e.g.  

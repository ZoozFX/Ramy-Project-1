# Kin99 Report & Webhook Service

This project combines:
- A FastAPI webhook to receive data from TradingView.
- An image report generator to parse uploaded HTML files and send visual reports to Telegram.

## 🚀 Endpoints

| Method | Path       | Description                        |
|--------|------------|------------------------------------|
| POST   | `/send`    | Receives TradingView webhook data |
| GET    | `/last`    | Returns the latest webhook data   |
| POST   | `/upload`  | Accepts HTML file and sends image report |

## 🔐 Required Environment Variables (in Render Dashboard)

Go to **Render > Your Service > Environment > Environment Variables**, and add:

| Key             | Example Value                                       |
|------------------|----------------------------------------------------|
| `TELEGRAM_TOKEN` | `7570...yJso`                                       |
| `CHAT_ID`        | `-1002799925948`                                   |
| `SECRET_KEY`     | `YourSuperSecretKey`                               |

## 🛡️ Security Notes

- Secrets are **not stored** in `render.yaml`. 
- They must be added manually via Render Dashboard.
- `/upload` requires `X-Secret-Key` in headers.

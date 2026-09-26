    bot.py
import os
import requests

BOT_TOKEN = os.environ["8619686161:AAEyfJQPMkowak5GCluszGZ9N7lGUQ0QVms"]
CHAT_ID = os.environ["942043461"]

API = f"https://api.telegram.org/bot{BOT_TOKEN}"

def send_message(text):
    requests.post(
        f"{API}/sendMessage",
        data={
            "chat_id": CHAT_ID,
            "text": text
        },
        timeout=20
    )

send_message(
    "✅ AbbasTradeBot چالاکە!\n\n"
    "Support/Resistance Strategy Ready\n\n"
    "🟢 BUY: Resistance + 5\n"
    "🔴 SELL: Support - 5\n\n"
    "15M Confirmation:\n"
    "🟢 Hammer / Bullish Engulfing\n"
    "🔴 Shooting Star / Bearish Engulfing"
)

print("Bot test completed.")

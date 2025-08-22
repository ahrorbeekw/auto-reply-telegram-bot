# 🤖 Avto-Reply Userbot

Bu userbot **[Telethon](https://docs.telethon.dev/)** kutubxonasi
yordamida yozilgan bo'lib, kiruvchi xabarlarga avtomatik tarzda **faqat
bir marta** javob qaytaradi.

------------------------------------------------------------------------

## 📌 Xususiyatlar

-   Har bir foydalanuvchiga faqat **1 marta javob beradi**.\
-   Javob matni: `👋 Salom! Men hozir bandman, keyin yozaman.`\
-   Konsolda foydalanuvchining ismi va unga javob berilganligi haqida
    yozib boradi.

------------------------------------------------------------------------

## ⚙️ O'rnatish

### 1. Repozitoriyani klonlash

``` bash
git clone https://github.com/username/autoreply-userbot.git
cd autoreply-userbot
```

### 2. Virtual muhit yaratish (ixtiyoriy)

``` bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3. Kerakli kutubxonalarni o'rnatish

``` bash
pip install telethon
```

------------------------------------------------------------------------

## 🔑 API ID va API Hash olish

1.  [my.telegram.org](https://my.telegram.org) saytiga kiring.\
2.  `API development tools` bo'limidan yangi **app** yarating.\
3.  `api_id` va `api_hash` ni oling.

------------------------------------------------------------------------

## 🚀 Ishga tushirish

`main.py` faylingizni ishga tushiring:

``` bash
python main.py
```

Konsolda quyidagiga o'xshash yozuv chiqadi:

    🤖 Avto-reply userbot ishga tushdi...

------------------------------------------------------------------------

## 📂 Kod namunasi

``` python
from telethon import TelegramClient, events
import asyncio

api_id = 1234567
api_hash = "YOUR_API_HASH"
session = "my_account"

client = TelegramClient(session, api_id, api_hash)

answered_users = set()

@client.on(events.NewMessage(incoming=True))
async def handler(event):
  sender = await event.get_sender()
  user_id = sender.id

  if user_id == (await client.get_me()).id:
    return

  if user_id not in answered_users:
    await event.reply("👋 Salom! Men hozir bandman, keyin yozaman.")
    answered_users.add(user_id)
    print(f"[AUTO-REPLY] {sender.first_name} ga 1 marta javob berildi.")

print("🤖 Avto-reply userbot ishga tushdi...")
async def main():
  await client.start()
  await client.run_until_disconnected()

asyncio.run(main())
```

------------------------------------------------------------------------

## ⚠️ Eslatma

-   Ushbu kod **faqat userbot sifatida ishlaydi** (Telegram hisobingiz
    bilan ishlaydi).\
-   **Bot token** emas, balki **API ID va API Hash** talab qiladi.\
-   Agar Telegram qoidalarini buzsangiz, akkauntingiz cheklanishi
    mumkin.

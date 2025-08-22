🤖 Telegram Auto-Reply Userbot

Ushbu Userbot Telethon kutubxonasi yordamida yozilgan bo‘lib, xabar kelganda avtomatik tarzda faqat birinchi marta javob beradi.

✨ Xususiyatlari

Har bir foydalanuvchiga faqat 1 marta avtomatik javob qaytaradi.

Xabar yuborgan odamga quyidagi javob qaytariladi:

👋 Salom! Men hozir bandman, keyin yozaman.


Konsolda foydalanuvchiga javob berilgani haqida ma’lumot chiqariladi.

O‘z akkauntingiz orqali ishlaydi (bot emas, userbot).

⚙️ O‘rnatish

Loyihani yuklab oling yoki kodni main.py fayliga saqlang.

Python kutubxonalarini o‘rnating:

pip install telethon


api_id va api_hash ni my.telegram.org
 orqali oling.

api_id = 1234567 joyiga o‘z API IDingizni yozing

api_hash = "YOUR_API_HASH" joyiga o‘z API HASHingizni yozing

Skriptni ishga tushiring:

python main.py


Birinchi marta ishga tushganda telefon raqamingizni va SMS orqali kelgan kodni kiritishingiz kerak bo‘ladi. Shundan keyin my_account.session fayl yaratiladi va qayta kiritish talab qilinmaydi.

📂 Fayl tarkibi

main.py — asosiy userbot kodi

my_account.session — avtorizatsiya fayli (avtomatik yaratiladi)

📌 Izoh

Ushbu userbot faqat bitta javob beradi, ya’ni har bir foydalanuvchi uchun faqat birinchi marta ishlaydi.

Xohlasa, answered_users o‘rniga ma’lumotni fayl yoki baza orqali saqlash mumkin.

✅ Endi skriptni ishga tushirsangiz, siz band bo‘lganda ham odamlar avtomatik javob oladi.

# Bot-Detection-Mouse-Telemetry

Faqat sichqoncha telemetriyasidan va 4 ta oddiy matematik amaldan foydalanadigan, aqlli, kengaytiriladigan va juda engil sinov loyihasi — server tomonidagi chuqur o‘rganishga ehtiyoj yo‘q.

Projekt haqida

Ushbu tizim foydalanuvchilarning tabiiy sichqoncha harakatlariga asoslanib, inson va botlarni ajratib beradi. Serverda ishlaydigan og‘ir mashinani o‘rganish modellari o‘rniga, biz hisoblashlarning katta qismini brauzerda amalga oshiramiz va faqat 2 latent qiymatni backendga yuboramiz.
U nima qiladi:

    Brauzerda sichqoncha telemetriyasini (x, y, dt) kuzatadi.

    ONNX yordamida JavaScriptda siqilgan modelni ishga tushiradi.

    Latent vektor [x1, x2] ni Flask backendga yuboradi.

    Backend 4 ta oddiy matematik amal yordamida bashorat qiladi: inson yoki bot.

    Natijaga qarab cookie o‘rnatadi va ko‘rinishni yangilaydi.

Qanday dasturni ishlatish mumkin:
Step 1: Install Dependencies

`pip install -r requirements.txt`

# Step 2: Flask serverni yurgizing
Option A: With PyTorch model

`python app.py`


# Step 3: Browserda oching

`Visit: http://127.0.0.1:5000`

Sichqonchangizni harakatlantiring — agar harakatlaringiz tabiiy bo‘lsa, siz insonlar uchun mo‘ljallangan sahifaga (human.html) yo‘naltirilasiz!

Talablar umumiy ko‘rinishi

    Python ≥ 3.8

    Flask

    Mashinani o‘rganish versiyasi uchun: PyTorch

    Tahlil uchun: Jupyter, pandas, matplotlib, torch va boshqalar (batafsil requirements.txt faylida)
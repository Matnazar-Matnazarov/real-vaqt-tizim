# Real-Time Systems - Amaliy Ishlar Koleksiyasi

Bu loyiha **Real vaqt tizimlari** fanidan amaliy ishlarni o'z ichiga oladi. Har bir lesson real vaqt rejimida ishlaydigan tizimlarni yaratish va boshqarish bo'yicha turli xil texnologiyalar va yondashuvlarni ko'rsatadi.

## 📋 Loyiha Tuzilishi

```
real-time-systems/
├── lesson_1/          # Timer va Count-Up dasturi
├── lesson_2/          # CPU va RAM real-time monitoring
├── lesson_3/          # FastAPI email sender
├── lesson_4/          # Telegram bot
├── lesson_5/          # Celery cron task scheduler
├── lesson_6/          # Real-time chat (Socket programming)
├── lesson_7/          # Log file monitoring (tail -f)
├── lesson_8/          # WebSocket real-time system metrics
├── lesson_9/          # Arduino multitasking simulation
├── lesson_10/         # IoT sensor simulation dashboard
├── lesson_11/         # RTOS task scheduling simulation
├── requirements.txt   # Asosiy dependencies
└── pyproject.toml     # Project konfiguratsiyasi
```

## 🚀 O'rnatish

### Talablar

- Python 3.12+
- pip yoki uv package manager
- Redis (lesson_5 uchun)
- Arduino IDE (lesson_9 uchun, ixtiyoriy)

### Qadamlar

1. Repositoryni klonlash:
```bash
git clone <repository-url>
cd real-time-systems
```

2. Virtual environment yaratish (tavsiya etiladi):
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# yoki
venv\Scripts\activate     # Windows
```

3. Dependencies o'rnatish:
```bash
pip install -r requirements.txt
```

Yoki `uv` ishlatilsa:
```bash
uv pip install -r requirements.txt
```

## 📚 Darslar Tafsilotlari

### Lesson 1: Timer va Count-Up Dasturi
**Texnologiyalar:** Python (standart kutubxonalar)

Oddiy timer dasturi bo'lib, foydalanuvchi belgilagan vaqtga qadar hisoblaydi. Terminalda real vaqtda vaqtni ko'rsatadi.

**Xususiyatlar:**
- Count-up timer funksiyasi
- Terminal tozalash (cross-platform)
- Formatlangan vaqt ko'rinishi (HH:MM:SS)
- Keyboard interrupt bilan to'xtatish

**Ishga tushirish:**
```bash
cd lesson_1
python main.py
```

---

### Lesson 2: CPU va RAM Real-Time Monitoring
**Texnologiyalar:** Python, Matplotlib, psutil

Sistema resurslarini (CPU va RAM) real vaqtda monitoring qilish va grafik ko'rinishda ko'rsatish.

**Xususiyatlar:**
- Real-time CPU foydalanish monitoring
- Real-time RAM foydalanish monitoring
- Matplotlib bilan animatsiyali grafiklar
- 30 ta oxirgi o'lchovlarni saqlash
- 2 soniyada bir yangilanish

**Ishga tushirish:**
```bash
cd lesson_2
pip install -r requirements.txt
python main.py
```

**Dependencies:**
- `psutil` - Sistema resurslarini o'qish
- `matplotlib` - Grafiklar yaratish

---

### Lesson 3: FastAPI Email Sender
**Texnologiyalar:** FastAPI, SMTP, Jinja2, email-validator

Web interfeys orqali email yuborish tizimi. SMTP orqali email jo'natish va email validatsiyasi.

**Xususiyatlar:**
- FastAPI web framework
- SMTP orqali email yuborish
- Email validatsiyasi
- Background task processing
- Jinja2 template engine
- TLS/SSL xavfsizlik
- **Uvicorn auto-start** - `python main.py` orqali avtomatik ishga tushadi

**Ishga tushirish:**
```bash
cd lesson_3
# .env fayl yaratish kerak (yoki .env.example dan nusxa olish):
# SMTP_HOST=smtp.gmail.com
# SMTP_PORT=587
# SMTP_USER=your_email@gmail.com
# SMTP_PASS=your_app_password
# FROM_NAME=FastAPI Mailer
# FROM_EMAIL=your_email@gmail.com

python main.py
# Yoki an'anaviy usul:
# uvicorn main:app --reload
```

**Dependencies:**
- `fastapi` - Web framework
- `uvicorn` - ASGI server
- `jinja2` - Template engine
- `email-validator` - Email validatsiya
- `environs` - Environment variables

---

### Lesson 4: Telegram Bot
**Texnologiyalar:** Python, aiogram 3.x

Telegram bot yaratish va foydalanuvchi ma'lumotlarini olish.

**Xususiyatlar:**
- aiogram 3.x framework
- Asynchronous bot
- Foydalanuvchi ma'lumotlarini ko'rsatish
- HTML formatlangan javoblar
- Command handlers

**Ishga tushirish:**
```bash
cd lesson_4
# .env fayl yaratish kerak (yoki .env.example dan nusxa olish):
# BOT_TOKEN=your_telegram_bot_token

python bot.py
```

**Dependencies:**
- `aiogram` - Telegram Bot API framework
- `environs` - Environment variables

---

### Lesson 5: Celery Cron Task Scheduler
**Texnologiyalar:** Python, Celery, Redis

Celery yordamida background task scheduling. Redis broker sifatida ishlatiladi.

**Xususiyatlar:**
- Celery task queue
- Redis broker
- Background task execution
- Periodic task scheduling
- Task monitoring

**Ishga tushirish:**
```bash
cd lesson_5
# Redis server ishga tushirish kerak:
# redis-server

# Celery worker ishga tushirish:
celery -A cron_task worker --loglevel=info

# Yoki oddiy ishga tushirish:
python cron_task.py
```

**Dependencies:**
- `celery` - Distributed task queue
- `redis` - Message broker

---

### Lesson 6: Real-Time Chat (Socket Programming)
**Texnologiyalar:** Python, socket, threading

Socket dasturlash orqali real vaqt chat tizimi. Server va mijoz arxitekturasi asosida bir nechta foydalanuvchi o'rtasida xabar almashish.

**Xususiyatlar:**
- Multi-client chat server
- Real-time messaging
- Threading orqali parallel ishlash
- Nickname support
- Thread-safe operations
- Vaqt belgisi bilan xabarlar
- Graceful disconnect handling
- Interactive menu (main.py)

**Ishga tushirish:**
```bash
cd lesson_6

# 1. Server ishga tushirish (birinchi terminal):
python server.py
# Yoki
python main.py  # Menu orqali tanlash

# 2. Mijoz ishga tushirish (ikkinchi terminal):
python client.py
# Yoki
python main.py  # Menu orqali tanlash
```

**Fayllar:**
- `server.py` - Chat serveri (bir nechta mijozlarni qabul qiladi)
- `client.py` - Chat mijoz dasturi
- `main.py` - Interactive menu

**Dependencies:**
- Python standart kutubxonalar (socket, threading)

---

### Lesson 7: Log File Monitoring
**Texnologiyalar:** Python (standart kutubxonalar)

Log faylni real vaqtda monitoring qilish (Linux `tail -f` kabi).

**Xususiyatlar:**
- Real-time log file monitoring
- Fayl o'zgarishlarini kuzatish
- UTF-8 encoding support
- Non-blocking file reading
- Error handling

**Ishga tushirish:**
```bash
cd lesson_7
python main.py
```

---

### Lesson 8: WebSocket Real-Time System Metrics
**Texnologiyalar:** FastAPI, WebSocket, psutil, Jinja2

WebSocket orqali real vaqtda sistema metrikalarini (CPU, RAM, Network) yuborish.

**Xususiyatlar:**
- WebSocket real-time communication
- CPU monitoring (umumiy va per-core)
- RAM monitoring
- Network I/O monitoring
- System load average
- FastAPI WebSocket endpoints
- Jinja2 template rendering
- **Uvicorn auto-start** - `python main.py` orqali avtomatik ishga tushadi

**Ishga tushirish:**
```bash
cd lesson_8
python main.py
# Yoki an'anaviy usul:
# uvicorn main:app --reload

# Browserda: http://localhost:8000
```

**Endpoints:**
- `GET /` - Dashboard (HTML)
- `GET /health` - Health check
- `WebSocket /ws/metrics` - Real-time metrics stream

**Dependencies:**
- `fastapi` - Web framework
- `uvicorn` - ASGI server
- `psutil` - Sistema metrikalari
- `jinja2` - Template engine

---

### Lesson 9: Arduino Multitasking Simulation
**Texnologiyalar:** Arduino, C++

Arduino mikrokontrollerida multitasking simulyatsiyasi. LED blinking va Serial output parallel ishlaydi.

**Xususiyatlar:**
- Non-blocking LED blinking
- Non-blocking Serial output
- `millis()` orqali vaqt boshqaruvi
- Real-time task scheduling
- Wokwi simulator bilan ishlaydi

**Ishga tushirish:**
```bash
cd lesson_9
# Arduino IDE da ochish:
# 1. Arduino IDE ni oching
# 2. sketch.ino faylini oching
# 3. Board va Port ni tanlang
# 4. Upload qiling

# Yoki Wokwi simulator:
# https://wokwi.com da ochish
```

**Fayllar:**
- `sketch.ino` - Arduino sketch kodi

**Dependencies:**
- Arduino IDE yoki Wokwi simulator

---

### Lesson 10: IoT Sensor Simulation Dashboard
**Texnologiyalar:** Python, Tkinter, CSV

IoT sensorlarini (harorat, namlik, bosim) simulyatsiya qilish va real vaqtda grafik ko'rinishda ko'rsatish.

**Xususiyatlar:**
- Real-time sensor data simulation
  - Harorat: 20-32°C
  - Namlik: 35-65%
  - Bosim: 990-1050 hPa (mm sim. ust.)
- Tkinter grafik interfeys
- Real-time graph plotting
- CSV faylga ma'lumotlarni yozish
- Professional dashboard UI
- Java versiyasiga mos layout
- Har 2 soniyada yangilanish

**Ishga tushirish:**
```bash
cd lesson_10
python main.py
```

**Chiqadigan fayllar:**
- `sensor_malumotlari.csv` - Sensor ma'lumotlari (avtomatik yaratiladi)

---

### Lesson 11: RTOS Task Scheduling Simulation
**Texnologiyalar:** Python, heapq, threading

RTOS (Real-Time Operating System) task scheduling mexanizmlarini simulyatsiya qilish.

**Xususiyatlar:**
- EDF (Earliest Deadline First) scheduling
- Priority-based task management
- Heap data structure (heapq)
- Task deadline tracking
- Real-time task execution simulation

**Ishga tushirish:**
```bash
cd lesson_11
python main.py
```

**Algoritmlar:**
- **EDF Scheduling:** Eng yaqin deadline'ga ega task birinchi bajariladi
- **Heap Structure:** O(log n) complexity bilan task tartiblash

---

## 🛠️ Asosiy Texnologiyalar

### Backend Frameworks
- **FastAPI** - Zamonaviy, tez web framework
- **Celery** - Distributed task queue
- **aiogram** - Telegram Bot API framework

### Monitoring va Analytics
- **psutil** - Sistema resurslarini monitoring
- **matplotlib** - Grafiklar va vizualizatsiya
- **plotly** - Interaktiv grafiklar

### Real-Time Communication
- **WebSocket** - Real-time bidirectional communication
- **Socket** - TCP/IP socket programming
- **Threading** - Parallel task execution
- **asyncio** - Asynchronous programming

### Hardware va Embedded
- **Arduino** - Mikrokontroller dasturlash
- **Tkinter** - Desktop GUI framework

### Data Processing
- **pandas** - Data analysis (agar kerak bo'lsa)
- **numpy** - Numerical computing

### Utilities
- **environs** - Environment variables management
- **email-validator** - Email validation
- **jinja2** - Template engine

## 📦 Dependencies

Barcha kerakli kutubxonalar `requirements.txt` faylida mavjud:

```bash
pip install -r requirements.txt
```

Asosiy dependencies:
- `fastapi>=0.118.0`
- `uvicorn>=0.37.0`
- `aiogram>=3.22.0`
- `celery[redis]>=5.5.3`
- `matplotlib>=3.10.6`
- `psutil>=7.1.0`
- `plotly>=6.3.0`
- `environs>=14.3.0`
- `email-validator>=2.3.0`

## 🔧 Konfiguratsiya

Ba'zi lessonlar `.env` fayl talab qiladi. `.env.example` fayllar mavjud:

### Lesson 3 (Email Sender)
```env
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password
FROM_NAME=FastAPI Mailer
FROM_EMAIL=your_email@gmail.com
```

**Eslatma:** Gmail uchun App Password yaratish kerak:
1. Google Account → Security → 2-Step Verification
2. App passwords → Generate new password
3. Yaratilgan parolni `SMTP_PASS` ga yozing

### Lesson 4 (Telegram Bot)
```env
BOT_TOKEN=your_telegram_bot_token
```

**Eslatma:** Bot token olish uchun [@BotFather](https://t.me/BotFather) ga murojaat qiling.

### Lesson 5 (Celery)
Redis server ishga tushirilgan bo'lishi kerak:
```bash
redis-server
```

## 📝 Foydalanish Misollari

### Real-Time Monitoring
```bash
# CPU/RAM monitoring
cd lesson_2 && python main.py

# System metrics via WebSocket
cd lesson_8 && python main.py
```

### Real-Time Communication
```bash
# Chat server (birinchi terminal)
cd lesson_6 && python server.py

# Chat client (ikkinchi terminal)
cd lesson_6 && python client.py
```

### IoT va Sensorlar
```bash
# IoT sensor simulation
cd lesson_10 && python main.py
```

### Task Scheduling
```bash
# RTOS task scheduling
cd lesson_11 && python main.py

# Celery cron tasks
cd lesson_5 && celery -A cron_task worker
```

### Web Services
```bash
# Email sender
cd lesson_3 && python main.py

# System metrics dashboard
cd lesson_8 && python main.py
```

## 🏗️ Loyiha Arxitekturasi

Loyiha modulli tuzilishga ega, har bir lesson mustaqil ishlaydi:

```
┌─────────────────────────────────────┐
│     Real-Time Systems Project       │
├─────────────────────────────────────┤
│                                     │
│  ┌──────────┐  ┌──────────┐        │
│  │ Lesson 1 │  │ Lesson 2 │  ...   │
│  │  Timer   │  │ Monitor  │        │
│  └──────────┘  └──────────┘        │
│                                     │
│  ┌──────────┐  ┌──────────┐        │
│  │ Lesson 3 │  │ Lesson 4 │  ...   │
│  │  Email   │  │   Bot    │        │
│  └──────────┘  └──────────┘        │
│                                     │
│  ┌──────────┐  ┌──────────┐        │
│  │ Lesson 6 │  │ Lesson 8 │        │
│  │   Chat   │  │ WebSocket│        │
│  └──────────┘  └──────────┘        │
│                                     │
│  ┌──────────┐  ┌──────────┐        │
│  │ Lesson 10│  │ Lesson 11│        │
│  │   IoT    │  │   RTOS   │        │
│  └──────────┘  └──────────┘        │
└─────────────────────────────────────┘
```

## 🎯 Darslar Ro'yxati

| Lesson | Nom | Texnologiyalar | Status |
|--------|-----|----------------|--------|
| 1 | Timer va Count-Up | Python | ✅ |
| 2 | CPU/RAM Monitoring | Python, Matplotlib, psutil | ✅ |
| 3 | FastAPI Email Sender | FastAPI, SMTP | ✅ |
| 4 | Telegram Bot | aiogram | ✅ |
| 5 | Celery Cron Tasks | Celery, Redis | ✅ |
| 6 | Real-Time Chat | Socket, Threading | ✅ |
| 7 | Log File Monitoring | Python | ✅ |
| 8 | WebSocket Metrics | FastAPI, WebSocket | ✅ |
| 9 | Arduino Multitasking | Arduino, C++ | ✅ |
| 10 | IoT Sensor Dashboard | Tkinter, CSV | ✅ |
| 11 | RTOS Scheduling | Python, heapq | ✅ |

## 🤝 Yordam va Qo'llab-quvvatlash

Muammo yoki savol bo'lsa:
1. Issue ochish
2. Pull request yuborish
3. Documentation yaxshilash

## 📄 Litsenziya

Loyiha `LICENSE` faylida ko'rsatilgan litsenziya ostida tarqatiladi.

## 👨‍💻 Muallif

**Urganch Davlat Universiteti**  
Real vaqt tizimlari fanidan amaliy ishlar

## 🎯 Kelajakdagi Rejalar

- [x] Lesson 6 va 9 ni qo'shish
- [ ] Docker containerization
- [ ] CI/CD pipeline
- [ ] Unit testlar qo'shish
- [ ] API documentation (Swagger/OpenAPI)
- [ ] Performance optimization
- [ ] Real-time dashboard birlashtirish
- [ ] More Arduino examples
- [ ] MQTT integration for IoT

## 📊 Statistika

- **Total Lessons:** 11
- **Technologies:** 15+
- **Lines of Code:** 2000+
- **Dependencies:** 90+
- **Programming Languages:** Python, C++ (Arduino), HTML/CSS/JS

## 🔗 Foydali Havolalar

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [aiogram Documentation](https://docs.aiogram.dev/)
- [Celery Documentation](https://docs.celeryq.dev/)
- [Arduino Reference](https://www.arduino.cc/reference/)
- [Socket Programming Guide](https://docs.python.org/3/library/socket.html)

---

⭐ Agar loyiha foydali bo'lsa, star qo'yishni unutmang!

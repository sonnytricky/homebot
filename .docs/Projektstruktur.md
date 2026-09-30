```txt
homebot/
├── src/
│   ├── core/
│   │   ├── config.js         # Lädt .env & allgemeine App-Einstellungen
│   │   ├── logger.js         # Zentrales Logging (z.B. mit Winston oder simplem Console-Wrapper)
│   │   ├── scheduler.js      # Plant Jobs/Cron-Tasks (z.B. node-cron)
│   │   ├── moduleLoader.js   # Lädt dynamisch alle Module aus /modules
│   │   └── bot.js            # Telegram-Bot Setup (z.B. telegraf oder node-telegram-bot-api)
│   │
│   ├── modules/              # Jedes Feature ist ein isoliertes Modul
│   │   ├── garbage/
│   │   │   ├── index.js      # Exportiert Modul-Definition (Cron-Jobs + Telegram-Commands)
│   │   │   └── calendar.js   # Spezifische Logik (Müllabfuhr-Termine)
│   │   │
│   │   ├── backup/
│   │   │   ├── index.js
│   │   │   └── rsync.js      # SSH / rsync Ausführung
│   │   │
│   │   └── weather/
│   │       └── index.js      # Wetter-API Abfrage
│   │
│   └── index.js              # Einstiegspunkt: Startet Bot, Loader & Scheduler
│
├── .env.example              # Vorlage für Secrets
├── Dockerfile                # Image-Definition
├── docker-compose.yml        # Lokaler/Server Container Start
└── package.json
```

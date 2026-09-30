# Wie ich mir das vorstelle:

- auf Githab eine eigene Repo erstellen die nur für das image des Botes zuständig ist.
- das images soll dann in einem docker-compose verwendet werden können.
- so dass der eigentliche **modulare** Bot unhabhängig vbom image in einer eigenen Repo erstellt wird, (siehe unten) aber statt ts nehme ich js

```text
bot/
├── core/
│   ├── scheduler.ts
│   ├── events.ts
│   ├── logger.ts
│   └── config.ts
│
├── modules/
│   ├── garbage/
│   │   ├── index.ts
│   │   └── calendar.ts
│   │
│   ├── backup/
│   │   └── index.ts
│   │
│   ├── weather/
│   │   └── index.ts
│   │
│   └── system/
│       └── index.ts
│
├── bot/
│   └── telegram.ts
│
├── Dockerfile
└── docker-compose.yml
```

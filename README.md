# Workout Tracker — Архитектурный паспорт

Архитектурный паспорт мобильного приложения для трекинга тренировок (offline-first, синхронизация с сервером).

## Структура репозитория

```
workout-tracker-arch-passport/
├── README.md
├── docs/architecture/
│   ├── ADR-001.md             # Выбор архитектуры, критерии, риски
│   ├── Container.png          # C4: Container
│   ├── System Context.png     # C4: System Context
│   ├── openapi.yaml           # REST API спецификация (10 endpoints)
│   └── er-diagram.mmd         # ER-диаграмма (Mermaid)
└── .gitignore
```

## Архитектурное решение

**Модульный монолит (сервер) + Offline-first мобильный клиент**

Обоснование — в [ADR-001.md](docs/architecture/ADR-001.md).

## Ключевые артефакты

| Артефакт | Файл | Описание |
|----------|------|----------|
| ADR | [ADR-001.md](docs/architecture/ADR-001.md) | Выбор архитектуры, критерии качества, риски |
| C4 | [c4-diagram.drawio](docs/architecture/c4-diagram.drawio) | System Context + Container диаграммы |
| OpenAPI | [openapi.yaml](docs/architecture/openapi.yaml) | 10 REST endpoints, схемы данных, JWT auth |
| ER | [er-diagram.drawio](docs/architecture/er-diagram.drawio) | 10 сущностей, связи |

## Предметная область

- Пользователи, программы тренировок, упражнения
- Проведение тренировок: подходы, веса, повторения
- История тренировок, статистика, прогресс
- Offline-first: локальная запись + фоновая синхронизация

## Ресурсы

- [C4 Model](https://c4model.com)
- [OpenAPI Specification](https://swagger.io/specification)
- [draw.io](https://app.diagrams.net)
- [Mermaid](https://mermaid.js.org)

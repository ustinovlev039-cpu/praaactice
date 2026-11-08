# DefectDojo: учёт результатов проверок

## Схема

```mermaid
flowchart LR
    n0["Отчёты анализаторов"]
    n1["Импорт в DefectDojo"]
    n2["Продукт и engagement"]
    n3["Findings и разбор"]
    n0 --> n1 --> n2 --> n3
```

## Что сделал

- Развернул DefectDojo с Docker Compose.
- Создал продукт NetTool и engagement для результатов статического анализа.
- Проверил состояние сервисов и готовность импорта отчётов.

# Службы Windows и Unquoted Service Path

## Схема

```mermaid
flowchart LR
    n0["Service Control Manager"]
    n1["Путь к бинарю и ACL"]
    n2["Процесс службы"]
    n3["Журналы Windows"]
    n0 --> n1 --> n2 --> n3
```

## Что сделал

- Настроил учебную службу Windows и разобрал Unquoted Service Path.
- Проверил путь запуска, разрешения каталогов и контекст службы.
- Исправил путь, ограничил права и повторил проверку.

# Драйверы, DLL Hijacking и Side-Loading

## Схема

```mermaid
flowchart LR
    n0["Учебное приложение"]
    n1["Порядок поиска DLL"]
    n2["Загруженный модуль"]
    n3["Procmon и Sysmon"]
    n0 --> n1 --> n2 --> n3
```

## Что сделал

- Исследовал драйверы Windows и загрузку DLL учебным приложением.
- Воспроизвёл DLL Hijacking и DLL Side-Loading на подготовленном стенде.
- Разобрал порядок поиска библиотек и файловые операции в Process Monitor.

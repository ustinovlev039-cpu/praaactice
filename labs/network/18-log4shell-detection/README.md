# Log4Shell: сетевое обнаружение

## Схема

```mermaid
flowchart LR
    client["Учебный узел / генерация сценария"] --> router["MikroTik"]
    router --> target["Учебный целевой узел"]
    router -. "копия трафика" .-> ids["Suricata / PT Open Rules"]
    ids --> eve["eve.json / EveBox"]
```

## Что сделал

- Настроил зеркалирование трафика с MikroTik на Suricata, подключил PT Open Rules и EveBox.
- Воспроизвёл учебный сценарий Log4Shell.
- Сопоставил сработавшую сигнатуру с HTTP-запросом и сетевым потоком.

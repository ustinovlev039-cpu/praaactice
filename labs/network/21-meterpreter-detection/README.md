# Metasploit и обнаружение Meterpreter

## Схема

```mermaid
flowchart LR
    client["Учебный узел / генерация сценария"] --> router["MikroTik"]
    router --> target["Учебный целевой узел"]
    router -. "копия трафика" .-> ids["Suricata / PT Open Rules"]
    ids --> eve["eve.json / EveBox"]
```

## Что сделал

- Воспроизвёл учебный сценарий Metasploit/Meterpreter в изолированной сети.
- Нашёл срабатывание Suricata в EveBox и разобрал сигнатуру и параметры потока.

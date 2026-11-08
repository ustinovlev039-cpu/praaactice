# Динамическая адресация DHCP

## Схема

```mermaid
flowchart LR
    n0["DHCP-клиент"]
    n1["MikroTik / DHCP"]
    n2["Пул и аренды"]
    n0 --> n1 --> n2
```

## Что сделал

- Настроил DHCP-сервер MikroTik, пул адресов, шлюз и DNS.
- Проверил выдачу аренды и разобрал обмен Discover, Offer, Request и ACK.
